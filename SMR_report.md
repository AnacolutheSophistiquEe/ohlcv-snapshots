# SMR

**Generated** : 2026-10-01T00:30:45.673511+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $7.90  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $7.90 (+1.7% vs entrée) · entrée $7.77 · stop $7.58 · T1 $8.08 · R/R 1.63  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.42% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +9.5 % ≠ (strike 8.5 − spot 7.90)/spot = +7.6 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -49 % hors [0,100] (R² max 0.54). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $7.71–$7.82 (mid $7.77)
- Spot actuel : $7.90 (+1.7% au-dessus de la zone — repli à attendre)
- Stop : $7.58 (plancher anti-bruit (R/R<2) ; -2.45 % depuis l'entree)
- Targets : T1 $8.08 · R/R 1.63 | T2 $8.39 · R/R 3.26 | T3 $8.71 · R/R 4.95
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $7.58


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.43 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (11.58 %)** : le gap seul le franchit 0.435 % des séances (5 fois sur 1150).
   - exécution **3.205 pt plus bas** dans le cas TYPIQUE (médiane), 13.507 au p90, **18.743 au pire**
   - perte réelle **17.667 %** en moyenne _(tirée par la queue)_, jusqu'à **30.323 %** — au lieu des 11.58 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0265 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.479 % | p01 -6.959 % | pire -30.323 % _(sur 1150 séances)_
- **P(stop avant cible)** _(source : daily, 1151 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5693** [0.4949 ; 0.6414] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4993** [0.4468 ; 0.5519] _(largeur 10.5 pt, n_eff 345.3)_
   - deep : **0.474** [0.4217 ; 0.5267] _(largeur 10.5 pt, n_eff 345.3)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-9.52 %** | CVaR **-12.13 %** | vol 6.98 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 10.78 % contre 6.17 % aujourd'hui, rapport 1.75)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -19.16 % vs -18.73 % si l'on extrapolait par √5 _(rapport 1.023 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6063** (β de hausse 1.3752, asymétrie 1.1681) vs IWM — 549 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.921× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 7.0016 sur support (1.1 ATR, 11.372 %) — p(stop avant cible) 0.5317 [0.48 ; 0.58], R/R 2.51, perte reelle 11.51 % (gap inclus), CVaR 12.84 %, EV -1.3748 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.4601 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 12.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.532, borne haute 0.584 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 12.84 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 1.1 ATR (stop 11.372 %) — p(stop avant cible) 0.5317 [0.48 ; 0.58], R/R 2.51, perte reelle 11.51 % (gap inclus), EV -1.3748 % — **REFUSE**
      - refuse : cible atteinte seulement 12.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.532, borne haute 0.584 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.84 % > budget 12.00 %
      - ⚠ support DETECTE a 0.84 ATR du spot — compartiment <1, mesure a 45.4 % de casse (IC clusterise [0.423 ; 0.484] sur 1130 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.37 %) : P(cible) 12.5 % x 28.89 % + P(rien) 34.3 % x 3.29 % ne couvrent pas P(stop) 53.2 % x 11.51 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 1.98 %) — p(stop avant cible) 0.9253 [0.89 ; 0.95], R/R 14.089, perte reelle 2.051 % (gap inclus), EV -0.5732 % — **REFUSE**
      - refuse : cible atteinte seulement 3.7 % du temps (< 15 %) meme a 10 seances : le R/R de 14.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.925, borne haute 0.950 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.57 %) : P(cible) 3.7 % x 28.89 % + P(rien) 3.8 % x 6.77 % ne couvrent pas P(stop) 92.5 % x 2.05 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 3.96 %) — p(stop avant cible) 0.8636 [0.82 ; 0.90], R/R 6.976, perte reelle 4.142 % (gap inclus), EV -1.0984 % — **REFUSE**
      - refuse : cible atteinte seulement 6.7 % du temps (< 15 %) meme a 10 seances : le R/R de 6.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.864, borne haute 0.897 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.10 %) : P(cible) 6.7 % x 28.89 % + P(rien) 6.9 % x 7.79 % ne couvrent pas P(stop) 86.4 % x 4.14 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 5.94 %) — p(stop avant cible) 0.7807 [0.73 ; 0.82], R/R 4.745, perte reelle 6.089 % (gap inclus), EV -1.1125 % — **REFUSE**
      - refuse : cible atteinte seulement 9.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.781, borne haute 0.822 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.11 %) : P(cible) 9.2 % x 28.89 % + P(rien) 12.7 % x 7.67 % ne couvrent pas P(stop) 78.1 % x 6.09 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 13.861 %) — p(stop avant cible) 0.4422 [0.39 ; 0.49], R/R 2.066, perte reelle 13.988 % (gap inclus), EV -1.2085 % — **REFUSE**
      - refuse : cible atteinte seulement 13.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.98 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.21 %) : P(cible) 13.2 % x 28.89 % + P(rien) 42.5 % x 2.71 % ne couvrent pas P(stop) 44.2 % x 13.99 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 15.841 %) — p(stop avant cible) 0.3802 [0.33 ; 0.43], R/R 1.805, perte reelle 16.011 % (gap inclus), EV -1.448 % — **REFUSE**
      - refuse : cible atteinte seulement 13.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.13 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.45 %) : P(cible) 13.4 % x 28.89 % + P(rien) 48.6 % x 1.57 % ne couvrent pas P(stop) 38.0 % x 16.01 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 17.821 %) — p(stop avant cible) 0.3032 [0.26 ; 0.35], R/R 1.607, perte reelle 17.977 % (gap inclus), EV -1.3541 % — **REFUSE**
      - refuse : cible atteinte seulement 13.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.77 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.35 %) : P(cible) 13.4 % x 28.89 % + P(rien) 56.2 % x 0.38 % ne couvrent pas P(stop) 30.3 % x 17.98 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 19.801 %) — p(stop avant cible) 0.2335 [0.19 ; 0.28], R/R 1.441, perte reelle 20.051 % (gap inclus), EV -1.263 % — **REFUSE**
      - refuse : cible atteinte seulement 13.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.97 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.26 %) : P(cible) 13.5 % x 28.89 % + P(rien) 63.2 % x -0.74 % ne couvrent pas P(stop) 23.4 % x 20.05 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 21.781 %) — p(stop avant cible) 0.1831 [0.14 ; 0.23], R/R 1.316, perte reelle 21.961 % (gap inclus), EV -1.2242 % — **REFUSE**
      - refuse : cible atteinte seulement 13.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.44 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.22 %) : P(cible) 13.5 % x 28.89 % + P(rien) 68.2 % x -1.61 % ne couvrent pas P(stop) 18.3 % x 21.96 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 23.761 %) — p(stop avant cible) 0.1427 [0.11 ; 0.18], R/R 1.198, perte reelle 24.126 % (gap inclus), EV -1.2079 % — **REFUSE**
      - refuse : cible atteinte seulement 13.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.80 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.21 %) : P(cible) 13.5 % x 28.89 % + P(rien) 72.2 % x -2.30 % ne couvrent pas P(stop) 14.3 % x 24.13 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 27.722 %) — p(stop avant cible) 0.0701 [0.05 ; 0.10], R/R 1.026, perte reelle 28.164 % (gap inclus), EV -0.9725 % — **REFUSE**
      - refuse : cible atteinte seulement 13.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.34 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.97 %) : P(cible) 13.5 % x 28.89 % + P(rien) 79.5 % x -3.65 % ne couvrent pas P(stop) 7.0 % x 28.16 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 31.682 %) — p(stop avant cible) 0.0447 [0.03 ; 0.07], R/R 0.907, perte reelle 31.873 % (gap inclus), EV -1.0182 % — **REFUSE**
      - refuse : cible atteinte seulement 13.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.57 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.02 %) : P(cible) 13.5 % x 28.89 % + P(rien) 82.0 % x -4.26 % ne couvrent pas P(stop) 4.5 % x 31.87 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 35.642 %) — p(stop avant cible) 0.0264 [0.01 ; 0.05], R/R 0.81, perte reelle 35.689 % (gap inclus), EV -0.9597 % — **REFUSE**
      - refuse : cible atteinte seulement 13.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.10 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.96 %) : P(cible) 13.5 % x 28.89 % + P(rien) 83.9 % x -4.68 % ne couvrent pas P(stop) 2.6 % x 35.69 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 39.602 %) — p(stop avant cible) 0.0168 [0.01 ; 0.03], R/R 0.727, perte reelle 39.755 % (gap inclus), EV -1.0159 % — **REFUSE**
      - refuse : cible atteinte seulement 13.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.18 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.02 %) : P(cible) 13.5 % x 28.89 % + P(rien) 84.8 % x -5.01 % ne couvrent pas P(stop) 1.7 % x 39.76 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 43.562 %) — p(stop avant cible) 0.0114 [0.00 ; 0.03], R/R 0.661, perte reelle 43.696 % (gap inclus), EV -0.9956 % — **REFUSE**
      - refuse : cible atteinte seulement 13.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.95 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.00 %) : P(cible) 13.5 % x 28.89 % + P(rien) 85.4 % x -5.16 % ne couvrent pas P(stop) 1.1 % x 43.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 47.523 %) — p(stop avant cible) 0.0054 [0.00 ; 0.02], R/R 0.608, perte reelle 47.523 % (gap inclus), EV -1.0032 % — **REFUSE**
      - refuse : cible atteinte seulement 13.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.12 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.00 %) : P(cible) 13.5 % x 28.89 % + P(rien) 86.0 % x -5.41 % ne couvrent pas P(stop) 0.5 % x 47.52 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 51.483 %) — p(stop avant cible) 0.0002 [0.00 ; 0.01], R/R 0.561, perte reelle 51.483 % (gap inclus), EV -1.001 % — **REFUSE**
      - refuse : cible atteinte seulement 13.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.06 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.00 %) : P(cible) 13.5 % x 28.89 % + P(rien) 86.5 % x -5.66 % ne couvrent pas P(stop) 0.0 % x 51.48 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 55.443 %) — p(stop avant cible) 0.0002 [0.00 ; 0.01], R/R 0.521, perte reelle 55.443 % (gap inclus), EV -1.0018 % — **REFUSE**
      - refuse : cible atteinte seulement 13.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.07 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.00 %) : P(cible) 13.5 % x 28.89 % + P(rien) 86.5 % x -5.66 % ne couvrent pas P(stop) 0.0 % x 55.44 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 59.403 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.486, perte reelle 59.403 % (gap inclus), EV -0.9963 % — **REFUSE**
      - refuse : cible atteinte seulement 13.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.01 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.00 %) : P(cible) 13.5 % x 28.89 % + P(rien) 86.5 % x -5.67 % ne couvrent pas P(stop) 0.0 % x 59.40 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 63.363 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.456, perte reelle 63.363 % (gap inclus), EV -0.9963 % — **REFUSE**
      - refuse : cible atteinte seulement 13.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.01 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.00 %) : P(cible) 13.5 % x 28.89 % + P(rien) 86.5 % x -5.67 % ne couvrent pas P(stop) 0.0 % x 63.36 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 7.9, ATR14 0.6257 (7.92 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.426 ATR = 3.374 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.396 % | 7.8687 | 92.47 % | 95.05 % | 96.28 % | 97.07 % | 97.96 % | 98.39 % |
| 0.1 ATR | 0.792 % | 7.8374 | 86.74 % | 91.23 % | 93.24 % | 94.7 % | 96.25 % | 97.47 % |
| 0.15 ATR | 1.188 % | 7.8061 | 80.79 % | 86.95 % | 89.64 % | 91.76 % | 93.98 % | 96.1 % |
| 0.2 ATR | 1.584 % | 7.7749 | 75.06 % | 82.68 % | 86.37 % | 89.28 % | 92.4 % | 95.06 % |
| 0.25 ATR | 1.98 % | 7.7436 | 69.89 % | 79.64 % | 83.78 % | 87.13 % | 90.69 % | 93.92 % |
| 0.35 ATR | 2.772 % | 7.681 | 58.2 % | 72.1 % | 77.36 % | 82.73 % | 87.63 % | 91.5 % |
| 0.5 ATR | 3.96 % | 7.5871 | 42.02 % | 58.83 % | 67.0 % | 74.04 % | 83.2 % | 88.52 % |
| 0.75 ATR | 5.94 % | 7.4307 | 20.56 % | 37.23 % | 47.64 % | 59.59 % | 72.3 % | 81.06 % |
| 1.0 ATR | 7.92 % | 7.2743 | 11.35 % | 25.76 % | 35.81 % | 49.32 % | 64.47 % | 75.2 % |
| 1.25 ATR | 9.901 % | 7.1179 | 4.72 % | 15.97 % | 25.0 % | 38.49 % | 54.82 % | 68.77 % |
| 1.5 ATR | 11.881 % | 6.9614 | 2.25 % | 9.79 % | 16.22 % | 28.33 % | 45.4 % | 62.0 % |
| 2.0 ATR | 15.841 % | 6.6486 | 0.34 % | 3.26 % | 6.53 % | 14.67 % | 31.33 % | 48.79 % |
| 2.5 ATR | 19.801 % | 6.3357 | 0.11 % | 1.35 % | 2.93 % | 6.88 % | 20.66 % | 38.0 % |
| 3.0 ATR | 23.761 % | 6.0229 | 0.11 % | 0.56 % | 1.91 % | 3.84 % | 11.8 % | 28.13 % |
| 4.0 ATR | 31.682 % | 5.3971 | 0.0 % | 0.22 % | 0.34 % | 1.13 % | 4.54 % | 13.55 % |
| 6.0 ATR | 47.523 % | 4.1457 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.34 % | 1.61 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.43 ATR | 0.47 ATR | 0.60 ATR | 0.70 ATR | 0.77 ATR | 1.05 ATR | 1.24 ATR |
| **2 s.** | 0.31 ATR | 0.60 ATR | 0.66 ATR | 0.84 ATR | 1.02 ATR | 1.15 ATR | 1.49 ATR | 1.87 ATR |
| **3 s.** | 0.38 ATR | 0.72 ATR | 0.81 ATR | 1.06 ATR | 1.25 ATR | 1.39 ATR | 1.82 ATR | 2.21 ATR |
| **5 s.** | 0.48 ATR | 0.98 ATR | 1.10 ATR | 1.39 ATR | 1.62 ATR | 1.80 ATR | 2.30 ATR | 2.81 ATR |
| **10 s.** | 0.69 ATR | 1.38 ATR | 1.51 ATR | 1.94 ATR | 2.30 ATR | 2.54 ATR | 3.25 ATR | 3.94 ATR |
| **20 s.** | 1.01 ATR | 1.95 ATR | 2.18 ATR | 2.75 ATR | 3.21 ATR | 3.56 ATR | 4.59 ATR | 5.43 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.472–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.96 %, prix 7.5872), p(touche) 42.02 % (en stress 82.02 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.66–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.94 %, prix 7.4307), p(touche) 37.23 % (en stress 88.76 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (69.0 % des re-echantillons)
- **3 seance(s)** : plage utile 0.806–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.92 %, prix 7.2743), p(touche) 35.81 % (en stress 89.89 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.1–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (9.901 %, prix 7.1178), p(touche) 38.49 % (en stress 95.51 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.514–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (15.841 %, prix 6.6486), p(touche) 31.33 % (en stress 96.63 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.176–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.004 | EV/share : $-0.001 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 46.1 | bear 44.1 | side 9.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.663% → cible +4.026% / stop −2.417%, p_fill 74%, n_eff≈78.6) : P(cible|rempli) **24%** · **EV/risk -0.064** (×p_fill ; si rempli -0.21% du capital)
  - **swing** (entrée dip −3.659% → cible +15.399% / stop −8.222%, p_fill 65%, n_eff≈75.9) : P(cible|rempli) **21%** · **EV/risk +0.047** (×p_fill ; si rempli +0.60% du capital)
  - **deep** (entrée dip −5.649% → cible +17.838% / stop −12.592%, p_fill 59%, n_eff≈67.6) : P(cible|rempli) **37%** · **EV/risk +0.049** (×p_fill ; si rempli +1.04% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→78% · +2.0%→62% · +3.0%→55% · +5.0%→34% · +8.0%→14%
- Range intraday médian 7.04% (p90 12.09%) · excursion haute méd. +3.32% / basse méd. −3.1%
- Profil de vol intra : ouverture 4.747% vs midi 1.418% vs clôture 1.69% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 76% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.135 ; mean-reverting — autocorr -0.038)_ ; drift intra méd. -0.408% ; recovery-V 32%
- **σ réalisé intraday** 4.129% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 44% / bas 66% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 7.8715 (VA 7.7725–7.9075 ; dernier close 7.76)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 47% · rebond 75% · **stop −4.79%** sous le fill (sous le bruit) · cible +2.63% · R/R 0.55 (high win-rate)
- Gaps overnight (n=159) : méd. -0.53% · baisse 56% (gap-down >1% 37% · >2% 23%)
- Excursion ouverture 5min (n=160) : bas méd −0.98% (p90 −2.95%) · haut méd +1.2% · range méd 2.65%
- Excursion ouverture 15min (n=160) : bas méd −1.4% (p90 −4.06%) · haut méd +1.54% · range méd 3.55%
- Excursion ouverture 30min (n=160) : bas méd −1.79% (p90 −4.8%) · haut méd +1.73% · range méd 4.08%
- Excursion ouverture 60min (n=160) : bas méd −2.14% (p90 −5.25%) · haut méd +2.26% · range méd 4.69%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 7.76 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 79% (128/159) · gap 50% · délai 0.0min · rebond 58% (77/128) (MFE +1.52%)
   - −1.0% : fill 30min 64% · séance 76% (122/159) · gap 38% · délai 0.0min · rebond 60% (74/122) (MFE +1.53%)
   - −1.5% : fill 30min 61% · séance 73% (116/159) · gap 27% · délai 0.0min · rebond 65% (80/116) (MFE +1.57%)
   - −2.0% : fill 30min 54% · séance 66% (107/159) · gap 23% · délai 0.9min · rebond 60% (69/107) (MFE +1.71%)
   - −3.0% : fill 30min 43% · séance 55% (92/159) · gap 10% · délai 4.8min · rebond 74% (70/92) (MFE +1.91%)
   - −4.0% : fill 30min 33% · séance 47% (81/159) · gap 4% · délai 7.8min · rebond 75% (61/81) (MFE +2.63%)
   - −5.0% : fill 30min 20% · séance 36% (62/159) · gap 2% · délai 23.4min · rebond 75% (45/62) (MFE +2.16%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.66% (p90 −2.57%) → stop au-delà de −1.9% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −2.32%) → stop au-delà de −1.96% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.95% (p90 −2.71%) → stop au-delà de −2.13% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1093 jambes) : jambe baissière méd −1.29% (p90 −3.14%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (86 séances) :
      · −1.0% : fill 96% (83/86) · rebond 59% (51/83)
      · −2.0% : fill 89% (78/86) · rebond 68% (56/78)
      · −3.0% : fill 83% (73/86) · rebond 79% (59/73)
      · −4.0% : fill 70% (63/86) · rebond 82% (51/63)
      · −5.0% : fill 53% (47/86) · rebond 80% (37/47)
   - **flat** (10 séances) :
      · −1.0% : fill 92% (8/10) · rebond 47% (4/8)
      · −2.0% : fill 79% (6/10) · rebond 39% (2/6)
      · −3.0% : fill 79% (6/10) · rebond 50% (3/6)
      · −4.0% : fill 79% (6/10) · rebond 62% (4/6)
      · −5.0% : fill 59% (4/10) · rebond 78% (3/4)
   - **gap-up** (63 séances) :
      · −1.0% : fill 49% (31/63) · rebond 67% (19/31)
      · −2.0% : fill 35% (23/63) · rebond 39% (11/23)
      · −3.0% : fill 17% (13/63) · rebond 49% (8/13)
      · −4.0% : fill 16% (12/63) · rebond 41% (6/12)
      · −5.0% : fill 12% (11/63) · rebond 49% (5/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 72% si les 15 1res min sont vertes (73 cas) · 28% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **39min** → P(séance verte=clôture>ouverture) 82% si début vert vs 20% si rouge (base 47% · écart 62 pts) ; prédictivité sature ensuite (plafond brut 197min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **82%** · continue >prix actuel 62% ; creux résiduel méd -2.23% (q20 -3.96%) → **SL/trailing à −3.96%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.58% / q75 +4.47% → **scale +2.58% / runner +4.47%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **20%** (continue à baisser 49%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.96%** (au-delà de la MAE q10 -5.96%), cible rebond +1.89% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.72% .. +4.42%] · haut q95 +6.18% · bas q05 -5.19%
   - 60min (n=160) : retour [-5.02% .. +4.86%] · haut q95 +6.57% · bas q05 -5.87%
   - 2h (n=160) : retour [-7.72% .. +5.4%] · haut q95 +7.8% · bas q05 -7.99%
   - 4h (n=160) : retour [-8.17% .. +6.96%] · haut q95 +8.33% · bas q05 -9.23%
   - 6h (n=160) : retour [-7.02% .. +8.06%] · haut q95 +9.69% · bas q05 -9.23%
   - session (n=160) : retour [-8.36% .. +8.42%] · haut q95 +10.41% · bas q05 -9.49%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 4.68%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.35 · part idiosyncratique 0.65
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 28.2  _(survente)_
- **ADX** : 14.7  _(pas de tendance nette)_
- **MACD** : hist -0.127  _(pas de croisement recent)_
- **BB** : %B 0.22 · largeur 42.6%
- **ATR** : 0.63 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.211  _(distribution)_
- **Vol ratio** : 0.68  _(volume normal)_
- **Choppiness** : 55.6  _(transition)_
- **MA** : MA20 8.96 · MA50 9.05 · MA200 12.05  _(prix < MA20)_
- **Dist MA** : MA20 -11.8% · MA50 -12.7% · MA200 -34.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (846197 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
