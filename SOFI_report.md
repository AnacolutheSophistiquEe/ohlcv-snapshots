# SOFI

**Generated** : 2026-11-09T01:30:44.045319+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 6/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $16.21  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-10 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot $16.21 (+3.8% vs entrée) · entrée $15.61 · stop $14.41 · T1 $18.01 · R/R 2.0  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-06 : 16.21 · ATR Wilder 0.8525 (5.26 %)_
- **Swing** : plage **15.11 → 14.48** (-6.8 % a -10.68 % sous la cloture, 0.74 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 14.42-15.43 (B) ; 14.85-15.22 (B). stop INDICATIF 13.17 (-9.02 % sous le bas ; sous le support 13.6-13.9 (- 0,5 ATR)).
- **Deep** : plage **14.48 → 12.89** (-10.68 % a -20.49 % sous la cloture, 1.87 ATR) — touchee 46 % → 15 % du temps en 20 seances ; supports reels dans la plage : 14.42-15.43 (B) ; 13.6-13.9 (A) ; 13.01-13.42 (C). stop INDICATIF 12.07 (-6.33 % sous le bas ; sous le support 12.5-12.86 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (1.79 ATR sous le plus haut 20 s., RSI(2) 34.0 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 15.5-15.65 (B, -3.45 %) ; 14.42-15.43 (B, -4.8 %) ; 14.85-15.22 (B, -6.11 %) ; 13.6-13.9 (A, -14.25 %) ; 13.01-13.42 (C, -17.21 %) ; 12.5-12.86 (A, -20.67 %)
- Resistances reelles au-dessus : 16.68-17.08 (A, 2.9 %) ; 17.11-17.19 (B, 5.55 %) ; 17.58-17.96 (A, 8.45 %) ; 18.42-18.8 (A, 13.63 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=5.90 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (11.08 %)** : le gap seul le franchit 0.08 % des séances (1 fois sur 1254).
   - exécution **0.025 pt plus bas** dans le cas TYPIQUE (médiane), 0.025 au p90, **0.025 au pire**
   - perte réelle **11.105 %** en moyenne _(tirée par la queue)_, jusqu'à **11.105 %** — au lieu des 11.08 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.204 % | p01 -6.517 % | pire -11.105 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5008** [0.4268 ; 0.5748] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.2577** [0.2137 ; 0.3057] _(largeur 9.2 pt, n_eff 345.7)_
   - deep : **0.3952** [0.3447 ; 0.4474] _(largeur 10.3 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : deep (27.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.24 %** | CVaR **-8.68 %** | vol 4.1 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.5 % vs -14.4 % si l'on extrapolait par √5 _(rapport 1.007 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7923** (β de hausse 1.7014, asymétrie 1.0534) vs IWM — 605 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 14.8516 sur atr_based (1.5 ATR, 8.38 %) — p(stop avant cible) 0.416 [0.36 ; 0.47], R/R 6.363, perte reelle 8.725 % (gap inclus), CVaR 11.137 %, EV -0.6679 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.9993 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 8.38 %) — p(stop avant cible) 0.416 [0.36 ; 0.47], R/R 6.363, perte reelle 8.725 % (gap inclus), EV -0.6679 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.67 %) : P(cible) 0.0 % x 55.51 % + P(rien) 58.4 % x 5.06 % ne couvrent pas P(stop) 41.6 % x 8.72 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+55.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🟢 support a 1.47 ATR (stop 10.73 %) — p(stop avant cible) 0.2953 [0.25 ; 0.34], R/R 5.016, perte reelle 11.067 % (gap inclus), EV -0.7805 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.70 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.78 %) : P(cible) 0.0 % x 55.51 % + P(rien) 70.5 % x 3.52 % ne couvrent pas P(stop) 29.5 % x 11.07 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+55.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🟢 support a 2.6 ATR (stop 17.022 %) — p(stop avant cible) 0.0631 [0.04 ; 0.09], R/R 3.238, perte reelle 17.146 % (gap inclus), EV -0.0307 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 17.18 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 0.0 % x 55.51 % + P(rien) 93.7 % x 1.12 % ne couvrent pas P(stop) 6.3 % x 17.15 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+55.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.25 ATR (stop 1.397 %) — p(stop avant cible) 0.9262 [0.90 ; 0.95], R/R 36.581, perte reelle 1.518 % (gap inclus), EV -0.3281 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 36.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.926, borne haute 0.950 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 0.0 % x 55.51 % + P(rien) 7.4 % x 14.62 % ne couvrent pas P(stop) 92.6 % x 1.52 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+55.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.5 ATR (stop 2.793 %) — p(stop avant cible) 0.8397 [0.80 ; 0.88], R/R 18.535, perte reelle 2.995 % (gap inclus), EV -0.683 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 18.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.840, borne haute 0.875 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.68 %) : P(cible) 0.0 % x 55.51 % + P(rien) 16.0 % x 11.43 % ne couvrent pas P(stop) 84.0 % x 2.99 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+55.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.75 ATR (stop 4.19 %) — p(stop avant cible) 0.7117 [0.66 ; 0.76], R/R 12.381, perte reelle 4.484 % (gap inclus), EV -0.4774 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 12.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.712, borne haute 0.757 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.48 %) : P(cible) 0.0 % x 55.51 % + P(rien) 28.8 % x 9.40 % ne couvrent pas P(stop) 71.2 % x 4.48 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+55.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.0 ATR (stop 5.586 %) — p(stop avant cible) 0.6157 [0.56 ; 0.67], R/R 9.38, perte reelle 5.918 % (gap inclus), EV -0.6463 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 9.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.616, borne haute 0.666 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.65 %) : P(cible) 0.0 % x 55.51 % + P(rien) 38.4 % x 7.79 % ne couvrent pas P(stop) 61.6 % x 5.92 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+55.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🟢 grid_snapped a 1.47 ATR (stop 9.881 %) — p(stop avant cible) 0.3486 [0.30 ; 0.40], R/R 5.394, perte reelle 10.292 % (gap inclus), EV -0.9528 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.57 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.95 %) : P(cible) 0.0 % x 55.51 % + P(rien) 65.1 % x 4.04 % ne couvrent pas P(stop) 34.9 % x 10.29 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+55.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.25 ATR (stop 12.57 %) — p(stop avant cible) 0.1939 [0.15 ; 0.24], R/R 4.316, perte reelle 12.861 % (gap inclus), EV -0.4451 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.70 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.45 %) : P(cible) 0.0 % x 55.51 % + P(rien) 80.6 % x 2.53 % ne couvrent pas P(stop) 19.4 % x 12.86 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+55.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🟢 grid_snapped a 2.6 ATR (stop 16.173 %) — p(stop avant cible) 0.0741 [0.05 ; 0.11], R/R 3.409, perte reelle 16.284 % (gap inclus), EV -0.036 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 16.34 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 0.0 % x 55.51 % + P(rien) 92.6 % x 1.26 % ne couvrent pas P(stop) 7.4 % x 16.28 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+55.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 3.5 ATR (stop 19.553 %) — p(stop avant cible) 0.0423 [0.02 ; 0.07], R/R 2.835, perte reelle 19.584 % (gap inclus), EV -0.0391 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.01 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 0.0 % x 55.51 % + P(rien) 95.8 % x 0.82 % ne couvrent pas P(stop) 4.2 % x 19.58 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+55.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 4.0 ATR (stop 22.346 %) — p(stop avant cible) 0.0259 [0.01 ; 0.05], R/R 2.465, perte reelle 22.516 % (gap inclus), EV -0.0679 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.86 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.07 %) : P(cible) 0.0 % x 55.51 % + P(rien) 97.4 % x 0.52 % ne couvrent pas P(stop) 2.6 % x 22.52 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+55.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 4.5 ATR (stop 25.139 %) — p(stop avant cible) 0.0133 [0.00 ; 0.03], R/R 2.194, perte reelle 25.296 % (gap inclus), EV -0.037 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.62 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 0.0 % x 55.51 % + P(rien) 98.7 % x 0.30 % ne couvrent pas P(stop) 1.3 % x 25.30 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+55.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 5.0 ATR (stop 27.932 %) — p(stop avant cible) 0.0031 [0.00 ; 0.01], R/R 1.986, perte reelle 27.953 % (gap inclus), EV 0.0366 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.48 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 30.726 %) — p(stop avant cible) 0.0024 [0.00 ; 0.01], R/R 1.807, perte reelle 30.728 % (gap inclus), EV 0.0401 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.44 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 33.519 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 1.656, perte reelle 33.519 % (gap inclus), EV 0.0516 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.28 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 36.312 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 1.528, perte reelle 36.328 % (gap inclus), EV 0.048 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.34 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 39.105 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.42, perte reelle 39.105 % (gap inclus), EV 0.0579 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.17 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 41.899 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.325, perte reelle 41.899 % (gap inclus), EV 0.0577 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.17 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 44.692 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.242, perte reelle 44.692 % (gap inclus), EV 0.0577 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.17 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 16.21, ATR14 0.9056 (5.586 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.377 ATR = 2.106 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.279 % | 16.1647 | 92.86 % | 95.77 % | 97.18 % | 97.47 % | 98.17 % | 98.87 % |
| 0.1 ATR | 0.559 % | 16.1194 | 84.91 % | 89.33 % | 92.14 % | 93.33 % | 95.33 % | 97.13 % |
| 0.15 ATR | 0.838 % | 16.0742 | 78.77 % | 84.59 % | 88.0 % | 90.3 % | 92.69 % | 94.87 % |
| 0.2 ATR | 1.117 % | 16.0289 | 71.53 % | 79.36 % | 83.37 % | 86.77 % | 90.36 % | 93.33 % |
| 0.25 ATR | 1.397 % | 15.9836 | 66.2 % | 75.13 % | 80.24 % | 84.44 % | 89.14 % | 92.21 % |
| 0.35 ATR | 1.955 % | 15.893 | 52.82 % | 65.36 % | 72.38 % | 78.69 % | 85.69 % | 89.03 % |
| 0.5 ATR | 2.793 % | 15.7572 | 37.42 % | 53.37 % | 61.69 % | 69.39 % | 79.59 % | 84.92 % |
| 0.75 ATR | 4.19 % | 15.5308 | 20.42 % | 36.86 % | 46.57 % | 57.17 % | 70.15 % | 78.46 % |
| 1.0 ATR | 5.586 % | 15.3044 | 8.75 % | 24.37 % | 33.67 % | 44.95 % | 59.9 % | 69.95 % |
| 1.25 ATR | 6.983 % | 15.078 | 4.23 % | 15.21 % | 24.09 % | 35.66 % | 51.07 % | 63.49 % |
| 1.5 ATR | 8.38 % | 14.8516 | 2.01 % | 9.47 % | 16.63 % | 27.17 % | 43.25 % | 57.23 % |
| 2.0 ATR | 11.173 % | 14.3989 | 0.7 % | 4.53 % | 8.57 % | 15.45 % | 29.95 % | 46.26 % |
| 2.5 ATR | 13.966 % | 13.9461 | 0.3 % | 1.91 % | 4.03 % | 9.6 % | 20.3 % | 36.72 % |
| 3.0 ATR | 16.759 % | 13.4933 | 0.1 % | 0.81 % | 2.82 % | 6.16 % | 14.01 % | 29.23 % |
| 4.0 ATR | 22.346 % | 12.5877 | 0.0 % | 0.3 % | 0.6 % | 2.42 % | 7.21 % | 15.08 % |
| 6.0 ATR | 33.519 % | 10.7766 | 0.0 % | 0.1 % | 0.2 % | 0.2 % | 0.91 % | 3.18 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.56 ATR | 0.68 ATR | 0.76 ATR | 0.97 ATR | 1.21 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.63 ATR | 0.83 ATR | 0.99 ATR | 1.12 ATR | 1.48 ATR | 1.95 ATR |
| **3 s.** | 0.32 ATR | 0.69 ATR | 0.78 ATR | 1.02 ATR | 1.23 ATR | 1.39 ATR | 1.91 ATR | 2.39 ATR |
| **5 s.** | 0.41 ATR | 0.90 ATR | 1.00 ATR | 1.33 ATR | 1.59 ATR | 1.81 ATR | 2.47 ATR | 3.31 ATR |
| **10 s.** | 0.62 ATR | 1.28 ATR | 1.44 ATR | 1.89 ATR | 2.26 ATR | 2.52 ATR | 3.59 ATR | 4.70 ATR |
| **20 s.** | 0.85 ATR | 1.83 ATR | 2.07 ATR | 2.75 ATR | 3.30 ATR | 3.65 ATR | 4.85 ATR | 5.69 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.426–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.793 %, prix 15.7573), p(touche) 37.42 % (en stress 82.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 21.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.627–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.19 %, prix 15.5308), p(touche) 36.86 % (en stress 92.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 20.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.78–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.586 %, prix 15.3045), p(touche) 33.67 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.999–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.586 %, prix 15.3045), p(touche) 44.95 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.444–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.38 %, prix 14.8516), p(touche) 43.25 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.066–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (13.966 %, prix 13.9461), p(touche) 36.72 % (en stress 98.98 %)  ✅ optimum identifie (77.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.133 | EV/share : $-0.160 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 8 % | T2 2 % | T3 0 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 58.9 | bear 33.2 | side 7.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 392.0 (= 27 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.674% → cible +2.841% / stop −1.705%, p_fill 54%, n_eff≈59.7) : P(cible|rempli) **10%** · **EV/risk -0.135** (×p_fill ; si rempli -0.43% du capital)
  - **swing** (entrée dip −3.682% → cible +15.363% / stop −7.681%, p_fill 36%, n_eff≈42.3) : P(cible|rempli) **6%** · **EV/risk +0.021** (×p_fill ; si rempli +0.46% du capital)
  - **deep** (entrée dip −5.696% → cible +17.822% / stop −8.911%, p_fill 31%, n_eff≈33.9) : P(cible|rempli) **13%** · **EV/risk +0.006** (×p_fill ; si rempli +0.17% du capital)
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

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.35 · part idiosyncratique 0.65
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-10 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-10 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-10 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 62.8  _(momentum haussier)_
- **ADX** : 23.5  _(pas de tendance nette)_
- **MACD** : hist 0.16  _(pas de croisement recent)_
- **BB** : %B 0.63 · largeur 28.7%
- **ATR** : 0.91 (49.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.019  _(neutre)_
- **Vol ratio** : 0.75  _(volume normal)_
- **Choppiness** : 48.1  _(transition)_
- **MA** : MA20 15.65 · MA50 16.35 · MA200 17.55  _(prix > MA20)_
- **Dist MA** : MA20 +3.6% · MA50 -0.9% · MA200 -7.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (713257 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
