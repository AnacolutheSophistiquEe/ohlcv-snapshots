# 005930

**Generated** : 2026-07-17T00:15:17.795248+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Buy  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · ₩255000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)  
> ↳ spot ₩255000.00 (+7.5% vs entrée) · entrée ₩237146.66 · stop ₩227411.24 · T1 ₩256617.51 · R/R 2.0  
> ↳ P(T1 av. stop) 37 % · EV/risk 0.537 · ¼-Kelly 0.022 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

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

Plan privilegie B (swing), composite 5/10, conviction 'Buy'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩233252.49–₩241040.83 (mid ₩237146.66)
- Spot actuel : ₩255000.00 (+7.5% au-dessus de la zone — repli à attendre)
- Stop : ₩227411.24 (stop swing_plan-based (-10.82%))
- Targets : T1 ₩256617.51 · R/R 2.0 | T2 ₩276088.36 · R/R 4.0 | T3 ₩295559.21 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩227411.24


## Edge, scénarios & sizing

- EV/risk : 0.537 | EV/share : ₩5230.592 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 12 % | T3 2 %
- Kelly (position) : f* 0.087 | ¼-Kelly 0.022 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 9.8 | bear 63.3 | side 26.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.182% → cible +6.122% / stop −3.22%, p_fill 47%, n_eff≈16.3) : P(cible|rempli) **3%** · **EV/risk -0.107** (×p_fill ; si rempli -0.74% du capital)
  - **swing** (entrée dip −7.002% → cible +8.21% / stop −4.105%, p_fill 36%, n_eff≈11.6) : P(cible|rempli) **40%** · **EV/risk +0.046** (×p_fill ; si rempli +0.52% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=9, n_eff=8))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→69% · +2.0%→48% · +3.0%→31% · +5.0%→20% · +8.0%→5%
