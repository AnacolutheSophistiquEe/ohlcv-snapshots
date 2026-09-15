# CEG

**Generated** : 2026-09-15T00:42:03.831962+00:00  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $264.64  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot $264.64 (+0.5% vs entrée) · entrée $263.37 · stop $253.07 · T1 $272.10 · R/R 0.85  
> ↳ P(T1 av. stop) 60 % _(réel 5 s)_ · EV/risk 0.095 _(réel 5 s)_ (GBM 0.002) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -1.7 % ≠ (strike 280.0 − spot 264.64)/spot = +5.8 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -48 % hors [0,100] (R² max 0.91). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.200 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $262.09–$264.64 (mid $263.37)
- Spot actuel : $264.64 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : $253.07 (stop swing_plan-based (-4.37%))
- Targets : T1 $272.10 · R/R 0.85 | T2 $280.82 · R/R 1.69 | T3 $289.55 · R/R 2.54
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $253.07


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.97 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (4.37 %)** : le gap seul le franchit 1.115 % des séances (13 fois sur 1166).
   - exécution **1.125 pt plus bas** dans le cas TYPIQUE (médiane), 5.143 au p90, **11.454 au pire**
   - perte réelle **6.642 %** en moyenne _(tirée par la queue)_, jusqu'à **15.824 %** — au lieu des 4.37 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0253 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 13 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.849 % | p01 -4.436 % | pire -15.824 % _(sur 1166 séances)_
