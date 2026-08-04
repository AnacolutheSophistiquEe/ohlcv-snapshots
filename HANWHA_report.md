# 012450

**Generated** : 2026-08-04T21:54:29.268034+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1005500.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩1005500.00 (+0.9% vs entrée) · entrée ₩996903.91 · stop ₩917151.60 · T1 ₩1069530.88 · R/R 0.91  
> ↳ P(T1 av. stop) 6 % _(réel 5 s)_ · EV/risk -0.127 _(réel 5 s)_ (GBM -0.156) · ¼-Kelly 0.019 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.160 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩990445.65–₩1003362.17 (mid ₩996903.91)
- Spot actuel : ₩1005500.00 (+0.9% au-dessus de la zone — repli à attendre)
- Stop : ₩917151.60 (stop swing_plan-based (-9.44%))
- Targets : T1 ₩1069530.88 · R/R 0.91 | T2 ₩1081507.58 · R/R 1.06 | T3 ₩1093484.27 · R/R 1.21
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩917151.60


## Edge, scénarios & sizing

- EV/risk : -0.156 | EV/share : ₩-12441.361 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 14 % | T2 14 % | T3 14 %
- Kelly (position) : f* 0.075 | ¼-Kelly 0.019 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 27.6 | bear 56.4 | side 15.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.859% → cible +7.285% / stop −8.0%, p_fill 88%, n_eff≈36.9) : P(cible|rempli) **6%** · **EV/risk -0.127** (×p_fill ; si rempli -1.16% du capital)
  - **swing** (entrée dip −1.882% → cible +7.221% / stop −7.703%, p_fill 88%, n_eff≈36.4) : P(cible|rempli) **33%** · **EV/risk -0.206** (×p_fill ; si rempli -1.80% du capital)
  - **deep** (entrée dip −2.902% → cible +10.212% / stop −11.677%, p_fill 87%, n_eff≈35.2) : P(cible|rempli) **48%** · **EV/risk -0.026** (×p_fill ; si rempli -0.35% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→60% · +2.0%→40% · +3.0%→24% · +5.0%→14% · +8.0%→2%
- Range intraday médian 5.96% (p90 9.06%) · excursion haute méd. +1.78% / basse méd. −2.99%
- Profil de vol intra : ouverture 4.265% vs midi 1.188% vs clôture 1.188% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (150 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 87% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; mean-reverting — autocorr -0.06)_ ; drift intra méd. -1.167% ; recovery-V 36%
- **σ réalisé intraday** 4.753% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 55% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 915375.0 (VA 912375.0–922875.0 ; dernier close 915000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 35% · rebond 82% · **stop −5.22%** sous le fill (sous le bruit) · cible +2.07% · R/R 0.4 (high win-rate)
- Gaps overnight (n=149) : méd. 0.63% · baisse 32% (gap-down >1% 19% · >2% 10%)
- Excursion ouverture 5min (n=150) : bas méd −1.76% (p90 −4.05%) · haut méd +0.85% · range méd 2.9%
- Excursion ouverture 15min (n=150) : bas méd −2.12% (p90 −4.64%) · haut méd +1.08% · range méd 3.44%
- Excursion ouverture 30min (n=150) : bas méd −2.16% (p90 −5.06%) · haut méd +1.16% · range méd 4.04%
- Excursion ouverture 60min (n=150) : bas méd −2.37% (p90 −5.52%) · haut méd +1.39% · range méd 4.53%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 915000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 72% (107/149) · gap 22% · délai 0.1min · rebond 50% (54/107) (MFE +0.88%)
   - −1.0% : fill 30min 56% · séance 69% (103/149) · gap 19% · délai 0.9min · rebond 53% (60/103) (MFE +1.01%)
   - −1.5% : fill 30min 54% · séance 65% (96/149) · gap 12% · délai 1.3min · rebond 62% (56/96) (MFE +1.36%)
   - −2.0% : fill 30min 45% · séance 57% (79/149) · gap 10% · délai 3.1min · rebond 65% (49/79) (MFE +1.6%)
   - −3.0% : fill 30min 31% · séance 46% (58/149) · gap 2% · délai 3.4min · rebond 71% (40/58) (MFE +1.58%)
   - −4.0% : fill 30min 22% · séance 35% (44/149) · gap 2% · délai 9.6min · rebond 82% (36/44) (MFE +2.07%)
   - −5.0% : fill 30min 14% · séance 25% (32/149) · gap 1% · délai 8.7min · rebond 79% (26/32) (MFE +2.47%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.67% (p90 −2.23%) → stop au-delà de −2.08% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.79% (p90 −2.69%) → stop au-delà de −2.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.44% (p90 −2.69%) → stop au-delà de −2.64% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=727 jambes) : jambe baissière méd −1.24% (p90 −3.27%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (33 séances) :
      · −1.0% : fill 100% (33/33) · rebond 40% (14/33)
      · −2.0% : fill 94% (30/33) · rebond 67% (18/30)
      · −3.0% : fill 90% (27/33) · rebond 75% (19/27)
      · −4.0% : fill 77% (24/33) · rebond 89% (20/24)
      · −5.0% : fill 50% (16/33) · rebond 88% (14/16)
   - **flat** (20 séances) :
      · −1.0% : fill 90% (19/20) · rebond 49% (10/19)
      · −2.0% : fill 69% (15/20) · rebond 48% (7/15)
      · −3.0% : fill 53% (9/20) · rebond 37% (3/9)
      · −4.0% : fill 53% (9/20) · rebond 48% (5/9)
      · −5.0% : fill 51% (8/20) · rebond 52% (4/8)
   - **gap-up** (96 séances) :
      · −1.0% : fill 52% (51/96) · rebond 66% (36/51)
      · −2.0% : fill 39% (34/96) · rebond 72% (24/34)
      · −3.0% : fill 26% (22/96) · rebond 86% (18/22)
      · −4.0% : fill 13% (11/96) · rebond 100% (11/11)
      · −5.0% : fill 9% (8/96) · rebond 100% (8/8)
- **P(clôture VERTE) selon le drive 15min** (n=150) : 37% en base · 67% si les 15 1res min sont vertes (50 cas) · 19% si rouges (100 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=150) : COUDE à **49min** → P(séance verte=clôture>ouverture) 86% si début vert vs 9% si rouge (base 37% · écart 77 pts) ; prédictivité sature ensuite (plafond brut 49min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=50) : tient le vert **86%** · continue >prix actuel 55% ; creux résiduel méd -1.6% (q20 -3.63%) → **SL/trailing à −3.63%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.52% / q75 +3.75% → **scale +2.52% / runner +3.75%**, sortie à la clôture
  - **si ROUGE au coude** (n=100) : edge inversé — récupère vert seulement **9%** (continue à baisser 60%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.35%** (au-delà de la MAE q10 -6.35%), cible rebond +1.43% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=150) : retour [-5.35% .. +4.64%] · haut q95 +5.79% · bas q05 -6.3%
   - 60min (n=150) : retour [-5.29% .. +5.29%] · haut q95 +7.09% · bas q05 -6.86%
   - 2h (n=150) : retour [-7.49% .. +5.47%] · haut q95 +7.09% · bas q05 -8.29%
   - 4h (n=150) : retour [-7.16% .. +5.8%] · haut q95 +7.85% · bas q05 -9.05%
   - 6h (n=150) : retour [-6.91% .. +5.97%] · haut q95 +8.28% · bas q05 -10.1%
   - session (n=150) : retour [-7.34% .. +5.9%] · haut q95 +8.28% · bas q05 -10.1%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 012450 = **volatil sans tendance propre (choppy)** (vol intra méd 3.54%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 60.7  _(momentum haussier)_
- **ADX** : 15.9  _(pas de tendance nette)_
- **MACD** : hist 12787.802  _(bullish_recent)_
- **BB** : %B 0.76 · largeur 29.8%
- **ATR** : 76000.0 (67.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.156  _(distribution)_
- **Vol ratio** : 0.89  _(volume normal)_
- **Choppiness** : 52.4  _(transition)_
- **MA** : MA20 932775.0 · MA50 1039690.0 · MA200 1138029.81  _(prix > MA20)_
- **Dist MA** : MA20 +7.8% · MA50 -3.3% · MA200 -11.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83997 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
