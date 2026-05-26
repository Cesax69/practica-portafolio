# Portafolio Web Profesional - César Enrique Garay García

Este proyecto es la entrega correspondiente a la **Práctica 1: Personalización y Publicación Profesional de un Sitio Web con Git y GitHub**. Se trata de un portafolio web de diseño premium, dinámico, completamente responsivo y adaptado para perfilar la trayectoria, habilidades, certificaciones y proyectos del alumno como Desarrollador Full Stack.

El sitio ha sido completamente personalizado a partir de una plantilla base, elevando sus estándares estéticos con variables modernas de diseño y corrigiendo errores lógicos y sintácticos nativos del código original.

---

## Características Clave

- **Selector de Tema Inteligente**: Soporte para Modo Claro y Modo Oscuro premium con persistencia en el navegador (`localStorage`).
- **Estética de Vanguardia**: Paleta de colores *Dark Slate & Neon Cyan* futurista con tipografías sofisticadas de Google Fonts (*Outfit* para títulos y *Plus Jakarta Sans* para lectura).
- **Efecto Glassmorphism**: Componentes translúcidos modernos con efectos de desenfoque de fondo (`backdrop-filter`) y sutiles bordes brillantes.
- **Diseño 100% Responsivo**: Adaptabilidad completa garantizada para smartphones, tablets y pantallas de escritorio grandes.
- **Efecto de Escritura Dinámica (Typewriter)**: Animación interactiva en la sección de inicio para resaltar roles profesionales.
- **Animaciones AOS (Animate On Scroll)**: Desplazamientos suaves y transiciones estéticas de entrada para todos los componentes.
- **Scrollspy Activo**: Resaltado automático y dinámico de la sección actual en la barra de navegación.

---

## Tecnologías Empleadas

- **HTML5** para la estructura semántica.
- **CSS3** para los estilos premium, gradientes interactivos y sistema de diseño adaptativo.
- **JavaScript (Vanilla JS - ES6+)** para la lógica del tema, modals, scroll spy y validación de interfaces.
- **Swiper.js** para un slider táctil y fluido en la sección de proyectos.
- **AOS Library** para disparar animaciones al hacer scroll.
- **Unicons** para una iconografía vectorial y estilizada.

---

## Estructura del Proyecto

```text
├── assets/
│   ├── img/            # Recursos visuales (Avatares, favicons y capturas de proyectos)
│   └── PDF/            # Currículum Vitae (CV) profesional en formato PDF
├── index.html          # Estructura HTML5 semántica y completamente traducida
├── main.js             # Lógica JavaScript con optimizaciones y corrección de fallos
├── styles.css          # Hojas de estilo personalizadas con variables premium
└── README.md           # Esta bitácora y guía técnica profesional
```

---

## Optimizaciones y Corrección de Bugs Realizadas

Como parte de una auditoría y refactorización profesional de código, se detectaron y corrigieron los siguientes errores nativos del repositorio base:

1. **Persistencia del Tema (Bug de LocalStorage)**:
   - *Fallo*: El script original guardaba el tema bajo la clave `'selected-themee'` (con doble 'e'), pero al recargar la página intentaba recuperarlo buscando la clave `'selected-theme'`. Esto provocaba que la selección de tema del usuario se perdiera al actualizar.
   - *Solución*: Se unificaron las referencias de guardado y lectura a la clave correcta `'selected-theme'`.
2. **Interactividad de Pestañas de Trayectoria (Bug de Clase CSS)**:
   - *Fallo*: Al pulsar sobre las pestañas de Educación o Experiencia, el JavaScript original asignaba de manera errónea la clase `ualification__content` (omitiendo la letra 'q'). Esto rompía la visibilidad y estilos CSS de la sección completa.
   - *Solución*: Se corrigió la asignación dinámica de la clase a `qualification__content`.
