# UniTrento_CropMenu
This is LaTeX code to (semi) automatize the cropped Menus sent in the Telegram channel UniTrento

## Cosa fare;
1. Scaricare i due PDF dei menù da https://www.operauni.tn.it/servizi/ristorazione/menu e metterli nella cartella con i nomi "scelta" e "lesto"
2. Aprire il file .TeX e rinominare le cinque frasi "\newcommand{\fraseuno}{MENÙ SETTIMANA 31 NOVEMBRE - 05 DICEMBRE 2019}" con il nome appropriato. _(Le ho inizializzate con novembre e dicembre per testare se ci stavano nella pagina)_
3. Aggiustare i valori di TRIM (crop della parte inutile dei pdf). Bisogna farlo per ogni pdf perché l'Opera non sa fare i pdf allineati nelle varie pagine alla stessa altezza 🤷‍♂️ 
Di defualt sono:
```
%Trim: sinistra - sotto - destra - sopra
%        0      16      0        2
```
4. Compilare e visulizzare il pdf
5. Vedere se ci sono sono problemi di crop
6. Vedi punto 4
7. Vedi punto 5
8. Vedi punto 4
9. Piangere
10. Convertire in immagine i pdf
11. Inviare su Telegram

## Problemi noti:
* Ogni tanto l'Opera ha la bella idea di mettere gli .xls e non i pdf nel sito -> provare a mandar loro una mail
* Come detto ogni pagina dei pdf di partenza parte da una quota diversa, perciò il trim va a tentativi. **Vedi punto 9**

## Cose che si potrebbero implementare
* Download automatico dei pdf dal sito dell'opera
* Automatizzare il nome delle cinque frasi del punto 2. Magari scrivendo solo il numero della settimana e in automatico scrive a parole?
* Automatizzare la conversione in png con questo metodo https://tex.stackexchange.com/questions/11866/compile-a-latex-document-into-a-png-image-thats-as-short-as-possible
```
pdflatex file
convert -density 300 CropMenu.pdf -quality 90 CropMenu.png
```
* Automatizzare l'invio delle immagini nel canale telegram
