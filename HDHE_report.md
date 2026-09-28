# 267260

**Generated** : 2026-09-28T22:00:37.666608+00:00  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · ₩693000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot ₩693000.00 (+14.1% vs entrée) · entrée ₩607246.50 · stop ₩576603.65 · T1 ₩630688.97 · R/R 0.77  
> ↳ P(T1 av. stop) 75 % · EV/risk 0.232 · ¼-Kelly 0.002 · _first-passage empirique daily (historique réel, n≈207) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 934 % hors [0,100] (R² max 0.86). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.230 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩602558.01–₩611935.00 (mid ₩607246.50)
- Spot actuel : ₩693000.00 (+14.1% au-dessus de la zone — repli à attendre)
- Stop : ₩576603.65 (stop swing_plan-based (-16.8%))
- Targets : T1 ₩630688.97 · R/R 0.77 | T2 ₩654131.45 · R/R 1.53 | T3 ₩677573.92 · R/R 2.3
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩576603.65


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.10 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (16.8 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1219).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 16.8 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.67 % | p01 -4.805 % | pire -11.715 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0663** [0.0362 ; 0.1107] _(largeur 7.4 pt, n_eff 173.1)_
   - swing : **0.4107** [0.3598 ; 0.4631] _(largeur 10.3 pt, n_eff 345.6)_
   - deep : **0.348** [0.2992 ; 0.3993] _(largeur 10.0 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (47.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.68 %** | CVaR **-8.85 %** | vol 4.43 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 2.75 % contre 4.90 % aujourd'hui, rapport 0.56)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.96 % vs -11.99 % si l'on extrapolait par √5 _(rapport 0.914 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0357** (β de hausse 0.8391, asymétrie 1.2343) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.004 | EV/share : ₩129.020 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 56 % | T2 34 % | T3 20 %
- Kelly (position) : f* 0.006 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈207) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 85.7 | bear 7.1 | side 7.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −5.62% → cible +1.726% / stop −8.0%, p_fill 12%, n_eff≈14.8) : P(cible|rempli) **39%** · **EV/risk -0.014** (×p_fill ; si rempli -0.89% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=11, n_eff=6))
  - **deep** : indisponible (échantillon insuffisant (n=7, n_eff=6))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→64% · +2.0%→42% · +3.0%→35% · +5.0%→12% · +8.0%→4%
