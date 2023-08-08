Next step is to train annif.
In this case I selected 350 row of complete data dump containing all Master thesis from TH Wildau repository in July 2023.
To start training insert following comand:
```
annif train thwildau-tfidf-de data-sets/THWildau/thwildau350.tsv
```
1) first call annif train
2) then call project ID as defined in projects.cfg
3) then insert path to folder of training data

