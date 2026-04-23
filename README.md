# Plantilla LaTeX para Proyectos Académicos

Esta es una plantilla de LaTeX diseñada para escribir papers y proyectos académicos estructurados, específicamente orientada a estudiantes de la **Facultad de Ciencias Naturales y Exactas**, **Departamento de Ciencias de la Computación**.

## Características

- **Portada Personalizada:** Diseñada con una imagen transversal que ocupa un poco menos de la mitad superior de la página y contiene la información de la facultad y autora en la mitad inferior.
- **Estructura Lista para Usar:** Incluye apartados de `Resumen`, `Abstract`, `Índice general`, `Desarrollo` y `Conclusiones`.
- **Manejo de Bibliografía Básico:** Incluye una sección de referencias básica, lista para ser extendida.
- **Fácil de Modificar:** Código comentado para que sepas qué cambiar.

## ¿Cómo usar esta plantilla?

**1. Instalar LaTeX en tu sistema:**
   - Si usas Linux (Ubuntu/Debian): `sudo apt install texlive-full`
   - O puedes usar plataformas online como [Overleaf](https://www.overleaf.com), simplemente subiendo todos los archivos de esta carpeta.

**2. Configurar la Imagen de la Portada:**
   - Coloca tu imagen en el mismo directorio que este archivo.
   - Renómbrala a `uo-big.png` **O** cambia el nombre de la imagen en el archivo [`utem.tex`](utem.tex) en la línea que dice:
     ```latex
     \includegraphics[width=\paperwidth,height=0.45\textheight,keepaspectratio=false]{uo-big.png}
     ```

**3. Modificar la Información Personal:**
   - Abre [`utem.tex`](utem.tex).
   - Busca la sección `PORTADA` (al inicio del documento después de `\begin{document}`).
   - Cambia `[Tu Nombre Aquí]` por tu nombre real.
   - Cambia `Título de tu Proyecto o Paper` por el título oficial.

**4. Escribir tu contenido:**
   - Empieza a rellenar las secciones de `\chapter*{Resumen}`, `\chapter{Desarrollo}`, etc., de acuerdo a las necesidades de tu trabajo.
   - Puedes crear nuevas secciones dentro de los capítulos usando el comando `\section{Nombre de tu sección}`.

**5. Compilar el documento:**
   - Si estás en tu terminal, puedes generar el PDF corriendo el siguiente comando:
     ```bash
     pdflatex utem.tex
     ```
   - Nota: Ejecuta este comando **dos veces** consecutivas para que el Índice de contenidos numere correctamente las páginas y detecte todas las referencias.

¡Mucho éxito con tu paper!

## ¿Por qué usar LaTeX y BibTeX?

**LaTeX** es un sistema de preparación de documentos de alta calidad construido para la academia y la ciencia. A diferencia de procesadores de texto habituales (como Word), en LaTeX escribes texto en plano acompañado de comandos de formato. ¿Por qué deberías usarlo?
- **Estética profesional inigualable:** Produce documentos con una tipografía y organización impecables, siendo el estándar de oro para fórmulas matemáticas y proyectos científicos.
- **Enfoque en lo que importa:** Te concentras únicamente en tu contenido; LaTeX se encarga automáticamente del diseño, los saltos de página, márgenes y alineaciones.
- **Estabilidad sin sorpresas:** Maneja índices, referencias cruzadas y cientos de páginas sin volverse lento, colgarse o desconfigurar tus imágenes al agregar un salto de línea.

**BibTeX** es el sistema compañero de LaTeX para manejar la bibliografía. En lugar de escribir cada fuente manualmente, guardas tus fuentes en un archivo `.bib` (muchos sitios web como Google Scholar te dan el código BibTeX listo para copiar y pegar) y este genera automáticamente todas las citas y la bibliografía de tu documento en el formato adecuado (APA, IEEE, etc.).

## ¿Dónde editar tus archivos?

Al estar basado en texto, puedes editar los archivos de varias maneras:
- **[Overleaf](https://www.overleaf.com/) (La opción más fácil):** Es un editor online colaborativo (como un Google Docs para LaTeX). No necesitas instalar nada; creas tu cuenta, subes esta carpeta y estás listo para empezar.
- **Visual Studio Code:** Usando la extensión *LaTeX Workshop*, es ideal si ya estás familiarizado con la programación y quieres mantener todo en un solo editor.
- **Editores de Escritorio Dedicados:** Programas como [TeXstudio](https://www.texstudio.org/) o [TeXmaker](https://www.xm1math.net/texmaker/) están construidos específicamente para LaTeX e incluyen atajos y autocompletado nativo.

## ¿Dónde aprender más?

Si quieres dominar LaTeX, estos sitios son excelentes puntos de partida:
1. [Learn LaTeX in 30 minutes de Overleaf](https://www.overleaf.com/learn/latex/Learn_LaTeX_in_30_minutes): El mejor tutorial express para arrancar desde cero.
2. [Documentación de Overleaf](https://www.overleaf.com/learn): Una enciclopedia masiva; si no sabes cómo hacer una tabla o insertar una imagen, la respuesta está aquí.
3. [LaTeX-Tutorial.com](https://www.latex-tutorial.com/): Guías prácticas y visuales muy amigables para todo nivel.
