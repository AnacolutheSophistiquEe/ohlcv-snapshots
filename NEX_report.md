# NEX

**Generated** : 2026-08-25T21:44:00.619321+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · €140.80  

> 🟡 **WAIT-FOR-DIP** — spot +2.8 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €140.80 (+2.8% vs entrée) · entrée €137.01 · stop €126.05 · T1 €138.66 · R/R 0.15  
> ↳ P(T1 av. stop) 43 % _(réel 5 s)_ · EV/risk 0.006 _(réel 5 s)_ (GBM -0.071) · ¼-Kelly 0.072 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.180 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €136.68–€137.34 (mid €137.01)
- Spot actuel : €140.80 (+2.8% au-dessus de la zone — repli à attendre)
- Stop : €126.05 (stop swing_plan-based (-8.77%))
- Targets : T1 €138.66 · R/R 0.15 | T2 €140.32 · R/R 0.3 | T3 €141.97 · R/R 0.45
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €126.05


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.64 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.77 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1280).
   - exécution **0.826 pt plus bas** dans le cas TYPIQUE (médiane), 0.826 au p90, **0.826 au pire**
   - perte réelle **9.596 %** en moyenne _(tirée par la queue)_, jusqu'à **9.596 %** — au lieu des 8.77 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0006 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.516 % | p01 -3.643 % | pire -9.596 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0047** [0.0004 ; 0.0247] _(largeur 2.4 pt, n_eff 173.1)_
   - swing : **0.4444** [0.3927 ; 0.4971] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4138** [0.3628 ; 0.4663] _(largeur 10.3 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 13.8 observations effectives », dont la borne haute a 95 % vaut environ 21.7 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (48.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-3.51 %** | CVaR **-5.25 %** | vol 2.3 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.51 % vs -7.85 % si l'on extrapolait par √5 _(rapport 0.956 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0188** (β de hausse 1.0932, asymétrie 0.932) vs FCHI — 618 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 126.75 sur atr_grid (3.5 ATR, 9.979 %) — p(stop avant cible) 0.1327 [0.10 ; 0.17], R/R 1.626, perte reelle 9.979 % (gap inclus), CVaR 9.979 %, EV 0.6432 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 5.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.277 %) — p(stop avant cible) 0.5287 [0.48 ; 0.58], R/R 2.42, perte reelle 6.706 % (gap inclus), EV -1.0095 % — **REFUSE**
      - refuse : cible atteinte seulement 5.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.529, borne haute 0.581 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.01 %) : P(cible) 5.2 % x 16.23 % + P(rien) 41.9 % x 4.03 % ne couvrent pas P(stop) 52.9 % x 6.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.32 ATR (stop 5.5 %) — p(stop avant cible) 0.4321 [0.38 ; 0.48], R/R 1.998, perte reelle 8.124 % (gap inclus), EV -0.8308 % — **REFUSE**
      - refuse : cible atteinte seulement 5.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.83 %) : P(cible) 5.2 % x 16.23 % + P(rien) 51.6 % x 3.55 % ne couvrent pas P(stop) 43.2 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 3.87 ATR (stop 12.781 %) — p(stop avant cible) 0.0605 [0.04 ; 0.09], R/R 1.27, perte reelle 12.781 % (gap inclus), EV 0.6235 % — **REFUSE**
      - refuse : cible atteinte seulement 5.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.27 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.78 % > budget 12.00 %
   - 🟢 support a 8.24 ATR (stop 25.221 %) — p(stop avant cible) 0.0008 [0.00 ; 0.01], R/R 0.643, perte reelle 25.221 % (gap inclus), EV 0.7389 % — **REFUSE**
      - refuse : cible atteinte seulement 5.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.64 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.22 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.713 %) — p(stop avant cible) 0.9075 [0.87 ; 0.93], R/R 9.524, perte reelle 1.704 % (gap inclus), EV -0.8115 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 9.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.907, borne haute 0.935 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.81 %) : P(cible) 1.2 % x 16.23 % + P(rien) 8.0 % x 6.67 % ne couvrent pas P(stop) 90.8 % x 1.70 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.426 %) — p(stop avant cible) 0.8217 [0.78 ; 0.86], R/R 5.737, perte reelle 2.829 % (gap inclus), EV -1.1041 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 5.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.822, borne haute 0.859 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.10 %) : P(cible) 1.8 % x 16.23 % + P(rien) 16.0 % x 5.80 % ne couvrent pas P(stop) 82.2 % x 2.83 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.138 %) — p(stop avant cible) 0.7345 [0.69 ; 0.78], R/R 3.976, perte reelle 4.082 % (gap inclus), EV -1.3167 % — **REFUSE**
      - refuse : cible atteinte seulement 2.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.735, borne haute 0.779 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.32 %) : P(cible) 2.7 % x 16.23 % + P(rien) 23.9 % x 5.22 % ne couvrent pas P(stop) 73.5 % x 4.08 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 2.851 %) — p(stop avant cible) 0.6699 [0.62 ; 0.72], R/R 3.328, perte reelle 4.876 % (gap inclus), EV -1.2 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.670, borne haute 0.718 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.20 %) : P(cible) 4.1 % x 16.23 % + P(rien) 28.9 % x 4.84 % ne couvrent pas P(stop) 67.0 % x 4.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 4.989 %) — p(stop avant cible) 0.461 [0.41 ; 0.51], R/R 2.108, perte reelle 7.697 % (gap inclus), EV -0.9172 % — **REFUSE**
      - refuse : cible atteinte seulement 5.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.92 %) : P(cible) 5.2 % x 16.23 % + P(rien) 48.7 % x 3.66 % ne couvrent pas P(stop) 46.1 % x 7.70 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 6.415 %) — p(stop avant cible) 0.3576 [0.31 ; 0.41], R/R 1.998, perte reelle 8.124 % (gap inclus), EV -0.2774 % — **REFUSE**
      - refuse : cible atteinte seulement 5.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.28 %) : P(cible) 5.2 % x 16.23 % + P(rien) 59.0 % x 3.01 % ne couvrent pas P(stop) 35.8 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 7.128 %) — p(stop avant cible) 0.2968 [0.25 ; 0.35], R/R 1.948, perte reelle 8.333 % (gap inclus), EV 0.1125 % — **REFUSE**
      - refuse : cible atteinte seulement 5.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.75 ATR (stop 7.84 %) — p(stop avant cible) 0.2341 [0.19 ; 0.28], R/R 1.893, perte reelle 8.571 % (gap inclus), EV 0.474 % — **REFUSE**
      - refuse : cible atteinte seulement 5.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 3.0 ATR (stop 8.553 %) — p(stop avant cible) 0.2073 [0.17 ; 0.25], R/R 1.691, perte reelle 9.596 % (gap inclus), EV 0.354 % — **REFUSE**
      - refuse : cible atteinte seulement 5.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 3.5 ATR (stop 9.979 %) — p(stop avant cible) 0.1327 [0.10 ; 0.17], R/R 1.626, perte reelle 9.979 % (gap inclus), EV 0.6432 % — **REFUSE**
      - refuse : cible atteinte seulement 5.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ grid_snapped a 3.87 ATR (stop 11.903 %) — p(stop avant cible) 0.0844 [0.06 ; 0.12], R/R 1.363, perte reelle 11.903 % (gap inclus), EV 0.6387 % — **REFUSE**
      - refuse : cible atteinte seulement 5.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.36 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 5.0 ATR (stop 14.255 %) — p(stop avant cible) 0.0305 [0.02 ; 0.05], R/R 1.138, perte reelle 14.255 % (gap inclus), EV 0.6733 % — **REFUSE**
      - refuse : cible atteinte seulement 5.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.25 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 15.681 %) — p(stop avant cible) 0.0145 [0.01 ; 0.03], R/R 1.035, perte reelle 15.681 % (gap inclus), EV 0.6943 % — **REFUSE**
      - refuse : cible atteinte seulement 5.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.68 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 17.106 %) — p(stop avant cible) 0.0108 [0.00 ; 0.03], R/R 0.949, perte reelle 17.106 % (gap inclus), EV 0.6897 % — **REFUSE**
      - refuse : cible atteinte seulement 5.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.95 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.11 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 18.532 %) — p(stop avant cible) 0.0058 [0.00 ; 0.02], R/R 0.876, perte reelle 18.532 % (gap inclus), EV 0.7141 % — **REFUSE**
      - refuse : cible atteinte seulement 5.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.88 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.53 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 19.957 %) — p(stop avant cible) 0.0031 [0.00 ; 0.01], R/R 0.813, perte reelle 19.957 % (gap inclus), EV 0.7324 % — **REFUSE**
      - refuse : cible atteinte seulement 5.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.81 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.96 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 21.383 %) — p(stop avant cible) 0.0023 [0.00 ; 0.01], R/R 0.759, perte reelle 21.383 % (gap inclus), EV 0.736 % — **REFUSE**
      - refuse : cible atteinte seulement 5.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.76 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.38 % > budget 12.00 %
   - 🟢 grid_snapped a 8.24 ATR (stop 24.343 %) — p(stop avant cible) 0.0008 [0.00 ; 0.01], R/R 0.667, perte reelle 24.343 % (gap inclus), EV 0.7396 % — **REFUSE**
      - refuse : cible atteinte seulement 5.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.67 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.34 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 140.8, ATR14 4.0143 (2.851 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.353 ATR = 1.006 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.143 % | 140.5993 | 88.04 % | 91.66 % | 93.32 % | 95.37 % | 96.93 % | 97.8 % |
| 0.1 ATR | 0.285 % | 140.3986 | 82.25 % | 87.93 % | 90.37 % | 93.21 % | 95.45 % | 97.0 % |
| 0.15 ATR | 0.428 % | 140.1979 | 75.59 % | 83.71 % | 86.94 % | 90.26 % | 93.97 % | 95.7 % |
| 0.2 ATR | 0.57 % | 139.9971 | 69.12 % | 78.7 % | 83.4 % | 88.29 % | 92.48 % | 95.0 % |
| 0.25 ATR | 0.713 % | 139.7964 | 62.55 % | 73.9 % | 79.27 % | 85.04 % | 90.41 % | 93.81 % |
| 0.35 ATR | 0.998 % | 139.395 | 50.29 % | 64.67 % | 72.0 % | 79.04 % | 86.45 % | 91.61 % |
| 0.5 ATR | 1.426 % | 138.7929 | 35.0 % | 52.89 % | 61.69 % | 70.96 % | 80.22 % | 87.61 % |
| 0.75 ATR | 2.138 % | 137.7893 | 20.29 % | 36.7 % | 47.84 % | 59.15 % | 70.43 % | 81.12 % |
| 1.0 ATR | 2.851 % | 136.7857 | 10.69 % | 24.53 % | 35.07 % | 48.82 % | 61.62 % | 74.63 % |
| 1.25 ATR | 3.564 % | 135.7821 | 4.9 % | 16.39 % | 25.25 % | 39.86 % | 54.7 % | 68.33 % |
| 1.5 ATR | 4.277 % | 134.7786 | 2.45 % | 11.09 % | 18.47 % | 30.91 % | 47.08 % | 60.94 % |
| 2.0 ATR | 5.702 % | 132.7714 | 0.78 % | 5.2 % | 10.02 % | 19.49 % | 35.61 % | 51.15 % |
| 2.5 ATR | 7.128 % | 130.7643 | 0.49 % | 2.65 % | 5.6 % | 11.52 % | 25.02 % | 39.36 % |
| 3.0 ATR | 8.553 % | 128.7571 | 0.2 % | 1.67 % | 3.24 % | 7.19 % | 17.71 % | 30.67 % |
| 4.0 ATR | 11.404 % | 124.7429 | 0.1 % | 0.49 % | 0.88 % | 1.87 % | 7.62 % | 18.08 % |
| 6.0 ATR | 17.106 % | 116.7143 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 1.38 % | 4.4 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.67 ATR | 0.76 ATR | 1.03 ATR | 1.25 ATR |
| **2 s.** | 0.24 ATR | 0.55 ATR | 0.62 ATR | 0.83 ATR | 0.99 ATR | 1.14 ATR | 1.59 ATR | 2.04 ATR |
| **3 s.** | 0.31 ATR | 0.71 ATR | 0.81 ATR | 1.05 ATR | 1.26 ATR | 1.44 ATR | 2.00 ATR | 2.63 ATR |
| **5 s.** | 0.42 ATR | 0.97 ATR | 1.11 ATR | 1.44 ATR | 1.76 ATR | 1.98 ATR | 2.68 ATR | 3.41 ATR |
| **10 s.** | 0.63 ATR | 1.40 ATR | 1.59 ATR | 2.12 ATR | 2.50 ATR | 2.84 ATR | 3.76 ATR | 4.84 ATR |
| **20 s.** | 0.99 ATR | 2.05 ATR | 2.26 ATR | 2.87 ATR | 3.45 ATR | 3.85 ATR | 5.18 ATR | 5.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.402–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (79.9 % des re-echantillons)
- **2 seance(s)** : plage utile 0.622–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.138 %, prix 137.7897), p(touche) 36.7 % (en stress 88.24 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 51.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.806–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.851 %, prix 136.7858), p(touche) 35.07 % (en stress 85.29 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.107–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (3.564 %, prix 135.7819), p(touche) 39.86 % (en stress 94.12 %)  ✅ optimum identifie (62.4 % des re-echantillons)
- **10 seance(s)** : plage utile 1.591–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (5.702 %, prix 132.7716), p(touche) 35.61 % (en stress 99.02 %)  ✅ optimum identifie (69.5 % des re-echantillons)
- **20 seance(s)** : plage utile 2.261–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (7.128 %, prix 130.7638), p(touche) 39.36 % (en stress 98.02 %)  ✅ optimum identifie (70.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.071 | EV/share : €-0.780 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 19 % | T3 5 %
- Kelly (position) : f* 0.287 | ¼-Kelly 0.072 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.7 | bear 11.8 | side 82.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 282.0 (= 2 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.696% → cible +1.206% / stop −8.0%, p_fill 26%, n_eff≈13.8) : P(cible|rempli) **43%** · **EV/risk +0.006** (×p_fill ; si rempli +0.20% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=7, n_eff=6))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→64% · +1.0%→50% · +2.0%→24% · +3.0%→10% · +5.0%→1% · +8.0%→0%
- Range intraday médian 3.0% (p90 4.72%) · excursion haute méd. +1.0% / basse méd. −1.43%
- Profil de vol intra : ouverture 1.747% vs midi 0.528% vs clôture 0.728% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 48% · recovery-V 19%)_
- **Régime intraday** : **chop** _(efficiency 0.108 ; neutre — autocorr -0.028)_ ; drift intra méd. -0.4% ; recovery-V 18%
- **σ réalisé intraday** 2.084% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 71% / whipsaw 29%
- POC intraday (dernière séance, temps-au-prix) : 141.89 (VA 141.33–142.87 ; dernier close 141.35)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 17% · rebond 56% · **stop −2.01%** sous le fill (sous le bruit) · cible +1.25% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. 0.35% · baisse 33% (gap-down >1% 6% · >2% 1%)
- Excursion ouverture 5min (n=160) : bas méd −0.43% (p90 −1.93%) · haut méd +0.29% · range méd 1.05%
- Excursion ouverture 15min (n=160) : bas méd −0.57% (p90 −2.08%) · haut méd +0.44% · range méd 1.3%
- Excursion ouverture 30min (n=160) : bas méd −0.59% (p90 −2.31%) · haut méd +0.57% · range méd 1.41%
- Excursion ouverture 60min (n=160) : bas méd −0.81% (p90 −2.58%) · haut méd +0.59% · range méd 1.57%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 141.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 46% · séance 63% (91/159) · gap 12% · délai 3.8min · rebond 46% (45/91) (MFE +0.78%)
   - −1.0% : fill 30min 28% · séance 55% (74/159) · gap 6% · délai 21.7min · rebond 46% (36/74) (MFE +0.86%)
   - −1.5% : fill 30min 17% · séance 42% (55/159) · gap 1% · délai 45.4min · rebond 44% (26/55) (MFE +0.8%)
   - −2.0% : fill 30min 12% · séance 28% (39/159) · gap 1% · délai 53.1min · rebond 54% (20/39) (MFE +1.14%)
   - −3.0% : fill 30min 4% · séance 17% (23/159) · gap 0% · délai 133.5min · rebond 56% (13/23) (MFE +1.25%)
   - −4.0% : fill 30min 0% · séance 6% (9/159) · gap 0% · délai 350.2min · rebond 11% (3/9) (MFE +0.48%)
   - −5.0% : fill 30min 0% · séance 2% (3/159) · gap 0% · délai 410.2min · rebond 42% (1/3) (MFE +0.73%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.15% (p90 −1.15%) → stop au-delà de −0.77% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.15% (p90 −0.96%) → stop au-delà de −0.58% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.16% (p90 −0.6%) → stop au-delà de −0.45% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=329 jambes) : jambe baissière méd −1.09% (p90 −2.42%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (30 séances) :
      · −1.0% : fill 80% (25/30) · rebond 55% (13/25)
      · −2.0% : fill 50% (16/30) · rebond 44% (7/16)
      · −3.0% : fill 32% (11/30) · rebond 44% (6/11)
      · −4.0% : fill 21% (6/30) · rebond 12% (2/6)
      · −5.0% : fill 12% (3/30) · rebond 42% (1/3)
   - **flat** (33 séances) :
      · −1.0% : fill 59% (20/33) · rebond 40% (9/20)
      · −2.0% : fill 30% (10/33) · rebond 38% (4/10)
      · −3.0% : fill 18% (6/33) · rebond 45% (3/6)
      · −4.0% : fill 8% (2/33) · rebond 0% (0/2)
      · −5.0% : fill 0% (0/33) · rebond 0% (0/0)
   - **gap-up** (96 séances) :
      · −1.0% : fill 44% (29/96) · rebond 45% (14/29)
      · −2.0% : fill 20% (13/96) · rebond 76% (9/13)
      · −3.0% : fill 11% (6/96) · rebond 78% (4/6)
      · −4.0% : fill 0% (1/96) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/96) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 68% si les 15 1res min sont vertes (86 cas) · 20% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **45min** → P(séance verte=clôture>ouverture) 75% si début vert vs 22% si rouge (base 46% · écart 53 pts) ; prédictivité sature ensuite (plafond brut 249min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **75%** · continue >prix actuel 48% ; creux résiduel méd -0.83% (q20 -2.03%) → **SL/trailing à −2.03%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.06% / q75 +1.63% → **scale +1.06% / runner +1.63%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **22%** (continue à baisser 55%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.04%** (au-delà de la MAE q10 -3.04%), cible rebond +1.04% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.01% .. +2.31%] · haut q95 +2.62% · bas q05 -2.59%
   - 60min (n=160) : retour [-2.82% .. +2.66%] · haut q95 +2.83% · bas q05 -3.24%
   - 2h (n=160) : retour [-3.55% .. +2.56%] · haut q95 +2.94% · bas q05 -3.74%
   - 4h (n=160) : retour [-3.12% .. +2.74%] · haut q95 +3.04% · bas q05 -3.88%
   - 6h (n=160) : retour [-3.81% .. +3.51%] · haut q95 +3.91% · bas q05 -4.17%
   - session (n=160) : retour [-3.51% .. +2.88%] · haut q95 +4.18% · bas q05 -4.67%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.94%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 54.2  _(neutre)_
- **ADX** : 14.5  _(pas de tendance nette)_
- **MACD** : hist 0.337  _(pas de croisement recent)_
- **BB** : %B 0.68 · largeur 13.0%
- **ATR** : 4.01 (46.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.183  _(distribution)_
- **Vol ratio** : 0.49  _(volume atone)_
- **Choppiness** : 67.0  _(marche en range (choppy))_
- **MA** : MA20 137.58 · MA50 138.87 · MA200 133.29  _(prix > MA20)_
- **Dist MA** : MA20 +2.3% · MA50 +1.4% · MA200 +5.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (824239 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
