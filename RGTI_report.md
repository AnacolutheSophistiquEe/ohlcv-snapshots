# RGTI

**Generated** : 2026-08-05T00:27:16.031549+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $17.45  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-06 — RGTI earnings (J-1 sess · earnings)  
> ↳ spot $17.45 (+0.5% vs entrée) · entrée $17.36 · stop $16.74 · T1 $18.61 · R/R 2.02  
> ↳ P(T1 av. stop) 19 % _(réel 5 s)_ · EV/risk 0.036 _(réel 5 s)_ (GBM 0.092) · ¼-Kelly 0.042 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.59% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.080 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._
- 🔴 **Santé haussière vs sur-extension** — Santé technique 7/10 élevée alors que : %B 0.98 (collé à la bande haute) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $17.28–$17.45 (mid $17.36)
- Spot actuel : $17.45 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : $16.74 (stop swing_plan-based (-12.32%))
- Targets : T1 $18.61 · R/R 2.02 | T2 $18.89 · R/R 2.47 | T3 $19.17 · R/R 2.92
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.74


## Edge, scénarios & sizing

- EV/risk : 0.092 | EV/share : $0.058 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 36 % | T3 36 %
- Kelly (position) : f* 0.166 | ¼-Kelly 0.042 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 17.7 | side 77.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 279.0 (= 16 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.493% → cible +7.19% / stop −3.595%, p_fill 91%, n_eff≈37.9) : P(cible|rempli) **19%** · **EV/risk +0.036** (×p_fill ; si rempli +0.14% du capital)
  - **swing** (entrée dip −1.062% → cible +22.758% / stop −11.379%, p_fill 92%, n_eff≈38.1) : P(cible|rempli) **2%** · **EV/risk -0.454** (×p_fill ; si rempli -5.59% du capital)
  - **deep** (entrée dip −1.537% → cible +10.973% / stop −10.809%, p_fill 89%, n_eff≈35.8) : P(cible|rempli) **22%** · **EV/risk -0.524** (×p_fill ; si rempli -6.37% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→79% · +2.0%→71% · +3.0%→55% · +5.0%→39% · +8.0%→16%
- Range intraday médian 8.18% (p90 13.36%) · excursion haute méd. +3.41% / basse méd. −2.93%
- Profil de vol intra : ouverture 5.452% vs midi 1.686% vs clôture 1.896% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 22% · trend ↑0%/↓0% ; spike-down 74% · recovery-V 42%)_
- **Régime intraday** : **chop** _(efficiency 0.136 ; neutre — autocorr 0.014)_ ; drift intra méd. -0.084% ; recovery-V 37%
- **σ réalisé intraday** 4.885% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 44% / bas 60% / whipsaw 10%
- POC intraday (dernière séance, temps-au-prix) : 16.0841 (VA 16.0449–16.2411 ; dernier close 16.005)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 46% · rebond 73% · **stop −6.42%** sous le fill (sous le bruit) · cible +2.32% · R/R 0.36 (high win-rate)
- Gaps overnight (n=159) : méd. -0.47% · baisse 56% (gap-down >1% 44% · >2% 29%)
- Excursion ouverture 5min (n=160) : bas méd −1.23% (p90 −2.74%) · haut méd +1.05% · range méd 2.56%
- Excursion ouverture 15min (n=160) : bas méd −1.44% (p90 −4.25%) · haut méd +1.58% · range méd 3.49%
- Excursion ouverture 30min (n=160) : bas méd −1.77% (p90 −5.52%) · haut méd +2.06% · range méd 4.78%
- Excursion ouverture 60min (n=160) : bas méd −2.07% (p90 −6.48%) · haut méd +2.4% · range méd 5.61%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 16.005 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 75% · séance 82% (135/159) · gap 49% · délai 0.0min · rebond 64% (88/135) (MFE +2.29%)
   - −1.0% : fill 30min 69% · séance 78% (130/159) · gap 44% · délai 0.0min · rebond 65% (85/130) (MFE +2.04%)
   - −1.5% : fill 30min 62% · séance 72% (122/159) · gap 38% · délai 0.0min · rebond 63% (80/122) (MFE +2.19%)
   - −2.0% : fill 30min 57% · séance 66% (114/159) · gap 29% · délai 0.0min · rebond 64% (75/114) (MFE +1.8%)
   - −3.0% : fill 30min 51% · séance 60% (97/159) · gap 12% · délai 1.2min · rebond 71% (70/97) (MFE +2.47%)
   - −4.0% : fill 30min 38% · séance 46% (76/159) · gap 4% · délai 5.9min · rebond 73% (55/76) (MFE +2.32%)
   - −5.0% : fill 30min 21% · séance 38% (62/159) · gap 1% · délai 21.5min · rebond 67% (46/62) (MFE +1.71%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.78% (p90 −2.57%) → stop au-delà de −1.67% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.19% (p90 −2.88%) → stop au-delà de −2.08% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.24% (p90 −4.02%) → stop au-delà de −2.14% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1174 jambes) : jambe baissière méd −1.29% (p90 −3.31%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (83 séances) :
      · −1.0% : fill 98% (82/83) · rebond 61% (50/82)
      · −2.0% : fill 89% (78/83) · rebond 64% (52/78)
      · −3.0% : fill 84% (70/83) · rebond 66% (48/70)
      · −4.0% : fill 65% (55/83) · rebond 69% (38/55)
      · −5.0% : fill 56% (47/83) · rebond 64% (35/47)
   - **flat** (16 séances) :
      · −1.0% : fill 93% (14/16) · rebond 92% (12/14)
      · −2.0% : fill 58% (11/16) · rebond 72% (8/11)
      · −3.0% : fill 46% (6/16) · rebond 84% (4/6)
      · −4.0% : fill 46% (6/16) · rebond 85% (4/6)
      · −5.0% : fill 28% (5/16) · rebond 87% (3/5)
   - **gap-up** (60 séances) :
      · −1.0% : fill 48% (34/60) · rebond 63% (23/34)
      · −2.0% : fill 37% (25/60) · rebond 63% (15/25)
      · −3.0% : fill 30% (21/60) · rebond 89% (18/21)
      · −4.0% : fill 19% (15/60) · rebond 85% (13/15)
      · −5.0% : fill 15% (10/60) · rebond 68% (8/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 69% si les 15 1res min sont vertes (80 cas) · 31% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:32** → P(séance verte=clôture>ouverture) 91% si début vert vs 14% si rouge (base 51% · écart 77 pts) ; prédictivité sature ensuite (plafond brut 140min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **91%** · continue >prix actuel 54% ; creux résiduel méd -1.89% (q20 -3.08%) → **SL/trailing à −3.08%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.64% / q75 +4.27% → **scale +2.64% / runner +4.27%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **14%** (continue à baisser 61%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.65%** (au-delà de la MAE q10 -5.65%), cible rebond +2.15% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.47% .. +4.97%] · haut q95 +6.8% · bas q05 -6.49%
   - 60min (n=160) : retour [-5.85% .. +6.75%] · haut q95 +7.01% · bas q05 -7.0%
   - 2h (n=160) : retour [-6.56% .. +7.59%] · haut q95 +9.18% · bas q05 -7.96%
   - 4h (n=160) : retour [-7.63% .. +7.76%] · haut q95 +9.18% · bas q05 -8.56%
   - 6h (n=160) : retour [-7.72% .. +8.6%] · haut q95 +9.88% · bas q05 -9.33%
   - session (n=160) : retour [-7.69% .. +8.98%] · haut q95 +10.34% · bas q05 -9.38%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 9 séances trend-up (n_eff 6.1)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **41%**. Lecture précoce 30 min : signature présente → 17% vs absente 1% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.17% (p75 1.66% / p90 2.13%) · ~4.12 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **85%** (reprise méd 10.0 min, n=39)
   - −1.0% → **83%** (reprise méd 35.86 min, n=24)
   - −1.5% → **74%** (reprise méd 89.24 min, n=14)
   - −2.0% → **69%** (reprise méd 145.0 min, n=7)
   - −3.0% → **26%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.13%** (p90, défaut prudent ; serré/agressif −1.66%) ; extension open→close méd +8.09% (q75 +9.41% / q95 +9.99%), MFE méd +9.52% / q90 +10.7%
   - Échelle scale-out : +9.52% (33%) / +10.28% (33%) / +10.7% (34%)
- **DÉSARMER** : repli > **−2.13%** depuis le plus-haut = décay → P(retournement) **38%** (préavis méd 141.49 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.7% : P(retournement après) 0% (mèche méd 1.88%)
- **CONTEXTE** : la dernière heure tient les gains 74% du temps (retour médian dernière heure +0.7%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-08-06 — RGTI earnings (J-1 sess · earnings)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-06 — RGTI earnings (J-1 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-06 — RGTI earnings (J-1 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 59.5  _(momentum haussier)_
- **ADX** : 26.2  _(tendance etablie)_
- **MACD** : hist 0.406  _(pas de croisement recent)_
- **BB** : %B 0.98 · largeur 29.2%
- **ATR** : 1.24 (17.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.075  _(distribution)_
- **Vol ratio** : 1.12  _(volume normal)_
- **Choppiness** : 50.4  _(transition)_
- **MA** : MA20 15.29 · MA50 19.04 · MA200 21.57  _(prix > MA20)_
- **Dist MA** : MA20 +14.1% · MA50 -8.4% · MA200 -19.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (94146 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
