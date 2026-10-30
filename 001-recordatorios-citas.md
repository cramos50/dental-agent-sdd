# Feature: Recordatorios y confirmación de citas

## 1. Problema

El consultorio de la Dra. Laura registra sus citas mediante Google Calendar, pero aproximadamente el 30% de los pacientes no asiste.

La asistente actualmente revisa las citas y envía recordatorios manualmente por WhatsApp. Este proceso consume tiempo y no permite conocer fácilmente qué pacientes confirmaron su asistencia.

Necesitamos automatizar el recordatorio y la confirmación de citas sin reemplazar Google Calendar.

## 2. Objetivo

Permitir que el sistema identifique las próximas citas, genere automáticamente un recordatorio y registre la respuesta del paciente.

Estados soportados:
- Pendiente
- Confirmada
- Cancelada
- Reprogramación solicitada

## 3. Diseño de la solución

1. El sistema obtiene las próximas citas.
2. Identifica aquellas dentro de la ventana configurada de recordatorio.
3. Genera un recordatorio para el paciente.
4. El paciente puede confirmar, cancelar o solicitar reprogramación.
5. El sistema registra la respuesta.
6. La asistente consulta el estado actualizado desde un panel.

### Panel

Debe mostrar como mínimo:
- nombre del paciente;
- fecha;
- hora;
- estado de la cita;
- estado del recordatorio.

## 4. Integraciones

La arquitectura debe permitir integrar Google Calendar y WhatsApp. Para este demo se utilizan datos simulados y una simulación del envío/respuesta de WhatsApp.

## 5. Criterios de aceptación

### CA-01 — Identificación de citas
Dada una lista de citas, cuando exista una cita dentro de la ventana configurada de recordatorio, el sistema debe identificarla como candidata.

### CA-02 — Recordatorio
Cuando una cita sea candidata y todavía no tenga un recordatorio enviado, el sistema debe generar un único recordatorio con nombre, fecha y hora. Ejecutar nuevamente el proceso no debe duplicarlo.

### CA-03 — Confirmación
Cuando el paciente seleccione “Confirmar”, la cita debe cambiar de Pendiente a Confirmada y mostrarse así en el panel.

### CA-04 — Cancelación o reprogramación
“Cancelar” cambia el estado a Cancelada. “Reprogramar” cambia el estado a Reprogramación solicitada.

### CA-05 — Visualización
El panel debe mostrar las citas con nombre, fecha/hora y estado actualizado, permitiendo identificar las pendientes.

## 6. Fuera de alcance

Facturación, expedientes clínicos, diagnósticos, pagos, inventario, reprogramación automática y creación automática de citas por WhatsApp.
