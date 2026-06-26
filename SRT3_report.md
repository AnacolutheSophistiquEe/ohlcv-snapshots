# SRT3

**Generated** : 2026-06-26T21:37:10.070641+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €224.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €224.00 (+0.5% vs entrée) · entrée €222.80 · stop €219.79 · T1 €225.80 · R/R 1.0  
> ↳ P(T1 av. stop) 37 % _(réel 5 s)_ · EV/risk -0.216 _(réel 5 s)_ (GBM 0.01) · ¼-Kelly 0.002 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €222.20–€223.40 (mid €222.80)
- Spot actuel : €224.00 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : €219.79 (stop swing_plan-based (-2.67%))
- Targets : T1 €225.80 · R/R 1.0 | T2 €228.81 · R/R 2.0 | T3 €231.82 · R/R 3.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €219.79


## Edge, scénarios & sizing

- EV/risk : 0.01 | EV/share : €0.030 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 46 % | T2 22 % | T3 8 %
- Kelly (position) : f* 0.007 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 67.2 | bear 15.0 | side 17.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.539% → cible +1.349% / stop −1.348%, p_fill 75%, n_eff≈29.8) : P(cible|rempli) **37%** · **EV/risk -0.216** (×p_fill ; si rempli -0.39% du capital)
  - **swing** (entrée dip −1.179% → cible +3.017% / stop −1.508%, p_fill 78%, n_eff≈31.1) : P(cible|rempli) **23%** · **EV/risk -0.285** (×p_fill ; si rempli -0.55% du capital)
  - **deep** (entrée dip −1.826% → cible +4.267% / stop −2.133%, p_fill 75%, n_eff≈29.7) : P(cible|rempli) **46%** · **EV/risk +0.255** (×p_fill ; si rempli +0.72% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→70% · +2.0%→44% · +3.0%→26% · +5.0%→9% · +8.0%→0%
- Range intraday médian 3.72% (p90 6.59%) · excursion haute méd. +1.8% / basse méd. −1.97%
- Profil de vol intra : ouverture 2.04% vs midi 0.909% vs clôture 1.025% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 8% · trend ↑1%/↓0% ; spike-down 55% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; neutre — autocorr 0.018)_ ; drift intra méd. 0.112% ; recovery-V 25%
- **σ réalisé intraday** 2.498% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 67% / whipsaw 32%
- POC intraday (dernière séance, temps-au-prix) : 221.0688 (VA 216.9438–223.9563 ; dernier close 230.6)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 59% · rebond 66% · **stop −2.62%** sous le fill (sous le bruit) · cible +1.5% · R/R 0.57 (high win-rate)
- Gaps overnight (n=159) : méd. -0.06% · baisse 52% (gap-down >1% 18% · >2% 7%)
- Excursion ouverture 5min (n=160) : bas méd −0.24% (p90 −1.83%) · haut méd +0.56% · range méd 1.16%
- Excursion ouverture 15min (n=160) : bas méd −0.5% (p90 −1.94%) · haut méd +0.67% · range méd 1.52%
- Excursion ouverture 30min (n=160) : bas méd −0.51% (p90 −2.09%) · haut méd +0.8% · range méd 1.75%
- Excursion ouverture 60min (n=160) : bas méd −0.61% (p90 −2.51%) · haut méd +0.84% · range méd 1.9%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 230.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 55% · séance 76% (123/159) · gap 29% · délai 0.3min · rebond 51% (58/123) (MFE +1.02%)
   - −1.0% : fill 30min 42% · séance 63% (103/159) · gap 18% · délai 1.1min · rebond 55% (57/103) (MFE +1.15%)
   - −1.5% : fill 30min 32% · séance 59% (90/159) · gap 12% · délai 13.3min · rebond 66% (54/90) (MFE +1.5%)
   - −2.0% : fill 30min 23% · séance 42% (68/159) · gap 7% · délai 15.1min · rebond 62% (44/68) (MFE +1.42%)
   - −3.0% : fill 30min 7% · séance 24% (39/159) · gap 2% · délai 158.2min · rebond 58% (24/39) (MFE +1.66%)
   - −4.0% : fill 30min 4% · séance 13% (20/159) · gap 1% · délai 208.7min · rebond 67% (15/20) (MFE +1.31%)
   - −5.0% : fill 30min 1% · séance 8% (10/159) · gap 1% · délai 99.8min · rebond 74% (8/10) (MFE +2.47%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.11% (p90 −1.91%) → stop au-delà de −1.1% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.09% (p90 −1.94%) → stop au-delà de −1.11% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.18% (p90 −2.2%) → stop au-delà de −1.45% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=410 jambes) : jambe baissière méd −1.04% (p90 −2.44%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 83% (62/75) · rebond 62% (38/62)
      · −2.0% : fill 60% (42/75) · rebond 67% (29/42)
      · −3.0% : fill 40% (28/75) · rebond 62% (17/28)
      · −4.0% : fill 24% (16/75) · rebond 71% (12/16)
      · −5.0% : fill 12% (7/75) · rebond 92% (6/7)
   - **flat** (37 séances) :
      · −1.0% : fill 59% (21/37) · rebond 40% (10/21)
      · −2.0% : fill 43% (14/37) · rebond 45% (7/14)
      · −3.0% : fill 19% (6/37) · rebond 49% (4/6)
      · −4.0% : fill 12% (3/37) · rebond 44% (2/3)
      · −5.0% : fill 12% (3/37) · rebond 44% (2/3)
   - **gap-up** (47 séances) :
      · −1.0% : fill 41% (20/47) · rebond 52% (9/20)
      · −2.0% : fill 20% (12/47) · rebond 72% (8/12)
      · −3.0% : fill 7% (5/47) · rebond 52% (3/5)
      · −4.0% : fill 2% (1/47) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/47) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 60% si les 15 1res min sont vertes (89 cas) · 41% si rouges (71 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.27% .. +2.12%] · haut q95 +2.66% · bas q05 -2.78%
   - 60min (n=160) : retour [-2.54% .. +2.32%] · haut q95 +2.84% · bas q05 -3.2%
   - session (n=160) : retour [-3.74% .. +4.8%] · haut q95 +5.66% · bas q05 -4.63%


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.45 · part idiosyncratique 0.55
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 35.9  _(momentum baissier)_
- **ADX** : 15.5  _(pas de tendance nette)_
- **MACD** : hist -1.138  _(pas de croisement recent)_
- **BB** : %B 0.36 · largeur 19.4%
- **ATR** : 10.01 (89.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.13  _(distribution)_
- **Vol ratio** : 0.63  _(volume normal)_
- **Choppiness** : 52.2  _(transition)_
- **MA** : MA20 230.43 · MA50 226.71 · MA200 228.85  _(prix < MA20)_
- **Dist MA** : MA20 -2.8% · MA50 -1.2% · MA200 -2.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (39682 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
