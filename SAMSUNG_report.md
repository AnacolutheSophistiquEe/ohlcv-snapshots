# 005930

**Generated** : 2026-09-01T00:15:55.398822+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩256250.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩256250.00 (+6.0% vs entrée) · entrée ₩241774.78 · stop ₩225060.49 · T1 ₩256798.28 · R/R 0.9  
> ↳ P(T1 av. stop) 25 % _(réel 5 s)_ · EV/risk -0.167 _(réel 5 s)_ (GBM 0.275) · ¼-Kelly 0.033 · _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.050 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩238770.08–₩244779.48 (mid ₩241774.78)
- Spot actuel : ₩256250.00 (+6.0% au-dessus de la zone — repli à attendre)
- Stop : ₩225060.49 (stop swing_plan-based (-12.17%))
- Targets : T1 ₩256798.28 · R/R 0.9 | T2 ₩271821.79 · R/R 1.8 | T3 ₩286845.29 · R/R 2.7
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩225060.49


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.86 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.17 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1217).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 12.17 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.403 % | p01 -4.952 % | pire -10.942 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4009** [0.33 ; 0.4751] _(largeur 14.5 pt, n_eff 173.1)_
   - swing : **0.2501** [0.2067 ; 0.2977] _(largeur 9.1 pt, n_eff 345.6)_
   - deep : **0.1853** [0.1471 ; 0.2288] _(largeur 8.2 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (36.5 pt), swing (40.1 pt), deep (38.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.71 %** | CVaR **-9.83 %** | vol 4.7 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 2.60 % contre 5.88 % aujourd'hui, rapport 0.44)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.36 % vs -7.05 % si l'on extrapolait par √5 _(rapport 0.903 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1701** (β de hausse 1.3374, asymétrie 0.8749) vs KS11 — 554 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.275 | EV/share : ₩4598.296 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 25 % | T3 11 %
- Kelly (position) : f* 0.132 | ¼-Kelly 0.033 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 50.0 | bear 7.9 | side 42.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.573% → cible +5.312% / stop −2.656%, p_fill 54%, n_eff≈26.3) : P(cible|rempli) **3%** · **EV/risk -0.204** (×p_fill ; si rempli -1.00% du capital)
  - **swing** (entrée dip −5.647% → cible +6.214% / stop −6.913%, p_fill 46%, n_eff≈21.3) : P(cible|rempli) **25%** · **EV/risk -0.167** (×p_fill ; si rempli -2.52% du capital)
  - **deep** (entrée dip −8.726% → cible +8.788% / stop −10.72%, p_fill 50%, n_eff≈23.1) : P(cible|rempli) **51%** · **EV/risk -0.021** (×p_fill ; si rempli -0.45% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→70% · +2.0%→48% · +3.0%→39% · +5.0%→25% · +8.0%→5%
- Range intraday médian 6.25% (p90 9.84%) · excursion haute méd. +1.88% / basse méd. −3.0%
- Profil de vol intra : ouverture 3.165% vs midi 1.367% vs clôture 1.57% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑0%/↓1% ; spike-down 72% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.139 ; mean-reverting — autocorr -0.089)_ ; drift intra méd. -0.657% ; recovery-V 21%
- **σ réalisé intraday** 3.942% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 69% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 260125.0 (VA 258125.0–262125.0 ; dernier close 258500.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 27% · rebond 51% · **stop −6.12%** sous le fill (sous le bruit) · cible +1.06% · R/R 0.17 (high win-rate)
- Gaps overnight (n=159) : méd. 0.89% · baisse 43% (gap-down >1% 34% · >2% 24%)
- Excursion ouverture 5min (n=160) : bas méd −0.73% (p90 −1.66%) · haut méd +0.6% · range méd 1.58%
- Excursion ouverture 15min (n=160) : bas méd −0.99% (p90 −2.38%) · haut méd +0.97% · range méd 2.17%
- Excursion ouverture 30min (n=160) : bas méd −1.27% (p90 −3.31%) · haut méd +1.09% · range méd 2.63%
- Excursion ouverture 60min (n=160) : bas méd −1.74% (p90 −3.6%) · haut méd +1.31% · range méd 3.13%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 257000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 50% · séance 67% (97/159) · gap 36% · délai 0.0min · rebond 46% (49/97) (MFE +0.91%)
   - −1.0% : fill 30min 45% · séance 58% (88/159) · gap 34% · délai 0.0min · rebond 55% (49/88) (MFE +1.02%)
   - −1.5% : fill 30min 41% · séance 51% (75/159) · gap 28% · délai 0.0min · rebond 57% (43/75) (MFE +1.49%)
   - −2.0% : fill 30min 35% · séance 48% (70/159) · gap 24% · délai 0.0min · rebond 60% (43/70) (MFE +1.62%)
   - −3.0% : fill 30min 29% · séance 44% (61/159) · gap 22% · délai 0.7min · rebond 52% (34/61) (MFE +1.06%)
   - −4.0% : fill 30min 21% · séance 33% (45/159) · gap 11% · délai 3.9min · rebond 51% (26/45) (MFE +1.06%)
   - −5.0% : fill 30min 14% · séance 27% (36/159) · gap 10% · délai 18.2min · rebond 51% (23/36) (MFE +1.06%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.52% (p90 −2.0%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.55% (p90 −2.96%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.65% (p90 −2.84%) → stop au-delà de −1.62% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=770 jambes) : jambe baissière méd −1.26% (p90 −3.03%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (61 séances) :
      · −1.0% : fill 96% (58/61) · rebond 47% (29/58)
      · −2.0% : fill 87% (49/61) · rebond 48% (26/49)
      · −3.0% : fill 86% (46/61) · rebond 45% (24/46)
      · −4.0% : fill 70% (36/61) · rebond 45% (20/36)
      · −5.0% : fill 60% (30/61) · rebond 41% (17/30)
   - **flat** (15 séances) :
      · −1.0% : fill 74% (12/15) · rebond 57% (6/12)
      · −2.0% : fill 49% (8/15) · rebond 82% (6/8)
      · −3.0% : fill 34% (6/15) · rebond 35% (3/6)
      · −4.0% : fill 24% (3/15) · rebond 25% (1/3)
      · −5.0% : fill 24% (3/15) · rebond 100% (3/3)
   - **gap-up** (83 séances) :
      · −1.0% : fill 28% (18/83) · rebond 74% (14/18)
      · −2.0% : fill 20% (13/83) · rebond 85% (11/13)
      · −3.0% : fill 16% (9/83) · rebond 82% (7/9)
      · −4.0% : fill 9% (6/83) · rebond 94% (5/6)
      · −5.0% : fill 4% (3/83) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 39% en base · 60% si les 15 1res min sont vertes (79 cas) · 17% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:15** → P(séance verte=clôture>ouverture) 83% si début vert vs 7% si rouge (base 39% · écart 76 pts) ; prédictivité sature ensuite (plafond brut 74min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **83%** · continue >prix actuel 60% ; creux résiduel méd -1.1% (q20 -3.64%) → **SL/trailing à −3.64%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.63% / q75 +3.67% → **scale +2.63% / runner +3.67%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **7%** (continue à baisser 61%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.77%** (au-delà de la MAE q10 -6.77%), cible rebond +1.3% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.83% .. +2.72%] · haut q95 +3.63% · bas q05 -3.72%
   - 60min (n=160) : retour [-3.13% .. +4.25%] · haut q95 +4.99% · bas q05 -5.01%
   - 2h (n=160) : retour [-4.55% .. +4.72%] · haut q95 +5.88% · bas q05 -5.68%
   - 4h (n=160) : retour [-6.01% .. +5.41%] · haut q95 +6.84% · bas q05 -7.57%
   - 6h (n=160) : retour [-7.0% .. +5.31%] · haut q95 +6.96% · bas q05 -7.8%
   - session (n=160) : retour [-6.59% .. +5.42%] · haut q95 +6.96% · bas q05 -8.48%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.97%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 58.8  _(momentum haussier)_
- **ADX** : 13.4  _(pas de tendance nette)_
- **MACD** : hist 1642.785  _(pas de croisement recent)_
- **BB** : %B 0.54 · largeur 24.2%
- **ATR** : 16714.29 (69.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.045  _(neutre)_
- **Vol ratio** : 0.37  _(volume atone)_
- **Choppiness** : 51.3  _(transition)_
- **MA** : MA20 253887.5 · MA50 272799.7 · MA200 208257.22  _(prix > MA20)_
- **Dist MA** : MA20 +0.9% · MA50 -6.1% · MA200 +23.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (507004 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
