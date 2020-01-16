# Modelling arXiv abstracts on machine learning

Cloning the files to a local repository and run
```markdown
import keyword_model.py as km
```
This imports all relevant functions.

This package contains the arXiv dataset as a default, which can be used to construct a keyword model.
```markdown
arxiv_data=km.load_arxiv()
model=km.corpusmodel(arxiv_data, 500, 1)
```
This initializes a model of 500 single word grams.

To retrieve the 10 most relevant abstracts given an input text, save your input text to a unformatted text file and run the following
```markdown
inputtext='relevant text'
# matches is an array titles, texts, vector_rep
matches=km.gettopn(inputtext, corpusmodel, 10)
km.printtitles(matches)
```

The shared keywords of two texts under this model can also be found
```markdown
commonkeys=km.intersection(inputtext, text2, corpusmodel)
print(commonkeys)
```
