# ernesto.github.io

Portfolio / CV web personal. HTML + CSS + JS puro, sin dependencias de build.

## 🚀 Deploy en GitHub Pages

### 1. Crear el repositorio

El repositorio **debe** llamarse `TU_USUARIO.github.io` para que GitHub Pages
lo sirva en la raíz de tu dominio.

```bash
# Clona este proyecto y cambia el remote
git clone <este-repo>
cd cv-ernesto

# Conecta con tu repo de GitHub
git remote set-url origin https://github.com/TU_USUARIO/TU_USUARIO.github.io.git
git push -u origin main
```

### 2. Activar GitHub Pages con Actions

En tu repositorio de GitHub:
1. Settings → Pages
2. Source → **GitHub Actions**
3. El workflow en `.github/workflows/deploy.yml` se encarga del resto

Cada `git push` a `main` desplegará automáticamente.

### 3. Personalizar antes de subir

Edita `index.html` y reemplaza estos placeholders:

| Placeholder | Reemplaza por |
|---|---|
| `TU_USUARIO` | Tu nombre de usuario de GitHub |
| `TU_REPO` | El nombre del repo de tu tienda backend |
| `tu@email.com` | Tu email real |
| `TU_ID` en Formspree | ID de tu form en formspree.io |
| URL de Railway | La URL de tu backend desplegado |

### 4. Dominio propio (opcional)

Si compras un dominio (ej: ernesto.dev):
1. Crea un archivo `CNAME` en la raíz con el dominio: `ernesto.dev`
2. En tu registrador (Namecheap, Cloudflare...) añade un CNAME: `www → TU_USUARIO.github.io`
3. En Settings → Pages activa "Enforce HTTPS"

## 📁 Estructura

```
.
├── index.html              # Todo el sitio (autocontenido)
├── README.md
└── .github/
    └── workflows/
        └── deploy.yml      # CI/CD automático
```

## ✏️ Personalización

### Cambiar colores

Las variables CSS están al inicio del `<style>`:

```css
:root {
  --accent:  #4f8ef7;  /* azul principal */
  --accent2: #1ed99a;  /* verde (activo/live) */
  --accent3: #f7874f;  /* naranja (WIP) */
}
```

### Añadir proyectos

Copia y pega un bloque `.project-card` en la sección `#proyectos`.
Cambia la clase del thumb (`.blue`, `.green`, `.orange`, `.purple`) para el color.

### Actualizar experiencia

Edita los `.exp-item` en la sección `#experiencia`.
Añade la clase `active` al más reciente para el efecto de punto verde.

## 🔧 Stack

- **Frontend**: HTML5 + CSS3 + Vanilla JS (sin frameworks, sin build)
- **Fuentes**: DM Serif Display + DM Sans + DM Mono (Google Fonts)
- **Deploy**: GitHub Pages + GitHub Actions
- **Formulario**: Formspree (tier gratuito)
- **Backend demo**: Railway (tu Spring Boot dockerizado)
