# PLTR

**Generated** : 2026-08-07T22:01:55.679395+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 9/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $172.01  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot $172.01 (+8.6% vs entrée) · entrée $158.32 · stop $149.05 · T1 $171.53 · R/R 1.43  
> ↳ P(T1 av. stop) 32 % · EV/risk -0.22 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 331 % hors [0,100] (R² max 0.40). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 9/10 élevée alors que : %B 1.12 (collé à la bande haute) ; extension extrême (≥3×ATR, confluence MA20/50) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $155.68–$160.96 (mid $158.32)
- Spot actuel : $172.01 (+8.6% au-dessus de la zone — repli à attendre)
- Stop : $149.05 (stop swing_plan-based (-13.35%))
- Targets : T1 $171.53 · R/R 1.43 | T2 $184.74 · R/R 2.85 | T3 $197.95 · R/R 4.28
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $149.05


## Edge, scénarios & sizing

- EV/risk : -0.061 | EV/share : $-0.562 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 22 % | T2 8 % | T3 3 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 73.7 | side 21.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 516.0 (= 3 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.62% → cible +3.732% / stop −8.0%, p_fill 20%, n_eff≈10.1) : P(cible|rempli) **0%** · **EV/risk +0.009** (×p_fill ; si rempli +0.38% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=4, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=5, n_eff=5))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→76% · +2.0%→46% · +3.0%→24% · +5.0%→8% · +8.0%→4%
- Range intraday médian 3.85% (p90 6.99%) · excursion haute méd. +1.88% / basse méd. −1.8%
- Profil de vol intra : ouverture 3.034% vs midi 0.735% vs clôture 0.861% _(ouverture ~4.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 20% · trend ↑2%/↓0% ; spike-down 57% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.127 ; neutre — autocorr 0.004)_ ; drift intra méd. 0.504% ; recovery-V 32%
- **σ réalisé intraday** 2.9% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 46% / whipsaw 13%
- POC intraday (dernière séance, temps-au-prix) : 155.818 (VA 155.05–156.714 ; dernier close 155.98)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 60% · rebond 71% · **stop −4.36%** sous le fill (sous le bruit) · cible +1.38% · R/R 0.32 (high win-rate)
- Gaps overnight (n=159) : méd. -0.14% · baisse 57% (gap-down >1% 31% · >2% 15%)
- Excursion ouverture 5min (n=160) : bas méd −0.96% (p90 −2.11%) · haut méd +0.95% · range méd 2.0%
- Excursion ouverture 15min (n=160) : bas méd −1.07% (p90 −3.0%) · haut méd +1.13% · range méd 2.39%
- Excursion ouverture 30min (n=160) : bas méd −1.16% (p90 −3.51%) · haut méd +1.18% · range méd 2.83%
- Excursion ouverture 60min (n=160) : bas méd −1.37% (p90 −4.0%) · haut méd +1.37% · range méd 3.08%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 155.98 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 75% (118/159) · gap 40% · délai 0.0min · rebond 54% (64/118) (MFE +1.07%)
   - −1.0% : fill 30min 60% · séance 67% (109/159) · gap 31% · délai 0.0min · rebond 60% (63/109) (MFE +1.31%)
   - −1.5% : fill 30min 48% · séance 60% (95/159) · gap 25% · délai 0.1min · rebond 71% (61/95) (MFE +1.38%)
   - −2.0% : fill 30min 42% · séance 53% (80/159) · gap 15% · délai 1.4min · rebond 66% (51/80) (MFE +1.58%)
   - −3.0% : fill 30min 24% · séance 35% (56/159) · gap 8% · délai 4.0min · rebond 53% (26/56) (MFE +1.15%)
   - −4.0% : fill 30min 17% · séance 24% (40/159) · gap 5% · délai 12.5min · rebond 55% (20/40) (MFE +1.02%)
   - −5.0% : fill 30min 10% · séance 18% (28/159) · gap 2% · délai 25.3min · rebond 51% (13/28) (MFE +1.01%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.44% (p90 −2.04%) → stop au-delà de −1.36% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.7% (p90 −2.13%) → stop au-delà de −1.34% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −1.38%) → stop au-delà de −1.16% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=560 jambes) : jambe baissière méd −1.02% (p90 −2.53%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (71 séances) :
      · −1.0% : fill 93% (68/71) · rebond 60% (40/68)
      · −2.0% : fill 81% (58/71) · rebond 65% (38/58)
      · −3.0% : fill 56% (40/71) · rebond 50% (19/40)
      · −4.0% : fill 40% (30/71) · rebond 51% (14/30)
      · −5.0% : fill 33% (23/71) · rebond 58% (12/23)
   - **flat** (29 séances) :
      · −1.0% : fill 81% (24/29) · rebond 44% (12/24)
      · −2.0% : fill 62% (13/29) · rebond 65% (8/13)
      · −3.0% : fill 41% (10/29) · rebond 57% (5/10)
      · −4.0% : fill 25% (7/29) · rebond 84% (5/7)
      · −5.0% : fill 13% (3/29) · rebond 9% (1/3)
   - **gap-up** (59 séances) :
      · −1.0% : fill 29% (17/59) · rebond 73% (11/17)
      · −2.0% : fill 16% (9/59) · rebond 71% (5/9)
      · −3.0% : fill 7% (6/59) · rebond 66% (2/6)
      · −4.0% : fill 2% (3/59) · rebond 20% (1/3)
      · −5.0% : fill 1% (2/59) · rebond 0% (0/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 67% si les 15 1res min sont vertes (77 cas) · 36% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **49min** → P(séance verte=clôture>ouverture) 83% si début vert vs 23% si rouge (base 52% · écart 61 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **83%** · continue >prix actuel 60% ; creux résiduel méd -0.98% (q20 -2.02%) → **SL/trailing à −2.02%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.47% / q75 +2.61% → **scale +1.47% / runner +2.61%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **23%** (continue à baisser 48%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.29%** (au-delà de la MAE q10 -3.29%), cible rebond +1.39% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.95% .. +3.79%] · haut q95 +4.05% · bas q05 -4.17%
   - 60min (n=160) : retour [-3.82% .. +3.9%] · haut q95 +4.78% · bas q05 -4.46%
   - 2h (n=160) : retour [-4.06% .. +5.54%] · haut q95 +5.66% · bas q05 -4.74%
   - 4h (n=160) : retour [-4.4% .. +5.64%] · haut q95 +6.4% · bas q05 -5.74%
   - 6h (n=160) : retour [-5.02% .. +5.73%] · haut q95 +6.82% · bas q05 -6.27%
   - session (n=160) : retour [-4.86% .. +4.88%] · haut q95 +6.82% · bas q05 -6.27%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 2.5% / strong 3.1%) · base = 9 séances trend-up (n_eff 6.3)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 18% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.79% (p75 1.05% / p90 1.52%) · ~3.91 replis/séance, durée méd 70.51 min. P(nouveau plus-haut après repli) :
   - −0.5% → **80%** (reprise méd 14.94 min, n=31)
   - −1.0% → **38%** (reprise méd 65.0 min, n=8)
   - −1.5% → **36%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.52%** (p90, défaut prudent ; serré/agressif −1.05%) ; extension open→close méd +4.69% (q75 +9.54% / q95 +12.13%), MFE méd +6.83% / q90 +13.49%
   - Échelle scale-out : +6.83% (33%) / +10.83% (33%) / +13.49% (34%)
- **DÉSARMER** : repli > **−1.52%** depuis le plus-haut = décay → P(retournement) **64%** (préavis méd 92.5 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.49% : P(retournement après) 0% (mèche méd 1.36%)
- **CONTEXTE** : la dernière heure tient les gains 52% du temps (retour médian dernière heure +-0.0%)


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 70.0  _(surachat)_
- **ADX** : 20.3  _(pas de tendance nette)_
- **MACD** : hist 4.79  _(bullish_recent)_
- **BB** : %B 1.12 · largeur 44.2%
- **ATR** : 9.27 (91.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.279  _(accumulation)_
- **Vol ratio** : 1.66  _(volume au-dessus de la moyenne)_
- **Choppiness** : 32.9  _(marche directionnel)_
- **MA** : MA20 135.04 · MA50 132.6 · MA200 152.28  _(prix > MA20)_
- **Dist MA** : MA20 +27.4% · MA50 +29.7% · MA200 +13.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91422 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
