# AL2SI

**Generated** : 2026-08-06T21:46:06.522125+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €27.82  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €27.82 (+4.9% vs entrée) · entrée €26.52 · stop €25.64 · T1 €27.38 · R/R 0.98  
> ↳ P(T1 av. stop) 33 % _(réel 5 s)_ · EV/risk -0.086 _(réel 5 s)_ (GBM -0.004) · ¼-Kelly 0.016 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.28% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €26.34–€26.69 (mid €26.52)
- Spot actuel : €27.82 (+4.9% au-dessus de la zone — repli à attendre)
- Stop : €25.64 (stop swing_plan-based (-20.75%))
- Targets : T1 €27.38 · R/R 0.98 | T2 €28.25 · R/R 1.97 | T3 €29.11 · R/R 2.94
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €25.64


## Edge, scénarios & sizing

- EV/risk : -0.004 | EV/share : €-0.003 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 45 % | T2 34 % | T3 34 %
- Kelly (position) : f* 0.064 | ¼-Kelly 0.016 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 56.1 | bear 28.5 | side 15.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 278.0 (= 10 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.691% → cible +3.267% / stop −3.283%, p_fill 57%, n_eff≈24.1) : P(cible|rempli) **33%** · **EV/risk -0.086** (×p_fill ; si rempli -0.49% du capital)
  - **swing** (entrée dip −10.321% → cible +7.306% / stop −11.629%, p_fill 39%, n_eff≈16.8) : P(cible|rempli) **59%** · **EV/risk -0.051** (×p_fill ; si rempli -1.54% du capital)
  - **deep** (entrée dip −15.951% → cible +10.332% / stop −18.0%, p_fill 41%, n_eff≈16.5) : P(cible|rempli) **66%** · **EV/risk -0.008** (×p_fill ; si rempli -0.37% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→78% · +2.0%→70% · +3.0%→60% · +5.0%→42% · +8.0%→19%
- Range intraday médian 8.62% (p90 22.19%) · excursion haute méd. +4.23% / basse méd. −4.75%
- Profil de vol intra : ouverture 5.684% vs midi 1.771% vs clôture 2.004% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 11% · trend ↑0%/↓1% ; spike-down 78% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.144 ; mean-reverting — autocorr -0.069)_ ; drift intra méd. -0.294% ; recovery-V 33%
- **σ réalisé intraday** 7.386% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 68% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 27.3185 (VA 26.9895–27.8825 ; dernier close 27.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 45% · rebond 86% · **stop −5.28%** sous le fill (sous le bruit) · cible +2.4% · R/R 0.45 (high win-rate)
- Gaps overnight (n=159) : méd. 0.21% · baisse 39% (gap-down >1% 22% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −1.36% (p90 −4.85%) · haut méd +1.04% · range méd 3.14%
- Excursion ouverture 15min (n=160) : bas méd −1.74% (p90 −5.86%) · haut méd +1.55% · range méd 4.26%
- Excursion ouverture 30min (n=160) : bas méd −1.76% (p90 −5.86%) · haut méd +2.33% · range méd 4.94%
- Excursion ouverture 60min (n=160) : bas méd −2.28% (p90 −6.96%) · haut méd +2.74% · range méd 6.24%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 27.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 84% (125/159) · gap 28% · délai 0.3min · rebond 68% (84/125) (MFE +3.33%)
   - −1.0% : fill 30min 61% · séance 82% (121/159) · gap 22% · délai 0.4min · rebond 68% (84/121) (MFE +2.59%)
   - −1.5% : fill 30min 54% · séance 78% (111/159) · gap 16% · délai 0.8min · rebond 71% (75/111) (MFE +2.21%)
   - −2.0% : fill 30min 45% · séance 68% (96/159) · gap 10% · délai 3.3min · rebond 62% (62/96) (MFE +1.79%)
   - −3.0% : fill 30min 34% · séance 58% (78/159) · gap 6% · délai 8.0min · rebond 80% (64/78) (MFE +2.05%)
   - −4.0% : fill 30min 27% · séance 50% (67/159) · gap 4% · délai 22.0min · rebond 75% (52/67) (MFE +2.49%)
   - −5.0% : fill 30min 18% · séance 45% (60/159) · gap 3% · délai 42.3min · rebond 86% (55/60) (MFE +2.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −1.04% (p90 −5.42%) → stop au-delà de −3.14% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.4% (p90 −5.46%) → stop au-delà de −3.9% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.41% (p90 −5.47%) → stop au-delà de −3.85% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1557 jambes) : jambe baissière méd −1.3% (p90 −3.54%) · ~21.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 99% (52/55) · rebond 68% (35/52)
      · −2.0% : fill 84% (44/55) · rebond 57% (27/44)
      · −3.0% : fill 77% (39/55) · rebond 82% (32/39)
      · −4.0% : fill 68% (34/55) · rebond 79% (28/34)
      · −5.0% : fill 61% (31/55) · rebond 84% (28/31)
   - **flat** (35 séances) :
      · −1.0% : fill 87% (28/35) · rebond 79% (22/28)
      · −2.0% : fill 68% (21/35) · rebond 83% (16/21)
      · −3.0% : fill 54% (15/35) · rebond 82% (13/15)
      · −4.0% : fill 48% (14/35) · rebond 84% (12/14)
      · −5.0% : fill 42% (12/35) · rebond 100% (12/12)
   - **gap-up** (69 séances) :
      · −1.0% : fill 68% (41/69) · rebond 61% (27/41)
      · −2.0% : fill 58% (31/69) · rebond 56% (19/31)
      · −3.0% : fill 47% (24/69) · rebond 76% (19/24)
      · −4.0% : fill 39% (19/69) · rebond 64% (12/19)
      · −5.0% : fill 35% (17/69) · rebond 79% (15/17)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 58% si les 15 1res min sont vertes (78 cas) · 35% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **3:06** → P(séance verte=clôture>ouverture) 85% si début vert vs 11% si rouge (base 46% · écart 74 pts) ; prédictivité sature ensuite (plafond brut 252min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **85%** · continue >prix actuel 60% ; creux résiduel méd -1.69% (q20 -3.66%) → **SL/trailing à −3.66%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.73% / q75 +5.88% → **scale +2.73% / runner +5.88%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **11%** (continue à baisser 64%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.25%** (au-delà de la MAE q10 -8.25%), cible rebond +1.27% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.71% .. +6.19%] · haut q95 +8.23% · bas q05 -7.65%
   - 60min (n=160) : retour [-5.92% .. +9.04%] · haut q95 +9.62% · bas q05 -7.85%
   - 2h (n=160) : retour [-6.18% .. +9.86%] · haut q95 +10.36% · bas q05 -8.02%
   - 4h (n=160) : retour [-7.84% .. +9.68%] · haut q95 +12.32% · bas q05 -10.9%
   - 6h (n=160) : retour [-6.82% .. +11.44%] · haut q95 +14.85% · bas q05 -11.13%
   - session (n=160) : retour [-8.51% .. +13.92%] · haut q95 +15.29% · bas q05 -12.56%


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
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 59.1  _(momentum haussier)_
- **ADX** : 21.2  _(pas de tendance nette)_
- **MACD** : hist 0.529  _(pas de croisement recent)_
- **BB** : %B 0.59 · largeur 29.8%
- **ATR** : 2.9 (70.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.169  _(distribution)_
- **Vol ratio** : 0.95  _(volume normal)_
- **Choppiness** : 61.7  _(transition)_
- **MA** : MA20 27.08 · MA50 35.44 · MA200 24.92  _(prix > MA20)_
- **Dist MA** : MA20 +2.7% · MA50 -21.5% · MA200 +11.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93684 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
