# Cómo publicar el formulario online

Seguí estos pasos una sola vez. Después el formulario queda online para siempre.

---

## Paso 1 — Configurar EmailJS (el que manda el mail)

1. Entrá a **https://www.emailjs.com** → Create Account (gratis)
2. Iniciá sesión con tu Gmail ``
3. Ir a **Email Services** → Add New Service → seleccioná **Gmail**
4. Autorizá con tu cuenta → copiá el **Service ID** (ej: `service_abc123`)
5. Ir a **Email Templates** → Create New Template
6. Completá así:
   - **To:** ``
   - **Subject:** `Nueva empresa: {{empresa}}`
   - **Body:** `{{cuerpo}}`
7. Guardá → copiá el **Template ID** (ej: `template_xyz789`)
8. Ir a **Account** → copiá tu **Public Key** (ej: `user_XXXXXXXXX`)

---

## Paso 2 — Pegar tus claves en el formulario

Abrí el archivo `index.html` con el Bloc de notas y buscá estas 3 líneas al final:

```
const EMAILJS_PUBLIC_KEY  = "TU_PUBLIC_KEY";
const EMAILJS_SERVICE_ID  = "TU_SERVICE_ID";
const EMAILJS_TEMPLATE_ID = "TU_TEMPLATE_ID";
```

Reemplazá los valores con los que copiaste en el Paso 1. Guardá el archivo.

---

## Paso 3 — Subir a GitHub

1. Entrá a **https://github.com** con tu cuenta (``)
2. Clic en **New repository**
   - Nombre: `unipase-alta`
   - Visibilidad: **Public**
   - Clic en **Create repository**
3. Subí el archivo `index.html`:
   - En la página del repo → **Add file** → **Upload files**
   - Arrastrá el `index.html` → **Commit changes**

---

## Paso 4 — Publicar con Vercel

1. Entrá a **https://vercel.com** → Sign up with GitHub
2. Clic en **Add New Project**
3. Seleccioná el repo `unipase-alta`
4. Dejá todo por defecto → **Deploy**
5. En menos de 1 minuto te da el link, algo como:
   `https://unipase-alta.vercel.app`

¡Listo! Ese es el link que le das a los encargados de cuenta.

---

## Cómo funciona después

- Los encargados entran al link, completan el formulario y hacen clic en "Enviar datos"
- A vos te llega un mail a `` con todos los datos
- Copiás el texto del mail y lo pegás en el bot (pestaña "Importar texto")
- Hacés clic en "Importar al formulario" → revisás → Llenar Empresa → Llenar Punto
