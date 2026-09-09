# SOI

**Generated** : 2026-09-09T00:15:20.051979+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 9/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €145.90  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot €145.90 (+4.0% vs entrée) · entrée €140.32 · stop €132.68 · T1 €150.36 · R/R 1.31  
> ↳ P(T1 av. stop) 45 % _(réel 5 s)_ · EV/risk 0.009 _(réel 5 s)_ (GBM 0.293) · ¼-Kelly 0.031 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 516 % hors [0,100] (R² max 0.64). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 19.1 < 20 (tendance pas encore confirmée) alors que Choppiness 36.9 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._
- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.210 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._
- 🔴 **Santé haussière vs sur-extension** — Santé technique 9/10 élevée alors que : RSI 82.6 > 70 (surachat) ; %B 1.02 (collé à la bande haute) ; extension extrême (≥3×ATR, confluence MA20/50) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €138.31–€142.33 (mid €140.32)
- Spot actuel : €145.90 (+4.0% au-dessus de la zone — repli à attendre)
- Stop : €132.68 (stop swing_plan-based (-9.06%))
- Targets : T1 €150.36 · R/R 1.31 | T2 €160.40 · R/R 2.63 | T3 €170.44 · R/R 3.94
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €132.68


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.83 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.06 %)** : le gap seul le franchit 0.391 % des séances (5 fois sur 1280).
   - exécution **7.296 pt plus bas** dans le cas TYPIQUE (médiane), 16.004 au p90, **20.234 au pire**
   - perte réelle **16.593 %** en moyenne _(tirée par la queue)_, jusqu'à **29.294 %** — au lieu des 9.06 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0294 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.584 % | p01 -4.832 % | pire -29.294 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4075** [0.3363 ; 0.4817] _(largeur 14.5 pt, n_eff 173.1)_
   - swing : **0.4313** [0.3799 ; 0.4839] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4687** [0.4165 ; 0.5214] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 24.8 observations effectives », dont la borne haute a 95 % vaut environ 12.1 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (36.0 pt), swing (40.0 pt), deep (36.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.63 %** | CVaR **-13.66 %** | vol 6.55 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 2.95 % contre 7.50 % aujourd'hui, rapport 0.39)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.22 % vs -11.25 % si l'on extrapolait par √5 _(rapport 1.086 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1332** (β de hausse 1.5825, asymétrie 0.7161) vs FCHI — 618 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut -0.011× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 130.6286 sur atr_grid (2.0 ATR, 10.467 %) — p(stop avant cible) 0.4341 [0.38 ; 0.49], R/R 0.784, perte reelle 21.456 % (gap inclus), CVaR 10.493 %, EV -4.2209 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 7.85 %) — p(stop avant cible) 0.5402 [0.49 ; 0.59], R/R 1.098, perte reelle 15.318 % (gap inclus), EV -3.4624 % — **REFUSE**
      - refuse : p_stop_first 0.540, borne haute 0.592 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.46 %) : P(cible) 26.3 % x 16.82 % + P(rien) 19.7 % x 2.01 % ne couvrent pas P(stop) 54.0 % x 15.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.38 ATR (stop 9.526 %) — p(stop avant cible) 0.4684 [0.42 ; 0.52], R/R 0.784, perte reelle 21.456 % (gap inclus), EV -5.0193 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.02 %) : P(cible) 28.6 % x 16.82 % + P(rien) 24.5 % x 0.89 % ne couvrent pas P(stop) 46.8 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.34 ATR (stop 14.598 %) — p(stop avant cible) 0.2985 [0.25 ; 0.35], R/R 0.784, perte reelle 21.456 % (gap inclus), EV -1.5972 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.61 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.60 %) : P(cible) 32.8 % x 16.82 % + P(rien) 37.4 % x -1.90 % ne couvrent pas P(stop) 29.8 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.78 ATR (stop 22.137 %) — p(stop avant cible) 0.1014 [0.07 ; 0.14], R/R 0.574, perte reelle 29.294 % (gap inclus), EV 0.5312 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.14 % > budget 12.00 %
   - ⚪ swing_based a 5.22 ATR (stop 29.661 %) — p(stop avant cible) 0.0318 [0.02 ; 0.05], R/R 0.567, perte reelle 29.661 % (gap inclus), EV 1.4653 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.66 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.308 %) — p(stop avant cible) 0.8905 [0.85 ; 0.92], R/R 5.819, perte reelle 2.89 % (gap inclus), EV -0.9745 % — **REFUSE**
      - refuse : cible atteinte seulement 8.8 % du temps (< 15 %) meme a 10 seances : le R/R de 5.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.890, borne haute 0.920 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.97 %) : P(cible) 8.8 % x 16.82 % + P(rien) 2.1 % x 5.49 % ne couvrent pas P(stop) 89.0 % x 2.89 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.617 %) — p(stop avant cible) 0.7976 [0.75 ; 0.84], R/R 3.47, perte reelle 4.847 % (gap inclus), EV -0.9441 % — **REFUSE**
      - refuse : p_stop_first 0.798, borne haute 0.837 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.94 %) : P(cible) 15.8 % x 16.82 % + P(rien) 4.5 % x 6.01 % ne couvrent pas P(stop) 79.8 % x 4.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 3.925 %) — p(stop avant cible) 0.7179 [0.67 ; 0.76], R/R 2.345, perte reelle 7.172 % (gap inclus), EV -1.4495 % — **REFUSE**
      - refuse : p_stop_first 0.718, borne haute 0.763 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.45 %) : P(cible) 19.9 % x 16.82 % + P(rien) 8.4 % x 4.31 % ne couvrent pas P(stop) 71.8 % x 7.17 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 5.234 %) — p(stop avant cible) 0.6452 [0.59 ; 0.69], R/R 1.505, perte reelle 11.172 % (gap inclus), EV -2.8376 % — **REFUSE**
      - refuse : p_stop_first 0.645, borne haute 0.694 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.84 %) : P(cible) 23.2 % x 16.82 % + P(rien) 12.3 % x 3.85 % ne couvrent pas P(stop) 64.5 % x 11.17 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 1.38 ATR (stop 8.767 %) — p(stop avant cible) 0.5072 [0.45 ; 0.56], R/R 1.098, perte reelle 15.318 % (gap inclus), EV -2.8921 % — **REFUSE**
      - refuse : p_stop_first 0.507, borne haute 0.560 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.89 %) : P(cible) 27.2 % x 16.82 % + P(rien) 22.1 % x 1.39 % ne couvrent pas P(stop) 50.7 % x 15.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 10.467 %) — p(stop avant cible) 0.4341 [0.38 ; 0.49], R/R 0.784, perte reelle 21.456 % (gap inclus), EV -4.2209 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.22 %) : P(cible) 29.9 % x 16.82 % + P(rien) 26.7 % x 0.26 % ne couvrent pas P(stop) 43.4 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 2.34 ATR (stop 13.839 %) — p(stop avant cible) 0.3218 [0.27 ; 0.37], R/R 0.784, perte reelle 21.456 % (gap inclus), EV -1.9445 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.86 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.94 %) : P(cible) 32.8 % x 16.82 % + P(rien) 35.0 % x -1.59 % ne couvrent pas P(stop) 32.2 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 15.701 %) — p(stop avant cible) 0.2539 [0.21 ; 0.30], R/R 0.784, perte reelle 21.456 % (gap inclus), EV -0.6918 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.71 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.69 %) : P(cible) 33.9 % x 16.82 % + P(rien) 40.7 % x -2.32 % ne couvrent pas P(stop) 25.4 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 18.317 %) — p(stop avant cible) 0.2009 [0.16 ; 0.25], R/R 0.701, perte reelle 24.006 % (gap inclus), EV -0.157 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.33 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 34.9 % x 16.82 % + P(rien) 45.0 % x -2.66 % ne couvrent pas P(stop) 20.1 % x 24.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 3.78 ATR (stop 21.378 %) — p(stop avant cible) 0.112 [0.08 ; 0.15], R/R 0.574, perte reelle 29.294 % (gap inclus), EV 0.3938 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.38 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 23.551 %) — p(stop avant cible) 0.0774 [0.05 ; 0.11], R/R 0.574, perte reelle 29.294 % (gap inclus), EV 1.0825 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.56 % > budget 12.00 %
   - ⚪ grid_snapped a 5.22 ATR (stop 28.902 %) — p(stop avant cible) 0.0318 [0.02 ; 0.05], R/R 0.574, perte reelle 29.294 % (gap inclus), EV 1.4769 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.90 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 31.401 %) — p(stop avant cible) 0.0318 [0.02 ; 0.05], R/R 0.536, perte reelle 31.401 % (gap inclus), EV 1.4099 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.40 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 34.018 %) — p(stop avant cible) 0.0266 [0.01 ; 0.05], R/R 0.494, perte reelle 34.018 % (gap inclus), EV 1.3793 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.02 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 36.635 %) — p(stop avant cible) 0.0181 [0.01 ; 0.04], R/R 0.459, perte reelle 36.635 % (gap inclus), EV 1.3712 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.63 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 39.251 %) — p(stop avant cible) 0.0111 [0.00 ; 0.03], R/R 0.428, perte reelle 39.251 % (gap inclus), EV 1.3818 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.25 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 41.868 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.402, perte reelle 41.868 % (gap inclus), EV 1.4358 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.87 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 145.9, ATR14 7.6357 (5.234 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.357 ATR = 1.868 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.262 % | 145.5182 | 90.98 % | 94.11 % | 95.58 % | 96.65 % | 97.73 % | 98.7 % |
| 0.1 ATR | 0.523 % | 145.1364 | 84.71 % | 89.89 % | 91.94 % | 94.59 % | 96.24 % | 97.4 % |
| 0.15 ATR | 0.785 % | 144.7546 | 77.75 % | 84.99 % | 87.82 % | 91.14 % | 93.77 % | 95.3 % |
| 0.2 ATR | 1.047 % | 144.3729 | 69.22 % | 79.88 % | 83.89 % | 88.29 % | 91.49 % | 93.41 % |
| 0.25 ATR | 1.308 % | 143.9911 | 62.75 % | 76.05 % | 80.65 % | 86.61 % | 90.21 % | 92.81 % |
| 0.35 ATR | 1.832 % | 143.2275 | 50.69 % | 67.62 % | 73.67 % | 81.5 % | 85.95 % | 90.21 % |
| 0.5 ATR | 2.617 % | 142.0821 | 35.78 % | 55.35 % | 62.87 % | 73.62 % | 81.31 % | 87.51 % |
| 0.75 ATR | 3.925 % | 140.1732 | 17.06 % | 35.43 % | 46.95 % | 58.86 % | 73.29 % | 81.32 % |
| 1.0 ATR | 5.234 % | 138.2643 | 8.24 % | 24.04 % | 34.18 % | 47.93 % | 65.28 % | 75.92 % |
| 1.25 ATR | 6.542 % | 136.3554 | 4.12 % | 15.7 % | 25.34 % | 37.7 % | 57.07 % | 70.13 % |
| 1.5 ATR | 7.85 % | 134.4464 | 2.35 % | 10.7 % | 18.57 % | 30.12 % | 49.36 % | 63.84 % |
| 2.0 ATR | 10.467 % | 130.6286 | 0.59 % | 4.61 % | 8.94 % | 18.31 % | 35.61 % | 53.35 % |
| 2.5 ATR | 13.084 % | 126.8107 | 0.29 % | 2.45 % | 4.81 % | 11.71 % | 24.73 % | 45.25 % |
| 3.0 ATR | 15.701 % | 122.9929 | 0.2 % | 0.79 % | 2.55 % | 7.09 % | 17.21 % | 37.26 % |
| 4.0 ATR | 20.934 % | 115.3571 | 0.1 % | 0.59 % | 1.38 % | 3.54 % | 9.79 % | 24.08 % |
| 6.0 ATR | 31.401 % | 100.0857 | 0.0 % | 0.29 % | 0.79 % | 1.57 % | 4.45 % | 12.19 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.36 ATR | 0.41 ATR | 0.54 ATR | 0.64 ATR | 0.71 ATR | 0.95 ATR | 1.20 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.63 ATR | 0.80 ATR | 0.98 ATR | 1.12 ATR | 1.56 ATR | 1.97 ATR |
| **3 s.** | 0.33 ATR | 0.70 ATR | 0.79 ATR | 1.03 ATR | 1.26 ATR | 1.45 ATR | 1.95 ATR | 2.48 ATR |
| **5 s.** | 0.47 ATR | 0.95 ATR | 1.07 ATR | 1.41 ATR | 1.72 ATR | 1.93 ATR | 2.69 ATR | 3.59 ATR |
| **10 s.** | 0.70 ATR | 1.48 ATR | 1.66 ATR | 2.12 ATR | 2.49 ATR | 2.81 ATR | 3.97 ATR | 5.79 ATR |
| **20 s.** | 1.04 ATR | 2.21 ATR | 2.52 ATR | 3.32 ATR | 3.93 ATR | 4.69 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.407–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.63–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.788–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.234 %, prix 138.2636), p(touche) 34.18 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.072–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (6.542 %, prix 136.3552), p(touche) 37.7 % (en stress 87.25 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 18.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.659–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.516–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.293 | EV/share : €2.238 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 51 % | T2 27 % | T3 14 %
- Kelly (position) : f* 0.124 | ¼-Kelly 0.031 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 80.2 | bear 13.8 | side 6.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 584.0 (= 4 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.744% → cible +3.2% / stop −2.5%, p_fill 60%, n_eff≈26.5) : P(cible|rempli) **27%** · **EV/risk -0.035** (×p_fill ; si rempli -0.15% du capital)
  - **swing** (entrée dip −3.826% → cible +7.155% / stop −5.442%, p_fill 40%, n_eff≈21.4) : P(cible|rempli) **45%** · **EV/risk +0.009** (×p_fill ; si rempli +0.12% du capital)
  - **deep** (entrée dip −5.909% → cible +10.119% / stop −8.344%, p_fill 57%, n_eff≈24.8) : P(cible|rempli) **41%** · **EV/risk -0.087** (×p_fill ; si rempli -1.28% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→78% · +2.0%→64% · +3.0%→50% · +5.0%→31% · +8.0%→9%
- Range intraday médian 7.57% (p90 13.58%) · excursion haute méd. +3.14% / basse méd. −2.94%
- Profil de vol intra : ouverture 4.623% vs midi 1.318% vs clôture 1.973% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 11% · trend ↑0%/↓2% ; spike-down 71% · recovery-V 40%)_
- **Régime intraday** : **chop** _(efficiency 0.104 ; mean-reverting — autocorr -0.066)_ ; drift intra méd. -0.422% ; recovery-V 38%
- **σ réalisé intraday** 4.323% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 56% / whipsaw 37%
- POC intraday (dernière séance, temps-au-prix) : 128.644 (VA 127.828–129.324 ; dernier close 127.56)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 44% · rebond 81% · **stop −7.63%** sous le fill (sous le bruit) · cible +3.11% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.59% · baisse 37% (gap-down >1% 26% · >2% 18%)
- Excursion ouverture 5min (n=160) : bas méd −1.11% (p90 −3.4%) · haut méd +0.9% · range méd 2.7%
- Excursion ouverture 15min (n=160) : bas méd −1.34% (p90 −4.51%) · haut méd +1.25% · range méd 3.23%
- Excursion ouverture 30min (n=160) : bas méd −1.48% (p90 −5.08%) · haut méd +1.36% · range méd 3.54%
- Excursion ouverture 60min (n=160) : bas méd −1.55% (p90 −5.31%) · haut méd +1.64% · range méd 3.96%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 128.3 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 74% (124/159) · gap 33% · délai 0.1min · rebond 68% (87/124) (MFE +1.75%)
   - −1.0% : fill 30min 56% · séance 69% (113/159) · gap 26% · délai 0.2min · rebond 76% (84/113) (MFE +1.99%)
   - −1.5% : fill 30min 48% · séance 61% (104/159) · gap 20% · délai 0.3min · rebond 76% (77/104) (MFE +2.3%)
   - −2.0% : fill 30min 41% · séance 56% (93/159) · gap 18% · délai 0.4min · rebond 70% (70/93) (MFE +2.4%)
   - −3.0% : fill 30min 31% · séance 44% (77/159) · gap 9% · délai 1.5min · rebond 81% (65/77) (MFE +3.11%)
   - −4.0% : fill 30min 24% · séance 37% (64/159) · gap 5% · délai 10.8min · rebond 76% (54/64) (MFE +3.3%)
   - −5.0% : fill 30min 15% · séance 30% (49/159) · gap 2% · délai 31.6min · rebond 72% (39/49) (MFE +2.33%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.87% (p90 −3.45%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −2.4%) → stop au-delà de −1.97% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.84% (p90 −2.25%) → stop au-delà de −1.9% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1344 jambes) : jambe baissière méd −1.31% (p90 −3.14%) · ~16.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 97% (54/56) · rebond 67% (36/54)
      · −2.0% : fill 93% (51/56) · rebond 68% (38/51)
      · −3.0% : fill 81% (46/56) · rebond 81% (39/46)
      · −4.0% : fill 67% (39/56) · rebond 89% (36/39)
      · −5.0% : fill 54% (31/56) · rebond 77% (26/31)
   - **flat** (13 séances) :
      · −1.0% : fill 93% (10/13) · rebond 77% (8/10)
      · −2.0% : fill 73% (9/13) · rebond 78% (8/9)
      · −3.0% : fill 70% (8/13) · rebond 78% (7/8)
      · −4.0% : fill 56% (7/13) · rebond 58% (5/7)
      · −5.0% : fill 56% (7/13) · rebond 72% (6/7)
   - **gap-up** (90 séances) :
      · −1.0% : fill 51% (49/90) · rebond 84% (40/49)
      · −2.0% : fill 33% (33/90) · rebond 73% (24/33)
      · −3.0% : fill 21% (23/90) · rebond 82% (19/23)
      · −4.0% : fill 18% (18/90) · rebond 57% (13/18)
      · −5.0% : fill 14% (11/90) · rebond 59% (7/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 62% si les 15 1res min sont vertes (77 cas) · 36% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 72% si début vert vs 25% si rouge (base 49% · écart 46 pts) ; prédictivité sature ensuite (plafond brut 272min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **72%** · continue >prix actuel 49% ; creux résiduel méd -1.81% (q20 -4.92%) → **SL/trailing à −4.92%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.35% / q75 +4.48% → **scale +2.35% / runner +4.48%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **25%** (continue à baisser 65%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.65%** (au-delà de la MAE q10 -8.65%), cible rebond +2.01% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.59% .. +6.13%] · haut q95 +7.22% · bas q05 -5.93%
   - 60min (n=160) : retour [-5.37% .. +6.48%] · haut q95 +7.85% · bas q05 -6.55%
   - 2h (n=160) : retour [-6.01% .. +5.93%] · haut q95 +9.18% · bas q05 -7.41%
   - 4h (n=160) : retour [-6.77% .. +7.89%] · haut q95 +10.91% · bas q05 -8.1%
   - 6h (n=160) : retour [-7.61% .. +9.07%] · haut q95 +12.33% · bas q05 -9.35%
   - session (n=160) : retour [-11.05% .. +10.07%] · haut q95 +13.99% · bas q05 -12.6%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 5.8)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **20%**. Lecture précoce 30 min : signature présente → 8% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.06% (p75 1.5% / p90 2.89%) · ~5.05 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **89%** (reprise méd 20.0 min, n=60)
   - −1.0% → **82%** (reprise méd 34.22 min, n=34)
   - −1.5% → **69%** (reprise méd 46.1 min, n=18)
   - −2.0% → **87%** (reprise méd 49.44 min, n=15)
   - −3.0% → **100%** (reprise méd 61.76 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.89%** (p90, défaut prudent ; serré/agressif −1.5%) ; extension open→close méd +7.26% (q75 +13.51% / q95 +17.04%), MFE méd +8.03% / q90 +18.1%
   - Échelle scale-out : +8.03% (33%) / +14.35% (33%) / +18.1% (34%)
- **DÉSARMER** : repli > **−2.89%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +18.1% : P(retournement après) 0% (mèche méd 1.42%)
- **CONTEXTE** : la dernière heure tient les gains 96% du temps (retour médian dernière heure +1.92%)


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : extreme
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

- **RSI** : 82.6  _(surachat)_
- **ADX** : 19.1  _(pas de tendance nette)_
- **MACD** : hist 3.446  _(bullish_recent)_
- **BB** : %B 1.02 · largeur 42.6%
- **ATR** : 7.64 (63.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.208  _(distribution)_
- **Vol ratio** : 0.51  _(volume atone)_
- **Choppiness** : 36.9  _(marche directionnel)_
- **MA** : MA20 119.6 · MA50 111.72 · MA200 82.06  _(prix > MA20)_
- **Dist MA** : MA20 +22.0% · MA50 +30.6% · MA200 +77.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (775553 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
