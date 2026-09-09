# NEX

**Generated** : 2026-09-09T00:13:14.915418+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · €141.30  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot €141.30 (+2.6% vs entrée) · entrée €137.76 · stop €126.74 · T1 €139.17 · R/R 0.13  
> ↳ P(T1 av. stop) 50 % _(réel 5 s)_ · EV/risk 0.006 _(réel 5 s)_ (GBM -0.074) · ¼-Kelly 0.084 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €137.47–€138.04 (mid €137.76)
- Spot actuel : €141.30 (+2.6% au-dessus de la zone — repli à attendre)
- Stop : €126.74 (stop swing_plan-based (-8.24%))
- Targets : T1 €139.17 · R/R 0.13 | T2 €140.58 · R/R 0.26 | T3 €142.00 · R/R 0.38
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €126.74


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.64 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.24 %)** : le gap seul le franchit 0.234 % des séances (3 fois sur 1280).
   - exécution **0.113 pt plus bas** dans le cas TYPIQUE (médiane), 1.107 au p90, **1.356 au pire**
   - perte réelle **8.739 %** en moyenne _(tirée par la queue)_, jusqu'à **9.596 %** — au lieu des 8.24 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0012 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.516 % | p01 -3.643 % | pire -9.596 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0042** [0.0003 ; 0.0237] _(largeur 2.3 pt, n_eff 173.1)_
   - swing : **0.4412** [0.3895 ; 0.4938] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4106** [0.3597 ; 0.463] _(largeur 10.3 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 14.1 observations effectives », dont la borne haute a 95 % vaut environ 21.3 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (48.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-3.5 %** | CVaR **-5.21 %** | vol 2.3 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.51 % vs -7.83 % si l'on extrapolait par √5 _(rapport 0.959 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0082** (β de hausse 1.1019, asymétrie 0.9149) vs FCHI — 618 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 125.5831 sur grid_snapped (3.78 ATR, 11.123 %) — p(stop avant cible) 0.0904 [0.06 ; 0.12], R/R 1.425, perte reelle 11.123 % (gap inclus), CVaR 11.123 %, EV 0.5756 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.087 %) — p(stop avant cible) 0.5253 [0.47 ; 0.58], R/R 2.364, perte reelle 6.706 % (gap inclus), EV -1.197 % — **REFUSE**
      - refuse : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.525, borne haute 0.578 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.20 %) : P(cible) 5.1 % x 15.85 % + P(rien) 42.4 % x 3.58 % ne couvrent pas P(stop) 52.5 % x 6.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.6 ATR (stop 6.105 %) — p(stop avant cible) 0.3715 [0.32 ; 0.42], R/R 1.951, perte reelle 8.124 % (gap inclus), EV -0.5265 % — **REFUSE**
      - refuse : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 5.1 % x 15.85 % + P(rien) 57.8 % x 2.91 % ne couvrent pas P(stop) 37.1 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 3.78 ATR (stop 12.044 %) — p(stop avant cible) 0.0783 [0.05 ; 0.11], R/R 1.316, perte reelle 12.044 % (gap inclus), EV 0.5591 % — **REFUSE**
      - refuse : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.04 % > budget 12.00 %
   - 🟢 support a 8.72 ATR (stop 25.497 %) — p(stop avant cible) 0.0007 [0.00 ; 0.01], R/R 0.622, perte reelle 25.497 % (gap inclus), EV 0.6635 % — **REFUSE**
      - refuse : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.50 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.681 %) — p(stop avant cible) 0.9127 [0.88 ; 0.94], R/R 9.526, perte reelle 1.664 % (gap inclus), EV -0.828 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 9.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.913, borne haute 0.939 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.83 %) : P(cible) 1.2 % x 15.85 % + P(rien) 7.5 % x 6.66 % ne couvrent pas P(stop) 91.3 % x 1.66 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.362 %) — p(stop avant cible) 0.8273 [0.78 ; 0.86], R/R 5.822, perte reelle 2.723 % (gap inclus), EV -1.1227 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 5.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.827, borne haute 0.864 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.12 %) : P(cible) 1.8 % x 15.85 % + P(rien) 15.4 % x 5.44 % ne couvrent pas P(stop) 82.7 % x 2.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.044 %) — p(stop avant cible) 0.7306 [0.68 ; 0.78], R/R 4.135, perte reelle 3.834 % (gap inclus), EV -1.2437 % — **REFUSE**
      - refuse : cible atteinte seulement 2.7 % du temps (< 15 %) meme a 10 seances : le R/R de 4.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.731, borne haute 0.775 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.24 %) : P(cible) 2.7 % x 15.85 % + P(rien) 24.3 % x 4.67 % ne couvrent pas P(stop) 73.1 % x 3.83 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 2.725 %) — p(stop avant cible) 0.6653 [0.61 ; 0.71], R/R 3.42, perte reelle 4.635 % (gap inclus), EV -1.2078 % — **REFUSE**
      - refuse : cible atteinte seulement 3.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.665, borne haute 0.714 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.21 %) : P(cible) 3.7 % x 15.85 % + P(rien) 29.8 % x 4.35 % ne couvrent pas P(stop) 66.5 % x 4.63 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 3.406 %) — p(stop avant cible) 0.5828 [0.53 ; 0.63], R/R 2.899, perte reelle 5.468 % (gap inclus), EV -1.038 % — **REFUSE**
      - refuse : cible atteinte seulement 4.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.583, borne haute 0.634 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.04 %) : P(cible) 4.4 % x 15.85 % + P(rien) 37.3 % x 3.88 % ne couvrent pas P(stop) 58.3 % x 5.47 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.6 ATR (stop 5.184 %) — p(stop avant cible) 0.4227 [0.37 ; 0.48], R/R 1.951, perte reelle 8.124 % (gap inclus), EV -0.9382 % — **REFUSE**
      - refuse : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.94 %) : P(cible) 5.1 % x 15.85 % + P(rien) 52.6 % x 3.20 % ne couvrent pas P(stop) 42.3 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 6.812 %) — p(stop avant cible) 0.3051 [0.26 ; 0.36], R/R 1.951, perte reelle 8.124 % (gap inclus), EV -0.0554 % — **REFUSE**
      - refuse : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.06 %) : P(cible) 5.1 % x 15.85 % + P(rien) 64.4 % x 2.51 % ne couvrent pas P(stop) 30.5 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 7.493 %) — p(stop avant cible) 0.2532 [0.21 ; 0.30], R/R 1.849, perte reelle 8.571 % (gap inclus), EV 0.1837 % — **REFUSE**
      - refuse : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 8.174 %) — p(stop avant cible) 0.2079 [0.17 ; 0.25], R/R 1.814, perte reelle 8.739 % (gap inclus), EV 0.4326 % — **REFUSE**
      - refuse : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 9.536 %) — p(stop avant cible) 0.152 [0.12 ; 0.19], R/R 1.652, perte reelle 9.596 % (gap inclus), EV 0.5382 % — **REFUSE**
      - refuse : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 3.78 ATR (stop 11.123 %) — p(stop avant cible) 0.0904 [0.06 ; 0.12], R/R 1.425, perte reelle 11.123 % (gap inclus), EV 0.5756 % — **REFUSE**
      - refuse : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 5.0 ATR (stop 13.624 %) — p(stop avant cible) 0.0417 [0.02 ; 0.07], R/R 1.164, perte reelle 13.624 % (gap inclus), EV 0.5696 % — **REFUSE**
      - refuse : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.62 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 14.986 %) — p(stop avant cible) 0.0256 [0.01 ; 0.05], R/R 1.058, perte reelle 14.986 % (gap inclus), EV 0.5904 % — **REFUSE**
      - refuse : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.99 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 16.348 %) — p(stop avant cible) 0.0137 [0.01 ; 0.03], R/R 0.97, perte reelle 16.348 % (gap inclus), EV 0.6103 % — **REFUSE**
      - refuse : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.35 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 17.711 %) — p(stop avant cible) 0.0067 [0.00 ; 0.02], R/R 0.895, perte reelle 17.711 % (gap inclus), EV 0.6302 % — **REFUSE**
      - refuse : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.71 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 19.073 %) — p(stop avant cible) 0.0048 [0.00 ; 0.02], R/R 0.831, perte reelle 19.073 % (gap inclus), EV 0.6479 % — **REFUSE**
      - refuse : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.07 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 20.435 %) — p(stop avant cible) 0.0029 [0.00 ; 0.01], R/R 0.776, perte reelle 20.435 % (gap inclus), EV 0.6551 % — **REFUSE**
      - refuse : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.43 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 21.798 %) — p(stop avant cible) 0.0022 [0.00 ; 0.01], R/R 0.727, perte reelle 21.798 % (gap inclus), EV 0.6579 % — **REFUSE**
      - refuse : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.80 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 141.3, ATR14 3.85 (2.725 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.349 ATR = 0.951 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.136 % | 141.1075 | 87.75 % | 91.46 % | 93.22 % | 95.28 % | 96.93 % | 97.8 % |
| 0.1 ATR | 0.272 % | 140.915 | 82.16 % | 87.93 % | 90.47 % | 93.31 % | 95.55 % | 96.9 % |
| 0.15 ATR | 0.409 % | 140.7225 | 75.39 % | 83.71 % | 87.03 % | 90.35 % | 94.07 % | 95.6 % |
| 0.2 ATR | 0.545 % | 140.53 | 68.73 % | 78.61 % | 83.4 % | 88.48 % | 92.68 % | 94.91 % |
| 0.25 ATR | 0.681 % | 140.3375 | 62.16 % | 73.8 % | 79.27 % | 85.24 % | 90.6 % | 93.71 % |
| 0.35 ATR | 0.954 % | 139.9525 | 49.9 % | 64.57 % | 72.0 % | 79.13 % | 86.65 % | 91.51 % |
| 0.5 ATR | 1.362 % | 139.375 | 34.8 % | 52.8 % | 61.59 % | 70.96 % | 80.32 % | 87.31 % |
| 0.75 ATR | 2.044 % | 138.4125 | 20.49 % | 36.8 % | 47.64 % | 59.15 % | 70.23 % | 80.82 % |
| 1.0 ATR | 2.725 % | 137.45 | 10.69 % | 24.53 % | 35.07 % | 48.92 % | 61.52 % | 74.13 % |
| 1.25 ATR | 3.406 % | 136.4875 | 4.9 % | 16.29 % | 25.15 % | 39.86 % | 54.4 % | 67.73 % |
| 1.5 ATR | 4.087 % | 135.525 | 2.45 % | 10.99 % | 18.47 % | 30.81 % | 46.79 % | 60.14 % |
| 2.0 ATR | 5.449 % | 133.6 | 0.78 % | 5.2 % | 9.92 % | 19.29 % | 35.41 % | 50.95 % |
| 2.5 ATR | 6.812 % | 131.675 | 0.49 % | 2.65 % | 5.6 % | 11.42 % | 24.93 % | 39.16 % |
| 3.0 ATR | 8.174 % | 129.75 | 0.2 % | 1.67 % | 3.24 % | 7.19 % | 17.71 % | 30.67 % |
| 4.0 ATR | 10.899 % | 125.9 | 0.1 % | 0.49 % | 0.88 % | 1.87 % | 7.62 % | 18.08 % |
| 6.0 ATR | 16.348 % | 118.2 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 1.29 % | 4.3 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.67 ATR | 0.76 ATR | 1.03 ATR | 1.25 ATR |
| **2 s.** | 0.24 ATR | 0.54 ATR | 0.62 ATR | 0.83 ATR | 0.99 ATR | 1.14 ATR | 1.58 ATR | 2.04 ATR |
| **3 s.** | 0.31 ATR | 0.71 ATR | 0.80 ATR | 1.05 ATR | 1.26 ATR | 1.44 ATR | 2.00 ATR | 2.63 ATR |
| **5 s.** | 0.43 ATR | 0.97 ATR | 1.11 ATR | 1.44 ATR | 1.75 ATR | 1.97 ATR | 2.67 ATR | 3.41 ATR |
| **10 s.** | 0.63 ATR | 1.40 ATR | 1.58 ATR | 2.12 ATR | 2.50 ATR | 2.84 ATR | 3.76 ATR | 4.83 ATR |
| **20 s.** | 0.97 ATR | 2.04 ATR | 2.25 ATR | 2.86 ATR | 3.45 ATR | 3.85 ATR | 5.17 ATR | 5.90 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.399–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (78.5 % des re-echantillons)
- **2 seance(s)** : plage utile 0.622–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.044 %, prix 138.4118), p(touche) 36.8 % (en stress 88.24 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.803–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.725 %, prix 137.4496), p(touche) 35.07 % (en stress 85.29 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.108–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (3.406 %, prix 136.4873), p(touche) 39.86 % (en stress 94.12 %)  ✅ optimum identifie (64.0 % des re-echantillons)
- **10 seance(s)** : plage utile 1.579–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (5.449 %, prix 133.6006), p(touche) 35.41 % (en stress 98.04 %)  ✅ optimum identifie (73.9 % des re-echantillons)
- **20 seance(s)** : plage utile 2.252–4.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (6.812 %, prix 131.6746), p(touche) 39.16 % (en stress 98.02 %)  ✅ optimum identifie (70.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.074 | EV/share : €-0.818 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 50 % | T2 22 % | T3 9 %
- Kelly (position) : f* 0.336 | ¼-Kelly 0.084 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.6 | bear 79.9 | side 13.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 283.0 (= 2 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.511% → cible +1.026% / stop −8.0%, p_fill 27%, n_eff≈14.1) : P(cible|rempli) **50%** · **EV/risk +0.006** (×p_fill ; si rempli +0.17% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=8, n_eff=6))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=2))
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
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 56.0  _(momentum haussier)_
- **ADX** : 11.6  _(pas de tendance nette)_
- **MACD** : hist -0.132  _(pas de croisement recent)_
- **BB** : %B 0.65 · largeur 6.4%
- **ATR** : 3.85 (36.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.295  _(distribution)_
- **Vol ratio** : 0.31  _(volume atone)_
- **Choppiness** : 64.2  _(marche en range (choppy))_
- **MA** : MA20 139.94 · MA50 136.78 · MA200 134.29  _(prix > MA20)_
- **Dist MA** : MA20 +1.0% · MA50 +3.3% · MA200 +5.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (763256 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
