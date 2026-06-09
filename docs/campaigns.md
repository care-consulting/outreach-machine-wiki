# 🎯 Campaigns - Gestisci le Tue Campagne

Guida per creare, organizzare e gestire le tue campagne di outreach.

---

## ➕ Crea una Nuova Campagna

### Passo 1: Nome Campagna
1. Clicca **"CAMPAIGNS"** nel menu
2. Clicca **"Nuova Campagna"**
3. Inserisci il nome (es: "Q2 Tech Outreach 2026")

**Buoni nomi:**
- ✅ "Q2 2026 Technology Companies"
- ✅ "Finance Directors - North Italy"
- ✅ "SaaS Founders Outreach"

**Non buoni nomi:**
- ❌ "Campaign 1" (troppo generico)
- ❌ "Test" (non specifico)

### Passo 2: Descrizione (Opzionale)
Aggiungi una breve descrizione:
- Settore target
- Ruolo target
- Obiettivo della campagna

Esempio:
```
Target: Technology Companies in Italy
Role: CTO, VP Engineering
Goal: Book demos for product X
```

### Passo 3: Seleziona Lead
1. Vedi la lista di tutti i lead
2. Seleziona i lead per questa campagna (checkbox)
3. Clicca **"Crea Campagna"**

✅ La campagna è creata!

### 💡 Bonus: Crea Buyer Personas Direttamente dalla Campagna

Mentre stai creando la campagna, puoi aggiungere rapidamente nuove **buyer personas** senza uscire dal flusso:

**Come funziona:**
1. Durante la creazione della campagna, vedrai una sezione **"Nuova buyer persona"**
2. Compila i campi:
   - **Nome persona** *(es. "Mario, il consulente")*
   - **Ruolo** *(es. "CEO", "Direttore Marketing")*
3. Clicca **"Crea Persona"**
4. Vedrai un'animazione ⚙️ **"Creando persona..."** mentre il sistema crea la persona in background

**Dopo la creazione (Success State):**
- Appare ✅ **"Persona creata!"** con i dettagli
- Puoi scegliere di:
  - **"Vai a Personas e modifica →"** - Vai al tab Personas per editare dettagli avanzati (tono, istruzioni, ecc.)
  - **"Continua nella campagna"** - Rimani nella campagna e crea un'altra persona se vuoi

**Vantaggi:**
- ✅ Creare personas al volo senza interrompere il flusso di creazione campagna
- ✅ Feedback visivo chiaro durante la creazione
- ✅ La persona è subito disponibile nel sistema
- ✅ Puoi continuare a creare altre personas o completare la campagna

---

## 📋 Visualizza Campagne

Clicca **"CAMPAIGNS"** per vedere tutte le tue campagne.

Per ogni campagna vedi:
- **Nome** della campagna
- **# Lead** - quanti lead sono in questa campagna
- **Status** - Attiva, In pausa, Completata
- **Email Sent** - quante email inviate
- **Open Rate** - % di email aperte
- **Reply Rate** - % di risposte ricevute

---

## ⚙️ Gestisci una Campagna

### Modifica Campagna
1. Clicca sulla campagna
2. Clicca **"Modifica"**
3. Cambia nome, descrizione, lead
4. Clicca **"Salva"**

### Pausa Campagna
Se non vuoi mandarla avanti al momento:
1. Clicca sulla campagna
2. Clicca **"Pausa"** (icon pausa)
3. La campagna entra in pausa
4. Potrai riprenderla dopo

### Riprendi Campagna
Se era in pausa:
1. Clicca sulla campagna
2. Clicca **"Riprendi"** (icon play)
3. La campagna ricomincia

### Completa Campagna
Quando finisci una campagna:
1. Clicca sulla campagna
2. Clicca **"Completa"**
3. La campagna va in archivio
4. Vedrai comunque i risultati

### Duplica Campagna
Quando duplichi una campagna:

- viene copiata la campagna
- vengono copiati anche gli step della sequenza
- **i lead non vengono copiati**

Dopo la duplicazione:
1. Rinomina la nuova campagna
2. Vai nel tab **Lead**
3. Assegna manualmente i lead alla nuova campagna

Il sistema mostra anche un promemoria con link diretto al tab **Lead**.

---

## 🔀 Consolidamento Campagne (Merge)

Se hai due campagne simili che vuoi unire in una:

