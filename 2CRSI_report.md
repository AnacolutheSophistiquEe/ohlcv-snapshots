# AL2SI

**Generated** : 2026-07-16T21:46:04.470394+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 9.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €24.34  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €24.34 (+4.0% vs entrée) · entrée €23.40 · stop €22.19 · T1 €24.64 · R/R 1.02  
> ↳ P(T1 av. stop) 28 % _(réel 5 s)_ · EV/risk -0.021 _(réel 5 s)_ (GBM -0.022) · ¼-Kelly 0.028 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −5.15% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -41 % hors [0,100] (R² max 0.55). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €23.15–€23.65 (mid €23.40)
- Spot actuel : €24.34 (+4.0% au-dessus de la zone — repli à attendre)
- Stop : €22.19 (stop swing_plan-based (-13.97%))
- Targets : T1 €24.64 · R/R 1.02 | T2 €25.89 · R/R 2.06 | T3 €27.13 · R/R 3.08
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €22.19


## Edge, scénarios & sizing

- EV/risk : -0.022 | EV/share : €-0.027 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 38 % | T2 38 % | T3 38 %
- Kelly (position) : f* 0.113 | ¼-Kelly 0.028 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 16.8 | bear 78.2 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.879% → cible +5.323% / stop −5.151%, p_fill 65%, n_eff≈22.9) : P(cible|rempli) **28%** · **EV/risk -0.021** (×p_fill ; si rempli -0.17% du capital)
  - **swing** (entrée dip −8.526% → cible +11.902% / stop −5.951%, p_fill 42%, n_eff≈14.6) : P(cible|rempli) **10%** · **EV/risk -0.302** (×p_fill ; si rempli -4.33% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=13, n_eff=10))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→79% · +2.0%→72% · +3.0%→62% · +5.0%→40% · +8.0%→21%
- Range intraday médian 8.29% (p90 20.17%) · excursion haute méd. +3.92% / basse méd. −3.6%
- Profil de vol intra : ouverture 5.772% vs midi 1.686% vs clôture 1.977% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (149 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 10% · trend ↑0%/↓1% ; spike-down 76% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.15 ; mean-reverting — autocorr -0.045)_ ; drift intra méd. -0.508% ; recovery-V 24%
- **σ réalisé intraday** 8.143% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 38% / bas 73% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 27.3903 (VA 27.1517–28.4237 ; dernier close 26.76)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 44% · rebond 91% · **stop −5.44%** sous le fill (sous le bruit) · cible +3.1% · R/R 0.57 (high win-rate)
- Gaps overnight (n=148) : méd. 0.22% · baisse 39% (gap-down >1% 21% · >2% 8%)
- Excursion ouverture 5min (n=149) : bas méd −1.24% (p90 −5.05%) · haut méd +1.03% · range méd 3.07%
- Excursion ouverture 15min (n=149) : bas méd −1.61% (p90 −5.91%) · haut méd +1.51% · range méd 4.47%
- Excursion ouverture 30min (n=149) : bas méd −1.75% (p90 −6.56%) · haut méd +1.99% · range méd 4.9%
- Excursion ouverture 60min (n=149) : bas méd −2.34% (p90 −7.13%) · haut méd +2.33% · range méd 5.8%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 26.76 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 81% (115/148) · gap 27% · délai 0.3min · rebond 67% (76/115) (MFE +2.76%)
   - −1.0% : fill 30min 61% · séance 79% (110/148) · gap 21% · délai 0.4min · rebond 70% (76/110) (MFE +2.43%)
   - −1.5% : fill 30min 53% · séance 74% (100/148) · gap 13% · délai 1.1min · rebond 71% (66/100) (MFE +1.75%)
   - −2.0% : fill 30min 44% · séance 66% (87/148) · gap 8% · délai 2.7min · rebond 68% (58/87) (MFE +1.86%)
   - −3.0% : fill 30min 33% · séance 56% (71/148) · gap 5% · délai 10.7min · rebond 84% (59/71) (MFE +2.26%)
   - −4.0% : fill 30min 28% · séance 49% (61/148) · gap 5% · délai 21.9min · rebond 75% (47/61) (MFE +2.74%)
   - −5.0% : fill 30min 20% · séance 44% (53/148) · gap 4% · délai 33.7min · rebond 91% (50/53) (MFE +3.1%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.91% (p90 −5.57%) → stop au-delà de −3.04% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.07% (p90 −5.61%) → stop au-delà de −4.08% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.98% (p90 −5.86%) → stop au-delà de −3.61% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1435 jambes) : jambe baissière méd −1.24% (p90 −3.5%) · ~20.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (51 séances) :
      · −1.0% : fill 98% (47/51) · rebond 64% (31/47)
      · −2.0% : fill 86% (40/51) · rebond 52% (24/40)
      · −3.0% : fill 83% (36/51) · rebond 77% (29/36)
      · −4.0% : fill 71% (31/51) · rebond 73% (25/31)
      · −5.0% : fill 62% (28/51) · rebond 80% (25/28)
   - **flat** (32 séances) :
      · −1.0% : fill 84% (25/32) · rebond 83% (20/25)
      · −2.0% : fill 69% (19/32) · rebond 78% (14/19)
      · −3.0% : fill 51% (13/32) · rebond 94% (12/13)
      · −4.0% : fill 51% (13/32) · rebond 81% (11/13)
      · −5.0% : fill 44% (11/32) · rebond 100% (11/11)
   - **gap-up** (65 séances) :
      · −1.0% : fill 63% (38/65) · rebond 67% (25/38)
      · −2.0% : fill 50% (28/65) · rebond 79% (20/28)
      · −3.0% : fill 40% (22/65) · rebond 88% (18/22)
      · −4.0% : fill 34% (17/65) · rebond 72% (11/17)
      · −5.0% : fill 32% (14/65) · rebond 100% (14/14)
