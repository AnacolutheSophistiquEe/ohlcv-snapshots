# EVT

**Generated** : 2026-08-03T21:38:54.083508+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €3.49  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €3.49 (+2.3% vs entrée) · entrée €3.41 · stop €3.29 · T1 €3.53 · R/R 1.0  
> ↳ P(T1 av. stop) 19 % _(réel 5 s)_ · EV/risk -0.005 _(réel 5 s)_ (GBM 0.016) · ¼-Kelly 0.006 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.5% cohérent avec le bruit 5 s (EV-optimal ≈ −3.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €3.39–€3.43 (mid €3.41)
- Spot actuel : €3.49 (+2.3% au-dessus de la zone — repli à attendre)
- Stop : €3.29 (stop swing_plan-based (-12.68%))
- Targets : T1 €3.53 · R/R 1.0 | T2 €3.65 · R/R 2.0 | T3 €3.77 · R/R 3.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €3.29


## Edge, scénarios & sizing

- EV/risk : 0.016 | EV/share : €0.002 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 21 % | T2 9 % | T3 9 %
- Kelly (position) : f* 0.025 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 22.0 | bear 70.7 | side 7.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.237% → cible +3.504% / stop −3.501%, p_fill 38%, n_eff≈14.8) : P(cible|rempli) **19%** · **EV/risk -0.005** (×p_fill ; si rempli -0.05% du capital)
  - **swing** (entrée dip −4.922% → cible +7.837% / stop −8.159%, p_fill 22%, n_eff≈9.3) : P(cible|rempli) **3%** · **EV/risk -0.052** (×p_fill ; si rempli -1.90% du capital)
  - **deep** (entrée dip −7.603% → cible +11.084% / stop −12.595%, p_fill 25%, n_eff≈8.2) : P(cible|rempli) **5%** · **EV/risk -0.103** (×p_fill ; si rempli -5.27% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→71% · +2.0%→46% · +3.0%→26% · +5.0%→9% · +8.0%→2%
- Range intraday médian 4.21% (p90 6.57%) · excursion haute méd. +1.75% / basse méd. −1.7%
- Profil de vol intra : ouverture 2.735% vs midi 1.205% vs clôture 1.252% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 96% · range 4% · trend ↑0%/↓0% ; spike-down 54% · recovery-V 38%)_
- **Régime intraday** : **chop** _(efficiency 0.078 ; mean-reverting — autocorr -0.138)_ ; drift intra méd. -0.302% ; recovery-V 36%
- **σ réalisé intraday** 3.43% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 64% / whipsaw 33%
- POC intraday (dernière séance, temps-au-prix) : 3.4891 (VA 3.4483–3.5027 ; dernier close 3.408)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.0%** sous le close veille · fill 75% · rebond 67% · **stop −3.18%** sous le fill (sous le bruit) · cible +1.6% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. 0.0% · baisse 48% (gap-down >1% 21% · >2% 9%)
- Excursion ouverture 5min (n=160) : bas méd −0.68% (p90 −2.57%) · haut méd +0.48% · range méd 1.43%
- Excursion ouverture 15min (n=160) : bas méd −0.85% (p90 −2.69%) · haut méd +0.79% · range méd 1.75%
- Excursion ouverture 30min (n=160) : bas méd −1.06% (p90 −2.8%) · haut méd +0.92% · range méd 2.06%
- Excursion ouverture 60min (n=160) : bas méd −1.11% (p90 −3.08%) · haut méd +0.95% · range méd 2.38%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.408 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 85% (133/159) · gap 30% · délai 0.2min · rebond 68% (88/133) (MFE +1.56%)
   - −1.0% : fill 30min 53% · séance 75% (119/159) · gap 21% · délai 0.6min · rebond 67% (77/119) (MFE +1.6%)
   - −1.5% : fill 30min 37% · séance 60% (100/159) · gap 15% · délai 2.5min · rebond 60% (64/100) (MFE +1.33%)
   - −2.0% : fill 30min 27% · séance 47% (80/159) · gap 9% · délai 14.8min · rebond 64% (53/80) (MFE +1.43%)
   - −3.0% : fill 30min 15% · séance 30% (56/159) · gap 5% · délai 30.4min · rebond 68% (42/56) (MFE +1.66%)
   - −4.0% : fill 30min 8% · séance 17% (30/159) · gap 2% · délai 35.3min · rebond 49% (18/30) (MFE +1.04%)
   - −5.0% : fill 30min 5% · séance 9% (17/159) · gap 2% · délai 5.0min · rebond 50% (11/17) (MFE +1.35%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.35% (p90 −2.52%) → stop au-delà de −1.48% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −1.92%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.62% (p90 −1.94%) → stop au-delà de −1.35% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=814 jambes) : jambe baissière méd −1.08% (p90 −2.32%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (62 séances) :
      · −1.0% : fill 95% (59/62) · rebond 71% (36/59)
      · −2.0% : fill 64% (44/62) · rebond 60% (28/44)
      · −3.0% : fill 38% (32/62) · rebond 68% (24/32)
      · −4.0% : fill 26% (20/62) · rebond 56% (14/20)
      · −5.0% : fill 16% (13/62) · rebond 57% (9/13)
   - **flat** (41 séances) :
      · −1.0% : fill 79% (32/41) · rebond 68% (24/32)
      · −2.0% : fill 53% (19/41) · rebond 68% (13/19)
      · −3.0% : fill 40% (12/41) · rebond 73% (9/12)
      · −4.0% : fill 17% (5/41) · rebond 20% (1/5)
      · −5.0% : fill 8% (3/41) · rebond 27% (1/3)
   - **gap-up** (56 séances) :
      · −1.0% : fill 50% (28/56) · rebond 59% (17/28)
      · −2.0% : fill 24% (17/56) · rebond 70% (12/17)
      · −3.0% : fill 14% (12/56) · rebond 57% (9/12)
      · −4.0% : fill 6% (5/56) · rebond 80% (3/5)
      · −5.0% : fill 1% (1/56) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 54% en base · 68% si les 15 1res min sont vertes (76 cas) · 42% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **6min** → P(séance verte=clôture>ouverture) 67% si début vert vs 42% si rouge (base 54% · écart 25 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **67%** · continue >prix actuel 48% ; creux résiduel méd -1.85% (q20 -3.13%) → **SL/trailing à −3.13%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.35% / q75 +2.2% → **scale +1.35% / runner +2.2%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **42%** (continue à baisser 43%) → **RÉDUIRE ~58%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.66%** (au-delà de la MAE q10 -4.66%), cible rebond +2.11% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.61% .. +2.44%] · haut q95 +3.51% · bas q05 -3.45%
   - 60min (n=160) : retour [-3.14% .. +3.21%] · haut q95 +4.42% · bas q05 -3.59%
   - 2h (n=160) : retour [-3.48% .. +3.22%] · haut q95 +4.58% · bas q05 -4.28%
   - 4h (n=160) : retour [-2.95% .. +3.09%] · haut q95 +4.58% · bas q05 -4.89%
   - 6h (n=160) : retour [-3.35% .. +3.26%] · haut q95 +4.89% · bas q05 -5.36%
   - session (n=160) : retour [-4.28% .. +4.1%] · haut q95 +6.03% · bas q05 -5.77%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.97%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 12.2  _(survente)_
- **ADX** : 40.6  _(tendance tres forte)_
- **MACD** : hist -0.008  _(pas de croisement recent)_
- **BB** : %B 0.34 · largeur 71.8%
- **ATR** : 0.27 (69.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF 0.044  _(neutre)_
- **Vol ratio** : 0.51  _(volume atone)_
- **Choppiness** : 64.1  _(marche en range (choppy))_
- **MA** : MA20 3.95 · MA50 4.52 · MA200 5.29  _(prix < MA20)_
- **Dist MA** : MA20 -11.6% · MA50 -22.9% · MA200 -34.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89816 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
