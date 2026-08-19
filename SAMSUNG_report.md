# 005930

**Generated** : 2026-08-19T00:14:26.022996+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩268500.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩268500.00 (+1.5% vs entrée) · entrée ₩264446.49 · stop ₩242496.49 · T1 ₩289498.79 · R/R 1.14  
> ↳ P(T1 av. stop) 32 % _(réel 5 s)_ · EV/risk -0.216 _(réel 5 s)_ (GBM 0.272) · ¼-Kelly 0.016 · _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.130 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩260392.98–₩268500.00 (mid ₩264446.49)
- Spot actuel : ₩268500.00 (+1.5% au-dessus de la zone — repli à attendre)
- Stop : ₩242496.49 (stop swing_plan-based (-9.68%))
- Targets : T1 ₩289498.79 · R/R 1.14 | T2 ₩314551.09 · R/R 2.28 | T3 ₩339603.39 · R/R 3.42
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩242496.49


## Edge, scénarios & sizing

- EV/risk : 0.272 | EV/share : ₩5978.106 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 11 % | T3 1 %
- Kelly (position) : f* 0.065 | ¼-Kelly 0.016 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 52.5 | bear 34.3 | side 13.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.677% → cible +4.237% / stop −2.469%, p_fill 93%, n_eff≈36.6) : P(cible|rempli) **19%** · **EV/risk -0.323** (×p_fill ; si rempli -0.86% du capital)
  - **swing** (entrée dip −1.505% → cible +9.473% / stop −8.3%, p_fill 91%, n_eff≈35.2) : P(cible|rempli) **32%** · **EV/risk -0.216** (×p_fill ; si rempli -1.96% du capital)
  - **deep** (entrée dip −2.197% → cible +13.398% / stop −12.539%, p_fill 86%, n_eff≈32.8) : P(cible|rempli) **23%** · **EV/risk -0.372** (×p_fill ; si rempli -5.43% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→69% · +2.0%→46% · +3.0%→36% · +5.0%→24% · +8.0%→5%
- Range intraday médian 6.21% (p90 9.84%) · excursion haute méd. +1.9% / basse méd. −3.08%
- Profil de vol intra : ouverture 3.118% vs midi 1.366% vs clôture 1.555% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (155 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 10% · trend ↑0%/↓1% ; spike-down 70% · recovery-V 20%)_
- **Régime intraday** : **chop** _(efficiency 0.12 ; mean-reverting — autocorr -0.091)_ ; drift intra méd. -1.093% ; recovery-V 19%
- **σ réalisé intraday** 4.386% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 40% / bas 76% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 269931.25 (VA 268868.75–272481.25 ; dernier close 274000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 29% · rebond 58% · **stop −6.75%** sous le fill (sous le bruit) · cible +1.3% · R/R 0.19 (high win-rate)
- Gaps overnight (n=154) : méd. 0.7% · baisse 41% (gap-down >1% 32% · >2% 23%)
- Excursion ouverture 5min (n=155) : bas méd −0.74% (p90 −1.65%) · haut méd +0.64% · range méd 1.56%
- Excursion ouverture 15min (n=155) : bas méd −1.03% (p90 −2.68%) · haut méd +1.06% · range méd 2.24%
- Excursion ouverture 30min (n=155) : bas méd −1.24% (p90 −3.24%) · haut méd +1.12% · range méd 2.79%
- Excursion ouverture 60min (n=155) : bas méd −1.75% (p90 −3.59%) · haut méd +1.25% · range méd 3.14%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 274000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 50% · séance 64% (95/154) · gap 34% · délai 0.0min · rebond 51% (51/95) (MFE +1.12%)
   - −1.0% : fill 30min 47% · séance 62% (89/154) · gap 32% · délai 0.0min · rebond 59% (51/89) (MFE +1.31%)
   - −1.5% : fill 30min 40% · séance 53% (77/154) · gap 24% · délai 0.3min · rebond 58% (46/77) (MFE +1.44%)
   - −2.0% : fill 30min 36% · séance 47% (68/154) · gap 23% · délai 0.2min · rebond 56% (39/68) (MFE +1.57%)
   - −3.0% : fill 30min 29% · séance 43% (59/154) · gap 18% · délai 1.7min · rebond 59% (38/59) (MFE +2.13%)
   - −4.0% : fill 30min 21% · séance 36% (47/154) · gap 14% · délai 26.2min · rebond 58% (31/47) (MFE +1.46%)
   - −5.0% : fill 30min 13% · séance 29% (36/154) · gap 9% · délai 50.8min · rebond 58% (23/36) (MFE +1.3%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.46% (p90 −2.2%) → stop au-delà de −1.24% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.53% (p90 −3.1%) → stop au-delà de −1.51% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.65% (p90 −3.57%) → stop au-delà de −1.62% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=729 jambes) : jambe baissière méd −1.27% (p90 −3.08%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (63 séances) :
      · −1.0% : fill 98% (60/63) · rebond 44% (30/60)
      · −2.0% : fill 90% (52/63) · rebond 44% (26/52)
      · −3.0% : fill 88% (47/63) · rebond 52% (29/47)
      · −4.0% : fill 78% (39/63) · rebond 48% (24/39)
      · −5.0% : fill 68% (31/63) · rebond 51% (18/31)
   - **flat** (14 séances) :
      · −1.0% : fill 65% (8/14) · rebond 78% (5/8)
      · −2.0% : fill 33% (4/14) · rebond 85% (3/4)
      · −3.0% : fill 33% (4/14) · rebond 85% (3/4)
      · −4.0% : fill 15% (2/14) · rebond 100% (2/2)
      · −5.0% : fill 15% (2/14) · rebond 100% (2/2)
   - **gap-up** (77 séances) :
      · −1.0% : fill 36% (21/77) · rebond 83% (16/21)
      · −2.0% : fill 20% (12/77) · rebond 83% (10/12)
      · −3.0% : fill 15% (8/77) · rebond 76% (6/8)
      · −4.0% : fill 12% (6/77) · rebond 94% (5/6)
      · −5.0% : fill 4% (3/77) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=155) : 38% en base · 58% si les 15 1res min sont vertes (77 cas) · 17% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=155) : COUDE à **1:15** → P(séance verte=clôture>ouverture) 84% si début vert vs 5% si rouge (base 38% · écart 79 pts) ; prédictivité sature ensuite (plafond brut 75min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **84%** · continue >prix actuel 57% ; creux résiduel méd -1.15% (q20 -4.2%) → **SL/trailing à −4.2%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.09% / q75 +3.65% → **scale +2.09% / runner +3.65%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **5%** (continue à baisser 61%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.99%** (au-delà de la MAE q10 -6.99%), cible rebond +1.3% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=155) : retour [-2.82% .. +2.83%] · haut q95 +3.68% · bas q05 -3.78%
   - 60min (n=155) : retour [-3.14% .. +4.47%] · haut q95 +5.39% · bas q05 -5.15%
   - 2h (n=155) : retour [-4.64% .. +4.57%] · haut q95 +6.18% · bas q05 -6.25%
   - 4h (n=155) : retour [-6.35% .. +5.63%] · haut q95 +6.89% · bas q05 -7.83%
   - 6h (n=155) : retour [-7.2% .. +5.07%] · haut q95 +7.02% · bas q05 -8.22%
   - session (n=155) : retour [-7.42% .. +5.29%] · haut q95 +7.02% · bas q05 -8.96%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.9% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.95%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 64.7  _(momentum haussier)_
- **ADX** : 20.9  _(pas de tendance nette)_
- **MACD** : hist 6646.073  _(pas de croisement recent)_
- **BB** : %B 0.78 · largeur 32.6%
- **ATR** : 21950.0 (79.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.133  _(distribution)_
- **Vol ratio** : 0.82  _(volume normal)_
- **Choppiness** : 43.0  _(transition)_
- **MA** : MA20 245700.0 · MA50 284250.14 · MA200 201091.36  _(prix > MA20)_
- **Dist MA** : MA20 +9.3% · MA50 -5.5% · MA200 +33.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (82587 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
