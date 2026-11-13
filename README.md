# Beautiful Decor

Mod de decoración para **Minecraft 1.20.1** / **Forge 47.4.5**.

Versión actual del proyecto: **6.16.1**

## Compilación automática con GitHub Actions

Este repositorio tiene configurado un workflow de **GitHub Actions** que:

1. Compila el mod con Gradle + ForgeGradle en cada push a `main` o cuando se dispara manualmente.
2. Sube el `.jar` como artifact.
3. **Publica automáticamente un Release** en GitHub cuando se crea un tag que empiece por `v` (ejemplo: `v6.16.1`).

### Cómo publicar una nueva versión

1. Sube el código fuente completo del mod a este repositorio (todo el contenido de la carpeta `BeautifulDecor/`, incluyendo `src/`, `gradle/`, `gradlew`, etc.).
2. Crea un tag:
   ```bash
   git tag v6.16.1
   git push origin v6.16.1
   ```
3. El workflow se ejecutará y creará el Release con el jar compilado.

También puedes disparar el workflow manualmente desde la pestaña **Actions**.

### Requisitos locales para compilar

- JDK 17
- Ejecutar `./gradlew build`

El jar resultante estará en `build/libs/`.

---

Autor: Santiago
