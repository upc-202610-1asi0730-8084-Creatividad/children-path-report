# **Chapter III: Requirements Specification**
## **3.1. User Stories** 

En esta sección se definen los requisitos funcionales del sistema mediante Epics y User Stories orientadas al valor de los diferentes actores de la solución: Apoderados, Conductores de Movilidad Escolar, Administradores de Empresa y Visitantes del Sitio Web. Asimismo, se contemplan Historias Técnicas para la integración de la API RESTful. Los Criterios de Aceptación han sido redactados en tiempo presente, tercera persona y bajo la estructura formal de Gherkin, garantizando que sean comprobables y desacoplados de detalles visuales.

<table>
    <thead>
        <tr>
            <th style="width: 8%">Epic/Story ID</th>
            <th style="width: 15%">Title</th>
            <th style="width: 30%">Description</th>
            <th style="width: 37%">Acceptance Criteria</th>
            <th style="width: 10%">Related to (Epic ID)</th>
        </tr>
    </thead>
    <tbody>
      <!-- EPIC 0 - LANDING PAGE -->
        <tr>
            <td class="epic-id" style="text-align:center">EP00</td>
            <td style="text-align:center">Portal Web Informativo y Captación (Landing Page)</td>
            <td>Como <strong>visitante del sitio web</strong>, quiero conocer la propuesta de valor, planes de suscripción y canales de contacto de Children Path, para evaluar la adopción del servicio.</td>
            <td class="acceptance-criteria">
                <ul>
                    <li><strong>Dado que</strong> un visitante accede a la dirección web pública, <strong>cuando</strong> carga la página principal, <strong>entonces</strong> el sistema expone el propósito de la plataforma, los beneficios clave por rol y botones de llamada a la acción (CTA).</li>
                    <li><strong>Dado que</strong> el visitante consulta la sección de tarifas, <strong>cuando</strong> revisa la comparativa, <strong>entonces</strong> el sistema muestra los límites y costos de cada plan.</li>
                    <li><strong>Dado que</strong> el visitante envía un formulario de contacto válido, <strong>cuando</strong> el sistema procesa la solicitud, <strong>entonces</strong> registra los datos de prospección y emite una confirmación en pantalla.</li>
                </ul>
            </td>
            <td style="text-align:center">-</td>
        </tr>  
        <!-- EPIC 1 - BOTH -->
<tr>
    <td class="epic-id" style="text-align:center">EP01</td>
    <td style="text-align:center">Registro digital de abordaje</td>
    <td>Como <strong>conductor independiente o administrador de empresa</strong>, quiero registrar rápidamente qué estudiantes abordan o están ausentes en cada parada, para evitar errores y optimizar la ruta.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor ha llegado a una parada programada, <strong>cuando</strong> el estudiante aborda el vehículo, <strong>entonces</strong> el sistema permite registrar el evento de "abordaje" con fecha y hora.</li>
            <li><strong>Dado que</strong> el conductor está en una parada y un estudiante no se presenta, <strong>cuando</strong> transcurren 2 minutos sin registro, <strong>entonces</strong> el sistema notifica automáticamente al padre sobre la ausencia.</li>
            <li><strong>Dado que</strong> el conductor opera sin conexión a internet, <strong>cuando</strong> registra abordajes, <strong>entonces</strong> el sistema almacena los eventos localmente y los sincroniza cuando se restablece la conectividad.</li>
            <li><strong>Dado que</strong> se registra un abordaje, <strong>cuando</strong> el evento es persistido, <strong>entonces</strong> el sistema envía una notificación push al padre del estudiante.</li>
        </ul>
    </td>
    <td style="text-align:center">-</td>
</tr>
<!-- EPIC 2 - BOTH -->
<tr>
    <td class="epic-id" style="text-align:center">EP02</td>
    <td style="text-align:center">Gestión de rutas</td>
    <td>Como <strong>conductor independiente o administrador de empresa</strong>, quiero visualizar y seguir una ruta organizada con paradas definidas, para reducir los tiempos de espera y el consumo de combustible.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor ha iniciado su turno, <strong>cuando</strong> accede a la ruta del día, <strong>entonces</strong> el sistema muestra el orden secuencial de las paradas con los tiempos estimados de llegada.</li>
            <li><strong>Dado que</strong> ocurre un retraso en una parada, <strong>cuando</strong> el sistema detecta el retraso, <strong>entonces</strong> recalcula automáticamente los tiempos estimados para las siguientes paradas.</li>
            <li><strong>Dado que</strong> el conductor ha registrado una ausencia, <strong>cuando</strong> la parada corresponde a ese estudiante, <strong>entonces</strong> el sistema omite automáticamente la parada y reordena la ruta.</li>
            <li><strong>Dado que</strong> el conductor desea ahorrar combustible, <strong>cuando</strong> el sistema detecta una alternativa más eficiente, <strong>entonces</strong> sugiere la ruta óptima considerando el tráfico en tiempo real.</li>
        </ul>
    </td>
    <td style="text-align:center">-</td>
</tr>
<!-- EPIC 3 - BOTH -->
<tr>
    <td class="epic-id" style="text-align:center">EP03</td>
    <td style="text-align:center">Registro de incidencias</td>
    <td>Como <strong>conductor independiente o administrador de empresa</strong>, quiero registrar eventos como retrasos, ausencias o cambios de ruta, para mantener la trazabilidad del servicio.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> ocurre una incidencia en la ruta, <strong>cuando</strong> el conductor selecciona el tipo de incidencia (retraso, accidente, cambio de ruta), <strong>entonces</strong> el sistema registra el evento con ubicación y fecha/hora.</li>
            <li><strong>Dado que</strong> se registra una incidencia, <strong>cuando</strong> la incidencia afecta el tiempo estimado de llegada, <strong>entonces</strong> el sistema notifica automáticamente a los padres afectados.</li>
            <li><strong>Dado que</strong> el conductor necesita documentar una incidencia, <strong>cuando</strong> adjunta evidencia (foto, audio, texto), <strong>entonces</strong> el sistema guarda el adjunto asociado al evento.</li>
            <li><strong>Dado que</strong> la incidencia es cerrada, <strong>cuando</strong> el administrador o conductor consulta el historial, <strong>entonces</strong> se muestra la línea de tiempo completa del evento.</li>
        </ul>
    </td>
    <td style="text-align:center">-</td>
</tr>
<!-- EPIC 4 - COMPANY ONLY -->
<tr>
    <td class="epic-id" style="text-align:center">EP04</td>
    <td style="text-align:center">Monitoreo de flota en tiempo real</td>
    <td>Como <strong>administrador de una empresa de movilidad escolar</strong>, quiero visualizar todos mis vehículos en tiempo real, para supervisar el cumplimiento de rutas y gestionar incidencias.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el administrador accede al panel de control, <strong>cuando</strong> selecciona la vista de flota, <strong>entonces</strong> el sistema muestra un mapa con la ubicación actual de todas las unidades activas de la empresa.</li>
            <li><strong>Dado que</strong> una unidad se desvía de su ruta establecida, <strong>cuando</strong> la desviación supera un umbral configurable, <strong>entonces</strong> el sistema genera una alerta en el panel del administrador.</li>
            <li><strong>Dado que</strong> el administrador selecciona una unidad específica, <strong>cuando</strong> visualiza sus detalles, <strong>entonces</strong> se muestran la ruta recorrida, las paradas realizadas y el estado actual.</li>
            <li><strong>Dado que</strong> ocurre una emergencia en una unidad, <strong>cuando</strong> el conductor reporta la emergencia, <strong>entonces</strong> el sistema resalta la unidad en el panel con un indicador visual de alerta.</li>
            <li><strong>Dado que</strong> una unidad no ha enviado ubicación por más de 5 minutos, <strong>cuando</strong> el monitoreo está en ejecución, <strong>entonces</strong> el sistema genera una alerta de "Unidad sin señal".</li>
        </ul>
    </td>
    <td style="text-align:center">-</td>
</tr>

<!-- EPIC 5A - INDEPENDENT DRIVER ONLY (Personal reports) -->
<tr>
    <td class="epic-id" style="text-align:center">EP05A</td>
    <td style="text-align:center">Reportes personales de viaje</td>
    <td>Como <strong>conductor independiente</strong>, quiero acceder a mi historial de viajes, puntualidad e incidencias, para evaluar mi desempeño y mejorar mi reputación.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor accede a su perfil, <strong>cuando</strong> selecciona "Mi historial", <strong>entonces</strong> el sistema muestra la lista de viajes realizados en los últimos 30 días con fechas y horas.</li>
            <li><strong>Dado que</strong> el conductor quiere conocer su puntualidad, <strong>cuando</strong> consulta su reporte de desempeño, <strong>entonces</strong> el sistema muestra el porcentaje de llegadas a tiempo por parada.</li>
            <li><strong>Dado que</strong> el conductor ha tenido incidencias, <strong>cuando</strong> consulta el registro, <strong>entonces</strong> ve la lista de eventos registrados con sus resoluciones.</li>
            <li><strong>Dado que</strong> el conductor quiere compartir su reputación, <strong>cuando</strong> genera un resumen, <strong>entonces</strong> el sistema permite exportar un reporte simple (PDF) con sus métricas.</li>
        </ul>
    </td>
    <td style="text-align:center">-</td>
</tr>
<!-- EPIC 5B - COMPANY ONLY (Management reports) -->
<tr>
    <td class="epic-id" style="text-align:center">EP05B</td>
    <td style="text-align:center">Reportes de gestión de flota</td>
    <td>Como <strong>administrador de una empresa de movilidad escolar</strong>, quiero generar reportes consolidados de toda la flota (puntualidad, asistencia, combustible, facturación), para evaluar el servicio y tomar decisiones.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el administrador necesita un reporte de puntualidad por conductor, <strong>cuando</strong> selecciona un rango de fechas, <strong>entonces</strong> el sistema genera un reporte con el porcentaje de llegadas a tiempo por unidad.</li>
            <li><strong>Dado que</strong> el administrador requiere el reporte consolidado de asistencia mensual, <strong>cuando</strong> selecciona el mes y la ruta, <strong>entonces</strong> el sistema exporta un archivo Excel con los días de servicio por estudiante (útil para la facturación).</li>
            <li><strong>Dado que</strong> el administrador quiere evaluar el consumo de combustible, <strong>cuando</strong> consulta el reporte de eficiencia, <strong>entonces</strong> el sistema muestra los kilómetros recorridos versus el tiempo con el motor encendido por unidad.</li>
            <li><strong>Dado que</strong> el administrador necesita un reporte de incidencias, <strong>cuando</strong> filtra por tipo de incidencia y período, <strong>entonces</strong> el sistema presenta una tabla con fechas, conductores y descripciones.</li>
            <li><strong>Dado que</strong> el administrador debe justificar la calidad del servicio ante un colegio, <strong>cuando</strong> solicita un reporte ejecutivo, <strong>entonces</strong> el sistema genera un PDF consolidado con los indicadores clave de la flota.</li>
        </ul>
    </td>
    <td style="text-align:center">-</td>
</tr>
<!-- EPIC 6 - PARENTS ONLY -->
<tr>
    <td class="epic-id" style="text-align:center">EP06</td>
    <td style="text-align:center">Supervisión parental y notificaciones</td>
    <td>Como <strong>padre de familia</strong>, quiero recibir notificaciones automáticas y visualizar la ubicación de mi hijo en tiempo real, para tener tranquilidad durante el trayecto escolar sin depender de llamadas o mensajes al conductor.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> un padre de familia ha contratado el servicio, <strong>cuando</strong> un evento relevante ocurre (proximidad, abordaje, llegada, ausencia, incidencia), <strong>entonces</strong> el sistema le envía una notificación automática.</li>
            <li><strong>Dado que</strong> el padre desea consultar la ubicación de su hijo, <strong>cuando</strong> accede a la aplicación, <strong>entonces</strong> el sistema muestra un mapa en tiempo real con la ubicación del vehículo.</li>
            <li><strong>Dado que</strong> el padre necesita revisar el historial de viajes de su hijo, <strong>cuando</strong> accede a la sección correspondiente, <strong>entonces</strong> el sistema muestra los eventos registrados (abordajes, llegadas, ausencias).</li>
        </ul>
    </td>
    <td style="text-align:center">-</td>
</tr>
<!-- EPIC 7 - RESTFUL API -->
        <tr>
            <td class="epic-id" style="text-align:center">EP07</td>
            <td style="text-align:center">Servicios de Integración Backend (RESTful API)</td>
            <td>Como <strong>developer</strong>, quiero disponer de endpoints estandarizados con respuestas HTTP adecuadas, para conectar las aplicaciones cliente con los servicios del dominio.</td>
            <td class="acceptance-criteria">
                <ul>
                    <li><strong>Dado que</strong> un cliente HTTP realiza una solicitud válida a un endpoint REST, <strong>cuando</strong> el backend procesa la petición, <strong>entonces</strong> retorna códigos de estado HTTP semánticos (200, 201, 202, 400, 401, 404, 500) y payloads en formato JSON.</li>
                    <li><strong>Dado que</strong> un endpoint requiere credenciales de seguridad, <strong>cuando</strong> la solicitud carece de un token JWT válido en la cabecera Authorization, <strong>entonces</strong> el servicio rechaza la petición con código HTTP 401 Unauthorized.</li>
                </ul>
            </td>
            <td style="text-align:center">-</td>
        </tr>
<!-- USER STORY 01 - Record student boarding -->
<tr>
    <td class="user-story-id" style="text-align:center">US01</td>
    <td style="text-align:center">Registrar abordaje del estudiante</td>
    <td>Como <strong>conductor</strong>, quiero registrar el momento en que un estudiante aborda el vehículo en cada parada, para mantener un registro digital de asistencia.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor ha llegado a una parada programada y el estudiante está presente, <strong>cuando</strong> el conductor selecciona al estudiante de la lista, <strong>entonces</strong> el sistema registra el evento con fecha, hora y ubicación.</li>
            <li><strong>Dado que</strong> el registro de abordaje es exitoso, <strong>cuando</strong> se completa la acción, <strong>entonces</strong> el sistema envía una notificación push al padre del estudiante con el mensaje "Su hijo ha abordado el bus".</li>
            <li><strong>Dado que</strong> el conductor opera sin conexión a internet, <strong>cuando</strong> registra un abordaje, <strong>entonces</strong> el sistema almacena el evento localmente y lo sincroniza automáticamente cuando se restablece la conectividad.</li>
        </ul>
    </td>
    <td style="text-align:center">EP01</td>
