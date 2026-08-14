# IONQ

**Generated** : 2026-08-14T22:04:20.293018+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite normal · $46.26  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $46.26 (+4.5% vs entrée) · entrée $44.26 · stop $41.21 · T1 $47.20 · R/R 0.96  
> ↳ P(T1 av. stop) 48 % _(réel 5 s)_ · EV/risk -0.058 _(réel 5 s)_ (GBM -0.043) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : triple_bullish (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.050 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._
- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $43.67–$44.85 (mid $44.26)
- Spot actuel : $46.26 (+4.5% au-dessus de la zone — repli à attendre)
- Stop : $41.21 (stop swing_plan-based (-10.91%))
- Targets : T1 $47.20 · R/R 0.96 | T2 $50.14 · R/R 1.93 | T3 $53.08 · R/R 2.89
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $41.21


## Edge, scénarios & sizing

- EV/risk : -0.043 | EV/share : $-0.130 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 27 % | T3 15 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 56.2 | bear 31.5 | side 12.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 601.0 (= 13 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.967% → cible +8.331% / stop −4.165%, p_fill 61%, n_eff≈27.3) : P(cible|rempli) **2%** · **EV/risk -0.127** (×p_fill ; si rempli -0.87% du capital)
  - **swing** (entrée dip −4.315% → cible +6.641% / stop −6.892%, p_fill 54%, n_eff≈26.8) : P(cible|rempli) **48%** · **EV/risk -0.058** (×p_fill ; si rempli -0.74% du capital)
  - **deep** (entrée dip −6.679% → cible +9.391% / stop −10.599%, p_fill 66%, n_eff≈26.9) : P(cible|rempli) **41%** · **EV/risk -0.170** (×p_fill ; si rempli -2.74% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→81% · +2.0%→68% · +3.0%→60% · +5.0%→30% · +8.0%→16%
- Range intraday médian 7.68% (p90 12.22%) · excursion haute méd. +3.66% / basse méd. −2.87%
- Profil de vol intra : ouverture 5.217% vs midi 1.49% vs clôture 1.696% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 17% · trend ↑0%/↓0% ; spike-down 71% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; neutre — autocorr -0.006)_ ; drift intra méd. 0.018% ; recovery-V 26%
- **σ réalisé intraday** 4.763% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 62% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 43.0019 (VA 42.5041–43.2281 ; dernier close 43.41)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 36% · rebond 84% · **stop −5.15%** sous le fill (sous le bruit) · cible +2.82% · R/R 0.55 (high win-rate)
- Gaps overnight (n=159) : méd. -0.24% · baisse 53% (gap-down >1% 38% · >2% 19%)
- Excursion ouverture 5min (n=160) : bas méd −1.16% (p90 −2.82%) · haut méd +1.23% · range méd 2.79%
- Excursion ouverture 15min (n=160) : bas méd −1.59% (p90 −4.09%) · haut méd +1.43% · range méd 3.7%
- Excursion ouverture 30min (n=160) : bas méd −1.91% (p90 −5.19%) · haut méd +1.98% · range méd 4.52%
- Excursion ouverture 60min (n=160) : bas méd −2.26% (p90 −5.87%) · haut méd +2.3% · range méd 5.37%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 43.41 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 81% (133/159) · gap 45% · délai 0.0min · rebond 65% (91/133) (MFE +1.88%)
   - −1.0% : fill 30min 66% · séance 73% (124/159) · gap 38% · délai 0.0min · rebond 73% (92/124) (MFE +2.34%)
   - −1.5% : fill 30min 64% · séance 72% (120/159) · gap 33% · délai 0.0min · rebond 66% (82/120) (MFE +2.45%)
   - −2.0% : fill 30min 56% · séance 65% (110/159) · gap 19% · délai 0.2min · rebond 69% (76/110) (MFE +2.42%)
   - −3.0% : fill 30min 45% · séance 55% (92/159) · gap 8% · délai 6.5min · rebond 74% (68/92) (MFE +2.49%)
   - −4.0% : fill 30min 30% · séance 44% (73/159) · gap 5% · délai 14.7min · rebond 75% (56/73) (MFE +2.52%)
   - −5.0% : fill 30min 19% · séance 36% (62/159) · gap 2% · délai 24.8min · rebond 84% (54/62) (MFE +2.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.73% (p90 −2.89%) → stop au-delà de −1.9% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.89% (p90 −2.89%) → stop au-delà de −2.2% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.89% (p90 −2.84%) → stop au-delà de −2.17% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1133 jambes) : jambe baissière méd −1.31% (p90 −3.12%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 100% (75/75) · rebond 72% (56/75)
      · −2.0% : fill 96% (71/75) · rebond 74% (54/71)
      · −3.0% : fill 82% (61/75) · rebond 73% (46/61)
      · −4.0% : fill 63% (46/75) · rebond 73% (36/46)
      · −5.0% : fill 54% (39/75) · rebond 79% (32/39)
   - **flat** (16 séances) :
      · −1.0% : fill 71% (13/16) · rebond 87% (9/13)
      · −2.0% : fill 58% (12/16) · rebond 64% (6/12)
      · −3.0% : fill 48% (9/16) · rebond 69% (5/9)
      · −4.0% : fill 47% (8/16) · rebond 81% (4/8)
      · −5.0% : fill 27% (7/16) · rebond 91% (6/7)
   - **gap-up** (68 séances) :
      · −1.0% : fill 43% (36/68) · rebond 71% (27/36)
      · −2.0% : fill 30% (27/68) · rebond 52% (16/27)
      · −3.0% : fill 26% (22/68) · rebond 79% (17/22)
      · −4.0% : fill 21% (19/68) · rebond 79% (16/19)
      · −5.0% : fill 18% (16/68) · rebond 100% (16/16)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 56% si les 15 1res min sont vertes (80 cas) · 31% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:23** → P(séance verte=clôture>ouverture) 70% si début vert vs 19% si rouge (base 44% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 234min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **70%** · continue >prix actuel 49% ; creux résiduel méd -2.1% (q20 -3.81%) → **SL/trailing à −3.81%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.98% / q75 +3.47% → **scale +1.98% / runner +3.47%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **19%** (continue à baisser 52%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.39%** (au-delà de la MAE q10 -5.39%), cible rebond +2.04% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.2% .. +7.16%] · haut q95 +7.94% · bas q05 -5.8%
   - 60min (n=160) : retour [-5.03% .. +5.94%] · haut q95 +8.73% · bas q05 -6.42%
   - 2h (n=160) : retour [-6.27% .. +8.46%] · haut q95 +9.87% · bas q05 -7.11%
   - 4h (n=160) : retour [-7.22% .. +7.56%] · haut q95 +11.18% · bas q05 -8.11%
   - 6h (n=160) : retour [-7.34% .. +8.9%] · haut q95 +11.9% · bas q05 -8.41%
   - session (n=160) : retour [-6.98% .. +9.33%] · haut q95 +11.9% · bas q05 -8.41%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 7.7)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **37%**. Lecture précoce 30 min : signature présente → 17% vs absente 4% (base 7%)
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

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : stretched_up
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

- **RSI** : 69.6  _(momentum haussier)_
- **ADX** : 25.9  _(tendance etablie)_
- **MACD** : hist 1.6  _(pas de croisement recent)_
- **BB** : %B 0.91 · largeur 48.2%
- **ATR** : 3.05 (26.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.054  _(distribution)_
- **Vol ratio** : 0.85  _(volume normal)_
- **Choppiness** : 36.9  _(marche directionnel)_
- **MA** : MA20 38.62 · MA50 46.1 · MA200 45.25  _(prix > MA20)_
- **Dist MA** : MA20 +19.8% · MA50 +0.3% · MA200 +2.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92786 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
