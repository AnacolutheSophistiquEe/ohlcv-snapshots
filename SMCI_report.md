# SMCI

**Generated** : 2026-10-01T22:04:26.405584+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 8/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $41.92  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $41.92 (+0.5% vs entrée) · entrée $41.72 · stop $40.67 · T1 $42.87 · R/R 1.1  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $41.52–$41.91 (mid $41.72)
- Spot actuel : $41.92 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : $40.67 (plancher anti-bruit 5 s — stop EV-optimal −2.5% (first-passage 5 s réel) ; -2.52 % depuis l'entree)
- Targets : T1 $42.87 · R/R 1.1 | T2 $44.03 · R/R 2.2 | T3 $45.19 · R/R 3.3
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $40.67


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.82 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.84 %)** : le gap seul le franchit 1.596 % des séances (20 fois sur 1253).
   - exécution **4.116 pt plus bas** dans le cas TYPIQUE (médiane), 17.037 au p90, **21.211 au pire**
   - perte réelle **14.137 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 7.84 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.1005 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.795 % | p01 -10.307 % | pire -29.051 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4429** [0.3704 ; 0.5173] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4351** [0.3836 ; 0.4877] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.4491** [0.3973 ; 0.5018] _(largeur 10.5 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.63 %** | CVaR **-12.34 %** | vol 5.83 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 3.64 % contre 6.47 % aujourd'hui, rapport 0.56)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.69 % vs -16.48 % si l'on extrapolait par √5 _(rapport 1.013 ; < 1 = le √5 surestime)_
- **β de baisse : 1.5297** (β de hausse 1.2172, asymétrie 1.2567) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.832× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 40.1761 sur grid_snapped (0.45 ATR, 4.16 %) — p(stop avant cible) 0.7201 [0.67 ; 0.77], R/R 5.155, perte reelle 4.818 % (gap inclus), CVaR 13.033 %, EV 0.9795 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 3.6981 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 5.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.720, borne haute 0.765 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 13.03 % > budget 3.09 %
- Budget de queue : **3.09 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.206 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 43.2 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.45 ATR (stop 5.1 %) — p(stop avant cible) 0.6874 [0.64 ; 0.73], R/R 4.252, perte reelle 5.84 % (gap inclus), EV 0.8004 % — **REFUSE**
      - refuse : cible atteinte seulement 14.3 % du temps (< 15 %) meme a 10 seances : le R/R de 4.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.687, borne haute 0.735 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 14.76 % > budget 3.09 %
   - 🔴 support a 1.06 ATR (stop 8.443 %) — p(stop avant cible) 0.4579 [0.41 ; 0.51], R/R 2.484, perte reelle 9.998 % (gap inclus), EV 1.7004 % — **REFUSE**
      - refuse : R/R 2.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.27 % > budget 3.09 %
      - ⚠ support DETECTE a 0.35 ATR du spot — compartiment <1, mesure a 46.7 % de casse (IC clusterise [0.436 ; 0.499] sur 1172 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 8.0 ATR (stop 46.826 %) — p(stop avant cible) 0.0022 [0.00 ; 0.01], R/R 0.524, perte reelle 47.353 % (gap inclus), EV 2.2801 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.38 % > budget 3.09 %
   - 🟢 support a 9.68 ATR (stop 56.129 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 0.442, perte reelle 56.229 % (gap inclus), EV 2.2725 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.52 % > budget 3.09 %
   - ⚪ grid_snapped a 0.45 ATR (stop 4.16 %) — p(stop avant cible) 0.7201 [0.67 ; 0.77], R/R 5.155, perte reelle 4.818 % (gap inclus), EV 0.9795 % — **REFUSE**
      - refuse : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 5.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.720, borne haute 0.765 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 13.03 % > budget 3.09 %
   - 🔴 grid_snapped a 1.06 ATR (stop 7.503 %) — p(stop avant cible) 0.5339 [0.48 ; 0.59], R/R 2.833, perte reelle 8.768 % (gap inclus), EV 1.2511 % — **REFUSE**
      - refuse : p_stop_first 0.534, borne haute 0.586 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.37 % > budget 3.09 %
   - ⚪ atr_grid a 1.75 ATR (stop 9.676 %) — p(stop avant cible) 0.4205 [0.37 ; 0.47], R/R 2.207, perte reelle 11.253 % (gap inclus), EV 1.5769 % — **REFUSE**
      - refuse : R/R 2.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.65 % > budget 3.09 %
   - ⚪ atr_grid a 2.0 ATR (stop 11.058 %) — p(stop avant cible) 0.3539 [0.30 ; 0.41], R/R 1.945, perte reelle 12.768 % (gap inclus), EV 1.8493 % — **REFUSE**
      - refuse : R/R 1.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.82 % > budget 3.09 %
   - ⚪ atr_grid a 2.25 ATR (stop 12.441 %) — p(stop avant cible) 0.2945 [0.25 ; 0.34], R/R 1.733, perte reelle 14.335 % (gap inclus), EV 2.0961 % — **REFUSE**
      - refuse : R/R 1.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.38 % > budget 3.09 %
   - ⚪ atr_grid a 2.5 ATR (stop 13.823 %) — p(stop avant cible) 0.2425 [0.20 ; 0.29], R/R 1.556, perte reelle 15.96 % (gap inclus), EV 2.2307 % — **REFUSE**
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.97 % > budget 3.09 %
   - ⚪ atr_grid a 2.75 ATR (stop 15.205 %) — p(stop avant cible) 0.2158 [0.17 ; 0.26], R/R 1.431, perte reelle 17.355 % (gap inclus), EV 2.1383 % — **REFUSE**
      - refuse : R/R 1.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.32 % > budget 3.09 %
   - ⚪ atr_grid a 3.0 ATR (stop 16.588 %) — p(stop avant cible) 0.1866 [0.15 ; 0.23], R/R 1.305, perte reelle 19.026 % (gap inclus), EV 2.3789 % — **REFUSE**
      - refuse : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.00 % > budget 3.09 %
   - ⚪ atr_grid a 3.5 ATR (stop 19.352 %) — p(stop avant cible) 0.1385 [0.11 ; 0.18], R/R 1.147, perte reelle 21.654 % (gap inclus), EV 2.632 % — **REFUSE**
      - refuse : R/R 1.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.46 % > budget 3.09 %
   - ⚪ atr_grid a 4.0 ATR (stop 22.117 %) — p(stop avant cible) 0.1214 [0.09 ; 0.16], R/R 1.04, perte reelle 23.872 % (gap inclus), EV 2.5028 % — **REFUSE**
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.38 % > budget 3.09 %
   - ⚪ atr_grid a 4.5 ATR (stop 24.882 %) — p(stop avant cible) 0.0947 [0.07 ; 0.13], R/R 0.948, perte reelle 26.185 % (gap inclus), EV 2.5591 % — **REFUSE**
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.35 % > budget 3.09 %
   - ⚪ atr_grid a 5.0 ATR (stop 27.646 %) — p(stop avant cible) 0.0814 [0.06 ; 0.11], R/R 0.882, perte reelle 28.148 % (gap inclus), EV 2.4527 % — **REFUSE**
      - refuse : R/R 0.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.46 % > budget 3.09 %
   - ⚪ atr_grid a 5.5 ATR (stop 30.411 %) — p(stop avant cible) 0.0761 [0.05 ; 0.11], R/R 0.813, perte reelle 30.55 % (gap inclus), EV 2.2889 % — **REFUSE**
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.62 % > budget 3.09 %
   - ⚪ atr_grid a 6.0 ATR (stop 33.175 %) — p(stop avant cible) 0.0677 [0.04 ; 0.10], R/R 0.744, perte reelle 33.367 % (gap inclus), EV 2.1448 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.43 % > budget 3.09 %
   - ⚪ atr_grid a 6.5 ATR (stop 35.94 %) — p(stop avant cible) 0.0564 [0.04 ; 0.08], R/R 0.69, perte reelle 36.009 % (gap inclus), EV 2.0608 % — **REFUSE**
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.02 % > budget 3.09 %
   - ⚪ atr_grid a 7.0 ATR (stop 38.705 %) — p(stop avant cible) 0.0246 [0.01 ; 0.05], R/R 0.641, perte reelle 38.73 % (gap inclus), EV 2.2449 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.06 % > budget 3.09 %
   - ⚪ atr_grid a 7.5 ATR (stop 41.469 %) — p(stop avant cible) 0.0083 [0.00 ; 0.02], R/R 0.599, perte reelle 41.469 % (gap inclus), EV 2.2832 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.29 % > budget 3.09 %
   - 🟢 grid_snapped a 8.0 ATR (stop 45.886 %) — p(stop avant cible) 0.0022 [0.00 ; 0.01], R/R 0.54, perte reelle 46.019 % (gap inclus), EV 2.283 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.32 % > budget 3.09 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 41.92, ATR14 2.3179 (5.529 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.343 ATR = 1.897 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.276 % | 41.8041 | 90.43 % | 93.25 % | 94.65 % | 95.15 % | 96.34 % | 97.54 % |
| 0.1 ATR | 0.553 % | 41.6882 | 82.07 % | 87.2 % | 89.2 % | 91.1 % | 92.89 % | 94.87 % |
| 0.15 ATR | 0.829 % | 41.5723 | 74.92 % | 82.06 % | 84.96 % | 88.17 % | 90.55 % | 93.53 % |
| 0.2 ATR | 1.106 % | 41.4564 | 67.98 % | 77.32 % | 80.52 % | 85.64 % | 89.02 % | 92.2 % |
| 0.25 ATR | 1.382 % | 41.3405 | 61.83 % | 72.68 % | 76.29 % | 82.2 % | 86.99 % | 90.45 % |
| 0.35 ATR | 1.935 % | 41.1087 | 49.14 % | 63.31 % | 69.53 % | 76.95 % | 82.62 % | 87.78 % |
| 0.5 ATR | 2.765 % | 40.7611 | 34.94 % | 49.8 % | 58.32 % | 68.55 % | 76.83 % | 83.26 % |
| 0.75 ATR | 4.147 % | 40.1816 | 17.32 % | 33.27 % | 42.89 % | 54.9 % | 66.26 % | 75.15 % |
| 1.0 ATR | 5.529 % | 39.6021 | 7.96 % | 21.37 % | 30.27 % | 43.38 % | 56.91 % | 68.38 % |
| 1.25 ATR | 6.912 % | 39.0227 | 3.73 % | 14.72 % | 22.0 % | 32.76 % | 47.56 % | 60.68 % |
| 1.5 ATR | 8.294 % | 38.4432 | 1.51 % | 9.38 % | 16.04 % | 25.68 % | 41.36 % | 54.41 % |
| 2.0 ATR | 11.058 % | 37.2843 | 0.3 % | 3.53 % | 8.17 % | 15.87 % | 29.57 % | 43.33 % |
| 2.5 ATR | 13.823 % | 36.1254 | 0.2 % | 1.51 % | 4.24 % | 9.5 % | 19.31 % | 31.52 % |
| 3.0 ATR | 16.588 % | 34.9664 | 0.2 % | 1.21 % | 2.62 % | 5.46 % | 13.82 % | 23.72 % |
| 4.0 ATR | 22.117 % | 32.6486 | 0.0 % | 0.6 % | 1.51 % | 2.63 % | 7.42 % | 14.17 % |
| 6.0 ATR | 33.175 % | 28.0129 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.54 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.34 ATR | 0.39 ATR | 0.53 ATR | 0.64 ATR | 0.71 ATR | 0.95 ATR | 1.18 ATR |
| **2 s.** | 0.23 ATR | 0.50 ATR | 0.57 ATR | 0.76 ATR | 0.92 ATR | 1.05 ATR | 1.47 ATR | 1.87 ATR |
| **3 s.** | 0.27 ATR | 0.64 ATR | 0.72 ATR | 0.95 ATR | 1.16 ATR | 1.33 ATR | 1.88 ATR | 2.40 ATR |
| **5 s.** | 0.39 ATR | 0.86 ATR | 0.96 ATR | 1.24 ATR | 1.53 ATR | 1.79 ATR | 2.46 ATR | 3.16 ATR |
| **10 s.** | 0.54 ATR | 1.19 ATR | 1.35 ATR | 1.85 ATR | 2.22 ATR | 2.47 ATR | 3.60 ATR | 4.90 ATR |
| **20 s.** | 0.76 ATR | 1.70 ATR | 1.93 ATR | 2.44 ATR | 2.92 ATR | 3.39 ATR | 4.97 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.394–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.573–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.147 %, prix 40.1816), p(touche) 33.27 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.716–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.147 %, prix 40.1816), p(touche) 42.89 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 16.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.965–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (6.912 %, prix 39.0225), p(touche) 32.76 % (en stress 89.9 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.353–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.294 %, prix 38.4432), p(touche) 41.36 % (en stress 95.96 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.925–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (16.588 %, prix 34.9663), p(touche) 23.72 % (en stress 96.94 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.005 | EV/share : $-0.006 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 42 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.0 | bear 5.9 | side 9.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 596.0 (= 16 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.482% → cible +2.778% / stop −2.5%, p_fill 90%, n_eff≈95.9) : P(cible|rempli) **36%** · **EV/risk -0.124** (×p_fill ; si rempli -0.35% du capital)
  - **swing** (entrée dip −1.068% → cible +13.69% / stop −6.845%, p_fill 84%, n_eff≈96.2) : P(cible|rempli) **25%** · **EV/risk +0.119** (×p_fill ; si rempli +0.97% du capital)
  - **deep** (entrée dip −1.656% → cible +14.366% / stop −8.434%, p_fill 83%, n_eff≈91.8) : P(cible|rempli) **40%** · **EV/risk +0.197** (×p_fill ; si rempli +2.01% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→77% · +2.0%→61% · +3.0%→43% · +5.0%→22% · +8.0%→9%
- Range intraday médian 5.81% (p90 9.37%) · excursion haute méd. +2.54% / basse méd. −2.39%
- Profil de vol intra : ouverture 3.828% vs midi 1.162% vs clôture 1.484% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 70% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.132 ; neutre — autocorr -0.021)_ ; drift intra méd. 0.108% ; recovery-V 33%
- **σ réalisé intraday** 3.422% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 57% / bas 62% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 40.6075 (VA 40.4975–40.7725 ; dernier close 41.05)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 24% · rebond 77% · **stop −4.35%** sous le fill (sous le bruit) · cible +2.21% · R/R 0.51 (high win-rate)
- Gaps overnight (n=159) : méd. 0.21% · baisse 42% (gap-down >1% 32% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.93% (p90 −2.6%) · haut méd +1.04% · range méd 2.17%
- Excursion ouverture 15min (n=160) : bas méd −1.13% (p90 −3.11%) · haut méd +1.34% · range méd 2.85%
- Excursion ouverture 30min (n=160) : bas méd −1.39% (p90 −3.62%) · haut méd +1.52% · range méd 3.54%
- Excursion ouverture 60min (n=160) : bas méd −1.67% (p90 −4.08%) · haut méd +1.8% · range méd 4.18%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 41.07 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 71% (117/159) · gap 38% · délai 0.0min · rebond 56% (69/117) (MFE +1.36%)
   - −1.0% : fill 30min 51% · séance 68% (109/159) · gap 32% · délai 0.0min · rebond 57% (64/109) (MFE +1.53%)
   - −1.5% : fill 30min 47% · séance 62% (99/159) · gap 20% · délai 0.2min · rebond 68% (65/99) (MFE +1.41%)
   - −2.0% : fill 30min 40% · séance 53% (86/159) · gap 16% · délai 0.7min · rebond 70% (56/86) (MFE +1.7%)
   - −3.0% : fill 30min 27% · séance 45% (73/159) · gap 8% · délai 12.9min · rebond 64% (44/73) (MFE +1.41%)
   - −4.0% : fill 30min 13% · séance 32% (53/159) · gap 4% · délai 41.3min · rebond 72% (35/53) (MFE +1.7%)
   - −5.0% : fill 30min 10% · séance 24% (42/159) · gap 3% · délai 50.4min · rebond 77% (30/42) (MFE +2.21%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.59% (p90 −2.8%) → stop au-delà de −1.94% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.59% (p90 −2.77%) → stop au-delà de −1.76% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.62% (p90 −2.36%) → stop au-delà de −1.85% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=876 jambes) : jambe baissière méd −1.19% (p90 −2.77%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 97% (68/70) · rebond 45% (35/68)
      · −2.0% : fill 94% (64/70) · rebond 73% (40/64)
      · −3.0% : fill 88% (58/70) · rebond 65% (35/58)
      · −4.0% : fill 64% (43/70) · rebond 71% (28/43)
      · −5.0% : fill 48% (34/70) · rebond 76% (24/34)
   - **flat** (13 séances) :
      · −1.0% : fill 85% (12/13) · rebond 75% (9/12)
      · −2.0% : fill 36% (5/13) · rebond 50% (3/5)
      · −3.0% : fill 29% (3/13) · rebond 43% (2/3)
      · −4.0% : fill 10% (1/13) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/13) · rebond 0% (0/0)
   - **gap-up** (76 séances) :
      · −1.0% : fill 39% (29/76) · rebond 74% (20/29)
      · −2.0% : fill 22% (17/76) · rebond 69% (13/17)
      · −3.0% : fill 12% (12/76) · rebond 68% (7/12)
      · −4.0% : fill 9% (9/76) · rebond 73% (6/9)
      · −5.0% : fill 8% (8/76) · rebond 84% (6/8)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 65% si les 15 1res min sont vertes (78 cas) · 27% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:46** → P(séance verte=clôture>ouverture) 82% si début vert vs 12% si rouge (base 46% · écart 70 pts) ; prédictivité sature ensuite (plafond brut 213min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=84) : tient le vert **82%** · continue >prix actuel 52% ; creux résiduel méd -1.47% (q20 -3.22%) → **SL/trailing à −3.22%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.54% / q75 +2.67% → **scale +1.54% / runner +2.67%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **12%** (continue à baisser 51%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.21%** (au-delà de la MAE q10 -3.21%), cible rebond +1.84% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.83% .. +4.13%] · haut q95 +5.17% · bas q05 -4.18%
   - 60min (n=160) : retour [-4.11% .. +5.36%] · haut q95 +6.57% · bas q05 -5.27%
   - 2h (n=160) : retour [-4.22% .. +6.1%] · haut q95 +7.33% · bas q05 -5.62%
   - 4h (n=160) : retour [-4.57% .. +6.71%] · haut q95 +7.82% · bas q05 -6.17%
   - 6h (n=160) : retour [-5.05% .. +6.6%] · haut q95 +8.71% · bas q05 -6.58%
   - session (n=160) : retour [-4.94% .. +6.92%] · haut q95 +9.01% · bas q05 -6.91%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — SMCI = **volatil sans tendance propre (choppy)** (vol intra méd 3.55%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.51 · part idiosyncratique 0.49
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 55.1  _(momentum haussier)_
- **ADX** : 26.3  _(tendance etablie)_
- **MACD** : hist -0.011  _(bearish_recent)_
- **BB** : %B 0.75 · largeur 20.7%
- **ATR** : 2.32 (60.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.051  _(accumulation)_
- **Vol ratio** : 0.69  _(volume normal)_
- **Choppiness** : 51.2  _(transition)_
- **MA** : MA20 39.88 · MA50 36.27 · MA200 31.94  _(prix > MA20)_
- **Dist MA** : MA20 +5.1% · MA50 +15.6% · MA200 +31.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (844533 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
