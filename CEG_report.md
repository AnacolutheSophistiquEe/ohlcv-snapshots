# CEG

**Generated** : 2026-09-04T00:32:44.897519+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $285.01  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $285.01 (+1.9% vs entrée) · entrée $279.64 · stop $275.45 · T1 $282.61 · R/R 0.71  
> ↳ P(T1 av. stop) 33 % _(réel 5 s)_ · EV/risk -0.053 _(réel 5 s)_ (GBM 0.076) · ¼-Kelly 0.034 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -5.2 % ≠ (strike 275.0 − spot 285.01)/spot = -3.5 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -291 % hors [0,100] (R² max 0.91). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.080 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $279.05–$280.23 (mid $279.64)
- Spot actuel : $285.01 (+1.9% au-dessus de la zone — repli à attendre)
- Stop : $275.45 (stop swing_plan-based (-7.44%))
- Targets : T1 $282.61 · R/R 0.71 | T2 $285.58 · R/R 1.42 | T3 $288.55 · R/R 2.13
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $275.45


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.98 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (7.44 %)** : le gap seul le franchit 0.259 % des séances (3 fois sur 1160).
   - exécution **2.479 pt plus bas** dans le cas TYPIQUE (médiane), 7.203 au p90, **8.384 au pire**
   - perte réelle **11.211 %** en moyenne _(tirée par la queue)_, jusqu'à **15.824 %** — au lieu des 7.44 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0098 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.825 % | p01 -4.436 % | pire -15.824 % _(sur 1160 séances)_
