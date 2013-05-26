Introduction to Haskell
=======================
Presentation designed to be given as an introduction to the Haskell Programming
Language. Intended to take between 1 and 2 hours, or be broken up into multiple
smaller segments.

For LaTeX'ers and people running the Makefile
---------------------------------------------
Makefile Info:
 - 'make presentation.pdf' will create the default presentation
 - adding notes=true to the make command will cause the Makefile to generate the
   presentation two screens wide, with the right side being notes, and the left
   the presentation
 - 'make handout.pdf' will create a handout, which is 2 slides per page, with no
   incremental bullet points
 - 'make notes.pdf' will create the accompanying notes to go with each
   slide/bulletpoint

 - When modifing src/haskell.tex, anything that you want explicitly in a
   particular make should be preceded by '%%%pdfname%%%'
   eg. For something only for presentation the line should look like
   %%%presentation%%%\LaTeX stuff
 - This can also be used to create unique pdfs not limited to the three examples
   above, the make file will preprocess haskell.tex for lines matching the
   desired pdf filename, so 'make presentation.pdf' will enable lines starting
   with %%%presentation%%%, adding 'notes=true' also enables lines starting with
   %%%withnotes%%%
 - If the above is too confusing just look at haskell.tex and you should see
   what I mean
 - GL,HF