- **P(stop avant cible)** _(source : daily, 1167 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4334** [0.3612 ; 0.5078] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4256** [0.3743 ; 0.4782] _(largeur 10.4 pt, n_eff 345.4)_
   - deep : **0.396** [0.3455 ; 0.4483] _(largeur 10.3 pt, n_eff 345.4)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (32.2 pt), swing (30.9 pt), deep (33.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-4.32 %** | CVaR **-6.35 %** | vol 3.01 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 5.91 % contre 2.76 % aujourd'hui, rapport 2.14)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.65 % vs -9.62 % si l'on extrapolait par √5 _(rapport 1.003 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1822** (β de hausse 1.1867, asymétrie 0.9962) vs SPY — 537 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 233.7619 sur atr_grid (3.0 ATR, 11.668 %) — p(stop avant cible) 0.2181 [0.18 ; 0.26], R/R 2.629, perte reelle 15.824 % (gap inclus), CVaR 11.672 %, EV -0.8796 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.18 ATR (stop 3.004 %) — p(stop avant cible) 0.6805 [0.63 ; 0.73], R/R 7.777, perte reelle 5.349 % (gap inclus), EV -1.0988 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 7.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.680, borne haute 0.728 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.10 %) : P(cible) 0.1 % x 41.60 % + P(rien) 31.8 % x 7.82 % ne couvrent pas P(stop) 68.0 % x 5.35 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 5.834 %) — p(stop avant cible) 0.5086 [0.46 ; 0.56], R/R 4.459, perte reelle 9.329 % (gap inclus), EV -1.7603 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.509, borne haute 0.561 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.76 %) : P(cible) 0.2 % x 41.60 % + P(rien) 49.0 % x 5.95 % ne couvrent pas P(stop) 50.9 % x 9.33 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 support a 3.53 ATR (stop 16.034 %) — p(stop avant cible) 0.0778 [0.05 ; 0.11], R/R 2.594, perte reelle 16.034 % (gap inclus), EV 0.1745 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.03 % > budget 12.00 %
      - ⚠ support DETECTE a 0.08 ATR du spot — compartiment <1, mesure a 47.5 % de casse (IC clusterise [0.444 ; 0.508] sur 1193 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ grid_snapped a 0.18 ATR (stop 1.876 %) — p(stop avant cible) 0.8116 [0.77 ; 0.85], R/R 11.511, perte reelle 3.614 % (gap inclus), EV -1.1792 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 11.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.812, borne haute 0.850 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.18 %) : P(cible) 0.1 % x 41.60 % + P(rien) 18.7 % x 9.09 % ne couvrent pas P(stop) 81.2 % x 3.61 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.889 %) — p(stop avant cible) 0.6293 [0.58 ; 0.68], R/R 6.861, perte reelle 6.063 % (gap inclus), EV -0.9743 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 6.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.629, borne haute 0.679 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.97 %) : P(cible) 0.2 % x 41.60 % + P(rien) 36.9 % x 7.51 % ne couvrent pas P(stop) 62.9 % x 6.06 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.862 %) — p(stop avant cible) 0.5586 [0.51 ; 0.61], R/R 5.497, perte reelle 7.568 % (gap inclus), EV -1.2632 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 5.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.559, borne haute 0.610 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.26 %) : P(cible) 0.2 % x 41.60 % + P(rien) 44.0 % x 6.58 % ne couvrent pas P(stop) 55.9 % x 7.57 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 6.806 %) — p(stop avant cible) 0.4296 [0.38 ; 0.48], R/R 3.711, perte reelle 11.211 % (gap inclus), EV -1.7728 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.77 %) : P(cible) 0.2 % x 41.60 % + P(rien) 56.9 % x 5.23 % ne couvrent pas P(stop) 43.0 % x 11.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 7.779 %) — p(stop avant cible) 0.3656 [0.32 ; 0.42], R/R 3.711, perte reelle 11.211 % (gap inclus), EV -1.1739 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.17 %) : P(cible) 0.2 % x 41.60 % + P(rien) 63.3 % x 4.51 % ne couvrent pas P(stop) 36.6 % x 11.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 8.751 %) — p(stop avant cible) 0.3264 [0.28 ; 0.38], R/R 3.232, perte reelle 12.871 % (gap inclus), EV -1.3442 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.34 %) : P(cible) 0.2 % x 41.60 % + P(rien) 67.2 % x 4.15 % ne couvrent pas P(stop) 32.6 % x 12.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 9.723 %) — p(stop avant cible) 0.2902 [0.24 ; 0.34], R/R 3.232, perte reelle 12.871 % (gap inclus), EV -0.9371 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.94 %) : P(cible) 0.2 % x 41.60 % + P(rien) 70.8 % x 3.85 % ne couvrent pas P(stop) 29.0 % x 12.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 10.696 %) — p(stop avant cible) 0.2526 [0.21 ; 0.30], R/R 2.629, perte reelle 15.824 % (gap inclus), EV -1.3104 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.31 %) : P(cible) 0.2 % x 41.60 % + P(rien) 74.6 % x 3.51 % ne couvrent pas P(stop) 25.3 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 11.668 %) — p(stop avant cible) 0.2181 [0.18 ; 0.26], R/R 2.629, perte reelle 15.824 % (gap inclus), EV -0.8796 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.88 %) : P(cible) 0.2 % x 41.60 % + P(rien) 78.0 % x 3.21 % ne couvrent pas P(stop) 21.8 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 grid_snapped a 3.53 ATR (stop 14.907 %) — p(stop avant cible) 0.12 [0.09 ; 0.16], R/R 2.629, perte reelle 15.824 % (gap inclus), EV -0.0233 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.91 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.02 %) : P(cible) 0.2 % x 41.60 % + P(rien) 87.8 % x 2.06 % ne couvrent pas P(stop) 12.0 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 17.502 %) — p(stop avant cible) 0.0501 [0.03 ; 0.08], R/R 2.377, perte reelle 17.502 % (gap inclus), EV 0.2168 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.50 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 19.447 %) — p(stop avant cible) 0.0288 [0.01 ; 0.05], R/R 2.139, perte reelle 19.447 % (gap inclus), EV 0.2706 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.45 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 21.391 %) — p(stop avant cible) 0.0132 [0.00 ; 0.03], R/R 1.945, perte reelle 21.391 % (gap inclus), EV 0.3475 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.39 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 23.336 %) — p(stop avant cible) 0.0089 [0.00 ; 0.02], R/R 1.783, perte reelle 23.336 % (gap inclus), EV 0.3621 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.34 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 25.281 %) — p(stop avant cible) 0.0079 [0.00 ; 0.02], R/R 1.646, perte reelle 25.281 % (gap inclus), EV 0.3662 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.28 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 27.225 %) — p(stop avant cible) 0.0067 [0.00 ; 0.02], R/R 1.528, perte reelle 27.225 % (gap inclus), EV 0.3624 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.22 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 29.17 %) — p(stop avant cible) 0.0039 [0.00 ; 0.02], R/R 1.426, perte reelle 29.17 % (gap inclus), EV 0.3707 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.17 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 31.115 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 1.337, perte reelle 31.115 % (gap inclus), EV 0.3759 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.11 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 264.64, ATR14 10.2927 (3.889 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.386 ATR = 1.501 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.194 % | 264.1254 | 91.5 % | 94.48 % | 95.46 % | 96.56 % | 97.55 % | 97.97 % |
| 0.1 ATR | 0.389 % | 263.6107 | 85.43 % | 90.28 % | 92.26 % | 93.9 % | 95.54 % | 96.73 % |
| 0.15 ATR | 0.583 % | 263.0961 | 78.92 % | 85.97 % | 88.27 % | 90.35 % | 93.65 % | 95.38 % |
| 0.2 ATR | 0.778 % | 262.5815 | 71.96 % | 80.55 % | 83.85 % | 86.47 % | 91.19 % | 94.02 % |
| 0.25 ATR | 0.972 % | 262.0668 | 65.01 % | 74.92 % | 78.98 % | 82.71 % | 88.41 % | 92.0 % |
| 0.35 ATR | 1.361 % | 261.0376 | 53.64 % | 65.41 % | 71.02 % | 76.27 % | 83.84 % | 88.39 % |
| 0.5 ATR | 1.945 % | 259.4937 | 38.52 % | 52.38 % | 58.96 % | 65.63 % | 76.48 % | 82.53 % |
| 0.75 ATR | 2.917 % | 256.9205 | 20.2 % | 36.13 % | 44.58 % | 52.66 % | 65.89 % | 75.42 % |
| 1.0 ATR | 3.889 % | 254.3473 | 11.15 % | 23.76 % | 32.74 % | 42.68 % | 56.74 % | 69.0 % |
| 1.25 ATR | 4.862 % | 251.7741 | 5.74 % | 15.91 % | 23.89 % | 34.92 % | 50.72 % | 62.8 % |
| 1.5 ATR | 5.834 % | 249.2009 | 2.76 % | 10.5 % | 17.15 % | 28.6 % | 44.04 % | 57.05 % |
| 2.0 ATR | 7.779 % | 244.0546 | 0.88 % | 4.31 % | 9.07 % | 17.63 % | 31.1 % | 45.89 % |
| 2.5 ATR | 9.723 % | 238.9082 | 0.44 % | 2.21 % | 4.65 % | 10.75 % | 20.74 % | 36.08 % |
| 3.0 ATR | 11.668 % | 233.7619 | 0.0 % | 1.1 % | 2.77 % | 6.65 % | 15.27 % | 28.18 % |
| 4.0 ATR | 15.557 % | 223.4692 | 0.0 % | 0.22 % | 0.88 % | 2.55 % | 6.69 % | 14.09 % |
| 6.0 ATR | 23.336 % | 202.8837 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.78 % | 2.71 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.39 ATR | 0.44 ATR | 0.57 ATR | 0.68 ATR | 0.76 ATR | 1.05 ATR | 1.31 ATR |
| **2 s.** | 0.25 ATR | 0.54 ATR | 0.61 ATR | 0.81 ATR | 0.97 ATR | 1.12 ATR | 1.54 ATR | 1.94 ATR |
| **3 s.** | 0.30 ATR | 0.66 ATR | 0.74 ATR | 0.99 ATR | 1.22 ATR | 1.39 ATR | 1.94 ATR | 2.46 ATR |
| **5 s.** | 0.37 ATR | 0.82 ATR | 0.94 ATR | 1.33 ATR | 1.66 ATR | 1.89 ATR | 2.59 ATR | 3.40 ATR |
| **10 s.** | 0.54 ATR | 1.28 ATR | 1.46 ATR | 1.93 ATR | 2.29 ATR | 2.57 ATR | 3.61 ATR | 4.57 ATR |
| **20 s.** | 0.77 ATR | 1.82 ATR | 2.04 ATR | 2.69 ATR | 3.23 ATR | 3.58 ATR | 4.72 ATR | 5.60 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.436–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.945 %, prix 259.4928), p(touche) 38.52 % (en stress 82.42 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.614–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.917 %, prix 256.9205), p(touche) 36.13 % (en stress 87.91 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.743–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.917 %, prix 256.9205), p(touche) 44.58 % (en stress 97.8 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.942–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.889 %, prix 254.3482), p(touche) 42.68 % (en stress 96.7 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.464–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.834 %, prix 249.2009), p(touche) 44.04 % (en stress 98.89 %)  ✅ optimum identifie (74.2 % des re-echantillons)
- **20 seance(s)** : plage utile 2.045–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (9.723 %, prix 238.9091), p(touche) 36.08 % (en stress 95.51 %)  ✅ optimum identifie (88.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.002 | EV/share : $0.016 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 29 % | T3 14 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 69.8 | bear 10.6 | side 19.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.305% → cible +1.482% / stop −1.5%, p_fill 79%, n_eff≈34.5) : P(cible|rempli) **49%** · **EV/risk +0.006** (×p_fill ; si rempli +0.01% du capital)
  - **swing** (entrée dip −0.481% → cible +3.315% / stop −3.908%, p_fill 88%, n_eff≈36.3) : P(cible|rempli) **60%** · **EV/risk +0.095** (×p_fill ; si rempli +0.42% du capital)
  - **deep** (entrée dip −0.616% → cible +4.688% / stop −5.87%, p_fill 82%, n_eff≈32.6) : P(cible|rempli) **55%** · **EV/risk +0.147** (×p_fill ; si rempli +1.05% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→72% · +2.0%→41% · +3.0%→19% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.29% (p90 5.36%) · excursion haute méd. +1.62% / basse méd. −1.05%
- Profil de vol intra : ouverture 2.272% vs midi 0.634% vs clôture 0.766% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 18% · trend ↑2%/↓0% ; spike-down 43% · recovery-V 13%)_
- **Régime intraday** : **chop** _(efficiency 0.145 ; mean-reverting — autocorr -0.05)_ ; drift intra méd. 0.205% ; recovery-V 6%
- **σ réalisé intraday** 2.217% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 60% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 294.8769 (VA 290.6501–297.1824 ; dernier close 298.95)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 16% · rebond 41% · **stop −2.19%** sous le fill (sous le bruit) · cible +0.73% · R/R 0.33 (high win-rate)
- Gaps overnight (n=159) : méd. 0.52% · baisse 37% (gap-down >1% 11% · >2% 3%)
- Excursion ouverture 5min (n=160) : bas méd −0.54% (p90 −1.78%) · haut méd +0.88% · range méd 1.53%
- Excursion ouverture 15min (n=160) : bas méd −0.6% (p90 −2.1%) · haut méd +1.05% · range méd 1.91%
- Excursion ouverture 30min (n=160) : bas méd −0.65% (p90 −2.52%) · haut méd +1.26% · range méd 2.17%
- Excursion ouverture 60min (n=160) : bas méd −0.84% (p90 −2.75%) · haut méd +1.39% · range méd 2.51%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 298.96 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 45% · séance 62% (105/159) · gap 19% · délai 1.4min · rebond 57% (61/105) (MFE +1.13%)
   - −1.0% : fill 30min 32% · séance 49% (88/159) · gap 11% · délai 5.3min · rebond 47% (46/88) (MFE +0.97%)
   - −1.5% : fill 30min 24% · séance 38% (70/159) · gap 8% · délai 10.4min · rebond 45% (36/70) (MFE +0.86%)
   - −2.0% : fill 30min 20% · séance 33% (59/159) · gap 3% · délai 15.3min · rebond 53% (33/59) (MFE +1.07%)
   - −3.0% : fill 30min 6% · séance 16% (31/159) · gap 1% · délai 46.4min · rebond 41% (13/31) (MFE +0.73%)
   - −4.0% : fill 30min 3% · séance 9% (18/159) · gap 1% · délai 42.9min · rebond 63% (11/18) (MFE +1.2%)
   - −5.0% : fill 30min 2% · séance 4% (11/159) · gap 0% · délai 46.0min · rebond 88% (9/11) (MFE +1.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.27% (p90 −0.98%) → stop au-delà de −0.82% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.3% (p90 −0.98%) → stop au-delà de −0.87% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.52% (p90 −1.17%) → stop au-delà de −0.92% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=464 jambes) : jambe baissière méd −1.06% (p90 −2.57%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (42 séances) :
      · −1.0% : fill 82% (38/42) · rebond 68% (25/38)
      · −2.0% : fill 65% (31/42) · rebond 56% (18/31)
      · −3.0% : fill 32% (16/42) · rebond 27% (6/16)
      · −4.0% : fill 28% (13/42) · rebond 64% (8/13)
      · −5.0% : fill 14% (9/42) · rebond 87% (7/9)
   - **flat** (28 séances) :
      · −1.0% : fill 53% (20/28) · rebond 12% (5/20)
      · −2.0% : fill 34% (12/28) · rebond 46% (6/12)
      · −3.0% : fill 16% (7/28) · rebond 22% (2/7)
      · −4.0% : fill 5% (3/28) · rebond 42% (2/3)
      · −5.0% : fill 1% (1/28) · rebond 100% (1/1)
   - **gap-up** (89 séances) :
      · −1.0% : fill 32% (30/89) · rebond 41% (16/30)
      · −2.0% : fill 18% (16/89) · rebond 51% (9/16)
      · −3.0% : fill 8% (8/89) · rebond 80% (5/8)
      · −4.0% : fill 1% (2/89) · rebond 76% (1/2)
      · −5.0% : fill 0% (1/89) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 64% si les 15 1res min sont vertes (93 cas) · 36% si rouges (67 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:21** → P(séance verte=clôture>ouverture) 85% si début vert vs 9% si rouge (base 52% · écart 76 pts) ; prédictivité sature ensuite (plafond brut 194min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=85) : tient le vert **85%** · continue >prix actuel 49% ; creux résiduel méd -0.97% (q20 -1.87%) → **SL/trailing à −1.87%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.92% / q75 +1.46% → **scale +0.92% / runner +1.46%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **9%** (continue à baisser 67%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.33%** (au-delà de la MAE q10 -2.33%), cible rebond +0.92% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.08% .. +2.26%] · haut q95 +2.56% · bas q05 -3.33%
   - 60min (n=160) : retour [-3.64% .. +2.77%] · haut q95 +3.06% · bas q05 -4.54%
   - 2h (n=160) : retour [-3.69% .. +3.01%] · haut q95 +4.2% · bas q05 -4.61%
   - 4h (n=160) : retour [-2.93% .. +3.48%] · haut q95 +4.39% · bas q05 -4.64%
   - 6h (n=160) : retour [-3.85% .. +3.99%] · haut q95 +5.02% · bas q05 -4.7%
   - session (n=160) : retour [-3.6% .. +3.78%] · haut q95 +5.18% · bas q05 -4.7%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.1% des séances sont trend-up (mild 5.6% / strong 2.5%) · base = 13 séances trend-up (n_eff 8.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **46%**. Lecture précoce 30 min : signature présente → 19% vs absente 6% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.09% (p75 1.89% / p90 2.34%) · ~1.0 replis/séance, durée méd 156.17 min. P(nouveau plus-haut après repli) :
   - −0.5% → **66%** (reprise méd 24.0 min, n=25)
   - −1.0% → **65%** (reprise méd 179.97 min, n=12)
   - −1.5% → **48%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.34%** (p90, défaut prudent ; serré/agressif −1.89%) ; extension open→close méd +3.6% (q75 +4.62% / q95 +6.15%), MFE méd +4.44% / q90 +5.76%
   - Échelle scale-out : +4.44% (33%) / +5.28% (33%) / +5.76% (34%)
- **DÉSARMER** : repli > **−2.34%** depuis le plus-haut = décay → P(retournement) **100%** (préavis méd 280.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.76% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 97% du temps (retour médian dernière heure +0.44%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict buy_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 44.8  _(momentum baissier)_
- **ADX** : 17.4  _(pas de tendance nette)_
- **MACD** : hist -1.487  _(bearish_recent)_
- **BB** : %B 0.08 · largeur 13.6%
- **ATR** : 10.29 (20.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.196  _(distribution)_
- **Vol ratio** : 1.26  _(volume normal)_
- **Choppiness** : 47.2  _(transition)_
- **MA** : MA20 280.63 · MA50 269.79 · MA200 293.98  _(prix < MA20)_
- **Dist MA** : MA20 -5.7% · MA50 -1.9% · MA200 -10.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (760798 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
