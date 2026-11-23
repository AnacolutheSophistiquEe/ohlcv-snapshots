# SMCI

**Generated** : 2026-11-23T01:23:35.443711+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 5.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 1/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $21.65  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $21.65 (+2.6% vs entrée) · entrée $21.11 · stop $20.36 · T1 $22.35 · R/R 1.65  
> ↳ _probas brutes, non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -87 % hors [0,100] (R² max 0.75). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 1/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-20 : 21.65 · ATR Wilder 2.42 (11.17 %)_
- **Swing** : plage **18.61 → 16.74** (-14.06 % a -22.68 % sous la cloture, 0.77 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 17.25-17.25 (C). stop INDICATIF 14.32 (-14.45 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- **Deep** : plage **16.74 → 10.73** (-22.68 % a -50.43 % sous la cloture, 2.48 ATR) — touchee 43 % → 15 % du temps en 20 seances ; aucun support reel dans la plage. stop INDICATIF 8.31 (-22.54 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 6.1 ATR sous le plus haut 20 s., RSI(2) 2.8. Limite **20.44** (seance suivante), stop catastrophe 10.76, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 18.79-20.2 (A, -6.7 %) ; 17.25-17.25 (C, -20.32 %)
- Resistances reelles au-dessus : 23.38-24.19 (A, 7.99 %) ; 25.13-26.06 (A, 16.07 %) ; 27.22-27.75 (A, 25.73 %) ; 28.5-29.68 (A, 31.66 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.45 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (16.85 %)** : le gap seul le franchit 0.399 % des séances (5 fois sur 1254).
   - exécution **7.807 pt plus bas** dans le cas TYPIQUE (médiane), 11.325 au p90, **12.201 au pire**
   - perte réelle **23.404 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 16.85 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0261 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.991 % | p01 -10.75 % | pire -29.051 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3533** [0.285 ; 0.4265] _(largeur 14.1 pt, n_eff 173.1)_
   - swing : **0.2212** [0.1799 ; 0.2672] _(largeur 8.7 pt, n_eff 345.7)_
   - deep : **0.2269** [0.1851 ; 0.2732] _(largeur 8.8 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : swing (29.3 pt), deep (33.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 900 séances)** : VaR **-8.25 %** | CVaR **-13.23 %** | vol 6.19 %/j
   - _fenêtre arrêtée : rupture de regime a 960 seances en arriere (volatilite 3.86 % contre 6.26 % aujourd'hui, rapport 0.62)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -17.94 % vs -17.06 % si l'on extrapolait par √5 _(rapport 1.052 ; < 1 = le √5 surestime)_
- **β de baisse : 1.5366** (β de hausse 1.1651, asymétrie 1.3188) vs IWM — 605 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.68× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 20.4032 sur atr_grid (0.5 ATR, 5.759 %) — p(stop avant cible) 0.6816 [0.63 ; 0.73], R/R 5.056, perte reelle 6.446 % (gap inclus), CVaR 14.624 %, EV 0.2943 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0215 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 7.8 % du temps (< 15 %) meme a 10 seances : le R/R de 5.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.682, borne haute 0.729 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 14.62 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.87 ATR (stop 14.123 %) — p(stop avant cible) 0.3084 [0.26 ; 0.36], R/R 2.094, perte reelle 15.563 % (gap inclus), EV 0.4414 % — **REFUSE**
      - refuse : cible atteinte seulement 9.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.59 % > budget 12.00 %
      - ⚠ support DETECTE a 0.87 ATR du spot — compartiment <1, mesure a 48.0 % de casse (IC clusterise [0.450 ; 0.511] sur 1225 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_based a 1.5 ATR (stop 17.277 %) — p(stop avant cible) 0.2512 [0.21 ; 0.30], R/R 1.73, perte reelle 18.836 % (gap inclus), EV 0.2405 % — **REFUSE**
      - refuse : cible atteinte seulement 9.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.23 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 2.879 %) — p(stop avant cible) 0.8406 [0.80 ; 0.88], R/R 10.222, perte reelle 3.188 % (gap inclus), EV 0.3193 % — **REFUSE**
      - refuse : cible atteinte seulement 5.6 % du temps (< 15 %) meme a 10 seances : le R/R de 10.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.841, borne haute 0.876 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 5.759 %) — p(stop avant cible) 0.6816 [0.63 ; 0.73], R/R 5.056, perte reelle 6.446 % (gap inclus), EV 0.2943 % — **REFUSE**
      - refuse : cible atteinte seulement 7.8 % du temps (< 15 %) meme a 10 seances : le R/R de 5.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.682, borne haute 0.729 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 14.62 % > budget 12.00 %
   - ⚪ atr_grid a 1.75 ATR (stop 20.156 %) — p(stop avant cible) 0.1897 [0.15 ; 0.23], R/R 1.517, perte reelle 21.482 % (gap inclus), EV 0.2686 % — **REFUSE**
      - refuse : cible atteinte seulement 9.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.93 % > budget 12.00 %
   - ⚪ atr_grid a 2.0 ATR (stop 23.035 %) — p(stop avant cible) 0.1557 [0.12 ; 0.20], R/R 1.359, perte reelle 23.987 % (gap inclus), EV 0.144 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.00 % > budget 12.00 %
   - ⚪ atr_grid a 2.25 ATR (stop 25.915 %) — p(stop avant cible) 0.1078 [0.08 ; 0.14], R/R 1.225, perte reelle 26.613 % (gap inclus), EV 0.1011 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.42 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 28.794 %) — p(stop avant cible) 0.0706 [0.05 ; 0.10], R/R 1.123, perte reelle 29.035 % (gap inclus), EV 0.0828 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.13 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 31.674 %) — p(stop avant cible) 0.0589 [0.04 ; 0.09], R/R 1.024, perte reelle 31.817 % (gap inclus), EV -0.0076 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.84 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.01 %) : P(cible) 9.9 % x 32.59 % + P(rien) 84.2 % x -1.60 % ne couvrent pas P(stop) 5.9 % x 31.82 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 34.553 %) — p(stop avant cible) 0.0515 [0.03 ; 0.08], R/R 0.94, perte reelle 34.69 % (gap inclus), EV -0.1118 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.69 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.11 %) : P(cible) 9.9 % x 32.59 % + P(rien) 85.0 % x -1.81 % ne couvrent pas P(stop) 5.1 % x 34.69 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 40.312 %) — p(stop avant cible) 0.0098 [0.00 ; 0.02], R/R 0.808, perte reelle 40.332 % (gap inclus), EV 0.0465 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.14 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 46.071 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.701, perte reelle 46.463 % (gap inclus), EV 0.0485 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.11 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 51.829 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 0.587, perte reelle 55.543 % (gap inclus), EV 0.0402 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.28 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 57.588 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 0.566, perte reelle 57.588 % (gap inclus), EV 0.0432 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.22 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 63.347 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.515, perte reelle 63.347 % (gap inclus), EV 0.0471 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.12 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 69.106 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.472, perte reelle 69.106 % (gap inclus), EV 0.0471 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.12 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 74.865 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.435, perte reelle 74.865 % (gap inclus), EV 0.0471 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.12 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 80.624 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.404, perte reelle 80.624 % (gap inclus), EV 0.0471 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.12 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 86.382 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.377, perte reelle 86.382 % (gap inclus), EV 0.0471 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.12 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 92.141 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.354, perte reelle 92.141 % (gap inclus), EV 0.0471 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.12 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 21.65, ATR14 2.4936 (11.518 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.35 ATR = 4.031 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.576 % | 21.5253 | 90.95 % | 93.76 % | 95.06 % | 95.66 % | 96.85 % | 97.95 % |
| 0.1 ATR | 1.152 % | 21.4006 | 82.49 % | 87.81 % | 89.62 % | 91.62 % | 93.4 % | 95.28 % |
| 0.15 ATR | 1.728 % | 21.276 | 75.55 % | 82.88 % | 85.58 % | 88.79 % | 91.17 % | 94.05 % |
| 0.2 ATR | 2.304 % | 21.1513 | 68.71 % | 78.15 % | 81.25 % | 86.46 % | 89.75 % | 92.82 % |
| 0.25 ATR | 2.879 % | 21.0266 | 62.47 % | 73.51 % | 77.02 % | 83.13 % | 87.82 % | 91.28 % |
| 0.35 ATR | 4.031 % | 20.7772 | 50.0 % | 64.35 % | 70.56 % | 78.18 % | 83.76 % | 88.92 % |
| 0.5 ATR | 5.759 % | 20.4032 | 34.81 % | 50.45 % | 59.38 % | 69.7 % | 77.97 % | 84.51 % |
| 0.75 ATR | 8.638 % | 19.7798 | 17.51 % | 33.94 % | 44.15 % | 56.46 % | 67.92 % | 76.72 % |
| 1.0 ATR | 11.518 % | 19.1564 | 7.85 % | 21.85 % | 31.05 % | 44.95 % | 58.68 % | 70.15 % |
| 1.25 ATR | 14.397 % | 18.533 | 3.72 % | 15.21 % | 22.88 % | 34.24 % | 49.54 % | 62.56 % |
| 1.5 ATR | 17.276 % | 17.9096 | 1.51 % | 9.97 % | 16.83 % | 26.67 % | 43.15 % | 56.31 % |
| 2.0 ATR | 23.035 % | 16.6629 | 0.3 % | 3.73 % | 8.87 % | 16.87 % | 31.17 % | 45.33 % |
| 2.5 ATR | 28.794 % | 15.4161 | 0.2 % | 1.51 % | 4.44 % | 10.3 % | 21.02 % | 33.64 % |
| 3.0 ATR | 34.553 % | 14.1693 | 0.2 % | 1.21 % | 2.62 % | 5.96 % | 15.03 % | 25.85 % |
| 4.0 ATR | 46.071 % | 11.6757 | 0.0 % | 0.6 % | 1.51 % | 2.83 % | 8.12 % | 16.0 % |
| 6.0 ATR | 69.106 % | 6.6886 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.95 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.64 ATR | 0.71 ATR | 0.94 ATR | 1.17 ATR |
| **2 s.** | 0.23 ATR | 0.51 ATR | 0.58 ATR | 0.77 ATR | 0.94 ATR | 1.07 ATR | 1.50 ATR | 1.90 ATR |
| **3 s.** | 0.28 ATR | 0.65 ATR | 0.74 ATR | 0.96 ATR | 1.19 ATR | 1.37 ATR | 1.93 ATR | 2.44 ATR |
| **5 s.** | 0.41 ATR | 0.89 ATR | 1.00 ATR | 1.29 ATR | 1.58 ATR | 1.84 ATR | 2.54 ATR | 3.31 ATR |
| **10 s.** | 0.57 ATR | 1.24 ATR | 1.43 ATR | 1.92 ATR | 2.30 ATR | 2.58 ATR | 3.73 ATR | 5.03 ATR |
| **20 s.** | 0.81 ATR | 1.79 ATR | 2.01 ATR | 2.54 ATR | 3.09 ATR | 3.59 ATR | 5.19 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.399 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile VIDE (borne basse 0.583 ATR au-dessus du haut de la grille, 0.5 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.736–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (8.638 %, prix 19.7799), p(touche) 44.15 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 18.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.999–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (11.518 %, prix 19.1564), p(touche) 44.95 % (en stress 93.94 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile VIDE (borne basse 1.428 ATR au-dessus du haut de la grille, 1.25 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile VIDE (borne basse 2.014 ATR au-dessus du haut de la grille, 1.5 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 54.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 15.1 | bear 79.9 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.505% → cible +5.907% / stop −3.544%, p_fill 51%, n_eff≈53.7) : P(cible|rempli) **6%** · **EV/risk -0.044** (×p_fill ; si rempli -0.31% du capital)
  - **swing** (entrée dip −5.511% → cible +13.072% / stop −12.0%, p_fill 35%, n_eff≈41.1) : P(cible|rempli) **26%** · **EV/risk -0.044** (×p_fill ; si rempli -1.51% du capital)
  - **deep** (entrée dip −8.524% → cible +27.577% / stop −18.0%, p_fill 27%, n_eff≈32.1) : P(cible|rempli) **14%** · **EV/risk -0.018** (×p_fill ; si rempli -1.21% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→74% · +2.0%→57% · +3.0%→40% · +5.0%→22% · +8.0%→8%
- Range intraday médian 5.72% (p90 9.37%) · excursion haute méd. +2.42% / basse méd. −2.68%
- Profil de vol intra : ouverture 3.884% vs midi 1.151% vs clôture 1.47% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 74% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.14 ; mean-reverting — autocorr -0.077)_ ; drift intra méd. -0.659% ; recovery-V 28%
- **σ réalisé intraday** 3.524% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 60% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 33.7346 (VA 33.3821–34.0871 ; dernier close 32.95)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 29% · rebond 74% · **stop −4.61%** sous le fill (sous le bruit) · cible +2.15% · R/R 0.47 (high win-rate)
- Gaps overnight (n=159) : méd. 0.0% · baisse 50% (gap-down >1% 38% · >2% 23%)
- Excursion ouverture 5min (n=160) : bas méd −1.11% (p90 −2.79%) · haut méd +0.93% · range méd 2.16%
- Excursion ouverture 15min (n=160) : bas méd −1.42% (p90 −3.55%) · haut méd +1.01% · range méd 2.85%
- Excursion ouverture 30min (n=160) : bas méd −1.65% (p90 −3.98%) · haut méd +1.23% · range méd 3.58%
- Excursion ouverture 60min (n=160) : bas méd −1.91% (p90 −4.46%) · haut méd +1.48% · range méd 4.31%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 32.94 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 73% (116/159) · gap 42% · délai 0.0min · rebond 49% (64/116) (MFE +0.98%)
   - −1.0% : fill 30min 58% · séance 70% (109/159) · gap 38% · délai 0.0min · rebond 51% (60/109) (MFE +1.09%)
   - −1.5% : fill 30min 52% · séance 66% (100/159) · gap 28% · délai 0.0min · rebond 56% (62/100) (MFE +1.13%)
   - −2.0% : fill 30min 47% · séance 59% (87/159) · gap 23% · délai 0.1min · rebond 56% (54/87) (MFE +1.2%)
   - −3.0% : fill 30min 34% · séance 48% (73/159) · gap 11% · délai 2.7min · rebond 62% (43/73) (MFE +1.34%)
   - −4.0% : fill 30min 21% · séance 35% (54/159) · gap 5% · délai 12.5min · rebond 72% (36/54) (MFE +1.72%)
   - −5.0% : fill 30min 15% · séance 29% (44/159) · gap 2% · délai 21.5min · rebond 74% (31/44) (MFE +2.15%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.69% (p90 −2.8%) → stop au-delà de −1.93% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.71% (p90 −2.84%) → stop au-delà de −1.86% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.65% (p90 −2.25%) → stop au-delà de −1.73% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=876 jambes) : jambe baissière méd −1.19% (p90 −2.78%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 98% (68/70) · rebond 39% (32/68)
      · −2.0% : fill 96% (64/70) · rebond 57% (37/64)
      · −3.0% : fill 86% (58/70) · rebond 60% (33/58)
      · −4.0% : fill 64% (44/70) · rebond 70% (29/44)
      · −5.0% : fill 53% (36/70) · rebond 71% (24/36)
   - **flat** (14 séances) :
      · −1.0% : fill 90% (13/14) · rebond 84% (10/13)
      · −2.0% : fill 57% (6/14) · rebond 47% (4/6)
      · −3.0% : fill 20% (3/14) · rebond 43% (2/3)
      · −4.0% : fill 7% (1/14) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/14) · rebond 0% (0/0)
   - **gap-up** (75 séances) :
      · −1.0% : fill 36% (28/75) · rebond 66% (18/28)
      · −2.0% : fill 21% (17/75) · rebond 58% (13/17)
      · −3.0% : fill 13% (12/75) · rebond 78% (8/12)
      · −4.0% : fill 11% (9/75) · rebond 81% (6/9)
      · −5.0% : fill 10% (8/75) · rebond 91% (7/8)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 67% si les 15 1res min sont vertes (78 cas) · 24% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:46** → P(séance verte=clôture>ouverture) 83% si début vert vs 11% si rouge (base 43% · écart 72 pts) ; prédictivité sature ensuite (plafond brut 213min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **83%** · continue >prix actuel 59% ; creux résiduel méd -1.33% (q20 -2.94%) → **SL/trailing à −2.94%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.67% / q75 +2.72% → **scale +1.67% / runner +2.72%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **11%** (continue à baisser 55%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.93%** (au-delà de la MAE q10 -3.93%), cible rebond +1.31% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.17% .. +4.1%] · haut q95 +5.04% · bas q05 -5.27%
   - 60min (n=160) : retour [-4.12% .. +4.96%] · haut q95 +6.21% · bas q05 -5.43%
   - 2h (n=160) : retour [-4.55% .. +5.52%] · haut q95 +7.12% · bas q05 -5.93%
   - 4h (n=160) : retour [-4.91% .. +6.39%] · haut q95 +7.24% · bas q05 -6.41%
   - 6h (n=160) : retour [-5.14% .. +6.41%] · haut q95 +7.8% · bas q05 -6.61%
   - session (n=160) : retour [-6.33% .. +6.37%] · haut q95 +7.95% · bas q05 -6.95%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (4) pour des stats fiables : 2.5% des séances seulement sont des jours de hausse propre — SMCI = **volatil sans tendance propre (choppy)** (vol intra méd 3.59%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.53 · part idiosyncratique 0.47
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 27.8  _(survente)_
- **ADX** : 31.1  _(tendance etablie)_
- **MACD** : hist -0.457  _(pas de croisement recent)_
- **BB** : %B 0.05 · largeur 55.7%
- **ATR** : 2.49 (74.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.23  _(distribution)_
- **Vol ratio** : 1.04  _(volume normal)_
- **Choppiness** : 42.8  _(transition)_
- **MA** : MA20 28.9 · MA50 34.99 · MA200 32.37  _(prix < MA20)_
- **Dist MA** : MA20 -25.1% · MA50 -38.1% · MA200 -33.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (681760 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
