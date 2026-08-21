# 207940

**Generated** : 2026-08-21T00:21:31.633508+00:00  
**Santé technique** : 9/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1574000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩1574000.00 (+0.3% vs entrée) · entrée ₩1568859.08 · stop ₩1443350.36 · T1 ₩1596566.62 · R/R 0.22  
> ↳ P(T1 av. stop) 39 % _(réel 5 s)_ · EV/risk -0.02 _(réel 5 s)_ (GBM -0.043) · ¼-Kelly 0.067 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -77 % hors [0,100] (R² max 0.97). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 9/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1563718.16–₩1574000.00 (mid ₩1568859.08)
- Spot actuel : ₩1574000.00 (+0.3% au-dessus de la zone — repli à attendre)
- Stop : ₩1443350.36 (stop swing_plan-based (-4.34%))
- Targets : T1 ₩1596566.62 · R/R 0.22 | T2 ₩1624274.16 · R/R 0.44 | T3 ₩1651981.70 · R/R 0.66
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1443350.36


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.49 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (4.34 %)** : le gap seul le franchit 0.247 % des séances (3 fois sur 1217).
   - exécution **0.891 pt plus bas** dans le cas TYPIQUE (médiane), 1.005 au p90, **1.033 au pire**
   - perte réelle **5.219 %** en moyenne _(tirée par la queue)_, jusqu'à **5.373 %** — au lieu des 4.34 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0022 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.249 % | p01 -2.575 % | pire -5.373 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0686** [0.0379 ; 0.1135] _(largeur 7.6 pt, n_eff 173.1)_
   - swing : **0.2969** [0.2506 ; 0.3466] _(largeur 9.6 pt, n_eff 345.6)_
   - deep : **0.4432** [0.3915 ; 0.4959] _(largeur 10.4 pt, n_eff 345.6)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 37.7 observations effectives », dont la borne haute a 95 % vaut environ 7.9 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (30.2 pt), swing (30.7 pt), deep (30.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-3.95 %** | CVaR **-5.65 %** | vol 2.5 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 1.68 % contre 3.04 % aujourd'hui, rapport 0.55)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.65 % vs -6.25 % si l'on extrapolait par √5 _(rapport 0.904 ; < 1 = le √5 surestime)_
- **β de baisse : 0.3223** (β de hausse 0.2167, asymétrie 1.4872) vs KS11 — 553 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : un couple (stop, cible) tient les contraintes : stop 1486785.7143 sur atr_based, cible 11.12 %**
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.35 ATR (stop 2.408 %) — p(stop avant cible) 0.6009 [0.55 ; 0.65], R/R 0.922, perte reelle 3.55 % (gap inclus), EV -0.9965 % — **REFUSE**
      - refuse : p_stop_first 0.601, borne haute 0.651 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.92 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.00 %) : P(cible) 34.8 % x 3.27 % + P(rien) 5.2 % x -0.02 % ne couvrent pas P(stop) 60.1 % x 3.55 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 5.541 %) — p(stop avant cible) 0.3433 [0.29 ; 0.39], R/R 0.591, perte reelle 5.541 % (gap inclus), EV -0.4802 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.48 %) : P(cible) 50.5 % x 3.27 % + P(rien) 15.2 % x -1.52 % ne couvrent pas P(stop) 34.3 % x 5.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 support a 2.89 ATR (stop 11.782 %) — p(stop avant cible) 0.0704 [0.05 ; 0.10], R/R 0.278, perte reelle 11.782 % (gap inclus), EV -0.2892 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.25 ATR du spot, sous le seuil de 1 ATR : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545] sur 940 touches) contre ~35 % au-dela. L'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.29 %) : P(cible) 56.1 % x 3.27 % + P(rien) 36.9 % x -3.51 % ne couvrent pas P(stop) 7.0 % x 11.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 5.95 ATR (stop 23.09 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.142, perte reelle 23.09 % (gap inclus), EV -0.0934 % — **REFUSE**
      - refuse : R/R 0.14 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.09 % > budget 12.0 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.09 %) : P(cible) 56.1 % x 3.27 % + P(rien) 43.9 % x -4.39 % ne couvrent pas P(stop) 0.0 % x 23.09 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : -0.043 | EV/share : ₩-5340.073 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 12 % | T3 6 %
