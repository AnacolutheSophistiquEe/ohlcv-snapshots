# SOFI

**Generated** : 2026-09-28T00:48:41.107754+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $16.58  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $16.58 (+0.6% vs entrée) · entrée $16.48 · stop $15.82 · T1 $16.73 · R/R 0.38  
> ↳ P(T1 av. stop) 55 % _(réel 5 s)_ · EV/risk -0.036 _(réel 5 s)_ (GBM 0.028) · ¼-Kelly 0.066 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.230 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $16.43–$16.53 (mid $16.48)
- Spot actuel : $16.58 (+0.6% au-dessus de la zone — repli à attendre)
- Stop : $15.82 (stop swing_plan-based (-4.99%))
- Targets : T1 $16.73 · R/R 0.38 | T2 $16.97 · R/R 0.74 | T3 $17.22 · R/R 1.12
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $15.82


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=5.90 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (4.99 %)** : le gap seul le franchit 1.834 % des séances (23 fois sur 1254).
   - exécution **1.783 pt plus bas** dans le cas TYPIQUE (médiane), 4.732 au p90, **6.115 au pire**
   - perte réelle **7.252 %** en moyenne _(tirée par la queue)_, jusqu'à **11.105 %** — au lieu des 4.99 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0415 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.226 % | p01 -6.517 % | pire -11.105 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1251** [0.0821 ; 0.1805] _(largeur 9.8 pt, n_eff 173.1)_
   - swing : **0.4808** [0.4285 ; 0.5334] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4737** [0.4215 ; 0.5264] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (32.9 pt), swing (33.1 pt), deep (30.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1080 séances)** : VaR **-5.98 %** | CVaR **-8.42 %** | vol 3.95 %/j
   - _fenêtre arrêtée : rupture de regime a 1140 seances en arriere (volatilite 5.70 % contre 3.51 % aujourd'hui, rapport 1.62)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.5 % vs -14.19 % si l'on extrapolait par √5 _(rapport 1.022 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8234** (β de hausse 1.713, asymétrie 1.0645) vs IWM — 605 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.375× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 14.6976 sur grid_snapped (2.8 ATR, 11.353 %) — p(stop avant cible) 0.2697 [0.23 ; 0.32], R/R 4.611, perte reelle 11.353 % (gap inclus), CVaR 11.353 %, EV -0.5414 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.28 ATR (stop 3.081 %) — p(stop avant cible) 0.8063 [0.76 ; 0.85], R/R 10.561, perte reelle 4.957 % (gap inclus), EV -2.1535 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 10.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.806, borne haute 0.845 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.15 %) : P(cible) 0.0 % x 52.35 % + P(rien) 19.4 % x 9.47 % ne couvrent pas P(stop) 80.6 % x 4.96 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 0.76 ATR (stop 4.815 %) — p(stop avant cible) 0.6533 [0.60 ; 0.70], R/R 7.411, perte reelle 7.064 % (gap inclus), EV -1.8369 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.653, borne haute 0.702 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.84 %) : P(cible) 0.0 % x 52.35 % + P(rien) 34.6 % x 7.99 % ne couvrent pas P(stop) 65.3 % x 7.06 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 support a 2.8 ATR (stop 12.299 %) — p(stop avant cible) 0.2237 [0.18 ; 0.27], R/R 4.256, perte reelle 12.299 % (gap inclus), EV -0.3566 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.30 % > budget 12.00 %
      - ⚠ support DETECTE a 0.66 ATR du spot — compartiment <1, mesure a 48.0 % de casse (IC clusterise [0.451 ; 0.508] sur 1182 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 0.0 % x 52.35 % + P(rien) 77.6 % x 3.07 % ne couvrent pas P(stop) 22.4 % x 12.30 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.28 ATR (stop 2.135 %) — p(stop avant cible) 0.881 [0.84 ; 0.91], R/R 14.039, perte reelle 3.729 % (gap inclus), EV -1.8358 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 14.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.881, borne haute 0.912 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.84 %) : P(cible) 0.0 % x 52.35 % + P(rien) 11.9 % x 12.11 % ne couvrent pas P(stop) 88.1 % x 3.73 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.76 ATR (stop 3.869 %) — p(stop avant cible) 0.7253 [0.68 ; 0.77], R/R 8.909, perte reelle 5.876 % (gap inclus), EV -1.9053 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 8.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.725, borne haute 0.770 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.91 %) : P(cible) 0.0 % x 52.35 % + P(rien) 27.4 % x 8.55 % ne couvrent pas P(stop) 72.5 % x 5.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.5 ATR (stop 5.499 %) — p(stop avant cible) 0.6084 [0.56 ; 0.66], R/R 7.034, perte reelle 7.442 % (gap inclus), EV -1.5512 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.608, borne haute 0.659 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.55 %) : P(cible) 0.0 % x 52.35 % + P(rien) 39.1 % x 7.56 % ne couvrent pas P(stop) 60.8 % x 7.44 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 6.416 %) — p(stop avant cible) 0.53 [0.48 ; 0.58], R/R 6.291, perte reelle 8.322 % (gap inclus), EV -1.3736 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.530, borne haute 0.582 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.37 %) : P(cible) 0.0 % x 52.35 % + P(rien) 47.0 % x 6.43 % ne couvrent pas P(stop) 53.0 % x 8.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 7.332 %) — p(stop avant cible) 0.4733 [0.42 ; 0.53], R/R 5.826, perte reelle 8.985 % (gap inclus), EV -1.2478 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.25 %) : P(cible) 0.0 % x 52.35 % + P(rien) 52.6 % x 5.68 % ne couvrent pas P(stop) 47.3 % x 8.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 8.249 %) — p(stop avant cible) 0.4161 [0.36 ; 0.47], R/R 5.393, perte reelle 9.707 % (gap inclus), EV -1.1523 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.15 %) : P(cible) 0.0 % x 52.35 % + P(rien) 58.4 % x 4.92 % ne couvrent pas P(stop) 41.6 % x 9.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 9.166 %) — p(stop avant cible) 0.3801 [0.33 ; 0.43], R/R 5.281, perte reelle 9.913 % (gap inclus), EV -0.9449 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.94 %) : P(cible) 0.0 % x 52.35 % + P(rien) 62.0 % x 4.53 % ne couvrent pas P(stop) 38.0 % x 9.91 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 grid_snapped a 2.8 ATR (stop 11.353 %) — p(stop avant cible) 0.2697 [0.23 ; 0.32], R/R 4.611, perte reelle 11.353 % (gap inclus), EV -0.5414 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.54 %) : P(cible) 0.0 % x 52.35 % + P(rien) 73.0 % x 3.43 % ne couvrent pas P(stop) 27.0 % x 11.35 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 12.832 %) — p(stop avant cible) 0.2083 [0.17 ; 0.25], R/R 4.08, perte reelle 12.832 % (gap inclus), EV -0.3635 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.83 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 0.0 % x 52.35 % + P(rien) 79.1 % x 2.90 % ne couvrent pas P(stop) 20.8 % x 12.83 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 14.665 %) — p(stop avant cible) 0.1282 [0.10 ; 0.17], R/R 3.57, perte reelle 14.665 % (gap inclus), EV -0.1014 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.66 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 0.0 % x 52.35 % + P(rien) 87.2 % x 2.02 % ne couvrent pas P(stop) 12.8 % x 14.66 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 16.498 %) — p(stop avant cible) 0.0834 [0.06 ; 0.12], R/R 3.173, perte reelle 16.498 % (gap inclus), EV 0.0292 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 16.50 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 18.331 %) — p(stop avant cible) 0.0599 [0.04 ; 0.09], R/R 2.856, perte reelle 18.331 % (gap inclus), EV 0.039 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.33 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 20.164 %) — p(stop avant cible) 0.0455 [0.03 ; 0.07], R/R 2.596, perte reelle 20.164 % (gap inclus), EV 0.0239 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.16 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 21.997 %) — p(stop avant cible) 0.0331 [0.02 ; 0.06], R/R 2.38, perte reelle 21.997 % (gap inclus), EV -0.0108 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.00 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.01 %) : P(cible) 0.0 % x 52.35 % + P(rien) 96.7 % x 0.73 % ne couvrent pas P(stop) 3.3 % x 22.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 23.83 %) — p(stop avant cible) 0.0231 [0.01 ; 0.04], R/R 2.197, perte reelle 23.83 % (gap inclus), EV 0.0054 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.83 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 25.663 %) — p(stop avant cible) 0.015 [0.01 ; 0.03], R/R 2.04, perte reelle 25.663 % (gap inclus), EV 0.0452 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.66 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 27.497 %) — p(stop avant cible) 0.0037 [0.00 ; 0.01], R/R 1.904, perte reelle 27.497 % (gap inclus), EV 0.1248 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.50 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 29.33 %) — p(stop avant cible) 0.0029 [0.00 ; 0.01], R/R 1.785, perte reelle 29.33 % (gap inclus), EV 0.1311 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.33 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 16.58, ATR14 0.6079 (3.666 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.376 ATR = 1.378 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.183 % | 16.5496 | 92.86 % | 95.77 % | 97.08 % | 97.47 % | 98.27 % | 98.87 % |
| 0.1 ATR | 0.367 % | 16.5192 | 85.21 % | 89.43 % | 92.04 % | 93.33 % | 95.53 % | 97.13 % |
| 0.15 ATR | 0.55 % | 16.4888 | 78.97 % | 84.69 % | 88.0 % | 90.4 % | 92.89 % | 94.87 % |
| 0.2 ATR | 0.733 % | 16.4584 | 71.63 % | 79.46 % | 83.37 % | 86.87 % | 90.56 % | 93.33 % |
| 0.25 ATR | 0.917 % | 16.428 | 66.3 % | 74.92 % | 79.94 % | 84.14 % | 88.93 % | 91.9 % |
| 0.35 ATR | 1.283 % | 16.3672 | 52.52 % | 65.16 % | 71.88 % | 78.28 % | 85.38 % | 88.62 % |
| 0.5 ATR | 1.833 % | 16.2761 | 37.73 % | 53.17 % | 61.49 % | 69.09 % | 79.39 % | 84.51 % |
| 0.75 ATR | 2.75 % | 16.1241 | 20.62 % | 36.86 % | 46.67 % | 56.77 % | 69.54 % | 77.64 % |
| 1.0 ATR | 3.666 % | 15.9721 | 8.85 % | 24.47 % | 33.77 % | 44.75 % | 59.29 % | 69.03 % |
| 1.25 ATR | 4.583 % | 15.8202 | 4.23 % | 15.01 % | 23.79 % | 35.05 % | 50.05 % | 62.26 % |
| 1.5 ATR | 5.499 % | 15.6682 | 2.01 % | 9.37 % | 16.53 % | 26.97 % | 42.23 % | 55.9 % |
| 2.0 ATR | 7.332 % | 15.3643 | 0.7 % | 4.43 % | 8.37 % | 15.05 % | 28.93 % | 45.13 % |
| 2.5 ATR | 9.166 % | 15.0604 | 0.3 % | 1.91 % | 3.93 % | 9.39 % | 19.49 % | 35.49 % |
| 3.0 ATR | 10.999 % | 14.7564 | 0.1 % | 0.91 % | 2.82 % | 6.06 % | 13.6 % | 28.1 % |
| 4.0 ATR | 14.665 % | 14.1486 | 0.0 % | 0.3 % | 0.71 % | 2.53 % | 7.41 % | 14.67 % |
| 6.0 ATR | 21.997 % | 12.9329 | 0.0 % | 0.1 % | 0.2 % | 0.2 % | 0.91 % | 3.08 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.69 ATR | 0.76 ATR | 0.98 ATR | 1.21 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.62 ATR | 0.83 ATR | 0.99 ATR | 1.12 ATR | 1.47 ATR | 1.94 ATR |
| **3 s.** | 0.31 ATR | 0.69 ATR | 0.78 ATR | 1.02 ATR | 1.22 ATR | 1.38 ATR | 1.90 ATR | 2.38 ATR |
| **5 s.** | 0.40 ATR | 0.89 ATR | 0.99 ATR | 1.31 ATR | 1.58 ATR | 1.79 ATR | 2.45 ATR | 3.30 ATR |
| **10 s.** | 0.61 ATR | 1.25 ATR | 1.41 ATR | 1.85 ATR | 2.21 ATR | 2.47 ATR | 3.58 ATR | 4.74 ATR |
| **20 s.** | 0.83 ATR | 1.77 ATR | 2.01 ATR | 2.67 ATR | 3.23 ATR | 3.60 ATR | 4.81 ATR | 5.67 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.426–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.833 %, prix 16.2761), p(touche) 37.73 % (en stress 84.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.625–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.75 %, prix 16.124), p(touche) 36.86 % (en stress 91.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 18.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.782–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.666 %, prix 15.9722), p(touche) 33.77 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.995–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.666 %, prix 15.9722), p(touche) 44.75 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 21.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.411–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.499 %, prix 15.6683), p(touche) 42.23 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.007–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (9.166 %, prix 15.0603), p(touche) 35.49 % (en stress 98.98 %)  ✅ optimum identifie (74.5 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.028 | EV/share : $0.018 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 58 % | T2 38 % | T3 18 %
- Kelly (position) : f* 0.264 | ¼-Kelly 0.066 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 14.6 | bear 8.1 | side 77.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.604% → cible +1.488% / stop −4.0%, p_fill 82%, n_eff≈32.8) : P(cible|rempli) **55%** · **EV/risk -0.036** (×p_fill ; si rempli -0.18% du capital)
  - **swing** (entrée dip −1.324% → cible +3.329% / stop −3.715%, p_fill 79%, n_eff≈31.5) : P(cible|rempli) **58%** · **EV/risk +0.119** (×p_fill ; si rempli +0.56% du capital)
  - **deep** (entrée dip −2.041% → cible +4.708% / stop −5.613%, p_fill 72%, n_eff≈30.8) : P(cible|rempli) **72%** · **EV/risk +0.226** (×p_fill ; si rempli +1.76% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→71% · +2.0%→50% · +3.0%→38% · +5.0%→14% · +8.0%→1%
- Range intraday médian 4.39% (p90 7.54%) · excursion haute méd. +2.04% / basse méd. −2.17%
- Profil de vol intra : ouverture 3.063% vs midi 0.835% vs clôture 0.985% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 16% · trend ↑2%/↓0% ; spike-down 59% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.15 ; neutre — autocorr -0.026)_ ; drift intra méd. 0.123% ; recovery-V 26%
- **σ réalisé intraday** 2.603% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 52% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 18.1833 (VA 18.1547–18.2972 ; dernier close 18.21)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 47% · rebond 67% · **stop −3.09%** sous le fill (sous le bruit) · cible +1.72% · R/R 0.56 (high win-rate)
- Gaps overnight (n=159) : méd. 0.19% · baisse 43% (gap-down >1% 24% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −1.69%) · haut méd +0.72% · range méd 1.65%
- Excursion ouverture 15min (n=160) : bas méd −0.92% (p90 −2.67%) · haut méd +1.07% · range méd 2.26%
- Excursion ouverture 30min (n=160) : bas méd −1.07% (p90 −3.18%) · haut méd +1.23% · range méd 2.66%
- Excursion ouverture 60min (n=160) : bas méd −1.28% (p90 −3.59%) · haut méd +1.33% · range méd 3.34%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 18.22 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 74% (121/159) · gap 31% · délai 0.0min · rebond 51% (64/121) (MFE +1.13%)
   - −1.0% : fill 30min 52% · séance 64% (109/159) · gap 24% · délai 1.2min · rebond 53% (62/109) (MFE +1.01%)
   - −1.5% : fill 30min 41% · séance 60% (100/159) · gap 21% · délai 7.1min · rebond 62% (66/100) (MFE +1.35%)
   - −2.0% : fill 30min 35% · séance 47% (80/159) · gap 11% · délai 3.8min · rebond 67% (55/80) (MFE +1.72%)
   - −3.0% : fill 30min 11% · séance 32% (57/159) · gap 2% · délai 50.3min · rebond 54% (37/57) (MFE +1.08%)
   - −4.0% : fill 30min 8% · séance 17% (36/159) · gap 2% · délai 48.8min · rebond 52% (23/36) (MFE +1.2%)
   - −5.0% : fill 30min 3% · séance 10% (20/159) · gap 2% · délai 192.2min · rebond 44% (10/20) (MFE +0.72%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.43% (p90 −1.73%) → stop au-delà de −1.25% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.48% (p90 −1.81%) → stop au-delà de −1.38% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.47% (p90 −1.44%) → stop au-delà de −1.18% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=664 jambes) : jambe baissière méd −1.08% (p90 −2.75%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (66 séances) :
      · −1.0% : fill 98% (65/66) · rebond 51% (38/65)
      · −2.0% : fill 86% (56/66) · rebond 72% (40/56)
      · −3.0% : fill 63% (42/66) · rebond 57% (28/42)
      · −4.0% : fill 36% (28/66) · rebond 60% (20/28)
      · −5.0% : fill 21% (16/66) · rebond 54% (9/16)
   - **flat** (21 séances) :
      · −1.0% : fill 59% (12/21) · rebond 42% (5/12)
      · −2.0% : fill 40% (7/21) · rebond 55% (4/7)
      · −3.0% : fill 31% (6/21) · rebond 38% (3/6)
      · −4.0% : fill 19% (3/21) · rebond 30% (1/3)
      · −5.0% : fill 11% (1/21) · rebond 0% (0/1)
   - **gap-up** (72 séances) :
      · −1.0% : fill 41% (32/72) · rebond 62% (19/32)
      · −2.0% : fill 20% (17/72) · rebond 58% (11/17)
      · −3.0% : fill 10% (9/72) · rebond 60% (6/9)
      · −4.0% : fill 3% (5/72) · rebond 22% (2/5)
      · −5.0% : fill 1% (3/72) · rebond 44% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 64% si les 15 1res min sont vertes (75 cas) · 27% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **52min** → P(séance verte=clôture>ouverture) 82% si début vert vs 12% si rouge (base 44% · écart 70 pts) ; prédictivité sature ensuite (plafond brut 228min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=68) : tient le vert **82%** · continue >prix actuel 61% ; creux résiduel méd -0.98% (q20 -2.13%) → **SL/trailing à −2.13%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.34% / q75 +2.83% → **scale +1.34% / runner +2.83%**, sortie à la clôture
  - **si ROUGE au coude** (n=92) : edge inversé — récupère vert seulement **12%** (continue à baisser 55%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.24%** (au-delà de la MAE q10 -3.24%), cible rebond +1.13% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.86% .. +3.66%] · haut q95 +4.01% · bas q05 -3.38%
   - 60min (n=160) : retour [-3.12% .. +4.25%] · haut q95 +4.63% · bas q05 -4.0%
   - 2h (n=160) : retour [-3.58% .. +4.46%] · haut q95 +5.16% · bas q05 -4.56%
   - 4h (n=160) : retour [-4.23% .. +4.54%] · haut q95 +5.67% · bas q05 -5.12%
   - 6h (n=160) : retour [-4.69% .. +4.63%] · haut q95 +5.7% · bas q05 -5.61%
   - session (n=160) : retour [-4.65% .. +4.94%] · haut q95 +5.7% · bas q05 -5.84%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.9%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 28.9  _(survente)_
- **ADX** : 9.5  _(pas de tendance nette)_
- **MACD** : hist -0.084  _(pas de croisement recent)_
- **BB** : %B 0.17 · largeur 13.3%
- **ATR** : 0.61 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.231  _(distribution)_
- **Vol ratio** : 0.71  _(volume normal)_
- **Choppiness** : 52.1  _(transition)_
- **MA** : MA20 17.34 · MA50 17.58 · MA200 19.22  _(prix < MA20)_
- **Dist MA** : MA20 -4.4% · MA50 -5.7% · MA200 -13.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (870637 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
