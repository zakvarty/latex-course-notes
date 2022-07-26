# Hello World! LaTeX Text {#text}

## Structure of a LaTeX Document 

## Hello world 

## A Basic Preamble

## Structure 

- bold 
- italic 
- underline 
- monospace 
- cross through 

- Paragraph breaks

- Sections 
- Subsections  

- lists: 
  - numbered  
  - unnumbered 
  - sublists 
  - subsublists 
  
- footnotes

## Lorem Ipsum 

A longer example text. Give as .txt and ask to format as seen in example pdf. 

## Labelling and Referencing 

- labelling sections and subsections 
- suggested naming structure ch-intro sec-intro-labelling
- Move sections around and numbers fix themselves (on double compiling) 
- Adding hyperlinks with the hyperref package

## Citations

- the .bib file & its structure 
  - recommend authorYYYYkeyword
  - recommend keeping aphabetical order within bib file
  - sorting by topic seems like a good idea when you start but there are alsways awkward in-between papers
- How to get bib references from google scholar 
- Can also get them from other citation managers such as Mendeley and Evernote 
- Can also create an entry manually yourself 
- Can edit entries manually yourself 
- This is important so that you can fix the dodgy references (Coles example) 
- Citing Websites 
- Citing ArXiV preprints 
- Citing other materials 
- what to add to the preamble and the end of the document 
- Where to go for extra help - the Overleaf help page is very good on this.


## Tips for writing longer documents 

- Can skip on first reading 
- multiple tex files 
  - file for preamble 
  - file for main text structure 
  - separate file for each section/chapter 
  - include and input 



Cross-references make it easier for your readers to find and link to elements in your book.

## Chapters and sub-chapters

There are two steps to cross-reference any heading:

1. Label the heading: `# Hello world {#nice-label}`. 
    - Leave the label off if you like the automated heading generated based on your heading title: for example, `# Hello world` = `# Hello world {#hello-world}`.
    - To label an un-numbered heading, use: `# Hello world {-#nice-label}` or `{# Hello world .unnumbered}`.

1. Next, reference the labeled heading anywhere in the text using `\@ref(nice-label)`; for example, please see Chapter \@ref(cross). 
    - If you prefer text as the link instead of a numbered reference use: [any text you want can go here](#cross).

## Captioned figures and tables

Figures and tables *with captions* can also be cross-referenced from elsewhere in your book using `\@ref(fig:chunk-label)` and `\@ref(tab:chunk-label)`, respectively.

See Figure \@ref(fig:nice-fig).


```r
par(mar = c(4, 4, .1, .1))
plot(pressure, type = 'b', pch = 19)
```

<div class="figure" style="text-align: center">
<img src="02-text_files/figure-epub3/nice-fig-1.png" alt="Plot with connected points showing that vapor pressure of mercury increases exponentially as temperature increases." width="80%" />
<p class="caption">(\#fig:nice-fig)Here is a nice figure!</p>
</div>

Don't miss Table \@ref(tab:nice-tab).


```r
knitr::kable(
  head(pressure, 10), caption = 'Here is a nice table!',
  booktabs = TRUE
)
```



Table: (\#tab:nice-tab)Here is a nice table!

| temperature| pressure|
|-----------:|--------:|
|           0|   0.0002|
|          20|   0.0012|
|          40|   0.0060|
|          60|   0.0300|
|          80|   0.0900|
|         100|   0.2700|
|         120|   0.7500|
|         140|   1.8500|
|         160|   4.2000|
|         180|   8.8000|
