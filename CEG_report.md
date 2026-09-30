# CEG

**Generated** : 2026-09-30T00:31:43.013966+00:00  
**Santé technique** : 7/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $264.64  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $264.64 (+3.5% vs entrée) · entrée $255.65 · stop $251.82 · T1 $259.37 · R/R 0.97  
> ↳ _probas brutes, non calibrées · n=0_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +1.8 % ≠ (strike 265.0 − spot 264.64)/spot = +0.1 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.190 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $254.91–$256.40 (mid $255.65)
- Spot actuel : $264.64 (+3.5% au-dessus de la zone — repli à attendre)
- Stop : $251.82 (plancher anti-bruit 5 s — stop EV-optimal −1.5% (first-passage 5 s réel) ; -1.50 % depuis l'entree)
- Targets : T1 $259.37 · R/R 0.97 | T2 $263.08 · R/R 1.94 | T3 $266.79 · R/R 2.91
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $251.82


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.95 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (10.19 %)** : le gap seul le franchit 0.085 % des séances (1 fois sur 1177).
   - exécution **5.634 pt plus bas** dans le cas TYPIQUE (médiane), 5.634 au p90, **5.634 au pire**
   - perte réelle **15.824 %** en moyenne _(tirée par la queue)_, jusqu'à **15.824 %** — au lieu des 10.19 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0048 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.83 % | p01 -4.434 % | pire -15.824 % _(sur 1177 séances)_
- **P(stop avant cible)** _(source : daily, 1178 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4549** [0.382 ; 0.5293] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4665** [0.4144 ; 0.5192] _(largeur 10.5 pt, n_eff 345.5)_
   - deep : **0.4223** [0.371 ; 0.4749] _(largeur 10.4 pt, n_eff 345.4)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (42.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-4.27 %** | CVaR **-6.17 %** | vol 2.83 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 4.59 % contre 2.66 % aujourd'hui, rapport 1.72)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.02 % vs -9.57 % si l'on extrapolait par √5 _(rapport 1.046 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1832** (β de hausse 1.1944, asymétrie 0.9906) vs SPY — 544 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 243.5232 sur swing_based (1.77 ATR, 7.979 %) — p(stop avant cible) 0.3714 [0.32 ; 0.42], R/R 5.133, perte reelle 8.134 % (gap inclus), CVaR 9.128 %, EV -0.3484 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.9893 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 5.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 17 des 19 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 41.9 % de la queue et il ne reste que 294.13 EUR a partager. Prix du risque 0.099 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.093 %) — p(stop avant cible) 0.5722 [0.52 ; 0.62], R/R 7.935, perte reelle 5.261 % (gap inclus), EV -0.2608 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 7.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.572, borne haute 0.624 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.26 %) : P(cible) 0.2 % x 41.75 % + P(rien) 42.6 % x 6.29 % ne couvrent pas P(stop) 57.2 % x 5.26 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ swing_based a 1.77 ATR (stop 7.979 %) — p(stop avant cible) 0.3714 [0.32 ; 0.42], R/R 5.133, perte reelle 8.134 % (gap inclus), EV -0.3484 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 5.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.35 %) : P(cible) 0.2 % x 41.75 % + P(rien) 62.7 % x 4.16 % ne couvrent pas P(stop) 37.1 % x 8.13 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 0.849 %) — p(stop avant cible) 0.9384 [0.91 ; 0.96], R/R 43.329, perte reelle 0.964 % (gap inclus), EV -0.27 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 43.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.938, borne haute 0.960 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.27 %) : P(cible) 0.0 % x 41.75 % + P(rien) 6.2 % x 10.29 % ne couvrent pas P(stop) 93.8 % x 0.96 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+41.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.5 ATR (stop 1.698 %) — p(stop avant cible) 0.8419 [0.80 ; 0.88], R/R 22.865, perte reelle 1.826 % (gap inclus), EV -0.0376 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 22.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.842, borne haute 0.877 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 0.1 % x 41.75 % + P(rien) 15.7 % x 9.21 % ne couvrent pas P(stop) 84.2 % x 1.83 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 2.547 %) — p(stop avant cible) 0.746 [0.70 ; 0.79], R/R 15.383, perte reelle 2.714 % (gap inclus), EV 0.1537 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 15.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.746, borne haute 0.790 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 3.395 %) — p(stop avant cible) 0.6842 [0.63 ; 0.73], R/R 11.648, perte reelle 3.584 % (gap inclus), EV 0.061 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 11.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.684, borne haute 0.732 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.25 ATR (stop 4.244 %) — p(stop avant cible) 0.6173 [0.57 ; 0.67], R/R 9.459, perte reelle 4.414 % (gap inclus), EV -0.035 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 9.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.617, borne haute 0.667 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 0.2 % x 41.75 % + P(rien) 38.1 % x 6.88 % ne couvrent pas P(stop) 61.7 % x 4.41 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 1.77 ATR (stop 7.022 %) — p(stop avant cible) 0.4402 [0.39 ; 0.49], R/R 5.773, perte reelle 7.232 % (gap inclus), EV -0.3737 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 5.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.37 %) : P(cible) 0.2 % x 41.75 % + P(rien) 55.8 % x 4.91 % ne couvrent pas P(stop) 44.0 % x 7.23 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 8.489 %) — p(stop avant cible) 0.3562 [0.31 ; 0.41], R/R 4.851, perte reelle 8.605 % (gap inclus), EV -0.423 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.42 %) : P(cible) 0.2 % x 41.75 % + P(rien) 64.2 % x 4.01 % ne couvrent pas P(stop) 35.6 % x 8.61 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 9.337 %) — p(stop avant cible) 0.3221 [0.27 ; 0.37], R/R 4.417, perte reelle 9.453 % (gap inclus), EV -0.5095 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.51 %) : P(cible) 0.2 % x 41.75 % + P(rien) 67.6 % x 3.65 % ne couvrent pas P(stop) 32.2 % x 9.45 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 10.186 %) — p(stop avant cible) 0.2823 [0.24 ; 0.33], R/R 4.048, perte reelle 10.312 % (gap inclus), EV -0.4613 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.46 %) : P(cible) 0.2 % x 41.75 % + P(rien) 71.6 % x 3.33 % ne couvrent pas P(stop) 28.2 % x 10.31 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 11.884 %) — p(stop avant cible) 0.2217 [0.18 ; 0.27], R/R 3.484, perte reelle 11.983 % (gap inclus), EV -0.4879 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.32 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.49 %) : P(cible) 0.2 % x 41.75 % + P(rien) 77.7 % x 2.71 % ne couvrent pas P(stop) 22.2 % x 11.98 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 13.582 %) — p(stop avant cible) 0.1785 [0.14 ; 0.22], R/R 3.06, perte reelle 13.645 % (gap inclus), EV -0.5371 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.81 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.54 %) : P(cible) 0.2 % x 41.75 % + P(rien) 82.0 % x 2.23 % ne couvrent pas P(stop) 17.8 % x 13.65 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 15.28 %) — p(stop avant cible) 0.1118 [0.08 ; 0.15], R/R 2.723, perte reelle 15.33 % (gap inclus), EV -0.4146 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.39 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.41 %) : P(cible) 0.2 % x 41.75 % + P(rien) 88.7 % x 1.39 % ne couvrent pas P(stop) 11.2 % x 15.33 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 16.977 %) — p(stop avant cible) 0.0553 [0.03 ; 0.08], R/R 2.445, perte reelle 17.074 % (gap inclus), EV -0.285 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.08 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.29 %) : P(cible) 0.2 % x 41.75 % + P(rien) 94.3 % x 0.63 % ne couvrent pas P(stop) 5.5 % x 17.07 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 18.675 %) — p(stop avant cible) 0.0304 [0.02 ; 0.05], R/R 2.209, perte reelle 18.899 % (gap inclus), EV -0.2388 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.83 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.24 %) : P(cible) 0.2 % x 41.75 % + P(rien) 96.8 % x 0.28 % ne couvrent pas P(stop) 3.0 % x 18.90 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 20.373 %) — p(stop avant cible) 0.0185 [0.01 ; 0.04], R/R 2.041, perte reelle 20.459 % (gap inclus), EV -0.2051 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.08 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.21 %) : P(cible) 0.2 % x 41.75 % + P(rien) 98.0 % x 0.11 % ne couvrent pas P(stop) 1.8 % x 20.46 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 22.07 %) — p(stop avant cible) 0.0106 [0.00 ; 0.03], R/R 1.885, perte reelle 22.151 % (gap inclus), EV -0.1544 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.64 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 0.2 % x 41.75 % + P(rien) 98.8 % x 0.01 % ne couvrent pas P(stop) 1.1 % x 22.15 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 23.768 %) — p(stop avant cible) 0.0081 [0.00 ; 0.02], R/R 1.753, perte reelle 23.813 % (gap inclus), EV -0.1436 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.65 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 0.2 % x 41.75 % + P(rien) 99.0 % x -0.02 % ne couvrent pas P(stop) 0.8 % x 23.81 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 25.466 %) — p(stop avant cible) 0.0074 [0.00 ; 0.02], R/R 1.639, perte reelle 25.466 % (gap inclus), EV -0.1381 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.76 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 0.2 % x 41.75 % + P(rien) 99.1 % x -0.02 % ne couvrent pas P(stop) 0.7 % x 25.47 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 27.164 %) — p(stop avant cible) 0.0062 [0.00 ; 0.02], R/R 1.532, perte reelle 27.243 % (gap inclus), EV -0.1383 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.83 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 0.2 % x 41.75 % + P(rien) 99.2 % x -0.04 % ne couvrent pas P(stop) 0.6 % x 27.24 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 264.64, ATR14 8.9857 (3.395 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.389 ATR = 1.321 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.17 % | 264.1907 | 91.6 % | 94.54 % | 95.52 % | 96.6 % | 97.58 % | 98.0 % |
| 0.1 ATR | 0.34 % | 263.7414 | 85.61 % | 90.39 % | 92.35 % | 93.98 % | 95.59 % | 96.77 % |
| 0.15 ATR | 0.509 % | 263.2922 | 79.17 % | 86.14 % | 88.42 % | 90.47 % | 93.72 % | 95.43 % |
| 0.2 ATR | 0.679 % | 262.8429 | 72.19 % | 80.79 % | 84.04 % | 86.64 % | 91.3 % | 94.1 % |
| 0.25 ATR | 0.849 % | 262.3936 | 65.32 % | 75.22 % | 79.23 % | 82.91 % | 88.55 % | 92.09 % |
| 0.35 ATR | 1.188 % | 261.495 | 53.98 % | 65.72 % | 71.37 % | 76.56 % | 84.03 % | 88.53 % |
| 0.5 ATR | 1.698 % | 260.1472 | 38.71 % | 52.73 % | 59.23 % | 66.05 % | 76.76 % | 82.74 % |
| 0.75 ATR | 2.547 % | 257.9007 | 20.17 % | 36.35 % | 44.81 % | 53.01 % | 66.3 % | 75.72 % |
| 1.0 ATR | 3.395 % | 255.6543 | 11.12 % | 23.8 % | 32.9 % | 43.04 % | 57.27 % | 69.38 % |
| 1.25 ATR | 4.244 % | 253.4079 | 5.67 % | 15.94 % | 24.04 % | 35.27 % | 51.21 % | 63.25 % |
| 1.5 ATR | 5.093 % | 251.1614 | 2.73 % | 10.59 % | 17.27 % | 28.81 % | 44.38 % | 57.35 % |
| 2.0 ATR | 6.791 % | 246.6686 | 0.87 % | 4.37 % | 9.29 % | 17.96 % | 31.61 % | 46.1 % |
| 2.5 ATR | 8.489 % | 242.1757 | 0.44 % | 2.29 % | 4.81 % | 11.06 % | 21.37 % | 36.19 % |
| 3.0 ATR | 10.186 % | 237.6829 | 0.0 % | 1.09 % | 2.84 % | 7.01 % | 15.75 % | 28.29 % |
| 4.0 ATR | 13.582 % | 228.6972 | 0.0 % | 0.22 % | 0.87 % | 2.74 % | 7.16 % | 13.92 % |
| 6.0 ATR | 20.373 % | 210.7257 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.77 % | 2.67 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.39 ATR | 0.44 ATR | 0.58 ATR | 0.69 ATR | 0.76 ATR | 1.05 ATR | 1.31 ATR |
| **2 s.** | 0.25 ATR | 0.54 ATR | 0.62 ATR | 0.82 ATR | 0.98 ATR | 1.12 ATR | 1.55 ATR | 1.95 ATR |
| **3 s.** | 0.30 ATR | 0.66 ATR | 0.75 ATR | 1.00 ATR | 1.22 ATR | 1.40 ATR | 1.96 ATR | 2.48 ATR |
| **5 s.** | 0.37 ATR | 0.82 ATR | 0.95 ATR | 1.34 ATR | 1.68 ATR | 1.91 ATR | 2.63 ATR | 3.47 ATR |
| **10 s.** | 0.54 ATR | 1.29 ATR | 1.48 ATR | 1.95 ATR | 2.32 ATR | 2.62 ATR | 3.67 ATR | 4.68 ATR |
| **20 s.** | 0.78 ATR | 1.83 ATR | 2.06 ATR | 2.70 ATR | 3.23 ATR | 3.58 ATR | 4.70 ATR | 5.59 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.438–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.698 %, prix 260.1464), p(touche) 38.71 % (en stress 81.52 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.618–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.547 %, prix 257.8996), p(touche) 36.35 % (en stress 88.04 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.747–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.547 %, prix 257.8996), p(touche) 44.81 % (en stress 97.83 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.951–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.395 %, prix 255.6555), p(touche) 43.04 % (en stress 96.74 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.477–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.093 %, prix 251.1619), p(touche) 44.38 % (en stress 98.9 %)  ✅ optimum identifie (71.2 % des re-echantillons)
- **20 seance(s)** : plage utile 2.055–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.489 %, prix 242.1747), p(touche) 36.19 % (en stress 95.56 %)  ✅ optimum identifie (87.4 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 68.0 | bear 5.3 | side 26.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈60.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.391% → cible +1.452% / stop −1.5%, p_fill 13%, n_eff≈16.2) : P(cible|rempli) **11%** · **EV/risk -0.021** (×p_fill ; si rempli -0.24% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=10, n_eff=10))
  - **deep** : indisponible (échantillon insuffisant (n=12, n_eff=12))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→62% · +2.0%→33% · +3.0%→17% · +5.0%→4% · +8.0%→0%
