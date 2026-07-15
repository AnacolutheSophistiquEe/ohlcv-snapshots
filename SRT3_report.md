# SRT3

**Generated** : 2026-07-15T00:03:17.469952+00:00  
**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €250.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot €250.00 (+7.3% vs entrée) · entrée €232.94 · stop €228.74 · T1 €241.32 · R/R 2.0  
> ↳ P(T1 av. stop) 34 % · EV/risk -0.007 · ¼-Kelly 0.002 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : RSI 70.0 > 70 (surachat) ; %B 1.02 (collé à la bande haute) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €231.26–€234.61 (mid €232.94)
- Spot actuel : €250.00 (+7.3% au-dessus de la zone — repli à attendre)
- Stop : €228.74 (stop swing_plan-based (-8.5%))
- Targets : T1 €241.32 · R/R 2.0 | T2 €249.71 · R/R 3.99 | T3 €258.09 · R/R 5.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €228.74


## Edge, scénarios & sizing

- EV/risk : -0.007 | EV/share : €-0.029 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 15 % | T3 5 %
- Kelly (position) : f* 0.008 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 27.2 | bear 9.5 | side 63.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 500.0 (= 2 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=12, n_eff=5))
  - **swing** : indisponible (échantillon insuffisant (n=4, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=5, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→75% · +2.0%→48% · +3.0%→26% · +5.0%→11% · +8.0%→0%
- Range intraday médian 3.63% (p90 6.82%) · excursion haute méd. +1.96% / basse méd. −1.75%
- Profil de vol intra : ouverture 2.047% vs midi 0.883% vs clôture 0.992% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑1%/↓0% ; spike-down 52% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.13 ; neutre — autocorr 0.03)_ ; drift intra méd. 0.372% ; recovery-V 25%
- **σ réalisé intraday** 2.437% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 63% / bas 58% / whipsaw 27%
- POC intraday (dernière séance, temps-au-prix) : 241.4437 (VA 241.0812–243.9812 ; dernier close 241.9)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 57% · rebond 65% · **stop −2.5%** sous le fill (sous le bruit) · cible +1.56% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. -0.04% · baisse 51% (gap-down >1% 18% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.27% (p90 −1.68%) · haut méd +0.59% · range méd 1.24%
- Excursion ouverture 15min (n=160) : bas méd −0.51% (p90 −1.86%) · haut méd +0.68% · range méd 1.57%
- Excursion ouverture 30min (n=160) : bas méd −0.53% (p90 −1.98%) · haut méd +0.95% · range méd 1.75%
- Excursion ouverture 60min (n=160) : bas méd −0.64% (p90 −2.25%) · haut méd +1.03% · range méd 1.93%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 241.9 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 55% · séance 75% (124/159) · gap 29% · délai 0.2min · rebond 53% (58/124) (MFE +1.11%)
   - −1.0% : fill 30min 43% · séance 63% (105/159) · gap 18% · délai 0.7min · rebond 57% (59/105) (MFE +1.2%)
   - −1.5% : fill 30min 31% · séance 57% (92/159) · gap 10% · délai 14.9min · rebond 65% (55/92) (MFE +1.56%)
   - −2.0% : fill 30min 20% · séance 41% (70/159) · gap 6% · délai 33.7min · rebond 56% (43/70) (MFE +1.26%)
   - −3.0% : fill 30min 6% · séance 21% (40/159) · gap 2% · délai 184.1min · rebond 54% (24/40) (MFE +1.51%)
   - −4.0% : fill 30min 4% · séance 11% (20/159) · gap 1% · délai 208.7min · rebond 67% (15/20) (MFE +1.31%)
   - −5.0% : fill 30min 1% · séance 7% (10/159) · gap 1% · délai 99.8min · rebond 74% (8/10) (MFE +2.47%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.14% (p90 −1.75%) → stop au-delà de −0.89% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −1.83%) → stop au-delà de −0.89% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.12% (p90 −1.84%) → stop au-delà de −1.08% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=412 jambes) : jambe baissière méd −1.05% (p90 −2.37%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (76 séances) :
      · −1.0% : fill 82% (63/76) · rebond 69% (40/63)
      · −2.0% : fill 56% (42/76) · rebond 65% (28/42)
      · −3.0% : fill 36% (29/76) · rebond 56% (17/29)
      · −4.0% : fill 19% (16/76) · rebond 71% (12/16)
      · −5.0% : fill 10% (7/76) · rebond 92% (6/7)
   - **flat** (35 séances) :
      · −1.0% : fill 62% (21/35) · rebond 35% (9/21)
      · −2.0% : fill 48% (15/35) · rebond 38% (7/15)
      · −3.0% : fill 18% (6/35) · rebond 49% (4/6)
      · −4.0% : fill 11% (3/35) · rebond 44% (2/3)
      · −5.0% : fill 11% (3/35) · rebond 44% (2/3)
   - **gap-up** (48 séances) :
      · −1.0% : fill 41% (21/48) · rebond 52% (10/21)
      · −2.0% : fill 21% (13/48) · rebond 55% (8/13)
      · −3.0% : fill 5% (5/48) · rebond 52% (3/5)
      · −4.0% : fill 1% (1/48) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/48) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 54% en base · 64% si les 15 1res min sont vertes (91 cas) · 40% si rouges (69 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:17** → P(séance verte=clôture>ouverture) 79% si début vert vs 28% si rouge (base 54% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 292min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **79%** · continue >prix actuel 53% ; creux résiduel méd -0.99% (q20 -2.2%) → **SL/trailing à −2.2%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.18% / q75 +2.19% → **scale +1.18% / runner +2.19%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **28%** (continue à baisser 52%) → **RÉDUIRE ~72%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.04%** (au-delà de la MAE q10 -3.04%), cible rebond +1.26% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.1% .. +2.18%] · haut q95 +2.72% · bas q05 -2.76%
   - 60min (n=160) : retour [-2.42% .. +2.42%] · haut q95 +2.89% · bas q05 -3.04%
   - 2h (n=160) : retour [-2.24% .. +2.84%] · haut q95 +3.25% · bas q05 -3.16%
   - 4h (n=160) : retour [-2.6% .. +2.86%] · haut q95 +3.44% · bas q05 -3.51%
   - 6h (n=160) : retour [-2.68% .. +3.61%] · haut q95 +4.57% · bas q05 -3.82%
   - session (n=160) : retour [-3.72% .. +5.11%] · haut q95 +6.39% · bas q05 -4.33%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.25%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : stretched_up
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

- **RSI** : 70.0  _(surachat)_
- **ADX** : 13.7  _(pas de tendance nette)_
- **MACD** : hist 2.789  _(pas de croisement recent)_
- **BB** : %B 1.02 · largeur 18.8%
- **ATR** : 9.59 (80.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.067  _(accumulation)_
- **Vol ratio** : 0.27  _(volume atone)_
- **Choppiness** : 50.8  _(transition)_
- **MA** : MA20 227.78 · MA50 228.91 · MA200 230.81  _(prix > MA20)_
- **Dist MA** : MA20 +9.8% · MA50 +9.2% · MA200 +8.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91430 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
