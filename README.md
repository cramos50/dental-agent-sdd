# Dental Agent — Dra. Laura

Proyecto académico construido con **Spec Driven Development** para resolver el problema de inasistencias en un consultorio dental.

## Feature implementado

Recordatorios y confirmación de citas.

El demo permite:
- visualizar las citas y sus estados;
- procesar recordatorios sin duplicarlos;
- simular el mensaje enviado al paciente;
- confirmar una cita;
- cancelar una cita;
- solicitar reprogramación;
- actualizar inmediatamente el panel.

## Estructura

- `AGENTS.md`: contexto persistente e instrucciones generales.
- `specs/001-recordatorios-citas.md`: especificación del feature.
- `skills/dental-brand/SKILL.md`: skill de diseño de marca.
- `src/index.html`: implementación funcional del demo.

## Ejecutar

No requiere instalación.

Abre `src/index.html` en un navegador.

También puede servirse con cualquier servidor HTTP estático.

## Integraciones

Para mantener el alcance académico, Google Calendar y WhatsApp están simulados. La spec define que la arquitectura debe permitir reemplazar posteriormente estas simulaciones por integraciones reales.

## Criterios de aceptación

La implementación demuestra los cinco criterios definidos en la spec:
1. identificación de citas candidatas;
2. recordatorio único;
3. confirmación;
4. cancelación/reprogramación;
5. visualización del estado actualizado.

## Alcance

No incluye facturación, expediente clínico, diagnósticos, pagos, inventario ni gestión clínica completa.
