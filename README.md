# Mirror estático — Revista Conciencia Democrática

Snapshot diario del sitio principal en [conciencia-democratica.vercel.app](https://conciencia-democratica.vercel.app), generado por GitHub Actions y servido vía GitHub Pages como fallback de solo lectura si el sitio principal cae.

**Sitio espejo (cuando GH Pages esté activado)**:
👉 https://juanasca1998.github.io/conciencia-democratica-mirror/

## Cómo se genera

Workflow `.github/workflows/mirror.yml` corre diariamente:
1. Descarga páginas públicas estáticas/ISR vía el sitemap
2. Re-escribe links absolutos a relativos (para navegación interna)
3. Inyecta banner discreto avisando "versión mirror"
4. Deploya a GitHub Pages

No se mirroreran páginas dinámicas: `/admin/*`, `/api/*`, `/mi-cuenta`, `/login`. Esas requieren backend vivo.

## Para activar GitHub Pages

(One-time setup) → Repo Settings → **Pages** → Source: **GitHub Actions**.

Después el primer workflow run automáticamente publica el sitio.

## Por qué es público

GitHub Pages requiere repo público en la cuenta personal. El contenido mirrorea solo páginas que YA son públicas (artículos, autores, secciones públicas) — no hay info nueva expuesta.
