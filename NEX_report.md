# NEX

**Generated** : 2026-07-22T00:07:59.236232+00:00  
**Santé technique** : 4/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €134.80  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot €134.80 (+4.5% vs entrée) · entrée €129.05 · stop €127.39 · T1 €132.37 · R/R 2.0  
> ↳ P(T1 av. stop) 39 % · EV/risk 0.12 · ¼-Kelly 0.011 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €128.39–€129.72 (mid €129.05)
- Spot actuel : €134.80 (+4.5% au-dessus de la zone — repli à attendre)
- Stop : €127.39 (stop swing_plan-based (-5.49%))
- Targets : T1 €132.37 · R/R 2.0 | T2 €135.69 · R/R 4.0 | T3 €139.01 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €127.39


## Edge, scénarios & sizing

- EV/risk : 0.12 | EV/share : €0.199 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 18 % | T3 8 %
- Kelly (position) : f* 0.044 | ¼-Kelly 0.011 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 10.3 | bear 54.8 | side 34.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 135.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.939% → cible +1.15% / stop −1.5%, p_fill 43%, n_eff≈18.3) : P(cible|rempli) **14%** · **EV/risk -0.260** (×p_fill ; si rempli -0.90% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=11, n_eff=9))
  - **deep** : indisponible (échantillon insuffisant (n=13, n_eff=11))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→71% · +1.0%→61% · +2.0%→30% · +3.0%→12% · +5.0%→5% · +8.0%→1%
- Range intraday médian 3.06% (p90 4.67%) · excursion haute méd. +1.42% / basse méd. −1.03%
- Profil de vol intra : ouverture 1.726% vs midi 0.545% vs clôture 0.758% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (136 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 46% · recovery-V 18%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; neutre — autocorr -0.019)_ ; drift intra méd. -0.516% ; recovery-V 8%
- **σ réalisé intraday** 2.13% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 59% / bas 62% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 135.55 (VA 135.35–136.65 ; dernier close 133.5)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 24% · rebond 55% · **stop −1.88%** sous le fill (sous le bruit) · cible +1.17% · R/R 0.62 (high win-rate)
- Gaps overnight (n=135) : méd. 0.13% · baisse 41% (gap-down >1% 11% · >2% 3%)
- Excursion ouverture 5min (n=136) : bas méd −0.45% (p90 −2.0%) · haut méd +0.3% · range méd 1.09%
- Excursion ouverture 15min (n=136) : bas méd −0.58% (p90 −2.15%) · haut méd +0.39% · range méd 1.3%
- Excursion ouverture 30min (n=136) : bas méd −0.6% (p90 −2.39%) · haut méd +0.47% · range méd 1.42%
- Excursion ouverture 60min (n=136) : bas méd −0.7% (p90 −2.51%) · haut méd +0.59% · range méd 1.57%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 133.5 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 73% (97/135) · gap 26% · délai 0.4min · rebond 50% (49/97) (MFE +0.99%)
   - −1.0% : fill 30min 40% · séance 63% (80/135) · gap 11% · délai 8.0min · rebond 41% (36/80) (MFE +0.69%)
   - −1.5% : fill 30min 27% · séance 49% (59/135) · gap 3% · délai 6.0min · rebond 44% (27/59) (MFE +0.71%)
   - −2.0% : fill 30min 18% · séance 35% (45/135) · gap 3% · délai 36.7min · rebond 48% (24/45) (MFE +0.99%)
   - −3.0% : fill 30min 5% · séance 24% (28/135) · gap 1% · délai 126.7min · rebond 55% (16/28) (MFE +1.17%)
   - −4.0% : fill 30min 1% · séance 8% (10/135) · gap 1% · délai 277.7min · rebond 20% (4/10) (MFE +0.82%)
   - −5.0% : fill 30min 1% · séance 3% (4/135) · gap 0% · délai 184.5min · rebond 89% (3/4) (MFE +1.52%)
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
   - **gap-up** (61 séances) :
      · −1.0% : fill 50% (25/61) · rebond 36% (11/25)
      · −2.0% : fill 28% (11/61) · rebond 44% (6/11)
      · −3.0% : fill 16% (6/61) · rebond 77% (5/6)
      · −4.0% : fill 4% (2/61) · rebond 15% (1/2)
      · −5.0% : fill 0% (0/61) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=136) : 49% en base · 77% si les 15 1res min sont vertes (73 cas) · 16% si rouges (63 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=136) : COUDE à **28min** → P(séance verte=clôture>ouverture) 85% si début vert vs 17% si rouge (base 49% · écart 68 pts) ; prédictivité sature ensuite (plafond brut 28min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=65) : tient le vert **85%** · continue >prix actuel 57% ; creux résiduel méd -0.96% (q20 -1.74%) → **SL/trailing à −1.74%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.23% / q75 +1.99% → **scale +1.23% / runner +1.99%**, sortie à la clôture
  - **si ROUGE au coude** (n=71) : edge inversé — récupère vert seulement **17%** (continue à baisser 57%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.14%** (au-delà de la MAE q10 -3.14%), cible rebond +1.03% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=136) : retour [-2.18% .. +1.86%] · haut q95 +2.34% · bas q05 -2.86%
   - 60min (n=136) : retour [-2.79% .. +2.06%] · haut q95 +2.41% · bas q05 -3.21%
   - 2h (n=136) : retour [-3.58% .. +2.2%] · haut q95 +2.69% · bas q05 -3.74%
   - 4h (n=136) : retour [-3.29% .. +2.55%] · haut q95 +2.92% · bas q05 -3.92%
   - 6h (n=136) : retour [-3.49% .. +3.52%] · haut q95 +4.1% · bas q05 -4.18%
   - session (n=136) : retour [-3.57% .. +2.92%] · haut q95 +4.2% · bas q05 -4.57%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.5% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.94%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 40.8  _(momentum baissier)_
- **ADX** : 32.0  _(tendance etablie)_
- **MACD** : hist 0.15  _(bullish_recent)_
- **BB** : %B 0.34 · largeur 14.8%
- **ATR** : 4.52 (72.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.025  _(neutre)_
- **Vol ratio** : 0.2  _(volume atone)_
- **Choppiness** : 62.4  _(marche en range (choppy))_
- **MA** : MA20 138.04 · MA50 148.74 · MA200 131.24  _(prix < MA20)_
- **Dist MA** : MA20 -2.3% · MA50 -9.4% · MA200 +2.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92004 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
