# RGTI

**Generated** : 2026-06-26T21:53:05.832872+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $18.36  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $18.36 (+3.2% vs entrée) · entrée $17.79 · stop $17.16 · T1 $18.43 · R/R 1.02  
> ↳ P(T1 av. stop) 27 % _(réel 5 s)_ · EV/risk -0.169 _(réel 5 s)_ (GBM -0.01) · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $17.67–$17.92 (mid $17.79)
- Spot actuel : $18.36 (+3.2% au-dessus de la zone — repli à attendre)
- Stop : $17.16 (stop swing_plan-based (-10.5%))
- Targets : T1 $18.43 · R/R 1.02 | T2 $19.06 · R/R 2.02 | T3 $19.70 · R/R 3.03
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $17.16


## Edge, scénarios & sizing

- EV/risk : -0.01 | EV/share : $-0.006 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 17 % | T3 6 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 13.0 | bear 77.1 | side 9.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.079% → cible +3.561% / stop −3.561%, p_fill 52%, n_eff≈20.2) : P(cible|rempli) **27%** · **EV/risk -0.169** (×p_fill ; si rempli -1.16% du capital)
  - **swing** (entrée dip −6.788% → cible +7.963% / stop −3.982%, p_fill 39%, n_eff≈15.8) : P(cible|rempli) **31%** · **EV/risk -0.021** (×p_fill ; si rempli -0.21% du capital)
  - **deep** (entrée dip −10.489% → cible +11.263% / stop −5.631%, p_fill 37%, n_eff≈13.6) : P(cible|rempli) **39%** · **EV/risk +0.026** (×p_fill ; si rempli +0.40% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→82% · +2.0%→68% · +3.0%→51% · +5.0%→36% · +8.0%→16%
- Range intraday médian 8.12% (p90 13.36%) · excursion haute méd. +3.19% / basse méd. −3.11%
- Profil de vol intra : ouverture 5.057% vs midi 1.71% vs clôture 1.987% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 20% · trend ↑0%/↓0% ; spike-down 79% · recovery-V 46%)_
- **Régime intraday** : **chop** _(efficiency 0.136 ; momentum — autocorr 0.06)_ ; drift intra méd. 0.183% ; recovery-V 49%
- **σ réalisé intraday** 5.913% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 46% / whipsaw 13%
- POC intraday (dernière séance, temps-au-prix) : 18.7306 (VA 18.6776–19.2076 ; dernier close 18.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 53% · rebond 76% · **stop −6.72%** sous le fill (sous le bruit) · cible +2.8% · R/R 0.42 (high win-rate)
- Gaps overnight (n=159) : méd. -0.64% · baisse 58% (gap-down >1% 46% · >2% 28%)
- Excursion ouverture 5min (n=160) : bas méd −1.48% (p90 −2.97%) · haut méd +1.01% · range méd 2.71%
- Excursion ouverture 15min (n=160) : bas méd −1.68% (p90 −4.57%) · haut méd +1.54% · range méd 3.61%
- Excursion ouverture 30min (n=160) : bas méd −1.85% (p90 −6.36%) · haut méd +1.78% · range méd 4.67%
- Excursion ouverture 60min (n=160) : bas méd −2.39% (p90 −6.58%) · haut méd +2.14% · range méd 5.72%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 18.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 80% · séance 86% (137/159) · gap 53% · délai 0.0min · rebond 67% (91/137) (MFE +2.33%)
   - −1.0% : fill 30min 72% · séance 83% (133/159) · gap 46% · délai 0.0min · rebond 66% (88/133) (MFE +2.05%)
   - −1.5% : fill 30min 67% · séance 79% (124/159) · gap 39% · délai 0.0min · rebond 66% (83/124) (MFE +2.42%)
   - −2.0% : fill 30min 61% · séance 72% (113/159) · gap 28% · délai 0.0min · rebond 66% (75/113) (MFE +2.51%)
   - −3.0% : fill 30min 55% · séance 65% (98/159) · gap 15% · délai 1.2min · rebond 76% (72/98) (MFE +2.75%)
   - −4.0% : fill 30min 42% · séance 53% (80/159) · gap 6% · délai 3.8min · rebond 76% (60/80) (MFE +2.8%)
   - −5.0% : fill 30min 28% · séance 46% (67/159) · gap 2% · délai 15.1min · rebond 71% (51/67) (MFE +2.54%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −1.07% (p90 −3.96%) → stop au-delà de −2.08% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.51% (p90 −4.4%) → stop au-delà de −2.72% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.53% (p90 −4.59%) → stop au-delà de −2.92% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1198 jambes) : jambe baissière méd −1.31% (p90 −3.37%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (82 séances) :
      · −1.0% : fill 98% (81/82) · rebond 62% (49/81)
      · −2.0% : fill 91% (76/82) · rebond 65% (51/76)
      · −3.0% : fill 86% (69/82) · rebond 75% (51/69)
      · −4.0% : fill 74% (58/82) · rebond 77% (44/58)
      · −5.0% : fill 64% (50/82) · rebond 74% (41/50)
   - **flat** (14 séances) :
      · −1.0% : fill 86% (12/14) · rebond 84% (10/12)
      · −2.0% : fill 53% (9/14) · rebond 89% (7/9)
      · −3.0% : fill 30% (4/14) · rebond 55% (2/4)
      · −4.0% : fill 30% (4/14) · rebond 55% (2/4)
      · −5.0% : fill 30% (4/14) · rebond 77% (2/4)
   - **gap-up** (63 séances) :
      · −1.0% : fill 59% (40/63) · rebond 71% (29/40)
      · −2.0% : fill 46% (28/63) · rebond 62% (17/28)
      · −3.0% : fill 40% (25/63) · rebond 83% (19/25)
      · −4.0% : fill 27% (18/63) · rebond 78% (14/18)
      · −5.0% : fill 21% (13/63) · rebond 54% (8/13)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 66% si les 15 1res min sont vertes (78 cas) · 40% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:32** → P(séance verte=clôture>ouverture) 90% si début vert vs 12% si rouge (base 52% · écart 78 pts) ; prédictivité sature ensuite (plafond brut 93min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **90%** · continue >prix actuel 58% ; creux résiduel méd -2.23% (q20 -3.47%) → **SL/trailing à −3.47%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.98% / q75 +4.51% → **scale +2.98% / runner +4.51%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **12%** (continue à baisser 54%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.12%** (au-delà de la MAE q10 -6.12%), cible rebond +1.53% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-6.41% .. +7.04%] · haut q95 +8.81% · bas q05 -7.17%
   - 60min (n=160) : retour [-6.16% .. +7.94%] · haut q95 +10.05% · bas q05 -7.34%
   - 2h (n=160) : retour [-7.78% .. +9.5%] · haut q95 +10.36% · bas q05 -8.48%
   - 4h (n=160) : retour [-9.13% .. +9.85%] · haut q95 +10.51% · bas q05 -10.52%
   - 6h (n=160) : retour [-8.89% .. +8.64%] · haut q95 +11.61% · bas q05 -10.52%
   - session (n=160) : retour [-8.13% .. +9.99%] · haut q95 +11.78% · bas q05 -10.52%


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.46 · part idiosyncratique 0.54
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 41.3  _(momentum baissier)_
- **ADX** : 17.0  _(pas de tendance nette)_
- **MACD** : hist -0.514  _(pas de croisement recent)_
- **BB** : %B 0.16 · largeur 44.8%
- **ATR** : 2.11 (63.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.146  _(distribution)_
- **Vol ratio** : 0.7  _(volume normal)_
- **Choppiness** : 61.4  _(transition)_
- **MA** : MA20 21.67 · MA50 20.2 · MA200 23.86  _(prix < MA20)_
- **Dist MA** : MA20 -15.3% · MA50 -9.1% · MA200 -23.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (68159 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