</tr>
<!-- USER STORY 02 - Automatic absence notification -->
<tr>
    <td class="user-story-id" style="text-align:center">US02</td>
    <td style="text-align:center">Notificación automática de ausencia</td>
    <td>Como <strong>conductor</strong>, quiero que el sistema detecte automáticamente cuando un estudiante no se presenta en su parada, para no tener que esperar más de lo necesario ni llamar manualmente al padre.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor ha llegado a una parada programada, <strong>cuando</strong> transcurren 2 minutos sin que se registre el abordaje del estudiante, <strong>entonces</strong> el sistema envía una notificación al padre informándole la ausencia.</li>
            <li><strong>Dado que</strong> la ausencia es notificada, <strong>cuando</strong> el padre responde que el estudiante no asistirá, <strong>entonces</strong> el sistema omite automáticamente la parada y continúa a la siguiente.</li>
            <li><strong>Dado que</strong> la ausencia es notificada pero el estudiante se presenta después del tiempo límite, <strong>cuando</strong> el conductor registra el abordaje tardío, <strong>entonces</strong> el sistema registra el evento con una marca de "demora del estudiante".</li>
        </ul>
    </td>
    <td style="text-align:center">EP01</td>
</tr>
<!-- USER STORY 03 - View optimized route -->
<tr>
    <td class="user-story-id" style="text-align:center">US03</td>
    <td style="text-align:center">Visualizar ruta diaria optimizada</td>
    <td>Como <strong>conductor</strong>, quiero visualizar la ruta del día con el orden de las paradas y los tiempos estimados, para reducir los tiempos de espera y el consumo de combustible.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor ha iniciado su turno, <strong>cuando</strong> accede a la pantalla de ruta, <strong>entonces</strong> el sistema muestra el orden secuencial de las paradas con la dirección y el tiempo estimado de llegada para cada una.</li>
            <li><strong>Dado que</strong> el conductor sigue la ruta sugerida, <strong>cuando</strong> completa una parada, <strong>entonces</strong> el sistema actualiza automáticamente la vista, mostrando la siguiente parada como destino actual.</li>
            <li><strong>Dado que</strong> el conductor se desvía de la ruta sugerida, <strong>cuando</strong> el sistema detecta la desviación, <strong>entonces</strong> recalcula la ruta restante y actualiza los tiempos estimados.</li>
        </ul>
    </td>
    <td style="text-align:center">EP02</td>
</tr>
<!-- USER STORY 04 - Reorder route due to absence -->
<tr>
    <td class="user-story-id" style="text-align:center">US04</td>
    <td style="text-align:center">Reordenar ruta por ausencia</td>
    <td>Como <strong>conductor</strong>, quiero que la ruta se reordene automáticamente cuando un estudiante está ausente, para no perder tiempo pasando por una parada vacía.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> se ha confirmado la ausencia de un estudiante en su parada, <strong>cuando</strong> el sistema recibe la confirmación, <strong>entonces</strong> omite esa parada de la ruta activa y reordena las siguientes.</li>
            <li><strong>Dado que</strong> la ruta ha sido reordenada, <strong>cuando</strong> el conductor visualiza la ruta actualizada, <strong>entonces</strong> los tiempos estimados de llegada han sido recalculados para todas las paradas restantes.</li>
            <li><strong>Dado que</strong> la ausencia fue registrada por el padre antes de que iniciara la ruta, <strong>cuando</strong> el conductor inicia el turno, <strong>entonces</strong> la parada del estudiante ausente no aparece en la ruta del día.</li>
        </ul>
    </td>
    <td style="text-align:center">EP02</td>
</tr>
<!-- USER STORY 05 - Record incident on route -->
<tr>
    <td class="user-story-id" style="text-align:center">US05</td>
    <td style="text-align:center">Registrar incidencia en la ruta</td>
    <td>Como <strong>conductor</strong>, quiero registrar cualquier incidencia que ocurra durante el viaje (retraso, accidente, cambio de ruta), para mantener la trazabilidad del servicio.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> ocurre una incidencia durante el viaje, <strong>cuando</strong> el conductor selecciona el tipo de incidencia (retraso, accidente, desvío, emergencia médica), <strong>entonces</strong> el sistema registra el evento con ubicación, fecha/hora y datos del vehículo.</li>
            <li><strong>Dado que</strong> el conductor necesita documentar la incidencia, <strong>cuando</strong> adjunta una foto o nota de texto, <strong>entonces</strong> el sistema guarda la evidencia asociada al evento.</li>
            <li><strong>Dado que</strong> la incidencia afecta los tiempos de llegada, <strong>cuando</strong> el conductor la registra, <strong>entonces</strong> el sistema recalcula los tiempos estimados y notifica a los padres afectados.</li>
        </ul>
    </td>
    <td style="text-align:center">EP03</td>
</tr>
<!-- USER STORY 06 - Notify parents due to incident (automatic) -->
<tr>
    <td class="user-story-id" style="text-align:center">US06</td>
    <td style="text-align:center">Notificar a los padres por incidencia</td>
    <td>Como <strong>sistema</strong>, quiero notificar automáticamente a los padres cuando se registra una incidencia que afecta la ruta de sus hijos, para mantenerlos informados sin intervención manual del conductor.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> se registra una incidencia que afecta los tiempos estimados, <strong>cuando</strong> el sistema calcula el nuevo tiempo de llegada, <strong>entonces</strong> envía una notificación push a los padres de los estudiantes afectados con el mensaje "El bus se retrasará X minutos".</li>
            <li><strong>Dado que</strong> se registra una incidencia grave (accidente, emergencia), <strong>cuando</strong> el conductor marca el evento como crítico, <strong>entonces</strong> el sistema notifica de inmediato al administrador de la empresa y envía una alerta prioritaria a los padres.</li>
            <li><strong>Dado que</strong> la incidencia es resuelta, <strong>cuando</strong> el conductor confirma que el servicio ha vuelto a la normalidad, <strong>entonces</strong> el sistema envía una notificación "Incidencia resuelta - el servicio continúa con normalidad".</li>
        </ul>
    </td>
    <td style="text-align:center">EP03</td>
</tr>
<!-- USER STORY 07 - View complete fleet on map (Company) -->
<tr>
    <td class="user-story-id" style="text-align:center">US07</td>
    <td style="text-align:center">Visualizar flota completa en el mapa</td>
    <td>Como <strong>administrador de una empresa de movilidad escolar</strong>, quiero visualizar todos mis vehículos activos en un mapa en tiempo real, para supervisar el cumplimiento de rutas sin depender de llamadas telefónicas.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el administrador accede al panel de la empresa, <strong>cuando</strong> selecciona la vista de flota, <strong>entonces</strong> el sistema muestra un mapa con la ubicación actual de todos los vehículos activos, identificados por número o nombre del conductor.</li>
            <li><strong>Dado que</strong> el administrador selecciona un vehículo específico en el mapa, <strong>cuando</strong> hace clic sobre él, <strong>entonces</strong> un panel muestra los detalles de la ruta, las paradas realizadas, el próximo destino y el estado actual.</li>
            <li><strong>Dado que</strong> un vehículo tiene activado el modo de emergencia, <strong>cuando</strong> el administrador visualiza el mapa, <strong>entonces</strong> ese vehículo se resalta con un ícono o color de alerta distintivo.</li>
        </ul>
    </td>
    <td style="text-align:center">EP04</td>
</tr>
<!-- USER STORY 08 - Alert for route deviation -->
<tr>
    <td class="user-story-id" style="text-align:center">US08</td>
    <td style="text-align:center">Recibir alerta por desviación de ruta</td>
    <td>Como <strong>administrador de una empresa de movilidad escolar</strong>, quiero recibir una alerta cuando un vehículo se desvía significativamente de su ruta establecida, para actuar rápidamente ante posibles incidentes.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> un vehículo activo tiene una ruta programada definida, <strong>cuando</strong> su ubicación se desvía más de 500 metros de la ruta planificada, <strong>entonces</strong> el sistema genera una alerta en el panel del administrador.</li>
            <li><strong>Dado que</strong> se genera una alerta de desviación, <strong>cuando</strong> el administrador hace clic en la alerta, <strong>entonces</strong> el sistema muestra la ubicación actual del vehículo y la ruta programada para comparación.</li>
            <li><strong>Dado que</strong> la desviación fue autorizada (por ejemplo, por cierre de vía), <strong>cuando</strong> el conductor registró previamente un desvío planificado, <strong>entonces</strong> el sistema no genera alerta por esa desviación específica.</li>
        </ul>
    </td>
    <td style="text-align:center">EP04</td>
</tr>
<!-- USER STORY 09 - Personal trip history (Driver) -->
<tr>
    <td class="user-story-id" style="text-align:center">US09</td>
    <td style="text-align:center">Visualizar historial personal de viajes</td>
    <td>Como <strong>conductor independiente</strong>, quiero acceder a mi historial de viajes, puntualidad e incidencias registradas, para evaluar mi desempeño y demostrar mi confiabilidad a los padres.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor accede a su perfil en la aplicación, <strong>cuando</strong> selecciona "Mi historial", <strong>entonces</strong> el sistema muestra una lista de viajes realizados en los últimos 30 días con fecha, hora de inicio y fin.</li>
            <li><strong>Dado que</strong> el conductor consulta un día específico, <strong>cuando</strong> selecciona una fecha, <strong>entonces</strong> el sistema muestra los detalles de la ruta: paradas, tiempos reales vs. programados e incidencias registradas.</li>
            <li><strong>Dado que</strong> el conductor quiere compartir su historial con un padre, <strong>cuando</strong> solicita exportar su reporte, <strong>entonces</strong> el sistema genera un PDF resumido con sus métricas de puntualidad y número de incidencias.</li>
        </ul>
    </td>
    <td style="text-align:center">EP05A</td>
</tr>
<!-- USER STORY 10 - Export monthly attendance report (Company) -->
<tr>
    <td class="user-story-id" style="text-align:center">US10</td>
    <td style="text-align:center">Exportar reporte de asistencia mensual</td>
    <td>Como <strong>administrador de una empresa de movilidad escolar</strong>, quiero exportar un reporte consolidado de asistencia mensual por estudiante, para agilizar el proceso de facturación a los padres sin errores manuales.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el administrador necesita facturar por estudiante, <strong>cuando</strong> selecciona un mes y una ruta, <strong>entonces</strong> el sistema genera un archivo Excel con la lista de estudiantes y los días del mes en que realmente usaron el servicio.</li>
            <li><strong>Dado que</strong> el reporte ha sido generado, <strong>cuando</strong> el administrador lo descarga, <strong>entonces</strong> el archivo contiene las columnas: nombre del estudiante, grado, dirección de recojo, total de días atendidos, ausencias justificadas e injustificadas.</li>
            <li><strong>Dado que</strong> un estudiante tuvo ausencias registradas por el conductor, <strong>cuando</strong> se genera el reporte, <strong>entonces</strong> esas ausencias aparecen marcadas con el tipo (justificada o injustificada) según lo reportado por el padre.</li>
        </ul>
    </td>
    <td style="text-align:center">EP05B</td>
</tr>
<!-- USER STORY 11 - Generate punctuality report per unit -->
<tr>
    <td class="user-story-id" style="text-align:center">US11</td>
    <td style="text-align:center">Generar reporte de puntualidad por unidad</td>
    <td>Como <strong>administrador de una empresa de movilidad escolar</strong>, quiero generar un reporte de puntualidad por conductor/unidad, para evaluar su desempeño y tomar decisiones de mejora o incentivos.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el administrador selecciona un rango de fechas, <strong>cuando</strong> solicita el reporte de puntualidad, <strong>entonces</strong> el sistema genera una tabla con cada unidad, su porcentaje de llegadas a tiempo por parada y el retraso promedio en minutos.</li>
            <li><strong>Dado que</strong> el reporte ha sido generado, <strong>cuando</strong> el administrador selecciona una unidad específica, <strong>entonces</strong> el sistema muestra el detalle día a día con los tiempos programados vs. reales.</li>
            <li><strong>Dado que</strong> el administrador necesita presentar el reporte a un colegio, <strong>cuando</strong> solicita exportar en PDF, <strong>entonces</strong> el sistema genera un documento profesional con gráficos de puntualidad semanal.</li>
        </ul>
    </td>
    <td style="text-align:center">EP05B</td>
</tr>
<!-- USER STORY 12 - View student list by route -->
<tr>
    <td class="user-story-id" style="text-align:center">US12</td>
    <td style="text-align:center">Visualizar lista de estudiantes por ruta</td>
    <td>Como <strong>conductor</strong>, quiero ver la lista de estudiantes asignados a mi ruta, para saber a quiénes debo recoger.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor ha iniciado sesión en la aplicación, <strong>cuando</strong> accede a la sección de la ruta del día, <strong>entonces</strong> el sistema presenta la lista de estudiantes ordenada por secuencia de paradas.</li>
            <li><strong>Dado que</strong> la lista de estudiantes es visible, <strong>cuando</strong> el conductor consulta un estudiante específico, <strong>entonces</strong> el sistema muestra su nombre completo y dirección de recojo.</li>
            <li><strong>Dado que</strong> hay estudiantes asignados a diferentes rutas, <strong>cuando</strong> el conductor visualiza su lista, <strong>entonces</strong> el sistema filtra y muestra solo los estudiantes asignados a la ruta activa del conductor.</li>
        </ul>
    </td>
    <td style="text-align:center">EP01</td>
</tr>
<!-- USER STORY 13 - View students by stop -->
<tr>
    <td class="user-story-id" style="text-align:center">US13</td>
    <td style="text-align:center">Visualizar estudiantes por parada</td>
    <td>Como <strong>conductor</strong>, quiero ver qué estudiantes corresponden a cada parada, para organizar el recojo.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor ha seleccionado una ruta activa, <strong>cuando</strong> accede a la lista de paradas, <strong>entonces</strong> el sistema agrupa a los estudiantes por cada parada programada.</li>
            <li><strong>Dado que</strong> el conductor se encuentra en una parada específica, <strong>cuando</strong> consulta la lista, <strong>entonces</strong> el sistema identifica la parada actual con un indicador visual distintivo.</li>
            <li><strong>Dado que</strong> el conductor necesita revisar otras paradas, <strong>cuando</strong> navega entre ellas, <strong>entonces</strong> el sistema permite cambiar de una parada a otra sin perder el contexto de la ruta.</li>
        </ul>
    </td>
    <td style="text-align:center">EP01</td>
