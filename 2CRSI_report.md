# AL2SI

**Generated** : 2026-06-24T21:42:59.033943+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 14.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite extreme · €26.60  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot €26.60 (+14.7% vs entrée) · entrée €23.20 · stop €21.34 · T1 €25.10 · R/R 1.02  
> ↳ P(T1 av. stop) 23 % · EV/risk -0.013 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €22.91–€23.49 (mid €23.20)
- Spot actuel : €26.60 (+14.7% au-dessus de la zone — repli à attendre)
- Stop : €21.34 (stop swing_plan-based (-35.56%))
- Targets : T1 €25.10 · R/R 1.02 | T2 €27.00 · R/R 2.04 | T3 €28.90 · R/R 3.06
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €21.34


## Edge, scénarios & sizing

- EV/risk : -0.013 | EV/share : €-0.025 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 23 % | T2 3 % | T3 0 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 10.2 | bear 62.0 | side 27.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 160.0 (= 6 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→80% · +2.0%→76% · +3.0%→65% · +5.0%→41% · +8.0%→21%
- Range intraday médian 7.78% (p90 13.94%) · excursion haute méd. +4.16% / basse méd. −3.18%
- Profil de vol intra : ouverture 5.337% vs midi 1.622% vs clôture 1.928% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (133 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 11% · trend ↑0%/↓2% ; spike-down 70% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.173 ; neutre — autocorr -0.019)_ ; drift intra méd. 1.036% ; recovery-V 34%
- **σ réalisé intraday** 7.901% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 62% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 28.926 (VA 26.346–28.926 ; dernier close 27.7)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 37% · rebond 86% · **stop −5.48%** sous le fill (sous le bruit) · cible +2.53% · R/R 0.46 (high win-rate)
- Gaps overnight (n=132) : méd. 0.14% · baisse 43% (gap-down >1% 26% · >2% 10%)
- Excursion ouverture 5min (n=133) : bas méd −0.86% (p90 −4.33%) · haut méd +0.97% · range méd 2.59%
- Excursion ouverture 15min (n=133) : bas méd −1.31% (p90 −4.99%) · haut méd +1.44% · range méd 3.23%
- Excursion ouverture 30min (n=133) : bas méd −1.36% (p90 −5.49%) · haut méd +1.6% · range méd 3.98%
- Excursion ouverture 60min (n=133) : bas méd −1.83% (p90 −6.5%) · haut méd +2.35% · range méd 5.11%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 27.7 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 76% (100/132) · gap 32% · délai 0.1min · rebond 64% (65/100) (MFE +2.65%)
   - −1.0% : fill 30min 60% · séance 73% (95/132) · gap 26% · délai 0.3min · rebond 66% (64/95) (MFE +2.49%)
   - −1.5% : fill 30min 51% · séance 68% (86/132) · gap 15% · délai 1.3min · rebond 66% (55/86) (MFE +1.75%)
   - −2.0% : fill 30min 42% · séance 57% (73/132) · gap 10% · délai 2.8min · rebond 66% (48/73) (MFE +1.64%)
   - −3.0% : fill 30min 29% · séance 51% (60/132) · gap 7% · délai 10.9min · rebond 80% (49/60) (MFE +2.22%)
   - −4.0% : fill 30min 22% · séance 42% (50/132) · gap 7% · délai 20.5min · rebond 76% (39/50) (MFE +2.67%)
   - −5.0% : fill 30min 19% · séance 37% (43/132) · gap 6% · délai 27.7min · rebond 86% (40/43) (MFE +2.53%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.32% (p90 −4.83%) → stop au-delà de −2.3% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.56% (p90 −4.78%) → stop au-delà de −2.89% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.47% (p90 −4.67%) → stop au-delà de −2.89% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1237 jambes) : jambe baissière méd −1.19% (p90 −2.99%) · ~19.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 97% (45/49) · rebond 66% (30/45)
      · −2.0% : fill 84% (38/49) · rebond 52% (23/38)
      · −3.0% : fill 81% (34/49) · rebond 74% (27/34)
      · −4.0% : fill 67% (29/49) · rebond 68% (23/29)
      · −5.0% : fill 63% (27/49) · rebond 77% (24/27)
   - **flat** (27 séances) :
      · −1.0% : fill 76% (20/27) · rebond 71% (15/20)
      · −2.0% : fill 53% (14/27) · rebond 79% (10/14)
      · −3.0% : fill 35% (9/27) · rebond 87% (8/9)
      · −4.0% : fill 35% (9/27) · rebond 91% (8/9)
      · −5.0% : fill 25% (7/27) · rebond 100% (7/7)
   - **gap-up** (56 séances) :
      · −1.0% : fill 50% (30/56) · rebond 62% (19/30)
      · −2.0% : fill 36% (21/56) · rebond 83% (15/21)
      · −3.0% : fill 31% (17/56) · rebond 92% (14/17)
      · −4.0% : fill 22% (12/56) · rebond 85% (8/12)
      · −5.0% : fill 21% (9/56) · rebond 100% (9/9)
- **P(clôture VERTE) selon le drive 15min** (n=133) : 53% en base · 70% si les 15 1res min sont vertes (64 cas) · 39% si rouges (69 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=133) : retour [-3.9% .. +7.01%] · haut q95 +8.78% · bas q05 -6.88%
   - 60min (n=133) : retour [-5.84% .. +9.5%] · haut q95 +9.98% · bas q05 -7.82%
   - session (n=133) : retour [-7.71% .. +18.88%] · haut q95 +19.52% · bas q05 -11.16%


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.11 · part idiosyncratique 0.89
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 23.3  _(survente)_
- **ADX** : 30.6  _(tendance etablie)_
- **MACD** : hist -3.352  _(pas de croisement recent)_
- **BB** : %B 0.12 · largeur 107.4%
- **ATR** : 6.58 (100.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.067  _(distribution)_
- **Vol ratio** : 2.01  _(volume au-dessus de la moyenne)_
- **Choppiness** : 31.6  _(marche directionnel)_
- **MA** : MA20 44.8 · MA50 42.0 · MA200 22.2  _(prix < MA20)_
- **Dist MA** : MA20 -40.6% · MA50 -36.7% · MA200 +19.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (42479 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