- Range intraday médian 3.34% (p90 5.37%) · excursion haute méd. +1.44% / basse méd. −1.5%
- Profil de vol intra : ouverture 2.368% vs midi 0.663% vs clôture 0.755% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑1%/↓0% ; spike-down 48% · recovery-V 16%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; neutre — autocorr 0.001)_ ; drift intra méd. -0.218% ; recovery-V 19%
- **σ réalisé intraday** 2.11% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 68% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 265.3861 (VA 263.4129–265.8246 ; dernier close 264.64)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 35% · rebond 57% · **stop −2.5%** sous le fill (sous le bruit) · cible +1.1% · R/R 0.44 (high win-rate)
- Gaps overnight (n=159) : méd. 0.46% · baisse 38% (gap-down >1% 10% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.59% (p90 −1.42%) · haut méd +0.76% · range méd 1.39%
- Excursion ouverture 15min (n=160) : bas méd −0.67% (p90 −1.91%) · haut méd +0.87% · range méd 1.83%
- Excursion ouverture 30min (n=160) : bas méd −0.89% (p90 −2.32%) · haut méd +1.01% · range méd 2.07%
- Excursion ouverture 60min (n=160) : bas méd −1.14% (p90 −2.56%) · haut méd +1.18% · range méd 2.43%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 264.64 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 50% · séance 66% (104/159) · gap 25% · délai 1.3min · rebond 45% (52/104) (MFE +0.84%)
   - −1.0% : fill 30min 36% · séance 52% (87/159) · gap 10% · délai 2.6min · rebond 43% (41/87) (MFE +0.96%)
   - −1.5% : fill 30min 30% · séance 44% (71/159) · gap 6% · délai 10.5min · rebond 52% (36/71) (MFE +1.02%)
   - −2.0% : fill 30min 22% · séance 35% (57/159) · gap 4% · délai 21.2min · rebond 57% (32/57) (MFE +1.1%)
   - −3.0% : fill 30min 6% · séance 15% (30/159) · gap 2% · délai 46.5min · rebond 44% (13/30) (MFE +0.76%)
   - −4.0% : fill 30min 4% · séance 8% (17/159) · gap 1% · délai 29.6min · rebond 51% (10/17) (MFE +0.98%)
   - −5.0% : fill 30min 3% · séance 4% (10/159) · gap 0% · délai 34.2min · rebond 57% (7/10) (MFE +1.05%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.25% (p90 −1.14%) → stop au-delà de −0.82% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.28% (p90 −1.19%) → stop au-delà de −0.94% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −2.25%) → stop au-delà de −1.16% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=460 jambes) : jambe baissière méd −1.05% (p90 −2.43%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (42 séances) :
      · −1.0% : fill 90% (39/42) · rebond 49% (21/39)
      · −2.0% : fill 79% (32/42) · rebond 62% (18/32)
      · −3.0% : fill 32% (17/42) · rebond 34% (6/17)
      · −4.0% : fill 24% (13/42) · rebond 50% (7/13)
      · −5.0% : fill 15% (9/42) · rebond 55% (6/9)
   - **flat** (28 séances) :
      · −1.0% : fill 47% (19/28) · rebond 12% (5/19)
      · −2.0% : fill 30% (11/28) · rebond 47% (6/11)
      · −3.0% : fill 13% (6/28) · rebond 24% (2/6)
      · −4.0% : fill 5% (3/28) · rebond 43% (2/3)
      · −5.0% : fill 1% (1/28) · rebond 100% (1/1)
   - **gap-up** (89 séances) :
      · −1.0% : fill 33% (29/89) · rebond 48% (15/29)
      · −2.0% : fill 14% (14/89) · rebond 51% (8/14)
      · −3.0% : fill 6% (7/89) · rebond 82% (5/7)
      · −4.0% : fill 1% (1/89) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/89) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 62% si les 15 1res min sont vertes (87 cas) · 32% si rouges (73 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:23** → P(séance verte=clôture>ouverture) 85% si début vert vs 11% si rouge (base 46% · écart 74 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **85%** · continue >prix actuel 47% ; creux résiduel méd -1.05% (q20 -1.79%) → **SL/trailing à −1.79%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.81% / q75 +1.38% → **scale +0.81% / runner +1.38%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **11%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.18%** (au-delà de la MAE q10 -2.18%), cible rebond +0.92% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.98% .. +2.1%] · haut q95 +2.62% · bas q05 -3.22%
   - 60min (n=160) : retour [-3.48% .. +2.56%] · haut q95 +3.28% · bas q05 -4.13%
   - 2h (n=160) : retour [-3.57% .. +2.98%] · haut q95 +3.46% · bas q05 -4.19%
   - 4h (n=160) : retour [-3.0% .. +3.31%] · haut q95 +4.12% · bas q05 -4.33%
   - 6h (n=160) : retour [-3.94% .. +3.53%] · haut q95 +4.52% · bas q05 -4.4%
   - session (n=160) : retour [-3.62% .. +3.57%] · haut q95 +4.64% · bas q05 -4.58%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 4.4% / strong 2.5%) · base = 11 séances trend-up (n_eff 7.7)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **41%**. Lecture précoce 30 min : signature présente → 16% vs absente 4% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.07% (p75 1.89% / p90 2.36%) · ~1.0 replis/séance, durée méd 144.56 min. P(nouveau plus-haut après repli) :
   - −0.5% → **69%** (reprise méd 24.3 min, n=22)
   - −1.0% → **69%** (reprise méd 179.47 min, n=11)
   - −1.5% → **48%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.36%** (p90, défaut prudent ; serré/agressif −1.89%) ; extension open→close méd +3.62% (q75 +4.82% / q95 +6.2%), MFE méd +4.65% / q90 +5.84%
   - Échelle scale-out : +4.65% (33%) / +5.3% (33%) / +5.84% (34%)
- **DÉSARMER** : repli > **−2.36%** depuis le plus-haut = décay → P(retournement) **100%** (préavis méd 280.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.84% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 96% du temps (retour médian dernière heure +0.48%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.43 · part idiosyncratique 0.57
**Short/Insider** : SI —% | insider — | verdict buy_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 27.8  _(survente)_
- **ADX** : 22.7  _(pas de tendance nette)_
- **MACD** : hist -1.142  _(pas de croisement recent)_
- **BB** : %B 0.36 · largeur 21.8%
- **ATR** : 8.99 (7.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.185  _(distribution)_
- **Vol ratio** : 0.51  _(volume atone)_
- **Choppiness** : 39.6  _(transition)_
- **MA** : MA20 272.95 · MA50 272.16 · MA200 288.62  _(prix < MA20)_
- **Dist MA** : MA20 -3.0% · MA50 -2.8% · MA200 -8.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (850976 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
