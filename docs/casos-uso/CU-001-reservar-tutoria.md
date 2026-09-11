|Campo | Descripcion|
|------|------------|
|ID| CU-001| 
|Nombre|Reservar Tutoria|
|RF Relacionado| RF-004|
|Actor Principal|Estudiante| 
|Objetivo| Reservar un espacio de tutoría disponible para una materia seleccionada|
|Precondiciones| 1. El estudiante debe estar registrado e iniciar sesión en el sistema. <br> 2. Deben existir tutorías disponibles para la materia seleccionada.|
|Flujo Principal|1. Estudiante: Selecciona la opción "Reservar Tutoría". <br> 2. Sistema: Muestra las materias disponibles para tutoría. <br> 3. Estudiante: Selecciona la materia que desea consultar. <br> 4. Sistema: Muestra los espacios de tutoría disponibles para la materia seleccionada. <br> 5. Estudiante: Selecciona el horario de su preferencia. <br> 6. Sistema: Muestra el resumen de la reserva y solicita confirmación. <br> 7. Estudiante: Confirma la reserva. <br> 8. Sistema: Registra la reserva y muestra un mensaje de confirmación. |
|Flujo Alternativo| FA-01: Selección de otro horario. En el paso 5, si el estudiante desea otro horario, puede regresar a la lista de espacios disponibles y seleccionar una opción diferente. El sistema actualiza el resumen de la reserva con el nuevo horario.|
|Excepciones| E-01: Si no existen espacios disponibles para la materia seleccionada, el sistema muestra un mensaje indicando que no hay horarios disponibles y permite al estudiante seleccionar otra materia. <br> E-02: Si el espacio seleccionado deja de estar disponible antes de confirmar la reserva, el sistema informa al estudiante y solicita seleccionar otro horario disponible.|
|Postcondiciones| Éxito: La reserva queda registrada para el estudiante, la materia y el horario seleccionado, y el espacio deja de estar disponible para nuevas reservas. <br> Fallo: Si la reserva no puede completarse, no se registra ninguna reserva y el estudiante puede intentar seleccionar otro espacio disponible. |


