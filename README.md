# VoiceCraft

VoiceCraft is a project based on Google Magenta ddsp, it includes the script to preprocess the training data, the script to train the autoencoder for the timbre transfer, and the script to test the autoencoder recording or uploading the audio to process.

1. Il dataset utilizzato è NSynth e può essere scaricato al seguente link: https://magenta.tensorflow.org/datasets/nsynth#files.
2. Il subeset di dati su cui si vuole addestrare l'autoencoder vanno caricati in una cartella su drive.
3. Nello script di preprocessing vanno specificati la cartella con i dati di input e la cartella dove salvare l'output e il numero di frame che si vuole estrarre da ogni file audio in input (default 2 secondi).
   Lo script estrarrà i primi 2 secondi di ogni file audio e li unirà in un unico file .wav da usare come input in fase di training.
4. Nello script di training vanno specificati:
       1. Cartella contenente il file audio di input;
       2. Cartella dove salvare i checkpoint del modello;
       3. Cartella contentente i file TFRecord (creata automaticamente dallo script);
       4. Batch size;
       5. Numero di passi di training;
       6. Numero di passi dopo i quali salvare un checkpoint;
       7. Numero massimo di checkpoint da mantenere;
5. Alla fine del training è possibile scariare un file .zip contente l'ultimo checkpoint del modello;
6. Nello script di training è possibile scegliere se registrare un audio dal proprio microfono o se caricare un file (.mp3 o .wav) e la sua durata;
7. Successivamente può essere caricato un qualsiasi autoencoder precedentemente addestrato come .zip;
8. Infine è possibile ascoltare i risultati ottenuti dal modello.

