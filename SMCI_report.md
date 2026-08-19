# SMCI

**Generated** : 2026-08-19T00:23:11.614315+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 9/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $37.41  

> 🟡 **WAIT-FOR-DIP** — spot +9.3 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $37.41 (+9.3% vs entrée) · entrée $34.23 · stop $30.79 · T1 $41.13 · R/R 2.01  
> ↳ P(T1 av. stop) 17 % · EV/risk 0.202 · ¼-Kelly 0.004 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 9/10 élevée alors que : RSI 77.6 > 70 (surachat) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $33.63–$34.84 (mid $34.23)
- Spot actuel : $37.41 (+9.3% au-dessus de la zone — repli à attendre)
- Stop : $30.79 (stop swing_plan-based (-17.7%))
- Targets : T1 $41.13 · R/R 2.01 | T2 $42.18 · R/R 2.31 | T3 $43.24 · R/R 2.62
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $30.79


## Edge, scénarios & sizing

- EV/risk : 0.188 | EV/share : $0.648 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 17 % | T2 15 % | T3 12 %
- Kelly (position) : f* 0.017 | ¼-Kelly 0.004 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 19.8 | bear 5.7 | side 74.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 636.0 (= 17 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.858% → cible +9.99% / stop −4.995%, p_fill 33%, n_eff≈17.0) : P(cible|rempli) **0%** · **EV/risk +0.001** (×p_fill ; si rempli +0.02% du capital)
  - **swing** (entrée dip −8.49% → cible +20.129% / stop −10.065%, p_fill 18%, n_eff≈9.7) : P(cible|rempli) **16%** · **EV/risk +0.009** (×p_fill ; si rempli +0.51% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=14, n_eff=9))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→78% · +2.0%→64% · +3.0%→49% · +5.0%→28% · +8.0%→14%
