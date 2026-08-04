# AL2SI

**Generated** : 2026-08-04T21:46:01.627075+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite high · €25.54  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €25.54 (+3.0% vs entrée) · entrée €24.80 · stop €23.83 · T1 €25.64 · R/R 0.87  
> ↳ P(T1 av. stop) 31 % _(réel 5 s)_ · EV/risk -0.15 _(réel 5 s)_ (GBM -0.009) · ¼-Kelly 0.02 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.91% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €24.64–€24.97 (mid €24.80)
- Spot actuel : €25.54 (+3.0% au-dessus de la zone — repli à attendre)
- Stop : €23.83 (stop swing_plan-based (-17.57%))
- Targets : T1 €25.64 · R/R 0.87 | T2 €26.48 · R/R 1.73 | T3 €27.32 · R/R 2.6
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €23.83


## Edge, scénarios & sizing

- EV/risk : -0.009 | EV/share : €-0.009 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 46 % | T2 38 % | T3 38 %
- Kelly (position) : f* 0.078 | ¼-Kelly 0.02 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 16.0 | bear 78.1 | side 5.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 153.0 (= 6 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.878% → cible +3.384% / stop −3.915%, p_fill 81%, n_eff≈32.0) : P(cible|rempli) **31%** · **EV/risk -0.150** (×p_fill ; si rempli -0.72% du capital)
  - **swing** (entrée dip −6.329% → cible +7.568% / stop −12.0%, p_fill 60%, n_eff≈22.5) : P(cible|rempli) **56%** · **EV/risk -0.116** (×p_fill ; si rempli -2.32% du capital)
  - **deep** (entrée dip −9.78% → cible +10.702% / stop −18.0%, p_fill 55%, n_eff≈21.1) : P(cible|rempli) **39%** · **EV/risk -0.238** (×p_fill ; si rempli -7.74% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→78% · +2.0%→70% · +3.0%→60% · +5.0%→44% · +8.0%→21%
- Range intraday médian 8.95% (p90 22.19%) · excursion haute méd. +4.23% / basse méd. −4.75%
- Profil de vol intra : ouverture 5.79% vs midi 1.774% vs clôture 1.994% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 11% · trend ↑0%/↓1% ; spike-down 81% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.148 ; mean-reverting — autocorr -0.051)_ ; drift intra méd. -0.653% ; recovery-V 29%
- **σ réalisé intraday** 7.616% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 43% / bas 70% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 25.1762 (VA 24.5012–25.3113 ; dernier close 24.84)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 46% · rebond 86% · **stop −5.28%** sous le fill (sous le bruit) · cible +2.4% · R/R 0.45 (high win-rate)
- Gaps overnight (n=159) : méd. 0.21% · baisse 38% (gap-down >1% 21% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −1.42% (p90 −4.91%) · haut méd +1.04% · range méd 3.14%
- Excursion ouverture 15min (n=160) : bas méd −1.75% (p90 −5.86%) · haut méd +1.55% · range méd 4.44%
- Excursion ouverture 30min (n=160) : bas méd −1.8% (p90 −5.86%) · haut méd +2.33% · range méd 4.97%
- Excursion ouverture 60min (n=160) : bas méd −2.4% (p90 −6.97%) · haut méd +2.74% · range méd 6.31%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 24.84 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 85% (126/159) · gap 28% · délai 0.3min · rebond 67% (85/126) (MFE +3.21%)
   - −1.0% : fill 30min 61% · séance 83% (121/159) · gap 21% · délai 0.4min · rebond 67% (84/121) (MFE +2.52%)
   - −1.5% : fill 30min 55% · séance 79% (111/159) · gap 15% · délai 1.0min · rebond 70% (75/111) (MFE +2.15%)
   - −2.0% : fill 30min 46% · séance 71% (97/159) · gap 11% · délai 3.4min · rebond 62% (63/97) (MFE +1.79%)
   - −3.0% : fill 30min 36% · séance 60% (79/159) · gap 6% · délai 8.1min · rebond 80% (64/79) (MFE +2.05%)
   - −4.0% : fill 30min 28% · séance 52% (68/159) · gap 4% · délai 22.1min · rebond 75% (53/68) (MFE +2.49%)
   - −5.0% : fill 30min 19% · séance 46% (60/159) · gap 3% · délai 42.3min · rebond 86% (55/60) (MFE +2.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −1.04% (p90 −5.47%) → stop au-delà de −3.46% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.4% (p90 −5.5%) → stop au-delà de −3.95% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.41% (p90 −5.51%) → stop au-delà de −3.9% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1558 jambes) : jambe baissière méd −1.31% (p90 −3.6%) · ~21.0 jambes/séance
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
      · −1.0% : fill 71% (42/69) · rebond 62% (28/42)
      · −2.0% : fill 61% (32/69) · rebond 56% (20/32)
      · −3.0% : fill 49% (25/69) · rebond 76% (19/25)
      · −4.0% : fill 41% (20/69) · rebond 65% (13/20)
      · −5.0% : fill 36% (17/69) · rebond 79% (15/17)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 54% si les 15 1res min sont vertes (76 cas) · 34% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **44min** → P(séance verte=clôture>ouverture) 70% si début vert vs 19% si rouge (base 44% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 252min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **70%** · continue >prix actuel 53% ; creux résiduel méd -2.63% (q20 -5.92%) → **SL/trailing à −5.92%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.23% / q75 +5.93% → **scale +3.23% / runner +5.93%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **19%** (continue à baisser 50%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −10.08%** (au-delà de la MAE q10 -10.08%), cible rebond +2.6% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.8% .. +6.25%] · haut q95 +8.24% · bas q05 -7.67%
   - 60min (n=160) : retour [-5.93% .. +9.04%] · haut q95 +9.69% · bas q05 -7.86%
   - 2h (n=160) : retour [-6.2% .. +9.89%] · haut q95 +10.55% · bas q05 -8.03%
   - 4h (n=160) : retour [-8.04% .. +9.72%] · haut q95 +12.33% · bas q05 -10.98%
   - 6h (n=160) : retour [-6.84% .. +13.05%] · haut q95 +15.03% · bas q05 -11.17%
   - session (n=160) : retour [-9.03% .. +14.36%] · haut q95 +15.59% · bas q05 -13.25%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.42%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 43.6  _(momentum baissier)_
- **ADX** : 24.0  _(pas de tendance nette)_
- **MACD** : hist 0.21  _(pas de croisement recent)_
- **BB** : %B 0.32 · largeur 44.7%
- **ATR** : 3.24 (76.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.225  _(distribution)_
- **Vol ratio** : 0.35  _(volume atone)_
- **Choppiness** : 65.8  _(marche en range (choppy))_
- **MA** : MA20 27.75 · MA50 36.26 · MA200 24.78  _(prix < MA20)_
- **Dist MA** : MA20 -8.0% · MA50 -29.6% · MA200 +3.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93964 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
