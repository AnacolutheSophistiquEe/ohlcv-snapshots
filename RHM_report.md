# RHM

**Generated** : 2026-06-26T21:35:47.531925+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €946.60  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (Kelly ≤ 0)  
> ↳ spot €946.60 (+7.0% vs entrée) · entrée €884.93 · stop €866.43 · T1 €909.18 · R/R 1.31  
> ↳ P(T1 av. stop) 27 % · EV/risk -0.024 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -66 % hors [0,100] (R² max 0.99). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €880.08–€889.78 (mid €884.93)
- Spot actuel : €946.60 (+7.0% au-dessus de la zone — repli à attendre)
- Stop : €866.43 (stop swing_plan-based (-15.69%))
- Targets : T1 €909.18 · R/R 1.31 | T2 €933.43 · R/R 2.62 | T3 €957.68 · R/R 3.93
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €866.43


## Edge, scénarios & sizing

- EV/risk : -0.024 | EV/share : €-0.443 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 27 % | T2 5 % | T3 0 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 16.5 | bear 37.1 | side 46.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=7, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→64% · +2.0%→50% · +3.0%→30% · +5.0%→2% · +8.0%→0%
- Range intraday médian 4.16% (p90 6.7%) · excursion haute méd. +2.02% / basse méd. −1.66%
- Profil de vol intra : ouverture 2.576% vs midi 0.912% vs clôture 1.024% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 53% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.095 ; neutre — autocorr 0.022)_ ; drift intra méd. -0.804% ; recovery-V 36%
- **σ réalisé intraday** 2.99% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 62% / bas 68% / whipsaw 30%
- POC intraday (dernière séance, temps-au-prix) : 954.0475 (VA 928.5775–956.8775 ; dernier close 946.7)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 49% · rebond 66% · **stop −3.38%** sous le fill (sous le bruit) · cible +1.38% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.03% · baisse 44% (gap-down >1% 18% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −0.64% (p90 −1.74%) · haut méd +0.59% · range méd 1.5%
- Excursion ouverture 15min (n=160) : bas méd −0.88% (p90 −1.99%) · haut méd +0.83% · range méd 1.87%
- Excursion ouverture 30min (n=160) : bas méd −0.98% (p90 −2.23%) · haut méd +0.99% · range méd 2.17%
- Excursion ouverture 60min (n=160) : bas méd −1.01% (p90 −2.55%) · haut méd +1.02% · range méd 2.29%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 946.7 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 78% (119/159) · gap 30% · délai 0.3min · rebond 57% (62/119) (MFE +1.21%)
   - −1.0% : fill 30min 48% · séance 73% (106/159) · gap 18% · délai 5.5min · rebond 59% (59/106) (MFE +1.4%)
   - −1.5% : fill 30min 29% · séance 56% (79/159) · gap 10% · délai 21.8min · rebond 55% (41/79) (MFE +1.21%)
   - −2.0% : fill 30min 25% · séance 49% (70/159) · gap 8% · délai 29.4min · rebond 66% (41/70) (MFE +1.38%)
   - −3.0% : fill 30min 10% · séance 30% (46/159) · gap 4% · délai 124.1min · rebond 65% (30/46) (MFE +1.47%)
   - −4.0% : fill 30min 5% · séance 21% (28/159) · gap 2% · délai 285.1min · rebond 51% (16/28) (MFE +1.06%)
   - −5.0% : fill 30min 2% · séance 11% (17/159) · gap 2% · délai 201.2min · rebond 49% (10/17) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.31% (p90 −1.45%) → stop au-delà de −1.12% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.29% (p90 −1.59%) → stop au-delà de −1.3% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.24% (p90 −1.61%) → stop au-delà de −1.25% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=460 jambes) : jambe baissière méd −1.19% (p90 −2.67%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 98% (49/50) · rebond 59% (25/49)
      · −2.0% : fill 80% (38/50) · rebond 72% (25/38)
      · −3.0% : fill 47% (27/50) · rebond 65% (19/27)
      · −4.0% : fill 34% (16/50) · rebond 54% (10/16)
      · −5.0% : fill 19% (10/50) · rebond 70% (8/10)
   - **flat** (50 séances) :
      · −1.0% : fill 76% (35/50) · rebond 70% (23/35)
      · −2.0% : fill 34% (17/50) · rebond 65% (9/17)
      · −3.0% : fill 20% (10/50) · rebond 42% (5/10)
      · −4.0% : fill 18% (8/50) · rebond 16% (2/8)
      · −5.0% : fill 16% (6/50) · rebond 22% (1/6)
   - **gap-up** (59 séances) :
      · −1.0% : fill 46% (22/59) · rebond 43% (11/22)
      · −2.0% : fill 33% (15/59) · rebond 53% (7/15)
      · −3.0% : fill 24% (9/59) · rebond 82% (6/9)
      · −4.0% : fill 10% (4/59) · rebond 100% (4/4)
      · −5.0% : fill 0% (1/59) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 64% si les 15 1res min sont vertes (86 cas) · 31% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.64% .. +3.21%] · haut q95 +3.9% · bas q05 -3.15%
   - 60min (n=160) : retour [-2.89% .. +3.04%] · haut q95 +4.15% · bas q05 -3.47%
   - session (n=160) : retour [-6.85% .. +3.41%] · haut q95 +4.74% · bas q05 -7.13%


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.29 · part idiosyncratique 0.71
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 20.4  _(survente)_
- **ADX** : 30.1  _(tendance etablie)_
- **MACD** : hist -22.992  _(bearish_recent)_
- **BB** : %B -0.07 · largeur 31.4%
- **ATR** : 61.67 (52.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.251  _(distribution)_
- **Vol ratio** : 1.02  _(volume normal)_
- **Choppiness** : 38.5  _(transition)_
- **MA** : MA20 1153.75 · MA50 1233.56 · MA200 1566.63  _(prix < MA20)_
- **Dist MA** : MA20 -18.0% · MA50 -23.3% · MA200 -39.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (38453 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
