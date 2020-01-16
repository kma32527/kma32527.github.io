# Package description
This project consists of an importable package keymodel.py, and auxilliary packages.

To create a model from input texts, clone the repository and run

```markdown
import keyword_model.py as km
arxiv_data=km.load_arxiv()
model=km.corpusmodel(arxiv_data, 1)
```
This initializes a 1-gram model on the set of arXiv abstracts.

To retrieve a set of matches given an input text, run
```markdown
inputtext='relevant text'
matches=km.gettopn(inputtext, corpusmodel, n)
km.corpusprint(matches, corpusmodel)
```
