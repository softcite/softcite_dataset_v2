# Softcite Dataset Version 2

This repository contains the resources (data and scripts) related to the version 2.* of the Softcite dataset, a corpus of 4971 scientific articles with software mention annotations. This is a gold standard corpus, resulting from multi-stage annotations from a team of annotators and reconcialiation phases by curators to solve disagreements. The dataset is available under CC-BY license. 

For the first versions of this dataset, see [here](https://github.com/howisonlab/softcite-dataset). This new repository is dedicated to new annotation iterations on the dataset and is independent from the previous repository for simplification. 

## Description of the dataset

### Statistics

The Softcite dataset consist of the 4,971 full-texts in English (available in Open Access under CC-BY license), half in Life Sciences and half in Economics, for a total of around 46 million tokens.

Annotations from the previous version of the dataset (v1.0) and this new release (v2.0) are summarized below: 

| Softcite dataset version | v1.0 (2020) | v2.0 (2023) | 
|---                       |---          |---          | 
| number of documents      | 4,971       | 4,971       |           
|---                       |---          |---          |
| software name (total)    | 4,093       | 5,134       |           
| - environment            |             | 1,089       |           
| - component              |             |   88        |           
| - implicit               |             |  106        |           
|---                       |---          |---          |        
| version                  | 1,258       | 1,478       |            
| publisher                | 1,111       | 1,311       |            
| URL                      |   172       |  231        |            
| programming language     |             |   71        |     

### Guidelines

The XML annotation guidelines describe the different mark-up and the annotation principles. They are available [here](annotation_guidelines_tei_xml.md).

For any have any suggestions, comments, contributions, welcome to start an issue or discussion in this repository, or contact us (see below).

### Resources

The versions 2.* of the Softcite dataset contains the following resources: 

1. Under the `xml/` subdirectory all the XML annotated corpus: 

- `softcite_corpus-full.tei.xml`: the dataset as a corpus with one TEI entry per document and paragraphs containing one software mention or more.
- `softcite_corpus-holdout-full.tei.xml`: for evaluation purpose, the so-called `holdout set` corresponding to 20% of the full texts with complete text content and software mentions. This holdout set represents a real distribution of mentions in papers and is, therefore, appropriate for evaluation. 
- `softcite_corpus-working.tei.xml`: the subset of the corpus excluding the 20% of the full texts of the holdout set, for evaluation purposes. 

Numerous XML tools and libraries allow to parse and extract information as needed. 

2. The `json/` subdirectory contains converted JSON files for the XML corpus. The JSON format is provided for users more confortable with JSON than XML. The name of the files is similar as for the above XML files but with `.json` extension. The JSON uses offsets for identifying the position of the annotation spans in paragraphs, which makes it less readable.  

## Some Python scripts

These Python scripts are related to the new version of the dataset and covers in particular the conversion of the master TEI XML corpus into JSON.


<!--
## About the creation and improvement of the dataset

This section describes the methodology and quality standard associated to this dataset. 
-->



## Acknowledgement

We thank Alfred P. Sloan Foundation for supporting this work. We also thank our collaborators and student annotators for making this dataset gold-standard and available.

## License 

The Softcite dataset is distributed under CC-BY license. The Python scrips are distributed under [Apache 2.0 license](http://www.apache.org/licenses/LICENSE-2.0). 

The documentation of the project is distributed under [CC-0](https://creativecommons.org/publicdomain/zero/1.0/) license.

If you contribute to Softcite dataset project, you agree to share your contribution following these licenses. 

Contact:  James Howison (PI, @jameshowison), Patrice Lopez (<patrice.lopez@science-miner.com>)
