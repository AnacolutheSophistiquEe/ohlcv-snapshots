# 012450

**Generated** : 2026-08-01T20:11:07.940194+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩917000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩917000.00 (+2.0% vs entrée) · entrée ₩898827.20 · stop ₩826921.03 · T1 ₩971115.65 · R/R 1.01  
> ↳ P(T1 av. stop) 0 % _(réel 5 s)_ · EV/risk -0.125 _(réel 5 s)_ (GBM -0.17) · ¼-Kelly 0.013 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.160 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩893283.78–₩904370.63 (mid ₩898827.20)
- Spot actuel : ₩917000.00 (+2.0% au-dessus de la zone — repli à attendre)
- Stop : ₩826921.03 (stop swing_plan-based (-12.83%))
- Targets : T1 ₩971115.65 · R/R 1.01 | T2 ₩976421.15 · R/R 1.08 | T3 ₩981726.65 · R/R 1.15
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩826921.03


## Edge, scénarios & sizing

- EV/risk : -0.17 | EV/share : ₩-12224.050 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 11 % | T2 11 % | T3 11 %
- Kelly (position) : f* 0.053 | ¼-Kelly 0.013 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.4 | bear 8.5 | side 78.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.978% → cible +8.043% / stop −8.0%, p_fill 79%, n_eff≈32.5) : P(cible|rempli) **0%** · **EV/risk -0.125** (×p_fill ; si rempli -1.26% du capital)
  - **swing** (entrée dip −4.355% → cible +6.874% / stop −8.861%, p_fill 58%, n_eff≈26.1) : P(cible|rempli) **44%** · **EV/risk -0.096** (×p_fill ; si rempli -1.47% du capital)
  - **deep** (entrée dip −6.738% → cible +9.722% / stop −13.631%, p_fill 68%, n_eff≈25.3) : P(cible|rempli) **45%** · **EV/risk -0.026** (×p_fill ; si rempli -0.51% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→59% · +2.0%→40% · +3.0%→22% · +5.0%→11% · +8.0%→1%
- Range intraday médian 5.9% (p90 8.74%) · excursion haute méd. +1.78% / basse méd. −3.17%
- Profil de vol intra : ouverture 4.132% vs midi 1.143% vs clôture 1.166% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (147 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 88% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.133 ; mean-reverting — autocorr -0.064)_ ; drift intra méd. -1.759% ; recovery-V 34%
- **σ réalisé intraday** 4.689% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 43% / bas 63% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 807412.5 (VA 786487.5–842287.5 ; dernier close 803000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 37% · rebond 82% · **stop −5.22%** sous le fill (sous le bruit) · cible +2.07% · R/R 0.4 (high win-rate)
- Gaps overnight (n=146) : méd. 0.6% · baisse 34% (gap-down >1% 20% · >2% 10%)
- Excursion ouverture 5min (n=147) : bas méd −1.78% (p90 −4.05%) · haut méd +0.79% · range méd 2.83%
- Excursion ouverture 15min (n=147) : bas méd −2.13% (p90 −4.8%) · haut méd +1.08% · range méd 3.43%
- Excursion ouverture 30min (n=147) : bas méd −2.2% (p90 −5.24%) · haut méd +1.1% · range méd 3.99%
- Excursion ouverture 60min (n=147) : bas méd −2.44% (p90 −5.68%) · haut méd +1.29% · range méd 4.51%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 803000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 75% (106/146) · gap 23% · délai 0.1min · rebond 48% (53/106) (MFE +0.73%)
   - −1.0% : fill 30min 58% · séance 72% (102/146) · gap 20% · délai 0.9min · rebond 52% (59/102) (MFE +1.01%)
   - −1.5% : fill 30min 55% · séance 67% (95/146) · gap 13% · délai 1.3min · rebond 61% (55/95) (MFE +1.26%)
   - −2.0% : fill 30min 47% · séance 60% (79/146) · gap 10% · délai 3.1min · rebond 65% (49/79) (MFE +1.6%)
   - −3.0% : fill 30min 33% · séance 48% (58/146) · gap 2% · délai 3.4min · rebond 71% (40/58) (MFE +1.58%)
   - −4.0% : fill 30min 23% · séance 37% (44/146) · gap 2% · délai 9.6min · rebond 82% (36/44) (MFE +2.07%)
   - −5.0% : fill 30min 14% · séance 27% (32/146) · gap 1% · délai 8.7min · rebond 79% (26/32) (MFE +2.47%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.7% (p90 −2.54%) → stop au-delà de −2.12% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.19% (p90 −2.76%) → stop au-delà de −2.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.56% (p90 −2.77%) → stop au-delà de −2.67% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=702 jambes) : jambe baissière méd −1.26% (p90 −3.4%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (33 séances) :
      · −1.0% : fill 100% (33/33) · rebond 40% (14/33)
      · −2.0% : fill 94% (30/33) · rebond 67% (18/30)
      · −3.0% : fill 90% (27/33) · rebond 75% (19/27)
      · −4.0% : fill 77% (24/33) · rebond 89% (20/24)
      · −5.0% : fill 50% (16/33) · rebond 88% (14/16)
   - **flat** (19 séances) :
      · −1.0% : fill 88% (18/19) · rebond 41% (9/18)
      · −2.0% : fill 78% (15/19) · rebond 48% (7/15)
      · −3.0% : fill 60% (9/19) · rebond 37% (3/9)
      · −4.0% : fill 60% (9/19) · rebond 48% (5/9)
      · −5.0% : fill 58% (8/19) · rebond 52% (4/8)
   - **gap-up** (94 séances) :
      · −1.0% : fill 55% (51/94) · rebond 66% (36/51)
      · −2.0% : fill 41% (34/94) · rebond 72% (24/34)
      · −3.0% : fill 27% (22/94) · rebond 86% (18/22)
      · −4.0% : fill 14% (11/94) · rebond 100% (11/11)
      · −5.0% : fill 9% (8/94) · rebond 100% (8/8)
- **P(clôture VERTE) selon le drive 15min** (n=147) : 35% en base · 63% si les 15 1res min sont vertes (48 cas) · 20% si rouges (99 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=147) : COUDE à **49min** → P(séance verte=clôture>ouverture) 85% si début vert vs 9% si rouge (base 35% · écart 75 pts) ; prédictivité sature ensuite (plafond brut 49min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=48) : tient le vert **85%** · continue >prix actuel 55% ; creux résiduel méd -1.6% (q20 -3.31%) → **SL/trailing à −3.31%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.34% / q75 +3.56% → **scale +2.34% / runner +3.56%**, sortie à la clôture
  - **si ROUGE au coude** (n=99) : edge inversé — récupère vert seulement **9%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.48%** (au-delà de la MAE q10 -6.48%), cible rebond +1.45% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=147) : retour [-5.44% .. +3.78%] · haut q95 +5.4% · bas q05 -6.31%
   - 60min (n=147) : retour [-5.29% .. +4.67%] · haut q95 +6.69% · bas q05 -7.01%
   - 2h (n=147) : retour [-7.7% .. +4.45%] · haut q95 +6.92% · bas q05 -8.36%
   - 4h (n=147) : retour [-7.25% .. +5.58%] · haut q95 +7.16% · bas q05 -9.43%
   - 6h (n=147) : retour [-7.11% .. +4.72%] · haut q95 +7.5% · bas q05 -10.26%
   - session (n=147) : retour [-7.53% .. +4.84%] · haut q95 +7.5% · bas q05 -10.26%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 012450 = **volatil sans tendance propre (choppy)** (vol intra méd 3.51%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 46.0  _(neutre)_
- **ADX** : 17.3  _(pas de tendance nette)_
- **MACD** : hist 1040.201  _(pas de croisement recent)_
- **BB** : %B 0.41 · largeur 41.7%
- **ATR** : 77714.29 (72.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.165  _(distribution)_
- **Vol ratio** : 1.14  _(volume normal)_
- **Choppiness** : 53.2  _(transition)_
- **MA** : MA20 953250.0 · MA50 1051140.0 · MA200 1139016.26  _(prix < MA20)_
- **Dist MA** : MA20 -3.8% · MA50 -12.8% · MA200 -19.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83637 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
