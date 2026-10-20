# PRY

**Generated** : 2026-10-20T21:50:30.831342+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €104.30  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 20/125 fenêtres (p_fill pondéré 16 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot €104.30 (+4.4% vs entrée) · entrée €99.88 · stop €98.30 · T1 €102.52 · R/R 1.67  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.59% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -302 % hors [0,100] (R² max 0.84). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-20 : 104.3 · ATR Wilder 5.13 (4.92 %)_
- **Swing** : plage **98.7 → 95.2** (-5.37 % a -8.73 % sous la cloture, 0.68 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 94.5-96.88 (A). stop INDICATIF 89.25 (-6.25 % sous le bas ; sous le support 91.82-92.37 (- 0,5 ATR)).
- **Deep** : plage **95.2 → 85.56** (-8.73 % a -17.97 % sous la cloture, 1.88 ATR) — touchee 39 % → 15 % du temps en 20 seances ; supports reels dans la plage : 94.5-96.88 (A) ; 91.82-92.37 (A) ; 89.22-91.78 (A) ; 86.22-86.95 (B). stop INDICATIF 80.59 (-5.8 % sous le bas ; sous le support 83.16-84.97 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 5.24 ATR sous le plus haut 20 s., RSI(2) 0.2. Limite **101.73** (seance suivante), stop catastrophe 81.21, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 98.7-100.75 (B, -3.4 %) ; 94.5-96.88 (A, -7.12 %) ; 91.82-92.37 (A, -11.44 %) ; 89.22-91.78 (A, -12.01 %) ; 86.22-86.95 (B, -16.63 %) ; 83.16-84.97 (A, -18.54 %)
- Resistances reelles au-dessus : 110.3-110.3 (C, 5.75 %) ; 115.85-117.1 (A, 11.07 %) ; 119.65-119.65 (B, 14.72 %) ; 122.29-123.2 (A, 17.25 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.65 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (14.38 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1270).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 14.38 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.87 % | p01 -3.601 % | pire -9.998 % _(sur 1270 séances)_
- **P(stop avant cible)** _(source : daily, 1271 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4578** [0.3848 ; 0.5322] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.325** [0.2773 ; 0.3757] _(largeur 9.8 pt, n_eff 345.8)_
   - deep : **0.2354** [0.193 ; 0.2822] _(largeur 8.9 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (42.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-4.11 %** | CVaR **-5.64 %** | vol 2.46 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 1.54 % contre 2.70 % aujourd'hui, rapport 0.57)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.64 % vs -7.57 % si l'on extrapolait par √5 _(rapport 0.877 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0261** (β de hausse 1.2323, asymétrie 0.8326) vs FTSEMIB — 567 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.32× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 99.0214 sur atr_grid (1.0 ATR, 5.061 %) — p(stop avant cible) 0.4939 [0.44 ; 0.55], R/R 9.217, perte reelle 5.22 % (gap inclus), CVaR 6.4 %, EV 0.041 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0143 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 9.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : CVaR 95 % 6.40 % > budget 6.31 %
- Budget de queue : **6.31 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.264 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 36.1 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 7.591 %) — p(stop avant cible) 0.278 [0.23 ; 0.33], R/R 6.232, perte reelle 7.72 % (gap inclus), EV 0.678 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 8.31 % > budget 6.31 %
   - ⚪ sr_based a 3.45 ATR (stop 20.222 %) — p(stop avant cible) 0.0198 [0.01 ; 0.04], R/R 2.323, perte reelle 20.713 % (gap inclus), EV 1.0348 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.50 % > budget 6.31 %
   - 🟢 support a 4.87 ATR (stop 27.428 %) — p(stop avant cible) 0.0025 [0.00 ; 0.01], R/R 1.604, perte reelle 29.993 % (gap inclus), EV 1.0841 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.56 % > budget 6.31 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.265 %) — p(stop avant cible) 0.8545 [0.81 ; 0.89], R/R 34.862, perte reelle 1.38 % (gap inclus), EV -0.0089 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 34.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.855, borne haute 0.889 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.01 %) : P(cible) 0.0 % x 48.11 % + P(rien) 14.5 % x 8.04 % ne couvrent pas P(stop) 85.5 % x 1.38 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+48.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.5 ATR (stop 2.53 %) — p(stop avant cible) 0.7297 [0.68 ; 0.77], R/R 17.937, perte reelle 2.682 % (gap inclus), EV -0.0791 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 17.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.730, borne haute 0.774 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.08 %) : P(cible) 0.0 % x 48.11 % + P(rien) 27.0 % x 6.95 % ne couvrent pas P(stop) 73.0 % x 2.68 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+48.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.75 ATR (stop 3.796 %) — p(stop avant cible) 0.6081 [0.56 ; 0.66], R/R 12.197, perte reelle 3.944 % (gap inclus), EV -0.028 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 12.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.608, borne haute 0.658 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 0.0 % x 48.11 % + P(rien) 39.2 % x 6.05 % ne couvrent pas P(stop) 60.8 % x 3.94 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+48.1 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.0 ATR (stop 5.061 %) — p(stop avant cible) 0.4939 [0.44 ; 0.55], R/R 9.217, perte reelle 5.22 % (gap inclus), EV 0.041 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 9.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 6.40 % > budget 6.31 %
   - ⚪ atr_grid a 1.25 ATR (stop 6.326 %) — p(stop avant cible) 0.3795 [0.33 ; 0.43], R/R 7.436, perte reelle 6.47 % (gap inclus), EV 0.4317 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 7.37 % > budget 6.31 %
   - ⚪ atr_grid a 1.75 ATR (stop 8.857 %) — p(stop avant cible) 0.2354 [0.19 ; 0.28], R/R 5.381, perte reelle 8.941 % (gap inclus), EV 0.6871 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 9.25 % > budget 6.31 %
   - ⚪ atr_grid a 2.0 ATR (stop 10.122 %) — p(stop avant cible) 0.1698 [0.13 ; 0.21], R/R 4.73, perte reelle 10.171 % (gap inclus), EV 0.8292 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 10.29 % > budget 6.31 %
   - ⚪ atr_grid a 2.25 ATR (stop 11.387 %) — p(stop avant cible) 0.1164 [0.09 ; 0.15], R/R 4.048, perte reelle 11.885 % (gap inclus), EV 0.876 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.55 % > budget 6.31 %
   - ⚪ atr_grid a 2.5 ATR (stop 12.652 %) — p(stop avant cible) 0.0848 [0.06 ; 0.12], R/R 3.513, perte reelle 13.695 % (gap inclus), EV 0.8959 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.42 % > budget 6.31 %
   - ⚪ atr_grid a 2.75 ATR (stop 13.918 %) — p(stop avant cible) 0.0573 [0.04 ; 0.09], R/R 3.064, perte reelle 15.699 % (gap inclus), EV 0.9578 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 15.96 % > budget 6.31 %
   - ⚪ atr_grid a 3.0 ATR (stop 15.183 %) — p(stop avant cible) 0.0397 [0.02 ; 0.06], R/R 2.778, perte reelle 17.32 % (gap inclus), EV 1.0315 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.35 % > budget 6.31 %
   - ⚪ grid_snapped a 3.45 ATR (stop 18.977 %) — p(stop avant cible) 0.0271 [0.01 ; 0.05], R/R 2.426, perte reelle 19.829 % (gap inclus), EV 1.0119 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.97 % > budget 6.31 %
   - ⚪ atr_grid a 4.5 ATR (stop 22.774 %) — p(stop avant cible) 0.006 [0.00 ; 0.02], R/R 2.012, perte reelle 23.916 % (gap inclus), EV 1.0767 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.72 % > budget 6.31 %
   - 🟢 grid_snapped a 4.87 ATR (stop 26.183 %) — p(stop avant cible) 0.0031 [0.00 ; 0.01], R/R 1.812, perte reelle 26.552 % (gap inclus), EV 1.0911 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.43 % > budget 6.31 %
   - ⚪ atr_grid a 6.0 ATR (stop 30.366 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 1.487, perte reelle 32.353 % (gap inclus), EV 1.0929 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.43 % > budget 6.31 %
   - ⚪ atr_grid a 6.5 ATR (stop 32.896 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 1.462, perte reelle 32.896 % (gap inclus), EV 1.0952 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.37 % > budget 6.31 %
   - ⚪ atr_grid a 7.0 ATR (stop 35.427 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.358, perte reelle 35.427 % (gap inclus), EV 1.0974 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.32 % > budget 6.31 %
   - ⚪ atr_grid a 7.5 ATR (stop 37.957 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.267, perte reelle 37.957 % (gap inclus), EV 1.0974 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.32 % > budget 6.31 %
   - ⚪ atr_grid a 8.0 ATR (stop 40.488 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.188, perte reelle 40.488 % (gap inclus), EV 1.0974 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.32 % > budget 6.31 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 104.3, ATR14 5.2786 (5.061 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.346 ATR = 1.751 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.253 % | 104.0361 | 91.88 % | 94.05 % | 94.74 % | 95.53 % | 97.2 % | 97.78 % |
| 0.1 ATR | 0.506 % | 103.7721 | 85.25 % | 89.0 % | 91.17 % | 92.94 % | 95.1 % | 96.17 % |
| 0.15 ATR | 0.759 % | 103.5082 | 77.92 % | 84.44 % | 87.5 % | 90.46 % | 92.91 % | 94.15 % |
| 0.2 ATR | 1.012 % | 103.2443 | 69.9 % | 79.19 % | 82.64 % | 86.98 % | 90.71 % | 92.23 % |
| 0.25 ATR | 1.265 % | 102.9804 | 62.28 % | 74.33 % | 78.57 % | 83.3 % | 88.11 % | 90.21 % |
| 0.35 ATR | 1.771 % | 102.4525 | 49.5 % | 63.92 % | 70.83 % | 76.74 % | 83.72 % | 87.39 % |
| 0.5 ATR | 2.53 % | 101.6607 | 35.15 % | 52.13 % | 60.02 % | 67.89 % | 76.52 % | 81.84 % |
| 0.75 ATR | 3.796 % | 100.3411 | 19.5 % | 34.79 % | 43.55 % | 54.67 % | 64.94 % | 73.46 % |
| 1.0 ATR | 5.061 % | 99.0214 | 10.0 % | 23.49 % | 31.85 % | 44.63 % | 55.74 % | 65.39 % |
| 1.25 ATR | 6.326 % | 97.7018 | 5.64 % | 16.15 % | 24.21 % | 34.89 % | 47.35 % | 57.82 % |
| 1.5 ATR | 7.591 % | 96.3821 | 2.57 % | 9.81 % | 16.47 % | 24.85 % | 36.96 % | 49.45 % |
| 2.0 ATR | 10.122 % | 93.7429 | 0.4 % | 4.06 % | 7.84 % | 14.41 % | 24.68 % | 37.74 % |
| 2.5 ATR | 12.652 % | 91.1036 | 0.0 % | 1.68 % | 3.57 % | 8.25 % | 15.98 % | 27.04 % |
| 3.0 ATR | 15.183 % | 88.4643 | 0.0 % | 0.89 % | 1.88 % | 4.47 % | 10.09 % | 19.27 % |
| 4.0 ATR | 20.244 % | 83.1857 | 0.0 % | 0.2 % | 0.69 % | 1.99 % | 5.09 % | 11.4 % |
| 6.0 ATR | 30.366 % | 72.6286 | 0.0 % | 0.0 % | 0.0 % | 0.4 % | 2.0 % | 3.63 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.66 ATR | 0.74 ATR | 1.00 ATR | 1.30 ATR |
| **2 s.** | 0.24 ATR | 0.53 ATR | 0.60 ATR | 0.79 ATR | 0.97 ATR | 1.12 ATR | 1.49 ATR | 1.92 ATR |
| **3 s.** | 0.30 ATR | 0.65 ATR | 0.73 ATR | 0.97 ATR | 1.22 ATR | 1.39 ATR | 1.88 ATR | 2.33 ATR |
| **5 s.** | 0.38 ATR | 0.87 ATR | 0.99 ATR | 1.30 ATR | 1.50 ATR | 1.73 ATR | 2.36 ATR | 2.93 ATR |
| **10 s.** | 0.53 ATR | 1.17 ATR | 1.31 ATR | 1.66 ATR | 1.99 ATR | 2.27 ATR | 3.02 ATR | 4.06 ATR |
| **20 s.** | 0.70 ATR | 1.48 ATR | 1.69 ATR | 2.22 ATR | 2.63 ATR | 2.95 ATR | 4.36 ATR | 5.65 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.397–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.603–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.796 %, prix 100.3408), p(touche) 34.79 % (en stress 89.11 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.728–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.796 %, prix 100.3408), p(touche) 43.55 % (en stress 95.05 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.991–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.061 %, prix 99.0214), p(touche) 44.63 % (en stress 99.01 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.307–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.591 %, prix 96.3826), p(touche) 36.96 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.69–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (10.122 %, prix 93.7428), p(touche) 37.74 % (en stress 99.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 56.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.042 | EV/share : €-0.066 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 27 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.0 | bear 31.5 | side 61.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈60.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.242% → cible +2.642% / stop −1.586%, p_fill 16%, n_eff≈18.7) : P(cible|rempli) **4%** · **EV/risk -0.025** (×p_fill ; si rempli -0.26% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→64% · +2.0%→40% · +3.0%→25% · +5.0%→6% · +8.0%→2%
- Range intraday médian 3.71% (p90 6.32%) · excursion haute méd. +1.5% / basse méd. −1.61%
- Profil de vol intra : ouverture 2.21% vs midi 0.779% vs clôture 1.066% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 53% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.12 ; neutre — autocorr 0.003)_ ; drift intra méd. -0.354% ; recovery-V 21%
- **σ réalisé intraday** 2.479% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 65% / whipsaw 36%
- POC intraday (dernière séance, temps-au-prix) : 129.9327 (VA 129.5263–130.8813 ; dernier close 130.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 23% · rebond 60% · **stop −2.81%** sous le fill (sous le bruit) · cible +1.15% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.51% · baisse 35% (gap-down >1% 13% · >2% 3%)
- Excursion ouverture 5min (n=160) : bas méd −0.71% (p90 −2.05%) · haut méd +0.51% · range méd 1.3%
- Excursion ouverture 15min (n=160) : bas méd −0.93% (p90 −2.32%) · haut méd +0.61% · range méd 1.71%
- Excursion ouverture 30min (n=160) : bas méd −0.95% (p90 −2.41%) · haut méd +0.74% · range méd 1.88%
- Excursion ouverture 60min (n=160) : bas méd −1.05% (p90 −2.93%) · haut méd +0.83% · range méd 2.13%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 129.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 46% · séance 65% (109/159) · gap 19% · délai 0.4min · rebond 54% (61/109) (MFE +1.1%)
   - −1.0% : fill 30min 39% · séance 54% (90/159) · gap 13% · délai 1.3min · rebond 60% (54/90) (MFE +1.25%)
   - −1.5% : fill 30min 24% · séance 45% (72/159) · gap 7% · délai 21.4min · rebond 51% (39/72) (MFE +1.06%)
   - −2.0% : fill 30min 18% · séance 37% (60/159) · gap 3% · délai 42.5min · rebond 51% (34/60) (MFE +1.01%)
   - −3.0% : fill 30min 6% · séance 23% (40/159) · gap 1% · délai 93.7min · rebond 60% (26/40) (MFE +1.15%)
   - −4.0% : fill 30min 2% · séance 14% (25/159) · gap 0% · délai 282.0min · rebond 57% (15/25) (MFE +1.06%)
   - −5.0% : fill 30min 2% · séance 9% (16/159) · gap 0% · délai 394.7min · rebond 66% (11/16) (MFE +1.06%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.46% (p90 −1.89%) → stop au-delà de −1.42% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.31% (p90 −1.63%) → stop au-delà de −1.12% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.02% (p90 −1.76%) → stop au-delà de −1.27% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=487 jambes) : jambe baissière méd −1.06% (p90 −2.48%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (43 séances) :
      · −1.0% : fill 94% (39/43) · rebond 49% (19/39)
      · −2.0% : fill 77% (31/43) · rebond 58% (18/31)
      · −3.0% : fill 47% (23/43) · rebond 50% (14/23)
      · −4.0% : fill 30% (15/43) · rebond 57% (9/15)
      · −5.0% : fill 26% (12/43) · rebond 57% (8/12)
   - **flat** (27 séances) :
      · −1.0% : fill 48% (15/27) · rebond 74% (11/15)
      · −2.0% : fill 27% (8/27) · rebond 76% (7/8)
      · −3.0% : fill 16% (5/27) · rebond 41% (3/5)
      · −4.0% : fill 6% (2/27) · rebond 69% (1/2)
      · −5.0% : fill 2% (1/27) · rebond 0% (0/1)
   - **gap-up** (89 séances) :
      · −1.0% : fill 38% (36/89) · rebond 65% (24/36)
      · −2.0% : fill 23% (21/89) · rebond 30% (9/21)
      · −3.0% : fill 14% (12/89) · rebond 80% (9/12)
      · −4.0% : fill 9% (8/89) · rebond 54% (5/8)
      · −5.0% : fill 4% (3/89) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 63% si les 15 1res min sont vertes (77 cas) · 28% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:23** → P(séance verte=clôture>ouverture) 82% si début vert vs 21% si rouge (base 46% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 298min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=69) : tient le vert **82%** · continue >prix actuel 45% ; creux résiduel méd -1.18% (q20 -1.89%) → **SL/trailing à −1.89%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.07% / q75 +2.01% → **scale +1.07% / runner +2.01%**, sortie à la clôture
  - **si ROUGE au coude** (n=91) : edge inversé — récupère vert seulement **21%** (continue à baisser 66%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.77%** (au-delà de la MAE q10 -3.77%), cible rebond +1.33% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.93% .. +2.17%] · haut q95 +3.13% · bas q05 -3.36%
   - 60min (n=160) : retour [-3.28% .. +2.31%] · haut q95 +3.46% · bas q05 -3.58%
   - 2h (n=160) : retour [-3.32% .. +2.69%] · haut q95 +3.52% · bas q05 -4.05%
   - 4h (n=160) : retour [-3.46% .. +3.2%] · haut q95 +4.0% · bas q05 -4.46%
   - 6h (n=160) : retour [-3.73% .. +3.5%] · haut q95 +4.42% · bas q05 -4.65%
   - session (n=160) : retour [-4.58% .. +3.44%] · haut q95 +4.53% · bas q05 -6.29%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.44%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.74 · part idiosyncratique 0.26
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 23.9  _(survente)_
- **ADX** : 22.9  _(pas de tendance nette)_
- **MACD** : hist -2.234  _(pas de croisement recent)_
- **BB** : %B -0.03 · largeur 25.4%
- **ATR** : 5.28 (68.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.147  _(distribution)_
- **Vol ratio** : 1.3  _(volume normal)_
- **Choppiness** : 35.3  _(marche directionnel)_
- **MA** : MA20 120.61 · MA50 122.45 · MA200 121.0  _(prix < MA20)_
- **Dist MA** : MA20 -13.5% · MA50 -14.8% · MA200 -13.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (757885 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
