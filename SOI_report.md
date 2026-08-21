# SOI

**Generated** : 2026-08-21T00:10:30.271205+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €109.55  

> 🟡 **WAIT-FOR-DIP** — spot +1.5 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €109.55 (+1.5% vs entrée) · entrée €107.94 · stop €97.91 · T1 €128.00 · R/R 2.0  
> ↳ P(T1 av. stop) 17 % _(réel 5 s)_ · EV/risk 0.144 _(réel 5 s)_ (GBM 0.211) · ¼-Kelly 0.004 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €106.33–€109.55 (mid €107.94)
- Spot actuel : €109.55 (+1.5% au-dessus de la zone — repli à attendre)
- Stop : €97.91 (stop swing_plan-based (-10.63%))
- Targets : T1 €128.00 · R/R 2.0 | T2 €135.75 · R/R 2.77 | T3 €137.26 · R/R 2.92
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €97.91


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.83 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.63 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1279).
   - exécution **8.089 pt plus bas** dans le cas TYPIQUE (médiane), 16.549 au p90, **18.664 au pire**
   - perte réelle **21.456 %** en moyenne _(tirée par la queue)_, jusqu'à **29.294 %** — au lieu des 10.63 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0254 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.589 % | p01 -4.835 % | pire -29.294 % _(sur 1279 séances)_
