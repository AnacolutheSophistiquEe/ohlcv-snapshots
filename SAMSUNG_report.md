# 005930

**Generated** : 2026-07-29T00:13:53.494131+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩220000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)  
> ↳ spot ₩220000.00 (+2.9% vs entrée) · entrée ₩213712.56 · stop ₩200568.84 · T1 ₩240000.00 · R/R 2.0  
> ↳ P(T1 av. stop) 19 % _(réel 5 s)_ · EV/risk -0.272 _(réel 5 s)_ (GBM 0.384) · ¼-Kelly 0.007 · _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -56 % hors [0,100] (R² max 0.97). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.250 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩210231.50–₩217193.62 (mid ₩213712.56)
- Spot actuel : ₩220000.00 (+2.9% au-dessus de la zone — repli à attendre)
- Stop : ₩200568.84 (stop swing_plan-based (-8.83%))
- Targets : T1 ₩240000.00 · R/R 2.0 | T2 ₩262000.00 · R/R 3.67 | T3 ₩265770.23 · R/R 3.96
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩200568.84


## Edge, scénarios & sizing

- EV/risk : 0.384 | EV/share : ₩5046.581 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 21 % | T2 3 % | T3 2 %
- Kelly (position) : f* 0.027 | ¼-Kelly 0.007 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 10.7 | bear 53.9 | side 35.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.303% → cible +2.486% / stop −3.158%, p_fill 81%, n_eff≈30.6) : P(cible|rempli) **24%** · **EV/risk -0.233** (×p_fill ; si rempli -0.91% du capital)
  - **swing** (entrée dip −2.855% → cible +12.3% / stop −6.15%, p_fill 70%, n_eff≈27.3) : P(cible|rempli) **19%** · **EV/risk -0.272** (×p_fill ; si rempli -2.40% du capital)
  - **deep** (entrée dip −4.416% → cible +24.594% / stop −12.297%, p_fill 64%, n_eff≈22.5) : P(cible|rempli) **8%** · **EV/risk -0.355** (×p_fill ; si rempli -6.79% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→65% · +2.0%→45% · +3.0%→30% · +5.0%→20% · +8.0%→5%
- Range intraday médian 5.45% (p90 9.05%) · excursion haute méd. +1.83% / basse méd. −2.61%
- Profil de vol intra : ouverture 2.796% vs midi 1.188% vs clôture 1.405% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (141 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 12% · trend ↑1%/↓1% ; spike-down 66% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; mean-reverting — autocorr -0.085)_ ; drift intra méd. -0.842% ; recovery-V 21%
- **σ réalisé intraday** 4.258% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 43% / bas 75% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 252450.0 (VA 248550.0–253950.0 ; dernier close 254500.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 30% · rebond 67% · **stop −6.06%** sous le fill (sous le bruit) · cible +1.51% · R/R 0.25 (high win-rate)
- Gaps overnight (n=140) : méd. 0.17% · baisse 45% (gap-down >1% 35% · >2% 24%)
- Excursion ouverture 5min (n=141) : bas méd −0.59% (p90 −1.46%) · haut méd +0.65% · range méd 1.44%
- Excursion ouverture 15min (n=141) : bas méd −0.89% (p90 −2.34%) · haut méd +1.04% · range méd 2.07%
- Excursion ouverture 30min (n=141) : bas méd −1.2% (p90 −2.78%) · haut méd +1.13% · range méd 2.47%
- Excursion ouverture 60min (n=141) : bas méd −1.54% (p90 −3.4%) · haut méd +1.36% · range méd 3.05%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 254500.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 53% · séance 66% (87/140) · gap 38% · délai 0.0min · rebond 55% (48/87) (MFE +1.51%)
   - −1.0% : fill 30min 48% · séance 64% (81/140) · gap 35% · délai 0.0min · rebond 62% (47/81) (MFE +1.48%)
   - −1.5% : fill 30min 44% · séance 57% (71/140) · gap 26% · délai 0.3min · rebond 60% (43/71) (MFE +1.69%)
   - −2.0% : fill 30min 41% · séance 49% (62/140) · gap 24% · délai 0.2min · rebond 57% (36/62) (MFE +1.77%)
   - −3.0% : fill 30min 31% · séance 44% (53/140) · gap 19% · délai 1.7min · rebond 61% (35/53) (MFE +2.05%)
   - −4.0% : fill 30min 23% · séance 37% (42/140) · gap 14% · délai 23.1min · rebond 63% (29/42) (MFE +2.09%)
   - −5.0% : fill 30min 13% · séance 30% (32/140) · gap 8% · délai 79.2min · rebond 67% (22/32) (MFE +1.51%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.34% (p90 −1.75%) → stop au-delà de −1.14% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.38% (p90 −2.56%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.31% (p90 −2.14%) → stop au-delà de −1.12% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=620 jambes) : jambe baissière méd −1.29% (p90 −3.07%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (60 séances) :
      · −1.0% : fill 97% (57/60) · rebond 50% (30/57)
      · −2.0% : fill 88% (49/60) · rebond 46% (25/49)
      · −3.0% : fill 86% (44/60) · rebond 55% (28/44)
      · −4.0% : fill 75% (36/60) · rebond 58% (24/36)
      · −5.0% : fill 64% (28/60) · rebond 63% (18/28)
   - **flat** (13 séances) :
      · −1.0% : fill 58% (7/13) · rebond 70% (4/7)
      · −2.0% : fill 40% (4/13) · rebond 85% (3/4)
      · −3.0% : fill 40% (4/13) · rebond 85% (3/4)
      · −4.0% : fill 18% (2/13) · rebond 100% (2/2)
      · −5.0% : fill 18% (2/13) · rebond 100% (2/2)
   - **gap-up** (67 séances) :
      · −1.0% : fill 36% (17/67) · rebond 86% (13/17)
      · −2.0% : fill 17% (9/67) · rebond 94% (8/9)
      · −3.0% : fill 9% (5/67) · rebond 89% (4/5)
      · −4.0% : fill 8% (4/67) · rebond 88% (3/4)
      · −5.0% : fill 2% (2/67) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=141) : 42% en base · 67% si les 15 1res min sont vertes (70 cas) · 18% si rouges (71 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=141) : COUDE à **1:14** → P(séance verte=clôture>ouverture) 82% si début vert vs 8% si rouge (base 42% · écart 74 pts) ; prédictivité sature ensuite (plafond brut 129min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **82%** · continue >prix actuel 52% ; creux résiduel méd -1.59% (q20 -4.19%) → **SL/trailing à −4.19%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.54% / q75 +3.38% → **scale +1.54% / runner +3.38%**, sortie à la clôture
  - **si ROUGE au coude** (n=65) : edge inversé — récupère vert seulement **8%** (continue à baisser 55%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.22%** (au-delà de la MAE q10 -7.22%), cible rebond +0.98% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=141) : retour [-2.64% .. +3.14%] · haut q95 +4.15% · bas q05 -3.08%
   - 60min (n=141) : retour [-3.02% .. +4.88%] · haut q95 +6.03% · bas q05 -3.62%
   - 2h (n=141) : retour [-4.23% .. +4.78%] · haut q95 +6.34% · bas q05 -5.12%
   - 4h (n=141) : retour [-6.03% .. +5.88%] · haut q95 +6.84% · bas q05 -7.27%
   - 6h (n=141) : retour [-6.44% .. +5.68%] · haut q95 +7.61% · bas q05 -7.85%
   - session (n=141) : retour [-6.09% .. +5.86%] · haut q95 +7.61% · bas q05 -8.58%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 4.3% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.77%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 31.2  _(momentum baissier)_
- **ADX** : 24.9  _(pas de tendance nette)_
- **MACD** : hist -4043.674  _(pas de croisement recent)_
- **BB** : %B 0.01 · largeur 41.2%
- **ATR** : 22857.14 (86.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.254  _(distribution)_
- **Vol ratio** : 1.47  _(volume normal)_
- **Choppiness** : 51.8  _(transition)_
- **MA** : MA20 275375.0 · MA50 302490.0 · MA200 190734.52  _(prix < MA20)_
- **Dist MA** : MA20 -20.1% · MA50 -27.3% · MA200 +15.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (84170 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
