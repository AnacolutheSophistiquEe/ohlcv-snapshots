# SOFI

**Generated** : 2026-10-01T00:33:29.103089+00:00  
**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $15.72  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $15.72 (+1.0% vs entrée) · entrée $15.57 · stop $14.32 · T1 $15.87 · R/R 0.24  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +3.7 % ≠ (strike 16.5 − spot 15.72)/spot = +5.0 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -81 % hors [0,100] (R² max 0.16). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.290 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $15.53–$15.61 (mid $15.57)
- Spot actuel : $15.72 (+1.0% au-dessus de la zone — repli à attendre)
- Stop : $14.32 (plancher anti-bruit 5 s — stop EV-optimal −8% (first-passage 5 s réel) ; -8.03 % depuis l'entree)
- Targets : T1 $15.87 · R/R 0.24 | T2 $16.17 · R/R 0.48 | T3 $16.47 · R/R 0.72
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $14.32


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=5.83 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (5.9 %)** : le gap seul le franchit 1.437 % des séances (18 fois sur 1253).
   - exécution **1.308 pt plus bas** dans le cas TYPIQUE (médiane), 3.901 au p90, **5.205 au pire**
   - perte réelle **7.728 %** en moyenne _(tirée par la queue)_, jusqu'à **11.105 %** — au lieu des 5.9 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0263 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.204 % | p01 -6.52 % | pire -11.105 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0124** [0.0027 ; 0.0379] _(largeur 3.5 pt, n_eff 173.1)_
   - swing : **0.5514** [0.4987 ; 0.6032] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.5078** [0.4552 ; 0.5603] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 80.0 observations effectives », dont la borne haute a 95 % vaut environ 3.8 %.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.29 %** | CVaR **-8.7 %** | vol 4.13 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.5 % vs -14.19 % si l'on extrapolait par √5 _(rapport 1.021 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8327** (β de hausse 1.7124, asymétrie 1.0702) vs IWM — 605 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.358× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 14.4988 sur support (1.39 ATR, 7.739 %) — p(stop avant cible) 0.4464 [0.39 ; 0.50], R/R 7.596, perte reelle 8.123 % (gap inclus), CVaR 10.832 %, EV -0.7409 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 1.08 ATR (stop 6.573 %) — p(stop avant cible) 0.5173 [0.46 ; 0.57], R/R 8.994, perte reelle 6.861 % (gap inclus), EV -0.5892 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 8.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.517, borne haute 0.570 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.59 %) : P(cible) 0.0 % x 61.70 % + P(rien) 48.3 % x 6.13 % ne couvrent pas P(stop) 51.7 % x 6.86 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🔴 support a 1.39 ATR (stop 7.739 %) — p(stop avant cible) 0.4464 [0.39 ; 0.50], R/R 7.596, perte reelle 8.123 % (gap inclus), EV -0.7409 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - ⚠ support DETECTE a 0.98 ATR du spot — compartiment <1, mesure a 45.4 % de casse (IC clusterise [0.423 ; 0.484] sur 1130 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.74 %) : P(cible) 0.0 % x 61.70 % + P(rien) 55.4 % x 5.21 % ne couvrent pas P(stop) 44.6 % x 8.12 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.25 ATR (stop 0.958 %) — p(stop avant cible) 0.9386 [0.91 ; 0.96], R/R 59.778, perte reelle 1.032 % (gap inclus), EV -0.1304 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 59.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.939, borne haute 0.960 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 0.0 % x 61.70 % + P(rien) 6.1 % x 13.68 % ne couvrent pas P(stop) 93.9 % x 1.03 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.5 ATR (stop 1.916 %) — p(stop avant cible) 0.8965 [0.86 ; 0.93], R/R 28.993, perte reelle 2.128 % (gap inclus), EV -0.5542 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 28.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.896, borne haute 0.925 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.55 %) : P(cible) 0.0 % x 61.70 % + P(rien) 10.3 % x 13.09 % ne couvrent pas P(stop) 89.6 % x 2.13 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.75 ATR (stop 2.874 %) — p(stop avant cible) 0.8359 [0.79 ; 0.87], R/R 19.897, perte reelle 3.101 % (gap inclus), EV -0.8798 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 19.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.836, borne haute 0.872 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.88 %) : P(cible) 0.0 % x 61.70 % + P(rien) 16.4 % x 10.44 % ne couvrent pas P(stop) 83.6 % x 3.10 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ grid_snapped a 1.08 ATR (stop 5.296 %) — p(stop avant cible) 0.6135 [0.56 ; 0.66], R/R 10.881, perte reelle 5.671 % (gap inclus), EV -0.6029 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 10.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.614, borne haute 0.664 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.60 %) : P(cible) 0.0 % x 61.70 % + P(rien) 38.6 % x 7.44 % ne couvrent pas P(stop) 61.4 % x 5.67 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.25 ATR (stop 8.621 %) — p(stop avant cible) 0.3965 [0.35 ; 0.45], R/R 6.756, perte reelle 9.134 % (gap inclus), EV -0.8535 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.23 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.85 %) : P(cible) 0.0 % x 61.70 % + P(rien) 60.3 % x 4.59 % ne couvrent pas P(stop) 39.6 % x 9.13 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.5 ATR (stop 9.579 %) — p(stop avant cible) 0.3552 [0.31 ; 0.41], R/R 6.131, perte reelle 10.065 % (gap inclus), EV -0.9798 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.68 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.98 %) : P(cible) 0.0 % x 61.70 % + P(rien) 64.5 % x 4.02 % ne couvrent pas P(stop) 35.5 % x 10.06 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.75 ATR (stop 10.537 %) — p(stop avant cible) 0.3015 [0.25 ; 0.35], R/R 5.63, perte reelle 10.96 % (gap inclus), EV -0.8172 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.96 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.82 %) : P(cible) 0.0 % x 61.70 % + P(rien) 69.8 % x 3.56 % ne couvrent pas P(stop) 30.1 % x 10.96 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 3.0 ATR (stop 11.495 %) — p(stop avant cible) 0.2582 [0.21 ; 0.31], R/R 5.211, perte reelle 11.842 % (gap inclus), EV -0.7516 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.27 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.75 %) : P(cible) 0.0 % x 61.70 % + P(rien) 74.2 % x 3.11 % ne couvrent pas P(stop) 25.8 % x 11.84 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 3.5 ATR (stop 13.411 %) — p(stop avant cible) 0.1771 [0.14 ; 0.22], R/R 4.516, perte reelle 13.664 % (gap inclus), EV -0.3467 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.31 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.35 %) : P(cible) 0.0 % x 61.70 % + P(rien) 82.3 % x 2.52 % ne couvrent pas P(stop) 17.7 % x 13.66 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 4.0 ATR (stop 15.327 %) — p(stop avant cible) 0.1144 [0.08 ; 0.15], R/R 3.993, perte reelle 15.454 % (gap inclus), EV -0.1472 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 15.62 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 0.0 % x 61.70 % + P(rien) 88.6 % x 1.83 % ne couvrent pas P(stop) 11.4 % x 15.45 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 4.5 ATR (stop 17.242 %) — p(stop avant cible) 0.0715 [0.05 ; 0.10], R/R 3.555, perte reelle 17.357 % (gap inclus), EV -0.0587 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 17.41 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.06 %) : P(cible) 0.0 % x 61.70 % + P(rien) 92.8 % x 1.27 % ne couvrent pas P(stop) 7.1 % x 17.36 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 5.0 ATR (stop 19.158 %) — p(stop avant cible) 0.0533 [0.03 ; 0.08], R/R 3.214, perte reelle 19.199 % (gap inclus), EV -0.078 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 19.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.08 %) : P(cible) 0.0 % x 61.70 % + P(rien) 94.7 % x 1.00 % ne couvrent pas P(stop) 5.3 % x 19.20 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 5.5 ATR (stop 21.074 %) — p(stop avant cible) 0.0342 [0.02 ; 0.06], R/R 2.912, perte reelle 21.189 % (gap inclus), EV -0.1004 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.17 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 0.0 % x 61.70 % + P(rien) 96.6 % x 0.65 % ne couvrent pas P(stop) 3.4 % x 21.19 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 6.0 ATR (stop 22.99 %) — p(stop avant cible) 0.0266 [0.01 ; 0.05], R/R 2.667, perte reelle 23.136 % (gap inclus), EV -0.1045 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.63 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 0.0 % x 61.70 % + P(rien) 97.3 % x 0.52 % ne couvrent pas P(stop) 2.7 % x 23.14 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 6.5 ATR (stop 24.906 %) — p(stop avant cible) 0.0179 [0.01 ; 0.04], R/R 2.462, perte reelle 25.063 % (gap inclus), EV -0.0748 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.41 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.07 %) : P(cible) 0.0 % x 61.70 % + P(rien) 98.2 % x 0.38 % ne couvrent pas P(stop) 1.8 % x 25.06 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+61.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 7.0 ATR (stop 26.821 %) — p(stop avant cible) 0.0042 [0.00 ; 0.02], R/R 2.284, perte reelle 27.011 % (gap inclus), EV 0.0111 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.13 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 28.737 %) — p(stop avant cible) 0.0029 [0.00 ; 0.01], R/R 2.146, perte reelle 28.753 % (gap inclus), EV 0.0179 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.99 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 30.653 %) — p(stop avant cible) 0.0028 [0.00 ; 0.01], R/R 2.012, perte reelle 30.664 % (gap inclus), EV 0.0138 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.08 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 15.715, ATR14 0.6021 (3.832 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.377 ATR = 1.445 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.192 % | 15.6849 | 92.85 % | 95.77 % | 97.07 % | 97.47 % | 98.27 % | 98.87 % |
| 0.1 ATR | 0.383 % | 15.6548 | 85.2 % | 89.42 % | 92.03 % | 93.33 % | 95.53 % | 97.13 % |
| 0.15 ATR | 0.575 % | 15.6247 | 78.95 % | 84.68 % | 87.99 % | 90.39 % | 92.89 % | 94.87 % |
| 0.2 ATR | 0.766 % | 15.5946 | 71.6 % | 79.44 % | 83.35 % | 86.86 % | 90.55 % | 93.33 % |
| 0.25 ATR | 0.958 % | 15.5645 | 66.26 % | 74.9 % | 79.92 % | 84.13 % | 88.92 % | 91.89 % |
| 0.35 ATR | 1.341 % | 15.5043 | 52.67 % | 65.12 % | 71.85 % | 78.26 % | 85.37 % | 88.6 % |
| 0.5 ATR | 1.916 % | 15.4139 | 37.66 % | 53.12 % | 61.45 % | 69.06 % | 79.37 % | 84.5 % |
| 0.75 ATR | 2.874 % | 15.2634 | 20.64 % | 37.0 % | 46.92 % | 57.03 % | 69.82 % | 77.93 % |
| 1.0 ATR | 3.832 % | 15.1129 | 8.86 % | 24.6 % | 34.01 % | 44.99 % | 59.55 % | 69.3 % |
| 1.25 ATR | 4.79 % | 14.9623 | 4.23 % | 15.12 % | 24.02 % | 35.39 % | 50.3 % | 62.63 % |
| 1.5 ATR | 5.747 % | 14.8118 | 2.01 % | 9.48 % | 16.65 % | 27.3 % | 42.48 % | 56.26 % |
| 2.0 ATR | 7.663 % | 14.5107 | 0.7 % | 4.44 % | 8.38 % | 15.17 % | 29.07 % | 45.38 % |
| 2.5 ATR | 9.579 % | 14.2096 | 0.3 % | 1.92 % | 3.94 % | 9.5 % | 19.51 % | 35.63 % |
| 3.0 ATR | 11.495 % | 13.9086 | 0.1 % | 0.91 % | 2.83 % | 6.17 % | 13.62 % | 28.23 % |
| 4.0 ATR | 15.327 % | 13.3064 | 0.0 % | 0.3 % | 0.71 % | 2.53 % | 7.42 % | 14.68 % |
| 6.0 ATR | 22.99 % | 12.1021 | 0.0 % | 0.1 % | 0.2 % | 0.2 % | 0.91 % | 3.08 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.69 ATR | 0.76 ATR | 0.98 ATR | 1.21 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.63 ATR | 0.83 ATR | 0.99 ATR | 1.12 ATR | 1.48 ATR | 1.94 ATR |
| **3 s.** | 0.31 ATR | 0.70 ATR | 0.79 ATR | 1.02 ATR | 1.23 ATR | 1.39 ATR | 1.90 ATR | 2.38 ATR |
| **5 s.** | 0.40 ATR | 0.90 ATR | 1.00 ATR | 1.32 ATR | 1.59 ATR | 1.80 ATR | 2.46 ATR | 3.32 ATR |
| **10 s.** | 0.61 ATR | 1.26 ATR | 1.42 ATR | 1.85 ATR | 2.21 ATR | 2.47 ATR | 3.58 ATR | 4.74 ATR |
| **20 s.** | 0.83 ATR | 1.79 ATR | 2.02 ATR | 2.68 ATR | 3.24 ATR | 3.61 ATR | 4.81 ATR | 5.67 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.427–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.916 %, prix 15.4139), p(touche) 37.66 % (en stress 84.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.626–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.874 %, prix 15.2634), p(touche) 37.0 % (en stress 91.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 19.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.787–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.832 %, prix 15.1128), p(touche) 34.01 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 21.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.0–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.832 %, prix 15.1128), p(touche) 44.99 % (en stress 96.97 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.419–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.747 %, prix 14.8119), p(touche) 42.48 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.019–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (9.579 %, prix 14.2097), p(touche) 35.63 % (en stress 98.98 %)  ✅ optimum identifie (75.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.024 | EV/share : $-0.030 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 18 % | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.8 | bear 6.5 | side 79.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.946% → cible +1.934% / stop −8.0%, p_fill 76%, n_eff≈80.0) : P(cible|rempli) **34%** · **EV/risk -0.036** (×p_fill ; si rempli -0.39% du capital)
  - **swing** (entrée dip −2.068% → cible +4.374% / stop −3.913%, p_fill 66%, n_eff≈77.1) : P(cible|rempli) **48%** · **EV/risk +0.063** (×p_fill ; si rempli +0.38% du capital)
  - **deep** (entrée dip −3.203% → cible +6.259% / stop −5.937%, p_fill 65%, n_eff≈72.4) : P(cible|rempli) **48%** · **EV/risk +0.026** (×p_fill ; si rempli +0.24% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→64% · +2.0%→43% · +3.0%→32% · +5.0%→10% · +8.0%→1%
- Range intraday médian 4.08% (p90 6.61%) · excursion haute méd. +1.55% / basse méd. −2.06%
- Profil de vol intra : ouverture 2.885% vs midi 0.825% vs clôture 0.939% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 22% · trend ↑1%/↓0% ; spike-down 61% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.159 ; neutre — autocorr -0.027)_ ; drift intra méd. -0.609% ; recovery-V 20%
- **σ réalisé intraday** 2.327% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 59% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 15.9081 (VA 15.8644–16.0306 ; dernier close 15.91)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 16% · rebond 60% · **stop −2.1%** sous le fill (sous le bruit) · cible +1.85% · R/R 0.88 (high win-rate)
- Gaps overnight (n=159) : méd. 0.11% · baisse 45% (gap-down >1% 23% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −0.67% (p90 −1.62%) · haut méd +0.63% · range méd 1.46%
- Excursion ouverture 15min (n=160) : bas méd −1.01% (p90 −2.49%) · haut méd +0.82% · range méd 2.05%
- Excursion ouverture 30min (n=160) : bas méd −1.12% (p90 −3.33%) · haut méd +0.87% · range méd 2.44%
- Excursion ouverture 60min (n=160) : bas méd −1.23% (p90 −3.61%) · haut méd +0.99% · range méd 2.87%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 15.91 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 75% (120/159) · gap 31% · délai 0.0min · rebond 53% (67/120) (MFE +1.13%)
   - −1.0% : fill 30min 52% · séance 63% (105/159) · gap 23% · délai 1.5min · rebond 49% (56/105) (MFE +0.93%)
   - −1.5% : fill 30min 43% · séance 58% (96/159) · gap 20% · délai 6.8min · rebond 59% (61/96) (MFE +1.3%)
   - −2.0% : fill 30min 32% · séance 45% (75/159) · gap 8% · délai 9.8min · rebond 63% (51/75) (MFE +1.46%)
   - −3.0% : fill 30min 8% · séance 32% (54/159) · gap 2% · délai 77.7min · rebond 49% (33/54) (MFE +1.02%)
   - −4.0% : fill 30min 6% · séance 16% (32/159) · gap 2% · délai 86.0min · rebond 60% (20/32) (MFE +1.85%)
   - −5.0% : fill 30min 2% · séance 7% (16/159) · gap 1% · délai 207.5min · rebond 43% (8/16) (MFE +0.65%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.48% (p90 −1.81%) → stop au-delà de −1.28% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.49% (p90 −1.87%) → stop au-delà de −1.42% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −1.43%) → stop au-delà de −1.1% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=623 jambes) : jambe baissière méd −1.0% (p90 −2.78%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (65 séances) :
      · −1.0% : fill 98% (64/65) · rebond 49% (35/64)
      · −2.0% : fill 86% (55/65) · rebond 68% (38/55)
      · −3.0% : fill 59% (40/65) · rebond 50% (26/40)
      · −4.0% : fill 35% (26/65) · rebond 69% (18/26)
      · −5.0% : fill 15% (13/65) · rebond 52% (7/13)
   - **flat** (24 séances) :
      · −1.0% : fill 73% (15/24) · rebond 36% (6/15)
      · −2.0% : fill 42% (8/24) · rebond 53% (5/8)
      · −3.0% : fill 37% (7/24) · rebond 44% (3/7)
      · −4.0% : fill 12% (3/24) · rebond 30% (1/3)
      · −5.0% : fill 7% (1/24) · rebond 0% (0/1)
   - **gap-up** (70 séances) :
      · −1.0% : fill 30% (26/70) · rebond 60% (15/26)
      · −2.0% : fill 14% (12/70) · rebond 55% (8/12)
      · −3.0% : fill 8% (7/70) · rebond 58% (4/7)
      · −4.0% : fill 2% (3/70) · rebond 17% (1/3)
      · −5.0% : fill 1% (2/70) · rebond 59% (1/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 40% en base · 66% si les 15 1res min sont vertes (71 cas) · 23% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:01** → P(séance verte=clôture>ouverture) 76% si début vert vs 12% si rouge (base 40% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 228min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **76%** · continue >prix actuel 56% ; creux résiduel méd -0.86% (q20 -2.09%) → **SL/trailing à −2.09%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.01% / q75 +2.59% → **scale +1.01% / runner +2.59%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **12%** (continue à baisser 60%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.7%** (au-delà de la MAE q10 -2.7%), cible rebond +1.13% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.02% .. +3.19%] · haut q95 +3.93% · bas q05 -3.59%
   - 60min (n=160) : retour [-3.14% .. +3.68%] · haut q95 +4.52% · bas q05 -4.01%
   - 2h (n=160) : retour [-3.57% .. +3.88%] · haut q95 +5.01% · bas q05 -4.49%
   - 4h (n=160) : retour [-3.93% .. +4.3%] · haut q95 +5.44% · bas q05 -5.11%
   - 6h (n=160) : retour [-4.47% .. +4.07%] · haut q95 +5.47% · bas q05 -5.18%
   - session (n=160) : retour [-4.49% .. +4.64%] · haut q95 +5.48% · bas q05 -5.25%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.77%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.56 · part idiosyncratique 0.44
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 30.0  _(survente)_
- **ADX** : 11.7  _(pas de tendance nette)_
- **MACD** : hist -0.142  _(pas de croisement recent)_
- **BB** : %B 0.05 · largeur 17.5%
- **ATR** : 0.6 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.289  _(distribution)_
- **Vol ratio** : 0.84  _(volume normal)_
- **Choppiness** : 50.1  _(transition)_
- **MA** : MA20 17.07 · MA50 17.5 · MA200 19.05  _(prix < MA20)_
- **Dist MA** : MA20 -7.9% · MA50 -10.2% · MA200 -17.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (845207 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