- **P(stop avant cible)** _(source : daily, 1280 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2532** [0.1929 ; 0.3217] _(largeur 12.9 pt, n_eff 173.1)_
   - swing : **0.443** [0.3913 ; 0.4956] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.494** [0.4415 ; 0.5466] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.5 pt), swing (32.0 pt), deep (31.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.63 %** | CVaR **-13.66 %** | vol 6.49 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 4.39 % contre 7.72 % aujourd'hui, rapport 0.57)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.13 % vs -11.25 % si l'on extrapolait par √5 _(rapport 1.078 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1305** (β de hausse 1.6122, asymétrie 0.7012) vs FCHI — 616 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.118× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : cela veut dire que la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier n'est alors PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable.**
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.5 ATR (stop 5.908 %) — p(stop avant cible) 0.4437 [0.39 ; 0.50], R/R 0.4, perte reelle 13.196 % (gap inclus), EV -3.0655 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.28 ATR du spot, sous le seuil de 1 ATR : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545] sur 940 touches) contre ~35 % au-dela. L'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.07 %) : P(cible) 53.5 % x 5.27 % + P(rien) 2.1 % x -1.46 % ne couvrent pas P(stop) 44.4 % x 13.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 11.057 %) — p(stop avant cible) 0.2736 [0.23 ; 0.32], R/R 0.246, perte reelle 21.456 % (gap inclus), EV -2.8325 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.83 %) : P(cible) 64.1 % x 5.27 % + P(rien) 8.5 % x -4.04 % ne couvrent pas P(stop) 27.4 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.2 ATR (stop 18.409 %) — p(stop avant cible) 0.113 [0.08 ; 0.15], R/R 0.22, perte reelle 24.006 % (gap inclus), EV -0.2729 % — **REFUSE**
      - refuse : R/R 0.22 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.42 % > budget 12.0 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.27 %) : P(cible) 70.9 % x 5.27 % + P(rien) 17.8 % x -7.32 % ne couvrent pas P(stop) 11.3 % x 24.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.45 ATR (stop 27.67 %) — p(stop avant cible) 0.0428 [0.03 ; 0.07], R/R 0.18, perte reelle 29.294 % (gap inclus), EV 0.2475 % — **REFUSE**
      - refuse : R/R 0.18 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.67 % > budget 12.0 %
   - 🟢 support a 5.5 ATR (stop 42.732 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.123, perte reelle 42.732 % (gap inclus), EV 0.3972 % — **REFUSE**
      - refuse : R/R 0.12 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.73 % > budget 12.0 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.211 | EV/share : €2.119 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 21 % | T2 15 % | T3 13 %
- Kelly (position) : f* 0.016 | ¼-Kelly 0.004 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 58.2 | bear 25.1 | side 16.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 219.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.665% → cible +8.204% / stop −4.102%, p_fill 87%, n_eff≈36.1) : P(cible|rempli) **4%** · **EV/risk -0.140** (×p_fill ; si rempli -0.66% du capital)
  - **swing** (entrée dip −1.474% → cible +18.585% / stop −9.293%, p_fill 80%, n_eff≈34.1) : P(cible|rempli) **17%** · **EV/risk +0.144** (×p_fill ; si rempli +1.68% du capital)
  - **deep** (entrée dip −2.149% → cible +26.634% / stop −13.317%, p_fill 80%, n_eff≈35.8) : P(cible|rempli) **24%** · **EV/risk -0.083** (×p_fill ; si rempli -1.38% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→78% · +2.0%→68% · +3.0%→54% · +5.0%→36% · +8.0%→14%
- Range intraday médian 8.65% (p90 15.11%) · excursion haute méd. +3.5% / basse méd. −3.33%
- Profil de vol intra : ouverture 5.439% vs midi 1.485% vs clôture 2.339% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (158 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 13% · trend ↑0%/↓3% ; spike-down 76% · recovery-V 40%)_
- **Régime intraday** : **chop** _(efficiency 0.138 ; mean-reverting — autocorr -0.07)_ ; drift intra méd. -0.588% ; recovery-V 34%
- **σ réalisé intraday** 4.956% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 68% / bas 54% / whipsaw 32%
- POC intraday (dernière séance, temps-au-prix) : 112.0793 (VA 109.9147–112.4123 ; dernier close 110.76)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 38% · rebond 75% · **stop −7.88%** sous le fill (sous le bruit) · cible +2.79% · R/R 0.35 (high win-rate)
- Gaps overnight (n=157) : méd. 0.11% · baisse 47% (gap-down >1% 31% · >2% 20%)
- Excursion ouverture 5min (n=158) : bas méd −1.16% (p90 −3.77%) · haut méd +0.95% · range méd 2.81%
- Excursion ouverture 15min (n=158) : bas méd −1.43% (p90 −5.09%) · haut méd +1.28% · range méd 3.48%
- Excursion ouverture 30min (n=158) : bas méd −1.55% (p90 −5.47%) · haut méd +1.58% · range méd 4.04%
- Excursion ouverture 60min (n=158) : bas méd −1.7% (p90 −5.87%) · haut méd +1.81% · range méd 4.42%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 110.76 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 79% (124/157) · gap 40% · délai 0.0min · rebond 63% (80/124) (MFE +1.92%)
   - −1.0% : fill 30min 59% · séance 74% (117/157) · gap 31% · délai 0.2min · rebond 70% (84/117) (MFE +1.77%)
   - −1.5% : fill 30min 53% · séance 68% (106/157) · gap 26% · délai 0.2min · rebond 71% (77/106) (MFE +2.12%)
   - −2.0% : fill 30min 48% · séance 61% (97/157) · gap 20% · délai 0.3min · rebond 75% (76/97) (MFE +2.6%)
   - −3.0% : fill 30min 35% · séance 48% (78/157) · gap 13% · délai 0.5min · rebond 73% (61/78) (MFE +2.64%)
   - −4.0% : fill 30min 28% · séance 41% (63/157) · gap 6% · délai 1.1min · rebond 72% (49/63) (MFE +2.44%)
   - −5.0% : fill 30min 22% · séance 38% (55/157) · gap 1% · délai 14.4min · rebond 75% (45/55) (MFE +2.79%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.79% (p90 −3.71%) → stop au-delà de −1.9% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −2.9%) → stop au-delà de −2.14% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.73% (p90 −2.37%) → stop au-delà de −1.98% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1348 jambes) : jambe baissière méd −1.3% (p90 −3.16%) · ~17.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (62 séances) :
      · −1.0% : fill 94% (60/62) · rebond 58% (37/60)
      · −2.0% : fill 91% (58/62) · rebond 68% (44/58)
      · −3.0% : fill 77% (48/62) · rebond 71% (38/48)
      · −4.0% : fill 67% (42/62) · rebond 77% (34/42)
      · −5.0% : fill 62% (37/62) · rebond 82% (31/37)
   - **flat** (17 séances) :
      · −1.0% : fill 100% (17/17) · rebond 79% (14/17)
      · −2.0% : fill 96% (15/17) · rebond 82% (12/15)
      · −3.0% : fill 69% (11/17) · rebond 67% (8/11)
      · −4.0% : fill 57% (8/17) · rebond 65% (6/8)
      · −5.0% : fill 57% (8/17) · rebond 77% (7/8)
   - **gap-up** (78 séances) :
      · −1.0% : fill 51% (40/78) · rebond 84% (33/40)
      · −2.0% : fill 29% (24/78) · rebond 88% (20/24)
      · −3.0% : fill 20% (19/78) · rebond 83% (15/19)
      · −4.0% : fill 15% (13/78) · rebond 55% (9/13)
      · −5.0% : fill 13% (10/78) · rebond 47% (7/10)
