# MSTR

**Generated** : 2026-07-15T00:22:29.623557+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $97.58  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $97.58 (+4.2% vs entrée) · entrée $93.64 · stop $86.15 · T1 $96.72 · R/R 0.41  
> ↳ P(T1 av. stop) 3 % _(réel 5 s)_ · EV/risk -0.039 _(réel 5 s)_ (GBM -0.081) · ¼-Kelly 0.029 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.270 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $93.02–$94.25 (mid $93.64)
- Spot actuel : $97.58 (+4.2% au-dessus de la zone — repli à attendre)
- Stop : $86.15 (stop swing_plan-based (-12.24%))
- Targets : T1 $96.72 · R/R 0.41 | T2 $99.80 · R/R 0.82 | T3 $102.88 · R/R 1.23
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $86.15


## Edge, scénarios & sizing

- EV/risk : -0.081 | EV/share : $-0.609 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 14 % | T3 14 %
- Kelly (position) : f* 0.117 | ¼-Kelly 0.029 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 8.1 | bear 83.1 | side 8.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.043% → cible +3.291% / stop −8.0%, p_fill 31%, n_eff≈13.4) : P(cible|rempli) **3%** · **EV/risk -0.039** (×p_fill ; si rempli -1.02% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=13, n_eff=10))
  - **deep** : indisponible (échantillon insuffisant (n=12, n_eff=9))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→71% · +2.0%→55% · +3.0%→35% · +5.0%→14% · +8.0%→8%
- Range intraday médian 5.36% (p90 9.85%) · excursion haute méd. +2.39% / basse méd. −2.84%
- Profil de vol intra : ouverture 3.392% vs midi 1.261% vs clôture 1.298% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 10% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; neutre — autocorr -0.006)_ ; drift intra méd. -0.775% ; recovery-V 35%
- **σ réalisé intraday** 4.231% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 62% / bas 62% / whipsaw 26%
- POC intraday (dernière séance, temps-au-prix) : 94.6587 (VA 93.8262–94.9917 ; dernier close 94.59)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 34% · rebond 68% · **stop −5.18%** sous le fill (sous le bruit) · cible +1.57% · R/R 0.3 (high win-rate)
- Gaps overnight (n=159) : méd. -0.15% · baisse 54% (gap-down >1% 39% · >2% 25%)
- Excursion ouverture 5min (n=160) : bas méd −1.03% (p90 −2.25%) · haut méd +0.62% · range méd 1.87%
- Excursion ouverture 15min (n=160) : bas méd −1.22% (p90 −3.0%) · haut méd +1.07% · range méd 2.56%
- Excursion ouverture 30min (n=160) : bas méd −1.43% (p90 −3.55%) · haut méd +1.32% · range méd 3.18%
- Excursion ouverture 60min (n=160) : bas méd −1.94% (p90 −4.55%) · haut méd +1.52% · range méd 3.93%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 94.59 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 81% (127/159) · gap 47% · délai 0.0min · rebond 53% (64/127) (MFE +1.42%)
   - −1.0% : fill 30min 65% · séance 75% (120/159) · gap 39% · délai 0.0min · rebond 57% (68/120) (MFE +1.47%)
   - −1.5% : fill 30min 57% · séance 70% (112/159) · gap 29% · délai 0.0min · rebond 56% (67/112) (MFE +1.45%)
   - −2.0% : fill 30min 48% · séance 63% (100/159) · gap 25% · délai 0.2min · rebond 56% (64/100) (MFE +1.32%)
   - −3.0% : fill 30min 35% · séance 53% (77/159) · gap 16% · délai 4.0min · rebond 54% (46/77) (MFE +1.49%)
   - −4.0% : fill 30min 23% · séance 44% (62/159) · gap 8% · délai 24.4min · rebond 56% (36/62) (MFE +1.27%)
   - −5.0% : fill 30min 19% · séance 34% (47/159) · gap 6% · délai 24.8min · rebond 68% (33/47) (MFE +1.57%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.99% (p90 −2.52%) → stop au-delà de −1.91% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.2% (p90 −2.84%) → stop au-delà de −2.28% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.35% (p90 −3.08%) → stop au-delà de −2.41% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=965 jambes) : jambe baissière méd −1.21% (p90 −2.84%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (73 séances) :
      · −1.0% : fill 99% (72/73) · rebond 48% (36/72)
      · −2.0% : fill 90% (65/73) · rebond 50% (38/65)
      · −3.0% : fill 81% (56/73) · rebond 54% (33/56)
      · −4.0% : fill 68% (46/73) · rebond 59% (29/46)
      · −5.0% : fill 56% (37/73) · rebond 70% (27/37)
   - **flat** (19 séances) :
      · −1.0% : fill 90% (18/19) · rebond 85% (12/18)
      · −2.0% : fill 60% (14/19) · rebond 66% (10/14)
      · −3.0% : fill 46% (10/19) · rebond 56% (6/10)
      · −4.0% : fill 29% (7/19) · rebond 12% (2/7)
      · −5.0% : fill 22% (5/19) · rebond 15% (2/5)
   - **gap-up** (67 séances) :
      · −1.0% : fill 41% (30/67) · rebond 62% (20/30)
      · −2.0% : fill 31% (21/67) · rebond 71% (16/21)
      · −3.0% : fill 21% (11/67) · rebond 56% (7/11)
      · −4.0% : fill 18% (9/67) · rebond 66% (5/9)
      · −5.0% : fill 9% (5/67) · rebond 93% (4/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 50% si les 15 1res min sont vertes (76 cas) · 36% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **58min** → P(séance verte=clôture>ouverture) 70% si début vert vs 20% si rouge (base 43% · écart 50 pts) ; prédictivité sature ensuite (plafond brut 136min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **70%** · continue >prix actuel 51% ; creux résiduel méd -2.3% (q20 -3.69%) → **SL/trailing à −3.69%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.14% / q75 +3.34% → **scale +2.14% / runner +3.34%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **20%** (continue à baisser 56%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.39%** (au-delà de la MAE q10 -5.39%), cible rebond +1.85% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.77% .. +4.07%] · haut q95 +5.39% · bas q05 -4.18%
   - 60min (n=160) : retour [-4.98% .. +4.42%] · haut q95 +5.54% · bas q05 -5.42%
   - 2h (n=160) : retour [-4.74% .. +5.68%] · haut q95 +6.72% · bas q05 -5.44%
   - 4h (n=160) : retour [-7.33% .. +8.08%] · haut q95 +9.2% · bas q05 -8.32%
   - 6h (n=160) : retour [-6.96% .. +6.96%] · haut q95 +10.07% · bas q05 -8.32%
   - session (n=160) : retour [-5.9% .. +6.34%] · haut q95 +10.07% · bas q05 -8.32%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0.6% / strong 5.0%) · base = 9 séances trend-up (n_eff 6.0)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **16%**. Lecture précoce 30 min : signature présente → 9% vs absente 3% (base 6%)
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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 45.3  _(neutre)_
- **ADX** : 24.6  _(pas de tendance nette)_
- **MACD** : hist 2.048  _(pas de croisement recent)_
- **BB** : %B 0.45 · largeur 50.5%
- **ATR** : 8.22 (8.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.269  _(distribution)_
- **Vol ratio** : 0.66  _(volume normal)_
- **Choppiness** : 61.1  _(transition)_
- **MA** : MA20 100.1 · MA50 134.79 · MA200 172.89  _(prix < MA20)_
- **Dist MA** : MA20 -2.5% · MA50 -27.6% · MA200 -43.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88493 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
