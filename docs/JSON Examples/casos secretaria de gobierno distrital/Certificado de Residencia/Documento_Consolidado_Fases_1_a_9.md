# Documento Consolidado de Implementación del Ciclo de Vida de Gobernanza de IA
## Caso de Uso: Sistema Automatizado de Validación y Expedición de Certificados de Residencia

Este documento consolida la simulación de ejecución de las 9 fases del Ciclo de Vida de Gobernanza de IA para el proyecto de Certificado de Residencia de la Secretaría de Gobierno del Distrito Capital.

---

# Simulación de Ejecución: Fase 1 - Intake y AI Use-Case Canvas
## Caso de Uso: Sistema Automatizado de Validación y Expedición de Certificados de Residencia

Este documento simula la ejecución de la **Fase 1** del Ciclo de Vida de Gobernanza de IA, siguiendo los lineamientos del *Framework de Gobernanza de IA del Distrito* y basado en la información del **AI Use-Case Canvas**.

---

### 1. Contexto de la Iniciativa

*   **Entidad:** Secretaría de Gobierno del Distrito Capital.
*   **Sponsor de Negocio:** Director de Atención al Ciudadano / Product Owner.
*   **Responsable Técnico:** Líder de Desarrollo e Innovación / Equipo TIC.
*   **Fecha de Solicitud:** 26/11/2025 - v1.0.

---

### 2. Actividad 1: Completar AI Use-Case Canvas

El Sponsor de Negocio ha liderado la creación de la propuesta, documentando las dimensiones clave del proyecto en la herramienta **AI Use-Case Canvas**.

#### A. Definición del Problema y Objetivos
*   **Problema a Resolver:** El proceso actual implica una validación manual de documentos que genera tiempos de espera de hasta 24 horas, depende de la capacidad humana limitada y horarios de oficina, y presenta riesgos de error en la subsanación.
*   **Propósito del Sistema:** Automatizar la clasificación y validación de documentos (Cédula y Recibos) mediante IA para emitir el certificado de forma inmediata y disponible 24/7.
*   **Métricas de Éxito Esperadas:**
    *   Reducción del 95% en el tiempo de expedición (de 24h a minutos).
    *   Aumento del 23% en la satisfacción ciudadana (CSAT).
    *   Disponibilidad del servicio 24/7.

#### B. Actores y Datos
*   **Usuarios:** Ciudadanos solicitantes del certificado (población general de Bogotá).
*   **Perfil:** Heterogéneo, con niveles variados de alfabetización digital y acceso a dispositivos de diferente calidad.
*   **Datos Requeridos:** Imágenes o PDFs cargados por el ciudadano (Documento de Identidad, Recibo de Servicio Público).
*   **Categoría de Datos:** Personales (nombres, direcciones, número de documento de identidad).

#### C. Identificación Preliminar de Riesgos
Se han identificado riesgos tempranos que activan principios de gobernanza:
*   **Equidad:** Riesgo de sesgo técnico (OCR) que falle más con documentos de baja calidad, discriminando a ciudadanos con menor acceso a tecnología.
*   **Privacidad:** Exposición de datos personales si la seguridad en el manejo de los archivos temporales es débil.
*   **Operativos:** Sobrecarga del personal humano si la tasa de derivación de casos es muy alta.

---

### 3. Actividad 2: Valoración de Viabilidad

El borrador del canvas fue sometido a un "filtro de viabilidad" por los roles clave:

*   **Responsable Técnico:** Confirma la viabilidad técnica de la solución (OCR/NLP) y establece KPIs técnicos (Precisión ≥ 98%).
*   **Área Jurídica:** Valida la base legal (Ejercicio de funciones públicas y simplificación de trámites) y la conformidad con la Ley 1581 de 2012.

---

### 4. Actividad 3: Identificación de Riesgos y Partes Interesadas

Se realizó una identificación temprana de riesgos y actores clave.

*   **Delegado de Protección de Datos (DPO):** Identifica la necesidad de un **ARA/DPIA** en fases posteriores debido al tratamiento masivo de datos personales y la toma de decisiones automatizada.
*   **Stakeholders:** Se identificaron a los ciudadanos, funcionarios de validación y el equipo de TI como los principales actores.

---

### 5. Punto de Control (Gate 1): Revisión y Decisión del Comité de IA

El Comité de IA evaluó la propuesta considerando la alineación estratégica, viabilidad y claridad del propósito.

#### Decisión Final

> **ESTADO:** ✅ **APROBADO**
>
> **Instrucción:** Se aprueba el paso a la **Fase 2 - Clasificación de Riesgo**.
>
> **Observaciones del Comité:**
> *   Se condiciona el desarrollo a la presentación de un plan de mitigación de sesgos por calidad de imagen.
> *   Se debe implementar un flujo de 'Human-in-the-loop' para casos de baja confianza, asegurando que no se rechacen automáticamente.

---

# Simulación de Ejecución: Fase 2 - Clasificación de Riesgo
## Caso de Uso: Sistema Automatizado de Validación y Expedición de Certificados de Residencia

Este documento simula la ejecución de la **Fase 2** del Ciclo de Vida de Gobernanza de IA, siguiendo los lineamientos del *Framework de Gobernanza de IA del Distrito*. Esta fase se activa tras la aprobación del *AI Use-Case Canvas* en el Gate 1.

---

### 1. Contexto de la Evaluación

