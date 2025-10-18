---
title: "Indicatori / Indicators  Trentino - Commuter Analysis"
author: "napo"
date: "2021"
license: "CC BY 4.0"
description: "Factsheet of all indicators computed available in Italian and English versions."
tags: ["mobility", "Trentino", "commuting", "data analysis", "accessibility"]
---

# Indicatori  - *Trentino Commuter Analysis*

**Anno di riferimento :** 2021  
**Unità di analisi:** Comune (Provincia di Trento, Italia / Municipality – Trentino, Italy)

## Scopo degl indicatori
- Misurare l’**integrazione funzionale** tra i comuni.  
- Evidenziare **disuguaglianze territoriali** in accessibilità e lavoro.  
- Supportare la **pianificazione basata sui dati** e le politiche di mobilità.  
- Consentire analisi **replicabili nel tempo** e **basate su dati aperti**.

<summary><b>Italiano</b></summary>

## Indicatori dei flussi di pendolarismo
Derivati dai microdati dei movimenti *in entrata* e *in uscita* per motivi di lavoro.

| **Indicatore** | **Formula / Fonte** | **Significato e utilizzo** |
|----------------|----------------------|-----------------------------|
| **in_Totale** | Totale degli ingressi (lavoratori che entrano nel comune) | Misura **quante persone lavorano nel comune**, indipendentemente da dove risiedono: rappresenta l’**offerta di lavoro** locale. |
| **out_Totale** | Totale delle uscite (residenti che lavorano altrove) | Misura **quante persone residenti escono dal comune per lavorare**: rappresenta la **dipendenza residenziale** dal resto del territorio. |
| **saldo_netto** | `in_Totale – out_Totale` | Se positivo<br/>- il comune **attrae lavoratori** (polo occupazionale)<br/> Se negativo<br/>- **esporta lavoratori** (area prevalentemente residenziale). |

## Intensità di pendolarismo e ruoli funzionali
Normalizzano i flussi rispetto alla popolazione per descrivere l’intensità e l’autonomia funzionale.

| **Indicatore** | **Formula / Definizione** | **Significato e utilizzo** |
|----------------|----------------------------|-----------------------------|
| **intensità_pendolarismo** | `(in_Totale + out_Totale) / popolazione` | Misura **quanto il comune è coinvolto nei flussi di mobilità quotidiana**.<br/>Valori alti<br/>- comune fortemente connesso alla rete provinciale. |
| **autocontenimento_pc** | `Stesso / popolazione` | Quota di residenti che **vivono e lavorano nello stesso comune**<br/>- indica l’**autonomia funzionale** locale. |
| **attrattività_pc** | `in_Totale / popolazione` | Numero di lavoratori entranti per abitante<br/>- misura **l’attrattività occupazionale** del comune. |

## Equilibrio territoriale
Descrive il bilanciamento tra funzioni residenziali e occupazionali.

| **Indicatore** | **Formula** | **Significato e utilizzo** |
|----------------|-------------|-----------------------------|
| **indice_bilancio** | `in_Totale / out_Totale` | Rapporto tra posti di lavoro e lavoratori residenti.<br/> >1 = polo occupazionale<br/> <1 = comune residenziale |
| **quota_stesso / quota_intra / quota_extra** | Percentuali interne ai flussi | Distinguono se i flussi provengono dallo stesso comune, da altri comuni trentini o da fuori provincia. |


## Accessibilità territoriale
Calcolata da matrici di **distanza (km)** e **tempo (minuti)** tra i comuni tramite modello gravitazionale.

| **Indicatore** | **Formula** | **Significato e utilizzo** |
|----------------|-------------|-----------------------------|
| **A_km_beta1_5** | &Sigma;(pop_j / d_ij^1.5) | **Potenziale di accessibilità gravitazionale.**<br/>Valori alti => grandi popolazioni raggiungibili a breve distanza => aree centrali. |
| **A_time** | &Sigma;(pop_j / (1 + t_ij)) | Variante in funzione del **tempo di percorrenza** invece che della distanza. |
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
| **inv_R50_km** | `1 / R50_km` | Inverso della distanza necessaria per raggiungere metà della popolazione provinciale<br/> più alto = **migliore accessibilità**. |

## Confronto statistico (medie e quartili)
Indicatori di confronto calcolati su tutti i comuni.

| **Indicatore** | **Definizione** | **Utilità** |
|----------------|------------------|-------------|
| **media, quartili (Q1, Q2, Q3)** | Statistiche provinciali per ogni indicatore | Permettono di capire se un comune è **sopra o sotto la media**. |
| **quartile_category** | Posizione del comune (Q1–Q4) | Semplifica la lettura: Q4 = migliori 25%, Q1 = peggiori 25%. |


</details>

