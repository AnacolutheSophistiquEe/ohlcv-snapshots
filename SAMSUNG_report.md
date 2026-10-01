# 005930

**Generated** : 2026-10-01T21:54:19.448731+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩276000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot ₩276000.00 (+8.4% vs entrée) · entrée ₩254714.47 · stop ₩242495.81 · T1 ₩279151.79 · R/R 2.0  
> ↳ ¼-Kelly 0.052 · _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩252828.21–₩256600.74 (mid ₩254714.47)
- Spot actuel : ₩276000.00 (+8.4% au-dessus de la zone — repli à attendre)
- Stop : ₩242495.81 (R/R 2 (resserré, parité Claude) ; -4.80 % depuis l'entree)
- Targets : T1 ₩279151.79 · R/R 2.0 | T2 ₩290172.41 · R/R 2.9 | T3 ₩301193.03 · R/R 3.8
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩242495.81


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.10 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.14 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1219).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 12.14 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.482 % | p01 -4.95 % | pire -10.942 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4646** [0.3914 ; 0.539] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.351** [0.3021 ; 0.4024] _(largeur 10.0 pt, n_eff 345.6)_
   - deep : **0.3255** [0.2777 ; 0.3762] _(largeur 9.8 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.4 pt), swing (36.7 pt), deep (38.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.71 %** | CVaR **-9.83 %** | vol 4.75 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 2.94 % contre 5.58 % aujourd'hui, rapport 0.53)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.38 % vs -7.35 % si l'on extrapolait par √5 _(rapport 0.869 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1733** (β de hausse 1.3385, asymétrie 0.8766) vs KS11 — 554 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.347 | EV/share : ₩4239.729 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 18 % | T3 9 %
- Kelly (position) : f* 0.208 | ¼-Kelly 0.052 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 31.5 | bear 5.0 | side 63.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 539.0 (= 3 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.503% → cible +1.851% / stop −1.5%, p_fill 30%, n_eff≈34.2) : P(cible|rempli) **29%** · **EV/risk -0.124** (×p_fill ; si rempli -0.63% du capital)
  - **swing** (entrée dip −7.713% → cible +9.594% / stop −4.797%, p_fill 21%, n_eff≈24.7) : P(cible|rempli) **29%** · **EV/risk -0.006** (×p_fill ; si rempli -0.15% du capital)
  - **deep** (entrée dip −11.92% → cible +14.828% / stop −7.414%, p_fill 19%, n_eff≈20.9) : P(cible|rempli) **9%** · **EV/risk -0.071** (×p_fill ; si rempli -2.81% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→67% · +2.0%→44% · +3.0%→30% · +5.0%→18% · +8.0%→3%
- Range intraday médian 4.91% (p90 9.02%) · excursion haute méd. +1.83% / basse méd. −2.09%
- Profil de vol intra : ouverture 2.598% vs midi 1.135% vs clôture 1.275% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑0%/↓1% ; spike-down 58% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; mean-reverting — autocorr -0.09)_ ; drift intra méd. -0.242% ; recovery-V 21%
- **σ réalisé intraday** 2.702% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 62% / bas 71% / whipsaw 34%
- POC intraday (dernière séance, temps-au-prix) : 269093.75 (VA 268881.25–272918.75 ; dernier close 269500.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 18% · rebond 48% · **stop −6.28%** sous le fill (sous le bruit) · cible +0.83% · R/R 0.13 (high win-rate)
- Gaps overnight (n=152) : méd. 0.73% · baisse 43% (gap-down >1% 32% · >2% 22%)
- Excursion ouverture 5min (n=160) : bas méd −0.53% (p90 −1.44%) · haut méd +0.58% · range méd 1.27%
- Excursion ouverture 15min (n=160) : bas méd −0.85% (p90 −2.21%) · haut méd +0.73% · range méd 1.88%
- Excursion ouverture 30min (n=160) : bas méd −1.0% (p90 −2.77%) · haut méd +0.92% · range méd 2.21%
- Excursion ouverture 60min (n=160) : bas méd −1.18% (p90 −3.41%) · haut méd +1.17% · range méd 2.81%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 268500.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 47% · séance 64% (91/152) · gap 34% · délai 0.0min · rebond 47% (43/91) (MFE +0.92%)
   - −1.0% : fill 30min 41% · séance 55% (82/152) · gap 32% · délai 0.0min · rebond 55% (43/82) (MFE +1.1%)
   - −1.5% : fill 30min 35% · séance 46% (71/152) · gap 25% · délai 0.0min · rebond 56% (38/71) (MFE +1.38%)
   - −2.0% : fill 30min 31% · séance 42% (66/152) · gap 22% · délai 0.0min · rebond 56% (37/66) (MFE +1.24%)
   - −3.0% : fill 30min 25% · séance 35% (57/152) · gap 21% · délai 0.0min · rebond 47% (30/57) (MFE +0.92%)
   - −4.0% : fill 30min 19% · séance 29% (45/152) · gap 9% · délai 4.0min · rebond 54% (26/45) (MFE +1.18%)
   - −5.0% : fill 30min 9% · séance 18% (32/152) · gap 6% · délai 42.7min · rebond 48% (19/32) (MFE +0.83%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.45% (p90 −1.78%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.41% (p90 −2.52%) → stop au-delà de −1.32% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.44% (p90 −2.45%) → stop au-delà de −1.61% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=737 jambes) : jambe baissière méd −1.2% (p90 −2.89%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 97% (54/56) · rebond 47% (24/54)
      · −2.0% : fill 82% (47/56) · rebond 42% (22/47)
      · −3.0% : fill 77% (45/56) · rebond 44% (23/45)
      · −4.0% : fill 67% (37/56) · rebond 51% (21/37)
      · −5.0% : fill 43% (27/56) · rebond 38% (14/27)
   - **flat** (15 séances) :
      · −1.0% : fill 57% (11/15) · rebond 64% (6/11)
      · −2.0% : fill 41% (7/15) · rebond 85% (5/7)
      · −3.0% : fill 18% (4/15) · rebond 18% (1/4)
      · −4.0% : fill 12% (2/15) · rebond 0% (0/2)
      · −5.0% : fill 12% (2/15) · rebond 100% (2/2)
   - **gap-up** (81 séances) :
      · −1.0% : fill 25% (17/81) · rebond 72% (13/17)
      · −2.0% : fill 16% (12/81) · rebond 86% (10/12)
      · −3.0% : fill 10% (8/81) · rebond 78% (6/8)
      · −4.0% : fill 7% (6/81) · rebond 93% (5/6)
      · −5.0% : fill 3% (3/81) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 41% en base · 61% si les 15 1res min sont vertes (78 cas) · 22% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:17** → P(séance verte=clôture>ouverture) 79% si début vert vs 11% si rouge (base 41% · écart 68 pts) ; prédictivité sature ensuite (plafond brut 227min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **79%** · continue >prix actuel 61% ; creux résiduel méd -1.05% (q20 -2.59%) → **SL/trailing à −2.59%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.52% / q75 +3.08% → **scale +1.52% / runner +3.08%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **11%** (continue à baisser 57%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.84%** (au-delà de la MAE q10 -5.84%), cible rebond +0.96% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.69% .. +2.46%] · haut q95 +3.18% · bas q05 -3.58%
   - 60min (n=160) : retour [-2.82% .. +3.7%] · haut q95 +4.65% · bas q05 -3.68%
   - 2h (n=160) : retour [-4.21% .. +4.5%] · haut q95 +5.68% · bas q05 -5.22%
   - 4h (n=160) : retour [-5.67% .. +5.05%] · haut q95 +6.31% · bas q05 -7.07%
   - 6h (n=160) : retour [-6.0% .. +5.02%] · haut q95 +6.78% · bas q05 -7.27%
   - session (n=160) : retour [-5.64% .. +5.32%] · haut q95 +6.78% · bas q05 -7.27%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (4) pour des stats fiables : 2.5% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.92%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.28 · part idiosyncratique 0.72
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 53.6  _(neutre)_
- **ADX** : 8.7  _(pas de tendance nette)_
- **MACD** : hist 1408.745  _(pas de croisement recent)_
- **BB** : %B 0.77 · largeur 16.7%
- **ATR** : 9857.14 (45.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.015  _(neutre)_
- **Vol ratio** : 0.82  _(volume normal)_
- **Choppiness** : 47.4  _(transition)_
- **MA** : MA20 264050.0 · MA50 256290.0 · MA200 225514.28  _(prix > MA20)_
- **Dist MA** : MA20 +4.5% · MA50 +7.7% · MA200 +22.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (557989 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