*   **Entidad:** Secretaría de Gobierno del Distrito Capital.
*   **Fecha de Sesión:** 28/11/2025.
*   **Participantes (Matriz RACI):**
    *   **Accountable (A):** Comité de IA.
    *   **Responsible (R):** Responsable Técnico (Líder de Desarrollo e Innovación).
    *   **Consulted (C):** DPO y Área Jurídica.
    *   **Informed (I):** Sponsor de Negocio.

---

### 2. Actividad 1: Evaluación de Matriz de Clasificación

El equipo del proyecto, liderado por el Responsable Técnico, evaluó el caso de uso contra los criterios definidos en la *Política de Gestión de Riesgos de IA* (alineada con el AI Act y CONPES 4144).

#### Análisis de Criterios

1.  **Propósito del Sistema:**
    *   Validar documentos (Cédula y Recibos) para la expedición de un acto administrativo (Certificado de Residencia).
    *   *Evaluación:* El sistema actúa como un filtro de acceso a un servicio público esencial.

2.  **Población Afectada y Tipo de Decisión:**
    *   Afecta a la ciudadanía general de Bogotá.
    *   La decisión (aprobar/rechazar) impacta el acceso a un derecho fundamental y es prerrequisito para otros trámites y subsidios.
    *   *Evaluación:* Impacto significativo en derechos y servicios esenciales.

3.  **Datos Procesados:**
    *   Datos personales (Nombres, ID, Direcciones).
    *   No utiliza datos biométricos para identificación remota en espacios públicos (solo validación documental 1:1).
    *   *Evaluación:* Tratamiento masivo de datos personales.

4.  **Consecuencias de Errores:**
    *   Un falso negativo (rechazo incorrecto) genera barreras administrativas injustificadas y vulnera el debido proceso.
    *   *Evaluación:* Impacto alto en el individuo, aunque reversible mediante intervención humana.

#### Resultado de la Clasificación

> **NIVEL DE RIESGO PRELIMINAR:** 🔴 **ALTO RIESGO**

---

### 3. Actividad 2: Asignación de Nivel de Riesgo

#### Justificación de la Clasificación

El sistema se clasifica como **Alto Riesgo** porque cumple con las siguientes condiciones de la taxonomía:
*   **Impacto en Servicios Esenciales:** Interviene en la provisión de un servicio público esencial.
*   **Decisión Automatizada:** Asiste en decisiones que tienen efectos jurídicos sobre las personas.

**¿Por qué NO es Riesgo Inaceptable?**
Se verificó que el sistema:
*   NO realiza puntuación social (*Social Scoring*).
*   NO utiliza técnicas subliminales.
*   NO realiza identificación biométrica remota masiva en tiempo real.
*   NO explota vulnerabilidades de grupos específicos.

---

### 4. Actividad 3: Activación de Obligaciones Reforzadas

Dada la clasificación de **Alto Riesgo**, se activan automáticamente las siguientes obligaciones reforzadas para las fases subsiguientes:

1.  **Fase 3 (ARA/DPIA):** Es **OBLIGATORIO** realizar una Evaluación de Impacto en Protección de Datos y Riesgos Algorítmicos completa.
2.  **Supervisión Humana:** Se exige implementar un mecanismo de *Human-in-the-loop* (HITL). No se permiten rechazos automáticos sin revisión.
3.  **Documentación Técnica:** Se requerirá una *Model Card* detallada y *Data Sheets* exhaustivos (Fases 4 y 6).
4.  **Pruebas de Equidad:** En la Fase 6, será obligatorio demostrar que la tasa de error no varía significativamente entre documentos digitales y físicos (riesgo de sesgo por calidad de imagen).
5.  **Auditoría:** El sistema estará sujeto a auditorías externas anuales en la Fase 8.

---

### 5. Punto de Control (Gate 2): Validación de la Clasificación

El Comité de IA revisó la propuesta de clasificación y la justificación presentada.

#### Decisión Final del Comité

> **DECISIÓN:** ✅ **VALIDADA**
>
> **Dictamen:** El Comité de IA ratifica la clasificación de **Alto Riesgo**.
>
> **Instrucción al Equipo:** Proceder inmediatamente a la **Fase 3 - ARA/DPIA** involucrando al DPO. El proyecto **NO** puede avanzar a desarrollo (Fase 5) hasta que el ARA/DPIA sea aprobado en el Gate 3.

---

# Simulación de Ejecución: Fase 3 - ARA/DPIA (Alto Riesgo)
## Caso de Uso: Sistema Automatizado de Validación y Expedición de Certificados de Residencia

Este documento simula la ejecución de la **Fase 3** del Ciclo de Vida de Gobernanza de IA, siguiendo los lineamientos del *Framework de Gobernanza de IA del Distrito*. Esta fase es obligatoria dado que el sistema fue clasificado como de **Alto Riesgo** en la Fase 2.

---

### 1. Contexto de la Evaluación

*   **Entidad:** Secretaría de Gobierno del Distrito Capital.
*   **Fecha de Sesión:** 02/12/2025.
*   **Participantes (Matriz RACI):**
    *   **Accountable (A):** Comité de IA y **DPO (Voto Vinculante)**.
    *   **Consulted (C):** Responsable Técnico y Sponsor de Negocio.

---

### 2. Actividad 1: Completar Plantilla ARA/DPIA

El DPO, junto con el Responsable Técnico, completó la **Plantilla ARA/DPIA** para evaluar los impactos en derechos fundamentales y privacidad.

