# SOFI

**Generated** : 2026-09-23T00:47:56.464282+00:00  
**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $17.17  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $17.17 (+1.5% vs entrée) · entrée $16.92 · stop $16.24 · T1 $17.18 · R/R 0.38  
> ↳ P(T1 av. stop) 43 % _(réel 5 s)_ · EV/risk -0.04 _(réel 5 s)_ (GBM 0.026) · ¼-Kelly 0.063 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +0.2 % ≠ (strike 17.0 − spot 17.17)/spot = -1.0 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.160 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $16.87–$16.97 (mid $16.92)
- Spot actuel : $17.17 (+1.5% au-dessus de la zone — repli à attendre)
- Stop : $16.24 (stop swing_plan-based (-7.01%))
- Targets : T1 $17.18 · R/R 0.38 | T2 $17.44 · R/R 0.76 | T3 $17.71 · R/R 1.16
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.24


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=5.91 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.01 %)** : le gap seul le franchit 0.718 % des séances (9 fois sur 1253).
   - exécution **2.313 pt plus bas** dans le cas TYPIQUE (médiane), 3.098 au p90, **4.095 au pire**
   - perte réelle **8.985 %** en moyenne _(tirée par la queue)_, jusqu'à **11.105 %** — au lieu des 7.01 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0142 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 9 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.229 % | p01 -6.52 % | pire -11.105 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1176** [0.076 ; 0.1718] _(largeur 9.6 pt, n_eff 173.1)_
   - swing : **0.4774** [0.4251 ; 0.5301] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.45** [0.3982 ; 0.5027] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (36.7 pt), swing (41.2 pt), deep (43.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1020 séances)** : VaR **-5.82 %** | CVaR **-8.35 %** | vol 3.83 %/j
   - _fenêtre arrêtée : rupture de regime a 1080 seances en arriere (volatilite 5.66 % contre 3.50 % aujourd'hui, rapport 1.62)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.5 % vs -14.19 % si l'on extrapolait par √5 _(rapport 1.021 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8245** (β de hausse 1.708, asymétrie 1.0682) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.368× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 15.1796 sur atr_grid (3.0 ATR, 11.566 %) — p(stop avant cible) 0.2672 [0.22 ; 0.32], R/R 4.069, perte reelle 11.566 % (gap inclus), CVaR 11.566 %, EV -0.5304 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.783 %) — p(stop avant cible) 0.5848 [0.53 ; 0.64], R/R 6.167, perte reelle 7.631 % (gap inclus), EV -1.3999 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.585, borne haute 0.636 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.40 %) : P(cible) 0.1 % x 47.06 % + P(rien) 41.5 % x 7.33 % ne couvrent pas P(stop) 58.5 % x 7.63 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.16 ATR (stop 6.965 %) — p(stop avant cible) 0.4964 [0.44 ; 0.55], R/R 5.355, perte reelle 8.788 % (gap inclus), EV -1.2467 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.25 %) : P(cible) 0.1 % x 47.06 % + P(rien) 50.3 % x 6.15 % ne couvrent pas P(stop) 49.6 % x 8.79 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 1.59 ATR (stop 8.609 %) — p(stop avant cible) 0.4046 [0.35 ; 0.46], R/R 4.848, perte reelle 9.707 % (gap inclus), EV -0.9427 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.94 %) : P(cible) 0.1 % x 47.06 % + P(rien) 59.5 % x 4.98 % ne couvrent pas P(stop) 40.5 % x 9.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.45 ATR (stop 15.807 %) — p(stop avant cible) 0.1017 [0.07 ; 0.14], R/R 2.977, perte reelle 15.807 % (gap inclus), EV 0.1191 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.81 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.964 %) — p(stop avant cible) 0.9365 [0.91 ; 0.96], R/R 19.289, perte reelle 2.44 % (gap inclus), EV -1.4165 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 19.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.936, borne haute 0.959 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.42 %) : P(cible) 0.0 % x 47.06 % + P(rien) 6.3 % x 13.68 % ne couvrent pas P(stop) 93.7 % x 2.44 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.928 %) — p(stop avant cible) 0.8929 [0.86 ; 0.92], R/R 13.291, perte reelle 3.541 % (gap inclus), EV -1.757 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 13.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.893, borne haute 0.922 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.76 %) : P(cible) 0.0 % x 47.06 % + P(rien) 10.7 % x 13.02 % ne couvrent pas P(stop) 89.3 % x 3.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.892 %) — p(stop avant cible) 0.8294 [0.79 ; 0.87], R/R 9.999, perte reelle 4.707 % (gap inclus), EV -2.115 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 10.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.829, borne haute 0.866 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.12 %) : P(cible) 0.0 % x 47.06 % + P(rien) 17.0 % x 10.40 % ne couvrent pas P(stop) 82.9 % x 4.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 7.711 %) — p(stop avant cible) 0.4505 [0.40 ; 0.50], R/R 4.848, perte reelle 9.707 % (gap inclus), EV -1.2934 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.29 %) : P(cible) 0.1 % x 47.06 % + P(rien) 54.9 % x 5.57 % ne couvrent pas P(stop) 45.1 % x 9.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 9.639 %) — p(stop avant cible) 0.3661 [0.32 ; 0.42], R/R 4.593, perte reelle 10.246 % (gap inclus), EV -0.8908 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.89 %) : P(cible) 0.1 % x 47.06 % + P(rien) 63.3 % x 4.48 % ne couvrent pas P(stop) 36.6 % x 10.25 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 10.602 %) — p(stop avant cible) 0.3064 [0.26 ; 0.36], R/R 4.238, perte reelle 11.105 % (gap inclus), EV -0.6838 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.68 %) : P(cible) 0.1 % x 47.06 % + P(rien) 69.3 % x 3.89 % ne couvrent pas P(stop) 30.6 % x 11.11 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 11.566 %) — p(stop avant cible) 0.2672 [0.22 ; 0.32], R/R 4.069, perte reelle 11.566 % (gap inclus), EV -0.5304 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 0.1 % x 47.06 % + P(rien) 73.2 % x 3.46 % ne couvrent pas P(stop) 26.7 % x 11.57 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 3.45 ATR (stop 14.469 %) — p(stop avant cible) 0.1351 [0.10 ; 0.17], R/R 3.253, perte reelle 14.469 % (gap inclus), EV -0.058 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.47 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.06 %) : P(cible) 0.1 % x 47.06 % + P(rien) 86.4 % x 2.17 % ne couvrent pas P(stop) 13.5 % x 14.47 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 17.349 %) — p(stop avant cible) 0.0732 [0.05 ; 0.10], R/R 2.713, perte reelle 17.349 % (gap inclus), EV 0.1187 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.35 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 19.277 %) — p(stop avant cible) 0.0551 [0.03 ; 0.08], R/R 2.441, perte reelle 19.277 % (gap inclus), EV 0.0877 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.28 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 21.205 %) — p(stop avant cible) 0.0354 [0.02 ; 0.06], R/R 2.219, perte reelle 21.205 % (gap inclus), EV 0.0676 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.20 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 23.133 %) — p(stop avant cible) 0.0275 [0.01 ; 0.05], R/R 2.034, perte reelle 23.133 % (gap inclus), EV 0.065 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.13 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 25.06 %) — p(stop avant cible) 0.0185 [0.01 ; 0.04], R/R 1.878, perte reelle 25.06 % (gap inclus), EV 0.0949 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.06 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 26.988 %) — p(stop avant cible) 0.0044 [0.00 ; 0.02], R/R 1.744, perte reelle 26.988 % (gap inclus), EV 0.1823 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.99 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 28.916 %) — p(stop avant cible) 0.003 [0.00 ; 0.01], R/R 1.628, perte reelle 28.916 % (gap inclus), EV 0.1903 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.92 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 30.843 %) — p(stop avant cible) 0.0029 [0.00 ; 0.01], R/R 1.526, perte reelle 30.843 % (gap inclus), EV 0.1858 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.84 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 17.165, ATR14 0.6618 (3.855 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.374 ATR = 1.442 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.193 % | 17.1319 | 92.85 % | 95.77 % | 97.07 % | 97.47 % | 98.27 % | 98.87 % |
| 0.1 ATR | 0.386 % | 17.0988 | 85.2 % | 89.42 % | 92.03 % | 93.33 % | 95.53 % | 97.13 % |
| 0.15 ATR | 0.578 % | 17.0657 | 78.95 % | 84.68 % | 87.99 % | 90.39 % | 92.89 % | 94.87 % |
| 0.2 ATR | 0.771 % | 17.0326 | 71.6 % | 79.44 % | 83.35 % | 86.86 % | 90.55 % | 93.33 % |
| 0.25 ATR | 0.964 % | 16.9996 | 66.26 % | 74.9 % | 79.92 % | 84.13 % | 88.92 % | 91.89 % |
| 0.35 ATR | 1.349 % | 16.9334 | 52.37 % | 65.12 % | 71.95 % | 78.26 % | 85.37 % | 88.6 % |
| 0.5 ATR | 1.928 % | 16.8341 | 37.66 % | 53.12 % | 61.55 % | 69.06 % | 79.37 % | 84.5 % |
| 0.75 ATR | 2.892 % | 16.6687 | 20.44 % | 36.69 % | 46.72 % | 56.72 % | 69.61 % | 77.62 % |
| 1.0 ATR | 3.855 % | 16.5032 | 8.76 % | 24.29 % | 33.7 % | 44.89 % | 59.35 % | 68.99 % |
| 1.25 ATR | 4.819 % | 16.3378 | 4.13 % | 14.82 % | 23.61 % | 35.29 % | 50.1 % | 62.22 % |
| 1.5 ATR | 5.783 % | 16.1723 | 2.01 % | 9.27 % | 16.45 % | 27.2 % | 42.28 % | 55.85 % |
| 2.0 ATR | 7.711 % | 15.8414 | 0.7 % | 4.33 % | 8.27 % | 15.07 % | 28.96 % | 44.87 % |
| 2.5 ATR | 9.639 % | 15.5105 | 0.3 % | 1.92 % | 3.83 % | 9.4 % | 19.51 % | 35.32 % |
| 3.0 ATR | 11.566 % | 15.1796 | 0.1 % | 0.91 % | 2.83 % | 6.07 % | 13.62 % | 27.93 % |
| 4.0 ATR | 15.422 % | 14.5179 | 0.0 % | 0.3 % | 0.71 % | 2.53 % | 7.42 % | 14.68 % |
| 6.0 ATR | 23.133 % | 13.1943 | 0.0 % | 0.1 % | 0.2 % | 0.2 % | 0.91 % | 3.08 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.37 ATR | 0.42 ATR | 0.57 ATR | 0.68 ATR | 0.76 ATR | 0.97 ATR | 1.20 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.62 ATR | 0.82 ATR | 0.99 ATR | 1.11 ATR | 1.47 ATR | 1.93 ATR |
| **3 s.** | 0.31 ATR | 0.69 ATR | 0.78 ATR | 1.02 ATR | 1.22 ATR | 1.38 ATR | 1.89 ATR | 2.37 ATR |
| **5 s.** | 0.40 ATR | 0.89 ATR | 1.00 ATR | 1.32 ATR | 1.59 ATR | 1.80 ATR | 2.45 ATR | 3.30 ATR |
| **10 s.** | 0.61 ATR | 1.25 ATR | 1.41 ATR | 1.85 ATR | 2.21 ATR | 2.47 ATR | 3.58 ATR | 4.74 ATR |
| **20 s.** | 0.83 ATR | 1.77 ATR | 1.99 ATR | 2.66 ATR | 3.22 ATR | 3.60 ATR | 4.81 ATR | 5.67 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.425–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.928 %, prix 16.8341), p(touche) 37.66 % (en stress 84.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.624–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.892 %, prix 16.6686), p(touche) 36.69 % (en stress 91.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 21.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.783–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.855 %, prix 16.5033), p(touche) 33.7 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.998–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.855 %, prix 16.5033), p(touche) 44.89 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 20.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.413–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.783 %, prix 16.1723), p(touche) 42.28 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.994–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.711 %, prix 15.8414), p(touche) 44.87 % (en stress 98.98 %)  ✅ optimum identifie (74.5 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.026 | EV/share : $0.017 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 57 % | T2 35 % | T3 16 %
- Kelly (position) : f* 0.251 | ¼-Kelly 0.063 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 76.5 | bear 7.2 | side 16.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 154.0 (= 9 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.427% → cible +1.553% / stop −4.0%, p_fill 52%, n_eff≈25.6) : P(cible|rempli) **43%** · **EV/risk -0.040** (×p_fill ; si rempli -0.31% du capital)
  - **swing** (entrée dip −3.155% → cible +3.472% / stop −3.981%, p_fill 49%, n_eff≈19.4) : P(cible|rempli) **59%** · **EV/risk +0.047** (×p_fill ; si rempli +0.38% du capital)
  - **deep** (entrée dip −4.867% → cible +4.91% / stop −6.079%, p_fill 30%, n_eff≈15.1) : P(cible|rempli) **68%** · **EV/risk +0.077** (×p_fill ; si rempli +1.55% du capital)
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
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 51.3  _(neutre)_
- **ADX** : 10.7  _(pas de tendance nette)_
- **MACD** : hist -0.09  _(pas de croisement recent)_
- **BB** : %B 0.33 · largeur 17.0%
- **ATR** : 0.66 (2.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.155  _(distribution)_
- **Vol ratio** : 2.2  _(volume au-dessus de la moyenne)_
- **Choppiness** : 54.8  _(transition)_
- **MA** : MA20 17.69 · MA50 17.66 · MA200 19.39  _(prix < MA20)_
- **Dist MA** : MA20 -3.0% · MA50 -2.8% · MA200 -11.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (846635 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
