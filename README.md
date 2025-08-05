# Laboratorio-Data-Mining
Progetto di Classificazione di Forme Geometriche

Autore: Chiappini Mario (Matricola: 0322135)

Descrizione

Questo progetto sviluppa un sistema automatico per il riconoscimento e la classificazione di forme geometriche (ellisse, rettangolo, segmento, croce) a partire da sequenze di punti che ne rappresentano il contorno. Il dataset è generato in modo sintetico, con possibilità di inserire rumore gaussiano e variare il numero di punti per ciascuna forma.

Le principali fasi del progetto sono:

Generazione del dataset: creazione di campioni di forme con parametri personalizzabili (numero di punti, rumore, dimensioni).

Estrazione delle feature:

Rapporto di aspetto (Aspect Ratio) della bounding box

Area della bounding box

Compattezza (ratio area reale / area bounding box)

Area del convex hull e relativo rapporto

Statistiche di distribuzione delle distanze dal baricentro (media, deviazione standard)

Analisi esplorativa (EDA): visualizzazione delle forme, boxplot delle feature, PCA per riduzione dimensionale.

Classificazione:

Problema binario (es. distinguere fra due classi a scelta)

Problema multiclasse (classificazione su tutte e 4 le classi)

Confronto di diversi algoritmi: Logistic Regression, SVM, Random Forest, Extra Trees

Ricerca iperparametri con GridSearchCV

Valutazione tramite accuratezza, precisione, recall, F1-score e confusion matrix

Struttura del repository

riconoscimento_forme_finale.ipynb – Notebook principale con tutto il workflow: generazione dati, EDA, feature extraction, modelli e valutazione.

(Opzionale) requirements.txt – elenco delle dipendenze Python.

Requisiti

Python 3.8 o superiore

Librerie Python:

numpy

pandas

scipy

scikit-learn

matplotlib

seaborn

Puoi installare tutte le dipendenze con:

pip install numpy pandas scipy scikit-learn matplotlib seaborn

Utilizzo

Clona questo repository sul tuo computer.

(Opzionale) Crea un ambiente virtuale:

python -m venv venv
source venv/bin/activate  # su Windows: venv\Scripts\activate

Installa le dipendenze:

pip install -r requirements.txt

Apri e esegui il notebook:

jupyter notebook riconoscimento_forme_finale.ipynb

Esegui le celle in sequenza. Puoi modificare i parametri di generazione del dataset (numero di forme, rumore, numero di punti) nella sezione iniziale.

Risultati

Alla fine del notebook troverai:

Grafici delle metriche di performance per ciascun modello e configurazione

Confusion matrix per problemi binari e multiclasse

Visualizzazioni PCA

Personalizzazione

Dataset: puoi aumentare il numero di forme o aggiungere nuove classi (p.es. triangolo, quadrato) estendendo la funzione di generazione.

Feature: aggiungere metriche geometriche (es. eccentricità, momenti invarianti di Hu).

Modelli: sperimentare nuove architetture o metodi ensemble.
