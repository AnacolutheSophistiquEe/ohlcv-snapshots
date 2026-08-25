# RGTI

**Generated** : 2026-08-25T00:29:09.127422+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $16.37  

> 🟢 **ARMED** — plan valide, prix dans/proche de la zone d'entrée — exécutable  
> ↳ spot $16.37 (+0.5% vs entrée) · entrée $16.29 · stop $15.95 · T1 $16.86 · R/R 1.68  
> ↳ P(T1 av. stop) 34 % _(réel 5 s)_ · EV/risk 0.034 _(réel 5 s)_ (GBM 0.271) · ¼-Kelly 0.042 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.07% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $16.21–$16.37 (mid $16.29)
- Spot actuel : $16.37 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : $15.95 (stop swing_plan-based (-7.8%))
- Targets : T1 $16.86 · R/R 1.68 | T2 $17.43 · R/R 3.35 | T3 $18.00 · R/R 5.03
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $15.95


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.30 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.8 %)** : le gap seul le franchit 1.277 % des séances (16 fois sur 1253).
   - exécution **3.084 pt plus bas** dans le cas TYPIQUE (médiane), 8.486 au p90, **23.413 au pire**
   - perte réelle **12.728 %** en moyenne _(tirée par la queue)_, jusqu'à **31.213 %** — au lieu des 7.8 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0629 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.085 % | p01 -8.973 % | pire -31.213 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.297** [0.2327 ; 0.368] _(largeur 13.5 pt, n_eff 173.1)_
   - swing : **0.5573** [0.5046 ; 0.609] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.5512** [0.4985 ; 0.603] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.6 pt), swing (31.7 pt), deep (30.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-8.8 %** | CVaR **-10.8 %** | vol 6.87 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 15.79 % contre 6.49 % aujourd'hui, rapport 2.43)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -21.76 % vs -22.11 % si l'on extrapolait par √5 _(rapport 0.984 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8315** (β de hausse 1.9815, asymétrie 0.9243) vs IWM — 602 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.652× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 14.683 sur atr_based (1.5 ATR, 10.305 %) — p(stop avant cible) 0.6236 [0.57 ; 0.67], R/R 1.931, perte reelle 15.002 % (gap inclus), CVaR 10.342 %, EV -3.3262 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.2245 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.624, borne haute 0.673 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 23 des 23 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 51.1 % de la queue et il ne reste que 2.34 EUR a partager. Prix du risque 0.001 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.06 ATR (stop 3.602 %) — p(stop avant cible) 0.8287 [0.79 ; 0.87], R/R 4.411, perte reelle 6.568 % (gap inclus), EV -1.9458 % — **REFUSE**
      - refuse : cible atteinte seulement 9.6 % du temps (< 15 %) meme a 10 seances : le R/R de 4.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.829, borne haute 0.866 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.06 ATR du spot — compartiment <1, mesure a 47.2 % de casse (IC clusterise [0.436 ; 0.506] sur 1081 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.95 %) : P(cible) 9.6 % x 28.97 % + P(rien) 7.5 % x 9.46 % ne couvrent pas P(stop) 82.9 % x 6.57 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 10.305 %) — p(stop avant cible) 0.6236 [0.57 ; 0.67], R/R 1.931, perte reelle 15.002 % (gap inclus), EV -3.3262 % — **REFUSE**
      - refuse : p_stop_first 0.624, borne haute 0.673 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.33 %) : P(cible) 15.7 % x 28.97 % + P(rien) 21.9 % x 6.73 % ne couvrent pas P(stop) 62.4 % x 15.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.69 ATR (stop 14.781 %) — p(stop avant cible) 0.424 [0.37 ; 0.48], R/R 1.179, perte reelle 24.565 % (gap inclus), EV -3.8647 % — **REFUSE**
      - refuse : R/R 1.18 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.80 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.86 %) : P(cible) 17.5 % x 28.97 % + P(rien) 40.1 % x 3.72 % ne couvrent pas P(stop) 42.4 % x 24.57 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 3.08 ATR (stop 24.34 %) — p(stop avant cible) 0.1364 [0.10 ; 0.18], R/R 0.928, perte reelle 31.213 % (gap inclus), EV 0.2876 % — **REFUSE**
      - refuse : R/R 0.93 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.35 % > budget 12.00 %
   - 🟢 support a 3.41 ATR (stop 26.632 %) — p(stop avant cible) 0.0927 [0.07 ; 0.13], R/R 0.928, perte reelle 31.213 % (gap inclus), EV 0.9927 % — **REFUSE**
      - refuse : R/R 0.93 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.64 % > budget 12.00 %
   - ⚪ atr_grid a 1.0 ATR (stop 6.87 %) — p(stop avant cible) 0.7072 [0.66 ; 0.75], R/R 2.529, perte reelle 11.454 % (gap inclus), EV -2.8786 % — **REFUSE**
      - refuse : cible atteinte seulement 14.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.707, borne haute 0.753 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.88 %) : P(cible) 14.1 % x 28.97 % + P(rien) 15.2 % x 7.45 % ne couvrent pas P(stop) 70.7 % x 11.45 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 8.588 %) — p(stop avant cible) 0.6584 [0.61 ; 0.71], R/R 2.166, perte reelle 13.376 % (gap inclus), EV -2.9692 % — **REFUSE**
      - refuse : p_stop_first 0.658, borne haute 0.707 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.97 %) : P(cible) 15.0 % x 28.97 % + P(rien) 19.1 % x 7.76 % ne couvrent pas P(stop) 65.8 % x 13.38 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 17.175 %) — p(stop avant cible) 0.3266 [0.28 ; 0.38], R/R 1.179, perte reelle 24.565 % (gap inclus), EV -1.5934 % — **REFUSE**
      - refuse : R/R 1.18 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.19 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.59 %) : P(cible) 18.9 % x 28.97 % + P(rien) 48.4 % x 1.97 % ne couvrent pas P(stop) 32.7 % x 24.57 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 30.916 %) — p(stop avant cible) 0.0561 [0.04 ; 0.08], R/R 0.928, perte reelle 31.213 % (gap inclus), EV 1.4377 % — **REFUSE**
      - refuse : R/R 0.93 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.92 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 34.351 %) — p(stop avant cible) 0.0303 [0.02 ; 0.05], R/R 0.843, perte reelle 34.351 % (gap inclus), EV 1.5599 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.35 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 37.786 %) — p(stop avant cible) 0.0173 [0.01 ; 0.04], R/R 0.767, perte reelle 37.786 % (gap inclus), EV 1.5744 % — **REFUSE**
      - refuse : R/R 0.77 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.79 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 41.221 %) — p(stop avant cible) 0.0089 [0.00 ; 0.02], R/R 0.703, perte reelle 41.221 % (gap inclus), EV 1.6399 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.22 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 44.656 %) — p(stop avant cible) 0.0059 [0.00 ; 0.02], R/R 0.649, perte reelle 44.656 % (gap inclus), EV 1.6324 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.66 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 48.091 %) — p(stop avant cible) 0.0037 [0.00 ; 0.01], R/R 0.602, perte reelle 48.091 % (gap inclus), EV 1.6262 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 48.09 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 51.526 %) — p(stop avant cible) 0.0036 [0.00 ; 0.01], R/R 0.562, perte reelle 51.526 % (gap inclus), EV 1.614 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 51.53 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 54.961 %) — p(stop avant cible) 0.0029 [0.00 ; 0.01], R/R 0.527, perte reelle 54.961 % (gap inclus), EV 1.6373 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 54.96 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.271 | EV/share : $0.091 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 34 % | T3 34 %
