# IONQ

**Generated** : 2026-10-01T00:27:02.533678+00:00  
**Santé technique** : 8/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $43.87  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $43.87 (+4.6% vs entrée) · entrée $41.93 · stop $39.09 · T1 $45.21 · R/R 1.15  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.220 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._
- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : RSI 74.8 > 70 (surachat) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $41.58–$42.28 (mid $41.93)
- Spot actuel : $43.87 (+4.6% au-dessus de la zone — repli à attendre)
- Stop : $39.09 (plancher anti-bruit (R/R<2) ; -6.77 % depuis l'entree)
- Targets : T1 $45.21 · R/R 1.15 | T2 $48.38 · R/R 2.27 | T3 $51.55 · R/R 3.39
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $39.09


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=9.02 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.88 %)** : le gap seul le franchit 0.239 % des séances (3 fois sur 1253).
   - exécution **1.066 pt plus bas** dans le cas TYPIQUE (médiane), 8.997 au p90, **10.979 au pire**
   - perte réelle **15.082 %** en moyenne _(tirée par la queue)_, jusqu'à **21.859 %** — au lieu des 10.88 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0101 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.069 % | p01 -6.632 % | pire -21.859 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.531** [0.4567 ; 0.6043] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.5028** [0.4503 ; 0.5553] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4878** [0.4354 ; 0.5404] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : deep (26.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.53 %** | CVaR **-10.49 %** | vol 6.1 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 11.59 % contre 5.95 % aujourd'hui, rapport 1.95)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -17.62 % vs -19.81 % si l'on extrapolait par √5 _(rapport 0.89 ; < 1 = le √5 surestime)_
