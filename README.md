Hungarian Wordnet (HuWN) / Magyar WordNet

Release date: 2014-08-14

Maintainer: 
Márton Miháltz <mmihaltz@gmail.com>
http://www.nytud.hu/depts/corpus/Mihaltz_Marton.html

History of changes:

Release 2014-08-14:
- Added mapping to Princeton WordNet 3.0 ILI synsets (see new ID3 and ELR3 tags).
  PWN2.0-PWN3.0 synset mapping by Tufis et al, 2011 was used
  (http://ws.racai.ro:9191/repository/browse/princeton-wordnet-30-to-20-concept-mapping/d0986cbefb6811e2a8ad00237df3e358726887c928ac4fdba813ba9657d93ead/ )
  For each HuWN synset with an "ENG20-XXXXXXXX-Y" ID, an ID3 element was added with the PWN30 mapped id of the PWN20 id.
  For each HuWN synset that that contained one or more ELR tags, an ELR3 tag was added for each with the mapped PWN30 id with the same TYPE under ELR3 as in ELR.
  The file PWN20-30_unmapped_ids.txt contains the list of HuWN ids (based on PWN20) that could not be mapped to PWN30 ids (ids that were not included in the mapping).
- Character encoding is now UTF-8 instead of ISO-8859-2.
- The DTD was updated to reflect changes.
- This release is based on the previous release dated 2009-09-05 (http://www.inf.u-szeged.hu/rgai/nlp?lang=en&page=nlpproj_hunont ),
  which is a revised version of HuWN produced by the Hungarian WordNet Project, which was completed in 2005-2007, was funded by grant GVOP 3.1.1-2004-05-0191/3.0 and was executed by a consortium of:
  Research Institute for Linguistics, Hungarian Academy of Sciences (RIL-MTA)
  The University of Szeged
  MorphoLogic Ltd.

Please cite the following paper:

Miháltz, Márton, Csaba Hatvani, Judit Kuti, György Szarvas, János Csirik, Gábor Prószéky, Tamás Váradi: Methods and Results of the Hungarian WordNet Project. In: Proceedings of The Fourth Global WordNet Conference, Szeged, Hungary (2008), pp. 311–321.
http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.148.6139&rep=rep1&type=pdf

License:

TODO

Summary:

HuWN contains 42288 synsets:
PoS             #synsets        #word senses
Nouns              33530              45508
Verbs               3607               6947
Adjectives          4112               6215
Adverbs             1039               1793
The database conforms to the Balkanet / Global Wordnet XML file format (with some additions).
Each HuWN synset is mapped to 1 or more English (Princeton) WordNet synsets serving as Inter Lingual Index (ILI) records. 
Most HuWN sysnets are also mapped to an entry in the Magyar Ertelmezo Keziszotar (EKSz) Hungarian monolingual explanatory dictionary,
and most HuWN verbs synsets are also mapped to a verb frame description entry in the MetaMorpho grammar.

List of files in this release:

huwn.xml -- the HuWN database in (extended) BalkaNet/Global WordNet XML format
wnxml.dtd -- DTD for huwn.xml
PWN20-30_unmapped_ids.txt -- list of HuWN synset ids based on PWN20 that could not be mapped to PWN30 because they were missing from the mapping files
README.md -- you are here

How to use HuWN with the VisDic browser/editor

TODO

Command-line tool (Windows, Linux)

TODO

API (C++, Python)

TODO
