# 🎯 Fit Score per Servizio - Intelligenza AI per l'Assegnazione Campagne

Scopri come l'Outreach Machine utilizza l'intelligenza artificiale per valutare automaticamente la compatibilità tra i tuoi lead e i servizi offerti.

---

## ❓ Cos'è il Fit Score?

Il **Fit Score** è un punteggio da **0 a 100** che rappresenta quanto bene un lead è "compatibile" con uno dei tuoi servizi.

- **70-100**: Altissima corrispondenza → Lead ideale per questo servizio
- **50-69**: Buona corrispondenza → Lead interessante, vale la pena contattare
- **30-49**: Corrispondenza moderata → Potrebbe essere interessato, ma non è il focus
- **0-29**: Bassa corrispondenza → Probabilmente non adatto per questo servizio

Ogni fit score include anche un **Confidence Level** (0-100) che indica quanto "sicuro" è il sistema nel valutare il lead.

---

## 🔄 Il Workflow Completo

### Passo 1: Enrichment dei Lead

Prima che il sistema possa calcolare un fit score accurato, il lead deve essere **arricchito** con informazioni:

```
Lead inserito
    ↓
Sistema analizza:
  • Settore/Industria
  • Ruolo
  • Dimensione azienda
  • Esigenze dichiarate
    ↓
Lead enriched ✅
```

**Lead sottoenricchito?** Il sistema ti avviserà "Lead sottoenricchito - consigliamo di enrichire". In questo caso, aggiungi più dettagli al lead prima di assegnarlo a una campagna.

### Passo 2: Assegnazione a Campagna

Quando assegni un lead a una campagna che ha un servizio associato:

```
Lead assegnato a campagna con servizio_id
    ↓
Sistema triggera automaticamente:
  • Calcolo fit_score vs il servizio
  • Analisi con Claude AI
    ↓
Fit Score calcolato automaticamente ✅
```

**Non devi fare nulla** – il sistema calcola il fit score da solo!

### Passo 3: Visualizzazione e Suggerimenti

Dopo l'assegnazione, puoi:
- 👁️ **Visualizzare** il fit score del lead nel dettaglio
- 💡 **Ricevere suggerimenti** sul miglior servizio per il lead
- 🔀 **Riassegnare** il lead a una campagna più appropriata se consigliato

---

## 📊 Cosa Misura il Fit Score?

Il sistema analizza il lead su multiple dimensioni:

### Fattori Analizzati

| Fattore | Cosa Valuta | Importanza |
|---------|-----------|-----------|
| **Settore** | L'industria del lead corrisponde al target del servizio? | 🔴 Alta |
| **Ruolo** | La posizione del lead è in target per questo servizio? | 🔴 Alta |
| **Dimensione Azienda** | Startup vs SMB vs Enterprise - il servizio è adatto? | 🟡 Media |
| **Pain Points** | I problemi del lead sono risolti dal servizio? | 🔴 Alta |
| **Budget** | Il lead ha capacità di spesa per questo servizio? | 🟡 Media |
| **Timeline** | Il lead è pronto a una decisione adesso o dopo? | 🟢 Bassa |

---

## 💡 Come Usare i Suggerimenti Automatici

Quando un lead viene arricchito e il sistema analizza i servizi, puoi ricevere **suggerimenti automatici**:

### Scenario 1: Miglior Fit
```
Lead: "Mario Rossi - CTO @ TechStartup (10 persone)"
Servizi nel workspace:
  1. "Cloud Migration" → Fit Score 85%
  2. "Cybersecurity" → Fit Score 45%
  3. "Team Augmentation" → Fit Score 30%

📌 Sistema consiglia: Cloud Migration (85%)
```

### Scenario 2: Fit Moderato
```
Lead: "Lucia Ferrari - HR Manager @ Agenzia Pubblicitaria"
Servizi nel workspace:
  1. "Recruitment" → Fit Score 62%
  2. "Training" → Fit Score 45%
  3. "Consulting" → Fit Score 25%

📌 Sistema consiglia: Recruitment (62%)
Alternativa: Training (45%)
```