- **P(stop avant cible)** _(source : daily, 1161 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.386** [0.3159 ; 0.4599] _(largeur 14.4 pt, n_eff 173.1)_
   - swing : **0.396** [0.3455 ; 0.4483] _(largeur 10.3 pt, n_eff 345.4)_
   - deep : **0.4016** [0.3509 ; 0.4539] _(largeur 10.3 pt, n_eff 345.4)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (45.8 pt), swing (58.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-4.5 %** | CVaR **-6.9 %** | vol 3.1 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 5.72 % contre 2.84 % aujourd'hui, rapport 2.01)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.62 % vs -9.56 % si l'on extrapolait par √5 _(rapport 1.006 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1843** (β de hausse 1.1871, asymétrie 0.9976) vs SPY — 532 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 252.1269 sur atr_grid (3.5 ATR, 11.538 %) — p(stop avant cible) 0.2267 [0.18 ; 0.27], R/R 1.995, perte reelle 15.824 % (gap inclus), CVaR 11.542 %, EV -1.1343 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.945 %) — p(stop avant cible) 0.5771 [0.52 ; 0.63], R/R 4.172, perte reelle 7.568 % (gap inclus), EV -1.4888 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.577, borne haute 0.628 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.49 %) : P(cible) 1.0 % x 31.57 % + P(rien) 41.3 % x 6.23 % ne couvrent pas P(stop) 57.7 % x 7.57 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.35 ATR (stop 9.663 %) — p(stop avant cible) 0.3035 [0.26 ; 0.35], R/R 2.453, perte reelle 12.871 % (gap inclus), EV -1.1888 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.19 %) : P(cible) 1.0 % x 31.57 % + P(rien) 68.7 % x 3.51 % ne couvrent pas P(stop) 30.3 % x 12.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 6.04 ATR (stop 21.824 %) — p(stop avant cible) 0.0117 [0.00 ; 0.03], R/R 1.447, perte reelle 21.824 % (gap inclus), EV 0.171 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.82 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.824 %) — p(stop avant cible) 0.9366 [0.91 ; 0.96], R/R 15.523, perte reelle 2.034 % (gap inclus), EV -1.2425 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 15.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.937, borne haute 0.959 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.24 %) : P(cible) 0.3 % x 31.57 % + P(rien) 6.0 % x 9.33 % ne couvrent pas P(stop) 93.7 % x 2.03 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.648 %) — p(stop avant cible) 0.8351 [0.79 ; 0.87], R/R 9.712, perte reelle 3.251 % (gap inclus), EV -1.1659 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 9.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.835, borne haute 0.871 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.17 %) : P(cible) 0.8 % x 31.57 % + P(rien) 15.7 % x 8.34 % ne couvrent pas P(stop) 83.5 % x 3.25 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.472 %) — p(stop avant cible) 0.7368 [0.69 ; 0.78], R/R 7.199, perte reelle 4.386 % (gap inclus), EV -0.9781 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 7.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.737, borne haute 0.781 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.98 %) : P(cible) 0.8 % x 31.57 % + P(rien) 25.5 % x 7.81 % ne couvrent pas P(stop) 73.7 % x 4.39 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.297 %) — p(stop avant cible) 0.6715 [0.62 ; 0.72], R/R 5.436, perte reelle 5.808 % (gap inclus), EV -1.2967 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.671, borne haute 0.719 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.30 %) : P(cible) 1.0 % x 31.57 % + P(rien) 31.9 % x 7.21 % ne couvrent pas P(stop) 67.2 % x 5.81 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.121 %) — p(stop avant cible) 0.6203 [0.57 ; 0.67], R/R 5.098, perte reelle 6.193 % (gap inclus), EV -1.0071 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.620, borne haute 0.670 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.01 %) : P(cible) 1.0 % x 31.57 % + P(rien) 37.0 % x 6.83 % ne couvrent pas P(stop) 62.0 % x 6.19 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 5.769 %) — p(stop avant cible) 0.5319 [0.48 ; 0.58], R/R 3.384, perte reelle 9.329 % (gap inclus), EV -2.0479 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.532, borne haute 0.584 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.05 %) : P(cible) 1.0 % x 31.57 % + P(rien) 45.8 % x 5.69 % ne couvrent pas P(stop) 53.2 % x 9.33 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 6.593 %) — p(stop avant cible) 0.4662 [0.41 ; 0.52], R/R 2.816, perte reelle 11.211 % (gap inclus), EV -2.243 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.24 %) : P(cible) 1.0 % x 31.57 % + P(rien) 52.4 % x 5.11 % ne couvrent pas P(stop) 46.6 % x 11.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.35 ATR (stop 8.733 %) — p(stop avant cible) 0.3385 [0.29 ; 0.39], R/R 2.453, perte reelle 12.871 % (gap inclus), EV -1.5867 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.59 %) : P(cible) 1.0 % x 31.57 % + P(rien) 65.2 % x 3.78 % ne couvrent pas P(stop) 33.9 % x 12.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 11.538 %) — p(stop avant cible) 0.2267 [0.18 ; 0.27], R/R 1.995, perte reelle 15.824 % (gap inclus), EV -1.1343 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.13 %) : P(cible) 1.0 % x 31.57 % + P(rien) 76.3 % x 2.79 % ne couvrent pas P(stop) 22.7 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 13.186 %) — p(stop avant cible) 0.1808 [0.14 ; 0.22], R/R 1.995, perte reelle 15.824 % (gap inclus), EV -0.6456 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.19 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.65 %) : P(cible) 1.0 % x 31.57 % + P(rien) 80.9 % x 2.34 % ne couvrent pas P(stop) 18.1 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 14.835 %) — p(stop avant cible) 0.1266 [0.09 ; 0.16], R/R 1.995, perte reelle 15.824 % (gap inclus), EV -0.2194 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.84 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.22 %) : P(cible) 1.0 % x 31.57 % + P(rien) 86.3 % x 1.69 % ne couvrent pas P(stop) 12.7 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 16.483 %) — p(stop avant cible) 0.0664 [0.04 ; 0.10], R/R 1.915, perte reelle 16.483 % (gap inclus), EV 0.0246 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.48 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 18.131 %) — p(stop avant cible) 0.051 [0.03 ; 0.08], R/R 1.741, perte reelle 18.131 % (gap inclus), EV 0.004 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.13 % > budget 12.00 %
   - 🟢 grid_snapped a 6.04 ATR (stop 20.894 %) — p(stop avant cible) 0.0143 [0.01 ; 0.03], R/R 1.511, perte reelle 20.894 % (gap inclus), EV 0.1646 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.89 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 23.076 %) — p(stop avant cible) 0.0102 [0.00 ; 0.03], R/R 1.368, perte reelle 23.076 % (gap inclus), EV 0.1696 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.08 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 24.725 %) — p(stop avant cible) 0.0081 [0.00 ; 0.02], R/R 1.277, perte reelle 24.725 % (gap inclus), EV 0.1928 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.72 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 26.373 %) — p(stop avant cible) 0.0069 [0.00 ; 0.02], R/R 1.197, perte reelle 26.373 % (gap inclus), EV 0.1893 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.37 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 285.012, ATR14 9.3957 (3.297 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.384 ATR = 1.266 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.165 % | 284.5422 | 91.56 % | 94.55 % | 95.55 % | 96.65 % | 97.53 % | 97.96 % |
| 0.1 ATR | 0.33 % | 284.0724 | 85.44 % | 90.32 % | 92.32 % | 93.97 % | 95.51 % | 96.71 % |
| 0.15 ATR | 0.494 % | 283.6026 | 78.89 % | 85.98 % | 88.31 % | 90.4 % | 93.6 % | 95.35 % |
| 0.2 ATR | 0.659 % | 283.1328 | 71.89 % | 80.53 % | 83.96 % | 86.61 % | 91.13 % | 93.98 % |
| 0.25 ATR | 0.824 % | 282.6631 | 64.89 % | 74.97 % | 79.18 % | 82.92 % | 88.33 % | 92.05 % |
| 0.35 ATR | 1.154 % | 281.7235 | 53.44 % | 65.41 % | 71.16 % | 76.45 % | 83.73 % | 88.42 % |
| 0.5 ATR | 1.648 % | 280.3141 | 38.44 % | 52.28 % | 59.02 % | 65.85 % | 76.43 % | 82.63 % |
| 0.75 ATR | 2.472 % | 277.9652 | 20.11 % | 36.04 % | 44.54 % | 52.68 % | 65.99 % | 75.6 % |
| 1.0 ATR | 3.297 % | 275.6163 | 11.11 % | 23.58 % | 32.63 % | 42.75 % | 56.79 % | 69.13 % |
| 1.25 ATR | 4.121 % | 273.2673 | 5.78 % | 16.02 % | 23.83 % | 35.04 % | 50.84 % | 62.88 % |
| 1.5 ATR | 4.945 % | 270.9184 | 2.78 % | 10.57 % | 17.15 % | 28.68 % | 44.11 % | 57.21 % |
| 2.0 ATR | 6.593 % | 266.2205 | 0.89 % | 4.34 % | 9.13 % | 17.75 % | 31.31 % | 46.2 % |
| 2.5 ATR | 8.242 % | 261.5226 | 0.44 % | 2.22 % | 4.68 % | 10.83 % | 20.88 % | 36.32 % |
| 3.0 ATR | 9.89 % | 256.8248 | 0.0 % | 1.11 % | 2.78 % | 6.7 % | 15.38 % | 28.38 % |
| 4.0 ATR | 13.186 % | 247.429 | 0.0 % | 0.22 % | 0.89 % | 2.57 % | 6.73 % | 14.19 % |
| 6.0 ATR | 19.78 % | 228.6375 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.79 % | 2.72 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.68 ATR | 0.75 ATR | 1.05 ATR | 1.31 ATR |
| **2 s.** | 0.25 ATR | 0.54 ATR | 0.61 ATR | 0.81 ATR | 0.97 ATR | 1.12 ATR | 1.55 ATR | 1.95 ATR |
| **3 s.** | 0.30 ATR | 0.66 ATR | 0.74 ATR | 0.99 ATR | 1.22 ATR | 1.39 ATR | 1.95 ATR | 2.46 ATR |
| **5 s.** | 0.37 ATR | 0.82 ATR | 0.94 ATR | 1.33 ATR | 1.67 ATR | 1.90 ATR | 2.60 ATR | 3.41 ATR |
| **10 s.** | 0.53 ATR | 1.28 ATR | 1.47 ATR | 1.93 ATR | 2.30 ATR | 2.58 ATR | 3.62 ATR | 4.58 ATR |
| **20 s.** | 0.77 ATR | 1.83 ATR | 2.06 ATR | 2.71 ATR | 3.24 ATR | 3.59 ATR | 4.73 ATR | 5.60 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.434–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.648 %, prix 280.315), p(touche) 38.44 % (en stress 82.22 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.612–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.472 %, prix 277.9665), p(touche) 36.04 % (en stress 88.89 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.742–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.472 %, prix 277.9665), p(touche) 44.54 % (en stress 97.78 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.943–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.297 %, prix 275.6151), p(touche) 42.75 % (en stress 96.67 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.467–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (4.945 %, prix 270.9182), p(touche) 44.11 % (en stress 98.89 %)  ✅ optimum identifie (74.5 % des re-echantillons)
- **20 seance(s)** : plage utile 2.061–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.242 %, prix 261.5213), p(touche) 36.32 % (en stress 95.51 %)  ✅ optimum identifie (87.4 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.076 | EV/share : $0.319 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 67 % | T2 34 % | T3 12 %
- Kelly (position) : f* 0.136 | ¼-Kelly 0.034 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 79.2 | bear 5.0 | side 15.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 285.0 (= 1 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.888% → cible +1.061% / stop −1.5%, p_fill 30%, n_eff≈14.5) : P(cible|rempli) **33%** · **EV/risk -0.053** (×p_fill ; si rempli -0.26% du capital)
  - **swing** (entrée dip −4.143% → cible +2.373% / stop −3.439%, p_fill 16%, n_eff≈8.8) : P(cible|rempli) **46%** · **EV/risk +0.004** (×p_fill ; si rempli +0.10% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=16, n_eff=7))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→71% · +2.0%→39% · +3.0%→16% · +5.0%→4% · +8.0%→0%
