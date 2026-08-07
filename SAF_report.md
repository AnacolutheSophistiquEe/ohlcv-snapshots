# SAF

**Generated** : 2026-08-07T00:06:03.617978+00:00  
**Santé technique** : 8/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €355.90  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot €355.90 (+1.6% vs entrée) · entrée €350.16 · stop €341.00 · T1 €356.88 · R/R 0.73  
> ↳ P(T1 av. stop) 67 % _(réel 5 s)_ · EV/risk 0.114 _(réel 5 s)_ (GBM 0.0) · ¼-Kelly 0.003 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 219 % hors [0,100] (R² max 0.75). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : RSI 71.1 > 70 (surachat) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €348.82–€351.51 (mid €350.16)
- Spot actuel : €355.90 (+1.6% au-dessus de la zone — repli à attendre)
- Stop : €341.00 (stop swing_plan-based (-4.19%))
- Targets : T1 €356.88 · R/R 0.73 | T2 €363.60 · R/R 1.47 | T3 €370.32 · R/R 2.2
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €341.00


## Edge, scénarios & sizing

- EV/risk : 0.0 | EV/share : €0.004 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 32 % | T3 19 %
- Kelly (position) : f* 0.011 | ¼-Kelly 0.003 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 38.8 | side 56.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 356.0 (= 1 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.735% → cible +2.125% / stop −2.0%, p_fill 57%, n_eff≈24.4) : P(cible|rempli) **17%** · **EV/risk -0.030** (×p_fill ; si rempli -0.11% du capital)
  - **swing** (entrée dip −1.615% → cible +1.919% / stop −2.617%, p_fill 60%, n_eff≈20.6) : P(cible|rempli) **67%** · **EV/risk +0.114** (×p_fill ; si rempli +0.50% du capital)
  - **deep** (entrée dip −2.487% → cible +2.713% / stop −3.961%, p_fill 54%, n_eff≈18.8) : P(cible|rempli) **57%** · **EV/risk +0.041** (×p_fill ; si rempli +0.30% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→55% · +2.0%→32% · +3.0%→14% · +5.0%→2% · +8.0%→1%
- Range intraday médian 2.75% (p90 4.55%) · excursion haute méd. +1.2% / basse méd. −0.98%
- Profil de vol intra : ouverture 1.69% vs midi 0.63% vs clôture 0.743% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 39% · recovery-V 20%)_
- **Régime intraday** : **chop** _(efficiency 0.094 ; mean-reverting — autocorr -0.066)_ ; drift intra méd. 0.136% ; recovery-V 23%
- **σ réalisé intraday** 1.947% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 71% / bas 52% / whipsaw 26%
- POC intraday (dernière séance, temps-au-prix) : 358.5519 (VA 357.5506–359.4419 ; dernier close 357.9)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 17% · rebond 54% · **stop −1.63%** sous le fill (sous le bruit) · cible +1.2% · R/R 0.74 (high win-rate)
- Gaps overnight (n=159) : méd. 0.13% · baisse 46% (gap-down >1% 9% · >2% 1%)
- Excursion ouverture 5min (n=160) : bas méd −0.44% (p90 −1.62%) · haut méd +0.21% · range méd 0.94%
- Excursion ouverture 15min (n=160) : bas méd −0.62% (p90 −1.91%) · haut méd +0.36% · range méd 1.22%
- Excursion ouverture 30min (n=160) : bas méd −0.62% (p90 −1.92%) · haut méd +0.56% · range méd 1.45%
- Excursion ouverture 60min (n=160) : bas méd −0.69% (p90 −1.93%) · haut méd +0.59% · range méd 1.62%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 357.9 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 68% (113/159) · gap 21% · délai 0.2min · rebond 43% (45/113) (MFE +0.89%)
   - −1.0% : fill 30min 41% · séance 51% (83/159) · gap 9% · délai 0.4min · rebond 43% (31/83) (MFE +0.67%)
   - −1.5% : fill 30min 28% · séance 42% (70/159) · gap 3% · délai 7.5min · rebond 45% (26/70) (MFE +0.91%)
   - −2.0% : fill 30min 13% · séance 32% (52/159) · gap 1% · délai 52.5min · rebond 52% (24/52) (MFE +1.14%)
   - −3.0% : fill 30min 3% · séance 17% (29/159) · gap 1% · délai 87.1min · rebond 54% (17/29) (MFE +1.2%)
   - −4.0% : fill 30min 2% · séance 7% (13/159) · gap 0% · délai 126.9min · rebond 62% (7/13) (MFE +1.25%)
   - −5.0% : fill 30min 0% · séance 1% (3/159) · gap 0% · délai 360.2min · rebond 31% (1/3) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.18% (p90 −0.89%) → stop au-delà de −0.73% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −0.78%) → stop au-delà de −0.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=210 jambes) : jambe baissière méd −1.04% (p90 −2.45%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 82% (44/54) · rebond 37% (16/44)
      · −2.0% : fill 63% (32/54) · rebond 48% (15/32)
      · −3.0% : fill 30% (17/54) · rebond 50% (9/17)
      · −4.0% : fill 16% (9/54) · rebond 69% (5/9)
      · −5.0% : fill 2% (2/54) · rebond 0% (0/2)
   - **flat** (43 séances) :
      · −1.0% : fill 45% (19/43) · rebond 56% (10/19)
      · −2.0% : fill 21% (9/43) · rebond 75% (5/9)
      · −3.0% : fill 11% (5/43) · rebond 85% (4/5)
      · −4.0% : fill 1% (1/43) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/43) · rebond 0% (0/0)
   - **gap-up** (62 séances) :
      · −1.0% : fill 29% (20/62) · rebond 42% (5/20)
      · −2.0% : fill 15% (11/62) · rebond 43% (4/11)
      · −3.0% : fill 10% (7/62) · rebond 36% (4/7)
      · −4.0% : fill 4% (3/62) · rebond 30% (1/3)
      · −5.0% : fill 1% (1/62) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 69% si les 15 1res min sont vertes (72 cas) · 33% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **44min** → P(séance verte=clôture>ouverture) 76% si début vert vs 26% si rouge (base 51% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 298min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **76%** · continue >prix actuel 57% ; creux résiduel méd -0.7% (q20 -1.49%) → **SL/trailing à −1.49%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.21% / q75 +1.63% → **scale +1.21% / runner +1.63%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **26%** (continue à baisser 47%) → **RÉDUIRE ~74%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.43%** (au-delà de la MAE q10 -2.43%), cible rebond +1.06% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.61% .. +1.74%] · haut q95 +2.01% · bas q05 -2.27%
   - 60min (n=160) : retour [-1.75% .. +2.17%] · haut q95 +2.5% · bas q05 -2.56%
   - 2h (n=160) : retour [-2.38% .. +2.31%] · haut q95 +2.65% · bas q05 -3.02%
   - 4h (n=160) : retour [-2.11% .. +2.23%] · haut q95 +2.98% · bas q05 -3.36%
   - 6h (n=160) : retour [-2.2% .. +2.7%] · haut q95 +3.15% · bas q05 -3.77%
   - session (n=160) : retour [-3.2% .. +2.69%] · haut q95 +3.64% · bas q05 -4.02%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.7%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 1.5/2 | R/R T1 : 0.5 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 71.1  _(surachat)_
- **ADX** : 16.3  _(pas de tendance nette)_
- **MACD** : hist 2.317  _(pas de croisement recent)_
- **BB** : %B 0.93 · largeur 13.6%
- **ATR** : 9.16 (63.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.193  _(accumulation)_
- **Vol ratio** : 0.36  _(volume atone)_
- **Choppiness** : 39.7  _(transition)_
- **MA** : MA20 336.39 · MA50 327.8 · MA200 306.21  _(prix > MA20)_
- **Dist MA** : MA20 +5.8% · MA50 +8.6% · MA200 +16.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93821 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
