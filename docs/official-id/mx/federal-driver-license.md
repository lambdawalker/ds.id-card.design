# Licencia Federal Digital de Conductor

[Mexico index](README.md) · `mx.federal-driver-license`

- **Issuer** SICT
- **Typical format** digital
- **Evidence** Issuer-confirmed QR purpose

## Human-readable fields

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Given name(s) | Given | — | — | — |
| Surname(s) | Inherited / legal | — | — | — |
| Portrait | Captured | — | — | — |
| Driver license or permit number | Issuer assigned | — | — | Assignment policy varies by issuer. Randomness is unverified. |
| License class or category | Issuer determined | — | — | — |
| Mode of transport | Document metadata | — | — | — |
| Expiration date | Issuer determined | — | — | — |
| Issuing authority | Document metadata | — | — | — |

## Machine-readable data

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Verification code | Computed | QR · SICT verification | Encoded license data and an agency verification link. Individual encoded fields are unverified. | Federal digital and print editions. |

## Sources

- [Credential family and issuer reference](https://www.gob.mx/public/tramites/detalleTramite.xhtml?homoclave=SICT-03-028-A)
- [Federal digital license rules](https://sidof.segob.gob.mx/notas/docFuente/5611493)
