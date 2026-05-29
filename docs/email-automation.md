# 📧 Email Automation - Invia Email Personalizzate

Guida per creare template email, schedularle e tracciare i risultati.

---

## 📨 Crea un Template Email

### Passo 1: Accedi alla Sezione Email
1. Clicca **"EMAIL"** nel menu
2. Clicca **"Nuovo Template"**

### Passo 2: Nome Template
Inserisci il nome del template:
- ✅ "First Contact - Tech Companies"
- ✅ "Follow-up After 3 Days"
- ✅ "Special Offer Email"

### Passo 3: Scrivi Soggetto
Il soggetto è importantissimo! Colpisce il primo impatto.

**Buoni soggetti:**
- ✅ "Scopri come aumentare le vendite del 30%"
- ✅ "Quick question about your tech stack"
- ✅ "Opportunità per [Settore] companies"

**Cattivi soggetti:**
- ❌ "Hello"
- ❌ "Important"
- ❌ "Check this out"

### Passo 4: Scrivi Corpo Email
Scrivi il messaggio principale.

**Formula efficace:**
```
1. SALUTO PERSONALE
   Ciao [First Name],

2. HOOK (Cattura attenzione)
   Ho notato che lavori in [Company]...
   Penso potremmo aiutarvi con [problema]

3. PROPOSIZIONE DI VALORE
   Offriamo [soluzione] che ha aiutato
   aziende come [competitor] a [risultato]

4. CALL TO ACTION
   Avrei 15 minuti per una call?
   Dimmi pure se ti interessa.

5. CHIUSURA PERSONALE
   [First Name], rimango in attesa
   
   Cordiali saluti,
   Marco Rossi
```

### Passo 5: Personalizzazione

Puoi usare **placeholder** che si riempiono automaticamente:

```
[First Name]    → Sostituisce con il nome del lead
[Last Name]     → Cognome
[Company]       → Azienda
[Email]         → Email
[Role]          → Posizione lavorativa
[Settore]       → Settore aziendale
```

**Esempio email personalizzata:**
```
Ciao [First Name],

Ho visto che lavori in [Company] come [Role].
Il vostro settore [Settore] è affascinante.

Potremmo aiutarvi con...

Disponibile per una call?

Cordiali,
Marco
```

Quando mandi l'email, i placeholder si riempiono con i dati del lead!

### Passo 6: Salva Template
Clicca **"Salva Template"**

✅ Il template è salvato e pronto!

---

## 📅 Schedula Email

### Step 1: Scegli Campagna
1. Clicca **"Invia Email"** dalla campagna
2. Seleziona il template che vuoi usare

### Step 2: Scegli Data e Ora
1. Clicca **"Schedula Invio"**
2. Scegli:
   - **Data:** Quando vuoi inviare (es: 25 Maggio 2026)
   - **Ora:** A che ora (es: 9:00 AM)
   - **Fuso orario:** Italia (UTC+2)

**💡 Consigli:**
- Invia durante ore di lavoro (9-11 AM, 14-16)
- Evita week-end
- Test con piccoli gruppi prima

### Step 3: Conferma
1. Rivedi email e lead
2. Clicca **"Conferma Invio"**

✅ Le email partiranno all'ora indicata!

---

## 👀 Monitora Email

Dopo l'invio puoi vedere in tempo reale:

**Status Email:**
```
📧 SENT       → Email inviata al server
📨 DELIVERED  → Email recapitata
💌 OPENED     → Email aperta da lead
🔗 CLICKED    → Lead ha clicato un link
📞 REPLIED    → Lead ha risposto
❌ BOUNCED    → Email non consegnabile
```

**Dove vedi questi dati:**
1. Vai alla campagna
2. Clicca **"Monitora Email"**
3. Vedi lo status di ogni email

---

## 📊 Analizza Performance

**Metriche Importanti:**

| Metrica | Formula | Cosa Significa |
|---------|---------|---|
| **Send Rate** | Email inviate / lead | Quante email mandiamo |
| **Delivery Rate** | Delivered / sent | Quante arrivano (non bounce) |
| **Open Rate** | Opened / delivered | % che legge l'email |
| **Reply Rate** | Replied / opened | % che risponde |
| **Conversion Rate** | Converted / sent | % che diventa cliente |

**Interpretazione:**
- Open rate 25%+ = buono
- Open rate 5-10% = medio (migliora soggetto)
- Reply rate 10%+ = eccellente
- Bounce rate < 3% = buono

---

## 💪 Come Migliorare le Email

### Se l'Open Rate è Basso (< 10%)
→ Cambia il **soggetto**
```
❌ Cattivo: "Update"
✅ Buono: "Come [Company] aumentò revenue del 40%"
```

### Se il Reply Rate è Basso (< 5%)
→ Migliora il **corpo** dell'email
```
❌ Lunghezza: 200 parole (troppo lungo)
✅ Lunghezza: 50-100 parole (veloce da leggere)

❌ Generico: "Possiamo aiutarvi"
✅ Specifico: "Abbiamo aiutato [competitor] a ridurre costi del 30%"
```

