# Mexican-ID complementary dataset: field coverage

[Mexico catalog](README.md) · [Machine-readable field inventory](complementary-fields.yaml)

Reviewed 2026-11-11 against the current photo generator’s v2 export and the 25 Mexican
credential families already in this catalog. This is a requirements inventory and
proposed schema, not a generated identity dataset or a claim that every Mexican ID
edition has been exhaustively audited. State/local credentials and historical editions
need explicit profiles. Supporting civil and fiscal fields are included conditionally.
The inventory also adds gaps for disability, pensioner and maritime identity credentials
that are not separate families in the original 25-item index.

The live Hugging Face card confirms layout v2. Its Dataset Viewer returned HTTP 500
during this review, so per-row completeness and population counts were not measured.
The classifications below are based on the verified export code and are conditional
on the value actually being present in a source row.

## Categories

| Code | Display name | Meaning |
| --- | --- | --- |
| `ready` | Ready | A source value/asset is present and can be reused directly. |
| `transform_code` | Derivable — code | Existing input can be deterministically mapped, formatted or rendered. |
| `transform_ai` | Transformable — AI | Existing descriptions can be rewritten or summarized without inventing identity facts. |
| `missing` | Missing — new input | A new personal fact, registry value, configuration/profile or asset is needed. |

Availability and generation method are separate axes. Names and addresses remain
**Missing** even if an LLM can invent them. CURP and MRZ remain **Missing** until their
absent inputs are created, even though their later generation uses code. A static issuer
label is missing from the portrait row but can simply come from a template profile.

Ready appearance values are the generator’s intended selections, not measured or
medically verified attributes. For legacy/partial rows, a value marked ready here may
still be unavailable. An absent birthmark field does not establish “no birthmarks.”

## Field inventory

The paths below are proposed fields in the new dataset. `parameters.*` refers to the
JSON object obtained by parsing the photo dataset’s parameters column. The `metadata`
group inside those parameters holds appearance selections, while the separate metadata
column holds seeds and execution history.
## Ready

| Proposed field | Existing source or completion method | Constraint |
| --- | --- | --- |
| `source.photo_id` — Photo dataset row ID | id | Use the complete session UUID/portrait-stem ID, not metadata.id alone. |
| `assets.portrait_original` — Original portrait | image | Asset is available; acceptance by a particular ID photo specification is not established. |
| `assets.portrait_transparent` — Transparent portrait | image_transparent | Asset is available; compose onto the document-specific photo background where needed. |
| `person.age_at_portrait` — Selected portrait age | parameters.age | Age is a synthetic prompt input. It has no defined civil reference date; age 100 represents the sampler’s 100+ bucket. |
| `appearance.gender_presentation` — Selected gender presentation | parameters.gender | Not an authoritative sex marker or a legal gender-identity declaration. |
| `appearance.race_ethnicity` — Selected race/ethnicity/ancestry label | parameters.race_ethnicity | Not nationality, citizenship, or Indigenous/Afromexican self-identification. |
| `appearance.eye_color` — Selected eye color | parameters.eyes.color | Conditional: omitted for some opaque-eye profiles and unknown in legacy rows. |
| `appearance.hair_color` — Selected hair color | parameters.hair.color | Conditional: unused hair color is omitted for bald subjects. |
| `appearance.skin_tone` — Selected skin tone | parameters.skin.tone | An intended appearance description, not a verified observation. |
| `appearance.face_shape` — Selected face outline | parameters.face.shape | May require a document-specific vocabulary before printing. |
| `appearance.build` — Selected visible build | parameters.build | Describes face/neck/shoulder appearance, not measured weight or stature. |
| `appearance.distinguishing_marks` — Selected birthmark and other appearance descriptions | parameters.skin.birthmark; parameters.face.detail; parameters.metadata.body_detail | Only stored selections are available. Absence of a field does not certify absence of marks. |

## Derivable — code

