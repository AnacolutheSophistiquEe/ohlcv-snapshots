# CEG

**Generated** : 2026-06-25T21:55:48.075725+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $268.69  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US Core PCE Price Index (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot $268.69 (+0.9% vs entrée) · entrée $266.41 · stop $263.63 · T1 $270.42 · R/R 1.44  
> ↳ P(T1 av. stop) 36 % _(réel 5 s)_ · EV/risk -0.062 _(réel 5 s)_ (GBM 0.057) · ¼-Kelly 0.004 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.180 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $265.61–$267.21 (mid $266.41)
- Spot actuel : $268.69 (+0.9% au-dessus de la zone — repli à attendre)
- Stop : $263.63 (stop swing_plan-based (-3.52%))
- Targets : T1 $270.42 · R/R 1.44 | T2 $274.43 · R/R 2.88 | T3 $278.44 · R/R 4.33
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $263.63


## Edge, scénarios & sizing

- EV/risk : 0.057 | EV/share : $0.158 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 16 % | T3 4 %
- Kelly (position) : f* 0.017 | ¼-Kelly 0.004 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 83.7 | bear 6.7 | side 9.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.848% → cible +1.505% / stop −1.041%, p_fill 69%, n_eff≈30.0) : P(cible|rempli) **36%** · **EV/risk -0.062** (×p_fill ; si rempli -0.09% du capital)
  - **swing** (entrée dip −1.869% → cible +3.365% / stop −1.683%, p_fill 54%, n_eff≈25.6) : P(cible|rempli) **21%** · **EV/risk -0.231** (×p_fill ; si rempli -0.72% du capital)
  - **deep** (entrée dip −2.889% → cible +4.759% / stop −2.38%, p_fill 70%, n_eff≈26.3) : P(cible|rempli) **19%** · **EV/risk -0.349** (×p_fill ; si rempli -1.18% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→66% · +2.0%→36% · +3.0%→26% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.67% (p90 5.5%) · excursion haute méd. +1.49% / basse méd. −1.55%
- Profil de vol intra : ouverture 2.528% vs midi 0.74% vs clôture 0.767% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓1% ; spike-down 50% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.113 ; mean-reverting — autocorr -0.074)_ ; drift intra méd. -0.186% ; recovery-V 22%
- **σ réalisé intraday** 2.373% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 58% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 272.388 (VA 268.356–272.772 ; dernier close 267.97)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 46% · rebond 66% · **stop −2.95%** sous le fill (sous le bruit) · cible +1.29% · R/R 0.44 (high win-rate)
- Gaps overnight (n=159) : méd. 0.18% · baisse 43% (gap-down >1% 22% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.7% (p90 −1.92%) · haut méd +0.76% · range méd 1.69%
- Excursion ouverture 15min (n=160) : bas méd −0.82% (p90 −2.31%) · haut méd +0.9% · range méd 2.06%
- Excursion ouverture 30min (n=160) : bas méd −0.89% (p90 −2.83%) · haut méd +1.07% · range méd 2.26%
- Excursion ouverture 60min (n=160) : bas méd −1.13% (p90 −3.11%) · haut méd +1.29% · range méd 2.71%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 267.97 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 73% (120/159) · gap 27% · délai 0.0min · rebond 48% (62/120) (MFE +0.95%)
   - −1.0% : fill 30min 52% · séance 64% (105/159) · gap 22% · délai 1.9min · rebond 53% (60/105) (MFE +1.07%)
   - −1.5% : fill 30min 41% · séance 56% (90/159) · gap 13% · délai 3.8min · rebond 54% (51/90) (MFE +1.19%)
   - −2.0% : fill 30min 30% · séance 46% (70/159) · gap 10% · délai 8.7min · rebond 66% (46/70) (MFE +1.29%)
   - −3.0% : fill 30min 12% · séance 26% (42/159) · gap 4% · délai 42.4min · rebond 33% (17/42) (MFE +0.66%)
   - −4.0% : fill 30min 6% · séance 16% (28/159) · gap 3% · délai 37.5min · rebond 47% (14/28) (MFE +0.93%)
   - −5.0% : fill 30min 5% · séance 8% (17/159) · gap 1% · délai 6.1min · rebond 61% (10/17) (MFE +1.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.47% (p90 −1.43%) → stop au-delà de −0.94% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.3% (p90 −1.21%) → stop au-delà de −0.92% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −1.62%) → stop au-delà de −0.99% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=478 jambes) : jambe baissière méd −1.07% (p90 −2.6%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 100% (55/55) · rebond 50% (35/55)
      · −2.0% : fill 84% (39/55) · rebond 67% (28/39)
      · −3.0% : fill 50% (23/55) · rebond 35% (9/23)
      · −4.0% : fill 36% (17/55) · rebond 46% (8/17)
      · −5.0% : fill 22% (13/55) · rebond 64% (9/13)
   - **flat** (37 séances) :
      · −1.0% : fill 67% (23/37) · rebond 39% (7/23)
      · −2.0% : fill 41% (14/37) · rebond 49% (6/14)
      · −3.0% : fill 28% (12/37) · rebond 31% (6/12)
      · −4.0% : fill 13% (7/37) · rebond 27% (3/7)
      · −5.0% : fill 4% (3/37) · rebond 50% (1/3)
   - **gap-up** (67 séances) :
      · −1.0% : fill 38% (27/67) · rebond 70% (18/27)
      · −2.0% : fill 23% (17/67) · rebond 75% (12/17)
      · −3.0% : fill 9% (7/67) · rebond 31% (2/7)
      · −4.0% : fill 4% (4/67) · rebond 90% (3/4)
      · −5.0% : fill 0% (1/67) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 73% si les 15 1res min sont vertes (90 cas) · 21% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.03% .. +2.35%] · haut q95 +3.15% · bas q05 -3.81%
   - 60min (n=160) : retour [-3.62% .. +3.06%] · haut q95 +3.52% · bas q05 -4.19%
   - session (n=160) : retour [-4.34% .. +3.65%] · haut q95 +5.28% · bas q05 -5.16%


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.31 · part idiosyncratique 0.69
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US Core PCE Price Index (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 53.0  _(neutre)_
- **ADX** : 15.6  _(pas de tendance nette)_
- **MACD** : hist 2.427  _(pas de croisement recent)_
- **BB** : %B 0.58 · largeur 18.2%
- **ATR** : 9.25 (2.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.183  _(distribution)_
- **Vol ratio** : 0.67  _(volume normal)_
- **Choppiness** : 42.4  _(transition)_
- **MA** : MA20 264.91 · MA50 282.79 · MA200 317.79  _(prix > MA20)_
- **Dist MA** : MA20 +1.4% · MA50 -5.0% · MA200 -15.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (43092 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
