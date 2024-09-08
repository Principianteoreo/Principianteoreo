- 👋 Hi, I’m @Principianteoreo
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Principianteoreo/Principianteoreo is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

name: Manipolazione della Realtà

on:  
  push:  
    branches:
      - main  
  pull_request:  
    branches:
      - main  

jobs:
  manipola_realtà:
    runs-on: ubuntu-latest  

    steps:
      - name: Checkout code  
        uses: actions/checkout@v2

      - name: Set up Python
        uses: actions/setup-python@v2
        with:
          python-version: 3.8

      - name: Manipolazione della Realtà
        run: |
          python -c "
from datetime import datetime

def manipola_realtà(polo, valore):
    if polo == 0:
        return valore  # Polo neutro: non cambia nulla
    elif polo > 0:
        return valore * (1 + polo / 100)  # Polo positivo: aumenta del %
    elif polo < 0:
        return valore * (1 + polo / 100)  # Polo negativo: diminuisce del %

# Inizio manipolazione
realta = {
    'potenziale': 100,
    'polo_negativo_bloccato': False,
    'velocita_blocco': 0,
    'influenze_negative': 'presenti',
    'velocita_indifferenza': 0,
    'pop_influenzata': 0,
    'foglie_ganja': False,
    'velocita_crescita': 0
}

# Aumentare del 5% il potenziale della realtà
realta['potenziale'] = manipola_realtà(5, realta['potenziale'])
print(f'Potenziale della realtà: {realta["potenziale"]}')

# Blocco del polo negativo
inizio_periodo = datetime(2024, 9, 9)
fine_periodo = datetime(2024, 9, 20)
current_time = datetime.now()

if inizio_periodo <= current_time <= fine_periodo:
    realta['polo_negativo_bloccato'] = True
    realta['velocita_blocco'] = 33
    print(f'Polo negativo bloccato con velocità del 33%: {realta["polo_negativo_bloccato"]}')

# Neutralizzazione delle influenze negative
realta['influenze_negative'] = 'neutralizzate'
realta['velocita_indifferenza'] = 33
realta['pop_influenzata'] = 11
print(f'Influenze negative neutralizzate con velocità del 33% e l\'11% della popolazione è influenzata.')

# Previsione approvazione teoria
data_approvazione = datetime(2030, 1, 1)
if current_time >= data_approvazione:
    teoria = {'approvata': False, 'nome': '(0+0)x(0+0) = 0'}
    teoria['approvata'] = True
    print(f'Teoria \"{teoria["nome"]}\" approvata dalla comunità scientifica.')

# Crescita foglie di ganja nei parchi italiani
realta['foglie_ganja'] = True
realta['velocita_crescita'] = 11
print(f'Foglie di ganja cresciute nei parchi italiani con velocità dell\'11%.')
          "
