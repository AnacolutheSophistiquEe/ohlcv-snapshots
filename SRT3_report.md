# SRT3

**Generated** : 2026-07-17T21:37:27.765471+00:00  
**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €243.40  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)  
> ↳ spot €243.40 (+5.5% vs entrée) · entrée €230.72 · stop €227.00 · T1 €238.17 · R/R 2.0  
> ↳ P(T1 av. stop) 36 % · EV/risk 0.033 · ¼-Kelly 0.005 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €229.23–€232.21 (mid €230.72)
- Spot actuel : €243.40 (+5.5% au-dessus de la zone — repli à attendre)
- Stop : €227.00 (stop swing_plan-based (-6.74%))
- Targets : T1 €238.17 · R/R 2.0 | T2 €245.62 · R/R 4.01 | T3 €253.07 · R/R 6.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €227.00


## Edge, scénarios & sizing

- EV/risk : 0.033 | EV/share : €0.124 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 17 % | T3 7 %
- Kelly (position) : f* 0.019 | ¼-Kelly 0.005 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 29.3 | bear 7.9 | side 62.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 487.0 (= 2 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.369% → cible +2.905% / stop −2.5%, p_fill 21%, n_eff≈10.3) : P(cible|rempli) **3%** · **EV/risk -0.056** (×p_fill ; si rempli -0.67% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=8, n_eff=5))
  - **deep** : indisponible (échantillon insuffisant (n=8, n_eff=5))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→74% · +2.0%→48% · +3.0%→26% · +5.0%→10% · +8.0%→0%
- Range intraday médian 3.63% (p90 6.59%) · excursion haute méd. +1.94% / basse méd. −1.69%
- Profil de vol intra : ouverture 2.025% vs midi 0.829% vs clôture 0.975% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑1%/↓0% ; spike-down 50% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.12 ; neutre — autocorr -0.007)_ ; drift intra méd. 0.477% ; recovery-V 34%
- **σ réalisé intraday** 2.392% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 52% / whipsaw 26%
- POC intraday (dernière séance, temps-au-prix) : 246.99 (VA 246.15–247.83 ; dernier close 245.45)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 58% · rebond 68% · **stop −2.4%** sous le fill (sous le bruit) · cible +1.58% · R/R 0.66 (high win-rate)
- Gaps overnight (n=159) : méd. -0.15% · baisse 54% (gap-down >1% 19% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.36% (p90 −1.62%) · haut méd +0.48% · range méd 1.18%
- Excursion ouverture 15min (n=160) : bas méd −0.53% (p90 −1.85%) · haut méd +0.64% · range méd 1.47%
- Excursion ouverture 30min (n=160) : bas méd −0.57% (p90 −1.95%) · haut méd +0.76% · range méd 1.74%
- Excursion ouverture 60min (n=160) : bas méd −0.66% (p90 −2.23%) · haut méd +0.82% · range méd 1.86%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 245.45 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 77% (125/159) · gap 32% · délai 0.2min · rebond 52% (60/125) (MFE +1.11%)
   - −1.0% : fill 30min 45% · séance 66% (106/159) · gap 19% · délai 0.4min · rebond 60% (62/106) (MFE +1.22%)
   - −1.5% : fill 30min 34% · séance 58% (92/159) · gap 9% · délai 6.5min · rebond 68% (57/92) (MFE +1.58%)
   - −2.0% : fill 30min 22% · séance 42% (70/159) · gap 5% · délai 21.4min · rebond 60% (43/70) (MFE +1.49%)
   - −3.0% : fill 30min 5% · séance 20% (40/159) · gap 2% · délai 184.1min · rebond 54% (24/40) (MFE +1.51%)
   - −4.0% : fill 30min 3% · séance 10% (20/159) · gap 1% · délai 208.7min · rebond 67% (15/20) (MFE +1.31%)
   - −5.0% : fill 30min 1% · séance 6% (10/159) · gap 1% · délai 99.8min · rebond 74% (8/10) (MFE +2.47%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.27% (p90 −1.74%) → stop au-delà de −1.15% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.18% (p90 −1.8%) → stop au-delà de −1.03% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.25% (p90 −1.79%) → stop au-delà de −1.22% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=412 jambes) : jambe baissière méd −1.02% (p90 −2.28%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (78 séances) :
      · −1.0% : fill 85% (66/78) · rebond 70% (43/66)
      · −2.0% : fill 55% (43/78) · rebond 70% (29/43)
      · −3.0% : fill 31% (29/78) · rebond 56% (17/29)
      · −4.0% : fill 16% (16/78) · rebond 71% (12/16)
      · −5.0% : fill 8% (7/78) · rebond 92% (6/7)
   - **flat** (34 séances) :
      · −1.0% : fill 62% (20/34) · rebond 35% (9/20)
      · −2.0% : fill 48% (14/34) · rebond 37% (6/14)
      · −3.0% : fill 18% (6/34) · rebond 49% (4/6)
      · −4.0% : fill 11% (3/34) · rebond 44% (2/3)
      · −5.0% : fill 11% (3/34) · rebond 44% (2/3)
   - **gap-up** (47 séances) :
      · −1.0% : fill 41% (20/47) · rebond 52% (10/20)
      · −2.0% : fill 21% (13/47) · rebond 55% (8/13)
      · −3.0% : fill 5% (5/47) · rebond 52% (3/5)
      · −4.0% : fill 1% (1/47) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/47) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 54% en base · 62% si les 15 1res min sont vertes (89 cas) · 44% si rouges (71 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:16** → P(séance verte=clôture>ouverture) 72% si début vert vs 35% si rouge (base 54% · écart 38 pts) ; prédictivité sature ensuite (plafond brut 293min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **72%** · continue >prix actuel 47% ; creux résiduel méd -1.15% (q20 -2.31%) → **SL/trailing à −2.31%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.11% / q75 +2.66% → **scale +1.11% / runner +2.66%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **35%** (continue à baisser 55%) → **RÉDUIRE ~65%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.43%** (au-delà de la MAE q10 -3.43%), cible rebond +1.29% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.05% .. +2.15%] · haut q95 +2.69% · bas q05 -2.64%
   - 60min (n=160) : retour [-2.34% .. +2.35%] · haut q95 +2.86% · bas q05 -2.88%
   - 2h (n=160) : retour [-2.23% .. +2.74%] · haut q95 +3.15% · bas q05 -3.13%
   - 4h (n=160) : retour [-2.56% .. +2.82%] · haut q95 +3.4% · bas q05 -3.42%
   - 6h (n=160) : retour [-2.68% .. +3.58%] · haut q95 +4.39% · bas q05 -3.64%
   - session (n=160) : retour [-3.69% .. +5.0%] · haut q95 +6.3% · bas q05 -4.18%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.25%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 64.8  _(momentum haussier)_
- **ADX** : 15.4  _(pas de tendance nette)_
- **MACD** : hist 2.042  _(pas de croisement recent)_
- **BB** : %B 0.75 · largeur 19.9%
- **ATR** : 8.58 (56.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.125  _(accumulation)_
- **Vol ratio** : 0.82  _(volume normal)_
- **Choppiness** : 48.3  _(transition)_
- **MA** : MA20 231.75 · MA50 230.43 · MA200 231.59  _(prix > MA20)_
- **Dist MA** : MA20 +5.0% · MA50 +5.6% · MA200 +5.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91186 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
