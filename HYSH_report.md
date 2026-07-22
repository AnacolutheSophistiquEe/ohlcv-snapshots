# 298040

**Generated** : 2026-07-22T00:16:35.239142+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩2578000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot ₩2578000.00 (+1.4% vs entrée) · entrée ₩2542550.10 · stop ₩2456171.53 · T1 ₩2671000.00 · R/R 1.49  
> ↳ P(T1 av. stop) 6 % _(réel 5 s)_ · EV/risk -0.26 _(réel 5 s)_ (GBM -0.151) · ¼-Kelly 0.003 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.4% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -60 % hors [0,100] (R² max 0.98). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.220 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩2526114.48–₩2558985.73 (mid ₩2542550.10)
- Spot actuel : ₩2578000.00 (+1.4% au-dessus de la zone — repli à attendre)
- Stop : ₩2456171.53 (stop swing_plan-based (-13.51%))
- Targets : T1 ₩2671000.00 · R/R 1.49 | T2 ₩2729668.74 · R/R 2.17 | T3 ₩2788337.47 · R/R 2.85
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2456171.53


## Edge, scénarios & sizing

- EV/risk : -0.151 | EV/share : ₩-13028.064 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 22 % | T2 22 % | T3 22 %
- Kelly (position) : f* 0.012 | ¼-Kelly 0.003 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 9.1 | bear 76.1 | side 14.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.38% → cible +5.052% / stop −3.397%, p_fill 90%, n_eff≈35.3) : P(cible|rempli) **6%** · **EV/risk -0.260** (×p_fill ; si rempli -0.97% du capital)
  - **swing** (entrée dip −3.031% → cible +21.613% / stop −10.807%, p_fill 85%, n_eff≈31.8) : P(cible|rempli) **5%** · **EV/risk -0.309** (×p_fill ; si rempli -3.95% du capital)
  - **deep** (entrée dip −4.673% → cible +10.19% / stop −5.095%, p_fill 83%, n_eff≈30.6) : P(cible|rempli) **29%** · **EV/risk -0.132** (×p_fill ; si rempli -0.82% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→64% · +2.0%→52% · +3.0%→38% · +5.0%→22% · +8.0%→6%
- Range intraday médian 6.88% (p90 9.73%) · excursion haute méd. +2.14% / basse méd. −3.74%
- Profil de vol intra : ouverture 4.177% vs midi 1.054% vs clôture 1.144% _(ouverture ~4.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (136 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 22% · trend ↑0%/↓1% ; spike-down 79% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; mean-reverting — autocorr -0.093)_ ; drift intra méd. -1.763% ; recovery-V 28%
- **σ réalisé intraday** 5.319% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 41% / bas 72% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 2542037.5 (VA 2513387.5–2575462.5 ; dernier close 2543000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 35% · rebond 92% · **stop −5.21%** sous le fill (sous le bruit) · cible +2.57% · R/R 0.49 (high win-rate)
- Gaps overnight (n=135) : méd. 0.6% · baisse 39% (gap-down >1% 25% · >2% 18%)
- Excursion ouverture 5min (n=136) : bas méd −1.29% (p90 −3.46%) · haut méd +0.81% · range méd 2.68%
- Excursion ouverture 15min (n=136) : bas méd −1.93% (p90 −4.79%) · haut méd +1.06% · range méd 3.65%
- Excursion ouverture 30min (n=136) : bas méd −2.4% (p90 −4.92%) · haut méd +1.11% · range méd 4.12%
- Excursion ouverture 60min (n=136) : bas méd −2.54% (p90 −5.31%) · haut méd +1.35% · range méd 4.72%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2543000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 72% (93/135) · gap 33% · délai 0.1min · rebond 59% (57/93) (MFE +1.31%)
   - −1.0% : fill 30min 56% · séance 68% (85/135) · gap 25% · délai 0.6min · rebond 58% (52/85) (MFE +1.52%)
   - −1.5% : fill 30min 48% · séance 60% (76/135) · gap 22% · délai 1.2min · rebond 52% (46/76) (MFE +1.29%)
   - −2.0% : fill 30min 43% · séance 57% (67/135) · gap 18% · délai 2.6min · rebond 51% (36/67) (MFE +1.1%)
   - −3.0% : fill 30min 32% · séance 46% (54/135) · gap 8% · délai 2.9min · rebond 54% (30/54) (MFE +1.03%)
   - −4.0% : fill 30min 22% · séance 42% (46/135) · gap 5% · délai 26.0min · rebond 75% (35/46) (MFE +1.89%)
   - −5.0% : fill 30min 19% · séance 35% (35/135) · gap 4% · délai 22.9min · rebond 92% (30/35) (MFE +2.57%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.72% (p90 −3.32%) → stop au-delà de −2.29% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.76% (p90 −3.53%) → stop au-delà de −2.46% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.81% (p90 −3.44%) → stop au-delà de −2.05% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=720 jambes) : jambe baissière méd −1.44% (p90 −3.43%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (47 séances) :
      · −1.0% : fill 100% (47/47) · rebond 57% (29/47)
      · −2.0% : fill 87% (39/47) · rebond 51% (21/39)
      · −3.0% : fill 82% (37/47) · rebond 52% (20/37)
      · −4.0% : fill 78% (32/47) · rebond 78% (24/32)
      · −5.0% : fill 70% (27/47) · rebond 90% (22/27)
   - **flat** (15 séances) :
      · −1.0% : fill 82% (10/15) · rebond 57% (7/10)
      · −2.0% : fill 72% (7/15) · rebond 73% (5/7)
      · −3.0% : fill 43% (4/15) · rebond 100% (4/4)
      · −4.0% : fill 43% (4/15) · rebond 63% (3/4)
      · −5.0% : fill 31% (2/15) · rebond 100% (2/2)
   - **gap-up** (73 séances) :
      · −1.0% : fill 45% (28/73) · rebond 59% (16/28)
      · −2.0% : fill 34% (21/73) · rebond 42% (10/21)
      · −3.0% : fill 23% (13/73) · rebond 43% (6/13)
      · −4.0% : fill 17% (10/73) · rebond 71% (8/10)
      · −5.0% : fill 12% (6/73) · rebond 100% (6/6)
- **P(clôture VERTE) selon le drive 15min** (n=136) : 38% en base · 62% si les 15 1res min sont vertes (55 cas) · 26% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=136) : COUDE à **1:21** → P(séance verte=clôture>ouverture) 81% si début vert vs 11% si rouge (base 38% · écart 69 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=61) : tient le vert **81%** · continue >prix actuel 52% ; creux résiduel méd -1.5% (q20 -3.91%) → **SL/trailing à −3.91%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.55% / q75 +2.9% → **scale +1.55% / runner +2.9%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **11%** (continue à baisser 61%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.04%** (au-delà de la MAE q10 -5.04%), cible rebond +1.32% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=136) : retour [-4.41% .. +4.29%] · haut q95 +6.12% · bas q05 -5.24%
   - 60min (n=136) : retour [-5.28% .. +4.9%] · haut q95 +6.6% · bas q05 -5.95%
   - 2h (n=136) : retour [-7.32% .. +4.53%] · haut q95 +7.18% · bas q05 -8.19%
   - 4h (n=136) : retour [-7.71% .. +5.36%] · haut q95 +8.01% · bas q05 -9.56%
   - 6h (n=136) : retour [-7.54% .. +5.15%] · haut q95 +8.42% · bas q05 -9.36%
   - session (n=136) : retour [-6.67% .. +5.4%] · haut q95 +8.42% · bas q05 -9.62%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 5.1% des séances seulement sont des jours de hausse propre — 298040 = **volatil sans tendance propre (choppy)** (vol intra méd 3.87%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 31.9  _(momentum baissier)_
- **ADX** : 15.0  _(pas de tendance nette)_
- **MACD** : hist -41154.406  _(pas de croisement recent)_
- **BB** : %B 0.17 · largeur 47.1%
- **ATR** : 287928.57 (87.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.221  _(distribution)_
- **Vol ratio** : 0.79  _(volume normal)_
- **Choppiness** : 38.7  _(transition)_
- **MA** : MA20 3052800.0 · MA50 3468900.0 · MA200 2600938.09  _(prix < MA20)_
- **Dist MA** : MA20 -15.6% · MA50 -25.7% · MA200 -0.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (84814 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
