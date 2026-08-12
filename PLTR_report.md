# PLTR

**Generated** : 2026-08-12T22:02:09.340091+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 10/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite high · $171.04  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot $171.04 (+8.3% vs entrée) · entrée $157.88 · stop $141.77 · T1 $190.10 · R/R 2.0  
> ↳ P(T1 av. stop) 5 % · EV/risk -0.136 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 121 % hors [0,100] (R² max 0.32). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : divergent_short_long (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 10/10 élevée alors que : RSI 76.8 > 70 (surachat) ; extension extrême (≥3×ATR, confluence MA20/50) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 10/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $155.22–$160.54 (mid $157.88)
- Spot actuel : $171.04 (+8.3% au-dessus de la zone — repli à attendre)
- Stop : $141.77 (stop swing_plan-based (-17.11%))
- Targets : T1 $190.10 · R/R 2.0 | T2 $193.87 · R/R 2.23 | T3 $197.64 · R/R 2.47
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $141.77


## Edge, scénarios & sizing

- EV/risk : 0.017 | EV/share : $0.273 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 5 % | T2 5 % | T3 4 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 71.7 | side 23.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 513.0 (= 3 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.493% → cible +6.73% / stop −3.365%, p_fill 17%, n_eff≈10.1) : P(cible|rempli) **0%** · **EV/risk +0.006** (×p_fill ; si rempli +0.13% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=6, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=5, n_eff=5))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→76% · +2.0%→49% · +3.0%→26% · +5.0%→10% · +8.0%→4%
- Range intraday médian 3.89% (p90 7.17%) · excursion haute méd. +1.9% / basse méd. −1.71%
- Profil de vol intra : ouverture 3.075% vs midi 0.75% vs clôture 0.858% _(ouverture ~4.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 21% · trend ↑2%/↓0% ; spike-down 54% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.132 ; neutre — autocorr 0.008)_ ; drift intra méd. 0.885% ; recovery-V 32%
- **σ réalisé intraday** 2.877% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 62% / bas 45% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 175.1387 (VA 174.8837–176.4137 ; dernier close 174.94)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 56% · rebond 71% · **stop −4.36%** sous le fill (sous le bruit) · cible +1.38% · R/R 0.32 (high win-rate)
- Gaps overnight (n=159) : méd. -0.2% · baisse 58% (gap-down >1% 29% · >2% 14%)
- Excursion ouverture 5min (n=160) : bas méd −0.86% (p90 −2.1%) · haut méd +0.96% · range méd 2.02%
- Excursion ouverture 15min (n=160) : bas méd −0.99% (p90 −2.88%) · haut méd +1.17% · range méd 2.41%
- Excursion ouverture 30min (n=160) : bas méd −1.09% (p90 −3.5%) · haut méd +1.3% · range méd 2.86%
- Excursion ouverture 60min (n=160) : bas méd −1.32% (p90 −3.93%) · haut méd +1.47% · range méd 3.2%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 174.94 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 74% (117/159) · gap 41% · délai 0.0min · rebond 57% (66/117) (MFE +1.15%)
   - −1.0% : fill 30min 56% · séance 65% (107/159) · gap 29% · délai 0.0min · rebond 61% (63/107) (MFE +1.31%)
   - −1.5% : fill 30min 45% · séance 56% (92/159) · gap 24% · délai 0.1min · rebond 71% (61/92) (MFE +1.38%)
   - −2.0% : fill 30min 40% · séance 50% (79/159) · gap 14% · délai 1.4min · rebond 66% (50/79) (MFE +1.58%)
   - −3.0% : fill 30min 22% · séance 33% (56/159) · gap 8% · délai 4.0min · rebond 53% (26/56) (MFE +1.15%)
   - −4.0% : fill 30min 16% · séance 22% (40/159) · gap 5% · délai 12.5min · rebond 55% (20/40) (MFE +1.02%)
   - −5.0% : fill 30min 10% · séance 17% (28/159) · gap 1% · délai 25.3min · rebond 51% (13/28) (MFE +1.01%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.34% (p90 −2.03%) → stop au-delà de −1.32% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.62% (p90 −2.01%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.45% (p90 −1.38%) → stop au-delà de −1.12% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=563 jambes) : jambe baissière méd −1.02% (p90 −2.51%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (72 séances) :
      · −1.0% : fill 90% (68/72) · rebond 62% (41/68)
      · −2.0% : fill 75% (57/72) · rebond 65% (37/57)
      · −3.0% : fill 52% (40/72) · rebond 50% (19/40)
      · −4.0% : fill 38% (30/72) · rebond 51% (14/30)
      · −5.0% : fill 31% (23/72) · rebond 58% (12/23)
   - **flat** (27 séances) :
      · −1.0% : fill 81% (22/27) · rebond 44% (11/22)
      · −2.0% : fill 63% (13/27) · rebond 65% (8/13)
      · −3.0% : fill 41% (10/27) · rebond 57% (5/10)
      · −4.0% : fill 26% (7/27) · rebond 84% (5/7)
      · −5.0% : fill 13% (3/27) · rebond 9% (1/3)
   - **gap-up** (60 séances) :
      · −1.0% : fill 28% (17/60) · rebond 73% (11/17)
      · −2.0% : fill 15% (9/60) · rebond 71% (5/9)
      · −3.0% : fill 6% (6/60) · rebond 66% (2/6)
      · −4.0% : fill 2% (3/60) · rebond 20% (1/3)
      · −5.0% : fill 1% (2/60) · rebond 0% (0/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 55% en base · 71% si les 15 1res min sont vertes (79 cas) · 36% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **49min** → P(séance verte=clôture>ouverture) 85% si début vert vs 23% si rouge (base 55% · écart 62 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **85%** · continue >prix actuel 57% ; creux résiduel méd -0.98% (q20 -1.81%) → **SL/trailing à −1.81%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.56% / q75 +2.53% → **scale +1.56% / runner +2.53%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **23%** (continue à baisser 48%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.29%** (au-delà de la MAE q10 -3.29%), cible rebond +1.4% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.89% .. +3.94%] · haut q95 +4.66% · bas q05 -4.13%
   - 60min (n=160) : retour [-3.76% .. +5.28%] · haut q95 +5.58% · bas q05 -4.46%
   - 2h (n=160) : retour [-4.01% .. +5.92%] · haut q95 +6.77% · bas q05 -4.7%
   - 4h (n=160) : retour [-4.38% .. +5.87%] · haut q95 +6.78% · bas q05 -5.65%
   - 6h (n=160) : retour [-4.99% .. +6.57%] · haut q95 +7.36% · bas q05 -6.24%
   - session (n=160) : retour [-4.75% .. +6.97%] · haut q95 +7.57% · bas q05 -6.24%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 2.5% / strong 3.7%) · base = 10 séances trend-up (n_eff 6.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **36%**. Lecture précoce 30 min : signature présente → 21% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.81% (p75 1.11% / p90 1.47%) · ~3.0 replis/séance, durée méd 75.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **83%** (reprise méd 30.0 min, n=33)
   - −1.0% → **51%** (reprise méd 64.44 min, n=9)
   - −1.5% → **36%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.47%** (p90, défaut prudent ; serré/agressif −1.11%) ; extension open→close méd +6.19% (q75 +7.89% / q95 +12.13%), MFE méd +7.32% / q90 +13.49%
   - Échelle scale-out : +7.32% (33%) / +9.14% (33%) / +13.49% (34%)
- **DÉSARMER** : repli > **−1.47%** depuis le plus-haut = décay → P(retournement) **64%** (préavis méd 92.5 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.49% : P(retournement après) 0% (mèche méd 1.36%)
- **CONTEXTE** : la dernière heure tient les gains 62% du temps (retour médian dernière heure +0.21%)


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 76.8  _(surachat)_
- **ADX** : 25.7  _(tendance etablie)_
- **MACD** : hist 4.904  _(pas de croisement recent)_
- **BB** : %B 0.86 · largeur 57.9%
- **ATR** : 9.42 (91.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.209  _(accumulation)_
- **Vol ratio** : 0.75  _(volume normal)_
- **Choppiness** : 28.8  _(marche directionnel)_
- **MA** : MA20 141.22 · MA50 133.81 · MA200 152.2  _(prix > MA20)_
- **Dist MA** : MA20 +21.1% · MA50 +27.8% · MA200 +12.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91973 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
