# 207940

**Generated** : 2026-08-14T00:18:36.999416+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩1564000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩1564000.00 (+0.6% vs entrée) · entrée ₩1555082.83 · stop ₩1485725.69 · T1 ₩1620417.89 · R/R 0.94  
> ↳ P(T1 av. stop) 44 % _(réel 5 s)_ · EV/risk -0.016 _(réel 5 s)_ (GBM -0.041) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩1546165.66–₩1564000.00 (mid ₩1555082.83)
- Spot actuel : ₩1564000.00 (+0.6% au-dessus de la zone — repli à attendre)
- Stop : ₩1485725.69 (stop swing_plan-based (-5.0%))
- Targets : T1 ₩1620417.89 · R/R 0.94 | T2 ₩1685752.95 · R/R 1.88 | T3 ₩1751088.01 · R/R 2.83
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1485725.69


## Edge, scénarios & sizing

- EV/risk : -0.041 | EV/share : ₩-2849.192 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 17 % | T3 5 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 50.1 | bear 28.1 | side 21.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.337% → cible +1.879% / stop −8.0%, p_fill 88%, n_eff≈38.5) : P(cible|rempli) **42%** · **EV/risk -0.018** (×p_fill ; si rempli -0.16% du capital)
  - **swing** (entrée dip −0.565% → cible +4.201% / stop −4.46%, p_fill 91%, n_eff≈38.8) : P(cible|rempli) **44%** · **EV/risk -0.016** (×p_fill ; si rempli -0.08% du capital)
  - **deep** (entrée dip −0.748% → cible +5.942% / stop −6.702%, p_fill 94%, n_eff≈38.5) : P(cible|rempli) **50%** · **EV/risk +0.068** (×p_fill ; si rempli +0.48% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→56% · +2.0%→40% · +3.0%→26% · +5.0%→6% · +8.0%→2%
- Range intraday médian 4.08% (p90 6.65%) · excursion haute méd. +1.09% / basse méd. −1.96%
- Profil de vol intra : ouverture 2.586% vs midi 0.753% vs clôture 0.841% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (152 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 10% · trend ↑2%/↓3% ; spike-down 57% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.134 ; mean-reverting — autocorr -0.052)_ ; drift intra méd. 0.205% ; recovery-V 40%
- **σ réalisé intraday** 3.126% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 45% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 1610525.0 (VA 1599725.0–1619975.0 ; dernier close 1606000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 15% · rebond 68% · **stop −2.28%** sous le fill (sous le bruit) · cible +1.74% · R/R 0.76 (high win-rate)
- Gaps overnight (n=151) : méd. 0.33% · baisse 31% (gap-down >1% 7% · >2% 3%)
- Excursion ouverture 5min (n=152) : bas méd −0.86% (p90 −2.52%) · haut méd +0.5% · range méd 1.51%
- Excursion ouverture 15min (n=152) : bas méd −1.08% (p90 −2.94%) · haut méd +0.68% · range méd 2.1%
- Excursion ouverture 30min (n=152) : bas méd −1.25% (p90 −3.36%) · haut méd +0.84% · range méd 2.44%
- Excursion ouverture 60min (n=152) : bas méd −1.29% (p90 −3.54%) · haut méd +0.9% · range méd 2.68%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1606000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 75% (103/151) · gap 18% · délai 1.2min · rebond 57% (48/103) (MFE +1.18%)
   - −1.0% : fill 30min 46% · séance 59% (81/151) · gap 7% · délai 2.5min · rebond 58% (37/81) (MFE +1.3%)
   - −1.5% : fill 30min 37% · séance 48% (63/151) · gap 4% · délai 3.3min · rebond 56% (30/63) (MFE +1.51%)
   - −2.0% : fill 30min 28% · séance 40% (54/151) · gap 3% · délai 6.3min · rebond 67% (30/54) (MFE +1.42%)
   - −3.0% : fill 30min 11% · séance 26% (34/151) · gap 2% · délai 62.4min · rebond 62% (19/34) (MFE +1.4%)
   - −4.0% : fill 30min 3% · séance 15% (18/151) · gap 2% · délai 73.5min · rebond 68% (11/18) (MFE +1.74%)
   - −5.0% : fill 30min 1% · séance 8% (10/151) · gap 1% · délai 175.9min · rebond 72% (7/10) (MFE +1.45%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.78% (p90 −2.24%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.88% (p90 −2.06%) → stop au-delà de −1.44% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.89% (p90 −2.13%) → stop au-delà de −1.69% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=391 jambes) : jambe baissière méd −1.1% (p90 −2.72%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (35 séances) :
      · −1.0% : fill 98% (34/35) · rebond 69% (18/34)
      · −2.0% : fill 84% (29/35) · rebond 68% (15/29)
      · −3.0% : fill 43% (15/35) · rebond 54% (8/15)
      · −4.0% : fill 31% (9/35) · rebond 76% (5/9)
      · −5.0% : fill 14% (5/35) · rebond 100% (5/5)
   - **flat** (44 séances) :
      · −1.0% : fill 54% (23/44) · rebond 31% (7/23)
      · −2.0% : fill 31% (10/44) · rebond 57% (5/10)
      · −3.0% : fill 24% (7/44) · rebond 97% (6/7)
      · −4.0% : fill 13% (4/44) · rebond 100% (4/4)
      · −5.0% : fill 6% (2/44) · rebond 89% (1/2)
   - **gap-up** (72 séances) :
      · −1.0% : fill 43% (24/72) · rebond 62% (12/24)
      · −2.0% : fill 24% (15/72) · rebond 72% (10/15)
      · −3.0% : fill 20% (12/72) · rebond 49% (5/12)
      · −4.0% : fill 9% (5/72) · rebond 33% (2/5)
      · −5.0% : fill 6% (3/72) · rebond 35% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=152) : 45% en base · 71% si les 15 1res min sont vertes (53 cas) · 28% si rouges (99 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=152) : COUDE à **33min** → P(séance verte=clôture>ouverture) 78% si début vert vs 23% si rouge (base 45% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 218min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=56) : tient le vert **78%** · continue >prix actuel 45% ; creux résiduel méd -1.26% (q20 -2.63%) → **SL/trailing à −2.63%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.49% / q75 +2.28% → **scale +1.49% / runner +2.28%**, sortie à la clôture
  - **si ROUGE au coude** (n=96) : edge inversé — récupère vert seulement **23%** (continue à baisser 51%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.44%** (au-delà de la MAE q10 -3.44%), cible rebond +1.34% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=152) : retour [-3.2% .. +3.38%] · haut q95 +3.74% · bas q05 -3.59%
   - 60min (n=152) : retour [-3.53% .. +2.76%] · haut q95 +4.14% · bas q05 -4.17%
   - 2h (n=152) : retour [-4.08% .. +3.43%] · haut q95 +4.6% · bas q05 -4.71%
   - 4h (n=152) : retour [-4.99% .. +3.81%] · haut q95 +5.09% · bas q05 -5.73%
   - 6h (n=152) : retour [-4.86% .. +4.07%] · haut q95 +5.27% · bas q05 -6.1%
   - session (n=152) : retour [-4.69% .. +3.66%] · haut q95 +5.27% · bas q05 -6.1%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 207940 = **plat / peu volatil** (vol intra méd 2.07%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 54.5  _(neutre)_
- **ADX** : 15.4  _(pas de tendance nette)_
- **MACD** : hist 7277.032  _(pas de croisement recent)_
- **BB** : %B 0.75 · largeur 20.7%
- **ATR** : 69357.14 (82.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.231  _(accumulation)_
- **Vol ratio** : 0.79  _(volume normal)_
- **Choppiness** : 55.9  _(transition)_
- **MA** : MA20 1487050.0 · MA50 1409860.0 · MA200 1605039.58  _(prix > MA20)_
- **Dist MA** : MA20 +5.2% · MA50 +10.9% · MA200 -2.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (80426 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
