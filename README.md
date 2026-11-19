# rey-midas

🔥 ABYSSAL HELLFIRE - PWA Metal Audio Engine | Cloudflare Edge + GitHub Actions + Web Audio DSP

Metal Music Hub: estructura profesional, mapa completo de 15 subgéneros de metal, arquitectura de plataforma y motor de audio metal, listo para Cloudflare Pages.

## Qué hay aquí

- `index.html` — Metal Music Hub completo: 8 módulos de arquitectura, flujo de plataforma, 15 subgéneros con buscador y filtros, y sección de despliegue.
- `wrangler.toml` — configuración de Cloudflare Pages (proyecto estático, sin build).
- `_headers` — cabeceras de seguridad y caché para Pages.
- `manifest.webmanifest` — manifiesto PWA.
- `.github/workflows/deploy-cloudflare-pages.yml` — despliegue a Cloudflare Pages con Wrangler en cada push a `main` (requiere los secretos `CLOUDFLARE_API_TOKEN` y `CLOUDFLARE_ACCOUNT_ID`).

## Despliegue en Cloudflare Pages (con iaabismalhellfire.net)

Opción recomendada, integración con Git:

1. En Cloudflare Dashboard → Workers & Pages → Create → Pages → Connect to Git.
2. Elige este repositorio `armandocampos19852020-jpg/rey-midas`, rama `main`.
3. Framework preset: None. Build command: (vacío). Build output directory: `.`
4. Deploy.
5. En Custom domains, agrega `iaabismalhellfire.net` (y `www.iaabismalhellfire.net` si lo quieres). Cloudflare crea el SSL automáticamente.

No se usa Vercel para este proyecto.

## Desarrollo local

Sirve la carpeta con cualquier servidor estático, por ejemplo:

```bash
python3 -m http.server 8000
```

Luego abre http://localhost:8000/
