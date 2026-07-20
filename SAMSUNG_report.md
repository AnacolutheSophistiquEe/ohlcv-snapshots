# 005930

**Generated** : 2026-07-20T00:14:32.196862+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · ₩255000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)  
> ↳ spot ₩255000.00 (+7.5% vs entrée) · entrée ₩237146.66 · stop ₩227411.24 · T1 ₩256617.51 · R/R 2.0  
> ↳ P(T1 av. stop) 31 % _(réel 5 s)_ · EV/risk -0.043 _(réel 5 s)_ (GBM 0.541) · ¼-Kelly 0.022 · _first-passage empirique daily (historique réel, n≈207) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -32 % hors [0,100] (R² max 0.97). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.140 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩233252.49–₩241040.83 (mid ₩237146.66)
- Spot actuel : ₩255000.00 (+7.5% au-dessus de la zone — repli à attendre)
- Stop : ₩227411.24 (stop swing_plan-based (-10.82%))
- Targets : T1 ₩256617.51 · R/R 2.0 | T2 ₩276088.36 · R/R 4.0 | T3 ₩295559.21 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩227411.24


## Edge, scénarios & sizing

- EV/risk : 0.541 | EV/share : ₩5265.048 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 12 % | T3 2 %
- Kelly (position) : f* 0.088 | ¼-Kelly 0.022 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈207) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 9.8 | bear 63.3 | side 26.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.182% → cible +6.122% / stop −3.22%, p_fill 51%, n_eff≈17.5) : P(cible|rempli) **2%** · **EV/risk -0.099** (×p_fill ; si rempli -0.62% du capital)
  - **swing** (entrée dip −7.002% → cible +8.21% / stop −4.105%, p_fill 42%, n_eff≈13.0) : P(cible|rempli) **31%** · **EV/risk -0.043** (×p_fill ; si rempli -0.41% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=10, n_eff=9))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→68% · +2.0%→46% · +3.0%→30% · +5.0%→19% · +8.0%→5%
