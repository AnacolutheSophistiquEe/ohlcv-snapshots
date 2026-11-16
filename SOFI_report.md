# SOFI

**Generated** : 2026-11-16T01:31:56.221690+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 3/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · $15.42  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (15 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot $15.42 (+0.5% vs entrée) · entrée $15.35 · stop $15.06 · T1 $15.85 · R/R 1.72  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.92% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-13 : 15.42 · ATR Wilder 0.811 (5.26 %)_
- **Swing** : plage **14.37 → 13.77** (-6.8 % a -10.67 % sous la cloture, 0.74 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 13.86-13.9 (A). stop INDICATIF 13.01 (-5.51 % sous le bas ; sous le support 13.42-13.75 (- 0,5 ATR)).
- **Deep** : plage **13.77 → 12.26** (-10.67 % a -20.49 % sous la cloture, 1.87 ATR) — touchee 46 % → 15 % du temps en 20 seances ; supports reels dans la plage : 13.42-13.75 (B) ; 12.5-12.86 (A). stop INDICATIF 11.02 (-10.08 % sous le bas ; sous le support 11.43-11.65 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (2.86 ATR sous le plus haut 20 s., RSI(2) 6.7 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 14.42-15.08 (B, -2.2 %) ; 13.86-13.9 (A, -9.86 %) ; 13.42-13.75 (B, -10.83 %) ; 12.5-12.86 (A, -16.6 %) ; 11.43-11.65 (B, -24.46 %) ; 10.49-10.85 (B, -29.64 %)
- Resistances reelles au-dessus : 16.25-16.61 (A, 5.38 %) ; 16.68-17.08 (A, 8.17 %) ; 17.11-17.19 (B, 10.96 %) ; 17.58-17.96 (A, 14.01 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=5.82 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.31 %)** : le gap seul le franchit 0.718 % des séances (9 fois sur 1254).
   - exécution **2.013 pt plus bas** dans le cas TYPIQUE (médiane), 2.798 au p90, **3.795 au pire**
   - perte réelle **8.985 %** en moyenne _(tirée par la queue)_, jusqu'à **11.105 %** — au lieu des 7.31 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.012 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 9 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.175 % | p01 -6.517 % | pire -11.105 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4479** [0.3752 ; 0.5223] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.3515** [0.3026 ; 0.4029] _(largeur 10.0 pt, n_eff 345.7)_
   - deep : **0.341** [0.2925 ; 0.3921] _(largeur 10.0 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.22 %** | CVaR **-8.58 %** | vol 4.07 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.5 % vs -14.28 % si l'on extrapolait par √5 _(rapport 1.015 ; < 1 = le √5 surestime)_
- **β de baisse : 1.786** (β de hausse 1.6958, asymétrie 1.0532) vs IWM — 605 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 14.1929 sur atr_grid (1.25 ATR, 7.958 %) — p(stop avant cible) 0.4447 [0.39 ; 0.50], R/R 7.669, perte reelle 8.258 % (gap inclus), CVaR 10.467 %, EV -0.6388 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.19 ATR (stop 4.289 %) — p(stop avant cible) 0.7067 [0.66 ; 0.75], R/R 13.769, perte reelle 4.599 % (gap inclus), EV -0.5125 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 13.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.707, borne haute 0.753 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.51 %) : P(cible) 0.0 % x 63.33 % + P(rien) 29.3 % x 9.34 % ne couvrent pas P(stop) 70.7 % x 4.60 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+63.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🔴 support a 0.55 ATR (stop 6.596 %) — p(stop avant cible) 0.5285 [0.48 ; 0.58], R/R 9.261, perte reelle 6.838 % (gap inclus), EV -0.5287 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 9.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.528, borne haute 0.581 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.24 ATR du spot — compartiment <1, mesure a 50.5 % de casse (IC clusterise [0.471 ; 0.539] sur 1216 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 0.0 % x 63.33 % + P(rien) 47.1 % x 6.54 % ne couvrent pas P(stop) 52.8 % x 6.84 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+63.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_based a 1.5 ATR (stop 9.55 %) — p(stop avant cible) 0.3546 [0.31 ; 0.41], R/R 6.363, perte reelle 9.952 % (gap inclus), EV -0.8907 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.26 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.89 %) : P(cible) 0.0 % x 63.33 % + P(rien) 64.5 % x 4.09 % ne couvrent pas P(stop) 35.5 % x 9.95 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+63.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🟢 support a 1.59 ATR (stop 13.211 %) — p(stop avant cible) 0.1642 [0.13 ; 0.21], R/R 4.703, perte reelle 13.466 % (gap inclus), EV -0.2843 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.05 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.28 %) : P(cible) 0.0 % x 63.33 % + P(rien) 83.6 % x 2.31 % ne couvrent pas P(stop) 16.4 % x 13.47 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+63.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ grid_snapped a 0.19 ATR (stop 3.105 %) — p(stop avant cible) 0.8141 [0.77 ; 0.85], R/R 18.934, perte reelle 3.345 % (gap inclus), EV -0.7709 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 18.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.814, borne haute 0.852 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.77 %) : P(cible) 0.0 % x 63.33 % + P(rien) 18.6 % x 10.50 % ne couvrent pas P(stop) 81.4 % x 3.34 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+63.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🔴 grid_snapped a 0.55 ATR (stop 5.412 %) — p(stop avant cible) 0.6268 [0.57 ; 0.68], R/R 11.024, perte reelle 5.745 % (gap inclus), EV -0.5912 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 11.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.627, borne haute 0.677 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.59 %) : P(cible) 0.0 % x 63.33 % + P(rien) 37.3 % x 8.06 % ne couvrent pas P(stop) 62.7 % x 5.74 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+63.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.25 ATR (stop 7.958 %) — p(stop avant cible) 0.4447 [0.39 ; 0.50], R/R 7.669, perte reelle 8.258 % (gap inclus), EV -0.6388 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.64 %) : P(cible) 0.0 % x 63.33 % + P(rien) 55.5 % x 5.46 % ne couvrent pas P(stop) 44.5 % x 8.26 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+63.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🟢 grid_snapped a 1.59 ATR (stop 12.027 %) — p(stop avant cible) 0.2177 [0.18 ; 0.26], R/R 5.147, perte reelle 12.303 % (gap inclus), EV -0.5624 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.23 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.56 %) : P(cible) 0.0 % x 63.33 % + P(rien) 78.2 % x 2.70 % ne couvrent pas P(stop) 21.8 % x 12.30 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+63.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.25 ATR (stop 14.325 %) — p(stop avant cible) 0.1107 [0.08 ; 0.15], R/R 4.354, perte reelle 14.544 % (gap inclus), EV -0.1709 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.81 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 0.0 % x 63.33 % + P(rien) 88.9 % x 1.62 % ne couvrent pas P(stop) 11.1 % x 14.54 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+63.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.5 ATR (stop 15.916 %) — p(stop avant cible) 0.0793 [0.05 ; 0.11], R/R 3.953, perte reelle 16.019 % (gap inclus), EV -0.0186 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 16.08 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.02 %) : P(cible) 0.0 % x 63.33 % + P(rien) 92.1 % x 1.36 % ne couvrent pas P(stop) 7.9 % x 16.02 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+63.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.75 ATR (stop 17.508 %) — p(stop avant cible) 0.0519 [0.03 ; 0.08], R/R 3.594, perte reelle 17.622 % (gap inclus), EV 0.006 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 17.63 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 19.1 %) — p(stop avant cible) 0.0448 [0.03 ; 0.07], R/R 3.308, perte reelle 19.143 % (gap inclus), EV -0.0236 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 18.79 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.02 %) : P(cible) 0.0 % x 63.33 % + P(rien) 95.5 % x 0.87 % ne couvrent pas P(stop) 4.5 % x 19.14 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+63.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 3.5 ATR (stop 22.283 %) — p(stop avant cible) 0.0252 [0.01 ; 0.05], R/R 2.819, perte reelle 22.462 % (gap inclus), EV -0.0533 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.69 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.05 %) : P(cible) 0.0 % x 63.33 % + P(rien) 97.5 % x 0.53 % ne couvrent pas P(stop) 2.5 % x 22.46 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+63.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 4.0 ATR (stop 25.466 %) — p(stop avant cible) 0.0128 [0.00 ; 0.03], R/R 2.474, perte reelle 25.594 % (gap inclus), EV -0.0254 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.55 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 0.0 % x 63.33 % + P(rien) 98.7 % x 0.31 % ne couvrent pas P(stop) 1.3 % x 25.59 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+63.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 4.5 ATR (stop 28.649 %) — p(stop avant cible) 0.0024 [0.00 ; 0.01], R/R 2.209, perte reelle 28.666 % (gap inclus), EV 0.0561 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.25 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 31.833 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 1.989, perte reelle 31.833 % (gap inclus), EV 0.0633 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.17 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 35.016 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 1.799, perte reelle 35.208 % (gap inclus), EV 0.0628 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.20 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 38.199 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.658, perte reelle 38.199 % (gap inclus), EV 0.0687 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.06 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 41.382 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.53, perte reelle 41.382 % (gap inclus), EV 0.0684 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.06 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 44.566 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.421, perte reelle 44.566 % (gap inclus), EV 0.0684 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.06 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 47.749 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.326, perte reelle 47.749 % (gap inclus), EV 0.0684 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.06 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 50.932 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.243, perte reelle 50.932 % (gap inclus), EV 0.0684 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.06 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 15.42, ATR14 0.9817 (6.367 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.374 ATR = 2.381 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.318 % | 15.3709 | 92.86 % | 95.77 % | 97.18 % | 97.47 % | 98.17 % | 98.87 % |
| 0.1 ATR | 0.637 % | 15.3218 | 84.91 % | 89.33 % | 92.14 % | 93.33 % | 95.33 % | 97.03 % |
| 0.15 ATR | 0.955 % | 15.2727 | 78.77 % | 84.59 % | 88.0 % | 90.3 % | 92.69 % | 94.77 % |
| 0.2 ATR | 1.273 % | 15.2237 | 71.43 % | 79.36 % | 83.37 % | 86.77 % | 90.36 % | 93.23 % |
| 0.25 ATR | 1.592 % | 15.1746 | 65.9 % | 75.03 % | 80.14 % | 84.44 % | 89.04 % | 92.1 % |
| 0.35 ATR | 2.228 % | 15.0764 | 52.41 % | 65.26 % | 72.28 % | 78.69 % | 85.58 % | 88.92 % |
| 0.5 ATR | 3.183 % | 14.9291 | 37.12 % | 53.27 % | 61.49 % | 69.39 % | 79.49 % | 84.82 % |
| 0.75 ATR | 4.775 % | 14.6837 | 20.12 % | 36.66 % | 46.37 % | 57.07 % | 69.95 % | 78.36 % |
| 1.0 ATR | 6.367 % | 14.4383 | 8.75 % | 24.27 % | 33.57 % | 45.05 % | 59.7 % | 69.85 % |
| 1.25 ATR | 7.958 % | 14.1929 | 4.23 % | 15.11 % | 24.09 % | 35.76 % | 50.86 % | 63.38 % |
| 1.5 ATR | 9.55 % | 13.9474 | 2.01 % | 9.47 % | 16.63 % | 27.37 % | 43.15 % | 57.23 % |
| 2.0 ATR | 12.733 % | 13.4566 | 0.7 % | 4.63 % | 8.57 % | 15.45 % | 29.85 % | 46.36 % |
| 2.5 ATR | 15.916 % | 12.9657 | 0.3 % | 1.91 % | 4.03 % | 9.6 % | 20.2 % | 36.82 % |
| 3.0 ATR | 19.1 % | 12.4749 | 0.1 % | 0.81 % | 2.82 % | 6.16 % | 14.01 % | 29.33 % |
| 4.0 ATR | 25.466 % | 11.4931 | 0.0 % | 0.3 % | 0.6 % | 2.42 % | 7.21 % | 15.08 % |
| 6.0 ATR | 38.199 % | 9.5297 | 0.0 % | 0.1 % | 0.2 % | 0.2 % | 0.91 % | 3.18 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.37 ATR | 0.42 ATR | 0.56 ATR | 0.68 ATR | 0.75 ATR | 0.97 ATR | 1.21 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.62 ATR | 0.82 ATR | 0.98 ATR | 1.12 ATR | 1.48 ATR | 1.96 ATR |
| **3 s.** | 0.32 ATR | 0.69 ATR | 0.78 ATR | 1.01 ATR | 1.23 ATR | 1.39 ATR | 1.91 ATR | 2.39 ATR |
| **5 s.** | 0.41 ATR | 0.90 ATR | 1.00 ATR | 1.33 ATR | 1.60 ATR | 1.81 ATR | 2.47 ATR | 3.31 ATR |
| **10 s.** | 0.62 ATR | 1.28 ATR | 1.44 ATR | 1.88 ATR | 2.25 ATR | 2.52 ATR | 3.59 ATR | 4.70 ATR |
| **20 s.** | 0.85 ATR | 1.83 ATR | 2.07 ATR | 2.75 ATR | 3.30 ATR | 3.65 ATR | 4.85 ATR | 5.69 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.423 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 21.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.624–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.775 %, prix 14.6837), p(touche) 36.66 % (en stress 91.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.777–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.367 %, prix 14.4382), p(touche) 33.57 % (en stress 96.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.001–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.958 %, prix 14.1929), p(touche) 35.76 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.44–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.55 %, prix 13.9474), p(touche) 43.15 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.071–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (15.916 %, prix 12.9658), p(touche) 36.82 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (76.5 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.035 | EV/share : $-0.011 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 25 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 25.7 | bear 69.3 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.42% → cible +3.197% / stop −1.918%, p_fill 83%, n_eff≈90.8) : P(cible|rempli) **13%** · **EV/risk -0.186** (×p_fill ; si rempli -0.43% du capital)
  - **swing** (entrée dip −0.944% → cible +7.186% / stop −6.427%, p_fill 84%, n_eff≈98.7) : P(cible|rempli) **19%** · **EV/risk -0.130** (×p_fill ; si rempli -0.99% du capital)
  - **deep** (entrée dip −1.381% → cible +18.218% / stop −9.683%, p_fill 89%, n_eff≈99.1) : P(cible|rempli) **6%** · **EV/risk -0.155** (×p_fill ; si rempli -1.69% du capital)
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
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.45 · part idiosyncratique 0.55
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 55.8  _(momentum haussier)_
- **ADX** : 18.8  _(pas de tendance nette)_
- **MACD** : hist -0.056  _(bearish_recent)_
- **BB** : %B 0.37 · largeur 26.0%
- **ATR** : 0.98 (66.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF 0.027  _(neutre)_
- **Vol ratio** : 0.68  _(volume normal)_
- **Choppiness** : 62.2  _(marche en range (choppy))_
- **MA** : MA20 15.95 · MA50 16.17 · MA200 17.32  _(prix < MA20)_
- **Dist MA** : MA20 -3.3% · MA50 -4.7% · MA200 -11.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (707368 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