#### A. Mapeo de Datos y Base Legal
*   **Datos Tratados:** Imágenes de Cédulas de Ciudadanía y Recibos de Servicios Públicos.
*   **Categoría:** Datos Personales (Ley 1581). No son datos sensibles biométricos (no se hace reconocimiento facial 1:N), pero sí datos de alto impacto administrativo.
*   **Base Legal:** Cumplimiento de una obligación legal y ejercicio de funciones públicas (Ley 2052 de 2020 - Simplificación de trámites).
*   **Flujo:** Carga por ciudadano -> Procesamiento en memoria (OCR) -> Validación -> Eliminación de archivo fuente -> Generación de Certificado.

---

### 3. Actividad 2: Análisis de Riesgos

#### B. Evaluación de Impactos en Derechos (Hallazgos Clave)
1.  **Derecho a la Igualdad (Equidad):**
    *   *Riesgo Identificado:* El modelo OCR podría tener una tasa de error mayor con fotos de baja calidad (celulares gama baja), discriminando indirectamente a poblaciones vulnerables.
    *   *Nivel:* Alto.
2.  **Debido Proceso:**
    *   *Riesgo Identificado:* Un "falso negativo" (rechazo erróneo) automático impediría el acceso a un derecho sin intervención humana.
    *   *Nivel:* Alto.
3.  **Privacidad:**
    *   *Riesgo Identificado:* Exposición de datos si los archivos temporales no se eliminan o si el proveedor los usa para entrenar sus propios modelos.
    *   *Nivel:* Medio.

---

### 4. Actividad 3: Propuestas de Medidas de Mitigación

Para gestionar los riesgos identificados, se definieron las siguientes medidas de mitigación obligatorias que el equipo técnico debe implementar en la Fase 5 (Desarrollo):

#### Medidas Técnicas
1.  **Protocolo "Human-in-the-loop" (HITL):** Se prohíbe el rechazo automático. Si la confianza del modelo es <90% o la imagen es borrosa, el caso se deriva a una bandeja de revisión humana.
2.  **Privacidad por Diseño:** Configuración de eliminación automática (TTL) de las imágenes cargadas inmediatamente después de la validación. Cifrado en tránsito y reposo.

#### Medidas Organizativas
1.  **Certificación de Datos:** El Propietario de Datos debe garantizar (en Fase 4) que el dataset de entrenamiento incluye una muestra representativa de recibos físicos, arrugados y de todos los proveedores de servicios de Bogotá.
2.  **Prohibición de Usos Secundarios:** Se prohíbe explícitamente usar los datos extraídos (estrato, consumo) para *scoring* crediticio o mapas de calor de morosidad.

#### Medidas de Validación (Criterios de Aceptación para Fase 6)
1.  **Prueba de Equidad:** La diferencia en la tasa de error entre documentos de alta calidad (digitales) y baja calidad (fotos) no debe superar el **5%**.

---

### 5. Punto de Control (Gate 3): Aprobación Vinculante del DPO

El documento ARA/DPIA y el plan de mitigación fueron presentados al Comité de IA.

#### Decisión del DPO (Voto Vinculante)

> **DECISIÓN:** ✅ **APROBADO CON CONDICIONES**
>
> **Dictamen del DPO:**
> "Apruebo el análisis de impacto bajo la condición estricta de que se implementen las cláusulas de confidencialidad reforzadas con el proveedor tecnológico y se verifique que no se utilicen los datos de los ciudadanos para re-entrenar modelos externos. La medida de *Human-in-the-loop* es indispensable para mitigar el riesgo de debido proceso."

#### Ratificación del Comité de IA

> **ESTADO:** **APROBADO**. Se autoriza el paso a la **Fase 4 - Gobierno de Datos**.
>
> **Instrucción:** El plan de mitigación se convierte en requisitos funcionales obligatorios para el desarrollo.

---

# Simulación de Ejecución: Fase 4 - Gobierno de Datos
## Caso de Uso: Sistema Automatizado de Validación y Expedición de Certificados de Residencia

Este documento simula la ejecución de la **Fase 4** del Ciclo de Vida de Gobernanza de IA, siguiendo los lineamientos del *Framework de Gobernanza de IA del Distrito*. Esta fase asegura que los datos utilizados para entrenar el modelo sean de alta calidad, representativos y gestionados éticamente.

---

### 1. Contexto de la Ejecución

*   **Entidad:** Secretaría de Gobierno del Distrito Capital.
*   **Fecha de Sesión:** 05/12/2025.
*   **Participantes (Matriz RACI):**
    *   **Accountable (A):** DPO (Oficial de Protección de Datos).
    *   **Responsible (R):** Responsable Técnico y Propietario de Datos (Data Steward).
    *   **Consulted (C):** Comité de IA y Sponsor de Negocio.

---

### 2. Actividad 1: Inventario y Documentación de Fuentes

El Propietario de Datos (Data Steward), junto con el equipo técnico, realizó una auditoría exhaustiva del conjunto de datos denominado **RESIDENCIA_BOG_VALIDATION_V1**.

*   **Fuentes:** Datos históricos de solicitudes previas anonimizadas y cargas controladas durante la fase piloto.

---

### 3. Actividad 2: Evaluación de Calidad Dimensional

*   **Volumen:** 15,000 registros (Imágenes PDF/JPG y texto extraído).
*   **Completitud:** Menos del 2% de datos faltantes en campos no estructurados.
*   **Consistencia:** Se identificaron inconsistencias en formatos de dirección (ej. "Cll" vs "Calle"), las cuales fueron normalizadas.

---

### 4. Actividad 3: Análisis de Representatividad y Detección de Sesgos

