# CEG

**Generated** : 2026-07-14T00:29:26.182388+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $257.57  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot $257.57 (+2.0% vs entrée) · entrée $252.49 · stop $248.70 · T1 $255.89 · R/R 0.9  
> ↳ P(T1 av. stop) 30 % _(réel 5 s)_ · EV/risk -0.031 _(réel 5 s)_ (GBM -0.039) · ¼-Kelly 0.006 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.080 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $251.81–$253.17 (mid $252.49)
- Spot actuel : $257.57 (+2.0% au-dessus de la zone — repli à attendre)
- Stop : $248.70 (stop swing_plan-based (-5.78%))
- Targets : T1 $255.89 · R/R 0.9 | T2 $259.28 · R/R 1.79 | T3 $262.68 · R/R 2.69
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $248.70


## Edge, scénarios & sizing

- EV/risk : -0.039 | EV/share : $-0.149 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 23 % | T3 8 %
- Kelly (position) : f* 0.026 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 82.0 | bear 5.7 | side 12.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.97% → cible +1.345% / stop −1.5%, p_fill 36%, n_eff≈17.3) : P(cible|rempli) **30%** · **EV/risk -0.031** (×p_fill ; si rempli -0.13% du capital)
  - **swing** (entrée dip −4.341% → cible +3.008% / stop −1.504%, p_fill 27%, n_eff≈11.4) : P(cible|rempli) **16%** · **EV/risk -0.150** (×p_fill ; si rempli -0.85% du capital)
  - **deep** (entrée dip −6.705% → cible +4.255% / stop −2.127%, p_fill 34%, n_eff≈12.8) : P(cible|rempli) **14%** · **EV/risk -0.212** (×p_fill ; si rempli -1.33% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→66% · +2.0%→38% · +3.0%→22% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.44% (p90 5.5%) · excursion haute méd. +1.51% / basse méd. −1.55%
- Profil de vol intra : ouverture 2.56% vs midi 0.735% vs clôture 0.77% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 48% · recovery-V 21%)_
- **Régime intraday** : **chop** _(efficiency 0.109 ; mean-reverting — autocorr -0.059)_ ; drift intra méd. -0.237% ; recovery-V 14%
- **σ réalisé intraday** 2.311% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 61% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 250.6275 (VA 250.2875–251.3925 ; dernier close 251.38)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 45% · rebond 60% · **stop −3.2%** sous le fill (sous le bruit) · cible +1.08% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. 0.1% · baisse 46% (gap-down >1% 21% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −0.63% (p90 −1.59%) · haut méd +0.84% · range méd 1.62%
- Excursion ouverture 15min (n=160) : bas méd −0.74% (p90 −2.23%) · haut méd +1.0% · range méd 2.05%
- Excursion ouverture 30min (n=160) : bas méd −0.84% (p90 −2.73%) · haut méd +1.07% · range méd 2.31%
- Excursion ouverture 60min (n=160) : bas méd −1.04% (p90 −3.06%) · haut méd +1.29% · range méd 2.71%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 251.38 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 72% (120/159) · gap 28% · délai 0.0min · rebond 46% (60/120) (MFE +0.92%)
   - −1.0% : fill 30min 52% · séance 63% (104/159) · gap 21% · délai 1.5min · rebond 51% (58/104) (MFE +1.06%)
   - −1.5% : fill 30min 39% · séance 53% (90/159) · gap 10% · délai 3.9min · rebond 52% (49/90) (MFE +1.05%)
   - −2.0% : fill 30min 29% · séance 45% (70/159) · gap 8% · délai 10.0min · rebond 60% (43/70) (MFE +1.08%)
   - −3.0% : fill 30min 12% · séance 27% (43/159) · gap 3% · délai 42.3min · rebond 36% (17/43) (MFE +0.79%)
   - −4.0% : fill 30min 5% · séance 16% (28/159) · gap 2% · délai 48.4min · rebond 37% (12/28) (MFE +0.6%)
   - −5.0% : fill 30min 4% · séance 10% (19/159) · gap 1% · délai 45.6min · rebond 74% (12/19) (MFE +1.21%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.47% (p90 −1.34%) → stop au-delà de −0.86% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.25% (p90 −1.1%) → stop au-delà de −0.73% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.28% (p90 −1.59%) → stop au-delà de −0.97% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=480 jambes) : jambe baissière méd −1.07% (p90 −2.6%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 100% (56/56) · rebond 50% (34/56)
      · −2.0% : fill 79% (41/56) · rebond 57% (27/41)
      · −3.0% : fill 55% (27/56) · rebond 39% (11/27)
      · −4.0% : fill 36% (19/56) · rebond 34% (8/19)
      · −5.0% : fill 25% (15/56) · rebond 77% (11/15)
   - **flat** (36 séances) :
      · −1.0% : fill 60% (21/36) · rebond 40% (7/21)
      · −2.0% : fill 36% (12/36) · rebond 48% (4/12)
      · −3.0% : fill 24% (10/36) · rebond 28% (4/10)
      · −4.0% : fill 11% (5/36) · rebond 19% (1/5)
      · −5.0% : fill 4% (3/36) · rebond 50% (1/3)
   - **gap-up** (67 séances) :
      · −1.0% : fill 35% (27/67) · rebond 63% (17/27)
      · −2.0% : fill 22% (17/67) · rebond 79% (12/17)
      · −3.0% : fill 7% (6/67) · rebond 32% (2/6)
      · −4.0% : fill 3% (4/67) · rebond 90% (3/4)
      · −5.0% : fill 0% (1/67) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 73% si les 15 1res min sont vertes (89 cas) · 21% si rouges (71 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:31** → P(séance verte=clôture>ouverture) 86% si début vert vs 12% si rouge (base 51% · écart 74 pts) ; prédictivité sature ensuite (plafond brut 194min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **86%** · continue >prix actuel 43% ; creux résiduel méd -0.85% (q20 -1.79%) → **SL/trailing à −1.79%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.77% / q75 +1.4% → **scale +0.77% / runner +1.4%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **12%** (continue à baisser 51%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.6%** (au-delà de la MAE q10 -2.6%), cible rebond +0.82% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.0% .. +2.38%] · haut q95 +2.84% · bas q05 -3.51%
   - 60min (n=160) : retour [-3.73% .. +2.77%] · haut q95 +3.43% · bas q05 -4.51%
   - 2h (n=160) : retour [-3.95% .. +3.04%] · haut q95 +4.21% · bas q05 -5.03%
   - 4h (n=160) : retour [-4.05% .. +3.35%] · haut q95 +5.08% · bas q05 -5.73%
   - 6h (n=160) : retour [-4.76% .. +3.42%] · haut q95 +5.28% · bas q05 -6.05%
   - session (n=160) : retour [-4.33% .. +3.39%] · haut q95 +5.28% · bas q05 -6.05%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 3.7% / strong 1.9%) · base = 9 séances trend-up (n_eff 6.2)
- **ARMER** : fenêtre la + prédictive = **60 min** → P(reste trend-up à la clôture) **26%**. Lecture précoce 30 min : signature présente → 15% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.07% (p75 1.33% / p90 1.7%) · ~1.3 replis/séance, durée méd 60.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **65%** (reprise méd 22.57 min, n=22)
   - −1.0% → **58%** (reprise méd 114.96 min, n=10)
   - −1.5% → **37%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.7%** (p90, défaut prudent ; serré/agressif −1.33%) ; extension open→close méd +3.24% (q75 +3.91% / q95 +6.6%), MFE méd +3.42% / q90 +5.81%
   - Échelle scale-out : +3.42% (33%) / +5.29% (33%) / +5.81% (34%)
- **DÉSARMER** : repli > **−1.7%** depuis le plus-haut = décay → P(retournement) **63%** (préavis méd 295.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.81% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 89% du temps (retour médian dernière heure +0.38%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : neutral_cautious


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 37.8  _(momentum baissier)_
- **ADX** : 22.2  _(pas de tendance nette)_
- **MACD** : hist 0.842  _(bullish_recent)_
- **BB** : %B 0.51 · largeur 19.0%
- **ATR** : 9.03 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.082  _(distribution)_
- **Vol ratio** : 0.72  _(volume normal)_
- **Choppiness** : 37.4  _(marche directionnel)_
- **MA** : MA20 257.25 · MA50 272.3 · MA200 313.67  _(prix > MA20)_
- **Dist MA** : MA20 +0.1% · MA50 -5.4% · MA200 -17.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89888 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
