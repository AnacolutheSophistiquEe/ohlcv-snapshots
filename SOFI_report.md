# SOFI

**Generated** : 2026-10-16T00:32:17.199355+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $15.07  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 20/125 fenêtres (p_fill pondéré 14 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot $15.07 (+3.9% vs entrée) · entrée $14.50 · stop $14.22 · T1 $15.07 · R/R 2.04  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.95% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +9.0 % ≠ (strike 15.5 − spot 15.07)/spot = +2.9 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -146 % hors [0,100] (R² max 0.16). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-15 : 15.07 · ATR Wilder 0.6462 (4.29 %)_
- **Swing** : plage **14.23 → 13.77** (-5.57 % a -8.65 % sous la cloture, 0.72 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 13.75-13.9 (B). stop INDICATIF 13.1 (-4.87 % sous le bas ; sous le support 13.42-13.6 (- 0,5 ATR)).
- **Deep** : plage **13.77 → 12.57** (-8.65 % a -16.6 % sous la cloture, 1.85 ATR) — touchee 45 % → 15 % du temps en 20 seances ; supports reels dans la plage : 13.75-13.9 (B) ; 13.42-13.6 (C) ; 12.86-13.01 (B) ; 12.5-12.74 (A). stop INDICATIF 11.92 (-5.14 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- ACHAT PAS CHER : inactif (4.47 ATR sous le plus haut 20 s., RSI(2) 59.6 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 14.42-14.68 (B, -2.59 %) ; 13.75-13.9 (B, -7.76 %) ; 13.42-13.6 (C, -9.75 %) ; 12.86-13.01 (B, -13.67 %) ; 12.5-12.74 (A, -15.46 %) ; 11.43-11.65 (B, -22.7 %)
- Resistances reelles au-dessus : 15.53-15.65 (A, 3.05 %) ; 16.25-16.53 (A, 7.83 %) ; 16.61-16.93 (A, 10.22 %) ; 17.08-17.19 (A, 13.34 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=5.83 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (11.33 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1253).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 11.33 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.204 % | p01 -6.52 % | pire -11.105 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.474** [0.4006 ; 0.5483] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.5703** [0.5177 ; 0.6217] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.5378** [0.4851 ; 0.5899] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (43.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1140 séances)** : VaR **-6.08 %** | CVaR **-8.5 %** | vol 4.02 %/j
   - _fenêtre arrêtée : rupture de regime a 1200 seances en arriere (volatilite 5.77 % contre 3.51 % aujourd'hui, rapport 1.65)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.5 % vs -14.29 % si l'on extrapolait par √5 _(rapport 1.015 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7987** (β de hausse 1.7187, asymétrie 1.0465) vs IWM — 605 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.362× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 14.0739 sur atr_grid (1.75 ATR, 6.61 %) — p(stop avant cible) 0.5219 [0.47 ; 0.57], R/R 2.762, perte reelle 6.873 % (gap inclus), CVaR 9.037 %, EV -0.6936 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.5133 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 9.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.522, borne haute 0.574 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.666 %) — p(stop avant cible) 0.6085 [0.56 ; 0.66], R/R 3.153, perte reelle 6.02 % (gap inclus), EV -0.7444 % — **REFUSE**
      - refuse : cible atteinte seulement 8.9 % du temps (< 15 %) meme a 10 seances : le R/R de 3.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.609, borne haute 0.659 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.74 %) : P(cible) 8.9 % x 18.98 % + P(rien) 30.2 % x 4.04 % ne couvrent pas P(stop) 60.9 % x 6.02 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 0.944 %) — p(stop avant cible) 0.9423 [0.91 ; 0.96], R/R 18.763, perte reelle 1.012 % (gap inclus), EV -0.168 % — **REFUSE**
      - refuse : cible atteinte seulement 2.7 % du temps (< 15 %) meme a 10 seances : le R/R de 18.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.942, borne haute 0.963 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 2.7 % x 18.98 % + P(rien) 3.1 % x 9.01 % ne couvrent pas P(stop) 94.2 % x 1.01 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 1.889 %) — p(stop avant cible) 0.9049 [0.87 ; 0.93], R/R 9.104, perte reelle 2.085 % (gap inclus), EV -0.6672 % — **REFUSE**
      - refuse : cible atteinte seulement 4.3 % du temps (< 15 %) meme a 10 seances : le R/R de 9.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.905, borne haute 0.932 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.67 %) : P(cible) 4.3 % x 18.98 % + P(rien) 5.2 % x 7.73 % ne couvrent pas P(stop) 90.5 % x 2.09 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 2.833 %) — p(stop avant cible) 0.8472 [0.81 ; 0.88], R/R 6.234, perte reelle 3.045 % (gap inclus), EV -0.9084 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 6.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.847, borne haute 0.882 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.91 %) : P(cible) 5.7 % x 18.98 % + P(rien) 9.6 % x 6.16 % ne couvrent pas P(stop) 84.7 % x 3.04 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 3.777 %) — p(stop avant cible) 0.7465 [0.70 ; 0.79], R/R 4.654, perte reelle 4.079 % (gap inclus), EV -0.752 % — **REFUSE**
      - refuse : cible atteinte seulement 7.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.747, borne haute 0.790 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.75 %) : P(cible) 7.1 % x 18.98 % + P(rien) 18.3 % x 5.18 % ne couvrent pas P(stop) 74.7 % x 4.08 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 4.721 %) — p(stop avant cible) 0.6847 [0.63 ; 0.73], R/R 3.742, perte reelle 5.073 % (gap inclus), EV -0.7439 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.685, borne haute 0.732 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.74 %) : P(cible) 8.6 % x 18.98 % + P(rien) 22.9 % x 4.75 % ne couvrent pas P(stop) 68.5 % x 5.07 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 6.61 %) — p(stop avant cible) 0.5219 [0.47 ; 0.57], R/R 2.762, perte reelle 6.873 % (gap inclus), EV -0.6936 % — **REFUSE**
      - refuse : cible atteinte seulement 9.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.522, borne haute 0.574 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.69 %) : P(cible) 9.2 % x 18.98 % + P(rien) 38.7 % x 2.99 % ne couvrent pas P(stop) 52.2 % x 6.87 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 7.554 %) — p(stop avant cible) 0.4726 [0.42 ; 0.53], R/R 2.396, perte reelle 7.921 % (gap inclus), EV -0.8899 % — **REFUSE**
      - refuse : cible atteinte seulement 9.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.89 %) : P(cible) 9.2 % x 18.98 % + P(rien) 43.5 % x 2.54 % ne couvrent pas P(stop) 47.3 % x 7.92 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 8.499 %) — p(stop avant cible) 0.4135 [0.36 ; 0.47], R/R 2.141, perte reelle 8.866 % (gap inclus), EV -0.9313 % — **REFUSE**
      - refuse : cible atteinte seulement 9.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.93 %) : P(cible) 9.2 % x 18.98 % + P(rien) 49.4 % x 1.99 % ne couvrent pas P(stop) 41.3 % x 8.87 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 9.443 %) — p(stop avant cible) 0.3552 [0.31 ; 0.41], R/R 1.914, perte reelle 9.918 % (gap inclus), EV -1.103 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.51 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.10 %) : P(cible) 9.3 % x 18.98 % + P(rien) 55.2 % x 1.20 % ne couvrent pas P(stop) 35.5 % x 9.92 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 10.387 %) — p(stop avant cible) 0.3046 [0.26 ; 0.35], R/R 1.757, perte reelle 10.803 % (gap inclus), EV -1.0087 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.83 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.01 %) : P(cible) 9.3 % x 18.98 % + P(rien) 60.3 % x 0.87 % ne couvrent pas P(stop) 30.5 % x 10.80 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 11.331 %) — p(stop avant cible) 0.26 [0.22 ; 0.31], R/R 1.624, perte reelle 11.688 % (gap inclus), EV -0.9123 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.17 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.91 %) : P(cible) 9.3 % x 18.98 % + P(rien) 64.7 % x 0.55 % ne couvrent pas P(stop) 26.0 % x 11.69 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 13.22 %) — p(stop avant cible) 0.1737 [0.14 ; 0.22], R/R 1.407, perte reelle 13.49 % (gap inclus), EV -0.5262 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.16 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 9.3 % x 18.98 % + P(rien) 73.3 % x 0.07 % ne couvrent pas P(stop) 17.4 % x 13.49 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 15.109 %) — p(stop avant cible) 0.1118 [0.08 ; 0.15], R/R 1.244, perte reelle 15.258 % (gap inclus), EV -0.3701 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.44 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.37 %) : P(cible) 9.3 % x 18.98 % + P(rien) 79.5 % x -0.55 % ne couvrent pas P(stop) 11.2 % x 15.26 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 16.997 %) — p(stop avant cible) 0.0692 [0.05 ; 0.10], R/R 1.109, perte reelle 17.123 % (gap inclus), EV -0.2771 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.17 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.28 %) : P(cible) 9.3 % x 18.98 % + P(rien) 83.8 % x -1.03 % ne couvrent pas P(stop) 6.9 % x 17.12 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 18.886 %) — p(stop avant cible) 0.0522 [0.03 ; 0.08], R/R 1.002, perte reelle 18.937 % (gap inclus), EV -0.2827 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.94 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.28 %) : P(cible) 9.3 % x 18.98 % + P(rien) 85.5 % x -1.24 % ne couvrent pas P(stop) 5.2 % x 18.94 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 20.774 %) — p(stop avant cible) 0.0381 [0.02 ; 0.06], R/R 0.908, perte reelle 20.895 % (gap inclus), EV -0.3074 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.88 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.31 %) : P(cible) 9.3 % x 18.98 % + P(rien) 86.9 % x -1.47 % ne couvrent pas P(stop) 3.8 % x 20.90 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 22.663 %) — p(stop avant cible) 0.0278 [0.01 ; 0.05], R/R 0.832, perte reelle 22.81 % (gap inclus), EV -0.3267 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.48 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 9.3 % x 18.98 % + P(rien) 87.9 % x -1.66 % ne couvrent pas P(stop) 2.8 % x 22.81 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 24.551 %) — p(stop avant cible) 0.0206 [0.01 ; 0.04], R/R 0.768, perte reelle 24.714 % (gap inclus), EV -0.3204 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.61 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.32 %) : P(cible) 9.3 % x 18.98 % + P(rien) 88.6 % x -1.78 % ne couvrent pas P(stop) 2.1 % x 24.71 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 26.44 %) — p(stop avant cible) 0.004 [0.00 ; 0.02], R/R 0.709, perte reelle 26.758 % (gap inclus), EV -0.2035 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.83 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 9.3 % x 18.98 % + P(rien) 90.3 % x -2.07 % ne couvrent pas P(stop) 0.4 % x 26.76 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 28.329 %) — p(stop avant cible) 0.0034 [0.00 ; 0.01], R/R 0.67, perte reelle 28.346 % (gap inclus), EV -0.2062 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.88 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.21 %) : P(cible) 9.3 % x 18.98 % + P(rien) 90.3 % x -2.08 % ne couvrent pas P(stop) 0.3 % x 28.35 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 30.217 %) — p(stop avant cible) 0.0026 [0.00 ; 0.01], R/R 0.626, perte reelle 30.338 % (gap inclus), EV -0.1989 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.79 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 9.3 % x 18.98 % + P(rien) 90.4 % x -2.09 % ne couvrent pas P(stop) 0.3 % x 30.34 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 15.07, ATR14 0.5692 (3.777 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.379 ATR = 1.432 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.189 % | 15.0415 | 93.05 % | 95.87 % | 97.17 % | 97.57 % | 98.27 % | 98.87 % |
| 0.1 ATR | 0.378 % | 15.0131 | 85.3 % | 89.42 % | 92.13 % | 93.43 % | 95.53 % | 97.13 % |
| 0.15 ATR | 0.567 % | 14.9846 | 79.05 % | 84.68 % | 88.09 % | 90.5 % | 92.89 % | 94.87 % |
| 0.2 ATR | 0.755 % | 14.9562 | 71.8 % | 79.44 % | 83.45 % | 86.96 % | 90.55 % | 93.33 % |
| 0.25 ATR | 0.944 % | 14.9277 | 66.47 % | 75.2 % | 80.32 % | 84.53 % | 89.23 % | 92.2 % |
| 0.35 ATR | 1.322 % | 14.8708 | 52.97 % | 65.42 % | 72.35 % | 78.77 % | 85.77 % | 89.01 % |
| 0.5 ATR | 1.889 % | 14.7854 | 37.66 % | 53.33 % | 61.76 % | 69.57 % | 79.78 % | 84.91 % |
| 0.75 ATR | 2.833 % | 14.6431 | 20.44 % | 37.0 % | 46.92 % | 57.43 % | 70.43 % | 78.44 % |
| 1.0 ATR | 3.777 % | 14.5008 | 8.86 % | 24.6 % | 34.11 % | 45.3 % | 60.26 % | 69.92 % |
| 1.25 ATR | 4.721 % | 14.3585 | 4.33 % | 15.22 % | 24.32 % | 35.89 % | 51.22 % | 63.45 % |
| 1.5 ATR | 5.666 % | 14.2162 | 2.11 % | 9.58 % | 16.75 % | 27.4 % | 43.29 % | 57.19 % |
| 2.0 ATR | 7.554 % | 13.9316 | 0.7 % | 4.54 % | 8.48 % | 15.37 % | 29.67 % | 46.1 % |
| 2.5 ATR | 9.443 % | 13.647 | 0.3 % | 2.02 % | 4.04 % | 9.61 % | 19.92 % | 36.24 % |
| 3.0 ATR | 11.331 % | 13.3624 | 0.1 % | 0.91 % | 2.93 % | 6.17 % | 13.82 % | 28.34 % |
| 4.0 ATR | 15.109 % | 12.7931 | 0.0 % | 0.3 % | 0.71 % | 2.53 % | 7.42 % | 14.78 % |
| 6.0 ATR | 22.663 % | 11.6547 | 0.0 % | 0.1 % | 0.2 % | 0.2 % | 0.91 % | 3.08 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.68 ATR | 0.76 ATR | 0.97 ATR | 1.21 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.63 ATR | 0.83 ATR | 0.99 ATR | 1.12 ATR | 1.48 ATR | 1.95 ATR |
| **3 s.** | 0.32 ATR | 0.70 ATR | 0.79 ATR | 1.03 ATR | 1.23 ATR | 1.39 ATR | 1.91 ATR | 2.39 ATR |
| **5 s.** | 0.41 ATR | 0.90 ATR | 1.01 ATR | 1.33 ATR | 1.60 ATR | 1.81 ATR | 2.47 ATR | 3.32 ATR |
| **10 s.** | 0.63 ATR | 1.29 ATR | 1.45 ATR | 1.88 ATR | 2.24 ATR | 2.50 ATR | 3.60 ATR | 4.74 ATR |
| **20 s.** | 0.85 ATR | 1.82 ATR | 2.06 ATR | 2.71 ATR | 3.25 ATR | 3.62 ATR | 4.82 ATR | 5.67 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.428–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.889 %, prix 14.7853), p(touche) 37.66 % (en stress 83.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.628–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.833 %, prix 14.6431), p(touche) 37.0 % (en stress 91.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 19.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.787–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.777 %, prix 14.5008), p(touche) 34.11 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 21.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.008–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.721 %, prix 14.3585), p(touche) 35.89 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.446–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.666 %, prix 14.2161), p(touche) 43.29 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.056–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (9.443 %, prix 13.6469), p(touche) 36.24 % (en stress 98.98 %)  ✅ optimum identifie (76.2 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.056 | EV/share : $-0.016 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 16 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.6 | bear 6.5 | side 79.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈60.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.773% → cible +3.902% / stop −1.951%, p_fill 14%, n_eff≈17.4) : P(cible|rempli) **16%** · **EV/risk +0.006** (×p_fill ; si rempli +0.08% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=8, n_eff=8))
  - **deep** : indisponible (échantillon insuffisant (n=7, n_eff=7))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→64% · +2.0%→42% · +3.0%→30% · +5.0%→10% · +8.0%→1%
