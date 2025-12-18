# Documento Consolidado de Implementación: Ciclo de Vida de Gobernanza de IA
## Caso de Uso: Sistema Automatizado de Validación y Expedición de Certificados de Residencia

Este documento consolida la simulación de ejecución de las 9 fases del Ciclo de Vida de Gobernanza de IA del Distrito para el proyecto de automatización del Certificado de Residencia.

---

## Fase 1: Intake y AI Use-Case Canvas

### 1. Contexto de la Iniciativa

*   **Entidad:** Secretaría de Gobierno del Distrito Capital.
*   **Sponsor de Negocio:** Director de Atención al Ciudadano / Product Owner.
*   **Responsable Técnico:** Líder de Desarrollo e Innovación / Equipo TIC.
*   **Fecha de Solicitud:** 26/11/2025 - v1.0.

### 2. Actividad 1: Diligenciamiento del AI Use-Case Canvas

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

### 3. Actividad 2: Valoración Preliminar Multidisciplinaria

El borrador del canvas fue sometido a un "filtro de viabilidad" por los roles clave:

*   **Responsable Técnico:** Confirma la viabilidad técnica de la solución (OCR/NLP) y establece KPIs técnicos (Precisión ≥ 98%).
*   **Delegado de Protección de Datos (DPO):** Identifica la necesidad de un **ARA/DPIA** en fases posteriores debido al tratamiento masivo de datos personales y la toma de decisiones automatizada.
*   **Área Jurídica:** Valida la base legal (Ejercicio de funciones públicas y simplificación de trámites) y la conformidad con la Ley 1581 de 2012.

### 4. Punto de Control (Gate 1): Revisión y Decisión del Comité de IA

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

## Fase 2: Clasificación de Riesgo

### 1. Contexto de la Evaluación

*   **Fecha de Sesión:** 28/11/2025.
*   **Participantes:** Comité de IA (A), Responsable Técnico (R), DPO y Jurídica (C).

### 2. Actividad 1: Aplicación de la Taxonomía de Riesgo

El equipo evaluó el caso de uso contra los criterios de la *Política de Gestión de Riesgos de IA*.

#### Análisis de Criterios
1.  **Propósito del Sistema:** Filtro de acceso a un servicio público esencial (Certificado de Residencia).
2.  **Población Afectada y Tipo de Decisión:** Afecta a la ciudadanía general; la decisión impacta el acceso a un derecho fundamental.
3.  **Datos Procesados:** Tratamiento masivo de datos personales (Nombres, ID, Direcciones).
4.  **Consecuencias de Errores:** Un falso negativo genera barreras administrativas injustificadas y vulnera el debido proceso.

#### Resultado de la Clasificación
> **NIVEL DE RIESGO ASIGNADO:** 🔴 **ALTO RIESGO**

#### Justificación
El sistema se clasifica como **Alto Riesgo** por intervenir en la provisión de un servicio público esencial y asistir en decisiones con efectos jurídicos. **NO** es Riesgo Inaceptable porque no realiza puntuación social ni biometría remota masiva.

### 3. Actividad 2: Determinación de las Obligaciones de Gobernanza

Se activan las siguientes obligaciones reforzadas:
1.  **Fase 3 (ARA/DPIA):** Obligatorio.
2.  **Supervisión Humana:** Mecanismo *Human-in-the-loop* obligatorio.
3.  **Documentación:** *Model Card* y *Data Sheets* exhaustivos.
4.  **Pruebas de Equidad:** Obligatorias en Fase 6.
5.  **Auditoría:** Auditorías externas anuales en Fase 8.

### 4. Punto de Control (Gate 2): Validación de la Clasificación

> **DECISIÓN:** ✅ **VALIDADA**
>
> **Dictamen:** El Comité de IA ratifica la clasificación de **Alto Riesgo**. Proceder a la **Fase 3**.

---

## Fase 3: ARA/DPIA (Alto Riesgo)

### 1. Contexto de la Evaluación

*   **Fecha de Sesión:** 02/12/2025.
*   **Participantes:** Comité de IA y DPO (A - Voto Vinculante), Responsable Técnico (C).

### 2. Actividad 1: Ejecución del Análisis de Impacto y Riesgos

#### A. Mapeo de Datos y Base Legal
*   **Datos:** Imágenes de Cédulas y Recibos (Datos Personales).
*   **Base Legal:** Ley 2052 de 2020 (Simplificación de trámites).

