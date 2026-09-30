# RHM

**Generated** : 2026-09-30T00:02:46.642105+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €963.40  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot €963.40 (+0.4% vs entrée) · entrée €959.30 · stop €882.56 · T1 €970.42 · R/R 0.14  
> ↳ P(T1 av. stop) 53 % _(réel 5 s)_ · EV/risk -0.054 _(réel 5 s)_ (GBM -0.055) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -22 % hors [0,100] (R² max 0.16). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €957.08–€961.52 (mid €959.30)
- Spot actuel : €963.40 (+0.4% au-dessus de la zone — repli à attendre)
- Stop : €882.56 (plancher anti-bruit 5 s — stop EV-optimal −8% (first-passage 5 s réel) ; -8.00 % depuis l'entree)
- Targets : T1 €970.42 · R/R 0.14 | T2 €981.54 · R/R 0.29 | T3 €992.67 · R/R 0.43
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €882.56


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.73 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (4.17 %)** : le gap seul le franchit 0.785 % des séances (10 fois sur 1274).
   - exécution **0.374 pt plus bas** dans le cas TYPIQUE (médiane), 5.14 au p90, **18.259 au pire**
   - perte réelle **6.788 %** en moyenne _(tirée par la queue)_, jusqu'à **22.429 %** — au lieu des 4.17 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0205 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 10 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.574 % | p01 -3.746 % | pire -22.429 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0102** [0.0019 ; 0.0343] _(largeur 3.2 pt, n_eff 173.1)_
   - swing : **0.4501** [0.3983 ; 0.5028] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4483** [0.3965 ; 0.501] _(largeur 10.4 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 480 séances)** : VaR **-4.86 %** | CVaR **-6.85 %** | vol 3.07 %/j
   - _fenêtre arrêtée : rupture de regime a 540 seances en arriere (volatilite 1.80 % contre 3.09 % aujourd'hui, rapport 0.58)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.83 % vs -8.98 % si l'on extrapolait par √5 _(rapport 0.871 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5284** (β de hausse 0.5878, asymétrie 0.8989) vs GDAXI — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.114× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 901.0857 sur atr_grid (2.0 ATR, 6.468 %) — p(stop avant cible) 0.4912 [0.44 ; 0.54], R/R 3.973, perte reelle 6.899 % (gap inclus), CVaR 10.464 %, EV -0.7978 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.94 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 3.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 17 des 19 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 41.9 % de la queue et il ne reste que 294.13 EUR a partager. Prix du risque 0.099 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.63 ATR (stop 3.908 %) — p(stop avant cible) 0.6725 [0.62 ; 0.72], R/R 6.589, perte reelle 4.159 % (gap inclus), EV -0.3578 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 6.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.672, borne haute 0.720 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 0.5 % x 27.41 % + P(rien) 32.3 % x 7.16 % ne couvrent pas P(stop) 67.2 % x 4.16 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 support a 1.11 ATR (stop 5.474 %) — p(stop avant cible) 0.5809 [0.53 ; 0.63], R/R 4.661, perte reelle 5.88 % (gap inclus), EV -0.8034 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 4.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.581, borne haute 0.632 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.53 ATR du spot — compartiment <1, mesure a 49.1 % de casse (IC clusterise [0.457 ; 0.522] sur 1123 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.80 %) : P(cible) 0.6 % x 27.41 % + P(rien) 41.3 % x 5.91 % ne couvrent pas P(stop) 58.1 % x 5.88 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 0.809 %) — p(stop avant cible) 0.938 [0.91 ; 0.96], R/R 31.776, perte reelle 0.863 % (gap inclus), EV -0.1056 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 31.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.938, borne haute 0.960 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.11 %) : P(cible) 0.2 % x 27.41 % + P(rien) 6.0 % x 10.75 % ne couvrent pas P(stop) 93.8 % x 0.86 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 0.63 ATR (stop 2.996 %) — p(stop avant cible) 0.7556 [0.71 ; 0.80], R/R 8.467, perte reelle 3.237 % (gap inclus), EV -0.4212 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 8.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.756, borne haute 0.799 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.42 %) : P(cible) 0.5 % x 27.41 % + P(rien) 24.0 % x 7.92 % ne couvrent pas P(stop) 75.6 % x 3.24 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 grid_snapped a 1.11 ATR (stop 4.562 %) — p(stop avant cible) 0.6334 [0.58 ; 0.68], R/R 5.639, perte reelle 4.86 % (gap inclus), EV -0.5189 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 5.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.633, borne haute 0.683 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.52 %) : P(cible) 0.5 % x 27.41 % + P(rien) 36.1 % x 6.69 % ne couvrent pas P(stop) 63.3 % x 4.86 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 6.468 %) — p(stop avant cible) 0.4912 [0.44 ; 0.54], R/R 3.973, perte reelle 6.899 % (gap inclus), EV -0.7978 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 3.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.80 %) : P(cible) 0.9 % x 27.41 % + P(rien) 50.0 % x 4.69 % ne couvrent pas P(stop) 49.1 % x 6.90 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 7.277 %) — p(stop avant cible) 0.4353 [0.38 ; 0.49], R/R 3.531, perte reelle 7.762 % (gap inclus), EV -0.8331 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 3.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.83 %) : P(cible) 0.9 % x 27.41 % + P(rien) 55.6 % x 4.14 % ne couvrent pas P(stop) 43.5 % x 7.76 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 8.085 %) — p(stop avant cible) 0.4163 [0.37 ; 0.47], R/R 3.199, perte reelle 8.568 % (gap inclus), EV -1.0378 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 3.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.04 %) : P(cible) 0.9 % x 27.41 % + P(rien) 57.5 % x 3.97 % ne couvrent pas P(stop) 41.6 % x 8.57 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 8.894 %) — p(stop avant cible) 0.3681 [0.32 ; 0.42], R/R 2.922, perte reelle 9.381 % (gap inclus), EV -1.0517 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.31 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.05 %) : P(cible) 0.9 % x 27.41 % + P(rien) 62.2 % x 3.44 % ne couvrent pas P(stop) 36.8 % x 9.38 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 9.702 %) — p(stop avant cible) 0.3091 [0.26 ; 0.36], R/R 2.695, perte reelle 10.169 % (gap inclus), EV -1.0293 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.56 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.03 %) : P(cible) 1.0 % x 27.41 % + P(rien) 68.1 % x 2.70 % ne couvrent pas P(stop) 30.9 % x 10.17 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 11.319 %) — p(stop avant cible) 0.2464 [0.20 ; 0.29], R/R 2.33, perte reelle 11.763 % (gap inclus), EV -1.1044 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.51 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.10 %) : P(cible) 1.0 % x 27.41 % + P(rien) 74.4 % x 2.04 % ne couvrent pas P(stop) 24.6 % x 11.76 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 12.936 %) — p(stop avant cible) 0.1732 [0.14 ; 0.22], R/R 2.023, perte reelle 13.548 % (gap inclus), EV -1.144 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.05 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.14 %) : P(cible) 1.0 % x 27.41 % + P(rien) 81.7 % x 1.13 % ne couvrent pas P(stop) 17.3 % x 13.55 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 14.553 %) — p(stop avant cible) 0.1339 [0.10 ; 0.17], R/R 1.809, perte reelle 15.15 % (gap inclus), EV -1.1165 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.15 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.12 %) : P(cible) 1.0 % x 27.41 % + P(rien) 85.6 % x 0.74 % ne couvrent pas P(stop) 13.4 % x 15.15 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 16.17 %) — p(stop avant cible) 0.0999 [0.07 ; 0.13], R/R 1.631, perte reelle 16.807 % (gap inclus), EV -1.1421 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.44 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.14 %) : P(cible) 1.0 % x 27.41 % + P(rien) 89.0 % x 0.29 % ne couvrent pas P(stop) 10.0 % x 16.81 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 17.787 %) — p(stop avant cible) 0.0755 [0.05 ; 0.11], R/R 1.49, perte reelle 18.397 % (gap inclus), EV -1.1541 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.71 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.15 %) : P(cible) 1.0 % x 27.41 % + P(rien) 91.4 % x -0.05 % ne couvrent pas P(stop) 7.5 % x 18.40 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 19.404 %) — p(stop avant cible) 0.0531 [0.03 ; 0.08], R/R 1.366, perte reelle 20.065 % (gap inclus), EV -1.137 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.11 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.14 %) : P(cible) 1.0 % x 27.41 % + P(rien) 93.7 % x -0.37 % ne couvrent pas P(stop) 5.3 % x 20.06 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 21.022 %) — p(stop avant cible) 0.0407 [0.02 ; 0.07], R/R 1.267, perte reelle 21.639 % (gap inclus), EV -1.1599 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.94 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.16 %) : P(cible) 1.0 % x 27.41 % + P(rien) 94.9 % x -0.59 % ne couvrent pas P(stop) 4.1 % x 21.64 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 22.639 %) — p(stop avant cible) 0.0173 [0.01 ; 0.04], R/R 1.164, perte reelle 23.554 % (gap inclus), EV -0.9309 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.93 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.93 %) : P(cible) 1.0 % x 27.41 % + P(rien) 97.3 % x -0.82 % ne couvrent pas P(stop) 1.7 % x 23.55 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 24.256 %) — p(stop avant cible) 0.01 [0.00 ; 0.03], R/R 1.093, perte reelle 25.065 % (gap inclus), EV -0.9098 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.54 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.91 %) : P(cible) 1.0 % x 27.41 % + P(rien) 98.0 % x -0.96 % ne couvrent pas P(stop) 1.0 % x 25.07 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 25.873 %) — p(stop avant cible) 0.0061 [0.00 ; 0.02], R/R 1.048, perte reelle 26.149 % (gap inclus), EV -0.9101 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.53 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.91 %) : P(cible) 1.0 % x 27.41 % + P(rien) 98.4 % x -1.04 % ne couvrent pas P(stop) 0.6 % x 26.15 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 963.4, ATR14 31.1571 (3.234 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.394 ATR = 1.274 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.162 % | 961.8422 | 89.45 % | 92.2 % | 93.38 % | 94.55 % | 97.01 % | 97.69 % |
| 0.1 ATR | 0.323 % | 960.2843 | 83.43 % | 87.96 % | 89.82 % | 91.39 % | 95.22 % | 96.28 % |
| 0.15 ATR | 0.485 % | 958.7265 | 76.53 % | 83.22 % | 85.87 % | 88.32 % | 92.94 % | 94.77 % |
| 0.2 ATR | 0.647 % | 957.1686 | 70.02 % | 78.78 % | 81.82 % | 85.25 % | 90.95 % | 93.17 % |
| 0.25 ATR | 0.809 % | 955.6107 | 62.52 % | 73.05 % | 76.88 % | 81.19 % | 88.46 % | 91.36 % |
| 0.35 ATR | 1.132 % | 952.495 | 53.94 % | 66.04 % | 71.44 % | 76.73 % | 85.87 % | 89.25 % |
| 0.5 ATR | 1.617 % | 947.8215 | 40.63 % | 54.99 % | 61.86 % | 69.21 % | 80.3 % | 83.82 % |
| 0.75 ATR | 2.426 % | 940.0322 | 23.57 % | 38.99 % | 47.33 % | 57.62 % | 70.35 % | 77.09 % |
| 1.0 ATR | 3.234 % | 932.2429 | 13.02 % | 26.55 % | 36.26 % | 48.51 % | 62.29 % | 70.55 % |
| 1.25 ATR | 4.043 % | 924.4536 | 7.4 % | 17.97 % | 26.28 % | 39.11 % | 54.13 % | 64.22 % |
| 1.5 ATR | 4.851 % | 916.6643 | 3.94 % | 13.13 % | 20.55 % | 31.78 % | 45.87 % | 57.09 % |
| 2.0 ATR | 6.468 % | 901.0857 | 1.78 % | 7.01 % | 12.15 % | 20.99 % | 34.23 % | 47.34 % |
| 2.5 ATR | 8.085 % | 885.5072 | 0.49 % | 3.36 % | 6.32 % | 12.48 % | 24.98 % | 38.09 % |
| 3.0 ATR | 9.702 % | 869.9286 | 0.1 % | 1.38 % | 3.85 % | 7.72 % | 17.41 % | 32.26 % |
| 4.0 ATR | 12.936 % | 838.7715 | 0.0 % | 0.3 % | 1.28 % | 3.27 % | 8.66 % | 20.5 % |
| 6.0 ATR | 19.404 % | 776.4572 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 0.8 % | 3.52 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.39 ATR | 0.45 ATR | 0.61 ATR | 0.73 ATR | 0.83 ATR | 1.13 ATR | 1.42 ATR |
| **2 s.** | 0.23 ATR | 0.58 ATR | 0.66 ATR | 0.87 ATR | 1.04 ATR | 1.19 ATR | 1.76 ATR | 2.27 ATR |
| **3 s.** | 0.28 ATR | 0.70 ATR | 0.80 ATR | 1.08 ATR | 1.31 ATR | 1.53 ATR | 2.18 ATR | 2.77 ATR |
| **5 s.** | 0.39 ATR | 0.96 ATR | 1.09 ATR | 1.46 ATR | 1.81 ATR | 2.06 ATR | 2.76 ATR | 3.61 ATR |
| **10 s.** | 0.63 ATR | 1.38 ATR | 1.54 ATR | 2.07 ATR | 2.50 ATR | 2.83 ATR | 3.85 ATR | 4.93 ATR |
| **20 s.** | 0.83 ATR | 1.86 ATR | 2.13 ATR | 2.94 ATR | 3.62 ATR | 4.06 ATR | 5.24 ATR | 5.83 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.451–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.656–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.426 %, prix 940.0279), p(touche) 38.99 % (en stress 91.18 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.803–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.234 %, prix 932.2437), p(touche) 36.26 % (en stress 95.1 %)  ✅ optimum identifie (60.0 % des re-echantillons)
- **5 seance(s)** : plage utile 1.093–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.043 %, prix 924.4498), p(touche) 39.11 % (en stress 98.02 %)  ✅ optimum identifie (86.6 % des re-echantillons)
- **10 seance(s)** : plage utile 1.537–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.468 %, prix 901.0873), p(touche) 34.23 % (en stress 96.04 %)  ✅ optimum identifie (98.4 % des re-echantillons)
- **20 seance(s)** : plage utile 2.126–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.085 %, prix 885.5091), p(touche) 38.09 % (en stress 98.0 %)  ✅ optimum identifie (99.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.055 | EV/share : €-4.209 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 56 % | T2 36 % | T3 19 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.0 | bear 5.0 | side 10.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.424% → cible +1.159% / stop −8.0%, p_fill 89%, n_eff≈94.7) : P(cible|rempli) **53%** · **EV/risk -0.054** (×p_fill ; si rempli -0.48% du capital)
  - **swing** (entrée dip −0.936% → cible +2.592% / stop −3.265%, p_fill 85%, n_eff≈97.9) : P(cible|rempli) **50%** · **EV/risk -0.115** (×p_fill ; si rempli -0.45% du capital)
  - **deep** (entrée dip −1.449% → cible +3.666% / stop −4.922%, p_fill 76%, n_eff≈85.7) : P(cible|rempli) **47%** · **EV/risk -0.158** (×p_fill ; si rempli -1.02% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→72% · +1.0%→60% · +2.0%→41% · +3.0%→25% · +5.0%→3% · +8.0%→1%
- Range intraday médian 3.82% (p90 6.51%) · excursion haute méd. +1.43% / basse méd. −1.76%
- Profil de vol intra : ouverture 2.333% vs midi 0.891% vs clôture 1.028% _(ouverture ~2.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 92% · range 8% · trend ↑0%/↓0% ; spike-down 58% · recovery-V 23%)_
- **Régime intraday** : **chop** _(efficiency 0.116 ; neutre — autocorr -0.029)_ ; drift intra méd. -0.64% ; recovery-V 11%
- **σ réalisé intraday** 2.281% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 73% / whipsaw 26%
- POC intraday (dernière séance, temps-au-prix) : 954.9975 (VA 949.0275–966.9375 ; dernier close 963.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 26% · rebond 48% · **stop −2.11%** sous le fill (sous le bruit) · cible +0.99% · R/R 0.47 (high win-rate)
- Gaps overnight (n=159) : méd. 0.42% · baisse 27% (gap-down >1% 7% · >2% 2%)
- Excursion ouverture 5min (n=160) : bas méd −0.7% (p90 −1.75%) · haut méd +0.43% · range méd 1.28%
- Excursion ouverture 15min (n=160) : bas méd −0.88% (p90 −2.03%) · haut méd +0.57% · range méd 1.69%
- Excursion ouverture 30min (n=160) : bas méd −0.93% (p90 −2.15%) · haut méd +0.67% · range méd 1.89%
- Excursion ouverture 60min (n=160) : bas méd −0.94% (p90 −2.42%) · haut méd +0.74% · range méd 2.03%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 963.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 53% · séance 74% (108/159) · gap 16% · délai 1.5min · rebond 48% (55/108) (MFE +0.96%)
   - −1.0% : fill 30min 38% · séance 65% (96/159) · gap 7% · délai 8.5min · rebond 58% (56/96) (MFE +1.2%)
   - −1.5% : fill 30min 23% · séance 53% (78/159) · gap 5% · délai 52.8min · rebond 52% (44/78) (MFE +1.02%)
   - −2.0% : fill 30min 15% · séance 43% (66/159) · gap 2% · délai 93.4min · rebond 54% (39/66) (MFE +1.2%)
   - −3.0% : fill 30min 6% · séance 26% (37/159) · gap 2% · délai 141.3min · rebond 48% (19/37) (MFE +0.99%)
   - −4.0% : fill 30min 2% · séance 12% (21/159) · gap 2% · délai 149.9min · rebond 65% (12/21) (MFE +1.74%)
   - −5.0% : fill 30min 1% · séance 5% (11/159) · gap 1% · délai 307.4min · rebond 92% (10/11) (MFE +2.43%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.61% (p90 −1.35%) → stop au-delà de −1.14% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.47% (p90 −1.63%) → stop au-delà de −1.28% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.31% (p90 −1.68%) → stop au-delà de −1.07% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=550 jambes) : jambe baissière méd −1.03% (p90 −2.42%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (30 séances) :
      · −1.0% : fill 97% (29/30) · rebond 62% (19/29)
      · −2.0% : fill 77% (25/30) · rebond 46% (15/25)
      · −3.0% : fill 53% (14/30) · rebond 33% (7/14)
      · −4.0% : fill 41% (11/30) · rebond 65% (7/11)
      · −5.0% : fill 17% (6/30) · rebond 100% (6/6)
   - **flat** (26 séances) :
      · −1.0% : fill 85% (20/26) · rebond 63% (14/20)
      · −2.0% : fill 48% (11/26) · rebond 71% (8/11)
      · −3.0% : fill 29% (6/26) · rebond 67% (3/6)
      · −4.0% : fill 4% (2/26) · rebond 62% (1/2)
      · −5.0% : fill 4% (2/26) · rebond 62% (1/2)
   - **gap-up** (103 séances) :
      · −1.0% : fill 46% (47/103) · rebond 50% (23/47)
      · −2.0% : fill 29% (30/103) · rebond 49% (16/30)
      · −3.0% : fill 15% (17/103) · rebond 50% (9/17)
      · −4.0% : fill 5% (8/103) · rebond 66% (4/8)
      · −5.0% : fill 1% (3/103) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 38% en base · 51% si les 15 1res min sont vertes (71 cas) · 28% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 64% si début vert vs 20% si rouge (base 38% · écart 44 pts) ; prédictivité sature ensuite (plafond brut 300min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=67) : tient le vert **64%** · continue >prix actuel 45% ; creux résiduel méd -1.2% (q20 -2.69%) → **SL/trailing à −2.69%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.33% / q75 +1.88% → **scale +1.33% / runner +1.88%**, sortie à la clôture
  - **si ROUGE au coude** (n=93) : edge inversé — récupère vert seulement **20%** (continue à baisser 60%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.43%** (au-delà de la MAE q10 -3.43%), cible rebond +1.02% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.6% .. +2.77%] · haut q95 +3.17% · bas q05 -2.98%
   - 60min (n=160) : retour [-2.48% .. +3.04%] · haut q95 +3.93% · bas q05 -3.38%
   - 2h (n=160) : retour [-3.2% .. +2.7%] · haut q95 +4.09% · bas q05 -3.83%
   - 4h (n=160) : retour [-3.21% .. +2.69%] · haut q95 +4.49% · bas q05 -4.14%
   - 6h (n=160) : retour [-3.59% .. +3.05%] · haut q95 +4.53% · bas q05 -4.32%
   - session (n=160) : retour [-4.07% .. +3.3%] · haut q95 +4.73% · bas q05 -4.89%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.32%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.27 · part idiosyncratique 0.73
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 38.1  _(momentum baissier)_
- **ADX** : 27.5  _(tendance etablie)_
- **MACD** : hist -2.311  _(pas de croisement recent)_
- **BB** : %B 0.1 · largeur 12.5%
- **ATR** : 31.16 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.227  _(distribution)_
- **Vol ratio** : 0.75  _(volume normal)_
- **Choppiness** : 56.0  _(transition)_
- **MA** : MA20 1014.1 · MA50 1088.81 · MA200 1343.45  _(prix < MA20)_
- **Dist MA** : MA20 -5.0% · MA50 -11.5% · MA200 -28.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (850319 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
