# Cantonese Dictionaries to be used with `Jieba` 

Last Updated: October 23, 2020
---

If you don't know what is `Jieba`, I suggest you google it.

This repository contains a list of Cantonese dictionaries for Jieba,
amassed over the past two years.

By default, Jieba uses a "dictionary" a.k.a a tab-delimited list in `.txt`
format to tokenize Cantonese phrases.  It will only revert to HMM when the 
phrase is not found in the dictionary. In general, better tokenization can be
achieved when Jieba is used with a dictionary tailored for a specific discourse.

Use the command line to concatenate a subset of text files to create a bigger
dictionary.  For example:

```bash
cat hk_street_names.txt golden_dictionary.txt nouns.txt > YOUR_NEW_FILENAME.txt
```

Please note that dictionaries generated from a specific corpus, i.e. 
`20th Century Cantonese Movie Corpus` or `PyCantonese` will have a frequency
count and/or parts of speech next to a Cantonese phrase.

Jieba noun tags were added to `hk_street_names.csv` to create the file 
`hk_street_names.txt`.  Under the directory `~notebook`
I've added jupyter notebook `Hong Kong Street Names.ipynb` to show 
how you can add Jieba pos tags to a list of know noun phrases.  Similar
routines can be done for verb and adjective lists.