# Portafolio Profesional

Este es un sitio web de portafolio moderno, rápido y optimizado para SEO, construido con las últimas tecnologías web. Fue diseñado para ser fácilmente personalizable y escalable.

## 🛠️ Tecnologías Utilizadas

Este proyecto utiliza un stack moderno para garantizar el mejor rendimiento y experiencia de desarrollador:

-   **[Astro 5](https://astro.build/)**: Framework web para sitios orientados a contenido. Genera HTML estático por defecto (cero JavaScript innecesario), lo que lo hace extremadamente rápido.
-   **[Tailwind CSS 4](https://tailwindcss.com/)**: Framework de utilidades CSS para un diseño rápido y responsivo. La versión 4 usa el nuevo motor de compilación (Vite) para un rendimiento instantáneo.
-   **[TypeScript](https://www.typescriptlang.org/)**: Superset de JavaScript que añade tipos estáticos, ayudando a prevenir errores y mejorar la calidad del código.
-   **[Vite](https://vitejs.dev/)**: La herramienta de construcción que impulsa Astro, ofreciendo una experiencia de desarrollo ultra rápida.

## 📂 Estructura del Proyecto

Aquí tienes una guía rápida de los archivos y carpetas más importantes:

```text
/
├── public/              # Archivos estáticos (imágenes, favicon, robots.txt) que se sirven tal cual.
├── src/
│   ├── assets/          # Imágenes y recursos optimizados por Astro.
│   ├── components/      # Bloques de construcción reutilizables (Header, Footer, Projects, etc.).
│   ├── layouts/         # Plantillas base html (contienen el <head>, <body>, metatags globales).
│   ├── pages/           # Rutas del sitio. `index.astro` es la página de inicio.
│   ├── styles/          # Estilos globales CSS.
│   └── config.ts        # ⚙️ ARCHIVO DE CONFIGURACIÓN PRINCIPAL.
├── astro.config.mjs     # Configuración de Astro.
├── package.json         # Dependencias y scripts del proyecto.
└── README.md            # Este archivo.
```

## ⚙️ Configuración y Personalización

La mayor parte del contenido del sitio se puede editar desde un único archivo centralizado, sin necesidad de tocar el código HTML complejo.

### 1. Información General, Servicios y Proyectos
Edita el archivo **`src/config.ts`**.
Aquí encontrarás constantes como `SITE_CONFIG`, `SERVICES` y `PROJECTS`.

*   **`SITE_CONFIG`**: Cambia tu nombre, email, teléfono de WhatsApp y descripción SEO.
*   **`SERVICES`**: Añade, elimina o modifica los servicios que ofreces.
*   **`PROJECTS`**: Gestiona tus proyectos mostrados. Cada proyecto incluye título, descripción, etiquetas (tags) y detalles para el modal/popup.

### 2. Estructura de la Página
Si quieres cambiar el orden de las secciones o añadir nuevas, edita **`src/pages/index.astro`**.
Este archivo actúa como el "lienzo" donde se importan y colocan los componentes.

```astro
<!-- Ejemplo de src/pages/index.astro -->
<Layout>
    <Hero />
    <Services />
    <Projects />
    <About />
    <Contact />
</Layout>
```

### 3. Estilos y Colores
El diseño usa **Tailwind CSS**. Los estilos globales están en `src/styles/global.css`.
Para cambios específicos de diseño, puedes editar las clases de Tailwind directamente en los archivos de componentes (`src/components/*.astro`).

## 🚀 Comandos

Todo se ejecuta desde la terminal en la raíz del proyecto.

| Comando | Acción |
| :--- | :--- |
| `npm run dev` | **Iniciar servidor de desarrollo**. Abre el sitio en `localhost:4321` y se actualiza al guardar cambios. |
| `npm run build` | **Construir para producción**. Genera los archivos finales en la carpeta `dist/`. |
| `npm run preview` | **Previsualizar producción**. Sirve la carpeta `dist/` localmente para verificar la build final. |

## 🌍 Despliegue (Hosting)

Al ser un sitio estático, puedes alojarlo **gratis** en plataformas modernas. Las mejores opciones son:

### Opción 1: Netlify (Recomendado)
Es la forma más sencilla.
1.  Sube este proyecto a tu GitHub.
2.  Entra en [netlify.com](https://www.netlify.com/) y crea una cuenta.
3.  Haz clic en "Add new site" > "Import from Git".
4.  Selecciona tu repositorio.
5.  Netlify detectará automáticamente Astro. Dale a **Deploy**.
6.  ¡Listo! Tu web estará online en segundos.

### Opción 2: Vercel
Similar a Netlify, muy rápido.
1.  Sube tu proyecto a GitHub.
2.  Entra en [vercel.com](https://vercel.com/).
3.  Importa tu repositorio.
4.  Vercel detectará Astro. Dale a **Deploy**.

## 🧐 ¿Por qué Astro?

A diferencia de React o Next.js (que envían mucho JavaScript al navegador), Astro elimina automáticamente todo el JavaScript que no es esencial para la interacción. Esto resulta en:
1.  **Carga instantánea**: Mejor SEO y retención de usuarios.
2.  **Menor consumo de datos**: Ideal para dispositivos móviles.
3.  **Simplicidad**: Escribes HTML/CSS/JS estándar con superpoderes.
