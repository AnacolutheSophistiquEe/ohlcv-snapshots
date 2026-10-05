# PLTR

**Generated** : 2026-10-05T00:26:07.624557+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 10/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $188.75  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 7/121 fenêtres (p_fill pondéré 5 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot $188.75 (+8.9% vs entrée) · entrée $173.36 · stop $167.61 · T1 $179.78 · R/R 1.12  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : divergent_short_long (score 1)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 10/10 élevée alors que : RSI 75.1 > 70 (surachat) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 10/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $172.50–$174.22 (mid $173.36)
- Spot actuel : $188.75 (+8.9% au-dessus de la zone — repli à attendre)
- Stop : $167.61 (plancher anti-bruit (R/R<2) ; -3.32 % depuis l'entree)
- Targets : T1 $179.78 · R/R 1.12 | T2 $186.21 · R/R 2.23 | T3 $192.63 · R/R 3.35
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $167.61


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.71 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (11.2 %)** : le gap seul le franchit 0.399 % des séances (5 fois sur 1254).
   - exécution **1.573 pt plus bas** dans le cas TYPIQUE (médiane), 5.428 au p90, **6.732 au pire**
   - perte réelle **13.763 %** en moyenne _(tirée par la queue)_, jusqu'à **17.932 %** — au lieu des 11.2 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0102 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.86 % | p01 -6.138 % | pire -17.932 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2407** [0.1817 ; 0.3083] _(largeur 12.7 pt, n_eff 173.1)_
   - swing : **0.4842** [0.4318 ; 0.5368] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4335** [0.382 ; 0.4861] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (44.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.14 %** | CVaR **-8.41 %** | vol 4.26 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.3 % vs -13.73 % si l'on extrapolait par √5 _(rapport 0.968 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6859** (β de hausse 1.4221, asymétrie 1.1854) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.77× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 187.3135 sur atr_grid (0.25 ATR, 0.761 %) — p(stop avant cible) 0.6788 [0.63 ; 0.73], R/R 2.692, perte reelle 0.764 % (gap inclus), CVaR 0.8 %, EV 0.1419 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.4235 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.679, borne haute 0.726 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.89 ATR (stop 4.407 %) — p(stop avant cible) 0.3267 [0.28 ; 0.38], R/R 0.46, perte reelle 4.468 % (gap inclus), EV -0.0752 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.08 %) : P(cible) 67.3 % x 2.06 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 32.7 % x 4.47 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ sr_based a 4.97 ATR (stop 16.842 %) — p(stop avant cible) 0.0523 [0.03 ; 0.08], R/R 0.121, perte reelle 17.034 % (gap inclus), EV 0.0779 % — **REFUSE**
      - refuse : R/R 0.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.04 % > budget 12.00 %
   - 🟢 support a 7.17 ATR (stop 23.533 %) — p(stop avant cible) 0.0082 [0.00 ; 0.02], R/R 0.086, perte reelle 23.876 % (gap inclus), EV 0.2455 % — **REFUSE**
      - refuse : R/R 0.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.95 % > budget 12.00 %
   - 🟢 support a 12.33 ATR (stop 39.253 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.052, perte reelle 39.352 % (gap inclus), EV 0.2991 % — **REFUSE**
      - refuse : R/R 0.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.08 % > budget 12.00 %
   - 🟢 support a 14.34 ATR (stop 45.356 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.045, perte reelle 45.356 % (gap inclus), EV 0.2989 % — **REFUSE**
      - refuse : R/R 0.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.08 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.761 %) — p(stop avant cible) 0.6788 [0.63 ; 0.73], R/R 2.692, perte reelle 0.764 % (gap inclus), EV 0.1419 % — **REFUSE**
      - refuse : p_stop_first 0.679, borne haute 0.726 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 0.5 ATR (stop 1.522 %) — p(stop avant cible) 0.5596 [0.51 ; 0.61], R/R 1.348, perte reelle 1.525 % (gap inclus), EV 0.052 % — **REFUSE**
      - refuse : p_stop_first 0.560, borne haute 0.611 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 0.89 ATR (stop 3.61 %) — p(stop avant cible) 0.3739 [0.32 ; 0.43], R/R 0.556, perte reelle 3.695 % (gap inclus), EV -0.0944 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.09 %) : P(cible) 62.6 % x 2.06 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 37.4 % x 3.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 5.327 %) — p(stop avant cible) 0.2629 [0.22 ; 0.31], R/R 0.381, perte reelle 5.393 % (gap inclus), EV 0.0776 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 6.088 %) — p(stop avant cible) 0.2337 [0.19 ; 0.28], R/R 0.334, perte reelle 6.161 % (gap inclus), EV 0.1087 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 6.849 %) — p(stop avant cible) 0.1983 [0.16 ; 0.24], R/R 0.297, perte reelle 6.928 % (gap inclus), EV 0.2474 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 7.61 %) — p(stop avant cible) 0.1882 [0.15 ; 0.23], R/R 0.268, perte reelle 7.669 % (gap inclus), EV 0.1926 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 8.371 %) — p(stop avant cible) 0.176 [0.14 ; 0.22], R/R 0.244, perte reelle 8.419 % (gap inclus), EV 0.16 % — **REFUSE**
      - refuse : R/R 0.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 9.132 %) — p(stop avant cible) 0.1628 [0.13 ; 0.20], R/R 0.223, perte reelle 9.202 % (gap inclus), EV 0.1222 % — **REFUSE**
      - refuse : R/R 0.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 10.655 %) — p(stop avant cible) 0.1432 [0.11 ; 0.18], R/R 0.191, perte reelle 10.759 % (gap inclus), EV 0.0269 % — **REFUSE**
      - refuse : R/R 0.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 12.177 %) — p(stop avant cible) 0.1008 [0.07 ; 0.14], R/R 0.167, perte reelle 12.308 % (gap inclus), EV 0.1475 % — **REFUSE**
      - refuse : R/R 0.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.44 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 13.699 %) — p(stop avant cible) 0.0781 [0.05 ; 0.11], R/R 0.147, perte reelle 13.972 % (gap inclus), EV 0.0753 % — **REFUSE**
      - refuse : R/R 0.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.12 % > budget 12.00 %
   - ⚪ grid_snapped a 4.97 ATR (stop 16.045 %) — p(stop avant cible) 0.0524 [0.03 ; 0.08], R/R 0.127, perte reelle 16.244 % (gap inclus), EV 0.1192 % — **REFUSE**
      - refuse : R/R 0.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.25 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 18.265 %) — p(stop avant cible) 0.0503 [0.03 ; 0.08], R/R 0.112, perte reelle 18.374 % (gap inclus), EV 0.0295 % — **REFUSE**
      - refuse : R/R 0.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.38 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 19.787 %) — p(stop avant cible) 0.03 [0.02 ; 0.05], R/R 0.103, perte reelle 19.972 % (gap inclus), EV 0.1254 % — **REFUSE**
      - refuse : R/R 0.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.75 % > budget 12.00 %
   - 🟢 grid_snapped a 7.17 ATR (stop 22.736 %) — p(stop avant cible) 0.0131 [0.00 ; 0.03], R/R 0.089, perte reelle 23.045 % (gap inclus), EV 0.2172 % — **REFUSE**
      - refuse : R/R 0.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.43 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 24.353 %) — p(stop avant cible) 0.0048 [0.00 ; 0.02], R/R 0.083, perte reelle 24.71 % (gap inclus), EV 0.2623 % — **REFUSE**
      - refuse : R/R 0.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.61 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 188.75, ATR14 5.7459 (3.044 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.358 ATR = 1.09 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.152 % | 188.4627 | 92.66 % | 95.17 % | 95.97 % | 96.77 % | 98.07 % | 98.67 % |
| 0.1 ATR | 0.304 % | 188.1754 | 84.71 % | 89.33 % | 91.23 % | 93.43 % | 95.03 % | 96.41 % |
| 0.15 ATR | 0.457 % | 187.8881 | 77.06 % | 83.69 % | 85.99 % | 89.8 % | 92.39 % | 94.26 % |
| 0.2 ATR | 0.609 % | 187.6008 | 69.01 % | 78.25 % | 81.75 % | 86.36 % | 90.15 % | 92.51 % |
| 0.25 ATR | 0.761 % | 187.3135 | 62.07 % | 73.41 % | 77.52 % | 82.93 % | 87.72 % | 90.97 % |
| 0.35 ATR | 1.065 % | 186.7389 | 50.8 % | 65.26 % | 70.97 % | 78.08 % | 83.65 % | 88.0 % |
| 0.5 ATR | 1.522 % | 185.8771 | 35.92 % | 52.47 % | 59.48 % | 68.89 % | 77.77 % | 83.49 % |
| 0.75 ATR | 2.283 % | 184.4406 | 19.42 % | 35.05 % | 44.46 % | 55.25 % | 66.7 % | 76.31 % |
| 1.0 ATR | 3.044 % | 183.0041 | 8.95 % | 22.76 % | 32.36 % | 43.74 % | 56.14 % | 67.38 % |
| 1.25 ATR | 3.805 % | 181.5677 | 4.43 % | 15.31 % | 23.19 % | 34.04 % | 46.29 % | 58.46 % |
| 1.5 ATR | 4.566 % | 180.1312 | 2.11 % | 10.47 % | 17.34 % | 26.57 % | 39.8 % | 53.95 % |
| 2.0 ATR | 6.088 % | 177.2583 | 0.6 % | 3.73 % | 9.38 % | 15.76 % | 29.04 % | 40.41 % |
| 2.5 ATR | 7.61 % | 174.3854 | 0.1 % | 1.51 % | 3.33 % | 9.29 % | 19.39 % | 30.26 % |
| 3.0 ATR | 9.132 % | 171.5124 | 0.0 % | 0.6 % | 1.51 % | 4.75 % | 12.89 % | 22.56 % |
| 4.0 ATR | 12.177 % | 165.7666 | 0.0 % | 0.0 % | 0.3 % | 1.52 % | 4.67 % | 11.79 % |
| 6.0 ATR | 18.265 % | 154.2749 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.51 % | 3.59 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.36 ATR | 0.41 ATR | 0.54 ATR | 0.67 ATR | 0.74 ATR | 0.97 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.61 ATR | 0.79 ATR | 0.95 ATR | 1.09 ATR | 1.53 ATR | 1.91 ATR |
| **3 s.** | 0.29 ATR | 0.66 ATR | 0.74 ATR | 0.99 ATR | 1.20 ATR | 1.39 ATR | 1.96 ATR | 2.36 ATR |
| **5 s.** | 0.40 ATR | 0.86 ATR | 0.97 ATR | 1.28 ATR | 1.57 ATR | 1.80 ATR | 2.44 ATR | 2.97 ATR |
| **10 s.** | 0.56 ATR | 1.16 ATR | 1.30 ATR | 1.82 ATR | 2.21 ATR | 2.47 ATR | 3.35 ATR | 3.96 ATR |
| **20 s.** | 0.79 ATR | 1.65 ATR | 1.83 ATR | 2.37 ATR | 2.84 ATR | 3.24 ATR | 4.44 ATR | 5.66 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.408–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.522 %, prix 185.8772), p(touche) 35.92 % (en stress 81.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.607–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.283 %, prix 184.4408), p(touche) 35.05 % (en stress 94.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.741–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.283 %, prix 184.4408), p(touche) 44.46 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.973–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.044 %, prix 183.0044), p(touche) 43.74 % (en stress 100.0 %)  ✅ optimum identifie (81.5 % des re-echantillons)
- **10 seance(s)** : plage utile 1.3–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (4.566 %, prix 180.1317), p(touche) 39.8 % (en stress 100.0 %)  ✅ optimum identifie (86.6 % des re-echantillons)
- **20 seance(s)** : plage utile 1.831–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (9.132 %, prix 171.5134), p(touche) 22.56 % (en stress 94.9 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (97.2 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.012 | EV/share : $-0.067 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 45 % | T2 24 % | T3 11 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 44.2 | bear 14.6 | side 41.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 503.0 (= 3 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈60.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.703% → cible +1.581% / stop −2.5%, p_fill 11%, n_eff≈16.2) : P(cible|rempli) **31%** · **EV/risk -0.022** (×p_fill ; si rempli -0.48% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=7, n_eff=7))
  - **deep** : indisponible (échantillon insuffisant (n=6, n_eff=6))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→73% · +2.0%→44% · +3.0%→24% · +5.0%→9% · +8.0%→2%
- Range intraday médian 3.72% (p90 6.89%) · excursion haute méd. +1.85% / basse méd. −1.67%
- Profil de vol intra : ouverture 2.899% vs midi 0.725% vs clôture 0.809% _(ouverture ~4.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (157 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 79% · range 20% · trend ↑1%/↓0% ; spike-down 55% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.112 ; neutre — autocorr -0.02)_ ; drift intra méd. 0.326% ; recovery-V 29%
- **σ réalisé intraday** 2.336% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 40% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 189.3098 (VA 188.5023–190.9247 ; dernier close 188.79)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 44% · rebond 70% · **stop −3.61%** sous le fill (sous le bruit) · cible +1.61% · R/R 0.45 (high win-rate)
- Gaps overnight (n=156) : méd. -0.06% · baisse 51% (gap-down >1% 29% · >2% 6%)
- Excursion ouverture 5min (n=157) : bas méd −0.81% (p90 −1.9%) · haut méd +0.74% · range méd 1.73%
- Excursion ouverture 15min (n=157) : bas méd −1.0% (p90 −2.43%) · haut méd +0.97% · range méd 2.2%
- Excursion ouverture 30min (n=157) : bas méd −1.11% (p90 −2.9%) · haut méd +1.17% · range méd 2.56%
- Excursion ouverture 60min (n=157) : bas méd −1.33% (p90 −3.06%) · haut méd +1.29% · range méd 2.76%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 188.75 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 75% (117/156) · gap 38% · délai 0.0min · rebond 61% (67/117) (MFE +1.35%)
   - −1.0% : fill 30min 55% · séance 62% (103/156) · gap 29% · délai 0.0min · rebond 66% (60/103) (MFE +1.43%)
   - −1.5% : fill 30min 42% · séance 50% (86/156) · gap 17% · délai 0.1min · rebond 64% (52/86) (MFE +1.42%)
   - −2.0% : fill 30min 35% · séance 44% (77/156) · gap 6% · délai 1.5min · rebond 70% (49/77) (MFE +1.61%)
   - −3.0% : fill 30min 16% · séance 23% (50/156) · gap 3% · délai 6.1min · rebond 53% (23/50) (MFE +1.19%)
   - −4.0% : fill 30min 10% · séance 15% (34/156) · gap 2% · délai 15.4min · rebond 52% (16/34) (MFE +1.04%)
   - −5.0% : fill 30min 4% · séance 10% (23/156) · gap 0% · délai 45.3min · rebond 48% (12/23) (MFE +0.93%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.48% (p90 −1.9%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.69% (p90 −1.84%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.56% (p90 −1.57%) → stop au-delà de −1.02% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=515 jambes) : jambe baissière méd −1.06% (p90 −2.33%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 91% (70/75) · rebond 63% (41/70)
      · −2.0% : fill 75% (57/75) · rebond 72% (36/57)
      · −3.0% : fill 42% (38/75) · rebond 52% (18/38)
      · −4.0% : fill 29% (27/75) · rebond 54% (13/27)
      · −5.0% : fill 19% (19/75) · rebond 53% (11/19)
   - **flat** (23 séances) :
      · −1.0% : fill 78% (19/23) · rebond 58% (9/19)
      · −2.0% : fill 45% (13/23) · rebond 61% (8/13)
      · −3.0% : fill 24% (9/23) · rebond 54% (4/9)
      · −4.0% : fill 15% (6/23) · rebond 43% (3/6)
      · −5.0% : fill 8% (3/23) · rebond 13% (1/3)
   - **gap-up** (58 séances) :
      · −1.0% : fill 25% (14/58) · rebond 85% (10/14)
      · −2.0% : fill 12% (7/58) · rebond 67% (5/7)
      · −3.0% : fill 3% (3/58) · rebond 66% (1/3)
      · −4.0% : fill 1% (1/58) · rebond 0% (0/1)
      · −5.0% : fill 1% (1/58) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=157) : 51% en base · 71% si les 15 1res min sont vertes (80 cas) · 29% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=157) : COUDE à **1:41** → P(séance verte=clôture>ouverture) 86% si début vert vs 15% si rouge (base 51% · écart 70 pts) ; prédictivité sature ensuite (plafond brut 230min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **86%** · continue >prix actuel 55% ; creux résiduel méd -0.8% (q20 -1.44%) → **SL/trailing à −1.44%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.07% / q75 +2.11% → **scale +1.07% / runner +2.11%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **15%** (continue à baisser 51%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.53%** (au-delà de la MAE q10 -2.53%), cible rebond +1.05% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=157) : retour [-2.87% .. +3.73%] · haut q95 +4.0% · bas q05 -3.52%
   - 60min (n=157) : retour [-3.01% .. +3.93%] · haut q95 +4.71% · bas q05 -3.64%
   - 2h (n=157) : retour [-3.61% .. +5.08%] · haut q95 +5.27% · bas q05 -4.46%
   - 4h (n=157) : retour [-3.99% .. +5.64%] · haut q95 +6.27% · bas q05 -5.01%
   - 6h (n=157) : retour [-4.0% .. +5.46%] · haut q95 +6.81% · bas q05 -5.37%
   - session (n=157) : retour [-3.98% .. +4.77%] · haut q95 +6.81% · bas q05 -5.37%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.7% des séances sont trend-up (mild 1.3% / strong 4.5%) · base = 9 séances trend-up (n_eff 7.0)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **26%**. Lecture précoce 30 min : signature présente → 13% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.91% (p75 1.39% / p90 1.52%) · ~2.0 replis/séance, durée méd 77.38 min. P(nouveau plus-haut après repli) :
   - −0.5% → **78%** (reprise méd 47.34 min, n=25)
   - −1.0% → **51%** (reprise méd 65.0 min, n=11)
   - −1.5% → **18%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.52%** (p90, défaut prudent ; serré/agressif −1.39%) ; extension open→close méd +4.55% (q75 +7.54% / q95 +12.13%), MFE méd +6.21% / q90 +12.4%
   - Échelle scale-out : +6.21% (33%) / +8.19% (33%) / +12.4% (34%)
- **DÉSARMER** : repli > **−1.52%** depuis le plus-haut = décay → P(retournement) **65%** (préavis méd 99.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.4% : P(retournement après) 0% (mèche méd 1.36%)
- **CONTEXTE** : la dernière heure tient les gains 53% du temps (retour médian dernière heure +0.12%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.61 · part idiosyncratique 0.39
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 75.1  _(surachat)_
- **ADX** : 27.5  _(tendance etablie)_
- **MACD** : hist 0.061  _(pas de croisement recent)_
- **BB** : %B 0.74 · largeur 19.8%
- **ATR** : 5.75 (5.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.092  _(accumulation)_
- **Vol ratio** : 0.77  _(volume normal)_
- **Choppiness** : 43.1  _(transition)_
- **MA** : MA20 180.19 · MA50 169.78 · MA200 152.1  _(prix > MA20)_
- **Dist MA** : MA20 +4.8% · MA50 +11.2% · MA200 +24.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (837223 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