- Range intraday médian 4.06% (p90 6.61%) · excursion haute méd. +1.52% / basse méd. −2.06%
- Profil de vol intra : ouverture 2.849% vs midi 0.819% vs clôture 0.934% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 20% · trend ↑1%/↓0% ; spike-down 62% · recovery-V 23%)_
- **Régime intraday** : **chop** _(efficiency 0.153 ; neutre — autocorr -0.023)_ ; drift intra méd. -0.686% ; recovery-V 22%
- **σ réalisé intraday** 2.273% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 64% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 15.8262 (VA 15.8138–15.9262 ; dernier close 15.75)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 15% · rebond 61% · **stop −2.1%** sous le fill (sous le bruit) · cible +1.97% · R/R 0.94 (high win-rate)
- Gaps overnight (n=159) : méd. 0.17% · baisse 43% (gap-down >1% 22% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −1.59%) · haut méd +0.65% · range méd 1.42%
- Excursion ouverture 15min (n=160) : bas méd −1.01% (p90 −2.37%) · haut méd +0.79% · range méd 2.05%
- Excursion ouverture 30min (n=160) : bas méd −1.09% (p90 −3.24%) · haut méd +0.86% · range méd 2.37%
- Excursion ouverture 60min (n=160) : bas méd −1.22% (p90 −3.59%) · haut méd +0.99% · range méd 2.76%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 15.77 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 76% (120/159) · gap 30% · délai 0.1min · rebond 56% (69/120) (MFE +1.22%)
   - −1.0% : fill 30min 49% · séance 63% (105/159) · gap 22% · délai 1.5min · rebond 49% (57/105) (MFE +0.93%)
   - −1.5% : fill 30min 41% · séance 55% (94/159) · gap 19% · délai 6.8min · rebond 59% (61/94) (MFE +1.3%)
   - −2.0% : fill 30min 30% · séance 43% (73/159) · gap 8% · délai 9.8min · rebond 63% (50/73) (MFE +1.47%)
   - −3.0% : fill 30min 7% · séance 30% (52/159) · gap 2% · délai 78.7min · rebond 49% (32/52) (MFE +1.02%)
   - −4.0% : fill 30min 5% · séance 15% (30/159) · gap 1% · délai 86.8min · rebond 61% (19/30) (MFE +1.97%)
   - −5.0% : fill 30min 2% · séance 7% (15/159) · gap 1% · délai 208.5min · rebond 44% (8/15) (MFE +0.67%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.48% (p90 −1.78%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.49% (p90 −1.87%) → stop au-delà de −1.42% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −1.43%) → stop au-delà de −1.11% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=612 jambes) : jambe baissière méd −1.0% (p90 −2.74%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (64 séances) :
      · −1.0% : fill 98% (63/64) · rebond 49% (35/63)
      · −2.0% : fill 85% (54/64) · rebond 68% (37/54)
      · −3.0% : fill 59% (39/64) · rebond 49% (25/39)
      · −4.0% : fill 35% (25/64) · rebond 69% (17/25)
      · −5.0% : fill 15% (13/64) · rebond 52% (7/13)
   - **flat** (24 séances) :
      · −1.0% : fill 76% (16/24) · rebond 31% (6/16)
      · −2.0% : fill 39% (8/24) · rebond 53% (5/8)
      · −3.0% : fill 33% (7/24) · rebond 44% (3/7)
      · −4.0% : fill 11% (3/24) · rebond 30% (1/3)
      · −5.0% : fill 7% (1/24) · rebond 0% (0/1)
   - **gap-up** (71 séances) :
      · −1.0% : fill 32% (26/71) · rebond 65% (16/26)
      · −2.0% : fill 13% (11/71) · rebond 56% (8/11)
      · −3.0% : fill 7% (6/71) · rebond 60% (4/6)
      · −4.0% : fill 2% (2/71) · rebond 20% (1/2)
      · −5.0% : fill 0% (1/71) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 39% en base · 65% si les 15 1res min sont vertes (72 cas) · 22% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **36min** → P(séance verte=clôture>ouverture) 71% si début vert vs 19% si rouge (base 39% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 230min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **71%** · continue >prix actuel 51% ; creux résiduel méd -1.51% (q20 -2.67%) → **SL/trailing à −2.67%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.8% / q75 +2.64% → **scale +1.8% / runner +2.64%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **19%** (continue à baisser 63%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.79%** (au-delà de la MAE q10 -2.79%), cible rebond +1.12% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.96% .. +3.18%] · haut q95 +3.88% · bas q05 -3.58%
   - 60min (n=160) : retour [-3.13% .. +3.65%] · haut q95 +4.44% · bas q05 -3.99%
   - 2h (n=160) : retour [-3.52% .. +3.76%] · haut q95 +4.95% · bas q05 -4.15%
   - 4h (n=160) : retour [-3.89% .. +4.27%] · haut q95 +5.43% · bas q05 -5.08%
   - 6h (n=160) : retour [-4.24% .. +4.07%] · haut q95 +5.44% · bas q05 -5.17%
   - session (n=160) : retour [-4.42% .. +4.63%] · haut q95 +5.47% · bas q05 -5.19%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.73%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.56 · part idiosyncratique 0.44
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 31.8  _(momentum baissier)_
- **ADX** : 22.4  _(pas de tendance nette)_
- **MACD** : hist -0.073  _(pas de croisement recent)_
- **BB** : %B 0.2 · largeur 18.3%
- **ATR** : 0.57 (3.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.237  _(distribution)_
- **Vol ratio** : 1.19  _(volume normal)_
- **Choppiness** : 43.3  _(transition)_
- **MA** : MA20 15.93 · MA50 17.16 · MA200 18.43  _(prix < MA20)_
- **Dist MA** : MA20 -5.4% · MA50 -12.2% · MA200 -18.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (850135 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
