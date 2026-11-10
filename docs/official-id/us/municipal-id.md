# Municipal resident ID

[United States index](README.md) · `us.municipal-id`

- **Issuer** Participating city or local government
- **Typical format** card
- **Evidence** Candidate fields, verify against specimen
- **Scope** IDNYC is one example

## Human-readable fields

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Given name(s) | Given | — | — | — |
| Surname(s) | Inherited / legal | — | — | — |
| Portrait | Captured | — | — | — |
| Program name | Document metadata | — | — | — |
| Card number | Issuer assigned | — | — | — |
| Date of birth | Recorded | — | — | — |
| Address | Recorded | — | — | Verify presence by issuer or edition. |
| Issue date | Issuer determined | — | — | Verify presence by issuer or edition. |
| Expiration date | Issuer determined | — | — | Verify presence by issuer or edition. |

## Machine-readable data

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Machine-readable feature | Unverified | barcode, QR | Unverified. | Check for a local barcode or QR. Separate embedded fields from issuer verification results. IDNYC does not establish the payload for other municipalities. |

## Sources

- [Credential family and issuer reference](https://www.nyc.gov/site/idnyc/index.page)