- Range intraday médian 6.64% (p90 10.49%) · excursion haute méd. +1.58% / basse méd. −4.07%
- Profil de vol intra : ouverture 4.476% vs midi 1.219% vs clôture 1.308% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 83% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.105 ; mean-reverting — autocorr -0.046)_ ; drift intra méd. -1.024% ; recovery-V 29%
- **σ réalisé intraday** 4.014% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 38% / bas 68% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 714037.5 (VA 710012.5–714037.5 ; dernier close 713000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 31% · rebond 79% · **stop −4.45%** sous le fill (sous le bruit) · cible +2.45% · R/R 0.55 (high win-rate)
- Gaps overnight (n=159) : méd. 0.91% · baisse 37% (gap-down >1% 19% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −1.72% (p90 −3.84%) · haut méd +0.86% · range méd 2.83%
- Excursion ouverture 15min (n=160) : bas méd −2.06% (p90 −4.32%) · haut méd +0.94% · range méd 3.5%
- Excursion ouverture 30min (n=160) : bas méd −2.27% (p90 −4.83%) · haut méd +1.03% · range méd 3.78%
- Excursion ouverture 60min (n=160) : bas méd −2.59% (p90 −5.0%) · haut méd +1.06% · range méd 4.12%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 714000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 74% (109/159) · gap 30% · délai 0.0min · rebond 51% (57/109) (MFE +1.06%)
   - −1.0% : fill 30min 56% · séance 70% (101/159) · gap 19% · délai 0.2min · rebond 58% (60/101) (MFE +1.31%)
   - −1.5% : fill 30min 50% · séance 66% (91/159) · gap 16% · délai 0.7min · rebond 64% (58/91) (MFE +1.27%)
   - −2.0% : fill 30min 42% · séance 60% (81/159) · gap 11% · délai 1.2min · rebond 69% (56/81) (MFE +1.66%)
   - −3.0% : fill 30min 34% · séance 48% (66/159) · gap 8% · délai 3.4min · rebond 75% (50/66) (MFE +1.92%)
   - −4.0% : fill 30min 23% · séance 39% (52/159) · gap 5% · délai 11.3min · rebond 75% (37/52) (MFE +2.1%)
   - −5.0% : fill 30min 16% · séance 31% (42/159) · gap 2% · délai 11.5min · rebond 79% (31/42) (MFE +2.45%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.92% (p90 −3.65%) → stop au-delà de −2.41% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.03% (p90 −3.14%) → stop au-delà de −2.41% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.23% (p90 −4.43%) → stop au-delà de −3.21% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=831 jambes) : jambe baissière méd −1.22% (p90 −3.26%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 100% (50/50) · rebond 44% (25/50)
      · −2.0% : fill 96% (44/50) · rebond 62% (27/44)
      · −3.0% : fill 88% (40/50) · rebond 75% (29/40)
      · −4.0% : fill 77% (34/50) · rebond 73% (24/34)
      · −5.0% : fill 63% (28/50) · rebond 84% (22/28)
   - **flat** (16 séances) :
      · −1.0% : fill 96% (15/16) · rebond 74% (10/15)
      · −2.0% : fill 73% (12/16) · rebond 73% (10/12)
      · −3.0% : fill 56% (10/16) · rebond 49% (7/10)
      · −4.0% : fill 51% (8/16) · rebond 62% (4/8)
      · −5.0% : fill 51% (8/16) · rebond 73% (6/8)
   - **gap-up** (93 séances) :
      · −1.0% : fill 47% (36/93) · rebond 70% (25/36)
      · −2.0% : fill 34% (25/93) · rebond 80% (19/25)
      · −3.0% : fill 22% (16/93) · rebond 89% (14/16)
      · −4.0% : fill 12% (10/93) · rebond 92% (9/10)
      · −5.0% : fill 7% (6/93) · rebond 55% (3/6)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 34% en base · 45% si les 15 1res min sont vertes (67 cas) · 29% si rouges (93 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:18** → P(séance verte=clôture>ouverture) 72% si début vert vs 15% si rouge (base 34% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=66) : tient le vert **72%** · continue >prix actuel 43% ; creux résiduel méd -1.79% (q20 -3.65%) → **SL/trailing à −3.65%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.57% / q75 +2.67% → **scale +1.57% / runner +2.67%**, sortie à la clôture
  - **si ROUGE au coude** (n=94) : edge inversé — récupère vert seulement **15%** (continue à baisser 38%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.72%** (au-delà de la MAE q10 -4.72%), cible rebond +1.58% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.93% .. +2.7%] · haut q95 +4.23% · bas q05 -5.45%
   - 60min (n=160) : retour [-5.58% .. +2.56%] · haut q95 +4.45% · bas q05 -5.92%
   - 2h (n=160) : retour [-6.24% .. +3.61%] · haut q95 +4.83% · bas q05 -7.08%
   - 4h (n=160) : retour [-6.83% .. +3.23%] · haut q95 +5.03% · bas q05 -8.32%
   - 6h (n=160) : retour [-6.97% .. +4.44%] · haut q95 +5.89% · bas q05 -8.86%
   - session (n=160) : retour [-7.15% .. +4.51%] · haut q95 +5.99% · bas q05 -9.19%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.51%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 45.2  _(neutre)_
- **ADX** : 10.8  _(pas de tendance nette)_
- **MACD** : hist -1593.772  _(pas de croisement recent)_
- **BB** : %B 0.19 · largeur 17.1%
- **ATR** : 30642.86 (4.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.226  _(distribution)_
- **Vol ratio** : 0.91  _(volume normal)_
- **Choppiness** : 63.6  _(marche en range (choppy))_
- **MA** : MA20 732100.0 · MA50 742983.05 · MA200 913590.71  _(prix < MA20)_
- **Dist MA** : MA20 -5.3% · MA50 -6.7% · MA200 -24.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (577031 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
