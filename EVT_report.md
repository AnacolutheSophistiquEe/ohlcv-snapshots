# EVT

**Generated** : 2026-08-01T21:24:07.095288+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 1/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €3.41  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €3.41 (+1.8% vs entrée) · entrée €3.35 · stop €3.24 · T1 €3.47 · R/R 1.09  
> ↳ P(T1 av. stop) 17 % _(réel 5 s)_ · EV/risk -0.035 _(réel 5 s)_ (GBM 0.01) · ¼-Kelly 0.004 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.5% cohérent avec le bruit 5 s (EV-optimal ≈ −3.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 1/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €3.33–€3.38 (mid €3.35)
- Spot actuel : €3.41 (+1.8% au-dessus de la zone — repli à attendre)
- Stop : €3.24 (stop swing_plan-based (-11.89%))
- Targets : T1 €3.47 · R/R 1.09 | T2 €3.59 · R/R 2.18 | T3 €3.71 · R/R 3.27
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €3.24


## Edge, scénarios & sizing

- EV/risk : 0.01 | EV/share : €0.001 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 21 % | T2 9 % | T3 9 %
- Kelly (position) : f* 0.018 | ¼-Kelly 0.004 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 21.1 | bear 71.6 | side 7.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.741% → cible +3.485% / stop −3.5%, p_fill 44%, n_eff≈18.3) : P(cible|rempli) **17%** · **EV/risk -0.035** (×p_fill ; si rempli -0.28% du capital)
  - **swing** (entrée dip −3.832% → cible +7.794% / stop −8.379%, p_fill 35%, n_eff≈12.8) : P(cible|rempli) **6%** · **EV/risk -0.091** (×p_fill ; si rempli -2.16% du capital)
  - **deep** (entrée dip −5.921% → cible +11.025% / stop −12.85%, p_fill 45%, n_eff≈15.3) : P(cible|rempli) **3%** · **EV/risk -0.211** (×p_fill ; si rempli -6.05% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→72% · +2.0%→46% · +3.0%→26% · +5.0%→9% · +8.0%→2%
- Range intraday médian 4.25% (p90 6.57%) · excursion haute méd. +1.75% / basse méd. −1.7%
- Profil de vol intra : ouverture 2.764% vs midi 1.194% vs clôture 1.246% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 96% · range 4% · trend ↑0%/↓0% ; spike-down 52% · recovery-V 40%)_
- **Régime intraday** : **chop** _(efficiency 0.077 ; mean-reverting — autocorr -0.133)_ ; drift intra méd. -0.144% ; recovery-V 41%
- **σ réalisé intraday** 3.529% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 62% / bas 65% / whipsaw 31%
- POC intraday (dernière séance, temps-au-prix) : 3.4951 (VA 3.4885–3.5193 ; dernier close 3.478)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 32% · rebond 68% · **stop −3.5%** sous le fill (sous le bruit) · cible +1.66% · R/R 0.47 (high win-rate)
- Gaps overnight (n=159) : méd. -0.01% · baisse 50% (gap-down >1% 22% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.61% (p90 −2.67%) · haut méd +0.61% · range méd 1.43%
- Excursion ouverture 15min (n=160) : bas méd −0.82% (p90 −2.75%) · haut méd +0.84% · range méd 1.76%
- Excursion ouverture 30min (n=160) : bas méd −1.06% (p90 −2.82%) · haut méd +0.95% · range méd 2.09%
- Excursion ouverture 60min (n=160) : bas méd −1.11% (p90 −3.17%) · haut méd +0.96% · range méd 2.38%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.478 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 85% (133/159) · gap 31% · délai 0.2min · rebond 67% (88/133) (MFE +1.57%)
   - −1.0% : fill 30min 53% · séance 74% (119/159) · gap 22% · délai 0.4min · rebond 66% (77/119) (MFE +1.6%)
   - −1.5% : fill 30min 39% · séance 60% (99/159) · gap 16% · délai 1.6min · rebond 62% (64/99) (MFE +1.39%)
   - −2.0% : fill 30min 28% · séance 47% (79/159) · gap 10% · délai 14.3min · rebond 63% (52/79) (MFE +1.42%)
   - −3.0% : fill 30min 15% · séance 32% (56/159) · gap 5% · délai 30.4min · rebond 68% (42/56) (MFE +1.66%)
   - −4.0% : fill 30min 8% · séance 17% (30/159) · gap 2% · délai 35.3min · rebond 49% (18/30) (MFE +1.04%)
   - −5.0% : fill 30min 5% · séance 9% (17/159) · gap 2% · délai 5.0min · rebond 50% (11/17) (MFE +1.35%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.35% (p90 −2.51%) → stop au-delà de −1.48% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −1.92%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.62% (p90 −1.94%) → stop au-delà de −1.35% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=815 jambes) : jambe baissière méd −1.08% (p90 −2.32%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (63 séances) :
      · −1.0% : fill 95% (60/63) · rebond 71% (37/60)
      · −2.0% : fill 64% (44/63) · rebond 60% (28/44)
      · −3.0% : fill 38% (32/63) · rebond 68% (24/32)
      · −4.0% : fill 26% (20/63) · rebond 56% (14/20)
      · −5.0% : fill 16% (13/63) · rebond 57% (9/13)
   - **flat** (42 séances) :
      · −1.0% : fill 79% (33/42) · rebond 68% (25/33)
      · −2.0% : fill 53% (19/42) · rebond 68% (13/19)
      · −3.0% : fill 40% (12/42) · rebond 73% (9/12)
      · −4.0% : fill 17% (5/42) · rebond 20% (1/5)
      · −5.0% : fill 8% (3/42) · rebond 27% (1/3)
   - **gap-up** (54 séances) :
      · −1.0% : fill 44% (26/54) · rebond 48% (15/26)
      · −2.0% : fill 21% (16/54) · rebond 61% (11/16)
      · −3.0% : fill 16% (12/54) · rebond 57% (9/12)
      · −4.0% : fill 7% (5/54) · rebond 80% (3/5)
      · −5.0% : fill 1% (1/54) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 56% en base · 68% si les 15 1res min sont vertes (77 cas) · 45% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **6min** → P(séance verte=clôture>ouverture) 70% si début vert vs 43% si rouge (base 56% · écart 26 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **70%** · continue >prix actuel 50% ; creux résiduel méd -1.84% (q20 -2.74%) → **SL/trailing à −2.74%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.39% / q75 +2.38% → **scale +1.39% / runner +2.38%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **43%** (continue à baisser 40%) → **RÉDUIRE ~57%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.72%** (au-delà de la MAE q10 -4.72%), cible rebond +2.12% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.74% .. +2.45%] · haut q95 +3.51% · bas q05 -3.48%
   - 60min (n=160) : retour [-3.18% .. +3.32%] · haut q95 +4.48% · bas q05 -3.66%
   - 2h (n=160) : retour [-3.49% .. +3.23%] · haut q95 +4.63% · bas q05 -4.29%
   - 4h (n=160) : retour [-3.0% .. +3.21%] · haut q95 +4.63% · bas q05 -5.29%
   - 6h (n=160) : retour [-3.41% .. +3.28%] · haut q95 +5.08% · bas q05 -5.41%
   - session (n=160) : retour [-4.36% .. +4.13%] · haut q95 +6.2% · bas q05 -5.86%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.98%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 10.3  _(survente)_
- **ADX** : 40.8  _(tendance tres forte)_
- **MACD** : hist -0.012  _(pas de croisement recent)_
- **BB** : %B 0.31 · largeur 72.1%
- **ATR** : 0.28 (72.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF 0.027  _(neutre)_
- **Vol ratio** : 0.55  _(volume atone)_
- **Choppiness** : 64.7  _(marche en range (choppy))_
- **MA** : MA20 3.94 · MA50 4.52 · MA200 5.29  _(prix < MA20)_
- **Dist MA** : MA20 -13.4% · MA50 -24.5% · MA200 -35.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90138 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
