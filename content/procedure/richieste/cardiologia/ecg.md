---
id: ecg
titolo: Richiesta ECG
categoria: richieste
sottocategoria: cardiologia
tag: [cardiologia, routine, ingressi]
termini_equivalenti: [elettrocardiogramma, tracciato, EKG]

sintesi: "ECG a 12 derivazioni per tutti i nuovi ingressi e per i pazienti senza ECG refertato recente su Galileo. Richiesta da coordinare con l'infermiere per evitare errori informatici."

indicazioni:
  - Nuovo ingresso (sempre)
  - Sospetta patologia cardiaca o aritmia
  - Dolore toracico
  - Sincope / pre-sincope
  - Monitoraggio post-terapia cardiotossica
  - Controllo post-inserimento CVC o midline

richiesta_galileo:
  percorso: "Strumenti paziente → Richiedi accertamenti → CARDIOLOGIA → ELETTROCARDIOGRAMMA"
  urgenza: "Selezionare 'Urgente' solo se clinica in atto (dolore, dispnea, instabilità)"
  note_quesito: "Specificare patologie cardiologiche note e motivo della richiesta"
  allegati: "Nessuno"

numeri_chiave:
  - etichetta: Ambulatorio refertazione ECG
    numeri: ["2393"]
    orari: "fino alle 14"
    note: "Per sollecitare refertazione"
  - etichetta: Cardiologo di guardia
    numeri: ["97503"]
    orari: "dopo le 14 / urgenze"
  - etichetta: MdG Cardiologia (urgenze notturne)
    numeri: ["97953"]

tempistica: "Eseguire entro 2 ore dalla richiesta informatica. Se supera, bisogna reinviare la richiesta. Se ECG parte da sistema prima della richiesta, re-inviarlo."

note_libere: |
  **Trucco operativo**: coordinarsi SEMPRE con l'infermiere prima di inviare la richiesta. L'ordine sbagliato (ECG prima della richiesta) causa errore informatico e va rifatto.
  
  **Lettura in autonomia**: controllare sempre l'ECG prima della refertazione per verificare qualità (artefatti) ed eventuali anomalie evidenti. Se artefatti, chiedere di rifarlo.
  
  **Quando sollecitare la refertazione**: sospetta patologia cardiaca in atto (FA di nuovo riscontro, dolore toracico, paziente instabile). Chiamare Amb. ECG (2393) prima delle 14, Cardiologo di guardia (97953) dopo.

numeri_correlati: [amb-refertazione-ecg, mdg-cardiologia]
procedure_correlate: [ecocardio, holter-ecg]

ultima_modifica: 2026-04-18T19:00:00Z
modificato_da: admin
cronologia_recente:
  - data: 2026-04-18T19:00:00Z
    utente: admin
    nota: prototipo prima scheda richieste
---