3. **Scrollspy Navegación (Bug de Clase con punto)**:
   - *Fallo*: El código original de Scrollspy estaba completamente comentado e inactivo debido a que utilizaba `.classList.add('.active-link')` y `.classList.remove('.active-link')` incluyendo un punto en el nombre de la clase, lo cual es inválido en la sintaxis de JavaScript.
   - *Solución*: Se refactorizó la función `scrollActive` con validación de existencia para evitar errores en consola y se corrigieron los nombres de las clases a `'active-link'`.
4. **Error de Sintaxis en Estilos `.about__img`**:
   - *Fallo*: En la regla de medios `@media screen and (min-width: 768px)`, la clase `.about__img` contenía la propiedad inválida `will-change: 350px;`, un error de sintaxis que causaba advertencias en los navegadores.
   - *Solución*: Se modificó por la propiedad correcta `width: 350px;`.
5. **Bloqueo del Scroll Vertical en CSS**:
   - *Fallo*: La hoja de estilos original contenía las propiedades `overflow: hidden; overflow-y: hidden;` directamente en la etiqueta `body`, lo que bloqueaba por completo la capacidad de deslizar verticalmente el sitio en dispositivos y navegadores modernos.
   - *Solución*: Se reconfiguró a `overflow-x: hidden;` para asegurar un deslizamiento suave sin desbordamiento horizontal.

---

## Flujo de Trabajo en Git (Comandos Utilizados)

Para llevar a cabo el proyecto bajo los mejores estándares de desarrollo profesional, se utilizó la siguiente secuencia de comandos en consola:

1. **Clonación del repositorio original**:
   ```bash
   git clone https://github.com/DaneshCode/Portfolio-Website.git .
   ```
2. **Desvinculación del repositorio original (limpieza de origen remoto)**:
   ```bash
   git remote remove origin
   ```
3. **Creación y cambio a una rama de desarrollo limpia**:
   ```bash
   git checkout -b feature/customization
   ```
4. **Commits atómicos organizados con el estándar *Conventional Commits***:
   - `style: actualizar sistema de diseño (Google Fonts, Slate & Neon y Glassmorphism)`
   - `fix: corregir errores de localStorage, tabs y reactivar scrollSpy`
   - `feat: personalizar portafolio en español para el perfil de César`
   - `feat: integrar proyectos reales de GitHub (Artesanias-Garay, Smart-Home IoT, cegg-api)`
   - `style: redisenar portafolio con efectos glassmorphic premium, gradientes de texto y glows de fondo`

---

## Instrucciones de Despliegue en GitHub Pages

Para publicar el portafolio en internet sin costo a través de **GitHub Pages**, siga estos pasos desde la terminal:

### Paso 1: Inicializar y Unificar Cambios en tu Git local
Fusione los cambios de la rama de desarrollo `feature/customization` a la rama principal `main`:
```bash
# Cambiar a la rama principal
git checkout main

# Fusionar los cambios
git merge feature/customization
```

### Paso 2: Crear un repositorio vacío en tu cuenta de GitHub
1. Acceda a su cuenta de GitHub y cree un nuevo repositorio llamado `practica-portafolio`.
2. **IMPORTANTE**: No lo inicialice con archivos README, .gitignore o licencias (déjelo vacío).

### Paso 3: Vincular tu repositorio local con el remoto de GitHub
Vincule el repositorio remoto y suba los cambios con los siguientes comandos:
```bash
# Vincular el repositorio remoto de GitHub
git remote add origin https://github.com/Cesax69/practica-portafolio.git

# Renombrar la rama a main si no lo está
git branch -M main

# Subir los cambios a GitHub
git push -u origin main
```

### Paso 4: Activar GitHub Pages
1. Abra su repositorio en la página de GitHub.
2. Diríjase a la pestaña de **Settings** (Configuración) en el menú superior.
3. En la barra lateral izquierda, haga clic en **Pages**.
4. En la sección **Build and deployment**, bajo el apartado *Branch*, seleccione la rama `main` y la carpeta `/ (root)`.
5. Haga clic en **Save** (Guardar).

En unos minutos, GitHub compilará el sitio y proporcionará un enlace permanente (por ejemplo: `https://Cesax69.github.io/practica-portafolio/`) para visualizar el portafolio premium en vivo.
