# GrupoC-_App_movimilagro
Integrantes:
- Mathias Ariel Abad Jiménez
- Kenneth Adonis Anchundia Arrieta
- Jonathan Stalin Tagua Soria
- Jonatan Josue Acosta Herrera
- Joselyn Guadalupe Leal Rios
- Jostin Juber Amaguaya Mendoza

MoviMilagro es una aplicación pensada para conectar a pasajeros con conductores particulares y facilitar los viajes dentro de la ciudad de manera rápida y ordenada. 
Para dar este servicio, la plataforma necesita usar la ubicación en tiempo real de ambos mientras dura cada recorrido, lo que exige cuidar mucho la privacidad de las personas. 
En este trabajo de Introducción a la ingeniería de software, analizamos los riesgos éticos de compartir la ubicación y definimos requisitos claros junto con sus pruebas. 
El objetivo es lograr una aplicación segura, transparente y que proteja los datos de todos los usuarios.

## Tabla de requisitos y pruebas de la actividad 1
| ID | Tipo de requisito | Descripción del requisito | Caso de prueba propuesto | Resultado esperado |
| :--- | :--- | :--- | :--- | :--- |
| RF-01  | Funcional | El sistema debe mantener desactivada por defecto la captura de ubicación fuera de viajes activos y permitir al conductor activarla o desactivarla libremente desde su configuración, previa información clara sobre su finalidad (mapas de calor y análisis de demanda) y consentimiento explícito.  | CP-01: Ingresar a la configuración de ubicación de un conductor, comprobar el estado inicial, aceptar el aviso para activar el rastreo fuera de viaje y luego desactivarlo.  |El permiso inicia desactivado sin registrar rutas fuera de servicio; al activarlo con consentimiento se envía la ubicación, y al desactivarlo el rastreo se detiene de inmediato.|
| RF-02  | Funcional | El sistema debe ejecutar una purga o eliminación automática de las coordenadas detalladas del recorrido una vez finalizado el viaje y cumplido el plazo máximo de retención, evitando guardar historiales de rutas por meses.  | CP-02: Completar un viaje de prueba entre pasajero y conductor, registrar el cierre y simular el cumplimiento del plazo de retención en el sistema.  | Se eliminan automáticamente los registros detallados del recorrido finalizado sin conservar historiales prolongados de rutas personales.  |
| RF-03  | Funcional  | El sistema debe anonimizar las ubicaciones usadas para análisis de demanda y distribución de vehículos, registrando únicamente puntos geográficos sin asociarlos al nombre, perfil o identificador del conductor.  | CP-03: Activar el envío de ubicación para análisis de demanda en una cuenta autorizada, generar puntos en distintas zonas y revisar el registro en la tabla analítica.  | Queda guardado solo el punto geográfico para el mapa de calor sin datos que identifiquen al conductor ni permitan inferir su domicilio o hábitos. |
| RNF-01 | No funcional | El sistema debe permitir ser fácil de usar y presentar opciones con nombres claros. | Pedir a una persona que busque la ruta sin recibír ayuda. | La persona  encuentra y consulta una ruta sin dificultad. |
| RNF-02 | No funcional  | El sistema debe mostrar los resultados de cada consulta en cinco segundos o menos. | Consultar rutas, paradas y horarios y medir el tiempo de respuesta. | Cada consulta muestra su información en un máximo de cinco segundos  |

## Documento PDF
[Documento PDF de Requerimientos y Pruebas]()