| Proposed field | Existing source or completion method | Constraint |
| --- | --- | --- |
| `person.person_id` — Stable complementary person ID | UUID/hash from source.photo_id and a dataset namespace | A new key can be deterministically generated without inventing biographical facts. |
| `assets.portrait_for_template` — Document-size portrait asset | Decode, resize, crop and composite image/image_transparent with profile.photo_spec | A crop cannot remove headwear or guarantee compliance; reject or regenerate incompatible portraits. |
| `assets.portrait_secondary` — Secondary or grayscale portrait | Resize, grayscale, opacity/compositing from the same portrait | Use only where the selected document edition has a secondary portrait; no authentication claim. |
| `appearance.eye_color_code` — Document vocabulary for eye color | Dictionary mapping from appearance.eye_color | Missing if eye color is absent; use the issuer/edition vocabulary. |
| `appearance.hair_color_code` — Document vocabulary for hair color | Dictionary mapping from appearance.hair_color and gray descriptors | Do not supply an invented color for a hairless/unknown row. |
| `appearance.skin_tone_code` — Tez / complexion vocabulary | Dictionary mapping from appearance.skin_tone | Explicit mapping policy; not a race inference. |
| `appearance.face_shape_code` — Face-outline vocabulary | Dictionary mapping from appearance.face_shape | Code can localize or coarsen the selected outline. |
| `appearance.build_code` — Complexión vocabulary | Dictionary mapping from appearance.build.category | A declared synthetic description, not a BMI/weight calculation. |
| `appearance.wears_glasses_in_portrait` — Visible eyewear selection flag | Boolean from parameters.metadata.glasses / eyewear_instruction | Only describes the sampled photo; not a requirement to wear corrective lenses while driving. |
| `person.age_band` — Portrait-age band | Bucket parameters.age | Reference is portrait age, not age on a future issuance date. |
| `eligibility.age_thresholds_at_portrait` — Age-only eligibility flags | Compare parameters.age to profile thresholds | For example 60+ for INAPAM. This is not a full legal-eligibility determination. |

## Transformable — AI

| Proposed field | Existing source or completion method | Constraint |
| --- | --- | --- |
| `appearance.distinguishing_marks_es` — Natural-language señas particulares | Rewrite stored birthmark location/size, facial detail and visible body-detail selections into Spanish | Do not add marks or diagnose conditions. A controlled dictionary/template may replace the LLM later. |
| `appearance.facial_description_es` — Natural-language facial description | Summarize stored face, nose, ears, eyes and skin descriptors | Describe selected features rather than inventing biography or medical evidence. |
| `appearance.hair_description_es` — Natural-language hair and facial-hair description | Rewrite stored hair style, baldness, graying and facial-hair selections | Restrict the output to supplied values; use unknown when the record lacks them. |

## Missing — new input

