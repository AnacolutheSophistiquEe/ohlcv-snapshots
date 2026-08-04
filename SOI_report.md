# SOI

**Generated** : 2026-08-04T21:44:38.073445+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 8.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €120.10  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €120.10 (+0.7% vs entrée) · entrée €119.26 · stop €114.89 · T1 €128.00 · R/R 2.0  
> ↳ P(T1 av. stop) 12 % _(réel 5 s)_ · EV/risk -0.207 _(réel 5 s)_ (GBM 0.118) · ¼-Kelly 0.058 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.67% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : %B 1.02 (collé à la bande haute) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €118.41–€120.10 (mid €119.26)
- Spot actuel : €120.10 (+0.7% au-dessus de la zone — repli à attendre)
- Stop : €114.89 (stop swing_plan-based (-10.69%))
- Targets : T1 €128.00 · R/R 2.0 | T2 €131.83 · R/R 2.88 | T3 €135.66 · R/R 3.75
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €114.89


## Edge, scénarios & sizing

- EV/risk : 0.118 | EV/share : €0.516 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 42 % | T2 42 % | T3 42 %
- Kelly (position) : f* 0.232 | ¼-Kelly 0.058 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.7 | bear 66.4 | side 27.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 360.0 (= 3 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.7% → cible +7.331% / stop −3.666%, p_fill 90%, n_eff≈36.1) : P(cible|rempli) **12%** · **EV/risk -0.207** (×p_fill ; si rempli -0.84% du capital)
  - **swing** (entrée dip −1.553% → cible +15.112% / stop −9.281%, p_fill 84%, n_eff≈34.3) : P(cible|rempli) **18%** · **EV/risk -0.237** (×p_fill ; si rempli -2.63% du capital)
  - **deep** (entrée dip −2.265% → cible +14.496% / stop −14.023%, p_fill 91%, n_eff≈37.0) : P(cible|rempli) **26%** · **EV/risk -0.370** (×p_fill ; si rempli -5.71% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→79% · +2.0%→70% · +3.0%→57% · +5.0%→44% · +8.0%→22%
- Range intraday médian 9.57% (p90 16.36%) · excursion haute méd. +3.82% / basse méd. −3.75%
- Profil de vol intra : ouverture 5.97% vs midi 1.68% vs clôture 2.603% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (146 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓1% ; spike-down 79% · recovery-V 42%)_
- **Régime intraday** : **chop** _(efficiency 0.128 ; mean-reverting — autocorr -0.086)_ ; drift intra méd. -0.602% ; recovery-V 38%
- **σ réalisé intraday** 5.716% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 63% / whipsaw 33%
- POC intraday (dernière séance, temps-au-prix) : 105.8713 (VA 103.3462–106.8812 ; dernier close 109.32)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 43% · rebond 78% · **stop −7.29%** sous le fill (sous le bruit) · cible +2.79% · R/R 0.38 (high win-rate)
- Gaps overnight (n=145) : méd. 0.09% · baisse 48% (gap-down >1% 32% · >2% 23%)
- Excursion ouverture 5min (n=146) : bas méd −1.27% (p90 −3.78%) · haut méd +0.97% · range méd 2.94%
- Excursion ouverture 15min (n=146) : bas méd −1.55% (p90 −5.12%) · haut méd +1.43% · range méd 3.8%
- Excursion ouverture 30min (n=146) : bas méd −1.7% (p90 −5.52%) · haut méd +1.78% · range méd 4.33%
- Excursion ouverture 60min (n=146) : bas méd −1.85% (p90 −5.88%) · haut méd +1.89% · range méd 4.71%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 109.32 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 80% (115/145) · gap 38% · délai 0.0min · rebond 65% (75/115) (MFE +2.03%)
   - −1.0% : fill 30min 61% · séance 75% (109/145) · gap 32% · délai 0.2min · rebond 72% (79/109) (MFE +1.87%)
   - −1.5% : fill 30min 57% · séance 72% (100/145) · gap 30% · délai 0.2min · rebond 75% (74/100) (MFE +2.26%)
   - −2.0% : fill 30min 53% · séance 66% (92/145) · gap 23% · délai 0.2min · rebond 77% (73/92) (MFE +2.82%)
   - −3.0% : fill 30min 39% · séance 56% (76/145) · gap 17% · délai 0.8min · rebond 75% (60/76) (MFE +2.91%)
   - −4.0% : fill 30min 31% · séance 46% (61/145) · gap 8% · délai 1.9min · rebond 74% (48/61) (MFE +2.43%)
   - −5.0% : fill 30min 23% · séance 43% (53/145) · gap 2% · délai 14.4min · rebond 78% (44/53) (MFE +2.79%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.87% (p90 −3.85%) → stop au-delà de −2.3% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.01% (p90 −3.97%) → stop au-delà de −2.24% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.97% (p90 −3.19%) → stop au-delà de −2.23% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1282 jambes) : jambe baissière méd −1.33% (p90 −3.17%) · ~18.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (57 séances) :
      · −1.0% : fill 98% (56/57) · rebond 61% (35/56)
      · −2.0% : fill 94% (54/57) · rebond 72% (42/54)
      · −3.0% : fill 86% (46/57) · rebond 74% (37/46)
      · −4.0% : fill 74% (40/57) · rebond 81% (33/40)
      · −5.0% : fill 67% (35/57) · rebond 87% (30/35)
   - **flat** (17 séances) :
      · −1.0% : fill 100% (17/17) · rebond 79% (14/17)
      · −2.0% : fill 96% (15/17) · rebond 82% (12/15)
      · −3.0% : fill 69% (11/17) · rebond 67% (8/11)
      · −4.0% : fill 57% (8/17) · rebond 65% (6/8)
      · −5.0% : fill 57% (8/17) · rebond 77% (7/8)
   - **gap-up** (71 séances) :
      · −1.0% : fill 49% (36/71) · rebond 87% (30/36)
      · −2.0% : fill 33% (23/71) · rebond 87% (19/23)
      · −3.0% : fill 26% (19/71) · rebond 83% (15/19)
      · −4.0% : fill 19% (13/71) · rebond 55% (9/13)
      · −5.0% : fill 18% (10/71) · rebond 47% (7/10)
- **P(clôture VERTE) selon le drive 15min** (n=146) : 51% en base · 69% si les 15 1res min sont vertes (68 cas) · 32% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=146) : COUDE à **47min** → P(séance verte=clôture>ouverture) 82% si début vert vs 27% si rouge (base 51% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 276min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=61) : tient le vert **82%** · continue >prix actuel 60% ; creux résiduel méd -2.36% (q20 -6.18%) → **SL/trailing à −6.18%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.17% / q75 +5.16% → **scale +3.17% / runner +5.16%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **27%** (continue à baisser 55%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.5%** (au-delà de la MAE q10 -8.5%), cible rebond +2.8% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=146) : retour [-5.25% .. +7.06%] · haut q95 +7.64% · bas q05 -6.64%
   - 60min (n=146) : retour [-5.96% .. +7.24%] · haut q95 +9.28% · bas q05 -7.09%
   - 2h (n=146) : retour [-6.05% .. +9.97%] · haut q95 +12.5% · bas q05 -7.95%
   - 4h (n=146) : retour [-6.99% .. +10.28%] · haut q95 +14.28% · bas q05 -8.22%
   - 6h (n=146) : retour [-7.95% .. +11.15%] · haut q95 +14.3% · bas q05 -9.87%
   - session (n=146) : retour [-11.39% .. +13.84%] · haut q95 +15.96% · bas q05 -13.33%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 9 séances trend-up (n_eff 5.7)
