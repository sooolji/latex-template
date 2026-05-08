# Plantilla LaTeX

Esta es una plantilla base para trabajos académicos en LaTeX. Está pensada para informes, proyectos y documentos universitarios que necesitan una portada cuidada, una estructura simple y un punto de entrada fácil de editar.

La idea es que puedas empezar rápido, mantener el documento ordenado y reutilizar la misma identidad visual en el documento corto y en la variante de tesis.

## Qué trae

- Portada reutilizable para el documento del root.
- Variante de tesis organizada por carpetas.
- Estructura básica de contenido en español.
- Estilo preparado para adaptar logos, datos institucionales y metadatos.

## Estructura

- `template.tex`: entrada principal del documento corto.
- `cover.tex`: define la portada del root y reutiliza el layout compartido.
- `thesis/template/Thesis.tex`: entrada principal de la plantilla de tesis.
- `thesis/template/thesis.cls`: clase que construye la portada y define comandos de la tesis.
- `thesis/template/cover-layout.tex`: diseño compartido de portada usado por ambas variantes.
- `thesis/template/FrontMatter/`: resumen, agradecimientos, dedicatoria, opinión del tutor e índice.
- `thesis/template/MainMatter/`: capítulos principales del trabajo.
- `thesis/template/BackMatter/`: conclusiones, recomendaciones y bibliografía.
- `thesis/template/Graphics/`: logos, imágenes y recursos visuales.

## Cómo funciona la portada

La portada no se arma a mano dentro del documento principal.

- En el root, `template.tex` carga `cover.tex`, y `cover.tex` llama al layout compartido.
- En la tesis, `Thesis.tex` define los metadatos y deja que `\maketitle` construya la portada desde `thesis.cls`.
- El archivo común `thesis/template/cover-layout.tex` mantiene el mismo lenguaje visual en ambos casos.

Eso te permite cambiar la composición una sola vez y reflejarla en las dos variantes.

## Qué puedes cambiar

Puedes adaptar sin tocar la estructura general:

- logo principal y fondo de portada;
- nombre de facultad, carrera o tutor;
- título, subtítulo y datos del autor;
- colores y distribución de la portada;
- capítulos, secciones y contenido interno.

## Plantilla de tesis

La tesis vive en `thesis/template/` y está pensada como una plantilla más larga y modular. La compilación de esa versión debe hacerse desde `thesis/template/Thesis.tex`.

Cada archivo del árbol tiene una función concreta: `FrontMatter` contiene las secciones preliminares, `MainMatter` agrupa los capítulos, `BackMatter` cierra el documento con conclusiones y bibliografía, y `Graphics` guarda los recursos visuales.

## Bibliografía

La variante del root usa bibliografía manual en `thebibliography`, así que sirve bien para documentos cortos o prototipos.

Si el documento va a crecer, lo recomendable es migrar la bibliografía a un flujo automático con `.bib` y BibTeX o BibLaTeX.

## Recomendación de uso

1. Edita `template.tex` si vas a trabajar el documento corto.
2. Edita `thesis/template/Thesis.tex` si vas a trabajar la tesis.
3. Cambia logos, nombres y portada en el layout compartido cuando quieras mantener ambas versiones sincronizadas.
4. Compila seguido para detectar errores de estructura, referencias o imágenes temprano.

## Editor

Puedes usar la herramienta que te resulte más cómoda:

- Overleaf para colaboración rápida.
- VS Code con LaTeX Workshop si trabajas con Git.
- TeXstudio o TeXmaker si prefieres un entorno de escritorio clásico.

## Recursos útiles

- [Overleaf: Learn LaTeX in 30 minutes](https://www.overleaf.com/learn/latex/Learn_LaTeX_in_30_minutes)
- [Documentación de Overleaf](https://www.overleaf.com/learn)
- [LaTeX-Tutorial.com](https://www.latex-tutorial.com/)
