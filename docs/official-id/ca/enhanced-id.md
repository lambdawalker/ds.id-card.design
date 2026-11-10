# Enhanced identification card

[Canada index](README.md) · `ca.enhanced-id`

- **Issuer** Participating provincial authority
- **Typical format** card
- **Evidence** Candidate fields, verify against specimen
- **Scope** Verify historical issuance and expiry by province

## Human-readable fields

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Given name(s) | Given | — | — | — |
| Surname(s) | Inherited / legal | — | — | — |
| Portrait | Captured | — | — | — |
| Date of birth | Recorded | — | — | — |
| Document number | Issuer assigned | — | — | — |
| Issuing province | Document metadata | — | — | — |
| Expiration date | Issuer determined | — | — | — |
| Citizenship indicator | Issuer determined | — | — | Verify presence by issuer or edition. |
| Border-travel legend | Document metadata | — | — | Verify presence by issuer or edition. |

## Machine-readable data

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Machine-readable feature | Unverified | RFID, MRZ, barcode | Unverified. | Some border credentials use RFID as a lookup identifier. Verify RFID and any printed MRZ or barcode for the particular enhanced product. The cited source describes the CBP lookup architecture. |

## Sources

- [Credential family and issuer reference](https://fintrac-canafe.canada.ca/guidance-directives/client-clientele/guide11/11-eng)
- [CBP border document privacy assessment](https://www.cbp.gov/sites/default/files/documents/privacy_july08_2.pdf)
