# SMCI

**Generated** : 2026-06-24T00:13:51.196001+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 10.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite extreme · $33.32  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $33.32 (+14.1% vs entrée) · entrée $29.19 · stop $27.95 · T1 $30.87 · R/R 1.35  
> ↳ P(T1 av. stop) 15 % · EV/risk 0.023 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $28.85–$29.52 (mid $29.19)
- Spot actuel : $33.32 (+14.1% au-dessus de la zone — repli à attendre)
- Stop : $27.95 (stop swing_plan-based (-29.66%))
- Targets : T1 $30.87 · R/R 1.35 | T2 $32.56 · R/R 2.72 | T3 $34.24 · R/R 4.07
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $27.95


## Edge, scénarios & sizing

- EV/risk : 0.023 | EV/share : $0.029 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 15 % | T2 1 % | T3 0 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 11.9 | bear 11.3 | side 76.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→81% · +2.0%→66% · +3.0%→48% · +5.0%→31% · +8.0%→12%
- Range intraday médian 6.17% (p90 10.16%) · excursion haute méd. +2.92% / basse méd. −2.54%
- Profil de vol intra : ouverture 3.625% vs midi 1.274% vs clôture 1.439% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 22% · trend ↑0%/↓2% ; spike-down 65% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.169 ; neutre — autocorr 0.003)_ ; drift intra méd. 0.727% ; recovery-V 32%
- **σ réalisé intraday** 4.407% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 57% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 35.3487 (VA 34.8113–36.2087 ; dernier close 35.46)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 55% · rebond 66% · **stop −5.91%** sous le fill (sous le bruit) · cible +1.75% · R/R 0.3 (high win-rate)
- Gaps overnight (n=159) : méd. 0.24% · baisse 47% (gap-down >1% 30% · >2% 19%)
- Excursion ouverture 5min (n=160) : bas méd −0.84% (p90 −2.26%) · haut méd +0.88% · range méd 1.92%
- Excursion ouverture 15min (n=160) : bas méd −1.14% (p90 −3.26%) · haut méd +1.18% · range méd 2.65%
- Excursion ouverture 30min (n=160) : bas méd −1.35% (p90 −3.82%) · haut méd +1.34% · range méd 3.31%
- Excursion ouverture 60min (n=160) : bas méd −1.62% (p90 −4.19%) · haut méd +1.75% · range méd 4.19%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 35.46 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 74% (126/159) · gap 42% · délai 0.0min · rebond 59% (72/126) (MFE +1.3%)
   - −1.0% : fill 30min 57% · séance 67% (113/159) · gap 30% · délai 0.0min · rebond 56% (62/113) (MFE +1.34%)
   - −1.5% : fill 30min 46% · séance 61% (98/159) · gap 24% · délai 0.3min · rebond 64% (57/98) (MFE +1.45%)
   - −2.0% : fill 30min 40% · séance 55% (87/159) · gap 19% · délai 1.2min · rebond 66% (52/87) (MFE +1.75%)
   - −3.0% : fill 30min 28% · séance 46% (67/159) · gap 16% · délai 6.8min · rebond 59% (39/67) (MFE +1.94%)
   - −4.0% : fill 30min 21% · séance 37% (49/159) · gap 12% · délai 12.1min · rebond 56% (29/49) (MFE +1.46%)
   - −5.0% : fill 30min 16% · séance 29% (39/159) · gap 7% · délai 15.8min · rebond 57% (24/39) (MFE +1.7%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −2.21%) → stop au-delà de −1.32% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.62% (p90 −3.0%) → stop au-delà de −1.82% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.55% (p90 −2.85%) → stop au-delà de −2.17% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=811 jambes) : jambe baissière méd −1.2% (p90 −2.76%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (68 séances) :
      · −1.0% : fill 97% (67/68) · rebond 56% (38/67)
      · −2.0% : fill 88% (59/68) · rebond 59% (32/59)
      · −3.0% : fill 80% (51/68) · rebond 61% (30/51)
      · −4.0% : fill 66% (40/68) · rebond 61% (24/40)
      · −5.0% : fill 54% (32/68) · rebond 57% (20/32)
   - **flat** (17 séances) :
      · −1.0% : fill 92% (15/17) · rebond 80% (10/15)
      · −2.0% : fill 61% (11/17) · rebond 76% (7/11)
      · −3.0% : fill 15% (3/17) · rebond 89% (2/3)
      · −4.0% : fill 6% (2/17) · rebond 100% (2/2)
      · −5.0% : fill 2% (1/17) · rebond 0% (0/1)
   - **gap-up** (74 séances) :
      · −1.0% : fill 34% (31/74) · rebond 47% (14/31)
      · −2.0% : fill 21% (17/74) · rebond 92% (13/17)
      · −3.0% : fill 18% (13/74) · rebond 44% (7/13)
      · −4.0% : fill 13% (7/74) · rebond 28% (3/7)
      · −5.0% : fill 10% (6/74) · rebond 56% (4/6)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 76% si les 15 1res min sont vertes (70 cas) · 30% si rouges (90 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.13% .. +4.95%] · haut q95 +6.66% · bas q05 -4.39%
   - 60min (n=160) : retour [-4.59% .. +5.61%] · haut q95 +6.66% · bas q05 -5.57%
   - session (n=160) : retour [-7.3% .. +8.87%] · haut q95 +9.79% · bas q05 -8.72%


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.41 · part idiosyncratique 0.59
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 30.4  _(momentum baissier)_
- **ADX** : 26.6  _(tendance etablie)_
- **MACD** : hist -1.03  _(pas de croisement recent)_
- **BB** : %B 0.34 · largeur 76.9%
- **ATR** : 4.13 (97.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.003  _(neutre)_
- **Vol ratio** : 0.73  _(volume normal)_
- **Choppiness** : 36.1  _(marche directionnel)_
- **MA** : MA20 37.97 · MA50 33.21 · MA200 35.49  _(prix < MA20)_
- **Dist MA** : MA20 -12.2% · MA50 +0.3% · MA200 -6.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (39529 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
