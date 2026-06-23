# RHM

**Generated** : 2026-06-23T21:35:52.429505+00:00  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · €1166.60  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot €1166.60 (+0.8% vs entrée) · entrée €1157.65 · stop €1142.31 · T1 €1173.10 · R/R 1.01  
> ↳ P(T1 av. stop) 48 % _(réel 5 s)_ · EV/risk 0.129 _(réel 5 s)_ (GBM -0.049) · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.070 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €1154.56–€1160.74 (mid €1157.65)
- Spot actuel : €1166.60 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : €1142.31 (stop swing_plan-based (-3.15%))
- Targets : T1 €1173.10 · R/R 1.01 | T2 €1188.55 · R/R 2.01 | T3 €1203.99 · R/R 3.02
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €1142.31


## Edge, scénarios & sizing

- EV/risk : -0.049 | EV/share : €-0.750 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 22 % | T3 8 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 51.7 | bear 10.2 | side 38.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.765% → cible +1.334% / stop −1.325%, p_fill 82%, n_eff≈34.3) : P(cible|rempli) **48%** · **EV/risk +0.129** (×p_fill ; si rempli +0.21% du capital)
  - **swing** (entrée dip −1.683% → cible +2.984% / stop −1.492%, p_fill 63%, n_eff≈25.1) : P(cible|rempli) **45%** · **EV/risk +0.154** (×p_fill ; si rempli +0.36% du capital)
  - **deep** (entrée dip −2.605% → cible +4.22% / stop −2.11%, p_fill 44%, n_eff≈23.2) : P(cible|rempli) **17%** · **EV/risk -0.234** (×p_fill ; si rempli -1.13% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→62% · +2.0%→49% · +3.0%→30% · +5.0%→2% · +8.0%→0%
- Range intraday médian 4.15% (p90 6.64%) · excursion haute méd. +1.85% / basse méd. −1.66%
- Profil de vol intra : ouverture 2.386% vs midi 0.898% vs clôture 1.012% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Régime intraday** : **chop** _(efficiency 0.097 ; neutre — autocorr 0.027)_ ; drift intra méd. -0.258% ; recovery-V 29%
- **σ réalisé intraday** 2.589% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 61% / bas 64% / whipsaw 25%
- POC intraday (dernière séance, temps-au-prix) : 1175.8325 (VA 1147.2975–1193.3925 ; dernier close 1181.4)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.33 · part idiosyncratique 0.67
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 43.2  _(momentum baissier)_
- **ADX** : 22.9  _(pas de tendance nette)_
- **MACD** : hist 3.641  _(pas de croisement recent)_
- **BB** : %B 0.26 · largeur 12.2%
- **ATR** : 51.14 (22.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.072  _(distribution)_
- **Vol ratio** : 0.84  _(volume normal)_
- **Choppiness** : 72.1  _(marche en range (choppy))_
- **MA** : MA20 1202.03 · MA50 1265.76 · MA200 1578.72  _(prix < MA20)_
- **Dist MA** : MA20 -2.9% · MA50 -7.8% · MA200 -26.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (26160 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
