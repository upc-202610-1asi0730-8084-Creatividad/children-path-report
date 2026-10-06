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


#### **5.2.2.2. Aspect Leaders and Collaborators**


#### **5.2.2.3. Sprint Backlog 2**

#### **5.2.2.4. Development Evidence for Sprint Review**

#### **5.2.2.5. Execution Evidence for Sprint Review**

#### **5.2.2.6. Services Documentation Evidence for Sprint Review**

#### **5.2.2.7. Software Deployment Evidence for Sprint Review**

#### **5.2.2.8. Team Collaboration Insights during Sprint**

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
