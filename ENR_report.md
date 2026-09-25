# ENR

**Generated** : 2026-09-25T21:43:57.518831+00:00  
**Santé technique** : 4/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €142.60  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)  
> ↳ spot €142.60 (+5.7% vs entrée) · entrée €134.95 · stop €130.00 · T1 €139.74 · R/R 0.97  
> ↳ P(T1 av. stop) 75 % · EV/risk 0.192 · ¼-Kelly 0.007 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.210 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €133.99–€135.91 (mid €134.95)
- Spot actuel : €142.60 (+5.7% au-dessus de la zone — repli à attendre)
- Stop : €130.00 (stop swing_plan-based (-8.83%))
- Targets : T1 €139.74 · R/R 0.97 | T2 €144.53 · R/R 1.94 | T3 €149.32 · R/R 2.9
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €130.00


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.59 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.83 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1274).
   - exécution **7.34 pt plus bas** dans le cas TYPIQUE (médiane), 23.01 au p90, **26.927 au pire**
   - perte réelle **21.854 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 8.83 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0307 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.33 % | p01 -5.088 % | pire -35.757 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0079** [0.0012 ; 0.0305] _(largeur 2.9 pt, n_eff 173.1)_
   - swing : **0.4935** [0.441 ; 0.5461] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4734** [0.4212 ; 0.5261] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 18.1 observations effectives », dont la borne haute a 95 % vaut environ 16.6 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (41.1 pt), swing (50.6 pt), deep (46.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-4.63 %** | CVaR **-6.59 %** | vol 3.19 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 5.95 % contre 3.00 % aujourd'hui, rapport 1.98)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.81 % vs -9.75 % si l'on extrapolait par √5 _(rapport 0.904 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3533** (β de hausse 1.0895, asymétrie 1.2421) vs GDAXI — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.352× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 127.0205 sur swing_based (2.49 ATR, 10.925 %) — p(stop avant cible) 0.2061 [0.17 ; 0.25], R/R 1.45, perte reelle 21.854 % (gap inclus), CVaR 10.951 %, EV -2.1207 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 22 des 22 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 49.8 % de la queue et il ne reste que -1061.59 EUR a partager. Prix du risque -0.364 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.204 %) — p(stop avant cible) 0.6083 [0.56 ; 0.66], R/R 3.19, perte reelle 9.934 % (gap inclus), EV -3.2845 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.608, borne haute 0.659 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.28 %) : P(cible) 0.4 % x 31.69 % + P(rien) 38.8 % x 6.82 % ne couvrent pas P(stop) 60.8 % x 9.93 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.49 ATR (stop 10.925 %) — p(stop avant cible) 0.2061 [0.17 ; 0.25], R/R 1.45, perte reelle 21.854 % (gap inclus), EV -2.1207 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.12 %) : P(cible) 0.4 % x 31.69 % + P(rien) 79.0 % x 2.88 % ne couvrent pas P(stop) 20.6 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 2.91 ATR (stop 12.395 %) — p(stop avant cible) 0.132 [0.10 ; 0.17], R/R 1.45, perte reelle 21.854 % (gap inclus), EV -0.8266 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.42 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.83 %) : P(cible) 0.4 % x 31.69 % + P(rien) 86.4 % x 2.25 % ne couvrent pas P(stop) 13.2 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 6.57 ATR (stop 25.098 %) — p(stop avant cible) 0.004 [0.00 ; 0.02], R/R 0.886, perte reelle 35.757 % (gap inclus), EV 1.0697 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.11 % > budget 12.00 %
   - 🟢 support a 9.82 ATR (stop 36.375 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 0.871, perte reelle 36.375 % (gap inclus), EV 1.1315 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.38 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.867 %) — p(stop avant cible) 0.9366 [0.91 ; 0.96], R/R 14.472, perte reelle 2.19 % (gap inclus), EV -1.3565 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 14.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.937, borne haute 0.959 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.36 %) : P(cible) 0.1 % x 31.69 % + P(rien) 6.2 % x 10.52 % ne couvrent pas P(stop) 93.7 % x 2.19 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.735 %) — p(stop avant cible) 0.8614 [0.82 ; 0.89], R/R 8.522, perte reelle 3.719 % (gap inclus), EV -1.8724 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 8.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.861, borne haute 0.895 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.87 %) : P(cible) 0.2 % x 31.69 % + P(rien) 13.7 % x 9.30 % ne couvrent pas P(stop) 86.1 % x 3.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.602 %) — p(stop avant cible) 0.7982 [0.75 ; 0.84], R/R 6.212, perte reelle 5.102 % (gap inclus), EV -2.2492 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 6.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.798, borne haute 0.838 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.25 %) : P(cible) 0.4 % x 31.69 % + P(rien) 19.8 % x 8.63 % ne couvrent pas P(stop) 79.8 % x 5.10 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.469 %) — p(stop avant cible) 0.7154 [0.67 ; 0.76], R/R 4.541, perte reelle 6.98 % (gap inclus), EV -2.6076 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 4.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.715, borne haute 0.761 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.61 %) : P(cible) 0.4 % x 31.69 % + P(rien) 28.1 % x 8.09 % ne couvrent pas P(stop) 71.5 % x 6.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.337 %) — p(stop avant cible) 0.6453 [0.59 ; 0.69], R/R 3.927, perte reelle 8.071 % (gap inclus), EV -2.5242 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.645, borne haute 0.694 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.52 %) : P(cible) 0.4 % x 31.69 % + P(rien) 35.1 % x 7.33 % ne couvrent pas P(stop) 64.5 % x 8.07 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 6.071 %) — p(stop avant cible) 0.5394 [0.49 ; 0.59], R/R 2.514, perte reelle 12.609 % (gap inclus), EV -3.9634 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.539, borne haute 0.591 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.96 %) : P(cible) 0.4 % x 31.69 % + P(rien) 45.7 % x 5.97 % ne couvrent pas P(stop) 53.9 % x 12.61 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 6.938 %) — p(stop avant cible) 0.4827 [0.43 ; 0.54], R/R 2.151, perte reelle 14.737 % (gap inclus), EV -4.3104 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.31 %) : P(cible) 0.4 % x 31.69 % + P(rien) 51.4 % x 5.24 % ne couvrent pas P(stop) 48.3 % x 14.74 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.49 ATR (stop 9.673 %) — p(stop avant cible) 0.291 [0.24 ; 0.34], R/R 1.45, perte reelle 21.854 % (gap inclus), EV -3.73 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.73 %) : P(cible) 0.4 % x 31.69 % + P(rien) 70.5 % x 3.57 % ne couvrent pas P(stop) 29.1 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 13.877 %) — p(stop avant cible) 0.0797 [0.05 ; 0.11], R/R 1.221, perte reelle 25.963 % (gap inclus), EV -0.2515 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.90 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.25 %) : P(cible) 0.4 % x 31.69 % + P(rien) 91.7 % x 1.86 % ne couvrent pas P(stop) 8.0 % x 25.96 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 15.612 %) — p(stop avant cible) 0.0496 [0.03 ; 0.08], R/R 1.221, perte reelle 25.963 % (gap inclus), EV 0.3596 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.63 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 17.346 %) — p(stop avant cible) 0.0303 [0.02 ; 0.05], R/R 0.886, perte reelle 35.757 % (gap inclus), EV 0.403 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.36 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 19.081 %) — p(stop avant cible) 0.0231 [0.01 ; 0.04], R/R 0.886, perte reelle 35.757 % (gap inclus), EV 0.5914 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.09 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 20.815 %) — p(stop avant cible) 0.0081 [0.00 ; 0.02], R/R 0.886, perte reelle 35.757 % (gap inclus), EV 0.9349 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.83 % > budget 12.00 %
   - 🟢 grid_snapped a 6.57 ATR (stop 23.845 %) — p(stop avant cible) 0.0054 [0.00 ; 0.02], R/R 0.886, perte reelle 35.757 % (gap inclus), EV 1.014 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.85 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 24.285 %) — p(stop avant cible) 0.0047 [0.00 ; 0.02], R/R 0.886, perte reelle 35.757 % (gap inclus), EV 1.0414 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.29 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 26.019 %) — p(stop avant cible) 0.004 [0.00 ; 0.02], R/R 0.886, perte reelle 35.757 % (gap inclus), EV 1.0697 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.03 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 27.754 %) — p(stop avant cible) 0.0033 [0.00 ; 0.01], R/R 0.886, perte reelle 35.757 % (gap inclus), EV 1.0899 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.76 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 142.6, ATR14 4.9471 (3.469 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.367 ATR = 1.273 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.173 % | 142.3526 | 91.52 % | 94.08 % | 95.55 % | 96.14 % | 97.21 % | 97.89 % |
| 0.1 ATR | 0.347 % | 142.1053 | 83.83 % | 88.15 % | 90.61 % | 92.67 % | 94.63 % | 95.68 % |
| 0.15 ATR | 0.52 % | 141.8579 | 76.33 % | 82.33 % | 85.87 % | 88.51 % | 91.24 % | 93.27 % |
| 0.2 ATR | 0.694 % | 141.6106 | 70.41 % | 79.07 % | 83.0 % | 86.34 % | 89.45 % | 91.86 % |
| 0.25 ATR | 0.867 % | 141.3632 | 63.91 % | 74.73 % | 79.35 % | 83.27 % | 87.36 % | 90.45 % |
| 0.35 ATR | 1.214 % | 140.8685 | 51.78 % | 64.86 % | 70.36 % | 75.84 % | 81.99 % | 86.33 % |
| 0.5 ATR | 1.735 % | 140.1264 | 36.29 % | 51.63 % | 59.39 % | 66.34 % | 74.43 % | 80.2 % |
| 0.75 ATR | 2.602 % | 138.8897 | 19.63 % | 35.74 % | 44.96 % | 54.26 % | 65.37 % | 73.27 % |
| 1.0 ATR | 3.469 % | 137.6529 | 11.05 % | 25.37 % | 34.09 % | 43.76 % | 56.72 % | 64.92 % |
| 1.25 ATR | 4.337 % | 136.4161 | 6.11 % | 17.28 % | 24.9 % | 35.54 % | 48.26 % | 57.29 % |
| 1.5 ATR | 5.204 % | 135.1793 | 2.76 % | 11.06 % | 17.79 % | 27.72 % | 41.09 % | 50.95 % |
| 2.0 ATR | 6.938 % | 132.7057 | 0.79 % | 3.95 % | 8.6 % | 16.24 % | 28.16 % | 39.8 % |
| 2.5 ATR | 8.673 % | 130.2322 | 0.3 % | 1.97 % | 3.95 % | 9.41 % | 19.4 % | 30.05 % |
| 3.0 ATR | 10.408 % | 127.7586 | 0.1 % | 0.79 % | 1.88 % | 4.85 % | 12.34 % | 22.41 % |
| 4.0 ATR | 13.877 % | 122.8114 | 0.1 % | 0.39 % | 1.09 % | 2.28 % | 6.27 % | 12.46 % |
| 6.0 ATR | 20.815 % | 112.9172 | 0.0 % | 0.2 % | 0.4 % | 0.89 % | 2.19 % | 5.33 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.37 ATR | 0.42 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 1.05 ATR | 1.33 ATR |
| **2 s.** | 0.25 ATR | 0.53 ATR | 0.60 ATR | 0.82 ATR | 1.01 ATR | 1.17 ATR | 1.57 ATR | 1.93 ATR |
| **3 s.** | 0.30 ATR | 0.66 ATR | 0.75 ATR | 1.03 ATR | 1.25 ATR | 1.42 ATR | 1.92 ATR | 2.39 ATR |
| **5 s.** | 0.36 ATR | 0.85 ATR | 0.97 ATR | 1.33 ATR | 1.62 ATR | 1.84 ATR | 2.46 ATR | 2.98 ATR |
| **10 s.** | 0.49 ATR | 1.20 ATR | 1.36 ATR | 1.81 ATR | 2.18 ATR | 2.47 ATR | 3.39 ATR | 4.62 ATR |
| **20 s.** | 0.69 ATR | 1.54 ATR | 1.77 ATR | 2.35 ATR | 2.83 ATR | 3.24 ATR | 4.69 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.416–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.604–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.602 %, prix 138.8896), p(touche) 35.74 % (en stress 91.18 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.749–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.602 %, prix 138.8896), p(touche) 44.96 % (en stress 96.08 %)  ✅ optimum identifie (85.4 % des re-echantillons)
- **5 seance(s)** : plage utile 0.97–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.469 %, prix 137.6532), p(touche) 43.76 % (en stress 99.01 %)  ✅ optimum identifie (90.8 % des re-echantillons)
- **10 seance(s)** : plage utile 1.364–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.204 %, prix 135.1791), p(touche) 41.09 % (en stress 100.0 %)  ✅ optimum identifie (92.8 % des re-echantillons)
- **20 seance(s)** : plage utile 1.767–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.938 %, prix 132.7064), p(touche) 39.8 % (en stress 99.0 %)  ✅ optimum identifie (89.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.054 | EV/share : €0.269 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 29 % | T3 9 %
- Kelly (position) : f* 0.03 | ¼-Kelly 0.007 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 20.6 | side 74.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 143.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.435% → cible +1.587% / stop −8.0%, p_fill 36%, n_eff≈18.1) : P(cible|rempli) **34%** · **EV/risk +0.000** (×p_fill ; si rempli +0.00% du capital)
  - **swing** (entrée dip −5.361% → cible +3.549% / stop −3.666%, p_fill 25%, n_eff≈11.4) : P(cible|rempli) **36%** · **EV/risk +0.009** (×p_fill ; si rempli +0.13% du capital)
  - **deep** (entrée dip −8.296% → cible +5.019% / stop −5.674%, p_fill 14%, n_eff≈8.9) : P(cible|rempli) **82%** · **EV/risk +0.073** (×p_fill ; si rempli +2.95% du capital)
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

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 43.3  _(momentum baissier)_
- **ADX** : 11.0  _(pas de tendance nette)_
- **MACD** : hist 0.643  _(pas de croisement recent)_
- **BB** : %B 0.51 · largeur 12.1%
- **ATR** : 4.95 (27.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.208  _(distribution)_
- **Vol ratio** : 0.94  _(volume normal)_
- **Choppiness** : 49.6  _(transition)_
- **MA** : MA20 142.4 · MA50 148.21 · MA200 152.69  _(prix > MA20)_
- **Dist MA** : MA20 +0.1% · MA50 -3.8% · MA200 -6.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (928881 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
