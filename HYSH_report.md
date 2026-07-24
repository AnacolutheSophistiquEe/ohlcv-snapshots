# 298040

**Generated** : 2026-07-24T00:15:12.480215+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩2866000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩2866000.00 (+1.7% vs entrée) · entrée ₩2817250.00 · stop ₩2705700.58 · T1 ₩3040348.84 · R/R 2.0  
> ↳ P(T1 av. stop) 3 % _(réel 5 s)_ · EV/risk -0.113 _(réel 5 s)_ (GBM -0.198) · ¼-Kelly 0.002 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.96% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.130 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩2798553.14–₩2835946.86 (mid ₩2817250.00)
- Spot actuel : ₩2866000.00 (+1.7% au-dessus de la zone — repli à attendre)
- Stop : ₩2705700.58 (stop swing_plan-based (-7.3%))
- Targets : T1 ₩3040348.84 · R/R 2.0 | T2 ₩3068600.95 · R/R 2.25 | T3 ₩3096853.07 · R/R 2.51
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2705700.58


## Edge, scénarios & sizing

- EV/risk : -0.198 | EV/share : ₩-22043.443 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 21 % | T2 21 % | T3 21 %
- Kelly (position) : f* 0.01 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 9.7 | bear 75.8 | side 14.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.698% → cible +7.919% / stop −3.96%, p_fill 86%, n_eff≈35.1) : P(cible|rempli) **3%** · **EV/risk -0.113** (×p_fill ; si rempli -0.52% du capital)
  - **swing** (entrée dip −3.74% → cible +7.397% / stop −3.699%, p_fill 75%, n_eff≈28.7) : P(cible|rempli) **41%** · **EV/risk +0.109** (×p_fill ; si rempli +0.54% du capital)
  - **deep** (entrée dip −5.782% → cible +10.462% / stop −5.231%, p_fill 76%, n_eff≈28.3) : P(cible|rempli) **29%** · **EV/risk -0.134** (×p_fill ; si rempli -0.92% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→64% · +2.0%→52% · +3.0%→39% · +5.0%→21% · +8.0%→6%
- Range intraday médian 6.88% (p90 9.73%) · excursion haute méd. +2.14% / basse méd. −3.88%
- Profil de vol intra : ouverture 4.246% vs midi 1.043% vs clôture 1.15% _(ouverture ~4.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (138 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 21% · trend ↑0%/↓1% ; spike-down 78% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; mean-reverting — autocorr -0.105)_ ; drift intra méd. -1.578% ; recovery-V 32%
- **σ réalisé intraday** 5.291% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 66% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 2768750.0 (VA 2747750.0–2796750.0 ; dernier close 2676000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 33% · rebond 92% · **stop −5.21%** sous le fill (sous le bruit) · cible +2.57% · R/R 0.49 (high win-rate)
- Gaps overnight (n=137) : méd. 0.6% · baisse 39% (gap-down >1% 24% · >2% 17%)
- Excursion ouverture 5min (n=138) : bas méd −1.28% (p90 −3.44%) · haut méd +0.84% · range méd 2.71%
- Excursion ouverture 15min (n=138) : bas méd −1.93% (p90 −4.74%) · haut méd +1.12% · range méd 3.77%
- Excursion ouverture 30min (n=138) : bas méd −2.4% (p90 −4.91%) · haut méd +1.15% · range méd 4.14%
- Excursion ouverture 60min (n=138) : bas méd −2.54% (p90 −5.3%) · haut méd +1.43% · range méd 4.72%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2676000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 71% (94/137) · gap 33% · délai 0.0min · rebond 60% (58/94) (MFE +1.39%)
   - −1.0% : fill 30min 56% · séance 68% (86/137) · gap 24% · délai 0.9min · rebond 59% (53/86) (MFE +1.56%)
   - −1.5% : fill 30min 48% · séance 60% (77/137) · gap 21% · délai 1.3min · rebond 54% (47/77) (MFE +1.44%)
   - −2.0% : fill 30min 43% · séance 57% (68/137) · gap 17% · délai 3.2min · rebond 52% (37/68) (MFE +1.33%)
   - −3.0% : fill 30min 32% · séance 46% (55/137) · gap 7% · délai 5.4min · rebond 56% (31/55) (MFE +1.27%)
   - −4.0% : fill 30min 23% · séance 42% (47/137) · gap 5% · délai 23.9min · rebond 76% (36/47) (MFE +1.91%)
   - −5.0% : fill 30min 18% · séance 33% (35/137) · gap 4% · délai 22.9min · rebond 92% (30/35) (MFE +2.57%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.71% (p90 −3.23%) → stop au-delà de −2.17% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.76% (p90 −4.19%) → stop au-delà de −2.49% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.81% (p90 −4.2%) → stop au-delà de −2.18% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=733 jambes) : jambe baissière méd −1.43% (p90 −3.42%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (48 séances) :
      · −1.0% : fill 100% (48/48) · rebond 60% (30/48)
      · −2.0% : fill 87% (40/48) · rebond 54% (22/40)
      · −3.0% : fill 83% (38/48) · rebond 55% (21/38)
      · −4.0% : fill 79% (33/48) · rebond 80% (25/33)
      · −5.0% : fill 66% (27/48) · rebond 90% (22/27)
   - **flat** (15 séances) :
      · −1.0% : fill 82% (10/15) · rebond 57% (7/10)
      · −2.0% : fill 72% (7/15) · rebond 73% (5/7)
      · −3.0% : fill 43% (4/15) · rebond 100% (4/4)
      · −4.0% : fill 43% (4/15) · rebond 63% (3/4)
      · −5.0% : fill 31% (2/15) · rebond 100% (2/2)
   - **gap-up** (74 séances) :
      · −1.0% : fill 43% (28/74) · rebond 59% (16/28)
      · −2.0% : fill 33% (21/74) · rebond 42% (10/21)
      · −3.0% : fill 22% (13/74) · rebond 43% (6/13)
      · −4.0% : fill 17% (10/74) · rebond 71% (8/10)
      · −5.0% : fill 11% (6/74) · rebond 100% (6/6)
- **P(clôture VERTE) selon le drive 15min** (n=138) : 38% en base · 58% si les 15 1res min sont vertes (56 cas) · 28% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=138) : COUDE à **1:21** → P(séance verte=clôture>ouverture) 77% si début vert vs 14% si rouge (base 38% · écart 63 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=62) : tient le vert **77%** · continue >prix actuel 50% ; creux résiduel méd -1.52% (q20 -3.58%) → **SL/trailing à −3.58%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.63% / q75 +2.79% → **scale +1.63% / runner +2.79%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **14%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.98%** (au-delà de la MAE q10 -4.98%), cible rebond +1.35% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=138) : retour [-4.41% .. +4.27%] · haut q95 +6.12% · bas q05 -5.24%
   - 60min (n=138) : retour [-5.25% .. +4.86%] · haut q95 +6.49% · bas q05 -5.81%
   - 2h (n=138) : retour [-7.2% .. +4.52%] · haut q95 +7.08% · bas q05 -8.15%
   - 4h (n=138) : retour [-7.48% .. +5.33%] · haut q95 +7.85% · bas q05 -9.43%
   - 6h (n=138) : retour [-7.51% .. +5.07%] · haut q95 +8.38% · bas q05 -9.34%
   - session (n=138) : retour [-6.67% .. +5.35%] · haut q95 +8.38% · bas q05 -9.51%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 5.1% des séances seulement sont des jours de hausse propre — 298040 = **volatil sans tendance propre (choppy)** (vol intra méd 3.89%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 36.5  _(momentum baissier)_
- **ADX** : 14.1  _(pas de tendance nette)_
- **MACD** : hist -5391.253  _(pas de croisement recent)_
- **BB** : %B 0.41 · largeur 44.9%
- **ATR** : 262928.57 (79.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.134  _(distribution)_
- **Vol ratio** : 0.62  _(volume normal)_
- **Choppiness** : 46.6  _(transition)_
- **MA** : MA20 2981600.0 · MA50 3405180.0 · MA200 2614697.96  _(prix < MA20)_
- **Dist MA** : MA20 -3.9% · MA50 -15.8% · MA200 +9.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (84179 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
