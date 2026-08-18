# PRY

**Generated** : 2026-08-18T00:11:44.061309+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · €131.35  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €131.35 (+3.5% vs entrée) · entrée €126.87 · stop €120.87 · T1 €130.78 · R/R 0.65  
> ↳ P(T1 av. stop) 54 % _(réel 5 s)_ · EV/risk -0.054 _(réel 5 s)_ (GBM -0.007) · ¼-Kelly 0.002 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.110 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €126.08–€127.65 (mid €126.87)
- Spot actuel : €131.35 (+3.5% au-dessus de la zone — repli à attendre)
- Stop : €120.87 (stop swing_plan-based (-7.98%))
- Targets : T1 €130.78 · R/R 0.65 | T2 €134.70 · R/R 1.3 | T3 €138.62 · R/R 1.96
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €120.87


## Edge, scénarios & sizing

- EV/risk : -0.007 | EV/share : €-0.045 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 26 % | T3 9 %
- Kelly (position) : f* 0.01 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 20.3 | bear 31.1 | side 48.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 394.0 (= 3 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.554% → cible +1.38% / stop −8.0%, p_fill 52%, n_eff≈23.2) : P(cible|rempli) **43%** · **EV/risk -0.023** (×p_fill ; si rempli -0.36% du capital)
  - **swing** (entrée dip −3.412% → cible +3.087% / stop −4.729%, p_fill 52%, n_eff≈20.9) : P(cible|rempli) **54%** · **EV/risk -0.054** (×p_fill ; si rempli -0.50% du capital)
  - **deep** (entrée dip −5.278% → cible +4.365% / stop −7.233%, p_fill 57%, n_eff≈19.7) : P(cible|rempli) **51%** · **EV/risk -0.089** (×p_fill ; si rempli -1.13% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→68% · +2.0%→42% · +3.0%→29% · +5.0%→10% · +8.0%→4%
- Range intraday médian 4.35% (p90 6.51%) · excursion haute méd. +1.51% / basse méd. −1.61%
- Profil de vol intra : ouverture 2.484% vs midi 0.844% vs clôture 1.205% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (155 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 10% · trend ↑0%/↓0% ; spike-down 54% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.118 ; neutre — autocorr -0.013)_ ; drift intra méd. -0.698% ; recovery-V 28%
- **σ réalisé intraday** 2.724% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 58% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 129.2 (VA 128.88–129.84 ; dernier close 128.26)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 19% · rebond 71% · **stop −2.55%** sous le fill (sous le bruit) · cible +1.37% · R/R 0.54 (high win-rate)
- Gaps overnight (n=154) : méd. 0.38% · baisse 38% (gap-down >1% 18% · >2% 9%)
- Excursion ouverture 5min (n=155) : bas méd −0.84% (p90 −2.2%) · haut méd +0.29% · range méd 1.4%
- Excursion ouverture 15min (n=155) : bas méd −1.03% (p90 −2.81%) · haut méd +0.55% · range méd 1.75%
- Excursion ouverture 30min (n=155) : bas méd −1.04% (p90 −2.97%) · haut méd +0.69% · range méd 1.97%
- Excursion ouverture 60min (n=155) : bas méd −1.18% (p90 −3.22%) · haut méd +0.87% · range méd 2.21%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 128.26 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 70% (111/154) · gap 24% · délai 0.2min · rebond 62% (70/111) (MFE +1.29%)
   - −1.0% : fill 30min 48% · séance 62% (94/154) · gap 18% · délai 0.4min · rebond 60% (57/94) (MFE +1.57%)
   - −1.5% : fill 30min 32% · séance 52% (81/154) · gap 14% · délai 3.2min · rebond 55% (45/81) (MFE +1.09%)
   - −2.0% : fill 30min 23% · séance 44% (66/154) · gap 9% · délai 13.1min · rebond 62% (42/66) (MFE +1.36%)
   - −3.0% : fill 30min 12% · séance 32% (47/154) · gap 3% · délai 76.9min · rebond 65% (32/47) (MFE +1.64%)
   - −4.0% : fill 30min 3% · séance 19% (25/154) · gap 1% · délai 249.0min · rebond 71% (18/25) (MFE +1.37%)
   - −5.0% : fill 30min 1% · séance 12% (17/154) · gap 1% · délai 394.0min · rebond 76% (13/17) (MFE +1.58%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −1.88%) → stop au-delà de −1.49% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.52% (p90 −2.03%) → stop au-delà de −1.37% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.09% (p90 −1.95%) → stop au-delà de −1.11% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=484 jambes) : jambe baissière méd −1.06% (p90 −2.49%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (53 séances) :
      · −1.0% : fill 90% (48/53) · rebond 50% (27/48)
      · −2.0% : fill 69% (38/53) · rebond 64% (26/38)
      · −3.0% : fill 56% (29/53) · rebond 71% (22/29)
      · −4.0% : fill 36% (16/53) · rebond 65% (11/16)
      · −5.0% : fill 27% (12/53) · rebond 73% (9/12)
   - **flat** (28 séances) :
      · −1.0% : fill 72% (16/28) · rebond 60% (10/16)
      · −2.0% : fill 51% (9/28) · rebond 89% (7/9)
      · −3.0% : fill 20% (5/28) · rebond 40% (2/5)
      · −4.0% : fill 9% (3/28) · rebond 59% (2/3)
      · −5.0% : fill 5% (2/28) · rebond 25% (1/2)
   - **gap-up** (73 séances) :
      · −1.0% : fill 40% (30/73) · rebond 74% (20/30)
      · −2.0% : fill 26% (19/73) · rebond 43% (9/19)
      · −3.0% : fill 21% (13/73) · rebond 63% (8/13)
      · −4.0% : fill 11% (6/73) · rebond 86% (5/6)
      · −5.0% : fill 5% (3/73) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=155) : 48% en base · 66% si les 15 1res min sont vertes (72 cas) · 33% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=155) : COUDE à **1:09** → P(séance verte=clôture>ouverture) 79% si début vert vs 24% si rouge (base 48% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **79%** · continue >prix actuel 62% ; creux résiduel méd -1.21% (q20 -2.02%) → **SL/trailing à −2.02%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.67% / q75 +2.66% → **scale +1.67% / runner +2.66%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **24%** (continue à baisser 66%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.12%** (au-delà de la MAE q10 -4.12%), cible rebond +1.22% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=155) : retour [-2.89% .. +2.72%] · haut q95 +3.45% · bas q05 -3.4%
   - 60min (n=155) : retour [-3.39% .. +2.19%] · haut q95 +3.92% · bas q05 -3.57%
   - 2h (n=155) : retour [-3.61% .. +2.73%] · haut q95 +4.05% · bas q05 -4.6%
   - 4h (n=155) : retour [-3.61% .. +3.3%] · haut q95 +4.25% · bas q05 -4.76%
   - 6h (n=155) : retour [-3.72% .. +3.84%] · haut q95 +4.61% · bas q05 -5.18%
   - session (n=155) : retour [-4.34% .. +4.08%] · haut q95 +5.53% · bas q05 -6.27%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.5% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.41%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 63.2  _(momentum haussier)_
- **ADX** : 25.3  _(tendance etablie)_
- **MACD** : hist 1.664  _(pas de croisement recent)_
- **BB** : %B 0.84 · largeur 15.1%
- **ATR** : 6.0 (82.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.107  _(distribution)_
- **Vol ratio** : 0.28  _(volume atone)_
- **Choppiness** : 46.5  _(transition)_
- **MA** : MA20 125.02 · MA50 135.24 · MA200 112.34  _(prix > MA20)_
- **Dist MA** : MA20 +5.1% · MA50 -2.9% · MA200 +16.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93404 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
