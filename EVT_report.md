# EVT

**Generated** : 2026-11-09T01:06:53.318096+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 8/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €3.16  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-10 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot €3.16 (+0.3% vs entrée) · entrée €3.15 · stop €3.03 · T1 €3.25 · R/R 0.83  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -113 % hors [0,100] (R² max 0.94). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.050 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._
- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : RSI 77.5 > 70 (surachat) ; %B 0.99 (collé à la bande haute) ; extension extrême (≥3×ATR, confluence MA20/50) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-06 : 3.16 · ATR Wilder 0.1396 (4.41 %)_
- **Swing** : plage **2.98 → 2.84** (-5.94 % a -10.31 % sous la cloture, 0.99 ATR) — touchee 50 % → 30 % du temps en 10 seances ; aucun support reel dans la plage. stop INDICATIF 2.64 (-6.96 % sous le bas ; sous le support 2.71-2.77 (- 0,5 ATR)).
- **Deep** : plage **2.84 → 2.26** (-10.31 % a -28.52 % sous la cloture, 4.13 ATR) — touchee 50 % → 15 % du temps en 20 seances ; supports reels dans la plage : 2.71-2.77 (A) ; 2.41-2.41 (C). stop INDICATIF 2.12 (-6.17 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- ACHAT PAS CHER : inactif (0.19 ATR sous le plus haut 20 s., RSI(2) 97.5 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 2.71-2.77 (A, -12.58 %) ; 2.41-2.41 (C, -23.96 %)
- Resistances reelles au-dessus : 3.37-3.41 (A, 6.64 %) ; 3.88-3.88 (C, 22.63 %) ; 3.99-4.01 (B, 26.26 %) ; 4.43-4.47 (A, 40.08 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.35 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (4.83 %)** : le gap seul le franchit 0.863 % des séances (11 fois sur 1274).
   - exécution **2.282 pt plus bas** dans le cas TYPIQUE (médiane), 16.781 au p90, **27.583 au pire**
   - perte réelle **11.717 %** en moyenne _(tirée par la queue)_, jusqu'à **32.413 %** — au lieu des 4.83 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0595 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 11 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.044 % | p01 -3.984 % | pire -32.413 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1082** [0.0685 ; 0.1609] _(largeur 9.2 pt, n_eff 173.1)_
   - swing : **0.5203** [0.4677 ; 0.5726] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.5107** [0.4581 ; 0.5631] _(largeur 10.5 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 480 séances)** : VaR **-4.8 %** | CVaR **-8.97 %** | vol 3.6 %/j
   - _fenêtre arrêtée : rupture de regime a 540 seances en arriere (volatilite 6.09 % contre 3.54 % aujourd'hui, rapport 1.72)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.04 % vs -11.16 % si l'on extrapolait par √5 _(rapport 1.169 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1004** (β de hausse 0.9219, asymétrie 1.1937) vs GDAXI — 601 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 3.0177 sur support (0.52 ATR, 4.624 %) — p(stop avant cible) 0.6342 [0.58 ; 0.68], R/R 7.868, perte reelle 5.11 % (gap inclus), CVaR 10.373 %, EV -0.4456 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.2344 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 7.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.634, borne haute 0.684 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.52 ATR (stop 4.624 %) — p(stop avant cible) 0.6342 [0.58 ; 0.68], R/R 7.868, perte reelle 5.11 % (gap inclus), EV -0.4456 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 7.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.634, borne haute 0.684 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.32 ATR du spot — compartiment <1, mesure a 45.0 % de casse (IC clusterise [0.421 ; 0.482] sur 1160 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.45 %) : P(cible) 0.1 % x 40.21 % + P(rien) 36.4 % x 7.53 % ne couvrent pas P(stop) 63.4 % x 5.11 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_based a 1.5 ATR (stop 5.973 %) — p(stop avant cible) 0.5426 [0.49 ; 0.59], R/R 5.903, perte reelle 6.811 % (gap inclus), EV -0.779 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 5.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.543, borne haute 0.595 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 14.75 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.78 %) : P(cible) 0.2 % x 40.21 % + P(rien) 45.6 % x 6.26 % ne couvrent pas P(stop) 54.3 % x 6.81 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 3.6 ATR (stop 16.887 %) — p(stop avant cible) 0.1342 [0.10 ; 0.17], R/R 2.146, perte reelle 18.738 % (gap inclus), EV -1.8006 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.85 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.80 %) : P(cible) 0.2 % x 40.21 % + P(rien) 86.4 % x 0.75 % ne couvrent pas P(stop) 13.4 % x 18.74 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 6.02 ATR (stop 26.495 %) — p(stop avant cible) 0.0579 [0.04 ; 0.09], R/R 1.502, perte reelle 26.772 % (gap inclus), EV -1.9417 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.82 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.94 %) : P(cible) 0.2 % x 40.21 % + P(rien) 94.0 % x -0.48 % ne couvrent pas P(stop) 5.8 % x 26.77 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 0.996 %) — p(stop avant cible) 0.9085 [0.87 ; 0.94], R/R 35.298, perte reelle 1.139 % (gap inclus), EV -0.1708 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 35.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.908, borne haute 0.935 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 0.1 % x 40.21 % + P(rien) 9.1 % x 9.24 % ne couvrent pas P(stop) 90.8 % x 1.14 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+40.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🔴 grid_snapped a 0.52 ATR (stop 3.281 %) — p(stop avant cible) 0.7118 [0.66 ; 0.76], R/R 10.905, perte reelle 3.687 % (gap inclus), EV -0.2874 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 10.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.712, borne haute 0.758 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.29 %) : P(cible) 0.1 % x 40.21 % + P(rien) 28.7 % x 8.01 % ne couvrent pas P(stop) 71.2 % x 3.69 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+40.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.0 ATR (stop 3.982 %) — p(stop avant cible) 0.6728 [0.62 ; 0.72], R/R 9.058, perte reelle 4.439 % (gap inclus), EV -0.3556 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 9.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.673, borne haute 0.721 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 0.1 % x 40.21 % + P(rien) 32.6 % x 7.95 % ne couvrent pas P(stop) 67.3 % x 4.44 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+40.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.75 ATR (stop 6.969 %) — p(stop avant cible) 0.4776 [0.43 ; 0.53], R/R 4.93, perte reelle 8.156 % (gap inclus), EV -1.0733 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 17.92 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.07 %) : P(cible) 0.2 % x 40.21 % + P(rien) 52.1 % x 5.29 % ne couvrent pas P(stop) 47.8 % x 8.16 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 7.965 %) — p(stop avant cible) 0.4222 [0.37 ; 0.47], R/R 4.313, perte reelle 9.323 % (gap inclus), EV -1.293 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 19.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.29 %) : P(cible) 0.2 % x 40.21 % + P(rien) 57.6 % x 4.48 % ne couvrent pas P(stop) 42.2 % x 9.32 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 8.96 %) — p(stop avant cible) 0.3766 [0.33 ; 0.43], R/R 3.873, perte reelle 10.381 % (gap inclus), EV -1.4134 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 19.57 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.41 %) : P(cible) 0.2 % x 40.21 % + P(rien) 62.2 % x 3.91 % ne couvrent pas P(stop) 37.7 % x 10.38 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 9.956 %) — p(stop avant cible) 0.3463 [0.30 ; 0.40], R/R 3.539, perte reelle 11.361 % (gap inclus), EV -1.5597 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 19.63 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.56 %) : P(cible) 0.2 % x 40.21 % + P(rien) 65.2 % x 3.54 % ne couvrent pas P(stop) 34.6 % x 11.36 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 10.951 %) — p(stop avant cible) 0.3176 [0.27 ; 0.37], R/R 3.255, perte reelle 12.353 % (gap inclus), EV -1.7334 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 19.83 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.73 %) : P(cible) 0.2 % x 40.21 % + P(rien) 68.1 % x 3.12 % ne couvrent pas P(stop) 31.8 % x 12.35 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 11.947 %) — p(stop avant cible) 0.2781 [0.23 ; 0.33], R/R 3.002, perte reelle 13.393 % (gap inclus), EV -1.8313 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 19.99 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.83 %) : P(cible) 0.2 % x 40.21 % + P(rien) 72.0 % x 2.54 % ne couvrent pas P(stop) 27.8 % x 13.39 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 grid_snapped a 3.6 ATR (stop 15.544 %) — p(stop avant cible) 0.1558 [0.12 ; 0.20], R/R 2.309, perte reelle 17.413 % (gap inclus), EV -1.8295 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.37 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.83 %) : P(cible) 0.2 % x 40.21 % + P(rien) 84.3 % x 0.97 % ne couvrent pas P(stop) 15.6 % x 17.41 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 17.92 %) — p(stop avant cible) 0.114 [0.08 ; 0.15], R/R 2.027, perte reelle 19.832 % (gap inclus), EV -1.7251 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.28 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.73 %) : P(cible) 0.2 % x 40.21 % + P(rien) 88.4 % x 0.53 % ne couvrent pas P(stop) 11.4 % x 19.83 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 19.912 %) — p(stop avant cible) 0.0928 [0.07 ; 0.13], R/R 1.874, perte reelle 21.455 % (gap inclus), EV -1.7526 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.78 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.75 %) : P(cible) 0.2 % x 40.21 % + P(rien) 90.6 % x 0.19 % ne couvrent pas P(stop) 9.3 % x 21.45 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 21.903 %) — p(stop avant cible) 0.077 [0.05 ; 0.11], R/R 1.753, perte reelle 22.939 % (gap inclus), EV -1.7724 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.77 %) : P(cible) 0.2 % x 40.21 % + P(rien) 92.1 % x -0.08 % ne couvrent pas P(stop) 7.7 % x 22.94 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 grid_snapped a 6.02 ATR (stop 25.152 %) — p(stop avant cible) 0.0636 [0.04 ; 0.09], R/R 1.58, perte reelle 25.451 % (gap inclus), EV -1.883 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.53 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.88 %) : P(cible) 0.2 % x 40.21 % + P(rien) 93.5 % x -0.35 % ne couvrent pas P(stop) 6.4 % x 25.45 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 25.885 %) — p(stop avant cible) 0.0594 [0.04 ; 0.09], R/R 1.535, perte reelle 26.198 % (gap inclus), EV -1.9103 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.26 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.91 %) : P(cible) 0.2 % x 40.21 % + P(rien) 93.9 % x -0.45 % ne couvrent pas P(stop) 5.9 % x 26.20 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 27.876 %) — p(stop avant cible) 0.0474 [0.03 ; 0.07], R/R 1.431, perte reelle 28.106 % (gap inclus), EV -1.9877 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.06 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.99 %) : P(cible) 0.2 % x 40.21 % + P(rien) 95.1 % x -0.76 % ne couvrent pas P(stop) 4.7 % x 28.11 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 29.867 %) — p(stop avant cible) 0.0365 [0.02 ; 0.06], R/R 1.337, perte reelle 30.071 % (gap inclus), EV -2.0224 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.02 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.02 %) : P(cible) 0.2 % x 40.21 % + P(rien) 96.2 % x -1.03 % ne couvrent pas P(stop) 3.6 % x 30.07 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 31.858 %) — p(stop avant cible) 0.0365 [0.02 ; 0.06], R/R 1.258, perte reelle 31.973 % (gap inclus), EV -2.0918 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.41 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.09 %) : P(cible) 0.2 % x 40.21 % + P(rien) 96.2 % x -1.03 % ne couvrent pas P(stop) 3.6 % x 31.97 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 3.164, ATR14 0.126 (3.982 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.367 ATR = 1.462 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.199 % | 3.1577 | 88.76 % | 91.51 % | 93.48 % | 95.45 % | 97.21 % | 98.29 % |
| 0.1 ATR | 0.398 % | 3.1514 | 81.36 % | 86.67 % | 89.62 % | 92.48 % | 95.52 % | 97.19 % |
| 0.15 ATR | 0.597 % | 3.1451 | 75.35 % | 82.92 % | 86.66 % | 89.8 % | 93.83 % | 96.08 % |
| 0.2 ATR | 0.796 % | 3.1388 | 69.13 % | 79.17 % | 83.6 % | 87.23 % | 91.94 % | 94.77 % |
| 0.25 ATR | 0.996 % | 3.1325 | 63.21 % | 75.72 % | 80.34 % | 84.65 % | 89.85 % | 93.57 % |
| 0.35 ATR | 1.394 % | 3.1199 | 51.87 % | 67.32 % | 73.62 % | 79.5 % | 85.87 % | 91.56 % |
| 0.5 ATR | 1.991 % | 3.101 | 35.6 % | 54.79 % | 62.65 % | 70.69 % | 79.9 % | 88.34 % |
| 0.75 ATR | 2.987 % | 3.0695 | 18.93 % | 37.61 % | 47.23 % | 59.21 % | 71.34 % | 82.11 % |
| 1.0 ATR | 3.982 % | 3.038 | 9.86 % | 24.88 % | 35.67 % | 47.23 % | 62.09 % | 75.68 % |
| 1.25 ATR | 4.978 % | 3.0065 | 4.64 % | 16.98 % | 27.08 % | 39.31 % | 55.52 % | 70.65 % |
| 1.5 ATR | 5.973 % | 2.975 | 2.86 % | 11.06 % | 19.27 % | 31.29 % | 48.46 % | 65.73 % |
| 2.0 ATR | 7.965 % | 2.912 | 1.28 % | 4.84 % | 9.29 % | 19.21 % | 35.02 % | 54.07 % |
| 2.5 ATR | 9.956 % | 2.849 | 0.49 % | 2.67 % | 5.63 % | 12.18 % | 27.76 % | 46.63 % |
| 3.0 ATR | 11.947 % | 2.786 | 0.39 % | 1.58 % | 3.75 % | 8.61 % | 20.9 % | 39.7 % |
| 4.0 ATR | 15.929 % | 2.66 | 0.2 % | 0.89 % | 1.98 % | 4.16 % | 11.94 % | 25.03 % |
| 6.0 ATR | 23.894 % | 2.408 | 0.0 % | 0.39 % | 0.89 % | 2.08 % | 5.17 % | 13.67 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.37 ATR | 0.41 ATR | 0.54 ATR | 0.66 ATR | 0.73 ATR | 1.00 ATR | 1.23 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.64 ATR | 0.84 ATR | 1.00 ATR | 1.15 ATR | 1.58 ATR | 1.99 ATR |
| **3 s.** | 0.33 ATR | 0.70 ATR | 0.80 ATR | 1.08 ATR | 1.32 ATR | 1.48 ATR | 1.96 ATR | 2.67 ATR |
| **5 s.** | 0.43 ATR | 0.94 ATR | 1.07 ATR | 1.45 ATR | 1.76 ATR | 1.97 ATR | 2.81 ATR | 3.81 ATR |
| **10 s.** | 0.64 ATR | 1.45 ATR | 1.63 ATR | 2.14 ATR | 2.70 ATR | 3.10 ATR | 4.57 ATR | hors grille |
| **20 s.** | 1.03 ATR | 2.27 ATR | 2.62 ATR | 3.46 ATR | 4.00 ATR | 4.89 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.413 ATR au-dessus du haut de la grille, 0.25 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.642–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.987 %, prix 3.0695), p(touche) 37.61 % (en stress 88.24 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (67.9 % des re-echantillons)
- **3 seance(s)** : plage utile 0.798–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.982 %, prix 3.038), p(touche) 35.67 % (en stress 96.08 %)  ✅ optimum identifie (69.1 % des re-echantillons)
- **5 seance(s)** : plage utile 1.07–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.978 %, prix 3.0065), p(touche) 39.31 % (en stress 94.06 %)  ✅ optimum identifie (76.8 % des re-echantillons)
- **10 seance(s)** : plage utile 1.629–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.965 %, prix 2.912), p(touche) 35.02 % (en stress 98.02 %)  ✅ optimum identifie (71.1 % des re-echantillons)
- **20 seance(s)** : plage utile 2.618–4.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (11.947 %, prix 2.786), p(touche) 39.7 % (en stress 98.0 %)  ✅ optimum identifie (81.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.027 | EV/share : €-0.004 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 24 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 9.0 | bear 5.9 | side 85.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 288.0 (= 91 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.385% → cible +3.239% / stop −4.001%, p_fill 87%, n_eff≈91.9) : P(cible|rempli) **17%** · **EV/risk -0.108** (×p_fill ; si rempli -0.50% du capital)
  - **swing** (entrée dip −0.848% → cible +7.883% / stop −4.016%, p_fill 82%, n_eff≈94.4) : P(cible|rempli) **22%** · **EV/risk -0.152** (×p_fill ; si rempli -0.74% du capital)
  - **deep** (entrée dip −1.247% → cible +8.315% / stop −6.049%, p_fill 82%, n_eff≈90.6) : P(cible|rempli) **26%** · **EV/risk -0.211** (×p_fill ; si rempli -1.56% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→67% · +2.0%→44% · +3.0%→26% · +5.0%→8% · +8.0%→1%
- Range intraday médian 4.09% (p90 6.5%) · excursion haute méd. +1.72% / basse méd. −1.92%
- Profil de vol intra : ouverture 2.643% vs midi 1.227% vs clôture 1.2% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 94% · range 6% · trend ↑0%/↓0% ; spike-down 65% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.104 ; mean-reverting — autocorr -0.139)_ ; drift intra méd. -0.506% ; recovery-V 28%
- **σ réalisé intraday** 3.475% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 81% / whipsaw 51%
- POC intraday (dernière séance, temps-au-prix) : 2.7892 (VA 2.7604–2.8204 ; dernier close 2.806)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 28% · rebond 80% · **stop −2.37%** sous le fill (sous le bruit) · cible +1.91% · R/R 0.81 (high win-rate)
- Gaps overnight (n=159) : méd. 0.35% · baisse 41% (gap-down >1% 10% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −2.26%) · haut méd +0.43% · range méd 1.65%
- Excursion ouverture 15min (n=160) : bas méd −0.96% (p90 −2.47%) · haut méd +0.78% · range méd 1.98%
- Excursion ouverture 30min (n=160) : bas méd −1.16% (p90 −2.82%) · haut méd +1.06% · range méd 2.33%
- Excursion ouverture 60min (n=160) : bas méd −1.26% (p90 −3.16%) · haut méd +1.11% · range méd 2.71%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2.81 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 84% (129/159) · gap 21% · délai 0.3min · rebond 63% (86/129) (MFE +1.64%)
   - −1.0% : fill 30min 42% · séance 72% (112/159) · gap 10% · délai 4.8min · rebond 65% (76/112) (MFE +1.44%)
   - −1.5% : fill 30min 28% · séance 56% (91/159) · gap 5% · délai 30.8min · rebond 68% (61/91) (MFE +1.46%)
   - −2.0% : fill 30min 19% · séance 47% (76/159) · gap 4% · délai 68.0min · rebond 60% (45/76) (MFE +1.59%)
   - −3.0% : fill 30min 8% · séance 28% (44/159) · gap 2% · délai 112.8min · rebond 80% (32/44) (MFE +1.91%)
   - −4.0% : fill 30min 2% · séance 12% (20/159) · gap 0% · délai 390.8min · rebond 36% (10/20) (MFE +0.51%)
   - −5.0% : fill 30min 1% · séance 6% (11/159) · gap 0% · délai 215.4min · rebond 14% (5/11) (MFE +0.65%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.41% (p90 −2.43%) → stop au-delà de −1.71% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.37% (p90 −2.02%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.31% (p90 −2.0%) → stop au-delà de −1.73% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=832 jambes) : jambe baissière méd −1.06% (p90 −2.31%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 80% (41/49) · rebond 67% (29/41)
      · −2.0% : fill 63% (32/49) · rebond 69% (20/32)
      · −3.0% : fill 36% (19/49) · rebond 79% (13/19)
      · −4.0% : fill 15% (10/49) · rebond 15% (4/10)
      · −5.0% : fill 12% (7/49) · rebond 15% (3/7)
   - **flat** (32 séances) :
      · −1.0% : fill 75% (25/32) · rebond 70% (16/25)
      · −2.0% : fill 50% (18/32) · rebond 65% (10/18)
      · −3.0% : fill 36% (11/32) · rebond 90% (9/11)
      · −4.0% : fill 14% (4/32) · rebond 60% (2/4)
      · −5.0% : fill 4% (2/32) · rebond 23% (1/2)
   - **gap-up** (78 séances) :
      · −1.0% : fill 67% (46/78) · rebond 61% (31/46)
      · −2.0% : fill 38% (26/78) · rebond 50% (15/26)
      · −3.0% : fill 20% (14/78) · rebond 73% (10/14)
      · −4.0% : fill 9% (6/78) · rebond 36% (4/6)
      · −5.0% : fill 3% (2/78) · rebond 7% (1/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 56% si les 15 1res min sont vertes (79 cas) · 28% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **5min** → P(séance verte=clôture>ouverture) 66% si début vert vs 22% si rouge (base 42% · écart 44 pts) ; prédictivité sature ensuite (plafond brut 281min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **66%** · continue >prix actuel 46% ; creux résiduel méd -1.84% (q20 -2.76%) → **SL/trailing à −2.76%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.97% / q75 +2.56% → **scale +1.97% / runner +2.56%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **22%** (continue à baisser 66%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.22%** (au-delà de la MAE q10 -4.22%), cible rebond +1.56% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.63% .. +3.32%] · haut q95 +3.93% · bas q05 -3.48%
   - 60min (n=160) : retour [-2.85% .. +3.84%] · haut q95 +4.96% · bas q05 -3.74%
   - 2h (n=160) : retour [-2.98% .. +3.29%] · haut q95 +5.01% · bas q05 -3.91%
   - 4h (n=160) : retour [-3.29% .. +3.8%] · haut q95 +5.1% · bas q05 -4.32%
   - 6h (n=160) : retour [-3.66% .. +4.62%] · haut q95 +5.27% · bas q05 -4.33%
   - session (n=160) : retour [-4.52% .. +4.02%] · haut q95 +5.67% · bas q05 -5.32%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 3.11%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 1.25/2 | R/R T1 : 2.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.1 · part idiosyncratique 0.91
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-10 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-10 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-10 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 77.5  _(surachat)_
- **ADX** : 15.6  _(pas de tendance nette)_
- **MACD** : hist 0.048  _(pas de croisement recent)_
- **BB** : %B 0.99 · largeur 28.0%
- **ATR** : 0.13 (10.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.049  _(neutre)_
- **Vol ratio** : 1.23  _(volume normal)_
- **Choppiness** : 41.5  _(transition)_
- **MA** : MA20 2.78 · MA50 2.9 · MA200 4.3  _(prix > MA20)_
- **Dist MA** : MA20 +13.7% · MA50 +9.2% · MA200 -26.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (731503 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
