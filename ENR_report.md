# ENR

**Generated** : 2026-08-18T00:05:32.313368+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €163.44  

> 🟡 **WAIT-FOR-DIP** — spot +13.7 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €163.44 (+13.7% vs entrée) · entrée €143.71 · stop €136.46 · T1 €149.13 · R/R 0.75  
> ↳ P(T1 av. stop) 56 % · EV/risk 0.072 · ¼-Kelly 0.01 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

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

Plan privilegie B (swing), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €142.62–€144.79 (mid €143.71)
- Spot actuel : €163.44 (+13.7% au-dessus de la zone — repli à attendre)
- Stop : €136.46 (stop swing_plan-based (-16.51%))
- Targets : T1 €149.13 · R/R 0.75 | T2 €154.55 · R/R 1.5 | T3 €159.98 · R/R 2.24
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €136.46


## Edge, scénarios & sizing

- EV/risk : 0.072 | EV/share : €0.526 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 56 % | T2 30 % | T3 10 %
- Kelly (position) : f* 0.04 | ¼-Kelly 0.01 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 7.9 | bear 8.2 | side 84.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 490.0 (= 3 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=8, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→60% · +2.0%→44% · +3.0%→24% · +5.0%→8% · +8.0%→1%
- Range intraday médian 4.02% (p90 6.24%) · excursion haute méd. +1.47% / basse méd. −1.96%
- Profil de vol intra : ouverture 2.12% vs midi 0.943% vs clôture 1.144% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 11% · trend ↑2%/↓0% ; spike-down 57% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; neutre — autocorr -0.016)_ ; drift intra méd. -0.28% ; recovery-V 14%
- **σ réalisé intraday** 2.68% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 67% / whipsaw 36%
- POC intraday (dernière séance, temps-au-prix) : 160.9212 (VA 160.4323–161.3288 ; dernier close 160.34)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 29% · rebond 62% · **stop −3.5%** sous le fill (sous le bruit) · cible +1.53% · R/R 0.44 (high win-rate)
- Gaps overnight (n=159) : méd. 0.38% · baisse 35% (gap-down >1% 19% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.52% (p90 −1.7%) · haut méd +0.5% · range méd 1.32%
- Excursion ouverture 15min (n=160) : bas méd −0.67% (p90 −2.22%) · haut méd +0.67% · range méd 1.64%
- Excursion ouverture 30min (n=160) : bas méd −0.78% (p90 −2.29%) · haut méd +0.68% · range méd 1.98%
- Excursion ouverture 60min (n=160) : bas méd −0.89% (p90 −2.57%) · haut méd +0.82% · range méd 2.16%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 160.34 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 53% · séance 70% (114/159) · gap 26% · délai 0.4min · rebond 57% (65/114) (MFE +1.22%)
   - −1.0% : fill 30min 44% · séance 65% (105/159) · gap 19% · délai 3.8min · rebond 67% (64/105) (MFE +1.57%)
   - −1.5% : fill 30min 34% · séance 60% (94/159) · gap 16% · délai 15.6min · rebond 67% (61/94) (MFE +1.74%)
   - −2.0% : fill 30min 20% · séance 45% (72/159) · gap 11% · délai 50.2min · rebond 64% (45/72) (MFE +1.51%)
   - −3.0% : fill 30min 12% · séance 29% (51/159) · gap 4% · délai 204.5min · rebond 62% (35/51) (MFE +1.53%)
   - −4.0% : fill 30min 6% · séance 19% (38/159) · gap 2% · délai 271.7min · rebond 59% (26/38) (MFE +1.22%)
   - −5.0% : fill 30min 2% · séance 14% (23/159) · gap 1% · délai 219.5min · rebond 63% (15/23) (MFE +1.33%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.45% (p90 −1.99%) → stop au-delà de −0.98% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.39% (p90 −1.94%) → stop au-delà de −0.95% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.41% (p90 −0.97%) → stop au-delà de −0.72% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=534 jambes) : jambe baissière méd −1.07% (p90 −2.6%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 97% (48/49) · rebond 62% (27/48)
      · −2.0% : fill 74% (38/49) · rebond 58% (24/38)
      · −3.0% : fill 58% (31/49) · rebond 50% (20/31)
      · −4.0% : fill 44% (25/49) · rebond 53% (17/25)
      · −5.0% : fill 35% (17/49) · rebond 59% (11/17)
   - **flat** (24 séances) :
      · −1.0% : fill 66% (18/24) · rebond 80% (12/18)
      · −2.0% : fill 30% (10/24) · rebond 69% (5/10)
      · −3.0% : fill 11% (5/24) · rebond 80% (3/5)
      · −4.0% : fill 9% (4/24) · rebond 76% (2/4)
      · −5.0% : fill 6% (2/24) · rebond 74% (1/2)
   - **gap-up** (86 séances) :
      · −1.0% : fill 47% (39/86) · rebond 67% (25/39)
      · −2.0% : fill 32% (24/86) · rebond 71% (16/24)
      · −3.0% : fill 18% (15/86) · rebond 81% (12/15)
      · −4.0% : fill 8% (9/86) · rebond 69% (7/9)
      · −5.0% : fill 4% (4/86) · rebond 78% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 75% si les 15 1res min sont vertes (78 cas) · 24% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:24** → P(séance verte=clôture>ouverture) 82% si début vert vs 26% si rouge (base 49% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 282min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **82%** · continue >prix actuel 53% ; creux résiduel méd -1.33% (q20 -2.02%) → **SL/trailing à −2.02%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.89% / q75 +2.58% → **scale +1.89% / runner +2.58%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **26%** (continue à baisser 54%) → **RÉDUIRE ~74%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.26%** (au-delà de la MAE q10 -4.26%), cible rebond +1.45% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.15% .. +2.3%] · haut q95 +2.68% · bas q05 -2.68%
   - 60min (n=160) : retour [-2.46% .. +2.34%] · haut q95 +2.74% · bas q05 -3.15%
   - 2h (n=160) : retour [-2.86% .. +2.69%] · haut q95 +3.11% · bas q05 -3.97%
   - 4h (n=160) : retour [-3.58% .. +2.68%] · haut q95 +3.79% · bas q05 -4.39%
   - 6h (n=160) : retour [-3.91% .. +3.62%] · haut q95 +4.6% · bas q05 -4.95%
   - session (n=160) : retour [-5.19% .. +4.34%] · haut q95 +5.45% · bas q05 -6.22%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 1.3% / strong 4.4%) · base = 9 séances trend-up (n_eff 6.6)
- **ARMER** : fenêtre la + prédictive = **45 min** → P(reste trend-up à la clôture) **15%**. Lecture précoce 30 min : signature présente → 14% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.83% (p75 1.19% / p90 1.45%) · ~3.0 replis/séance, durée méd 78.78 min. P(nouveau plus-haut après repli) :
   - −0.5% → **99%** (reprise méd 55.57 min, n=25)
   - −1.0% → **100%** (reprise méd 80.0 min, n=10)
- **RIDER — climb (trail + cibles)** : trail **−1.45%** (p90, défaut prudent ; serré/agressif −1.19%) ; extension open→close méd +4.46% (q75 +6.49% / q95 +8.61%), MFE méd +5.07% / q90 +9.14%
   - Échelle scale-out : +5.07% (33%) / +6.83% (33%) / +9.14% (34%)
- **DÉSARMER** : repli > **−1.45%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +9.14% : P(retournement après) 0% (mèche méd 0.54%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.37%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 67.2  _(momentum haussier)_
- **ADX** : 17.0  _(pas de tendance nette)_
- **MACD** : hist 2.032  _(pas de croisement recent)_
- **BB** : %B 0.88 · largeur 19.2%
- **ATR** : 7.25 (53.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.132  _(distribution)_
- **Vol ratio** : 0.24  _(volume atone)_
- **Choppiness** : 43.1  _(transition)_
- **MA** : MA20 152.44 · MA50 155.49 · MA200 147.29  _(prix > MA20)_
- **Dist MA** : MA20 +7.2% · MA50 +5.1% · MA200 +11.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93647 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
