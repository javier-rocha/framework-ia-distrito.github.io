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

### 2. Actividad 1: Ejecución del Análisis de Impacto y Riesgos

El DPO, junto con el Responsable Técnico, completó la **Plantilla ARA/DPIA** para evaluar los impactos en derechos fundamentales y privacidad.

#### A. Mapeo de Datos y Base Legal
*   **Datos Tratados:** Imágenes de Cédulas de Ciudadanía y Recibos de Servicios Públicos.
*   **Categoría:** Datos Personales (Ley 1581). No son datos sensibles biométricos (no se hace reconocimiento facial 1:N), pero sí datos de alto impacto administrativo.
*   **Base Legal:** Cumplimiento de una obligación legal y ejercicio de funciones públicas (Ley 2052 de 2020 - Simplificación de trámites).
*   **Flujo:** Carga por ciudadano -> Procesamiento en memoria (OCR) -> Validación -> Eliminación de archivo fuente -> Generación de Certificado.

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

### 3. Actividad 2: Diseño del Plan de Mitigación de Riesgos

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

### 4. Punto de Control (Gate 3): Aprobación Vinculante del DPO

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