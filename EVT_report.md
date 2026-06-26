# EVT

**Generated** : 2026-06-26T21:38:33.470683+00:00  
**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · €4.91  

> 🟡 **WAIT-FOR-DIP** — spot +2.3 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €4.91 (+2.3% vs entrée) · entrée €4.80 · stop €4.74 · T1 €4.86 · R/R 1.0  
> ↳ P(T1 av. stop) 42 % _(réel 5 s)_ · EV/risk 0.029 _(réel 5 s)_ (GBM -0.023) · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 244 % hors [0,100] (R² max 0.92). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €4.79–€4.81 (mid €4.80)
- Spot actuel : €4.91 (+2.3% au-dessus de la zone — repli à attendre)
- Stop : €4.74 (stop swing_plan-based (-6.28%))
- Targets : T1 €4.86 · R/R 1.0 | T2 €4.93 · R/R 2.17 | T3 €4.99 · R/R 3.17
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €4.74


## Edge, scénarios & sizing

- EV/risk : -0.023 | EV/share : €-0.001 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 25 % | T3 13 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 11.3 | bear 6.1 | side 82.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 285.0 (= 58 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.199% → cible +1.355% / stop −1.146%, p_fill 44%, n_eff≈19.5) : P(cible|rempli) **42%** · **EV/risk +0.029** (×p_fill ; si rempli +0.08% du capital)
  - **swing** (entrée dip −4.849% → cible +3.031% / stop −1.514%, p_fill 25%, n_eff≈11.4) : P(cible|rempli) **11%** · **EV/risk -0.175** (×p_fill ; si rempli -1.07% du capital)
  - **deep** (entrée dip −7.489% → cible +4.285% / stop −2.142%, p_fill 22%, n_eff≈10.4) : P(cible|rempli) **35%** · **EV/risk -0.003** (×p_fill ; si rempli -0.03% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→69% · +2.0%→42% · +3.0%→26% · +5.0%→9% · +8.0%→2%
- Range intraday médian 4.63% (p90 7.61%) · excursion haute méd. +1.82% / basse méd. −2.41%
- Profil de vol intra : ouverture 2.976% vs midi 1.275% vs clôture 1.278% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 94% · range 6% · trend ↑0%/↓0% ; spike-down 60% · recovery-V 40%)_
- **Régime intraday** : **chop** _(efficiency 0.095 ; mean-reverting — autocorr -0.115)_ ; drift intra méd. 0.12% ; recovery-V 45%
- **σ réalisé intraday** 3.079% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 72% / bas 71% / whipsaw 44%
- POC intraday (dernière séance, temps-au-prix) : 4.7358 (VA 4.71–4.7718 ; dernier close 4.88)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 34% · rebond 75% · **stop −2.37%** sous le fill (sous le bruit) · cible +2.14% · R/R 0.9 (high win-rate)
- Gaps overnight (n=159) : méd. -0.02% · baisse 50% (gap-down >1% 20% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.61% (p90 −2.26%) · haut méd +0.48% · range méd 1.43%
- Excursion ouverture 15min (n=160) : bas méd −0.82% (p90 −2.59%) · haut méd +0.83% · range méd 1.79%
- Excursion ouverture 30min (n=160) : bas méd −1.0% (p90 −2.76%) · haut méd +0.94% · range méd 2.09%
- Excursion ouverture 60min (n=160) : bas méd −1.1% (p90 −2.99%) · haut méd +0.95% · range méd 2.43%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 4.88 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 85% (130/159) · gap 33% · délai 0.3min · rebond 62% (84/130) (MFE +1.39%)
   - −1.0% : fill 30min 52% · séance 76% (118/159) · gap 20% · délai 1.0min · rebond 64% (75/118) (MFE +1.42%)
   - −1.5% : fill 30min 36% · séance 60% (95/159) · gap 15% · délai 11.6min · rebond 61% (60/95) (MFE +1.32%)
   - −2.0% : fill 30min 30% · séance 50% (77/159) · gap 11% · délai 14.3min · rebond 60% (49/77) (MFE +1.33%)
   - −3.0% : fill 30min 16% · séance 34% (54/159) · gap 6% · délai 30.7min · rebond 75% (42/54) (MFE +2.14%)
   - −4.0% : fill 30min 8% · séance 20% (29/159) · gap 1% · délai 46.2min · rebond 66% (19/29) (MFE +1.67%)
   - −5.0% : fill 30min 4% · séance 9% (17/159) · gap 0% · délai 63.2min · rebond 75% (12/17) (MFE +2.03%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.49% (p90 −2.44%) → stop au-delà de −1.5% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.56% (p90 −2.39%) → stop au-delà de −1.18% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −1.79%) → stop au-delà de −1.03% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=796 jambes) : jambe baissière méd −1.07% (p90 −2.33%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (63 séances) :
      · −1.0% : fill 93% (60/63) · rebond 62% (35/60)
      · −2.0% : fill 69% (45/63) · rebond 61% (28/45)
      · −3.0% : fill 52% (34/63) · rebond 76% (26/34)
      · −4.0% : fill 34% (21/63) · rebond 65% (15/21)
      · −5.0% : fill 19% (14/63) · rebond 74% (10/14)
   - **flat** (39 séances) :
      · −1.0% : fill 81% (28/39) · rebond 78% (22/28)
      · −2.0% : fill 49% (15/39) · rebond 57% (10/15)
      · −3.0% : fill 25% (8/39) · rebond 94% (7/8)
      · −4.0% : fill 12% (3/39) · rebond 52% (1/3)
      · −5.0% : fill 6% (2/39) · rebond 72% (1/2)
   - **gap-up** (57 séances) :
      · −1.0% : fill 54% (30/57) · rebond 56% (18/30)
      · −2.0% : fill 29% (17/57) · rebond 60% (11/17)
      · −3.0% : fill 21% (12/57) · rebond 57% (9/12)
      · −4.0% : fill 9% (5/57) · rebond 80% (3/5)
      · −5.0% : fill 1% (1/57) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 56% en base · 65% si les 15 1res min sont vertes (76 cas) · 47% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.42% .. +2.53%] · haut q95 +3.84% · bas q05 -3.02%
   - 60min (n=160) : retour [-2.84% .. +3.32%] · haut q95 +4.51% · bas q05 -3.37%
   - session (n=160) : retour [-4.44% .. +4.17%] · haut q95 +6.27% · bas q05 -5.39%


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.25/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.23 · part idiosyncratique 0.77
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 49.1  _(neutre)_
- **ADX** : 11.6  _(pas de tendance nette)_
- **MACD** : hist 0.021  _(bullish_recent)_
- **BB** : %B 0.6 · largeur 16.3%
- **ATR** : 0.18 (4.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.11  _(accumulation)_
- **Vol ratio** : 0.88  _(volume normal)_
- **Choppiness** : 65.8  _(marche en range (choppy))_
- **MA** : MA20 4.83 · MA50 5.03 · MA200 5.56  _(prix > MA20)_
- **Dist MA** : MA20 +1.6% · MA50 -2.4% · MA200 -11.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (43395 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
