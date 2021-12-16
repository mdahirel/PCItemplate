# RMarkdown template for preprints recommended by one of the Peer Communities In

written by Maxime Dahirel (GitHub: [@mdahirel](https://github.com/mdahirel)), from the original LaTeX templates.

\[The creation of this template was a side-project/learning exercice for the author. **It is delivered as is, sparsely maintained, and may not receive further updates**. I encourage users to open issues to signal bugs, but cannot guarantee I will be able to solve them, or even see them. I also encourage users to propose solutions, and open PRs, about issues *they* may be able to solve. I especially encourage anyone with more time than me to fork this repo and make their own, better version\]

# To use this template

- (on GitHub) click on the "Code" button at the top of this page, then "Download ZIP", and unzip the `.zip` folder where you want it
- open the `manuscript.Rmd` file
- modify the YAML header (all the lines until the second `---`) with your informations (including your bibliography file path)
- write your preprint in the body of the document
- press `Knit` (if you use RStudio) or use `render()`
- *Voila!*

This RMarkdown template is based on the LaTeX templates available here https://peercommunityin.org/templates/, with modifications to allow you to fill all metadata fields directly from the YAML header of the `Rmd` file. 

If you need any help in how to write your RMarkdown document, the RMarkdown Cookbook by Yihui Xie, Christophe Dervieux, Emily Riederer (https://bookdown.org/yihui/rmarkdown-cookbook/) is a good start, but many resources are available online.

**Important notes about config:**

- This template relies on the `bookdown` package (https://bookdown.org/), which must be installed. It is actually possible to output without it, but some functions are lost. See the "DO NOT CHANGE these settings unless you know what you're doing" block of the YAML header. 

- Like the authors of `bookdown`, I strongly recommend the use of `tinytex` as the underlying LaTeX distribution (see https://yihui.org/tinytex/ for details and instructions about installation). Anecdotally, users have reported that some bugs during pdf knitting have actually been repaired by installing `tinytex`.

**Important notes regarding references lists:** 

- please ensure there is *no* reference with the key 'recommendedpreprint' in your own bibliography files. This is the key used by the LaTeX templates to generate a "recommendedpreprint.bib" file and use it to display the "cite as" paragraph on the first page of the pdf.

- In some cases, some unwanted annotation fields can appear in the reference lists. While we work on ironing these out, the best solution may be to delete manually the unwanted fields from the .bib file. For Zotero users, use Better BibTeX and export bibliographies as Better BibLaTeX to reduce these problems (preferentially with automatic title capitalization turned off, see Advanced> Export in Better BibTex preference panel). Using Better BibTeX, one can also automate the exclusion of the unwanted fields from the .bib exports, if the problems persist (Export in preference panel, which is different from Advanced> Export). We recommend putting *at least* "annotation,month" on the exclude list.

# for admins: how to add new PCIs to the template

PCIs all have the exact same template, with the exception of the name (obviously) and the header images. This makes adding a new PCI to the template very straightforward:

- start by coining a short name for the PCI (e.g. "Evolutionary Biology" -> "evolbiol")
- add this name to the list at the top of the `manuscript.Rmd` file, so that authors can find it
- add both the first page header image and the secondary header image to the `resources` folder, with filenames `logo_pour_PDF_PCIshortname.png` and `small_logo_pour_PDF_PCIshortname.png` respectively, where `PCIshortname` is of course, your PCI short code name
- in the `templates/preamble.tex` file, starting line ≈ 171, there is a series of nested if statements on how to expand a short code into the PCI long name. Add yours to the list
- the template is ready for the new PCI!
