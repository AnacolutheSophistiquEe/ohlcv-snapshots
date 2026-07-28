# SOI

**Generated** : 2026-07-28T21:43:49.440408+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €99.38  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot €99.38 (+10.9% vs entrée) · entrée €89.63 · stop €85.32 · T1 €98.26 · R/R 2.0  
> ↳ P(T1 av. stop) 35 % · EV/risk 0.272 · ¼-Kelly 0.013 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -93 % hors [0,100] (R² max 0.13). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.120 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €87.91–€91.36 (mid €89.63)
- Spot actuel : €99.38 (+10.9% au-dessus de la zone — repli à attendre)
- Stop : €85.32 (stop swing_plan-based (-14.15%))
- Targets : T1 €98.26 · R/R 2.0 | T2 €106.88 · R/R 4.0 | T3 €115.50 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €85.32


## Edge, scénarios & sizing

- EV/risk : 0.272 | EV/share : €1.172 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 16 % | T3 11 %
- Kelly (position) : f* 0.052 | ¼-Kelly 0.013 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 15.7 | bear 77.7 | side 6.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 199.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.461% → cible +4.302% / stop −3.244%, p_fill 49%, n_eff≈19.5) : P(cible|rempli) **35%** · **EV/risk -0.028** (×p_fill ; si rempli -0.18% du capital)
  - **swing** (entrée dip −9.812% → cible +9.62% / stop −4.81%, p_fill 28%, n_eff≈11.8) : P(cible|rempli) **29%** · **EV/risk -0.018** (×p_fill ; si rempli -0.31% du capital)
  - **deep** (entrée dip −15.159% → cible +13.605% / stop −6.802%, p_fill 30%, n_eff≈10.9) : P(cible|rempli) **42%** · **EV/risk +0.058** (×p_fill ; si rempli +1.31% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→78% · +2.0%→70% · +3.0%→59% · +5.0%→45% · +8.0%→22%
- Range intraday médian 9.35% (p90 17.62%) · excursion haute méd. +3.82% / basse méd. −3.36%
- Profil de vol intra : ouverture 6.014% vs midi 1.704% vs clôture 2.609% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (141 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 16% · trend ↑0%/↓1% ; spike-down 77% · recovery-V 42%)_
- **Régime intraday** : **chop** _(efficiency 0.133 ; mean-reverting — autocorr -0.081)_ ; drift intra méd. -0.599% ; recovery-V 37%
- **σ réalisé intraday** 5.711% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 61% / bas 58% / whipsaw 25%
- POC intraday (dernière séance, temps-au-prix) : 112.425 (VA 111.725–117.325 ; dernier close 107.66)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 58% · rebond 76% · **stop −7.58%** sous le fill (sous le bruit) · cible +2.91% · R/R 0.38 (high win-rate)
- Gaps overnight (n=140) : méd. 0.08% · baisse 49% (gap-down >1% 32% · >2% 24%)
- Excursion ouverture 5min (n=141) : bas méd −1.28% (p90 −3.86%) · haut méd +0.99% · range méd 3.18%
- Excursion ouverture 15min (n=141) : bas méd −1.68% (p90 −5.25%) · haut méd +1.28% · range méd 4.07%
- Excursion ouverture 30min (n=141) : bas méd −1.78% (p90 −5.7%) · haut méd +1.72% · range méd 4.42%
- Excursion ouverture 60min (n=141) : bas méd −1.94% (p90 −6.17%) · haut méd +1.84% · range méd 4.92%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 107.66 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 78% (110/140) · gap 38% · délai 0.0min · rebond 65% (72/110) (MFE +1.93%)
   - −1.0% : fill 30min 63% · séance 75% (105/140) · gap 32% · délai 0.2min · rebond 71% (76/105) (MFE +1.87%)
   - −1.5% : fill 30min 59% · séance 71% (96/140) · gap 29% · délai 0.2min · rebond 75% (71/96) (MFE +2.26%)
   - −2.0% : fill 30min 55% · séance 67% (89/140) · gap 24% · délai 0.2min · rebond 78% (71/89) (MFE +2.72%)
   - −3.0% : fill 30min 41% · séance 58% (74/140) · gap 16% · délai 0.8min · rebond 76% (59/74) (MFE +2.91%)
   - −4.0% : fill 30min 32% · séance 49% (60/140) · gap 7% · délai 2.1min · rebond 73% (47/60) (MFE +2.64%)
   - −5.0% : fill 30min 24% · séance 45% (52/140) · gap 2% · délai 18.4min · rebond 76% (43/52) (MFE +2.85%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.84% (p90 −3.78%) → stop au-delà de −2.29% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.9% (p90 −3.03%) → stop au-delà de −2.21% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.84% (p90 −3.19%) → stop au-delà de −2.18% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1236 jambes) : jambe baissière méd −1.34% (p90 −3.17%) · ~18.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 97% (54/55) · rebond 62% (34/54)
      · −2.0% : fill 94% (52/55) · rebond 74% (41/52)
      · −3.0% : fill 85% (44/55) · rebond 76% (36/44)
      · −4.0% : fill 76% (39/55) · rebond 80% (32/39)
      · −5.0% : fill 68% (34/55) · rebond 86% (29/34)
   - **flat** (17 séances) :
      · −1.0% : fill 100% (17/17) · rebond 79% (14/17)
      · −2.0% : fill 96% (15/17) · rebond 82% (12/15)
      · −3.0% : fill 69% (11/17) · rebond 67% (8/11)
      · −4.0% : fill 57% (8/17) · rebond 65% (6/8)
      · −5.0% : fill 57% (8/17) · rebond 77% (7/8)
   - **gap-up** (68 séances) :
      · −1.0% : fill 47% (34/68) · rebond 85% (28/34)
      · −2.0% : fill 33% (22/68) · rebond 85% (18/22)
      · −3.0% : fill 30% (19/68) · rebond 83% (15/19)
      · −4.0% : fill 22% (13/68) · rebond 55% (9/13)
      · −5.0% : fill 20% (10/68) · rebond 47% (7/10)
- **P(clôture VERTE) selon le drive 15min** (n=141) : 52% en base · 73% si les 15 1res min sont vertes (65 cas) · 30% si rouges (76 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=141) : COUDE à **36min** → P(séance verte=clôture>ouverture) 81% si début vert vs 23% si rouge (base 52% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 276min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=64) : tient le vert **81%** · continue >prix actuel 62% ; creux résiduel méd -2.55% (q20 -5.44%) → **SL/trailing à −5.44%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.36% / q75 +5.85% → **scale +3.36% / runner +5.85%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **23%** (continue à baisser 64%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.41%** (au-delà de la MAE q10 -8.41%), cible rebond +2.1% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=141) : retour [-5.3% .. +7.17%] · haut q95 +8.11% · bas q05 -6.67%
   - 60min (n=141) : retour [-6.02% .. +7.38%] · haut q95 +9.8% · bas q05 -7.18%
   - 2h (n=141) : retour [-6.52% .. +10.08%] · haut q95 +12.65% · bas q05 -8.11%
   - 4h (n=141) : retour [-7.17% .. +10.47%] · haut q95 +14.28% · bas q05 -8.38%
   - 6h (n=141) : retour [-8.43% .. +11.8%] · haut q95 +14.33% · bas q05 -10.27%
   - session (n=141) : retour [-11.72% .. +13.89%] · haut q95 +16.26% · bas q05 -13.97%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.4% des séances sont trend-up (mild 0% / strong 6.4%) · base = 9 séances trend-up (n_eff 5.7)
- **ARMER** : fenêtre la + prédictive = **60 min** → P(reste trend-up à la clôture) **14%**. Lecture précoce 30 min : signature présente → 6% vs absente 6% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.08% (p75 1.67% / p90 2.95%) · ~6.0 replis/séance, durée méd 38.95 min. P(nouveau plus-haut après repli) :
   - −0.5% → **94%** (reprise méd 20.0 min, n=57)
   - −1.0% → **92%** (reprise méd 34.22 min, n=33)
   - −1.5% → **88%** (reprise méd 46.1 min, n=17)
   - −2.0% → **87%** (reprise méd 49.44 min, n=15)
   - −3.0% → **100%** (reprise méd 61.76 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.95%** (p90, défaut prudent ; serré/agressif −1.67%) ; extension open→close méd +10.12% (q75 +13.85% / q95 +17.31%), MFE méd +10.12% / q90 +18.28%
   - Échelle scale-out : +10.12% (33%) / +16.57% (33%) / +18.28% (34%)
- **DÉSARMER** : repli > **−2.95%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +18.28% : P(retournement après) 0% (mèche méd 1.42%)
- **CONTEXTE** : la dernière heure tient les gains 94% du temps (retour médian dernière heure +3.01%)


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 50.6  _(neutre)_
- **ADX** : 17.4  _(pas de tendance nette)_
- **MACD** : hist 2.307  _(pas de croisement recent)_
- **BB** : %B 0.42 · largeur 39.8%
- **ATR** : 10.27 (77.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.125  _(distribution)_
- **Vol ratio** : 1.42  _(volume normal)_
- **Choppiness** : 42.9  _(transition)_
- **MA** : MA20 102.74 · MA50 126.47 · MA200 70.05  _(prix < MA20)_
- **Dist MA** : MA20 -3.3% · MA50 -21.4% · MA200 +41.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (99550 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