Durante el análisis estadístico, se detectó un riesgo significativo de sesgo en la composición original del dataset:
*   **Hallazgo:** El 80% de las facturas correspondían al proveedor **Enel** en formato nativo digital.
*   **Riesgo:** El modelo podría fallar sistemáticamente con recibos de otros proveedores (Acueducto, Vanti) o con formatos físicos escaneados, discriminando a ciudadanos que no reciben factura digital.
*   **Acción Correctiva:** Se aplicó una técnica de balanceo (oversampling) enriqueciendo el dataset con muestras de otros proveedores y fotografías de baja calidad tomadas con celulares de gama baja.

---

### 5. Actividad 4: Elaboración de Data Sheets

Se documentó el conjunto de datos utilizando la plantilla estándar de **Data Sheet** del framework, asegurando transparencia sobre su origen y limitaciones.

#### Resumen del Data Sheet (RESIDENCIA_BOG_VALIDATION_V1)
*   **Propósito:** Entrenar modelos OCR/NLP para validación de identidad y residencia.
*   **Datos Personales:** Sí (Nombres, Cédulas, Direcciones).
*   **Datos Sensibles:** No.
*   **Base Legal:** Ejercicio de funciones públicas y simplificación de trámites.
*   **Transformaciones:** Pre-procesamiento de imágenes (contraste) y normalización de texto.
*   **Usos Prohibidos:** Se estableció explícitamente la prohibición de usar estos datos para evaluar capacidad de pago, crear mapas de morosidad o compartir con terceros comerciales.

---

### 6. Punto de Control (Gate 4): Certificación de la Calidad de los Datos

El Propietario de Datos y el DPO realizaron la revisión final del Data Sheet y la calidad del dataset enriquecido.

#### Certificación del Propietario de Datos y DPO

> **DECISIÓN:** ✅ **APROBADO CON CONDICIÓN DE EQUIDAD**
>
> **Dictamen:**
> "Se certifica que el dataset cumple con los estándares de calidad y que se han aplicado las medidas correctivas para mitigar el sesgo de proveedor.
>
> **Condición para Fase 6:** No se autoriza el despliegue hasta que se demuestre estadísticamente en la Fase de Pruebas que el modelo reconoce con igual precisión (diferencia <5%) una factura digital y una fotografía de celular de un recibo físico."

> **Instrucción:** El dataset queda habilitado para ser utilizado por el equipo de desarrollo en la **Fase 5**.

---

# Simulación de Ejecución: Fase 5 - Desarrollo y Adquisición
## Caso de Uso: Sistema Automatizado de Validación y Expedición de Certificados de Residencia

Este documento simula la ejecución de la **Fase 5** del Ciclo de Vida de Gobernanza de IA, siguiendo los lineamientos del *Framework de Gobernanza de IA del Distrito*. Esta fase materializa los requisitos éticos y legales definidos en las fases anteriores (Canvas, Riesgo, ARA/DPIA) en obligaciones contractuales y especificaciones técnicas tangibles.

---

### 1. Contexto de la Ejecución

*   **Entidad:** Secretaría de Gobierno del Distrito Capital.
*   **Fecha de Cierre de Fase:** 15/12/2025.
*   **Estrategia de Implementación:** Híbrida (Adquisición de Motor OCR + Desarrollo Interno de Integración).
*   **Participantes (Matriz RACI):**
    *   **Accountable (A):** Responsable Técnico (Desarrollo) y Área Jurídica (Contratación).
    *   **Consulted (C):** DPO y Comité de IA.

---

### 2. Camino B: Adquisición Externa

#### Actividad 1: Debida Diligencia y Selección del Proveedor (Motor OCR)

Dado que la entidad no cuenta con la capacidad para desarrollar un motor de OCR/NLP desde cero, se procedió a la adquisición de una solución de mercado. Se aplicó el **Checklist de Evaluación de Proveedores de IA** (versión Estándar para Alto Riesgo).

*   **Proveedor Evaluado:** VisionTech OCR Services.
*   **Resultado del Checklist:** **RECOMENDADO** (Cumplimiento de criterios mandatorios).
*   **Hallazgos Clave:**
    *   **Conformidad Regulatoria:** El proveedor presentó certificación de conformidad con la Ley 1581 y aceptó firmar el DPA del Distrito.
    *   **Transparencia (Caja Blanca):** Se obligó contractualmente a la entrega de la *Model Card* del modelo base y el *Data Sheet* de sus datos de entrenamiento.
    *   **Seguridad:** Cuenta con certificación ISO 27001 vigente.
    *   **Auditoría:** Aceptó la cláusula de "Derecho a Auditoría" por parte del Distrito.

#### Actividad 2: Negociación del Contrato con Cláusulas de Gobernanza

El Área Jurídica, con apoyo del DPO, blindó la contratación del motor OCR mediante cláusulas específicas.

*   **Acuerdo de Procesamiento de Datos (DPA):** Define al Distrito como Responsable y a VisionTech como Encargado. Prohíbe el uso de los datos del Distrito para re-entrenar los modelos comerciales del proveedor.
*   **SLA de Precisión:** Se establece un nivel de servicio donde la precisión del OCR no puede ser inferior al 95%. Penalizaciones económicas por degradación del modelo.
*   **Portabilidad:** Obligación de devolver o destruir todos los datos al finalizar el contrato.

---

### 3. Camino A: Desarrollo Interno

#### Actividad 1: Diseño e Implementación con Gobernanza Integrada

El equipo de desarrollo interno de la Secretaría construyó la capa de orquestación y la interfaz de usuario (Chatbot), implementando los controles definidos en el ARA/DPIA (Fase 3).

