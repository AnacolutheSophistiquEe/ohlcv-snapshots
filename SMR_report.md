# SMR

**Generated** : 2026-07-20T00:29:49.801893+00:00  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $7.72  

> 🟡 **WAIT-FOR-DIP** — spot +9.8 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $7.72 (+9.8% vs entrée) · entrée $7.03 · stop $6.83 · T1 $7.22 · R/R 0.95  
> ↳ P(T1 av. stop) 53 % · EV/risk 0.041 · ¼-Kelly 0.017 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.94% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -39 % hors [0,100] (R² max 0.70). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $6.99–$7.07 (mid $7.03)
- Spot actuel : $7.72 (+9.8% au-dessus de la zone — repli à attendre)
- Stop : $6.83 (stop swing_plan-based (-20.5%))
- Targets : T1 $7.22 · R/R 0.95 | T2 $7.40 · R/R 1.85 | T3 $7.59 · R/R 2.8
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $6.83


## Edge, scénarios & sizing

- EV/risk : 0.041 | EV/share : $0.009 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 53 % | T2 35 % | T3 35 %
- Kelly (position) : f* 0.066 | ¼-Kelly 0.017 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 33.9 | bear 50.6 | side 15.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=10, n_eff=7))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→78% · +2.0%→65% · +3.0%→56% · +5.0%→39% · +8.0%→18%
- Range intraday médian 7.73% (p90 12.61%) · excursion haute méd. +3.54% / basse méd. −3.29%
- Profil de vol intra : ouverture 4.987% vs midi 1.575% vs clôture 1.739% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; neutre — autocorr -0.012)_ ; drift intra méd. -0.603% ; recovery-V 19%
- **σ réalisé intraday** 4.838% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 63% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 7.7725 (VA 7.5855–7.8915 ; dernier close 7.715)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 56% · rebond 78% · **stop −6.08%** sous le fill (sous le bruit) · cible +2.53% · R/R 0.42 (high win-rate)
- Gaps overnight (n=159) : méd. -0.74% · baisse 59% (gap-down >1% 43% · >2% 30%)
- Excursion ouverture 5min (n=160) : bas méd −1.18% (p90 −3.39%) · haut méd +0.98% · range méd 2.69%
- Excursion ouverture 15min (n=160) : bas méd −1.68% (p90 −3.82%) · haut méd +1.3% · range méd 3.66%
- Excursion ouverture 30min (n=160) : bas méd −1.86% (p90 −4.81%) · haut méd +1.71% · range méd 4.45%
- Excursion ouverture 60min (n=160) : bas méd −2.16% (p90 −6.04%) · haut méd +2.57% · range méd 5.46%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 7.715 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 75% · séance 83% (132/159) · gap 52% · délai 0.0min · rebond 67% (82/132) (MFE +1.73%)
   - −1.0% : fill 30min 70% · séance 79% (126/159) · gap 43% · délai 0.0min · rebond 66% (83/126) (MFE +2.01%)
   - −1.5% : fill 30min 66% · séance 76% (120/159) · gap 40% · délai 0.0min · rebond 73% (87/120) (MFE +2.23%)
   - −2.0% : fill 30min 60% · séance 71% (114/159) · gap 30% · délai 0.1min · rebond 68% (82/114) (MFE +2.5%)
   - −3.0% : fill 30min 49% · séance 63% (103/159) · gap 11% · délai 2.1min · rebond 75% (84/103) (MFE +2.58%)
   - −4.0% : fill 30min 38% · séance 56% (88/159) · gap 6% · délai 9.3min · rebond 78% (69/88) (MFE +2.53%)
   - −5.0% : fill 30min 26% · séance 44% (65/159) · gap 3% · délai 19.5min · rebond 67% (47/65) (MFE +1.87%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.98% (p90 −2.71%) → stop au-delà de −2.07% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.03% (p90 −2.9%) → stop au-delà de −2.16% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.09% (p90 −3.03%) → stop au-delà de −2.35% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1178 jambes) : jambe baissière méd −1.4% (p90 −3.2%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (85 séances) :
      · −1.0% : fill 100% (85/85) · rebond 68% (56/85)
      · −2.0% : fill 94% (81/85) · rebond 74% (61/81)
      · −3.0% : fill 86% (77/85) · rebond 78% (64/77)
      · −4.0% : fill 78% (68/85) · rebond 84% (57/68)
      · −5.0% : fill 60% (48/85) · rebond 69% (37/48)
   - **flat** (14 séances) :
      · −1.0% : fill 80% (11/14) · rebond 54% (7/11)
      · −2.0% : fill 69% (9/14) · rebond 22% (4/9)
      · −3.0% : fill 66% (7/14) · rebond 47% (4/7)
      · −4.0% : fill 66% (7/14) · rebond 55% (3/7)
      · −5.0% : fill 56% (6/14) · rebond 80% (5/6)
   - **gap-up** (60 séances) :
      · −1.0% : fill 47% (30/60) · rebond 67% (20/30)
      · −2.0% : fill 38% (24/60) · rebond 67% (17/24)
      · −3.0% : fill 29% (19/60) · rebond 80% (16/19)
      · −4.0% : fill 21% (13/60) · rebond 67% (9/13)
      · −5.0% : fill 16% (11/60) · rebond 41% (5/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 41% en base · 53% si les 15 1res min sont vertes (68 cas) · 32% si rouges (92 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:25** → P(séance verte=clôture>ouverture) 77% si début vert vs 11% si rouge (base 41% · écart 67 pts) ; prédictivité sature ensuite (plafond brut 233min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **77%** · continue >prix actuel 49% ; creux résiduel méd -2.31% (q20 -3.72%) → **SL/trailing à −3.72%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.25% / q75 +4.33% → **scale +2.25% / runner +4.33%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **11%** (continue à baisser 56%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.75%** (au-delà de la MAE q10 -5.75%), cible rebond +1.44% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.54% .. +4.91%] · haut q95 +6.59% · bas q05 -6.05%
   - 60min (n=160) : retour [-6.69% .. +5.61%] · haut q95 +7.9% · bas q05 -7.9%
   - 2h (n=160) : retour [-7.84% .. +7.9%] · haut q95 +11.26% · bas q05 -8.89%
   - 4h (n=160) : retour [-8.62% .. +7.96%] · haut q95 +11.25% · bas q05 -10.71%
   - 6h (n=160) : retour [-8.11% .. +8.63%] · haut q95 +11.42% · bas q05 -10.72%
   - session (n=160) : retour [-8.16% .. +10.56%] · haut q95 +11.65% · bas q05 -10.74%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 4.95%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 21.4  _(survente)_
- **ADX** : 21.8  _(pas de tendance nette)_
- **MACD** : hist -0.148  _(pas de croisement recent)_
- **BB** : %B 0.1 · largeur 47.0%
- **ATR** : 0.69 (3.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.092  _(distribution)_
- **Vol ratio** : 0.77  _(volume normal)_
- **Choppiness** : 36.7  _(marche directionnel)_
- **MA** : MA20 9.52 · MA50 10.69 · MA200 18.0  _(prix < MA20)_
- **Dist MA** : MA20 -18.9% · MA50 -27.8% · MA200 -57.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (81441 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
