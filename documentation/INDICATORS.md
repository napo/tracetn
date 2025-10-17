---
title: "Indicatori / Indicators – Trentino Commuter Analysis (tracetn)"
author: "Digital Commons Lab – FBK"
date: "2021"
license: "CC BY 4.0"
description: "Factsheet of all indicators computed in the tracetn project, available in Italian and English versions."
tags: ["mobility", "Trentino", "commuting", "data analysis", "accessibility"]
---

# 📊 Indicatori / Indicators - *Trentino Commuter Analysis (tracetn)*

**Anno di riferimento / Reference year:** 2021  
**Unità di analisi / Unit of analysis:** Comune (Provincia di Trento, Italia / Municipality – Trentino, Italy)

---

<details open>
<summary><b>Italiano</b></summary>

## Indicatori dei flussi di pendolarismo
Derivati dai microdati dei movimenti *in entrata* e *in uscita* per motivi di lavoro.

| **Indicatore** | **Formula / Fonte** | **Significato e utilizzo** |
|----------------|----------------------|-----------------------------|
| **in_Totale** | Totale degli ingressi (lavoratori che entrano nel comune) | Misura **quante persone lavorano nel comune**, indipendentemente da dove risiedono: rappresenta l’**offerta di lavoro** locale. |
| **out_Totale** | Totale delle uscite (residenti che lavorano altrove) | Misura **quante persone residenti escono dal comune per lavorare**: rappresenta la **dipendenza residenziale** dal resto del territorio. |
| **saldo_netto** | `in_Totale – out_Totale` | Se positivo => il comune **attrae lavoratori** (polo occupazionale). Se negativo => **esporta lavoratori** (area prevalentemente residenziale). |

## Intensità di pendolarismo e ruoli funzionali
Normalizzano i flussi rispetto alla popolazione per descrivere l’intensità e l’autonomia funzionale.

| **Indicatore** | **Formula / Definizione** | **Significato e utilizzo** |
|----------------|----------------------------|-----------------------------|
| **intensità_pendolarismo** | `(in_Totale + out_Totale) / popolazione` | Misura **quanto il comune è coinvolto nei flussi di mobilità quotidiana**. Valori alti => comune fortemente connesso alla rete provinciale. |
| **autocontenimento_pc** | `Stesso / popolazione` | Quota di residenti che **vivono e lavorano nello stesso comune** => indica l’**autonomia funzionale** locale. |
| **attrattività_pc** | `in_Totale / popolazione` | Numero di lavoratori entranti per abitante => misura **l’attrattività occupazionale** del comune. |

## Equilibrio territoriale
Descrive il bilanciamento tra funzioni residenziali e occupazionali.

| **Indicatore** | **Formula** | **Significato e utilizzo** |
|----------------|-------------|-----------------------------|
| **indice_bilancio** | `in_Totale / out_Totale` | Rapporto tra posti di lavoro e lavoratori residenti. >1 = polo occupazionale, <1 = comune residenziale. |
| **quota_stesso / quota_intra / quota_extra** | Percentuali interne ai flussi | Distinguono se i flussi provengono dallo stesso comune, da altri comuni trentini o da fuori provincia. |


## Accessibilità territoriale
Calcolata da matrici di **distanza (km)** e **tempo (minuti)** tra i comuni tramite modello gravitazionale.

| **Indicatore** | **Formula** | **Significato e utilizzo** |
|----------------|-------------|-----------------------------|
| **A_km_beta1_5** | Σ(pop_j / d_ij^1.5) | **Potenziale di accessibilità gravitazionale.** Valori alti => grandi popolazioni raggiungibili a breve distanza => aree centrali. |
| **A_time** | Σ(pop_j / (1 + t_ij)) | Variante in funzione del **tempo di percorrenza** invece che della distanza. |
| **R25_km / R50_km** | km necessari per raggiungere il 25% / 50% della popolazione provinciale | Misura la **densità demografica e centralità** del comune. |
| **T25_min / T50_min** | minuti necessari per raggiungere il 25% / 50% della popolazione | Variante temporale: evidenzia i **tempi di accesso ai poli principali**. |


## Connettività locale
Basata sul numero di comuni raggiungibili entro soglie di distanza o tempo.

| **Indicatore** | **Definizione** | **Significato e utilizzo** |
|----------------|------------------|-----------------------------|
| **neighbors_km_le_10 / 20 / 30** | Numero di comuni entro 10, 20, 30 km | Misura la **densità territoriale** e la vicinanza fisica dei comuni. |
| **neighbors_min_le_15 / 30 / 45** | Numero di comuni entro 15, 30, 45 minuti | Misura l’**accessibilità effettiva** tramite rete stradale. |


## Indicatori sintetici
Utilizzati per le classifiche e la visualizzazione.

| **Indicatore** | **Formula / Metodo** | **Significato e utilizzo** |
|----------------|----------------------|-----------------------------|
| **composite_score** | Media normalizzata (z-score) di 4 indicatori (`saldo_netto`, `intensità_pendolarismo`, `autocontenimento_pc`, `attrattività_pc`) | Indice sintetico di **performance complessiva** del comune. |
| **inv_R50_km** | `1 / R50_km` | Inverso della distanza necessaria per raggiungere metà della popolazione provinciale => più alto = **migliore accessibilità**. |