</tr>
<!-- USER STORY 14 - Record boarding -->
<tr>
    <td class="user-story-id" style="text-align:center">US14</td>
    <td style="text-align:center">Registrar abordaje</td>
    <td>Como <strong>conductor</strong>, quiero marcar rápidamente cuándo un estudiante sube al vehículo, para llevar el control del viaje.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor está en una parada y el estudiante aborda el vehículo, <strong>cuando</strong> el conductor realiza la acción de registro, <strong>entonces</strong> el sistema cambia el estado del estudiante a "abordado" en la lista.</li>
            <li><strong>Dado que</strong> el abordaje ha sido registrado, <strong>cuando</strong> el conductor continúa con la ruta, <strong>entonces</strong> el sistema guarda automáticamente el evento con fecha, hora y ubicación.</li>
            <li><strong>Dado que</strong> el registro es exitoso, <strong>cuando</strong> el conductor consulta la lista actualizada, <strong>entonces</strong> el estudiante aparece como ya abordado y no se requiere ninguna acción adicional.</li>
        </ul>
    </td>
    <td style="text-align:center">EP01</td>
</tr>
<!-- USER STORY 15 - Record absence -->
<tr>
    <td class="user-story-id" style="text-align:center">US15</td>
    <td style="text-align:center">Registrar ausencia</td>
    <td>Como <strong>conductor</strong>, quiero marcar cuándo un estudiante no sube al vehículo, para evitar esperas innecesarias.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor ha llegado a una parada programada y el estudiante no se presenta, <strong>cuando</strong> el conductor selecciona la opción de ausencia, <strong>entonces</strong> el sistema registra al estudiante como "ausente" en esa parada.</li>
            <li><strong>Dado que</strong> el conductor registra una ausencia, <strong>cuando</strong> el sistema lo solicita, <strong>entonces</strong> el conductor puede registrar opcionalmente el motivo de la ausencia.</li>
            <li><strong>Dado que</strong> se registra una ausencia, <strong>cuando</strong> el evento es persistido, <strong>entonces</strong> la información se actualiza en tiempo real en el sistema y queda disponible para el administrador o los padres.</li>
        </ul>
    </td>
    <td style="text-align:center">EP01</td>
</tr>
<!-- USER STORY 16 - Quick status editing -->
<tr>
    <td class="user-story-id" style="text-align:center">US16</td>
    <td style="text-align:center">Edición rápida de estado</td>
    <td>Como <strong>conductor</strong>, quiero corregir el estado de un estudiante en caso de error, para mantener la información precisa.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> un estudiante tiene un estado registrado erróneamente (abordaje o ausencia), <strong>cuando</strong> el conductor selecciona la opción de edición, <strong>entonces</strong> el sistema permite cambiar el estado al valor correcto.</li>
            <li><strong>Dado que</strong> se realiza una corrección de estado, <strong>cuando</strong> se guarda el cambio, <strong>entonces</strong> el sistema registra la última actualización con una nueva marca de tiempo y mantiene la trazabilidad del cambio.</li>
            <li><strong>Dado que</strong> el conductor necesita corregir un estado, <strong>cuando</strong> accede a la edición, <strong>entonces</strong> el sistema permite completar la corrección sin requerir múltiples pasos ni pantallas adicionales.</li>
        </ul>
    </td>
    <td style="text-align:center">EP01</td>
</tr>
<!-- USER STORY 17 - Offline functionality -->
<tr>
    <td class="user-story-id" style="text-align:center">US17</td>
    <td style="text-align:center">Funcionalidad sin conexión</td>
    <td>Como <strong>conductor</strong>, quiero poder registrar abordajes sin conexión a internet, para no depender de la señal.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el dispositivo del conductor no tiene conexión a internet, <strong>cuando</strong> el conductor registra un abordaje o una ausencia, <strong>entonces</strong> el sistema almacena el evento localmente en el dispositivo.</li>
            <li><strong>Dado que</strong> existen eventos pendientes de sincronizar, <strong>cuando</strong> el dispositivo recupera la conexión a internet, <strong>entonces</strong> el sistema envía automáticamente todos los eventos almacenados al servidor.</li>
            <li><strong>Dado que</strong> la sincronización se completa, <strong>cuando</strong> el sistema verifica los eventos transmitidos, <strong>entonces</strong> ninguna información registrada durante el modo sin conexión se pierde ni se duplica.</li>
        </ul>
    </td>
    <td style="text-align:center">EP01</td>
</tr>
<!-- USER STORY 18 - Quick visual confirmation -->
<tr>
    <td class="user-story-id" style="text-align:center">US18</td>
    <td style="text-align:center">Confirmación visual rápida</td>
    <td>Como <strong>conductor</strong>, quiero identificar rápidamente quién ya subió y quién no, para tomar decisiones rápidas.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor visualiza la lista de estudiantes en una parada, <strong>cuando</strong> un estudiante tiene el estado "abordado", <strong>entonces</strong> el sistema lo diferencia visualmente de aquellos con estado pendiente.</li>
            <li><strong>Dado que</strong> el conductor está en movimiento, <strong>cuando</strong> consulta la lista de estudiantes, <strong>entonces</strong> el sistema presenta la información de forma legible sin requerir interacciones complejas.</li>
            <li><strong>Dado que</strong> el conductor necesita conocer el estado general de la parada, <strong>cuando</strong> revisa la lista, <strong>entonces</strong> el sistema le permite ver de un vistazo cuántos estudiantes han abordado y cuántos faltan.</li>
        </ul>
    </td>
    <td style="text-align:center">EP01</td>
</tr>
<!-- USER STORY 19 - View assigned route -->
<tr>
    <td class="user-story-id" style="text-align:center">US19</td>
    <td style="text-align:center">Visualizar ruta asignada</td>
    <td>Como <strong>conductor</strong>, quiero visualizar la ruta asignada del día, para conocer el orden del recorrido.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor ha iniciado su turno laboral, <strong>cuando</strong> accede a la sección de ruta, <strong>entonces</strong> el sistema presenta la ruta asignada para el día actual.</li>
            <li><strong>Dado que</strong> la ruta del día es visible, <strong>cuando</strong> el conductor la consulta, <strong>entonces</strong> el sistema muestra la lista completa de paradas en el orden secuencial del recorrido.</li>
            <li><strong>Dado que</strong> hay múltiples conductores en una misma empresa, <strong>cuando</strong> un conductor consulta su ruta, <strong>entonces</strong> el sistema muestra únicamente la ruta asignada a ese conductor específico.</li>
        </ul>
    </td>
    <td style="text-align:center">EP02</td>
</tr>
<!-- USER STORY 20 - View stops on map -->
<tr>
    <td class="user-story-id" style="text-align:center">US20</td>
    <td style="text-align:center">Visualizar paradas en el mapa</td>
    <td>Como <strong>conductor</strong>, quiero ver las paradas de mi ruta en un mapa, para ubicarme fácilmente durante el recorrido.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor ha seleccionado su ruta activa, <strong>cuando</strong> accede a la vista del mapa, <strong>entonces</strong> el sistema muestra todas las paradas de la ruta como puntos geolocalizados.</li>
            <li><strong>Dado que</strong> el mapa es visible, <strong>cuando</strong> el conductor se desplaza durante el recorrido, <strong>entonces</strong> el sistema muestra la ubicación actual del vehículo en el mapa.</li>
            <li><strong>Dado que</strong> las paradas están representadas en el mapa, <strong>cuando</strong> el conductor las visualiza, <strong>entonces</strong> cada parada se diferencia claramente (por ejemplo, paradas completadas vs. pendientes).</li>
        </ul>
    </td>
    <td style="text-align:center">EP02</td>
</tr>
<!-- USER STORY 21 - Navigation between stops -->
<tr>
    <td class="user-story-id" style="text-align:center">US21</td>
    <td style="text-align:center">Navegación entre paradas</td>
    <td>Como <strong>conductor</strong>, quiero recibir indicaciones para llegar a cada parada, para optimizar mi recorrido.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor ha completado una parada, <strong>cuando</strong> el sistema detecta la finalización, <strong>entonces</strong> selecciona automáticamente la siguiente parada como próximo destino.</li>
            <li><strong>Dado que</strong> la siguiente parada está seleccionada, <strong>cuando</strong> el conductor necesita orientación, <strong>entonces</strong> el sistema proporciona indicaciones de navegación para llegar a esa parada.</li>
            <li><strong>Dado que</strong> el conductor necesita cambiar el orden de navegación, <strong>cuando</strong> selecciona manualmente otra parada, <strong>entonces</strong> el sistema actualiza las indicaciones hacia la parada recién seleccionada.</li>
        </ul>
    </td>
    <td style="text-align:center">EP02</td>
</tr>
<!-- USER STORY 22 - Mark stop as completed -->
<tr>
    <td class="user-story-id" style="text-align:center">US22</td>
    <td style="text-align:center">Marcar parada como completada</td>
    <td>Como <strong>conductor</strong>, quiero marcar una parada como completada, para avanzar en mi ruta de manera ordenada.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor ha completado las acciones en una parada (abordajes y ausencias), <strong>cuando</strong> el conductor realiza la acción de finalizar la parada, <strong>entonces</strong> el sistema cambia el estado de la parada a "completada".</li>
            <li><strong>Dado que</strong> una parada ha sido marcada como completada, <strong>cuando</strong> el conductor visualiza la lista de paradas, <strong>entonces</strong> la parada completada se diferencia visualmente de las paradas pendientes.</li>
            <li><strong>Dado que</strong> la parada actual se marca como completada, <strong>cuando</strong> el sistema registra el evento, <strong>entonces</strong> avanza automáticamente a la siguiente parada de la ruta.</li>
        </ul>
    </td>
    <td style="text-align:center">EP02</td>
</tr>
<!-- USER STORY 23 - Basic route reordering -->
<tr>
    <td class="user-story-id" style="text-align:center">US23</td>
    <td style="text-align:center">Reordenamiento básico de ruta</td>
    <td>Como <strong>conductor</strong>, quiero ajustar el orden de las paradas en caso de imprevistos, para adaptarme a cambios en el recorrido.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> ocurre un imprevisto que requiere un cambio en el orden de las paradas, <strong>cuando</strong> el conductor modifica la secuencia de paradas, <strong>entonces</strong> el sistema permite reordenar la lista según la nueva prioridad.</li>
            <li><strong>Dado que</strong> el conductor ha reordenado las paradas, <strong>cuando</strong> confirma los cambios, <strong>entonces</strong> el sistema actualiza la ruta activa en tiempo real con el nuevo orden.</li>
            <li><strong>Dado que</strong> la ruta ha sido reordenada, <strong>cuando</strong> el conductor consulta los registros de estudiantes, <strong>entonces</strong> los datos de abordaje y ausencia permanecen correctamente asociados a cada estudiante.</li>
        </ul>
    </td>
    <td style="text-align:center">EP02</td>
</tr>
<!-- USER STORY 24 - View route status -->
<tr>
    <td class="user-story-id" style="text-align:center">US24</td>
    <td style="text-align:center">Visualizar estado de la ruta</td>
    <td>Como <strong>conductor</strong>, quiero ver el progreso de mi ruta, para saber cuánto falta por completar.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor tiene una ruta activa, <strong>cuando</strong> accede a la vista de progreso, <strong>entonces</strong> el sistema muestra el número o porcentaje de paradas completadas sobre el total.</li>
            <li><strong>Dado que</strong> el conductor visualiza el estado de la ruta, <strong>cuando</strong> consulta la lista de paradas, <strong>entonces</strong> el sistema diferencia claramente entre paradas completadas y paradas pendientes.</li>
            <li><strong>Dado que</strong> el conductor avanza en su recorrido, <strong>cuando</strong> completa una nueva parada, <strong>entonces</strong> el sistema actualiza el estado de progreso en tiempo real.</li>
        </ul>
    </td>
    <td style="text-align:center">EP02</td>
</tr>
<!-- USER STORY 25 - Offline route functionality -->
<tr>
    <td class="user-story-id" style="text-align:center">US25</td>
    <td style="text-align:center">Funcionalidad de ruta sin conexión</td>
    <td>Como <strong>conductor</strong>, quiero acceder a mi ruta sin conexión a internet, para no depender de la señal.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor tiene conexión a internet al inicio del turno, <strong>cuando</strong> el sistema descarga la ruta asignada, <strong>entonces</strong> los datos de la ruta se almacenan localmente en el dispositivo.</li>
            <li><strong>Dado que</strong> la ruta está almacenada localmente, <strong>cuando</strong> el dispositivo no tiene conexión a internet, <strong>entonces</strong> el conductor puede visualizar la ruta y sus paradas sin interrupciones.</li>
            <li><strong>Dado que</strong> el conductor realiza cambios en la ruta (reordenamiento, estados) sin conexión, <strong>cuando</strong> el dispositivo recupera la conexión, <strong>entonces</strong> el sistema sincroniza automáticamente todos los cambios pendientes con el servidor.</li>
        </ul>
    </td>
    <td style="text-align:center">EP02</td>
</tr>
<!-- USER STORY 26 - Quick incident logging -->
<tr>
    <td class="user-story-id" style="text-align:center">US26</td>
    <td style="text-align:center">Registro rápido de incidencia</td>
    <td>Como <strong>conductor</strong>, quiero registrar una incidencia en pocos pasos, para no distraerme durante el recorrido.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> ocurre un evento imprevisto durante el recorrido, <strong>cuando</strong> el conductor necesita reportarlo, <strong>entonces</strong> el sistema permite iniciar el registro de la incidencia con una acción accesible.</li>
            <li><strong>Dado que</strong> el conductor ha iniciado el registro de una incidencia, <strong>cuando</strong> selecciona el tipo de evento, <strong>entonces</strong> el sistema permite completar la selección en un máximo de dos interacciones.</li>
            <li><strong>Dado que</strong> el conductor necesita registrar la incidencia, <strong>cuando</strong> completa el registro, <strong>entonces</strong> el sistema no requiere que el conductor escriba texto para guardar el evento.</li>
        </ul>
    </td>
    <td style="text-align:center">EP03</td>
</tr>
<!-- USER STORY 28 - Select incident type -->
<tr>
    <td class="user-story-id" style="text-align:center">US28</td>
    <td style="text-align:center">Seleccionar tipo de incidencia</td>
    <td>Como <strong>conductor</strong>, quiero elegir el tipo de incidencia, para clasificar correctamente el evento.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor está registrando una incidencia, <strong>cuando</strong> accede a la selección de tipo, <strong>entonces</strong> el sistema presenta una lista predefinida de tipos de incidencia disponibles.</li>
            <li><strong>Dado que</strong> la lista de tipos de incidencia es visible, <strong>cuando</strong> el conductor la revisa, <strong>entonces</strong> cada opción está redactada de forma clara y comprensible para su contexto.</li>
            <li><strong>Dado que</strong> el conductor necesita clasificar la incidencia, <strong>cuando</strong> selecciona un tipo, <strong>entonces</strong> el sistema permite elegir solo una opción principal por evento.</li>
        </ul>
    </td>
    <td style="text-align:center">EP03</td>
