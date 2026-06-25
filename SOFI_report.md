# SOFI

**Generated** : 2026-06-25T00:23:36.594787+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $17.31  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)  
> ↳ spot $17.31 (+5.2% vs entrée) · entrée $16.45 · stop $16.05 · T1 $17.24 · R/R 1.98  
> ↳ P(T1 av. stop) 34 % · EV/risk 0.008 · ¼-Kelly 0.001 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.070 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $16.29–$16.61 (mid $16.45)
- Spot actuel : $17.31 (+5.2% au-dessus de la zone — repli à attendre)
- Stop : $16.05 (stop swing_plan-based (-7.26%))
- Targets : T1 $17.24 · R/R 1.98 | T2 $18.02 · R/R 3.93 | T3 $18.81 · R/R 5.9
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.05


## Edge, scénarios & sizing

- EV/risk : 0.008 | EV/share : $0.003 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 17 % | T3 7 %
- Kelly (position) : f* 0.003 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, swing) : bull 24.8 | bear 38.7 | side 36.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 398.0 (= 23 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.263% → cible +2.142% / stop −1.767%, p_fill 51%, n_eff≈19.0) : P(cible|rempli) **27%** · **EV/risk +0.040** (×p_fill ; si rempli +0.14% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=14, n_eff=7))
  - **deep** (entrée dip −7.704% → cible +6.775% / stop −3.387%, p_fill 21%, n_eff≈8.2) : P(cible|rempli) **27%** · **EV/risk -0.051** (×p_fill ; si rempli -0.82% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→71% · +2.0%→46% · +3.0%→35% · +5.0%→8% · +8.0%→0%
- Range intraday médian 4.38% (p90 6.6%) · excursion haute méd. +1.89% / basse méd. −2.16%
- Profil de vol intra : ouverture 2.957% vs midi 0.934% vs clôture 1.021% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 12% · trend ↑1%/↓1% ; spike-down 67% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.115 ; momentum — autocorr 0.046)_ ; drift intra méd. 0.076% ; recovery-V 36%
- **σ réalisé intraday** 3.096% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 56% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 17.4909 (VA 17.2684–17.5354 ; dernier close 17.29)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 48% · rebond 70% · **stop −3.95%** sous le fill (sous le bruit) · cible +2.09% · R/R 0.53 (high win-rate)
- Gaps overnight (n=159) : méd. -0.11% · baisse 51% (gap-down >1% 28% · >2% 12%)
- Excursion ouverture 5min (n=160) : bas méd −0.7% (p90 −1.96%) · haut méd +0.62% · range méd 1.65%
- Excursion ouverture 15min (n=160) : bas méd −1.1% (p90 −3.17%) · haut méd +0.95% · range méd 2.33%
- Excursion ouverture 30min (n=160) : bas méd −1.19% (p90 −3.2%) · haut méd +1.14% · range méd 2.75%
- Excursion ouverture 60min (n=160) : bas méd −1.42% (p90 −3.33%) · haut méd +1.43% · range méd 3.42%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 17.29 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 78% (124/159) · gap 36% · délai 0.0min · rebond 60% (68/124) (MFE +1.34%)
   - −1.0% : fill 30min 53% · séance 69% (113/159) · gap 28% · délai 0.1min · rebond 64% (71/113) (MFE +1.45%)
   - −1.5% : fill 30min 44% · séance 62% (102/159) · gap 20% · délai 1.0min · rebond 66% (65/102) (MFE +1.89%)
   - −2.0% : fill 30min 39% · séance 48% (77/159) · gap 12% · délai 1.7min · rebond 70% (53/77) (MFE +2.09%)
   - −3.0% : fill 30min 23% · séance 36% (58/159) · gap 4% · délai 10.5min · rebond 73% (42/58) (MFE +1.67%)
   - −4.0% : fill 30min 10% · séance 24% (42/159) · gap 2% · délai 62.8min · rebond 62% (27/42) (MFE +1.49%)
   - −5.0% : fill 30min 5% · séance 13% (24/159) · gap 1% · délai 57.6min · rebond 49% (14/24) (MFE +0.96%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.56% (p90 −1.94%) → stop au-delà de −1.59% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.71% (p90 −2.02%) → stop au-delà de −1.59% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.51% (p90 −1.96%) → stop au-delà de −1.27% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=687 jambes) : jambe baissière méd −1.12% (p90 −2.75%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 100% (69/70) · rebond 65% (43/69)
      · −2.0% : fill 85% (56/70) · rebond 71% (41/56)
      · −3.0% : fill 67% (45/70) · rebond 74% (33/45)
      · −4.0% : fill 46% (32/70) · rebond 65% (23/32)
      · −5.0% : fill 25% (17/70) · rebond 48% (11/17)
   - **flat** (24 séances) :
      · −1.0% : fill 58% (16/24) · rebond 43% (10/16)
      · −2.0% : fill 32% (9/24) · rebond 59% (5/9)
      · −3.0% : fill 21% (6/24) · rebond 62% (4/6)
      · −4.0% : fill 9% (3/24) · rebond 0% (0/3)
      · −5.0% : fill 3% (2/24) · rebond 0% (0/2)
   - **gap-up** (65 séances) :
      · −1.0% : fill 38% (28/65) · rebond 72% (18/28)
      · −2.0% : fill 13% (12/65) · rebond 68% (7/12)
      · −3.0% : fill 6% (7/65) · rebond 71% (5/7)
      · −4.0% : fill 6% (7/65) · rebond 64% (4/7)
      · −5.0% : fill 4% (5/65) · rebond 65% (3/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 52% si les 15 1res min sont vertes (72 cas) · 37% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.53% .. +3.59%] · haut q95 +3.9% · bas q05 -4.01%
   - 60min (n=160) : retour [-3.28% .. +3.43%] · haut q95 +4.05% · bas q05 -4.41%
   - session (n=160) : retour [-4.07% .. +4.77%] · haut q95 +5.62% · bas q05 -6.18%


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.38 · part idiosyncratique 0.62
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US Core PCE Price Index (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 54.8  _(neutre)_
- **ADX** : 20.3  _(pas de tendance nette)_
- **MACD** : hist 0.068  _(pas de croisement recent)_
- **BB** : %B 0.58 · largeur 17.0%
- **ATR** : 1.0 (31.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.072  _(distribution)_
- **Vol ratio** : 1.39  _(volume normal)_
- **Choppiness** : 57.6  _(transition)_
- **MA** : MA20 17.07 · MA50 16.98 · MA200 22.58  _(prix > MA20)_
- **Dist MA** : MA20 +1.4% · MA50 +1.9% · MA200 -23.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (45925 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
