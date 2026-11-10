# Tarjeta de Residente Permanente

[Mexico index](README.md) · `mx.resident-permanent`

- **Issuer** INM
- **Typical format** card
- **Evidence** Historical issuer specification, verify newer editions

## Human-readable fields

The circular lists name, nationality, country and date of birth, sex, portrait, immigration status, foreign-national identifier (NUE), expiration when applicable and CURP where required. The reverse includes signature, issuance place and date, migration document number, authority and renewal count where applicable. The circular excludes the renewal count for adult permanent residents.

## Machine-readable data

The circular lists a reverse OCR zone. Field-level payload, format and any QR or chip on later editions require specimen verification.

## Sources

- [Credential family and issuer reference](https://www.gob.mx/inm/articulos/no-te-dejes-enganar-215042)
- [INM circular, card fields](https://www.inm.gob.mx/static/marco_juridico/pdf/circulares/CIRCULAR_referente_documentos_migratorios_formatos_solicitud.pdf)
