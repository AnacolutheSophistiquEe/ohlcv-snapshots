# RHM

**Generated** : 2026-08-03T21:36:06.989977+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €1175.00  

> 🟡 **WAIT-FOR-DIP** — spot +0.9 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €1175.00 (+0.9% vs entrée) · entrée €1164.90 · stop €1141.60 · T1 €1181.77 · R/R 0.72  
> ↳ P(T1 av. stop) 55 % _(réel 5 s)_ · EV/risk 0.032 _(réel 5 s)_ (GBM 0.044) · ¼-Kelly 0.021 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 210 % hors [0,100] (R² max 0.98). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 7/10 élevée alors que : RSI 88.3 > 70 (surachat) ; %B 0.99 (collé à la bande haute) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €1161.53–€1168.27 (mid €1164.90)
- Spot actuel : €1175.00 (+0.9% au-dessus de la zone — repli à attendre)
- Stop : €1141.60 (stop swing_plan-based (-5.62%))
- Targets : T1 €1181.77 · R/R 0.72 | T2 €1198.63 · R/R 1.45 | T3 €1215.50 · R/R 2.17
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €1141.60


## Edge, scénarios & sizing

- EV/risk : 0.044 | EV/share : €1.015 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 56 % | T2 30 % | T3 7 %
- Kelly (position) : f* 0.084 | ¼-Kelly 0.021 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 72.8 | bear 5.0 | side 22.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.857% → cible +1.448% / stop −2.0%, p_fill 86%, n_eff≈35.5) : P(cible|rempli) **55%** · **EV/risk +0.032** (×p_fill ; si rempli +0.07% du capital)
  - **swing** (entrée dip −1.896% → cible +3.238% / stop −3.796%, p_fill 52%, n_eff≈23.8) : P(cible|rempli) **55%** · **EV/risk +0.031** (×p_fill ; si rempli +0.23% du capital)
  - **deep** (entrée dip −2.924% → cible +4.579% / stop −5.754%, p_fill 54%, n_eff≈20.7) : P(cible|rempli) **48%** · **EV/risk -0.104** (×p_fill ; si rempli -1.11% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→66% · +2.0%→50% · +3.0%→29% · +5.0%→2% · +8.0%→1%
- Range intraday médian 3.99% (p90 6.65%) · excursion haute méd. +2.05% / basse méd. −1.63%
- Profil de vol intra : ouverture 2.522% vs midi 0.893% vs clôture 1.088% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 51% · recovery-V 42%)_
- **Régime intraday** : **chop** _(efficiency 0.095 ; neutre — autocorr -0.016)_ ; drift intra méd. 0.026% ; recovery-V 49%
- **σ réalisé intraday** 2.903% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 76% / bas 60% / whipsaw 41%
- POC intraday (dernière séance, temps-au-prix) : 1137.7525 (VA 1128.1925–1156.8725 ; dernier close 1141.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 20% · rebond 60% · **stop −3.16%** sous le fill (sous le bruit) · cible +1.45% · R/R 0.46 (high win-rate)
- Gaps overnight (n=159) : méd. 0.18% · baisse 38% (gap-down >1% 11% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.72% (p90 −1.75%) · haut méd +0.62% · range méd 1.42%
- Excursion ouverture 15min (n=160) : bas méd −0.94% (p90 −2.03%) · haut méd +0.71% · range méd 1.87%
- Excursion ouverture 30min (n=160) : bas méd −0.98% (p90 −2.75%) · haut méd +0.88% · range méd 2.12%
- Excursion ouverture 60min (n=160) : bas méd −1.07% (p90 −3.19%) · haut méd +1.0% · range méd 2.25%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1141.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 74% (119/159) · gap 26% · délai 0.3min · rebond 59% (63/119) (MFE +1.34%)
   - −1.0% : fill 30min 45% · séance 66% (108/159) · gap 11% · délai 4.4min · rebond 61% (64/108) (MFE +1.4%)
   - −1.5% : fill 30min 30% · séance 52% (81/159) · gap 6% · délai 18.2min · rebond 55% (43/81) (MFE +1.14%)
   - −2.0% : fill 30min 21% · séance 44% (71/159) · gap 4% · délai 30.4min · rebond 64% (44/71) (MFE +1.38%)
   - −3.0% : fill 30min 9% · séance 27% (45/159) · gap 2% · délai 119.5min · rebond 60% (27/45) (MFE +1.31%)
   - −4.0% : fill 30min 4% · séance 20% (27/159) · gap 1% · délai 152.8min · rebond 60% (15/27) (MFE +1.45%)
   - −5.0% : fill 30min 1% · séance 10% (15/159) · gap 1% · délai 201.2min · rebond 48% (7/15) (MFE +0.73%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.67% (p90 −1.75%) → stop au-delà de −1.25% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.56% (p90 −1.82%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.33% (p90 −1.95%) → stop au-delà de −1.61% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=481 jambes) : jambe baissière méd −1.07% (p90 −2.56%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 94% (48/50) · rebond 63% (28/48)
      · −2.0% : fill 78% (38/50) · rebond 64% (25/38)
      · −3.0% : fill 50% (26/50) · rebond 59% (16/26)
      · −4.0% : fill 36% (15/50) · rebond 70% (10/15)
      · −5.0% : fill 16% (8/50) · rebond 76% (6/8)
   - **flat** (49 séances) :
      · −1.0% : fill 67% (36/49) · rebond 69% (24/36)
      · −2.0% : fill 29% (17/49) · rebond 72% (10/17)
      · −3.0% : fill 19% (10/49) · rebond 55% (5/10)
      · −4.0% : fill 17% (8/49) · rebond 36% (2/8)
      · −5.0% : fill 11% (6/49) · rebond 22% (1/6)
   - **gap-up** (60 séances) :
      · −1.0% : fill 43% (24/60) · rebond 49% (12/24)
      · −2.0% : fill 30% (16/60) · rebond 62% (9/16)
      · −3.0% : fill 16% (9/60) · rebond 66% (6/9)
      · −4.0% : fill 9% (4/60) · rebond 61% (3/4)
      · −5.0% : fill 3% (1/60) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 55% en base · 72% si les 15 1res min sont vertes (83 cas) · 41% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:38** → P(séance verte=clôture>ouverture) 81% si début vert vs 30% si rouge (base 55% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 225min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **81%** · continue >prix actuel 51% ; creux résiduel méd -0.94% (q20 -2.15%) → **SL/trailing à −2.15%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.35% / q75 +2.12% → **scale +1.35% / runner +2.12%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **30%** (continue à baisser 54%) → **RÉDUIRE ~70%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.52%** (au-delà de la MAE q10 -4.52%), cible rebond +1.13% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.64% .. +2.93%] · haut q95 +3.65% · bas q05 -3.49%
   - 60min (n=160) : retour [-3.06% .. +2.89%] · haut q95 +3.76% · bas q05 -4.43%
   - 2h (n=160) : retour [-3.44% .. +2.98%] · haut q95 +4.01% · bas q05 -4.65%
   - 4h (n=160) : retour [-3.8% .. +3.15%] · haut q95 +4.56% · bas q05 -4.99%
   - 6h (n=160) : retour [-4.38% .. +3.62%] · haut q95 +4.56% · bas q05 -5.61%
   - session (n=160) : retour [-6.16% .. +4.4%] · haut q95 +4.82% · bas q05 -6.31%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.3%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : stretched_up
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

- **RSI** : 88.3  _(surachat)_
- **ADX** : 24.6  _(pas de tendance nette)_
- **MACD** : hist 25.945  _(pas de croisement recent)_
- **BB** : %B 0.99 · largeur 25.8%
- **ATR** : 43.76 (3.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.028  _(neutre)_
- **Vol ratio** : 0.97  _(volume normal)_
- **Choppiness** : 33.1  _(marche directionnel)_
- **MA** : MA20 1042.12 · MA50 1108.58 · MA200 1459.05  _(prix > MA20)_
- **Dist MA** : MA20 +12.8% · MA50 +6.0% · MA200 -19.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92104 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
