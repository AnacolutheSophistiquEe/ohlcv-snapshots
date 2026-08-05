# SRT3

**Generated** : 2026-08-05T21:37:30.101536+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · €228.90  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €228.90 (+0.7% vs entrée) · entrée €227.28 · stop €223.62 · T1 €231.38 · R/R 1.12  
> ↳ P(T1 av. stop) 33 % _(réel 5 s)_ · EV/risk -0.084 _(réel 5 s)_ (GBM 0.061) · ¼-Kelly 0.013 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.61% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.050 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €226.45–€228.10 (mid €227.28)
- Spot actuel : €228.90 (+0.7% au-dessus de la zone — repli à attendre)
- Stop : €223.62 (stop swing_plan-based (-6.88%))
- Targets : T1 €231.38 · R/R 1.12 | T2 €235.49 · R/R 2.24 | T3 €239.59 · R/R 3.36
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €223.62


## Edge, scénarios & sizing

- EV/risk : 0.061 | EV/share : €0.223 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 48 % | T2 18 % | T3 9 %
- Kelly (position) : f* 0.053 | ¼-Kelly 0.013 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.2 | bear 78.8 | side 8.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.714% → cible +1.807% / stop −1.608%, p_fill 77%, n_eff≈30.4) : P(cible|rempli) **33%** · **EV/risk -0.084** (×p_fill ; si rempli -0.17% du capital)
  - **swing** (entrée dip −1.559% → cible +4.04% / stop −5.405%, p_fill 71%, n_eff≈26.9) : P(cible|rempli) **54%** · **EV/risk +0.058** (×p_fill ; si rempli +0.44% du capital)
  - **deep** (entrée dip −2.409% → cible +5.714% / stop −8.178%, p_fill 60%, n_eff≈23.0) : P(cible|rempli) **31%** · **EV/risk -0.185** (×p_fill ; si rempli -2.52% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→76% · +2.0%→49% · +3.0%→28% · +5.0%→10% · +8.0%→0%
- Range intraday médian 3.63% (p90 7.16%) · excursion haute méd. +1.96% / basse méd. −1.55%
- Profil de vol intra : ouverture 2.145% vs midi 0.918% vs clôture 1.039% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 10% · trend ↑0%/↓0% ; spike-down 53% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.113 ; neutre — autocorr -0.003)_ ; drift intra méd. -0.057% ; recovery-V 29%
- **σ réalisé intraday** 2.843% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 72% / bas 70% / whipsaw 45%
- POC intraday (dernière séance, temps-au-prix) : 220.5712 (VA 219.7387–225.5662 ; dernier close 227.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 60% · rebond 72% · **stop −2.49%** sous le fill (sous le bruit) · cible +1.79% · R/R 0.72 (high win-rate)
- Gaps overnight (n=159) : méd. 0.03% · baisse 50% (gap-down >1% 15% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.43% (p90 −2.26%) · haut méd +0.5% · range méd 1.24%
- Excursion ouverture 15min (n=160) : bas méd −0.58% (p90 −2.25%) · haut méd +0.65% · range méd 1.56%
- Excursion ouverture 30min (n=160) : bas méd −0.61% (p90 −2.76%) · haut méd +0.77% · range méd 1.75%
- Excursion ouverture 60min (n=160) : bas méd −0.73% (p90 −2.81%) · haut méd +0.82% · range méd 1.89%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 227.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 80% (126/159) · gap 29% · délai 0.2min · rebond 57% (65/126) (MFE +1.2%)
   - −1.0% : fill 30min 46% · séance 67% (106/159) · gap 15% · délai 0.6min · rebond 61% (63/106) (MFE +1.37%)
   - −1.5% : fill 30min 37% · séance 60% (93/159) · gap 7% · délai 4.4min · rebond 72% (60/93) (MFE +1.79%)
   - −2.0% : fill 30min 23% · séance 42% (72/159) · gap 4% · délai 17.5min · rebond 63% (44/72) (MFE +1.96%)
   - −3.0% : fill 30min 7% · séance 20% (40/159) · gap 1% · délai 138.5min · rebond 57% (23/40) (MFE +1.67%)
   - −4.0% : fill 30min 4% · séance 11% (21/159) · gap 1% · délai 49.4min · rebond 76% (16/21) (MFE +2.62%)
   - −5.0% : fill 30min 1% · séance 8% (12/159) · gap 1% · délai 94.0min · rebond 65% (9/12) (MFE +2.48%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.51% (p90 −2.34%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.4% (p90 −2.43%) → stop au-delà de −1.45% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.65% (p90 −2.8%) → stop au-delà de −1.9% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=428 jambes) : jambe baissière méd −1.04% (p90 −2.67%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (74 séances) :
      · −1.0% : fill 86% (62/74) · rebond 68% (41/62)
      · −2.0% : fill 54% (42/74) · rebond 64% (27/42)
      · −3.0% : fill 32% (28/74) · rebond 48% (15/28)
      · −4.0% : fill 15% (15/74) · rebond 71% (11/15)
      · −5.0% : fill 8% (7/74) · rebond 92% (6/7)
   - **flat** (33 séances) :
      · −1.0% : fill 59% (19/33) · rebond 50% (9/19)
      · −2.0% : fill 49% (15/33) · rebond 55% (7/15)
      · −3.0% : fill 20% (6/33) · rebond 66% (4/6)
      · −4.0% : fill 15% (4/33) · rebond 70% (3/4)
      · −5.0% : fill 15% (4/33) · rebond 24% (2/4)
   - **gap-up** (52 séances) :
      · −1.0% : fill 52% (25/52) · rebond 55% (13/25)
      · −2.0% : fill 24% (15/52) · rebond 72% (10/15)
      · −3.0% : fill 8% (6/52) · rebond 78% (4/6)
      · −4.0% : fill 5% (2/52) · rebond 100% (2/2)
      · −5.0% : fill 4% (1/52) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 56% si les 15 1res min sont vertes (91 cas) · 42% si rouges (69 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **3:25** → P(séance verte=clôture>ouverture) 71% si début vert vs 25% si rouge (base 50% · écart 46 pts) ; prédictivité sature ensuite (plafond brut 293min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=83) : tient le vert **71%** · continue >prix actuel 49% ; creux résiduel méd -0.98% (q20 -1.96%) → **SL/trailing à −1.96%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.11% / q75 +2.3% → **scale +1.11% / runner +2.3%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **25%** (continue à baisser 57%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.35%** (au-delà de la MAE q10 -3.35%), cible rebond +1.3% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.08% .. +2.1%] · haut q95 +2.66% · bas q05 -3.57%
   - 60min (n=160) : retour [-3.31% .. +2.31%] · haut q95 +2.7% · bas q05 -3.86%
   - 2h (n=160) : retour [-2.25% .. +2.59%] · haut q95 +3.04% · bas q05 -4.16%
   - 4h (n=160) : retour [-2.69% .. +2.52%] · haut q95 +3.33% · bas q05 -5.34%
   - 6h (n=160) : retour [-2.72% .. +3.36%] · haut q95 +3.86% · bas q05 -7.2%
   - session (n=160) : retour [-3.76% .. +4.39%] · haut q95 +5.85% · bas q05 -7.2%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.27%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 35.5  _(momentum baissier)_
- **ADX** : 19.1  _(pas de tendance nette)_
- **MACD** : hist -0.317  _(pas de croisement recent)_
- **BB** : %B 0.46 · largeur 20.4%
- **ATR** : 12.18 (98.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.047  _(neutre)_
- **Vol ratio** : 0.42  _(volume atone)_
- **Choppiness** : 51.9  _(transition)_
- **MA** : MA20 230.89 · MA50 230.99 · MA200 231.94  _(prix < MA20)_
- **Dist MA** : MA20 -0.9% · MA50 -0.9% · MA200 -1.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91041 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