</tr>
<!-- USER STORY 29 - Record optional detail -->
<tr>
    <td class="user-story-id" style="text-align:center">US29</td>
    <td style="text-align:center">Registrar detalle opcional</td>
    <td>Como <strong>conductor</strong>, quiero agregar un comentario opcional, para proporcionar más contexto si es necesario.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor está registrando una incidencia, <strong>cuando</strong> desea agregar información adicional, <strong>entonces</strong> el sistema cuenta con un campo para ingresar texto de forma opcional.</li>
            <li><strong>Dado que</strong> el conductor no tiene información adicional que agregar, <strong>cuando</strong> omite el campo de comentario, <strong>entonces</strong> el sistema permite completar el registro sin bloquear la acción.</li>
            <li><strong>Dado que</strong> el conductor ingresa un comentario, <strong>cuando</strong> la incidencia es guardada, <strong>entonces</strong> el sistema almacena el comentario junto con el resto de los datos del evento.</li>
        </ul>
    </td>
    <td style="text-align:center">EP03</td>
</tr>
<!-- USER STORY 30 - Associate incident with stop or student -->
<tr>
    <td class="user-story-id" style="text-align:center">US30</td>
    <td style="text-align:center">Asociar incidencia con parada o estudiante</td>
    <td>Como <strong>conductor</strong>, quiero vincular la incidencia a una parada o estudiante, para mayor precisión en el registro.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor está registrando una incidencia, <strong>cuando</strong> la incidencia está relacionada con un punto específico del recorrido, <strong>entonces</strong> el sistema permite seleccionar la parada o el estudiante asociado.</li>
            <li><strong>Dado que</strong> el conductor vincula la incidencia a una parada o estudiante, <strong>cuando</strong> confirma el registro, <strong>entonces</strong> el sistema guarda la asociación como parte del evento.</li>
            <li><strong>Dado que</strong> la incidencia no está relacionada con una parada o estudiante específico, <strong>cuando</strong> el conductor completa el registro, <strong>entonces</strong> el sistema permite guardar la incidencia sin necesidad de realizar una asociación.</li>
        </ul>
    </td>
    <td style="text-align:center">EP03</td>
</tr>
<!-- USER STORY 31 - Automatic time and location logging -->
<tr>
    <td class="user-story-id" style="text-align:center">US31</td>
    <td style="text-align:center">Registro automático de hora y ubicación</td>
    <td>Como <strong>conductor</strong>, quiero que el sistema registre automáticamente la hora y la ubicación, para no tener que hacerlo manualmente.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor registra una incidencia, <strong>cuando</strong> el evento es creado, <strong>entonces</strong> el sistema guarda automáticamente una marca de tiempo con la fecha y hora del registro.</li>
            <li><strong>Dado que</strong> el conductor registra una incidencia, <strong>cuando</strong> el dispositivo tiene GPS disponible, <strong>entonces</strong> el sistema captura y almacena automáticamente la ubicación geográfica del evento.</li>
            <li><strong>Dado que</strong> el sistema registra hora y ubicación, <strong>cuando</strong> el registro se completa, <strong>entonces</strong> no se requiere ninguna acción adicional del conductor para capturar estos datos.</li>
        </ul>
    </td>
    <td style="text-align:center">EP03</td>
</tr>
<!-- USER STORY 32 - View incident history -->
<tr>
    <td class="user-story-id" style="text-align:center">US32</td>
    <td style="text-align:center">Visualizar historial de incidencias</td>
    <td>Como <strong>conductor</strong>, quiero ver las incidencias registradas, para hacer seguimiento del recorrido.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor necesita revisar los eventos del día, <strong>cuando</strong> accede al historial de incidencias, <strong>entonces</strong> el sistema presenta una lista de todas las incidencias registradas durante el turno actual.</li>
            <li><strong>Dado que</strong> la lista de incidencias es visible, <strong>cuando</strong> el conductor consulta un evento, <strong>entonces</strong> el sistema muestra el tipo de incidencia, la hora de registro y el estado actual.</li>
            <li><strong>Dado que</strong> se han registrado múltiples incidencias, <strong>cuando</strong> el conductor visualiza la lista, <strong>entonces</strong> el sistema las presenta en orden cronológico (de la más reciente a la más antigua o viceversa).</li>
        </ul>
    </td>
    <td style="text-align:center">EP03</td>
</tr>
<!-- USER STORY 33 - Edit or correct incident -->
<tr>
    <td class="user-story-id" style="text-align:center">US33</td>
    <td style="text-align:center">Editar o corregir incidencia</td>
    <td>Como <strong>conductor</strong>, quiero corregir una incidencia en caso de error, para mantener la información precisa.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor identifica un error en una incidencia previamente registrada, <strong>cuando</strong> accede a la opción de edición, <strong>entonces</strong> el sistema permite modificar el tipo de incidencia y/o el comentario asociado.</li>
            <li><strong>Dado que</strong> el conductor ha realizado cambios en una incidencia, <strong>cuando</strong> confirma la edición, <strong>entonces</strong> el sistema guarda correctamente los nuevos valores.</li>
            <li><strong>Dado que</strong> una incidencia es editada, <strong>cuando</strong> el conductor consulta el historial, <strong>entonces</strong> el sistema muestra la información actualizada con el registro de la última modificación.</li>
        </ul>
    </td>
    <td style="text-align:center">EP03</td>
</tr>
<!-- USER STORY 34 - Offline incident functionality -->
<tr>
    <td class="user-story-id" style="text-align:center">US34</td>
    <td style="text-align:center">Funcionalidad de incidencias sin conexión</td>
    <td>Como <strong>conductor</strong>, quiero registrar incidencias sin conexión, para no depender de la red.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el dispositivo del conductor no tiene conexión a internet, <strong>cuando</strong> el conductor registra una incidencia, <strong>entonces</strong> el sistema almacena la incidencia localmente en el dispositivo.</li>
            <li><strong>Dado que</strong> existen incidencias pendientes de sincronizar, <strong>cuando</strong> el dispositivo recupera la conexión a internet, <strong>entonces</strong> el sistema envía automáticamente todas las incidencias almacenadas al servidor.</li>
            <li><strong>Dado que</strong> la sincronización se completa, <strong>cuando</strong> el sistema verifica los datos transmitidos, <strong>entonces</strong> ninguna incidencia registrada durante el modo sin conexión se pierde.</li>
        </ul>
    </td>
    <td style="text-align:center">EP03</td>
</tr>
<!-- USER STORY 35 - View vehicles on map -->
<tr>
    <td class="user-story-id" style="text-align:center">US35</td>
    <td style="text-align:center">Visualizar vehículos en el mapa</td>
    <td>Como <strong>administrador de una empresa de movilidad escolar</strong>, quiero ver todos mis vehículos en un mapa en tiempo real, para monitorear su ubicación.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el administrador accede al panel de monitoreo, <strong>cuando</strong> selecciona la vista del mapa, <strong>entonces</strong> el sistema muestra todos los vehículos activos de la empresa geolocalizados en el mapa.</li>
            <li><strong>Dado que</strong> los vehículos están representados en el mapa, <strong>cuando</strong> el administrador los visualiza, <strong>entonces</strong> cada vehículo cuenta con un identificador visible (número o nombre del conductor).</li>
            <li><strong>Dado que</strong> los vehículos se desplazan durante el turno, <strong>cuando</strong> su ubicación cambia, <strong>entonces</strong> el sistema actualiza automáticamente las posiciones en el mapa.</li>
        </ul>
    </td>
    <td style="text-align:center">EP04</td>
</tr>
<!-- USER STORY 36 - View vehicle details -->
<tr>
    <td class="user-story-id" style="text-align:center">US36</td>
    <td style="text-align:center">Visualizar detalles del vehículo</td>
    <td>Como <strong>administrador de una empresa de movilidad escolar</strong>, quiero seleccionar un vehículo y ver su información, para conocer su estado actual.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el administrador visualiza el mapa con los vehículos activos, <strong>cuando</strong> selecciona un vehículo específico, <strong>entonces</strong> el sistema despliega un panel con información detallada de ese vehículo.</li>
            <li><strong>Dado que</strong> el panel de detalle es visible, <strong>cuando</strong> el administrador consulta la información, <strong>entonces</strong> el sistema muestra los datos del conductor, la ruta asignada y el estado actual del vehículo.</li>
            <li><strong>Dado que</strong> la información del vehículo ha cambiado, <strong>cuando</strong> el administrador consulta los detalles, <strong>entonces</strong> los datos presentados se encuentran actualizados al momento de la consulta.</li>
        </ul>
    </td>
    <td style="text-align:center">EP04</td>
</tr>
<!-- USER STORY 37 - View vehicle statuses -->
<tr>
    <td class="user-story-id" style="text-align:center">US37</td>
    <td style="text-align:center">Visualizar estados de los vehículos</td>
    <td>Como <strong>administrador de una empresa de movilidad escolar</strong>, quiero identificar el estado de cada vehículo, para detectar problemas rápidamente.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el administrador visualiza el mapa o la lista de vehículos, <strong>cuando</strong> consulta su estado, <strong>entonces</strong> el sistema muestra el estado actual de cada vehículo (en ruta, detenido, retrasado).</li>
            <li><strong>Dado que</strong> los estados están representados, <strong>cuando</strong> el administrador los revisa, <strong>entonces</strong> cada estado se diferencia visualmente de los demás (por ejemplo, marca visual distintiva según el tipo de estado).</li>
            <li><strong>Dado que</strong> el estado de un vehículo cambia durante el turno, <strong>cuando</strong> ocurre el cambio, <strong>entonces</strong> el sistema actualiza la información en tiempo real en el panel del administrador.</li>
        </ul>
    </td>
    <td style="text-align:center">EP04</td>
</tr>
<!-- USER STORY 38 - Filter units -->
<tr>
    <td class="user-story-id" style="text-align:center">US38</td>
    <td style="text-align:center">Filtrar unidades</td>
    <td>Como <strong>administrador de una empresa de movilidad escolar</strong>, quiero filtrar vehículos por estado o ruta, para enfocarme en lo relevante.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el administrador visualiza la lista de vehículos o el mapa, <strong>cuando</strong> aplica un filtro por estado, <strong>entonces</strong> el sistema muestra solo los vehículos que coinciden con el estado seleccionado.</li>
            <li><strong>Dado que</strong> el administrador necesita filtrar por ruta, <strong>cuando</strong> selecciona una ruta específica, <strong>entonces</strong> el sistema muestra solo los vehículos asignados a esa ruta.</li>
            <li><strong>Dado que</strong> el administrador aplica uno o más filtros, <strong>cuando</strong> confirma la selección, <strong>entonces</strong> la vista se actualiza automáticamente mostrando solo los vehículos que cumplen los criterios.</li>
        </ul>
    </td>
    <td style="text-align:center">EP04</td>
</tr>
<!-- USER STORY 39 - Deviation alerts -->
<tr>
    <td class="user-story-id" style="text-align:center">US39</td>
    <td style="text-align:center">Alertas de desviación</td>
    <td>Como <strong>administrador de una empresa de movilidad escolar</strong>, quiero recibir alertas cuando un vehículo se desvía de su ruta, para actuar oportunamente.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> un vehículo activo tiene una ruta programada definida, <strong>cuando</strong> su ubicación se desvía significativamente de la ruta planificada, <strong>entonces</strong> el sistema detecta automáticamente la desviación.</li>
            <li><strong>Dado que</strong> se detecta una desviación, <strong>cuando</strong> ocurre el evento, <strong>entonces</strong> el sistema genera una alerta o notificación visible para el administrador.</li>
            <li><strong>Dado que</strong> se genera una alerta de desviación, <strong>cuando</strong> el administrador la recibe, <strong>entonces</strong> la alerta indica claramente qué vehículo presenta el problema.</li>
        </ul>
    </td>
    <td style="text-align:center">EP04</td>
</tr>
<!-- USER STORY 40 - View real-time journey -->
<tr>
    <td class="user-story-id" style="text-align:center">US40</td>
    <td style="text-align:center">Visualizar recorrido en tiempo real</td>
    <td>Como <strong>administrador de una empresa de movilidad escolar</strong>, quiero ver el recorrido que realiza cada vehículo, para validar el cumplimiento de la ruta.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el administrador selecciona un vehículo activo, <strong>cuando</strong> accede a la vista de recorrido, <strong>entonces</strong> el sistema muestra la trayectoria que ha seguido el vehículo en el mapa.</li>
            <li><strong>Dado que</strong> la trayectoria es visible, <strong>cuando</strong> el vehículo avanza durante su recorrido, <strong>entonces</strong> el sistema actualiza la trayectoria en el mapa conforme progresa.</li>
            <li><strong>Dado que</strong> el administrador consulta el recorrido de un vehículo, <strong>cuando</strong> lo visualiza, <strong>entonces</strong> el sistema permite identificar qué parte de la ruta ya fue completada y qué falta.</li>
        </ul>
    </td>
    <td style="text-align:center">EP04</td>
</tr>
<!-- USER STORY 41 - Recent location history -->
<tr>
    <td class="user-story-id" style="text-align:center">US41</td>
    <td style="text-align:center">Historial reciente de ubicaciones</td>
    <td>Como <strong>administrador de una empresa de movilidad escolar</strong>, quiero consultar las ubicaciones recientes de un vehículo, para analizar su comportamiento.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el administrador selecciona un vehículo específico, <strong>cuando</strong> accede a la sección de historial, <strong>entonces</strong> el sistema muestra las ubicaciones recientes registradas de ese vehículo.</li>
            <li><strong>Dado que</strong> el historial de ubicaciones es visible, <strong>cuando</strong> el administrador lo consulta, <strong>entonces</strong> las ubicaciones se presentan en orden cronológico.</li>
            <li><strong>Dado que</strong> el administrador necesita revisar el historial de un vehículo, <strong>cuando</strong> se encuentra en la página de detalles del vehículo, <strong>entonces</strong> el sistema permite acceder al historial desde esa misma vista.</li>
        </ul>
    </td>
    <td style="text-align:center">EP04</td>
