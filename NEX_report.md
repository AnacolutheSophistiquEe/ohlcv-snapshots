# NEX

**Generated** : 2026-09-11T21:49:45.997624+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · €142.20  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-11 — US Core CPI (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot €142.20 (+2.7% vs entrée) · entrée €138.43 · stop €127.36 · T1 €142.45 · R/R 0.36  
> ↳ P(T1 av. stop) 53 % · EV/risk 0.068 · ¼-Kelly 0.027 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.320 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €138.16–€138.70 (mid €138.43)
- Spot actuel : €142.20 (+2.7% au-dessus de la zone — repli à attendre)
- Stop : €127.36 (stop swing_plan-based (-8.86%))
- Targets : T1 €142.45 · R/R 0.36 | T2 €142.49 · R/R 0.37 | T3 €142.53 · R/R 0.37
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €127.36


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.64 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.86 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1279).
   - exécution **0.736 pt plus bas** dans le cas TYPIQUE (médiane), 0.736 au p90, **0.736 au pire**
   - perte réelle **9.596 %** en moyenne _(tirée par la queue)_, jusqu'à **9.596 %** — au lieu des 8.86 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0006 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.516 % | p01 -3.644 % | pire -9.596 % _(sur 1279 séances)_
- **P(stop avant cible)** _(source : daily, 1280 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0042** [0.0003 ; 0.0237] _(largeur 2.3 pt, n_eff 173.1)_
   - swing : **0.391** [0.3407 ; 0.4432] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3491** [0.3003 ; 0.4004] _(largeur 10.0 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 11.9 observations effectives », dont la borne haute a 95 % vaut environ 25.3 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (32.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-3.5 %** | CVaR **-5.21 %** | vol 2.3 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.51 % vs -7.83 % si l'on extrapolait par √5 _(rapport 0.959 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0086** (β de hausse 1.0948, asymétrie 0.9213) vs FCHI — 619 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 125.4003 sur grid_snapped (3.6 ATR, 11.814 %) — p(stop avant cible) 0.0793 [0.05 ; 0.11], R/R 1.272, perte reelle 11.814 % (gap inclus), CVaR 11.814 %, EV 0.5401 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 5.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.543 %) — p(stop avant cible) 0.4808 [0.43 ; 0.53], R/R 1.952, perte reelle 7.697 % (gap inclus), EV -1.3113 % — **REFUSE**
      - refuse : cible atteinte seulement 5.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.31 %) : P(cible) 5.5 % x 15.02 % + P(rien) 46.4 % x 3.37 % ne couvrent pas P(stop) 48.1 % x 7.70 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.66 ATR (stop 6.966 %) — p(stop avant cible) 0.2878 [0.24 ; 0.34], R/R 1.849, perte reelle 8.124 % (gap inclus), EV 0.0239 % — **REFUSE**
      - refuse : cible atteinte seulement 5.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 3.6 ATR (stop 12.835 %) — p(stop avant cible) 0.0564 [0.04 ; 0.08], R/R 1.17, perte reelle 12.835 % (gap inclus), EV 0.517 % — **REFUSE**
      - refuse : cible atteinte seulement 5.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.84 % > budget 12.00 %
   - 🟢 support a 8.0 ATR (stop 26.171 %) — p(stop avant cible) 0.0007 [0.00 ; 0.01], R/R 0.574, perte reelle 26.171 % (gap inclus), EV 0.6276 % — **REFUSE**
      - refuse : cible atteinte seulement 5.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.17 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.757 %) — p(stop avant cible) 0.9093 [0.88 ; 0.94], R/R 8.497, perte reelle 1.768 % (gap inclus), EV -0.9116 % — **REFUSE**
      - refuse : cible atteinte seulement 1.3 % du temps (< 15 %) meme a 10 seances : le R/R de 8.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.909, borne haute 0.936 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.91 %) : P(cible) 1.3 % x 15.02 % + P(rien) 7.8 % x 6.46 % ne couvrent pas P(stop) 90.9 % x 1.77 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.514 %) — p(stop avant cible) 0.8103 [0.77 ; 0.85], R/R 4.947, perte reelle 3.037 % (gap inclus), EV -1.2711 % — **REFUSE**
      - refuse : cible atteinte seulement 1.9 % du temps (< 15 %) meme a 10 seances : le R/R de 4.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.810, borne haute 0.849 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.27 %) : P(cible) 1.9 % x 15.02 % + P(rien) 17.1 % x 5.29 % ne couvrent pas P(stop) 81.0 % x 3.04 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.272 %) — p(stop avant cible) 0.7112 [0.66 ; 0.76], R/R 3.63, perte reelle 4.138 % (gap inclus), EV -1.2912 % — **REFUSE**
      - refuse : cible atteinte seulement 3.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.711, borne haute 0.757 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.29 %) : P(cible) 3.0 % x 15.02 % + P(rien) 25.9 % x 4.63 % ne couvrent pas P(stop) 71.1 % x 4.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.029 %) — p(stop avant cible) 0.6336 [0.58 ; 0.68], R/R 2.971, perte reelle 5.057 % (gap inclus), EV -1.1873 % — **REFUSE**
      - refuse : cible atteinte seulement 4.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.634, borne haute 0.683 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.19 %) : P(cible) 4.4 % x 15.02 % + P(rien) 32.2 % x 4.19 % ne couvrent pas P(stop) 63.4 % x 5.06 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 3.786 %) — p(stop avant cible) 0.5472 [0.49 ; 0.60], R/R 2.402, perte reelle 6.254 % (gap inclus), EV -1.1672 % — **REFUSE**
      - refuse : cible atteinte seulement 5.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.547, borne haute 0.599 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.17 %) : P(cible) 5.5 % x 15.02 % + P(rien) 39.8 % x 3.60 % ne couvrent pas P(stop) 54.7 % x 6.25 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.66 ATR (stop 5.945 %) — p(stop avant cible) 0.3748 [0.33 ; 0.43], R/R 1.849, perte reelle 8.124 % (gap inclus), EV -0.6027 % — **REFUSE**
      - refuse : cible atteinte seulement 5.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.60 %) : P(cible) 5.5 % x 15.02 % + P(rien) 57.0 % x 2.83 % ne couvrent pas P(stop) 37.5 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 7.572 %) — p(stop avant cible) 0.2474 [0.20 ; 0.29], R/R 1.753, perte reelle 8.571 % (gap inclus), EV 0.1762 % — **REFUSE**
      - refuse : cible atteinte seulement 5.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 8.33 %) — p(stop avant cible) 0.2001 [0.16 ; 0.24], R/R 1.674, perte reelle 8.974 % (gap inclus), EV 0.3636 % — **REFUSE**
      - refuse : cible atteinte seulement 5.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 9.087 %) — p(stop avant cible) 0.1635 [0.13 ; 0.21], R/R 1.566, perte reelle 9.596 % (gap inclus), EV 0.4146 % — **REFUSE**
      - refuse : cible atteinte seulement 5.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 3.6 ATR (stop 11.814 %) — p(stop avant cible) 0.0793 [0.05 ; 0.11], R/R 1.272, perte reelle 11.814 % (gap inclus), EV 0.5401 % — **REFUSE**
      - refuse : cible atteinte seulement 5.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.5 ATR (stop 13.63 %) — p(stop avant cible) 0.0412 [0.02 ; 0.07], R/R 1.102, perte reelle 13.63 % (gap inclus), EV 0.5355 % — **REFUSE**
      - refuse : cible atteinte seulement 5.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.63 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 15.145 %) — p(stop avant cible) 0.0209 [0.01 ; 0.04], R/R 0.992, perte reelle 15.145 % (gap inclus), EV 0.5726 % — **REFUSE**
      - refuse : cible atteinte seulement 5.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.14 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 16.659 %) — p(stop avant cible) 0.0135 [0.01 ; 0.03], R/R 0.902, perte reelle 16.659 % (gap inclus), EV 0.5721 % — **REFUSE**
      - refuse : cible atteinte seulement 5.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.66 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 18.174 %) — p(stop avant cible) 0.0055 [0.00 ; 0.02], R/R 0.827, perte reelle 18.174 % (gap inclus), EV 0.6044 % — **REFUSE**
      - refuse : cible atteinte seulement 5.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.17 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 19.688 %) — p(stop avant cible) 0.0029 [0.00 ; 0.01], R/R 0.763, perte reelle 19.688 % (gap inclus), EV 0.6219 % — **REFUSE**
      - refuse : cible atteinte seulement 5.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.69 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 21.203 %) — p(stop avant cible) 0.0021 [0.00 ; 0.01], R/R 0.709, perte reelle 21.203 % (gap inclus), EV 0.6257 % — **REFUSE**
      - refuse : cible atteinte seulement 5.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.20 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 22.717 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.661, perte reelle 22.717 % (gap inclus), EV 0.6267 % — **REFUSE**
      - refuse : cible atteinte seulement 5.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.72 % > budget 12.00 %
   - 🟢 grid_snapped a 8.0 ATR (stop 25.15 %) — p(stop avant cible) 0.0007 [0.00 ; 0.01], R/R 0.597, perte reelle 25.15 % (gap inclus), EV 0.6283 % — **REFUSE**
      - refuse : cible atteinte seulement 5.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.15 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 142.2, ATR14 4.3071 (3.029 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.349 ATR = 1.057 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.151 % | 141.9846 | 87.83 % | 91.45 % | 93.22 % | 95.27 % | 96.93 % | 97.8 % |
| 0.1 ATR | 0.303 % | 141.7693 | 82.14 % | 87.92 % | 90.46 % | 93.3 % | 95.54 % | 96.9 % |
| 0.15 ATR | 0.454 % | 141.5539 | 75.27 % | 83.69 % | 87.02 % | 90.34 % | 94.06 % | 95.6 % |
| 0.2 ATR | 0.606 % | 141.3386 | 68.6 % | 78.49 % | 83.28 % | 88.37 % | 92.67 % | 94.9 % |
| 0.25 ATR | 0.757 % | 141.1232 | 62.12 % | 73.77 % | 79.25 % | 85.22 % | 90.59 % | 93.7 % |
| 0.35 ATR | 1.06 % | 140.6925 | 49.85 % | 64.54 % | 71.98 % | 79.11 % | 86.63 % | 91.5 % |
| 0.5 ATR | 1.514 % | 140.0464 | 34.74 % | 52.75 % | 61.55 % | 70.84 % | 80.3 % | 87.3 % |
| 0.75 ATR | 2.272 % | 138.9696 | 20.51 % | 36.74 % | 47.59 % | 59.01 % | 70.2 % | 80.7 % |
| 1.0 ATR | 3.029 % | 137.8929 | 10.6 % | 24.36 % | 34.91 % | 48.77 % | 61.49 % | 74.0 % |
| 1.25 ATR | 3.786 % | 136.8161 | 4.81 % | 16.21 % | 24.98 % | 39.7 % | 54.36 % | 67.5 % |
| 1.5 ATR | 4.543 % | 135.7393 | 2.36 % | 11.0 % | 18.39 % | 30.64 % | 46.63 % | 60.0 % |
| 2.0 ATR | 6.058 % | 133.5857 | 0.79 % | 5.11 % | 9.83 % | 19.11 % | 35.25 % | 50.7 % |
| 2.5 ATR | 7.572 % | 131.4321 | 0.49 % | 2.65 % | 5.6 % | 11.33 % | 24.75 % | 38.9 % |
| 3.0 ATR | 9.087 % | 129.2786 | 0.2 % | 1.67 % | 3.24 % | 7.09 % | 17.52 % | 30.4 % |
| 4.0 ATR | 12.116 % | 124.9714 | 0.1 % | 0.49 % | 0.88 % | 1.87 % | 7.52 % | 17.9 % |
| 6.0 ATR | 18.174 % | 116.3571 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 1.39 % | 4.4 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.67 ATR | 0.76 ATR | 1.03 ATR | 1.24 ATR |
| **2 s.** | 0.24 ATR | 0.54 ATR | 0.62 ATR | 0.83 ATR | 0.99 ATR | 1.13 ATR | 1.58 ATR | 2.02 ATR |
| **3 s.** | 0.31 ATR | 0.71 ATR | 0.80 ATR | 1.05 ATR | 1.25 ATR | 1.44 ATR | 1.99 ATR | 2.63 ATR |
| **5 s.** | 0.42 ATR | 0.97 ATR | 1.10 ATR | 1.44 ATR | 1.75 ATR | 1.96 ATR | 2.66 ATR | 3.40 ATR |
| **10 s.** | 0.63 ATR | 1.39 ATR | 1.57 ATR | 2.11 ATR | 2.49 ATR | 2.83 ATR | 3.75 ATR | 4.82 ATR |
| **20 s.** | 0.96 ATR | 2.03 ATR | 2.24 ATR | 2.85 ATR | 3.43 ATR | 3.83 ATR | 5.17 ATR | 5.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.398–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (78.1 % des re-echantillons)
- **2 seance(s)** : plage utile 0.621–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.272 %, prix 138.9692), p(touche) 36.74 % (en stress 88.24 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.801–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.029 %, prix 137.8928), p(touche) 34.91 % (en stress 85.29 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.104–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (3.786 %, prix 136.8163), p(touche) 39.7 % (en stress 93.14 %)  ✅ optimum identifie (62.0 % des re-echantillons)
- **10 seance(s)** : plage utile 1.572–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.058 %, prix 133.5855), p(touche) 35.25 % (en stress 98.02 %)  ✅ optimum identifie (72.5 % des re-echantillons)
- **20 seance(s)** : plage utile 2.242–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (7.572 %, prix 131.4326), p(touche) 38.9 % (en stress 98.0 %)  ✅ optimum identifie (70.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.083 | EV/share : €-0.916 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 11 % | T2 11 % | T3 10 %
- Kelly (position) : f* 0.108 | ¼-Kelly 0.027 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 14.9 | bear 79.4 | side 5.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 427.0 (= 3 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.652% → cible +2.904% / stop −8.0%, p_fill 23%, n_eff≈11.9) : P(cible|rempli) **8%** · **EV/risk -0.001** (×p_fill ; si rempli -0.03% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=7, n_eff=6))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→65% · +1.0%→51% · +2.0%→22% · +3.0%→10% · +5.0%→1% · +8.0%→0%
- Range intraday médian 2.95% (p90 4.72%) · excursion haute méd. +1.01% / basse méd. −1.35%
- Profil de vol intra : ouverture 1.739% vs midi 0.517% vs clôture 0.7% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 47% · recovery-V 15%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; mean-reverting — autocorr -0.041)_ ; drift intra méd. -0.566% ; recovery-V 11%
- **σ réalisé intraday** 1.96% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 68% / whipsaw 26%
- POC intraday (dernière séance, temps-au-prix) : 138.1975 (VA 137.3925–138.7725 ; dernier close 136.7)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 16% · rebond 50% · **stop −1.94%** sous le fill (sous le bruit) · cible +1.05% · R/R 0.54 (high win-rate)
- Gaps overnight (n=159) : méd. 0.36% · baisse 31% (gap-down >1% 5% · >2% 1%)
- Excursion ouverture 5min (n=160) : bas méd −0.55% (p90 −1.78%) · haut méd +0.15% · range méd 1.05%
- Excursion ouverture 15min (n=160) : bas méd −0.76% (p90 −1.95%) · haut méd +0.37% · range méd 1.29%
- Excursion ouverture 30min (n=160) : bas méd −0.8% (p90 −2.21%) · haut méd +0.48% · range méd 1.41%
- Excursion ouverture 60min (n=160) : bas méd −0.86% (p90 −2.44%) · haut méd +0.58% · range méd 1.59%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 136.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 45% · séance 61% (94/159) · gap 10% · délai 3.0min · rebond 45% (45/94) (MFE +0.74%)
   - −1.0% : fill 30min 27% · séance 53% (77/159) · gap 5% · délai 26.0min · rebond 43% (36/77) (MFE +0.73%)
   - −1.5% : fill 30min 14% · séance 42% (58/159) · gap 1% · délai 47.0min · rebond 36% (25/58) (MFE +0.67%)
   - −2.0% : fill 30min 10% · séance 29% (42/159) · gap 1% · délai 66.4min · rebond 45% (20/42) (MFE +0.78%)
   - −3.0% : fill 30min 4% · séance 16% (24/159) · gap 0% · délai 207.9min · rebond 50% (13/24) (MFE +1.05%)
   - −4.0% : fill 30min 0% · séance 5% (9/159) · gap 0% · délai 350.2min · rebond 11% (3/9) (MFE +0.48%)
   - −5.0% : fill 30min 0% · séance 2% (3/159) · gap 0% · délai 410.2min · rebond 42% (1/3) (MFE +0.73%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.15% (p90 −1.27%) → stop au-delà de −0.86% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.15% (p90 −0.88%) → stop au-delà de −0.6% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.13% (p90 −0.6%) → stop au-delà de −0.44% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=327 jambes) : jambe baissière méd −1.06% (p90 −2.3%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (30 séances) :
      · −1.0% : fill 80% (25/30) · rebond 55% (13/25)
      · −2.0% : fill 50% (16/30) · rebond 44% (7/16)
      · −3.0% : fill 32% (11/30) · rebond 44% (6/11)
      · −4.0% : fill 21% (6/30) · rebond 12% (2/6)
      · −5.0% : fill 12% (3/30) · rebond 42% (1/3)
   - **flat** (36 séances) :
      · −1.0% : fill 55% (21/36) · rebond 37% (9/21)
      · −2.0% : fill 30% (11/36) · rebond 32% (4/11)
      · −3.0% : fill 20% (7/36) · rebond 33% (3/7)
      · −4.0% : fill 6% (2/36) · rebond 0% (0/2)
      · −5.0% : fill 0% (0/36) · rebond 0% (0/0)
   - **gap-up** (93 séances) :
      · −1.0% : fill 45% (31/93) · rebond 42% (14/31)
      · −2.0% : fill 23% (15/93) · rebond 55% (9/15)
      · −3.0% : fill 9% (6/93) · rebond 78% (4/6)
      · −4.0% : fill 0% (1/93) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/93) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 71% si les 15 1res min sont vertes (86 cas) · 15% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **30min** → P(séance verte=clôture>ouverture) 78% si début vert vs 18% si rouge (base 43% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 221min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **78%** · continue >prix actuel 51% ; creux résiduel méd -1.0% (q20 -1.89%) → **SL/trailing à −1.89%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.06% / q75 +1.76% → **scale +1.06% / runner +1.76%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **18%** (continue à baisser 59%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.2%** (au-delà de la MAE q10 -3.2%), cible rebond +0.98% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.85% .. +2.03%] · haut q95 +2.5% · bas q05 -2.59%
   - 60min (n=160) : retour [-2.77% .. +2.4%] · haut q95 +2.64% · bas q05 -3.21%
   - 2h (n=160) : retour [-3.18% .. +2.43%] · haut q95 +2.93% · bas q05 -3.68%
   - 4h (n=160) : retour [-2.91% .. +3.17%] · haut q95 +3.22% · bas q05 -3.77%
   - 6h (n=160) : retour [-3.48% .. +3.64%] · haut q95 +3.9% · bas q05 -4.14%
   - session (n=160) : retour [-3.39% .. +2.81%] · haut q95 +3.91% · bas q05 -4.65%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.93%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-11 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 50.7  _(neutre)_
- **ADX** : 10.9  _(pas de tendance nette)_
- **MACD** : hist 0.033  _(bullish_recent)_
- **BB** : %B 0.84 · largeur 5.5%
- **ATR** : 4.31 (54.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.322  _(distribution)_
- **Vol ratio** : 1.49  _(volume normal)_
- **Choppiness** : 68.5  _(marche en range (choppy))_
- **MA** : MA20 139.64 · MA50 136.83 · MA200 134.49  _(prix > MA20)_
- **Dist MA** : MA20 +1.8% · MA50 +3.9% · MA200 +5.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (760827 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
