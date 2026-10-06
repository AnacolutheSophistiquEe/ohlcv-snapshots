# SRT3

**Generated** : 2026-10-06T21:41:33.521350+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €259.70  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 24/125 fenêtres (p_fill pondéré 16 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot €259.70 (+2.8% vs entrée) · entrée €252.63 · stop €245.05 · T1 €260.71 · R/R 1.07  
> ↳ ¼-Kelly 0.008 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €252.00–€253.26 (mid €252.63)
- Spot actuel : €259.70 (+2.8% au-dessus de la zone — repli à attendre)
- Stop : €245.05 (plancher anti-bruit 5 s — stop EV-optimal −3% (first-passage 5 s réel) ; -3.00 % depuis l'entree)
- Targets : T1 €260.71 · R/R 1.07 | T2 €265.30 · R/R 1.67 | T3 €269.89 · R/R 2.28
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €245.05


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.18 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (9.52 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1274).
   - exécution **0.452 pt plus bas** dans le cas TYPIQUE (médiane), 3.839 au p90, **4.685 au pire**
   - perte réelle **11.278 %** en moyenne _(tirée par la queue)_, jusqu'à **14.205 %** — au lieu des 9.52 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0041 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.607 % | p01 -3.24 % | pire -14.205 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1218** [0.0794 ; 0.1767] _(largeur 9.7 pt, n_eff 173.1)_
   - swing : **0.4564** [0.4044 ; 0.5091] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.3945** [0.344 ; 0.4467] _(largeur 10.3 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (35.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-4.09 %** | CVaR **-6.57 %** | vol 2.85 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.98 % vs -9.13 % si l'on extrapolait par √5 _(rapport 1.092 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0841** (β de hausse 1.1668, asymétrie 0.9292) vs GDAXI — 599 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.303× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 252.8161 sur atr_grid (0.75 ATR, 2.651 %) — p(stop avant cible) 0.6882 [0.64 ; 0.74], R/R 3.055, perte reelle 2.714 % (gap inclus), CVaR 3.516 %, EV 0.1664 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.3369 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.688, borne haute 0.735 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.301 %) — p(stop avant cible) 0.4291 [0.38 ; 0.48], R/R 1.524, perte reelle 5.442 % (gap inclus), EV 0.6886 % — **REFUSE**
      - refuse : R/R 1.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 3.18 ATR (stop 13.458 %) — p(stop avant cible) 0.0773 [0.05 ; 0.11], R/R 0.611, perte reelle 13.583 % (gap inclus), EV 0.8558 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.65 % > budget 12.00 %
   - ⚪ swing_based a 3.85 ATR (stop 15.822 %) — p(stop avant cible) 0.0292 [0.02 ; 0.05], R/R 0.506, perte reelle 16.389 % (gap inclus), EV 0.9915 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.56 % > budget 12.00 %
   - 🟢 support a 6.74 ATR (stop 26.044 %) — p(stop avant cible) 0.0016 [0.00 ; 0.01], R/R 0.309, perte reelle 26.818 % (gap inclus), EV 1.096 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.02 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.884 %) — p(stop avant cible) 0.8854 [0.85 ; 0.92], R/R 9.082, perte reelle 0.913 % (gap inclus), EV 0.0479 % — **REFUSE**
      - refuse : cible atteinte seulement 9.8 % du temps (< 15 %) meme a 10 seances : le R/R de 9.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.885, borne haute 0.916 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 1.767 %) — p(stop avant cible) 0.7881 [0.74 ; 0.83], R/R 4.588, perte reelle 1.808 % (gap inclus), EV 0.032 % — **REFUSE**
      - refuse : p_stop_first 0.788, borne haute 0.829 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 2.651 %) — p(stop avant cible) 0.6882 [0.64 ; 0.74], R/R 3.055, perte reelle 2.714 % (gap inclus), EV 0.1664 % — **REFUSE**
      - refuse : p_stop_first 0.688, borne haute 0.735 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 3.534 %) — p(stop avant cible) 0.5933 [0.54 ; 0.64], R/R 2.286, perte reelle 3.627 % (gap inclus), EV 0.3694 % — **REFUSE**
      - refuse : p_stop_first 0.593, borne haute 0.644 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.25 ATR (stop 4.418 %) — p(stop avant cible) 0.5164 [0.46 ; 0.57], R/R 1.83, perte reelle 4.531 % (gap inclus), EV 0.4132 % — **REFUSE**
      - refuse : p_stop_first 0.516, borne haute 0.569 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.75 ATR (stop 6.185 %) — p(stop avant cible) 0.3651 [0.32 ; 0.42], R/R 1.318, perte reelle 6.291 % (gap inclus), EV 0.7411 % — **REFUSE**
      - refuse : R/R 1.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 7.069 %) — p(stop avant cible) 0.3275 [0.28 ; 0.38], R/R 1.158, perte reelle 7.165 % (gap inclus), EV 0.6929 % — **REFUSE**
      - refuse : R/R 1.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 7.952 %) — p(stop avant cible) 0.2578 [0.21 ; 0.31], R/R 1.025, perte reelle 8.09 % (gap inclus), EV 0.7658 % — **REFUSE**
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 8.836 %) — p(stop avant cible) 0.2087 [0.17 ; 0.25], R/R 0.923, perte reelle 8.98 % (gap inclus), EV 0.7606 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 9.719 %) — p(stop avant cible) 0.1777 [0.14 ; 0.22], R/R 0.844, perte reelle 9.825 % (gap inclus), EV 0.8464 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 3.18 ATR (stop 12.303 %) — p(stop avant cible) 0.0921 [0.07 ; 0.13], R/R 0.672, perte reelle 12.334 % (gap inclus), EV 0.8974 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.36 % > budget 12.00 %
   - ⚪ grid_snapped a 3.85 ATR (stop 14.667 %) — p(stop avant cible) 0.0443 [0.03 ; 0.07], R/R 0.552, perte reelle 15.022 % (gap inclus), EV 0.9349 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.78 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 17.671 %) — p(stop avant cible) 0.0128 [0.00 ; 0.03], R/R 0.442, perte reelle 18.748 % (gap inclus), EV 1.0542 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.67 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 19.439 %) — p(stop avant cible) 0.0112 [0.00 ; 0.03], R/R 0.414, perte reelle 20.047 % (gap inclus), EV 1.0478 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.77 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 21.206 %) — p(stop avant cible) 0.0085 [0.00 ; 0.02], R/R 0.372, perte reelle 22.276 % (gap inclus), EV 1.0459 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.82 % > budget 12.00 %
   - 🟢 grid_snapped a 6.74 ATR (stop 24.888 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.314, perte reelle 26.391 % (gap inclus), EV 1.0941 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.04 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 26.507 %) — p(stop avant cible) 0.0016 [0.00 ; 0.01], R/R 0.309, perte reelle 26.868 % (gap inclus), EV 1.0959 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.02 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 28.274 %) — p(stop avant cible) 0.0008 [0.00 ; 0.01], R/R 0.293, perte reelle 28.274 % (gap inclus), EV 1.0995 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.95 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 259.7, ATR14 9.1786 (3.534 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.383 ATR = 1.354 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.177 % | 259.2411 | 89.05 % | 92.79 % | 94.27 % | 96.04 % | 97.81 % | 98.49 % |
| 0.1 ATR | 0.353 % | 258.7822 | 82.64 % | 88.45 % | 90.81 % | 93.47 % | 95.72 % | 96.98 % |
| 0.15 ATR | 0.53 % | 258.3232 | 75.05 % | 83.61 % | 86.76 % | 90.3 % | 93.33 % | 94.97 % |
| 0.2 ATR | 0.707 % | 257.8643 | 68.54 % | 78.78 % | 82.81 % | 87.23 % | 92.04 % | 94.37 % |
| 0.25 ATR | 0.884 % | 257.4054 | 63.12 % | 75.42 % | 79.55 % | 84.85 % | 90.25 % | 93.07 % |
| 0.35 ATR | 1.237 % | 256.4875 | 53.25 % | 69.0 % | 73.81 % | 80.5 % | 86.87 % | 90.95 % |
| 0.5 ATR | 1.767 % | 255.1107 | 38.36 % | 56.47 % | 64.23 % | 73.76 % | 82.29 % | 88.24 % |
| 0.75 ATR | 2.651 % | 252.8161 | 19.23 % | 36.72 % | 47.63 % | 59.01 % | 72.04 % | 81.71 % |
| 1.0 ATR | 3.534 % | 250.5214 | 9.86 % | 24.48 % | 34.58 % | 47.62 % | 62.79 % | 74.57 % |
| 1.25 ATR | 4.418 % | 248.2268 | 4.73 % | 14.91 % | 24.6 % | 38.32 % | 53.13 % | 67.34 % |
| 1.5 ATR | 5.301 % | 245.9322 | 2.27 % | 9.97 % | 17.79 % | 30.79 % | 45.77 % | 61.51 % |
| 2.0 ATR | 7.069 % | 241.3429 | 0.69 % | 4.54 % | 8.1 % | 17.13 % | 34.43 % | 51.66 % |
| 2.5 ATR | 8.836 % | 236.7536 | 0.3 % | 1.97 % | 4.74 % | 10.69 % | 24.08 % | 41.51 % |
| 3.0 ATR | 10.603 % | 232.1643 | 0.2 % | 1.48 % | 2.96 % | 6.34 % | 17.21 % | 33.97 % |
| 4.0 ATR | 14.137 % | 222.9857 | 0.0 % | 0.69 % | 1.78 % | 3.56 % | 8.76 % | 19.9 % |
| 6.0 ATR | 21.206 % | 204.6286 | 0.0 % | 0.0 % | 0.0 % | 0.59 % | 2.09 % | 7.04 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.68 ATR | 0.74 ATR | 1.00 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.58 ATR | 0.65 ATR | 0.83 ATR | 0.99 ATR | 1.12 ATR | 1.50 ATR | 1.96 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.80 ATR | 1.04 ATR | 1.24 ATR | 1.42 ATR | 1.90 ATR | 2.46 ATR |
| **5 s.** | 0.47 ATR | 0.95 ATR | 1.07 ATR | 1.43 ATR | 1.71 ATR | 1.90 ATR | 2.58 ATR | 3.48 ATR |
| **10 s.** | 0.68 ATR | 1.36 ATR | 1.53 ATR | 2.07 ATR | 2.46 ATR | 2.80 ATR | 3.85 ATR | 5.13 ATR |
| **20 s.** | 0.98 ATR | 2.08 ATR | 2.33 ATR | 3.07 ATR | 3.64 ATR | 3.99 ATR | 5.54 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.433–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.767 %, prix 255.1111), p(touche) 38.36 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.645–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.651 %, prix 252.8154), p(touche) 36.72 % (en stress 88.24 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.8–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.534 %, prix 250.5222), p(touche) 34.58 % (en stress 92.16 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.07–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.418 %, prix 248.2265), p(touche) 38.32 % (en stress 93.07 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.534–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.069 %, prix 241.3418), p(touche) 34.43 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.328–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.836 %, prix 236.7529), p(touche) 41.51 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.006 | EV/share : €0.049 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 22 % | T2 — | T3 —
- Kelly (position) : f* 0.033 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 16.8 | bear 10.6 | side 72.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 260.0 (= 1 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈60.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.722% → cible +3.199% / stop −3.0%, p_fill 16%, n_eff≈20.9) : P(cible|rempli) **15%** · **EV/risk +0.021** (×p_fill ; si rempli +0.38% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=8, n_eff=8))
  - **deep** : indisponible (échantillon insuffisant (n=11, n_eff=11))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→72% · +2.0%→44% · +3.0%→23% · +5.0%→7% · +8.0%→0%
