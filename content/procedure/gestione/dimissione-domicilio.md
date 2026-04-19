---
id: dimissione-domicilio
titolo: Dimissione a domicilio
categoria: gestione
sottocategoria: dimissione
tag: [dimissione, lettera, domicilio, follow-up]
termini_equivalenti: [dimissione, dimissioni a casa, ritorno a casa]

sintesi: "Workflow di dimissione del paziente clinicamente stabile verso il domicilio. Coordinamento con paziente, familiari, MMG e follow-up ambulatoriale."

prerequisiti:
  - Stabilità clinica confermata dallo strutturato
  - Rimozione CV/CVC eseguita il giorno prima (se non più necessari)
  - Ripresa diuresi spontanea documentata (se aveva CV)
  - Terapia domiciliare definita
  - Accertamenti programmati per follow-up
  - Lettera di dimissione pronta in cartella

richiesta_galileo:
  percorso: "Strumenti di fine ricovero → Dimissione → compilare lettera → Stampa"
  allegati: "Lettera dimissione firmata, impegnative per farmaci/esami, certificato ricovero"

numeri_chiave:
  - etichetta: Segreteria ambulatori
    numeri: ["3623"]
    note: "Prenotazione post-degenza"
  - etichetta: CUP
    numeri: ["2102"]
    note: "Prenotazione esami ambulatoriali"
  - etichetta: Servizio Sociale
    numeri: ["8805", "8983"]
    note: "Se necessita assistenza domiciliare"
  - etichetta: SeCC (Continuità delle Cure)
    numeri: ["8460", "8461"]
    note: "Per passaggio ai servizi territoriali"

post_procedura:
  - Consegnare lettera di dimissione al paziente (2 copie)
  - Spiegare terapia domiciliare al paziente/familiari
  - Programmare visita neurologica di controllo
  - Prescrivere esami di follow-up necessari
  - Informare MMG (telefono o via lettera)
  - Se paziente fragile: attivare assistenza domiciliare

nota_diario_template: |
  Paziente dimesso in data odierna in condizioni cliniche stabili. All'esame obiettivo neurologico: [descrivere]. Terapia domiciliare: [elencare]. Consegnata lettera di dimissione con indicazioni. Programmato controllo neurologico tra __ settimane/mesi. Esami di follow-up: __. Consigliato in caso di [sintomi] di rivolgersi al MMG o al PS.

note_libere: |
  ### Checklist dimissione (da spuntare prima di firmare)
  - [ ] Lettera di dimissione completa e firmata
  - [ ] Terapia domiciliare prescritta (impegnative farmaci)
  - [ ] Esami di controllo prescritti
  - [ ] Visite ambulatoriali prenotate
  - [ ] Certificato di ricovero stampato
  - [ ] Eventuale certificato INPS per lavoratori
  - [ ] Informazioni per MMG (lettera o telefonata)
  - [ ] CV rimosso e diuresi ripresa (se applicabile)
  - [ ] CVC/midline rimosso se non serve più
  
  ### Casi particolari
  - **Paziente che rifiuta terapia**: modulo dimissione volontaria (su Galileo → Stampa Modulistica)
  - **Paziente non autosufficiente**: attivare servizi territoriali tramite SeCC (8460), considerare SVAMA
  - **Paziente straniero non italofono**: lettera tradotta se disponibile, o affiancare servizio interprete (0294758819, cod. Padova23)
  - **Paziente con terapia complessa**: rivedere con paziente/caregiver la gestione farmaci, soprattutto antiepilettici/anticoagulanti
  
  ### Cosa NON dimenticare
  - Verificare allergie in lettera
  - Se paziente ha fatto trombolisi: impegnative per RM controllo, visita cardiologica se FA
  - Se paziente epilettico: ribadire divieto guida per 6 mesi dalla crisi (D.M. specifico)
  - Se paziente anticoagulato: schema chiaro con dosaggio, timing e target INR se VKA

procedure_correlate: [trasferimento-riabilitazione, svama]
moduli_correlati: []

ultima_modifica: 2026-04-18T19:00:00Z
modificato_da: admin
cronologia_recente:
  - data: 2026-04-18T19:00:00Z
    utente: admin
    nota: prototipo gestione
---
