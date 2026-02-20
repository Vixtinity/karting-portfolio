# 🏎️ Karting Portfolio — Marco Rodríguez

Portfolio profesional para piloto de karting, construido con **Astro**.

## 🚀 Inicio rápido

```bash
# Instalar dependencias
npm install

# Servidor de desarrollo
npm run dev

# Build para producción
npm run build

# Preview del build
npm run preview
```

El sitio estará en `http://localhost:4321`

## 📁 Estructura

```
src/
├── components/
│   ├── Nav.astro          # Navegación sticky
│   ├── Hero.astro         # Sección principal con stats
│   ├── About.astro        # Sobre mí + habilidades
│   ├── Seasons.astro      # Temporadas + resultados
│   ├── Achievements.astro # Logros + línea del tiempo
│   ├── Gallery.astro      # Galería de fotos/vídeos
│   └── Contact.astro      # Formulario + footer
├── layouts/
│   └── Layout.astro       # Layout base con fuentes
├── pages/
│   └── index.astro        # Página principal
└── styles/
    └── global.css         # Variables y estilos base
```

## ✏️ Personalización

- **Nombre y número**: Cambia "Marco Rodríguez" y "#11" en los componentes
- **Estadísticas**: Edita los datos en `Hero.astro` y `About.astro`
- **Temporadas**: Modifica el array `seasons` en `Seasons.astro`
- **Logros**: Edita `trophies` y `timeline` en `Achievements.astro`
- **Fotos**: Reemplaza los placeholder cards en `Gallery.astro` con `<img>` reales
- **Colores**: Variables CSS en `global.css` (`--red`, `--yellow`)
- **Email**: Actualiza en `Contact.astro`

## 🎨 Diseño

- Paleta: Negro profundo, Rojo Ferrari, Amarillo bandera
- Tipografía: Barlow Condensed (titulares) + Rajdhani (texto)
- Animaciones CSS puras, sin dependencias JS externas
- Totalmente responsive

## 🌐 Deploy

Compatible con Netlify, Vercel, Cloudflare Pages:
```bash
npm run build
# Sube la carpeta /dist
```