</tr>
<!-- USER STORY 42 - Automatic data refresh -->
<tr>
    <td class="user-story-id" style="text-align:center">US42</td>
    <td style="text-align:center">Actualización automática de datos</td>
    <td>Como <strong>administrador de una empresa de movilidad escolar</strong>, quiero que la información se actualice automáticamente, para no tener que recargarla manualmente.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el administrador está visualizando el panel de monitoreo, <strong>cuando</strong> transcurre un intervalo de tiempo definido, <strong>entonces</strong> el sistema actualiza automáticamente los datos mostrados.</li>
            <li><strong>Dado que</strong> los datos se actualizan automáticamente, <strong>cuando</strong> ocurre la actualización, <strong>entonces</strong> el administrador no necesita realizar ninguna acción manual para recargar la información.</li>
            <li><strong>Dado que</strong> se ha realizado una actualización automática, <strong>cuando</strong> el administrador consulta la información, <strong>entonces</strong> el sistema indica la hora de la última actualización realizada.</li>
            <li><strong>Dado que</strong> los datos se actualizan en segundo plano, <strong>cuando</strong> ocurre la actualización, <strong>entonces</strong> la navegación o interacción del administrador no se interrumpe.</li>
        </ul>
    </td>
    <td style="text-align:center">EP04</td>
</tr>
<!-- USER STORY 43 - Generate journey report -->
<tr>
    <td class="user-story-id" style="text-align:center">US43</td>
    <td style="text-align:center">Generar reporte de recorridos</td>
    <td>Como <strong>administrador de una empresa de movilidad escolar</strong>, quiero generar reportes de recorridos realizados, para analizar el cumplimiento de rutas.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el administrador necesita un reporte de recorridos, <strong>cuando</strong> selecciona un rango de fechas, <strong>entonces</strong> el sistema genera un reporte con los recorridos completados en ese período.</li>
            <li><strong>Dado que</strong> el reporte ha sido generado, <strong>cuando</strong> el administrador lo consulta, <strong>entonces</strong> el reporte incluye las rutas tomadas por cada vehículo.</li>
            <li><strong>Dado que</strong> el reporte está disponible, <strong>cuando</strong> el administrador lo visualiza, <strong>entonces</strong> la información se presenta en pantalla de forma legible.</li>
        </ul>
    </td>
    <td style="text-align:center">EP05B</td>
</tr>
<!-- USER STORY 44 - Generate performance report -->
<tr>
    <td class="user-story-id" style="text-align:center">US44</td>
    <td style="text-align:center">Generar reporte de desempeño</td>
    <td>Como <strong>administrador de una empresa de movilidad escolar</strong>, quiero visualizar métricas de desempeño de conductores y vehículos, para evaluar la eficiencia operativa.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el administrador solicita un reporte de desempeño, <strong>cuando</strong> el reporte es generado, <strong>entonces</strong> el sistema muestra métricas clave como tiempos de viaje y paradas completadas.</li>
            <li><strong>Dado que</strong> el reporte de desempeño es visible, <strong>cuando</strong> el administrador lo consulta, <strong>entonces</strong> la información se presenta agrupada por conductor o por vehículo.</li>
            <li><strong>Dado que</strong> el reporte contiene métricas, <strong>cuando</strong> el administrador las revisa, <strong>entonces</strong> los datos son claros, comprensibles y permiten evaluar la eficiencia operativa.</li>
        </ul>
    </td>
    <td style="text-align:center">EP05B</td>
</tr>
<!-- USER STORY 45 - Export reports -->
<tr>
    <td class="user-story-id" style="text-align:center">US45</td>
    <td style="text-align:center">Exportar reportes</td>
    <td>Como <strong>administrador de una empresa de movilidad escolar</strong>, quiero exportar reportes, para compartirlos o analizarlos externamente.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el administrador ha generado un reporte, <strong>cuando</strong> selecciona la opción de exportar, <strong>entonces</strong> el sistema permite exportar el reporte en formato PDF o Excel.</li>
            <li><strong>Dado que</strong> la exportación es iniciada, <strong>cuando</strong> el proceso finaliza, <strong>entonces</strong> el archivo se descarga rápidamente en el dispositivo del administrador.</li>
            <li><strong>Dado que</strong> el administrador exporta un reporte, <strong>cuando</strong> abre el archivo descargado, <strong>entonces</strong> el contenido incluye toda la información seleccionada durante la generación del reporte.</li>
        </ul>
    </td>
    <td style="text-align:center">EP05B</td>
</tr>
<!-- USER STORY 46 - Filter reports -->
<tr>
    <td class="user-story-id" style="text-align:center">US46</td>
    <td style="text-align:center">Filtrar reportes</td>
    <td>Como <strong>administrador de una empresa de movilidad escolar</strong>, quiero aplicar filtros a los reportes, para enfocarme en información específica.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el administrador está generando un reporte, <strong>cuando</strong> aplica un filtro por rango de fechas, <strong>entonces</strong> el sistema muestra solo la información correspondiente a ese período.</li>
            <li><strong>Dado que</strong> el administrador necesita información específica, <strong>cuando</strong> aplica un filtro por conductor o por vehículo, <strong>entonces</strong> el sistema muestra solo los datos asociados a ese conductor o vehículo.</li>
            <li><strong>Dado que</strong> el administrador aplica uno o más filtros, <strong>cuando</strong> confirma la selección, <strong>entonces</strong> la información del reporte se actualiza automáticamente según los filtros aplicados.</li>
        </ul>
    </td>
    <td style="text-align:center">EP05B</td>
</tr>
<!-- USER STORY 47 - Include incidents in reports -->
<tr>
    <td class="user-story-id" style="text-align:center">US47</td>
    <td style="text-align:center">Incluir incidencias en los reportes</td>
    <td>Como <strong>administrador de una empresa de movilidad escolar</strong>, quiero incluir las incidencias en los reportes, para tener un contexto completo del servicio.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el administrador genera un reporte, <strong>cuando</strong> el reporte incluye incidencias, <strong>entonces</strong> el sistema muestra las incidencias registradas en el período seleccionado.</li>
            <li><strong>Dado que</strong> las incidencias son visibles en el reporte, <strong>cuando</strong> el administrador las consulta, <strong>entonces</strong> cada incidencia se asocia con la ruta o vehículo correspondiente.</li>
            <li><strong>Dado que</strong> el administrador exporta el reporte, <strong>cuando</strong> se genera el archivo, <strong>entonces</strong> las incidencias quedan incluidas en el reporte exportado.</li>
        </ul>
    </td>
    <td style="text-align:center">EP05B</td>
</tr>
<!-- USER STORY 48 - General summary -->
<tr>
    <td class="user-story-id" style="text-align:center">US48</td>
    <td style="text-align:center">Resumen general</td>
    <td>Como <strong>administrador de una empresa de movilidad escolar</strong>, quiero ver un resumen general de desempeño, para tomar decisiones rápidas.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el administrador accede al panel de reportes, <strong>cuando</strong> visualiza el resumen general, <strong>entonces</strong> el sistema muestra indicadores clave resumidos del desempeño operativo.</li>
            <li><strong>Dado que</strong> el resumen general es visible, <strong>cuando</strong> el administrador lo consulta, <strong>entonces</strong> la presentación de los indicadores es simple, clara y fácil de entender.</li>
            <li><strong>Dado que</strong> el administrador utiliza el resumen para la toma de decisiones, <strong>cuando</strong> los datos cambian durante el turno, <strong>entonces</strong> el sistema actualiza periódicamente los indicadores.</li>
        </ul>
    </td>
    <td style="text-align:center">EP05B</td>
</tr>
<!-- USER STORY 49 - Quick download of recent reports -->
<tr>
    <td class="user-story-id" style="text-align:center">US49</td>
    <td style="text-align:center">Descarga rápida de reportes recientes</td>
    <td>Como <strong>administrador de una empresa de movilidad escolar</strong>, quiero acceder rápidamente a reportes recientes, para ahorrar tiempo en consultas frecuentes.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el administrador ha generado reportes previamente, <strong>cuando</strong> accede a la sección de reportes recientes, <strong>entonces</strong> el sistema presenta una lista de los reportes generados recientemente.</li>
            <li><strong>Dado que</strong> el administrador visualiza la lista de reportes recientes, <strong>cuando</strong> selecciona uno de ellos, <strong>entonces</strong> el sistema permite acceder al reporte con una sola acción.</li>
            <li><strong>Dado que</strong> el administrador necesita un reporte ya generado previamente, <strong>cuando</strong> accede a él desde la lista de recientes, <strong>entonces</strong> no es necesario generarlo nuevamente desde cero.</li>
        </ul>
    </td>
    <td style="text-align:center">EP05B</td>
</tr>
<!-- USER STORY 50 - View personal trip summary -->
<tr>
    <td class="user-story-id" style="text-align:center">US50</td>
    <td style="text-align:center">Visualizar resumen personal de viajes</td>
    <td>Como <strong>conductor independiente</strong>, quiero ver un resumen de mis viajes completados, para hacer seguimiento de mi actividad diaria.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor ha completado uno o más viajes, <strong>cuando</strong> accede a su sección de reportes, <strong>entonces</strong> el sistema muestra un resumen de los viajes completados durante el turno o período seleccionado.</li>
            <li><strong>Dado que</strong> el resumen de viajes es visible, <strong>cuando</strong> el conductor lo consulta, <strong>entonces</strong> el sistema incluye la cantidad de viajes, paradas realizadas y tiempos.</li>
            <li><strong>Dado que</strong> el conductor necesita revisar su actividad, <strong>cuando</strong> accede al resumen, <strong>entonces</strong> la información es clara y fácil de entender.</li>
        </ul>
    </td>
    <td style="text-align:center">EP05A</td>
</tr>
<!-- USER STORY 51 - View personal punctuality metrics -->
<tr>
    <td class="user-story-id" style="text-align:center">US51</td>
    <td style="text-align:center">Visualizar métricas personales de puntualidad</td>
    <td>Como <strong>conductor independiente</strong>, quiero ver mis métricas de puntualidad, para evaluar mi desempeño y mejorar mi reputación.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor ha realizado viajes en los últimos días, <strong>cuando</strong> accede a sus métricas de puntualidad, <strong>entonces</strong> el sistema muestra el porcentaje de llegadas a tiempo por parada o por viaje.</li>
            <li><strong>Dado que</strong> las métricas son visibles, <strong>cuando</strong> el conductor las consulta, <strong>entonces</strong> la información se presenta de forma clara y comprensible.</li>
            <li><strong>Dado que</strong> el conductor quiere mejorar su reputación, <strong>cuando</strong> revisa sus métricas, <strong>entonces</strong> puede identificar los días o paradas en los que tuvo retrasos.</li>
        </ul>
    </td>
    <td style="text-align:center">EP05A</td>
</tr>
<!-- USER STORY 52 - Export personal trip history -->
<tr>
    <td class="user-story-id" style="text-align:center">US52</td>
    <td style="text-align:center">Exportar historial personal de viajes</td>
    <td>Como <strong>conductor independiente</strong>, quiero exportar mi historial de viajes, para compartirlo con padres o empresas que soliciten referencias.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor ha seleccionado un período de tiempo, <strong>cuando</strong> solicita exportar su historial, <strong>entonces</strong> el sistema permite exportar los datos en formato PDF.</li>
            <li><strong>Dado que</strong> la exportación es iniciada, <strong>cuando</strong> el proceso finaliza, <strong>entonces</strong> el archivo descargado incluye los viajes realizados, fechas, horas y puntualidad.</li>
            <li><strong>Dado que</strong> el conductor necesita demostrar su confiabilidad, <strong>cuando</strong> comparte el reporte exportado, <strong>entonces</strong> la información es suficiente para validar su desempeño.</li>
        </ul>
    </td>
    <td style="text-align:center">EP05A</td>
</tr>
<!-- USER STORY 53 - View personal incident history -->
<tr>
    <td class="user-story-id" style="text-align:center">US53</td>
    <td style="text-align:center">Visualizar historial personal de incidencias</td>
    <td>Como <strong>conductor independiente</strong>, quiero ver las incidencias que he registrado, para tener trazabilidad de los eventos ocurridos durante mis servicios.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor ha registrado incidencias en viajes pasados, <strong>cuando</strong> accede a su historial de incidencias, <strong>entonces</strong> el sistema muestra una lista de las incidencias registradas.</li>
            <li><strong>Dado que</strong> la lista de incidencias es visible, <strong>cuando</strong> el conductor la consulta, <strong>entonces</strong> cada incidencia incluye el tipo, fecha, hora y ubicación.</li>
            <li><strong>Dado que</strong> el conductor necesita justificar un evento ante un padre o empresa, <strong>cuando</strong> consulta el detalle de una incidencia, <strong>entonces</strong> la información es suficiente para respaldar su explicación.</li>
        </ul>
    </td>
    <td style="text-align:center">EP05A</td>
</tr>
<!-- USER STORY 54 - Receive proximity notification -->
<tr>
    <td class="user-story-id" style="text-align:center">US54</td>
    <td style="text-align:center">Recibir notificación de proximidad</td>
    <td>Como <strong>padre de familia</strong>, quiero recibir una notificación automática cuando el vehículo escolar esté cerca de mi casa, para bajar a la puerta a tiempo sin esperar en la calle.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el vehículo escolar se encuentra en ruta hacia mi domicilio, <strong>cuando</strong> se aproxima a una distancia configurada (por ejemplo, 5 minutos o 500 metros), <strong>entonces</strong> el sistema envía una notificación push a mi dispositivo móvil indicando que el vehículo está por llegar.</li>
            <li><strong>Dado que</strong> la notificación de proximidad ha sido enviada, <strong>cuando</strong> la recibo, <strong>entonces</strong> el mensaje incluye el tiempo estimado de llegada y el nombre del conductor.</li>
            <li><strong>Dado que</strong> el vehículo se detiene en mi parada, <strong>cuando</strong> el conductor registra el abordaje, <strong>entonces</strong> el sistema envía una segunda notificación confirmando que mi hijo ha subido al vehículo.</li>
            <li><strong>Dado que</strong> no me encuentro disponible para recibir la notificación, <strong>cuando</strong> el sistema la envía, <strong>entonces</strong> queda almacenada en el historial de notificaciones para su consulta posterior.</li>
        </ul>
    </td>
    <td style="text-align:center">EP06</td>
