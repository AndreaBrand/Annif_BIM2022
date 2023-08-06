Following the instructions https://github.com/NatLibFi/Annif-tutorial, the first step was to add the necessary information to the projects.cfg file:
```
[thwildau-tfidf-de]
name=THWILDAU TFIDF project
language=de
backend=tfidf
vocab=rvkthwildau
analyzer=snowball(german)
```
thwildau-tfidf-de is project ID

tfidf is the algorithm applied, in this case it is more or less the "Hello world" version

vaocab is the vocabulary ID

projects.cfg can hold more than one project

In order to verify that annif can read project information start annif and call annif list projects
```
source annif-venv/bin/activate
```
```
annif list-projects
```
images/thwildauprojects.png
