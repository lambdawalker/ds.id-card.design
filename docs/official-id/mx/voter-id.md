# Credencial para Votar

[Mexico index](README.md) · `mx.voter-id`

- **Issuer** INE
- **Typical format** card
- **Evidence** Issuer-confirmed QR and verifier output
- **Scope** Domestic and overseas issuance

## Human-readable fields

Check surname and given names, photo, date of birth, sex, signature, address or masked address, clave de elector, CURP, electoral section and validity. Record CIC and OCR identifiers separately where shown.

## Machine-readable data

INE documents rear verification QR codes on G/H and continued QR use on newer models. Its verifier shows names, sex, CURP, OCR and production date in the cited example. Treat this as verified app output, with raw field membership, model-specific changes and any issuer lookup tracked separately.

## Sources

- [Credential family and issuer reference](https://www.ine.mx/credencial/)
- [INE card models](https://portal.ine.mx/conoce-tu-credencial-para-votar/)
- [INE verification example](https://centralelectoral.ine.mx/wp-content/uploads/2024/01/Credencial_aclaracion-1.pdf)
