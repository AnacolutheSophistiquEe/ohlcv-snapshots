# NEX

**Generated** : 2026-07-17T21:43:29.767522+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · €135.30  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €135.30 (+2.1% vs entrée) · entrée €132.56 · stop €130.57 · T1 €134.23 · R/R 0.84  
> ↳ P(T1 av. stop) 6 % _(réel 5 s)_ · EV/risk -0.301 _(réel 5 s)_ (GBM -0.024) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -24 % hors [0,100] (R² max 0.84). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €132.23–€132.90 (mid €132.56)
- Spot actuel : €135.30 (+2.1% au-dessus de la zone — repli à attendre)
- Stop : €130.57 (stop swing_plan-based (-5.79%))
- Targets : T1 €134.23 · R/R 0.84 | T2 €135.89 · R/R 1.67 | T3 €137.55 · R/R 2.51
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €130.57


## Edge, scénarios & sizing

- EV/risk : -0.024 | EV/share : €-0.047 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 49 % | T2 20 % | T3 7 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 18.2 | bear 65.2 | side 16.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.02% → cible +1.255% / stop −1.5%, p_fill 42%, n_eff≈16.9) : P(cible|rempli) **6%** · **EV/risk -0.301** (×p_fill ; si rempli -1.07% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=10, n_eff=8))
  - **deep** : indisponible (échantillon insuffisant (n=11, n_eff=9))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→70% · +1.0%→60% · +2.0%→30% · +3.0%→12% · +5.0%→5% · +8.0%→1%
- Range intraday médian 3.03% (p90 4.67%) · excursion haute méd. +1.37% / basse méd. −1.03%
- Profil de vol intra : ouverture 1.719% vs midi 0.555% vs clôture 0.763% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (134 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 48% · recovery-V 18%)_
- **Régime intraday** : **chop** _(efficiency 0.122 ; neutre — autocorr -0.005)_ ; drift intra méd. -0.65% ; recovery-V 9%
- **σ réalisé intraday** 2.159% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 63% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 131.5412 (VA 131.2563–132.9663 ; dernier close 133.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 25% · rebond 55% · **stop −1.88%** sous le fill (sous le bruit) · cible +1.17% · R/R 0.62 (high win-rate)
- Gaps overnight (n=133) : méd. 0.18% · baisse 39% (gap-down >1% 10% · >2% 3%)
- Excursion ouverture 5min (n=134) : bas méd −0.45% (p90 −2.06%) · haut méd +0.3% · range méd 1.14%
- Excursion ouverture 15min (n=134) : bas méd −0.58% (p90 −2.16%) · haut méd +0.39% · range méd 1.37%
- Excursion ouverture 30min (n=134) : bas méd −0.6% (p90 −2.41%) · haut méd +0.44% · range méd 1.43%
- Excursion ouverture 60min (n=134) : bas méd −0.7% (p90 −2.52%) · haut méd +0.57% · range méd 1.57%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 133.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 72% (95/133) · gap 23% · délai 0.4min · rebond 47% (47/95) (MFE +0.86%)
   - −1.0% : fill 30min 39% · séance 62% (78/133) · gap 10% · délai 8.0min · rebond 40% (35/78) (MFE +0.69%)
   - −1.5% : fill 30min 26% · séance 47% (57/133) · gap 3% · délai 5.7min · rebond 43% (26/57) (MFE +0.71%)
   - −2.0% : fill 30min 18% · séance 37% (45/133) · gap 3% · délai 36.7min · rebond 48% (24/45) (MFE +0.99%)
   - −3.0% : fill 30min 6% · séance 25% (28/133) · gap 1% · délai 126.7min · rebond 55% (16/28) (MFE +1.17%)
   - −4.0% : fill 30min 1% · séance 9% (10/133) · gap 1% · délai 277.7min · rebond 20% (4/10) (MFE +0.82%)
   - −5.0% : fill 30min 1% · séance 3% (4/133) · gap 0% · délai 184.5min · rebond 89% (3/4) (MFE +1.52%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.08% (p90 −0.97%) → stop au-delà de −0.58% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.08% (p90 −0.68%) → stop au-delà de −0.5% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.19% (p90 −1.32%) → stop au-delà de −0.6% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=270 jambes) : jambe baissière méd −1.09% (p90 −2.47%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (41 séances) :
      · −1.0% : fill 75% (33/41) · rebond 38% (13/33)
      · −2.0% : fill 54% (25/41) · rebond 43% (13/25)
      · −3.0% : fill 37% (16/41) · rebond 47% (9/16)
      · −4.0% : fill 18% (7/41) · rebond 28% (3/7)
      · −5.0% : fill 10% (4/41) · rebond 89% (3/4)
   - **flat** (31 séances) :
      · −1.0% : fill 66% (20/31) · rebond 49% (11/20)
      · −2.0% : fill 32% (9/31) · rebond 63% (5/9)
      · −3.0% : fill 26% (6/31) · rebond 42% (2/6)
      · −4.0% : fill 6% (1/31) · rebond 0% (0/1)
      · −5.0% : fill 0% (0/31) · rebond 0% (0/0)
   - **gap-up** (61 séances) :
      · −1.0% : fill 50% (25/61) · rebond 36% (11/25)
      · −2.0% : fill 28% (11/61) · rebond 44% (6/11)
      · −3.0% : fill 16% (6/61) · rebond 77% (5/6)
      · −4.0% : fill 4% (2/61) · rebond 15% (1/2)
      · −5.0% : fill 0% (0/61) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=134) : 49% en base · 79% si les 15 1res min sont vertes (71 cas) · 16% si rouges (63 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=134) : COUDE à **28min** → P(séance verte=clôture>ouverture) 88% si début vert vs 17% si rouge (base 49% · écart 71 pts) ; prédictivité sature ensuite (plafond brut 28min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=63) : tient le vert **88%** · continue >prix actuel 57% ; creux résiduel méd -0.96% (q20 -1.65%) → **SL/trailing à −1.65%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.23% / q75 +1.71% → **scale +1.23% / runner +1.71%**, sortie à la clôture
  - **si ROUGE au coude** (n=71) : edge inversé — récupère vert seulement **17%** (continue à baisser 57%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.14%** (au-delà de la MAE q10 -3.14%), cible rebond +1.03% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=134) : retour [-2.25% .. +1.92%] · haut q95 +2.35% · bas q05 -2.87%
   - 60min (n=134) : retour [-2.81% .. +2.06%] · haut q95 +2.48% · bas q05 -3.22%
   - 2h (n=134) : retour [-3.59% .. +2.23%] · haut q95 +2.73% · bas q05 -3.74%
   - 4h (n=134) : retour [-3.34% .. +2.57%] · haut q95 +2.96% · bas q05 -3.94%
   - 6h (n=134) : retour [-3.59% .. +3.54%] · haut q95 +4.18% · bas q05 -4.18%
   - session (n=134) : retour [-3.58% .. +2.96%] · haut q95 +4.21% · bas q05 -4.61%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.5% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.95%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 39.3  _(momentum baissier)_
- **ADX** : 32.3  _(tendance etablie)_
- **MACD** : hist -0.078  _(pas de croisement recent)_
- **BB** : %B 0.33 · largeur 20.6%
- **ATR** : 4.85 (84.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.038  _(neutre)_
- **Vol ratio** : 1.47  _(volume normal)_
- **Choppiness** : 53.8  _(transition)_
- **MA** : MA20 140.14 · MA50 149.84 · MA200 131.19  _(prix < MA20)_
- **Dist MA** : MA20 -3.5% · MA50 -9.7% · MA200 +3.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89127 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
