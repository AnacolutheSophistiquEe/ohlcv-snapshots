# RGTI

**Generated** : 2026-08-21T00:30:08.158263+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $16.07  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $16.07 (+3.8% vs entrée) · entrée $15.48 · stop $14.38 · T1 $17.27 · R/R 1.63  
> ↳ P(T1 av. stop) 23 % _(réel 5 s)_ · EV/risk -0.052 _(réel 5 s)_ (GBM -0.054) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $15.25–$15.71 (mid $15.48)
- Spot actuel : $16.07 (+3.8% au-dessus de la zone — repli à attendre)
- Stop : $14.38 (stop swing_plan-based (-10.5%))
- Targets : T1 $17.27 · R/R 1.63 | T2 $18.10 · R/R 2.38 | T3 $18.93 · R/R 3.14
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $14.38


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.30 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.5 %)** : le gap seul le franchit 0.718 % des séances (9 fois sur 1253).
   - exécution **3.316 pt plus bas** dans le cas TYPIQUE (médiane), 10.076 au p90, **20.713 au pire**
   - perte réelle **15.505 %** en moyenne _(tirée par la queue)_, jusqu'à **31.213 %** — au lieu des 10.5 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.036 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 9 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.085 % | p01 -8.973 % | pire -31.213 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2923** [0.2284 ; 0.3631] _(largeur 13.5 pt, n_eff 173.1)_
   - swing : **0.5522** [0.4995 ; 0.604] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.5576** [0.5049 ; 0.6093] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (36.5 pt), swing (38.3 pt), deep (34.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-8.8 %** | CVaR **-10.8 %** | vol 6.84 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 16.36 % contre 6.37 % aujourd'hui, rapport 2.57)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -21.76 % vs -22.11 % si l'on extrapolait par √5 _(rapport 0.984 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8381** (β de hausse 1.9888, asymétrie 0.9242) vs IWM — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.663× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : cela veut dire que la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier n'est alors PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable.**
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 1.06 ATR (stop 9.353 %) — p(stop avant cible) 0.4499 [0.40 ; 0.50], R/R 0.531, perte reelle 14.11 % (gap inclus), EV -2.3987 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.40 %) : P(cible) 53.6 % x 7.49 % + P(rien) 1.5 % x -4.23 % ne couvrent pas P(stop) 45.0 % x 14.11 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 support a 1.45 ATR (stop 11.989 %) — p(stop avant cible) 0.3974 [0.35 ; 0.45], R/R 0.445, perte reelle 16.825 % (gap inclus), EV -2.4458 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.02 % > budget 12.0 %
      - ⚠ support DETECTE a 0.96 ATR du spot, sous le seuil de 1 ATR : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545] sur 940 touches) contre ~35 % au-dela. L'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.45 %) : P(cible) 58.0 % x 7.49 % + P(rien) 2.3 % x -4.41 % ne couvrent pas P(stop) 39.7 % x 16.83 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.86 ATR (stop 21.703 %) — p(stop avant cible) 0.1497 [0.12 ; 0.19], R/R 0.24, perte reelle 31.213 % (gap inclus), EV -1.4676 % — **REFUSE**
      - refuse : R/R 0.24 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.71 % > budget 12.0 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.47 %) : P(cible) 65.5 % x 7.49 % + P(rien) 19.5 % x -8.71 % ne couvrent pas P(stop) 15.0 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.2 ATR (stop 24.065 %) — p(stop avant cible) 0.1037 [0.07 ; 0.14], R/R 0.24, perte reelle 31.213 % (gap inclus), EV -0.7184 % — **REFUSE**
      - refuse : R/R 0.24 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.07 % > budget 12.0 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.72 %) : P(cible) 65.5 % x 7.49 % + P(rien) 24.1 % x -9.91 % ne couvrent pas P(stop) 10.4 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : -0.054 | EV/share : $-0.059 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 30 % | T2 19 % | T3 11 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.7 | bear 27.9 | side 66.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 145.0 (= 9 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.65% → cible +3.167% / stop −2.095%, p_fill 61%, n_eff≈26.3) : P(cible|rempli) **35%** · **EV/risk +0.004** (×p_fill ; si rempli +0.01% du capital)
  - **swing** (entrée dip −3.633% → cible +11.541% / stop −7.126%, p_fill 47%, n_eff≈23.7) : P(cible|rempli) **23%** · **EV/risk -0.052** (×p_fill ; si rempli -0.79% du capital)
  - **deep** (entrée dip −5.611% → cible +25.404% / stop −12.702%, p_fill 61%, n_eff≈28.8) : P(cible|rempli) **23%** · **EV/risk +0.018** (×p_fill ; si rempli +0.36% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→91% · +1.0%→80% · +2.0%→74% · +3.0%→57% · +5.0%→42% · +8.0%→14%
- Range intraday médian 7.89% (p90 13.36%) · excursion haute méd. +4.06% / basse méd. −2.46%
- Profil de vol intra : ouverture 5.491% vs midi 1.576% vs clôture 1.842% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 19% · trend ↑0%/↓0% ; spike-down 71% · recovery-V 40%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; neutre — autocorr -0.026)_ ; drift intra méd. 0.325% ; recovery-V 33%
- **σ réalisé intraday** 4.584% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 45% / whipsaw 6%
- POC intraday (dernière séance, temps-au-prix) : 16.9713 (VA 16.777–17.2488 ; dernier close 17.01)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 43% · rebond 77% · **stop −6.3%** sous le fill (sous le bruit) · cible +2.32% · R/R 0.37 (high win-rate)
- Gaps overnight (n=159) : méd. -0.48% · baisse 58% (gap-down >1% 42% · >2% 29%)
- Excursion ouverture 5min (n=160) : bas méd −1.19% (p90 −2.9%) · haut méd +1.28% · range méd 2.68%
- Excursion ouverture 15min (n=160) : bas méd −1.44% (p90 −3.99%) · haut méd +1.87% · range méd 3.78%
- Excursion ouverture 30min (n=160) : bas méd −1.83% (p90 −4.77%) · haut méd +2.1% · range méd 4.66%
- Excursion ouverture 60min (n=160) : bas méd −2.13% (p90 −6.02%) · haut méd +2.53% · range méd 5.52%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 17.01 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 78% · séance 84% (135/159) · gap 48% · délai 0.0min · rebond 66% (88/135) (MFE +2.44%)
   - −1.0% : fill 30min 68% · séance 76% (127/159) · gap 42% · délai 0.0min · rebond 69% (83/127) (MFE +2.02%)
   - −1.5% : fill 30min 60% · séance 69% (120/159) · gap 36% · délai 0.0min · rebond 69% (80/120) (MFE +2.24%)
   - −2.0% : fill 30min 56% · séance 63% (112/159) · gap 29% · délai 0.0min · rebond 70% (76/112) (MFE +2.48%)
   - −3.0% : fill 30min 50% · séance 56% (98/159) · gap 13% · délai 1.2min · rebond 76% (72/98) (MFE +2.48%)
   - −4.0% : fill 30min 36% · séance 43% (77/159) · gap 5% · délai 5.6min · rebond 77% (57/77) (MFE +2.32%)
   - −5.0% : fill 30min 19% · séance 34% (63/159) · gap 3% · délai 21.6min · rebond 70% (48/63) (MFE +1.99%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.74% (p90 −2.21%) → stop au-delà de −1.53% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.89% (p90 −2.69%) → stop au-delà de −2.01% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.04% (p90 −2.93%) → stop au-delà de −2.07% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1177 jambes) : jambe baissière méd −1.29% (p90 −3.09%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (84 séances) :
      · −1.0% : fill 95% (82/84) · rebond 64% (50/82)
      · −2.0% : fill 85% (77/84) · rebond 69% (52/77)
      · −3.0% : fill 80% (71/84) · rebond 71% (50/71)
      · −4.0% : fill 65% (57/84) · rebond 75% (41/57)
      · −5.0% : fill 52% (48/84) · rebond 69% (37/48)
   - **flat** (16 séances) :
      · −1.0% : fill 96% (15/16) · rebond 95% (13/15)
      · −2.0% : fill 71% (12/16) · rebond 85% (10/12)
      · −3.0% : fill 48% (7/16) · rebond 90% (5/7)
      · −4.0% : fill 32% (6/16) · rebond 85% (4/6)
      · −5.0% : fill 20% (5/16) · rebond 87% (3/5)
   - **gap-up** (59 séances) :
      · −1.0% : fill 43% (30/59) · rebond 67% (20/30)
      · −2.0% : fill 30% (23/59) · rebond 63% (14/23)
      · −3.0% : fill 25% (20/59) · rebond 89% (17/20)
      · −4.0% : fill 16% (14/59) · rebond 84% (12/14)
      · −5.0% : fill 13% (10/59) · rebond 68% (8/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 70% si les 15 1res min sont vertes (80 cas) · 30% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **51min** → P(séance verte=clôture>ouverture) 88% si début vert vs 16% si rouge (base 52% · écart 72 pts) ; prédictivité sature ensuite (plafond brut 91min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **88%** · continue >prix actuel 50% ; creux résiduel méd -2.39% (q20 -3.58%) → **SL/trailing à −3.58%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.34% / q75 +5.27% → **scale +2.34% / runner +5.27%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **16%** (continue à baisser 57%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.37%** (au-delà de la MAE q10 -5.37%), cible rebond +2.1% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.24% .. +4.96%] · haut q95 +6.51% · bas q05 -6.36%
   - 60min (n=160) : retour [-5.57% .. +6.41%] · haut q95 +6.71% · bas q05 -6.86%
   - 2h (n=160) : retour [-5.84% .. +7.05%] · haut q95 +9.14% · bas q05 -7.6%
   - 4h (n=160) : retour [-7.26% .. +7.22%] · haut q95 +9.18% · bas q05 -7.88%
   - 6h (n=160) : retour [-7.5% .. +8.25%] · haut q95 +9.43% · bas q05 -8.66%
   - session (n=160) : retour [-7.39% .. +8.56%] · haut q95 +10.21% · bas q05 -8.66%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 6.8)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **30%**. Lecture précoce 30 min : signature présente → 14% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.25% (p75 1.69% / p90 2.67%) · ~4.0 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 13.25 min, n=41)
   - −1.0% → **77%** (reprise méd 55.8 min, n=26)
   - −1.5% → **78%** (reprise méd 94.96 min, n=15)
   - −2.0% → **79%** (reprise méd 109.11 min, n=8)
   - −3.0% → **67%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.67%** (p90, défaut prudent ; serré/agressif −1.69%) ; extension open→close méd +7.29% (q75 +9.11% / q95 +9.99%), MFE méd +9.12% / q90 +10.34%
   - Échelle scale-out : +9.12% (33%) / +10.23% (33%) / +10.34% (34%)
- **DÉSARMER** : repli > **−2.67%** depuis le plus-haut = décay → P(retournement) **33%** (préavis méd 141.49 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.34% : P(retournement après) 0% (mèche méd 1.02%)
- **CONTEXTE** : la dernière heure tient les gains 59% du temps (retour médian dernière heure +0.5%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 56.2  _(momentum haussier)_
- **ADX** : 18.0  _(pas de tendance nette)_
- **MACD** : hist 0.06  _(pas de croisement recent)_
- **BB** : %B 0.41 · largeur 40.1%
- **ATR** : 1.1 (8.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.003  _(neutre)_
- **Vol ratio** : 1.02  _(volume normal)_
- **Choppiness** : 45.4  _(transition)_
- **MA** : MA20 16.66 · MA50 17.46 · MA200 20.15  _(prix < MA20)_
- **Dist MA** : MA20 -3.5% · MA50 -8.0% · MA200 -20.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (598625 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
