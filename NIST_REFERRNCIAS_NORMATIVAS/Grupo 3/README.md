# Documentación de Referencias de Marcos de Ciberseguridad

## Grupo 3

> **Propósito:** Este documento describe cada referencia de marco/norma de ciberseguridad presente en el mapeo de controles, contextualizando su importancia, aplicabilidad en el CSF 2.0 y ejemplos prácticos en entornos de ciberdefensa.

---

## Índice de Marcos

- [CCMv4.0](#ccmv40-cloud-controls-matrix)
- [CIS Controls v8.0](#cis-controls-v80)
- [CRI Profile v2.0](#cri-profile-v20)
- [CSF v1.1 (NIST)](#csf-v11-nist-cybersecurity-framework)
- [NICE Framework v1.0.0](#nice-framework-v100)
- [SP 800-221A](#sp-800-221a)
- [SP 800-53 Rev 5.1.1](#sp-800-53-rev-511)
- [SP 800-218](#sp-800-218)
- [SP 800-37 Rev 2](#sp-800-37-rev-2)

---

## CCMv4.0: Cloud Controls Matrix

### ¿Qué es este marco?

La **Cloud Controls Matrix (CCM) v4.0** es un marco de controles de seguridad específicamente diseñado para entornos de computación en la nube, desarrollado y mantenido por la **Cloud Security Alliance (CSA)**. Proporciona un conjunto de controles organizados en 17 dominios que cubren todos los aspectos de la seguridad en la nube, desde la gobernanza hasta la gestión de identidades y la seguridad física.

### ¿Por qué es relevante en ciberseguridad y ciberdefensa?

La migración masiva de sistemas críticos a entornos cloud ha hecho que CCMv4.0 sea esencial para garantizar que proveedores y clientes de servicios en la nube mantengan estándares de seguridad consistentes. En contextos de defensa, la adopción de nubes gubernamentales (GovCloud, nubes clasificadas) exige controles específicos para proteger información sensible.

### ¿Cuál es su alcance principal?

Cubre la gestión de cadena de suministro (STA), gobernanza de proveedores, seguridad de datos (DSP), control de cambios (CCC), criptografía (CEK), gestión de identidades (IAM), interoperabilidad (IPY), gestión de endpoints (UEM), continuidad del negocio (BCR), respuesta a incidentes (SEF) y recursos humanos (HRS).

---

### CCMv4.0: STA-01 — Política de Gestión de la Cadena de Suministro

**Contexto e importancia:**
STA-01 exige que la organización establezca, documente y revise periódicamente una política formal de gestión de la cadena de suministro de tecnología. Esta política debe definir roles, responsabilidades y requisitos mínimos de seguridad que los proveedores deben cumplir.

**Aplicabilidad en el CSF 2.0:**
Corresponde a la subcategoría **GV.SC-01** (Gobernanza de la Cadena de Suministro de Ciberseguridad). Ayuda a cumplir el resultado de establecer estrategias y políticas que formalicen la gestión del riesgo de terceros.

**Ejemplo práctico en ciberdefensa:**
Una agencia gubernamental de inteligencia debe migrar parte de su infraestructura a un proveedor cloud certificado. STA-01 obliga a que exista una política documentada que establezca: qué tipos de datos pueden alojar proveedores externos, requisitos de certificación mínima (ej. FedRAMP, ISO 27001), y el proceso para incorporar/retirar proveedores. Sin esta política, el riesgo de comprometer información clasificada por un proveedor externo no auditado es significativo.

---

### CCMv4.0: STA-02 — Inventario de Proveedores

**Contexto e importancia:**
Requiere mantener un inventario actualizado de todos los proveedores de servicios en la nube y terceros con acceso a datos o sistemas de la organización.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.SC-02** (Roles y responsabilidades en la cadena de suministro). Permite conocer quiénes son los actores en el ecosistema de proveedores y asignarles responsabilidades de seguridad.

**Ejemplo práctico en ciberdefensa:**
Un comando militar que opera múltiples sistemas de comunicación necesita saber en tiempo real cuántos proveedores externos tienen acceso a sus redes. El inventario de STA-02 permite, ante un incidente, identificar rápidamente si el vector de ataque provino de un proveedor comprometido.

---

### CCMv4.0: STA-03 — Evaluación de Riesgos de Proveedores

**Contexto e importancia:**
Exige que se realicen evaluaciones de riesgo formales antes de contratar a un proveedor y de manera periódica durante la relación contractual.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.SC-03** (Evaluación de riesgo de la cadena de suministro). Asegura que los riesgos introducidos por terceros sean identificados y tratados sistemáticamente.

**Ejemplo práctico en ciberdefensa:**
Antes de contratar un proveedor de servicios de análisis de amenazas (Threat Intelligence), una organización de ciberdefensa nacional aplica STA-03 para evaluar: la jurisdicción legal del proveedor, sus prácticas de seguridad, historial de brechas y exposición a adversarios estatales.

---

### CCMv4.0: STA-04 — Requisitos de Seguridad en Contratos

**Contexto e importancia:**
Establece que los contratos con proveedores deben incluir cláusulas específicas de seguridad, incluyendo notificación de incidentes, derechos de auditoría y requisitos de cumplimiento normativo.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.SC-02 / EX.CN-01** (Contratos con la cadena de suministro). Formaliza los compromisos de seguridad entre las partes.

**Ejemplo práctico en ciberdefensa:**
Una entidad gubernamental que contrata desarrollo de software de misión crítica incluye en el contrato, bajo STA-04: cláusulas de notificación obligatoria de vulnerabilidades en 24 horas, derecho a auditorías de código fuente, y penalidades por incumplimiento de estándares de seguridad definidos.

---

### CCMv4.0: STA-05 — Gestión del Ciclo de Vida de Proveedores

**Contexto e importancia:**
Regula el proceso completo de incorporación, mantenimiento y terminación de relaciones con proveedores, asegurando que los accesos sean revocados y los datos recuperados al finalizar la relación.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.SC-02** (Roles en la cadena de suministro). Garantiza que no queden "puertas traseras" tras finalizar una relación con un proveedor.

**Ejemplo práctico en ciberdefensa:**
Cuando una agencia de defensa finaliza un contrato con un proveedor de servicios cloud, STA-05 obliga a verificar la eliminación segura de todos los datos almacenados, la revocación de credenciales y la validación de que no existan copias de información clasificada en sistemas del proveedor.

---

### CCMv4.0: STA-06 — Auditorías a Proveedores

**Contexto e importancia:**
Requiere que los proveedores sean sometidos a auditorías periódicas de seguridad para verificar el cumplimiento de los requisitos contractuales y regulatorios.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.SC-01 / GV.SC-03**. Proporciona evidencia objetiva de que los controles de seguridad del proveedor funcionan como se espera.

**Ejemplo práctico en ciberdefensa:**
Una organización de infraestructura crítica realiza auditorías anuales —y en ocasiones no anunciadas— a sus proveedores de servicios ICS/SCADA cloud, verificando que los controles de acceso, cifrado y monitoreo cumplan con los estándares acordados en el contrato, alineados con NERC CIP.

---

### CCMv4.0: STA-07 — Evaluación de Componentes de la Cadena de Suministro

**Contexto e importancia:**
Se centra en identificar y evaluar los componentes de hardware y software que forman parte de la cadena de suministro, incluyendo bibliotecas de terceros y componentes de código abierto.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.SC-04** (Evaluación de proveedores). Fundamental para detectar riesgos en software embebido o componentes de origen desconocido.

**Ejemplo práctico en ciberdefensa:**
Ante el riesgo de ataques tipo SolarWinds, una organización de defensa aplica STA-07 para exigir a sus proveedores de software una **Software Bill of Materials (SBOM)**, documentando todos los componentes de terceros incluidos en sus soluciones. Esto permite detectar si alguna librería utilizada tiene vulnerabilidades conocidas (CVEs).

---

### CCMv4.0: STA-08 — Política de Divulgación de Incidentes de Proveedores

**Contexto e importancia:**
Establece los requisitos y plazos para que los proveedores notifiquen a la organización sobre incidentes de seguridad que puedan afectar sus datos o sistemas.

**Aplicabilidad en el CSF 2.0:**
Subcategorías **GV.SC-01 / GV.SC-03**. Asegura que la organización tenga visibilidad oportuna sobre compromisos en su cadena de suministro.

**Ejemplo práctico en ciberdefensa:**
Un contrato bajo STA-08 exige que el proveedor cloud notifique en máximo 4 horas ante cualquier brecha que afecte datos del cliente gubernamental, con actualizaciones cada 2 horas durante la gestión del incidente. Este requisito es crítico para activar los protocolos de respuesta de la organización a tiempo.

---

### CCMv4.0: STA-09 — Evaluación de Riesgo de la Cadena de Suministro

**Contexto e importancia:**
Complementa STA-03 con un enfoque más amplio, considerando riesgos geopolíticos, de concentración y de dependencia en la cadena de suministro tecnológica.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **EX.CN** (Contratos en la cadena de suministro). Permite una visión holística del riesgo de terceros.

**Ejemplo práctico en ciberdefensa:**
Una agencia nacional evalúa bajo STA-09 el riesgo de depender de un único proveedor de semiconductores para sus sistemas de comunicación cifrada. Si dicho proveedor está sujeto a sanciones internacionales o es de origen adversario, el riesgo de backdoors de hardware se vuelve crítico.

---

### CCMv4.0: STA-10 — Métricas y Desempeño de Proveedores

**Contexto e importancia:**
Define indicadores clave de desempeño (KPIs) y métricas de seguridad para evaluar continuamente el rendimiento de los proveedores.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **EX.MM** (Monitoreo y medición). Permite una gestión basada en evidencia del desempeño de seguridad de terceros.

**Ejemplo práctico en ciberdefensa:**
Una organización de defensa establece KPIs de seguridad para sus proveedores: tiempo promedio de remediación de vulnerabilidades críticas (< 48h), porcentaje de controles auditados con cumplimiento > 95%, y número de incidentes reportados por trimestre.

---

### CCMv4.0: STA-11 — Gestión de Riesgos de Proveedores

**Contexto e importancia:**
Integra la gestión de riesgos de proveedores con el programa general de gestión de riesgos de la organización.

**Aplicabilidad en el CSF 2.0:**
Subcategorías **GV.SC-09 / EX.DD** (Diligencia debida). Garantiza que los riesgos de terceros se traten con el mismo rigor que los riesgos internos.

**Ejemplo práctico en ciberdefensa:**
En el proceso de autorización de operación (ATO) de un sistema militar, STA-11 exige que los riesgos identificados en los proveedores del sistema sean documentados en el Plan de Seguridad del Sistema (SSP) y que existan planes de tratamiento activos.

---

### CCMv4.0: STA-12 — Análisis de Impacto de Proveedores

**Contexto e importancia:**
Requiere evaluar el impacto potencial en la operación de la organización si un proveedor clave experimenta una interrupción o un incidente de seguridad.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **EX.MM** (Monitoreo y medición de la cadena de suministro). Fundamental para la planificación de continuidad del negocio.

**Ejemplo práctico en ciberdefensa:**
Antes de una operación crítica, una unidad de ciberdefensa evalúa bajo STA-12 qué pasaría si su proveedor de servicios de inteligencia de amenazas quedara inaccesible. Esto lleva a definir proveedores alternativos y capacidades de respaldo para garantizar la continuidad operacional.

---

### CCMv4.0: STA-13 — Continuidad del Servicio de Proveedores

**Contexto e importancia:**
Exige que los proveedores demuestren capacidades de continuidad del negocio y recuperación ante desastres equivalentes a las requeridas por la organización contratante.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **EX.CN** (Contratos en la cadena de suministro). Asegura que los compromisos de disponibilidad se mantengan incluso bajo condiciones adversas.

**Ejemplo práctico en ciberdefensa:**
Para sistemas de comando y control, STA-13 exige que el proveedor cloud demuestre RPO (Recovery Point Objective) < 1 hora y RTO (Recovery Time Objective) < 4 horas, con pruebas de continuidad documentadas al menos dos veces por año.

---

### CCMv4.0: STA-14 — Mejora Continua en la Gestión de Proveedores

**Contexto e importancia:**
Establece procesos de revisión y mejora continua del programa de gestión de proveedores basados en lecciones aprendidas e incidentes.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **EX.MM** (Monitoreo y medición). Garantiza que el programa de gestión de cadena de suministro evolucione ante nuevas amenazas.

**Ejemplo práctico en ciberdefensa:**
Tras un incidente que afectó a un proveedor en la cadena de suministro, la organización utiliza STA-14 para revisar y actualizar sus controles, incorporando nuevos requisitos de seguridad en contratos futuros basándose en las vulnerabilidades explotadas.

---

### CCMv4.0: UEM-14 — Gestión de Endpoints de Proveedores

**Contexto e importancia:**
Extiende los requisitos de gestión de endpoints (dispositivos) a los proveedores que se conectan a los sistemas de la organización, asegurando que sus dispositivos cumplan con los estándares de seguridad requeridos.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **EX.MM / GV.SC-02**. Controla el riesgo de dispositivos no gestionados de terceros como vector de ataque.

**Ejemplo práctico en ciberdefensa:**
Antes de permitir que los ingenieros de un proveedor accedan remotamente a sistemas de control industrial (ICS), UEM-14 exige verificar que sus dispositivos tengan EDR actualizado, parches al día y cumplan con la política de seguridad de endpoints de la organización.

---

### CCMv4.0: HRS-09 — Acuerdos de Confidencialidad con Terceros

**Contexto e importancia:**
Requiere que todos los proveedores y terceros con acceso a información sensible firmen acuerdos de confidencialidad (NDA) formales.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.SC-02** (Roles y responsabilidades). Protege legalmente la información de la organización compartida con terceros.

**Ejemplo práctico en ciberdefensa:**
Un contratista de defensa que desarrolla software para sistemas de armas debe firmar, bajo HRS-09, un NDA que incluya cláusulas específicas sobre información clasificada, restricciones de exportación y obligaciones post-contractuales de confidencialidad.

---

### CCMv4.0: HRS-10 — Verificación de Antecedentes de Personal de Proveedores

**Contexto e importancia:**
Exige que los proveedores realicen verificaciones de antecedentes equivalentes a las de la organización para el personal que tendrá acceso a sus sistemas o datos.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.SC-02**. Reduce el riesgo de amenazas internas a través de personal de terceros no verificado.

**Ejemplo práctico en ciberdefensa:**
Para sistemas de alto impacto, HRS-10 exige que el personal del proveedor con acceso a redes clasificadas haya pasado una investigación de seguridad equivalente al nivel de habilitación requerido, incluyendo verificación de antecedentes penales internacionales.

---

### CCMv4.0: HRS-13 — Concienciación de Seguridad para Personal de Proveedores

**Contexto e importancia:**
Requiere que el personal de proveedores con acceso a sistemas de la organización reciba formación en concienciación de seguridad adecuada.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.SC-02**. Extiende la cultura de seguridad de la organización a su ecosistema de proveedores.

**Ejemplo práctico en ciberdefensa:**
Antes de dar acceso a un contratista, HRS-13 exige que complete un módulo de entrenamiento sobre amenazas de phishing, ingeniería social y manejo de información sensible, con evaluación aprobatoria documentada.

---

### CCMv4.0: IAM-11 — Gestión de Accesos de Terceros

**Contexto e importancia:**
Regula cómo se otorgan, monitorean y revocan los accesos de proveedores y terceros a los sistemas de la organización, aplicando el principio de mínimo privilegio.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.SC-02**. Previene el acceso no autorizado a través de cuentas de proveedores con permisos excesivos.

**Ejemplo práctico en ciberdefensa:**
Bajo IAM-11, los accesos de proveedores a sistemas militares son limitados en tiempo (sesiones con expiración automática), alcance (solo los sistemas necesarios para su tarea) y se monitorean mediante herramientas PAM (Privileged Access Management) con grabación de sesiones.

---

### CCMv4.0: IPY-04 — Interoperabilidad y Portabilidad de Datos con Proveedores

**Contexto e importancia:**
Asegura que los datos almacenados en servicios de terceros puedan ser exportados y migrados en formatos estándar, evitando el lock-in y garantizando la soberanía de datos.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **EX.CN** (Contratos en la cadena de suministro). Protege la capacidad de la organización de cambiar de proveedor sin perder datos críticos.

**Ejemplo práctico en ciberdefensa:**
Una entidad gubernamental exige, bajo IPY-04, que todos sus datos almacenados en un proveedor cloud puedan ser exportados en formatos abiertos (JSON, CSV, XML) en un plazo máximo de 72 horas, garantizando la continuidad operacional si se requiere migrar a otro proveedor o repatriar datos.

---

### CCMv4.0: CCC-05 — Control de Cambios en la Cadena de Suministro

**Contexto e importancia:**
Extiende el proceso de gestión de cambios para incluir cambios en los componentes de la cadena de suministro, como actualizaciones de software de terceros o cambios en la infraestructura del proveedor.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **EX.CN** (Contratos en la cadena de suministro). Previene que cambios no autorizados en componentes de terceros introduzcan vulnerabilidades.

**Ejemplo práctico en ciberdefensa:**
CCC-05 exige que cualquier actualización de software de un proveedor que afecte sistemas críticos pase por un proceso de evaluación de seguridad antes de su despliegue, incluyendo análisis de composición de software (SCA) para detectar nuevas dependencias vulnerables.

---

### CCMv4.0: CEK-08 — Gestión de Claves Criptográficas con Proveedores

**Contexto e importancia:**
Regula cómo se gestionan las claves criptográficas en entornos de nube compartidos con proveedores, estableciendo quién controla las claves de cifrado.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **EX.CN** (Contratos en la cadena de suministro). Garantiza que la organización mantenga el control sobre sus datos cifrados, incluso cuando los almacena un tercero.

**Ejemplo práctico en ciberdefensa:**
Para datos clasificados en la nube, CEK-08 exige que las claves de cifrado sean gestionadas exclusivamente por la organización mediante un HSM (Hardware Security Module) on-premise, de manera que el proveedor cloud no pueda acceder al contenido en claro bajo ninguna circunstancia.

---

### CCMv4.0: DSP-02, DSP-13, DSP-14, DSP-16, DSP-18 — Seguridad y Privacidad de Datos

**Contexto e importancia:**
Este conjunto de controles del dominio Data Security & Privacy (DSP) regula la clasificación, retención, eliminación, transferencia transfronteriza y compartición de datos con terceros.

**Aplicabilidad en el CSF 2.0:**
Subcategorías **EX.CN / EX.TR** (Contratos y confianza). Garantiza el cumplimiento de requisitos legales y contractuales en el manejo de datos compartidos con proveedores.

**Ejemplo práctico en ciberdefensa:**
- **DSP-13**: Exige que los datos de personal militar almacenados en la nube tengan un período de retención definido y procesos de eliminación segura al expirar.
- **DSP-14**: Requiere procedimientos para gestionar solicitudes de acceso a datos por parte de terceros (incluyendo requerimientos legales extranjeros).
- **DSP-18**: Establece controles para la transferencia transfronteriza de datos, crítico cuando se operan nubes multinacionales en operaciones de coalición.

---

### CCMv4.0: BCR-06, BCR-07 — Continuidad del Negocio y Recuperación

**Contexto e importancia:**
Estos controles del dominio Business Continuity Management (BCR) exigen que los planes de continuidad consideren la dependencia de proveedores cloud y que se realicen pruebas periódicas de recuperación.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.SC-08** (Continuidad y resiliencia en la cadena de suministro). Asegura que la organización pueda operar incluso si un proveedor cloud falla.

**Ejemplo práctico en ciberdefensa:**
Ante un ciberataque que interrumpa un servicio cloud crítico, BCR-06 y BCR-07 garantizan que existan procedimientos documentados y probados para migrar operaciones a un proveedor alternativo o a infraestructura on-premise en un tiempo previamente definido.

---

### CCMv4.0: SEF-03, SEF-04, SEF-07 — Gestión de Eventos de Seguridad

**Contexto e importancia:**
El dominio Security Incident Management, E-Discovery & Cloud Forensics (SEF) regula la detección, reporte y respuesta a incidentes que involucren proveedores cloud, incluyendo capacidades forenses.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.SC-08** (Cadena de suministro y resiliencia). Garantiza que los incidentes que involucren terceros sean gestionados con la misma rigurosidad que los internos.

**Ejemplo práctico en ciberdefensa:**
Ante un incidente que afecte datos gubernamentales en un proveedor cloud, SEF-04 exige que el proveedor proporcione logs forenses en menos de 4 horas para apoyar la investigación, y SEF-07 requiere que se preserve la cadena de custodia de las evidencias digitales recopiladas.

---

## CIS Controls v8.0

### ¿Qué es este marco?

Los **CIS Controls v8.0** (Center for Internet Security Controls) son un conjunto priorizado de acciones de ciberdefensa desarrolladas por consenso entre expertos mundiales. Están organizados en 18 controles críticos clasificados en tres grupos de implementación (IG1, IG2, IG3) según la madurez y tamaño de la organización.

### ¿Por qué es relevante en ciberseguridad y ciberdefensa?

Los CIS Controls son conocidos por su enfoque pragmático y basado en datos sobre las amenazas más comunes. Cada control está mapeado a vectores de ataque reales (MITRE ATT&CK), lo que los hace especialmente útiles para organizaciones que buscan reducir su superficie de ataque con recursos limitados.

### ¿Cuál es su alcance principal?

El **Control 15** específicamente aborda la gestión de proveedores de servicios, estableciendo cómo evaluar, monitorear y gestionar la seguridad de terceros en la cadena de suministro.

---

### CIS Controls v8.0: 15.1 — Establecer un Programa de Gestión de Proveedores

**Contexto e importancia:**
Establece que toda organización debe tener un programa formal documentado para gestionar el riesgo de proveedores de servicios, incluyendo criterios de selección, evaluación continua y requisitos mínimos de seguridad.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.SC-04** (Identificación y evaluación de proveedores). Forma la base estructural del programa de gestión de terceros.

**Ejemplo práctico en ciberdefensa:**
Una organización de infraestructura crítica usa CIS 15.1 para crear un programa que categoriza a sus proveedores en tres niveles de riesgo (Alto, Medio, Bajo) según el acceso que tienen, y aplica controles diferenciados: los proveedores de Alto riesgo requieren auditorías anuales y acceso con autenticación multifactor obligatoria.

---

### CIS Controls v8.0: 15.2 — Establecer Acuerdos de Nivel de Servicio con Proveedores

**Contexto e importancia:**
Los SLAs con proveedores deben incluir métricas de seguridad específicas: tiempos de respuesta ante incidentes, disponibilidad de logs, notificación de brechas y cumplimiento de estándares.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.SC-01** (Política de cadena de suministro). Formaliza los compromisos de seguridad en términos medibles y exigibles.

**Ejemplo práctico en ciberdefensa:**
Un SLA bajo CIS 15.2 para un proveedor de SOC gestionado especifica: detección de amenazas críticas en < 15 minutos, notificación al cliente en < 30 minutos, y disponibilidad del servicio ≥ 99.9%. Estas métricas permiten responsabilizar al proveedor contractualmente por fallos en la defensa.

---

### CIS Controls v8.0: 15.3 — Clasificar a los Proveedores

**Contexto e importancia:**
Requiere clasificar a todos los proveedores según su nivel de acceso y el impacto potencial de un compromiso, para aplicar controles proporcionales al riesgo.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.SC-04** (Evaluación de proveedores). Permite priorizar recursos de gestión de riesgo en los proveedores de mayor impacto.

**Ejemplo práctico en ciberdefensa:**
Una agencia clasifica sus proveedores: Nivel 1 (acceso a sistemas clasificados), Nivel 2 (acceso a red interna sin clasificar), Nivel 3 (solo acceso lógico a sistemas públicos). Los controles aplicados son escalonados: Nivel 1 requiere investigación de seguridad del personal, certificaciones de cumplimiento y auditorías semestrales.

---

### CIS Controls v8.0: 15.4 — Asegurar que los Contratos con Proveedores Incluyan Requisitos de Seguridad

**Contexto e importancia:**
Todos los contratos con proveedores deben incluir requisitos de seguridad explícitos, derechos de auditoría, manejo de datos, notificación de incidentes y condiciones de terminación por incumplimiento de seguridad.

**Aplicabilidad en el CSF 2.0:**
Subcategorías **GV.SC-02 / EX.CN** (Roles y contratos en la cadena de suministro). Garantiza que los acuerdos legales respalden los requisitos de seguridad técnicos.

**Ejemplo práctico en ciberdefensa:**
CIS 15.4 exige que el contrato con un proveedor de servicios de nube para sistemas de gestión de personal militar incluya: cifrado AES-256 de datos en reposo y tránsito, prohibición de subcontratar sin aprobación previa, y obligación de notificar brechas en < 72 horas.

---

### CIS Controls v8.0: 15.5 — Evaluar Proveedores

**Contexto e importancia:**
Exige realizar evaluaciones de seguridad formales de los proveedores antes de la contratación y de manera periódica, utilizando cuestionarios estandarizados, certificaciones de terceros o auditorías directas.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **EX.DD** (Diligencia debida). Proporciona evidencia objetiva de la postura de seguridad de los proveedores.

**Ejemplo práctico en ciberdefensa:**
Antes de contratar un servicio de análisis de malware, CIS 15.5 exige revisar las certificaciones del proveedor (SOC 2 Tipo II, ISO 27001), sus últimos reportes de pruebas de penetración y sus procedimientos de manejo de muestras de malware para evitar filtraciones.

---

### CIS Controls v8.0: 15.6 — Monitorear Proveedores

**Contexto e importancia:**
Establece la necesidad de monitorear continuamente el desempeño de seguridad de los proveedores, incluyendo el seguimiento de incidentes, cambios en su postura de seguridad y cumplimiento de SLAs.

**Aplicabilidad en el CSF 2.0:**
Subcategorías **EX.MM / GV.SC-09** (Monitoreo de la cadena de suministro). Convierte la gestión de proveedores de un proceso puntual a uno continuo.

**Ejemplo práctico en ciberdefensa:**
Una organización de defensa implementa un portal de gestión de proveedores que agrega automáticamente datos de monitoreo: puntuaciones de riesgo de terceros (BitSight, SecurityScorecard), alertas de vulnerabilidades en productos del proveedor (CVEs) y métricas de cumplimiento de SLA en tiempo real.

---

### CIS Controls v8.0: 15.7 — Desincorporar Proveedores de Forma Segura

**Contexto e importancia:**
Cuando se termina una relación con un proveedor, se deben seguir procedimientos formales para revocar accesos, recuperar datos, asegurar la eliminación de información confidencial y verificar que no queden conexiones activas.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **EX.TR** (Transferencia en la cadena de suministro). Cierra el ciclo de vida del proveedor de forma segura.

**Ejemplo práctico en ciberdefensa:**
Al terminar un contrato con un proveedor de inteligencia de amenazas, CIS 15.7 exige: revocar todas las credenciales de API en el día de terminación, obtener certificación escrita de eliminación de datos del cliente, realizar escaneo de red para verificar ausencia de conexiones activas del proveedor, y documentar el proceso para auditorías futuras.

---

## CRI Profile v2.0

### ¿Qué es este marco?

El **Cyber Risk Institute (CRI) Profile v2.0** es un marco de gestión de riesgo cibernético diseñado específicamente para el **sector de servicios financieros**. Mapea requisitos regulatorios financieros (FFIEC, OCC, Fed, FDIC, SEC) al NIST Cybersecurity Framework, proporcionando una herramienta de evaluación unificada para instituciones financieras.

### ¿Por qué es relevante en ciberseguridad y ciberdefensa?

El sector financiero es considerado infraestructura crítica en todos los países. Los ataques a bancos centrales, sistemas de pagos y bolsas de valores pueden tener efectos desestabilizadores equivalentes a ataques militares. El CRI Profile permite a estas instituciones demostrar madurez en ciberdefensa ante múltiples reguladores simultáneamente.

### ¿Cuál es su alcance principal?

Organizado en subcategorías que mapean a las funciones del NIST CSF (Identificar, Proteger, Detectar, Responder, Recuperar), con énfasis en gobernanza, gestión de riesgo de terceros y continuidad operacional.

---

### CRI Profile v2.0: GV.SC-01 / GV.SC-01.01 / GV.SC-01.02 — Estrategia de Cadena de Suministro

**Contexto e importancia:**
Establece que la organización debe tener una estrategia documentada para gestionar el riesgo de la cadena de suministro de ciberseguridad, incluyendo roles, procesos y herramientas.

**Aplicabilidad en el CSF 2.0:**
Directamente en la subcategoría **GV.SC-01** del CSF 2.0. Ayuda a cumplir el resultado de establecer una función de gestión de riesgo de cadena de suministro con recursos asignados.

**Ejemplo práctico en ciberdefensa:**
Un banco central aplica GV.SC-01 para documentar su estrategia de gestión de proveedores críticos de tecnología, incluyendo cómo se evalúan proveedores de sistemas de pago, cómo se monitorean y qué acciones se toman ante deterioro de su postura de seguridad.

---

### CRI Profile v2.0: GV.SC-02 / GV.SC-02.01 — Roles y Responsabilidades en la Cadena de Suministro

**Contexto e importancia:**
Define claramente quién dentro de la organización es responsable de gestionar el riesgo de cada categoría de proveedor, desde la alta dirección hasta los equipos técnicos.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.SC-02** del CSF 2.0. Asegura la rendición de cuentas en la gestión de riesgo de terceros.

**Ejemplo práctico en ciberdefensa:**
Una institución financiera define en GV.SC-02: el CISO es responsable de proveedores de seguridad, el CTO de proveedores de infraestructura cloud, y el responsable de compras de contratos con proveedores Tier 1. Esta claridad asegura que nadie asuma que "alguien más está manejando" un proveedor crítico.

---

### CRI Profile v2.0: GV.SC-03 / GV.SC-03.01 — Inventario de la Cadena de Suministro

**Contexto e importancia:**
Requiere mantener un inventario completo y actualizado de todos los proveedores, su criticidad, el tipo de datos a los que acceden y los sistemas que soportan.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.SC-03** del CSF 2.0. Proporciona la visibilidad necesaria para gestionar el riesgo de terceros efectivamente.

**Ejemplo práctico en ciberdefensa:**
Un operador de infraestructura crítica financiera mantiene un registro de proveedores que incluye para cada uno: nombre, servicios prestados, nivel de acceso, datos procesados, controles de seguridad requeridos y estado actual de cumplimiento. Este inventario es revisado trimestralmente.

---

### CRI Profile v2.0: GV.SC-04 / GV.SC-04.01 — Evaluación de Proveedores

**Contexto e importancia:**
Establece los criterios y el proceso para evaluar la postura de seguridad de los proveedores antes de su contratación y de manera continua.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.SC-04** del CSF 2.0. Garantiza que solo proveedores con controles de seguridad adecuados tengan acceso a sistemas y datos críticos.

**Ejemplo práctico en ciberdefensa:**
Antes de contratar un proveedor de procesamiento de transacciones, GV.SC-04 exige revisar su SOC 2 Tipo II, completar un cuestionario de seguridad de 200+ preguntas y realizar una visita de evaluación presencial a sus centros de datos.

---

### CRI Profile v2.0: GV.SC-08 / GV.SC-08.01 — Resiliencia de la Cadena de Suministro

**Contexto e importancia:**
Evalúa y mejora la capacidad de la organización para continuar operando si un proveedor crítico experimenta una interrupción o un incidente de seguridad.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.SC-08** del CSF 2.0. Alinea la planificación de continuidad con los riesgos específicos de la cadena de suministro.

**Ejemplo práctico en ciberdefensa:**
Un sistema de pagos interbancario aplica GV.SC-08 para mapear sus dependencias críticas de terceros y definir planes de contingencia: si su proveedor principal de conectividad falla, hay un acuerdo pre-establecido con un proveedor alternativo que puede activarse en < 2 horas.

---

### CRI Profile v2.0: GV.SC-09 / GV.SC-09.01 — Monitoreo Continuo de la Cadena de Suministro

**Contexto e importancia:**
Exige mecanismos de monitoreo continuo para detectar cambios en la postura de seguridad de los proveedores, como nuevas vulnerabilidades en sus productos, brechas o cambios regulatorios que les afecten.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.SC-09** del CSF 2.0. Transforma la evaluación puntual de proveedores en un proceso de inteligencia continua.

**Ejemplo práctico en ciberdefensa:**
Una institución financiera suscribe un servicio de clasificación de seguridad de terceros (ej. SecurityScorecard) que monitorea automáticamente a sus 50 proveedores críticos y alerta cuando la puntuación de seguridad de alguno cae por debajo del umbral aceptable, activando el proceso de revisión.

---

### CRI Profile v2.0: EX.CN (Contratos en la Cadena de Suministro)

**Subcategorías:** EX.CN-01, EX.CN-02 y sus sub-niveles (.01 al .04)

**Contexto e importancia:**
El dominio EX.CN aborda la estructura contractual con proveedores, asegurando que los contratos incluyan todos los requisitos de seguridad necesarios y que sean ejecutables ante incumplimientos.

**Aplicabilidad en el CSF 2.0:**
Corresponde a las subcategorías de gestión de contratos en la cadena de suministro del CSF 2.0. Garantiza que los acuerdos legales respalden la postura de seguridad técnica.

**Ejemplo práctico en ciberdefensa:**
Una institución financiera sistematiza bajo EX.CN la plantilla de cláusulas de seguridad para contratos con proveedores, incluyendo: requisitos de cifrado, gestión de accesos, notificación de incidentes, auditorías, manejo de datos personales (GDPR/CCPA) y condiciones de terminación por incumplimiento.

---

### CRI Profile v2.0: EX.DD (Diligencia Debida)

**Subcategorías:** EX.DD-01, EX.DD-02 y sus sub-niveles (.01 al .04)

**Contexto e importancia:**
El dominio EX.DD establece el proceso de due diligence en seguridad que debe realizarse antes de contratar un proveedor y de manera periódica durante la relación.

**Aplicabilidad en el CSF 2.0:**
Corresponde a la función de Identificar del CSF 2.0, específicamente en la gestión de riesgos de terceros. Garantiza que la organización toma decisiones de contratación informadas sobre el riesgo de seguridad.

**Ejemplo práctico en ciberdefensa:**
El proceso de diligencia debida bajo EX.DD para proveedores de sistemas bancarios críticos incluye: revisión de certificaciones (ISO 27001, PCI DSS), análisis de antecedentes corporativos, evaluación de la seguridad de su cadena de suministro propia (cuarto nivel), y revisión de su historial de incidentes.

---

### CRI Profile v2.0: EX.MM (Monitoreo y Medición)

**Subcategorías:** EX.MM-01, EX.MM-02 y sus sub-niveles (.01 al .06)

**Contexto e importancia:**
El dominio EX.MM establece métricas e indicadores para monitorear continuamente el desempeño de seguridad de los proveedores y detectar deterioro en su postura de riesgo.

**Aplicabilidad en el CSF 2.0:**
Corresponde a las funciones de Detectar y Monitorear del CSF 2.0 en el contexto de terceros. Convierte la gestión de proveedores de reactiva a proactiva.

**Ejemplo práctico en ciberdefensa:**
Un banco sistémico implementa bajo EX.MM un cuadro de mando de riesgo de proveedores con KPIs: tiempo promedio de respuesta a incidentes, porcentaje de evaluaciones de seguridad completadas a tiempo, número de hallazgos críticos abiertos por proveedor, y tendencia de puntuación de riesgo trimestral.

---

### CRI Profile v2.0: EX.TR (Transferencia y Terminación)

**Subcategorías:** EX.TR-01, EX.TR-02 y sus sub-niveles

**Contexto e importancia:**
Regula el proceso de transferencia de servicios o terminación de la relación con un proveedor, asegurando que se mantenga la seguridad durante la transición.

**Aplicabilidad en el CSF 2.0:**
Subcategoría relacionada con la función de Responder y Recuperar del CSF 2.0 en contexto de terceros. Garantiza continuidad y seguridad en cambios de proveedor.

**Ejemplo práctico en ciberdefensa:**
Bajo EX.TR, cuando una institución financiera migra su core bancario de un proveedor a otro, el proceso incluye: período de operación en paralelo, verificación de integridad de datos migrados, revocación gradual de accesos del proveedor saliente, y auditoría de seguridad post-migración.

---

## CSF v1.1: NIST Cybersecurity Framework

### ¿Qué es este marco?

El **NIST Cybersecurity Framework v1.1** es un marco voluntario desarrollado por el Instituto Nacional de Estándares y Tecnología de EE.UU. (NIST) para ayudar a organizaciones de todos los sectores a gestionar y reducir el riesgo de ciberseguridad. Está organizado en cinco funciones principales: Identificar, Proteger, Detectar, Responder y Recuperar.

### ¿Por qué es relevante en ciberseguridad y ciberdefensa?

El CSF es ampliamente adoptado por agencias gubernamentales, infraestructura crítica y empresas globales como referencia para evaluar y comunicar la madurez en ciberseguridad. La versión 2.0 (2024) agregó la función "Gobernar" y expandió significativamente el tratamiento de la cadena de suministro.

### ¿Cuál es su alcance principal?

Proporciona un lenguaje común para gestionar el riesgo de ciberseguridad, estructurado en funciones, categorías y subcategorías que se pueden adaptar a cualquier sector o tamaño de organización.

---

### CSF v1.1: ID.SC-1 — Identificar: Política de Cadena de Suministro

**Contexto e importancia:**
Establece que la organización debe tener una política formal y procesos para identificar, evaluar y gestionar los riesgos de la cadena de suministro de ciberseguridad.

**Aplicabilidad en el CSF 2.0:**
En CSF 2.0, esta subcategoría evolucionó y se expandió dentro de la nueva función **Gobernar (GV)**, específicamente en GV.SC (Supply Chain Risk Management).

**Ejemplo práctico en ciberdefensa:**
Una organización gubernamental usa ID.SC-1 como base para su programa de C-SCRM (Cyber Supply Chain Risk Management), estableciendo la política que obliga a todas las unidades a documentar sus proveedores críticos y aplicar controles proporcionales al riesgo que representan.

---

### CSF v1.1: ID.SC-2 — Identificar: Inventario de Proveedores y Partners

**Contexto e importancia:**
Exige identificar y documentar todos los proveedores, partners y terceros en la cadena de suministro que puedan introducir riesgos de ciberseguridad.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.SC-03** del CSF 2.0. La visibilidad de quién está en la cadena de suministro es el primer paso para gestionar su riesgo.

**Ejemplo práctico en ciberdefensa:**
Un operador de infraestructura crítica de energía aplica ID.SC-2 para mantener un registro de todos los proveedores de hardware (PLCs, sensores ICS), software (SCADA, HMI) y servicios (mantenimiento remoto) que tienen acceso —físico o lógico— a sus sistemas de control industrial.

---

### CSF v1.1: ID.SC-3 — Identificar: Contratos con Proveedores

**Contexto e importancia:**
Los contratos con proveedores deben reflejar los requisitos de ciberseguridad de la organización y establecer mecanismos de verificación del cumplimiento.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.SC-06 / EX.CN** del CSF 2.0. Asegura que los acuerdos contractuales sean el vehículo para implementar requisitos de seguridad en terceros.

**Ejemplo práctico en ciberdefensa:**
Bajo ID.SC-3, una agencia de defensa requiere que todos sus contratos con proveedores de TI incluyan el flujo de cláusulas de seguridad del DFARS (Defense Federal Acquisition Regulation Supplement), que exige cumplimiento con NIST SP 800-171 para el manejo de Información No Clasificada Controlada (CUI).

---

### CSF v1.1: ID.SC-4 — Identificar: Evaluación de Proveedores

**Contexto e importancia:**
Los proveedores y partners deben ser evaluados periódicamente para verificar que sus prácticas de ciberseguridad cumplen con los requisitos de la organización.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.SC-04** del CSF 2.0. Garantiza que la evaluación de proveedores sea un proceso continuo, no solo al momento de la contratación.

**Ejemplo práctico en ciberdefensa:**
Una instalación nuclear aplica ID.SC-4 mediante revisiones anuales formales de todos sus proveedores de sistemas de seguridad física-cibernética, verificando que mantengan las certificaciones requeridas y que sus controles de acceso al código fuente de los sistemas que desarrollan cumplan con los estándares de la organización.

---

### CSF v1.1: ID.SC-5 — Identificar: Respuesta a Incidentes con Proveedores

**Contexto e importancia:**
Los planes de respuesta a incidentes y recuperación ante desastres deben incluir proveedores y partners, probando la coordinación conjunta mediante ejercicios periódicos.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.SC-08** del CSF 2.0. Garantiza que la resiliencia operacional incluya la dimensión de terceros en la cadena de suministro.

**Ejemplo práctico en ciberdefensa:**
Una organización de infraestructura crítica financiera realiza anualmente, bajo ID.SC-5, ejercicios de simulación de incidentes (tabletop exercises) que incluyen a sus proveedores críticos de TI, simulando un ataque ransomware que afecta tanto los sistemas internos como los del proveedor de procesamiento de pagos.

---

### CSF v1.1: ID.AM-6 — Identificar: Roles y Responsabilidades en Ciberseguridad

**Contexto e importancia:**
Establece que los roles y responsabilidades de ciberseguridad deben ser definidos y comunicados para todo el personal, incluyendo terceros y proveedores que tienen acceso a sistemas de la organización.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.RR-02** del CSF 2.0 (Roles, responsabilidades y autoridades). Garantiza que no existan ambigüedades sobre quién es responsable de qué en materia de seguridad.

**Ejemplo práctico en ciberdefensa:**
Un ministerio de defensa aplica ID.AM-6 para definir en su política de seguridad que los contratistas de TI son responsables de proteger los datos CUI que manejan, que el ISSO (Information System Security Officer) es responsable de monitorear su cumplimiento, y que el contratista debe reportar incidentes al ISSO en < 1 hora.

---

## NICE Framework v1.0.0

### ¿Qué es este marco?

El **NICE Cybersecurity Workforce Framework v1.0.0** (National Initiative for Cybersecurity Education) es un marco del NIST que proporciona un lenguaje común y taxonomía para describir el trabajo en ciberseguridad. Define categorías de trabajo, áreas de especialización y roles laborales (Work Roles) con sus conocimientos, habilidades y tareas asociadas.

### ¿Por qué es relevante en ciberseguridad y ciberdefensa?

El NICE Framework es esencial para desarrollar la fuerza laboral de ciberseguridad, definir requisitos de personal, crear programas de formación y evaluar la capacidad humana en ciberdefensa. Permite a las organizaciones asegurarse de que tienen el talento adecuado para implementar sus controles de seguridad.

### ¿Cuál es su alcance principal?

Clasifica los roles de ciberseguridad en categorías como: Operar y Mantener (OM), Supervisar y Gobernar (OG), Proteger y Defender (PD), Analizar (AN), Investigar (IN), Recopilar y Operar (CO) e Implementar Provisionalmente (IP).

---

### NICE Framework v1.0.0: OG-WRL-002 — Rol: Gestor de Autorización

**Contexto e importancia:**
Describe las competencias necesarias para el rol que lidera el proceso de Autorización de Operación (ATO) de sistemas, evaluando y aceptando formalmente el riesgo residual de operar un sistema.

**Aplicabilidad en el CSF 2.0:**
Relevante para la función **Gobernar (GV)** del CSF 2.0, específicamente en la toma de decisiones de riesgo basada en evidencia.

**Ejemplo práctico en ciberdefensa:**
En el proceso RMF del DoD, OG-WRL-002 define las competencias del Authorizing Official (AO): debe entender el análisis de riesgo, interpretar evaluaciones de controles y tomar decisiones informadas sobre si los riesgos residuales son aceptables para la misión. Un AO sin las competencias definidas puede autorizar sistemas con riesgos inadmisibles.

---

### NICE Framework v1.0.0: OG-WRL-003 — Rol: Oficial de Seguridad de la Información del Sistema

**Contexto e importancia:**
Define las competencias del ISSO (Information System Security Officer), responsable de la seguridad diaria de sistemas específicos, monitoreo de controles y reporte al ISSM.

**Aplicabilidad en el CSF 2.0:**
Relevante para la función **Proteger** y **Detectar** del CSF 2.0. El ISSO es quien implementa y verifica los controles en el nivel del sistema.

**Ejemplo práctico en ciberdefensa:**
Un ISSO en un sistema de armas aplica OG-WRL-003 para monitorear diariamente los logs de seguridad, gestionar las cuentas de usuarios con privilegios, mantener el Plan de Seguridad del Sistema (SSP) actualizado y coordinar con el proveedor ante vulnerabilidades en el software del sistema.

---

### NICE Framework v1.0.0: OG-WRL-009 — Rol: Gestor de Riesgo de Ciberseguridad

**Contexto e importancia:**
Describe las competencias para el profesional que gestiona el programa de riesgo de ciberseguridad de la organización, integrando evaluaciones de riesgo, tratamientos y métricas en la toma de decisiones estratégicas.

**Aplicabilidad en el CSF 2.0:**
Central para la función **Gobernar (GV.RM)** del CSF 2.0. El gestor de riesgo es quien asegura que los riesgos de ciberseguridad —incluyendo los de la cadena de suministro— se gestionen de forma coherente con la estrategia organizacional.

**Ejemplo práctico en ciberdefensa:**
El Cyber Risk Manager en una agencia gubernamental aplica OG-WRL-009 para desarrollar el programa de C-SCRM: define metodologías de evaluación de riesgo de proveedores, establece umbrales de riesgo aceptable, y reporta trimestralmente a la dirección sobre el estado del riesgo de la cadena de suministro.

---

### NICE Framework v1.0.0: OG-WRL-012 — Rol: Gestor de Seguridad de Sistemas de Información

**Contexto e importancia:**
Define las competencias del ISSM (Information System Security Manager), que supervisa múltiples ISSOs y es responsable del programa de seguridad de información de una organización o unidad.

**Aplicabilidad en el CSF 2.0:**
Relevante para todas las funciones del CSF 2.0. El ISSM es el eje entre la estrategia de seguridad y su implementación en los sistemas.

**Ejemplo práctico en ciberdefensa:**
Un ISSM en un comando militar aplica OG-WRL-012 para supervisar la implementación del programa RMF en 15 sistemas bajo su responsabilidad, asegurando que todos los ISSOs mantengan sus documentos actualizados, que los planes de acción (POA&M) progresen y que los riesgos de cadena de suministro sean reportados al AO.

---

### NICE Framework v1.0.0: OG-WRL-015 — Rol: Oficial de Cumplimiento de Privacidad y Seguridad

**Contexto e importancia:**
Describe las competencias para garantizar que la organización cumpla con los requisitos legales, regulatorios y políticos de seguridad y privacidad, incluyendo los que aplican a proveedores.

**Aplicabilidad en el CSF 2.0:**
Relevante para la función **Gobernar (GV.PO)** del CSF 2.0. El oficial de cumplimiento asegura que las políticas y controles cumplan con el marco legal aplicable.

**Ejemplo práctico en ciberdefensa:**
En una agencia de defensa, el responsable de cumplimiento bajo OG-WRL-015 verifica que todos los contratos con proveedores incluyan las cláusulas DFARS requeridas, que los proveedores hayan completado su autoevaluación CMMC, y que los sistemas que manejan CUI cumplan con NIST SP 800-171.

---

### NICE Framework v1.0.0: OG-WRL-016 — Rol: Ejecutivo de Ciberseguridad

**Contexto e importancia:**
Define las competencias necesarias para los líderes ejecutivos de ciberseguridad (CISO, Director de Ciberseguridad) responsables de la estrategia, recursos y cultura de seguridad organizacional.

**Aplicabilidad en el CSF 2.0:**
Central para la función **Gobernar** del CSF 2.0. El ejecutivo de ciberseguridad es quien establece la visión y asegura los recursos para implementar el framework.

**Ejemplo práctico en ciberdefensa:**
Un CISO en una organización de infraestructura crítica aplica OG-WRL-016 para presentar ante la junta directiva el estado del riesgo de la cadena de suministro, solicitar presupuesto para implementar herramientas de monitoreo de terceros, y establecer políticas que obliguen a todas las unidades de negocio a aplicar C-SCRM.

---

### NICE Framework v1.0.0: IO-WRL-003 — Rol: Desarrollador de Sistemas

**Contexto e importancia:**
Define las competencias para desarrolladores que implementan sistemas de información de forma segura, incluyendo prácticas de desarrollo seguro (SDLC) y gestión de dependencias de terceros.

**Aplicabilidad en el CSF 2.0:**
Relevante para la función **Proteger** del CSF 2.0. Los desarrolladores seguros son la primera línea de defensa contra vulnerabilidades en el software que la organización crea o adquiere.

**Ejemplo práctico en ciberdefensa:**
Un desarrollador en un equipo de software de defensa aplica IO-WRL-003 para: mantener un inventario de dependencias de código abierto (SBOM), ejecutar análisis de composición de software (SCA) en cada build, y asegurar que ninguna librería con CVE crítico sea incluida en el sistema antes de un despliegue operacional.

---

### NICE Framework v1.0.0: IO-WRL-005 — Rol: Especialista en Respuesta a Incidentes

**Contexto e importancia:**
Define las competencias para detectar, analizar, contener y remediar incidentes de ciberseguridad, incluyendo aquellos que involucren compromisos en la cadena de suministro.

**Aplicabilidad en el CSF 2.0:**
Relevante para la función **Responder** del CSF 2.0. El respondedor de incidentes debe tener capacidades específicas para manejar incidentes originados en terceros.

**Ejemplo práctico en ciberdefensa:**
Un especialista en respuesta a incidentes aplica IO-WRL-005 para investigar un posible compromiso de cadena de suministro: analiza los logs del sistema para determinar si una actualización maliciosa de un proveedor de software introdujo un backdoor, documenta el alcance del compromiso y coordina con el proveedor para remediar la brecha.

---

### NICE Framework v1.0.0: DD-WRL-001 — Rol: Analista de Datos

**Contexto e importancia:**
Define las competencias para analistas que procesan y analizan grandes volúmenes de datos de seguridad para identificar patrones, tendencias y amenazas relacionadas con la cadena de suministro.

**Aplicabilidad en el CSF 2.0:**
Relevante para la función **Identificar** del CSF 2.0. Los analistas de datos permiten transformar datos crudos de seguridad de proveedores en inteligencia accionable.

**Ejemplo práctico en ciberdefensa:**
Un analista de datos bajo DD-WRL-001 procesa las puntuaciones de riesgo de 200 proveedores, identificando correlaciones entre características de los proveedores (tamaño, sector, país de origen) y su historial de incidentes, para refinar el modelo de clasificación de riesgo de la organización.

---

### NICE Framework v1.0.0: PD-WRL-003 — Rol: Especialista en Protección de Datos

**Contexto e importancia:**
Define las competencias para proteger datos sensibles de la organización, incluyendo cuando son procesados o almacenados por proveedores externos.

**Aplicabilidad en el CSF 2.0:**
Relevante para la función **Proteger** del CSF 2.0. El especialista en protección de datos asegura que los controles de privacidad y seguridad de datos se extiendan a los proveedores.

**Ejemplo práctico en ciberdefensa:**
Un especialista bajo PD-WRL-003 verifica que los proveedores cloud que procesan datos de personal militar implementen controles de Data Loss Prevention (DLP), que el cifrado de datos en tránsito y reposo cumpla con los estándares requeridos, y que los acuerdos de procesamiento de datos (DPA) incluyan todas las restricciones de uso necesarias.

---

## SP 800-221A

### ¿Qué es este marco?

**NIST SP 800-221A** (Information and Communications Technology Risk Outcomes) es una guía del NIST que describe cómo los resultados del NIST CSF se relacionan con la gestión de riesgos de TIC (Tecnologías de Información y Comunicaciones). Proporciona orientación sobre cómo integrar la gestión de riesgos de ciberseguridad en las prácticas de gestión empresarial.

### ¿Por qué es relevante en ciberseguridad y ciberdefensa?

Ayuda a las organizaciones a conectar los resultados técnicos de ciberseguridad con los objetivos de negocio y misión, justificando inversiones en seguridad en términos de riesgo organizacional. Es especialmente útil para presentar el estado de riesgo ante la alta dirección.

---

### SP 800-221A: GV.PO-1 — Política de Gestión de Riesgos de TIC

**Contexto e importancia:**
Establece la necesidad de una política documentada que defina el enfoque de la organización para gestionar los riesgos de TIC, incluyendo los de la cadena de suministro.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.PO-01** del CSF 2.0. La política es el instrumento que formaliza el compromiso de la dirección con la gestión del riesgo de ciberseguridad.

**Ejemplo práctico en ciberdefensa:**
La política de gestión de riesgos TIC bajo GV.PO-1 en una agencia gubernamental establece: niveles de apetito de riesgo para diferentes categorías de sistemas, autoridades para aceptar riesgos residuales, y el proceso para tratar riesgos que exceden el umbral aceptable, incluyendo los provenientes de proveedores comprometidos.

---

### SP 800-221A: GV.RR-1 / GV.RR-2 — Roles y Responsabilidades de Gestión de Riesgos

**Contexto e importancia:**
Define cómo los roles de gestión de riesgos de TIC deben ser establecidos, asignados y comunicados en la organización, desde la alta dirección hasta los equipos técnicos.

**Aplicabilidad en el CSF 2.0:**
Subcategorías **GV.RR-01 / GV.RR-02** del CSF 2.0. Asegura la rendición de cuentas en la gestión del riesgo de ciberseguridad.

**Ejemplo práctico en ciberdefensa:**
Una organización de defensa formaliza bajo GV.RR-1 y GV.RR-2 la estructura de responsabilidades: el Jefe de Adquisiciones es responsable de que todos los contratos incluyan requisitos C-SCRM, el CISO de que las evaluaciones de riesgo de proveedores sean realizadas, y el AO de aceptar formalmente los riesgos residuales documentados.

---

### SP 800-221A: GV.CT-2 / GV.CT-3 — Cultura y Entrenamiento en Gestión de Riesgos

**Contexto e importancia:**
Establece que la organización debe promover una cultura de concienciación del riesgo y que el personal con responsabilidades en ciberseguridad tenga la formación adecuada para sus roles.

**Aplicabilidad en el CSF 2.0:**
Subcategorías **GV.AT-01 / GV.AT-02** del CSF 2.0 (Concienciación y entrenamiento). La gestión efectiva del riesgo requiere tanto controles técnicos como competencias humanas.

**Ejemplo práctico en ciberdefensa:**
Bajo GV.CT-2 y GV.CT-3, una organización desarrolla un programa de formación específico para gestores de contratos sobre cómo evaluar el riesgo de seguridad de proveedores, cómo interpretar certificaciones de seguridad (SOC 2, ISO 27001) y cómo incluir cláusulas de seguridad efectivas en contratos.

---

### SP 800-221A: MA.RM-2 / MA.RM-3 — Gestión de Riesgos de Madurez

**Contexto e importancia:**
Proporciona criterios para evaluar la madurez del programa de gestión de riesgos de TIC y define los pasos para mejorar continuamente su efectividad.

**Aplicabilidad en el CSF 2.0:**
Relacionado con la mejora continua en la función **Gobernar** del CSF 2.0. Permite a las organizaciones medir su progreso en la implementación del framework.

**Ejemplo práctico en ciberdefensa:**
Una agencia gubernamental usa MA.RM-2 y MA.RM-3 para realizar una evaluación anual de la madurez de su programa C-SCRM, identificando brechas (ej. falta de monitoreo continuo de proveedores) y definiendo un plan de mejora con hitos específicos para el siguiente año fiscal.

---

## SP 800-53 Rev 5.1.1

### ¿Qué es este marco?

**NIST SP 800-53 Rev 5.1.1** es el catálogo de controles de seguridad y privacidad más completo del NIST, utilizado principalmente por agencias federales de EE.UU. pero ampliamente adoptado en el sector privado y defensa globalmente. Contiene más de 1,000 controles organizados en 20 familias.

### ¿Por qué es relevante en ciberseguridad y ciberdefensa?

Es el estándar de referencia para el proceso Risk Management Framework (RMF) del DoD y las agencias civiles federales. Proporciona controles específicos y medibles para cada aspecto de la seguridad de sistemas de información, desde el control de acceso hasta la gestión de la cadena de suministro.

---

### SP 800-53 Rev 5.1.1: SR-01 al SR-10 — Familia: Gestión de Riesgos de la Cadena de Suministro

**Contexto e importancia:**
La familia **Supply Chain Risk Management (SR)** fue introducida en Rev 5 y proporciona controles específicos para gestionar los riesgos de la cadena de suministro de TIC, incluyendo la selección de proveedores, evaluación, monitoreo y terminación de relaciones.

**Aplicabilidad en el CSF 2.0:**
Corresponde directamente a la nueva función **Gobernar (GV.SC)** del CSF 2.0. Los controles SR son la implementación técnica de las políticas y estrategias de gestión de la cadena de suministro.

**Controles clave:**

| Control | Nombre | Descripción |
|---------|--------|-------------|
| SR-01 | Política y Procedimientos | Documentar la política de C-SCRM |
| SR-02 | Plan de Gestión de Riesgos SC | Plan formal de C-SCRM |
| SR-03 | Controles de Cadena de Suministro | Implementar controles de seguridad SC |
| SR-05 | Acuerdos con Proveedores | Contratos con requisitos de seguridad |
| SR-06 | Revisiones de Proveedores | Auditorías y evaluaciones periódicas |
| SR-08 | Notificación de Cambios | Proveedores notifican cambios relevantes |
| SR-10 | Inspección de Componentes | Verificar integridad de componentes adquiridos |

**Ejemplo práctico en ciberdefensa:**
Un sistema de armas bajo el proceso RMF implementa SR-03 exigiendo que todos los componentes de hardware y software sean adquiridos de proveedores en la lista de fuentes aprobadas (Qualified Products List), y que cualquier componente de origen desconocido sea inspeccionado antes de su instalación para detectar componentes falsificados o adulterados.

---

### SP 800-53 Rev 5.1.1: SA-04 / SA-09 — Familia: Adquisición de Sistemas y Servicios

**Contexto e importancia:**
**SA-04** (Proceso de Adquisición) exige que los requisitos de seguridad sean incluidos en todos los contratos de adquisición de sistemas y servicios de TIC. **SA-09** (Servicios de Sistemas de Información Externos) establece controles para monitorear y hacer cumplir los requisitos de seguridad en servicios provistos por externos.

**Aplicabilidad en el CSF 2.0:**
Subcategorías **GV.SC-05 / GV.SC-06** del CSF 2.0. Son controles fundamentales para asegurar que el ciclo de adquisición de tecnología incorpore seguridad desde el inicio.

**Ejemplo práctico en ciberdefensa:**
Bajo SA-04, una agencia de defensa requiere que el contrato de desarrollo de un sistema de comunicaciones seguras incluya: requisitos de seguridad derivados de su categorización FIPS 199, obligación de entregar un SBOM, pruebas de penetración antes de la entrega, y la posibilidad de auditar el código fuente. SA-09 exige que el proveedor de la infraestructura cloud que aloja el sistema proporcione reportes de cumplimiento mensuales y notifique incidentes en < 1 hora.

---

### SP 800-53 Rev 5.1.1: PM-09 / PM-28 / PM-30 / PM-31 — Familia: Gestión de Programas

**Contexto e importancia:**
Los controles de la familia **Program Management (PM)** garantizan que los programas de seguridad de la información tengan el apoyo organizacional, recursos y estructura de gobernanza necesarios.

- **PM-09**: Estrategia de gestión de riesgos
- **PM-28**: Evaluación de riesgos de la cadena de suministro
- **PM-30**: Programa de seguridad de la cadena de suministro
- **PM-31**: Programa de gestión continua de vulnerabilidades

**Aplicabilidad en el CSF 2.0:**
Subcategorías **GV.RM / GV.SC** del CSF 2.0. Estos controles establecen la infraestructura organizacional para gestionar el riesgo de ciberseguridad a nivel estratégico.

**Ejemplo práctico en ciberdefensa:**
PM-30 exige que una agencia federal establezca un programa formal de C-SCRM con: un oficial designado responsable del programa, procesos documentados para la evaluación de proveedores, herramientas de monitoreo de terceros, y métricas de desempeño que se reportan a la alta dirección trimestralmente.

---

### SP 800-53 Rev 5.1.1: RA-03 / RA-05 / RA-07 / RA-09 — Familia: Evaluación de Riesgos

**Contexto e importancia:**
La familia **Risk Assessment (RA)** proporciona controles para evaluar sistemáticamente los riesgos de ciberseguridad, incluyendo los provenientes de la cadena de suministro.

- **RA-03**: Evaluación de riesgos (incluyendo de terceros)
- **RA-05**: Escaneo de vulnerabilidades
- **RA-07**: Respuesta a riesgos
- **RA-09**: Criticidad de componentes

**Aplicabilidad en el CSF 2.0:**
Subcategorías **ID.RA** del CSF 2.0 (Evaluación de riesgos). Proporcionan la metodología para identificar y cuantificar los riesgos de la cadena de suministro.

**Ejemplo práctico en ciberdefensa:**
RA-09 exige identificar los componentes críticos del sistema (aquellos cuya falla o compromiso tendría mayor impacto en la misión) y aplicar controles adicionales de la cadena de suministro para esos componentes específicos. Por ejemplo, en un sistema de radar, el procesador de señales es identificado como componente crítico y requiere verificación de procedencia y pruebas de integridad adicionales.

---

### SP 800-53 Rev 5.1.1: AC-01 / AT-01 / AU-01 / CA-01 / CM-01 y familias políticas

**Contexto e importancia:**
Los controles "-01" de cada familia (AC, AT, AU, CA, CM, CP, IA, IR, MA, MP, PE, PL, PM, PS, PT, RA, SA, SC, SI, SR) exigen que cada dominio de seguridad tenga una política documentada y procedimientos aprobados y revisados periódicamente.

**Aplicabilidad en el CSF 2.0:**
Corresponden a la subcategoría **GV.PO** (Políticas) del CSF 2.0. Las políticas son la base documental que demuestra el compromiso de la organización con cada aspecto de la seguridad.

**Ejemplo práctico en ciberdefensa:**
Bajo el proceso RMF, antes de que un sistema pueda ser autorizado para operación (ATO), el ISSO debe demostrar que existen políticas aprobadas para todas las familias de controles aplicables, que esas políticas han sido revisadas en los últimos 3 años, y que los procedimientos de implementación están documentados y son coherentes con las políticas.

---

### SP 800-53 Rev 5.1.1: CP-01 / IR-01 — Continuidad y Respuesta a Incidentes

**Contexto e importancia:**
**CP-01** establece la política de planificación de contingencia, y **IR-01** la política de respuesta a incidentes. Ambas deben extenderse a escenarios que involucren proveedores y cadena de suministro.

**Aplicabilidad en el CSF 2.0:**
Subcategorías **RC.PO / RS.PO** del CSF 2.0 (Políticas de recuperación y respuesta). Garantizan que la organización esté preparada para responder a incidentes que afecten su cadena de suministro.

**Ejemplo práctico en ciberdefensa:**
Bajo IR-01, el plan de respuesta a incidentes de una organización de defensa incluye playbooks específicos para incidentes de cadena de suministro: qué hacer si se descubre malware en una actualización de software de un proveedor, cómo coordinar con el proveedor, cómo comunicar a los afectados y cuándo escalar al CISA o equivalente nacional.

---

### SP 800-53 Rev 5.1.1: PM-19 — Oficial de Gestión de Privacidad

**Contexto e importancia:**
Requiere que la organización designe un oficial de privacidad con la autoridad y recursos necesarios para implementar el programa de privacidad, incluyendo en relación con proveedores que procesan datos personales.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.RR-03** del CSF 2.0 (Roles y responsabilidades). Asegura que la privacidad tenga un responsable formal con autoridad para hacer cumplir los requisitos con proveedores.

**Ejemplo práctico en ciberdefensa:**
El oficial de privacidad bajo PM-19 revisa todos los contratos con proveedores que procesen datos biométricos de personal militar, asegurando que incluyan: restricciones de uso de datos, obligaciones de eliminación segura, y notificación en caso de brecha que afecte datos personales.

---

## SP 800-218

### ¿Qué es este marco?

**NIST SP 800-218** (Secure Software Development Framework - SSDF) proporciona prácticas de alto nivel para el desarrollo seguro de software, aplicables tanto a organizaciones que desarrollan software internamente como para exigir a proveedores que entreguen software desarrollado de forma segura.

### ¿Por qué es relevante en ciberseguridad y ciberdefensa?

Los ataques a la cadena de suministro de software (como SolarWinds, Log4Shell, XZ Utils) han demostrado que el software es el vector más crítico de la cadena de suministro. El SSDF proporciona un marco para reducir este riesgo mediante prácticas de desarrollo seguro.

---

### SP 800-218: PO.1.3 — Implementar Revisiones de Componentes de Terceros

**Contexto e importancia:**
Exige que las organizaciones identifiquen y evalúen la seguridad de todos los componentes de software de terceros (bibliotecas, frameworks, APIs) incluidos en sus aplicaciones.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **EX.CN** (Contratos en la cadena de suministro de software). Fundamental para prevenir que vulnerabilidades en dependencias de terceros comprometan el software propio.

**Ejemplo práctico en ciberdefensa:**
Bajo PO.1.3, el equipo de desarrollo de software de un sistema de mando y control exige a sus contratistas entregar, junto con cada versión del software, una SBOM (Software Bill of Materials) completa. El equipo de seguridad usa esta SBOM para verificar automáticamente si algún componente tiene CVEs conocidos antes de aprobar el despliegue.

---

### SP 800-218: PO.2.1 — Definir Criterios de Seguridad para Componentes de Terceros

**Contexto e importancia:**
Establece que la organización debe definir criterios mínimos de seguridad que deben cumplir los componentes de software de terceros antes de ser utilizados, incluyendo el estado de soporte, historial de vulnerabilidades y prácticas de desarrollo del proveedor.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.SC-02** (Roles y responsabilidades en la cadena de suministro de software). Define estándares mínimos para el software de terceros.

**Ejemplo práctico en ciberdefensa:**
PO.2.1 lleva a una organización a crear una política que prohíbe el uso de bibliotecas de código abierto que no hayan tenido una actualización de seguridad en los últimos 12 meses, que tengan vulnerabilidades críticas sin parchar, o que provengan de repositorios sin proceso de revisión de código verificable.

---

### SP 800-218: PW.4.1 / PW.4.4 — Reutilización Segura de Software

**Contexto e importancia:**
Establece prácticas para el uso seguro de software de terceros y componentes reutilizables, incluyendo la verificación de su integridad, el análisis de vulnerabilidades y la gestión de actualizaciones.

**Aplicabilidad en el CSF 2.0:**
Subcategorías **GV.SC-03 / EX.MM** (Inventario y monitoreo de la cadena de suministro de software). Asegura que los componentes reutilizados no introduzcan vulnerabilidades en los sistemas.

**Ejemplo práctico en ciberdefensa:**
Bajo PW.4.1 y PW.4.4, un equipo de desarrollo de software de defensa implementa un repositorio interno de componentes aprobados (Artifact Repository) donde solo se almacenan versiones verificadas y sin vulnerabilidades críticas. Cualquier componente externo debe pasar por una revisión de seguridad antes de ser añadido al repositorio.

---

## SP 800-37 Rev 2

### ¿Qué es este marco?

**NIST SP 800-37 Rev 2** describe el **Risk Management Framework (RMF)** para sistemas de información, proporcionando un proceso estructurado de 7 pasos (Preparar, Categorizar, Seleccionar, Implementar, Evaluar, Autorizar, Monitorear) para gestionar el riesgo de seguridad y privacidad en sistemas federales.

### ¿Por qué es relevante en ciberseguridad y ciberdefensa?

El RMF es el proceso obligatorio para todos los sistemas de información del gobierno federal de EE.UU. y el Departamento de Defensa. Es también ampliamente adoptado como estándar de facto para sistemas críticos en el sector privado y gobiernos aliados.

---

### SP-800-37 Rev 2: RMF Prepare Step (Organización) — TASK P-1: Roles de Gestión de Riesgos

**Contexto e importancia:**
Define los roles formales que deben ser establecidos antes de iniciar el RMF: Authorizing Official (AO), Information System Owner (ISO), ISSM, ISSO y System Security Officer (SSO). Cada rol tiene responsabilidades específicas en la gestión del riesgo del sistema.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.RR** del CSF 2.0. Garantiza que la gobernanza de la seguridad del sistema tenga una estructura formal de rendición de cuentas.

**Ejemplo práctico en ciberdefensa:**
Antes de iniciar el desarrollo de un sistema de vigilancia aérea, P-1 exige designar formalmente: quién es el AO responsable de autorizar la operación del sistema, quién es el ISO dueño del sistema, y quién es el ISSM responsable del programa de seguridad. Sin esta estructura, nadie tiene autoridad formal para tomar decisiones de riesgo.

---

### SP-800-37 Rev 2: RMF Prepare Step (Organización) — TASK P-2: Estrategia de Gestión de Riesgos

**Contexto e importancia:**
Exige que la organización desarrolle, documente y comunique una estrategia de gestión de riesgos que incluya la tolerancia al riesgo, las prioridades de la misión y los enfoques para tratar riesgos de ciberseguridad, incluyendo los de la cadena de suministro.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.RM-01** del CSF 2.0. La estrategia de riesgo es el marco dentro del cual se toman todas las decisiones de seguridad.

**Ejemplo práctico en ciberdefensa:**
La estrategia de gestión de riesgos bajo P-2 para un comando militar establece: sistemas clasificados secretos no pueden operar con riesgo alto sin aprobación del Comandante, los riesgos de cadena de suministro de componentes COTS deben evaluarse con el mismo rigor que los riesgos técnicos del sistema, y cualquier componente de origen de país adversario requiere aprobación especial del AO.

---

### SP-800-37 Rev 2: RMF Prepare Step (Organización) — TASK P-3: Evaluación de Riesgos Organizacional

**Contexto e importancia:**
Exige realizar una evaluación de riesgos a nivel organizacional que considere las amenazas al sector, las vulnerabilidades de la cadena de suministro y los impactos potenciales en la misión.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **ID.RA** del CSF 2.0. La evaluación organizacional del riesgo informa la selección de controles para todos los sistemas.

**Ejemplo práctico en ciberdefensa:**
Bajo P-3, una agencia de inteligencia realiza anualmente una evaluación de riesgos que incluye: amenazas de actores estatales a su cadena de suministro tecnológica, vulnerabilidades en los productos de sus principales proveedores identificadas en el período, y cambios en el entorno geopolítico que puedan afectar la confiabilidad de ciertos proveedores.

---

### SP-800-37 Rev 2: RMF Prepare Step (Organización) — TASK P-7: Estrategia de Monitoreo Continuo

**Contexto e importancia:**
Establece la estrategia de monitoreo continuo a nivel organizacional que define qué controles se monitorean continuamente, con qué frecuencia y cómo los resultados se integran en las decisiones de autorización.

**Aplicabilidad en el CSF 2.0:**
Subcategorías **ID.IM / DE.CM** del CSF 2.0. El monitoreo continuo es lo que convierte la autorización puntual en una gestión dinámica del riesgo.

**Ejemplo práctico en ciberdefensa:**
La estrategia de monitoreo continuo bajo P-7 para una organización de defensa establece: los controles de gestión de identidades se evalúan mensualmente mediante herramientas automatizadas, los controles de gestión de configuración se evalúan semanalmente, y los riesgos de cadena de suministro (incluyendo nuevas vulnerabilidades en productos de proveedores) se monitorean con feeds de inteligencia de amenazas en tiempo real.

---

### SP-800-37 Rev 2: RMF Prepare Step (Sistema) — TASK P-9: Stakeholders del Sistema

**Contexto e importancia:**
Requiere identificar a todos los interesados relevantes del sistema, incluyendo proveedores, operadores, usuarios finales y otras partes afectadas por la operación del sistema.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.RR** del CSF 2.0. Asegura que todas las partes interesadas, incluyendo proveedores, sean consideradas en el proceso de gestión del riesgo del sistema.

**Ejemplo práctico en ciberdefensa:**
Para un sistema de gestión de cadena de suministro logístico del ejército, P-9 identifica como stakeholders no solo a los usuarios militares sino también a los proveedores contratados que acceden al sistema para actualizar estados de inventario. Esto lleva a incluir requisitos de seguridad específicos para el acceso de proveedores en los controles del sistema.

---

### SP-800-37 Rev 2: RMF Prepare Step (Sistema) — TASK P-10: Identificación de Activos

**Contexto e importancia:**
Requiere identificar y documentar todos los activos del sistema, incluyendo componentes de hardware, software, datos y servicios de terceros que forman parte del sistema o de su cadena de suministro.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **ID.AM** del CSF 2.0 (Gestión de activos). Sin conocer qué activos forman parte del sistema y de qué proveedores provienen, no es posible gestionar los riesgos de la cadena de suministro.

**Ejemplo práctico en ciberdefensa:**
Bajo P-10, el inventario de activos de un sistema de radar incluye no solo el hardware propio sino también las librerías de software de terceros incluidas en el sistema de procesamiento de señales, los certificados digitales provistos por una autoridad de certificación externa, y los servicios de sincronización de tiempo utilizados. Cada componente de terceros es documentado con su proveedor, versión y estado de soporte.

---

### SP-800-37 Rev 2: RMF Prepare Step (Sistema) — TASK P-14: Evaluación de Riesgos del Sistema

**Contexto e importancia:**
Exige realizar una evaluación de riesgos específica del sistema que identifique amenazas, vulnerabilidades (incluyendo las de la cadena de suministro) e impactos potenciales en la misión.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **ID.RA** del CSF 2.0. Esta evaluación es la base técnica para la selección de controles apropiados para el sistema.

**Ejemplo práctico en ciberdefensa:**
La evaluación de riesgos bajo P-14 para un sistema de comunicaciones tácticas identifica como riesgo de alta prioridad: el uso de un chip de procesamiento fabricado en un país de preocupación, que podría contener hardware malicioso (hardware implant). Este riesgo lleva a implementar controles adicionales de monitoreo de tráfico y aislamiento de red para el sistema.

---

### SP-800-37 Rev 2: RMF Prepare Step (Sistema) — TASK P-15: Definición de Requisitos

**Contexto e importancia:**
Requiere definir los requisitos de seguridad y privacidad del sistema, incluyendo los que aplican a componentes y servicios de la cadena de suministro.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.SC-06** del CSF 2.0. Los requisitos de seguridad son el puente entre la política organizacional y la implementación técnica en sistemas y contratos.

**Ejemplo práctico en ciberdefensa:**
Bajo P-15, los requisitos de seguridad de un sistema de mando y control incluyen: todos los componentes COTS deben provenir de la Lista de Productos Aprobados (APL), el software embebido debe ser verificado con análisis de código estático y dinámico, y los proveedores de servicios cloud deben mantener certificación FedRAMP Moderate o superior durante toda la vida del contrato.

---

### SP-800-37 Rev 2: RMF Select Step — TASK S-5: Estrategia de Monitoreo Continuo del Sistema

**Contexto e importancia:**
Define la estrategia de monitoreo continuo específica para el sistema, incluyendo qué controles se monitorean, con qué herramientas y cómo los resultados se reportan al AO para apoyar la toma de decisiones de autorización continua.

**Aplicabilidad en el CSF 2.0:**
Subcategorías **DE.CM / ID.IM** del CSF 2.0. Establece el mecanismo técnico para el monitoreo continuo de los controles del sistema, incluyendo los que mitigan riesgos de cadena de suministro.

**Ejemplo práctico en ciberdefensa:**
Bajo S-5, la estrategia de monitoreo del sistema incluye: escaneo automatizado diario de vulnerabilidades en todos los componentes de software del sistema (incluyendo librerías de terceros), alertas automáticas cuando se publican CVEs críticos en productos incluidos en el SBOM del sistema, y revisión mensual del estado de los proveedores de servicios externalizados.

---

### SP-800-37 Rev 2: RMF Assess Step — TASK A-3, A-5, A-6: Evaluación, Remediación y POA&M

**Contexto e importancia:**
- **A-3**: Evaluación formal de controles por un evaluador independiente
- **A-5**: Acciones de remediación de hallazgos de la evaluación
- **A-6**: Plan de Acción y Hitos (POA&M) para tracking de remediaciones pendientes

**Aplicabilidad en el CSF 2.0:**
Subcategorías **ID.IM / RS.MI** del CSF 2.0 (Mejora continua y mitigación). El ciclo evaluar-remediar-planificar es lo que mantiene la postura de seguridad del sistema en el tiempo.

**Ejemplo práctico en ciberdefensa:**
En la evaluación bajo A-3 de un sistema de logística, el evaluador identifica que el proveedor de la base de datos no ha aplicado un parche crítico en 90 días. Bajo A-5 se exige remediación inmediata, y bajo A-6 se crea un elemento en el POA&M con fechas límite y responsables para verificar el parche y cualquier otro hallazgo similar.

---

### SP-800-37 Rev 2: RMF Authorize Step — TASK R-2, R-3: Análisis y Respuesta al Riesgo

**Contexto e importancia:**
- **R-2**: Análisis formal del riesgo residual del sistema por el AO, considerando todos los hallazgos y riesgos identificados
- **R-3**: Decisión formal del AO sobre cómo responder al riesgo: aceptar, mitigar, transferir o evitar

**Aplicabilidad en el CSF 2.0:**
Subcategoría **GV.RM-06** del CSF 2.0 (Respuesta al riesgo). La autorización formal es el mecanismo de gobernanza que asegura que alguien con autoridad acepta formalmente los riesgos del sistema.

**Ejemplo práctico en ciberdefensa:**
El AO bajo R-2 y R-3 revisa el riesgo de cadena de suministro identificado (chip de fabricación extranjera con posible backdoor) y decide en R-3: acepta el riesgo con controles compensatorios (aislamiento de red, monitoreo de tráfico anómalo), documenta la decisión, y establece una revisión en 6 meses para evaluar si hay nueva inteligencia sobre el fabricante.

---

### SP-800-37 Rev 2: RMF Monitor Step — TASK M-1, M-2, M-3: Monitoreo Continuo Operacional

**Contexto e importancia:**
- **M-1**: Monitoreo de cambios en el sistema y su entorno (incluyendo cambios en proveedores)
- **M-2**: Evaluaciones continuas de controles seleccionados
- **M-3**: Respuesta continua a riesgos emergentes identificados en el monitoreo

**Aplicabilidad en el CSF 2.0:**
Subcategorías **DE.CM / ID.IM / RS.MI** del CSF 2.0. El monitoreo continuo cierra el ciclo del RMF, convirtiendo la autorización puntual en gestión dinámica del riesgo.

**Ejemplo práctico en ciberdefensa:**
Bajo M-1, el sistema detecta que el proveedor de un componente crítico fue adquirido por una empresa de un país adversario. Esta información, capturada a través del sistema de inteligencia de amenazas de la organización, activa bajo M-3 una revisión de emergencia del riesgo de ese componente y una evaluación de si la autorización existente sigue siendo válida o debe ser revisada.

---

### SP-800-37 Rev 2: RMF Monitor Step — TASK M-7: Disposición del Sistema

**Contexto e importancia:**
Define las acciones de seguridad requeridas cuando un sistema es retirado de servicio, incluyendo la eliminación segura de datos, revocación de accesos y notificación a todas las partes relevantes, incluyendo proveedores.

**Aplicabilidad en el CSF 2.0:**
Subcategoría **EX.TR** del CSF 2.0 (Terminación). Garantiza que el ciclo de vida del sistema finalice de forma segura, sin dejar datos o accesos residuales.

**Ejemplo práctico en ciberdefensa:**
Bajo M-7, cuando un sistema de comunicaciones seguras es retirado, el proceso incluye: notificar a todos los proveedores con acceso activo para que revoquen sus credenciales, destruir físicamente los medios de almacenamiento con datos clasificados siguiendo los procedimientos de eliminación segura (NSA/CSS EPL), revocar todos los certificados digitales asociados al sistema, y documentar el proceso completo en el expediente del sistema.

---

*Documento generado como referencia técnica para la implementación de marcos de ciberseguridad en entornos de ciberdefensa. Versión 1.0 — 2026.*