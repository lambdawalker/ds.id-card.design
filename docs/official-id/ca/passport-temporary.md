# Temporary passport

[Canada index](README.md) · `ca.passport-temporary`

- **Issuer** Canadian mission abroad
- **Typical format** booklet
- **Evidence** ICAO baseline, verify temporary booklet

## Human-readable fields

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Document type | Document metadata | — | — | — |
| Issuing country | Document metadata | — | — | — |
| Given name(s) | Given | — | — | — |
| Surname(s) | Inherited / legal | — | — | — |
| Passport number | Issuer assigned | — | — | — |
| Nationality | Issuer determined | — | — | — |
| Date of birth | Recorded | — | — | — |
| Sex marker | Recorded | — | — | — |
| Expiration date | Issuer determined | — | — | — |
| Portrait | Captured | — | — | — |
| Issue date | Issuer determined | — | — | Verify presence by issuer or edition. |
| Place of birth | Recorded | — | — | Verify presence by issuer or edition. |
| Issuing authority | Document metadata | — | — | Verify presence by issuer or edition. |
| Holder signature | Captured | — | — | Verify presence by issuer or edition. |
| National identifier | Issuer assigned | — | — | Verify presence by issuer or edition. |

## Machine-readable data

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Passport MRZ | Computed | ICAO Doc 9303 TD3 | Document type, issuing state, names, document number, nationality, date of birth, sex marker, expiration date, optional issuer data and check digits. | Check document edition. |
| Contactless chip | Unverified | — | Unverified. | Check the temporary booklet separately. |

## Sources

- [Credential family and issuer reference](https://www.canada.ca/en/immigration-refugees-citizenship/services/canadian-passports/document-types.html)
- [ICAO Doc 9303, Part 4](https://www.icao.int/publications/documents/9303_p4_cons_en.pdf)
