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

### 2. Actividad 1: Selección y Evaluación del Proveedor (Motor OCR)

Dado que la entidad no cuenta con la capacidad para desarrollar un motor de OCR/NLP desde cero, se procedió a la adquisición de una solución de mercado. Se aplicó el **Checklist de Evaluación de Proveedores de IA** (versión Estándar para Alto Riesgo).

#### Resumen de la Evaluación
*   **Proveedor Evaluado:** VisionTech OCR Services.
*   **Resultado del Checklist:** **RECOMENDADO** (Cumplimiento de criterios mandatorios).
*   **Hallazgos Clave:**
    *   **Conformidad Regulatoria:** El proveedor presentó certificación de conformidad con la Ley 1581 y aceptó firmar el DPA del Distrito.
    *   **Transparencia (Caja Blanca):** Se obligó contractualmente a la entrega de la *Model Card* del modelo base y el *Data Sheet* de sus datos de entrenamiento.
    *   **Seguridad:** Cuenta con certificación ISO 27001 vigente.
    *   **Auditoría:** Aceptó la cláusula de "Derecho a Auditoría" por parte del Distrito.

---

### 3. Actividad 2: Desarrollo Interno e Integración con Gobernanza

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

### 4. Actividad 3: Formalización Contractual

El Área Jurídica, con apoyo del DPO, blindó la contratación del motor OCR mediante cláusulas específicas.

#### Cláusulas de Gobernanza Incluidas
*   **Acuerdo de Procesamiento de Datos (DPA):** Define al Distrito como Responsable y a VisionTech como Encargado. Prohíbe el uso de los datos del Distrito para re-entrenar los modelos comerciales del proveedor.
*   **SLA de Precisión:** Se establece un nivel de servicio donde la precisión del OCR no puede ser inferior al 95%. Penalizaciones económicas por degradación del modelo.
*   **Portabilidad:** Obligación de devolver o destruir todos los datos al finalizar el contrato.

---

### 5. Punto de Control (Gate 5): Revisión de la Solución y Contrato

El Comité Técnico y Jurídico revisó los entregables antes de autorizar el paso a pruebas.

#### Decisión del Gate 5

> **DECISIÓN:** ✅ **APROBADO**
>
> **Dictamen:**
> "Se aprueba la arquitectura híbrida y el contrato con VisionTech OCR Services.
> *   **Verificación Técnica:** La integración implementa correctamente el flujo de derivación a humanos (HITL).
> *   **Verificación Jurídica:** El contrato incluye las salvaguardas de la Ley 1581 y garantías de auditoría.
>
> **Instrucción:** Proceder a la **Fase 6 - Pruebas y Validación**, donde se deberá ejecutar el test de equidad (diferencia de error < 5%) exigido en la Fase 3."

---
*Documento generado para el expediente del proyecto en el Registro Central de Casos de Uso de IA.*