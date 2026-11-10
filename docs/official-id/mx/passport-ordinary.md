# Pasaporte ordinario

[Mexico index](README.md) · `mx.passport-ordinary`

- **Issuer** SRE
- **Typical format** booklet
- **Evidence** ICAO baseline, verify Mexican edition and chip use

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
| Contactless chip | Encoded | ICAO Doc 9303 logical data structure | MRZ data and digital facial image. | Electronic editions. Confirm any additional data groups. |

## Sources

- [Credential family and issuer reference](https://portales.sre.gob.mx/transparencia/transparencia-categorias/category/1735-i?download=60394%3Areglamento-de-pasaportes-y-del-documento-de-identidad-y-viaje&start=180)
- [ICAO Doc 9303, Part 4](https://www.icao.int/publications/documents/9303_p4_cons_en.pdf)
- [ICAO Doc 9303, Part 10](https://www.icao.int/publications/documents/9303_p10_cons_en.pdf)