#### Implementación de Controles en Código
1.  **Protocolo "Human-in-the-loop" (HITL):**
    *   *Implementación:* Se desarrolló un microservicio de "Gestión de Excepciones".
    *   *Lógica:* Si `confianza_ocr < 0.90` OR `calidad_imagen == 'baja'`, el sistema no emite respuesta de rechazo. En su lugar, encola la solicitud en el dashboard de los funcionarios supervisores.
2.  **Privacidad por Diseño (Minimización):**
    *   *Implementación:* Configuración de políticas de ciclo de vida en el almacenamiento (Bucket S3).
    *   *Regla:* Las imágenes de cédulas y recibos tienen un TTL (Time-to-Live) de 1 hora tras la finalización del trámite. Solo se persisten los metadatos y logs de auditoría.
3.  **Trazabilidad Inmutable:**
    *   *Implementación:* Sistema de logs centralizado que registra cada decisión: `Input_ID`, `Score_Confianza`, `Decisión_IA`, `Decisión_Humana` (si aplica), `Timestamp`.

---

### 4. Punto de Control (Gate 5): Revisión de la Solución y Contrato

El Comité Técnico y Jurídico revisó los entregables antes de autorizar el paso a pruebas.

#### Decisión

> **DECISIÓN:** ✅ **APROBADO**
>
> **Dictamen:**
> "Se aprueba la arquitectura híbrida y el contrato con VisionTech OCR Services.
> *   **Verificación Técnica:** La integración implementa correctamente el flujo de derivación a humanos (HITL).
> *   **Verificación Jurídica:** El contrato incluye las salvaguardas de la Ley 1581 y garantías de auditoría.
>
> **Instrucción:** Proceder a la **Fase 6 - Pruebas y Validación**, donde se deberá ejecutar el test de equidad (diferencia de error < 5%) exigido en la Fase 3."

---

# Simulación de Ejecución: Fase 6 - Pruebas y Validación
## Caso de Uso: Sistema Automatizado de Validación y Expedición de Certificados de Residencia

Este documento simula la ejecución de la **Fase 6** del Ciclo de Vida de Gobernanza de IA, siguiendo los lineamientos del *Framework de Gobernanza de IA del Distrito*. Esta fase tiene como objetivo demostrar con evidencia empírica que el sistema cumple con los requisitos técnicos, éticos y funcionales definidos en las fases previas (especialmente en el ARA/DPIA).

---

### 1. Contexto de la Ejecución

*   **Entidad:** Secretaría de Gobierno del Distrito Capital.
*   **Fecha de Cierre de Fase:** 20/01/2026.
*   **Participantes (Matriz RACI):**
    *   **Accountable (A):** Responsable Técnico (Líder de Desarrollo).
    *   **Consulted (C):** Comité de IA, DPO.
    *   **Informed (I):** Área Jurídica.

---

### 2. Actividad 1: Pruebas Técnicas

El equipo técnico ejecutó una batería de pruebas sobre el modelo **RESIDENCIA_BOG_OCR_VALIDATOR_V1.0** utilizando el conjunto de datos de prueba reservado (10% del dataset total, nunca visto por el modelo).

#### A. Rendimiento del Modelo
Se evaluaron las métricas de desempeño contra los KPIs definidos en la Fase 1:
*   **Precisión Global (Accuracy):** 96.5% (Meta: ≥ 95%). ✅ **CUMPLE**
*   **Tasa de Resolución Autónoma:** 92% de los documentos fueron procesados con una confianza superior al 90%. ✅ **CUMPLE**
*   **Tiempo de Respuesta:** Promedio de 1.8 segundos por documento. ✅ **CUMPLE**

#### B. Robustez Técnica
Se sometió al modelo a pruebas de estrés con imágenes degradadas:
*   **Prueba de Ruido:** Se inyectó ruido gaussiano a las imágenes. El modelo mantuvo una precisión >90% hasta niveles de ruido moderado.
*   **Prueba de Rotación:** El modelo corrigió automáticamente rotaciones de hasta 45 grados.

#### C. Seguridad (Ciberseguridad)
Se realizó un *pentesting* enfocado en riesgos de IA:
*   **Ataques de Evasión:** Se intentó engañar al OCR modificando píxeles imperceptibles. El modelo mostró resistencia adecuada.
*   **Inyección de Prompts (Chatbot):** Se verificó que el componente de chat no revelara instrucciones del sistema ni datos de otros usuarios.

---

### 3. Actividad 2: Pruebas de Equidad

Esta fue la prueba crítica condicionada por el DPO y el Comité de IA en la Fase 3 y 4.

#### Objetivo
Verificar que el sistema no discrimine a ciudadanos que aportan documentos físicos (fotos de celular) frente a los que aportan documentos digitales (PDFs originales).

#### Resultados Cuantitativos
*   **Tasa de Acierto en Documentos Digitales (Alta Calidad):** 98.5%
*   **Tasa de Acierto en Fotos de Celular (Baja/Media Calidad):** 94.7%
*   **Diferencia (Gap de Equidad):** 3.8%

#### Evaluación
> **Criterio de Aceptación:** La diferencia no debe superar el 5%.
> **Resultado:** 3.8% < 5%. ✅ **CUMPLE**

*Observación:* Aunque cumple el umbral, la diferencia existente justifica plenamente la medida de mitigación de "Human-in-the-loop" para los casos que caen en ese margen de error.

---

### 4. Actividad 3: Pruebas de Explicabilidad

Se validó que el sistema sea transparente para el usuario final y explicable para el auditor.

