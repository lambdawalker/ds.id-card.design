# NEXUS card

[Canada index](README.md) · `ca.nexus`

- **Issuer** CBSA / U.S. CBP
- **Typical format** card
- **Evidence** Documented RFID architecture, verify card generation
- **Scope** Joint program, shared with US

## Human-readable fields

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Given name(s) | Given | — | — | — |
| Surname(s) | Inherited / legal | — | — | — |
| Portrait | Captured | — | — | — |
| Membership or affiliation number | Issuer assigned | — | — | Verify presence by issuer or edition. |
| Card serial | Issuer assigned | — | — | Verify presence by issuer or edition. |
| Program name | Document metadata | — | — | — |
| Expiration date | Issuer determined | — | — | — |
| Date of birth | Recorded | — | — | Verify presence by issuer or edition. |
| Nationality | Issuer determined | — | — | Verify presence by issuer or edition. |
| Issuing authority | Document metadata | — | — | Verify presence by issuer or edition. |

## Machine-readable data

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| RFID tag | Issuer assigned + encoded | RFID · CBP lookup | Reference identifier. Agency records can return biographic data separately. | Verify supported card generation. |

## Sources

- [Credential family and issuer reference](https://fintrac-canafe.canada.ca/guidance-directives/client-clientele/guide11/11-eng)
- [CBP border document privacy assessment](https://www.cbp.gov/sites/default/files/documents/privacy_july08_2.pdf)
