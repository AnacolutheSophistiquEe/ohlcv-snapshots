# 005930

**Generated** : 2026-08-27T21:51:29.509818+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩266000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩266000.00 (+0.6% vs entrée) · entrée ₩264536.78 · stop ₩259245.13 · T1 ₩275120.09 · R/R 2.0  
> ↳ P(T1 av. stop) 21 % _(réel 5 s)_ · EV/risk -0.249 _(réel 5 s)_ (GBM -0.037) · ¼-Kelly 0.011 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.010 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩263073.57–₩266000.00 (mid ₩264536.78)
- Spot actuel : ₩266000.00 (+0.6% au-dessus de la zone — repli à attendre)
- Stop : ₩259245.13 (stop swing_plan-based (-7.43%))
- Targets : T1 ₩275120.09 · R/R 2.0 | T2 ₩285703.41 · R/R 4.0 | T3 ₩296286.72 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩259245.13


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.78 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.43 %)** : le gap seul le franchit 0.246 % des séances (3 fois sur 1218).
   - exécution **0.381 pt plus bas** dans le cas TYPIQUE (médiane), 2.886 au p90, **3.512 au pire**
   - perte réelle **8.848 %** en moyenne _(tirée par la queue)_, jusqu'à **10.942 %** — au lieu des 7.43 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0035 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.389 % | p01 -4.951 % | pire -10.942 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4676** [0.3943 ; 0.542] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.2811** [0.2357 ; 0.3302] _(largeur 9.4 pt, n_eff 345.6)_
   - deep : **0.243** [0.2001 ; 0.2902] _(largeur 9.0 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (29.8 pt), swing (31.0 pt), deep (31.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.71 %** | CVaR **-9.83 %** | vol 4.7 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 2.64 % contre 5.95 % aujourd'hui, rapport 0.44)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.32 % vs -6.93 % si l'on extrapolait par √5 _(rapport 0.912 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1694** (β de hausse 1.3377, asymétrie 0.8742) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.037 | EV/share : ₩-197.115 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 26 % | T2 22 % | T3 22 %
- Kelly (position) : f* 0.045 | ¼-Kelly 0.011 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 67.3 | bear 6.6 | side 26.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.551% → cible +4.001% / stop −2.0%, p_fill 90%, n_eff≈37.1) : P(cible|rempli) **21%** · **EV/risk -0.249** (×p_fill ; si rempli -0.56% du capital)
  - **swing** (entrée dip −1.214% → cible +8.946% / stop −6.292%, p_fill 85%, n_eff≈35.5) : P(cible|rempli) **34%** · **EV/risk -0.177** (×p_fill ; si rempli -1.30% du capital)
  - **deep** (entrée dip −1.745% → cible +12.651% / stop −9.49%, p_fill 90%, n_eff≈35.0) : P(cible|rempli) **39%** · **EV/risk -0.123** (×p_fill ; si rempli -1.29% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→71% · +2.0%→46% · +3.0%→38% · +5.0%→26% · +8.0%→5%
- Range intraday médian 6.4% (p90 9.84%) · excursion haute méd. +1.9% / basse méd. −3.08%
- Profil de vol intra : ouverture 3.184% vs midi 1.381% vs clôture 1.582% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (159 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑0%/↓1% ; spike-down 71% · recovery-V 21%)_
- **Régime intraday** : **chop** _(efficiency 0.133 ; mean-reverting — autocorr -0.087)_ ; drift intra méd. -0.674% ; recovery-V 21%
- **σ réalisé intraday** 4.246% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 71% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 279537.5 (VA 277162.5–283812.5 ; dernier close 281300.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 28% · rebond 55% · **stop −6.26%** sous le fill (sous le bruit) · cible +1.25% · R/R 0.2 (high win-rate)
- Gaps overnight (n=158) : méd. 1.25% · baisse 39% (gap-down >1% 32% · >2% 22%)
- Excursion ouverture 5min (n=159) : bas méd −0.74% (p90 −1.64%) · haut méd +0.61% · range méd 1.56%
- Excursion ouverture 15min (n=159) : bas méd −1.03% (p90 −2.57%) · haut méd +1.04% · range méd 2.24%
- Excursion ouverture 30min (n=159) : bas méd −1.24% (p90 −3.11%) · haut méd +1.17% · range méd 2.66%
- Excursion ouverture 60min (n=159) : bas méd −1.75% (p90 −3.58%) · haut méd +1.33% · range méd 3.14%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 281500.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 47% · séance 66% (95/158) · gap 34% · délai 0.0min · rebond 49% (49/95) (MFE +0.94%)
   - −1.0% : fill 30min 43% · séance 58% (87/158) · gap 32% · délai 0.0min · rebond 54% (49/87) (MFE +1.18%)
   - −1.5% : fill 30min 39% · séance 50% (72/158) · gap 26% · délai 0.0min · rebond 56% (41/72) (MFE +1.42%)
   - −2.0% : fill 30min 32% · séance 47% (67/158) · gap 22% · délai 0.0min · rebond 59% (41/67) (MFE +1.43%)
   - −3.0% : fill 30min 28% · séance 42% (58/158) · gap 20% · délai 4.6min · rebond 50% (32/58) (MFE +0.98%)
   - −4.0% : fill 30min 19% · séance 32% (43/158) · gap 12% · délai 7.6min · rebond 51% (25/43) (MFE +1.06%)
   - −5.0% : fill 30min 14% · séance 28% (35/158) · gap 10% · délai 39.6min · rebond 55% (23/35) (MFE +1.25%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.48% (p90 −2.08%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.53% (p90 −3.03%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.65% (p90 −3.1%) → stop au-delà de −1.7% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=752 jambes) : jambe baissière méd −1.27% (p90 −3.07%) · ~12.4 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (59 séances) :
      · −1.0% : fill 96% (56/59) · rebond 44% (28/56)
      · −2.0% : fill 84% (46/59) · rebond 44% (24/46)
      · −3.0% : fill 83% (43/59) · rebond 41% (22/43)
      · −4.0% : fill 70% (34/59) · rebond 44% (19/34)
      · −5.0% : fill 64% (29/59) · rebond 45% (17/29)
   - **flat** (15 séances) :
      · −1.0% : fill 87% (12/15) · rebond 57% (6/12)
      · −2.0% : fill 58% (8/15) · rebond 82% (6/8)
      · −3.0% : fill 40% (6/15) · rebond 35% (3/6)
      · −4.0% : fill 29% (3/15) · rebond 25% (1/3)
      · −5.0% : fill 29% (3/15) · rebond 100% (3/3)
   - **gap-up** (84 séances) :
      · −1.0% : fill 29% (19/84) · rebond 75% (15/19)
      · −2.0% : fill 21% (13/84) · rebond 85% (11/13)
      · −3.0% : fill 17% (9/84) · rebond 82% (7/9)
      · −4.0% : fill 9% (6/84) · rebond 94% (5/6)
      · −5.0% : fill 4% (3/84) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=159) : 38% en base · 59% si les 15 1res min sont vertes (80 cas) · 16% si rouges (79 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=159) : COUDE à **1:15** → P(séance verte=clôture>ouverture) 82% si début vert vs 5% si rouge (base 38% · écart 77 pts) ; prédictivité sature ensuite (plafond brut 75min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=83) : tient le vert **82%** · continue >prix actuel 58% ; creux résiduel méd -1.14% (q20 -3.72%) → **SL/trailing à −3.72%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.14% / q75 +3.77% → **scale +2.14% / runner +3.77%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **5%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.96%** (au-delà de la MAE q10 -6.96%), cible rebond +1.3% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=159) : retour [-2.82% .. +2.79%] · haut q95 +3.67% · bas q05 -3.72%
   - 60min (n=159) : retour [-3.14% .. +4.34%] · haut q95 +5.25% · bas q05 -5.13%
   - 2h (n=159) : retour [-4.6% .. +4.75%] · haut q95 +6.04% · bas q05 -6.0%
   - 4h (n=159) : retour [-6.2% .. +5.55%] · haut q95 +6.86% · bas q05 -7.75%
   - 6h (n=159) : retour [-7.2% .. +5.36%] · haut q95 +7.0% · bas q05 -8.03%
   - session (n=159) : retour [-7.24% .. +5.44%] · haut q95 +7.0% · bas q05 -8.58%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.8% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.96%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 62.6  _(momentum haussier)_
- **ADX** : 15.0  _(pas de tendance nette)_
- **MACD** : hist 3151.792  _(pas de croisement recent)_
- **BB** : %B 0.69 · largeur 29.7%
- **ATR** : 16535.71 (70.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.008  _(neutre)_
- **Vol ratio** : 0.62  _(volume normal)_
- **Choppiness** : 50.8  _(transition)_
- **MA** : MA20 251700.0 · MA50 276699.08 · MA200 206710.26  _(prix > MA20)_
- **Dist MA** : MA20 +5.7% · MA50 -3.9% · MA200 +28.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (566574 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
