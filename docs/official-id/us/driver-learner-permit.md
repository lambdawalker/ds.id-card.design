# Learner’s permit

[United States index](README.md) · `us.driver-learner-permit`

- **Issuer** State, DC or territorial licensing authority
- **Typical format** varies
- **Evidence** U.S. REAL ID baseline, confirm jurisdiction and edition
- **Scope** Verify photo and format by issuer

## Human-readable fields

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Given name(s) | Given | — | — | — |
| Surname(s) | Inherited / legal | — | — | — |
| Portrait | Captured | — | — | — |
| Date of birth | Recorded | — | — | — |
| Address | Recorded | — | — | — |
| Driver license or permit number | Issuer assigned | — | — | Assignment policy varies by issuer. Randomness is unverified. |
| Issue date | Issuer determined | — | — | — |
| Expiration date | Issuer determined | — | — | — |
| Sex marker | Recorded | — | — | — |
| Holder signature | Captured | — | — | — |
| License class or category | Issuer determined | — | — | Verify presence by issuer or edition. |
| Endorsements | Issuer determined | — | — | Verify presence by issuer or edition. |
| Restrictions | Issuer determined | — | — | Verify presence by issuer or edition. |
| Physical descriptors | Recorded | — | — | Verify presence by issuer or edition. |

## Machine-readable data

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Barcode | Computed | PDF417 · 6 CFR §37.19 / AAMVA | Name, date of birth, sex marker, address, card number, issue and expiration dates, issuing jurisdiction, card design revision date and inventory control number. | REAL ID baseline where applicable. Optional driving privileges or descriptors depend on AAMVA edition and issuer adoption. Verify standard and temporary editions separately. |

## Sources

- [Credential family and issuer reference](https://www.uscis.gov/sites/default/files/document/forms/i-9.pdf)
- [6 CFR §37.19](https://www.law.cornell.edu/cfr/text/6/37.19)
- [AAMVA DL/ID card design standard](https://www.aamva.org/assets/best-practices%2C-guides%2C-standards%2C-manuals%2C-whitepapers/aamva-dl-id-card-design-standard-%282020%29)
