# EVT

**Generated** : 2026-06-24T00:04:37.633236+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €4.72  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot €4.72 (+1.5% vs entrée) · entrée €4.65 · stop €4.59 · T1 €4.71 · R/R 1.0  
> ↳ P(T1 av. stop) 38 % _(réel 5 s)_ · EV/risk -0.084 _(réel 5 s)_ (GBM -0.016) · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -103 % hors [0,100] (R² max 0.95). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €4.63–€4.66 (mid €4.65)
- Spot actuel : €4.72 (+1.5% au-dessus de la zone — repli à attendre)
- Stop : €4.59 (stop swing_plan-based (-4.91%))
- Targets : T1 €4.71 · R/R 1.0 | T2 €4.78 · R/R 2.17 | T3 €4.85 · R/R 3.33
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €4.59


## Edge, scénarios & sizing

- EV/risk : -0.016 | EV/share : €-0.001 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 23 % | T3 11 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 11.1 | bear 6.2 | side 82.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.525% → cible +1.435% / stop −1.142%, p_fill 59%, n_eff≈25.9) : P(cible|rempli) **38%** · **EV/risk -0.084** (×p_fill ; si rempli -0.16% du capital)
  - **swing** (entrée dip −3.359% → cible +3.209% / stop −1.605%, p_fill 46%, n_eff≈17.1) : P(cible|rempli) **22%** · **EV/risk -0.187** (×p_fill ; si rempli -0.66% du capital)
  - **deep** (entrée dip −5.187% → cible +4.538% / stop −2.27%, p_fill 47%, n_eff≈16.6) : P(cible|rempli) **29%** · **EV/risk -0.088** (×p_fill ; si rempli -0.42% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→66% · +2.0%→41% · +3.0%→25% · +5.0%→8% · +8.0%→2%
- Range intraday médian 4.77% (p90 7.61%) · excursion haute méd. +1.75% / basse méd. −2.44%
- Profil de vol intra : ouverture 2.973% vs midi 1.271% vs clôture 1.286% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 93% · range 7% · trend ↑0%/↓0% ; spike-down 61% · recovery-V 38%)_
- **Régime intraday** : **chop** _(efficiency 0.096 ; mean-reverting — autocorr -0.13)_ ; drift intra méd. -0.228% ; recovery-V 41%
- **σ réalisé intraday** 3.056% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 71% / whipsaw 41%
- POC intraday (dernière séance, temps-au-prix) : 4.6504 (VA 4.6055–4.6607 ; dernier close 4.636)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 34% · rebond 74% · **stop −2.37%** sous le fill (sous le bruit) · cible +1.89% · R/R 0.8 (high win-rate)
- Gaps overnight (n=159) : méd. 0.01% · baisse 47% (gap-down >1% 19% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.61% (p90 −2.28%) · haut méd +0.49% · range méd 1.43%
- Excursion ouverture 15min (n=160) : bas méd −0.82% (p90 −2.64%) · haut méd +0.81% · range méd 1.82%
- Excursion ouverture 30min (n=160) : bas méd −1.02% (p90 −2.73%) · haut méd +0.93% · range méd 2.16%
- Excursion ouverture 60min (n=160) : bas méd −1.1% (p90 −2.9%) · haut méd +0.95% · range méd 2.46%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 4.636 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 84% (128/159) · gap 31% · délai 0.3min · rebond 60% (81/128) (MFE +1.29%)
   - −1.0% : fill 30min 49% · séance 74% (116/159) · gap 19% · délai 1.6min · rebond 61% (72/116) (MFE +1.33%)
   - −1.5% : fill 30min 36% · séance 62% (95/159) · gap 16% · délai 13.9min · rebond 59% (59/95) (MFE +1.28%)
   - −2.0% : fill 30min 29% · séance 50% (77/159) · gap 11% · délai 14.9min · rebond 58% (48/77) (MFE +1.31%)
   - −3.0% : fill 30min 17% · séance 34% (54/159) · gap 6% · délai 28.0min · rebond 74% (42/54) (MFE +1.89%)
   - −4.0% : fill 30min 8% · séance 21% (30/159) · gap 1% · délai 46.1min · rebond 66% (20/30) (MFE +1.7%)
   - −5.0% : fill 30min 4% · séance 10% (18/159) · gap 0% · délai 63.5min · rebond 75% (13/18) (MFE +2.03%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.48% (p90 −2.18%) → stop au-delà de −1.49% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.56% (p90 −2.5%) → stop au-delà de −1.31% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −1.86%) → stop au-delà de −1.25% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=802 jambes) : jambe baissière méd −1.06% (p90 −2.33%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (61 séances) :
      · −1.0% : fill 92% (58/61) · rebond 57% (33/58)
      · −2.0% : fill 76% (45/61) · rebond 61% (28/45)
      · −3.0% : fill 57% (34/61) · rebond 76% (26/34)
      · −4.0% : fill 37% (21/61) · rebond 65% (15/21)
      · −5.0% : fill 21% (14/61) · rebond 74% (10/14)
   - **flat** (39 séances) :
      · −1.0% : fill 80% (28/39) · rebond 75% (21/28)
      · −2.0% : fill 45% (15/39) · rebond 48% (9/15)
      · −3.0% : fill 19% (8/39) · rebond 92% (7/8)
      · −4.0% : fill 14% (4/39) · rebond 54% (2/4)
      · −5.0% : fill 7% (3/39) · rebond 74% (2/3)
   - **gap-up** (59 séances) :
      · −1.0% : fill 54% (30/59) · rebond 56% (18/30)
      · −2.0% : fill 29% (17/59) · rebond 60% (11/17)
      · −3.0% : fill 21% (12/59) · rebond 57% (9/12)
      · −4.0% : fill 9% (5/59) · rebond 80% (3/5)
      · −5.0% : fill 1% (1/59) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 53% en base · 62% si les 15 1res min sont vertes (76 cas) · 45% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.32% .. +2.62%] · haut q95 +4.0% · bas q05 -3.13%
   - 60min (n=160) : retour [-2.89% .. +3.33%] · haut q95 +4.55% · bas q05 -3.4%
   - session (n=160) : retour [-4.53% .. +4.24%] · haut q95 +5.49% · bas q05 -5.43%


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.17 · part idiosyncratique 0.83
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 39.8  _(momentum baissier)_
- **ADX** : 10.3  _(pas de tendance nette)_
- **MACD** : hist -0.015  _(pas de croisement recent)_
- **BB** : %B 0.34 · largeur 18.8%
- **ATR** : 0.18 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.164  _(accumulation)_
- **Vol ratio** : 0.39  _(volume atone)_
- **Choppiness** : 49.1  _(transition)_
- **MA** : MA20 4.87 · MA50 5.07 · MA200 5.58  _(prix < MA20)_
- **Dist MA** : MA20 -3.1% · MA50 -6.8% · MA200 -15.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (41345 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
