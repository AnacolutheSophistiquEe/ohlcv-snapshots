# PLTR

**Generated** : 2026-08-11T00:24:55.431131+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 9/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $175.23  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot $175.23 (+9.7% vs entrée) · entrée $159.77 · stop $150.14 · T1 $173.09 · R/R 1.38  
> ↳ P(T1 av. stop) 34 % · EV/risk -0.132 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 352 % hors [0,100] (R² max 0.40). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 9/10 élevée alors que : RSI 72.6 > 70 (surachat) ; %B 1.05 (collé à la bande haute) ; extension extrême (≥3×ATR, confluence MA20/50) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $157.10–$162.43 (mid $159.77)
- Spot actuel : $175.23 (+9.7% au-dessus de la zone — repli à attendre)
- Stop : $150.14 (stop swing_plan-based (-14.32%))
- Targets : T1 $173.09 · R/R 1.38 | T2 $186.42 · R/R 2.77 | T3 $199.74 · R/R 4.15
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $150.14


## Edge, scénarios & sizing

- EV/risk : -0.01 | EV/share : $-0.093 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 23 % | T2 8 % | T3 4 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 76.6 | side 18.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 526.0 (= 3 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=13, n_eff=8))
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→76% · +2.0%→46% · +3.0%→25% · +5.0%→9% · +8.0%→4%
- Range intraday médian 3.89% (p90 7.17%) · excursion haute méd. +1.88% / basse méd. −1.8%
- Profil de vol intra : ouverture 3.071% vs midi 0.737% vs clôture 0.864% _(ouverture ~4.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 76% · range 22% · trend ↑2%/↓0% ; spike-down 56% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.138 ; neutre — autocorr 0.008)_ ; drift intra méd. 0.827% ; recovery-V 32%
- **σ réalisé intraday** 2.911% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 44% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 170.7726 (VA 169.3114–171.0649 ; dernier close 171.99)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 58% · rebond 71% · **stop −4.36%** sous le fill (sous le bruit) · cible +1.38% · R/R 0.32 (high win-rate)
- Gaps overnight (n=159) : méd. -0.1% · baisse 56% (gap-down >1% 30% · >2% 15%)
- Excursion ouverture 5min (n=160) : bas méd −0.92% (p90 −2.11%) · haut méd +0.96% · range méd 2.02%
- Excursion ouverture 15min (n=160) : bas méd −1.07% (p90 −3.0%) · haut méd +1.17% · range méd 2.41%
- Excursion ouverture 30min (n=160) : bas méd −1.16% (p90 −3.5%) · haut méd +1.22% · range méd 2.86%
- Excursion ouverture 60min (n=160) : bas méd −1.37% (p90 −4.0%) · haut méd +1.38% · range méd 3.2%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 171.99 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 73% (117/159) · gap 39% · délai 0.0min · rebond 54% (64/117) (MFE +1.07%)
   - −1.0% : fill 30min 58% · séance 66% (108/159) · gap 30% · délai 0.0min · rebond 60% (63/108) (MFE +1.31%)
   - −1.5% : fill 30min 47% · séance 58% (94/159) · gap 24% · délai 0.1min · rebond 71% (61/94) (MFE +1.38%)
   - −2.0% : fill 30min 41% · séance 52% (79/159) · gap 15% · délai 1.4min · rebond 66% (50/79) (MFE +1.58%)
   - −3.0% : fill 30min 23% · séance 34% (56/159) · gap 8% · délai 4.0min · rebond 53% (26/56) (MFE +1.15%)
   - −4.0% : fill 30min 16% · séance 23% (40/159) · gap 5% · délai 12.5min · rebond 55% (20/40) (MFE +1.02%)
   - −5.0% : fill 30min 10% · séance 18% (28/159) · gap 2% · délai 25.3min · rebond 51% (13/28) (MFE +1.01%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −2.04%) → stop au-delà de −1.34% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.69% (p90 −2.13%) → stop au-delà de −1.33% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.48% (p90 −1.38%) → stop au-delà de −1.14% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=560 jambes) : jambe baissière méd −1.02% (p90 −2.53%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 93% (67/70) · rebond 60% (40/67)
      · −2.0% : fill 81% (57/70) · rebond 65% (37/57)
      · −3.0% : fill 56% (40/70) · rebond 50% (19/40)
      · −4.0% : fill 41% (30/70) · rebond 51% (14/30)
      · −5.0% : fill 34% (23/70) · rebond 58% (12/23)
   - **flat** (29 séances) :
      · −1.0% : fill 81% (24/29) · rebond 44% (12/24)
      · −2.0% : fill 62% (13/29) · rebond 65% (8/13)
      · −3.0% : fill 41% (10/29) · rebond 57% (5/10)
      · −4.0% : fill 25% (7/29) · rebond 84% (5/7)
      · −5.0% : fill 13% (3/29) · rebond 9% (1/3)
   - **gap-up** (60 séances) :
      · −1.0% : fill 28% (17/60) · rebond 73% (11/17)
      · −2.0% : fill 15% (9/60) · rebond 71% (5/9)
      · −3.0% : fill 6% (6/60) · rebond 66% (2/6)
      · −4.0% : fill 2% (3/60) · rebond 20% (1/3)
      · −5.0% : fill 1% (2/60) · rebond 0% (0/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 53% en base · 68% si les 15 1res min sont vertes (78 cas) · 36% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **49min** → P(séance verte=clôture>ouverture) 84% si début vert vs 23% si rouge (base 53% · écart 61 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **84%** · continue >prix actuel 62% ; creux résiduel méd -0.96% (q20 -1.95%) → **SL/trailing à −1.95%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.56% / q75 +2.58% → **scale +1.56% / runner +2.58%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **23%** (continue à baisser 48%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.29%** (au-delà de la MAE q10 -3.29%), cible rebond +1.39% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.93% .. +4.05%] · haut q95 +4.75% · bas q05 -4.16%
   - 60min (n=160) : retour [-3.8% .. +5.45%] · haut q95 +5.77% · bas q05 -4.46%
   - 2h (n=160) : retour [-4.04% .. +5.99%] · haut q95 +6.83% · bas q05 -4.73%
   - 4h (n=160) : retour [-4.4% .. +6.03%] · haut q95 +6.81% · bas q05 -5.71%
   - 6h (n=160) : retour [-5.02% .. +6.66%] · haut q95 +7.37% · bas q05 -6.26%
   - session (n=160) : retour [-4.82% .. +7.18%] · haut q95 +7.64% · bas q05 -6.26%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 2.5% / strong 3.7%) · base = 10 séances trend-up (n_eff 6.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **39%**. Lecture précoce 30 min : signature présente → 22% vs absente 2% (base 6%)
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
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : extreme
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

- **RSI** : 72.6  _(surachat)_
- **ADX** : 22.5  _(pas de tendance nette)_
- **MACD** : hist 5.405  _(pas de croisement recent)_
- **BB** : %B 1.05 · largeur 50.5%
- **ATR** : 9.63 (93.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.245  _(accumulation)_
- **Vol ratio** : 1.18  _(volume normal)_
- **Choppiness** : 29.6  _(marche directionnel)_
- **MA** : MA20 137.3 · MA50 133.24 · MA200 152.25  _(prix > MA20)_
- **Dist MA** : MA20 +27.6% · MA50 +31.5% · MA200 +15.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90934 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
