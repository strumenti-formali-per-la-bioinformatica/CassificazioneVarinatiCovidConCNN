# ClassificazioneVariantiCovidConCNN

## Abstact
 Negli ultimi anni la **sindrome respiratoria acuta grave (SARS-CoV-2)** si è manifestata in maniera spropositata, portando in condizioni gravissime, e in alcuni casi anche la morte alle persone che venivano a contatto, ci si è trovati a imbattere in un nuovo virus che ha preso il nome COVID-19 dove per 19 si intende l'anno della scoperta, portando in breve tempo a una pandemia globale dove siamo stati costretti a stare quasi un anno senza uscire per evitare contatti e trasmissione del virus. 
Nonostante i vaccini che non sono tardati ad arrivare, anche i cambiamenti del genoma del virus non sono tardati ad arrivare, portando cosi a cambiare il modo di infettare le cellule ospitanti generando cosi diverse varianti del virus. È stato notato che queste mutazioni si verificano in modo sproporzionato nella regione della punta del genoma (simile ad una corona) del virus, rendendo così tale zona importante per distinguere le varianti.
Quello che tratteremo in questo lavoro riguardo la classificazioni di tali varianti sulla base di dati che rappresentano la regione della punto dove si evidenziano le mutazioni.
Prima di addestrare i nostri modelli di classificazione andremo ad operare sui dati del data set, in quanto essendo dati alfabetici,  non si adattano ai modelli di deep learning.
Quello che verrà fatto è usare delle tecniche capaci di trasformare tali sequenze alfabetiche in numeriche sottoposta successivamente di una ulteriore trasformazione, che permette di rappresentare tali sequenze numeriche in segnali.
Dopo il trattamento dei dati, proponendo prima una classificazione basata su serie temporali che prendono in input delle serie(in questo caso i nostri segnali creati prima) e successivamente adoperiamo delle trasformazioni sui segnali per trasformarli in immagini per darle in pasto a un modello di reti neurali convoluzionali per il riconoscimento di immagini.
Una volta calcolati i risultati di entrambi i modelli quello che andremo a fare e lavorare sulla trasformazione delle immagini, infatti come vedremo è passibile applicare ai segnali trasformati in immagine dei parametri aggiuntivi, come filtri di colori che caratterizzano e aggiungono dettagli alla rappresentazione di immagine del segnale in modo da evidenziare più caratteristiche nell'immagine cosi da poter valutare se il nostro modello migliorare/ peggiorare in base a queste aggiunte di dettaglio e trarne delle conclusioni finali.

# Passi per utilizzare il progetto

## Prerequisiti

In caso non si usa google colab per l'utilizzo della gpu, è necessario per attivarla sul proprio pc:

Prima cosa installare cuda versione 11.6

Successivamente per collegare cuda con pytorch (su cui si basa il codice) è necessario scaricare nel terminare:

```cmd

pip3 install torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/cu116

```

In alternativa a chi usa l'ambiente di anaconda:

```cmd

conda install pytorch torchvision torchaudio pytorch-cuda=11.6 -c pytorch -c nvidia

```
## Installazioni
Per Utilizzare il progetto è necessario intallare le seguenti librerie:

```cmd

pip install fastcore==1.4.1

pip install tsai==0.3.0

pip install fastai==2.5.5

pip install fastai2==0.0.30

```

Una volta fatto ciò è possibile usare un qualsiasi compilatore (visual studio, google colab, notebook jupyter) per eseguire il codie.

Le libreria con la versione corretta sono già presenti anche nel file del progetto.ipynp.
Mentre per implementarlo sul pc occore scaricare tali libreria specificate sopra.
