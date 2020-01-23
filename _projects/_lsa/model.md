## Model assumptions

## Feature extraction
Given the assumption that the contents of a paper is valid, one can consider a paper to be a bag of concepts, where concepts are represented by an ordered set of words. I use binary variables representing the inclusion of ngrams in texts. Since this algorithm seeks to highlight topical relations between texts, it's more important to consider the inclusion or exclusion of key words rather than the number of times they appear. This is optimized for short, informationally-dense summaries since summaries contain only the important points and concepts from a paper.