*   **Notificación al Usuario:** Se verificó que el Chatbot inicia la conversación con el mensaje: *"Hola, soy un asistente virtual automatizado de la Secretaría de Gobierno..."*.
*   **Explicabilidad de la Decisión:**
    *   En caso de aprobación: El sistema informa qué datos validó.
    *   En caso de derivación a humano: El sistema informa *"La calidad de la imagen no permite una validación automática segura. Un funcionario revisará su caso en breve"*. No se generan rechazos "caja negra".

---

### 5. Actividad 4: Pruebas de Usabilidad

*   **Accesibilidad:** Se auditó la interfaz web del Chatbot cumpliendo con **WCAG 2.1 Nivel AA** (compatible con lectores de pantalla).
*   **Usabilidad:** Se realizaron pruebas con ciudadanos de diferentes perfiles para asegurar que la interacción con el chatbot fuera intuitiva.

---

### 6. Actividad 5: Pruebas de Integración

*   **Integración:** Se verificó la correcta comunicación con la base de datos de radicación y la generación del PDF del certificado firmado digitalmente.
*   **Prueba de Carga:** El sistema soportó 500 peticiones concurrentes sin degradación del servicio (simulando picos de demanda).

---

### 7. Punto de Control (Gate 6): Aprobación para Despliegue

El Responsable Técnico presentó el **Informe de Pruebas y Validación** y la **Model Card** actualizada al Comité de IA.

#### Decisión del Comité de IA

> **DECISIÓN:** ✅ **APROBADO PARA DESPLIEGUE (GO-LIVE)**
>
> **Dictamen:**
> "La evidencia presentada demuestra que el sistema es técnicamente robusto y cumple con los criterios de equidad establecidos en el ARA/DPIA.
>
> **Instrucciones para Fase 7 (Despliegue):**
> 1.  Proceder con el despliegue gradual (Piloto en 2 localidades) durante las primeras 2 semanas.
> 2.  Activar el monitoreo intensivo de 'Drift' para asegurar que los datos de producción se comporten igual que los de prueba."

---

# Simulación de Ejecución: Fase 7 - Despliegue
## Caso de Uso: Sistema Automatizado de Validación y Expedición de Certificados de Residencia

Este documento simula la ejecución de la **Fase 7** del Ciclo de Vida de Gobernanza de IA, siguiendo los lineamientos del *Framework de Gobernanza de IA del Distrito*. Esta fase marca la transición crítica del entorno de pruebas al entorno de producción, asegurando una puesta en marcha controlada.

---

### 1. Contexto de la Ejecución

*   **Entidad:** Secretaría de Gobierno del Distrito Capital.
*   **Fecha de Sesión (Gate 7):** 25/01/2026.
*   **Participantes (Matriz RACI):**
    *   **Accountable (A):** Comité de IA (Autorización Final).
    *   **Responsible (R):** Responsable Técnico.
    *   **Consulted (C):** Sponsor de Negocio y DPO.

---

### 2. Actividad 1: Capacitación de Usuarios

Antes de activar el sistema, se ejecutó el plan de formación para garantizar que el componente humano del sistema ("Human-in-the-loop") fuera competente.

*   **Funcionarios Supervisores:** Se capacitó al equipo de Atención al Ciudadano en el manejo de la "Bandeja de Excepciones".
    *   *Enfoque:* Cambio de rol de "validadores de todo" a "gestores de excepciones".
    *   *Protocolo:* Instrucción clara de que ante la duda razonable en una imagen borrosa, prevalece el criterio humano garantista (pro-ciudadano).
*   **Ciudadanía:** Se publicaron infografías en el portal web explicando el nuevo trámite inmediato y cómo tomar correctamente la foto del recibo para evitar rechazos técnicos.

---

### 3. Actividad 2: Configuración de Controles

El equipo técnico activó la infraestructura de observabilidad definida en el ARA/DPIA:

*   **Logs de Auditoría:** Activación del registro inmutable de transacciones (`Input_ID`, `Score_Confianza`, `Decisión`, `Timestamp`).
*   **Dashboard de Gobernanza:** Se habilitó el tablero en tiempo real para monitorear:
    *   Tasa de Derivación a Humanos (Meta: <15%).
    *   Tiempos de Respuesta (Meta: <3 min).
    *   Alertas de *Drift* (si la distribución de proveedores de recibos cambia drásticamente).

---

### 4. Actividad 3: Despliegue Gradual

Siguiendo la instrucción del Gate 6, se optó por un lanzamiento faseado para minimizar riesgos operativos.

*   **Fase A (Semana 1-2): Piloto Controlado.**
    *   *Alcance:* Habilitado solo para solicitudes originadas en las localidades de **Kennedy y Suba**.
    *   *Objetivo:* Validar carga y comportamiento con documentos reales en zonas de alta demanda.
*   **Fase B (Semana 3+): Escalamiento General.**
    *   *Condición:* Si no se presentan incidentes críticos en Fase A, se abre a todo el Distrito.

---

### 5. Actividad 4: Establecimiento de Canales de Reporte

Se implementaron los mecanismos de transparencia y defensa del ciudadano:

*   **Botón de Apelación:** En caso de que el sistema (o el humano supervisor) rechace la solicitud, se habilitó un botón visible: *"No estoy de acuerdo, solicitar segunda revisión"*, que escala el caso a un nivel superior.

---

### 6. Actividad 5: Comunicación Transparente

*   **Transparencia Activa:** El Chatbot inicia con el mensaje: *"Hola, soy un asistente virtual automatizado. Estoy aquí para validar tus documentos y expedir tu certificado al instante."*

---

