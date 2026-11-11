# NEX

**Generated** : 2026-11-11T01:09:20.916275+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €128.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-0 sess · macro taux)  
> ↳ spot €128.00 (+4.4% vs entrée) · entrée €122.66 · stop €112.85 · T1 €128.19 · R/R 0.56  
> ↳ _probas brutes, non calibrées · n=0_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-10 : 128.0 · ATR Wilder 4.96 (3.87 %)_
- **Swing** : plage **121.23 → 117.19** (-5.29 % a -8.44 % sous la cloture, 0.81 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 118.73-121.04 (B) ; 115.59-117.84 (B). stop INDICATIF 110.45 (-5.75 % sous le bas ; sous le support 112.93-114.01 (- 0,5 ATR)).
- **Deep** : plage **117.19 → 105.71** (-8.44 % a -17.42 % sous la cloture, 2.32 ATR) — touchee 42 % → 15 % du temps en 20 seances ; supports reels dans la plage : 115.59-117.84 (B) ; 112.93-114.01 (B) ; 109.66-111.7 (A) ; 107.17-109.18 (A) ; 104.49-106.6 (B). stop INDICATIF 99.43 (-5.94 % sous le bas ; sous le support 101.91-102.92 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (1.19 ATR sous le plus haut 20 s., RSI(2) 93.8 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 121.91-124.33 (B, -2.87 %) ; 118.73-121.04 (B, -5.43 %) ; 115.59-117.84 (B, -7.93 %) ; 112.93-114.01 (B, -10.93 %) ; 109.66-111.7 (A, -12.73 %) ; 107.17-109.18 (A, -14.7 %)
- Resistances reelles au-dessus : 130.61-131.89 (A, 2.04 %) ; 133.87-136.3 (A, 4.58 %) ; 137.58-139.35 (A, 7.49 %) ; 140.66-142.7 (A, 9.89 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.64 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (12.58 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1280).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 12.58 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.57 % | p01 -3.604 % | pire -9.596 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0026** [0.0001 ; 0.0205] _(largeur 2.0 pt, n_eff 173.1)_
   - swing : **0.3572** [0.3081 ; 0.4087] _(largeur 10.1 pt, n_eff 345.8)_
   - deep : **0.3004** [0.2539 ; 0.3502] _(largeur 9.6 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-3.62 %** | CVaR **-5.37 %** | vol 2.33 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.8 % vs -8.12 % si l'on extrapolait par √5 _(rapport 0.961 ; < 1 = le √5 surestime)_
- **β de baisse : 0.996** (β de hausse 1.077, asymétrie 0.9248) vs FCHI — 622 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 117.3286 sur atr_grid (2.0 ATR, 8.337 %) — p(stop avant cible) 0.231 [0.19 ; 0.28], R/R 3.261, perte reelle 8.445 % (gap inclus), CVaR 8.836 %, EV -0.3173 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 6.253 %) — p(stop avant cible) 0.4024 [0.35 ; 0.45], R/R 4.306, perte reelle 6.397 % (gap inclus), EV -0.6534 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.65 %) : P(cible) 0.0 % x 27.54 % + P(rien) 59.8 % x 3.21 % ne couvrent pas P(stop) 40.2 % x 6.40 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+27.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ swing_based a 3.25 ATR (stop 15.656 %) — p(stop avant cible) 0.0215 [0.01 ; 0.04], R/R 1.718, perte reelle 16.036 % (gap inclus), EV -0.2032 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.64 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 0.0 % x 27.54 % + P(rien) 97.9 % x 0.14 % ne couvrent pas P(stop) 2.1 % x 16.04 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+27.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.25 ATR (stop 1.042 %) — p(stop avant cible) 0.9123 [0.88 ; 0.94], R/R 25.544, perte reelle 1.078 % (gap inclus), EV -0.2771 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 25.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.912, borne haute 0.939 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.28 %) : P(cible) 0.0 % x 27.54 % + P(rien) 8.8 % x 8.06 % ne couvrent pas P(stop) 91.2 % x 1.08 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+27.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.5 ATR (stop 2.084 %) — p(stop avant cible) 0.7706 [0.72 ; 0.81], R/R 12.75, perte reelle 2.16 % (gap inclus), EV -0.342 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 12.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.771, borne haute 0.812 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.34 %) : P(cible) 0.0 % x 27.54 % + P(rien) 22.9 % x 5.77 % ne couvrent pas P(stop) 77.1 % x 2.16 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+27.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.75 ATR (stop 3.126 %) — p(stop avant cible) 0.6869 [0.64 ; 0.73], R/R 8.456, perte reelle 3.257 % (gap inclus), EV -0.5169 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 8.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.687, borne haute 0.734 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.52 %) : P(cible) 0.0 % x 27.54 % + P(rien) 31.3 % x 5.49 % ne couvrent pas P(stop) 68.7 % x 3.26 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+27.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.0 ATR (stop 4.169 %) — p(stop avant cible) 0.5919 [0.54 ; 0.64], R/R 6.361, perte reelle 4.33 % (gap inclus), EV -0.635 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.592, borne haute 0.643 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.64 %) : P(cible) 0.0 % x 27.54 % + P(rien) 40.8 % x 4.72 % ne couvrent pas P(stop) 59.2 % x 4.33 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+27.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.25 ATR (stop 5.211 %) — p(stop avant cible) 0.4859 [0.43 ; 0.54], R/R 5.114, perte reelle 5.386 % (gap inclus), EV -0.6035 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.60 %) : P(cible) 0.0 % x 27.54 % + P(rien) 51.4 % x 3.92 % ne couvrent pas P(stop) 48.6 % x 5.39 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+27.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.75 ATR (stop 7.295 %) — p(stop avant cible) 0.2932 [0.25 ; 0.34], R/R 3.701, perte reelle 7.443 % (gap inclus), EV -0.3667 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.37 %) : P(cible) 0.0 % x 27.54 % + P(rien) 70.7 % x 2.57 % ne couvrent pas P(stop) 29.3 % x 7.44 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+27.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.0 ATR (stop 8.337 %) — p(stop avant cible) 0.231 [0.19 ; 0.28], R/R 3.261, perte reelle 8.445 % (gap inclus), EV -0.3173 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.32 %) : P(cible) 0.0 % x 27.54 % + P(rien) 76.9 % x 2.12 % ne couvrent pas P(stop) 23.1 % x 8.44 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+27.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.25 ATR (stop 9.379 %) — p(stop avant cible) 0.172 [0.14 ; 0.21], R/R 2.899, perte reelle 9.502 % (gap inclus), EV -0.2997 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.30 %) : P(cible) 0.0 % x 27.54 % + P(rien) 82.8 % x 1.61 % ne couvrent pas P(stop) 17.2 % x 9.50 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+27.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.5 ATR (stop 10.421 %) — p(stop avant cible) 0.1338 [0.10 ; 0.17], R/R 2.616, perte reelle 10.529 % (gap inclus), EV -0.3327 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 0.0 % x 27.54 % + P(rien) 86.6 % x 1.24 % ne couvrent pas P(stop) 13.4 % x 10.53 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+27.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.75 ATR (stop 11.463 %) — p(stop avant cible) 0.103 [0.07 ; 0.14], R/R 2.365, perte reelle 11.644 % (gap inclus), EV -0.3082 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.31 %) : P(cible) 0.0 % x 27.54 % + P(rien) 89.7 % x 0.99 % ne couvrent pas P(stop) 10.3 % x 11.64 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+27.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 3.0 ATR (stop 12.506 %) — p(stop avant cible) 0.0739 [0.05 ; 0.11], R/R 2.16, perte reelle 12.752 % (gap inclus), EV -0.3174 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.87 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.32 %) : P(cible) 0.0 % x 27.54 % + P(rien) 92.6 % x 0.67 % ne couvrent pas P(stop) 7.4 % x 12.75 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+27.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ grid_snapped a 3.25 ATR (stop 14.819 %) — p(stop avant cible) 0.0306 [0.02 ; 0.05], R/R 1.803, perte reelle 15.272 % (gap inclus), EV -0.219 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.89 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.22 %) : P(cible) 0.0 % x 27.54 % + P(rien) 96.9 % x 0.26 % ne couvrent pas P(stop) 3.1 % x 15.27 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+27.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 4.0 ATR (stop 16.674 %) — p(stop avant cible) 0.0105 [0.00 ; 0.03], R/R 1.598, perte reelle 17.239 % (gap inclus), EV -0.1658 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.13 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 0.0 % x 27.54 % + P(rien) 99.0 % x 0.02 % ne couvrent pas P(stop) 1.1 % x 17.24 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+27.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 4.5 ATR (stop 18.758 %) — p(stop avant cible) 0.0037 [0.00 ; 0.01], R/R 1.4, perte reelle 19.668 % (gap inclus), EV -0.1305 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.82 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 0.0 % x 27.54 % + P(rien) 99.6 % x -0.06 % ne couvrent pas P(stop) 0.4 % x 19.67 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+27.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 5.0 ATR (stop 20.843 %) — p(stop avant cible) 0.0022 [0.00 ; 0.01], R/R 1.24, perte reelle 22.21 % (gap inclus), EV -0.126 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.77 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 0.0 % x 27.54 % + P(rien) 99.8 % x -0.08 % ne couvrent pas P(stop) 0.2 % x 22.21 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+27.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 5.5 ATR (stop 22.927 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 1.152, perte reelle 23.904 % (gap inclus), EV -0.1191 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.63 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 0.0 % x 27.54 % + P(rien) 99.9 % x -0.09 % ne couvrent pas P(stop) 0.1 % x 23.90 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+27.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 6.0 ATR (stop 25.011 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 1.101, perte reelle 25.011 % (gap inclus), EV -0.1175 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.57 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 0.0 % x 27.54 % + P(rien) 99.9 % x -0.10 % ne couvrent pas P(stop) 0.1 % x 25.01 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+27.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 6.5 ATR (stop 27.095 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.016, perte reelle 27.095 % (gap inclus), EV -0.1128 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.11 %) : P(cible) 0.0 % x 27.54 % + P(rien) 100.0 % x -0.11 % ne couvrent pas P(stop) 0.0 % x 27.09 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+27.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 7.0 ATR (stop 29.18 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.944, perte reelle 29.18 % (gap inclus), EV -0.1128 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.11 %) : P(cible) 0.0 % x 27.54 % + P(rien) 100.0 % x -0.11 % ne couvrent pas P(stop) 0.0 % x 29.18 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+27.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 7.5 ATR (stop 31.264 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.881, perte reelle 31.264 % (gap inclus), EV -0.1128 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.11 %) : P(cible) 0.0 % x 27.54 % + P(rien) 100.0 % x -0.11 % ne couvrent pas P(stop) 0.0 % x 31.26 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+27.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 8.0 ATR (stop 33.348 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.826, perte reelle 33.348 % (gap inclus), EV -0.1128 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.11 %) : P(cible) 0.0 % x 27.54 % + P(rien) 100.0 % x -0.11 % ne couvrent pas P(stop) 0.0 % x 33.35 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+27.5 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 128.0, ATR14 5.3357 (4.169 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.347 ATR = 1.446 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.208 % | 127.7332 | 87.55 % | 91.46 % | 93.22 % | 95.08 % | 96.93 % | 97.9 % |
| 0.1 ATR | 0.417 % | 127.4664 | 81.67 % | 87.73 % | 90.37 % | 93.11 % | 95.55 % | 97.0 % |
| 0.15 ATR | 0.625 % | 127.1996 | 75.1 % | 83.51 % | 86.94 % | 90.16 % | 94.07 % | 95.7 % |
| 0.2 ATR | 0.834 % | 126.9329 | 68.43 % | 78.21 % | 83.2 % | 88.19 % | 92.78 % | 95.0 % |
| 0.25 ATR | 1.042 % | 126.6661 | 61.96 % | 73.6 % | 79.08 % | 85.14 % | 90.8 % | 93.81 % |
| 0.35 ATR | 1.459 % | 126.1325 | 49.61 % | 64.18 % | 71.91 % | 79.13 % | 87.04 % | 91.71 % |
| 0.5 ATR | 2.084 % | 125.3321 | 34.71 % | 52.6 % | 61.49 % | 71.16 % | 80.61 % | 87.71 % |
| 0.75 ATR | 3.126 % | 123.9982 | 20.69 % | 36.51 % | 47.45 % | 58.96 % | 70.62 % | 81.32 % |
| 1.0 ATR | 4.169 % | 122.6643 | 10.78 % | 24.44 % | 34.77 % | 48.52 % | 61.92 % | 74.63 % |
| 1.25 ATR | 5.211 % | 121.3304 | 4.71 % | 16.39 % | 25.25 % | 39.67 % | 54.9 % | 68.23 % |
| 1.5 ATR | 6.253 % | 119.9964 | 2.45 % | 11.38 % | 18.96 % | 30.91 % | 47.48 % | 60.94 % |
| 2.0 ATR | 8.337 % | 117.3286 | 0.78 % | 5.4 % | 10.12 % | 19.59 % | 35.61 % | 50.95 % |
| 2.5 ATR | 10.421 % | 114.6607 | 0.49 % | 2.45 % | 5.4 % | 11.42 % | 24.73 % | 39.06 % |
| 3.0 ATR | 12.506 % | 111.9929 | 0.2 % | 1.57 % | 3.14 % | 7.19 % | 17.61 % | 30.57 % |
| 4.0 ATR | 16.674 % | 106.6571 | 0.1 % | 0.49 % | 0.88 % | 1.97 % | 7.52 % | 18.58 % |
| 6.0 ATR | 25.011 % | 95.9857 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 1.29 % | 4.5 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.67 ATR | 0.77 ATR | 1.03 ATR | 1.24 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.62 ATR | 0.82 ATR | 0.99 ATR | 1.14 ATR | 1.61 ATR | 2.07 ATR |
| **3 s.** | 0.31 ATR | 0.70 ATR | 0.80 ATR | 1.05 ATR | 1.26 ATR | 1.46 ATR | 2.01 ATR | 2.59 ATR |
| **5 s.** | 0.43 ATR | 0.96 ATR | 1.10 ATR | 1.44 ATR | 1.76 ATR | 1.98 ATR | 2.67 ATR | 3.42 ATR |
| **10 s.** | 0.64 ATR | 1.42 ATR | 1.60 ATR | 2.12 ATR | 2.49 ATR | 2.83 ATR | 3.75 ATR | 4.81 ATR |
| **20 s.** | 0.99 ATR | 2.04 ATR | 2.25 ATR | 2.86 ATR | 3.46 ATR | 3.88 ATR | 5.22 ATR | 5.93 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.396 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (82.5 % des re-echantillons)
- **2 seance(s)** : plage utile 0.618–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.126 %, prix 123.9987), p(touche) 36.51 % (en stress 90.2 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 55.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.798–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.169 %, prix 122.6637), p(touche) 34.77 % (en stress 85.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.099–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (5.211 %, prix 121.3299), p(touche) 39.67 % (en stress 93.14 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 53.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.604–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (8.337 %, prix 117.3286), p(touche) 35.61 % (en stress 98.04 %)  ✅ optimum identifie (65.0 % des re-echantillons)
- **20 seance(s)** : plage utile 2.25–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (10.421 %, prix 114.6611), p(touche) 39.06 % (en stress 98.02 %)  ✅ optimum identifie (65.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 52.1 | side 42.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 256.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=11, n_eff=9))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→65% · +1.0%→52% · +2.0%→22% · +3.0%→10% · +5.0%→1% · +8.0%→0%
- Range intraday médian 2.94% (p90 4.66%) · excursion haute méd. +1.05% / basse méd. −1.41%
- Profil de vol intra : ouverture 1.742% vs midi 0.526% vs clôture 0.695% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 49% · recovery-V 14%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; mean-reverting — autocorr -0.042)_ ; drift intra méd. -0.944% ; recovery-V 13%
- **σ réalisé intraday** 2.228% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 71% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 113.2062 (VA 112.9812–114.2188 ; dernier close 113.5)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 20% · rebond 52% · **stop −2.11%** sous le fill (sous le bruit) · cible +1.29% · R/R 0.61 (high win-rate)
- Gaps overnight (n=159) : méd. 0.37% · baisse 28% (gap-down >1% 9% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.58% (p90 −1.83%) · haut méd +0.2% · range méd 1.01%
- Excursion ouverture 15min (n=160) : bas méd −0.77% (p90 −2.19%) · haut méd +0.36% · range méd 1.31%
- Excursion ouverture 30min (n=160) : bas méd −0.78% (p90 −2.35%) · haut méd +0.37% · range méd 1.59%
- Excursion ouverture 60min (n=160) : bas méd −0.86% (p90 −2.75%) · haut méd +0.57% · range méd 1.85%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 113.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 45% · séance 63% (90/159) · gap 13% · délai 0.8min · rebond 38% (37/90) (MFE +0.64%)
   - −1.0% : fill 30min 29% · séance 54% (74/159) · gap 9% · délai 21.4min · rebond 31% (27/74) (MFE +0.58%)
   - −1.5% : fill 30min 22% · séance 43% (59/159) · gap 0% · délai 27.4min · rebond 30% (19/59) (MFE +0.58%)
   - −2.0% : fill 30min 14% · séance 34% (43/159) · gap 0% · délai 56.6min · rebond 26% (14/43) (MFE +0.54%)
   - −3.0% : fill 30min 8% · séance 20% (26/159) · gap 0% · délai 101.3min · rebond 52% (13/26) (MFE +1.29%)
   - −4.0% : fill 30min 4% · séance 12% (12/159) · gap 0% · délai 107.9min · rebond 28% (2/12) (MFE +0.49%)
   - −5.0% : fill 30min 0% · séance 4% (4/159) · gap 0% · délai 119.3min · rebond 58% (2/4) (MFE +1.2%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.16% (p90 −1.31%) → stop au-delà de −0.94% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.15% (p90 −0.79%) → stop au-delà de −0.68% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.16% (p90 −0.78%) → stop au-delà de −0.73% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=328 jambes) : jambe baissière méd −1.12% (p90 −2.37%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (25 séances) :
      · −1.0% : fill 88% (21/25) · rebond 23% (7/21)
      · −2.0% : fill 69% (15/25) · rebond 19% (3/15)
      · −3.0% : fill 51% (11/25) · rebond 43% (4/11)
      · −4.0% : fill 41% (8/25) · rebond 46% (2/8)
      · −5.0% : fill 11% (3/25) · rebond 20% (1/3)
   - **flat** (35 séances) :
      · −1.0% : fill 57% (20/35) · rebond 23% (6/20)
      · −2.0% : fill 30% (12/35) · rebond 24% (4/12)
      · −3.0% : fill 22% (8/35) · rebond 22% (3/8)
      · −4.0% : fill 12% (3/35) · rebond 0% (0/3)
      · −5.0% : fill 0% (0/35) · rebond 0% (0/0)
   - **gap-up** (99 séances) :
      · −1.0% : fill 43% (33/99) · rebond 39% (14/33)
      · −2.0% : fill 24% (16/99) · rebond 35% (7/16)
      · −3.0% : fill 10% (7/99) · rebond 92% (6/7)
      · −4.0% : fill 3% (1/99) · rebond 0% (0/1)
      · −5.0% : fill 3% (1/99) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 40% en base · 61% si les 15 1res min sont vertes (82 cas) · 20% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **19min** → P(séance verte=clôture>ouverture) 71% si début vert vs 14% si rouge (base 40% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 299min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **71%** · continue >prix actuel 61% ; creux résiduel méd -0.98% (q20 -2.02%) → **SL/trailing à −2.02%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.09% / q75 +1.87% → **scale +1.09% / runner +1.87%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **14%** (continue à baisser 64%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.11%** (au-delà de la MAE q10 -3.11%), cible rebond +0.93% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.81% .. +1.6%] · haut q95 +2.12% · bas q05 -3.19%
   - 60min (n=160) : retour [-2.91% .. +2.05%] · haut q95 +2.46% · bas q05 -3.43%
   - 2h (n=160) : retour [-3.54% .. +2.1%] · haut q95 +2.53% · bas q05 -3.73%
   - 4h (n=160) : retour [-3.23% .. +2.19%] · haut q95 +2.93% · bas q05 -3.86%
   - 6h (n=160) : retour [-3.81% .. +3.34%] · haut q95 +3.4% · bas q05 -4.16%
   - session (n=160) : retour [-3.59% .. +2.46%] · haut q95 +3.6% · bas q05 -4.66%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.94%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.61 · part idiosyncratique 0.39
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 56.0  _(momentum haussier)_
- **ADX** : 16.0  _(pas de tendance nette)_
- **MACD** : hist 1.19  _(pas de croisement recent)_
- **BB** : %B 0.83 · largeur 14.9%
- **ATR** : 5.34 (93.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.078  _(accumulation)_
- **Vol ratio** : 0.66  _(volume normal)_
- **Choppiness** : 53.9  _(transition)_
- **MA** : MA20 122.09 · MA50 130.19 · MA200 135.52  _(prix > MA20)_
- **Dist MA** : MA20 +4.8% · MA50 -1.7% · MA200 -5.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (719468 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
