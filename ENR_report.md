# ENR

**Generated** : 2026-09-11T21:44:14.937456+00:00  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €144.26  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-11 — US Core CPI (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot €144.26 (+2.8% vs entrée) · entrée €140.32 · stop €129.09 · T1 €142.09 · R/R 0.16  
> ↳ P(T1 av. stop) 44 % _(réel 5 s)_ · EV/risk 0.011 _(réel 5 s)_ (GBM -0.06) · ¼-Kelly 0.095 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.200 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €139.96–€140.67 (mid €140.32)
- Spot actuel : €144.26 (+2.8% au-dessus de la zone — repli à attendre)
- Stop : €129.09 (stop swing_plan-based (-9.5%))
- Targets : T1 €142.09 · R/R 0.16 | T2 €143.87 · R/R 0.32 | T3 €145.65 · R/R 0.47
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €129.09


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.51 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (9.5 %)** : le gap seul le franchit 0.236 % des séances (3 fois sur 1273).
   - exécution **6.67 pt plus bas** dans le cas TYPIQUE (médiane), 22.34 au p90, **26.257 au pire**
   - perte réelle **21.854 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 9.5 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0291 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.307 % | p01 -5.092 % | pire -35.757 % _(sur 1273 séances)_
- **P(stop avant cible)** _(source : daily, 1274 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.009** [0.0015 ; 0.0323] _(largeur 3.1 pt, n_eff 173.1)_
   - swing : **0.4348** [0.3833 ; 0.4874] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4079** [0.357 ; 0.4603] _(largeur 10.3 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 16.2 observations effectives », dont la borne haute a 95 % vaut environ 18.5 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (45.0 pt), swing (53.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-4.63 %** | CVaR **-6.59 %** | vol 3.23 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 5.54 % contre 3.23 % aujourd'hui, rapport 1.71)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.69 % vs -9.74 % si l'on extrapolait par √5 _(rapport 0.892 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3544** (β de hausse 1.092, asymétrie 1.2403) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.378× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 131.6921 sur atr_grid (2.5 ATR, 8.712 %) — p(stop avant cible) 0.3252 [0.28 ; 0.38], R/R 1.624, perte reelle 18.578 % (gap inclus), CVaR 8.743 %, EV -3.0736 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 15 des 15 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 65.8 % de la queue et il ne reste que -887.74 EUR a partager. Prix du risque -0.635 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.227 %) — p(stop avant cible) 0.588 [0.54 ; 0.64], R/R 3.036, perte reelle 9.934 % (gap inclus), EV -2.8939 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.588, borne haute 0.639 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.89 %) : P(cible) 0.4 % x 30.16 % + P(rien) 40.8 % x 6.92 % ne couvrent pas P(stop) 58.8 % x 9.93 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.21 ATR (stop 6.205 %) — p(stop avant cible) 0.5136 [0.46 ; 0.57], R/R 2.228, perte reelle 13.536 % (gap inclus), EV -3.919 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.514, borne haute 0.566 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.92 %) : P(cible) 0.4 % x 30.16 % + P(rien) 48.2 % x 6.03 % ne couvrent pas P(stop) 51.4 % x 13.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 3.24 ATR (stop 13.256 %) — p(stop avant cible) 0.1004 [0.07 ; 0.14], R/R 1.38, perte reelle 21.854 % (gap inclus), EV 0.0375 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.28 % > budget 12.00 %
   - 🟢 support a 6.8 ATR (stop 25.665 %) — p(stop avant cible) 0.0043 [0.00 ; 0.02], R/R 0.844, perte reelle 35.757 % (gap inclus), EV 1.3201 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.67 % > budget 12.00 %
   - 🟢 support a 10.0 ATR (stop 36.813 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 0.819, perte reelle 36.813 % (gap inclus), EV 1.3858 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.81 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.871 %) — p(stop avant cible) 0.9324 [0.90 ; 0.96], R/R 13.76, perte reelle 2.192 % (gap inclus), EV -1.3041 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 13.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.932, borne haute 0.955 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.30 %) : P(cible) 0.2 % x 30.16 % + P(rien) 6.6 % x 10.48 % ne couvrent pas P(stop) 93.2 % x 2.19 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.742 %) — p(stop avant cible) 0.8523 [0.81 ; 0.89], R/R 8.154, perte reelle 3.699 % (gap inclus), EV -1.7334 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 8.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.852, borne haute 0.887 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.73 %) : P(cible) 0.2 % x 30.16 % + P(rien) 14.5 % x 9.26 % ne couvrent pas P(stop) 85.2 % x 3.70 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.614 %) — p(stop avant cible) 0.7821 [0.74 ; 0.82], R/R 5.877, perte reelle 5.132 % (gap inclus), EV -2.0399 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 5.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.782, borne haute 0.823 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.04 %) : P(cible) 0.4 % x 30.16 % + P(rien) 21.4 % x 8.65 % ne couvrent pas P(stop) 78.2 % x 5.13 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 6.97 %) — p(stop avant cible) 0.4662 [0.41 ; 0.52], R/R 2.047, perte reelle 14.737 % (gap inclus), EV -3.8113 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.81 %) : P(cible) 0.4 % x 30.16 % + P(rien) 53.0 % x 5.54 % ne couvrent pas P(stop) 46.6 % x 14.74 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 7.841 %) — p(stop avant cible) 0.3984 [0.35 ; 0.45], R/R 1.624, perte reelle 18.578 % (gap inclus), EV -4.226 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.23 %) : P(cible) 0.4 % x 30.16 % + P(rien) 59.7 % x 5.10 % ne couvrent pas P(stop) 39.8 % x 18.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 8.712 %) — p(stop avant cible) 0.3252 [0.28 ; 0.38], R/R 1.624, perte reelle 18.578 % (gap inclus), EV -3.0736 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.07 %) : P(cible) 0.4 % x 30.16 % + P(rien) 67.1 % x 4.24 % ne couvrent pas P(stop) 32.5 % x 18.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 9.583 %) — p(stop avant cible) 0.289 [0.24 ; 0.34], R/R 1.38, perte reelle 21.854 % (gap inclus), EV -3.3871 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.39 %) : P(cible) 0.4 % x 30.16 % + P(rien) 70.7 % x 3.96 % ne couvrent pas P(stop) 28.9 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 3.24 ATR (stop 12.329 %) — p(stop avant cible) 0.1407 [0.11 ; 0.18], R/R 1.38, perte reelle 21.854 % (gap inclus), EV -0.7001 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.35 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.70 %) : P(cible) 0.4 % x 30.16 % + P(rien) 85.5 % x 2.63 % ne couvrent pas P(stop) 14.1 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 13.939 %) — p(stop avant cible) 0.0849 [0.06 ; 0.12], R/R 1.162, perte reelle 25.963 % (gap inclus), EV -0.0858 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.96 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.09 %) : P(cible) 0.4 % x 30.16 % + P(rien) 91.1 % x 2.19 % ne couvrent pas P(stop) 8.5 % x 25.96 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 15.682 %) — p(stop avant cible) 0.0482 [0.03 ; 0.07], R/R 1.162, perte reelle 25.963 % (gap inclus), EV 0.6529 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.70 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 17.424 %) — p(stop avant cible) 0.0323 [0.02 ; 0.06], R/R 0.844, perte reelle 35.757 % (gap inclus), EV 0.6106 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.44 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 19.166 %) — p(stop avant cible) 0.0246 [0.01 ; 0.05], R/R 0.844, perte reelle 35.757 % (gap inclus), EV 0.8122 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.18 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 20.909 %) — p(stop avant cible) 0.0086 [0.00 ; 0.02], R/R 0.844, perte reelle 35.757 % (gap inclus), EV 1.1788 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.92 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 22.651 %) — p(stop avant cible) 0.0065 [0.00 ; 0.02], R/R 0.844, perte reelle 35.757 % (gap inclus), EV 1.2361 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.66 % > budget 12.00 %
   - 🟢 grid_snapped a 6.8 ATR (stop 24.738 %) — p(stop avant cible) 0.005 [0.00 ; 0.02], R/R 0.844, perte reelle 35.757 % (gap inclus), EV 1.2915 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.75 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 26.136 %) — p(stop avant cible) 0.0043 [0.00 ; 0.02], R/R 0.844, perte reelle 35.757 % (gap inclus), EV 1.3201 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.14 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 27.878 %) — p(stop avant cible) 0.0035 [0.00 ; 0.01], R/R 0.844, perte reelle 35.757 % (gap inclus), EV 1.3437 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.88 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 144.26, ATR14 5.0271 (3.485 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.366 ATR = 1.275 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.174 % | 144.0086 | 91.31 % | 93.97 % | 95.45 % | 96.23 % | 97.21 % | 97.89 % |
| 0.1 ATR | 0.348 % | 143.7573 | 83.71 % | 87.94 % | 90.5 % | 92.77 % | 94.62 % | 95.67 % |
| 0.15 ATR | 0.523 % | 143.5059 | 76.31 % | 82.31 % | 85.95 % | 88.8 % | 91.24 % | 93.26 % |
| 0.2 ATR | 0.697 % | 143.2546 | 70.29 % | 79.05 % | 83.09 % | 86.62 % | 89.44 % | 91.85 % |
| 0.25 ATR | 0.871 % | 143.0032 | 63.77 % | 74.8 % | 79.53 % | 83.45 % | 87.35 % | 90.44 % |
| 0.35 ATR | 1.22 % | 142.5005 | 51.63 % | 64.92 % | 70.62 % | 76.02 % | 81.97 % | 86.32 % |
| 0.5 ATR | 1.742 % | 141.7464 | 36.33 % | 51.88 % | 59.64 % | 66.5 % | 74.4 % | 80.18 % |
| 0.75 ATR | 2.614 % | 140.4896 | 19.84 % | 35.97 % | 45.2 % | 54.51 % | 65.34 % | 73.24 % |
| 1.0 ATR | 3.485 % | 139.2329 | 11.06 % | 25.4 % | 34.22 % | 44.0 % | 56.67 % | 64.89 % |
| 1.25 ATR | 4.356 % | 137.9761 | 6.02 % | 17.19 % | 24.83 % | 35.58 % | 48.11 % | 57.24 % |
| 1.5 ATR | 5.227 % | 136.7193 | 2.76 % | 10.97 % | 17.51 % | 27.45 % | 41.04 % | 50.91 % |
| 2.0 ATR | 6.97 % | 134.2057 | 0.79 % | 3.85 % | 8.41 % | 15.86 % | 27.99 % | 39.64 % |
| 2.5 ATR | 8.712 % | 131.6921 | 0.3 % | 1.98 % | 3.86 % | 9.12 % | 19.12 % | 29.88 % |
| 3.0 ATR | 10.454 % | 129.1786 | 0.1 % | 0.79 % | 1.88 % | 4.66 % | 12.05 % | 22.13 % |
| 4.0 ATR | 13.939 % | 124.1514 | 0.1 % | 0.4 % | 1.09 % | 2.28 % | 6.27 % | 12.37 % |
| 6.0 ATR | 20.909 % | 114.0971 | 0.0 % | 0.2 % | 0.4 % | 0.89 % | 2.19 % | 5.33 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.37 ATR | 0.41 ATR | 0.55 ATR | 0.67 ATR | 0.75 ATR | 1.05 ATR | 1.33 ATR |
| **2 s.** | 0.25 ATR | 0.53 ATR | 0.61 ATR | 0.82 ATR | 1.01 ATR | 1.16 ATR | 1.57 ATR | 1.92 ATR |
| **3 s.** | 0.30 ATR | 0.67 ATR | 0.76 ATR | 1.03 ATR | 1.25 ATR | 1.42 ATR | 1.91 ATR | 2.38 ATR |
| **5 s.** | 0.37 ATR | 0.86 ATR | 0.98 ATR | 1.33 ATR | 1.61 ATR | 1.82 ATR | 2.44 ATR | 2.96 ATR |
| **10 s.** | 0.49 ATR | 1.20 ATR | 1.36 ATR | 1.81 ATR | 2.17 ATR | 2.45 ATR | 3.35 ATR | 4.62 ATR |
| **20 s.** | 0.69 ATR | 1.54 ATR | 1.76 ATR | 2.34 ATR | 2.81 ATR | 3.22 ATR | 4.67 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.415–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.608–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.614 %, prix 140.489), p(touche) 35.97 % (en stress 91.18 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.755–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.485 %, prix 139.2325), p(touche) 34.22 % (en stress 91.18 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (85.9 % des re-echantillons)
- **5 seance(s)** : plage utile 0.976–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.485 %, prix 139.2325), p(touche) 44.0 % (en stress 99.01 %)  ✅ optimum identifie (91.1 % des re-echantillons)
- **10 seance(s)** : plage utile 1.36–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.227 %, prix 136.7195), p(touche) 41.04 % (en stress 100.0 %)  ✅ optimum identifie (93.4 % des re-echantillons)
- **20 seance(s)** : plage utile 1.762–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.97 %, prix 134.2051), p(touche) 39.64 % (en stress 99.0 %)  ✅ optimum identifie (88.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.06 | EV/share : €-0.679 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 28 % | T3 12 %
- Kelly (position) : f* 0.38 | ¼-Kelly 0.095 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 11.8 | bear 6.2 | side 81.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.739% → cible +1.267% / stop −8.0%, p_fill 34%, n_eff≈16.2) : P(cible|rempli) **44%** · **EV/risk +0.011** (×p_fill ; si rempli +0.26% du capital)
  - **swing** (entrée dip −6.015% → cible +2.834% / stop −3.708%, p_fill 22%, n_eff≈9.6) : P(cible|rempli) **67%** · **EV/risk +0.106** (×p_fill ; si rempli +1.75% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=12, n_eff=7))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→59% · +2.0%→39% · +3.0%→20% · +5.0%→8% · +8.0%→1%