### 7. Punto de Control (Gate 7): Aprobación del Go-Live

El Comité de IA se reunió con el Sponsor de Negocio para la autorización final.

#### Verificación de Pre-requisitos
1.  ¿Personal capacitado? **SÍ**.
2.  ¿Monitoreo activo? **SÍ**.
3.  ¿Plan de comunicación ejecutado? **SÍ**.
4.  ¿Pruebas de equidad superadas (Fase 6)? **SÍ**.

#### Decisión Final

> **DECISIÓN:** ✅ **AUTORIZADO EL GO-LIVE (Fase A - Piloto)**
>
> **Dictamen:**
> "Se autoriza la puesta en producción del sistema bajo la modalidad de piloto controlado en Kennedy y Suba.
>
> **Condición de Operación:** Se declara estado de *Hypercare* (monitoreo intensivo) durante las próximas 2 semanas. El Responsable Técnico debe reportar diariamente al Comité de IA cualquier anomalía en la tasa de rechazos."

---

# Simulación de Ejecución: Fase 8 - Monitoreo y Auditoría
## Caso de Uso: Sistema Automatizado de Validación y Expedición de Certificados de Residencia

Este documento simula la ejecución de la **Fase 8** del Ciclo de Vida de Gobernanza de IA, siguiendo los lineamientos del *Framework de Gobernanza de IA del Distrito*. Esta fase abarca el primer trimestre de operación tras el despliegue, enfocándose en la vigilancia continua y la rendición de cuentas.

---

### 1. Contexto de la Ejecución

*   **Entidad:** Secretaría de Gobierno del Distrito Capital.
*   **Periodo Evaluado:** Primer Trimestre de Operación (Febrero - Abril 2026).
*   **Fecha de Sesión (Gate 8):** 30/04/2026.
*   **Participantes (Matriz RACI):**
    *   **Accountable (A):** Comité de IA.
    *   **Responsible (R):** Responsable Técnico.
    *   **Consulted (C):** DPO y Sponsor de Negocio.

---

### 2. Actividad 1: Monitoreo Técnico

El Responsable Técnico presentó el reporte del **Dashboard de Gobernanza** con los datos acumulados de los primeros 90 días de operación.

#### A. Métricas de Desempeño y Servicio
*   **Volumen:** 45,000 solicitudes procesadas.
*   **Tasa de Resolución Autónoma:** 91.5% (Meta: >90%). ✅ **CUMPLE**
    *   *Observación:* El sistema validó automáticamente la gran mayoría de casos, liberando carga operativa.
*   **Tiempo Promedio de Respuesta:** 1.5 minutos (Meta: <3 min). ✅ **CUMPLE**
*   **Satisfacción Ciudadana (CSAT):** 4.6/5.0 (Meta: >4.2). ✅ **CUMPLE**

#### B. Métricas de Equidad y Drift
*   **Monitoreo de Equidad:**
    *   Tasa de error en documentos digitales: 1.2%.
    *   Tasa de error en fotos de celular (gama baja): 4.5%.
    *   *Gap:* 3.3% (Meta: <5%). ✅ **CUMPLE**
*   **Detección de Drift:**
    *   Se detectó una leve desviación en la segunda semana de marzo debido a un cambio estético en la factura de un proveedor menor de internet (no contemplado inicialmente).
    *   *Acción:* El sistema derivó estos casos a humanos (baja confianza) correctamente. No se requirió reentrenamiento urgente, pero se agendó para el próximo ciclo.

---

### 3. Actividad 2: Gestión de Incidentes

Se revisó el registro de incidentes reportados durante el trimestre.

#### Incidente Destacado: INC-2026-003 (Queja por Rechazo)
*   **Descripción:** Un ciudadano reportó vía PQR que el sistema rechazó su certificado alegando "Dirección no coincide", aunque él afirmaba que sí.
*   **Investigación:** Se revisaron los logs de auditoría.
    *   La IA marcó confianza baja (85%) por una abreviatura no estándar en la dirección.
    *   El caso fue derivado a un supervisor humano (protocolo HITL).
    *   El supervisor humano rechazó la solicitud por error de lectura.
*   **Resolución:** Se contactó al ciudadano, se corrigió el error manualmente y se expidió el certificado.
*   **Lección Aprendida:** Se reforzó la capacitación de los supervisores humanos sobre abreviaturas no estándar. El caso se etiquetó para futuro reentrenamiento (Golden Dataset).

---

### 4. Actividad 3: Auditoría Periódica (Interna)

El equipo de Control Interno realizó una verificación muestral de cumplimiento.

*   **Verificación de Supervisión Humana:** Se auditaron 50 casos derivados a la "Bandeja de Excepciones". En el 100% de los casos hubo una acción registrada por un funcionario (Aprobar/Rechazar) con su respectiva justificación.
*   **Verificación de Privacidad (Retención de Datos):** Se verificó aleatoriamente si existían imágenes de cédulas de solicitudes cerradas en febrero.
    *   *Resultado:* No se encontraron archivos. El script de borrado seguro (TTL 30 días) funcionó correctamente. ✅ **CUMPLE**

---

### 5. Actividad 4: Gestión de Cambios

*   **Evaluación de Impacto:** El *drift* detectado en marzo fue analizado. Se determinó que no afectaba la precisión de forma crítica, pero se agendó una actualización.
*   **Actualización de Documentación:** Se creó una nueva versión del *Data Sheet* para incluir los nuevos formatos de factura y se planificó el reentrenamiento del modelo para la versión v1.1.

---

### 5. Punto de Control (Gate 8): Revisión Trimestral de Desempeño

