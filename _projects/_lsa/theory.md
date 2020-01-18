## Model details

## Basis
Given the assumption that the contents of a paper is valid, one can consider a paper to be a bag of concepts, where concepts are represented by an ordered set of words. I use binary variables from ngrams representing inclusion in a text. This is in an effort to remove author bias when discussing the contents of a paper, since authors discuss their personal interests in more depth and detail. By standardizing the feature extraction  binary inclusion variables, the model evenly weights all concepts that an author brings up.

### Filtering for mathematical terminology
Scientific models incorporate math because it is demonstrably a good representation. However, these mathematical models are more than just a good representation; they also can provide insight into the underlying *dynamics*. For instance, two-componnt reaction-diffusion equations 

However, by discussing the mathematics at all, authors establish a relation between a scientific concept, and some representative mathematical structure describing its behaviour. This can be picked up on in a naive manner with a term inclusion feature representation. An advantage of this is that it removes the author's bias towards or against mathematics, instead conditioning on the *existence* of the connections between math and science themselves. I believe that through clustering scientific papers on mathematical terms and concepts would allow us to build a better intuitive framework of mathematics and how it connects to the world around us.
