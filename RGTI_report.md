# RGTI

**Generated** : 2026-06-25T21:54:17.284057+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · $18.41  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US Core PCE Price Index (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot $18.41 (+14.3% vs entrée) · entrée $16.10 · stop $15.40 · T1 $16.71 · R/R 0.87  
> ↳ P(T1 av. stop) 40 % · EV/risk -0.021 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $15.97–$16.22 (mid $16.10)
- Spot actuel : $18.41 (+14.3% au-dessus de la zone — repli à attendre)
- Stop : $15.40 (stop swing_plan-based (-28.9%))
- Targets : T1 $16.71 · R/R 0.87 | T2 $17.33 · R/R 1.76 | T3 $17.94 · R/R 2.63
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $15.40


## Edge, scénarios & sizing

- EV/risk : -0.021 | EV/share : $-0.015 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 40 % | T2 15 % | T3 4 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 14.9 | bear 77.9 | side 7.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→81% · +2.0%→66% · +3.0%→51% · +5.0%→36% · +8.0%→16%
- Range intraday médian 8.05% (p90 13.36%) · excursion haute méd. +3.19% / basse méd. −3.11%
- Profil de vol intra : ouverture 4.992% vs midi 1.713% vs clôture 1.996% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 19% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 47%)_
- **Régime intraday** : **chop** _(efficiency 0.129 ; momentum — autocorr 0.054)_ ; drift intra méd. 0.577% ; recovery-V 51%
- **σ réalisé intraday** 5.907% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 43% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 19.2687 (VA 19.1764–19.9144 ; dernier close 19.535)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 45% · rebond 74% · **stop −6.01%** sous le fill (sous le bruit) · cible +2.97% · R/R 0.49 (high win-rate)
- Gaps overnight (n=159) : méd. -0.72% · baisse 59% (gap-down >1% 47% · >2% 29%)
- Excursion ouverture 5min (n=160) : bas méd −1.51% (p90 −2.97%) · haut méd +1.01% · range méd 2.71%
- Excursion ouverture 15min (n=160) : bas méd −1.66% (p90 −4.57%) · haut méd +1.53% · range méd 3.55%
- Excursion ouverture 30min (n=160) : bas méd −1.84% (p90 −6.02%) · haut méd +1.77% · range méd 4.63%
- Excursion ouverture 60min (n=160) : bas méd −2.36% (p90 −6.42%) · haut méd +2.16% · range méd 5.7%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 19.535 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 80% · séance 86% (137/159) · gap 54% · délai 0.0min · rebond 68% (92/137) (MFE +2.42%)
   - −1.0% : fill 30min 72% · séance 82% (133/159) · gap 47% · délai 0.0min · rebond 65% (88/133) (MFE +2.07%)
   - −1.5% : fill 30min 66% · séance 78% (124/159) · gap 40% · délai 0.0min · rebond 66% (83/124) (MFE +2.54%)
   - −2.0% : fill 30min 60% · séance 71% (113/159) · gap 29% · délai 0.0min · rebond 65% (75/113) (MFE +2.73%)
   - −3.0% : fill 30min 54% · séance 64% (98/159) · gap 15% · délai 1.1min · rebond 76% (72/98) (MFE +2.78%)
   - −4.0% : fill 30min 41% · séance 52% (80/159) · gap 6% · délai 3.3min · rebond 75% (60/80) (MFE +2.57%)
   - −5.0% : fill 30min 28% · séance 45% (67/159) · gap 2% · délai 12.5min · rebond 74% (52/67) (MFE +2.97%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −1.12% (p90 −4.06%) → stop au-delà de −2.08% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.52% (p90 −4.5%) → stop au-delà de −2.73% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.53% (p90 −4.59%) → stop au-delà de −2.92% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1200 jambes) : jambe baissière méd −1.31% (p90 −3.36%) · ~15.6 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (83 séances) :
      · −1.0% : fill 98% (82/83) · rebond 62% (50/82)
      · −2.0% : fill 91% (77/83) · rebond 65% (52/77)
      · −3.0% : fill 86% (70/83) · rebond 75% (52/70)
      · −4.0% : fill 74% (59/83) · rebond 77% (45/59)
      · −5.0% : fill 64% (51/83) · rebond 74% (42/51)
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
- **P(clôture VERTE) selon le drive 15min** (n=160) : 53% en base · 66% si les 15 1res min sont vertes (78 cas) · 42% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.37% .. +7.24%] · haut q95 +8.89% · bas q05 -6.71%
   - 60min (n=160) : retour [-6.17% .. +8.04%] · haut q95 +10.1% · bas q05 -7.34%
   - session (n=160) : retour [-8.24% .. +9.99%] · haut q95 +11.91% · bas q05 -10.54%


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.47 · part idiosyncratique 0.53
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US Core PCE Price Index (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 32.8  _(momentum baissier)_
- **ADX** : 17.0  _(pas de tendance nette)_
- **MACD** : hist -0.471  _(pas de croisement recent)_
- **BB** : %B 0.14 · largeur 46.6%
- **ATR** : 2.31 (67.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.078  _(distribution)_
- **Vol ratio** : 0.58  _(volume atone)_
- **Choppiness** : 68.7  _(marche en range (choppy))_
- **MA** : MA20 22.1 · MA50 20.21 · MA200 23.85  _(prix < MA20)_
- **Dist MA** : MA20 -16.7% · MA50 -8.9% · MA200 -22.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (40372 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
