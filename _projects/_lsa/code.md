# Modelling arXiv abstracts on machine learning

Start by, cloning the repository and importing the model package
```markdown
import keyword_model.py as km
```

This package contains the arXiv dataset as a default, which can be used to construct a keyword model.
```markdown
arxiv_data=km.load_arxiv()
model=km.corpusmodel(arxiv_data, 500, 1)
```
This initializes a model of 500 single word grams.

To retrieve the 10 most relevant abstracts given an input text, save your input text to a unformatted text file.
```markdown
inputtext='relevant text'
\# matches is an array \[titles, texts, vector_rep\]
matches=km.gettopn(inputtext, corpusmodel, n)
km.printtitles(matches)
```
