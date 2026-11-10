# Official personal credential catalog

Research snapshot · 2026-11-10

This first inventory records 83 country-scoped credential types for a future synthetic document-image dataset. It covers personal documents issued by public authorities, including tribal and First Nation issuers where relevant. It includes primary identity credentials and specialized credentials whose use depends on the transaction. Acceptance rules belong to the authority requesting the document.

The key identifies the document type. Keep the issuing jurisdiction, issuer, program, medium, class, edition and issuance dates separate when expanding to individual products. For example, a standard and a REAL ID-compliant driver's license can share a type while remaining distinct products for a state. Passport age and validity periods generally describe variants. Shared border programs appear under both participating countries and should be deduplicated by program and issuer when assigning dataset labels.

The format column describes the typical artifact. `varies` means the issuer or edition needs its own check. A listed family can contain historic products, including ones no longer issued. The source links verify credential families and examples. The coverage checklist identifies where product-level verification remains open.

## Mexico

| Key | Credential | Issuer | Typical format | Scope or variants | Source |
| --- | --- | --- | --- | --- | --- |
| `mx.passport-ordinary` | Pasaporte ordinario | SRE | booklet | — | [mx-pass] |
| `mx.passport-official` | Pasaporte oficial | SRE | booklet | — | [mx-pass] |
| `mx.passport-diplomatic` | Pasaporte diplomático | SRE | booklet | — | [mx-pass] |
| `mx.travel-identity` | Documento de Identidad y Viaje | SRE | travel document | — | [mx-travel] |
| `mx.voter-id` | Credencial para Votar | INE | card | Domestic and overseas issuance | [mx-ine] |
| `mx.consular-id` | Certificado de Matrícula Consular | SRE / Mexican consulates | card | — | [mx-consular] |
| `mx.driver-license` | Licencia de conducir | State or Mexico City licensing authority | varies | Private, motorcycle, public-service and commercial classes where issued | [mx-criteria] |
| `mx.driver-permit` | Permiso para conducir | State or Mexico City licensing authority | varies | Minor, provisional or learner permits where issued | [mx-criteria] |
| `mx.federal-driver-license` | Licencia Federal Digital de Conductor | SICT | digital | — | [mx-sict] |
| `mx.military-service` | Cartilla del Servicio Militar Nacional | SEDENA | document | Liberada and sin liberar are status variants | [mx-criteria] |
| `mx.professional-id` | Cédula profesional | SEP / Dirección General de Profesiones | varies | Record photo presence and medium by edition | [mx-criteria] |
| `mx.senior-id` | Credencial INAPAM | INAPAM | card | — | [mx-senior] |
| `mx.resident-temporary` | Tarjeta de Residente Temporal | INM | card | — | [mx-inm] |
| `mx.resident-student` | Tarjeta de Residente Temporal Estudiante | INM | card | — | [mx-inm] |
| `mx.resident-permanent` | Tarjeta de Residente Permanente | INM | card | — | [mx-inm] |
| `mx.visitor-regional` | Tarjeta de Visitante Regional | INM | card | — | [mx-inm] |
| `mx.visitor-border-worker` | Tarjeta de Visitante Trabajador Fronterizo | INM | card | — | [mx-inm] |
| `mx.visitor-humanitarian` | Tarjeta de Visitante por Razones Humanitarias | INM | card | — | [mx-inm] |
| `mx.visitor-adoption` | Tarjeta de Visitante con Fines de Adopción | INM | card | — | [mx-inm] |
| `mx.visitor-remunerated` | Tarjeta de Visitante con Permiso para Realizar Actividades Remuneradas | INM | card | — | [mx-inm-notice] |
| `mx.temporary-photo-curp` | CURP temporal con fotografía | INM / population registry | document | Specific migration context | [mx-inm-notice] |
| `mx.local-identity-certificate` | Constancia o certificado de identidad u origen | Municipal authority | document | Verify local program and photo presence | [mx-criteria] |
| `mx.government-personnel-id` | Government employee, military or public-safety ID | Issuing public authority | varies | Agency-specific scope | [mx-declara] |
| `mx.public-health-beneficiary-id` | Credencial de identificación de persona derechohabiente | Federal, state or municipal public health institution | varies | Separate from appointment booklets and insurance paperwork | [mx-criteria] |
| `mx.public-school-id` | Public-school or INEA student credential | Public educational institution / INEA | varies | Institution-specific | [mx-criteria] |