</tr>
<!-- USER STORY 55 - View real-time location of my child -->
<tr>
    <td class="user-story-id" style="text-align:center">US55</td>
    <td style="text-align:center">Visualizar ubicación en tiempo real de mi hijo</td>
    <td>Como <strong>padre de familia</strong>, quiero ver en un mapa la ubicación en tiempo real del vehículo escolar, para tener tranquilidad durante el trayecto de mi hijo.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> mi hijo ha abordado el vehículo escolar, <strong>cuando</strong> accedo a la sección de seguimiento en la aplicación, <strong>entonces</strong> el sistema muestra un mapa con la ubicación actual del vehículo.</li>
            <li><strong>Dado que</strong> el vehículo se desplaza durante el trayecto, <strong>cuando</strong> su ubicación cambia, <strong>entonces</strong> el sistema actualiza automáticamente el punto en el mapa en tiempo real.</li>
            <li><strong>Dado que</strong> el vehículo se encuentra dentro del colegio o en una zona sin señal, <strong>cuando</strong> consulto la ubicación, <strong>entonces</strong> el sistema muestra la última ubicación conocida con una marca de tiempo.</li>
            <li><strong>Dado que</strong> mi hijo aún no ha abordado el vehículo, <strong>cuando</strong> accedo al mapa, <strong>entonces</strong> el sistema indica que el seguimiento estará disponible una vez que se registre el abordaje.</li>
        </ul>
    </td>
    <td style="text-align:center">EP06</td>
</tr>
<!-- USER STORY 56 - Receive arrival confirmation at school -->
<tr>
    <td class="user-story-id" style="text-align:center">US56</td>
    <td style="text-align:center">Recibir confirmación de llegada al colegio</td>
    <td>Como <strong>padre de familia</strong>, quiero recibir una notificación cuando mi hijo llegue al colegio, para confirmar que arribó sano y salvo a su destino.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el vehículo escolar llega al colegio y el conductor registra el descenso de mi hijo, <strong>cuando</strong> el evento es registrado en el sistema, <strong>entonces</strong> recibo una notificación push confirmando la llegada segura al colegio.</li>
            <li><strong>Dado que</strong> la notificación de llegada ha sido enviada, <strong>cuando</strong> la recibo, <strong>entonces</strong> el mensaje incluye la hora exacta de llegada y el nombre del colegio.</li>
            <li><strong>Dado que</strong> mi hijo no desciende del vehículo en el colegio, <strong>cuando</strong> el conductor finaliza la ruta, <strong>entonces</strong> el sistema me notifica que mi hijo no ha sido registrado como descendido para que pueda contactar al conductor.</li>
        </ul>
    </td>
    <td style="text-align:center">EP06</td>
</tr>
<!-- USER STORY 57 - Receive absence notification -->
<tr>
    <td class="user-story-id" style="text-align:center">US57</td>
    <td style="text-align:center">Recibir notificación de ausencia del estudiante</td>
    <td>Como <strong>padre de familia</strong>, quiero recibir una notificación cuando mi hijo no aborde el vehículo en su parada, para saber que no fue recogido y actuar en consecuencia.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor ha llegado a mi parada y mi hijo no se ha presentado en el tiempo establecido, <strong>cuando</strong> el sistema detecta la ausencia, <strong>entonces</strong> recibo una notificación informándome que mi hijo no abordó el vehículo.</li>
            <li><strong>Dado que</strong> he recibido la notificación de ausencia, <strong>cuando</strong> accedo a la aplicación, <strong>entonces</strong> puedo confirmar si mi hijo no asistirá al colegio o si hubo un error.</li>
            <li><strong>Dado que</strong> confirmo que mi hijo no asistirá, <strong>cuando</strong> envío la respuesta, <strong>entonces</strong> el sistema omite la parada en la ruta del conductor y actualiza el registro de asistencia.</li>
        </ul>
    </td>
    <td style="text-align:center">EP06</td>
</tr>
<!-- USER STORY 58 - Receive notification of incident affecting my child -->
<tr>
    <td class="user-story-id" style="text-align:center">US58</td>
    <td style="text-align:center">Recibir notificación de incidencia que afecta a mi hijo</td>
    <td>Como <strong>padre de familia</strong>, quiero recibir una notificación cuando ocurra una incidencia que afecte la ruta de mi hijo, para estar informado sin tener que llamar al conductor.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el conductor registra una incidencia que afecta el tiempo estimado de llegada (retraso, desvío, avería), <strong>cuando</strong> el sistema procesa el evento, <strong>entonces</strong> recibo una notificación push informándome sobre la incidencia y el nuevo tiempo estimado.</li>
            <li><strong>Dado que</strong> la incidencia es de carácter grave (accidente, emergencia médica), <strong>cuando</strong> el conductor la marca como crítica, <strong>entonces</strong> recibo una alerta prioritaria con instrucciones claras sobre el estado de mi hijo.</li>
            <li><strong>Dado que</strong> la incidencia ha sido resuelta y el servicio se normaliza, <strong>cuando</strong> el conductor confirma la resolución, <strong>entonces</strong> recibo una notificación indicando que el servicio continúa con normalidad.</li>
            <li><strong>Dado que</strong> recibo una notificación de incidencia, <strong>cuando</strong> accedo al detalle desde la aplicación, <strong>entonces</strong> el sistema muestra la descripción del evento, la ubicación y el tiempo estimado actualizado.</li>
        </ul>
    </td>
    <td style="text-align:center">EP06</td>
</tr>
<!-- USER STORY 59 - Hero & Core Pitch -->
        <tr>
            <td class="user-story-id" style="text-align:center">US59</td>
            <td style="text-align:center">Visualizar Hero section, métricas y pitch principal</td>
            <td>Como <strong>visitante del sitio web</strong>, quiero visualizar un lema principal claro, métricas de confianza y accesos directos en la cabecera, para entender de inmediato el propósito de Children Path e iniciar mi interacción.</td>
            <td class="acceptance-criteria">
                <ul>
                    <li><strong>Dado que</strong> un visitante carga la página web pública, <strong>cuando</strong> la sección principal se renderiza, <strong>entonces</strong> el sistema presenta la barra de navegación, el titular de monitoreo en vivo, la tarjeta interactiva de simulación de ruta y botones CTA ("Request a demo", "View plans").</li>
                    <li><strong>Dado que</strong> el usuario visualiza la parte inferior del Hero, <strong>cuando</strong> continúa navegando, <strong>entonces</strong> el sistema expone los indicadores de confianza (24/7, 100% de cobertura, diseñado para Lima, +500 familias y conductores).</li>
                </ul>
            </td>
            <td style="text-align:center">EP00</td>
        </tr>
        <!-- USER STORY 60 - Stakeholder Benefits -->
        <tr>
            <td class="user-story-id" style="text-align:center">US60</td>
            <td style="text-align:center">Explorar beneficios segmentados por rol de usuario</td>
            <td>Como <strong>visitante (padre de familia, conductor o directivo escolar)</strong>, quiero consultar las tarjetas de beneficios específicas para mi segmento, para evaluar cómo la solución resuelve mis necesidades particulares.</td>
            <td class="acceptance-criteria">
                <ul>
                    <li><strong>Dado que</strong> el visitante navega hacia la sección "Benefits for every stakeholder", <strong>cuando</strong> revisa las tarjetas, <strong>entonces</strong> el sistema presenta columnas diferenciadas para Families, Drivers y Companies & Schools con listas de verificación de características.</li>
                    <li><strong>Dado que</strong> el usuario accede desde un smartphone, <strong>cuando</strong> el ancho de pantalla es inferior a 768px, <strong>entonces</strong> las tarjetas de beneficios se reorganizan en una sola columna vertical sin desbordes horizontales.</li>
                </ul>
            </td>
            <td style="text-align:center">EP00</td>
        </tr>
        <!-- USER STORY 61 - How it works modules -->
        <tr>
            <td class="user-story-id" style="text-align:center">US61</td>
            <td style="text-align:center">Consultar módulos de funcionamiento y seguridad de la plataforma</td>
            <td>Como <strong>visitante interesado en la operatividad</strong>, quiero examinar la sección "How ChildrenPath Works", para conocer las garantías de alertas, soporte digital, geocercas y privacidad de datos.</td>
            <td class="acceptance-criteria">
                <ul>
                    <li><strong>Dado que</strong> el visitante revisa la cuadrícula funcional, <strong>cuando</strong> explora los bloques interactivos, <strong>entonces</strong> el sistema detalla los módulos de Alerts, Digital Assistance, Safe Routes, Fleet Monitoring, Integration y Privacy.</li>
                    <li><strong>Dado que</strong> el visitante presiona un elemento informativo, <strong>cuando</strong> interactúa con el contenido, <strong>entonces</strong> la descripción técnica del servicio se visualiza de forma legible y clara.</li>
                </ul>
            </td>
            <td style="text-align:center">EP00</td>
        </tr>
        <!-- USER STORY 62 - Pricing Tiers -->
        <tr>
            <td class="user-story-id" style="text-align:center">US62</td>
            <td style="text-align:center">Consultar planes de suscripción y tarifas comerciales</td>
            <td>Como <strong>visitante del segmento transportista o directivo</strong>, quiero consultar las opciones tarifarias en "Plans for every need", para comparar el alcance según el tamaño de la flota o colegio.</td>
            <td class="acceptance-criteria">
                <ul>
                    <li><strong>Dado que</strong> el visitante llega al bloque de tarifas, <strong>cuando</strong> revisa las tarjetas de precios, <strong>entonces</strong> el sistema expone los planes Independent Driver, Company y School destacando sus características incluidas y botones de selección ("Get Started", "Request Demo").</li>
                    <li><strong>Dado que</strong> el visitante hace clic sobre "Request Demo" en el plan School, <strong>cuando</strong> se acciona el botón, <strong>entonces</strong> la página se desplaza mediante scroll suave directamente a la sección de contacto.</li>
                </ul>
            </td>
            <td style="text-align:center">EP00</td>
        </tr>
        <!-- USER STORY 63 - Testimonials & FAQ -->
        <tr>
            <td class="user-story-id" style="text-align:center">US63</td>
            <td style="text-align:center">Revisar testimonios reales y preguntas frecuentes (FAQ)</td>
            <td>Como <strong>visitante con dudas sobre el servicio</strong>, quiero leer testimonios de usuarios activos y desplegar preguntas frecuentes interactivas, para resolver inquietudes técnicas y de cobertura antes de solicitar una demo.</td>
            <td class="acceptance-criteria">
                <ul>
                    <li><strong>Dado que</strong> el visitante llega a "What our users say", <strong>cuando</strong> revisa los testimonios, <strong>entonces</strong> el sistema muestra citas y roles validados de padres, conductores y colegios aliados.</li>
                    <li><strong>Dado que</strong> el visitante interactúa con el acordeón de "Frequently Asked Questions", <strong>cuando</strong> hace clic en una pregunta, <strong>entonces</strong> la respuesta se despliega de manera fluida y contrae cualquier otra respuesta previamente abierta.</li>
                </ul>
            </td>
            <td style="text-align:center">EP00</td>
        </tr>
        <!-- USER STORY 64 - Contact & Footer -->
        <tr>
            <td class="user-story-id" style="text-align:center">US64</td>
            <td style="text-align:center">Solicitar demostración comercial y acceder a canales de contacto</td>
            <td>Como <strong>visitante interesado</strong>, quiero consultar los canales de soporte directo y enlaces en el pie de página, para comunicarme por WhatsApp, correo o teléfono con el equipo de Children Path.</td>
            <td class="acceptance-criteria">
                <ul>
                    <li><strong>Dado que</strong> el visitante llega al contenedor "Contact Us", <strong>cuando</strong> revisa la información de atención, <strong>entonces</strong> el sistema muestra el número telefónico, correo oficial, botón de WhatsApp y horario de atención para Lima Metropolitana.</li>
                    <li><strong>Dado que</strong> el usuario visualiza el pie de página (footer), <strong>cuando</strong> presiona los botones de redes sociales (F, I, L) o enlaces a políticas de privacidad, <strong>entonces</strong> el sistema abre los destinos correspondientes en pestañas independientes.</li>
                </ul>
            </td>
            <td style="text-align:center">EP00</td>
        </tr>
        <!-- USER STORY 65 - Authentication Endpoint -->
        <tr>
            <td class="user-story-id" style="text-align:center">US65</td>
            <td style="text-align:center">Endpoint de autenticación y emisión de tokens JWT</td>
            <td>Como <strong>developer</strong>, quiero disponer de un endpoint POST <code>/api/v1/authentication/sign-in</code>, para validar credenciales y emitir tokens de sesión estructurados.</td>
            <td class="acceptance-criteria">
                <ul>
                    <li><strong>Dado que</strong> el cliente envía una petición POST con correo y contraseña válidos, <strong>cuando</strong> el servicio autentica la cuenta, <strong>entonces</strong> retorna código de estado HTTP 200 con el token JWT y los datos de perfil en el cuerpo de la respuesta.</li>
                    <li><strong>Dado que</strong> el cliente envía credenciales inválidas o no registradas, <strong>cuando</strong> el servicio procesa la solicitud, <strong>entonces</strong> responde con código de estado HTTP 401 Unauthorized y un objeto de error detallado.</li>
                </ul>
            </td>
            <td style="text-align:center">EP07</td>
        </tr>
        <!-- USER STORY 66 - Attendance Check Endpoint -->
        <tr>
            <td class="user-story-id" style="text-align:center">US66</td>
            <td style="text-align:center">Endpoint para registro de asistencia en un solo toque</td>
            <td>Como <strong>developer</strong>, quiero disponer de un endpoint PUT <code>/api/v1/attendance-records/{id}</code>, para actualizar el estado de abordaje y persistir marcas temporales.</td>
            <td class="acceptance-criteria">
                <ul>
                    <li><strong>Dado que</strong> el cliente envía una petición PUT válida con el identificador del registro y el nuevo estado (<code>on_board</code>, <code>arrived</code>, <code>absent</code>), <strong>cuando</strong> la solicitud es procesada, <strong>entonces</strong> el servidor actualiza la entidad de asistencia y responde con código HTTP 200 y el recurso modificado.</li>
                    <li><strong>Dado que</strong> se provee un identificador inexistente, <strong>cuando</strong> se ejecuta la consulta, <strong>entonces</strong> el servidor devuelve un código HTTP 404 Not Found.</li>
                </ul>
            </td>
            <td style="text-align:center">EP07</td>
        </tr>
        <!-- USER STORY 67 - Telemetry and Geofence Endpoint -->
        <tr>
            <td class="user-story-id" style="text-align:center">US67</td>
            <td style="text-align:center">Endpoint para telemetría y geocercas en tiempo real</td>
            <td>Como <strong>developer</strong>, quiero un endpoint POST <code>/api/v1/trips/{id}/location</code>, para recibir coordenadas GPS periódicas y disparar alertas de proximidad automáticas.</td>
            <td class="acceptance-criteria">
                <ul>
                    <li><strong>Dado que</strong> el dispositivo móvil del conductor transmite latitud y longitud válidas, <strong>cuando</strong> el servicio verifica las geocercas configuradas, <strong>entonces</strong> registra la posición, evalúa los radios de alerta y responde con código HTTP 202 Accepted.</li>
                    <li><strong>Dado que</strong> la carga de datos presenta valores numéricos nulos o fuera de rango, <strong>cuando</strong> el validador inspecciona la petición, <strong>entonces</strong> retorna código HTTP 400 Bad Request.</li>
                </ul>
            </td>
            <td style="text-align:center">EP07</td>
        </tr>
