# IONQ

**Generated** : 2026-08-18T22:03:02.826865+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $44.12  

> 🟡 **WAIT-FOR-DIP** — spot +1.9 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $44.12 (+1.9% vs entrée) · entrée $43.30 · stop $40.30 · T1 $46.27 · R/R 0.99  
> ↳ P(T1 av. stop) 58 % _(réel 5 s)_ · EV/risk 0.123 _(réel 5 s)_ (GBM -0.026) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : divergent_short_long (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.030 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._
- 🔴 **Santé haussière vs sur-extension** — Santé technique 7/10 élevée alors que : RSI 73.5 > 70 (surachat) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $42.70–$43.89 (mid $43.30)
- Spot actuel : $44.12 (+1.9% au-dessus de la zone — repli à attendre)
- Stop : $40.30 (stop swing_plan-based (-8.66%))
- Targets : T1 $46.27 · R/R 0.99 | T2 $49.25 · R/R 1.98 | T3 $52.22 · R/R 2.97
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $40.30


## Edge, scénarios & sizing

- EV/risk : -0.026 | EV/share : $-0.078 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 45 % | T2 25 % | T3 14 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 56.7 | bear 31.5 | side 11.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 485.0 (= 11 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.85% → cible +3.071% / stop −2.057%, p_fill 77%, n_eff≈34.4) : P(cible|rempli) **35%** · **EV/risk +0.004** (×p_fill ; si rempli +0.01% du capital)
  - **swing** (entrée dip −1.86% → cible +6.868% / stop −6.929%, p_fill 80%, n_eff≈35.2) : P(cible|rempli) **58%** · **EV/risk +0.123** (×p_fill ; si rempli +1.07% du capital)
  - **deep** (entrée dip −2.87% → cible +9.712% / stop −10.501%, p_fill 87%, n_eff≈36.5) : P(cible|rempli) **51%** · **EV/risk -0.078** (×p_fill ; si rempli -0.95% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→82% · +2.0%→69% · +3.0%→61% · +5.0%→32% · +8.0%→16%
- Range intraday médian 7.64% (p90 12.17%) · excursion haute méd. +3.69% / basse méd. −2.68%
- Profil de vol intra : ouverture 5.217% vs midi 1.463% vs clôture 1.711% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 69% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.116 ; neutre — autocorr 0.026)_ ; drift intra méd. 0.252% ; recovery-V 31%
- **σ réalisé intraday** 4.682% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 57% / bas 58% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 46.2984 (VA 46.0891–46.7866 ; dernier close 46.31)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 35% · rebond 84% · **stop −5.15%** sous le fill (sous le bruit) · cible +2.82% · R/R 0.55 (high win-rate)
- Gaps overnight (n=159) : méd. -0.33% · baisse 54% (gap-down >1% 36% · >2% 18%)
- Excursion ouverture 5min (n=160) : bas méd −1.14% (p90 −2.91%) · haut méd +1.28% · range méd 2.85%
- Excursion ouverture 15min (n=160) : bas méd −1.55% (p90 −4.08%) · haut méd +1.49% · range méd 3.79%
- Excursion ouverture 30min (n=160) : bas méd −1.89% (p90 −5.18%) · haut méd +2.17% · range méd 4.54%
- Excursion ouverture 60min (n=160) : bas méd −2.16% (p90 −5.75%) · haut méd +2.33% · range méd 5.4%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 46.31 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 72% · séance 82% (134/159) · gap 46% · délai 0.0min · rebond 67% (92/134) (MFE +2.03%)
   - −1.0% : fill 30min 68% · séance 75% (126/159) · gap 36% · délai 0.0min · rebond 75% (94/126) (MFE +2.4%)
   - −1.5% : fill 30min 60% · séance 68% (119/159) · gap 31% · délai 0.0min · rebond 66% (81/119) (MFE +2.45%)
   - −2.0% : fill 30min 53% · séance 61% (109/159) · gap 18% · délai 0.1min · rebond 69% (75/109) (MFE +2.42%)
   - −3.0% : fill 30min 43% · séance 52% (92/159) · gap 8% · délai 6.5min · rebond 74% (68/92) (MFE +2.49%)
   - −4.0% : fill 30min 29% · séance 42% (73/159) · gap 5% · délai 14.7min · rebond 75% (56/73) (MFE +2.52%)
   - −5.0% : fill 30min 18% · séance 35% (62/159) · gap 2% · délai 24.8min · rebond 84% (54/62) (MFE +2.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.76% (p90 −3.49%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.88% (p90 −3.58%) → stop au-delà de −2.26% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.84% (p90 −2.82%) → stop au-delà de −1.94% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1132 jambes) : jambe baissière méd −1.31% (p90 −3.15%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (77 séances) :
      · −1.0% : fill 100% (77/77) · rebond 74% (58/77)
      · −2.0% : fill 89% (71/77) · rebond 74% (54/71)
      · −3.0% : fill 76% (61/77) · rebond 73% (46/61)
      · −4.0% : fill 59% (46/77) · rebond 73% (36/46)
      · −5.0% : fill 50% (39/77) · rebond 79% (32/39)
   - **flat** (16 séances) :
      · −1.0% : fill 71% (13/16) · rebond 87% (9/13)
      · −2.0% : fill 58% (12/16) · rebond 64% (6/12)
      · −3.0% : fill 48% (9/16) · rebond 69% (5/9)
      · −4.0% : fill 47% (8/16) · rebond 81% (4/8)
      · −5.0% : fill 27% (7/16) · rebond 91% (6/7)
   - **gap-up** (66 séances) :
      · −1.0% : fill 46% (36/66) · rebond 74% (27/36)
      · −2.0% : fill 29% (26/66) · rebond 51% (15/26)
      · −3.0% : fill 25% (22/66) · rebond 79% (17/22)
      · −4.0% : fill 20% (19/66) · rebond 79% (16/19)
      · −5.0% : fill 18% (16/66) · rebond 100% (16/16)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 59% si les 15 1res min sont vertes (80 cas) · 34% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:23** → P(séance verte=clôture>ouverture) 73% si début vert vs 22% si rouge (base 47% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 234min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **73%** · continue >prix actuel 50% ; creux résiduel méd -2.1% (q20 -3.63%) → **SL/trailing à −3.63%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.99% / q75 +3.47% → **scale +1.99% / runner +3.47%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **22%** (continue à baisser 50%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.37%** (au-delà de la MAE q10 -5.37%), cible rebond +2.06% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.17% .. +7.12%] · haut q95 +7.91% · bas q05 -5.74%
   - 60min (n=160) : retour [-5.01% .. +6.41%] · haut q95 +8.51% · bas q05 -6.32%
   - 2h (n=160) : retour [-6.15% .. +8.44%] · haut q95 +9.15% · bas q05 -7.06%
   - 4h (n=160) : retour [-7.19% .. +7.47%] · haut q95 +10.36% · bas q05 -8.1%
   - 6h (n=160) : retour [-7.27% .. +8.58%] · haut q95 +11.54% · bas q05 -8.38%
   - session (n=160) : retour [-6.86% .. +9.33%] · haut q95 +11.59% · bas q05 -8.38%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 7.7)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 16% vs absente 4% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.29% (p75 2.28% / p90 3.82%) · ~3.0 replis/séance, durée méd 69.04 min. P(nouveau plus-haut après repli) :
   - −0.5% → **85%** (reprise méd 24.37 min, n=47)
   - −1.0% → **78%** (reprise méd 68.85 min, n=30)
   - −1.5% → **68%** (reprise méd 81.24 min, n=16)
   - −2.0% → **67%** (reprise méd 84.17 min, n=12)
   - −3.0% → **75%** (reprise méd 175.72 min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−3.82%** (p90, défaut prudent ; serré/agressif −2.28%) ; extension open→close méd +8.23% (q75 +10.03% / q95 +16.4%), MFE méd +10.28% / q90 +13.1%
   - Échelle scale-out : +10.28% (33%) / +11.83% (33%) / +13.1% (34%)
- **DÉSARMER** : repli > **−3.82%** depuis le plus-haut = décay → P(retournement) **30%** (préavis méd 235.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.1% : P(retournement après) 0% (mèche méd 3.44%)
- **CONTEXTE** : la dernière heure tient les gains 80% du temps (retour médian dernière heure +0.52%)


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 73.5  _(surachat)_
- **ADX** : 25.3  _(tendance etablie)_
- **MACD** : hist 1.272  _(pas de croisement recent)_
- **BB** : %B 0.73 · largeur 49.5%
- **ATR** : 3.0 (24.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.025  _(neutre)_
- **Vol ratio** : 0.69  _(volume normal)_
- **Choppiness** : 39.2  _(transition)_
- **MA** : MA20 39.68 · MA50 45.47 · MA200 45.12  _(prix > MA20)_
- **Dist MA** : MA20 +11.2% · MA50 -3.0% · MA200 -2.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92658 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
