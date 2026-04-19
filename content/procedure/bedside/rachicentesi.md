---
id: rachicentesi
titolo: Rachicentesi
categoria: bedside
sottocategoria: liquorali
tag: [procedura, liquor, diagnostica, puntura-lombare]
termini_equivalenti: [puntura lombare, LP, PL, LCR, liquor]
urgenza_tipica: programmata

sintesi: "Prelievo di liquor cefalorachidiano per diagnosi di patologie infiammatorie, infettive, neoplastiche, neurodegenerative. Mattina dopo giro visite, strutturato presente."

indicazioni:
  - Sospetta meningite/encefalite
  - Sospetta SM o malattia demielinizzante (bande oligoclonali)
  - Sospetta malattia prionica (RT-QuIC)
  - Sospetta encefalite autoimmune (autoanticorpi)
  - Sospetta carcinomatosi meningea (citologia)
  - Sospetta Alzheimer (pannello neurodegenerazione)

controindicazioni:
  - Coagulopatia non corretta (INR >1.4, PLT <50.000)
  - Ipertensione endocranica con effetto massa
  - Infezione cutanea al sito
  - Paziente non collaborante senza sedazione

prerequisiti:
  - Paziente a digiuno
  - Sospensione antiaggreganti/anticoagulanti secondo tabella correlata
  - Consenso informato firmato in cartella
  - TC encefalo se dubbio di effetto massa
  - Coagulazione e piastrine disponibili

richiesta_galileo:
  percorso: "Modulo verde cartaceo (Lab Neurologia) OPPURE SR MEDICINA DI LABORATORIO → ESAME DEL LIQUOR [LIQUO] + CELLULARITA [LCEL]"
  urgenza: "Feriali entro 14 per Lab Neurologia; post-14 e festivi al Lab Urgenze Giustinianeo"
  allegati: "Modulo dedicato per ogni analisi (bande, micro, citologia, paraneoplastici)"

numeri_chiave:
  - etichetta: Lab Neurologia (chimico-fisico)
    numeri: ["3608"]
    orari: "feriali 8-14"
  - etichetta: Lab Urgenze Giustinianeo
    numeri: ["3996"]
    orari: "post 14 e festivi"
    note: Avvertire prima di pungere
  - etichetta: Microbiologia
    numeri: ["3046", "3047"]
    note: Avvertire prima di pungere
  - etichetta: Citodiagnostica
    numeri: ["3784", "3781"]
    note: NON dopo le 14 (cellule lisano)
  - etichetta: Lab Immunoematologia
    numeri: ["2481", "2299"]
    note: Portare personalmente al Monoblocco

preparazione:
  materiale: "Kit rachicentesi, provette etichettate, sacchetti biohazard, modulo verde"
  note: Etichettare SUBITO ogni provetta. Prelevare 2-3 cc extra da stoccare.

post_procedura:
  - Posizione supina 1-2 ore
  - Abbondante idratazione (per os o fisiologica EV)
  - Antiemetico e paracetamolo al bisogno
  - Monitoraggio cefalea post-puntura

nota_diario_template: |
  Previa raccolta del consenso informato (firmato e in cartella), eseguita rachicentesi in posizione seduta. Procedura eseguita senza complicanze peri e post-procedurali, ben tollerata, in assenza di traumatismo significativo. Si prelevano circa 10 cc di liquor limpido come acqua di rocca, a goccia rapida, in N aliquote. Si dispone per riposo a letto ed abbondante idratazione.

note_libere: |
  ### Richieste di analisi specifiche
  
  | Analisi | Volume | Codice Galileo | Dove va |
  | --- | --- | --- | --- |
  | Chimico-fisico feriale | 1 cc | LIQUO + LCEL | Lab Neurologia |
  | Chimico-fisico urgenze | 1 cc | MED.LAB URGENZE | Lab Urgenze Giustinianeo |
  | Bande oligoclonali | 1 cc + 2x sangue beige | OLIG | Lab Neurologia |
  | Film-array virale | ≥2 cc | LVIRUS | Lab Centrale |
  | Citologia | 2 cc | LIQUOR (Anat Pat) | Citodiagnostica |
  | Paraneoplastici | 2 cc | LCERV + CERV | Lab Centrale |
  | Pannello neurodegen. | 1-2 cc tappo azzurro | ALZH | Lab Centrale |
  
  ### Spedizione esterna
  1. Ordinare ghiaccio secco al Magazzino (3876/3877), 5 kg
  2. Pacco polistirolo da Lab Neurologia o DH
  3. Modulo giallo richiesta ghiaccio dalla Coordinatrice
  4. Relazione clinica + consenso raccolta dati
  5. Consegna Magazzino ore 7.45-8.00

invii_campioni_correlati: [rt-quic-verona, autoanticorpi-pavia]
tabelle_correlate: [anticoagulanti-rachicentesi]
moduli_correlati: [consenso-rachicentesi]
numeri_correlati: [lab-neurologia, lab-urgenze-giustinianeo, microbiologia-accettazione, citodiagnostica]

ultima_modifica: 2026-04-18T19:00:00Z
modificato_da: admin
cronologia_recente:
  - data: 2026-04-18T19:00:00Z
    utente: admin
    nota: migrazione al nuovo schema scheda flessibile
---
