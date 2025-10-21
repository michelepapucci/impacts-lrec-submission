# Italian Multi-level Parallel Corpus for Controlled Text Generation (IMPaCTS)

This anonymized repository contains the IMPaCTS (Italian Multi-level Parallel Corpus for Controlled Text Simplification) dataset. 

The dataset is contained in the archive IMPaCTS.zip. Given the large size of the dataset, to download the repository please install [git-lfs](https://git-lfs.com/).

This resource is related to a paper under submission for LREC 2026. 


### Dataset Description

Each row in the dataset represents a pair consisting of a human-written complex sentence and a machine-generated simplified sentence. Each row is identified by the `idx` field, which is a unique id for each row, and `original_sentence_idx` that represents a unique id for each original human-written sentence. 
Each original sentence has multiple simplifications, each identified with a different row. The average number of simplifications per original sentence is 9.6. 
The original text of each pair is under the `original_text` column, while the simplified text is under `simplification`. 

Each pair is annotated with a variety of linguistic features and with a readability score (obtained with Read-it). There are four readability scores for each sentence (both the original and the simplification):
- raw - Readability score related to raw textual features (e.g. average number of characters per token, average number of tokens per sentence, etc.)
- lexical - Readability score related to lexical features (e.g. Type-Token Ratio)
- syntactic - Readability score related to syntactic features (e.g. average depth of the syntactic tree, distribution of subordinate clauses, etc.)
- all - An overall score that uses all the aforementioned features.

The readability scores related to the original sentence have the prefix `original_`, e.g. `original_all`, and the readability scores related to the simplification have the prefix `simplification_`. 

Each row contains all the linguistic features extracted for both the original text and the simplification. The linguistic features of the original text have a suffix `_original`, e.g. `char_per_tok_original`, while the linguistic features of the simplification have a `_simplification` suffix. 