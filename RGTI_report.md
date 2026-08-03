# RGTI

**Generated** : 2026-08-03T22:04:27.740247+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $16.02  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $16.02 (+2.4% vs entrée) · entrée $15.65 · stop $15.28 · T1 $16.30 · R/R 1.76  
> ↳ P(T1 av. stop) 12 % _(réel 5 s)_ · EV/risk -0.273 _(réel 5 s)_ (GBM 0.185) · ¼-Kelly 0.03 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.34% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $15.54–$15.76 (mid $15.65)
- Spot actuel : $16.02 (+2.4% au-dessus de la zone — repli à attendre)
- Stop : $15.28 (stop swing_plan-based (-12.7%))
- Targets : T1 $16.30 · R/R 1.76 | T2 $16.78 · R/R 3.05 | T3 $17.27 · R/R 4.38
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $15.28


## Edge, scénarios & sizing

- EV/risk : 0.185 | EV/share : $0.068 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 38 % | T2 32 % | T3 32 %
- Kelly (position) : f* 0.122 | ¼-Kelly 0.03 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.5 | bear 16.9 | side 77.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.312% → cible +4.152% / stop −2.342%, p_fill 54%, n_eff≈23.1) : P(cible|rempli) **12%** · **EV/risk -0.273** (×p_fill ; si rempli -1.19% du capital)
  - **swing** (entrée dip −5.084% → cible +13.557% / stop −8.034%, p_fill 53%, n_eff≈24.1) : P(cible|rempli) **7%** · **EV/risk -0.277** (×p_fill ; si rempli -4.19% du capital)
  - **deep** (entrée dip −7.847% → cible +26.072% / stop −13.036%, p_fill 60%, n_eff≈23.2) : P(cible|rempli) **4%** · **EV/risk -0.297** (×p_fill ; si rempli -6.49% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→79% · +2.0%→71% · +3.0%→55% · +5.0%→39% · +8.0%→15%
- Range intraday médian 8.12% (p90 13.36%) · excursion haute méd. +3.41% / basse méd. −2.93%
- Profil de vol intra : ouverture 5.421% vs midi 1.682% vs clôture 1.907% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 20% · trend ↑0%/↓0% ; spike-down 75% · recovery-V 40%)_
- **Régime intraday** : **chop** _(efficiency 0.129 ; neutre — autocorr 0.005)_ ; drift intra méd. -0.431% ; recovery-V 33%
- **σ réalisé intraday** 4.907% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 41% / bas 63% / whipsaw 11%
- POC intraday (dernière séance, temps-au-prix) : 15.0378 (VA 14.8934–15.0997 ; dernier close 14.925)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 46% · rebond 73% · **stop −6.42%** sous le fill (sous le bruit) · cible +2.32% · R/R 0.36 (high win-rate)
- Gaps overnight (n=159) : méd. -0.5% · baisse 57% (gap-down >1% 45% · >2% 30%)
- Excursion ouverture 5min (n=160) : bas méd −1.23% (p90 −2.74%) · haut méd +1.1% · range méd 2.58%
- Excursion ouverture 15min (n=160) : bas méd −1.42% (p90 −4.26%) · haut méd +1.55% · range méd 3.43%
- Excursion ouverture 30min (n=160) : bas méd −1.79% (p90 −5.61%) · haut méd +2.0% · range méd 4.68%
- Excursion ouverture 60min (n=160) : bas méd −2.08% (p90 −6.49%) · haut méd +2.38% · range méd 5.58%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 14.925 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 74% · séance 82% (135/159) · gap 50% · délai 0.0min · rebond 63% (87/135) (MFE +2.24%)
   - −1.0% : fill 30min 68% · séance 78% (130/159) · gap 45% · délai 0.0min · rebond 64% (84/130) (MFE +1.91%)
   - −1.5% : fill 30min 64% · séance 73% (123/159) · gap 39% · délai 0.0min · rebond 63% (80/123) (MFE +2.19%)
   - −2.0% : fill 30min 58% · séance 68% (115/159) · gap 30% · délai 0.0min · rebond 64% (76/115) (MFE +1.78%)
   - −3.0% : fill 30min 52% · séance 61% (98/159) · gap 13% · délai 1.2min · rebond 72% (71/98) (MFE +2.47%)
   - −4.0% : fill 30min 39% · séance 46% (77/159) · gap 4% · délai 5.8min · rebond 73% (56/77) (MFE +2.32%)
   - −5.0% : fill 30min 21% · séance 39% (63/159) · gap 1% · délai 21.5min · rebond 67% (47/63) (MFE +1.72%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.77% (p90 −2.62%) → stop au-delà de −1.72% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.13% (p90 −2.92%) → stop au-delà de −2.08% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.23% (p90 −4.04%) → stop au-delà de −2.22% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1176 jambes) : jambe baissière méd −1.31% (p90 −3.31%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (84 séances) :
      · −1.0% : fill 98% (83/84) · rebond 61% (50/83)
      · −2.0% : fill 89% (79/84) · rebond 64% (53/79)
      · −3.0% : fill 84% (71/84) · rebond 66% (49/71)
      · −4.0% : fill 65% (56/84) · rebond 69% (39/56)
      · −5.0% : fill 56% (48/84) · rebond 64% (36/48)
   - **flat** (15 séances) :
      · −1.0% : fill 91% (13/15) · rebond 90% (11/13)
      · −2.0% : fill 71% (11/15) · rebond 72% (8/11)
      · −3.0% : fill 56% (6/15) · rebond 84% (4/6)
      · −4.0% : fill 56% (6/15) · rebond 85% (4/6)
      · −5.0% : fill 35% (5/15) · rebond 87% (3/5)
   - **gap-up** (60 séances) :
      · −1.0% : fill 48% (34/60) · rebond 63% (23/34)
      · −2.0% : fill 37% (25/60) · rebond 63% (15/25)
      · −3.0% : fill 30% (21/60) · rebond 89% (18/21)
      · −4.0% : fill 19% (15/60) · rebond 85% (13/15)
      · −5.0% : fill 15% (10/60) · rebond 68% (8/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 68% si les 15 1res min sont vertes (80 cas) · 31% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:32** → P(séance verte=clôture>ouverture) 91% si début vert vs 14% si rouge (base 50% · écart 77 pts) ; prédictivité sature ensuite (plafond brut 140min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **91%** · continue >prix actuel 56% ; creux résiduel méd -1.91% (q20 -3.08%) → **SL/trailing à −3.08%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.68% / q75 +4.37% → **scale +2.68% / runner +4.37%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **14%** (continue à baisser 61%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.65%** (au-delà de la MAE q10 -5.65%), cible rebond +2.15% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.47% .. +4.97%] · haut q95 +6.83% · bas q05 -6.5%
   - 60min (n=160) : retour [-5.88% .. +6.2%] · haut q95 +7.02% · bas q05 -7.01%
   - 2h (n=160) : retour [-6.77% .. +7.59%] · haut q95 +9.13% · bas q05 -8.02%
   - 4h (n=160) : retour [-7.65% .. +6.81%] · haut q95 +9.19% · bas q05 -8.67%
   - 6h (n=160) : retour [-7.81% .. +8.62%] · haut q95 +10.01% · bas q05 -9.45%
   - session (n=160) : retour [-7.69% .. +9.05%] · haut q95 +10.34% · bas q05 -9.5%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0% / strong 5.0%) · base = 8 séances trend-up (n_eff 5.6)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 12% vs absente 1% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.17% (p75 1.73% / p90 2.57%) · ~4.96 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **88%** (reprise méd 10.31 min, n=35)
   - −1.0% → **92%** (reprise méd 32.63 min, n=22)
   - −1.5% → **85%** (reprise méd 66.19 min, n=12)
   - −2.0% → **69%** (reprise méd 145.0 min, n=7)
   - −3.0% → **26%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.57%** (p90, défaut prudent ; serré/agressif −1.73%) ; extension open→close méd +8.81% (q75 +9.71% / q95 +9.99%), MFE méd +9.89% / q90 +11.18%
   - Échelle scale-out : +9.89% (33%) / +10.33% (33%) / +11.18% (34%)
- **DÉSARMER** : repli > **−2.57%** depuis le plus-haut = décay → P(retournement) **48%** (préavis méd 141.49 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +11.18% : P(retournement après) 0% (mèche méd 1.88%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +0.82%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-06 — RGTI earnings (J-2 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-06 — RGTI earnings (J-2 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 49.6  _(neutre)_
- **ADX** : 27.8  _(tendance etablie)_
- **MACD** : hist 0.247  _(pas de croisement recent)_
- **BB** : %B 0.69 · largeur 27.3%
- **ATR** : 1.22 (16.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.14  _(distribution)_
- **Vol ratio** : 1.03  _(volume normal)_
- **Choppiness** : 62.9  _(marche en range (choppy))_
- **MA** : MA20 15.25 · MA50 19.14 · MA200 21.77  _(prix > MA20)_
- **Dist MA** : MA20 +5.1% · MA50 -16.3% · MA200 -26.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88152 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
