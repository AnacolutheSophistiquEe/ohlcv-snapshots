# PRY

**Generated** : 2026-11-11T01:12:37.189741+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €106.90  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-0 sess · macro taux)  
> ↳ spot €106.90 (+0.4% vs entrée) · entrée €106.50 · stop €97.98 · T1 €109.56 · R/R 0.36  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-10 : 106.9 · ATR Wilder 5.77 (5.4 %)_
- **Swing** : plage **100.53 → 96.56** (-5.96 % a -9.67 % sous la cloture, 0.69 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 96.88-98.8 (A). stop INDICATIF 89.49 (-7.33 % sous le bas ; sous le support 92.37-95.09 (- 0,5 ATR)).
- **Deep** : plage **96.56 → 83.76** (-9.67 % a -21.65 % sous la cloture, 2.22 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 92.37-95.09 (A) ; 89.22-92.05 (A) ; 86.22-86.95 (B) ; 83.16-84.97 (A). stop INDICATIF 76.54 (-8.62 % sous le bas ; sous le support 79.43-81.87 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (2.61 ATR sous le plus haut 20 s., RSI(2) 74.1 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 96.88-98.8 (A, -7.57 %) ; 92.37-95.09 (A, -11.05 %) ; 89.22-92.05 (A, -13.89 %) ; 86.22-86.95 (B, -18.66 %) ; 83.16-84.97 (A, -20.52 %) ; 79.43-81.87 (A, -23.41 %)
- Resistances reelles au-dessus : 110.3-110.3 (C, 3.18 %) ; 115.65-117.1 (A, 8.19 %) ; 119.65-122.29 (A, 11.93 %) ; 129.4-131.2 (A, 21.05 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.73 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (6.36 %)** : le gap seul le franchit 0.315 % des séances (4 fois sur 1270).
   - exécution **1.536 pt plus bas** dans le cas TYPIQUE (médiane), 3.223 au p90, **3.638 au pire**
   - perte réelle **8.086 %** en moyenne _(tirée par la queue)_, jusqu'à **9.998 %** — au lieu des 6.36 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0054 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.898 % | p01 -3.733 % | pire -9.998 % _(sur 1270 séances)_
- **P(stop avant cible)** _(source : daily, 1271 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0002** [0.0 ; 0.0149] _(largeur 1.5 pt, n_eff 173.1)_
   - swing : **0.3279** [0.28 ; 0.3787] _(largeur 9.9 pt, n_eff 345.8)_
   - deep : **0.2648** [0.2204 ; 0.3131] _(largeur 9.3 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-4.19 %** | CVaR **-5.84 %** | vol 2.54 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 1.59 % contre 2.85 % aujourd'hui, rapport 0.56)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.73 % vs -7.85 % si l'on extrapolait par √5 _(rapport 0.857 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0422** (β de hausse 1.2075, asymétrie 0.8631) vs FTSEMIB — 566 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.481× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 99.2656 sur atr_grid (1.25 ATR, 7.142 %) — p(stop avant cible) 0.3491 [0.30 ; 0.40], R/R 5.924, perte reelle 7.474 % (gap inclus), CVaR 9.442 %, EV 0.1108 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.14 ATR (stop 3.641 %) — p(stop avant cible) 0.6492 [0.60 ; 0.70], R/R 11.691, perte reelle 3.787 % (gap inclus), EV -0.2681 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 11.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.649, borne haute 0.698 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.27 %) : P(cible) 0.0 % x 44.27 % + P(rien) 35.1 % x 6.24 % ne couvrent pas P(stop) 64.9 % x 3.79 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🔴 support a 0.48 ATR (stop 5.599 %) — p(stop avant cible) 0.4595 [0.41 ; 0.51], R/R 7.726, perte reelle 5.73 % (gap inclus), EV -0.0922 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - ⚠ support DETECTE a 0.04 ATR du spot — compartiment <1, mesure a 48.2 % de casse (IC clusterise [0.451 ; 0.515] sur 1149 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.09 %) : P(cible) 0.0 % x 44.27 % + P(rien) 54.0 % x 4.70 % ne couvrent pas P(stop) 46.0 % x 5.73 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_based a 1.5 ATR (stop 8.57 %) — p(stop avant cible) 0.2648 [0.22 ; 0.31], R/R 4.73, perte reelle 9.36 % (gap inclus), EV 0.1381 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.75 % > budget 12.00 %
   - ⚪ swing_based a 1.75 ATR (stop 12.854 %) — p(stop avant cible) 0.1153 [0.08 ; 0.15], R/R 2.991, perte reelle 14.801 % (gap inclus), EV 0.2918 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.22 % > budget 12.00 %
   - 🟢 support a 4.64 ATR (stop 29.36 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 1.368, perte reelle 32.353 % (gap inclus), EV 0.6092 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.47 % > budget 12.00 %
   - ⚪ grid_snapped a 0.14 ATR (stop 2.492 %) — p(stop avant cible) 0.7516 [0.70 ; 0.79], R/R 16.827, perte reelle 2.631 % (gap inclus), EV -0.2837 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 16.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.752, borne haute 0.795 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.28 %) : P(cible) 0.0 % x 44.27 % + P(rien) 24.8 % x 6.82 % ne couvrent pas P(stop) 75.2 % x 2.63 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🔴 grid_snapped a 0.48 ATR (stop 4.45 %) — p(stop avant cible) 0.5636 [0.51 ; 0.62], R/R 9.632, perte reelle 4.597 % (gap inclus), EV -0.2645 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 9.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.564, borne haute 0.615 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.26 %) : P(cible) 0.0 % x 44.27 % + P(rien) 43.6 % x 5.33 % ne couvrent pas P(stop) 56.4 % x 4.60 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.3 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.25 ATR (stop 7.142 %) — p(stop avant cible) 0.3491 [0.30 ; 0.40], R/R 5.924, perte reelle 7.474 % (gap inclus), EV 0.1108 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ grid_snapped a 1.75 ATR (stop 11.706 %) — p(stop avant cible) 0.1201 [0.09 ; 0.16], R/R 3.424, perte reelle 12.929 % (gap inclus), EV 0.4723 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.64 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 14.283 %) — p(stop avant cible) 0.0849 [0.06 ; 0.12], R/R 2.762, perte reelle 16.027 % (gap inclus), EV 0.4689 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.24 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 15.712 %) — p(stop avant cible) 0.0633 [0.04 ; 0.09], R/R 2.574, perte reelle 17.199 % (gap inclus), EV 0.5403 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.60 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 17.14 %) — p(stop avant cible) 0.0593 [0.04 ; 0.09], R/R 2.44, perte reelle 18.144 % (gap inclus), EV 0.4954 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.33 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 19.996 %) — p(stop avant cible) 0.0289 [0.01 ; 0.05], R/R 2.173, perte reelle 20.379 % (gap inclus), EV 0.5494 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.50 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 22.853 %) — p(stop avant cible) 0.0055 [0.00 ; 0.02], R/R 1.848, perte reelle 23.963 % (gap inclus), EV 0.5941 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.70 % > budget 12.00 %
   - 🟢 grid_snapped a 4.64 ATR (stop 28.211 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 1.43, perte reelle 30.959 % (gap inclus), EV 0.603 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.57 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 31.423 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 1.368, perte reelle 32.353 % (gap inclus), EV 0.6092 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.47 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 34.28 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.292, perte reelle 34.28 % (gap inclus), EV 0.6133 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.36 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 37.136 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.192, perte reelle 37.136 % (gap inclus), EV 0.6133 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.36 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 39.993 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.107, perte reelle 39.993 % (gap inclus), EV 0.6133 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.36 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 42.85 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.033, perte reelle 42.85 % (gap inclus), EV 0.6133 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.36 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 45.706 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.969, perte reelle 45.706 % (gap inclus), EV 0.6133 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.36 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 106.9, ATR14 6.1075 (5.713 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.344 ATR = 1.965 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.286 % | 106.5946 | 91.78 % | 94.05 % | 94.74 % | 95.53 % | 97.3 % | 97.88 % |
| 0.1 ATR | 0.571 % | 106.2893 | 85.05 % | 88.9 % | 91.07 % | 92.84 % | 95.2 % | 96.27 % |
| 0.15 ATR | 0.857 % | 105.9839 | 77.52 % | 84.34 % | 87.4 % | 90.36 % | 93.01 % | 94.25 % |
| 0.2 ATR | 1.143 % | 105.6785 | 69.5 % | 79.09 % | 82.64 % | 86.88 % | 90.81 % | 92.33 % |
| 0.25 ATR | 1.428 % | 105.3731 | 61.88 % | 74.23 % | 78.57 % | 83.2 % | 88.21 % | 90.31 % |
| 0.35 ATR | 2.0 % | 104.7624 | 49.21 % | 64.02 % | 71.03 % | 76.74 % | 83.92 % | 87.69 % |
| 0.5 ATR | 2.857 % | 103.8463 | 35.15 % | 52.33 % | 60.32 % | 67.99 % | 76.92 % | 82.34 % |
| 0.75 ATR | 4.285 % | 102.3194 | 19.6 % | 34.79 % | 43.85 % | 54.87 % | 65.43 % | 74.07 % |
| 1.0 ATR | 5.713 % | 100.7925 | 10.0 % | 23.59 % | 32.24 % | 45.03 % | 56.24 % | 66.2 % |
| 1.25 ATR | 7.142 % | 99.2656 | 5.45 % | 16.25 % | 24.4 % | 35.19 % | 47.75 % | 58.63 % |
| 1.5 ATR | 8.57 % | 97.7388 | 2.38 % | 9.61 % | 16.47 % | 24.95 % | 37.26 % | 50.35 % |
| 2.0 ATR | 11.427 % | 94.685 | 0.4 % | 4.06 % | 7.74 % | 14.71 % | 25.07 % | 38.85 % |
| 2.5 ATR | 14.283 % | 91.6313 | 0.0 % | 1.68 % | 3.57 % | 8.45 % | 16.68 % | 28.56 % |
| 3.0 ATR | 17.14 % | 88.5775 | 0.0 % | 0.89 % | 1.88 % | 4.57 % | 10.69 % | 20.79 % |
| 4.0 ATR | 22.853 % | 82.47 | 0.0 % | 0.2 % | 0.69 % | 2.09 % | 5.69 % | 12.92 % |
| 6.0 ATR | 34.28 % | 70.255 | 0.0 % | 0.0 % | 0.0 % | 0.4 % | 2.0 % | 4.24 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.34 ATR | 0.40 ATR | 0.54 ATR | 0.66 ATR | 0.74 ATR | 1.00 ATR | 1.29 ATR |
| **2 s.** | 0.24 ATR | 0.53 ATR | 0.60 ATR | 0.79 ATR | 0.97 ATR | 1.12 ATR | 1.49 ATR | 1.92 ATR |
| **3 s.** | 0.30 ATR | 0.66 ATR | 0.73 ATR | 0.98 ATR | 1.23 ATR | 1.39 ATR | 1.87 ATR | 2.33 ATR |
| **5 s.** | 0.38 ATR | 0.87 ATR | 1.00 ATR | 1.30 ATR | 1.50 ATR | 1.74 ATR | 2.38 ATR | 2.94 ATR |
| **10 s.** | 0.54 ATR | 1.18 ATR | 1.32 ATR | 1.68 ATR | 2.00 ATR | 2.30 ATR | 3.14 ATR | 4.37 ATR |
| **20 s.** | 0.72 ATR | 1.51 ATR | 1.73 ATR | 2.28 ATR | 2.73 ATR | 3.10 ATR | 4.67 ATR | 5.83 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.395 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.604–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.285 %, prix 102.3193), p(touche) 34.79 % (en stress 88.12 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.733–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.285 %, prix 102.3193), p(touche) 43.85 % (en stress 96.04 %)  ✅ optimum identifie (66.8 % des re-echantillons)
- **5 seance(s)** : plage utile 1.001–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.57 %, prix 97.7387), p(touche) 24.95 % (en stress 91.09 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.316–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.57 %, prix 97.7387), p(touche) 37.26 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.733–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (11.427 %, prix 94.6845), p(touche) 38.85 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 55.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.032 | EV/share : €-0.274 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 25 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 78.7 | bear 14.3 | side 7.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.37% → cible +2.867% / stop −8.0%, p_fill 86%, n_eff≈89.9) : P(cible|rempli) **17%** · **EV/risk -0.093** (×p_fill ; si rempli -0.87% du capital)
  - **swing** (entrée dip −0.647% → cible +6.429% / stop −5.75%, p_fill 83%, n_eff≈96.1) : P(cible|rempli) **17%** · **EV/risk -0.257** (×p_fill ; si rempli -1.78% du capital)
  - **deep** (entrée dip −0.85% → cible +17.247% / stop −8.644%, p_fill 91%, n_eff≈101.3) : P(cible|rempli) **1%** · **EV/risk -0.321** (×p_fill ; si rempli -3.06% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→64% · +2.0%→38% · +3.0%→23% · +5.0%→5% · +8.0%→1%
- Range intraday médian 3.91% (p90 6.39%) · excursion haute méd. +1.39% / basse méd. −1.8%
- Profil de vol intra : ouverture 2.349% vs midi 0.783% vs clôture 1.094% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 14% · trend ↑0%/↓2% ; spike-down 60% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.136 ; neutre — autocorr 0.012)_ ; drift intra méd. -1.197% ; recovery-V 21%
- **σ réalisé intraday** 2.694% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 76% / whipsaw 34%
- POC intraday (dernière séance, temps-au-prix) : 98.2458 (VA 97.8063–98.9783 ; dernier close 98.9)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 29% · rebond 70% · **stop −3.71%** sous le fill (sous le bruit) · cible +1.6% · R/R 0.43 (high win-rate)
- Gaps overnight (n=159) : méd. 0.53% · baisse 36% (gap-down >1% 16% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.7% (p90 −2.11%) · haut méd +0.38% · range méd 1.27%
- Excursion ouverture 15min (n=160) : bas méd −0.98% (p90 −2.84%) · haut méd +0.52% · range méd 1.72%
- Excursion ouverture 30min (n=160) : bas méd −1.06% (p90 −3.39%) · haut méd +0.62% · range méd 1.89%
- Excursion ouverture 60min (n=160) : bas méd −1.19% (p90 −3.66%) · haut méd +0.75% · range méd 2.17%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 99.08 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 49% · séance 70% (113/159) · gap 24% · délai 0.4min · rebond 49% (62/113) (MFE +0.99%)
   - −1.0% : fill 30min 41% · séance 62% (94/159) · gap 16% · délai 2.4min · rebond 52% (54/94) (MFE +1.04%)
   - −1.5% : fill 30min 30% · séance 53% (76/159) · gap 10% · délai 21.2min · rebond 41% (38/76) (MFE +0.77%)
   - −2.0% : fill 30min 23% · séance 44% (63/159) · gap 6% · délai 26.7min · rebond 58% (38/63) (MFE +1.03%)
   - −3.0% : fill 30min 9% · séance 29% (43/159) · gap 2% · délai 84.2min · rebond 70% (30/43) (MFE +1.6%)
   - −4.0% : fill 30min 5% · séance 18% (26/159) · gap 2% · délai 229.5min · rebond 49% (14/26) (MFE +0.95%)
   - −5.0% : fill 30min 3% · séance 13% (18/159) · gap 0% · délai 267.1min · rebond 70% (12/18) (MFE +1.27%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.39% (p90 −1.87%) → stop au-delà de −1.39% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.38% (p90 −1.5%) → stop au-delà de −1.08% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.02% (p90 −1.69%) → stop au-delà de −1.16% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=488 jambes) : jambe baissière méd −1.11% (p90 −2.74%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (45 séances) :
      · −1.0% : fill 96% (41/45) · rebond 38% (18/41)
      · −2.0% : fill 84% (33/45) · rebond 55% (19/33)
      · −3.0% : fill 54% (24/45) · rebond 71% (16/24)
      · −4.0% : fill 36% (15/45) · rebond 63% (9/15)
      · −5.0% : fill 28% (12/45) · rebond 73% (8/12)
   - **flat** (27 séances) :
      · −1.0% : fill 53% (15/27) · rebond 78% (11/15)
      · −2.0% : fill 25% (8/27) · rebond 76% (7/8)
      · −3.0% : fill 15% (5/27) · rebond 41% (3/5)
      · −4.0% : fill 5% (2/27) · rebond 69% (1/2)
      · −5.0% : fill 2% (1/27) · rebond 0% (0/1)
   - **gap-up** (87 séances) :
      · −1.0% : fill 47% (38/87) · rebond 59% (25/38)
      · −2.0% : fill 29% (22/87) · rebond 59% (12/22)
      · −3.0% : fill 20% (14/87) · rebond 75% (11/14)
      · −4.0% : fill 13% (9/87) · rebond 28% (4/9)
      · −5.0% : fill 9% (5/87) · rebond 69% (4/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 41% en base · 60% si les 15 1res min sont vertes (73 cas) · 27% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:21** → P(séance verte=clôture>ouverture) 76% si début vert vs 21% si rouge (base 41% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 279min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=64) : tient le vert **76%** · continue >prix actuel 47% ; creux résiduel méd -1.25% (q20 -2.04%) → **SL/trailing à −2.04%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.02% / q75 +2.15% → **scale +1.02% / runner +2.15%**, sortie à la clôture
  - **si ROUGE au coude** (n=96) : edge inversé — récupère vert seulement **21%** (continue à baisser 64%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.16%** (au-delà de la MAE q10 -4.16%), cible rebond +1.19% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.28% .. +2.1%] · haut q95 +3.19% · bas q05 -3.99%
   - 60min (n=160) : retour [-3.73% .. +2.17%] · haut q95 +3.52% · bas q05 -4.4%
   - 2h (n=160) : retour [-4.27% .. +2.64%] · haut q95 +3.99% · bas q05 -5.11%
   - 4h (n=160) : retour [-4.12% .. +2.69%] · haut q95 +4.11% · bas q05 -5.31%
   - 6h (n=160) : retour [-5.24% .. +3.41%] · haut q95 +4.21% · bas q05 -5.56%
   - session (n=160) : retour [-5.48% .. +3.26%] · haut q95 +4.45% · bas q05 -6.56%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.42%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.77 · part idiosyncratique 0.23
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 48.6  _(neutre)_
- **ADX** : 22.1  _(pas de tendance nette)_
- **MACD** : hist 0.332  _(pas de croisement recent)_
- **BB** : %B 0.5 · largeur 17.1%
- **ATR** : 6.11 (84.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.063  _(accumulation)_
- **Vol ratio** : 0.4  _(volume atone)_
- **Choppiness** : 58.6  _(transition)_
- **MA** : MA20 106.82 · MA50 117.12 · MA200 121.98  _(prix > MA20)_
- **Dist MA** : MA20 +0.1% · MA50 -8.7% · MA200 -12.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (705828 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
