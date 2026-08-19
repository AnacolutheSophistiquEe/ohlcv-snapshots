# SOFI

**Generated** : 2026-08-19T00:32:35.908527+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $17.66  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $17.66 (+5.7% vs entrée) · entrée $16.70 · stop $15.96 · T1 $17.54 · R/R 1.14  
> ↳ P(T1 av. stop) 53 % · EV/risk -0.024 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $16.53–$16.87 (mid $16.70)
- Spot actuel : $17.66 (+5.7% au-dessus de la zone — repli à attendre)
- Stop : $15.96 (stop swing_plan-based (-9.63%))
- Targets : T1 $17.54 · R/R 1.14 | T2 $18.38 · R/R 2.27 | T3 $19.22 · R/R 3.41
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $15.96


## Edge, scénarios & sizing

- EV/risk : -0.136 | EV/share : $-0.101 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 38 % | T2 18 % | T3 7 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 69.0 | bear 14.4 | side 16.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 389.0 (= 22 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.467% → cible +2.246% / stop −1.5%, p_fill 39%, n_eff≈19.2) : P(cible|rempli) **23%** · **EV/risk +0.034** (×p_fill ; si rempli +0.13% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=11, n_eff=7))
  - **deep** : indisponible (échantillon insuffisant (n=13, n_eff=8))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→69% · +2.0%→49% · +3.0%→38% · +5.0%→11% · +8.0%→1%
- Range intraday médian 4.32% (p90 7.29%) · excursion haute méd. +1.9% / basse méd. −2.18%
- Profil de vol intra : ouverture 3.004% vs midi 0.897% vs clôture 1.008% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 14% · trend ↑2%/↓0% ; spike-down 64% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.136 ; mean-reverting — autocorr -0.031)_ ; drift intra méd. 0.123% ; recovery-V 21%
- **σ réalisé intraday** 2.66% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 62% / bas 62% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 18.3813 (VA 18.3738–18.4638 ; dernier close 18.29)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 48% · rebond 71% · **stop −2.96%** sous le fill (sous le bruit) · cible +1.86% · R/R 0.63 (high win-rate)
- Gaps overnight (n=159) : méd. 0.24% · baisse 42% (gap-down >1% 24% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.65% (p90 −1.62%) · haut méd +0.7% · range méd 1.59%
- Excursion ouverture 15min (n=160) : bas méd −1.01% (p90 −2.86%) · haut méd +0.95% · range méd 2.21%
- Excursion ouverture 30min (n=160) : bas méd −1.15% (p90 −3.2%) · haut méd +1.1% · range méd 2.67%
- Excursion ouverture 60min (n=160) : bas méd −1.43% (p90 −3.75%) · haut méd +1.11% · range méd 3.29%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 18.29 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 73% (122/159) · gap 30% · délai 0.0min · rebond 51% (64/122) (MFE +1.06%)
   - −1.0% : fill 30min 53% · séance 65% (111/159) · gap 24% · délai 1.0min · rebond 60% (69/111) (MFE +1.27%)
   - −1.5% : fill 30min 44% · séance 62% (103/159) · gap 18% · délai 10.2min · rebond 69% (67/103) (MFE +1.51%)
   - −2.0% : fill 30min 35% · séance 48% (80/159) · gap 10% · délai 4.9min · rebond 71% (55/80) (MFE +1.86%)
   - −3.0% : fill 30min 16% · séance 33% (58/159) · gap 3% · délai 31.4min · rebond 66% (40/58) (MFE +1.57%)
   - −4.0% : fill 30min 9% · séance 20% (39/159) · gap 3% · délai 41.0min · rebond 57% (25/39) (MFE +1.46%)
   - −5.0% : fill 30min 4% · séance 8% (18/159) · gap 2% · délai 26.7min · rebond 40% (10/18) (MFE +0.71%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.43% (p90 −1.83%) → stop au-delà de −1.2% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.47% (p90 −1.69%) → stop au-delà de −1.25% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.42% (p90 −1.71%) → stop au-delà de −1.19% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=662 jambes) : jambe baissière méd −1.08% (p90 −2.78%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (65 séances) :
      · −1.0% : fill 97% (64/65) · rebond 62% (40/64)
      · −2.0% : fill 86% (55/65) · rebond 73% (40/55)
      · −3.0% : fill 68% (44/65) · rebond 73% (33/44)
      · −4.0% : fill 40% (29/65) · rebond 65% (21/29)
      · −5.0% : fill 20% (14/65) · rebond 38% (8/14)
   - **flat** (24 séances) :
      · −1.0% : fill 53% (14/24) · rebond 35% (6/14)
      · −2.0% : fill 42% (9/24) · rebond 69% (5/9)
      · −3.0% : fill 26% (6/24) · rebond 57% (3/6)
      · −4.0% : fill 11% (3/24) · rebond 67% (1/3)
      · −5.0% : fill 1% (1/24) · rebond 0% (0/1)
   - **gap-up** (70 séances) :
      · −1.0% : fill 45% (33/70) · rebond 68% (23/33)
      · −2.0% : fill 22% (16/70) · rebond 66% (10/16)
      · −3.0% : fill 9% (8/70) · rebond 39% (4/8)
      · −4.0% : fill 7% (7/70) · rebond 20% (3/7)
      · −5.0% : fill 1% (3/70) · rebond 70% (2/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 41% en base · 60% si les 15 1res min sont vertes (71 cas) · 27% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 80% si début vert vs 11% si rouge (base 41% · écart 69 pts) ; prédictivité sature ensuite (plafond brut 228min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=69) : tient le vert **80%** · continue >prix actuel 57% ; creux résiduel méd -1.53% (q20 -2.76%) → **SL/trailing à −2.76%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.91% / q75 +2.81% → **scale +1.91% / runner +2.81%**, sortie à la clôture
  - **si ROUGE au coude** (n=91) : edge inversé — récupère vert seulement **11%** (continue à baisser 58%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.96%** (au-delà de la MAE q10 -2.96%), cible rebond +1.38% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.83% .. +3.6%] · haut q95 +3.96% · bas q05 -3.54%
   - 60min (n=160) : retour [-3.1% .. +3.43%] · haut q95 +4.1% · bas q05 -4.0%
   - 2h (n=160) : retour [-3.58% .. +3.7%] · haut q95 +4.83% · bas q05 -4.54%
   - 4h (n=160) : retour [-3.79% .. +4.73%] · haut q95 +5.7% · bas q05 -5.02%
   - 6h (n=160) : retour [-4.37% .. +4.28%] · haut q95 +6.43% · bas q05 -5.08%
   - session (n=160) : retour [-4.31% .. +5.31%] · haut q95 +6.62% · bas q05 -5.1%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (4) pour des stats fiables : 2.5% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.91%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 68.9  _(momentum haussier)_
- **ADX** : 14.1  _(pas de tendance nette)_
- **MACD** : hist 0.043  _(pas de croisement recent)_
- **BB** : %B 0.54 · largeur 21.5%
- **ATR** : 0.74 (3.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.051  _(distribution)_
- **Vol ratio** : 0.46  _(volume atone)_
- **Choppiness** : 39.1  _(transition)_
- **MA** : MA20 17.5 · MA50 17.54 · MA200 20.69  _(prix > MA20)_
- **Dist MA** : MA20 +0.9% · MA50 +0.7% · MA200 -14.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (84005 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
