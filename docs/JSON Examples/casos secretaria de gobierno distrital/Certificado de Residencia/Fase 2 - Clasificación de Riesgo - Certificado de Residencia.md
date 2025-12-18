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

### 2. Actividad 1: Aplicación de la Taxonomía de Riesgo

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

> **NIVEL DE RIESGO ASIGNADO:** 🔴 **ALTO RIESGO**

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

### 3. Actividad 2: Determinación de las Obligaciones de Gobernanza

Dada la clasificación de **Alto Riesgo**, se activan automáticamente las siguientes obligaciones reforzadas para las fases subsiguientes:

1.  **Fase 3 (ARA/DPIA):** Es **OBLIGATORIO** realizar una Evaluación de Impacto en Protección de Datos y Riesgos Algorítmicos completa.
2.  **Supervisión Humana:** Se exige implementar un mecanismo de *Human-in-the-loop* (HITL). No se permiten rechazos automáticos sin revisión.
3.  **Documentación Técnica:** Se requerirá una *Model Card* detallada y *Data Sheets* exhaustivos (Fases 4 y 6).
4.  **Pruebas de Equidad:** En la Fase 6, será obligatorio demostrar que la tasa de error no varía significativamente entre documentos digitales y físicos (riesgo de sesgo por calidad de imagen).
5.  **Auditoría:** El sistema estará sujeto a auditorías externas anuales en la Fase 8.

---

### 4. Punto de Control (Gate 2): Validación de la Clasificación

El Comité de IA revisó la propuesta de clasificación y la justificación presentada.

#### Decisión Final del Comité

> **DECISIÓN:** ✅ **VALIDADA**
>
> **Dictamen:** El Comité de IA ratifica la clasificación de **Alto Riesgo**.
>
> **Instrucción al Equipo:** Proceder inmediatamente a la **Fase 3 - ARA/DPIA** involucrando al DPO. El proyecto **NO** puede avanzar a desarrollo (Fase 5) hasta que el ARA/DPIA sea aprobado en el Gate 3.

---
*Documento generado para el expediente del proyecto en el Registro Central de Casos de Uso de IA.*