# U.S. passport card

[United States index](README.md) · `us.passport-card`

- **Issuer** Department of State
- **Typical format** card
- **Evidence** Documented RFID architecture, verify printed MRZ fields

## Human-readable fields

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Given name(s) | Given | — | — | — |
| Surname(s) | Inherited / legal | — | — | — |
| Card number | Issuer assigned | — | — | — |
| Nationality | Issuer determined | — | — | — |
| Date of birth | Recorded | — | — | — |
| Sex marker | Recorded | — | — | — |
| Portrait | Captured | — | — | — |
| Issue date | Issuer determined | — | — | — |
| Expiration date | Issuer determined | — | — | — |
| Issuing authority | Document metadata | — | — | — |

## Machine-readable data

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Printed MRZ | Computed | Machine-readable zone | Edition-specific field list unverified. | Check the card edition. |
| RFID tag | Issuer assigned + encoded | RFID · CBP lookup | Reference identifier. Agency records can return biographic data separately. | Verify supported card generation. |

## Sources

- [Credential family and issuer reference](https://travel.state.gov/en/passports/apply/help/passport-card-vs-book.html)
- [CBP border document privacy assessment](https://www.cbp.gov/sites/default/files/documents/privacy_july08_2.pdf)
- [State Department passport card editions](https://travel.state.gov/content/travel/en/passports/passport-help/next-generation-passport.html)
