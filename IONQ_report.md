# IONQ

**Generated** : 2026-08-11T22:02:59.658013+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $43.44  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot $43.44 (+1.2% vs entrée) · entrée $42.91 · stop $39.92 · T1 $45.95 · R/R 1.02  
> ↳ P(T1 av. stop) 48 % _(réel 5 s)_ · EV/risk -0.053 _(réel 5 s)_ (GBM -0.078) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.130 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._
- 🔴 **Santé haussière vs sur-extension** — Santé technique 7/10 élevée alors que : extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $42.38–$43.44 (mid $42.91)
- Spot actuel : $43.44 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : $39.92 (stop swing_plan-based (-8.11%))
- Targets : T1 $45.95 · R/R 1.02 | T2 $49.00 · R/R 2.04 | T3 $52.04 · R/R 3.05
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $39.92


## Edge, scénarios & sizing

- EV/risk : -0.078 | EV/share : $-0.232 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 42 % | T2 22 % | T3 13 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 66.4 | bear 22.8 | side 10.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 478.0 (= 11 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.553% → cible +3.171% / stop −2.079%, p_fill 86%, n_eff≈36.5) : P(cible|rempli) **31%** · **EV/risk -0.068** (×p_fill ; si rempli -0.17% du capital)
  - **swing** (entrée dip −1.219% → cible +7.091% / stop −6.976%, p_fill 89%, n_eff≈38.7) : P(cible|rempli) **48%** · **EV/risk -0.053** (×p_fill ; si rempli -0.41% du capital)
  - **deep** (entrée dip −1.784% → cible +10.028% / stop −10.524%, p_fill 97%, n_eff≈38.0) : P(cible|rempli) **41%** · **EV/risk -0.163** (×p_fill ; si rempli -1.77% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→80% · +2.0%→66% · +3.0%→61% · +5.0%→31% · +8.0%→16%
- Range intraday médian 7.68% (p90 12.22%) · excursion haute méd. +3.69% / basse méd. −3.16%
- Profil de vol intra : ouverture 5.215% vs midi 1.517% vs clôture 1.715% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 17% · trend ↑0%/↓0% ; spike-down 70% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; neutre — autocorr -0.015)_ ; drift intra méd. 0.058% ; recovery-V 23%
- **σ réalisé intraday** 4.906% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 68% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 43.2551 (VA 42.6059–44.1826 ; dernier close 44.45)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 36% · rebond 83% · **stop −5.16%** sous le fill (sous le bruit) · cible +2.66% · R/R 0.52 (high win-rate)
- Gaps overnight (n=159) : méd. -0.24% · baisse 53% (gap-down >1% 38% · >2% 17%)
- Excursion ouverture 5min (n=160) : bas méd −1.16% (p90 −2.83%) · haut méd +1.2% · range méd 2.73%
- Excursion ouverture 15min (n=160) : bas méd −1.52% (p90 −4.13%) · haut méd +1.37% · range méd 3.7%
- Excursion ouverture 30min (n=160) : bas méd −1.87% (p90 −5.21%) · haut méd +1.98% · range méd 4.52%
- Excursion ouverture 60min (n=160) : bas méd −2.21% (p90 −5.89%) · haut méd +2.4% · range méd 5.58%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 44.45 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 80% (132/159) · gap 44% · délai 0.0min · rebond 66% (90/132) (MFE +1.88%)
   - −1.0% : fill 30min 66% · séance 74% (124/159) · gap 38% · délai 0.0min · rebond 75% (92/124) (MFE +2.35%)
   - −1.5% : fill 30min 64% · séance 72% (119/159) · gap 32% · délai 0.0min · rebond 68% (82/119) (MFE +2.52%)
   - −2.0% : fill 30min 56% · séance 65% (109/159) · gap 17% · délai 0.2min · rebond 68% (75/109) (MFE +2.53%)
   - −3.0% : fill 30min 45% · séance 55% (91/159) · gap 8% · délai 7.0min · rebond 73% (67/91) (MFE +2.77%)
   - −4.0% : fill 30min 29% · séance 43% (72/159) · gap 5% · délai 15.4min · rebond 74% (55/72) (MFE +2.39%)
   - −5.0% : fill 30min 18% · séance 36% (61/159) · gap 2% · délai 31.1min · rebond 83% (53/61) (MFE +2.66%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.82% (p90 −2.89%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.89% (p90 −2.93%) → stop au-delà de −2.27% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.89% (p90 −2.84%) → stop au-delà de −2.17% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1132 jambes) : jambe baissière méd −1.31% (p90 −3.14%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (74 séances) :
      · −1.0% : fill 100% (74/74) · rebond 75% (56/74)
      · −2.0% : fill 96% (70/74) · rebond 73% (53/70)
      · −3.0% : fill 81% (60/74) · rebond 72% (45/60)
      · −4.0% : fill 62% (45/74) · rebond 71% (35/45)
      · −5.0% : fill 52% (38/74) · rebond 77% (31/38)
   - **flat** (16 séances) :
      · −1.0% : fill 71% (13/16) · rebond 87% (9/13)
      · −2.0% : fill 58% (12/16) · rebond 64% (6/12)
      · −3.0% : fill 48% (9/16) · rebond 69% (5/9)
      · −4.0% : fill 47% (8/16) · rebond 81% (4/8)
      · −5.0% : fill 27% (7/16) · rebond 91% (6/7)
   - **gap-up** (69 séances) :
      · −1.0% : fill 45% (37/69) · rebond 71% (27/37)
      · −2.0% : fill 32% (27/69) · rebond 52% (16/27)
      · −3.0% : fill 27% (22/69) · rebond 79% (17/22)
      · −4.0% : fill 22% (19/69) · rebond 79% (16/19)
      · −5.0% : fill 19% (16/69) · rebond 100% (16/16)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 55% si les 15 1res min sont vertes (81 cas) · 29% si rouges (79 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:50** → P(séance verte=clôture>ouverture) 78% si début vert vs 17% si rouge (base 44% · écart 61 pts) ; prédictivité sature ensuite (plafond brut 198min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **78%** · continue >prix actuel 54% ; creux résiduel méd -2.07% (q20 -3.5%) → **SL/trailing à −3.5%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.96% / q75 +3.05% → **scale +1.96% / runner +3.05%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **17%** (continue à baisser 55%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.06%** (au-delà de la MAE q10 -4.06%), cible rebond +1.9% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.23% .. +7.16%] · haut q95 +8.03% · bas q05 -5.83%
   - 60min (n=160) : retour [-5.04% .. +6.34%] · haut q95 +8.91% · bas q05 -6.46%
   - 2h (n=160) : retour [-6.31% .. +8.49%] · haut q95 +10.43% · bas q05 -7.16%
   - 4h (n=160) : retour [-7.23% .. +7.63%] · haut q95 +11.8% · bas q05 -8.16%
   - 6h (n=160) : retour [-7.4% .. +9.14%] · haut q95 +11.94% · bas q05 -8.42%
   - session (n=160) : retour [-7.11% .. +9.41%] · haut q95 +11.94% · bas q05 -8.42%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 7.7)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **37%**. Lecture précoce 30 min : signature présente → 17% vs absente 5% (base 7%)
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
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 65.6  _(momentum haussier)_
- **ADX** : 26.3  _(tendance etablie)_
- **MACD** : hist 1.629  _(pas de croisement recent)_
- **BB** : %B 0.93 · largeur 39.5%
- **ATR** : 2.99 (25.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.126  _(distribution)_
- **Vol ratio** : 0.56  _(volume atone)_
- **Choppiness** : 44.9  _(transition)_
- **MA** : MA20 37.17 · MA50 47.55 · MA200 45.48  _(prix > MA20)_
- **Dist MA** : MA20 +16.9% · MA50 -8.6% · MA200 -4.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93404 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
