# Pasaporte diplomático

[Mexico index](README.md) · `mx.passport-diplomatic`

- **Issuer** SRE
- **Typical format** booklet
- **Evidence** ICAO baseline, verify Mexican edition and chip use

## Human-readable fields

Passport type, issuing country, surname and given names, passport number, nationality, date of birth, sex marker, expiration date and portrait. Also check issue date, place of birth, authority, signature and any country-specific identifier on the applicable edition.

## Machine-readable data

The passport MRZ carries document type, issuing state, names, document number, nationality, date of birth, sex marker, expiration date, optional issuer data and check digits. On electronic editions, the contactless chip stores MRZ data and a digital facial image under ICAO specifications. Confirm any additional data groups with the issuer.

## Sources

- [Credential family and issuer reference](https://portales.sre.gob.mx/transparencia/transparencia-categorias/category/1735-i?download=60394%3Areglamento-de-pasaportes-y-del-documento-de-identidad-y-viaje&start=180)
- [ICAO Doc 9303, Part 4](https://www.icao.int/publications/documents/9303_p4_cons_en.pdf)
- [ICAO Doc 9303, Part 10](https://www.icao.int/publications/documents/9303_p10_cons_en.pdf)
