# Enhanced Tribal Card (ETC)

[United States index](README.md) · `us.enhanced-tribal-id`

- **Issuer** Participating tribal nation
- **Typical format** card
- **Evidence** Candidate fields, verify against specimen

## Human-readable fields

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Given name(s) | Given | — | — | — |
| Surname(s) | Inherited / legal | — | — | — |
| Portrait | Captured | — | — | — |
| Date of birth | Recorded | — | — | — |
| Tribe or First Nation | Document metadata | — | — | — |
| Registration or enrollment number | Issuer assigned | — | — | Verify presence by issuer or edition. |
| Document number | Issuer assigned | — | — | Verify presence by issuer or edition. |
| Expiration date | Issuer determined | — | — | — |
| Holder signature | Captured | — | — | — |
| Citizenship indicator | Issuer determined | — | — | Verify presence by issuer or edition. |
| Border-travel legend | Document metadata | — | — | Verify presence by issuer or edition. |

## Machine-readable data

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Machine-readable feature | Unverified | barcode, MRZ | Unverified. | Verify individual tribal card barcodes and MRZ. Enhanced border-enabled editions may use a lookup identifier; the CBP architecture alone does not establish technology or fields for a specific nation. |

## Sources

- [Credential family and issuer reference](https://boyle.house.gov/services/real-id-requirements-acceptable-alternatives-air-travel)
- [CBP border document privacy assessment](https://www.cbp.gov/sites/default/files/documents/privacy_july08_2.pdf)
