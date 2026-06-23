# SMR

**Generated** : 2026-06-23T00:20:49.428211+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $11.24  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $11.24 (+11.5% vs entrée) · entrée $10.08 · stop $9.74 · T1 $10.47 · R/R 1.15  
> ↳ P(T1 av. stop) 43 % · EV/risk 0.009 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.080 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $10.01–$10.16 (mid $10.08)
- Spot actuel : $11.24 (+11.5% au-dessus de la zone — repli à attendre)
- Stop : $9.74 (stop atr-based (-15.45%))
- Targets : T1 $10.47 · R/R 1.15 | T2 $10.85 · R/R 2.26 | T3 $11.24 · R/R 3.41
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $9.74


## Edge, scénarios & sizing

- EV/risk : 0.009 | EV/share : $0.003 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 20 % | T3 8 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 30.2 | bear 15.2 | side 54.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 157.0 (= 14 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 160 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s ; entrée au DIP du plan + p_fill ; à comparer à l'EV GBM du bloc Edge — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −10.301% → cible +3.814% / stop −3.444%, p_fill 9%, 15 remplis) : P(cible|rempli) **33%** · **EV/risk +0.006** (×p_fill ; si rempli +0.21% du capital)
  - **swing** : indisponible (trop peu de remplissages (1))
  - **deep** : indisponible (trop peu de remplissages (0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→73% · +2.0%→62% · +3.0%→50% · +5.0%→29% · +8.0%→13%
- Range intraday médian 7.71% (p90 12.61%) · excursion haute méd. +2.99% / basse méd. −3.53%
- Profil de vol intra : ouverture 4.681% vs midi 1.576% vs clôture 1.788% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.43 · part idiosyncratique 2.52
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 42.3  _(momentum baissier)_
- **ADX** : 13.8  _(pas de tendance nette)_
- **MACD** : hist 0.044  _(bullish_recent)_
- **BB** : %B 0.49 · largeur 44.8%
- **ATR** : 1.16 (22.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.075  _(distribution)_
- **Vol ratio** : 0.74  _(volume normal)_
- **Choppiness** : 43.2  _(transition)_
- **MA** : MA20 11.28 · MA50 11.58 · MA200 20.58  _(prix < MA20)_
- **Dist MA** : MA20 -0.3% · MA50 -2.9% · MA200 -45.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (26465 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