- Range intraday médian 3.19% (p90 5.36%) · excursion haute méd. +1.53% / basse méd. −1.13%
- Profil de vol intra : ouverture 2.336% vs midi 0.648% vs clôture 0.766% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 44% · recovery-V 13%)_
- **Régime intraday** : **chop** _(efficiency 0.116 ; mean-reverting — autocorr -0.061)_ ; drift intra méd. -0.094% ; recovery-V 6%
- **σ réalisé intraday** 2.25% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 65% / whipsaw 27%
- POC intraday (dernière séance, temps-au-prix) : 279.8442 (VA 277.5613–281.3663 ; dernier close 280.27)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 16% · rebond 41% · **stop −2.19%** sous le fill (sous le bruit) · cible +0.73% · R/R 0.33 (high win-rate)
- Gaps overnight (n=159) : méd. 0.54% · baisse 36% (gap-down >1% 12% · >2% 3%)
- Excursion ouverture 5min (n=160) : bas méd −0.58% (p90 −1.83%) · haut méd +0.88% · range méd 1.6%
- Excursion ouverture 15min (n=160) : bas méd −0.61% (p90 −2.17%) · haut méd +1.04% · range méd 1.98%
- Excursion ouverture 30min (n=160) : bas méd −0.71% (p90 −2.55%) · haut méd +1.22% · range méd 2.18%
- Excursion ouverture 60min (n=160) : bas méd −0.86% (p90 −2.85%) · haut méd +1.36% · range méd 2.48%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 280.31 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 46% · séance 62% (105/159) · gap 20% · délai 1.4min · rebond 58% (61/105) (MFE +1.13%)
   - −1.0% : fill 30min 34% · séance 50% (89/159) · gap 12% · délai 4.5min · rebond 49% (48/89) (MFE +0.98%)
   - −1.5% : fill 30min 26% · séance 38% (70/159) · gap 8% · délai 8.0min · rebond 42% (35/70) (MFE +0.82%)
   - −2.0% : fill 30min 21% · séance 33% (59/159) · gap 3% · délai 12.9min · rebond 56% (33/59) (MFE +1.1%)
   - −3.0% : fill 30min 6% · séance 16% (31/159) · gap 1% · délai 46.4min · rebond 41% (13/31) (MFE +0.73%)
   - −4.0% : fill 30min 3% · séance 9% (18/159) · gap 1% · délai 42.9min · rebond 63% (11/18) (MFE +1.2%)
   - −5.0% : fill 30min 2% · séance 4% (11/159) · gap 0% · délai 46.0min · rebond 88% (9/11) (MFE +1.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.27% (p90 −1.04%) → stop au-delà de −0.8% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.3% (p90 −0.98%) → stop au-delà de −0.89% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.52% (p90 −1.29%) → stop au-delà de −1.0% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=466 jambes) : jambe baissière méd −1.06% (p90 −2.51%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (42 séances) :
      · −1.0% : fill 88% (39/42) · rebond 68% (26/39)
      · −2.0% : fill 70% (31/42) · rebond 56% (18/31)
      · −3.0% : fill 34% (16/42) · rebond 27% (6/16)
      · −4.0% : fill 30% (13/42) · rebond 64% (8/13)
      · −5.0% : fill 15% (9/42) · rebond 87% (7/9)
   - **flat** (27 séances) :
      · −1.0% : fill 59% (20/27) · rebond 12% (5/20)
      · −2.0% : fill 38% (12/27) · rebond 46% (6/12)
      · −3.0% : fill 17% (7/27) · rebond 22% (2/7)
      · −4.0% : fill 6% (3/27) · rebond 42% (2/3)
      · −5.0% : fill 1% (1/27) · rebond 100% (1/1)
   - **gap-up** (90 séances) :
      · −1.0% : fill 30% (30/90) · rebond 46% (17/30)
      · −2.0% : fill 15% (16/90) · rebond 61% (9/16)
      · −3.0% : fill 8% (8/90) · rebond 80% (5/8)
      · −4.0% : fill 1% (2/90) · rebond 76% (1/2)
      · −5.0% : fill 0% (1/90) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 65% si les 15 1res min sont vertes (92 cas) · 33% si rouges (68 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:21** → P(séance verte=clôture>ouverture) 84% si début vert vs 10% si rouge (base 51% · écart 75 pts) ; prédictivité sature ensuite (plafond brut 194min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=84) : tient le vert **84%** · continue >prix actuel 46% ; creux résiduel méd -1.23% (q20 -1.9%) → **SL/trailing à −1.9%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.87% / q75 +1.31% → **scale +0.87% / runner +1.31%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **10%** (continue à baisser 66%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.34%** (au-delà de la MAE q10 -2.34%), cible rebond +0.93% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.09% .. +2.27%] · haut q95 +2.58% · bas q05 -3.42%
   - 60min (n=160) : retour [-3.64% .. +2.82%] · haut q95 +3.15% · bas q05 -4.61%
   - 2h (n=160) : retour [-3.7% .. +3.01%] · haut q95 +4.21% · bas q05 -4.64%
   - 4h (n=160) : retour [-2.97% .. +3.35%] · haut q95 +4.47% · bas q05 -4.67%
   - 6h (n=160) : retour [-4.04% .. +3.54%] · haut q95 +4.74% · bas q05 -4.71%
   - session (n=160) : retour [-3.62% .. +3.56%] · haut q95 +4.69% · bas q05 -4.71%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 5.0% / strong 1.9%) · base = 11 séances trend-up (n_eff 7.0)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **41%**. Lecture précoce 30 min : signature présente → 16% vs absente 3% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.05% (p75 1.37% / p90 2.39%) · ~2.0 replis/séance, durée méd 90.1 min. P(nouveau plus-haut après repli) :
   - −0.5% → **61%** (reprise méd 20.0 min, n=24)
   - −1.0% → **56%** (reprise méd 54.64 min, n=11)
   - −1.5% → **7%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.39%** (p90, défaut prudent ; serré/agressif −1.37%) ; extension open→close méd +3.51% (q75 +3.93% / q95 +5.58%), MFE méd +4.09% / q90 +5.3%
   - Échelle scale-out : +4.09% (33%) / +5.12% (33%) / +5.3% (34%)
- **DÉSARMER** : repli > **−2.39%** depuis le plus-haut = décay → P(retournement) **100%** (préavis méd 280.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.3% : P(retournement après) 0% (mèche méd 0.83%)
- **CONTEXTE** : la dernière heure tient les gains 95% du temps (retour médian dernière heure +0.37%)


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict buy_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 52.4  _(neutre)_
- **ADX** : 16.3  _(pas de tendance nette)_
- **MACD** : hist 0.671  _(pas de croisement recent)_
- **BB** : %B 0.86 · largeur 8.0%
- **ATR** : 9.4 (11.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.078  _(distribution)_
- **Vol ratio** : 1.1  _(volume normal)_
- **Choppiness** : 53.8  _(transition)_
- **MA** : MA20 277.06 · MA50 265.52 · MA200 295.67  _(prix > MA20)_
- **Dist MA** : MA20 +2.9% · MA50 +7.3% · MA200 -3.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (762911 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