- Range intraday médian 3.33% (p90 6.12%) · excursion haute méd. +1.77% / basse méd. −1.47%
- Profil de vol intra : ouverture 1.936% vs midi 0.828% vs clôture 0.957% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 49% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; mean-reverting — autocorr -0.047)_ ; drift intra méd. 0.284% ; recovery-V 26%
- **σ réalisé intraday** 2.228% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 63% / bas 61% / whipsaw 25%
- POC intraday (dernière séance, temps-au-prix) : 252.4856 (VA 251.8969–253.2706 ; dernier close 252.85)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 46% · rebond 59% · **stop −1.74%** sous le fill (sous le bruit) · cible +1.24% · R/R 0.71 (high win-rate)
- Gaps overnight (n=159) : méd. -0.13% · baisse 58% (gap-down >1% 6% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.26% (p90 −1.61%) · haut méd +0.6% · range méd 1.05%
- Excursion ouverture 15min (n=160) : bas méd −0.3% (p90 −1.79%) · haut méd +0.78% · range méd 1.34%
- Excursion ouverture 30min (n=160) : bas méd −0.43% (p90 −1.9%) · haut méd +0.86% · range méd 1.52%
- Excursion ouverture 60min (n=160) : bas méd −0.49% (p90 −2.03%) · haut méd +0.91% · range méd 1.74%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 251.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 80% (123/159) · gap 25% · délai 0.5min · rebond 51% (67/123) (MFE +1.04%)
   - −1.0% : fill 30min 39% · séance 67% (103/159) · gap 6% · délai 7.9min · rebond 58% (60/103) (MFE +1.2%)
   - −1.5% : fill 30min 22% · séance 46% (78/159) · gap 2% · délai 38.9min · rebond 59% (45/78) (MFE +1.24%)
   - −2.0% : fill 30min 7% · séance 32% (57/159) · gap 0% · délai 236.0min · rebond 50% (29/57) (MFE +1.06%)
   - −3.0% : fill 30min 2% · séance 10% (26/159) · gap 0% · délai 183.5min · rebond 50% (12/26) (MFE +0.88%)
   - −4.0% : fill 30min 1% · séance 5% (13/159) · gap 0% · délai 55.4min · rebond 62% (8/13) (MFE +1.73%)
   - −5.0% : fill 30min 0% · séance 3% (7/159) · gap 0% · délai 141.9min · rebond 84% (6/7) (MFE +2.49%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.18% (p90 −1.59%) → stop au-delà de −1.0% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.07% (p90 −1.59%) → stop au-delà de −1.09% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.15% (p90 −1.99%) → stop au-delà de −1.15% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=442 jambes) : jambe baissière méd −1.02% (p90 −2.22%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (61 séances) :
      · −1.0% : fill 78% (49/61) · rebond 61% (30/49)
      · −2.0% : fill 37% (27/61) · rebond 47% (14/27)
      · −3.0% : fill 13% (15/61) · rebond 34% (7/15)
      · −4.0% : fill 6% (8/61) · rebond 60% (6/8)
      · −5.0% : fill 3% (4/61) · rebond 100% (4/4)
   - **flat** (40 séances) :
      · −1.0% : fill 61% (25/40) · rebond 53% (12/25)
      · −2.0% : fill 34% (16/40) · rebond 49% (7/16)
      · −3.0% : fill 6% (5/40) · rebond 34% (1/5)
      · −4.0% : fill 2% (2/40) · rebond 0% (0/2)
      · −5.0% : fill 2% (1/40) · rebond 0% (0/1)
   - **gap-up** (58 séances) :
      · −1.0% : fill 56% (29/58) · rebond 57% (18/29)
      · −2.0% : fill 22% (14/58) · rebond 59% (8/14)
      · −3.0% : fill 9% (6/58) · rebond 88% (4/6)
      · −4.0% : fill 6% (3/58) · rebond 89% (2/3)
      · −5.0% : fill 5% (2/58) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 56% si les 15 1res min sont vertes (88 cas) · 42% si rouges (72 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:31** → P(séance verte=clôture>ouverture) 67% si début vert vs 27% si rouge (base 50% · écart 40 pts) ; prédictivité sature ensuite (plafond brut 235min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=84) : tient le vert **67%** · continue >prix actuel 50% ; creux résiduel méd -1.2% (q20 -2.49%) → **SL/trailing à −2.49%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.95% / q75 +1.97% → **scale +0.95% / runner +1.97%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **27%** (continue à baisser 50%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.65%** (au-delà de la MAE q10 -2.65%), cible rebond +1.2% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.07% .. +2.01%] · haut q95 +2.53% · bas q05 -2.81%
   - 60min (n=160) : retour [-2.27% .. +2.33%] · haut q95 +2.72% · bas q05 -2.84%
   - 2h (n=160) : retour [-2.12% .. +2.25%] · haut q95 +2.93% · bas q05 -2.95%
   - 4h (n=160) : retour [-2.23% .. +2.43%] · haut q95 +3.11% · bas q05 -3.15%
   - 6h (n=160) : retour [-2.48% .. +2.87%] · haut q95 +3.58% · bas q05 -3.16%
   - session (n=160) : retour [-3.0% .. +4.36%] · haut q95 +5.16% · bas q05 -3.82%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.32%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.15 · part idiosyncratique 0.85
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 64.8  _(momentum haussier)_
- **ADX** : 24.4  _(pas de tendance nette)_
- **MACD** : hist -0.022  _(bearish_recent)_
- **BB** : %B 0.74 · largeur 17.6%
- **ATR** : 9.18 (66.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.001  _(neutre)_
- **Vol ratio** : 2.64  _(volume au-dessus de la moyenne)_
- **Choppiness** : 57.6  _(transition)_
- **MA** : MA20 249.0 · MA50 242.04 · MA200 233.53  _(prix > MA20)_
- **Dist MA** : MA20 +4.3% · MA50 +7.3% · MA200 +11.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (548542 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
