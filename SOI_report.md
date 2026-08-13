# SOI

**Generated** : 2026-08-13T21:44:48.411285+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €133.20  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €133.20 (+1.0% vs entrée) · entrée €131.90 · stop €128.60 · T1 €136.10 · R/R 1.27  
> ↳ P(T1 av. stop) 42 % _(réel 5 s)_ · EV/risk -0.059 _(réel 5 s)_ (GBM 0.114) · ¼-Kelly 0.029 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 318 % hors [0,100] (R² max 0.13). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €131.06–€132.74 (mid €131.90)
- Spot actuel : €133.20 (+1.0% au-dessus de la zone — repli à attendre)
- Stop : €128.60 (stop swing_plan-based (-8.76%))
- Targets : T1 €136.10 · R/R 1.27 | T2 €141.37 · R/R 2.87 | T3 €146.64 · R/R 4.47
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €128.60


## Edge, scénarios & sizing

- EV/risk : 0.114 | EV/share : €0.376 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 47 % | T2 32 % | T3 32 %
- Kelly (position) : f* 0.118 | ¼-Kelly 0.029 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 28.3 | bear 8.3 | side 63.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 533.0 (= 4 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.974% → cible +3.184% / stop −2.5%, p_fill 86%, n_eff≈34.9) : P(cible|rempli) **42%** · **EV/risk -0.059** (×p_fill ; si rempli -0.17% du capital)
  - **swing** (entrée dip −2.149% → cible +8.33% / stop −6.756%, p_fill 70%, n_eff≈29.3) : P(cible|rempli) **45%** · **EV/risk -0.041** (×p_fill ; si rempli -0.40% du capital)
  - **deep** (entrée dip −3.313% → cible +11.781% / stop −10.257%, p_fill 82%, n_eff≈34.7) : P(cible|rempli) **25%** · **EV/risk -0.408** (×p_fill ; si rempli -5.08% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→79% · +2.0%→70% · +3.0%→56% · +5.0%→39% · +8.0%→18%
- Range intraday médian 9.07% (p90 15.49%) · excursion haute méd. +3.57% / basse méd. −3.75%
- Profil de vol intra : ouverture 5.67% vs midi 1.609% vs clôture 2.458% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (152 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 13% · trend ↑0%/↓1% ; spike-down 78% · recovery-V 44%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; mean-reverting — autocorr -0.097)_ ; drift intra méd. -0.23% ; recovery-V 44%
- **σ réalisé intraday** 5.351% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 74% / bas 60% / whipsaw 37%
- POC intraday (dernière séance, temps-au-prix) : 122.6412 (VA 120.3137–123.4988 ; dernier close 121.7)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 62% · rebond 79% · **stop −8.3%** sous le fill (sous le bruit) · cible +2.81% · R/R 0.34 (high win-rate)
- Gaps overnight (n=151) : méd. 0.41% · baisse 44% (gap-down >1% 30% · >2% 21%)
- Excursion ouverture 5min (n=152) : bas méd −1.16% (p90 −3.62%) · haut méd +1.0% · range méd 2.91%
- Excursion ouverture 15min (n=152) : bas méd −1.42% (p90 −4.98%) · haut méd +1.56% · range méd 3.55%
- Excursion ouverture 30min (n=152) : bas méd −1.58% (p90 −5.26%) · haut méd +1.84% · range méd 4.1%
- Excursion ouverture 60min (n=152) : bas méd −1.75% (p90 −5.84%) · haut méd +1.89% · range méd 4.52%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 121.7 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 80% (120/151) · gap 36% · délai 0.1min · rebond 66% (79/120) (MFE +2.15%)
   - −1.0% : fill 30min 60% · séance 76% (114/151) · gap 30% · délai 0.2min · rebond 73% (83/114) (MFE +2.07%)
   - −1.5% : fill 30min 53% · séance 70% (103/151) · gap 27% · délai 0.2min · rebond 74% (76/103) (MFE +2.27%)
   - −2.0% : fill 30min 48% · séance 62% (94/151) · gap 21% · délai 0.4min · rebond 79% (75/94) (MFE +2.81%)
   - −3.0% : fill 30min 35% · séance 50% (76/151) · gap 15% · délai 0.8min · rebond 75% (60/76) (MFE +2.91%)
   - −4.0% : fill 30min 28% · séance 42% (61/151) · gap 7% · délai 1.9min · rebond 74% (48/61) (MFE +2.43%)
   - −5.0% : fill 30min 21% · séance 38% (53/151) · gap 1% · délai 14.4min · rebond 78% (44/53) (MFE +2.79%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.79% (p90 −3.77%) → stop au-delà de −2.05% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.89% (p90 −3.01%) → stop au-delà de −2.2% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.9% (p90 −2.64%) → stop au-delà de −2.09% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1322 jambes) : jambe baissière méd −1.3% (p90 −3.14%) · ~17.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (58 séances) :
      · −1.0% : fill 98% (57/58) · rebond 63% (36/57)
      · −2.0% : fill 95% (55/58) · rebond 74% (43/55)
      · −3.0% : fill 82% (46/58) · rebond 74% (37/46)
      · −4.0% : fill 71% (40/58) · rebond 81% (33/40)
      · −5.0% : fill 64% (35/58) · rebond 87% (30/35)
   - **flat** (17 séances) :
      · −1.0% : fill 100% (17/17) · rebond 79% (14/17)
      · −2.0% : fill 96% (15/17) · rebond 82% (12/15)
      · −3.0% : fill 69% (11/17) · rebond 67% (8/11)
      · −4.0% : fill 57% (8/17) · rebond 65% (6/8)
      · −5.0% : fill 57% (8/17) · rebond 77% (7/8)
   - **gap-up** (76 séances) :
      · −1.0% : fill 55% (40/76) · rebond 84% (33/40)
      · −2.0% : fill 31% (24/76) · rebond 88% (20/24)
      · −3.0% : fill 22% (19/76) · rebond 83% (15/19)
      · −4.0% : fill 16% (13/76) · rebond 55% (9/13)
      · −5.0% : fill 14% (10/76) · rebond 47% (7/10)
- **P(clôture VERTE) selon le drive 15min** (n=152) : 52% en base · 67% si les 15 1res min sont vertes (72 cas) · 37% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=152) : COUDE à **37min** → P(séance verte=clôture>ouverture) 76% si début vert vs 31% si rouge (base 52% · écart 45 pts) ; prédictivité sature ensuite (plafond brut 276min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=69) : tient le vert **76%** · continue >prix actuel 57% ; creux résiduel méd -2.59% (q20 -5.94%) → **SL/trailing à −5.94%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.93% / q75 +4.86% → **scale +2.93% / runner +4.86%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **31%** (continue à baisser 58%) → **RÉDUIRE ~69%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.58%** (au-delà de la MAE q10 -8.58%), cible rebond +2.79% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=152) : retour [-5.22% .. +6.91%] · haut q95 +7.84% · bas q05 -6.46%
   - 60min (n=152) : retour [-5.88% .. +6.92%] · haut q95 +9.0% · bas q05 -6.84%
   - 2h (n=152) : retour [-5.99% .. +8.51%] · haut q95 +12.2% · bas q05 -7.38%
   - 4h (n=152) : retour [-6.71% .. +9.92%] · haut q95 +13.72% · bas q05 -8.07%
   - 6h (n=152) : retour [-7.54% .. +10.3%] · haut q95 +14.11% · bas q05 -9.42%
   - session (n=152) : retour [-10.87% .. +13.45%] · haut q95 +15.17% · bas q05 -12.49%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.9% des séances sont trend-up (mild 0% / strong 5.9%) · base = 9 séances trend-up (n_eff 5.7)
- **ARMER** : fenêtre la + prédictive = **60 min** → P(reste trend-up à la clôture) **14%**. Lecture précoce 30 min : signature présente → 5% vs absente 4% (base 6%)
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

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : stretched_up
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

- **RSI** : 62.9  _(momentum haussier)_
- **ADX** : 21.0  _(pas de tendance nette)_
- **MACD** : hist 3.588  _(pas de croisement recent)_
- **BB** : %B 0.9 · largeur 53.0%
- **ATR** : 8.81 (68.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.067  _(accumulation)_
- **Vol ratio** : 0.61  _(volume normal)_
- **Choppiness** : 40.8  _(transition)_
- **MA** : MA20 109.69 · MA50 115.77 · MA200 74.33  _(prix > MA20)_
- **Dist MA** : MA20 +21.4% · MA50 +15.1% · MA200 +79.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (99806 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
