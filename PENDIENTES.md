# Pendientes del portafolio

Lista de lo que queda por hacer. Última actualización: 2026-10-15.

## 1. Integrar la IA (Ollama)
- Ya hay una ventana **🤖 Asistente IA** lista como placeholder (`#w-ia` en `index.html`).
- Falta conectarla a un modelo local en **Ollama** para que responda sobre proyectos, labs y experiencia.
- Nota técnica: GitHub Pages es **solo estático**, no ejecuta Ollama. Para que funcione en línea hace falta
  una de estas opciones:
  - Un backend propio (p. ej. un pequeño servidor Node/Python que hable con Ollama) accesible por HTTPS.
  - Un túnel al equipo donde corre Ollama (Cloudflare Tunnel, ngrok, etc.).
  - Dejarla funcionando solo en local para demos.
- Dónde tocar: el bloque `#w-ia` (HTML) y agregar la lógica de chat en el `<script>`.

## 2. Cambiar el cielo / fondo del escritorio
- El fondo actual es un degradado de cielo + pradera generado por CSS (clase `.desktop`, `.hills`, `.flowers`).
- Se quiere reemplazar por otro fondo (imagen o un diseño distinto).
- Dónde tocar: la regla `.desktop { background: ... }` y los elementos `.hills` (SVG) y `.flowers` en `index.html`.

## 3. Enlace de la comunidad (opcional)
- La ventana **👥 Comunidad** menciona que es una comunidad de WhatsApp, sin publicar el enlace.
- Si en el futuro se quiere activar el botón de unirse, poner la URL en la constante `COMUNIDAD_URL`
  dentro del `<script>` de `index.html`.

---

## Ramas del repositorio
- `main` — versión actual (diseño estilo Windows). Es la que se publica.
- `diseno-retro` — misma versión de Windows (rama de trabajo).
- `diseno-plano` — diseño anterior tipo "plano azul", por si se quiere volver a él.
