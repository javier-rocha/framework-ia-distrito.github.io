# 4. Desarrollo de la Propuesta y Análisis de Resultados

Este capítulo presenta la propuesta de Framework de Gobernanza de IA
desarrollada para las entidades públicas del Distrito Capital de Bogotá,
junto con los resultados de su proceso de validación. Se estructura en
dos grandes secciones: la primera expone en detalle la arquitectura del
framework y su caja de herramientas operativa (toolkit); la segunda
presenta el análisis de los resultados obtenidos mediante la validación
con expertos y la ejecución de pilotos controlados.
 
## Tabla de Contenido
 
- **[4.1 Arquitectura del Framework de Gobernanza de IA](#41-arquitectura-del-framework-de-gobernanza-de-ia)**
  - **[4.1.1 Capa 1: Carta de IA Responsable y Política de Uso de IA](#411-capa-1-carta-de-ia-responsable-y-política-de-uso-de-ia)**
    - [4.1.1.1 Política de Gobierno de Datos](#4111-política-de-gobierno-de-datos)
    - [4.1.1.2 Política de Gestión de Riesgos de IA](#4112-política-de-gestión-de-riesgos-de-ia)
    - [4.1.1.3 Política de Compras y Proveedores de IA](#4113-política-de-compras-y-proveedores-de-ia)
  - **[4.1.2 Capa 2: Modelo de Gobierno](#412-capa-2-modelo-de-gobierno)**
    - [4.1.2.1 Comité de IA Distrital o por Entidad](#4121-comité-de-ia-distrital-o-por-entidad)
    - [4.1.2.2 Roles a Nivel de Caso de Uso](#4122-roles-a-nivel-de-caso-de-uso)
    - [4.1.2.3 Matriz de Responsabilidades (RACI)](#4123-matriz-de-responsabilidades-raci)
    - [4.1.2.4 Instrumentos Operativos de Gobernanza](#4124-instrumentos-operativos-de-gobernanza)
    - [4.1.2.5 Alineación con CONPES 4144 y Vigilancia de Cumplimiento](#4125-alineación-con-conpes-4144-y-vigilancia-de-cumplimiento)
  - **[4.1.3 Capa 3: Fases del Framework de Gobernanza de IA](#413-capa-3-fases-del-framework-de-gobernanza-de-ia)**
  - **[4.1.4 Capa 4: Controles Clave](#414-capa-4-controles-clave)**
  - **[4.1.5 Capa 5: Métricas y KPIs](#415-capa-5-métricas-y-kpis)**
  - **[4.1.6 Modelo de Madurez Institucional](#416-modelo-de-madurez-institucional)**
- **[4.2 Caja de Herramientas Operativa (Toolkit)](#42-caja-de-herramientas-operativa-toolkit)**
  - **[4.2.1 AI Use-Case Canvas](#421-ai-use-case-canvas)**
  - **[4.2.2 Matriz de Riesgos de IA](#422-matriz-de-riesgos-de-ia)**
  - **[4.2.3 Plantilla ARA / DPIA](#423-plantilla-ara--dpia)**
  - **[4.2.4 Model Card](#424-model-card)**
  - **[4.2.5 Data Sheet](#425-data-sheet)**
  - **[4.2.6 Checklist de Evaluación de Proveedores de IA](#426-checklist-de-evaluación-de-proveedores-de-ia)**
  - **[4.2.7 Guía de Uso Interno de IA Generativa](#427-guía-de-uso-interno-de-ia-generativa)**

## 4.1 Arquitectura del Framework de Gobernanza de IA

El framework propuesto constituye un sistema integrado de gobernanza
estructurado en cinco capas interoperables que traducen los principios
del CONPES 4144 y los marcos internacionales en instrumentos operativos
adaptados al contexto institucional del Distrito Capital de Bogotá. Esta
arquitectura responde directamente a las tres limitaciones identificadas
en el estado del arte: falta de adaptación contextual, fragmentación
implementativa y déficit de validación empírica.

En el Anexo B se ilustra la arquitectura general del framework,
mostrando las secciones de cada una de sus cinco capas y su alineación
con el CONPES 4144..
 
### 4.1.1 Capa 1: Carta de IA Responsable y Política de Uso de IA

La Carta de IA Responsable constituye el documento declarativo que
establece el compromiso institucional del Distrito con una
implementación ética de sistemas de inteligencia artificial. Este
documento se fundamenta en estándares internacionales de la UNESCO
(2021) y OCDE (2024), adaptados específicamente al marco normativo
colombiano mediante su articulación con la Constitución Política, la Ley
1581 de 2012 y el CONPES 4144.

Este marco normativo se complementa con la Ley 2279 de 2022 de
Transformación Digital, que establece las bases para la modernización
del Estado mediante tecnologías emergentes, habilitando jurídicamente la
adopción de sistemas automatizados en servicios públicos.
Adicionalmente, el framework incorpora flexibilidad para integrar las
disposiciones de la futura Ley de Inteligencia Artificial actualmente en
trámite legislativo, asegurando adaptabilidad normativa prospectiva.

Los principios fundamentales establecidos son:

**Respeto por los derechos humanos y dignidad.** Todo sistema de IA
implementado en servicios públicos distritales debe respetar los
derechos fundamentales consagrados en la Constitución, con especial
énfasis en el derecho a la igualdad (Art. 13), el habeas data o
protección de datos personales (Art. 15), el debido proceso (Art. 29) y
el acceso a servicios públicos (Art. 365). Este principio se materializa
mediante evaluaciones obligatorias de impacto antes del despliegue de
sistemas que afecten decisiones sobre ciudadanos.

**Transparencia y explicabilidad.** Las entidades distritales deberán
implementar mecanismos de comunicación proactiva que informen a la
ciudadanía cuando estén interactuando con sistemas de inteligencia
artificial. Esta comunicación deberá incluir explicaciones claras y
comprensibles sobre el propósito, funcionamiento y criterios de decisión
de estos sistemas.

Para sistemas de alto riesgo, se requiere documentación técnica
accesible mediante Model Cards y Data Sheets, junto con mecanismos de
explicación adaptados a cada perfil de usuario: ciudadanos recibirán
información simplificada, funcionarios contarán con datos técnicos para
supervisión, y auditores dispondrán de documentación completa para
verificación del cumplimiento normativo.

**Rendición de cuentas y supervisión humana.** Se establece el principio
de que los sistemas de IA complementarán pero no reemplazarán el
criterio humano en decisiones que afecten derechos fundamentales o
servicios esenciales. Cada sistema deberá incorporar mecanismos de
supervisión humana efectiva que permitan la intervención, modificación o
revocación de decisiones algorítmicas cuando sea necesario.

Para garantizar esta supervisión, se designarán responsables específicos
para cada implementación de IA, estableciendo una cadena clara de
responsabilidades que incluye al sponsor del área usuaria, el
responsable técnico y el Comité de IA correspondiente. Esta estructura
asegura la debida rendición de cuentas y mantiene el control
institucional sobre los sistemas automatizados.

**Equidad y no discriminación.** Los sistemas de IA implementados en el
Distrito deberán garantizar la ausencia de sesgos discriminatorios
basados en categorías protegidas por la normativa colombiana, incluyendo
raza, género, orientación sexual, discapacidad y condición
socioeconómica. Este compromiso se materializa mediante la aplicación de
pruebas obligatorias de equidad en todas las fases del ciclo de vida de
los sistemas.

La implementación incluye la definición de umbrales máximos de
disparidad específicos para cada tipo de servicio, asegurando que los
sistemas no repliquen o amplifiquen patrones de discriminación
existentes. Este enfoque preventivo garantiza que la IA promueva la
igualdad de trato en la prestación de servicios distritales.

**Seguridad y robustez.** Los sistemas de IA implementados en el
Distrito deberán garantizar niveles adecuados de seguridad y resistencia
técnica ante fallos operativos y amenazas cibernéticas. Para ello, se
implementarán controles de seguridad basados en el marco del NIST
Cybersecurity Framework, adaptados a las particularidades de los
sistemas de inteligencia artificial.

Como parte integral del proceso de validación, se realizarán pruebas de
robustez que incluirán escenarios de estrés operativo, evaluación con
datos atípicos y simulaciones de intentos de manipulación. Estas
verificaciones asegurarán que los sistemas mantengan su funcionalidad y
confiabilidad incluso en condiciones adversas, protegiendo la integridad
de los servicios distritales.

**Privacidad por diseño y por defecto.** La protección de datos
personales se integrará desde la fase inicial de diseño de todos los
sistemas de IA, aplicando configuraciones predeterminadas que maximicen
la privacidad de los ciudadanos. Este enfoque garantiza el cumplimiento
de la Ley 1581 de 2012 y la Circular Externa 002 de 2024 de la SIC
mediante la implementación sistemática de medidas técnicas y
organizativas.

La implementación incluirá técnicas de minimización de datos,
seudonimización y anonimización, junto con controles de acceso basados
en el principio de privilegio mínimo. Estas medidas asegurarán que el
tratamiento de información personal se realice dentro de los marcos
legales establecidos, priorizando la protección de los derechos de los
titulares en todas las operaciones con sistemas de IA.

La Política de Uso de IA complementa estos principios con directrices
operativas específicas para diferentes tipos de casos de uso,
estableciendo requisitos diferenciados según el nivel de riesgo y el
dominio de aplicación (atención ciudadana, trámites administrativos,
analítica para políticas públicas, gestión de recursos, salud pública,
movilidad).
 
#### 4.1.1.1 Política de Gobierno de Datos
 
La Política de Gobierno de Datos establece los estándares y
procedimientos para garantizar la calidad, integridad y gestión adecuada
de los datos utilizados en sistemas de inteligencia artificial del
Distrito. Reconociendo que los datos constituyen el fundamento crítico
para el éxito y la confiabilidad de estas tecnologías, esta política
regula todo el ciclo de vida de la información, desde su obtención hasta
su disposición final.

La implementación de esta política asegura que los datos cumplan con
requisitos de representatividad, exactitud y actualidad, mitigando
riesgos asociados a sesgos y errores. Este marco permite a las entidades
distritales contar con información confiable para la toma de decisiones
automatizadas, manteniendo el cumplimiento de la normativa vigente en
protección de datos personales.

La Figura 2 sintetiza los componentes fundamentales de la Política de
Gobierno de Datos propuesta, incluyendo estándares de calidad y
representatividad, principios de minimización y propósito específico,
mecanismos de gestión de sesgos y discriminación, la obligatoriedad de
evaluaciones de impacto en privacidad (ARA/DPIA), garantías para el
ejercicio de los derechos de los titulares y criterios de localización y
soberanía de datos.

Los componentes principales incluyen:

**Calidad y representatividad de datos.** Se establecen estándares
mínimos de calidad que garantizan completitud, precisión, consistencia,
actualidad y validez de los datos. Para casos sensibles, se requiere
análisis estadístico de representatividad demográfica y documentación de
limitaciones mediante Data Sheets, asegurando que los datos reflejen
adecuadamente la diversidad poblacional de Bogotá.

**Minimización y propósito específico.** En cumplimiento de la Ley 1581,
se recolectarán únicamente los datos estrictamente necesarios para el
propósito declarado, evitando acumulación innecesaria. Se prohíbe el uso
de datos para fines incompatibles sin la debida autorización legal.

**Gestión de sesgos y discriminación.** Se implementa evaluación
sistemática de sesgos en datos fuente, con documentación obligatoria de
sesgos identificados y aplicación de técnicas de mitigación cuando sea
viable. Se reconoce que no todos los sesgos son eliminables,
requiriéndose transparencia sobre limitaciones residuales.

**Evaluaciones de impacto en privacidad.** Siguiendo las directrices de
la SIC Circular Externa 002/2024, se establece la obligatoriedad de
realizar Análisis de Riesgos y Gestión (ARA) o Data Protection Impact
Assessments (DPIA) para todo sistema de IA que procese datos personales,
con especial profundidad para datos sensibles o tratamientos de alto
riesgo utilizando la plantilla DPIA del toolkit (sección 4.2.3).

**Derechos de los titulares.** Se establecen mecanismos para garantizar
el ejercicio efectivo de los derechos de habeas data (conocer,
actualizar, rectificar, suprimir, revocar) en el contexto de sistemas de
IA. Para sistemas con capacidades de aprendizaje continuo, se documentan
las implicaciones técnicas del derecho al olvido y se implementan
procesos de \"desaprendizaje\" cuando sea técnicamente viable.

**Localización y soberanía de datos.** Para datos sensibles o críticos,
se establecen requisitos de localización en infraestructura nacional o
con garantías contractuales estrictas de jurisdicción y protección
legal. En casos de transferencia internacional de datos, se exige el
cumplimiento de los requisitos del Capítulo IV del Decreto 1377 de 2013
y cláusulas contractuales estándar que garanticen un nivel de protección
adecuado.

#### Política de Gestión de Riesgos de IA
 
Esta política establece un marco integral para la identificación,
evaluación y gestión de riesgos asociados a los sistemas de IA en el
Distrito, integrando estándares internacionales (NIST AI RMF 2023,
ISO/IEC 23894) con el enfoque de clasificación por niveles del AI Act,
adaptado al contexto regulatorio colombiano.

Sistema de clasificación de riesgos: Adoptando el enfoque basado en
riesgo del AI Act, se establece una taxonomía de cuatro niveles:

**Riesgo Inaceptable (Prohibido).** Categoría que incluye sistemas que
vulneran derechos fundamentales o principios constitucionales. En el
ámbito distrital, comprende: sistemas de puntuación social ciudadana,
manipulación subliminal, causante de daño, explotación de
vulnerabilidades de grupos específicos, biometría remota en tiempo real
para vigilancia masiva sin orden judicial.

**Alto Riesgo.** Sistemas con impacto significativo en derechos
fundamentales, seguridad o acceso a servicios esenciales, que requieren
obligaciones reforzadas de evaluación, documentación y auditoría.
Incluye: evaluación y priorización de beneficiarios de programas
sociales, asistencia en decisiones judiciales o administrativas,
sistemas biométricos de identificación, gestión de infraestructura
crítica (movilidad, servicios públicos), evaluación de elegibilidad para
servicios de salud o educación.

**Riesgo Limitado.** Sistemas con requisitos de transparencia básicos,
como chatbots de atención ciudadana, recomendación de información
pública y asistentes virtuales para trámites no sensibles. La obligación
principal es la divulgación clara de la interacción con IA.

**Riesgo Mínimo.** Sistemas sin impacto significativo en derechos o
servicios esenciales, como filtros de spam, optimización de rutas
internas y herramientas de productividad. Aplican principios generales
sin evaluaciones formales obligatorias.

Este enfoque proporcional permite una implementación eficiente de
controles, focalizando recursos en los sistemas de mayor impacto y
riesgo.

Metodología de evaluación de riesgos: Basada en el marco del NIST AI
RMF, esta política establece un proceso estructurado en cuatro fases
para la gestión integral de riesgos en sistemas de IA:

**Identificación de riesgos.** Identificación y análisis sistemático que
considera el contexto de uso, actores afectados, datos utilizados y tipo
de decisiones, identificando riesgos potenciales en categorías clave
como sesgos, privacidad, seguridad, explicabilidad y robustez técnica.

**Medición de riesgos.** Evaluación cuantitativa y cualitativa de
probabilidad e impacto mediante matrices estandarizadas, considerando
dimensiones críticas como afectación a derechos fundamentales, equidad,
continuidad del servicio, seguridad y reputación institucional.

**Gestión de riesgos.** Selección y aplicación de medidas proporcionales
al nivel de riesgo identificado, que incluyen prevención, detección,
mitigación, transferencia o aceptación de riesgos, documentadas en
planes de mitigación específicos.

**Gobernanza de riesgos.** Asignación clara de responsabilidades,
procesos de escalamiento, y mecanismos de monitoreo continuo con
revisiones periódicas y activación de protocolos de respuesta ante
materialización de riesgos.
 
#### Política de Compras y Proveedores de IA
 
Ante la dependencia identificada del Distrito de proveedores externos
para soluciones de inteligencia artificial (identificada en el
diagnóstico de la Fase 1), esta política establece requisitos de debida
diligencia y cláusulas contractuales mínimas para mitigar riesgos
asociados a la cadena de suministro tecnológica.

El objetivo es mitigar los riesgos asociados a la cadena de suministro
tecnológica mediante la estandarización de procesos de selección y
contratación, asegurando que los proveedores cumplan con los estándares
éticos, técnicos y normativos del Distrito.

Los requisitos de conformidad regulatoria establecen que los proveedores
deben demostrar cumplimiento con: el marco regulatorio colombiano
aplicable (Ley 1581/2012, normativa SIC, CONPES 4144); para sistemas de
alto riesgo, la conformidad con obligaciones equivalentes a las del AI
Act o compromiso de certificación dentro de plazos razonables; las
políticas públicas de IA responsable y transparencia, preferiblemente
con informes anuales verificables; y un Sistema de Gestión de IA (AIMS)
según ISO/IEC 42001 implementado o en vías de certificación, con
evidencia documentada.

En cuanto a los requisitos de documentación técnica, los proveedores
deberán entregar documentación técnica completa que garantice la
transparencia y auditabilidad de los sistemas de IA. Esta incluye: Model
Cards describiendo arquitectura, propósito, datos de entrenamiento,
métricas de desempeño, limitaciones conocidas y casos de uso
apropiados/inapropiados; Data Sheets para todos los conjuntos de datos
utilizados, documentando metodología de recolección, composición
demográfica, procesos de limpieza y limitaciones; documentación técnica
detallada para auditoría (arquitectura, hiperparámetros, proceso de
entrenamiento, resultados de pruebas de robustez y equidad); y bitácoras
de decisiones de diseño y gestión de sesgos. Esta documentación
permitirá al Distrito verificar la calidad técnica, comprender las
limitaciones operativas y mantener la trazabilidad necesaria para la
auditoría continua de los sistemas implementados.

Los requisitos de privacidad y seguridad incluyen: claridad sobre la
titularidad de datos (distinguiendo datos de entrenamiento, operación y
metadatos generados); especificación de localización física y
jurisdiccional de datos; políticas de retención, borrado y portabilidad
de datos con compromisos contractuales exigibles; Data Processing
Agreements (DPA) para tratamiento de datos personales, estableciendo
roles de responsable y encargado según Ley 1581 de 2012; certificaciones
de seguridad relevantes (ISO 27001, SOC 2) y resultados de pruebas de
robustez y pentesting; y compromiso de notificación de incidentes de
seguridad dentro de plazos definidos. Estos requisitos aseguran que los
proveedores manejen los datos del Distrito con los más altos estándares
de seguridad y en estricto cumplimiento de la normativa colombiana de
protección de datos personales.

Los requisitos de auditoría y mejora continua establecen que los
contratos con proveedores de sistemas de IA incorporarán cláusulas
específicas que garanticen la supervisión continua y la evolución
controlada de las soluciones implementadas. Estas incorporan: cláusulas
de derecho a auditoría, permitiendo evaluaciones independientes con
acceso a documentación, código (cuando sea viable), y evidencias de
pruebas; implementación de sistemas de telemetría para detectar
desviaciones en el comportamiento de los modelos (drift), degradación de
desempeño y sesgos emergentes; Acuerdos de Niveles de Servicio (Service
Level Agreements) con compromisos de disponibilidad, tiempo de
respuesta, y calidad del servicio; y un roadmap de producto, gestión de
versiones y control de cambios con procesos de notificación y evaluación
de impacto de actualizaciones. Estos requisitos permiten al Distrito
mantener supervisión efectiva sobre los sistemas de IA a lo largo de su
ciclo de vida, asegurando que evolucionen de manera controlada y
mantengan los estándares de calidad y ética establecidos.

El Checklist de Evaluación de Proveedores del toolkit (sección 4.2.5)
operacionaliza estos requisitos en un instrumento práctico para procesos
de selección y contratación.
 
### 4.1.2 Capa 2: Modelo de Gobierno
 
Esta capa establece la estructura organizacional y los mecanismos de
decisión para implementar la gobernanza de IA en el Distrito Capital,
reconociendo las diferentes capacidades institucionales. El modelo
ofrece dos modalidades prácticas: un Comité Distrital centralizado para
entidades con menor madurez técnica, y Comités por entidad para
organizaciones con mayor capacidad y volumen de casos de uso.

El diseño incorpora mecanismos claros de toma de decisiones y se integra
con los sistemas de gestión existentes, incluyendo el MIPG y el control
interno, asegurando que la gobernanza de IA se implemente de manera
articulada con la operación institucional. La composición de los comités
refleja roles realistas y representativos, facilitando la implementación
efectiva del Framework en toda la administración distrital.

#### 4.1.2.1 Comité de IA Distrital o por Entidad
 
El Comité de IA se establece como la máxima instancia de gobernanza para
la inteligencia artificial en el Distrito Capital, responsable de la
dirección estratégica, supervisión y coordinación de todas las
iniciativas en esta materia. Como órgano colegiado de carácter
multidisciplinario, integra las perspectivas técnicas, jurídicas, éticas
y operativas necesarias para una toma de decisiones balanceada y
fundamentada. Su diseño operativo incorpora mecanismos claros de toma de
decisiones y se articula con los sistemas de gestión existentes,
incluyendo el MIPG y el control interno, asegurando que la gobernanza de
IA se implemente de manera coherente con la estructura institucional del
Distrito. La composición del comité refleja roles realistas y
representativos, facilitando la implementación efectiva del Framework en
toda la administración distrital.

La composición y roles del Comité se estructuran de la siguiente manera:
la Alta Dirección (Presidente del Comité) corresponde a un Secretario,
Director o nivel directivo equivalente que aporta patrocinio
institucional, alineación estratégica con objetivos de la entidad y
capacidad de decisión sobre recursos y prioridades. El Oficial de IA
Responsable (Secretaría Técnica) es un rol dedicado responsable de la
coordinación operativa del comité, seguimiento de casos de uso, gestión
de riesgos corporativos de IA y enlace con la Alta Dirección, pudiendo
ser desempeñado por el responsable de transformación digital, innovación
o calidad según la estructura organizacional. El Representante de
Tecnologías de Información (TIC) y Seguridad aporta perspectiva técnica
sobre arquitectura, desarrollo, operación, ciberseguridad y viabilidad
de implementación, siendo responsable de evaluar requisitos técnicos y
garantizar la robustez de los sistemas. El Data Protection Officer (DPO)
o Responsable de Habeas Data asegura el cumplimiento de la Ley 1581 y
normativa SIC, evalúa ARA/DPIA, supervisa derechos de los titulares y
gestiona riesgos de privacidad, contando con voto vinculante en
decisiones que afecten datos personales. El Representante Jurídico
evalúa bases legales para tratamiento de datos, conformidad regulatoria,
viabilidad de contratos con proveedores y gestión de riesgos legales,
siendo responsable de la revisión de cláusulas contractuales y términos
de servicio. El Representante de Planeación asegura la alineación con el
plan estratégico institucional, evalúa viabilidad presupuestal, coordina
con otros proyectos de transformación y vela por la sostenibilidad de
iniciativas. El Representante de Control Interno aporta perspectiva de
gestión de riesgos institucionales, evalúa controles y mecanismos de
auditoría, y vela por la coherencia con sistemas de gestión de calidad y
control interno existentes. El Representante de Atención al Ciudadano o
Área de Negocio aporta comprensión profunda del contexto de uso,
necesidades de usuarios finales, viabilidad operativa y calidad del
servicio, asegurando que las soluciones respondan a problemáticas reales
y sean apropiadas para el perfil de los ciudadanos beneficiarios.

Las funciones del Comité incluyen: aprobar o rechazar la implementación
de casos de uso de IA basándose en la evaluación de riesgos, conformidad
normativa y alineación estratégica; supervisar el portafolio de
iniciativas de IA, priorizando según impacto, riesgo y recursos
disponibles; establecer y actualizar políticas institucionales de IA
alineadas con el framework distrital; revisar y aprobar ARA/DPIA para
casos de alto riesgo; monitorear KPIs agregados y gestionar incidentes
significativos; aprobar contratos con proveedores de IA y renovaciones
basándose en evaluación de desempeño; coordinar capacitación y gestión
del cambio organizacional; supervisar la implementación del programa
obligatorio de capacitación en IA Generativa**;** y mantener enlace con
instancias distritales superiores (para Comités por entidad) o con otras
entidades (para Comité Distrital centralizado).

Respecto a las modalidades de implementación, se contemplan dos
opciones. El Comité de IA Distrital (centralizado) es recomendado para
la fase inicial de implementación o para entidades de menor tamaño y
madurez, donde un único Comité a nivel del Distrito brinda servicios de
gobernanza a múltiples entidades, asegurando consistencia de criterios,
compartiendo costos de expertise especializada y facilitando el
aprendizaje inter-institucional, requiriendo la designación de un equipo
técnico de soporte con capacidad para atender múltiples entidades. Los
Comités por Entidad son recomendados para entidades de gran tamaño, alta
complejidad o con volumen significativo de casos de uso (más de 5
sistemas en operación o planificación), permitiendo mayor agilidad en la
toma de decisiones, especialización en el contexto específico de la
entidad y apropiación institucional más profunda, requiriendo
coordinación con el nivel distrital para consistencia normativa y
compartición de lecciones aprendidas.

#### 4.1.2.2 Roles a Nivel de Caso de Uso
 
Complementando la estructura de gobernanza corporativa, se definen roles
operativos específicos para cada iniciativa o sistema de IA.

**El Sponsor de Negocio (Product Owner)** es el líder del área usuaria
que impulsa la iniciativa de IA, definiendo su propósito estratégico y
requisitos funcionales. Como responsable último de los resultados,
asegura la alineación con los objetivos institucionales, gestiona el
cambio organizacional y garantiza la apropiación del sistema en su área,
rindiendo cuentas sobre su impacto operativo.

**El Responsable Técnico (Technical Lead)** lidera el desarrollo o
implementación técnica, asegura la calidad del sistema, supervisa
pruebas, coordina con proveedores externos y es responsable del
monitoreo técnico continuo. Este rol debe tener conocimientos sólidos en
IA/ML y comprensión de los principios de IA responsable.

**El Propietario de Datos (Data Steward)** gestiona integralmente el
ciclo de vida de los datos utilizados por el sistema, garantizando su
calidad, disponibilidad y gobierno. En coordinación con el Oficial de
Datos Personales y el área técnica, vela por el cumplimiento normativo
de privacidad y la correcta gestión de los datos desde su obtención
hasta su disposición final.

**Los Usuarios Finales y Representantes de Ciudadanía** participan
activamente en el diseño, validación y mejora continua del sistema,
aportando perspectivas basadas en la experiencia real de uso. En casos
de alto riesgo, su participación se formaliza mediante grupos focales
que aseguran que las voces de las comunidades afectadas sean
consideradas.

La matriz RACI (Responsible, Accountable, Consulted, Informed) del
toolkit especifica las responsabilidades detalladas para cada rol en las
diferentes fases del ciclo de vida.
 
#### 4.1.2.3 Matriz de Responsabilidades (RACI)
 
Para garantizar claridad en la ejecución del framework, se establece la
siguiente matriz RACI que define roles por fase del ciclo de vida:
 
**Tabla 3. Capa 2: Matriz de Responsabilidad (RACI)**
 
| Fase del Ciclo de Vida | Comité de IA | DPO | Responsable Técnico | Sponsor de Negocio | Área Jurídica |
| :--- | :---: | :---: | :---: | :---: | :---: |
| Intake y Canvas | C | C | R | A | C |
| Clasificación de Riesgo | A | C | R | I | C |
| ARA/DPIA | A | A (voto vinculante) | C | C | C |
| Gobierno de Datos | C | A | R | C | I |
| Desarrollo/Adquisición | C | C | A | C | A (contratos) |
| Pruebas y Validación | C | C | A | C | I |
| Despliegue | A (go-live) | C | R | C | I |
| Monitoreo y Auditoría | A | C | R | I | C |
| Retiro | A (datos) | R | C | C | A |

Fuente: Elaboración Propia

El DPO ejerce veto vinculante en fases que involucren tratamiento de
datos personales (ARA/DPIA, Gobierno de Datos, Retiro). El Comité de IA
actúa como gate decisorio en todas las fases críticas, mientras que la
Alta Dirección retiene autoridad final para sistemas de alto riesgo o
inversiones significativas.

#### 4.1.2.4 Instrumentos Operativos de Gobernanza
 
Para facilitar la coordinación, trazabilidad y eficiencia en la gestión
del portafolio de IA, se establecen dos instrumentos operativos
obligatorios:

**Registro Central de Casos de Uso de IA**

Sistema centralizado que documenta todos los casos de uso en operación,
desarrollo o evaluación. Estructura mínima de datos: ID único, nombre
del sistema, entidad responsable, clasificación de riesgo, estado del
ciclo de vida, fecha de inicio, responsables (técnico, sponsor, DPO),
descripción breve, datos personales tratados (Sí/No/Sensibles), fecha de
última actualización. Actualización obligatoria: mensual para sistemas
en operación, semanal para sistemas en desarrollo. Acceso: consulta
pública (datos no sensibles) para transparencia ciudadana; acceso
completo para Comité de IA, control interno y auditoría. Responsable:
Oficial de IA Responsable (Secretaría Técnica del Comité).

**Catálogo Distrital de Proveedores Pre-evaluados**

Listado de proveedores que han superado evaluación previa mediante el
Checklist de Evaluación (sección 4.2.6), clasificados por nivel de
riesgo y tipo de solución. Criterios de inclusión: aprobación ≥75% en
checklist estándar, cumplimiento obligatorio de Ley 1581 y Ley 2279,
certificaciones de seguridad vigentes, referencias verificables en
sector público. Beneficios: reducción de 40-60% en tiempo de evaluación
para licitaciones, estandarización de cláusulas contractuales, mayor
poder de negociación institucional. Actualización: anual con revisión
semestral de certificaciones. Responsable: Comité de IA con soporte del
área de Contratación.

Estos instrumentos se integran al dashboard de gobernanza (Anexo C)
mediante indicadores de cobertura de registro (objetivo: 100%) y uso del
catálogo en procesos de contratación (objetivo: ≥70% para sistemas de
alto riesgo)
 
#### 4.1.2.5 Alineación con CONPES 4144 y Vigilancia de Cumplimiento
 
El modelo de gobierno establece mecanismos específicos de trazabilidad y
reporte que garantizan la alineación estratégica con los cinco ejes del
CONPES 4144, integrando la gobernanza de IA con los sistemas de gestión
existentes en el Distrito.

El Eje de Ética y Gobernanza establece que el Comité de IA supervisa la
implementación de la Carta de IA Responsable y reporta trimestralmente
el estado del portafolio, incidentes éticos y lecciones aprendidas,
integrando estos indicadores al Sistema de Seguimiento a Metas del MIPG.

En el Eje de Datos e Infraestructura, el DPO y el área TIC reportan
trimestralmente sobre la madurez de la gobernanza de datos, calidad de
conjuntos de datos utilizados y estado de la infraestructura
tecnológica, información que se incorpora a los indicadores de gestión
del MIPG.

El Eje de Gestión de Riesgos mantiene un registro corporativo de riesgos
de IA actualizado trimestralmente, el cual se articula con la matriz de
riesgos del sistema de control interno, reportando riesgos
materializados, efectividad de controles y necesidades de mejora.

Respecto al Eje de Talento, el área de Gestión Humana reporta
semestralmente los avances del programa de capacitación en IA
responsable, cobertura de formación y desarrollo de capacidades
internas, integrando estas métricas al plan de desarrollo del talento
humano.

En el Eje de Uso y Adopción, se cuantifica y reporta trimestralmente el
avance en adopción mediante indicadores de casos de uso por fase del
ciclo de vida, servicios transformados, beneficiarios impactados y
resultados en eficiencia y calidad del servicio.

Para la vigilancia de cumplimiento regulatorio, el Comité establece un
calendario de revisiones que incluye: cumplimiento de Ley 1581 y
normativa SIC, con revisión mensual de ARA/DPIA vigentes, atención de
derechos de habeas data, y respuesta a requerimientos de la autoridad de
protección de datos; la conformidad con políticas de gobierno digital y
transparencia, mediante la publicación de inventario de sistemas de IA
(cuando aplique según normativa de datos abiertos), divulgaciones
ciudadanas requeridas, y rendición de cuentas; y el seguimiento al plan
de acción derivado del CONPES 4144 a nivel institucional, con reporte
anual de avances al nivel distrital correspondiente.

Esta estructura asegura que la implementación del Framework de IA
mantenga coherencia total con la política nacional, mientras se integra
eficientemente con los sistemas de gestión y control ya establecidos en
la administración distrital.
 
### 4.1.3 Capa 3: Fases del Framework de Gobernanza de IA
 
El modelo propuesto se organiza en nueve etapas sucesivas que pretenden
garantizar una adopción responsable y estructurada de sistemas de
inteligencia artificial. Cada fase incorpora controles progresivos que
reducen los riesgos desde la concepción del proyecto hasta su retiro
definitivo.

La Figura 3 presenta el Proceso de Ciclo de Vida de Gobernanza de IA,
estructurado como un diagrama de flujo que integra las fases
secuenciales, los puntos de control (gates) y los entregables
obligatorios en cada etapa. Este modelo permite visualizar de forma
clara cómo la gobernanza se articula desde la concepción del caso de
uso, pasando por la evaluación de riesgos y la validación técnica, hasta
la puesta en producción, seguimiento y auditoría continua. Asimismo,
evidencia la estructura de toma de decisiones y los hitos de revisión
que garantizan trazabilidad, transparencia y control institucional en
todo el ciclo de vida de los sistemas de IA, alineándose con la
arquitectura de cinco capas del Framework propuesto.

#### Fase 1 -- Intake y AI Use‑Case Canvas
 
En la fase inicial se formaliza la idea del caso de uso mediante
el *AI Use‑Case Canvas* (disponible en el toolkit, sección 4.2.1). El
sponsor de negocio completa la plantilla describiendo el problema, los
objetivos, los actores involucrados, los datos requeridos, los
resultados esperados y las métricas de éxito. Simultáneamente, el
responsable técnico, el oficial de protección de datos (DPO) y el área
de planeación realizan una primera valoración de viabilidad técnica,
legal y presupuestal, al tiempo que identifican riesgos y partes
interesadas.

El Comité de IA actúa como *gate* de revisión (G1). Sus criterios
--alineación estratégica, viabilidad preliminar, claridad del propósito
y disponibilidad de recursos-- determinan si el caso avanza a la
clasificación de riesgo. El entregable de esta fase es
el *AI Use‑Case Canvas* aprobado.

#### Fase 2 -- Clasificación de Riesgo
 
Esta etapa asigna un nivel de riesgo (inaceptable, alto, limitado o
mínimo) siguiendo la taxonomía del AI Act. La matriz de clasificación
evalúa propósito del sistema, tipo de decisiones, datos procesados,
población afectada, reversibilidad y consecuencias de errores. Cuando el
caso se ubica en la categoría prohibida (riesgo inaceptable), el proceso
se detiene; para los de alto riesgo se activan obligaciones reforzadas
(ARA/DPIA obligatorio, documentación técnica ampliada, supervisión
humana y auditoría).

El Comité de IA revisa y valida la clasificación (G2). El resultado se
plasma en la *Ficha de Clasificación de Riesgo*, que constituye el
documento de referencia para las fases posteriores.

#### Fase 3 -- ARA/DPIA (alto riesgo o datos sensibles)
 
El objetivo es identificar y mitigar impactos sobre derechos
fundamentales y la privacidad antes de la puesta en marcha. Se completa
la *Plantilla ARA/DPIA* (toolkit, sección 4.2.3), que incluye:
descripción del sistema, mapeo de flujos de datos, bases legales de
tratamiento, evaluación de impactos en privacidad, no discriminación,
debido proceso y acceso equitativo; análisis de riesgos mediante
la *Matriz de Riesgos* (sección 4.2.2); y propuestas de medidas técnicas
y organizativas (minimización, seudonimización, cifrado, auditoría,
supervisión humana).

El DPO, como voto decisivo dentro del Comité de IA, aprueba o rechaza el
documento (G3). Cuando la aprobación está condicionada, se establecen
mitigaciones específicas que deben incorporarse antes de avanzar. El
entregable es el ARA/DPIA aprobado con su plan de mitigación.

#### Fase 4 -- Gobierno de Datos
 
En esta fase se asegura que los datos que alimentarán el modelo sean de
alta calidad, representativos y gestionados éticamente. Las actividades
comprenden: inventario y documentación de fuentes (internas, externas,
terceros); evaluación de calidad dimensional (completitud, precisión,
consistencia, actualidad) mediante la lista de verificación del toolkit;
análisis de representatividad demográfica y detección de sesgos;
aplicación de técnicas de mitigación (remuestreo, reponderación,
recolección complementaria); y elaboración de *Data Sheets* siguiendo la
plantilla de Gebru et al. (2018).

El propietario de datos y el DPO certifican la calidad y la gobernanza
adecuada (G4). En casos de alto riesgo, se puede requerir auditoría
independiente o validación estadística formal. El resultado son
los *Data Sheets* aprobados y el plan de gobernanza de datos.

#### Fase 5 -- Desarrollo o Adquisición
 
Esta etapa traduce los requisitos de gobernanza, seguridad y calidad en
un producto técnico.

**Desarrollo interno.** Se convierten los requisitos funcionales y no
funcionales (incluidos los de IA responsable) en especificaciones
técnicas; se elige arquitectura, algoritmos y tecnologías que favorezcan
la interpretabilidad sin sacrificar el desempeño crítico; se incorporan
controles de privacidad por diseño (minimización, seudonimización,
control de accesos) y de seguridad (validación de entradas, defensa
contra ataques adversarios, cifrado). Además, se implementa versionado
de código, datos de entrenamiento y modelos para garantizar
trazabilidad, y se mantiene una documentación continua de decisiones de
diseño, hiperparámetros y procesos de entrenamiento.

**Adquisición externa.** Se redactan términos de referencia que integran
el *Checklist de Proveedores* (toolkit, sección 4.2.5); se evalúan
propuestas ponderando criterios técnicos, de conformidad regulatoria y
experiencia del proveedor; y se negocian contratos que incluyan
cláusulas de privacidad (DPA), seguridad, auditoría, SLA y gestión de
cambios. La documentación entregada por el proveedor tales como Model
Cards, Data Sheets (toolkit, sección 4.2.4) y certificaciones sen valida
antes de la firma.

El *gate* de revisión (G5) difiere según la vía elegida: para desarrollo
interno, el comité técnico verifica arquitectura y código; para
adquisición, el área jurídica, el DPO y el Comité de IA aprueban el
contrato y confirman que el sistema satisface el ARA/DPIA aprobado
(toolkit, sección 4.2.3). El entregable es el sistema (con documentación
técnica completa) o el contrato firmado.

#### Fase 6 -- Pruebas y Validación
 
Antes del despliegue, el sistema debe demostrar cumplimiento con
requisitos funcionales, técnicos, éticos y de usabilidad. Las pruebas se
agrupan en cinco categorías.

Las pruebas técnicas evalúan métricas objetivas (precisión, recall, F1,
AUC ROC), utilizan conjuntos de validación independientes y examinan la
robustez frente a datos fuera de distribución, ruido y pequeñas
perturbaciones. Además, se realizan pruebas de seguridad (penetration
testing) y de rendimiento (tiempo de respuesta, uso de recursos,
escalabilidad).

Las pruebas de equidad calculan métricas de fairness (disparate impact,
equal opportunity, predictive parity) y desglosan los resultados por
grupos demográficos relevantes. Cuando aparecen disparidades
inaceptables, se aplican técnicas de mitigación (post processing,
optimización de umbrales) y se documentan los trade offs entre equidad y
desempeño.

Las pruebas de explicabilidad verifican la presencia de mecanismos
explicativos (LIME, SHAP, mapas de atención, contra factuales) y validan
su comprensibilidad mediante pruebas con usuarios finales.

Las pruebas de usabilidad y accesibilidad consisten en la realización de
sesiones con usuarios representativos (funcionarios, ciudadanos)
siguiendo los principios de diseño centrado en el usuario y aseguran el
cumplimiento de WCAG 2.1 nivel AA para personas con discapacidad.

Las pruebas de integración comprueban la interoperabilidad con sistemas
legados, la correcta exposición de APIs y la capacidad de recuperación
ante fallos.

El responsable técnico presenta los resultados al Comité de IA (G6).
Para sistemas de alto riesgo, la aprobación depende de evidencia
documental que demuestre el cumplimiento de umbrales predefinidos en
desempeño, equidad, robustez y seguridad. El entregable es el Informe de
pruebas y validación acompañado de una Model Card completa.

#### Fase 7 -- Despliegue
 
El objetivo es poner el sistema en producción de forma controlada,
garantizando que el personal esté preparado y que los controles
operativos estén activos. Las actividades incluyen: capacitación de
usuarios finales (operadores y, cuando corresponda, ciudadanos) sobre
funcionamiento, limitaciones y procedimientos de supervisión humana;
configuración de logs de auditoría, telemetría, alertas y dashboards de
monitoreo; despliegue gradual (piloto limitado seguido de escalamiento
progresivo); establecimiento de canales de reporte de incidentes y
quejas; y comunicación transparente a la ciudadanía cuando el sistema
interactúe con el público.

El Comité de IA verifica la preparación operativa (G7) y el sponsor de
negocio autoriza el *go‑live*. El entregable es el sistema en producción
con los controles operativos activos y el personal debidamente
capacitado.

#### Fase 8 -- Monitoreo y Auditoría
 
Una vez en funcionamiento, el sistema requiere supervisión continua para
detectar desviaciones y aplicar correcciones. Las actividades se
estructuran en cuatro áreas.

El monitoreo técnico continuo comprende el seguimiento de métricas de
desempeño, la detección de data drift y concept drift, el cálculo
periódico de métricas de equidad y la vigilancia de intentos de ataque.

La gestión de incidentes implica el registro, clasificación y respuesta
a incidentes (técnicos, de privacidad, de equidad, de seguridad o quejas
ciudadanas) siguiendo protocolos de contención, investigación,
remediación y comunicación.

La auditoría periódica consiste en la revisión trimestral (o con mayor
frecuencia según el nivel de riesgo) del cumplimiento de los controles
del ARA/DPIA, la auditoría de logs para validar la supervisión humana y
el análisis de quejas. Los sistemas de alto riesgo requieren una
auditoría anual independiente que evalúe la conformidad técnica, ética y
regulatoria.

La gestión de cambios abarca la evaluación de impacto de actualizaciones
(nuevas versiones del modelo, cambios en datos o código), la
re-ejecución de pruebas críticas y la actualización de la documentación
(Model Cards, Data Sheets).

El Comité de IA revisa trimestralmente el dashboard de KPIs, incidentes
y hallazgos de auditoría (G8) y decide si se mantiene la operación, se
implementan mejoras o se procede al retiro. Los entregables son los
reportes de monitoreo, los registros de incidentes y los informes de
auditoría.
 
#### Fase 9 -- Retiro o Fin de Vida
 
Cuando el sistema deja de ser necesario, viable o conforme, se lleva a
cabo un retiro ordenado que preserve la continuidad del servicio y
garantice una gestión adecuada de los datos. Las actividades incluyen:
decisión de retiro basada en obsolescencia técnica, cambios
regulatorios, riesgos inaceptables, fin del propósito o análisis
costo‑beneficio desfavorable; planificación de la transición (retorno a
procesos manuales o sustitución por otro sistema); gestión de datos
(exportación para fines legales, anonimización o borrado seguro conforme
a la Ley 1581); documentación de lecciones aprendidas y comunicación a
los ciudadanos afectados.

El Comité de IA aprueba el plan de retiro y el DPO verifica el
cumplimiento de la normativa de protección de datos (G9). El entregable
final es el sistema retirado, los datos gestionados conforme a la
normativa y un informe de lecciones aprendidas archivado.

### Capa 4: Controles Clave
 
Esta capa define los controles técnicos y organizacionales necesarios
para implementar de manera transversal los principios éticos y mitigar
riesgos a lo largo del ciclo de vida de los sistemas de inteligencia
artificial. Los controles se estructuran en seis dimensiones
fundamentales.
 
#### 4.1.4.1 Ética y Derechos Fundamentales
 
**Supervisión humana significativa.** En decisiones que afecten derechos
fundamentales o servicios esenciales, se requieren mecanismos que
garanticen una supervisión humana competente. Esta supervisión debe
permitir comprender el funcionamiento y las limitaciones del sistema,
monitorear su operación en tiempo real o revisar
decisiones *ex-post* según la criticidad, intervenir o anular decisiones
algorítmicas cuando sea necesario, y activar protocolos de escalamiento
ante situaciones fuera del diseño original. La supervisión debe ser
genuina---ya sea *human-in-the-loop* u *human-on-the-loop*---y no
meramente ceremonial, lo que exige interfaces adecuadas y capacitación
específica del personal supervisor.

**No discriminación y equidad.** Los controles implementados incluyen
análisis de sesgos en los datos de entrenamiento y la aplicación de
técnicas de mitigación, pruebas de equidad durante el desarrollo y
monitoreo continuo de métricas de *fairness*. Se establecen umbrales
máximos de disparidad según el tipo de servicio; por ejemplo, para
servicios sociales críticos se podría requerir un *disparate impact
ratio* no inferior a 0.8. Además, se incorporan mecanismos de
explicación que permitan detectar discriminación en casos individuales y
procesos de apelación accesibles cuando las decisiones algorítmicas
afecten negativamente a los ciudadanos.

**Acceso equitativo.** El diseño debe ser inclusivo, considerando la
accesibilidad para personas con discapacidad visual, auditiva, motriz o
cognitiva. Es crucial disponer de canales alternativos de atención
humana para quienes no puedan utilizar el sistema de IA, así como
adaptar las interfaces a diversos niveles de alfabetización digital.
Finalmente, se debe evitar condicionar el acceso a servicios esenciales
exclusivamente a sistemas digitales, mitigando así la brecha digital.

#### 4.1.4.2 Privacidad y Protección de Datos
 
**Bases legales claras.** Todo tratamiento de datos personales debe
fundamentarse en una base legal válida conforme a la Ley 1581 de 2012,
como el consentimiento informado, previo y expreso; la ejecución de un
contrato; el cumplimiento de una obligación legal; la protección de
intereses vitales; o el ejercicio de funciones públicas. El Análisis de
Riesgos y Aspectos (ARA) o la Evaluación de Impacto en la Protección de
Datos (DPIA) deben documentar específicamente la base legal aplicable.

**Minimización de datos.** Se aplica el principio de que solo deben
recolectarse y procesarse los datos estrictamente necesarios para el
propósito declarado. Esto implica una evaluación crítica de cada campo
de datos, preferencia por datos agregados o anonimizados cuando sea
posible, evitar la recolección especulativa y realizar revisiones
periódicas para eliminar datos innecesarios.

**Anonimización y seudonimización.** Se emplean técnicas de protección
según la proporcionalidad: la anonimización irreversible para datos
estadísticos y la seudonimización cuando se requiera trazabilidad sin
identificación rutinaria. Es esencial evaluar el riesgo de
re-identificación y reforzar los controles de acceso para las llaves de
des-seudonimización.

**DPIA obligatorio.** Para tratamientos de alto riesgo según la Circular
002/2024 de la Superintendencia de Industria y Comercio (SIC), se
realiza una evaluación sistemática. El ARA/DPIA del framework cumple con
estos requisitos, cubriendo aspectos como la creación de perfiles o el
tratamiento a gran escala de datos sensibles.

**Gestión de consentimiento.** Cuando sea requerido, el consentimiento
debe ser previo, informado, específico e inequívoco. Los mecanismos
deben permitir su retiro con la misma facilidad con que se otorgó,
registrarse de manera auditable y gestionar las consecuencias de su
retirada.

Derechos de los titulares. Se establecen procedimientos operativos para
garantizar los derechos de acceso, rectificación, supresión, oposición y
portabilidad, siempre dentro de los marcos legales aplicables.
 
#### 4.1.4.3 Seguridad y Resiliencia
 
**Robustez técnica.** Los controles aseguran un funcionamiento confiable
mediante el manejo de errores y casos excepcionales, una degradación
graciosa hacia comportamientos seguros, pruebas con datos adversarios y
monitoreo de *drift* en el desempeño.

**Ciberseguridad.** Se implementan protecciones contra amenazas basadas
en mejores prácticas como el NIST CSF o CIS Controls. Esto incluye
defensas contra ataques específicos de *machine
learning* (envenenamiento, evasión, extracción de modelos), validación
robusta de entradas, cifrado de datos y gestión segura de credenciales.

**Autenticación y procedencia de contenido (para GenAI).** Cuando sea
viable técnicamente, se incorporan marcas de agua o firmas digitales
para detectar contenido sintético y mecanismos de procedencia que
permitan rastrear su origen, reconociendo al mismo tiempo las
limitaciones tecnológicas actuales.

**Telemetría y respuesta a incidentes.** Se implementa
un *logging* comprehensivo, sistemas de alerta para eventos críticos y
protocolos de respuesta con roles definidos, incluyendo la notificación
a autoridades y titulares según lo dispuesto por la SIC en caso de
brechas.
 
#### 4.1.4.4 Transparencia y Explicabilidad
 
**Divulgaciones ciudadanas.** Se requiere una transparencia proactiva,
notificando claramente cuando un ciudadano interactúe con un sistema de
IA, informando sobre su propósito, el tipo de decisiones que toma y los
derechos del ciudadano. Para sistemas de alto riesgo, se publica
información adicional en portales institucionales.

**Documentación técnica.** Para garantizar la auditabilidad, se
elaboran *Model Cards* (Mitchell et al., 2019) y *Data Sheets* (Gebru et
al., 2018), documentando el modelo, los datos, la arquitectura y las
decisiones de diseño, incluyendo el manejo de *trade-offs*.

**Trazabilidad.** Se mantiene una capacidad de auditoría mediante
el *logging* de entradas, salidas y versiones, junto con la
implementación de métodos de explicabilidad (SHAP, LIME) adecuados al
modelo y al usuario, balanceando las necesidades de explicabilidad con
el desempeño y la privacidad.

**Inteligibilidad de explicaciones.** Las explicaciones se adaptan al
destinatario: simples y sin jerga para el ciudadano, técnicas para el
operador y completas para el auditor.
 
#### 4.1.4.5 Atención al Ciudadano
 
**Canales de reclamación y apelación.** Se disponen mecanismos
accesibles, gratuitos y con plazos razonables para reportar problemas,
apelar decisiones automatizadas y solicitar revisión humana,
garantizando que las apelaciones sean resueltas por humanos con
capacidad de decisión.

**Integridad del servicio.** Se monitorea la satisfacción ciudadana y se
compara la calidad del servicio con la línea base pre-IA, detectando
exclusiones involuntarias y asegurando alternativas de servicio.

**Accesibilidad universal.** El diseño cumple con los estándares WCAG
2.1 nivel AA, es compatible con tecnologías asistivas y ofrece contenido
comprensible y alternativas para población con baja alfabetización
digital.
 
#### 4.1.4.6 Gestión de Terceros (Proveedores)
 
**Debida diligencia en selección.** Se aplica un checklist que evalúa la
conformidad regulatoria, la madurez en IA responsable, la calidad de la
documentación técnica, las capacidades de seguridad y el soporte para
auditoría.

**Cláusulas contractuales obligatorias.** Los contratos incluyen
Acuerdos de Procesamiento de Datos (DPA), claridad sobre propiedad
intelectual, SLAs cuantificables, gestión de cambios, derecho a
auditoría y cláusulas de continuidad y portabilidad.

**Monitoreo de desempeño de proveedores.** Se evalúa periódicamente el
cumplimiento de los SLAs, se revisan incidentes y se toman decisiones
informadas sobre la renovación o cambio de proveedor basadas en
evidencia.
 
### 4.1.5 Capa 5: Métricas y KPIs
 
La quinta capa del framework establece un sistema integral de métricas e
indicadores clave de desempeño que permite medir, monitorear y demostrar
el cumplimiento normativo, la gestión efectiva de riesgos, la calidad
técnica y el impacto transformador de los sistemas de inteligencia
artificial en el servicio público distrital. Esta capa responde
directamente a la necesidad de medición basada en evidencia planteada
por el CONPES 4144, que señala la necesidad de sistemas robustos de
seguimiento y evaluación para asegurar que las políticas públicas de IA
generen resultados cuantificables y sostenibles. En el contexto
específico de la Secretaría Distrital de Gobierno de Bogotá, cuyo Plan
Estratégico Institucional 2024-2028 establece objetivos ambiciosos de
transformación digital y modernización administrativa, la implementación
de un sistema de medición consistente con los principios del COBIT 2019
se convierte en un elemento diferenciador que permite demostrar el valor
agregado de las inversiones en tecnología y la gobernanza efectiva de
estos sistemas críticos para la administración pública distrital.

#### ​*Marco Conceptual de Medición y Alineación con COBIT 2019*
 
El sistema de métricas propuesto integra tres perspectivas
complementarias de medición derivadas de los marcos internacionales de
referencia, siendo especialmente importante la integración con el modelo
COBIT 2019, que en sus procesos MEA (Monitor, Evaluate and Assess)
establece que la medición de la conformidad y el desempeño de los
procesos de tecnología de la información debe estar vinculada
directamente con los objetivos corporativos y las metas de negocio.
COBIT 2019 enfatiza que la medición no es un fin en sí mismo, sino un
medio para verificar que los procesos de gobierno de TI generan valor y
cumplen con los requisitos de control y conformidad establecidos. La
perspectiva de cumplimiento regulatorio, alineada con el AI Act y CONPES
4144, incluye métricas que demuestran adherencia a requisitos normativos
obligatorios, tales como la realización de evaluaciones de impacto
ARA/DPIA (Análisis de Riesgos y Gestión de Datos Personales en
Inteligencia Artificial), la documentación técnica mediante Model Cards
y Data Sheets, y la implementación de controles específicos según el
nivel de riesgo del sistema. Esta perspectiva operacionaliza el concepto
de responsabilidad mediante indicadores verificables de cumplimiento que
pueden ser auditados tanto internamente como por entidades externas,
cumpliendo así con los requisitos del COBIT 2019 en materia de monitoreo
continuo de la conformidad regulatoria.

La perspectiva de gestión de riesgos, fundamentada en el NIST AI RMF e
ISO/IEC 23894, incluye métricas que cuantifican la efectividad de los
procesos de identificación, evaluación y mitigación de riesgos a lo
largo del ciclo de vida de los sistemas de IA. Esta perspectiva es
particularmente importante en el contexto de la Secretaría Distrital de
Gobierno, dado que administra servicios públicos críticos cuyo mal
funcionamiento o la discriminación podría afectar directamente a la
ciudadanía bogotana. Los indicadores en esta perspectiva incluyen tasas
de materialización de riesgos, tiempos de respuesta a incidentes
identificados, y efectividad de controles implementados, permitiendo una
gestión proactiva basada en evidencia cuantitativa. El COBIT 2019, en su
proceso DSS (Deliver, Service and Support), establece que el monitoreo
de incidentes y la capacidad de respuesta son elementos críticos para la
entrega de servicios de TI de calidad, lo cual se adapta perfectamente
al contexto de sistemas de IA cuya ejecución incorrecta podría acarrear
consecuencias significativas.

La perspectiva de creación de valor público, desarrollada mediante un
enfoque adaptado del Balanced Scorecard, incluye métricas que miden el
impacto tangible de la IA en la eficiencia operativa, la calidad del
servicio, la satisfacción ciudadana y la equidad en el acceso a los
servicios. Esta perspectiva responde a la necesidad fundamental de que
la adopción de IA en el sector público genere valor observable para la
ciudadanía, no solo innovación tecnológica per se. El DAFP (Departamento
Administrativo de la Función Pública) ha señalado en sus guías de
gobierno de TI que la continuidad de las iniciativas de transformación
digital depende críticamente de la capacidad de demostrar un impacto
positivo en la calidad y la eficiencia del servicio público, lo cual se
refleja en esta perspectiva de medición.

#### Principios de Diseño de las Métricas Vinculados a Niveles de Madurez COBIT 2019
 
Las métricas y KPIs del framework se diseñaron siguiendo principios
específicos que aseguran su utilidad práctica y viabilidad operativa,
especialmente considerando el contexto institucional particular de la
Secretaría Distrital de Gobierno y sus capacidades actuales. El COBIT
2019 define seis niveles de capacidad para los procesos de gobierno de
TI: Nivel 0 (Incomplete) donde los procesos no están implementados o no
alcanzan los objetivos; Nivel 1 (Performed) donde los procesos se
ejecutan informalmente; Nivel 2 (Managed) donde los procesos se
planifican, ejecutan y monitorean; Nivel 3 (Defined) donde los procesos
están estandarizados y documentados; Nivel 4 (Quantitatively Managed)
donde los procesos son controlados cuantitativamente; y Nivel 5
(Optimizing) donde los procesos se mejoran continuamente. La
proporcionalidad al riesgo es un principio fundamental que establece que
los requisitos de medición deben aumentar según el nivel de riesgo del
sistema implementado. Los sistemas de alto riesgo, definidos como
aquellos que afectan derechos fundamentales o beneficios significativos
de la ciudadanía, requieren un monitoreo continuo automatizado que
abarque múltiples dimensiones de equidad, privacidad y seguridad. Por el
contrario, en sistemas de riesgo limited o mínimo se aplican métricas
más simplificadas, con frecuencias de revisión menos exigentes, lo que
permite optimizar la asignación de recursos de monitoreo. En términos de
COBIT 2019, esto se alinea con el concepto de que distintos procesos y
dominios pueden alcanzar distintos niveles de madurez según su
criticidad para el negocio.

La viabilidad operativa es otro principio crítico que reconoce las
capacidades heterogéneas de las entidades distritales y la necesidad de
que el framework sea implementable de forma progresiva. Las métricas
priorizan aquellas que pueden ser capturadas con infraestructura
estándar, como logs de aplicaciones, encuestas de satisfacción, y
registros administrativos, sobre aquellas que requieren herramientas
especializadas costosas o procesos de recolección de datos complejos. La
Secretaría Distrital de Gobierno, a través del Plan Estratégico de
Tecnologías de la Información (PETI) vigente desde 2025, ha establecido
una infraestructura básica de monitoreo que puede aprovecharse para la
captura de estas métricas estándar. El principio de accionabilidad
establece que cada métrica se conecta directamente con acciones de
mejora o respuesta automática. Los umbrales de aceptabilidad definen
cuándo se activan protocolos de revisión, mitigación o escalamiento,
evitando así medición que no genere cambios o mejoras reales.
Finalmente, la trazabilidad a objetivos estratégicos garantiza que las
métricas de la Capa 5 se mapean directamente a las metas institucionales
establecidas en la Capa 1 Principios y Políticas y a los objetivos del
CONPES 4144, asegurando que todo lo que se mide contribuye realmente a
lograr objetivos concretos.

#### Métricas de Cumplimiento Normativo y Ciclo de Vida Regulatorio
 
Este conjunto de métricas verifica que se cumplen los requisitos
normativos del CONPES 4144, la Ley 1581 de 2012 sobre protección de
datos personales, las circulares de la Superintendencia de Industria y
Comercio (SIC), y las reglas del AI Act aplicables por analogía a
sistemas de alto riesgo en entidades públicas.

El porcentaje de casos de uso registrados en el sistema central
constituye un indicador fundamental de trazabilidad institucional que
mide la completitud del inventario distrital de sistemas de IA. La
fórmula específica es: (Casos de uso registrados en el Registro Central
/ Total de casos de uso identificados en operación o desarrollo) × 100.
El objetivo establecido es 100%, dado que la ausencia de registro
imposibilita la aplicación sistemática de controles de gobernanza y
representa un riesgo de cumplimiento normativo significativo. La
frecuencia de medición es mensual, con auditoría trimestral de
completitud mediante cruce con registros de áreas de TI, contratación y
presupuesto. El CONPES 4144 establece que la trazabilidad del ecosistema
de IA es una condición necesaria para la gobernanza efectiva, mientras
que la Ley 2279 de 2022 exige transparencia en la implementación de
tecnologías emergentes en el sector público. Un porcentaje inferior al
90% indica riesgos sistémicos de gobernanza y requiere acciones
correctivas inmediatas del Comité de IA.

La cobertura de uso del Catálogo Distrital de Proveedores Pre-evaluados
mide el grado de adopción de este instrumento de eficiencia en los
procesos de contratación de soluciones de IA. La fórmula es: (Número de
contrataciones que utilizaron proveedores del catálogo / Total de
contrataciones de sistemas de IA durante el período) × 100. El objetivo
diferenciado es ≥70% para sistemas de alto riesgo (donde la evaluación
previa mitiga riesgos críticos) y ≥50% para sistemas de riesgo limitado
(permitiendo mayor flexibilidad). La frecuencia es trimestral, con
consolidación anual para análisis de tendencias. La Ley 2279 de 2022
promueve la eficiencia en la contratación pública mediante la
estandarización de procesos y la reducción de cargas administrativas. El
uso sistemático del catálogo permite reducir entre 40-60% el tiempo de
evaluación técnica en licitaciones, fortalece el poder de negociación
institucional mediante compras agregadas y facilita la transferencia de
lecciones aprendidas entre entidades. Un porcentaje de adopción inferior
al 40% sugiere barreras operativas que deben ser investigadas y
removidas.

El porcentaje de casos de uso con clasificación de riesgo documentada es
una métrica fundamental que proporciona visibilidad sobre qué tantos
sistemas han sido clasificados según el marco de riesgos. La fórmula
específica es: (Casos de uso con clasificación de riesgo formalizada /
Total de casos de uso de IA en operación o desarrollo) × 100. El
objetivo establecido es 100%, ya que clasificar el riesgo es el primer
paso obligatorio del framework y sin ello no es posible aplicar
controles apropiados. La frecuencia de medición es trimestral, con
revisión completa anual para identificar casos nuevos. El CONPES 4144
establece que la gestión basada en riesgos debe ser el eje transversal
de la gobernanza de IA en Colombia, y el AI Act de la Unión Europea
proporciona un modelo que el Gobierno Nacional ha adoptado como
referencia conceptual para dividir sistemas en cuatro niveles de riesgo.

El porcentaje de sistemas de alto riesgo con ARA/DPIA completo y
aprobado es otra métrica crítica que verifica que los sistemas que
manejan datos personales hayan sido sometidos a un análisis riguroso de
riesgos. La fórmula es: (Sistemas de alto riesgo con ARA/DPIA realizado
según plantilla del toolkit / Total de sistemas de alto riesgo) × 100.
El objetivo es 100%, indicando que ningún sistema de alto riesgo puede
ponerse en funcionamiento sin que el ARADPIA haya sido aprobado por el
Comité de IA. La frecuencia es verificación continua antes de cada
despliegue, consolidado trimestralmente en reportes de gobernanza. La
Circular Externa 002-2024 de la SIC establece que es obligatorio
realizar Análisis de Riesgos y Gestión (ARA) para tratamientos de datos
personales con riesgos significativos, lo que aplica directamente a
sistemas de IA que procesan datos personales.

El porcentaje de sistemas con documentación técnica completa (Model
Cards y Data Sheets) mide la capacidad de transparencia y auditabilidad
del ecosistema de IA. La fórmula es: (Sistemas con Model Card y Data
Sheets actualizados / Total de sistemas en operación) × 100. Los
objetivos diferenciados son: 100% para sistemas de alto riesgo (donde la
documentación es indispensable para propósitos de auditoría
regulatoria), 80% para riesgo limitado en el primer año progresando a
100% en años subsecuentes. La frecuencia es semestral, reconociendo que
los sistemas evolucionan y requieren la actualización de su
documentación. El CONPES 4144 establece que los sistemas de IA deben
disponer de información técnica accesible para auditores, supervisores,
y cuando sea apropiado, para los usuarios finales.

El porcentaje de reuniones del Comité de IA realizadas según calendario
es una métrica de gobernanza que verifica que la estructura de
gobernanza está funcionando de verdad. La fórmula es: (Reuniones del
Comité de IA efectivamente realizadas / Reuniones programadas según
política) × 100. El objetivo es ≥ 90%, reconociendo que circunstancias
excepcionales pueden requerir reprogramación pero sin permitir que esto
se convierte en práctica regular. La frecuencia es trimestral,
consolidando los registros de asistencia y actas.

La cobertura de capacitación obligatoria en IA Responsable y Generativa
es una métrica compuesta que evalúa si se está desarrollando la
capacidad institucional necesaria para la adopción responsable de estas
tecnologías. La fórmula específica es: (Funcionarios certificados
vigentemente en IA Responsable y/o IA Generativa según rol / Total de
funcionarios en roles clave + usuarios activos de herramientas GenAI) ×
100. Los roles considerados incluyen: (a) roles de gobernanza: miembros
del Comité de IA, Oficial de IA Responsable, DPO, auditores internos;
(b) roles técnicos: responsables técnicos de casos de uso,
desarrolladores, arquitectos de datos; (c) roles operativos: sponsors de
negocio, funcionarios con acceso a herramientas de IA Generativa
institucionales.

Los objetivos se establecen de forma diferenciada según criticidad: 100%
para roles de gobernanza y técnicos (capacitación obligatoria previa al
ejercicio del rol), 100% para usuarios de IA Generativa antes de
habilitar acceso a herramientas (requisito de seguridad no negociable),
y ≥80% para roles de soporte (meta progresiva). La frecuencia de
medición es trimestral, con verificación continua integrada a los
sistemas de autenticación de herramientas GenAI que validan
certificación vigente antes de conceder acceso.

La certificación en IA Responsable tiene vigencia de 12 meses con
actualización anual de contenidos, mientras que la certificación en IA
Generativa tiene vigencia de 12 meses pero requiere actualización
trimestral de contenidos dada la velocidad de evolución tecnológica y
normativa en este dominio específico. La recertificación anticipada es
obligatoria ante cambios normativos significativos o identificación de
brechas de conocimiento mediante análisis de incidentes.

El CONPES 4144 establece explícitamente que el desarrollo de capacidades
es una condición habilitadora crítica para que el sector público pueda
adoptar IA de manera responsable, reconociendo que la tecnología sin
capital humano preparado genera riesgos inaceptables. La Ley 2279 de
2022 de Transformación Digital establece que las entidades públicas
deben garantizar la alfabetización digital de sus funcionarios en
tecnologías emergentes como condición para su implementación efectiva.
Un porcentaje de cobertura inferior al 70% en roles críticos representa
un riesgo operativo severo que debe activar protocolos de mitigación
inmediata, incluyendo la posible suspensión temporal de acceso a
sistemas críticos hasta completar la capacitación requerida.

#### 4.1.5.1 Métricas de Gestión de Riesgos y Monitoreo de Incidentes
 
Estas métricas hacen funcional el proceso de gestión de riesgos
establecido en la Capa 1 Política de Gestión de Riesgos y permiten
verificar cuantitativamente si los controles implementados en la Capa 4
están funcionando. El número de incidentes de IA por tipología
proporciona visibilidad clara sobre qué tipos de problemas experimentan
los sistemas implementados. Las categorías contempladas incluyen
incidentes técnicos (fallos operacionales, errores de predicción,
indisponibilidad del servicio), incidentes de privacidad (brechas de
datos, accesos indebidos a información personal), incidentes de equidad
(discriminación detectada en decisiones automatizadas, sesgos que
generan resultados discriminatorios), incidentes de seguridad (ataques
adversarios contra modelos, vulnerabilidades explotadas), y quejas
ciudadanas (retroalimentación de usuarios sobre problemas no formalmente
categorizados). El objetivo es una tendencia decreciente trimestre a
trimestre, con una tasa de incidentes críticos por debajo del umbral
definido según nivel de riesgo del sistema específico. La frecuencia es
registro continuo con reporte consolidado mensual. El proceso DSS01
(Manage Operations) de COBIT 2019 establece que las organizaciones deben
monitorear continuamente el desempeño operativo de sus sistemas,
identificar problemas y tomar acciones correctivas de manera oportuna.

El tiempo medio de respuesta a incidentes es una métrica que evalúa la
capacidad de la organización de reaccionar ante problemas identificados.
La fórmula específica es: Σ (tiempo desde detección hasta resolución
completa) / Número total de incidentes procesados. Los objetivos
diferenciados según criticidad son: ≤ 24 horas para incidentes críticos
(aquellos que afectan derechos fundamentales o generan exclusión de
ciudadanos), ≤ 72 horas para incidentes de alto impacto, ≤ 1 semana para
incidentes de impacto medio. La frecuencia es consolidación mensual con
alertas automatizadas cuando se violan los tiempos máximos de respuesta.
La tasa de materialización de riesgos mide si el análisis de riesgos fue
suficientemente profundo. La fórmula es: (Riesgos que efectivamente se
presentaron durante período / Total de riesgos identificados en ARA/DPIA
durante período anterior) × 100. El objetivo es \< 5%, lo que indicaría
que el análisis de riesgos fue suficientemente completo y que los
controles preventivos fueron efectivos en prevenir la mayoría de riesgos
identificados. Una tasa baja valida la calidad del proceso de análisis
de riesgos y demuestra que las mitigaciones están funcionando. La
frecuencia es semestral permitiendo acumular suficientes incidentes para
análisis estadístico.

La efectividad de controles es una métrica cualitativa pero fundamentada
en evidencia que evalúa si los controles implementados están funcionando
como fueron diseñados. La evaluación se realiza durante auditorías
internas por el equipo de control interno, o externas por auditores
independientes certificados. El objetivo es ≥ 85% de los controles
evaluados como efectivos, lo que indica que la mayoría de los mecanismos
de protección están operando correctamente. La frecuencia es anual
mediante auditoría interna para todos los sistemas, y bianual mediante
auditoría externa independiente específicamente para sistemas de alto
riesgo. Los procesos MEA (Monitor, Evaluate and Assess) del COBIT 2019
establecen que las organizaciones deben evaluar periódicamente si sus
controles continúan cumpliendo objetivos.

#### Métricas de Calidad de Datos y Confiabilidad de Fuentes
 
Reconociendo que la calidad de los datos determina de forma crítica la
calidad, equidad y confiabilidad de los sistemas de IA, estas métricas
evalúan las dimensiones fundamentales del ciclo de vida de datos desde
su recolección hasta su depuración y uso en modelos. La completitud de
datos mide qué porcentaje de registros contienen valores válidos en
campos críticos. La fórmula es: (Registros sin valores faltantes en
campos críticos / Total de registros en dataset) × 100. El objetivo es ≥
95% para campos críticos, reconociendo que un porcentaje bajo de datos
faltantes puede introducir sesgos si la ausencia no es aleatoria. La
frecuencia es evaluación mensual para datasets en uso activo,
facilitando detección temprana de problemas de calidad. El CONPES 4144
enfatiza explícitamente que contar con datos de buena calidad es un
pilar fundamental de la estrategia nacional de IA, reconociendo que
datos deficientes limitan significativamente los beneficios potenciales.

La tasa de detección de drift (cambio de datos o cambio de patrón en el
tiempo) mide la capacidad del sistema de identificar cambios en la
distribución de datos o en la relación entre variables a lo largo del
tiempo. Esta es una métrica importante porque el drift es una causa
frecuente de que los modelos pierdan desempeño en producción sin que se
haya anticipado durante la fase de entrenamiento. La métrica es: Número
de casos donde se detectó drift significativo durante monitoreo. El
objetivo es detección temprana antes de que el desempeño del modelo se
deteriore de forma severa. La frecuencia depende de la criticidad del
sistema: semanal para sistemas de alto riesgo, mensual para riesgo
limitado. La representatividad demográfica es una métrica que evalúa si
la distribución de datos refleja adecuadamente la población objetivo en
dimensiones protegidas como género, edad, estrato socioeconómico, y
localidad geográfica. La evaluación se realiza mediante tests
estadísticos como Chi-cuadrado o pruebas de similitud distribucional. El
objetivo es un p-valor ≥ 0.05 indicando que no hay diferencia
estadísticamente significativa entre la distribución de datos y la
población objetivo, o justificación documentada y aprobada de
diferencias intencionales. La frecuencia es trimestral o con cada
actualización significativa de datos de entrenamiento. El índice de
calidad de documentación de datos evalúa si la documentación sobre los
datos es suficientemente completa en dimensiones clave como origen de
datos, composición del dataset, procesos de limpieza aplicados, sesgos
identificados, y limitaciones conocidas. La evaluación se realiza en una
escala 0-100 basada en un checklist comprehensivo. El objetivo es ≥ 80%.
La frecuencia es con cada nuevo conjunto de datos o actualización
importante. La documentación rigurosa de datos es un requisito de
transparencia y auditabilidad establecido en los marcos internacionales.

#### Métricas de Desempeño Técnico y Confiabilidad de Modelos
 
Estas métricas evalúan el rendimiento técnico de los sistemas de IA,
asegurando que cumplan con estándares de precisión, equidad,
disponibilidad y velocidad de respuesta apropiados para el contexto del
servicio público distrital. Las métricas de precisión varían según el
tipo de sistema: para sistemas de clasificación se utilizan Precisión
(qué porcentaje de predicciones positivas fueron correctas), Recall o
Sensibilidad (qué porcentaje de casos positivos fueron identificados
correctamente), F1-Score (promedio ponderado de Precisión y Recall), y
AUC-ROC (medida de qué tan bien el modelo diferencia entre categorías).
Para sistemas de regresión se utilizan MAE (Error Absoluto Medio), RMSE
(Raíz del Error Cuadrático Medio), y R² (qué proporción de variación es
explicada por el modelo). Para sistemas de generación de texto se
utilizan BLEU y ROUGE (medidas de similitud de texto) además de
evaluación humana de calidad. El objetivo de precisión es un umbral
específico definido durante la fase de análisis de riesgos en ARADPIA,
típicamente ≥ 85% para casos críticos donde errores tienen consecuencias
significativas. La frecuencia es monitoreo continuo con alertas
automatizadas cuando se cruzan umbrales de alerta, con reporte
consolidado semanal o mensual. El desempeño técnico insuficiente
compromete directamente la confiabilidad del servicio público y puede
generar consecuencias adversas para ciudadanos.

Las métricas de equidad (fairness) cuantifican el grado de
discriminación potencial del sistema. El Disparate Impact Ratio es:
(Tasa de resultado positivo en grupo protegido) / (Tasa de resultado
positivo en grupo mayoritario). El Equal Opportunity Difference es la
diferencia absoluta en tasas de acierto entre grupos demográficos. El
objetivo es un Disparate Impact ≥ 0.8 (indicando que el grupo protegido
recibe resultados positivos en al menos 80% de la tasa del grupo
mayoritario) y Equal Opportunity Difference ≤ 0.1 (diferencia menor a 10
puntos porcentuales, ajustable según contexto específico). La frecuencia
es semanal o mensual en monitoreo continuo. El AI Act y el CONPES 4144
establecen explícitamente que la no discriminación es un principio
fundamental que debe permear todos los sistemas de IA del sector
público.

La disponibilidad del sistema (uptime o tiempo en que el servicio está
activo) es una métrica operacional crítica en el contexto de servicios
públicos. La fórmula es: (Tiempo de operación efectiva / Tiempo total
planificado) × 100. El objetivo es ≥ 99% para servicios críticos cuya
indisponibilidad afectaría derechos de ciudadanos, y ≥ 95% para
servicios no críticos. La frecuencia es monitoreo continuo por
infraestructura de TI con reporte consolidado mensual. El tiempo de
respuesta mide cuán rápido el sistema responde a las solicitudes de
usuarios. La métrica específica es el Percentil 95 del tiempo de
respuesta a consultas o inferencias del modelo. El objetivo es un umbral
definido en acuerdos de nivel de servicio (SLA), típicamente ≤ 2
segundos para interacciones ciudadanas directas en portales web o
aplicaciones móviles. La frecuencia es monitoreo continuo con reporte
semanal. La experiencia de usuario determina críticamente si la
población adopta y está satisfecha con servicios digitales.

#### 4.1.5.2 Métricas de Impacto en Servicio Público y Satisfacción Ciudadana
 
Este conjunto de métricas evalúa el valor real que generan los sistemas
de IA, respondiendo a la pregunta fundamental: Está la IA mejorando
efectivamente los servicios públicos y la experiencia ciudadana de
manera medible?. La satisfacción ciudadana se mide mediante encuestas
post-interacción que capturan el CSAT (Customer Satisfaction Score)
medido en escala 1-5, y NPS (Net Promoter Score) calculado como: (% de
personas que recomendarían - % de personas que no recomendarían). El
objetivo es ≥ 80% de respondientes satisfecho o muy satisfecho, y NPS ≥
50 indicando que la mayoría de ciudadanos recomendaría el servicio. La
frecuencia es captura continua mediante muestreo estadístico con
consolidación mensual. La aceptación ciudadana de la IA en el sector
público depende fundamentalmente de si la población experimenta mejoras
reales en los servicios que recibe.

La eficiencia operativa es una métrica que compara cómo funcionaban las
cosas antes y después de implementar IA. Las métricas específicas son:
(1) Tiempo promedio de atención o resolución de trámite, usando los
datos previos a IA como comparación, y (2) Reducción de costos
operativos. El objetivo es mejora ≥ 20% respecto a cómo era antes, un
umbral conservador que reconoce que no todos los casos de uso generarán
ganancias de eficiencia equivalentes. La frecuencia es evaluación
trimestral. El CONPES 4144 establece explícitamente que eficiencia y
productividad son objetivos clave de la adopción de IA en el sector
público.

El volumen de servicio mide la capacidad de atender más transacciones
con la implementación de IA. La métrica es: Número de transacciones o
consultas procesadas por el sistema de IA. Una métrica complementaria es
la tasa de resolución en primer contacto: (Casos resueltos sin
escalamiento a humano / Total de casos procesados) × 100. El objetivo es
crecimiento sostenido del volumen de transacciones, con tasa de
resolución ≥ 70% indicando que el sistema es capaz de manejar la mayoría
de las solicitudes de ciudadanos. La frecuencia es consolidación
mensual. La escalabilidad es un beneficio clave esperado de la
automatización con IA, permitiendo al sector público servir a más
ciudadanos con igual o menor inversión presupuestal.

La tasa de escalamiento a humano mide el balance entre dejar que el
sistema trabaje solo y el nivel de supervisión que se necesita. La
fórmula es: (Casos escalados a revisión o decisión humana / Total de
casos procesados) × 100. El objetivo es un balance pragmático,
típicamente 5-15% según criticidad del servicio, reconociendo que un
porcentaje muy alto indica que el sistema no es suficientemente
independiente para generar eficiencia, mientras que un porcentaje muy
bajo puede indicar que no se está revisando suficientemente y hay
riesgos de problemas no detectados. La frecuencia es consolidación
semanal o mensual. La equidad de acceso es una métrica que evalúa si
todos los segmentos de la población bogotana están accediendo
equitativamente al servicio. Se realiza análisis desagregado de uso por
grupos demográficos (género, edad, estrato, localidad), para identificar
si hay exclusión o subrepresentación de grupos vulnerables. El objetivo
es no diferencias estadísticamente significativas entre grupos, sin
justificación por diferencias en elegibilidad. La frecuencia es
evaluación trimestral. El principio constitucional de igualdad exige que
los servicios públicos no generen exclusión digital ni discriminación
por proximidad geográfica o estrato socioeconómico.

#### 4.1.5.3 Métricas de Madurez Institucional y Sostenibilidad
 
Este conjunto de métricas evalúa qué tan desarrolladas están las
capacidades de gobernanza de IA dentro de la Secretaría, facilitando la
planificación estratégica y la asignación de recursos a lo largo del
tiempo. El nivel de madurez institucional se evalúa según un modelo de
madurez 0-3 que será descrito en detalle en la sección 4.1.6 del
framework. Brevemente, Nivel 0 indica iniciativas incipientes sin
estructura formal, Nivel 1 indica procesos informales y inconsistentes,
Nivel 2 indica procesos documentados y parcialmente implementados, y
Nivel 3 indica procesos plenamente implementados, monitoreados y sujetos
a mejora continua. El objetivo es avanzar de al menos un nivel cada año,
reconociendo que el desarrollo institucional es un proceso gradual. La
frecuencia es evaluación anual mediante autoevaluación del Comité de IA
con validación externa por consultores especializados.

La métrica de cobertura de capacitación obligatoria, detallada en la
subsección 4.1.5.3 como componente de cumplimiento normativo, constituye
simultáneamente un indicador de madurez institucional. Las
organizaciones en Nivel 0 (Incipiente) típicamente presentan cobertura
inferior al 30% y sin sistematización; en Nivel 1 (Informal) la
cobertura oscila entre 30-60% con contenidos heterogéneos; en Nivel 2
(Documentado) la cobertura supera el 80% en roles clave con programas
estructurados; y en Nivel 3 (Optimizado) se alcanza 100% en roles
críticos con actualización continua y evaluación de efectividad mediante
análisis de reducción de incidentes atribuibles a brecha de
conocimiento.

El porcentaje de trámites y servicios con IA implementada es una métrica
de transformación digital que mide cuántos de los servicios que ofrece
la Secretaría ya tienen componentes de IA. La fórmula es: (Servicios con
componentes de IA / Total de servicios candidatos identificados en
roadmap) × 100. El objetivo es crecimiento progresivo según roadmap
aprobado, por ejemplo: 20% en el año 1, 40% en el año 2, 60% en el año
3, reconociendo que la transformación requiere tiempo y debe hacerse de
forma ordenada. La frecuencia es evaluación semestral. La relación
costo-beneficio es una métrica de sostenibilidad financiera que evalúa
si la inversión en IA está generando retorno. La fórmula es: (Beneficios
tangibles monetarios + valor estimado de beneficios intangibles) /
(Costos totales de implementación incluyendo desarrollo,
infraestructura, operación y soporte) sobre período de 3 años. El
objetivo es ROI ≥ 1.5 a 3, indicando que por cada peso invertido se
generan entre 1.50 y 3 pesos de valor. La frecuencia es evaluación
anual. La sostenibilidad fiscal exige demostración clara de que la
inversión pública en tecnología está generando valor.

El índice de sostenibilidad institucional incorpora como dimensión
específica la \"capacidad de autosuficiencia en capacitación\",
evaluando si la entidad depende críticamente de consultores externos
para formación o si ha desarrollado capacidades internas de formadores
certificados. Las entidades con puntuación ≥70 en sostenibilidad
típicamente cuentan con al menos 2-3 formadores internos certificados
por cada 100 funcionarios usuarios de IA, permitiendo escalabilidad y
actualización ágil de contenidos sin dependencia presupuestal externa.
 
#### 4.1.5.4 Dashboard Integrado y Reportería
 
Las métricas descritas se integran en un Dashboard de Gobernanza de IA
que proporciona visibilidad clara del estado de los sistemas de IA. El
dashboard se estructura en tres niveles de información: Vista ejecutiva
para Alta Dirección que muestra indicadores resumen por dimensión
(cumplimiento, riesgos, impacto), con colores verde/amarillo/rojo según
umbrales, actualizado mensualmente para facilitar toma de decisiones.
Vista operativa para gestores de sistemas que muestra métricas técnicas
y de servicio para cada caso de uso específico, con alertas
automatizadas cuando se superan umbrales, actualización continua para
permitir respuesta rápida a problemas. Vista de auditoría para control
interno y auditores que muestra trazabilidad completa de cumplimiento
normativo, evidencias de que los controles están funcionando, registro
de incidentes, actualización trimestral. Este sistema de medición
transforma la gobernanza de IA de una aspiración normativa en una
práctica basada en evidencia cuantitativa observable, permitiendo la
mejora continua, la rendición de cuentas clara, y la demostración
concreta de valor público generado por la adopción responsable de
inteligencia artificial en el Distrito Capital de Bogotá. Los
componentes del Dashboard se referencian en el Anexo C.

### 4.1.6 Modelo de Madurez Institucional
 
El modelo de madurez institucional proporciona un marco de referencia
para evaluar y orientar el progreso de la Secretaría Distrital de
Gobierno en la adopción responsable de la inteligencia artificial. Este
modelo se fundamenta en los principios de COBIT 2019, que establece una
escala de madurez de cinco niveles para los procesos de gobierno de TI,
adaptándose específicamente al contexto de gobernanza de IA en entidades
públicas del Distrito Capital. El modelo propuesto contempla cuatro
niveles de madurez (Nivel 0 a Nivel 3) reconociendo las capacidades
actuales de las entidades distritales y estableciendo una trayectoria
clara de evolución institucional que responde a los objetivos del CONPES
4144 de desarrollar capacidades progresivas en el ecosistema de IA
colombiano.

Nivel 0: Incipiente representa la situación inicial donde no existe
gobernanza formal de IA. A este nivel, las iniciativas de IA son
aisladas, informales y carecen de coordinación institucional. No hay
políticas documentadas, ni procesos establecidos para la gestión de
riesgos, y la decisión de adoptar IA se toma de forma reactiva respecto
a necesidades operativas puntuales sin evaluación comprehensiva de
impacto. La infraestructura de monitoreo no existe, o es mínima. Las
capacidades técnicas se concentran en individuos específicos sin
transferencia de conocimiento. Los requisitos de conformidad normativa
no se abordan de forma sistemática. La Secretaría podría estar en este
nivel si inicia exploraciones puntuales de IA sin estructura
institucional, identificable cuando solo algunos departamentos
experimentan con soluciones de IA sin coordinación central.

Nivel 1: Informal marca el primer paso donde comienzan a surgir
iniciativas coordinadas de IA pero sin formalización completa. Se
establece un Comité de IA incipiente que se reúne de forma irregular. Se
inician procesos de evaluación de riesgos pero de manera inconsistente,
aplicados solo a algunos sistemas. Existe documentación parcial de
políticas y procedimientos, pero estos no se comunican ni se cumplen
sistemáticamente. Se realizan algunas capacitaciones en IA responsable
para ciertos grupos, pero sin cobertura integral. Los controles son
parcialmente implementados y se detectan incidentes pero la respuesta es
reactiva. Este nivel refleja una transición donde la organización
reconoce la necesidad de gobernanza pero aún opera con muchos aspectos
informales y personas clave.

Nivel 2: Documentado representa un punto de madurez intermedia donde la
gobernanza de IA está parcialmente implementada y documentada. A este
nivel, el Comité de IA funciona regularmente con actas y trazabilidad de
decisiones. Se cuenta con políticas formales de gobernanza de IA
comunicadas a toda la organización, aunque su cumplimiento requiere
supervisión activa. Los procesos de gestión de riesgos están
documentados y aplicados a todos los sistemas de alto riesgo, aunque con
variabilidad en profundidad y calidad. La documentación técnica de
sistemas existe aunque puede presentar gaps. Se realiza capacitación
sistemática en roles clave, con cobertura de ≥80% en roles de
gobernanza. Los controles están implementados para sistemas críticos,
monitoreados de forma regular. Los incidentes se registran, clasifican y
se inician protocolos de respuesta. La infraestructura de monitoreo
básica está en operación. Este nivel es alcanzable en el mediano plazo
con inversión en formalización de procesos.

Nivel 3: Optimizado representa la madurez institucional objetivo a tres
años, donde la gobernanza de IA está completamente implementada,
documentada, monitoreada y sometida a mejora continua. A este nivel, el
Comité de IA funciona operativamente con alta efectividad, tomando
decisiones informadas con datos. Las políticas están plenamente
implementadas con cumplimiento ≥90%. Los procesos de gestión de riesgos
son robustos, aplicados consistentemente a todos los sistemas con
documentación completa de ARADPIA y controles. La documentación técnica
es exhaustiva, actualizada y accesible. La capacitación alcanza 100% en
roles clave con actualizaciones continuas. Los controles son altamente
efectivos (≥85%), monitoreados en tiempo real. La respuesta a incidentes
es ágil y efectiva. El dashboard de gobernanza proporciona visibilidad
en tiempo real de todas las dimensiones. La cultura organizacional
valora la IA responsable. Se genera valor público cuantificable. La
sostenibilidad institucional es alta con apropiación de líderes,
continuidad presupuestal y capacidades internas robustas.

El movimiento entre niveles debe ser progresivo, con evaluaciones
anuales formales mediante autoevaluación del Comité de IA validada por
auditores externos independientes. Cada nivel incorpora las capacidades
del anterior, generando una progresión que es realista pero ambiciosa.
El CONPES 4144 enfatiza que la madurez institucional es determinante
para la adopción responsable y sostenible de IA. El modelo propuesto
permite a la Secretaría Distrital de Gobierno comunicar claramente dónde
se encuentra, qué capacidades necesita desarrollar, y cuáles son los
hitos de progreso esperados, facilitando la planificación estratégica y
la asignación de recursos para convertir la gobernanza de IA en una
capacidad institucional permanente y efectiva que genere confianza
pública y valor sostenible.

## Caja de Herramientas Operativa (Toolkit)

El toolkit representa el componente práctico del framework, al ofrecer
un conjunto de plantillas, matrices y guías listas para su aplicación,
cuyo propósito es facilitar la implementación de la gobernanza de la
inteligencia artificial en entidades que presentan niveles diversos de
capacidad técnica. Cada uno de los instrumentos ha sido concebido con
criterios de usabilidad, mediante el uso de lenguaje claro, estructuras
intuitivas e instrucciones detalladas paso a paso; de adaptabilidad, al
incluir campos obligatorios y opcionales claramente diferenciados, así
como escalabilidad conforme al nivel de riesgo; de trazabilidad, al
incorporar referencias explícitas a requisitos normativos como el CONPES
4144, la Ley 1581, el AI Act y los estándares ISO; y de integrabilidad,
al asegurar su compatibilidad tanto entre sí como con el proceso de
ciclo de vida definido por el framework.

El toolkit representa el componente práctico del framework, al ofrecer
un conjunto de plantillas, matrices y guías listas para su aplicación,
cuyo propósito es facilitar la implementación de la gobernanza de la
inteligencia artificial en entidades que presentan niveles diversos de
capacidad técnica. En la Figura 4 se presenta una visión general y la
interrelación de los siete instrumentos que componen este toolkit
operativo, los cuales se detallarán a continuación.

### AI Use-Case Canvas
 
El propósito de esta herramienta consiste en estructurar y documentar de
manera sistemática la propuesta de caso de uso durante la fase inicial
de intake. Su objetivo es garantizar una comprensión clara del propósito
del sistema, una identificación precisa de los actores involucrados, así
como una evaluación preliminar de los riesgos asociados y de la
viabilidad técnica y legal del proyecto. La Figura 5 ilustra la
estructura completa y las doce secciones que componen el AI Use-Case
Canvas, herramienta fundamental para el proceso de gobernanza.

La plantilla correspondiente se organiza en doce secciones, las cuales
se describen detalladamente a continuación.
 
**Sección 1: Identificación del Caso de Uso** -- Se incluye un título
descriptivo que sintetiza la finalidad del sistema propuesto, junto con
la identificación de la entidad responsable y su unidad organizacional
correspondiente. Asimismo, se requiere consignar los datos del sponsor
de negocio, incluyendo su nombre, cargo y medios de contacto, así como
los del responsable técnico, especificando igualmente su nombre, cargo y
datos de contacto. Esta sección concluye con la indicación de la fecha
de elaboración del documento y la versión correspondiente, lo que
permite establecer un control de versiones y asegurar la trazabilidad
del proceso.
 
**Sección 2: Contexto y Propósito** - Describe de forma concisa el
problema o necesidad que se pretende abordar, limitando la extensión a
un máximo de 200 palabras para garantizar claridad y enfoque. En este
apartado se debe especificar el servicio, trámite o proceso
institucional al que se aplicará la solución basada en inteligencia
artificial, así como el propósito específico del sistema, es decir, la
función que se espera que cumpla dentro del flujo operativo. También se
debe indicar el tipo de sistema de IA que se propone implementar, ya sea
de clasificación, regresión, generación de lenguaje, recomendación u
otro, según corresponda. Finalmente, se deben detallar los resultados
esperados, procurando que estos sean cuantificables en la medida de lo
posible, con el fin de facilitar su posterior evaluación y seguimiento.
La Figura 6 presenta una vista detallada de las dos primeras secciones
del AI Use-Case Canvas, correspondientes a la Identificación del Caso de
Uso y al Contexto y Propósito, que constituyen la base informativa y de
justificación del proyecto.
 
**Sección 3: Actores Involucrados** - La identificación de los actores
involucrados en el sistema contempla, en primer lugar, a los usuarios
finales, entre los que se incluyen funcionarios públicos, ciudadanos y
otros grupos que interactúan directamente con la solución tecnológica.
El perfil de estos usuarios se caracteriza por niveles diversos de
alfabetización digital, condiciones particulares de accesibilidad y una
amplia diversidad sociocultural, lo que exige enfoques inclusivos en el
diseño y despliegue del sistema. El responsable de los datos utilizados,
identificado como el propietario de los datos, asume la obligación de
garantizar su integridad, legalidad y uso ético. Además, se reconocen
stakeholders que podrían verse afectados por las decisiones
automatizadas del sistema, lo que implica una evaluación anticipada de
impactos. En cuanto a la gobernanza, se definen roles específicos que
incluyen al Delegado de Protección de Datos (DPO), las áreas de
Tecnologías de la Información y Seguridad, el equipo jurídico y el
Comité de Inteligencia Artificial, todos ellos con funciones
diferenciadas en la supervisión, validación y toma de decisiones
estratégicas.
 
**Sección 4: Datos Requeridos** - El funcionamiento del sistema depende
de un conjunto de datos provenientes de fuentes internas
institucionales, externas gubernamentales y de terceros autorizados.
Estas fuentes aportan categorías de datos que incluyen información
personal, datos sensibles y registros públicos, cuya combinación permite
alimentar los modelos de análisis y toma de decisiones. El volumen
estimado de datos, así como la frecuencia de actualización, se
determinan en función de la naturaleza del servicio y de los
requerimientos operativos. Una evaluación preliminar de la calidad y
representatividad de los datos permite identificar posibles sesgos,
vacíos informativos o inconsistencias que podrían afectar el desempeño
del sistema. Asimismo, se realiza una evaluación inicial en materia de
privacidad, en la que se determina si el conjunto de datos incluye
información personal o sensible, lo que activa protocolos específicos de
protección conforme a la legislación vigente y a los estándares
internacionales de gobernanza de datos. La Figura 7 muestra las
siguientes dos secciones del *AI Use-Case Canvas*, dedicadas a los
Actores Involucrados y a los Datos Requeridos, elementos críticos para
comprender el ecosistema y los insumos del sistema propuesto.

**Sección 5: Revisión Legal y Bases Jurídicas** - La revisión legal del
sistema parte de la identificación de la base normativa que habilita la
prestación del servicio público correspondiente, considerando tanto
disposiciones generales como específicas del sector involucrado. En los
casos en que se contempla el tratamiento de datos personales, se
analizan las bases jurídicas aplicables, entre las que se incluyen el
consentimiento informado, la ejecución de contratos, el cumplimiento de
obligaciones legales, el interés legítimo y el ejercicio de funciones
públicas. Este análisis se complementa con la identificación de
normativa específica aplicable, ya sea de carácter sectorial o
territorial, que pueda incidir en el diseño, operación o supervisión del
sistema. Finalmente, el área Jurídica realiza una evaluación preliminar
de conformidad legal, con el propósito de anticipar ajustes normativos
necesarios y asegurar la alineación del sistema con el marco regulatorio
vigente.
 
**Sección 6: Clasificación Preliminar de Riesgo** - La clasificación
inicial del riesgo se realiza conforme a los criterios establecidos en
el Reglamento de Inteligencia Artificial (AI Act), los cuales permiten
determinar si el sistema afecta derechos fundamentales, interviene en
servicios esenciales, participa en decisiones que impactan directamente
a personas o incorpora tecnologías de reconocimiento biométrico. A
partir de esta evaluación, se asigna una clasificación preliminar que
puede ubicarse en las categorías de riesgo inaceptable, alto, limitado o
mínimo. Esta categorización se sustenta en una justificación técnica y
normativa que considera el contexto de uso, el tipo de datos procesados,
el grado de automatización y el impacto potencial sobre los derechos de
los individuos, así como sobre la operación institucional. La Figura 8
presenta las secciones 5 y 6 del AI Use-Case Canvas, enfocadas en el
análisis del marco legal aplicable y la clasificación preliminar de
riesgo del sistema, aspectos fundamentales para garantizar la viabilidad
normativa y la gestión proactiva de impactos.

**Sección 7: Identificación Preliminar de Riesgos** - La evaluación
inicial de riesgos contempla dimensiones éticas, de privacidad,
seguridad, equidad, operación y reputación institucional. En el plano
ético, se identifican posibles afectaciones a la autonomía individual,
la dignidad humana y la aparición de sesgos discriminatorios. En cuanto
a la privacidad, se reconocen riesgos asociados con la re-identificación
de datos, el uso secundario no autorizado y la existencia de brechas de
protección. Los riesgos de seguridad incluyen vulnerabilidades frente a
ataques cibernéticos, fallos sistémicos y posibles manipulaciones
maliciosas. Desde una perspectiva de equidad, se advierte la posibilidad
de sesgos algorítmicos que generen exclusión de grupos poblacionales
específicos. En el ámbito operativo, se consideran factores como la
dependencia de proveedores externos, la sostenibilidad técnica del
sistema y su eventual obsolescencia. Finalmente, se señalan riesgos
reputacionales vinculados con la pérdida de confianza pública y la
generación de controversias. Para cada uno de estos escenarios, se han
delineado mitigaciones preliminares que orientan la gestión proactiva de
los riesgos identificados.
 
**Sección 8: Métricas de Éxito e Indicadores de Impacto** - La medición
del desempeño del sistema se estructura en torno a indicadores clave
(KPIs) que abarcan aspectos técnicos, de servicio y de cumplimiento
normativo. En el ámbito técnico, se consideran métricas como la
precisión de los resultados, la disponibilidad operativa y los tiempos
de respuesta. En relación con el impacto en el servicio, se incluyen
indicadores de eficiencia institucional, niveles de satisfacción de los
usuarios y cobertura poblacional alcanzada. Los KPIs de cumplimiento se
centran en la ejecución de evaluaciones de riesgo algorítmico (ARA) y de
impacto en protección de datos (DPIA), así como en la implementación de
controles y auditorías periódicas. Para establecer una línea base
comparativa, se documenta el estado actual de los procesos, lo que
permite medir mejoras de manera objetiva. Asimismo, se definen metas
cuantificables a seis y doce meses, con el propósito de orientar la toma
de decisiones y evaluar el progreso del sistema en función de sus
objetivos estratégicos. La Figura 9 muestra las secciones 7 y 8 del *AI
Use-Case Canvas*, dedicadas a la identificación preliminar de riesgos y
a la definición de métricas de éxito, componentes esenciales para
anticipar desafíos y establecer criterios claros de evaluación del
proyecto.
 
**Sección 9: Plan de Despliegue, Formación y Comunicación** - La
estrategia de implementación contempla diversas modalidades, entre las
que se incluyen el desarrollo de pilotos, el despliegue gradual por
fases y el enfoque de implementación total o *big bang*, según la
naturaleza del sistema y el contexto institucional. El alcance inicial
se define en función de las capacidades disponibles, mientras que el
escalamiento se planifica conforme a criterios de madurez tecnológica y
sostenibilidad operativa. En este marco, se han identificado necesidades
específicas de capacitación tanto para funcionarios públicos como para
ciudadanos, con el objetivo de asegurar una apropiada adopción y
comprensión del sistema. Cuando el proyecto lo amerite, se establece un
plan de comunicación y divulgación dirigido a la ciudadanía, orientado a
promover la transparencia, la participación informada y la confianza
pública. Finalmente, se presenta un cronograma estimado de
implementación que permite visualizar las etapas clave del proceso y
anticipar los recursos requeridos en cada fase.
 
**Sección 10: Monitoreo, Auditoría y Respuesta a Incidentes** - El
sistema incorpora controles de monitoreo continuo que abarcan
dimensiones técnicas, de equidad algorítmica y de privacidad, con el fin
de garantizar su funcionamiento ético y conforme a los estándares
normativos vigentes. La frecuencia de las revisiones y auditorías se
establece en función del nivel de riesgo asociado y de los
requerimientos regulatorios aplicables. En caso de presentarse
incidentes, se activa un protocolo de respuesta que define
responsabilidades, tiempos de reacción y mecanismos de mitigación.
Adicionalmente, cuando el sistema tiene implicaciones directas sobre la
ciudadanía, se habilitan canales específicos para la recepción de
reclamaciones, los cuales deben ser accesibles, eficaces y respetuosos
de los derechos fundamentales. La Figura 10 ilustra las secciones 9 y 10
del AI Use-Case Canvas, que abordan la planificación operativa del
despliegue, la formación necesaria y los mecanismos de monitoreo y
respuesta a incidentes, asegurando una implementación controlada y una
operación vigilante del sistema.
 
**Sección 11: Criterios y Plan de Fin de Vida** - El sistema deberá ser
retirado en caso de que se presenten condiciones como obsolescencia
tecnológica, aparición de riesgos considerados inaceptables, una
relación costo-beneficio desfavorable o modificaciones sustantivas en el
marco regulatorio vigente. Ante tales escenarios, se establece un plan
preliminar para la gestión de datos al final del ciclo de vida del
sistema, el cual contempla medidas de resguardo, eliminación segura y
cumplimiento de obligaciones legales en materia de protección de datos
personales. Asimismo, se propone un plan de transición hacia soluciones
alternativas, con el fin de garantizar la continuidad operativa y
mitigar impactos negativos sobre los procesos institucionales afectados.
 
**Sección 12: Aprobaciones y Decisión** - La evaluación de viabilidad
técnica queda a cargo del Responsable Técnico, quien debe determinar si
el proyecto es viable, viable con condiciones o no viable. En paralelo,
el área Jurídica realiza una evaluación de conformidad legal,
clasificando la propuesta como conforme, sujeta a ajustes o no conforme.
Por su parte, el Delegado de Protección de Datos (DPO) evalúa los
aspectos de privacidad, indicando si el proyecto está aprobado, requiere
la elaboración de una Evaluación de Impacto en la Protección de Datos
(DPIA) o no ha sido aprobado. La dimensión presupuestal es revisada por
el equipo de Planeación, que establece si existen recursos disponibles,
si se requiere gestión adicional o si el proyecto resulta no viable
desde el punto de vista financiero. Finalmente, el Comité de IA emite
una decisión formal, la cual puede consistir en la aprobación para
proceder a la Fase 2, la aprobación con condiciones, el rechazo o la
solicitud de información adicional. Esta decisión debe ser refrendada
mediante la firma del Presidente del Comité, acompañada de la fecha
correspondiente. Finalmente, la **Figura 11** presenta las dos últimas
secciones del *AI Use-Case Canvas*, que establecen los criterios para el
fin de vida del sistema y documentan el proceso formal de aprobaciones,
cerrando así el ciclo de evaluación inicial con claridad en la
gobernanza y la toma de decisiones.

### 4.2.2 Matriz de Riesgos de IA
 
El propósito de esta herramienta es ofrecer un instrumento estandarizado
que facilite la identificación, evaluación y priorización de riesgos
asociados al uso de sistemas basados en IA. Esta herramienta se
fundamenta en un enfoque analítico que considera tanto la probabilidad
de ocurrencia como el impacto potencial de cada riesgo, evaluados a
través de múltiples dimensiones críticas para el entorno institucional.

La metodología adoptada se estructura en una matriz de evaluación de
3x3, en la cual se cruzan los niveles de probabilidad e impacto,
clasificados en tres categorías: bajo, medio y alto. Esta combinación
genera una calificación de riesgo final que oscila entre 1 y 9,
permitiendo su categorización en tres niveles: bajo (1-3), medio (4-6) y
alto (7-9). Cada nivel de riesgo conlleva un conjunto específico de
acciones requeridas, orientadas a mitigar sus posibles efectos adversos.
En este sentido, la matriz no solo actúa como un mecanismo de
diagnóstico, sino también como una guía para la toma de decisiones
estratégicas en la gestión responsable de tecnologías basadas en IA.
La Figura 12 presenta de forma visual la metodología central de
evaluación de riesgos, basada en la matriz de probabilidad e impacto que
permite clasificar y priorizar los riesgos identificados.

**Dimensiones de impacto**
 
La evaluación de riesgos en sistemas de inteligencia artificial debe
considerar múltiples dimensiones que reflejan el alcance potencial de
sus consecuencias. En primer lugar, se encuentra la dimensión relativa a
los derechos y libertades fundamentales, la cual contempla el riesgo de
que los sistemas vulneren o restrinjan garantías constitucionales como
la privacidad, la igualdad ante la ley, el debido proceso, la libertad
de expresión y el acceso equitativo a servicios públicos. Esta dimensión
resulta crítica, dado que cualquier afectación en estos ámbitos puede
comprometer la legitimidad institucional y la protección de los derechos
humanos (United Nations Educational, Scientific and Cultural
Organization \[UNESCO\], 2021).

En segundo lugar, la equidad y la no discriminación constituyen una
dimensión clave para identificar sesgos algorítmicos, así como posibles
mecanismos de exclusión que afecten a grupos protegidos o en situación
de vulnerabilidad.

La tercera dimensión corresponde a la continuidad y calidad del
servicio, entendida como el impacto que los sistemas de IA pueden tener
sobre la capacidad institucional para garantizar la prestación de
servicios esenciales. Aspectos como la disponibilidad, la confiabilidad
operativa y la resiliencia frente a fallos técnicos son elementos
centrales en esta evaluación (Organisation for Economic Co-operation and
Development \[OECD\], 2022).

La cuarta dimensión aborda la seguridad y la ciberseguridad,
considerando la exposición a ataques maliciosos, brechas de datos
sensibles y fallos que puedan derivar en consecuencias físicas o
digitales de alto riesgo. En este contexto, la protección de
infraestructuras críticas y la integridad de los sistemas se convierten
en prioridades estratégicas (European Commission, 2021).

En quinto lugar, se analiza el impacto sobre la reputación institucional
y la confianza pública. El uso de tecnologías opacas o mal gestionadas
puede deteriorar la percepción ciudadana respecto a la transparencia y
responsabilidad del sector público, generando resistencia social y
pérdida de legitimidad (Floridi et al., 2018).

Finalmente, la dimensión de cumplimiento regulatorio contempla el riesgo
de que los sistemas de IA infrinjan normativas vigentes, lo cual podría
acarrear sanciones legales, responsabilidades administrativas o
consecuencias reputacionales. Esta dimensión exige una revisión
constante del marco jurídico aplicable y una articulación efectiva entre
los equipos técnicos y jurídicos (González Fuster, 2020)

**Escala de probabilidad e impacto**
 
La evaluación de riesgos en sistemas de inteligencia artificial requiere
una estimación sistemática tanto de la probabilidad de ocurrencia como
del impacto potencial de cada evento identificado. Para ello, la matriz
propone una escala ordinal de tres niveles ---bajo, medio y alto--- que
permite clasificar de forma estandarizada los distintos escenarios de
riesgo.

En cuanto a la probabilidad, se establecen tres categorías. El nivel
bajo (valor 1) se asigna a eventos cuya ocurrencia se considera
improbable, es decir, con una probabilidad inferior al 10 % durante el
horizonte temporal previsto para la operación del sistema. El nivel
medio (valor 2) corresponde a situaciones con una posibilidad razonable
de materialización, estimada entre el 10 % y el 50 %. Finalmente, el
nivel alto (valor 3) se reserva para aquellos riesgos cuya ocurrencia se
considera probable o altamente probable, superando el umbral del 50 %.

Por su parte, la escala de impacto también se estructura en tres
niveles. El impacto bajo (valor 1) se refiere a consecuencias menores,
de alcance localizado y reversibles con un esfuerzo mínimo. El impacto
medio (valor 2) implica efectos significativos que, aunque no
necesariamente irreversibles, requieren un esfuerzo sustancial para su
mitigación y pueden afectar a grupos específicos de personas. En
contraste, el impacto alto (valor 3) se asocia con consecuencias graves,
difíciles o imposibles de revertir, que comprometen derechos
fundamentales o afectan a un número considerable de individuos, además
de generar un daño reputacional severo para la entidad responsable.

La combinación de estos dos ejes ---probabilidad e impacto--- permite
calcular una calificación de riesgo mediante la multiplicación de ambos
valores, generando un rango que va de 1 a 9. Esta puntuación se traduce
en tres niveles de riesgo: bajo (1 a 3), medio (4 a 6) y alto (7 a 9),
los cuales orientan la selección de medidas de mitigación proporcionales
a la magnitud del riesgo identificado.

**Plantilla de la matriz y acciones según nivel de riesgo**
 
La Matriz de Riesgos de IA se operacionaliza mediante una plantilla
estructurada que permite documentar de forma sistemática cada riesgo
identificado. Esta plantilla incluye los siguientes campos: ID del
riesgo, descripción detallada, categoría temática, dimensiones de
impacto involucradas, probabilidad estimada (valor entre 1 y 3), impacto
proyectado (valor entre 1 y 3), calificación total obtenida por la
multiplicación de probabilidad e impacto, nivel de riesgo resultante,
controles existentes, evaluación de la efectividad de dichos controles,
controles adicionales propuestos, responsable asignado y estado actual
del riesgo.

Este formato facilita la trazabilidad de los riesgos y la articulación
de medidas de mitigación proporcionales a su nivel. La calificación
final, obtenida mediante la fórmula P × I, permite clasificar el riesgo
en tres niveles: bajo (1 a 3), medio (4 a 6) y alto (7 a 9). Cada nivel
conlleva un conjunto diferenciado de acciones institucionales.

Para los riesgos clasificados como bajos, se recomienda mantener un
monitoreo rutinario, aplicar controles básicos y realizar una revisión
anual del estado del riesgo. En el caso de los riesgos medios, se
requiere la implementación de controles específicos, un monitoreo más
frecuente ---mensual o trimestral---, revisión semestral y aprobación
por parte de niveles gerenciales. Finalmente, los riesgos altos demandan
una respuesta más robusta: deben ser mitigados antes del despliegue del
sistema, contar con controles reforzados obligatorios, someterse a
monitoreo continuo y revisión frecuente. Además, pueden requerir el
rediseño del sistema o incluso el rechazo del caso de uso, y su
aprobación debe ser otorgada por la Alta Dirección o el Comité de IA
correspondiente.

Este enfoque escalonado permite una gestión proporcional del riesgo,
alineada con principios de gobernanza tecnológica responsable, y asegura
que los sistemas de IA operen dentro de márgenes aceptables de
seguridad, equidad y legalidad.  La Figura 13 muestra el formato
operativo de la plantilla de la Matriz de Riesgos, con los campos para
registrar cada riesgo identificado y su correspondiente plan de acción.
 
### 4.2.3 Plantilla ARA / DPIA
 
La plantilla ARA/DPIA constituye uno de los instrumentos más críticos
dentro del toolkit del framework, al integrar en un solo documento la
*Evaluación de Riesgos Algorítmicos (ARA)* y la *Evaluación de Impacto
en Protección de Datos (DPIA)*. Su propósito es ofrecer una metodología
estructurada que permita identificar, analizar y mitigar los riesgos
derivados del uso de sistemas de inteligencia artificial, tanto en lo
referente a derechos fundamentales como a aspectos de privacidad,
equidad, seguridad y transparencia.\
Este instrumento es fundamental para asegurar la alineación con marcos
regulatorios como la **Circular 002 de la SIC**, el **CONPES 4144**, la
**Ley 1581 de Habeas Data**, el **AI Act**, así como con estándares
internacionales como **ISO/IEC 23894**, **ISO 42001**, **NIST AI RMF** y
buenas prácticas de gobernanza algorítmica. La Figura 14 muestra la
estructura completa y las doce secciones que componen la plantilla
ARA/DPIA, herramienta central para la evaluación integral de riesgos e
impactos de los sistemas de IA.

**Sección 1. Información General**
 
Esta sección reúne los datos básicos que identifican el sistema
evaluado, tales como la entidad responsable, la unidad operativa, la
denominación del sistema, los responsables del análisis, la fecha de
elaboración y el número de versión.

Su función principal es establecer trazabilidad documental y permitir
que cualquier auditor o evaluador comprenda quién está a cargo, cuándo
se elaboró el documento y sobre qué sistema recae la evaluación.\
Se completa al inicio y se actualiza cada vez que se modifique el modelo
o el análisis de riesgos. La **Figura 15** ilustra el diseño y los
campos específicos de la Sección 1: Información General, que establece
los datos fundamentales de identificación y trazabilidad del ARA/DPIA.

**Sección 2. Descripción del Sistema y Alcance**
 
Incluye una explicación clara del sistema de IA: su propósito, los
elementos técnicos que lo componen, la base legal que justifica su
implementación, la población a la que afecta, los casos de uso
permitidos y los expresamente prohibidos, así como el tipo de decisiones
que genera.\
Esta sección permite comprender de manera integral qué hace el sistema y
en qué condiciones debe operar. También ayuda a prevenir usos indebidos,
sobre todo cuando un sistema podría ampliarse a contextos no
autorizados.

Se completa con apoyo del responsable técnico y del área jurídica.
La Figura 16 muestra la estructura de la Sección 2: Descripción del
Sistema y Alcance, diseñada para capturar de manera exhaustiva las
características fundamentales y los límites operativos del sistema de IA
bajo evaluación.
 
**Sección 3. Datos y Origen de la Información**
 
La tercera sección integra el mapeo de datos y una versión simplificada
del Data Sheet. En ella se describen las categorías de información
utilizadas, el tipo de dato, las fuentes de origen, la licitud del
tratamiento, las técnicas aplicadas, los sesgos potenciales y las
observaciones relevantes.\
Con esta información se evalúan aspectos fundamentales como calidad,
representatividad, presencia de datos personales y eventuales riesgos de
uso indebido.\
La sección es crítica para dar cumplimiento a la normativa de protección
de datos y para anticipar posibles sesgos o desigualdades.

Se completa en conjunto con el equipo de datos. La Figura 17 ilustra la
Sección 3: Datos y Origen de la Información, que documenta de manera
sistemática el mapeo de datos, su procedencia y las características
relevantes para evaluar riesgos de calidad y privacidad.

**Sección 4. Base Legal y Consentimiento**

Aquí se identifica la base jurídica que permite el tratamiento de los
datos, incluyendo si el sistema requiere o no consentimiento explícito
de los titulares. También se documentan los mecanismos de obtención del
consentimiento y las alternativas aplicables cuando este no es viable.\
La finalidad de esta sección es demostrar que el tratamiento de datos es
legítimo y compatible con la legislación vigente.

Generalmente la llena el área jurídica y el Delegado de Protección de
Datos. La Figura 18 presenta la estructura de la Sección 4: Base Legal y
Consentimiento, que registra de forma clara los soportes jurídicos del
tratamiento de datos y los mecanismos de consentimiento aplicables.

**Sección 5. Evaluación de Impactos en Derechos**
 
Esta sección analiza los posibles impactos del sistema sobre cuatro
derechos fundamentales:\
privacidad, igualdad, debido proceso y acceso a servicios públicos.

Para cada derecho se responde a una pregunta orientadora, se describe el
riesgo asociado, y se valora la probabilidad, el impacto y el nivel de
riesgo (bajo, medio o alto).

Es una de las secciones más importantes del DPIA, ya que determina si el
sistema puede afectar derechos fundamentales y si se requieren medidas
adicionales de mitigación.

La Figura 19 muestra la Sección 5: Evaluación de Impactos en Derechos,
donde se analiza de manera sistemática el efecto potencial del sistema
sobre derechos fundamentales como la privacidad, la igualdad, el debido
proceso y el acceso a servicios.
 
**Sección 6. Matriz de Riesgos Algorítmicos**
 
La matriz consolida los riesgos identificados y asigna una puntuación
basada en la probabilidad y el impacto. Cada riesgo se clasifica por
categoría (por ejemplo, privacidad, equidad o seguridad) y se registran
los controles existentes.

Esta sección facilita la priorización de riesgos y permite tomar
decisiones informadas sobre la viabilidad del sistema.

Es utilizada durante la revisión del Comité de IA. La Figura 20 ilustra
la Sección 6: Matriz de Riesgos Algorítmicos, una herramienta
estructurada para consolidar, evaluar y priorizar los riesgos
identificados durante el análisis.
 
**Sección 7. Medidas de Mitigación y Controles**
 
Una vez definidos los riesgos, en esta sección se especifican las
medidas para atenderlos: de qué tipo son (técnicas u organizativas),
quién es el responsable, en qué plazo se implementarán, cuál es su
indicador de cumplimiento y cuál es su estado actual.

Es, en la práctica, el plan de acción que la entidad debe seguir para
reducir los riesgos identificados.\
Se revisa y actualiza con periodicidad. La Figura 21 presenta la Sección
7: Medidas de Mitigación y Controles, donde se registra el plan de
acción específico para cada riesgo, incluyendo responsables, plazos e
indicadores de seguimiento.
 
**Sección 8. Supervisión Humana**
 
Esta sección define los mecanismos mediante los cuales los seres humanos
supervisarán y podrán intervenir en el funcionamiento del sistema.
Incluye los criterios de escalamiento, los roles responsables, la
frecuencia de revisión y los pasos a seguir en caso de desacuerdo entre
la decisión humana y la decisión del sistema.

Su propósito es asegurar que toda decisión automatizada esté respaldada
por supervisión humana efectiva.\
Corresponde al cumplimiento del principio de "intervención humana
significativa". La Figura 22 muestra la Sección 8: Supervisión Humana,
que documenta los protocolos y responsabilidades para garantizar una
supervisión humana efectiva y significativa sobre las decisiones
automatizadas.
 
**Sección 9. Monitoreo Continuo y KPI**
 
El monitoreo continuo recoge los indicadores con los que se evaluará
periódicamente el desempeño del sistema. Se definen las métricas, su
fórmula, el valor objetivo, el valor actual, la frecuencia de medición y
el responsable de cada una.

Permite identificar degradación del modelo (drift), cambios en los
datos, variaciones de desempeño y efectos no deseados. La Figura
23 ilustra la Sección 9: Monitoreo Continuo y KPI, que estructura el
plan de seguimiento mediante indicadores clave para evaluar el desempeño
y la estabilidad del sistema en operación.

**Sección 10. Comunicación y Transparencia**
 
Aquí se documentan los mecanismos para informar a los ciudadanos y los
usuarios del sistema acerca del uso de la inteligencia artificial, así
como los documentos publicados y los canales para consultas o reportes
de problemas.

La sección permite demostrar que la entidad cumple los principios de
transparencia y rendición de cuentas.\
Es especialmente importante cuando el sistema afecta a ciudadanos de
manera directa. La Figura 24 presenta la Sección 10: Comunicación y
Transparencia, que registra las estrategias y canales establecidos para
informar a los ciudadanos y garantizar la transparencia en el uso de
sistemas de IA.
 
**Sección 11. Auditoría y Actualizaciones**
 
Registra las auditorías internas o externas realizadas al sistema, su
alcance, frecuencia, fecha de próxima evaluación, responsables,
hallazgos y acciones correctivas.\
La finalidad es asegurar el seguimiento permanente del sistema y el
cumplimiento de las medidas de calidad y seguridad. La Figura 25 ilustra
la Sección 11: Auditoría y Actualizaciones, que documenta el programa de
auditorías, sus hallazgos y las acciones correctivas derivadas para
garantizar la mejora continua del sistema.
 
**Sección 12. Aprobaciones y Decisión Final**
 
Es la sección que formaliza la decisión institucional. Incluye la
evaluación del Delegado de Protección de Datos, del responsable técnico
y del área jurídica.

Finalmente, se consigna la decisión del Comité de IA, las condiciones
establecidas, la fecha de aprobación y la fecha programada para la
siguiente revisión.

Sin esta sección firmada, el sistema no debería entrar en operación.
La Figura 26 muestra la Sección 12: Aprobaciones y Decisión Final, que
consolida las validaciones institucionales requeridas y formaliza la
decisión de implementación del sistema.

**Importancia dentro del Framework**

Esta herramienta resulta esencial en el marco de gobernanza porque
permite cumplir con los requerimientos regulatorios colombianos, como la
Circular 002 y la Ley 1581, así como con estándares internacionales,
entre ellos el AI Act. Su implementación garantiza que los sistemas de
inteligencia artificial no vulneren derechos fundamentales, además de
proveer un marco unificado que evita la creación de formatos dispares
por parte de cada entidad. Asimismo, facilita la trazabilidad y la
auditoría del ciclo de vida algorítmico, aportando criterios objetivos
para aprobar o rechazar sistemas de IA en el sector público. De esta
manera, contribuye a reducir riesgos reputacionales y operativos
mediante la anticipación de posibles fallos.

Este instrumento constituye la pieza central del enfoque de gobernanza,
ya que articula de manera secuencial los componentes clave: datos,
modelos, riesgos, medidas de mitigación, supervisión, transparencia,
auditoría y aprobación final.
 
**¿Cómo se utiliza la plantilla?**
 
La plantilla está diseñada para aplicarse de forma secuencial y
colaborativa por diferentes áreas: técnica, jurídica, delegados de
protección de datos, comité de IA, equipos de datos y analítica, así
como equipos de TI y seguridad. El proceso de uso comprende las
siguientes etapas:

1.  El área técnica completa la descripción del sistema y los datos
    utilizados.

2.  El equipo jurídico valida la base legal y los mecanismos de
    consentimiento.

3.  El delegado de protección de datos analiza riesgos de privacidad y
    determina la necesidad de una evaluación completa (DPIA).

4.  El equipo multidisciplinario evalúa riesgos algorítmicos y llena la
    matriz correspondiente.

5.  Se documentan los controles y medidas de mitigación.

6.  Los equipos de TI y seguridad definen indicadores clave (KPIs) y
    procedimientos de monitoreo.

7.  Se establecen protocolos de transparencia y mecanismos de
    participación ciudadana.

8.  Auditoría revisa la consistencia del instrumento.

9.  Finalmente, el comité de IA toma la decisión de aprobación.

**¿Por qué es clave para el sector público?**
 
La ARA/DPIA proporciona transparencia algorítmica, responsabilidad
institucional y evidencia de cumplimiento normativo. Además, ofrece
protección jurídica tanto para la entidad como para los funcionarios,
asegura trazabilidad para auditorías internas y externas, y establece un
estándar unificado aplicable a todas las entidades del Distrito. En
síntesis, esta herramienta garantiza que ningún sistema de IA se
despliegue sin un análisis riguroso de riesgos y derechos.Conclusión

Esta plantilla se convierte en el instrumento rector de gobernanza de
IA, articulando datos, modelos, riesgos, legalidad, derechos
fundamentales y transparencia. Su diseño facilita la adopción del
framework por entidades con capacidades técnicas diversas y garantiza
alineación con los estándares nacionales e internacionales.

La plantilla se convierte en el instrumento rector de la gobernanza de
IA, articulando datos, modelos, riesgos, legalidad, derechos
fundamentales y transparencia. Su diseño facilita la adopción del
framework por entidades con capacidades técnicas diversas y asegura la
alineación con los estándares nacionales e internacionales.
 
### 4.2.4 Model Card
 
La Model Card es un instrumento estándar internacional que permite
documentar, de manera clara y estructurada, las características técnicas
y operativas de los modelos de inteligencia artificial utilizados por
una entidad pública. Originalmente propuesta por Google y actualmente
adoptada por gobiernos, organismos multilaterales y estándares como el
NIST AI RMF y la ISO/IEC 42001, su propósito es garantizar que un modelo
sea comprensible, auditable, explicable y supervisable a lo largo de su
ciclo de vida.

Dentro del framework de Gobernanza de IA del Distrito, la Model Card
cumple un rol central, ya que permite registrar información detallada
sobre el propósito del modelo, su arquitectura, los datos utilizados,
los riesgos identificados y los mecanismos de supervisión humana y
monitoreo continuo. Al consolidar esta información, la herramienta
facilita la trazabilidad del sistema, el reporte a los órganos de
control y la rendición de cuentas ante la ciudadanía.

**Alineación con la Circular 002 de la SIC**
 
La Circular 002 establece obligaciones específicas para las entidades
que implementan sistemas automatizados, entre las que se incluyen la
documentación de dichos sistemas, la identificación de riesgos, la
garantía de transparencia, la información clara al ciudadano sobre
decisiones automatizadas y la demostración de supervisión humana. En
este contexto, la *Model Card* constituye una herramienta que facilita
el cumplimiento de estas disposiciones, ya que describe el modelo,
explica su funcionamiento, documenta riesgos y sesgos, define los
mecanismos de supervisión y permite informar de manera clara a los
titulares de datos.
 
**Alineación con el CONPES 4144**
 
El documento CONPES 4144 establece lineamientos orientados a la
transparencia, la responsabilidad, la gestión de riesgos, la equidad y
la supervisión humana en el uso de tecnologías emergentes. La *Model
Card* se alinea con estos principios porque ofrece trazabilidad del
ciclo de vida del modelo, documenta métricas diferenciales para
garantizar equidad, identifica riesgos éticos, técnicos y sociales,
incorpora pautas para un uso responsable, describe mecanismos de
supervisión y control, y facilita tanto auditorías internas como
externas.
 
**Descripción de la estructura de la herramienta**
 
La herramienta está compuesta por catorce secciones diseñadas para
capturar información esencial que asegure transparencia, seguridad y uso
responsable del modelo. Cada sección cumple una función específica
orientada a documentar aspectos técnicos, operativos y éticos, lo que
permite una comprensión integral del sistema y su impacto. La Figura
27 presenta la estructura general y las catorce secciones que componen
la Model Card, herramienta estandarizada para documentar de manera
integral las características técnicas y operativas de un modelo de IA.

**Sección 1: Información general**
 
Incluye nombre, versión, entidad, área responsable, fecha de creación,
fecha de actualización y estado del ciclo de vida. Garantiza
trazabilidad documental. La Figura 28 ilustra la Sección 1: Información
General, que recopila los datos básicos de identificación y
administración del modelo, esenciales para su trazabilidad y gestión
documental.
 
**Sección 2: Propósito del modelo**
 
Describe el objetivo del modelo, su caso de uso, alcance, usuarios
previstos y procesos institucionales impactados. La Figura 29 presenta
la Sección 2: Propósito del Modelo, que documenta de manera clara los
objetivos, el alcance operativo y los impactos institucionales previstos
para el sistema de IA.
 
**Sección 3: Descripción técnica**
 
Define el tipo de modelo (clasificación, regresión, NLP, etc.), la
arquitectura, los algoritmos utilizados y las tecnologías empleadas.
La Figura 30 muestra la Sección 3: Descripción Técnica, que documenta
las características fundamentales de arquitectura, algoritmos y
tecnologías que componen el modelo de IA.
 
**Sección 4: Datos utilizados**
 
Resume los datasets de entrenamiento, validación y prueba. Incluye
referencias cruzadas al Data Sheet correspondiente. La Figura 31 ilustra
la Sección 4: Datos Utilizados, que documenta de manera organizada los
conjuntos de datos empleados en el desarrollo y evaluación del modelo,
asegurando trazabilidad con su documentación detallada.
 
**Sección 5: Métricas de desempeño**
 
Reporta métricas técnicas como precisión, recall, F1-score, AUC y
métricas desagregadas por subpoblaciones. Permite evaluar equidad.
La Figura 32 presenta la Sección 5: Métricas de Desempeño, que consolida
los resultados cuantitativos del modelo, incluyendo tanto métricas
globales como desgloses específicos para evaluar su rendimiento y
equidad.
 
**Sección 6: Evaluación de sesgos**
 
Identifica sesgos potenciales, resultados de pruebas diferenciales y
medidas aplicadas para mitigarlos. La Figura 33 ilustra la Sección 6:
Evaluación de Sesgos, que documenta los análisis realizados para
identificar sesgos potenciales y las medidas implementadas para promover
la equidad del modelo.
 
**Sección 7: Riesgos del modelo**
 
Clasifica riesgos técnicos, operativos, sociales y éticos asociados al
modelo y su implementación. La Figura 34 muestra la Sección 7: Riesgos
del Modelo, que sistematiza la identificación y clasificación de los
riesgos potenciales en diversas dimensiones, desde aspectos técnicos
hasta impactos sociales y éticos.
 
**Sección 8: Controles implementados**
 
Documenta medidas técnicas y organizacionales, tales como validación
humana, monitoreo, auditorías y alertas. La Figura 35 presenta la
Sección 8: Controles Implementados, que registra las salvaguardas
técnicas y organizativas establecidas para gestionar los riesgos
identificados y asegurar la operación responsable del modelo.
 
**Sección 9: Explicabilidad y transparencia**
 
Describe técnicas de explicabilidad (SHAP, LIME, análisis de
características, etc.), información pública y mecanismos de rendición de
cuentas. La Figura 36 muestra la Sección 9: Explicabilidad y
Transparencia, que documenta los métodos empleados para hacer
comprensible el funcionamiento del modelo y los mecanismos establecidos
para garantizar la transparencia ante usuarios y auditores.
 
**Sección 10: Reglas de uso responsable**
 
Define usos permitidos, usos restringidos, escenarios prohibidos y
buenas prácticas operativas. La Figura 37 ilustra la Sección 10: Reglas
de Uso Responsable, que establece los límites operativos y éticos del
modelo, especificando claramente los contextos de uso aprobados,
restringidos y prohibidos.
 
**Sección 11: Entradas y salidas del modelo**
 
Especifica los tipos de datos aceptados por el modelo y el tipo de
predicciones generadas. La Figura 38 presenta la Sección 11: Entradas y
Salidas del Modelo, que documenta las interfaces de datos del sistema,
definiendo claramente qué información requiere para operar y qué tipo de
resultados produce.
 
**Sección 12: Monitoreo y mantenimiento**
 
Indica la frecuencia de reentrenamiento, KPIs de calidad, métodos de
detección de drift y responsables del monitoreo. La Figura 39 muestra la
Sección 12: Monitoreo y Mantenimiento, que establece el plan de
vigilancia continua y las actividades de sostenimiento necesarias para
garantizar el desempeño y la vigencia del modelo a lo largo de su ciclo
de vida.
 
**Sección 13: Historial de cambios**
 
Registra modificaciones, fechas, responsables y justificaciones.
La Figura 40 presenta la Sección 13: Historial de Cambios, que documenta
de manera cronológica todas las modificaciones realizadas al modelo, su
documentación o sus parámetros, asegurando una trazabilidad completa de
su evolución.
 
**Sección 14: Aprobaciones**
 
Incluye la validación del área técnica, jurídica, Delegado de Protección
de Datos y Comité Distrital de IA. La Figura 41 ilustra la Sección 14:
Aprobaciones, que consolida las firmas y validaciones institucionales
requeridas para formalizar la implementación y el uso del modelo de IA,
cerrando el ciclo de gobernanza documental.
 
**Importancia dentro del framework**
 
La herramienta adquiere un papel esencial en el marco de gobernanza de
modelos de inteligencia artificial, ya que contribuye a evitar el uso de
sistemas como "cajas negras", lo que incrementa la transparencia y la
comprensión del proceso decisional. Además, facilita auditorías del
sistema, reduce riesgos asociados a prácticas discriminatorias,
documenta el cumplimiento normativo, y permite una supervisión humana
efectiva en todas las etapas del ciclo de vida del modelo. De igual
manera, protege a poblaciones vulnerables mediante la identificación
temprana de sesgos, genera confianza ciudadana al garantizar procesos
claros y verificables, y asegura la transparencia institucional frente a
actores internos y externos. En síntesis, la *Model Card* se configura
como la pieza clave para que el Distrito pueda operar modelos de IA de
manera segura, ética y responsable, alineándose con los principios de
gobernanza tecnológica contemporánea (CONPES, 2022; SIC, 2023).

### 4.2.5 Data Sheet
 
El *Data Sheet* constituye un instrumento de documentación diseñado para
describir de manera exhaustiva las características, la calidad, el
origen, la composición, los riesgos y las limitaciones del conjunto de
datos utilizado para entrenar, validar o ejecutar un sistema de
inteligencia artificial. Su propósito principal es garantizar que las
entidades públicas comprendan el funcionamiento, la procedencia y las
implicaciones del dataset antes de su incorporación en cualquier proceso
automatizado. Esta herramienta, propuesta inicialmente por
investigadores del MIT como un estándar para la transparencia de datos
(Gebru et al., 2018), se ha consolidado como un componente esencial
dentro de los marcos de gobernanza y en regulaciones internacionales,
tales como el *NIST AI RMF*, las normas ISO/IEC 25012 e ISO/IEC 5259,
así como en diversas políticas públicas de IA. En el contexto del
Distrito, el *Data Sheet* asegura que los datos utilizados sean
confiables, legales, representativos y compatibles con criterios éticos
y de protección de derechos fundamentales.
 
**Alineación con la Circular 002 de la SIC**
 
La Circular 002 establece que cualquier entidad que procese datos debe
documentar su origen, registrar su finalidad, evaluar riesgos sobre los
titulares, identificar datos personales y sensibles, y definir medidas
de seguridad y minimización (Superintendencia de Industria y Comercio
\[SIC\], 2023). El *Data Sheet* se ajusta plenamente a estos
requerimientos, ya que documenta el flujo de datos y su procedencia,
justifica la base legal del tratamiento, identifica datos sensibles y su
necesidad, evalúa riesgos para los titulares, registra controles de
seguridad y permite auditorías sobre el uso del dataset. Por ello, se
convierte en una herramienta indispensable para demostrar el
cumplimiento normativo ante la SIC.
 
**Alineación con el CONPES 4144**
 
El CONPES 4144 establece que los sistemas de IA en el país deben
garantizar gobernanza de datos, trazabilidad del ciclo de vida,
identificación de sesgos, transparencia en los procesos, uso
responsable, protección de derechos fundamentales y mitigación de
riesgos (Departamento Nacional de Planeación \[DNP\], 2022). El *Data
Sheet* responde directamente a estos lineamientos porque documenta la
calidad, representatividad y sesgos del conjunto de datos, permite
identificar discriminación estructural, facilita la trazabilidad
completa del dataset, registra transformaciones, limpieza y medidas de
seguridad, define usos permitidos e indebidos, y evalúa riesgos éticos y
sociales. En consecuencia, se configura como la "hoja de vida" del
dataset y como un mecanismo de control esencial dentro del framework de
gobernanza. La Figura 42 presenta la estructura general del Data Sheet,
herramienta estandarizada para documentar exhaustivamente las
características, origen, calidad y riesgos de los conjuntos de datos
utilizados en sistemas de IA.
 
**Descripción y estructura de la herramienta**
 
La herramienta se organiza en trece secciones que documentan los
componentes esenciales del dataset:

**Sección 1: Información general del dataset**
 
Incluye nombre, entidad propietaria, área responsable, versión, fecha de
creación/actualización y contacto institucional. Permite trazabilidad
administrativa. La Figura 43 presenta la Sección 1: Información General
del Dataset, que recopila los datos básicos de identificación y gestión
administrativa del conjunto de datos, fundamentales para su trazabilidad
y referencia institucional.
 
**Sección 2: Descripción y propósito**
 
Explica qué contiene el dataset y cuál es su finalidad dentro del
proceso institucional o servicio público que soporta.

**Sección 3: Origen y método de recolección**
 
Describe las fuentes (sistemas internos, sensores, encuestas, terceros
autorizados), la metodología de captura y la frecuencia de
actualización. La Figura 44 muestra la Sección 2: Descripción y
Propósito, que define de manera clara el contenido del conjunto de datos
y su función específica dentro de los procesos o servicios públicos que
utiliza.
 
**Sección 4: Composición del dataset**
 
Incluye número de registros, número de variables, tipos de datos,
descripción del diccionario de datos y representatividad poblacional.
La Figura 45 ilustra la Sección 4: Composición del Dataset, que
documenta las características estructurales y estadísticas fundamentales
del conjunto de datos, proporcionando una visión clara de su escala y
diversidad.
 
**Sección 5: Presencia de datos personales y sensibles**
 
Clasifica los datos en personales, sensibles o no personales, justifica
su uso y especifica la base legal del tratamiento. La Figura 46 presenta
la Sección 5: Presencia de Datos Personales y Sensibles, que evalúa y
documenta la naturaleza de la información contenida en el dataset,
asegurando el cumplimiento de la normativa de protección de datos
personales y sensibles.
 
**Sección 6: Calidad del dataset**
 
Evalúa datos faltantes, inconsistencias, duplicados, procesos de
limpieza, técnicas de validación y estándares de calidad aplicados.
La Figura 47 muestra la Sección 6: Calidad del Dataset, que sistematiza
la evaluación de la integridad, consistencia y confiabilidad de los
datos mediante métricas y procesos documentados de limpieza y
validación.
 
**Sección 7: Evaluación de sesgos y representatividad**
 
Analiza sesgos potenciales, distribución de variables sensibles y
riesgos para poblaciones vulnerables. La Figura 48 presenta la Sección
7: Evaluación de Sesgos y Representatividad, que documenta los análisis
realizados para identificar posibles desbalances, subrepresentaciones o
sesgos sistemáticos en el conjunto de datos que puedan afectar la
equidad de los modelos.
 
**Sección 8: Procesamiento y transformaciones aplicadas**
 
Documenta normalización, imputación, balanceo, anonimización o cualquier
operación realizada sobre los datos. La Figura 49 ilustra la Sección 8:
Procesamiento y Transformaciones Aplicadas, que registra de manera
detallada las operaciones de preparación, limpieza y transformación
ejecutadas sobre los datos antes de su uso en modelos de IA.
 
**Sección 9: Riesgos éticos y legales**
 
Identifica riesgos de discriminación, reidentificación, uso indebido,
sesgos estructurales y vulneración de derechos. La Figura 50 presenta la
Sección 9: Riesgos Éticos y Legales, que sistematiza la identificación
de amenazas potenciales relacionadas con el uso del conjunto de datos,
desde perspectivas tanto éticas como de cumplimiento normativo.
 
**Sección 10: Uso permitido y no permitido**
 
Establece condiciones de uso, finalidades autorizadas, limitaciones y
restricciones de acceso. La Figura 51 presenta la Sección 10: Uso
Permitido y No Permitido, que define claramente los límites operativos y
éticos del conjunto de datos, especificando los contextos de uso
aprobados y aquellos expresamente prohibidos.
 
**Sección 11: Seguridad del dataset**
 
Incluye medidas de cifrado, accesos permitidos, políticas de custodia y
controles de seguridad. La Figura 52 presenta la Sección 11: Seguridad
del Dataset, que documenta las salvaguardas técnicas y organizativas
implementadas para proteger la integridad, confidencialidad y
disponibilidad del conjunto de datos.
 
**Sección 12: Historial del dataset**
 
Registra versiones, cambios realizados, fecha de modificación y
responsable del ajuste. La Figura 53 ilustra la Sección 12: Historial
del Dataset, que mantiene un registro cronológico de todas las
modificaciones y actualizaciones realizadas al conjunto de datos,
garantizando trazabilidad completa de su evolución.
 
**Sección 13: Aprobaciones institucionales**
 
Incluye validación del equipo de datos, área jurídica y Comité Distrital
de IA. La Figura 54 presenta la Sección 13: Aprobaciones
Institucionales, que consolida las validaciones requeridas de los
diferentes actores responsables, formalizando la aprobación del conjunto
de datos para su uso en sistemas de IA.
 
**Importancia dentro del framework**
 
El *Data Sheet* desempeña un papel esencial en el marco de gobernanza de
inteligencia artificial, ya que contribuye a eliminar la opacidad en la
recolección y manipulación de datos, previene que los modelos se
entrenen sobre información discriminatoria y permite la realización de
auditorías tanto internas como externas. Además, garantiza el
cumplimiento legal, protege a los ciudadanos y a las poblaciones
vulnerables, facilita la rendición de cuentas y estandariza los procesos
relacionados con la calidad y la gobernanza de datos. Junto con el
Diccionario de Datos y la *Model Card*, conforma un sistema integral
orientado a la transparencia algorítmica, lo que refuerza la confianza
institucional y asegura la trazabilidad en todo el ciclo de vida del
modelo.

### 4.2.6 Checklist de Evaluación de Proveedores de IA
 
El presente Checklist constituye una herramienta operativa fundamental
del Framework de Gobernanza de IA, diseñada para estandarizar y
robustecer los procesos de selección y contratación de proveedores de
sistemas de inteligencia artificial en el Distrito Capital. Su función
principal es servir como instrumento de debida diligencia, permitiendo a
las entidades públicas evaluar de manera objetiva, sistemática y
proporcional al riesgo, la capacidad de un proveedor para cumplir con
los requisitos normativos, técnicos y éticos establecidos. El checklist
evalúa integralmente siete dimensiones críticas: 1) la conformidad con
el marco regulatorio colombiano (Ley 1581 de 2012, CONPES 4144) y la
gobernanza interna del proveedor; 2) la transparencia y documentación
técnica de los modelos y datos; 3) las garantías de privacidad y
protección de datos personales; 4) la seguridad, robustez y resiliencia
de los sistemas; 5) las capacidades de auditoría y rendición de cuentas;
6) la calidad del servicio y el soporte técnico; y 7) la sostenibilidad
de la solución. Al aplicar este instrumento, las entidades no solo
mitigan riesgos legales, reputacionales y operativos, sino que también
fomentan un mercado de proveedores más maduro y alineado con los
principios de una IA responsable en el sector público. Como se visualiza
en la **Figura 54**, el checklist evalúa integralmente siete dimensiones
críticas. En lugar de un instrumento único y masivo, proponemos **tres
versiones** adaptadas al nivel de riesgo.

En lugar de un checklist único y masivo, proponemos **tres versiones**:

**Checklist Básico (Para Riesgo Mínimo/Limitado):** 15 criterios
críticos. Enfocado en privacidad (Ley 1581), seguridad básica y
funcionalidad. Se aplica en procesos de menor cuantía o para
herramientas de productividad interna.
 
**Checklist Estándar (Para Riesgo Alto):** El checklist actual, pero
rationalizado a \~25 criterios. Es la versión completa que se incluiría
en pliegos tipo para la mayoría de licitaciones públicas.
 
**Checklist Reforzado (Para Riesgo Inaceptable o Crítico):** El
checklist estándar + criterios adicionales de auditoría profunda,
pruebas de estrés ético específicas y cláusulas contractuales
excepcionales (ej.: para sistemas de biometría o salud).

**Esto reduce la carga administrativa donde el riesgo lo permite.**
 
**Instrucciones Generales:**

**Seleccione el Nivel de Checklist** según la clasificación de riesgo
del caso de uso:

**BÁSICO:** Para sistemas de **Riesgo Mínimo o Limitado** (ej.: chatbots
informativos, herramientas de productividad interna).

**ESTÁNDAR:** Para sistemas de **Alto Riesgo** (ej.: priorización de
trámites, evaluación de beneficiarios, sistemas de recomendación que
afecten acceso a servicios). *Este es el checklist por defecto para la
mayoría de licitaciones.*

**REFORZADO:** Para sistemas de **Riesgo Inaceptable o Crítico** (ej.:
biometría, sistemas de salud, puntuación social). Incluye todos los
criterios del Estándar más requisitos excepcionales.

**Para cada criterio**, marque la opción que mejor describa la evidencia
presentada por el proveedor. Utilice la columna \"Evidencia/Referencia\"
para anotar el documento o sección específica que respalda su
evaluación. La Figura 55 presenta la estructura general del Checklist de
Evaluación de Proveedores de IA, herramienta diseñada para estandarizar
la evaluación de proveedores según su nivel de riesgo y capacidad de
cumplimiento.
 
**Sección 1: Conformidad Regulatoria Y Gobernanza (Peso: 25%)**

Esta sección evalúa el grado en que el proveedor cumple con las
regulaciones colombianas de protección de datos establecidas en la Ley
1581, así como la existencia de políticas formales orientadas a una
inteligencia artificial responsable. También considera la implementación
de sistemas de gestión de IA, como la norma ISO/IEC 42001, y la adopción
de procesos sistemáticos para identificar y gestionar riesgos asociados
al uso de inteligencia artificial.

**Tabla 4. Checklist Evaluación Proveedores: Sección 1**
 
| ID | Criterio | 0 - No Cumple | 1 - Cumple Parcialmente | 2 - Cumple Plenamente | Puntuación | Evidencia |
|:---|:---|:---|:---|:---|:---:|:---|
| 1.1 | **Conformidad con marco regulatorio colombiano** | No tiene política de privacidad | Política básica no alineada | Política robusta y alineada con Ley 1581 | | |
| 1.2 | **Política de IA Responsable o Ética** | No tiene política documentada | Borrador o política interna no formal | Política pública formal y referenciable | | |
| 1.3 | **Sistema de Gestión de IA (AIMS)** | No tiene sistema de gestión | Elementos de un sistema pero no formalizado | Sistema documentado e implementado (ej. ISO/IEC 42001) | | |
| 1.4 | **Gestión de Riesgos de IA** | No tiene proceso definido | Evaluaciones de riesgo ad-hoc | Proceso sistemático y documentado | | |

Fuente: Elaboración Propia
 
**Sección 2: Documentación Y Transparencia Técnica (Peso: 20%)**

Se verifica que el proveedor proporcione documentación técnica completa,
incluyendo Model Cards que describen métricas y limitaciones del modelo
y Data Sheets con información detallada sobre los datos de
entrenamiento. Además, se exige documentación auditable que permita
comprender la arquitectura del sistema, los hiperparámetros utilizados y
las decisiones clave en el diseño.

**Tabla 5. Checklist Evaluación Proveedores: Sección 2**
 
| ID | Criterio | 0 - No Cumple | 1 - Cumple Parcialmente | 2 - Cumple Plenamente | Puntuación | Evidencia |
|:---|:---|:---|:---|:---|:---:|:---|
| 2.1 | **Model Card (Ficha del Modelo)** | No proporciona Model Card | Model Card básico, falta info clave | Model Card completo | | |
| 2.2 | **Data Sheet (Ficha de Datos)** | No proporciona Data Sheet | Descripción básica de datos | Data Sheet detallado | | |
| 2.3 | **Documentación Técnica para Auditoría** | No proporciona documentación | Documentación superficial | Documentación detallada y bitácoras | | |

Fuente: Elaboración Propia
 
**Sección 3: Privacidad Y Protección De Datos (Peso: 20%)**

En esta sección se examina la claridad contractual respecto a la
titularidad de los datos, la existencia de acuerdos sólidos de
procesamiento (DPA) alineados con la Ley 1581 y los procedimientos que
garantizan el ejercicio de derechos de habeas data, como acceso,
rectificación y supresión. También se revisan las políticas específicas
de retención y eliminación de información.

**Tabla 6. Checklist Evaluación Proveedores: Sección 3**
 
| ID | Criterio | 0 - No Cumple | 1 - Cumple Parcialmente | 2 - Cumple Plenamente | Puntuación | Evidencia |
|:---|:---|:---|:---|:---|:---:|:---|
| 3.1 | **Claridad sobre Titularidad de Datos** | No hay claridad contractual | Titularidad definida con ambigüedades | Contrato define claramente la titularidad | | |
| 3.2 | **Data Processing Agreement (DPA)** | No ofrece un DPA | DPA básico que requiere ajustes | DPA robusto y alineado con Ley 1581 | | |
| 3.3 | **Gestión de Derechos de los Titulares** | No tiene procedimientos | Procedimientos manuales o lentos | Procedimientos eficientes y canales claros | | |
| 3.4 | **Políticas de Retención y Borrado de Datos** | No tiene políticas definidas | Políticas genéricas | Políticas específicas y alineadas | | |

Fuente: Elaboración Propia
 
**Sección 4: Seguridad Y Robustez (Peso: 20%)**

Se evalúa la vigencia de certificaciones de seguridad como ISO 27001 y
SOC 2, la realización de pruebas de robustez frente a ataques
adversarios y datos fuera de distribución, así como la existencia de
protocolos actualizados y comprobados para responder ante incidentes de
seguridad.

**Tabla 7. Checklist Evaluación Proveedores: Sección 4**
 
| ID | Criterio | 0 - No Cumple | 1 - Cumple Parcialmente | 2 - Cumple Plenamente | Puntuación | Evidencia |
|:---|:---|:---|:---|:---|:---:|:---|
| 4.1 | **Certificaciones de Seguridad** | No tiene certificaciones | Certificaciones básicas o con hallazgos | ISO 27001 o equivalente vigente | | |
| 4.2 | **Pruebas de Robustez y Seguridad de IA** | No ha realizado pruebas de robustez | Pruebas básicas de rendimiento | Pruebas de robustez y seguridad con resultados | | |
| 4.3 | **Respuesta a Incidentes de Seguridad** | No tiene protocolo documentado | Protocolo básico no probado | Protocolo completo, actualizado y probado | | |

Fuente: Elaboración Propia
 
**Sección 5: Auditoría Y Rendición De Cuentas (Peso: 10%)**

Esta sección verifica que el proveedor acepte cláusulas contractuales
que otorguen derecho a auditoría con acceso completo a documentación y
evidencias. Asimismo, se exige la implementación de sistemas de
trazabilidad que incluyan registros comprensivos e inmutables de todas
las decisiones tomadas por el sistema de IA.

**Tabla 8. Checklist Evaluación Proveedores: Sección 5**
 
| ID | Criterio | 0 - No Cumple | 1 - Cumple Parcialmente | 2 - Cumple Plenamente | Puntuación | Evidencia |
|:---|:---|:---|:---|:---|:---:|:---|
| 5.1 | **Derecho a Auditoría** | Se niega a incluir cláusulas de auditoría | Acepta auditorías con limitaciones | Acepta cláusulas de derecho a auditoría | | |
| 5.2 | **Trazabilidad de Decisiones** | No registra logs o son insuficientes | Registra logs básicos | Registra logs comprehensivos e inmutables | | |

Fuente: Elaboración Propia
 
**Sección 6: Calidad Del Servicio Y Soporte (Peso: 15%)**

Finalmente, se revisa la existencia de acuerdos de nivel de servicio
(SLA) robustos, con métricas cuantificables y penalizaciones claras, la
disponibilidad de soporte técnico prioritario y planes de transferencia
de conocimiento. También se considera la transparencia en el roadmap,
incluyendo la notificación anticipada de cambios significativos.

**Tabla 9. Checklist Evaluación Proveedores: Sección 6**
 
| ID | Criterio | 0 - No Cumple | 1 - Cumple Parcialmente | 2 - Cumple Plenamente | Puntuación | Evidencia |
|:---|:---|:---|:---|:---|:---:|:---|
| 6.1 | **Acuerdos de Nivel de Servicio (SLA)** | No ofrece SLA cuantificables | SLA con métricas básicas sin penalizaciones | SLA robustos con métricas y compensaciones | | |
| 6.2 | **Soporte Técnico y Transferencia de Conocimiento** | No ofrece plan de soporte | Soporte estándar y documentación básica | Soporte prioritario y plan de transferencia | | |
| 6.3 | **Gestión de Cambios y Roadmap** | No comparte roadmap | Roadmap de alto nivel | Roadmap detallado y notificaciones >30 días | | |

Fuente: Elaboración Propia
 
**Informe Final De Evaluación**

El informe final de evaluación resume la revisión integral del proveedor
en relación con criterios regulatorios, técnicos y contractuales,
verificando el cumplimiento obligatorio de la Ley 1581, la capacidad de
suscribir acuerdos de procesamiento de datos (DPA), la existencia de
certificaciones de seguridad y la oferta de SLA con métricas claras. Con
base en la puntuación ponderada y la verificación de estos requisitos,
se determina si el proveedor es recomendado, recomendado con condiciones
o no recomendado, incorporando observaciones finales y la validación por
parte del responsable técnico, el área jurídica y el comité de IA.
La Figura 55 presenta la estructura general del Checklist de Evaluación
de Proveedores de IA, herramienta diseñada para estandarizar la
evaluación de proveedores según su nivel de riesgo y capacidad de
cumplimiento.
 
### 4.2.7 Guía de Uso Interno de IA Generativa
 
La presente Guía Institucional de Uso Interno de IA Generativa establece
los lineamientos, responsabilidades y protocolos necesarios para
garantizar un uso seguro, ético y jurídicamente adecuado de las
herramientas de inteligencia artificial generativa en las entidades
públicas del Distrito Capital. Su propósito es ofrecer un marco claro y
práctico que permita aprovechar los beneficios de estas tecnologías
emergentes sin comprometer la protección de datos personales, la
integridad institucional, la transparencia administrativa ni los
derechos de la ciudadanía. Dado el acelerado avance de la GenAI y su
creciente incorporación en el mapa de procesos misionales, estratégicos
y de apoyo, esta guía se configura como un instrumento esencial para
orientar su adopción responsable, alineado con la normativa colombiana
vigente, las capacidades actuales del Distrito y las mejores prácticas
internacionales adaptadas al contexto local.
 
#### Principales riesgos asociados al uso de IA Generativa en el sector público
 
Los sistemas de IA generativa presentan riesgos relevantes que deben
gestionarse antes, durante y después de su uso institucional. Los
principales riesgos identificados son:

**Errores formales:** La IA puede generar información incorrecta o
inventada, lo cual puede afectar decisiones administrativas,
comunicaciones oficiales o análisis para políticas públicas.

**Riesgos de privacidad:** Si el funcionario ingresa datos personales,
reservados o clasificados, existe riesgo de filtración, tratamiento
indebido o uso no autorizado. Esto puede constituir vulneración de la
Ley 1581 de 2012.

**Sesgos y discriminación:** Los modelos pueden reproducir sesgos
históricos, afectando grupos vulnerables. Esto es especialmente crítico
en entidades que atienden poblaciones específicas (niñez, mujeres,
migrantes, personas mayores).

**Dependencia tecnológica de proveedores privados:** Puede generarse
dependencia excesiva de plataformas de terceros, afectando la soberanía
tecnológica y continuidad del servicio.

**Riesgos reputacionales:** La generación de textos erróneos,
inadecuados o discriminatorios puede comprometer la imagen
institucional.

**Automatización sin supervisión:** La ejecución automática de
decisiones sin intervención humana puede generar fallas graves en
trámites y servicios públicos.
 
#### Tipología de casos de uso relevantes en el Distrito Capital
 
En la Tabla 10 se presentan casos de uso iniciales y acotados, ajustados
al contexto distrital:
 
**Tabla 10. Guia de Uso Interno IA: Tipología de Casos de Uso Relevantes**
 
| Entidad / Dependencia | Caso de Uso Permitido | Nivel de Riesgo | Condiciones de Uso |
| :--- | :--- | :--- | :--- |
| Secretaría General | Redacción de borradores de documentos no sensibles | Bajo | Supervisión humana obligatoria |
| Sector Gobierno | Resúmenes preliminares de normativa o jurisprudencia | Bajo/Medio | Verificación jurídica posterior |
| DTI Distrital | Automatización de reportes técnicos o analíticos | Medio | Validación de datos por expertos |
| Secretaría de Salud | Guías informativas al ciudadano | Bajo | No ingresar datos clínicos ni reservados |
| Secretaría de Movilidad | Chatbots informativos de normas y servicios | Medio/Alto | Pruebas piloto + Comité de IA |
| Uaesp / Ambiente | Análisis preliminar de datos abiertos | Bajo | Solo usar datos públicos |
| Jurídica Distrital | Borradores de conceptos no vinculantes | Bajo | Revisión posterior por abogado |

Fuente: Elaboración Propia
 
#### Obligaciones mínimas del proveedor de IA generativa
 
Para plataformas internas o de terceros aplican los siguientes
requisitos mínimos:

**Protección de datos (Ley 1581)**

Prohibición contractual de almacenar prompts con datos personales.

Prohibición de entrenar modelos con información del Distrito.

Garantía de ubicación de datos en jurisdicciones compatibles (no exige
nube nacional, pero sí cumplimiento estricto).

**Seguridad**

Medidas razonables equivalentes a controles ISO 27001 (sin exigir
certificación).

Reporte de incidentes de seguridad en máximo 72 horas.

**Transparencia y trazabilidad**

Registro básico de versiones y actualizaciones.

Descripción clara de limitaciones y alcances de la herramienta.

**Condiciones contractuales**

Prohibición de reutilizar información institucional.

Cláusula de confidencialidad reforzada para datos sensibles.

Destrucción de datos una vez finalice el contrato.

#### Matriz simplificada de clasificación de riesgos en casos de uso de GenAI
 
La siguiente matriz permite clasificar rápidamente el nivel de riesgo
del caso de uso:
 
**Tabla 11. Guía de Uso Interno IA: Matriz de Clasificación de Riesgos**
 
| Nivel de Riesgo | Características | Requisitos |
| :--- | :--- | :--- |
| Bajo | Borradores, textos no sensibles, información pública | Supervisión humana |
| Medio | Trámites administrativos, datos semisensibles | Validación técnica + supervisor |
| Alto | Impacto sobre derechos ciudadanos, automatización | Piloto + Aprobación Comité IA |
| Muy Alto | Datos personales sensibles, decisiones automáticas, impacto jurídico | Prohibido |

Fuente: Elaboración Propia

Este cuadro permite que cualquier entidad evalúe rápidamente si un uso
está permitido, condicionado o prohibido.
 
#### Procedimiento de respuesta ante incidentes
 
En caso de presentarse un incidente relacionado con el uso de IA
generativa, se aplicarán las siguientes acciones según la naturaleza del
evento. Si se ingresó información personal por error, se debe cerrar
inmediatamente el prompt, reportar el hecho al Delegado de Protección de
Datos (DPO), registrar el incidente en el sistema interno y evaluar la
necesidad de notificar al titular del dato. Posteriormente, el Comité de
IA revisará el caso y emitirá las recomendaciones correspondientes.

Cuando la IA genere contenido inapropiado, no se debe copiar ni
distribuir dicho material. Es necesario registrar una captura interna
como evidencia, reportar el incidente al Comité de IA y proceder a
ajustar las configuraciones o bloquear temporalmente la herramienta para
prevenir recurrencias.

Finalmente, si se detecta un error grave o una alucinación en la salida
generada, esta no debe ser utilizada bajo ninguna circunstancia. El
hecho debe reportarse al supervisor o líder del proceso y documentarse
adecuadamente para fortalecer el protocolo y evitar futuros incidentes.
Como se especifica en la Figura 56 se puede identificar el procedimiento
de respuesta ante incidentes.

#### **Programa obligatorio de capacitación**
 
Para acceder a las herramientas de IA generativa será indispensable
completar un programa de formación orientado a garantizar un uso seguro
y responsable. Este programa incluye contenidos mínimos obligatorios,
impartidos en sesiones presenciales o virtuales sincrónicas, con una
duración total de cuatro horas. Los módulos se distribuyen de la
siguiente manera: el primero aborda los riesgos asociados a la IA
generativa, como alucinaciones, sesgos y aspectos de privacidad, durante
una hora; el segundo se centra en la normativa aplicable, incluyendo la
Ley 1581, la Ley 2279 y las políticas institucionales, también con una
hora de duración; el tercero desarrolla la matriz de usos permitidos y
prohibidos mediante casos prácticos, en una sesión de hora y media;
finalmente, el cuarto módulo explica el protocolo de respuesta ante
incidentes en treinta minutos.

Para obtener la certificación será necesario aprobar una evaluación con
un puntaje mínimo del 80 %. La vigencia de la certificación será de doce
meses, considerando la rápida evolución de la tecnología, y se exigirá
una re-certificación cada vez que se produzcan actualizaciones
normativas significativas.

La implementación se realizará de manera escalonada. En la primera fase,
durante los tres primeros meses, se capacitará a los miembros del Comité
de IA, al Delegado de Protección de Datos (DPO) y a los responsables
técnicos. La segunda fase, entre los meses cuatro y seis, estará
dirigida a funcionarios de áreas estratégicas y misionales. Finalmente,
la tercera fase, que abarcará del mes siete al doce, garantizará la
cobertura completa para todos los funcionarios usuarios.

El control de cumplimiento se efectuará mediante el sistema de acceso a
las herramientas institucionales de IA generativa, que verificará
automáticamente la vigencia de la certificación. En caso de no contar
con ella, el acceso será suspendido. La responsabilidad de este programa
recaerá en el Oficial de IA Responsable, en coordinación con el área de
Gestión Humana.

En conjunto, la Guía Institucional de Uso Interno de IA Generativa
constituye un instrumento estructural que habilita una adopción
responsable, progresiva y segura de estas tecnologías dentro del
Distrito Capital. Más que un documento normativo, es un mecanismo de
gestión del cambio que articula la protección de derechos, la eficiencia
administrativa y la innovación pública. Su diseño flexible permite
actualizar fácilmente los lineamientos conforme evolucione la regulación
nacional y las capacidades institucionales, consolidando al Distrito
como referente nacional en prácticas de IA responsable.
