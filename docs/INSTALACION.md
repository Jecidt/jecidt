# Instalación — Perfil Archivo Gotham de Jecidt

Repositorio especial del perfil: https://github.com/Jecidt/jecidt

## 1. Subir los archivos del perfil

1. Descarga el ZIP y usa **Extraer todo**.
2. Abre la carpeta `jecidt_gotham_profile` extraída.
3. Entra en https://github.com/Jecidt/jecidt.
4. Pulsa **Add file → Upload files**.
5. Arrastra el contenido de la carpeta, incluyendo `README.md`, `assets/`, `.github/` y `docs/`. No subas una carpeta contenedora adicional dentro del repositorio.
6. Asegúrate de reemplazar el `README.md` antiguo por el nuevo y pulsa **Commit changes**.

Si el navegador no conserva la estructura de carpetas, usa GitHub Desktop: clona `Jecidt/jecidt`, copia los archivos de esta carpeta dentro de la carpeta local del repositorio, revisa los cambios y haz commit + push.

## 2. Activar la serpiente animada de contribuciones

1. Dentro de `Jecidt/jecidt`, abre **Settings → Actions → General**.
2. En **Workflow permissions**, elige **Read and write permissions** y guarda. Si la opción está bloqueada, la política del repositorio debe permitirla.
3. Abre **Actions → Actualizar serpiente de contribuciones**.
4. Pulsa **Run workflow** para la primera ejecución. Espera a que termine en verde.
5. La ejecución publica los SVG en la rama `output`; el README los carga desde esa rama. También se intenta actualizar a diario.

## 3. Si la serpiente no aparece

- Confirma que el flujo terminó correctamente en la pestaña **Actions**.
- Comprueba que exista la rama `output`.
- Prueba estas direcciones después de la primera ejecución:
  - https://raw.githubusercontent.com/Jecidt/jecidt/output/github-contribution-grid-snake-dark.svg
  - https://raw.githubusercontent.com/Jecidt/jecidt/output/github-contribution-grid-snake.svg
- Espera un par de minutos y recarga el perfil con `Ctrl + F5`.

## 4. Portada para compartir

El archivo `assets/gotham-social-preview.png` se puede seleccionar en **Settings → Social preview** para que el repositorio tenga una vista previa cuidada al compartirlo. Es una configuración aparte del README.

## Importante

- No hace falta crear otro repositorio: `Jecidt/jecidt` es el repositorio especial del perfil.
- No borres `.github/workflows/snake.yml`; automatiza la generación de la serpiente.
- El banner y el emblema animado son recursos locales; no dependen de servicios externos.
- Algunas imágenes SVG usan animaciones SVG. El banner y el logo GIF son las animaciones de respaldo para la parte visual.
