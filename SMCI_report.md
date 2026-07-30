# SMCI

**Generated** : 2026-07-30T21:59:02.607271+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $27.73  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $27.73 (+2.1% vs entrée) · entrée $27.16 · stop $26.47 · T1 $28.08 · R/R 1.33  
> ↳ P(T1 av. stop) 22 % _(réel 5 s)_ · EV/risk -0.142 _(réel 5 s)_ (GBM 0.02) · ¼-Kelly 0.014 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.54% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

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

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $26.97–$27.34 (mid $27.16)
- Spot actuel : $27.73 (+2.1% au-dessus de la zone — repli à attendre)
- Stop : $26.47 (stop swing_plan-based (-8.18%))
- Targets : T1 $28.08 · R/R 1.33 | T2 $29.01 · R/R 2.68 | T3 $29.93 · R/R 4.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $26.47


## Edge, scénarios & sizing

- EV/risk : 0.02 | EV/share : $0.014 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 25 % | T3 25 %
- Kelly (position) : f* 0.057 | ¼-Kelly 0.014 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 64.5 | bear 6.2 | side 29.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 139.0 (= 5 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.073% → cible +3.405% / stop −2.54%, p_fill 64%, n_eff≈25.3) : P(cible|rempli) **22%** · **EV/risk -0.142** (×p_fill ; si rempli -0.56% du capital)
  - **swing** (entrée dip −4.547% → cible +7.613% / stop −3.806%, p_fill 44%, n_eff≈20.9) : P(cible|rempli) **24%** · **EV/risk -0.159** (×p_fill ; si rempli -1.39% du capital)
  - **deep** (entrée dip −7.036% → cible +10.766% / stop −5.383%, p_fill 60%, n_eff≈21.3) : P(cible|rempli) **33%** · **EV/risk -0.070** (×p_fill ; si rempli -0.63% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→76% · +2.0%→62% · +3.0%→44% · +5.0%→26% · +8.0%→12%
- Range intraday médian 6.47% (p90 10.14%) · excursion haute méd. +2.55% / basse méd. −2.66%
- Profil de vol intra : ouverture 3.999% vs midi 1.233% vs clôture 1.589% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 18% · trend ↑0%/↓1% ; spike-down 69% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.134 ; mean-reverting — autocorr -0.049)_ ; drift intra méd. -0.67% ; recovery-V 16%
- **σ réalisé intraday** 4.215% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 43% / bas 63% / whipsaw 11%
- POC intraday (dernière séance, temps-au-prix) : 26.773 (VA 26.541–27.237 ; dernier close 25.7)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 36% · rebond 78% · **stop −4.6%** sous le fill (sous le bruit) · cible +2.22% · R/R 0.48 (high win-rate)
- Gaps overnight (n=159) : méd. 0.27% · baisse 46% (gap-down >1% 34% · >2% 20%)
- Excursion ouverture 5min (n=160) : bas méd −0.81% (p90 −2.49%) · haut méd +0.93% · range méd 1.99%
- Excursion ouverture 15min (n=160) : bas méd −1.24% (p90 −3.33%) · haut méd +1.24% · range méd 2.79%
- Excursion ouverture 30min (n=160) : bas méd −1.37% (p90 −3.86%) · haut méd +1.4% · range méd 3.66%
- Excursion ouverture 60min (n=160) : bas méd −1.88% (p90 −4.64%) · haut méd +1.57% · range méd 4.33%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 25.7 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 78% (125/159) · gap 42% · délai 0.0min · rebond 54% (71/125) (MFE +1.18%)
   - −1.0% : fill 30min 58% · séance 72% (113/159) · gap 34% · délai 0.0min · rebond 57% (65/113) (MFE +1.22%)
   - −1.5% : fill 30min 46% · séance 64% (97/159) · gap 27% · délai 0.0min · rebond 58% (58/97) (MFE +1.21%)
   - −2.0% : fill 30min 43% · séance 56% (87/159) · gap 20% · délai 0.1min · rebond 62% (54/87) (MFE +1.56%)
   - −3.0% : fill 30min 30% · séance 51% (71/159) · gap 14% · délai 15.6min · rebond 58% (43/71) (MFE +1.64%)
   - −4.0% : fill 30min 24% · séance 42% (53/159) · gap 9% · délai 15.4min · rebond 68% (33/53) (MFE +1.68%)
   - −5.0% : fill 30min 17% · séance 36% (44/159) · gap 6% · délai 39.0min · rebond 78% (31/44) (MFE +2.22%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.51% (p90 −2.44%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.54% (p90 −3.8%) → stop au-delà de −1.72% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −3.05%) → stop au-delà de −1.62% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=860 jambes) : jambe baissière méd −1.2% (p90 −2.88%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 95% (68/70) · rebond 49% (37/68)
      · −2.0% : fill 86% (60/70) · rebond 56% (34/60)
      · −3.0% : fill 81% (53/70) · rebond 53% (30/53)
      · −4.0% : fill 70% (42/70) · rebond 67% (26/42)
      · −5.0% : fill 59% (35/70) · rebond 76% (24/35)
   - **flat** (14 séances) :
      · −1.0% : fill 94% (12/14) · rebond 87% (9/12)
      · −2.0% : fill 44% (8/14) · rebond 76% (5/8)
      · −3.0% : fill 11% (2/14) · rebond 100% (2/2)
      · −4.0% : fill 4% (1/14) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/14) · rebond 0% (0/0)
   - **gap-up** (75 séances) :
      · −1.0% : fill 49% (33/75) · rebond 66% (19/33)
      · −2.0% : fill 29% (19/75) · rebond 77% (15/19)
      · −3.0% : fill 27% (16/75) · rebond 70% (11/16)
      · −4.0% : fill 20% (10/75) · rebond 71% (6/10)
      · −5.0% : fill 18% (9/75) · rebond 85% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 69% si les 15 1res min sont vertes (73 cas) · 20% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:10** → P(séance verte=clôture>ouverture) 78% si début vert vs 10% si rouge (base 43% · écart 67 pts) ; prédictivité sature ensuite (plafond brut 212min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **78%** · continue >prix actuel 46% ; creux résiduel méd -1.74% (q20 -3.39%) → **SL/trailing à −3.39%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.69% / q75 +2.94% → **scale +1.69% / runner +2.94%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **10%** (continue à baisser 58%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.55%** (au-delà de la MAE q10 -5.55%), cible rebond +1.8% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.25% .. +4.76%] · haut q95 +6.5% · bas q05 -4.54%
   - 60min (n=160) : retour [-4.57% .. +5.57%] · haut q95 +6.6% · bas q05 -5.38%
   - 2h (n=160) : retour [-5.25% .. +6.66%] · haut q95 +8.38% · bas q05 -5.86%
   - 4h (n=160) : retour [-5.77% .. +7.49%] · haut q95 +8.76% · bas q05 -6.93%
   - 6h (n=160) : retour [-6.45% .. +6.9%] · haut q95 +9.55% · bas q05 -7.82%
   - session (n=160) : retour [-7.9% .. +7.85%] · haut q95 +9.55% · bas q05 -8.47%


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
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 48.5  _(neutre)_
- **ADX** : 18.7  _(pas de tendance nette)_
- **MACD** : hist 0.332  _(pas de croisement recent)_
- **BB** : %B 0.53 · largeur 29.8%
- **ATR** : 2.3 (66.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.075  _(distribution)_
- **Vol ratio** : 0.85  _(volume normal)_
- **Choppiness** : 47.4  _(transition)_
- **MA** : MA20 27.47 · MA50 32.43 · MA200 32.91  _(prix > MA20)_
- **Dist MA** : MA20 +1.0% · MA50 -14.5% · MA200 -15.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92690 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
