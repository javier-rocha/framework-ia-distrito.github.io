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

### 2. Actividad 1: Capacitación y Gestión del Cambio

Antes de activar el sistema, se ejecutó el plan de formación para garantizar que el componente humano del sistema ("Human-in-the-loop") fuera competente.

*   **Funcionarios Supervisores:** Se capacitó al equipo de Atención al Ciudadano en el manejo de la "Bandeja de Excepciones".
    *   *Enfoque:* Cambio de rol de "validadores de todo" a "gestores de excepciones".
    *   *Protocolo:* Instrucción clara de que ante la duda razonable en una imagen borrosa, prevalece el criterio humano garantista (pro-ciudadano).
*   **Ciudadanía:** Se publicaron infografías en el portal web explicando el nuevo trámite inmediato y cómo tomar correctamente la foto del recibo para evitar rechazos técnicos.

---

### 3. Actividad 2: Configuración de Controles y Monitoreo

El equipo técnico activó la infraestructura de observabilidad definida en el ARA/DPIA:

*   **Logs de Auditoría:** Activación del registro inmutable de transacciones (`Input_ID`, `Score_Confianza`, `Decisión`, `Timestamp`).
*   **Dashboard de Gobernanza:** Se habilitó el tablero en tiempo real para monitorear:
    *   Tasa de Derivación a Humanos (Meta: <15%).
    *   Tiempos de Respuesta (Meta: <3 min).
    *   Alertas de *Drift* (si la distribución de proveedores de recibos cambia drásticamente).

---

### 4. Actividad 3: Estrategia de Despliegue Gradual

Siguiendo la instrucción del Gate 6, se optó por un lanzamiento faseado para minimizar riesgos operativos.

*   **Fase A (Semana 1-2): Piloto Controlado.**
    *   *Alcance:* Habilitado solo para solicitudes originadas en las localidades de **Kennedy y Suba**.
    *   *Objetivo:* Validar carga y comportamiento con documentos reales en zonas de alta demanda.
*   **Fase B (Semana 3+): Escalamiento General.**
    *   *Condición:* Si no se presentan incidentes críticos en Fase A, se abre a todo el Distrito.

---

### 5. Actividad 4: Comunicación y Canales de Apelación

Se implementaron los mecanismos de transparencia y defensa del ciudadano:

*   **Transparencia Activa:** El Chatbot inicia con el mensaje: *"Hola, soy un asistente virtual automatizado. Estoy aquí para validar tus documentos y expedir tu certificado al instante."*
*   **Botón de Apelación:** En caso de que el sistema (o el humano supervisor) rechace la solicitud, se habilitó un botón visible: *"No estoy de acuerdo, solicitar segunda revisión"*, que escala el caso a un nivel superior.

---

### 6. Punto de Control (Gate 7): Aprobación del Go-Live

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
*Documento generado para el expediente del proyecto en el Registro Central de Casos de Uso de IA.*