### Se il Bounce Rate è Alto (> 5%)
→ Miglior **qualità dei lead**
- Verifica che le email siano valide
- Usa dati Apollo verificati
- Pulisci liste vecchie

---

## 🤖 AI-Powered Email Generation (Avanzato)

Se il workspace ha Claude integrato, puoi usare AI per generare email:

1. Clicca **"Genera con AI"**
2. Scegli il "tone" (professionale, amichevole, aggressivo)
3. Scrivi il prompt: "Email di cold outreach per CEO di startup tech"
4. AI genera 3 versioni
5. Scegli quella che preferisci
6. Modifica/affina come vuoi

---

## ❓ FAQ - Email Automation

**D: Posso mandare email subito o devo schedularle?**  
A: Puoi fare entrambi! "Invia adesso" oppure "Schedula per dopo"

**D: Quante email posso mandare al giorno?**  
A: Dipende dal piano. Vai in Settings per vedere il limite.

**D: Se una email bounca, che succede?**  
A: Il lead passa a status "Error" e non riceve altri messaggi fino a fix manuale.

**D: Posso tracciare i click nei link?**  
A: Sì! Tracciamo automaticamente link cliccati.

**D: Posso mandare allegati?**  
A: Attualmente no, ma puoi mettere link a Drive/Dropbox nel corpo.

---

## 📊 Monitora Follow-up Email

### Come Vedere i Dati dei Follow-up

Se hai una campagna con Step 1, Step 2, Step 3:

1. Vai a **CAMPAIGNS**
2. Clicca sulla tua campagna
3. Clicca tab **EMAIL**
4. Vedi tutti gli step con metriche separate

### Metriche per Ogni Step

Ogni step ha le sue metriche:

**Step 1 (Primo contatto):**
```
📧 Sent: 12
📨 Delivered: 11 (91%)
💌 Opened: 4 (36%)
🔗 Clicked: 2 (18%)
📞 Replied: 1 (9%)
❌ Bounced: 1
```

**Step 2 (Follow-up a 7 giorni):**
```
📧 Sent: 11 (solo chi non ha risposto a Step 1)
📨 Delivered: 11 (100%)
💌 Opened: 6 (55%) ← Spesso MIGLIORE di Step 1!
🔗 Clicked: 3 (27%)
📞 Replied: 2 (18%) ← Più persone rispondono qui
```

**Step 3 (Ultimo tentativo a 10 giorni):**
```
📧 Sent: 9 (solo chi non ha risposto a Step 1 e 2)
📨 Delivered: 9 (100%)
💌 Opened: 3 (33%)
🔗 Clicked: 1 (11%)
📞 Replied: 1 (11%)
```

### Interpretazione Dati Follow-up

**Se Step 2 ha open rate più alto di Step 1:**
✅ **Normale e positivo!** Il follow-up spesso ottiene più attenzione.
- Motivo: Il lead ha visto il primo email ma era occupato, ora ha più tempo.
- Azione: Mantieni lo stesso tono/tema per continuità.

**Se Step 2 ha reply rate molto più alto:**
✅ **Eccellente!** Significa il timing a 7 giorni è perfetto.
- Il lead ha avuto tempo di considerare
- L'urgenza gentile del follow-up funziona

**Se Step 3 ha bassi numeri:**
✅ **Atteso.** Chi non ha risposto a Step 1 e 2 spesso non risponde.
- Azione: Considera se Step 3 vale la pena (dipende dal conversione rate)

### Confronto Step per Prendere Decisioni

**Domanda: Quale step è più efficace?**

Confronta le metriche:

```
                Step 1    Step 2    Step 3
Open Rate:      36%       55%       33%
Reply Rate:      9%       18%       11%
Bounce Rate:     8%        0%        0%
```

**Conclusione:** Step 2 è il più efficace (55% open, 18% reply).

**Azione:** Se vuoi modificare il template, lavora sul Step 2 per massimizzare la risposta.

### Quando i Follow-up Arrivano Davvero

**Un punto importante:** Il sistema invia i follow-up **automaticamente** ai tempi esatti.

Non serve controllare i log o fare nulla manualmente:
- ✅ Day 0: Step 1 automaticamente inviato
- ✅ Day 7: Step 2 automaticamente inviato (non devi fare nulla)
- ✅ Day 10: Step 3 automaticamente inviato (non devi fare nulla)

Puoi stare tranquillo che il timing è rispettato! 🎯

---

## 🆘 Troubleshooting

**Problema: Email non viene mandata all'ora indicata**  
Soluzione: Verifica che sia stato confermato il scheduling. Controlla i log.

**Problema: Soggetto tronco nella email**  
Soluzione: Fai il soggetto più corto (max 60 caratteri per mobile-friendly)

**Problema: Placeholder non si riempisce [First Name]**  
Soluzione: Verifica che il lead abbia effettivamente first_name nel profilo.

**Problema: Molti bounce**  
Soluzione: Verifica email valide, ripulisci lista, usa dati Apollo verificati.

---

[← Torna a Campaigns](campaigns) | [Analytics →](analytics)
