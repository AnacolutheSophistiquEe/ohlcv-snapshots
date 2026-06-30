# RHM

**Generated** : 2026-06-30T21:35:58.551965+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €990.50  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot €990.50 (+6.6% vs entrée) · entrée €929.25 · stop €910.66 · T1 €954.51 · R/R 1.36  
> ↳ P(T1 av. stop) 34 % · EV/risk -0.001 · ¼-Kelly 0.007 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €924.20–€934.30 (mid €929.25)
- Spot actuel : €990.50 (+6.6% au-dessus de la zone — repli à attendre)
- Stop : €910.66 (stop swing_plan-based (-15.03%))
- Targets : T1 €954.51 · R/R 1.36 | T2 €979.78 · R/R 2.72 | T3 €1005.04 · R/R 4.08
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €910.66


## Edge, scénarios & sizing

- EV/risk : -0.001 | EV/share : €-0.012 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 2 % | T3 2 %
- Kelly (position) : f* 0.028 | ¼-Kelly 0.007 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 11.1 | bear 46.7 | side 42.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=7, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→62% · +2.0%→49% · +3.0%→29% · +5.0%→2% · +8.0%→0%
- Range intraday médian 4.15% (p90 6.7%) · excursion haute méd. +1.98% / basse méd. −1.66%
- Profil de vol intra : ouverture 2.556% vs midi 0.913% vs clôture 1.021% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 53% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.091 ; neutre — autocorr 0.016)_ ; drift intra méd. -0.687% ; recovery-V 38%
- **σ réalisé intraday** 2.967% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 65% / bas 71% / whipsaw 37%
- POC intraday (dernière séance, temps-au-prix) : 949.8406 (VA 947.3094–960.8094 ; dernier close 973.3)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 47% · rebond 66% · **stop −3.38%** sous le fill (sous le bruit) · cible +1.38% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.06% · baisse 42% (gap-down >1% 17% · >2% 7%)
- Excursion ouverture 5min (n=160) : bas méd −0.69% (p90 −1.73%) · haut méd +0.57% · range méd 1.5%
- Excursion ouverture 15min (n=160) : bas méd −0.94% (p90 −1.96%) · haut méd +0.78% · range méd 1.87%
- Excursion ouverture 30min (n=160) : bas méd −0.99% (p90 −2.23%) · haut méd +0.91% · range méd 2.12%
- Excursion ouverture 60min (n=160) : bas méd −1.06% (p90 −2.5%) · haut méd +1.01% · range méd 2.25%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 973.3 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 77% (119/159) · gap 29% · délai 0.2min · rebond 55% (61/119) (MFE +1.12%)
   - −1.0% : fill 30min 48% · séance 72% (106/159) · gap 17% · délai 5.3min · rebond 60% (59/106) (MFE +1.4%)
   - −1.5% : fill 30min 30% · séance 56% (80/159) · gap 9% · délai 20.1min · rebond 56% (42/80) (MFE +1.24%)
   - −2.0% : fill 30min 24% · séance 47% (70/159) · gap 7% · délai 29.4min · rebond 66% (41/70) (MFE +1.38%)
   - −3.0% : fill 30min 10% · séance 29% (46/159) · gap 4% · délai 124.1min · rebond 65% (30/46) (MFE +1.47%)
   - −4.0% : fill 30min 5% · séance 20% (28/159) · gap 2% · délai 285.1min · rebond 51% (16/28) (MFE +1.06%)
   - −5.0% : fill 30min 2% · séance 11% (17/159) · gap 2% · délai 201.2min · rebond 49% (10/17) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.35% (p90 −1.41%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.35% (p90 −1.58%) → stop au-delà de −1.33% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.24% (p90 −1.61%) → stop au-delà de −1.25% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=467 jambes) : jambe baissière méd −1.16% (p90 −2.65%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 98% (48/49) · rebond 59% (24/48)
      · −2.0% : fill 80% (38/49) · rebond 72% (25/38)
      · −3.0% : fill 47% (27/49) · rebond 65% (19/27)
      · −4.0% : fill 34% (16/49) · rebond 54% (10/16)
      · −5.0% : fill 19% (10/49) · rebond 70% (8/10)
   - **flat** (50 séances) :
      · −1.0% : fill 77% (36/50) · rebond 72% (24/36)
      · −2.0% : fill 32% (17/50) · rebond 65% (9/17)
      · −3.0% : fill 19% (10/50) · rebond 42% (5/10)
      · −4.0% : fill 17% (8/50) · rebond 16% (2/8)
      · −5.0% : fill 15% (6/50) · rebond 22% (1/6)
   - **gap-up** (60 séances) :
      · −1.0% : fill 44% (22/60) · rebond 43% (11/22)
      · −2.0% : fill 31% (15/60) · rebond 53% (7/15)
      · −3.0% : fill 22% (9/60) · rebond 82% (6/9)
      · −4.0% : fill 10% (4/60) · rebond 100% (4/4)
      · −5.0% : fill 0% (1/60) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 65% si les 15 1res min sont vertes (86 cas) · 30% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 77% si début vert vs 20% si rouge (base 48% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 299min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **77%** · continue >prix actuel 44% ; creux résiduel méd -1.37% (q20 -2.5%) → **SL/trailing à −2.5%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.19% / q75 +1.88% → **scale +1.19% / runner +1.88%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **20%** (continue à baisser 56%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.27%** (au-delà de la MAE q10 -5.27%), cible rebond +1.04% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.63% .. +3.19%] · haut q95 +3.87% · bas q05 -3.13%
   - 60min (n=160) : retour [-2.86% .. +3.01%] · haut q95 +4.14% · bas q05 -3.46%
   - 2h (n=160) : retour [-3.45% .. +2.99%] · haut q95 +4.16% · bas q05 -4.02%
   - 4h (n=160) : retour [-3.63% .. +2.94%] · haut q95 +4.52% · bas q05 -4.52%
   - 6h (n=160) : retour [-4.56% .. +2.98%] · haut q95 +4.56% · bas q05 -5.71%
   - session (n=160) : retour [-6.74% .. +3.36%] · haut q95 +4.74% · bas q05 -7.1%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.28%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : stretched_down
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

- **RSI** : 27.2  _(survente)_
- **ADX** : 32.0  _(tendance etablie)_
- **MACD** : hist -19.098  _(pas de croisement recent)_
- **BB** : %B 0.16 · largeur 36.5%
- **ATR** : 61.25 (52.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.147  _(distribution)_
- **Vol ratio** : 1.19  _(volume normal)_
- **Choppiness** : 38.2  _(marche directionnel)_
- **MA** : MA20 1131.97 · MA50 1213.95 · MA200 1558.03  _(prix < MA20)_
- **Dist MA** : MA20 -12.5% · MA50 -18.4% · MA200 -36.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91495 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
