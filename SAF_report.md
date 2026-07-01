# SAF

**Generated** : 2026-07-01T00:07:10.196010+00:00  
**Santé technique** : 10/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite normal · €344.70  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot €344.70 (+9.4% vs entrée) · entrée €315.13 · stop €311.51 · T1 €322.36 · R/R 2.0  
> ↳ P(T1 av. stop) 36 % · EV/risk 0.146 · ¼-Kelly 0.008 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 819 % hors [0,100] (R² max 0.87). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : triple_bullish (score 3)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 10/10 élevée alors que : RSI 81.8 > 70 (surachat) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 10/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €313.68–€316.57 (mid €315.13)
- Spot actuel : €344.70 (+9.4% au-dessus de la zone — repli à attendre)
- Stop : €311.51 (stop swing_plan-based (-9.63%))
- Targets : T1 €322.36 · R/R 2.0 | T2 €329.60 · R/R 4.0 | T3 €336.84 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €311.51


## Edge, scénarios & sizing

- EV/risk : 0.146 | EV/share : €0.530 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 18 % | T3 12 %
- Kelly (position) : f* 0.032 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 50.5 | side 44.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 345.0 (= 1 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=7, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→71% · +1.0%→60% · +2.0%→35% · +3.0%→15% · +5.0%→5% · +8.0%→2%
- Range intraday médian 2.77% (p90 5.22%) · excursion haute méd. +1.21% / basse méd. −1.11%
- Profil de vol intra : ouverture 1.661% vs midi 0.673% vs clôture 0.783% _(ouverture ~2.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (138 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 35% · recovery-V 19%)_
- **Régime intraday** : **chop** _(efficiency 0.111 ; mean-reverting — autocorr -0.033)_ ; drift intra méd. 0.463% ; recovery-V 27%
- **σ réalisé intraday** 1.928% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 45% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 331.2262 (VA 330.7237–332.7337 ; dernier close 334.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 21% · rebond 59% · **stop −1.6%** sous le fill (sous le bruit) · cible +1.23% · R/R 0.77 (high win-rate)
- Gaps overnight (n=137) : méd. -0.07% · baisse 53% (gap-down >1% 14% · >2% 2%)
- Excursion ouverture 5min (n=138) : bas méd −0.39% (p90 −1.45%) · haut méd +0.22% · range méd 0.92%
- Excursion ouverture 15min (n=138) : bas méd −0.47% (p90 −1.64%) · haut méd +0.43% · range méd 1.2%
- Excursion ouverture 30min (n=138) : bas méd −0.53% (p90 −1.89%) · haut méd +0.54% · range méd 1.31%
- Excursion ouverture 60min (n=138) : bas méd −0.72% (p90 −1.97%) · haut méd +0.65% · range méd 1.55%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 334.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 68% (98/137) · gap 29% · délai 0.2min · rebond 38% (36/98) (MFE +0.78%)
   - −1.0% : fill 30min 42% · séance 51% (70/137) · gap 14% · délai 0.4min · rebond 42% (25/70) (MFE +0.58%)
   - −1.5% : fill 30min 29% · séance 44% (60/137) · gap 5% · délai 6.9min · rebond 38% (20/60) (MFE +0.89%)
   - −2.0% : fill 30min 14% · séance 33% (43/137) · gap 2% · délai 39.0min · rebond 48% (19/43) (MFE +0.91%)
   - −3.0% : fill 30min 5% · séance 21% (26/137) · gap 1% · délai 203.0min · rebond 59% (16/26) (MFE +1.23%)
   - −4.0% : fill 30min 3% · séance 10% (12/137) · gap 0% · délai 153.7min · rebond 53% (6/12) (MFE +1.49%)
   - −5.0% : fill 30min 0% · séance 2% (3/137) · gap 0% · délai 360.2min · rebond 31% (1/3) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.27% (p90 −0.95%) → stop au-delà de −0.77% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.24% (p90 −0.91%) → stop au-delà de −0.77% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.15% (p90 −1.02%) → stop au-delà de −0.88% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=166 jambes) : jambe baissière méd −1.05% (p90 −2.72%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 76% (38/49) · rebond 39% (14/38)
      · −2.0% : fill 56% (27/49) · rebond 51% (13/27)
      · −3.0% : fill 35% (16/49) · rebond 58% (9/16)
      · −4.0% : fill 16% (8/49) · rebond 59% (4/8)
      · −5.0% : fill 3% (2/49) · rebond 0% (0/2)
   - **flat** (37 séances) :
      · −1.0% : fill 49% (16/37) · rebond 62% (8/16)
      · −2.0% : fill 21% (7/37) · rebond 50% (3/7)
      · −3.0% : fill 10% (4/37) · rebond 69% (3/4)
      · −4.0% : fill 2% (1/37) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/37) · rebond 0% (0/0)
   - **gap-up** (51 séances) :
      · −1.0% : fill 24% (16/51) · rebond 26% (3/16)
      · −2.0% : fill 15% (9/51) · rebond 34% (3/9)
      · −3.0% : fill 11% (6/51) · rebond 55% (4/6)
      · −4.0% : fill 8% (3/51) · rebond 30% (1/3)
      · −5.0% : fill 2% (1/51) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=138) : 51% en base · 66% si les 15 1res min sont vertes (61 cas) · 36% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=138) : COUDE à **44min** → P(séance verte=clôture>ouverture) 78% si début vert vs 24% si rouge (base 51% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=62) : tient le vert **78%** · continue >prix actuel 61% ; creux résiduel méd -0.57% (q20 -1.5%) → **SL/trailing à −1.5%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.29% / q75 +1.83% → **scale +1.29% / runner +1.83%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **24%** (continue à baisser 47%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.5%** (au-delà de la MAE q10 -2.5%), cible rebond +0.92% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=138) : retour [-1.82% .. +1.83%] · haut q95 +2.65% · bas q05 -2.28%
   - 60min (n=138) : retour [-1.83% .. +2.43%] · haut q95 +3.13% · bas q05 -2.6%
   - 2h (n=138) : retour [-2.23% .. +2.37%] · haut q95 +3.39% · bas q05 -2.92%
   - 4h (n=138) : retour [-2.16% .. +2.76%] · haut q95 +3.49% · bas q05 -3.03%
   - 6h (n=138) : retour [-2.24% .. +3.48%] · haut q95 +3.76% · bas q05 -3.14%
   - session (n=138) : retour [-2.96% .. +3.66%] · haut q95 +4.23% · bas q05 -4.15%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.4% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.67%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.76 · part idiosyncratique 0.24
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 81.8  _(surachat)_
- **ADX** : 29.0  _(tendance etablie)_
- **MACD** : hist 1.67  _(pas de croisement recent)_
- **BB** : %B 0.85 · largeur 23.8%
- **ATR** : 9.39 (72.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.038  _(neutre)_
- **Vol ratio** : 0.38  _(volume atone)_
- **Choppiness** : 32.9  _(marche directionnel)_
- **MA** : MA20 318.06 · MA50 295.78 · MA200 300.23  _(prix > MA20)_
- **Dist MA** : MA20 +8.4% · MA50 +16.5% · MA200 +14.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92219 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