- Range intraday médian 3.81% (p90 6.15%) · excursion haute méd. +1.47% / basse méd. −2.11%
- Profil de vol intra : ouverture 2.113% vs midi 0.87% vs clôture 1.056% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 10% · trend ↑1%/↓0% ; spike-down 58% · recovery-V 20%)_
- **Régime intraday** : **chop** _(efficiency 0.11 ; neutre — autocorr -0.022)_ ; drift intra méd. -0.48% ; recovery-V 14%
- **σ réalisé intraday** 2.425% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 72% / bas 69% / whipsaw 41%
- POC intraday (dernière séance, temps-au-prix) : 147.6975 (VA 146.6265–147.9355 ; dernier close 146.9)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 19% · rebond 66% · **stop −3.12%** sous le fill (sous le bruit) · cible +1.27% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.52% · baisse 33% (gap-down >1% 18% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.63% (p90 −1.67%) · haut méd +0.43% · range méd 1.16%
- Excursion ouverture 15min (n=160) : bas méd −0.79% (p90 −2.21%) · haut méd +0.58% · range méd 1.56%
- Excursion ouverture 30min (n=160) : bas méd −0.85% (p90 −2.28%) · haut méd +0.63% · range méd 1.92%
- Excursion ouverture 60min (n=160) : bas méd −1.0% (p90 −2.6%) · haut méd +0.74% · range méd 2.02%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 146.52 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 73% (116/159) · gap 25% · délai 0.4min · rebond 59% (65/116) (MFE +1.2%)
   - −1.0% : fill 30min 46% · séance 67% (107/159) · gap 18% · délai 6.9min · rebond 62% (62/107) (MFE +1.53%)
   - −1.5% : fill 30min 30% · séance 53% (89/159) · gap 14% · délai 10.1min · rebond 62% (53/89) (MFE +1.52%)
   - −2.0% : fill 30min 21% · séance 42% (74/159) · gap 10% · délai 33.3min · rebond 65% (50/74) (MFE +1.49%)
   - −3.0% : fill 30min 11% · séance 28% (52/159) · gap 4% · délai 208.4min · rebond 53% (33/52) (MFE +1.05%)
   - −4.0% : fill 30min 7% · séance 19% (38/159) · gap 2% · délai 129.6min · rebond 66% (27/38) (MFE +1.27%)
   - −5.0% : fill 30min 2% · séance 14% (25/159) · gap 0% · délai 398.5min · rebond 36% (13/25) (MFE +0.62%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.55% (p90 −1.58%) → stop au-delà de −1.06% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.47% (p90 −1.68%) → stop au-delà de −0.92% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.43% (p90 −0.97%) → stop au-delà de −0.72% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=543 jambes) : jambe baissière méd −1.09% (p90 −2.59%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (52 séances) :
      · −1.0% : fill 98% (51/52) · rebond 58% (28/51)
      · −2.0% : fill 73% (39/52) · rebond 49% (23/39)
      · −3.0% : fill 60% (31/52) · rebond 40% (18/31)
      · −4.0% : fill 48% (26/52) · rebond 71% (20/26)
      · −5.0% : fill 36% (18/52) · rebond 39% (11/18)
   - **flat** (14 séances) :
      · −1.0% : fill 85% (12/14) · rebond 91% (10/12)
      · −2.0% : fill 51% (8/14) · rebond 88% (6/8)
      · −3.0% : fill 25% (5/14) · rebond 76% (3/5)
      · −4.0% : fill 14% (4/14) · rebond 52% (2/4)
      · −5.0% : fill 11% (3/14) · rebond 0% (0/3)
   - **gap-up** (93 séances) :
      · −1.0% : fill 48% (44/93) · rebond 56% (24/44)
      · −2.0% : fill 25% (27/93) · rebond 78% (21/27)
      · −3.0% : fill 12% (16/93) · rebond 74% (12/16)
      · −4.0% : fill 5% (8/93) · rebond 50% (5/8)
      · −5.0% : fill 3% (4/93) · rebond 40% (2/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 75% si les 15 1res min sont vertes (75 cas) · 20% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:26** → P(séance verte=clôture>ouverture) 76% si début vert vs 21% si rouge (base 45% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **76%** · continue >prix actuel 56% ; creux résiduel méd -1.11% (q20 -2.16%) → **SL/trailing à −2.16%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.46% / q75 +2.28% → **scale +1.46% / runner +2.28%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **21%** (continue à baisser 56%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.96%** (au-delà de la MAE q10 -3.96%), cible rebond +1.22% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.05% .. +1.95%] · haut q95 +2.65% · bas q05 -2.71%
   - 60min (n=160) : retour [-2.48% .. +2.32%] · haut q95 +2.69% · bas q05 -2.94%
   - 2h (n=160) : retour [-2.79% .. +2.64%] · haut q95 +2.9% · bas q05 -3.6%
   - 4h (n=160) : retour [-3.15% .. +2.61%] · haut q95 +3.68% · bas q05 -3.96%
   - 6h (n=160) : retour [-3.7% .. +3.22%] · haut q95 +4.1% · bas q05 -4.58%
   - session (n=160) : retour [-4.9% .. +3.93%] · haut q95 +5.13% · bas q05 -6.19%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 1.3% / strong 4.4%) · base = 9 séances trend-up (n_eff 6.6)
- **ARMER** : fenêtre la + prédictive = **60 min** → P(reste trend-up à la clôture) **13%**. Lecture précoce 30 min : signature présente → 11% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.83% (p75 1.19% / p90 1.45%) · ~3.0 replis/séance, durée méd 78.78 min. P(nouveau plus-haut après repli) :
   - −0.5% → **99%** (reprise méd 55.57 min, n=25)
   - −1.0% → **100%** (reprise méd 80.0 min, n=10)
- **RIDER — climb (trail + cibles)** : trail **−1.45%** (p90, défaut prudent ; serré/agressif −1.19%) ; extension open→close méd +4.46% (q75 +6.49% / q95 +8.61%), MFE méd +5.07% / q90 +9.14%
   - Échelle scale-out : +5.07% (33%) / +6.83% (33%) / +9.14% (34%)
- **DÉSARMER** : repli > **−1.45%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +9.14% : P(retournement après) 0% (mèche méd 0.54%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.37%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-11 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 38.5  _(momentum baissier)_
- **ADX** : 11.6  _(pas de tendance nette)_
- **MACD** : hist -0.477  _(pas de croisement recent)_
- **BB** : %B 0.29 · largeur 16.4%
- **ATR** : 5.03 (30.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.201  _(distribution)_
- **Vol ratio** : 0.94  _(volume normal)_
- **Choppiness** : 52.5  _(transition)_
- **MA** : MA20 149.36 · MA50 151.33 · MA200 151.21  _(prix < MA20)_
- **Dist MA** : MA20 -3.4% · MA50 -4.7% · MA200 -4.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (771331 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
