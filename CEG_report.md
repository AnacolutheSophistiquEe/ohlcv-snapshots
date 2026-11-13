# CEG

**Generated** : 2026-11-13T01:27:10.799643+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 8/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $282.33  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (14 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot $282.33 (+0.4% vs entrée) · entrée $281.31 · stop $258.80 · T1 $293.74 · R/R 0.55  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -5.4 % ≠ (strike 260.0 − spot 282.33)/spot = -7.9 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : %B 0.99 (collé à la bande haute) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-12 : 282.33 · ATR Wilder 13.76 (4.88 %)_
- **Swing** : plage **263.14 → 252.99** (-6.8 % a -10.39 % sous la cloture, 0.74 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 255.71-260.27 (B). stop INDICATIF 240.32 (-5.01 % sous le bas ; sous le support 247.2-250.55 (- 0,5 ATR)).
- **Deep** : plage **252.99 → 227.23** (-10.39 % a -19.52 % sous la cloture, 1.87 ATR) — touchee 45 % → 15 % du temps en 20 seances ; supports reels dans la plage : 247.2-250.55 (B) ; 240.14-246.18 (A) ; 232.79-236.2 (A) ; 224.73-231.3 (A) ; 216.13-228.28 (B). stop INDICATIF 213.46 (-6.06 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- ACHAT PAS CHER : inactif (0.02 ATR sous le plus haut 20 s., RSI(2) 85.4 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 263.92-268.72 (B, -4.82 %) ; 255.71-260.27 (B, -7.81 %) ; 247.2-250.55 (B, -11.26 %) ; 240.14-246.18 (A, -12.8 %) ; 232.79-236.2 (A, -16.34 %) ; 224.73-231.3 (A, -18.07 %)
- Resistances reelles au-dessus : 291.53-294.09 (A, 3.26 %) ; 299.33-305.8 (A, 6.02 %) ; 306.91-309.97 (A, 8.71 %) ; 317.52-322.17 (A, 12.46 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.07 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (5.52 %)** : le gap seul le franchit 0.496 % des séances (6 fois sur 1209).
   - exécution **1.687 pt plus bas** dans le cas TYPIQUE (médiane), 7.351 au p90, **10.304 au pire**
   - perte réelle **8.699 %** en moyenne _(tirée par la queue)_, jusqu'à **15.824 %** — au lieu des 5.52 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0158 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.862 % | p01 -4.443 % | pire -15.824 % _(sur 1209 séances)_
- **P(stop avant cible)** _(source : daily, 1210 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0071** [0.0009 ; 0.0291] _(largeur 2.8 pt, n_eff 173.1)_
   - swing : **0.4566** [0.4046 ; 0.5093] _(largeur 10.5 pt, n_eff 345.6)_
   - deep : **0.4126** [0.3616 ; 0.4651] _(largeur 10.3 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-4.72 %** | CVaR **-6.89 %** | vol 3.16 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 5.63 % contre 3.01 % aujourd'hui, rapport 1.87)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.09 % vs -9.8 % si l'on extrapolait par √5 _(rapport 1.03 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1516** (β de hausse 1.1947, asymétrie 0.9639) vs SPY — 559 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.715× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 262.2643 sur atr_based (1.5 ATR, 7.107 %) — p(stop avant cible) 0.4548 [0.40 ; 0.51], R/R 4.453, perte reelle 7.276 % (gap inclus), CVaR 8.64 %, EV -0.5306 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.952 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 4.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.34 ATR (stop 3.901 %) — p(stop avant cible) 0.69 [0.64 ; 0.74], R/R 7.964, perte reelle 4.068 % (gap inclus), EV -0.5853 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 7.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.690, borne haute 0.737 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.59 %) : P(cible) 0.7 % x 32.40 % + P(rien) 30.3 % x 6.57 % ne couvrent pas P(stop) 69.0 % x 4.07 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_based a 1.5 ATR (stop 7.107 %) — p(stop avant cible) 0.4548 [0.40 ; 0.51], R/R 4.453, perte reelle 7.276 % (gap inclus), EV -0.5306 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 4.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 0.7 % x 32.40 % + P(rien) 53.8 % x 4.73 % ne couvrent pas P(stop) 45.5 % x 7.28 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 support a 4.04 ATR (stop 21.447 %) — p(stop avant cible) 0.0093 [0.00 ; 0.02], R/R 1.503, perte reelle 21.553 % (gap inclus), EV -0.1845 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.13 % > budget 12.00 %
      - ⚠ support DETECTE a 0.24 ATR du spot — compartiment <1, mesure a 50.7 % de casse (IC clusterise [0.471 ; 0.542] sur 1138 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.18 %) : P(cible) 0.8 % x 32.40 % + P(rien) 98.3 % x -0.23 % ne couvrent pas P(stop) 0.9 % x 21.55 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 0.34 ATR (stop 3.02 %) — p(stop avant cible) 0.7444 [0.70 ; 0.79], R/R 10.102, perte reelle 3.207 % (gap inclus), EV -0.3666 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 10.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.744, borne haute 0.788 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.37 %) : P(cible) 0.7 % x 32.40 % + P(rien) 24.8 % x 7.20 % ne couvrent pas P(stop) 74.4 % x 3.21 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 4.738 %) — p(stop avant cible) 0.6496 [0.60 ; 0.70], R/R 6.625, perte reelle 4.89 % (gap inclus), EV -0.8886 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 6.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.650, borne haute 0.699 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.89 %) : P(cible) 0.7 % x 32.40 % + P(rien) 34.3 % x 5.99 % ne couvrent pas P(stop) 65.0 % x 4.89 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 5.923 %) — p(stop avant cible) 0.5352 [0.48 ; 0.59], R/R 5.328, perte reelle 6.081 % (gap inclus), EV -0.5003 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 5.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.535, borne haute 0.587 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.50 %) : P(cible) 0.7 % x 32.40 % + P(rien) 45.8 % x 5.51 % ne couvrent pas P(stop) 53.5 % x 6.08 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 8.292 %) — p(stop avant cible) 0.3898 [0.34 ; 0.44], R/R 3.861, perte reelle 8.391 % (gap inclus), EV -0.6252 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.63 %) : P(cible) 0.7 % x 32.40 % + P(rien) 60.3 % x 4.00 % ne couvrent pas P(stop) 39.0 % x 8.39 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 9.476 %) — p(stop avant cible) 0.3374 [0.29 ; 0.39], R/R 3.387, perte reelle 9.566 % (gap inclus), EV -0.7396 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.74 %) : P(cible) 0.7 % x 32.40 % + P(rien) 65.5 % x 3.44 % ne couvrent pas P(stop) 33.7 % x 9.57 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 10.661 %) — p(stop avant cible) 0.2655 [0.22 ; 0.31], R/R 3.012, perte reelle 10.758 % (gap inclus), EV -0.5404 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.54 %) : P(cible) 0.7 % x 32.40 % + P(rien) 72.7 % x 2.86 % ne couvrent pas P(stop) 26.6 % x 10.76 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 11.845 %) — p(stop avant cible) 0.2112 [0.17 ; 0.26], R/R 2.715, perte reelle 11.935 % (gap inclus), EV -0.457 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.22 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.46 %) : P(cible) 0.8 % x 32.40 % + P(rien) 78.1 % x 2.33 % ne couvrent pas P(stop) 21.1 % x 11.93 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 13.03 %) — p(stop avant cible) 0.1778 [0.14 ; 0.22], R/R 2.47, perte reelle 13.115 % (gap inclus), EV -0.4979 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.33 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.50 %) : P(cible) 0.8 % x 32.40 % + P(rien) 81.5 % x 1.95 % ne couvrent pas P(stop) 17.8 % x 13.12 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 14.214 %) — p(stop avant cible) 0.1371 [0.10 ; 0.18], R/R 2.273, perte reelle 14.252 % (gap inclus), EV -0.456 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.32 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.46 %) : P(cible) 0.8 % x 32.40 % + P(rien) 85.5 % x 1.46 % ne couvrent pas P(stop) 13.7 % x 14.25 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 16.583 %) — p(stop avant cible) 0.0581 [0.04 ; 0.09], R/R 1.948, perte reelle 16.632 % (gap inclus), EV -0.3028 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.64 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.30 %) : P(cible) 0.8 % x 32.40 % + P(rien) 93.4 % x 0.45 % ne couvrent pas P(stop) 5.8 % x 16.63 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 grid_snapped a 4.04 ATR (stop 20.566 %) — p(stop avant cible) 0.0136 [0.01 ; 0.03], R/R 1.57, perte reelle 20.635 % (gap inclus), EV -0.2081 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.46 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.21 %) : P(cible) 0.8 % x 32.40 % + P(rien) 97.9 % x -0.18 % ne couvrent pas P(stop) 1.4 % x 20.63 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 23.691 %) — p(stop avant cible) 0.0067 [0.00 ; 0.02], R/R 1.365, perte reelle 23.731 % (gap inclus), EV -0.177 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.19 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.18 %) : P(cible) 0.8 % x 32.40 % + P(rien) 98.6 % x -0.27 % ne couvrent pas P(stop) 0.7 % x 23.73 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 26.06 %) — p(stop avant cible) 0.0052 [0.00 ; 0.02], R/R 1.241, perte reelle 26.113 % (gap inclus), EV -0.1693 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.23 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 0.8 % x 32.40 % + P(rien) 98.7 % x -0.28 % ne couvrent pas P(stop) 0.5 % x 26.11 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 28.429 %) — p(stop avant cible) 0.0036 [0.00 ; 0.01], R/R 1.133, perte reelle 28.609 % (gap inclus), EV -0.1724 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.27 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 0.8 % x 32.40 % + P(rien) 98.9 % x -0.32 % ne couvrent pas P(stop) 0.4 % x 28.61 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 30.798 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 1.052, perte reelle 30.798 % (gap inclus), EV -0.1645 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.13 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 0.8 % x 32.40 % + P(rien) 99.1 % x -0.38 % ne couvrent pas P(stop) 0.1 % x 30.80 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 33.167 %) — p(stop avant cible) 0.0005 [0.00 ; 0.01], R/R 0.977, perte reelle 33.167 % (gap inclus), EV -0.1643 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.13 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 0.8 % x 32.40 % + P(rien) 99.2 % x -0.40 % ne couvrent pas P(stop) 0.1 % x 33.17 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 35.536 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.912, perte reelle 35.536 % (gap inclus), EV -0.1641 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.13 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 0.8 % x 32.40 % + P(rien) 99.2 % x -0.41 % ne couvrent pas P(stop) 0.0 % x 35.54 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 37.905 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.855, perte reelle 37.905 % (gap inclus), EV -0.1641 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.13 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 0.8 % x 32.40 % + P(rien) 99.2 % x -0.41 % ne couvrent pas P(stop) 0.0 % x 37.91 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 282.33, ATR14 13.3771 (4.738 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.39 ATR = 1.848 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.237 % | 281.6611 | 91.78 % | 94.73 % | 95.67 % | 96.72 % | 97.66 % | 98.06 % |
| 0.1 ATR | 0.474 % | 280.9923 | 85.67 % | 90.61 % | 92.61 % | 94.18 % | 95.74 % | 96.88 % |
| 0.15 ATR | 0.711 % | 280.3234 | 79.03 % | 86.39 % | 88.6 % | 90.79 % | 93.94 % | 95.59 % |
| 0.2 ATR | 0.948 % | 279.6546 | 72.08 % | 81.01 % | 84.27 % | 86.98 % | 91.49 % | 94.3 % |
| 0.25 ATR | 1.185 % | 278.9857 | 65.23 % | 75.42 % | 79.41 % | 83.28 % | 88.83 % | 92.37 % |
| 0.35 ATR | 1.658 % | 277.648 | 54.06 % | 66.14 % | 71.7 % | 77.14 % | 84.47 % | 88.92 % |
| 0.5 ATR | 2.369 % | 275.6414 | 38.88 % | 53.06 % | 59.66 % | 66.77 % | 77.45 % | 83.33 % |
| 0.75 ATR | 3.554 % | 272.2971 | 20.44 % | 36.81 % | 45.51 % | 53.97 % | 67.34 % | 76.56 % |
| 1.0 ATR | 4.738 % | 268.9528 | 11.06 % | 24.05 % | 33.47 % | 43.92 % | 58.4 % | 70.32 % |
| 1.25 ATR | 5.923 % | 265.6085 | 5.69 % | 16.14 % | 24.39 % | 36.08 % | 52.13 % | 64.19 % |
| 1.5 ATR | 7.107 % | 262.2643 | 2.74 % | 10.76 % | 17.42 % | 29.21 % | 45.11 % | 58.06 % |
| 2.0 ATR | 9.476 % | 255.5757 | 0.84 % | 4.32 % | 9.19 % | 17.88 % | 31.49 % | 46.34 % |
| 2.5 ATR | 11.845 % | 248.8871 | 0.42 % | 2.22 % | 4.75 % | 11.01 % | 21.17 % | 36.67 % |
| 3.0 ATR | 14.214 % | 242.1985 | 0.0 % | 1.05 % | 2.75 % | 6.77 % | 15.32 % | 28.82 % |
| 4.0 ATR | 18.953 % | 228.8214 | 0.0 % | 0.21 % | 0.84 % | 2.65 % | 6.91 % | 14.19 % |
| 6.0 ATR | 28.429 % | 202.0671 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.74 % | 2.69 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.39 ATR | 0.44 ATR | 0.58 ATR | 0.69 ATR | 0.76 ATR | 1.05 ATR | 1.31 ATR |
| **2 s.** | 0.26 ATR | 0.55 ATR | 0.62 ATR | 0.82 ATR | 0.98 ATR | 1.13 ATR | 1.56 ATR | 1.95 ATR |
| **3 s.** | 0.31 ATR | 0.67 ATR | 0.76 ATR | 1.01 ATR | 1.23 ATR | 1.41 ATR | 1.95 ATR | 2.47 ATR |
| **5 s.** | 0.38 ATR | 0.85 ATR | 0.97 ATR | 1.36 ATR | 1.69 ATR | 1.91 ATR | 2.62 ATR | 3.43 ATR |
| **10 s.** | 0.56 ATR | 1.33 ATR | 1.50 ATR | 1.95 ATR | 2.31 ATR | 2.60 ATR | 3.63 ATR | 4.62 ATR |
| **20 s.** | 0.81 ATR | 1.84 ATR | 2.07 ATR | 2.73 ATR | 3.26 ATR | 3.60 ATR | 4.73 ATR | 5.60 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.44–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.369 %, prix 275.6416), p(touche) 38.88 % (en stress 82.11 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.624–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.554 %, prix 272.296), p(touche) 36.81 % (en stress 87.37 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.761–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.738 %, prix 268.9532), p(touche) 33.47 % (en stress 95.79 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.973–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.738 %, prix 268.9532), p(touche) 43.92 % (en stress 96.84 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 55.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.504–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (9.476 %, prix 255.5764), p(touche) 31.49 % (en stress 96.81 %)  ✅ optimum identifie (77.2 % des re-echantillons)
- **20 seance(s)** : plage utile 2.069–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (11.845 %, prix 248.888), p(touche) 36.67 % (en stress 95.7 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (87.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.037 | EV/share : $-0.828 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 6 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 18.2 | side 76.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 509.0 (= 2 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.359% → cible +4.422% / stop −8.0%, p_fill 86%, n_eff≈90.4) : P(cible|rempli) **5%** · **EV/risk -0.063** (×p_fill ; si rempli -0.59% du capital)
  - **swing** (entrée dip −0.782% → cible +4.865% / stop −4.776%, p_fill 82%, n_eff≈95.0) : P(cible|rempli) **32%** · **EV/risk -0.137** (×p_fill ; si rempli -0.80% du capital)
  - **deep** (entrée dip −1.142% → cible +7.579% / stop −7.19%, p_fill 76%, n_eff≈83.6) : P(cible|rempli) **36%** · **EV/risk -0.019** (×p_fill ; si rempli -0.18% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→62% · +2.0%→34% · +3.0%→18% · +5.0%→4% · +8.0%→0%
- Range intraday médian 3.36% (p90 5.65%) · excursion haute méd. +1.38% / basse méd. −1.56%
- Profil de vol intra : ouverture 2.53% vs midi 0.658% vs clôture 0.771% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 15% · trend ↑1%/↓0% ; spike-down 52% · recovery-V 16%)_
- **Régime intraday** : **chop** _(efficiency 0.135 ; neutre — autocorr 0.005)_ ; drift intra méd. -0.554% ; recovery-V 16%
- **σ réalisé intraday** 2.532% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 59% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 253.5534 (VA 252.1149–254.9919 ; dernier close 253.44)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 15% · rebond 39% · **stop −2.72%** sous le fill (sous le bruit) · cible +0.65% · R/R 0.24 (high win-rate)
- Gaps overnight (n=159) : méd. 0.39% · baisse 43% (gap-down >1% 15% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.72% (p90 −1.8%) · haut méd +0.66% · range méd 1.52%
- Excursion ouverture 15min (n=160) : bas méd −0.97% (p90 −2.69%) · haut méd +0.84% · range méd 2.02%
- Excursion ouverture 30min (n=160) : bas méd −1.06% (p90 −3.19%) · haut méd +0.92% · range méd 2.31%
- Excursion ouverture 60min (n=160) : bas méd −1.18% (p90 −3.97%) · haut méd +1.01% · range méd 2.73%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 253.45 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 68% (102/159) · gap 29% · délai 0.0min · rebond 38% (45/102) (MFE +0.8%)
   - −1.0% : fill 30min 46% · séance 58% (87/159) · gap 15% · délai 1.4min · rebond 46% (38/87) (MFE +0.97%)
   - −1.5% : fill 30min 41% · séance 52% (75/159) · gap 7% · délai 4.1min · rebond 52% (34/75) (MFE +1.03%)
   - −2.0% : fill 30min 30% · séance 46% (64/159) · gap 4% · délai 9.6min · rebond 52% (33/64) (MFE +1.03%)
   - −3.0% : fill 30min 15% · séance 25% (35/159) · gap 3% · délai 14.2min · rebond 50% (15/35) (MFE +0.96%)
   - −4.0% : fill 30min 9% · séance 15% (21/159) · gap 0% · délai 21.4min · rebond 39% (10/21) (MFE +0.65%)
   - −5.0% : fill 30min 3% · séance 10% (13/159) · gap 0% · délai 61.8min · rebond 33% (7/13) (MFE +0.56%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.3% (p90 −1.42%) → stop au-delà de −0.98% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.53% (p90 −1.41%) → stop au-delà de −1.07% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −1.48%) → stop au-delà de −1.05% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=471 jambes) : jambe baissière méd −1.09% (p90 −2.58%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (45 séances) :
      · −1.0% : fill 94% (42/45) · rebond 46% (19/42)
      · −2.0% : fill 88% (37/45) · rebond 54% (19/37)
      · −3.0% : fill 51% (22/45) · rebond 40% (8/22)
      · −4.0% : fill 41% (18/45) · rebond 38% (8/18)
      · −5.0% : fill 26% (12/45) · rebond 32% (6/12)
   - **flat** (24 séances) :
      · −1.0% : fill 52% (15/24) · rebond 31% (3/15)
      · −2.0% : fill 40% (11/24) · rebond 64% (6/11)
      · −3.0% : fill 11% (5/24) · rebond 18% (1/5)
      · −4.0% : fill 3% (2/24) · rebond 28% (1/2)
      · −5.0% : fill 1% (1/24) · rebond 100% (1/1)
   - **gap-up** (90 séances) :
      · −1.0% : fill 34% (30/90) · rebond 52% (16/30)
      · −2.0% : fill 19% (16/90) · rebond 41% (8/16)
      · −3.0% : fill 11% (8/90) · rebond 92% (6/8)
      · −4.0% : fill 0% (1/90) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/90) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 62% si les 15 1res min sont vertes (80 cas) · 27% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **39min** → P(séance verte=clôture>ouverture) 80% si début vert vs 16% si rouge (base 42% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **80%** · continue >prix actuel 46% ; creux résiduel méd -1.18% (q20 -2.14%) → **SL/trailing à −2.14%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.2% / q75 +2.04% → **scale +1.2% / runner +2.04%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **16%** (continue à baisser 56%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.3%** (au-delà de la MAE q10 -2.3%), cible rebond +0.93% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.44% .. +2.01%] · haut q95 +3.41% · bas q05 -3.51%
   - 60min (n=160) : retour [-3.66% .. +2.94%] · haut q95 +3.74% · bas q05 -4.68%
   - 2h (n=160) : retour [-3.81% .. +3.8%] · haut q95 +4.14% · bas q05 -5.27%
   - 4h (n=160) : retour [-4.48% .. +3.64%] · haut q95 +4.31% · bas q05 -5.39%
   - 6h (n=160) : retour [-4.7% .. +3.8%] · haut q95 +4.82% · bas q05 -5.75%
   - session (n=160) : retour [-4.6% .. +3.49%] · haut q95 +4.82% · bas q05 -5.87%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 4.4% / strong 1.9%) · base = 10 séances trend-up (n_eff 7.4)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **32%**. Lecture précoce 30 min : signature présente → 14% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.11% (p75 1.79% / p90 2.39%) · ~1.0 replis/séance, durée méd 169.74 min. P(nouveau plus-haut après repli) :
   - −0.5% → **68%** (reprise méd 29.55 min, n=17)
   - −1.0% → **67%** (reprise méd 182.65 min, n=9)
   - −1.5% → **45%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.39%** (p90, défaut prudent ; serré/agressif −1.79%) ; extension open→close méd +3.62% (q75 +4.52% / q95 +6.21%), MFE méd +4.59% / q90 +5.86%
   - Échelle scale-out : +4.59% (33%) / +5.3% (33%) / +5.86% (34%)
- **DÉSARMER** : repli > **−2.39%** depuis le plus-haut = décay → P(retournement) **100%** (préavis méd 280.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.86% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 96% du temps (retour médian dernière heure +0.49%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.56 · part idiosyncratique 0.44
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 63.0  _(momentum haussier)_
- **ADX** : 14.2  _(pas de tendance nette)_
- **MACD** : hist 2.898  _(bullish_recent)_
- **BB** : %B 0.99 · largeur 16.3%
- **ATR** : 13.38 (58.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.066  _(accumulation)_
- **Vol ratio** : 0.7  _(volume normal)_
- **Choppiness** : 49.0  _(transition)_
- **MA** : MA20 261.31 · MA50 269.6 · MA200 277.92  _(prix > MA20)_
- **Dist MA** : MA20 +8.0% · MA50 +4.7% · MA200 +1.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (719241 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
