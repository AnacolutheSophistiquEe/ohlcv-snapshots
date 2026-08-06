# SMCI

**Generated** : 2026-08-06T22:00:26.009642+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $29.38  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-11 — SMCI earnings (J-4 sess · earnings)  
> ↳ spot $29.38 (+7.8% vs entrée) · entrée $27.26 · stop $24.83 · T1 $29.43 · R/R 0.89  
> ↳ P(T1 av. stop) 46 % _(réel 5 s)_ · EV/risk -0.045 _(réel 5 s)_ (GBM 0.004) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.040 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $26.82–$27.69 (mid $27.26)
- Spot actuel : $29.38 (+7.8% au-dessus de la zone — repli à attendre)
- Stop : $24.83 (stop swing_plan-based (-15.49%))
- Targets : T1 $29.43 · R/R 0.89 | T2 $31.61 · R/R 1.79 | T3 $33.78 · R/R 2.68
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $24.83


## Edge, scénarios & sizing

- EV/risk : 0.004 | EV/share : $0.009 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 18 % | T3 11 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 45.6 | bear 9.1 | side 45.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 382.0 (= 13 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.283% → cible +3.569% / stop −2.561%, p_fill 46%, n_eff≈17.8) : P(cible|rempli) **17%** · **EV/risk -0.038** (×p_fill ; si rempli -0.21% du capital)
  - **swing** (entrée dip −7.235% → cible +7.982% / stop −8.899%, p_fill 33%, n_eff≈12.1) : P(cible|rempli) **46%** · **EV/risk -0.045** (×p_fill ; si rempli -1.23% du capital)
  - **deep** (entrée dip −11.177% → cible +11.288% / stop −13.941%, p_fill 27%, n_eff≈11.7) : P(cible|rempli) **50%** · **EV/risk -0.017** (×p_fill ; si rempli -0.90% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→76% · +2.0%→62% · +3.0%→45% · +5.0%→26% · +8.0%→11%
- Range intraday médian 6.69% (p90 10.14%) · excursion haute méd. +2.55% / basse méd. −2.68%
- Profil de vol intra : ouverture 4.028% vs midi 1.227% vs clôture 1.62% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 18% · trend ↑0%/↓1% ; spike-down 70% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.14 ; mean-reverting — autocorr -0.059)_ ; drift intra méd. -0.243% ; recovery-V 24%
- **σ réalisé intraday** 4.108% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 58% / whipsaw 9%
- POC intraday (dernière séance, temps-au-prix) : 31.3151 (VA 30.8981–31.3846 ; dernier close 30.32)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 33% · rebond 78% · **stop −4.6%** sous le fill (sous le bruit) · cible +2.22% · R/R 0.48 (high win-rate)
- Gaps overnight (n=159) : méd. 0.29% · baisse 44% (gap-down >1% 32% · >2% 18%)
- Excursion ouverture 5min (n=160) : bas méd −0.81% (p90 −2.63%) · haut méd +0.92% · range méd 2.0%
- Excursion ouverture 15min (n=160) : bas méd −1.28% (p90 −3.26%) · haut méd +1.36% · range méd 2.81%
- Excursion ouverture 30min (n=160) : bas méd −1.62% (p90 −3.79%) · haut méd +1.45% · range méd 3.72%
- Excursion ouverture 60min (n=160) : bas méd −1.92% (p90 −4.89%) · haut méd +1.58% · range méd 4.31%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 30.32 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 76% (124/159) · gap 40% · délai 0.0min · rebond 55% (73/124) (MFE +1.2%)
   - −1.0% : fill 30min 56% · séance 72% (114/159) · gap 32% · délai 0.0min · rebond 60% (67/114) (MFE +1.27%)
   - −1.5% : fill 30min 46% · séance 64% (99/159) · gap 25% · délai 0.1min · rebond 62% (61/99) (MFE +1.48%)
   - −2.0% : fill 30min 43% · séance 55% (88/159) · gap 18% · délai 0.6min · rebond 64% (55/88) (MFE +1.6%)
   - −3.0% : fill 30min 31% · séance 50% (73/159) · gap 13% · délai 10.6min · rebond 61% (45/73) (MFE +1.79%)
   - −4.0% : fill 30min 22% · séance 40% (54/159) · gap 8% · délai 21.7min · rebond 70% (34/54) (MFE +1.68%)
   - −5.0% : fill 30min 16% · séance 33% (44/159) · gap 5% · délai 39.0min · rebond 78% (31/44) (MFE +2.22%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −2.05%) → stop au-delà de −1.41% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.6% (p90 −3.22%) → stop au-delà de −1.89% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.69% (p90 −2.74%) → stop au-delà de −1.92% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=866 jambes) : jambe baissière méd −1.19% (p90 −2.87%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (69 séances) :
      · −1.0% : fill 95% (67/69) · rebond 51% (37/67)
      · −2.0% : fill 87% (60/69) · rebond 57% (34/60)
      · −3.0% : fill 82% (54/69) · rebond 55% (31/54)
      · −4.0% : fill 67% (42/69) · rebond 67% (26/42)
      · −5.0% : fill 57% (35/69) · rebond 76% (24/35)
   - **flat** (14 séances) :
      · −1.0% : fill 97% (13/14) · rebond 91% (10/13)
      · −2.0% : fill 60% (9/14) · rebond 87% (6/9)
      · −3.0% : fill 35% (3/14) · rebond 100% (3/3)
      · −4.0% : fill 29% (2/14) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/14) · rebond 0% (0/0)
   - **gap-up** (76 séances) :
      · −1.0% : fill 47% (34/76) · rebond 69% (20/34)
      · −2.0% : fill 26% (19/76) · rebond 77% (15/19)
      · −3.0% : fill 24% (16/76) · rebond 70% (11/16)
      · −4.0% : fill 18% (10/76) · rebond 71% (6/10)
      · −5.0% : fill 16% (9/76) · rebond 85% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 70% si les 15 1res min sont vertes (72 cas) · 24% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:50** → P(séance verte=clôture>ouverture) 85% si début vert vs 6% si rouge (base 45% · écart 79 pts) ; prédictivité sature ensuite (plafond brut 212min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=85) : tient le vert **85%** · continue >prix actuel 48% ; creux résiduel méd -1.38% (q20 -2.58%) → **SL/trailing à −2.58%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.71% / q75 +3.05% → **scale +1.71% / runner +3.05%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **6%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.94%** (au-delà de la MAE q10 -4.94%), cible rebond +1.73% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.18% .. +4.68%] · haut q95 +6.05% · bas q05 -4.51%
   - 60min (n=160) : retour [-4.45% .. +5.41%] · haut q95 +6.58% · bas q05 -5.33%
   - 2h (n=160) : retour [-4.91% .. +6.65%] · haut q95 +8.15% · bas q05 -5.85%
   - 4h (n=160) : retour [-5.53% .. +7.42%] · haut q95 +8.66% · bas q05 -6.92%
   - 6h (n=160) : retour [-6.1% .. +6.85%] · haut q95 +9.15% · bas q05 -7.39%
   - session (n=160) : retour [-7.66% .. +7.84%] · haut q95 +9.42% · bas q05 -8.3%


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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-11 — SMCI earnings (J-4 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-11 — SMCI earnings (J-4 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 62.1  _(momentum haussier)_
- **ADX** : 15.5  _(pas de tendance nette)_
- **MACD** : hist 0.492  _(pas de croisement recent)_
- **BB** : %B 0.65 · largeur 33.1%
- **ATR** : 2.43 (70.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.04  _(neutre)_
- **Vol ratio** : 0.61  _(volume normal)_
- **Choppiness** : 51.1  _(transition)_
- **MA** : MA20 28.03 · MA50 32.0 · MA200 32.31  _(prix > MA20)_
- **Dist MA** : MA20 +4.8% · MA50 -8.2% · MA200 -9.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92455 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
