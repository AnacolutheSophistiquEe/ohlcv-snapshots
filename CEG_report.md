# CEG

**Generated** : 2026-08-17T00:28:29.454384+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $282.50  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $282.50 (+1.6% vs entrée) · entrée $277.92 · stop $273.75 · T1 $281.36 · R/R 0.82  
> ↳ P(T1 av. stop) 37 % _(réel 5 s)_ · EV/risk -0.045 _(réel 5 s)_ (GBM -0.019) · ¼-Kelly 0.011 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -219 % hors [0,100] (R² max 0.86). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.220 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $277.23–$278.61 (mid $277.92)
- Spot actuel : $282.50 (+1.6% au-dessus de la zone — repli à attendre)
- Stop : $273.75 (stop swing_plan-based (-7.28%))
- Targets : T1 $281.36 · R/R 0.82 | T2 $284.81 · R/R 1.65 | T3 $288.25 · R/R 2.48
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $273.75


## Edge, scénarios & sizing

- EV/risk : -0.019 | EV/share : $-0.077 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 56 % | T2 25 % | T3 7 %
- Kelly (position) : f* 0.046 | ¼-Kelly 0.011 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 84.7 | bear 7.2 | side 8.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 282.0 (= 1 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.624% → cible +1.239% / stop −1.5%, p_fill 42%, n_eff≈18.2) : P(cible|rempli) **37%** · **EV/risk -0.045** (×p_fill ; si rempli -0.16% du capital)
  - **swing** (entrée dip −3.57% → cible +2.771% / stop −3.847%, p_fill 27%, n_eff≈12.1) : P(cible|rempli) **62%** · **EV/risk +0.032** (×p_fill ; si rempli +0.46% du capital)
  - **deep** (entrée dip −5.516% → cible +3.919% / stop −5.889%, p_fill 25%, n_eff≈12.9) : P(cible|rempli) **60%** · **EV/risk -0.007** (×p_fill ; si rempli -0.18% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→66% · +2.0%→38% · +3.0%→18% · +5.0%→4% · +8.0%→0%
- Range intraday médian 3.38% (p90 5.5%) · excursion haute méd. +1.44% / basse méd. −1.43%
- Profil de vol intra : ouverture 2.517% vs midi 0.665% vs clôture 0.777% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑0%/↓0% ; spike-down 47% · recovery-V 15%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; mean-reverting — autocorr -0.04)_ ; drift intra méd. -0.312% ; recovery-V 9%
- **σ réalisé intraday** 2.312% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 52% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 283.5543 (VA 283.2532–284.3067 ; dernier close 282.51)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 36% · rebond 60% · **stop −2.95%** sous le fill (sous le bruit) · cible +1.09% · R/R 0.37 (high win-rate)
- Gaps overnight (n=159) : méd. 0.41% · baisse 35% (gap-down >1% 16% · >2% 7%)
- Excursion ouverture 5min (n=160) : bas méd −0.63% (p90 −1.91%) · haut méd +0.88% · range méd 1.74%
- Excursion ouverture 15min (n=160) : bas méd −0.67% (p90 −2.31%) · haut méd +1.04% · range méd 2.06%
- Excursion ouverture 30min (n=160) : bas méd −0.82% (p90 −2.71%) · haut méd +1.08% · range méd 2.31%
- Excursion ouverture 60min (n=160) : bas méd −0.98% (p90 −2.98%) · haut méd +1.3% · range méd 2.65%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 282.51 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 50% · séance 66% (115/159) · gap 22% · délai 1.3min · rebond 48% (57/115) (MFE +0.95%)
   - −1.0% : fill 30min 41% · séance 56% (100/159) · gap 16% · délai 2.0min · rebond 49% (55/100) (MFE +0.97%)
   - −1.5% : fill 30min 32% · séance 41% (84/159) · gap 9% · délai 3.7min · rebond 49% (45/84) (MFE +0.98%)
   - −2.0% : fill 30min 24% · séance 36% (68/159) · gap 7% · délai 9.2min · rebond 60% (43/68) (MFE +1.09%)
   - −3.0% : fill 30min 10% · séance 22% (41/159) · gap 2% · délai 38.6min · rebond 42% (15/41) (MFE +0.96%)
   - −4.0% : fill 30min 5% · séance 12% (26/159) · gap 1% · délai 37.8min · rebond 45% (12/26) (MFE +0.8%)
   - −5.0% : fill 30min 2% · séance 6% (17/159) · gap 0% · délai 45.1min · rebond 76% (12/17) (MFE +1.23%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.32% (p90 −1.36%) → stop au-delà de −0.82% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.3% (p90 −1.06%) → stop au-delà de −0.93% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.4% (p90 −1.38%) → stop au-delà de −1.07% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=472 jambes) : jambe baissière méd −1.07% (p90 −2.62%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 96% (54/55) · rebond 49% (30/54)
      · −2.0% : fill 76% (42/55) · rebond 58% (27/42)
      · −3.0% : fill 53% (29/55) · rebond 42% (12/29)
      · −4.0% : fill 33% (20/55) · rebond 44% (9/20)
      · −5.0% : fill 20% (15/55) · rebond 77% (11/15)
   - **flat** (28 séances) :
      · −1.0% : fill 57% (16/28) · rebond 34% (5/16)
      · −2.0% : fill 29% (9/28) · rebond 48% (3/9)
      · −3.0% : fill 19% (7/28) · rebond 21% (1/7)
      · −4.0% : fill 9% (4/28) · rebond 20% (1/4)
      · −5.0% : fill 3% (2/28) · rebond 61% (1/2)
   - **gap-up** (76 séances) :
      · −1.0% : fill 34% (30/76) · rebond 57% (20/30)
      · −2.0% : fill 17% (17/76) · rebond 70% (13/17)
      · −3.0% : fill 6% (5/76) · rebond 64% (2/5)
      · −4.0% : fill 1% (2/76) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/76) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 66% si les 15 1res min sont vertes (90 cas) · 26% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **32min** → P(séance verte=clôture>ouverture) 78% si début vert vs 11% si rouge (base 48% · écart 68 pts) ; prédictivité sature ensuite (plafond brut 194min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=91) : tient le vert **78%** · continue >prix actuel 48% ; creux résiduel méd -0.92% (q20 -2.14%) → **SL/trailing à −2.14%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.09% / q75 +2.18% → **scale +1.09% / runner +2.18%**, sortie à la clôture
  - **si ROUGE au coude** (n=69) : edge inversé — récupère vert seulement **11%** (continue à baisser 73%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.75%** (au-delà de la MAE q10 -2.75%), cible rebond +1.0% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.08% .. +2.3%] · haut q95 +2.66% · bas q05 -3.5%
   - 60min (n=160) : retour [-3.67% .. +2.63%] · haut q95 +3.33% · bas q05 -4.7%
   - 2h (n=160) : retour [-3.86% .. +2.94%] · haut q95 +4.16% · bas q05 -4.94%
   - 4h (n=160) : retour [-3.94% .. +3.38%] · haut q95 +4.2% · bas q05 -5.13%
   - 6h (n=160) : retour [-4.71% .. +3.28%] · haut q95 +4.51% · bas q05 -5.13%
   - session (n=160) : retour [-4.33% .. +3.31%] · haut q95 +4.61% · bas q05 -5.41%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 4.4% / strong 1.9%) · base = 10 séances trend-up (n_eff 6.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 14% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.05% (p75 1.33% / p90 1.45%) · ~1.45 replis/séance, durée méd 90.1 min. P(nouveau plus-haut après repli) :
   - −0.5% → **65%** (reprise méd 23.89 min, n=22)
   - −1.0% → **74%** (reprise méd 54.64 min, n=10)
- **RIDER — climb (trail + cibles)** : trail **−1.45%** (p90, défaut prudent ; serré/agressif −1.33%) ; extension open→close méd +3.33% (q75 +4.19% / q95 +6.07%), MFE méd +3.68% / q90 +5.35%
   - Échelle scale-out : +3.68% (33%) / +4.76% (33%) / +5.35% (34%)
- **DÉSARMER** : repli > **−1.45%** depuis le plus-haut = décay → P(retournement) **70%** (préavis méd 295.0 min, n=0) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.35% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 93% du temps (retour médian dernière heure +0.39%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict buy_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 59.8  _(momentum haussier)_
- **ADX** : 20.2  _(pas de tendance nette)_
- **MACD** : hist 1.746  _(pas de croisement recent)_
- **BB** : %B 0.92 · largeur 12.0%
- **ATR** : 10.48 (18.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.223  _(distribution)_
- **Vol ratio** : 0.72  _(volume normal)_
- **Choppiness** : 59.1  _(transition)_
- **MA** : MA20 269.02 · MA50 261.1 · MA200 302.07  _(prix > MA20)_
- **Dist MA** : MA20 +5.0% · MA50 +8.2% · MA200 -6.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91579 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