| Proposed field | Existing source or completion method | Constraint |
| --- | --- | --- |
| `person.given_names` — Given names | New fictional-name source/sampler; optionally an LLM backed by a name catalog | Appearance, gender presentation and age do not contain a person’s name. |
| `person.first_surname` — First surname | New fictional-name source/sampler | Preserve compound surnames and cultural naming variants. |
| `person.second_surname` — Second surname | New fictional-name source/sampler; nullable | Do not require two surnames for every identity, especially foreign-document holders. |
| `person.birth_date` — Exact date of birth | Sample a calendar date consistent with age_at_portrait and an explicitly chosen identity reference date | Age is partial evidence, not an exact date. Save birth date once and reuse it across documents. |
| `person.birth_country` — Country of birth | New geographic/person-history input | Cannot infer from race/ethnicity or from the fact that a document is Mexican-issued. |
| `person.birth_state` — Birth state/entity or foreign-place representation | New geographic/person-history input | Needed for civil text and some identifier rules; distinct from residence and issuing state. |
| `person.birth_municipality` — Birth municipality/locality | New geographic/person-history input | Link to the chosen birth state/country. |
| `person.nationalities` — Nationality/citizenship | New person-history input with document eligibility constraints | Mexican passports and Mexican-issued foreign-resident cards require different holder profiles. |
| `person.document_sex_marker` — Document sex marker | Explicit fictional identity choice and document-edition mapping | Do not automatically map woman/man presentation to an authoritative sex field. |
| `person.gender_identity_declaration` — Gender-identity declaration, where supported | Explicit synthetic self-declaration and edition policy | Separate from presentation and the document sex marker. |
| `person.community_self_identification` — Indigenous/Afromexican self-identification, where supported | Explicit synthetic self-declaration | Not recoverable from the sampled ancestry label or skin tone. |
| `person.marital_status` — Marital status, where applicable | New person-history input | Not present in a headshot. |
| `person.occupation` — Occupation or activity | New person-history input | A garment such as a chef jacket or scrubs is not occupational evidence. |
| `address.country` — Residential country | New address source/sampler | Consular credentials may use an address outside Mexico. |
| `address.state` — Residential state/entity | New geographically consistent address input | Distinct from birth and issuance locations. |
| `address.municipality` — Municipality/alcaldía | New geographically consistent address input | Use an address catalog, not appearance inference. |
| `address.locality` — Locality/city | New geographically consistent address input | Retain foreign-address support. |
| `address.neighborhood` — Colonia/neighborhood | New geographically consistent address input | Nullable according to local/foreign address structure. |
| `address.postal_code` — Postal code | New address catalog input | Validate compatibility with state, municipality and neighborhood. |
| `address.street` — Street name/type | New address source/sampler | Prefer structured address components. |
| `address.exterior_number` — Exterior/building number | New address sampler | Allow jurisdiction-specific values such as S/N. |
| `address.interior_number` — Interior/unit number | New address sampler; nullable | Preserve absent versus unknown. |
| `person.contact` — Telephone/email, if required | New fictional-contact input | Not a universal printed-ID requirement. |
| `person.emergency_contact` — Emergency contact name, relationship, phone and optional address | New related-person/contact input | Not inferable from the portrait; coordinate related records. |
| `person.guardians` — Parent/guardian identity and relationship, if required | New related-person/civil-history input | Needed for some minor/supporting-document profiles; current portraits are adults only. |
| `person.height_cm` — Measured/synthetic stature | New explicitly synthetic numerical sample | A headshot has no reliable full-body scale. |
| `person.weight_kg` — Measured/synthetic weight | New explicitly synthetic numerical sample | Visible build does not determine kilograms or BMI. |
| `person.blood_group_rh` — Blood group and Rh, where required | New independent synthetic health input | Not inferable from appearance, ancestry, or condition prompts. |
| `person.allergies` — Allergy information, where required | New independent synthetic health input | Not contained in the image. |
| `person.organ_donation_consent` — Organ-donation declaration, where required | Explicit fictional consent value | Not an appearance-derived property. |
| `person.driving_restrictions` — Recorded driving restrictions/medical assessment | New synthetic assessed-status input and issuer rules | Do not infer a driving restriction or permission from glasses, blindness or syndrome prompts. |
| `assets.holder_signature` — Handwritten holder-signature image | New synthetic signature generator/asset source, after selecting a name | A name can condition a new signature but cannot recover a missing signature from the portrait. |
| `assets.fingerprints` — Fingerprint image/template, where required | Independent synthetic biometric assets | Not derivable from facial photographs. |
| `assets.iris` — Iris capture/template, only where the selected profile requires it | Independent synthetic biometric assets | A 512-pixel headshot or eye-color string is not a proper iris acquisition; do not assume universal requirement. |
| `civil.birth_registration` — Acta, book, folio, registry office, year and registration locality | New civil-record fixtures | Needed for supporting civil documents and source-document provenance, not every card. |
| `civil.nationality_document` — Naturalization/nationality certificate reference, if applicable | New civil-history fixtures | Conditional on the person/document profile. |
| `identifiers.curp` — CURP | Compute synthetic structure after selecting names, birth date, recorded sex and birthplace; supply synthetic allocation component and check digit | Missing now. Predictable structure does not establish an officially assigned RENAPO identity. |
| `identifiers.rfc` — RFC, if required by a selected profile/supporting fiscal document | Generate a synthetic identifier after names/DOB and an allocation policy are available | Missing now; do not equate a generated homoclave with a SAT registration. |
| `identifiers.nss` — NSS/health identifier | New synthetic affiliation/registry input; optional format/check-digit logic | Not recoverable from age or from a portrait. |
| `document.profile` — Document family, issuer, jurisdiction, edition and valid-from version | Template/profile catalog | Missing from photo data but normally provided by rendering configuration, not invented per portrait. |
| `document.number` — Passport/license/card/document number | New synthetic issuer-specific numbering policy | Treat as issuer-assigned; do not claim it is random or computable from identity without evidence. |
| `document.issue_date` — Issue date | New document-event input | Photo image_requested_at is not an official issue date. |
| `document.expiration` — Expiry date and validity kind | New document-event input plus profile validity rules | Support fixed expiry, indefinite validity, no-expiry and unknown as distinct cases. |
| `document.issue_place` — Place of issue | Issuer/profile and new issuance-event input | Distinct from residence and birth location. |
| `document.registration_or_enrollment` — Registration/enrollment number and date/year | New synthetic issuer registry input | Applies to consular, military and other program-specific cards. |
| `document.renewal_history` — Renewal/replacement count and previous-document references | New coherent document-event history | Do not independently randomize history-dependent fields. |
| `document.observations` — Restrictions, status legends and endorsements | Profile vocabulary plus new document-status inputs | Not every legend applies to every document family. |
| `voter.clave_de_elector` — Clave de elector | New identity inputs plus version-specific issuer/allocation rules | Not present in photo data; some structure may become computable later. |
| `voter.cic` — CIC identifier | New synthetic INE control identifier | Not the same as OCR or clave de elector. |
| `voter.ocr_identifier` — Printed OCR/control identifier | New synthetic INE control identifier and edition rules | OCR is a field name here; recognizing letters in an image does not create this ID. |
| `voter.electoral_geography` — Electoral section, entity, municipality, locality and district where applicable | New electoral-geography catalog/join and selected residence | Cannot derive an electoral section from a postal code alone without an appropriate geographic source. |
| `voter.registration_and_emission` — Registration year, emission/replacement details | New coherent voter-record history | Keep age, registration and issue chronology compatible. |
| `driver.category` — License/permit classes and categories | New selected authorization plus state/federal profile vocabulary | Not derivable from appearance; categories differ by issuer. |
| `driver.vehicle_service_mode` — Authorized vehicle, service modality and transport mode | New selected authorization plus issuer rules | Needed for relevant federal/special driving profiles. |
| `military.record` — Military matrícula, class, service/status and applicable rank/unit | New military-record fixtures | Appearance and age alone do not establish military status. |
| `professional.record` — Professional license number, degree, institution and award/registration dates | New educational/professional history and synthetic registry identifiers | Distinguish historical photo credentials from electronic professional records. |
| `migration.nue` — Número Único de Extranjero | New synthetic foreign-national registry identifier | Distinct from CURP and the individual card/document number. |
| `migration.status` — Residence/visitor category, work authorization and status legends | New immigration-history input plus selected document profile | Do not infer nationality or immigration status from ancestry. |
| `migration.family_or_authorization` — Dependent-family flag or special work/adoption/humanitarian authorization | New related-record/status input | Conditional on the specific INM document family. |
| `employee.record` — Employee ID, badge ID, agency, role/rank and access level | New employment/service history and issuer profile | A uniform-like shirt in the portrait is not proof of employment. |
| `student.record` — Student number, institution, program/grade and school cycle | New education-history fixtures | Age constrains plausible history but does not determine it. |
| `health.affiliation` — Beneficiary number, coverage class and institution/unit | New affiliation-history fixtures | No clinical status should be inferred from the portrait. |
| `senior.affiliation` — INAPAM/other program affiliation number | New synthetic program registry input | Age 60+ can be tested separately, but age does not supply membership. |
| `issuer.static_fields` — Issuer name, country codes, headings, logos and fixed legends | Template/profile catalog | Mexico is an issuing country here, not an inferred holder nationality. |
| `issuer.signatory_assets` — Authority name/title, signature and seal/stamp assets | Versioned template assets and synthetic signatory fixtures | Not contained in the portrait; distinguish holder signature from issuer signature. |
| `machine.mrz` — MRZ text and check digits | Deterministic generation after identity, document number, nationality/sex and validity inputs exist | Missing currently, despite a computable final format. Use the correct passport/card edition rules. |
| `machine.qr` — QR payload and QR image | Define a test payload from completed identity/document fields, then encode in code | Missing payload today; an arbitrary QR is not an authentic issuer-verifiable credential. |
| `machine.barcode` — Barcode payload and barcode image | Document-edition schema plus completed fields, then code encoding | Do not assume every Mexican ID uses PDF417, the same barcode, or the same field set. |
| `machine.chip` — Contactless-chip data groups and document security objects | Profile-specific data encoding after full identity/document inputs; separate test fixtures | A face image alone is not a complete electronic passport/consular chip. |
| `machine.issuer_authentication` — Issuer digital signatures, certificates and verification service state | External issuer material; use explicitly separate test keys/verification fixtures for synthetic testing | Authenticity is not created by copying a QR layout, computing a check digit or using an LLM. |

