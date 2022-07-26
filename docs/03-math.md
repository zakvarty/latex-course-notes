# Beautiful Math in LaTeX

## Introduction 
- This is what we are really here for and where things start to get really fun! 

- several ways of writnig math, all of which come into some sort of math environment. 

- first is inline math, that is used for when you are talking about a mathematical object or expression in the middle of a sentence. The math text should be "wrapped" in dollar signs. 

- For displayed math there are several options: wrap in double dollar signs, wrap with `\[` and `\]` or explicitly use an equation environment. 

- Displayed equataions by default get numbered and you can label and reference them in the same way as sections and subsections earlier. Remember, it might take two compilations to get these references to appear.  

- Only equations that you mention in the text should get numbers. To typeset a displayed equation without a number you can add `\nonumber` to any of the above options or you can use the `equation*` environment instead. 

## Some oddments 

$\times$ is `$times$`. 


You can add parts to organize one or more book chapters together. Parts can be inserted at the top of an .Rmd file, before the first-level chapter heading in that same file. 

Add a numbered part: `# (PART) Act one {-}` (followed by `# A chapter`)

Add an unnumbered part: `# (PART\*) Act one {-}` (followed by `# A chapter`)

Add an appendix as a special kind of un-numbered part: `# (APPENDIX) Other stuff {-}` (followed by `# A chapter`). Chapters in an appendix are prepended with letters instead of numbers.



