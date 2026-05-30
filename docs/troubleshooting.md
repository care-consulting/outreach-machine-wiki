# 🆘 Troubleshooting - Risolvi i Problemi

Guida rapida per risolvere i problemi comuni su Outreach Machine.

---

## 📥 Problemi di Importazione Lead

### Problema: L'importazione fallisce
**Cosa vedi:** Errore durante l'upload del CSV

**Cause possibili:**
- File CSV non valido o corrotto
- Colonna "Email" mancante
- File troppo grande (>10MB)
- Formato non supportato

**Soluzione:**
1. Verifica che il CSV abbia almeno la colonna "Email"
2. Riprova con un file CSV piccolo (10 lead)
3. Se funziona, il problema è il file grande - dividi in chunk
4. Esporta Excel come CSV (UTF-8, separatore virgola)

---

### Problema: I lead importati non hanno i dati enrichiti
**Cosa vedi:** Campi come Company, Settore, Industry sono vuoti

**Cause possibili:**
- Enrichment ancora in corso (ci vuole tempo)
- Dati non disponibili da Apollo
- Email non valida

**Soluzione:**
1. Attendi 5-10 minuti (enrichment è asincrono)
2. Aggiorna la pagina (F5)
3. Se ancora vuoto, controlla manualmente l'email del lead

---

### Problema: Duplicate lead importati
**Cosa vedi:** Stesso lead importato due volte con email identica

**Cause possibili:**
- Hai importato lo stesso CSV due volte
- Due persone hanno stessa email (raro)

**Soluzione:**
1. Sistema blocca i duplicati per email automaticamente
2. Se vedi duplicati, significa email diversa
3. Controlla: marcorossi@azienda.it vs marco.rossi@azienda.it (spazi, punti)
4. Elimina i duplicati manualmente

---

### Problema: Importazione interrotta a metà
**Cosa vedi:** Alcuni lead importati, altri no

**Cause possibili:**
- Connessione internet interrotta
- Server non ha risposto
- File corrotto

**Soluzione:**
1. Controlla internet connection (speedtest)
2. Riprova l'importazione
3. Se continua a fallire, dividi il file CSV in pezzi più piccoli
4. Importa pezzi uno per uno

---

## 👥 Problemi con Lead

### Problema: Non vedo i miei lead nella tabella
**Cosa vedi:** Tabella vuota anche se hai importato lead

**Cause possibili:**
- I lead sono in una campagna (nascosti da filtri)
- I lead sono archiviati
- Filtri attivi nascondono i lead

**Soluzione:**
1. Clicca su "Filtri" in alto
2. Assicurati che Status non sia "Archived"
3. Assicurati che non ci sia filtro "Campaign" attivo
4. Se lead esiste, appare nella ricerca testo

---

### Problema: Un lead è scomparso
**Cosa vedi:** Un lead che avevo non c'è più

**Cause possibili:**
- Lead è stato archiviato
- Lead è stato eliminato
- Lead è stato spostato in un'altra campagna

