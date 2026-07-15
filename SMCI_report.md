# SMCI

**Generated** : 2026-07-15T22:01:40.127873+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $26.89  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $26.89 (+1.4% vs entrée) · entrée $26.53 · stop $26.00 · T1 $27.36 · R/R 1.57  
> ↳ P(T1 av. stop) 16 % _(réel 5 s)_ · EV/risk -0.249 _(réel 5 s)_ (GBM 0.082) · ¼-Kelly 0.017 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.97% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $26.36–$26.69 (mid $26.53)
- Spot actuel : $26.89 (+1.4% au-dessus de la zone — repli à attendre)
- Stop : $26.00 (stop swing_plan-based (-6.37%))
- Targets : T1 $27.36 · R/R 1.57 | T2 $28.19 · R/R 3.13 | T3 $29.02 · R/R 4.7
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $26.00


## Edge, scénarios & sizing

- EV/risk : 0.082 | EV/share : $0.043 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 27 % | T3 27 %
- Kelly (position) : f* 0.07 | ¼-Kelly 0.017 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.1 | bear 8.9 | side 6.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.353% → cible +3.128% / stop −1.974%, p_fill 73%, n_eff≈28.8) : P(cible|rempli) **16%** · **EV/risk -0.249** (×p_fill ; si rempli -0.67% du capital)
  - **swing** (entrée dip −2.977% → cible +6.994% / stop −3.497%, p_fill 72%, n_eff≈25.8) : P(cible|rempli) **17%** · **EV/risk -0.374** (×p_fill ; si rempli -1.82% du capital)
  - **deep** (entrée dip −4.602% → cible +9.891% / stop −4.945%, p_fill 63%, n_eff≈22.7) : P(cible|rempli) **17%** · **EV/risk -0.362** (×p_fill ; si rempli -2.84% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→81% · +2.0%→65% · +3.0%→48% · +5.0%→31% · +8.0%→12%
- Range intraday médian 6.47% (p90 10.14%) · excursion haute méd. +2.83% / basse méd. −2.56%
- Profil de vol intra : ouverture 3.841% vs midi 1.27% vs clôture 1.519% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 18% · trend ↑0%/↓1% ; spike-down 66% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.141 ; mean-reverting — autocorr -0.05)_ ; drift intra méd. -0.16% ; recovery-V 24%
- **σ réalisé intraday** 4.254% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 66% / whipsaw 13%
- POC intraday (dernière séance, temps-au-prix) : 28.759 (VA 28.603–28.889 ; dernier close 28.33)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 30% · rebond 68% · **stop −4.65%** sous le fill (sous le bruit) · cible +2.15% · R/R 0.46 (high win-rate)
- Gaps overnight (n=159) : méd. 0.29% · baisse 44% (gap-down >1% 30% · >2% 21%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −2.06%) · haut méd +0.97% · range méd 1.96%
- Excursion ouverture 15min (n=160) : bas méd −0.96% (p90 −3.11%) · haut méd +1.36% · range méd 2.67%
- Excursion ouverture 30min (n=160) : bas méd −1.29% (p90 −3.69%) · haut méd +1.47% · range méd 3.51%
- Excursion ouverture 60min (n=160) : bas méd −1.53% (p90 −4.4%) · haut méd +1.77% · range méd 4.26%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 28.33 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 76% (126/159) · gap 38% · délai 0.0min · rebond 57% (73/126) (MFE +1.32%)
   - −1.0% : fill 30min 57% · séance 69% (113/159) · gap 30% · délai 0.0min · rebond 58% (63/113) (MFE +1.18%)
   - −1.5% : fill 30min 46% · séance 63% (98/159) · gap 25% · délai 1.2min · rebond 63% (59/98) (MFE +1.45%)
   - −2.0% : fill 30min 42% · séance 55% (87/159) · gap 21% · délai 1.2min · rebond 66% (55/87) (MFE +1.59%)
   - −3.0% : fill 30min 27% · séance 48% (67/159) · gap 15% · délai 18.9min · rebond 57% (39/67) (MFE +1.76%)
   - −4.0% : fill 30min 19% · séance 38% (49/159) · gap 11% · délai 22.8min · rebond 67% (30/49) (MFE +1.49%)
   - −5.0% : fill 30min 16% · séance 30% (40/159) · gap 7% · délai 22.7min · rebond 68% (26/40) (MFE +2.15%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.5% (p90 −2.1%) → stop au-delà de −1.29% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.54% (p90 −2.7%) → stop au-delà de −1.6% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −2.68%) → stop au-delà de −1.62% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=821 jambes) : jambe baissière méd −1.21% (p90 −2.87%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (68 séances) :
      · −1.0% : fill 93% (66/68) · rebond 51% (36/66)
      · −2.0% : fill 86% (58/68) · rebond 58% (32/58)
      · −3.0% : fill 80% (50/68) · rebond 55% (28/50)
      · −4.0% : fill 68% (40/68) · rebond 69% (25/40)
      · −5.0% : fill 55% (33/68) · rebond 66% (21/33)
   - **flat** (17 séances) :
      · −1.0% : fill 94% (15/17) · rebond 86% (11/15)
      · −2.0% : fill 45% (10/17) · rebond 78% (7/10)
      · −3.0% : fill 10% (2/17) · rebond 100% (2/2)
      · −4.0% : fill 3% (1/17) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/17) · rebond 0% (0/0)
   - **gap-up** (74 séances) :
      · −1.0% : fill 44% (32/74) · rebond 62% (16/32)
      · −2.0% : fill 28% (19/74) · rebond 85% (16/19)
      · −3.0% : fill 26% (15/74) · rebond 60% (9/15)
      · −4.0% : fill 16% (8/74) · rebond 56% (4/8)
      · −5.0% : fill 14% (7/74) · rebond 75% (5/7)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 66% si les 15 1res min sont vertes (74 cas) · 27% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **58min** → P(séance verte=clôture>ouverture) 82% si début vert vs 18% si rouge (base 46% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 212min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **82%** · continue >prix actuel 54% ; creux résiduel méd -1.31% (q20 -3.17%) → **SL/trailing à −3.17%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.06% / q75 +3.8% → **scale +2.06% / runner +3.8%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **18%** (continue à baisser 60%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.16%** (au-delà de la MAE q10 -6.16%), cible rebond +1.89% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.15% .. +4.68%] · haut q95 +6.02% · bas q05 -4.45%
   - 60min (n=160) : retour [-4.36% .. +5.15%] · haut q95 +6.52% · bas q05 -5.81%
   - 2h (n=160) : retour [-4.83% .. +6.65%] · haut q95 +7.67% · bas q05 -5.84%
   - 4h (n=160) : retour [-6.33% .. +7.42%] · haut q95 +8.59% · bas q05 -7.19%
   - 6h (n=160) : retour [-6.52% .. +7.21%] · haut q95 +8.99% · bas q05 -8.66%
   - session (n=160) : retour [-7.58% .. +8.28%] · haut q95 +9.39% · bas q05 -9.14%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 9 séances trend-up (n_eff 5.7)
- **ARMER** : fenêtre la + prédictive = **60 min** → P(reste trend-up à la clôture) **21%**. Lecture précoce 30 min : signature présente → 11% vs absente 3% (base 6%)
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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 26.9  _(survente)_
- **ADX** : 22.2  _(pas de tendance nette)_
- **MACD** : hist -0.033  _(pas de croisement recent)_
- **BB** : %B 0.26 · largeur 33.3%
- **ATR** : 1.75 (32.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.212  _(distribution)_
- **Vol ratio** : 0.51  _(volume atone)_
- **Choppiness** : 41.1  _(transition)_
- **MA** : MA20 29.2 · MA50 33.45 · MA200 34.28  _(prix < MA20)_
- **Dist MA** : MA20 -7.9% · MA50 -19.6% · MA200 -21.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88076 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
