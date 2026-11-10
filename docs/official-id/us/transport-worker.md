# Transportation Worker Identification Credential (TWIC)

[United States index](README.md) · `us.transport-worker`

- **Issuer** TSA
- **Typical format** card
- **Evidence** Candidate fields, verify against specimen

## Human-readable fields

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Given name(s) | Given | — | — | — |
| Surname(s) | Inherited / legal | — | — | — |
| Portrait | Captured | — | — | — |
| Expiration date | Issuer determined | — | — | — |
| Document number | Issuer assigned | — | — | Verify presence by issuer or edition. |
| Card serial | Issuer assigned | — | — | Verify presence by issuer or edition. |
| Program name | Document metadata | — | — | — |

## Machine-readable data

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Machine-readable feature | Unverified | — | Unverified. | Check smart-card credential identifier and any certificate or biometric categories against TSA's applicable technical profile. No field-level payload established here. |

## Sources

- [Credential family and issuer reference](https://boyle.house.gov/services/real-id-requirements-acceptable-alternatives-air-travel)
