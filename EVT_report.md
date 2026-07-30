# EVT

**Generated** : 2026-07-30T00:04:16.543359+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite high · €3.48  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €3.48 (+2.1% vs entrée) · entrée €3.41 · stop €3.29 · T1 €3.53 · R/R 1.0  
> ↳ P(T1 av. stop) 25 % _(réel 5 s)_ · EV/risk -0.01 _(réel 5 s)_ (GBM 0.021) · ¼-Kelly 0.006 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.5% cohérent avec le bruit 5 s (EV-optimal ≈ −3.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €3.38–€3.43 (mid €3.41)
- Spot actuel : €3.48 (+2.1% au-dessus de la zone — repli à attendre)
- Stop : €3.29 (stop swing_plan-based (-8.6%))
- Targets : T1 €3.53 · R/R 1.0 | T2 €3.65 · R/R 2.0 | T3 €3.77 · R/R 3.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €3.29


## Edge, scénarios & sizing

- EV/risk : 0.021 | EV/share : €0.003 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 22 % | T2 9 % | T3 9 %
- Kelly (position) : f* 0.023 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 22.2 | bear 70.4 | side 7.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.209% → cible +3.51% / stop −3.499%, p_fill 33%, n_eff≈15.0) : P(cible|rempli) **25%** · **EV/risk -0.010** (×p_fill ; si rempli -0.10% du capital)
  - **swing** (entrée dip −4.866% → cible +7.847% / stop −3.925%, p_fill 26%, n_eff≈9.4) : P(cible|rempli) **4%** · **EV/risk -0.103** (×p_fill ; si rempli -1.56% du capital)
  - **deep** (entrée dip −7.518% → cible +11.098% / stop −5.549%, p_fill 28%, n_eff≈8.2) : P(cible|rempli) **3%** · **EV/risk -0.174** (×p_fill ; si rempli -3.42% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→74% · +2.0%→48% · +3.0%→28% · +5.0%→9% · +8.0%→2%
- Range intraday médian 4.32% (p90 6.78%) · excursion haute méd. +1.87% / basse méd. −1.7%
- Profil de vol intra : ouverture 2.827% vs midi 1.196% vs clôture 1.271% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 96% · range 4% · trend ↑0%/↓0% ; spike-down 51% · recovery-V 41%)_
- **Régime intraday** : **chop** _(efficiency 0.076 ; mean-reverting — autocorr -0.13)_ ; drift intra méd. -0.069% ; recovery-V 44%
- **σ réalisé intraday** 3.558% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 65% / bas 63% / whipsaw 32%
- POC intraday (dernière séance, temps-au-prix) : 3.4627 (VA 3.4337–3.4808 ; dernier close 3.506)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.0%** sous le close veille · fill 74% · rebond 67% · **stop −3.19%** sous le fill (sous le bruit) · cible +1.65% · R/R 0.52 (high win-rate)
- Gaps overnight (n=159) : méd. -0.04% · baisse 51% (gap-down >1% 22% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.61% (p90 −2.71%) · haut méd +0.62% · range méd 1.44%
- Excursion ouverture 15min (n=160) : bas méd −0.82% (p90 −2.78%) · haut méd +0.85% · range méd 1.76%
- Excursion ouverture 30min (n=160) : bas méd −1.01% (p90 −2.83%) · haut méd +0.96% · range méd 2.2%
- Excursion ouverture 60min (n=160) : bas méd −1.1% (p90 −3.18%) · haut méd +0.97% · range méd 2.45%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.506 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 84% (133/159) · gap 32% · délai 0.2min · rebond 66% (88/133) (MFE +1.59%)
   - −1.0% : fill 30min 54% · séance 74% (119/159) · gap 22% · délai 0.4min · rebond 67% (78/119) (MFE +1.65%)
   - −1.5% : fill 30min 39% · séance 60% (99/159) · gap 16% · délai 1.2min · rebond 63% (64/99) (MFE +1.49%)
   - −2.0% : fill 30min 29% · séance 48% (79/159) · gap 10% · délai 14.3min · rebond 63% (52/79) (MFE +1.42%)
   - −3.0% : fill 30min 16% · séance 32% (56/159) · gap 5% · délai 30.4min · rebond 68% (42/56) (MFE +1.66%)
   - −4.0% : fill 30min 8% · séance 18% (30/159) · gap 2% · délai 35.3min · rebond 49% (18/30) (MFE +1.04%)
   - −5.0% : fill 30min 6% · séance 9% (17/159) · gap 2% · délai 5.0min · rebond 50% (11/17) (MFE +1.35%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.35% (p90 −2.51%) → stop au-delà de −1.48% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −1.92%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.62% (p90 −1.94%) → stop au-delà de −1.35% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=813 jambes) : jambe baissière méd −1.09% (p90 −2.33%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (63 séances) :
      · −1.0% : fill 95% (60/63) · rebond 71% (37/60)
      · −2.0% : fill 64% (44/63) · rebond 60% (28/44)
      · −3.0% : fill 38% (32/63) · rebond 68% (24/32)
      · −4.0% : fill 26% (20/63) · rebond 56% (14/20)
      · −5.0% : fill 16% (13/63) · rebond 57% (9/13)
   - **flat** (43 séances) :
      · −1.0% : fill 79% (34/43) · rebond 68% (26/34)
      · −2.0% : fill 53% (19/43) · rebond 68% (13/19)
      · −3.0% : fill 40% (12/43) · rebond 73% (9/12)
      · −4.0% : fill 17% (5/43) · rebond 20% (1/5)
      · −5.0% : fill 8% (3/43) · rebond 27% (1/3)
   - **gap-up** (53 séances) :
      · −1.0% : fill 41% (25/53) · rebond 55% (15/25)
      · −2.0% : fill 22% (16/53) · rebond 61% (11/16)
      · −3.0% : fill 17% (12/53) · rebond 57% (9/12)
      · −4.0% : fill 7% (5/53) · rebond 80% (3/5)
      · −5.0% : fill 1% (1/53) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 57% en base · 68% si les 15 1res min sont vertes (77 cas) · 46% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **6min** → P(séance verte=clôture>ouverture) 70% si début vert vs 45% si rouge (base 57% · écart 25 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **70%** · continue >prix actuel 50% ; creux résiduel méd -1.84% (q20 -2.74%) → **SL/trailing à −2.74%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.39% / q75 +2.38% → **scale +1.39% / runner +2.38%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **45%** (continue à baisser 38%) → **RÉDUIRE ~55%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.8%** (au-delà de la MAE q10 -4.8%), cible rebond +2.33% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.76% .. +2.49%] · haut q95 +3.51% · bas q05 -3.49%
   - 60min (n=160) : retour [-3.2% .. +3.32%] · haut q95 +4.51% · bas q05 -3.7%
   - 2h (n=160) : retour [-3.49% .. +3.24%] · haut q95 +4.63% · bas q05 -4.3%
   - 4h (n=160) : retour [-3.08% .. +3.27%] · haut q95 +4.63% · bas q05 -5.51%
   - 6h (n=160) : retour [-3.48% .. +3.31%] · haut q95 +5.18% · bas q05 -5.44%
   - session (n=160) : retour [-4.41% .. +4.14%] · haut q95 +6.28% · bas q05 -5.91%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.97%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : stretched_down
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

- **RSI** : 10.4  _(survente)_
- **ADX** : 39.1  _(tendance etablie)_
- **MACD** : hist -0.04  _(pas de croisement recent)_
- **BB** : %B 0.3 · largeur 75.2%
- **ATR** : 0.28 (78.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.074  _(accumulation)_
- **Vol ratio** : 0.26  _(volume atone)_
- **Choppiness** : 27.7  _(marche directionnel)_
- **MA** : MA20 4.11 · MA50 4.59 · MA200 5.33  _(prix < MA20)_
- **Dist MA** : MA20 -15.3% · MA50 -24.1% · MA200 -34.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89786 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
