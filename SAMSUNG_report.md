# 005930

**Generated** : 2026-08-28T21:51:32.486897+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩256500.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩256500.00 (+6.0% vs entrée) · entrée ₩241887.27 · stop ₩213894.01 · T1 ₩297873.81 · R/R 2.0  
> ↳ P(T1 av. stop) 6 % _(réel 5 s)_ · EV/risk -0.118 _(réel 5 s)_ (GBM 0.202) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩237504.97–₩246269.58 (mid ₩241887.27)
- Spot actuel : ₩256500.00 (+6.0% au-dessus de la zone — repli à attendre)
- Stop : ₩213894.01 (stop swing_plan-based (-16.61%))
- Targets : T1 ₩297873.81 · R/R 2.0 | T2 ₩302648.24 · R/R 2.17 | T3 ₩307422.68 · R/R 2.34
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩213894.01


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.78 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (16.61 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1218).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 16.61 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.389 % | p01 -4.951 % | pire -10.942 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4061** [0.335 ; 0.4803] _(largeur 14.5 pt, n_eff 173.1)_
   - swing : **0.1365** [0.1034 ; 0.1757] _(largeur 7.2 pt, n_eff 345.6)_
   - deep : **0.2087** [0.1684 ; 0.2539] _(largeur 8.5 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (36.5 pt), swing (37.8 pt), deep (38.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.71 %** | CVaR **-9.83 %** | vol 4.7 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 2.60 % contre 5.88 % aujourd'hui, rapport 0.44)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.36 % vs -7.04 % si l'on extrapolait par √5 _(rapport 0.904 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1694** (β de hausse 1.3377, asymétrie 0.8742) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.202 | EV/share : ₩5641.767 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 5 % | T2 3 % | T3 2 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 53.5 | bear 8.3 | side 38.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.592% → cible +5.233% / stop −2.616%, p_fill 57%, n_eff≈26.4) : P(cible|rempli) **3%** · **EV/risk -0.210** (×p_fill ; si rempli -0.96% du capital)
  - **swing** (entrée dip −5.696% → cible +23.146% / stop −11.573%, p_fill 43%, n_eff≈21.9) : P(cible|rempli) **6%** · **EV/risk -0.118** (×p_fill ; si rempli -3.21% du capital)
  - **deep** (entrée dip −8.801% → cible +12.772% / stop −10.558%, p_fill 47%, n_eff≈23.8) : P(cible|rempli) **36%** · **EV/risk -0.051** (×p_fill ; si rempli -1.15% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→70% · +2.0%→48% · +3.0%→39% · +5.0%→25% · +8.0%→5%
- Range intraday médian 6.26% (p90 9.84%) · excursion haute méd. +1.88% / basse méd. −3.08%
- Profil de vol intra : ouverture 3.212% vs midi 1.378% vs clôture 1.574% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 12% · trend ↑0%/↓1% ; spike-down 71% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.14 ; mean-reverting — autocorr -0.087)_ ; drift intra méd. -0.615% ; recovery-V 23%
- **σ réalisé intraday** 4.013% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 68% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 265581.25 (VA 265368.75–268556.25 ; dernier close 265000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 27% · rebond 51% · **stop −6.12%** sous le fill (sous le bruit) · cible +1.06% · R/R 0.17 (high win-rate)
- Gaps overnight (n=159) : méd. 0.95% · baisse 42% (gap-down >1% 33% · >2% 24%)
- Excursion ouverture 5min (n=160) : bas méd −0.74% (p90 −1.66%) · haut méd +0.61% · range méd 1.6%
- Excursion ouverture 15min (n=160) : bas méd −1.03% (p90 −2.42%) · haut méd +1.0% · range méd 2.21%
- Excursion ouverture 30min (n=160) : bas méd −1.24% (p90 −3.36%) · haut méd +1.12% · range méd 2.67%
- Excursion ouverture 60min (n=160) : bas méd −1.75% (p90 −3.61%) · haut méd +1.24% · range méd 3.14%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 266000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 49% · séance 66% (96/159) · gap 35% · délai 0.0min · rebond 48% (49/96) (MFE +0.93%)
   - −1.0% : fill 30min 44% · séance 57% (87/159) · gap 33% · délai 0.0min · rebond 54% (48/87) (MFE +1.18%)
   - −1.5% : fill 30min 40% · séance 50% (74/159) · gap 28% · délai 0.0min · rebond 56% (42/74) (MFE +1.43%)
   - −2.0% : fill 30min 34% · séance 47% (69/159) · gap 24% · délai 0.0min · rebond 58% (42/69) (MFE +1.44%)
   - −3.0% : fill 30min 30% · séance 43% (60/159) · gap 22% · délai 0.0min · rebond 50% (33/60) (MFE +0.98%)
   - −4.0% : fill 30min 22% · séance 34% (45/159) · gap 11% · délai 3.9min · rebond 51% (26/45) (MFE +1.06%)
   - −5.0% : fill 30min 14% · séance 27% (36/159) · gap 10% · délai 18.2min · rebond 51% (23/36) (MFE +1.06%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.48% (p90 −2.03%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.54% (p90 −2.96%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.65% (p90 −2.84%) → stop au-delà de −1.62% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=765 jambes) : jambe baissière méd −1.28% (p90 −3.05%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (60 séances) :
      · −1.0% : fill 96% (57/60) · rebond 44% (28/57)
      · −2.0% : fill 86% (48/60) · rebond 45% (25/48)
      · −3.0% : fill 85% (45/60) · rebond 42% (23/45)
      · −4.0% : fill 74% (36/60) · rebond 45% (20/36)
      · −5.0% : fill 63% (30/60) · rebond 41% (17/30)
   - **flat** (15 séances) :
      · −1.0% : fill 74% (12/15) · rebond 57% (6/12)
      · −2.0% : fill 49% (8/15) · rebond 82% (6/8)
      · −3.0% : fill 34% (6/15) · rebond 35% (3/6)
      · −4.0% : fill 24% (3/15) · rebond 25% (1/3)
      · −5.0% : fill 24% (3/15) · rebond 100% (3/3)
   - **gap-up** (84 séances) :
      · −1.0% : fill 28% (18/84) · rebond 74% (14/18)
      · −2.0% : fill 20% (13/84) · rebond 85% (11/13)
      · −3.0% : fill 16% (9/84) · rebond 82% (7/9)
      · −4.0% : fill 9% (6/84) · rebond 94% (5/6)
      · −5.0% : fill 4% (3/84) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 39% en base · 61% si les 15 1res min sont vertes (80 cas) · 18% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:15** → P(séance verte=clôture>ouverture) 83% si début vert vs 7% si rouge (base 39% · écart 76 pts) ; prédictivité sature ensuite (plafond brut 74min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **83%** · continue >prix actuel 60% ; creux résiduel méd -1.09% (q20 -3.64%) → **SL/trailing à −3.64%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.62% / q75 +3.66% → **scale +2.62% / runner +3.66%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **7%** (continue à baisser 60%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.92%** (au-delà de la MAE q10 -6.92%), cible rebond +1.3% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.83% .. +2.73%] · haut q95 +3.64% · bas q05 -3.73%
   - 60min (n=160) : retour [-3.13% .. +4.27%] · haut q95 +5.0% · bas q05 -5.13%
   - 2h (n=160) : retour [-4.56% .. +4.72%] · haut q95 +5.9% · bas q05 -5.75%
   - 4h (n=160) : retour [-6.05% .. +5.44%] · haut q95 +6.84% · bas q05 -7.61%
   - 6h (n=160) : retour [-7.07% .. +5.32%] · haut q95 +6.97% · bas q05 -7.85%
   - session (n=160) : retour [-6.68% .. +5.42%] · haut q95 +6.97% · bas q05 -8.5%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.97%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 58.5  _(momentum haussier)_
- **ADX** : 14.1  _(pas de tendance nette)_
- **MACD** : hist 2282.711  _(pas de croisement recent)_
- **BB** : %B 0.54 · largeur 24.4%
- **ATR** : 16464.29 (69.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.02  _(neutre)_
- **Vol ratio** : 0.49  _(volume atone)_
- **Choppiness** : 50.7  _(transition)_
- **MA** : MA20 254175.0 · MA50 274906.72 · MA200 207472.45  _(prix > MA20)_
- **Dist MA** : MA20 +0.9% · MA50 -6.7% · MA200 +23.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (618022 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
