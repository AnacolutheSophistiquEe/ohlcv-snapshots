# CEG

**Generated** : 2026-06-25T00:19:35.989598+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $267.97  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)  
> ↳ spot $267.97 (+1.8% vs entrée) · entrée $263.35 · stop $258.69 · T1 $272.65 · R/R 2.0  
> ↳ P(T1 av. stop) 20 % _(réel 5 s)_ · EV/risk -0.258 _(réel 5 s)_ (GBM 0.135) · ¼-Kelly 0.009 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.180 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $261.49–$265.21 (mid $263.35)
- Spot actuel : $267.97 (+1.8% au-dessus de la zone — repli à attendre)
- Stop : $258.69 (stop swing_plan-based (-3.46%))
- Targets : T1 $272.65 · R/R 2.0 | T2 $281.95 · R/R 3.99 | T3 $291.26 · R/R 5.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $258.69


## Edge, scénarios & sizing

- EV/risk : 0.135 | EV/share : $0.626 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 20 % | T3 9 %
- Kelly (position) : f* 0.035 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, swing) : bull 80.0 | bear 7.6 | side 12.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.788% → cible +1.58% / stop −1.04%, p_fill 73%, n_eff≈30.4) : P(cible|rempli) **45%** · **EV/risk +0.060** (×p_fill ; si rempli +0.09% du capital)
  - **swing** (entrée dip −1.724% → cible +3.533% / stop −1.766%, p_fill 57%, n_eff≈26.5) : P(cible|rempli) **20%** · **EV/risk -0.258** (×p_fill ; si rempli -0.80% du capital)
  - **deep** (entrée dip −2.669% → cible +4.996% / stop −2.498%, p_fill 74%, n_eff≈26.5) : P(cible|rempli) **19%** · **EV/risk -0.362** (×p_fill ; si rempli -1.22% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→66% · +2.0%→36% · +3.0%→26% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.67% (p90 5.5%) · excursion haute méd. +1.49% / basse méd. −1.55%
- Profil de vol intra : ouverture 2.535% vs midi 0.738% vs clôture 0.762% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓1% ; spike-down 49% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.112 ; mean-reverting — autocorr -0.066)_ ; drift intra méd. -0.115% ; recovery-V 24%
- **σ réalisé intraday** 2.383% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 56% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 274.1845 (VA 272.8755–275.3065 ; dernier close 270.25)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 47% · rebond 65% · **stop −2.95%** sous le fill (sous le bruit) · cible +1.29% · R/R 0.44 (high win-rate)
- Gaps overnight (n=159) : méd. 0.12% · baisse 44% (gap-down >1% 23% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.68% (p90 −1.96%) · haut méd +0.76% · range méd 1.69%
- Excursion ouverture 15min (n=160) : bas méd −0.8% (p90 −2.32%) · haut méd +0.97% · range méd 2.06%
- Excursion ouverture 30min (n=160) : bas méd −0.88% (p90 −2.87%) · haut méd +1.08% · range méd 2.28%
- Excursion ouverture 60min (n=160) : bas méd −1.11% (p90 −3.13%) · haut méd +1.3% · range méd 2.75%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 270.25 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 73% (120/159) · gap 27% · délai 0.0min · rebond 46% (61/120) (MFE +0.93%)
   - −1.0% : fill 30min 53% · séance 64% (105/159) · gap 23% · délai 1.6min · rebond 55% (60/105) (MFE +1.11%)
   - −1.5% : fill 30min 41% · séance 57% (91/159) · gap 13% · délai 3.8min · rebond 54% (51/91) (MFE +1.17%)
   - −2.0% : fill 30min 31% · séance 47% (71/159) · gap 10% · délai 8.6min · rebond 65% (46/71) (MFE +1.29%)
   - −3.0% : fill 30min 12% · séance 27% (43/159) · gap 4% · délai 42.0min · rebond 33% (17/43) (MFE +0.65%)
   - −4.0% : fill 30min 7% · séance 17% (29/159) · gap 3% · délai 37.4min · rebond 48% (15/29) (MFE +0.94%)
   - −5.0% : fill 30min 5% · séance 9% (18/159) · gap 1% · délai 6.5min · rebond 60% (10/18) (MFE +1.7%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.47% (p90 −1.43%) → stop au-delà de −0.94% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.3% (p90 −1.21%) → stop au-delà de −0.92% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −1.62%) → stop au-delà de −0.99% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=478 jambes) : jambe baissière méd −1.06% (p90 −2.62%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 100% (56/56) · rebond 50% (35/56)
      · −2.0% : fill 84% (40/56) · rebond 67% (28/40)
      · −3.0% : fill 50% (24/56) · rebond 34% (9/24)
      · −4.0% : fill 37% (18/56) · rebond 46% (9/18)
      · −5.0% : fill 23% (14/56) · rebond 63% (9/14)
   - **flat** (37 séances) :
      · −1.0% : fill 67% (23/37) · rebond 39% (7/23)
      · −2.0% : fill 41% (14/37) · rebond 49% (6/14)
      · −3.0% : fill 28% (12/37) · rebond 31% (6/12)
      · −4.0% : fill 13% (7/37) · rebond 27% (3/7)
      · −5.0% : fill 4% (3/37) · rebond 50% (1/3)
   - **gap-up** (66 séances) :
      · −1.0% : fill 36% (26/66) · rebond 79% (18/26)
      · −2.0% : fill 24% (17/66) · rebond 75% (12/17)
      · −3.0% : fill 9% (7/66) · rebond 31% (2/7)
      · −4.0% : fill 4% (4/66) · rebond 90% (3/4)
      · −5.0% : fill 0% (1/66) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 73% si les 15 1res min sont vertes (90 cas) · 22% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.04% .. +2.35%] · haut q95 +3.19% · bas q05 -3.83%
   - 60min (n=160) : retour [-3.65% .. +3.07%] · haut q95 +3.54% · bas q05 -4.21%
   - session (n=160) : retour [-4.36% .. +3.69%] · haut q95 +5.28% · bas q05 -5.29%


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.31 · part idiosyncratique 0.69
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US Core PCE Price Index (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 50.5  _(neutre)_
- **ADX** : 16.7  _(pas de tendance nette)_
- **MACD** : hist 2.594  _(pas de croisement recent)_
- **BB** : %B 0.54 · largeur 19.8%
- **ATR** : 9.22 (2.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.18  _(distribution)_
- **Vol ratio** : 0.6  _(volume atone)_
- **Choppiness** : 42.3  _(transition)_
- **MA** : MA20 265.91 · MA50 283.34 · MA200 317.93  _(prix > MA20)_
- **Dist MA** : MA20 +0.8% · MA50 -5.4% · MA200 -15.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (43127 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
