# RHM

**Generated** : 2026-07-29T21:36:05.444884+00:00  
**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €1153.40  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)  
> ↳ spot €1153.40 (+0.4% vs entrée) · entrée €1148.70 · stop €1125.73 · T1 €1166.93 · R/R 0.79  
> ↳ P(T1 av. stop) 41 % _(réel 5 s)_ · EV/risk 0.017 _(réel 5 s)_ (GBM 0.018) · ¼-Kelly 0.015 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 182 % hors [0,100] (R² max 0.98). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : RSI 79.2 > 70 (surachat) ; %B 0.99 (collé à la bande haute) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €1145.05–€1152.35 (mid €1148.70)
- Spot actuel : €1153.40 (+0.4% au-dessus de la zone — repli à attendre)
- Stop : €1125.73 (stop swing_plan-based (-2.65%))
- Targets : T1 €1166.93 · R/R 0.79 | T2 €1185.16 · R/R 1.59 | T3 €1203.39 · R/R 2.38
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €1125.73


## Edge, scénarios & sizing

- EV/risk : 0.018 | EV/share : €0.416 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 25 % | T3 3 %
- Kelly (position) : f* 0.06 | ¼-Kelly 0.015 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 69.5 | bear 5.0 | side 25.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.408% → cible +1.587% / stop −2.0%, p_fill 84%, n_eff≈36.3) : P(cible|rempli) **41%** · **EV/risk +0.017** (×p_fill ; si rempli +0.04% du capital)
  - **swing** (entrée dip −0.892% → cible +3.548% / stop −1.774%, p_fill 90%, n_eff≈37.1) : P(cible|rempli) **49%** · **EV/risk +0.348** (×p_fill ; si rempli +0.69% du capital)
  - **deep** (entrée dip −1.386% → cible +5.018% / stop −2.509%, p_fill 87%, n_eff≈33.1) : P(cible|rempli) **40%** · **EV/risk +0.104** (×p_fill ; si rempli +0.30% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→64% · +2.0%→48% · +3.0%→26% · +5.0%→1% · +8.0%→0%
- Range intraday médian 3.94% (p90 6.65%) · excursion haute méd. +1.85% / basse méd. −1.68%
- Profil de vol intra : ouverture 2.479% vs midi 0.852% vs clôture 1.077% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 50% · recovery-V 40%)_
- **Régime intraday** : **chop** _(efficiency 0.094 ; mean-reverting — autocorr -0.031)_ ; drift intra méd. -0.051% ; recovery-V 45%
- **σ réalisé intraday** 2.681% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 78% / bas 59% / whipsaw 37%
- POC intraday (dernière séance, temps-au-prix) : 1080.71 (VA 1072.55–1092.95 ; dernier close 1079.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 21% · rebond 60% · **stop −3.16%** sous le fill (sous le bruit) · cible +1.45% · R/R 0.46 (high win-rate)
- Gaps overnight (n=159) : méd. 0.09% · baisse 41% (gap-down >1% 12% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.7% (p90 −1.72%) · haut méd +0.65% · range méd 1.45%
- Excursion ouverture 15min (n=160) : bas méd −0.93% (p90 −1.99%) · haut méd +0.72% · range méd 1.86%
- Excursion ouverture 30min (n=160) : bas méd −0.98% (p90 −2.35%) · haut méd +0.88% · range méd 2.06%
- Excursion ouverture 60min (n=160) : bas méd −1.06% (p90 −2.62%) · haut méd +1.0% · range méd 2.22%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1079.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 75% (120/159) · gap 27% · délai 0.3min · rebond 59% (64/120) (MFE +1.34%)
   - −1.0% : fill 30min 46% · séance 66% (108/159) · gap 12% · délai 4.4min · rebond 62% (64/108) (MFE +1.4%)
   - −1.5% : fill 30min 30% · séance 52% (80/159) · gap 6% · délai 18.1min · rebond 51% (42/80) (MFE +1.14%)
   - −2.0% : fill 30min 21% · séance 43% (69/159) · gap 5% · délai 30.4min · rebond 61% (42/69) (MFE +1.32%)
   - −3.0% : fill 30min 10% · séance 29% (45/159) · gap 2% · délai 119.5min · rebond 60% (27/45) (MFE +1.31%)
   - −4.0% : fill 30min 5% · séance 21% (27/159) · gap 1% · délai 152.8min · rebond 60% (15/27) (MFE +1.45%)
   - −5.0% : fill 30min 1% · séance 10% (15/159) · gap 1% · délai 201.2min · rebond 48% (7/15) (MFE +0.73%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.67% (p90 −1.63%) → stop au-delà de −1.2% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.56% (p90 −1.71%) → stop au-delà de −1.34% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.28% (p90 −1.73%) → stop au-delà de −1.47% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=468 jambes) : jambe baissière méd −1.05% (p90 −2.51%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (51 séances) :
      · −1.0% : fill 94% (49/51) · rebond 63% (28/49)
      · −2.0% : fill 77% (38/51) · rebond 64% (25/38)
      · −3.0% : fill 49% (26/51) · rebond 59% (16/26)
      · −4.0% : fill 36% (15/51) · rebond 70% (10/15)
      · −5.0% : fill 16% (8/51) · rebond 76% (6/8)
   - **flat** (50 séances) :
      · −1.0% : fill 67% (36/50) · rebond 69% (24/36)
      · −2.0% : fill 28% (17/50) · rebond 72% (10/17)
      · −3.0% : fill 19% (10/50) · rebond 55% (5/10)
      · −4.0% : fill 17% (8/50) · rebond 36% (2/8)
      · −5.0% : fill 11% (6/50) · rebond 22% (1/6)
   - **gap-up** (58 séances) :
      · −1.0% : fill 40% (23/58) · rebond 49% (12/23)
      · −2.0% : fill 24% (14/58) · rebond 46% (7/14)
      · −3.0% : fill 18% (9/58) · rebond 66% (6/9)
      · −4.0% : fill 10% (4/58) · rebond 61% (3/4)
      · −5.0% : fill 4% (1/58) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 55% en base · 72% si les 15 1res min sont vertes (84 cas) · 38% si rouges (76 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:38** → P(séance verte=clôture>ouverture) 80% si début vert vs 29% si rouge (base 55% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 225min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=83) : tient le vert **80%** · continue >prix actuel 53% ; creux résiduel méd -0.94% (q20 -1.98%) → **SL/trailing à −1.98%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.42% / q75 +2.15% → **scale +1.42% / runner +2.15%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **29%** (continue à baisser 54%) → **RÉDUIRE ~71%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.58%** (au-delà de la MAE q10 -4.58%), cible rebond +1.13% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.64% .. +3.0%] · haut q95 +3.72% · bas q05 -3.1%
   - 60min (n=160) : retour [-3.18% .. +2.97%] · haut q95 +3.88% · bas q05 -3.82%
   - 2h (n=160) : retour [-3.5% .. +3.02%] · haut q95 +4.04% · bas q05 -4.47%
   - 4h (n=160) : retour [-3.45% .. +3.23%] · haut q95 +4.38% · bas q05 -5.02%
   - 6h (n=160) : retour [-4.49% .. +3.05%] · haut q95 +4.53% · bas q05 -5.68%
   - session (n=160) : retour [-6.17% .. +4.1%] · haut q95 +4.72% · bas q05 -6.52%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.3%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 79.2  _(surachat)_
- **ADX** : 23.6  _(pas de tendance nette)_
- **MACD** : hist 21.378  _(pas de croisement recent)_
- **BB** : %B 0.99 · largeur 22.8%
- **ATR** : 45.35 (5.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.071  _(accumulation)_
- **Vol ratio** : 1.96  _(volume au-dessus de la moyenne)_
- **Choppiness** : 35.1  _(marche directionnel)_
- **MA** : MA20 1036.81 · MA50 1111.02 · MA200 1465.88  _(prix > MA20)_
- **Dist MA** : MA20 +11.2% · MA50 +3.8% · MA200 -21.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92735 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
