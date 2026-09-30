# 298040

**Generated** : 2026-09-30T21:59:06.473614+00:00  
**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · ₩2773000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot ₩2773000.00 (+1.8% vs entrée) · entrée ₩2725100.03 · stop ₩2507092.03 · T1 ₩2781707.18 · R/R 0.26  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 188 % hors [0,100] (R² max 0.81). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.150 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩2715422.84–₩2734777.23 (mid ₩2725100.03)
- Spot actuel : ₩2773000.00 (+1.8% au-dessus de la zone — repli à attendre)
- Stop : ₩2507092.03 (plancher anti-bruit 5 s — stop EV-optimal −8% (first-passage 5 s réel) ; -8.00 % depuis l'entree)
- Targets : T1 ₩2781707.18 · R/R 0.26 | T2 ₩2838314.32 · R/R 0.52 | T3 ₩2894921.46 · R/R 0.78
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2507092.03


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.20 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.19 %)** : le gap seul le franchit 0.082 % des séances (1 fois sur 1219).
   - exécution **2.496 pt plus bas** dans le cas TYPIQUE (médiane), 2.496 au p90, **2.496 au pire**
   - perte réelle **11.686 %** en moyenne _(tirée par la queue)_, jusqu'à **11.686 %** — au lieu des 9.19 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.002 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.475 % | p01 -4.657 % | pire -11.686 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0624** [0.0334 ; 0.1058] _(largeur 7.2 pt, n_eff 173.1)_
   - swing : **0.5042** [0.4516 ; 0.5567] _(largeur 10.5 pt, n_eff 345.6)_
   - deep : **0.5064** [0.4538 ; 0.5589] _(largeur 10.5 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.93 %** | CVaR **-9.26 %** | vol 4.94 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 3.50 % contre 5.73 % aujourd'hui, rapport 0.61)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -11.96 % vs -12.6 % si l'on extrapolait par √5 _(rapport 0.949 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0763** (β de hausse 0.9975, asymétrie 1.079) vs KS11 — 554 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.079 | EV/share : ₩-17314.312 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 48 % | T2 23 % | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.0 | bear 8.5 | side 6.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.728% → cible +2.077% / stop −8.0%, p_fill 71%, n_eff≈79.1) : P(cible|rempli) **44%** · **EV/risk -0.061** (×p_fill ; si rempli -0.69% du capital)
  - **swing** (entrée dip −3.805% → cible +11.196% / stop −5.598%, p_fill 60%, n_eff≈71.0) : P(cible|rempli) **26%** · **EV/risk -0.009** (×p_fill ; si rempli -0.09% du capital)
  - **deep** (entrée dip −5.868% → cible +13.645% / stop −6.822%, p_fill 59%, n_eff≈65.4) : P(cible|rempli) **22%** · **EV/risk -0.141** (×p_fill ; si rempli -1.63% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→77% · +1.0%→62% · +2.0%→50% · +3.0%→34% · +5.0%→18% · +8.0%→5%
- Range intraday médian 5.82% (p90 9.57%) · excursion haute méd. +2.0% / basse méd. −3.35%
- Profil de vol intra : ouverture 3.935% vs midi 1.034% vs clôture 1.056% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 76% · range 23% · trend ↑0%/↓0% ; spike-down 76% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; mean-reverting — autocorr -0.051)_ ; drift intra méd. -0.704% ; recovery-V 30%
- **σ réalisé intraday** 3.223% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 43% / bas 56% / whipsaw 10%
- POC intraday (dernière séance, temps-au-prix) : 2804350.0 (VA 2791750.0–2829550.0 ; dernier close 2801000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 27% · rebond 75% · **stop −4.27%** sous le fill (sous le bruit) · cible +2.24% · R/R 0.52 (high win-rate)
- Gaps overnight (n=152) : méd. 0.83% · baisse 34% (gap-down >1% 24% · >2% 17%)
- Excursion ouverture 5min (n=160) : bas méd −1.33% (p90 −3.0%) · haut méd +0.47% · range méd 2.13%
- Excursion ouverture 15min (n=160) : bas méd −1.79% (p90 −3.87%) · haut méd +0.78% · range méd 2.75%
- Excursion ouverture 30min (n=160) : bas méd −2.09% (p90 −4.2%) · haut méd +0.81% · range méd 3.28%
- Excursion ouverture 60min (n=160) : bas méd −2.27% (p90 −4.76%) · haut méd +1.1% · range méd 3.72%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2804000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 70% (100/152) · gap 30% · délai 0.1min · rebond 53% (55/100) (MFE +1.13%)
   - −1.0% : fill 30min 54% · séance 63% (92/152) · gap 24% · délai 0.4min · rebond 49% (48/92) (MFE +0.95%)
   - −1.5% : fill 30min 46% · séance 55% (82/152) · gap 20% · délai 2.3min · rebond 51% (45/82) (MFE +1.02%)
   - −2.0% : fill 30min 41% · séance 52% (76/152) · gap 17% · délai 3.6min · rebond 50% (38/76) (MFE +0.99%)
   - −3.0% : fill 30min 31% · séance 43% (63/152) · gap 9% · délai 7.1min · rebond 65% (40/63) (MFE +1.58%)
   - −4.0% : fill 30min 22% · séance 36% (55/152) · gap 5% · délai 21.8min · rebond 67% (40/55) (MFE +2.23%)
   - −5.0% : fill 30min 13% · séance 27% (41/152) · gap 4% · délai 57.8min · rebond 75% (30/41) (MFE +2.24%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.88% (p90 −2.88%) → stop au-delà de −2.03% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.96% (p90 −2.53%) → stop au-delà de −1.99% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.91% (p90 −2.46%) → stop au-delà de −1.89% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=838 jambes) : jambe baissière méd −1.33% (p90 −3.29%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (47 séances) :
      · −1.0% : fill 94% (46/47) · rebond 35% (22/46)
      · −2.0% : fill 90% (41/47) · rebond 43% (19/41)
      · −3.0% : fill 90% (40/47) · rebond 66% (25/40)
      · −4.0% : fill 78% (36/47) · rebond 69% (25/36)
      · −5.0% : fill 57% (27/47) · rebond 83% (21/27)
   - **flat** (20 séances) :
      · −1.0% : fill 85% (16/20) · rebond 65% (10/16)
      · −2.0% : fill 55% (13/20) · rebond 31% (5/13)
      · −3.0% : fill 30% (8/20) · rebond 57% (5/8)
      · −4.0% : fill 30% (8/20) · rebond 54% (6/8)
      · −5.0% : fill 23% (4/20) · rebond 40% (2/4)
   - **gap-up** (85 séances) :
      · −1.0% : fill 39% (30/85) · rebond 60% (16/30)
      · −2.0% : fill 28% (22/85) · rebond 72% (14/22)
      · −3.0% : fill 18% (15/85) · rebond 66% (10/15)
      · −4.0% : fill 13% (11/85) · rebond 66% (9/11)
      · −5.0% : fill 10% (10/85) · rebond 67% (7/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 40% en base · 60% si les 15 1res min sont vertes (57 cas) · 31% si rouges (103 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **46min** → P(séance verte=clôture>ouverture) 77% si début vert vs 20% si rouge (base 40% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 140min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=62) : tient le vert **77%** · continue >prix actuel 42% ; creux résiduel méd -1.61% (q20 -3.47%) → **SL/trailing à −3.47%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.66% / q75 +3.3% → **scale +1.66% / runner +3.3%**, sortie à la clôture
  - **si ROUGE au coude** (n=98) : edge inversé — récupère vert seulement **20%** (continue à baisser 55%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.48%** (au-delà de la MAE q10 -5.48%), cible rebond +1.28% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.6% .. +3.89%] · haut q95 +5.86% · bas q05 -5.13%
   - 60min (n=160) : retour [-5.02% .. +3.39%] · haut q95 +5.94% · bas q05 -5.46%
   - 2h (n=160) : retour [-5.46% .. +3.62%] · haut q95 +6.11% · bas q05 -6.34%
   - 4h (n=160) : retour [-6.39% .. +4.61%] · haut q95 +6.12% · bas q05 -7.92%
   - 6h (n=160) : retour [-7.34% .. +5.24%] · haut q95 +6.34% · bas q05 -8.46%
   - session (n=160) : retour [-6.64% .. +5.45%] · haut q95 +6.34% · bas q05 -8.88%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — 298040 = **volatil sans tendance propre (choppy)** (vol intra méd 3.7%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.12 · part idiosyncratique 0.88
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 46.0  _(neutre)_
- **ADX** : 6.1  _(pas de tendance nette)_
- **MACD** : hist -8055.313  _(bearish_recent)_
- **BB** : %B 0.29 · largeur 11.0%
- **ATR** : 113214.29 (15.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.149  _(distribution)_
- **Vol ratio** : 0.92  _(volume normal)_
- **Choppiness** : 59.6  _(transition)_
- **MA** : MA20 2837900.0 · MA50 2773580.0 · MA200 2828873.81  _(prix < MA20)_
- **Dist MA** : MA20 -2.3% · MA50 -0.0% · MA200 -2.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (551516 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