- **β de baisse : 2.215** (β de hausse 1.9963, asymétrie 1.1096) vs IWM — 605 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 39.2121 sur grid_snapped (1.34 ATR, 10.607 %) — p(stop avant cible) 0.5234 [0.47 ; 0.58], R/R 2.01, perte reelle 10.712 % (gap inclus), CVaR 11.705 %, EV 0.1603 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.3765 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.523, borne haute 0.576 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 9.696 %) — p(stop avant cible) 0.5851 [0.53 ; 0.64], R/R 2.201, perte reelle 9.785 % (gap inclus), EV -0.0737 % — **REFUSE**
      - refuse : p_stop_first 0.585, borne haute 0.636 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.07 %) : P(cible) 22.9 % x 21.54 % + P(rien) 18.6 % x 3.89 % ne couvrent pas P(stop) 58.5 % x 9.78 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ sr_based a 1.34 ATR (stop 11.693 %) — p(stop avant cible) 0.476 [0.42 ; 0.53], R/R 1.824, perte reelle 11.806 % (gap inclus), EV -0.0085 % — **REFUSE**
      - refuse : R/R 1.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.77 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.01 %) : P(cible) 24.1 % x 21.54 % + P(rien) 28.3 % x 1.50 % ne couvrent pas P(stop) 47.6 % x 11.81 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 3.42 ATR (stop 25.104 %) — p(stop avant cible) 0.0897 [0.06 ; 0.12], R/R 0.857, perte reelle 25.139 % (gap inclus), EV 0.5091 % — **REFUSE**
      - refuse : R/R 0.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.17 % > budget 12.00 %
   - 🟢 support a 4.89 ATR (stop 34.656 %) — p(stop avant cible) 0.0163 [0.01 ; 0.03], R/R 0.621, perte reelle 34.692 % (gap inclus), EV 0.466 % — **REFUSE**
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.26 % > budget 12.00 %
   - 🟢 support a 6.34 ATR (stop 44.003 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.489, perte reelle 44.003 % (gap inclus), EV 0.493 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.87 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.616 %) — p(stop avant cible) 0.9153 [0.88 ; 0.94], R/R 13.033, perte reelle 1.652 % (gap inclus), EV 0.1293 % — **REFUSE**
      - refuse : cible atteinte seulement 6.8 % du temps (< 15 %) meme a 10 seances : le R/R de 13.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.915, borne haute 0.941 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 3.232 %) — p(stop avant cible) 0.8419 [0.80 ; 0.88], R/R 6.43, perte reelle 3.349 % (gap inclus), EV 0.088 % — **REFUSE**
      - refuse : cible atteinte seulement 12.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.842, borne haute 0.877 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 4.848 %) — p(stop avant cible) 0.7894 [0.74 ; 0.83], R/R 4.328, perte reelle 4.976 % (gap inclus), EV -0.3611 % — **REFUSE**
      - refuse : cible atteinte seulement 14.3 % du temps (< 15 %) meme a 10 seances : le R/R de 4.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.789, borne haute 0.830 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 14.3 % x 21.54 % + P(rien) 6.8 % x 7.28 % ne couvrent pas P(stop) 78.9 % x 4.98 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 6.464 %) — p(stop avant cible) 0.7271 [0.68 ; 0.77], R/R 3.274, perte reelle 6.577 % (gap inclus), EV -0.3497 % — **REFUSE**
      - refuse : p_stop_first 0.727, borne haute 0.772 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.35 %) : P(cible) 18.0 % x 21.54 % + P(rien) 9.3 % x 5.94 % ne couvrent pas P(stop) 72.7 % x 6.58 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 1.34 ATR (stop 10.607 %) — p(stop avant cible) 0.5234 [0.47 ; 0.58], R/R 2.01, perte reelle 10.712 % (gap inclus), EV 0.1603 % — **REFUSE**
      - refuse : p_stop_first 0.523, borne haute 0.576 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 12.928 %) — p(stop avant cible) 0.4249 [0.37 ; 0.48], R/R 1.657, perte reelle 12.998 % (gap inclus), EV 0.0237 % — **REFUSE**
      - refuse : R/R 1.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.52 % > budget 12.00 %
   - ⚪ atr_grid a 2.25 ATR (stop 14.544 %) — p(stop avant cible) 0.3539 [0.30 ; 0.41], R/R 1.47, perte reelle 14.647 % (gap inclus), EV -0.1453 % — **REFUSE**
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.27 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 24.9 % x 21.54 % + P(rien) 39.7 % x -0.81 % ne couvrent pas P(stop) 35.4 % x 14.65 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 16.16 %) — p(stop avant cible) 0.2835 [0.24 ; 0.33], R/R 1.326, perte reelle 16.246 % (gap inclus), EV -0.0632 % — **REFUSE**
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.65 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.06 %) : P(cible) 25.1 % x 21.54 % + P(rien) 46.6 % x -1.83 % ne couvrent pas P(stop) 28.3 % x 16.25 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 17.776 %) — p(stop avant cible) 0.243 [0.20 ; 0.29], R/R 1.208, perte reelle 17.835 % (gap inclus), EV 0.1254 % — **REFUSE**
      - refuse : R/R 1.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.06 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 19.392 %) — p(stop avant cible) 0.197 [0.16 ; 0.24], R/R 1.104, perte reelle 19.503 % (gap inclus), EV 0.337 % — **REFUSE**
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.83 % > budget 12.00 %
   - 🟢 grid_snapped a 3.42 ATR (stop 24.018 %) — p(stop avant cible) 0.1017 [0.07 ; 0.14], R/R 0.896, perte reelle 24.044 % (gap inclus), EV 0.5532 % — **REFUSE**
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.07 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 29.088 %) — p(stop avant cible) 0.0624 [0.04 ; 0.09], R/R 0.738, perte reelle 29.19 % (gap inclus), EV 0.3517 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.22 % > budget 12.00 %
   - 🟢 grid_snapped a 4.89 ATR (stop 33.57 %) — p(stop avant cible) 0.0218 [0.01 ; 0.04], R/R 0.64, perte reelle 33.626 % (gap inclus), EV 0.4417 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.64 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 35.552 %) — p(stop avant cible) 0.0121 [0.00 ; 0.03], R/R 0.603, perte reelle 35.696 % (gap inclus), EV 0.4894 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.87 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 38.784 %) — p(stop avant cible) 0.0068 [0.00 ; 0.02], R/R 0.554, perte reelle 38.874 % (gap inclus), EV 0.4975 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.75 % > budget 12.00 %
   - 🟢 grid_snapped a 6.34 ATR (stop 42.917 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.502, perte reelle 42.92 % (gap inclus), EV 0.4947 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.83 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 45.248 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 0.476, perte reelle 45.248 % (gap inclus), EV 0.4933 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.86 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 48.48 %) — p(stop avant cible) 0.0005 [0.00 ; 0.01], R/R 0.444, perte reelle 48.485 % (gap inclus), EV 0.511 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.69 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 51.712 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.416, perte reelle 51.712 % (gap inclus), EV 0.5254 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.46 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 43.865, ATR14 2.8354 (6.464 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.378 ATR = 2.443 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.323 % | 43.7232 | 93.55 % | 95.36 % | 96.06 % | 97.47 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.646 % | 43.5815 | 85.8 % | 91.03 % | 92.13 % | 94.44 % | 95.83 % | 96.92 % |
| 0.15 ATR | 0.97 % | 43.4397 | 78.75 % | 85.99 % | 88.19 % | 91.51 % | 93.6 % | 95.69 % |
| 0.2 ATR | 1.293 % | 43.2979 | 71.2 % | 80.24 % | 84.16 % | 88.37 % | 90.85 % | 93.63 % |
| 0.25 ATR | 1.616 % | 43.1561 | 65.16 % | 76.11 % | 80.42 % | 85.64 % | 88.72 % | 92.09 % |
| 0.35 ATR | 2.262 % | 42.8726 | 52.77 % | 67.14 % | 73.66 % | 78.97 % | 84.04 % | 88.5 % |
| 0.5 ATR | 3.232 % | 42.4473 | 37.87 % | 54.13 % | 61.76 % | 70.68 % | 78.46 % | 84.5 % |
| 0.75 ATR | 4.848 % | 41.7384 | 22.46 % | 38.91 % | 48.03 % | 58.54 % | 69.0 % | 76.9 % |
| 1.0 ATR | 6.464 % | 41.0296 | 10.07 % | 24.29 % | 34.41 % | 45.5 % | 57.72 % | 68.28 % |
| 1.25 ATR | 8.08 % | 40.3207 | 3.83 % | 14.31 % | 23.92 % | 34.48 % | 49.9 % | 62.01 % |
| 1.5 ATR | 9.696 % | 39.6119 | 1.11 % | 7.06 % | 15.54 % | 25.28 % | 40.96 % | 56.26 % |
| 2.0 ATR | 12.928 % | 38.1941 | 0.1 % | 1.92 % | 4.94 % | 14.05 % | 28.05 % | 45.17 % |
| 2.5 ATR | 16.16 % | 36.7764 | 0.0 % | 0.2 % | 1.21 % | 5.66 % | 17.99 % | 34.19 % |
| 3.0 ATR | 19.392 % | 35.3587 | 0.0 % | 0.1 % | 0.4 % | 2.53 % | 11.28 % | 25.87 % |
| 4.0 ATR | 25.856 % | 32.5233 | 0.0 % | 0.1 % | 0.1 % | 0.2 % | 2.95 % | 10.57 % |
| 6.0 ATR | 38.784 % | 26.8524 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.1 % | 1.23 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.38 ATR | 0.43 ATR | 0.58 ATR | 0.71 ATR | 0.80 ATR | 1.00 ATR | 1.20 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.65 ATR | 0.85 ATR | 0.99 ATR | 1.11 ATR | 1.40 ATR | 1.70 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.81 ATR | 1.03 ATR | 1.22 ATR | 1.37 ATR | 1.76 ATR | 2.00 ATR |
| **5 s.** | 0.42 ATR | 0.91 ATR | 1.01 ATR | 1.29 ATR | 1.51 ATR | 1.74 ATR | 2.24 ATR | 2.60 ATR |
| **10 s.** | 0.59 ATR | 1.25 ATR | 1.39 ATR | 1.81 ATR | 2.15 ATR | 2.40 ATR | 3.15 ATR | 3.75 ATR |
| **20 s.** | 0.81 ATR | 1.78 ATR | 2.01 ATR | 2.57 ATR | 3.06 ATR | 3.38 ATR | 4.12 ATR | 5.19 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.428–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.65–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.848 %, prix 41.7384), p(touche) 38.91 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.806–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.464 %, prix 41.0296), p(touche) 34.41 % (en stress 92.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.011–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.08 %, prix 40.3207), p(touche) 34.48 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.387–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.696 %, prix 39.6119), p(touche) 40.96 % (en stress 97.98 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.008–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (16.16 %, prix 36.7764), p(touche) 34.19 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (65.5 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.009 | EV/share : $-0.026 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 18 % | T3 8 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 71.4 | bear 8.8 | side 19.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 581.0 (= 15 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.001% → cible +3.298% / stop −1.979%, p_fill 57%, n_eff≈64.3) : P(cible|rempli) **23%** · **EV/risk -0.120** (×p_fill ; si rempli -0.42% du capital)
  - **swing** (entrée dip −4.416% → cible +7.814% / stop −6.763%, p_fill 51%, n_eff≈60.8) : P(cible|rempli) **42%** · **EV/risk -0.046** (×p_fill ; si rempli -0.61% du capital)
  - **deep** (entrée dip −6.814% → cible +10.599% / stop −10.405%, p_fill 46%, n_eff≈53.4) : P(cible|rempli) **41%** · **EV/risk -0.078** (×p_fill ; si rempli -1.74% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→80% · +2.0%→64% · +3.0%→55% · +5.0%→28% · +8.0%→14%
- Range intraday médian 7.06% (p90 11.57%) · excursion haute méd. +3.57% / basse méd. −2.49%
- Profil de vol intra : ouverture 4.837% vs midi 1.386% vs clôture 1.548% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 22% · trend ↑0%/↓0% ; spike-down 63% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; neutre — autocorr 0.003)_ ; drift intra méd. -0.07% ; recovery-V 28%
- **σ réalisé intraday** 4.09% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 55% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 44.0647 (VA 43.9617–44.2707 ; dernier close 43.89)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 26% · rebond 78% · **stop −4.36%** sous le fill (sous le bruit) · cible +2.2% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. -0.18% · baisse 51% (gap-down >1% 36% · >2% 22%)
- Excursion ouverture 5min (n=160) : bas méd −1.04% (p90 −2.74%) · haut méd +1.32% · range méd 2.6%
- Excursion ouverture 15min (n=160) : bas méd −1.2% (p90 −3.96%) · haut méd +1.49% · range méd 3.38%
- Excursion ouverture 30min (n=160) : bas méd −1.44% (p90 −5.0%) · haut méd +1.82% · range méd 4.19%
- Excursion ouverture 60min (n=160) : bas méd −1.71% (p90 −5.39%) · haut méd +2.02% · range méd 4.69%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 43.91 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 76% (127/159) · gap 46% · délai 0.0min · rebond 61% (83/127) (MFE +1.81%)
   - −1.0% : fill 30min 64% · séance 73% (121/159) · gap 36% · délai 0.0min · rebond 68% (86/121) (MFE +2.02%)
   - −1.5% : fill 30min 56% · séance 67% (113/159) · gap 32% · délai 0.0min · rebond 69% (77/113) (MFE +2.09%)
   - −2.0% : fill 30min 49% · séance 57% (102/159) · gap 22% · délai 0.0min · rebond 69% (71/102) (MFE +2.13%)
   - −3.0% : fill 30min 39% · séance 45% (83/159) · gap 10% · délai 4.1min · rebond 70% (60/83) (MFE +2.38%)
   - −4.0% : fill 30min 23% · séance 35% (66/159) · gap 4% · délai 15.5min · rebond 68% (48/66) (MFE +2.2%)
   - −5.0% : fill 30min 11% · séance 26% (52/159) · gap 1% · délai 32.1min · rebond 78% (42/52) (MFE +2.2%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.75% (p90 −2.64%) → stop au-delà de −1.86% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.75% (p90 −2.65%) → stop au-delà de −1.77% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.69% (p90 −2.36%) → stop au-delà de −1.32% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1061 jambes) : jambe baissière méd −1.26% (p90 −2.97%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (80 séances) :
      · −1.0% : fill 100% (80/80) · rebond 69% (56/80)
      · −2.0% : fill 87% (73/80) · rebond 75% (54/73)
      · −3.0% : fill 72% (61/80) · rebond 72% (44/61)
      · −4.0% : fill 54% (47/80) · rebond 67% (34/47)
      · −5.0% : fill 38% (37/80) · rebond 70% (28/37)
   - **flat** (15 séances) :
      · −1.0% : fill 74% (11/15) · rebond 83% (9/11)
      · −2.0% : fill 52% (9/15) · rebond 88% (6/9)
      · −3.0% : fill 33% (6/15) · rebond 65% (5/6)
      · −4.0% : fill 28% (5/15) · rebond 55% (3/5)
      · −5.0% : fill 20% (4/15) · rebond 94% (3/4)
   - **gap-up** (64 séances) :
      · −1.0% : fill 40% (30/64) · rebond 62% (21/30)
      · −2.0% : fill 24% (20/64) · rebond 32% (11/20)
      · −3.0% : fill 17% (16/64) · rebond 59% (11/16)
      · −4.0% : fill 15% (14/64) · rebond 83% (11/14)
      · −5.0% : fill 13% (11/64) · rebond 100% (11/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 60% si les 15 1res min sont vertes (89 cas) · 28% si rouges (71 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **56min** → P(séance verte=clôture>ouverture) 67% si début vert vs 20% si rouge (base 46% · écart 47 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=85) : tient le vert **67%** · continue >prix actuel 41% ; creux résiduel méd -1.75% (q20 -3.89%) → **SL/trailing à −3.89%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.64% / q75 +3.36% → **scale +1.64% / runner +3.36%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **20%** (continue à baisser 57%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.33%** (au-delà de la MAE q10 -4.33%), cible rebond +2.06% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.24% .. +5.59%] · haut q95 +7.58% · bas q05 -5.55%
   - 60min (n=160) : retour [-5.58% .. +5.95%] · haut q95 +7.84% · bas q05 -6.76%
   - 2h (n=160) : retour [-6.38% .. +5.95%] · haut q95 +8.14% · bas q05 -7.07%
   - 4h (n=160) : retour [-6.77% .. +6.88%] · haut q95 +8.88% · bas q05 -8.07%
   - 6h (n=160) : retour [-6.66% .. +7.27%] · haut q95 +9.82% · bas q05 -8.06%
   - session (n=160) : retour [-6.42% .. +8.16%] · haut q95 +9.87% · bas q05 -8.23%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 7.5% des séances sont trend-up (mild 0% / strong 7.5%) · base = 12 séances trend-up (n_eff 7.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **35%**. Lecture précoce 30 min : signature présente → 14% vs absente 5% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.3% (p75 2.44% / p90 3.18%) · ~4.0 replis/séance, durée méd 70.31 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 30.0 min, n=48)
   - −1.0% → **77%** (reprise méd 34.75 min, n=35)
   - −1.5% → **67%** (reprise méd 44.94 min, n=18)
   - −2.0% → **61%** (reprise méd 64.1 min, n=13)
   - −3.0% → **74%** (reprise méd 175.76 min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−3.18%** (p90, défaut prudent ; serré/agressif −2.44%) ; extension open→close méd +8.16% (q75 +8.39% / q95 +13.57%), MFE méd +9.48% / q90 +12.4%
   - Échelle scale-out : +9.48% (33%) / +10.45% (33%) / +12.4% (34%)
- **DÉSARMER** : repli > **−3.18%** depuis le plus-haut = décay → P(retournement) **26%** (préavis méd 167.77 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.4% : P(retournement après) 0% (mèche méd 2.07%)
- **CONTEXTE** : la dernière heure tient les gains 70% du temps (retour médian dernière heure +0.1%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.52 · part idiosyncratique 0.48
**Short/Insider** : SI —% | insider — | verdict sell_bias_modere
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 74.8  _(surachat)_
- **ADX** : 19.9  _(pas de tendance nette)_
- **MACD** : hist 0.706  _(pas de croisement recent)_
- **BB** : %B 0.8 · largeur 29.6%
- **ATR** : 2.84 (24.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.219  _(distribution)_
- **Vol ratio** : 0.97  _(volume normal)_
- **Choppiness** : 42.6  _(transition)_
- **MA** : MA20 40.29 · MA50 40.22 · MA200 43.5  _(prix > MA20)_
- **Dist MA** : MA20 +8.9% · MA50 +9.1% · MA200 +0.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (854801 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
