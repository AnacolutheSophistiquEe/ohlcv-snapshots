# AL2SI

**Generated** : 2026-07-30T21:45:30.979501+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite high · €26.58  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €26.58 (+3.9% vs entrée) · entrée €25.59 · stop €24.61 · T1 €26.47 · R/R 0.9  
> ↳ P(T1 av. stop) 38 % _(réel 5 s)_ · EV/risk -0.086 _(réel 5 s)_ (GBM 0.01) · ¼-Kelly 0.021 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.82% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €25.41–€25.76 (mid €25.59)
- Spot actuel : €26.58 (+3.9% au-dessus de la zone — repli à attendre)
- Stop : €24.61 (stop swing_plan-based (-11.91%))
- Targets : T1 €26.47 · R/R 0.9 | T2 €27.35 · R/R 1.8 | T3 €28.23 · R/R 2.69
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €24.61


## Edge, scénarios & sizing

- EV/risk : 0.01 | EV/share : €0.009 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 46 % | T2 39 % | T3 39 %
- Kelly (position) : f* 0.086 | ¼-Kelly 0.021 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 15.2 | bear 78.8 | side 6.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 159.0 (= 6 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.744% → cible +3.443% / stop −3.819%, p_fill 70%, n_eff≈26.3) : P(cible|rempli) **38%** · **EV/risk -0.086** (×p_fill ; si rempli -0.47% du capital)
  - **swing** (entrée dip −8.234% → cible +7.7% / stop −4.006%, p_fill 53%, n_eff≈19.2) : P(cible|rempli) **30%** · **EV/risk -0.145** (×p_fill ; si rempli -1.10% du capital)
  - **deep** (entrée dip −12.728% → cible +10.89% / stop −5.445%, p_fill 53%, n_eff≈17.5) : P(cible|rempli) **8%** · **EV/risk -0.438** (×p_fill ; si rempli -4.49% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→78% · +2.0%→71% · +3.0%→61% · +5.0%→45% · +8.0%→22%
- Range intraday médian 8.62% (p90 22.19%) · excursion haute méd. +4.29% / basse méd. −4.31%
- Profil de vol intra : ouverture 5.839% vs midi 1.772% vs clôture 1.985% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (159 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 8% · trend ↑0%/↓1% ; spike-down 80% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.13 ; mean-reverting — autocorr -0.051)_ ; drift intra méd. -0.667% ; recovery-V 29%
- **σ réalisé intraday** 7.972% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 44% / bas 70% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 24.8188 (VA 24.2413–25.0113 ; dernier close 23.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 47% · rebond 90% · **stop −5.35%** sous le fill (sous le bruit) · cible +2.41% · R/R 0.45 (high win-rate)
- Gaps overnight (n=158) : méd. 0.21% · baisse 41% (gap-down >1% 22% · >2% 11%)
- Excursion ouverture 5min (n=159) : bas méd −1.3% (p90 −5.03%) · haut méd +1.02% · range méd 3.13%
- Excursion ouverture 15min (n=159) : bas méd −1.72% (p90 −5.95%) · haut méd +1.51% · range méd 4.48%
- Excursion ouverture 30min (n=159) : bas méd −1.94% (p90 −6.63%) · haut méd +2.13% · range méd 4.97%
- Excursion ouverture 60min (n=159) : bas méd −2.6% (p90 −7.2%) · haut méd +2.71% · range méd 6.28%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 23.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 84% (125/158) · gap 29% · délai 0.3min · rebond 67% (83/125) (MFE +3.33%)
   - −1.0% : fill 30min 62% · séance 82% (120/158) · gap 22% · délai 0.4min · rebond 70% (83/120) (MFE +2.59%)
   - −1.5% : fill 30min 56% · séance 78% (110/158) · gap 16% · délai 0.8min · rebond 72% (74/110) (MFE +2.2%)
   - −2.0% : fill 30min 49% · séance 71% (97/158) · gap 11% · délai 2.8min · rebond 66% (64/97) (MFE +1.9%)
   - −3.0% : fill 30min 38% · séance 60% (79/158) · gap 6% · délai 7.0min · rebond 85% (66/79) (MFE +2.24%)
   - −4.0% : fill 30min 30% · séance 51% (67/158) · gap 4% · délai 14.7min · rebond 76% (52/67) (MFE +2.61%)
   - −5.0% : fill 30min 20% · séance 47% (59/158) · gap 4% · délai 34.4min · rebond 90% (55/59) (MFE +2.41%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.99% (p90 −5.52%) → stop au-delà de −3.84% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.32% (p90 −5.53%) → stop au-delà de −3.99% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.25% (p90 −5.56%) → stop au-delà de −3.95% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1551 jambes) : jambe baissière méd −1.3% (p90 −3.6%) · ~21.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 98% (51/55) · rebond 66% (34/51)
      · −2.0% : fill 88% (44/55) · rebond 57% (27/44)
      · −3.0% : fill 82% (39/55) · rebond 82% (32/39)
      · −4.0% : fill 72% (34/55) · rebond 79% (28/34)
      · −5.0% : fill 65% (31/55) · rebond 84% (28/31)
   - **flat** (34 séances) :
      · −1.0% : fill 86% (27/34) · rebond 77% (21/27)
      · −2.0% : fill 74% (21/34) · rebond 83% (16/21)
      · −3.0% : fill 58% (15/34) · rebond 82% (13/15)
      · −4.0% : fill 51% (14/34) · rebond 84% (12/14)
      · −5.0% : fill 45% (12/34) · rebond 100% (12/12)
   - **gap-up** (69 séances) :
      · −1.0% : fill 69% (42/69) · rebond 69% (28/42)
      · −2.0% : fill 57% (32/69) · rebond 64% (21/32)
      · −3.0% : fill 45% (25/69) · rebond 91% (21/25)
      · −4.0% : fill 36% (19/69) · rebond 68% (12/19)
      · −5.0% : fill 35% (16/69) · rebond 89% (15/16)
- **P(clôture VERTE) selon le drive 15min** (n=159) : 44% en base · 55% si les 15 1res min sont vertes (76 cas) · 36% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=159) : COUDE à **44min** → P(séance verte=clôture>ouverture) 72% si début vert vs 20% si rouge (base 44% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 252min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **72%** · continue >prix actuel 53% ; creux résiduel méd -2.63% (q20 -5.6%) → **SL/trailing à −5.6%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.24% / q75 +5.03% → **scale +3.24% / runner +5.03%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **20%** (continue à baisser 49%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −10.21%** (au-delà de la MAE q10 -10.21%), cible rebond +2.82% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=159) : retour [-5.93% .. +6.35%] · haut q95 +8.29% · bas q05 -7.69%
   - 60min (n=159) : retour [-5.94% .. +9.08%] · haut q95 +9.79% · bas q05 -7.87%
   - 2h (n=159) : retour [-6.22% .. +9.93%] · haut q95 +10.86% · bas q05 -8.03%
   - 4h (n=159) : retour [-8.33% .. +9.94%] · haut q95 +12.36% · bas q05 -11.11%
   - 6h (n=159) : retour [-7.29% .. +14.11%] · haut q95 +15.37% · bas q05 -11.22%
   - session (n=159) : retour [-9.82% .. +13.36%] · haut q95 +16.26% · bas q05 -14.26%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.49%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 39.8  _(momentum baissier)_
- **ADX** : 24.6  _(pas de tendance nette)_
- **MACD** : hist 0.182  _(pas de croisement recent)_
- **BB** : %B 0.36 · largeur 58.4%
- **ATR** : 3.26 (77.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.203  _(distribution)_
- **Vol ratio** : 0.79  _(volume normal)_
- **Choppiness** : 66.0  _(marche en range (choppy))_
- **MA** : MA20 29.02 · MA50 37.18 · MA200 24.67  _(prix < MA20)_
- **Dist MA** : MA20 -8.4% · MA50 -28.5% · MA200 +7.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93871 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
