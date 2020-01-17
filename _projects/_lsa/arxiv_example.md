# Generating a model with arXiv abstracts

Cloning the files to a local repository and run
```markdown
import keyword_model.py as km
```
This imports all relevant functions.

This package contains the arXiv dataset as a default, which can be used to construct a keyword model.
```markdown
titles, abstracts=km.load_arxiv()
model=km.corpusmodel(titles, abstracts, 500, 1)
```
This initializes a model with 500 1-gram features.

To retrieve the 10 most relevant abstracts given an input text, save your input text to a unformatted text file and run the following
```markdown
inputtext='relevant text'
# matches is an array titles, texts, vector_rep
matches=km.printmatches(inputtext, corpusmodel, 10)
```

The shared keywords of two texts under this model can also be found
```markdown
commonkeys=km.intersection(inputtext, text2, corpusmodel)
print(commonkeys)
```
