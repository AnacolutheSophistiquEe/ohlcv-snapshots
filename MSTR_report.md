# MSTR

**Generated** : 2026-07-20T21:58:06.531570+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $97.82  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $97.82 (+2.0% vs entrée) · entrée $95.87 · stop $91.56 · T1 $104.47 · R/R 2.0  
> ↳ P(T1 av. stop) 4 % _(réel 5 s)_ · EV/risk -0.051 _(réel 5 s)_ (GBM -0.065) · ¼-Kelly 0.01 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.5% cohérent avec le bruit 5 s (EV-optimal ≈ −4.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 159 % hors [0,100] (R² max 0.91). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.200 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $95.27–$96.47 (mid $95.87)
- Spot actuel : $97.82 (+2.0% au-dessus de la zone — repli à attendre)
- Stop : $91.56 (stop swing_plan-based (-7.71%))
- Targets : T1 $104.47 · R/R 2.0 | T2 $104.65 · R/R 2.04 | T3 $104.82 · R/R 2.08
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $91.56


## Edge, scénarios & sizing

- EV/risk : -0.065 | EV/share : $-0.281 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 15 % | T2 15 % | T3 15 %
- Kelly (position) : f* 0.039 | ¼-Kelly 0.01 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.5 | bear 78.9 | side 13.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 98.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.989% → cible +8.976% / stop −4.5%, p_fill 63%, n_eff≈27.3) : P(cible|rempli) **4%** · **EV/risk -0.051** (×p_fill ; si rempli -0.37% du capital)
  - **swing** (entrée dip −4.383% → cible +6.96% / stop −3.48%, p_fill 49%, n_eff≈21.6) : P(cible|rempli) **12%** · **EV/risk -0.303** (×p_fill ; si rempli -2.16% du capital)
  - **deep** (entrée dip −6.783% → cible +9.843% / stop −4.921%, p_fill 55%, n_eff≈23.7) : P(cible|rempli) **19%** · **EV/risk -0.183** (×p_fill ; si rempli -1.64% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→74% · +2.0%→59% · +3.0%→38% · +5.0%→15% · +8.0%→8%
- Range intraday médian 5.61% (p90 9.85%) · excursion haute méd. +2.46% / basse méd. −2.74%
- Profil de vol intra : ouverture 3.43% vs midi 1.292% vs clôture 1.315% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 10% · trend ↑0%/↓0% ; spike-down 76% · recovery-V 37%)_
- **Régime intraday** : **chop** _(efficiency 0.113 ; neutre — autocorr -0.027)_ ; drift intra méd. -0.44% ; recovery-V 38%
- **σ réalisé intraday** 4.142% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 62% / bas 62% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 94.2425 (VA 93.3725–95.2575 ; dernier close 94.85)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 31% · rebond 68% · **stop −5.19%** sous le fill (sous le bruit) · cible +1.57% · R/R 0.3 (high win-rate)
- Gaps overnight (n=159) : méd. -0.21% · baisse 55% (gap-down >1% 41% · >2% 27%)
- Excursion ouverture 5min (n=160) : bas méd −1.02% (p90 −2.13%) · haut méd +0.68% · range méd 1.83%
- Excursion ouverture 15min (n=160) : bas méd −1.21% (p90 −2.92%) · haut méd +1.09% · range méd 2.54%
- Excursion ouverture 30min (n=160) : bas méd −1.42% (p90 −3.48%) · haut méd +1.36% · range méd 3.19%
- Excursion ouverture 60min (n=160) : bas méd −1.91% (p90 −4.23%) · haut méd +1.57% · range méd 3.96%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 94.85 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 81% (127/159) · gap 48% · délai 0.0min · rebond 52% (63/127) (MFE +1.42%)
   - −1.0% : fill 30min 64% · séance 76% (121/159) · gap 41% · délai 0.0min · rebond 56% (68/121) (MFE +1.37%)
   - −1.5% : fill 30min 57% · séance 69% (112/159) · gap 32% · délai 0.0min · rebond 54% (65/112) (MFE +1.34%)
   - −2.0% : fill 30min 49% · séance 63% (101/159) · gap 27% · délai 0.2min · rebond 60% (65/101) (MFE +1.24%)
   - −3.0% : fill 30min 37% · séance 54% (78/159) · gap 19% · délai 2.0min · rebond 58% (47/78) (MFE +1.52%)
   - −4.0% : fill 30min 24% · séance 45% (64/159) · gap 7% · délai 17.3min · rebond 61% (38/64) (MFE +1.65%)
   - −5.0% : fill 30min 17% · séance 31% (46/159) · gap 5% · délai 24.1min · rebond 68% (32/46) (MFE +1.57%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.91% (p90 −2.3%) → stop au-delà de −1.86% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.2% (p90 −2.83%) → stop au-delà de −2.28% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.27% (p90 −2.9%) → stop au-delà de −2.28% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=966 jambes) : jambe baissière méd −1.2% (p90 −2.77%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (74 séances) :
      · −1.0% : fill 99% (73/74) · rebond 47% (36/73)
      · −2.0% : fill 91% (66/74) · rebond 56% (39/66)
      · −3.0% : fill 83% (57/74) · rebond 59% (34/57)
      · −4.0% : fill 71% (48/74) · rebond 65% (31/48)
      · −5.0% : fill 50% (36/74) · rebond 70% (26/36)
   - **flat** (19 séances) :
      · −1.0% : fill 90% (18/19) · rebond 85% (12/18)
      · −2.0% : fill 60% (14/19) · rebond 66% (10/14)
      · −3.0% : fill 46% (10/19) · rebond 56% (6/10)
      · −4.0% : fill 29% (7/19) · rebond 12% (2/7)
      · −5.0% : fill 22% (5/19) · rebond 15% (2/5)
   - **gap-up** (66 séances) :
      · −1.0% : fill 42% (30/66) · rebond 66% (20/30)
      · −2.0% : fill 29% (21/66) · rebond 71% (16/21)
      · −3.0% : fill 19% (11/66) · rebond 56% (7/11)
      · −4.0% : fill 17% (9/66) · rebond 66% (5/9)
      · −5.0% : fill 8% (5/66) · rebond 93% (4/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 51% si les 15 1res min sont vertes (74 cas) · 38% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:12** → P(séance verte=clôture>ouverture) 71% si début vert vs 16% si rouge (base 44% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 136min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **71%** · continue >prix actuel 58% ; creux résiduel méd -1.75% (q20 -3.1%) → **SL/trailing à −3.1%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.97% / q75 +3.1% → **scale +1.97% / runner +3.1%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **16%** (continue à baisser 65%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.48%** (au-delà de la MAE q10 -5.48%), cible rebond +1.29% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.76% .. +4.01%] · haut q95 +5.08% · bas q05 -4.14%
   - 60min (n=160) : retour [-4.91% .. +3.96%] · haut q95 +5.43% · bas q05 -5.25%
   - 2h (n=160) : retour [-4.74% .. +5.63%] · haut q95 +6.55% · bas q05 -5.3%
   - 4h (n=160) : retour [-7.33% .. +7.97%] · haut q95 +9.07% · bas q05 -8.32%
   - 6h (n=160) : retour [-6.71% .. +6.91%] · haut q95 +9.83% · bas q05 -8.32%
   - session (n=160) : retour [-5.88% .. +6.25%] · haut q95 +9.83% · bas q05 -8.32%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0.6% / strong 5.0%) · base = 9 séances trend-up (n_eff 6.0)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **16%**. Lecture précoce 30 min : signature présente → 10% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.43% (p75 2.48% / p90 3.79%) · ~3.8 replis/séance, durée méd 50.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **80%** (reprise méd 25.0 min, n=32)
   - −1.0% → **71%** (reprise méd 35.0 min, n=20)
   - −1.5% → **57%** (reprise méd 74.97 min, n=13)
   - −2.0% → **40%** (reprise méd 89.44 min, n=8)
   - −3.0% → **79%** (reprise méd 89.44 min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−3.79%** (p90, défaut prudent ; serré/agressif −2.48%) ; extension open→close méd +7.18% (q75 +8.18% / q95 +12.92%), MFE méd +9.29% / q90 +12.58%
   - Échelle scale-out : +9.29% (33%) / +10.7% (33%) / +12.58% (34%)
- **DÉSARMER** : repli > **−3.79%** depuis le plus-haut = décay → P(retournement) **29%** (préavis méd 300.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.58% : P(retournement après) 0% (mèche méd 0.76%)
- **CONTEXTE** : la dernière heure tient les gains 96% du temps (retour médian dernière heure +0.68%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 56.0  _(momentum haussier)_
- **ADX** : 20.0  _(pas de tendance nette)_
- **MACD** : hist 2.327  _(pas de croisement recent)_
- **BB** : %B 0.61 · largeur 25.9%
- **ATR** : 6.97 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.202  _(distribution)_
- **Vol ratio** : 0.63  _(volume normal)_
- **Choppiness** : 57.5  _(transition)_
- **MA** : MA20 95.16 · MA50 127.78 · MA200 168.51  _(prix > MA20)_
- **Dist MA** : MA20 +2.8% · MA50 -23.4% · MA200 -42.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92583 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
