# 298040

**Generated** : 2026-07-20T00:17:00.383413+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩2789000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩2789000.00 (+1.1% vs entrée) · entrée ₩2759500.00 · stop ₩2538740.00 · T1 ₩2846194.03 · R/R 0.39  
> ↳ P(T1 av. stop) 43 % _(réel 5 s)_ · EV/risk -0.087 _(réel 5 s)_ (GBM -0.102) · ¼-Kelly 0.033 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩2742161.19–₩2776838.81 (mid ₩2759500.00)
- Spot actuel : ₩2789000.00 (+1.1% au-dessus de la zone — repli à attendre)
- Stop : ₩2538740.00 (stop swing_plan-based (-5.76%))
- Targets : T1 ₩2846194.03 · R/R 0.39 | T2 ₩2932888.06 · R/R 0.79 | T3 ₩3019582.09 · R/R 1.18
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2538740.00


## Edge, scénarios & sizing

- EV/risk : -0.102 | EV/share : ₩-22414.031 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 22 % | T3 22 %
- Kelly (position) : f* 0.132 | ¼-Kelly 0.033 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.5 | bear 75.9 | side 10.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.054% → cible +3.142% / stop −8.0%, p_fill 90%, n_eff≈35.3) : P(cible|rempli) **43%** · **EV/risk -0.087** (×p_fill ; si rempli -0.78% du capital)
  - **swing** (entrée dip −2.329% → cible +7.025% / stop −3.512%, p_fill 89%, n_eff≈34.2) : P(cible|rempli) **29%** · **EV/risk -0.171** (×p_fill ; si rempli -0.67% du capital)
  - **deep** (entrée dip −3.602% → cible +9.935% / stop −4.967%, p_fill 84%, n_eff≈31.5) : P(cible|rempli) **27%** · **EV/risk -0.181** (×p_fill ; si rempli -1.07% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→64% · +2.0%→52% · +3.0%→38% · +5.0%→22% · +8.0%→6%
- Range intraday médian 6.81% (p90 9.73%) · excursion haute méd. +2.14% / basse méd. −3.63%
- Profil de vol intra : ouverture 4.164% vs midi 1.055% vs clôture 1.135% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (135 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 22% · trend ↑0%/↓1% ; spike-down 79% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; mean-reverting — autocorr -0.086)_ ; drift intra méd. -1.567% ; recovery-V 30%
- **σ réalisé intraday** 5.345% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 43% / bas 71% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 2771875.0 (VA 2730175.0–2785775.0 ; dernier close 2762000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 33% · rebond 92% · **stop −5.35%** sous le fill (sous le bruit) · cible +2.4% · R/R 0.45 (high win-rate)
- Gaps overnight (n=134) : méd. 0.7% · baisse 38% (gap-down >1% 24% · >2% 16%)
- Excursion ouverture 5min (n=135) : bas méd −1.29% (p90 −3.4%) · haut méd +0.81% · range méd 2.67%
- Excursion ouverture 15min (n=135) : bas méd −1.89% (p90 −4.79%) · haut méd +1.11% · range méd 3.57%
- Excursion ouverture 30min (n=135) : bas méd −2.28% (p90 −4.92%) · haut méd +1.12% · range méd 4.07%
- Excursion ouverture 60min (n=135) : bas méd −2.51% (p90 −5.31%) · haut méd +1.36% · range méd 4.73%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2762000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 71% (92/134) · gap 31% · délai 0.1min · rebond 60% (57/92) (MFE +1.38%)
   - −1.0% : fill 30min 56% · séance 68% (84/134) · gap 24% · délai 0.8min · rebond 60% (52/84) (MFE +1.56%)
   - −1.5% : fill 30min 47% · séance 60% (75/134) · gap 20% · délai 1.3min · rebond 54% (46/75) (MFE +1.44%)
   - −2.0% : fill 30min 42% · séance 56% (66/134) · gap 16% · délai 3.1min · rebond 52% (36/66) (MFE +1.33%)
   - −3.0% : fill 30min 30% · séance 45% (53/134) · gap 8% · délai 5.3min · rebond 56% (30/53) (MFE +1.27%)
   - −4.0% : fill 30min 20% · séance 40% (45/134) · gap 5% · délai 33.4min · rebond 74% (34/45) (MFE +1.8%)
   - −5.0% : fill 30min 18% · séance 33% (34/134) · gap 4% · délai 28.4min · rebond 92% (29/34) (MFE +2.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.72% (p90 −3.32%) → stop au-delà de −2.29% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.76% (p90 −3.53%) → stop au-delà de −2.46% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.81% (p90 −3.44%) → stop au-delà de −2.05% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=710 jambes) : jambe baissière méd −1.43% (p90 −3.48%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (46 séances) :
      · −1.0% : fill 100% (46/46) · rebond 61% (29/46)
      · −2.0% : fill 86% (38/46) · rebond 54% (21/38)
      · −3.0% : fill 82% (36/46) · rebond 55% (20/36)
      · −4.0% : fill 76% (31/46) · rebond 77% (23/31)
      · −5.0% : fill 68% (26/46) · rebond 89% (21/26)
   - **flat** (15 séances) :
      · −1.0% : fill 82% (10/15) · rebond 57% (7/10)
      · −2.0% : fill 72% (7/15) · rebond 73% (5/7)
      · −3.0% : fill 43% (4/15) · rebond 100% (4/4)
      · −4.0% : fill 43% (4/15) · rebond 63% (3/4)
      · −5.0% : fill 31% (2/15) · rebond 100% (2/2)
   - **gap-up** (73 séances) :
      · −1.0% : fill 45% (28/73) · rebond 59% (16/28)
      · −2.0% : fill 34% (21/73) · rebond 42% (10/21)
      · −3.0% : fill 23% (13/73) · rebond 43% (6/13)
      · −4.0% : fill 17% (10/73) · rebond 71% (8/10)
      · −5.0% : fill 12% (6/73) · rebond 100% (6/6)
- **P(clôture VERTE) selon le drive 15min** (n=135) : 39% en base · 62% si les 15 1res min sont vertes (55 cas) · 27% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=135) : COUDE à **1:21** → P(séance verte=clôture>ouverture) 81% si début vert vs 12% si rouge (base 39% · écart 69 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=61) : tient le vert **81%** · continue >prix actuel 52% ; creux résiduel méd -1.5% (q20 -3.91%) → **SL/trailing à −3.91%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.55% / q75 +2.9% → **scale +1.55% / runner +2.9%**, sortie à la clôture
  - **si ROUGE au coude** (n=74) : edge inversé — récupère vert seulement **12%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.54%** (au-delà de la MAE q10 -5.54%), cible rebond +1.35% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=135) : retour [-4.47% .. +4.3%] · haut q95 +6.12% · bas q05 -5.24%
   - 60min (n=135) : retour [-5.32% .. +4.92%] · haut q95 +6.66% · bas q05 -5.97%
   - 2h (n=135) : retour [-7.37% .. +4.54%] · haut q95 +7.22% · bas q05 -8.2%
   - 4h (n=135) : retour [-7.83% .. +5.37%] · haut q95 +8.09% · bas q05 -9.62%
   - 6h (n=135) : retour [-7.56% .. +5.2%] · haut q95 +8.44% · bas q05 -9.41%
   - session (n=135) : retour [-6.68% .. +5.42%] · haut q95 +8.44% · bas q05 -9.68%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 5.2% des séances seulement sont des jours de hausse propre — 298040 = **volatil sans tendance propre (choppy)** (vol intra méd 3.87%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 43.5  _(momentum baissier)_
- **ADX** : 14.4  _(pas de tendance nette)_
- **MACD** : hist -39324.209  _(pas de croisement recent)_
- **BB** : %B 0.25 · largeur 49.0%
- **ATR** : 288571.43 (88.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.228  _(distribution)_
- **Vol ratio** : 0.87  _(volume normal)_
- **Choppiness** : 41.1  _(transition)_
- **MA** : MA20 3181400.0 · MA50 3550520.0 · MA200 2589134.01  _(prix < MA20)_
- **Dist MA** : MA20 -12.3% · MA50 -21.4% · MA200 +7.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (82837 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
