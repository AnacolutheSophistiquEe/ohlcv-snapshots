# PRY

**Generated** : 2026-08-07T21:47:28.201762+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · €126.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €126.00 (+0.6% vs entrée) · entrée €125.30 · stop €115.28 · T1 €127.19 · R/R 0.19  
> ↳ P(T1 av. stop) 38 % _(réel 5 s)_ · EV/risk -0.103 _(réel 5 s)_ (GBM -0.05) · ¼-Kelly 0.088 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €124.92–€125.68 (mid €125.30)
- Spot actuel : €126.00 (+0.6% au-dessus de la zone — repli à attendre)
- Stop : €115.28 (stop swing_plan-based (-6.16%))
- Targets : T1 €127.19 · R/R 0.19 | T2 €129.08 · R/R 0.38 | T3 €130.96 · R/R 0.56
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €115.28


## Edge, scénarios & sizing

- EV/risk : -0.05 | EV/share : €-0.504 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 49 % | T2 29 % | T3 11 %
- Kelly (position) : f* 0.351 | ¼-Kelly 0.088 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 29.2 | bear 58.4 | side 12.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 252.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.554% → cible +1.506% / stop −8.0%, p_fill 84%, n_eff≈32.4) : P(cible|rempli) **38%** · **EV/risk -0.103** (×p_fill ; si rempli -0.98% du capital)
  - **swing** (entrée dip −1.219% → cible +3.368% / stop −5.002%, p_fill 78%, n_eff≈29.5) : P(cible|rempli) **31%** · **EV/risk -0.363** (×p_fill ; si rempli -2.32% du capital)
  - **deep** (entrée dip −1.889% → cible +4.764% / stop −7.553%, p_fill 87%, n_eff≈32.6) : P(cible|rempli) **25%** · **EV/risk -0.480** (×p_fill ; si rempli -4.16% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→64% · +2.0%→40% · +3.0%→29% · +5.0%→9% · +8.0%→4%
- Range intraday médian 4.35% (p90 6.51%) · excursion haute méd. +1.45% / basse méd. −1.86%
- Profil de vol intra : ouverture 2.425% vs midi 0.857% vs clôture 1.204% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (149 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 58% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.127 ; neutre — autocorr 0.007)_ ; drift intra méd. -0.908% ; recovery-V 27%
- **σ réalisé intraday** 2.94% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 71% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 124.2765 (VA 123.5845–125.3145 ; dernier close 124.36)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 21% · rebond 71% · **stop −2.55%** sous le fill (sous le bruit) · cible +1.37% · R/R 0.54 (high win-rate)
- Gaps overnight (n=148) : méd. 0.3% · baisse 41% (gap-down >1% 20% · >2% 10%)
- Excursion ouverture 5min (n=149) : bas méd −0.82% (p90 −2.37%) · haut méd +0.5% · range méd 1.51%
- Excursion ouverture 15min (n=149) : bas méd −0.99% (p90 −2.92%) · haut méd +0.64% · range méd 1.86%
- Excursion ouverture 30min (n=149) : bas méd −1.08% (p90 −3.2%) · haut méd +0.76% · range méd 2.04%
- Excursion ouverture 60min (n=149) : bas méd −1.24% (p90 −3.38%) · haut méd +0.87% · range méd 2.27%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 124.36 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 72% (108/148) · gap 27% · délai 0.2min · rebond 62% (68/108) (MFE +1.27%)
   - −1.0% : fill 30min 49% · séance 65% (92/148) · gap 20% · délai 0.3min · rebond 61% (56/92) (MFE +1.57%)
   - −1.5% : fill 30min 35% · séance 56% (80/148) · gap 16% · délai 2.0min · rebond 53% (44/80) (MFE +1.14%)
   - −2.0% : fill 30min 26% · séance 47% (65/148) · gap 10% · délai 5.4min · rebond 61% (41/65) (MFE +1.34%)
   - −3.0% : fill 30min 14% · séance 36% (47/148) · gap 4% · délai 76.9min · rebond 65% (32/47) (MFE +1.64%)
   - −4.0% : fill 30min 3% · séance 21% (25/148) · gap 1% · délai 249.0min · rebond 71% (18/25) (MFE +1.37%)
   - −5.0% : fill 30min 1% · séance 13% (17/148) · gap 1% · délai 394.0min · rebond 76% (13/17) (MFE +1.58%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.39% (p90 −2.02%) → stop au-delà de −1.55% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.43% (p90 −2.13%) → stop au-delà de −1.5% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.26% (p90 −2.02%) → stop au-delà de −1.2% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=470 jambes) : jambe baissière méd −1.07% (p90 −2.61%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (52 séances) :
      · −1.0% : fill 90% (47/52) · rebond 46% (26/47)
      · −2.0% : fill 73% (38/52) · rebond 64% (26/38)
      · −3.0% : fill 60% (29/52) · rebond 71% (22/29)
      · −4.0% : fill 38% (16/52) · rebond 65% (11/16)
      · −5.0% : fill 29% (12/52) · rebond 73% (9/12)
   - **flat** (27 séances) :
      · −1.0% : fill 69% (15/27) · rebond 71% (10/15)
      · −2.0% : fill 45% (8/27) · rebond 86% (6/8)
      · −3.0% : fill 22% (5/27) · rebond 40% (2/5)
      · −4.0% : fill 10% (3/27) · rebond 59% (2/3)
      · −5.0% : fill 6% (2/27) · rebond 25% (1/2)
   - **gap-up** (69 séances) :
      · −1.0% : fill 46% (30/69) · rebond 74% (20/30)
      · −2.0% : fill 30% (19/69) · rebond 43% (9/19)
      · −3.0% : fill 24% (13/69) · rebond 63% (8/13)
      · −4.0% : fill 13% (6/69) · rebond 86% (5/6)
      · −5.0% : fill 6% (3/69) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=149) : 47% en base · 70% si les 15 1res min sont vertes (69 cas) · 29% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=149) : COUDE à **1:10** → P(séance verte=clôture>ouverture) 83% si début vert vs 23% si rouge (base 47% · écart 61 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=67) : tient le vert **83%** · continue >prix actuel 64% ; creux résiduel méd -1.32% (q20 -2.06%) → **SL/trailing à −2.06%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.41% / q75 +2.58% → **scale +1.41% / runner +2.58%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **23%** (continue à baisser 67%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.13%** (au-delà de la MAE q10 -4.13%), cible rebond +1.25% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=149) : retour [-2.97% .. +2.78%] · haut q95 +3.51% · bas q05 -3.41%
   - 60min (n=149) : retour [-3.39% .. +2.22%] · haut q95 +3.98% · bas q05 -3.59%
   - 2h (n=149) : retour [-3.73% .. +2.57%] · haut q95 +4.1% · bas q05 -4.86%
   - 4h (n=149) : retour [-3.68% .. +3.22%] · haut q95 +4.44% · bas q05 -4.97%
   - 6h (n=149) : retour [-3.77% .. +3.71%] · haut q95 +4.71% · bas q05 -5.61%
   - session (n=149) : retour [-4.61% .. +4.49%] · haut q95 +5.72% · bas q05 -6.36%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.7% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.43%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 50.9  _(neutre)_
- **ADX** : 34.0  _(tendance etablie)_
- **MACD** : hist 0.7  _(bullish_recent)_
- **BB** : %B 0.49 · largeur 19.7%
- **ATR** : 6.22 (89.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.006  _(neutre)_
- **Vol ratio** : 0.88  _(volume normal)_
- **Choppiness** : 55.0  _(transition)_
- **MA** : MA20 126.15 · MA50 137.79 · MA200 111.13  _(prix < MA20)_
- **Dist MA** : MA20 -0.1% · MA50 -8.6% · MA200 +13.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92993 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
