# 298040

**Generated** : 2026-07-17T00:18:01.447244+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩2789000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩2789000.00 (+1.1% vs entrée) · entrée ₩2759500.00 · stop ₩2538740.00 · T1 ₩2846194.03 · R/R 0.39  
> ↳ P(T1 av. stop) 36 % _(réel 5 s)_ · EV/risk -0.127 _(réel 5 s)_ (GBM -0.128) · ¼-Kelly 0.027 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
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

- EV/risk : -0.128 | EV/share : ₩-28228.294 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 33 % | T2 20 % | T3 20 %
- Kelly (position) : f* 0.106 | ¼-Kelly 0.027 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.5 | bear 75.9 | side 10.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.054% → cible +3.142% / stop −8.0%, p_fill 89%, n_eff≈34.9) : P(cible|rempli) **36%** · **EV/risk -0.127** (×p_fill ; si rempli -1.14% du capital)
  - **swing** (entrée dip −2.329% → cible +7.025% / stop −3.512%, p_fill 88%, n_eff≈33.8) : P(cible|rempli) **32%** · **EV/risk -0.101** (×p_fill ; si rempli -0.41% du capital)
  - **deep** (entrée dip −3.602% → cible +9.935% / stop −4.967%, p_fill 83%, n_eff≈31.0) : P(cible|rempli) **30%** · **EV/risk -0.106** (×p_fill ; si rempli -0.64% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→62% · +2.0%→51% · +3.0%→35% · +5.0%→20% · +8.0%→6%
- Range intraday médian 6.78% (p90 9.49%) · excursion haute méd. +2.1% / basse méd. −3.63%
- Profil de vol intra : ouverture 4.072% vs midi 1.055% vs clôture 1.126% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (133 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 76% · range 23% · trend ↑0%/↓1% ; spike-down 78% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.132 ; mean-reverting — autocorr -0.052)_ ; drift intra méd. -1.616% ; recovery-V 33%
- **σ réalisé intraday** 4.985% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 68% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 2829250.0 (VA 2790750.0–2846750.0 ; dernier close 2857000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 33% · rebond 92% · **stop −5.49%** sous le fill (sous le bruit) · cible +2.33% · R/R 0.42 (high win-rate)
- Gaps overnight (n=132) : méd. 0.7% · baisse 37% (gap-down >1% 23% · >2% 15%)
- Excursion ouverture 5min (n=133) : bas méd −1.28% (p90 −3.43%) · haut méd +0.78% · range méd 2.6%
- Excursion ouverture 15min (n=133) : bas méd −1.95% (p90 −4.79%) · haut méd +0.98% · range méd 3.47%
- Excursion ouverture 30min (n=133) : bas méd −2.46% (p90 −5.01%) · haut méd +1.1% · range méd 4.04%
- Excursion ouverture 60min (n=133) : bas méd −2.58% (p90 −5.32%) · haut méd +1.22% · range méd 4.72%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2857000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 70% (90/132) · gap 31% · délai 0.1min · rebond 58% (55/90) (MFE +1.28%)
   - −1.0% : fill 30min 56% · séance 67% (82/132) · gap 23% · délai 0.9min · rebond 57% (50/82) (MFE +1.44%)
   - −1.5% : fill 30min 46% · séance 58% (73/132) · gap 19% · délai 1.3min · rebond 51% (44/73) (MFE +1.17%)
   - −2.0% : fill 30min 41% · séance 54% (64/132) · gap 15% · délai 3.1min · rebond 49% (34/64) (MFE +0.98%)
   - −3.0% : fill 30min 30% · séance 45% (52/132) · gap 8% · délai 6.8min · rebond 54% (29/52) (MFE +1.03%)
   - −4.0% : fill 30min 21% · séance 40% (44/132) · gap 5% · délai 26.3min · rebond 72% (33/44) (MFE +1.66%)
   - −5.0% : fill 30min 18% · séance 33% (33/132) · gap 4% · délai 23.1min · rebond 92% (28/33) (MFE +2.33%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.72% (p90 −3.41%) → stop au-delà de −2.42% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −3.77%) → stop au-delà de −2.47% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.72% (p90 −4.05%) → stop au-delà de −2.13% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=690 jambes) : jambe baissière méd −1.43% (p90 −3.48%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (45 séances) :
      · −1.0% : fill 100% (45/45) · rebond 58% (28/45)
      · −2.0% : fill 85% (37/45) · rebond 51% (20/37)
      · −3.0% : fill 80% (35/45) · rebond 52% (19/35)
      · −4.0% : fill 75% (30/45) · rebond 75% (22/30)
      · −5.0% : fill 66% (25/45) · rebond 88% (20/25)
   - **flat** (15 séances) :
      · −1.0% : fill 82% (10/15) · rebond 57% (7/10)
      · −2.0% : fill 72% (7/15) · rebond 73% (5/7)
      · −3.0% : fill 43% (4/15) · rebond 100% (4/4)
      · −4.0% : fill 43% (4/15) · rebond 63% (3/4)
      · −5.0% : fill 31% (2/15) · rebond 100% (2/2)
   - **gap-up** (72 séances) :
      · −1.0% : fill 43% (27/72) · rebond 56% (15/27)
      · −2.0% : fill 32% (20/72) · rebond 35% (9/20)
      · −3.0% : fill 24% (13/72) · rebond 43% (6/13)
      · −4.0% : fill 18% (10/72) · rebond 71% (8/10)
      · −5.0% : fill 12% (6/72) · rebond 100% (6/6)
- **P(clôture VERTE) selon le drive 15min** (n=133) : 40% en base · 70% si les 15 1res min sont vertes (53 cas) · 27% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=133) : COUDE à **1:21** → P(séance verte=clôture>ouverture) 81% si début vert vs 13% si rouge (base 40% · écart 68 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=61) : tient le vert **81%** · continue >prix actuel 52% ; creux résiduel méd -1.5% (q20 -3.91%) → **SL/trailing à −3.91%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.55% / q75 +2.9% → **scale +1.55% / runner +2.9%**, sortie à la clôture
  - **si ROUGE au coude** (n=72) : edge inversé — récupère vert seulement **13%** (continue à baisser 63%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.27%** (au-delà de la MAE q10 -6.27%), cible rebond +1.31% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=133) : retour [-4.58% .. +4.31%] · haut q95 +5.83% · bas q05 -5.24%
   - 60min (n=133) : retour [-5.39% .. +4.96%] · haut q95 +6.76% · bas q05 -5.99%
   - 2h (n=133) : retour [-7.4% .. +4.55%] · haut q95 +7.32% · bas q05 -8.24%
   - 4h (n=133) : retour [-7.97% .. +5.39%] · haut q95 +8.24% · bas q05 -9.75%
   - 6h (n=133) : retour [-7.59% .. +5.24%] · haut q95 +8.59% · bas q05 -9.6%
   - session (n=133) : retour [-6.73% .. +5.44%] · haut q95 +8.59% · bas q05 -9.78%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 5.3% des séances seulement sont des jours de hausse propre — 298040 = **volatil sans tendance propre (choppy)** (vol intra méd 3.83%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)


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

_Bulletin compact généré depuis `<TICKER>_report_data.json` (82859 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
