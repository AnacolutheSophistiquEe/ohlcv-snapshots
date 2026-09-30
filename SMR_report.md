# SMR

**Generated** : 2026-09-30T00:32:53.811091+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $7.76  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $7.76 (+1.2% vs entrée) · entrée $7.67 · stop $7.44 · T1 $8.04 · R/R 1.61  
> ↳ ¼-Kelly 0.001 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +13.8 % ≠ (strike 9.0 − spot 7.76)/spot = +15.9 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -54 % hors [0,100] (R² max 0.54). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $7.61–$7.72 (mid $7.67)
- Spot actuel : $7.76 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : $7.44 (plancher anti-bruit 5 s — stop EV-optimal −3% (first-passage 5 s réel) ; -3.00 % depuis l'entree)
- Targets : T1 $8.04 · R/R 1.61 | T2 $8.26 · R/R 2.57 | T3 $8.48 · R/R 3.52
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $7.44


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.44 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (11.1 %)** : le gap seul le franchit 0.435 % des séances (5 fois sur 1149).
   - exécution **3.685 pt plus bas** dans le cas TYPIQUE (médiane), 13.987 au p90, **19.223 au pire**
   - perte réelle **17.667 %** en moyenne _(tirée par la queue)_, jusqu'à **30.323 %** — au lieu des 11.1 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0286 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.479 % | p01 -6.959 % | pire -30.323 % _(sur 1149 séances)_
- **P(stop avant cible)** _(source : daily, 1150 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4986** [0.4247 ; 0.5726] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4801** [0.4278 ; 0.5328] _(largeur 10.5 pt, n_eff 345.3)_
   - deep : **0.4415** [0.3898 ; 0.4942] _(largeur 10.4 pt, n_eff 345.3)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-9.52 %** | CVaR **-12.13 %** | vol 6.99 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 10.79 % contre 6.19 % aujourd'hui, rapport 1.74)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -19.17 % vs -18.73 % si l'on extrapolait par √5 _(rapport 1.023 ; < 1 = le √5 surestime)_
- **β de baisse : 1.602** (β de hausse 1.3752, asymétrie 1.165) vs IWM — 548 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.9× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 6.9414 sur support (0.86 ATR, 10.607 %) — p(stop avant cible) 0.567 [0.51 ; 0.62], R/R 1.893, perte reelle 10.712 % (gap inclus), CVaR 11.802 %, EV -1.1162 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.4934 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.567, borne haute 0.619 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 1.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.86 ATR (stop 10.607 %) — p(stop avant cible) 0.567 [0.51 ; 0.62], R/R 1.893, perte reelle 10.712 % (gap inclus), EV -1.1162 % — **REFUSE**
      - refuse : p_stop_first 0.567, borne haute 0.619 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.60 ATR du spot — compartiment <1, mesure a 49.1 % de casse (IC clusterise [0.457 ; 0.522] sur 1123 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.12 %) : P(cible) 23.0 % x 20.28 % + P(rien) 20.3 % x 1.45 % ne couvrent pas P(stop) 56.7 % x 10.71 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 2.079 %) — p(stop avant cible) 0.8987 [0.86 ; 0.93], R/R 9.456, perte reelle 2.145 % (gap inclus), EV -0.1794 % — **REFUSE**
      - refuse : cible atteinte seulement 8.3 % du temps (< 15 %) meme a 10 seances : le R/R de 9.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.899, borne haute 0.927 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.18 %) : P(cible) 8.3 % x 20.28 % + P(rien) 1.8 % x 3.26 % ne couvrent pas P(stop) 89.9 % x 2.14 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 4.158 %) — p(stop avant cible) 0.8272 [0.78 ; 0.86], R/R 4.692, perte reelle 4.322 % (gap inclus), EV -0.7723 % — **REFUSE**
      - refuse : cible atteinte seulement 12.8 % du temps (< 15 %) meme a 10 seances : le R/R de 4.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.827, borne haute 0.864 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.77 %) : P(cible) 12.8 % x 20.28 % + P(rien) 4.5 % x 4.69 % ne couvrent pas P(stop) 82.7 % x 4.32 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.5 ATR (stop 12.474 %) — p(stop avant cible) 0.4937 [0.44 ; 0.55], R/R 1.604, perte reelle 12.647 % (gap inclus), EV -1.0178 % — **REFUSE**
      - refuse : R/R 1.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.17 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.02 %) : P(cible) 24.9 % x 20.28 % + P(rien) 25.8 % x 0.71 % ne couvrent pas P(stop) 49.4 % x 12.65 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 14.552 %) — p(stop avant cible) 0.4298 [0.38 ; 0.48], R/R 1.381, perte reelle 14.689 % (gap inclus), EV -0.9228 % — **REFUSE**
      - refuse : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.73 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.92 %) : P(cible) 25.5 % x 20.28 % + P(rien) 31.5 % x 0.70 % ne couvrent pas P(stop) 43.0 % x 14.69 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 16.631 %) — p(stop avant cible) 0.3451 [0.30 ; 0.40], R/R 1.21, perte reelle 16.76 % (gap inclus), EV -0.9145 % — **REFUSE**
      - refuse : R/R 1.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.52 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.91 %) : P(cible) 26.0 % x 20.28 % + P(rien) 39.5 % x -1.01 % ne couvrent pas P(stop) 34.5 % x 16.76 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 18.71 %) — p(stop avant cible) 0.2761 [0.23 ; 0.33], R/R 1.07, perte reelle 18.963 % (gap inclus), EV -0.9232 % — **REFUSE**
      - refuse : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.11 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.92 %) : P(cible) 26.1 % x 20.28 % + P(rien) 46.3 % x -2.11 % ne couvrent pas P(stop) 27.6 % x 18.96 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 20.789 %) — p(stop avant cible) 0.2151 [0.17 ; 0.26], R/R 0.966, perte reelle 20.987 % (gap inclus), EV -0.8551 % — **REFUSE**
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.64 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.86 %) : P(cible) 26.1 % x 20.28 % + P(rien) 52.3 % x -3.14 % ne couvrent pas P(stop) 21.5 % x 20.99 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 22.868 %) — p(stop avant cible) 0.1654 [0.13 ; 0.21], R/R 0.877, perte reelle 23.12 % (gap inclus), EV -0.7491 % — **REFUSE**
      - refuse : R/R 0.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.70 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.75 %) : P(cible) 26.1 % x 20.28 % + P(rien) 57.3 % x -3.88 % ne couvrent pas P(stop) 16.5 % x 23.12 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 24.947 %) — p(stop avant cible) 0.1281 [0.10 ; 0.17], R/R 0.804, perte reelle 25.219 % (gap inclus), EV -0.7324 % — **REFUSE**
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.64 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.73 %) : P(cible) 26.2 % x 20.28 % + P(rien) 61.0 % x -4.60 % ne couvrent pas P(stop) 12.8 % x 25.22 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 29.105 %) — p(stop avant cible) 0.0649 [0.04 ; 0.09], R/R 0.687, perte reelle 29.529 % (gap inclus), EV -0.5478 % — **REFUSE**
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.66 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.55 %) : P(cible) 26.2 % x 20.28 % + P(rien) 67.3 % x -5.85 % ne couvrent pas P(stop) 6.5 % x 29.53 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 33.263 %) — p(stop avant cible) 0.0348 [0.02 ; 0.06], R/R 0.608, perte reelle 33.353 % (gap inclus), EV -0.481 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.79 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.48 %) : P(cible) 26.2 % x 20.28 % + P(rien) 70.3 % x -6.59 % ne couvrent pas P(stop) 3.5 % x 33.35 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 37.421 %) — p(stop avant cible) 0.0209 [0.01 ; 0.04], R/R 0.542, perte reelle 37.445 % (gap inclus), EV -0.4957 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.72 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.50 %) : P(cible) 26.2 % x 20.28 % + P(rien) 71.7 % x -7.01 % ne couvrent pas P(stop) 2.1 % x 37.45 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 41.579 %) — p(stop avant cible) 0.0143 [0.01 ; 0.03], R/R 0.486, perte reelle 41.701 % (gap inclus), EV -0.5196 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.26 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.52 %) : P(cible) 26.2 % x 20.28 % + P(rien) 72.4 % x -7.23 % ne couvrent pas P(stop) 1.4 % x 41.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 45.736 %) — p(stop avant cible) 0.0092 [0.00 ; 0.02], R/R 0.443, perte reelle 45.736 % (gap inclus), EV -0.5099 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.23 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.51 %) : P(cible) 26.2 % x 20.28 % + P(rien) 72.9 % x -7.41 % ne couvrent pas P(stop) 0.9 % x 45.74 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 49.894 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.407, perte reelle 49.894 % (gap inclus), EV -0.5053 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.14 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.51 %) : P(cible) 26.2 % x 20.28 % + P(rien) 73.6 % x -7.78 % ne couvrent pas P(stop) 0.2 % x 49.89 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 54.052 %) — p(stop avant cible) 0.0002 [0.00 ; 0.01], R/R 0.375, perte reelle 54.052 % (gap inclus), EV -0.5073 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.12 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.51 %) : P(cible) 26.2 % x 20.28 % + P(rien) 73.8 % x -7.87 % ne couvrent pas P(stop) 0.0 % x 54.05 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 58.21 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.348, perte reelle 58.21 % (gap inclus), EV -0.5015 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.06 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.50 %) : P(cible) 26.2 % x 20.28 % + P(rien) 73.8 % x -7.88 % ne couvrent pas P(stop) 0.0 % x 58.21 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 62.368 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.325, perte reelle 62.368 % (gap inclus), EV -0.5015 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.06 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.50 %) : P(cible) 26.2 % x 20.28 % + P(rien) 73.8 % x -7.88 % ne couvrent pas P(stop) 0.0 % x 62.37 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 66.526 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.305, perte reelle 66.526 % (gap inclus), EV -0.5015 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.06 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.50 %) : P(cible) 26.2 % x 20.28 % + P(rien) 73.8 % x -7.88 % ne couvrent pas P(stop) 0.0 % x 66.53 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 7.765, ATR14 0.6457 (8.316 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.426 ATR = 3.542 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.416 % | 7.7327 | 92.46 % | 95.05 % | 96.28 % | 97.06 % | 97.95 % | 98.39 % |
| 0.1 ATR | 0.832 % | 7.7004 | 86.73 % | 91.22 % | 93.24 % | 94.69 % | 96.25 % | 97.47 % |
| 0.15 ATR | 1.247 % | 7.6681 | 80.76 % | 86.94 % | 89.63 % | 91.75 % | 93.98 % | 96.09 % |
| 0.2 ATR | 1.663 % | 7.6359 | 75.03 % | 82.66 % | 86.36 % | 89.27 % | 92.39 % | 95.06 % |
| 0.25 ATR | 2.079 % | 7.6036 | 69.85 % | 79.62 % | 83.77 % | 87.12 % | 90.68 % | 93.91 % |
| 0.35 ATR | 2.91 % | 7.539 | 58.16 % | 72.07 % | 77.34 % | 82.71 % | 87.61 % | 91.49 % |
| 0.5 ATR | 4.158 % | 7.4421 | 41.96 % | 58.78 % | 66.97 % | 74.01 % | 83.18 % | 88.51 % |
| 0.75 ATR | 6.237 % | 7.2807 | 20.58 % | 37.27 % | 47.58 % | 59.55 % | 72.27 % | 81.03 % |
| 1.0 ATR | 8.316 % | 7.1193 | 11.36 % | 25.79 % | 35.74 % | 49.27 % | 64.43 % | 75.17 % |
| 1.25 ATR | 10.395 % | 6.9579 | 4.72 % | 15.99 % | 25.03 % | 38.42 % | 54.89 % | 68.74 % |
| 1.5 ATR | 12.474 % | 6.7964 | 2.25 % | 9.8 % | 16.23 % | 28.36 % | 45.45 % | 61.95 % |
| 2.0 ATR | 16.631 % | 6.4736 | 0.34 % | 3.27 % | 6.54 % | 14.69 % | 31.36 % | 48.85 % |
| 2.5 ATR | 20.789 % | 6.1507 | 0.11 % | 1.35 % | 2.93 % | 6.89 % | 20.68 % | 38.05 % |
| 3.0 ATR | 24.947 % | 5.8279 | 0.11 % | 0.56 % | 1.92 % | 3.84 % | 11.82 % | 28.16 % |
| 4.0 ATR | 33.263 % | 5.1821 | 0.0 % | 0.23 % | 0.34 % | 1.13 % | 4.55 % | 13.56 % |
| 6.0 ATR | 49.894 % | 3.8907 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.34 % | 1.61 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.43 ATR | 0.47 ATR | 0.60 ATR | 0.70 ATR | 0.77 ATR | 1.05 ATR | 1.24 ATR |
| **2 s.** | 0.31 ATR | 0.60 ATR | 0.66 ATR | 0.84 ATR | 1.02 ATR | 1.15 ATR | 1.49 ATR | 1.87 ATR |
| **3 s.** | 0.38 ATR | 0.72 ATR | 0.80 ATR | 1.06 ATR | 1.25 ATR | 1.39 ATR | 1.82 ATR | 2.21 ATR |
| **5 s.** | 0.48 ATR | 0.98 ATR | 1.10 ATR | 1.39 ATR | 1.62 ATR | 1.81 ATR | 2.30 ATR | 2.81 ATR |
| **10 s.** | 0.69 ATR | 1.38 ATR | 1.52 ATR | 1.94 ATR | 2.30 ATR | 2.54 ATR | 3.25 ATR | 3.94 ATR |
| **20 s.** | 1.01 ATR | 1.96 ATR | 2.18 ATR | 2.75 ATR | 3.22 ATR | 3.56 ATR | 4.60 ATR | 5.43 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.472–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (4.158 %, prix 7.4421), p(touche) 41.96 % (en stress 82.02 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.66–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (6.237 %, prix 7.2807), p(touche) 37.27 % (en stress 88.76 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (69.4 % des re-echantillons)
- **3 seance(s)** : plage utile 0.804–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (8.316 %, prix 7.1193), p(touche) 35.74 % (en stress 89.89 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.098–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (10.395 %, prix 6.9578), p(touche) 38.42 % (en stress 95.51 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.516–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (16.631 %, prix 6.4736), p(touche) 31.36 % (en stress 96.59 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.178–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.003 | EV/share : $0.001 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 29 % | T2 — | T3 —
- Kelly (position) : f* 0.005 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 34.1 | bear 53.8 | side 12.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.258% → cible +4.923% / stop −3.0%, p_fill 79%, n_eff≈84.3) : P(cible|rempli) **24%** · **EV/risk -0.025** (×p_fill ; si rempli -0.10% du capital)
  - **swing** (entrée dip −2.757% → cible +17.158% / stop −8.58%, p_fill 73%, n_eff≈85.3) : P(cible|rempli) **10%** · **EV/risk -0.050** (×p_fill ; si rempli -0.58% du capital)
  - **deep** (entrée dip −4.27% → cible +28.203% / stop −14.102%, p_fill 74%, n_eff≈83.9) : P(cible|rempli) **8%** · **EV/risk -0.101** (×p_fill ; si rempli -1.94% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→80% · +2.0%→66% · +3.0%→56% · +5.0%→31% · +8.0%→12%
- Range intraday médian 6.97% (p90 11.85%) · excursion haute méd. +3.23% / basse méd. −3.11%
- Profil de vol intra : ouverture 4.614% vs midi 1.472% vs clôture 1.716% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 77% · recovery-V 41%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; mean-reverting — autocorr -0.073)_ ; drift intra méd. 0.422% ; recovery-V 48%
- **σ réalisé intraday** 4.319% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 60% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 9.4737 (VA 9.4479–9.5856 ; dernier close 9.695)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 40% · rebond 75% · **stop −3.97%** sous le fill (sous le bruit) · cible +2.48% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. -0.56% · baisse 58% (gap-down >1% 36% · >2% 22%)
- Excursion ouverture 5min (n=160) : bas méd −1.01% (p90 −3.01%) · haut méd +1.22% · range méd 2.65%
- Excursion ouverture 15min (n=160) : bas méd −1.3% (p90 −3.81%) · haut méd +1.74% · range méd 3.49%
- Excursion ouverture 30min (n=160) : bas méd −1.59% (p90 −4.63%) · haut méd +2.22% · range méd 4.13%
- Excursion ouverture 60min (n=160) : bas méd −2.1% (p90 −5.45%) · haut méd +2.56% · range méd 4.9%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 9.7 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 79% (129/159) · gap 51% · délai 0.0min · rebond 63% (79/129) (MFE +1.63%)
   - −1.0% : fill 30min 63% · séance 74% (121/159) · gap 36% · délai 0.0min · rebond 63% (74/121) (MFE +1.99%)
   - −1.5% : fill 30min 59% · séance 70% (115/159) · gap 27% · délai 0.0min · rebond 70% (81/115) (MFE +1.95%)
   - −2.0% : fill 30min 51% · séance 63% (107/159) · gap 22% · délai 0.9min · rebond 67% (73/107) (MFE +1.98%)
   - −3.0% : fill 30min 39% · séance 53% (94/159) · gap 10% · délai 4.7min · rebond 76% (75/94) (MFE +2.27%)
   - −4.0% : fill 30min 31% · séance 47% (83/159) · gap 3% · délai 9.1min · rebond 75% (63/83) (MFE +2.42%)
   - −5.0% : fill 30min 23% · séance 40% (67/159) · gap 1% · délai 23.2min · rebond 75% (50/67) (MFE +2.48%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.7% (p90 −2.66%) → stop au-delà de −1.96% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.71% (p90 −2.69%) → stop au-delà de −2.06% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.05% (p90 −2.79%) → stop au-delà de −2.16% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1136 jambes) : jambe baissière méd −1.33% (p90 −3.1%) · ~13.1 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (87 séances) :
      · −1.0% : fill 95% (84/87) · rebond 62% (51/84)
      · −2.0% : fill 86% (79/87) · rebond 73% (58/79)
      · −3.0% : fill 79% (74/87) · rebond 82% (62/74)
      · −4.0% : fill 69% (66/87) · rebond 81% (53/66)
      · −5.0% : fill 59% (52/87) · rebond 82% (42/52)
   - **flat** (10 séances) :
      · −1.0% : fill 92% (8/10) · rebond 47% (4/8)
      · −2.0% : fill 79% (6/10) · rebond 39% (2/6)
      · −3.0% : fill 79% (6/10) · rebond 50% (3/6)
      · −4.0% : fill 79% (6/10) · rebond 62% (4/6)
      · −5.0% : fill 59% (4/10) · rebond 78% (3/4)
   - **gap-up** (62 séances) :
      · −1.0% : fill 43% (29/62) · rebond 73% (19/29)
      · −2.0% : fill 28% (22/62) · rebond 52% (13/22)
      · −3.0% : fill 14% (14/62) · rebond 52% (10/14)
      · −4.0% : fill 12% (11/62) · rebond 36% (6/11)
      · −5.0% : fill 12% (11/62) · rebond 28% (5/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 66% si les 15 1res min sont vertes (74 cas) · 37% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:15** → P(séance verte=clôture>ouverture) 85% si début vert vs 20% si rouge (base 51% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 197min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **85%** · continue >prix actuel 59% ; creux résiduel méd -1.65% (q20 -3.23%) → **SL/trailing à −3.23%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.12% / q75 +4.06% → **scale +3.12% / runner +4.06%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **20%** (continue à baisser 55%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.4%** (au-delà de la MAE q10 -5.4%), cible rebond +1.43% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.06% .. +4.37%] · haut q95 +6.15% · bas q05 -5.73%
   - 60min (n=160) : retour [-5.13% .. +4.76%] · haut q95 +6.49% · bas q05 -6.27%
   - 2h (n=160) : retour [-6.23% .. +5.39%] · haut q95 +7.8% · bas q05 -7.93%
   - 4h (n=160) : retour [-7.16% .. +6.95%] · haut q95 +8.12% · bas q05 -8.18%
   - 6h (n=160) : retour [-6.98% .. +8.06%] · haut q95 +9.69% · bas q05 -8.86%
   - session (n=160) : retour [-6.99% .. +8.31%] · haut q95 +10.38% · bas q05 -8.81%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 4.84%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.36 · part idiosyncratique 0.64
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 23.6  _(survente)_
- **ADX** : 14.3  _(pas de tendance nette)_
- **MACD** : hist -0.134  _(pas de croisement recent)_
- **BB** : %B 0.16 · largeur 40.8%
- **ATR** : 0.65 (4.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.185  _(distribution)_
- **Vol ratio** : 0.72  _(volume normal)_
- **Choppiness** : 42.6  _(transition)_
- **MA** : MA20 9.03 · MA50 9.07 · MA200 12.11  _(prix < MA20)_
- **Dist MA** : MA20 -14.0% · MA50 -14.3% · MA200 -35.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (842237 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
