# SAF

**Generated** : 2026-07-02T00:07:53.268702+00:00  
**Santé technique** : 10/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite normal · €350.40  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)  
> ↳ spot €350.40 (+0.8% vs entrée) · entrée €347.69 · stop €343.82 · T1 €355.42 · R/R 2.0  
> ↳ P(T1 av. stop) 44 % _(réel 5 s)_ · EV/risk 0.148 _(réel 5 s)_ (GBM 0.15) · ¼-Kelly 0.01 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 994 % hors [0,100] (R² max 0.87). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : triple_bullish (score 3)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 10/10 élevée alors que : RSI 82.2 > 70 (surachat) ; extension extrême (≥3×ATR, confluence MA20/50) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 10/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €346.14–€349.23 (mid €347.69)
- Spot actuel : €350.40 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : €343.82 (stop swing_plan-based (-1.88%))
- Targets : T1 €355.42 · R/R 2.0 | T2 €363.16 · R/R 4.0 | T3 €370.89 · R/R 5.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €343.82


## Edge, scénarios & sizing

- EV/risk : 0.15 | EV/share : €0.580 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 20 % | T3 12 %
- Kelly (position) : f* 0.038 | ¼-Kelly 0.01 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 42.4 | side 52.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 350.0 (= 1 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.355% → cible +0.995% / stop −1.5%, p_fill 75%, n_eff≈31.5) : P(cible|rempli) **46%** · **EV/risk +0.032** (×p_fill ; si rempli +0.06% du capital)
  - **swing** (entrée dip −0.776% → cible +2.225% / stop −1.112%, p_fill 56%, n_eff≈28.3) : P(cible|rempli) **44%** · **EV/risk +0.148** (×p_fill ; si rempli +0.29% du capital)
  - **deep** (entrée dip −1.196% → cible +3.147% / stop −1.573%, p_fill 63%, n_eff≈30.0) : P(cible|rempli) **39%** · **EV/risk +0.080** (×p_fill ; si rempli +0.20% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→72% · +1.0%→61% · +2.0%→36% · +3.0%→15% · +5.0%→5% · +8.0%→2%
- Range intraday médian 2.77% (p90 5.22%) · excursion haute méd. +1.22% / basse méd. −1.06%
- Profil de vol intra : ouverture 1.663% vs midi 0.667% vs clôture 0.784% _(ouverture ~2.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (139 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 35% · recovery-V 19%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; mean-reverting — autocorr -0.035)_ ; drift intra méd. 0.531% ; recovery-V 27%
- **σ réalisé intraday** 1.912% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 71% / bas 43% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 343.7575 (VA 341.9075–345.2375 ; dernier close 344.7)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 20% · rebond 59% · **stop −1.6%** sous le fill (sous le bruit) · cible +1.23% · R/R 0.77 (high win-rate)
- Gaps overnight (n=138) : méd. -0.06% · baisse 52% (gap-down >1% 14% · >2% 2%)
- Excursion ouverture 5min (n=139) : bas méd −0.37% (p90 −1.44%) · haut méd +0.25% · range méd 0.92%
- Excursion ouverture 15min (n=139) : bas méd −0.44% (p90 −1.62%) · haut méd +0.44% · range méd 1.19%
- Excursion ouverture 30min (n=139) : bas méd −0.51% (p90 −1.82%) · haut méd +0.57% · range méd 1.31%
- Excursion ouverture 60min (n=139) : bas méd −0.69% (p90 −1.95%) · haut méd +0.69% · range méd 1.52%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 344.7 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 67% (98/138) · gap 28% · délai 0.2min · rebond 38% (36/98) (MFE +0.78%)
   - −1.0% : fill 30min 41% · séance 50% (70/138) · gap 14% · délai 0.4min · rebond 42% (25/70) (MFE +0.58%)
   - −1.5% : fill 30min 28% · séance 43% (60/138) · gap 5% · délai 6.9min · rebond 38% (20/60) (MFE +0.89%)
   - −2.0% : fill 30min 14% · séance 32% (43/138) · gap 2% · délai 39.0min · rebond 48% (19/43) (MFE +0.91%)
   - −3.0% : fill 30min 5% · séance 20% (26/138) · gap 1% · délai 203.0min · rebond 59% (16/26) (MFE +1.23%)
   - −4.0% : fill 30min 3% · séance 9% (12/138) · gap 0% · délai 153.7min · rebond 53% (6/12) (MFE +1.49%)
   - −5.0% : fill 30min 0% · séance 2% (3/138) · gap 0% · délai 360.2min · rebond 31% (1/3) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.25% (p90 −0.94%) → stop au-delà de −0.77% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.19% (p90 −0.91%) → stop au-delà de −0.73% (survit 80% du bruit)
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
   - **gap-up** (52 séances) :
      · −1.0% : fill 23% (16/52) · rebond 26% (3/16)
      · −2.0% : fill 14% (9/52) · rebond 34% (3/9)
      · −3.0% : fill 11% (6/52) · rebond 55% (4/6)
      · −4.0% : fill 7% (3/52) · rebond 30% (1/3)
      · −5.0% : fill 2% (1/52) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=139) : 52% en base · 67% si les 15 1res min sont vertes (62 cas) · 36% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=139) : COUDE à **44min** → P(séance verte=clôture>ouverture) 79% si début vert vs 24% si rouge (base 52% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=63) : tient le vert **79%** · continue >prix actuel 63% ; creux résiduel méd -0.57% (q20 -1.44%) → **SL/trailing à −1.44%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.32% / q75 +1.79% → **scale +1.32% / runner +1.79%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **24%** (continue à baisser 47%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.5%** (au-delà de la MAE q10 -2.5%), cible rebond +0.92% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=139) : retour [-1.81% .. +1.79%] · haut q95 +2.55% · bas q05 -2.28%
   - 60min (n=139) : retour [-1.82% .. +2.4%] · haut q95 +3.08% · bas q05 -2.58%
   - 2h (n=139) : retour [-2.21% .. +2.35%] · haut q95 +3.39% · bas q05 -2.92%
   - 4h (n=139) : retour [-2.16% .. +2.7%] · haut q95 +3.48% · bas q05 -3.02%
   - 6h (n=139) : retour [-2.22% .. +3.47%] · haut q95 +3.73% · bas q05 -3.1%
   - session (n=139) : retour [-2.93% .. +3.65%] · haut q95 +4.16% · bas q05 -4.06%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.4% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.66%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.76 · part idiosyncratique 0.24
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 82.2  _(surachat)_
- **ADX** : 30.3  _(tendance etablie)_
- **MACD** : hist 1.86  _(pas de croisement recent)_
- **BB** : %B 0.88 · largeur 24.2%
- **ATR** : 9.37 (70.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.094  _(accumulation)_
- **Vol ratio** : 0.37  _(volume atone)_
- **Choppiness** : 37.2  _(marche directionnel)_
- **MA** : MA20 320.91 · MA50 297.2 · MA200 300.58  _(prix > MA20)_
- **Dist MA** : MA20 +9.2% · MA50 +17.9% · MA200 +16.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (96150 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
