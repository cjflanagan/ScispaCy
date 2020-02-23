**ScispaCy for Named Entity Recognition**

Named entity recognition (‘NER’) is a method of extracting knowledge from documents. It allows us (and machines) to better understand their contents and to ask specific questions about them.

For this project we will be using NER to extract Genes, Diseases and possibly other entities from Pubmed and other documents.

The way NER works is that a model is trained to identify certain entities by being showing many thousands of previous examples which are tagged and their place (index) within a string clearly identified. The natural language model (state of the art are bi-directional LSTM's) then learn how to identify these entities by finding patterns in the placement of the entity and its common surrounding words.

For this project we are fortunate that their are a number of high quality pre-trained NER models that we can leverage - I would particularly recommend a python package called scispacy which has particular models specifically for genes and diseases.

As a stretch goal I would like to have us train an NER model rather than using a pre-trained one. This is not likely to be better than the scispacy one but would be a useful learning experience.

In terms of delivery of the NER element of the project, I recommend we deploy the NER as a microservice accessible via a restful API which can be called by the workflow which likely will form the backbone of the pipeline. The service would take a long string of text as input and return all identified entities as a JSON object
