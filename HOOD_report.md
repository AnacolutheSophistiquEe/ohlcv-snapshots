# HOOD

**Generated** : 2026-08-21T00:34:21.796397+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $95.10  

> 🟡 **WAIT-FOR-DIP** — spot +0.8 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $95.10 (+0.8% vs entrée) · entrée $94.33 · stop $89.60 · T1 $98.15 · R/R 0.81  
> ↳ P(T1 av. stop) 51 % _(réel 5 s)_ · EV/risk 0.007 _(réel 5 s)_ (GBM -0.057) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.200 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $93.57–$95.09 (mid $94.33)
- Spot actuel : $95.10 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : $89.60 (stop swing_plan-based (-5.79%))
- Targets : T1 $98.15 · R/R 0.81 | T2 $101.96 · R/R 1.61 | T3 $105.78 · R/R 2.42
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $89.60


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.10 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (5.79 %)** : le gap seul le franchit 1.437 % des séances (18 fois sur 1253).
   - exécution **2.983 pt plus bas** dans le cas TYPIQUE (médiane), 6.781 au p90, **11.995 au pire**
   - perte réelle **9.362 %** en moyenne _(tirée par la queue)_, jusqu'à **17.785 %** — au lieu des 5.79 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0513 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.458 % | p01 -7.308 % | pire -17.785 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1332** [0.0888 ; 0.1898] _(largeur 10.1 pt, n_eff 173.1)_
   - swing : **0.5122** [0.4596 ; 0.5646] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.5581** [0.5054 ; 0.6098] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.2 pt), swing (32.0 pt), deep (30.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-6.19 %** | CVaR **-9.11 %** | vol 4.31 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 2.08 % contre 4.31 % aujourd'hui, rapport 0.48)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.55 % vs -14.5 % si l'on extrapolait par √5 _(rapport 1.003 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7606** (β de hausse 1.6157, asymétrie 1.0897) vs IWM — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.519× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : cela veut dire que la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier n'est alors PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable.**
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.49 ATR (stop 3.912 %) — p(stop avant cible) 0.4517 [0.40 ; 0.50], R/R 0.497, perte reelle 6.451 % (gap inclus), EV -1.1593 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.30 ATR du spot, sous le seuil de 1 ATR : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545] sur 940 touches) contre ~35 % au-dela. L'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.16 %) : P(cible) 54.8 % x 3.20 % + P(rien) 0.1 % x -0.22 % ne couvrent pas P(stop) 45.2 % x 6.45 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 7.469 %) — p(stop avant cible) 0.3006 [0.25 ; 0.35], R/R 0.305, perte reelle 10.494 % (gap inclus), EV -0.9528 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.95 %) : P(cible) 69.4 % x 3.20 % + P(rien) 0.5 % x -4.38 % ne couvrent pas P(stop) 30.1 % x 10.49 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.61 ATR (stop 14.498 %) — p(stop avant cible) 0.1406 [0.11 ; 0.18], R/R 0.18, perte reelle 17.785 % (gap inclus), EV -0.4363 % — **REFUSE**
      - refuse : R/R 0.18 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.50 % > budget 12.0 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.44 %) : P(cible) 78.8 % x 3.20 % + P(rien) 7.2 % x -6.39 % ne couvrent pas P(stop) 14.1 % x 17.79 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.41 ATR (stop 18.497 %) — p(stop avant cible) 0.0807 [0.06 ; 0.11], R/R 0.173, perte reelle 18.497 % (gap inclus), EV 0.052 % — **REFUSE**
      - refuse : R/R 0.17 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.50 % > budget 12.0 %
   - 🟢 support a 5.47 ATR (stop 28.707 %) — p(stop avant cible) 0.0204 [0.01 ; 0.04], R/R 0.112, perte reelle 28.707 % (gap inclus), EV 0.0458 % — **REFUSE**
      - refuse : R/R 0.11 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.71 % > budget 12.0 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : -0.057 | EV/share : $-0.268 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 28 % | T3 15 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 65.0 | bear 27.4 | side 7.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 476.0 (= 5 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.371% → cible +1.809% / stop −3.0%, p_fill 91%, n_eff≈36.9) : P(cible|rempli) **49%** · **EV/risk -0.044** (×p_fill ; si rempli -0.14% du capital)
  - **swing** (entrée dip −0.811% → cible +4.044% / stop −5.02%, p_fill 86%, n_eff≈35.0) : P(cible|rempli) **51%** · **EV/risk +0.007** (×p_fill ; si rempli +0.04% du capital)
  - **deep** (entrée dip −1.251% → cible +5.72% / stop −7.564%, p_fill 86%, n_eff≈36.5) : P(cible|rempli) **60%** · **EV/risk +0.011** (×p_fill ; si rempli +0.10% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→80% · +2.0%→56% · +3.0%→35% · +5.0%→21% · +8.0%→6%
- Range intraday médian 5.07% (p90 8.92%) · excursion haute méd. +2.16% / basse méd. −2.21%
- Profil de vol intra : ouverture 3.708% vs midi 1.039% vs clôture 1.144% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 17% · trend ↑1%/↓0% ; spike-down 67% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.113 ; neutre — autocorr -0.014)_ ; drift intra méd. -0.286% ; recovery-V 31%
- **σ réalisé intraday** 3.53% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 41% / bas 48% / whipsaw 8%
- POC intraday (dernière séance, temps-au-prix) : 94.2961 (VA 93.9326–95.2049 ; dernier close 95.11)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 28% · rebond 80% · **stop −4.62%** sous le fill (sous le bruit) · cible +2.37% · R/R 0.51 (high win-rate)
- Gaps overnight (n=159) : méd. 0.03% · baisse 49% (gap-down >1% 33% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.94% (p90 −2.69%) · haut méd +0.85% · range méd 2.17%
- Excursion ouverture 15min (n=160) : bas méd −1.16% (p90 −3.88%) · haut méd +1.24% · range méd 2.83%
- Excursion ouverture 30min (n=160) : bas méd −1.37% (p90 −4.21%) · haut méd +1.67% · range méd 3.41%
- Excursion ouverture 60min (n=160) : bas méd −1.77% (p90 −4.66%) · haut méd +1.71% · range méd 3.88%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 95.11 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 79% (125/159) · gap 39% · délai 0.0min · rebond 58% (67/125) (MFE +1.48%)
   - −1.0% : fill 30min 60% · séance 70% (110/159) · gap 33% · délai 0.0min · rebond 63% (65/110) (MFE +1.54%)
   - −1.5% : fill 30min 50% · séance 60% (100/159) · gap 24% · délai 0.2min · rebond 60% (58/100) (MFE +1.34%)
   - −2.0% : fill 30min 40% · séance 50% (88/159) · gap 16% · délai 0.2min · rebond 68% (55/88) (MFE +1.37%)
   - −3.0% : fill 30min 28% · séance 39% (68/159) · gap 7% · délai 6.5min · rebond 73% (46/68) (MFE +1.84%)
   - −4.0% : fill 30min 17% · séance 28% (50/159) · gap 3% · délai 10.8min · rebond 80% (34/50) (MFE +2.37%)
   - −5.0% : fill 30min 10% · séance 17% (33/159) · gap 2% · délai 19.0min · rebond 76% (25/33) (MFE +2.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.62% (p90 −2.45%) → stop au-delà de −1.59% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.62% (p90 −2.42%) → stop au-delà de −1.41% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −2.43%) → stop au-delà de −1.53% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=765 jambes) : jambe baissière méd −1.14% (p90 −2.84%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (73 séances) :
      · −1.0% : fill 97% (70/73) · rebond 51% (36/70)
      · −2.0% : fill 82% (60/73) · rebond 62% (36/60)
      · −3.0% : fill 69% (50/73) · rebond 70% (33/50)
      · −4.0% : fill 53% (39/73) · rebond 83% (29/39)
      · −5.0% : fill 32% (27/73) · rebond 72% (20/27)
   - **flat** (20 séances) :
      · −1.0% : fill 64% (14/20) · rebond 80% (9/14)
      · −2.0% : fill 40% (11/20) · rebond 61% (7/11)
      · −3.0% : fill 14% (6/20) · rebond 23% (2/6)
      · −4.0% : fill 13% (5/20) · rebond 16% (1/5)
      · −5.0% : fill 6% (3/20) · rebond 82% (2/3)
   - **gap-up** (66 séances) :
      · −1.0% : fill 45% (26/66) · rebond 82% (20/26)
      · −2.0% : fill 22% (17/66) · rebond 90% (12/17)
      · −3.0% : fill 16% (12/66) · rebond 98% (11/12)
      · −4.0% : fill 8% (6/66) · rebond 88% (4/6)
      · −5.0% : fill 4% (3/66) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 65% si les 15 1res min sont vertes (76 cas) · 33% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:23** → P(séance verte=clôture>ouverture) 78% si début vert vs 23% si rouge (base 48% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 227min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **78%** · continue >prix actuel 47% ; creux résiduel méd -1.26% (q20 -2.42%) → **SL/trailing à −2.42%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.25% / q75 +2.7% → **scale +1.25% / runner +2.7%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **23%** (continue à baisser 54%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.53%** (au-delà de la MAE q10 -3.53%), cible rebond +1.71% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.47% .. +3.97%] · haut q95 +4.24% · bas q05 -5.21%
   - 60min (n=160) : retour [-4.23% .. +4.34%] · haut q95 +5.16% · bas q05 -5.76%
   - 2h (n=160) : retour [-4.97% .. +4.98%] · haut q95 +6.42% · bas q05 -6.15%
   - 4h (n=160) : retour [-5.1% .. +5.75%] · haut q95 +7.4% · bas q05 -6.84%
   - 6h (n=160) : retour [-5.78% .. +6.15%] · haut q95 +7.4% · bas q05 -7.13%
   - session (n=160) : retour [-5.55% .. +5.88%] · haut q95 +7.5% · bas q05 -7.23%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 7.5% des séances sont trend-up (mild 0% / strong 7.5%) · base = 12 séances trend-up (n_eff 9.5)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **27%**. Lecture précoce 30 min : signature présente → 14% vs absente 3% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.92% (p75 1.43% / p90 2.14%) · ~4.0 replis/séance, durée méd 36.99 min. P(nouveau plus-haut après repli) :
   - −0.5% → **82%** (reprise méd 20.0 min, n=45)
   - −1.0% → **70%** (reprise méd 33.9 min, n=21)
   - −1.5% → **45%** (reprise méd 52.28 min, n=11)
   - −2.0% → **25%** (reprise méd None min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−2.14%** (p90, défaut prudent ; serré/agressif −1.43%) ; extension open→close méd +6.08% (q75 +9.71% / q95 +13.38%), MFE méd +6.85% / q90 +14.87%
   - Échelle scale-out : +6.85% (33%) / +11.38% (33%) / +14.87% (34%)
- **DÉSARMER** : repli > **−2.14%** depuis le plus-haut = décay → P(retournement) **75%** (préavis méd 165.69 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +14.87% : P(retournement après) 0% (mèche méd 5.8%)
- **CONTEXTE** : la dernière heure tient les gains 78% du temps (retour médian dernière heure +0.75%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 63.0  _(momentum haussier)_
- **ADX** : 14.7  _(pas de tendance nette)_
- **MACD** : hist 0.411  _(pas de croisement recent)_
- **BB** : %B 0.65 · largeur 13.7%
- **ATR** : 4.74 (23.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.203  _(distribution)_
- **Vol ratio** : 1.37  _(volume normal)_
- **Choppiness** : 53.1  _(transition)_
- **MA** : MA20 93.22 · MA50 99.87 · MA200 96.28  _(prix > MA20)_
- **Dist MA** : MA20 +2.0% · MA50 -4.8% · MA200 -1.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (603551 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