- Kelly (position) : f* 0.166 | ¼-Kelly 0.042 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 19.2 | side 75.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.499% → cible +3.503% / stop −2.071%, p_fill 81%, n_eff≈36.0) : P(cible|rempli) **34%** · **EV/risk +0.034** (×p_fill ; si rempli +0.09% du capital)
  - **swing** (entrée dip −0.93% → cible +7.832% / stop −6.935%, p_fill 83%, n_eff≈35.5) : P(cible|rempli) **44%** · **EV/risk +0.008** (×p_fill ; si rempli +0.07% du capital)
  - **deep** (entrée dip −1.285% → cible +11.077% / stop −10.439%, p_fill 91%, n_eff≈37.7) : P(cible|rempli) **46%** · **EV/risk -0.106** (×p_fill ; si rempli -1.22% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→79% · +2.0%→72% · +3.0%→57% · +5.0%→42% · +8.0%→14%
- Range intraday médian 7.89% (p90 13.36%) · excursion haute méd. +4.06% / basse méd. −2.61%
- Profil de vol intra : ouverture 5.522% vs midi 1.598% vs clôture 1.838% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 22% · trend ↑0%/↓0% ; spike-down 70% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.128 ; neutre — autocorr -0.026)_ ; drift intra méd. 0.515% ; recovery-V 31%
- **σ réalisé intraday** 4.56% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 45% / whipsaw 5%
- POC intraday (dernière séance, temps-au-prix) : 17.6928 (VA 17.3518–17.9911 ; dernier close 17.895)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 44% · rebond 74% · **stop −6.28%** sous le fill (sous le bruit) · cible +2.24% · R/R 0.36 (high win-rate)
- Gaps overnight (n=159) : méd. -0.48% · baisse 58% (gap-down >1% 41% · >2% 28%)
- Excursion ouverture 5min (n=160) : bas méd −1.19% (p90 −2.84%) · haut méd +1.28% · range méd 2.63%
- Excursion ouverture 15min (n=160) : bas méd −1.44% (p90 −3.96%) · haut méd +1.88% · range méd 3.78%
- Excursion ouverture 30min (n=160) : bas méd −1.83% (p90 −4.65%) · haut méd +2.1% · range méd 4.66%
- Excursion ouverture 60min (n=160) : bas méd −2.13% (p90 −5.98%) · haut méd +2.53% · range méd 5.53%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 17.895 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 77% · séance 83% (134/159) · gap 48% · délai 0.0min · rebond 64% (86/134) (MFE +2.42%)
   - −1.0% : fill 30min 68% · séance 75% (126/159) · gap 41% · délai 0.0min · rebond 67% (81/126) (MFE +1.87%)
   - −1.5% : fill 30min 60% · séance 68% (119/159) · gap 35% · délai 0.0min · rebond 67% (78/119) (MFE +2.16%)
   - −2.0% : fill 30min 56% · séance 62% (111/159) · gap 28% · délai 0.0min · rebond 71% (76/111) (MFE +2.37%)
   - −3.0% : fill 30min 48% · séance 56% (98/159) · gap 13% · délai 1.2min · rebond 73% (71/98) (MFE +2.45%)
   - −4.0% : fill 30min 35% · séance 44% (78/159) · gap 5% · délai 6.2min · rebond 74% (57/78) (MFE +2.24%)
   - −5.0% : fill 30min 18% · séance 35% (64/159) · gap 3% · délai 25.1min · rebond 67% (48/64) (MFE +1.8%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.67% (p90 −2.2%) → stop au-delà de −1.53% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.87% (p90 −2.65%) → stop au-delà de −1.98% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.94% (p90 −2.91%) → stop au-delà de −2.04% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1171 jambes) : jambe baissière méd −1.29% (p90 −3.14%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (84 séances) :
      · −1.0% : fill 96% (82/84) · rebond 61% (49/82)
      · −2.0% : fill 85% (77/84) · rebond 70% (52/77)
      · −3.0% : fill 81% (71/84) · rebond 68% (49/71)
      · −4.0% : fill 67% (58/84) · rebond 71% (41/58)
      · −5.0% : fill 54% (49/84) · rebond 65% (37/49)
   - **flat** (16 séances) :
      · −1.0% : fill 96% (15/16) · rebond 95% (13/15)
      · −2.0% : fill 71% (12/16) · rebond 85% (10/12)
      · −3.0% : fill 48% (7/16) · rebond 90% (5/7)
      · −4.0% : fill 32% (6/16) · rebond 85% (4/6)
      · −5.0% : fill 20% (5/16) · rebond 87% (3/5)
   - **gap-up** (59 séances) :
      · −1.0% : fill 41% (29/59) · rebond 66% (19/29)
      · −2.0% : fill 29% (22/59) · rebond 63% (14/22)
      · −3.0% : fill 24% (20/59) · rebond 89% (17/20)
      · −4.0% : fill 15% (14/59) · rebond 84% (12/14)
      · −5.0% : fill 12% (10/59) · rebond 68% (8/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 71% si les 15 1res min sont vertes (80 cas) · 29% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **51min** → P(séance verte=clôture>ouverture) 89% si début vert vs 15% si rouge (base 52% · écart 73 pts) ; prédictivité sature ensuite (plafond brut 91min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **89%** · continue >prix actuel 52% ; creux résiduel méd -2.13% (q20 -3.51%) → **SL/trailing à −3.51%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.53% / q75 +5.77% → **scale +2.53% / runner +5.77%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **15%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.35%** (au-delà de la MAE q10 -5.35%), cible rebond +2.07% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.17% .. +4.96%] · haut q95 +6.49% · bas q05 -6.26%
   - 60min (n=160) : retour [-5.56% .. +6.35%] · haut q95 +6.68% · bas q05 -6.83%
   - 2h (n=160) : retour [-6.39% .. +6.97%] · haut q95 +9.12% · bas q05 -7.59%
   - 4h (n=160) : retour [-7.13% .. +8.07%] · haut q95 +9.21% · bas q05 -7.87%
   - 6h (n=160) : retour [-7.45% .. +8.87%] · haut q95 +10.37% · bas q05 -8.62%
   - session (n=160) : retour [-7.26% .. +9.29%] · haut q95 +10.63% · bas q05 -8.63%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 7.4)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **30%**. Lecture précoce 30 min : signature présente → 14% vs absente 6% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.25% (p75 1.66% / p90 2.45%) · ~4.39 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **82%** (reprise méd 15.0 min, n=47)
   - −1.0% → **83%** (reprise méd 35.0 min, n=29)
   - −1.5% → **84%** (reprise méd 94.96 min, n=17)
   - −2.0% → **86%** (reprise méd 54.27 min, n=9)
   - −3.0% → **67%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.45%** (p90, défaut prudent ; serré/agressif −1.66%) ; extension open→close méd +8.3% (q75 +9.62% / q95 +9.99%), MFE méd +9.65% / q90 +11.14%
   - Échelle scale-out : +9.65% (33%) / +10.43% (33%) / +11.14% (34%)
- **DÉSARMER** : repli > **−2.45%** depuis le plus-haut = décay → P(retournement) **23%** (préavis méd 141.49 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +11.14% : P(retournement après) 0% (mèche méd 1.88%)
- **CONTEXTE** : la dernière heure tient les gains 67% du temps (retour médian dernière heure +0.16%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 44.6  _(momentum baissier)_
- **ADX** : 15.6  _(pas de tendance nette)_
- **MACD** : hist -0.021  _(bearish_recent)_
- **BB** : %B 0.42 · largeur 37.0%
- **ATR** : 1.12 (10.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.019  _(neutre)_
- **Vol ratio** : 1.1  _(volume normal)_
- **Choppiness** : 54.9  _(transition)_
- **MA** : MA20 16.88 · MA50 17.34 · MA200 19.95  _(prix < MA20)_
- **Dist MA** : MA20 -3.0% · MA50 -5.6% · MA200 -18.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (811344 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
