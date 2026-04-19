---
id: crisi-epilettica
titolo: Crisi epilettica e stato di male
categoria: emergenze
tag: [emergenza, epilessia, status, crisi, convulsioni]
termini_equivalenti: [convulsione, convulsioni, stato epilettico, status epilepticus, crisi tonico-clonica]

sintesi: "Crisi epilettica singola >5 min o crisi ripetute senza recupero di coscienza = **stato di male epilettico**. Tempo è outcome: ogni minuto di stato aumenta il danno neuronale. Chiamare subito aiuto se >5 min."

indicazioni:
  - Crisi tonico-clonica >5 minuti (stato convulsivo)
  - Crisi ripetute senza recupero di coscienza tra una e l'altra
  - Stato di male non convulsivo (alterazione coscienza, necessario EEG)
  - Crisi focale con consciousness impaired >10 minuti

prerequisiti:
  - Accesso venoso (2 vie se possibile)
  - Monitoraggio PV continuo (SpO2, FC, PA)
  - Ossigeno in maschera se SpO2 <94%
  - Glicemia subito (escludere ipoglicemia)
  - EGA (se disponibile rapidamente)

algoritmo_linee:
  linea_1:
    finestra_temporale: "0-5 minuti dall'inizio della crisi"
    farmaci:
      - nome: Diazepam
        dose: "0.15-0.2 mg/kg EV (max 10 mg) in 2-5 min"
        via: EV lenta
        alternative: "Rettale 0.2-0.5 mg/kg se no accesso venoso"
      - nome: Lorazepam
        dose: "0.1 mg/kg EV (max 4 mg) in 2 min"
        via: EV lenta
        note: "Preferito se disponibile — minor rischio di accumulo"
      - nome: Midazolam
        dose: "0.2 mg/kg IM (max 10 mg) / 0.1 mg/kg EV"
        via: IM o EV
        note: "IM utile se no accesso venoso, rapidamente efficace"
    ripetibile: "Una volta dopo 5 min se persiste"

  linea_2:
    finestra_temporale: "5-30 minuti (stato definito)"
    condizione: "Crisi non risolta dopo prima dose di BDZ"
    farmaci:
      - nome: Levetiracetam (Keppra)
        dose: "60 mg/kg EV (max 4.5 g) in 10-15 min"
        via: EV
        note: "Prima scelta — pochi effetti collaterali, no monitoraggio livelli"
      - nome: Valproato (Depakin)
        dose: "40 mg/kg EV (max 3 g) in 10 min"
        via: EV
        controindicazioni: "Epatopatia, gravidanza, sospetto mitocondriopatia"
      - nome: Fenitoina
        dose: "20 mg/kg EV in 20 min (max 50 mg/min)"
        via: EV con monitoraggio ECG
        note: "Monitoraggio cardiaco obbligatorio (aritmie, ipotensione). Via centrale preferita."

  linea_3:
    finestra_temporale: "oltre 30 minuti — stato refrattario"
    condizione: "Persistenza dopo BDZ + antiepilettico di linea 2"
    richiede: "Chiamare Rianimazione. Paziente verosimilmente da intubare e portare in NeuroTIPO."
    farmaci:
      - nome: Midazolam continuo
        dose: "0.2 mg/kg bolo, poi 0.05-2 mg/kg/h"
        via: EV continua, con intubazione
      - nome: Propofol
        dose: "2 mg/kg bolo, poi 2-10 mg/kg/h"
        via: EV continua, con intubazione
      - nome: Tiopentale
        dose: "2-7 mg/kg bolo, poi 0.5-5 mg/kg/h"
        via: EV continua, solo in rianimazione

target_clinici:
  - "Cessazione attività motoria entro 30 min"
  - "EEG: soppressione delle scariche (burst-suppression se in coma farmacologico)"
  - "PA sistolica >90 mmHg, PAM >65 mmHg"
  - "SpO2 >94%, glicemia 80-180 mg/dL"

numeri_chiave:
  - etichetta: MdG Anestesista / NeuroTIPO / Emergenze
    numeri: ["97012"]
    note: "Chiamare se stato >30 min o instabilità respiratoria"
  - etichetta: EEG urgente
    numeri: ["3605", "8565"]
    note: "Per stato non convulsivo o monitoraggio coma"
  - etichetta: Laboratorio urgenze
    numeri: ["3996"]
    note: "Per valproemia urgente, glicemia, emogas"

post_procedura:
  - Ricerca causa scatenante (imaging, EEG, ematochimici, tossicologici)
  - Impostare terapia di mantenimento antiepilettica
  - Ricerca infezioni (CSF se sospetta encefalite)
  - Monitoraggio funzionale post-ictale
  - Informare familiari, evitare scatenanti (privazione sonno, alcol, farmaci abbassanti soglia)

nota_diario_template: |
  Paziente con crisi tonico-clonica generalizzata insorta alle ore __, durata __ minuti con perdita di coscienza e automatismi. Accesso venoso posizionato. Glicemia __ mg/dL. Somministrato __ EV. Cessazione della crisi alle ore __. Al risveglio [descrivi stato di coscienza, deficit focali transitori di Todd, lingua morsicata, incontinenza]. Avviati accertamenti per ricerca eziologica: [TC/RM, EEG, screening ematochimico]. Impostata terapia di mantenimento con __.

note_libere: |
  ### Cose da non dimenticare nei primi 5 minuti
  - **Glicemia capillare**: l'ipoglicemia è una causa trattabile e sottostimata
  - **Posizione di sicurezza** laterale per ridurre aspirazione
  - **Cronometrare** l'inizio della crisi (chiedere a chi ha assistito)
  - **Non forzare** oggetti in bocca (rischio frattura denti, lesioni)
  - **Accesso venoso x2** appena possibile
  
  ### Cause più comuni da investigare
  1. Sospensione brusca di antiepilettici (paziente noto, livelli infraterapeutici)
  2. Infezioni SNC (meningite, encefalite — pensare a HSV!)
  3. Stroke (ischemico o emorragico)
  4. Disturbi metabolici (iponatriemia, ipoglicemia, uremia)
  5. Intossicazione / astinenza (alcol, benzodiazepine)
  6. Tumore SNC (primitivo o metastatico)
  7. Traumi cranici recenti
  
  ### Stato non convulsivo — sospettarlo quando
  - Alterazione dello stato di coscienza senza causa chiara
  - Confusione prolungata post-ictale >30 min
  - Automatismi, nistagmo, afasia "fluttuante"
  - EEG urgente è diagnostico

procedure_correlate: [eeg-urgente, edema-cerebrale]
tabelle_correlate: []
numeri_correlati: [mdg-anestesista-neurotipo, eeg, lab-urgenze-giustinianeo]

ultima_modifica: 2026-04-18T19:00:00Z
modificato_da: admin
cronologia_recente:
  - data: 2026-04-18T19:00:00Z
    utente: admin
    nota: prototipo emergenze con algoritmo linee
---
