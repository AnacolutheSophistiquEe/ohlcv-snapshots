# RHM

**Generated** : 2026-06-25T00:02:01.791139+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 0/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €945.40  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US Core PCE Price Index (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot €945.40 (+7.5% vs entrée) · entrée €879.67 · stop €859.95 · T1 €904.93 · R/R 1.28  
> ↳ P(T1 av. stop) 21 % · EV/risk -0.039 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -74 % hors [0,100] (R² max 0.99). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 0/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €874.62–€884.72 (mid €879.67)
- Spot actuel : €945.40 (+7.5% au-dessus de la zone — repli à attendre)
- Stop : €859.95 (stop swing_plan-based (-16.67%))
- Targets : T1 €904.93 · R/R 1.28 | T2 €930.18 · R/R 2.56 | T3 €955.44 · R/R 3.84
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €859.95


## Edge, scénarios & sizing

- EV/risk : -0.039 | EV/share : €-0.776 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 21 % | T2 2 % | T3 0 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 50.1 | bear 6.8 | side 43.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=4, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→62% · +2.0%→50% · +3.0%→31% · +5.0%→2% · +8.0%→0%
- Range intraday médian 4.16% (p90 6.64%) · excursion haute méd. +2.01% / basse méd. −1.59%
- Profil de vol intra : ouverture 2.418% vs midi 0.888% vs clôture 1.011% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 51% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.093 ; neutre — autocorr 0.02)_ ; drift intra méd. -0.237% ; recovery-V 34%
- **σ réalisé intraday** 2.648% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 62% / bas 65% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 1190.885 (VA 1183.335–1196.925 ; dernier close 1169.6)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 47% · rebond 67% · **stop −3.12%** sous le fill (sous le bruit) · cible +1.37% · R/R 0.44 (high win-rate)
- Gaps overnight (n=159) : méd. 0.05% · baisse 42% (gap-down >1% 17% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.64% (p90 −1.66%) · haut méd +0.57% · range méd 1.48%
- Excursion ouverture 15min (n=160) : bas méd −0.88% (p90 −1.94%) · haut méd +0.78% · range méd 1.81%
- Excursion ouverture 30min (n=160) : bas méd −0.97% (p90 −2.2%) · haut méd +0.92% · range méd 2.11%
- Excursion ouverture 60min (n=160) : bas méd −0.98% (p90 −2.42%) · haut méd +1.0% · range méd 2.25%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1169.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 77% (118/159) · gap 27% · délai 0.3min · rebond 57% (61/118) (MFE +1.21%)
   - −1.0% : fill 30min 46% · séance 72% (105/159) · gap 17% · délai 5.4min · rebond 60% (58/105) (MFE +1.39%)
   - −1.5% : fill 30min 27% · séance 55% (78/159) · gap 8% · délai 28.1min · rebond 55% (40/78) (MFE +1.2%)
   - −2.0% : fill 30min 22% · séance 47% (69/159) · gap 6% · délai 40.4min · rebond 67% (40/69) (MFE +1.37%)
   - −3.0% : fill 30min 9% · séance 28% (45/159) · gap 2% · délai 122.6min · rebond 67% (30/45) (MFE +1.46%)
   - −4.0% : fill 30min 3% · séance 18% (27/159) · gap 1% · délai 319.7min · rebond 52% (16/27) (MFE +1.08%)
   - −5.0% : fill 30min 1% · séance 10% (17/159) · gap 0% · délai 239.3min · rebond 40% (10/17) (MFE +0.69%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.4% (p90 −1.47%) → stop au-delà de −1.18% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.35% (p90 −1.59%) → stop au-delà de −1.3% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.24% (p90 −1.61%) → stop au-delà de −1.25% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=439 jambes) : jambe baissière méd −1.11% (p90 −2.51%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 98% (48/49) · rebond 60% (24/48)
      · −2.0% : fill 78% (37/49) · rebond 75% (24/37)
      · −3.0% : fill 41% (26/49) · rebond 70% (19/26)
      · −4.0% : fill 26% (15/49) · rebond 56% (10/15)
      · −5.0% : fill 15% (10/49) · rebond 59% (8/10)
   - **flat** (50 séances) :
      · −1.0% : fill 76% (35/50) · rebond 70% (23/35)
      · −2.0% : fill 34% (17/50) · rebond 65% (9/17)
      · −3.0% : fill 20% (10/50) · rebond 42% (5/10)
      · −4.0% : fill 18% (8/50) · rebond 16% (2/8)
      · −5.0% : fill 16% (6/50) · rebond 22% (1/6)
   - **gap-up** (60 séances) :
      · −1.0% : fill 46% (22/60) · rebond 43% (11/22)
      · −2.0% : fill 33% (15/60) · rebond 53% (7/15)
      · −3.0% : fill 24% (9/60) · rebond 82% (6/9)
      · −4.0% : fill 10% (4/60) · rebond 100% (4/4)
      · −5.0% : fill 0% (1/60) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 62% si les 15 1res min sont vertes (87 cas) · 32% si rouges (73 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.26% .. +3.22%] · haut q95 +3.92% · bas q05 -2.82%
   - 60min (n=160) : retour [-2.6% .. +3.07%] · haut q95 +4.16% · bas q05 -3.21%
   - session (n=160) : retour [-5.91% .. +3.42%] · haut q95 +4.74% · bas q05 -6.79%


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.31 · part idiosyncratique 0.69
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US Core PCE Price Index (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 23.3  _(survente)_
- **ADX** : 25.4  _(tendance etablie)_
- **MACD** : hist -11.038  _(bearish_recent)_
- **BB** : %B -0.4 · largeur 22.7%
- **ATR** : 65.73 (65.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.203  _(distribution)_
- **Vol ratio** : 4.11  _(volume au-dessus de la moyenne)_
- **Choppiness** : 41.1  _(transition)_
- **MA** : MA20 1187.66 · MA50 1255.23 · MA200 1574.81  _(prix < MA20)_
- **Dist MA** : MA20 -20.4% · MA50 -24.7% · MA200 -40.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (39594 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
