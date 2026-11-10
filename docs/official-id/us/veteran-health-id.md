# Veteran Health Identification Card (VHIC)

[United States index](README.md) · `us.veteran-health-id`

- **Issuer** Department of Veterans Affairs
- **Typical format** card
- **Evidence** Candidate fields, verify against specimen

## Human-readable fields

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Given name(s) | Given | — | — | — |
| Surname(s) | Inherited / legal | — | — | — |
| Portrait | Captured | — | — | — |
| Membership or affiliation number | Issuer assigned | — | — | Verify presence by issuer or edition. |
| Card number | Issuer assigned | — | — | Verify presence by issuer or edition. |
| Status or eligibility category | Issuer determined | — | — | Verify presence by issuer or edition. |
| Expiration date | Issuer determined | — | — | Verify presence by issuer or edition. |

## Machine-readable data

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Machine-readable feature | Unverified | barcode, stripe | Unverified. | Verify barcode or stripe and which member identifier it carries from an edition-specific VA source. Do not equate a healthcare identifier with a Social Security number. |

## Sources

- [Credential family and issuer reference](https://boyle.house.gov/services/real-id-requirements-acceptable-alternatives-air-travel)
