# SMR

**Generated** : 2026-07-30T00:28:41.442199+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $7.59  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $7.59 (+1.2% vs entrée) · entrée $7.50 · stop $7.30 · T1 $7.70 · R/R 1.0  
> ↳ P(T1 av. stop) 34 % _(réel 5 s)_ · EV/risk -0.114 _(réel 5 s)_ (GBM 0.081) · ¼-Kelly 0.025 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.6% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.090 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $7.45–$7.54 (mid $7.50)
- Spot actuel : $7.59 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : $7.30 (stop swing_plan-based (-5.75%))
- Targets : T1 $7.70 · R/R 1.0 | T2 $7.91 · R/R 2.05 | T3 $8.11 · R/R 3.05
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $7.30


## Edge, scénarios & sizing

- EV/risk : 0.081 | EV/share : $0.016 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 35 % | T3 35 %
- Kelly (position) : f* 0.099 | ¼-Kelly 0.025 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 64.5 | bear 25.3 | side 10.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.251% → cible +2.753% / stop −2.602%, p_fill 83%, n_eff≈32.1) : P(cible|rempli) **34%** · **EV/risk -0.114** (×p_fill ; si rempli -0.36% du capital)
  - **swing** (entrée dip −2.758% → cible +6.154% / stop −3.077%, p_fill 66%, n_eff≈28.4) : P(cible|rempli) **19%** · **EV/risk -0.260** (×p_fill ; si rempli -1.20% du capital)
  - **deep** (entrée dip −4.254% → cible +8.702% / stop −4.351%, p_fill 83%, n_eff≈30.8) : P(cible|rempli) **32%** · **EV/risk -0.020** (×p_fill ; si rempli -0.11% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→80% · +2.0%→66% · +3.0%→59% · +5.0%→40% · +8.0%→18%
- Range intraday médian 7.73% (p90 12.61%) · excursion haute méd. +3.54% / basse méd. −3.15%
- Profil de vol intra : ouverture 5.088% vs midi 1.557% vs clôture 1.794% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 17% · trend ↑0%/↓0% ; spike-down 79% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.118 ; mean-reverting — autocorr -0.042)_ ; drift intra méd. -0.084% ; recovery-V 38%
- **σ réalisé intraday** 4.831% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 70% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 8.0999 (VA 8.0845–8.3151 ; dernier close 8.21)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 53% · rebond 76% · **stop −6.0%** sous le fill (sous le bruit) · cible +2.53% · R/R 0.42 (high win-rate)
- Gaps overnight (n=159) : méd. -0.63% · baisse 59% (gap-down >1% 43% · >2% 30%)
- Excursion ouverture 5min (n=160) : bas méd −1.12% (p90 −3.22%) · haut méd +1.07% · range méd 2.68%
- Excursion ouverture 15min (n=160) : bas méd −1.46% (p90 −3.72%) · haut méd +1.41% · range méd 3.5%
- Excursion ouverture 30min (n=160) : bas méd −1.81% (p90 −4.68%) · haut méd +1.97% · range méd 4.32%
- Excursion ouverture 60min (n=160) : bas méd −2.15% (p90 −5.9%) · haut méd +2.63% · range méd 5.35%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 8.21 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 75% · séance 82% (130/159) · gap 51% · délai 0.0min · rebond 66% (80/130) (MFE +1.73%)
   - −1.0% : fill 30min 68% · séance 78% (124/159) · gap 43% · délai 0.0min · rebond 68% (82/124) (MFE +2.02%)
   - −1.5% : fill 30min 63% · séance 75% (118/159) · gap 38% · délai 0.0min · rebond 74% (87/118) (MFE +2.21%)
   - −2.0% : fill 30min 58% · séance 69% (111/159) · gap 30% · délai 0.1min · rebond 68% (81/111) (MFE +2.34%)
   - −3.0% : fill 30min 47% · séance 60% (99/159) · gap 11% · délai 2.4min · rebond 74% (80/99) (MFE +2.39%)
   - −4.0% : fill 30min 36% · séance 53% (83/159) · gap 7% · délai 9.2min · rebond 76% (64/83) (MFE +2.53%)
   - −5.0% : fill 30min 26% · séance 42% (62/159) · gap 3% · délai 19.5min · rebond 70% (45/62) (MFE +1.87%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.82% (p90 −2.71%) → stop au-delà de −2.03% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −3.19%) → stop au-delà de −2.16% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.03% (p90 −3.71%) → stop au-delà de −2.5% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1176 jambes) : jambe baissière méd −1.4% (p90 −3.21%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (84 séances) :
      · −1.0% : fill 100% (84/84) · rebond 69% (56/84)
      · −2.0% : fill 94% (80/84) · rebond 74% (61/80)
      · −3.0% : fill 84% (75/84) · rebond 76% (62/75)
      · −4.0% : fill 74% (65/84) · rebond 81% (53/65)
      · −5.0% : fill 59% (47/84) · rebond 73% (36/47)
   - **flat** (13 séances) :
      · −1.0% : fill 80% (10/13) · rebond 53% (6/10)
      · −2.0% : fill 69% (8/13) · rebond 22% (4/8)
      · −3.0% : fill 66% (6/13) · rebond 46% (3/6)
      · −4.0% : fill 66% (6/13) · rebond 56% (3/6)
      · −5.0% : fill 56% (5/13) · rebond 79% (4/5)
   - **gap-up** (62 séances) :
      · −1.0% : fill 45% (30/62) · rebond 70% (20/30)
      · −2.0% : fill 32% (23/62) · rebond 66% (16/23)
      · −3.0% : fill 25% (18/62) · rebond 80% (15/18)
      · −4.0% : fill 18% (12/62) · rebond 67% (8/12)
      · −5.0% : fill 13% (10/62) · rebond 42% (5/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 61% si les 15 1res min sont vertes (72 cas) · 33% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **40min** → P(séance verte=clôture>ouverture) 68% si début vert vs 20% si rouge (base 46% · écart 48 pts) ; prédictivité sature ensuite (plafond brut 176min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=83) : tient le vert **68%** · continue >prix actuel 44% ; creux résiduel méd -3.13% (q20 -5.01%) → **SL/trailing à −5.01%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.13% / q75 +3.93% → **scale +2.13% / runner +3.93%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **20%** (continue à baisser 52%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.77%** (au-delà de la MAE q10 -6.77%), cible rebond +2.1% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.48% .. +4.91%] · haut q95 +6.52% · bas q05 -6.02%
   - 60min (n=160) : retour [-6.44% .. +5.4%] · haut q95 +7.53% · bas q05 -7.76%
   - 2h (n=160) : retour [-7.58% .. +7.6%] · haut q95 +11.07% · bas q05 -8.45%
   - 4h (n=160) : retour [-8.1% .. +7.72%] · haut q95 +11.05% · bas q05 -10.5%
   - 6h (n=160) : retour [-7.99% .. +8.31%] · haut q95 +11.34% · bas q05 -10.53%
   - session (n=160) : retour [-7.87% .. +10.04%] · haut q95 +11.42% · bas q05 -10.72%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 4.95%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-05 — SMR earnings (J-4 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-05 — SMR earnings (J-4 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 36.3  _(momentum baissier)_
- **ADX** : 23.8  _(pas de tendance nette)_
- **MACD** : hist 0.027  _(pas de croisement recent)_
- **BB** : %B 0.12 · largeur 31.9%
- **ATR** : 0.65 (2.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.089  _(distribution)_
- **Vol ratio** : 1.1  _(volume normal)_
- **Choppiness** : 56.8  _(transition)_
- **MA** : MA20 8.63 · MA50 10.04 · MA200 16.77  _(prix < MA20)_
- **Dist MA** : MA20 -12.0% · MA50 -24.4% · MA200 -54.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (84629 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
