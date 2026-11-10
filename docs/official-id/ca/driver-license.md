# Driver’s licence / Permis de conduire

[Canada index](README.md) · `ca.driver-license`

- **Issuer** Province or territory
- **Typical format** varies
- **Evidence** Documented BC example, province and edition specific
- **Scope** Passenger, commercial, motorcycle and graduated variants as applicable

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
| Barcode | Computed | PDF417 where adopted · AAMVA | BC's ICBC confirms the license number in the barcode it documents. Other fields are unverified. | Verify symbology and payload by province and edition. |
| Magnetic stripe | Encoded | ICBC legacy card channel | Driver license number confirmed on the editions ICBC documents. | Check medium and edition, especially learner permits. |

## Sources

- [Credential family and issuer reference](https://fintrac-canafe.canada.ca/guidance-directives/client-clientele/guide11/11-eng)
- [AAMVA DL/ID card design standard](https://www.aamva.org/assets/best-practices%2C-guides%2C-standards%2C-manuals%2C-whitepapers/aamva-dl-id-card-design-standard-%282020%29)
- [ICBC technical guidance, section 7](https://partners.icbc.com/assets/3r0rg6eeZ7PkeCIz3K9Usq/dln-technical-guidelines.pdf)