#### B. Evaluación de Impactos en Derechos
1.  **Igualdad (Equidad):** Riesgo alto de sesgo técnico (OCR) en fotos de baja calidad.
2.  **Debido Proceso:** Riesgo alto de rechazo automático erróneo sin intervención humana.
3.  **Privacidad:** Riesgo medio de exposición de datos temporales.

### 3. Actividad 2: Diseño del Plan de Mitigación

#### Medidas Obligatorias
1.  **Técnicas:** Protocolo "Human-in-the-loop" (prohibido rechazo automático si confianza <90%). Privacidad por diseño (eliminación automática de imágenes tras validación).
2.  **Organizativas:** Certificación de representatividad del dataset (Fase 4). Prohibición de usos secundarios (scoring crediticio).
3.  **Validación:** Prueba de equidad en Fase 6 (diferencia de error < 5%).

### 4. Punto de Control (Gate 3): Aprobación Vinculante del DPO

> **DECISIÓN:** ✅ **APROBADO CON CONDICIONES**
>
> **Dictamen del DPO:** Aprobado bajo condición de implementar cláusulas de confidencialidad reforzadas y el mecanismo *Human-in-the-loop*.

---

## Fase 4: Gobierno de Datos

### 1. Contexto de la Ejecución

*   **Fecha de Sesión:** 05/12/2025.
*   **Participantes:** DPO (A), Responsable Técnico y Data Steward (R).

### 2. Actividad 1: Evaluación de Calidad y Representatividad

Auditoría del dataset **RESIDENCIA_BOG_VALIDATION_V1**.
*   **Hallazgo de Sesgo:** El 80% de facturas eran digitales (Enel). Riesgo de discriminar recibos físicos o de otros proveedores.
*   **Acción Correctiva:** Balanceo (oversampling) con muestras de otros proveedores y fotos de baja calidad.

### 3. Actividad 2: Elaboración de Data Sheets

Se documentó el dataset:
*   **Propósito:** Entrenamiento OCR/NLP.
*   **Usos Prohibidos:** Evaluación de capacidad de pago o mapas de morosidad.

### 4. Punto de Control (Gate 4): Certificación de Calidad

> **DECISIÓN:** ✅ **APROBADO CON CONDICIÓN DE EQUIDAD**
>
> **Dictamen:** Se certifica la calidad. No se autoriza despliegue hasta demostrar en Fase 6 que el modelo reconoce con igual precisión facturas digitales y fotos de celular.

---

## Fase 5: Desarrollo y Adquisición

### 1. Contexto de la Ejecución

*   **Fecha de Cierre:** 15/12/2025.
*   **Estrategia:** Híbrida (Adquisición Motor OCR + Desarrollo Interno).

### 2. Actividad 1: Selección del Proveedor (Motor OCR)

*   **Proveedor:** VisionTech OCR Services.
*   **Evaluación:** RECOMENDADO (Checklist Estándar).
*   **Hallazgos:** Cumple Ley 1581, entrega Model Card (Caja Blanca), ISO 27001 vigente, acepta auditoría.

### 3. Actividad 2: Desarrollo Interno e Integración

Implementación de controles del ARA/DPIA:
1.  **Human-in-the-loop:** Microservicio de gestión de excepciones (si confianza < 0.90 -> humano).
2.  **Privacidad:** TTL de 1 hora para imágenes en S3.
3.  **Trazabilidad:** Logs inmutables de decisión.

### 4. Actividad 3: Formalización Contractual

*   **DPA:** Distrito como Responsable, Proveedor como Encargado.
*   **SLA:** Precisión mínima 95%.

### 5. Punto de Control (Gate 5): Revisión

> **DECISIÓN:** ✅ **APROBADO**
>
> **Dictamen:** Se aprueba arquitectura y contrato. Proceder a **Fase 6**.

---

## Fase 6: Pruebas y Validación

### 1. Contexto de la Ejecución

*   **Fecha de Cierre:** 20/01/2026.
*   **Participantes:** Responsable Técnico (A), Comité de IA (C).

### 2. Actividad 1: Pruebas Técnicas

*   **Precisión Global:** 96.5% (Meta ≥ 95%). ✅
*   **Resolución Autónoma:** 92%. ✅
*   **Seguridad:** Resistencia a ataques de evasión y protección de prompts.

### 3. Actividad 2: Pruebas de Equidad (Crítica)