### Scenario Esempio
Hai:
- "Recruiting Campaign A" (15 lead)
- "Recruiting Campaign B" (12 lead)

Vuoi unire in una sola: "Sistema Recruiting CARE"

### Come Fare (per Admin)
Contact l'amministratore - ha un tool speciale per unire campagne.

---

## 🤖 Fit Score Automatico per Servizio

Quando assegni un lead a una campagna che ha un **servizio associato**, il sistema calcola automaticamente il **Fit Score** - un punteggio di compatibilità tra il lead e il servizio.

### Come Funziona

```
Lead assegnato a campagna + campagna ha servizio
         ↓
Sistema analizza automaticamente il lead
         ↓
Calcola Fit Score vs il servizio (0-100)
         ↓
Fit Score salvato e visualizzabile nel lead
```

### Cosa Succede Automaticamente

Quando assegni uno o più lead a una campagna:

1. ✅ **Assegnazione**: Lead vengono assegnati alla campagna
2. 🤖 **Fit Score Auto-Calculate**: Se la campagna ha un servizio, il sistema triggera il calcolo
3. 📊 **Risultati Salvati**: Fit score, confidence level e breakdown vengono salvati per ogni lead

**Non devi fare nulla** – il sistema calcola tutto da solo in background!

### Fit Score Levels

| Score | Significato | Azione Consigliata |
|-------|-----------|-----------------|
| **70-100** | Altissima corrispondenza | 🟢 Contatta subito |
| **50-69** | Buona corrispondenza | 🟡 Includi nel follow-up |
| **30-49** | Corrispondenza moderata | 🔵 Valuta case-by-case |
| **0-29** | Bassa corrispondenza | 🔴 Considera riassegnazione |

### Confidence Level

Ogni fit score include un **Confidence Level** (0-100):
- **80-100**: Sistema molto sicuro della valutazione
- **50-79**: Abbastanza sicuro, potrebbe migliorare con più info
- **<50**: Lead sottoenricchito - consigliamo di aggiungere dettagli

---

## 💡 Suggerimenti Intelligenti Campagne

Vuoi scoprire quale campagna è MIGLIORE per un lead? Usa la feature **Suggerisci Campagna**:

```
Hai un lead interessante ma non sai quale campagna è più adatta?
         ↓
Clicca "Suggerisci Campagna" nel lead
         ↓
Sistema analizza fit_score vs TUTTI i servizi
         ↓
Ti mostra:
  🥇 Miglior campagna con fit_score
  🥈 Alternativa 1
  🥉 Alternativa 2
```

### Esempio

```
Lead: "Marco - CTO @ Startup Tech"

Sistema consiglia:
  🥇 Cloud Migration (Fit Score 85%)
     "Altissima corrispondenza"
  
  🥈 Cybersecurity (Fit Score 52%)
  
  🥉 Team Augmentation (Fit Score 38%)
```

**Vantaggi**:
- Scopri automaticamente i lead ideali per ogni servizio
- Riassegna i lead a campagne migliori basandoti sui dati
- Massimizza il ROI contattando i lead con miglior compatibilità

---

## 📊 Analytics Campagna

Dentro ogni campagna vedi i dati:

**Metriche Principali:**
```
📧 EMAIL SENT          → 50 email inviate
💌 OPENED              → 15 aperte (30%)
📞 REPLIED             → 5 risposte (10%)
✅ CONVERTED           → 2 clienti (4%)
⏰ AVG RESPONSE TIME   → 2 giorni
```

**Cosa Significa:**
- **Open Rate (30%)** = 30% delle persone ha aperto l'email
- **Reply Rate (10%)** = 10% ha risposto
- **Conversion Rate (4%)** = 4% è diventato cliente

---

## 🎯 Best Practices Campagne

**✅ FAI:**
- Dai nomi descrittivi e specifici
- Crea campagne per segmento (per ruolo, settore, geo)
- Monitora gli open rate e reply rate
- Archiva le campagne completate
- Testa con piccole campagne prima di scalare

**❌ NON FARE:**
- Creare troppe piccole campagne (consolidare)
- Inviare email non personalizzate
- Ignorare i dati di performance
- Tenere 100+ campagne attive contemporaneamente

---

## 💡 Strategie di Campagna

### Segmentazione
Crea campagne diverse per:
- **Settore:** Tech, Finance, Manufacturing
- **Ruolo:** CTO, CFO, CEO
- **Geo:** North Italy, Milan, Rome
- **Tamaño:** Startup (0-10 emp), SMB (10-100), Enterprise (100+)

