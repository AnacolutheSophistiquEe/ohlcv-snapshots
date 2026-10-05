# SOFI

**Generated** : 2026-10-05T00:33:31.237947+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $15.77  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $15.77 (+1.0% vs entrée) · entrée $15.61 · stop $14.36 · T1 $15.91 · R/R 0.24  
> ↳ P(T1 av. stop) 35 % _(réel 5 s)_ · EV/risk -0.034 _(réel 5 s)_ · _probas brutes, non calibrées · n=0_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $15.58–$15.64 (mid $15.61)
- Spot actuel : $15.77 (+1.0% au-dessus de la zone — repli à attendre)
- Stop : $14.36 (plancher anti-bruit 5 s — stop EV-optimal −8% (first-passage 5 s réel) ; -8.01 % depuis l'entree)
- Targets : T1 $15.91 · R/R 0.24 | T2 $16.20 · R/R 0.47 | T3 $16.50 · R/R 0.71
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $14.36


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=5.82 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (6.03 %)** : le gap seul le franchit 1.356 % des séances (17 fois sur 1254).
   - exécution **1.377 pt plus bas** dans le cas TYPIQUE (médiane), 3.779 au p90, **5.075 au pire**
   - perte réelle **7.833 %** en moyenne _(tirée par la queue)_, jusqu'à **11.105 %** — au lieu des 6.03 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0244 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.204 % | p01 -6.517 % | pire -11.105 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0122** [0.0027 ; 0.0376] _(largeur 3.5 pt, n_eff 173.1)_
   - swing : **0.5556** [0.5029 ; 0.6073] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.5122** [0.4596 ; 0.5646] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 78.9 observations effectives », dont la borne haute a 95 % vaut environ 3.8 %.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.29 %** | CVaR **-8.7 %** | vol 4.13 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.5 % vs -14.19 % si l'on extrapolait par √5 _(rapport 1.022 ; < 1 = le √5 surestime)_
- **β de baisse : 1.833** (β de hausse 1.7132, asymétrie 1.0699) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.359× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 14.5458 sur support (1.5 ATR, 7.763 %) — p(stop avant cible) 0.4468 [0.40 ; 0.50], R/R 7.515, perte reelle 8.138 % (gap inclus), CVaR 10.806 %, EV -0.8194 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 1.19 ATR (stop 6.596 %) — p(stop avant cible) 0.5224 [0.47 ; 0.57], R/R 8.897, perte reelle 6.874 % (gap inclus), EV -0.6628 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 8.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.522, borne haute 0.575 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.66 %) : P(cible) 0.0 % x 61.16 % + P(rien) 47.8 % x 6.13 % ne couvrent pas P(stop) 52.2 % x 6.87 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🟢 support a 1.5 ATR (stop 7.763 %) — p(stop avant cible) 0.4468 [0.40 ; 0.50], R/R 7.515, perte reelle 8.138 % (gap inclus), EV -0.8194 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.82 %) : P(cible) 0.0 % x 61.16 % + P(rien) 55.3 % x 5.09 % ne couvrent pas P(stop) 44.7 % x 8.14 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.25 ATR (stop 0.943 %) — p(stop avant cible) 0.9401 [0.91 ; 0.96], R/R 60.277, perte reelle 1.015 % (gap inclus), EV -0.1425 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 60.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.940, borne haute 0.962 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 0.0 % x 61.16 % + P(rien) 6.0 % x 13.54 % ne couvrent pas P(stop) 94.0 % x 1.01 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.5 ATR (stop 1.885 %) — p(stop avant cible) 0.9001 [0.87 ; 0.93], R/R 29.296, perte reelle 2.087 % (gap inclus), EV -0.5719 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 29.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.900, borne haute 0.928 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.57 %) : P(cible) 0.0 % x 61.16 % + P(rien) 10.0 % x 13.10 % ne couvrent pas P(stop) 90.0 % x 2.09 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.75 ATR (stop 2.828 %) — p(stop avant cible) 0.8394 [0.80 ; 0.88], R/R 20.025, perte reelle 3.054 % (gap inclus), EV -0.893 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 20.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.839, borne haute 0.875 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.89 %) : P(cible) 0.0 % x 61.16 % + P(rien) 16.1 % x 10.41 % ne couvrent pas P(stop) 83.9 % x 3.05 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ grid_snapped a 1.19 ATR (stop 5.608 %) — p(stop avant cible) 0.6013 [0.55 ; 0.65], R/R 10.205, perte reelle 5.993 % (gap inclus), EV -0.7485 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 10.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.601, borne haute 0.652 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.75 %) : P(cible) 0.0 % x 61.16 % + P(rien) 39.9 % x 7.16 % ne couvrent pas P(stop) 60.1 % x 5.99 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.25 ATR (stop 8.484 %) — p(stop avant cible) 0.4063 [0.36 ; 0.46], R/R 6.887, perte reelle 8.88 % (gap inclus), EV -0.8588 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.86 %) : P(cible) 0.0 % x 61.16 % + P(rien) 59.4 % x 4.63 % ne couvrent pas P(stop) 40.6 % x 8.88 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.5 ATR (stop 9.427 %) — p(stop avant cible) 0.3577 [0.31 ; 0.41], R/R 6.16, perte reelle 9.928 % (gap inclus), EV -1.0533 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.62 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.05 %) : P(cible) 0.0 % x 61.16 % + P(rien) 64.2 % x 3.89 % ne couvrent pas P(stop) 35.8 % x 9.93 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.75 ATR (stop 10.369 %) — p(stop avant cible) 0.3059 [0.26 ; 0.36], R/R 5.658, perte reelle 10.809 % (gap inclus), EV -0.9218 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.92 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.92 %) : P(cible) 0.0 % x 61.16 % + P(rien) 69.4 % x 3.44 % ne couvrent pas P(stop) 30.6 % x 10.81 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 3.0 ATR (stop 11.312 %) — p(stop avant cible) 0.262 [0.22 ; 0.31], R/R 5.238, perte reelle 11.676 % (gap inclus), EV -0.808 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.81 %) : P(cible) 0.0 % x 61.16 % + P(rien) 73.8 % x 3.05 % ne couvrent pas P(stop) 26.2 % x 11.68 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 3.5 ATR (stop 13.198 %) — p(stop avant cible) 0.1772 [0.14 ; 0.22], R/R 4.537, perte reelle 13.48 % (gap inclus), EV -0.4025 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.40 %) : P(cible) 0.0 % x 61.16 % + P(rien) 82.3 % x 2.41 % ne couvrent pas P(stop) 17.7 % x 13.48 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 4.0 ATR (stop 15.083 %) — p(stop avant cible) 0.1178 [0.09 ; 0.15], R/R 4.014, perte reelle 15.236 % (gap inclus), EV -0.2506 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 15.44 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.25 %) : P(cible) 0.0 % x 61.16 % + P(rien) 88.2 % x 1.75 % ne couvrent pas P(stop) 11.8 % x 15.24 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 4.5 ATR (stop 16.968 %) — p(stop avant cible) 0.073 [0.05 ; 0.10], R/R 3.577, perte reelle 17.096 % (gap inclus), EV -0.1525 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 17.15 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 0.0 % x 61.16 % + P(rien) 92.7 % x 1.18 % ne couvrent pas P(stop) 7.3 % x 17.10 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 5.0 ATR (stop 18.854 %) — p(stop avant cible) 0.0551 [0.03 ; 0.08], R/R 3.235, perte reelle 18.907 % (gap inclus), EV -0.1609 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 18.91 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 0.0 % x 61.16 % + P(rien) 94.5 % x 0.93 % ne couvrent pas P(stop) 5.5 % x 18.91 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 5.5 ATR (stop 20.739 %) — p(stop avant cible) 0.0402 [0.02 ; 0.06], R/R 2.931, perte reelle 20.864 % (gap inclus), EV -0.1866 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.09 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.19 %) : P(cible) 0.0 % x 61.16 % + P(rien) 96.0 % x 0.68 % ne couvrent pas P(stop) 4.0 % x 20.86 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 6.0 ATR (stop 22.624 %) — p(stop avant cible) 0.0293 [0.02 ; 0.05], R/R 2.685, perte reelle 22.774 % (gap inclus), EV -0.2062 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.73 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.21 %) : P(cible) 0.0 % x 61.16 % + P(rien) 97.1 % x 0.47 % ne couvrent pas P(stop) 2.9 % x 22.77 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 6.5 ATR (stop 24.51 %) — p(stop avant cible) 0.0217 [0.01 ; 0.04], R/R 2.478, perte reelle 24.679 % (gap inclus), EV -0.1995 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.89 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 0.0 % x 61.16 % + P(rien) 97.8 % x 0.34 % ne couvrent pas P(stop) 2.2 % x 24.68 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 7.0 ATR (stop 26.395 %) — p(stop avant cible) 0.0042 [0.00 ; 0.02], R/R 2.288, perte reelle 26.728 % (gap inclus), EV -0.0765 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.05 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.08 %) : P(cible) 0.0 % x 61.16 % + P(rien) 99.6 % x 0.04 % ne couvrent pas P(stop) 0.4 % x 26.73 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 7.5 ATR (stop 28.28 %) — p(stop avant cible) 0.0035 [0.00 ; 0.01], R/R 2.161, perte reelle 28.298 % (gap inclus), EV -0.0774 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.10 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.08 %) : P(cible) 0.0 % x 61.16 % + P(rien) 99.6 % x 0.02 % ne couvrent pas P(stop) 0.4 % x 28.30 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 8.0 ATR (stop 30.166 %) — p(stop avant cible) 0.0027 [0.00 ; 0.01], R/R 2.018, perte reelle 30.3 % (gap inclus), EV -0.0708 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.01 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.07 %) : P(cible) 0.0 % x 61.16 % + P(rien) 99.7 % x 0.01 % ne couvrent pas P(stop) 0.3 % x 30.30 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.2 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 15.77, ATR14 0.5946 (3.771 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.378 ATR = 1.425 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.189 % | 15.7403 | 92.86 % | 95.77 % | 97.08 % | 97.47 % | 98.27 % | 98.87 % |
| 0.1 ATR | 0.377 % | 15.7105 | 85.21 % | 89.43 % | 92.04 % | 93.33 % | 95.53 % | 97.13 % |
| 0.15 ATR | 0.566 % | 15.6808 | 78.97 % | 84.69 % | 88.0 % | 90.4 % | 92.89 % | 94.87 % |
| 0.2 ATR | 0.754 % | 15.6511 | 71.73 % | 79.46 % | 83.37 % | 86.87 % | 90.56 % | 93.33 % |
| 0.25 ATR | 0.943 % | 15.6213 | 66.4 % | 75.03 % | 80.04 % | 84.24 % | 89.04 % | 92.0 % |
| 0.35 ATR | 1.32 % | 15.5619 | 52.82 % | 65.26 % | 71.98 % | 78.38 % | 85.48 % | 88.72 % |
| 0.5 ATR | 1.885 % | 15.4727 | 37.63 % | 53.27 % | 61.59 % | 69.19 % | 79.49 % | 84.62 % |
| 0.75 ATR | 2.828 % | 15.324 | 20.62 % | 36.96 % | 47.08 % | 57.17 % | 69.95 % | 78.05 % |
| 1.0 ATR | 3.771 % | 15.1754 | 8.85 % | 24.57 % | 33.97 % | 45.15 % | 59.7 % | 69.44 % |
| 1.25 ATR | 4.713 % | 15.0267 | 4.23 % | 15.11 % | 23.99 % | 35.56 % | 50.46 % | 62.77 % |
| 1.5 ATR | 5.656 % | 14.878 | 2.01 % | 9.47 % | 16.63 % | 27.37 % | 42.64 % | 56.41 % |
| 2.0 ATR | 7.541 % | 14.5807 | 0.7 % | 4.43 % | 8.37 % | 15.25 % | 29.24 % | 45.44 % |
| 2.5 ATR | 9.427 % | 14.2834 | 0.3 % | 1.91 % | 3.93 % | 9.49 % | 19.49 % | 35.69 % |
| 3.0 ATR | 11.312 % | 13.9861 | 0.1 % | 0.91 % | 2.82 % | 6.16 % | 13.6 % | 28.21 % |
| 4.0 ATR | 15.083 % | 13.3914 | 0.0 % | 0.3 % | 0.71 % | 2.53 % | 7.41 % | 14.67 % |
| 6.0 ATR | 22.624 % | 12.2021 | 0.0 % | 0.1 % | 0.2 % | 0.2 % | 0.91 % | 3.08 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.69 ATR | 0.76 ATR | 0.98 ATR | 1.21 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.63 ATR | 0.83 ATR | 0.99 ATR | 1.12 ATR | 1.48 ATR | 1.94 ATR |
| **3 s.** | 0.31 ATR | 0.70 ATR | 0.79 ATR | 1.02 ATR | 1.23 ATR | 1.39 ATR | 1.90 ATR | 2.38 ATR |
| **5 s.** | 0.41 ATR | 0.90 ATR | 1.00 ATR | 1.33 ATR | 1.60 ATR | 1.80 ATR | 2.46 ATR | 3.32 ATR |
| **10 s.** | 0.62 ATR | 1.26 ATR | 1.43 ATR | 1.86 ATR | 2.22 ATR | 2.47 ATR | 3.58 ATR | 4.74 ATR |
| **20 s.** | 0.84 ATR | 1.79 ATR | 2.02 ATR | 2.68 ATR | 3.24 ATR | 3.61 ATR | 4.81 ATR | 5.67 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.427–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.885 %, prix 15.4727), p(touche) 37.63 % (en stress 84.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.627–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.828 %, prix 15.324), p(touche) 36.96 % (en stress 91.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 18.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.79–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.771 %, prix 15.1753), p(touche) 33.97 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 19.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.004–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.713 %, prix 15.0268), p(touche) 35.56 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.425–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.656 %, prix 14.878), p(touche) 42.64 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.023–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (9.427 %, prix 14.2834), p(touche) 35.69 % (en stress 98.98 %)  ✅ optimum identifie (74.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 13.3 | bear 6.5 | side 80.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.022% → cible +1.905% / stop −8.0%, p_fill 75%, n_eff≈78.9) : P(cible|rempli) **35%** · **EV/risk -0.034** (×p_fill ; si rempli -0.36% du capital)
  - **swing** (entrée dip −2.26% → cible +4.313% / stop −3.857%, p_fill 61%, n_eff≈71.2) : P(cible|rempli) **43%** · **EV/risk +0.013** (×p_fill ; si rempli +0.08% du capital)
  - **deep** (entrée dip −3.484% → cible +6.177% / stop −5.861%, p_fill 62%, n_eff≈69.4) : P(cible|rempli) **48%** · **EV/risk +0.032** (×p_fill ; si rempli +0.30% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→64% · +2.0%→42% · +3.0%→30% · +5.0%→10% · +8.0%→1%
- Range intraday médian 4.06% (p90 6.61%) · excursion haute méd. +1.52% / basse méd. −2.06%
- Profil de vol intra : ouverture 2.849% vs midi 0.819% vs clôture 0.934% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 20% · trend ↑1%/↓0% ; spike-down 62% · recovery-V 23%)_
- **Régime intraday** : **chop** _(efficiency 0.153 ; neutre — autocorr -0.023)_ ; drift intra méd. -0.686% ; recovery-V 22%
- **σ réalisé intraday** 2.273% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 64% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 15.8262 (VA 15.8138–15.9262 ; dernier close 15.75)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 15% · rebond 61% · **stop −2.1%** sous le fill (sous le bruit) · cible +1.97% · R/R 0.94 (high win-rate)
- Gaps overnight (n=159) : méd. 0.17% · baisse 43% (gap-down >1% 22% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −1.59%) · haut méd +0.65% · range méd 1.42%
- Excursion ouverture 15min (n=160) : bas méd −1.01% (p90 −2.37%) · haut méd +0.79% · range méd 2.05%
- Excursion ouverture 30min (n=160) : bas méd −1.09% (p90 −3.24%) · haut méd +0.86% · range méd 2.37%
- Excursion ouverture 60min (n=160) : bas méd −1.22% (p90 −3.59%) · haut méd +0.99% · range méd 2.76%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 15.77 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 76% (120/159) · gap 30% · délai 0.1min · rebond 56% (69/120) (MFE +1.22%)
   - −1.0% : fill 30min 49% · séance 63% (105/159) · gap 22% · délai 1.5min · rebond 49% (57/105) (MFE +0.93%)
   - −1.5% : fill 30min 41% · séance 55% (94/159) · gap 19% · délai 6.8min · rebond 59% (61/94) (MFE +1.3%)
   - −2.0% : fill 30min 30% · séance 43% (73/159) · gap 8% · délai 9.8min · rebond 63% (50/73) (MFE +1.47%)
   - −3.0% : fill 30min 7% · séance 30% (52/159) · gap 2% · délai 78.7min · rebond 49% (32/52) (MFE +1.02%)
   - −4.0% : fill 30min 5% · séance 15% (30/159) · gap 1% · délai 86.8min · rebond 61% (19/30) (MFE +1.97%)
   - −5.0% : fill 30min 2% · séance 7% (15/159) · gap 1% · délai 208.5min · rebond 44% (8/15) (MFE +0.67%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.48% (p90 −1.78%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.49% (p90 −1.87%) → stop au-delà de −1.42% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −1.43%) → stop au-delà de −1.11% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=612 jambes) : jambe baissière méd −1.0% (p90 −2.74%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (64 séances) :
      · −1.0% : fill 98% (63/64) · rebond 49% (35/63)
      · −2.0% : fill 85% (54/64) · rebond 68% (37/54)
      · −3.0% : fill 59% (39/64) · rebond 49% (25/39)
      · −4.0% : fill 35% (25/64) · rebond 69% (17/25)
      · −5.0% : fill 15% (13/64) · rebond 52% (7/13)
   - **flat** (24 séances) :
      · −1.0% : fill 76% (16/24) · rebond 31% (6/16)
      · −2.0% : fill 39% (8/24) · rebond 53% (5/8)
      · −3.0% : fill 33% (7/24) · rebond 44% (3/7)
      · −4.0% : fill 11% (3/24) · rebond 30% (1/3)
      · −5.0% : fill 7% (1/24) · rebond 0% (0/1)
   - **gap-up** (71 séances) :
      · −1.0% : fill 32% (26/71) · rebond 65% (16/26)
      · −2.0% : fill 13% (11/71) · rebond 56% (8/11)
      · −3.0% : fill 7% (6/71) · rebond 60% (4/6)
      · −4.0% : fill 2% (2/71) · rebond 20% (1/2)
      · −5.0% : fill 0% (1/71) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 39% en base · 65% si les 15 1res min sont vertes (72 cas) · 22% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **36min** → P(séance verte=clôture>ouverture) 71% si début vert vs 19% si rouge (base 39% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 230min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **71%** · continue >prix actuel 51% ; creux résiduel méd -1.51% (q20 -2.67%) → **SL/trailing à −2.67%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.8% / q75 +2.64% → **scale +1.8% / runner +2.64%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **19%** (continue à baisser 63%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.79%** (au-delà de la MAE q10 -2.79%), cible rebond +1.12% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.96% .. +3.18%] · haut q95 +3.88% · bas q05 -3.58%
   - 60min (n=160) : retour [-3.13% .. +3.65%] · haut q95 +4.44% · bas q05 -3.99%
   - 2h (n=160) : retour [-3.52% .. +3.76%] · haut q95 +4.95% · bas q05 -4.15%
   - 4h (n=160) : retour [-3.89% .. +4.27%] · haut q95 +5.43% · bas q05 -5.08%
   - 6h (n=160) : retour [-4.24% .. +4.07%] · haut q95 +5.44% · bas q05 -5.17%
   - session (n=160) : retour [-4.42% .. +4.63%] · haut q95 +5.47% · bas q05 -5.19%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.73%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.54 · part idiosyncratique 0.46
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 23.0  _(survente)_
- **ADX** : 13.2  _(pas de tendance nette)_
- **MACD** : hist -0.117  _(pas de croisement recent)_
- **BB** : %B 0.13 · largeur 17.2%
- **ATR** : 0.59 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.38  _(distribution)_
- **Vol ratio** : 0.99  _(volume normal)_
- **Choppiness** : 46.7  _(transition)_
- **MA** : MA20 16.83 · MA50 17.45 · MA200 18.94  _(prix < MA20)_
- **Dist MA** : MA20 -6.3% · MA50 -9.7% · MA200 -16.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (837281 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
