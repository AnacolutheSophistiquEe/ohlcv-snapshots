# SAF

**Generated** : 2026-07-10T21:42:10.584925+00:00  
**Santé technique** : 8/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €336.10  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)  
> ↳ spot €336.10 (+8.0% vs entrée) · entrée €311.26 · stop €307.23 · T1 €319.30 · R/R 2.0  
> ↳ P(T1 av. stop) 35 % · EV/risk 0.129 · ¼-Kelly 0.006 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 127 % hors [0,100] (R² max 0.68). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €309.65–€312.87 (mid €311.26)
- Spot actuel : €336.10 (+8.0% au-dessus de la zone — repli à attendre)
- Stop : €307.23 (stop swing_plan-based (-8.59%))
- Targets : T1 €319.30 · R/R 2.0 | T2 €327.35 · R/R 3.99 | T3 €335.39 · R/R 5.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €307.23


## Edge, scénarios & sizing

- EV/risk : 0.129 | EV/share : €0.519 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 16 % | T3 10 %
- Kelly (position) : f* 0.026 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 10.8 | side 84.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 336.0 (= 1 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=9, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→72% · +1.0%→59% · +2.0%→39% · +3.0%→16% · +5.0%→5% · +8.0%→2%
- Range intraday médian 2.8% (p90 4.93%) · excursion haute méd. +1.52% / basse méd. −0.95%
- Profil de vol intra : ouverture 1.652% vs midi 0.649% vs clôture 0.764% _(ouverture ~2.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (145 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 20% · trend ↑0%/↓0% ; spike-down 35% · recovery-V 17%)_
- **Régime intraday** : **chop** _(efficiency 0.129 ; mean-reverting — autocorr -0.038)_ ; drift intra méd. 0.271% ; recovery-V 20%
- **σ réalisé intraday** 1.827% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 49% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 332.5425 (VA 332.1975–335.9925 ; dernier close 331.9)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 22% · rebond 49% · **stop −1.79%** sous le fill (sous le bruit) · cible +0.95% · R/R 0.53 (high win-rate)
- Gaps overnight (n=144) : méd. -0.06% · baisse 52% (gap-down >1% 13% · >2% 2%)
- Excursion ouverture 5min (n=145) : bas méd −0.36% (p90 −1.59%) · haut méd +0.27% · range méd 0.92%
- Excursion ouverture 15min (n=145) : bas méd −0.38% (p90 −1.84%) · haut méd +0.48% · range méd 1.19%
- Excursion ouverture 30min (n=145) : bas méd −0.46% (p90 −1.92%) · haut méd +0.57% · range méd 1.29%
- Excursion ouverture 60min (n=145) : bas méd −0.67% (p90 −1.92%) · haut méd +0.69% · range méd 1.52%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 331.9 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 65% (101/144) · gap 29% · délai 0.2min · rebond 37% (37/101) (MFE +0.72%)
   - −1.0% : fill 30min 42% · séance 50% (73/144) · gap 13% · délai 0.4min · rebond 41% (26/73) (MFE +0.6%)
   - −1.5% : fill 30min 27% · séance 42% (62/144) · gap 5% · délai 6.9min · rebond 35% (20/62) (MFE +0.87%)
   - −2.0% : fill 30min 14% · séance 32% (45/144) · gap 2% · délai 38.8min · rebond 42% (19/45) (MFE +0.77%)
   - −3.0% : fill 30min 4% · séance 22% (28/144) · gap 1% · délai 202.9min · rebond 49% (16/28) (MFE +0.95%)
   - −4.0% : fill 30min 2% · séance 10% (13/144) · gap 0% · délai 126.9min · rebond 62% (7/13) (MFE +1.25%)
   - −5.0% : fill 30min 0% · séance 2% (3/144) · gap 0% · délai 360.2min · rebond 31% (1/3) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.19% (p90 −0.92%) → stop au-delà de −0.76% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −0.91%) → stop au-delà de −0.69% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=171 jambes) : jambe baissière méd −1.07% (p90 −2.69%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (51 séances) :
      · −1.0% : fill 78% (40/51) · rebond 40% (15/40)
      · −2.0% : fill 55% (28/51) · rebond 47% (13/28)
      · −3.0% : fill 37% (17/51) · rebond 50% (9/17)
      · −4.0% : fill 19% (9/51) · rebond 69% (5/9)
      · −5.0% : fill 3% (2/51) · rebond 0% (0/2)
   - **flat** (40 séances) :
      · −1.0% : fill 39% (16/40) · rebond 62% (8/16)
      · −2.0% : fill 17% (7/40) · rebond 50% (3/7)
      · −3.0% : fill 8% (4/40) · rebond 69% (3/4)
      · −4.0% : fill 2% (1/40) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/40) · rebond 0% (0/0)
   - **gap-up** (53 séances) :
      · −1.0% : fill 27% (17/53) · rebond 21% (3/17)
      · −2.0% : fill 19% (10/53) · rebond 24% (3/10)
      · −3.0% : fill 15% (7/53) · rebond 36% (4/7)
      · −4.0% : fill 7% (3/53) · rebond 30% (1/3)
      · −5.0% : fill 1% (1/53) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=145) : 54% en base · 72% si les 15 1res min sont vertes (66 cas) · 33% si rouges (79 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=145) : COUDE à **44min** → P(séance verte=clôture>ouverture) 81% si début vert vs 25% si rouge (base 54% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=66) : tient le vert **81%** · continue >prix actuel 63% ; creux résiduel méd -0.56% (q20 -1.41%) → **SL/trailing à −1.41%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.29% / q75 +1.83% → **scale +1.29% / runner +1.83%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **25%** (continue à baisser 49%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.78%** (au-delà de la MAE q10 -2.78%), cible rebond +0.86% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=145) : retour [-1.68% .. +1.61%] · haut q95 +1.98% · bas q05 -2.27%
   - 60min (n=145) : retour [-1.74% .. +2.24%] · haut q95 +2.8% · bas q05 -2.45%
   - 2h (n=145) : retour [-2.49% .. +2.24%] · haut q95 +3.32% · bas q05 -3.0%
   - 4h (n=145) : retour [-2.49% .. +2.33%] · haut q95 +3.42% · bas q05 -3.35%
   - 6h (n=145) : retour [-2.37% .. +3.28%] · haut q95 +3.58% · bas q05 -3.66%
   - session (n=145) : retour [-3.51% .. +3.55%] · haut q95 +3.94% · bas q05 -4.02%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 2.1% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.66%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 52.9  _(neutre)_
- **ADX** : 28.9  _(tendance etablie)_
- **MACD** : hist -2.169  _(bearish_recent)_
- **BB** : %B 0.46 · largeur 13.2%
- **ATR** : 9.04 (66.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.096  _(accumulation)_
- **Vol ratio** : 0.47  _(volume atone)_
- **Choppiness** : 49.5  _(transition)_
- **MA** : MA20 337.94 · MA50 307.91 · MA200 302.67  _(prix < MA20)_
- **Dist MA** : MA20 -0.5% · MA50 +9.2% · MA200 +11.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88361 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