### Testing
1. Crea campagna small (10-20 lead)
2. Misura open/reply rate
3. Migliora il messaggio
4. Scala con più lead

### Follow-up Automatico (IMPORTANTE!)
Il sistema invia **automaticamente** fino a 3 email in sequenza, rispettando i delay configurati nella campagna:

1. **Step 1 (Giorno 0)**: Prima email - Introduzione + problema
2. **Step 2**: Follow-up gentile dopo il delay configurato dal Step 1
3. **Step 3**: Ultimo tentativo dopo il delay configurato dal Step 2

⚠️ **Non devi fare nulla** - il sistema manda tutto automaticamente!

**Esempio Timeline:**
```
Lunedì 1 Maggio @ 09:00
└─ 📧 Step 1 inviato

Lunedì 8 Maggio @ 09:00 (delay configurato dopo Step 1)
└─ 📧 Step 2 inviato automaticamente

Giovedì 11 Maggio @ 09:00 (delay configurato dopo Step 2)
└─ 📧 Step 3 inviato automaticamente
```

**Vantaggi:**
- ✅ Non dimentichi i follow-up
- ✅ I timing sono **sempre** rispettati
- ✅ Nessun lead riceve Step 1 e Step 2 lo stesso giorno
- ✅ Puoi monitorare tutti i dati in tempo reale

---

## 📧 Come Funziona il Follow-up Email Timing (Sistema Automatico)

### La Domanda Importante
**"Può capitare che io riceva Step 1 e Step 2 lo stesso giorno?"**

**Risposta: NO! ✅** Il sistema rispetta **sempre** i delay configurati e non invia piu email allo stesso lead nello stesso giorno.

### Timeline Garantita

Quando avvii una campagna con Step 1, Step 2 e Step 3:

```
┌──────────────────────────────────────────────────────────────┐
│ GIORNO 0                                                     │
│ ├─ 🚀 Campagna avviata a 09:00                              │
│ └─ 📧 Step 1 INVIATO                                         │
│                                                              │
│ ┌──────────────────────────────────────────────────────────┐ │
│ │ Step 2 già preparato dal sistema (in attesa)            │ │
│ │ Sarà attivato quando Step 1 avrà raggiunto il suo delay │ │
│ └──────────────────────────────────────────────────────────┘ │
│                                                              │
├──────────────────────────────────────────────────────────────┤
│ GIORNO X                                                     │
│ └─ 📧 Step 2 INVIATO AUTOMATICAMENTE (delay dopo Step 1)     │
│                                                              │
│ ┌──────────────────────────────────────────────────────────┐ │
│ │ Step 3 già preparato dal sistema (in attesa)            │ │
│ │ Sarà attivato quando Step 2 avrà raggiunto il suo delay │ │
│ └──────────────────────────────────────────────────────────┘ │
│                                                              │
├──────────────────────────────────────────────────────────────┤
│ GIORNO Y                                                     │
│ └─ 📧 Step 3 INVIATO AUTOMATICAMENTE (delay dopo Step 2)     │
│                                                              │
│ ✅ CAMPAGNA COMPLETATA                                       │
└──────────────────────────────────────────────────────────────┘
```

### Come Funziona Dietro le Quinte

Quando avvii una campagna:

1. **Generazione**: Il sistema crea TUTTI i 3 step subito
   - Step 1: Marcato come "pronto" ✅
   - Step 2: Marcato come "in attesa" ⏳
   - Step 3: Marcato come "in attesa" ⏳

2. **Invio Step 1**: All'ora configurata nella campagna, Step 1 viene inviato

3. **Preparazione Step 2**: Il sistema automaticamente prepara Step 2
   - Lo attiva dopo il delay configurato da Step 1
   - Cambia stato da "in attesa" a "pronto"

4. **Invio Step 2**: Quando arriva il suo momento, Step 2 viene inviato

5. **Preparazione Step 3**: Il sistema automaticamente prepara Step 3
   - Lo attiva dopo il delay configurato da Step 2
   - Cambia stato da "in attesa" a "pronto"

6. **Invio Step 3**: Quando arriva il suo momento, Step 3 viene inviato

### Cosa Vedi nel Dashboard

Nel tab **EMAIL** della campagna vedrai:

