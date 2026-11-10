# U.S. passport card

[United States index](README.md) · `us.passport-card`

- **Issuer** Department of State
- **Typical format** card
- **Evidence** Documented RFID architecture, verify printed MRZ fields

## Human-readable fields

Check surname and given names, card number, nationality, date of birth, sex marker, portrait, issue and expiration dates, and authority.

## Machine-readable data

Verify the printed machine-readable zone against the card edition. For supported RFID editions, the tag is a reference identifier used to retrieve the agency record. The retrieved biographic data is a separate channel. Verify the specific card generation and any printed machine-readable fields independently.

## Sources

- [Credential family and issuer reference](https://travel.state.gov/en/passports/apply/help/passport-card-vs-book.html)
- [CBP border document privacy assessment](https://www.cbp.gov/sites/default/files/documents/privacy_july08_2.pdf)
- [State Department passport card editions](https://travel.state.gov/content/travel/en/passports/passport-help/next-generation-passport.html)
