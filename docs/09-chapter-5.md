# **Capítulo V: Implementación, Validación y Despliegue del Producto**

## **5.1. Gestión de la Configuración del Software**

Esta sección describe las herramientas, configuraciones y convenciones adoptadas por el equipo para garantizar la consistencia, calidad y trazabilidad a lo largo del ciclo de vida del producto **Children Path**.

La implementación de prácticas de gestión de la configuración permitió una colaboración efectiva, un control de versiones adecuado y un proceso de desarrollo estructurado, asegurando que todos los componentes de la solución estuvieran alineados y fueran mantenibles.

### **5.1.1. Configuración del Entorno de Desarrollo de Software**

Para apoyar el desarrollo del proyecto, el equipo utilizó un conjunto de herramientas que cubren todas las etapas del ciclo de vida del software:

- **GitHub:** utilizado como plataforma principal para el control de versiones y la colaboración del equipo.
- **Visual Studio Code:** entorno de desarrollo principal para la landing page.
- **Figma:** utilizado para el diseño UI/UX y la creación de prototipos.
- **Structurizer:** utilizado para el modelado C4.
- **Miro:** utilizado para la creación de diagramas de flujo y mapas conceptuales.
- **UXXPRESSIA** utilizado para la creación de mapas de experiencia del usuario y customer journey maps.

Estas herramientas permitieron una integración eficiente entre los procesos de diseño, desarrollo, pruebas y validación.

### **5.1.2. Gestión del Código Fuente**

El proyecto utiliza **GitHub** como sistema de control de versiones. Se crearon repositorios separados para cada componente principal de la solución:

- Landing Page

El equipo adoptó el modelo de ramificación **GitFlow** para gestionar el desarrollo de manera eficiente:

- **main:** contiene la versión estable de producción.
- **develop:** integra el trabajo de desarrollo en curso.
- **feature/*:** ramas para nuevas funcionalidades.

Convenciones de nomenclatura:

- `feature/add-section-1-1`
- `feature/add-chapter-3`
- `release/v0.1.0`
- `fix/remodalate-impact-mapping`
- `hotfix/cover-fix`

Además, el equipo aplicó **Versionado Semántico (SemVer)**:

- `v1.0.0` → versión estable inicial
- `v0.1.0` → nuevas funcionalidades agregadas
- `v0.1.1` → corrección de errores

Los mensajes de commit siguen el estándar **Conventional Commits**. Este enfoque garantiza un historial de desarrollo claro y trazable.

### **5.1.3. Guía de Estilo y Convenciones de Código Fuente**

Para garantizar la calidad y mantenibilidad del código, el equipo adoptó convenciones estándar de codificación:

- Todos los elementos del código (variables, funciones, clases) se escriben en inglés.
- **camelCase** para variables y funciones.
- Estructura de código modular para una mejor organización.

Se consideraron las siguientes guías de estilo:

- Google HTML/CSS Style Guide
- Buenas prácticas de JavaScript/TypeScript
- Principios de Clean Code

Las Historias de Usuario y los Criterios de Aceptación se redactaron utilizando un formato estructurado basado en **Gherkin** para mejorar la claridad y legibilidad.

### **5.1.4. Configuración de Despliegue del Software**

El proceso de despliegue para cada componente del sistema se define de la siguiente manera:

**Landing Page**
- Abrir el archivo HTML principal o desplegarlo en un servicio de hosting.
- Validar la capacidad responsive en diferentes dispositivos.

Esta configuración permite que cualquier miembro del equipo ejecute y despliegue el sistema de forma consistente.

## **5.2. Implementación de la Landing Page, Servicios y Aplicaciones**

### **5.2.1. Sprint 1**

#### **5.2.1.1. Sprint Planning 1**

Durante el Sprint 1, el equipo planificó, diseñó, implementó y desplegó el sitio web estático público (Landing Page) de **Children Path**. El objetivo primordial consistió en materializar la presencia digital de la plataforma mediante un portal web responsive y estructurado que comunicara la propuesta de valor, los beneficios diferenciados por actor clave, los módulos de seguridad vehicular, testimonios de validación social y canales interactivos de contacto directo.

| Sprint # | Sprint 1 |
| :--- | :--- |
| **Sprint Planning Background** | Implementación, maquetación responsive y despliegue continuo de la Landing Page |
| **Date** | 2026-09-06 |
| **Time** | 07:00 PM |
| **Location** | Reunión virtual vía Google Meet |
| **Prepared By** | Huaco Oliva, Luis Alonso |
| **Attendees (to planning meeting)** | Huaco Oliva, Luis Alonso / Pareja Cáceres, Diana / Soto, Brandon / Rázuri, Piero |
| **Sprint n – 1 Review Summary** | No aplica. Sprint inicial del ciclo del producto. |
| **Sprint n – 1 Retrospective Summary** | No aplica. Sprint inicial del ciclo del producto. |
**Sprint Goal & User Stories**

| Sprint Goal | Description |
| ------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Sprint 1 Goal** | Nuestro enfoque está en diseñar una Landing Page clara y estructurada. Creemos que esto permitirá que los usuarios potenciales comprendan el valor del producto. Esto se confirmará cuando los usuarios puedan identificar el problema y la solución en la primera interacción. |
| **Sprint 1 Velocity** | 14 Story Points |
| **Sum of Story Points** | 14 Story Points |

#### **5.2.1.2. Aspect Leaders and Collaborators**

Durante este Sprint, el equipo trabajó en el diseño de la Landing Page, la estructura UX y la creación de contenido.

| Team Member | GitHub Username | UI/UX Wireframing & Design | HTML/CSS Component Layout | JavaScript Interactivity (FAQ & CTA) | Deployment & Cross-Browser QA |
| :--- | :--- | :---: | :---: | :---: | :---: |
| Huaco, Luis | perghormaru-pixel | L | C | L | C |
| Pareja, Diana | DianaParejaCaceres | C | L | C | L |
| Soto, Brandon | Brandon1677 | C | C | L | C |
| Rázuri, Piero | piero-razuri | L | C | C | C |

**Leyenda:** L = Leader (Líder) | C = Collaborator (Colaborador)

#### **5.2.1.3. Sprint Backlog 1**

El Sprint Backlog se enfocó en definir la estructura y el diseño inicial de la Landing Page.

<table width="100%">
  <thead>
    <tr>
      <th colspan="2" style="text-align:center">User Story</th>
      <th colspan="6" style="text-align:center">Work-Item / Task</th>
    </tr>
    <tr>
      <th style="width: 8%; text-align:center">Story Id</th>
      <th style="width: 20%; text-align:center">Story Title</th>
      <th style="width: 9%; text-align:center">Task Id</th>
      <th style="width: 20%; text-align:center">Task Title</th>
      <th style="width: 25%; text-align:center">Task Description</th>
      <th style="width: 6%; text-align:center">Estimation (Hours)</th>
      <th style="width: 12%; text-align:center">Assigned To</th>
      <th style="width: 8%; text-align:center">Status</th>
    </tr>
  </thead>
  <tbody>
    <!-- US59 -->
    <tr>
      <td rowspan="2" align="center" style="font-weight:bold; vertical-align:middle">US59</td>
      <td rowspan="2" style="vertical-align:middle">Visualizar Hero section, métricas y pitch principal</td>
      <td align="center">TS1-01</td>
      <td>Diseño UI y Maquetación de Navbar, Hero y Métricas</td>
      <td>Diseñar y codificar el encabezado institucional, banner con simulación de ruta en vivo y la barra de métricas (Trust in every journey).</td>
      <td align="center">7</td>
      <td>Diana Pareja</td>
      <td align="center">Done</td>
    </tr>
    <tr>
      <td align="center">TS1-02</td>
      <td>Implementación de Botones CTA y Redirección Login</td>
      <td>Configurar botones "Request a demo", "View plans" y enlace de acceso al aplicativo en JavaScript.</td>
      <td align="center">5</td>
      <td>Brandon Soto</td>
      <td align="center">Done</td>
    </tr>
    <!-- US60 -->
    <tr>
      <td rowspan="2" align="center" style="font-weight:bold; vertical-align:middle">US60</td>
      <td rowspan="2" style="vertical-align:middle">Explorar beneficios segmentados por rol de usuario</td>
      <td align="center">TS1-03</td>
      <td>Maquetación de Tarjetas de Beneficios por Stakeholder</td>
      <td>Estructurar la cuadrícula CSS para las tres tarjetas diferenciadas: Families, Drivers y Companies & Schools con listas de verificación.</td>
      <td align="center">6</td>
      <td>Luis Huaco</td>
      <td align="center">Done</td>
    </tr>
    <tr>
      <td align="center">TS1-04</td>
      <td>Adaptabilidad Responsive de Beneficios (Mobile/Tablet)</td>
      <td>Configurar Media Queries para colapsar las tres columnas en layout apilado fluido en resoluciones de 360px a 768px.</td>
      <td align="center">5</td>
      <td>Diana Pareja</td>
      <td align="center">Done</td>
    </tr>
    <!-- US61 -->
    <tr>
      <td rowspan="2" align="center" style="font-weight:bold; vertical-align:middle">US61</td>
      <td rowspan="2" style="vertical-align:middle">Consultar módulos de funcionamiento y seguridad de la plataforma</td>
      <td align="center">TS1-05</td>
      <td>Maquetación de la Sección "How ChildrenPath Works"</td>
      <td>Codificar el contenedor de 6 tarjetas: Alerts, Digital Assistance, Safe Routes, Fleet Monitoring, Integration y Privacy.</td>
      <td align="center">6</td>
      <td>Piero Rázuri</td>
      <td align="center">Done</td>
    </tr>
    <tr>
      <td align="center">TS1-06</td>
      <td>Optimización de Iconografía SVG y Tipografía</td>
      <td>Estandarizar iconos vectoriales, paleta de colores corporativos y pesos de fuente para garantizar contraste accesible.</td>
      <td align="center">4</td>
      <td>Diana Pareja</td>
      <td align="center">Done</td>
    </tr>
    <!-- US62 -->
    <tr>
      <td rowspan="2" align="center" style="font-weight:bold; vertical-align:middle">US62</td>
      <td rowspan="2" style="vertical-align:middle">Consultar planes de suscripción y tarifas comerciales</td>
      <td align="center">TS1-07</td>
      <td>Maquetación de la Tarjeta Comparativa de Planes</td>
      <td>Codificar las tarjetas de precios para Independent Driver, Company y School destacando el plan institucional.</td>
      <td align="center">6</td>
      <td>Brandon Soto</td>
      <td align="center">Done</td>
    </tr>
    <tr>
      <td align="center">TS1-08</td>
      <td>Configuración de Enlaces y Smooth Scrolling a Contacto</td>
      <td>Vincular botones de contratación y solicitud de demo hacia el formulario de contacto mediante desplazamiento suave.</td>
      <td align="center">4</td>
      <td>Luis Huaco</td>
      <td align="center">Done</td>
    </tr>
    <!-- US63 -->
    <tr>
      <td rowspan="2" align="center" style="font-weight:bold; vertical-align:middle">US63</td>
      <td rowspan="2" style="vertical-align:middle">Revisar testimonios reales y preguntas frecuentes (FAQ)</td>
      <td align="center">TS1-09</td>
      <td>Maquetación de Testimonios (Social Proof)</td>
      <td>Crear tarjetas con citas y perfiles de apoderados, conductores y directivos de centros educativos en Lima.</td>
      <td align="center">5</td>
      <td>Piero Rázuri</td>
      <td align="center">Done</td>
    </tr>
    <tr>
      <td align="center">TS1-10</td>
      <td>Lógica de Acordeón Interactivo para FAQ en JS</td>
      <td>Programar interactividad de apertura y cierre animado de preguntas frecuentes sobre cobertura, flotas y soporte.</td>
      <td align="center">6</td>
      <td>Brandon Soto</td>
      <td align="center">Done</td>
    </tr>
    <!-- US64 -->
    <tr>
      <td rowspan="2" align="center" style="font-weight:bold; vertical-align:middle">US64</td>
      <td rowspan="2" style="vertical-align:middle">Solicitar demostración comercial y acceder a canales de contacto</td>
      <td align="center">TS1-11</td>
      <td>Maquetación de Bloque de Contacto y Canales Directos</td>
      <td>Codificar tarjeta de contacto con teléfono, correo hola@childrenpath.com, WhatsApp oficial y horario de atención.</td>
      <td align="center">5</td>
      <td>Luis Huaco</td>
      <td align="center">Done</td>
    </tr>
    <tr>
      <td align="center">TS1-12</td>
      <td>Implementación de Footer, Redes y Despliegue en GitHub Pages</td>
      <td>Estructurar pie de página con enlaces legales, redes sociales y configurar pipeline de publicación en GitHub Pages.</td>
      <td align="center">5</td>
      <td>Brandon Soto</td>
      <td align="center">Done</td>
    </tr>
  </tbody>
</table>

#### **5.2.1.4. Development Evidence for Sprint Review**

Durante este Sprint, el equipo completó el diseño conceptual de la Landing Page.

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Commited on (Date) |
| :--- | :--- | :---: | :--- | :--- | :---: |
| children-path-landing-page | `main` | `3cc3693` | Merge pull request #6 from upc-2.../develop | Synced accessibility styles and responsive improvements into production branch. | 2026-10-05 |
| children-path-landing-page | `develop` | `c84b74b` | Merge pull request #5 from .../feature/accessibility-styling | Integrated WCAG accessibility layers and typographic optimizations into develop. | 2026-10-05 |
| children-path-landing-page | `feature/accessibility-styling` | `6e06ef3` | style: enhance accessibility focus states and typographic rendering | Added WCAG focus-visible indicators, cross-browser font smoothing, and prefers-reduced-motion media query in styles.css. | 2026-10-05 |
| children-path-landing-page | `main` | `d17ed10` | Merge pull request #4 from upc-2.../develop | Merged brand logo style corrections and asset link updates into main. | 2026-10-05 |
| children-path-landing-page | `develop` | `1c024bd` | Feat: add new brand logo and style | Consolidated core branding updates, visual style guides, and typography definitions across views. | 2026-10-05 |
| children-path-landing-page | `feature/views-markup` | `3eb7039` | Fix: brand logo problems fixed | Resolved SVG logo path references and dimensions across all HTML view templates. | 2026-10-05 |
| children-path-landing-page | `main` | `02fb93f` | Merge pull request #3 from upc-2.../develop | Merged auth redirection script and About section content fixes. | 2026-10-05 |
| children-path-landing-page | `feature/auth-redirect` | `f23619e` | Feat: add the redirect link of login | Added JavaScript event listeners linking header CTA buttons to the web application sign-in entry point. | 2026-10-05 |
| children-path-landing-page | `feature/views-markup` | `986be3a` | Fix: Changes on about us section | Updated mission, vision, and team card descriptions in about.html. | 2026-10-05 |
| children-path-landing-page | `main` | `db7be07` | Merge pull request #2 from upc-2.../develop | Merged asset integration and internationalization dictionary updates. | 2026-10-05 |
| children-path-landing-page | `develop` | `8d1befd` | Feat: add landing page imagery assets | Imported optimized vector icons and graphic banners for stakeholder and hero sections. | 2026-10-05 |
| children-path-landing-page | `feature/i18n` | `fe4cf99` | Feat: Update i18n.js | Configured internationalization language dictionary and dynamic string binding logic. | 2026-10-05 |
| children-path-landing-page | `feature/styles` | `22a2f66` | Feat: Update styles.css content | Configured base typography, color variables, layout grids, and card styling. | 2026-10-05 |
| children-path-landing-page | `feature/views-markup` | `5cbfa23` | Feat: add terms.html file content | Implemented markup and legal policy containers in terms.html. | 2026-10-05 |
| children-path-landing-page | `feature/views-markup` | `cacc083` | Feat: add contact.html file content | Maquetted contact form container and commercial communication channels in contact.html. | 2026-10-05 |
| children-path-landing-page | `feature/views-markup` | `64bde1f` | Feat: add about.html file content | Added structured sections for company vision, benefits, and team cards in about.html. | 2026-10-05 |
| children-path-landing-page | `feature/views-markup` | `65bb15e` | Feat: add index.html file content | Structured primary layout, hero section, stakeholder benefits, and pricing cards in index.html. | 2026-10-05 |
| children-path-landing-page | `feature/scripts` | `3577fd3` | Feat: add main interactive JS for UI behaviors | Programmed FAQ collapsible accordion and smooth scrolling behavior for action buttons. | 2026-10-05 |
| children-path-landing-page | `develop` | `923fcab` | Chore: Initial commits | Initialized Git repository structure and root directories. | 2026-10-05 |

#### **5.2.1.5. Execution Evidence for Sprint Review**

Durante este Sprint, el equipo validó la estructura y claridad de la Landing Page.

| Evidence Type | Description |
| --------------- | -------------------------------------------------------------------------------------------------- |
| Wireframes | Diseño de baja fidelidad que muestra el layout |
| UX validation | Flujo lógico entre secciones |
| Internal review | Retroalimentación de los miembros del equipo |


##### Vistas y Secciones Implementadas:

* **Figura 5.1:** *Hero Section, Simulación de Ruta y Métricas de Confianza (`index.html`).*  
  Encabezado principal con propuesta de valor, navegación institucional, llamado a la acción para solicitud de demostración y widget interactivo de monitoreo de ruta en vivo.  
  ![Hero Section Children Path](https://raw.githubusercontent.com/upc-202610-1asi0730-8084-Creatividad/children-path-report/develop/assets/landing-hero.png)

* **Figura 5.2:** *Beneficios Segmentados para Stakeholders y Módulos de Operación ("How ChildrenPath Works").*  
  Cuadrícula con listas de verificación para Familias, Conductores y Colegios, complementada con los módulos de alertas inmediatas, asistencia digital y trazabilidad segura.  
  ![Beneficios por Stakeholder](https://raw.githubusercontent.com/upc-202610-1asi0730-8084-Creatividad/children-path-report/develop/assets/landing-benefits.png)

* **Figura 5.3:** *Planes de Suscripción Comerciales y Preguntas Frecuentes (FAQ).*  
  Estructura tarifaria comercial diferenciada para Independent Driver, Company y School, junto con el acordeón interactivo de dudas frecuentes implementado en JavaScript.  
  ![Planes y FAQ Children Path](https://raw.githubusercontent.com/upc-202610-1asi0730-8084-Creatividad/children-path-report/develop/assets/landing-plans-faq.png)

* **Figura 5.4:** *Canales de Contacto Directo ("Contact Us") y Pie de Página Institucional.*  
  Tarjeta de contacto con teléfono corporativo, correo de soporte, canal oficial de WhatsApp y pie de página con navegación legal y enlaces institucionales.  
  ![Contacto y Footer Children Path](https://raw.githubusercontent.com/upc-202610-1asi0730-8084-Creatividad/children-path-report/develop/assets/landing-contact-footer.png)

#### **5.2.1.6. Services Documentation Evidence for Sprint Review**

| Status |
| ------------------------------------------------------------------------ |
| No aplica. No se implementaron servicios RESTful durante este Sprint. |

#### **5.2.1.7. Software Deployment Evidence for Sprint Review**

A continuación, se detalla la evidencia del despliegue en producción del sitio web público de captación:

| Plataforma de Despliegue | Entorno | URL Pública del Despliegue | Evidencia de Operación |
| :--- | :---: | :--- | :--- |
| GitHub Pages | Producción | [https://upc-202610-1asi0730-8084-creatividad.github.io/children-path-landing-page/](https://upc-202610-1asi0730-8084-creatividad.github.io/children-path-landing-page/) | Sitio web estático desplegado de forma automatizada mediante pipeline de GitHub Actions, con certificado SSL/TLS activo y disponibilidad pública continua. |

#### **5.2.1.8. Team Collaboration Insights during Sprint**

| Insight |
| ----------------------------------------------------------------------- |
| El equipo alineó exitosamente la investigación con las decisiones de diseño. |
| Herramientas colaborativas como Figma mejoraron la visibilidad del flujo de trabajo. |
| La definición temprana de la propuesta de valor redujo retrabajos futuros. |
| La distribución de tareas entre los miembros mejoró la eficiencia y la responsabilidad. |


### **5.2.2. Sprint 2**

#### **5.2.2.1. Sprint Planning 2**

Durante el Sprint 2, el equipo planificó, diseñó e implementó la primera versión del aplicativo web frontend (**Frontend Web Application**) de **Children Path** en el repositorio `children-path-frontend`. Siguiendo el enfoque pedagógico y técnico del curso, el desarrollo se concentró estrictamente en la capa de presentación (Frontend UI) mediante una arquitectura modular en **Vue 3 y Vite**, prescindiendo de lógica de negocio transaccional compleja de backend. 

El alcance del incremento comprende el diseño de interfaces de usuario interactivas, formularios reactivos de captura de datos, vistas de catálogos tabulares y operaciones fundamentales de lectura, registro, actualización y eliminación (**CRUD**) conectadas a un servicio de datos simulado (Fake API con `json-server`). Los módulos implementados corresponden a los Bounded Contexts centrales de la operación: gestión de estudiantes, control de abordaje en paradas, administración de unidades vehiculares y conductores, visualización de secuencias de ruta y registro estructurado de incidencias.

| Sprint # | Sprint 2 |
| :--- | :--- |
| **Sprint Planning Background** | Implementación de la interfaz de usuario del Frontend Web Application (Vue 3/Vite), vistas CRUD de entidades operativas y consumo de Fake API |
| **Date** | 2026-09-21 |
| **Time** | 07:30 PM |
| **Location** | Reunión virtual vía Google Meet |
| **Prepared By** | Huaco Oliva, Luis Alonso |
| **Attendees (to planning meeting)** | Huaco Oliva, Luis Alonso / Pareja Cáceres, Diana / Soto, Brandon / Rázuri, Piero |
| **Sprint n – 1 Review Summary** | Despliegue en producción de la Landing Page en GitHub Pages cumpliendo las historias US59 a US64, optimizando accesibilidad WCAG y maquetación responsive. |
| **Sprint n – 1 Retrospective Summary** | Se acordó utilizar una arquitectura modular por Bounded Contexts dentro del directorio `src/` del proyecto en Vue 3 para permitir que cada integrante desarrolle sus componentes y formularios sin generar conflictos de merge. |

**Sprint Goal & User Stories**

| Campo | Detalle |
| :--- | :--- |
| **Sprint 2 Goal** | **Our focus is on** delivering the core Frontend Web Application using Vue 3 and Vite, implementing interactive CRUD views, data tables, and reactive forms for students, boarding attendance, fleet units, assigned routes, and route incident logs consuming a mock API (`json-server`). <br><br>**We believe it delivers** an intuitive, accessible administrative interface allowing **school transport drivers and transport fleet administrators** to manage their operational rosters, record pupil attendance states, and inspect route milestones without server-side dependencies. <br><br>**This will be confirmed when** the frontend application executes locally (`npm run dev`) and passes UI functional checks, validating that form inputs mutate the client-side state correctly and display real-time feedback across responsive viewports. |
| **Sprint 2 Velocity** | 16 Story Points |
| **Sum of Story Points** | 16 Story Points (US12: 2 SP, US13: 2 SP, US14: 2 SP, US15: 2 SP, US19: 2 SP, US24: 2 SP, US26: 2 SP, US36: 2 SP) |

#### **5.2.2.2. Aspect Leaders and Collaborators**

El equipo distribuyó las responsabilidades técnicas del desarrollo frontend asegurando la cobertura de los módulos core y la homogeneidad en los componentes de interfaz:

| Team Member | GitHub Username | Bounded Contexts Core a Cargo | UI Component Architecture & Routing | Reactive Forms & Validation | Data Table & Mock API Services |
| :--- | :--- | :--- | :---: | :---: | :---: |
| Huaco, Luis | perghormaru-pixel | `dashboard`, `routes` | L | C | L |
| Pareja, Diana | DianaParejaCaceres | `attendance`, `assignments` | C | L | C |
| Soto, Brandon | Brandon1677 | `students`, `trips` | L | C | C |
| Rázuri, Piero | piero-razuri | `drivers`, `fleet`, `incidents` | C | L | L |

*Leyenda: L = Leader (Líder) | C = Collaborator (Colaborador)*

#### **5.2.2.3. Sprint Backlog 2**

El Sprint Backlog desagrega las 8 Historias de Usuario seleccionadas del Product Backlog en tareas de ingeniería (*Engineering Tasks*) de frontend individuales, estimadas en el rango reglamentario de 4 a 8 horas cada una:

<table width="100%">
  <thead>
    <tr>
      <th colspan="2" style="text-align:center">User Story</th>
      <th colspan="6" style="text-align:center">Work-Item / Task</th>
    </tr>
    <tr>
      <th style="width: 8%; text-align:center">Story Id</th>
      <th style="width: 20%; text-align:center">Story Title</th>
      <th style="width: 9%; text-align:center">Task Id</th>
      <th style="width: 20%; text-align:center">Task Title</th>
      <th style="width: 25%; text-align:center">Task Description</th>
      <th style="width: 6%; text-align:center">Estimation (Hours)</th>
      <th style="width: 12%; text-align:center">Assigned To</th>
      <th style="width: 8%; text-align:center">Status</th>
    </tr>
  </thead>
  <tbody>
    <!-- US14: Diana Pareja (Attendance) -->
    <tr>
      <td rowspan="2" align="center" style="font-weight:bold; vertical-align:middle">US14</td>
      <td rowspan="2" style="vertical-align:middle">Registrar abordaje</td>
      <td align="center">TS2-01</td>
      <td>Componente Interactivo de Lista de Abordaje</td>
      <td>Diseñar y programar componente Vue 3 con switches y botones de un solo toque para registrar el abordaje de estudiantes por parada.</td>
      <td align="center">6</td>
      <td>Diana Pareja</td>
      <td align="center">Done</td>
    </tr>
    <tr>
      <td align="center">TS2-02</td>
      <td>Integración de Servicio Mock para Estados de Asistencia</td>
      <td>Configurar llamadas HTTP asíncronas hacia json-server para actualizar la propiedad de abordaje y reflejar la hora en la interfaz.</td>
      <td align="center">5</td>
      <td>Diana Pareja</td>
      <td align="center">Done</td>
    </tr>
    <!-- US15: Diana Pareja (Attendance & Assignments) -->
    <tr>
      <td rowspan="2" align="center" style="font-weight:bold; vertical-align:middle">US15</td>
      <td rowspan="2" style="vertical-align:middle">Registrar ausencia</td>
      <td align="center">TS2-03</td>
      <td>Modal Reactivo de Registro de Ausencia</td>
      <td>Implementar diálogo modal con selector de tipo de falta (justificada/injustificada) y campo de motivo para actualizar la vista.</td>
      <td align="center">5</td>
      <td>Diana Pareja</td>
      <td align="center">Done</td>
    </tr>
    <tr>
      <td align="center">TS2-04</td>
      <td>Tabla de Resumen de Asistencia por Unidad Escolar</td>
      <td>Maquetar vista tabular de consulta de alumnos abordados versus ausentes con filtros por fecha y unidad de movilidad.</td>
      <td align="center">6</td>
      <td>Diana Pareja</td>
      <td align="center">Done</td>
    </tr>
    <!-- US12: Brandon Soto (Students) -->
    <tr>
      <td rowspan="2" align="center" style="font-weight:bold; vertical-align:middle">US12</td>
      <td rowspan="2" style="vertical-align:middle">Visualizar lista de estudiantes por ruta</td>
      <td align="center">TS2-05</td>
      <td>Vista de Catálogo CRUD de Estudiantes (Students Context)</td>
      <td>Crear componente de tabla reactiva para listar alumnos matriculados, mostrando nombre, apoderado, grado y dirección de recojo.</td>
      <td align="center">6</td>
      <td>Brandon Soto</td>
      <td align="center">Done</td>
    </tr>
    <tr>
      <td align="center">TS2-06</td>
      <td>Formulario de Registro y Edición de Estudiante</td>
      <td>Codificar formulario con validaciones en cliente para agregar nuevo alumno y actualizar datos de contacto del tutor.</td>
      <td align="center">5</td>
      <td>Brandon Soto</td>
      <td align="center">Done</td>
    </tr>
    <!-- US13: Brandon Soto (Students & Trips) -->
    <tr>
      <td rowspan="1" align="center" style="font-weight:bold; vertical-align:middle">US13</td>
      <td rowspan="1" style="vertical-align:middle">Visualizar estudiantes por parada</td>
      <td align="center">TS2-07</td>
      <td>Componente de Agrupamiento de Alumnos por Parada</td>
      <td>Maquetar tarjetas ordenadas secuencialmente que agrupan y listan a los escolares asignados a cada punto de ascenso del vehículo.</td>
      <td align="center">6</td>
      <td>Brandon Soto</td>
      <td align="center">Done</td>
    </tr>
    <!-- US36: Piero Rázuri (Fleet & Drivers) -->
    <tr>
      <td rowspan="2" align="center" style="font-weight:bold; vertical-align:middle">US36</td>
      <td rowspan="2" style="vertical-align:middle">Visualizar detalles del vehículo</td>
      <td align="center">TS2-08</td>
      <td>Catálogo y Tabla CRUD de Unidades Vehiculares (Fleet)</td>
      <td>Implementar vista de tarjetas y tabla con placa, modelo, capacidad de asientos y estado operativo de las unidades de transporte.</td>
      <td align="center">6</td>
      <td>Piero Rázuri</td>
      <td align="center">Done</td>
    </tr>
    <tr>
      <td align="center">TS2-09</td>
      <td>Formulario de Registro de Vehículo y Asignación de Chofer</td>
      <td>Diseñar formulario de registro vehicular y vinculación con el perfil del conductor responsable en la capa cliente.</td>
      <td align="center">5</td>
      <td>Piero Rázuri</td>
      <td align="center">Done</td>
    </tr>
    <!-- US26: Piero Rázuri (Incidents) -->
    <tr>
      <td rowspan="1" align="center" style="font-weight:bold; vertical-align:middle">US26</td>
      <td rowspan="1" style="vertical-align:middle">Registro rápido de incidencia</td>
      <td align="center">TS2-10</td>
      <td>Formulario Reactivo de Incidencias en Ruta (Incidents)</td>
      <td>Codificar interfaz de dos toques con selector de categoría (tráfico, percance mecánico, retraso) y campo opcional de observaciones.</td>
      <td align="center">5</td>
      <td>Piero Rázuri</td>
      <td align="center">Done</td>
    </tr>
    <!-- US19: Luis Huaco (Routes) -->
    <tr>
      <td rowspan="2" align="center" style="font-weight:bold; vertical-align:middle">US19</td>
      <td rowspan="2" style="vertical-align:middle">Visualizar ruta asignada</td>
      <td align="center">TS2-11</td>
      <td>Vista de Secuencia de Paradas del Conductor (Routes Context)</td>
      <td>Maquetar interfaz cronológica de paradas con indicación de dirección, hora estimada de llegada y estado completado/pendiente.</td>
      <td align="center">6</td>
      <td>Luis Huaco</td>
      <td align="center">Done</td>
    </tr>
    <tr>
      <td align="center">TS2-12</td>
      <td>Formulario de Alta y Configuración de Paradas de Ruta</td>
      <td>Crear formulario para añadir nuevas paradas a un trayecto escolar y definir el orden de paso del recorrido.</td>
      <td align="center">5</td>
      <td>Luis Huaco</td>
      <td align="center">Done</td>
    </tr>
    <!-- US24: Luis Huaco (Dashboard) -->
    <tr>
      <td rowspan="1" align="center" style="font-weight:bold; vertical-align:middle">US24</td>
      <td rowspan="1" style="vertical-align:middle">Visualizar estado de la ruta</td>
      <td align="center">TS2-13</td>
      <td>Dashboard de Control y Resumen de Estado Operativo</td>
      <td>Integrar panel principal con tarjetas de resumen: total de estudiantes recogidos, paradas concluidas y progreso visual de la ruta activa.</td>
      <td align="center">6</td>
      <td>Luis Huaco</td>
      <td align="center">Done</td>
    </tr>
  </tbody>
</table>

#### **5.2.2.4. Development Evidence for Sprint Review**

Durante el Sprint 2, el equipo desarrolló la arquitectura modular del Frontend Web Application utilizando Vue 3 y Vite, estructurada por Bounded Contexts y organizada en capas limpias (Domain, Application/Store, Infrastructure/API y Presentation). A continuación, se presenta la trazabilidad del historial de commits registrados en el repositorio oficial conforme al estándar Conventional Commits:

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Commited on (Date) |
| :--- | :--- | :---: | :--- | :--- | :---: |
| children-path-frontend | `develop` | `1159d73` | fix: fixing | General bug fixes and style alignment across frontend views. | 2026-10-05 |
| children-path-frontend | `develop` | `792a678` | Merge branch 'feature/add-tracking' into develop | Integrated real-time tracking views and telemetry mock components into develop. | 2026-10-05 |
| children-path-frontend | `feature/add-tracking` | `cf28be9` | feat: add tracking presentation | Implemented tracking map container and UI live status indicators. | 2026-10-05 |
| children-path-frontend | `feature/add-tracking` | `320e0a5` | feat: add tracking api and entity | Configured mock API client endpoints and domain entities for vehicle tracking. | 2026-10-05 |
| children-path-frontend | `feature/add-tracking` | `abda4ba` | feat: add tracking store | Implemented Pinia store for tracking coordinates and telemetry states. | 2026-10-05 |
| children-path-frontend | `feature/add-tracking` | `d7c5c65` | feat: add tracking models | Defined TypeScript data interfaces and domain models for geo-tracking. | 2026-10-05 |
| children-path-frontend | `develop` | `2de06f2` | Merge branch 'feature/iam-test' into develop | Integrated authentication mock views and incident logging into develop. | 2026-10-05 |
| children-path-frontend | `feature/incidents` | `89c064c` | feat: add incidents presentation views | Maquetted incident reporting form and incident history table component. | 2026-10-05 |
| children-path-frontend | `feature/incidents` | `e8960c4` | feat: add incidents infrastructure api | Configured HTTP Axios services and json-server endpoints for incident persistence. | 2026-10-05 |
| children-path-frontend | `feature/incidents` | `1661825` | feat: add incidents domain models | Defined incident severity levels, categories, and domain entities. | 2026-10-05 |
| children-path-frontend | `feature/incidents` | `981b37c` | feat: add incidents store | Configured reactive store for incident logging and filter state. | 2026-10-05 |
| children-path-frontend | `feature/fleet` | `f609296` | feat: add fleet presentation - views , components and routes | Developed vehicle catalog cards, fleet status tables, and Vue routes. | 2026-10-05 |
| children-path-frontend | `feature/fleet` | `4e56041` | feat: add fleet domain - models and entitys | Defined vehicle specifications, license plate structures, and fleet models. | 2026-10-05 |
| children-path-frontend | `feature/fleet` | `9ec35de` | feat: add fleet infrastructure - assembler and api | Implemented DTO mappers, assemblers, and HTTP client for vehicle entities. | 2026-10-05 |
| children-path-frontend | `feature/fleet` | `ad2631c` | feat: add fleet application - store | Created Pinia state management for fleet units and active assignments. | 2026-10-05 |
| children-path-frontend | `feature/iam` | `8859ac6` | feat: add iam views fakes | Implemented simulated login and role-based credential views. | 2026-10-05 |
| children-path-frontend | `develop` | `a0ea932` | Merge branch 'feature/drivers' into develop | Merged driver management views, domain models, and API assemblers into develop. | 2026-10-05 |
| children-path-frontend | `feature/drivers` | `79dd741` | feat: add drivers presentation | Maquetted driver profile roster and driver detail card components. | 2026-10-05 |
| children-path-frontend | `feature/drivers` | `e8a1bec` | feat: add drivers infrastructure - api and routes | Configured driver API endpoints and child routes under Vue Router. | 2026-10-05 |
| children-path-frontend | `feature/drivers` | `c14a6be` | feat: add drivers infrastructure - assembler | Created assembler mappers from json-server payloads to driver domain entities. | 2026-10-05 |
| children-path-frontend | `feature/drivers` | `f19e889` | feat: add drivers domain - entities | Defined domain entities and lifecycle validation for driver profiles. | 2026-10-05 |
| children-path-frontend | `feature/drivers` | `3da0acd` | feat: add drivers domain - models | Created TypeScript interfaces and data contracts for drivers. | 2026-10-05 |
| children-path-frontend | `feature/drivers` | `dd3a691` | feat: add drivers domain - summary | Structured domain summary aggregations for driver operational statistics. | 2026-10-05 |
| children-path-frontend | `feature/drivers` | `6deac71` | feat: add drivers application - store | Configured central store actions for fetching and filtering active drivers. | 2026-10-05 |
| children-path-frontend | `develop` | `634bd16` | Merge branch 'feature/dashboard' into develop | Integrated operational dashboard components, routes, and API mocks into develop. | 2026-10-05 |
| children-path-frontend | `feature/dashboard` | `bd4757d` | feat: add dashboard components | Created summary metric cards, route progress bars, and status widgets. | 2026-10-05 |
| children-path-frontend | `feature/dashboard` | `b11ebdc` | feat: add dashboard views | Assembled main dashboard overview layout linking active fleet and trips. | 2026-10-05 |
| children-path-frontend | `feature/dashboard` | `c451180` | feat: add dashboard models | Defined operational dashboard data contracts and KPI metric interfaces. | 2026-10-05 |
| children-path-frontend | `feature/dashboard` | `4db6a08` | feat: add dashboard routes | Configured navigation routes and redirects for dashboard views. | 2026-10-05 |
| children-path-frontend | `feature/dashboard` | `28a8023` | feat: add dashboard api | Implemented mock API requests for operational summary telemetry data. | 2026-10-05 |
| children-path-frontend | `feature/dashboard` | `2e202b1` | feat: add dashboard store | Created Pinia store for caching dashboard statistics and active trip counts. | 2026-10-05 |
| children-path-frontend | `develop` | `588d69b` | Merge branch 'feature/init-images' into develop | Merged application brand logos and visual assets into develop. | 2026-10-05 |
| children-path-frontend | `feature/init-images` | `9ade521` | feat: add logo | Added high-resolution brand logo and graphical UI icons. | 2026-10-05 |
| children-path-frontend | `develop` | `2e793ee` | Merge pull request #11 from .../feature/companies | Integrated company management presentation views and routing into develop. | 2026-10-05 |
| children-path-frontend | `feature/companies` | `88d9dd4` | feat(companies): add company management view and presentation routes | Created school transport company catalog view and associated Vue navigation routes. | 2026-10-05 |

#### **5.2.2.5. Execution Evidence for Sprint Review**

Durante el Sprint 2 se implementó y validó la ejecución de la primera versión del aplicativo web frontend (**Frontend Web Application**) desarrollado en Vue 3 y Vite. A continuación, se presenta la evidencia de ejecución organizada por vista, Bounded Context implementado y el registro visual de las interfaces operativas:

| Módulo / Bounded Context | Vista / Componente | Descripción de la Evidencia | Captura de Pantalla |
| :--- | :--- | :--- | :---: |
| **Dashboard** | Panel General Operativo (`DashboardView.vue`) | Vista principal con tarjetas de métricas, resumen de unidades en tránsito y estado de las rutas activas del día. | ![Dashboard Overview](https://raw.githubusercontent.com/upc-202610-1asi0730-8084-Creatividad/children-path-report/develop/assets/app-dashboard.png) |
| **Attendance & Assignments** | Control de Abordaje de Estudiantes (`AttendanceView.vue`) | Lista interactiva para registrar el abordaje (`on_board`) y marcar ausencias justificadas o injustificadas en cada parada programada. | ![Control de Abordaje](https://raw.githubusercontent.com/upc-202610-1asi0730-8084-Creatividad/children-path-report/develop/assets/app-attendance.png) |
| **Fleet & Vehicles** | Catálogo de Flota Escolar (`FleetView.vue`) | Tabla CRUD con el listado de unidades vehiculares, placa, capacidad de estudiantes, modelo y asignación operativa. | ![Gestion de Flota](https://raw.githubusercontent.com/upc-202610-1asi0730-8084-Creatividad/children-path-report/develop/assets/app-fleet.png) |
| **Drivers** | Directorio de Conductores (`DriversView.vue`) | Listado y tarjetas de perfil de los transportistas escolares con sus datos de contacto y número de licencia de conducir. | ![Directorio de Conductores](https://raw.githubusercontent.com/upc-202610-1asi0730-8084-Creatividad/children-path-report/develop/assets/app-drivers.png) |
| **Routes & Tracking** | Vista de Ruta y Paradas (`RoutesView.vue`) | Detalle secuencial de paradas con indicación de hora estimada de llegada (ETA) y visualización del recorrido geolocalizado. | ![Seguimiento y Rutas](https://raw.githubusercontent.com/upc-202610-1asi0730-8084-Creatividad/children-path-report/develop/assets/app-routes.png) |
| **Incidents** | Registro de Incidencias en Ruta (`IncidentsView.vue`) | Formulario reactivo y tabla de historial para registrar imprevistos mecánicos, desvíos autorizados o congestión vehicular. | ![Registro de Incidencias](https://raw.githubusercontent.com/upc-202610-1asi0730-8084-Creatividad/children-path-report/develop/assets/app-incidents.png) |
| **Companies** | Gestión de Empresas de Transporte (`CompaniesView.vue`) | Panel de administración de datos corporativos, colegios asociados y configuración del servicio de movilidad. | ![Gestion de Empresas](https://raw.githubusercontent.com/upc-202610-1asi0730-8084-Creatividad/children-path-report/develop/assets/app-companies.png) |

#### **5.2.2.6. Services Documentation Evidence for Sprint Review**

| Status |
| :--- |
| **No aplica para este Sprint.** De acuerdo con el alcance pedagógico de la entrega TB1 (Semana 7), el equipo se enfocó de manera exclusiva en el desarrollo de la capa cliente (**Frontend Web Application**), maquetación de vistas de usuario, formularios interactivos y simulación de persistencia mediante un servidor de desarrollo mock (`json-server`). La especificación técnica y documentación formal OpenAPI/Swagger de los servicios RESTful del Backend en C#/.NET se completará en los sprints subsecuentes. |


#### **5.2.2.7. Software Deployment Evidence for Sprint Review**

#### **5.2.2.8. Team Collaboration Insights during Sprint**

Durante el desarrollo del Sprint 2, el equipo consolidó las siguientes lecciones aprendidas y prácticas de ingeniería frontend:

| Insight |
| :--- |
| **Estructuración DDD por Bounded Contexts:** La división del frontend en subdirectorios independientes (`dashboard`, `drivers`, `fleet`, `incidents`, `companies`, `tracking`) con sus propias capas de presentación, modelos y almacenes (Pinia) evitó conflictos de merge al trabajar múltiples integrantes de forma simultánea. |
| **Desacoplamiento con Fake API (json-server):** Utilizar contratos de datos simulados y capas de ensamblado (*assemblers*) facilitó la construcción de vistas y tablas CRUD sin depender de la disponibilidad del backend real, agilizando las pruebas funcionales de la UI. |
| **Enfoque estricto en funcionalidades Core y formularios reactivos:** Centrar los esfuerzos en el flujo operativo esencial (gestión de flotas, conductores, estados de abordaje y registro rápido de incidencias) permitió optimizar la usabilidad y los tiempos de interacción de las vistas principales antes de incorporar lógica más compleja. |
| **Estandarización de componentes reutilizables:** Establecer convenciones uniformes para tablas de datos, botones de acción rápida y modales de diálogo aseguró una experiencia visual homogénea y coherente a lo largo de todos los módulos del aplicativo web. |

### **5.2.3. Sprint 3**

#### **5.2.3.1. Sprint Planning 3**


#### **5.2.3.2. Aspect Leaders and Collaborators**


#### **5.2.3.3. Sprint Backlog 3**


#### **5.2.3.4. Development Evidence for Sprint Review**


#### **5.2.3.5. Execution Evidence for Sprint Review**

#### **5.2.3.6. Services Documentation Evidence for Sprint Review**

#### **5.2.3.7. Software Deployment Evidence for Sprint Review**


#### **5.2.3.8. Team Collaboration Insights during Sprint**

## **5.3. Validation Interviews**

### **5.3.1. Interview Design**

### **5.3.2. Interview Recording**

### **5.3.3. Evaluations Based on Heuristics**

## **5.4. About-the-Product Video**
