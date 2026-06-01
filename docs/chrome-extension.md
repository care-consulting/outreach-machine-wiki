# Estensione Chrome - Outreach Machine

## Overview

L'estensione Chrome di Outreach Machine consente agli utenti di importare contatti LinkedIn direttamente nell'applicazione. L'estensione è personalizzata per ogni workspace con un API key univoco incorporato.

## Download e Installazione

### Download Personalizato

Ogni utente autenticato può scaricare una versione personalizzata dell'estensione:

1. Accedi a Outreach Machine
2. Vai a **Impostazioni** → **Estensione Chrome**
3. Clicca su **Scarica Estensione**
4. Un file ZIP `outreach-machine-extension.zip` verrà scaricato

### Instalazione in Chrome

1. Estrai il file ZIP in una cartella sul tuo computer
2. Apri Chrome e vai a `chrome://extensions/`
3. Attiva **Modalità sviluppatore** (toggle in alto a destra)
4. Clicca su **Carica estensione non pacchettizzata**
5. Seleziona la cartella estratta

L'estensione è ora installata e pronta all'uso.

## Come Funziona

### Estrazione Contatti LinkedIn

1. Vai su LinkedIn e apri il profilo di un contatto
2. L'estensione mostrerà un'icona nel browser
3. Clicca sull'icona per estrarre i dati dal profilo:
   - Nome
   - Ruolo
   - Azienda
   - Ubicazione
   - URL LinkedIn
   - Settore

### Importazione in Outreach Machine

1. Dopo l'estrazione, l'estensione mostra una lista di contatti estratti
2. Seleziona i contatti che vuoi importare
3. Scegli una campagna di destinazione
4. Clicca su **Importa**

I contatti verranno aggiunti alla campagna selezionata con stato "Importato da LinkedIn".

## Dettagli Tecnici

### Architettura

L'estensione è composta da:

- **manifest.json** - Configurazione dell'estensione
- **background.js** - Service Worker che gestisce l'API key
- **content.js** - Script iniettato nelle pagine LinkedIn
- **popup.html/popup.js** - UI della popup dell'estensione
- **icon*.png** - Icone per la barra dei comandi

### API Key

Ogni workspace ha un'API key univoca generata automaticamente. L'API key è incorporata nel file `background.js` durante il download e viene salvata nel storage del browser alla prima installazione.

**⚠️ Sicurezza:** L'API key è presente nel file ZIP scaricato. Non condividere l'estensione con altri - ogni utente deve scaricare la propria copia personalizzata.

### Endpoint API

L'estensione comunica con l'applicazione tramite:

**GET /api/extension**
- Query: `action=ping` - Verifica connessione
- Query: `action=campaigns` - Ottiene liste campagne attive

**POST /api/extension**
- Body: Dati contatto estratto
- Response: ID lead creato

Tutti i requests includono l'header: `x-api-key: {workspace_api_key}`

## Troubleshooting

### "L'estensione non si carica"
- Verifica di aver estratto completamente il file ZIP
- Controlla che manifest.json sia nella cartella radice
- Abilita la "Modalità sviluppatore" su `chrome://extensions/`

### "Errore durante l'importazione"
- Verifica di essere autenticato in Outreach Machine
- Assicurati che la campagna di destinazione esista ed sia attiva
- Controlla la connessione a internet

### "L'estensione non estrae i dati da LinkedIn"
- LinkedIn potrebbe aver bloccato l'estensione - ricarica la pagina
- Verifica che il profilo LinkedIn sia accessibile al tuo account
- Prova con un profilo pubblico come test

## Storico Implementazione

### Data: 2026-06-01

**Problema risolto:** Download dell'estensione per il workspace di Marianna

**Soluzione:**
- Creato endpoint `GET /api/extension/download` che genera un ZIP personalizzato
- L'endpoint:
  1. Autentica l'utente tramite Supabase
  2. Recupera il workspace dell'utente
  3. Cerca o crea un'API key per il workspace
  4. Genera un ZIP con l'estensione e il background.js personalizzato
  5. Ritorna il ZIP pronto per il download

**Miglioramenti:**
- API key univoca per workspace garantisce isolamento dei dati
- ZIP generato dinamicamente con API key incorporato
- Supporto per più workspaces simultanei

**Problemi riscontrati e soluzioni:**
1. RLS policy ricorsiva su `workspace_members` → Fixata con migration che utilizza subquery non-ricorsive
2. Incompatibilità archiver con Turbopack → Sostituito con jszip (modulo JavaScript puro)
3. Query `.single()` fallava senza API key → Cambiato a `.maybeSingle()` per permettere zero righe

**Test:**
- ✅ Download extension per utente autenticato
- ✅ Generazione ZIP con API key personalizzata
- ✅ Import da LinkedIn funzionante

---

**Versione:** 1.0  
**Ultimo aggiornamento:** 2026-06-01  
**Autore:** Sistema Outreach Machine
