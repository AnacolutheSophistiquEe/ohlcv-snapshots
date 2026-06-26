# ENR

**Generated** : 2026-06-26T00:05:46.902975+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €163.82  

> 🟡 **WAIT-FOR-DIP** — spot +9.2 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €163.82 (+9.2% vs entrée) · entrée €150.06 · stop €147.75 · T1 €152.78 · R/R 1.18  
> ↳ P(T1 av. stop) 39 % · EV/risk 0.032 · ¼-Kelly 0.002 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €149.52–€150.61 (mid €150.06)
- Spot actuel : €163.82 (+9.2% au-dessus de la zone — repli à attendre)
- Stop : €147.75 (stop swing_plan-based (-20.13%))
- Targets : T1 €152.78 · R/R 1.18 | T2 €155.51 · R/R 2.36 | T3 €158.23 · R/R 3.54
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €147.75


## Edge, scénarios & sizing

- EV/risk : 0.032 | EV/share : €0.075 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 14 % | T3 3 %
- Kelly (position) : f* 0.009 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 45.4 | bear 26.2 | side 28.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 328.0 (= 2 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→65% · +2.0%→49% · +3.0%→28% · +5.0%→10% · +8.0%→1%
- Range intraday médian 4.42% (p90 6.72%) · excursion haute méd. +1.69% / basse méd. −1.82%
- Profil de vol intra : ouverture 2.195% vs midi 1.026% vs clôture 1.236% _(ouverture ~2.1× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 57% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; neutre — autocorr -0.026)_ ; drift intra méd. -0.379% ; recovery-V 11%
- **σ réalisé intraday** 2.642% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 61% / bas 71% / whipsaw 32%
- POC intraday (dernière séance, temps-au-prix) : 159.3928 (VA 158.7548–160.0308 ; dernier close 159.74)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 36% · rebond 74% · **stop −3.13%** sous le fill (sous le bruit) · cible +1.71% · R/R 0.55 (high win-rate)
- Gaps overnight (n=159) : méd. 0.44% · baisse 39% (gap-down >1% 20% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.61% (p90 −1.83%) · haut méd +0.47% · range méd 1.21%
- Excursion ouverture 15min (n=160) : bas méd −0.71% (p90 −2.21%) · haut méd +0.6% · range méd 1.51%
- Excursion ouverture 30min (n=160) : bas méd −0.87% (p90 −2.47%) · haut méd +0.63% · range méd 1.81%
- Excursion ouverture 60min (n=160) : bas méd −0.97% (p90 −2.57%) · haut méd +0.8% · range méd 2.01%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 159.74 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 73% (111/159) · gap 27% · délai 0.4min · rebond 49% (54/111) (MFE +0.97%)
   - −1.0% : fill 30min 47% · séance 66% (99/159) · gap 20% · délai 2.3min · rebond 54% (57/99) (MFE +1.08%)
   - −1.5% : fill 30min 36% · séance 60% (86/159) · gap 17% · délai 15.6min · rebond 61% (54/86) (MFE +1.47%)
   - −2.0% : fill 30min 23% · séance 44% (63/159) · gap 11% · délai 22.1min · rebond 57% (37/63) (MFE +1.27%)
   - −3.0% : fill 30min 16% · séance 36% (49/159) · gap 5% · délai 169.3min · rebond 74% (37/49) (MFE +1.71%)
   - −4.0% : fill 30min 9% · séance 26% (37/159) · gap 2% · délai 308.0min · rebond 69% (25/37) (MFE +1.79%)
   - −5.0% : fill 30min 2% · séance 16% (21/159) · gap 1% · délai 393.5min · rebond 72% (14/21) (MFE +1.36%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.56% (p90 −1.99%) → stop au-delà de −0.99% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −2.46%) → stop au-delà de −1.46% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −1.54%) → stop au-delà de −0.91% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=510 jambes) : jambe baissière méd −1.07% (p90 −2.5%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (45 séances) :
      · −1.0% : fill 95% (44/45) · rebond 58% (25/44)
      · −2.0% : fill 68% (32/45) · rebond 62% (21/32)
      · −3.0% : fill 61% (28/45) · rebond 74% (21/28)
      · −4.0% : fill 49% (23/45) · rebond 68% (16/23)
      · −5.0% : fill 33% (15/45) · rebond 69% (10/15)
   - **flat** (27 séances) :
      · −1.0% : fill 62% (18/27) · rebond 55% (12/18)
      · −2.0% : fill 30% (8/27) · rebond 35% (3/8)
      · −3.0% : fill 23% (5/27) · rebond 80% (3/5)
      · −4.0% : fill 20% (4/27) · rebond 76% (2/4)
      · −5.0% : fill 12% (2/27) · rebond 74% (1/2)
   - **gap-up** (87 séances) :
      · −1.0% : fill 50% (37/87) · rebond 48% (20/37)
      · −2.0% : fill 33% (23/87) · rebond 56% (13/23)
      · −3.0% : fill 24% (16/87) · rebond 74% (13/16)
      · −4.0% : fill 15% (10/87) · rebond 67% (7/10)
      · −5.0% : fill 8% (4/87) · rebond 78% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 85% si les 15 1res min sont vertes (81 cas) · 18% si rouges (79 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.27% .. +2.21%] · haut q95 +2.84% · bas q05 -2.79%
   - 60min (n=160) : retour [-2.45% .. +2.28%] · haut q95 +3.02% · bas q05 -3.35%
   - session (n=160) : retour [-5.12% .. +4.49%] · haut q95 +5.96% · bas q05 -6.17%


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.54 · part idiosyncratique 0.46
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 54.5  _(neutre)_
- **ADX** : 17.9  _(pas de tendance nette)_
- **MACD** : hist 1.333  _(pas de croisement recent)_
- **BB** : %B 0.67 · largeur 19.1%
- **ATR** : 7.7 (77.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.072  _(distribution)_
- **Vol ratio** : 0.38  _(volume atone)_
- **Choppiness** : 42.1  _(transition)_
- **MA** : MA20 158.61 · MA50 168.85 · MA200 137.51  _(prix > MA20)_
- **Dist MA** : MA20 +3.3% · MA50 -3.0% · MA200 +19.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (37871 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
