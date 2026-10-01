# ENR

**Generated** : 2026-10-01T00:07:52.766402+00:00  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €142.50  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot €142.50 (+5.6% vs entrée) · entrée €134.90 · stop €129.78 · T1 €140.64 · R/R 1.12  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €133.97–€135.84 (mid €134.90)
- Spot actuel : €142.50 (+5.6% au-dessus de la zone — repli à attendre)
- Stop : €129.78 (plancher anti-bruit (R/R<2) ; -3.80 % depuis l'entree)
- Targets : T1 €140.64 · R/R 1.12 | T2 €146.37 · R/R 2.24 | T3 €152.10 · R/R 3.36
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €129.78


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.59 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.93 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1274).
   - exécution **7.24 pt plus bas** dans le cas TYPIQUE (médiane), 22.91 au p90, **26.827 au pire**
   - perte réelle **21.854 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 8.93 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0304 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.33 % | p01 -5.088 % | pire -35.757 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5124** [0.4382 ; 0.5861] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.502** [0.4495 ; 0.5545] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4676** [0.4155 ; 0.5203] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (29.3 pt), swing (35.2 pt), deep (32.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-4.63 %** | CVaR **-6.59 %** | vol 3.2 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 5.95 % contre 3.01 % aujourd'hui, rapport 1.98)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.81 % vs -9.75 % si l'on extrapolait par √5 _(rapport 0.904 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3567** (β de hausse 1.084, asymétrie 1.2516) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.34× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 128.7165 sur grid_snapped (2.39 ATR, 9.673 %) — p(stop avant cible) 0.286 [0.24 ; 0.34], R/R 3.201, perte reelle 9.919 % (gap inclus), CVaR 11.083 %, EV -0.156 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.9767 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.397 %) — p(stop avant cible) 0.585 [0.53 ; 0.64], R/R 5.679, perte reelle 5.591 % (gap inclus), EV -0.398 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 5.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.585, borne haute 0.636 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.40 %) : P(cible) 0.4 % x 31.75 % + P(rien) 41.1 % x 6.71 % ne couvrent pas P(stop) 58.5 % x 5.59 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ swing_based a 2.39 ATR (stop 10.871 %) — p(stop avant cible) 0.2027 [0.16 ; 0.25], R/R 2.805, perte reelle 11.319 % (gap inclus), EV 0.1455 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.69 % > budget 12.00 %
   - ⚪ sr_based a 2.79 ATR (stop 12.328 %) — p(stop avant cible) 0.1298 [0.10 ; 0.17], R/R 2.453, perte reelle 12.943 % (gap inclus), EV 0.4393 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.92 % > budget 12.00 %
   - 🟢 support a 6.32 ATR (stop 25.028 %) — p(stop avant cible) 0.0039 [0.00 ; 0.02], R/R 1.139, perte reelle 27.881 % (gap inclus), EV 1.1796 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.59 % > budget 12.00 %
   - 🟢 support a 9.46 ATR (stop 36.313 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 0.872, perte reelle 36.424 % (gap inclus), EV 1.2076 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.06 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.899 %) — p(stop avant cible) 0.9308 [0.90 ; 0.95], R/R 33.261, perte reelle 0.955 % (gap inclus), EV -0.1481 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 33.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.931, borne haute 0.954 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 0.1 % x 31.75 % + P(rien) 6.8 % x 10.30 % ne couvrent pas P(stop) 93.1 % x 0.95 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 1.799 %) — p(stop avant cible) 0.852 [0.81 ; 0.89], R/R 16.703, perte reelle 1.901 % (gap inclus), EV -0.2299 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 16.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.852, borne haute 0.886 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.23 %) : P(cible) 0.2 % x 31.75 % + P(rien) 14.6 % x 9.10 % ne couvrent pas P(stop) 85.2 % x 1.90 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 2.698 %) — p(stop avant cible) 0.7858 [0.74 ; 0.83], R/R 11.257, perte reelle 2.82 % (gap inclus), EV -0.2979 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 11.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.786, borne haute 0.827 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.30 %) : P(cible) 0.3 % x 31.75 % + P(rien) 21.1 % x 8.59 % ne couvrent pas P(stop) 78.6 % x 2.82 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 3.598 %) — p(stop avant cible) 0.7079 [0.66 ; 0.75], R/R 8.527, perte reelle 3.723 % (gap inclus), EV -0.2071 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 8.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.708, borne haute 0.754 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.21 %) : P(cible) 0.3 % x 31.75 % + P(rien) 28.9 % x 8.04 % ne couvrent pas P(stop) 70.8 % x 3.72 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 4.497 %) — p(stop avant cible) 0.6324 [0.58 ; 0.68], R/R 6.818, perte reelle 4.657 % (gap inclus), EV -0.1932 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 6.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.632, borne haute 0.682 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.19 %) : P(cible) 0.3 % x 31.75 % + P(rien) 36.4 % x 7.26 % ne couvrent pas P(stop) 63.2 % x 4.66 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 6.296 %) — p(stop avant cible) 0.5221 [0.47 ; 0.57], R/R 4.856, perte reelle 6.538 % (gap inclus), EV -0.5358 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 4.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.522, borne haute 0.574 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.54 %) : P(cible) 0.4 % x 31.75 % + P(rien) 47.4 % x 5.83 % ne couvrent pas P(stop) 52.2 % x 6.54 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 7.196 %) — p(stop avant cible) 0.4572 [0.41 ; 0.51], R/R 4.283, perte reelle 7.412 % (gap inclus), EV -0.4617 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 4.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.46 %) : P(cible) 0.4 % x 31.75 % + P(rien) 53.9 % x 5.22 % ne couvrent pas P(stop) 45.7 % x 7.41 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 2.39 ATR (stop 9.673 %) — p(stop avant cible) 0.286 [0.24 ; 0.34], R/R 3.201, perte reelle 9.919 % (gap inclus), EV -0.156 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 0.4 % x 31.75 % + P(rien) 71.0 % x 3.62 % ne couvrent pas P(stop) 28.6 % x 9.92 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 14.392 %) — p(stop avant cible) 0.0736 [0.05 ; 0.10], R/R 2.041, perte reelle 15.554 % (gap inclus), EV 0.7391 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.10 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 16.191 %) — p(stop avant cible) 0.0351 [0.02 ; 0.06], R/R 1.776, perte reelle 17.879 % (gap inclus), EV 0.9789 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.26 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 17.99 %) — p(stop avant cible) 0.0284 [0.01 ; 0.05], R/R 1.672, perte reelle 18.988 % (gap inclus), EV 1.0052 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.08 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 19.789 %) — p(stop avant cible) 0.0152 [0.01 ; 0.03], R/R 1.502, perte reelle 21.142 % (gap inclus), EV 1.0892 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.37 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 21.588 %) — p(stop avant cible) 0.0073 [0.00 ; 0.02], R/R 1.282, perte reelle 24.767 % (gap inclus), EV 1.1113 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.15 % > budget 12.00 %
   - 🟢 grid_snapped a 6.32 ATR (stop 23.83 %) — p(stop avant cible) 0.0053 [0.00 ; 0.02], R/R 1.193, perte reelle 26.624 % (gap inclus), EV 1.1417 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.91 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 26.985 %) — p(stop avant cible) 0.0033 [0.00 ; 0.01], R/R 1.096, perte reelle 28.964 % (gap inclus), EV 1.1882 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.43 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 28.784 %) — p(stop avant cible) 0.0026 [0.00 ; 0.01], R/R 1.055, perte reelle 30.082 % (gap inclus), EV 1.1966 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.28 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 142.5, ATR14 5.1271 (3.598 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.367 ATR = 1.32 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.18 % | 142.2436 | 91.52 % | 94.08 % | 95.55 % | 96.14 % | 97.21 % | 97.89 % |
| 0.1 ATR | 0.36 % | 141.9873 | 83.83 % | 88.15 % | 90.61 % | 92.67 % | 94.63 % | 95.68 % |
| 0.15 ATR | 0.54 % | 141.7309 | 76.33 % | 82.33 % | 85.87 % | 88.51 % | 91.14 % | 93.27 % |
| 0.2 ATR | 0.72 % | 141.4746 | 70.41 % | 79.07 % | 83.0 % | 86.34 % | 89.35 % | 91.86 % |
| 0.25 ATR | 0.899 % | 141.2182 | 63.91 % | 74.73 % | 79.35 % | 83.17 % | 87.26 % | 90.45 % |
| 0.35 ATR | 1.259 % | 140.7055 | 51.78 % | 64.86 % | 70.36 % | 75.74 % | 81.89 % | 86.33 % |
| 0.5 ATR | 1.799 % | 139.9364 | 36.39 % | 51.73 % | 59.49 % | 66.24 % | 74.23 % | 80.2 % |
| 0.75 ATR | 2.698 % | 138.6546 | 19.63 % | 35.74 % | 45.16 % | 54.26 % | 65.17 % | 73.27 % |
| 1.0 ATR | 3.598 % | 137.3729 | 11.05 % | 25.37 % | 34.19 % | 43.86 % | 56.52 % | 64.92 % |
| 1.25 ATR | 4.497 % | 136.0911 | 6.11 % | 17.28 % | 24.9 % | 35.54 % | 48.06 % | 57.29 % |
| 1.5 ATR | 5.397 % | 134.8093 | 2.76 % | 11.06 % | 17.79 % | 27.72 % | 40.8 % | 50.95 % |
| 2.0 ATR | 7.196 % | 132.2457 | 0.79 % | 3.95 % | 8.6 % | 16.14 % | 27.96 % | 39.7 % |
| 2.5 ATR | 8.995 % | 129.6821 | 0.3 % | 1.97 % | 3.95 % | 9.41 % | 19.3 % | 30.05 % |
| 3.0 ATR | 10.794 % | 127.1186 | 0.1 % | 0.79 % | 1.88 % | 4.85 % | 12.24 % | 22.31 % |
| 4.0 ATR | 14.392 % | 121.9914 | 0.1 % | 0.39 % | 1.09 % | 2.28 % | 6.27 % | 12.46 % |
| 6.0 ATR | 21.588 % | 111.7371 | 0.0 % | 0.2 % | 0.4 % | 0.89 % | 2.19 % | 5.33 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.37 ATR | 0.42 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 1.05 ATR | 1.33 ATR |
| **2 s.** | 0.25 ATR | 0.53 ATR | 0.60 ATR | 0.82 ATR | 1.01 ATR | 1.17 ATR | 1.57 ATR | 1.93 ATR |
| **3 s.** | 0.30 ATR | 0.67 ATR | 0.75 ATR | 1.03 ATR | 1.25 ATR | 1.42 ATR | 1.92 ATR | 2.39 ATR |
| **5 s.** | 0.36 ATR | 0.85 ATR | 0.97 ATR | 1.33 ATR | 1.62 ATR | 1.83 ATR | 2.46 ATR | 2.98 ATR |
| **10 s.** | 0.48 ATR | 1.19 ATR | 1.35 ATR | 1.80 ATR | 2.17 ATR | 2.46 ATR | 3.38 ATR | 4.62 ATR |
| **20 s.** | 0.69 ATR | 1.54 ATR | 1.76 ATR | 2.35 ATR | 2.83 ATR | 3.23 ATR | 4.69 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.416–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.605–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.698 %, prix 138.6553), p(touche) 35.74 % (en stress 91.18 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.754–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.598 %, prix 137.3728), p(touche) 34.19 % (en stress 91.18 %)  ✅ optimum identifie (86.0 % des re-echantillons)
- **5 seance(s)** : plage utile 0.973–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.598 %, prix 137.3728), p(touche) 43.86 % (en stress 99.01 %)  ✅ optimum identifie (90.2 % des re-echantillons)
- **10 seance(s)** : plage utile 1.355–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.397 %, prix 134.8093), p(touche) 40.8 % (en stress 100.0 %)  ✅ optimum identifie (92.2 % des re-echantillons)
- **20 seance(s)** : plage utile 1.764–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.196 %, prix 132.2457), p(touche) 39.7 % (en stress 99.0 %)  ✅ optimum identifie (89.2 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.005 | EV/share : €-0.025 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 18 % | T3 5 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 18.4 | bear 76.6 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 142.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.426% → cible +1.844% / stop −1.5%, p_fill 34%, n_eff≈42.2) : P(cible|rempli) **25%** · **EV/risk -0.069** (×p_fill ; si rempli -0.30% du capital)
  - **swing** (entrée dip −5.332% → cible +4.249% / stop −3.801%, p_fill 24%, n_eff≈28.2) : P(cible|rempli) **55%** · **EV/risk +0.056** (×p_fill ; si rempli +0.89% du capital)
  - **deep** (entrée dip −8.233% → cible +6.2% / stop −5.881%, p_fill 19%, n_eff≈22.3) : P(cible|rempli) **80%** · **EV/risk +0.118** (×p_fill ; si rempli +3.60% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→64% · +2.0%→39% · +3.0%→19% · +5.0%→6% · +8.0%→1%
- Range intraday médian 3.7% (p90 6.11%) · excursion haute méd. +1.55% / basse méd. −1.72%
- Profil de vol intra : ouverture 1.963% vs midi 0.871% vs clôture 1.071% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 10% · trend ↑1%/↓0% ; spike-down 55% · recovery-V 23%)_
- **Régime intraday** : **chop** _(efficiency 0.109 ; mean-reverting — autocorr -0.038)_ ; drift intra méd. -0.291% ; recovery-V 23%
- **σ réalisé intraday** 2.179% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 73% / whipsaw 39%
- POC intraday (dernière séance, temps-au-prix) : 146.7725 (VA 144.4065–147.2795 ; dernier close 145.52)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 50% · rebond 61% · **stop −3.94%** sous le fill (sous le bruit) · cible +1.52% · R/R 0.39 (high win-rate)
- Gaps overnight (n=159) : méd. 0.39% · baisse 35% (gap-down >1% 16% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −0.51% (p90 −1.67%) · haut méd +0.45% · range méd 1.12%
- Excursion ouverture 15min (n=160) : bas méd −0.65% (p90 −2.18%) · haut méd +0.6% · range méd 1.45%
- Excursion ouverture 30min (n=160) : bas méd −0.81% (p90 −2.23%) · haut méd +0.67% · range méd 1.68%
- Excursion ouverture 60min (n=160) : bas méd −0.92% (p90 −2.53%) · haut méd +0.77% · range méd 1.74%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 145.82 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 50% · séance 69% (115/159) · gap 26% · délai 0.4min · rebond 59% (61/115) (MFE +1.2%)
   - −1.0% : fill 30min 40% · séance 63% (107/159) · gap 16% · délai 7.6min · rebond 58% (60/107) (MFE +1.36%)
   - −1.5% : fill 30min 27% · séance 50% (88/159) · gap 12% · délai 19.6min · rebond 61% (50/88) (MFE +1.52%)
   - −2.0% : fill 30min 18% · séance 40% (73/159) · gap 8% · délai 60.5min · rebond 56% (44/73) (MFE +1.2%)
   - −3.0% : fill 30min 9% · séance 23% (47/159) · gap 2% · délai 200.8min · rebond 44% (27/47) (MFE +0.88%)
   - −4.0% : fill 30min 6% · séance 15% (33/159) · gap 1% · délai 76.7min · rebond 58% (22/33) (MFE +1.12%)
   - −5.0% : fill 30min 3% · séance 12% (24/159) · gap 0% · délai 388.5min · rebond 43% (12/24) (MFE +0.87%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.48% (p90 −1.75%) → stop au-delà de −1.19% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.39% (p90 −1.49%) → stop au-delà de −0.86% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.26% (p90 −0.95%) → stop au-delà de −0.7% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=524 jambes) : jambe baissière méd −1.04% (p90 −2.34%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (53 séances) :
      · −1.0% : fill 98% (52/53) · rebond 55% (28/52)
      · −2.0% : fill 75% (39/53) · rebond 44% (20/39)
      · −3.0% : fill 45% (27/53) · rebond 33% (14/27)
      · −4.0% : fill 37% (22/53) · rebond 60% (16/22)
      · −5.0% : fill 31% (18/53) · rebond 49% (11/18)
   - **flat** (17 séances) :
      · −1.0% : fill 78% (14/17) · rebond 65% (10/14)
      · −2.0% : fill 44% (9/17) · rebond 67% (6/9)
      · −3.0% : fill 27% (6/17) · rebond 46% (3/6)
      · −4.0% : fill 9% (4/17) · rebond 52% (2/4)
      · −5.0% : fill 7% (3/17) · rebond 0% (0/3)
   - **gap-up** (89 séances) :
      · −1.0% : fill 40% (41/89) · rebond 59% (22/41)
      · −2.0% : fill 19% (25/89) · rebond 75% (18/25)
      · −3.0% : fill 10% (14/89) · rebond 73% (10/14)
      · −4.0% : fill 4% (7/89) · rebond 47% (4/7)
      · −5.0% : fill 2% (3/89) · rebond 35% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 64% si les 15 1res min sont vertes (75 cas) · 26% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:29** → P(séance verte=clôture>ouverture) 72% si début vert vs 23% si rouge (base 45% · écart 48 pts) ; prédictivité sature ensuite (plafond brut 219min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **72%** · continue >prix actuel 56% ; creux résiduel méd -1.05% (q20 -2.14%) → **SL/trailing à −2.14%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.34% / q75 +2.29% → **scale +1.34% / runner +2.29%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **23%** (continue à baisser 60%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.79%** (au-delà de la MAE q10 -3.79%), cible rebond +1.13% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.94% .. +1.72%] · haut q95 +2.43% · bas q05 -2.61%
   - 60min (n=160) : retour [-2.48% .. +1.97%] · haut q95 +2.58% · bas q05 -2.94%
   - 2h (n=160) : retour [-2.81% .. +2.38%] · haut q95 +2.77% · bas q05 -3.56%
   - 4h (n=160) : retour [-3.18% .. +2.66%] · haut q95 +3.27% · bas q05 -4.06%
   - 6h (n=160) : retour [-3.72% .. +3.48%] · haut q95 +4.29% · bas q05 -4.6%
   - session (n=160) : retour [-4.9% .. +3.16%] · haut q95 +4.79% · bas q05 -6.19%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — ENR = **plat / peu volatil** (vol intra méd 2.43%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.56 · part idiosyncratique 0.44
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 51.8  _(neutre)_
- **ADX** : 9.5  _(pas de tendance nette)_
- **MACD** : hist 0.678  _(pas de croisement recent)_
- **BB** : %B 0.5 · largeur 12.3%
- **ATR** : 5.13 (28.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.172  _(distribution)_
- **Vol ratio** : 0.43  _(volume atone)_
- **Choppiness** : 55.1  _(transition)_
- **MA** : MA20 142.59 · MA50 147.54 · MA200 153.01  _(prix < MA20)_
- **Dist MA** : MA20 -0.1% · MA50 -3.4% · MA200 -6.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (849360 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
