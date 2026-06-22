# SMR

**Generated** : 2026-06-22T00:19:05.611989+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $11.74  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.020 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $10.38–$10.70 (mid $10.54)
- Spot actuel : $11.74 (+11.4% au-dessus de la zone — repli à attendre)
- Stop : $9.70 (stop atr-based (-15.34%))
- Targets : T1 $10.95 · R/R 0.49 | T2 $11.36 · R/R 0.98 | T3 $11.78 · R/R 1.48
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $9.70


## Edge, scénarios & sizing

- EV/risk : -0.072 | EV/share : $-0.060 | p_fill : —
- Régime probabiliste (posterior HMM, intraday) : bull 29.3 | bear 11.1 | side 59.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 153.0 (= 13 part(s) × prix) · cible 160.0


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.43 · part idiosyncratique 2.31
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Indicateurs (résumé)

- **RSI** : 45.5  _(neutre)_
- **ADX** : 14.2  _(pas de tendance nette)_
- **MACD** : hist -0.011  _(pas de croisement recent)_
- **BB** : %B 0.59 · largeur 44.8%
- **ATR** : 1.2 (25.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.021  _(neutre)_
- **Vol ratio** : 1.75  _(volume au-dessus de la moyenne)_
- **Choppiness** : 44.6  _(transition)_
- **MA** : MA20 11.28 · MA50 11.54 · MA200 20.72  _(prix > MA20)_
- **Dist MA** : MA20 +4.1% · MA50 +1.7% · MA200 -43.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (18626 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
