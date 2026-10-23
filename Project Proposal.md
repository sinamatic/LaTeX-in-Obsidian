# Scientific Writing in Obsidian with Markdown

## 1. Introduction and Motivation

Obsidian serves as my personal knowledge management system. It contains almost all of my notes and documentation, including daily notes, to-do lists, work documentation, customer meetings, tutorials, lecture summaries, and even vacation planning.

The main exception is scientific writing. For academic papers and theses, I currently use LaTeX in Visual Studio Code or Overleaf because my university provides templates that meet its formatting requirements.

However, this creates a separation between knowledge management and academic writing. For example, while working on my Bachelor's thesis, I documented research findings and project progress in Obsidian but had to manually transfer the relevant content into LaTeX. Furthermore, LaTeX source code is less intuitive to read and edit, as elements such as tables are only properly displayed after compilation. In contrast, Markdown provides a more readable editing experience, but the standard PDF export from Obsidian lacks the formatting quality required for academic documents.

## 2. Project Goal

The objective of this project is to investigate and develop a workflow for writing scientific documents directly in Obsidian using Markdown, while a separate typesetting system handles the document layout and formatting. The underlying concept is similar to the separation of content and presentation in HTML and CSS.

Ideally, the workflow should integrate into an existing Obsidian vault and provide reusable university-specific templates, such as an "Ohm Master Thesis" template. The intended transformation is illustrated below.

### Before: LaTeX in VS Code

```
Docu_EduK-AR-t/
├── content/
│   ├── 0_abstract.tex
│   ├── 1_intro.tex
│   ├── 2_background.tex
│   ├── 3_technology_selection.tex
│   ├── 5_implementation.tex
│   ├── 5-2_implementation.tex
│   ├── 5-3_implementation.tex
│   └── 6_evaluation.tex
├── figures/
├── cover.tex
├── glossary.tex
├── refs.bib
├── thesis.tex
└── thesis.pdf
```

### After: Markdown in Obsidian

```
templates/
├── Ohm Master Thesis
Docu_EduK-AR-t/
├── content/
│   ├── 0_abstract.md
│   ├── 1_intro.md
│   ├── 2_background.md
│   ├── 3_technology_selection.md
│   ├── 5_implementation.md
│   ├── 5-2_implementation.md
│   ├── 5-3_implementation.md
│   └── 6_evaluation.md
├── glossary.md
├── refs.bib
├── thesis.md → Export to thesis.pdf.
```

The proposed structure keeps the original organization while replacing LaTeX chapter files with Markdown. Typst templates would handle the document formatting in the background. 

## 3. Proposed Approach

The project will begin by setting up a new, empty Obsidian vault as an isolated testing environment. A dedicated GitHub repository (https://github.com/sinamatic/LaTeX-in-Obsidian) will be used to document the development process, track changes, and make the results reproducible.

Several existing Obsidian plugins appear suitable for this project and will be evaluated:

- Omd2Typst: Converts Obsidian Markdown notes into Typst documents or PDFs
- Typst PDF Export: Supports PDF generation from individual notes or collections
- Tinymist / Typstian: Allow Typst files to be edited and previewed

A particular focus will be on [Typst](https://typst.app/), an open-source typesetting system designed for creating scientific papers, theses, reports, and other structured documents. Typst provides a simpler markup language than LaTeX, supports reusable templates, bibliographies, figures, and tables, and offers a browser-based editor with live document previews. Its language and compiler are open source and can also be used locally. 

The practical approach is to transfer my existing Bachelor's thesis from LaTeX into Obsidian and convert its university-specific LaTeX template into a reusable Markdown-based workflow. This template should then serve as a foundation for my  Master's thesis, project reports, and other academic documents at Ohm University.

## 4. Evaluation and Expected Results

The final PDF should match or exceed the visual quality of the original LaTeX thesis while meeting the university's formatting requirements. The main evaluation criteria are the readability of the Markdown files without rendering, minimal use of LaTeX-specific syntax, and the effort required to write and export documents.

The project will also provide step-by-step documentation and reusable templates, allowing others to reproduce the workflow in their own Obsidian vaults.

***
Sources: [Typst Documentation](https://typst.app/docs/), [Omd2Typst](https://community.obsidian.md/plugins/omd-to-typst),  [Typst PDF Export](https://community.obsidian.md/plugins/typst-pdf-export), [Tinymist](https://community.obsidian.md/plugins/tinymist), [Typstian](https://community.obsidian.md/plugins/typstian)

