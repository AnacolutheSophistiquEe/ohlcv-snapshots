# RGTI

**Generated** : 2026-08-07T00:27:27.911686+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $16.53  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot $16.53 (+1.2% vs entrée) · entrée $16.34 · stop $15.09 · T1 $18.84 · R/R 2.0  
> ↳ P(T1 av. stop) 14 % _(réel 5 s)_ · EV/risk -0.394 _(réel 5 s)_ (GBM -0.091) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.140 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $16.15–$16.53 (mid $16.34)
- Spot actuel : $16.53 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : $15.09 (stop swing_plan-based (-8.73%))
- Targets : T1 $18.84 · R/R 2.0 | T2 $20.17 · R/R 3.06 | T3 $20.17 · R/R 3.06
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $15.09


## Edge, scénarios & sizing

- EV/risk : -0.091 | EV/share : $-0.113 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 21 % | T2 10 % | T3 10 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.3 | bear 28.3 | side 66.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 149.0 (= 9 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.526% → cible +5.015% / stop −2.507%, p_fill 87%, n_eff≈37.5) : P(cible|rempli) **35%** · **EV/risk +0.215** (×p_fill ; si rempli +0.62% du capital)
  - **swing** (entrée dip −1.161% → cible +15.314% / stop −7.658%, p_fill 89%, n_eff≈38.0) : P(cible|rempli) **14%** · **EV/risk -0.394** (×p_fill ; si rempli -3.40% du capital)
  - **deep** (entrée dip −1.685% → cible +24.116% / stop −12.058%, p_fill 90%, n_eff≈36.0) : P(cible|rempli) **2%** · **EV/risk -0.504** (×p_fill ; si rempli -6.75% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→79% · +2.0%→70% · +3.0%→54% · +5.0%→38% · +8.0%→14%
- Range intraday médian 8.05% (p90 13.36%) · excursion haute méd. +3.37% / basse méd. −2.93%
- Profil de vol intra : ouverture 5.405% vs midi 1.617% vs clôture 1.874% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 23% · trend ↑0%/↓0% ; spike-down 73% · recovery-V 41%)_
- **Régime intraday** : **chop** _(efficiency 0.138 ; neutre — autocorr 0.0)_ ; drift intra méd. 0.024% ; recovery-V 35%
- **σ réalisé intraday** 4.826% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 44% / bas 60% / whipsaw 10%
- POC intraday (dernière séance, temps-au-prix) : 16.9691 (VA 16.8344–17.0269 ; dernier close 16.76)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 46% · rebond 74% · **stop −6.41%** sous le fill (sous le bruit) · cible +2.26% · R/R 0.35 (high win-rate)
- Gaps overnight (n=159) : méd. -0.48% · baisse 56% (gap-down >1% 45% · >2% 28%)
- Excursion ouverture 5min (n=160) : bas méd −1.23% (p90 −2.73%) · haut méd +1.13% · range méd 2.56%
- Excursion ouverture 15min (n=160) : bas méd −1.44% (p90 −4.16%) · haut méd +1.58% · range méd 3.59%
- Excursion ouverture 30min (n=160) : bas méd −1.77% (p90 −5.37%) · haut méd +2.06% · range méd 4.81%
- Excursion ouverture 60min (n=160) : bas méd −2.07% (p90 −6.34%) · haut méd +2.4% · range méd 5.47%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 16.76 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 74% · séance 81% (134/159) · gap 49% · délai 0.0min · rebond 63% (87/134) (MFE +2.25%)
   - −1.0% : fill 30min 68% · séance 78% (129/159) · gap 45% · délai 0.0min · rebond 66% (85/129) (MFE +1.91%)
   - −1.5% : fill 30min 62% · séance 71% (121/159) · gap 37% · délai 0.0min · rebond 64% (80/121) (MFE +2.1%)
   - −2.0% : fill 30min 57% · séance 66% (114/159) · gap 28% · délai 0.0min · rebond 66% (76/114) (MFE +2.08%)
   - −3.0% : fill 30min 51% · séance 59% (97/159) · gap 12% · délai 1.3min · rebond 72% (70/97) (MFE +2.38%)
   - −4.0% : fill 30min 37% · séance 46% (76/159) · gap 4% · délai 6.2min · rebond 74% (55/76) (MFE +2.26%)
   - −5.0% : fill 30min 20% · séance 37% (62/159) · gap 1% · délai 21.5min · rebond 67% (46/62) (MFE +1.71%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.78% (p90 −2.46%) → stop au-delà de −1.65% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.13% (p90 −2.85%) → stop au-delà de −2.07% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.23% (p90 −3.9%) → stop au-delà de −2.08% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1173 jambes) : jambe baissière méd −1.29% (p90 −3.27%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (84 séances) :
      · −1.0% : fill 98% (83/84) · rebond 62% (51/83)
      · −2.0% : fill 90% (79/84) · rebond 65% (53/79)
      · −3.0% : fill 84% (71/84) · rebond 67% (49/71)
      · −4.0% : fill 66% (56/84) · rebond 71% (39/56)
      · −5.0% : fill 54% (47/84) · rebond 64% (35/47)
   - **flat** (16 séances) :
      · −1.0% : fill 93% (14/16) · rebond 92% (12/14)
      · −2.0% : fill 58% (11/16) · rebond 72% (8/11)
      · −3.0% : fill 46% (6/16) · rebond 84% (4/6)
      · −4.0% : fill 46% (6/16) · rebond 85% (4/6)
      · −5.0% : fill 28% (5/16) · rebond 87% (3/5)
   - **gap-up** (59 séances) :
      · −1.0% : fill 45% (32/59) · rebond 64% (22/32)
      · −2.0% : fill 35% (24/59) · rebond 63% (15/24)
      · −3.0% : fill 28% (20/59) · rebond 89% (17/20)
      · −4.0% : fill 18% (14/59) · rebond 84% (12/14)
      · −5.0% : fill 15% (10/59) · rebond 68% (8/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 70% si les 15 1res min sont vertes (80 cas) · 30% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:32** → P(séance verte=clôture>ouverture) 91% si début vert vs 14% si rouge (base 51% · écart 78 pts) ; prédictivité sature ensuite (plafond brut 140min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **91%** · continue >prix actuel 56% ; creux résiduel méd -1.86% (q20 -3.07%) → **SL/trailing à −3.07%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.68% / q75 +4.26% → **scale +2.68% / runner +4.26%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **14%** (continue à baisser 63%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.65%** (au-delà de la MAE q10 -5.65%), cible rebond +2.12% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.47% .. +4.97%] · haut q95 +6.74% · bas q05 -6.48%
   - 60min (n=160) : retour [-5.77% .. +6.68%] · haut q95 +7.0% · bas q05 -6.99%
   - 2h (n=160) : retour [-6.5% .. +7.58%] · haut q95 +9.18% · bas q05 -7.84%
   - 4h (n=160) : retour [-7.59% .. +7.71%] · haut q95 +9.18% · bas q05 -8.35%
   - 6h (n=160) : retour [-7.62% .. +8.54%] · haut q95 +9.77% · bas q05 -9.08%
   - session (n=160) : retour [-7.68% .. +8.91%] · haut q95 +10.32% · bas q05 -9.11%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 6.8)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **41%**. Lecture précoce 30 min : signature présente → 17% vs absente 4% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.25% (p75 1.69% / p90 2.67%) · ~4.0 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 13.25 min, n=41)
   - −1.0% → **77%** (reprise méd 55.8 min, n=26)
   - −1.5% → **78%** (reprise méd 94.96 min, n=15)
   - −2.0% → **79%** (reprise méd 109.11 min, n=8)
   - −3.0% → **67%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.67%** (p90, défaut prudent ; serré/agressif −1.69%) ; extension open→close méd +7.29% (q75 +9.11% / q95 +9.99%), MFE méd +9.12% / q90 +10.34%
   - Échelle scale-out : +9.12% (33%) / +10.23% (33%) / +10.34% (34%)
- **DÉSARMER** : repli > **−2.67%** depuis le plus-haut = décay → P(retournement) **33%** (préavis méd 141.49 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.34% : P(retournement après) 0% (mèche méd 1.02%)
- **CONTEXTE** : la dernière heure tient les gains 59% du temps (retour médian dernière heure +0.5%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 60.7  _(momentum haussier)_
- **ADX** : 23.0  _(pas de tendance nette)_
- **MACD** : hist 0.452  _(pas de croisement recent)_
- **BB** : %B 0.8 · largeur 28.1%
- **ATR** : 1.19 (15.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.142  _(distribution)_
- **Vol ratio** : 1.02  _(volume normal)_
- **Choppiness** : 48.9  _(transition)_
- **MA** : MA20 15.26 · MA50 18.68 · MA200 21.27  _(prix > MA20)_
- **Dist MA** : MA20 +8.3% · MA50 -11.5% · MA200 -22.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91508 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
