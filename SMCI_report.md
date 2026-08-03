# SMCI

**Generated** : 2026-08-03T21:59:53.840097+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $28.64  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $28.64 (+2.9% vs entrée) · entrée $27.84 · stop $27.11 · T1 $28.79 · R/R 1.3  
> ↳ P(T1 av. stop) 23 % _(réel 5 s)_ · EV/risk -0.018 _(réel 5 s)_ (GBM 0.003) · ¼-Kelly 0.011 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.61% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.020 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $27.65–$28.03 (mid $27.84)
- Spot actuel : $28.64 (+2.9% au-dessus de la zone — repli à attendre)
- Stop : $27.11 (stop swing_plan-based (-14.6%))
- Targets : T1 $28.79 · R/R 1.3 | T2 $29.74 · R/R 2.6 | T3 $30.69 · R/R 3.9
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $27.11


## Edge, scénarios & sizing

- EV/risk : 0.003 | EV/share : $0.002 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 24 % | T3 24 %
- Kelly (position) : f* 0.046 | ¼-Kelly 0.011 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 33.2 | bear 7.7 | side 59.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 286.0 (= 10 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.796% → cible +3.411% / stop −2.606%, p_fill 52%, n_eff≈19.9) : P(cible|rempli) **23%** · **EV/risk -0.018** (×p_fill ; si rempli -0.09% du capital)
  - **swing** (entrée dip −6.154% → cible +7.626% / stop −9.0%, p_fill 39%, n_eff≈15.2) : P(cible|rempli) **23%** · **EV/risk -0.223** (×p_fill ; si rempli -5.13% du capital)
  - **deep** (entrée dip −9.511% → cible +10.785% / stop −14.0%, p_fill 39%, n_eff≈15.2) : P(cible|rempli) **60%** · **EV/risk +0.025** (×p_fill ; si rempli +0.91% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→76% · +2.0%→62% · +3.0%→44% · +5.0%→25% · +8.0%→11%
- Range intraday médian 6.47% (p90 10.14%) · excursion haute méd. +2.55% / basse méd. −2.68%
- Profil de vol intra : ouverture 3.999% vs midi 1.228% vs clôture 1.596% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 17% · trend ↑0%/↓1% ; spike-down 68% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.127 ; mean-reverting — autocorr -0.042)_ ; drift intra méd. -0.515% ; recovery-V 15%
- **σ réalisé intraday** 4.219% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 44% / bas 62% / whipsaw 10%
- POC intraday (dernière séance, temps-au-prix) : 28.2242 (VA 27.8122–28.4303 ; dernier close 28.39)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 35% · rebond 78% · **stop −4.6%** sous le fill (sous le bruit) · cible +2.22% · R/R 0.48 (high win-rate)
- Gaps overnight (n=159) : méd. 0.31% · baisse 45% (gap-down >1% 32% · >2% 19%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −2.44%) · haut méd +0.94% · range méd 1.99%
- Excursion ouverture 15min (n=160) : bas méd −1.1% (p90 −3.28%) · haut méd +1.36% · range méd 2.79%
- Excursion ouverture 30min (n=160) : bas méd −1.37% (p90 −3.83%) · haut méd +1.47% · range méd 3.75%
- Excursion ouverture 60min (n=160) : bas méd −1.88% (p90 −5.03%) · haut méd +1.63% · range méd 4.4%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 28.39 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 77% (125/159) · gap 41% · délai 0.0min · rebond 55% (72/125) (MFE +1.2%)
   - −1.0% : fill 30min 56% · séance 72% (114/159) · gap 32% · délai 0.0min · rebond 58% (66/114) (MFE +1.23%)
   - −1.5% : fill 30min 45% · séance 64% (98/159) · gap 26% · délai 0.1min · rebond 60% (59/98) (MFE +1.34%)
   - −2.0% : fill 30min 42% · séance 54% (87/159) · gap 19% · délai 0.1min · rebond 62% (54/87) (MFE +1.56%)
   - −3.0% : fill 30min 29% · séance 49% (71/159) · gap 14% · délai 15.6min · rebond 58% (43/71) (MFE +1.64%)
   - −4.0% : fill 30min 23% · séance 40% (53/159) · gap 8% · délai 15.4min · rebond 68% (33/53) (MFE +1.68%)
   - −5.0% : fill 30min 17% · séance 35% (44/159) · gap 5% · délai 39.0min · rebond 78% (31/44) (MFE +2.22%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.52% (p90 −2.27%) → stop au-delà de −1.15% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.54% (p90 −3.54%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −2.93%) → stop au-delà de −1.61% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=865 jambes) : jambe baissière méd −1.2% (p90 −2.88%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 95% (68/70) · rebond 49% (37/68)
      · −2.0% : fill 86% (60/70) · rebond 56% (34/60)
      · −3.0% : fill 81% (53/70) · rebond 53% (30/53)
      · −4.0% : fill 70% (42/70) · rebond 67% (26/42)
      · −5.0% : fill 59% (35/70) · rebond 76% (24/35)
   - **flat** (13 séances) :
      · −1.0% : fill 96% (12/13) · rebond 87% (9/12)
      · −2.0% : fill 45% (8/13) · rebond 76% (5/8)
      · −3.0% : fill 11% (2/13) · rebond 100% (2/2)
      · −4.0% : fill 4% (1/13) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/13) · rebond 0% (0/0)
   - **gap-up** (76 séances) :
      · −1.0% : fill 49% (34/76) · rebond 69% (20/34)
      · −2.0% : fill 27% (19/76) · rebond 77% (15/19)
      · −3.0% : fill 25% (16/76) · rebond 70% (11/16)
      · −4.0% : fill 18% (10/76) · rebond 71% (6/10)
      · −5.0% : fill 17% (9/76) · rebond 85% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 70% si les 15 1res min sont vertes (73 cas) · 19% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:10** → P(séance verte=clôture>ouverture) 78% si début vert vs 10% si rouge (base 43% · écart 68 pts) ; prédictivité sature ensuite (plafond brut 212min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **78%** · continue >prix actuel 44% ; creux résiduel méd -1.91% (q20 -3.24%) → **SL/trailing à −3.24%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.62% / q75 +2.87% → **scale +1.62% / runner +2.87%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **10%** (continue à baisser 56%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.52%** (au-delà de la MAE q10 -5.52%), cible rebond +1.86% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.23% .. +4.68%] · haut q95 +6.28% · bas q05 -4.53%
   - 60min (n=160) : retour [-4.52% .. +5.51%] · haut q95 +6.59% · bas q05 -5.35%
   - 2h (n=160) : retour [-5.16% .. +6.65%] · haut q95 +8.38% · bas q05 -5.85%
   - 4h (n=160) : retour [-5.66% .. +7.45%] · haut q95 +8.72% · bas q05 -6.92%
   - 6h (n=160) : retour [-6.45% .. +6.88%] · haut q95 +9.38% · bas q05 -7.72%
   - session (n=160) : retour [-7.81% .. +7.85%] · haut q95 +9.46% · bas q05 -8.41%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0% / strong 5.0%) · base = 8 séances trend-up (n_eff 5.5)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **18%**. Lecture précoce 30 min : signature présente → 9% vs absente 2% (base 5%)
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
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 52.5  _(neutre)_
- **ADX** : 16.6  _(pas de tendance nette)_
- **MACD** : hist 0.359  _(pas de croisement recent)_
- **BB** : %B 0.63 · largeur 30.0%
- **ATR** : 2.42 (70.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.021  _(neutre)_
- **Vol ratio** : 0.54  _(volume atone)_
- **Choppiness** : 49.3  _(transition)_
- **MA** : MA20 27.6 · MA50 32.29 · MA200 32.65  _(prix > MA20)_
- **Dist MA** : MA20 +3.8% · MA50 -11.3% · MA200 -12.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92990 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
