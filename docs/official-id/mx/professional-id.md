# Cédula profesional

[Mexico index](README.md) · `mx.professional-id`

- **Issuer** SEP / Dirección General de Profesiones
- **Typical format** varies
- **Evidence** Documented specimen
- **Scope** Record photo presence and medium by edition

## Human-readable fields

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Given name(s) | Given | — | — | — |
| Surname(s) | Inherited / legal | — | — | — |
| License number | Issuer assigned | — | — | — |
| CURP | Computed + issuer assigned | [RENAPO CURP composition](https://www.gob.mx/segob/renapo/es/articulos/sabes-como-se-conforma-tu-curp?idiom=es) | Derived from names, date of birth, sex and birthplace, with an issuer-assigned disambiguator and a check digit. The biographic inputs alone do not establish the official key. | — |
| Professional title or degree | Issuer determined | — | — | — |
| Institution | Document metadata | — | — | — |
| Issue date | Issuer determined | — | — | Verify presence by issuer or edition. |
| Portrait | Captured | — | — | Verify presence by issuer or edition. |
| Holder signature | Captured | — | — | Verify presence by issuer or edition. |

## Machine-readable data

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Verification code | Computed | QR | The court describes public information including name and professional license number across the codes reviewed. Exact QR field membership is unverified. | Electronic specimen reviewed by SCJN. |
| License-number barcode | Computed | Barcode · exact symbology unverified | Professional license number. | Same specimen. |
| Electronic credential identifier barcode | Computed | Barcode · exact symbology unverified | Electronic credential identifier. | Same specimen. |

## Sources

- [Credential family and issuer reference](https://www.dof.gob.mx/2026/INE/Acuerdo_INE_CNV02_ENE-2026.pdf)
- [SCJN electronic credential decision](https://www.scjn.gob.mx/sites/default/files/resoluciones/2021-01/CT-CUM-A-17-2020.pdf)
