# 005930

**Generated** : 2026-07-23T21:48:26.907498+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩270000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)  
> ↳ spot ₩270000.00 (+0.7% vs entrée) · entrée ₩268000.00 · stop ₩260875.00 · T1 ₩276849.36 · R/R 1.24  
> ↳ P(T1 av. stop) 31 % _(réel 5 s)_ · EV/risk -0.167 _(réel 5 s)_ (GBM -0.057) · ¼-Kelly 0.004 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.66% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

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
- Entry (zone de repli) : ₩266230.13–₩269769.87 (mid ₩268000.00)
- Spot actuel : ₩270000.00 (+0.7% au-dessus de la zone — repli à attendre)
- Stop : ₩260875.00 (stop swing_plan-based (-5.26%))
- Targets : T1 ₩276849.36 · R/R 1.24 | T2 ₩285698.71 · R/R 2.48 | T3 ₩294548.07 · R/R 3.73
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩260875.00


## Edge, scénarios & sizing

- EV/risk : -0.057 | EV/share : ₩-406.433 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 27 % | T2 19 % | T3 19 %
- Kelly (position) : f* 0.017 | ¼-Kelly 0.004 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.7 | bear 56.1 | side 37.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.741% → cible +3.302% / stop −2.659%, p_fill 84%, n_eff≈33.2) : P(cible|rempli) **31%** · **EV/risk -0.167** (×p_fill ; si rempli -0.53% du capital)
  - **swing** (entrée dip −1.628% → cible +7.383% / stop −3.692%, p_fill 84%, n_eff≈31.3) : P(cible|rempli) **25%** · **EV/risk -0.239** (×p_fill ; si rempli -1.05% du capital)
  - **deep** (entrée dip −2.521% → cible +10.442% / stop −5.221%, p_fill 79%, n_eff≈28.5) : P(cible|rempli) **27%** · **EV/risk -0.187** (×p_fill ; si rempli -1.23% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→66% · +2.0%→45% · +3.0%→30% · +5.0%→20% · +8.0%→5%
- Range intraday médian 5.45% (p90 9.32%) · excursion haute méd. +1.86% / basse méd. −2.52%
- Profil de vol intra : ouverture 2.767% vs midi 1.167% vs clôture 1.399% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (138 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 10% · trend ↑1%/↓1% ; spike-down 64% · recovery-V 21%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; mean-reverting — autocorr -0.083)_ ; drift intra méd. -0.634% ; recovery-V 19%
- **σ réalisé intraday** 4.345% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 71% / whipsaw 27%
- POC intraday (dernière séance, temps-au-prix) : 272981.25 (VA 270656.25–274918.75 ; dernier close 260800.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 30% · rebond 71% · **stop −6.28%** sous le fill (sous le bruit) · cible +1.69% · R/R 0.27 (high win-rate)
- Gaps overnight (n=137) : méd. 0.13% · baisse 46% (gap-down >1% 36% · >2% 25%)
- Excursion ouverture 5min (n=138) : bas méd −0.53% (p90 −1.48%) · haut méd +0.71% · range méd 1.45%
- Excursion ouverture 15min (n=138) : bas méd −0.88% (p90 −2.33%) · haut méd +1.05% · range méd 2.06%
- Excursion ouverture 30min (n=138) : bas méd −1.19% (p90 −2.71%) · haut méd +1.14% · range méd 2.47%
- Excursion ouverture 60min (n=138) : bas méd −1.52% (p90 −3.4%) · haut méd +1.36% · range méd 3.04%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 260800.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 54% · séance 66% (85/137) · gap 39% · délai 0.0min · rebond 55% (47/85) (MFE +1.51%)
   - −1.0% : fill 30min 49% · séance 64% (79/137) · gap 36% · délai 0.0min · rebond 62% (46/79) (MFE +1.48%)
   - −1.5% : fill 30min 44% · séance 56% (69/137) · gap 27% · délai 0.3min · rebond 60% (42/69) (MFE +1.69%)
   - −2.0% : fill 30min 41% · séance 50% (61/137) · gap 25% · délai 0.0min · rebond 59% (36/61) (MFE +1.86%)
   - −3.0% : fill 30min 31% · séance 45% (52/137) · gap 20% · délai 0.9min · rebond 64% (35/52) (MFE +2.42%)
   - −4.0% : fill 30min 22% · séance 38% (41/137) · gap 14% · délai 16.7min · rebond 66% (29/41) (MFE +2.44%)
   - −5.0% : fill 30min 14% · séance 30% (31/137) · gap 9% · délai 61.2min · rebond 71% (22/31) (MFE +1.69%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.33% (p90 −1.76%) → stop au-delà de −1.19% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.38% (p90 −2.56%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.31% (p90 −2.14%) → stop au-delà de −1.12% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=595 jambes) : jambe baissière méd −1.32% (p90 −3.07%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (59 séances) :
      · −1.0% : fill 97% (56/59) · rebond 52% (30/56)
      · −2.0% : fill 88% (48/59) · rebond 48% (25/48)
      · −3.0% : fill 85% (43/59) · rebond 58% (28/43)
      · −4.0% : fill 74% (35/59) · rebond 62% (24/35)
      · −5.0% : fill 62% (27/59) · rebond 68% (18/27)
   - **flat** (13 séances) :
      · −1.0% : fill 58% (7/13) · rebond 70% (4/7)
      · −2.0% : fill 40% (4/13) · rebond 85% (3/4)
      · −3.0% : fill 40% (4/13) · rebond 85% (3/4)
      · −4.0% : fill 18% (2/13) · rebond 100% (2/2)
      · −5.0% : fill 18% (2/13) · rebond 100% (2/2)
   - **gap-up** (65 séances) :
      · −1.0% : fill 34% (16/65) · rebond 84% (12/16)
      · −2.0% : fill 18% (9/65) · rebond 94% (8/9)
      · −3.0% : fill 9% (5/65) · rebond 89% (4/5)
      · −4.0% : fill 9% (4/65) · rebond 88% (3/4)
      · −5.0% : fill 3% (2/65) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=138) : 43% en base · 66% si les 15 1res min sont vertes (69 cas) · 19% si rouges (69 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=138) : COUDE à **27min** → P(séance verte=clôture>ouverture) 78% si début vert vs 11% si rouge (base 43% · écart 67 pts) ; prédictivité sature ensuite (plafond brut 125min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **78%** · continue >prix actuel 63% ; creux résiduel méd -1.61% (q20 -4.63%) → **SL/trailing à −4.63%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.45% / q75 +4.41% → **scale +2.45% / runner +4.41%**, sortie à la clôture
  - **si ROUGE au coude** (n=68) : edge inversé — récupère vert seulement **11%** (continue à baisser 64%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.74%** (au-delà de la MAE q10 -6.74%), cible rebond +1.32% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=138) : retour [-2.28% .. +3.3%] · haut q95 +4.51% · bas q05 -3.09%
   - 60min (n=138) : retour [-3.04% .. +4.89%] · haut q95 +6.2% · bas q05 -3.69%
   - 2h (n=138) : retour [-4.41% .. +4.84%] · haut q95 +6.45% · bas q05 -5.12%
   - 4h (n=138) : retour [-5.31% .. +5.97%] · haut q95 +6.87% · bas q05 -7.36%
   - 6h (n=138) : retour [-6.49% .. +5.77%] · haut q95 +7.77% · bas q05 -8.06%
   - session (n=138) : retour [-5.96% .. +5.93%] · haut q95 +7.77% · bas q05 -8.81%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 4.3% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.73%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 45.9  _(neutre)_
- **ADX** : 22.8  _(pas de tendance nette)_
- **MACD** : hist -3197.694  _(pas de croisement recent)_
- **BB** : %B 0.34 · largeur 44.7%
- **ATR** : 23750.0 (88.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.162  _(distribution)_
- **Vol ratio** : 0.55  _(volume atone)_
- **Choppiness** : 51.7  _(transition)_
- **MA** : MA20 290250.0 · MA50 305200.0 · MA200 188376.62  _(prix < MA20)_
- **Dist MA** : MA20 -7.0% · MA50 -11.5% · MA200 +43.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (84577 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
