# RHM

**Generated** : 2026-07-17T00:01:58.301867+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €965.30  

> 🟡 **WAIT-FOR-DIP** — spot +1.0 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €965.30 (+1.0% vs entrée) · entrée €956.17 · stop €937.05 · T1 €984.74 · R/R 1.49  
> ↳ P(T1 av. stop) 31 % _(réel 5 s)_ · EV/risk 0.091 _(réel 5 s)_ (GBM 0.018) · ¼-Kelly 0.005 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €950.46–€961.89 (mid €956.17)
- Spot actuel : €965.30 (+1.0% au-dessus de la zone — repli à attendre)
- Stop : €937.05 (stop swing_plan-based (-5.35%))
- Targets : T1 €984.74 · R/R 1.49 | T2 €1013.30 · R/R 2.99 | T3 €1041.86 · R/R 4.48
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €937.05


## Edge, scénarios & sizing

- EV/risk : 0.018 | EV/share : €0.353 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 30 % | T2 4 % | T3 4 %
- Kelly (position) : f* 0.021 | ¼-Kelly 0.005 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 32.2 | bear 5.0 | side 62.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.949% → cible +2.987% / stop −2.0%, p_fill 86%, n_eff≈33.8) : P(cible|rempli) **31%** · **EV/risk +0.091** (×p_fill ; si rempli +0.21% du capital)
  - **swing** (entrée dip −2.08% → cible +6.679% / stop −3.34%, p_fill 48%, n_eff≈17.7) : P(cible|rempli) **18%** · **EV/risk -0.229** (×p_fill ; si rempli -1.60% du capital)
  - **deep** (entrée dip −3.219% → cible +9.446% / stop −4.723%, p_fill 43%, n_eff≈18.6) : P(cible|rempli) **14%** · **EV/risk -0.239** (×p_fill ; si rempli -2.62% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→72% · +1.0%→61% · +2.0%→48% · +3.0%→30% · +5.0%→4% · +8.0%→0%
- Range intraday médian 4.15% (p90 6.86%) · excursion haute méd. +1.85% / basse méd. −1.72%
- Profil de vol intra : ouverture 2.55% vs midi 0.889% vs clôture 1.09% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 56% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; neutre — autocorr 0.027)_ ; drift intra méd. -0.594% ; recovery-V 38%
- **σ réalisé intraday** 2.87% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 76% / whipsaw 41%
- POC intraday (dernière séance, temps-au-prix) : 975.4075 (VA 967.7675–980.1825 ; dernier close 980.3)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 23% · rebond 58% · **stop −3.37%** sous le fill (sous le bruit) · cible +1.38% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.07% · baisse 43% (gap-down >1% 14% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.77% (p90 −1.51%) · haut méd +0.57% · range méd 1.44%
- Excursion ouverture 15min (n=160) : bas méd −0.98% (p90 −1.96%) · haut méd +0.74% · range méd 1.97%
- Excursion ouverture 30min (n=160) : bas méd −1.06% (p90 −2.37%) · haut méd +0.96% · range méd 2.2%
- Excursion ouverture 60min (n=160) : bas méd −1.1% (p90 −2.65%) · haut méd +1.01% · range méd 2.37%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 980.3 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 78% (121/159) · gap 27% · délai 0.3min · rebond 58% (64/121) (MFE +1.25%)
   - −1.0% : fill 30min 50% · séance 73% (109/159) · gap 14% · délai 5.6min · rebond 58% (62/109) (MFE +1.41%)
   - −1.5% : fill 30min 30% · séance 56% (81/159) · gap 7% · délai 24.8min · rebond 46% (40/81) (MFE +0.89%)
   - −2.0% : fill 30min 21% · séance 47% (70/159) · gap 6% · délai 35.9min · rebond 58% (40/70) (MFE +1.2%)
   - −3.0% : fill 30min 10% · séance 33% (47/159) · gap 3% · délai 121.9min · rebond 58% (29/47) (MFE +1.3%)
   - −4.0% : fill 30min 4% · séance 23% (28/159) · gap 2% · délai 210.8min · rebond 58% (16/28) (MFE +1.38%)
   - −5.0% : fill 30min 2% · séance 12% (16/159) · gap 1% · délai 206.9min · rebond 48% (8/16) (MFE +0.74%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.58% (p90 −1.46%) → stop au-delà de −1.18% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.57% (p90 −1.65%) → stop au-delà de −1.35% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.3% (p90 −1.64%) → stop au-delà de −1.32% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=464 jambes) : jambe baissière méd −1.1% (p90 −2.6%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 93% (48/50) · rebond 55% (25/48)
      · −2.0% : fill 79% (38/50) · rebond 58% (23/38)
      · −3.0% : fill 53% (27/50) · rebond 55% (17/27)
      · −4.0% : fill 37% (15/50) · rebond 66% (10/15)
      · −5.0% : fill 20% (9/50) · rebond 77% (7/9)
   - **flat** (51 séances) :
      · −1.0% : fill 80% (38/51) · rebond 69% (25/38)
      · −2.0% : fill 34% (18/51) · rebond 71% (10/18)
      · −3.0% : fill 23% (11/51) · rebond 56% (6/11)
      · −4.0% : fill 20% (9/51) · rebond 38% (3/9)
      · −5.0% : fill 13% (6/51) · rebond 22% (1/6)
   - **gap-up** (58 séances) :
      · −1.0% : fill 48% (23/58) · rebond 49% (12/23)
      · −2.0% : fill 29% (14/58) · rebond 46% (7/14)
      · −3.0% : fill 22% (9/58) · rebond 66% (6/9)
      · −4.0% : fill 12% (4/58) · rebond 61% (3/4)
      · −5.0% : fill 5% (1/58) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 66% si les 15 1res min sont vertes (83 cas) · 30% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 77% si début vert vs 22% si rouge (base 48% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 295min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **77%** · continue >prix actuel 48% ; creux résiduel méd -1.37% (q20 -2.57%) → **SL/trailing à −2.57%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.25% / q75 +1.89% → **scale +1.25% / runner +1.89%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **22%** (continue à baisser 57%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.99%** (au-delà de la MAE q10 -4.99%), cible rebond +1.06% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.66% .. +3.12%] · haut q95 +3.81% · bas q05 -2.88%
   - 60min (n=160) : retour [-3.58% .. +3.1%] · haut q95 +4.03% · bas q05 -4.17%
   - 2h (n=160) : retour [-3.67% .. +2.84%] · haut q95 +4.15% · bas q05 -4.98%
   - 4h (n=160) : retour [-4.0% .. +3.01%] · haut q95 +4.53% · bas q05 -5.14%
   - 6h (n=160) : retour [-4.76% .. +3.15%] · haut q95 +4.53% · bas q05 -5.77%
   - session (n=160) : retour [-6.34% .. +4.21%] · haut q95 +4.75% · bas q05 -6.84%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.28%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 52.4  _(neutre)_
- **ADX** : 26.8  _(tendance etablie)_
- **MACD** : hist -3.357  _(bearish_recent)_
- **BB** : %B 0.28 · largeur 32.9%
- **ATR** : 49.76 (15.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.074  _(distribution)_
- **Vol ratio** : 0.29  _(volume atone)_
- **Choppiness** : 45.5  _(transition)_
- **MA** : MA20 1041.49 · MA50 1135.14 · MA200 1505.3  _(prix < MA20)_
- **Dist MA** : MA20 -7.3% · MA50 -15.0% · MA200 -35.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90124 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
