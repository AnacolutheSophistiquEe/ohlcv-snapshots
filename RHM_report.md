# RHM

**Generated** : 2026-06-24T00:02:02.773008+00:00  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · €1169.80  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot €1169.80 (+0.8% vs entrée) · entrée €1160.05 · stop €1144.71 · T1 €1175.47 · R/R 1.01  
> ↳ P(T1 av. stop) 51 % _(réel 5 s)_ · EV/risk 0.149 _(réel 5 s)_ (GBM -0.047) · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.060 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €1156.97–€1163.13 (mid €1160.05)
- Spot actuel : €1169.80 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : €1144.71 (stop swing_plan-based (-3.29%))
- Targets : T1 €1175.47 · R/R 1.01 | T2 €1190.90 · R/R 2.01 | T3 €1206.32 · R/R 3.02
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €1144.71


## Edge, scénarios & sizing

- EV/risk : -0.047 | EV/share : €-0.719 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 22 % | T3 9 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 51.9 | bear 10.2 | side 37.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.838% → cible +1.33% / stop −1.323%, p_fill 81%, n_eff≈33.8) : P(cible|rempli) **51%** · **EV/risk +0.149** (×p_fill ; si rempli +0.24% du capital)
  - **swing** (entrée dip −1.831% → cible +2.973% / stop −1.486%, p_fill 56%, n_eff≈22.2) : P(cible|rempli) **38%** · **EV/risk +0.017** (×p_fill ; si rempli +0.04% du capital)
  - **deep** (entrée dip −2.838% → cible +4.204% / stop −2.102%, p_fill 41%, n_eff≈20.7) : P(cible|rempli) **12%** · **EV/risk -0.278** (×p_fill ; si rempli -1.44% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→62% · +2.0%→49% · +3.0%→30% · +5.0%→2% · +8.0%→0%
- Range intraday médian 4.15% (p90 6.64%) · excursion haute méd. +1.85% / basse méd. −1.66%
- Profil de vol intra : ouverture 2.386% vs midi 0.898% vs clôture 1.012% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 52% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.097 ; neutre — autocorr 0.027)_ ; drift intra méd. -0.258% ; recovery-V 29%
- **σ réalisé intraday** 2.589% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 61% / bas 64% / whipsaw 25%
- POC intraday (dernière séance, temps-au-prix) : 1175.8325 (VA 1147.2975–1193.3925 ; dernier close 1181.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 46% · rebond 66% · **stop −3.15%** sous le fill (sous le bruit) · cible +1.41% · R/R 0.45 (high win-rate)
- Gaps overnight (n=159) : méd. 0.08% · baisse 41% (gap-down >1% 15% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.68% (p90 −1.7%) · haut méd +0.57% · range méd 1.45%
- Excursion ouverture 15min (n=160) : bas méd −0.91% (p90 −1.95%) · haut méd +0.75% · range méd 1.79%
- Excursion ouverture 30min (n=160) : bas méd −0.98% (p90 −2.21%) · haut méd +0.89% · range méd 2.01%
- Excursion ouverture 60min (n=160) : bas méd −1.0% (p90 −2.42%) · haut méd +1.0% · range méd 2.25%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1181.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 76% (118/159) · gap 26% · délai 0.3min · rebond 56% (61/118) (MFE +1.13%)
   - −1.0% : fill 30min 45% · séance 71% (104/159) · gap 15% · délai 5.5min · rebond 58% (57/104) (MFE +1.39%)
   - −1.5% : fill 30min 27% · séance 54% (77/159) · gap 8% · délai 20.1min · rebond 57% (40/77) (MFE +1.24%)
   - −2.0% : fill 30min 22% · séance 46% (68/159) · gap 6% · délai 33.6min · rebond 66% (39/68) (MFE +1.41%)
   - −3.0% : fill 30min 9% · séance 28% (45/159) · gap 2% · délai 122.6min · rebond 67% (30/45) (MFE +1.46%)
   - −4.0% : fill 30min 3% · séance 18% (27/159) · gap 1% · délai 319.7min · rebond 52% (16/27) (MFE +1.08%)
   - −5.0% : fill 30min 1% · séance 10% (17/159) · gap 0% · délai 239.3min · rebond 40% (10/17) (MFE +0.69%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.54% (p90 −1.47%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.43% (p90 −1.6%) → stop au-delà de −1.31% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.27% (p90 −1.62%) → stop au-delà de −1.32% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=441 jambes) : jambe baissière méd −1.11% (p90 −2.52%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (48 séances) :
      · −1.0% : fill 97% (47/48) · rebond 58% (23/47)
      · −2.0% : fill 76% (36/48) · rebond 73% (23/36)
      · −3.0% : fill 43% (26/48) · rebond 70% (19/26)
      · −4.0% : fill 28% (15/48) · rebond 56% (10/15)
      · −5.0% : fill 16% (10/48) · rebond 59% (8/10)
   - **flat** (51 séances) :
      · −1.0% : fill 75% (35/51) · rebond 70% (23/35)
      · −2.0% : fill 34% (17/51) · rebond 65% (9/17)
      · −3.0% : fill 20% (10/51) · rebond 42% (5/10)
      · −4.0% : fill 18% (8/51) · rebond 16% (2/8)
      · −5.0% : fill 15% (6/51) · rebond 22% (1/6)
   - **gap-up** (60 séances) :
      · −1.0% : fill 46% (22/60) · rebond 43% (11/22)
      · −2.0% : fill 33% (15/60) · rebond 53% (7/15)
      · −3.0% : fill 24% (9/60) · rebond 82% (6/9)
      · −4.0% : fill 10% (4/60) · rebond 100% (4/4)
      · −5.0% : fill 0% (1/60) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 61% si les 15 1res min sont vertes (86 cas) · 32% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.28% .. +2.84%] · haut q95 +3.93% · bas q05 -2.84%
   - 60min (n=160) : retour [-2.62% .. +2.8%] · haut q95 +4.02% · bas q05 -3.26%
   - session (n=160) : retour [-5.92% .. +3.43%] · haut q95 +4.74% · bas q05 -6.8%


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.33 · part idiosyncratique 0.67
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 43.7  _(momentum baissier)_
- **ADX** : 22.9  _(pas de tendance nette)_
- **MACD** : hist 3.846  _(pas de croisement recent)_
- **BB** : %B 0.28 · largeur 12.2%
- **ATR** : 51.14 (22.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.059  _(distribution)_
- **Vol ratio** : 0.47  _(volume atone)_
- **Choppiness** : 72.1  _(marche en range (choppy))_
- **MA** : MA20 1202.19 · MA50 1265.82 · MA200 1578.73  _(prix < MA20)_
- **Dist MA** : MA20 -2.7% · MA50 -7.6% · MA200 -25.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (42124 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
