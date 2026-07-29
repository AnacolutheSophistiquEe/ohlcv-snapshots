# PRY

**Generated** : 2026-07-29T21:46:48.392834+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · €114.70  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)  
> ↳ spot €114.70 (+2.2% vs entrée) · entrée €112.24 · stop €110.39 · T1 €115.95 · R/R 2.01  
> ↳ P(T1 av. stop) 1 % _(réel 5 s)_ · EV/risk -0.278 _(réel 5 s)_ (GBM -0.031) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.65% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -60 % hors [0,100] (R² max 0.86). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €111.89–€112.59 (mid €112.24)
- Spot actuel : €114.70 (+2.2% au-dessus de la zone — repli à attendre)
- Stop : €110.39 (stop swing_plan-based (-6.36%))
- Targets : T1 €115.95 · R/R 2.01 | T2 €116.69 · R/R 2.41 | T3 €117.44 · R/R 2.81
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €110.39


## Edge, scénarios & sizing

- EV/risk : -0.031 | EV/share : €-0.058 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 20 % | T2 14 % | T3 8 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.5 | bear 18.4 | side 75.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.144% → cible +3.303% / stop −1.652%, p_fill 52%, n_eff≈18.6) : P(cible|rempli) **1%** · **EV/risk -0.278** (×p_fill ; si rempli -0.88% du capital)
  - **swing** (entrée dip −4.717% → cible +3.449% / stop −1.724%, p_fill 34%, n_eff≈13.2) : P(cible|rempli) **17%** · **EV/risk -0.178** (×p_fill ; si rempli -0.89% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=14, n_eff=8))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→64% · +2.0%→38% · +3.0%→26% · +5.0%→9% · +8.0%→4%
- Range intraday médian 3.92% (p90 6.33%) · excursion haute méd. +1.37% / basse méd. −1.61%
- Profil de vol intra : ouverture 2.283% vs midi 0.826% vs clôture 1.145% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (142 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 56% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.134 ; neutre — autocorr 0.001)_ ; drift intra méd. -0.794% ; recovery-V 15%
- **σ réalisé intraday** 2.636% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 66% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 120.5968 (VA 116.6697–120.9538 ; dernier close 116.52)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 15% · rebond 76% · **stop −2.6%** sous le fill (sous le bruit) · cible +1.58% · R/R 0.61 (high win-rate)
- Gaps overnight (n=141) : méd. 0.2% · baisse 43% (gap-down >1% 21% · >2% 12%)
- Excursion ouverture 5min (n=142) : bas méd −0.75% (p90 −2.05%) · haut méd +0.53% · range méd 1.38%
- Excursion ouverture 15min (n=142) : bas méd −0.91% (p90 −2.29%) · haut méd +0.67% · range méd 1.72%
- Excursion ouverture 30min (n=142) : bas méd −0.94% (p90 −2.93%) · haut méd +0.84% · range méd 1.86%
- Excursion ouverture 60min (n=142) : bas méd −1.21% (p90 −3.09%) · haut méd +0.89% · range méd 2.1%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 116.52 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 72% (103/141) · gap 28% · délai 0.2min · rebond 59% (64/103) (MFE +1.18%)
   - −1.0% : fill 30min 50% · séance 64% (87/141) · gap 21% · délai 0.3min · rebond 54% (51/87) (MFE +1.45%)
   - −1.5% : fill 30min 34% · séance 54% (75/141) · gap 16% · délai 1.5min · rebond 48% (40/75) (MFE +0.88%)
   - −2.0% : fill 30min 25% · séance 46% (61/141) · gap 12% · délai 4.3min · rebond 54% (37/61) (MFE +1.2%)
   - −3.0% : fill 30min 16% · séance 37% (45/141) · gap 4% · délai 76.7min · rebond 62% (30/45) (MFE +1.58%)
   - −4.0% : fill 30min 4% · séance 24% (25/141) · gap 2% · délai 249.0min · rebond 71% (18/25) (MFE +1.37%)
   - −5.0% : fill 30min 2% · séance 15% (17/141) · gap 1% · délai 394.0min · rebond 76% (13/17) (MFE +1.58%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.35% (p90 −1.75%) → stop au-delà de −1.5% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.22% (p90 −1.6%) → stop au-delà de −1.05% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.09% (p90 −1.56%) → stop au-delà de −1.02% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=431 jambes) : jambe baissière méd −1.08% (p90 −2.55%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (51 séances) :
      · −1.0% : fill 89% (46/51) · rebond 43% (25/46)
      · −2.0% : fill 72% (37/51) · rebond 62% (25/37)
      · −3.0% : fill 63% (29/51) · rebond 71% (22/29)
      · −4.0% : fill 40% (16/51) · rebond 65% (11/16)
      · −5.0% : fill 30% (12/51) · rebond 73% (9/12)
   - **flat** (26 séances) :
      · −1.0% : fill 65% (14/26) · rebond 66% (9/14)
      · −2.0% : fill 38% (7/26) · rebond 82% (5/7)
      · −3.0% : fill 25% (5/26) · rebond 40% (2/5)
      · −4.0% : fill 12% (3/26) · rebond 59% (2/3)
      · −5.0% : fill 6% (2/26) · rebond 25% (1/2)
   - **gap-up** (64 séances) :
      · −1.0% : fill 44% (27/64) · rebond 66% (17/27)
      · −2.0% : fill 28% (17/64) · rebond 26% (7/17)
      · −3.0% : fill 21% (11/64) · rebond 48% (6/11)
      · −4.0% : fill 15% (6/64) · rebond 86% (5/6)
      · −5.0% : fill 7% (3/64) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=142) : 48% en base · 75% si les 15 1res min sont vertes (66 cas) · 26% si rouges (76 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=142) : COUDE à **1:10** → P(séance verte=clôture>ouverture) 86% si début vert vs 20% si rouge (base 48% · écart 67 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=65) : tient le vert **86%** · continue >prix actuel 65% ; creux résiduel méd -1.29% (q20 -2.05%) → **SL/trailing à −2.05%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.4% / q75 +2.6% → **scale +1.4% / runner +2.6%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **20%** (continue à baisser 68%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.11%** (au-delà de la MAE q10 -4.11%), cible rebond +1.2% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=142) : retour [-2.84% .. +2.68%] · haut q95 +3.44% · bas q05 -3.34%
   - 60min (n=142) : retour [-2.9% .. +2.27%] · haut q95 +3.9% · bas q05 -3.47%
   - 2h (n=142) : retour [-3.57% .. +3.2%] · haut q95 +4.08% · bas q05 -3.68%
   - 4h (n=142) : retour [-3.46% .. +3.55%] · haut q95 +4.53% · bas q05 -4.44%
   - 6h (n=142) : retour [-3.71% .. +3.75%] · haut q95 +4.88% · bas q05 -4.61%
   - session (n=142) : retour [-4.9% .. +4.78%] · haut q95 +5.88% · bas q05 -6.14%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.9% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.41%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 24.7  _(survente)_
- **ADX** : 32.9  _(tendance etablie)_
- **MACD** : hist -1.485  _(pas de croisement recent)_
- **BB** : %B 0.0 · largeur 25.2%
- **ATR** : 5.5 (76.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.179  _(distribution)_
- **Vol ratio** : 1.3  _(volume normal)_
- **Choppiness** : 42.8  _(transition)_
- **MA** : MA20 131.14 · MA50 141.06 · MA200 110.09  _(prix < MA20)_
- **Dist MA** : MA20 -12.5% · MA50 -18.7% · MA200 +4.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91404 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
