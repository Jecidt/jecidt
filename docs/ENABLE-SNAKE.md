# Activar la serpiente de contribuciones

El workflow `.github/workflows/snake.yml` genera dos SVG y los publica en la rama `output` del mismo repositorio.

1. Sube todos los archivos de este paquete a `Jecidt/jecidt`, respetando las carpetas.
2. En GitHub, abre **Settings → Actions → General** y confirma que los workflows están habilitados.
3. En la sección de permisos del workflow, permite escritura de contenidos si la política del repositorio lo exige.
4. Abre **Actions → Generate contribution snake → Run workflow** y ejecuta el workflow manualmente.
5. Comprueba que el workflow termina en verde y que existe la rama `output` con los SVG.
6. Recarga el README del perfil. El primer render puede tardar unos minutos.

Si falla, abre el run en Actions y revisa el paso que aparece en rojo. Las políticas de una organización pueden impedir permisos de escritura incluso si el workflow los solicita. No guardes tokens personales dentro del README.
