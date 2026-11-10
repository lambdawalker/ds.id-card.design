# FAST card

[Canada index](README.md) · `ca.fast`

- **Issuer** CBSA / U.S. CBP for northern-border program
- **Typical format** card
- **Evidence** Documented RFID architecture, verify card generation
- **Scope** Track northern and southern program context separately

## Human-readable fields

Check printed name, portrait, membership or card number, program name, expiry, and any date of birth, nationality or issuer marks on the applicable card. Treat membership number and physical card serial as separate fields when both appear.

## Machine-readable data

For supported RFID editions, the tag is a reference identifier used to retrieve the agency record. The retrieved biographic data is a separate channel. Verify the specific card generation and any printed machine-readable fields independently.

## Sources

- [Credential family and issuer reference](https://www.help.cbp.gov/s/article/Article-1885)
- [CBP border document privacy assessment](https://www.cbp.gov/sites/default/files/documents/privacy_july08_2.pdf)
