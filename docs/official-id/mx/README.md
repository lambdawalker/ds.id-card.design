# Mexico

[Catalog index](../../official-id-catalog.md)

| Credential | Key | Issuer | Typical format |
| --- | --- | --- | --- |
| [Pasaporte ordinario](./passport-ordinary.md) | `mx.passport-ordinary` | SRE | booklet |
| [Pasaporte oficial](./passport-official.md) | `mx.passport-official` | SRE | booklet |
| [Pasaporte diplomático](./passport-diplomatic.md) | `mx.passport-diplomatic` | SRE | booklet |
| [Documento de Identidad y Viaje](./travel-identity.md) | `mx.travel-identity` | SRE | travel document |
| [Credencial para Votar](./voter-id.md) | `mx.voter-id` | INE | card |
| [Certificado de Matrícula Consular](./consular-id.md) | `mx.consular-id` | SRE / Mexican consulates | card |
| [Licencia de conducir](./driver-license.md) | `mx.driver-license` | State or Mexico City licensing authority | varies |
| [Permiso para conducir](./driver-permit.md) | `mx.driver-permit` | State or Mexico City licensing authority | varies |
| [Licencia Federal Digital de Conductor](./federal-driver-license.md) | `mx.federal-driver-license` | SICT | digital |
| [Cartilla del Servicio Militar Nacional](./military-service.md) | `mx.military-service` | SEDENA | document |
| [Cédula profesional](./professional-id.md) | `mx.professional-id` | SEP / Dirección General de Profesiones | varies |
| [Credencial INAPAM](./senior-id.md) | `mx.senior-id` | INAPAM | card |
| [Tarjeta de Residente Temporal](./resident-temporary.md) | `mx.resident-temporary` | INM | card |
| [Tarjeta de Residente Temporal Estudiante](./resident-student.md) | `mx.resident-student` | INM | card |
| [Tarjeta de Residente Permanente](./resident-permanent.md) | `mx.resident-permanent` | INM | card |
| [Tarjeta de Visitante Regional](./visitor-regional.md) | `mx.visitor-regional` | INM | card |
| [Tarjeta de Visitante Trabajador Fronterizo](./visitor-border-worker.md) | `mx.visitor-border-worker` | INM | card |
| [Tarjeta de Visitante por Razones Humanitarias](./visitor-humanitarian.md) | `mx.visitor-humanitarian` | INM | card |
| [Tarjeta de Visitante con Fines de Adopción](./visitor-adoption.md) | `mx.visitor-adoption` | INM | card |
| [Tarjeta de Visitante con Permiso para Realizar Actividades Remuneradas](./visitor-remunerated.md) | `mx.visitor-remunerated` | INM | card |
| [CURP temporal con fotografía](./temporary-photo-curp.md) | `mx.temporary-photo-curp` | INM / population registry | document |
| [Constancia o certificado de identidad u origen](./local-identity-certificate.md) | `mx.local-identity-certificate` | Municipal authority | document |
| [Government employee, military or public-safety ID](./government-personnel-id.md) | `mx.government-personnel-id` | Issuing public authority | varies |
| [Credencial de identificación de persona derechohabiente](./public-health-beneficiary-id.md) | `mx.public-health-beneficiary-id` | Federal, state or municipal public health institution | varies |
| [Public-school or INEA student credential](./public-school-id.md) | `mx.public-school-id` | Public educational institution / INEA | varies |

## Supporting documents

Birth registration and certified birth certificate, naturalization letter or certificate, Mexican nationality certificate and declarations, ordinary CURP record, visas, Forma Migratoria Múltiple (FMM), refugee application acknowledgments, and public education records. Research biometric CURP and historical child identity credentials separately by program and issuance period. [mx-criteria](https://www.dof.gob.mx/2026/INE/Acuerdo_INE_CNV02_ENE-2026.pdf), [mx-inm](https://www.gob.mx/inm/articulos/no-te-dejes-enganar-215042), [mx-curp](https://www.chihuahua.gob.mx/prensa/arranca-en-chihuahua-programa-piloto-de-curp-biometrica)

## Issuer coverage

**Mexico · 32 federal entities.** Aguascalientes, Baja California, Baja California Sur, Campeche, Chiapas, Chihuahua, Ciudad de México, Coahuila, Colima, Durango, Estado de México, Guanajuato, Guerrero, Hidalgo, Jalisco, Michoacán, Morelos, Nayarit, Nuevo León, Oaxaca, Puebla, Querétaro, Quintana Roo, San Luis Potosí, Sinaloa, Sonora, Tabasco, Tamaulipas, Tlaxcala, Veracruz, Yucatán and Zacatecas. Check local digital editions, license classes, provisional permits, and municipal identity letters. [mx-criteria](https://www.dof.gob.mx/2026/INE/Acuerdo_INE_CNV02_ENE-2026.pdf)

## Complementary identity dataset planning

See the [photo dataset field-coverage report](complementary-dataset.md) and
[machine-readable field inventory](complementary-fields.yaml) for fields that are
ready, derivable in code, transformable with AI, or missing from `lambdaWalker/ds.photo-id`.
The inventory separates current input availability from future generation methods.