| `disability.record` — Disability-credential registration and any printed certified category/status | New synthetic certification/registration fixtures and a DIF/local document profile | An intended facial-condition or blindness prompt is not a disability certification or a certified degree of disability. |
| `pension.record` — Pensioner/retiree identifier, institution and benefit-status fields | New synthetic pension/retirement history and institution profile | Age and appearance do not establish pension entitlement; validity may be permanent for a selected edition. |
| `maritime.record` — Maritime identity/seafarer registration and credential category | New synthetic seafarer registration/qualification history and SEMAR credential profile | Confirm the individual edition’s printed fields, physical descriptors and validity rules; not derivable from portrait clothing. |

## Suggested data organization

Use one stable fictional identity per portrait, with multiple document instances:

| Component | Key | Contents |
| --- | --- | --- |
| `people` | `person_id` | `photo_id`, identity reference date, names, DOB, recorded identity fields, birthplace/nationality, canonical address and independent personal facts. |
| `documents` | `document_id`, `person_id` | Profile/edition/jurisdiction, issuer-assigned test identifiers, issue/expiry events, document-specific facts and references to assets. |
| `document_profiles` | `profile_id`, `edition` | Required/optional fields, labels, issuer, vocabularies, date/number formats, eligibility and photo rules, machine-code schema and static assets. |
| `assets` | `asset_id`, `person_id` or `document_id` | Source portrait references plus separately generated signatures, fingerprints and any other required synthetic assets. |

