# Personal Identity Verification (PIV) card

[United States index](README.md) · `us.federal-piv`

- **Issuer** Issuing federal agency
- **Typical format** card
- **Evidence** Standard reference, verify agency implementation
- **Scope** HSPD-12 federal personnel credential

## Human-readable fields

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Given name(s) | Given | — | — | — |
| Surname(s) | Inherited / legal | — | — | — |
| Portrait | Captured | — | — | — |
| Issuing authority | Document metadata | — | — | — |
| Affiliation | Issuer determined | — | — | — |
| Expiration date | Issuer determined | — | — | — |
| Card serial | Issuer assigned | — | — | Verify presence by issuer or edition. |

## Machine-readable data

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| PIV smart chip | Encoded | NIST FIPS 201-3 | Can hold authentication certificates and a card or credential identifier. | The smart chip can hold identity authentication certificates and a card or credential identifier. Agency access decisions and backend personnel data are separate. Verify optional attributes and edition requirements against the PIV profile. |

## Sources

- [Credential family and issuer reference](https://boyle.house.gov/services/real-id-requirements-acceptable-alternatives-air-travel)
- [NIST FIPS 201-3](https://csrc.nist.gov/pubs/fips/201-3/final)
