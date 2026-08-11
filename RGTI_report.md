# RGTI

**Generated** : 2026-08-11T00:27:45.131339+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $17.65  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot $17.65 (+0.6% vs entrée) · entrée $17.54 · stop $16.89 · T1 $18.84 · R/R 2.0  
> ↳ P(T1 av. stop) 22 % _(réel 5 s)_ · EV/risk 0.087 _(réel 5 s)_ (GBM 0.136) · ¼-Kelly 0.052 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.7% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.030 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $17.43–$17.65 (mid $17.54)
- Spot actuel : $17.65 (+0.6% au-dessus de la zone — repli à attendre)
- Stop : $16.89 (stop swing_plan-based (-12.1%))
- Targets : T1 $18.84 · R/R 2.0 | T2 $19.11 · R/R 2.42 | T3 $19.38 · R/R 2.83
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.89


## Edge, scénarios & sizing

- EV/risk : 0.136 | EV/share : $0.088 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 39 % | T3 39 %
- Kelly (position) : f* 0.206 | ¼-Kelly 0.052 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 17.5 | side 77.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 282.0 (= 16 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.619% → cible +7.407% / stop −3.704%, p_fill 83%, n_eff≈36.5) : P(cible|rempli) **22%** · **EV/risk +0.087** (×p_fill ; si rempli +0.39% du capital)
  - **swing** (entrée dip −1.364% → cible +21.747% / stop −10.874%, p_fill 87%, n_eff≈36.1) : P(cible|rempli) **12%** · **EV/risk -0.206** (×p_fill ; si rempli -2.57% du capital)
  - **deep** (entrée dip −2.013% → cible +11.058% / stop −10.733%, p_fill 87%, n_eff≈35.2) : P(cible|rempli) **26%** · **EV/risk -0.435** (×p_fill ; si rempli -5.34% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→79% · +2.0%→71% · +3.0%→56% · +5.0%→40% · +8.0%→14%
- Range intraday médian 8.05% (p90 13.36%) · excursion haute méd. +3.52% / basse méd. −2.82%
- Profil de vol intra : ouverture 5.386% vs midi 1.613% vs clôture 1.879% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 22% · trend ↑0%/↓0% ; spike-down 72% · recovery-V 42%)_
- **Régime intraday** : **chop** _(efficiency 0.137 ; neutre — autocorr -0.027)_ ; drift intra méd. 0.456% ; recovery-V 39%
- **σ réalisé intraday** 4.826% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 54% / whipsaw 9%
- POC intraday (dernière séance, temps-au-prix) : 17.1659 (VA 16.9746–17.3571 ; dernier close 17.935)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 46% · rebond 75% · **stop −6.39%** sous le fill (sous le bruit) · cible +2.32% · R/R 0.36 (high win-rate)
- Gaps overnight (n=159) : méd. -0.47% · baisse 55% (gap-down >1% 45% · >2% 29%)
- Excursion ouverture 5min (n=160) : bas méd −1.23% (p90 −2.72%) · haut méd +1.18% · range méd 2.56%
- Excursion ouverture 15min (n=160) : bas méd −1.44% (p90 −4.09%) · haut méd +1.76% · range méd 3.75%
- Excursion ouverture 30min (n=160) : bas méd −1.77% (p90 −5.31%) · haut méd +2.1% · range méd 4.81%
- Excursion ouverture 60min (n=160) : bas méd −2.07% (p90 −6.17%) · haut méd +2.52% · range méd 5.62%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 17.935 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 75% · séance 82% (134/159) · gap 49% · délai 0.0min · rebond 65% (88/134) (MFE +2.38%)
   - −1.0% : fill 30min 67% · séance 76% (128/159) · gap 45% · délai 0.0min · rebond 67% (85/128) (MFE +2.04%)
   - −1.5% : fill 30min 62% · séance 70% (120/159) · gap 37% · délai 0.0min · rebond 65% (80/120) (MFE +2.2%)
   - −2.0% : fill 30min 57% · séance 65% (113/159) · gap 29% · délai 0.0min · rebond 66% (76/113) (MFE +2.28%)
   - −3.0% : fill 30min 51% · séance 59% (96/159) · gap 13% · délai 1.2min · rebond 73% (70/96) (MFE +2.47%)
   - −4.0% : fill 30min 37% · séance 46% (76/159) · gap 3% · délai 5.7min · rebond 75% (56/76) (MFE +2.32%)
   - −5.0% : fill 30min 20% · séance 35% (61/159) · gap 1% · délai 21.5min · rebond 67% (46/61) (MFE +1.72%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.78% (p90 −2.31%) → stop au-delà de −1.73% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.13% (p90 −2.79%) → stop au-delà de −2.09% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.23% (p90 −3.4%) → stop au-delà de −2.17% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1180 jambes) : jambe baissière méd −1.3% (p90 −3.21%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (83 séances) :
      · −1.0% : fill 98% (82/83) · rebond 64% (51/82)
      · −2.0% : fill 90% (78/83) · rebond 67% (53/78)
      · −3.0% : fill 84% (70/83) · rebond 68% (49/70)
      · −4.0% : fill 67% (56/83) · rebond 72% (40/56)
      · −5.0% : fill 52% (46/83) · rebond 65% (35/46)
   - **flat** (16 séances) :
      · −1.0% : fill 93% (14/16) · rebond 92% (12/14)
      · −2.0% : fill 58% (11/16) · rebond 72% (8/11)
      · −3.0% : fill 46% (6/16) · rebond 84% (4/6)
      · −4.0% : fill 46% (6/16) · rebond 85% (4/6)
      · −5.0% : fill 28% (5/16) · rebond 87% (3/5)
   - **gap-up** (60 séances) :
      · −1.0% : fill 43% (32/60) · rebond 64% (22/32)
      · −2.0% : fill 33% (24/60) · rebond 63% (15/24)
      · −3.0% : fill 27% (20/60) · rebond 89% (17/20)
      · −4.0% : fill 17% (14/60) · rebond 84% (12/14)
      · −5.0% : fill 14% (10/60) · rebond 68% (8/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 53% en base · 72% si les 15 1res min sont vertes (82 cas) · 30% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:32** → P(séance verte=clôture>ouverture) 92% si début vert vs 14% si rouge (base 53% · écart 78 pts) ; prédictivité sature ensuite (plafond brut 140min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **92%** · continue >prix actuel 56% ; creux résiduel méd -1.86% (q20 -3.08%) → **SL/trailing à −3.08%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.68% / q75 +4.37% → **scale +2.68% / runner +4.37%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **14%** (continue à baisser 63%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.65%** (au-delà de la MAE q10 -5.65%), cible rebond +2.13% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.46% .. +4.97%] · haut q95 +6.67% · bas q05 -6.47%
   - 60min (n=160) : retour [-5.69% .. +6.62%] · haut q95 +6.97% · bas q05 -6.96%
   - 2h (n=160) : retour [-6.48% .. +7.49%] · haut q95 +9.18% · bas q05 -7.71%
   - 4h (n=160) : retour [-7.54% .. +7.65%] · haut q95 +9.18% · bas q05 -8.14%
   - 6h (n=160) : retour [-7.59% .. +8.49%] · haut q95 +9.66% · bas q05 -8.83%
   - session (n=160) : retour [-7.62% .. +8.85%] · haut q95 +10.3% · bas q05 -8.84%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 6.8)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **37%**. Lecture précoce 30 min : signature présente → 15% vs absente 4% (base 6%)
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
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 60.0  _(momentum haussier)_
- **ADX** : 21.1  _(pas de tendance nette)_
- **MACD** : hist 0.533  _(pas de croisement recent)_
- **BB** : %B 0.92 · largeur 33.8%
- **ATR** : 1.24 (18.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.033  _(neutre)_
- **Vol ratio** : 0.8  _(volume normal)_
- **Choppiness** : 45.9  _(transition)_
- **MA** : MA20 15.44 · MA50 18.36 · MA200 21.03  _(prix > MA20)_
- **Dist MA** : MA20 +14.3% · MA50 -3.9% · MA200 -16.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92016 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
