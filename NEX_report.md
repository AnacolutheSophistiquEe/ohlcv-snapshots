# NEX

**Generated** : 2026-07-24T00:06:50.624980+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €133.40  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €133.40 (+1.7% vs entrée) · entrée €131.14 · stop €129.17 · T1 €132.63 · R/R 0.76  
> ↳ P(T1 av. stop) 19 % _(réel 5 s)_ · EV/risk -0.264 _(réel 5 s)_ (GBM 0.001) · ¼-Kelly 0.005 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €130.84–€131.44 (mid €131.14)
- Spot actuel : €133.40 (+1.7% au-dessus de la zone — repli à attendre)
- Stop : €129.17 (stop swing_plan-based (-4.95%))
- Targets : T1 €132.63 · R/R 0.76 | T2 €134.12 · R/R 1.51 | T3 €135.60 · R/R 2.26
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €129.17


## Edge, scénarios & sizing

- EV/risk : 0.001 | EV/share : €0.001 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 24 % | T3 8 %
- Kelly (position) : f* 0.022 | ¼-Kelly 0.005 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 44.7 | bear 10.3 | side 45.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 133.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.695% → cible +1.135% / stop −1.5%, p_fill 41%, n_eff≈18.5) : P(cible|rempli) **19%** · **EV/risk -0.264** (×p_fill ; si rempli -0.95% du capital)
  - **swing** (entrée dip −3.728% → cible +2.538% / stop −1.269%, p_fill 36%, n_eff≈13.7) : P(cible|rempli) **42%** · **EV/risk +0.062** (×p_fill ; si rempli +0.22% du capital)
  - **deep** (entrée dip −5.769% → cible +3.59% / stop −1.795%, p_fill 40%, n_eff≈12.5) : P(cible|rempli) **48%** · **EV/risk +0.144** (×p_fill ; si rempli +0.65% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→71% · +1.0%→60% · +2.0%→30% · +3.0%→12% · +5.0%→5% · +8.0%→1%
- Range intraday médian 3.03% (p90 4.67%) · excursion haute méd. +1.42% / basse méd. −0.99%
- Profil de vol intra : ouverture 1.709% vs midi 0.538% vs clôture 0.759% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (137 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 45% · recovery-V 18%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; neutre — autocorr -0.021)_ ; drift intra méd. -0.5% ; recovery-V 8%
- **σ réalisé intraday** 2.087% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 64% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 134.5206 (VA 134.3819–135.6769 ; dernier close 134.7)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 23% · rebond 55% · **stop −1.88%** sous le fill (sous le bruit) · cible +1.17% · R/R 0.62 (high win-rate)
- Gaps overnight (n=136) : méd. 0.13% · baisse 40% (gap-down >1% 11% · >2% 3%)
- Excursion ouverture 5min (n=137) : bas méd −0.46% (p90 −1.97%) · haut méd +0.3% · range méd 1.05%
- Excursion ouverture 15min (n=137) : bas méd −0.59% (p90 −2.15%) · haut méd +0.43% · range méd 1.29%
- Excursion ouverture 30min (n=137) : bas méd −0.6% (p90 −2.38%) · haut méd +0.54% · range méd 1.41%
- Excursion ouverture 60min (n=137) : bas méd −0.66% (p90 −2.51%) · haut méd +0.6% · range méd 1.56%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 134.7 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 72% (97/136) · gap 25% · délai 0.4min · rebond 50% (49/97) (MFE +0.99%)
   - −1.0% : fill 30min 39% · séance 62% (80/136) · gap 11% · délai 8.0min · rebond 41% (36/80) (MFE +0.69%)
   - −1.5% : fill 30min 26% · séance 48% (59/136) · gap 3% · délai 6.0min · rebond 44% (27/59) (MFE +0.71%)
   - −2.0% : fill 30min 17% · séance 35% (45/136) · gap 3% · délai 36.7min · rebond 48% (24/45) (MFE +0.99%)
   - −3.0% : fill 30min 5% · séance 23% (28/136) · gap 1% · délai 126.7min · rebond 55% (16/28) (MFE +1.17%)
   - −4.0% : fill 30min 1% · séance 8% (10/136) · gap 1% · délai 277.7min · rebond 20% (4/10) (MFE +0.82%)
   - −5.0% : fill 30min 1% · séance 3% (4/136) · gap 0% · délai 184.5min · rebond 89% (3/4) (MFE +1.52%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.08% (p90 −0.96%) → stop au-delà de −0.6% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −0.9%) → stop au-delà de −0.6% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.19% (p90 −1.32%) → stop au-delà de −0.6% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=271 jambes) : jambe baissière méd −1.08% (p90 −2.47%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (43 séances) :
      · −1.0% : fill 78% (35/43) · rebond 40% (14/35)
      · −2.0% : fill 48% (25/43) · rebond 43% (13/25)
      · −3.0% : fill 33% (16/43) · rebond 47% (9/16)
      · −4.0% : fill 16% (7/43) · rebond 28% (3/7)
      · −5.0% : fill 9% (4/43) · rebond 89% (3/4)
   - **flat** (31 séances) :
      · −1.0% : fill 66% (20/31) · rebond 49% (11/20)
      · −2.0% : fill 32% (9/31) · rebond 63% (5/9)
      · −3.0% : fill 26% (6/31) · rebond 42% (2/6)
      · −4.0% : fill 6% (1/31) · rebond 0% (0/1)
      · −5.0% : fill 0% (0/31) · rebond 0% (0/0)
   - **gap-up** (62 séances) :
      · −1.0% : fill 48% (25/62) · rebond 36% (11/25)
      · −2.0% : fill 27% (11/62) · rebond 44% (6/11)
      · −3.0% : fill 15% (6/62) · rebond 77% (5/6)
      · −4.0% : fill 4% (2/62) · rebond 15% (1/2)
      · −5.0% : fill 0% (0/62) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=137) : 48% en base · 74% si les 15 1res min sont vertes (74 cas) · 16% si rouges (63 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=137) : COUDE à **28min** → P(séance verte=clôture>ouverture) 85% si début vert vs 16% si rouge (base 48% · écart 68 pts) ; prédictivité sature ensuite (plafond brut 28min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=65) : tient le vert **85%** · continue >prix actuel 57% ; creux résiduel méd -0.96% (q20 -1.74%) → **SL/trailing à −1.74%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.23% / q75 +1.99% → **scale +1.23% / runner +1.99%**, sortie à la clôture
  - **si ROUGE au coude** (n=72) : edge inversé — récupère vert seulement **16%** (continue à baisser 58%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.09%** (au-delà de la MAE q10 -3.09%), cible rebond +1.01% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=137) : retour [-2.15% .. +1.84%] · haut q95 +2.33% · bas q05 -2.86%
   - 60min (n=137) : retour [-2.77% .. +2.06%] · haut q95 +2.4% · bas q05 -3.21%
   - 2h (n=137) : retour [-3.57% .. +2.19%] · haut q95 +2.67% · bas q05 -3.74%
   - 4h (n=137) : retour [-3.26% .. +2.53%] · haut q95 +2.91% · bas q05 -3.92%
   - 6h (n=137) : retour [-3.44% .. +3.5%] · haut q95 +4.06% · bas q05 -4.18%
   - session (n=137) : retour [-3.56% .. +2.91%] · haut q95 +4.2% · bas q05 -4.56%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.5% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.94%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 32.8  _(momentum baissier)_
- **ADX** : 32.3  _(tendance etablie)_
- **MACD** : hist 0.278  _(bullish_recent)_
- **BB** : %B 0.3 · largeur 11.7%
- **ATR** : 4.08 (56.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.081  _(accumulation)_
- **Vol ratio** : 0.33  _(volume atone)_
- **Choppiness** : 61.7  _(transition)_
- **MA** : MA20 136.65 · MA50 147.52 · MA200 131.32  _(prix < MA20)_
- **Dist MA** : MA20 -2.4% · MA50 -9.6% · MA200 +1.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92577 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