### Scenario 3: Nessun Fit Ideale
```
Lead: "Giovanni Bianchi - CFO @ Banca"
Servizi nel workspace:
  1. "Cloud Migration" → Fit Score 35%
  2. "Cybersecurity" → Fit Score 40%
  3. "Team Augmentation" → Fit Score 15%

⚠️ Nessun servizio ha alta compatibilità
💡 Puoi comunque contattare per esplorare soluzioni custom
```

---

## 📋 Breakdown del Fit Score

Ogni fit score viene scomposto in componenti per capire **perché** il lead è una buona o cattiva corrispondenza:

```json
{
  "fit_score": 78,
  "confidence": 85,
  "breakdown": {
    "settore": "Match perfetto (Tech)",
    "ruolo": "CTO - target ideale per questo servizio",
    "dimensione": "10-50 persone - fascia ideale",
    "pain_points": "Migrazione cloud non coperta",
    "budget": "Azienda in crescita, capacità media-alta"
  }
}
```

**Come leggerlo:**
- Ogni campo spiega il contributo al punteggio finale
- I campi con "Match" sono i punti di forza
- I campi con "non" o "insufficiente" sono aree deboli

---

## ⚙️ Flusso Tecnico (per Chi Vuole Sapere Di Più)

### 1️⃣ Quando Assegni un Lead a Campagna

```
POST /api/campaigns/{campaign_id}/assign-lead
{
  "lead_ids": ["lead_123", "lead_456"]
}
```

**Cosa succede:**
- Lead viene assegnato alla campagna
- Se la campagna ha un `service_id`, il sistema triggera il calcolo fit_score
- Sistema legge il lead (settore, ruolo, azienda, ecc.)
- Sistema chiama Claude AI con la Buyer Persona del servizio
- Risultato viene salvato nel database

**Risposta:**
```json
{
  "success": true,
  "assigned": 2,
  "fit_score_triggered": true,
  "fit_score_result": {
    "success": true,
    "updated": 2,
    "errors": null
  }
}
```

### 2️⃣ Quando Richiedi Suggerimenti

```
POST /api/leads/{lead_id}/suggest-campaign
```

**Cosa succede:**
- Sistema legge il lead
- Calcola fit_score vs OGNI servizio nel workspace
- Restituisce i 3 migliori candidati
- Include il servizio attuale se già assegnato

**Risposta:**
```json
{
  "success": true,
  "suggestion": {
    "campaign_id": "camp_123",
    "campaign_name": "Cloud Migration Q2",
    "service_id": "svc_456",
    "service_name": "Cloud Migration",
    "fit_score": 85,
    "confidence": 92,
    "reason": "Altissima corrispondenza",
    "breakdown": { ... }
  },
  "alternatives": [
    {
      "campaign_id": "camp_789",
      "service_name": "Cybersecurity",
      "fit_score": 45
    }
  ]
}
```

---

## ✅ Best Practices

### ✅ FAI

- **Arricchisci i lead** il più possibile prima di assegnarli
- **Monitora il Confidence Level** - se è basso (<50%), il lead potrebbe aver bisogno di più informazioni
- **Usa i suggerimenti** come guida per la riassegnazione
- **Testa il fit_score** su piccoli batch prima di scalare
- **Rivedi periodicamente** i lead con fit_score basso per capire perché

### ❌ NON FARE

- Ignorare fit_score bassi - potrebbero indicare lead non adatti
- Assegnare troppe volte lo stesso lead a campagne diverse
- Contattare lead con confidence molto bassa (<30%) senza arricchimento aggiuntivo
- Ignorare i "breakdown" che mostrano quali fattori contribuiscono al punteggio

---

## 🎯 Strategie di Utilizzo

### Strategia 1: Qualification Automatica

```
1. Importa lead in bulk
2. Arricchisci con dati pubblici (LinkedIn, web scraping, ecc.)
3. Sistema calcola fit_score automaticamente
4. Contatta solo i lead con fit_score > 70
5. Segui i lead 50-70 con messaging diverso
```

