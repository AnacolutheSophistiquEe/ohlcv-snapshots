# ENR

**Generated** : 2026-06-23T21:40:14.190681+00:00  
**Santé technique** : 6/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €162.50  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot €162.50 (+22.5% vs entrée) · entrée €132.69 · stop €129.87 · T1 €138.33 · R/R 2.0  
> ↳ P(T1 av. stop) 36 % · EV/risk 0.127 · ¼-Kelly 0.008 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.120 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €131.56–€133.82 (mid €132.69)
- Spot actuel : €162.50 (+22.5% au-dessus de la zone — repli à attendre)
- Stop : €129.87 (stop swing_plan-based (-20.08%))
- Targets : T1 €138.33 · R/R 2.0 | T2 €143.98 · R/R 4.0 | T3 €149.62 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €129.87


## Edge, scénarios & sizing

- EV/risk : 0.127 | EV/share : €0.358 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 20 % | T3 9 %
- Kelly (position) : f* 0.031 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, swing) : bull 46.9 | bear 27.4 | side 25.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 325.0 (= 2 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→68% · +2.0%→50% · +3.0%→29% · +5.0%→11% · +8.0%→1%
- Range intraday médian 4.6% (p90 7.11%) · excursion haute méd. +1.9% / basse méd. −1.81%
- Profil de vol intra : ouverture 2.213% vs midi 1.031% vs clôture 1.271% _(ouverture ~2.1× plus volatile → privilégier/éviter selon le setup)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; neutre — autocorr -0.025)_ ; drift intra méd. -0.214% ; recovery-V 12%
- **σ réalisé intraday** 2.655% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 68% / whipsaw 36%
- POC intraday (dernière séance, temps-au-prix) : 170.1021 (VA 169.7966–171.6296 ; dernier close 169.64)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.55 · part idiosyncratique 0.45
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 52.0  _(neutre)_
- **ADX** : 19.5  _(pas de tendance nette)_
- **MACD** : hist 1.821  _(pas de croisement recent)_
- **BB** : %B 0.59 · largeur 21.2%
- **ATR** : 7.38 (71.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.124  _(distribution)_
- **Vol ratio** : 0.73  _(volume normal)_
- **Choppiness** : 40.5  _(transition)_
- **MA** : MA20 159.48 · MA50 169.18 · MA200 136.77  _(prix > MA20)_
- **Dist MA** : MA20 +1.9% · MA50 -4.0% · MA200 +18.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (24491 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
