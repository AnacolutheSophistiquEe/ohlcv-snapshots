# RHM

**Generated** : 2026-06-30T00:02:05.919681+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite normal · €973.30  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot €973.30 (+6.6% vs entrée) · entrée €913.33 · stop €895.06 · T1 €937.97 · R/R 1.35  
> ↳ P(T1 av. stop) 35 % · EV/risk 0.01 · ¼-Kelly 0.009 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €908.40–€918.26 (mid €913.33)
- Spot actuel : €973.30 (+6.6% au-dessus de la zone — repli à attendre)
- Stop : €895.06 (stop swing_plan-based (-14.97%))
- Targets : T1 €937.97 · R/R 1.35 | T2 €962.62 · R/R 2.7 | T3 €987.26 · R/R 4.05
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €895.06


## Edge, scénarios & sizing

- EV/risk : 0.01 | EV/share : €0.177 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 2 % | T3 2 %
- Kelly (position) : f* 0.035 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 12.2 | bear 41.1 | side 46.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=7, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→62% · +2.0%→49% · +3.0%→30% · +5.0%→2% · +8.0%→0%
- Range intraday médian 4.16% (p90 6.7%) · excursion haute méd. +1.98% / basse méd. −1.72%
- Profil de vol intra : ouverture 2.561% vs midi 0.911% vs clôture 1.02% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 54% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.092 ; neutre — autocorr 0.02)_ ; drift intra méd. -0.787% ; recovery-V 34%
- **σ réalisé intraday** 2.978% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 63% / bas 70% / whipsaw 34%
- POC intraday (dernière séance, temps-au-prix) : 939.1231 (VA 935.1131–942.6319 ; dernier close 943.9)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 48% · rebond 66% · **stop −3.38%** sous le fill (sous le bruit) · cible +1.38% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.04% · baisse 43% (gap-down >1% 18% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −0.68% (p90 −1.74%) · haut méd +0.58% · range méd 1.54%
- Excursion ouverture 15min (n=160) : bas méd −0.91% (p90 −1.97%) · haut méd +0.8% · range méd 1.9%
- Excursion ouverture 30min (n=160) : bas méd −0.98% (p90 −2.23%) · haut méd +0.98% · range méd 2.15%
- Excursion ouverture 60min (n=160) : bas méd −1.05% (p90 −2.52%) · haut méd +1.01% · range méd 2.25%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 943.9 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 78% (120/159) · gap 29% · délai 0.2min · rebond 55% (62/120) (MFE +1.12%)
   - −1.0% : fill 30min 49% · séance 73% (107/159) · gap 18% · délai 5.3min · rebond 60% (60/107) (MFE +1.41%)
   - −1.5% : fill 30min 31% · séance 57% (80/159) · gap 9% · délai 20.1min · rebond 56% (42/80) (MFE +1.24%)
   - −2.0% : fill 30min 24% · séance 48% (70/159) · gap 8% · délai 29.4min · rebond 66% (41/70) (MFE +1.38%)
   - −3.0% : fill 30min 10% · séance 30% (46/159) · gap 4% · délai 124.1min · rebond 65% (30/46) (MFE +1.47%)
   - −4.0% : fill 30min 5% · séance 20% (28/159) · gap 2% · délai 285.1min · rebond 51% (16/28) (MFE +1.06%)
   - −5.0% : fill 30min 2% · séance 11% (17/159) · gap 2% · délai 201.2min · rebond 49% (10/17) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.31% (p90 −1.45%) → stop au-delà de −1.12% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.29% (p90 −1.59%) → stop au-delà de −1.3% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.24% (p90 −1.61%) → stop au-delà de −1.25% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=462 jambes) : jambe baissière méd −1.19% (p90 −2.66%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 98% (49/50) · rebond 59% (25/49)
      · −2.0% : fill 80% (38/50) · rebond 72% (25/38)
      · −3.0% : fill 47% (27/50) · rebond 65% (19/27)
      · −4.0% : fill 34% (16/50) · rebond 54% (10/16)
      · −5.0% : fill 19% (10/50) · rebond 70% (8/10)
   - **flat** (50 séances) :
      · −1.0% : fill 77% (36/50) · rebond 72% (24/36)
      · −2.0% : fill 32% (17/50) · rebond 65% (9/17)
      · −3.0% : fill 19% (10/50) · rebond 42% (5/10)
      · −4.0% : fill 17% (8/50) · rebond 16% (2/8)
      · −5.0% : fill 15% (6/50) · rebond 22% (1/6)
   - **gap-up** (59 séances) :
      · −1.0% : fill 46% (22/59) · rebond 43% (11/22)
      · −2.0% : fill 33% (15/59) · rebond 53% (7/15)
      · −3.0% : fill 24% (9/59) · rebond 82% (6/9)
      · −4.0% : fill 10% (4/59) · rebond 100% (4/4)
      · −5.0% : fill 0% (1/59) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 64% si les 15 1res min sont vertes (86 cas) · 30% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:32** → P(séance verte=clôture>ouverture) 79% si début vert vs 15% si rouge (base 48% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 299min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=84) : tient le vert **79%** · continue >prix actuel 55% ; creux résiduel méd -1.05% (q20 -2.81%) → **SL/trailing à −2.81%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.28% / q75 +1.99% → **scale +1.28% / runner +1.99%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **15%** (continue à baisser 55%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.82%** (au-delà de la MAE q10 -4.82%), cible rebond +1.08% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.63% .. +3.2%] · haut q95 +3.88% · bas q05 -3.14%
   - 60min (n=160) : retour [-2.87% .. +3.02%] · haut q95 +4.15% · bas q05 -3.46%
   - 2h (n=160) : retour [-3.48% .. +3.0%] · haut q95 +4.16% · bas q05 -4.03%
   - 4h (n=160) : retour [-3.81% .. +2.96%] · haut q95 +4.54% · bas q05 -4.53%
   - 6h (n=160) : retour [-4.6% .. +2.98%] · haut q95 +4.56% · bas q05 -5.72%
   - session (n=160) : retour [-6.81% .. +3.39%] · haut q95 +4.74% · bas q05 -7.12%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.27%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.34 · part idiosyncratique 0.66
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 23.8  _(survente)_
- **ADX** : 31.5  _(tendance etablie)_
- **MACD** : hist -22.198  _(bearish_recent)_
- **BB** : %B 0.07 · largeur 34.4%
- **ATR** : 59.97 (50.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.175  _(distribution)_
- **Vol ratio** : 0.77  _(volume normal)_
- **Choppiness** : 37.4  _(marche directionnel)_
- **MA** : MA20 1142.06 · MA50 1223.42 · MA200 1562.4  _(prix < MA20)_
- **Dist MA** : MA20 -14.8% · MA50 -20.4% · MA200 -37.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91551 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