## Canada

| Key | Credential | Issuer | Typical format | Scope or variants | Source |
| --- | --- | --- | --- | --- | --- |
| `ca.passport-regular` | Regular passport | IRCC Passport Program | booklet | — | [ca-pass] |
| `ca.passport-special` | Special passport | IRCC Passport Program | booklet | — | [ca-pass] |
| `ca.passport-diplomatic` | Diplomatic passport | IRCC Passport Program | booklet | — | [ca-pass] |
| `ca.passport-temporary` | Temporary passport | Canadian mission abroad | booklet | — | [ca-pass] |
| `ca.travel-emergency` | Emergency travel document | Canadian mission abroad | document | — | [ca-pass] |
| `ca.travel-refugee` | Refugee travel document | IRCC | booklet | — | [ca-pass] |
| `ca.travel-certificate-identity` | Certificate of identity | IRCC | booklet | — | [ca-pass] |
| `ca.driver-license` | Driver’s licence / Permis de conduire | Province or territory | varies | Passenger, commercial, motorcycle and graduated variants as applicable | [ca-fin] |
| `ca.driver-permit` | Learner’s licence or permit | Province or territory | varies | Separate only where jurisdiction issues a distinct credential | [ca-fin] |
| `ca.non-driver-id` | Provincial or territorial photo identification card | Province or territory | card | Verify product availability by jurisdiction | [ca-fin] |
| `ca.enhanced-driver-license` | Enhanced driver’s licence | Participating provincial authority | card | Verify historical issuance and expiry by province | [ca-border] |
| `ca.enhanced-id` | Enhanced identification card | Participating provincial authority | card | Verify historical issuance and expiry by province | [ca-fin] |
| `ca.health-services-id` | Photo health or services card | Provincial or territorial health authority | card | Examples include BC Services Card and combined BC driver’s licence/services card. Photo and permitted use vary. | [ca-fin] |
| `ca.resident-permanent` | Permanent resident card | IRCC | card | — | [ca-fin] |
| `ca.refugee-protection-id` | Refugee Protection Identity Document (RPID) | IRCC / CBSA | document | — | [ca-rpid] |
| `ca.refugee-claimant` | Refugee Protection Claimant Document (RPCD) | IRCC / CBSA | document | Predecessor to RPID | [ca-rpid] |
| `ca.citizenship-card` | Canadian citizenship card | Federal citizenship authority | card | Legacy issuance | [ca-cit] |
| `ca.indigenous-secure-status` | Secure Certificate of Indian Status | Indigenous Services Canada | card | — | [ca-border] |
| `ca.indigenous-status` | Certificate of Indian Status | Indigenous Services Canada / authorized First Nation office | card | — | [ca-border] |
| `ca.forces-id` | Canadian Armed Forces identification | Department of National Defence | card | — | [ca-border] |
| `ca.forces-driver-license` | DND 404 driver’s licence | Department of National Defence | varies | — | [ca-fin] |
| `ca.veteran-service` | Veteran’s Service Card | Department of National Defence | card | Service credential | [ca-vet] |
| `ca.firearms-pal` | Possession and Acquisition Licence (PAL) | RCMP Canadian Firearms Program | card | Restricted privileges are a variant | [ca-pal] |
| `ca.firearms-fac` | Firearms Acquisition Certificate (FAC) | Historical firearms licensing authority | document | Legacy credential | [ca-border] |
| `ca.nexus` | NEXUS card | CBSA / U.S. CBP | card | Joint program, shared with US | [ca-fin] |
| `ca.fast` | FAST card | CBSA / U.S. CBP for northern-border program | card | Track northern and southern program context separately | [us-ttp] |

