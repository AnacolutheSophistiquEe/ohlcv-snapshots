# AL2SI

**Generated** : 2026-07-03T00:08:57.943832+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 15.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite extreme · €37.50  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €37.50 (+1.7% vs entrée) · entrée €36.88 · stop €33.95 · T1 €42.74 · R/R 2.0  
> ↳ P(T1 av. stop) 3 % _(réel 5 s)_ · EV/risk -0.086 _(réel 5 s)_ (GBM 0.055) · ¼-Kelly 0.083 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −7.95% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €36.42–€37.34 (mid €36.88)
- Spot actuel : €37.50 (+1.7% au-dessus de la zone — repli à attendre)
- Stop : €33.95 (stop swing_plan-based (-15.2%))
- Targets : T1 €42.74 · R/R 2.0 | T2 €44.63 · R/R 2.65 | T3 €46.52 · R/R 3.29
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €33.95


## Edge, scénarios & sizing

- EV/risk : 0.055 | EV/share : €0.161 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 39 % | T3 39 %
- Kelly (position) : f* 0.334 | ¼-Kelly 0.083 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 16.5 | bear 37.6 | side 45.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 262.0 (= 7 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.652% → cible +15.899% / stop −7.949%, p_fill 74%, n_eff≈28.8) : P(cible|rempli) **3%** · **EV/risk -0.086** (×p_fill ; si rempli -0.93% du capital)
  - **swing** (entrée dip −3.636% → cible +39.044% / stop −12.0%, p_fill 58%, n_eff≈20.6) : P(cible|rempli) **7%** · **EV/risk -0.255** (×p_fill ; si rempli -5.29% du capital)
  - **deep** (entrée dip −5.622% → cible +69.389% / stop −18.0%, p_fill 61%, n_eff≈21.0) : P(cible|rempli) **0%** · **EV/risk -0.309** (×p_fill ; si rempli -9.15% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→80% · +2.0%→75% · +3.0%→64% · +5.0%→40% · +8.0%→22%
- Range intraday médian 7.53% (p90 17.21%) · excursion haute méd. +4.16% / basse méd. −3.18%
- Profil de vol intra : ouverture 5.472% vs midi 1.671% vs clôture 1.951% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (139 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 12% · trend ↑0%/↓2% ; spike-down 71% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.169 ; neutre — autocorr -0.013)_ ; drift intra méd. 1.512% ; recovery-V 36%
- **σ réalisé intraday** 8.635% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 62% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 35.8275 (VA 35.2125–37.4675 ; dernier close 37.2)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 39% · rebond 88% · **stop −6.02%** sous le fill (sous le bruit) · cible +2.8% · R/R 0.47 (high win-rate)
- Gaps overnight (n=138) : méd. 0.21% · baisse 38% (gap-down >1% 23% · >2% 9%)
- Excursion ouverture 5min (n=139) : bas méd −0.91% (p90 −5.52%) · haut méd +1.05% · range méd 2.98%
- Excursion ouverture 15min (n=139) : bas méd −1.34% (p90 −5.91%) · haut méd +1.51% · range méd 3.94%
- Excursion ouverture 30min (n=139) : bas méd −1.48% (p90 −6.59%) · haut méd +1.8% · range méd 4.69%
- Excursion ouverture 60min (n=139) : bas méd −2.0% (p90 −6.94%) · haut méd +2.64% · range méd 5.48%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 37.2 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 77% (105/138) · gap 28% · délai 0.2min · rebond 66% (69/105) (MFE +2.42%)
   - −1.0% : fill 30min 57% · séance 74% (100/138) · gap 23% · délai 0.4min · rebond 70% (69/100) (MFE +2.46%)
   - −1.5% : fill 30min 49% · séance 68% (90/138) · gap 14% · délai 1.3min · rebond 65% (57/90) (MFE +1.75%)
   - −2.0% : fill 30min 41% · séance 58% (77/138) · gap 9% · délai 2.8min · rebond 64% (50/77) (MFE +1.64%)
   - −3.0% : fill 30min 29% · séance 51% (63/138) · gap 6% · délai 10.5min · rebond 79% (51/63) (MFE +2.33%)
   - −4.0% : fill 30min 23% · séance 43% (53/138) · gap 6% · délai 15.0min · rebond 75% (41/53) (MFE +2.75%)
   - −5.0% : fill 30min 20% · séance 39% (46/138) · gap 5% · délai 18.8min · rebond 88% (43/46) (MFE +2.8%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.61% (p90 −5.81%) → stop au-delà de −3.6% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.81% (p90 −5.82%) → stop au-delà de −4.17% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.64% (p90 −5.86%) → stop au-delà de −4.18% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1313 jambes) : jambe baissière méd −1.24% (p90 −3.25%) · ~19.0 jambes/séance
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
   - **gap-up** (60 séances) :
      · −1.0% : fill 54% (33/60) · rebond 71% (22/33)
      · −2.0% : fill 38% (23/60) · rebond 66% (15/23)
      · −3.0% : fill 30% (18/60) · rebond 80% (14/18)
      · −4.0% : fill 23% (13/60) · rebond 70% (8/13)
      · −5.0% : fill 21% (10/60) · rebond 100% (10/10)
- **P(clôture VERTE) selon le drive 15min** (n=139) : 53% en base · 67% si les 15 1res min sont vertes (68 cas) · 40% si rouges (71 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=139) : COUDE à **31min** → P(séance verte=clôture>ouverture) 78% si début vert vs 28% si rouge (base 53% · écart 50 pts) ; prédictivité sature ensuite (plafond brut 209min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **78%** · continue >prix actuel 59% ; creux résiduel méd -2.04% (q20 -4.44%) → **SL/trailing à −4.44%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.7% / q75 +6.39% → **scale +3.7% / runner +6.39%**, sortie à la clôture
  - **si ROUGE au coude** (n=69) : edge inversé — récupère vert seulement **28%** (continue à baisser 56%) → **RÉDUIRE ~72%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.69%** (au-delà de la MAE q10 -8.69%), cible rebond +2.27% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=139) : retour [-4.9% .. +9.46%] · haut q95 +9.96% · bas q05 -7.71%
   - 60min (n=139) : retour [-5.4% .. +11.23%] · haut q95 +11.44% · bas q05 -7.89%
   - 2h (n=139) : retour [-5.26% .. +11.1%] · haut q95 +13.12% · bas q05 -8.06%
   - 4h (n=139) : retour [-8.07% .. +13.54%] · haut q95 +14.54% · bas q05 -10.93%
   - 6h (n=139) : retour [-7.61% .. +15.52%] · haut q95 +21.33% · bas q05 -11.25%
   - session (n=139) : retour [-9.9% .. +21.25%] · haut q95 +24.42% · bas q05 -14.81%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.19%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 37.3  _(momentum baissier)_
- **ADX** : 26.8  _(tendance etablie)_
- **MACD** : hist 0.141  _(bullish_recent)_
- **BB** : %B 0.49 · largeur 117.5%
- **ATR** : 6.09 (98.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.029  _(neutre)_
- **Vol ratio** : 0.52  _(volume atone)_
- **Choppiness** : 33.2  _(marche directionnel)_
- **MA** : MA20 37.94 · MA50 40.98 · MA200 22.9  _(prix < MA20)_
- **Dist MA** : MA20 -1.2% · MA50 -8.5% · MA200 +63.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93247 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
