# Feature 002: Seguimiento de tratamientos pendientes

## Problema
Algunos pacientes comienzan tratamientos de varias sesiones y dejan de asistir antes de terminarlos. La asistente no cuenta con una forma sencilla de identificar y seguir estos casos.

## Objetivo
Identificar pacientes con tratamientos activos, sesiones pendientes y sin próxima cita, y facilitar una acción administrativa de seguimiento.

## Diseño
El dashboard incluye **Tratamientos por recuperar** con nombre, tratamiento, progreso, última visita y estado.

Estados: `Requiere seguimiento`, `Contactado`, `Cita programada`.

Un paciente requiere seguimiento cuando:
1. tiene tratamiento activo;
2. tiene sesiones pendientes;
3. no tiene próxima cita.

Al seleccionar **Contactar**, se genera un mensaje administrativo personalizado. WhatsApp y la programación se simulan en el demo.

## Criterios de aceptación
### CA-01 — Detección
Un paciente con tratamiento activo, sesiones pendientes y sin próxima cita debe clasificarse como `Requiere seguimiento`.

### CA-02 — Exclusión
Un paciente con próxima cita no debe aparecer en pendientes por recuperar.

### CA-03 — Información
Cada seguimiento muestra nombre, tratamiento, progreso y última visita.

### CA-04 — Contacto
`Contactar` genera un mensaje personalizado y cambia el estado a `Contactado`.

### CA-05 — Actualización
Al registrar próxima cita cambia a `Cita programada` y sale de pendientes.

## Métricas de éxito
- **Tasa de recuperación:** pacientes que agendan / pacientes contactados. Objetivo ≥ 30%.
- **Abandono:** reducir tratamientos abandonados ≥ 20% en tres meses.
- **Tiempo administrativo:** reducir ≥ 50% el tiempo de identificación manual.
- **Cobertura:** detectar 100% de tratamientos registrados que cumplan las reglas.

## Fuera de alcance
Historia clínica, diagnóstico, prescripciones, facturación, pagos, notas médicas y recomendaciones clínicas automatizadas.
