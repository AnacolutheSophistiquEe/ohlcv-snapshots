# HOOD

**Generated** : 2026-09-29T00:45:52.578970+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $116.50  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $116.50 (+2.0% vs entrée) · entrée $114.23 · stop $108.31 · T1 $122.28 · R/R 1.36  
> ↳ P(T1 av. stop) 38 % _(réel 5 s)_ · EV/risk 0.017 _(réel 5 s)_ (GBM 0.005) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -2.9 % ≠ (strike 116.0 − spot 116.50)/spot = -0.4 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $112.88–$115.57 (mid $114.23)
- Spot actuel : $116.50 (+2.0% au-dessus de la zone — repli à attendre)
- Stop : $108.31 (plancher anti-bruit (R/R<2) ; -5.18 % depuis l'entree)
- Targets : T1 $122.28 · R/R 1.36 | T2 $128.32 · R/R 2.38 | T3 $134.36 · R/R 3.4
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $108.31


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.02 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.04 %)** : le gap seul le franchit 1.038 % des séances (13 fois sur 1253).
   - exécution **2.95 pt plus bas** dans le cas TYPIQUE (médiane), 6.641 au p90, **10.745 au pire**
   - perte réelle **10.494 %** en moyenne _(tirée par la queue)_, jusqu'à **17.785 %** — au lieu des 7.04 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0358 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 13 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.416 % | p01 -7.308 % | pire -17.785 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3933** [0.3228 ; 0.4673] _(largeur 14.5 pt, n_eff 173.1)_
   - swing : **0.5095** [0.4569 ; 0.5619] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4598** [0.4078 ; 0.5125] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.7 pt), swing (35.1 pt), deep (35.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-6.16 %** | CVaR **-8.88 %** | vol 4.37 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 2.78 % contre 4.71 % aujourd'hui, rapport 0.59)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.55 % vs -14.36 % si l'on extrapolait par √5 _(rapport 1.013 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7744** (β de hausse 1.6058, asymétrie 1.105) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.406× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 112.0645 sur atr_grid (0.75 ATR, 3.811 %) — p(stop avant cible) 0.7125 [0.66 ; 0.76], R/R 4.55, perte reelle 6.392 % (gap inclus), CVaR 3.912 %, EV -0.6965 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.3787 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 3.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.713, borne haute 0.758 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **4.41 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.18 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 47.6 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 1.03 ATR (stop 7.569 %) — p(stop avant cible) 0.501 [0.45 ; 0.55], R/R 2.771, perte reelle 10.494 % (gap inclus), EV 0.1283 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.501, borne haute 0.553 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 7.60 % > budget 4.41 %
      - ⚠ support DETECTE a 0.70 ATR du spot — compartiment <1, mesure a 47.5 % de casse (IC clusterise [0.441 ; 0.507] sur 1150 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 2.67 ATR (stop 15.921 %) — p(stop avant cible) 0.1726 [0.14 ; 0.22], R/R 1.635, perte reelle 17.785 % (gap inclus), EV 2.3786 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.92 % > budget 4.41 %
   - 🟢 support a 4.23 ATR (stop 23.852 %) — p(stop avant cible) 0.0363 [0.02 ; 0.06], R/R 1.219, perte reelle 23.852 % (gap inclus), EV 2.9348 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.85 % > budget 4.41 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.27 %) — p(stop avant cible) 0.9129 [0.88 ; 0.94], R/R 9.899, perte reelle 2.938 % (gap inclus), EV -1.3397 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 9.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.913, borne haute 0.939 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 5.77 % > budget 4.41 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.34 %) : P(cible) 1.5 % x 29.08 % + P(rien) 7.2 % x 12.66 % ne couvrent pas P(stop) 91.3 % x 2.94 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 2.541 %) — p(stop avant cible) 0.803 [0.76 ; 0.84], R/R 6.53, perte reelle 4.454 % (gap inclus), EV -0.7556 % — **REFUSE**
      - refuse : cible atteinte seulement 2.9 % du temps (< 15 %) meme a 10 seances : le R/R de 6.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.803, borne haute 0.842 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 5.77 % > budget 4.41 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.76 %) : P(cible) 2.9 % x 29.08 % + P(rien) 16.8 % x 11.81 % ne couvrent pas P(stop) 80.3 % x 4.45 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 3.811 %) — p(stop avant cible) 0.7125 [0.66 ; 0.76], R/R 4.55, perte reelle 6.392 % (gap inclus), EV -0.6965 % — **REFUSE**
      - refuse : cible atteinte seulement 3.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.713, borne haute 0.758 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.70 %) : P(cible) 3.5 % x 29.08 % + P(rien) 25.2 % x 11.24 % ne couvrent pas P(stop) 71.2 % x 6.39 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 grid_snapped a 1.03 ATR (stop 6.756 %) — p(stop avant cible) 0.5527 [0.50 ; 0.60], R/R 2.841, perte reelle 10.236 % (gap inclus), EV -0.4478 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.553, borne haute 0.605 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 6.79 % > budget 4.41 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.45 %) : P(cible) 5.3 % x 29.08 % + P(rien) 39.5 % x 9.32 % ne couvrent pas P(stop) 55.3 % x 10.24 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 8.893 %) — p(stop avant cible) 0.4253 [0.37 ; 0.48], R/R 2.508, perte reelle 11.595 % (gap inclus), EV 0.9468 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 8.91 % > budget 4.41 %
   - ⚪ atr_grid a 2.0 ATR (stop 10.164 %) — p(stop avant cible) 0.3641 [0.31 ; 0.42], R/R 2.288, perte reelle 12.711 % (gap inclus), EV 1.3666 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 10.18 % > budget 4.41 %
   - ⚪ atr_grid a 2.25 ATR (stop 11.434 %) — p(stop avant cible) 0.3049 [0.26 ; 0.35], R/R 1.991, perte reelle 14.605 % (gap inclus), EV 1.5514 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 11.44 % > budget 4.41 %
   - 🟢 grid_snapped a 2.67 ATR (stop 15.108 %) — p(stop avant cible) 0.2024 [0.16 ; 0.25], R/R 1.635, perte reelle 17.785 % (gap inclus), EV 2.0346 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.11 % > budget 4.41 %
   - ⚪ atr_grid a 3.5 ATR (stop 17.787 %) — p(stop avant cible) 0.1231 [0.09 ; 0.16], R/R 1.635, perte reelle 17.787 % (gap inclus), EV 2.7734 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.79 % > budget 4.41 %
   - 🟢 grid_snapped a 4.23 ATR (stop 23.039 %) — p(stop avant cible) 0.0498 [0.03 ; 0.08], R/R 1.262, perte reelle 23.039 % (gap inclus), EV 2.8742 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.04 % > budget 4.41 %
   - ⚪ atr_grid a 5.0 ATR (stop 25.41 %) — p(stop avant cible) 0.0336 [0.02 ; 0.06], R/R 1.145, perte reelle 25.41 % (gap inclus), EV 2.8948 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.41 % > budget 4.41 %
   - ⚪ atr_grid a 5.5 ATR (stop 27.951 %) — p(stop avant cible) 0.0246 [0.01 ; 0.05], R/R 1.041, perte reelle 27.951 % (gap inclus), EV 2.9065 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.95 % > budget 4.41 %
   - ⚪ atr_grid a 6.0 ATR (stop 30.492 %) — p(stop avant cible) 0.022 [0.01 ; 0.04], R/R 0.954, perte reelle 30.492 % (gap inclus), EV 2.8882 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.49 % > budget 4.41 %
   - ⚪ atr_grid a 6.5 ATR (stop 33.033 %) — p(stop avant cible) 0.0062 [0.00 ; 0.02], R/R 0.88, perte reelle 33.033 % (gap inclus), EV 2.9813 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.03 % > budget 4.41 %
   - ⚪ atr_grid a 7.0 ATR (stop 35.574 %) — p(stop avant cible) 0.0025 [0.00 ; 0.01], R/R 0.818, perte reelle 35.574 % (gap inclus), EV 3.0299 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.57 % > budget 4.41 %
   - ⚪ atr_grid a 7.5 ATR (stop 38.115 %) — p(stop avant cible) 0.0019 [0.00 ; 0.01], R/R 0.763, perte reelle 38.115 % (gap inclus), EV 3.0287 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.12 % > budget 4.41 %
   - ⚪ atr_grid a 8.0 ATR (stop 40.656 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.715, perte reelle 40.656 % (gap inclus), EV 3.0488 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.66 % > budget 4.41 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 116.505, ATR14 5.9207 (5.082 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.374 ATR = 1.901 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.254 % | 116.209 | 93.05 % | 95.16 % | 96.06 % | 96.56 % | 97.05 % | 98.05 % |
| 0.1 ATR | 0.508 % | 115.9129 | 85.5 % | 90.52 % | 92.23 % | 93.73 % | 94.72 % | 96.41 % |
| 0.15 ATR | 0.762 % | 115.6169 | 77.54 % | 85.18 % | 87.99 % | 90.29 % | 92.58 % | 95.07 % |
| 0.2 ATR | 1.016 % | 115.3209 | 71.5 % | 80.14 % | 83.75 % | 86.96 % | 90.35 % | 93.22 % |
| 0.25 ATR | 1.27 % | 115.0248 | 64.65 % | 74.5 % | 79.21 % | 83.42 % | 87.7 % | 90.86 % |
| 0.35 ATR | 1.779 % | 114.4327 | 52.47 % | 65.32 % | 71.95 % | 77.55 % | 83.43 % | 87.99 % |
| 0.5 ATR | 2.541 % | 113.5446 | 37.26 % | 53.43 % | 61.15 % | 68.25 % | 76.52 % | 82.34 % |
| 0.75 ATR | 3.811 % | 112.0645 | 19.64 % | 36.09 % | 45.81 % | 55.51 % | 65.65 % | 73.2 % |
| 1.0 ATR | 5.082 % | 110.5843 | 9.26 % | 22.98 % | 32.59 % | 43.68 % | 54.98 % | 65.61 % |
| 1.25 ATR | 6.352 % | 109.1041 | 4.83 % | 14.52 % | 22.3 % | 33.37 % | 46.95 % | 59.03 % |
| 1.5 ATR | 7.623 % | 107.6239 | 2.42 % | 9.78 % | 16.15 % | 26.9 % | 40.04 % | 53.29 % |
| 2.0 ATR | 10.164 % | 104.6636 | 0.5 % | 3.83 % | 7.27 % | 15.37 % | 29.57 % | 43.84 % |
| 2.5 ATR | 12.705 % | 101.7032 | 0.1 % | 1.51 % | 3.83 % | 8.19 % | 21.44 % | 34.6 % |
| 3.0 ATR | 15.246 % | 98.7428 | 0.0 % | 0.71 % | 2.32 % | 5.26 % | 15.45 % | 26.59 % |
| 4.0 ATR | 20.328 % | 92.8221 | 0.0 % | 0.4 % | 0.91 % | 2.22 % | 6.91 % | 14.89 % |
| 6.0 ATR | 30.492 % | 80.9807 | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.32 % | 4.62 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.37 ATR | 0.42 ATR | 0.56 ATR | 0.67 ATR | 0.74 ATR | 0.98 ATR | 1.24 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.62 ATR | 0.81 ATR | 0.96 ATR | 1.09 ATR | 1.49 ATR | 1.90 ATR |
| **3 s.** | 0.31 ATR | 0.68 ATR | 0.77 ATR | 0.99 ATR | 1.18 ATR | 1.34 ATR | 1.85 ATR | 2.33 ATR |
| **5 s.** | 0.39 ATR | 0.87 ATR | 0.97 ATR | 1.26 ATR | 1.58 ATR | 1.80 ATR | 2.37 ATR | 3.09 ATR |
| **10 s.** | 0.54 ATR | 1.16 ATR | 1.32 ATR | 1.84 ATR | 2.28 ATR | 2.62 ATR | 3.64 ATR | 4.68 ATR |
| **20 s.** | 0.70 ATR | 1.67 ATR | 1.94 ATR | 2.60 ATR | 3.14 ATR | 3.56 ATR | 4.95 ATR | 5.93 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.424–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.622–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.811 %, prix 112.065), p(touche) 36.09 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.765–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.082 %, prix 110.5842), p(touche) 32.59 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (61.1 % des re-echantillons)
- **5 seance(s)** : plage utile 0.972–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.082 %, prix 110.5842), p(touche) 43.68 % (en stress 98.99 %)  ✅ optimum identifie (61.8 % des re-echantillons)
- **10 seance(s)** : plage utile 1.321–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.623 %, prix 107.6238), p(touche) 40.04 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.939–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (10.164 %, prix 104.6634), p(touche) 43.84 % (en stress 97.96 %)  ✅ optimum identifie (65.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.005 | EV/share : $0.032 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 20 % | T3 13 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 62.9 | bear 26.5 | side 10.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 466.0 (= 4 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.889% → cible +5.409% / stop −2.705%, p_fill 73%, n_eff≈31.7) : P(cible|rempli) **7%** · **EV/risk -0.024** (×p_fill ; si rempli -0.09% du capital)
  - **swing** (entrée dip −1.958% → cible +7.051% / stop −5.183%, p_fill 73%, n_eff≈28.6) : P(cible|rempli) **38%** · **EV/risk +0.017** (×p_fill ; si rempli +0.12% du capital)
  - **deep** (entrée dip −3.017% → cible +8.307% / stop −7.86%, p_fill 62%, n_eff≈26.6) : P(cible|rempli) **63%** · **EV/risk +0.221** (×p_fill ; si rempli +2.78% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→84% · +2.0%→57% · +3.0%→38% · +5.0%→22% · +8.0%→10%
- Range intraday médian 5.24% (p90 9.08%) · excursion haute méd. +2.18% / basse méd. −2.24%
- Profil de vol intra : ouverture 3.95% vs midi 1.007% vs clôture 1.167% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 19% · trend ↑0%/↓0% ; spike-down 68% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.127 ; neutre — autocorr -0.028)_ ; drift intra méd. 0.571% ; recovery-V 34%
- **σ réalisé intraday** 3.51% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 42% / whipsaw 8%
- POC intraday (dernière séance, temps-au-prix) : 123.065 (VA 122.039–123.635 ; dernier close 122.07)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 40% · rebond 80% · **stop −3.83%** sous le fill (sous le bruit) · cible +2.2% · R/R 0.57 (high win-rate)
- Gaps overnight (n=159) : méd. 0.01% · baisse 50% (gap-down >1% 32% · >2% 15%)
- Excursion ouverture 5min (n=160) : bas méd −0.94% (p90 −2.68%) · haut méd +1.04% · range méd 2.28%
- Excursion ouverture 15min (n=160) : bas méd −1.3% (p90 −3.52%) · haut méd +1.41% · range méd 2.91%
- Excursion ouverture 30min (n=160) : bas méd −1.38% (p90 −3.84%) · haut méd +1.64% · range méd 3.42%
- Excursion ouverture 60min (n=160) : bas méd −1.84% (p90 −3.9%) · haut méd +1.69% · range méd 3.9%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 122.11 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 80% (124/159) · gap 42% · délai 0.0min · rebond 61% (68/124) (MFE +1.5%)
   - −1.0% : fill 30min 61% · séance 69% (110/159) · gap 32% · délai 0.0min · rebond 64% (65/110) (MFE +1.69%)
   - −1.5% : fill 30min 51% · séance 61% (101/159) · gap 24% · délai 0.6min · rebond 65% (59/101) (MFE +1.44%)
   - −2.0% : fill 30min 39% · séance 51% (89/159) · gap 15% · délai 1.5min · rebond 71% (56/89) (MFE +1.45%)
   - −3.0% : fill 30min 28% · séance 40% (69/159) · gap 7% · délai 10.8min · rebond 80% (49/69) (MFE +2.2%)
   - −4.0% : fill 30min 16% · séance 27% (51/159) · gap 3% · délai 11.9min · rebond 72% (34/51) (MFE +2.29%)
   - −5.0% : fill 30min 8% · séance 16% (33/159) · gap 2% · délai 28.3min · rebond 67% (24/33) (MFE +2.22%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.64% (p90 −2.62%) → stop au-delà de −1.74% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.65% (p90 −2.3%) → stop au-delà de −1.8% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.59% (p90 −2.37%) → stop au-delà de −1.77% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=786 jambes) : jambe baissière méd −1.12% (p90 −2.73%) · ~9.7 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (76 séances) :
      · −1.0% : fill 95% (73/76) · rebond 52% (38/73)
      · −2.0% : fill 82% (63/76) · rebond 66% (38/63)
      · −3.0% : fill 72% (54/76) · rebond 79% (38/54)
      · −4.0% : fill 49% (41/76) · rebond 71% (29/41)
      · −5.0% : fill 29% (28/76) · rebond 62% (19/28)
   - **flat** (17 séances) :
      · −1.0% : fill 69% (12/17) · rebond 85% (8/12)
      · −2.0% : fill 33% (9/17) · rebond 61% (6/9)
      · −3.0% : fill 10% (4/17) · rebond 18% (1/4)
      · −4.0% : fill 10% (4/17) · rebond 18% (1/4)
      · −5.0% : fill 4% (2/17) · rebond 100% (2/2)
   - **gap-up** (66 séances) :
      · −1.0% : fill 42% (25/66) · rebond 84% (19/25)
      · −2.0% : fill 23% (17/66) · rebond 92% (12/17)
      · −3.0% : fill 13% (11/66) · rebond 97% (10/11)
      · −4.0% : fill 9% (6/66) · rebond 91% (4/6)
      · −5.0% : fill 4% (3/66) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 67% si les 15 1res min sont vertes (75 cas) · 34% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **21min** → P(séance verte=clôture>ouverture) 70% si début vert vs 27% si rouge (base 49% · écart 43 pts) ; prédictivité sature ensuite (plafond brut 218min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **70%** · continue >prix actuel 53% ; creux résiduel méd -1.6% (q20 -3.49%) → **SL/trailing à −3.49%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.96% / q75 +3.54% → **scale +1.96% / runner +3.54%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **27%** (continue à baisser 58%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.71%** (au-delà de la MAE q10 -3.71%), cible rebond +1.67% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.1% .. +4.84%] · haut q95 +5.45% · bas q05 -4.99%
   - 60min (n=160) : retour [-3.67% .. +5.05%] · haut q95 +6.42% · bas q05 -5.48%
   - 2h (n=160) : retour [-4.69% .. +6.51%] · haut q95 +7.7% · bas q05 -5.97%
   - 4h (n=160) : retour [-4.7% .. +7.65%] · haut q95 +8.51% · bas q05 -6.61%
   - 6h (n=160) : retour [-5.74% .. +7.98%] · haut q95 +8.8% · bas q05 -7.09%
   - session (n=160) : retour [-5.29% .. +8.24%] · haut q95 +8.88% · bas q05 -7.11%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.7% des séances sont trend-up (mild 0% / strong 8.7%) · base = 14 séances trend-up (n_eff 8.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 22% vs absente 2% (base 9%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.92% (p75 1.5% / p90 2.5%) · ~4.0 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **77%** (reprise méd 20.0 min, n=51)
   - −1.0% → **65%** (reprise méd 38.77 min, n=23)
   - −1.5% → **47%** (reprise méd 41.95 min, n=13)
   - −2.0% → **14%** (reprise méd None min, n=6)
   - −3.0% → **20%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.5%** (p90, défaut prudent ; serré/agressif −1.5%) ; extension open→close méd +6.95% (q75 +9.04% / q95 +12.46%), MFE méd +8.52% / q90 +13.87%
   - Échelle scale-out : +8.52% (33%) / +9.47% (33%) / +13.87% (34%)
- **DÉSARMER** : repli > **−2.5%** depuis le plus-haut = décay → P(retournement) **81%** (préavis méd 286.42 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.87% : P(retournement après) 0% (mèche méd 5.8%)
- **CONTEXTE** : la dernière heure tient les gains 67% du temps (retour médian dernière heure +0.38%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 49.1  _(neutre)_
- **ADX** : 17.7  _(pas de tendance nette)_
- **MACD** : hist -0.081  _(bearish_recent)_
- **BB** : %B 0.54 · largeur 24.0%
- **ATR** : 5.92 (49.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.028  _(neutre)_
- **Vol ratio** : 0.49  _(volume atone)_
- **Choppiness** : 45.4  _(transition)_
- **MA** : MA20 115.32 · MA50 104.58 · MA200 94.53  _(prix > MA20)_
- **Dist MA** : MA20 +1.0% · MA50 +11.4% · MA200 +23.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (860940 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
