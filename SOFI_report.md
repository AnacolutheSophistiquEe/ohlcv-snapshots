# SOFI

**Generated** : 2026-11-05T01:33:18.105037+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 8/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $17.39  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-06 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $17.39 (+0.4% vs entrée) · entrée $17.32 · stop $17.06 · T1 $17.74 · R/R 1.62  
> ↳ _probas brutes, non calibrées · n=0_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -4.6 % ≠ (strike 16.0 − spot 17.39)/spot = -8.0 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : triple_bullish (score 3)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-04 : 17.39 · ATR Wilder 0.7813 (4.49 %)_
- **Swing** : plage **16.37 → 15.8** (-5.84 % a -9.12 % sous la cloture, 0.73 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 16.25-16.61 (B). stop INDICATIF 15.11 (-4.39 % sous le bas ; sous le support 15.5-15.65 (- 0,5 ATR)).
- **Deep** : plage **15.8 → 14.35** (-9.12 % a -17.5 % sous la cloture, 1.87 ATR) — touchee 46 % → 15 % du temps en 20 seances ; supports reels dans la plage : 14.42-15.67 (B) ; 15.5-15.65 (B) ; 14.85-15.22 (B). stop INDICATIF 13.47 (-6.11 % sous le bas ; sous le support 13.86-13.9 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (0.45 ATR sous le plus haut 20 s., RSI(2) 84.1 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 16.68-16.93 (B, -2.65 %) ; 16.25-16.61 (B, -4.49 %) ; 14.42-15.67 (B, -9.89 %) ; 15.5-15.65 (B, -10.0 %) ; 14.85-15.22 (B, -12.48 %) ; 13.86-13.9 (A, -20.07 %)
- Resistances reelles au-dessus : 18.42-18.8 (A, 5.92 %) ; 18.86-19.19 (A, 8.45 %) ; 19.48-19.82 (A, 12.02 %) ; 20.13-20.43 (A, 15.76 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=5.91 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (5.49 %)** : le gap seul le franchit 1.676 % des séances (21 fois sur 1253).
   - exécution **1.342 pt plus bas** dans le cas TYPIQUE (médiane), 4.286 au p90, **5.615 au pire**
   - perte réelle **7.442 %** en moyenne _(tirée par la queue)_, jusqu'à **11.105 %** — au lieu des 5.49 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0327 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.204 % | p01 -6.52 % | pire -11.105 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5431** [0.4687 ; 0.6161] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4655** [0.4134 ; 0.5182] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.354** [0.305 ; 0.4055] _(largeur 10.0 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.22 %** | CVaR **-8.65 %** | vol 4.1 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.5 % vs -14.29 % si l'on extrapolait par √5 _(rapport 1.015 ; < 1 = le √5 surestime)_
- **β de baisse : 1.797** (β de hausse 1.7013, asymétrie 1.0563) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.289× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 16.1327 sur atr_based (1.5 ATR, 7.23 %) — p(stop avant cible) 0.4955 [0.44 ; 0.55], R/R 5.967, perte reelle 7.554 % (gap inclus), CVaR 10.152 %, EV -0.7603 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.9967 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.13 ATR (stop 2.879 %) — p(stop avant cible) 0.8467 [0.81 ; 0.88], R/R 14.621, perte reelle 3.083 % (gap inclus), EV -0.8976 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 14.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.847, borne haute 0.882 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.90 %) : P(cible) 0.0 % x 45.08 % + P(rien) 15.3 % x 11.08 % ne couvrent pas P(stop) 84.7 % x 3.08 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_based a 1.5 ATR (stop 7.23 %) — p(stop avant cible) 0.4955 [0.44 ; 0.55], R/R 5.967, perte reelle 7.554 % (gap inclus), EV -0.7603 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.76 %) : P(cible) 0.1 % x 45.08 % + P(rien) 50.4 % x 5.87 % ne couvrent pas P(stop) 49.5 % x 7.55 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🟢 support a 2.99 ATR (stop 16.665 %) — p(stop avant cible) 0.0665 [0.04 ; 0.10], R/R 2.681, perte reelle 16.811 % (gap inclus), EV -0.2047 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.86 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 0.1 % x 45.08 % + P(rien) 93.3 % x 0.95 % ne couvrent pas P(stop) 6.7 % x 16.81 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🟢 support a 4.21 ATR (stop 22.531 %) — p(stop avant cible) 0.0262 [0.01 ; 0.05], R/R 1.987, perte reelle 22.685 % (gap inclus), EV -0.2465 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.00 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.25 %) : P(cible) 0.1 % x 45.08 % + P(rien) 97.3 % x 0.33 % ne couvrent pas P(stop) 2.6 % x 22.68 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ grid_snapped a 0.13 ATR (stop 2.093 %) — p(stop avant cible) 0.8885 [0.85 ; 0.92], R/R 19.679, perte reelle 2.29 % (gap inclus), EV -0.5826 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 19.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.888, borne haute 0.918 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.58 %) : P(cible) 0.0 % x 45.08 % + P(rien) 11.1 % x 12.94 % ne couvrent pas P(stop) 88.8 % x 2.29 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.75 ATR (stop 3.615 %) — p(stop avant cible) 0.7693 [0.72 ; 0.81], R/R 11.615, perte reelle 3.881 % (gap inclus), EV -0.931 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 11.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.769, borne haute 0.811 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.93 %) : P(cible) 0.0 % x 45.08 % + P(rien) 23.0 % x 8.84 % ne couvrent pas P(stop) 76.9 % x 3.88 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.0 ATR (stop 4.82 %) — p(stop avant cible) 0.6774 [0.63 ; 0.72], R/R 8.773, perte reelle 5.138 % (gap inclus), EV -0.7488 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 8.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.677, borne haute 0.725 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.75 %) : P(cible) 0.0 % x 45.08 % + P(rien) 32.2 % x 8.42 % ne couvrent pas P(stop) 67.7 % x 5.14 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.25 ATR (stop 6.025 %) — p(stop avant cible) 0.5868 [0.53 ; 0.64], R/R 7.135, perte reelle 6.318 % (gap inclus), EV -0.777 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 7.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.587, borne haute 0.638 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.78 %) : P(cible) 0.1 % x 45.08 % + P(rien) 41.3 % x 7.05 % ne couvrent pas P(stop) 58.7 % x 6.32 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.75 ATR (stop 8.435 %) — p(stop avant cible) 0.4196 [0.37 ; 0.47], R/R 5.138, perte reelle 8.773 % (gap inclus), EV -0.8594 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.86 %) : P(cible) 0.1 % x 45.08 % + P(rien) 58.0 % x 4.83 % ne couvrent pas P(stop) 42.0 % x 8.77 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.0 ATR (stop 9.64 %) — p(stop avant cible) 0.3596 [0.31 ; 0.41], R/R 4.487, perte reelle 10.047 % (gap inclus), EV -1.102 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.38 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.10 %) : P(cible) 0.1 % x 45.08 % + P(rien) 64.0 % x 3.89 % ne couvrent pas P(stop) 36.0 % x 10.05 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.25 ATR (stop 10.845 %) — p(stop avant cible) 0.2917 [0.25 ; 0.34], R/R 4.032, perte reelle 11.181 % (gap inclus), EV -0.9735 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.77 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.97 %) : P(cible) 0.1 % x 45.08 % + P(rien) 70.8 % x 3.20 % ne couvrent pas P(stop) 29.2 % x 11.18 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.5 ATR (stop 12.05 %) — p(stop avant cible) 0.2267 [0.18 ; 0.27], R/R 3.658, perte reelle 12.323 % (gap inclus), EV -0.7754 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.29 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.78 %) : P(cible) 0.1 % x 45.08 % + P(rien) 77.3 % x 2.58 % ne couvrent pas P(stop) 22.7 % x 12.32 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🟢 grid_snapped a 2.99 ATR (stop 15.88 %) — p(stop avant cible) 0.0826 [0.06 ; 0.12], R/R 2.82, perte reelle 15.985 % (gap inclus), EV -0.202 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.05 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 0.1 % x 45.08 % + P(rien) 91.7 % x 1.20 % ne couvrent pas P(stop) 8.3 % x 15.98 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🟢 grid_snapped a 4.21 ATR (stop 21.745 %) — p(stop avant cible) 0.0282 [0.01 ; 0.05], R/R 2.063, perte reelle 21.852 % (gap inclus), EV -0.2451 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.81 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.25 %) : P(cible) 0.1 % x 45.08 % + P(rien) 97.1 % x 0.36 % ne couvrent pas P(stop) 2.8 % x 21.85 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 5.0 ATR (stop 24.1 %) — p(stop avant cible) 0.0191 [0.01 ; 0.04], R/R 1.853, perte reelle 24.327 % (gap inclus), EV -0.2355 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.02 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.24 %) : P(cible) 0.1 % x 45.08 % + P(rien) 98.0 % x 0.21 % ne couvrent pas P(stop) 1.9 % x 24.33 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 5.5 ATR (stop 26.511 %) — p(stop avant cible) 0.0037 [0.00 ; 0.01], R/R 1.682, perte reelle 26.805 % (gap inclus), EV -0.1346 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.51 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 0.1 % x 45.08 % + P(rien) 99.6 % x -0.06 % ne couvrent pas P(stop) 0.4 % x 26.80 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 6.0 ATR (stop 28.921 %) — p(stop avant cible) 0.0025 [0.00 ; 0.01], R/R 1.558, perte reelle 28.937 % (gap inclus), EV -0.1281 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.41 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 0.1 % x 45.08 % + P(rien) 99.7 % x -0.08 % ne couvrent pas P(stop) 0.2 % x 28.94 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 6.5 ATR (stop 31.331 %) — p(stop avant cible) 0.0024 [0.00 ; 0.01], R/R 1.439, perte reelle 31.331 % (gap inclus), EV -0.1324 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.51 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 0.1 % x 45.08 % + P(rien) 99.7 % x -0.08 % ne couvrent pas P(stop) 0.2 % x 31.33 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 7.0 ATR (stop 33.741 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 1.336, perte reelle 33.741 % (gap inclus), EV -0.1201 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.33 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 0.1 % x 45.08 % + P(rien) 99.8 % x -0.10 % ne couvrent pas P(stop) 0.1 % x 33.74 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 7.5 ATR (stop 36.151 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 1.244, perte reelle 36.247 % (gap inclus), EV -0.1233 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.39 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 0.1 % x 45.08 % + P(rien) 99.8 % x -0.10 % ne couvrent pas P(stop) 0.1 % x 36.25 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 8.0 ATR (stop 38.561 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.169, perte reelle 38.561 % (gap inclus), EV -0.1138 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.22 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.11 %) : P(cible) 0.1 % x 45.08 % + P(rien) 100.0 % x -0.14 % ne couvrent pas P(stop) 0.0 % x 38.56 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 17.39, ATR14 0.8382 (4.82 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.377 ATR = 1.817 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.241 % | 17.3481 | 92.85 % | 95.77 % | 97.17 % | 97.47 % | 98.17 % | 98.87 % |
| 0.1 ATR | 0.482 % | 17.3062 | 84.99 % | 89.31 % | 92.13 % | 93.33 % | 95.33 % | 97.13 % |
| 0.15 ATR | 0.723 % | 17.2643 | 78.75 % | 84.58 % | 87.99 % | 90.29 % | 92.68 % | 94.87 % |
| 0.2 ATR | 0.964 % | 17.2224 | 71.5 % | 79.33 % | 83.35 % | 86.75 % | 90.35 % | 93.33 % |
| 0.25 ATR | 1.205 % | 17.1804 | 66.16 % | 75.1 % | 80.22 % | 84.43 % | 89.13 % | 92.2 % |
| 0.35 ATR | 1.687 % | 17.0966 | 52.77 % | 65.42 % | 72.35 % | 78.67 % | 85.67 % | 89.01 % |
| 0.5 ATR | 2.41 % | 16.9709 | 37.36 % | 53.33 % | 61.65 % | 69.36 % | 79.67 % | 84.91 % |
| 0.75 ATR | 3.615 % | 16.7613 | 20.34 % | 36.79 % | 46.62 % | 57.23 % | 70.33 % | 78.44 % |
| 1.0 ATR | 4.82 % | 16.5518 | 8.66 % | 24.29 % | 33.7 % | 44.99 % | 60.06 % | 69.92 % |
| 1.25 ATR | 6.025 % | 16.3422 | 4.13 % | 15.12 % | 24.12 % | 35.69 % | 51.22 % | 63.45 % |
| 1.5 ATR | 7.23 % | 16.1327 | 1.91 % | 9.38 % | 16.55 % | 27.2 % | 43.39 % | 57.19 % |
| 2.0 ATR | 9.64 % | 15.7136 | 0.6 % | 4.54 % | 8.58 % | 15.47 % | 30.08 % | 46.2 % |
| 2.5 ATR | 12.05 % | 15.2945 | 0.3 % | 1.92 % | 4.04 % | 9.61 % | 20.33 % | 36.65 % |
| 3.0 ATR | 14.46 % | 14.8754 | 0.1 % | 0.81 % | 2.83 % | 6.17 % | 14.02 % | 29.16 % |
| 4.0 ATR | 19.28 % | 14.0371 | 0.0 % | 0.3 % | 0.61 % | 2.43 % | 7.22 % | 15.09 % |
| 6.0 ATR | 28.921 % | 12.3607 | 0.0 % | 0.1 % | 0.2 % | 0.2 % | 0.91 % | 3.18 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.56 ATR | 0.68 ATR | 0.76 ATR | 0.97 ATR | 1.20 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.63 ATR | 0.83 ATR | 0.99 ATR | 1.12 ATR | 1.47 ATR | 1.95 ATR |
| **3 s.** | 0.32 ATR | 0.69 ATR | 0.78 ATR | 1.02 ATR | 1.23 ATR | 1.39 ATR | 1.91 ATR | 2.39 ATR |
| **5 s.** | 0.41 ATR | 0.90 ATR | 1.00 ATR | 1.33 ATR | 1.59 ATR | 1.81 ATR | 2.47 ATR | 3.31 ATR |
| **10 s.** | 0.62 ATR | 1.29 ATR | 1.45 ATR | 1.89 ATR | 2.26 ATR | 2.53 ATR | 3.59 ATR | 4.70 ATR |
| **20 s.** | 0.85 ATR | 1.83 ATR | 2.06 ATR | 2.74 ATR | 3.30 ATR | 3.65 ATR | 4.86 ATR | 5.69 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.426–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.41 %, prix 16.9709), p(touche) 37.36 % (en stress 83.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.626–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.615 %, prix 16.7614), p(touche) 36.79 % (en stress 91.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 21.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.781–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.82 %, prix 16.5518), p(touche) 33.7 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.0–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.82 %, prix 16.5518), p(touche) 44.99 % (en stress 96.97 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.449–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.23 %, prix 16.1327), p(touche) 43.39 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.063–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (12.05 %, prix 15.2945), p(touche) 36.65 % (en stress 98.98 %)  ✅ optimum identifie (77.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 70.2 | bear 17.2 | side 12.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 511.0 (= 33 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.386% → cible +2.419% / stop −1.5%, p_fill 84%, n_eff≈91.8) : P(cible|rempli) **18%** · **EV/risk -0.271** (×p_fill ; si rempli -0.48% du capital)
  - **swing** (entrée dip −0.67% → cible +6.942% / stop −4.853%, p_fill 87%, n_eff≈101.7) : P(cible|rempli) **20%** · **EV/risk -0.209** (×p_fill ; si rempli -1.17% du capital)
  - **deep** (entrée dip −0.892% → cible +19.511% / stop −9.755%, p_fill 90%, n_eff≈101.0) : P(cible|rempli) **5%** · **EV/risk -0.198** (×p_fill ; si rempli -2.13% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→65% · +2.0%→42% · +3.0%→31% · +5.0%→10% · +8.0%→2%
- Range intraday médian 4.0% (p90 6.7%) · excursion haute méd. +1.55% / basse méd. −2.04%
- Profil de vol intra : ouverture 2.79% vs midi 0.796% vs clôture 0.916% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 21% · trend ↑2%/↓0% ; spike-down 58% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.156 ; mean-reverting — autocorr -0.042)_ ; drift intra méd. -0.193% ; recovery-V 30%
- **σ réalisé intraday** 2.295% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 53% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 14.6352 (VA 14.5663–14.6583 ; dernier close 14.62)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 44% · rebond 65% · **stop −2.96%** sous le fill (sous le bruit) · cible +1.55% · R/R 0.52 (high win-rate)
- Gaps overnight (n=159) : méd. 0.0% · baisse 50% (gap-down >1% 27% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.59% (p90 −1.66%) · haut méd +0.66% · range méd 1.44%
- Excursion ouverture 15min (n=160) : bas méd −0.81% (p90 −2.19%) · haut méd +0.86% · range méd 2.02%
- Excursion ouverture 30min (n=160) : bas méd −1.03% (p90 −3.07%) · haut méd +0.91% · range méd 2.35%
- Excursion ouverture 60min (n=160) : bas méd −1.13% (p90 −3.56%) · haut méd +1.02% · range méd 2.79%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 14.615 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 79% (121/159) · gap 37% · délai 0.0min · rebond 52% (68/121) (MFE +1.12%)
   - −1.0% : fill 30min 50% · séance 64% (103/159) · gap 27% · délai 0.9min · rebond 44% (52/103) (MFE +0.88%)
   - −1.5% : fill 30min 42% · séance 56% (92/159) · gap 22% · délai 1.2min · rebond 61% (59/92) (MFE +1.28%)
   - −2.0% : fill 30min 31% · séance 44% (71/159) · gap 10% · délai 2.8min · rebond 65% (48/71) (MFE +1.55%)
   - −3.0% : fill 30min 8% · séance 29% (49/159) · gap 1% · délai 68.9min · rebond 44% (28/49) (MFE +0.9%)
   - −4.0% : fill 30min 5% · séance 14% (27/159) · gap 1% · délai 91.2min · rebond 47% (16/27) (MFE +0.59%)
   - −5.0% : fill 30min 1% · séance 8% (13/159) · gap 1% · délai 214.3min · rebond 45% (6/13) (MFE +0.64%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.39% (p90 −1.8%) → stop au-delà de −1.24% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.25% (p90 −1.74%) → stop au-delà de −1.2% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.22% (p90 −1.25%) → stop au-delà de −0.84% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=576 jambes) : jambe baissière méd −1.02% (p90 −2.7%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (62 séances) :
      · −1.0% : fill 91% (59/62) · rebond 42% (30/59)
      · −2.0% : fill 79% (51/62) · rebond 72% (35/51)
      · −3.0% : fill 50% (35/62) · rebond 45% (21/35)
      · −4.0% : fill 26% (21/62) · rebond 58% (14/21)
      · −5.0% : fill 13% (10/62) · rebond 34% (4/10)
   - **flat** (24 séances) :
      · −1.0% : fill 73% (16/24) · rebond 26% (5/16)
      · −2.0% : fill 42% (9/24) · rebond 40% (5/9)
      · −3.0% : fill 38% (8/24) · rebond 32% (3/8)
      · −4.0% : fill 19% (4/24) · rebond 15% (1/4)
      · −5.0% : fill 15% (2/24) · rebond 64% (1/2)
   - **gap-up** (73 séances) :
      · −1.0% : fill 35% (28/73) · rebond 63% (17/28)
      · −2.0% : fill 11% (11/73) · rebond 56% (8/11)
      · −3.0% : fill 6% (6/73) · rebond 60% (4/6)
      · −4.0% : fill 2% (2/73) · rebond 20% (1/2)
      · −5.0% : fill 0% (1/73) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 70% si les 15 1res min sont vertes (75 cas) · 25% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **28min** → P(séance verte=clôture>ouverture) 76% si début vert vs 18% si rouge (base 46% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 215min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **76%** · continue >prix actuel 49% ; creux résiduel méd -1.53% (q20 -2.61%) → **SL/trailing à −2.61%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.24% / q75 +2.49% → **scale +1.24% / runner +2.49%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **18%** (continue à baisser 64%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.81%** (au-delà de la MAE q10 -2.81%), cible rebond +1.0% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.87% .. +3.38%] · haut q95 +3.7% · bas q05 -3.56%
   - 60min (n=160) : retour [-3.14% .. +4.07%] · haut q95 +4.61% · bas q05 -4.01%
   - 2h (n=160) : retour [-3.61% .. +4.53%] · haut q95 +5.04% · bas q05 -4.49%
   - 4h (n=160) : retour [-3.96% .. +4.31%] · haut q95 +5.5% · bas q05 -5.12%
   - 6h (n=160) : retour [-4.61% .. +4.09%] · haut q95 +5.63% · bas q05 -5.18%
   - session (n=160) : retour [-4.53% .. +4.64%] · haut q95 +5.63% · bas q05 -5.28%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (4) pour des stats fiables : 2.5% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.71%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.39 · part idiosyncratique 0.61
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-06 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-06 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-06 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 67.0  _(momentum haussier)_
- **ADX** : 26.3  _(tendance etablie)_
- **MACD** : hist 0.316  _(pas de croisement recent)_
- **BB** : %B 0.9 · largeur 28.5%
- **ATR** : 0.84 (32.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.106  _(accumulation)_
- **Vol ratio** : 0.92  _(volume normal)_
- **Choppiness** : 45.2  _(transition)_
- **MA** : MA20 15.61 · MA50 16.47 · MA200 17.65  _(prix > MA20)_
- **Dist MA** : MA20 +11.4% · MA50 +5.6% · MA200 -1.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (753485 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
