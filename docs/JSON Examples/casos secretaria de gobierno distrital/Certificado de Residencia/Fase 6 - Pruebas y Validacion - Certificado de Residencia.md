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

### 2. Actividad 1: Pruebas Técnicas (Robustez, Seguridad y Rendimiento)

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

### 3. Actividad 2: Pruebas de Equidad y No Discriminación

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

### 4. Actividad 3: Pruebas de Transparencia y Explicabilidad

Se validó que el sistema sea transparente para el usuario final y explicable para el auditor.

*   **Notificación al Usuario:** Se verificó que el Chatbot inicia la conversación con el mensaje: *"Hola, soy un asistente virtual automatizado de la Secretaría de Gobierno..."*.
*   **Explicabilidad de la Decisión:**
    *   En caso de aprobación: El sistema informa qué datos validó.
    *   En caso de derivación a humano: El sistema informa *"La calidad de la imagen no permite una validación automática segura. Un funcionario revisará su caso en breve"*. No se generan rechazos "caja negra".

---

### 5. Actividad 4: Pruebas de Usabilidad, Accesibilidad e Integración

*   **Accesibilidad:** Se auditó la interfaz web del Chatbot cumpliendo con **WCAG 2.1 Nivel AA** (compatible con lectores de pantalla).
*   **Integración:** Se verificó la correcta comunicación con la base de datos de radicación y la generación del PDF del certificado firmado digitalmente.
*   **Prueba de Carga:** El sistema soportó 500 peticiones concurrentes sin degradación del servicio (simulando picos de demanda).

---

### 6. Punto de Control (Gate 6): Aprobación para Despliegue

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
*Documento generado para el expediente del proyecto en el Registro Central de Casos de Uso de IA.*