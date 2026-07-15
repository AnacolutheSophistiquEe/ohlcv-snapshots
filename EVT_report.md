# EVT

**Generated** : 2026-07-15T21:39:15.449577+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €3.51  

> 🟡 **WAIT-FOR-DIP** — spot +9.3 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €3.51 (+9.3% vs entrée) · entrée €3.21 · stop €3.10 · T1 €3.32 · R/R 1.0  
> ↳ P(T1 av. stop) 25 % · EV/risk 0.061 · ¼-Kelly 0.01 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.5% cohérent avec le bruit 5 s (EV-optimal ≈ −3.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €3.19–€3.23 (mid €3.21)
- Spot actuel : €3.51 (+9.3% au-dessus de la zone — repli à attendre)
- Stop : €3.10 (stop swing_plan-based (-20.32%))
- Targets : T1 €3.32 · R/R 1.0 | T2 €3.44 · R/R 2.09 | T3 €3.55 · R/R 3.09
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €3.10


## Edge, scénarios & sizing

- EV/risk : 0.061 | EV/share : €0.007 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 25 % | T2 9 % | T3 9 %
- Kelly (position) : f* 0.039 | ¼-Kelly 0.01 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 18.3 | bear 30.1 | side 51.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→74% · +2.0%→48% · +3.0%→30% · +5.0%→9% · +8.0%→2%
- Range intraday médian 4.43% (p90 6.71%) · excursion haute méd. +1.98% / basse méd. −1.7%
- Profil de vol intra : ouverture 2.673% vs midi 1.197% vs clôture 1.237% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 95% · range 5% · trend ↑0%/↓0% ; spike-down 52% · recovery-V 41%)_
- **Régime intraday** : **chop** _(efficiency 0.086 ; mean-reverting — autocorr -0.115)_ ; drift intra méd. 0.168% ; recovery-V 46%
- **σ réalisé intraday** 2.959% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 65% / whipsaw 30%
- POC intraday (dernière séance, temps-au-prix) : 4.9802 (VA 4.8986–5.0312 ; dernier close 4.902)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 30% · rebond 70% · **stop −2.37%** sous le fill (sous le bruit) · cible +1.87% · R/R 0.79 (high win-rate)
- Gaps overnight (n=159) : méd. -0.04% · baisse 51% (gap-down >1% 21% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.58% (p90 −2.07%) · haut méd +0.7% · range méd 1.38%
- Excursion ouverture 15min (n=160) : bas méd −0.78% (p90 −2.58%) · haut méd +0.86% · range méd 1.76%
- Excursion ouverture 30min (n=160) : bas méd −0.83% (p90 −2.75%) · haut méd +0.98% · range méd 2.2%
- Excursion ouverture 60min (n=160) : bas méd −0.91% (p90 −2.83%) · haut méd +1.0% · range méd 2.36%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 4.902 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 83% (132/159) · gap 33% · délai 0.3min · rebond 65% (87/132) (MFE +1.4%)
   - −1.0% : fill 30min 51% · séance 76% (120/159) · gap 21% · délai 1.3min · rebond 68% (78/120) (MFE +1.56%)
   - −1.5% : fill 30min 35% · séance 58% (97/159) · gap 16% · délai 10.8min · rebond 63% (61/97) (MFE +1.48%)
   - −2.0% : fill 30min 28% · séance 48% (78/159) · gap 10% · délai 15.1min · rebond 62% (50/78) (MFE +1.41%)
   - −3.0% : fill 30min 13% · séance 30% (55/159) · gap 5% · délai 31.3min · rebond 70% (42/55) (MFE +1.87%)
   - −4.0% : fill 30min 6% · séance 18% (30/159) · gap 1% · délai 65.4min · rebond 59% (19/30) (MFE +1.42%)
   - −5.0% : fill 30min 3% · séance 8% (17/159) · gap 0% · délai 63.2min · rebond 75% (12/17) (MFE +2.03%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.35% (p90 −1.97%) → stop au-delà de −1.46% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.41% (p90 −1.84%) → stop au-delà de −1.35% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.61% (p90 −1.69%) → stop au-delà de −1.3% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=791 jambes) : jambe baissière méd −1.05% (p90 −2.33%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (64 séances) :
      · −1.0% : fill 94% (61/64) · rebond 70% (37/61)
      · −2.0% : fill 67% (45/64) · rebond 61% (28/45)
      · −3.0% : fill 42% (34/64) · rebond 76% (26/34)
      · −4.0% : fill 27% (21/64) · rebond 65% (15/21)
      · −5.0% : fill 15% (14/64) · rebond 74% (10/14)
   - **flat** (40 séances) :
      · −1.0% : fill 86% (31/40) · rebond 75% (24/31)
      · −2.0% : fill 46% (16/40) · rebond 63% (11/16)
      · −3.0% : fill 27% (9/40) · rebond 69% (7/9)
      · −4.0% : fill 17% (4/40) · rebond 30% (1/4)
      · −5.0% : fill 5% (2/40) · rebond 72% (1/2)
   - **gap-up** (55 séances) :
      · −1.0% : fill 46% (28/55) · rebond 56% (17/28)
      · −2.0% : fill 25% (17/55) · rebond 60% (11/17)
      · −3.0% : fill 18% (12/55) · rebond 57% (9/12)
      · −4.0% : fill 8% (5/55) · rebond 80% (3/5)
      · −5.0% : fill 1% (1/55) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 58% en base · 67% si les 15 1res min sont vertes (78 cas) · 49% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:05** → P(séance verte=clôture>ouverture) 79% si début vert vs 34% si rouge (base 58% · écart 44 pts) ; prédictivité sature ensuite (plafond brut 286min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **79%** · continue >prix actuel 58% ; creux résiduel méd -1.45% (q20 -2.66%) → **SL/trailing à −2.66%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.17% / q75 +2.67% → **scale +1.17% / runner +2.67%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **34%** (continue à baisser 48%) → **RÉDUIRE ~66%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.72%** (au-delà de la MAE q10 -3.72%), cible rebond +1.5% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.35% .. +2.41%] · haut q95 +3.59% · bas q05 -2.85%
   - 60min (n=160) : retour [-2.76% .. +2.92%] · haut q95 +4.25% · bas q05 -3.29%
   - 2h (n=160) : retour [-2.99% .. +3.12%] · haut q95 +4.44% · bas q05 -3.63%
   - 4h (n=160) : retour [-2.88% .. +2.92%] · haut q95 +4.44% · bas q05 -3.92%
   - 6h (n=160) : retour [-3.33% .. +3.22%] · haut q95 +4.59% · bas q05 -4.31%
   - session (n=160) : retour [-4.14% .. +4.05%] · haut q95 +5.58% · bas q05 -5.29%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.9%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
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

- **RSI** : 19.2  _(survente)_
- **ADX** : 22.5  _(pas de tendance nette)_
- **MACD** : hist -0.137  _(bearish_recent)_
- **BB** : %B -0.24 · largeur 36.2%
- **ATR** : 0.3 (83.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.215  _(accumulation)_
- **Vol ratio** : 3.54  _(volume au-dessus de la moyenne)_
- **Choppiness** : 26.8  _(marche directionnel)_
- **MA** : MA20 4.78 · MA50 4.88 · MA200 5.48  _(prix < MA20)_
- **Dist MA** : MA20 -26.7% · MA50 -28.1% · MA200 -36.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88696 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
