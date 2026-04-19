---
id: nihss
titolo: NIHSS — National Institutes of Health Stroke Scale
categoria: clinica
sottocategoria: scale-cliniche
tag: [stroke, score, valutazione, nihss, trombolisi, trombectomia]
termini_equivalenti: [stroke scale, scala ictus, NIH]

sintesi: "Scala standardizzata per quantificare la severità di uno stroke ischemico. 15 item, punteggio 0-42. Usata per decisione trombolisi/trombectomia e follow-up temporale."

indicazioni:
  - Ogni paziente con sospetto stroke (baseline e follow-up)
  - Prima e dopo trombolisi EV
  - Prima e dopo trombectomia
  - Rivalutazione quotidiana nei pazienti in Stroke Unit

criteri_valutazione:
  - "1a. Livello di coscienza (0-3)"
  - "1b. Domande orientamento: mese, età (0-2)"
  - "1c. Esecuzione comandi: chiudere occhi, stringere pugno (0-2)"
  - "2. Sguardo coniugato (0-2)"
  - "3. Campo visivo (0-3)"
  - "4. Paralisi facciale (0-3)"
  - "5a. Motilità arto superiore sx (0-4)"
  - "5b. Motilità arto superiore dx (0-4)"
  - "6a. Motilità arto inferiore sx (0-4)"
  - "6b. Motilità arto inferiore dx (0-4)"
  - "7. Atassia degli arti (0-2)"
  - "8. Sensibilità (0-2)"
  - "9. Linguaggio (0-3)"
  - "10. Disartria (0-2)"
  - "11. Estinzione / negligenza (0-2)"

punteggio:
  range: "0-42"
  interpretazione:
    - "0 = nessun deficit"
    - "1-4 = stroke minore"
    - "5-15 = stroke moderato"
    - "16-20 = stroke moderato-severo"
    - "21-42 = stroke severo"

interpretazione: |
  **Soglie operative**:
  - NIHSS ≥6 nel territorio carotideo con occlusione grande vaso → candidato a trombectomia
  - NIHSS <4 → valutare beneficio/rischio trombolisi individualmente
  - NIHSS ≥25 + tempo dalla finestra terapeutica → rischio emorragico aumentato
  
  **Variazioni nel tempo**:
  - Miglioramento di ≥4 punti = risposta significativa a terapia
  - Peggioramento di ≥4 punti = stroke in progression, valutare imaging urgente

note_libere: |
  ### Come valutarla al letto
  - **Ordine fisso dei punti**: non saltare o riordinare (altrimenti score non comparabile)
  - **Non aiutare il paziente**: se non capisce, punteggio penalizzante
  - **Non ripetere** item a distanza di tempo nello stesso esame
  - Usare il **modulo cartaceo** o app MDCalc per calcolare
  
  ### Item più tricky
  - **1a LOC**: se paziente intubato, considerare la reattività allo stimolo
  - **2 Sguardo**: testare solo movimenti orizzontali volontari/reflex
  - **5-6 Motilità**: arto pretest a 90° (AS) o 30° (AI), cronometrare 10s (AS) o 5s (AI)
  - **9 Linguaggio**: usare il set di immagini/frasi standardizzate per riproducibilità
  
  ### Quando ricalcolarla
  - All'arrivo in PS (baseline)
  - Prima della trombolisi
  - A 2h, 24h post-trombolisi
  - Prima e dopo trombectomia
  - Ogni peggioramento clinico
  - Ogni turno in Stroke Unit

riferimenti_bibliografici: |
  - Brott T, et al. Measurements of acute cerebral infarction: a clinical examination scale. Stroke. 1989;20(7):864-70.
  - Lyden P. Using the National Institutes of Health Stroke Scale. Stroke. 2017;48(2):513-9.

procedure_correlate: [stroke-ischemico, trombolisi-alteplase]
tabelle_correlate: []
numeri_correlati: [cicalino-stroke-team]

ultima_modifica: 2026-04-18T19:00:00Z
modificato_da: admin
cronologia_recente:
  - data: 2026-04-18T19:00:00Z
    utente: admin
    nota: prototipo score-scale
---