**Soluzione:**
1. Filtra per Status = "Archived" (vedi se c'è)
2. Se non lo trovi, è stato eliminato (non recuperabile)
3. Ricorda: fai backup regolari con "Esporta CSV"

---

### Problema: Non posso modificare i dati di un lead
**Cosa vedi:** Campi di modifica bloccati o read-only

**Cause possibili:**
- Lead è in una campagna attiva
- Permessi insufficienti
- Browser cache

**Soluzione:**
1. Aggiorna la pagina (F5)
2. Prova con un altro browser
3. Se lead è in campagna attiva, mettila in pausa prima

---

### Problema: Placeholder [First Name] non si riempie nell'email
**Cosa vedi:** Email inviata con [First Name] letterale invece del nome

**Cause possibili:**
- Lead non ha "First Name" nel profilo
- Campo First Name è vuoto
- Placeholder scritto male: [firstname] invece di [First Name] (maiuscole importanti!)

**Soluzione:**
1. Verifica il profilo del lead: clicca, vedi First Name
2. Se vuoto, modifica manualmente
3. Verifica placeholder: [First Name] (case-sensitive)
4. Prova con lead che ha tutti i dati

---

## 🎯 Problemi con Campagne

### Problema: Non posso creare una campagna
**Cosa vedi:** Bottone "Crea Campagna" disabilitato o errore

**Cause possibili:**
- Nessun lead selezionato
- Nessun lead disponibile (tutti in altre campagne)
- Nome campagna già esiste

**Soluzione:**
1. Assicurati di selezionare almeno 1 lead con checkbox
2. Controlla che i lead non siano già in un'altra campagna
3. Dai un nome univoco alla campagna (es: "Q2 2026 Tech")

---

### Problema: La campagna è sparita
**Cosa vedi:** Una campagna che avevo non si vede più

**Cause possibili:**
- Campagna è stata completata e archiviata
- Filtri nascondono la campagna
- Campagna è stata eliminata

**Soluzione:**
1. Scorri in basso nella lista campagne
2. Vedi se c'è una sezione "Archived Campaigns"
3. Se completata, ancora vedi i dati ma è in archivio
4. Se eliminata, non è recuperabile

---

### Problema: Voglio aggiungere lead a una campagna esistente
**Cosa vedi:** Campagna creata, ma voglio aggiungere altri lead

**Soluzione:**
1. Clicca sulla campagna
2. Clicca "Modifica"
3. Seleziona i nuovi lead
4. Clicca "Salva"

---

### Problema: Non posso mettere pausa a una campagna
**Cosa vedi:** Bottone pausa disabilitato

**Cause possibili:**
- Campagna già completata (non si può mettere in pausa una completata)
- Permessi insufficienti

**Soluzione:**
1. Se è completata, è in archivio e non si modifica
2. Se è attiva, il bottone pausa deve funzionare
3. Aggiorna pagina (F5)

---

## 📧 Problemi con Email

### Problema: Email non viene mandata all'ora indicata
**Cosa vedi:** Email schedulata per le 9 AM ma parte più tardi (o non parte)

**Cause possibili:**
- Scheduling non è stato confermato (controlla i log)
- Fuso orario sbagliato
- Permessi insufficienti

**Soluzione:**
1. Verifica che scheduling sia "Confermato"
2. Controlla il fuso orario (Italia = UTC+2 d'estate, UTC+1 d'inverno)
3. Vedi i log di invio per errori
4. Riprova a schedularla

---

### Problema: Soggetto email è tronco
**Cosa vedi:** Nel client mail il soggetto è incompleto (vedi solo metà)

**Cause possibili:**
- Soggetto troppo lungo (>60 caratteri è male per mobile)
- Placeholder non si è riempito

**Soluzione:**
1. Accorcia il soggetto a max 60 caratteri
2. Verifica che placeholder sia corretto: [First Name], non [firstname]
3. Testa con email piccolo prima di mandare a lista grande

---

### Problema: Molti bounce (email non recapitate)
**Cosa vedi:** Status "BOUNCED" per tanti lead

**Cause possibili:**
- Email non valide
- Lista vecchia (lead non lavora più lì)
- Indirizzi fake

**Soluzione:**
1. Usa Apollo per dati verificati (più accurati)
2. Pulisci la lista manualmente (verifica email visivamente)
3. Per liste future, usa sempre dati Apollo
4. Se bounce > 5%, la lista è di qualità bassa

---

### Problema: Template email scompare
**Cosa vedi:** Template che avevo salvato non c'è più

**Cause possibili:**
- Accidentalmente eliminato
- Filtri nascondono il template
- Sistema glitch (raro)

**Soluzione:**
1. Cercalo nella lista templates
2. Se non trovi, è stato eliminato (non recuperabile)
3. Ricrea il template salvando più spesso
4. Ricorda: salva template PRIMA di mandarle (backup)

---

### Problema: Placeholder non si riempie
**Cosa vedi:** Email inviata con [Company] letterale invece del nome azienda

**Cause possibili:**
- Lead non ha il valore di quel campo
- Placeholder scritto male
- Spazi o maiuscole sbagliate

**Soluzione:**
1. Verifica il lead: ha "Company" compilato?
2. Accertati maiuscole: [Company] non [company]
3. Niente spazi: [First Name] non [ First Name ]
4. Usa solo placeholder supportati: [First Name], [Last Name], [Company], [Email], [Role], [Settore]

---

## 📊 Problemi con Analytics

### Problema: Non vedo dati di analytics
**Cosa vedi:** Dashboard vuota, nessuna metrica

**Cause possibili:**
- Nessuna email mandata ancora
- Email mandata da meno di 24 ore
- Lead non ha ricevuto email

**Soluzione:**
1. Devi aver mandato almeno 10 email prima che compaia
2. Attendi 24 ore per il tracking
3. Verifica che email sia "DELIVERED" (non bounced)

---

### Problema: Open rate è 0%
**Cosa vedi:** Nessuna email aperta anche dopo 24 ore

**Cause possibili:**
- Email appena mandate (troppo presto)
- Email non recapitate (bounce rate alto)
- Tracking non funziona (raro)

**Soluzione:**
1. Se < 24h, attendi
2. Controlla status email: sono "DELIVERED"?
3. Se molte sono "BOUNCED", pulisci lista
4. Se tutte "DELIVERED" ma 0% dopo 48h, potrebbe essere tracking

---

### Problema: Conversion rate è sempre 0%
**Cosa vedi:** Nessun lead marcato come "Converted"

**Cause possibili:**
- Non hai marcato i lead come convertiti
- I lead non hanno convertito (legittimo!)

**Soluzione:**
1. Conversion NON è automatica - devi marcare manualmente
2. Quando un lead diventa cliente:
   - Clicca sul lead
   - Cambia Status a "Converted"
   - Salva
3. Ora apparirà nei dati di analytics

---

### Problema: Metriche non si aggiornano
**Cosa vedi:** Dati analytics fermi, non cambiano

**Cause possibili:**
- Analisi cacciata (cache browser)
- Dati non ancora processati
- Glitch raro

**Soluzione:**
1. Aggiorna pagina (F5)
2. Cancella cache browser (Ctrl+Shift+Del)
3. Attendi 30 minuti (i dati si processano ogni 30 min)
4. Prova altro browser

---

## ⚙️ Problemi Generali

### Problema: Pagina non carica
**Cosa vedi:** Pagina bianca, caricamento infinito, errore

**Cause possibili:**
- Internet connection scadente
- Browser cache corrotta
- Server down (raro)

**Soluzione:**
1. Controlla internet (speedtest.net)
2. Ricaricar pagina (F5)
3. Prova Ctrl+Shift+Del (cancella cache)
4. Prova con incognito mode
5. Prova altro browser

---

### Problema: Non riesco ad accedere
**Cosa vedi:** Errore login, non entra

**Cause possibili:**
- Email/password sbagliati
- Account non confermato
- Account non esiste

**Soluzione:**
1. Verifica email esatta (maiuscole, spazi)
2. Verifica password (maiuscole importanti)
3. Se dimentichi password: Forgot Password → email reset
4. Se nuovo account: verifica email di conferma (spam?)

---

### Problema: Perdita di dati
**Cosa vedi:** Dati importanti scomparsi

**Cause possibili:**
- Lead eliminato accidentalmente
- Campagna eliminata
- Database issue (raro)

**Soluzione:**
1. Una volta eliminato, non è recuperabile
2. **Fai backup regolari:** Esporta CSV dei lead settimanalmente
3. Se importante, contatta supporto (potrebbero avere backup)

---

### Problema: Errore generico
**Cosa vedi:** Un errore che non è nella lista qui

**Soluzione:**
1. Annota il messaggio di errore esatto
2. Che azione stavi facendo?
3. Su quale pagina?
4. Contatta supporto con questi dettagli:
   - Messaggio di errore
   - Step che hai fatto
   - Browser e OS
   - Screenshot

---

## 🔧 Performance Issues

### Problema: Applicazione lenta
**Cosa vedi:** Pagine si caricano lentamente, bottoni tardano a rispondere

**Cause possibili:**
- Troppe campagne/lead caricate
- Internet lenta
- Browser con troppe tab/extension

**Soluzione:**
1. Chiudi tab non necessarie
2. Disabilita browser extension (potrebbero rallentare)
3. Usa internet più veloce
4. Filtra i dati (es: non caricare 10000 lead contemporaneamente)

---

### Problema: Errore "Quota Exceeded"
**Cosa vedi:** Errore quando cerchi di mandare email

**Cause possibili:**
- Hai raggiunto il limite email del tuo piano
- Hai raggiunto il limite API (Apollo, Brevo, etc.)

**Soluzione:**
1. Controlla il tuo piano in Settings
2. Upgrade a piano superiore se necessario
3. Attendi il reset quota (di solito mensile)
4. Contatta supporto per limiti temporanei

---

### Problema: Errore quando clicco su "Arricchimento" nella campagna
**Cosa vedi:** Errore o la funzione non risponde quando cerchi di arricchire i lead

**Cause possibili:**
- Configurazione API non valida
- Bug nell'endpoint di enrichment (RISOLTO in v1.2.4)
- Workspace non ha permessi sufficienti

**Soluzione:**
1. **Aggiorna all'ultima versione** (Commit `a742749` o successivo)
   - Il bug dei personas relationship è stato risolto
   - Se sei su Vercel, il fix è già online
2. Verifica che il workspace abbia permessi su campaigns e personas
3. Se l'errore persiste, contatta supporto con:
   - Nome del workspace
   - Email del lead che stai cercando di arricchire
   - Screenshot dell'errore

**Nota Tecnica:**
La feature di enrichment carica dati addizionali dai servizi Apollo e Tavily. Il processo è asincrono e può richiedere 10-30 secondi. Se vedi un errore immediato, è probabile che sia un issue di API.

---

## 📞 Quando Contattare il Supporto

Contatta il team se:
- ❌ Errore non risolto con troubleshooting sopra
- ❌ Perdita di dati critica
- ❌ Applicazione completamente inaccessibile
- ❌ Feature non funziona come documentato
- ❌ Errore con error code o messaggio specifico

**Quando contatti, includi:**
✅ Messaggio di errore esatto  
✅ Step che hai fatto (1, 2, 3...)  
✅ Browser e sistema operativo  
✅ Screenshot dell'errore  
✅ Timestamp di quando è successo  

---

[← Torna alla Home](home) | [FAQ →](faq) | [Best Practices →](best-practices)
