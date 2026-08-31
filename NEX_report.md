# NEX

**Generated** : 2026-08-31T21:43:41.564728+00:00  
**Santé technique** : 6/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · €139.50  

> 🟡 **WAIT-FOR-DIP** — spot +5.5 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €139.50 (+5.5% vs entrée) · entrée €132.18 · stop €128.40 · T1 €135.53 · R/R 0.89  
> ↳ P(T1 av. stop) 70 % · EV/risk 0.15 · ¼-Kelly 0.009 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.230 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €131.51–€132.85 (mid €132.18)
- Spot actuel : €139.50 (+5.5% au-dessus de la zone — repli à attendre)
- Stop : €128.40 (stop swing_plan-based (-7.96%))
- Targets : T1 €135.53 · R/R 0.89 | T2 €138.88 · R/R 1.77 | T3 €142.23 · R/R 2.66
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €128.40


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.64 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (7.96 %)** : le gap seul le franchit 0.312 % des séances (4 fois sur 1280).
   - exécution **0.35 pt plus bas** dans le cas TYPIQUE (médiane), 1.263 au p90, **1.636 au pire**
   - perte réelle **8.571 %** en moyenne _(tirée par la queue)_, jusqu'à **9.596 %** — au lieu des 7.96 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0019 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.516 % | p01 -3.643 % | pire -9.596 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0045** [0.0004 ; 0.0243] _(largeur 2.4 pt, n_eff 173.1)_
   - swing : **0.4597** [0.4077 ; 0.5124] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4365** [0.3849 ; 0.4891] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 15.5 observations effectives », dont la borne haute a 95 % vaut environ 19.4 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (45.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-3.51 %** | CVaR **-5.25 %** | vol 2.3 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.51 % vs -7.85 % si l'on extrapolait par √5 _(rapport 0.956 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0148** (β de hausse 1.098, asymétrie 0.9243) vs FCHI — 618 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 124.6746 sur grid_snapped (3.62 ATR, 10.628 %) — p(stop avant cible) 0.1078 [0.08 ; 0.14], R/R 1.634, perte reelle 10.628 % (gap inclus), CVaR 10.628 %, EV 0.6602 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 3.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 1.05 ATR (stop 4.255 %) — p(stop avant cible) 0.5282 [0.48 ; 0.58], R/R 2.589, perte reelle 6.706 % (gap inclus), EV -1.0277 % — **REFUSE**
      - refuse : cible atteinte seulement 3.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.528, borne haute 0.580 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.03 %) : P(cible) 3.8 % x 17.36 % + P(rien) 43.4 % x 4.27 % ne couvrent pas P(stop) 52.8 % x 6.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 3.62 ATR (stop 11.234 %) — p(stop avant cible) 0.0935 [0.07 ; 0.13], R/R 1.546, perte reelle 11.234 % (gap inclus), EV 0.6416 % — **REFUSE**
      - refuse : cible atteinte seulement 3.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 8.41 ATR (stop 24.194 %) — p(stop avant cible) 0.0007 [0.00 ; 0.01], R/R 0.718, perte reelle 24.194 % (gap inclus), EV 0.7436 % — **REFUSE**
      - refuse : cible atteinte seulement 3.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.19 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.677 %) — p(stop avant cible) 0.91 [0.88 ; 0.94], R/R 10.466, perte reelle 1.659 % (gap inclus), EV -0.7846 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 10.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.910, borne haute 0.937 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.78 %) : P(cible) 1.1 % x 17.36 % + P(rien) 7.9 % x 6.75 % ne couvrent pas P(stop) 91.0 % x 1.66 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.354 %) — p(stop avant cible) 0.8384 [0.80 ; 0.87], R/R 6.414, perte reelle 2.707 % (gap inclus), EV -1.0932 % — **REFUSE**
      - refuse : cible atteinte seulement 1.6 % du temps (< 15 %) meme a 10 seances : le R/R de 6.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.838, borne haute 0.874 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.09 %) : P(cible) 1.6 % x 17.36 % + P(rien) 14.6 % x 6.18 % ne couvrent pas P(stop) 83.8 % x 2.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.031 %) — p(stop avant cible) 0.7499 [0.70 ; 0.79], R/R 4.581, perte reelle 3.79 % (gap inclus), EV -1.2192 % — **REFUSE**
      - refuse : cible atteinte seulement 2.4 % du temps (< 15 %) meme a 10 seances : le R/R de 4.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.750, borne haute 0.793 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.22 %) : P(cible) 2.4 % x 17.36 % + P(rien) 22.7 % x 5.36 % ne couvrent pas P(stop) 75.0 % x 3.79 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.05 ATR (stop 3.648 %) — p(stop avant cible) 0.5808 [0.53 ; 0.63], R/R 2.866, perte reelle 6.058 % (gap inclus), EV -1.1774 % — **REFUSE**
      - refuse : cible atteinte seulement 3.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.581, borne haute 0.632 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.18 %) : P(cible) 3.8 % x 17.36 % + P(rien) 38.1 % x 4.41 % ne couvrent pas P(stop) 58.1 % x 6.06 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 4.74 %) — p(stop avant cible) 0.4743 [0.42 ; 0.53], R/R 2.256, perte reelle 7.697 % (gap inclus), EV -1.0685 % — **REFUSE**
      - refuse : cible atteinte seulement 3.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.07 %) : P(cible) 3.8 % x 17.36 % + P(rien) 48.8 % x 3.94 % ne couvrent pas P(stop) 47.4 % x 7.70 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 5.417 %) — p(stop avant cible) 0.4292 [0.38 ; 0.48], R/R 2.137, perte reelle 8.124 % (gap inclus), EV -0.8401 % — **REFUSE**
      - refuse : cible atteinte seulement 3.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.84 %) : P(cible) 3.8 % x 17.36 % + P(rien) 53.3 % x 3.73 % ne couvrent pas P(stop) 42.9 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 6.094 %) — p(stop avant cible) 0.3868 [0.34 ; 0.44], R/R 2.137, perte reelle 8.124 % (gap inclus), EV -0.502 % — **REFUSE**
      - refuse : cible atteinte seulement 3.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.50 %) : P(cible) 3.8 % x 17.36 % + P(rien) 57.5 % x 3.44 % ne couvrent pas P(stop) 38.7 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 6.772 %) — p(stop avant cible) 0.3159 [0.27 ; 0.37], R/R 2.137, perte reelle 8.124 % (gap inclus), EV -0.0022 % — **REFUSE**
      - refuse : cible atteinte seulement 3.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.00 %) : P(cible) 3.8 % x 17.36 % + P(rien) 64.6 % x 2.95 % ne couvrent pas P(stop) 31.6 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 7.449 %) — p(stop avant cible) 0.2637 [0.22 ; 0.31], R/R 2.026, perte reelle 8.571 % (gap inclus), EV 0.2389 % — **REFUSE**
      - refuse : cible atteinte seulement 3.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 8.126 %) — p(stop avant cible) 0.2152 [0.17 ; 0.26], R/R 1.987, perte reelle 8.739 % (gap inclus), EV 0.5034 % — **REFUSE**
      - refuse : cible atteinte seulement 3.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 3.62 ATR (stop 10.628 %) — p(stop avant cible) 0.1078 [0.08 ; 0.14], R/R 1.634, perte reelle 10.628 % (gap inclus), EV 0.6602 % — **REFUSE**
      - refuse : cible atteinte seulement 3.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.5 ATR (stop 12.189 %) — p(stop avant cible) 0.0769 [0.05 ; 0.11], R/R 1.424, perte reelle 12.189 % (gap inclus), EV 0.631 % — **REFUSE**
      - refuse : cible atteinte seulement 3.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.19 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 13.543 %) — p(stop avant cible) 0.0448 [0.03 ; 0.07], R/R 1.282, perte reelle 13.543 % (gap inclus), EV 0.6377 % — **REFUSE**
      - refuse : cible atteinte seulement 3.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.54 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 14.898 %) — p(stop avant cible) 0.0265 [0.01 ; 0.05], R/R 1.165, perte reelle 14.898 % (gap inclus), EV 0.6688 % — **REFUSE**
      - refuse : cible atteinte seulement 3.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.90 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 16.252 %) — p(stop avant cible) 0.0142 [0.01 ; 0.03], R/R 1.068, perte reelle 16.252 % (gap inclus), EV 0.6881 % — **REFUSE**
      - refuse : cible atteinte seulement 3.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.25 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 17.606 %) — p(stop avant cible) 0.0097 [0.00 ; 0.02], R/R 0.986, perte reelle 17.606 % (gap inclus), EV 0.7 % — **REFUSE**
      - refuse : cible atteinte seulement 3.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.61 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 18.961 %) — p(stop avant cible) 0.0049 [0.00 ; 0.02], R/R 0.916, perte reelle 18.961 % (gap inclus), EV 0.7278 % — **REFUSE**
      - refuse : cible atteinte seulement 3.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.96 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 20.315 %) — p(stop avant cible) 0.003 [0.00 ; 0.01], R/R 0.855, perte reelle 20.315 % (gap inclus), EV 0.7338 % — **REFUSE**
      - refuse : cible atteinte seulement 3.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.32 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 21.669 %) — p(stop avant cible) 0.0022 [0.00 ; 0.01], R/R 0.801, perte reelle 21.669 % (gap inclus), EV 0.7383 % — **REFUSE**
      - refuse : cible atteinte seulement 3.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.67 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 139.5, ATR14 3.7786 (2.709 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.349 ATR = 0.945 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.135 % | 139.3111 | 87.84 % | 91.46 % | 93.22 % | 95.37 % | 96.93 % | 97.8 % |
| 0.1 ATR | 0.271 % | 139.1221 | 82.06 % | 87.73 % | 90.28 % | 93.21 % | 95.45 % | 97.0 % |
| 0.15 ATR | 0.406 % | 138.9332 | 75.39 % | 83.51 % | 86.84 % | 90.26 % | 93.97 % | 95.7 % |
| 0.2 ATR | 0.542 % | 138.7443 | 68.73 % | 78.41 % | 83.2 % | 88.29 % | 92.48 % | 95.0 % |
| 0.25 ATR | 0.677 % | 138.5554 | 62.16 % | 73.6 % | 79.08 % | 85.04 % | 90.41 % | 93.81 % |
| 0.35 ATR | 0.948 % | 138.1775 | 49.9 % | 64.38 % | 71.81 % | 78.94 % | 86.45 % | 91.61 % |
| 0.5 ATR | 1.354 % | 137.6107 | 34.61 % | 52.6 % | 61.39 % | 70.67 % | 80.22 % | 87.61 % |
| 0.75 ATR | 2.031 % | 136.6661 | 20.2 % | 36.51 % | 47.54 % | 58.86 % | 70.33 % | 81.12 % |
| 1.0 ATR | 2.709 % | 135.7214 | 10.69 % | 24.44 % | 34.87 % | 48.52 % | 61.42 % | 74.53 % |
| 1.25 ATR | 3.386 % | 134.7768 | 4.9 % | 16.19 % | 24.95 % | 39.47 % | 54.4 % | 67.93 % |
| 1.5 ATR | 4.063 % | 133.8321 | 2.45 % | 10.89 % | 18.27 % | 30.51 % | 46.79 % | 60.54 % |
| 2.0 ATR | 5.417 % | 131.9429 | 0.78 % | 5.2 % | 9.92 % | 19.29 % | 35.41 % | 51.05 % |
| 2.5 ATR | 6.772 % | 130.0536 | 0.49 % | 2.65 % | 5.6 % | 11.42 % | 24.93 % | 39.26 % |
| 3.0 ATR | 8.126 % | 128.1643 | 0.2 % | 1.67 % | 3.24 % | 7.19 % | 17.71 % | 30.67 % |
| 4.0 ATR | 10.835 % | 124.3857 | 0.1 % | 0.49 % | 0.88 % | 1.87 % | 7.62 % | 18.08 % |
| 6.0 ATR | 16.252 % | 116.8286 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 1.29 % | 4.3 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.67 ATR | 0.76 ATR | 1.03 ATR | 1.25 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.62 ATR | 0.82 ATR | 0.99 ATR | 1.14 ATR | 1.58 ATR | 2.04 ATR |
| **3 s.** | 0.31 ATR | 0.71 ATR | 0.80 ATR | 1.05 ATR | 1.25 ATR | 1.44 ATR | 2.00 ATR | 2.63 ATR |
| **5 s.** | 0.42 ATR | 0.96 ATR | 1.10 ATR | 1.43 ATR | 1.75 ATR | 1.97 ATR | 2.67 ATR | 3.41 ATR |
| **10 s.** | 0.63 ATR | 1.40 ATR | 1.58 ATR | 2.12 ATR | 2.50 ATR | 2.84 ATR | 3.76 ATR | 4.83 ATR |
| **20 s.** | 0.98 ATR | 2.04 ATR | 2.26 ATR | 2.86 ATR | 3.45 ATR | 3.85 ATR | 5.17 ATR | 5.90 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.398–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (78.9 % des re-echantillons)
- **2 seance(s)** : plage utile 0.618–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.031 %, prix 136.6668), p(touche) 36.51 % (en stress 88.24 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.8–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.709 %, prix 135.7209), p(touche) 34.87 % (en stress 85.29 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.097–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (3.386 %, prix 134.7765), p(touche) 39.47 % (en stress 94.12 %)  ✅ optimum identifie (63.2 % des re-echantillons)
- **10 seance(s)** : plage utile 1.579–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (5.417 %, prix 131.9433), p(touche) 35.41 % (en stress 98.04 %)  ✅ optimum identifie (72.6 % des re-echantillons)
- **20 seance(s)** : plage utile 2.257–4.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (6.772 %, prix 130.0531), p(touche) 39.26 % (en stress 98.02 %)  ✅ optimum identifie (69.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.031 | EV/share : €0.116 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 27 % | T3 10 %
- Kelly (position) : f* 0.034 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 10.6 | bear 16.3 | side 73.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 279.0 (= 2 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.391% → cible +1.134% / stop −8.0%, p_fill 30%, n_eff≈15.5) : P(cible|rempli) **38%** · **EV/risk -0.003** (×p_fill ; si rempli -0.07% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=9, n_eff=7))
  - **deep** : indisponible (échantillon insuffisant (n=6, n_eff=5))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→62% · +1.0%→50% · +2.0%→24% · +3.0%→10% · +5.0%→1% · +8.0%→0%
- Range intraday médian 2.95% (p90 4.72%) · excursion haute méd. +1.0% / basse méd. −1.4%
- Profil de vol intra : ouverture 1.746% vs midi 0.516% vs clôture 0.715% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 46% · recovery-V 18%)_
- **Régime intraday** : **chop** _(efficiency 0.108 ; neutre — autocorr -0.028)_ ; drift intra méd. -0.364% ; recovery-V 15%
- **σ réalisé intraday** 2.0% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 63% / bas 64% / whipsaw 27%
- POC intraday (dernière séance, temps-au-prix) : 144.9706 (VA 144.0119–145.4131 ; dernier close 143.5)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 17% · rebond 50% · **stop −1.94%** sous le fill (sous le bruit) · cible +1.05% · R/R 0.54 (high win-rate)
- Gaps overnight (n=159) : méd. 0.36% · baisse 34% (gap-down >1% 5% · >2% 1%)
- Excursion ouverture 5min (n=160) : bas méd −0.49% (p90 −1.86%) · haut méd +0.24% · range méd 1.04%
- Excursion ouverture 15min (n=160) : bas méd −0.61% (p90 −1.97%) · haut méd +0.42% · range méd 1.29%
- Excursion ouverture 30min (n=160) : bas méd −0.74% (p90 −2.26%) · haut méd +0.55% · range méd 1.41%
- Excursion ouverture 60min (n=160) : bas méd −0.84% (p90 −2.5%) · haut méd +0.58% · range méd 1.58%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 142.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 44% · séance 59% (91/159) · gap 11% · délai 3.0min · rebond 44% (44/91) (MFE +0.74%)
   - −1.0% : fill 30min 27% · séance 52% (75/159) · gap 5% · délai 23.2min · rebond 44% (36/75) (MFE +0.83%)
   - −1.5% : fill 30min 16% · séance 40% (56/159) · gap 1% · délai 41.2min · rebond 42% (26/56) (MFE +0.74%)
   - −2.0% : fill 30min 11% · séance 28% (40/159) · gap 1% · délai 57.0min · rebond 51% (20/40) (MFE +1.02%)
   - −3.0% : fill 30min 4% · séance 17% (24/159) · gap 0% · délai 207.9min · rebond 50% (13/24) (MFE +1.05%)
   - −4.0% : fill 30min 0% · séance 6% (9/159) · gap 0% · délai 350.2min · rebond 11% (3/9) (MFE +0.48%)
   - −5.0% : fill 30min 0% · séance 2% (3/159) · gap 0% · délai 410.2min · rebond 42% (1/3) (MFE +0.73%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.15% (p90 −0.99%) → stop au-delà de −0.81% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.15% (p90 −0.9%) → stop au-delà de −0.6% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.13% (p90 −0.6%) → stop au-delà de −0.44% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=324 jambes) : jambe baissière méd −1.09% (p90 −2.39%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (30 séances) :
      · −1.0% : fill 80% (25/30) · rebond 55% (13/25)
      · −2.0% : fill 50% (16/30) · rebond 44% (7/16)
      · −3.0% : fill 32% (11/30) · rebond 44% (6/11)
      · −4.0% : fill 21% (6/30) · rebond 12% (2/6)
      · −5.0% : fill 12% (3/30) · rebond 42% (1/3)
   - **flat** (35 séances) :
      · −1.0% : fill 58% (21/35) · rebond 37% (9/21)
      · −2.0% : fill 32% (11/35) · rebond 32% (4/11)
      · −3.0% : fill 21% (7/35) · rebond 33% (3/7)
      · −4.0% : fill 7% (2/35) · rebond 0% (0/2)
      · −5.0% : fill 0% (0/35) · rebond 0% (0/0)
   - **gap-up** (94 séances) :
      · −1.0% : fill 40% (29/94) · rebond 45% (14/29)
      · −2.0% : fill 18% (13/94) · rebond 76% (9/13)
      · −3.0% : fill 10% (6/94) · rebond 78% (4/6)
      · −4.0% : fill 0% (1/94) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/94) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 70% si les 15 1res min sont vertes (85 cas) · 18% si rouges (75 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **29min** → P(séance verte=clôture>ouverture) 75% si début vert vs 21% si rouge (base 45% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 249min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **75%** · continue >prix actuel 50% ; creux résiduel méd -0.94% (q20 -1.96%) → **SL/trailing à −1.96%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.18% / q75 +1.67% → **scale +1.18% / runner +1.67%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **21%** (continue à baisser 56%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.14%** (au-delà de la MAE q10 -3.14%), cible rebond +1.07% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.95% .. +2.23%] · haut q95 +2.55% · bas q05 -2.59%
   - 60min (n=160) : retour [-2.81% .. +2.54%] · haut q95 +2.74% · bas q05 -3.24%
   - 2h (n=160) : retour [-3.45% .. +2.49%] · haut q95 +2.93% · bas q05 -3.73%
   - 4h (n=160) : retour [-2.92% .. +3.24%] · haut q95 +3.34% · bas q05 -3.82%
   - 6h (n=160) : retour [-3.72% .. +3.69%] · haut q95 +3.99% · bas q05 -4.15%
   - session (n=160) : retour [-3.45% .. +2.85%] · haut q95 +4.02% · bas q05 -4.66%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.93%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 51.1  _(neutre)_
- **ADX** : 12.9  _(pas de tendance nette)_
- **MACD** : hist 0.247  _(pas de croisement recent)_
- **BB** : %B 0.47 · largeur 7.3%
- **ATR** : 3.78 (31.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.231  _(distribution)_
- **Vol ratio** : 0.93  _(volume normal)_
- **Choppiness** : 65.1  _(marche en range (choppy))_
- **MA** : MA20 139.81 · MA50 137.68 · MA200 133.72  _(prix < MA20)_
- **Dist MA** : MA20 -0.2% · MA50 +1.3% · MA200 +4.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (791985 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
