# Referencias Normativas del NIST Cybersecurity Framework 2.0 (CSF 2.0)
## Documentación para Organizaciones Militares, Gubernamentales e Infraestructura Crítica — Colombia

> **Fuente:** Archivo `csf2.xlsx`, Hoja `CSF 2.0`  
> **Versión del marco:** NIST CSF 2.0 (www.nist.gov/cyberframework)  
> **Propósito:** Documentar cada referencia normativa (Informative References) citada en el CSF 2.0, con énfasis en ciberseguridad y ciberdefensa para Colombia.

---

## Tabla de Contenidos

1. [CCMv4.0 — Cloud Controls Matrix](#1-ccmv40--cloud-controls-matrix)
2. [ISO/IEC 27001:2022](#2-isoiec-270012022)
3. [NICE Framework (NIST SP 800-181r1)](#3-nice-framework-nist-sp-800-181r1)
4. [PCI DSS v4.0](#4-pci-dss-v40)
5. [NIST SP 800-53 Rev. 5](#5-nist-sp-800-53-rev-5)
6. [SCF — Secure Controls Framework](#6-scf--secure-controls-framework)
7. [CIS Controls v8](#7-cis-controls-v8)
8. [COBIT 2019](#8-cobit-2019)
9. [ISA/IEC 62443](#9-isaiec-62443)
10. [NIST SP 800-37 (RMF)](#10-nist-sp-800-37-rmf)
11. [NIST SP 800-39](#11-nist-sp-800-39)
12. [NIST SP 800-30](#12-nist-sp-800-30)
13. [NIST SP 800-161r1 (C-SCRM)](#13-nist-sp-800-161r1-c-scrm)
14. [NIST SP 800-82 (OT/ICS)](#14-nist-sp-800-82-ottics)
15. [NIST SP 800-61r2 (Incident Response)](#15-nist-sp-800-61r2-incident-response)
16. [NIST SP 800-137 (ISCM)](#16-nist-sp-800-137-iscm)
17. [NIST SP 800-218 (SSDF)](#17-nist-sp-800-218-ssdf)
18. [NIST SP 800-160 Vol. 1](#18-nist-sp-800-160-vol-1)
19. [NIST AI RMF 1.0](#19-nist-ai-rmf-10)
20. [SOC 2 (AICPA TSC)](#20-soc-2-aicpa-tsc)

---

## Mapa de Funciones y Subcategorías Activas del CSF 2.0

El CSF 2.0 organiza 106 subcategorías activas en 6 funciones:

| Función | Código | Subcategorías activas |
|---------|--------|----------------------|
| GOVERN  | GV     | 31                   |
| PROTECT | PR     | 22                   |
| IDENTIFY | ID    | 21                   |
| RESPOND | RS     | 13                   |
| DETECT  | DE     | 11                   |
| RECOVER | RC     | 8                    |

---

## 1. CCMv4.0 — Cloud Controls Matrix

### Referencia: CCMv4.0 (Cloud Controls Matrix versión 4.0)

**Contexto e importancia:**

**¿Qué es este marco/norma?**  
El Cloud Controls Matrix (CCM) versión 4.0 es un marco de controles de seguridad desarrollado por la Cloud Security Alliance (CSA), diseñado específicamente para entornos de computación en la nube. Comprende 197 objetivos de control organizados en 17 dominios, que cubren desde la gestión de identidades y accesos hasta la seguridad física e inteligencia de amenazas.

**¿Por qué es relevante en ciberseguridad y ciberdefensa?**  
En un contexto de ciberdefensa, las organizaciones gubernamentales y militares dependen cada vez más de infraestructuras en la nube (pública, privada o híbrida) para el procesamiento de información clasificada y operaciones críticas. El CCMv4.0 proporciona controles específicos para asegurar que los proveedores de nube cumplan con los requisitos de seguridad operacional, continuidad del servicio y protección de datos soberanos.

**¿Cuál es su alcance principal?**  
Proveedores de servicios en la nube (CSP), consumidores de nube y terceros que gestionan datos o sistemas en entornos cloud. Cubre controles técnicos, operativos y de gobernanza.

**Aplicabilidad en el CSF 2.0:**

| Subcategoría CSF 2.0 | Dominio CCMv4.0 relacionado | Cómo ayuda |
|----------------------|----------------------------|------------|
| GV.SC-07: Riesgos de proveedores son comprendidos | STA (Supply Chain Management) | Evalúa seguridad de proveedores cloud |
| PR.AA-01: Identidades y credenciales gestionadas | IAM (Identity & Access Management) | Control de acceso a servicios en nube |
| PR.DS-01: Datos en reposo protegidos | EKM (Encryption & Key Management) | Cifrado de datos almacenados en cloud |
| PR.DS-02: Datos en tránsito protegidos | EKM / IVS | Protección de comunicaciones cloud |
| DE.CM-09: Hardware y software monitoreados | LOG (Logging & Monitoring) | Monitoreo de eventos en entornos cloud |
| GV.SC-05: Requisitos de seguridad en cadena de suministro | STA | Cláusulas contractuales con proveedores cloud |

**Ejemplo práctico en Colombia — Organización Militar/Gubernamental:**

> La **Armada Nacional de Colombia** requiere migrar su sistema de inteligencia marítima a una nube privada. Aplicando CCMv4.0, el equipo de ciberdefensa evalúa a cada proveedor candidato contra los controles del dominio STA (Supply Chain), garantizando que los datos de patrullaje de aguas territoriales no salgan de soberanía nacional (subcategoría GV.SC-07 del CSF 2.0). Además, mediante los controles IAM del CCMv4.0 se implementa autenticación multifactor para todos los analistas de inteligencia que acceden al sistema desde bases remotas, alineado con PR.AA-03 del CSF 2.0.

---

## 2. ISO/IEC 27001:2022

### Referencia: ISO/IEC 27001:2022

**Contexto e importancia:**

**¿Qué es este marco/norma?**  
ISO/IEC 27001:2022 es el estándar internacional para Sistemas de Gestión de Seguridad de la Información (SGSI). Publicado por la Organización Internacional de Normalización (ISO) y la Comisión Electrotécnica Internacional (IEC), define los requisitos para establecer, implementar, mantener y mejorar continuamente un SGSI. La versión 2022 incorpora 93 controles en el Anexo A, organizados en 4 temas: Organizacional, Personal, Físico y Tecnológico.

**¿Por qué es relevante en ciberseguridad y ciberdefensa?**  
ISO 27001 es el estándar de facto global para la gestión de seguridad de la información. Para entidades gubernamentales colombianas, su implementación cumple con los lineamientos del **Modelo de Seguridad y Privacidad de la Información (MSPI)** del MinTIC y del **CONPES 3995** de política nacional de confianza y seguridad digital. Es también base para la certificación que demuestra madurez ante organismos internacionales y aliados estratégicos.

**¿Cuál es su alcance principal?**  
Cualquier organización, independientemente de su tamaño o sector, que desee gestionar sistemáticamente los riesgos asociados a la seguridad de la información, asegurando confidencialidad, integridad y disponibilidad.

**Aplicabilidad en el CSF 2.0:**

| Subcategoría CSF 2.0 | Control ISO 27001:2022 | Cómo ayuda |
|----------------------|------------------------|------------|
| GV.PO-01: Política de gestión de riesgos establecida | A.5.1 Políticas de seguridad | Marco para crear política de SI |
| GV.RR-02: Roles y responsabilidades definidos | A.5.2 Roles y responsabilidades | Asignación formal de funciones |
| ID.RA-01: Vulnerabilidades identificadas y registradas | A.8.8 Gestión de vulnerabilidades | Proceso sistemático de evaluación |
| PR.AT-01: Personal con concienciación y formación | A.6.3 Concienciación, educación y formación | Programa formal de sensibilización |
| PR.DS-01: Datos en reposo protegidos | A.8.24 Uso de criptografía | Cifrado de información clasificada |
| DE.CM-01: Redes monitoreadas | A.8.16 Monitoreo de actividades | SOC y gestión de eventos de seguridad |
| RS.MA-01: Plan de respuesta a incidentes ejecutado | A.5.26 Respuesta a incidentes de SI | Proceso formal de gestión de incidentes |
| RC.RP-01: Plan de recuperación ejecutado | A.5.29 Seguridad de la información durante interrupción | Continuidad del negocio |

**Ejemplo práctico en Colombia — Organización Gubernamental:**

> El **Ministerio de Defensa Nacional de Colombia** certifica su SGSI bajo ISO 27001:2022 para todos sus sistemas de información clasificados. Esto permite demostrar ante la OTAN y aliados de la Alianza del Pacífico que los datos de inteligencia compartidos se gestionan bajo estándares internacionales auditados. La certificación facilita, por ejemplo, el intercambio de información de amenazas transnacionales (narcoterrorismo, ciberataques patrocinados por Estados) con agencias como la DEA o INTERPOL, alineando GV.PO-01 y GV.RR-02 del CSF 2.0 con controles formalmente auditados.

---

## 3. NICE Framework (NIST SP 800-181r1)

### Referencia: NICE Framework — National Initiative for Cybersecurity Education

**Contexto e importancia:**

**¿Qué es este marco/norma?**  
El NICE Cybersecurity Workforce Framework (NIST SP 800-181 Rev. 1) es un marco desarrollado por NIST que categoriza y describe el trabajo en ciberseguridad. Define **Áreas de Trabajo**, **Roles de Trabajo** y **Tareas/Conocimientos/Habilidades/Destrezas (TKSA)** necesarios para la fuerza laboral de ciberseguridad. Organiza el trabajo de ciberseguridad en 7 categorías y más de 50 roles especializados.

**¿Por qué es relevante en ciberseguridad y ciberdefensa?**  
Una organización de ciberdefensa es tan fuerte como las capacidades de su personal. El NICE Framework permite estructurar los perfiles de cargo del talento humano en ciberseguridad, identificar brechas de capacidades y diseñar programas de formación y entrenamiento alineados con las funciones reales de defensa cibernética. Es especialmente relevante para el **Comando Conjunto Cibernético (CCOCI)** de las Fuerzas Militares de Colombia.

**¿Cuál es su alcance principal?**  
Empleadores, educadores e individuos que necesitan un lenguaje común para describir, reclutar, desarrollar y retener talento en ciberseguridad.

**Aplicabilidad en el CSF 2.0:**

| Subcategoría CSF 2.0 | Categoría NICE relacionada | Cómo ayuda |
|----------------------|---------------------------|------------|
| GV.RR-02: Roles y autoridades establecidos | Todas las categorías NICE | Define roles formales de ciberseguridad |
| GV.RR-04: Ciberseguridad en prácticas de RRHH | Operate & Maintain / Protect & Defend | Perfiles de cargo para contratación |
| PR.AT-01: Personal con concienciación | Educationally Related Work | Programas de formación basados en roles |
| PR.AT-02: Personal en roles especializados entrenado | Protect & Defend / Analyze / Collect & Operate | Certificaciones y entrenamiento avanzado |
| DE.CM-01: Redes monitoreadas | Operate & Maintain / Analyze | Operadores de SOC cualificados |
| RS.MA-01: Plan de respuesta ejecutado | Incident Response | Personal certificado en respuesta a incidentes |
| ID.RA-02: Inteligencia de amenazas recibida | Analyze / Collect & Operate | Analistas de ciberinteligencia |

**Ejemplo práctico en Colombia — Organización Militar:**

> El **Ejército Nacional de Colombia** usa el NICE Framework para estructurar su plantilla de ciberdefensa en el CCOCI. Define roles como: Analista de Ciberinteligencia (corresponde al Work Role "All-Source Analyst"), Operador de SOC (Work Role "Cyber Defense Analyst") y Respondedor de Incidentes (Work Role "Cyber Defense Incident Responder"). Cada rol tiene asociado un conjunto de competencias medibles. Esto permite a RR.HH. reclutar con precisión (alineando GV.RR-04 del CSF 2.0) y al CCOCI diseñar ejercicios de entrenamiento como el "Cyber Range" conjunto con la Policía Nacional, alineado con PR.AT-02 del CSF 2.0.

---

## 4. PCI DSS v4.0

### Referencia: PCI DSS v4.0 — Payment Card Industry Data Security Standard

**Contexto e importancia:**

**¿Qué es este marco/norma?**  
El Estándar de Seguridad de Datos de la Industria de Tarjetas de Pago (PCI DSS) versión 4.0, publicado en 2022 por el PCI Security Standards Council, establece requisitos técnicos y operativos para proteger los datos de titulares de tarjetas de pago. Comprende 12 requisitos principales y más de 250 controles específicos.

**¿Por qué es relevante en ciberseguridad y ciberdefensa?**  
Aunque PCI DSS surge del sector financiero, es altamente relevante para entidades gubernamentales que gestionan pagos electrónicos (impuestos, servicios públicos, multas) y para el sector defensa cuando administra sistemas de nómina, compras de equipamento y logística con pagos digitales. La versión 4.0 incorpora enfoques basados en riesgo que la alinean mejor con marcos de ciberdefensa.

**¿Cuál es su alcance principal?**  
Cualquier entidad que almacene, procese o transmita datos de titulares de tarjetas de pago o datos de autenticación confidenciales.

**Aplicabilidad en el CSF 2.0:**

| Subcategoría CSF 2.0 | Requisito PCI DSS v4.0 | Cómo ayuda |
|----------------------|------------------------|------------|
| PR.DS-01: Datos en reposo protegidos | Req. 3: Proteger datos almacenados del titular | Cifrado de datos financieros |
| PR.DS-02: Datos en tránsito protegidos | Req. 4: Cifrar transmisión de datos | TLS/SSL en canales de pago |
| PR.AA-01: Identidades y credenciales gestionadas | Req. 8: Identificar y autenticar acceso | MFA para sistemas de pago |
| PR.AA-05: Permisos de acceso definidos | Req. 7: Restringir acceso según necesidad | Principio de mínimo privilegio |
| PR.PS-01: Prácticas de gestión de configuración | Req. 2: Aplicar configuraciones seguras | Hardening de sistemas de pago |
| DE.CM-01: Redes monitoreadas | Req. 10: Registrar y monitorear todo acceso | SIEM para detección de fraude |
| DE.CM-09: Hardware y software monitoreados | Req. 5: Protección contra malware | EDR en terminales de pago |
| ID.RA-01: Vulnerabilidades identificadas | Req. 6: Gestión de vulnerabilidades | Escaneos trimestrales y pentest anual |

**Ejemplo práctico en Colombia — Organización Gubernamental:**

> La **Dirección de Impuestos y Aduanas Nacionales (DIAN)** procesa millones de pagos electrónicos anuales por concepto de impuestos. Al implementar PCI DSS v4.0, el equipo de ciberseguridad de la DIAN asegura que los datos de las tarjetas de contribuyentes estén cifrados en reposo (alineando PR.DS-01 del CSF 2.0) y que se monitoreen en tiempo real las transacciones sospechosas (DE.CM-01). Un incidente de filtración de datos de pago en una entidad del Estado generaría pérdida de confianza ciudadana y vulneraría la seguridad económica nacional, lo que convierte a PCI DSS en un control de ciberdefensa estratégico.

---

## 5. NIST SP 800-53 Rev. 5

### Referencia: NIST SP 800-53 Rev. 5 — Security and Privacy Controls for Information Systems and Organizations

**Contexto e importancia:**

**¿Qué es este marco/norma?**  
El NIST Special Publication 800-53 Revisión 5 es el catálogo más completo de controles de seguridad y privacidad para sistemas de información federales de EE.UU., publicado por NIST en 2020. Contiene más de 1,000 controles y mejoras de control distribuidos en 20 familias, que van desde Control de Acceso (AC) hasta Planificación de Contingencias (CP) y Respuesta a Incidentes (IR).

**¿Por qué es relevante en ciberseguridad y ciberdefensa?**  
SP 800-53 Rev. 5 es la referencia técnica más detallada y completa del ecosistema NIST. Es el estándar base para sistemas de información del gobierno de EE.UU. (bajo FISMA) y es adoptado globalmente como referencia de mejores prácticas. Para Colombia, es especialmente relevante dado que el CSF 2.0 fue diseñado para mapear directamente con SP 800-53, y organizaciones como el **ColCERT** y las Fuerzas Militares lo usan como referencia técnica.

**¿Cuál es su alcance principal?**  
Sistemas de información federales de EE.UU. y cualquier organización que adopte el marco NIST. Incluye sistemas de control industrial (OT/ICS) y sistemas de seguridad nacional.

**Aplicabilidad en el CSF 2.0 — Ejemplos clave:**

| Subcategoría CSF 2.0 | Familia SP 800-53 Rev. 5 | Controles clave |
|----------------------|--------------------------|-----------------|
| GV.PO-01: Política de riesgos establecida | PL (Planning) / PM (Program Management) | PL-1, PM-9 |
| GV.OC-03: Requisitos legales comprendidos | SA (System Acquisition) | SA-9, SA-15 |
| ID.AM-01: Inventario de hardware mantenido | CM (Config. Management) | CM-8 |
| ID.AM-02: Inventario de software mantenido | CM | CM-8, CM-11 |
| ID.RA-01: Vulnerabilidades identificadas | RA (Risk Assessment) | RA-3, RA-5 |
| PR.AA-01: Identidades y credenciales gestionadas | IA (Identification & Authentication) | IA-2, IA-5 |
| PR.AA-03: Usuarios autenticados | IA | IA-2, IA-8 |
| PR.AA-05: Permisos de acceso definidos | AC (Access Control) | AC-2, AC-6 |
| PR.DS-01: Datos en reposo protegidos | SC (System & Comm. Protection) | SC-28 |
| PR.DS-02: Datos en tránsito protegidos | SC | SC-8 |
| PR.PS-04: Registros de log generados | AU (Audit & Accountability) | AU-2, AU-12 |
| DE.CM-01: Redes monitoreadas | SI (System & Information Integrity) | SI-4 |
| DE.AE-02: Eventos adversos analizados | IR (Incident Response) | IR-4 |
| RS.MA-01: Plan de respuesta ejecutado | IR | IR-8 |
| RC.RP-01: Recuperación ejecutada | CP (Contingency Planning) | CP-10 |

**Ejemplo práctico en Colombia — Organización Militar:**

> El **Comando Conjunto Cibernético (CCOCI)** de Colombia adopta SP 800-53 Rev. 5 como catálogo técnico para sus sistemas de mando y control (C2). Para cada sistema clasificado, se selecciona una línea base de controles (Bajo, Moderado o Alto impacto según FIPS 199) y se adapta al contexto operacional. Por ejemplo, para el sistema de comunicaciones tácticas del Ejército se implementa IA-2(1) — Autenticación multifactor para acceso de red — alineado con PR.AA-03 del CSF 2.0. El control AU-2 (Eventos auditables) asegura que todas las acciones en sistemas clasificados sean trazables, cumpliendo DE.CM-03 del CSF 2.0 y los requisitos de no repudio operacional.

---

## 6. SCF — Secure Controls Framework

### Referencia: SCF — Secure Controls Framework

**Contexto e importancia:**

**¿Qué es este marco/norma?**  
El Secure Controls Framework (SCF) es un metamarco de controles de ciberseguridad y privacidad de uso libre, desarrollado por una iniciativa comunitaria. Actúa como un "superconjunto" que mapea y armoniza más de 100 marcos y regulaciones diferentes (ISO 27001, NIST SP 800-53, PCI DSS, HIPAA, GDPR, etc.) en un único catálogo de controles. Incluye más de 1,000 controles organizados en 34 dominios.

**¿Por qué es relevante en ciberseguridad y ciberdefensa?**  
El SCF es especialmente útil cuando una organización debe cumplir simultáneamente con múltiples marcos normativos — situación muy común en entidades gubernamentales colombianas que deben cumplir con el MSPI del MinTIC, el CONPES 3995, estándares internacionales ISO y referencias del NIST. El SCF permite un enfoque de "compliance único" que satisface múltiples marcos a la vez, reduciendo esfuerzo duplicado.

**¿Cuál es su alcance principal?**  
Organizaciones de cualquier tamaño y sector que necesiten gestionar el cumplimiento de múltiples marcos regulatorios o normativos de forma eficiente.

**Aplicabilidad en el CSF 2.0:**

| Subcategoría CSF 2.0 | Dominio SCF relacionado | Cómo ayuda |
|----------------------|------------------------|------------|
| GV.PO-01: Política de riesgos establecida | GOV (Governance) | Políticas integradas que satisfacen múltiples marcos |
| GV.RM-01: Objetivos de gestión de riesgos | RSK (Risk Management) | Gestión unificada de riesgos multi-marco |
| GV.SC-01: Programa de gestión de riesgos en cadena de suministro | THR (Threat Management) | Control de proveedores bajo múltiples normativas |
| ID.RA-01: Vulnerabilidades identificadas | VUL (Vulnerability Management) | Proceso unificado de gestión de vulnerabilidades |
| PR.AA-05: Permisos de acceso definidos | IAO (Identity & Access Management) | Control de acceso que cumple múltiples marcos |
| PR.DS-01: Datos en reposo protegidos | CRY (Cryptography) | Cifrado que satisface ISO, NIST y PCI DSS |
| DE.CM-01: Redes monitoreadas | MON (Continuous Monitoring) | Monitoreo unificado para cumplimiento multi-norma |

**Ejemplo práctico en Colombia — Organización Gubernamental:**

> La **Agencia Nacional de Infraestructuras (ANI)** administra sistemas de información para concesiones de infraestructura crítica (carreteras, puertos, aeropuertos). Debe cumplir simultáneamente con: MSPI del MinTIC, ISO 27001:2022, normas de la Contraloría General, y referencias del NIST CSF 2.0 exigidas por socios internacionales. En lugar de implementar cuatro programas de seguridad separados, el SCF permite mapear todos los controles en una sola estructura. Así, el control SCF "GOV-01 Cybersecurity & Data Protection Governance" satisface a la vez GV.PO-01 del CSF 2.0, A.5.1 de ISO 27001 y PM-9 de SP 800-53, reduciendo el esfuerzo de auditoría en un 60%.

---

## 7. CIS Controls v8

### Referencia: CIS Controls v8 — Center for Internet Security Critical Security Controls

**Contexto e importancia:**

**¿Qué es este marco/norma?**  
Los CIS Controls versión 8 son un conjunto de 18 controles de seguridad prioritizados, desarrollados por el Center for Internet Security (CIS). Basados en las amenazas más comunes observadas en el mundo real, están organizados en 3 grupos de implementación (IG1, IG2, IG3) que permiten una adopción escalonada según la madurez de la organización. Incluyen 153 salvaguardas específicas.

**¿Por qué es relevante en ciberseguridad y ciberdefensa?**  
Los CIS Controls son ampliamente reconocidos como los controles de mayor impacto para reducir el riesgo cibernético más común. Para Colombia, son especialmente prácticos porque ofrecen una ruta de implementación clara y priorizada, ideal para entidades gubernamentales que están iniciando o madurando su programa de ciberseguridad. El IG1 es considerado "higiene cibernética básica" alcanzable por cualquier organización.

**¿Cuál es su alcance principal?**  
Cualquier organización, desde pequeñas entidades gubernamentales municipales hasta grandes agencias de defensa, con implementación escalonada según capacidades.

**Aplicabilidad en el CSF 2.0:**

| Subcategoría CSF 2.0 | CIS Control v8 | Grupo (IG) |
|----------------------|----------------|------------|
| ID.AM-01: Inventario de hardware | Control 1: Inventario y control de activos enterprise | IG1 |
| ID.AM-02: Inventario de software | Control 2: Inventario y control de activos de software | IG1 |
| PR.PS-01: Gestión de configuración | Control 4: Configuración segura de activos enterprise | IG1 |
| PR.AA-01: Identidades y credenciales gestionadas | Control 5: Gestión de cuentas | IG1 |
| PR.AA-05: Permisos de acceso | Control 6: Gestión de control de acceso | IG1 |
| PR.DS-11: Backups creados y protegidos | Control 11: Recuperación de datos | IG1 |
| DE.CM-01: Redes monitoreadas | Control 13: Monitoreo y defensa de la red | IG2 |
| ID.RA-01: Vulnerabilidades identificadas | Control 7: Gestión continua de vulnerabilidades | IG1 |
| PR.PS-05: Software no autorizado prevenido | Control 2 / Control 10 | IG1/IG2 |
| RS.MA-01: Plan de respuesta ejecutado | Control 17: Gestión de respuesta a incidentes | IG2 |

**Ejemplo práctico en Colombia — Infraestructura Crítica:**

> **Ecopetrol**, como infraestructura crítica nacional del sector energético, implementa los CIS Controls v8 como base de su programa de ciberseguridad OT/IT. Comienza con IG1 (higiene básica): inventario de activos industriales (ID.AM-01 del CSF 2.0), gestión de cuentas privilegiadas en sistemas SCADA (PR.AA-01), y backups de configuraciones de PLCs (PR.DS-11). Esto protege la infraestructura de refinación frente a ataques tipo ransomware similares al incidente de Colonial Pipeline en EE.UU. (2021). La implementación escalonada IG1→IG2→IG3 permite una mejora continua medible que el CCOCI puede verificar como parte del modelo nacional de gestión de ciberriesgos.

---

## 8. COBIT 2019

### Referencia: COBIT 2019 — Control Objectives for Information and Related Technologies

**Contexto e importancia:**

**¿Qué es este marco/norma?**  
COBIT 2019, publicado por ISACA, es un marco de gobernanza y gestión de tecnologías de información empresarial. Define 40 objetivos de gobernanza/gestión organizados en 5 dominios: Evaluar, Dirigir y Monitorear (EDM); Alinear, Planificar y Organizar (APO); Construir, Adquirir e Implementar (BAI); Entregar, Servir y Dar Soporte (DSS); Monitorear, Evaluar y Valorar (MEA).

**¿Por qué es relevante en ciberseguridad y ciberdefensa?**  
COBIT 2019 conecta la gobernanza de TI con los objetivos estratégicos de la organización. Para entidades gubernamentales colombianas, es relevante porque alinea la ciberseguridad con los procesos de rendición de cuentas, auditoría y control interno exigidos por la Contraloría General de la República y las normas de gestión pública (MIPG - Modelo Integrado de Planeación y Gestión).

**¿Cuál es su alcance principal?**  
Alta dirección, juntas directivas, gerentes de TI y auditores que necesitan asegurar que la TI crea valor y gestiona riesgos de forma alineada con los objetivos organizacionales.

**Aplicabilidad en el CSF 2.0:**

| Subcategoría CSF 2.0 | Objetivo COBIT 2019 | Cómo ayuda |
|----------------------|--------------------|-|------------|
| GV.OC-01: Misión organizacional comprendida | EDM01 (Marco de Gobernanza) | Alinea ciberseguridad con misión |
| GV.RM-01: Objetivos de gestión de riesgos | EDM03 (Aseguramiento de riesgos) | Integra riesgo cibernético en gobernanza |
| GV.RR-01: Liderazgo responsable | EDM01 | Responsabilidad ejecutiva en ciberseguridad |
| GV.OV-01: Resultados de estrategia revisados | MEA01 (Monitoreo del desempeño) | Revisión y ajuste de estrategia de seguridad |
| ID.RA-03: Amenazas internas y externas identificadas | APO12 (Gestión de riesgos) | Proceso formal de identificación de amenazas |
| GV.SC-03: Riesgo en cadena de suministro integrado | APO10 (Gestión de proveedores) | Gestión formal de proveedores de TI |

**Ejemplo práctico en Colombia — Organización Gubernamental:**

> El **Departamento Administrativo de la Función Pública (DAFP)** integra COBIT 2019 con el MIPG para asegurar que la ciberseguridad sea un tema de gobernanza en todas las entidades públicas de Colombia. A través del objetivo EDM03, los comités directivos de entidades como el INVIMA o el IGAC incluyen el riesgo cibernético en sus matrices de riesgos institucionales (alineando GV.RM-01 del CSF 2.0), facilitando la rendición de cuentas ante la Contraloría y asegurando que los recursos presupuestales para ciberseguridad sean justificados a nivel estratégico.

---

## 9. ISA/IEC 62443

### Referencia: ISA/IEC 62443 — Industrial Automation and Control Systems Security

**Contexto e importancia:**

**¿Qué es este marco/norma?**  
ISA/IEC 62443 es una serie de normas internacionales desarrolladas por la International Society of Automation (ISA) y adoptadas por IEC, que abordan la ciberseguridad en Sistemas de Automatización y Control Industrial (IACS). La serie cubre desde la política organizacional hasta los requisitos técnicos a nivel de componente para entornos OT (Operational Technology).

**¿Por qué es relevante en ciberseguridad y ciberdefensa?**  
Colombia posee infraestructuras críticas con componentes OT: plantas de generación eléctrica (EPM, ISAGEN), oleoductos (Ecopetrol, OCP), acueductos (EAAB), plantas de tratamiento y sistemas de control de tráfico aéreo (Aerocivil). Un ataque a estos sistemas OT puede causar daños físicos, víctimas humanas e impacto estratégico equivalente a un acto de guerra. ISA/IEC 62443 es el estándar específico para proteger estos entornos.

**¿Cuál es su alcance principal?**  
Operadores de infraestructuras críticas, integradores de sistemas de automatización y fabricantes de componentes industriales (PLCs, HMI, SCADA).

**Aplicabilidad en el CSF 2.0:**

| Subcategoría CSF 2.0 | Requisito ISA/IEC 62443 | Cómo ayuda |
|----------------------|------------------------|------------|
| ID.AM-01: Inventario de hardware | IEC 62443-2-1 (Sec. 4.2.3) | Inventario de activos OT/ICS |
| PR.IR-01: Redes protegidas de acceso no autorizado | IEC 62443-3-3 (SR 5.1) | Segmentación de zonas OT |
| PR.AA-03: Usuarios y servicios autenticados | IEC 62443-2-1 / SR 1.1 | Autenticación en sistemas SCADA |
| DE.CM-01: Redes monitoreadas | IEC 62443-2-1 (Sec. 4.3) | Monitoreo de redes industriales |
| ID.RA-01: Vulnerabilidades identificadas | IEC 62443-2-1 (Sec. 4.2.3) | Gestión de vulnerabilidades OT |
| GV.SC-07: Riesgos de proveedores comprendidos | IEC 62443-2-4 | Requisitos para integradores de sistemas |
| RS.MI-01: Incidentes contenidos | IEC 62443-2-1 (Sec. 4.3.6) | Respuesta a incidentes en entornos ICS |

**Ejemplo práctico en Colombia — Infraestructura Crítica:**

> **XM S.A. E.S.P.** (operador del Sistema de Interconexión Eléctrica Nacional de Colombia) implementa ISA/IEC 62443 para proteger los sistemas de control del despacho de energía eléctrica a nivel nacional. Aplicando IEC 62443-3-3, segmenta la red OT en zonas de seguridad: la zona de despacho (máxima criticidad) está aislada de las redes corporativas mediante firewalls industriales (alineando PR.IR-01 del CSF 2.0). Un ataque exitoso a XM podría dejar sin electricidad a millones de colombianos, impactando hospitales, bases militares y comunicaciones estratégicas — convirtiendo su protección en un asunto de ciberdefensa nacional.

---

## 10. NIST SP 800-37 (RMF)

### Referencia: NIST SP 800-37 Rev. 2 — Risk Management Framework for Information Systems and Organizations

**Contexto e importancia:**

**¿Qué es este marco/norma?**  
El Risk Management Framework (RMF) del NIST, documentado en SP 800-37 Rev. 2, proporciona un proceso estructurado de 7 pasos para gestionar el riesgo de seguridad y privacidad en sistemas de información: Preparar, Categorizar, Seleccionar, Implementar, Evaluar, Autorizar y Monitorear. Es el marco de autorización de sistemas del gobierno federal de EE.UU.

**¿Por qué es relevante en ciberseguridad y ciberdefensa?**  
El RMF proporciona un proceso formal para autorizar la operación de sistemas de información críticos, asegurando que los riesgos residuales sean aceptados explícitamente por un Funcionario Autorizante (AO). Este concepto de Autorización para Operar (ATO) es fundamental en contextos de defensa, donde los sistemas deben ser formalmente aprobados antes de manejar información clasificada.

**¿Cuál es su alcance principal?**  
Sistemas de información federales de EE.UU., pero adoptado como referencia por organizaciones de defensa y seguridad a nivel global.

**Aplicabilidad en el CSF 2.0:**

| Subcategoría CSF 2.0 | Paso RMF | Cómo ayuda |
|----------------------|---------|------------|
| GV.RM-01: Objetivos de gestión de riesgos | Paso 1: Preparar | Establece contexto y estrategia de riesgo |
| ID.AM-05: Activos priorizados | Paso 2: Categorizar | Categorización de impacto de sistemas |
| GV.PO-01: Política de gestión de riesgos | Paso 3: Seleccionar | Selección de controles basada en política |
| ID.RA-05: Riesgo inherente comprendido | Paso 4: Implementar / Paso 5: Evaluar | Evaluación de efectividad de controles |
| GV.OV-01: Resultados revisados | Paso 6: Autorizar | Decisión formal de aceptación de riesgo |
| DE.CM-01: Monitoreo continuo | Paso 7: Monitorear | Monitoreo continuo de controles y riesgos |

**Ejemplo práctico en Colombia — Organización Militar:**

> Las **Fuerzas Militares de Colombia** aplican el concepto de ATO (Authorization to Operate) del RMF para sus sistemas de comunicaciones clasificadas. Antes de poner en operación un nuevo sistema de inteligencia de señales (SIGINT), el sistema pasa por los 7 pasos del RMF: se categoriza según su nivel de clasificación (Reservado, Secreto, Ultra Secreto), se implementan los controles de SP 800-53 correspondientes, se evalúan mediante pruebas de penetración, y el Comandante autoriza formalmente su operación aceptando el riesgo residual. Esto alinea GV.RM-01, GV.OV-01 y DE.CM-01 del CSF 2.0 en un proceso formal y auditable.

---

## 11. NIST SP 800-39

### Referencia: NIST SP 800-39 — Managing Information Security Risk

**Contexto e importancia:**

**¿Qué es este marco/norma?**  
NIST SP 800-39 proporciona orientación para la gestión del riesgo de seguridad de la información a nivel organizacional, de misión/proceso de negocio y de sistema de información. Establece un proceso de gestión de riesgos en 4 componentes: Enmarcar, Evaluar, Responder y Monitorear el riesgo.

**¿Por qué es relevante en ciberseguridad y ciberdefensa?**  
Proporciona la visión estratégica de gestión de riesgos que complementa el RMF (SP 800-37) a nivel táctico. Para organizaciones de defensa, establece cómo gestionar el riesgo a través de los tres niveles: estratégico (jefatura), táctico (operaciones) y técnico (sistemas).

**Aplicabilidad en el CSF 2.0:**

| Subcategoría CSF 2.0 | Componente SP 800-39 | Cómo ayuda |
|----------------------|---------------------|------------|
| GV.RM-01: Objetivos de gestión de riesgos | Enmarcar el riesgo | Define estrategia y apetito de riesgo |
| GV.RM-02: Declaraciones de apetito de riesgo | Enmarcar el riesgo | Formaliza tolerancia al riesgo |
| ID.RA-04: Impactos y probabilidades identificados | Evaluar el riesgo | Metodología de evaluación de riesgos |
| ID.RA-06: Respuestas a riesgos elegidas | Responder al riesgo | Opciones: aceptar, transferir, mitigar, evitar |
| GV.OV-01: Estrategia revisada | Monitorear el riesgo | Revisión continua del perfil de riesgo |

**Ejemplo práctico en Colombia — Organización Gubernamental:**

> La **Agencia Nacional de Inteligencia (ANI)** de Colombia usa SP 800-39 para estructurar su gestión de riesgos en tres niveles: a nivel estratégico (Nivel 1), el Director define el apetito de riesgo para operaciones de inteligencia; a nivel de misión (Nivel 2), los jefes de área evalúan riesgos específicos de cada programa de inteligencia; a nivel de sistema (Nivel 3), los equipos técnicos aplican controles específicos. Esta jerarquía alinea GV.RM-02 y GV.OV-01 del CSF 2.0 en una estructura coherente desde la estrategia hasta la implementación técnica.

---

## 12. NIST SP 800-30

### Referencia: NIST SP 800-30 Rev. 1 — Guide for Conducting Risk Assessments

**Contexto e importancia:**

**¿Qué es este marco/norma?**  
NIST SP 800-30 Rev. 1 proporciona orientación para llevar a cabo evaluaciones de riesgo de seguridad de la información. Define un proceso de 4 pasos: Preparar la evaluación, Llevar a cabo la evaluación (identificar fuentes de amenaza, eventos de amenaza, vulnerabilidades, probabilidad e impacto), Comunicar los resultados y Mantener la evaluación.

**¿Por qué es relevante en ciberseguridad y ciberdefensa?**  
Una evaluación de riesgos rigurosa y metodológicamente sólida es el fundamento de cualquier programa de ciberseguridad. SP 800-30 proporciona tablas de referencia para clasificar fuentes de amenaza (naciones-estado, hacktivistas, ciberdelincuentes, insiders), eventos de amenaza y vulnerabilidades, adaptables al contexto específico de cada organización.

**Aplicabilidad en el CSF 2.0:**

| Subcategoría CSF 2.0 | Paso SP 800-30 | Cómo ayuda |
|----------------------|---------------|------------|
| ID.RA-01: Vulnerabilidades identificadas | Llevar a cabo la evaluación | Identificación sistemática de vulnerabilidades |
| ID.RA-02: Inteligencia de amenazas recibida | Preparar la evaluación | Fuentes de amenaza contextualizadas |
| ID.RA-03: Amenazas internas y externas identificadas | Llevar a cabo la evaluación | Taxonomía de fuentes de amenaza |
| ID.RA-04: Impactos y probabilidades identificados | Llevar a cabo la evaluación | Matrices de probabilidad e impacto |
| ID.RA-05: Riesgo inherente comprendido | Llevar a cabo la evaluación | Determinación del nivel de riesgo |
| GV.OV-01: Estrategia revisada | Mantener la evaluación | Actualización periódica del perfil de riesgo |

**Ejemplo práctico en Colombia — Organización Militar:**

> El **Departamento de Ciberoperaciones del Ejército Nacional** realiza evaluaciones de riesgo trimestrales usando SP 800-30 para sus sistemas de mando y control. Identifica como fuentes de amenaza prioritarias: grupos de APT (Advanced Persistent Threat) asociados a carteles del narcotráfico con capacidades cibernéticas, actores estatales con intereses en desestabilización regional, e insiders con acceso a sistemas clasificados. La probabilidad e impacto de cada escenario se cuantifica y documenta (ID.RA-04 del CSF 2.0), generando un perfil de riesgo que guía las decisiones de inversión en controles de ciberseguridad para el año fiscal siguiente.

---

## 13. NIST SP 800-161r1 (C-SCRM)

### Referencia: NIST SP 800-161 Rev. 1 — Cybersecurity Supply Chain Risk Management Practices

**Contexto e importancia:**

**¿Qué es este marco/norma?**  
NIST SP 800-161 Rev. 1 proporciona orientación para gestionar los riesgos de ciberseguridad en cadenas de suministro (C-SCRM). Aborda cómo identificar, evaluar, responder y monitorear los riesgos cibernéticos que emergen de los productos, sistemas, servicios y proveedores que forman la cadena de suministro de una organización.

**¿Por qué es relevante en ciberseguridad y ciberdefensa?**  
Los ataques a la cadena de suministro (supply chain attacks) como SolarWinds (2020) o el ataque a Kaseya (2021) han demostrado que los adversarios pueden comprometer a miles de organizaciones atacando a un solo proveedor. Para el sector defensa colombiano, la dependencia de equipamiento importado (hardware, software, sistemas de comunicaciones) hace crítica la gestión de riesgos en la cadena de suministro, especialmente ante la posibilidad de implantación de backdoors o vulnerabilidades deliberadas.

**¿Cuál es su alcance principal?**  
Organizaciones que dependen de proveedores, contratistas y terceros para bienes y servicios de TI, OT y sistemas de comunicación.

**Aplicabilidad en el CSF 2.0:**

| Subcategoría CSF 2.0 | Práctica C-SCRM | Cómo ayuda |
|----------------------|----------------|------------|
| GV.SC-01: Programa C-SCRM establecido | Nivel organizacional | Marco completo de gestión de riesgo en suministro |
| GV.SC-04: Proveedores conocidos y priorizados | Nivel de misión | Inventario y criticidad de proveedores |
| GV.SC-05: Requisitos de ciberseguridad en contratos | Nivel de sistema | Cláusulas contractuales de seguridad |
| GV.SC-07: Riesgos de proveedores comprendidos | Evaluación de riesgos | Due diligence de ciberseguridad |
| ID.RA-09: Autenticidad de hardware/software evaluada | Integridad de componentes | Verificación de autenticidad de componentes |
| ID.RA-10: Proveedores críticos evaluados | Evaluación de proveedores | Auditorías de seguridad a proveedores clave |
| GV.SC-08: Proveedores incluidos en respuesta a incidentes | Planificación de respuesta | Coordinación con proveedores en incidentes |

**Ejemplo práctico en Colombia — Organización Militar:**

> La **Industria Militar (INDUMIL)** y el **Ministerio de Defensa** aplican C-SCRM al adquirir sistemas de comunicaciones tácticas (radios cifradas, sistemas C4ISR). Antes de cada adquisición, el equipo de ciberseguridad realiza evaluaciones de autenticidad de hardware (ID.RA-09 del CSF 2.0): verifica que los componentes no contengan backdoors de hardware, evalúa la reputación del fabricante y exige certificaciones de seguridad. Esto previene que adversarios estatales introduzcan vulnerabilidades en equipos de comunicación military — un vector de ataque documentado en conflictos modernos como el uso de equipos Huawei con supuestas capacidades de espionaje.

---

## 14. NIST SP 800-82 (OT/ICS)

### Referencia: NIST SP 800-82 Rev. 3 — Guide to Operational Technology Security

**Contexto e importancia:**

**¿Qué es este marco/norma?**  
NIST SP 800-82 Rev. 3 es la guía de referencia para asegurar sistemas de Tecnología Operacional (OT), incluyendo Sistemas de Control Industrial (ICS), SCADA, Sistemas de Control Distribuido (DCS) y otros sistemas de control que interactúan con el mundo físico. La revisión 3 (2023) amplía la cobertura a IoT industrial y sistemas ciber-físicos.

**¿Por qué es relevante en ciberseguridad y ciberdefensa?**  
Colombia tiene infraestructura crítica OT en sectores estratégicos: energía (EPM, Celsia, Isagen), petróleo y gas (Ecopetrol), agua potable (acueductos municipales), transporte y telecomunicaciones. La convergencia IT/OT crea nuevas superficies de ataque donde un ciberataque puede causar daños físicos. SP 800-82 proporciona orientación específica que reconoce las restricciones únicas de los entornos OT (sistemas legacy, tiempo real, alta disponibilidad requerida).

**Aplicabilidad en el CSF 2.0:**

| Subcategoría CSF 2.0 | Sección SP 800-82 | Cómo ayuda |
|----------------------|------------------|------------|
| ID.AM-01: Inventario de hardware | Cap. 4: Descripción de sistemas OT | Inventario de activos industriales |
| PR.IR-01: Redes protegidas | Cap. 6.2: Arquitectura de red OT | Segmentación IT/OT, DMZ industrial |
| PR.AA-03: Autenticación | Cap. 6.1: Gestión de identidad OT | Autenticación en contextos OT |
| DE.CM-01: Redes monitoreadas | Cap. 6.3: Monitoreo OT | Detección de anomalías en redes industriales |
| ID.RA-01: Vulnerabilidades identificadas | Cap. 5: Amenazas y vulnerabilidades OT | Gestión de vulnerabilidades OT-específicas |
| PR.PS-03: Hardware mantenido | Cap. 6.4: Gestión de parches OT | Patching en entornos de producción continua |
| RS.MI-01: Incidentes contenidos | Cap. 6.8: Respuesta a incidentes OT | Plan de respuesta adaptado a OT |

**Ejemplo práctico en Colombia — Infraestructura Crítica:**

> **EPM (Empresas Públicas de Medellín)** opera el sistema hidroeléctrico más grande de Colombia (Hidroituango y otras plantas). Aplica SP 800-82 para separar la red de control de las turbinas (OT) de la red corporativa (IT) mediante una zona desmilitarizada (DMZ) industrial (alineando PR.IR-01 del CSF 2.0). El sistema SCADA de control de compuertas opera en una red aislada, con monitoreo de anomalías mediante sensores de tráfico OT que detectan comunicaciones no estándar en protocolos Modbus/DNP3 (DE.CM-01). Un ataque a este sistema podría afectar el suministro eléctrico de Antioquia y generar daños catastróficos a la represa, por lo que su protección es prioridad de seguridad nacional.

---

## 15. NIST SP 800-61r2 (Incident Response)

### Referencia: NIST SP 800-61 Rev. 2 — Computer Security Incident Handling Guide

**Contexto e importancia:**

**¿Qué es este marco/norma?**  
NIST SP 800-61 Rev. 2 proporciona orientación para el manejo efectivo de incidentes de seguridad informática. Define un ciclo de vida de respuesta a incidentes de 4 fases: Preparación; Detección y Análisis; Contención, Erradicación y Recuperación; y Actividades Post-Incidente.

**¿Por qué es relevante en ciberseguridad y ciberdefensa?**  
La capacidad de respuesta a incidentes es el componente más crítico de la ciberdefensa operacional. Para Colombia, el ColCERT (Equipo de Respuesta a Emergencias Cibernéticas de Colombia) y el csirt-ccoc del CCOCI basan sus procedimientos en este marco. Un tiempo de respuesta rápido puede limitar el daño de un ciberataque a infraestructura crítica o sistemas gubernamentales.

**Aplicabilidad en el CSF 2.0:**

| Subcategoría CSF 2.0 | Fase SP 800-61 | Cómo ayuda |
|----------------------|---------------|------------|
| ID.IM-04: Planes de respuesta establecidos | Preparación | Plan de respuesta documentado y actualizado |
| DE.AE-08: Incidentes declarados | Detección y Análisis | Criterios formales de declaración de incidente |
| DE.AE-02: Eventos adversos analizados | Detección y Análisis | Análisis técnico de indicadores de compromiso |
| RS.MA-01: Plan de respuesta ejecutado | Contención, Erradicación, Recuperación | Ejecución coordinada del plan |
| RS.MI-01: Incidentes contenidos | Contención | Estrategias de contención (aislamiento de red) |
| RS.MI-02: Incidentes erradicados | Erradicación | Eliminación de malware y accesos no autorizados |
| RS.AN-03: Análisis de causa raíz | Actividades post-incidente | Lecciones aprendidas y mejora continua |
| RS.AN-06: Acciones de investigación registradas | Todas las fases | Cadena de custodia para evidencia digital |

**Ejemplo práctico en Colombia — Organización Gubernamental:**

> El **ColCERT** activa su procedimiento SP 800-61 cuando detecta un incidente de ransomware en una entidad del Estado. Fase 1 (Preparación): el ColCERT mantiene playbooks actualizados para diferentes tipos de incidentes, incluyendo ransomware, DDoS y APT. Fase 2 (Detección): el SIEM del ColCERT correlaciona alertas de múltiples entidades y declara el incidente (DE.AE-08 del CSF 2.0). Fase 3 (Contención): coordina el aislamiento de los sistemas afectados (RS.MI-01), preserva evidencia forense (RS.AN-07) y coordina con la Fiscalía General para la investigación penal. Fase 4 (Post-incidente): publica un informe de lecciones aprendidas para las demás entidades del Estado, mejorando la ciberresiliencia nacional.

---

## 16. NIST SP 800-137 (ISCM)

### Referencia: NIST SP 800-137 — Information Security Continuous Monitoring (ISCM)

**Contexto e importancia:**

**¿Qué es este marco/norma?**  
NIST SP 800-137 proporciona orientación para establecer, implementar y mantener un programa de Monitoreo Continuo de Seguridad de la Información (ISCM). El monitoreo continuo permite a las organizaciones mantener conciencia situacional sobre su postura de seguridad y tomar decisiones de riesgo informadas en tiempo real.

**¿Por qué es relevante en ciberseguridad y ciberdefensa?**  
En el contexto de ciberdefensa, la conciencia situacional continua (Cyber Situational Awareness) es equivalente al concepto militar de "Common Operating Picture" (COP). SP 800-137 proporciona el marco para que organizaciones como el ColCERT o el CCOCI mantengan visibilidad constante sobre el estado de seguridad de los sistemas críticos nacionales.

**Aplicabilidad en el CSF 2.0:**

| Subcategoría CSF 2.0 | Componente ISCM | Cómo ayuda |
|----------------------|----------------|------------|
| DE.CM-01: Redes monitoreadas | Monitoreo de red | IDS/IPS, análisis de tráfico continuo |
| DE.CM-03: Actividad de personal monitoreada | Monitoreo de usuarios | UEBA (User and Entity Behavior Analytics) |
| DE.CM-09: Hardware y software monitoreados | Monitoreo de endpoints | EDR, inventario dinámico de activos |
| GV.OV-01: Resultados de estrategia revisados | Métricas e indicadores | KPIs de seguridad para alta dirección |
| ID.RA-07: Cambios y excepciones gestionados | Gestión de cambios | Monitoreo de cambios no autorizados |
| DE.AE-03: Información correlacionada de múltiples fuentes | Correlación de eventos | SIEM con feeds de inteligencia de amenazas |

**Ejemplo práctico en Colombia — Organización Gubernamental:**

> La **Presidencia de la República de Colombia** implementa ISCM bajo SP 800-137 para todos sus sistemas de información estratégicos. Un panel de control de seguridad (Security Dashboard) muestra en tiempo real: número de vulnerabilidades abiertas por criticidad, alertas de seguridad activas, estado de parches de todos los sistemas, y métricas de cumplimiento (DE.CM-01, DE.CM-09 del CSF 2.0). Esta información alimenta los informes mensuales de postura de seguridad para el Consejo de Seguridad Nacional, alineando GV.OV-01 del CSF 2.0 con la toma de decisiones ejecutivas.

---

## 17. NIST SP 800-218 (SSDF)

### Referencia: NIST SP 800-218 — Secure Software Development Framework (SSDF) v1.1

**Contexto e importancia:**

**¿Qué es este marco/norma?**  
El Secure Software Development Framework (SSDF) de NIST, documentado en SP 800-218, es un conjunto de prácticas fundamentales para el desarrollo seguro de software. Organiza las prácticas en 4 grupos: Preparar la Organización (PO), Proteger el Software (PS), Producir Software Bien Asegurado (PW) y Responder a Vulnerabilidades (RV).

**¿Por qué es relevante en ciberseguridad y ciberdefensa?**  
El software desarrollado inseguramente es una de las principales causas de vulnerabilidades en sistemas críticos. Para Colombia, es especialmente relevante para el software desarrollado por entidades como la DIAN (sistemas tributarios), el MinTIC (sistemas de e-gobierno) y el sector defensa (aplicaciones de mando y control). El SSDF reduce la introducción de vulnerabilidades desde la fase de desarrollo.

**Aplicabilidad en el CSF 2.0:**

| Subcategoría CSF 2.0 | Práctica SSDF | Cómo ayuda |
|----------------------|--------------|------------|
| PR.PS-06: Prácticas de desarrollo seguro integradas | PW (Producir Software Bien Asegurado) | DevSecOps y revisión de código |
| ID.RA-01: Vulnerabilidades identificadas | RV (Responder a Vulnerabilidades) | Proceso de divulgación responsable |
| ID.RA-08: Procesos de respuesta a divulgaciones | RV.1 / RV.2 | Gestión de vulnerabilidades divulgadas |
| GV.SC-05: Requisitos de seguridad en cadena de suministro | PO.1 / PS.3 | Requisitos de seguridad en contratos de software |
| ID.RA-09: Autenticidad de software evaluada | PS.2 (Proteger el código) | Firma de código y verificación de integridad |

**Ejemplo práctico en Colombia — Organización Gubernamental:**

> El **Centro de Desarrollo Tecnológico del Ejército (CDE)** desarrolla aplicaciones para gestión logística y comunicaciones internas. Implementando el SSDF, integra controles de seguridad en todo el ciclo de desarrollo: análisis estático de código (SAST) en cada commit, pruebas de penetración antes de cada release, y firma digital de ejecutables para verificar integridad (ID.RA-09 del CSF 2.0). Esto previene que vulnerabilidades de software sean explotadas para comprometer sistemas de logística militar sensibles, como inventarios de armamento o rutas de abastecimiento.

---

## 18. NIST SP 800-160 Vol. 1

### Referencia: NIST SP 800-160 Vol. 1 — Engineering Trustworthy Secure Systems

**Contexto e importancia:**

**¿Qué es este marco/norma?**  
NIST SP 800-160 Volumen 1 proporciona orientación para la ingeniería de sistemas seguros y confiables (Systems Security Engineering - SSE). Integra consideraciones de seguridad, resiliencia, fiabilidad y privacidad en el proceso de ingeniería de sistemas desde las fases más tempranas del ciclo de vida.

**¿Por qué es relevante en ciberseguridad y ciberdefensa?**  
Para sistemas de defensa, la confiabilidad (trustworthiness) del sistema es fundamental: un sistema de armas, comunicaciones o mando y control debe ser correcto, seguro y fiable incluso bajo condiciones adversas. SP 800-160 proporciona el marco de ingeniería para construir estos atributos desde el diseño, no como un añadido posterior.

**Aplicabilidad en el CSF 2.0:**

| Subcategoría CSF 2.0 | Proceso SSE relacionado | Cómo ayuda |
|----------------------|------------------------|------------|
| ID.AM-08: Activos gestionados en su ciclo de vida | Gestión del ciclo de vida del sistema | Seguridad integrada en todo el ciclo de vida |
| PR.PS-06: Desarrollo seguro integrado | Diseño y desarrollo seguro | Principios de seguridad por diseño |
| GV.SC-07: Riesgos de proveedores comprendidos | Cadena de suministro en SSE | Evaluación de seguridad de componentes |
| PR.IR-03: Mecanismos de resiliencia implementados | Ingeniería de resiliencia | Redundancia y tolerancia a fallos |

**Ejemplo práctico en Colombia — Organización Militar:**

> El **programa de fragatas ARC de la Armada Nacional** incorpora SP 800-160 en el proceso de adquisición de nuevas unidades navales. Los requisitos de seguridad cibernética se especifican desde la fase de diseño conceptual: los sistemas de combate, propulsión y comunicaciones de la fragata se diseñan con arquitecturas de seguridad que garantizan disponibilidad operacional incluso si un subsistema es comprometido (PR.IR-03 del CSF 2.0). Esto evita el escenario de un ciberataque que deje una unidad naval sin capacidad de maniobra en zona de operaciones.

---

## 19. NIST AI RMF 1.0

### Referencia: NIST AI RMF 1.0 — Artificial Intelligence Risk Management Framework

**Contexto e importancia:**

**¿Qué es este marco/norma?**  
El NIST AI Risk Management Framework (AI RMF) 1.0, publicado en enero de 2023, es un marco voluntario para gestionar los riesgos de los sistemas de inteligencia artificial a lo largo de su ciclo de vida. Organiza las acciones en 4 funciones: GOVERN, MAP, MEASURE y MANAGE. Aborda riesgos de IA como sesgos, opacidad, robustez, privacidad y seguridad.

**¿Por qué es relevante en ciberseguridad y ciberdefensa?**  
La IA se está integrando en sistemas de ciberdefensa (detección de anomalías, análisis de malware, reconocimiento de patrones en inteligencia) y en sistemas de armas (sistemas autónomos, drones). El AI RMF proporciona un marco para gestionar los riesgos únicos que la IA introduce: ¿puede el modelo ser engañado (adversarial attacks)? ¿Es el modelo fiable para decisiones de defensa? ¿Qué sesgos tiene?

**Aplicabilidad en el CSF 2.0:**

| Subcategoría CSF 2.0 | Función AI RMF | Cómo ayuda |
|----------------------|---------------|------------|
| GV.RM-01: Objetivos de gestión de riesgos | GOVERN | Gobernanza de riesgos de IA |
| ID.RA-04: Impactos y probabilidades identificados | MAP | Mapeo de riesgos específicos de IA |
| ID.RA-01: Vulnerabilidades identificadas | MEASURE | Evaluación de robustez y fiabilidad de modelos IA |
| GV.OV-01: Resultados revisados | MANAGE | Gestión continua del ciclo de vida de IA |
| DE.CM-09: Hardware y software monitoreados | MEASURE / MANAGE | Monitoreo de comportamiento de modelos IA en producción |

**Ejemplo práctico en Colombia — Organización Militar/Gubernamental:**

> El **ColCERT** implementa un sistema de IA para detección de amenazas cibernéticas en tiempo real sobre el tráfico de redes gubernamentales. Aplicando el AI RMF, el equipo evalúa: ¿puede el modelo ser engañado mediante adversarial examples que camuflen malware? ¿Tiene sesgos que lleven a ignorar ciertos vectores de ataque? ¿Qué tan transparente es el proceso de decisión? Estas preguntas, mapeadas a ID.RA-01 y GV.RM-01 del CSF 2.0, garantizan que el sistema de IA sea una herramienta de ciberdefensa confiable y no introduzca nuevos riesgos operacionales.

---

## 20. SOC 2 (AICPA TSC)

### Referencia: SOC 2 — Service Organization Control 2 (Trust Services Criteria)

**Contexto e importancia:**

**¿Qué es este marco/norma?**  
SOC 2 es un marco de auditoría desarrollado por el American Institute of CPAs (AICPA) para evaluar los controles de seguridad de proveedores de servicios basados en 5 Trust Service Criteria (TSC): Seguridad, Disponibilidad, Integridad del procesamiento, Confidencialidad y Privacidad. Los reportes SOC 2 Tipo I y Tipo II proporcionan evidencia auditada de los controles de un proveedor de servicios.

**¿Por qué es relevante en ciberseguridad y ciberdefensa?**  
Las organizaciones gubernamentales y militares colombianas contratan crecientemente proveedores de servicios cloud, SaaS y managed services. Exigir certificación SOC 2 Tipo II a los proveedores garantiza que sus controles de seguridad han sido auditados independientemente, reduciendo el riesgo en la cadena de suministro de servicios tecnológicos.

**Aplicabilidad en el CSF 2.0:**

| Subcategoría CSF 2.0 | Criterio SOC 2 TSC | Cómo ayuda |
|----------------------|--------------------|------------|
| GV.SC-07: Riesgos de proveedores comprendidos | Seguridad (CC6, CC7) | Evidencia auditada de controles del proveedor |
| GV.SC-05: Requisitos en contratos | Todos los TSC | Base para cláusulas contractuales |
| PR.DS-01: Datos en reposo protegidos | Confidencialidad (C1) | Cifrado verificado por auditor independiente |
| DE.CM-01: Redes monitoreadas | Seguridad (CC7.2) | Monitoreo del proveedor verificado |
| PR.IR-04: Capacidad de disponibilidad mantenida | Disponibilidad (A1) | SLAs de disponibilidad verificados |
| ID.RA-10: Proveedores críticos evaluados | Todos los TSC | Due diligence con evidencia auditada |

**Ejemplo práctico en Colombia — Organización Gubernamental:**

> El **Ministerio de Tecnologías de la Información y las Comunicaciones (MinTIC)** exige certificación SOC 2 Tipo II a todos los proveedores de servicios en la nube que almacenen datos de ciudadanos colombianos en el marco de la Política de Gobierno Digital. Cuando el proveedor del sistema de historia clínica electrónica del SGSSS contrata con una firma de cloud computing, el MinTIC revisa el reporte SOC 2 Tipo II para verificar que los controles de confidencialidad (datos de salud) y disponibilidad (acceso 24/7 para urgencias) han sido auditados independientemente, alineando GV.SC-07 e ID.RA-10 del CSF 2.0 con evidencia objetiva de cumplimiento.

---

## Resumen General: Mapa de Referencias por Función del CSF 2.0

| Marco/Norma | GOVERN (GV) | IDENTIFY (ID) | PROTECT (PR) | DETECT (DE) | RESPOND (RS) | RECOVER (RC) |
|-------------|:-----------:|:-------------:|:------------:|:-----------:|:------------:|:------------:|
| CCMv4.0 | ✓ | | ✓ | ✓ | | |
| ISO/IEC 27001:2022 | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| NICE Framework | ✓ | ✓ | ✓ | ✓ | ✓ | |
| PCI DSS v4.0 | | ✓ | ✓ | ✓ | | |
| NIST SP 800-53 Rev.5 | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| SCF | ✓ | ✓ | ✓ | ✓ | | |
| CIS Controls v8 | | ✓ | ✓ | ✓ | ✓ | ✓ |
| COBIT 2019 | ✓ | ✓ | | ✓ | | |
| ISA/IEC 62443 | | ✓ | ✓ | ✓ | ✓ | |
| NIST SP 800-37 (RMF) | ✓ | ✓ | | ✓ | | |
| NIST SP 800-39 | ✓ | ✓ | | | | |
| NIST SP 800-30 | | ✓ | | | | |
| NIST SP 800-161r1 | ✓ | ✓ | | | | |
| NIST SP 800-82 | | ✓ | ✓ | ✓ | ✓ | |
| NIST SP 800-61r2 | | ✓ | | ✓ | ✓ | ✓ |
| NIST SP 800-137 | ✓ | ✓ | | ✓ | | |
| NIST SP 800-218 (SSDF) | | ✓ | ✓ | | | |
| NIST SP 800-160 | | ✓ | ✓ | | | |
| NIST AI RMF 1.0 | ✓ | ✓ | | ✓ | | |
| SOC 2 (AICPA TSC) | ✓ | ✓ | ✓ | ✓ | | ✓ |

---

## Contexto Normativo Nacional — Colombia

Para organizaciones colombianas, estas referencias internacionales deben articularse con el marco normativo nacional:

| Marco Nacional | Relación con CSF 2.0 | Marco Internacional Afín |
|----------------|---------------------|--------------------------|
| **CONPES 3995** — Política Nacional de Confianza y Seguridad Digital | Base estratégica de ciberseguridad nacional | CSF 2.0 completo |
| **Decreto 1078/2015 (MinTIC)** — Marco normativo TIC | Gobernanza TI en entidades públicas | COBIT 2019 / NIST SP 800-37 |
| **MSPI** — Modelo de Seguridad y Privacidad de la Información (MinTIC) | Sistema de gestión de seguridad de la información | ISO/IEC 27001:2022 |
| **Ley 1581/2012** — Protección de datos personales | Privacidad de datos de ciudadanos | ISO/IEC 27001:2022 / SOC 2 |
| **Decreto 2573/2014** — Estrategia de Gobierno en Línea | Transformación digital segura | CCMv4.0 / NIST CSF 2.0 |
| **Directiva Ministerial 003/2016** — Ciberdefensa | Protección de sistemas de defensa nacional | NIST SP 800-53 / ISA 62443 |

---

*Documento generado con base en: Archivo `csf2.xlsx`, Hoja `CSF 2.0` — NIST Cybersecurity Framework 2.0.*  
*Referencias normativas documentadas conforme a los marcos citados en el CSF 2.0 Informative References.*  
*Contexto de aplicabilidad adaptado para organizaciones militares, gubernamentales e infraestructura crítica de Colombia.*
