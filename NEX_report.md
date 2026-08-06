# NEX

**Generated** : 2026-08-06T21:43:15.162845+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · €140.50  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot €140.50 (+6.7% vs entrée) · entrée €131.73 · stop €126.51 · T1 €135.13 · R/R 0.65  
> ↳ P(T1 av. stop) 66 % · EV/risk 0.014 · ¼-Kelly 0.002 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 7/10 élevée alors que : %B 1.02 (collé à la bande haute) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €131.05–€132.41 (mid €131.73)
- Spot actuel : €140.50 (+6.7% au-dessus de la zone — repli à attendre)
- Stop : €126.51 (stop swing_plan-based (-9.96%))
- Targets : T1 €135.13 · R/R 0.65 | T2 €138.53 · R/R 1.3 | T3 €141.93 · R/R 1.95
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €126.51


## Edge, scénarios & sizing

- EV/risk : -0.044 | EV/share : €-0.230 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 53 % | T2 26 % | T3 11 %
- Kelly (position) : f* 0.009 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 24.6 | bear 45.9 | side 29.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 422.0 (= 3 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.837% → cible +1.153% / stop −8.0%, p_fill 37%, n_eff≈13.9) : P(cible|rempli) **54%** · **EV/risk +0.017** (×p_fill ; si rempli +0.38% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=6, n_eff=5))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→68% · +1.0%→54% · +2.0%→28% · +3.0%→12% · +5.0%→5% · +8.0%→1%
- Range intraday médian 3.1% (p90 5.26%) · excursion haute méd. +1.07% / basse méd. −1.35%
- Profil de vol intra : ouverture 1.789% vs midi 0.554% vs clôture 0.782% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (148 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 50% · recovery-V 16%)_
- **Régime intraday** : **chop** _(efficiency 0.109 ; mean-reverting — autocorr -0.035)_ ; drift intra méd. -0.707% ; recovery-V 10%
- **σ réalisé intraday** 2.255% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 51% / bas 74% / whipsaw 26%
- POC intraday (dernière séance, temps-au-prix) : 137.7694 (VA 137.2781–139.2431 ; dernier close 137.85)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 24% · rebond 57% · **stop −1.95%** sous le fill (sous le bruit) · cible +1.55% · R/R 0.79 (high win-rate)
- Gaps overnight (n=147) : méd. 0.15% · baisse 36% (gap-down >1% 9% · >2% 2%)
- Excursion ouverture 5min (n=148) : bas méd −0.45% (p90 −1.95%) · haut méd +0.34% · range méd 1.11%
- Excursion ouverture 15min (n=148) : bas méd −0.58% (p90 −2.14%) · haut méd +0.44% · range méd 1.39%
- Excursion ouverture 30min (n=148) : bas méd −0.59% (p90 −2.31%) · haut méd +0.57% · range méd 1.42%
- Excursion ouverture 60min (n=148) : bas méd −0.82% (p90 −2.59%) · haut méd +0.62% · range méd 1.59%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 137.85 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 70% (104/147) · gap 22% · délai 0.5min · rebond 44% (50/104) (MFE +0.84%)
   - −1.0% : fill 30min 38% · séance 62% (87/147) · gap 9% · délai 9.5min · rebond 46% (41/87) (MFE +0.93%)
   - −1.5% : fill 30min 23% · séance 49% (65/147) · gap 3% · délai 45.7min · rebond 48% (31/65) (MFE +0.76%)
   - −2.0% : fill 30min 16% · séance 35% (49/147) · gap 2% · délai 56.4min · rebond 49% (26/49) (MFE +0.99%)
   - −3.0% : fill 30min 4% · séance 24% (31/147) · gap 1% · délai 115.7min · rebond 57% (18/31) (MFE +1.55%)
   - −4.0% : fill 30min 1% · séance 8% (11/147) · gap 1% · délai 369.3min · rebond 16% (4/11) (MFE +0.77%)
   - −5.0% : fill 30min 1% · séance 2% (4/147) · gap 0% · délai 184.5min · rebond 89% (3/4) (MFE +1.52%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.1% (p90 −1.01%) → stop au-delà de −0.7% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.08% (p90 −0.81%) → stop au-delà de −0.52% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.16% (p90 −0.92%) → stop au-delà de −0.55% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=313 jambes) : jambe baissière méd −1.05% (p90 −2.47%) · ~6.3 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (44 séances) :
      · −1.0% : fill 80% (36/44) · rebond 44% (15/36)
      · −2.0% : fill 45% (25/44) · rebond 43% (13/25)
      · −3.0% : fill 31% (16/44) · rebond 47% (9/16)
      · −4.0% : fill 15% (7/44) · rebond 28% (3/7)
      · −5.0% : fill 8% (4/44) · rebond 89% (3/4)
   - **flat** (36 séances) :
      · −1.0% : fill 70% (24/36) · rebond 49% (13/24)
      · −2.0% : fill 40% (12/36) · rebond 51% (6/12)
      · −3.0% : fill 30% (8/36) · rebond 46% (3/8)
      · −4.0% : fill 10% (2/36) · rebond 0% (0/2)
      · −5.0% : fill 0% (0/36) · rebond 0% (0/0)
   - **gap-up** (67 séances) :
      · −1.0% : fill 46% (27/67) · rebond 46% (13/27)
      · −2.0% : fill 26% (12/67) · rebond 53% (7/12)
      · −3.0% : fill 16% (7/67) · rebond 82% (6/7)
      · −4.0% : fill 3% (2/67) · rebond 15% (1/2)
      · −5.0% : fill 0% (0/67) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=148) : 42% en base · 64% si les 15 1res min sont vertes (80 cas) · 17% si rouges (68 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=148) : COUDE à **45min** → P(séance verte=clôture>ouverture) 73% si début vert vs 16% si rouge (base 42% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 306min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=69) : tient le vert **73%** · continue >prix actuel 50% ; creux résiduel méd -1.08% (q20 -2.04%) → **SL/trailing à −2.04%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.07% / q75 +1.64% → **scale +1.07% / runner +1.64%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **16%** (continue à baisser 58%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.18%** (au-delà de la MAE q10 -3.18%), cible rebond +0.87% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=148) : retour [-2.06% .. +2.17%] · haut q95 +2.52% · bas q05 -2.75%
   - 60min (n=148) : retour [-2.89% .. +2.08%] · haut q95 +2.71% · bas q05 -3.25%
   - 2h (n=148) : retour [-3.63% .. +2.28%] · haut q95 +2.93% · bas q05 -3.81%
   - 4h (n=148) : retour [-3.41% .. +2.36%] · haut q95 +2.94% · bas q05 -4.03%
   - 6h (n=148) : retour [-3.83% .. +3.2%] · haut q95 +3.64% · bas q05 -4.2%
   - session (n=148) : retour [-3.61% .. +2.83%] · haut q95 +3.9% · bas q05 -4.76%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.4% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.95%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 59.0  _(momentum haussier)_
- **ADX** : 30.3  _(tendance etablie)_
- **MACD** : hist 1.413  _(pas de croisement recent)_
- **BB** : %B 1.02 · largeur 10.5%
- **ATR** : 5.22 (92.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.042  _(neutre)_
- **Vol ratio** : 1.3  _(volume normal)_
- **Choppiness** : 51.3  _(transition)_
- **MA** : MA20 133.26 · MA50 142.82 · MA200 131.88  _(prix > MA20)_
- **Dist MA** : MA20 +5.4% · MA50 -1.6% · MA200 +6.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92402 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
