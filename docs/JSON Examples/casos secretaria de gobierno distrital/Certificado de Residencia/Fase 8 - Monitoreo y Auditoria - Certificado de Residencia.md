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

### 2. Actividad 1: Monitoreo Técnico Continuo

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
*Documento generado para el expediente del proyecto en el Registro Central de Casos de Uso de IA.*