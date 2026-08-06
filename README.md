# Portafolio — James Steven Velásquez Vásquez

Página de portafolio construida en HTML/CSS/JS puro (sin frameworks), lista para
publicarse gratis en **GitHub Pages**.

## Estructura del proyecto

```
portafolio/
├── index.html              ← la página completa (diseño + contenido + interactividad)
├── README.md                ← este archivo
└── assets/
    ├── LEEME-foto.txt       ← instrucciones para tu foto de perfil
    └── proyectos/
        └── LEEME.txt        ← instrucciones para las imágenes de tus proyectos
```

## 1. Agregar tu foto de perfil

1. Copia tu foto dentro de la carpeta `assets/` con el nombre **`foto.jpg`**.
   (Si tu foto es `.png`, cambia `src="assets/foto.jpg"` por `src="assets/foto.png"`
   en `index.html`, dentro de la etiqueta `<img id="foto-img" ...>`).
2. Borra el archivo `assets/LEEME-foto.txt`, ya no lo necesitas.

> Truco: mientras trabajas, el botón "cambiar foto" dentro de la página te deja
> previsualizar una foto directamente en el navegador (se guarda solo en tu
> computadora). Para que la vean **todas** las personas que visiten tu página
> publicada, tiene que ser el archivo real `assets/foto.jpg`.

## 2. Agregar imágenes de tus proyectos (galería)

Tienes dos formas, y puedes combinarlas:

- **Rápida / de prueba:** en la pestaña "06 · Galería" de la página, usa el botón
  "Subir imágenes". Se guardan en tu navegador para que veas cómo luce la galería.
- **Permanente (recomendada):** copia tus imágenes dentro de `assets/proyectos/`
  y agrega su ruta en `index.html`, en el arreglo `IMAGENES_ESTATICAS` (búscalo
  con Ctrl+F). Ejemplo:

  ```js
  const IMAGENES_ESTATICAS = [
    'assets/proyectos/proyecto-1.jpg',
    'assets/proyectos/proyecto-2.jpg',
  ];
  ```

  Estas sí se ven para cualquier visitante de tu página publicada.

## 3. Editar contenido, colores o textos

Todo el contenido (perfil, formación, experiencia, certificaciones, etc.) está
directamente en `index.html`, organizado por secciones con comentarios `<!-- ... -->`.
Los colores y fuentes están centralizados al inicio del archivo, dentro de
`:root { ... }`.

## 4. Ver la página en tu computadora antes de subirla

Simplemente abre `index.html` haciendo doble clic, o arrástralo a tu navegador.

## 5. Subir el proyecto a GitHub y publicarlo con GitHub Pages

Instala Git si no lo tienes (https://git-scm.com/downloads) y crea una cuenta en
GitHub (https://github.com) si aún no tienes una.

### a) Crear el repositorio en GitHub

1. Entra a https://github.com/new
2. Ponle un nombre, por ejemplo `portafolio` (puede ser cualquier nombre).
3. Déjalo en **Public**.
4. NO marques "Add a README" (ya tienes uno). Clic en **Create repository**.
5. Copia la URL que te da GitHub, algo como:
   `https://github.com/TU-USUARIO/portafolio.git`

### b) Subir el proyecto desde tu computadora

Abre una terminal dentro de la carpeta `portafolio/` (donde está `index.html`)
y ejecuta, en orden:

```bash
git init
git add .
git commit -m "Primera versión de mi portafolio"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/portafolio.git
git push -u origin main
```

Reemplaza `TU-USUARIO` por tu usuario real de GitHub. Si es la primera vez que
usas Git en esa computadora, antes de todo esto ejecuta una sola vez:

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu-correo@ejemplo.com"
```

### c) Activar GitHub Pages

1. En tu repositorio en GitHub, ve a **Settings → Pages**.
2. En "Branch", elige `main` y la carpeta `/ (root)`. Clic en **Save**.
3. Espera 1-2 minutos. Tu página quedará publicada en:
   `https://TU-USUARIO.github.io/portafolio/`

### d) Subir cambios futuros

Cada vez que edites algo (foto, proyectos, textos) y quieras actualizar la
página publicada:

```bash
git add .
git commit -m "Describe aquí qué cambiaste"
git push
```

Para más detalle sobre cada comando de Git, revisa el PDF de comandos que te
entregué junto con este proyecto.
