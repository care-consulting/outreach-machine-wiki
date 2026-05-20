# ❓ FAQ - Domande Frequenti

Risposte alle domande più comuni su Outreach Machine.

---

## 🚀 Getting Started

**D: Come faccio a registrarmi?**  
A: Vai su https://outreach-machine.vercel.app e clicca "Sign Up". Inserisci email e password, poi verifica l'email che riceverai.

**D: Ho dimenticato la password. Come la resetto?**  
A: Clicca "Forgot Password?" nella pagina di login. Riceverai un email con il link per resettarla.

**D: Posso avere più workspace?**  
A: Attualmente uno per account, ma puoi creare tante campagne diverse nello stesso workspace.

**D: Qual è il limite di email che posso mandare?**  
A: Dipende dal tuo piano. Contatta il supporto per i dettagli sui limiti.

---

## 👥 Lead Management

**D: Che formato deve avere il CSV che importo?**  
A: Deve avere almeno la colonna "Email". Altre colonne supportate: First Name, Last Name, Company, Job Title, Website, Location, Industry, Company Size, LinkedIn URL.

**D: Posso importare lead duplicati?**  
A: No, il sistema blocca automaticamente i duplicati per email. Se cerchi di importare la stessa email due volte, la seconda viene scartata.

**D: Quanto tempo ci vuole ad importare i lead?**  
A: Dipende dalla quantità: 100 lead = ~1 minuto, 1000 lead = ~5 minuti. Ogni lead viene arricchito con dati da Apollo.

**D: Che cosa significa "Lead Enrichment"?**  
A: Il sistema aggiunge automaticamente dati al tuo lead (settore aziendale, dimensioni azienda, revenue, LinkedIn URL) da Apollo.

**D: Posso modificare i dati di un lead dopo averlo importato?**  
A: Sì! Clicca sul lead nella tabella e modifica i campi che vuoi.

**D: Se elimino un lead, posso recuperarlo?**  
A: No, l'eliminazione è permanente. Fai regolarmente backup dei tuoi lead esportando il CSV!

**D: Come filtro i lead per settore?**  
A: Usa il dropdown "Settore" in alto a sinistra della tabella lead. Vedrai solo lead in quel settore.

**D: Che differenza c'è tra "Status" e "Campaign"?**  
A: **Status** = lo stato del lead (Imported, Sent, Replied, Converted, etc.). **Campaign** = in quale campagna è assegnato.

---

## 🎯 Campaigns

**D: Quanti lead posso mettere in una campagna?**  
A: Illimitati! Puoi avere 1, 10, 100, 1000+ lead per campagna.

**D: Un lead può essere in più campagne contemporaneamente?**  
A: No, ogni lead può essere in una sola campagna alla volta.

**D: Qual è la differenza tra "Pausa" e "Completa"?**  
A: **Pausa** = la campagna si ferma ma puoi riprenderla dopo. **Completa** = la campagna va in archivio e non puoi più mandarla avanti (ma vedi comunque i risultati).

**D: Posso cambiare i lead di una campagna dopo averla creata?**  
A: Sì! Clicca sulla campagna, modifica, aggiungi/rimuovi lead, salva.

**D: Qual è il reply rate medio che dovrei aspettarmi?**  
A: Dipende dal settore, ma 5-15% è buono. 20%+ è eccellente!

**D: Come faccio a unire due campagne?**  
A: Contatta l'amministratore - ha un tool speciale per unire campagne (merge).

---

## 📧 Email Automation

**D: Posso mandare email subito oppure devo schedularle?**  
A: Puoi fare entrambi! "Invia adesso" oppure "Schedula per dopo".

**D: Che significano i placeholder come [First Name]?**  
A: Sono wildcards che si riempiono automaticamente con i dati del lead. [First Name] → nome del lead, [Company] → azienda, etc.

**D: Quali placeholder posso usare?**  
A: [First Name], [Last Name], [Company], [Email], [Role], [Settore]

**D: A che ora dovrei mandare le email?**  
A: Durante ore di lavoro: 9-11 AM oppure 14-16 (2-4 PM). Evita week-end. Test con piccoli gruppi prima di scalare.

**D: Posso mandare allegati?**  
A: Attualmente no, ma puoi inserire link a Google Drive, Dropbox, etc. nel corpo email.

**D: Come faccio A/B testing?**  
A: Crea 2 template diversi, mandi a 2 gruppi identici di lead, compara i risultati (open rate, reply rate).

**D: Se una email bounca, cosa succede?**  
A: Il lead passa a status "ERROR" e non riceve altri messaggi fino a fix manuale. Verifica che l'email sia valida.

**D: Posso tracciare i click nei link?**  
A: Sì! Tracciamo automaticamente i link cliccati dentro le email.

**D: Posso usare AI per generare email?**  
A: Sì, se il workspace ha Claude integrato. Clicca "Genera con AI", scrivi il prompt, e AI genera 3 versioni.

