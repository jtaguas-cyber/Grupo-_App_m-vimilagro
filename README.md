# GrupoC - App_movimilagro
## Integrantes:
- Mathias Ariel Abad Jiménez
- Kenneth Adonis Anchundia Arrieta
- Jonathan Stalin Tagua Soria
- Jonatan Josue Acosta Herrera
- Joselyn Guadalupe Leal Rios
- Jostin Juber Amaguaya Mendoza

## Introducción
MoviMilagro es una aplicación pensada para conectar a pasajeros con conductores particulares y facilitar los viajes dentro de la ciudad de forma rápida y ordenada. Para dar este servicio, la plataforma usa la ubicación en tiempo real, pero querer rastrear a los conductores fuera de su horario de trabajo y guardar sus recorridos por meses afecta su privacidad y seguridad. En este proyecto de Introducción a la ingeniería de software, transformamos este problema en requisitos funcionales y no funcionales con sus respectivos casos de prueba. Así buscamos lograr una aplicación segura, que cifre los datos y permita controlar la ubicación de manera fácil y transparente.

## Tabla de requisitos y pruebas de la actividad 1
| ID | Tipo de requisito | Descripción del requisito | Caso de prueba propuesto | Resultado esperado |
| :--- | :--- | :--- | :--- | :--- |
| RF-01  | Funcional | El sistema debe mantener desactivada por defecto la captura de ubicación fuera de viajes activos y permitir al conductor activarla o desactivarla libremente desde su configuración, previa información clara sobre su finalidad (mapas de calor y análisis de demanda) y consentimiento explícito.  | CP-01: Ingresar a la configuración de ubicación de un conductor, comprobar el estado inicial, aceptar el aviso para activar el rastreo fuera de viaje y luego desactivarlo.  |El permiso inicia desactivado sin registrar rutas fuera de servicio; al activarlo con consentimiento se envía la ubicación, y al desactivarlo el rastreo se detiene de inmediato.|
| RF-02  | Funcional | El sistema debe ejecutar una purga o eliminación automática de las coordenadas detalladas del recorrido una vez finalizado el viaje y cumplido el plazo máximo de retención, evitando guardar historiales de rutas por meses.  | CP-02: Completar un viaje de prueba entre pasajero y conductor, registrar el cierre y simular el cumplimiento del plazo de retención en el sistema.  | Se eliminan automáticamente los registros detallados del recorrido finalizado sin conservar historiales prolongados de rutas personales.  |
| RF-03  | Funcional  | El sistema debe anonimizar las ubicaciones usadas para análisis de demanda y distribución de vehículos, registrando únicamente puntos geográficos sin asociarlos al nombre, perfil o identificador del conductor.  | CP-03: Activar el envío de ubicación para análisis de demanda en una cuenta autorizada, generar puntos en distintas zonas y revisar el registro en la tabla analítica.  | Queda guardado solo el punto geográfico para el mapa de calor sin datos que identifiquen al conductor ni permitan inferir su domicilio o hábitos. |
| RNF-01 | No funcional | El sistema debe cifrar los datos de ubicación GPS en tiempo real y restringir el acceso a la base de datos únicamente a personal autorizado. | CP-04: Intentar acceder a la base de datos de ubicaciones desde una cuenta sin permisos de administrador y revisar el envío de datos. | El sistema bloquea el acceso no autorizado y las coordenadas viajan cifradas sin quedar expuestas. |
| RNF-02 | No funcional  | El conductor debe poder activar o desactivar el rastreo de ubicación fuera de viaje en un máximo de dos clics y en menos de 10 segundos desde la pantalla principal.| CP-05: Entrar a la aplicación con una cuenta de conductor, medir el tiempo y contar los clics necesarios para apagar la ubicación fuera de servicio. | El conductor logra desactivar el rastreo en 2 clics o menos y en un tiempo inferior a 10 segundos. |

## Documento PDF
[Documento PDF de Requerimientos y Pruebas]()
