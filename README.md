# Sistema de Gestión de Asistencia — EETN N.° 1

## Descripción general

Sistema digital que reemplaza, en parte, el registro físico de asistencia en planillas y hojas de papel. Permite a preceptores, profesores de taller y profesores de educación física registrar la asistencia diaria desde un dispositivo móvil (app), mientras que los roles administrativos y de supervisión acceden a una versión de escritorio para gestionar usuarios, cursos, alumnos, reportes y configuraciones del ciclo lectivo.

## Alcance funcional

- Registro de asistencia diaria (teóricas, taller y educación física) desde app móvil.
- Gestión de tardanzas con equivalencia a faltas (cada 4 tardanzas = 1 falta general).
- Tres contadores de faltas por área + contador general por alumno.
- Alertas automáticas por superación del 20 % de inasistencias, por acumulación de 3 faltas sin aviso y por asistencia perfecta trimestral.
- Registro de faltas justificadas con notificación cruzada entre preceptoría y taller.
- Reportes semanales, mensuales y trimestrales exportables en formato Excel
- Gestión administrativa completa desde la versión web.
- Calendario escolar con registro de días sin clases (feriados, paros, etc.)

## Roles del sistema

## Acceso desde app móvil

Preceptor: toma asistencia de sus cursos. Registra tardanzas y justificaciones. Puede modificar durante el dia.
profesores de taller: toma asistencia de sus grupos de taller asignado.
preceptor de taller: verifica y envía la asistencia de taller a preceptoria.
profesor de educación física: toma asistencia de sus grupos.

## Acceso desde versión web

jefa de preceptores: corrige asistencia sin restricción de fecha, por el momento. Realiza cargas semanalmente.
jefe de taller: solo lectura de asistencia en los talleres, gestiona notificaciones de justificaciones.
director: solo lectura, acceso a todos los reportes y estadísticas.
administrador del sistema: acceso total, configuración de roles, cursos, alumnos, calendario, elimina registros. Comparte las tareas junto a la preceptora.

## Estados de asistencia

presente: ninguno.
ausente: suma 0.5 al contador del área y al contador general.
tardanza: suma 1 al contador global de tardanzas. Cada 4 tardanzas suman 1 falta al contador general.
falta justificada: se registra en un contador paralelo. No modifica los contadores de asistencia.

## Requisitos funcionales principales

— Administración del sistema (ciclo lectivo, usuarios, cursos, alumnos).
— Registro de asistencia (flujos para teóricas, taller y educación física).
— Estados de asistencia.
— Sistema de contadores (por área, general, tardanzas y justificaciones).
— Gestión de faltas justificadas con notificación cruzada.
— Alertas automáticas (límite, seguimiento, asistencia perfecta).
— Reportes y estadísticas exportables en Excel.

## Datos principales del sistema

- Alumnos: nombre, DNI, curso, grupo de taller, grupo de educación física.
- Asistencia: fecha, área, estado, hora, usuario registrador, observaciones.
- Cursos: año, división, turno, preceptores asignados, lista de alumnos.
- Grupos de taller: año, nombre, especialidad, profesores, preceptor de taller, alumnos.
- Grupos de educación física: año, nombre, profesor, alumnos.
- Justificaciones:alumno, fechas, tipo, fecha de presentación, área receptora, estado de notificación cruzada.
- Días sin clases: fecha, motivo, alcance (todos los turnos o turno específico).

## Tecnologías

Laravel, Flutter, MySQL (Versiones)
Librerias? 

## Integrantes del equipo

Leonardo Sarmiento - Gutierrez Nicolás

## Institución

Escuela de Educación Técnica N.° 1 Cnel. Manuel Álvarez Prado — San Pedro de Jujuy, Jujuy, Argentina.
