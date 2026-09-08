# IONQ

**Generated** : 2026-09-08T00:41:39.520525+00:00  
**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $39.52  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot $39.52 (+0.5% vs entrée) · entrée $39.34 · stop $38.55 · T1 $40.33 · R/R 1.25  
> ↳ P(T1 av. stop) 51 % _(réel 5 s)_ · EV/risk 0.21 _(réel 5 s)_ (GBM 0.047) · ¼-Kelly 0.01 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.080 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $39.16–$39.52 (mid $39.34)
- Spot actuel : $39.52 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : $38.55 (stop swing_plan-based (-7.36%))
- Targets : T1 $40.33 · R/R 1.25 | T2 $41.31 · R/R 2.49 | T3 $42.30 · R/R 3.75
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $38.55


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.85 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.36 %)** : le gap seul le franchit 0.797 % des séances (10 fois sur 1254).
   - exécution **1.743 pt plus bas** dans le cas TYPIQUE (médiane), 5.578 au p90, **14.499 au pire**
   - perte réelle **10.638 %** en moyenne _(tirée par la queue)_, jusqu'à **21.859 %** — au lieu des 7.36 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0261 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 10 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.033 % | p01 -6.63 % | pire -21.859 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5202** [0.446 ; 0.5938] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4931** [0.4406 ; 0.5457] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4715** [0.4193 ; 0.5242] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (30.5 pt), swing (31.4 pt), deep (31.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 540 séances)** : VaR **-9.0 %** | CVaR **-12.13 %** | vol 6.97 %/j
   - _fenêtre arrêtée : rupture de regime a 600 seances en arriere (volatilite 3.60 % contre 6.02 % aujourd'hui, rapport 0.60)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -18.22 % vs -19.88 % si l'on extrapolait par √5 _(rapport 0.917 ; < 1 = le √5 surestime)_
- **β de baisse : 2.2175** (β de hausse 1.9862, asymétrie 1.1165) vs IWM — 602 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 35.1213 sur atr_grid (1.75 ATR, 11.13 %) — p(stop avant cible) 0.5274 [0.47 ; 0.58], R/R 2.33, perte reelle 15.082 % (gap inclus), CVaR 11.139 %, EV -1.3524 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.0538 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.527, borne haute 0.580 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.35 ATR (stop 5.27 %) — p(stop avant cible) 0.7728 [0.73 ; 0.81], R/R 4.705, perte reelle 7.47 % (gap inclus), EV -1.4218 % — **REFUSE**
      - refuse : cible atteinte seulement 7.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.773, borne haute 0.815 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.42 %) : P(cible) 7.2 % x 35.14 % + P(rien) 15.5 % x 11.70 % ne couvrent pas P(stop) 77.3 % x 7.47 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 support a 0.6 ATR (stop 6.867 %) — p(stop avant cible) 0.6992 [0.65 ; 0.75], R/R 3.404, perte reelle 10.324 % (gap inclus), EV -1.6549 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.699, borne haute 0.746 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.25 ATR du spot — compartiment <1, mesure a 45.8 % de casse (IC clusterise [0.427 ; 0.489] sur 1234 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.65 %) : P(cible) 8.6 % x 35.14 % + P(rien) 21.5 % x 11.81 % ne couvrent pas P(stop) 69.9 % x 10.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 9.54 %) — p(stop avant cible) 0.6019 [0.55 ; 0.65], R/R 2.516, perte reelle 13.966 % (gap inclus), EV -1.9605 % — **REFUSE**
      - refuse : cible atteinte seulement 9.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.602, borne haute 0.652 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.96 %) : P(cible) 9.4 % x 35.14 % + P(rien) 30.4 % x 10.29 % ne couvrent pas P(stop) 60.2 % x 13.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.12 ATR (stop 16.533 %) — p(stop avant cible) 0.2886 [0.24 ; 0.34], R/R 1.608, perte reelle 21.859 % (gap inclus), EV -0.7153 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.54 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.72 %) : P(cible) 10.6 % x 35.14 % + P(rien) 60.6 % x 3.10 % ne couvrent pas P(stop) 28.9 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.79 ATR (stop 27.135 %) — p(stop avant cible) 0.0774 [0.05 ; 0.11], R/R 1.295, perte reelle 27.135 % (gap inclus), EV 0.9954 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.13 % > budget 12.00 %
   - ⚪ grid_snapped a 0.35 ATR (stop 4.157 %) — p(stop avant cible) 0.8092 [0.77 ; 0.85], R/R 5.692, perte reelle 6.174 % (gap inclus), EV -1.2049 % — **REFUSE**
      - refuse : cible atteinte seulement 5.9 % du temps (< 15 %) meme a 10 seances : le R/R de 5.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.809, borne haute 0.848 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.20 %) : P(cible) 5.9 % x 35.14 % + P(rien) 13.2 % x 12.98 % ne couvrent pas P(stop) 80.9 % x 6.17 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 7.95 %) — p(stop avant cible) 0.6538 [0.60 ; 0.70], R/R 3.088, perte reelle 11.379 % (gap inclus), EV -1.3039 % — **REFUSE**
      - refuse : cible atteinte seulement 9.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.654, borne haute 0.703 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.30 %) : P(cible) 9.1 % x 35.14 % + P(rien) 25.5 % x 11.52 % ne couvrent pas P(stop) 65.4 % x 11.38 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 11.13 %) — p(stop avant cible) 0.5274 [0.47 ; 0.58], R/R 2.33, perte reelle 15.082 % (gap inclus), EV -1.3524 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.527, borne haute 0.580 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.35 %) : P(cible) 9.9 % x 35.14 % + P(rien) 37.3 % x 8.34 % ne couvrent pas P(stop) 52.7 % x 15.08 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 2.12 ATR (stop 15.42 %) — p(stop avant cible) 0.333 [0.28 ; 0.38], R/R 1.608, perte reelle 21.859 % (gap inclus), EV -1.5705 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.43 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.57 %) : P(cible) 10.6 % x 35.14 % + P(rien) 56.1 % x 3.56 % ne couvrent pas P(stop) 33.3 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 17.491 %) — p(stop avant cible) 0.2756 [0.23 ; 0.32], R/R 1.608, perte reelle 21.859 % (gap inclus), EV -0.4718 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.49 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.47 %) : P(cible) 10.6 % x 35.14 % + P(rien) 61.8 % x 2.94 % ne couvrent pas P(stop) 27.6 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 19.081 %) — p(stop avant cible) 0.226 [0.18 ; 0.27], R/R 1.608, perte reelle 21.859 % (gap inclus), EV 0.273 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.08 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 22.261 %) — p(stop avant cible) 0.1594 [0.12 ; 0.20], R/R 1.579, perte reelle 22.261 % (gap inclus), EV 1.0307 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.26 % > budget 12.00 %
   - 🟢 grid_snapped a 3.79 ATR (stop 26.022 %) — p(stop avant cible) 0.0958 [0.07 ; 0.13], R/R 1.351, perte reelle 26.022 % (gap inclus), EV 1.0027 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.02 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 28.621 %) — p(stop avant cible) 0.0721 [0.05 ; 0.10], R/R 1.228, perte reelle 28.621 % (gap inclus), EV 0.9007 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.62 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 31.801 %) — p(stop avant cible) 0.0425 [0.02 ; 0.07], R/R 1.105, perte reelle 31.801 % (gap inclus), EV 0.9102 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.80 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 34.981 %) — p(stop avant cible) 0.021 [0.01 ; 0.04], R/R 1.005, perte reelle 34.981 % (gap inclus), EV 0.9627 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.98 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 38.162 %) — p(stop avant cible) 0.0102 [0.00 ; 0.03], R/R 0.921, perte reelle 38.162 % (gap inclus), EV 1.0173 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.16 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 41.342 %) — p(stop avant cible) 0.006 [0.00 ; 0.02], R/R 0.85, perte reelle 41.342 % (gap inclus), EV 1.0195 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.34 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 44.522 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.789, perte reelle 44.522 % (gap inclus), EV 1.0473 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.52 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 47.702 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 0.737, perte reelle 47.702 % (gap inclus), EV 1.0684 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.70 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 50.882 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.691, perte reelle 50.882 % (gap inclus), EV 1.0864 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 50.88 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 39.52, ATR14 2.5136 (6.36 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.381 ATR = 2.423 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.318 % | 39.3943 | 93.66 % | 95.37 % | 96.07 % | 97.47 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.636 % | 39.2686 | 85.92 % | 91.14 % | 92.14 % | 94.65 % | 96.04 % | 96.92 % |
| 0.15 ATR | 0.954 % | 39.143 | 78.97 % | 86.3 % | 88.41 % | 91.72 % | 93.81 % | 95.69 % |
| 0.2 ATR | 1.272 % | 39.0173 | 71.53 % | 80.56 % | 84.38 % | 88.59 % | 91.07 % | 93.64 % |
| 0.25 ATR | 1.59 % | 38.8916 | 65.59 % | 76.64 % | 80.85 % | 85.96 % | 88.83 % | 92.1 % |
| 0.35 ATR | 2.226 % | 38.6403 | 53.12 % | 67.67 % | 74.29 % | 79.39 % | 84.16 % | 88.51 % |
| 0.5 ATR | 3.18 % | 38.2632 | 38.03 % | 54.68 % | 62.4 % | 71.11 % | 78.58 % | 84.51 % |
| 0.75 ATR | 4.77 % | 37.6348 | 22.33 % | 38.97 % | 48.29 % | 58.89 % | 68.93 % | 76.62 % |
| 1.0 ATR | 6.36 % | 37.0064 | 9.96 % | 24.47 % | 34.68 % | 45.96 % | 57.87 % | 67.9 % |
| 1.25 ATR | 7.95 % | 36.378 | 3.62 % | 14.3 % | 24.19 % | 34.85 % | 50.05 % | 61.54 % |
| 1.5 ATR | 9.54 % | 35.7496 | 1.01 % | 7.05 % | 15.83 % | 25.76 % | 41.22 % | 55.69 % |
| 2.0 ATR | 12.721 % | 34.4929 | 0.1 % | 1.91 % | 4.94 % | 14.44 % | 28.43 % | 44.41 % |
| 2.5 ATR | 15.901 % | 33.2361 | 0.0 % | 0.2 % | 1.21 % | 5.76 % | 18.07 % | 33.44 % |
| 3.0 ATR | 19.081 % | 31.9793 | 0.0 % | 0.1 % | 0.4 % | 2.63 % | 11.37 % | 25.74 % |
| 4.0 ATR | 25.441 % | 29.4657 | 0.0 % | 0.1 % | 0.1 % | 0.2 % | 2.94 % | 10.56 % |
| 6.0 ATR | 38.162 % | 24.4386 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.1 % | 1.23 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.58 ATR | 0.71 ATR | 0.80 ATR | 1.00 ATR | 1.20 ATR |
| **2 s.** | 0.27 ATR | 0.57 ATR | 0.65 ATR | 0.85 ATR | 0.99 ATR | 1.11 ATR | 1.40 ATR | 1.70 ATR |
| **3 s.** | 0.34 ATR | 0.72 ATR | 0.81 ATR | 1.04 ATR | 1.23 ATR | 1.38 ATR | 1.77 ATR | 2.00 ATR |
| **5 s.** | 0.43 ATR | 0.92 ATR | 1.02 ATR | 1.30 ATR | 1.53 ATR | 1.75 ATR | 2.26 ATR | 2.62 ATR |
| **10 s.** | 0.59 ATR | 1.25 ATR | 1.39 ATR | 1.82 ATR | 2.17 ATR | 2.41 ATR | 3.16 ATR | 3.76 ATR |
| **20 s.** | 0.80 ATR | 1.75 ATR | 1.97 ATR | 2.53 ATR | 3.05 ATR | 3.38 ATR | 4.12 ATR | 5.19 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.431–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.654–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.77 %, prix 37.6349), p(touche) 38.97 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.81–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.36 %, prix 37.0065), p(touche) 34.68 % (en stress 92.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.022–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.95 %, prix 36.3782), p(touche) 34.85 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.393–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.54 %, prix 35.7498), p(touche) 41.22 % (en stress 97.98 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.974–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (12.721 %, prix 34.4927), p(touche) 44.41 % (en stress 98.98 %)  ✅ optimum identifie (69.4 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.047 | EV/share : $0.037 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 45 % | T2 24 % | T3 24 %
- Kelly (position) : f* 0.042 | ¼-Kelly 0.01 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 63.8 | bear 27.7 | side 8.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.449% → cible +2.505% / stop −2.0%, p_fill 96%, n_eff≈38.8) : P(cible|rempli) **51%** · **EV/risk +0.210** (×p_fill ; si rempli +0.44% du capital)
  - **swing** (entrée dip −1.0% → cible +5.601% / stop −6.424%, p_fill 91%, n_eff≈36.5) : P(cible|rempli) **52%** · **EV/risk +0.083** (×p_fill ; si rempli +0.59% du capital)
  - **deep** (entrée dip −1.47% → cible +7.921% / stop −9.683%, p_fill 89%, n_eff≈35.5) : P(cible|rempli) **42%** · **EV/risk -0.212** (×p_fill ; si rempli -2.30% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→91% · +1.0%→82% · +2.0%→66% · +3.0%→55% · +5.0%→28% · +8.0%→12%
- Range intraday médian 7.27% (p90 11.71%) · excursion haute méd. +3.6% / basse méd. −2.65%
- Profil de vol intra : ouverture 4.994% vs midi 1.407% vs clôture 1.611% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 66% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.118 ; mean-reverting — autocorr -0.042)_ ; drift intra méd. 0.05% ; recovery-V 28%
- **σ réalisé intraday** 4.012% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 53% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 39.3778 (VA 39.1437–39.4753 ; dernier close 39.52)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 32% · rebond 77% · **stop −4.73%** sous le fill (sous le bruit) · cible +2.48% · R/R 0.52 (high win-rate)
- Gaps overnight (n=159) : méd. -0.44% · baisse 54% (gap-down >1% 39% · >2% 20%)
- Excursion ouverture 5min (n=160) : bas méd −1.14% (p90 −2.74%) · haut méd +1.35% · range méd 2.72%
- Excursion ouverture 15min (n=160) : bas méd −1.42% (p90 −3.85%) · haut méd +1.69% · range méd 3.56%
- Excursion ouverture 30min (n=160) : bas méd −1.81% (p90 −4.85%) · haut méd +2.05% · range méd 4.31%
- Excursion ouverture 60min (n=160) : bas méd −1.95% (p90 −5.3%) · haut méd +2.23% · range méd 4.91%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 39.52 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 78% (130/159) · gap 49% · délai 0.0min · rebond 58% (83/130) (MFE +1.8%)
   - −1.0% : fill 30min 67% · séance 72% (123/159) · gap 39% · délai 0.0min · rebond 67% (88/123) (MFE +2.21%)
   - −1.5% : fill 30min 61% · séance 67% (115/159) · gap 33% · délai 0.0min · rebond 69% (79/115) (MFE +1.96%)
   - −2.0% : fill 30min 54% · séance 60% (105/159) · gap 20% · délai 0.0min · rebond 71% (72/105) (MFE +2.19%)
   - −3.0% : fill 30min 43% · séance 51% (89/159) · gap 10% · délai 4.4min · rebond 68% (63/89) (MFE +2.33%)
   - −4.0% : fill 30min 26% · séance 42% (73/159) · gap 5% · délai 15.6min · rebond 65% (54/73) (MFE +2.14%)
   - −5.0% : fill 30min 17% · séance 32% (60/159) · gap 3% · délai 24.8min · rebond 77% (50/60) (MFE +2.48%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.76% (p90 −2.83%) → stop au-delà de −1.89% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.84% (p90 −2.85%) → stop au-delà de −1.94% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.78% (p90 −2.66%) → stop au-delà de −1.8% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1104 jambes) : jambe baissière méd −1.28% (p90 −2.98%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (81 séances) :
      · −1.0% : fill 100% (81/81) · rebond 66% (57/81)
      · −2.0% : fill 88% (74/81) · rebond 74% (55/74)
      · −3.0% : fill 75% (63/81) · rebond 68% (45/63)
      · −4.0% : fill 61% (50/81) · rebond 64% (37/50)
      · −5.0% : fill 46% (41/81) · rebond 69% (32/41)
   - **flat** (15 séances) :
      · −1.0% : fill 62% (11/15) · rebond 67% (7/11)
      · −2.0% : fill 55% (10/15) · rebond 79% (5/10)
      · −3.0% : fill 49% (8/15) · rebond 61% (5/8)
      · −4.0% : fill 42% (7/15) · rebond 54% (4/7)
      · −5.0% : fill 31% (6/15) · rebond 95% (5/6)
   - **gap-up** (63 séances) :
      · −1.0% : fill 36% (31/63) · rebond 73% (24/31)
      · −2.0% : fill 22% (21/63) · rebond 48% (12/21)
      · −3.0% : fill 19% (18/63) · rebond 76% (13/18)
      · −4.0% : fill 16% (16/63) · rebond 78% (13/16)
      · −5.0% : fill 14% (13/63) · rebond 100% (13/13)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 60% si les 15 1res min sont vertes (85 cas) · 28% si rouges (75 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:05** → P(séance verte=clôture>ouverture) 72% si début vert vs 17% si rouge (base 47% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 231min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **72%** · continue >prix actuel 41% ; creux résiduel méd -1.93% (q20 -3.68%) → **SL/trailing à −3.68%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.63% / q75 +2.84% → **scale +1.63% / runner +2.84%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **17%** (continue à baisser 53%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.75%** (au-delà de la MAE q10 -4.75%), cible rebond +1.8% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.52% .. +6.1%] · haut q95 +7.59% · bas q05 -5.47%
   - 60min (n=160) : retour [-4.88% .. +5.95%] · haut q95 +7.86% · bas q05 -6.04%
   - 2h (n=160) : retour [-6.29% .. +6.53%] · haut q95 +8.52% · bas q05 -6.97%
   - 4h (n=160) : retour [-6.89% .. +6.88%] · haut q95 +9.0% · bas q05 -8.03%
   - 6h (n=160) : retour [-7.11% .. +7.68%] · haut q95 +10.23% · bas q05 -8.07%
   - session (n=160) : retour [-6.38% .. +8.29%] · haut q95 +10.34% · bas q05 -8.2%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 7.7)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **23%**. Lecture précoce 30 min : signature présente → 13% vs absente 3% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.29% (p75 2.28% / p90 3.82%) · ~3.0 replis/séance, durée méd 69.04 min. P(nouveau plus-haut après repli) :
   - −0.5% → **85%** (reprise méd 24.37 min, n=47)
   - −1.0% → **78%** (reprise méd 68.85 min, n=30)
   - −1.5% → **68%** (reprise méd 81.24 min, n=16)
   - −2.0% → **67%** (reprise méd 84.17 min, n=12)
   - −3.0% → **75%** (reprise méd 175.72 min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−3.82%** (p90, défaut prudent ; serré/agressif −2.28%) ; extension open→close méd +8.23% (q75 +10.03% / q95 +16.4%), MFE méd +10.28% / q90 +13.1%
   - Échelle scale-out : +10.28% (33%) / +11.83% (33%) / +13.1% (34%)
- **DÉSARMER** : repli > **−3.82%** depuis le plus-haut = décay → P(retournement) **30%** (préavis méd 235.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.1% : P(retournement après) 0% (mèche méd 3.44%)
- **CONTEXTE** : la dernière heure tient les gains 80% du temps (retour médian dernière heure +0.52%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 35.2  _(momentum baissier)_
- **ADX** : 15.3  _(pas de tendance nette)_
- **MACD** : hist -0.381  _(pas de croisement recent)_
- **BB** : %B 0.27 · largeur 26.7%
- **ATR** : 2.51 (9.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.076  _(distribution)_
- **Vol ratio** : 0.75  _(volume normal)_
- **Choppiness** : 48.9  _(transition)_
- **MA** : MA20 42.06 · MA50 41.21 · MA200 44.22  _(prix < MA20)_
- **Dist MA** : MA20 -6.0% · MA50 -4.1% · MA200 -10.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (768183 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