<!-- USER STORY 68 - Sticky Navigation & Smooth Scroll -->
<tr>
    <td class="user-story-id" style="text-align:center">US68</td>
    <td style="text-align:center">Navegación sticky y desplazamiento suave entre secciones</td>
    <td>Como <strong>visitante del sitio web</strong>, quiero navegar entre las secciones del Landing Page mediante una barra de navegación fija y desplazamiento suave, para acceder rápidamente a la información que me interesa sin perder mi contexto.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el visitante se encuentra en cualquier sección del Landing Page, <strong>cuando</strong> hace clic en un enlace del menú de navegación, <strong>entonces</strong> el sistema desplaza la vista suavemente hasta la sección seleccionada.</li>
            <li><strong>Dado que</strong> el visitante ha iniciado el desplazamiento hacia abajo, <strong>cuando</strong> supera la altura del Hero, <strong>entonces</strong> la barra de navegación permanece fija en la parte superior de la ventana.</li>
            <li><strong>Dado que</strong> el visitante navega en un dispositivo móvil, <strong>cuando</strong> abre el menú de navegación, <strong>entonces</strong> el sistema presenta un menú colapsable adaptado al ancho de pantalla.</li>
        </ul>
    </td>
    <td style="text-align:center">EP00</td>
</tr>

<!-- USER STORY 69 - CTA Redirection to Web Application -->
<tr>
    <td class="user-story-id" style="text-align:center">US69</td>
    <td style="text-align:center">Redirección de CTAs al Web Application según segmento</td>
    <td>Como <strong>visitante del sitio web</strong>, quiero que los botones de llamada a la acción (CTA) me dirijan a la vista correspondiente dentro del Web Application según mi perfil, para iniciar la experiencia como padre, conductor o empresa sin pasos redundantes.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el visitante se identifica como padre de familia, <strong>cuando</strong> presiona el CTA "Start as Parent", <strong>entonces</strong> el sistema lo redirige a la vista de registro/inicio de sesión del Web Application para padres.</li>
            <li><strong>Dado que</strong> el visitante se identifica como conductor, <strong>cuando</strong> presiona el CTA "Start as Driver", <strong>entonces</strong> el sistema lo redirige a la vista de registro/inicio de sesión del Web Application para conductores.</li>
            <li><strong>Dado que</strong> el visitante representa a una empresa o colegio, <strong>cuando</strong> presiona el CTA "Request Demo", <strong>entonces</strong> el sistema lo redirige al formulario de contacto institucional del Web Application.</li>
            <li><strong>Dado que</strong> el visitante es recurrente y ya tiene cuenta, <strong>cuando</strong> presiona "Sign In", <strong>entonces</strong> el sistema lo redirige a la vista de autenticación correspondiente.</li>
        </ul>
    </td>
    <td style="text-align:center">EP00</td>
</tr>

<!-- USER STORY 70 - Language Switcher (i18n) -->
<tr>
    <td class="user-story-id" style="text-align:center">US70</td>
    <td style="text-align:center">Selector de idioma en el Landing Page (i18n)</td>
    <td>Como <strong>visitante del sitio web</strong>, quiero cambiar el idioma del Landing Page entre inglés (en_US) y español latinoamericano (es_419), para consumir la información en mi idioma preferido.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el visitante accede al Landing Page, <strong>cuando</strong> la página carga por primera vez, <strong>entonces</strong> el sistema presenta el contenido por defecto en inglés (en_US).</li>
            <li><strong>Dado que</strong> el visitante interactúa con el selector de idioma, <strong>cuando</strong> selecciona español (es_419), <strong>entonces</strong> el sistema actualiza todos los textos, etiquetas y metadatos del Landing Page al idioma seleccionado sin recargar la página.</li>
            <li><strong>Dado que</strong> el visitante ha cambiado el idioma, <strong>cuando</strong> navega entre secciones o recarga la página, <strong>entonces</strong> el sistema conserva el idioma seleccionado durante la sesión.</li>
            <li><strong>Dado que</strong> el visitante regresa al sitio posteriormente, <strong>cuando</strong> accede al Landing Page, <strong>entonces</strong> el sistema recupera la preferencia de idioma previamente almacenada.</li>
        </ul>
    </td>
    <td style="text-align:center">EP00</td>
</tr>

<!-- USER STORY 71 - Accessibility (a11y) -->
<tr>
    <td class="user-story-id" style="text-align:center">US71</td>
    <td style="text-align:center">Accesibilidad del Landing Page (a11y)</td>
    <td>Como <strong>visitante con necesidades de accesibilidad</strong>, quiero que el Landing Page cumpla con atributos ARIA, contraste adecuado y navegación por teclado, para poder consumir la información sin barreras.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el visitante utiliza un lector de pantalla, <strong>cuando</strong> navega por el Landing Page, <strong>entonces</strong> el sistema expone los atributos ARIA (roles, labels, descriptions) en los elementos interactivos.</li>
            <li><strong>Dado que</strong> el visitante navega únicamente con el teclado, <strong>cuando</strong> presiona la tecla Tab, <strong>entonces</strong> el sistema resalta secuencialmente cada elemento interactivo con un indicador de foco visible.</li>
            <li><strong>Dado que</strong> el visitante tiene baja visión, <strong>cuando</strong> visualiza el contenido, <strong>entonces</strong> el sistema mantiene un ratio de contraste mínimo de 4.5:1 entre texto y fondo según WCAG 2.1 AA.</li>
            <li><strong>Dado que</strong> el visitante accede a través de un dispositivo con imágenes desactivadas, <strong>cuando</strong> el navegador carga la página, <strong>entonces</strong> todas las imágenes incluyen el atributo <code>alt</code> con descripción textual.</li>
        </ul>
    </td>
    <td style="text-align:center">EP00</td>
</tr>

<!-- USER STORY 72 - About-the-Product Video -->
<tr>
    <td class="user-story-id" style="text-align:center">US72</td>
    <td style="text-align:center">Reproducir el video About-the-Product en el Landing Page</td>
    <td>Como <strong>visitante del sitio web</strong>, quiero reproducir el video About-the-Product desde el Landing Page, para conocer de forma audiovisual el modelo de negocio y las características principales de Children Path.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el visitante accede a la sección de video del Landing Page, <strong>cuando</strong> la página carga, <strong>entonces</strong> el sistema muestra el reproductor incrustado con el video About-the-Product en formato reproducible.</li>
            <li><strong>Dado que</strong> el visitante presiona el botón de reproducción, <strong>cuando</strong> el video inicia, <strong>entonces</strong> el sistema reproduce el contenido audiovisual sin salir del Landing Page.</li>
            <li><strong>Dado que</strong> el visitante accede desde un dispositivo móvil, <strong>cuando</strong> visualiza el video, <strong>entonces</strong> el reproductor se adapta al ancho de pantalla manteniendo la proporción original.</li>
        </ul>
    </td>
    <td style="text-align:center">EP00</td>
</tr>

<!-- USER STORY 73 - About-the-Team Video -->
<tr>
    <td class="user-story-id" style="text-align:center">US73</td>
    <td style="text-align:center">Reproducir el video About-the-Team en el Landing Page</td>
    <td>Como <strong>visitante del sitio web</strong>, quiero reproducir el video About-the-Team desde el Landing Page, para conocer al equipo detrás de Children Path y su proceso de trabajo.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el visitante accede a la sección "Our Team" del Landing Page, <strong>cuando</strong> la página carga, <strong>entonces</strong> el sistema muestra el reproductor incrustado con el video About-the-Team.</li>
            <li><strong>Dado que</strong> el visitante presiona el botón de reproducción, <strong>cuando</strong> el video inicia, <strong>entonces</strong> el sistema reproduce el contenido sin salir del Landing Page.</li>
            <li><strong>Dado que</strong> el visitante no puede reproducir el video (por restricciones de red o dispositivo), <strong>cuando</strong> el reproductor falla, <strong>entonces</strong> el sistema muestra un enlace alternativo al video publicado en YouTube.</li>
        </ul>
    </td>
    <td style="text-align:center">EP00</td>
</tr>

<!-- USER STORY 74 - Legal Terms, Privacy & Policies -->
<tr>
    <td class="user-story-id" style="text-align:center">US74</td>
    <td style="text-align:center">Acceder a términos, privacidad y políticas legales</td>
    <td>Como <strong>visitante del sitio web</strong>, quiero acceder a los términos y condiciones, política de privacidad y código de ética desde el footer del Landing Page, para conocer el marco legal y ético bajo el cual opera Children Path.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el visitante se encuentra en el footer del Landing Page, <strong>cuando</strong> revisa los enlaces legales, <strong>entonces</strong> el sistema muestra los accesos a "Terms and Conditions", "Privacy Policy" y "Code of Ethics".</li>
            <li><strong>Dado que</strong> el visitante presiona cualquiera de los enlaces legales, <strong>cuando</strong> el sistema procesa la acción, <strong>entonces</strong> abre el documento correspondiente en una nueva pestaña del navegador.</li>
            <li><strong>Dado que</strong> el visitante accede a los términos y condiciones, <strong>cuando</strong> la página carga, <strong>entonces</strong> el sistema presenta el contenido completo redactado conforme al código de ética ACM/IEEE y CIP.</li>
        </ul>
    </td>
    <td style="text-align:center">EP00</td>
</tr>

<!-- USER STORY 75 - SEO Tags and Meta Tags -->
<tr>
    <td class="user-story-id" style="text-align:center">US75</td>
    <td style="text-align:center">Optimización SEO y metadatos del Landing Page</td>
    <td>Como <strong>visitante que llega desde un motor de búsqueda</strong>, quiero que el Landing Page cuente con meta tags y estructura semántica adecuada, para encontrar la información de Children Path fácilmente.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> un buscador indexa el Landing Page, <strong>cuando</strong> analiza la página principal, <strong>entonces</strong> el sistema expone los metadatos Title, Description, Keywords y Author en el <code>&lt;head&gt;</code> del documento.</li>
            <li><strong>Dado que</strong> el visitante comparte el enlace del Landing Page en redes sociales, <strong>cuando</strong> la plataforma genera la vista previa, <strong>entonces</strong> el sistema muestra el título, descripción e imagen Open Graph configurados.</li>
            <li><strong>Dado que</strong> el buscador rastrea el sitio, <strong>cuando</strong> indexa el contenido, <strong>entonces</strong> el sistema emplea etiquetas HTML semánticas (header, nav, main, section, article, footer) para estructurar la información.</li>
        </ul>
    </td>
    <td style="text-align:center">EP00</td>
</tr>

<!-- USER STORY 76 - Responsive Design -->
<tr>
    <td class="user-story-id" style="text-align:center">US76</td>
    <td style="text-align:center">Adaptabilidad responsive del Landing Page</td>
    <td>Como <strong>visitante del sitio web</strong>, quiero que el Landing Page se adapte a las dimensiones de mi dispositivo (desktop, tablet, mobile), para visualizar el contenido de forma clara sin desplazamientos horizontales.</td>
    <td class="acceptance-criteria">
        <ul>
            <li><strong>Dado que</strong> el visitante accede desde un dispositivo móvil, <strong>cuando</strong> el ancho de pantalla es inferior a 768px, <strong>entonces</strong> el sistema reorganiza el contenido en una sola columna vertical sin desbordes horizontales.</li>
            <li><strong>Dado que</strong> el visitante accede desde una tablet, <strong>cuando</strong> el ancho de pantalla está entre 768px y 1024px, <strong>entonces</strong> el sistema ajusta el layout a dos columnas manteniendo la legibilidad.</li>
            <li><strong>Dado que</strong> el visitante accede desde un desktop, <strong>cuando</strong> el ancho de pantalla supera los 1024px, <strong>entonces</strong> el sistema muestra el layout completo con todas las secciones en su disposición original.</li>
            <li><strong>Dado que</strong> el visitante rota su dispositivo, <strong>cuando</strong> cambia entre orientación vertical y horizontal, <strong>entonces</strong> el sistema reacomoda el contenido sin pérdida de información.</li>
        </ul>
    </td>
    <td style="text-align:center">EP00</td>
</tr>
    </tbody>
</table>


## **3.2. Impact Mapping**

<img width="1240" height="12991" alt="Impact map 60 (3)" src="../assets/chapter-3/impact-map-60.jpg" />



