# SMCI

**Generated** : 2026-08-13T00:23:10.114943+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $37.61  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $37.61 (+4.1% vs entrée) · entrée $36.12 · stop $33.96 · T1 $40.44 · R/R 2.0  
> ↳ P(T1 av. stop) 0 % _(réel 5 s)_ · EV/risk -0.004 _(réel 5 s)_ (GBM -0.013) · ¼-Kelly 0.048 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −5.98% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : %B 1.15 (collé à la bande haute) ; extension extrême (≥3×ATR, confluence MA20/50) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $35.82–$36.42 (mid $36.12)
- Spot actuel : $37.61 (+4.1% au-dessus de la zone — repli à attendre)
- Stop : $33.96 (stop swing_plan-based (-15.29%))
- Targets : T1 $40.44 · R/R 2.0 | T2 $40.51 · R/R 2.03 | T3 $40.58 · R/R 2.06
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $33.96


## Edge, scénarios & sizing

- EV/risk : -0.013 | EV/share : $-0.029 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 26 % | T2 26 % | T3 26 %
- Kelly (position) : f* 0.194 | ¼-Kelly 0.048 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 52.8 | bear 6.9 | side 40.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 489.0 (= 13 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.969% → cible +11.956% / stop −5.978%, p_fill 35%, n_eff≈16.0) : P(cible|rempli) **0%** · **EV/risk -0.004** (×p_fill ; si rempli -0.07% du capital)
  - **swing** (entrée dip −8.738% → cible +9.22% / stop −7.179%, p_fill 20%, n_eff≈9.4) : P(cible|rempli) **38%** · **EV/risk -0.028** (×p_fill ; si rempli -0.98% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=14, n_eff=9))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→78% · +2.0%→62% · +3.0%→48% · +5.0%→26% · +8.0%→11%
