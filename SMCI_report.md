# SMCI

**Generated** : 2026-08-10T22:00:22.209629+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $31.46  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-11 — SMCI earnings (J-1 sess · earnings)  
> ↳ spot $31.46 (+5.0% vs entrée) · entrée $29.97 · stop $29.14 · T1 $31.64 · R/R 2.01  
> ↳ P(T1 av. stop) 0 % _(réel 5 s)_ · EV/risk 0.05 _(réel 5 s)_ (GBM 0.032) · ¼-Kelly 0.016 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.77% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.060 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $29.76–$30.19 (mid $29.97)
- Spot actuel : $31.46 (+5.0% au-dessus de la zone — repli à attendre)
- Stop : $29.14 (stop swing_plan-based (-18.49%))
- Targets : T1 $31.64 · R/R 2.01 | T2 $32.43 · R/R 2.96 | T3 $33.23 · R/R 3.93
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $29.14


## Edge, scénarios & sizing

- EV/risk : 0.032 | EV/share : $0.026 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 25 % | T2 25 % | T3 25 %
- Kelly (position) : f* 0.065 | ¼-Kelly 0.016 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 63.3 | bear 7.3 | side 29.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 378.0 (= 12 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.727% → cible +5.548% / stop −2.774%, p_fill 29%, n_eff≈12.8) : P(cible|rempli) **0%** · **EV/risk +0.050** (×p_fill ; si rempli +0.49% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=8, n_eff=5))
  - **deep** : indisponible (échantillon insuffisant (n=10, n_eff=7))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→78% · +2.0%→64% · +3.0%→46% · +5.0%→26% · +8.0%→11%