**Vantaggio**: Massimizza il ROI contattando i migliori lead prima

### Strategia 2: A/B Testing Campagne

```
Campagna A: Lead con Fit Score 70+
Campagna B: Lead con Fit Score 50-70

Misura:
- Open Rate
- Reply Rate
- Conversion Rate

→ Scopri quale fit_score range converte meglio per il tuo servizio
```

### Strategia 3: Riassegnazione Intelligente

```
1. Lead assegnato a Campagna X, ma fit_score è basso
2. Richiedi suggerimenti → Sistema propone Campagna Y
3. Riassegna il lead a Campagna Y
4. Monitora miglioramenti in metriche di risposta
```

---

## 📊 Metriche da Monitorare

Per ogni campagna, traccia la relazione tra fit_score e performance:

| Metrica | Formula | Target |
|---------|---------|--------|
| **Avg Fit Score** | Media fit_score lead in campagna | >60 |
| **Fit Score Distribution** | % lead per range (0-30, 30-50, 50-70, 70+) | 60%+ in 70+ |
| **Reply Rate by Fit** | Reply rate per range di fit_score | Aumenta con fit_score |
| **Conversion by Fit** | Clienti acquisiti per range di fit_score | >80% da 70+ |

---

## ❓ FAQ - Fit Score

**D: Perché il fit_score di un lead è cambato?**  
A: Il fit_score si aggiorna quando:
- Aggiungi nuove informazioni al lead
- Modifichi la Buyer Persona del servizio
- Aggiorni la descrizione del servizio

**D: Posso forzare il ricalcolo del fit_score?**  
A: Sì - quando assegni un lead a una campagna con servizio, il fit_score viene ricalcolato automaticamente. Se vuoi un ricalcolo manuale, contatta l'admin.

**D: Cosa significa "Lead sottoenricchito"?**  
A: Il sistema non ha abbastanza informazioni per fare una valutazione affidabile (Confidence < 50%). Aggiungi dettagli: settore, ruolo, azienda, problemi specifici.

**D: Il Confidence Level è basso - cosa faccio?**  
A: Arricchisci il lead:
- Visita il sito aziendale del lead
- Cerca il profilo LinkedIn
- Aggiungi note su settore, ruolo, esigenze
- Riassegna → Confidence aumenterà

**D: Quale fit_score è "buono"?**  
A: Dipende dal tuo settore, ma:
- **70+**: Contatta prima questi
- **50-69**: Segui con messaging meno aggressivo
- **<50**: O arricchisci o scarta

**D: Posso vedere il fit_score per TUTTI i servizi, non solo quello della campagna?**  
A: Sì! Usa la feature "Suggerisci Campagna" per vedere il fit_score vs tutti i servizi contemporaneamente.

---

## 🆘 Troubleshooting - Fit Score

**Problema: Fit Score non è stato calcolato dopo l'assegnazione**

Possibili cause:
- Campagna non ha un servizio associato
- Lead non è arricchito abbastanza
- Errore di sistema (contatta admin)

Soluzione:
1. Verifica che la campagna abbia un servizio
2. Arricchisci il lead con più dati
3. Riassegna il lead alla campagna
4. Attendi alcuni secondi per il ricalcolo

**Problema: Confidence Level è molto basso**

Cause:
- Lead senza informazioni sul settore
- Lead senza informazioni sul ruolo
- Lead senza dati aziendali

Soluzione:
- Completa tutti i campi disponibili del lead
- Aggiungi note descrittive nelle note del lead
- Riassegna → Confidence aumenterà

**Problema: Suggerimenti non sembrano accurati**

Possibili motivi:
- Buyer Persona non ben definita per il servizio
- Lead non abbastanza arricchito
- Servizio target non ben configurato

Soluzione:
1. Rivedi la Buyer Persona del servizio
2. Migliora la descrizione del servizio
3. Arricchisci il lead con informazioni aggiuntive
4. Contatta admin per aiuto sulla Buyer Persona

---

[← Torna a Campaigns](campaigns) | [Email Automation →](email-automation)