[Ver artefacto en uxpressia](https://uxpressia.com/w/v8FzI/i/Fy0pk?tagId=EaWxj)

## **3.3. Product Backlog**

En esta sección se presenta el Product Backlog priorizado por valor de negocio para los distintos actores de la plataforma. Siguiendo las directrices metodológicas, las historias de usuario asociadas al sitio web estático (Landing Page) han sido situadas al inicio para su despliegue y validación temprana desde el Sprint 1. Asimismo, los ítems han sido estimados en Story Points utilizando la escala estándar (1, 2, 3, 5, 8).

| # Orden | User Story Id | Título | Descripción | Story Points |
| :---: | :---: | :--- | :--- | :---: |
| **1** | **US59** | Visualizar Hero section, métricas y pitch principal | Como visitante del sitio web, quiero visualizar un lema principal claro, métricas de confianza y accesos directos en la cabecera, para entender de inmediato el propósito de Children Path e iniciar mi interacción. | 3 |
| **2** | **US60** | Explorar beneficios segmentados por rol de usuario | Como visitante (padre de familia, conductor o directivo escolar), quiero consultar las tarjetas de beneficios específicas para mi segmento, para evaluar cómo la solución resuelve mis necesidades particulares. | 2 |
| **3** | **US61** | Consultar módulos de funcionamiento y seguridad de la plataforma | Como visitante interesado en la operatividad, quiero examinar la sección "How ChildrenPath Works", para conocer las garantías de alertas, soporte digital, geocercas y privacidad de datos. | 3 |
| **4** | **US62** | Consultar planes de suscripción y tarifas comerciales | Como visitante del segmento transportista o directivo, quiero consultar las opciones tarifarias en "Plans for every need", para comparar el alcance según el tamaño de la flota o colegio. | 2 |
| **5** | **US63** | Revisar testimonios reales y preguntas frecuentes (FAQ) | Como visitante con dudas sobre el servicio, quiero leer testimonios de usuarios activos y desplegar preguntas frecuentes interactivas, para resolver inquietudes técnicas y de cobertura antes de solicitar una demo. | 2 |
| **6** | **US64** | Solicitar demostración comercial y acceder a canales de contacto | Como visitante interesado, quiero consultar los canales de soporte directo y enlaces en el pie de página, para comunicarme por WhatsApp, correo o teléfono con el equipo de Children Path. | 2 |
| **7** | **US68** | Navegación sticky y desplazamiento suave entre secciones | Como visitante del sitio web, quiero navegar entre las secciones del Landing Page mediante una barra de navegación fija y desplazamiento suave, para acceder rápidamente a la información que me interesa sin perder mi contexto. | 3 |
| **8** | **US69** | Redirección de CTAs al Web Application según segmento | Como visitante del sitio web, quiero que los botones de llamada a la acción (CTA) me dirijan a la vista correspondiente dentro del Web Application según mi perfil, para iniciar la experiencia como padre, conductor o empresa sin pasos redundantes. | 5 |
| **9** | **US70** | Selector de idioma en el Landing Page (i18n) | Como visitante del sitio web, quiero cambiar el idioma del Landing Page entre inglés (en_US) y español latinoamericano (es_419), para consumir la información en mi idioma preferido. | 5 |
| **10** | **US71** | Accesibilidad del Landing Page (a11y) | Como visitante con necesidades de accesibilidad, quiero que el Landing Page cumpla con atributos ARIA, contraste adecuado y navegación por teclado, para poder consumir la información sin barreras. | 5 |
| **11** | **US72** | Reproducir el video About-the-Product en el Landing Page | Como visitante del sitio web, quiero reproducir el video About-the-Product desde el Landing Page, para conocer de forma audiovisual el modelo de negocio y las características principales de Children Path. | 2 |
| **12** | **US73** | Reproducir el video About-the-Team en el Landing Page | Como visitante del sitio web, quiero reproducir el video About-the-Team desde el Landing Page, para conocer al equipo detrás de Children Path y su proceso de trabajo. | 2 |
| **13** | **US74** | Acceder a términos, privacidad y políticas legales | Como visitante del sitio web, quiero acceder a los términos y condiciones, política de privacidad y código de ética desde el footer del Landing Page, para conocer el marco legal y ético bajo el cual opera Children Path. | 2 |
| **14** | **US75** | Optimización SEO y metadatos del Landing Page | Como visitante que llega desde un motor de búsqueda, quiero que el Landing Page cuente con meta tags y estructura semántica adecuada, para encontrar la información de Children Path fácilmente. | 2 |
| **15** | **US76** | Adaptabilidad responsive del Landing Page | Como visitante del sitio web, quiero que el Landing Page se adapte a las dimensiones de mi dispositivo (desktop, tablet, mobile), para visualizar el contenido de forma clara sin desplazamientos horizontales. | 3 |
| **16** | **US12** | Visualizar lista de estudiantes por ruta | Como conductor, quiero ver la lista de estudiantes asignados a mi ruta, para saber a quiénes debo recoger. | 2 |
| **17** | **US13** | Visualizar estudiantes por parada | Como conductor, quiero ver qué estudiantes corresponden a cada parada, para organizar el recojo. | 2 |
| **18** | **US14** | Registrar abordaje | Como conductor, quiero marcar rápidamente cuándo un estudiante sube al vehículo, para llevar el control del viaje. | 2 |
| **19** | **US15** | Registrar ausencia | Como conductor, quiero marcar cuándo un estudiante no sube al vehículo, para evitar esperas innecesarias. | 2 |
| **20** | **US16** | Edición rápida de estado | Como conductor, quiero corregir el estado de un estudiante en caso de error, para mantener la información precisa. | 2 |
| **21** | **US18** | Confirmación visual rápida | Como conductor, quiero identificar rápidamente quién ya subió y quién no, para tomar decisiones rápidas. | 1 |
| **22** | **US01** | Registrar abordaje del estudiante | Como conductor, quiero registrar el momento en que un estudiante aborda el vehículo en cada parada, para mantener un registro digital de asistencia. | 3 |
| **23** | **US19** | Visualizar ruta asignada | Como conductor, quiero visualizar la ruta asignada del día, para conocer el orden del recorrido. | 2 |
| **24** | **US22** | Marcar parada como completada | Como conductor, quiero marcar una parada como completada, para avanzar en mi ruta de manera ordenada. | 1 |
| **25** | **US24** | Visualizar estado de la ruta | Como conductor, quiero ver el progreso de mi ruta, para saber cuánto falta por completar. | 2 |
| **26** | **US36** | Visualizar detalles del vehículo | Como administrador de una empresa de movilidad escolar, quiero seleccionar un vehículo y ver su información, para conocer su estado actual. | 2 |
| **27** | **US37** | Visualizar estados de los vehículos | Como administrador de una empresa de movilidad escolar, quiero identificar el estado de cada vehículo, para detectar problemas rápidamente. | 2 |
| **28** | **US38** | Filtrar unidades | Como administrador de una empresa de movilidad escolar, quiero filtrar vehículos por estado o ruta, para enfocarme en lo relevante. | 2 |
| **29** | **US50** | Visualizar resumen personal de viajes | Como conductor independiente, quiero ver un resumen de mis viajes completados, para hacer seguimiento de mi actividad diaria. | 2 |
| **30** | **US28** | Seleccionar tipo de incidencia | Como conductor, quiero elegir el tipo de incidencia, para clasificar correctamente el evento. | 2 |
| **31** | **US29** | Registrar detalle opcional | Como conductor, quiero agregar un comentario opcional, para proporcionar más contexto si es necesario. | 1 |
| **32** | **US30** | Asociar incidencia con parada o estudiante | Como conductor, quiero vincular la incidencia a una parada o estudiante, para mayor precisión en el registro. | 2 |
| **33** | **US32** | Visualizar historial de incidencias | Como conductor, quiero ver las incidencias registradas, para hacer seguimiento del recorrido. | 2 |
| **34** | **US33** | Editar o corregir incidencia | Como conductor, quiero corregir una incidencia en caso de error, para mantener la información precisa. | 2 |
| **35** | **US26** | Registro rápido de incidencia | Como conductor, quiero registrar una incidencia en pocos pasos, para no distraerme durante el recorrido. | 2 |
| **36** | **US05** | Registrar incidencia en la ruta | Como conductor, quiero registrar cualquier incidencia que ocurra durante el viaje (retraso, accidente, cambio de ruta), para mantener la trazabilidad del servicio. | 3 |
| **37** | **US20** | Visualizar paradas en el mapa | Como conductor, quiero ver las paradas de mi ruta en un mapa, para ubicarme fácilmente durante el recorrido. | 3 |
| **38** | **US03** | Visualizar ruta diaria optimizada | Como conductor, quiero visualizar la ruta del día con el orden de las paradas y los tiempos estimados, para reducir los tiempos de espera y el consumo de combustible. | 3 |
| **39** | **US21** | Navegación entre paradas | Como conductor, quiero recibir indicaciones para llegar a cada parada, para optimizar mi recorrido. | 3 |
| **40** | **US23** | Reordenamiento básico de ruta | Como conductor, quiero ajustar el orden de las paradas en caso de imprevistos, para adaptarme a cambios en el recorrido. | 3 |
| **41** | **US04** | Reordenar ruta por ausencia | Como conductor, quiero que la ruta se reordene automáticamente cuando un estudiante está ausente, para no perder tiempo pasando por una parada vacía. | 3 |
| **42** | **US09** | Visualizar historial personal de viajes | Como conductor independiente, quiero acceder a mi historial de viajes, puntualidad e incidencias registradas, para evaluar mi desempeño y demostrar mi confiabilidad a los padres. | 3 |
| **43** | **US51** | Visualizar métricas personales de puntualidad | Como conductor independiente, quiero ver mis métricas de puntualidad, para evaluar mi desempeño y mejorar mi reputación. | 3 |
| **44** | **US52** | Exportar historial personal de viajes | Como conductor independiente, quiero exportar mi historial de viajes, para compartirlo con padres o empresas que soliciten referencias. | 3 |
| **45** | **US53** | Visualizar historial personal de incidencias | Como conductor independiente, quiero ver las incidencias que he registrado, para tener trazabilidad de los eventos ocurridos durante mis servicios. | 2 |
| **46** | **US07** | Visualizar flota completa en el mapa | Como administrador de una empresa de movilidad escolar, quiero visualizar todos mis vehículos activos en un mapa en tiempo real, para supervisar el cumplimiento de rutas sin depender de llamadas telefónicas. | 3 |
| **47** | **US35** | Visualizar vehículos en el mapa | Como administrador de una empresa de movilidad escolar, quiero ver todos mis vehículos en un mapa en tiempo real, para monitorear su ubicación. | 3 |
| **48** | **US40** | Visualizar recorrido en tiempo real | Como administrador de una empresa de movilidad escolar, quiero ver el recorrido que realiza cada vehículo, para validar el cumplimiento de la ruta. | 3 |
| **49** | **US41** | Historial reciente de ubicaciones | Como administrador de una empresa de movilidad escolar, quiero consultar las ubicaciones recientes de un vehículo, para analizar su comportamiento. | 2 |
| **50** | **US42** | Actualización automática de datos | Como administrador de una empresa de movilidad escolar, quiero que la información se actualice automáticamente, para no tener que recargarla manualmente. | 3 |
| **51** | **US46** | Filtrar reportes | Como administrador de una empresa de movilidad escolar, quiero aplicar filtros a los reportes, para enfocarme en información específica. | 2 |
| **52** | **US47** | Incluir incidencias en los reportes | Como administrador de una empresa de movilidad escolar, quiero incluir las incidencias en los reportes, para tener un contexto completo del servicio. | 2 |
| **53** | **US48** | Resumen general | Como administrador de una empresa de movilidad escolar, quiero ver un resumen general de desempeño, para tomar decisiones rápidas. | 3 |
| **54** | **US49** | Descarga rápida de reportes recientes | Como administrador de una empresa de movilidad escolar, quiero acceder rápidamente a reportes recientes, para ahorrar tiempo en consultas frecuentes. | 2 |
| **55** | **US43** | Generar reporte de recorridos | Como administrador de una empresa de movilidad escolar, quiero generar reportes de recorridos realizados, para analizar el cumplimiento de rutas. | 3 |
| **56** | **US45** | Exportar reportes | Como administrador de una empresa de movilidad escolar, quiero exportar reportes, para compartirlos o analizarlos externamente. | 3 |
| **57** | **US10** | Exportar reporte de asistencia mensual | Como administrador de una empresa de movilidad escolar, quiero exportar un reporte consolidado de asistencia mensual por estudiante, para agilizar el proceso de facturación a los padres sin errores manuales. | 5 |
| **58** | **US11** | Generar reporte de puntualidad por unidad | Como administrador de una empresa de movilidad escolar, quiero generar un reporte de puntualidad por conductor/unidad, para evaluar su desempeño y tomar decisiones de mejora o incentivos. | 5 |
| **59** | **US44** | Generar reporte de desempeño | Como administrador de una empresa de movilidad escolar, quiero visualizar métricas de desempeño de conductores y vehículos, para evaluar la eficiencia operativa. | 5 |
| **60** | **US54** | Recibir notificación de proximidad | Como padre de familia, quiero recibir una notificación automática cuando el vehículo escolar esté cerca de mi casa, para bajar a la puerta a tiempo sin esperar en la calle. | 3 |
| **61** | **US55** | Visualizar ubicación en tiempo real de mi hijo | Como padre de familia, quiero ver en un mapa la ubicación en tiempo real del vehículo escolar, para tener tranquilidad durante el trayecto de mi hijo. | 3 |
| **62** | **US56** | Recibir confirmación de llegada al colegio | Como padre de familia, quiero recibir una notificación cuando mi hijo llegue al colegio, para confirmar que arribó sano y salvo a su destino. | 2 |
| **63** | **US02** | Notificación automática de ausencia | Como conductor, quiero que el sistema detecte automáticamente cuando un estudiante no se presenta en su parada, para no tener que esperar más de lo necesario ni llamar manualmente al padre. | 3 |
| **64** | **US57** | Recibir notificación de ausencia del estudiante | Como padre de familia, quiero recibir una notificación cuando mi hijo no aborde el vehículo en su parada, para saber que no fue recogido y actuar en consecuencia. | 2 |
| **65** | **US08** | Recibir alerta por desviación de ruta | Como administrador de una empresa de movilidad escolar, quiero recibir una alerta cuando un vehículo se desvía significativamente de su ruta establecida, para actuar rápidamente ante posibles incidentes. | 3 |
| **66** | **US39** | Alertas de desviación | Como administrador de una empresa de movilidad escolar, quiero recibir alertas cuando un vehículo se desvía de su ruta, para actuar oportunamente. | 3 |
| **67** | **US06** | Notificar a los padres por incidencia | Como sistema, quiero notificar automáticamente a los padres cuando se registra una incidencia que afecta la ruta de sus hijos, para mantenerlos informados sin intervención manual del conductor. | 3 |
| **68** | **US58** | Recibir notificación de incidencia que afecta a mi hijo | Como padre de familia, quiero recibir una notificación cuando ocurra una incidencia que afecte la ruta de mi hijo, para estar informado sin tener que llamar al conductor. | 3 |
| **69** | **US31** | Registro automático de hora y ubicación | Como conductor, quiero que el sistema registre automáticamente la hora y la ubicación, para no tener que hacerlo manualmente. | 2 |
| **70** | **US17** | Funcionalidad sin conexión | Como conductor, quiero poder registrar abordajes sin conexión a internet, para no depender de la señal. | 5 |
| **71** | **US25** | Funcionalidad de ruta sin conexión | Como conductor, quiero acceder a mi ruta sin conexión a internet, para no depender de la señal. | 5 |
| **72** | **US34** | Funcionalidad de incidencias sin conexión | Como conductor, quiero registrar incidencias sin conexión, para no depender de la red. | 5 |
| **73** | **US65** | Endpoint de autenticación y emisión de tokens JWT | Como developer, quiero disponer de un endpoint POST `/api/v1/authentication/sign-in`, para validar credenciales y emitir tokens de sesión estructurados. | 3 |
| **74** | **US66** | Endpoint para registro de asistencia en un solo toque | Como developer, quiero disponer de un endpoint PUT `/api/v1/attendance-records/{id}`, para actualizar el estado de abordaje y persistir marcas temporales. | 3 |
| **75** | **US67** | Endpoint para telemetría y geocercas en tiempo real | Como developer, quiero un endpoint POST `/api/v1/trips/{id}/location`, para recibir coordenadas GPS periódicas y disparar alertas de proximidad automáticas. | 5 |