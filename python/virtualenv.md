Installi virtualev e ti sposti nella cartella dove vuoi creare l'ambiente virtuale

```
pip3 install virtualenv
mkdir ambiente
cd ambiente
```
Associ al nuovo ambiente python 3, dove `/usr/bin` è il percorso dove si trova python 3 (che puoi trovare con `whereis python3`)

`virtualenv --python=/usr/bin/python3.6 nome_ambiente`

Per attivare l'ambiente:

`source nome_ambiente/bin/activate`

Se guardi la versione di python c'è solo la 3: python --version dà python3.6 (non serve che tu cerchi python3 --version per avere la versione del 3, perché è l'unica versione di python presente!)

Se guardi i pacchetti installati con `pip freeze` non c'è alcun pacchetto.

Dopo aver installato qualcosa con `pip install nome_pacchetto` puoi salvare la lista di tutti i pacchetti e tutte le dipendenze fino a quel momento installate con

`pip freeze > requirements.txt`

Per spegnere la macchina

`deactivate`

Quando poi crei una nuova macchina e vuoi usare gli stessi pacchetti e dipendenze, basta che usi da dentro la macchina attivata

`pip install -r requirements.txt`