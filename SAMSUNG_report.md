# 005930

**Generated** : 2026-08-25T00:15:23.286143+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 8.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩257000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩257000.00 (+6.1% vs entrée) · entrée ₩242112.27 · stop ₩213058.80 · T1 ₩302166.77 · R/R 2.07  
> ↳ P(T1 av. stop) 6 % _(réel 5 s)_ · EV/risk -0.115 _(réel 5 s)_ (GBM 0.194) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.100 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩237237.25–₩246987.30 (mid ₩242112.27)
- Spot actuel : ₩257000.00 (+6.1% au-dessus de la zone — repli à attendre)
- Stop : ₩213058.80 (stop swing_plan-based (-17.1%))
- Targets : T1 ₩302166.77 · R/R 2.07 | T2 ₩308591.39 · R/R 2.29 | T3 ₩315016.02 · R/R 2.51
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩213058.80


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.70 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (17.1 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1217).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 17.1 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.357 % | p01 -4.952 % | pire -10.942 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2008** [0.1464 ; 0.2651] _(largeur 11.9 pt, n_eff 173.1)_
   - swing : **0.3094** [0.2624 ; 0.3596] _(largeur 9.7 pt, n_eff 345.6)_
   - deep : **0.3594** [0.3102 ; 0.411] _(largeur 10.1 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (35.7 pt), swing (38.1 pt), deep (38.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.71 %** | CVaR **-9.83 %** | vol 4.7 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 3.12 % contre 6.13 % aujourd'hui, rapport 0.51)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.32 % vs -6.94 % si l'on extrapolait par √5 _(rapport 0.912 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1611** (β de hausse 1.3379, asymétrie 0.8678) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.194 | EV/share : ₩5627.934 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 3 % | T2 2 % | T3 1 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 55.6 | bear 8.9 | side 35.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.629% → cible +5.075% / stop −2.537%, p_fill 58%, n_eff≈27.5) : P(cible|rempli) **6%** · **EV/risk -0.206** (×p_fill ; si rempli -0.90% du capital)
  - **swing** (entrée dip −5.795% → cible +24.804% / stop −12.0%, p_fill 46%, n_eff≈22.0) : P(cible|rempli) **6%** · **EV/risk -0.115** (×p_fill ; si rempli -2.98% du capital)
  - **deep** (entrée dip −8.953% → cible +14.195% / stop −11.31%, p_fill 57%, n_eff≈23.8) : P(cible|rempli) **36%** · **EV/risk -0.043** (×p_fill ; si rempli -0.86% du capital)
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
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 29% · rebond 54% · **stop −6.67%** sous le fill (sous le bruit) · cible +1.2% · R/R 0.18 (high win-rate)
- Gaps overnight (n=158) : méd. 0.7% · baisse 42% (gap-down >1% 33% · >2% 23%)
- Excursion ouverture 5min (n=159) : bas méd −0.74% (p90 −1.64%) · haut méd +0.61% · range méd 1.56%
- Excursion ouverture 15min (n=159) : bas méd −1.03% (p90 −2.57%) · haut méd +1.04% · range méd 2.24%
- Excursion ouverture 30min (n=159) : bas méd −1.24% (p90 −3.11%) · haut méd +1.17% · range méd 2.66%
- Excursion ouverture 60min (n=159) : bas méd −1.75% (p90 −3.58%) · haut méd +1.33% · range méd 3.14%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 281300.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 50% · séance 65% (98/158) · gap 35% · délai 0.0min · rebond 50% (52/98) (MFE +0.97%)
   - −1.0% : fill 30min 47% · séance 63% (92/158) · gap 33% · délai 0.0min · rebond 60% (53/92) (MFE +1.25%)
   - −1.5% : fill 30min 41% · séance 55% (80/158) · gap 24% · délai 0.1min · rebond 59% (48/80) (MFE +1.34%)
   - −2.0% : fill 30min 35% · séance 47% (70/158) · gap 23% · délai 0.2min · rebond 56% (40/70) (MFE +1.57%)
   - −3.0% : fill 30min 28% · séance 44% (61/158) · gap 18% · délai 1.7min · rebond 58% (39/61) (MFE +1.75%)
   - −4.0% : fill 30min 21% · séance 36% (48/158) · gap 14% · délai 22.5min · rebond 55% (31/48) (MFE +1.33%)
   - −5.0% : fill 30min 14% · séance 29% (37/158) · gap 10% · délai 47.6min · rebond 54% (23/37) (MFE +1.2%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.48% (p90 −2.08%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.53% (p90 −3.03%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.65% (p90 −3.1%) → stop au-delà de −1.7% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=752 jambes) : jambe baissière méd −1.27% (p90 −3.07%) · ~12.4 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (65 séances) :
      · −1.0% : fill 98% (62/65) · rebond 44% (31/62)
      · −2.0% : fill 86% (53/65) · rebond 42% (26/53)
      · −3.0% : fill 84% (48/65) · rebond 49% (29/48)
      · −4.0% : fill 75% (40/65) · rebond 46% (24/40)
      · −5.0% : fill 67% (32/65) · rebond 48% (18/32)
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

- **RSI** : 55.7  _(momentum haussier)_
- **ADX** : 17.5  _(pas de tendance nette)_
- **MACD** : hist 4980.6  _(pas de croisement recent)_
- **BB** : %B 0.62 · largeur 34.7%
- **ATR** : 17642.86 (72.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.097  _(distribution)_
- **Vol ratio** : 1.05  _(volume normal)_
- **Choppiness** : 53.3  _(transition)_
- **MA** : MA20 246600.0 · MA50 281036.99 · MA200 204388.37  _(prix > MA20)_
- **Dist MA** : MA20 +4.2% · MA50 -8.6% · MA200 +25.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (743088 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
