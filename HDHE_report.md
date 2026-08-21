# 267260

**Generated** : 2026-08-21T21:52:31.911530+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩718000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩718000.00 (+8.2% vs entrée) · entrée ₩663717.73 · stop ₩584071.60 · T1 ₩836988.64 · R/R 2.18  
> ↳ P(T1 av. stop) 0 % _(réel 5 s)_ · EV/risk -0.122 _(réel 5 s)_ (GBM 0.041) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.070 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩652065.91–₩675369.55 (mid ₩663717.73)
- Spot actuel : ₩718000.00 (+8.2% au-dessus de la zone — repli à attendre)
- Stop : ₩584071.60 (stop swing_plan-based (-18.65%))
- Targets : T1 ₩836988.64 · R/R 2.18 | T2 ₩837477.03 · R/R 2.18 | T3 ₩837965.43 · R/R 2.19
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩584071.60


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.94 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (18.65 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1218).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 18.65 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.638 % | p01 -4.805 % | pire -11.715 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2349** [0.1765 ; 0.3021] _(largeur 12.6 pt, n_eff 173.1)_
   - swing : **0.4581** [0.4061 ; 0.5108] _(largeur 10.5 pt, n_eff 345.6)_
   - deep : **0.4959** [0.4434 ; 0.5485] _(largeur 10.5 pt, n_eff 345.6)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_target_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 19.9 observations effectives », dont la borne haute a 95 % vaut environ 15.0 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (28.9 pt), swing (41.4 pt), deep (39.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.59 %** | CVaR **-8.78 %** | vol 4.39 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 2.99 % contre 5.20 % aujourd'hui, rapport 0.58)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.73 % vs -11.89 % si l'on extrapolait par √5 _(rapport 0.902 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0429** (β de hausse 0.822, asymétrie 1.2687) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.041 | EV/share : ₩3248.993 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 3 % | T2 3 % | T3 3 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 58.8 | bear 9.4 | side 31.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.435% → cible +6.645% / stop −8.0%, p_fill 54%, n_eff≈26.7) : P(cible|rempli) **13%** · **EV/risk +0.017** (×p_fill ; si rempli +0.25% du capital)
  - **swing** (entrée dip −7.557% → cible +26.106% / stop −12.0%, p_fill 32%, n_eff≈19.9) : P(cible|rempli) **0%** · **EV/risk -0.122** (×p_fill ; si rempli -4.51% du capital)
  - **deep** (entrée dip −11.686% → cible +12.376% / stop −10.581%, p_fill 35%, n_eff≈16.9) : P(cible|rempli) **16%** · **EV/risk -0.202** (×p_fill ; si rempli -6.07% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→68% · +2.0%→45% · +3.0%→36% · +5.0%→11% · +8.0%→4%
- Range intraday médian 6.79% (p90 10.49%) · excursion haute méd. +1.61% / basse méd. −3.96%
- Profil de vol intra : ouverture 4.388% vs midi 1.215% vs clôture 1.26% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (158 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 83% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; mean-reverting — autocorr -0.059)_ ; drift intra méd. -1.401% ; recovery-V 29%
- **σ réalisé intraday** 4.452% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 42% / bas 64% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 744237.5 (VA 742062.5–747862.5 ; dernier close 745000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 32% · rebond 83% · **stop −5.04%** sous le fill (sous le bruit) · cible +2.79% · R/R 0.55 (high win-rate)
- Gaps overnight (n=157) : méd. 1.21% · baisse 37% (gap-down >1% 21% · >2% 12%)
- Excursion ouverture 5min (n=158) : bas méd −1.77% (p90 −3.89%) · haut méd +0.97% · range méd 2.89%
- Excursion ouverture 15min (n=158) : bas méd −2.08% (p90 −4.64%) · haut méd +1.05% · range méd 3.42%
- Excursion ouverture 30min (n=158) : bas méd −2.27% (p90 −4.99%) · haut méd +1.06% · range méd 3.8%
- Excursion ouverture 60min (n=158) : bas méd −2.63% (p90 −5.59%) · haut méd +1.19% · range méd 4.12%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 745000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 73% (112/157) · gap 30% · délai 0.1min · rebond 55% (63/112) (MFE +1.17%)
   - −1.0% : fill 30min 53% · séance 69% (104/157) · gap 21% · délai 0.3min · rebond 58% (62/104) (MFE +1.3%)
   - −1.5% : fill 30min 46% · séance 63% (90/157) · gap 15% · délai 0.4min · rebond 64% (58/90) (MFE +1.28%)
   - −2.0% : fill 30min 42% · séance 59% (82/157) · gap 12% · délai 0.7min · rebond 72% (57/82) (MFE +1.71%)
   - −3.0% : fill 30min 31% · séance 48% (64/157) · gap 8% · délai 1.8min · rebond 77% (45/64) (MFE +1.85%)
   - −4.0% : fill 30min 23% · séance 38% (52/157) · gap 5% · délai 14.8min · rebond 78% (41/52) (MFE +2.2%)
   - −5.0% : fill 30min 15% · séance 32% (41/157) · gap 3% · délai 37.5min · rebond 83% (32/41) (MFE +2.79%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.74% (p90 −3.32%) → stop au-delà de −2.41% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.97% (p90 −3.32%) → stop au-delà de −2.89% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.63% (p90 −4.83%) → stop au-delà de −3.36% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=812 jambes) : jambe baissière méd −1.22% (p90 −3.35%) · ~11.9 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 99% (53/54) · rebond 49% (28/53)
      · −2.0% : fill 94% (46/54) · rebond 64% (28/46)
      · −3.0% : fill 87% (40/54) · rebond 74% (27/40)
      · −4.0% : fill 76% (35/54) · rebond 78% (28/35)
      · −5.0% : fill 63% (27/54) · rebond 84% (21/27)
   - **flat** (18 séances) :
      · −1.0% : fill 90% (15/18) · rebond 56% (8/15)
      · −2.0% : fill 82% (13/18) · rebond 83% (10/13)
      · −3.0% : fill 65% (11/18) · rebond 83% (8/11)
      · −4.0% : fill 48% (7/18) · rebond 68% (5/7)
      · −5.0% : fill 48% (7/18) · rebond 89% (6/7)
   - **gap-up** (85 séances) :
      · −1.0% : fill 48% (36/85) · rebond 70% (26/36)
      · −2.0% : fill 34% (23/85) · rebond 81% (19/23)
      · −3.0% : fill 22% (13/85) · rebond 80% (10/13)
      · −4.0% : fill 15% (10/85) · rebond 82% (8/10)
      · −5.0% : fill 10% (7/85) · rebond 78% (5/7)
- **P(clôture VERTE) selon le drive 15min** (n=158) : 34% en base · 48% si les 15 1res min sont vertes (69 cas) · 27% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=158) : COUDE à **1:19** → P(séance verte=clôture>ouverture) 69% si début vert vs 12% si rouge (base 34% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=69) : tient le vert **69%** · continue >prix actuel 41% ; creux résiduel méd -1.87% (q20 -3.48%) → **SL/trailing à −3.48%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.46% / q75 +2.35% → **scale +1.46% / runner +2.35%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **12%** (continue à baisser 49%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.3%** (au-delà de la MAE q10 -5.3%), cible rebond +1.22% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=158) : retour [-5.08% .. +2.68%] · haut q95 +3.92% · bas q05 -5.6%
   - 60min (n=158) : retour [-5.64% .. +2.65%] · haut q95 +4.37% · bas q05 -6.01%
   - 2h (n=158) : retour [-6.83% .. +3.66%] · haut q95 +4.95% · bas q05 -7.37%
   - 4h (n=158) : retour [-6.94% .. +3.79%] · haut q95 +5.26% · bas q05 -8.44%
   - 6h (n=158) : retour [-7.72% .. +3.72%] · haut q95 +6.22% · bas q05 -9.27%
   - session (n=158) : retour [-7.49% .. +3.9%] · haut q95 +6.29% · bas q05 -9.67%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.51%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 55.9  _(momentum haussier)_
- **ADX** : 18.2  _(pas de tendance nette)_
- **MACD** : hist 8356.815  _(pas de croisement recent)_
- **BB** : %B 0.43 · largeur 35.1%
- **ATR** : 44729.64 (36.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.066  _(distribution)_
- **Vol ratio** : 0.84  _(volume normal)_
- **Choppiness** : 50.5  _(transition)_
- **MA** : MA20 735417.21 · MA50 854212.29 · MA200 924350.67  _(prix < MA20)_
- **Dist MA** : MA20 -2.4% · MA50 -15.9% · MA200 -22.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (606851 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
