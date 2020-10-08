# RMarkdown template for preprint recommended by one of the Peer Communities In

written by Maxime Dahirel (GitHub: [@mdahirel](https://github.com/mdahirel)), from original LaTeX templates

# To use this template

- open the `manuscript.Rmd` file
- modify the YAML with your informations (including your bibliography file path)
- write your preprint in the body of the document
- press `Knit` or use `render()`
- *Voila!*

This RMarkdown template is based on the LaTeX templates available here https://peercommunityin.org/templates/, with modifications to allow you to fill all metadata fields directly from the YAML header of the `Rmd` file. 

This template relies on the `bookdown` package. It is possible to output without it, but some functions are lost. See the "DO NOT CHANGE these settings unless you know what you're doing" block of the YAML header.

**Important:** we recommend Better BibTeX users to *not* export their bibliography as Better BibTex files, but rather as "classical" BibTeX files. Using Better BibTeX can use to unwanted changes in title capitalization, among others (corrections to this problem will be attempted in later updates).

If you need any help in how to write your RMarkdown document, the RMarkdown Cookbook by Yihui Xie, Christophe Dervieux, Emily Riederer (https://bookdown.org/yihui/rmarkdown-cookbook/) is a good start, but many resources are available online.

NB: please ensure there is no reference with the key 'recommendedpreprint' in your bibliography files. This key is used by the LaTeX templates to build and display the "cite as" paragraph on the first page of the pdf.

# PS: how to add new PCIs to the template

PCIs all have the exact same template, with the exception of the name (obviously) and the header images. This makes adding a new PCI to the template very straightforward:

- start by coining a short name for the PCI (e.g. "Evolutionary Biology" -> "evolbiol")
- add this name to the list at the top of the `manuscript.Rmd` file, so that authors can find it
- add both the first page header image and the secondary header image to the `resources` folder, with filenames `logo_pour_PDF_PCIshortname.png` and `small_logo_pour_PDF_PCIshortname.png` respectively, where `PCIshortname` is of course, your PCI short code name
- in the `templates\preamble.tex` file, starting line ≈ 156, there is a series of nested if statements on how to expand a short code into the PCI long name. Add yours to the list
- you're ready to write fully formatted articles for the new PCI!
