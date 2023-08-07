Since the project goal is to add RVK notation to master theses of TH Wildau one team member extracet files from TH Wildau repository (see: https://github.com/mensslen/Annif-Project)

Be carefull to follow the recommendations of https://github.com/NatLibFi/Annif/wiki/Subject-vocabulary-formats. Be sure that the TSV file only contains 2 columns.
Encoding seem not to matter. UTF-8 works as well as Latin-3.

Take a closer look on hidden character in the TSV file or faulty clean up when extracting classification form web sources. (I experienced problems with quotes. If you get stuck open TSV file in terminal with cat and check wheter there are still characters you already removed!)

TSV File should look like this:
```
th-wildau:A	Allgemeines
th-wildau:AA	Bibliografien der Bibliografien, Universalbibliografien, Bibliothekskataloge, Nationalbibliografien
th-wildau:AA09900	Bibliografische Zeitschriften
th-wildau:AA10000-AA19900	Bibliografien der Bibliografien
th-wildau:AA10000	International, Allgemeines
th-wildau:AA10100	Antike Welt
th-wildau:AA10300	Ländergruppen/Entwicklungsländer
th-wildau:AA10400	Westliche Welt, Abendland, Europäische Welt
th-wildau:AA10500	Germanischer Kulturkreis
th-wildau:AA10600	Europa
```
Then load vocabulary 
```
annif load-vocab --language german rvkthwildau data-sets/THWildau/rvk_test2023v3.tsv
```
rvkthwildau is the vocabulary ID; data-sets/THWildau/rvk_test2023v3.tsv is the path

Attention: 

#) don't forget to put options --langage in the string otherwise you will get error message

#) if you run into error "getötet" or "killed" depending on OS language settings, data directory and take a closer look into date /vocab directory and inspec subject.csv and subject.ttl file 
see: images/load_vocabulary.png

Depending on TSV file load-vocab should not take to long, only a couple of minutes