Use the full HF row ID (`session_uuid/photoId_00001`) as `photo_id`, with a pinned dataset
revision. The local filename stem alone can collide between sessions. Keep names and
DOB canonical; create uppercase/transliterated/line-broken display variants in code.
Keep sex markers, visual presentation and optional identity declarations as separate
fields. Birthplace, residential location and issuing location must also remain distinct.

For each generated field, save its origin (`source`, `mapped`, `ai_rewritten`,
`new_synthetic`, `template`, or `test_fixture`) and dependencies. Conditional fields
should distinguish `not_applicable`, `unknown` and an actual negative declaration.
Do not fill every field for every person merely to avoid nulls.

## Document-family crosswalk

| Family | Principal additional facts beyond portrait/appearance |
| --- | --- |
| Ordinary, official and diplomatic passports; travel/identity document | Names, DOB, nationality/status, birth location, recorded sex, passport/document number, issuance/expiry, issuer, holder signature, edition-specific MRZ/chip requirements. |
| INE, domestic/abroad and edition variants | Canonical identity, residential/electoral geography, clave de elector, CIC, OCR, registration/emission/expiry history, signature/fingerprint; supported optional identity/self-identification declarations. |
| Consular matrícula | Canonical Mexican identity, consulate, foreign residence, enrollment/card identifiers, issue/expiry and signature; chip profile when applicable. |
| State/CDMX licenses and permits | Identity/address/CURP, class/category/vehicle/service authorization, number, issue/expiry, restrictions; medical/donor/emergency fields and biometrics where that edition requires them. |
| Federal driver credential | Federal numbering/category/mode, authorization/validity and verification profile. |
| Military service credential | Identity, birthplace and civil history, matrícula/class/status; physical descriptors and biometric assets where the selected edition requires them. |
| Professional credential, historical/electronic variants | Professional registry number, degree, institution and registration/award dates; edition-specific signature/verification data and portrait presence. |
| INAPAM | Identity/CURP/address where printed, affiliation identifier and age-compatible program profile. |
| INM permanent, temporary, student and visitor categories | Nationality/birthplace, NUE, CURP where applicable, individual card number, authorized status/work/family flags, issue/validity/renewal data and edition-specific machine-readable zone. |
| Temporary photo CURP and biometric CURP profiles | Canonical identity/CURP, status/validity where applicable, photo and separately sourced fingerprints/other profile-specific biometrics. |
| Municipal identity/origin certificate | Identity/address/origin, municipality, folio, certification wording, issuer/signatory/seal and issuance event. |
| Government/military/public-safety employee credentials | Organization, employee/badge ID, rank/role/access and validity. |
| Public-health beneficiary credential | Beneficiary/affiliation identifier, institution/unit, coverage and validity. |
| Public-school/INEA credential | Institution, student ID, study program/grade/cycle and validity; guardian facts where applicable. |
| DIF/disability credential | Independent certification/registration fixtures and any edition-specific category/status; never equate a condition prompt with certification. |
| Pensioner/retiree credential | Pension/retirement affiliation and institution-specific status/validity. |
| Maritime identity document / libreta de mar | Seafarer registration, qualification/category and edition-specific physical descriptors and validity. |
| Supporting birth/nationality/fiscal documents | Civil-registration/parentage/nationality provenance and RFC/fiscal fixtures as appropriate; not all are photo identity cards. |

