# 267260

**Generated** : 2026-08-20T21:52:33.868372+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩746000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩746000.00 (+1.2% vs entrée) · entrée ₩737401.49 · stop ₩687185.82 · T1 ₩804563.85 · R/R 1.34  
> ↳ P(T1 av. stop) 28 % _(réel 5 s)_ · EV/risk -0.152 _(réel 5 s)_ (GBM 0.082) · ¼-Kelly 0.003 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

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

Plan privilegie B (swing), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩728802.98–₩746000.00 (mid ₩737401.49)
- Spot actuel : ₩746000.00 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : ₩687185.82 (stop swing_plan-based (-7.88%))
- Targets : T1 ₩804563.85 · R/R 1.34 | T2 ₩871726.22 · R/R 2.67 | T3 ₩938888.58 · R/R 4.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩687185.82


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.94 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.88 %)** : le gap seul le franchit 0.082 % des séances (1 fois sur 1218).
   - exécution **3.835 pt plus bas** dans le cas TYPIQUE (médiane), 3.835 au p90, **3.835 au pire**
   - perte réelle **11.715 %** en moyenne _(tirée par la queue)_, jusqu'à **11.715 %** — au lieu des 7.88 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0031 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.638 % | p01 -4.805 % | pire -11.715 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2376** [0.1789 ; 0.305] _(largeur 12.6 pt, n_eff 173.1)_
   - swing : **0.4549** [0.403 ; 0.5076] _(largeur 10.5 pt, n_eff 345.6)_
   - deep : **0.4988** [0.4463 ; 0.5513] _(largeur 10.5 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (29.6 pt), swing (30.6 pt), deep (29.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.59 %** | CVaR **-8.78 %** | vol 4.38 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 3.03 % contre 5.19 % aujourd'hui, rapport 0.58)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.73 % vs -11.89 % si l'on extrapolait par √5 _(rapport 0.902 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0429** (β de hausse 0.8457, asymétrie 1.2332) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.082 | EV/share : ₩4134.391 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 9 % | T3 3 %
- Kelly (position) : f* 0.013 | ¼-Kelly 0.003 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 36.6 | bear 10.8 | side 52.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.554% → cible +4.073% / stop −8.0%, p_fill 99%, n_eff≈40.1) : P(cible|rempli) **32%** · **EV/risk -0.071** (×p_fill ; si rempli -0.58% du capital)
  - **swing** (entrée dip −1.148% → cible +9.108% / stop −6.81%, p_fill 96%, n_eff≈38.4) : P(cible|rempli) **28%** · **EV/risk -0.152** (×p_fill ; si rempli -1.08% du capital)
  - **deep** (entrée dip −1.664% → cible +12.881% / stop −10.267%, p_fill 98%, n_eff≈38.4) : P(cible|rempli) **32%** · **EV/risk -0.310** (×p_fill ; si rempli -3.26% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→68% · +2.0%→46% · +3.0%→36% · +5.0%→11% · +8.0%→4%
- Range intraday médian 6.79% (p90 10.49%) · excursion haute méd. +1.66% / basse méd. −3.96%
- Profil de vol intra : ouverture 4.361% vs midi 1.216% vs clôture 1.256% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (157 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 83% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; mean-reverting — autocorr -0.072)_ ; drift intra méd. -1.415% ; recovery-V 30%
- **σ réalisé intraday** 4.477% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 44% / bas 67% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 753525.0 (VA 745425.0–756225.0 ; dernier close 752000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 32% · rebond 83% · **stop −5.04%** sous le fill (sous le bruit) · cible +2.79% · R/R 0.55 (high win-rate)
- Gaps overnight (n=156) : méd. 1.26% · baisse 38% (gap-down >1% 21% · >2% 12%)
- Excursion ouverture 5min (n=157) : bas méd −1.71% (p90 −3.92%) · haut méd +0.95% · range méd 2.87%
- Excursion ouverture 15min (n=157) : bas méd −2.06% (p90 −4.66%) · haut méd +1.04% · range méd 3.39%
- Excursion ouverture 30min (n=157) : bas méd −2.26% (p90 −5.01%) · haut méd +1.06% · range méd 3.78%
- Excursion ouverture 60min (n=157) : bas méd −2.58% (p90 −5.61%) · haut méd +1.12% · range méd 4.12%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 752000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 72% (111/156) · gap 31% · délai 0.0min · rebond 54% (62/111) (MFE +1.17%)
   - −1.0% : fill 30min 52% · séance 69% (103/156) · gap 21% · délai 0.2min · rebond 57% (61/103) (MFE +1.24%)
   - −1.5% : fill 30min 45% · séance 62% (89/156) · gap 16% · délai 0.4min · rebond 63% (57/89) (MFE +1.27%)
   - −2.0% : fill 30min 41% · séance 58% (81/156) · gap 12% · délai 0.7min · rebond 71% (56/81) (MFE +1.61%)
   - −3.0% : fill 30min 32% · séance 48% (64/156) · gap 8% · délai 1.8min · rebond 77% (45/64) (MFE +1.85%)
   - −4.0% : fill 30min 23% · séance 39% (52/156) · gap 5% · délai 14.8min · rebond 78% (41/52) (MFE +2.2%)
   - −5.0% : fill 30min 15% · séance 32% (41/156) · gap 3% · délai 37.5min · rebond 83% (32/41) (MFE +2.79%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.76% (p90 −3.37%) → stop au-delà de −2.61% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.97% (p90 −3.32%) → stop au-delà de −2.89% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.63% (p90 −4.83%) → stop au-delà de −3.36% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=807 jambes) : jambe baissière méd −1.24% (p90 −3.33%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 99% (53/54) · rebond 49% (28/53)
      · −2.0% : fill 94% (46/54) · rebond 64% (28/46)
      · −3.0% : fill 87% (40/54) · rebond 74% (27/40)
      · −4.0% : fill 76% (35/54) · rebond 78% (28/35)
      · −5.0% : fill 63% (27/54) · rebond 84% (21/27)
   - **flat** (17 séances) :
      · −1.0% : fill 88% (14/17) · rebond 47% (7/14)
      · −2.0% : fill 79% (12/17) · rebond 78% (9/12)
      · −3.0% : fill 78% (11/17) · rebond 83% (8/11)
      · −4.0% : fill 57% (7/17) · rebond 68% (5/7)
      · −5.0% : fill 57% (7/17) · rebond 89% (6/7)
   - **gap-up** (85 séances) :
      · −1.0% : fill 48% (36/85) · rebond 70% (26/36)
      · −2.0% : fill 34% (23/85) · rebond 81% (19/23)
      · −3.0% : fill 22% (13/85) · rebond 80% (10/13)
      · −4.0% : fill 15% (10/85) · rebond 82% (8/10)
      · −5.0% : fill 10% (7/85) · rebond 78% (5/7)
- **P(clôture VERTE) selon le drive 15min** (n=157) : 35% en base · 48% si les 15 1res min sont vertes (69 cas) · 28% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=157) : COUDE à **1:18** → P(séance verte=clôture>ouverture) 69% si début vert vs 13% si rouge (base 35% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=68) : tient le vert **69%** · continue >prix actuel 42% ; creux résiduel méd -1.83% (q20 -3.73%) → **SL/trailing à −3.73%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.57% / q75 +2.45% → **scale +1.57% / runner +2.45%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **13%** (continue à baisser 47%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.38%** (au-delà de la MAE q10 -5.38%), cible rebond +1.43% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=157) : retour [-5.13% .. +2.68%] · haut q95 +3.96% · bas q05 -5.63%
   - 60min (n=157) : retour [-5.65% .. +2.7%] · haut q95 +4.37% · bas q05 -6.02%
   - 2h (n=157) : retour [-6.89% .. +3.67%] · haut q95 +4.97% · bas q05 -7.39%
   - 4h (n=157) : retour [-6.94% .. +3.81%] · haut q95 +5.28% · bas q05 -8.47%
   - 6h (n=157) : retour [-7.83% .. +3.72%] · haut q95 +6.25% · bas q05 -9.29%
   - session (n=157) : retour [-7.51% .. +3.91%] · haut q95 +6.32% · bas q05 -9.67%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.51%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 72.2  _(surachat)_
- **ADX** : 18.3  _(pas de tendance nette)_
- **MACD** : hist 12324.511  _(pas de croisement recent)_
- **BB** : %B 0.51 · largeur 38.1%
- **ATR** : 50215.67 (43.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.007  _(neutre)_
- **Vol ratio** : 0.62  _(volume normal)_
- **Choppiness** : 50.0  _(transition)_
- **MA** : MA20 742893.28 · MA50 859538.73 · MA200 924924.11  _(prix > MA20)_
- **Dist MA** : MA20 +0.4% · MA50 -13.2% · MA200 -19.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (570465 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
