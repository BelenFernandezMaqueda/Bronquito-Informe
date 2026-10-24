# Informe en LaTeX

## Puesta en marcha (lo hace una sola persona)

1. Crear una cuenta en GitHub (si no tienen) y un repositorio nuevo, por ejemplo `informe`. Puede ser privado.
2. Subir todos los archivos de esta carpeta: en el repositorio vacío, "uploading an existing file" y arrastrarlos.
   La carpeta `.github` tiene que quedar incluida (en Mac/Linux es oculta: con Cmd+Shift+. se ve en Finder).
3. Ir a **Settings → Collaborators → Add people** y sumar a los otros dos.

## Cómo trabaja cada uno

### Opción A: en el navegador, sin instalar nada (Codespaces)
1. En el repositorio: botón verde **Code → Codespaces → Create codespace on main**.
2. La primera vez tarda varios minutos (baja LaTeX completo). Después abre rápido.
3. Abrir `main.tex` y guardar (Ctrl+S): se compila solo. El ícono "View LaTeX PDF" muestra el PDF.
4. Al terminar, en el panel **Source Control** (ícono de ramitas): escribir un mensaje, **Commit**, y después **Sync Changes**.
5. Cerrar o detener el codespace cuando no lo usen para no gastar las horas gratis.

### Opción B: en la compu
1. Instalar LaTeX: MiKTeX (Windows), MacTeX (Mac) o TeX Live (Linux).
2. Instalar VS Code y la extensión **LaTeX Workshop**.
3. En VS Code: **Clone Git Repository** y pegar la URL del repositorio.
4. Mismo flujo: guardar compila, y Commit + Sync para compartir.

## Reglas para no pisarse

- **Antes de empezar: Sync / Pull** para bajar lo que hicieron los demás.
- Cada uno trabaja en **su archivo** dentro de `secciones/`.
- **Una oración por línea.**
- Commits chicos y seguidos, no uno gigante al final.
- Si aparece un conflicto, VS Code muestra las dos versiones: elegir "Accept Current", "Accept Incoming" o "Accept Both".

## Dónde está el PDF final

Cada vez que alguien sube cambios, GitHub compila solo.
Pestaña **Actions** → la última ejecución → abajo, en **Artifacts**, descargar `informe-pdf`.
Si sale una cruz roja, hay un error de LaTeX: hacer clic para ver el log.

## Agregar cosas

- **Nueva sección:** crear `secciones/nombre.tex` y agregar `\input{secciones/nombre}` en `main.tex`.
- **Imágenes:** guardarlas en `figuras/` y usar `\includegraphics{nombre.png}`.
- **Bibliografía:** agregar entradas en `referencias.bib` (Google Scholar → Citar → BibTeX) y citar con `\cite{clave}`.