## Source checks and important gaps

1. **INE editions matter.** The current INE description includes optional gender identity
   and Indigenous/Afromexican self-identification features. These require new declarations,
   not an inference from the photo generator’s race/ethnicity label. [S1]
2. **Health/licensing facts are independent.** Nuevo León’s published license field list
   includes blood group, possible allergies, voluntary organ-donation declaration and
   driving conditions. This is an example of a local profile, not a nationwide field list.
   A portrait’s glasses or condition selection is not a recorded medical assessment. [S2]
3. **CURP is only partly determined by biography.** The current normative framework and
   RENAPO explanation must govern any synthetic-format implementation; a computed string
   is not an officially allocated CURP. New biography is needed before generation. [S3]
4. **Machine codes need payloads and profiles.** ICAO MRZ normalization/check digits can be
   computed after the required identity/document fields exist. INE verification codes
   and electronic credentials also involve issuer verification mechanisms; arbitrary
   encoded text does not supply those credentials. [S1, S4]
5. **Photo eligibility is separate from field availability.** Some military photo rules
   require no glasses/headwear and uncovered ears. Resizing cannot make every existing
   synthetic portrait comply. Use selection/validation or regenerate an appropriate
   portrait rather than silently treating all photos as compliant. [S5]
6. **Adults-only coverage is incomplete.** The current sampler uses ages 18–100, with 100
   standing for 100+. A full library covering minor passports, child/student credentials
   and minor driver permits requires additional age-appropriate portraits. INAPAM’s
   60+ age criterion can be checked, but membership must still be generated. The source
   age distribution is US-calibrated, not representative of Mexican document holders. [S6]
7. **Biometric CURP needs a versioned profile.** The 2025 legal change identifies photo
   and fingerprints alongside core identity data. Do not assume every biometric system
   requires an iris image or that every deployment/printed edition is identical. [S7]
8. **“Mexican ID” includes foreign holders.** INM resident/visitor documents require
   foreign-person histories; nationality must not be hardcoded from the issuing country.
   NUE, CURP and the individual document number are separate identifiers. [S8]

## Generation order

1. Pin the source photo row/revision and choose an explicit identity reference date.
2. Select a coherent fictional biography: names, DOB compatible with the selected age,
   birthplace, nationality, recorded identity declarations and address.
3. Derive display variants and synthetic-format personal identifiers in code, after
   their missing prerequisites have been supplied. Preserve registry-allocation versus
   computable-component distinctions.
4. Choose compatible document profiles and create document/affiliation histories,
   issuer control numbers and any independent health or authorization facts.
