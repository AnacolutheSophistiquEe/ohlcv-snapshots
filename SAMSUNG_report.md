# 005930

**Generated** : 2026-08-21T21:51:01.588272+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 8.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩281500.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩281500.00 (+1.7% vs entrée) · entrée ₩276857.96 · stop ₩264203.55 · T1 ₩302166.77 · R/R 2.0  
> ↳ P(T1 av. stop) 1 % _(réel 5 s)_ · EV/risk -0.117 _(réel 5 s)_ (GBM -0.132) · ¼-Kelly 0.022 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.57% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.090 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._
- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩274385.54–₩279330.37 (mid ₩276857.96)
- Spot actuel : ₩281500.00 (+1.7% au-dessus de la zone — repli à attendre)
- Stop : ₩264203.55 (stop swing_plan-based (-9.84%))
- Targets : T1 ₩302166.77 · R/R 2.0 | T2 ₩307999.31 · R/R 2.46 | T3 ₩313831.84 · R/R 2.92
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩264203.55


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.61 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.84 %)** : le gap seul le franchit 0.082 % des séances (1 fois sur 1218).
   - exécution **1.102 pt plus bas** dans le cas TYPIQUE (médiane), 1.102 au p90, **1.102 au pire**
   - perte réelle **10.942 %** en moyenne _(tirée par la queue)_, jusqu'à **10.942 %** — au lieu des 9.84 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0009 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.284 % | p01 -4.951 % | pire -10.942 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2031** [0.1484 ; 0.2677] _(largeur 11.9 pt, n_eff 173.1)_
   - swing : **0.3054** [0.2586 ; 0.3554] _(largeur 9.7 pt, n_eff 345.6)_
   - deep : **0.3614** [0.3121 ; 0.413] _(largeur 10.1 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (29.1 pt), swing (33.5 pt), deep (34.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.29 %** | CVaR **-9.74 %** | vol 4.66 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 3.04 % contre 6.10 % aujourd'hui, rapport 0.50)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.29 % vs -6.91 % si l'on extrapolait par √5 _(rapport 0.911 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1611** (β de hausse 1.3389, asymétrie 0.8671) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.132 | EV/share : ₩-1664.790 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 24 % | T2 24 % | T3 24 %
- Kelly (position) : f* 0.086 | ¼-Kelly 0.022 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 73.5 | bear 7.1 | side 19.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.644% → cible +9.141% / stop −4.571%, p_fill 83%, n_eff≈32.9) : P(cible|rempli) **1%** · **EV/risk -0.117** (×p_fill ; si rempli -0.65% du capital)
  - **swing** (entrée dip −3.623% → cible +9.954% / stop −6.451%, p_fill 62%, n_eff≈28.1) : P(cible|rempli) **14%** · **EV/risk -0.310** (×p_fill ; si rempli -3.24% du capital)
  - **deep** (entrée dip −5.605% → cible +14.077% / stop −9.879%, p_fill 78%, n_eff≈28.0) : P(cible|rempli) **32%** · **EV/risk -0.153** (×p_fill ; si rempli -1.93% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→70% · +2.0%→45% · +3.0%→36% · +5.0%→25% · +8.0%→5%
- Range intraday médian 6.24% (p90 9.84%) · excursion haute méd. +1.88% / basse méd. −3.12%
- Profil de vol intra : ouverture 3.165% vs midi 1.375% vs clôture 1.581% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (158 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑0%/↓1% ; spike-down 72% · recovery-V 21%)_
- **Régime intraday** : **chop** _(efficiency 0.129 ; mean-reverting — autocorr -0.092)_ ; drift intra méd. -0.969% ; recovery-V 21%
- **σ réalisé intraday** 4.259% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 75% / whipsaw 25%
- POC intraday (dernière séance, temps-au-prix) : 269668.75 (VA 267106.25–271718.75 ; dernier close 271000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 29% · rebond 54% · **stop −6.67%** sous le fill (sous le bruit) · cible +1.2% · R/R 0.18 (high win-rate)
- Gaps overnight (n=157) : méd. 0.78% · baisse 41% (gap-down >1% 32% · >2% 24%)
- Excursion ouverture 5min (n=158) : bas méd −0.77% (p90 −1.64%) · haut méd +0.6% · range méd 1.58%
- Excursion ouverture 15min (n=158) : bas méd −1.03% (p90 −2.6%) · haut méd +1.03% · range méd 2.23%
- Excursion ouverture 30min (n=158) : bas méd −1.25% (p90 −3.13%) · haut méd +1.15% · range méd 2.69%
- Excursion ouverture 60min (n=158) : bas méd −1.75% (p90 −3.58%) · haut méd +1.31% · range méd 3.12%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 271000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 50% · séance 64% (97/157) · gap 34% · délai 0.0min · rebond 48% (51/97) (MFE +0.88%)
   - −1.0% : fill 30min 46% · séance 62% (91/157) · gap 32% · délai 0.0min · rebond 59% (52/91) (MFE +1.22%)
   - −1.5% : fill 30min 40% · séance 54% (79/157) · gap 25% · délai 0.3min · rebond 58% (47/79) (MFE +1.34%)
   - −2.0% : fill 30min 36% · séance 48% (70/157) · gap 24% · délai 0.2min · rebond 56% (40/70) (MFE +1.57%)
   - −3.0% : fill 30min 29% · séance 45% (61/157) · gap 19% · délai 1.7min · rebond 58% (39/61) (MFE +1.75%)
   - −4.0% : fill 30min 22% · séance 36% (48/157) · gap 15% · délai 22.5min · rebond 55% (31/48) (MFE +1.33%)
   - −5.0% : fill 30min 14% · séance 29% (37/157) · gap 11% · délai 47.6min · rebond 54% (23/37) (MFE +1.2%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.52% (p90 −2.11%) → stop au-delà de −1.67% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.66% (p90 −3.07%) → stop au-delà de −1.64% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.68% (p90 −3.22%) → stop au-delà de −1.75% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=746 jambes) : jambe baissière méd −1.28% (p90 −3.07%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (64 séances) :
      · −1.0% : fill 98% (61/64) · rebond 41% (30/61)
      · −2.0% : fill 90% (53/64) · rebond 42% (26/53)
      · −3.0% : fill 88% (48/64) · rebond 49% (29/48)
      · −4.0% : fill 79% (40/64) · rebond 46% (24/40)
      · −5.0% : fill 70% (32/64) · rebond 48% (18/32)
   - **flat** (14 séances) :
      · −1.0% : fill 65% (8/14) · rebond 78% (5/8)
      · −2.0% : fill 33% (4/14) · rebond 85% (3/4)
      · −3.0% : fill 33% (4/14) · rebond 85% (3/4)
      · −4.0% : fill 15% (2/14) · rebond 100% (2/2)
      · −5.0% : fill 15% (2/14) · rebond 100% (2/2)
   - **gap-up** (79 séances) :
      · −1.0% : fill 37% (22/79) · rebond 84% (17/22)
      · −2.0% : fill 22% (13/79) · rebond 86% (11/13)
      · −3.0% : fill 17% (9/79) · rebond 81% (7/9)
      · −4.0% : fill 11% (6/79) · rebond 94% (5/6)
      · −5.0% : fill 4% (3/79) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=158) : 37% en base · 58% si les 15 1res min sont vertes (79 cas) · 16% si rouges (79 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=158) : COUDE à **1:15** → P(séance verte=clôture>ouverture) 82% si début vert vs 5% si rouge (base 37% · écart 77 pts) ; prédictivité sature ensuite (plafond brut 75min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **82%** · continue >prix actuel 57% ; creux résiduel méd -1.15% (q20 -3.87%) → **SL/trailing à −3.87%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.1% / q75 +3.47% → **scale +2.1% / runner +3.47%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **5%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.96%** (au-delà de la MAE q10 -6.96%), cible rebond +1.3% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=158) : retour [-2.82% .. +2.8%] · haut q95 +3.67% · bas q05 -3.74%
   - 60min (n=158) : retour [-3.14% .. +4.37%] · haut q95 +5.31% · bas q05 -5.13%
   - 2h (n=158) : retour [-4.61% .. +4.75%] · haut q95 +6.08% · bas q05 -6.07%
   - 4h (n=158) : retour [-6.24% .. +5.57%] · haut q95 +6.87% · bas q05 -7.77%
   - 6h (n=158) : retour [-7.2% .. +5.06%] · haut q95 +7.0% · bas q05 -8.08%
   - session (n=158) : retour [-7.38% .. +5.44%] · haut q95 +7.0% · bas q05 -8.63%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.8% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.95%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : stretched_up
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

- **RSI** : 56.2  _(momentum haussier)_
- **ADX** : 18.4  _(pas de tendance nette)_
- **MACD** : hist 6366.005  _(pas de croisement recent)_
- **BB** : %B 0.92 · largeur 34.5%
- **ATR** : 17500.0 (72.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.089  _(distribution)_
- **Vol ratio** : 0.9  _(volume normal)_
- **Choppiness** : 53.0  _(transition)_
- **MA** : MA20 246225.0 · MA50 281870.41 · MA200 203601.86  _(prix > MA20)_
- **Dist MA** : MA20 +14.3% · MA50 -0.1% · MA200 +38.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (608936 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