*   **Acierto Digital:** 98.5%.
*   **Acierto Fotos Celular:** 94.7%.
*   **Gap:** 3.8% (Meta < 5%). ✅ **CUMPLE**.

### 4. Actividad 3: Transparencia y Usabilidad

*   **Transparencia:** Chatbot se identifica como IA.
*   **Explicabilidad:** Informa razones de derivación a humano (calidad de imagen).
*   **Accesibilidad:** Cumple WCAG 2.1 AA.

### 5. Punto de Control (Gate 6): Aprobación para Despliegue

> **DECISIÓN:** ✅ **APROBADO PARA DESPLIEGUE (GO-LIVE)**
>
> **Dictamen:** Sistema robusto y equitativo. Autorizado despliegue gradual con monitoreo de Drift.

---

## Fase 7: Despliegue

### 1. Contexto de la Ejecución

*   **Fecha de Sesión:** 25/01/2026.
*   **Participantes:** Comité de IA (A), Responsable Técnico (R).

### 2. Actividades de Preparación

1.  **Capacitación:** Equipo de Atención al Ciudadano formado como "gestores de excepciones" (criterio pro-ciudadano).
2.  **Monitoreo:** Activación de logs y dashboard en tiempo real.
3.  **Estrategia:** Despliegue gradual (Piloto en Kennedy y Suba semanas 1-2).
4.  **Canales:** Botón de apelación habilitado ("Solicitar segunda revisión").

### 3. Punto de Control (Gate 7): Aprobación del Go-Live

> **DECISIÓN:** ✅ **AUTORIZADO EL GO-LIVE (Fase A - Piloto)**
>
> **Dictamen:** Se autoriza piloto. Estado de *Hypercare* (monitoreo intensivo) por 2 semanas.

---

## Fase 8: Monitoreo y Auditoría

### 1. Contexto de la Ejecución

*   **Periodo:** Primer Trimestre (Feb-Abr 2026).
*   **Fecha de Sesión:** 30/04/2026.

### 2. Actividad 1: Monitoreo Técnico

*   **Resolución Autónoma:** 91.5% (Meta >90%). ✅
*   **Satisfacción (CSAT):** 4.6/5.0. ✅
*   **Equidad:** Gap de error digital/físico en 3.3% (Meta <5%). ✅
*   **Drift:** Leve desviación detectada y gestionada por humanos.

### 3. Actividad 2: Gestión de Incidentes

*   **Incidente INC-2026-003:** Rechazo erróneo por supervisor humano tras derivación de IA. Corregido manualmente. Se reforzó capacitación.

### 4. Actividad 3: Auditoría Interna

*   **Supervisión Humana:** 100% de casos derivados tuvieron acción humana registrada.
*   **Privacidad:** Borrado seguro de imágenes (TTL 30 días) verificado exitosamente.

### 5. Punto de Control (Gate 8): Revisión Trimestral

> **DECISIÓN:** 🔄 **MANTENER**
>
> **Dictamen:** El sistema opera correctamente. Se programa reentrenamiento (v1.1) para incluir nuevos formatos de facturas detectados.

---

## Fase 9: Retiro o Fin de Vida

### 1. Contexto de la Ejecución

*   **Fecha de Sesión (Simulada):** 30/11/2028.
*   **Participantes:** Comité de IA y DPO (A).

### 2. Actividad 1: Decisión y Planificación

*   **Causal:** Obsolescencia Técnica (superado por IA Generativa Multimodal).
*   **Transición:** Migración a plataforma v2.0. Notificación a ciudadanía con 30 días de antelación.

### 3. Actividad 2: Gestión de Datos

1.  **Eliminación Segura:** Borrado de imágenes en hot storage y backups.
2.  **Archivado Legal:** Conservación de logs de auditoría por 5 años (Ley de Archivo).
3.  **Modelo:** Destrucción/Archivo del modelo neuronal v1.0.

### 4. Actividad 3: Lecciones Aprendidas

*   **Éxito:** Integración de bases de datos y protocolo HITL.
*   **Fallo:** Dificultades persistentes del OCR con recibos muy arrugados.
*   **Recomendación:** Usar modelos multimodales en v2.0.

### 5. Punto de Control (Gate 9): Cierre

> **DECISIÓN:** ✅ **APROBADO EL RETIRO DEFINITIVO**
>
> **Dictamen:** Terminación del ciclo de vida del sistema 'Chatbot Certificado Residencia v1.0'. Archivo del expediente.