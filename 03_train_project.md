Next step is to train annif.
In this case I selected 350 row of complete data dump containing all Master thesis from TH Wildau repository in July 2023.
To start training insert following comand:
```
annif train thwildau-tfidf-de data-sets/THWildau/thwildau350.tsv
```
1) first call annif train
2) then call project ID as defined in projects.cfg
3) then insert path to folder of training data
4) training takes just couple of seconds since *tsv file is very small resulting in
5) -transforming subject corpus
   -creating vectorizer
   -creating similarity index
   Hint: controll if all three processes are comlpete. due to unknown reasons sometimes the creation of similarity index is not completed
6) test with command
```
echo "Technologie" | annif suggest thwildau-tfidf-de
```
leads to error: KeyError 'de' 

see images: images/train_annif.png, error_suggest.png
7) Controlled language settings in projects.cfg and fix KeyError 'de' by adjusting language termin to "de" instead of "german".

```
[thwildau-tfidf-de]
name=THWILDAU TFIDF project
language=de
backend=tfidf
vocab=rvkthwildau
analyzer=snowball(german)
```

analyzer=snowball(german)
