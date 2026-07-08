# SMR

**Generated** : 2026-07-08T00:21:09.203624+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $8.96  

> 🟡 **WAIT-FOR-DIP** — spot +10.9 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $8.96 (+10.9% vs entrée) · entrée $8.08 · stop $7.81 · T1 $8.32 · R/R 0.89  
> ↳ P(T1 av. stop) 50 % · EV/risk 0.018 · ¼-Kelly 0.018 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.27% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $8.03–$8.13 (mid $8.08)
- Spot actuel : $8.96 (+10.9% au-dessus de la zone — repli à attendre)
- Stop : $7.81 (stop swing_plan-based (-22.64%))
- Targets : T1 $8.32 · R/R 0.89 | T2 $8.56 · R/R 1.78 | T3 $8.80 · R/R 2.67
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $7.81


## Edge, scénarios & sizing

- EV/risk : 0.018 | EV/share : $0.005 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 50 % | T2 34 % | T3 34 %
- Kelly (position) : f* 0.073 | ¼-Kelly 0.018 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 25.6 | bear 14.5 | side 59.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=8, n_eff=5))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→79% · +2.0%→68% · +3.0%→55% · +5.0%→38% · +8.0%→18%
- Range intraday médian 7.26% (p90 12.61%) · excursion haute méd. +3.45% / basse méd. −3.16%
- Profil de vol intra : ouverture 4.918% vs midi 1.555% vs clôture 1.754% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 74% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.116 ; neutre — autocorr 0.016)_ ; drift intra méd. -0.086% ; recovery-V 17%
- **σ réalisé intraday** 5.198% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 50% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 9.8651 (VA 9.6412–9.9351 ; dernier close 9.6)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 60% · rebond 76% · **stop −6.48%** sous le fill (sous le bruit) · cible +2.82% · R/R 0.44 (high win-rate)
- Gaps overnight (n=159) : méd. -0.63% · baisse 60% (gap-down >1% 41% · >2% 27%)
- Excursion ouverture 5min (n=160) : bas méd −1.23% (p90 −3.44%) · haut méd +1.08% · range méd 2.84%
- Excursion ouverture 15min (n=160) : bas méd −1.62% (p90 −3.96%) · haut méd +1.48% · range méd 3.86%
- Excursion ouverture 30min (n=160) : bas méd −1.84% (p90 −5.31%) · haut méd +2.14% · range méd 4.45%
- Excursion ouverture 60min (n=160) : bas méd −2.1% (p90 −6.04%) · haut méd +2.65% · range méd 5.63%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 9.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 75% · séance 82% (131/159) · gap 52% · délai 0.0min · rebond 68% (82/131) (MFE +2.01%)
   - −1.0% : fill 30min 68% · séance 79% (126/159) · gap 41% · délai 0.0min · rebond 68% (84/126) (MFE +1.95%)
   - −1.5% : fill 30min 64% · séance 76% (120/159) · gap 37% · délai 0.0min · rebond 76% (88/120) (MFE +2.21%)
   - −2.0% : fill 30min 60% · séance 70% (114/159) · gap 27% · délai 0.2min · rebond 70% (83/114) (MFE +2.54%)
   - −3.0% : fill 30min 48% · séance 60% (101/159) · gap 13% · délai 2.3min · rebond 76% (82/101) (MFE +2.82%)
   - −4.0% : fill 30min 38% · séance 54% (85/159) · gap 6% · délai 9.3min · rebond 73% (65/85) (MFE +2.7%)
   - −5.0% : fill 30min 24% · séance 41% (62/159) · gap 4% · délai 17.7min · rebond 73% (46/62) (MFE +1.98%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.8% (p90 −2.73%) → stop au-delà de −2.09% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.02% (p90 −3.12%) → stop au-delà de −2.16% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.1% (p90 −3.65%) → stop au-delà de −2.3% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1190 jambes) : jambe baissière méd −1.39% (p90 −3.19%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (84 séances) :
      · −1.0% : fill 100% (84/84) · rebond 73% (56/84)
      · −2.0% : fill 92% (80/84) · rebond 77% (60/80)
      · −3.0% : fill 83% (76/84) · rebond 81% (63/76)
      · −4.0% : fill 74% (65/84) · rebond 79% (53/65)
      · −5.0% : fill 56% (46/84) · rebond 81% (37/46)
   - **flat** (14 séances) :
      · −1.0% : fill 76% (11/14) · rebond 42% (7/11)
      · −2.0% : fill 63% (9/14) · rebond 30% (5/9)
      · −3.0% : fill 60% (7/14) · rebond 29% (4/7)
      · −4.0% : fill 60% (7/14) · rebond 40% (3/7)
      · −5.0% : fill 46% (5/14) · rebond 70% (4/5)
   - **gap-up** (61 séances) :
      · −1.0% : fill 49% (31/61) · rebond 64% (21/31)
      · −2.0% : fill 38% (25/61) · rebond 63% (18/25)
      · −3.0% : fill 28% (18/61) · rebond 77% (15/18)
      · −4.0% : fill 24% (13/61) · rebond 67% (9/13)
      · −5.0% : fill 18% (11/61) · rebond 41% (5/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 56% si les 15 1res min sont vertes (67 cas) · 35% si rouges (93 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:25** → P(séance verte=clôture>ouverture) 78% si début vert vs 13% si rouge (base 44% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 233min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **78%** · continue >prix actuel 47% ; creux résiduel méd -2.33% (q20 -4.03%) → **SL/trailing à −4.03%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.21% / q75 +4.24% → **scale +2.21% / runner +4.24%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **13%** (continue à baisser 57%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.28%** (au-delà de la MAE q10 -6.28%), cible rebond +1.45% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.67% .. +4.91%] · haut q95 +6.59% · bas q05 -6.69%
   - 60min (n=160) : retour [-6.42% .. +5.82%] · haut q95 +8.35% · bas q05 -7.96%
   - 2h (n=160) : retour [-7.93% .. +9.08%] · haut q95 +11.38% · bas q05 -9.07%
   - 4h (n=160) : retour [-8.81% .. +8.4%] · haut q95 +11.38% · bas q05 -10.73%
   - 6h (n=160) : retour [-8.63% .. +8.76%] · haut q95 +11.61% · bas q05 -10.85%
   - session (n=160) : retour [-8.46% .. +10.86%] · haut q95 +11.74% · bas q05 -10.83%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 5.0%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 36.0  _(momentum baissier)_
- **ADX** : 12.2  _(pas de tendance nette)_
- **MACD** : hist -0.09  _(pas de croisement recent)_
- **BB** : %B 0.03 · largeur 25.5%
- **ATR** : 0.88 (10.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.181  _(distribution)_
- **Vol ratio** : 0.84  _(volume normal)_
- **Choppiness** : 51.0  _(transition)_
- **MA** : MA20 10.17 · MA50 11.27 · MA200 19.29  _(prix < MA20)_
- **Dist MA** : MA20 -11.9% · MA50 -20.5% · MA200 -53.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (81539 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
