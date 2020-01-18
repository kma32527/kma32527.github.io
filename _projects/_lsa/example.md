# Generating a model with arXiv abstracts

Clone the files to a local repository and run
```markdown
import keyword_model.py as km
```
This imports all relevant functions for running latent semantic analysis.

The package keyword_model.py contains the arXiv dataset as a default.
```markdown
titles, abstracts=km.load_arxiv()
model=km.corpusmodel(titles, abstracts, 500, 1)
```
This initializes a recommendation model with 500 1-gram features.

To receive a database recommendation given an input text,
```markdown
inputtext='some text as a string'
km.printmatches(inputtext, corpusmodel, 10)
```

To find the shared keywords between two texts under this model,
```markdown
commonkeys=km.intersection(text1, text2, corpusmodel)
print(commonkeys)
```
