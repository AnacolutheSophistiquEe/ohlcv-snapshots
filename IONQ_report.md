# IONQ

**Generated** : 2026-06-24T21:51:56.999486+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $53.60  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $53.60 (+5.0% vs entrée) · entrée $51.03 · stop $49.10 · T1 $54.90 · R/R 2.01  
> ↳ P(T1 av. stop) 31 % _(réel 5 s)_ · EV/risk -0.07 _(réel 5 s)_ (GBM 0.037) · ¼-Kelly 0.002 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $50.26–$51.81 (mid $51.03)
- Spot actuel : $53.60 (+5.0% au-dessus de la zone — repli à attendre)
- Stop : $49.10 (stop swing_plan-based (-8.4%))
- Targets : T1 $54.90 · R/R 2.01 | T2 $58.77 · R/R 4.01 | T3 $62.64 · R/R 6.02
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $49.10


## Edge, scénarios & sizing

- EV/risk : 0.037 | EV/share : $0.071 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 18 % | T3 8 %
- Kelly (position) : f* 0.007 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, swing) : bull 12.1 | bear 16.0 | side 72.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 107.0 (= 2 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.178% → cible +3.389% / stop −3.366%, p_fill 64%, n_eff≈26.6) : P(cible|rempli) **56%** · **EV/risk +0.140** (×p_fill ; si rempli +0.74% du capital)
  - **swing** (entrée dip −4.792% → cible +7.578% / stop −3.789%, p_fill 56%, n_eff≈20.6) : P(cible|rempli) **31%** · **EV/risk -0.070** (×p_fill ; si rempli -0.48% du capital)
  - **deep** (entrée dip −7.398% → cible +10.717% / stop −5.359%, p_fill 48%, n_eff≈17.2) : P(cible|rempli) **23%** · **EV/risk -0.179** (×p_fill ; si rempli -1.99% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→85% · +2.0%→69% · +3.0%→57% · +5.0%→31% · +8.0%→18%
- Range intraday médian 7.58% (p90 12.54%) · excursion haute méd. +3.58% / basse méd. −2.78%
- Profil de vol intra : ouverture 4.678% vs midi 1.613% vs clôture 1.674% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 16% · trend ↑0%/↓1% ; spike-down 74% · recovery-V 45%)_
- **Régime intraday** : **chop** _(efficiency 0.115 ; neutre — autocorr 0.029)_ ; drift intra méd. 0.734% ; recovery-V 49%
- **σ réalisé intraday** 5.481% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 63% / bas 46% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 57.7256 (VA 57.0594–58.9249 ; dernier close 57.84)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 60% · rebond 78% · **stop −5.85%** sous le fill (sous le bruit) · cible +3.61% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. -0.31% · baisse 52% (gap-down >1% 39% · >2% 20%)
- Excursion ouverture 5min (n=160) : bas méd −1.31% (p90 −2.98%) · haut méd +1.0% · range méd 2.57%
- Excursion ouverture 15min (n=160) : bas méd −1.83% (p90 −3.9%) · haut méd +1.34% · range méd 3.59%
- Excursion ouverture 30min (n=160) : bas méd −1.95% (p90 −5.16%) · haut méd +1.78% · range méd 4.24%
- Excursion ouverture 60min (n=160) : bas méd −2.43% (p90 −5.67%) · haut méd +2.21% · range méd 5.36%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 57.84 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 76% · séance 82% (133/159) · gap 47% · délai 0.0min · rebond 75% (95/133) (MFE +2.31%)
   - −1.0% : fill 30min 72% · séance 80% (126/159) · gap 39% · délai 0.0min · rebond 80% (94/126) (MFE +2.8%)
   - −1.5% : fill 30min 68% · séance 77% (120/159) · gap 30% · délai 0.0min · rebond 73% (84/120) (MFE +2.6%)
   - −2.0% : fill 30min 58% · séance 71% (113/159) · gap 20% · délai 0.4min · rebond 73% (80/113) (MFE +2.85%)
   - −3.0% : fill 30min 48% · séance 60% (91/159) · gap 12% · délai 5.9min · rebond 78% (69/91) (MFE +3.61%)
   - −4.0% : fill 30min 29% · séance 46% (73/159) · gap 6% · délai 15.7min · rebond 79% (55/73) (MFE +3.43%)
   - −5.0% : fill 30min 18% · séance 40% (65/159) · gap 3% · délai 32.0min · rebond 83% (55/65) (MFE +3.52%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.98% (p90 −2.89%) → stop au-delà de −2.52% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.14% (p90 −3.71%) → stop au-delà de −2.68% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.28% (p90 −3.75%) → stop au-delà de −2.72% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1113 jambes) : jambe baissière méd −1.35% (p90 −3.19%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (71 séances) :
      · −1.0% : fill 100% (71/71) · rebond 78% (53/71)
      · −2.0% : fill 92% (66/71) · rebond 78% (51/66)
      · −3.0% : fill 81% (56/71) · rebond 79% (45/56)
      · −4.0% : fill 62% (44/71) · rebond 79% (35/44)
      · −5.0% : fill 55% (39/71) · rebond 78% (32/39)
   - **flat** (17 séances) :
      · −1.0% : fill 78% (14/17) · rebond 81% (9/14)
      · −2.0% : fill 60% (13/17) · rebond 49% (7/13)
      · −3.0% : fill 45% (10/17) · rebond 52% (6/10)
      · −4.0% : fill 40% (7/17) · rebond 67% (3/7)
      · −5.0% : fill 40% (7/17) · rebond 91% (6/7)
   - **gap-up** (71 séances) :
      · −1.0% : fill 56% (41/71) · rebond 83% (32/41)
      · −2.0% : fill 48% (34/71) · rebond 70% (22/34)
      · −3.0% : fill 37% (25/71) · rebond 83% (18/25)
      · −4.0% : fill 27% (22/71) · rebond 86% (17/22)
      · −5.0% : fill 22% (19/71) · rebond 96% (17/19)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 53% en base · 63% si les 15 1res min sont vertes (78 cas) · 43% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.85% .. +7.2%] · haut q95 +8.39% · bas q05 -5.67%
   - 60min (n=160) : retour [-5.01% .. +7.93%] · haut q95 +11.25% · bas q05 -6.19%
   - session (n=160) : retour [-7.34% .. +9.71%] · haut q95 +12.94% · bas q05 -10.33%


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.32 · part idiosyncratique 0.68
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 33.1  _(momentum baissier)_
- **ADX** : 20.7  _(pas de tendance nette)_
- **MACD** : hist -1.297  _(pas de croisement recent)_
- **BB** : %B 0.18 · largeur 39.7%
- **ATR** : 5.88 (87.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.131  _(distribution)_
- **Vol ratio** : 0.79  _(volume normal)_
- **Choppiness** : 59.6  _(transition)_
- **MA** : MA20 61.46 · MA50 54.09 · MA200 49.51  _(prix < MA20)_
- **Dist MA** : MA20 -12.8% · MA50 -0.9% · MA200 +8.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (44215 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