El Comité de IA analizó la evidencia presentada para decidir el futuro del sistema.

#### Evaluación del Comité
1.  **Desempeño:** El sistema supera las metas de eficiencia y satisfacción.
2.  **Riesgos:** Los riesgos de equidad están controlados dentro de los márgenes aceptables.
3.  **Cumplimiento:** La auditoría confirma la adherencia a la política de datos.

#### Decisión Final

> **DECISIÓN:** 🔄 **MANTENER**
>
> **Dictamen:**
> "El sistema opera correctamente y genera valor público. Se autoriza la continuidad de la operación.
>
> **Instrucciones para el próximo trimestre:**
> 1.  Recopilar los casos de facturas con nuevos formatos (detectados por drift) para preparar un reentrenamiento programado (v1.1) en el siguiente ciclo.
> 2.  Mantener la vigilancia sobre la tasa de error en fotos de baja calidad."

---

# Simulación de Ejecución: Fase 9 - Retiro o Fin de Vida
## Caso de Uso: Sistema Automatizado de Validación y Expedición de Certificados de Residencia

Este documento simula la ejecución de la **Fase 9** del Ciclo de Vida de Gobernanza de IA, siguiendo los lineamientos del *Framework de Gobernanza de IA del Distrito*. Esta fase cierra el ciclo de vida del sistema, asegurando un desmantelamiento seguro, legal y ordenado.

---

### 1. Contexto de la Ejecución

*   **Entidad:** Secretaría de Gobierno del Distrito Capital.
*   **Fecha de Sesión (Gate 9):** [Fecha Futura Simulada, ej. 30/11/2028].
*   **Participantes (Matriz RACI):**
    *   **Accountable (A):** Comité de IA y DPO (Voto Decisivo en Datos).
    *   **Responsible (R):** Responsable Técnico.
    *   **Consulted (C):** Sponsor de Negocio.

---

### 2. Actividad 1: Decisión de Retiro

El Comité de IA ha decidido retirar el sistema basándose en uno de los triggers definidos en la Fase 1.

#### Causal de Retiro (Simulada)
*   **Obsolescencia Técnica:** La tecnología OCR utilizada (v1.0) ha sido superada por nuevos modelos de IA Generativa Multimodal que ofrecen mayor precisión a menor costo, haciendo insostenible el mantenimiento del actual.

---

### 3. Actividad 2: Planificación de la Transición

#### Plan de Transición (Continuidad del Servicio)
*   **Estrategia:** Migración a nuevo sistema (v2.0).
*   **Acción:** Se notifica a la ciudadanía con 30 días de antelación mediante el portal web y el mismo chatbot.
*   **Mensaje:** "Este asistente dejará de funcionar el día [Fecha]. A partir de entonces, el trámite se realizará a través de la nueva plataforma Distrital de Servicios."

---

### 4. Actividad 3: Gestión de Datos

El Propietario de Datos y el DPO supervisaron la disposición final de los activos de información.

#### Acciones Ejecutadas
1.  **Eliminación Segura (Secure Wipe):**
    *   El Responsable Técnico ejecutó scripts de borrado seguro (sobreescritura) de todas las imágenes de cédulas y recibos almacenados en "hot storage" y copias de seguridad temporales.
2.  **Archivado Legal (Cold Storage):**
    *   Se conservaron únicamente los **logs de auditoría** y los metadatos de las transacciones (ID de radicado, fecha, resultado de validación) durante el tiempo exigido por la Ley de Archivo General de la Nación (5 años) para responder a futuras acciones legales.
3.  **Destrucción del Modelo:**
    *   El modelo neuronal entrenado fue archivado como activo de propiedad intelectual del Distrito, pero desconectado de los entornos de producción.

---

### 5. Actividad 4: Documentación de Lecciones Aprendidas

Se realizó una sesión de cierre ("Post-Mortem") para documentar el conocimiento adquirido.

#### Informe de Lecciones Aprendidas
*   **Lo que funcionó:** La integración con la base de datos de servicios públicos redujo los tiempos en un 95%. El protocolo "Human-in-the-loop" evitó crisis reputacionales por falsos negativos.
*   **Lo que falló:** El OCR tuvo dificultades persistentes con recibos muy arrugados en zonas rurales, requiriendo más intervención humana de la planeada inicialmente.
*   **Recomendación:** Para la v2.0, utilizar modelos multimodales que entiendan mejor el contexto visual de documentos deteriorados.

---

### 6. Punto de Control (Gate 9): Aprobación Final y Cierre

El Comité de IA, el DPO y Auditoría Interna se reunieron para el cierre formal.

#### Verificación de Requisitos (Checklist de Cierre)
1.  ¿Se ha garantizado la continuidad del servicio por otro canal? **SÍ**.
2.  **(Veto del DPO)** ¿Existe certificado técnico de eliminación segura de las imágenes de documentos de identidad? **SÍ**.
3.  ¿Se han revocado los accesos y claves API del proveedor externo? **SÍ**.
4.  ¿Está guardado el informe de Lecciones Aprendidas? **SÍ**.

#### Decisión Final

> **DECISIÓN:** ✅ **APROBADO EL RETIRO DEFINITIVO**
>
> **Dictamen:**
> "Se declara la terminación del ciclo de vida del sistema 'Chatbot Certificado Residencia v1.0'. Se instruye a TI liberar los recursos de nube asociados y archivar el expediente en el Registro Central de Casos de Uso de IA."

---
*Documento generado para el cierre del expediente del proyecto en el Registro Central de Casos de Uso de IA.*
