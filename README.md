# Mi Portfolio Minimalista

Este es un portfolio web moderno y minimalista, diseñado con HTML, CSS y JavaScript, con un enfoque en tonos grises y una experiencia de usuario adaptable a diferentes dispositivos. Incluye funcionalidades como un modo oscuro/claro y un formulario de contacto funcional.

## Contenido

1.  [Características Principales](#características-principales)
2.  [Tecnologías Utilizadas](#tecnologías-utilizadas)
3.  [Estructura del Proyecto](#estructura-del-proyecto)
4.  [Configuración y Ejecución Local](#configuración-y-ejecución-local)
5.  [Guía de Personalización (Explicación del Código)](#guía-de-personalización-explicación-del-código)
    *   [HTML (`index.html`)](#html-indexhtml)
    *   [CSS (`styles.css`)](#css-stylescss)
    *   [JavaScript (`script.js`)](#javascript-scriptjs)
6.  [Despliegue en Producción (GitHub Pages)](#despliegue-en-producción-github-pages)
7.  [Próximas Mejoras Sugeridas](#próximas-mejoras-sugeridas)

---

## 1. Características Principales

*   **Diseño Minimalista:** Estética limpia y moderna con énfasis en la simplicidad y la usabilidad.
*   **Paleta de Grises:** Uso predominante de tonos grises para una apariencia sofisticada.
*   **Modo Oscuro/Claro:** Botón de alternancia de tema con persistencia de la preferencia del usuario.
*   **Responsive Design:** Adaptable a diferentes tamaños de pantalla (escritorio, tabletas, móviles).
*   **Animaciones Suaves:** Efectos de aparición al hacer scroll y transiciones fluidas en interacciones.
*   **Botón "Volver Arriba":** Facilita la navegación en páginas largas.
*   **Formulario de Contacto Funcional:** Integrado con Formspree para envíos de correo sin backend.
*   **Estructura Modular:** Código organizado en secciones claras para facilitar la personalización.

## 2. Tecnologías Utilizadas

*   **HTML5:** Estructura semántica del contenido.
*   **CSS3:** Estilización, variables CSS, Flexbox, Grid y Media Queries.
*   **JavaScript:** Funcionalidades dinámicas (cambio de tema, scroll-to-top, animaciones).
*   **Font Awesome:** Biblioteca de iconos para elementos visuales.
*   **Formspree:** Servicio para manejar los envíos del formulario de contacto.

## 3. Estructura del Proyecto

El proyecto está organizado de la siguiente manera:

```
.
├── index.html          # Estructura principal de la página web
├── styles.css          # Estilos CSS de la página
├── script.js           # Lógica JavaScript
└── images/             # Carpeta para almacenar imágenes del proyecto (ej: banner.jpg)
    └── banner.jpg      # Imagen de fondo para el banner
```

## 4. Configuración y Ejecución Local

Para ver el portfolio en tu máquina local:

1.  **Clona o descarga el repositorio:**
    ```bash
    git clone https://github.com/tu-usuario/tu-repositorio.git
    cd tu-repositorio
    ```
2.  **Abre el archivo `index.html`:** Simplemente haz doble clic en `index.html` en tu explorador de archivos, o ábrelo en tu navegador web preferido.

## 5. Guía de Personalización (Explicación del Código)

### HTML (`index.html`)

Este archivo define la estructura y el contenido de tu portfolio.

*   **`<head>`:**
    *   `<!DOCTYPE html>`: Define el tipo de documento HTML5.
    *   `<html lang="es">`: Declara el idioma principal de la página (español).
    *   `<meta charset="UTF-8">`: Especifica la codificación de caracteres.
    *   `<meta name="viewport" content="width=device-width, initial-scale=1.0">`: Asegura la correcta visualización en dispositivos móviles.
    *   `<title>Mi Portfolio</title>`: Título que aparece en la pestaña del navegador.
    *   `<link rel="stylesheet" href="styles.css">`: Vincula el archivo CSS principal.
    *   `<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">`: Incluye la librería de iconos Font Awesome.

*   **`<body>`:**
    *   **`<header>`:** Contiene la barra de navegación.
        *   `<nav>`: Elemento de navegación.
            *   `<ul>`: Lista de enlaces a las secciones principales (`#inicio`, `#sobre-mi`, `#proyectos`, `#contacto`).
            *   `<button id="theme-toggle" class="theme-toggle">`: Botón para alternar el modo oscuro/claro con un icono de luna/sol.
    *   **`<main>`:** Contenido principal de la página.
        *   **`<section class="banner">`**: Sección principal de bienvenida con un título y un subtítulo.
            *   `<h1>Bienvenido usuario</h1>`: Título principal del portfolio.
            *   `<p>QA Automation Engineer</p>`: Subtítulo que describe tu rol.
        *   **`<section id="sobre-mi" class="about">`**: Información sobre ti.
            *   `<h2>Sobre Mí</h2>`: Título de la sección.
            *   `<div class="about-content">`: Contenedor para la descripción personal.
            *   `<p>QA con más de 3 años de experiencia...</p>`: Tu texto de presentación.
        *   **`<section id="proyectos" class="projects">`**: Muestra tus proyectos.
            *   `<h2>Proyectos QA</h2>`: Título de la sección.
            *   `<div class="project-grid">`: Contenedor para la cuadrícula de proyectos.
            *   `<div class="project-card">`: Cada tarjeta de proyecto.
                *   `<h3>Pruebas automatizadas en formularios</h3>`: Nombre del proyecto.
                *   `<p>Automatización de pruebas funcionales...</p>`: Descripción del proyecto.
        *   **`<section id="contacto" class="contact">`**: Información de contacto y formulario.
            *   `<h2>Contacto</h2>`: Título de la sección.
            *   `<form action="https://formspree.io/f/xeokaego" method="POST" class="contact-form">`: Formulario de contacto.
                *   `action`: URL de Formspree donde se enviarán los datos.
                *   `method="POST"`: Envío de datos.
                *   `<input type="text" name="name" placeholder="Tu Nombre" required>`: Campo para el nombre.
                *   `<input type="email" name="email" placeholder="Tu Email" required>`: Campo para el email.
                *   `<textarea name="message" placeholder="Tu Mensaje" required></textarea>`: Área de texto para el mensaje.
                *   `<button type="submit">Escribime</button>`: Botón para enviar el formulario.
            *   `<div class="contact-info">`: Información adicional de contacto.
                *   `<p>Email: alexx.ibarra@gmail.com</p>`: Tu correo electrónico.
                *   `<p>LinkedIn: <a href="..." target="_blank">alexisibarra5</a></p>`: Enlace a tu perfil de LinkedIn.
                *   `<p>GitHub: <a href="..." target="_blank">alexisibarra55</a></p>`: Enlace a tu perfil de GitHub.
    *   **`<button id="scroll-top" class="scroll-top">`**: Botón flotante para volver arriba en la página.
    *   **`<footer>`**: Pie de página con información de copyright.
        *   `<p>&copy; 2024 Mi Portfolio. Todos los derechos reservados.</p>`
    *   `<script src="script.js"></script>`: Vincula el archivo JavaScript para las funcionalidades dinámicas.

### CSS (`styles.css`)

Este archivo contiene todos los estilos visuales de la página.

*   **Variables de Color (`:root` y `[data-theme="dark"]`)**:
    *   `--primary-gray`, `--light-gray`, `--medium-gray`, `--accent-gray`, `--section-gray`: Diferentes tonos de gris utilizados para fondos, bordes y acentos.
    *   `--text-light`, `--text-dark`: Colores de texto para fondos claros y oscuros, respectivamente.
    *   `--header-text`: Color específico para el texto en la barra de navegación.
    *   `--transition-speed`: Define la duración de las transiciones CSS.
    *   **`[data-theme="dark"]`**: Bloque que redefine estas variables para el modo oscuro, invirtiendo o ajustando los colores para una experiencia visual agradable.

*   **Reset y Estilos Base (`*`, `body`)**:
    *   `margin: 0; padding: 0; box-sizing: border-box;`: Reseteo básico para eliminar estilos por defecto del navegador.
    *   `font-family`, `line-height`, `color`, `background-color`: Estilos generales de tipografía y fondo para todo el cuerpo de la página.

*   **Navegación (`header`, `nav ul`, `nav ul li`, `nav ul li a`, `.theme-toggle`)**:
    *   Estilos para la barra de navegación fija en la parte superior, incluyendo alineación, padding, sombras.
    *   Estilos para los enlaces de navegación y el botón de alternar tema, incluyendo efectos `hover`.

*   **Banner (`.banner`, `.banner-content`, `h1`, `p`)**:
    *   Define la altura, ancho, imagen de fondo (con degradado oscuro para legibilidad), y cómo se centra el contenido.
    *   Estilos para el título y subtítulo del banner, incluyendo color de texto (`--text-dark`) y sombras para contraste.

*   **Secciones Principales (`main`, `section`, `.about`, `.projects`, `.contact`, `h2`)**:
    *   Estilos para el `main` y las secciones generales, incluyendo padding y las animaciones de aparición.
    *   Fondo y color de texto específicos para las secciones "Sobre Mí", "Proyectos" y "Contacto" usando las variables de color.
    *   Estilos para los títulos de sección (`h2`).

*   **Proyectos (`.project-grid`, `.project-card`)**:
    *   Diseño de cuadrícula para los proyectos (`display: grid`).
    *   Estilos para las tarjetas individuales de proyectos, incluyendo padding, bordes redondeados y un efecto `transform` al hacer `hover`.

*   **Formulario de Contacto (`.contact-form`, `input`, `textarea`, `button`, `::placeholder`)**:
    *   Estilos para el contenedor del formulario (Flexbox para organización vertical, ancho máximo, padding, sombras).
    *   Estilos para los campos de texto y área de texto (padding, bordes, fondo, color de texto, `focus`).
    *   Estilos para el botón de envío (fondo, color de texto, `hover`).
    *   Estilos específicos para el texto del placeholder (`::placeholder`).

*   **Botón de Scroll Arriba (`.scroll-top`)**:
    *   Posicionamiento fijo, forma redondeada, colores y un efecto `hover`.
    *   La clase `.visible` controla su visibilidad (gestionada por JavaScript).

*   **Animaciones (`@keyframes fadeIn`, `@keyframes slideUp`)**:
    *   Definición de las animaciones `fadeIn` (para secciones) y `slideUp` (para tarjetas de proyecto) que se activan al hacer scroll.

*   **Responsive Design (`@media (max-width: 768px)`)**:
    *   Contiene reglas CSS que se aplican solo a pantallas con un ancho máximo de 768 píxeles (dispositivos móviles y tabletas).
    *   Ajustes para el tamaño del banner, tamaños de fuente y, muy importante, el layout del `header` y `nav` para que se vean bien en pantallas pequeñas (enlaces en fila, botón de tema bien posicionado).

*   **Estilos de Modo Oscuro para Formulario (`[data-theme="dark"] .contact-form`)**:
    *   Reglas específicas para el formulario cuando el modo oscuro está activado, asegurando un contraste adecuado para sus elementos.

### JavaScript (`script.js`)

Este archivo maneja las funcionalidades interactivas de la página.

*   **Funcionalidad del Botón "Volver Arriba"**:
    *   Obtiene el botón por su `id`.
    *   `window.addEventListener('scroll', ...) `: Escucha el evento de scroll para mostrar u ocultar el botón (añadiendo/removiendo la clase `visible` a `.scroll-top`) cuando el usuario ha bajado lo suficiente en la página.
    *   `scrollTopButton.addEventListener('click', ...)`: Al hacer clic, la página se desplaza suavemente al inicio (`window.scrollTo({ top: 0, behavior: 'smooth' })`).

*   **Funcionalidad del Cambio de Tema (Modo Oscuro/Claro)**:
    *   Obtiene el botón (`#theme-toggle`) y su icono (`<i>`).
    *   **Persistencia del Tema**: `localStorage.getItem('theme') || 'light'` recupera la preferencia del usuario o establece "light" como predeterminado. El tema se aplica inmediatamente al cargar la página (`document.body.setAttribute('data-theme', savedTheme);`).
    *   `themeToggle.addEventListener('click', ...)`: Al hacer clic, alterna el atributo `data-theme` del `body` entre 'light' y 'dark', y guarda la preferencia en `localStorage`.
    *   `function updateThemeIcon(theme)`: Cambia el icono (luna o sol) según el tema actual.

*   **Animación de Aparición de Elementos al Hacer Scroll**:
    *   `IntersectionObserver`: Una API de navegador que permite observar si un elemento entra o sale del viewport del navegador.
    *   `observerOptions`: Configura cuándo se activa el observador (cuando el 10% del elemento es visible).
    *   El observador se aplica a todas las `section` y `.project-card`.
    *   Inicialmente, estos elementos tienen `opacity: 0` y `transform: translateY(20px)` (invisibles y ligeramente desplazados).
    *   Cuando un elemento entra en el viewport (`entry.isIntersecting` es `true`), su opacidad se vuelve `1` y el `transform` vuelve a `translateY(0)`, creando el efecto de aparición suave.

## 6. Despliegue en Producción (GitHub Pages)

Tu portfolio ya está desplegado en GitHub Pages. Aquí un recordatorio de los pasos:

1.  **Crea un repositorio en GitHub:** Sube todos los archivos de tu proyecto a un repositorio público.
2.  **Configura GitHub Pages:**
    *   En tu repositorio, ve a **Settings** > **Pages**.
    *   En "Source", selecciona la rama `main` y la carpeta `/ (root)`.
    *   Haz clic en "Save".
3.  **Accede a tu portfolio:** Después de unos minutos, tu sitio estará en vivo en una URL como `https://tu-usuario.github.io/nombre-del-repositorio/` (en tu caso: `https://alexisibarra55.github.io/portfolio/`).

## 7. Próximas Mejoras Sugeridas

Considera estas ideas para seguir evolucionando tu portfolio:

*   **Páginas de Detalle de Proyectos:** Crea una página HTML separada para cada proyecto con más imágenes, videos y una descripción técnica profunda.
*   **Sección de Habilidades:** Muestra tus habilidades (idiomas, frameworks, herramientas) de forma visual (ej. barras de progreso, iconos).
*   **Carrusel de Proyectos:** Un carrusel interactivo en la sección de proyectos.
*   **Testimonios:** Una sección para mostrar lo que otros dicen de tu trabajo.
*   **Blog Personal:** Si te gusta escribir, un blog integrado para compartir tus conocimientos.
*   **Animaciones Avanzadas:** Explorar librerías como GSAP o ScrollReveal para animaciones más complejas.
*   **Personalización de Favicon:** Cambia el icono de la pestaña del navegador.
*   **Optimización de Rendimiento:** Comprimir imágenes, minificar CSS/JS para cargas más rápidas.

---

Espero que esta documentación te sea de gran utilidad para entender y seguir desarrollando tu portfolio. ¡Felicidades por tu proyecto! 