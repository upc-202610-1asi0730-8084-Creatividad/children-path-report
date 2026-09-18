# **Chapter III: Requirements Specification**
## **3.1. User Stories** 

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
    </tbody>
</table>


## **3.2. Impact Mapping**

<img alt="Impact map 60" src="assets/chapter-3/impact-mapping-UXPRESSIA.png" />

[Ver artefacto en uxpressia](https://uxpressia.com/w/v8FzI/i/Fy0pk?tagId=EaWxj)

## **3.3. Product Backlog**

| Orden | ID de Historia de Usuario | Título | Descripción | Puntos de Historia |
|-------|---------------------------|--------|-------------|--------------------|
| 1 | US01 | Registrar abordaje del estudiante | Como conductor, quiero registrar el momento en que un estudiante aborda el vehículo en cada parada, para mantener un registro digital de asistencia. | 3 |
| 2 | US02 | Notificación automática de ausencia | Como conductor, quiero que el sistema detecte automáticamente cuando un estudiante no se presenta en su parada, para no tener que esperar más de lo necesario ni llamar manualmente al padre. | 3 |
| 3 | US14 | Registrar abordaje | Como conductor, quiero marcar rápidamente cuándo un estudiante sube al vehículo, para llevar el control del viaje. | 2 |
| 4 | US15 | Registrar ausencia | Como conductor, quiero marcar cuándo un estudiante no sube al vehículo, para evitar esperas innecesarias. | 2 |
| 5 | US12 | Visualizar lista de estudiantes por ruta | Como conductor, quiero ver la lista de estudiantes asignados a mi ruta, para saber a quiénes debo recoger. | 2 |
| 6 | US13 | Visualizar estudiantes por parada | Como conductor, quiero ver qué estudiantes corresponden a cada parada, para organizar el recojo. | 2 |
| 7 | US18 | Confirmación visual rápida | Como conductor, quiero identificar rápidamente quién ya subió y quién no, para tomar decisiones rápidas. | 1 |
| 8 | US16 | Edición rápida de estado | Como conductor, quiero corregir el estado de un estudiante en caso de error, para mantener la información precisa. | 2 |
| 9 | US17 | Funcionalidad sin conexión | Como conductor, quiero poder registrar abordajes sin conexión a internet, para no depender de la señal. | 5 |
| 10 | US03 | Visualizar ruta diaria optimizada | Como conductor, quiero visualizar la ruta del día con el orden de las paradas y los tiempos estimados, para reducir los tiempos de espera y el consumo de combustible. | 3 |
| 11 | US19 | Visualizar ruta asignada | Como conductor, quiero visualizar la ruta asignada del día, para conocer el orden del recorrido. | 2 |
| 12 | US20 | Visualizar paradas en el mapa | Como conductor, quiero ver las paradas de mi ruta en un mapa, para ubicarme fácilmente durante el recorrido. | 3 |
| 13 | US21 | Navegación entre paradas | Como conductor, quiero recibir indicaciones para llegar a cada parada, para optimizar mi recorrido. | 3 |
| 14 | US22 | Marcar parada como completada | Como conductor, quiero marcar una parada como completada, para avanzar en mi ruta de manera ordenada. | 1 |
| 15 | US24 | Visualizar estado de la ruta | Como conductor, quiero ver el progreso de mi ruta, para saber cuánto falta por completar. | 2 |
| 16 | US04 | Reordenar ruta por ausencia | Como conductor, quiero que la ruta se reordene automáticamente cuando un estudiante está ausente, para no perder tiempo pasando por una parada vacía. | 3 |
| 17 | US23 | Reordenamiento básico de ruta | Como conductor, quiero ajustar el orden de las paradas en caso de imprevistos, para adaptarme a cambios en el recorrido. | 3 |
| 18 | US25 | Funcionalidad de ruta sin conexión | Como conductor, quiero acceder a mi ruta sin conexión a internet, para no depender de la señal. | 5 |
| 19 | US05 | Registrar incidencia en la ruta | Como conductor, quiero registrar cualquier incidencia que ocurra durante el viaje (retraso, accidente, cambio de ruta), para mantener la trazabilidad del servicio. | 3 |
| 20 | US26 | Registro rápido de incidencia | Como conductor, quiero registrar una incidencia en pocos pasos, para no distraerme durante el recorrido. | 2 |
| 21 | US28 | Seleccionar tipo de incidencia | Como conductor, quiero elegir el tipo de incidencia, para clasificar correctamente el evento. | 2 |
| 22 | US29 | Registrar detalle opcional | Como conductor, quiero agregar un comentario opcional, para proporcionar más contexto si es necesario. | 1 |
| 23 | US30 | Asociar incidencia con parada o estudiante | Como conductor, quiero vincular la incidencia a una parada o estudiante, para mayor precisión en el registro. | 2 |
| 24 | US31 | Registro automático de hora y ubicación | Como conductor, quiero que el sistema registre automáticamente la hora y la ubicación, para no tener que hacerlo manualmente. | 2 |
| 25 | US32 | Visualizar historial de incidencias | Como conductor, quiero ver las incidencias registradas, para hacer seguimiento del recorrido. | 2 |
| 26 | US33 | Editar o corregir incidencia | Como conductor, quiero corregir una incidencia en caso de error, para mantener la información precisa. | 2 |
| 27 | US34 | Funcionalidad de incidencias sin conexión | Como conductor, quiero registrar incidencias sin conexión, para no depender de la red. | 5 |
| 28 | US06 | Notificar a los padres por incidencia | Como sistema, quiero notificar automáticamente a los padres cuando se registra una incidencia que afecta la ruta de sus hijos, para mantenerlos informados sin intervención manual del conductor. | 3 |
| 29 | US07 | Visualizar flota completa en el mapa | Como administrador de una empresa de movilidad escolar, quiero visualizar todos mis vehículos activos en un mapa en tiempo real, para supervisar el cumplimiento de rutas sin depender de llamadas telefónicas. | 3 |
| 30 | US35 | Visualizar vehículos en el mapa | Como administrador de una empresa de movilidad escolar, quiero ver todos mis vehículos en un mapa en tiempo real, para monitorear su ubicación. | 3 |
| 31 | US36 | Visualizar detalles del vehículo | Como administrador de una empresa de movilidad escolar, quiero seleccionar un vehículo y ver su información, para conocer su estado actual. | 2 |
| 32 | US37 | Visualizar estados de los vehículos | Como administrador de una empresa de movilidad escolar, quiero identificar el estado de cada vehículo, para detectar problemas rápidamente. | 2 |
| 33 | US38 | Filtrar unidades | Como administrador de una empresa de movilidad escolar, quiero filtrar vehículos por estado o ruta, para enfocarme en lo relevante. | 2 |
| 34 | US39 | Alertas de desviación | Como administrador de una empresa de movilidad escolar, quiero recibir alertas cuando un vehículo se desvía de su ruta, para actuar oportunamente. | 3 |
| 35 | US08 | Recibir alerta por desviación de ruta | Como administrador de una empresa de movilidad escolar, quiero recibir una alerta cuando un vehículo se desvía significativamente de su ruta establecida, para actuar rápidamente ante posibles incidentes. | 3 |
| 36 | US40 | Visualizar recorrido en tiempo real | Como administrador de una empresa de movilidad escolar, quiero ver el recorrido que realiza cada vehículo, para validar el cumplimiento de la ruta. | 3 |
| 37 | US41 | Historial reciente de ubicaciones | Como administrador de una empresa de movilidad escolar, quiero consultar las ubicaciones recientes de un vehículo, para analizar su comportamiento. | 2 |
| 38 | US42 | Actualización automática de datos | Como administrador de una empresa de movilidad escolar, quiero que la información se actualice automáticamente, para no tener que recargarla manualmente. | 3 |
| 39 | US09 | Visualizar historial personal de viajes | Como conductor independiente, quiero acceder a mi historial de viajes, puntualidad e incidencias registradas, para evaluar mi desempeño y demostrar mi confiabilidad a los padres. | 3 |
| 40 | US50 | Visualizar resumen personal de viajes | Como conductor independiente, quiero ver un resumen de mis viajes completados, para hacer seguimiento de mi actividad diaria. | 2 |
| 41 | US51 | Visualizar métricas personales de puntualidad | Como conductor independiente, quiero ver mis métricas de puntualidad, para evaluar mi desempeño y mejorar mi reputación. | 3 |
| 42 | US52 | Exportar historial personal de viajes | Como conductor independiente, quiero exportar mi historial de viajes, para compartirlo con padres o empresas que soliciten referencias. | 3 |
| 43 | US53 | Visualizar historial personal de incidencias | Como conductor independiente, quiero ver las incidencias que he registrado, para tener trazabilidad de los eventos ocurridos durante mis servicios. | 2 |
| 44 | US10 | Exportar reporte de asistencia mensual | Como administrador de una empresa de movilidad escolar, quiero exportar un reporte consolidado de asistencia mensual por estudiante, para agilizar el proceso de facturación a los padres sin errores manuales. | 5 |
| 45 | US11 | Generar reporte de puntualidad por unidad | Como administrador de una empresa de movilidad escolar, quiero generar un reporte de puntualidad por conductor/unidad, para evaluar su desempeño y tomar decisiones de mejora o incentivos. | 5 |
| 46 | US43 | Generar reporte de recorridos | Como administrador de una empresa de movilidad escolar, quiero generar reportes de recorridos realizados, para analizar el cumplimiento de rutas. | 3 |
| 47 | US44 | Generar reporte de desempeño | Como administrador de una empresa de movilidad escolar, quiero visualizar métricas de desempeño de conductores y vehículos, para evaluar la eficiencia operativa. | 5 |
| 48 | US45 | Exportar reportes | Como administrador de una empresa de movilidad escolar, quiero exportar reportes, para compartirlos o analizarlos externamente. | 3 |
| 49 | US46 | Filtrar reportes | Como administrador de una empresa de movilidad escolar, quiero aplicar filtros a los reportes, para enfocarme en información específica. | 2 |
| 50 | US47 | Incluir incidencias en los reportes | Como administrador de una empresa de movilidad escolar, quiero incluir las incidencias en los reportes, para tener un contexto completo del servicio. | 2 |
| 51 | US48 | Resumen general | Como administrador de una empresa de movilidad escolar, quiero ver un resumen general de desempeño, para tomar decisiones rápidas. | 3 |
| 52 | US49 | Descarga rápida de reportes recientes | Como administrador de una empresa de movilidad escolar, quiero acceder rápidamente a reportes recientes, para ahorrar tiempo en consultas frecuentes. | 2 |
| 53 | US54 | Recibir notificación de proximidad | Como padre de familia, quiero recibir una notificación automática cuando el vehículo escolar esté cerca de mi casa, para bajar a la puerta a tiempo sin esperar en la calle. | 3 |
| 54 | US55 | Visualizar ubicación en tiempo real de mi hijo | Como padre de familia, quiero ver en un mapa la ubicación en tiempo real del vehículo escolar, para tener tranquilidad durante el trayecto de mi hijo. | 3 |
| 55 | US56 | Recibir confirmación de llegada al colegio | Como padre de familia, quiero recibir una notificación cuando mi hijo llegue al colegio, para confirmar que arribó sano y salvo a su destino. | 2 |
| 56 | US57 | Recibir notificación de ausencia del estudiante | Como padre de familia, quiero recibir una notificación cuando mi hijo no aborde el vehículo en su parada, para saber que no fue recogido y actuar en consecuencia. | 2 |
| 57 | US58 | Recibir notificación de incidencia que afecta a mi hijo | Como padre de familia, quiero recibir una notificación cuando ocurra una incidencia que afecte la ruta de mi hijo, para estar informado sin tener que llamar al conductor. | 3 |
