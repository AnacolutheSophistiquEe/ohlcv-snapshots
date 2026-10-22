# CEG

**Generated** : 2026-10-22T00:26:25.241771+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $270.65  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 4/125 fenêtres (p_fill pondéré 3 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot $270.65 (+6.3% vs entrée) · entrée $254.54 · stop $234.18 · T1 $262.59 · R/R 0.4  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +5.3 % ≠ (strike 272.5 − spot 270.65)/spot = +0.7 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-21 : 270.65 · ATR Wilder 13.2 (4.88 %)_
- **Swing** : plage **252.96 → 243.36** (-6.54 % a -10.08 % sous la cloture, 0.73 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 247.2-250.55 (A) ; 240.14-246.18 (A). stop INDICATIF 226.19 (-7.06 % sous le bas ; sous le support 232.79-236.2 (- 0,5 ATR)).
- **Deep** : plage **243.36 → 218.47** (-10.08 % a -19.28 % sous la cloture, 1.89 ATR) — touchee 46 % → 15 % du temps en 20 seances ; supports reels dans la plage : 240.14-246.18 (A) ; 232.79-236.2 (A) ; 224.73-229.28 (A) ; 216.13-228.28 (B). stop INDICATIF 194.18 (-11.12 % sous le bas ; sous le support 200.78-206.79 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (2.97 ATR sous le plus haut 20 s., RSI(2) 68.3 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 255.71-260.27 (A, -3.83 %) ; 247.2-250.55 (A, -7.43 %) ; 240.14-246.18 (A, -9.04 %) ; 232.79-236.2 (A, -12.73 %) ; 224.73-229.28 (A, -15.29 %) ; 216.13-228.28 (B, -15.66 %)
- Resistances reelles au-dessus : 275.99-282.34 (A, 1.97 %) ; 284.07-286.56 (A, 4.96 %) ; 291.53-294.09 (A, 7.71 %) ; 299.33-305.8 (A, 10.6 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.01 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (17.86 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1193).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 17.86 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.861 % | p01 -4.432 % | pire -15.824 % _(sur 1193 séances)_
- **P(stop avant cible)** _(source : daily, 1194 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0086** [0.0014 ; 0.0317] _(largeur 3.0 pt, n_eff 173.1)_
   - swing : **0.2827** [0.2372 ; 0.3318] _(largeur 9.5 pt, n_eff 345.5)_
   - deep : **0.2392** [0.1965 ; 0.2862] _(largeur 9.0 pt, n_eff 345.5)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-4.32 %** | CVaR **-6.27 %** | vol 2.86 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 4.83 % contre 2.89 % aujourd'hui, rapport 1.67)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.14 % vs -9.68 % si l'on extrapolait par √5 _(rapport 1.047 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1742** (β de hausse 1.1892, asymétrie 0.9874) vs SPY — 551 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 254.5391 sur atr_grid (1.0 ATR, 5.953 %) — p(stop avant cible) 0.4962 [0.44 ; 0.55], R/R 6.16, perte reelle 6.138 % (gap inclus), CVaR 7.787 %, EV -0.0182 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0917 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 6.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : CVaR 95 % 7.79 % > budget 7.00 %
- Budget de queue : **7.0 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.376 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 19.2 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 8.929 %) — p(stop avant cible) 0.3255 [0.28 ; 0.38], R/R 4.179, perte reelle 9.047 % (gap inclus), EV -0.0753 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 4.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 9.69 % > budget 7.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.08 %) : P(cible) 0.3 % x 37.81 % + P(rien) 67.1 % x 4.10 % ne couvrent pas P(stop) 32.6 % x 9.05 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ swing_based a 1.66 ATR (stop 12.724 %) — p(stop avant cible) 0.1825 [0.14 ; 0.23], R/R 2.949, perte reelle 12.82 % (gap inclus), EV -0.1015 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.08 % > budget 7.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 0.3 % x 37.81 % + P(rien) 81.4 % x 2.60 % ne couvrent pas P(stop) 18.2 % x 12.82 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 1.488 %) — p(stop avant cible) 0.8687 [0.83 ; 0.90], R/R 23.833, perte reelle 1.586 % (gap inclus), EV -0.1729 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 23.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.869, borne haute 0.901 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 0.2 % x 37.81 % + P(rien) 12.9 % x 8.76 % ne couvrent pas P(stop) 86.9 % x 1.59 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 2.976 %) — p(stop avant cible) 0.721 [0.67 ; 0.77], R/R 12.015, perte reelle 3.147 % (gap inclus), EV -0.0644 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 12.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.721, borne haute 0.766 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.06 %) : P(cible) 0.3 % x 37.81 % + P(rien) 27.6 % x 7.60 % ne couvrent pas P(stop) 72.1 % x 3.15 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 4.464 %) — p(stop avant cible) 0.6275 [0.58 ; 0.68], R/R 8.176, perte reelle 4.625 % (gap inclus), EV -0.3971 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 8.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.627, borne haute 0.677 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.40 %) : P(cible) 0.3 % x 37.81 % + P(rien) 36.9 % x 6.46 % ne couvrent pas P(stop) 62.7 % x 4.62 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 5.953 %) — p(stop avant cible) 0.4962 [0.44 ; 0.55], R/R 6.16, perte reelle 6.138 % (gap inclus), EV -0.0182 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 6.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 7.79 % > budget 7.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.02 %) : P(cible) 0.3 % x 37.81 % + P(rien) 50.1 % x 5.81 % ne couvrent pas P(stop) 49.6 % x 6.14 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 7.441 %) — p(stop avant cible) 0.3823 [0.33 ; 0.43], R/R 4.958, perte reelle 7.627 % (gap inclus), EV 0.1016 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 4.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 8.86 % > budget 7.00 %
   - ⚪ grid_snapped a 1.66 ATR (stop 11.641 %) — p(stop avant cible) 0.2123 [0.17 ; 0.26], R/R 3.216, perte reelle 11.756 % (gap inclus), EV -0.0682 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.13 % > budget 7.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.07 %) : P(cible) 0.3 % x 37.81 % + P(rien) 78.5 % x 2.94 % ne couvrent pas P(stop) 21.2 % x 11.76 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 14.882 %) — p(stop avant cible) 0.1129 [0.08 ; 0.15], R/R 2.535, perte reelle 14.914 % (gap inclus), EV -0.0012 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.95 % > budget 7.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.00 %) : P(cible) 0.3 % x 37.81 % + P(rien) 88.4 % x 1.77 % ne couvrent pas P(stop) 11.3 % x 14.91 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 16.37 %) — p(stop avant cible) 0.0626 [0.04 ; 0.09], R/R 2.304, perte reelle 16.414 % (gap inclus), EV 0.1047 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.43 % > budget 7.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 17.858 %) — p(stop avant cible) 0.0428 [0.03 ; 0.07], R/R 2.094, perte reelle 18.057 % (gap inclus), EV 0.1129 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.78 % > budget 7.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 20.834 %) — p(stop avant cible) 0.0118 [0.00 ; 0.03], R/R 1.811, perte reelle 20.882 % (gap inclus), EV 0.2459 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.26 % > budget 7.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 23.811 %) — p(stop avant cible) 0.0074 [0.00 ; 0.02], R/R 1.586, perte reelle 23.844 % (gap inclus), EV 0.2568 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.33 % > budget 7.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 26.787 %) — p(stop avant cible) 0.0057 [0.00 ; 0.02], R/R 1.405, perte reelle 26.908 % (gap inclus), EV 0.2629 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.45 % > budget 7.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 29.763 %) — p(stop avant cible) 0.0022 [0.00 ; 0.01], R/R 1.27, perte reelle 29.763 % (gap inclus), EV 0.2706 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.29 % > budget 7.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 32.74 %) — p(stop avant cible) 0.0005 [0.00 ; 0.01], R/R 1.155, perte reelle 32.74 % (gap inclus), EV 0.2747 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.25 % > budget 7.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 35.716 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.059, perte reelle 35.716 % (gap inclus), EV 0.273 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.25 % > budget 7.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 38.692 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.977, perte reelle 38.692 % (gap inclus), EV 0.273 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.25 % > budget 7.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 41.669 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.907, perte reelle 41.669 % (gap inclus), EV 0.273 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.25 % > budget 7.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 44.645 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.847, perte reelle 44.645 % (gap inclus), EV 0.273 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.25 % > budget 7.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 47.621 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.794, perte reelle 47.621 % (gap inclus), EV 0.273 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.25 % > budget 7.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 270.65, ATR14 16.1109 (5.953 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.389 ATR = 2.316 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.298 % | 269.8445 | 91.64 % | 94.64 % | 95.6 % | 96.66 % | 97.62 % | 98.03 % |
| 0.1 ATR | 0.595 % | 269.0389 | 85.53 % | 90.45 % | 92.48 % | 94.08 % | 95.67 % | 96.83 % |
| 0.15 ATR | 0.893 % | 268.2334 | 79.1 % | 86.27 % | 88.51 % | 90.64 % | 93.83 % | 95.51 % |
| 0.2 ATR | 1.191 % | 267.4278 | 72.03 % | 80.9 % | 84.1 % | 86.76 % | 91.34 % | 94.2 % |
| 0.25 ATR | 1.488 % | 266.6223 | 65.27 % | 75.43 % | 79.38 % | 83.1 % | 88.64 % | 92.23 % |
| 0.35 ATR | 2.083 % | 265.0112 | 53.91 % | 66.09 % | 71.64 % | 76.86 % | 84.2 % | 88.73 % |
| 0.5 ATR | 2.976 % | 262.5946 | 38.8 % | 53.0 % | 59.72 % | 66.52 % | 77.06 % | 83.04 % |
| 0.75 ATR | 4.464 % | 258.5669 | 20.36 % | 36.8 % | 45.44 % | 53.61 % | 66.77 % | 76.15 % |
| 1.0 ATR | 5.953 % | 254.5391 | 11.25 % | 24.14 % | 33.4 % | 43.6 % | 57.79 % | 69.8 % |
| 1.25 ATR | 7.441 % | 250.5114 | 5.79 % | 16.09 % | 24.38 % | 35.84 % | 51.52 % | 63.68 % |
| 1.5 ATR | 8.929 % | 246.4837 | 2.79 % | 10.73 % | 17.4 % | 29.06 % | 44.48 % | 57.66 % |
| 2.0 ATR | 11.905 % | 238.4283 | 0.86 % | 4.29 % | 9.13 % | 17.87 % | 31.28 % | 46.28 % |
| 2.5 ATR | 14.882 % | 230.3728 | 0.43 % | 2.25 % | 4.73 % | 10.87 % | 21.0 % | 36.43 % |
| 3.0 ATR | 17.858 % | 222.3174 | 0.0 % | 1.07 % | 2.79 % | 6.89 % | 15.48 % | 28.56 % |
| 4.0 ATR | 23.811 % | 206.2066 | 0.0 % | 0.21 % | 0.86 % | 2.69 % | 7.03 % | 14.22 % |
| 6.0 ATR | 35.716 % | 173.9848 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.76 % | 2.74 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.39 ATR | 0.44 ATR | 0.58 ATR | 0.69 ATR | 0.76 ATR | 1.06 ATR | 1.32 ATR |
| **2 s.** | 0.26 ATR | 0.55 ATR | 0.62 ATR | 0.82 ATR | 0.98 ATR | 1.13 ATR | 1.56 ATR | 1.95 ATR |
| **3 s.** | 0.31 ATR | 0.67 ATR | 0.76 ATR | 1.01 ATR | 1.23 ATR | 1.41 ATR | 1.95 ATR | 2.47 ATR |
| **5 s.** | 0.38 ATR | 0.84 ATR | 0.96 ATR | 1.35 ATR | 1.68 ATR | 1.91 ATR | 2.61 ATR | 3.45 ATR |
| **10 s.** | 0.55 ATR | 1.30 ATR | 1.48 ATR | 1.94 ATR | 2.31 ATR | 2.59 ATR | 3.65 ATR | 4.65 ATR |
| **20 s.** | 0.80 ATR | 1.84 ATR | 2.06 ATR | 2.72 ATR | 3.25 ATR | 3.60 ATR | 4.74 ATR | 5.61 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.438–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.976 %, prix 262.5955), p(touche) 38.8 % (en stress 81.91 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.623–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.464 %, prix 258.5682), p(touche) 36.8 % (en stress 88.3 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.759–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.953 %, prix 254.5382), p(touche) 33.4 % (en stress 95.74 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.965–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.953 %, prix 254.5382), p(touche) 43.6 % (en stress 96.77 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 51.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.482–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.929 %, prix 246.4837), p(touche) 44.48 % (en stress 98.92 %)  ✅ optimum identifie (72.0 % des re-echantillons)
- **20 seance(s)** : plage utile 2.065–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (14.882 %, prix 230.3719), p(touche) 36.43 % (en stress 95.65 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (87.2 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.033 | EV/share : $-0.664 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 15 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.2 | bear 73.4 | side 21.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=4, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→61% · +2.0%→33% · +3.0%→18% · +5.0%→4% · +8.0%→0%
- Range intraday médian 3.35% (p90 5.52%) · excursion haute méd. +1.42% / basse méd. −1.56%
- Profil de vol intra : ouverture 2.454% vs midi 0.669% vs clôture 0.758% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑1%/↓0% ; spike-down 51% · recovery-V 15%)_
- **Régime intraday** : **chop** _(efficiency 0.116 ; neutre — autocorr 0.022)_ ; drift intra méd. -0.452% ; recovery-V 16%
- **σ réalisé intraday** 2.399% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 40% / bas 68% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 254.8755 (VA 253.3035–256.4475 ; dernier close 257.55)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 37% · rebond 57% · **stop −2.7%** sous le fill (sous le bruit) · cible +1.1% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.47% · baisse 38% (gap-down >1% 10% · >2% 3%)
- Excursion ouverture 5min (n=160) : bas méd −0.61% (p90 −1.58%) · haut méd +0.77% · range méd 1.41%
- Excursion ouverture 15min (n=160) : bas méd −0.79% (p90 −2.27%) · haut méd +0.93% · range méd 1.85%
- Excursion ouverture 30min (n=160) : bas méd −0.95% (p90 −2.61%) · haut méd +1.01% · range méd 2.12%
- Excursion ouverture 60min (n=160) : bas méd −1.14% (p90 −3.48%) · haut méd +1.13% · range méd 2.52%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 257.49 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 51% · séance 66% (103/159) · gap 26% · délai 1.3min · rebond 43% (50/103) (MFE +0.8%)
   - −1.0% : fill 30min 38% · séance 53% (87/159) · gap 10% · délai 2.5min · rebond 43% (40/87) (MFE +0.95%)
   - −1.5% : fill 30min 32% · séance 45% (72/159) · gap 6% · délai 10.5min · rebond 52% (36/72) (MFE +1.02%)
   - −2.0% : fill 30min 25% · séance 37% (59/159) · gap 3% · délai 21.2min · rebond 57% (33/59) (MFE +1.1%)
   - −3.0% : fill 30min 9% · séance 18% (32/159) · gap 2% · délai 31.6min · rebond 45% (14/32) (MFE +0.78%)
   - −4.0% : fill 30min 6% · séance 9% (18/159) · gap 1% · délai 9.3min · rebond 42% (10/18) (MFE +0.76%)
   - −5.0% : fill 30min 4% · séance 6% (11/159) · gap 0% · délai 17.8min · rebond 70% (8/11) (MFE +1.46%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.25% (p90 −1.1%) → stop au-delà de −0.8% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.32% (p90 −1.17%) → stop au-delà de −0.91% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.56% (p90 −2.23%) → stop au-delà de −1.08% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=464 jambes) : jambe baissière méd −1.08% (p90 −2.55%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (43 séances) :
      · −1.0% : fill 91% (40/43) · rebond 45% (21/40)
      · −2.0% : fill 80% (33/43) · rebond 57% (18/33)
      · −3.0% : fill 36% (18/43) · rebond 29% (6/18)
      · −4.0% : fill 28% (14/43) · rebond 39% (7/14)
      · −5.0% : fill 20% (10/43) · rebond 69% (7/10)
   - **flat** (27 séances) :
      · −1.0% : fill 47% (18/27) · rebond 11% (4/18)
      · −2.0% : fill 30% (11/27) · rebond 47% (6/11)
      · −3.0% : fill 13% (6/27) · rebond 24% (2/6)
      · −4.0% : fill 5% (3/27) · rebond 43% (2/3)
      · −5.0% : fill 1% (1/27) · rebond 100% (1/1)
   - **gap-up** (89 séances) :
      · −1.0% : fill 34% (29/89) · rebond 52% (15/29)
      · −2.0% : fill 16% (15/89) · rebond 61% (9/15)
      · −3.0% : fill 9% (8/89) · rebond 88% (6/8)
      · −4.0% : fill 1% (1/89) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/89) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 59% si les 15 1res min sont vertes (86 cas) · 30% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:31** → P(séance verte=clôture>ouverture) 85% si début vert vs 8% si rouge (base 44% · écart 77 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=83) : tient le vert **85%** · continue >prix actuel 57% ; creux résiduel méd -0.88% (q20 -1.57%) → **SL/trailing à −1.57%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.8% / q75 +1.26% → **scale +0.8% / runner +1.26%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **8%** (continue à baisser 66%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.22%** (au-delà de la MAE q10 -2.22%), cible rebond +0.94% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.58% .. +2.04%] · haut q95 +3.04% · bas q05 -4.75%
   - 60min (n=160) : retour [-3.48% .. +2.54%] · haut q95 +3.33% · bas q05 -4.99%
   - 2h (n=160) : retour [-3.71% .. +2.98%] · haut q95 +3.95% · bas q05 -5.37%
   - 4h (n=160) : retour [-3.72% .. +3.29%] · haut q95 +4.1% · bas q05 -5.37%
   - 6h (n=160) : retour [-3.86% .. +3.44%] · haut q95 +4.48% · bas q05 -5.37%
   - session (n=160) : retour [-3.61% .. +3.56%] · haut q95 +4.53% · bas q05 -5.47%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 4.4% / strong 2.5%) · base = 11 séances trend-up (n_eff 7.7)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **41%**. Lecture précoce 30 min : signature présente → 16% vs absente 4% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.07% (p75 1.89% / p90 2.36%) · ~1.0 replis/séance, durée méd 144.56 min. P(nouveau plus-haut après repli) :
   - −0.5% → **69%** (reprise méd 24.3 min, n=22)
   - −1.0% → **69%** (reprise méd 179.47 min, n=11)
   - −1.5% → **48%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.36%** (p90, défaut prudent ; serré/agressif −1.89%) ; extension open→close méd +3.62% (q75 +4.82% / q95 +6.2%), MFE méd +4.65% / q90 +5.84%
   - Échelle scale-out : +4.65% (33%) / +5.3% (33%) / +5.84% (34%)
- **DÉSARMER** : repli > **−2.36%** depuis le plus-haut = décay → P(retournement) **100%** (préavis méd 280.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.84% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 96% du temps (retour médian dernière heure +0.48%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.47 · part idiosyncratique 0.53
**Short/Insider** : SI —% | insider — | verdict buy_bias_strong
**Options** : bearish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 54.6  _(neutre)_
- **ADX** : 17.4  _(pas de tendance nette)_
- **MACD** : hist -2.019  _(bearish_recent)_
- **BB** : %B 0.45 · largeur 23.2%
- **ATR** : 16.11 (86.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.02  _(neutre)_
- **Vol ratio** : 0.59  _(volume atone)_
- **Choppiness** : 49.7  _(transition)_
- **MA** : MA20 273.97 · MA50 275.13 · MA200 282.17  _(prix < MA20)_
- **Dist MA** : MA20 -1.2% · MA50 -1.6% · MA200 -4.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (769561 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
