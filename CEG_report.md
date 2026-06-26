# CEG

**Generated** : 2026-06-26T21:54:33.288915+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $264.02  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)  
> ↳ spot $264.02 (+4.9% vs entrée) · entrée $251.66 · stop $247.40 · T1 $260.18 · R/R 2.0  
> ↳ P(T1 av. stop) 35 % _(réel 5 s)_ · EV/risk -0.011 _(réel 5 s)_ (GBM 0.137) · ¼-Kelly 0.009 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.200 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $249.96–$253.37 (mid $251.66)
- Spot actuel : $264.02 (+4.9% au-dessus de la zone — repli à attendre)
- Stop : $247.40 (stop swing_plan-based (-6.29%))
- Targets : T1 $260.18 · R/R 2.0 | T2 $268.70 · R/R 4.0 | T3 $277.22 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $247.40


## Edge, scénarios & sizing

- EV/risk : 0.137 | EV/share : $0.582 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 20 % | T3 9 %
- Kelly (position) : f* 0.036 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, swing) : bull 79.6 | bear 7.3 | side 13.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.124% → cible +1.514% / stop −1.059%, p_fill 38%, n_eff≈18.3) : P(cible|rempli) **30%** · **EV/risk +0.032** (×p_fill ; si rempli +0.09% du capital)
  - **swing** (entrée dip −4.677% → cible +3.385% / stop −1.692%, p_fill 23%, n_eff≈12.3) : P(cible|rempli) **35%** · **EV/risk -0.011** (×p_fill ; si rempli -0.08% du capital)
  - **deep** (entrée dip −7.23% → cible +4.787% / stop −2.393%, p_fill 33%, n_eff≈13.6) : P(cible|rempli) **17%** · **EV/risk -0.174** (×p_fill ; si rempli -1.28% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→66% · +2.0%→36% · +3.0%→25% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.54% (p90 5.5%) · excursion haute méd. +1.49% / basse méd. −1.55%
- Profil de vol intra : ouverture 2.517% vs midi 0.735% vs clôture 0.761% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 13% · trend ↑0%/↓1% ; spike-down 49% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.11 ; mean-reverting — autocorr -0.075)_ ; drift intra méd. -0.212% ; recovery-V 22%
- **σ réalisé intraday** 2.405% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 60% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 270.7677 (VA 269.4622–271.7002 ; dernier close 268.71)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 46% · rebond 65% · **stop −2.95%** sous le fill (sous le bruit) · cible +1.29% · R/R 0.44 (high win-rate)
- Gaps overnight (n=159) : méd. 0.2% · baisse 42% (gap-down >1% 22% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.68% (p90 −1.9%) · haut méd +0.76% · range méd 1.69%
- Excursion ouverture 15min (n=160) : bas méd −0.8% (p90 −2.3%) · haut méd +0.99% · range méd 2.06%
- Excursion ouverture 30min (n=160) : bas méd −0.88% (p90 −2.76%) · haut méd +1.08% · range méd 2.27%
- Excursion ouverture 60min (n=160) : bas méd −1.1% (p90 −3.08%) · haut méd +1.3% · range méd 2.65%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 268.71 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 72% (119/159) · gap 26% · délai 0.0min · rebond 48% (61/119) (MFE +0.95%)
   - −1.0% : fill 30min 51% · séance 63% (104/159) · gap 22% · délai 1.9min · rebond 53% (59/104) (MFE +1.06%)
   - −1.5% : fill 30min 40% · séance 55% (89/159) · gap 12% · délai 3.8min · rebond 54% (50/89) (MFE +1.17%)
   - −2.0% : fill 30min 30% · séance 46% (69/159) · gap 10% · délai 8.8min · rebond 65% (45/69) (MFE +1.29%)
   - −3.0% : fill 30min 11% · séance 26% (42/159) · gap 4% · délai 42.4min · rebond 33% (17/42) (MFE +0.66%)
   - −4.0% : fill 30min 6% · séance 16% (28/159) · gap 3% · délai 37.5min · rebond 47% (14/28) (MFE +0.93%)
   - −5.0% : fill 30min 5% · séance 8% (17/159) · gap 1% · délai 6.1min · rebond 61% (10/17) (MFE +1.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.44% (p90 −1.43%) → stop au-delà de −0.93% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.27% (p90 −1.19%) → stop au-delà de −0.88% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −1.62%) → stop au-delà de −0.99% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=476 jambes) : jambe baissière méd −1.07% (p90 −2.59%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 100% (54/54) · rebond 50% (34/54)
      · −2.0% : fill 84% (38/54) · rebond 67% (27/38)
      · −3.0% : fill 50% (23/54) · rebond 35% (9/23)
      · −4.0% : fill 37% (17/54) · rebond 46% (8/17)
      · −5.0% : fill 22% (13/54) · rebond 64% (9/13)
   - **flat** (37 séances) :
      · −1.0% : fill 67% (23/37) · rebond 39% (7/23)
      · −2.0% : fill 41% (14/37) · rebond 49% (6/14)
      · −3.0% : fill 28% (12/37) · rebond 31% (6/12)
      · −4.0% : fill 13% (7/37) · rebond 27% (3/7)
      · −5.0% : fill 4% (3/37) · rebond 50% (1/3)
   - **gap-up** (68 séances) :
      · −1.0% : fill 36% (27/68) · rebond 70% (18/27)
      · −2.0% : fill 22% (17/68) · rebond 75% (12/17)
      · −3.0% : fill 8% (7/68) · rebond 31% (2/7)
      · −4.0% : fill 4% (4/68) · rebond 90% (3/4)
      · −5.0% : fill 0% (1/68) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 71% si les 15 1res min sont vertes (91 cas) · 21% si rouges (69 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:24** → P(séance verte=clôture>ouverture) 83% si début vert vs 12% si rouge (base 50% · écart 71 pts) ; prédictivité sature ensuite (plafond brut 163min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=84) : tient le vert **83%** · continue >prix actuel 40% ; creux résiduel méd -0.93% (q20 -1.95%) → **SL/trailing à −1.95%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.84% / q75 +1.7% → **scale +0.84% / runner +1.7%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **12%** (continue à baisser 55%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.48%** (au-delà de la MAE q10 -2.48%), cible rebond +0.9% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.03% .. +2.34%] · haut q95 +3.13% · bas q05 -3.79%
   - 60min (n=160) : retour [-3.56% .. +3.06%] · haut q95 +3.51% · bas q05 -4.17%
   - 2h (n=160) : retour [-3.78% .. +3.19%] · haut q95 +4.29% · bas q05 -4.78%
   - 4h (n=160) : retour [-3.82% .. +3.35%] · haut q95 +5.28% · bas q05 -5.08%
   - 6h (n=160) : retour [-4.43% .. +3.57%] · haut q95 +5.28% · bas q05 -5.08%
   - session (n=160) : retour [-4.33% .. +3.6%] · haut q95 +5.28% · bas q05 -5.08%


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.45 · part idiosyncratique 0.55
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 57.4  _(momentum haussier)_
- **ADX** : 15.2  _(pas de tendance nette)_
- **MACD** : hist 1.951  _(pas de croisement recent)_
- **BB** : %B 0.51 · largeur 16.6%
- **ATR** : 9.12 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.199  _(distribution)_
- **Vol ratio** : 0.82  _(volume normal)_
- **Choppiness** : 41.9  _(transition)_
- **MA** : MA20 263.8 · MA50 282.18 · MA200 317.61  _(prix > MA20)_
- **Dist MA** : MA20 +0.1% · MA50 -6.4% · MA200 -16.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (69157 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
