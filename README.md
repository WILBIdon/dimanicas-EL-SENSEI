# Dinámicas El Sensei

Landing page para sorteos y dinámicas exclusivas a través de WhatsApp.

## 🎯 Descripción

Sitio web promocional para la comunidad "Dinámicas El Sensei", que ofrece sorteos diarios de premios en efectivo, tecnología y experiencias exclusivas. Los usuarios pueden unirse a través de un grupo de WhatsApp y participar en dinámicas transparentes y seguras.

## 🚀 Tecnologías

- **HTML5**: Estructura del sitio
- **Tailwind CSS**: Framework CSS (CDN)
- **Font Awesome**: Iconos (CDN)
- **Google Fonts**: Tipografías Montserrat y Playfair Display
- **JavaScript Vanilla**: Interacciones y funcionalidad

## 📦 Estructura del Proyecto

```
/
├── index.html          # Página principal
├── README.md           # Este archivo
└── .gitignore          # Archivos ignorados por git
```

## 🌐 Despliegue

Este sitio está desplegado en GitHub Pages:

**URL**: https://wilbidon.github.io/dimanicas-EL-SENSEI/

## ⚙️ Configuración

### Actualizar el enlace de WhatsApp

Para actualizar el enlace del grupo de WhatsApp, edita las siguientes líneas en `index.html`:

1. **Navbar (Desktop)** - Línea 98:
```html
<a href="https://chat.whatsapp.com/TU_ENLACE_AQUI" target="_blank" ...>
```

2. **Navbar (Mobile)** - Línea 118:
```html
<a href="https://chat.whatsapp.com/TU_ENLACE_AQUI" ...>
```

3. **Hero Section** - Línea 136:
```html
<a href="https://chat.whatsapp.com/TU_ENLACE_AQUI" target="_blank" ...>
```

4. **Call to Action** - Línea 291:
```html
<a href="https://chat.whatsapp.com/TU_ENLACE_AQUI" target="_blank" ...>
```

### Añadir el logo

El sitio espera un archivo de imagen llamado `Gemini_Generated_Image_k5araik5araik5ar.jpg` en la raíz del proyecto. 

Para añadir tu logo:
1. Coloca tu imagen en la raíz del proyecto
2. Actualiza la referencia en `index.html` (líneas 88 y 348) si usas un nombre diferente

## 📝 Secciones del Sitio

- **Hero**: Presentación principal con llamado a la acción
- **Video Promocional**: Sección para video explicativo (placeholder)
- **Ventajas**: Tres beneficios principales (Premios, Fácil, Seguro)
- **¿Cómo Funciona?**: Proceso en 4 pasos
- **Call to Action**: Invitación a unirse al grupo
- **FAQ**: Preguntas frecuentes con acordeones
- **Footer**: Información legal y contacto

## 📄 Legal

El sitio incluye modales con:
- Términos y Condiciones
- Política de Privacidad
- Tratamiento de Datos

## 🔧 Desarrollo Local

Para visualizar el sitio localmente:

1. Clona el repositorio:
```bash
git clone https://github.com/WILBIdon/dimanicas-EL-SENSEI.git
cd dimanicas-EL-SENSEI
```

2. Abre `index.html` en tu navegador:
```bash
open index.html
```

O usa un servidor local como Live Server (VS Code extension) o Python:
```bash
python -m http.server 8000
```

## 📧 Contacto

- Email: soporte@dinamicaslyd.com

## 📅 Última Actualización

Diciembre 2025

---

© 2025 Dinámicas El Sensei. Todos los derechos reservados.
