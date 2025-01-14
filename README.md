# SEMPL-IT: un modello di intelligenza artificiale per la semplificazione dell’italiano
Vittorio Ganfi e Marco Russodivito

## Abstract
In questo articolo, viene presentato un sistema di Intelligenza Artificiale, denominato SEMPL-IT e dedicato alla semplificazione del linguaggio amministrativo italiano. Come mostrato in una nutrita serie di lavori (tra gli altri, Piemontese 2023, Cortellazzo e Pellegrino 2003, Fiorentino e Ganfi in stampa), il linguaggio amministrativo è caratterizzato da strutture morfosintattiche complesse e dall'uso di un lessico poco trasparente. Tali caratteristiche possono rendere questa varietà piuttosto ostica per molti potenziali fruitori dei testi istituzionali, ostacolando la piena fruizione del contenuto testuale. Attraverso lo sviluppo di SEMPL-IT si è tentato di dare un contributo esplicito al problema della complessità dei testi amministrativi, creando uno strumento facile da usare che semplifichi automaticamente i testi.

Il modello è stato addestrato sulla base dei dati del corpus ItaIst, che colleziona testi di italiano amministrativo e consta di 915.759 token. Sfruttando tecniche avanzate di elaborazione del linguaggio naturale, sono state selezionate alcune versioni semplificate del corpus ItaIst, per le quali sono stati impiegati (a) procedure di semplificazione automatica che si sono avvalse del modello di intelligenza artificiale di OpenAI (ChatGPT) e (b) controlli manuali. Le due versioni del corpus, quella originale e quella semplificata, sono state impiegate per addestrare vari modelli di intelligenza artificiale che permettono il funzionamento di SEMPL-IT. Il software, infatti, impiegando questi modelli, se riceve come input dei testi complessi, effettua una semplificazione automatica, che accresce la leggibilità dei testi. L'efficacia delle operazioni di semplificazione viene misurata, in fine, attraverso varie metriche (ad esempio, gli indici di Gulpease o di Flesch).

## Setup
Create a virtual environment
```sh
python3 -m venv venv
source venv/bin/activate
```

Install dependencies
```sh
pip install -r requirements.txt
```

## Replication Package Content
* `corpus`: folder that contains the ItaIst corpus in `.csv` and `.xlsx` format
* `dataset`: folder that contains the simplified ItaIst dataset in `.json`, `.csv` and `.xlsx` format. It also contains the train, test and val splits.
* `1_dataset_creation`: jupyter notebook used to simplify the ItaIst corpus with OpenAI `gpt-3.5-turbo` model.
* `2_dataset_analysis`: jupyter notebook used to analyze the simplified ItaIst dataset. It employs [italian-ats-evaluator](https://github.com/RedHitMark/italian-ats-evaluator).
* `3_gpt2_small_italian`, `3_mt5_small` and `3_umt5_small`: folder that contains the jupyter notebooks used to train, upload, infer and validate `sempl-it` models.
* `4_comparison`: folder that contains the jupyter notebooks used to compare `sempl-it` with `gpt-3-5-turbo`, `gpt-4`, `gemini`, `llama3`, `phi3` and two human simplifiers.

## Acknowledgements
This contribution is a result of the research conducted within the framework of the PRIN 2020 (Progetti di Rilevante Interesse Nazionale) "VerbACxSS: on analytic verbs, complexity, synthetic verbs, and simplification. For accessibility" (Prot. 2020BJKB9M), funded by the Italian Ministero dell'Università e della Ricerca.