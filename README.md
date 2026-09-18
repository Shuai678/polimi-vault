# Polimi Vault

Raccolta personale di appunti e materiali di studio per il percorso al Politecnico di Milano, organizzata come vault [Obsidian](https://obsidian.md/).

Il vault non è soltanto un archivio di lezioni: collega corsi, concetti, esercizi ed errori per facilitare il ripasso e la preparazione degli esami. I contenuti sono in continua evoluzione e non costituiscono materiale ufficiale del Politecnico di Milano.

## Contenuto

- **`00 Dashboard`** — punto di accesso principale al vault.
- **`01 Courses`** — corsi suddivisi per anno accademico e semestre.
- **`02 Shared Concepts`** — concetti utili in più insegnamenti.
- **`03 Resources`** — libri, formulari e collegamenti utili.
- **`04 Templates`** — modelli per creare note con una struttura coerente.
- **`99 Archive`** — materiale non più attivo, conservato per riferimento.

Al momento il primo semestre dell'anno accademico 2026-2027 comprende:

- Analisi Matematica 1;
- Algebra Lineare;
- Fondamenti di Informatica.

## Struttura di un corso

Ogni corso può contenere:

- **Course Map** — programma, dipendenze tra argomenti e avanzamento;
- **Learning Memory** — cosa è stato compreso, cosa va ripassato e quale sarà il prossimo passo;
- **Exam Book** — formule, condizioni, errori ricorrenti e strategie d'esame;
- **Lectures** — note cronologiche delle lezioni;
- **Concepts** — conoscenze consolidate, organizzate per argomento;
- **Exercises** — esercizi e metodi risolutivi;
- **Exams** — prove d'esame e osservazioni;
- **Knowledge Map** — rappresentazione visuale dei collegamenti principali.

## Come usare il vault

1. Installa [Obsidian](https://obsidian.md/download).
2. Clona il repository:

   ```bash
   git clone git@github.com:Shuai678/polimi-vault.git
   ```

3. In Obsidian scegli **Open folder as vault** e seleziona la cartella `polimi-vault`.
4. Apri la [Home](<00 Dashboard/Home.md>) e raggiungi da lì il semestre e il corso desiderato.

La configurazione essenziale di Obsidian è inclusa. I plugin della community e lo stato locale dell'interfaccia non vengono versionati, perché possono variare da dispositivo a dispositivo.

## Flusso di studio consigliato

1. Prima della lezione, consulta la **Course Map** e la **Learning Memory** del corso.
2. Crea la nota della nuova lezione usando il template dedicato.
3. Dopo la lezione, sposta le conoscenze durature nelle note in **Concepts**.
4. Collega concetti, esercizi e lezioni usando i wikilink di Obsidian (`[[Nome nota]]`).
5. Aggiorna la **Learning Memory** con dubbi e prossimi passi.
6. Registra nell'**Exam Book** gli errori ricorrenti e le condizioni dei teoremi o delle formule.

I template disponibili in [`04 Templates`](<04 Templates>) aiutano a mantenere uniforme la struttura delle note.

## Aggiornare il repository

Prima di iniziare una sessione di studio, recupera gli ultimi aggiornamenti:

```bash
git pull --rebase origin main
```

Al termine, controlla e pubblica le modifiche:

```bash
git status
git add "01 Courses" "02 Shared Concepts" "03 Resources" "04 Templates" README.md
git commit -m "Aggiorna appunti"
git push origin main
```

Controlla sempre l'output di `git status` prima del commit, soprattutto se il vault si trova in una cartella sincronizzata anche tramite iCloud.

## Avvertenza

Questi appunti sono personali e possono contenere errori o parti incomplete. Per programma, modalità d'esame e comunicazioni ufficiali, fare sempre riferimento ai docenti e ai servizi del Politecnico di Milano.