```
Step 1
├─ Status: SENT ✅
├─ Sent At: 1 Maggio @ 09:00
└─ Recipients: 12

Step 2  
├─ Status: SENT ✅
├─ Sent At: 8 Maggio @ 09:00 (+delay dal Step 1)
└─ Recipients: 12

Step 3
├─ Status: SENT ✅
├─ Sent At: 11 Maggio @ 09:00 (+delay dal Step 2)
└─ Recipients: 12
```

### Monitoraggio in Tempo Reale

Puoi controllare lo stato dei follow-up qui:

1. Vai alla **CAMPAIGNS**
2. Clicca sulla tua campagna
3. Clicca il tab **EMAIL**
4. Vedi tutti gli step con:
   - ✅ Status (SENT, DELIVERED, OPENED, CLICKED, REPLIED)
   - 📅 Data e ora invio
   - 📊 Metriche (open rate, reply rate, bounce rate)

### Best Practices per Follow-up

**✅ FAI:**
- Usa 3-step campaign (il timing ottimale)
- Varia il tono tra gli step
  - Step 1: Introduzione professionale
  - Step 2: Valore aggiunto, risorse utili
  - Step 3: Urgenza gentile, ultima opportunità
- Monitora le metriche per ogni step
- A/B testa i soggetti

**❌ NON FARE:**
- Imposta delay coerenti con il tuo ciclo commerciale
- Non inviare step aggiuntivi manualmente (il sistema li manda automaticamente)
- Non preoccuparti dei timing (il sistema se ne occupa)

### Cosa Succede se un Lead non Risponde?

Il sistema continua a seguire la timeline anche se il lead non apre/non risponde:

```
Lead IGNORA Step 1 (non aperto)
       ↓
Step 2 arriva comunque quando il suo delay e il suo orario sono maturi
       ↓
Se lead APRE Step 2, vedi nel tab EMAIL: "Opened" ✅
       ↓
Se lead non risponde, Step 3 arriva comunque quando matura dopo Step 2
```

Non serve agire manualmente - il sistema invia tutto secondo il timing!

### Domande Frequenti sul Timing

**D: Posso cambiare i delay tra gli step?**  
A: Si, i delay dipendono dalla configurazione della campagna.

**D: E se un lead non apre Step 1?**  
A: Step 2 arriva comunque quando matura il suo delay. Spesso il follow-up ottiene risposta anche da chi ha ignorato Step 1.

**D: E se un lead risponde a Step 1?**  
A: Idealmente interrompi la campagna per quel lead (lo puoi fare manualmente). Altrimenti continua con Step 2 - di solito il lead lo ignora se già in conversazione.

**D: Posso aggiungere Step 4?**  
A: Attualmente il sistema supporta 3 step. Se vuoi più follow-up, parla con l'admin.

**D: A che ora vengono inviate le email?**  
A: All'ora configurata nella campagna, nel fuso orario del workspace. Non cambia tra i giorni.

**D: Posso mandare i follow-up il weekend?**  
A: No, il sistema salta automaticamente i weekend. Se Step 2 cade sabato, viene inviato lunedì.

---

## ❓ FAQ - Campaigns

**D: Quanti lead posso mettere in una campagna?**  
A: Illimitati! Puoi mettere 1000+ lead se vuoi.

**D: Posso cambiare i lead di una campagna dopo crearla?**  
A: Sì! Clicca modifica e aggiungi/rimuovi lead.

**D: Se elimino una campagna, cosa succede ai lead?**  
A: I lead rimangono nel sistema, solo assegnazione alla campagna viene cancellata.

**D: Qual è il reply rate buono?**  
A: Dipende dal settore, ma 5-15% è considerato buono. 20%+ è eccellente!

**D: Posso avere lead in più campagne contemporaneamente?**  
A: No, ogni lead può essere in una sola campagna.

---

## 🆘 Troubleshooting

**Problema: Non vedo i miei lead nel form di creazione**  
Soluzione: Forse sono già in un'altra campagna. Vedi la lista di tutti i lead in "LEAD" → filtra per "Imported"

**Problema: Voglio aggiungere lead a una campagna esistente**  
Soluzione: Clicca sulla campagna, modifica, aggiungi lead, salva

**Problema: La campagna è sparita**  
Soluzione: Potrebbe essere archiviata. Scorri in basso per vedere campagne archiviate.

---

[← Torna a Lead Management](lead-management) | [Fit Score per Servizio →](fit-score) | [Email Automation →](email-automation)
