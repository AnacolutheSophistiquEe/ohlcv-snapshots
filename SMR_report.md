# SMR

**Generated** : 2026-10-15T00:27:09.400698+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 1/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $5.84  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 13/125 fenêtres (p_fill pondéré 8 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot $5.84 (+8.6% vs entrée) · entrée $5.38 · stop $5.23 · T1 $5.61 · R/R 1.53  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.62% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +15.6 % ≠ (strike 7.5 − spot 5.84)/spot = +28.3 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -760 % hors [0,100] (R² max 0.54). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 1/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-14 : 5.84 · ATR Wilder 0.5508 (9.42 %)_
- **Swing** : plage **5.2 → 4.85** (-11.08 % a -17.05 % sous la cloture, 0.63 ATR) — touchee 50 % → 30 % du temps en 10 seances ; aucun support reel dans la plage. stop INDICATIF 4.33 (-10.6 % sous le bas ; sous le support 4.61-4.69 (- 0,5 ATR)).
- **Deep** : plage **4.85 → 3.94** (-17.05 % a -32.6 % sous la cloture, 1.65 ATR) — touchee 44 % → 15 % du temps en 20 seances ; supports reels dans la plage : 4.61-4.69 (C). stop INDICATIF 3.48 (-11.55 % sous le bas ; sous le support 3.76-3.79 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 6.19 ATR sous le plus haut 20 s., RSI(2) 0.6. Limite **5.57** (seance suivante), stop catastrophe 3.37, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 5.3-5.5 (B, -5.9 %) ; 4.61-4.69 (C, -19.76 %) ; 3.76-3.79 (A, -35.16 %) ; 3.48-3.65 (B, -37.55 %) ; 3.18-3.42 (B, -41.4 %) ; 2.8-3.01 (B, -48.5 %)
- Resistances reelles au-dessus : 6.35-6.61 (A, 8.64 %) ; 6.88-6.88 (C, 17.71 %) ; 7.21-7.37 (A, 23.35 %) ; 7.54-7.81 (A, 29.0 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.55 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (24.09 %)** : le gap seul le franchit 0.086 % des séances (1 fois sur 1160).
   - exécution **6.233 pt plus bas** dans le cas TYPIQUE (médiane), 6.233 au p90, **6.233 au pire**
   - perte réelle **30.323 %** en moyenne _(tirée par la queue)_, jusqu'à **30.323 %** — au lieu des 24.09 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0054 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.521 % | p01 -6.957 % | pire -30.323 % _(sur 1160 séances)_
- **P(stop avant cible)** _(source : daily, 1161 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5416** [0.4672 ; 0.6146] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.3999** [0.3492 ; 0.4522] _(largeur 10.3 pt, n_eff 345.4)_
   - deep : **0.3471** [0.2983 ; 0.3984] _(largeur 10.0 pt, n_eff 345.4)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-9.52 %** | CVaR **-12.02 %** | vol 6.93 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 10.95 % contre 5.77 % aujourd'hui, rapport 1.90)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -19.23 % vs -18.74 % si l'on extrapolait par √5 _(rapport 1.026 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6016** (β de hausse 1.3844, asymétrie 1.1569) vs IWM — 555 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.036× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 5.6104 sur atr_grid (0.5 ATR, 4.014 %) — p(stop avant cible) 0.7706 [0.72 ; 0.81], R/R 2.604, perte reelle 4.175 % (gap inclus), CVaR 6.332 %, EV -0.7896 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.6094 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.771, borne haute 0.813 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 23 des 23 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 27.9 % de la queue et il ne reste que 13.84 EUR a partager. Prix du risque 0.004 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 12.043 %) — p(stop avant cible) 0.4385 [0.39 ; 0.49], R/R 0.895, perte reelle 12.149 % (gap inclus), EV -0.8633 % — **REFUSE**
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.98 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.86 %) : P(cible) 45.2 % x 10.87 % + P(rien) 10.9 % x -4.15 % ne couvrent pas P(stop) 43.9 % x 12.15 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 2.007 %) — p(stop avant cible) 0.8599 [0.82 ; 0.89], R/R 5.282, perte reelle 2.058 % (gap inclus), EV -0.3009 % — **REFUSE**
      - refuse : cible atteinte seulement 13.5 % du temps (< 15 %) meme a 10 seances : le R/R de 5.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.860, borne haute 0.893 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.30 %) : P(cible) 13.5 % x 10.87 % + P(rien) 0.5 % x 0.23 % ne couvrent pas P(stop) 86.0 % x 2.06 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 4.014 %) — p(stop avant cible) 0.7706 [0.72 ; 0.81], R/R 2.604, perte reelle 4.175 % (gap inclus), EV -0.7896 % — **REFUSE**
      - refuse : p_stop_first 0.771, borne haute 0.813 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.79 %) : P(cible) 22.3 % x 10.87 % + P(rien) 0.6 % x 0.31 % ne couvrent pas P(stop) 77.1 % x 4.18 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 6.022 %) — p(stop avant cible) 0.6597 [0.61 ; 0.71], R/R 1.766, perte reelle 6.157 % (gap inclus), EV -0.5827 % — **REFUSE**
      - refuse : p_stop_first 0.660, borne haute 0.708 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.58 %) : P(cible) 32.0 % x 10.87 % + P(rien) 2.0 % x -0.07 % ne couvrent pas P(stop) 66.0 % x 6.16 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 8.029 %) — p(stop avant cible) 0.5906 [0.54 ; 0.64], R/R 1.326, perte reelle 8.197 % (gap inclus), EV -0.7152 % — **REFUSE**
      - refuse : p_stop_first 0.591, borne haute 0.641 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.72 %) : P(cible) 38.2 % x 10.87 % + P(rien) 2.8 % x -0.87 % ne couvrent pas P(stop) 59.1 % x 8.20 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 10.036 %) — p(stop avant cible) 0.5105 [0.46 ; 0.56], R/R 1.074, perte reelle 10.123 % (gap inclus), EV -0.8356 % — **REFUSE**
      - refuse : p_stop_first 0.510, borne haute 0.563 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.84 %) : P(cible) 42.0 % x 10.87 % + P(rien) 7.0 % x -3.34 % ne couvrent pas P(stop) 51.0 % x 10.12 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 14.05 %) — p(stop avant cible) 0.3653 [0.32 ; 0.42], R/R 0.768, perte reelle 14.151 % (gap inclus), EV -0.7255 % — **REFUSE**
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.79 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.73 %) : P(cible) 47.8 % x 10.87 % + P(rien) 15.7 % x -4.82 % ne couvrent pas P(stop) 36.5 % x 14.15 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 16.058 %) — p(stop avant cible) 0.2994 [0.25 ; 0.35], R/R 0.67, perte reelle 16.226 % (gap inclus), EV -0.8524 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.06 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.85 %) : P(cible) 48.7 % x 10.87 % + P(rien) 21.4 % x -6.04 % ne couvrent pas P(stop) 29.9 % x 16.23 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 18.065 %) — p(stop avant cible) 0.2447 [0.20 ; 0.29], R/R 0.597, perte reelle 18.204 % (gap inclus), EV -0.7322 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.75 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.73 %) : P(cible) 49.3 % x 10.87 % + P(rien) 26.2 % x -6.24 % ne couvrent pas P(stop) 24.5 % x 18.20 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 20.072 %) — p(stop avant cible) 0.1788 [0.14 ; 0.22], R/R 0.536, perte reelle 20.279 % (gap inclus), EV -0.6156 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.81 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.62 %) : P(cible) 49.5 % x 10.87 % + P(rien) 32.6 % x -7.28 % ne couvrent pas P(stop) 17.9 % x 20.28 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 22.079 %) — p(stop avant cible) 0.1477 [0.11 ; 0.19], R/R 0.49, perte reelle 22.194 % (gap inclus), EV -0.6347 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.42 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.63 %) : P(cible) 49.6 % x 10.87 % + P(rien) 35.6 % x -7.70 % ne couvrent pas P(stop) 14.8 % x 22.19 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 24.087 %) — p(stop avant cible) 0.1136 [0.08 ; 0.15], R/R 0.445, perte reelle 24.425 % (gap inclus), EV -0.6169 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.85 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.62 %) : P(cible) 49.8 % x 10.87 % + P(rien) 38.9 % x -8.37 % ne couvrent pas P(stop) 11.4 % x 24.42 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 28.101 %) — p(stop avant cible) 0.0608 [0.04 ; 0.09], R/R 0.381, perte reelle 28.502 % (gap inclus), EV -0.4342 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.59 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.43 %) : P(cible) 49.9 % x 10.87 % + P(rien) 44.1 % x -9.35 % ne couvrent pas P(stop) 6.1 % x 28.50 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 32.115 %) — p(stop avant cible) 0.0331 [0.02 ; 0.06], R/R 0.337, perte reelle 32.257 % (gap inclus), EV -0.4176 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.70 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.42 %) : P(cible) 49.9 % x 10.87 % + P(rien) 46.8 % x -10.19 % ne couvrent pas P(stop) 3.3 % x 32.26 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 36.13 %) — p(stop avant cible) 0.0247 [0.01 ; 0.05], R/R 0.301, perte reelle 36.163 % (gap inclus), EV -0.4473 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.81 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.45 %) : P(cible) 49.9 % x 10.87 % + P(rien) 47.7 % x -10.44 % ne couvrent pas P(stop) 2.5 % x 36.16 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 40.144 %) — p(stop avant cible) 0.0149 [0.01 ; 0.03], R/R 0.27, perte reelle 40.247 % (gap inclus), EV -0.4804 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.52 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.48 %) : P(cible) 49.9 % x 10.87 % + P(rien) 48.6 % x -10.90 % ne couvrent pas P(stop) 1.5 % x 40.25 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 44.159 %) — p(stop avant cible) 0.0106 [0.00 ; 0.03], R/R 0.246, perte reelle 44.207 % (gap inclus), EV -0.4735 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.45 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.47 %) : P(cible) 49.9 % x 10.87 % + P(rien) 49.1 % x -11.06 % ne couvrent pas P(stop) 1.1 % x 44.21 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 48.173 %) — p(stop avant cible) 0.002 [0.00 ; 0.01], R/R 0.22, perte reelle 49.514 % (gap inclus), EV -0.4803 % — **REFUSE**
      - refuse : R/R 0.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.59 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.48 %) : P(cible) 49.9 % x 10.87 % + P(rien) 49.9 % x -11.62 % ne couvrent pas P(stop) 0.2 % x 49.51 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 52.187 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.208, perte reelle 52.187 % (gap inclus), EV -0.4711 % — **REFUSE**
      - refuse : R/R 0.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.49 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.47 %) : P(cible) 49.9 % x 10.87 % + P(rien) 50.1 % x -11.75 % ne couvrent pas P(stop) 0.0 % x 52.19 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 56.202 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.193, perte reelle 56.202 % (gap inclus), EV -0.4715 % — **REFUSE**
      - refuse : R/R 0.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.51 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.47 %) : P(cible) 49.9 % x 10.87 % + P(rien) 50.1 % x -11.75 % ne couvrent pas P(stop) 0.0 % x 56.20 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 60.216 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.181, perte reelle 60.216 % (gap inclus), EV -0.4704 % — **REFUSE**
      - refuse : R/R 0.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.44 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.47 %) : P(cible) 49.9 % x 10.87 % + P(rien) 50.1 % x -11.75 % ne couvrent pas P(stop) 0.0 % x 60.22 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 64.231 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.169, perte reelle 64.231 % (gap inclus), EV -0.4704 % — **REFUSE**
      - refuse : R/R 0.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.44 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.47 %) : P(cible) 49.9 % x 10.87 % + P(rien) 50.1 % x -11.75 % ne couvrent pas P(stop) 0.0 % x 64.23 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 5.845, ATR14 0.4693 (8.029 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.426 ATR = 3.42 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.401 % | 5.8215 | 92.56 % | 95.11 % | 96.33 % | 97.1 % | 97.98 % | 98.41 % |
| 0.1 ATR | 0.803 % | 5.7981 | 86.89 % | 91.32 % | 93.32 % | 94.75 % | 96.3 % | 97.5 % |
| 0.15 ATR | 1.204 % | 5.7746 | 80.89 % | 87.1 % | 89.76 % | 91.85 % | 94.05 % | 96.14 % |
| 0.2 ATR | 1.606 % | 5.7511 | 75.11 % | 82.76 % | 86.53 % | 89.4 % | 92.48 % | 95.12 % |
| 0.25 ATR | 2.007 % | 5.7277 | 69.89 % | 79.64 % | 83.96 % | 87.28 % | 90.8 % | 93.98 % |
| 0.35 ATR | 2.81 % | 5.6807 | 58.11 % | 72.19 % | 77.62 % | 82.92 % | 87.77 % | 91.6 % |
| 0.5 ATR | 4.014 % | 5.6104 | 42.11 % | 59.07 % | 67.26 % | 74.22 % | 83.39 % | 88.65 % |
| 0.75 ATR | 6.022 % | 5.493 | 20.56 % | 37.49 % | 47.66 % | 59.93 % | 72.62 % | 81.27 % |
| 1.0 ATR | 8.029 % | 5.3757 | 11.22 % | 25.92 % | 35.86 % | 49.55 % | 64.87 % | 75.48 % |
| 1.25 ATR | 10.036 % | 5.2584 | 4.67 % | 16.02 % | 25.17 % | 38.5 % | 55.11 % | 69.13 % |
| 1.5 ATR | 12.043 % | 5.1411 | 2.22 % | 9.79 % | 16.37 % | 28.35 % | 45.79 % | 62.43 % |
| 2.0 ATR | 16.058 % | 4.9064 | 0.33 % | 3.23 % | 6.57 % | 14.73 % | 31.2 % | 49.26 % |
| 2.5 ATR | 20.072 % | 4.6718 | 0.11 % | 1.33 % | 2.9 % | 7.03 % | 20.43 % | 38.37 % |
| 3.0 ATR | 24.087 % | 4.4371 | 0.11 % | 0.56 % | 1.89 % | 3.79 % | 11.67 % | 28.6 % |
| 4.0 ATR | 32.115 % | 3.9679 | 0.0 % | 0.22 % | 0.33 % | 1.12 % | 4.49 % | 13.62 % |
| 6.0 ATR | 48.173 % | 3.0293 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.34 % | 1.59 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.43 ATR | 0.47 ATR | 0.61 ATR | 0.70 ATR | 0.77 ATR | 1.05 ATR | 1.24 ATR |
| **2 s.** | 0.31 ATR | 0.60 ATR | 0.66 ATR | 0.85 ATR | 1.02 ATR | 1.15 ATR | 1.49 ATR | 1.86 ATR |
| **3 s.** | 0.39 ATR | 0.72 ATR | 0.81 ATR | 1.07 ATR | 1.25 ATR | 1.40 ATR | 1.82 ATR | 2.21 ATR |
| **5 s.** | 0.49 ATR | 0.99 ATR | 1.10 ATR | 1.39 ATR | 1.62 ATR | 1.81 ATR | 2.31 ATR | 2.81 ATR |
| **10 s.** | 0.69 ATR | 1.39 ATR | 1.53 ATR | 1.94 ATR | 2.29 ATR | 2.52 ATR | 3.23 ATR | 3.93 ATR |
| **20 s.** | 1.02 ATR | 1.97 ATR | 2.20 ATR | 2.77 ATR | 3.24 ATR | 3.57 ATR | 4.60 ATR | 5.43 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.473–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (4.014 %, prix 5.6104), p(touche) 42.11 % (en stress 82.22 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (60.6 % des re-echantillons)
- **2 seance(s)** : plage utile 0.663–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (6.022 %, prix 5.493), p(touche) 37.49 % (en stress 88.89 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (71.6 % des re-echantillons)
- **3 seance(s)** : plage utile 0.806–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (8.029 %, prix 5.3757), p(touche) 35.86 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.103–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (10.036 %, prix 5.2584), p(touche) 38.5 % (en stress 95.56 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.527–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (16.058 %, prix 4.9064), p(touche) 31.2 % (en stress 96.67 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.196–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.006 | EV/share : $-0.001 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 33 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 72.8 | bear 22.2 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=13, n_eff=10))
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→78% · +2.0%→62% · +3.0%→54% · +5.0%→34% · +8.0%→14%
- Range intraday médian 7.02% (p90 12.09%) · excursion haute méd. +3.23% / basse méd. −3.1%
- Profil de vol intra : ouverture 4.766% vs midi 1.404% vs clôture 1.695% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 76% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.13 ; neutre — autocorr -0.024)_ ; drift intra méd. -0.568% ; recovery-V 32%
- **σ réalisé intraday** 4.046% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 62% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 7.8201 (VA 7.7996–7.8714 ; dernier close 7.75)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 45% · rebond 75% · **stop −4.75%** sous le fill (sous le bruit) · cible +2.64% · R/R 0.56 (high win-rate)
- Gaps overnight (n=159) : méd. -0.3% · baisse 53% (gap-down >1% 35% · >2% 22%)
- Excursion ouverture 5min (n=160) : bas méd −1.0% (p90 −2.94%) · haut méd +1.32% · range méd 2.67%
- Excursion ouverture 15min (n=160) : bas méd −1.4% (p90 −4.33%) · haut méd +1.53% · range méd 3.57%
- Excursion ouverture 30min (n=160) : bas méd −1.69% (p90 −4.84%) · haut méd +1.7% · range méd 4.04%
- Excursion ouverture 60min (n=160) : bas méd −2.12% (p90 −5.34%) · haut méd +2.25% · range méd 4.69%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 7.75 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 79% (127/159) · gap 48% · délai 0.0min · rebond 60% (77/127) (MFE +1.63%)
   - −1.0% : fill 30min 63% · séance 75% (121/159) · gap 36% · délai 0.0min · rebond 62% (75/121) (MFE +1.79%)
   - −1.5% : fill 30min 60% · séance 72% (115/159) · gap 26% · délai 0.1min · rebond 67% (80/115) (MFE +1.81%)
   - −2.0% : fill 30min 52% · séance 64% (105/159) · gap 22% · délai 1.0min · rebond 61% (69/105) (MFE +1.75%)
   - −3.0% : fill 30min 40% · séance 52% (90/159) · gap 10% · délai 4.8min · rebond 74% (69/90) (MFE +1.92%)
   - −4.0% : fill 30min 31% · séance 45% (79/159) · gap 4% · délai 7.8min · rebond 75% (60/79) (MFE +2.64%)
   - −5.0% : fill 30min 19% · séance 34% (60/159) · gap 2% · délai 23.4min · rebond 76% (44/60) (MFE +2.19%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.66% (p90 −2.48%) → stop au-delà de −1.86% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −2.29%) → stop au-delà de −1.89% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.99% (p90 −2.71%) → stop au-delà de −2.1% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1089 jambes) : jambe baissière méd −1.28% (p90 −3.12%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (86 séances) :
      · −1.0% : fill 96% (83/86) · rebond 59% (51/83)
      · −2.0% : fill 89% (78/86) · rebond 68% (56/78)
      · −3.0% : fill 83% (73/86) · rebond 79% (59/73)
      · −4.0% : fill 70% (63/86) · rebond 82% (51/63)
      · −5.0% : fill 53% (47/86) · rebond 80% (37/47)
   - **flat** (11 séances) :
      · −1.0% : fill 94% (9/11) · rebond 66% (5/9)
      · −2.0% : fill 52% (6/11) · rebond 39% (2/6)
      · −3.0% : fill 52% (6/11) · rebond 50% (3/6)
      · −4.0% : fill 52% (6/11) · rebond 62% (4/6)
      · −5.0% : fill 39% (4/11) · rebond 78% (3/4)
   - **gap-up** (62 séances) :
      · −1.0% : fill 49% (29/62) · rebond 70% (19/29)
      · −2.0% : fill 36% (21/62) · rebond 46% (11/21)
      · −3.0% : fill 15% (11/62) · rebond 49% (7/11)
      · −4.0% : fill 14% (10/62) · rebond 41% (5/10)
      · −5.0% : fill 11% (9/62) · rebond 49% (4/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 72% si les 15 1res min sont vertes (73 cas) · 29% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **51min** → P(séance verte=clôture>ouverture) 84% si début vert vs 19% si rouge (base 47% · écart 65 pts) ; prédictivité sature ensuite (plafond brut 222min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **84%** · continue >prix actuel 59% ; creux résiduel méd -1.71% (q20 -3.75%) → **SL/trailing à −3.75%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.66% / q75 +4.53% → **scale +2.66% / runner +4.53%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **19%** (continue à baisser 53%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.21%** (au-delà de la MAE q10 -5.21%), cible rebond +2.1% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.68% .. +4.36%] · haut q95 +6.14% · bas q05 -5.36%
   - 60min (n=160) : retour [-5.02% .. +4.72%] · haut q95 +6.47% · bas q05 -5.85%
   - 2h (n=160) : retour [-7.52% .. +5.37%] · haut q95 +7.8% · bas q05 -7.94%
   - 4h (n=160) : retour [-7.67% .. +6.92%] · haut q95 +8.32% · bas q05 -9.19%
   - 6h (n=160) : retour [-6.72% .. +8.0%] · haut q95 +9.66% · bas q05 -9.21%
   - session (n=160) : retour [-7.99% .. +8.0%] · haut q95 +10.29% · bas q05 -9.32%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 4.62%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.29 · part idiosyncratique 0.71
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 13.4  _(survente)_
- **ADX** : 22.0  _(pas de tendance nette)_
- **MACD** : hist -0.173  _(pas de croisement recent)_
- **BB** : %B -0.1 · largeur 42.2%
- **ATR** : 0.47 (2.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.31  _(distribution)_
- **Vol ratio** : 1.1  _(volume normal)_
- **Choppiness** : 30.2  _(marche directionnel)_
- **MA** : MA20 7.83 · MA50 8.79 · MA200 11.59  _(prix < MA20)_
- **Dist MA** : MA20 -25.3% · MA50 -33.5% · MA200 -49.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (888350 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