- Kelly (position) : f* 0.268 | ¼-Kelly 0.067 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 71.1 | bear 19.1 | side 9.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.326% → cible +1.766% / stop −8.0%, p_fill 90%, n_eff≈37.7) : P(cible|rempli) **39%** · **EV/risk -0.020** (×p_fill ; si rempli -0.17% du capital)
  - **swing** (entrée dip −0.646% → cible +3.949% / stop −3.718%, p_fill 93%, n_eff≈38.2) : P(cible|rempli) **49%** · **EV/risk +0.034** (×p_fill ; si rempli +0.14% du capital)
  - **deep** (entrée dip −0.949% → cible +5.585% / stop −5.594%, p_fill 89%, n_eff≈37.4) : P(cible|rempli) **57%** · **EV/risk +0.176** (×p_fill ; si rempli +1.10% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→60% · +2.0%→41% · +3.0%→26% · +5.0%→6% · +8.0%→2%
- Range intraday médian 4.08% (p90 6.65%) · excursion haute méd. +1.14% / basse méd. −1.96%
- Profil de vol intra : ouverture 2.61% vs midi 0.763% vs clôture 0.872% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (157 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 11% · trend ↑1%/↓2% ; spike-down 55% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; mean-reverting — autocorr -0.07)_ ; drift intra méd. 0.114% ; recovery-V 42%
- **σ réalisé intraday** 2.855% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 59% / bas 43% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 1534362.5 (VA 1521112.5–1538337.5 ; dernier close 1539000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 42% · rebond 67% · **stop −2.76%** sous le fill (sous le bruit) · cible +1.4% · R/R 0.51 (high win-rate)
- Gaps overnight (n=156) : méd. 0.28% · baisse 34% (gap-down >1% 10% · >2% 3%)
- Excursion ouverture 5min (n=157) : bas méd −0.86% (p90 −2.41%) · haut méd +0.51% · range méd 1.47%
- Excursion ouverture 15min (n=157) : bas méd −1.1% (p90 −2.9%) · haut méd +0.64% · range méd 1.92%
- Excursion ouverture 30min (n=157) : bas méd −1.21% (p90 −3.21%) · haut méd +0.78% · range méd 2.34%
- Excursion ouverture 60min (n=157) : bas méd −1.27% (p90 −3.5%) · haut méd +0.9% · range méd 2.52%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1539000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 77% (108/156) · gap 20% · délai 1.1min · rebond 57% (51/108) (MFE +1.15%)
   - −1.0% : fill 30min 47% · séance 61% (85/156) · gap 10% · délai 2.5min · rebond 57% (39/85) (MFE +1.3%)
   - −1.5% : fill 30min 38% · séance 49% (66/156) · gap 6% · délai 3.2min · rebond 54% (31/66) (MFE +1.42%)
   - −2.0% : fill 30min 29% · séance 42% (57/156) · gap 3% · délai 7.1min · rebond 67% (32/57) (MFE +1.4%)
   - −3.0% : fill 30min 10% · séance 26% (35/156) · gap 1% · délai 87.0min · rebond 57% (19/35) (MFE +1.39%)
   - −4.0% : fill 30min 3% · séance 14% (18/156) · gap 1% · délai 73.5min · rebond 68% (11/18) (MFE +1.74%)
   - −5.0% : fill 30min 1% · séance 7% (10/156) · gap 1% · délai 175.9min · rebond 72% (7/10) (MFE +1.45%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.74% (p90 −2.1%) → stop au-delà de −1.41% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.9% (p90 −2.06%) → stop au-delà de −1.45% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.89% (p90 −2.13%) → stop au-delà de −1.69% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=404 jambes) : jambe baissière méd −1.09% (p90 −2.71%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (37 séances) :
      · −1.0% : fill 99% (36/37) · rebond 66% (19/36)
      · −2.0% : fill 86% (31/37) · rebond 73% (17/31)
      · −3.0% : fill 37% (15/37) · rebond 54% (8/15)
      · −4.0% : fill 26% (9/37) · rebond 76% (5/9)
      · −5.0% : fill 12% (5/37) · rebond 100% (5/5)
   - **flat** (46 séances) :
      · −1.0% : fill 53% (24/46) · rebond 27% (7/24)
      · −2.0% : fill 33% (11/46) · rebond 45% (5/11)
      · −3.0% : fill 27% (8/46) · rebond 73% (6/8)
      · −4.0% : fill 12% (4/46) · rebond 100% (4/4)
      · −5.0% : fill 5% (2/46) · rebond 89% (1/2)
   - **gap-up** (73 séances) :
      · −1.0% : fill 45% (25/73) · rebond 64% (13/25)
      · −2.0% : fill 23% (15/73) · rebond 72% (10/15)
      · −3.0% : fill 19% (12/73) · rebond 49% (5/12)
      · −4.0% : fill 8% (5/73) · rebond 33% (2/5)
      · −5.0% : fill 6% (3/73) · rebond 35% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=157) : 44% en base · 64% si les 15 1res min sont vertes (55 cas) · 32% si rouges (102 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=157) : COUDE à **34min** → P(séance verte=clôture>ouverture) 74% si début vert vs 27% si rouge (base 44% · écart 48 pts) ; prédictivité sature ensuite (plafond brut 225min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=56) : tient le vert **74%** · continue >prix actuel 42% ; creux résiduel méd -1.77% (q20 -2.64%) → **SL/trailing à −2.64%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.36% / q75 +2.27% → **scale +1.36% / runner +2.27%**, sortie à la clôture
  - **si ROUGE au coude** (n=101) : edge inversé — récupère vert seulement **27%** (continue à baisser 49%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.69%** (au-delà de la MAE q10 -3.69%), cible rebond +1.25% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=157) : retour [-3.14% .. +3.26%] · haut q95 +3.64% · bas q05 -3.55%
   - 60min (n=157) : retour [-3.44% .. +2.74%] · haut q95 +3.92% · bas q05 -4.07%
   - 2h (n=157) : retour [-3.9% .. +3.41%] · haut q95 +4.44% · bas q05 -4.67%
   - 4h (n=157) : retour [-4.9% .. +3.56%] · haut q95 +5.03% · bas q05 -5.51%
   - 6h (n=157) : retour [-4.73% .. +3.95%] · haut q95 +5.03% · bas q05 -6.09%
   - session (n=157) : retour [-4.6% .. +3.57%] · haut q95 +5.03% · bas q05 -6.09%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 207940 = **plat / peu volatil** (vol intra méd 2.07%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 55.3  _(momentum haussier)_
- **ADX** : 15.2  _(pas de tendance nette)_
- **MACD** : hist -33.254  _(bearish_recent)_
- **BB** : %B 0.74 · largeur 14.2%
- **ATR** : 58142.86 (62.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.245  _(accumulation)_
- **Vol ratio** : 0.89  _(volume normal)_
- **Choppiness** : 46.4  _(transition)_
- **MA** : MA20 1521500.0 · MA50 1429220.0 · MA200 1599731.04  _(prix > MA20)_
- **Dist MA** : MA20 +3.5% · MA50 +10.1% · MA200 -1.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (588732 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
