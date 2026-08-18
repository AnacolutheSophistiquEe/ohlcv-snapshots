# HOOD

**Generated** : 2026-08-18T00:30:58.991393+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $96.25  

> 🟡 **WAIT-FOR-DIP** — spot +1.5 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $96.25 (+1.5% vs entrée) · entrée $94.85 · stop $90.38 · T1 $98.81 · R/R 0.89  
> ↳ P(T1 av. stop) 51 % _(réel 5 s)_ · EV/risk 0.011 _(réel 5 s)_ (GBM -0.047) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.140 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $94.06–$95.64 (mid $94.85)
- Spot actuel : $96.25 (+1.5% au-dessus de la zone — repli à attendre)
- Stop : $90.38 (stop swing_plan-based (-6.1%))
- Targets : T1 $98.81 · R/R 0.89 | T2 $102.78 · R/R 1.77 | T3 $106.74 · R/R 2.66
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $90.38


## Edge, scénarios & sizing

- EV/risk : -0.047 | EV/share : $-0.209 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 50 % | T2 26 % | T3 15 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 73.6 | bear 18.1 | side 8.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 385.0 (= 4 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.66% → cible +1.869% / stop −3.0%, p_fill 76%, n_eff≈32.1) : P(cible|rempli) **41%** · **EV/risk -0.074** (×p_fill ; si rempli -0.29% du capital)
  - **swing** (entrée dip −1.46% → cible +4.179% / stop −4.709%, p_fill 77%, n_eff≈34.3) : P(cible|rempli) **51%** · **EV/risk +0.011** (×p_fill ; si rempli +0.07% du capital)
  - **deep** (entrée dip −2.25% → cible +5.91% / stop −7.121%, p_fill 81%, n_eff≈31.6) : P(cible|rempli) **46%** · **EV/risk -0.159** (×p_fill ; si rempli -1.39% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→81% · +2.0%→57% · +3.0%→35% · +5.0%→20% · +8.0%→6%
- Range intraday médian 5.04% (p90 8.92%) · excursion haute méd. +2.16% / basse méd. −2.21%
- Profil de vol intra : ouverture 3.679% vs midi 1.028% vs clôture 1.134% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 16% · trend ↑1%/↓0% ; spike-down 68% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.107 ; neutre — autocorr 0.001)_ ; drift intra méd. -0.148% ; recovery-V 31%
- **σ réalisé intraday** 3.494% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 40% / bas 47% / whipsaw 10%
- POC intraday (dernière séance, temps-au-prix) : 97.179 (VA 96.217–98.141 ; dernier close 95.53)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 28% · rebond 79% · **stop −4.7%** sous le fill (sous le bruit) · cible +2.33% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. 0.03% · baisse 49% (gap-down >1% 33% · >2% 15%)
- Excursion ouverture 5min (n=160) : bas méd −0.81% (p90 −2.45%) · haut méd +0.85% · range méd 2.16%
- Excursion ouverture 15min (n=160) : bas méd −1.07% (p90 −3.83%) · haut méd +1.2% · range méd 2.82%
- Excursion ouverture 30min (n=160) : bas méd −1.39% (p90 −3.89%) · haut méd +1.71% · range méd 3.45%
- Excursion ouverture 60min (n=160) : bas méd −1.83% (p90 −4.02%) · haut méd +1.74% · range méd 3.9%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 95.53 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 72% · séance 80% (125/159) · gap 41% · délai 0.0min · rebond 57% (65/125) (MFE +1.39%)
   - −1.0% : fill 30min 61% · séance 70% (110/159) · gap 33% · délai 0.0min · rebond 62% (64/110) (MFE +1.51%)
   - −1.5% : fill 30min 51% · séance 59% (100/159) · gap 24% · délai 0.0min · rebond 59% (57/100) (MFE +1.6%)
   - −2.0% : fill 30min 41% · séance 50% (89/159) · gap 15% · délai 0.2min · rebond 69% (56/89) (MFE +1.46%)
   - −3.0% : fill 30min 28% · séance 40% (69/159) · gap 7% · délai 7.1min · rebond 72% (47/69) (MFE +2.0%)
   - −4.0% : fill 30min 17% · séance 28% (51/159) · gap 4% · délai 11.9min · rebond 79% (34/51) (MFE +2.33%)
   - −5.0% : fill 30min 11% · séance 18% (33/159) · gap 2% · délai 19.0min · rebond 76% (25/33) (MFE +2.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.62% (p90 −2.51%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.6% (p90 −2.42%) → stop au-delà de −1.49% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −2.43%) → stop au-delà de −1.57% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=757 jambes) : jambe baissière méd −1.14% (p90 −2.84%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (73 séances) :
      · −1.0% : fill 97% (70/73) · rebond 51% (36/70)
      · −2.0% : fill 84% (61/73) · rebond 65% (37/61)
      · −3.0% : fill 70% (50/73) · rebond 68% (33/50)
      · −4.0% : fill 53% (39/73) · rebond 81% (28/39)
      · −5.0% : fill 35% (27/73) · rebond 72% (20/27)
   - **flat** (20 séances) :
      · −1.0% : fill 64% (14/20) · rebond 80% (9/14)
      · −2.0% : fill 40% (11/20) · rebond 61% (7/11)
      · −3.0% : fill 14% (6/20) · rebond 23% (2/6)
      · −4.0% : fill 13% (5/20) · rebond 16% (1/5)
      · −5.0% : fill 6% (3/20) · rebond 82% (2/3)
   - **gap-up** (66 séances) :
      · −1.0% : fill 44% (26/66) · rebond 80% (19/26)
      · −2.0% : fill 20% (17/66) · rebond 88% (12/17)
      · −3.0% : fill 17% (13/66) · rebond 98% (12/13)
      · −4.0% : fill 9% (7/66) · rebond 88% (5/7)
      · −5.0% : fill 5% (3/66) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 64% si les 15 1res min sont vertes (76 cas) · 33% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **31min** → P(séance verte=clôture>ouverture) 71% si début vert vs 26% si rouge (base 48% · écart 44 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **71%** · continue >prix actuel 47% ; creux résiduel méd -1.56% (q20 -3.01%) → **SL/trailing à −3.01%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.62% / q75 +3.16% → **scale +1.62% / runner +3.16%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **26%** (continue à baisser 50%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.94%** (au-delà de la MAE q10 -3.94%), cible rebond +1.89% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.52% .. +4.01%] · haut q95 +4.34% · bas q05 -5.25%
   - 60min (n=160) : retour [-3.65% .. +4.35%] · haut q95 +5.17% · bas q05 -5.34%
   - 2h (n=160) : retour [-4.57% .. +4.78%] · haut q95 +6.45% · bas q05 -5.71%
   - 4h (n=160) : retour [-4.67% .. +5.76%] · haut q95 +7.43% · bas q05 -6.28%
   - 6h (n=160) : retour [-5.71% .. +6.24%] · haut q95 +7.46% · bas q05 -7.08%
   - session (n=160) : retour [-5.21% .. +6.0%] · haut q95 +7.6% · bas q05 -7.29%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.1% des séances sont trend-up (mild 0% / strong 8.1%) · base = 13 séances trend-up (n_eff 9.8)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **34%**. Lecture précoce 30 min : signature présente → 15% vs absente 3% (base 8%)
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

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 55.9  _(momentum haussier)_
- **ADX** : 16.1  _(pas de tendance nette)_
- **MACD** : hist 0.591  _(bullish_recent)_
- **BB** : %B 0.57 · largeur 21.8%
- **ATR** : 4.47 (17.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.145  _(distribution)_
- **Vol ratio** : 0.59  _(volume atone)_
- **Choppiness** : 50.1  _(transition)_
- **MA** : MA20 94.72 · MA50 99.25 · MA200 97.01  _(prix > MA20)_
- **Dist MA** : MA20 +1.6% · MA50 -3.0% · MA200 -0.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91136 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
