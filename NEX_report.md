# NEX

**Generated** : 2026-07-30T00:07:55.400284+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €129.40  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €129.40 (+0.9% vs entrée) · entrée €128.20 · stop €126.27 · T1 €129.77 · R/R 0.81  
> ↳ P(T1 av. stop) 20 % _(réel 5 s)_ · EV/risk -0.266 _(réel 5 s)_ (GBM -0.037) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €127.88–€128.51 (mid €128.20)
- Spot actuel : €129.40 (+0.9% au-dessus de la zone — repli à attendre)
- Stop : €126.27 (stop swing_plan-based (-3.39%))
- Targets : T1 €129.77 · R/R 0.81 | T2 €131.34 · R/R 1.63 | T3 €132.91 · R/R 2.44
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €126.27


## Edge, scénarios & sizing

- EV/risk : -0.037 | EV/share : €-0.070 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 48 % | T2 21 % | T3 7 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.3 | bear 68.4 | side 26.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.934% → cible +1.227% / stop −1.5%, p_fill 66%, n_eff≈24.9) : P(cible|rempli) **20%** · **EV/risk -0.266** (×p_fill ; si rempli -0.60% du capital)
  - **swing** (entrée dip −2.047% → cible +2.743% / stop −1.371%, p_fill 48%, n_eff≈22.7) : P(cible|rempli) **8%** · **EV/risk -0.397** (×p_fill ; si rempli -1.12% du capital)
  - **deep** (entrée dip −3.162% → cible +3.879% / stop −1.94%, p_fill 59%, n_eff≈22.6) : P(cible|rempli) **17%** · **EV/risk -0.322** (×p_fill ; si rempli -1.06% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→68% · +1.0%→55% · +2.0%→29% · +3.0%→12% · +5.0%→5% · +8.0%→1%
- Range intraday médian 3.0% (p90 4.83%) · excursion haute méd. +1.11% / basse méd. −1.03%
- Profil de vol intra : ouverture 1.693% vs midi 0.522% vs clôture 0.765% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (142 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 10% · trend ↑0%/↓0% ; spike-down 48% · recovery-V 15%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; neutre — autocorr -0.024)_ ; drift intra méd. -0.717% ; recovery-V 5%
- **σ réalisé intraday** 2.049% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 71% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 129.4913 (VA 125.5863–129.6687 ; dernier close 125.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 23% · rebond 50% · **stop −1.98%** sous le fill (sous le bruit) · cible +1.03% · R/R 0.52 (high win-rate)
- Gaps overnight (n=141) : méd. 0.13% · baisse 40% (gap-down >1% 10% · >2% 2%)
- Excursion ouverture 5min (n=142) : bas méd −0.45% (p90 −1.93%) · haut méd +0.3% · range méd 0.99%
- Excursion ouverture 15min (n=142) : bas méd −0.58% (p90 −2.08%) · haut méd +0.37% · range méd 1.29%
- Excursion ouverture 30min (n=142) : bas méd −0.59% (p90 −2.3%) · haut méd +0.43% · range méd 1.4%
- Excursion ouverture 60min (n=142) : bas méd −0.76% (p90 −2.48%) · haut méd +0.56% · range méd 1.5%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 125.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 74% (102/141) · gap 25% · délai 0.4min · rebond 44% (49/102) (MFE +0.84%)
   - −1.0% : fill 30min 41% · séance 65% (85/141) · gap 10% · délai 9.5min · rebond 43% (39/85) (MFE +0.79%)
   - −1.5% : fill 30min 24% · séance 51% (63/141) · gap 3% · délai 60.9min · rebond 44% (29/63) (MFE +0.7%)
   - −2.0% : fill 30min 16% · séance 35% (47/141) · gap 2% · délai 78.4min · rebond 43% (24/47) (MFE +0.84%)
   - −3.0% : fill 30min 5% · séance 23% (29/141) · gap 1% · délai 143.6min · rebond 50% (16/29) (MFE +1.03%)
   - −4.0% : fill 30min 1% · séance 9% (11/141) · gap 1% · délai 369.3min · rebond 16% (4/11) (MFE +0.77%)
   - −5.0% : fill 30min 1% · séance 2% (4/141) · gap 0% · délai 184.5min · rebond 89% (3/4) (MFE +1.52%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.1% (p90 −0.95%) → stop au-delà de −0.68% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −0.9%) → stop au-delà de −0.6% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.19% (p90 −1.32%) → stop au-delà de −0.6% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=285 jambes) : jambe baissière méd −1.08% (p90 −2.43%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (44 séances) :
      · −1.0% : fill 80% (36/44) · rebond 44% (15/36)
      · −2.0% : fill 45% (25/44) · rebond 43% (13/25)
      · −3.0% : fill 31% (16/44) · rebond 47% (9/16)
      · −4.0% : fill 15% (7/44) · rebond 28% (3/7)
      · −5.0% : fill 8% (4/44) · rebond 89% (3/4)
   - **flat** (34 séances) :
      · −1.0% : fill 73% (23/34) · rebond 44% (12/23)
      · −2.0% : fill 39% (11/34) · rebond 42% (5/11)
      · −3.0% : fill 27% (7/34) · rebond 32% (2/7)
      · −4.0% : fill 12% (2/34) · rebond 0% (0/2)
      · −5.0% : fill 0% (0/34) · rebond 0% (0/0)
   - **gap-up** (63 séances) :
      · −1.0% : fill 50% (26/63) · rebond 41% (12/26)
      · −2.0% : fill 26% (11/63) · rebond 44% (6/11)
      · −3.0% : fill 15% (6/63) · rebond 77% (5/6)
      · −4.0% : fill 4% (2/63) · rebond 15% (1/2)
      · −5.0% : fill 0% (0/63) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=142) : 44% en base · 67% si les 15 1res min sont vertes (77 cas) · 15% si rouges (65 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=142) : COUDE à **28min** → P(séance verte=clôture>ouverture) 81% si début vert vs 14% si rouge (base 44% · écart 67 pts) ; prédictivité sature ensuite (plafond brut 152min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=66) : tient le vert **81%** · continue >prix actuel 54% ; creux résiduel méd -0.96% (q20 -1.85%) → **SL/trailing à −1.85%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.18% / q75 +1.87% → **scale +1.18% / runner +1.87%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **14%** (continue à baisser 57%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.85%** (au-delà de la MAE q10 -2.85%), cible rebond +0.88% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=142) : retour [-2.1% .. +1.76%] · haut q95 +2.26% · bas q05 -2.83%
   - 60min (n=142) : retour [-2.66% .. +2.05%] · haut q95 +2.36% · bas q05 -3.19%
   - 2h (n=142) : retour [-3.55% .. +2.15%] · haut q95 +2.53% · bas q05 -3.74%
   - 4h (n=142) : retour [-3.12% .. +2.42%] · haut q95 +2.89% · bas q05 -3.88%
   - 6h (n=142) : retour [-3.4% .. +3.39%] · haut q95 +3.84% · bas q05 -4.13%
   - session (n=142) : retour [-3.61% .. +2.88%] · haut q95 +4.18% · bas q05 -4.64%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.4% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.94%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 43.6  _(momentum baissier)_
- **ADX** : 34.9  _(tendance etablie)_
- **MACD** : hist -0.194  _(bearish_recent)_
- **BB** : %B 0.21 · largeur 11.7%
- **ATR** : 4.22 (61.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF 0.023  _(neutre)_
- **Vol ratio** : 0.88  _(volume normal)_
- **Choppiness** : 52.2  _(transition)_
- **MA** : MA20 134.02 · MA50 145.39 · MA200 131.5  _(prix < MA20)_
- **Dist MA** : MA20 -3.4% · MA50 -11.0% · MA200 -1.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89816 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
