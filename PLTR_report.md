# PLTR

**Generated** : 2026-06-26T00:14:48.738132+00:00  
**Santé technique** : 1/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $107.27  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (Kelly ≤ 0)  
> ↳ spot $107.27 (+6.0% vs entrée) · entrée $101.18 · stop $99.36 · T1 $103.63 · R/R 1.35  
> ↳ P(T1 av. stop) 27 % · EV/risk -0.031 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -60 % hors [0,100] (R² max 0.34). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 1/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $100.69–$101.67 (mid $101.18)
- Spot actuel : $107.27 (+6.0% au-dessus de la zone — repli à attendre)
- Stop : $99.36 (stop swing_plan-based (-13.75%))
- Targets : T1 $103.63 · R/R 1.35 | T2 $106.08 · R/R 2.69 | T3 $108.53 · R/R 4.04
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $99.36


## Edge, scénarios & sizing

- EV/risk : -0.031 | EV/share : $-0.057 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 27 % | T2 5 % | T3 0 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 19.0 | bear 70.7 | side 10.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=3, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→71% · +2.0%→38% · +3.0%→20% · +5.0%→6% · +8.0%→1%
- Range intraday médian 3.89% (p90 7.17%) · excursion haute méd. +1.75% / basse méd. −1.71%
- Profil de vol intra : ouverture 2.801% vs midi 0.73% vs clôture 0.805% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 79% · range 20% · trend ↑0%/↓1% ; spike-down 58% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; neutre — autocorr 0.002)_ ; drift intra méd. -0.516% ; recovery-V 24%
- **σ réalisé intraday** 2.652% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 55% / whipsaw 11%
- POC intraday (dernière séance, temps-au-prix) : 113.2594 (VA 112.3266–115.2581 ; dernier close 113.44)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 18% · rebond 55% · **stop −3.03%** sous le fill (sous le bruit) · cible +1.08% · R/R 0.36 (high win-rate)
- Gaps overnight (n=159) : méd. -0.24% · baisse 58% (gap-down >1% 32% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.87% (p90 −1.97%) · haut méd +0.83% · range méd 1.75%
- Excursion ouverture 15min (n=160) : bas méd −1.02% (p90 −2.79%) · haut méd +1.0% · range méd 2.19%
- Excursion ouverture 30min (n=160) : bas méd −1.26% (p90 −3.33%) · haut méd +1.22% · range méd 2.61%
- Excursion ouverture 60min (n=160) : bas méd −1.37% (p90 −3.83%) · haut méd +1.44% · range méd 3.04%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 113.44 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 76% (118/159) · gap 43% · délai 0.0min · rebond 54% (65/118) (MFE +1.07%)
   - −1.0% : fill 30min 61% · séance 74% (110/159) · gap 32% · délai 0.0min · rebond 63% (66/110) (MFE +1.39%)
   - −1.5% : fill 30min 50% · séance 64% (92/159) · gap 21% · délai 1.3min · rebond 67% (59/92) (MFE +1.55%)
   - −2.0% : fill 30min 42% · séance 55% (77/159) · gap 16% · délai 4.6min · rebond 63% (50/77) (MFE +1.53%)
   - −3.0% : fill 30min 19% · séance 36% (56/159) · gap 5% · délai 21.8min · rebond 48% (28/56) (MFE +0.96%)
   - −4.0% : fill 30min 12% · séance 25% (39/159) · gap 4% · délai 29.5min · rebond 45% (19/39) (MFE +0.88%)
   - −5.0% : fill 30min 9% · séance 18% (26/159) · gap 3% · délai 30.2min · rebond 55% (14/26) (MFE +1.08%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.3% (p90 −1.83%) → stop au-delà de −1.32% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.54% (p90 −1.45%) → stop au-delà de −1.33% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.38% (p90 −1.38%) → stop au-delà de −1.36% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=550 jambes) : jambe baissière méd −1.09% (p90 −2.7%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (68 séances) :
      · −1.0% : fill 97% (65/68) · rebond 67% (42/65)
      · −2.0% : fill 81% (54/68) · rebond 65% (38/54)
      · −3.0% : fill 56% (39/68) · rebond 42% (21/39)
      · −4.0% : fill 40% (27/68) · rebond 41% (13/27)
      · −5.0% : fill 33% (19/68) · rebond 57% (10/19)
   - **flat** (33 séances) :
      · −1.0% : fill 83% (26/33) · rebond 42% (14/26)
      · −2.0% : fill 55% (13/33) · rebond 70% (8/13)
      · −3.0% : fill 43% (11/33) · rebond 75% (6/11)
      · −4.0% : fill 22% (8/33) · rebond 71% (5/8)
      · −5.0% : fill 5% (4/33) · rebond 63% (3/4)
   - **gap-up** (58 séances) :
      · −1.0% : fill 37% (19/58) · rebond 72% (10/19)
      · −2.0% : fill 17% (10/58) · rebond 42% (4/10)
      · −3.0% : fill 6% (6/58) · rebond 14% (1/6)
      · −4.0% : fill 4% (4/58) · rebond 18% (1/4)
      · −5.0% : fill 3% (3/58) · rebond 12% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 62% si les 15 1res min sont vertes (79 cas) · 32% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.04% .. +2.49%] · haut q95 +3.22% · bas q05 -4.29%
   - 60min (n=160) : retour [-3.53% .. +2.91%] · haut q95 +3.55% · bas q05 -4.46%
   - session (n=160) : retour [-4.98% .. +4.06%] · haut q95 +4.6% · bas q05 -5.85%


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.66 · part idiosyncratique 0.34
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 16.6  _(survente)_
- **ADX** : 21.2  _(pas de tendance nette)_
- **MACD** : hist -2.797  _(pas de croisement recent)_
- **BB** : %B 0.01 · largeur 40.7%
- **ATR** : 6.09 (14.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.12  _(distribution)_
- **Vol ratio** : 1.33  _(volume normal)_
- **Choppiness** : 33.1  _(marche directionnel)_
- **MA** : MA20 133.7 · MA50 137.04 · MA200 159.09  _(prix < MA20)_
- **Dist MA** : MA20 -19.8% · MA50 -21.7% · MA200 -32.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (39071 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
