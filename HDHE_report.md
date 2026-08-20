# 267260

**Generated** : 2026-08-20T00:12:40.457585+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩752000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩752000.00 (+1.4% vs entrée) · entrée ₩741709.24 · stop ₩690000.02 · T1 ₩809438.54 · R/R 1.31  
> ↳ P(T1 av. stop) 27 % _(réel 5 s)_ · EV/risk -0.181 _(réel 5 s)_ (GBM 0.082) · ¼-Kelly 0.004 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.020 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩731418.48–₩752000.00 (mid ₩741709.24)
- Spot actuel : ₩752000.00 (+1.4% au-dessus de la zone — repli à attendre)
- Stop : ₩690000.02 (stop swing_plan-based (-8.24%))
- Targets : T1 ₩809438.54 · R/R 1.31 | T2 ₩877167.84 · R/R 2.62 | T3 ₩944897.14 · R/R 3.93
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩690000.02


## Edge, scénarios & sizing

- EV/risk : 0.082 | EV/share : ₩4241.597 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 9 % | T3 3 %
- Kelly (position) : f* 0.014 | ¼-Kelly 0.004 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 33.6 | bear 12.9 | side 53.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.62% → cible +11.993% / stop −8.0%, p_fill 98%, n_eff≈40.0) : P(cible|rempli) **0%** · **EV/risk -0.135** (×p_fill ; si rempli -1.10% du capital)
  - **swing** (entrée dip −1.363% → cible +9.132% / stop −6.972%, p_fill 95%, n_eff≈38.2) : P(cible|rempli) **27%** · **EV/risk -0.181** (×p_fill ; si rempli -1.32% du capital)
  - **deep** (entrée dip −1.985% → cible +12.914% / stop −10.524%, p_fill 97%, n_eff≈38.1) : P(cible|rempli) **31%** · **EV/risk -0.387** (×p_fill ; si rempli -4.19% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→68% · +2.0%→45% · +3.0%→35% · +5.0%→11% · +8.0%→4%
- Range intraday médian 6.79% (p90 10.49%) · excursion haute méd. +1.66% / basse méd. −3.96%
- Profil de vol intra : ouverture 4.404% vs midi 1.203% vs clôture 1.248% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (155 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 82% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.12 ; mean-reverting — autocorr -0.063)_ ; drift intra méd. -1.508% ; recovery-V 28%
- **σ réalisé intraday** 4.493% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 43% / bas 68% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 783093.75 (VA 770906.25–790406.25 ; dernier close 800000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 32% · rebond 82% · **stop −4.53%** sous le fill (sous le bruit) · cible +2.54% · R/R 0.56 (high win-rate)
- Gaps overnight (n=154) : méd. 1.26% · baisse 38% (gap-down >1% 20% · >2% 11%)
- Excursion ouverture 5min (n=155) : bas méd −1.64% (p90 −3.96%) · haut méd +0.98% · range méd 2.84%
- Excursion ouverture 15min (n=155) : bas méd −1.95% (p90 −4.69%) · haut méd +1.06% · range méd 3.46%
- Excursion ouverture 30min (n=155) : bas méd −2.2% (p90 −5.04%) · haut méd +1.08% · range méd 3.78%
- Excursion ouverture 60min (n=155) : bas méd −2.58% (p90 −5.62%) · haut méd +1.26% · range méd 4.13%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 800000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 72% (109/154) · gap 30% · délai 0.0min · rebond 57% (62/109) (MFE +1.27%)
   - −1.0% : fill 30min 52% · séance 68% (101/154) · gap 20% · délai 0.3min · rebond 60% (61/101) (MFE +1.34%)
   - −1.5% : fill 30min 44% · séance 61% (87/154) · gap 14% · délai 0.4min · rebond 67% (57/87) (MFE +1.39%)
   - −2.0% : fill 30min 41% · séance 57% (79/154) · gap 11% · délai 0.7min · rebond 73% (55/79) (MFE +1.79%)
   - −3.0% : fill 30min 31% · séance 46% (62/154) · gap 6% · délai 1.8min · rebond 79% (44/62) (MFE +1.97%)
   - −4.0% : fill 30min 22% · séance 39% (51/154) · gap 3% · délai 16.5min · rebond 77% (40/51) (MFE +2.28%)
   - −5.0% : fill 30min 14% · séance 32% (40/154) · gap 1% · délai 39.2min · rebond 82% (31/40) (MFE +2.54%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.74% (p90 −3.43%) → stop au-delà de −2.34% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.93% (p90 −3.44%) → stop au-delà de −2.41% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.26% (p90 −5.02%) → stop au-delà de −3.41% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=798 jambes) : jambe baissière méd −1.22% (p90 −3.35%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (53 séances) :
      · −1.0% : fill 98% (52/53) · rebond 52% (28/52)
      · −2.0% : fill 94% (45/53) · rebond 68% (28/45)
      · −3.0% : fill 86% (39/53) · rebond 79% (27/39)
      · −4.0% : fill 74% (34/53) · rebond 77% (27/34)
      · −5.0% : fill 61% (26/53) · rebond 82% (20/26)
   - **flat** (17 séances) :
      · −1.0% : fill 88% (14/17) · rebond 47% (7/14)
      · −2.0% : fill 79% (12/17) · rebond 78% (9/12)
      · −3.0% : fill 78% (11/17) · rebond 83% (8/11)
      · −4.0% : fill 57% (7/17) · rebond 68% (5/7)
      · −5.0% : fill 57% (7/17) · rebond 89% (6/7)
   - **gap-up** (84 séances) :
      · −1.0% : fill 47% (35/84) · rebond 75% (26/35)
      · −2.0% : fill 32% (22/84) · rebond 79% (18/22)
      · −3.0% : fill 19% (12/84) · rebond 77% (9/12)
      · −4.0% : fill 15% (10/84) · rebond 82% (8/10)
      · −5.0% : fill 11% (7/84) · rebond 78% (5/7)
- **P(clôture VERTE) selon le drive 15min** (n=155) : 34% en base · 48% si les 15 1res min sont vertes (69 cas) · 27% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=155) : COUDE à **1:19** → P(séance verte=clôture>ouverture) 68% si début vert vs 13% si rouge (base 34% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=68) : tient le vert **68%** · continue >prix actuel 43% ; creux résiduel méd -1.81% (q20 -3.51%) → **SL/trailing à −3.51%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.45% / q75 +2.48% → **scale +1.45% / runner +2.48%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **13%** (continue à baisser 49%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.34%** (au-delà de la MAE q10 -5.34%), cible rebond +1.64% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=155) : retour [-5.24% .. +2.68%] · haut q95 +4.03% · bas q05 -5.68%
   - 60min (n=155) : retour [-5.65% .. +2.71%] · haut q95 +4.39% · bas q05 -6.04%
   - 2h (n=155) : retour [-7.0% .. +3.67%] · haut q95 +5.0% · bas q05 -7.43%
   - 4h (n=155) : retour [-6.94% .. +3.84%] · haut q95 +5.31% · bas q05 -8.54%
   - 6h (n=155) : retour [-8.04% .. +3.84%] · haut q95 +6.29% · bas q05 -9.32%
   - session (n=155) : retour [-7.55% .. +3.92%] · haut q95 +6.39% · bas q05 -9.68%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.49%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 72.8  _(surachat)_
- **ADX** : 18.7  _(pas de tendance nette)_
- **MACD** : hist 15244.755  _(pas de croisement recent)_
- **BB** : %B 0.52 · largeur 38.4%
- **ATR** : 51709.22 (46.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.021  _(neutre)_
- **Vol ratio** : 0.61  _(volume normal)_
- **Choppiness** : 39.5  _(transition)_
- **MA** : MA20 745275.64 · MA50 863466.61 · MA200 925263.26  _(prix > MA20)_
- **Dist MA** : MA20 +0.9% · MA50 -12.9% · MA200 -18.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (98863 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