- Range intraday médian 6.47% (p90 10.14%) · excursion haute méd. +2.55% / basse méd. −2.52%
- Profil de vol intra : ouverture 4.043% vs midi 1.228% vs clôture 1.639% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 17% · trend ↑0%/↓1% ; spike-down 70% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.133 ; mean-reverting — autocorr -0.095)_ ; drift intra méd. -0.251% ; recovery-V 20%
- **σ réalisé intraday** 4.014% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 62% / whipsaw 11%
- POC intraday (dernière séance, temps-au-prix) : 31.5469 (VA 31.0534–31.6526 ; dernier close 31.68)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 31% · rebond 78% · **stop −4.6%** sous le fill (sous le bruit) · cible +2.22% · R/R 0.48 (high win-rate)
- Gaps overnight (n=159) : méd. 0.36% · baisse 43% (gap-down >1% 32% · >2% 17%)
- Excursion ouverture 5min (n=160) : bas méd −0.87% (p90 −2.53%) · haut méd +0.94% · range méd 2.06%
- Excursion ouverture 15min (n=160) : bas méd −1.28% (p90 −3.18%) · haut méd +1.36% · range méd 2.78%
- Excursion ouverture 30min (n=160) : bas méd −1.62% (p90 −3.67%) · haut méd +1.45% · range méd 3.6%
- Excursion ouverture 60min (n=160) : bas méd −1.9% (p90 −4.69%) · haut méd +1.68% · range méd 4.32%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 31.68 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 74% (122/159) · gap 39% · délai 0.0min · rebond 57% (72/122) (MFE +1.33%)
   - −1.0% : fill 30min 54% · séance 70% (112/159) · gap 32% · délai 0.0min · rebond 62% (67/112) (MFE +1.38%)
   - −1.5% : fill 30min 45% · séance 63% (99/159) · gap 23% · délai 0.1min · rebond 64% (61/99) (MFE +1.55%)
   - −2.0% : fill 30min 42% · séance 53% (87/159) · gap 17% · délai 0.8min · rebond 66% (55/87) (MFE +1.68%)
   - −3.0% : fill 30min 30% · séance 49% (74/159) · gap 12% · délai 9.8min · rebond 62% (46/74) (MFE +1.8%)
   - −4.0% : fill 30min 20% · séance 37% (54/159) · gap 8% · délai 21.7min · rebond 70% (34/54) (MFE +1.68%)
   - −5.0% : fill 30min 15% · séance 31% (44/159) · gap 5% · délai 39.0min · rebond 78% (31/44) (MFE +2.22%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.56% (p90 −2.21%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.7% (p90 −3.04%) → stop au-delà de −1.91% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.78% (p90 −2.61%) → stop au-delà de −1.93% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=879 jambes) : jambe baissière méd −1.19% (p90 −2.79%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (69 séances) :
      · −1.0% : fill 95% (67/69) · rebond 53% (37/67)
      · −2.0% : fill 87% (60/69) · rebond 59% (34/60)
      · −3.0% : fill 83% (55/69) · rebond 57% (32/55)
      · −4.0% : fill 65% (42/69) · rebond 67% (26/42)
      · −5.0% : fill 55% (35/69) · rebond 76% (24/35)
   - **flat** (12 séances) :
      · −1.0% : fill 97% (11/12) · rebond 92% (9/11)
      · −2.0% : fill 60% (8/12) · rebond 90% (6/8)
      · −3.0% : fill 36% (3/12) · rebond 100% (3/3)
      · −4.0% : fill 30% (2/12) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/12) · rebond 0% (0/0)
   - **gap-up** (78 séances) :
      · −1.0% : fill 46% (34/78) · rebond 71% (21/34)
      · −2.0% : fill 24% (19/78) · rebond 77% (15/19)
      · −3.0% : fill 22% (16/78) · rebond 70% (11/16)
      · −4.0% : fill 16% (10/78) · rebond 71% (6/10)
      · −5.0% : fill 14% (9/78) · rebond 85% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 66% si les 15 1res min sont vertes (74 cas) · 23% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:50** → P(séance verte=clôture>ouverture) 79% si début vert vs 6% si rouge (base 43% · écart 74 pts) ; prédictivité sature ensuite (plafond brut 212min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=87) : tient le vert **79%** · continue >prix actuel 47% ; creux résiduel méd -1.42% (q20 -3.39%) → **SL/trailing à −3.39%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.59% / q75 +2.98% → **scale +1.59% / runner +2.98%**, sortie à la clôture
  - **si ROUGE au coude** (n=73) : edge inversé — récupère vert seulement **6%** (continue à baisser 57%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.92%** (au-delà de la MAE q10 -4.92%), cible rebond +1.68% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.15% .. +4.68%] · haut q95 +5.88% · bas q05 -4.44%
   - 60min (n=160) : retour [-4.37% .. +5.27%] · haut q95 +6.49% · bas q05 -5.32%
   - 2h (n=160) : retour [-4.81% .. +6.65%] · haut q95 +7.3% · bas q05 -5.84%
   - 4h (n=160) : retour [-5.42% .. +7.42%] · haut q95 +8.49% · bas q05 -6.91%
   - 6h (n=160) : retour [-5.95% .. +6.82%] · haut q95 +8.93% · bas q05 -6.99%
   - session (n=160) : retour [-7.46% .. +7.84%] · haut q95 +9.36% · bas q05 -8.16%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0% / strong 5.0%) · base = 8 séances trend-up (n_eff 5.5)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **15%**. Lecture précoce 30 min : signature présente → 8% vs absente 2% (base 5%)
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

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : extreme
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

- **RSI** : 64.5  _(momentum haussier)_
- **ADX** : 17.2  _(pas de tendance nette)_
- **MACD** : hist 0.913  _(pas de croisement recent)_
- **BB** : %B 1.15 · largeur 45.0%
- **ATR** : 2.46 (71.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.066  _(accumulation)_
- **Vol ratio** : 2.93  _(volume au-dessus de la moyenne)_
- **Choppiness** : 38.6  _(transition)_
- **MA** : MA20 29.1 · MA50 31.18 · MA200 31.92  _(prix > MA20)_
- **Dist MA** : MA20 +29.3% · MA50 +20.6% · MA200 +17.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92311 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
