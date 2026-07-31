# 000660

**Generated** : 2026-07-31T21:48:31.412347+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩1718000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩1718000.00 (+0.8% vs entrée) · entrée ₩1704673.08 · stop ₩1629509.63 · T1 ₩1855000.00 · R/R 2.0  
> ↳ P(T1 av. stop) 4 % _(réel 5 s)_ · EV/risk -0.391 _(réel 5 s)_ (GBM -0.06) · ¼-Kelly 0.031 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.41% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1691346.17–₩1718000.00 (mid ₩1704673.08)
- Spot actuel : ₩1718000.00 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : ₩1629509.63 (stop swing_plan-based (-11.36%))
- Targets : T1 ₩1855000.00 · R/R 2.0 | T2 ₩1920749.45 · R/R 2.87 | T3 ₩1986498.90 · R/R 3.75
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1629509.63


## Edge, scénarios & sizing

- EV/risk : -0.06 | EV/share : ₩-4502.168 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 25 % | T2 25 % | T3 25 %
- Kelly (position) : f* 0.125 | ¼-Kelly 0.031 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.9 | bear 62.1 | side 31.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.775% → cible +8.819% / stop −4.409%, p_fill 87%, n_eff≈33.7) : P(cible|rempli) **4%** · **EV/risk -0.391** (×p_fill ; si rempli -1.99% du capital)
  - **swing** (entrée dip −1.715% → cible +19.626% / stop −9.813%, p_fill 81%, n_eff≈30.9) : P(cible|rempli) **9%** · **EV/risk -0.304** (×p_fill ; si rempli -3.70% du capital)
  - **deep** (entrée dip −2.488% → cible +43.679% / stop −18.0%, p_fill 82%, n_eff≈29.1) : P(cible|rempli) **2%** · **EV/risk -0.467** (×p_fill ; si rempli -10.29% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→94% · +1.0%→79% · +2.0%→54% · +3.0%→39% · +5.0%→26% · +8.0%→14%
- Range intraday médian 6.39% (p90 11.5%) · excursion haute méd. +2.16% / basse méd. −2.61%
- Profil de vol intra : ouverture 3.062% vs midi 1.295% vs clôture 1.561% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (147 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 79% · range 19% · trend ↑2%/↓0% ; spike-down 70% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.134 ; neutre — autocorr -0.018)_ ; drift intra méd. -1.595% ; recovery-V 26%
- **σ réalisé intraday** 5.24% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 75% / whipsaw 32%
- POC intraday (dernière séance, temps-au-prix) : 1344387.5 (VA 1251637.5–1427862.5 ; dernier close 1404000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 33% · rebond 73% · **stop −9.06%** sous le fill (sous le bruit) · cible +2.72% · R/R 0.3 (high win-rate)
- Gaps overnight (n=146) : méd. 0.01% · baisse 49% (gap-down >1% 35% · >2% 28%)
- Excursion ouverture 5min (n=147) : bas méd −0.64% (p90 −1.79%) · haut méd +0.91% · range méd 1.59%
- Excursion ouverture 15min (n=147) : bas méd −0.79% (p90 −2.67%) · haut méd +1.17% · range méd 2.27%
- Excursion ouverture 30min (n=147) : bas méd −1.3% (p90 −3.47%) · haut méd +1.3% · range méd 2.89%
- Excursion ouverture 60min (n=147) : bas méd −1.46% (p90 −3.87%) · haut méd +1.57% · range méd 3.64%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1404000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 69% (93/146) · gap 41% · délai 0.0min · rebond 55% (49/93) (MFE +1.28%)
   - −1.0% : fill 30min 54% · séance 65% (85/146) · gap 35% · délai 0.0min · rebond 65% (53/85) (MFE +1.79%)
   - −1.5% : fill 30min 49% · séance 60% (76/146) · gap 33% · délai 0.0min · rebond 66% (48/76) (MFE +2.17%)
   - −2.0% : fill 30min 42% · séance 55% (69/146) · gap 28% · délai 0.0min · rebond 64% (45/69) (MFE +2.04%)
   - −3.0% : fill 30min 39% · séance 48% (59/146) · gap 23% · délai 3.1min · rebond 70% (42/59) (MFE +2.25%)
   - −4.0% : fill 30min 29% · séance 40% (46/146) · gap 14% · délai 6.2min · rebond 76% (35/46) (MFE +2.45%)
   - −5.0% : fill 30min 15% · séance 33% (37/146) · gap 11% · délai 30.4min · rebond 73% (28/37) (MFE +2.72%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.41% (p90 −2.48%) → stop au-delà de −1.45% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.57% (p90 −3.38%) → stop au-delà de −2.42% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −3.61%) → stop au-delà de −2.43% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=771 jambes) : jambe baissière méd −1.33% (p90 −3.54%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (63 séances) :
      · −1.0% : fill 98% (61/63) · rebond 51% (32/61)
      · −2.0% : fill 88% (52/63) · rebond 56% (30/52)
      · −3.0% : fill 84% (47/63) · rebond 68% (32/47)
      · −4.0% : fill 75% (40/63) · rebond 71% (29/40)
      · −5.0% : fill 64% (33/63) · rebond 69% (24/33)
   - **flat** (12 séances) :
      · −1.0% : fill 91% (9/12) · rebond 86% (7/9)
      · −2.0% : fill 77% (7/12) · rebond 86% (6/7)
      · −3.0% : fill 45% (5/12) · rebond 100% (5/5)
      · −4.0% : fill 24% (2/12) · rebond 100% (2/2)
      · −5.0% : fill 11% (1/12) · rebond 100% (1/1)
   - **gap-up** (71 séances) :
      · −1.0% : fill 30% (15/71) · rebond 99% (14/15)
      · −2.0% : fill 20% (10/71) · rebond 85% (9/10)
      · −3.0% : fill 14% (7/71) · rebond 66% (5/7)
      · −4.0% : fill 10% (4/71) · rebond 100% (4/4)
      · −5.0% : fill 8% (3/71) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=147) : 44% en base · 50% si les 15 1res min sont vertes (79 cas) · 37% si rouges (68 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=147) : COUDE à **1:35** → P(séance verte=clôture>ouverture) 77% si début vert vs 15% si rouge (base 44% · écart 62 pts) ; prédictivité sature ensuite (plafond brut 211min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **77%** · continue >prix actuel 52% ; creux résiduel méd -1.63% (q20 -4.87%) → **SL/trailing à −4.87%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.66% / q75 +3.43% → **scale +1.66% / runner +3.43%**, sortie à la clôture
  - **si ROUGE au coude** (n=70) : edge inversé — récupère vert seulement **15%** (continue à baisser 67%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.13%** (au-delà de la MAE q10 -7.13%), cible rebond +1.2% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=147) : retour [-3.01% .. +3.18%] · haut q95 +3.81% · bas q05 -3.76%
   - 60min (n=147) : retour [-3.42% .. +5.53%] · haut q95 +6.22% · bas q05 -4.94%
   - 2h (n=147) : retour [-5.01% .. +5.43%] · haut q95 +8.24% · bas q05 -6.97%
   - 4h (n=147) : retour [-6.74% .. +6.92%] · haut q95 +8.48% · bas q05 -8.23%
   - 6h (n=147) : retour [-8.36% .. +7.67%] · haut q95 +9.53% · bas q05 -10.03%
   - session (n=147) : retour [-8.15% .. +8.02%] · haut q95 +9.53% · bas q05 -10.03%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.1% des séances sont trend-up (mild 0% / strong 6.1%) · base = 9 séances trend-up (n_eff 7.5)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 19% vs absente 1% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.94% (p75 1.08% / p90 1.73%) · ~3.08 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **86%** (reprise méd 23.01 min, n=33)
   - −1.0% → **88%** (reprise méd 32.85 min, n=12)
   - −1.5% → **67%** (reprise méd 29.94 min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.73%** (p90, défaut prudent ; serré/agressif −1.08%) ; extension open→close méd +7.9% (q75 +8.22% / q95 +11.4%), MFE méd +8.29% / q90 +10.64%
   - Échelle scale-out : +8.29% (33%) / +8.54% (33%) / +10.64% (34%)
- **DÉSARMER** : repli > **−1.73%** depuis le plus-haut = décay → P(retournement) **48%** (préavis méd 275.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.64% : P(retournement après) 0% (mèche méd 0.34%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.03%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 39.3  _(momentum baissier)_
- **ADX** : 31.9  _(tendance etablie)_
- **MACD** : hist -43209.882  _(pas de croisement recent)_
- **BB** : %B 0.34 · largeur 60.8%
- **ATR** : 229571.43 (92.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.181  _(distribution)_
- **Vol ratio** : 1.55  _(volume au-dessus de la moyenne)_
- **Choppiness** : 47.2  _(transition)_
- **MA** : MA20 1900400.0 · MA50 2168306.83 · MA200 1174687.07  _(prix < MA20)_
- **Dist MA** : MA20 -9.6% · MA50 -20.8% · MA200 +46.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (87846 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