- **P(clôture VERTE) selon le drive 15min** (n=158) : 50% en base · 69% si les 15 1res min sont vertes (74 cas) · 32% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=158) : COUDE à **38min** → P(séance verte=clôture>ouverture) 79% si début vert vs 26% si rouge (base 50% · écart 53 pts) ; prédictivité sature ensuite (plafond brut 272min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **79%** · continue >prix actuel 62% ; creux résiduel méd -2.32% (q20 -5.45%) → **SL/trailing à −5.45%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.12% / q75 +4.83% → **scale +3.12% / runner +4.83%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **26%** (continue à baisser 63%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.71%** (au-delà de la MAE q10 -8.71%), cible rebond +2.71% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=158) : retour [-5.16% .. +6.66%] · haut q95 +7.84% · bas q05 -6.28%
   - 60min (n=158) : retour [-5.72% .. +6.8%] · haut q95 +8.27% · bas q05 -6.74%
   - 2h (n=158) : retour [-6.93% .. +6.73%] · haut q95 +11.9% · bas q05 -7.8%
   - 4h (n=158) : retour [-7.23% .. +9.58%] · haut q95 +12.47% · bas q05 -8.59%
   - 6h (n=158) : retour [-8.73% .. +10.2%] · haut q95 +13.59% · bas q05 -9.46%
   - session (n=158) : retour [-12.24% .. +12.71%] · haut q95 +14.62% · bas q05 -12.96%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.3% des séances sont trend-up (mild 0% / strong 6.3%) · base = 10 séances trend-up (n_eff 5.8)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **23%**. Lecture précoce 30 min : signature présente → 10% vs absente 4% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.06% (p75 1.5% / p90 2.89%) · ~5.05 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **89%** (reprise méd 20.0 min, n=60)
   - −1.0% → **82%** (reprise méd 34.22 min, n=34)
   - −1.5% → **69%** (reprise méd 46.1 min, n=18)
   - −2.0% → **87%** (reprise méd 49.44 min, n=15)
   - −3.0% → **100%** (reprise méd 61.76 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.89%** (p90, défaut prudent ; serré/agressif −1.5%) ; extension open→close méd +7.26% (q75 +13.51% / q95 +17.04%), MFE méd +8.03% / q90 +18.1%
   - Échelle scale-out : +8.03% (33%) / +14.35% (33%) / +18.1% (34%)
- **DÉSARMER** : repli > **−2.89%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +18.1% : P(retournement après) 0% (mèche méd 1.42%)
- **CONTEXTE** : la dernière heure tient les gains 96% du temps (retour médian dernière heure +1.92%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 53.8  _(neutre)_
- **ADX** : 18.8  _(pas de tendance nette)_
- **MACD** : hist -0.716  _(bearish_recent)_
- **BB** : %B 0.33 · largeur 36.8%
- **ATR** : 8.07 (65.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.163  _(distribution)_
- **Vol ratio** : 0.29  _(volume atone)_
- **Choppiness** : 45.2  _(transition)_
- **MA** : MA20 116.68 · MA50 113.17 · MA200 76.29  _(prix < MA20)_
- **Dist MA** : MA20 -6.1% · MA50 -3.2% · MA200 +43.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (609105 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
