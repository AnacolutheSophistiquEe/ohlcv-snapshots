# EVT

**Generated** : 2026-06-25T00:04:41.795835+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €4.85  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US Core PCE Price Index (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot €4.85 (+1.9% vs entrée) · entrée €4.76 · stop €4.70 · T1 €4.83 · R/R 1.17  
> ↳ P(T1 av. stop) 36 % _(réel 5 s)_ · EV/risk -0.028 _(réel 5 s)_ (GBM -0.017) · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €4.74–€4.77 (mid €4.76)
- Spot actuel : €4.85 (+1.9% au-dessus de la zone — repli à attendre)
- Stop : €4.70 (stop swing_plan-based (-5.86%))
- Targets : T1 €4.83 · R/R 1.17 | T2 €4.90 · R/R 2.33 | T3 €4.97 · R/R 3.5
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €4.70


## Edge, scénarios & sizing

- EV/risk : -0.017 | EV/share : €-0.001 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 42 % | T2 22 % | T3 10 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 10.9 | bear 6.2 | side 83.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 155.0 (= 32 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.935% → cible +1.487% / stop −1.198%, p_fill 47%, n_eff≈22.6) : P(cible|rempli) **36%** · **EV/risk -0.028** (×p_fill ; si rempli -0.07% du capital)
  - **swing** (entrée dip −4.268% → cible +3.325% / stop −1.663%, p_fill 28%, n_eff≈12.1) : P(cible|rempli) **10%** · **EV/risk -0.214** (×p_fill ; si rempli -1.27% du capital)
  - **deep** (entrée dip −6.592% → cible +4.704% / stop −2.353%, p_fill 38%, n_eff≈13.2) : P(cible|rempli) **33%** · **EV/risk -0.027** (×p_fill ; si rempli -0.17% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→68% · +2.0%→42% · +3.0%→26% · +5.0%→8% · +8.0%→2%
- Range intraday médian 4.73% (p90 7.61%) · excursion haute méd. +1.82% / basse méd. −2.41%
- Profil de vol intra : ouverture 2.965% vs midi 1.285% vs clôture 1.278% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 93% · range 7% · trend ↑0%/↓0% ; spike-down 60% · recovery-V 38%)_
- **Régime intraday** : **chop** _(efficiency 0.097 ; mean-reverting — autocorr -0.12)_ ; drift intra méd. -0.092% ; recovery-V 41%
- **σ réalisé intraday** 3.028% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 73% / whipsaw 44%
- POC intraday (dernière séance, temps-au-prix) : 4.6776 (VA 4.6215–4.7592 ; dernier close 4.72)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 34% · rebond 74% · **stop −2.37%** sous le fill (sous le bruit) · cible +1.89% · R/R 0.8 (high win-rate)
- Gaps overnight (n=159) : méd. 0.0% · baisse 48% (gap-down >1% 19% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.61% (p90 −2.27%) · haut méd +0.48% · range méd 1.43%
- Excursion ouverture 15min (n=160) : bas méd −0.82% (p90 −2.6%) · haut méd +0.83% · range méd 1.8%
- Excursion ouverture 30min (n=160) : bas méd −1.0% (p90 −2.73%) · haut méd +0.94% · range méd 2.09%
- Excursion ouverture 60min (n=160) : bas méd −1.1% (p90 −2.88%) · haut méd +0.95% · range méd 2.45%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 4.72 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 84% (129/159) · gap 32% · délai 0.3min · rebond 61% (82/129) (MFE +1.3%)
   - −1.0% : fill 30min 50% · séance 75% (117/159) · gap 19% · délai 1.1min · rebond 62% (73/117) (MFE +1.35%)
   - −1.5% : fill 30min 36% · séance 60% (95/159) · gap 15% · délai 13.9min · rebond 59% (59/95) (MFE +1.28%)
   - −2.0% : fill 30min 29% · séance 50% (77/159) · gap 11% · délai 14.9min · rebond 58% (48/77) (MFE +1.31%)
   - −3.0% : fill 30min 17% · séance 34% (54/159) · gap 6% · délai 28.0min · rebond 74% (42/54) (MFE +1.89%)
   - −4.0% : fill 30min 8% · séance 20% (30/159) · gap 1% · délai 46.1min · rebond 66% (20/30) (MFE +1.7%)
   - −5.0% : fill 30min 4% · séance 10% (18/159) · gap 0% · délai 63.5min · rebond 75% (13/18) (MFE +2.03%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.49% (p90 −2.14%) → stop au-delà de −1.48% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.6% (p90 −2.44%) → stop au-delà de −1.28% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.57% (p90 −1.82%) → stop au-delà de −1.12% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=797 jambes) : jambe baissière méd −1.06% (p90 −2.33%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (62 séances) :
      · −1.0% : fill 93% (59/62) · rebond 60% (34/59)
      · −2.0% : fill 72% (45/62) · rebond 61% (28/45)
      · −3.0% : fill 54% (34/62) · rebond 76% (26/34)
      · −4.0% : fill 35% (21/62) · rebond 65% (15/21)
      · −5.0% : fill 20% (14/62) · rebond 74% (10/14)
   - **flat** (39 séances) :
      · −1.0% : fill 80% (28/39) · rebond 75% (21/28)
      · −2.0% : fill 45% (15/39) · rebond 48% (9/15)
      · −3.0% : fill 19% (8/39) · rebond 92% (7/8)
      · −4.0% : fill 14% (4/39) · rebond 54% (2/4)
      · −5.0% : fill 7% (3/39) · rebond 74% (2/3)
   - **gap-up** (58 séances) :
      · −1.0% : fill 54% (30/58) · rebond 56% (18/30)
      · −2.0% : fill 29% (17/58) · rebond 60% (11/17)
      · −3.0% : fill 21% (12/58) · rebond 57% (9/12)
      · −4.0% : fill 9% (5/58) · rebond 80% (3/5)
      · −5.0% : fill 1% (1/58) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 54% en base · 63% si les 15 1res min sont vertes (76 cas) · 45% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.3% .. +2.59%] · haut q95 +3.93% · bas q05 -3.09%
   - 60min (n=160) : retour [-2.88% .. +3.33%] · haut q95 +4.53% · bas q05 -3.39%
   - session (n=160) : retour [-4.5% .. +4.22%] · haut q95 +5.44% · bas q05 -5.41%


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 41.4  _(momentum baissier)_
- **ADX** : 10.7  _(pas de tendance nette)_
- **MACD** : hist 0.0  _(bullish_recent)_
- **BB** : %B 0.49 · largeur 18.8%
- **ATR** : 0.19 (6.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.197  _(accumulation)_
- **Vol ratio** : 1.47  _(volume normal)_
- **Choppiness** : 51.7  _(transition)_
- **MA** : MA20 4.86 · MA50 5.05 · MA200 5.57  _(prix < MA20)_
- **Dist MA** : MA20 -0.3% · MA50 -4.0% · MA200 -13.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (43630 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
