# AL2SI

**Generated** : 2026-08-04T00:10:36.296420+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite high · €24.84  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €24.84 (+5.2% vs entrée) · entrée €23.61 · stop €20.77 · T1 €25.31 · R/R 0.6  
> ↳ P(T1 av. stop) 54 % _(réel 5 s)_ · EV/risk -0.136 _(réel 5 s)_ (GBM 0.112) · ¼-Kelly 0.032 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €23.27–€23.95 (mid €23.61)
- Spot actuel : €24.84 (+5.2% au-dessus de la zone — repli à attendre)
- Stop : €20.77 (stop swing_plan-based (-16.36%))
- Targets : T1 €25.31 · R/R 0.6 | T2 €27.01 · R/R 1.2 | T3 €28.71 · R/R 1.8
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €20.77


## Edge, scénarios & sizing

- EV/risk : 0.112 | EV/share : €0.316 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 59 % | T2 34 % | T3 21 %
- Kelly (position) : f* 0.128 | ¼-Kelly 0.032 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 30.8 | bear 64.2 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 149.0 (= 6 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.255% → cible +3.219% / stop −4.22%, p_fill 80%, n_eff≈31.8) : P(cible|rempli) **34%** · **EV/risk -0.136** (×p_fill ; si rempli -0.72% du capital)
  - **swing** (entrée dip −4.954% → cible +7.198% / stop −12.0%, p_fill 67%, n_eff≈26.0) : P(cible|rempli) **54%** · **EV/risk -0.136** (×p_fill ; si rempli -2.43% du capital)
  - **deep** (entrée dip −7.671% → cible +10.179% / stop −18.0%, p_fill 67%, n_eff≈25.5) : P(cible|rempli) **43%** · **EV/risk -0.274** (×p_fill ; si rempli -7.41% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→78% · +2.0%→71% · +3.0%→61% · +5.0%→45% · +8.0%→22%
- Range intraday médian 8.95% (p90 22.19%) · excursion haute méd. +4.29% / basse méd. −4.64%
- Profil de vol intra : ouverture 5.816% vs midi 1.788% vs clôture 1.998% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 10% · trend ↑0%/↓1% ; spike-down 81% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.142 ; mean-reverting — autocorr -0.048)_ ; drift intra méd. -0.35% ; recovery-V 31%
- **σ réalisé intraday** 7.754% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 68% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 26.975 (VA 26.885–27.965 ; dernier close 25.66)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 47% · rebond 86% · **stop −5.28%** sous le fill (sous le bruit) · cible +2.4% · R/R 0.45 (high win-rate)
- Gaps overnight (n=159) : méd. 0.21% · baisse 39% (gap-down >1% 22% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −1.41% (p90 −4.95%) · haut méd +1.03% · range méd 3.13%
- Excursion ouverture 15min (n=160) : bas méd −1.75% (p90 −5.86%) · haut méd +1.53% · range méd 4.47%
- Excursion ouverture 30min (n=160) : bas méd −1.77% (p90 −6.1%) · haut méd +2.35% · range méd 4.97%
- Excursion ouverture 60min (n=160) : bas méd −2.34% (p90 −7.02%) · haut méd +2.83% · range méd 6.44%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 25.66 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 85% (126/159) · gap 28% · délai 0.3min · rebond 68% (85/126) (MFE +3.33%)
   - −1.0% : fill 30min 62% · séance 83% (121/159) · gap 22% · délai 0.4min · rebond 69% (84/121) (MFE +2.59%)
   - −1.5% : fill 30min 55% · séance 79% (111/159) · gap 15% · délai 0.8min · rebond 72% (75/111) (MFE +2.2%)
   - −2.0% : fill 30min 47% · séance 70% (97/159) · gap 11% · délai 3.1min · rebond 64% (63/97) (MFE +1.88%)
   - −3.0% : fill 30min 36% · séance 60% (79/159) · gap 6% · délai 7.5min · rebond 82% (65/79) (MFE +2.18%)
   - −4.0% : fill 30min 29% · séance 51% (67/159) · gap 4% · délai 18.8min · rebond 74% (52/67) (MFE +2.52%)
   - −5.0% : fill 30min 20% · séance 47% (60/159) · gap 4% · délai 42.3min · rebond 86% (55/60) (MFE +2.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −1.06% (p90 −5.49%) → stop au-delà de −3.6% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.4% (p90 −5.5%) → stop au-delà de −3.95% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.41% (p90 −5.51%) → stop au-delà de −3.9% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1558 jambes) : jambe baissière méd −1.3% (p90 −3.61%) · ~21.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 98% (51/55) · rebond 66% (34/51)
      · −2.0% : fill 88% (44/55) · rebond 57% (27/44)
      · −3.0% : fill 82% (39/55) · rebond 82% (32/39)
      · −4.0% : fill 72% (34/55) · rebond 79% (28/34)
      · −5.0% : fill 65% (31/55) · rebond 84% (28/31)
   - **flat** (35 séances) :
      · −1.0% : fill 87% (28/35) · rebond 79% (22/28)
      · −2.0% : fill 68% (21/35) · rebond 83% (16/21)
      · −3.0% : fill 54% (15/35) · rebond 82% (13/15)
      · −4.0% : fill 48% (14/35) · rebond 84% (12/14)
      · −5.0% : fill 42% (12/35) · rebond 100% (12/12)
   - **gap-up** (69 séances) :
      · −1.0% : fill 70% (42/69) · rebond 65% (28/42)
      · −2.0% : fill 59% (32/69) · rebond 60% (20/32)
      · −3.0% : fill 47% (25/69) · rebond 83% (20/25)
      · −4.0% : fill 39% (19/69) · rebond 61% (12/19)
      · −5.0% : fill 38% (17/69) · rebond 79% (15/17)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 54% si les 15 1res min sont vertes (77 cas) · 36% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **44min** → P(séance verte=clôture>ouverture) 70% si début vert vs 20% si rouge (base 44% · écart 50 pts) ; prédictivité sature ensuite (plafond brut 252min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **70%** · continue >prix actuel 53% ; creux résiduel méd -2.63% (q20 -5.92%) → **SL/trailing à −5.92%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.23% / q75 +5.93% → **scale +3.23% / runner +5.93%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **20%** (continue à baisser 49%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −10.21%** (au-delà de la MAE q10 -10.21%), cible rebond +2.82% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.84% .. +6.28%] · haut q95 +8.24% · bas q05 -7.68%
   - 60min (n=160) : retour [-5.93% .. +9.04%] · haut q95 +9.73% · bas q05 -7.86%
   - 2h (n=160) : retour [-6.21% .. +9.9%] · haut q95 +10.65% · bas q05 -8.03%
   - 4h (n=160) : retour [-8.13% .. +9.77%] · haut q95 +12.34% · bas q05 -11.03%
   - 6h (n=160) : retour [-6.9% .. +13.83%] · haut q95 +15.12% · bas q05 -11.19%
   - session (n=160) : retour [-9.4% .. +14.57%] · haut q95 +15.73% · bas q05 -13.59%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.42%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 41.4  _(momentum baissier)_
- **ADX** : 22.9  _(pas de tendance nette)_
- **MACD** : hist 0.207  _(pas de croisement recent)_
- **BB** : %B 0.26 · largeur 44.4%
- **ATR** : 3.42 (82.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.25  _(distribution)_
- **Vol ratio** : 0.64  _(volume normal)_
- **Choppiness** : 67.8  _(marche en range (choppy))_
- **MA** : MA20 27.77 · MA50 36.27 · MA200 24.78  _(prix < MA20)_
- **Dist MA** : MA20 -10.5% · MA50 -31.5% · MA200 +0.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93309 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