5. Create the missing signature/biometric test assets. Transform existing portraits only
   when they meet the profile’s photo constraints.
6. Render document-specific fields, MRZ/QR/barcodes and test verification fixtures from
   canonical inputs; validate cross-field consistency and retain expected OCR labels.

An LLM is useful for constrained prose and optional fictional biography proposals.
Prefer catalogs/samplers for geographically consistent addresses and name distributions,
and deterministic code for identifiers, dates, codes, checksums and formatting. An LLM
must not infer nationality, medical facts, fingerprints, consent, legal sex or an exact
DOB from a portrait. Synthetic biographies are invented inputs, not recovered facts.

## Sources

- Photo source: [v2 schema](https://github.com/lambdawalker/ds.photo_id/blob/03b7a595274869875ff58044b49948f6ee743b86/incremental_upload.py) and [selected-value export](https://github.com/lambdawalker/ds.photo_id/blob/03b7a595274869875ff58044b49948f6ee743b86/generation_session.py); [adult age sampler](https://github.com/lambdawalker/ds.photo_id/blob/03b7a595274869875ff58044b49948f6ee743b86/id_data/age.py).
- Catalog baseline: [25 Mexican credential families](README.md), reviewed from the repository’s current document tables; this is a starting inventory, not proof of every state/edition’s fields.
- S1: [INE: current credential model](https://ine.mx/conoce-tu-credencial-para-votar/) and [2025 model update](https://centralelectoral.ine.mx/2025/08/07/actualiza-ine-modelo-de-credencial-para-votar-con-nuevas-tecnologias-y-mayor-seguridad/).
- S2: [Nuevo León legislature: license field requirements, article 18](https://www.hcnl.gob.mx/trabajo_legislativo/leyes/leyes/ley_que_regula_la_expedicion_de_licencias_para_conducir_del_estado_de_nuevo_leon/).
- S3: [RENAPO: CURP structure](https://www.gob.mx/segob/renapo/es/articulos/sabes-como-se-conforma-tu-curp?idiom=es), [CURP assignment instruction](https://sidof.segob.gob.mx/notas/docFuente/5526717).
- S4: [ICAO Doc 9303, Part 3](https://www.icao.int/publications/documents/9303_p3_cons_en.pdf) and [Part 4](https://www.icao.int/publications/documents/9303_p4_cons_en.pdf).
- S5: [DEFENSA: military service credential photo requirements](https://www.gob.mx/defensa/acciones-y-programas/cuales-son-los-requisitos-para-tramitar-la-cartilla-de-identidad-del-servicio-militar).
- S6: [INAPAM credential](https://www.gob.mx/public/tramites/detalleTramite.xhtml?homoclave=INAPAM-2019-233-006-A).
- S7: [DOF: 2025 population-law amendment](https://dof.gob.mx/nota_detalle.php?codigo=5763157&fecha=16/07/2025) and [SEGOB: progressive biometric CURP adoption](https://www.gob.mx/segob/prensa/311603).
- S8: [SEGOB: CURP for foreign nationals and NUE](https://www.gob.mx/public/tramites/detalleTramite.xhtml?homoclave=SEGOB-2021-069-009-A).
- Additional scope notes: [SEP: electronic professional credential and identity-document distinction](https://www.gob.mx/sep/articulos/boletin-sep-no-145-ratifica-scjn-validez-de-la-cedula-profesional-electronica-educacion); [SAT: RFC registration](https://wwwmatnp.sat.gob.mx/tramites/82714/realiza-tu-inscripcion-en-el-rfc-persona-fisica).

Additional official credential sources: [DIF disability credential program](https://www.gob.mx/difnacional/acciones-y-programas/credencializacion-de-las-personas-con-discapacidad), [ISSSTE pensioner credentials](https://www.gob.mx/issste/prensa/inicia-issste-entrega-de-credenciales-con-vigencia-permanente-para-jubilados-y-pensionados), and [SEMAR maritime identity documents](https://www.gob.mx/semar/unaman/acciones-y-programas/tabla-tramites-de-documento-de-identidad-maritima-y-libreta-de-mar-418153). These establish additional profile families; their edition-specific fields still need individual validation.
