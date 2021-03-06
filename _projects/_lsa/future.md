## Future directions

### Summarizing model "findings"

This is a natural extension of the current algorithm for human use. Ideally, given an input text, the output would be lexically similar to the input text for increased comprehensibility.

### Clustering on mathematical terminology
Scientific models incorporate math because it is demonstrably a good representation. However, these mathematical models are more than just a good representation; they also can provide insight into the underlying *dynamics*. By discussing the mathematics at all, authors establish a relation between words associated with a scientific concept and words associated with a representative mathematical structure. This also has the benefit of being (mostly) standardized across research disciplines; a matrix is a matrix regardless of what data it contains.

This can be picked up on in a naive manner with a bag of words model, since academic terminology favours precision over brevity. Furthermore, using a binary 'term-presence' feature representation reduces the author's personal bias towards or against a mathematical model, instead conditioning on the *existence* of a given connections between math and science. I believe that this has potential for identifying broad, interdisciplinary trends in the existing literature by reducing the level of mathematical knowledge necessary to identify similarities between research disciplines.
