# SAF

**Generated** : 2026-07-03T21:41:41.433530+00:00  
**Santé technique** : 9/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €356.70  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €356.70 (+1.8% vs entrée) · entrée €350.52 · stop €346.75 · T1 €358.06 · R/R 2.0  
> ↳ P(T1 av. stop) 22 % _(réel 5 s)_ · EV/risk -0.17 _(réel 5 s)_ (GBM 0.15) · ¼-Kelly 0.011 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 1416 % hors [0,100] (R² max 0.87). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : triple_bullish (score 3)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 9/10 élevée alors que : RSI 78.5 > 70 (surachat) ; extension extrême (≥3×ATR, confluence MA20/50) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €349.01–€352.03 (mid €350.52)
- Spot actuel : €356.70 (+1.8% au-dessus de la zone — repli à attendre)
- Stop : €346.75 (stop swing_plan-based (-2.79%))
- Targets : T1 €358.06 · R/R 2.0 | T2 €365.61 · R/R 4.0 | T3 €373.15 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €346.75


## Edge, scénarios & sizing

- EV/risk : 0.15 | EV/share : €0.567 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 21 % | T3 12 %
- Kelly (position) : f* 0.043 | ¼-Kelly 0.011 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 37.6 | side 57.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 357.0 (= 1 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.792% → cible +0.962% / stop −1.5%, p_fill 38%, n_eff≈21.4) : P(cible|rempli) **47%** · **EV/risk -0.047** (×p_fill ; si rempli -0.19% du capital)
  - **swing** (entrée dip −1.733% → cible +2.151% / stop −1.076%, p_fill 39%, n_eff≈18.4) : P(cible|rempli) **22%** · **EV/risk -0.170** (×p_fill ; si rempli -0.47% du capital)
  - **deep** (entrée dip −2.679% → cible +3.043% / stop −1.521%, p_fill 34%, n_eff≈21.3) : P(cible|rempli) **35%** · **EV/risk -0.007** (×p_fill ; si rempli -0.03% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→62% · +2.0%→39% · +3.0%→16% · +5.0%→5% · +8.0%→2%
- Range intraday médian 2.77% (p90 4.93%) · excursion haute méd. +1.52% / basse méd. −1.01%
- Profil de vol intra : ouverture 1.661% vs midi 0.66% vs clôture 0.783% _(ouverture ~2.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (141 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 17% · trend ↑0%/↓0% ; spike-down 33% · recovery-V 19%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; mean-reverting — autocorr -0.038)_ ; drift intra méd. 0.67% ; recovery-V 27%
- **σ réalisé intraday** 1.869% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 74% / bas 39% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 353.1687 (VA 350.2937–355.4688 ; dernier close 354.65)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 19% · rebond 59% · **stop −1.6%** sous le fill (sous le bruit) · cible +1.23% · R/R 0.77 (high win-rate)
- Gaps overnight (n=140) : méd. -0.11% · baisse 54% (gap-down >1% 14% · >2% 2%)
- Excursion ouverture 5min (n=141) : bas méd −0.36% (p90 −1.42%) · haut méd +0.28% · range méd 0.92%
- Excursion ouverture 15min (n=141) : bas méd −0.38% (p90 −1.6%) · haut méd +0.48% · range méd 1.19%
- Excursion ouverture 30min (n=141) : bas méd −0.46% (p90 −1.69%) · haut méd +0.58% · range méd 1.29%
- Excursion ouverture 60min (n=141) : bas méd −0.67% (p90 −1.92%) · haut méd +0.7% · range méd 1.52%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 354.65 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 66% (99/140) · gap 29% · délai 0.2min · rebond 39% (37/99) (MFE +0.82%)
   - −1.0% : fill 30min 41% · séance 50% (71/140) · gap 14% · délai 0.4min · rebond 44% (26/71) (MFE +0.62%)
   - −1.5% : fill 30min 27% · séance 41% (60/140) · gap 5% · délai 6.9min · rebond 38% (20/60) (MFE +0.89%)
   - −2.0% : fill 30min 13% · séance 31% (43/140) · gap 2% · délai 39.0min · rebond 48% (19/43) (MFE +0.91%)
   - −3.0% : fill 30min 5% · séance 19% (26/140) · gap 1% · délai 203.0min · rebond 59% (16/26) (MFE +1.23%)
   - −4.0% : fill 30min 3% · séance 9% (12/140) · gap 0% · délai 153.7min · rebond 53% (6/12) (MFE +1.49%)
   - −5.0% : fill 30min 0% · séance 2% (3/140) · gap 0% · délai 360.2min · rebond 31% (1/3) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.19% (p90 −0.92%) → stop au-delà de −0.76% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −0.91%) → stop au-delà de −0.69% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=166 jambes) : jambe baissière méd −1.05% (p90 −2.72%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 77% (39/50) · rebond 43% (15/39)
      · −2.0% : fill 53% (27/50) · rebond 51% (13/27)
      · −3.0% : fill 33% (16/50) · rebond 58% (9/16)
      · −4.0% : fill 15% (8/50) · rebond 59% (4/8)
      · −5.0% : fill 3% (2/50) · rebond 0% (0/2)
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
- **P(clôture VERTE) selon le drive 15min** (n=141) : 54% en base · 69% si les 15 1res min sont vertes (64 cas) · 36% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=141) : COUDE à **44min** → P(séance verte=clôture>ouverture) 80% si début vert vs 24% si rouge (base 54% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=65) : tient le vert **80%** · continue >prix actuel 65% ; creux résiduel méd -0.54% (q20 -1.42%) → **SL/trailing à −1.42%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.32% / q75 +1.91% → **scale +1.32% / runner +1.91%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **24%** (continue à baisser 47%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.5%** (au-delà de la MAE q10 -2.5%), cible rebond +0.92% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=141) : retour [-1.8% .. +1.75%] · haut q95 +2.18% · bas q05 -2.28%
   - 60min (n=141) : retour [-1.81% .. +2.35%] · haut q95 +2.98% · bas q05 -2.54%
   - 2h (n=141) : retour [-2.16% .. +2.31%] · haut q95 +3.38% · bas q05 -2.91%
   - 4h (n=141) : retour [-2.16% .. +2.56%] · haut q95 +3.46% · bas q05 -3.01%
   - 6h (n=141) : retour [-2.18% .. +3.43%] · haut q95 +3.67% · bas q05 -3.08%
   - session (n=141) : retour [-2.87% .. +3.64%] · haut q95 +4.08% · bas q05 -4.04%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 2.1% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.66%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
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

- **RSI** : 78.5  _(surachat)_
- **ADX** : 33.3  _(tendance etablie)_
- **MACD** : hist 1.998  _(pas de croisement recent)_
- **BB** : %B 0.87 · largeur 25.0%
- **ATR** : 8.19 (60.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.124  _(accumulation)_
- **Vol ratio** : 0.68  _(volume normal)_
- **Choppiness** : 39.4  _(transition)_
- **MA** : MA20 326.44 · MA50 300.49 · MA200 301.33  _(prix > MA20)_
- **Dist MA** : MA20 +9.3% · MA50 +18.7% · MA200 +18.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93993 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
