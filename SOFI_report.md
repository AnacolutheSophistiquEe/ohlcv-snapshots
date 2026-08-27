# SOFI

**Generated** : 2026-08-27T00:37:16.807432+00:00  
**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $18.84  

> 🟡 **WAIT-FOR-DIP** — spot +3.7 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $18.84 (+3.7% vs entrée) · entrée $18.16 · stop $17.61 · T1 $19.25 · R/R 1.98  
> ↳ P(T1 av. stop) 27 % · EV/risk 0.219 · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $18.08–$18.23 (mid $18.16)
- Spot actuel : $18.84 (+3.7% au-dessus de la zone — repli à attendre)
- Stop : $17.61 (stop swing_plan-based (-12.03%))
- Targets : T1 $19.25 · R/R 1.98 | T2 $19.26 · R/R 2.0 | T3 $19.28 · R/R 2.04
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $17.61


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=5.99 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.03 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1253).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 12.03 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.268 % | p01 -6.52 % | pire -11.105 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2892** [0.2256 ; 0.3598] _(largeur 13.4 pt, n_eff 173.1)_
   - swing : **0.4789** [0.4266 ; 0.5316] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4516** [0.3997 ; 0.5043] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_target_first, p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 8.3 observations effectives », dont la borne haute a 95 % vaut environ 36.2 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (25.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 960 séances)** : VaR **-5.82 %** | CVaR **-8.4 %** | vol 3.84 %/j
   - _fenêtre arrêtée : rupture de regime a 1020 seances en arriere (volatilite 5.58 % contre 3.47 % aujourd'hui, rapport 1.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.5 % vs -14.19 % si l'on extrapolait par √5 _(rapport 1.021 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8277** (β de hausse 1.7104, asymétrie 1.0686) vs IWM — 602 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.278× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 16.7461 sur atr_grid (2.75 ATR, 11.114 %) — p(stop avant cible) 0.3087 [0.26 ; 0.36], R/R 3.044, perte reelle 11.114 % (gap inclus), CVaR 11.114 %, EV -0.1675 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 6.062 %) — p(stop avant cible) 0.5572 [0.50 ; 0.61], R/R 4.319, perte reelle 7.833 % (gap inclus), EV -0.8928 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 4.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.557, borne haute 0.609 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.89 %) : P(cible) 0.6 % x 33.83 % + P(rien) 43.7 % x 7.51 % ne couvrent pas P(stop) 55.7 % x 7.83 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.78 ATR (stop 8.948 %) — p(stop avant cible) 0.4007 [0.35 ; 0.45], R/R 3.413, perte reelle 9.913 % (gap inclus), EV -0.5447 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.54 %) : P(cible) 0.6 % x 33.83 % + P(rien) 59.4 % x 5.45 % ne couvrent pas P(stop) 40.1 % x 9.91 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 3.7 ATR (stop 16.705 %) — p(stop avant cible) 0.0855 [0.06 ; 0.12], R/R 2.025, perte reelle 16.705 % (gap inclus), EV 0.5665 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.70 % > budget 12.00 %
   - 🟢 support a 5.2 ATR (stop 22.789 %) — p(stop avant cible) 0.034 [0.02 ; 0.06], R/R 1.484, perte reelle 22.789 % (gap inclus), EV 0.479 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.79 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.01 %) — p(stop avant cible) 0.929 [0.90 ; 0.95], R/R 13.636, perte reelle 2.481 % (gap inclus), EV -1.3229 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 13.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.929, borne haute 0.953 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.32 %) : P(cible) 0.2 % x 33.83 % + P(rien) 6.9 % x 13.37 % ne couvrent pas P(stop) 92.9 % x 2.48 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.021 %) — p(stop avant cible) 0.8769 [0.84 ; 0.91], R/R 9.309, perte reelle 3.634 % (gap inclus), EV -1.5816 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 9.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.877, borne haute 0.908 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.58 %) : P(cible) 0.3 % x 33.83 % + P(rien) 12.0 % x 12.45 % ne couvrent pas P(stop) 87.7 % x 3.63 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 3.031 %) — p(stop avant cible) 0.8067 [0.76 ; 0.85], R/R 6.931, perte reelle 4.881 % (gap inclus), EV -1.8223 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 6.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.807, borne haute 0.846 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.82 %) : P(cible) 0.4 % x 33.83 % + P(rien) 18.9 % x 10.41 % ne couvrent pas P(stop) 80.7 % x 4.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 4.042 %) — p(stop avant cible) 0.6933 [0.64 ; 0.74], R/R 5.454, perte reelle 6.203 % (gap inclus), EV -1.3479 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 5.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.693, borne haute 0.740 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.35 %) : P(cible) 0.5 % x 33.83 % + P(rien) 30.1 % x 9.19 % ne couvrent pas P(stop) 69.3 % x 6.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 5.052 %) — p(stop avant cible) 0.6197 [0.57 ; 0.67], R/R 4.665, perte reelle 7.252 % (gap inclus), EV -1.1442 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.620, borne haute 0.670 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.14 %) : P(cible) 0.5 % x 33.83 % + P(rien) 37.5 % x 8.44 % ne couvrent pas P(stop) 62.0 % x 7.25 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.78 ATR (stop 8.39 %) — p(stop avant cible) 0.4173 [0.37 ; 0.47], R/R 3.485, perte reelle 9.707 % (gap inclus), EV -0.5613 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.56 %) : P(cible) 0.6 % x 33.83 % + P(rien) 57.7 % x 5.72 % ne couvrent pas P(stop) 41.7 % x 9.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 10.104 %) — p(stop avant cible) 0.3595 [0.31 ; 0.41], R/R 3.046, perte reelle 11.105 % (gap inclus), EV -0.6284 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.63 %) : P(cible) 0.6 % x 33.83 % + P(rien) 63.4 % x 4.98 % ne couvrent pas P(stop) 35.9 % x 11.10 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 11.114 %) — p(stop avant cible) 0.3087 [0.26 ; 0.36], R/R 3.044, perte reelle 11.114 % (gap inclus), EV -0.1675 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 0.6 % x 33.83 % + P(rien) 68.5 % x 4.47 % ne couvrent pas P(stop) 30.9 % x 11.11 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 12.125 %) — p(stop avant cible) 0.2653 [0.22 ; 0.31], R/R 2.79, perte reelle 12.125 % (gap inclus), EV -0.0308 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.12 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 0.6 % x 33.83 % + P(rien) 72.9 % x 4.09 % ne couvrent pas P(stop) 26.5 % x 12.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 3.7 ATR (stop 16.148 %) — p(stop avant cible) 0.0995 [0.07 ; 0.13], R/R 2.095, perte reelle 16.148 % (gap inclus), EV 0.5434 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.15 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 18.187 %) — p(stop avant cible) 0.0677 [0.04 ; 0.10], R/R 1.86, perte reelle 18.187 % (gap inclus), EV 0.5413 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.19 % > budget 12.00 %
   - 🟢 grid_snapped a 5.2 ATR (stop 22.232 %) — p(stop avant cible) 0.0371 [0.02 ; 0.06], R/R 1.522, perte reelle 22.232 % (gap inclus), EV 0.4698 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.23 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 24.249 %) — p(stop avant cible) 0.0253 [0.01 ; 0.05], R/R 1.395, perte reelle 24.249 % (gap inclus), EV 0.4972 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.25 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 26.27 %) — p(stop avant cible) 0.0056 [0.00 ; 0.02], R/R 1.288, perte reelle 26.27 % (gap inclus), EV 0.6263 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.27 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 28.291 %) — p(stop avant cible) 0.0041 [0.00 ; 0.02], R/R 1.196, perte reelle 28.291 % (gap inclus), EV 0.6273 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.29 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 30.312 %) — p(stop avant cible) 0.0032 [0.00 ; 0.01], R/R 1.116, perte reelle 30.312 % (gap inclus), EV 0.6339 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.31 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 32.332 %) — p(stop avant cible) 0.0024 [0.00 ; 0.01], R/R 1.046, perte reelle 32.332 % (gap inclus), EV 0.6454 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.33 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 18.84, ATR14 0.7614 (4.042 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.375 ATR = 1.516 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.202 % | 18.8019 | 92.85 % | 95.77 % | 96.97 % | 97.37 % | 98.27 % | 98.87 % |
| 0.1 ATR | 0.404 % | 18.7639 | 85.1 % | 89.52 % | 91.93 % | 93.23 % | 95.53 % | 97.33 % |
| 0.15 ATR | 0.606 % | 18.7258 | 79.05 % | 84.98 % | 88.19 % | 90.39 % | 92.78 % | 94.97 % |
| 0.2 ATR | 0.808 % | 18.6877 | 71.4 % | 79.64 % | 83.55 % | 86.96 % | 90.45 % | 93.43 % |
| 0.25 ATR | 1.01 % | 18.6496 | 66.16 % | 75.1 % | 80.12 % | 84.23 % | 88.82 % | 91.99 % |
| 0.35 ATR | 1.415 % | 18.5735 | 52.47 % | 65.42 % | 72.25 % | 78.36 % | 85.26 % | 88.71 % |
| 0.5 ATR | 2.021 % | 18.4593 | 37.56 % | 53.43 % | 61.65 % | 69.06 % | 79.27 % | 84.5 % |
| 0.75 ATR | 3.031 % | 18.2689 | 20.14 % | 36.69 % | 46.82 % | 56.83 % | 69.82 % | 77.72 % |
| 1.0 ATR | 4.042 % | 18.0786 | 8.76 % | 24.29 % | 33.8 % | 44.99 % | 59.55 % | 68.99 % |
| 1.25 ATR | 5.052 % | 17.8882 | 4.03 % | 14.92 % | 23.61 % | 35.39 % | 50.3 % | 62.32 % |
| 1.5 ATR | 6.062 % | 17.6979 | 2.01 % | 9.48 % | 16.65 % | 27.4 % | 42.28 % | 55.75 % |
| 2.0 ATR | 8.083 % | 17.3171 | 0.7 % | 4.33 % | 8.27 % | 15.27 % | 29.47 % | 45.48 % |
| 2.5 ATR | 10.104 % | 16.9364 | 0.3 % | 1.92 % | 3.73 % | 9.4 % | 20.02 % | 36.14 % |
| 3.0 ATR | 12.125 % | 16.5557 | 0.1 % | 0.91 % | 2.83 % | 6.07 % | 14.33 % | 28.75 % |
| 4.0 ATR | 16.166 % | 15.7943 | 0.0 % | 0.3 % | 0.71 % | 2.53 % | 7.52 % | 14.99 % |
| 6.0 ATR | 24.249 % | 14.2714 | 0.0 % | 0.1 % | 0.2 % | 0.2 % | 0.91 % | 3.08 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.42 ATR | 0.56 ATR | 0.68 ATR | 0.75 ATR | 0.97 ATR | 1.20 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.63 ATR | 0.82 ATR | 0.99 ATR | 1.11 ATR | 1.48 ATR | 1.94 ATR |
| **3 s.** | 0.32 ATR | 0.70 ATR | 0.79 ATR | 1.02 ATR | 1.22 ATR | 1.38 ATR | 1.90 ATR | 2.36 ATR |
| **5 s.** | 0.40 ATR | 0.89 ATR | 1.00 ATR | 1.32 ATR | 1.60 ATR | 1.80 ATR | 2.45 ATR | 3.30 ATR |
| **10 s.** | 0.61 ATR | 1.26 ATR | 1.42 ATR | 1.86 ATR | 2.24 ATR | 2.50 ATR | 3.64 ATR | 4.76 ATR |
| **20 s.** | 0.83 ATR | 1.78 ATR | 2.03 ATR | 2.71 ATR | 3.27 ATR | 3.64 ATR | 4.84 ATR | 5.68 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.425–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.021 %, prix 18.4592), p(touche) 37.56 % (en stress 83.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.626–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.031 %, prix 18.269), p(touche) 36.69 % (en stress 91.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 18.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.785–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.042 %, prix 18.0785), p(touche) 33.8 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.0–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.042 %, prix 18.0785), p(touche) 44.99 % (en stress 97.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.415–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (6.062 %, prix 17.6979), p(touche) 42.28 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.026–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (10.104 %, prix 16.9364), p(touche) 36.14 % (en stress 98.98 %)  ✅ optimum identifie (69.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.081 | EV/share : $-0.044 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 12 % | T2 12 % | T3 12 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 78.7 | bear 11.5 | side 9.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 509.0 (= 27 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.629% → cible +6.0% / stop −3.0%, p_fill 20%, n_eff≈8.3) : P(cible|rempli) **0%** · **EV/risk +0.026** (×p_fill ; si rempli +0.39% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=4, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→69% · +2.0%→48% · +3.0%→36% · +5.0%→12% · +8.0%→1%
- Range intraday médian 4.32% (p90 7.29%) · excursion haute méd. +1.84% / basse méd. −2.18%
- Profil de vol intra : ouverture 3.005% vs midi 0.875% vs clôture 0.988% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 15% · trend ↑2%/↓0% ; spike-down 64% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.146 ; mean-reverting — autocorr -0.036)_ ; drift intra méd. 0.051% ; recovery-V 17%
- **σ réalisé intraday** 2.738% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 61% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 18.9512 (VA 18.8717–18.9778 ; dernier close 18.9)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 46% · rebond 69% · **stop −2.96%** sous le fill (sous le bruit) · cible +1.82% · R/R 0.61 (high win-rate)
- Gaps overnight (n=159) : méd. 0.38% · baisse 42% (gap-down >1% 23% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −1.7%) · haut méd +0.69% · range méd 1.59%
- Excursion ouverture 15min (n=160) : bas méd −0.99% (p90 −2.94%) · haut méd +0.96% · range méd 2.24%
- Excursion ouverture 30min (n=160) : bas méd −1.08% (p90 −3.21%) · haut méd +1.13% · range méd 2.71%
- Excursion ouverture 60min (n=160) : bas méd −1.38% (p90 −3.78%) · haut méd +1.25% · range méd 3.33%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 18.91 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 71% (119/159) · gap 29% · délai 0.0min · rebond 53% (64/119) (MFE +1.2%)
   - −1.0% : fill 30min 51% · séance 63% (109/159) · gap 23% · délai 1.5min · rebond 59% (65/109) (MFE +1.18%)
   - −1.5% : fill 30min 41% · séance 60% (100/159) · gap 19% · délai 10.2min · rebond 68% (66/100) (MFE +1.51%)
   - −2.0% : fill 30min 33% · séance 46% (78/159) · gap 11% · délai 9.7min · rebond 69% (54/78) (MFE +1.82%)
   - −3.0% : fill 30min 14% · séance 33% (56/159) · gap 3% · délai 35.5min · rebond 64% (39/56) (MFE +1.37%)
   - −4.0% : fill 30min 9% · séance 17% (35/159) · gap 3% · délai 26.0min · rebond 65% (24/35) (MFE +1.93%)
   - −5.0% : fill 30min 4% · séance 8% (18/159) · gap 2% · délai 46.1min · rebond 41% (9/18) (MFE +0.71%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.43% (p90 −1.72%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.47% (p90 −1.63%) → stop au-delà de −1.22% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.42% (p90 −1.51%) → stop au-delà de −1.12% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=669 jambes) : jambe baissière méd −1.08% (p90 −2.78%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (65 séances) :
      · −1.0% : fill 98% (64/65) · rebond 63% (40/64)
      · −2.0% : fill 83% (54/65) · rebond 72% (38/54)
      · −3.0% : fill 66% (42/65) · rebond 67% (30/42)
      · −4.0% : fill 38% (28/65) · rebond 70% (21/28)
      · −5.0% : fill 20% (15/65) · rebond 40% (8/15)
   - **flat** (20 séances) :
      · −1.0% : fill 56% (11/20) · rebond 38% (5/11)
      · −2.0% : fill 43% (7/20) · rebond 77% (5/7)
      · −3.0% : fill 29% (5/20) · rebond 59% (3/5)
      · −4.0% : fill 12% (2/20) · rebond 72% (1/2)
      · −5.0% : fill 0% (0/20) · rebond 0% (0/0)
   - **gap-up** (74 séances) :
      · −1.0% : fill 42% (34/74) · rebond 59% (20/34)
      · −2.0% : fill 22% (17/74) · rebond 58% (11/17)
      · −3.0% : fill 11% (9/74) · rebond 60% (6/9)
      · −4.0% : fill 4% (5/74) · rebond 22% (2/5)
      · −5.0% : fill 1% (3/74) · rebond 44% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 41% en base · 61% si les 15 1res min sont vertes (72 cas) · 25% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 78% si début vert vs 10% si rouge (base 41% · écart 69 pts) ; prédictivité sature ensuite (plafond brut 228min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **78%** · continue >prix actuel 54% ; creux résiduel méd -1.53% (q20 -2.61%) → **SL/trailing à −2.61%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.9% / q75 +2.85% → **scale +1.9% / runner +2.85%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **10%** (continue à baisser 60%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.11%** (au-delà de la MAE q10 -3.11%), cible rebond +1.11% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.94% .. +3.87%] · haut q95 +4.11% · bas q05 -3.5%
   - 60min (n=160) : retour [-3.2% .. +3.99%] · haut q95 +4.6% · bas q05 -4.02%
   - 2h (n=160) : retour [-3.7% .. +4.13%] · haut q95 +5.43% · bas q05 -4.97%
   - 4h (n=160) : retour [-4.01% .. +4.63%] · haut q95 +5.69% · bas q05 -5.08%
   - 6h (n=160) : retour [-4.64% .. +4.14%] · haut q95 +5.74% · bas q05 -5.12%
   - session (n=160) : retour [-4.56% .. +5.24%] · haut q95 +5.78% · bas q05 -5.37%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.89%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.25/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 56.3  _(momentum haussier)_
- **ADX** : 15.9  _(pas de tendance nette)_
- **MACD** : hist 0.075  _(pas de croisement recent)_
- **BB** : %B 0.76 · largeur 15.1%
- **ATR** : 0.76 (6.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.075  _(accumulation)_
- **Vol ratio** : 0.71  _(volume normal)_
- **Choppiness** : 70.0  _(marche en range (choppy))_
- **MA** : MA20 18.12 · MA50 17.79 · MA200 20.36  _(prix > MA20)_
- **Dist MA** : MA20 +4.0% · MA50 +5.9% · MA200 -7.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (807975 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
