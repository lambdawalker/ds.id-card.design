# Documento de Identidad y Viaje

[Mexico index](README.md) · `mx.travel-identity`

- **Issuer** SRE
- **Typical format** travel document
- **Evidence** Candidate fields, verify against specimen

## Human-readable fields

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Given name(s) | Given | — | — | — |
| Surname(s) | Inherited / legal | — | — | — |
| Date of birth | Recorded | — | — | — |
| Place of birth | Recorded | — | — | — |
| Portrait | Captured | — | — | — |
| Document number | Issuer assigned | — | — | — |
| Issue date | Issuer determined | — | — | — |
| Expiration date | Issuer determined | — | — | — |
| Issuing authority | Document metadata | — | — | — |
| Restrictions | Issuer determined | — | — | Verify presence by issuer or edition. |
| Endorsements | Issuer determined | — | — | Verify presence by issuer or edition. |
| Nationality | Issuer determined | — | — | Verify presence by issuer or edition. |
| Status or eligibility category | Issuer determined | — | — | Verify presence by issuer or edition. |

## Machine-readable data

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Machine-readable feature | Unverified | MRZ, chip | Unverified. | Check the data page for an MRZ and chip by edition. Where an ICAO TD3 MRZ is confirmed, its field categories follow the passport-booklet standard. The source here does not establish a payload for this credential. |

## Sources

- [Credential family and issuer reference](https://sre.gob.mx/component/phocadownload/category/5-transparencia-y-acceso-a-la-informacion?download=1372%3Aaviso-de-privacidad-integral-para-la-solicitud-de-documento-de-identidad-y-viaje)
- [ICAO Doc 9303, Part 4](https://www.icao.int/publications/documents/9303_p4_cons_en.pdf)
