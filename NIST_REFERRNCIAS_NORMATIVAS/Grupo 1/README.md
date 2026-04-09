# Referencias Normativas — NIST CSF 2.0

Este documento describe cada marco normativo referenciado en el NIST Cybersecurity Framework 2.0. Se documentan 17 marcos, con sus controles representativos, relevancia en ciberdefensa y ejemplos de aplicación práctica.

---

## Índice de Marcos

| # | Marco | Apariciones en CSF 2.0 |
|---|-------|------------------------|
| 1 | [CCMv4.0](#1-ccmv40--cloud-controls-matrix-v40) | 657 |
| 2 | [CIS Controls v8.0 / v8.1](#2-cis-controls-v80--v81) | 122 |
| 3 | [CRI Profile v2.0](#3-cri-profile-v20) | 405 |
| 4 | [CSF v1.1](#4-csf-v11--nist-cybersecurity-framework-v11) | 156 |
| 5 | [CoP](#5-cop--code-of-practice) | 61 |
| 6 | [IRP](#6-irp--incident-response-plan-framework) | 45 |
| 7 | [ISO/IEC 27001:2022](#7-isoiec-270012022) | 395 |
| 8 | [NICE Framework](#8-nice-framework) | 647 |
| 9 | [PCI DSS](#9-pci-dss--payment-card-industry-data-security-standard) | 552 |
| 10 | [SCF](#10-scf--secure-controls-framework) | 363 |
| 11 | [SP 800-171 Rev 3](#11-sp-800-171-rev-3) | 310 |
| 12 | [SP 800-221A](#12-sp-800-221a) | 74 |
| 13 | [SP 800-53 Rev 5.1.1](#13-sp-800-53-rev-511) | 734 |
| 14 | [SP 800-53 Rev 5.2.0](#14-sp-800-53-rev-520) | 740 |
| 15 | [SP-800-37 Rev 2](#15-sp-800-37-rev-2--risk-management-framework) | 166 |
| 16 | [SSDF](#16-ssdf--secure-software-development-framework) | 33 |
| 17 | [SP 800-221A (ERM)](#12-sp-800-221a) | 74 |

---

## 1. CCMv4.0 — Cloud Controls Matrix v4.0

### Contexto e importancia

**¿Qué es?** El Cloud Controls Matrix (CCM) es un marco de controles de seguridad desarrollado por la Cloud Security Alliance (CSA), específicamente diseñado para entornos de computación en la nube.

**¿Por qué es relevante?** La nube se ha convertido en infraestructura crítica para gobiernos, fuerzas armadas y empresas. El CCM proporciona un lenguaje común para evaluar el riesgo compartido entre proveedor y cliente (modelo de responsabilidad compartida). Es la analogía de un contrato de arrendamiento: el arrendatario (organización) y el arrendador (proveedor cloud) tienen obligaciones distintas pero complementarias.

**Alcance principal:** 197 controles agrupados en 17 dominios: desde continuidad de negocio (BCR) hasta gestión de vulnerabilidades (TVM), identidades (IAM), criptografía (CEK) y gestión de cadena de suministro (STA).

### Aplicabilidad en el CSF 2.0

Aparece en prácticamente todas las subcategorías del CSF 2.0 (657 referencias). Dominios más frecuentes:

| Dominio CCM | Código | Subcategorías CSF 2.0 |
|-------------|--------|----------------------|
| Business Continuity | BCR-01 a BCR-11 | GV.OC-01, GV.OC-04 |
| Audit & Assurance | A&A-01 a A&A-06 | ID.IM, GV.OV |
| Identity & Access Mgmt | IAM-01 a IAM-16 | PR.AA-01 a PR.AA-06 |
| Cryptography & Key Mgmt | CEK-01 a CEK-21 | PR.DS-01, GV.OC-03 |
| Threat & Vulnerability | TVM-01 a TVM-10 | ID.RA, DE.CM |
| Logging & Monitoring | LOG-01 a LOG-13 | DE.AE, DE.CM |
| Supply Chain Mgmt | STA-01 a STA-14 | GV.SC |
| Security Incident | SEF-01 a SEF-08 | RS.MA, RS.AN |
| Unified Endpoint Mgmt | UEM-01 a UEM-14 | PR.PS, ID.AM |

**Ejemplo de mapeo:**
- `CCMv4.0: BCR-01` → `GV.OC-01` (La misión organizacional informa la gestión de riesgos de ciberseguridad)
- `CCMv4.0: IAM-05` → `PR.AA-03` (Identidades gestionadas y autenticadas)
- `CCMv4.0: LOG-07` → `DE.CM-03` (Actividades del personal monitoreadas)

### Ejemplo práctico en ciberdefensa

**Situación:** Una agencia gubernamental migra su sistema de gestión de inteligencia a una nube gubernamental privada (GovCloud).

**Aplicación:** Usando CCMv4.0 como referencia normativa:
- **CEK-01 a CEK-21**: Define qué algoritmos criptográficos se usan para clasificar información (p.ej., AES-256 para datos TOP SECRET).
- **IAM-14 / IAM-15**: Implementa autenticación multifactor (MFA) obligatoria + gestión de privilegios mínimos para analistas.
- **LOG-04 / LOG-07**: Centraliza logs de acceso en un SIEM con retención de 2 años para cumplir regulaciones de auditoría.
- **BCR-09**: Documenta el RTO (Recovery Time Objective) para sistemas críticos de inteligencia: máximo 4 horas.

---

## 2. CIS Controls v8.0 / v8.1

### Contexto e importancia

**¿Qué es?** Los CIS Controls (Center for Internet Security) son un conjunto priorizado de 18 controles de seguridad desarrollados por consenso de expertos globales, con énfasis en defensa práctica e implementable.

**¿Por qué es relevante?** Funciona como una "lista de verificación de mecánico": controles concretos, medibles y ordenados por impacto. A diferencia de ISO 27001 (basado en gestión), CIS se enfoca en *técnicas defensivas específicas*. La versión 8.1 introduce mejoras en cobertura de seguridad en la nube.

**Alcance principal:** 18 controles (CIS Controls 1-18) agrupados en 3 grupos de implementación (IG1 básico, IG2 intermedio, IG3 avanzado). Cubre inventario de activos, configuración segura, protección de datos, gestión de accesos, respuesta a incidentes, entre otros.

### Aplicabilidad en el CSF 2.0

Aparece en 122 referencias (60 para v8.0 + 62 para v8.1). Los controles más citados:

| Control CIS | Descripción | Subcategoría CSF 2.0 |
|-------------|-------------|----------------------|
| 1.1 / 1.2 | Inventario de activos de hardware | ID.AM-01, ID.AM-02 |
| 2.1 / 2.2 | Inventario de software autorizado | ID.AM-02, PR.PS-01 |
| 3.2 / 3.3 | Protección de datos y clasificación | PR.DS-01 |
| 5.1 | Gestión de cuentas | PR.AA-01 |
| 6.1 / 6.2 | Control de acceso | PR.AA-05 |
| 7.1 / 7.2 | Gestión de vulnerabilidades | ID.RA-01 |
| 17.x | Gestión de respuesta a incidentes | RS.MA |

**v8.1 agrega:** Control `5.6` (gestión de cuentas de aplicaciones) que aparece en subcategorías de acceso privilegiado.

### Ejemplo práctico en ciberdefensa

**Situación:** Un ministerio de defensa necesita establecer una línea base de seguridad mínima en 500 estaciones de trabajo operacionales.

**Aplicación:**
- **CIS Control 1 (Inventario de activos)**: Despliega agente de inventario en todas las estaciones; ningún dispositivo no inventariado puede conectarse a la red (principio de lista blanca de dispositivos).
- **CIS Control 4 (Configuración segura)**: Aplica hardening basado en CIS Benchmarks para Windows 11 DoD STIG antes de desplegar cada equipo.
- **CIS Control 17 (Gestión de incidentes)**: Establece un equipo de respuesta con roles definidos, guión de escalamiento y ejercicios tabletop trimestrales.

El enfoque IG1 (controles básicos 1-6) garantiza protección mínima; IG3 (todos los controles) aplica a sistemas de comando y control.

---

## 3. CRI Profile v2.0

### Contexto e importancia

**¿Qué es?** El Cyber Risk Institute (CRI) Profile es un marco derivado del CSF 1.1, diseñado específicamente para el sector financiero. La v2.0 se actualiza para alinearse con CSF 2.0.

**¿Por qué es relevante?** El sector financiero es infraestructura crítica nacional. El CRI Profile traduce los requisitos de reguladores financieros (Fed, OCC, FDIC en EE.UU.) al lenguaje del CSF, facilitando auditorías de cumplimiento regulatorio en bancos, aseguradoras y mercados de capitales.

**Alcance principal:** Extiende las 6 funciones del CSF 2.0 con sub-declaraciones adicionales de diagnóstico (declaraciones de práctica numeradas), cuantificando el nivel de madurez (1-4) por control.

### Aplicabilidad en el CSF 2.0

Con 405 referencias, cubre todas las funciones CSF 2.0:

| Función CSF | Prefijo CRI Profile | Ejemplo de control |
|-------------|--------------------|--------------------|
| GOVERN | GV.OC, GV.RM, GV.RR, GV.PO, GV.OV, GV.SC | GV.OC-01.01 |
| IDENTIFY | ID.AM, ID.RA, ID.IM | ID.RA-01.01 |
| PROTECT | PR.AA, PR.AT, PR.DS, PR.PS, PR.IR | PR.AA-03.01 |
| DETECT | DE.CM, DE.AE | DE.CM-01.01 |
| RESPOND | RS.MA, RS.AN, RS.CO, RS.MI | RS.MA-01.01 |
| RECOVER | RC.RP, RC.CO | RC.RP-02.01 |

**Ejemplo:** `CRI Profile v2.0: DE.CM-01.01` → `DE.CM-01` (Redes y entornos de red monitoreados para detectar eventos potencialmente adversos).

### Ejemplo práctico en ciberdefensa

**Situación:** Un banco central (infraestructura crítica financiera nacional) debe demostrar resiliencia cibernética ante reguladores.

**Aplicación:**
- `GV.RM-03.01 / GV.RM-03.02`: Define apetito de riesgo cuantitativo (p.ej., pérdida máxima tolerable por ciberincidente: USD 50M) aprobado por la junta directiva.
- `DE.CM-01.05 / DE.CM-01.06`: Monitoreo de transacciones en tiempo real buscando patrones de fraude mediante ML (detección de anomalías en transferencias SWIFT).
- `RS.AN-07.01`: Correlación de indicadores de compromiso (IoCs) con inteligencia de amenazas financieras del FS-ISAC.

---

## 4. CSF v1.1 — NIST Cybersecurity Framework v1.1

### Contexto e importancia

**¿Qué es?** La versión anterior del propio NIST CSF (2018), incluida como referencia de trazabilidad para organizaciones que ya implementaban la v1.1 y necesitan migrar a la v2.0.

**¿Por qué es relevante?** Permite mapeo de continuidad: organizaciones con programas maduros en CSF 1.1 pueden identificar qué subcategorías son nuevas en 2.0 (como la función GOVERN) y cuáles son equivalentes o renombradas. Es como un manual de migración entre versiones de sistema operativo.

**Alcance principal:** 5 funciones (IDENTIFY, PROTECT, DETECT, RESPOND, RECOVER), 23 categorías, 108 subcategorías. La v2.0 agrega GOVERN y expande a 106 subcategorías restructuradas.

### Aplicabilidad en el CSF 2.0

Con 156 referencias, actúa como ancla de trazabilidad. Ejemplos de correspondencia:

| CSF v1.1 | CSF v2.0 | Descripción |
|----------|----------|-------------|
| ID.BE-2 | GV.OC-01 | Misión organizacional |
| ID.GV-3 | GV.OC-03 | Requisitos legales y regulatorios |
| ID.RM-1 | GV.RM-01 | Objetivos de gestión de riesgos |
| PR.AC-1 | PR.AA-01 | Gestión de identidades |
| DE.CM-1 | DE.CM-01 | Monitoreo de redes |
| RS.RP-1 | RS.MA-01 | Activación del plan de respuesta |

### Ejemplo práctico en ciberdefensa

**Situación:** Una organización gubernamental certificada en CSF 1.1 debe actualizar su programa a CSF 2.0.

**Aplicación:** Usando la tabla de correspondencia, mapean sus controles existentes. La nueva función **GOVERN** (GV) no tiene equivalente directo en 1.1; se construye a partir de fragmentos de ID.GV, ID.BE y ID.RM. El equipo usa esta referencia para priorizar brechas de gobernanza sin reconstruir todo el programa desde cero.

---

## 5. CoP — Code of Practice

### Contexto e importancia

**¿Qué es?** Código de Práctica para Seguridad de la Información, típicamente referenciado como el UK Code of Practice o estándares sectoriales equivalentes que establecen buenas prácticas en protección de datos e información.

**¿Por qué es relevante?** Proporciona orientación prescriptiva sobre comportamientos aceptables en el tratamiento de información, complementando marcos de controles técnicos con expectativas de conducta organizacional. Similar a un "reglamento de tránsito" aplicado a la información.

**Alcance principal:** Organizado en dominios A-E que cubren: gestión de información (A), acceso y autenticación (B), protección de datos (C), respuesta a incidentes (D) y continuidad (E).

### Aplicabilidad en el CSF 2.0

61 referencias cubren subcategorías de gobernanza y protección. Controles representativos:

| Control CoP | Subcategoría CSF 2.0 | Descripción |
|-------------|----------------------|-------------|
| CoP: A1 | GV.OC-02 | Contexto organizacional y partes interesadas |
| CoP: A3 | GV.OC-01 | Misión organizacional |
| CoP: B2 | PR.AA-01 | Gestión de identidades |
| CoP: C1 | PR.DS-01 | Protección de datos en reposo |
| CoP: D1 | RS.MA-01 | Plan de respuesta a incidentes |
| CoP: E2 | RC.RP-02 | Recuperación y restauración |

### Ejemplo práctico en ciberdefensa

**Situación:** Una agencia gubernamental implementa un programa de protección de información clasificada para personal con acceso a sistemas de inteligencia.

**Aplicación:** El CoP define el comportamiento esperado del personal: `CoP: A2` establece que toda información clasificada debe etiquetarse; `CoP: B3` requiere que el acceso sea revocado dentro de 24 horas de la terminación del empleado. Estas prácticas se implementan como políticas de RRHH vinculadas a controles técnicos del sistema.

---

## 6. IRP — Incident Response Plan Framework

### Contexto e importancia

**¿Qué es?** Marco de planificación de respuesta a incidentes (IRP) que define la estructura, roles, procedimientos y criterios de activación para gestionar ciberincidentes. Puede referirse a estándares sectoriales específicos (p.ej., IRP financiero, IRP de infraestructura crítica).

**¿Por qué es relevante?** Un incidente sin plan de respuesta es como un incendio sin extintor: el daño se multiplica por la confusión. El IRP garantiza que la respuesta sea coordinada, documentada y mejore con cada incidente.

**Alcance principal:** 6 secciones (IRP-Sec-1 a IRP-Sec-6) que cubren: preparación, identificación, contención, erradicación, recuperación y lecciones aprendidas — el ciclo PICERL.

### Aplicabilidad en el CSF 2.0

45 referencias concentradas en las funciones RESPOND y RECOVER:

| Control IRP | Subcategoría CSF 2.0 | Descripción |
|-------------|----------------------|-------------|
| IRP-Sec-1 | GV.OC-01, RS.MA-01 | Preparación y activación del plan |
| IRP-Sec-2 | GV.RM-01, ID.RA | Identificación y clasificación del incidente |
| IRP-Sec-3 | RS.MA-03, RS.MI | Contención y mitigación |
| IRP-Sec-4 | RS.AN-06 | Análisis forense y erradicación |
| IRP-Sec-5 | RC.RP-03 | Recuperación de servicios |
| IRP-Sec-6 | ID.IM-02 | Lecciones aprendidas y mejora |

### Ejemplo práctico en ciberdefensa

**Situación:** Un equipo CSIRT gubernamental responde a un ataque de ransomware en sistemas de gestión de infraestructura eléctrica.

**Aplicación:**
- **IRP-Sec-1**: El CISO activa el plan (declaración de incidente P1) y convoca al equipo de crisis en 30 minutos.
- **IRP-Sec-2**: Se clasifica como incidente de infraestructura crítica; se notifica al CERT nacional en 4 horas (obligación regulatoria).
- **IRP-Sec-3**: Se aíslan los segmentos OT/ICS afectados para prevenir propagación al SCADA de la red eléctrica.
- **IRP-Sec-6**: Post-incidente: se actualiza el IRP con las brechas identificadas (p.ej., ausencia de segmentación OT/IT).

---

## 7. ISO/IEC 27001:2022

### Contexto e importancia

**¿Qué es?** Estándar internacional para Sistemas de Gestión de Seguridad de la Información (SGSI), publicado por ISO/IEC. La versión 2022 moderniza los controles del Anexo A, reduciendo de 114 a 93 controles y agregando 11 nuevos controles en temas como inteligencia de amenazas, seguridad en la nube y privacidad.

**¿Por qué es relevante?** ISO 27001 es el estándar de seguridad de la información más adoptado globalmente. La certificación demuestra a clientes, socios y reguladores que la organización tiene un SGSI formal y auditado. Es la analogía de un "sello de calidad ISO" pero para ciberseguridad.

**Alcance principal:** Dos niveles:
- **Cláusulas Mandatorias (4-10)**: Requisitos de gestión del SGSI (contexto, liderazgo, planificación, soporte, operación, evaluación, mejora).
- **Annexo A**: 93 controles técnicos y organizacionales en 4 dominios: Organizacional (5.x), Personas (6.x), Físico (7.x), Tecnológico (8.x).

### Aplicabilidad en el CSF 2.0

Con 395 referencias, ISO 27001 aparece en prácticamente toda la estructura del CSF 2.0:

**Cláusulas Mandatorias más citadas:**

| Cláusula ISO | Descripción | Subcategoría CSF 2.0 |
|-------------|-------------|----------------------|
| 4.1 | Contexto de la organización | GV.OC-01 |
| 4.2 | Partes interesadas | GV.OC-02 |
| 5.2 | Política de seguridad | GV.PO-01 |
| 6.1 | Acciones para riesgos y oportunidades | GV.RM-01, ID.RA |
| 6.1.2 | Evaluación de riesgos | ID.RA-03 |
| 8.1 | Planificación y control operacional | PR.PS |
| 9.1 | Seguimiento y medición | ID.IM-01 |
| 9.2 | Auditoría interna | GV.OV |
| 10.1 / 10.2 | Mejora continua | ID.IM-04 |

**Controles del Annexo A más citados:**

| Control ISO | Descripción | Subcategoría CSF 2.0 |
|------------|-------------|----------------------|
| 5.1 | Políticas de seguridad | GV.PO-01 |
| 5.15 | Control de acceso | PR.AA-01 |
| 5.19 | Seguridad en la cadena de suministro | GV.SC-01 |
| 5.24 | Gestión de incidentes | RS.MA |
| 8.5 | Autenticación segura | PR.AA-03 |
| 8.8 | Gestión de vulnerabilidades | ID.RA-01 |
| 8.15 | Logging | DE.AE-03 |
| 8.16 | Monitoreo | DE.CM-01 |
| 8.25 | Ciclo de vida de desarrollo seguro | PR.PS-06 |

### Ejemplo práctico en ciberdefensa

**Situación:** Una empresa de defensa (DEFENSE PRIME) que provee sistemas de armas debe demostrar cumplimiento de seguridad ante el Ministerio de Defensa (cliente).

**Aplicación:**
- **ISO 27001 Cláusula 4.2**: Identifica al Ministerio como parte interesada clave con requisitos de clasificación de información → se mapea a `GV.OC-02`.
- **ISO 27001 Annex A 5.19 / 5.20 / 5.21**: Gestión de seguridad en proveedores (subcontratistas de electrónica): acuerdos de seguridad, auditorías de la cadena de suministro → mapea a `GV.SC-01` a `GV.SC-09`.
- **ISO 27001 Annex A 8.15 + 8.16**: Implementa SIEM con retención de logs de 5 años para auditoría forense → mapea a `DE.AE-03` y `DE.CM-01`.
- La certificación ISO 27001 se usa como evidencia contractual en licitaciones de defensa.

---

## 8. NICE Framework

### Contexto e importancia

**¿Qué es?** El NICE Cybersecurity Workforce Framework (NIST SP 800-181) es un marco de referencia para la fuerza laboral en ciberseguridad, desarrollado por el National Initiative for Cybersecurity Education (NICE). Define roles de trabajo, tareas, conocimientos y habilidades.

**¿Por qué es relevante?** La ciberseguridad no solo es tecnología: son **personas**. NICE proporciona un lenguaje común para definir qué hace un "analista de seguridad", un "arquitecto de redes" o un "investigador forense digital". Piénsalo como una descripción de cargos militares (MOS) pero para el ámbito cibernético.

**Alcance principal:** Organizado en categorías de trabajo identificadas por prefijos:
- **OG** (Oversee and Govern): Roles de liderazgo y gobernanza en ciberseguridad (OG-WRL-001 a OG-WRL-016)
- **PD** (Protect and Defend): Roles de protección y defensa (PD-WRL-001 a PD-WRL-007)
- **DD** (Detect and Defend): Roles de detección (DD-WRL-001 a DD-WRL-009)
- **IO** (Investigate and Operate): Roles de investigación y operaciones (IO-WRL-001 a IO-WRL-007)

### Aplicabilidad en el CSF 2.0

Con 647 referencias, es el segundo marco más citado. Aparece en casi todas las subcategorías porque el CSF 2.0 reconoce que cada control requiere personal capacitado:

| Categoría NICE | Roles típicos | Subcategorías CSF 2.0 |
|----------------|---------------|----------------------|
| OG-WRL-001 a 016 | CISO, Risk Manager, Compliance Officer | GV.OC, GV.RM, GV.RR |
| PD-WRL-001 a 007 | Security Engineer, Network Defender | PR.AA, PR.DS, PR.PS |
| DD-WRL-001 a 009 | SOC Analyst, Threat Hunter | DE.CM, DE.AE |
| IO-WRL-001 a 007 | Incident Responder, Digital Forensics | RS.AN, RS.MA |

### Ejemplo práctico en ciberdefensa

**Situación:** Un Comando Cibernético Militar necesita estructurar su fuerza laboral de ciberdefensa.

**Aplicación:**
- **OG-WRL-005 (Cybersecurity Manager)**: Rol de Director del Centro de Operaciones de Seguridad (SOC), responsable de la postura de seguridad → mapea a `GV.RR-02`.
- **DD-WRL-003 (Cyber Defense Analyst)**: Analistas SOC que monitoran alertas del SIEM en tiempo real → mapea a `DE.CM-01` y `DE.AE-02`.
- **IO-WRL-004 (Cyber Defense Forensics Analyst)**: Investigadores forenses que analizan malware tras un incidente → mapea a `RS.AN-06`.
- El Marco NICE permite establecer la plantilla orgánica del Comando Cibernético con roles estandarizados, facilitando intercambio de personal con aliados de la OTAN.

---

## 9. PCI DSS — Payment Card Industry Data Security Standard

### Contexto e importancia

**¿Qué es?** Estándar de seguridad de datos para la industria de tarjetas de pago, desarrollado por el PCI Security Standards Council (fundado por Visa, Mastercard, American Express, Discover y JCB). La versión más reciente (v4.0) es la referenciada.

**¿Por qué es relevante?** Cualquier organización que procese, almacene o transmita datos de tarjetas de crédito debe cumplir PCI DSS. En términos de infraestructura crítica, los sistemas de pago son el sistema nervioso de la economía. Un compromiso masivo podría paralizar el comercio nacional.

**Alcance principal:** 12 requisitos organizados en 6 metas de control: construir y mantener redes seguras, proteger datos del titular de tarjeta, mantener un programa de gestión de vulnerabilidades, implementar medidas de control de acceso, monitorear y probar redes regularmente, y mantener una política de seguridad de la información.

### Aplicabilidad en el CSF 2.0

Con 552 referencias, PCI DSS aparece extensamente en las funciones de protección, detección y gobernanza:

| Requisito PCI DSS | Descripción | Subcategoría CSF 2.0 |
|-------------------|-------------|----------------------|
| 1.x | Instalar y mantener controles de red | PR.IR-01, DE.CM-01 |
| 2.x | Configuraciones seguras | PR.PS-01 |
| 3.x | Proteger datos del titular | PR.DS-01, PR.DS-02 |
| 4.x | Cifrado en transmisión | PR.DS-02 |
| 5.x | Protección contra malware | DE.CM-09 |
| 6.x | Desarrollo seguro de software | PR.PS-06 |
| 7.x | Control de acceso | PR.AA-05 |
| 8.x | Gestión de identidades | PR.AA-01, PR.AA-03 |
| 10.x | Logging y monitoreo | DE.AE-03, DE.CM-03 |
| 11.x | Pruebas de seguridad | ID.RA-01 |
| 12.x | Políticas y programa de seguridad | GV.PO-01 |

**Ejemplos específicos:**
- `PCI DSS: 10.3.3` → `DE.AE-07` (Logs protegidos contra modificación)
- `PCI DSS: 12.10.1` → `RS.MA-01` (Plan de respuesta a incidentes)
- `PCI DSS: 6.3.3` → `ID.RA-01` (Gestión de vulnerabilidades en software)

### Ejemplo práctico en ciberdefensa

**Situación:** Las fuerzas armadas operan un sistema de pago para beneficios del personal militar (nómina, viáticos, bonificaciones de combate).

**Aplicación:**
- **PCI DSS 3.4.1**: Cifrado de números de tarjeta almacenados con tokenización → `PR.DS-01`.
- **PCI DSS 8.3.6**: Contraseñas de al menos 12 caracteres con complejidad + MFA → `PR.AA-03`.
- **PCI DSS 11.3.1**: Pruebas de penetración al sistema de pago al menos anualmente → `ID.RA-01`.
- **PCI DSS 12.10.4**: Personal de respuesta a incidentes entrenado específicamente para brechas de datos de tarjetas → `RS.MA-04`.

---

## 10. SCF — Secure Controls Framework

### Contexto e importancia

**¿Qué es?** El Secure Controls Framework (SCF) es un metamarco de ciberseguridad y privacidad de código abierto que consolida y armoniza más de 100 marcos y regulaciones en un único catálogo de controles. Funciona como un "traductor universal" entre normas.

**¿Por qué es relevante?** Las organizaciones deben cumplir simultáneamente múltiples regulaciones (ISO 27001, NIST, PCI DSS, GDPR, etc.). El SCF mapea todos estos requisitos a controles únicos, evitando duplicar esfuerzos. Es como una navaja suiza normativa: un control SCF puede satisfacer requisitos de 5 marcos diferentes simultáneamente.

**Alcance principal:** Más de 1,000 controles organizados en dominios como: AST (Gestión de Activos), BCD (Continuidad), CFG (Gestión de Configuración), CRY (Criptografía), IAC (Control de Acceso), IRO (Respuesta a Incidentes), MON (Monitoreo), RSK (Gestión de Riesgos), entre otros.

### Aplicabilidad en el CSF 2.0

Con 363 referencias, SCF cubre todas las funciones del CSF 2.0. Dominios más frecuentes:

| Dominio SCF | Código | Subcategorías CSF 2.0 |
|-------------|--------|----------------------|
| Asset Management | AST-01 a AST-15 | ID.AM-01 a ID.AM-08 |
| Business Continuity | BCD-01 a BCD-13 | GV.OC-04, RC.RP |
| Configuration Mgmt | CFG-01 a CFG-05 | PR.PS-01, ID.AM |
| Cryptography | CRY-01 a CRY-05 | PR.DS-01, PR.DS-02 |
| Access Control | IAC-01 a IAC-28 | PR.AA-01 a PR.AA-06 |
| Incident Response | IRO-01 a IRO-16 | RS.MA, RS.AN, RS.MI |
| Monitoring | MON-01 a MON-16 | DE.CM, DE.AE |
| Risk Management | RSK-01 a RSK-09 | ID.RA, GV.RM |
| Threat Management | THR-01 a THR-07 | ID.RA-02, DE.AE |
| Third Party Mgmt | TPM-01 a TPM-11 | GV.SC |
| Vulnerability Mgmt | VPM-01 a VPM-06 | ID.RA-01 |

### Ejemplo práctico en ciberdefensa

**Situación:** Una organización de defensa multinacional (alianza tipo OTAN) necesita demostrar cumplimiento simultáneo con ISO 27001, NIST SP 800-53, y regulaciones nacionales de cada país miembro.

**Aplicación:** El SCF actúa como capa de armonización:
- `SCF: MON-01` satisface simultáneamente ISO 27001 A.8.16, SP 800-53 AU-12, y PCI DSS 10.2 → `DE.CM-01`.
- `SCF: IRO-04.2` cubre SP 800-53 IR-04, ISO 27001 A.5.24, y PCI DSS 12.10.5 → `RS.MA-03`.
- Un solo control SCF implementado elimina la necesidad de mapear individualmente cada regulación, reduciendo el costo de cumplimiento en un 40-60%.

---

## 11. SP 800-171 Rev 3

### Contexto e importancia

**¿Qué es?** NIST Special Publication 800-171 "Protecting Controlled Unclassified Information in Nonfederal Systems and Organizations". Define requisitos de seguridad para proteger CUI (Controlled Unclassified Information) en sistemas no gubernamentales.

**¿Por qué es relevante?** Los contratistas de defensa, universidades y empresas que trabajan con el gobierno de EE.UU. manejan información sensible no clasificada (planos de sistemas de armas, datos de personal, investigación). SP 800-171 es el requisito de facto para participar en contratos federales de defensa (DFARS 252.204-7012). La Rev 3 agrega controles de organizaciones que operan en entornos avanzados de amenazas.

**Alcance principal:** 17 familias de controles (03.01 a 03.17), incluyendo: Control de Acceso (03.01), Concienciación y Entrenamiento (03.02), Auditoría (03.03), Gestión de Configuración (03.04), Identificación y Autenticación (03.05), Respuesta a Incidentes (03.06), Protección de Medios (03.08), Protección Física (03.10), Evaluación de Riesgos (03.11), Evaluación de Seguridad (03.12), Protección de Sistemas (03.13), Integridad de Sistemas (03.14), entre otros.

### Aplicabilidad en el CSF 2.0

Con 310 referencias, cubre principalmente las funciones PROTECT, DETECT y RESPOND:

| Familia SP 800-171 | Código | Subcategorías CSF 2.0 |
|--------------------|--------|----------------------|
| Control de Acceso | 03.01.xx | PR.AA-01 a PR.AA-06 |
| Auditoría | 03.03.xx | DE.AE-03, DE.CM-03 |
| Config. Management | 03.04.xx | PR.PS-01, ID.AM |
| Identificación/Autent. | 03.05.xx | PR.AA-01, PR.AA-03 |
| Respuesta Incidentes | 03.06.xx | RS.MA, RS.AN |
| Evaluación de Riesgos | 03.11.xx | ID.RA-01 a ID.RA-08 |
| Protección Sistemas | 03.13.xx | PR.IR-01, DE.CM |
| Integridad Sistemas | 03.14.xx | DE.CM-09, ID.RA-01 |

### Ejemplo práctico en ciberdefensa

**Situación:** Una empresa aeroespacial contratista del Pentágono desarrolla software de navegación para sistemas de misiles. Debe cumplir SP 800-171 Rev 3.

**Aplicación:**
- **03.01.01 / 03.01.02**: Límites de acceso al sistema: solo personal con necesidad de conocimiento (need-to-know) accede a repositorios de código clasificado → `PR.AA-05`.
- **03.05.03**: Autenticación multifactor para acceso remoto a entornos de desarrollo → `PR.AA-03`.
- **03.14.01**: Identificación, reporte y corrección de vulnerabilidades en software embebido dentro de 30 días → `ID.RA-01`.
- **03.06.01 / 03.06.02**: Establecer capacidad de respuesta a incidentes; reportar incidentes al DoD en 72 horas → `RS.MA-01`, `RS.CO-02`.

---

## 12. SP 800-221A

### Contexto e importancia

**¿Qué es?** NIST SP 800-221A "Information and Communications Technology (ICT) Risk Outcomes" es una guía que integra la gestión de riesgos de TIC con la gestión de riesgos empresariales (ERM). Complementa el SP 800-221 que establece las directrices generales de ERM para TIC.

**¿Por qué es relevante?** El riesgo de TIC no existe en el vacío: afecta directamente a objetivos de negocio. SP 800-221A proporciona el puente conceptual entre el lenguaje técnico de ciberseguridad y el lenguaje financiero y estratégico que entiende la alta dirección. Es como un "intérprete" entre el CISO y el CEO.

**Alcance principal:** Organizado en dos niveles:
- **GV (Govern)**: Gobernanza de riesgos TIC — GV.AD (Administración), GV.BE (Entorno de Negocio), GV.CO (Cumplimiento), GV.CT (Contexto), GV.PO (Política), GV.RR (Roles y Responsabilidades).
- **MA (Manage)**: Gestión de riesgos TIC — MA.IM (Mejora), MA.RA (Evaluación de Riesgos), MA.RI (Respuesta al Riesgo), MA.RM (Monitoreo de Riesgos), MA.RP (Reporte de Riesgos), MA.RR (Registro de Riesgos).

### Aplicabilidad en el CSF 2.0

Con 74 referencias, concentradas principalmente en las funciones GOVERN e IDENTIFY:

| Control SP 800-221A | Descripción | Subcategoría CSF 2.0 |
|---------------------|-------------|----------------------|
| GV.AD-1 / GV.AD-2 | Gobierno y liderazgo | GV.RR-01, GV.RR-02 |
| GV.PO-1 / GV.PO-2 | Políticas de gestión de riesgos TIC | GV.PO-01, GV.PO-02 |
| GV.CT-2 a GV.CT-5 | Contexto de riesgo | GV.OC-01 a GV.OC-05 |
| MA.RA-2 | Evaluación de riesgos TIC | ID.RA-03 |
| MA.RI-1 a MA.RI-4 | Respuesta al riesgo | ID.RA-06, GV.RM |
| MA.RM-2 / MA.RM-3 | Monitoreo de riesgos | GV.OV-01 |

### Ejemplo práctico en ciberdefensa

**Situación:** Un Ministerio de Defensa integra el riesgo cibernético en su marco de gestión de riesgos institucional (ERM).

**Aplicación:**
- **GV.BE-1**: El riesgo cibernético se cuantifica en términos de impacto operacional misión (p.ej., degradación del 30% de capacidad de C2 si el sistema de comunicaciones es comprometido) → `GV.OC-04`.
- **MA.RI-3**: Opciones de respuesta al riesgo evaluadas: aceptar (riesgo residual bajo), mitigar (controles técnicos), transferir (ciberseguro), evitar (discontinuar sistema vulnerable) → `ID.RA-06`.
- **GV.RR-1 / GV.RR-2**: El Jefe de Estado Mayor asume responsabilidad formal por los riesgos cibernéticos operacionales en el plan de campaña → `GV.RR-02`.

---

## 13. SP 800-53 Rev 5.1.1

### Contexto e importancia

**¿Qué es?** NIST Special Publication 800-53 "Security and Privacy Controls for Information Systems and Organizations" Revisión 5.1.1 es el catálogo más completo de controles de seguridad del gobierno federal de EE.UU. Con más de 1,000 controles y mejoras, es el estándar dorado para sistemas de información federales.

**¿Por qué es relevante?** Es el estándar de referencia obligatorio para todas las agencias federales de EE.UU. (per FISMA) y adoptado ampliamente por gobiernos y organizaciones de defensa aliadas. Si el NIST CSF 2.0 es el "mapa estratégico" de ciberseguridad, SP 800-53 es el "manual técnico" con instrucciones detalladas de implementación.

**Alcance principal:** 20 familias de controles identificadas por siglas de dos letras:

| Familia | Sigla | Descripción |
|---------|-------|-------------|
| Access Control | AC | Control de acceso |
| Awareness & Training | AT | Concienciación y entrenamiento |
| Audit & Accountability | AU | Auditoría y responsabilidad |
| Assessment & Auth. | CA | Evaluación y autorización |
| Config. Management | CM | Gestión de configuración |
| Contingency Planning | CP | Planificación de contingencias |
| Identification & Auth. | IA | Identificación y autenticación |
| Incident Response | IR | Respuesta a incidentes |
| Maintenance | MA | Mantenimiento |
| Media Protection | MP | Protección de medios |
| Physical & Env. | PE | Protección física y ambiental |
| Planning | PL | Planificación |
| Program Management | PM | Gestión del programa |
| Personnel Security | PS | Seguridad del personal |
| Privacy | PT | Privacidad |
| Risk Assessment | RA | Evaluación de riesgos |
| System & Serv. Acq. | SA | Adquisición de sistemas y servicios |
| System Comms Prot. | SC | Protección de comunicaciones |
| System & Info Int. | SI | Integridad de sistemas e información |
| Supply Chain Risk | SR | Riesgo en cadena de suministro |

### Aplicabilidad en el CSF 2.0

Con 734 referencias, es el marco más citado junto con Rev 5.2.0. Ejemplos representativos:

| Control SP 800-53 | Descripción | Subcategoría CSF 2.0 |
|-------------------|-------------|----------------------|
| AC-01 | Política de control de acceso | GV.PO-01 |
| AC-02 | Gestión de cuentas | PR.AA-01 |
| AC-06 | Privilegio mínimo | PR.AA-05 |
| AU-06 | Revisión de auditoría | DE.AE-06 |
| AU-12 | Generación de registros de auditoría | DE.AE-03 |
| CA-07 | Monitoreo continuo | DE.CM-01 |
| CM-06 | Configuración de ajustes | PR.PS-01 |
| CM-08 | Inventario de componentes del sistema | ID.AM-01 |
| IR-04 | Manejo de incidentes | RS.MA-03 |
| IR-08 | Plan de respuesta a incidentes | RS.MA-01 |
| PM-09 | Estrategia de gestión de riesgos | GV.RM-01 |
| RA-05 | Escaneo de vulnerabilidades | ID.RA-01 |
| SC-07 | Protección de límites (firewalls) | PR.IR-01 |
| SI-03 | Protección contra código malicioso | DE.CM-09 |
| SI-04 | Monitoreo del sistema | DE.CM-03 |
| SR-02 | Plan de riesgo de cadena de suministro | GV.SC-03 |

### Ejemplo práctico en ciberdefensa

**Situación:** Una agencia de inteligencia nacional implementa un nuevo sistema de análisis de señales electrónicas (SIGINT) clasificado en nivel SECRET.

**Aplicación del proceso RMF con SP 800-53:**
1. **CA-02 (Evaluación de Controles)**: Evaluación independiente de todos los controles implementados antes de autorizar el sistema.
2. **AC-06 (Mínimo Privilegio)**: Analistas solo acceden a datasets relevantes a sus asignaciones específicas; no hay acceso generalizado.
3. **AU-09 (Protección de Información de Auditoría)**: Logs almacenados en sistema separado con integridad criptográfica; solo el auditor jefe puede acceder.
4. **SC-08 (Confidencialidad e Integridad en Transmisión)**: Toda comunicación SIGINT cifrada con criptografía de grado nacional (NSA Type 1).
5. **PM-16 (Programa de Inteligencia de Amenazas)**: Subscripción activa a feeds de inteligencia de amenazas del CISA y aliados de Five Eyes.

---

## 14. SP 800-53 Rev 5.2.0

### Contexto e importancia

**¿Qué es?** Versión actualizada de SP 800-53 (publicada como actualización menor tras Rev 5.1.1). Introduce refinamientos en controles existentes y agrega controles nuevos como:
- **SA-24**: Especialistas en seguridad del software
- **SI-02(07)**: Automatización de remediación de vulnerabilidades
- **SA-15(13)**: Gestión de derechos de propiedad intelectual en software

**¿Por qué es relevante?** La Rev 5.2.0 fortalece el enfoque en seguridad de la cadena de suministro de software (post incidentes como SolarWinds y XZ Utils) y en automatización de operaciones de seguridad.

**Alcance principal:** Idéntico a Rev 5.1.1 en estructura de familias, con refinamientos en controles de SA (Adquisición de Sistemas) y SI (Integridad de Sistemas). Introduce capacidades de automatización más explícitas.

### Aplicabilidad en el CSF 2.0

Con 740 referencias (ligeramente más que Rev 5.1.1), los controles adicionales más relevantes:

| Control nuevo/mejorado | Descripción | Subcategoría CSF 2.0 |
|------------------------|-------------|----------------------|
| SA-15(13) | Gestión IPR en cadena de suministro de software | GV.SC-06 |
| SA-24 | Especialistas en seguridad del ciclo de vida del software | PR.PS-06 |
| SI-02(07) | Automatización de parches y remediación | ID.RA-01 |
| RA-04 | Evaluación de riesgos de tecnología | ID.RA-03 |

### Ejemplo práctico en ciberdefensa

**Situación:** Tras el ataque a la cadena de suministro de software de una empresa de defensa (similar al caso SolarWinds), el Comando Cibernético revisa sus controles de adquisición de software.

**Aplicación de controles Rev 5.2.0:**
- **SA-15(13)**: Verifica derechos de propiedad intelectual y autenticidad de todos los componentes de software de terceros en sistemas críticos de C2 → `GV.SC-06`.
- **SA-10(01)**: Exige repositorio de código fuente con control de versiones y análisis de composición de software (SCA) para detectar dependencias maliciosas → `PR.PS-06`.
- **SI-02(07)**: Implementa pipeline de CI/CD con parches automatizados y pruebas de regresión de seguridad antes de despliegue en sistemas de misión → `ID.RA-01`.

---

## 15. SP-800-37 Rev 2 — Risk Management Framework

### Contexto e importancia

**¿Qué es?** NIST SP 800-37 "Risk Management Framework for Information Systems and Organizations" define el proceso RMF (Risk Management Framework): el ciclo estructurado que las agencias federales deben seguir para autorizar sistemas de información para operar.

**¿Por qué es relevante?** El RMF es el proceso de "certificación y acreditación" (C&A) de sistemas federales. Ningún sistema federal puede operar sin pasar por el RMF. Es como el proceso de certificación de aeronavegabilidad para aviones: antes de volar, el sistema debe ser evaluado y autorizado por una autoridad competente.

**Alcance principal:** 7 pasos del ciclo RMF:

```
PREPARE → CATEGORIZE → SELECT → IMPLEMENT → ASSESS → AUTHORIZE → MONITOR
```

| Paso RMF | Tareas clave |
|----------|-------------|
| **PREPARE** | P-1 a P-17: Roles, estrategia, evaluación de riesgos |
| **CATEGORIZE** | C-2, C-3: Categorización de seguridad (impacto: Bajo/Moderado/Alto) |
| **SELECT** | S-4, S-5: Selección de controles base + mejoras |
| **IMPLEMENT** | I-2: Implementación y documentación de controles |
| **ASSESS** | A-3 a A-6: Evaluación de efectividad de controles |
| **AUTHORIZE** | R-2 a R-5: Análisis de riesgo residual y decisión de autorización |
| **MONITOR** | M-1 a M-7: Monitoreo continuo y gestión de cambios |

### Aplicabilidad en el CSF 2.0

Con 166 referencias, SP-800-37 aparece principalmente en subcategorías de gobernanza y mejora continua:

| Tarea RMF | Descripción | Subcategoría CSF 2.0 |
|-----------|-------------|----------------------|
| TASK P-1 | Roles de gestión de riesgos | GV.RR-02 |
| TASK P-2 | Estrategia de gestión de riesgos | GV.RM-01 |
| TASK P-3 | Evaluación de riesgos organizacional | ID.RA-03 |
| TASK C-2 | Categorización de seguridad | ID.RA-04 |
| TASK A-3 | Evaluación de controles | GV.OV-01 |
| TASK R-2 | Análisis y determinación de riesgo | ID.RA-06 |
| TASK M-1 | Cambios en sistema y entorno | ID.IM-01 |
| TASK M-2 | Evaluaciones continuas | GV.OV-02 |

### Ejemplo práctico en ciberdefensa

**Situación:** El Ejército de EE.UU. despliega un nuevo sistema de mando y control táctico (C2) para operaciones en zona de combate.

**Aplicación del RMF:**
1. **PREPARE (P-14)**: Evaluación de riesgo del sistema C2: amenazas de actores APT estatales, pérdida de comunicaciones en combate.
2. **CATEGORIZE (C-2)**: Impacto ALTO en confidencialidad, integridad y disponibilidad (pérdida puede costar vidas).
3. **SELECT**: Línea base de controles SP 800-53 de ALTO impacto + controles adicionales para amenazas específicas (Electronic Warfare).
4. **ASSESS (A-3)**: Evaluadores independientes (Red Team) validan controles durante ejercicio de campo con adversario simulado.
5. **AUTHORIZE (R-4)**: El General Comandante firma la Autorización de Operación (ATO) con riesgo residual aceptado.
6. **MONITOR (M-2)**: Evaluaciones de seguridad continuas durante operación; cualquier cambio operacional reinicia el ciclo.

---

## 16. SSDF — Secure Software Development Framework

### Contexto e importancia

**¿Qué es?** NIST SP 800-218 "Secure Software Development Framework" (SSDF) define un conjunto de prácticas de desarrollo de software seguro para reducir el número y severidad de vulnerabilidades en productos de software.

**¿Por qué es relevante?** La mayoría de las brechas de seguridad explotan vulnerabilidades en software. El SSDF mueve la seguridad "hacia la izquierda" (shift-left): se integra desde el diseño, no se añade al final como parche. Es la analogía de diseñar una casa con puertas con cerradura desde los planos, en lugar de instalar cerraduras después de construirla.

**Alcance principal:** 4 grupos de prácticas:

| Grupo | Sigla | Descripción |
|-------|-------|-------------|
| Prepare the Organization | PO | Políticas, roles, herramientas y entornos de desarrollo seguro |
| Protect the Software | PS | Protección del código y artefactos de software |
| Produce Well-Secured Software | PW | Prácticas de diseño, codificación y revisión segura |
| Respond to Vulnerabilities | RV | Gestión de vulnerabilidades identificadas post-lanzamiento |

### Aplicabilidad en el CSF 2.0

Con 33 referencias, SSDF aparece concentrado en subcategorías de protección y mejora:

| Control SSDF | Descripción | Subcategoría CSF 2.0 |
|-------------|-------------|----------------------|
| PO.1.1 / PO.1.2 | Políticas y requisitos de seguridad del software | GV.OC-03, GV.PO |
| PO.2.1 / PO.2.2 | Roles y responsabilidades en desarrollo seguro | GV.OC-02, GV.RR |
| PO.3.3 | Implementar canales de divulgación de vulnerabilidades | ID.RA-08 |
| PO.5.1 / PO.5.2 | Proteger entornos de desarrollo | PR.PS-01 |
| PS.1.1 | Proteger el código en repositorios | PR.DS-01 |
| PS.2.1 | Verificar integridad del software | PR.DS-02 |
| PS.3.1 | Gestión de dependencias (SBOM) | GV.SC-06 |
| PW.1.1 | Diseño seguro y modelado de amenazas | ID.RA-03 |
| PW.4.1 / PW.4.4 | Revisión de código y análisis estático (SAST) | PR.PS-06 |

### Ejemplo práctico en ciberdefensa

**Situación:** Una empresa contratista desarrolla firmware para sistemas de comunicaciones tácticas militares (radios SINCGARS). El Departamento de Defensa exige cumplimiento SSDF.

**Aplicación:**
- **PO.1.1**: Se establece política de seguridad del software: todo firmware debe someterse a análisis estático (SAST) y dinámico (DAST) antes del lanzamiento → `GV.PO-01`.
- **PS.3.1**: Se genera un SBOM (Software Bill of Materials) de cada versión de firmware; permite identificar rápidamente si una librería vulnerable (p.ej., OpenSSL) está presente en sistemas desplegados → `GV.SC-06`.
- **PW.4.1**: Revisión de código obligatoria por pares con checklist de seguridad: sin funciones prohibidas (strcpy, gets), sin credenciales hardcodeadas → `PR.PS-06`.
- **PO.3.3**: Canal de divulgación responsable de vulnerabilidades: investigadores externos pueden reportar fallos; tiempo de respuesta garantizado 90 días → `ID.RA-08`.
- **PO.5.2**: Entornos de desarrollo aislados de redes de producción y clasificadas; acceso restringido a ingenieros con habilitación de seguridad → `PR.PS-01`.

---

## Resumen: Distribución de Referencias por Función CSF 2.0

| Función CSF 2.0 | Marcos más relevantes |
|-----------------|----------------------|
| **GOVERN (GV)** | ISO/IEC 27001, SP 800-53, CRI Profile v2.0, SP 800-221A |
| **IDENTIFY (ID)** | SP 800-53, SP 800-37 RMF, NICE Framework, SCF |
| **PROTECT (PR)** | SP 800-53, CCMv4.0, PCI DSS, SP 800-171, CIS Controls |
| **DETECT (DE)** | SP 800-53, NICE Framework, CCMv4.0, SCF |
| **RESPOND (RS)** | SP 800-53, IRP, NICE Framework, CCMv4.0 |
| **RECOVER (RC)** | SP 800-53, CCMv4.0, ISO/IEC 27001, CRI Profile v2.0 |

---

## Notas de Uso

- Las referencias en columna E son **informativas** (no prescriptivas): el CSF 2.0 no exige implementar todos los controles de cada marco, sino que los señala como recursos de implementación compatibles.
- La presencia de un control en múltiples marcos (p.ej., monitoreo de logs aparece en SP 800-53 AU-12, ISO 27001 A.8.15, PCI DSS 10.2, CCMv4.0 LOG-04) permite a las organizaciones satisfacer múltiples obligaciones con una única implementación técnica.
- Para organizaciones de defensa, los marcos más relevantes son: **SP 800-53**, **SP 800-171**, **SP 800-37 RMF**, **NICE Framework** y **SSDF** — todos de origen NIST y con respaldo contractual en el ecosistema de defensa de EE.UU. y sus aliados.

---

*Documento generado a partir del archivo csf2.xlsx — Hoja "CSF 2.0", Columna E (Informative References) — NIST Cybersecurity Framework 2.0*
