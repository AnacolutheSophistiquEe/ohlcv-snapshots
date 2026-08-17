# AL2SI

**Generated** : 2026-08-17T00:10:35.682023+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €27.86  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €27.86 (+4.6% vs entrée) · entrée €26.64 · stop €26.07 · T1 €27.42 · R/R 1.37  
> ↳ P(T1 av. stop) 28 % _(réel 5 s)_ · EV/risk -0.041 _(réel 5 s)_ (GBM 0.085) · ¼-Kelly 0.019 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.15% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.120 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €26.49–€26.80 (mid €26.64)
- Spot actuel : €27.86 (+4.6% au-dessus de la zone — repli à attendre)
- Stop : €26.07 (stop swing_plan-based (-16.46%))
- Targets : T1 €27.42 · R/R 1.37 | T2 €28.19 · R/R 2.72 | T3 €28.96 · R/R 4.07
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €26.07


## Edge, scénarios & sizing

- EV/risk : 0.085 | EV/share : €0.049 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 32 % | T3 32 %
- Kelly (position) : f* 0.074 | ¼-Kelly 0.019 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.7 | bear 8.8 | side 5.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 390.0 (= 14 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.365% → cible +2.901% / stop −2.148%, p_fill 46%, n_eff≈24.2) : P(cible|rempli) **28%** · **EV/risk -0.041** (×p_fill ; si rempli -0.19% du capital)
  - **swing** (entrée dip −9.612% → cible +6.487% / stop −7.577%, p_fill 34%, n_eff≈17.5) : P(cible|rempli) **54%** · **EV/risk -0.048** (×p_fill ; si rempli -1.07% du capital)
  - **deep** (entrée dip −14.858% → cible +9.173% / stop −12.065%, p_fill 33%, n_eff≈16.7) : P(cible|rempli) **59%** · **EV/risk -0.021** (×p_fill ; si rempli -0.76% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→76% · +2.0%→70% · +3.0%→57% · +5.0%→42% · +8.0%→20%
- Range intraday médian 8.23% (p90 22.19%) · excursion haute méd. +4.23% / basse méd. −4.2%
- Profil de vol intra : ouverture 5.625% vs midi 1.776% vs clôture 1.92% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 10% · trend ↑0%/↓1% ; spike-down 74% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; mean-reverting — autocorr -0.057)_ ; drift intra méd. -0.159% ; recovery-V 30%
- **σ réalisé intraday** 6.47% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 51% / bas 69% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 27.5925 (VA 27.3765–27.7545 ; dernier close 27.88)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 40% · rebond 86% · **stop −5.28%** sous le fill (sous le bruit) · cible +2.4% · R/R 0.45 (high win-rate)
- Gaps overnight (n=159) : méd. 0.13% · baisse 43% (gap-down >1% 20% · >2% 9%)
- Excursion ouverture 5min (n=160) : bas méd −1.23% (p90 −4.73%) · haut méd +1.01% · range méd 3.0%
- Excursion ouverture 15min (n=160) : bas méd −1.61% (p90 −5.6%) · haut méd +1.54% · range méd 3.99%
- Excursion ouverture 30min (n=160) : bas méd −1.74% (p90 −5.84%) · haut méd +2.11% · range méd 4.77%
- Excursion ouverture 60min (n=160) : bas méd −2.26% (p90 −6.69%) · haut méd +2.54% · range méd 5.76%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 27.88 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 82% (125/159) · gap 30% · délai 0.3min · rebond 69% (85/125) (MFE +2.74%)
   - −1.0% : fill 30min 62% · séance 81% (121/159) · gap 20% · délai 0.6min · rebond 69% (83/121) (MFE +2.75%)
   - −1.5% : fill 30min 51% · séance 78% (112/159) · gap 14% · délai 1.2min · rebond 69% (74/112) (MFE +2.15%)
   - −2.0% : fill 30min 43% · séance 66% (96/159) · gap 9% · délai 4.7min · rebond 62% (61/96) (MFE +1.69%)
   - −3.0% : fill 30min 32% · séance 55% (80/159) · gap 5% · délai 10.8min · rebond 78% (65/80) (MFE +2.05%)
   - −4.0% : fill 30min 24% · séance 48% (69/159) · gap 3% · délai 27.7min · rebond 77% (54/69) (MFE +2.49%)
   - −5.0% : fill 30min 16% · séance 40% (60/159) · gap 3% · délai 42.3min · rebond 86% (55/60) (MFE +2.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −1.01% (p90 −4.99%) → stop au-delà de −2.35% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.26% (p90 −5.1%) → stop au-delà de −3.37% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.27% (p90 −5.37%) → stop au-delà de −3.63% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1569 jambes) : jambe baissière méd −1.28% (p90 −3.33%) · ~20.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 99% (53/56) · rebond 69% (35/53)
      · −2.0% : fill 82% (45/56) · rebond 58% (27/45)
      · −3.0% : fill 72% (41/56) · rebond 77% (33/41)
      · −4.0% : fill 64% (36/56) · rebond 82% (30/36)
      · −5.0% : fill 49% (31/56) · rebond 84% (28/31)
   - **flat** (35 séances) :
      · −1.0% : fill 81% (28/35) · rebond 79% (22/28)
      · −2.0% : fill 63% (21/35) · rebond 83% (16/21)
      · −3.0% : fill 50% (15/35) · rebond 82% (13/15)
      · −4.0% : fill 44% (14/35) · rebond 84% (12/14)
      · −5.0% : fill 39% (12/35) · rebond 100% (12/12)
   - **gap-up** (68 séances) :
      · −1.0% : fill 67% (40/68) · rebond 64% (26/40)
      · −2.0% : fill 54% (30/68) · rebond 55% (18/30)
      · −3.0% : fill 44% (24/68) · rebond 76% (19/24)
      · −4.0% : fill 37% (19/68) · rebond 64% (12/19)
      · −5.0% : fill 33% (17/68) · rebond 79% (15/17)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 56% si les 15 1res min sont vertes (76 cas) · 35% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **44min** → P(séance verte=clôture>ouverture) 74% si début vert vs 19% si rouge (base 45% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 252min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **74%** · continue >prix actuel 56% ; creux résiduel méd -2.35% (q20 -5.08%) → **SL/trailing à −5.08%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.24% / q75 +5.15% → **scale +3.24% / runner +5.15%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **19%** (continue à baisser 49%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −9.21%** (au-delà de la MAE q10 -9.21%), cible rebond +2.68% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.37% .. +6.56%] · haut q95 +8.06% · bas q05 -7.51%
   - 60min (n=160) : retour [-5.87% .. +7.0%] · haut q95 +9.42% · bas q05 -7.73%
   - 2h (n=160) : retour [-6.07% .. +9.75%] · haut q95 +10.09% · bas q05 -8.02%
   - 4h (n=160) : retour [-7.37% .. +9.52%] · haut q95 +12.06% · bas q05 -10.5%
   - 6h (n=160) : retour [-6.74% .. +10.15%] · haut q95 +14.18% · bas q05 -10.93%
   - session (n=160) : retour [-8.09% .. +12.84%] · haut q95 +14.18% · bas q05 -11.27%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.44%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 51.0  _(neutre)_
- **ADX** : 15.1  _(pas de tendance nette)_
- **MACD** : hist 0.601  _(pas de croisement recent)_
- **BB** : %B 0.68 · largeur 19.3%
- **ATR** : 1.91 (54.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.118  _(distribution)_
- **Vol ratio** : 0.43  _(volume atone)_
- **Choppiness** : 52.9  _(transition)_
- **MA** : MA20 26.91 · MA50 32.26 · MA200 25.34  _(prix > MA20)_
- **Dist MA** : MA20 +3.5% · MA50 -13.6% · MA200 +9.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93693 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
