# 005930

**Generated** : 2026-07-31T00:12:57.278474+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩207000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩207000.00 (+5.0% vs entrée) · entrée ₩197175.12 · stop ₩189925.83 · T1 ₩208338.53 · R/R 1.54  
> ↳ P(T1 av. stop) 4 % _(réel 5 s)_ · EV/risk -0.091 _(réel 5 s)_ (GBM -0.043) · ¼-Kelly 0.009 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.68% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩195766.47–₩198583.76 (mid ₩197175.12)
- Spot actuel : ₩207000.00 (+5.0% au-dessus de la zone — repli à attendre)
- Stop : ₩189925.83 (stop swing_plan-based (-19.36%))
- Targets : T1 ₩208338.53 · R/R 1.54 | T2 ₩213289.62 · R/R 2.22 | T3 ₩218240.72 · R/R 2.91
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩189925.83


## Edge, scénarios & sizing

- EV/risk : -0.043 | EV/share : ₩-311.474 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 20 % | T2 20 % | T3 20 %
- Kelly (position) : f* 0.035 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.5 | bear 80.3 | side 14.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.748% → cible +5.662% / stop −3.677%, p_fill 37%, n_eff≈13.0) : P(cible|rempli) **4%** · **EV/risk -0.091** (×p_fill ; si rempli -0.91% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=11, n_eff=10))
  - **deep** : indisponible (échantillon insuffisant (n=4, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→66% · +2.0%→46% · +3.0%→31% · +5.0%→20% · +8.0%→5%
- Range intraday médian 5.73% (p90 9.34%) · excursion haute méd. +1.86% / basse méd. −2.61%
- Profil de vol intra : ouverture 2.835% vs midi 1.24% vs clôture 1.46% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (143 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 13% · trend ↑1%/↓1% ; spike-down 67% · recovery-V 21%)_
- **Régime intraday** : **chop** _(efficiency 0.134 ; mean-reverting — autocorr -0.082)_ ; drift intra méd. -1.463% ; recovery-V 19%
- **σ réalisé intraday** 4.523% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 39% / bas 77% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 202007.5 (VA 197587.5–225212.5 ; dernier close 209500.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 32% · rebond 65% · **stop −6.89%** sous le fill (sous le bruit) · cible +1.51% · R/R 0.22 (high win-rate)
- Gaps overnight (n=142) : méd. 0.17% · baisse 45% (gap-down >1% 36% · >2% 25%)
- Excursion ouverture 5min (n=143) : bas méd −0.59% (p90 −1.45%) · haut méd +0.65% · range méd 1.44%
- Excursion ouverture 15min (n=143) : bas méd −0.89% (p90 −2.34%) · haut méd +1.04% · range méd 2.14%
- Excursion ouverture 30min (n=143) : bas méd −1.2% (p90 −2.81%) · haut méd +1.13% · range méd 2.61%
- Excursion ouverture 60min (n=143) : bas méd −1.54% (p90 −3.4%) · haut méd +1.36% · range méd 3.06%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 209500.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 53% · séance 68% (89/142) · gap 39% · délai 0.0min · rebond 52% (48/89) (MFE +1.21%)
   - −1.0% : fill 30min 49% · séance 65% (83/142) · gap 36% · délai 0.0min · rebond 58% (47/83) (MFE +1.31%)
   - −1.5% : fill 30min 44% · séance 59% (73/142) · gap 26% · délai 0.3min · rebond 56% (43/73) (MFE +1.46%)
   - −2.0% : fill 30min 41% · séance 51% (64/142) · gap 25% · délai 0.1min · rebond 53% (36/64) (MFE +1.34%)
   - −3.0% : fill 30min 32% · séance 46% (55/142) · gap 20% · délai 1.7min · rebond 56% (35/55) (MFE +1.75%)
   - −4.0% : fill 30min 24% · séance 40% (44/142) · gap 15% · délai 23.1min · rebond 62% (30/44) (MFE +1.53%)
   - −5.0% : fill 30min 14% · séance 32% (34/142) · gap 10% · délai 79.3min · rebond 65% (23/34) (MFE +1.51%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.35% (p90 −1.75%) → stop au-delà de −1.07% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.4% (p90 −2.54%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.4% (p90 −1.98%) → stop au-delà de −1.05% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=641 jambes) : jambe baissière méd −1.31% (p90 −3.14%) · ~12.8 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (61 séances) :
      · −1.0% : fill 97% (58/61) · rebond 48% (30/58)
      · −2.0% : fill 89% (50/61) · rebond 44% (25/50)
      · −3.0% : fill 86% (45/61) · rebond 52% (28/45)
      · −4.0% : fill 76% (37/61) · rebond 55% (24/37)
      · −5.0% : fill 65% (29/61) · rebond 59% (18/29)
   - **flat** (13 séances) :
      · −1.0% : fill 58% (7/13) · rebond 70% (4/7)
      · −2.0% : fill 40% (4/13) · rebond 85% (3/4)
      · −3.0% : fill 40% (4/13) · rebond 85% (3/4)
      · −4.0% : fill 18% (2/13) · rebond 100% (2/2)
      · −5.0% : fill 18% (2/13) · rebond 100% (2/2)
   - **gap-up** (68 séances) :
      · −1.0% : fill 38% (18/68) · rebond 77% (13/18)
      · −2.0% : fill 20% (10/68) · rebond 76% (8/10)
      · −3.0% : fill 12% (6/68) · rebond 60% (4/6)
      · −4.0% : fill 12% (5/68) · rebond 92% (4/5)
      · −5.0% : fill 6% (3/68) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=143) : 41% en base · 65% si les 15 1res min sont vertes (71 cas) · 17% si rouges (72 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=143) : COUDE à **1:14** → P(séance verte=clôture>ouverture) 82% si début vert vs 8% si rouge (base 41% · écart 74 pts) ; prédictivité sature ensuite (plafond brut 129min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **82%** · continue >prix actuel 52% ; creux résiduel méd -1.59% (q20 -4.19%) → **SL/trailing à −4.19%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.54% / q75 +3.38% → **scale +1.54% / runner +3.38%**, sortie à la clôture
  - **si ROUGE au coude** (n=67) : edge inversé — récupère vert seulement **8%** (continue à baisser 58%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.27%** (au-delà de la MAE q10 -7.27%), cible rebond +1.17% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=143) : retour [-2.63% .. +3.03%] · haut q95 +3.91% · bas q05 -3.18%
   - 60min (n=143) : retour [-3.13% .. +4.87%] · haut q95 +5.92% · bas q05 -3.59%
   - 2h (n=143) : retour [-5.29% .. +4.74%] · haut q95 +6.33% · bas q05 -5.26%
   - 4h (n=143) : retour [-6.69% .. +5.78%] · haut q95 +6.84% · bas q05 -8.28%
   - 6h (n=143) : retour [-7.55% .. +5.62%] · haut q95 +7.47% · bas q05 -8.95%
   - session (n=143) : retour [-7.63% .. +5.77%] · haut q95 +7.47% · bas q05 -9.47%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 4.2% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.84%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 31.9  _(momentum baissier)_
- **ADX** : 28.3  _(tendance etablie)_
- **MACD** : hist -5931.181  _(pas de croisement recent)_
- **BB** : %B 0.02 · largeur 45.1%
- **ATR** : 24164.29 (88.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.266  _(distribution)_
- **Vol ratio** : 1.5  _(volume au-dessus de la moyenne)_
- **Choppiness** : 43.0  _(transition)_
- **MA** : MA20 263725.0 · MA50 299577.38 · MA200 191800.23  _(prix < MA20)_
- **Dist MA** : MA20 -21.5% · MA50 -30.9% · MA200 +7.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (82341 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
