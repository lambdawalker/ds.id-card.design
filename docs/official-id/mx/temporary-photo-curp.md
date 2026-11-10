# CURP temporal con fotografía

[Mexico index](README.md) · `mx.temporary-photo-curp`

- **Issuer** INM / population registry
- **Typical format** document
- **Evidence** Partial issuer evidence
- **Scope** Specific migration context

## Human-readable fields

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Given name(s) | Given | — | — | — |
| Surname(s) | Inherited / legal | — | — | — |
| CURP | Computed + issuer assigned | [RENAPO CURP composition](https://www.gob.mx/segob/renapo/es/articulos/sabes-como-se-conforma-tu-curp?idiom=es) | Derived from names, date of birth, sex and birthplace, with an issuer-assigned disambiguator and a check digit. The biographic inputs alone do not establish the official key. | — |
| Portrait | Captured | — | — | — |
| Expiration date | Issuer determined | — | — | Verify presence by issuer or edition. |
| Issuing authority | Document metadata | — | — | Verify presence by issuer or edition. |

## Machine-readable data

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Machine-readable feature | Unverified | — | Unverified. | Code presence and payload unverified. Verify separately from the ordinary CURP printout. |

## Sources

- [Credential family and issuer reference](https://www.inm.gob.mx/gobmx/word/wp-content/uploads/2023/08/Tarjeta-Migratoria-100823.pdf)
