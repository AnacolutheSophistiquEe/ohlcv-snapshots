# SOFI

**Generated** : 2026-10-20T00:30:18.446022+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 2/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $14.30  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 15/125 fenêtres (p_fill pondéré 10 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot $14.30 (+4.5% vs entrée) · entrée $13.68 · stop $12.58 · T1 $13.99 · R/R 0.28  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +6.5 % ≠ (strike 15.5 − spot 14.30)/spot = +8.4 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-19 : 14.3 · ATR Wilder 0.6737 (4.71 %)_
- **Swing** : plage **13.42 → 12.94** (-6.12 % a -9.5 % sous la cloture, 0.72 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 12.86-13.01 (B). stop INDICATIF 12.16 (-5.99 % sous le bas ; sous le support 12.5-12.74 (- 0,5 ATR)).
- **Deep** : plage **12.94 → 11.69** (-9.5 % a -18.25 % sous la cloture, 1.86 ATR) — touchee 45 % → 15 % du temps en 20 seances ; supports reels dans la plage : 12.86-13.01 (B) ; 12.5-12.74 (A). stop INDICATIF 11.09 (-5.08 % sous le bas ; sous le support 11.43-11.65 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 5.44 ATR sous le plus haut 20 s., RSI(2) 24.8. Limite **13.96** (seance suivante), stop catastrophe 11.26, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 13.42-13.75 (B, -3.81 %) ; 12.86-13.01 (B, -8.99 %) ; 12.5-12.74 (A, -10.88 %) ; 11.43-11.65 (B, -18.51 %) ; 10.16-10.49 (C, -26.62 %) ; 9.18-9.45 (C, -33.89 %)
- Resistances reelles au-dessus : 14.78-14.93 (A, 3.39 %) ; 15.2-15.53 (A, 6.33 %) ; 15.62-15.65 (A, 9.26 %) ; 16.25-16.53 (A, 13.68 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=5.83 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.94 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1253).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 12.94 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.204 % | p01 -6.52 % | pire -11.105 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0107** [0.0021 ; 0.0352] _(largeur 3.3 pt, n_eff 173.1)_
   - swing : **0.4912** [0.4388 ; 0.5438] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.46** [0.408 ; 0.5127] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 12.8 observations effectives », dont la borne haute a 95 % vaut environ 23.4 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (42.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1140 séances)** : VaR **-6.08 %** | CVaR **-8.5 %** | vol 4.02 %/j
   - _fenêtre arrêtée : rupture de regime a 1200 seances en arriere (volatilite 5.71 % contre 3.52 % aujourd'hui, rapport 1.62)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.5 % vs -14.29 % si l'on extrapolait par √5 _(rapport 1.015 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7992** (β de hausse 1.7194, asymétrie 1.0464) vs IWM — 606 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.357× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 13.2164 sur atr_grid (1.75 ATR, 7.545 %) — p(stop avant cible) 0.4788 [0.43 ; 0.53], R/R 4.254, perte reelle 7.905 % (gap inclus), CVaR 10.659 %, EV -1.149 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.97 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 4.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 6.467 %) — p(stop avant cible) 0.5402 [0.49 ; 0.59], R/R 4.995, perte reelle 6.732 % (gap inclus), EV -0.9246 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 4.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.540, borne haute 0.592 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.92 %) : P(cible) 0.4 % x 33.63 % + P(rien) 45.5 % x 5.62 % ne couvrent pas P(stop) 54.0 % x 6.73 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 1.078 %) — p(stop avant cible) 0.9377 [0.91 ; 0.96], R/R 29.303, perte reelle 1.148 % (gap inclus), EV -0.2308 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 29.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.938, borne haute 0.960 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.23 %) : P(cible) 0.1 % x 33.63 % + P(rien) 6.1 % x 13.11 % ne couvrent pas P(stop) 93.8 % x 1.15 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 2.156 %) — p(stop avant cible) 0.8906 [0.85 ; 0.92], R/R 14.302, perte reelle 2.351 % (gap inclus), EV -0.7359 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 14.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.891, borne haute 0.920 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.74 %) : P(cible) 0.3 % x 33.63 % + P(rien) 10.7 % x 11.86 % ne couvrent pas P(stop) 89.1 % x 2.35 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 3.234 %) — p(stop avant cible) 0.8081 [0.76 ; 0.85], R/R 9.613, perte reelle 3.498 % (gap inclus), EV -1.072 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 9.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.808, borne haute 0.847 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.07 %) : P(cible) 0.4 % x 33.63 % + P(rien) 18.8 % x 8.68 % ne couvrent pas P(stop) 80.8 % x 3.50 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 4.312 %) — p(stop avant cible) 0.7221 [0.67 ; 0.77], R/R 7.237, perte reelle 4.646 % (gap inclus), EV -0.9541 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 7.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.722, borne haute 0.767 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.95 %) : P(cible) 0.4 % x 33.63 % + P(rien) 27.4 % x 8.24 % ne couvrent pas P(stop) 72.2 % x 4.65 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 5.39 %) — p(stop avant cible) 0.6342 [0.58 ; 0.68], R/R 5.847, perte reelle 5.751 % (gap inclus), EV -0.9563 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 5.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.634, borne haute 0.684 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.96 %) : P(cible) 0.4 % x 33.63 % + P(rien) 36.1 % x 7.04 % ne couvrent pas P(stop) 63.4 % x 5.75 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 7.545 %) — p(stop avant cible) 0.4788 [0.43 ; 0.53], R/R 4.254, perte reelle 7.905 % (gap inclus), EV -1.149 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 4.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.15 %) : P(cible) 0.4 % x 33.63 % + P(rien) 51.7 % x 4.81 % ne couvrent pas P(stop) 47.9 % x 7.91 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 8.623 %) — p(stop avant cible) 0.4124 [0.36 ; 0.46], R/R 3.7, perte reelle 9.088 % (gap inclus), EV -1.2761 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.10 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.28 %) : P(cible) 0.4 % x 33.63 % + P(rien) 58.3 % x 3.98 % ne couvrent pas P(stop) 41.2 % x 9.09 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 9.701 %) — p(stop avant cible) 0.3513 [0.30 ; 0.40], R/R 3.318, perte reelle 10.133 % (gap inclus), EV -1.3886 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.52 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.39 %) : P(cible) 0.5 % x 33.63 % + P(rien) 64.4 % x 3.12 % ne couvrent pas P(stop) 35.1 % x 10.13 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 10.779 %) — p(stop avant cible) 0.3026 [0.26 ; 0.35], R/R 3.022, perte reelle 11.126 % (gap inclus), EV -1.3087 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.84 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.31 %) : P(cible) 0.5 % x 33.63 % + P(rien) 69.2 % x 2.73 % ne couvrent pas P(stop) 30.3 % x 11.13 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 11.857 %) — p(stop avant cible) 0.2444 [0.20 ; 0.29], R/R 2.769, perte reelle 12.142 % (gap inclus), EV -1.2191 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.25 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.22 %) : P(cible) 0.5 % x 33.63 % + P(rien) 75.1 % x 2.11 % ne couvrent pas P(stop) 24.4 % x 12.14 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 12.935 %) — p(stop avant cible) 0.1888 [0.15 ; 0.23], R/R 2.548, perte reelle 13.197 % (gap inclus), EV -0.8588 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.93 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.86 %) : P(cible) 0.5 % x 33.63 % + P(rien) 80.6 % x 1.82 % ne couvrent pas P(stop) 18.9 % x 13.20 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 15.091 %) — p(stop avant cible) 0.1106 [0.08 ; 0.15], R/R 2.206, perte reelle 15.243 % (gap inclus), EV -0.6306 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.43 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.63 %) : P(cible) 0.5 % x 33.63 % + P(rien) 88.5 % x 1.01 % ne couvrent pas P(stop) 11.1 % x 15.24 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 17.247 %) — p(stop avant cible) 0.0663 [0.04 ; 0.10], R/R 1.937, perte reelle 17.361 % (gap inclus), EV -0.5307 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.40 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 0.5 % x 33.63 % + P(rien) 92.9 % x 0.49 % ne couvrent pas P(stop) 6.6 % x 17.36 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 19.403 %) — p(stop avant cible) 0.0493 [0.03 ; 0.08], R/R 1.73, perte reelle 19.436 % (gap inclus), EV -0.5601 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.42 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.56 %) : P(cible) 0.5 % x 33.63 % + P(rien) 94.6 % x 0.25 % ne couvrent pas P(stop) 4.9 % x 19.44 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 21.558 %) — p(stop avant cible) 0.0304 [0.02 ; 0.05], R/R 1.551, perte reelle 21.676 % (gap inclus), EV -0.5794 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.05 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.58 %) : P(cible) 0.5 % x 33.63 % + P(rien) 96.5 % x -0.09 % ne couvrent pas P(stop) 3.0 % x 21.68 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 23.714 %) — p(stop avant cible) 0.0212 [0.01 ; 0.04], R/R 1.402, perte reelle 23.989 % (gap inclus), EV -0.5789 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.38 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.58 %) : P(cible) 0.5 % x 33.63 % + P(rien) 97.4 % x -0.24 % ne couvrent pas P(stop) 2.1 % x 23.99 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 25.87 %) — p(stop avant cible) 0.013 [0.00 ; 0.03], R/R 1.295, perte reelle 25.97 % (gap inclus), EV -0.5297 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.93 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 0.5 % x 33.63 % + P(rien) 98.2 % x -0.36 % ne couvrent pas P(stop) 1.3 % x 25.97 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 28.026 %) — p(stop avant cible) 0.0033 [0.00 ; 0.01], R/R 1.199, perte reelle 28.046 % (gap inclus), EV -0.4665 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.81 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.47 %) : P(cible) 0.5 % x 33.63 % + P(rien) 99.2 % x -0.54 % ne couvrent pas P(stop) 0.3 % x 28.05 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 30.182 %) — p(stop avant cible) 0.0026 [0.00 ; 0.01], R/R 1.109, perte reelle 30.312 % (gap inclus), EV -0.4628 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.74 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.46 %) : P(cible) 0.5 % x 33.63 % + P(rien) 99.2 % x -0.55 % ne couvrent pas P(stop) 0.3 % x 30.31 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 32.338 %) — p(stop avant cible) 0.0019 [0.00 ; 0.01], R/R 1.04, perte reelle 32.338 % (gap inclus), EV -0.4519 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.61 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.45 %) : P(cible) 0.5 % x 33.63 % + P(rien) 99.3 % x -0.56 % ne couvrent pas P(stop) 0.2 % x 32.34 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 34.494 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 0.962, perte reelle 34.946 % (gap inclus), EV -0.4535 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.63 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.45 %) : P(cible) 0.5 % x 33.63 % + P(rien) 99.4 % x -0.58 % ne couvrent pas P(stop) 0.1 % x 34.95 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 14.295, ATR14 0.6164 (4.312 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.379 ATR = 1.634 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.216 % | 14.2642 | 93.05 % | 95.87 % | 97.17 % | 97.57 % | 98.27 % | 98.87 % |
| 0.1 ATR | 0.431 % | 14.2334 | 85.2 % | 89.31 % | 92.13 % | 93.43 % | 95.53 % | 97.13 % |
| 0.15 ATR | 0.647 % | 14.2025 | 78.95 % | 84.58 % | 88.09 % | 90.5 % | 92.89 % | 94.87 % |
| 0.2 ATR | 0.862 % | 14.1717 | 71.7 % | 79.33 % | 83.45 % | 86.96 % | 90.55 % | 93.33 % |
| 0.25 ATR | 1.078 % | 14.1409 | 66.36 % | 75.1 % | 80.32 % | 84.53 % | 89.23 % | 92.2 % |
| 0.35 ATR | 1.509 % | 14.0793 | 52.97 % | 65.42 % | 72.45 % | 78.77 % | 85.77 % | 89.01 % |
| 0.5 ATR | 2.156 % | 13.9868 | 37.66 % | 53.33 % | 61.86 % | 69.57 % | 79.78 % | 84.91 % |
| 0.75 ATR | 3.234 % | 13.8327 | 20.54 % | 37.1 % | 47.02 % | 57.43 % | 70.43 % | 78.44 % |
| 1.0 ATR | 4.312 % | 13.6786 | 8.96 % | 24.7 % | 34.21 % | 45.3 % | 60.26 % | 69.92 % |
| 1.25 ATR | 5.39 % | 13.5246 | 4.33 % | 15.32 % | 24.42 % | 36.0 % | 51.22 % | 63.45 % |
| 1.5 ATR | 6.468 % | 13.3705 | 2.11 % | 9.68 % | 16.85 % | 27.5 % | 43.39 % | 57.19 % |
| 2.0 ATR | 8.623 % | 13.0623 | 0.7 % | 4.64 % | 8.68 % | 15.57 % | 29.78 % | 46.1 % |
| 2.5 ATR | 10.779 % | 12.7541 | 0.3 % | 2.02 % | 4.14 % | 9.81 % | 20.12 % | 36.24 % |
| 3.0 ATR | 12.935 % | 12.4459 | 0.1 % | 0.91 % | 2.93 % | 6.37 % | 14.02 % | 28.44 % |
| 4.0 ATR | 17.247 % | 11.8296 | 0.0 % | 0.3 % | 0.71 % | 2.53 % | 7.42 % | 14.99 % |
| 6.0 ATR | 25.87 % | 10.5969 | 0.0 % | 0.1 % | 0.2 % | 0.2 % | 0.91 % | 3.08 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.69 ATR | 0.76 ATR | 0.98 ATR | 1.21 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.63 ATR | 0.83 ATR | 0.99 ATR | 1.12 ATR | 1.49 ATR | 1.96 ATR |
| **3 s.** | 0.32 ATR | 0.70 ATR | 0.79 ATR | 1.03 ATR | 1.24 ATR | 1.40 ATR | 1.92 ATR | 2.40 ATR |
| **5 s.** | 0.41 ATR | 0.90 ATR | 1.01 ATR | 1.34 ATR | 1.60 ATR | 1.81 ATR | 2.48 ATR | 3.36 ATR |
| **10 s.** | 0.63 ATR | 1.29 ATR | 1.45 ATR | 1.88 ATR | 2.25 ATR | 2.51 ATR | 3.61 ATR | 4.74 ATR |
| **20 s.** | 0.85 ATR | 1.82 ATR | 2.06 ATR | 2.71 ATR | 3.26 ATR | 3.63 ATR | 4.84 ATR | 5.68 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.428–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.156 %, prix 13.9868), p(touche) 37.66 % (en stress 83.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.628–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.234 %, prix 13.8327), p(touche) 37.1 % (en stress 91.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 19.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.789–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.312 %, prix 13.6786), p(touche) 34.21 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.008–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (5.39 %, prix 13.5245), p(touche) 36.0 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.449–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (6.468 %, prix 13.3704), p(touche) 43.39 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.056–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (10.779 %, prix 12.7541), p(touche) 36.24 % (en stress 98.98 %)  ✅ optimum identifie (76.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.024 | EV/share : $-0.026 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 13 % | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 16.0 | bear 5.0 | side 79.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈60.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.316% → cible +2.253% / stop −7.999%, p_fill 10%, n_eff≈12.8) : P(cible|rempli) **22%** · **EV/risk +0.001** (×p_fill ; si rempli +0.09% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=4, n_eff=4))
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

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.56 · part idiosyncratique 0.43
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-27 — SOFI earnings (J-5 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-27 — SOFI earnings (J-5 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 31.2  _(momentum baissier)_
- **ADX** : 23.8  _(pas de tendance nette)_
- **MACD** : hist -0.091  _(pas de croisement recent)_
- **BB** : %B 0.05 · largeur 19.7%
- **ATR** : 0.62 (7.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.289  _(distribution)_
- **Vol ratio** : 0.76  _(volume normal)_
- **Choppiness** : 48.6  _(transition)_
- **MA** : MA20 15.68 · MA50 17.01 · MA200 18.31  _(prix < MA20)_
- **Dist MA** : MA20 -8.8% · MA50 -16.0% · MA200 -21.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (759147 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
