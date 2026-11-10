# Official personal credential catalog

Research snapshot · 2026-11-10

- [Mexico](official-id/mx/README.md) · 25 credential types
- [Canada](official-id/ca/README.md) · 26 credential types
- [United States](official-id/us/README.md) · 32 credential types

Each credential page records its stable key, issuer, typical format, visible fields, machine-readable data and evidence. Supporting records and jurisdiction coverage are listed in each country's index.

## Reading the field profiles

Each table separates the field's **data origin** from its **algorithm or format** and its **contents or inputs**. Coverage notes record what varies or still needs verification.

| Data origin | Meaning |
| --- | --- |
| Given | A personal given name. |
| Inherited / legal | A surname as recorded for the holder, including surnames acquired through legal changes. |
| Recorded | A fact or attribute taken from the holder's record. |
| Captured | A portrait or signature captured for the credential. |
| Issuer assigned | A value allocated by the issuer. Its assignment method may be unknown. |
| Issuer determined | A date, status, privilege or other value established by the issuer. |
| Document metadata | Information about the document, program or issuing authority. |
| Computed | A value derived from inputs or an encoded representation assembled from data. |
| Encoded | Data stored in a machine-readable medium. |
| Mixed categories | More than one origin applies. For example, CURP includes derived elements and an issuer-assigned disambiguator. |
| Unverified | The available evidence does not establish how the feature is produced. |

- **Human-readable fields** cover text and visual elements such as portraits and signatures. A field listed as a candidate needs an issuer specimen before it is required in a dataset schema.
- **Machine-readable data** distinguishes text zones such as the passport MRZ, optical codes such as QR and PDF417, magnetic stripes, and chips or RFID tags. Document what is carried on the artifact separately from what a verifier displays or retrieves.
- **Evidence** applies to a standard, issuer example or edition. An unknown code or payload remains unverified. Preserve jurisdiction, issuer, edition, medium and issuance period when adding product-level profiles. Shared border credentials can be linked across country catalogs by program.

The pages document field categories. Synthetic images can use fictional data and visibly marked specimen codes without real identifiers or issuer-verifiable payloads.