- Range intraday médian 5.33% (p90 9.32%) · excursion haute méd. +1.91% / basse méd. −2.45%
- Profil de vol intra : ouverture 2.691% vs midi 1.155% vs clôture 1.377% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (135 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 11% · trend ↑1%/↓1% ; spike-down 64% · recovery-V 20%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; mean-reverting — autocorr -0.087)_ ; drift intra méd. -0.784% ; recovery-V 16%
- **σ réalisé intraday** 4.361% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 76% / whipsaw 31%
- POC intraday (dernière séance, temps-au-prix) : 256612.5 (VA 253562.5–257527.5 ; dernier close 256500.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 30% · rebond 69% · **stop −6.49%** sous le fill (sous le bruit) · cible +1.52% · R/R 0.23 (high win-rate)
- Gaps overnight (n=134) : méd. 0.05% · baisse 46% (gap-down >1% 36% · >2% 25%)
- Excursion ouverture 5min (n=135) : bas méd −0.51% (p90 −1.48%) · haut méd +0.7% · range méd 1.4%
- Excursion ouverture 15min (n=135) : bas méd −0.88% (p90 −2.34%) · haut méd +1.04% · range méd 2.04%
- Excursion ouverture 30min (n=135) : bas méd −1.15% (p90 −2.74%) · haut méd +1.13% · range méd 2.47%
- Excursion ouverture 60min (n=135) : bas méd −1.46% (p90 −3.4%) · haut méd +1.36% · range méd 3.02%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 256500.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 54% · séance 66% (83/134) · gap 39% · délai 0.0min · rebond 55% (46/83) (MFE +1.51%)
   - −1.0% : fill 30min 48% · séance 63% (77/134) · gap 36% · délai 0.0min · rebond 60% (44/77) (MFE +1.33%)
   - −1.5% : fill 30min 45% · séance 58% (68/134) · gap 27% · délai 0.3min · rebond 59% (41/68) (MFE +1.65%)
   - −2.0% : fill 30min 42% · séance 51% (60/134) · gap 25% · délai 0.1min · rebond 58% (35/60) (MFE +1.78%)
   - −3.0% : fill 30min 31% · séance 46% (51/134) · gap 20% · délai 1.7min · rebond 62% (34/51) (MFE +2.08%)
   - −4.0% : fill 30min 22% · séance 38% (40/134) · gap 13% · délai 22.8min · rebond 65% (28/40) (MFE +2.13%)
   - −5.0% : fill 30min 12% · séance 30% (30/134) · gap 7% · délai 78.9min · rebond 69% (21/30) (MFE +1.52%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.31% (p90 −1.95%) → stop au-delà de −1.03% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.32% (p90 −2.65%) → stop au-delà de −1.12% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.29% (p90 −2.36%) → stop au-delà de −0.97% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=575 jambes) : jambe baissière méd −1.31% (p90 −3.09%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (58 séances) :
      · −1.0% : fill 97% (55/58) · rebond 50% (29/55)
      · −2.0% : fill 87% (47/58) · rebond 46% (24/47)
      · −3.0% : fill 84% (42/58) · rebond 56% (27/42)
      · −4.0% : fill 73% (34/58) · rebond 59% (23/34)
      · −5.0% : fill 60% (26/58) · rebond 65% (17/26)
   - **flat** (13 séances) :
      · −1.0% : fill 58% (7/13) · rebond 70% (4/7)
      · −2.0% : fill 40% (4/13) · rebond 85% (3/4)
      · −3.0% : fill 40% (4/13) · rebond 85% (3/4)
      · −4.0% : fill 18% (2/13) · rebond 100% (2/2)
      · −5.0% : fill 18% (2/13) · rebond 100% (2/2)
   - **gap-up** (63 séances) :
      · −1.0% : fill 33% (15/63) · rebond 82% (11/15)
      · −2.0% : fill 20% (9/63) · rebond 94% (8/9)
      · −3.0% : fill 10% (5/63) · rebond 89% (4/5)
      · −4.0% : fill 10% (4/63) · rebond 88% (3/4)
      · −5.0% : fill 3% (2/63) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=135) : 42% en base · 63% si les 15 1res min sont vertes (67 cas) · 20% si rouges (68 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=135) : COUDE à **1:14** → P(séance verte=clôture>ouverture) 80% si début vert vs 9% si rouge (base 42% · écart 70 pts) ; prédictivité sature ensuite (plafond brut 125min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **80%** · continue >prix actuel 54% ; creux résiduel méd -1.39% (q20 -4.38%) → **SL/trailing à −4.38%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.68% / q75 +3.78% → **scale +1.68% / runner +3.78%**, sortie à la clôture
  - **si ROUGE au coude** (n=62) : edge inversé — récupère vert seulement **9%** (continue à baisser 54%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.25%** (au-delà de la MAE q10 -7.25%), cible rebond +1.03% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=135) : retour [-2.3% .. +2.85%] · haut q95 +3.69% · bas q05 -3.1%
   - 60min (n=135) : retour [-3.06% .. +4.9%] · haut q95 +5.44% · bas q05 -3.75%
   - 2h (n=135) : retour [-4.58% .. +4.85%] · haut q95 +6.23% · bas q05 -5.13%
   - 4h (n=135) : retour [-5.34% .. +5.28%] · haut q95 +6.79% · bas q05 -7.54%
   - 6h (n=135) : retour [-6.63% .. +6.03%] · haut q95 +7.91% · bas q05 -8.25%
   - session (n=135) : retour [-6.04% .. +6.39%] · haut q95 +7.91% · bas q05 -9.05%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.71%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 32.1  _(momentum baissier)_
- **ADX** : 21.3  _(pas de tendance nette)_
- **MACD** : hist -7175.818  _(pas de croisement recent)_
- **BB** : %B 0.12 · largeur 43.7%
- **ATR** : 26500.0 (96.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.137  _(distribution)_
- **Vol ratio** : 0.82  _(volume normal)_
- **Choppiness** : 51.2  _(transition)_
- **MA** : MA20 306475.0 · MA50 306360.0 · MA200 184824.15  _(prix < MA20)_
- **Dist MA** : MA20 -16.8% · MA50 -16.8% · MA200 +38.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83276 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
