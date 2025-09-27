# SEMPL-IT: un modello di intelligenza artificiale per la semplificazione dell'italiano
Vittorio Ganfi e Marco Russodivito


## Abstract
La complessità testuale dei documenti amministrativi rappresenta un ostacolo significativo per la loro piena comprensione e fruizione da parte dei cittadini. Numerosi studi, tra cui quelli di Fioritto 1997; Piemontese 1996, 2023; Cortelazzo 2021; Cortelazzo/Pellegrino 2003, hanno evidenziato come il linguaggio burocratico sia spesso caratterizzato da strutture morfosintattiche e lessicali complesse, che riducono drasticamente la leggibilità dei testi prodotti dalle pubbliche amministrazioni. Per affrontare questo, la semplificazione linguistica si configura come una strategia cruciale. Negli ultimi decenni, il progresso tecnologico ha aperto nuove prospettive per la semplificazione automatica dei testi, con particolare attenzione all’uso dell’intelligenza artificiale (AI). Questo articolo presenta una prima versione del Large Language Model (d’ora innanzi LLM) SEMPL-IT, sviluppato per semplificare i testi amministrativi redatti in lingua italiana.


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


## How to cite us
Vittorio Ganfi e Marco Russodivito (2025). SEMPL-IT: un modello di intelligenza artificiale per la semplificazione dell'italiano. In *Giuliana Fiorentino, Alessandro Cioffi, Maria Ausilia Simonelli (a cura di), AMMINISTRAZIONE ATTIVA. Semplicità e chiarezza per la comunicazione amministrativa (Quaderni della Rassegna, 254). Firenze: Franco Cesati Editore. ISBN 979-12-5496-268-8*.

```bibtex
@inproceedings{ganfi2025semplit,
  title     = {SEMPL-IT: un modello di intelligenza artificiale per la semplificazione dell'italiano},
  author    = {Ganfi, Vittorio AND Russodivito, Marco},
  booktitle = {AMMINISTRAZIONE ATTIVA. Semplicità e chiarezza per la comunicazione amministrativa},
  editor    = {Fiorentino, Giuliana AND Cioffi, Alessandro AND Simonelli, Maria Ausilia},
  series    = {Quaderni della Rassegna},
  volume    = {254},
  publisher = {Franco Cesati Editore},
  address   = {Firenze},
  year      = {2025},
  isbn      = {979-12-5496-268-8}
}
```