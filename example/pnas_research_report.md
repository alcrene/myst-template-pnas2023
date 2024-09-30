---
title: Template for preparing your research report submission to PNAS
bibliography: pnas-sample.bib
affiliations:
  - id: one
    institution: Affiliation One
  - id: two
    institution: Affiliation Two
  - id: three
    institution: Affiliation Three
authors:
  - name: Author One
    equal_contributor: true
    affiliations:
      - one
      - three
  - name: Author Two
    equal_contributor: true
    corresponding: true
    email: author.two@email.com
    affiliations:
      - two
  - name: Author Three
    affiliations:
      - one
  
numbering:
  math: true
  figure: true
  table: true
  code: false
  headings: false
exports:
  - format: tex
    template: ../
    output: ../exports/pnas_research_report.tex
  - format: pdf
    template: ../
    output: ../exports/pnas_research_report.pdf
---

+++ { "part": "firstpage" }

This PNAS journal template is provided to help you write your work in the correct journal format. Instructions for use are provided below.

Note: please start your introduction without including the word “Introduction” as a section heading (except for math articles in the Physical Sciences section); this heading is implied in the first paragraphs.

# Guide to using this template on Overleaf

Please note that whilst this template provides a preview of the typeset manuscript for submission, to help in this preparation, it will not necessarily be the final publication layout. For more detailed information please see the [PNAS Information for Authors](https://www.pnas.org/page/authors/format).

If you have a question while using this template on Overleaf, please use the help menu (“?”) on the top bar to search for [help and tutorials](https://www.overleaf.com/help). You can also [contact the Overleaf support team](https://www.overleaf.com/contact) at any time with specific questions about your manuscript or feedback on the template.

## Author Affiliations

Include department, institution, and complete address, with the ZIP/postal code, for each author. Use lower case letters to match authors with institutions, as shown in the example. PNAS strongly encourages authors to supply an [ORCID identifier](https://orcid.org/) for each author. Individual authors must link their ORCID account to their PNAS account at [www.pnascentral.org](http://www.pnascentral.org/). For proper authentication, authors must provide their ORCID at submission and are not permitted to add ORCIDs on proofs.

## Submitting Manuscripts

All authors must submit their articles at [PNAScentral](http://www.pnascentral.org/cgi-bin/main.plex). If you are using Overleaf to write your article, you can use the “Submit to PNAS” option in the top bar of the editor window.

## Format

Many authors find it useful to organize their manuscripts with the following order of sections: title, author line and affiliations, keywords, abstract, significance statement, introduction, results, discussion, materials and methods, acknowledgments, and references. Other orders and headings are permitted.

## Manuscript Length

A standard 6-page article is approximately 4,000 words, 50 references, and 4 medium-size graphical elements (i.e., figures and tables). The preferred length of articles remains at 6 pages, but PNAS will allow articles up to a maximum of 12 pages.

## References

References should be cited in numerical order as they appear in text; this will be done automatically via bibtex, e.g. [@belkin2002using] and [@berard1994embedding; @coifman2005geometric; @phdthesis; @masterthesis]. All references cited in the main text should be included in the main manuscript file.

## Data Archival

PNAS must be able to archive the data essential to a published article. Where such archiving is not possible, deposition of data in public databases, such as GenBank, ArrayExpress, Protein Data Bank, Unidata, and others outlined in the [Information for Authors](https://www.pnas.org/author-center/editorial-and-journal-policies#materials-and-data-availability), is acceptable.

+++

## Language-Editing Services
Prior to submission, authors who believe their manuscripts would benefit from professional editing are encouraged to use a language-editing service (see list at https://www.pnas.org/author-center/language-editing). PNAS does not take responsibility for or endorse these services, and their use has no bearing on acceptance of a manuscript for publication.

```{figure} frog.pdf
:label: fig:frog
:width: 80%
:align: center

Placeholder image of a frog with a long example legend to show justification setting.
```



````{table} Comparison of the fitted potential energy surfaces and ab initio benchmark electronic energy calculations
:align: center

| Species              | CBS  | CV   | G3   |
| :------------------- | ---: | ---: | ---: |
| 1. Acetaldehyde      | 0.0  | 0.0  | 0.0  |
| 2. Vinyl alcohol     | 9.1  | 9.6  | 13.5 |
| 3. Hydroxyethylidene | 50.8 | 51.2 | 54.0 |
````

(Currently not supported: the `\addtabletext` macro.)


## Digital Figures

EPS, high-resolution PDF, and PowerPoint are preferred formats for figures that will be used in the main manuscript. Authors may submit PRC or U3D files for 3D images; these must be accompanied by 2D representations in TIFF, EPS, or high-resolution PDF format. Color images must be in RGB (red, green, blue) mode. Include the font files for any text.

Images must be provided at final size, preferably 1 column width (8.7cm). Figures wider than 1 column should be sized to 11.4cm or 17.8cm wide. Numbers, letters, and symbols should be no smaller than 6 points (2mm) and no larger than 12 points (6mm) after reduction and must be consistent.

Figures and tables should be labelled and referenced in the standard way using the `\label{}` and `\ref{}` commands.

Figure [](#fig:frog) shows an example of how to insert a column-wide figure. To insert a figure wider than one column, please use the `\begin{figure*}...\end{figure*}` environment. Figures wider than one column should be sized to 11.4 cm or 17.8 cm wide. Use `\begin{SCfigure*}...\end{SCfigure*}` for a wide figure with side legends.

```latex
\begin{SCfigure*}[\sidecaptionrelwidth][t!]
\centering
\includegraphics[width=11.4cm,height=11.4cm]{frog.pdf}
\caption{This legend would be placed at the side of the figure, rather than below it.}\label{fig:side}
\end{SCfigure*}
```


## Tables
Tables should be included in the main manuscript file and should not be uploaded separately.


## Single column equations

Authors may use 1- or 2-column equations in their article, according to their preference.

To allow an equation to span both columns, use the `\begin{figure*}...\end{figure*}` environment mentioned above for figures.

Note that the use of the `widetext` environment for equations is not recommended, and should not be used.

```latex
\begin{figure*}[bt!]
\begin{align*}
(x+y)^3&=(x+y)(x+y)^2\\
       &=(x+y)(x^2+2xy+y^2) \numberthis \label{eqn:example} \\
       &=x^3+3x^2y+3xy^3+x^3.
\end{align*}
\end{figure*}
```


## Supporting Information Appendix (SI)

Authors should submit SI as a single separate SI Appendix PDF file, combining all text, figures, tables, movie legends, and SI references. SI will be published as provided by the authors; it will not be edited or composed. Additional details can be found in the [PNAS Author Center](https://www.pnas.org/authors/submitting-your-manuscript#manuscript-formatting-guidelines). The PNAS Overleaf SI template can be found [here](https://www.overleaf.com/latex/templates/pnas-template-for-supplementary-information/wqfsfqwyjtsd). Refer to the SI Appendix in the manuscript at an appropriate point in the text. Number supporting figures and tables starting with S1, S2, etc.

Authors who place detailed materials and methods in an SI Appendix must provide sufficient detail in the main text methods to enable a reader to follow the logic of the procedures and results and also must reference the SI methods. If a paper is fundamentally a study of a new method or technique, then the methods must be described completely in the main text.

### SI Datasets

Supply .xlsx, .csv, .txt, .rtf, or .pdf files. This file type will be published in raw format and will not be edited or composed.


### SI Movies

Supply Audio Video Interleave (avi), Quicktime (mov), Windows Media (wmv), animated GIF (gif), or MPEG files. Movie legends should be included in the SI Appendix file. All movies should be submitted at the desired reproduction size and length. Movies should be no more than 10MB in size.


+++ { "part": "matmethods" }

Please describe your materials and methods here. This can be more than one paragraph, and may contain subsections and equations as required.

## Subsection for Method
Example text for subsection.

+++ { "part": "acknowledgments" }

Please include your acknowledgments here, set in a single paragraph. Please do not include any acknowledgments in the Supporting Information, or anywhere else in the manuscript.

+++

