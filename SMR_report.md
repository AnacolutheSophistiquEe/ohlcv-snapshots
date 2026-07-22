# SMR

**Generated** : 2026-07-22T00:29:22.598070+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $8.71  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot $8.71 (+8.6% vs entrée) · entrée $8.02 · stop $7.82 · T1 $8.22 · R/R 1.0  
> ↳ P(T1 av. stop) 52 % · EV/risk 0.028 · ¼-Kelly 0.011 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.57% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.090 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $7.98–$8.06 (mid $8.02)
- Spot actuel : $8.71 (+8.6% au-dessus de la zone — repli à attendre)
- Stop : $7.82 (stop swing_plan-based (-18.14%))
- Targets : T1 $8.22 · R/R 1.0 | T2 $8.41 · R/R 1.95 | T3 $8.60 · R/R 2.9
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $7.82


## Edge, scénarios & sizing

- EV/risk : 0.028 | EV/share : $0.006 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 34 % | T3 34 %
- Kelly (position) : f* 0.046 | ¼-Kelly 0.011 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 48.4 | bear 38.9 | side 12.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=12, n_eff=6))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→78% · +2.0%→65% · +3.0%→57% · +5.0%→39% · +8.0%→18%
- Range intraday médian 7.73% (p90 12.61%) · excursion haute méd. +3.65% / basse méd. −3.09%
- Profil de vol intra : ouverture 4.993% vs midi 1.573% vs clôture 1.726% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.118 ; neutre — autocorr -0.011)_ ; drift intra méd. -0.46% ; recovery-V 24%
- **σ réalisé intraday** 4.82% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 64% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 7.9348 (VA 7.7707–8.0737 ; dernier close 7.96)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 55% · rebond 78% · **stop −6.09%** sous le fill (sous le bruit) · cible +2.53% · R/R 0.42 (high win-rate)
- Gaps overnight (n=159) : méd. -0.63% · baisse 58% (gap-down >1% 42% · >2% 29%)
- Excursion ouverture 5min (n=160) : bas méd −1.18% (p90 −3.37%) · haut méd +0.99% · range méd 2.68%
- Excursion ouverture 15min (n=160) : bas méd −1.67% (p90 −3.82%) · haut méd +1.31% · range méd 3.51%
- Excursion ouverture 30min (n=160) : bas méd −1.91% (p90 −4.79%) · haut méd +1.75% · range méd 4.42%
- Excursion ouverture 60min (n=160) : bas méd −2.19% (p90 −6.04%) · haut méd +2.45% · range méd 5.43%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 7.96 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 76% · séance 84% (132/159) · gap 51% · délai 0.0min · rebond 68% (82/132) (MFE +1.73%)
   - −1.0% : fill 30min 70% · séance 79% (126/159) · gap 42% · délai 0.0min · rebond 67% (83/126) (MFE +2.02%)
   - −1.5% : fill 30min 65% · séance 76% (120/159) · gap 39% · délai 0.0min · rebond 74% (87/120) (MFE +2.3%)
   - −2.0% : fill 30min 59% · séance 70% (113/159) · gap 29% · délai 0.1min · rebond 68% (81/113) (MFE +2.49%)
   - −3.0% : fill 30min 48% · séance 62% (102/159) · gap 11% · délai 2.1min · rebond 75% (83/102) (MFE +2.57%)
   - −4.0% : fill 30min 37% · séance 55% (87/159) · gap 5% · délai 9.4min · rebond 78% (68/87) (MFE +2.53%)
   - −5.0% : fill 30min 25% · séance 43% (65/159) · gap 3% · délai 19.5min · rebond 67% (47/65) (MFE +1.87%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.93% (p90 −2.71%) → stop au-delà de −2.05% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.03% (p90 −2.8%) → stop au-delà de −2.16% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.18% (p90 −2.97%) → stop au-delà de −2.5% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1179 jambes) : jambe baissière méd −1.39% (p90 −3.19%) · ~14.4 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (84 séances) :
      · −1.0% : fill 100% (84/84) · rebond 68% (55/84)
      · −2.0% : fill 94% (80/84) · rebond 74% (60/80)
      · −3.0% : fill 86% (76/84) · rebond 78% (63/76)
      · −4.0% : fill 78% (67/84) · rebond 84% (56/67)
      · −5.0% : fill 60% (48/84) · rebond 69% (37/48)
   - **flat** (14 séances) :
      · −1.0% : fill 80% (11/14) · rebond 54% (7/11)
      · −2.0% : fill 69% (9/14) · rebond 22% (4/9)
      · −3.0% : fill 66% (7/14) · rebond 47% (4/7)
      · −4.0% : fill 66% (7/14) · rebond 55% (3/7)
      · −5.0% : fill 56% (6/14) · rebond 80% (5/6)
   - **gap-up** (61 séances) :
      · −1.0% : fill 50% (31/61) · rebond 70% (21/31)
      · −2.0% : fill 36% (24/61) · rebond 67% (17/24)
      · −3.0% : fill 27% (19/61) · rebond 80% (16/19)
      · −4.0% : fill 20% (13/61) · rebond 67% (9/13)
      · −5.0% : fill 15% (11/61) · rebond 41% (5/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 55% si les 15 1res min sont vertes (69 cas) · 32% si rouges (91 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:25** → P(séance verte=clôture>ouverture) 77% si début vert vs 14% si rouge (base 42% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 233min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **77%** · continue >prix actuel 49% ; creux résiduel méd -2.31% (q20 -3.72%) → **SL/trailing à −3.72%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.25% / q75 +4.33% → **scale +2.25% / runner +4.33%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **14%** (continue à baisser 55%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.68%** (au-delà de la MAE q10 -5.68%), cible rebond +1.57% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.52% .. +4.91%] · haut q95 +6.59% · bas q05 -6.03%
   - 60min (n=160) : retour [-6.64% .. +5.59%] · haut q95 +7.88% · bas q05 -7.9%
   - 2h (n=160) : retour [-7.82% .. +7.82%] · haut q95 +11.23% · bas q05 -8.88%
   - 4h (n=160) : retour [-8.61% .. +7.91%] · haut q95 +11.22% · bas q05 -10.71%
   - 6h (n=160) : retour [-8.1% .. +8.59%] · haut q95 +11.41% · bas q05 -10.72%
   - session (n=160) : retour [-8.13% .. +10.49%] · haut q95 +11.62% · bas q05 -10.73%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 4.92%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 36.1  _(momentum baissier)_
- **ADX** : 23.0  _(pas de tendance nette)_
- **MACD** : hist -0.043  _(pas de croisement recent)_
- **BB** : %B 0.37 · largeur 41.1%
- **ATR** : 0.69 (3.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.092  _(distribution)_
- **Vol ratio** : 1.16  _(volume normal)_
- **Choppiness** : 36.6  _(marche directionnel)_
- **MA** : MA20 9.21 · MA50 10.5 · MA200 17.72  _(prix < MA20)_
- **Dist MA** : MA20 -5.4% · MA50 -17.1% · MA200 -50.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83199 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
