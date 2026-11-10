# Permiso para conducir

[Mexico index](README.md) · `mx.driver-permit`

- **Issuer** State or Mexico City licensing authority
- **Typical format** varies
- **Evidence** Candidate fields and issuer-confirmed QR example
- **Scope** Minor, provisional or learner permits where issued

## Human-readable fields

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Given name(s) | Given | — | — | — |
| Surname(s) | Inherited / legal | — | — | — |
| Portrait | Captured | — | — | — |
| Date of birth | Recorded | — | — | — |
| Driver license or permit number | Issuer assigned | — | — | Assignment policy varies by issuer. Randomness is unverified. |
| License class or category | Issuer determined | — | — | — |
| Issuing authority | Document metadata | — | — | — |
| Issue date | Issuer determined | — | — | — |
| Expiration date | Issuer determined | — | — | — |
| Holder signature | Captured | — | — | — |
| Restrictions | Issuer determined | — | — | Verify presence by issuer or edition. |
| CURP | Computed + issuer assigned | [RENAPO CURP composition](https://www.gob.mx/segob/renapo/es/articulos/sabes-como-se-conforma-tu-curp?idiom=es) | Derived from names, date of birth, sex and birthplace, with an issuer-assigned disambiguator and a check digit. The biographic inputs alone do not establish the official key. | Verify presence by issuer or edition. |
| Address | Recorded | — | — | Verify presence by issuer or edition. |
| Medical information | Recorded | — | — | Verify presence by issuer or edition. |
| Emergency contact | Recorded | — | — | Verify presence by issuer or edition. |

## Machine-readable data

| Field | Data origin | Algorithm or format | Contents or inputs | Coverage notes |
| --- | --- | --- | --- | --- |
| Verification code | Computed | QR · Chihuahua digital driver license example | Link to a state verification page that displays driver data. Embedded field list unverified. | The example establishes QR use for the digital license. Check permits, physical cards and other jurisdictions separately. |

## Sources

- [Credential family and issuer reference](https://www.dof.gob.mx/2026/INE/Acuerdo_INE_CNV02_ENE-2026.pdf)
- [Chihuahua digital license](https://sspe.chihuahua.gob.mx/supera-sspe-las-15-mil-licencias-digitales-registradas-en-chihuahua/)
