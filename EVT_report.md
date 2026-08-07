# EVT

**Generated** : 2026-08-07T21:38:56.954534+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €3.46  

> 🟡 **WAIT-FOR-DIP** — spot +2.1 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €3.46 (+2.1% vs entrée) · entrée €3.39 · stop €3.27 · T1 €3.51 · R/R 1.0  
> ↳ P(T1 av. stop) 16 % _(réel 5 s)_ · EV/risk 0.002 _(réel 5 s)_ (GBM -0.032) · ¼-Kelly 0.002 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.5% cohérent avec le bruit 5 s (EV-optimal ≈ −3.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €3.37–€3.42 (mid €3.39)
- Spot actuel : €3.46 (+2.1% au-dessus de la zone — repli à attendre)
- Stop : €3.27 (stop swing_plan-based (-8.3%))
- Targets : T1 €3.51 · R/R 1.0 | T2 €3.63 · R/R 2.0 | T3 €3.75 · R/R 3.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €3.27


## Edge, scénarios & sizing

- EV/risk : -0.032 | EV/share : €-0.004 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 19 % | T2 6 % | T3 6 %
- Kelly (position) : f* 0.007 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 26.9 | bear 17.5 | side 55.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.083% → cible +3.491% / stop −3.499%, p_fill 35%, n_eff≈15.2) : P(cible|rempli) **16%** · **EV/risk +0.002** (×p_fill ; si rempli +0.01% du capital)
  - **swing** (entrée dip −4.576% → cible +7.805% / stop −3.902%, p_fill 21%, n_eff≈10.3) : P(cible|rempli) **3%** · **EV/risk -0.105** (×p_fill ; si rempli -1.98% du capital)
  - **deep** (entrée dip −7.067% → cible +11.037% / stop −5.964%, p_fill 23%, n_eff≈9.6) : P(cible|rempli) **3%** · **EV/risk -0.110** (×p_fill ; si rempli -2.89% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→70% · +2.0%→45% · +3.0%→24% · +5.0%→6% · +8.0%→1%
- Range intraday médian 4.03% (p90 6.25%) · excursion haute méd. +1.74% / basse méd. −1.8%
- Profil de vol intra : ouverture 2.673% vs midi 1.214% vs clôture 1.197% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 96% · range 4% · trend ↑0%/↓0% ; spike-down 54% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.072 ; mean-reverting — autocorr -0.142)_ ; drift intra méd. -0.434% ; recovery-V 30%
- **σ réalisé intraday** 3.284% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 63% / bas 70% / whipsaw 36%
- POC intraday (dernière séance, temps-au-prix) : 3.4952 (VA 3.4603–3.5027 ; dernier close 3.449)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.0%** sous le close veille · fill 70% · rebond 67% · **stop −3.18%** sous le fill (sous le bruit) · cible +1.59% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. 0.11% · baisse 44% (gap-down >1% 19% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −0.68% (p90 −2.34%) · haut méd +0.61% · range méd 1.44%
- Excursion ouverture 15min (n=160) : bas méd −0.82% (p90 −2.66%) · haut méd +0.84% · range méd 1.74%
- Excursion ouverture 30min (n=160) : bas méd −0.99% (p90 −2.77%) · haut méd +0.95% · range méd 2.06%
- Excursion ouverture 60min (n=160) : bas méd −1.08% (p90 −2.98%) · haut méd +0.96% · range méd 2.38%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.449 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 83% (132/159) · gap 27% · délai 0.2min · rebond 68% (86/132) (MFE +1.45%)
   - −1.0% : fill 30min 49% · séance 70% (116/159) · gap 19% · délai 0.6min · rebond 67% (74/116) (MFE +1.59%)
   - −1.5% : fill 30min 34% · séance 56% (97/159) · gap 14% · délai 2.8min · rebond 60% (61/97) (MFE +1.32%)
   - −2.0% : fill 30min 25% · séance 44% (77/159) · gap 8% · délai 14.9min · rebond 64% (50/77) (MFE +1.43%)
   - −3.0% : fill 30min 13% · séance 28% (53/159) · gap 5% · délai 31.1min · rebond 68% (39/53) (MFE +1.65%)
   - −4.0% : fill 30min 7% · séance 16% (30/159) · gap 2% · délai 35.3min · rebond 49% (18/30) (MFE +1.04%)
   - −5.0% : fill 30min 5% · séance 8% (17/159) · gap 1% · délai 5.0min · rebond 50% (11/17) (MFE +1.35%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.31% (p90 −2.42%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.4% (p90 −1.86%) → stop au-delà de −1.26% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.64% (p90 −1.95%) → stop au-delà de −1.35% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=812 jambes) : jambe baissière méd −1.08% (p90 −2.31%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (59 séances) :
      · −1.0% : fill 95% (56/59) · rebond 71% (33/56)
      · −2.0% : fill 64% (41/59) · rebond 60% (25/41)
      · −3.0% : fill 38% (29/59) · rebond 68% (21/29)
      · −4.0% : fill 27% (20/59) · rebond 56% (14/20)
      · −5.0% : fill 16% (13/59) · rebond 57% (9/13)
   - **flat** (42 séances) :
      · −1.0% : fill 74% (32/42) · rebond 68% (24/32)
      · −2.0% : fill 50% (19/42) · rebond 68% (13/19)
      · −3.0% : fill 38% (12/42) · rebond 73% (9/12)
      · −4.0% : fill 16% (5/42) · rebond 20% (1/5)
      · −5.0% : fill 8% (3/42) · rebond 27% (1/3)
   - **gap-up** (58 séances) :
      · −1.0% : fill 43% (28/58) · rebond 59% (17/28)
      · −2.0% : fill 21% (17/58) · rebond 70% (12/17)
      · −3.0% : fill 12% (12/58) · rebond 57% (9/12)
      · −4.0% : fill 5% (5/58) · rebond 80% (3/5)
      · −5.0% : fill 1% (1/58) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 60% si les 15 1res min sont vertes (75 cas) · 40% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **6min** → P(séance verte=clôture>ouverture) 62% si début vert vs 39% si rouge (base 50% · écart 23 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **62%** · continue >prix actuel 44% ; creux résiduel méd -1.85% (q20 -2.97%) → **SL/trailing à −2.97%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.29% / q75 +2.11% → **scale +1.29% / runner +2.11%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **39%** (continue à baisser 43%) → **RÉDUIRE ~61%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.5%** (au-delà de la MAE q10 -4.5%), cible rebond +2.02% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.44% .. +2.41%] · haut q95 +3.5% · bas q05 -3.42%
   - 60min (n=160) : retour [-3.06% .. +2.81%] · haut q95 +4.27% · bas q05 -3.49%
   - 2h (n=160) : retour [-3.48% .. +3.15%] · haut q95 +4.32% · bas q05 -4.22%
   - 4h (n=160) : retour [-2.84% .. +2.75%] · haut q95 +4.32% · bas q05 -4.3%
   - 6h (n=160) : retour [-3.32% .. +3.22%] · haut q95 +4.52% · bas q05 -5.14%
   - session (n=160) : retour [-4.14% .. +4.06%] · haut q95 +5.51% · bas q05 -5.61%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.93%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 52.3  _(neutre)_
- **ADX** : 40.8  _(tendance tres forte)_
- **MACD** : hist 0.031  _(bullish_recent)_
- **BB** : %B 0.41 · largeur 50.1%
- **ATR** : 0.13 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.05  _(neutre)_
- **Vol ratio** : 0.57  _(volume atone)_
- **Choppiness** : 70.6  _(marche en range (choppy))_
- **MA** : MA20 3.63 · MA50 4.4 · MA200 5.23  _(prix < MA20)_
- **Dist MA** : MA20 -4.6% · MA50 -21.2% · MA200 -33.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89545 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
