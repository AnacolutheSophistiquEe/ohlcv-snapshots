# AL2SI

**Generated** : 2026-06-25T21:43:37.647670+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 14.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite extreme · €25.48  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US Core PCE Price Index (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot €25.48 (+14.0% vs entrée) · entrée €22.36 · stop €20.57 · T1 €24.18 · R/R 1.02  
> ↳ P(T1 av. stop) 25 % · EV/risk -0.012 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -20 % hors [0,100] (R² max 0.95). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €22.08–€22.64 (mid €22.36)
- Spot actuel : €25.48 (+14.0% au-dessus de la zone — repli à attendre)
- Stop : €20.57 (stop swing_plan-based (-34.78%))
- Targets : T1 €24.18 · R/R 1.02 | T2 €26.01 · R/R 2.04 | T3 €27.83 · R/R 3.06
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €20.57


## Edge, scénarios & sizing

- EV/risk : -0.012 | EV/share : €-0.022 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 25 % | T2 4 % | T3 0 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 10.2 | bear 62.0 | side 27.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 153.0 (= 6 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→80% · +2.0%→76% · +3.0%→65% · +5.0%→42% · +8.0%→21%
- Range intraday médian 7.78% (p90 13.94%) · excursion haute méd. +4.23% / basse méd. −3.18%
- Profil de vol intra : ouverture 5.392% vs midi 1.608% vs clôture 1.902% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (134 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 11% · trend ↑0%/↓2% ; spike-down 70% · recovery-V 38%)_
- **Régime intraday** : **chop** _(efficiency 0.175 ; neutre — autocorr -0.022)_ ; drift intra méd. 0.277% ; recovery-V 32%
- **σ réalisé intraday** 8.171% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 63% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 30.0938 (VA 29.5312–33.2812 ; dernier close 27.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 37% · rebond 86% · **stop −5.48%** sous le fill (sous le bruit) · cible +2.53% · R/R 0.46 (high win-rate)
- Gaps overnight (n=133) : méd. 0.16% · baisse 42% (gap-down >1% 26% · >2% 10%)
- Excursion ouverture 5min (n=134) : bas méd −0.86% (p90 −4.54%) · haut méd +1.01% · range méd 2.69%
- Excursion ouverture 15min (n=134) : bas méd −1.32% (p90 −5.86%) · haut méd +1.5% · range méd 3.25%
- Excursion ouverture 30min (n=134) : bas méd −1.39% (p90 −5.86%) · haut méd +1.69% · range méd 4.05%
- Excursion ouverture 60min (n=134) : bas méd −1.93% (p90 −6.69%) · haut méd +2.54% · range méd 5.21%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 27.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 77% (101/133) · gap 31% · délai 0.1min · rebond 65% (66/101) (MFE +2.42%)
   - −1.0% : fill 30min 58% · séance 74% (96/133) · gap 26% · délai 0.4min · rebond 67% (65/96) (MFE +2.06%)
   - −1.5% : fill 30min 50% · séance 69% (87/133) · gap 15% · délai 1.5min · rebond 65% (55/87) (MFE +1.73%)
   - −2.0% : fill 30min 41% · séance 58% (74/133) · gap 10% · délai 3.1min · rebond 63% (48/74) (MFE +1.34%)
   - −3.0% : fill 30min 28% · séance 50% (60/133) · gap 7% · délai 10.9min · rebond 80% (49/60) (MFE +2.22%)
   - −4.0% : fill 30min 21% · séance 41% (50/133) · gap 6% · délai 20.5min · rebond 76% (39/50) (MFE +2.67%)
   - −5.0% : fill 30min 18% · séance 37% (43/133) · gap 6% · délai 27.7min · rebond 86% (40/43) (MFE +2.53%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.47% (p90 −5.51%) → stop au-delà de −2.66% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.62% (p90 −5.43%) → stop au-delà de −2.99% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −5.57%) → stop au-delà de −2.99% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1247 jambes) : jambe baissière méd −1.21% (p90 −3.19%) · ~19.0 jambes/séance
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
   - **gap-up** (57 séances) :
      · −1.0% : fill 53% (31/57) · rebond 66% (20/31)
      · −2.0% : fill 39% (22/57) · rebond 73% (15/22)
      · −3.0% : fill 30% (17/57) · rebond 92% (14/17)
      · −4.0% : fill 21% (12/57) · rebond 85% (8/12)
      · −5.0% : fill 20% (9/57) · rebond 100% (9/9)
- **P(clôture VERTE) selon le drive 15min** (n=134) : 52% en base · 67% si les 15 1res min sont vertes (65 cas) · 39% si rouges (69 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=134) : retour [-3.79% .. +6.85%] · haut q95 +8.73% · bas q05 -7.7%
   - 60min (n=134) : retour [-5.77% .. +9.46%] · haut q95 +9.97% · bas q05 -8.24%
   - session (n=134) : retour [-8.33% .. +18.38%] · haut q95 +19.16% · bas q05 -11.49%


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.25 · part idiosyncratique 0.75
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US Core PCE Price Index (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 25.1  _(survente)_
- **ADX** : 31.0  _(tendance etablie)_
- **MACD** : hist -3.059  _(pas de croisement recent)_
- **BB** : %B 0.14 · largeur 116.7%
- **ATR** : 6.64 (100.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.075  _(distribution)_
- **Vol ratio** : 1.48  _(volume normal)_
- **Choppiness** : 32.0  _(marche directionnel)_
- **MA** : MA20 43.6 · MA50 41.74 · MA200 22.29  _(prix < MA20)_
- **Dist MA** : MA20 -41.6% · MA50 -39.0% · MA200 +14.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (42676 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