## Confronto statistico (medie e quartili)
Indicatori di confronto calcolati su tutti i comuni.

| **Indicatore** | **Definizione** | **Utilità** |
|----------------|------------------|-------------|
| **media, quartili (Q1, Q2, Q3)** | Statistiche provinciali per ogni indicatore | Permettono di capire se un comune è **sopra o sotto la media**. |
| **quartile_category** | Posizione del comune (Q1–Q4) | Semplifica la lettura: Q4 = migliori 25%, Q1 = peggiori 25%. |



## A cosa servono
- Misurano l’**integrazione funzionale** tra i comuni.  
- Evidenziano **disuguaglianze territoriali** in accessibilità e lavoro.  
- Supportano la **pianificazione basata sui dati** e le politiche di mobilità.  
- Consentono analisi **replicabili nel tempo** e **basate su dati aperti**.

</details>

---

<details>
<summary><b> English</b></summary>

## Commuting Flow Indicators
Derived from microdata of *incoming* and *outgoing* work movements.

| **Indicator** | **Formula / Source** | **Purpose & Interpretation** |
|----------------|----------------------|------------------------------|
| **in_Totale** | Total inbound commuters | Measures **how many people work in the municipality**, regardless of residence - proxy for *job supply*. |
| **out_Totale** | Total outbound commuters | Measures **how many residents work elsewhere**: proxy for *residential dependency*. |
| **saldo_netto (net balance)** | `in_Totale – out_Totale` | Positive => **attracts workers**. Negative => **exports workers**. |


## Commuting Intensity and Functional Roles

| **Indicator** | **Formula / Definition** | **Purpose & Interpretation** |
|----------------|--------------------------|------------------------------|
| **commuting_intensity** | `(in_Totale + out_Totale) / population` | **Overall level of commuting activity** relative to population. |
| **self_containment_pc** | `Stesso / population` | Residents who both live and work in the municipality - **local functional autonomy**. |
| **attractiveness_pc** | `in_Totale / population` | **Workplace attractiveness** relative to population. |


## Territorial Balance Indicators

| **Indicator** | **Formula** | **Purpose & Interpretation** |
|----------------|-------------|------------------------------|
| **balance_index** | `in_Totale / out_Totale` | Ratio of job inflows to outflows. >1 = employment hub; <1 = residential area. |
| **quota_stesso / quota_intra / quota_extra** | Flow composition | Identify whether movements are **local**, **intra-provincial**, or **external**. |

---

## Accessibility Potential Indicators

| **Indicator** | **Formula** | **Purpose & Interpretation** |
|----------------|-------------|------------------------------|
| **A_km_beta1_5** | Σ(pop_j / distance_ij^1.5) | **Gravity-based potential accessibility.** High values = many people reachable at short distance. |
| **A_time** | Σ(pop_j / (1 + time_ij)) | Accessibility based on **travel time**. |
| **R25_km / R50_km** | Distance to reach 25% / 50% of total population | **Spatial centrality and density.** |
| **T25_min / T50_min** | Time to reach 25% / 50% of population | **Temporal accessibility advantage** of central areas. |

---

## Local Connectivity Indicators

| **Indicator** | **Definition** | **Purpose & Interpretation** |
|----------------|----------------|------------------------------|
| **neighbors_km_le_10 / 20 / 30** | Number of municipalities within ≤10/20/30 km | **Spatial proximity and local density**. |
| **neighbors_min_le_15 / 30 / 45** | Number of municipalities within ≤15/30/45 minutes | **Effective road accessibility**. |

---

## Synthetic Indicators

| **Indicator** | **Formula / Method** | **Purpose & Interpretation** |
|----------------|----------------------|------------------------------|
| **composite_score** | Mean of z-scores of 4 indicators (`saldo_netto`, `commuting_intensity`, `self_containment_pc`, `attractiveness_pc`) | **Overall performance index** summarizing mobility and employment structure. |
| **inv_R50_km** | `1 / R50_km` | Inverse of the distance to half the provincial population - higher = **better accessibility**. |


## Statistical Comparison Metrics

| **Indicator** | **Definition** | **Purpose** |
|----------------|----------------|--------------|
| **mean, quartiles (Q1, Q2, Q3)** | Provincial descriptive stats | Benchmark municipalities (above/below average). |
| **quartile_category** | Position (Q1–Q4) | "Q4" = top 25% performers; "Q1" = bottom 25%. |

## Why these indicators matter
- Quantify **functional integration** among municipalities.  
- Reveal **urban–rural disparities** in accessibility and employment.  
- Support **evidence-based planning** and mobility policy.  
- Enable **replicable, open-data analysis** over time.

</details>

---

_This factsheet is part of the **tracetn** project - *Trentino Commuter Analysis*, mapping the invisible daily mobility patterns across the province._