## United States

| Key | Credential | Issuer | Typical format | Scope or variants | Source |
| --- | --- | --- | --- | --- | --- |
| `us.passport-book` | U.S. passport book | Department of State | booklet | — | [us-pass] |
| `us.passport-card` | U.S. passport card | Department of State | card | — | [us-pass] |
| `us.passport-diplomatic` | Diplomatic passport | Department of State | booklet | — | [us-special] |
| `us.passport-official` | Official passport | Department of State | booklet | — | [us-special] |
| `us.passport-service` | Service passport | Department of State | booklet | — | [us-special] |
| `us.passport-no-fee` | No-fee regular passport | Department of State | booklet | Special issuance | [us-special] |
| `us.driver-license` | Driver’s license | State, DC or territorial licensing authority | varies | Track standard, REAL ID and enhanced variants where offered | [us-tsa] |
| `us.non-driver-id` | Non-driver identification card | State, DC or territorial licensing authority | card | Track standard, REAL ID and enhanced variants where offered | [us-tsa] |
| `us.driver-learner-permit` | Learner’s permit | State, DC or territorial licensing authority | varies | Verify photo and format by issuer | [us-i9] |
| `us.driver-commercial-license` | Commercial driver’s license (CDL) | State or participating jurisdiction | varies | — | [us-cdl] |
| `us.driver-commercial-permit` | Commercial learner’s permit (CLP) | State or participating jurisdiction | varies | — | [us-cdl] |
| `us.resident-permanent` | Permanent Resident Card (I-551) | USCIS | card | Older Alien Registration Receipt Card labels belong in edition history | [us-i9] |
| `us.employment-authorization` | Employment Authorization Document (I-766) | USCIS | card | — | [us-i9] |
| `us.border-crossing` | Border Crossing Card (DSP-150 / BCC) | Department of State | card | — | [us-bcc] |
| `us.global-entry` | Global Entry card | CBP | card | — | [us-ttp] |
| `us.nexus` | NEXUS card | CBP / Canada CBSA | card | Joint program, shared with CA | [us-ttp] |
| `us.sentri` | SENTRI card | CBP | card | — | [us-ttp] |
| `us.fast` | FAST card | CBP / Canada CBSA for northern-border program | card | Track northern and southern program context separately | [us-ttp] |
| `us.tribal-photo-id` | Tribal government photo ID | Federally recognized tribal nation | card | Track individual tribal issuers | [us-tsa] |
| `us.enhanced-tribal-id` | Enhanced Tribal Card (ETC) | Participating tribal nation | card | — | [us-tsa] |
| `us.military-cac` | Common Access Card (CAC) | Department of Defense | card | Uniformed personnel and eligible civilian or contractor categories | [us-dod] |
| `us.military-usid` | Uniformed Services ID (USID) | Department of Defense | card | Retirees, eligible dependents and other eligible categories | [us-dod] |
| `us.federal-piv` | Personal Identity Verification (PIV) card | Issuing federal agency | card | HSPD-12 federal personnel credential | [us-tsa] |
| `us.transport-worker` | Transportation Worker Identification Credential (TWIC) | TSA | card | — | [us-tsa] |
| `us.merchant-mariner` | Merchant Mariner Credential (MMC) | U.S. Coast Guard | varies | — | [us-tsa] |
| `us.veteran-health-id` | Veteran Health Identification Card (VHIC) | Department of Veterans Affairs | card | — | [us-tsa] |
| `us.public-employee-id` | State or local public employee ID | Issuing government agency | varies | Agency-specific scope | [us-i9] |
| `us.municipal-id` | Municipal resident ID | Participating city or local government | card | IDNYC is one example | [us-city] |
| `us.travel-reentry` | Reentry Permit (I-327) | USCIS | booklet | — | [us-return] |
| `us.travel-refugee` | Refugee Travel Document (I-571) | USCIS | booklet | — | [us-return] |
| `us.travel-advance-parole` | Advance parole travel document | USCIS | varies | Standalone and eligible combined EAD variants | [us-return] |
| `us.veteran-id` | Veteran ID Card (VIC) | Department of Veterans Affairs | digital | Veteran status credential, distinct from VHIC | [us-vic] |

