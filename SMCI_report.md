# SMCI

**Generated** : 2026-07-28T21:58:23.230771+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $28.45  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot $28.45 (+6.2% vs entrée) · entrée $26.79 · stop $25.85 · T1 $28.67 · R/R 2.0  
> ↳ P(T1 av. stop) 13 % _(réel 5 s)_ · EV/risk -0.241 _(réel 5 s)_ (GBM 0.059) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.070 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $26.42–$27.17 (mid $26.79)
- Spot actuel : $28.45 (+6.2% au-dessus de la zone — repli à attendre)
- Stop : $25.85 (stop swing_plan-based (-9.13%))
- Targets : T1 $28.67 · R/R 2.0 | T2 $30.55 · R/R 4.0 | T3 $32.43 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $25.85


## Edge, scénarios & sizing

- EV/risk : 0.059 | EV/share : $0.055 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 15 % | T3 10 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 85.3 | bear 7.6 | side 7.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 142.0 (= 5 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.648% → cible +6.454% / stop −3.227%, p_fill 50%, n_eff≈20.9) : P(cible|rempli) **1%** · **EV/risk -0.147** (×p_fill ; si rempli -0.95% du capital)
  - **swing** (entrée dip −5.824% → cible +7.02% / stop −3.51%, p_fill 36%, n_eff≈15.3) : P(cible|rempli) **13%** · **EV/risk -0.241** (×p_fill ; si rempli -2.34% du capital)
  - **deep** (entrée dip −9.003% → cible +9.928% / stop −4.964%, p_fill 43%, n_eff≈16.2) : P(cible|rempli) **31%** · **EV/risk -0.078** (×p_fill ; si rempli -0.89% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→78% · +2.0%→64% · +3.0%→45% · +5.0%→26% · +8.0%→12%
- Range intraday médian 6.19% (p90 10.14%) · excursion haute méd. +2.57% / basse méd. −2.56%
- Profil de vol intra : ouverture 3.973% vs midi 1.224% vs clôture 1.567% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 17% · trend ↑0%/↓1% ; spike-down 67% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; mean-reverting — autocorr -0.065)_ ; drift intra méd. -0.29% ; recovery-V 19%
- **σ réalisé intraday** 4.167% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 64% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 28.8949 (VA 28.7231–29.2384 ; dernier close 29.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 34% · rebond 76% · **stop −4.11%** sous le fill (sous le bruit) · cible +2.56% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. 0.3% · baisse 44% (gap-down >1% 31% · >2% 19%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −2.03%) · haut méd +0.96% · range méd 1.99%
- Excursion ouverture 15min (n=160) : bas méd −1.1% (p90 −3.11%) · haut méd +1.36% · range méd 2.79%
- Excursion ouverture 30min (n=160) : bas méd −1.36% (p90 −3.7%) · haut méd +1.47% · range méd 3.66%
- Excursion ouverture 60min (n=160) : bas méd −1.64% (p90 −4.4%) · haut méd +1.62% · range méd 4.32%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 29.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 77% (125/159) · gap 40% · délai 0.0min · rebond 57% (72/125) (MFE +1.23%)
   - −1.0% : fill 30min 56% · séance 71% (113/159) · gap 31% · délai 0.0min · rebond 60% (65/113) (MFE +1.28%)
   - −1.5% : fill 30min 44% · séance 63% (97/159) · gap 24% · délai 0.5min · rebond 62% (59/97) (MFE +1.43%)
   - −2.0% : fill 30min 41% · séance 55% (87/159) · gap 19% · délai 1.0min · rebond 66% (55/87) (MFE +1.59%)
   - −3.0% : fill 30min 27% · séance 49% (70/159) · gap 13% · délai 18.5min · rebond 62% (43/70) (MFE +1.79%)
   - −4.0% : fill 30min 21% · séance 39% (52/159) · gap 9% · délai 15.6min · rebond 70% (32/52) (MFE +1.7%)
   - −5.0% : fill 30min 16% · séance 34% (43/159) · gap 6% · délai 39.9min · rebond 76% (30/43) (MFE +2.56%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.51% (p90 −2.43%) → stop au-delà de −1.26% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.54% (p90 −3.8%) → stop au-delà de −1.72% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −3.05%) → stop au-delà de −1.62% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=853 jambes) : jambe baissière méd −1.2% (p90 −2.88%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (69 séances) :
      · −1.0% : fill 95% (67/69) · rebond 53% (37/67)
      · −2.0% : fill 85% (59/69) · rebond 61% (34/59)
      · −3.0% : fill 80% (52/69) · rebond 58% (30/52)
      · −4.0% : fill 67% (41/69) · rebond 69% (25/41)
      · −5.0% : fill 56% (34/69) · rebond 73% (23/34)
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
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 69% si les 15 1res min sont vertes (75 cas) · 21% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:10** → P(séance verte=clôture>ouverture) 78% si début vert vs 11% si rouge (base 45% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 212min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **78%** · continue >prix actuel 46% ; creux résiduel méd -1.71% (q20 -3.39%) → **SL/trailing à −3.39%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.68% / q75 +2.94% → **scale +1.68% / runner +2.94%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **11%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.6%** (au-delà de la MAE q10 -5.6%), cible rebond +1.69% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.07% .. +4.94%] · haut q95 +6.65% · bas q05 -4.33%
   - 60min (n=160) : retour [-4.61% .. +5.61%] · haut q95 +6.65% · bas q05 -5.41%
   - 2h (n=160) : retour [-5.26% .. +6.7%] · haut q95 +8.47% · bas q05 -5.88%
   - 4h (n=160) : retour [-5.88% .. +7.52%] · haut q95 +8.84% · bas q05 -6.94%
   - 6h (n=160) : retour [-6.46% .. +6.92%] · haut q95 +9.77% · bas q05 -7.91%
   - session (n=160) : retour [-7.13% .. +7.85%] · haut q95 +9.77% · bas q05 -8.13%


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
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 50.9  _(neutre)_
- **ADX** : 19.9  _(pas de tendance nette)_
- **MACD** : hist 0.622  _(pas de croisement recent)_
- **BB** : %B 0.6 · largeur 29.6%
- **ATR** : 2.07 (48.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.065  _(distribution)_
- **Vol ratio** : 0.8  _(volume normal)_
- **Choppiness** : 43.4  _(transition)_
- **MA** : MA20 27.64 · MA50 32.6 · MA200 33.19  _(prix > MA20)_
- **Dist MA** : MA20 +2.9% · MA50 -12.7% · MA200 -14.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92483 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
