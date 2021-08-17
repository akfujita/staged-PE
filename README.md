# Staged PE Dataset

## Introduction

Aiming to analyze extra-document and non-linguistic information that must be referred to when translating documents, we collected examples of translation issues and their revisions through 2-stage post-editing (PE) of machine translation (MT) outputs.

## Contents

Post-editing (PE) has been a prevalent approach to make machine translation (MT) output to be acceptable translation, where human post-editors solve two types of translation issues that MT systems have caused.  One type covers issues that must be avoided only referring to the given text, i.e., by text-to-text MT, and the other type that is caused due to lack of extra-document and non-linguistic information that are indispensable for translation, such as norms and skopos.
To collect examples of translation issues and analyze the sub-types of necessary information to avoid/solve them, we performed 2-stage manual PE for MT outputs.

This repository currently contains the results for the English-to-Japanese news translation task in [the Asian Language Treebank (ALT) project](https://www2.nict.go.jp/astrec-att/member/mutiyama/ALT/).  Data consist of the following two types.

* ***Parallel data*** consisting of (a) source text, (b) an output of a domain-adapted MT system, (c) segment-level minimal PE results, and (d) document-level full PE results.
	* ***Segment-level minimal PE***, i.e., changes from (b) to (c): We performed this stage referring to each segment only.  Aiming to preclude non-compulsory preferential edits, we constrained the degree of edits relying on HTER between (b) the MT output and reference translation produced independently by professionals.  We consider the results represent translations attainable based on the given textual information only.
	* ***Document-level full PE***, i.e., changes from (c) to (d): We performed this stage regarding (c) as if it is raw MT output.  Unlike the previous stage, post-editors are allowed to refer to any kind of information that are necessary to produce the translation of minimum-level quality as the TSP product.

* ***Annotated revision examples*** extracted from the pairs of (c) and (d).  Pairs of an erroneous text span in (c) and its revision in (d) were extracted and annotated with the following three type of information.
	* ***Necessity of document-level textual information***: whether the textual information outside the segment but in the document was necessary to solve the issue.
	* ***Necessity of extra information***: whether any extra-document and/or non-linguistic information was necessary to solve the issue.  If yes, we also annotated with such information types (more than one if applicable).
	* ***Issue type***: one of the 16 types in [a typology of translation issues](https://aclweb.org/anthology/W17-0807/).

## Todo

* To obtain the attainable translation by so-called document-level machine translation, another ***Document-level minimal PE*** could be introduced, which prohibits to refer to extra-document and non-linguistic information, similarly to the Segment-level minimal PE, but unlike Document-level full PE.
* Exercise on other translation directions and domains.

## References

* Atsushi Fujita. [Attainable Text-to-Text Machine Translation vs. Translation: Issues Beyond Linguistic Processing](https://aclanthology.org/2021.mtsummit-research.18/). In Proceedings of the 18th Machine Translation Summit (MT Summit), pp.215-230, Aug., 2021.

## Precautions

* National Institute of Information and Communications Technology (henceforth, NICT) has made the dataset publicly available under the conditions of license specified below.
* NICT bears no responsibility for the contents of the dataset and assumes no liability for any direct or indirect damage or loss whatsoever that may be incurred as a result of using the dataset.
* If any copyright infringement or other problems are found in the dataset, please contact us at atsushi.fujita[at]nict[dot]go[dot]jp. We will review the issue and undertake appropriate measures when needed.

## License

![Creative Commons License](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png)

* Use and/or redistribution of this dataset is permitted under the conditions of [Creative Commons Attribution-NonCommercial-ShareAlike License 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).
* The source English texts of the dataset have been sampled from [English Wikinews](https://en.wikinews.org/wiki/) that are available under [Creative Commons Attribution 2.5 License](https://creativecommons.org/licenses/by/2.5/) by [the Asian Language Treebank (ALT) Project](https://www2.nict.go.jp/astrec-att/member/mutiyama/ALT/).  Users of the dataset are requested to take careful consideration when encountering any instances of defamation, discriminatory terms, or personal information that might be found within it.  To ensure proper usage of the dataset, refer to [Terms of Use](https://foundation.wikimedia.org/wiki/Terms_of_Use/en) of Wikinews.

## Acknowledgments

This dataset has been developed partly supported by JSPS KAKENHI Grant-in-Aid for Scientific Research (S) [19H05660, Developing a Translation Process Model and Constructing an Integrated Translation Environment through Detailed Descriptions of Translation Norms and Competences](https://kaken.nii.ac.jp/en/grant/KAKENHI-PROJECT-19H05660/), as a part of work at [Advanced Translation Technology Laboratory](https://att-astrec.nict.go.jp/), [Advanced Speech Translation Research and Development Promotion Center](https://astrec.nict.go.jp/), [National Institute of Information and Communications Technology](https://www.nict.go.jp/en/).