## Related official documents

Keep these in a separate document group for tasks that also include supporting evidence. Record photo presence by edition. A document may be accepted as evidence in one procedure and serve a different purpose elsewhere.

| Country | Related document types | Sources |
| --- | --- | --- |
| Mexico | Birth registration and certified birth certificate, naturalization letter or certificate, Mexican nationality certificate and declarations, ordinary CURP record, visas, Forma Migratoria Múltiple (FMM), refugee application acknowledgments, and public education records. Research biometric CURP and historical child identity credentials separately by program and issuance period. | [mx-criteria], [mx-inm], [mx-curp] |
| Canada | Birth certificate, citizenship certificate, Confirmation of Permanent Residence (COPR), permanent resident travel document (PRTD), Verification of Status, visitor record, work permit, study permit, visa, and non-photo health coverage card. | [ca-cit], [ca-rpid], [ca-border] |
| United States | Birth certificate, Consular Report of Birth Abroad, certificates of citizenship and naturalization, Social Security card, visa foil, Form I-94 arrival/departure record, and voter registration card. Check jurisdiction-specific voter photo ID programs separately from registration. | [us-i9], [us-return] |

## Issuer coverage checklist

These are jurisdictions to audit for licensing and other local credentials. Presence in the checklist gives no product-level coverage guarantee.

- **Mexico · 32 federal entities.** Aguascalientes, Baja California, Baja California Sur, Campeche, Chiapas, Chihuahua, Ciudad de México, Coahuila, Colima, Durango, Estado de México, Guanajuato, Guerrero, Hidalgo, Jalisco, Michoacán, Morelos, Nayarit, Nuevo León, Oaxaca, Puebla, Querétaro, Quintana Roo, San Luis Potosí, Sinaloa, Sonora, Tabasco, Tamaulipas, Tlaxcala, Veracruz, Yucatán and Zacatecas. Check local digital editions, license classes, provisional permits, and municipal identity letters. [mx-criteria]
- **Canada · 10 provinces and 3 territories.** Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland and Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, Saskatchewan, Northwest Territories, Nunavut and Yukon. Check driver and learner products, non-driver cards, photo health and combined cards, and legacy enhanced credentials separately. FINTRAC links to licence issuers for all 13 jurisdictions and gives examples of non-driver IDs. [ca-fin]
- **United States · 50 states, DC and 5 inhabited territories.** Alabama, Alaska, Arizona, Arkansas, California, Colorado, Connecticut, Delaware, Florida, Georgia, Hawaii, Idaho, Illinois, Indiana, Iowa, Kansas, Kentucky, Louisiana, Maine, Maryland, Massachusetts, Michigan, Minnesota, Mississippi, Missouri, Montana, Nebraska, Nevada, New Hampshire, New Jersey, New Mexico, New York, North Carolina, North Dakota, Ohio, Oklahoma, Oregon, Pennsylvania, Rhode Island, South Carolina, South Dakota, Tennessee, Texas, Utah, Vermont, Virginia, Washington, West Virginia, Wisconsin, Wyoming, District of Columbia, American Samoa, Guam, Northern Mariana Islands, Puerto Rico and U.S. Virgin Islands. Check standard, REAL ID, enhanced, temporary and mobile credentials where available. Verify tribal, municipal, voter photo ID and occupational credentials at their own issuing authorities. [us-dmv], [us-tsa]

Local and Indigenous issuer inventories, public employee and occupational programs, mobile credential availability, and historical designs are open coverage areas across the catalog.

## Sources

