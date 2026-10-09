# SMCI

**Generated** : 2026-10-09T00:25:24.431730+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 9/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $42.78  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot $42.78 (+2.2% vs entrée) · entrée $41.86 · stop $39.21 · T1 $47.16 · R/R 2.0  
> ↳ ¼-Kelly 0.021 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -4.3 % ≠ (strike 43.0 − spot 42.78)/spot = +0.5 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-08 : 42.78 · ATR Wilder 2.32 (5.42 %)_
- **Swing** : plage **39.92 → 38.19** (-6.69 % a -10.72 % sous la cloture, 0.74 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 39.47-40.13 (A) ; 38.28-39.23 (B). stop INDICATIF 35.64 (-6.68 % sous le bas ; sous le support 36.8-37.85 (- 0,5 ATR)).
- **Deep** : plage **38.19 → 33.15** (-10.72 % a -22.52 % sous la cloture, 2.18 ATR) — touchee 44 % → 15 % du temps en 20 seances ; supports reels dans la plage : 36.8-37.85 (B) ; 35.36-36.37 (A) ; 33.86-34.98 (A) ; 31.03-33.94 (B) ; 32.59-33.64 (B). stop INDICATIF 28.52 (-13.95 % sous le bas ; sous le support 29.68-30.65 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (1.29 ATR sous le plus haut 20 s., RSI(2) 29.8 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 40.74-41.53 (B, -2.92 %) ; 39.47-40.13 (A, -6.19 %) ; 38.28-39.23 (B, -8.3 %) ; 36.8-37.85 (B, -11.52 %) ; 35.36-36.37 (A, -14.98 %) ; 33.86-34.98 (A, -18.23 %)
- Resistances reelles au-dessus : 43.69-44.72 (A, 2.13 %) ; 44.99-45.99 (A, 5.17 %) ; 46.22-47.0 (A, 8.04 %) ; 47.38-48.53 (A, 10.76 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.82 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.35 %)** : le gap seul le franchit 1.596 % des séances (20 fois sur 1253).
   - exécution **3.606 pt plus bas** dans le cas TYPIQUE (médiane), 16.527 au p90, **20.701 au pire**
   - perte réelle **14.137 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 8.35 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0924 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.795 % | p01 -10.307 % | pire -29.051 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4886** [0.4148 ; 0.5627] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4662** [0.4141 ; 0.5189] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4626** [0.4105 ; 0.5153] _(largeur 10.5 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.63 %** | CVaR **-12.34 %** | vol 5.82 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 3.78 % contre 6.48 % aujourd'hui, rapport 0.58)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.69 % vs -16.48 % si l'on extrapolait par √5 _(rapport 1.013 ; < 1 = le √5 surestime)_
- **β de baisse : 1.5186** (β de hausse 1.2187, asymétrie 1.2461) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.776× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 42.2296 sur atr_grid (0.25 ATR, 1.284 %) — p(stop avant cible) 0.9188 [0.89 ; 0.94], R/R 14.636, perte reelle 1.484 % (gap inclus), CVaR 4.965 %, EV 0.1868 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.9434 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 6.4 % du temps (< 15 %) meme a 10 seances : le R/R de 14.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.919, borne haute 0.944 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 4.96 % > budget 3.00 %
- Budget de queue : **3.0 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.114 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 42.1 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
   - ⚠ role de queue **non etabli** pour cette ligne (l'intervalle contient zero) : le budget vient de son NOTIONNEL seul, pas d'une mesure de co-mouvement.
   - ⚠ budget **borne** (brut 2.02 %) : les bornes sont un choix declare, pas une mesure.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.86 ATR (stop 6.844 %) — p(stop avant cible) 0.5454 [0.49 ; 0.60], R/R 2.687, perte reelle 8.086 % (gap inclus), EV 1.0805 % — **REFUSE**
      - refuse : p_stop_first 0.545, borne haute 0.597 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.77 % > budget 3.00 %
   - 🟢 support a 1.51 ATR (stop 10.148 %) — p(stop avant cible) 0.397 [0.35 ; 0.45], R/R 1.851, perte reelle 11.735 % (gap inclus), EV 1.3324 % — **REFUSE**
      - refuse : R/R 1.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.47 % > budget 3.00 %
   - 🟢 support a 8.83 ATR (stop 47.76 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.442, perte reelle 49.133 % (gap inclus), EV 2.1668 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.20 % > budget 3.00 %
   - 🟢 support a 10.61 ATR (stop 56.877 %) — p(stop avant cible) 0.0007 [0.00 ; 0.01], R/R 0.382, perte reelle 56.877 % (gap inclus), EV 2.1643 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.27 % > budget 3.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.284 %) — p(stop avant cible) 0.9188 [0.89 ; 0.94], R/R 14.636, perte reelle 1.484 % (gap inclus), EV 0.1868 % — **REFUSE**
      - refuse : cible atteinte seulement 6.4 % du temps (< 15 %) meme a 10 seances : le R/R de 14.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.919, borne haute 0.944 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 4.96 % > budget 3.00 %
   - ⚪ atr_grid a 0.5 ATR (stop 2.568 %) — p(stop avant cible) 0.8247 [0.78 ; 0.86], R/R 7.431, perte reelle 2.924 % (gap inclus), EV 0.3528 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.825, borne haute 0.862 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 8.36 % > budget 3.00 %
   - ⚪ grid_snapped a 0.86 ATR (stop 5.971 %) — p(stop avant cible) 0.6184 [0.57 ; 0.67], R/R 3.137, perte reelle 6.925 % (gap inclus), EV 0.8058 % — **REFUSE**
      - refuse : p_stop_first 0.618, borne haute 0.668 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 17.19 % > budget 3.00 %
   - 🟢 grid_snapped a 1.51 ATR (stop 9.275 %) — p(stop avant cible) 0.4264 [0.38 ; 0.48], R/R 2.012, perte reelle 10.797 % (gap inclus), EV 1.3861 % — **REFUSE**
      - refuse : R/R 2.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.10 % > budget 3.00 %
   - ⚪ atr_grid a 2.25 ATR (stop 11.554 %) — p(stop avant cible) 0.3297 [0.28 ; 0.38], R/R 1.629, perte reelle 13.336 % (gap inclus), EV 1.6751 % — **REFUSE**
      - refuse : R/R 1.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.04 % > budget 3.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 12.838 %) — p(stop avant cible) 0.2719 [0.23 ; 0.32], R/R 1.472, perte reelle 14.758 % (gap inclus), EV 2.0086 % — **REFUSE**
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.17 % > budget 3.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 14.122 %) — p(stop avant cible) 0.2263 [0.18 ; 0.27], R/R 1.335, perte reelle 16.269 % (gap inclus), EV 2.122 % — **REFUSE**
      - refuse : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.74 % > budget 3.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 15.406 %) — p(stop avant cible) 0.2051 [0.17 ; 0.25], R/R 1.231, perte reelle 17.652 % (gap inclus), EV 2.052 % — **REFUSE**
      - refuse : R/R 1.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.39 % > budget 3.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 17.973 %) — p(stop avant cible) 0.1496 [0.12 ; 0.19], R/R 1.058, perte reelle 20.541 % (gap inclus), EV 2.4574 % — **REFUSE**
      - refuse : R/R 1.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.14 % > budget 3.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 20.541 %) — p(stop avant cible) 0.1291 [0.10 ; 0.17], R/R 0.967, perte reelle 22.456 % (gap inclus), EV 2.4658 % — **REFUSE**
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.47 % > budget 3.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 23.108 %) — p(stop avant cible) 0.1098 [0.08 ; 0.15], R/R 0.874, perte reelle 24.859 % (gap inclus), EV 2.3919 % — **REFUSE**
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.95 % > budget 3.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 25.676 %) — p(stop avant cible) 0.0847 [0.06 ; 0.12], R/R 0.811, perte reelle 26.801 % (gap inclus), EV 2.4182 % — **REFUSE**
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.58 % > budget 3.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 28.244 %) — p(stop avant cible) 0.0789 [0.05 ; 0.11], R/R 0.76, perte reelle 28.604 % (gap inclus), EV 2.2993 % — **REFUSE**
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.81 % > budget 3.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 30.811 %) — p(stop avant cible) 0.0733 [0.05 ; 0.10], R/R 0.703, perte reelle 30.919 % (gap inclus), EV 2.1543 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.97 % > budget 3.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 33.379 %) — p(stop avant cible) 0.0657 [0.04 ; 0.10], R/R 0.647, perte reelle 33.557 % (gap inclus), EV 2.0246 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.61 % > budget 3.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 35.947 %) — p(stop avant cible) 0.0548 [0.03 ; 0.08], R/R 0.603, perte reelle 36.016 % (gap inclus), EV 1.9543 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.02 % > budget 3.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 38.514 %) — p(stop avant cible) 0.0239 [0.01 ; 0.04], R/R 0.564, perte reelle 38.546 % (gap inclus), EV 2.1382 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.78 % > budget 3.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 41.082 %) — p(stop avant cible) 0.0117 [0.00 ; 0.03], R/R 0.529, perte reelle 41.082 % (gap inclus), EV 2.1589 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.37 % > budget 3.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 42.7788, ATR14 2.1968 (5.135 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.342 ATR = 1.756 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.257 % | 42.669 | 90.53 % | 93.35 % | 94.75 % | 95.25 % | 96.44 % | 97.64 % |
| 0.1 ATR | 0.514 % | 42.5591 | 82.07 % | 87.3 % | 89.3 % | 91.2 % | 92.99 % | 94.97 % |
| 0.15 ATR | 0.77 % | 42.4493 | 74.92 % | 82.16 % | 85.07 % | 88.27 % | 90.65 % | 93.63 % |
| 0.2 ATR | 1.027 % | 42.3394 | 68.08 % | 77.42 % | 80.63 % | 85.74 % | 89.13 % | 92.3 % |
| 0.25 ATR | 1.284 % | 42.2296 | 61.83 % | 72.68 % | 76.29 % | 82.31 % | 86.99 % | 90.55 % |
| 0.35 ATR | 1.797 % | 42.0099 | 49.04 % | 63.31 % | 69.53 % | 77.05 % | 82.62 % | 87.99 % |
| 0.5 ATR | 2.568 % | 41.6804 | 34.64 % | 49.7 % | 58.32 % | 68.66 % | 76.83 % | 83.47 % |
| 0.75 ATR | 3.851 % | 41.1312 | 17.02 % | 33.06 % | 42.79 % | 55.01 % | 66.16 % | 75.26 % |
| 1.0 ATR | 5.135 % | 40.582 | 7.75 % | 21.17 % | 30.17 % | 43.38 % | 56.81 % | 68.58 % |
| 1.25 ATR | 6.419 % | 40.0328 | 3.73 % | 14.72 % | 22.0 % | 32.76 % | 47.56 % | 60.99 % |
| 1.5 ATR | 7.703 % | 39.4836 | 1.51 % | 9.38 % | 16.04 % | 25.68 % | 41.36 % | 54.62 % |
| 2.0 ATR | 10.27 % | 38.3852 | 0.3 % | 3.53 % | 8.17 % | 15.87 % | 29.57 % | 43.43 % |
| 2.5 ATR | 12.838 % | 37.2868 | 0.2 % | 1.51 % | 4.24 % | 9.5 % | 19.31 % | 31.52 % |
| 3.0 ATR | 15.406 % | 36.1884 | 0.2 % | 1.21 % | 2.62 % | 5.46 % | 13.82 % | 23.72 % |
| 4.0 ATR | 20.541 % | 33.9917 | 0.0 % | 0.6 % | 1.51 % | 2.63 % | 7.42 % | 14.17 % |
| 6.0 ATR | 30.811 % | 29.5981 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.54 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.34 ATR | 0.39 ATR | 0.52 ATR | 0.64 ATR | 0.71 ATR | 0.94 ATR | 1.17 ATR |
| **2 s.** | 0.23 ATR | 0.50 ATR | 0.57 ATR | 0.75 ATR | 0.92 ATR | 1.04 ATR | 1.47 ATR | 1.87 ATR |
| **3 s.** | 0.27 ATR | 0.63 ATR | 0.71 ATR | 0.94 ATR | 1.16 ATR | 1.33 ATR | 1.88 ATR | 2.40 ATR |
| **5 s.** | 0.39 ATR | 0.86 ATR | 0.96 ATR | 1.24 ATR | 1.53 ATR | 1.79 ATR | 2.46 ATR | 3.16 ATR |
| **10 s.** | 0.54 ATR | 1.18 ATR | 1.35 ATR | 1.85 ATR | 2.22 ATR | 2.47 ATR | 3.60 ATR | 4.90 ATR |
| **20 s.** | 0.76 ATR | 1.71 ATR | 1.93 ATR | 2.44 ATR | 2.92 ATR | 3.39 ATR | 4.97 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.392–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.571–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.851 %, prix 41.1314), p(touche) 33.06 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.714–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.851 %, prix 41.1314), p(touche) 42.79 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 17.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.965–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (6.419 %, prix 40.0328), p(touche) 32.76 % (en stress 89.9 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.353–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.703 %, prix 39.4835), p(touche) 41.36 % (en stress 95.96 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.93–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (15.406 %, prix 36.1883), p(touche) 23.72 % (en stress 96.94 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.136 | EV/share : $0.361 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 22 % | T2 14 % | T3 11 %
- Kelly (position) : f* 0.084 | ¼-Kelly 0.021 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 78.5 | bear 5.0 | side 16.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 611.0 (= 16 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.98% → cible +2.593% / stop −2.0%, p_fill 80%, n_eff≈84.8) : P(cible|rempli) **34%** · **EV/risk -0.081** (×p_fill ; si rempli -0.20% du capital)
  - **swing** (entrée dip −2.152% → cible +12.669% / stop −6.335%, p_fill 68%, n_eff≈79.2) : P(cible|rempli) **25%** · **EV/risk +0.138** (×p_fill ; si rempli +1.29% du capital)
  - **deep** (entrée dip −3.327% → cible +14.039% / stop −7.968%, p_fill 65%, n_eff≈72.7) : P(cible|rempli) **35%** · **EV/risk +0.160** (×p_fill ; si rempli +1.94% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→77% · +2.0%→62% · +3.0%→43% · +5.0%→22% · +8.0%→9%
- Range intraday médian 5.66% (p90 9.37%) · excursion haute méd. +2.56% / basse méd. −2.37%
- Profil de vol intra : ouverture 3.84% vs midi 1.155% vs clôture 1.48% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓0% ; spike-down 69% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; neutre — autocorr -0.011)_ ; drift intra méd. 0.304% ; recovery-V 40%
- **σ réalisé intraday** 3.371% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 61% / bas 61% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 43.4066 (VA 43.1796–43.8039 ; dernier close 43.68)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 23% · rebond 78% · **stop −4.35%** sous le fill (sous le bruit) · cible +2.23% · R/R 0.51 (high win-rate)
- Gaps overnight (n=159) : méd. 0.21% · baisse 42% (gap-down >1% 31% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.93% (p90 −2.5%) · haut méd +1.02% · range méd 2.13%
- Excursion ouverture 15min (n=160) : bas méd −1.13% (p90 −3.1%) · haut méd +1.28% · range méd 2.8%
- Excursion ouverture 30min (n=160) : bas méd −1.36% (p90 −3.6%) · haut méd +1.53% · range méd 3.54%
- Excursion ouverture 60min (n=160) : bas méd −1.66% (p90 −4.07%) · haut méd +1.81% · range méd 4.18%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 43.69 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 71% (116/159) · gap 37% · délai 0.0min · rebond 57% (69/116) (MFE +1.39%)
   - −1.0% : fill 30min 51% · séance 67% (109/159) · gap 31% · délai 0.0min · rebond 58% (64/109) (MFE +1.64%)
   - −1.5% : fill 30min 45% · séance 61% (99/159) · gap 20% · délai 0.2min · rebond 69% (65/99) (MFE +1.56%)
   - −2.0% : fill 30min 39% · séance 53% (86/159) · gap 16% · délai 1.1min · rebond 72% (57/86) (MFE +1.74%)
   - −3.0% : fill 30min 26% · séance 44% (72/159) · gap 8% · délai 12.8min · rebond 64% (44/72) (MFE +1.42%)
   - −4.0% : fill 30min 13% · séance 31% (52/159) · gap 4% · délai 41.3min · rebond 72% (34/52) (MFE +1.7%)
   - −5.0% : fill 30min 10% · séance 23% (41/159) · gap 3% · délai 49.2min · rebond 78% (30/41) (MFE +2.23%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.62% (p90 −2.8%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.66% (p90 −2.62%) → stop au-delà de −1.86% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.65% (p90 −2.32%) → stop au-delà de −1.68% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=870 jambes) : jambe baissière méd −1.18% (p90 −2.77%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (71 séances) :
      · −1.0% : fill 98% (69/71) · rebond 48% (36/69)
      · −2.0% : fill 94% (65/71) · rebond 74% (41/65)
      · −3.0% : fill 85% (58/71) · rebond 65% (35/58)
      · −4.0% : fill 62% (43/71) · rebond 71% (28/43)
      · −5.0% : fill 46% (34/71) · rebond 76% (24/34)
   - **flat** (13 séances) :
      · −1.0% : fill 85% (12/13) · rebond 75% (9/12)
      · −2.0% : fill 36% (5/13) · rebond 50% (3/5)
      · −3.0% : fill 29% (3/13) · rebond 43% (2/3)
      · −4.0% : fill 10% (1/13) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/13) · rebond 0% (0/0)
   - **gap-up** (75 séances) :
      · −1.0% : fill 38% (28/75) · rebond 74% (19/28)
      · −2.0% : fill 21% (16/75) · rebond 70% (13/16)
      · −3.0% : fill 11% (11/75) · rebond 70% (7/11)
      · −4.0% : fill 8% (8/75) · rebond 72% (5/8)
      · −5.0% : fill 8% (7/75) · rebond 86% (6/7)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 68% si les 15 1res min sont vertes (80 cas) · 27% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **39min** → P(séance verte=clôture>ouverture) 78% si début vert vs 18% si rouge (base 48% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 213min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **78%** · continue >prix actuel 54% ; creux résiduel méd -1.96% (q20 -3.57%) → **SL/trailing à −3.57%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.91% / q75 +4.23% → **scale +1.91% / runner +4.23%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **18%** (continue à baisser 53%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.85%** (au-delà de la MAE q10 -4.85%), cible rebond +1.68% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.7% .. +4.13%] · haut q95 +5.15% · bas q05 -4.15%
   - 60min (n=160) : retour [-4.08% .. +5.23%] · haut q95 +6.49% · bas q05 -5.23%
   - 2h (n=160) : retour [-4.2% .. +6.08%] · haut q95 +7.25% · bas q05 -5.52%
   - 4h (n=160) : retour [-4.43% .. +6.66%] · haut q95 +7.77% · bas q05 -5.98%
   - 6h (n=160) : retour [-4.87% .. +6.53%] · haut q95 +8.68% · bas q05 -6.54%
   - session (n=160) : retour [-4.8% .. +6.89%] · haut q95 +8.93% · bas q05 -6.91%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — SMCI = **volatil sans tendance propre (choppy)** (vol intra méd 3.54%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.5 · part idiosyncratique 0.5
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 63.5  _(momentum haussier)_
- **ADX** : 29.6  _(tendance etablie)_
- **MACD** : hist 0.052  _(pas de croisement recent)_
- **BB** : %B 0.67 · largeur 23.7%
- **ATR** : 2.2 (46.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.103  _(accumulation)_
- **Vol ratio** : 0.93  _(volume normal)_
- **Choppiness** : 62.4  _(marche en range (choppy))_
- **MA** : MA20 41.08 · MA50 37.72 · MA200 32.27  _(prix > MA20)_
- **Dist MA** : MA20 +4.1% · MA50 +13.4% · MA200 +32.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (859946 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
