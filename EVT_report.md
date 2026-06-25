# EVT

**Generated** : 2026-06-25T21:39:14.194701+00:00  
**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · €4.84  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US Core PCE Price Index (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot €4.84 (+1.9% vs entrée) · entrée €4.75 · stop €4.69 · T1 €4.81 · R/R 1.0  
> ↳ P(T1 av. stop) 41 % _(réel 5 s)_ · EV/risk 0.003 _(réel 5 s)_ (GBM -0.019) · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €4.73–€4.76 (mid €4.75)
- Spot actuel : €4.84 (+1.9% au-dessus de la zone — repli à attendre)
- Stop : €4.69 (stop swing_plan-based (-5.65%))
- Targets : T1 €4.81 · R/R 1.0 | T2 €4.88 · R/R 2.17 | T3 €4.95 · R/R 3.33
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €4.69


## Edge, scénarios & sizing

- EV/risk : -0.019 | EV/share : €-0.001 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 24 % | T3 11 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 11.2 | bear 6.2 | side 82.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 285.0 (= 59 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.881% → cible +1.411% / stop −1.171%, p_fill 48%, n_eff≈23.2) : P(cible|rempli) **41%** · **EV/risk +0.003** (×p_fill ; si rempli +0.01% du capital)
  - **swing** (entrée dip −4.135% → cible +3.159% / stop −1.58%, p_fill 28%, n_eff≈12.7) : P(cible|rempli) **12%** · **EV/risk -0.194** (×p_fill ; si rempli -1.11% du capital)
  - **deep** (entrée dip −6.398% → cible +4.467% / stop −2.235%, p_fill 38%, n_eff≈14.1) : P(cible|rempli) **36%** · **EV/risk +0.002** (×p_fill ; si rempli +0.01% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→68% · +2.0%→42% · +3.0%→26% · +5.0%→9% · +8.0%→2%
- Range intraday médian 4.73% (p90 7.61%) · excursion haute méd. +1.82% / basse méd. −2.41%
- Profil de vol intra : ouverture 2.962% vs midi 1.283% vs clôture 1.282% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 94% · range 6% · trend ↑0%/↓0% ; spike-down 59% · recovery-V 38%)_
- **Régime intraday** : **chop** _(efficiency 0.099 ; mean-reverting — autocorr -0.116)_ ; drift intra méd. 0.089% ; recovery-V 41%
- **σ réalisé intraday** 3.064% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 69% / whipsaw 42%
- POC intraday (dernière séance, temps-au-prix) : 4.7769 (VA 4.6698–4.7922 ; dernier close 4.85)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 33% · rebond 74% · **stop −2.37%** sous le fill (sous le bruit) · cible +1.89% · R/R 0.8 (high win-rate)
- Gaps overnight (n=159) : méd. 0.0% · baisse 49% (gap-down >1% 20% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.61% (p90 −2.26%) · haut méd +0.49% · range méd 1.39%
- Excursion ouverture 15min (n=160) : bas méd −0.81% (p90 −2.59%) · haut méd +0.84% · range méd 1.78%
- Excursion ouverture 30min (n=160) : bas méd −0.96% (p90 −2.72%) · haut méd +0.95% · range méd 2.08%
- Excursion ouverture 60min (n=160) : bas méd −1.09% (p90 −2.86%) · haut méd +0.96% · range méd 2.38%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 4.85 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 84% (130/159) · gap 33% · délai 0.3min · rebond 62% (83/130) (MFE +1.32%)
   - −1.0% : fill 30min 51% · séance 76% (118/159) · gap 20% · délai 1.0min · rebond 63% (74/118) (MFE +1.39%)
   - −1.5% : fill 30min 35% · séance 59% (95/159) · gap 15% · délai 13.9min · rebond 59% (59/95) (MFE +1.28%)
   - −2.0% : fill 30min 28% · séance 49% (77/159) · gap 11% · délai 14.9min · rebond 58% (48/77) (MFE +1.31%)
   - −3.0% : fill 30min 17% · séance 33% (54/159) · gap 6% · délai 28.0min · rebond 74% (42/54) (MFE +1.89%)
   - −4.0% : fill 30min 8% · séance 20% (30/159) · gap 1% · délai 46.1min · rebond 66% (20/30) (MFE +1.7%)
   - −5.0% : fill 30min 4% · séance 10% (18/159) · gap 0% · délai 63.5min · rebond 75% (13/18) (MFE +2.03%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.48% (p90 −2.05%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.56% (p90 −2.39%) → stop au-delà de −1.18% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −1.79%) → stop au-delà de −1.03% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=794 jambes) : jambe baissière méd −1.07% (p90 −2.33%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (63 séances) :
      · −1.0% : fill 93% (60/63) · rebond 62% (35/60)
      · −2.0% : fill 69% (45/63) · rebond 61% (28/45)
      · −3.0% : fill 52% (34/63) · rebond 76% (26/34)
      · −4.0% : fill 34% (21/63) · rebond 65% (15/21)
      · −5.0% : fill 19% (14/63) · rebond 74% (10/14)
   - **flat** (39 séances) :
      · −1.0% : fill 80% (28/39) · rebond 75% (21/28)
      · −2.0% : fill 45% (15/39) · rebond 48% (9/15)
      · −3.0% : fill 19% (8/39) · rebond 92% (7/8)
      · −4.0% : fill 14% (4/39) · rebond 54% (2/4)
      · −5.0% : fill 7% (3/39) · rebond 74% (2/3)
   - **gap-up** (57 séances) :
      · −1.0% : fill 54% (30/57) · rebond 56% (18/30)
      · −2.0% : fill 29% (17/57) · rebond 60% (11/17)
      · −3.0% : fill 21% (12/57) · rebond 57% (9/12)
      · −4.0% : fill 9% (5/57) · rebond 80% (3/5)
      · −5.0% : fill 1% (1/57) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 55% en base · 65% si les 15 1res min sont vertes (77 cas) · 45% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.26% .. +2.56%] · haut q95 +3.86% · bas q05 -3.06%
   - 60min (n=160) : retour [-2.86% .. +3.32%] · haut q95 +4.52% · bas q05 -3.38%
   - session (n=160) : retour [-4.47% .. +4.19%] · haut q95 +6.32% · bas q05 -5.4%


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.17 · part idiosyncratique 0.83
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US Core PCE Price Index (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 46.5  _(neutre)_
- **ADX** : 11.1  _(pas de tendance nette)_
- **MACD** : hist 0.009  _(bullish_recent)_
- **BB** : %B 0.49 · largeur 18.2%
- **ATR** : 0.19 (5.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.141  _(accumulation)_
- **Vol ratio** : 1.28  _(volume normal)_
- **Choppiness** : 66.2  _(marche en range (choppy))_
- **MA** : MA20 4.85 · MA50 5.04 · MA200 5.57  _(prix < MA20)_
- **Dist MA** : MA20 -0.2% · MA50 -4.0% · MA200 -13.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (43687 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
