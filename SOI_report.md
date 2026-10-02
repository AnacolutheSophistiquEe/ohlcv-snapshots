# SOI

**Generated** : 2026-10-02T00:11:43.523814+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 6.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 9/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €160.10  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)  
> ↳ spot €160.10 (+2.6% vs entrée) · entrée €156.02 · stop €144.53 · T1 €178.99 · R/R 2.0  
> ↳ ¼-Kelly 0.044 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : triple_bullish (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €153.71–€158.33 (mid €156.02)
- Spot actuel : €160.10 (+2.6% au-dessus de la zone — repli à attendre)
- Stop : €144.53 (R/R 2 (resserré, parité Claude) ; -7.36 % depuis l'entree)
- Targets : T1 €178.99 · R/R 2.0 | T2 €190.32 · R/R 2.99 | T3 €201.65 · R/R 3.97
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €144.53


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.91 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.72 %)** : le gap seul le franchit 0.234 % des séances (3 fois sur 1280).
   - exécution **8.999 pt plus bas** dans le cas TYPIQUE (médiane), 17.459 au p90, **19.574 au pire**
   - perte réelle **21.456 %** en moyenne _(tirée par la queue)_, jusqu'à **29.294 %** — au lieu des 9.72 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0275 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.675 % | p01 -5.132 % | pire -29.294 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4708** [0.3974 ; 0.5451] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4037** [0.353 ; 0.456] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.4375** [0.3859 ; 0.4901] _(largeur 10.4 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.65 %** | CVaR **-14.04 %** | vol 6.66 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 4.01 % contre 7.41 % aujourd'hui, rapport 0.54)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.4 % vs -11.44 % si l'on extrapolait par √5 _(rapport 1.084 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1123** (β de hausse 1.575, asymétrie 0.7062) vs FCHI — 619 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.056× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 146.8976 sur sr_based (0.83 ATR, 8.246 %) — p(stop avant cible) 0.5328 [0.48 ; 0.58], R/R 3.011, perte reelle 8.619 % (gap inclus), CVaR 12.092 %, EV 1.9238 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.0712 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.533, borne haute 0.585 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 12.09 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.83 ATR (stop 8.246 %) — p(stop avant cible) 0.5328 [0.48 ; 0.58], R/R 3.011, perte reelle 8.619 % (gap inclus), EV 1.9238 % — **REFUSE**
      - refuse : p_stop_first 0.533, borne haute 0.585 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 12.09 % > budget 12.00 %
   - 🔴 support a 1.12 ATR (stop 10.065 %) — p(stop avant cible) 0.4485 [0.40 ; 0.50], R/R 2.47, perte reelle 10.507 % (gap inclus), EV 2.1696 % — **REFUSE**
      - refuse : R/R 2.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.90 % > budget 12.00 %
      - ⚠ support DETECTE a 0.73 ATR du spot — compartiment <1, mesure a 46.7 % de casse (IC clusterise [0.436 ; 0.499] sur 1172 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ swing_based a 2.25 ATR (stop 17.234 %) — p(stop avant cible) 0.2139 [0.17 ; 0.26], R/R 1.472, perte reelle 17.632 % (gap inclus), EV 2.9883 % — **REFUSE**
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.94 % > budget 12.00 %
   - 🟢 support a 4.25 ATR (stop 29.896 %) — p(stop avant cible) 0.0288 [0.01 ; 0.05], R/R 0.863, perte reelle 30.058 % (gap inclus), EV 3.7329 % — **REFUSE**
      - refuse : R/R 0.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.13 % > budget 12.00 %
   - 🟢 support a 5.39 ATR (stop 37.079 %) — p(stop avant cible) 0.0154 [0.01 ; 0.03], R/R 0.697, perte reelle 37.213 % (gap inclus), EV 3.6563 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.64 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.583 %) — p(stop avant cible) 0.8705 [0.83 ; 0.90], R/R 15.366, perte reelle 1.689 % (gap inclus), EV 1.05 % — **REFUSE**
      - refuse : cible atteinte seulement 6.6 % du temps (< 15 %) meme a 10 seances : le R/R de 15.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.871, borne haute 0.903 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 3.165 %) — p(stop avant cible) 0.7567 [0.71 ; 0.80], R/R 7.643, perte reelle 3.396 % (gap inclus), EV 1.7779 % — **REFUSE**
      - refuse : cible atteinte seulement 10.9 % du temps (< 15 %) meme a 10 seances : le R/R de 7.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.757, borne haute 0.800 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ grid_snapped a 0.83 ATR (stop 7.17 %) — p(stop avant cible) 0.5644 [0.51 ; 0.62], R/R 3.429, perte reelle 7.568 % (gap inclus), EV 2.1749 % — **REFUSE**
      - refuse : p_stop_first 0.564, borne haute 0.616 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.75 ATR (stop 11.079 %) — p(stop avant cible) 0.4097 [0.36 ; 0.46], R/R 2.253, perte reelle 11.518 % (gap inclus), EV 2.2477 % — **REFUSE**
      - refuse : R/R 2.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.67 % > budget 12.00 %
   - ⚪ atr_grid a 2.0 ATR (stop 12.662 %) — p(stop avant cible) 0.3549 [0.31 ; 0.41], R/R 1.984, perte reelle 13.081 % (gap inclus), EV 2.2827 % — **REFUSE**
      - refuse : R/R 1.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.63 % > budget 12.00 %
   - ⚪ grid_snapped a 2.25 ATR (stop 16.157 %) — p(stop avant cible) 0.2395 [0.20 ; 0.29], R/R 1.573, perte reelle 16.498 % (gap inclus), EV 2.9945 % — **REFUSE**
      - refuse : R/R 1.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.79 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 18.993 %) — p(stop avant cible) 0.1737 [0.14 ; 0.22], R/R 1.338, perte reelle 19.403 % (gap inclus), EV 3.3032 % — **REFUSE**
      - refuse : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.42 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 22.158 %) — p(stop avant cible) 0.091 [0.06 ; 0.12], R/R 1.145, perte reelle 22.668 % (gap inclus), EV 3.7062 % — **REFUSE**
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.09 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 25.323 %) — p(stop avant cible) 0.053 [0.03 ; 0.08], R/R 1.0, perte reelle 25.962 % (gap inclus), EV 3.7577 % — **REFUSE**
      - refuse : R/R 1.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.00 % > budget 12.00 %
   - 🟢 grid_snapped a 4.25 ATR (stop 28.82 %) — p(stop avant cible) 0.0288 [0.01 ; 0.05], R/R 0.892, perte reelle 29.107 % (gap inclus), EV 3.7603 % — **REFUSE**
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.58 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 31.654 %) — p(stop avant cible) 0.0288 [0.01 ; 0.05], R/R 0.82, perte reelle 31.662 % (gap inclus), EV 3.6867 % — **REFUSE**
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.06 % > budget 12.00 %
   - 🟢 grid_snapped a 5.39 ATR (stop 36.003 %) — p(stop avant cible) 0.0191 [0.01 ; 0.04], R/R 0.721, perte reelle 36.003 % (gap inclus), EV 3.6588 % — **REFUSE**
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.61 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 37.985 %) — p(stop avant cible) 0.0137 [0.01 ; 0.03], R/R 0.682, perte reelle 38.059 % (gap inclus), EV 3.6616 % — **REFUSE**
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.53 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 41.151 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.631, perte reelle 41.151 % (gap inclus), EV 3.7157 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.45 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 44.316 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.586, perte reelle 44.316 % (gap inclus), EV 3.7307 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.17 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 47.481 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.547, perte reelle 47.481 % (gap inclus), EV 3.7307 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.17 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 50.647 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.512, perte reelle 50.647 % (gap inclus), EV 3.7307 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.17 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 160.1, ATR14 10.1357 (6.331 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.356 ATR = 2.254 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.317 % | 159.5932 | 91.18 % | 94.21 % | 95.48 % | 96.56 % | 97.73 % | 98.7 % |
| 0.1 ATR | 0.633 % | 159.0864 | 84.71 % | 89.79 % | 91.65 % | 94.29 % | 96.04 % | 97.3 % |
| 0.15 ATR | 0.95 % | 158.5796 | 77.75 % | 84.89 % | 87.52 % | 90.85 % | 93.57 % | 95.2 % |
| 0.2 ATR | 1.266 % | 158.0729 | 69.02 % | 79.59 % | 83.5 % | 87.8 % | 91.2 % | 93.21 % |
| 0.25 ATR | 1.583 % | 157.5661 | 62.45 % | 75.66 % | 80.16 % | 86.12 % | 89.91 % | 92.61 % |
| 0.35 ATR | 2.216 % | 156.5525 | 50.59 % | 67.22 % | 73.08 % | 80.81 % | 85.46 % | 89.91 % |
| 0.5 ATR | 3.165 % | 155.0321 | 35.59 % | 55.05 % | 62.48 % | 72.83 % | 80.61 % | 87.01 % |
| 0.75 ATR | 4.748 % | 152.4982 | 16.96 % | 34.94 % | 46.46 % | 58.07 % | 72.3 % | 80.22 % |
| 1.0 ATR | 6.331 % | 149.9643 | 8.33 % | 23.75 % | 33.89 % | 47.15 % | 64.19 % | 74.73 % |
| 1.25 ATR | 7.914 % | 147.4304 | 4.12 % | 15.51 % | 24.95 % | 37.11 % | 56.08 % | 69.03 % |
| 1.5 ATR | 9.496 % | 144.8964 | 2.25 % | 10.4 % | 18.07 % | 29.43 % | 48.17 % | 62.74 % |
| 2.0 ATR | 12.662 % | 139.8286 | 0.59 % | 4.51 % | 8.84 % | 17.81 % | 34.62 % | 52.25 % |
| 2.5 ATR | 15.827 % | 134.7607 | 0.29 % | 2.45 % | 4.91 % | 11.61 % | 23.94 % | 44.36 % |
| 3.0 ATR | 18.993 % | 129.6929 | 0.2 % | 0.79 % | 2.55 % | 7.09 % | 16.42 % | 36.36 % |
| 4.0 ATR | 25.323 % | 119.5572 | 0.1 % | 0.59 % | 1.38 % | 3.54 % | 9.4 % | 23.18 % |
| 6.0 ATR | 37.985 % | 99.2857 | 0.0 % | 0.29 % | 0.79 % | 1.57 % | 4.45 % | 11.99 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.36 ATR | 0.41 ATR | 0.54 ATR | 0.64 ATR | 0.71 ATR | 0.95 ATR | 1.20 ATR |
| **2 s.** | 0.26 ATR | 0.56 ATR | 0.62 ATR | 0.79 ATR | 0.97 ATR | 1.11 ATR | 1.53 ATR | 1.96 ATR |
| **3 s.** | 0.32 ATR | 0.69 ATR | 0.78 ATR | 1.02 ATR | 1.25 ATR | 1.43 ATR | 1.94 ATR | 2.49 ATR |
| **5 s.** | 0.46 ATR | 0.94 ATR | 1.05 ATR | 1.38 ATR | 1.69 ATR | 1.91 ATR | 2.68 ATR | 3.59 ATR |
| **10 s.** | 0.67 ATR | 1.44 ATR | 1.62 ATR | 2.08 ATR | 2.45 ATR | 2.76 ATR | 3.92 ATR | 5.78 ATR |
| **20 s.** | 0.99 ATR | 2.14 ATR | 2.46 ATR | 3.25 ATR | 3.86 ATR | 4.57 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.406–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.625–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.779–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.331 %, prix 149.9641), p(touche) 33.89 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.054–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.914 %, prix 147.4297), p(touche) 37.11 % (en stress 87.25 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 18.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.617–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 19.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.459–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.281 | EV/share : €3.232 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 28 % | T2 16 % | T3 12 %
- Kelly (position) : f* 0.176 | ¼-Kelly 0.044 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 10.0 | bear 5.0 | side 85.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 480.0 (= 3 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.163% → cible +3.203% / stop −2.0%, p_fill 74%, n_eff≈81.4) : P(cible|rempli) **33%** · **EV/risk -0.073** (×p_fill ; si rempli -0.20% du capital)
  - **swing** (entrée dip −2.546% → cible +14.723% / stop −7.361%, p_fill 61%, n_eff≈72.1) : P(cible|rempli) **24%** · **EV/risk -0.026** (×p_fill ; si rempli -0.31% du capital)
  - **deep** (entrée dip −3.944% → cible +16.385% / stop −9.886%, p_fill 64%, n_eff≈73.0) : P(cible|rempli) **26%** · **EV/risk -0.155** (×p_fill ; si rempli -2.39% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→78% · +2.0%→66% · +3.0%→55% · +5.0%→37% · +8.0%→18%
- Range intraday médian 7.97% (p90 14.88%) · excursion haute méd. +3.44% / basse méd. −3.03%
- Profil de vol intra : ouverture 4.937% vs midi 1.448% vs clôture 2.148% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 11% · trend ↑1%/↓2% ; spike-down 70% · recovery-V 42%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; mean-reverting — autocorr -0.03)_ ; drift intra méd. 0.426% ; recovery-V 42%
- **σ réalisé intraday** 3.911% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 55% / whipsaw 32%
- POC intraday (dernière séance, temps-au-prix) : 155.931 (VA 155.415–156.361 ; dernier close 156.88)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 42% · rebond 75% · **stop −7.26%** sous le fill (sous le bruit) · cible +3.18% · R/R 0.44 (high win-rate)
- Gaps overnight (n=159) : méd. 0.46% · baisse 40% (gap-down >1% 24% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −1.05% (p90 −2.94%) · haut méd +0.85% · range méd 2.29%
- Excursion ouverture 15min (n=160) : bas méd −1.29% (p90 −4.33%) · haut méd +1.12% · range méd 3.01%
- Excursion ouverture 30min (n=160) : bas méd −1.49% (p90 −4.85%) · haut méd +1.24% · range méd 3.39%
- Excursion ouverture 60min (n=160) : bas méd −1.63% (p90 −5.0%) · haut méd +1.26% · range méd 3.65%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 155.95 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 75% (122/159) · gap 31% · délai 0.2min · rebond 73% (88/122) (MFE +2.07%)
   - −1.0% : fill 30min 55% · séance 70% (112/159) · gap 24% · délai 0.2min · rebond 73% (82/112) (MFE +2.02%)
   - −1.5% : fill 30min 48% · séance 60% (102/159) · gap 18% · délai 0.5min · rebond 75% (77/102) (MFE +2.33%)
   - −2.0% : fill 30min 42% · séance 57% (95/159) · gap 16% · délai 4.8min · rebond 74% (74/95) (MFE +2.56%)
   - −3.0% : fill 30min 27% · séance 42% (75/159) · gap 8% · délai 3.3min · rebond 75% (63/75) (MFE +3.18%)
   - −4.0% : fill 30min 20% · séance 35% (64/159) · gap 5% · délai 15.0min · rebond 77% (53/64) (MFE +2.54%)
   - −5.0% : fill 30min 12% · séance 28% (50/159) · gap 2% · délai 53.0min · rebond 67% (38/50) (MFE +2.27%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.81% (p90 −3.3%) → stop au-delà de −1.98% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −2.39%) → stop au-delà de −1.96% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.91% (p90 −2.29%) → stop au-delà de −1.91% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1335 jambes) : jambe baissière méd −1.25% (p90 −3.03%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (57 séances) :
      · −1.0% : fill 93% (54/57) · rebond 67% (36/54)
      · −2.0% : fill 90% (52/57) · rebond 72% (39/52)
      · −3.0% : fill 72% (45/57) · rebond 73% (37/45)
      · −4.0% : fill 63% (39/57) · rebond 85% (35/39)
      · −5.0% : fill 50% (32/57) · rebond 74% (26/32)
   - **flat** (13 séances) :
      · −1.0% : fill 78% (11/13) · rebond 86% (9/11)
      · −2.0% : fill 68% (10/13) · rebond 88% (9/10)
      · −3.0% : fill 66% (9/13) · rebond 64% (7/9)
      · −4.0% : fill 60% (8/13) · rebond 79% (6/8)
      · −5.0% : fill 44% (7/13) · rebond 45% (5/7)
   - **gap-up** (89 séances) :
      · −1.0% : fill 54% (47/89) · rebond 77% (37/47)
      · −2.0% : fill 35% (33/89) · rebond 73% (26/33)
      · −3.0% : fill 19% (21/89) · rebond 87% (19/21)
      · −4.0% : fill 14% (17/89) · rebond 56% (12/17)
      · −5.0% : fill 11% (11/89) · rebond 60% (7/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 67% si les 15 1res min sont vertes (77 cas) · 39% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:25** → P(séance verte=clôture>ouverture) 77% si début vert vs 30% si rouge (base 52% · écart 46 pts) ; prédictivité sature ensuite (plafond brut 272min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **77%** · continue >prix actuel 60% ; creux résiduel méd -1.17% (q20 -3.79%) → **SL/trailing à −3.79%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.78% / q75 +5.21% → **scale +2.78% / runner +5.21%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **30%** (continue à baisser 52%) → **RÉDUIRE ~69%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.35%** (au-delà de la MAE q10 -7.35%), cible rebond +2.31% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.65% .. +5.8%] · haut q95 +6.52% · bas q05 -5.95%
   - 60min (n=160) : retour [-5.43% .. +4.94%] · haut q95 +7.75% · bas q05 -6.57%
   - 2h (n=160) : retour [-6.04% .. +5.6%] · haut q95 +7.85% · bas q05 -7.51%
   - 4h (n=160) : retour [-6.94% .. +7.21%] · haut q95 +8.66% · bas q05 -8.18%
   - 6h (n=160) : retour [-7.82% .. +8.61%] · haut q95 +9.16% · bas q05 -9.43%
   - session (n=160) : retour [-7.99% .. +8.94%] · haut q95 +11.8% · bas q05 -11.05%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 6.6)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **42%**. Lecture précoce 30 min : signature présente → 23% vs absente 2% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.98% (p75 1.39% / p90 1.98%) · ~4.89 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **90%** (reprise méd 25.0 min, n=57)
   - −1.0% → **90%** (reprise méd 45.44 min, n=31)
   - −1.5% → **80%** (reprise méd 50.92 min, n=16)
   - −2.0% → **85%** (reprise méd 52.07 min, n=12)
   - −3.0% → **100%** (reprise méd 60.96 min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.98%** (p90, défaut prudent ; serré/agressif −1.39%) ; extension open→close méd +8.74% (q75 +9.15% / q95 +13.89%), MFE méd +9.28% / q90 +14.1%
   - Échelle scale-out : +9.28% (33%) / +9.96% (33%) / +14.1% (34%)
- **DÉSARMER** : repli > **−1.98%** depuis le plus-haut = décay → P(retournement) **15%** (préavis méd 36.46 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +14.1% : P(retournement après) 0% (mèche méd 2.71%)
- **CONTEXTE** : la dernière heure tient les gains 79% du temps (retour médian dernière heure +1.27%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.49 · part idiosyncratique 0.51
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 61.7  _(momentum haussier)_
- **ADX** : 26.6  _(tendance etablie)_
- **MACD** : hist 0.999  _(pas de croisement recent)_
- **BB** : %B 0.91 · largeur 28.4%
- **ATR** : 10.14 (67.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF 0.176  _(accumulation)_
- **Vol ratio** : 0.36  _(volume atone)_
- **Choppiness** : 45.4  _(transition)_
- **MA** : MA20 143.37 · MA50 126.05 · MA200 92.12  _(prix > MA20)_
- **Dist MA** : MA20 +11.7% · MA50 +27.0% · MA200 +73.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (851298 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
