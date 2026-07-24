# RGTI

**Generated** : 2026-07-24T22:02:50.260272+00:00  
**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $14.15  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $14.15 (+3.0% vs entrée) · entrée $13.74 · stop $13.41 · T1 $14.41 · R/R 2.03  
> ↳ P(T1 av. stop) 7 % _(réel 5 s)_ · EV/risk -0.3 _(réel 5 s)_ (GBM 0.214) · ¼-Kelly 0.023 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.41% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -108 % hors [0,100] (R² max 0.43). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $13.68–$13.81 (mid $13.74)
- Spot actuel : $14.15 (+3.0% au-dessus de la zone — repli à attendre)
- Stop : $13.41 (stop swing_plan-based (-8.78%))
- Targets : T1 $14.41 · R/R 2.03 | T2 $14.56 · R/R 2.48 | T3 $14.72 · R/R 2.97
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $13.41


## Edge, scénarios & sizing

- EV/risk : 0.214 | EV/share : $0.071 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 32 % | T2 31 % | T3 31 %
- Kelly (position) : f* 0.09 | ¼-Kelly 0.023 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 17.7 | side 77.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.857% → cible +4.823% / stop −2.412%, p_fill 47%, n_eff≈21.8) : P(cible|rempli) **7%** · **EV/risk -0.300** (×p_fill ; si rempli -1.55% du capital)
  - **swing** (entrée dip −6.301% → cible +5.292% / stop −2.646%, p_fill 51%, n_eff≈19.2) : P(cible|rempli) **33%** · **EV/risk -0.029** (×p_fill ; si rempli -0.15% du capital)
  - **deep** (entrée dip −9.733% → cible +7.483% / stop −3.741%, p_fill 44%, n_eff≈17.4) : P(cible|rempli) **20%** · **EV/risk -0.164** (×p_fill ; si rempli -1.41% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→81% · +2.0%→72% · +3.0%→56% · +5.0%→38% · +8.0%→16%
- Range intraday médian 8.12% (p90 13.36%) · excursion haute méd. +3.49% / basse méd. −2.82%
- Profil de vol intra : ouverture 5.317% vs midi 1.669% vs clôture 1.87% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 19% · trend ↑0%/↓0% ; spike-down 76% · recovery-V 43%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; neutre — autocorr -0.018)_ ; drift intra méd. -0.318% ; recovery-V 39%
- **σ réalisé intraday** 4.871% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 51% / bas 55% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 15.2106 (VA 15.1987–15.4369 ; dernier close 15.24)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 61% · rebond 74% · **stop −7.09%** sous le fill (sous le bruit) · cible +2.55% · R/R 0.36 (high win-rate)
- Gaps overnight (n=159) : méd. -0.53% · baisse 56% (gap-down >1% 45% · >2% 30%)
- Excursion ouverture 5min (n=160) : bas méd −1.23% (p90 −2.85%) · haut méd +1.14% · range méd 2.56%
- Excursion ouverture 15min (n=160) : bas méd −1.52% (p90 −4.15%) · haut méd +1.54% · range méd 3.49%
- Excursion ouverture 30min (n=160) : bas méd −1.8% (p90 −5.37%) · haut méd +1.94% · range méd 4.57%
- Excursion ouverture 60min (n=160) : bas méd −2.07% (p90 −6.36%) · haut méd +2.23% · range méd 5.4%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 15.24 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 76% · séance 83% (135/159) · gap 51% · délai 0.0min · rebond 66% (88/135) (MFE +2.28%)
   - −1.0% : fill 30min 70% · séance 81% (131/159) · gap 45% · délai 0.0min · rebond 66% (85/131) (MFE +2.06%)
   - −1.5% : fill 30min 64% · séance 76% (123/159) · gap 40% · délai 0.0min · rebond 65% (81/123) (MFE +2.38%)
   - −2.0% : fill 30min 58% · séance 69% (114/159) · gap 30% · délai 0.0min · rebond 63% (74/114) (MFE +2.43%)
   - −3.0% : fill 30min 51% · séance 61% (97/159) · gap 12% · délai 1.2min · rebond 74% (70/97) (MFE +2.55%)
   - −4.0% : fill 30min 38% · séance 47% (77/159) · gap 4% · délai 4.7min · rebond 74% (55/77) (MFE +2.33%)
   - −5.0% : fill 30min 22% · séance 40% (64/159) · gap 1% · délai 21.7min · rebond 68% (47/64) (MFE +1.71%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.75% (p90 −2.79%) → stop au-delà de −1.85% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.22% (p90 −3.76%) → stop au-delà de −2.13% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.24% (p90 −4.13%) → stop au-delà de −2.53% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1176 jambes) : jambe baissière méd −1.32% (p90 −3.29%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (83 séances) :
      · −1.0% : fill 98% (82/83) · rebond 64% (50/82)
      · −2.0% : fill 88% (77/83) · rebond 64% (52/77)
      · −3.0% : fill 82% (69/83) · rebond 70% (49/69)
      · −4.0% : fill 64% (55/83) · rebond 71% (39/55)
      · −5.0% : fill 55% (47/83) · rebond 66% (36/47)
   - **flat** (14 séances) :
      · −1.0% : fill 89% (12/14) · rebond 88% (10/12)
      · −2.0% : fill 63% (10/14) · rebond 61% (7/10)
      · −3.0% : fill 44% (5/14) · rebond 75% (3/5)
      · −4.0% : fill 44% (5/14) · rebond 75% (3/5)
      · −5.0% : fill 44% (5/14) · rebond 87% (3/5)
   - **gap-up** (62 séances) :
      · −1.0% : fill 55% (37/62) · rebond 64% (25/37)
      · −2.0% : fill 43% (27/62) · rebond 62% (15/27)
      · −3.0% : fill 35% (23/62) · rebond 87% (18/23)
      · −4.0% : fill 22% (17/62) · rebond 82% (13/17)
      · −5.0% : fill 18% (12/62) · rebond 66% (8/12)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 64% si les 15 1res min sont vertes (81 cas) · 36% si rouges (79 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:32** → P(séance verte=clôture>ouverture) 90% si début vert vs 16% si rouge (base 51% · écart 73 pts) ; prédictivité sature ensuite (plafond brut 140min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **90%** · continue >prix actuel 55% ; creux résiduel méd -1.97% (q20 -3.13%) → **SL/trailing à −3.13%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.68% / q75 +4.27% → **scale +2.68% / runner +4.27%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **16%** (continue à baisser 55%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.71%** (au-delà de la MAE q10 -5.71%), cible rebond +2.05% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.32% .. +4.67%] · haut q95 +7.12% · bas q05 -6.58%
   - 60min (n=160) : retour [-6.04% .. +6.7%] · haut q95 +8.35% · bas q05 -7.07%
   - 2h (n=160) : retour [-7.35% .. +7.76%] · haut q95 +9.2% · bas q05 -8.2%
   - 4h (n=160) : retour [-7.97% .. +6.36%] · haut q95 +9.2% · bas q05 -9.43%
   - 6h (n=160) : retour [-8.43% .. +7.9%] · haut q95 +9.5% · bas q05 -10.27%
   - session (n=160) : retour [-7.7% .. +8.8%] · haut q95 +10.58% · bas q05 -10.32%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RGTI = **volatil sans tendance propre (choppy)** (vol intra méd 4.64%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 27.7  _(survente)_
- **ADX** : 30.4  _(tendance etablie)_
- **MACD** : hist -0.055  _(pas de croisement recent)_
- **BB** : %B 0.19 · largeur 43.4%
- **ATR** : 1.03 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.223  _(distribution)_
- **Vol ratio** : 0.67  _(volume normal)_
- **Choppiness** : 47.2  _(transition)_
- **MA** : MA20 16.37 · MA50 19.45 · MA200 22.77  _(prix < MA20)_
- **Dist MA** : MA20 -13.6% · MA50 -27.3% · MA200 -37.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83306 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