- **P(clôture VERTE) selon le drive 15min** (n=149) : 45% en base · 63% si les 15 1res min sont vertes (71 cas) · 32% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=149) : COUDE à **31min** → P(séance verte=clôture>ouverture) 73% si début vert vs 22% si rouge (base 45% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 241min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **73%** · continue >prix actuel 56% ; creux résiduel méd -2.39% (q20 -5.16%) → **SL/trailing à −5.16%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.63% / q75 +5.81% → **scale +3.63% / runner +5.81%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **22%** (continue à baisser 59%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −10.63%** (au-delà de la MAE q10 -10.63%), cible rebond +2.32% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=149) : retour [-5.46% .. +7.61%] · haut q95 +8.99% · bas q05 -7.79%
   - 60min (n=149) : retour [-6.05% .. +9.65%] · haut q95 +10.04% · bas q05 -8.68%
   - 2h (n=149) : retour [-6.1% .. +10.13%] · haut q95 +10.25% · bas q05 -8.68%
   - 4h (n=149) : retour [-10.53% .. +11.0%] · haut q95 +13.1% · bas q05 -12.37%
   - 6h (n=149) : retour [-10.02% .. +14.79%] · haut q95 +19.44% · bas q05 -13.74%
   - session (n=149) : retour [-10.38% .. +20.66%] · haut q95 +20.76% · bas q05 -16.39%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.31%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 44.7  _(momentum baissier)_
- **ADX** : 23.8  _(pas de tendance nette)_
- **MACD** : hist -0.507  _(bearish_recent)_
- **BB** : %B 0.2 · largeur 65.3%
- **ATR** : 4.02 (88.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.017  _(neutre)_
- **Vol ratio** : 1.36  _(volume normal)_
- **Choppiness** : 44.8  _(transition)_
- **MA** : MA20 30.36 · MA50 39.66 · MA200 24.02  _(prix < MA20)_
- **Dist MA** : MA20 -19.8% · MA50 -38.6% · MA200 +1.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90879 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
