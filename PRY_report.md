# PRY

**Generated** : 2026-07-22T21:47:04.654663+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · €128.25  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot €128.25 (+2.5% vs entrée) · entrée €125.17 · stop €123.30 · T1 €127.06 · R/R 1.01  
> ↳ P(T1 av. stop) 25 % _(réel 5 s)_ · EV/risk -0.135 _(réel 5 s)_ (GBM 0.068) · ¼-Kelly 0.008 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -25 % hors [0,100] (R² max 0.86). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €124.80–€125.55 (mid €125.17)
- Spot actuel : €128.25 (+2.5% au-dessus de la zone — repli à attendre)
- Stop : €123.30 (stop swing_plan-based (-6.87%))
- Targets : T1 €127.06 · R/R 1.01 | T2 €128.95 · R/R 2.02 | T3 €130.83 · R/R 3.03
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €123.30


## Edge, scénarios & sizing

- EV/risk : 0.068 | EV/share : €0.127 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 49 % | T2 29 % | T3 10 %
- Kelly (position) : f* 0.032 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 27.7 | bear 54.5 | side 17.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 128.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.396% → cible +1.507% / stop −1.5%, p_fill 43%, n_eff≈16.0) : P(cible|rempli) **25%** · **EV/risk -0.135** (×p_fill ; si rempli -0.47% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=13, n_eff=9))
  - **deep** : indisponible (échantillon insuffisant (n=10, n_eff=6))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→68% · +2.0%→44% · +3.0%→32% · +5.0%→9% · +8.0%→4%
- Range intraday médian 3.97% (p90 6.32%) · excursion haute méd. +1.67% / basse méd. −1.47%
- Profil de vol intra : ouverture 2.282% vs midi 0.804% vs clôture 1.124% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (137 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 52% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.135 ; neutre — autocorr 0.003)_ ; drift intra méd. -0.401% ; recovery-V 13%
- **σ réalisé intraday** 2.651% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 63% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 128.8075 (VA 128.4435–129.4445 ; dernier close 130.16)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 34% · rebond 61% · **stop −2.89%** sous le fill (sous le bruit) · cible +1.6% · R/R 0.55 (high win-rate)
- Gaps overnight (n=136) : méd. 0.29% · baisse 43% (gap-down >1% 21% · >2% 13%)
- Excursion ouverture 5min (n=137) : bas méd −0.6% (p90 −2.13%) · haut méd +0.5% · range méd 1.31%
- Excursion ouverture 15min (n=137) : bas méd −0.77% (p90 −2.68%) · haut méd +0.73% · range méd 1.73%
- Excursion ouverture 30min (n=137) : bas méd −0.9% (p90 −2.96%) · haut méd +0.86% · range méd 1.87%
- Excursion ouverture 60min (n=137) : bas méd −1.08% (p90 −3.2%) · haut méd +0.94% · range méd 2.12%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 130.16 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 70% (98/136) · gap 27% · délai 0.2min · rebond 59% (61/98) (MFE +1.16%)
   - −1.0% : fill 30min 50% · séance 62% (83/136) · gap 21% · délai 0.2min · rebond 55% (49/83) (MFE +1.46%)
   - −1.5% : fill 30min 34% · séance 52% (71/136) · gap 18% · délai 0.4min · rebond 52% (39/71) (MFE +1.07%)
   - −2.0% : fill 30min 26% · séance 42% (57/136) · gap 13% · délai 3.8min · rebond 55% (35/57) (MFE +1.2%)
   - −3.0% : fill 30min 15% · séance 34% (42/136) · gap 5% · délai 72.3min · rebond 61% (28/42) (MFE +1.6%)
   - −4.0% : fill 30min 4% · séance 20% (22/136) · gap 2% · délai 160.8min · rebond 62% (15/22) (MFE +1.31%)
   - −5.0% : fill 30min 2% · séance 13% (15/136) · gap 1% · délai 332.6min · rebond 84% (12/15) (MFE +1.58%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.2% (p90 −1.62%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.22% (p90 −1.6%) → stop au-delà de −1.05% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.09% (p90 −1.56%) → stop au-delà de −1.02% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=411 jambes) : jambe baissière méd −1.07% (p90 −2.48%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 88% (44/49) · rebond 49% (25/44)
      · −2.0% : fill 69% (35/49) · rebond 63% (24/35)
      · −3.0% : fill 59% (27/49) · rebond 66% (20/27)
      · −4.0% : fill 33% (14/49) · rebond 53% (9/14)
      · −5.0% : fill 28% (11/49) · rebond 89% (9/11)
   - **flat** (25 séances) :
      · −1.0% : fill 60% (13/25) · rebond 59% (8/13)
      · −2.0% : fill 30% (6/25) · rebond 75% (4/6)
      · −3.0% : fill 28% (5/25) · rebond 40% (2/5)
      · −4.0% : fill 13% (3/25) · rebond 59% (2/3)
      · −5.0% : fill 7% (2/25) · rebond 25% (1/2)
   - **gap-up** (62 séances) :
      · −1.0% : fill 43% (26/62) · rebond 62% (16/26)
      · −2.0% : fill 26% (16/62) · rebond 30% (7/16)
      · −3.0% : fill 18% (10/62) · rebond 59% (6/10)
      · −4.0% : fill 12% (5/62) · rebond 81% (4/5)
      · −5.0% : fill 3% (2/62) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=137) : 51% en base · 78% si les 15 1res min sont vertes (65 cas) · 26% si rouges (72 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=137) : COUDE à **1:03** → P(séance verte=clôture>ouverture) 86% si début vert vs 23% si rouge (base 51% · écart 63 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=64) : tient le vert **86%** · continue >prix actuel 66% ; creux résiduel méd -1.24% (q20 -2.11%) → **SL/trailing à −2.11%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.65% / q75 +2.65% → **scale +1.65% / runner +2.65%**, sortie à la clôture
  - **si ROUGE au coude** (n=73) : edge inversé — récupère vert seulement **23%** (continue à baisser 62%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.13%** (au-delà de la MAE q10 -4.13%), cible rebond +1.15% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=137) : retour [-2.88% .. +2.71%] · haut q95 +3.45% · bas q05 -3.37%
   - 60min (n=137) : retour [-2.93% .. +2.46%] · haut q95 +3.92% · bas q05 -3.49%
   - 2h (n=137) : retour [-3.6% .. +3.47%] · haut q95 +4.11% · bas q05 -3.7%
   - 4h (n=137) : retour [-3.46% .. +3.67%] · haut q95 +4.57% · bas q05 -4.47%
   - 6h (n=137) : retour [-3.71% .. +3.77%] · haut q95 +5.02% · bas q05 -4.66%
   - session (n=137) : retour [-4.34% .. +4.81%] · haut q95 +6.1% · bas q05 -5.62%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 5.1% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.4%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 35.7  _(momentum baissier)_
- **ADX** : 25.7  _(tendance etablie)_
- **MACD** : hist -1.051  _(pas de croisement recent)_
- **BB** : %B 0.19 · largeur 20.8%
- **ATR** : 5.78 (81.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.223  _(distribution)_
- **Vol ratio** : 1.27  _(volume normal)_
- **Choppiness** : 46.3  _(transition)_
- **MA** : MA20 137.05 · MA50 143.77 · MA200 109.26  _(prix < MA20)_
- **Dist MA** : MA20 -6.4% · MA50 -10.8% · MA200 +17.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93626 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
