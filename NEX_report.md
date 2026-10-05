# NEX

**Generated** : 2026-10-05T00:11:14.170848+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 8/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €136.40  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (usable=false (intervalle le plus large 27.1 pt > 25)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot €136.40 (+1.5% vs entrée) · entrée €134.34 · stop €132.32 · T1 €136.18 · R/R 0.91  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €133.97–€134.71 (mid €134.34)
- Spot actuel : €136.40 (+1.5% au-dessus de la zone — repli à attendre)
- Stop : €132.32 (plancher anti-bruit 5 s — stop EV-optimal −1.5% (first-passage 5 s réel) ; -1.50 % depuis l'entree)
- Targets : T1 €136.18 · R/R 0.91 | T2 €138.03 · R/R 1.83 | T3 €139.88 · R/R 2.74
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €132.32


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.64 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (6.46 %)** : le gap seul le franchit 0.469 % des séances (6 fois sur 1280).
   - exécution **1.708 pt plus bas** dans le cas TYPIQUE (médiane), 2.514 au p90, **3.136 au pire**
   - perte réelle **8.124 %** en moyenne _(tirée par la queue)_, jusqu'à **9.596 %** — au lieu des 6.46 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0078 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.516 % | p01 -3.643 % | pire -9.596 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3671** [0.298 ; 0.4406] _(largeur 14.3 pt, n_eff 173.1)_
   - swing : **0.4813** [0.429 ; 0.5339] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.5181** [0.4655 ; 0.5704] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (27.1 pt), swing (31.5 pt), deep (35.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-3.52 %** | CVaR **-5.28 %** | vol 2.31 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.51 % vs -7.85 % si l'on extrapolait par √5 _(rapport 0.956 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0021** (β de hausse 1.0894, asymétrie 0.9199) vs FCHI — 619 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 129.0535 sur grid_snapped (1.69 ATR, 5.386 %) — p(stop avant cible) 0.4015 [0.35 ; 0.45], R/R 3.566, perte reelle 5.623 % (gap inclus), CVaR 7.196 %, EV -0.0149 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.9113 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.061 %) — p(stop avant cible) 0.5502 [0.50 ; 0.60], R/R 4.737, perte reelle 4.233 % (gap inclus), EV -0.1979 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 4.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.550, borne haute 0.602 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 1.3 % x 20.05 % + P(rien) 43.6 % x 4.27 % ne couvrent pas P(stop) 55.0 % x 4.23 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ swing_based a 1.69 ATR (stop 6.095 %) — p(stop avant cible) 0.3589 [0.31 ; 0.41], R/R 3.181, perte reelle 6.302 % (gap inclus), EV -0.0535 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.05 %) : P(cible) 1.3 % x 20.05 % + P(rien) 62.8 % x 3.09 % ne couvrent pas P(stop) 35.9 % x 6.30 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ sr_based a 2.34 ATR (stop 7.846 %) — p(stop avant cible) 0.1974 [0.16 ; 0.24], R/R 2.49, perte reelle 8.052 % (gap inclus), EV 0.4187 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 7.76 ATR (stop 22.541 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 0.846, perte reelle 23.712 % (gap inclus), EV 0.5234 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.43 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.677 %) — p(stop avant cible) 0.9216 [0.89 ; 0.95], R/R 28.238, perte reelle 0.71 % (gap inclus), EV -0.0231 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 28.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.922, borne haute 0.947 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.02 %) : P(cible) 0.3 % x 20.05 % + P(rien) 7.5 % x 7.54 % ne couvrent pas P(stop) 92.2 % x 0.71 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 1.354 %) — p(stop avant cible) 0.8377 [0.80 ; 0.87], R/R 14.072, perte reelle 1.425 % (gap inclus), EV -0.1597 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 14.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.838, borne haute 0.874 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 0.6 % x 20.05 % + P(rien) 15.6 % x 5.82 % ne couvrent pas P(stop) 83.8 % x 1.42 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 2.031 %) — p(stop avant cible) 0.7504 [0.70 ; 0.79], R/R 9.486, perte reelle 2.114 % (gap inclus), EV -0.1566 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 9.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.750, borne haute 0.794 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 0.9 % x 20.05 % + P(rien) 24.0 % x 5.16 % ne couvrent pas P(stop) 75.0 % x 2.11 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 2.707 %) — p(stop avant cible) 0.6903 [0.64 ; 0.74], R/R 7.147, perte reelle 2.805 % (gap inclus), EV -0.2398 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.690, borne haute 0.737 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.24 %) : P(cible) 1.0 % x 20.05 % + P(rien) 29.9 % x 4.98 % ne couvrent pas P(stop) 69.0 % x 2.81 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 3.384 %) — p(stop avant cible) 0.6131 [0.56 ; 0.66], R/R 5.719, perte reelle 3.505 % (gap inclus), EV -0.1487 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 5.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.613, borne haute 0.663 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 1.3 % x 20.05 % + P(rien) 37.4 % x 4.64 % ne couvrent pas P(stop) 61.3 % x 3.51 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 1.69 ATR (stop 5.386 %) — p(stop avant cible) 0.4015 [0.35 ; 0.45], R/R 3.566, perte reelle 5.623 % (gap inclus), EV -0.0149 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.01 %) : P(cible) 1.3 % x 20.05 % + P(rien) 58.5 % x 3.38 % ne couvrent pas P(stop) 40.2 % x 5.62 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 2.34 ATR (stop 7.137 %) — p(stop avant cible) 0.2579 [0.21 ; 0.31], R/R 2.735, perte reelle 7.33 % (gap inclus), EV 0.1962 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 9.476 %) — p(stop avant cible) 0.1374 [0.10 ; 0.18], R/R 2.08, perte reelle 9.639 % (gap inclus), EV 0.4076 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 10.829 %) — p(stop avant cible) 0.0884 [0.06 ; 0.12], R/R 1.82, perte reelle 11.017 % (gap inclus), EV 0.4396 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.5 ATR (stop 12.183 %) — p(stop avant cible) 0.0669 [0.04 ; 0.10], R/R 1.602, perte reelle 12.515 % (gap inclus), EV 0.4085 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.63 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 13.537 %) — p(stop avant cible) 0.039 [0.02 ; 0.06], R/R 1.429, perte reelle 14.031 % (gap inclus), EV 0.4166 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.54 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 14.891 %) — p(stop avant cible) 0.0231 [0.01 ; 0.04], R/R 1.289, perte reelle 15.558 % (gap inclus), EV 0.4474 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.38 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 16.244 %) — p(stop avant cible) 0.0123 [0.00 ; 0.03], R/R 1.179, perte reelle 17.002 % (gap inclus), EV 0.4714 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.99 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 17.598 %) — p(stop avant cible) 0.0084 [0.00 ; 0.02], R/R 1.114, perte reelle 18.002 % (gap inclus), EV 0.4874 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.90 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 18.952 %) — p(stop avant cible) 0.0043 [0.00 ; 0.02], R/R 1.014, perte reelle 19.776 % (gap inclus), EV 0.51 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.67 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 20.305 %) — p(stop avant cible) 0.0026 [0.00 ; 0.01], R/R 0.958, perte reelle 20.925 % (gap inclus), EV 0.5181 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.54 % > budget 12.00 %
   - 🟢 grid_snapped a 7.76 ATR (stop 21.832 %) — p(stop avant cible) 0.0019 [0.00 ; 0.01], R/R 0.872, perte reelle 23.002 % (gap inclus), EV 0.5211 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.50 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 136.4, ATR14 3.6929 (2.707 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.348 ATR = 0.942 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.135 % | 136.2154 | 87.94 % | 91.56 % | 93.32 % | 95.18 % | 97.03 % | 97.9 % |
| 0.1 ATR | 0.271 % | 136.0307 | 82.06 % | 87.83 % | 90.47 % | 93.21 % | 95.65 % | 97.0 % |
| 0.15 ATR | 0.406 % | 135.8461 | 75.39 % | 83.61 % | 87.03 % | 90.26 % | 94.16 % | 95.7 % |
| 0.2 ATR | 0.541 % | 135.6614 | 68.82 % | 78.41 % | 83.3 % | 88.29 % | 92.78 % | 95.0 % |
| 0.25 ATR | 0.677 % | 135.4768 | 62.16 % | 73.7 % | 79.27 % | 85.14 % | 90.7 % | 93.81 % |
| 0.35 ATR | 0.948 % | 135.1075 | 49.71 % | 64.38 % | 71.81 % | 78.84 % | 86.65 % | 91.61 % |
| 0.5 ATR | 1.354 % | 134.5536 | 34.61 % | 52.6 % | 61.39 % | 70.77 % | 80.22 % | 87.41 % |
| 0.75 ATR | 2.031 % | 133.6303 | 20.29 % | 36.31 % | 47.25 % | 58.76 % | 70.23 % | 80.92 % |
| 1.0 ATR | 2.707 % | 132.7071 | 10.59 % | 24.14 % | 34.68 % | 48.52 % | 61.62 % | 74.23 % |
| 1.25 ATR | 3.384 % | 131.7839 | 4.8 % | 16.0 % | 24.85 % | 39.57 % | 54.4 % | 67.83 % |
| 1.5 ATR | 4.061 % | 130.8607 | 2.45 % | 11.19 % | 18.66 % | 30.81 % | 46.88 % | 60.34 % |
| 2.0 ATR | 5.415 % | 129.0143 | 0.88 % | 5.3 % | 10.12 % | 19.49 % | 35.21 % | 50.75 % |
| 2.5 ATR | 6.768 % | 127.1678 | 0.49 % | 2.65 % | 5.6 % | 11.52 % | 24.43 % | 38.86 % |
| 3.0 ATR | 8.122 % | 125.3214 | 0.2 % | 1.67 % | 3.24 % | 7.09 % | 17.51 % | 30.37 % |
| 4.0 ATR | 10.829 % | 121.6286 | 0.1 % | 0.49 % | 0.88 % | 1.87 % | 7.52 % | 17.88 % |
| 6.0 ATR | 16.244 % | 114.2428 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 1.38 % | 4.4 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.67 ATR | 0.76 ATR | 1.02 ATR | 1.24 ATR |
| **2 s.** | 0.24 ATR | 0.54 ATR | 0.62 ATR | 0.82 ATR | 0.98 ATR | 1.13 ATR | 1.60 ATR | 2.06 ATR |
| **3 s.** | 0.31 ATR | 0.70 ATR | 0.80 ATR | 1.04 ATR | 1.25 ATR | 1.45 ATR | 2.01 ATR | 2.63 ATR |
| **5 s.** | 0.42 ATR | 0.96 ATR | 1.10 ATR | 1.44 ATR | 1.76 ATR | 1.98 ATR | 2.67 ATR | 3.40 ATR |
| **10 s.** | 0.63 ATR | 1.40 ATR | 1.58 ATR | 2.10 ATR | 2.47 ATR | 2.82 ATR | 3.75 ATR | 4.82 ATR |
| **20 s.** | 0.97 ATR | 2.03 ATR | 2.24 ATR | 2.85 ATR | 3.43 ATR | 3.83 ATR | 5.17 ATR | 5.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.397–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (75.9 % des re-echantillons)
- **2 seance(s)** : plage utile 0.617–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.031 %, prix 133.6297), p(touche) 36.31 % (en stress 88.24 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.795–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.707 %, prix 132.7076), p(touche) 34.68 % (en stress 84.31 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.098–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (3.384 %, prix 131.7842), p(touche) 39.57 % (en stress 93.14 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.581–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (5.415 %, prix 129.0139), p(touche) 35.21 % (en stress 99.02 %)  ✅ optimum identifie (69.8 % des re-echantillons)
- **20 seance(s)** : plage utile 2.242–4.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (6.768 %, prix 127.1684), p(touche) 38.86 % (en stress 98.02 %)  ✅ optimum identifie (69.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.118 | EV/share : €-0.238 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 15 % | T3 4 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 24.6 | bear 22.6 | side 52.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 273.0 (= 2 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.513% → cible +1.374% / stop −1.5%, p_fill 43%, n_eff≈47.2) : P(cible|rempli) **22%** · **EV/risk -0.150** (×p_fill ; si rempli -0.52% du capital)
  - **swing** (entrée dip −3.333% → cible +6.469% / stop −3.235%, p_fill 31%, n_eff≈36.2) : P(cible|rempli) **9%** · **EV/risk -0.041** (×p_fill ; si rempli -0.43% du capital)
  - **deep** (entrée dip −5.149% → cible +8.508% / stop −4.281%, p_fill 25%, n_eff≈27.4) : P(cible|rempli) **30%** · **EV/risk +0.117** (×p_fill ; si rempli +2.02% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→70% · +1.0%→57% · +2.0%→28% · +3.0%→12% · +5.0%→2% · +8.0%→1%
- Range intraday médian 2.73% (p90 4.75%) · excursion haute méd. +1.13% / basse méd. −1.13%
- Profil de vol intra : ouverture 1.673% vs midi 0.529% vs clôture 0.71% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 44% · recovery-V 13%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; mean-reverting — autocorr -0.04)_ ; drift intra méd. -0.332% ; recovery-V 10%
- **σ réalisé intraday** 1.991% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 71% / whipsaw 35%
- POC intraday (dernière séance, temps-au-prix) : 136.2225 (VA 135.7475–137.0775 ; dernier close 136.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 25% · rebond 31% · **stop −2.1%** sous le fill (sous le bruit) · cible +0.53% · R/R 0.25 (high win-rate)
- Gaps overnight (n=159) : méd. 0.37% · baisse 25% (gap-down >1% 3% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.34% (p90 −1.71%) · haut méd +0.28% · range méd 0.92%
- Excursion ouverture 15min (n=160) : bas méd −0.45% (p90 −1.95%) · haut méd +0.44% · range méd 1.27%
- Excursion ouverture 30min (n=160) : bas méd −0.53% (p90 −2.08%) · haut méd +0.6% · range méd 1.4%
- Excursion ouverture 60min (n=160) : bas méd −0.73% (p90 −2.28%) · haut méd +0.64% · range méd 1.5%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 136.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 38% · séance 57% (88/159) · gap 9% · délai 3.9min · rebond 41% (38/88) (MFE +0.64%)
   - −1.0% : fill 30min 20% · séance 46% (69/159) · gap 3% · délai 51.9min · rebond 35% (27/69) (MFE +0.58%)
   - −1.5% : fill 30min 12% · séance 36% (54/159) · gap 0% · délai 62.0min · rebond 31% (19/54) (MFE +0.58%)
   - −2.0% : fill 30min 7% · séance 25% (39/159) · gap 0% · délai 111.9min · rebond 31% (15/39) (MFE +0.53%)
   - −3.0% : fill 30min 4% · séance 14% (23/159) · gap 0% · délai 268.3min · rebond 37% (10/23) (MFE +0.59%)
   - −4.0% : fill 30min 2% · séance 5% (10/159) · gap 0% · délai 161.7min · rebond 8% (3/10) (MFE +0.38%)
   - −5.0% : fill 30min 0% · séance 3% (4/159) · gap 0% · délai 260.4min · rebond 24% (2/4) (MFE +0.39%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.15% (p90 −0.99%) → stop au-delà de −0.79% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.15% (p90 −0.81%) → stop au-delà de −0.74% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.16% (p90 −0.78%) → stop au-delà de −0.72% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=327 jambes) : jambe baissière méd −1.01% (p90 −2.27%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (22 séances) :
      · −1.0% : fill 77% (17/22) · rebond 27% (6/17)
      · −2.0% : fill 61% (12/22) · rebond 12% (2/12)
      · −3.0% : fill 43% (9/22) · rebond 15% (3/9)
      · −4.0% : fill 26% (6/22) · rebond 4% (1/6)
      · −5.0% : fill 20% (3/22) · rebond 20% (1/3)
   - **flat** (36 séances) :
      · −1.0% : fill 54% (21/36) · rebond 27% (7/21)
      · −2.0% : fill 25% (12/36) · rebond 33% (5/12)
      · −3.0% : fill 16% (8/36) · rebond 32% (3/8)
      · −4.0% : fill 5% (3/36) · rebond 8% (1/3)
      · −5.0% : fill 0% (1/36) · rebond 100% (1/1)
   - **gap-up** (101 séances) :
      · −1.0% : fill 35% (31/101) · rebond 44% (14/31)
      · −2.0% : fill 18% (15/101) · rebond 45% (8/15)
      · −3.0% : fill 6% (6/101) · rebond 78% (4/6)
      · −4.0% : fill 0% (1/101) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/101) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 65% si les 15 1res min sont vertes (85 cas) · 22% si rouges (75 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **20min** → P(séance verte=clôture>ouverture) 69% si début vert vs 23% si rouge (base 46% · écart 46 pts) ; prédictivité sature ensuite (plafond brut 242min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **69%** · continue >prix actuel 58% ; creux résiduel méd -0.98% (q20 -1.84%) → **SL/trailing à −1.84%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.1% / q75 +1.84% → **scale +1.1% / runner +1.84%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **23%** (continue à baisser 63%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.05%** (au-delà de la MAE q10 -3.05%), cible rebond +0.91% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.96% .. +1.64%] · haut q95 +2.01% · bas q05 -2.58%
   - 60min (n=160) : retour [-2.59% .. +2.13%] · haut q95 +2.44% · bas q05 -3.21%
   - 2h (n=160) : retour [-3.07% .. +2.15%] · haut q95 +2.67% · bas q05 -3.66%
   - 4h (n=160) : retour [-2.91% .. +2.47%] · haut q95 +3.05% · bas q05 -3.75%
   - 6h (n=160) : retour [-3.6% .. +3.4%] · haut q95 +3.53% · bas q05 -4.13%
   - session (n=160) : retour [-3.38% .. +2.74%] · haut q95 +3.86% · bas q05 -4.65%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.93%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.47 · part idiosyncratique 0.53
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 58.0  _(momentum haussier)_
- **ADX** : 10.7  _(pas de tendance nette)_
- **MACD** : hist -0.43  _(pas de croisement recent)_
- **BB** : %B 0.46 · largeur 10.6%
- **ATR** : 3.69 (23.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.182  _(distribution)_
- **Vol ratio** : 0.85  _(volume normal)_
- **Choppiness** : 51.2  _(transition)_
- **MA** : MA20 137.04 · MA50 137.26 · MA200 135.49  _(prix < MA20)_
- **Dist MA** : MA20 -0.5% · MA50 -0.6% · MA200 +0.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (843058 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