- **ARMER** : fenêtre la + prédictive = **60 min** → P(reste trend-up à la clôture) **14%**. Lecture précoce 30 min : signature présente → 6% vs absente 5% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.08% (p75 1.67% / p90 2.95%) · ~6.0 replis/séance, durée méd 38.95 min. P(nouveau plus-haut après repli) :
   - −0.5% → **94%** (reprise méd 20.0 min, n=57)
   - −1.0% → **92%** (reprise méd 34.22 min, n=33)
   - −1.5% → **88%** (reprise méd 46.1 min, n=17)
   - −2.0% → **87%** (reprise méd 49.44 min, n=15)
   - −3.0% → **100%** (reprise méd 61.76 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.95%** (p90, défaut prudent ; serré/agressif −1.67%) ; extension open→close méd +10.12% (q75 +13.85% / q95 +17.31%), MFE méd +10.12% / q90 +18.28%
   - Échelle scale-out : +10.12% (33%) / +16.57% (33%) / +18.28% (34%)
- **DÉSARMER** : repli > **−2.95%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +18.28% : P(retournement après) 0% (mèche méd 1.42%)
- **CONTEXTE** : la dernière heure tient les gains 94% du temps (retour médian dernière heure +3.01%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 59.5  _(momentum haussier)_
- **ADX** : 15.5  _(pas de tendance nette)_
- **MACD** : hist 3.022  _(pas de croisement recent)_
- **BB** : %B 1.02 · largeur 36.2%
- **ATR** : 10.97 (81.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.05  _(neutre)_
- **Vol ratio** : 0.92  _(volume normal)_
- **Choppiness** : 45.4  _(transition)_
- **MA** : MA20 101.04 · MA50 121.5 · MA200 71.43  _(prix > MA20)_
- **Dist MA** : MA20 +18.9% · MA50 -1.2% · MA200 +68.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (100459 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