- Range intraday médian 6.47% (p90 10.14%) · excursion haute méd. +2.57% / basse méd. −2.52%
- Profil de vol intra : ouverture 4.003% vs midi 1.234% vs clôture 1.634% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 17% · trend ↑0%/↓1% ; spike-down 69% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.138 ; mean-reverting — autocorr -0.07)_ ; drift intra méd. -0.133% ; recovery-V 22%
- **σ réalisé intraday** 4.055% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 51% / bas 58% / whipsaw 13%
- POC intraday (dernière séance, temps-au-prix) : 31.1159 (VA 30.4231–31.2789 ; dernier close 31.11)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 32% · rebond 78% · **stop −4.6%** sous le fill (sous le bruit) · cible +2.22% · R/R 0.48 (high win-rate)
- Gaps overnight (n=159) : méd. 0.29% · baisse 44% (gap-down >1% 33% · >2% 18%)
- Excursion ouverture 5min (n=160) : bas méd −0.81% (p90 −2.59%) · haut méd +0.92% · range méd 2.0%
- Excursion ouverture 15min (n=160) : bas méd −1.28% (p90 −3.22%) · haut méd +1.36% · range méd 2.78%
- Excursion ouverture 30min (n=160) : bas méd −1.62% (p90 −3.73%) · haut méd +1.45% · range méd 3.61%
- Excursion ouverture 60min (n=160) : bas méd −1.92% (p90 −4.79%) · haut méd +1.68% · range méd 4.31%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 31.11 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 75% (123/159) · gap 41% · délai 0.0min · rebond 56% (72/123) (MFE +1.27%)
   - −1.0% : fill 30min 56% · séance 71% (113/159) · gap 33% · délai 0.0min · rebond 61% (66/113) (MFE +1.32%)
   - −1.5% : fill 30min 46% · séance 64% (99/159) · gap 24% · délai 0.0min · rebond 63% (61/99) (MFE +1.53%)
   - −2.0% : fill 30min 43% · séance 55% (88/159) · gap 18% · délai 0.8min · rebond 66% (55/88) (MFE +1.67%)
   - −3.0% : fill 30min 32% · séance 50% (74/159) · gap 12% · délai 9.8min · rebond 62% (46/74) (MFE +1.8%)
   - −4.0% : fill 30min 21% · séance 39% (54/159) · gap 8% · délai 21.7min · rebond 70% (34/54) (MFE +1.68%)
   - −5.0% : fill 30min 15% · séance 32% (44/159) · gap 5% · délai 39.0min · rebond 78% (31/44) (MFE +2.22%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −2.26%) → stop au-delà de −1.57% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.7% (p90 −3.08%) → stop au-delà de −1.91% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.73% (p90 −2.67%) → stop au-delà de −1.94% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=875 jambes) : jambe baissière méd −1.19% (p90 −2.87%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (69 séances) :
      · −1.0% : fill 95% (67/69) · rebond 53% (37/67)
      · −2.0% : fill 87% (60/69) · rebond 59% (34/60)
      · −3.0% : fill 83% (55/69) · rebond 57% (32/55)
      · −4.0% : fill 65% (42/69) · rebond 67% (26/42)
      · −5.0% : fill 55% (35/69) · rebond 76% (24/35)
   - **flat** (13 séances) :
      · −1.0% : fill 97% (12/13) · rebond 90% (9/12)
      · −2.0% : fill 61% (9/13) · rebond 87% (6/9)
      · −3.0% : fill 35% (3/13) · rebond 100% (3/3)
      · −4.0% : fill 30% (2/13) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/13) · rebond 0% (0/0)
   - **gap-up** (77 séances) :
      · −1.0% : fill 45% (34/77) · rebond 69% (20/34)
      · −2.0% : fill 25% (19/77) · rebond 77% (15/19)
      · −3.0% : fill 24% (16/77) · rebond 70% (11/16)
      · −4.0% : fill 17% (10/77) · rebond 71% (6/10)
      · −5.0% : fill 16% (9/77) · rebond 85% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 71% si les 15 1res min sont vertes (73 cas) · 23% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:50** → P(séance verte=clôture>ouverture) 82% si début vert vs 6% si rouge (base 45% · écart 76 pts) ; prédictivité sature ensuite (plafond brut 213min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=87) : tient le vert **82%** · continue >prix actuel 48% ; creux résiduel méd -1.38% (q20 -2.82%) → **SL/trailing à −2.82%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.72% / q75 +3.03% → **scale +1.72% / runner +3.03%**, sortie à la clôture
  - **si ROUGE au coude** (n=73) : edge inversé — récupère vert seulement **6%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.94%** (au-delà de la MAE q10 -4.94%), cible rebond +1.74% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.16% .. +4.68%] · haut q95 +6.04% · bas q05 -4.48%
   - 60min (n=160) : retour [-4.4% .. +5.34%] · haut q95 +6.55% · bas q05 -5.33%
   - 2h (n=160) : retour [-4.86% .. +6.65%] · haut q95 +7.73% · bas q05 -5.84%
   - 4h (n=160) : retour [-5.47% .. +7.42%] · haut q95 +8.6% · bas q05 -6.92%
   - 6h (n=160) : retour [-6.01% .. +6.83%] · haut q95 +9.0% · bas q05 -7.14%
   - session (n=160) : retour [-7.56% .. +7.84%] · haut q95 +9.39% · bas q05 -8.23%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0% / strong 5.0%) · base = 8 séances trend-up (n_eff 5.5)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **16%**. Lecture précoce 30 min : signature présente → 9% vs absente 2% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.96% (p75 1.84% / p90 2.17%) · ~4.0 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **80%** (reprise méd 14.9 min, n=37)
   - −1.0% → **72%** (reprise méd 30.0 min, n=17)
   - −1.5% → **57%** (reprise méd 48.62 min, n=13)
   - −2.0% → **85%** (reprise méd 120.86 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.17%** (p90, défaut prudent ; serré/agressif −1.84%) ; extension open→close méd +7.84% (q75 +8.68% / q95 +9.89%), MFE méd +8.72% / q90 +10.39%
   - Échelle scale-out : +8.72% (33%) / +9.19% (33%) / +10.39% (34%)
- **DÉSARMER** : repli > **−2.17%** depuis le plus-haut = décay → P(retournement) **18%** (préavis méd 100.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.39% : P(retournement après) 0% (mèche méd 1.08%)
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
- **intraday** : ❄️ GELÉ jusqu'au 2026-08-11 — SMCI earnings (J-1 sess · earnings)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-11 — SMCI earnings (J-1 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-11 — SMCI earnings (J-1 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 63.8  _(momentum haussier)_
- **ADX** : 15.4  _(pas de tendance nette)_
- **MACD** : hist 0.561  _(pas de croisement recent)_
- **BB** : %B 0.81 · largeur 35.6%
- **ATR** : 2.55 (74.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.059  _(distribution)_
- **Vol ratio** : 1.2  _(volume normal)_
- **Choppiness** : 58.1  _(transition)_
- **MA** : MA20 28.36 · MA50 31.66 · MA200 32.07  _(prix > MA20)_
- **Dist MA** : MA20 +10.9% · MA50 -0.6% · MA200 -1.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92318 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
