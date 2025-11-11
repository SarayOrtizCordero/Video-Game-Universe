# Video Game Universe

## Descripción

Video Game Universe es un sitio web estático desarrollado con HTML5, CSS3 y Font Awesome, enfocado en proporcionar una plataforma de visualización de videojuegos con diseño responsivo y accesible. El proyecto implementa las mejores prácticas de desarrollo web frontend, incluyendo semántica HTML, CSS Grid y Flexbox para layouts avanzados, y cumplimiento de estándares WCAG 2.1 para accesibilidad.

## Tabla de Contenidos

- [Descripción](#descripción)
- [Características Técnicas](#características-técnicas)
- [Requisitos Previos](#requisitos-previos)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Instalación](#instalación)
- [Uso](#uso)
- [Tecnologías Implementadas](#tecnologías-implementadas)
- [Diseño y Arquitectura CSS](#diseño-y-arquitectura-css)
- [Accesibilidad](#accesibilidad)
- [Navegadores Compatibles](#navegadores-compatibles)
- [Optimización y Rendimiento](#optimización-y-rendimiento)
- [Contribuciones](#contribuciones)
- [Licencia](#licencia)
- [Autor](#autor)

## Características Técnicas

- Diseño responsivo con sistema de breakpoints adaptativo (360px, 768px, 1200px, 1400px)
- Arquitectura CSS modular con variables CSS personalizadas
- Sistema de grid avanzado con CSS Grid y Flexbox
- Implementación de Font Awesome 6.6.0 para iconografía
- Optimización de imágenes con lazy loading nativo
- Validación HTML5 semántico
- Tema oscuro premium con paleta de colores consistente
- Animaciones y transiciones CSS optimizadas
- Sistema de navegación accesible con ARIA labels

## Requisitos Previos

### Herramientas Necesarias

- Navegador web moderno (Google Chrome 90+, Mozilla Firefox 88+, Safari 14+, Microsoft Edge 90+)
- Editor de código (Visual Studio Code, Sublime Text, o similar)
- Servidor web local (opcional, recomendado):
  - Node.js 18.x o superior con `http-server`
  - Python 3.x con `http.server`
  - Live Server (extensión de VS Code)

### Dependencias Externas

- Font Awesome 6.6.0 (cargado vía CDN)

## Estructura del Proyecto

```
video-game-universe/
│
├── index.html                 # Página principal
├── favicon.ico                # Icono del sitio
│
├── assets/                    # Recursos multimedia
│   └── images/                # Imágenes de productos y logos
│       ├── Assassins-Creed-Shadows.jpg
│       ├── metal-gear-solid-delta-art.jpg
│       ├── resident-evil-2-remake.jpg
│       ├── Silent-Hill-2-Remake.jpeg
│       ├── Uncharted-4.jpeg
│       ├── Until-Dawn-Remake.jpeg
│       └── [más imágenes...]
│
├── css/                       # Hojas de estilo
│   ├── styles.css             # Estilos globales y base
│   ├── productos.css          # Estilos de catálogo de productos
│   ├── boletin.css            # Estilos de formulario de boletín
│   └── contacto.css           # Estilos de página de contacto
│
└── views/                     # Páginas secundarias
    ├── productos.html         # Catálogo de videojuegos
    ├── boletin.html           # Formulario de suscripción
    └── contacto.html          # Información de contacto
```

## Instalación

### Método 1: Clonar el Repositorio

```bash
# Clonar el repositorio
git clone https://github.com/SarayOrtizCordero/video-game-universe

# Navegar al directorio del proyecto
cd video-game-universe
```

### Método 2: Descarga Directa

1. Descargar el archivo ZIP del repositorio
2. Extraer el contenido en el directorio deseado
3. Asegurar que la estructura de carpetas se mantenga intacta

### Configuración del Servidor Local

#### Opción A: Usar Python

```bash
# Python 3.x
python -m http.server 8000

# Acceder a: http://localhost:8000
```

#### Opción B: Usar Node.js

```bash
# Instalar http-server globalmente
npm install -g http-server

# Ejecutar el servidor
http-server -p 8000

# Acceder a: http://localhost:8000
```

#### Opción C: Usar Live Server (VS Code)

1. Instalar la extensión "Live Server" en Visual Studio Code
2. Clic derecho en `index.html`
3. Seleccionar "Open with Live Server"

## Uso

### Navegación del Sitio

El sitio web consta de cuatro secciones principales accesibles desde el menú de navegación:

1. **Inicio** (`index.html`)
   - Página principal con características destacadas
   - Catálogo de videojuegos destacados
   - Enlaces a redes sociales

2. **Productos** (`views/productos.html`)
   - Catálogo completo de videojuegos
   - Galería de imágenes para cada producto
   - Información de precios

3. **Boletín** (`views/boletin.html`)
   - Formulario de suscripción al boletín
   - Validación HTML5 nativa
   - Campos de datos de usuario y preferencias

4. **Contacto** (`views/contacto.html`)
   - Información de ubicación
   - Datos de contacto
   - Integración con redes sociales

### Personalización

#### Modificar Colores del Tema

Editar las variables CSS en `css/styles.css`:

```css
:root {
    --color-primary: #003087;
    --color-accent: #00d9ff;
    --color-gold: #ffd900ab;
    --color-bg-main: #0a0e27;
    /* Más variables disponibles */
}
```

#### Añadir Nuevos Productos

En `views/productos.html`, duplicar la estructura de un `article` existente:

```html
<article class="product-card">
    <h2>Nombre del Juego <span class="price">XX,XX€</span></h2>
    <div class="product-gallery">
        <img src="../assets/images/imagen.jpg" alt="Descripción" loading="lazy">
        <!-- Más imágenes -->
    </div>
</article>
```

#### Modificar Enlaces de Redes Sociales

Actualizar los enlaces en el `footer` de cada página HTML:

```html
<div class="social-links">
    <a href="https://www.instagram.com/tu_usuario" aria-label="Instagram">
        <i class="fa-brands fa-instagram"></i>
    </a>
    <!-- Más enlaces -->
</div>
```

## Tecnologías Implementadas

### Frontend

- **HTML5**: Estructura semántica con elementos como `<article>`, `<section>`, `<nav>`, `<aside>`
- **CSS3**: Diseño avanzado con Grid, Flexbox, Custom Properties, Gradients, Transforms
- **Font Awesome 6.6.0**: Biblioteca de iconos vectoriales

### Características CSS Avanzadas

- CSS Grid Layout para estructuras complejas
- Flexbox para alineación y distribución
- CSS Custom Properties (variables) para tematización
- Media Queries para diseño responsivo
- Pseudo-elementos (::before, ::after) para efectos visuales
- Animaciones y transiciones CSS
- Gradientes lineales y radiales
- Box-shadow y text-shadow para profundidad
- Filter y backdrop-filter para efectos visuales

## Diseño y Arquitectura CSS

### Sistema de Variables CSS

El proyecto utiliza un sistema centralizado de variables CSS para mantener consistencia:

```css
:root {
    /* Colores */
    --color-primary: #003087;
    --color-accent: #00d9ff;
    
    /* Espaciado */
    --spacing-xs: 0.5rem;
    --spacing-sm: 1rem;
    --spacing-md: 2rem;
    
    /* Efectos */
    --glow-cyan: 0 0 20px rgba(0, 217, 255, 0.5);
    --shadow-card: 0 8px 32px rgba(0, 0, 0, 0.6);
}
```

### Arquitectura de Archivos CSS

- `styles.css`: Estilos base, reset, variables globales, layout principal
- `productos.css`: Estilos específicos del catálogo, grid de productos, galerías
- `boletin.css`: Estilos de formularios, validación, estados de entrada
- `contacto.css`: Estilos de información de contacto, mapas, listas de datos

### Sistema Responsivo

Breakpoints definidos:

| Breakpoint | Rango | Descripción |
|------------|-------|-------------|
| Móvil pequeño | ≤ 360px | Smartphones antiguos |
| Móvil | ≤ 480px | Smartphones estándar |
| Tablet | ≤ 768px | Tablets y dispositivos medianos |
| Desktop | ≤ 1200px | Pantallas estándar |
| Desktop grande | ≥ 1400px | Pantallas amplias |

## Accesibilidad

### Estándares Implementados

El proyecto cumple con las pautas WCAG 2.1 Nivel AA:

- **Navegación por teclado**: Todos los elementos interactivos son accesibles mediante Tab
- **ARIA labels**: Etiquetas descriptivas en elementos sin texto visible
- **Contraste de color**: Ratio mínimo de 4.5:1 para texto normal
- **Semántica HTML**: Uso correcto de elementos HTML5 semánticos
- **Atributos alt**: Descripciones alternativas para todas las imágenes
- **Estructura jerárquica**: Orden lógico de encabezados (h1-h6)

### Características de Accesibilidad

```html
<!-- Ejemplo de navegación accesible -->
<nav aria-label="Navegación principal">
    <ul>
        <li><a href="#" aria-current="page">Inicio</a></li>
    </ul>
</nav>

<!-- Ejemplo de formulario accesible -->
<label for="email">Correo Electrónico</label>
<input type="email" id="email" name="email" required aria-required="true">
```

## Navegadores Compatibles

| Navegador | Versión Mínima | Estado |
|-----------|---------------|--------|
| Google Chrome | 90+ | Totalmente compatible |
| Mozilla Firefox | 88+ | Totalmente compatible |
| Safari | 14+ | Totalmente compatible |
| Microsoft Edge | 90+ | Totalmente compatible |
| Opera | 76+ | Totalmente compatible |

**Nota**: Internet Explorer no es compatible debido al uso de CSS Grid y Custom Properties.

## Optimización y Rendimiento

### Técnicas Implementadas

1. **Lazy Loading de Imágenes**
   ```html
   <img src="imagen.jpg" alt="Descripción" loading="lazy">
   ```

2. **Minificación CSS** (producción)
   ```bash
   # Ejemplo con cssnano
   npx cssnano styles.css styles.min.css
   ```

3. **CDN para Font Awesome**
   - Carga desde CDN de Cloudflare
   - Reduce el tamaño del proyecto
   - Mejora tiempos de carga mediante caché compartida

4. **Optimización de Selectores CSS**
   - Evitar selectores universales en cascada
   - Uso de clases específicas sobre selectores complejos
   - Minimizar profundidad de selectores

### Métricas de Rendimiento Objetivo

- First Contentful Paint (FCP): < 1.8s
- Time to Interactive (TTI): < 3.8s
- Total Blocking Time (TBT): < 300ms
- Cumulative Layout Shift (CLS): < 0.1

## Contribuciones

### Proceso de Contribución

1. Fork del repositorio
2. Crear una rama para la característica o corrección:
   ```bash
   git checkout -b feature/nueva-caracteristica
   ```
3. Realizar cambios siguiendo las convenciones del proyecto
4. Commit de los cambios con mensajes descriptivos:
   ```bash
   git commit -m "Add: Nueva funcionalidad de filtrado de productos"
   ```
5. Push a la rama:
   ```bash
   git push origin feature/nueva-caracteristica
   ```
6. Crear un Pull Request con descripción detallada

### Guía de Estilo

#### HTML

- Indentación: 4 espacios
- Atributos en minúsculas
- Comillas dobles para valores de atributos
- Estructura semántica HTML5
- Incluir atributos `alt` en todas las imágenes

#### CSS

- Indentación: 4 espacios
- Selectores en minúsculas con guiones (kebab-case)
- Un selector por línea en reglas múltiples
- Propiedades ordenadas alfabéticamente
- Comentarios para secciones principales

### Reportar Issues

Al reportar un problema, incluir:

- Descripción clara del problema
- Pasos para reproducir el error
- Navegador y versión utilizada
- Capturas de pantalla si es aplicable
- Código relevante o ejemplos

## Licencia

Este proyecto es parte de un portafolio. El código está disponible para propósitos de aprendizaje y demostración.

**Nota Legal**: Los nombres, logotipos e imágenes de videojuegos son propiedad de sus respectivos titulares y se utilizan únicamente con fines educativos y de demostración.

## Autor

**Saray Ortiz Cordero**

Proyecto desarrollado como parte del aprendizaje en desarrollo web frontend, demostrando competencias en HTML5, CSS3, diseño responsivo, accesibilidad web y mejores prácticas de desarrollo.

---

**Versión**: 1.0.0  
**Última actualización**: Octubre 2025  
**Estado del proyecto**: Activo - En desarrollo continuo

