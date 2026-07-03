# AL2SI

**Generated** : 2026-07-03T21:43:08.121043+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 15.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite extreme · €36.32  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €36.32 (+2.4% vs entrée) · entrée €35.46 · stop €31.21 · T1 €50.24 · R/R 3.48  
> ↳ P(T1 av. stop) 11 % _(réel 5 s)_ · EV/risk -0.102 _(réel 5 s)_ (GBM 0.426) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €34.61–€36.32 (mid €35.46)
- Spot actuel : €36.32 (+2.4% au-dessus de la zone — repli à attendre)
- Stop : €31.21 (stop swing_plan-based (-14.07%))
- Targets : T1 €50.24 · R/R 3.48 | T2 €53.16 · R/R 4.16 | T3 €56.08 · R/R 4.85
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €31.21


## Edge, scénarios & sizing

- EV/risk : 0.426 | EV/share : €1.813 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 6 % | T2 3 % | T3 1 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 25.3 | bear 56.6 | side 18.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 254.0 (= 7 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.065% → cible +18.955% / stop −8.0%, p_fill 81%, n_eff≈32.8) : P(cible|rempli) **3%** · **EV/risk -0.104** (×p_fill ; si rempli -1.04% du capital)
  - **swing** (entrée dip −2.352% → cible +41.675% / stop −12.0%, p_fill 74%, n_eff≈27.7) : P(cible|rempli) **11%** · **EV/risk -0.102** (×p_fill ; si rempli -1.64% du capital)
  - **deep** (entrée dip −3.439% → cible +70.937% / stop −18.0%, p_fill 67%, n_eff≈24.3) : P(cible|rempli) **0%** · **EV/risk -0.330** (×p_fill ; si rempli -8.80% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→81% · +2.0%→76% · +3.0%→64% · +5.0%→40% · +8.0%→22%
- Range intraday médian 7.78% (p90 17.21%) · excursion haute méd. +4.16% / basse méd. −3.18%
- Profil de vol intra : ouverture 5.554% vs midi 1.677% vs clôture 1.949% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (140 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑0%/↓2% ; spike-down 72% · recovery-V 38%)_
- **Régime intraday** : **chop** _(efficiency 0.166 ; neutre — autocorr -0.02)_ ; drift intra méd. 1.235% ; recovery-V 34%
- **σ réalisé intraday** 8.576% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 64% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 37.975 (VA 36.985–38.065 ; dernier close 37.24)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 38% · rebond 88% · **stop −6.02%** sous le fill (sous le bruit) · cible +2.8% · R/R 0.47 (high win-rate)
- Gaps overnight (n=139) : méd. 0.21% · baisse 37% (gap-down >1% 23% · >2% 9%)
- Excursion ouverture 5min (n=140) : bas méd −0.94% (p90 −5.48%) · haut méd +1.24% · range méd 3.0%
- Excursion ouverture 15min (n=140) : bas méd −1.37% (p90 −5.88%) · haut méd +1.54% · range méd 4.02%
- Excursion ouverture 30min (n=140) : bas méd −1.51% (p90 −6.32%) · haut méd +2.04% · range méd 4.71%
- Excursion ouverture 60min (n=140) : bas méd −2.05% (p90 −7.08%) · haut méd +2.54% · range méd 5.58%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 37.24 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 77% (106/139) · gap 28% · délai 0.3min · rebond 67% (70/106) (MFE +2.67%)
   - −1.0% : fill 30min 56% · séance 75% (101/139) · gap 23% · délai 0.4min · rebond 71% (70/101) (MFE +2.56%)
   - −1.5% : fill 30min 48% · séance 69% (91/139) · gap 13% · délai 1.5min · rebond 66% (58/91) (MFE +1.84%)
   - −2.0% : fill 30min 40% · séance 59% (78/139) · gap 9% · délai 3.1min · rebond 65% (51/78) (MFE +1.65%)
   - −3.0% : fill 30min 29% · séance 50% (63/139) · gap 6% · délai 10.5min · rebond 79% (51/63) (MFE +2.33%)
   - −4.0% : fill 30min 22% · séance 42% (53/139) · gap 6% · délai 15.0min · rebond 75% (41/53) (MFE +2.75%)
   - −5.0% : fill 30min 20% · séance 38% (46/139) · gap 5% · délai 18.8min · rebond 88% (43/46) (MFE +2.8%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.63% (p90 −5.77%) → stop au-delà de −3.52% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.89% (p90 −5.78%) → stop au-delà de −4.27% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.64% (p90 −5.86%) → stop au-delà de −4.18% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1328 jambes) : jambe baissière méd −1.24% (p90 −3.26%) · ~19.5 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 97% (45/49) · rebond 66% (30/45)
      · −2.0% : fill 84% (38/49) · rebond 52% (23/38)
      · −3.0% : fill 81% (34/49) · rebond 74% (27/34)
      · −4.0% : fill 67% (29/49) · rebond 68% (23/29)
      · −5.0% : fill 63% (27/49) · rebond 77% (24/27)
   - **flat** (29 séances) :
      · −1.0% : fill 80% (22/29) · rebond 77% (17/22)
      · −2.0% : fill 60% (16/29) · rebond 84% (12/16)
      · −3.0% : fill 46% (11/29) · rebond 92% (10/11)
      · −4.0% : fill 46% (11/29) · rebond 94% (10/11)
      · −5.0% : fill 37% (9/29) · rebond 100% (9/9)
   - **gap-up** (61 séances) :
      · −1.0% : fill 56% (34/61) · rebond 73% (23/34)
      · −2.0% : fill 40% (24/61) · rebond 69% (16/24)
      · −3.0% : fill 29% (18/61) · rebond 80% (14/18)
      · −4.0% : fill 22% (13/61) · rebond 70% (8/13)
      · −5.0% : fill 20% (10/61) · rebond 100% (10/10)
- **P(clôture VERTE) selon le drive 15min** (n=140) : 52% en base · 67% si les 15 1res min sont vertes (68 cas) · 39% si rouges (72 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=140) : COUDE à **31min** → P(séance verte=clôture>ouverture) 78% si début vert vs 27% si rouge (base 52% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 209min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **78%** · continue >prix actuel 59% ; creux résiduel méd -2.04% (q20 -4.44%) → **SL/trailing à −4.44%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.7% / q75 +6.39% → **scale +3.7% / runner +6.39%**, sortie à la clôture
  - **si ROUGE au coude** (n=70) : edge inversé — récupère vert seulement **27%** (continue à baisser 58%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.52%** (au-delà de la MAE q10 -8.52%), cible rebond +2.37% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=140) : retour [-4.88% .. +9.46%] · haut q95 +9.96% · bas q05 -7.7%
   - 60min (n=140) : retour [-5.95% .. +11.06%] · haut q95 +11.25% · bas q05 -7.87%
   - 2h (n=140) : retour [-5.65% .. +10.8%] · haut q95 +12.7% · bas q05 -8.03%
   - 4h (n=140) : retour [-7.91% .. +13.44%] · haut q95 +14.32% · bas q05 -10.83%
   - 6h (n=140) : retour [-7.47% .. +15.43%] · haut q95 +21.17% · bas q05 -11.24%
   - session (n=140) : retour [-9.86% .. +21.23%] · haut q95 +24.09% · bas q05 -14.57%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.2%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 36.2  _(momentum baissier)_
- **ADX** : 25.1  _(tendance etablie)_
- **MACD** : hist 0.478  _(bullish_recent)_
- **BB** : %B 0.48 · largeur 115.8%
- **ATR** : 6.13 (98.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.014  _(neutre)_
- **Vol ratio** : 0.63  _(volume normal)_
- **Choppiness** : 35.4  _(marche directionnel)_
- **MA** : MA20 37.28 · MA50 40.88 · MA200 23.04  _(prix < MA20)_
- **Dist MA** : MA20 -2.6% · MA50 -11.2% · MA200 +57.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93349 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
