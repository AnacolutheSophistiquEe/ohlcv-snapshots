# RGTI

**Generated** : 2026-10-02T00:27:42.317204+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $15.61  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)  
> ↳ spot $15.61 (+4.3% vs entrée) · entrée $14.96 · stop $14.66 · T1 $15.42 · R/R 1.53  
> ↳ ¼-Kelly 0.01 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +1.6 % ≠ (strike 16.0 − spot 15.61)/spot = +2.5 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $14.91–$15.01 (mid $14.96)
- Spot actuel : $15.61 (+4.3% au-dessus de la zone — repli à attendre)
- Stop : $14.66 (plancher anti-bruit 5 s — stop EV-optimal −2% (first-passage 5 s réel) ; -2.01 % depuis l'entree)
- Targets : T1 $15.42 · R/R 1.53 | T2 $15.88 · R/R 3.07 | T3 $16.34 · R/R 4.6
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $14.66


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.46 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (15.0 %)** : le gap seul le franchit 0.16 % des séances (2 fois sur 1253).
   - exécution **9.565 pt plus bas** dans le cas TYPIQUE (médiane), 14.883 au p90, **16.213 au pire**
   - perte réelle **24.565 %** en moyenne _(tirée par la queue)_, jusqu'à **31.213 %** — au lieu des 15.0 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0153 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 2 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.113 % | p01 -8.973 % | pire -31.213 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5038** [0.4298 ; 0.5777] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.5477** [0.495 ; 0.5996] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.5314** [0.4787 ; 0.5836] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (29.7 pt), swing (40.5 pt), deep (42.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.95 %** | CVaR **-11.33 %** | vol 6.83 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 19.50 % contre 6.39 % aujourd'hui, rapport 3.05)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -21.76 % vs -22.11 % si l'on extrapolait par √5 _(rapport 0.984 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8458** (β de hausse 1.9945, asymétrie 0.9255) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.502× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 15.1407 sur grid_snapped (0.21 ATR, 3.006 %) — p(stop avant cible) 0.8386 [0.80 ; 0.87], R/R 6.524, perte reelle 3.073 % (gap inclus), CVaR 4.127 %, EV 0.1592 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.8307 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 12.7 % du temps (< 15 %) meme a 10 seances : le R/R de 6.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.839, borne haute 0.875 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 4.13 % > budget 3.80 %