---

## 📊 Analytics

**D: Dopo quanto vedo i risultati?**  
A: **Open tracking** = istantaneo (quando la email viene aperta). **Reply** = quando il lead risponde. **Conversion** = quando concludi il deal.

**D: Qual è un buon Open Rate?**  
A: 5-10% = media, 15-25% = buono, 30%+ = eccellente.

**D: Qual è un buon Reply Rate?**  
A: 2-5% = media, 10-15% = buono, 20%+ = eccellente.

**D: Qual è un buon Conversion Rate?**  
A: 1-2% = media, 5-10% = buono, 15%+ = eccellente (dipende dal settore).

**D: Perché il mio Open Rate è 0%?**  
A: Probabilmente le email sono appena state mandate. Attendi 24 ore per i dati di tracking.

**D: Perché il mio Conversion Rate è sempre 0%?**  
A: Devi marcare manualmente i lead come "Converted" quando diventano clienti. Non è automatico.

**D: Come esporto i dati di analytics?**  
A: Clicca "Esporta CSV" nella sezione Analytics per salvare i dati.

**D: Quali segmenti posso analizzare?**  
A: Puoi segmentare per: Settore (industry), Ruolo (CTO, CEO, VP, etc.), Dimensione Azienda (Startup, SMB, Enterprise).

---

## ⚙️ Integrations & Settings

**D: Posso collegare il mio account Apollo?**  
A: Sì, se hai account Apollo puoi esportare lead come CSV e importarli in Outreach Machine.

**D: Come cambio il nome del workspace?**  
A: Vai in Settings → Workspace Settings → cambia nome e salva.

**D: Dove vedo i limiti del mio piano?**  
A: Vai in Settings per visualizzare i dettagli del tuo piano (email/giorno, lead massimi, etc.).

**D: Posso invitare altri utenti al workspace?**  
A: Attualmente Outreach Machine è single-user per workspace. Contatta il supporto per multi-user.

---

## 🎓 Strategy & Best Practices

**D: Come faccio a trovare i miei target ideal?**  
A: Filtra per settore, ruolo, dimensione azienda. Crea test campaign piccoli (10-20 lead) e misura quale segmento risponde meglio.

**D: Come faccio A/B testing efficace?**  
A: Test UNA SOLA variabile alla volta. Es: cambia soggetto, mantieni corpo uguale. Misura open rate. Poi test successivo.

**D: Quante email dovrei mandare al giorno?**  
A: Dipende dal tuo piano e dalla qualità della lista. Consiglio: inizia con 50/giorno e scala gradualmente.

**D: Qual è la strategia di follow-up migliore?**  
A: 1. First email (giorno 1) - Introduzione + valore. 2. Follow-up (giorno 3-5) - Ricorda gentilmente. 3. Ultimo tentativo (giorno 7-10). 4. Archive se non risponde.

**D: Come miglioro il mio Open Rate?**  
A: Cambia il **soggetto**. Usa A/B testing. Personalizza il soggetto con [First Name]. Manda a orari specifici (9 AM test vs 2 PM). Evita spam words ("FREE", "URGENT", "!!!").

**D: Come miglioro il mio Reply Rate?**  
A: Accorcia l'email (50-100 parole). Fai CTA più chiara ("Disponibile per una call?"). Aggiungi valore specifico ("Abbiamo aiutato [competitor] a...").

**D: Che cosa fare se il Reply Rate è alto ma Conversion è basso?**  
A: Gente risponde ma non converte. Problema nel follow-up o nella proposta di vendita. Migliora il pitch.

**D: Che cosa fare se l'Open Rate è alto ma Reply Rate è basso?**  
A: Gente apre ma non risponde. Corpo email non convincente o CTA poco chiara. Cambia il messaggio.

---

## 🆘 Troubleshooting Reference

**D: Che cosa fare se le email non vengono mandate?**  
A: Vedi [Troubleshooting →](troubleshooting)

**D: Che cosa fare se il bounce rate è alto?**  
A: Vedi [Troubleshooting →](troubleshooting)

**D: Che cosa fare se non vedo i dati analytics?**  
A: Vedi [Troubleshooting →](troubleshooting)

**D: Che cosa fare se un placeholder non si riempie?**  
A: Vedi [Troubleshooting →](troubleshooting)

---

## 📞 Support & Resources

**D: Non trovo la risposta qui. Come contatto il supporto?**  
A: Contatta il team tecnico con una descrizione dettagliata del problema.

**D: Voglio imparare le best practices. Dove comincio?**  
A: Leggi [Best Practices →](best-practices)

**D: Voglio completare il mio primo ciclo di outreach. Quali step?**  
A: Segui [Getting Started →](getting-started) → First Workflow (15 minuti)

---

[← Torna alla Home](home) | [Troubleshooting →](troubleshooting)
