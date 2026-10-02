# SRT3

**Generated** : 2026-10-02T21:41:31.868280+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €251.40  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)  
> ↳ spot €251.40 (+4.6% vs entrée) · entrée €240.41 · stop €231.68 · T1 €250.18 · R/R 1.12  
> ↳ ¼-Kelly 0.015 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €239.09–€241.74 (mid €240.41)
- Spot actuel : €251.40 (+4.6% au-dessus de la zone — repli à attendre)
- Stop : €231.68 (plancher anti-bruit (R/R<2) ; -3.63 % depuis l'entree)
- Targets : T1 €250.18 · R/R 1.12 | T2 €259.95 · R/R 2.24 | T3 €269.71 · R/R 3.36
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €231.68


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.18 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (7.85 %)** : le gap seul le franchit 0.392 % des séances (5 fois sur 1274).
   - exécution **1.807 pt plus bas** dans le cas TYPIQUE (médiane), 4.662 au p90, **6.355 au pire**
   - perte réelle **10.096 %** en moyenne _(tirée par la queue)_, jusqu'à **14.205 %** — au lieu des 7.85 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0088 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.607 % | p01 -3.24 % | pire -14.205 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4223** [0.3505 ; 0.4967] _(largeur 14.6 pt, n_eff 173.1)_
   - swing : **0.4377** [0.3861 ; 0.4903] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.3873** [0.3371 ; 0.4394] _(largeur 10.2 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (29.9 pt), swing (43.1 pt), deep (46.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-4.09 %** | CVaR **-6.57 %** | vol 2.85 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.98 % vs -9.13 % si l'on extrapolait par √5 _(rapport 1.092 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0837** (β de hausse 1.1676, asymétrie 0.9281) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.281× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 244.8482 sur atr_grid (0.75 ATR, 2.606 %) — p(stop avant cible) 0.6945 [0.64 ; 0.74], R/R 2.727, perte reelle 2.671 % (gap inclus), CVaR 3.496 %, EV 0.0604 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.4388 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.695, borne haute 0.741 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.212 %) — p(stop avant cible) 0.4446 [0.39 ; 0.50], R/R 1.367, perte reelle 5.329 % (gap inclus), EV 0.4408 % — **REFUSE**
      - refuse : R/R 1.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 2.39 ATR (stop 10.105 %) — p(stop avant cible) 0.1728 [0.14 ; 0.22], R/R 0.715, perte reelle 10.191 % (gap inclus), EV 0.6535 % — **REFUSE**
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ swing_based a 3.08 ATR (stop 12.529 %) — p(stop avant cible) 0.0917 [0.06 ; 0.13], R/R 0.58, perte reelle 12.556 % (gap inclus), EV 0.729 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.58 % > budget 12.00 %
   - 🟢 support a 6.13 ATR (stop 23.124 %) — p(stop avant cible) 0.0035 [0.00 ; 0.01], R/R 0.297, perte reelle 24.542 % (gap inclus), EV 0.9372 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.22 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.869 %) — p(stop avant cible) 0.8778 [0.84 ; 0.91], R/R 8.114, perte reelle 0.898 % (gap inclus), EV 0.057 % — **REFUSE**
      - refuse : cible atteinte seulement 11.4 % du temps (< 15 %) meme a 10 seances : le R/R de 8.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.878, borne haute 0.909 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 1.737 %) — p(stop avant cible) 0.792 [0.75 ; 0.83], R/R 4.098, perte reelle 1.777 % (gap inclus), EV -0.0213 % — **REFUSE**
      - refuse : p_stop_first 0.792, borne haute 0.832 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.02 %) : P(cible) 18.3 % x 7.28 % + P(rien) 2.5 % x 2.10 % ne couvrent pas P(stop) 79.2 % x 1.78 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 2.606 %) — p(stop avant cible) 0.6945 [0.64 ; 0.74], R/R 2.727, perte reelle 2.671 % (gap inclus), EV 0.0604 % — **REFUSE**
      - refuse : p_stop_first 0.695, borne haute 0.741 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.0 ATR (stop 3.475 %) — p(stop avant cible) 0.601 [0.55 ; 0.65], R/R 2.043, perte reelle 3.566 % (gap inclus), EV 0.2042 % — **REFUSE**
      - refuse : p_stop_first 0.601, borne haute 0.652 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.25 ATR (stop 4.344 %) — p(stop avant cible) 0.5228 [0.47 ; 0.58], R/R 1.632, perte reelle 4.462 % (gap inclus), EV 0.2686 % — **REFUSE**
      - refuse : p_stop_first 0.523, borne haute 0.575 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.75 ATR (stop 6.081 %) — p(stop avant cible) 0.3703 [0.32 ; 0.42], R/R 1.174, perte reelle 6.203 % (gap inclus), EV 0.6034 % — **REFUSE**
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 6.95 %) — p(stop avant cible) 0.3313 [0.28 ; 0.38], R/R 1.035, perte reelle 7.037 % (gap inclus), EV 0.5777 % — **REFUSE**
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 2.39 ATR (stop 9.337 %) — p(stop avant cible) 0.1927 [0.15 ; 0.24], R/R 0.77, perte reelle 9.457 % (gap inclus), EV 0.6528 % — **REFUSE**
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 3.08 ATR (stop 11.761 %) — p(stop avant cible) 0.1158 [0.09 ; 0.15], R/R 0.617, perte reelle 11.797 % (gap inclus), EV 0.6795 % — **REFUSE**
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 13.899 %) — p(stop avant cible) 0.0638 [0.04 ; 0.09], R/R 0.519, perte reelle 14.036 % (gap inclus), EV 0.7567 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.07 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 15.637 %) — p(stop avant cible) 0.0339 [0.02 ; 0.06], R/R 0.451, perte reelle 16.149 % (gap inclus), EV 0.8132 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.89 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 17.374 %) — p(stop avant cible) 0.013 [0.00 ; 0.03], R/R 0.393, perte reelle 18.542 % (gap inclus), EV 0.9051 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.65 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 19.112 %) — p(stop avant cible) 0.0114 [0.00 ; 0.03], R/R 0.367, perte reelle 19.831 % (gap inclus), EV 0.8998 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.76 % > budget 12.00 %
   - 🟢 grid_snapped a 6.13 ATR (stop 22.356 %) — p(stop avant cible) 0.0049 [0.00 ; 0.02], R/R 0.308, perte reelle 23.652 % (gap inclus), EV 0.9269 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.40 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 24.324 %) — p(stop avant cible) 0.0025 [0.00 ; 0.01], R/R 0.283, perte reelle 25.721 % (gap inclus), EV 0.9398 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.13 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 26.061 %) — p(stop avant cible) 0.0016 [0.00 ; 0.01], R/R 0.272, perte reelle 26.82 % (gap inclus), EV 0.9457 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.05 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 27.799 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.262, perte reelle 27.799 % (gap inclus), EV 0.9432 % — **REFUSE**
      - refuse : R/R 0.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.07 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 251.4, ATR14 8.7357 (3.475 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.383 ATR = 1.331 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.174 % | 250.9632 | 89.05 % | 92.79 % | 94.27 % | 96.04 % | 97.81 % | 98.49 % |
| 0.1 ATR | 0.347 % | 250.5264 | 82.64 % | 88.45 % | 90.81 % | 93.47 % | 95.72 % | 96.98 % |
| 0.15 ATR | 0.521 % | 250.0896 | 74.95 % | 83.61 % | 86.76 % | 90.3 % | 93.33 % | 94.97 % |
| 0.2 ATR | 0.695 % | 249.6529 | 68.44 % | 78.78 % | 82.81 % | 87.23 % | 92.04 % | 94.37 % |
| 0.25 ATR | 0.869 % | 249.2161 | 63.12 % | 75.42 % | 79.55 % | 84.85 % | 90.25 % | 93.07 % |
| 0.35 ATR | 1.216 % | 248.3425 | 53.25 % | 69.1 % | 73.81 % | 80.5 % | 86.87 % | 90.95 % |
| 0.5 ATR | 1.737 % | 247.0321 | 38.36 % | 56.56 % | 64.23 % | 73.76 % | 82.39 % | 88.24 % |
| 0.75 ATR | 2.606 % | 244.8482 | 19.33 % | 36.82 % | 47.63 % | 59.01 % | 72.24 % | 81.71 % |
| 1.0 ATR | 3.475 % | 242.6643 | 9.86 % | 24.58 % | 34.58 % | 47.62 % | 62.99 % | 74.67 % |
| 1.25 ATR | 4.344 % | 240.4804 | 4.73 % | 15.0 % | 24.6 % | 38.32 % | 53.33 % | 67.54 % |
| 1.5 ATR | 5.212 % | 238.2964 | 2.27 % | 9.97 % | 17.79 % | 30.79 % | 45.97 % | 61.71 % |
| 2.0 ATR | 6.95 % | 233.9286 | 0.69 % | 4.54 % | 8.2 % | 17.13 % | 34.63 % | 51.86 % |
| 2.5 ATR | 8.687 % | 229.5607 | 0.3 % | 1.97 % | 4.74 % | 10.69 % | 24.28 % | 41.71 % |
| 3.0 ATR | 10.424 % | 225.1929 | 0.2 % | 1.48 % | 2.96 % | 6.34 % | 17.41 % | 34.17 % |
| 4.0 ATR | 13.899 % | 216.4571 | 0.0 % | 0.69 % | 1.78 % | 3.56 % | 8.86 % | 20.0 % |
| 6.0 ATR | 20.849 % | 198.9857 | 0.0 % | 0.0 % | 0.0 % | 0.59 % | 2.09 % | 7.04 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.68 ATR | 0.74 ATR | 1.00 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.58 ATR | 0.65 ATR | 0.83 ATR | 0.99 ATR | 1.12 ATR | 1.50 ATR | 1.96 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.80 ATR | 1.04 ATR | 1.24 ATR | 1.42 ATR | 1.91 ATR | 2.46 ATR |
| **5 s.** | 0.47 ATR | 0.95 ATR | 1.07 ATR | 1.43 ATR | 1.71 ATR | 1.90 ATR | 2.58 ATR | 3.48 ATR |
| **10 s.** | 0.68 ATR | 1.36 ATR | 1.54 ATR | 2.08 ATR | 2.46 ATR | 2.81 ATR | 3.87 ATR | 5.14 ATR |
| **20 s.** | 0.99 ATR | 2.09 ATR | 2.34 ATR | 3.08 ATR | 3.65 ATR | 4.00 ATR | 5.54 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.433–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.737 %, prix 247.0332), p(touche) 38.36 % (en stress 83.33 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.646–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.606 %, prix 244.8485), p(touche) 36.82 % (en stress 89.22 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.8–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.475 %, prix 242.6638), p(touche) 34.58 % (en stress 92.16 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.07–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.344 %, prix 240.4792), p(touche) 38.32 % (en stress 93.07 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.543–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.95 %, prix 233.9277), p(touche) 34.63 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.338–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.687 %, prix 229.5609), p(touche) 41.71 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.062 | EV/share : €0.545 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 13 % | T3 3 %
- Kelly (position) : f* 0.058 | ¼-Kelly 0.015 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 35.1 | bear 15.6 | side 49.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 503.0 (= 2 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.99% → cible +1.773% / stop −1.5%, p_fill 35%, n_eff≈40.5) : P(cible|rempli) **29%** · **EV/risk +0.067** (×p_fill ; si rempli +0.29% du capital)
  - **swing** (entrée dip −4.375% → cible +4.063% / stop −3.634%, p_fill 13%, n_eff≈16.5) : P(cible|rempli) **65%** · **EV/risk +0.055** (×p_fill ; si rempli +1.54% du capital)
  - **deep** (entrée dip −6.758% → cible +5.892% / stop −5.59%, p_fill 12%, n_eff≈15.6) : P(cible|rempli) **43%** · **EV/risk -0.014** (×p_fill ; si rempli -0.61% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→73% · +2.0%→45% · +3.0%→24% · +5.0%→7% · +8.0%→0%
- Range intraday médian 3.33% (p90 6.12%) · excursion haute méd. +1.81% / basse méd. −1.46%
- Profil de vol intra : ouverture 1.953% vs midi 0.825% vs clôture 0.959% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 10% · trend ↑0%/↓0% ; spike-down 48% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.113 ; mean-reverting — autocorr -0.044)_ ; drift intra méd. 0.446% ; recovery-V 22%
- **σ réalisé intraday** 2.244% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 62% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 262.1338 (VA 259.0288–263.3413 ; dernier close 257.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 44% · rebond 55% · **stop −1.51%** sous le fill (sous le bruit) · cible +1.15% · R/R 0.76 (high win-rate)
- Gaps overnight (n=159) : méd. -0.13% · baisse 58% (gap-down >1% 6% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.21% (p90 −1.5%) · haut méd +0.61% · range méd 1.05%
- Excursion ouverture 15min (n=160) : bas méd −0.27% (p90 −1.75%) · haut méd +0.82% · range méd 1.34%
- Excursion ouverture 30min (n=160) : bas méd −0.41% (p90 −1.76%) · haut méd +0.88% · range méd 1.52%
- Excursion ouverture 60min (n=160) : bas méd −0.46% (p90 −1.9%) · haut méd +0.95% · range méd 1.74%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 259.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 79% (121/159) · gap 24% · délai 0.7min · rebond 51% (66/121) (MFE +1.04%)
   - −1.0% : fill 30min 36% · séance 65% (101/159) · gap 6% · délai 12.4min · rebond 56% (58/101) (MFE +1.2%)
   - −1.5% : fill 30min 21% · séance 44% (76/159) · gap 2% · délai 48.3min · rebond 55% (43/76) (MFE +1.15%)
   - −2.0% : fill 30min 7% · séance 31% (56/159) · gap 0% · délai 221.7min · rebond 53% (29/56) (MFE +1.19%)
   - −3.0% : fill 30min 2% · séance 8% (25/159) · gap 0% · délai 116.8min · rebond 61% (12/25) (MFE +1.19%)
   - −4.0% : fill 30min 1% · séance 5% (13/159) · gap 0% · délai 55.4min · rebond 62% (8/13) (MFE +1.73%)
   - −5.0% : fill 30min 0% · séance 3% (7/159) · gap 0% · délai 141.9min · rebond 84% (6/7) (MFE +2.49%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.18% (p90 −1.59%) → stop au-delà de −1.0% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.07% (p90 −1.59%) → stop au-delà de −1.09% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.15% (p90 −1.99%) → stop au-delà de −1.15% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=439 jambes) : jambe baissière méd −1.03% (p90 −2.27%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (60 séances) :
      · −1.0% : fill 77% (48/60) · rebond 59% (29/48)
      · −2.0% : fill 34% (26/60) · rebond 54% (14/26)
      · −3.0% : fill 9% (14/60) · rebond 52% (7/14)
      · −4.0% : fill 6% (8/60) · rebond 60% (6/8)
      · −5.0% : fill 3% (4/60) · rebond 100% (4/4)
   - **flat** (41 séances) :
      · −1.0% : fill 61% (25/41) · rebond 53% (12/25)
      · −2.0% : fill 34% (16/41) · rebond 49% (7/16)
      · −3.0% : fill 6% (5/41) · rebond 34% (1/5)
      · −4.0% : fill 2% (2/41) · rebond 0% (0/2)
      · −5.0% : fill 2% (1/41) · rebond 0% (0/1)
   - **gap-up** (58 séances) :
      · −1.0% : fill 53% (28/58) · rebond 52% (17/28)
      · −2.0% : fill 24% (14/58) · rebond 59% (8/14)
      · −3.0% : fill 10% (6/58) · rebond 88% (4/6)
      · −4.0% : fill 6% (3/58) · rebond 89% (2/3)
      · −5.0% : fill 5% (2/58) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 56% si les 15 1res min sont vertes (89 cas) · 41% si rouges (71 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:32** → P(séance verte=clôture>ouverture) 63% si début vert vs 32% si rouge (base 50% · écart 31 pts) ; prédictivité sature ensuite (plafond brut 265min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **63%** · continue >prix actuel 45% ; creux résiduel méd -1.32% (q20 -2.41%) → **SL/trailing à −2.41%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.99% / q75 +1.85% → **scale +0.99% / runner +1.85%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **32%** (continue à baisser 44%) → **RÉDUIRE ~68%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.16%** (au-delà de la MAE q10 -2.16%), cible rebond +1.26% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.2% .. +2.03%] · haut q95 +2.53% · bas q05 -2.82%
   - 60min (n=160) : retour [-2.29% .. +2.34%] · haut q95 +2.77% · bas q05 -2.93%
   - 2h (n=160) : retour [-2.16% .. +2.27%] · haut q95 +2.94% · bas q05 -3.02%
   - 4h (n=160) : retour [-2.24% .. +2.47%] · haut q95 +3.13% · bas q05 -3.15%
   - 6h (n=160) : retour [-2.48% .. +2.89%] · haut q95 +3.6% · bas q05 -3.16%
   - session (n=160) : retour [-3.02% .. +4.45%] · haut q95 +5.21% · bas q05 -3.82%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.33%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.12 · part idiosyncratique 0.88
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 68.2  _(momentum haussier)_
- **ADX** : 24.3  _(pas de tendance nette)_
- **MACD** : hist 0.177  _(pas de croisement recent)_
- **BB** : %B 0.6 · largeur 18.4%
- **ATR** : 8.74 (52.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.057  _(accumulation)_
- **Vol ratio** : 1.13  _(volume normal)_
- **Choppiness** : 39.3  _(transition)_
- **MA** : MA20 247.02 · MA50 240.55 · MA200 233.33  _(prix > MA20)_
- **Dist MA** : MA20 +1.8% · MA50 +4.5% · MA200 +7.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (868531 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
