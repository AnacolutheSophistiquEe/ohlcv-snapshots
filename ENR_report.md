# ENR

**Generated** : 2026-11-11T01:07:09.343684+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 2/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €119.48  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-0 sess · macro taux)  
> ↳ spot €119.48 (+0.7% vs entrée) · entrée €118.69 · stop €109.20 · T1 €123.52 · R/R 0.51  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-10 : 119.48 · ATR Wilder 7.16 (5.99 %)_
- **Swing** : plage **110.69 → 104.96** (-7.36 % a -12.15 % sous la cloture, 0.8 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 109.88-110.92 (A). stop INDICATIF 99.63 (-5.08 % sous le bas ; sous le support 103.21-104.4 (- 0,5 ATR)).
- **Deep** : plage **104.96 → 94.02** (-12.15 % a -21.31 % sous la cloture, 1.53 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 103.21-104.4 (B) ; 98.56-100.32 (A) ; 94.0-95.27 (A). stop INDICATIF 85.72 (-8.83 % sous le bas ; sous le support 89.3-92.68 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (3.59 ATR sous le plus haut 20 s., RSI(2) 40.6 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 113.47-116.84 (A, -2.21 %) ; 109.88-110.92 (A, -7.16 %) ; 103.21-104.4 (B, -12.62 %) ; 98.56-100.32 (A, -16.03 %) ; 94.0-95.27 (A, -20.26 %) ; 89.3-92.68 (A, -22.43 %)
- Resistances reelles au-dessus : 122.83-124.46 (A, 2.8 %) ; 130.89-133.85 (A, 9.55 %) ; 135.7-139.16 (A, 13.58 %) ; 140.18-143.38 (B, 17.33 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.75 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.97 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1274).
   - exécution **7.2 pt plus bas** dans le cas TYPIQUE (médiane), 22.87 au p90, **26.787 au pire**
   - perte réelle **21.854 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 8.97 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0303 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.382 % | p01 -5.39 % | pire -35.757 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0078** [0.0011 ; 0.0303] _(largeur 2.9 pt, n_eff 173.1)_
   - swing : **0.2773** [0.2321 ; 0.3262] _(largeur 9.4 pt, n_eff 345.8)_
   - deep : **0.2917** [0.2457 ; 0.3412] _(largeur 9.6 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 84.3 observations effectives », dont la borne haute a 95 % vaut environ 3.6 %.
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_target_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 87.3 observations effectives », dont la borne haute a 95 % vaut environ 3.4 %.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-4.83 %** | CVaR **-6.82 %** | vol 3.22 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 6.19 % contre 3.21 % aujourd'hui, rapport 1.93)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.9 % vs -10.11 % si l'on extrapolait par √5 _(rapport 0.881 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3008** (β de hausse 1.05, asymétrie 1.2389) vs GDAXI — 600 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 110.4844 sur support (0.62 ATR, 7.529 %) — p(stop avant cible) 0.4467 [0.39 ; 0.50], R/R 4.05, perte reelle 8.192 % (gap inclus), CVaR 12.8 %, EV -1.1464 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0487 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 4.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : CVaR 95 % 12.80 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.62 ATR (stop 7.529 %) — p(stop avant cible) 0.4467 [0.39 ; 0.50], R/R 4.05, perte reelle 8.192 % (gap inclus), EV -1.1464 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 4.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.80 % > budget 12.00 %
      - ⚠ support DETECTE a 0.39 ATR du spot — compartiment <1, mesure a 48.2 % de casse (IC clusterise [0.451 ; 0.515] sur 1149 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.15 %) : P(cible) 0.3 % x 33.18 % + P(rien) 55.1 % x 4.40 % ne couvrent pas P(stop) 44.7 % x 8.19 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_based a 1.5 ATR (stop 10.092 %) — p(stop avant cible) 0.3076 [0.26 ; 0.36], R/R 3.09, perte reelle 10.736 % (gap inclus), EV -1.04 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.44 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.04 %) : P(cible) 0.3 % x 33.18 % + P(rien) 69.0 % x 3.15 % ne couvrent pas P(stop) 30.8 % x 10.74 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ swing_based a 1.26 ATR (stop 11.881 %) — p(stop avant cible) 0.1714 [0.13 ; 0.21], R/R 2.626, perte reelle 12.634 % (gap inclus), EV -0.4462 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.29 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.45 %) : P(cible) 0.3 % x 33.18 % + P(rien) 82.6 % x 1.97 % ne couvrent pas P(stop) 17.1 % x 12.63 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 2.43 ATR (stop 19.738 %) — p(stop avant cible) 0.0129 [0.00 ; 0.03], R/R 1.572, perte reelle 21.105 % (gap inclus), EV 0.3067 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.20 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.682 %) — p(stop avant cible) 0.8718 [0.83 ; 0.90], R/R 19.065, perte reelle 1.74 % (gap inclus), EV -0.3584 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 19.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.872, borne haute 0.904 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 0.1 % x 33.18 % + P(rien) 12.7 % x 8.77 % ne couvrent pas P(stop) 87.2 % x 1.74 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 grid_snapped a 0.62 ATR (stop 6.177 %) — p(stop avant cible) 0.5462 [0.49 ; 0.60], R/R 5.052, perte reelle 6.567 % (gap inclus), EV -1.1273 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 5.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.546, borne haute 0.598 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.13 %) : P(cible) 0.3 % x 33.18 % + P(rien) 45.1 % x 5.25 % ne couvrent pas P(stop) 54.6 % x 6.57 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 13.456 %) — p(stop avant cible) 0.1197 [0.09 ; 0.16], R/R 2.341, perte reelle 14.174 % (gap inclus), EV -0.1888 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.18 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.19 %) : P(cible) 0.3 % x 33.18 % + P(rien) 87.8 % x 1.62 % ne couvrent pas P(stop) 12.0 % x 14.17 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 grid_snapped a 2.43 ATR (stop 18.386 %) — p(stop avant cible) 0.0382 [0.02 ; 0.06], R/R 1.741, perte reelle 19.053 % (gap inclus), EV 0.1861 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.74 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 23.548 %) — p(stop avant cible) 0.0045 [0.00 ; 0.02], R/R 1.252, perte reelle 26.507 % (gap inclus), EV 0.3515 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.83 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 26.912 %) — p(stop avant cible) 0.0028 [0.00 ; 0.01], R/R 1.146, perte reelle 28.946 % (gap inclus), EV 0.3907 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.45 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 30.276 %) — p(stop avant cible) 0.0016 [0.00 ; 0.01], R/R 1.055, perte reelle 31.463 % (gap inclus), EV 0.4032 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.24 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 33.64 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 0.968, perte reelle 34.283 % (gap inclus), EV 0.4071 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.12 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 37.004 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 0.896, perte reelle 37.033 % (gap inclus), EV 0.4072 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.15 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 40.368 %) — p(stop avant cible) 0.0008 [0.00 ; 0.01], R/R 0.822, perte reelle 40.368 % (gap inclus), EV 0.4054 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.18 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 43.732 %) — p(stop avant cible) 0.0003 [0.00 ; 0.01], R/R 0.759, perte reelle 43.732 % (gap inclus), EV 0.4125 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.02 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 47.096 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.704, perte reelle 47.096 % (gap inclus), EV 0.4166 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.96 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 50.46 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.658, perte reelle 50.46 % (gap inclus), EV 0.4166 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.96 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 53.824 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.616, perte reelle 53.824 % (gap inclus), EV 0.4166 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.96 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 119.48, ATR14 8.0386 (6.728 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.368 ATR = 2.476 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.336 % | 119.0781 | 91.42 % | 94.18 % | 95.65 % | 96.24 % | 97.31 % | 97.99 % |
| 0.1 ATR | 0.673 % | 118.6761 | 83.63 % | 88.25 % | 90.61 % | 92.67 % | 94.73 % | 95.78 % |
| 0.15 ATR | 1.009 % | 118.2742 | 76.33 % | 82.43 % | 85.97 % | 88.71 % | 91.44 % | 93.57 % |
| 0.2 ATR | 1.346 % | 117.8723 | 70.32 % | 78.97 % | 83.0 % | 86.63 % | 89.65 % | 92.16 % |
| 0.25 ATR | 1.682 % | 117.4704 | 63.51 % | 74.53 % | 79.25 % | 83.37 % | 87.66 % | 90.85 % |
| 0.35 ATR | 2.355 % | 116.6665 | 51.87 % | 65.05 % | 70.55 % | 76.14 % | 82.59 % | 87.04 % |
| 0.5 ATR | 3.364 % | 115.4607 | 36.69 % | 52.22 % | 59.98 % | 67.03 % | 75.22 % | 81.21 % |
| 0.75 ATR | 5.046 % | 113.4511 | 19.82 % | 36.23 % | 45.75 % | 55.05 % | 66.27 % | 74.57 % |
| 1.0 ATR | 6.728 % | 111.4414 | 11.24 % | 26.06 % | 35.18 % | 45.25 % | 58.21 % | 66.93 % |
| 1.25 ATR | 8.41 % | 109.4318 | 6.21 % | 17.47 % | 25.49 % | 36.44 % | 49.55 % | 59.4 % |
| 1.5 ATR | 10.092 % | 107.4221 | 2.96 % | 11.35 % | 18.48 % | 28.71 % | 42.39 % | 53.17 % |
| 2.0 ATR | 13.456 % | 103.4029 | 0.79 % | 4.34 % | 9.19 % | 17.23 % | 29.35 % | 41.91 % |
| 2.5 ATR | 16.82 % | 99.3836 | 0.3 % | 2.07 % | 4.25 % | 10.2 % | 20.4 % | 32.16 % |
| 3.0 ATR | 20.184 % | 95.3643 | 0.1 % | 0.89 % | 2.08 % | 5.35 % | 13.23 % | 24.32 % |
| 4.0 ATR | 26.912 % | 87.3257 | 0.1 % | 0.39 % | 1.19 % | 2.48 % | 7.06 % | 13.87 % |
| 6.0 ATR | 40.368 % | 71.2486 | 0.0 % | 0.2 % | 0.4 % | 0.89 % | 2.19 % | 5.83 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.37 ATR | 0.42 ATR | 0.56 ATR | 0.67 ATR | 0.75 ATR | 1.06 ATR | 1.34 ATR |
| **2 s.** | 0.24 ATR | 0.54 ATR | 0.61 ATR | 0.83 ATR | 1.03 ATR | 1.18 ATR | 1.60 ATR | 1.95 ATR |
| **3 s.** | 0.30 ATR | 0.68 ATR | 0.77 ATR | 1.06 ATR | 1.27 ATR | 1.45 ATR | 1.96 ATR | 2.42 ATR |
| **5 s.** | 0.37 ATR | 0.88 ATR | 1.01 ATR | 1.36 ATR | 1.66 ATR | 1.88 ATR | 2.52 ATR | 3.12 ATR |
| **10 s.** | 0.51 ATR | 1.24 ATR | 1.41 ATR | 1.86 ATR | 2.24 ATR | 2.53 ATR | 3.52 ATR | 4.85 ATR |
| **20 s.** | 0.73 ATR | 1.64 ATR | 1.86 ATR | 2.46 ATR | 2.96 ATR | 3.41 ATR | 4.96 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.418 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 21.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.613–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.046 %, prix 113.451), p(touche) 36.23 % (en stress 89.22 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.768–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.728 %, prix 111.4414), p(touche) 35.18 % (en stress 91.18 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (86.5 % des re-echantillons)
- **5 seance(s)** : plage utile 1.007–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.41 %, prix 109.4317), p(touche) 36.44 % (en stress 96.04 %)  ✅ optimum identifie (90.8 % des re-echantillons)
- **10 seance(s)** : plage utile 1.409–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.092 %, prix 107.4221), p(touche) 42.39 % (en stress 100.0 %)  ✅ optimum identifie (92.6 % des re-echantillons)
- **20 seance(s)** : plage utile 1.863–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (13.456 %, prix 103.4028), p(touche) 41.91 % (en stress 99.0 %)  ✅ optimum identifie (91.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.04 | EV/share : €-0.378 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 7 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 28.1 | bear 61.6 | side 10.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.663% → cible +4.063% / stop −8.0%, p_fill 80%, n_eff≈84.3) : P(cible|rempli) **3%** · **EV/risk -0.069** (×p_fill ; si rempli -0.69% du capital)
  - **swing** (entrée dip −1.453% → cible +15.256% / stop −7.628%, p_fill 75%, n_eff≈87.3) : P(cible|rempli) **0%** · **EV/risk -0.185** (×p_fill ; si rempli -1.89% du capital)
  - **deep** (entrée dip −2.238% → cible +16.187% / stop −10.323%, p_fill 76%, n_eff≈86.7) : P(cible|rempli) **2%** · **EV/risk -0.171** (×p_fill ; si rempli -2.32% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→62% · +2.0%→34% · +3.0%→15% · +5.0%→5% · +8.0%→1%
- Range intraday médian 3.62% (p90 6.06%) · excursion haute méd. +1.37% / basse méd. −1.89%
- Profil de vol intra : ouverture 1.961% vs midi 0.824% vs clôture 1.048% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑1%/↓0% ; spike-down 61% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; mean-reverting — autocorr -0.032)_ ; drift intra méd. -0.864% ; recovery-V 25%
- **σ réalisé intraday** 2.273% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 59% / bas 83% / whipsaw 42%
- POC intraday (dernière séance, temps-au-prix) : 121.5065 (VA 120.2185–123.5995 ; dernier close 118.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 18% · rebond 57% · **stop −4.86%** sous le fill (sous le bruit) · cible +1.05% · R/R 0.22 (high win-rate)
- Gaps overnight (n=159) : méd. 0.38% · baisse 38% (gap-down >1% 20% · >2% 9%)
- Excursion ouverture 5min (n=160) : bas méd −0.49% (p90 −1.69%) · haut méd +0.49% · range méd 1.14%
- Excursion ouverture 15min (n=160) : bas méd −0.67% (p90 −2.05%) · haut méd +0.58% · range méd 1.45%
- Excursion ouverture 30min (n=160) : bas méd −0.83% (p90 −2.19%) · haut méd +0.62% · range méd 1.69%
- Excursion ouverture 60min (n=160) : bas méd −0.99% (p90 −2.35%) · haut méd +0.68% · range méd 1.81%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 118.68 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 52% · séance 70% (115/159) · gap 30% · délai 0.2min · rebond 48% (59/115) (MFE +0.88%)
   - −1.0% : fill 30min 40% · séance 66% (107/159) · gap 20% · délai 8.6min · rebond 51% (59/107) (MFE +1.04%)
   - −1.5% : fill 30min 29% · séance 53% (88/159) · gap 13% · délai 12.6min · rebond 55% (48/88) (MFE +1.28%)
   - −2.0% : fill 30min 23% · séance 44% (73/159) · gap 9% · délai 20.7min · rebond 50% (41/73) (MFE +1.0%)
   - −3.0% : fill 30min 10% · séance 29% (48/159) · gap 3% · délai 251.6min · rebond 40% (24/48) (MFE +0.66%)
   - −4.0% : fill 30min 6% · séance 18% (32/159) · gap 2% · délai 200.1min · rebond 57% (20/32) (MFE +1.05%)
   - −5.0% : fill 30min 4% · séance 13% (24/159) · gap 0% · délai 397.7min · rebond 38% (11/24) (MFE +0.78%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −2.17%) → stop au-delà de −1.55% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.39% (p90 −1.63%) → stop au-delà de −0.96% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.45% (p90 −1.66%) → stop au-delà de −0.95% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=526 jambes) : jambe baissière méd −1.04% (p90 −2.31%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 99% (53/54) · rebond 41% (26/53)
      · −2.0% : fill 84% (41/54) · rebond 49% (20/41)
      · −3.0% : fill 59% (30/54) · rebond 40% (14/30)
      · −4.0% : fill 39% (22/54) · rebond 75% (16/22)
      · −5.0% : fill 30% (18/54) · rebond 47% (10/18)
   - **flat** (18 séances) :
      · −1.0% : fill 59% (13/18) · rebond 64% (9/13)
      · −2.0% : fill 33% (8/18) · rebond 68% (6/8)
      · −3.0% : fill 20% (5/18) · rebond 48% (3/5)
      · −4.0% : fill 6% (3/18) · rebond 59% (2/3)
      · −5.0% : fill 5% (2/18) · rebond 0% (0/2)
   - **gap-up** (87 séances) :
      · −1.0% : fill 46% (41/87) · rebond 61% (24/41)
      · −2.0% : fill 23% (24/87) · rebond 46% (15/24)
      · −3.0% : fill 13% (13/87) · rebond 36% (7/13)
      · −4.0% : fill 9% (7/87) · rebond 11% (2/7)
      · −5.0% : fill 5% (4/87) · rebond 12% (1/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 61% si les 15 1res min sont vertes (71 cas) · 30% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:31** → P(séance verte=clôture>ouverture) 72% si début vert vs 21% si rouge (base 43% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 290min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **72%** · continue >prix actuel 56% ; creux résiduel méd -1.18% (q20 -2.25%) → **SL/trailing à −2.25%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.08% / q75 +2.1% → **scale +1.08% / runner +2.1%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **21%** (continue à baisser 57%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.96%** (au-delà de la MAE q10 -4.96%), cible rebond +1.06% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.97% .. +1.62%] · haut q95 +2.08% · bas q05 -2.65%
   - 60min (n=160) : retour [-2.5% .. +1.42%] · haut q95 +2.41% · bas q05 -3.07%
   - 2h (n=160) : retour [-2.53% .. +2.22%] · haut q95 +2.56% · bas q05 -3.58%
   - 4h (n=160) : retour [-2.61% .. +2.42%] · haut q95 +3.02% · bas q05 -4.04%
   - 6h (n=160) : retour [-3.22% .. +3.06%] · haut q95 +3.68% · bas q05 -4.31%
   - session (n=160) : retour [-5.78% .. +2.83%] · haut q95 +4.66% · bas q05 -6.21%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — ENR = **plat / peu volatil** (vol intra méd 2.37%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.51 · part idiosyncratique 0.49
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-17 — ENR earnings (J-4 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-17 — ENR earnings (J-4 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 40.7  _(momentum baissier)_
- **ADX** : 22.7  _(pas de tendance nette)_
- **MACD** : hist -0.51  _(pas de croisement recent)_
- **BB** : %B 0.22 · largeur 21.4%
- **ATR** : 8.04 (80.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.014  _(neutre)_
- **Vol ratio** : 0.79  _(volume normal)_
- **Choppiness** : 54.3  _(transition)_
- **MA** : MA20 127.18 · MA50 136.8 · MA200 153.68  _(prix < MA20)_
- **Dist MA** : MA20 -6.1% · MA50 -12.7% · MA200 -22.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (700159 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