- Range intraday médian 5.38% (p90 9.32%) · excursion haute méd. +1.96% / basse méd. −2.37%
- Profil de vol intra : ouverture 2.655% vs midi 1.121% vs clôture 1.344% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (133 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 12% · trend ↑1%/↓1% ; spike-down 62% · recovery-V 21%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; mean-reverting — autocorr -0.075)_ ; drift intra méd. -0.558% ; recovery-V 18%
- **σ réalisé intraday** 4.277% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 57% / bas 74% / whipsaw 34%
- POC intraday (dernière séance, temps-au-prix) : 279921.25 (VA 276531.25–282463.75 ; dernier close 279000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 29% · rebond 74% · **stop −6.56%** sous le fill (sous le bruit) · cible +1.69% · R/R 0.26 (high win-rate)
- Gaps overnight (n=132) : méd. 0.03% · baisse 46% (gap-down >1% 35% · >2% 24%)
- Excursion ouverture 5min (n=133) : bas méd −0.48% (p90 −1.49%) · haut méd +0.71% · range méd 1.35%
- Excursion ouverture 15min (n=133) : bas méd −0.88% (p90 −2.35%) · haut méd +1.07% · range méd 2.07%
- Excursion ouverture 30min (n=133) : bas méd −1.08% (p90 −2.76%) · haut méd +1.17% · range méd 2.41%
- Excursion ouverture 60min (n=133) : bas méd −1.29% (p90 −3.38%) · haut méd +1.37% · range méd 2.97%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 279000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 54% · séance 65% (81/132) · gap 38% · délai 0.0min · rebond 55% (45/81) (MFE +1.5%)
   - −1.0% : fill 30min 48% · séance 62% (75/132) · gap 35% · délai 0.0min · rebond 60% (43/75) (MFE +1.33%)
   - −1.5% : fill 30min 45% · séance 56% (66/132) · gap 26% · délai 0.3min · rebond 60% (40/66) (MFE +1.65%)
   - −2.0% : fill 30min 41% · séance 52% (59/132) · gap 24% · délai 0.5min · rebond 60% (35/59) (MFE +1.86%)
   - −3.0% : fill 30min 30% · séance 45% (50/132) · gap 18% · délai 2.3min · rebond 65% (34/50) (MFE +2.41%)
   - −4.0% : fill 30min 21% · séance 37% (39/132) · gap 12% · délai 25.8min · rebond 68% (28/39) (MFE +2.42%)
   - −5.0% : fill 30min 11% · séance 29% (29/132) · gap 6% · délai 83.9min · rebond 74% (21/29) (MFE +1.69%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.31% (p90 −1.95%) → stop au-delà de −1.03% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.32% (p90 −2.65%) → stop au-delà de −1.12% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.29% (p90 −2.36%) → stop au-delà de −0.97% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=557 jambes) : jambe baissière méd −1.28% (p90 −3.16%) · ~11.8 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (57 séances) :
      · −1.0% : fill 97% (54/57) · rebond 53% (29/54)
      · −2.0% : fill 87% (46/57) · rebond 48% (24/46)
      · −3.0% : fill 84% (41/57) · rebond 59% (27/41)
      · −4.0% : fill 71% (33/57) · rebond 63% (23/33)
      · −5.0% : fill 59% (25/57) · rebond 70% (17/25)
   - **flat** (13 séances) :
      · −1.0% : fill 58% (7/13) · rebond 70% (4/7)
      · −2.0% : fill 40% (4/13) · rebond 85% (3/4)
      · −3.0% : fill 40% (4/13) · rebond 85% (3/4)
      · −4.0% : fill 18% (2/13) · rebond 100% (2/2)
      · −5.0% : fill 18% (2/13) · rebond 100% (2/2)
   - **gap-up** (62 séances) :
      · −1.0% : fill 30% (14/62) · rebond 79% (10/14)
      · −2.0% : fill 21% (9/62) · rebond 94% (8/9)
      · −3.0% : fill 11% (5/62) · rebond 89% (4/5)
      · −4.0% : fill 10% (4/62) · rebond 88% (3/4)
      · −5.0% : fill 3% (2/62) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=133) : 43% en base · 63% si les 15 1res min sont vertes (67 cas) · 22% si rouges (66 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=133) : COUDE à **1:14** → P(séance verte=clôture>ouverture) 80% si début vert vs 10% si rouge (base 43% · écart 70 pts) ; prédictivité sature ensuite (plafond brut 125min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **80%** · continue >prix actuel 54% ; creux résiduel méd -1.39% (q20 -4.38%) → **SL/trailing à −4.38%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.68% / q75 +3.78% → **scale +1.68% / runner +3.78%**, sortie à la clôture
  - **si ROUGE au coude** (n=60) : edge inversé — récupère vert seulement **10%** (continue à baisser 58%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.26%** (au-delà de la MAE q10 -7.26%), cible rebond +0.94% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=133) : retour [-2.37% .. +2.86%] · haut q95 +3.69% · bas q05 -3.1%
   - 60min (n=133) : retour [-2.68% .. +4.9%] · haut q95 +5.47% · bas q05 -3.79%
   - 2h (n=133) : retour [-4.68% .. +4.85%] · haut q95 +6.25% · bas q05 -5.13%
   - 4h (n=133) : retour [-5.35% .. +5.47%] · haut q95 +6.85% · bas q05 -7.65%
   - 6h (n=133) : retour [-6.73% .. +6.28%] · haut q95 +7.99% · bas q05 -8.25%
   - session (n=133) : retour [-6.19% .. +6.9%] · haut q95 +7.99% · bas q05 -9.14%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.8% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.68%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 32.1  _(momentum baissier)_
- **ADX** : 21.3  _(pas de tendance nette)_
- **MACD** : hist -7175.818  _(pas de croisement recent)_
- **BB** : %B 0.12 · largeur 43.7%
- **ATR** : 26500.0 (97.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.137  _(distribution)_
- **Vol ratio** : 0.82  _(volume normal)_
- **Choppiness** : 51.2  _(transition)_
- **MA** : MA20 306475.0 · MA50 306360.0 · MA200 184824.15  _(prix < MA20)_
- **Dist MA** : MA20 -16.8% · MA50 -16.8% · MA200 +38.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83089 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
