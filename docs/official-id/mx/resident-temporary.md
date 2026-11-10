# Tarjeta de Residente Temporal

[Mexico index](README.md) · `mx.resident-temporary`

- **Issuer** INM
- **Typical format** card
- **Evidence** Historical issuer specification, verify newer editions

## Human-readable fields

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Given name(s) | Given | — | — | — |
| Surname(s) | Inherited / legal | — | — | — |
| Nationality | Issuer determined | — | — | — |
| Country of birth | Recorded | — | — | — |
| Date of birth | Recorded | — | — | — |
| Sex marker | Recorded | — | — | — |
| Portrait | Captured | — | — | — |
| Status or eligibility category | Issuer determined | — | — | — |
| Foreign national identifier (NUE) | Issuer assigned | — | — | — |
| Expiration date | Issuer determined | — | — | Verify presence by issuer or edition. |
| CURP | Computed + issuer assigned | [RENAPO CURP composition](https://www.gob.mx/segob/renapo/es/articulos/sabes-como-se-conforma-tu-curp?idiom=es) | Derived from names, date of birth, sex and birthplace, with an issuer-assigned disambiguator and a check digit. The biographic inputs alone do not establish the official key. | Verify presence by issuer or edition. |
| Holder signature | Captured | — | — | — |
| Issuance place | Document metadata | — | — | — |
| Issue date | Issuer determined | — | — | — |
| Document number | Issuer assigned | — | — | — |
| Issuing authority | Document metadata | — | — | — |
| Authority signature | Captured | — | — | — |
| Renewal count | Issuer determined | — | — | Verify presence by issuer or edition. |
| Work authorization indicator | Issuer determined | — | — | — |

The historical INM circular places the signature, issuance place and date, migration document number, authority details and any renewal count on the reverse.

## Machine-readable data

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Reverse OCR zone | Computed | OCR-readable text · INM circular | Field list unverified. | Historical specification. Verify QR or chip on later editions. |

## Sources

- [Credential family and issuer reference](https://www.gob.mx/inm/articulos/no-te-dejes-enganar-215042)
- [INM circular, card fields](https://www.inm.gob.mx/static/marco_juridico/pdf/circulares/CIRCULAR_referente_documentos_migratorios_formatos_solicitud.pdf)
