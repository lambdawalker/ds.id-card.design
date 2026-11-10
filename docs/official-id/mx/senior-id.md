# Credencial INAPAM

[Mexico index](README.md) · `mx.senior-id`

- **Issuer** INAPAM
- **Typical format** card
- **Evidence** Candidate fields, verify against specimen

## Human-readable fields

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Given name(s) | Given | — | — | — |
| Surname(s) | Inherited / legal | — | — | — |
| Portrait | Captured | — | — | — |
| Membership or affiliation number | Issuer assigned | — | — | — |
| Issue date | Issuer determined | — | — | Verify presence by issuer or edition. |
| CURP | Computed + issuer assigned | [RENAPO CURP composition](https://www.gob.mx/segob/renapo/es/articulos/sabes-como-se-conforma-tu-curp?idiom=es) | Derived from names, date of birth, sex and birthplace, with an issuer-assigned disambiguator and a check digit. The biographic inputs alone do not establish the official key. | Verify presence by issuer or edition. |
| Date of birth | Recorded | — | — | Verify presence by issuer or edition. |
| Holder signature | Captured | — | — | Verify presence by issuer or edition. |
| Address | Recorded | — | — | Verify presence by issuer or edition. |

## Machine-readable data

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Machine-readable feature | Unverified | — | Unverified. | Check each card design. Code presence and payload unverified. |

## Sources

- [Credential family and issuer reference](https://www.gob.mx/public/tramites/detalleTramite.xhtml?homoclave=INAPAM-2019-233-006-A)
- [INAPAM designs in circulation](https://www.gob.mx/inapam/documentos/credenciales-inapam-vigentes)
