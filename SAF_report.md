# SAF

**Generated** : 2026-09-09T21:48:00.873464+00:00  
**Santé technique** : 4/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €322.80  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot €322.80 (+5.2% vs entrée) · entrée €306.92 · stop €299.66 · T1 €312.10 · R/R 0.71  
> ↳ P(T1 av. stop) 73 % · EV/risk 0.102 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €305.89–€307.96 (mid €306.92)
- Spot actuel : €322.80 (+5.2% au-dessus de la zone — repli à attendre)
- Stop : €299.66 (stop swing_plan-based (-7.17%))
- Targets : T1 €312.10 · R/R 0.71 | T2 €317.27 · R/R 1.43 | T3 €322.45 · R/R 2.14
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €299.66


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.62 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (7.17 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1279).
   - exécution **2.816 pt plus bas** dans le cas TYPIQUE (médiane), 2.816 au p90, **2.816 au pire**
   - perte réelle **9.986 %** en moyenne _(tirée par la queue)_, jusqu'à **9.986 %** — au lieu des 7.17 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0022 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.405 % | p01 -2.356 % | pire -9.986 % _(sur 1279 séances)_
- **P(stop avant cible)** _(source : daily, 1280 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1777** [0.1263 ; 0.2397] _(largeur 11.3 pt, n_eff 173.1)_
   - swing : **0.3757** [0.3259 ; 0.4276] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.3274** [0.2795 ; 0.3781] _(largeur 9.9 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-3.21 %** | CVaR **-4.01 %** | vol 2.07 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 1.30 % contre 2.46 % aujourd'hui, rapport 0.53)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.66 % vs -6.14 % si l'on extrapolait par √5 _(rapport 0.921 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3721** (β de hausse 1.3371, asymétrie 1.0262) vs FCHI — 619 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.259× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 288.5601 sur sr_based (4.07 ATR, 10.607 %) — p(stop avant cible) 0.07 [0.05 ; 0.10], R/R 1.129, perte reelle 10.607 % (gap inclus), CVaR 10.607 %, EV 1.0979 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 3.376 %) — p(stop avant cible) 0.4503 [0.40 ; 0.50], R/R 2.102, perte reelle 5.698 % (gap inclus), EV 0.0019 % — **REFUSE**
      - refuse : cible atteinte seulement 8.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 4.07 ATR (stop 10.607 %) — p(stop avant cible) 0.07 [0.05 ; 0.10], R/R 1.129, perte reelle 10.607 % (gap inclus), EV 1.0979 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 8.69 ATR (stop 20.993 %) — p(stop avant cible) 0.0051 [0.00 ; 0.02], R/R 0.571, perte reelle 20.993 % (gap inclus), EV 1.0536 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.99 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.563 %) — p(stop avant cible) 0.8949 [0.86 ; 0.92], R/R 9.194, perte reelle 1.303 % (gap inclus), EV -0.4091 % — **REFUSE**
      - refuse : cible atteinte seulement 3.6 % du temps (< 15 %) meme a 10 seances : le R/R de 9.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.895, borne haute 0.924 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.41 %) : P(cible) 3.6 % x 11.98 % + P(rien) 6.9 % x 4.74 % ne couvrent pas P(stop) 89.5 % x 1.30 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.125 %) — p(stop avant cible) 0.7825 [0.74 ; 0.82], R/R 6.153, perte reelle 1.947 % (gap inclus), EV -0.19 % — **REFUSE**
      - refuse : cible atteinte seulement 5.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.782, borne haute 0.824 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.19 %) : P(cible) 5.0 % x 11.98 % + P(rien) 16.8 % x 4.39 % ne couvrent pas P(stop) 78.2 % x 1.95 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 1.688 %) — p(stop avant cible) 0.69 [0.64 ; 0.74], R/R 4.447, perte reelle 2.694 % (gap inclus), EV 0.0027 % — **REFUSE**
      - refuse : cible atteinte seulement 6.9 % du temps (< 15 %) meme a 10 seances : le R/R de 4.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.690, borne haute 0.737 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 2.25 %) — p(stop avant cible) 0.6102 [0.56 ; 0.66], R/R 3.267, perte reelle 3.667 % (gap inclus), EV -0.0796 % — **REFUSE**
      - refuse : cible atteinte seulement 7.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.610, borne haute 0.660 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.08 %) : P(cible) 7.4 % x 11.98 % + P(rien) 31.6 % x 4.02 % ne couvrent pas P(stop) 61.0 % x 3.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 2.813 %) — p(stop avant cible) 0.5221 [0.47 ; 0.57], R/R 2.708, perte reelle 4.424 % (gap inclus), EV 0.1208 % — **REFUSE**
      - refuse : cible atteinte seulement 7.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.522, borne haute 0.574 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.75 ATR (stop 3.938 %) — p(stop avant cible) 0.3807 [0.33 ; 0.43], R/R 1.944, perte reelle 6.163 % (gap inclus), EV 0.3222 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 4.501 %) — p(stop avant cible) 0.331 [0.28 ; 0.38], R/R 1.762, perte reelle 6.799 % (gap inclus), EV 0.4055 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 5.063 %) — p(stop avant cible) 0.2824 [0.24 ; 0.33], R/R 1.559, perte reelle 7.683 % (gap inclus), EV 0.5614 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 5.626 %) — p(stop avant cible) 0.251 [0.21 ; 0.30], R/R 1.2, perte reelle 9.986 % (gap inclus), EV 0.2163 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 6.189 %) — p(stop avant cible) 0.226 [0.18 ; 0.27], R/R 1.2, perte reelle 9.986 % (gap inclus), EV 0.4382 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 6.751 %) — p(stop avant cible) 0.1859 [0.15 ; 0.23], R/R 1.2, perte reelle 9.986 % (gap inclus), EV 0.6393 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 7.876 %) — p(stop avant cible) 0.1364 [0.10 ; 0.18], R/R 1.2, perte reelle 9.986 % (gap inclus), EV 0.9123 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 4.07 ATR (stop 9.842 %) — p(stop avant cible) 0.0846 [0.06 ; 0.12], R/R 1.2, perte reelle 9.986 % (gap inclus), EV 1.0879 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.5 ATR (stop 10.127 %) — p(stop avant cible) 0.0814 [0.06 ; 0.11], R/R 1.183, perte reelle 10.127 % (gap inclus), EV 1.0846 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 5.0 ATR (stop 11.252 %) — p(stop avant cible) 0.0609 [0.04 ; 0.09], R/R 1.065, perte reelle 11.252 % (gap inclus), EV 1.0736 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 5.5 ATR (stop 12.377 %) — p(stop avant cible) 0.0426 [0.03 ; 0.07], R/R 0.968, perte reelle 12.377 % (gap inclus), EV 1.085 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.38 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 13.502 %) — p(stop avant cible) 0.0331 [0.02 ; 0.06], R/R 0.887, perte reelle 13.502 % (gap inclus), EV 1.0487 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.50 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 14.628 %) — p(stop avant cible) 0.0194 [0.01 ; 0.04], R/R 0.819, perte reelle 14.628 % (gap inclus), EV 1.0487 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.63 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 15.753 %) — p(stop avant cible) 0.0096 [0.00 ; 0.02], R/R 0.76, perte reelle 15.753 % (gap inclus), EV 1.0559 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.75 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 16.878 %) — p(stop avant cible) 0.0066 [0.00 ; 0.02], R/R 0.71, perte reelle 16.878 % (gap inclus), EV 1.0622 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.88 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 18.003 %) — p(stop avant cible) 0.0059 [0.00 ; 0.02], R/R 0.665, perte reelle 18.003 % (gap inclus), EV 1.0611 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.00 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 322.8, ATR14 7.2643 (2.25 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.346 ATR = 0.779 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.113 % | 322.4368 | 89.21 % | 92.53 % | 93.71 % | 95.67 % | 96.34 % | 97.1 % |
| 0.1 ATR | 0.225 % | 322.0736 | 81.45 % | 87.23 % | 89.18 % | 91.43 % | 93.47 % | 94.8 % |
| 0.15 ATR | 0.338 % | 321.7103 | 75.17 % | 83.3 % | 86.23 % | 88.67 % | 91.29 % | 92.7 % |
| 0.2 ATR | 0.45 % | 321.3471 | 68.4 % | 78.19 % | 82.6 % | 85.32 % | 88.91 % | 90.9 % |
| 0.25 ATR | 0.563 % | 320.9839 | 61.33 % | 73.48 % | 78.96 % | 83.25 % | 87.62 % | 90.0 % |
| 0.35 ATR | 0.788 % | 320.2575 | 49.56 % | 63.36 % | 69.81 % | 76.95 % | 82.67 % | 87.0 % |
| 0.5 ATR | 1.125 % | 319.1678 | 35.53 % | 51.77 % | 59.29 % | 68.67 % | 75.84 % | 81.3 % |
| 0.75 ATR | 1.688 % | 317.3518 | 20.51 % | 35.66 % | 43.17 % | 53.4 % | 63.17 % | 70.7 % |
| 1.0 ATR | 2.25 % | 315.5357 | 9.72 % | 23.77 % | 32.74 % | 42.27 % | 53.47 % | 61.2 % |
| 1.25 ATR | 2.813 % | 313.7196 | 4.32 % | 15.52 % | 24.19 % | 33.5 % | 46.14 % | 54.4 % |
| 1.5 ATR | 3.376 % | 311.9036 | 2.26 % | 10.12 % | 16.72 % | 25.42 % | 38.02 % | 46.4 % |
| 2.0 ATR | 4.501 % | 308.2714 | 0.98 % | 4.42 % | 7.57 % | 15.76 % | 27.03 % | 36.7 % |
| 2.5 ATR | 5.626 % | 304.6393 | 0.2 % | 1.47 % | 3.64 % | 9.16 % | 18.61 % | 27.9 % |
| 3.0 ATR | 6.751 % | 301.0071 | 0.0 % | 0.88 % | 2.06 % | 5.81 % | 12.48 % | 21.6 % |
| 4.0 ATR | 9.002 % | 293.7428 | 0.0 % | 0.2 % | 0.59 % | 1.08 % | 5.05 % | 10.7 % |
| 6.0 ATR | 13.502 % | 279.2143 | 0.0 % | 0.1 % | 0.2 % | 0.39 % | 1.09 % | 3.1 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.54 ATR | 0.68 ATR | 0.76 ATR | 0.99 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.53 ATR | 0.60 ATR | 0.81 ATR | 0.97 ATR | 1.11 ATR | 1.51 ATR | 1.95 ATR |
| **3 s.** | 0.29 ATR | 0.64 ATR | 0.72 ATR | 0.99 ATR | 1.23 ATR | 1.39 ATR | 1.87 ATR | 2.33 ATR |
| **5 s.** | 0.39 ATR | 0.83 ATR | 0.94 ATR | 1.26 ATR | 1.52 ATR | 1.78 ATR | 2.44 ATR | 3.17 ATR |
| **10 s.** | 0.52 ATR | 1.12 ATR | 1.28 ATR | 1.73 ATR | 2.12 ATR | 2.42 ATR | 3.33 ATR | 4.03 ATR |
| **20 s.** | 0.65 ATR | 1.39 ATR | 1.57 ATR | 2.21 ATR | 2.73 ATR | 3.15 ATR | 4.18 ATR | 5.50 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.399–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 20.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.605–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.688 %, prix 317.3511), p(touche) 35.66 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.722–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.688 %, prix 317.3511), p(touche) 43.17 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.939–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.25 %, prix 315.537), p(touche) 42.27 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.285–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (3.376 %, prix 311.9023), p(touche) 38.02 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.572–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (4.501 %, prix 308.2708), p(touche) 36.7 % (en stress 99.0 %)  ✅ optimum identifie (60.4 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.044 | EV/share : €-0.322 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 55 % | T2 33 % | T3 20 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 46.0 | bear 47.8 | side 6.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=13, n_eff=7))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→52% · +2.0%→28% · +3.0%→9% · +5.0%→0% · +8.0%→0%
- Range intraday médian 2.45% (p90 3.72%) · excursion haute méd. +1.09% / basse méd. −0.77%
- Profil de vol intra : ouverture 1.461% vs midi 0.5% vs clôture 0.665% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 41% · recovery-V 16%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; mean-reverting — autocorr -0.075)_ ; drift intra méd. -0.3% ; recovery-V 12%
- **σ réalisé intraday** 1.544% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 65% / bas 61% / whipsaw 30%
- POC intraday (dernière séance, temps-au-prix) : 331.8075 (VA 331.3325–332.7575 ; dernier close 333.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 23% · rebond 36% · **stop −1.2%** sous le fill (sous le bruit) · cible +0.74% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. 0.29% · baisse 31% (gap-down >1% 1% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.41% (p90 −1.56%) · haut méd +0.18% · range méd 0.85%
- Excursion ouverture 15min (n=160) : bas méd −0.48% (p90 −1.76%) · haut méd +0.31% · range méd 1.02%
- Excursion ouverture 30min (n=160) : bas méd −0.49% (p90 −1.78%) · haut méd +0.44% · range méd 1.22%
- Excursion ouverture 60min (n=160) : bas méd −0.65% (p90 −1.84%) · haut méd +0.53% · range méd 1.4%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 333.5 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 46% · séance 60% (86/159) · gap 10% · délai 0.4min · rebond 38% (34/86) (MFE +0.84%)
   - −1.0% : fill 30min 25% · séance 48% (71/159) · gap 1% · délai 25.1min · rebond 42% (33/71) (MFE +0.79%)
   - −1.5% : fill 30min 11% · séance 29% (45/159) · gap 1% · délai 67.5min · rebond 31% (19/45) (MFE +0.52%)
   - −2.0% : fill 30min 4% · séance 23% (37/159) · gap 0% · délai 240.5min · rebond 36% (16/37) (MFE +0.74%)
   - −3.0% : fill 30min 1% · séance 7% (14/159) · gap 0% · délai 316.1min · rebond 43% (7/14) (MFE +0.58%)
   - −4.0% : fill 30min 0% · séance 2% (4/159) · gap 0% · délai 280.9min · rebond 72% (3/4) (MFE +1.17%)
   - −5.0% : fill 30min 0% · séance 0% (1/159) · gap 0% · délai 457.9min · rebond 0% (0/1) (MFE +0.86%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.18% (p90 −0.77%) → stop au-delà de −0.68% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −0.77%) → stop au-delà de −0.61% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=205 jambes) : jambe baissière méd −1.05% (p90 −2.26%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (22 séances) :
      · −1.0% : fill 76% (18/22) · rebond 29% (7/18)
      · −2.0% : fill 48% (12/22) · rebond 42% (6/12)
      · −3.0% : fill 16% (5/22) · rebond 31% (2/5)
      · −4.0% : fill 7% (2/22) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/22) · rebond 0% (0/0)
   - **flat** (38 séances) :
      · −1.0% : fill 49% (20/38) · rebond 40% (10/20)
      · −2.0% : fill 26% (9/38) · rebond 12% (1/9)
      · −3.0% : fill 5% (3/38) · rebond 82% (2/3)
      · −4.0% : fill 0% (0/38) · rebond 0% (0/0)
      · −5.0% : fill 0% (0/38) · rebond 0% (0/0)
   - **gap-up** (99 séances) :
      · −1.0% : fill 39% (33/99) · rebond 53% (16/33)
      · −2.0% : fill 13% (16/99) · rebond 59% (9/16)
      · −3.0% : fill 5% (6/99) · rebond 26% (3/6)
      · −4.0% : fill 2% (2/99) · rebond 38% (1/2)
      · −5.0% : fill 1% (1/99) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 70% si les 15 1res min sont vertes (73 cas) · 27% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **37min** → P(séance verte=clôture>ouverture) 77% si début vert vs 22% si rouge (base 48% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **77%** · continue >prix actuel 50% ; creux résiduel méd -0.71% (q20 -1.34%) → **SL/trailing à −1.34%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.96% / q75 +1.45% → **scale +0.96% / runner +1.45%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **22%** (continue à baisser 60%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.29%** (au-delà de la MAE q10 -2.29%), cible rebond +0.8% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.49% .. +1.54%] · haut q95 +1.94% · bas q05 -2.06%
   - 60min (n=160) : retour [-1.63% .. +1.81%] · haut q95 +1.99% · bas q05 -2.34%
   - 2h (n=160) : retour [-2.32% .. +2.06%] · haut q95 +2.49% · bas q05 -2.92%
   - 4h (n=160) : retour [-1.87% .. +2.1%] · haut q95 +2.7% · bas q05 -2.94%
   - 6h (n=160) : retour [-2.06% .. +2.31%] · haut q95 +2.78% · bas q05 -2.98%
   - session (n=160) : retour [-2.7% .. +2.39%] · haut q95 +3.33% · bas q05 -3.76%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.68%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : stretched_down
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

- **RSI** : 27.7  _(survente)_
- **ADX** : 19.1  _(pas de tendance nette)_
- **MACD** : hist -2.63  _(pas de croisement recent)_
- **BB** : %B 0.05 · largeur 13.5%
- **ATR** : 7.26 (40.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.351  _(distribution)_
- **Vol ratio** : 1.54  _(volume au-dessus de la moyenne)_
- **Choppiness** : 42.4  _(transition)_
- **MA** : MA20 343.64 · MA50 342.34 · MA200 311.64  _(prix < MA20)_
- **Dist MA** : MA20 -6.1% · MA50 -5.7% · MA200 +3.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (762106 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
