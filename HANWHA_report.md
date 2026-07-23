# 012450

**Generated** : 2026-07-23T21:52:15.143845+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩958000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)  
> ↳ spot ₩958000.00 (+1.5% vs entrée) · entrée ₩943425.57 · stop ₩867951.53 · T1 ₩1023728.53 · R/R 1.06  
> ↳ P(T1 av. stop) 3 % _(réel 5 s)_ · EV/risk -0.085 _(réel 5 s)_ (GBM -0.154) · ¼-Kelly 0.016 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩937998.56–₩948852.58 (mid ₩943425.57)
- Spot actuel : ₩958000.00 (+1.5% au-dessus de la zone — repli à attendre)
- Stop : ₩867951.53 (stop swing_plan-based (-6.45%))
- Targets : T1 ₩1023728.53 · R/R 1.06 | T2 ₩1024156.28 · R/R 1.07 | T3 ₩1024584.02 · R/R 1.08
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩867951.53


## Edge, scénarios & sizing

- EV/risk : -0.154 | EV/share : ₩-11651.306 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 10 % | T2 10 % | T3 10 %
- Kelly (position) : f* 0.065 | ¼-Kelly 0.016 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 16.1 | bear 8.7 | side 75.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.522% → cible +8.512% / stop −8.0%, p_fill 92%, n_eff≈36.6) : P(cible|rempli) **3%** · **EV/risk -0.085** (×p_fill ; si rempli -0.73% du capital)
  - **swing** (entrée dip −3.351% → cible +6.412% / stop −3.206%, p_fill 66%, n_eff≈28.1) : P(cible|rempli) **19%** · **EV/risk -0.281** (×p_fill ; si rempli -1.36% du capital)
  - **deep** (entrée dip −5.17% → cible +9.068% / stop −4.534%, p_fill 72%, n_eff≈26.8) : P(cible|rempli) **19%** · **EV/risk -0.315** (×p_fill ; si rempli -2.00% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→59% · +2.0%→40% · +3.0%→24% · +5.0%→10% · +8.0%→2%
- Range intraday médian 5.75% (p90 8.37%) · excursion haute méd. +1.72% / basse méd. −2.99%
- Profil de vol intra : ouverture 4.086% vs midi 1.108% vs clôture 1.136% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (142 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑0%/↓1% ; spike-down 88% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.13 ; mean-reverting — autocorr -0.076)_ ; drift intra méd. -1.771% ; recovery-V 31%
- **σ réalisé intraday** 4.586% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 39% / bas 58% / whipsaw 13%
- POC intraday (dernière séance, temps-au-prix) : 900975.0 (VA 891475.0–911425.0 ; dernier close 893000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 26% · rebond 83% · **stop −4.03%** sous le fill (sous le bruit) · cible +2.46% · R/R 0.61 (high win-rate)
- Gaps overnight (n=141) : méd. 0.78% · baisse 29% (gap-down >1% 18% · >2% 7%)
- Excursion ouverture 5min (n=142) : bas méd −1.83% (p90 −4.05%) · haut méd +0.79% · range méd 2.86%
- Excursion ouverture 15min (n=142) : bas méd −2.14% (p90 −4.64%) · haut méd +0.99% · range méd 3.4%
- Excursion ouverture 30min (n=142) : bas méd −2.33% (p90 −5.0%) · haut méd +1.08% · range méd 3.95%
- Excursion ouverture 60min (n=142) : bas méd −2.56% (p90 −5.44%) · haut méd +1.29% · range méd 4.36%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 893000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 74% (102/141) · gap 21% · délai 0.2min · rebond 51% (52/102) (MFE +1.05%)
   - −1.0% : fill 30min 57% · séance 72% (99/141) · gap 18% · délai 1.1min · rebond 56% (59/99) (MFE +1.08%)
   - −1.5% : fill 30min 55% · séance 68% (92/141) · gap 10% · délai 1.7min · rebond 60% (53/92) (MFE +1.35%)
   - −2.0% : fill 30min 46% · séance 60% (76/141) · gap 7% · délai 3.6min · rebond 65% (47/76) (MFE +1.63%)
   - −3.0% : fill 30min 30% · séance 47% (55/141) · gap 3% · délai 7.1min · rebond 72% (38/55) (MFE +1.54%)
   - −4.0% : fill 30min 21% · séance 35% (41/141) · gap 2% · délai 14.0min · rebond 84% (34/41) (MFE +1.99%)
   - −5.0% : fill 30min 12% · séance 26% (30/141) · gap 1% · délai 41.9min · rebond 83% (25/30) (MFE +2.46%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.87% (p90 −2.62%) → stop au-delà de −2.13% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.41% (p90 −2.86%) → stop au-delà de −2.64% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.79% (p90 −2.83%) → stop au-delà de −2.69% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=665 jambes) : jambe baissière méd −1.29% (p90 −3.19%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (31 séances) :
      · −1.0% : fill 100% (31/31) · rebond 47% (14/31)
      · −2.0% : fill 93% (28/31) · rebond 61% (16/28)
      · −3.0% : fill 88% (25/31) · rebond 70% (17/25)
      · −4.0% : fill 73% (22/31) · rebond 87% (18/22)
      · −5.0% : fill 50% (15/31) · rebond 85% (13/15)
   - **flat** (17 séances) :
      · −1.0% : fill 100% (17/17) · rebond 48% (9/17)
      · −2.0% : fill 87% (14/17) · rebond 56% (7/14)
      · −3.0% : fill 63% (8/17) · rebond 46% (3/8)
      · −4.0% : fill 63% (8/17) · rebond 60% (5/8)
      · −5.0% : fill 60% (7/17) · rebond 66% (4/7)
   - **gap-up** (93 séances) :
      · −1.0% : fill 57% (51/93) · rebond 66% (36/51)
      · −2.0% : fill 42% (34/93) · rebond 72% (24/34)
      · −3.0% : fill 28% (22/93) · rebond 86% (18/22)
      · −4.0% : fill 15% (11/93) · rebond 100% (11/11)
      · −5.0% : fill 10% (8/93) · rebond 100% (8/8)
- **P(clôture VERTE) selon le drive 15min** (n=142) : 33% en base · 59% si les 15 1res min sont vertes (46 cas) · 19% si rouges (96 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=142) : COUDE à **51min** → P(séance verte=clôture>ouverture) 82% si début vert vs 7% si rouge (base 33% · écart 75 pts) ; prédictivité sature ensuite (plafond brut 49min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=47) : tient le vert **82%** · continue >prix actuel 55% ; creux résiduel méd -2.07% (q20 -3.28%) → **SL/trailing à −3.28%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.95% / q75 +3.28% → **scale +1.95% / runner +3.28%**, sortie à la clôture
  - **si ROUGE au coude** (n=95) : edge inversé — récupère vert seulement **7%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.04%** (au-delà de la MAE q10 -5.04%), cible rebond +1.41% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=142) : retour [-5.39% .. +3.89%] · haut q95 +5.49% · bas q05 -6.59%
   - 60min (n=142) : retour [-5.18% .. +3.33%] · haut q95 +6.0% · bas q05 -7.14%
   - 2h (n=142) : retour [-6.91% .. +3.69%] · haut q95 +6.0% · bas q05 -8.02%
   - 4h (n=142) : retour [-6.59% .. +5.51%] · haut q95 +6.9% · bas q05 -8.38%
   - 6h (n=142) : retour [-6.81% .. +4.18%] · haut q95 +7.1% · bas q05 -8.43%
   - session (n=142) : retour [-6.83% .. +4.37%] · haut q95 +7.1% · bas q05 -8.43%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 012450 = **volatil sans tendance propre (choppy)** (vol intra méd 3.46%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 37.4  _(momentum baissier)_
- **ADX** : 19.1  _(pas de tendance nette)_
- **MACD** : hist -4034.975  _(pas de croisement recent)_
- **BB** : %B 0.39 · largeur 37.9%
- **ATR** : 84285.71 (85.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.135  _(distribution)_
- **Vol ratio** : 0.89  _(volume normal)_
- **Choppiness** : 42.5  _(transition)_
- **MA** : MA20 1001100.0 · MA50 1096340.0 · MA200 1144108.19  _(prix < MA20)_
- **Dist MA** : MA20 -4.3% · MA50 -12.6% · MA200 -16.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83140 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
