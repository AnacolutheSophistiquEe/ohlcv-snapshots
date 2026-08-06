# SRT3

**Generated** : 2026-08-06T21:37:32.701326+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · €229.50  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €229.50 (+0.8% vs entrée) · entrée €227.73 · stop €224.05 · T1 €231.55 · R/R 1.04  
> ↳ P(T1 av. stop) 42 % _(réel 5 s)_ · EV/risk -0.05 _(réel 5 s)_ (GBM 0.021) · ¼-Kelly 0.012 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.61% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.030 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €226.96–€228.49 (mid €227.73)
- Spot actuel : €229.50 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : €224.05 (stop swing_plan-based (-7.03%))
- Targets : T1 €231.55 · R/R 1.04 | T2 €235.37 · R/R 2.08 | T3 €239.19 · R/R 3.11
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €224.05


## Edge, scénarios & sizing

- EV/risk : 0.021 | EV/share : €0.078 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 49 % | T2 20 % | T3 8 %
- Kelly (position) : f* 0.047 | ¼-Kelly 0.012 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.2 | bear 78.8 | side 8.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.771% → cible +1.678% / stop −1.612%, p_fill 72%, n_eff≈28.3) : P(cible|rempli) **42%** · **EV/risk -0.050** (×p_fill ; si rempli -0.11% du capital)
  - **swing** (entrée dip −1.698% → cible +3.752% / stop −5.424%, p_fill 68%, n_eff≈26.4) : P(cible|rempli) **60%** · **EV/risk +0.077** (×p_fill ; si rempli +0.61% du capital)
  - **deep** (entrée dip −2.633% → cible +5.307% / stop −8.213%, p_fill 63%, n_eff≈23.2) : P(cible|rempli) **38%** · **EV/risk -0.090** (×p_fill ; si rempli -1.17% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→76% · +2.0%→48% · +3.0%→26% · +5.0%→9% · +8.0%→0%
- Range intraday médian 3.63% (p90 7.16%) · excursion haute méd. +1.94% / basse méd. −1.69%
- Profil de vol intra : ouverture 2.12% vs midi 0.937% vs clôture 1.032% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 10% · trend ↑0%/↓0% ; spike-down 53% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.109 ; neutre — autocorr -0.01)_ ; drift intra méd. -0.062% ; recovery-V 27%
- **σ réalisé intraday** 2.778% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 72% / whipsaw 45%
- POC intraday (dernière séance, temps-au-prix) : 224.5325 (VA 223.5925–226.6475 ; dernier close 227.2)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 59% · rebond 73% · **stop −2.45%** sous le fill (sous le bruit) · cible +1.68% · R/R 0.69 (high win-rate)
- Gaps overnight (n=159) : méd. 0.04% · baisse 49% (gap-down >1% 15% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.39% (p90 −2.06%) · haut méd +0.54% · range méd 1.24%
- Excursion ouverture 15min (n=160) : bas méd −0.54% (p90 −2.11%) · haut méd +0.65% · range méd 1.5%
- Excursion ouverture 30min (n=160) : bas méd −0.59% (p90 −2.62%) · haut méd +0.8% · range méd 1.74%
- Excursion ouverture 60min (n=160) : bas méd −0.7% (p90 −2.81%) · haut méd +0.82% · range méd 1.86%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 227.2 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 80% (126/159) · gap 28% · délai 0.3min · rebond 57% (66/126) (MFE +1.2%)
   - −1.0% : fill 30min 44% · séance 68% (106/159) · gap 15% · délai 2.1min · rebond 60% (62/106) (MFE +1.36%)
   - −1.5% : fill 30min 36% · séance 59% (94/159) · gap 7% · délai 4.7min · rebond 73% (61/94) (MFE +1.68%)
   - −2.0% : fill 30min 22% · séance 42% (73/159) · gap 4% · délai 24.1min · rebond 65% (45/73) (MFE +1.67%)
   - −3.0% : fill 30min 7% · séance 20% (40/159) · gap 1% · délai 138.5min · rebond 57% (23/40) (MFE +1.67%)
   - −4.0% : fill 30min 4% · séance 11% (21/159) · gap 1% · délai 49.4min · rebond 76% (16/21) (MFE +2.62%)
   - −5.0% : fill 30min 1% · séance 8% (12/159) · gap 1% · délai 94.0min · rebond 65% (9/12) (MFE +2.48%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.51% (p90 −2.28%) → stop au-delà de −1.26% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.4% (p90 −2.43%) → stop au-delà de −1.45% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.65% (p90 −2.8%) → stop au-delà de −1.9% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=427 jambes) : jambe baissière méd −1.04% (p90 −2.61%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (72 séances) :
      · −1.0% : fill 86% (60/72) · rebond 68% (39/60)
      · −2.0% : fill 55% (42/72) · rebond 64% (27/42)
      · −3.0% : fill 32% (28/72) · rebond 48% (15/28)
      · −4.0% : fill 15% (15/72) · rebond 71% (11/15)
      · −5.0% : fill 8% (7/72) · rebond 92% (6/7)
   - **flat** (34 séances) :
      · −1.0% : fill 62% (20/34) · rebond 56% (10/20)
      · −2.0% : fill 46% (15/34) · rebond 55% (7/15)
      · −3.0% : fill 18% (6/34) · rebond 66% (4/6)
      · −4.0% : fill 14% (4/34) · rebond 70% (3/4)
      · −5.0% : fill 14% (4/34) · rebond 24% (2/4)
   - **gap-up** (53 séances) :
      · −1.0% : fill 55% (26/53) · rebond 50% (13/26)
      · −2.0% : fill 28% (16/53) · rebond 77% (11/16)
      · −3.0% : fill 8% (6/53) · rebond 78% (4/6)
      · −4.0% : fill 5% (2/53) · rebond 100% (2/2)
      · −5.0% : fill 4% (1/53) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 58% si les 15 1res min sont vertes (90 cas) · 40% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **3:25** → P(séance verte=clôture>ouverture) 72% si début vert vs 24% si rouge (base 50% · écart 48 pts) ; prédictivité sature ensuite (plafond brut 293min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **72%** · continue >prix actuel 50% ; creux résiduel méd -1.06% (q20 -1.96%) → **SL/trailing à −1.96%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.06% / q75 +2.26% → **scale +1.06% / runner +2.26%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **24%** (continue à baisser 55%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.35%** (au-delà de la MAE q10 -3.35%), cible rebond +1.39% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.05% .. +2.08%] · haut q95 +2.65% · bas q05 -3.56%
   - 60min (n=160) : retour [-3.21% .. +2.31%] · haut q95 +2.69% · bas q05 -3.85%
   - 2h (n=160) : retour [-2.25% .. +2.57%] · haut q95 +3.01% · bas q05 -3.98%
   - 4h (n=160) : retour [-2.64% .. +2.43%] · haut q95 +3.33% · bas q05 -4.8%
   - 6h (n=160) : retour [-2.69% .. +3.25%] · haut q95 +3.83% · bas q05 -6.4%
   - session (n=160) : retour [-3.74% .. +4.27%] · haut q95 +5.78% · bas q05 -6.4%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.28%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 36.3  _(momentum baissier)_
- **ADX** : 18.8  _(pas de tendance nette)_
- **MACD** : hist 0.032  _(bullish_recent)_
- **BB** : %B 0.46 · largeur 19.9%
- **ATR** : 12.24 (98.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.027  _(neutre)_
- **Vol ratio** : 0.54  _(volume atone)_
- **Choppiness** : 52.1  _(transition)_
- **MA** : MA20 231.35 · MA50 230.87 · MA200 231.95  _(prix < MA20)_
- **Dist MA** : MA20 -0.8% · MA50 -0.6% · MA200 -1.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90212 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
