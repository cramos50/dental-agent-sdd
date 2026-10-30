# AGENTS.md

## Proyecto

Este proyecto desarrolla una solución sencilla de automatización para el consultorio dental de la Dra. Laura.

El problema principal es que aproximadamente el 30% de los pacientes no asiste a sus citas. Actualmente las citas se gestionan correctamente mediante Google Calendar, pero la asistente debe enviar manualmente recordatorios por WhatsApp.

La aplicación debe reducir las inasistencias automatizando la comunicación con los pacientes sin reemplazar Google Calendar ni obligarlos a instalar una aplicación.

## Usuarios

### Dra. Laura
Odontóloga y propietaria del consultorio.

### Asistente
Gestiona citas y atención administrativa. Necesita identificar rápidamente qué pacientes confirmaron, cancelaron o necesitan atención.

### Paciente
Recibe comunicaciones mediante WhatsApp y debe poder confirmar, cancelar o solicitar reprogramación fácilmente.

## Principios del proyecto

- Mantener la solución sencilla.
- Google Calendar continúa siendo la fuente principal de las citas.
- WhatsApp es el canal principal de comunicación.
- Los pacientes no deben instalar aplicaciones.
- Automatizar tareas repetitivas.
- Permitir intervención humana cuando sea necesaria.
- No almacenar información clínica innecesaria.
- Diseñar primero para dispositivos móviles.
- Mantener una interfaz clara para usuarios con poca experiencia técnica.

## Fuera de alcance

No implementar facturación, historia clínica, diagnósticos, prescripciones, inventario, pagos ni gestión clínica completa.

## Reglas de desarrollo

1. Revisar la especificación antes de implementar o modificar una funcionalidad.
2. Implementar únicamente lo definido en la spec.
3. No agregar funcionalidades no solicitadas.
4. Validar todos los criterios de aceptación.
5. Si existe una contradicción entre implementación y spec, la spec es la fuente de verdad.
6. Si la spec resulta incorrecta o insuficiente, corregir primero la spec y luego la implementación.
7. Mantener separadas la lógica de negocio, interfaz e integraciones externas.

## Objetivo

Reducir las inasistencias y el trabajo manual de la asistente mediante automatización de recordatorios y confirmaciones de citas.
