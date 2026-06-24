# SOFI

**Generated** : 2026-06-24T00:23:23.417888+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $17.29  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $17.29 (+5.2% vs entrée) · entrée $16.44 · stop $16.04 · T1 $17.23 · R/R 1.97  
> ↳ P(T1 av. stop) 34 % · EV/risk 0.009 · ¼-Kelly 0.001 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.060 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $16.28–$16.60 (mid $16.44)
- Spot actuel : $17.29 (+5.2% au-dessus de la zone — repli à attendre)
- Stop : $16.04 (stop swing_plan-based (-7.21%))
- Targets : T1 $17.23 · R/R 1.97 | T2 $18.02 · R/R 3.95 | T3 $18.81 · R/R 5.92
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.04


## Edge, scénarios & sizing

- EV/risk : 0.009 | EV/share : $0.003 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 17 % | T3 7 %
- Kelly (position) : f* 0.004 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, swing) : bull 23.2 | bear 43.4 | side 33.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 277.0 (= 16 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.243% → cible +2.154% / stop −1.756%, p_fill 54%, n_eff≈19.0) : P(cible|rempli) **27%** · **EV/risk +0.042** (×p_fill ; si rempli +0.14% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=15, n_eff=7))
  - **deep** (entrée dip −7.614% → cible +6.812% / stop −3.406%, p_fill 22%, n_eff≈8.2) : P(cible|rempli) **27%** · **EV/risk -0.054** (×p_fill ; si rempli -0.83% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→71% · +2.0%→46% · +3.0%→35% · +5.0%→8% · +8.0%→0%
- Range intraday médian 4.38% (p90 6.64%) · excursion haute méd. +1.89% / basse méd. −2.16%
- Profil de vol intra : ouverture 2.942% vs midi 0.942% vs clôture 1.022% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 12% · trend ↑1%/↓1% ; spike-down 68% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.113 ; momentum — autocorr 0.038)_ ; drift intra méd. -0.079% ; recovery-V 36%
- **σ réalisé intraday** 3.102% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 62% / bas 59% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 17.2782 (VA 17.1803–17.3272 ; dernier close 17.09)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 36% · rebond 73% · **stop −3.53%** sous le fill (sous le bruit) · cible +1.67% · R/R 0.47 (high win-rate)
- Gaps overnight (n=159) : méd. 0.0% · baisse 50% (gap-down >1% 26% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.73% (p90 −1.97%) · haut méd +0.58% · range méd 1.64%
- Excursion ouverture 15min (n=160) : bas méd −1.13% (p90 −3.18%) · haut méd +0.95% · range méd 2.31%
- Excursion ouverture 30min (n=160) : bas méd −1.2% (p90 −3.2%) · haut méd +1.12% · range méd 2.73%
- Excursion ouverture 60min (n=160) : bas méd −1.44% (p90 −3.34%) · haut méd +1.34% · range méd 3.39%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 17.09 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 77% (123/159) · gap 35% · délai 0.0min · rebond 58% (67/123) (MFE +1.33%)
   - −1.0% : fill 30min 52% · séance 68% (112/159) · gap 26% · délai 0.1min · rebond 63% (70/112) (MFE +1.43%)
   - −1.5% : fill 30min 43% · séance 61% (101/159) · gap 18% · délai 1.3min · rebond 64% (64/101) (MFE +1.85%)
   - −2.0% : fill 30min 38% · séance 47% (76/159) · gap 10% · délai 1.7min · rebond 68% (52/76) (MFE +1.71%)
   - −3.0% : fill 30min 23% · séance 36% (58/159) · gap 4% · délai 10.5min · rebond 73% (42/58) (MFE +1.67%)
   - −4.0% : fill 30min 11% · séance 25% (42/159) · gap 2% · délai 62.8min · rebond 62% (27/42) (MFE +1.49%)
   - −5.0% : fill 30min 5% · séance 14% (24/159) · gap 1% · délai 57.6min · rebond 49% (14/24) (MFE +0.96%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.62% (p90 −1.97%) → stop au-delà de −1.61% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.76% (p90 −2.06%) → stop au-delà de −1.6% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.56% (p90 −2.03%) → stop au-delà de −1.29% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=693 jambes) : jambe baissière méd −1.12% (p90 −2.75%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (69 séances) :
      · −1.0% : fill 100% (68/69) · rebond 63% (42/68)
      · −2.0% : fill 84% (55/69) · rebond 69% (40/55)
      · −3.0% : fill 70% (45/69) · rebond 74% (33/45)
      · −4.0% : fill 48% (32/69) · rebond 65% (23/32)
      · −5.0% : fill 26% (17/69) · rebond 48% (11/17)
   - **flat** (24 séances) :
      · −1.0% : fill 58% (16/24) · rebond 43% (10/16)
      · −2.0% : fill 32% (9/24) · rebond 59% (5/9)
      · −3.0% : fill 21% (6/24) · rebond 62% (4/6)
      · −4.0% : fill 9% (3/24) · rebond 0% (0/3)
      · −5.0% : fill 3% (2/24) · rebond 0% (0/2)
   - **gap-up** (66 séances) :
      · −1.0% : fill 38% (28/66) · rebond 72% (18/28)
      · −2.0% : fill 13% (12/66) · rebond 68% (7/12)
      · −3.0% : fill 6% (7/66) · rebond 71% (5/7)
      · −4.0% : fill 6% (7/66) · rebond 64% (4/7)
      · −5.0% : fill 4% (5/66) · rebond 65% (3/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 50% si les 15 1res min sont vertes (71 cas) · 37% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.61% .. +3.13%] · haut q95 +3.69% · bas q05 -4.02%
   - 60min (n=160) : retour [-3.29% .. +3.09%] · haut q95 +3.89% · bas q05 -4.45%
   - session (n=160) : retour [-4.08% .. +4.82%] · haut q95 +5.46% · bas q05 -6.18%


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 47.0  _(neutre)_
- **ADX** : 19.6  _(pas de tendance nette)_
- **MACD** : hist 0.083  _(pas de croisement recent)_
- **BB** : %B 0.59 · largeur 17.9%
- **ATR** : 0.99 (29.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.055  _(distribution)_
- **Vol ratio** : 1.06  _(volume normal)_
- **Choppiness** : 57.4  _(transition)_
- **MA** : MA20 17.01 · MA50 16.98 · MA200 22.62  _(prix > MA20)_
- **Dist MA** : MA20 +1.7% · MA50 +1.8% · MA200 -23.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (45776 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
