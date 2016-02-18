#Hungarian Wordnet (HuWN) / Magyar WordNet

Maintainer: 
[Márton Miháltz](http://www.nytud.hu/depts/corpus/Mihaltz_Marton.html) <mmihaltz@gmail.com>

##Changes

Release 2015-06-09:
- 52 definitions were edited. Definition rewriting completed.

Release 2015-06-03:
- 2688 definitions were edited

Release 2015-04-29:
- 3162 definitions were edited
- URL of the project is now https://github.com/dlt-rilmta/huwn

Release 2015-02-18:
- Fixed sense numbers: no duplicates, consecutive numbering (starting from 1) for literals in a PoS, trying to preserve original order
- Internal relations lists uniq'ed in synsets
- XML now contains inverted relations as well
- no LF characters in XML file
- fixed synset ENG20-00981788-v: nl_emphasize:4 -> nl_emphasise:1

Release 2014-08-14:
- Added mapping to Princeton WordNet 3.0 ILI synsets (see new ID3 and ELR3 tags).
  PWN2.0-PWN3.0 [synset mapping](http://ws.racai.ro:9191/repository/browse/princeton-wordnet-30-to-20-concept-mapping/d0986cbefb6811e2a8ad00237df3e358726887c928ac4fdba813ba9657d93ead/ ) by Tufis et al., 2011 was used 
  For each HuWN synset with an "ENG20-XXXXXXXX-Y" ID, an ID3 element was added with the PWN30 mapped id of the PWN20 id.
  For each HuWN synset that that contained one or more ELR tags, an ELR3 tag was added for each with the mapped PWN30 id with the same TYPE under ELR3 as in ELR.
  The file PWN20-30_unmapped_ids.txt contains the list of HuWN ids (based on PWN20) that could not be mapped to PWN30 ids (ids that were not included in the mapping).
- Character encoding is now UTF-8 instead of ISO-8859-2.
- The DTD was updated to reflect changes.
- This release is based on the [previous release](http://www.inf.u-szeged.hu/rgai/nlp?lang=en&page=nlpproj_hunont) dated 2009-09-05, which is a revised version of HuWN produced in the Hungarian WordNet Project completed in 2005-2007, funded by grant GVOP 3.1.1-2004-05-0191/3.0 and executed by a consortium of:
  * Research Institute for Linguistics, Hungarian Academy of Sciences (RIL-MTA)
  * University of Szeged
  * MorphoLogic Ltd.


##Citing

When writing about HuWN, please cite the following paper:

Miháltz, Márton, Csaba Hatvani, Judit Kuti, György Szarvas, János Csirik, Gábor Prószéky, Tamás Váradi: Methods and Results of the Hungarian WordNet Project. In: Proceedings of The Fourth Global WordNet Conference, Szeged, Hungary (2008), pp. 311–321.
http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.148.6139&rep=rep1&type=pdf

BibTeX entry:
```
@Inproceedings{Mihaltzetal2008HuWN,
  Title                    = {Methods and Results of the Hungarian WordNet Project},
  Author                   = {M{\'{a}}rton Mih{\'{a}}ltz and Csaba Hatvani and Judit Kuti and Gy{\"{o}}rgy Szarvas and J{\'{a}}nos Csirik and G{\'{a}}bor Pr{\'{o}}sz{\'{e}}ky and Tam{\'{a}}s V{\'{a}}radi},
  Booktitle                = {Proceedings of The Fourth Global WordNet Conference},
  Year                     = {2008},
  Location                 = {Szeged, Hungary},
  Pages                    = {311--321}
}
```

##Summary

HuWN contains 42288 synsets:

| PoS | #synsets | #word senses | #words |
| --- | -------: | -----------:| -----: |
| Nouns | 33530 | 45508 | 39079 |
| Verbs | 3607 | 6947 | 4905 |
| Adjectives | 4112 | 6215 | 4900 |
| Adverbs | 1039 | 1793 | 1354 |

The database conforms to the Balkanet / Global Wordnet XML file format (with some additions).
Each HuWN synset is mapped to 1 or more English (Princeton) WordNet synsets serving as Inter Lingual Index (ILI) records. 
Most HuWN sysnets are also mapped to an entry in the Magyar Ertelmezo Keziszotar (EKSz) Hungarian monolingual explanatory dictionary,
and most HuWN verbs synsets are also mapped to a verb frame description entry in the MetaMorpho grammar.

##Files

* huwn.xml -- the HuWN database in (extended) BalkaNet/Global WordNet XML format
* wnxml.dtd -- DTD for huwn.xml
* PWN20-30_unmapped_ids.2014-08-14.txt.gz -- list of HuWN synset ids based on PWN20 that could not be mapped to PWN30 because they were missing from the mapping files
* new_sense_numbers.2015-02-18.txt.gz -- List of sense numbers changed in Release 2015-02-18. Tab-separated: synset id (PWN20), literal, old sense number, new sense number
* README.md -- you are here
* LICENSE.txt -- license information

##Linked Open Data (RDF) Version of Hungarian WordNet

An RDF format version is available for the semantic web, which uses existing schemas and links to other existing resources.
Please visit: https://github.com/dlt-rilmta/huwn.rdf

##APIs
- Pyhton 3 API: https://github.com/ppke-nlpg/pywnxml
- C++ API: https://github.com/mmihaltz/libWNXML

##Command-line Tools

- You can use [wnxmlconsole.py](https://github.com/ppke-nlpg/pywnxml) to execute all kinds of queries using simple text commmands on the XML database.
- [libWNXML](https://github.com/mmihaltz/libWNXML) includes a **Windows** binary executable of the same console application.

##License

META-SHARE Commons BY NC ND License v1.0 (see LICENSE.pdf, or [META-SHARE licenses](http://www.meta-net.eu/meta-share/licenses))
