# Guía de Autenticación con GitHub

## Problema

El push falló con el error:
```
remote: Permission to WILBIdon/dimanicas-EL-SENSEI.git denied to WILBIdon.
fatal: unable to access 'https://github.com/WILBIdon/dimanicas-EL-SENSEI.git/': The requested URL returned error: 403
```

Esto significa que necesitas autenticarte con GitHub para poder subir los archivos.

## Soluciones

### Opción 1: Usar Personal Access Token (Recomendada)

1. **Generar un Personal Access Token en GitHub:**
   - Ve a GitHub.com y inicia sesión
   - Haz clic en tu foto de perfil → Settings
   - En el menú izquierdo, ve a: Developer settings → Personal access tokens → Tokens (classic)
   - Clic en "Generate new token" → "Generate new token (classic)"
   - Dale un nombre descriptivo (ej: "Dinamicas El Sensei Deploy")
   - Selecciona los permisos: marca "repo" (esto incluye todo lo necesario)
   - Clic en "Generate token"
   - **IMPORTANTE**: Copia el token inmediatamente (solo se muestra una vez)

2. **Usar el token para hacer push:**
   ```bash
   cd "/Users/merkaorganico/Pagina El SEI"
   git push -u origin main
   ```
   - Cuando te pida credenciales:
     - Username: tu usuario de GitHub (WILBIdon)
     - Password: pega el Personal Access Token (no tu contraseña)

### Opción 2: Usar SSH (Más seguro a largo plazo)

1. **Generar una clave SSH (si no tienes una):**
   ```bash
   ssh-keygen -t ed25519 -C "soporte@dinamicaslyd.com"
   ```
   - Presiona Enter para aceptar la ubicación por defecto
   - Opcionalmente, ingresa una contraseña

2. **Añadir la clave SSH a GitHub:**
   ```bash
   cat ~/.ssh/id_ed25519.pub
   ```
   - Copia la salida
   - Ve a GitHub.com → Settings → SSH and GPG keys → New SSH key
   - Pega la clave y guarda

3. **Cambiar la URL del remoto a SSH:**
   ```bash
   cd "/Users/merkaorganico/Pagina El SEI"
   git remote set-url origin git@github.com:WILBIdon/dimanicas-EL-SENSEI.git
   git push -u origin main
   ```

### Opción 3: Usar GitHub CLI (gh)

1. **Instalar GitHub CLI (si no lo tienes):**
   ```bash
   brew install gh
   ```

2. **Autenticarte:**
   ```bash
   gh auth login
   ```
   - Sigue las instrucciones en pantalla

3. **Hacer push:**
   ```bash
   cd "/Users/merkaorganico/Pagina El SEI"
   git push -u origin main
   ```

## Estado Actual

✅ Repositorio Git inicializado
✅ Archivos añadidos y commiteados
✅ Remote configurado: https://github.com/WILBIdon/dimanicas-EL-SENSEI.git
✅ Branch renombrado a `main`
⏳ **PENDIENTE**: Push al repositorio (esperando autenticación)

## Después de Autenticar

Una vez que hayas completado la autenticación y el push sea exitoso, deberás:

1. **Configurar GitHub Pages:**
   - Ve a https://github.com/WILBIdon/dimanicas-EL-SENSEI/settings/pages
   - En "Source", selecciona "Deploy from a branch"
   - Selecciona la branch `main` y la carpeta `/ (root)`
   - Guarda los cambios
   - Espera 1-2 minutos

2. **Visitar tu sitio:**
   - URL: https://wilbidon.github.io/dimanicas-EL-SENSEI/

3. **Actualizar contenido pendiente:**
   - Añadir el logo (`Gemini_Generated_Image_k5araik5araik5ar.jpg`)
   - Actualizar los enlaces de WhatsApp en `index.html`
   - Hacer commit y push de los cambios
