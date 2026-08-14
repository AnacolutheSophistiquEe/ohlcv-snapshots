# HOOD

**Generated** : 2026-08-14T00:30:54.302150+00:00  
**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $99.37  

> 🟡 **WAIT-FOR-DIP** — spot +1.4 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $99.37 (+1.4% vs entrée) · entrée $97.95 · stop $95.01 · T1 $103.28 · R/R 1.81  
> ↳ P(T1 av. stop) 7 % _(réel 5 s)_ · EV/risk 0.033 _(réel 5 s)_ (GBM 0.031) · ¼-Kelly 0.006 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.160 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $97.57–$98.33 (mid $97.95)
- Spot actuel : $99.37 (+1.4% au-dessus de la zone — repli à attendre)
- Stop : $95.01 (stop swing_plan-based (-8.11%))
- Targets : T1 $103.28 · R/R 1.81 | T2 $103.47 · R/R 1.88 | T3 $103.66 · R/R 1.94
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $95.01


## Edge, scénarios & sizing

- EV/risk : 0.031 | EV/share : $0.091 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 20 % | T2 20 % | T3 20 %
- Kelly (position) : f* 0.025 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 30.0 | bear 62.8 | side 7.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 497.0 (= 5 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.423% → cible +5.433% / stop −3.0%, p_fill 71%, n_eff≈30.1) : P(cible|rempli) **7%** · **EV/risk +0.033** (×p_fill ; si rempli +0.14% du capital)
  - **swing** (entrée dip −3.139% → cible +4.343% / stop −5.133%, p_fill 58%, n_eff≈22.8) : P(cible|rempli) **51%** · **EV/risk -0.064** (×p_fill ; si rempli -0.57% du capital)
  - **deep** (entrée dip −4.853% → cible +6.142% / stop −7.837%, p_fill 62%, n_eff≈21.2) : P(cible|rempli) **38%** · **EV/risk -0.237** (×p_fill ; si rempli -3.00% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→81% · +2.0%→56% · +3.0%→34% · +5.0%→20% · +8.0%→6%
- Range intraday médian 5.05% (p90 8.92%) · excursion haute méd. +2.11% / basse méd. −2.21%
- Profil de vol intra : ouverture 3.642% vs midi 1.035% vs clôture 1.125% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 17% · trend ↑1%/↓0% ; spike-down 69% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.1 ; neutre — autocorr 0.012)_ ; drift intra méd. -0.104% ; recovery-V 35%
- **σ réalisé intraday** 3.605% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 44% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 93.5426 (VA 93.3754–93.9329 ; dernier close 94.39)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 30% · rebond 79% · **stop −4.7%** sous le fill (sous le bruit) · cible +2.33% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. 0.02% · baisse 50% (gap-down >1% 33% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.85% (p90 −2.61%) · haut méd +0.89% · range méd 2.11%
- Excursion ouverture 15min (n=160) : bas méd −1.1% (p90 −3.84%) · haut méd +1.25% · range méd 2.83%
- Excursion ouverture 30min (n=160) : bas méd −1.52% (p90 −4.0%) · haut méd +1.72% · range méd 3.45%
- Excursion ouverture 60min (n=160) : bas méd −1.88% (p90 −4.53%) · haut méd +1.74% · range méd 3.9%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 94.39 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 72% · séance 80% (124/159) · gap 41% · délai 0.0min · rebond 57% (65/124) (MFE +1.39%)
   - −1.0% : fill 30min 63% · séance 70% (109/159) · gap 33% · délai 0.0min · rebond 63% (64/109) (MFE +1.51%)
   - −1.5% : fill 30min 51% · séance 61% (100/159) · gap 23% · délai 0.2min · rebond 61% (58/100) (MFE +1.74%)
   - −2.0% : fill 30min 42% · séance 51% (89/159) · gap 16% · délai 0.3min · rebond 68% (56/89) (MFE +1.54%)
   - −3.0% : fill 30min 30% · séance 40% (68/159) · gap 8% · délai 6.6min · rebond 76% (47/68) (MFE +2.11%)
   - −4.0% : fill 30min 18% · séance 30% (51/159) · gap 4% · délai 11.9min · rebond 79% (34/51) (MFE +2.33%)
   - −5.0% : fill 30min 11% · séance 19% (33/159) · gap 2% · délai 19.0min · rebond 76% (25/33) (MFE +2.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.62% (p90 −2.54%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.62% (p90 −2.43%) → stop au-delà de −1.56% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −2.44%) → stop au-delà de −1.61% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=754 jambes) : jambe baissière méd −1.14% (p90 −2.83%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (72 séances) :
      · −1.0% : fill 97% (69/72) · rebond 53% (36/69)
      · −2.0% : fill 84% (60/72) · rebond 63% (36/60)
      · −3.0% : fill 69% (49/72) · rebond 73% (33/49)
      · −4.0% : fill 55% (39/72) · rebond 81% (28/39)
      · −5.0% : fill 36% (27/72) · rebond 72% (20/27)
   - **flat** (20 séances) :
      · −1.0% : fill 64% (14/20) · rebond 80% (9/14)
      · −2.0% : fill 40% (11/20) · rebond 61% (7/11)
      · −3.0% : fill 14% (6/20) · rebond 23% (2/6)
      · −4.0% : fill 13% (5/20) · rebond 16% (1/5)
      · −5.0% : fill 6% (3/20) · rebond 82% (2/3)
   - **gap-up** (67 séances) :
      · −1.0% : fill 44% (26/67) · rebond 78% (19/26)
      · −2.0% : fill 22% (18/67) · rebond 88% (13/18)
      · −3.0% : fill 18% (13/67) · rebond 98% (12/13)
      · −4.0% : fill 10% (7/67) · rebond 88% (5/7)
      · −5.0% : fill 5% (3/67) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 62% si les 15 1res min sont vertes (75 cas) · 35% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **31min** → P(séance verte=clôture>ouverture) 70% si début vert vs 28% si rouge (base 48% · écart 41 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **70%** · continue >prix actuel 49% ; creux résiduel méd -1.55% (q20 -3.14%) → **SL/trailing à −3.14%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.69% / q75 +3.19% → **scale +1.69% / runner +3.19%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **28%** (continue à baisser 50%) → **RÉDUIRE ~72%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.04%** (au-delà de la MAE q10 -4.04%), cible rebond +2.05% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.53% .. +4.05%] · haut q95 +4.42% · bas q05 -5.25%
   - 60min (n=160) : retour [-3.66% .. +4.35%] · haut q95 +5.17% · bas q05 -5.41%
   - 2h (n=160) : retour [-4.63% .. +4.84%] · haut q95 +6.53% · bas q05 -5.84%
   - 4h (n=160) : retour [-4.68% .. +5.77%] · haut q95 +7.77% · bas q05 -6.45%
   - 6h (n=160) : retour [-5.73% .. +6.35%] · haut q95 +7.77% · bas q05 -7.09%
   - session (n=160) : retour [-5.27% .. +6.07%] · haut q95 +7.77% · bas q05 -7.43%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.1% des séances sont trend-up (mild 0% / strong 8.1%) · base = 13 séances trend-up (n_eff 9.8)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **34%**. Lecture précoce 30 min : signature présente → 16% vs absente 3% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.92% (p75 1.42% / p90 2.12%) · ~4.0 replis/séance, durée méd 36.99 min. P(nouveau plus-haut après repli) :
   - −0.5% → **82%** (reprise méd 20.0 min, n=47)
   - −1.0% → **70%** (reprise méd 32.75 min, n=22)
   - −1.5% → **45%** (reprise méd 52.28 min, n=11)
   - −2.0% → **25%** (reprise méd None min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−2.12%** (p90, défaut prudent ; serré/agressif −1.42%) ; extension open→close méd +6.08% (q75 +9.69% / q95 +13.38%), MFE méd +6.77% / q90 +14.84%
   - Échelle scale-out : +6.77% (33%) / +11.24% (33%) / +14.84% (34%)
- **DÉSARMER** : repli > **−2.12%** depuis le plus-haut = décay → P(retournement) **75%** (préavis méd 165.69 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +14.84% : P(retournement après) 0% (mèche méd 5.8%)
- **CONTEXTE** : la dernière heure tient les gains 78% du temps (retour médian dernière heure +0.61%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 57.8  _(momentum haussier)_
- **ADX** : 18.2  _(pas de tendance nette)_
- **MACD** : hist 0.505  _(bullish_recent)_
- **BB** : %B 0.7 · largeur 22.6%
- **ATR** : 4.94 (27.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.158  _(distribution)_
- **Vol ratio** : 0.87  _(volume normal)_
- **Choppiness** : 53.9  _(transition)_
- **MA** : MA20 95.09 · MA50 98.84 · MA200 97.51  _(prix > MA20)_
- **Dist MA** : MA20 +4.5% · MA50 +0.5% · MA200 +1.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91605 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
