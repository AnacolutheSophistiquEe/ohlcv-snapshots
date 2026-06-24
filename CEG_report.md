# CEG

**Generated** : 2026-06-24T00:19:22.512391+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $270.26  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $270.26 (+2.2% vs entrée) · entrée $264.38 · stop $259.58 · T1 $273.98 · R/R 2.0  
> ↳ P(T1 av. stop) 20 % _(réel 5 s)_ · EV/risk -0.258 _(réel 5 s)_ (GBM 0.133) · ¼-Kelly 0.008 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

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
- Entry (zone de repli) : $262.46–$266.30 (mid $264.38)
- Spot actuel : $270.26 (+2.2% au-dessus de la zone — repli à attendre)
- Stop : $259.58 (stop swing_plan-based (-3.95%))
- Targets : T1 $273.98 · R/R 2.0 | T2 $283.58 · R/R 4.0 | T3 $293.19 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $259.58


## Edge, scénarios & sizing

- EV/risk : 0.133 | EV/share : $0.636 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 20 % | T3 9 %
- Kelly (position) : f* 0.034 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, swing) : bull 80.3 | bear 7.7 | side 11.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.994% → cible +1.624% / stop −1.046%, p_fill 62%, n_eff≈26.9) : P(cible|rempli) **27%** · **EV/risk -0.128** (×p_fill ; si rempli -0.22% du capital)
  - **swing** (entrée dip −2.173% → cible +3.632% / stop −1.816%, p_fill 57%, n_eff≈24.6) : P(cible|rempli) **20%** · **EV/risk -0.258** (×p_fill ; si rempli -0.82% du capital)
  - **deep** (entrée dip −3.368% → cible +5.137% / stop −2.569%, p_fill 73%, n_eff≈25.9) : P(cible|rempli) **18%** · **EV/risk -0.370** (×p_fill ; si rempli -1.31% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→66% · +2.0%→36% · +3.0%→28% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.72% (p90 5.52%) · excursion haute méd. +1.49% / basse méd. −1.6%
- Profil de vol intra : ouverture 2.553% vs midi 0.747% vs clôture 0.771% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑0%/↓1% ; spike-down 50% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.113 ; mean-reverting — autocorr -0.068)_ ; drift intra méd. -0.125% ; recovery-V 24%
- **σ réalisé intraday** 2.414% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 58% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 276.4106 (VA 273.5569–276.6009 ; dernier close 275.55)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 46% · rebond 64% · **stop −2.95%** sous le fill (sous le bruit) · cible +1.18% · R/R 0.4 (high win-rate)
- Gaps overnight (n=159) : méd. 0.18% · baisse 42% (gap-down >1% 21% · >2% 9%)
- Excursion ouverture 5min (n=160) : bas méd −0.7% (p90 −2.01%) · haut méd +0.78% · range méd 1.7%
- Excursion ouverture 15min (n=160) : bas méd −0.79% (p90 −2.32%) · haut méd +0.9% · range méd 2.06%
- Excursion ouverture 30min (n=160) : bas méd −0.9% (p90 −2.91%) · haut méd +1.07% · range méd 2.31%
- Excursion ouverture 60min (n=160) : bas méd −1.14% (p90 −3.15%) · haut méd +1.29% · range méd 2.71%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 275.55 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 72% (120/159) · gap 26% · délai 0.0min · rebond 48% (62/120) (MFE +0.95%)
   - −1.0% : fill 30min 52% · séance 63% (105/159) · gap 21% · délai 1.8min · rebond 56% (61/105) (MFE +1.18%)
   - −1.5% : fill 30min 40% · séance 57% (91/159) · gap 11% · délai 4.1min · rebond 52% (51/91) (MFE +1.06%)
   - −2.0% : fill 30min 30% · séance 46% (70/159) · gap 9% · délai 10.5min · rebond 64% (45/70) (MFE +1.18%)
   - −3.0% : fill 30min 12% · séance 27% (43/159) · gap 4% · délai 42.0min · rebond 33% (17/43) (MFE +0.65%)
   - −4.0% : fill 30min 7% · séance 17% (29/159) · gap 3% · délai 37.4min · rebond 48% (15/29) (MFE +0.94%)
   - −5.0% : fill 30min 5% · séance 9% (18/159) · gap 1% · délai 6.5min · rebond 60% (10/18) (MFE +1.7%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.44% (p90 −1.44%) → stop au-delà de −0.95% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.27% (p90 −1.23%) → stop au-delà de −0.94% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −1.62%) → stop au-delà de −0.99% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=483 jambes) : jambe baissière méd −1.06% (p90 −2.62%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 100% (55/55) · rebond 53% (35/55)
      · −2.0% : fill 83% (39/55) · rebond 65% (27/39)
      · −3.0% : fill 53% (24/55) · rebond 34% (9/24)
      · −4.0% : fill 39% (18/55) · rebond 46% (9/18)
      · −5.0% : fill 24% (14/55) · rebond 63% (9/14)
   - **flat** (37 séances) :
      · −1.0% : fill 67% (23/37) · rebond 39% (7/23)
      · −2.0% : fill 41% (14/37) · rebond 49% (6/14)
      · −3.0% : fill 28% (12/37) · rebond 31% (6/12)
      · −4.0% : fill 13% (7/37) · rebond 27% (3/7)
      · −5.0% : fill 4% (3/37) · rebond 50% (1/3)
   - **gap-up** (67 séances) :
      · −1.0% : fill 36% (27/67) · rebond 79% (19/27)
      · −2.0% : fill 24% (17/67) · rebond 75% (12/17)
      · −3.0% : fill 9% (7/67) · rebond 31% (2/7)
      · −4.0% : fill 4% (4/67) · rebond 90% (3/4)
      · −5.0% : fill 0% (1/67) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 72% si les 15 1res min sont vertes (89 cas) · 22% si rouges (71 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.04% .. +2.35%] · haut q95 +3.22% · bas q05 -3.85%
   - 60min (n=160) : retour [-3.65% .. +3.08%] · haut q95 +3.55% · bas q05 -4.23%
   - session (n=160) : retour [-4.39% .. +3.74%] · haut q95 +5.28% · bas q05 -5.41%


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.32 · part idiosyncratique 0.69
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 48.4  _(neutre)_
- **ADX** : 17.9  _(pas de tendance nette)_
- **MACD** : hist 2.811  _(pas de croisement recent)_
- **BB** : %B 0.54 · largeur 23.0%
- **ATR** : 9.33 (3.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.184  _(distribution)_
- **Vol ratio** : 0.77  _(volume normal)_
- **Choppiness** : 42.8  _(transition)_
- **MA** : MA20 267.59 · MA50 283.8 · MA200 318.09  _(prix > MA20)_
- **Dist MA** : MA20 +1.0% · MA50 -4.8% · MA200 -15.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (43072 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
