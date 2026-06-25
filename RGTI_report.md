# RGTI

**Generated** : 2026-06-25T00:18:14.082182+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $19.53  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)  
> ↳ spot $19.53 (+1.0% vs entrée) · entrée $19.34 · stop $18.52 · T1 $20.97 · R/R 1.99  
> ↳ P(T1 av. stop) 41 % _(réel 5 s)_ · EV/risk 0.169 _(réel 5 s)_ (GBM 0.042) · ¼-Kelly 0.002 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.060 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $19.14–$19.53 (mid $19.34)
- Spot actuel : $19.53 (+1.0% au-dessus de la zone — repli à attendre)
- Stop : $18.52 (stop swing_plan-based (-5.17%))
- Targets : T1 $20.97 · R/R 1.99 | T2 $22.60 · R/R 3.98 | T3 $24.23 · R/R 5.96
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $18.52


## Edge, scénarios & sizing

- EV/risk : 0.042 | EV/share : $0.034 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 18 % | T3 8 %
- Kelly (position) : f* 0.007 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, swing) : bull 29.4 | bear 56.8 | side 13.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 156.0 (= 8 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.523% → cible +3.775% / stop −3.566%, p_fill 96%, n_eff≈39.3) : P(cible|rempli) **48%** · **EV/risk +0.021** (×p_fill ; si rempli +0.08% du capital)
  - **swing** (entrée dip −0.991% → cible +8.442% / stop −4.221%, p_fill 94%, n_eff≈38.3) : P(cible|rempli) **41%** · **EV/risk +0.169** (×p_fill ; si rempli +0.76% du capital)
  - **deep** (entrée dip −1.34% → cible +11.939% / stop −5.97%, p_fill 92%, n_eff≈36.2) : P(cible|rempli) **41%** · **EV/risk +0.139** (×p_fill ; si rempli +0.90% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→82% · +2.0%→68% · +3.0%→52% · +5.0%→38% · +8.0%→16%
- Range intraday médian 8.01% (p90 13.36%) · excursion haute méd. +3.31% / basse méd. −3.0%
- Profil de vol intra : ouverture 4.975% vs midi 1.704% vs clôture 2.008% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 19% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 48%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; momentum — autocorr 0.055)_ ; drift intra méd. 0.907% ; recovery-V 54%
- **σ réalisé intraday** 5.915% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 41% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 21.5317 (VA 20.9322–21.6953 ; dernier close 21.265)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 64% · rebond 78% · **stop −7.4%** sous le fill (sous le bruit) · cible +3.41% · R/R 0.46 (high win-rate)
- Gaps overnight (n=159) : méd. -0.65% · baisse 59% (gap-down >1% 46% · >2% 28%)
- Excursion ouverture 5min (n=160) : bas méd −1.48% (p90 −2.98%) · haut méd +1.01% · range méd 2.71%
- Excursion ouverture 15min (n=160) : bas méd −1.63% (p90 −4.47%) · haut méd +1.54% · range méd 3.52%
- Excursion ouverture 30min (n=160) : bas méd −1.84% (p90 −6.02%) · haut méd +1.78% · range méd 4.58%
- Excursion ouverture 60min (n=160) : bas méd −2.28% (p90 −6.02%) · haut méd +2.18% · range méd 5.67%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 21.265 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 79% · séance 85% (137/159) · gap 53% · délai 0.0min · rebond 70% (92/137) (MFE +2.44%)
   - −1.0% : fill 30min 71% · séance 82% (133/159) · gap 46% · délai 0.0min · rebond 67% (88/133) (MFE +2.22%)
   - −1.5% : fill 30min 66% · séance 78% (124/159) · gap 39% · délai 0.0min · rebond 67% (83/124) (MFE +2.57%)
   - −2.0% : fill 30min 60% · séance 71% (113/159) · gap 28% · délai 0.0min · rebond 66% (75/113) (MFE +2.79%)
   - −3.0% : fill 30min 53% · séance 64% (98/159) · gap 16% · délai 1.2min · rebond 78% (72/98) (MFE +3.41%)
   - −4.0% : fill 30min 40% · séance 51% (80/159) · gap 6% · délai 3.6min · rebond 74% (59/80) (MFE +2.8%)
   - −5.0% : fill 30min 27% · séance 44% (67/159) · gap 2% · délai 14.9min · rebond 77% (52/67) (MFE +3.13%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −1.12% (p90 −4.05%) → stop au-delà de −2.08% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.52% (p90 −4.5%) → stop au-delà de −2.73% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.53% (p90 −4.59%) → stop au-delà de −2.92% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1195 jambes) : jambe baissière méd −1.31% (p90 −3.36%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (83 séances) :
      · −1.0% : fill 98% (82/83) · rebond 64% (50/82)
      · −2.0% : fill 91% (77/83) · rebond 67% (52/77)
      · −3.0% : fill 86% (70/83) · rebond 78% (52/70)
      · −4.0% : fill 73% (59/83) · rebond 76% (44/59)
      · −5.0% : fill 63% (51/83) · rebond 77% (42/51)
   - **flat** (14 séances) :
      · −1.0% : fill 86% (12/14) · rebond 84% (10/12)
      · −2.0% : fill 53% (9/14) · rebond 89% (7/9)
      · −3.0% : fill 30% (4/14) · rebond 55% (2/4)
      · −4.0% : fill 30% (4/14) · rebond 55% (2/4)
      · −5.0% : fill 30% (4/14) · rebond 77% (2/4)
   - **gap-up** (62 séances) :
      · −1.0% : fill 57% (39/62) · rebond 68% (28/39)
      · −2.0% : fill 43% (27/62) · rebond 57% (16/27)
      · −3.0% : fill 37% (24/62) · rebond 80% (18/24)
      · −4.0% : fill 23% (17/62) · rebond 73% (13/17)
      · −5.0% : fill 16% (12/62) · rebond 72% (8/12)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 54% en base · 66% si les 15 1res min sont vertes (78 cas) · 43% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.38% .. +7.43%] · haut q95 +8.97% · bas q05 -6.78%
   - 60min (n=160) : retour [-6.18% .. +8.14%] · haut q95 +10.15% · bas q05 -7.34%
   - session (n=160) : retour [-9.12% .. +9.99%] · haut q95 +12.04% · bas q05 -10.58%


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.48 · part idiosyncratique 0.52
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US Core PCE Price Index (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 35.4  _(momentum baissier)_
- **ADX** : 17.4  _(pas de tendance nette)_
- **MACD** : hist -0.373  _(pas de croisement recent)_
- **BB** : %B 0.21 · largeur 44.2%
- **ATR** : 2.31 (66.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.057  _(distribution)_
- **Vol ratio** : 0.71  _(volume normal)_
- **Choppiness** : 60.5  _(transition)_
- **MA** : MA20 22.41 · MA50 20.18 · MA200 23.83  _(prix < MA20)_
- **Dist MA** : MA20 -12.9% · MA50 -3.2% · MA200 -18.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (46111 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
