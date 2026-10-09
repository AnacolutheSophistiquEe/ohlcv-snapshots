# RGTI

**Generated** : 2026-10-09T00:29:13.231986+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 2/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $14.16  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (4 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot $14.16 (+2.1% vs entrée) · entrée $13.87 · stop $13.60 · T1 $14.29 · R/R 1.56  
> ↳ ¼-Kelly 0.002 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +2.8 % ≠ (strike 15.0 − spot 14.16)/spot = +5.9 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 255 % hors [0,100] (R² max 0.90). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-08 : 14.16 · ATR Wilder 0.8691 (6.14 %)_
- **Swing** : plage **13.11 → 12.67** (-7.41 % a -10.48 % sous la cloture, 0.5 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 12.34-12.75 (A). stop INDICATIF 11.44 (-9.77 % sous le bas ; sous le support 11.87-12.08 (- 0,5 ATR)).
- **Deep** : plage **12.67 → 11.61** (-10.48 % a -18.0 % sous la cloture, 1.22 ATR) — touchee 43 % → 15 % du temps en 20 seances ; supports reels dans la plage : 12.34-12.75 (A) ; 11.87-12.08 (B) ; 11.4-11.8 (B). stop INDICATIF 10.28 (-11.49 % sous le bas ; sous le support 10.71-10.92 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (COMBO) : 4.03 ATR sous le plus haut 20 s., RSI(2) 0.8. Limite **13.72** (seance suivante), stop catastrophe 10.25, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 13.61-13.82 (C, -2.39 %) ; 13.13-13.56 (A, -4.22 %) ; 12.34-12.75 (A, -9.94 %) ; 11.87-12.08 (B, -14.68 %) ; 11.4-11.8 (B, -16.65 %) ; 10.71-10.92 (A, -22.87 %)
- Resistances reelles au-dessus : 14.75-15.18 (A, 4.18 %) ; 15.3-15.66 (A, 8.07 %) ; 15.94-16.3 (A, 12.59 %) ; 16.74-17.05 (A, 18.24 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.46 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.23 %)** : le gap seul le franchit 0.798 % des séances (10 fois sur 1253).
   - exécution **3.405 pt plus bas** dans le cas TYPIQUE (médiane), 9.017 au p90, **20.983 au pire**
   - perte réelle **15.002 %** en moyenne _(tirée par la queue)_, jusqu'à **31.213 %** — au lieu des 10.23 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0381 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 10 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.113 % | p01 -8.973 % | pire -31.213 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5037** [0.4297 ; 0.5776] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.5073** [0.4547 ; 0.5598] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.528** [0.4753 ; 0.5802] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : deep (25.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.95 %** | CVaR **-11.33 %** | vol 6.82 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 19.32 % contre 6.20 % aujourd'hui, rapport 3.12)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -21.76 % vs -22.11 % si l'on extrapolait par √5 _(rapport 0.984 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8364** (β de hausse 1.9993, asymétrie 0.9185) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.474× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 13.7456 sur atr_grid (0.5 ATR, 2.913 %) — p(stop avant cible) 0.8493 [0.81 ; 0.88], R/R 6.969, perte reelle 2.99 % (gap inclus), CVaR 4.2 %, EV 0.0632 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.2432 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 11.5 % du temps (< 15 %) meme a 10 seances : le R/R de 6.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.849, borne haute 0.884 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 4.20 % > budget 3.00 %
- Budget de queue : **3.0 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.114 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 42.1 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
   - ⚠ budget **borne** (brut 1.95 %) : les bornes sont un choix declare, pas une mesure.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 8.739 %) — p(stop avant cible) 0.6192 [0.57 ; 0.67], R/R 2.336, perte reelle 8.92 % (gap inclus), EV -0.624 % — **REFUSE**
      - refuse : p_stop_first 0.619, borne haute 0.669 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 10.96 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.62 %) : P(cible) 20.9 % x 20.83 % + P(rien) 17.2 % x 3.18 % ne couvrent pas P(stop) 61.9 % x 8.92 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ sr_based a 1.48 ATR (stop 11.336 %) — p(stop avant cible) 0.5371 [0.48 ; 0.59], R/R 1.816, perte reelle 11.472 % (gap inclus), EV -1.0796 % — **REFUSE**
      - refuse : p_stop_first 0.537, borne haute 0.589 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.80 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.08 %) : P(cible) 22.2 % x 20.83 % + P(rien) 24.1 % x 1.87 % ne couvrent pas P(stop) 53.7 % x 11.47 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 1.97 ATR (stop 14.237 %) — p(stop avant cible) 0.3956 [0.35 ; 0.45], R/R 1.447, perte reelle 14.401 % (gap inclus), EV -0.5554 % — **REFUSE**
      - refuse : R/R 1.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.53 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.56 %) : P(cible) 24.3 % x 20.83 % + P(rien) 36.1 % x 0.22 % ne couvrent pas P(stop) 39.6 % x 14.40 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 1.456 %) — p(stop avant cible) 0.9289 [0.90 ; 0.95], R/R 13.646, perte reelle 1.527 % (gap inclus), EV -0.048 % — **REFUSE**
      - refuse : cible atteinte seulement 6.3 % du temps (< 15 %) meme a 10 seances : le R/R de 13.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.929, borne haute 0.953 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.05 %) : P(cible) 6.3 % x 20.83 % + P(rien) 0.8 % x 7.61 % ne couvrent pas P(stop) 92.9 % x 1.53 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 2.913 %) — p(stop avant cible) 0.8493 [0.81 ; 0.88], R/R 6.969, perte reelle 2.99 % (gap inclus), EV 0.0632 % — **REFUSE**
      - refuse : cible atteinte seulement 11.5 % du temps (< 15 %) meme a 10 seances : le R/R de 6.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.849, borne haute 0.884 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 4.20 % > budget 3.00 %
   - ⚪ atr_grid a 0.75 ATR (stop 4.369 %) — p(stop avant cible) 0.7938 [0.75 ; 0.83], R/R 4.678, perte reelle 4.453 % (gap inclus), EV -0.1792 % — **REFUSE**
      - refuse : cible atteinte seulement 14.4 % du temps (< 15 %) meme a 10 seances : le R/R de 4.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.794, borne haute 0.834 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 5.62 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.18 %) : P(cible) 14.4 % x 20.83 % + P(rien) 6.3 % x 5.82 % ne couvrent pas P(stop) 79.4 % x 4.45 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 5.826 %) — p(stop avant cible) 0.7349 [0.69 ; 0.78], R/R 3.49, perte reelle 5.97 % (gap inclus), EV -0.3584 % — **REFUSE**
      - refuse : p_stop_first 0.735, borne haute 0.779 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 7.82 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 17.2 % x 20.83 % + P(rien) 9.4 % x 4.87 % ne couvrent pas P(stop) 73.5 % x 5.97 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 1.48 ATR (stop 10.345 %) — p(stop avant cible) 0.5846 [0.53 ; 0.64], R/R 1.983, perte reelle 10.504 % (gap inclus), EV -1.2354 % — **REFUSE**
      - refuse : p_stop_first 0.585, borne haute 0.636 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.16 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.24 %) : P(cible) 21.5 % x 20.83 % + P(rien) 20.1 % x 2.15 % ne couvrent pas P(stop) 58.5 % x 10.50 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 grid_snapped a 1.97 ATR (stop 13.247 %) — p(stop avant cible) 0.431 [0.38 ; 0.48], R/R 1.552, perte reelle 13.423 % (gap inclus), EV -0.568 % — **REFUSE**
      - refuse : R/R 1.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.76 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.57 %) : P(cible) 23.7 % x 20.83 % + P(rien) 33.2 % x 0.86 % ne couvrent pas P(stop) 43.1 % x 13.42 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 16.021 %) — p(stop avant cible) 0.3111 [0.26 ; 0.36], R/R 1.283, perte reelle 16.233 % (gap inclus), EV -0.4134 % — **REFUSE**
      - refuse : R/R 1.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.34 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.41 %) : P(cible) 24.8 % x 20.83 % + P(rien) 44.1 % x -1.21 % ne couvrent pas P(stop) 31.1 % x 16.23 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 17.478 %) — p(stop avant cible) 0.2648 [0.22 ; 0.31], R/R 1.178, perte reelle 17.688 % (gap inclus), EV -0.2532 % — **REFUSE**
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.59 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.25 %) : P(cible) 25.7 % x 20.83 % + P(rien) 47.9 % x -1.91 % ne couvrent pas P(stop) 26.5 % x 17.69 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 20.391 %) — p(stop avant cible) 0.1845 [0.15 ; 0.23], R/R 1.006, perte reelle 20.713 % (gap inclus), EV 0.0251 % — **REFUSE**
      - refuse : R/R 1.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.58 % > budget 3.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 23.304 %) — p(stop avant cible) 0.1146 [0.08 ; 0.15], R/R 0.882, perte reelle 23.631 % (gap inclus), EV 0.152 % — **REFUSE**
      - refuse : R/R 0.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.05 % > budget 3.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 26.217 %) — p(stop avant cible) 0.0773 [0.05 ; 0.11], R/R 0.786, perte reelle 26.494 % (gap inclus), EV 0.2783 % — **REFUSE**
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.64 % > budget 3.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 29.13 %) — p(stop avant cible) 0.0611 [0.04 ; 0.09], R/R 0.709, perte reelle 29.363 % (gap inclus), EV 0.2637 % — **REFUSE**
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.42 % > budget 3.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 32.043 %) — p(stop avant cible) 0.0403 [0.02 ; 0.07], R/R 0.646, perte reelle 32.272 % (gap inclus), EV 0.2596 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.46 % > budget 3.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 34.956 %) — p(stop avant cible) 0.0242 [0.01 ; 0.04], R/R 0.589, perte reelle 35.38 % (gap inclus), EV 0.3558 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.23 % > budget 3.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 37.869 %) — p(stop avant cible) 0.0134 [0.00 ; 0.03], R/R 0.543, perte reelle 38.369 % (gap inclus), EV 0.3882 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.60 % > budget 3.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 40.782 %) — p(stop avant cible) 0.008 [0.00 ; 0.02], R/R 0.509, perte reelle 40.912 % (gap inclus), EV 0.4366 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.41 % > budget 3.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 43.695 %) — p(stop avant cible) 0.0041 [0.00 ; 0.02], R/R 0.477, perte reelle 43.695 % (gap inclus), EV 0.4419 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.34 % > budget 3.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 46.607 %) — p(stop avant cible) 0.0039 [0.00 ; 0.02], R/R 0.446, perte reelle 46.661 % (gap inclus), EV 0.4333 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.51 % > budget 3.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 14.158, ATR14 0.8248 (5.826 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.407 ATR = 2.371 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.291 % | 14.1168 | 91.94 % | 94.35 % | 95.56 % | 96.97 % | 97.46 % | 98.56 % |
| 0.1 ATR | 0.583 % | 14.0755 | 86.3 % | 91.03 % | 92.43 % | 94.94 % | 95.93 % | 97.43 % |
| 0.15 ATR | 0.874 % | 14.0343 | 80.77 % | 87.3 % | 89.1 % | 92.01 % | 94.0 % | 96.1 % |
| 0.2 ATR | 1.165 % | 13.993 | 74.22 % | 82.76 % | 85.57 % | 88.78 % | 91.46 % | 94.46 % |
| 0.25 ATR | 1.456 % | 13.9518 | 68.18 % | 78.53 % | 81.63 % | 85.74 % | 88.92 % | 92.51 % |
| 0.35 ATR | 2.039 % | 13.8693 | 55.59 % | 68.55 % | 73.86 % | 79.58 % | 84.55 % | 89.63 % |
| 0.5 ATR | 2.913 % | 13.7456 | 40.99 % | 56.96 % | 64.78 % | 71.59 % | 79.17 % | 85.32 % |
| 0.75 ATR | 4.369 % | 13.5394 | 21.75 % | 38.81 % | 49.95 % | 58.95 % | 70.83 % | 78.95 % |
| 1.0 ATR | 5.826 % | 13.3332 | 9.77 % | 23.89 % | 33.6 % | 46.71 % | 61.99 % | 72.48 % |
| 1.25 ATR | 7.282 % | 13.127 | 4.13 % | 14.62 % | 23.61 % | 36.91 % | 52.85 % | 65.09 % |
| 1.5 ATR | 8.739 % | 12.9207 | 1.81 % | 7.16 % | 13.62 % | 25.48 % | 42.99 % | 56.98 % |
| 2.0 ATR | 11.652 % | 12.5083 | 0.4 % | 1.81 % | 4.04 % | 10.72 % | 25.3 % | 40.76 % |
| 2.5 ATR | 14.565 % | 12.0959 | 0.1 % | 0.4 % | 1.21 % | 4.35 % | 14.43 % | 28.54 % |
| 3.0 ATR | 17.478 % | 11.6835 | 0.0 % | 0.2 % | 0.5 % | 1.52 % | 7.22 % | 16.84 % |
| 4.0 ATR | 23.304 % | 10.8587 | 0.0 % | 0.1 % | 0.2 % | 0.61 % | 1.93 % | 4.31 % |
| 6.0 ATR | 34.956 % | 9.209 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.03 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.41 ATR | 0.46 ATR | 0.60 ATR | 0.71 ATR | 0.79 ATR | 0.99 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.60 ATR | 0.67 ATR | 0.85 ATR | 0.98 ATR | 1.10 ATR | 1.41 ATR | 1.70 ATR |
| **3 s.** | 0.34 ATR | 0.75 ATR | 0.83 ATR | 1.01 ATR | 1.22 ATR | 1.34 ATR | 1.69 ATR | 1.95 ATR |
| **5 s.** | 0.44 ATR | 0.93 ATR | 1.04 ATR | 1.34 ATR | 1.52 ATR | 1.69 ATR | 2.06 ATR | 2.45 ATR |
| **10 s.** | 0.62 ATR | 1.32 ATR | 1.45 ATR | 1.78 ATR | 2.01 ATR | 2.24 ATR | 2.81 ATR | 3.42 ATR |
| **20 s.** | 0.90 ATR | 1.72 ATR | 1.87 ATR | 2.32 ATR | 2.65 ATR | 2.87 ATR | 3.55 ATR | 3.94 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.459–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.913 %, prix 13.7456), p(touche) 40.99 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (67.4 % des re-echantillons)
- **2 seance(s)** : plage utile 0.665–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.369 %, prix 13.5394), p(touche) 38.81 % (en stress 93.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.826–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.826 %, prix 13.3332), p(touche) 33.6 % (en stress 89.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.044–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.282 %, prix 13.127), p(touche) 36.91 % (en stress 94.95 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.449–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.739 %, prix 12.9207), p(touche) 42.99 % (en stress 96.97 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (67.2 % des re-echantillons)
- **20 seance(s)** : plage utile 1.869–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (11.652 %, prix 12.5083), p(touche) 40.76 % (en stress 97.96 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.005 | EV/share : $0.001 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 38 % | T2 — | T3 —
- Kelly (position) : f* 0.007 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 18.9 | side 76.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.0% → cible +2.972% / stop −2.0%, p_fill 53%, n_eff≈60.1) : P(cible|rempli) **29%** · **EV/risk -0.121** (×p_fill ; si rempli -0.45% du capital)
  - **swing** (entrée dip −4.404% → cible +6.814% / stop −6.094%, p_fill 53%, n_eff≈63.6) : P(cible|rempli) **41%** · **EV/risk -0.069** (×p_fill ; si rempli -0.78% du capital)
  - **deep** (entrée dip −6.811% → cible +9.885% / stop −9.377%, p_fill 51%, n_eff≈58.2) : P(cible|rempli) **45%** · **EV/risk -0.002** (×p_fill ; si rempli -0.03% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→87% · +1.0%→77% · +2.0%→64% · +3.0%→46% · +5.0%→31% · +8.0%→10%
- Range intraday médian 6.8% (p90 11.03%) · excursion haute méd. +2.76% / basse méd. −2.46%
- Profil de vol intra : ouverture 4.714% vs midi 1.402% vs clôture 1.624% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 79% · range 21% · trend ↑0%/↓0% ; spike-down 65% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.134 ; neutre — autocorr -0.001)_ ; drift intra méd. -0.541% ; recovery-V 20%
- **σ réalisé intraday** 3.707% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 62% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 15.5684 (VA 15.2377–15.7574 ; dernier close 15.26)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 37% · rebond 75% · **stop −5.27%** sous le fill (sous le bruit) · cible +2.24% · R/R 0.43 (high win-rate)
- Gaps overnight (n=159) : méd. -0.2% · baisse 55% (gap-down >1% 36% · >2% 22%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −2.87%) · haut méd +1.18% · range méd 2.39%
- Excursion ouverture 15min (n=160) : bas méd −1.22% (p90 −3.58%) · haut méd +1.56% · range méd 3.3%
- Excursion ouverture 30min (n=160) : bas méd −1.45% (p90 −4.44%) · haut méd +1.84% · range méd 3.8%
- Excursion ouverture 60min (n=160) : bas méd −1.69% (p90 −5.46%) · haut méd +2.09% · range méd 4.51%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 15.25 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 80% (130/159) · gap 44% · délai 0.0min · rebond 63% (83/130) (MFE +1.59%)
   - −1.0% : fill 30min 60% · séance 71% (119/159) · gap 36% · délai 0.0min · rebond 70% (78/119) (MFE +1.68%)
   - −1.5% : fill 30min 54% · séance 63% (111/159) · gap 27% · délai 0.0min · rebond 68% (74/111) (MFE +1.92%)
   - −2.0% : fill 30min 48% · séance 57% (102/159) · gap 22% · délai 0.2min · rebond 67% (68/102) (MFE +2.13%)
   - −3.0% : fill 30min 33% · séance 48% (89/159) · gap 8% · délai 8.9min · rebond 65% (63/89) (MFE +1.87%)
   - −4.0% : fill 30min 24% · séance 37% (67/159) · gap 5% · délai 15.3min · rebond 75% (50/67) (MFE +2.24%)
   - −5.0% : fill 30min 12% · séance 26% (54/159) · gap 1% · délai 32.8min · rebond 57% (35/54) (MFE +1.49%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.35% (p90 −1.86%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.57% (p90 −2.28%) → stop au-delà de −1.73% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.57% (p90 −2.38%) → stop au-delà de −1.65% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1068 jambes) : jambe baissière méd −1.27% (p90 −3.0%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (83 séances) :
      · −1.0% : fill 92% (79/83) · rebond 66% (48/79)
      · −2.0% : fill 82% (73/83) · rebond 68% (48/73)
      · −3.0% : fill 70% (66/83) · rebond 62% (45/66)
      · −4.0% : fill 60% (52/83) · rebond 70% (38/52)
      · −5.0% : fill 43% (43/83) · rebond 50% (26/43)
   - **flat** (16 séances) :
      · −1.0% : fill 84% (14/16) · rebond 98% (13/14)
      · −2.0% : fill 48% (10/16) · rebond 90% (9/10)
      · −3.0% : fill 24% (5/16) · rebond 92% (4/5)
      · −4.0% : fill 16% (4/16) · rebond 87% (3/4)
      · −5.0% : fill 10% (3/16) · rebond 100% (3/3)
   - **gap-up** (60 séances) :
      · −1.0% : fill 41% (26/60) · rebond 64% (17/26)
      · −2.0% : fill 30% (19/60) · rebond 53% (11/19)
      · −3.0% : fill 29% (18/60) · rebond 65% (14/18)
      · −4.0% : fill 15% (11/60) · rebond 91% (9/11)
      · −5.0% : fill 10% (8/60) · rebond 78% (6/8)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 70% si les 15 1res min sont vertes (86 cas) · 21% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:38** → P(séance verte=clôture>ouverture) 86% si début vert vs 10% si rouge (base 47% · écart 76 pts) ; prédictivité sature ensuite (plafond brut 140min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=83) : tient le vert **86%** · continue >prix actuel 47% ; creux résiduel méd -1.49% (q20 -2.51%) → **SL/trailing à −2.51%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.67% / q75 +3.2% → **scale +1.67% / runner +3.2%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **10%** (continue à baisser 61%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.18%** (au-delà de la MAE q10 -4.18%), cible rebond +1.6% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.03% .. +4.37%] · haut q95 +5.8% · bas q05 -6.04%
   - 60min (n=160) : retour [-6.1% .. +5.82%] · haut q95 +6.56% · bas q05 -7.0%
   - 2h (n=160) : retour [-6.68% .. +5.93%] · haut q95 +6.77% · bas q05 -7.24%
   - 4h (n=160) : retour [-6.76% .. +6.25%] · haut q95 +7.97% · bas q05 -7.75%
   - 6h (n=160) : retour [-6.74% .. +6.96%] · haut q95 +9.18% · bas q05 -8.44%
   - session (n=160) : retour [-7.06% .. +7.17%] · haut q95 +9.19% · bas q05 -8.49%


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
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.57 · part idiosyncratique 0.43
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 32.2  _(momentum baissier)_
- **ADX** : 9.5  _(pas de tendance nette)_
- **MACD** : hist -0.148  _(pas de croisement recent)_
- **BB** : %B -0.02 · largeur 17.6%
- **ATR** : 0.82 (2.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.172  _(distribution)_
- **Vol ratio** : 0.89  _(volume normal)_
- **Choppiness** : 40.9  _(transition)_
- **MA** : MA20 15.59 · MA50 16.17 · MA200 18.16  _(prix < MA20)_
- **Dist MA** : MA20 -9.2% · MA50 -12.5% · MA200 -22.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (860550 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
