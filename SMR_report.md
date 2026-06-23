# SMR

**Generated** : 2026-06-23T21:56:33.359065+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $10.86  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $10.86 (+11.4% vs entrée) · entrée $9.75 · stop $9.41 · T1 $10.12 · R/R 1.09  
> ↳ P(T1 av. stop) 36 % · EV/risk -0.004 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.090 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $9.67–$9.82 (mid $9.75)
- Spot actuel : $10.86 (+11.4% au-dessus de la zone — repli à attendre)
- Stop : $9.41 (stop swing_plan-based (-23.93%))
- Targets : T1 $10.12 · R/R 1.09 | T2 $10.49 · R/R 2.18 | T3 $10.87 · R/R 3.29
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $9.41


## Edge, scénarios & sizing

- EV/risk : -0.004 | EV/share : $-0.001 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 12 % | T3 3 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 15.2 | bear 40.4 | side 44.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=7, n_eff=5))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→81% · +2.0%→69% · +3.0%→55% · +5.0%→34% · +8.0%→18%
- Range intraday médian 7.23% (p90 12.61%) · excursion haute méd. +3.23% / basse méd. −2.99%
- Profil de vol intra : ouverture 4.728% vs midi 1.552% vs clôture 1.825% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_
- **Régime intraday** : **chop** _(efficiency 0.14 ; neutre — autocorr 0.007)_ ; drift intra méd. 0.764% ; recovery-V 29%
- **σ réalisé intraday** 5.361% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 43% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 11.5377 (VA 11.4013–11.6743 ; dernier close 11.22)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.43 · part idiosyncratique 0.57
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 34.6  _(momentum baissier)_
- **ADX** : 13.0  _(pas de tendance nette)_
- **MACD** : hist 0.055  _(bullish_recent)_
- **BB** : %B 0.42 · largeur 45.0%
- **ATR** : 1.11 (19.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.091  _(distribution)_
- **Vol ratio** : 0.72  _(volume normal)_
- **Choppiness** : 48.0  _(transition)_
- **MA** : MA20 11.25 · MA50 11.61 · MA200 20.45  _(prix < MA20)_
- **Dist MA** : MA20 -3.5% · MA50 -6.5% · MA200 -46.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (25105 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
