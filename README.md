# Don Marco Agency — Landing

Landing page estática de Don Marco Agency ("Tecnología que vende sola para turismo").

Sitio de una sola página (`index.html`), sin build step: usa Tailwind y Google Fonts vía CDN.

## Despliegue

El sitio se publica automáticamente en **GitHub Pages** mediante GitHub Actions
(`.github/workflows/deploy.yml`) en cada push a la rama `main`.

- **Dominio:** https://donmarco.ai (configurado vía el archivo `CNAME`)
- **URL de Pages:** https://donmarcoai.github.io/webpage/

### Desarrollo local

Al ser un sitio estático basta con abrir `index.html` en el navegador, o servirlo:

```bash
python3 -m http.server 8000
# luego abre http://localhost:8000
```

## Configuración de Pages (una sola vez)

En el repositorio `donmarcoai/webpage`:

1. **Settings → Pages → Source:** selecciona **GitHub Actions**.
2. **Settings → Pages → Custom domain:** escribe `donmarco.ai` y guarda.
3. Marca **Enforce HTTPS** cuando el certificado esté listo.

### DNS del dominio apex (`donmarco.ai`)

Crea estos registros **A** apuntando a las IPs de GitHub Pages:

```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

Y opcionalmente un registro **CNAME** para `www` → `donmarcoai.github.io`.
