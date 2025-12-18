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

### 2. Actividad 1: Evaluación de Calidad y Representatividad

El Propietario de Datos (Data Steward), junto con el equipo técnico, realizó una auditoría exhaustiva del conjunto de datos denominado **RESIDENCIA_BOG_VALIDATION_V1**.

#### A. Inventario y Calidad Dimensional
*   **Volumen:** 15,000 registros (Imágenes PDF/JPG y texto extraído).
*   **Completitud:** Menos del 2% de datos faltantes en campos no estructurados.
*   **Consistencia:** Se identificaron inconsistencias en formatos de dirección (ej. "Cll" vs "Calle"), las cuales fueron normalizadas.

#### B. Análisis de Representatividad y Hallazgos de Sesgo
Durante el análisis estadístico, se detectó un riesgo significativo de sesgo en la composición original del dataset:
*   **Hallazgo:** El 80% de las facturas correspondían al proveedor **Enel** en formato nativo digital.
*   **Riesgo:** El modelo podría fallar sistemáticamente con recibos de otros proveedores (Acueducto, Vanti) o con formatos físicos escaneados, discriminando a ciudadanos que no reciben factura digital.
*   **Acción Correctiva:** Se aplicó una técnica de balanceo (oversampling) enriqueciendo el dataset con muestras de otros proveedores y fotografías de baja calidad tomadas con celulares de gama baja.

---

### 3. Actividad 2: Elaboración de Data Sheets y Mitigación

Se documentó el conjunto de datos utilizando la plantilla estándar de **Data Sheet** del framework, asegurando transparencia sobre su origen y limitaciones.

#### Resumen del Data Sheet (RESIDENCIA_BOG_VALIDATION_V1)
*   **Propósito:** Entrenar modelos OCR/NLP para validación de identidad y residencia.
*   **Datos Personales:** Sí (Nombres, Cédulas, Direcciones).
*   **Datos Sensibles:** No.
*   **Base Legal:** Ejercicio de funciones públicas y simplificación de trámites.
*   **Transformaciones:** Pre-procesamiento de imágenes (contraste) y normalización de texto.
*   **Usos Prohibidos:** Se estableció explícitamente la prohibición de usar estos datos para evaluar capacidad de pago, crear mapas de morosidad o compartir con terceros comerciales.

---

### 4. Punto de Control (Gate 4): Certificación de la Calidad de los Datos

El Propietario de Datos y el DPO realizaron la revisión final del Data Sheet y la calidad del dataset enriquecido.

#### Certificación del Propietario de Datos y DPO

> **DECISIÓN:** ✅ **APROBADO CON CONDICIÓN DE EQUIDAD**
>
> **Dictamen:**
> "Se certifica que el dataset cumple con los estándares de calidad y que se han aplicado las medidas correctivas para mitigar el sesgo de proveedor.
>
> **Condición para Fase 6:** No se autoriza el despliegue hasta que se demuestre estadísticamente en la Fase de Pruebas que el modelo reconoce con igual precisión (diferencia <5%) una factura digital y una fotografía de celular de un recibo físico."

> **Instrucción:** El dataset queda habilitado para ser utilizado por el equipo de desarrollo en la **Fase 5**.