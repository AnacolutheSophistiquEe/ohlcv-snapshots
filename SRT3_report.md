# SRT3

**Generated** : 2026-06-26T00:03:16.831050+00:00  
**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €230.70  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €230.70 (+1.3% vs entrée) · entrée €227.82 · stop €224.80 · T1 €230.93 · R/R 1.03  
> ↳ P(T1 av. stop) 35 % _(réel 5 s)_ · EV/risk -0.046 _(réel 5 s)_ (GBM 0.013) · ¼-Kelly 0.002 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €227.20–€228.44 (mid €227.82)
- Spot actuel : €230.70 (+1.3% au-dessus de la zone — repli à attendre)
- Stop : €224.80 (stop swing_plan-based (-4.23%))
- Targets : T1 €230.93 · R/R 1.03 | T2 €234.03 · R/R 2.06 | T3 €237.14 · R/R 3.09
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €224.80


## Edge, scénarios & sizing

- EV/risk : 0.013 | EV/share : €0.038 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 45 % | T2 21 % | T3 8 %
- Kelly (position) : f* 0.008 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 66.9 | bear 15.1 | side 18.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 231.0 (= 1 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.25% → cible +1.363% / stop −1.326%, p_fill 63%, n_eff≈25.2) : P(cible|rempli) **35%** · **EV/risk -0.046** (×p_fill ; si rempli -0.10% du capital)
  - **swing** (entrée dip −2.748% → cible +3.048% / stop −1.524%, p_fill 45%, n_eff≈16.5) : P(cible|rempli) **46%** · **EV/risk +0.140** (×p_fill ; si rempli +0.47% du capital)
  - **deep** (entrée dip −4.236% → cible +4.31% / stop −2.155%, p_fill 38%, n_eff≈15.6) : P(cible|rempli) **41%** · **EV/risk +0.059** (×p_fill ; si rempli +0.34% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→70% · +2.0%→44% · +3.0%→25% · +5.0%→8% · +8.0%→0%
- Range intraday médian 3.72% (p90 6.57%) · excursion haute méd. +1.8% / basse méd. −1.97%
- Profil de vol intra : ouverture 2.042% vs midi 0.914% vs clôture 1.029% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 93% · range 6% · trend ↑1%/↓0% ; spike-down 55% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; neutre — autocorr 0.014)_ ; drift intra méd. -0.3% ; recovery-V 19%
- **σ réalisé intraday** 2.492% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 73% / whipsaw 36%
- POC intraday (dernière séance, temps-au-prix) : 214.6525 (VA 213.6375–215.2325 ; dernier close 212.5)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 59% · rebond 65% · **stop −2.64%** sous le fill (sous le bruit) · cible +1.47% · R/R 0.56 (high win-rate)
- Gaps overnight (n=159) : méd. -0.06% · baisse 52% (gap-down >1% 19% · >2% 7%)
- Excursion ouverture 5min (n=160) : bas méd −0.21% (p90 −1.74%) · haut méd +0.59% · range méd 1.16%
- Excursion ouverture 15min (n=160) : bas méd −0.46% (p90 −1.94%) · haut méd +0.68% · range méd 1.51%
- Excursion ouverture 30min (n=160) : bas méd −0.51% (p90 −2.11%) · haut méd +0.84% · range méd 1.75%
- Excursion ouverture 60min (n=160) : bas méd −0.55% (p90 −2.54%) · haut méd +1.03% · range méd 1.93%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 212.5 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 77% (124/159) · gap 30% · délai 0.3min · rebond 49% (57/124) (MFE +1.0%)
   - −1.0% : fill 30min 42% · séance 63% (104/159) · gap 19% · délai 2.0min · rebond 53% (56/104) (MFE +1.15%)
   - −1.5% : fill 30min 32% · séance 59% (91/159) · gap 12% · délai 17.4min · rebond 65% (54/91) (MFE +1.47%)
   - −2.0% : fill 30min 22% · séance 42% (69/159) · gap 7% · délai 19.3min · rebond 60% (44/69) (MFE +1.33%)
   - −3.0% : fill 30min 7% · séance 24% (39/159) · gap 2% · délai 158.2min · rebond 58% (24/39) (MFE +1.66%)
   - −4.0% : fill 30min 4% · séance 14% (20/159) · gap 1% · délai 208.7min · rebond 67% (15/20) (MFE +1.31%)
   - −5.0% : fill 30min 2% · séance 8% (10/159) · gap 1% · délai 99.8min · rebond 74% (8/10) (MFE +2.47%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.04% (p90 −1.79%) → stop au-delà de −1.01% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.03% (p90 −1.97%) → stop au-delà de −0.81% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.05% (p90 −2.06%) → stop au-delà de −1.08% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=406 jambes) : jambe baissière méd −1.04% (p90 −2.5%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 82% (62/75) · rebond 60% (37/62)
      · −2.0% : fill 58% (42/75) · rebond 65% (29/42)
      · −3.0% : fill 42% (28/75) · rebond 62% (17/28)
      · −4.0% : fill 25% (16/75) · rebond 71% (12/16)
      · −5.0% : fill 13% (7/75) · rebond 92% (6/7)
   - **flat** (37 séances) :
      · −1.0% : fill 59% (21/37) · rebond 40% (10/21)
      · −2.0% : fill 43% (14/37) · rebond 45% (7/14)
      · −3.0% : fill 19% (6/37) · rebond 49% (4/6)
      · −4.0% : fill 12% (3/37) · rebond 44% (2/3)
      · −5.0% : fill 12% (3/37) · rebond 44% (2/3)
   - **gap-up** (47 séances) :
      · −1.0% : fill 44% (21/47) · rebond 52% (9/21)
      · −2.0% : fill 22% (13/47) · rebond 71% (8/13)
      · −3.0% : fill 7% (5/47) · rebond 52% (3/5)
      · −4.0% : fill 2% (1/47) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/47) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 59% si les 15 1res min sont vertes (88 cas) · 38% si rouges (72 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.29% .. +2.13%] · haut q95 +2.67% · bas q05 -2.79%
   - 60min (n=160) : retour [-2.72% .. +2.32%] · haut q95 +2.86% · bas q05 -3.2%
   - session (n=160) : retour [-3.8% .. +3.8%] · haut q95 +5.37% · bas q05 -4.69%


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.42 · part idiosyncratique 0.58
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 44.6  _(momentum baissier)_
- **ADX** : 16.5  _(pas de tendance nette)_
- **MACD** : hist -1.576  _(pas de croisement recent)_
- **BB** : %B 0.48 · largeur 19.9%
- **ATR** : 10.07 (91.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.153  _(distribution)_
- **Vol ratio** : 0.78  _(volume normal)_
- **Choppiness** : 52.4  _(transition)_
- **MA** : MA20 231.51 · MA50 226.8 · MA200 228.73  _(prix < MA20)_
- **Dist MA** : MA20 -0.3% · MA50 +1.7% · MA200 +0.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (41766 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