- [SRE passport regulation and official passport issuance](https://portales.sre.gob.mx/transparencia/transparencia-categorias/category/1735-i?download=60394%3Areglamento-de-pasaportes-y-del-documento-de-identidad-y-viaje&start=180)

[mx-pass]: https://portales.sre.gob.mx/transparencia/transparencia-categorias/category/1735-i?download=60394%3Areglamento-de-pasaportes-y-del-documento-de-identidad-y-viaje&start=180

- [SRE Documento de Identidad y Viaje](https://sre.gob.mx/component/phocadownload/category/5-transparencia-y-acceso-a-la-informacion?download=1372%3Aaviso-de-privacidad-integral-para-la-solicitud-de-documento-de-identidad-y-viaje)

[mx-travel]: https://sre.gob.mx/component/phocadownload/category/5-transparencia-y-acceso-a-la-informacion?download=1372%3Aaviso-de-privacidad-integral-para-la-solicitud-de-documento-de-identidad-y-viaje

- [INE Credencial para Votar](https://www.ine.mx/credencial/)

[mx-ine]: https://www.ine.mx/credencial/

- [SRE overseas voter credential](https://www.gob.mx/public/tramites/detalleTramite.xhtml?homoclave=SRE-01-041)

[mx-abroad]: https://www.gob.mx/public/tramites/detalleTramite.xhtml?homoclave=SRE-01-041

- [SRE consular registration certificate](https://www.gob.mx/public/tramites/detalleTramite.xhtml?homoclave=SRE-01-013-A)

[mx-consular]: https://www.gob.mx/public/tramites/detalleTramite.xhtml?homoclave=SRE-01-013-A

- [INE photo-document criteria](https://www.dof.gob.mx/2026/INE/Acuerdo_INE_CNV02_ENE-2026.pdf)

[mx-criteria]: https://www.dof.gob.mx/2026/INE/Acuerdo_INE_CNV02_ENE-2026.pdf

- [SICT federal digital driver credential](https://www.gob.mx/public/tramites/detalleTramite.xhtml?homoclave=SICT-03-028-A)

[mx-sict]: https://www.gob.mx/public/tramites/detalleTramite.xhtml?homoclave=SICT-03-028-A

- [INAPAM senior credential](https://www.gob.mx/public/tramites/detalleTramite.xhtml?homoclave=INAPAM-2019-233-006-A)

[mx-senior]: https://www.gob.mx/public/tramites/detalleTramite.xhtml?homoclave=INAPAM-2019-233-006-A

- [INM migration card types](https://www.gob.mx/inm/articulos/no-te-dejes-enganar-215042)

[mx-inm]: https://www.gob.mx/inm/articulos/no-te-dejes-enganar-215042

- [INM notice on migration cards and temporary photo CURP](https://www.inm.gob.mx/gobmx/word/wp-content/uploads/2023/08/Tarjeta-Migratoria-100823.pdf)

[mx-inm-notice]: https://www.inm.gob.mx/gobmx/word/wp-content/uploads/2023/08/Tarjeta-Migratoria-100823.pdf

- [DeclaraNet identification criteria](https://declaranet.gob.mx/firma-electronica/identificaciones-oficiales.html)

[mx-declara]: https://declaranet.gob.mx/firma-electronica/identificaciones-oficiales.html

- [Chihuahua biometric CURP pilot](https://www.chihuahua.gob.mx/prensa/arranca-en-chihuahua-programa-piloto-de-curp-biometrica)

[mx-curp]: https://www.chihuahua.gob.mx/prensa/arranca-en-chihuahua-programa-piloto-de-curp-biometrica

- [IRCC passport and travel-document types](https://www.canada.ca/en/immigration-refugees-citizenship/services/canadian-passports/document-types.html)

[ca-pass]: https://www.canada.ca/en/immigration-refugees-citizenship/services/canadian-passports/document-types.html

- [FINTRAC identity verification guidance, Annex 4](https://fintrac-canafe.canada.ca/guidance-directives/client-clientele/guide11/11-eng)

[ca-fin]: https://fintrac-canafe.canada.ca/guidance-directives/client-clientele/guide11/11-eng

- [CBSA travel and identification documents](https://www.cbsa-asfc.gc.ca/travel-voyage/td-dv-eng.html)

[ca-border]: https://www.cbsa-asfc.gc.ca/travel-voyage/td-dv-eng.html

- [IRCC immigration and status documents](https://www.canada.ca/en/immigration-refugees-citizenship/corporate/partners-service-providers/status-documents.html)

[ca-rpid]: https://www.canada.ca/en/immigration-refugees-citizenship/corporate/partners-service-providers/status-documents.html

- [IRCC proof of citizenship](https://www.canada.ca/en/immigration-refugees-citizenship/services/canadian-citizenship/proof-citizenship/about.html)

[ca-cit]: https://www.canada.ca/en/immigration-refugees-citizenship/services/canadian-citizenship/proof-citizenship/about.html

- [DND Veteran’s Service Card](https://www.canada.ca/en/department-national-defence/services/benefits-military/transition/service-card.html)

[ca-vet]: https://www.canada.ca/en/department-national-defence/services/benefits-military/transition/service-card.html

- [RCMP firearms licence](https://www.rcmp.ca/en/firearms/apply-firearms-licence)

[ca-pal]: https://www.rcmp.ca/en/firearms/apply-firearms-licence

- [State Department passport book and card comparison](https://travel.state.gov/en/passports/apply/help/passport-card-vs-book.html)

[us-pass]: https://travel.state.gov/en/passports/apply/help/passport-card-vs-book.html

- [State Department special-issuance passports](https://travel.state.gov/en/passports/apply/unique-needs/special-issuance-passport.html)

[us-special]: https://travel.state.gov/en/passports/apply/unique-needs/special-issuance-passport.html

- [U.S. House summary of TSA identification categories](https://boyle.house.gov/services/real-id-requirements-acceptable-alternatives-air-travel)

[us-tsa]: https://boyle.house.gov/services/real-id-requirements-acceptable-alternatives-air-travel

- [USCIS Form I-9 lists of acceptable documents](https://www.uscis.gov/sites/default/files/document/forms/i-9.pdf)

[us-i9]: https://www.uscis.gov/sites/default/files/document/forms/i-9.pdf

- [FMCSA commercial licensing](https://www.fmcsa.dot.gov/registration/commercial-drivers-license/drivers)

[us-cdl]: https://www.fmcsa.dot.gov/registration/commercial-drivers-license/drivers

- [State Department Border Crossing Card](https://travel.state.gov/content/travel/en/us-visas/tourism-visit/border-crossing-card.html)

[us-bcc]: https://travel.state.gov/content/travel/en/us-visas/tourism-visit/border-crossing-card.html

- [CBP Trusted Traveler Programs](https://www.help.cbp.gov/s/article/Article-1885)

[us-ttp]: https://www.help.cbp.gov/s/article/Article-1885

- [DMDC military ID cards](https://dwp.dmdc.osd.mil/dwp/app/id-management/id-cards)

[us-dod]: https://dwp.dmdc.osd.mil/dwp/app/id-management/id-cards

- [New York City IDNYC program](https://www.nyc.gov/site/idnyc/index.page)

[us-city]: https://www.nyc.gov/site/idnyc/index.page

- [USAGov travel documents for returning noncitizens](https://www.usa.gov/travel-documents-foreign-citizens)

[us-return]: https://www.usa.gov/travel-documents-foreign-citizens

- [VA Veteran ID Card](https://www.va.gov/records/get-veteran-id-cards/vic/)

[us-vic]: https://www.va.gov/records/get-veteran-id-cards/vic/

- [USAGov motor vehicle authority directory](https://www.usa.gov/state-motor-vehicle-services)

[us-dmv]: https://www.usa.gov/state-motor-vehicle-services
