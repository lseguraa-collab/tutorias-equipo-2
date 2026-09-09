## Requerimientos Funcionales

| Campo                  | Contenido esperado |
|------------------------|--------------------|
| ID                     | RF-001                   |
| Nombre                 | Consultar tutor y materias disponibles.                    |
| Actor                  | Estudiante                   |
| Descripción            | El sistema debe permitir al estudiante consultar qué tutor está disponible y cuáles son las materias atiende para la fecha seleccionada.                    |
| Resultado esperado     | Se muestran los tutores y materias disponibles para la fecha seleccionada.                    |
| Fuente                 | Necesidad identificada: Los estudiantes necesitan consultar de manera clara qué tutor atiende cada materia y cuáles horarios están disponibles.                   |
| Método de verificación | Seleccionar una fecha y comprobar que no aparecen espacios de fechas diferentes.                    |

| Campo                  | Contenido esperado |
|------------------------|--------------------|
| ID                     | RF-002                   |
| Nombre                 | Consultar disponibilidad de horarios                   |
| Actor                  | Estudiante                    |
| Descripción            | El sistema debe permitir al estudiante consultar en tiempo real si un horario se encuentra disponible antes de realizar una reserva.                   |
| Resultado esperado     | El sistema indica si el horario seleccionado está disponible o no para realizar la consulta.                    |
| Fuente                 | Necesidad identificada: Los estudiantes necesitan conocer inmediatamente si un horario continúa disponible antes de realizar una reserva.                    |
| Método de verificación | Seleccionar un horario disponible y comprobar que el sistema indique su disponibilidad antes de confirmar la reserva.                   |

| Campo                  | Contenido esperado |
|------------------------|--------------------|
| ID                     | RF-003                   |
| Nombre                 | Validar disponibilidad al realizar una reserva                    |
| Actor                  | Estudiante                    |
| Descripción            | El sistema debe verificar nuevamente la disponibilidad del horario al momento de confirmar una reserva, evitando que sea asignado si otra persona lo reservó previamente.                    |
| Resultado esperado     | El sistema confirma la reserva únicamente si el horario continúa disponible. De lo contrario, informa al estudiante que el horario ya fue reservado.                   |
| Fuente                 | Necesidad identificada: Existe el riesgo de que un horario sea reservado por otra persona antes de que el estudiante reciba respuesta.                    |
| Método de verificación | Intentar reservar un horario que haya sido reservado previamente y comprobar que el sistema rechace la reserva e informe que ya no está disponible.                    |

## Requerimientos No Funcionales

| Campo                 | Contenido esperado |
|-----------------------|--------------------|
| ID                    | RNF - 001          |
| Atributo              | Rendimiento                   |
| Escenario / Condición | Cuando un usuario reserva una sesión en el sistema, sin importar el tutor, la materia ni el horario elegido.                   |
| Métrica               | Duración en minutos de cada sesión reservada (50 min)                  |
| Umbral / Criterio     | El sistema no debe permitir crear, editar ni guardar sesiones con una duración distinta a la establecida                   |
| Fuente                | F-05 Restricciones entregadas por el patrocinador didáctico                   |
| Método Verificación   | Por definir                   |

| Campo                 | Contenido esperado |
|-----------------------|--------------------|
| ID                    | RNF - 002                    |
| Atributo              | Disponibilidad                   |
| Escenario / Condición | Cuando un usuario autenticado intenta reservar una sesión teniendo ya sesiones activas (pendientes o confirmadas) registradas en el sistema.                   |
| Métrica               | Cantidad de sesiones activas reservadas por usuario.                   |
| Umbral / Criterio     | Máximo 2 sesiones activas por usuario. Al intentar reservar una tercera, el sistema debe rechazar la solicitud y mostrar un mensaje indicando que se alcanzó el límite.                   |
| Fuente                | F-05 Restricciones entregadas por el patrocinador didáctico                   |
| Método Verificación   | Por definir                   |