# Credencial para Votar

[Mexico index](README.md) · `mx.voter-id`

- **Issuer** INE
- **Typical format** card
- **Evidence** Issuer-confirmed QR and verifier output
- **Scope** Domestic and overseas issuance

## Human-readable fields

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Given name(s) | Given | — | — | — |
| Surname(s) | Inherited / legal | — | — | — |
| Portrait | Captured | — | — | — |
| Date of birth | Recorded | — | — | — |
| Sex marker | Recorded | — | — | — |
| Holder signature | Captured | — | — | — |
| Address | Recorded | — | — | May be masked. |
| Clave de elector | Issuer assigned | — | — | — |
| CURP | Computed + issuer assigned | [RENAPO CURP composition](https://www.gob.mx/segob/renapo/es/articulos/sabes-como-se-conforma-tu-curp?idiom=es) | Derived from names, date of birth, sex and birthplace, with an issuer-assigned disambiguator and a check digit. The biographic inputs alone do not establish the official key. | — |
| Electoral section | Issuer determined | — | — | — |
| Expiration date | Issuer determined | — | — | — |
| CIC identifier | Issuer assigned | — | — | Verify presence by issuer or edition. |
| Printed OCR identifier | Issuer assigned | — | — | Verify presence by issuer or edition. |

## Machine-readable data

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Rear verification codes | Computed | QR · INE verification | Embedded field list unverified. INE's verifier example displays names, sex, CURP, OCR identifier and production date. | Documented on G/H and newer models. App output alone does not establish where each value is stored. |

## Sources

- [Credential family and issuer reference](https://www.ine.mx/credencial/)
- [INE card models](https://portal.ine.mx/conoce-tu-credencial-para-votar/)
- [INE verification example](https://centralelectoral.ine.mx/wp-content/uploads/2024/01/Credencial_aclaracion-1.pdf)
