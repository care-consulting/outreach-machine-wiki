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
