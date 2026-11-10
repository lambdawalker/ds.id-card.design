# Certificado de Matrícula Consular

[Mexico index](README.md) · `mx.consular-id`

- **Issuer** SRE / Mexican consulates
- **Typical format** card
- **Evidence** Chip presence confirmed, visual fields partly edition-dependent

## Human-readable fields

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Given name(s) | Given | — | — | — |
| Surname(s) | Inherited / legal | — | — | — |
| Portrait | Captured | — | — | — |
| Date of birth | Recorded | — | — | — |
| Registration or enrollment number | Issuer assigned | — | — | Verify presence by issuer or edition. |
| Card number | Issuer assigned | — | — | Verify presence by issuer or edition. |
| Issuing authority | Document metadata | — | — | — |
| Issue date | Issuer determined | — | — | — |
| Expiration date | Issuer determined | — | — | — |
| Address | Recorded | — | — | Verify presence by issuer or edition. |
| Holder signature | Captured | — | — | Verify presence by issuer or edition. |
| Sex marker | Recorded | — | — | Third-generation editions can show X or omit the marker. |

## Machine-readable data

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Embedded chip | Encoded | SRE third-generation chip | Credential information. Individual fields and data groups are unverified. | Third-generation consular card. |

## Sources

- [Credential family and issuer reference](https://www.gob.mx/public/tramites/detalleTramite.xhtml?homoclave=SRE-01-013-A)
- [SRE third-generation specimen](https://consulmex.sre.gob.mx/fresno/images/2022/folletoMCAS3G.pdf)
