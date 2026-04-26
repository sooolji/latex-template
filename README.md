# Plantilla LaTeX

Esta plantilla nació para tener un **prototipo rápido** con el que puedas empezar a escribir trabajos universitarios sin pelearte con el formato desde el día uno.

Está orientada a informes, papers y proyectos académicos (especialmente en Ciencias de la Computación), con portada institucional, estructura base y bibliografía.

---

## ¿Qué incluye esta plantilla?

- Portada con identidad visual institucional.
- Estructura inicial del documento:
  - Resumen
  - Abstract
  - Índice
  - Introducción
  - Desarrollo
  - Conclusiones
  - Bibliografía
- Configuración de idioma en español.
- Márgenes y formato académico base.
- Archivo `.bib` para referencias (listo para usar si decides migrar a BibTeX).

---

## Importante: bibliografía por defecto vs recomendación

Actualmente, el template viene por defecto con bibliografía manual usando `thebibliography` (es decir, **sin `bibitem` predefinidos ni gestión automática**).

Eso te permite arrancar rápido, pero para trabajos serios y medianos/grandes te recomiendo fuertemente usar **BibTeX** (o biblatex/biber).

### ¿Por qué te invito a usar BibTeX?

Porque te evita errores y trabajo repetitivo:

- Centralizas tus fuentes en un solo archivo `.bib`.
- Reutilizas referencias entre varios documentos.
- Cambias de estilo (APA, IEEE, etc.) sin reescribir toda la bibliografía.
- Evitas inconsistencias en autores, años, títulos y formato de citas.
- Escala muchísimo mejor cuando tienes 10, 30 o 100+ referencias.

---

## Flujo recomendado con BibTeX

1. Guarda tus referencias en un archivo como `.bib/referencias.bib`.
2. Cita en el texto con claves, por ejemplo: `\cite{clave2024}`.
3. Genera la bibliografía automáticamente.

Ejemplo mínimo (si usas BibTeX clásico):

```latex-template/README.md#L1-8
\bibliographystyle{plain}   % o IEEEtran, apalike, etc.
\bibliography{.bib/referencias}
```

> Nota: para compilar con BibTeX normalmente se usa la secuencia:
> `pdflatex -> bibtex -> pdflatex -> pdflatex`

---

## Buenas prácticas (recomendadas desde el inicio)

### 1) Separa contenido de formato
- Evita meter estilos locales en cada párrafo.
- Define estructura y comandos reutilizables.

### 2) Cita siempre con clave, nunca “a mano”
- No escribas referencias completas en cada documento.
- Mantén tu `.bib` como fuente única de verdad.

### 3) Usa nombres claros para assets
- Imágenes: `figuras/arquitectura-general.png`
- Tablas y anexos con nombres semánticos.
- Evita `imagen1.png`, `final_final.png`, etc.

### 4) Mantén consistencia de estilo
- Una convención de títulos.
- Una convención para figuras/tablas.
- Un estilo de bibliografía coherente.

### 5) Compila frecuentemente
- Detecta errores temprano (llaves, referencias rotas, labels duplicados).
- No esperes al final para “arreglar todo”.

### 6) Control de versiones (Git)
- Commits pequeños y con mensajes claros.
- Ignora archivos temporales de compilación.
- Etiqueta versiones importantes (entrega parcial, versión final).

---

## Cómo manejar proyectos grandes en LaTeX

Cuando tu documento crezca (tesis, memoria, informe largo), no trabajes todo en un solo `.tex`.

### Estructura sugerida

```latex-template/README.md#L1-13
proyecto/
├── main.tex
├── .bib/
│   └── referencias.bib
├── capitulos/
│   ├── 01-introduccion.tex
│   ├── 02-marco-teorico.tex
│   ├── 03-metodologia.tex
│   └── 04-resultados.tex
├── figuras/
└── tablas/
```

### Recomendación de organización

- `main.tex` solo orquesta el documento.
- Cada capítulo vive en su archivo (`\input{}` o `\include{}`).
- Bibliografía centralizada en `.bib`.
- Figuras y tablas separadas por carpetas.
- Usa `\label{}` y `\ref{}` de forma sistemática.

### Ventajas reales

- Menos conflictos al trabajar en equipo.
- Navegación más rápida.
- Menor riesgo de romper todo al editar.
- Revisiones y correcciones más simples.

---

## ¿Dónde editar?

Puedes usar lo que te resulte más cómodo:

- **Overleaf** (rápido para empezar y colaborar).
- **VS Code + LaTeX Workshop** (ideal si ya trabajas con Git).
- **TeXstudio / TeXmaker** (entorno clásico de escritorio).

---

## Recursos útiles

- [Overleaf: Learn LaTeX in 30 minutes](https://www.overleaf.com/learn/latex/Learn_LaTeX_in_30_minutes)
- [Documentación de Overleaf](https://www.overleaf.com/learn)
- [LaTeX-Tutorial.com](https://www.latex-tutorial.com/)