- Budget de queue : **3.8 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.206 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 43.2 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.21 ATR (stop 4.007 %) — p(stop avant cible) 0.7977 [0.75 ; 0.84], R/R 4.899, perte reelle 4.092 % (gap inclus), EV 0.0751 % — **REFUSE**
      - refuse : p_stop_first 0.798, borne haute 0.838 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 5.32 % > budget 3.80 %
   - ⚪ atr_based a 1.5 ATR (stop 8.828 %) — p(stop avant cible) 0.6232 [0.57 ; 0.67], R/R 2.226, perte reelle 9.005 % (gap inclus), EV -0.4915 % — **REFUSE**
      - refuse : p_stop_first 0.623, borne haute 0.673 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 11.01 % > budget 3.80 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.49 %) : P(cible) 22.6 % x 20.05 % + P(rien) 15.1 % x 3.95 % ne couvrent pas P(stop) 62.3 % x 9.00 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ sr_based a 2.92 ATR (stop 19.926 %) — p(stop avant cible) 0.2038 [0.16 ; 0.25], R/R 0.993, perte reelle 20.188 % (gap inclus), EV 0.1356 % — **REFUSE**
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.99 % > budget 3.80 %
   - 🟢 support a 3.35 ATR (stop 22.497 %) — p(stop avant cible) 0.1353 [0.10 ; 0.17], R/R 0.88, perte reelle 22.793 % (gap inclus), EV 0.2931 % — **REFUSE**
      - refuse : R/R 0.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.30 % > budget 3.80 %
   - ⚪ grid_snapped a 0.21 ATR (stop 3.006 %) — p(stop avant cible) 0.8386 [0.80 ; 0.87], R/R 6.524, perte reelle 3.073 % (gap inclus), EV 0.1592 % — **REFUSE**
      - refuse : cible atteinte seulement 12.7 % du temps (< 15 %) meme a 10 seances : le R/R de 6.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.839, borne haute 0.875 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 4.13 % > budget 3.80 %
   - ⚪ atr_grid a 1.0 ATR (stop 5.885 %) — p(stop avant cible) 0.7207 [0.67 ; 0.77], R/R 3.324, perte reelle 6.031 % (gap inclus), EV -0.1056 % — **REFUSE**
      - refuse : p_stop_first 0.721, borne haute 0.766 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 7.87 % > budget 3.80 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.11 %) : P(cible) 18.9 % x 20.05 % + P(rien) 9.0 % x 4.94 % ne couvrent pas P(stop) 72.1 % x 6.03 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 7.356 %) — p(stop avant cible) 0.6654 [0.61 ; 0.71], R/R 2.684, perte reelle 7.47 % (gap inclus), EV -0.1746 % — **REFUSE**
      - refuse : p_stop_first 0.665, borne haute 0.714 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 8.83 % > budget 3.80 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 21.3 % x 20.05 % + P(rien) 12.2 % x 4.36 % ne couvrent pas P(stop) 66.5 % x 7.47 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 10.299 %) — p(stop avant cible) 0.5956 [0.54 ; 0.65], R/R 1.917, perte reelle 10.456 % (gap inclus), EV -1.0565 % — **REFUSE**
      - refuse : p_stop_first 0.596, borne haute 0.646 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.15 % > budget 3.80 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.06 %) : P(cible) 23.2 % x 20.05 % + P(rien) 17.3 % x 3.06 % ne couvrent pas P(stop) 59.6 % x 10.46 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 11.77 %) — p(stop avant cible) 0.5179 [0.47 ; 0.57], R/R 1.676, perte reelle 11.961 % (gap inclus), EV -0.8348 % — **REFUSE**
      - refuse : p_stop_first 0.518, borne haute 0.570 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.75 % > budget 3.80 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.83 %) : P(cible) 24.3 % x 20.05 % + P(rien) 23.9 % x 2.01 % ne couvrent pas P(stop) 51.8 % x 11.96 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 13.241 %) — p(stop avant cible) 0.4378 [0.39 ; 0.49], R/R 1.494, perte reelle 13.42 % (gap inclus), EV -0.4083 % — **REFUSE**
      - refuse : R/R 1.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.80 % > budget 3.80 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.41 %) : P(cible) 25.4 % x 20.05 % + P(rien) 30.8 % x 1.19 % ne couvrent pas P(stop) 43.8 % x 13.42 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 14.712 %) — p(stop avant cible) 0.3833 [0.33 ; 0.44], R/R 1.339, perte reelle 14.968 % (gap inclus), EV -0.4744 % — **REFUSE**
      - refuse : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.68 % > budget 3.80 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.47 %) : P(cible) 26.2 % x 20.05 % + P(rien) 35.5 % x 0.04 % ne couvrent pas P(stop) 38.3 % x 14.97 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 2.92 ATR (stop 18.925 %) — p(stop avant cible) 0.2387 [0.20 ; 0.29], R/R 1.045, perte reelle 19.18 % (gap inclus), EV -0.0107 % — **REFUSE**
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.14 % > budget 3.80 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.01 %) : P(cible) 27.7 % x 20.05 % + P(rien) 48.4 % x -2.05 % ne couvrent pas P(stop) 23.9 % x 19.18 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 grid_snapped a 3.35 ATR (stop 21.496 %) — p(stop avant cible) 0.1645 [0.13 ; 0.21], R/R 0.92, perte reelle 21.797 % (gap inclus), EV 0.2059 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.48 % > budget 3.80 %
   - ⚪ atr_grid a 4.0 ATR (stop 23.54 %) — p(stop avant cible) 0.1161 [0.09 ; 0.15], R/R 0.841, perte reelle 23.841 % (gap inclus), EV 0.317 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.24 % > budget 3.80 %
   - ⚪ atr_grid a 4.5 ATR (stop 26.482 %) — p(stop avant cible) 0.0775 [0.05 ; 0.11], R/R 0.75, perte reelle 26.738 % (gap inclus), EV 0.4429 % — **REFUSE**
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.88 % > budget 3.80 %
   - ⚪ atr_grid a 5.0 ATR (stop 29.425 %) — p(stop avant cible) 0.0609 [0.04 ; 0.09], R/R 0.676, perte reelle 29.642 % (gap inclus), EV 0.4348 % — **REFUSE**
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.69 % > budget 3.80 %
   - ⚪ atr_grid a 5.5 ATR (stop 32.367 %) — p(stop avant cible) 0.0414 [0.02 ; 0.07], R/R 0.616, perte reelle 32.565 % (gap inclus), EV 0.4241 % — **REFUSE**
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.86 % > budget 3.80 %
   - ⚪ atr_grid a 6.0 ATR (stop 35.31 %) — p(stop avant cible) 0.0249 [0.01 ; 0.05], R/R 0.561, perte reelle 35.737 % (gap inclus), EV 0.5243 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.61 % > budget 3.80 %
   - ⚪ atr_grid a 6.5 ATR (stop 38.252 %) — p(stop avant cible) 0.0138 [0.01 ; 0.03], R/R 0.519, perte reelle 38.66 % (gap inclus), EV 0.5615 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.87 % > budget 3.80 %
   - ⚪ atr_grid a 7.0 ATR (stop 41.195 %) — p(stop avant cible) 0.0067 [0.00 ; 0.02], R/R 0.486, perte reelle 41.288 % (gap inclus), EV 0.6219 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.49 % > budget 3.80 %
   - ⚪ atr_grid a 7.5 ATR (stop 44.137 %) — p(stop avant cible) 0.0042 [0.00 ; 0.02], R/R 0.454, perte reelle 44.137 % (gap inclus), EV 0.6213 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.54 % > budget 3.80 %
   - ⚪ atr_grid a 8.0 ATR (stop 47.08 %) — p(stop avant cible) 0.0039 [0.00 ; 0.02], R/R 0.426, perte reelle 47.08 % (gap inclus), EV 0.615 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.72 % > budget 3.80 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 15.61, ATR14 0.9186 (5.885 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.408 ATR = 2.401 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.294 % | 15.5641 | 91.94 % | 94.35 % | 95.56 % | 96.97 % | 97.46 % | 98.56 % |
| 0.1 ATR | 0.588 % | 15.5181 | 86.2 % | 90.93 % | 92.33 % | 94.84 % | 95.93 % | 97.43 % |
| 0.15 ATR | 0.883 % | 15.4722 | 80.66 % | 87.2 % | 89.0 % | 91.91 % | 94.0 % | 96.1 % |
| 0.2 ATR | 1.177 % | 15.4263 | 74.12 % | 82.66 % | 85.47 % | 88.68 % | 91.46 % | 94.46 % |
| 0.25 ATR | 1.471 % | 15.3803 | 67.98 % | 78.33 % | 81.43 % | 85.54 % | 88.82 % | 92.51 % |
| 0.35 ATR | 2.06 % | 15.2885 | 55.59 % | 68.25 % | 73.56 % | 79.27 % | 84.35 % | 89.63 % |
| 0.5 ATR | 2.942 % | 15.1507 | 41.09 % | 56.85 % | 64.48 % | 71.28 % | 78.86 % | 85.42 % |
| 0.75 ATR | 4.414 % | 14.921 | 21.85 % | 38.81 % | 49.65 % | 58.65 % | 70.53 % | 79.16 % |
| 1.0 ATR | 5.885 % | 14.6914 | 9.87 % | 23.89 % | 33.5 % | 46.41 % | 61.59 % | 72.79 % |
| 1.25 ATR | 7.356 % | 14.4617 | 4.23 % | 14.62 % | 23.61 % | 36.7 % | 52.54 % | 65.5 % |
| 1.5 ATR | 8.827 % | 14.232 | 1.81 % | 7.16 % | 13.62 % | 25.38 % | 42.78 % | 57.39 % |
| 2.0 ATR | 11.77 % | 13.7727 | 0.4 % | 1.81 % | 4.04 % | 10.72 % | 25.2 % | 41.27 % |
| 2.5 ATR | 14.712 % | 13.3134 | 0.1 % | 0.4 % | 1.21 % | 4.35 % | 14.33 % | 29.06 % |
| 3.0 ATR | 17.655 % | 12.8541 | 0.0 % | 0.2 % | 0.5 % | 1.52 % | 7.11 % | 17.35 % |
| 4.0 ATR | 23.54 % | 11.9354 | 0.0 % | 0.1 % | 0.2 % | 0.61 % | 1.93 % | 4.83 % |
| 6.0 ATR | 35.31 % | 10.0981 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.03 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.41 ATR | 0.46 ATR | 0.60 ATR | 0.71 ATR | 0.79 ATR | 1.00 ATR | 1.22 ATR |
| **2 s.** | 0.28 ATR | 0.59 ATR | 0.66 ATR | 0.85 ATR | 0.98 ATR | 1.10 ATR | 1.41 ATR | 1.70 ATR |
| **3 s.** | 0.33 ATR | 0.74 ATR | 0.82 ATR | 1.01 ATR | 1.22 ATR | 1.34 ATR | 1.69 ATR | 1.95 ATR |
| **5 s.** | 0.43 ATR | 0.93 ATR | 1.04 ATR | 1.33 ATR | 1.51 ATR | 1.68 ATR | 2.06 ATR | 2.45 ATR |
| **10 s.** | 0.62 ATR | 1.31 ATR | 1.44 ATR | 1.78 ATR | 2.01 ATR | 2.24 ATR | 2.80 ATR | 3.41 ATR |
| **20 s.** | 0.91 ATR | 1.73 ATR | 1.88 ATR | 2.34 ATR | 2.67 ATR | 2.89 ATR | 3.59 ATR | 3.99 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.46–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.942 %, prix 15.1508), p(touche) 41.09 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (70.0 % des re-echantillons)
- **2 seance(s)** : plage utile 0.664–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.414 %, prix 14.921), p(touche) 38.81 % (en stress 93.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.822–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.885 %, prix 14.6914), p(touche) 33.5 % (en stress 89.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.036–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.356 %, prix 14.4617), p(touche) 36.7 % (en stress 94.95 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.443–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.827 %, prix 14.2321), p(touche) 42.78 % (en stress 96.97 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.884–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (11.77 %, prix 13.7727), p(touche) 41.27 % (en stress 97.96 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.027 | EV/share : $0.008 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 — | T3 —
- Kelly (position) : f* 0.039 | ¼-Kelly 0.01 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 17.8 | side 77.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 153.0 (= 11 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.143% → cible +3.07% / stop −2.0%, p_fill 31%, n_eff≈36.8) : P(cible|rempli) **16%** · **EV/risk -0.128** (×p_fill ; si rempli -0.82% du capital)
  - **swing** (entrée dip −9.115% → cible +9.956% / stop −6.475%, p_fill 16%, n_eff≈19.5) : P(cible|rempli) **36%** · **EV/risk +0.023** (×p_fill ; si rempli +0.94% du capital)
  - **deep** (entrée dip −14.082% → cible +10.83% / stop −10.275%, p_fill 14%, n_eff≈17.7) : P(cible|rempli) **63%** · **EV/risk +0.057** (×p_fill ; si rempli +4.16% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→78% · +2.0%→66% · +3.0%→48% · +5.0%→32% · +8.0%→11%
- Range intraday médian 6.92% (p90 11.08%) · excursion haute méd. +2.81% / basse méd. −2.46%
- Profil de vol intra : ouverture 4.738% vs midi 1.412% vs clôture 1.634% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 20% · trend ↑0%/↓0% ; spike-down 64% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.128 ; neutre — autocorr -0.007)_ ; drift intra méd. -0.305% ; recovery-V 24%
- **σ réalisé intraday** 3.787% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 58% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 15.7512 (VA 15.7308–15.9767 ; dernier close 15.73)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 38% · rebond 74% · **stop −5.33%** sous le fill (sous le bruit) · cible +2.24% · R/R 0.42 (high win-rate)
- Gaps overnight (n=159) : méd. -0.29% · baisse 57% (gap-down >1% 38% · >2% 23%)
- Excursion ouverture 5min (n=160) : bas méd −0.81% (p90 −2.89%) · haut méd +1.21% · range méd 2.42%
- Excursion ouverture 15min (n=160) : bas méd −1.22% (p90 −3.63%) · haut méd +1.67% · range méd 3.36%
- Excursion ouverture 30min (n=160) : bas méd −1.46% (p90 −4.51%) · haut méd +1.92% · range méd 3.85%
- Excursion ouverture 60min (n=160) : bas méd −1.69% (p90 −5.47%) · haut méd +2.14% · range méd 4.65%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 15.74 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 72% · séance 80% (130/159) · gap 46% · délai 0.0min · rebond 63% (83/130) (MFE +1.59%)
   - −1.0% : fill 30min 61% · séance 70% (119/159) · gap 38% · délai 0.0min · rebond 68% (77/119) (MFE +1.69%)
   - −1.5% : fill 30min 56% · séance 63% (111/159) · gap 28% · délai 0.0min · rebond 70% (74/111) (MFE +2.07%)
   - −2.0% : fill 30min 50% · séance 57% (102/159) · gap 23% · délai 0.1min · rebond 69% (68/102) (MFE +2.19%)
   - −3.0% : fill 30min 34% · séance 48% (89/159) · gap 9% · délai 5.2min · rebond 67% (63/89) (MFE +1.88%)
   - −4.0% : fill 30min 25% · séance 38% (68/159) · gap 6% · délai 15.0min · rebond 74% (50/68) (MFE +2.24%)
   - −5.0% : fill 30min 12% · séance 27% (55/159) · gap 1% · délai 32.8min · rebond 57% (36/55) (MFE +1.51%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.38% (p90 −1.89%) → stop au-delà de −1.5% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.57% (p90 −2.28%) → stop au-delà de −1.73% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.57% (p90 −2.38%) → stop au-delà de −1.65% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1080 jambes) : jambe baissière méd −1.27% (p90 −3.04%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (84 séances) :
      · −1.0% : fill 92% (80/84) · rebond 65% (48/80)
      · −2.0% : fill 82% (74/84) · rebond 68% (48/74)
      · −3.0% : fill 70% (67/84) · rebond 62% (45/67)
      · −4.0% : fill 60% (53/84) · rebond 70% (38/53)
      · −5.0% : fill 43% (44/84) · rebond 51% (27/44)
   - **flat** (15 séances) :
      · −1.0% : fill 81% (13/15) · rebond 97% (12/13)
      · −2.0% : fill 56% (10/15) · rebond 90% (9/10)
      · −3.0% : fill 28% (5/15) · rebond 92% (4/5)
      · −4.0% : fill 18% (4/15) · rebond 87% (3/4)
      · −5.0% : fill 11% (3/15) · rebond 100% (3/3)
   - **gap-up** (60 séances) :
      · −1.0% : fill 39% (26/60) · rebond 60% (17/26)
      · −2.0% : fill 27% (18/60) · rebond 62% (11/18)
      · −3.0% : fill 25% (17/60) · rebond 77% (14/17)
      · −4.0% : fill 16% (11/60) · rebond 91% (9/11)
      · −5.0% : fill 11% (8/60) · rebond 78% (6/8)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 70% si les 15 1res min sont vertes (86 cas) · 23% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:29** → P(séance verte=clôture>ouverture) 89% si début vert vs 10% si rouge (base 49% · écart 78 pts) ; prédictivité sature ensuite (plafond brut 94min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **89%** · continue >prix actuel 49% ; creux résiduel méd -1.48% (q20 -2.59%) → **SL/trailing à −2.59%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.78% / q75 +3.27% → **scale +1.78% / runner +3.27%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **10%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.43%** (au-delà de la MAE q10 -4.43%), cible rebond +1.71% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.11% .. +4.42%] · haut q95 +5.8% · bas q05 -6.2%
   - 60min (n=160) : retour [-6.15% .. +5.95%] · haut q95 +6.56% · bas q05 -7.0%
   - 2h (n=160) : retour [-6.81% .. +5.99%] · haut q95 +6.81% · bas q05 -7.33%
   - 4h (n=160) : retour [-6.6% .. +6.26%] · haut q95 +8.18% · bas q05 -7.79%
   - 6h (n=160) : retour [-7.05% .. +7.2%] · haut q95 +9.18% · bas q05 -8.48%
   - session (n=160) : retour [-7.08% .. +7.21%] · haut q95 +9.2% · bas q05 -8.56%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 7.1)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **21%**. Lecture précoce 30 min : signature présente → 10% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.26% (p75 1.66% / p90 2.43%) · ~4.04 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 15.0 min, n=43)
   - −1.0% → **83%** (reprise méd 35.0 min, n=27)
   - −1.5% → **83%** (reprise méd 93.49 min, n=16)
   - −2.0% → **84%** (reprise méd 44.98 min, n=8)
   - −3.0% → **66%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.43%** (p90, défaut prudent ; serré/agressif −1.66%) ; extension open→close méd +8.12% (q75 +9.53% / q95 +9.89%), MFE méd +9.52% / q90 +11.18%
   - Échelle scale-out : +9.52% (33%) / +10.45% (33%) / +11.18% (34%)
- **DÉSARMER** : repli > **−2.43%** depuis le plus-haut = décay → P(retournement) **26%** (préavis méd 141.49 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +11.18% : P(retournement après) 0% (mèche méd 1.88%)
- **CONTEXTE** : la dernière heure tient les gains 67% du temps (retour médian dernière heure +0.12%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.61 · part idiosyncratique 0.39
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 53.5  _(neutre)_
- **ADX** : 10.5  _(pas de tendance nette)_
- **MACD** : hist 0.035  _(pas de croisement recent)_
- **BB** : %B 0.46 · largeur 14.1%
- **ATR** : 0.92 (4.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.182  _(distribution)_
- **Vol ratio** : 0.66  _(volume normal)_
- **Choppiness** : 52.1  _(transition)_
- **MA** : MA20 15.7 · MA50 16.13 · MA200 18.37  _(prix < MA20)_
- **Dist MA** : MA20 -0.6% · MA50 -3.2% · MA200 -15.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (853387 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
