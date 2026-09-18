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

Durante el Sprint 1, el equipo se enfocó en definir la estructura y el diseño inicial de la Landing Page de **Children Path**. El objetivo fue comunicar claramente la propuesta de valor y presentar el problema y la solución a los usuarios potenciales.

| Sprint # | Sprint 1                                          |
| ------------------------------ |---------------------------------------------------|
| **Sprint Planning Background** | Definición y diseño conceptual de la Landing Page |
| **Date** | 2026-09-06                                        |
| **Time** | 07:00 PM                                          |
| **Location** | Reunión virtual vía Google Meet                   |
| **Prepared By** | Huaco Oliva, Luis Alonso                          |
| **Attendees** | Miembros del equipo                               |

**Sprint Goal & User Stories**

| Sprint Goal | Description |
| ------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Sprint 1 Goal** | Nuestro enfoque está en diseñar una Landing Page clara y estructurada. Creemos que esto permitirá que los usuarios potenciales comprendan el valor del producto. Esto se confirmará cuando los usuarios puedan identificar el problema y la solución en la primera interacción. |
| **Sprint 1 Velocity** | 10 Story Points |
| **Sum of Story Points** | 10 |

#### **5.2.1.2. Aspect Leaders and Collaborators**

Durante este Sprint, el equipo trabajó en el diseño de la Landing Page, la estructura UX y la creación de contenido.

| Team Member | GitHub Username | Wireframe Design | Content Writing | UX Structure |
| --------------------- | --------------- | ---------------- | --------------- | ------------ |
| Huaco, Luis | perghomarv-pixel | L | C | L |
| Pareja, Diana | diana-pareja | C | L | C |
| Soto, Bradon | bradon-soto | C | C | C |
| Razuri, Piero | piero-razuri | C | C | L |

**Leyenda:** L = Leader (Líder) | C = Collaborator (Colaborador)

#### **5.2.1.3. Sprint Backlog 1**

El Sprint Backlog se enfocó en definir la estructura y el diseño inicial de la Landing Page.

| User Story | Work-Item / Task Id | Title | Description | Estimation (Hours) | Assigned To | Status |
| ---------- | ------------------- | ------------------ | --------------------------------------------- | ------------------ | ----------- | ------ |
| LP-01 | T1 | Definir estructura | Identificar las secciones principales de la Landing Page | 4 | Luis | Done |
| LP-02 | T2 | Crear wireframe | Diseñar prototipo de baja fidelidad en Figma | 6 | Diana | Done |
| LP-03 | T3 | Redactar contenido | Redactar textos del problema y la solución | 5 | Bradon | Done |
| LP-04 | T4 | Validación del flujo UX | Validar el orden de las secciones y la comprensión del usuario | 3 | Piero | Done |
| LP-05 | T5 | Revisión interna | Revisar la consistencia del diseño y el contenido | 2 | Luis | Done |

#### **5.2.1.4. Development Evidence for Sprint Review**

Durante este Sprint, el equipo completó el diseño conceptual de la Landing Page.

| Repository | Branch | Committed on |
| ----------------- | ----------------- | ------------ |
| children-path-landing | feature/chapter-4 | 2026-04-10 |
| children-path-landing | feature/chapter-4 | 2026-04-11 |
| children-path-landing | feature/chapter-4 | 2026-04-12 |

#### **5.2.1.5. Execution Evidence for Sprint Review**

Durante este Sprint, el equipo validó la estructura y claridad de la Landing Page.

| Evidence Type | Description |
| --------------- | -------------------------------------------------------------------------------------------------- |
| Wireframes | Diseño de baja fidelidad que muestra el layout |
| UX validation | Flujo lógico entre secciones |
| Internal review | Retroalimentación de los miembros del equipo |

#### **5.2.1.6. Services Documentation Evidence for Sprint Review**

| Status |
| ------------------------------------------------------------------------ |
| No aplica. No se implementaron servicios RESTful durante este Sprint. |

#### **5.2.1.7. Software Deployment Evidence for Sprint Review**

| Status |
| --------------------------------------------------------------- |
| No aplica. La Landing Page aún se encontraba en fase de diseño. |

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