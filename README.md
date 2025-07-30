# Despliegue a Cloudflare Pages

## Comandos para guardar y publicar cambios

```bash
# 1. Agrega todos los cambios al área de staging (prepara archivos para commit)
git add .

# 2. Crea un commit con un mensaje que describa los cambios realizados
git commit -m "Actualización de archivos del sitio web"

# 3. Envía (push) los commits al repositorio remoto en GitHub (opcional si usas GitHub)
git push origin main

# ---------------------------------------------------------------
# Si NO usas GitHub y quieres subir directamente desde tu máquina local:
# ---------------------------------------------------------------

# 4. Publica (sube) todos los archivos del directorio actual a Cloudflare Pages,
#    indicando el nombre del proyecto en Pages
wrangler pages publish . --project-name lavadorasplayancha

# 5. Opcional: Simula la publicación para verificar qué archivos se subirían,
#    sin hacer cambios reales en el sitio web
wrangler pages publish . --project-name lavadorasplayancha --dry-run

# 6. Verifica tu identidad y token configurado en Wrangler
wrangler whoami

# 7. (Solo la primera vez) Configura wrangler para usar un nuevo API token de Cloudflare
wrangler config