- Range intraday médian 6.69% (p90 11.21%) · excursion haute méd. +2.57% / basse méd. −2.66%
- Profil de vol intra : ouverture 4.103% vs midi 1.269% vs clôture 1.654% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 16% · trend ↑0%/↓1% ; spike-down 68% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; mean-reverting — autocorr -0.067)_ ; drift intra méd. 0.27% ; recovery-V 29%
- **σ réalisé intraday** 4.144% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 58% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 39.6781 (VA 39.4006–40.1869 ; dernier close 39.84)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 29% · rebond 78% · **stop −4.6%** sous le fill (sous le bruit) · cible +2.22% · R/R 0.48 (high win-rate)
- Gaps overnight (n=159) : méd. 0.39% · baisse 42% (gap-down >1% 30% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.83% (p90 −2.72%) · haut méd +1.01% · range méd 2.14%
- Excursion ouverture 15min (n=160) : bas méd −1.26% (p90 −3.12%) · haut méd +1.46% · range méd 2.85%
- Excursion ouverture 30min (n=160) : bas méd −1.59% (p90 −3.65%) · haut méd +1.55% · range méd 3.7%
- Excursion ouverture 60min (n=160) : bas méd −1.87% (p90 −4.55%) · haut méd +1.83% · range méd 4.33%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 39.84 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 72% (121/159) · gap 37% · délai 0.0min · rebond 59% (73/121) (MFE +1.43%)
   - −1.0% : fill 30min 52% · séance 68% (112/159) · gap 30% · délai 0.0min · rebond 64% (68/112) (MFE +1.47%)
   - −1.5% : fill 30min 42% · séance 60% (98/159) · gap 22% · délai 0.1min · rebond 64% (60/98) (MFE +1.55%)
   - −2.0% : fill 30min 40% · séance 50% (86/159) · gap 16% · délai 0.8min · rebond 66% (55/86) (MFE +1.68%)
   - −3.0% : fill 30min 29% · séance 46% (73/159) · gap 11% · délai 9.7min · rebond 62% (45/73) (MFE +1.8%)
   - −4.0% : fill 30min 19% · séance 35% (54/159) · gap 7% · délai 21.7min · rebond 70% (34/54) (MFE +1.68%)
   - −5.0% : fill 30min 14% · séance 29% (44/159) · gap 5% · délai 39.0min · rebond 78% (31/44) (MFE +2.22%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.54% (p90 −2.43%) → stop au-delà de −1.57% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.7% (p90 −3.03%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.73% (p90 −2.91%) → stop au-delà de −1.97% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=892 jambes) : jambe baissière méd −1.19% (p90 −2.82%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (69 séances) :
      · −1.0% : fill 95% (67/69) · rebond 53% (37/67)
      · −2.0% : fill 87% (60/69) · rebond 59% (34/60)
      · −3.0% : fill 83% (55/69) · rebond 57% (32/55)
      · −4.0% : fill 65% (42/69) · rebond 67% (26/42)
      · −5.0% : fill 55% (35/69) · rebond 76% (24/35)
   - **flat** (13 séances) :
      · −1.0% : fill 98% (12/13) · rebond 94% (10/12)
      · −2.0% : fill 46% (8/13) · rebond 90% (6/8)
      · −3.0% : fill 27% (3/13) · rebond 100% (3/3)
      · −4.0% : fill 23% (2/13) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/13) · rebond 0% (0/0)
   - **gap-up** (77 séances) :
      · −1.0% : fill 43% (33/77) · rebond 72% (21/33)
      · −2.0% : fill 22% (18/77) · rebond 78% (15/18)
      · −3.0% : fill 20% (15/77) · rebond 70% (10/15)
      · −4.0% : fill 15% (10/77) · rebond 71% (6/10)
      · −5.0% : fill 14% (9/77) · rebond 85% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 69% si les 15 1res min sont vertes (76 cas) · 23% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:50** → P(séance verte=clôture>ouverture) 81% si début vert vs 6% si rouge (base 46% · écart 76 pts) ; prédictivité sature ensuite (plafond brut 211min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=89) : tient le vert **81%** · continue >prix actuel 49% ; creux résiduel méd -1.38% (q20 -3.47%) → **SL/trailing à −3.47%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.76% / q75 +3.03% → **scale +1.76% / runner +3.03%**, sortie à la clôture
  - **si ROUGE au coude** (n=71) : edge inversé — récupère vert seulement **6%** (continue à baisser 57%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.92%** (au-delà de la MAE q10 -4.92%), cible rebond +1.68% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.12% .. +4.68%] · haut q95 +6.28% · bas q05 -4.39%
   - 60min (n=160) : retour [-4.32% .. +5.71%] · haut q95 +8.38% · bas q05 -5.31%
   - 2h (n=160) : retour [-4.79% .. +7.76%] · haut q95 +8.9% · bas q05 -5.83%
   - 4h (n=160) : retour [-5.33% .. +7.42%] · haut q95 +9.32% · bas q05 -6.91%
   - 6h (n=160) : retour [-5.86% .. +7.22%] · haut q95 +10.46% · bas q05 -6.96%
   - session (n=160) : retour [-7.33% .. +7.84%] · haut q95 +10.46% · bas q05 -8.04%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0% / strong 5.0%) · base = 8 séances trend-up (n_eff 5.5)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **13%**. Lecture précoce 30 min : signature présente → 7% vs absente 2% (base 5%)
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
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : stretched_up
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

- **RSI** : 77.6  _(surachat)_
- **ADX** : 24.1  _(pas de tendance nette)_
- **MACD** : hist 1.071  _(pas de croisement recent)_
- **BB** : %B 0.83 · largeur 52.2%
- **ATR** : 2.53 (72.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.02  _(neutre)_
- **Vol ratio** : 0.78  _(volume normal)_
- **Choppiness** : 30.9  _(marche directionnel)_
- **MA** : MA20 31.92 · MA50 30.55 · MA200 31.67  _(prix > MA20)_
- **Dist MA** : MA20 +17.2% · MA50 +22.4% · MA200 +18.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91491 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
