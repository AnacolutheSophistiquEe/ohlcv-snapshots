# SMCI

**Generated** : 2026-07-30T00:22:24.316767+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $25.70  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $25.70 (+1.0% vs entrée) · entrée $25.44 · stop $24.49 · T1 $27.33 · R/R 1.99  
> ↳ P(T1 av. stop) 28 % _(réel 5 s)_ · EV/risk -0.212 _(réel 5 s)_ (GBM 0.087) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.130 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $25.17–$25.70 (mid $25.44)
- Spot actuel : $25.70 (+1.0% au-dessus de la zone — repli à attendre)
- Stop : $24.49 (stop swing_plan-based (-4.71%))
- Targets : T1 $27.33 · R/R 1.99 | T2 $29.22 · R/R 3.98 | T3 $31.12 · R/R 5.98
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $24.49


## Edge, scénarios & sizing

- EV/risk : 0.087 | EV/share : $0.082 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 29 % | T2 16 % | T3 11 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 81.5 | bear 12.3 | side 6.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.481% → cible +3.33% / stop −2.581%, p_fill 89%, n_eff≈36.0) : P(cible|rempli) **22%** · **EV/risk -0.285** (×p_fill ; si rempli -0.83% du capital)
  - **swing** (entrée dip −1.025% → cible +7.446% / stop −3.723%, p_fill 83%, n_eff≈33.5) : P(cible|rempli) **28%** · **EV/risk -0.212** (×p_fill ; si rempli -0.95% du capital)
  - **deep** (entrée dip −1.483% → cible +10.53% / stop −5.265%, p_fill 86%, n_eff≈33.0) : P(cible|rempli) **15%** · **EV/risk -0.510** (×p_fill ; si rempli -3.14% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→76% · +2.0%→62% · +3.0%→44% · +5.0%→26% · +8.0%→12%
- Range intraday médian 6.19% (p90 10.14%) · excursion haute méd. +2.55% / basse méd. −2.66%
- Profil de vol intra : ouverture 4.012% vs midi 1.233% vs clôture 1.56% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 16% · trend ↑0%/↓1% ; spike-down 68% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.127 ; mean-reverting — autocorr -0.057)_ ; drift intra méd. -0.31% ; recovery-V 17%
- **σ réalisé intraday** 4.21% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 61% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 28.4076 (VA 28.1661–28.6089 ; dernier close 28.46)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 35% · rebond 77% · **stop −4.18%** sous le fill (sous le bruit) · cible +2.47% · R/R 0.59 (high win-rate)
- Gaps overnight (n=159) : méd. 0.29% · baisse 45% (gap-down >1% 32% · >2% 20%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −2.52%) · haut méd +0.95% · range méd 1.99%
- Excursion ouverture 15min (n=160) : bas méd −1.18% (p90 −3.41%) · haut méd +1.35% · range méd 2.81%
- Excursion ouverture 30min (n=160) : bas méd −1.36% (p90 −3.88%) · haut méd +1.45% · range méd 3.71%
- Excursion ouverture 60min (n=160) : bas méd −1.74% (p90 −4.69%) · haut méd +1.58% · range méd 4.34%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 28.46 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 78% (125/159) · gap 41% · délai 0.0min · rebond 55% (71/125) (MFE +1.2%)
   - −1.0% : fill 30min 57% · séance 72% (113/159) · gap 32% · délai 0.0min · rebond 59% (65/113) (MFE +1.23%)
   - −1.5% : fill 30min 45% · séance 63% (97/159) · gap 26% · délai 0.1min · rebond 60% (58/97) (MFE +1.33%)
   - −2.0% : fill 30min 42% · séance 55% (87/159) · gap 20% · délai 0.4min · rebond 64% (55/87) (MFE +1.58%)
   - −3.0% : fill 30min 28% · séance 50% (70/159) · gap 14% · délai 11.3min · rebond 60% (43/70) (MFE +1.72%)
   - −4.0% : fill 30min 22% · séance 40% (52/159) · gap 9% · délai 13.7min · rebond 67% (32/52) (MFE +1.68%)
   - −5.0% : fill 30min 18% · séance 35% (43/159) · gap 6% · délai 23.1min · rebond 77% (30/43) (MFE +2.47%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.51% (p90 −2.43%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.54% (p90 −3.8%) → stop au-delà de −1.72% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −3.05%) → stop au-delà de −1.62% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=857 jambes) : jambe baissière méd −1.2% (p90 −2.88%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (69 séances) :
      · −1.0% : fill 95% (67/69) · rebond 51% (37/67)
      · −2.0% : fill 85% (59/69) · rebond 58% (34/59)
      · −3.0% : fill 80% (52/69) · rebond 56% (30/52)
      · −4.0% : fill 68% (41/69) · rebond 65% (25/41)
      · −5.0% : fill 58% (34/69) · rebond 75% (23/34)
   - **flat** (14 séances) :
      · −1.0% : fill 94% (12/14) · rebond 87% (9/12)
      · −2.0% : fill 44% (8/14) · rebond 76% (5/8)
      · −3.0% : fill 11% (2/14) · rebond 100% (2/2)
      · −4.0% : fill 4% (1/14) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/14) · rebond 0% (0/0)
   - **gap-up** (76 séances) :
      · −1.0% : fill 49% (34/76) · rebond 66% (19/34)
      · −2.0% : fill 29% (20/76) · rebond 77% (16/20)
      · −3.0% : fill 27% (16/76) · rebond 70% (11/16)
      · −4.0% : fill 19% (10/76) · rebond 71% (6/10)
      · −5.0% : fill 18% (9/76) · rebond 85% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 69% si les 15 1res min sont vertes (74 cas) · 20% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:10** → P(séance verte=clôture>ouverture) 78% si début vert vs 11% si rouge (base 44% · écart 67 pts) ; prédictivité sature ensuite (plafond brut 212min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **78%** · continue >prix actuel 46% ; creux résiduel méd -1.74% (q20 -3.39%) → **SL/trailing à −3.39%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.69% / q75 +2.94% → **scale +1.69% / runner +2.94%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **11%** (continue à baisser 57%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.57%** (au-delà de la MAE q10 -5.57%), cible rebond +1.74% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.27% .. +4.85%] · haut q95 +6.6% · bas q05 -4.54%
   - 60min (n=160) : retour [-4.59% .. +5.59%] · haut q95 +6.6% · bas q05 -5.39%
   - 2h (n=160) : retour [-5.26% .. +6.67%] · haut q95 +8.43% · bas q05 -5.86%
   - 4h (n=160) : retour [-5.82% .. +7.5%] · haut q95 +8.8% · bas q05 -6.94%
   - 6h (n=160) : retour [-6.46% .. +6.91%] · haut q95 +9.66% · bas q05 -7.86%
   - session (n=160) : retour [-7.1% .. +7.85%] · haut q95 +9.66% · bas q05 -8.04%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 9 séances trend-up (n_eff 5.7)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **18%**. Lecture précoce 30 min : signature présente → 9% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.96% (p75 1.83% / p90 2.16%) · ~4.0 replis/séance, durée méd 39.36 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 15.85 min, n=40)
   - −1.0% → **72%** (reprise méd 30.0 min, n=18)
   - −1.5% → **57%** (reprise méd 48.62 min, n=13)
   - −2.0% → **85%** (reprise méd 120.86 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.16%** (p90, défaut prudent ; serré/agressif −1.83%) ; extension open→close méd +7.84% (q75 +8.65% / q95 +9.89%), MFE méd +8.72% / q90 +10.35%
   - Échelle scale-out : +8.72% (33%) / +9.18% (33%) / +10.35% (34%)
- **DÉSARMER** : repli > **−2.16%** depuis le plus-haut = décay → P(retournement) **18%** (préavis méd 100.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.35% : P(retournement après) 0% (mèche méd 1.08%)
- **CONTEXTE** : la dernière heure tient les gains 92% du temps (retour médian dernière heure +1.13%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 42.7  _(momentum baissier)_
- **ADX** : 19.3  _(pas de tendance nette)_
- **MACD** : hist 0.369  _(pas de croisement recent)_
- **BB** : %B 0.28 · largeur 29.8%
- **ATR** : 2.2 (53.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.131  _(distribution)_
- **Vol ratio** : 0.89  _(volume normal)_
- **Choppiness** : 45.8  _(transition)_
- **MA** : MA20 27.46 · MA50 32.49 · MA200 33.03  _(prix < MA20)_
- **Dist MA** : MA20 -6.4% · MA50 -20.9% · MA200 -22.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89116 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
