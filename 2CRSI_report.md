# AL2SI

**Generated** : 2026-07-22T00:10:27.652674+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · €28.80  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot €28.80 (+7.7% vs entrée) · entrée €26.74 · stop €25.61 · T1 €27.91 · R/R 1.04  
> ↳ P(T1 av. stop) 54 % _(réel 5 s)_ · EV/risk 0.116 _(réel 5 s)_ (GBM -0.028) · ¼-Kelly 0.021 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.23% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €26.51–€26.97 (mid €26.74)
- Spot actuel : €28.80 (+7.7% au-dessus de la zone — repli à attendre)
- Stop : €25.61 (stop swing_plan-based (-19.82%))
- Targets : T1 €27.91 · R/R 1.04 | T2 €29.07 · R/R 2.06 | T3 €30.23 · R/R 3.09
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €25.61


## Edge, scénarios & sizing

- EV/risk : -0.028 | EV/share : €-0.032 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 36 % | T3 36 %
- Kelly (position) : f* 0.084 | ¼-Kelly 0.021 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 19.4 | bear 6.8 | side 73.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −7.144% → cible +4.352% / stop −4.228%, p_fill 40%, n_eff≈14.6) : P(cible|rempli) **54%** · **EV/risk +0.116** (×p_fill ; si rempli +1.21% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=7, n_eff=6))
  - **deep** : indisponible (échantillon insuffisant (n=8, n_eff=7))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→80% · +2.0%→74% · +3.0%→64% · +5.0%→41% · +8.0%→24%
- Range intraday médian 8.62% (p90 22.19%) · excursion haute méd. +4.16% / basse méd. −3.97%
- Profil de vol intra : ouverture 5.895% vs midi 1.776% vs clôture 2.018% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (152 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 9% · trend ↑0%/↓1% ; spike-down 77% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.138 ; mean-reverting — autocorr -0.046)_ ; drift intra méd. -0.15% ; recovery-V 30%
- **σ réalisé intraday** 8.46% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 68% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 25.835 (VA 25.485–26.325 ; dernier close 26.58)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 46% · rebond 92% · **stop −6.56%** sous le fill (sous le bruit) · cible +3.1% · R/R 0.47 (high win-rate)
- Gaps overnight (n=151) : méd. 0.2% · baisse 40% (gap-down >1% 24% · >2% 11%)
- Excursion ouverture 5min (n=152) : bas méd −1.24% (p90 −5.3%) · haut méd +1.0% · range méd 3.08%
- Excursion ouverture 15min (n=152) : bas méd −1.64% (p90 −5.86%) · haut méd +1.5% · range méd 4.51%
- Excursion ouverture 30min (n=152) : bas méd −1.77% (p90 −5.86%) · haut méd +2.07% · range méd 4.97%
- Excursion ouverture 60min (n=152) : bas méd −2.4% (p90 −6.97%) · haut méd +2.7% · range méd 6.13%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 26.58 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 82% (118/151) · gap 29% · délai 0.3min · rebond 69% (79/118) (MFE +3.3%)
   - −1.0% : fill 30min 63% · séance 80% (113/151) · gap 24% · délai 0.3min · rebond 72% (79/113) (MFE +2.68%)
   - −1.5% : fill 30min 55% · séance 75% (103/151) · gap 16% · délai 1.0min · rebond 73% (69/103) (MFE +2.16%)
   - −2.0% : fill 30min 47% · séance 67% (90/151) · gap 11% · délai 1.4min · rebond 70% (61/90) (MFE +1.94%)
   - −3.0% : fill 30min 37% · séance 58% (74/151) · gap 7% · délai 7.5min · rebond 86% (62/74) (MFE +2.37%)
   - −4.0% : fill 30min 30% · séance 50% (63/151) · gap 5% · délai 14.9min · rebond 76% (49/63) (MFE +3.07%)
   - −5.0% : fill 30min 21% · séance 46% (55/151) · gap 4% · délai 33.6min · rebond 92% (52/55) (MFE +3.1%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.94% (p90 −5.56%) → stop au-delà de −3.84% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.26% (p90 −5.59%) → stop au-delà de −4.22% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.07% (p90 −5.74%) → stop au-delà de −4.06% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1477 jambes) : jambe baissière méd −1.25% (p90 −3.6%) · ~21.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (53 séances) :
      · −1.0% : fill 98% (49/53) · rebond 68% (33/49)
      · −2.0% : fill 87% (42/53) · rebond 58% (26/42)
      · −3.0% : fill 85% (38/53) · rebond 80% (31/38)
      · −4.0% : fill 74% (33/53) · rebond 77% (27/33)
      · −5.0% : fill 66% (30/53) · rebond 83% (27/30)
   - **flat** (33 séances) :
      · −1.0% : fill 85% (26/33) · rebond 84% (21/26)
      · −2.0% : fill 71% (20/33) · rebond 81% (15/20)
      · −3.0% : fill 55% (14/33) · rebond 95% (13/14)
      · −4.0% : fill 47% (13/33) · rebond 81% (11/13)
      · −5.0% : fill 41% (11/33) · rebond 100% (11/11)
   - **gap-up** (65 séances) :
      · −1.0% : fill 63% (38/65) · rebond 67% (25/38)
      · −2.0% : fill 50% (28/65) · rebond 79% (20/28)
      · −3.0% : fill 40% (22/65) · rebond 88% (18/22)
      · −4.0% : fill 34% (17/65) · rebond 72% (11/17)
      · −5.0% : fill 32% (14/65) · rebond 100% (14/14)
- **P(clôture VERTE) selon le drive 15min** (n=152) : 46% en base · 60% si les 15 1res min sont vertes (72 cas) · 36% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=152) : COUDE à **31min** → P(séance verte=clôture>ouverture) 72% si début vert vs 22% si rouge (base 46% · écart 50 pts) ; prédictivité sature ensuite (plafond brut 252min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **72%** · continue >prix actuel 54% ; creux résiduel méd -2.68% (q20 -6.55%) → **SL/trailing à −6.55%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.7% / q75 +6.8% → **scale +3.7% / runner +6.8%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **22%** (continue à baisser 59%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −10.63%** (au-delà de la MAE q10 -10.63%), cible rebond +2.32% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=152) : retour [-5.34% .. +6.93%] · haut q95 +8.76% · bas q05 -7.76%
   - 60min (n=152) : retour [-6.02% .. +9.48%] · haut q95 +9.97% · bas q05 -8.41%
   - 2h (n=152) : retour [-6.06% .. +9.94%] · haut q95 +11.56% · bas q05 -8.47%
   - 4h (n=152) : retour [-9.49% .. +10.52%] · haut q95 +12.86% · bas q05 -11.81%
   - 6h (n=152) : retour [-9.21% .. +14.58%] · haut q95 +18.05% · bas q05 -12.47%
   - session (n=152) : retour [-10.15% .. +18.63%] · haut q95 +19.34% · bas q05 -16.01%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.32%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 31.8  _(momentum baissier)_
- **ADX** : 25.4  _(tendance etablie)_
- **MACD** : hist -0.151  _(pas de croisement recent)_
- **BB** : %B 0.4 · largeur 60.0%
- **ATR** : 3.77 (86.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.054  _(distribution)_
- **Vol ratio** : 0.77  _(volume normal)_
- **Choppiness** : 41.6  _(transition)_
- **MA** : MA20 30.65 · MA50 39.06 · MA200 24.22  _(prix < MA20)_
- **Dist MA** : MA20 -6.0% · MA50 -26.3% · MA200 +18.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91023 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
