# SRT3

**Generated** : 2026-06-24T00:03:20.064504+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €212.40  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot €212.40 (+4.8% vs entrée) · entrée €202.72 · stop €199.82 · T1 €205.06 · R/R 0.81  
> ↳ P(T1 av. stop) 50 % · EV/risk -0.013 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €202.25–€203.19 (mid €202.72)
- Spot actuel : €212.40 (+4.8% au-dessus de la zone — repli à attendre)
- Stop : €199.82 (stop swing_plan-based (-10.48%))
- Targets : T1 €205.06 · R/R 0.81 | T2 €207.40 · R/R 1.61 | T3 €209.74 · R/R 2.42
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €199.82


## Edge, scénarios & sizing

- EV/risk : -0.013 | EV/share : €-0.037 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 50 % | T2 28 % | T3 13 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 61.5 | bear 10.2 | side 28.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=3, n_eff=2))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→69% · +2.0%→42% · +3.0%→25% · +5.0%→8% · +8.0%→0%
- Range intraday médian 3.72% (p90 6.57%) · excursion haute méd. +1.78% / basse méd. −1.98%
- Profil de vol intra : ouverture 2.022% vs midi 0.915% vs clôture 1.029% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 93% · range 6% · trend ↑1%/↓0% ; spike-down 56% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; neutre — autocorr 0.017)_ ; drift intra méd. -0.344% ; recovery-V 19%
- **σ réalisé intraday** 2.482% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 59% / bas 77% / whipsaw 37%
- POC intraday (dernière séance, temps-au-prix) : 213.9062 (VA 213.0362–215.6463 ; dernier close 212.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 60% · rebond 65% · **stop −2.64%** sous le fill (sous le bruit) · cible +1.47% · R/R 0.56 (high win-rate)
- Gaps overnight (n=159) : méd. -0.04% · baisse 51% (gap-down >1% 19% · >2% 7%)
- Excursion ouverture 5min (n=160) : bas méd −0.21% (p90 −1.76%) · haut méd +0.57% · range méd 1.15%
- Excursion ouverture 15min (n=160) : bas méd −0.47% (p90 −1.95%) · haut méd +0.68% · range méd 1.47%
- Excursion ouverture 30min (n=160) : bas méd −0.51% (p90 −2.11%) · haut méd +0.83% · range méd 1.74%
- Excursion ouverture 60min (n=160) : bas méd −0.61% (p90 −2.55%) · haut méd +0.99% · range méd 1.92%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 212.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 55% · séance 76% (123/159) · gap 31% · délai 0.3min · rebond 48% (56/123) (MFE +0.99%)
   - −1.0% : fill 30min 42% · séance 64% (104/159) · gap 19% · délai 2.0min · rebond 53% (56/104) (MFE +1.15%)
   - −1.5% : fill 30min 32% · séance 60% (91/159) · gap 13% · délai 17.4min · rebond 65% (54/91) (MFE +1.47%)
   - −2.0% : fill 30min 22% · séance 43% (69/159) · gap 7% · délai 19.3min · rebond 60% (44/69) (MFE +1.33%)
   - −3.0% : fill 30min 7% · séance 25% (39/159) · gap 2% · délai 158.2min · rebond 58% (24/39) (MFE +1.66%)
   - −4.0% : fill 30min 5% · séance 14% (20/159) · gap 1% · délai 208.7min · rebond 67% (15/20) (MFE +1.31%)
   - −5.0% : fill 30min 2% · séance 8% (10/159) · gap 1% · délai 99.8min · rebond 74% (8/10) (MFE +2.47%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.03% (p90 −1.87%) → stop au-delà de −1.06% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.0% (p90 −1.97%) → stop au-delà de −0.93% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.04% (p90 −2.05%) → stop au-delà de −1.08% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=406 jambes) : jambe baissière méd −1.04% (p90 −2.5%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (74 séances) :
      · −1.0% : fill 86% (62/74) · rebond 60% (37/62)
      · −2.0% : fill 60% (42/74) · rebond 65% (29/42)
      · −3.0% : fill 44% (28/74) · rebond 62% (17/28)
      · −4.0% : fill 26% (16/74) · rebond 71% (12/16)
      · −5.0% : fill 13% (7/74) · rebond 92% (6/7)
   - **flat** (38 séances) :
      · −1.0% : fill 59% (21/38) · rebond 40% (10/21)
      · −2.0% : fill 43% (14/38) · rebond 45% (7/14)
      · −3.0% : fill 19% (6/38) · rebond 49% (4/6)
      · −4.0% : fill 12% (3/38) · rebond 44% (2/3)
      · −5.0% : fill 12% (3/38) · rebond 44% (2/3)
   - **gap-up** (47 séances) :
      · −1.0% : fill 44% (21/47) · rebond 52% (9/21)
      · −2.0% : fill 22% (13/47) · rebond 71% (8/13)
      · −3.0% : fill 7% (5/47) · rebond 52% (3/5)
      · −4.0% : fill 2% (1/47) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/47) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 57% si les 15 1res min sont vertes (88 cas) · 38% si rouges (72 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.29% .. +2.13%] · haut q95 +2.63% · bas q05 -2.79%
   - 60min (n=160) : retour [-2.82% .. +2.33%] · haut q95 +2.86% · bas q05 -3.21%
   - session (n=160) : retour [-3.8% .. +3.9%] · haut q95 +5.43% · bas q05 -4.73%


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.44 · part idiosyncratique 0.56
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 22.2  _(survente)_
- **ADX** : 17.5  _(pas de tendance nette)_
- **MACD** : hist -3.476  _(pas de croisement recent)_
- **BB** : %B 0.05 · largeur 19.4%
- **ATR** : 9.68 (85.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.218  _(distribution)_
- **Vol ratio** : 0.5  _(volume atone)_
- **Choppiness** : 43.4  _(transition)_
- **MA** : MA20 232.75 · MA50 226.98 · MA200 228.41  _(prix < MA20)_
- **Dist MA** : MA20 -8.7% · MA50 -6.4% · MA200 -7.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (39211 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
