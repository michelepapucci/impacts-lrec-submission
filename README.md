# Italian Multi-level Parallel Corpus for Controlled Text Generation (IMPaCTS)

This anonymized repository contains the IMPaCTS (Italian Multi-level Parallel Corpus for Controlled Text Simplification) dataset. 

The dataset is contained in the archive IMPaCTS.zip. Given the large nature of the dataset, to download the repository please install [git-lfs](https://git-lfs.com/).

This resource is related to a paper under submision for LREC 2026. 


### Dataset Description

Each row in the dataset represents a couple of human-written complex sentence and machine-translated simplified sentence. Each row is identified by the `idx` field, which is a unique id to each row, and `original_sentence_idx` that represents a unique id for each original human-written sentence. 
Each original sentence has multiple simplification, identified each with a different row. The average number of simplifications per original sentence is 9.6. 
The original text of each pair is under the `original_text` column, while the simplified text is under `simplification`. 

Each pairs is annotated with a variety of linguistic features (Obtained with Profiling-UD) and with a readability score (Obtained with Read-it). The readability score are four for each sentence:
- raw - Readability score related to raw textual feature (e.g. average number of characters per token, average number of token per sentence, etc.)
- lexical - Readbility score related to lexical features (e.g. Type-Token Ration, etc.)
- syntactic - Readability score releated to syntactic features (e.g. average depth of the syntactic tree, distribution of subordinate clauses, etc.)
- all - An overall score that uses all the aforementioned features.

Those related to the original sentence have the prefix `original_`, e.g. `original_all`, and those related to the simplification have the prefix `simplification_`. 

Each rows contains all the linguistic features extracted for both the original text and the simplification. Those referred to the original, have a subfix `_original`, e.g. `char_per_tok_original`, while those that refer to the simplification have a `_simplification` subfix. 