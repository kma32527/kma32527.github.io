# Generating a model with arXiv abstracts

Clone the files to a local repository and run
```markdown
import keyword_model.py as km
```
This imports all relevant functions for running latent semantic analysis.

This package contains the arXiv dataset as a default, which can be used to construct a bag of words representation.
```markdown
titles, abstracts=km.load_arxiv()
model=km.corpusmodel(titles, abstracts, 500, 1)
```
This initializes a model with 500 1-gram features.

To retrieve the 10 most relevant abstracts given an input text, save your input text to a unformatted text file and run the following
```markdown
inputtext='some text as a string'
km.printmatches(inputtext, corpusmodel, 10)
```

One can also find the shared keywords under this model between two texts.
```markdown
commonkeys=km.intersection(text1, text2, corpusmodel)
print(commonkeys)
```
