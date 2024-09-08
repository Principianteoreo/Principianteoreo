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
# Definizione delle variabili principali
polo_neutro = 0
polo_negativo = -1
polo_positivo = 1

# Parametri per l'inizio e fine del periodo specificato
inizio_periodo = "2024-09-09 00:00:00"
fine_periodo = "2024-09-20 00:00:00"

# Funzione per incrementare il potenziale positivo
def aumenta_potenziale(realta, incremento):
    realta['potenziale'] += incremento
    return realta

# Funzione per bloccare il polo negativo
def blocca_polo_negativo(realta, inizio, fine, velocita):
    if inizio <= current_time <= fine:
        realta['polo_negativo_bloccato'] = True
        realta['velocita_blocco'] = velocita
    return realta

# Funzione per neutralizzare le influenze negative
def neutralizza_influenze(realta, velocita_indifferenza, pop_influenzata):
    realta['influenze_negative'] = 'neutralizzate'
    realta['velocita_indifferenza'] = velocita_indifferenza
    realta['pop_influenzata'] = pop_influenzata
    return realta

# Funzione per approvazione scientifica
def approvazione_teoria(teoria, data):
    if current_time == data:
        teoria['approvata'] = True
    return teoria

# Funzione per crescita delle foglie nei parchi
def crescita_foglie(parchi, velocita_crescita):
    parchi['foglie_ganja'] = True
    parchi['velocita_crescita'] = velocita_crescita
    return parchi

# Simulazione dell'esecuzione del codice
current_time = "2024-09-10 00:00:00"
realta = {
    'potenziale': 100,
    'polo_negativo_bloccato': False,
    'velocita_blocco': 0,
    'influenze_negative': 'presenti',
    'velocita_indifferenza': 0,
    'pop_influenzata': 0
}

teoria = {
    'approvata': False,
    'nome': "(0+0)x(0+0) = 0"
}

parchi = {
    'foglie_ganja': False,
    'velocita_crescita': 0
}

# Incremento del potenziale positivo
realta = aumenta_potenziale(realta, 5)

# Blocco del polo negativo
realta = blocca_polo_negativo(realta, inizio_periodo, fine_periodo, 33)

# Neutralizzazione delle influenze negative
realta = neutralizza_influenze(realta, 33, 11)

# Approvazione della teoria nel 2030
teoria = approvazione_teoria(teoria, "2030-01-01 00:00:00")

# Crescita delle foglie di ganja nei parchi italiani
parchi = crescita_foglie(parchi, 11)

print(realta)
print(teoria)
print(parchi)
