# PRY

**Generated** : 2026-11-26T21:50:50.044258+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 5/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €99.24  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (24 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot €99.24 (+2.5% vs entrée) · entrée €96.86 · stop €89.11 · T1 €99.63 · R/R 0.36  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-26 : 99.24 · ATR Wilder 5.78 (5.83 %)_
- **Swing** : plage **92.77 → 88.57** (-6.52 % a -10.75 % sous la cloture, 0.73 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 92.37-95.09 (A) ; 89.22-92.05 (A). stop INDICATIF 83.33 (-5.92 % sous le bas ; sous le support 86.22-86.95 (- 0,5 ATR)).
- **Deep** : plage **88.57 → 75.58** (-10.75 % a -23.84 % sous la cloture, 2.25 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 86.22-86.95 (B) ; 83.16-84.97 (A) ; 79.43-81.87 (A) ; 76.37-78.57 (A). stop INDICATIF 68.04 (-9.97 % sous le bas ; sous le support 70.94-72.58 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (2.43 ATR sous le plus haut 20 s., RSI(2) 56.9 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 92.37-95.09 (A, -4.18 %) ; 89.22-92.05 (A, -7.24 %) ; 86.22-86.95 (B, -12.38 %) ; 83.16-84.97 (A, -14.38 %) ; 79.43-81.87 (A, -17.5 %) ; 76.37-78.57 (A, -20.82 %)
- Resistances reelles au-dessus : 103.98-105.9 (A, 4.77 %) ; 110.3-112.3 (A, 11.14 %) ; 115.65-117.1 (A, 16.54 %) ; 119.65-122.29 (A, 20.57 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.73 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (10.84 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1270).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 10.84 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.903 % | p01 -3.733 % | pire -9.998 % _(sur 1270 séances)_
- **P(stop avant cible)** _(source : daily, 1271 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0115** [0.0024 ; 0.0365] _(largeur 3.4 pt, n_eff 173.1)_
   - swing : **0.3198** [0.2723 ; 0.3703] _(largeur 9.8 pt, n_eff 345.8)_
   - deep : **0.2682** [0.2236 ; 0.3167] _(largeur 9.3 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 43.7 observations effectives », dont la borne haute a 95 % vaut environ 6.9 %.
- ⚠ **5 s — échantillon insuffisant sur : swing (34.2 pt), deep (44.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 300 séances)** : VaR **-4.54 %** | CVaR **-5.94 %** | vol 2.8 %/j
   - _fenêtre arrêtée : rupture de regime a 360 seances en arriere (volatilite 1.79 % contre 3.04 % aujourd'hui, rapport 0.59)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.82 % vs -7.96 % si l'on extrapolait par √5 _(rapport 0.857 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0752** (β de hausse 1.2277, asymétrie 0.8757) vs FTSEMIB — 568 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.608× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 92.3351 sur atr_grid (1.25 ATR, 6.958 %) — p(stop avant cible) 0.388 [0.34 ; 0.44], R/R 7.663, perte reelle 7.254 % (gap inclus), CVaR 9.183 %, EV -0.2884 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 8.349 %) — p(stop avant cible) 0.2983 [0.25 ; 0.35], R/R 6.165, perte reelle 9.017 % (gap inclus), EV -0.1598 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.33 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 0.0 % x 55.59 % + P(rien) 70.2 % x 3.61 % ne couvrent pas P(stop) 29.8 % x 9.02 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+55.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ sr_based a 1.82 ATR (stop 12.625 %) — p(stop avant cible) 0.1137 [0.08 ; 0.15], R/R 3.907, perte reelle 14.227 % (gap inclus), EV 0.2099 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 16.26 % > budget 12.00 %
   - 🟢 support a 3.34 ATR (stop 21.092 %) — p(stop avant cible) 0.0066 [0.00 ; 0.02], R/R 2.501, perte reelle 22.222 % (gap inclus), EV 0.4292 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.48 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.392 %) — p(stop avant cible) 0.8555 [0.82 ; 0.89], R/R 37.444, perte reelle 1.485 % (gap inclus), EV -0.189 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 37.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.856, borne haute 0.889 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.19 %) : P(cible) 0.0 % x 55.59 % + P(rien) 14.4 % x 7.48 % ne couvrent pas P(stop) 85.5 % x 1.48 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+55.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.5 ATR (stop 2.783 %) — p(stop avant cible) 0.724 [0.68 ; 0.77], R/R 18.982, perte reelle 2.929 % (gap inclus), EV -0.2625 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 18.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.724, borne haute 0.769 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.26 %) : P(cible) 0.0 % x 55.59 % + P(rien) 27.6 % x 6.73 % ne couvrent pas P(stop) 72.4 % x 2.93 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+55.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.75 ATR (stop 4.175 %) — p(stop avant cible) 0.607 [0.55 ; 0.66], R/R 12.89, perte reelle 4.313 % (gap inclus), EV -0.4494 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 12.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.607, borne haute 0.657 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.45 %) : P(cible) 0.0 % x 55.59 % + P(rien) 39.3 % x 5.52 % ne couvrent pas P(stop) 60.7 % x 4.31 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+55.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.0 ATR (stop 5.566 %) — p(stop avant cible) 0.4818 [0.43 ; 0.53], R/R 9.772, perte reelle 5.688 % (gap inclus), EV -0.3128 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 9.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.31 %) : P(cible) 0.0 % x 55.59 % + P(rien) 51.8 % x 4.69 % ne couvrent pas P(stop) 48.2 % x 5.69 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+55.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.25 ATR (stop 6.958 %) — p(stop avant cible) 0.388 [0.34 ; 0.44], R/R 7.663, perte reelle 7.254 % (gap inclus), EV -0.2884 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.29 %) : P(cible) 0.0 % x 55.59 % + P(rien) 61.2 % x 4.13 % ne couvrent pas P(stop) 38.8 % x 7.25 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+55.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ grid_snapped a 1.82 ATR (stop 11.806 %) — p(stop avant cible) 0.1214 [0.09 ; 0.16], R/R 4.31, perte reelle 12.897 % (gap inclus), EV 0.2808 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.46 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 13.916 %) — p(stop avant cible) 0.085 [0.06 ; 0.12], R/R 3.534, perte reelle 15.731 % (gap inclus), EV 0.3309 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 17.00 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 15.307 %) — p(stop avant cible) 0.0694 [0.05 ; 0.10], R/R 3.31, perte reelle 16.793 % (gap inclus), EV 0.3773 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 17.37 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 16.699 %) — p(stop avant cible) 0.0554 [0.03 ; 0.08], R/R 3.124, perte reelle 17.792 % (gap inclus), EV 0.3569 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 17.91 % > budget 12.00 %
   - 🟢 grid_snapped a 3.34 ATR (stop 20.273 %) — p(stop avant cible) 0.0269 [0.01 ; 0.05], R/R 2.703, perte reelle 20.565 % (gap inclus), EV 0.3856 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.35 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 22.265 %) — p(stop avant cible) 0.0061 [0.00 ; 0.02], R/R 2.417, perte reelle 22.994 % (gap inclus), EV 0.4305 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.49 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 25.048 %) — p(stop avant cible) 0.0032 [0.00 ; 0.01], R/R 2.16, perte reelle 25.735 % (gap inclus), EV 0.4403 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.37 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 27.831 %) — p(stop avant cible) 0.0021 [0.00 ; 0.01], R/R 1.847, perte reelle 30.093 % (gap inclus), EV 0.4384 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.43 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 30.614 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 1.718, perte reelle 32.353 % (gap inclus), EV 0.4425 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.31 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 33.397 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.664, perte reelle 33.397 % (gap inclus), EV 0.4488 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.22 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 36.181 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.536, perte reelle 36.181 % (gap inclus), EV 0.4488 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.22 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 38.964 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.427, perte reelle 38.964 % (gap inclus), EV 0.4488 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.22 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 41.747 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.332, perte reelle 41.747 % (gap inclus), EV 0.4488 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.22 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 44.53 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.248, perte reelle 44.53 % (gap inclus), EV 0.4488 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.22 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 99.24, ATR14 5.5239 (5.566 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.345 ATR = 1.92 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.278 % | 98.9638 | 91.68 % | 93.95 % | 94.64 % | 95.43 % | 97.3 % | 97.88 % |
| 0.1 ATR | 0.557 % | 98.6876 | 84.95 % | 88.8 % | 91.07 % | 92.94 % | 95.3 % | 96.37 % |
| 0.15 ATR | 0.835 % | 98.4114 | 77.43 % | 84.24 % | 87.3 % | 90.46 % | 93.21 % | 94.55 % |
| 0.2 ATR | 1.113 % | 98.1352 | 69.6 % | 79.09 % | 82.64 % | 87.08 % | 91.01 % | 92.73 % |
| 0.25 ATR | 1.392 % | 97.859 | 61.98 % | 74.33 % | 78.57 % | 83.4 % | 88.41 % | 90.72 % |
| 0.35 ATR | 1.948 % | 97.3066 | 49.31 % | 64.12 % | 71.13 % | 76.94 % | 84.12 % | 87.99 % |
| 0.5 ATR | 2.783 % | 96.478 | 35.25 % | 52.43 % | 60.52 % | 68.49 % | 77.32 % | 82.85 % |
| 0.75 ATR | 4.175 % | 95.0971 | 19.8 % | 34.99 % | 43.95 % | 55.17 % | 66.03 % | 74.77 % |
| 1.0 ATR | 5.566 % | 93.7161 | 10.1 % | 23.89 % | 32.74 % | 45.63 % | 57.14 % | 67.1 % |
| 1.25 ATR | 6.958 % | 92.3351 | 5.54 % | 16.45 % | 24.7 % | 35.49 % | 48.65 % | 59.43 % |
| 1.5 ATR | 8.349 % | 90.9541 | 2.48 % | 9.81 % | 16.77 % | 25.25 % | 38.06 % | 50.96 % |
| 2.0 ATR | 11.132 % | 88.1921 | 0.4 % | 4.26 % | 7.94 % | 15.01 % | 25.67 % | 39.25 % |
| 2.5 ATR | 13.916 % | 85.4302 | 0.0 % | 1.78 % | 3.57 % | 8.55 % | 16.78 % | 28.86 % |
| 3.0 ATR | 16.699 % | 82.6682 | 0.0 % | 0.89 % | 1.88 % | 4.67 % | 10.69 % | 20.99 % |
| 4.0 ATR | 22.265 % | 77.1443 | 0.0 % | 0.2 % | 0.69 % | 2.09 % | 5.69 % | 13.02 % |
| 6.0 ATR | 33.397 % | 66.0964 | 0.0 % | 0.0 % | 0.0 % | 0.4 % | 2.0 % | 4.24 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.34 ATR | 0.40 ATR | 0.54 ATR | 0.67 ATR | 0.75 ATR | 1.00 ATR | 1.29 ATR |
| **2 s.** | 0.24 ATR | 0.54 ATR | 0.61 ATR | 0.80 ATR | 0.97 ATR | 1.13 ATR | 1.49 ATR | 1.93 ATR |
| **3 s.** | 0.30 ATR | 0.66 ATR | 0.73 ATR | 0.99 ATR | 1.24 ATR | 1.40 ATR | 1.88 ATR | 2.34 ATR |
| **5 s.** | 0.38 ATR | 0.89 ATR | 1.02 ATR | 1.31 ATR | 1.51 ATR | 1.76 ATR | 2.39 ATR | 2.96 ATR |
| **10 s.** | 0.55 ATR | 1.21 ATR | 1.34 ATR | 1.70 ATR | 2.04 ATR | 2.32 ATR | 3.14 ATR | 4.37 ATR |
| **20 s.** | 0.74 ATR | 1.54 ATR | 1.75 ATR | 2.30 ATR | 2.75 ATR | 3.12 ATR | 4.69 ATR | 5.83 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.396 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.607–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.175 %, prix 95.0967), p(touche) 34.99 % (en stress 88.12 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.734–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.175 %, prix 95.0967), p(touche) 43.95 % (en stress 96.04 %)  ✅ optimum identifie (67.6 % des re-echantillons)
- **5 seance(s)** : plage utile 1.016–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (6.958 %, prix 92.3349), p(touche) 35.49 % (en stress 92.08 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.336–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.349 %, prix 90.9545), p(touche) 38.06 % (en stress 98.02 %)  ✅ optimum identifie (63.5 % des re-echantillons)
- **20 seance(s)** : plage utile 1.754–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (11.132 %, prix 88.1926), p(touche) 39.25 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.032 | EV/share : €-0.250 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 26 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.5 | bear 14.6 | side 78.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.391% → cible +2.851% / stop −8.0%, p_fill 42%, n_eff≈43.7) : P(cible|rempli) **8%** · **EV/risk -0.038** (×p_fill ; si rempli -0.73% du capital)
  - **swing** (entrée dip −5.274% → cible +6.569% / stop −5.876%, p_fill 25%, n_eff≈28.9) : P(cible|rempli) **35%** · **EV/risk +0.026** (×p_fill ; si rempli +0.60% du capital)
  - **deep** (entrée dip −8.14% → cible +9.581% / stop −9.09%, p_fill 14%, n_eff≈16.4) : P(cible|rempli) **47%** · **EV/risk +0.051** (×p_fill ; si rempli +3.33% du capital)
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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.74 · part idiosyncratique 0.26
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-3 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-3 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 48.3  _(neutre)_
- **ADX** : 16.1  _(pas de tendance nette)_
- **MACD** : hist -0.693  _(bearish_recent)_
- **BB** : %B 0.2 · largeur 19.6%
- **ATR** : 5.52 (65.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.204  _(distribution)_
- **Vol ratio** : 0.92  _(volume normal)_
- **Choppiness** : 51.2  _(transition)_
- **MA** : MA20 105.55 · MA50 112.81 · MA200 122.21  _(prix < MA20)_
- **Dist MA** : MA20 -6.0% · MA50 -12.0% · MA200 -18.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (689995 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
