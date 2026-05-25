# 👥 Lead Management - Gestisci i Tuoi Lead

Guida completa per importare, visualizzare e gestire i tuoi lead.

---

## 📥 Importazione Lead

### Metodo 1: Importa da CSV

**Che cos'è un CSV?**
Un file CSV è un file di testo semplice con i tuoi lead. Puoi crearlo in Excel/Google Sheets.

**Come esportare da Excel:**
1. Apri il tuo file Excel
2. File → Esporta come → CSV
3. Salva il file

**Campi supportati:**
```
First Name       (Nome)
Last Name        (Cognome)
Email            (Email)
Company          (Azienda)
Job Title        (Posizione lavorativa)
Website          (Sito aziendale)
Location         (Città/Provincia)
Industry         (Settore)
Company Size     (Dimensioni azienda)
LinkedIn URL     (Profilo LinkedIn)
```

**Come importare:**
1. Clicca **"LEAD"** nel menu
2. Clicca **"Importa Lead"**
3. Drag & drop il file CSV (oppure clicca per selezionare)
4. Verifica il **field mapping** (i tuoi campi → i nostri campi)
5. Clicca **"Importa"**

✅ I tuoi lead sono importati!

**💡 Consiglio:** Inizia con 10-20 lead per testare prima di importarne 1000

---

### Metodo 2: Importa da Apollo

Apollo è un database di milioni di profili professionali. Se hai account Apollo:

1. Vai su apollo.io
2. Cerca i tuoi lead target
3. Esporta come CSV
4. Importa in Outreach Machine (vedi Metodo 1)

**Vantaggi Apollo:**
- Database con milioni di profili
- Filtra per settore, ruolo, azienda
- Email verified e updated
- Integrazione diretta

---

## 👁️ Visualizzazione Lead

### Tabella Lead
La tabella mostra tutti i tuoi lead con colonne:

| Colonna | Significa |
|---------|-----------|
| **Name** | Nome cognome |
| **Email** | Indirizzo email |
| **Company** | Azienda |
| **Role** | Posizione lavorativa |
| **Settore** | Settore aziendale (dalla risorsa Apollo) |
| **Status** | Stato del lead (vedi sotto) |
| **Campaign** | In quale campagna è |
| **Replied** | Ha risposto? (sì/no) |

### Stati Lead

Ogni lead ha uno stato:

```
📩 IMPORTED    → Lead appena importato
📧 SENT        → Email inviata
💬 REPLIED     → Ha risposto alla email
✅ CONVERTED   → Diventato cliente
❌ ERROR       → Email bounced o errore
📋 ARCHIVED    → Lead archiviato
```

---

## 🔍 Filtri & Ricerca

### Filtra per Status
1. Clicca il dropdown **"Status"** in alto
2. Seleziona: Imported, Sent, Replied, Converted, Error, Archived
3. La tabella si aggiorna automaticamente

**Esempi:**
- "Replied" → Vedi solo lead che hanno risposto
- "Imported" → Lead non ancora contattati
- "Converted" → Clienti acquisiti

### Filtra per Settore
1. Clicca il dropdown **"Settore"**
2. Seleziona il settore (es: "Technology", "Finance", "Healthcare")
3. Vedrai solo lead in quel settore

**Settori disponibili:**
- Technology
- Finance
- Healthcare
- Manufacturing
- Retail
- E-commerce
- [altri...]

### Filtra per Campagna
1. Clicca il dropdown **"Campaign"**
2. Seleziona la campagna (es: "Q2 Outreach")
3. Vedrai solo lead in quella campagna

### Ricerca Testo
1. Usa la **barra di ricerca** in alto
2. Scrivi un nome, email o azienda
3. Risultati si aggiornano in tempo reale

**Esempi:**
- "Marco Rossi" → Cerca per nome
- "marco@azienda.it" → Cerca per email
- "Apple" → Cerca azienda

---

## ✏️ Modifica Lead

### Modifica un Singolo Lead

1. Clicca sul lead nella tabella
2. Si apre un **drawer** (pannello) a destra
3. Modifica i campi che vuoi:
   - Nome, email, azienda
   - Status, campagna, note
   - Persona (per generazione email AI)
4. Clicca **"Salva"**

### Modifica Multipli Lead

**Cambia status a più lead:**
1. Seleziona i lead (checkbox a sinistra)
2. Clicca **"Bulk Update"** in alto
3. Seleziona nuovo status (es: "Replied")
4. Clicca **"Aggiorna"**

**Sposta più lead in una campagna:**
1. Seleziona i lead
2. Clicca **"Bulk Update"**
3. Seleziona campagna
4. Clicca **"Aggiorna"**

---

## 🗑️ Elimina Lead

### Elimina un Singolo Lead
1. Clicca sul lead
2. Clicca **"Elimina"** (icona cestino)
3. Conferma

### Elimina Multipli Lead
1. Seleziona i lead (checkbox)
2. Clicca **"Bulk Delete"**
3. Conferma

⚠️ **Attenzione:** L'eliminazione è permanente!

---

## 💡 Lead Enrichment

"Enrichment" significa aggiungere informazioni ai tuoi lead da fonti esterne.

### Quali Informazioni Aggiungiamo?

Automaticamente aggiungiamo:
- ✅ **Settore azienda** (da Apollo)
- ✅ **Dimensioni azienda** (numero dipendenti)
- ✅ **Revenue annuale**
- ✅ **Sito web aziendale**
- ✅ **LinkedIn URL**
- ✅ **Contatti aggiuntivi** (altre persone in azienda)

### Quando Enrichiamo?

All'importazione, il sistema:
1. Verifica il dominio email
2. Cerca l'azienda su Apollo
3. Aggiunge tutti i dati disponibili

⏱️ Impiega qualche secondo per lead.

---

## 🎯 Best Practices per Lead Management

**✅ FAI:**
- Importa lead qualificati (che hanno realmente interesse)
- Usa categorie/filtri per organizzare
- Archiva lead non interessati
- Monitora il status "Replied"
- Arricchisci i lead regolarmente

**❌ NON FARE:**
- Importare liste troppo grandi senza qualificarle
- Inviare email a persone che non hanno interesse
- Trascurare i lead che rispondono
- Tenere i lead "Imported" per mesi senza contatto

---

## ❓ FAQ - Lead Management

**D: Posso importare il doppio della stessa email?**  
A: No, il sistema blocca automaticamente i duplicati per email.

**D: Quanto tempo impiega l'importazione?**  
A: Dipende dal numero: 100 lead = 1 minuto, 1000 lead = 5 minuti

**D: Posso fare bulk update di note?**  
A: Attualmente il bulk update funziona per status e campagna. Per note, edita uno per uno.

**D: Che cosa significa "Settore Azienda"?**  
A: È il settore industriale dell'azienda del lead (es: Automotive, Chemicals, Technology, Finance, Healthcare).

**D: Posso esportare i lead?**  
A: Sì! Seleziona i lead, clicca "Esporta CSV"

---

## 🆘 Troubleshooting

**Problema: L'importazione fallisce**  
Soluzione: Verifica che il file CSV abbia almeno "Email" come colonna

**Problema: Non vedo i filtri**  
Soluzione: Clicca il bottone "Filtri" in alto a sinistra

**Problema: Un lead è scomparso**  
Soluzione: Potrebbe essere archiviato. Clicca filtro Status → "Archived"

**Problema: Voglio recuperare lead eliminati**  
Soluzione: Sfortunatamente una volta eliminati non possono essere recuperati. Usa il backup/esporta regolarmente!

---

[← Torna a Getting Started](getting-started) | [Campaigns →](campaigns)
