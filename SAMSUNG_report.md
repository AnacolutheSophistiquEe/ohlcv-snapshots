# 005930

**Generated** : 2026-08-20T20:00:24.454414+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 8.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩267000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩267000.00 (+1.4% vs entrée) · entrée ₩263265.16 · stop ₩242836.59 · T1 ₩289199.26 · R/R 1.27  
> ↳ P(T1 av. stop) 28 % _(réel 5 s)_ · EV/risk -0.24 _(réel 5 s)_ (GBM 0.312) · ¼-Kelly 0.015 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.130 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩259530.33–₩267000.00 (mid ₩263265.16)
- Spot actuel : ₩267000.00 (+1.4% au-dessus de la zone — repli à attendre)
- Stop : ₩242836.59 (stop swing_plan-based (-9.05%))
- Targets : T1 ₩289199.26 · R/R 1.27 | T2 ₩315133.36 · R/R 2.54 | T3 ₩341067.46 · R/R 3.81
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩242836.59


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.61 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.05 %)** : le gap seul le franchit 0.082 % des séances (1 fois sur 1218).
   - exécution **1.892 pt plus bas** dans le cas TYPIQUE (médiane), 1.892 au p90, **1.892 au pire**
   - perte réelle **10.942 %** en moyenne _(tirée par la queue)_, jusqu'à **10.942 %** — au lieu des 9.05 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0016 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.284 % | p01 -4.951 % | pire -10.942 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2055** [0.1505 ; 0.2703] _(largeur 12.0 pt, n_eff 173.1)_
   - swing : **0.3072** [0.2603 ; 0.3573] _(largeur 9.7 pt, n_eff 345.6)_
   - deep : **0.3577** [0.3085 ; 0.4093] _(largeur 10.1 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (30.1 pt), swing (31.6 pt), deep (32.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.29 %** | CVaR **-9.74 %** | vol 4.65 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 3.04 % contre 6.07 % aujourd'hui, rapport 0.50)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.29 % vs -6.91 % si l'on extrapolait par √5 _(rapport 0.911 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1611** (β de hausse 1.3323, asymétrie 0.8714) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.312 | EV/share : ₩6372.784 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 10 % | T3 1 %
- Kelly (position) : f* 0.061 | ¼-Kelly 0.015 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 57.6 | bear 12.6 | side 29.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.635% → cible +4.405% / stop −2.31%, p_fill 94%, n_eff≈36.9) : P(cible|rempli) **17%** · **EV/risk -0.349** (×p_fill ; si rempli -0.86% du capital)
  - **swing** (entrée dip −1.399% → cible +9.851% / stop −7.76%, p_fill 83%, n_eff≈35.1) : P(cible|rempli) **28%** · **EV/risk -0.240** (×p_fill ; si rempli -2.24% du capital)
  - **deep** (entrée dip −2.023% → cible +13.931% / stop −11.714%, p_fill 87%, n_eff≈33.3) : P(cible|rempli) **23%** · **EV/risk -0.275** (×p_fill ; si rempli -3.69% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→70% · +2.0%→45% · +3.0%→36% · +5.0%→24% · +8.0%→5%
- Range intraday médian 6.22% (p90 9.84%) · excursion haute méd. +1.88% / basse méd. −3.12%
- Profil de vol intra : ouverture 3.131% vs midi 1.377% vs clôture 1.574% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (157 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 10% · trend ↑0%/↓1% ; spike-down 72% · recovery-V 19%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; mean-reverting — autocorr -0.102)_ ; drift intra méd. -1.276% ; recovery-V 17%
- **σ réalisé intraday** 4.303% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 78% / whipsaw 26%
- POC intraday (dernière séance, temps-au-prix) : 248600.0 (VA 248400.0–251000.0 ; dernier close 248300.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 30% · rebond 54% · **stop −6.67%** sous le fill (sous le bruit) · cible +1.2% · R/R 0.18 (high win-rate)
- Gaps overnight (n=156) : méd. 0.7% · baisse 41% (gap-down >1% 33% · >2% 24%)
- Excursion ouverture 5min (n=157) : bas méd −0.74% (p90 −1.64%) · haut méd +0.61% · range méd 1.56%
- Excursion ouverture 15min (n=157) : bas méd −1.03% (p90 −2.64%) · haut méd +1.04% · range méd 2.21%
- Excursion ouverture 30min (n=157) : bas méd −1.24% (p90 −3.16%) · haut méd +1.12% · range méd 2.66%
- Excursion ouverture 60min (n=157) : bas méd −1.75% (p90 −3.59%) · haut méd +1.24% · range méd 3.11%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 248300.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 50% · séance 65% (97/156) · gap 35% · délai 0.0min · rebond 48% (51/97) (MFE +0.88%)
   - −1.0% : fill 30min 47% · séance 63% (91/156) · gap 33% · délai 0.0min · rebond 59% (52/91) (MFE +1.22%)
   - −1.5% : fill 30min 40% · séance 55% (79/156) · gap 25% · délai 0.3min · rebond 58% (47/79) (MFE +1.34%)
   - −2.0% : fill 30min 36% · séance 49% (70/156) · gap 24% · délai 0.2min · rebond 56% (40/70) (MFE +1.57%)
   - −3.0% : fill 30min 30% · séance 45% (61/156) · gap 19% · délai 1.7min · rebond 58% (39/61) (MFE +1.75%)
   - −4.0% : fill 30min 22% · séance 37% (48/156) · gap 15% · délai 22.5min · rebond 55% (31/48) (MFE +1.33%)
   - −5.0% : fill 30min 14% · séance 30% (37/156) · gap 11% · délai 47.6min · rebond 54% (23/37) (MFE +1.2%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.48% (p90 −2.14%) → stop au-delà de −1.55% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.53% (p90 −3.1%) → stop au-delà de −1.51% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.65% (p90 −3.57%) → stop au-delà de −1.62% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=740 jambes) : jambe baissière méd −1.28% (p90 −3.08%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (64 séances) :
      · −1.0% : fill 98% (61/64) · rebond 41% (30/61)
      · −2.0% : fill 90% (53/64) · rebond 42% (26/53)
      · −3.0% : fill 88% (48/64) · rebond 49% (29/48)
      · −4.0% : fill 79% (40/64) · rebond 46% (24/40)
      · −5.0% : fill 70% (32/64) · rebond 48% (18/32)
   - **flat** (14 séances) :
      · −1.0% : fill 65% (8/14) · rebond 78% (5/8)
      · −2.0% : fill 33% (4/14) · rebond 85% (3/4)
      · −3.0% : fill 33% (4/14) · rebond 85% (3/4)
      · −4.0% : fill 15% (2/14) · rebond 100% (2/2)
      · −5.0% : fill 15% (2/14) · rebond 100% (2/2)
   - **gap-up** (78 séances) :
      · −1.0% : fill 38% (22/78) · rebond 84% (17/22)
      · −2.0% : fill 23% (13/78) · rebond 86% (11/13)
      · −3.0% : fill 18% (9/78) · rebond 81% (7/9)
      · −4.0% : fill 11% (6/78) · rebond 94% (5/6)
      · −5.0% : fill 4% (3/78) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=157) : 36% en base · 56% si les 15 1res min sont vertes (78 cas) · 16% si rouges (79 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=157) : COUDE à **1:15** → P(séance verte=clôture>ouverture) 81% si début vert vs 5% si rouge (base 36% · écart 76 pts) ; prédictivité sature ensuite (plafond brut 75min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **81%** · continue >prix actuel 55% ; creux résiduel méd -1.37% (q20 -4.07%) → **SL/trailing à −4.07%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.82% / q75 +3.53% → **scale +1.82% / runner +3.53%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **5%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.96%** (au-delà de la MAE q10 -6.96%), cible rebond +1.3% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=157) : retour [-2.82% .. +2.81%] · haut q95 +3.68% · bas q05 -3.75%
   - 60min (n=157) : retour [-3.14% .. +4.4%] · haut q95 +5.34% · bas q05 -5.13%
   - 2h (n=157) : retour [-4.62% .. +4.55%] · haut q95 +6.11% · bas q05 -6.13%
   - 4h (n=157) : retour [-6.28% .. +5.59%] · haut q95 +6.88% · bas q05 -7.79%
   - 6h (n=157) : retour [-7.2% .. +5.06%] · haut q95 +7.01% · bas q05 -8.13%
   - session (n=157) : retour [-7.39% .. +5.28%] · haut q95 +7.01% · bas q05 -8.74%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.8% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.95%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 65.5  _(momentum haussier)_
- **ADX** : 18.8  _(pas de tendance nette)_
- **MACD** : hist 5393.717  _(pas de croisement recent)_
- **BB** : %B 0.77 · largeur 32.8%
- **ATR** : 20428.57 (76.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.131  _(distribution)_
- **Vol ratio** : 0.72  _(volume normal)_
- **Choppiness** : 58.9  _(transition)_
- **MA** : MA20 245450.0 · MA50 282203.74 · MA200 202667.88  _(prix > MA20)_
- **Dist MA** : MA20 +8.8% · MA50 -5.4% · MA200 +31.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (401983 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
