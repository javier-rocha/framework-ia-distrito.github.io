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

---

### 3. Actividad 2: Valoración Preliminar Multidisciplinaria

El borrador del canvas fue sometido a un "filtro de viabilidad" por los roles clave:

*   **Responsable Técnico:** Confirma la viabilidad técnica de la solución (OCR/NLP) y establece KPIs técnicos (Precisión ≥ 98%).
*   **Delegado de Protección de Datos (DPO):** Identifica la necesidad de un **ARA/DPIA** en fases posteriores debido al tratamiento masivo de datos personales y la toma de decisiones automatizada.
*   **Área Jurídica:** Valida la base legal (Ejercicio de funciones públicas y simplificación de trámites) y la conformidad con la Ley 1581 de 2012.

---

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