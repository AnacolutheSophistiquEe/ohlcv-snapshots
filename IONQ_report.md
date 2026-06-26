# IONQ

**Generated** : 2026-06-26T00:16:10.810382+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite high · $50.56  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)  
> ↳ spot $50.56 (+1.8% vs entrée) · entrée $49.66 · stop $47.77 · T1 $53.45 · R/R 2.01  
> ↳ P(T1 av. stop) 38 % _(réel 5 s)_ · EV/risk 0.079 _(réel 5 s)_ (GBM 0.037) · ¼-Kelly 0.002 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $48.91–$50.42 (mid $49.66)
- Spot actuel : $50.56 (+1.8% au-dessus de la zone — repli à attendre)
- Stop : $47.77 (stop swing_plan-based (-5.51%))
- Targets : T1 $53.45 · R/R 2.01 | T2 $57.23 · R/R 4.01 | T3 $61.02 · R/R 6.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $47.77


## Edge, scénarios & sizing

- EV/risk : 0.037 | EV/share : $0.070 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 18 % | T3 8 %
- Kelly (position) : f* 0.006 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, swing) : bull 12.0 | bear 15.7 | side 72.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 152.0 (= 3 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.805% → cible +3.408% / stop −3.503%, p_fill 89%, n_eff≈35.0) : P(cible|rempli) **53%** · **EV/risk +0.054** (×p_fill ; si rempli +0.21% du capital)
  - **swing** (entrée dip −1.767% → cible +7.62% / stop −3.81%, p_fill 86%, n_eff≈33.0) : P(cible|rempli) **38%** · **EV/risk +0.079** (×p_fill ; si rempli +0.35% du capital)
  - **deep** (entrée dip −2.739% → cible +10.777% / stop −5.388%, p_fill 79%, n_eff≈29.6) : P(cible|rempli) **36%** · **EV/risk -0.018** (×p_fill ; si rempli -0.12% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→84% · +2.0%→69% · +3.0%→57% · +5.0%→31% · +8.0%→18%
- Range intraday médian 7.61% (p90 12.54%) · excursion haute méd. +3.58% / basse méd. −2.78%
- Profil de vol intra : ouverture 4.708% vs midi 1.622% vs clôture 1.666% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓1% ; spike-down 74% · recovery-V 44%)_
- **Régime intraday** : **chop** _(efficiency 0.116 ; momentum — autocorr 0.031)_ ; drift intra méd. 0.401% ; recovery-V 47%
- **σ réalisé intraday** 5.491% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 48% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 53.9333 (VA 53.1737–54.9098 ; dernier close 53.61)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 41% · rebond 84% · **stop −4.76%** sous le fill (sous le bruit) · cible +3.44% · R/R 0.72 (high win-rate)
- Gaps overnight (n=159) : méd. -0.34% · baisse 53% (gap-down >1% 38% · >2% 20%)
- Excursion ouverture 5min (n=160) : bas méd −1.32% (p90 −3.16%) · haut méd +0.99% · range méd 2.59%
- Excursion ouverture 15min (n=160) : bas méd −1.85% (p90 −4.03%) · haut méd +1.33% · range méd 3.61%
- Excursion ouverture 30min (n=160) : bas méd −2.05% (p90 −5.18%) · haut méd +1.76% · range méd 4.31%
- Excursion ouverture 60min (n=160) : bas méd −2.51% (p90 −5.85%) · haut méd +2.12% · range méd 5.42%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 53.61 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 76% · séance 83% (133/159) · gap 48% · délai 0.0min · rebond 74% (95/133) (MFE +2.26%)
   - −1.0% : fill 30min 73% · séance 80% (126/159) · gap 38% · délai 0.0min · rebond 78% (94/126) (MFE +2.73%)
   - −1.5% : fill 30min 68% · séance 77% (120/159) · gap 30% · délai 0.0min · rebond 71% (84/120) (MFE +2.54%)
   - −2.0% : fill 30min 58% · séance 72% (113/159) · gap 20% · délai 0.3min · rebond 74% (81/113) (MFE +2.71%)
   - −3.0% : fill 30min 49% · séance 60% (91/159) · gap 12% · délai 5.3min · rebond 75% (68/91) (MFE +3.44%)
   - −4.0% : fill 30min 30% · séance 47% (73/159) · gap 6% · délai 15.0min · rebond 80% (56/73) (MFE +2.94%)
   - −5.0% : fill 30min 20% · séance 41% (65/159) · gap 3% · délai 31.2min · rebond 84% (56/65) (MFE +3.44%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.98% (p90 −2.9%) → stop au-delà de −2.53% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.14% (p90 −3.71%) → stop au-delà de −2.68% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.28% (p90 −3.75%) → stop au-delà de −2.72% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1114 jambes) : jambe baissière méd −1.36% (p90 −3.33%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (71 séances) :
      · −1.0% : fill 100% (71/71) · rebond 75% (53/71)
      · −2.0% : fill 92% (66/71) · rebond 79% (52/66)
      · −3.0% : fill 82% (56/71) · rebond 75% (44/56)
      · −4.0% : fill 63% (44/71) · rebond 80% (36/44)
      · −5.0% : fill 56% (39/71) · rebond 80% (33/39)
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
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 63% si les 15 1res min sont vertes (78 cas) · 42% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.85% .. +7.18%] · haut q95 +8.36% · bas q05 -5.83%
   - 60min (n=160) : retour [-5.36% .. +7.8%] · haut q95 +11.23% · bas q05 -6.47%
   - session (n=160) : retour [-7.25% .. +9.71%] · haut q95 +12.93% · bas q05 -10.29%


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.31 · part idiosyncratique 0.69
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 32.8  _(momentum baissier)_
- **ADX** : 20.4  _(pas de tendance nette)_
- **MACD** : hist -1.509  _(pas de croisement recent)_
- **BB** : %B 0.11 · largeur 42.7%
- **ATR** : 5.86 (87.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.202  _(distribution)_
- **Vol ratio** : 0.8  _(volume normal)_
- **Choppiness** : 65.0  _(marche en range (choppy))_
- **MA** : MA20 60.72 · MA50 54.39 · MA200 49.56  _(prix < MA20)_
- **Dist MA** : MA20 -16.7% · MA50 -7.0% · MA200 +2.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (43240 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
