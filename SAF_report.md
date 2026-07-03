# SAF

**Generated** : 2026-07-03T00:07:36.447373+00:00  
**Santé technique** : 9/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €354.70  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €354.70 (+1.5% vs entrée) · entrée €349.62 · stop €345.79 · T1 €357.30 · R/R 2.01  
> ↳ P(T1 av. stop) 32 % _(réel 5 s)_ · EV/risk -0.056 _(réel 5 s)_ (GBM 0.141) · ¼-Kelly 0.009 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 1195 % hors [0,100] (R² max 0.87). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : triple_bullish (score 3)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 9/10 élevée alors que : RSI 80.8 > 70 (surachat) ; extension extrême (≥3×ATR, confluence MA20/50) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €348.09–€351.16 (mid €349.62)
- Spot actuel : €354.70 (+1.5% au-dessus de la zone — repli à attendre)
- Stop : €345.79 (stop swing_plan-based (-2.51%))
- Targets : T1 €357.30 · R/R 2.01 | T2 €364.97 · R/R 4.01 | T3 €372.64 · R/R 6.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €345.79


## Edge, scénarios & sizing

- EV/risk : 0.141 | EV/share : €0.539 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 20 % | T3 12 %
- Kelly (position) : f* 0.038 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 43.0 | side 52.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 355.0 (= 1 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.65% → cible +0.981% / stop −1.5%, p_fill 57%, n_eff≈26.0) : P(cible|rempli) **55%** · **EV/risk +0.043** (×p_fill ; si rempli +0.11% du capital)
  - **swing** (entrée dip −1.428% → cible +2.195% / stop −1.097%, p_fill 40%, n_eff≈21.4) : P(cible|rempli) **32%** · **EV/risk -0.056** (×p_fill ; si rempli -0.15% du capital)
  - **deep** (entrée dip −2.213% → cible +3.104% / stop −1.552%, p_fill 37%, n_eff≈22.2) : P(cible|rempli) **31%** · **EV/risk -0.049** (×p_fill ; si rempli -0.20% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→62% · +2.0%→38% · +3.0%→15% · +5.0%→5% · +8.0%→2%
- Range intraday médian 2.77% (p90 5.22%) · excursion haute méd. +1.34% / basse méd. −1.04%
- Profil de vol intra : ouverture 1.664% vs midi 0.665% vs clôture 0.787% _(ouverture ~2.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (140 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 34% · recovery-V 19%)_
- **Régime intraday** : **chop** _(efficiency 0.115 ; mean-reverting — autocorr -0.037)_ ; drift intra méd. 0.591% ; recovery-V 27%
- **σ réalisé intraday** 1.906% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 72% / bas 41% / whipsaw 13%
- POC intraday (dernière séance, temps-au-prix) : 349.8875 (VA 348.3125–350.5875 ; dernier close 350.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 20% · rebond 59% · **stop −1.6%** sous le fill (sous le bruit) · cible +1.23% · R/R 0.77 (high win-rate)
- Gaps overnight (n=139) : méd. -0.07% · baisse 53% (gap-down >1% 14% · >2% 2%)
- Excursion ouverture 5min (n=140) : bas méd −0.36% (p90 −1.43%) · haut méd +0.27% · range méd 0.92%
- Excursion ouverture 15min (n=140) : bas méd −0.4% (p90 −1.61%) · haut méd +0.46% · range méd 1.2%
- Excursion ouverture 30min (n=140) : bas méd −0.48% (p90 −1.76%) · haut méd +0.58% · range méd 1.3%
- Excursion ouverture 60min (n=140) : bas méd −0.68% (p90 −1.94%) · haut méd +0.69% · range méd 1.55%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 350.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 55% · séance 66% (98/139) · gap 28% · délai 0.2min · rebond 38% (36/98) (MFE +0.78%)
   - −1.0% : fill 30min 40% · séance 49% (70/139) · gap 14% · délai 0.4min · rebond 42% (25/70) (MFE +0.58%)
   - −1.5% : fill 30min 28% · séance 42% (60/139) · gap 5% · délai 6.9min · rebond 38% (20/60) (MFE +0.89%)
   - −2.0% : fill 30min 14% · séance 31% (43/139) · gap 2% · délai 39.0min · rebond 48% (19/43) (MFE +0.91%)
   - −3.0% : fill 30min 5% · séance 20% (26/139) · gap 1% · délai 203.0min · rebond 59% (16/26) (MFE +1.23%)
   - −4.0% : fill 30min 3% · séance 9% (12/139) · gap 0% · délai 153.7min · rebond 53% (6/12) (MFE +1.49%)
   - −5.0% : fill 30min 0% · séance 2% (3/139) · gap 0% · délai 360.2min · rebond 31% (1/3) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.23% (p90 −0.93%) → stop au-delà de −0.77% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.17% (p90 −0.91%) → stop au-delà de −0.7% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.15% (p90 −1.02%) → stop au-delà de −0.88% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=166 jambes) : jambe baissière méd −1.05% (p90 −2.72%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 76% (38/49) · rebond 39% (14/38)
      · −2.0% : fill 56% (27/49) · rebond 51% (13/27)
      · −3.0% : fill 35% (16/49) · rebond 58% (9/16)
      · −4.0% : fill 16% (8/49) · rebond 59% (4/8)
      · −5.0% : fill 3% (2/49) · rebond 0% (0/2)
   - **flat** (38 séances) :
      · −1.0% : fill 45% (16/38) · rebond 62% (8/16)
      · −2.0% : fill 19% (7/38) · rebond 50% (3/7)
      · −3.0% : fill 10% (4/38) · rebond 69% (3/4)
      · −4.0% : fill 2% (1/38) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/38) · rebond 0% (0/0)
   - **gap-up** (52 séances) :
      · −1.0% : fill 23% (16/52) · rebond 26% (3/16)
      · −2.0% : fill 14% (9/52) · rebond 34% (3/9)
      · −3.0% : fill 11% (6/52) · rebond 55% (4/6)
      · −4.0% : fill 7% (3/52) · rebond 30% (1/3)
      · −5.0% : fill 2% (1/52) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=140) : 53% en base · 68% si les 15 1res min sont vertes (63 cas) · 36% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=140) : COUDE à **44min** → P(séance verte=clôture>ouverture) 80% si début vert vs 24% si rouge (base 53% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=64) : tient le vert **80%** · continue >prix actuel 64% ; creux résiduel méd -0.56% (q20 -1.43%) → **SL/trailing à −1.43%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.29% / q75 +1.78% → **scale +1.29% / runner +1.78%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **24%** (continue à baisser 47%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.5%** (au-delà de la MAE q10 -2.5%), cible rebond +0.92% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=140) : retour [-1.8% .. +1.77%] · haut q95 +2.37% · bas q05 -2.28%
   - 60min (n=140) : retour [-1.82% .. +2.37%] · haut q95 +3.03% · bas q05 -2.57%
   - 2h (n=140) : retour [-2.18% .. +2.33%] · haut q95 +3.38% · bas q05 -2.92%
   - 4h (n=140) : retour [-2.16% .. +2.63%] · haut q95 +3.47% · bas q05 -3.02%
   - 6h (n=140) : retour [-2.2% .. +3.45%] · haut q95 +3.7% · bas q05 -3.09%
   - session (n=140) : retour [-2.9% .. +3.65%] · haut q95 +4.11% · bas q05 -4.05%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.4% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.67%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : extreme
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

- **RSI** : 80.8  _(surachat)_
- **ADX** : 31.8  _(tendance etablie)_
- **MACD** : hist 2.019  _(pas de croisement recent)_
- **BB** : %B 0.89 · largeur 24.9%
- **ATR** : 8.98 (65.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.095  _(accumulation)_
- **Vol ratio** : 0.29  _(volume atone)_
- **Choppiness** : 41.0  _(transition)_
- **MA** : MA20 323.6 · MA50 298.9 · MA200 300.97  _(prix > MA20)_
- **Dist MA** : MA20 +9.6% · MA50 +18.7% · MA200 +17.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93621 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
