# SOFI

**Generated** : 2026-09-30T00:35:45.932845+00:00  
**Santé technique** : 2/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $15.91  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $15.91 (+1.2% vs entrée) · entrée $15.72 · stop $15.09 · T1 $15.94 · R/R 0.35  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -67 % hors [0,100] (R² max 0.16). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.280 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $15.67–$15.76 (mid $15.72)
- Spot actuel : $15.91 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : $15.09 (plancher anti-bruit 5 s — stop EV-optimal −4% (first-passage 5 s réel) ; -4.01 % depuis l'entree)
- Targets : T1 $15.94 · R/R 0.35 | T2 $16.16 · R/R 0.7 | T3 $16.37 · R/R 1.03
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $15.09


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=5.83 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (6.52 %)** : le gap seul le franchit 1.038 % des séances (13 fois sur 1253).
   - exécution **1.148 pt plus bas** dans le cas TYPIQUE (médiane), 3.322 au p90, **4.585 au pire**
   - perte réelle **8.322 %** en moyenne _(tirée par la queue)_, jusqu'à **11.105 %** — au lieu des 6.52 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0187 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 13 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.204 % | p01 -6.52 % | pire -11.105 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1172** [0.0757 ; 0.1714] _(largeur 9.6 pt, n_eff 173.1)_
   - swing : **0.4614** [0.4094 ; 0.5141] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4563** [0.4043 ; 0.509] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : deep (25.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.29 %** | CVaR **-8.7 %** | vol 4.13 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.5 % vs -14.19 % si l'on extrapolait par √5 _(rapport 1.021 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8334** (β de hausse 1.713, asymétrie 1.0703) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.362× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 14.7129 sur sr_based (1.41 ATR, 7.553 %) — p(stop avant cible) 0.465 [0.41 ; 0.52], R/R 7.503, perte reelle 7.953 % (gap inclus), CVaR 10.84 %, EV -0.7263 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.9993 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.675 %) — p(stop avant cible) 0.5885 [0.54 ; 0.64], R/R 9.837, perte reelle 6.066 % (gap inclus), EV -0.6397 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 9.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.589, borne haute 0.639 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.64 %) : P(cible) 0.0 % x 59.67 % + P(rien) 41.1 % x 7.11 % ne couvrent pas P(stop) 58.9 % x 6.07 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+59.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ sr_based a 1.41 ATR (stop 7.553 %) — p(stop avant cible) 0.465 [0.41 ; 0.52], R/R 7.503, perte reelle 7.953 % (gap inclus), EV -0.7263 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.73 %) : P(cible) 0.0 % x 59.67 % + P(rien) 53.5 % x 5.55 % ne couvrent pas P(stop) 46.5 % x 7.95 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+59.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🟢 support a 1.72 ATR (stop 8.705 %) — p(stop avant cible) 0.3943 [0.34 ; 0.45], R/R 6.475, perte reelle 9.216 % (gap inclus), EV -0.8373 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.26 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.84 %) : P(cible) 0.0 % x 59.67 % + P(rien) 60.6 % x 4.61 % ne couvrent pas P(stop) 39.4 % x 9.22 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+59.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.25 ATR (stop 0.946 %) — p(stop avant cible) 0.939 [0.91 ; 0.96], R/R 58.567, perte reelle 1.019 % (gap inclus), EV -0.1319 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 58.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.939, borne haute 0.961 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 0.0 % x 59.67 % + P(rien) 6.1 % x 13.54 % ne couvrent pas P(stop) 93.9 % x 1.02 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+59.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.5 ATR (stop 1.892 %) — p(stop avant cible) 0.8984 [0.86 ; 0.93], R/R 28.452, perte reelle 2.097 % (gap inclus), EV -0.5535 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 28.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.898, borne haute 0.927 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.55 %) : P(cible) 0.0 % x 59.67 % + P(rien) 10.2 % x 13.10 % ne couvrent pas P(stop) 89.8 % x 2.10 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+59.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.75 ATR (stop 2.838 %) — p(stop avant cible) 0.8366 [0.79 ; 0.87], R/R 19.453, perte reelle 3.068 % (gap inclus), EV -0.8659 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 19.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.837, borne haute 0.873 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.87 %) : P(cible) 0.0 % x 59.67 % + P(rien) 16.3 % x 10.41 % ne couvrent pas P(stop) 83.7 % x 3.07 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+59.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.0 ATR (stop 3.783 %) — p(stop avant cible) 0.7302 [0.68 ; 0.77], R/R 14.509, perte reelle 4.113 % (gap inclus), EV -0.7037 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 14.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.730, borne haute 0.775 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.70 %) : P(cible) 0.0 % x 59.67 % + P(rien) 27.0 % x 8.53 % ne couvrent pas P(stop) 73.0 % x 4.11 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+59.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ grid_snapped a 1.41 ATR (stop 6.487 %) — p(stop avant cible) 0.5196 [0.47 ; 0.57], R/R 8.796, perte reelle 6.784 % (gap inclus), EV -0.5302 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 8.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.520, borne haute 0.572 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 0.0 % x 59.67 % + P(rien) 48.0 % x 6.22 % ne couvrent pas P(stop) 52.0 % x 6.78 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+59.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.5 ATR (stop 9.459 %) — p(stop avant cible) 0.3627 [0.31 ; 0.41], R/R 5.995, perte reelle 9.954 % (gap inclus), EV -0.928 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.66 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.93 %) : P(cible) 0.0 % x 59.67 % + P(rien) 63.7 % x 4.20 % ne couvrent pas P(stop) 36.3 % x 9.95 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+59.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.75 ATR (stop 10.405 %) — p(stop avant cible) 0.3083 [0.26 ; 0.36], R/R 5.504, perte reelle 10.841 % (gap inclus), EV -0.8102 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.95 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.81 %) : P(cible) 0.0 % x 59.67 % + P(rien) 69.2 % x 3.65 % ne couvrent pas P(stop) 30.8 % x 10.84 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+59.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 3.0 ATR (stop 11.35 %) — p(stop avant cible) 0.2666 [0.22 ; 0.32], R/R 5.092, perte reelle 11.718 % (gap inclus), EV -0.7005 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.28 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.70 %) : P(cible) 0.0 % x 59.67 % + P(rien) 73.3 % x 3.30 % ne couvrent pas P(stop) 26.7 % x 11.72 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+59.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 3.5 ATR (stop 13.242 %) — p(stop avant cible) 0.1802 [0.14 ; 0.22], R/R 4.414, perte reelle 13.518 % (gap inclus), EV -0.2823 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.24 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.28 %) : P(cible) 0.0 % x 59.67 % + P(rien) 82.0 % x 2.62 % ne couvrent pas P(stop) 18.0 % x 13.52 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+59.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 4.0 ATR (stop 15.134 %) — p(stop avant cible) 0.1181 [0.09 ; 0.16], R/R 3.905, perte reelle 15.281 % (gap inclus), EV -0.0921 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 15.48 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.09 %) : P(cible) 0.0 % x 59.67 % + P(rien) 88.2 % x 1.94 % ne couvrent pas P(stop) 11.8 % x 15.28 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+59.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 4.5 ATR (stop 17.026 %) — p(stop avant cible) 0.0737 [0.05 ; 0.10], R/R 3.479, perte reelle 17.15 % (gap inclus), EV -0.025 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 17.21 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.02 %) : P(cible) 0.0 % x 59.67 % + P(rien) 92.6 % x 1.33 % ne couvrent pas P(stop) 7.4 % x 17.15 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+59.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 5.0 ATR (stop 18.917 %) — p(stop avant cible) 0.056 [0.04 ; 0.08], R/R 3.146, perte reelle 18.967 % (gap inclus), EV -0.0332 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 18.97 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 0.0 % x 59.67 % + P(rien) 94.4 % x 1.08 % ne couvrent pas P(stop) 5.6 % x 18.97 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+59.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 5.5 ATR (stop 20.809 %) — p(stop avant cible) 0.0409 [0.02 ; 0.07], R/R 2.852, perte reelle 20.926 % (gap inclus), EV -0.0595 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.23 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.06 %) : P(cible) 0.0 % x 59.67 % + P(rien) 95.9 % x 0.82 % ne couvrent pas P(stop) 4.1 % x 20.93 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+59.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 6.0 ATR (stop 22.701 %) — p(stop avant cible) 0.0298 [0.02 ; 0.05], R/R 2.612, perte reelle 22.845 % (gap inclus), EV -0.0785 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.87 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.08 %) : P(cible) 0.0 % x 59.67 % + P(rien) 97.0 % x 0.61 % ne couvrent pas P(stop) 3.0 % x 22.85 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+59.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 6.5 ATR (stop 24.593 %) — p(stop avant cible) 0.0203 [0.01 ; 0.04], R/R 2.41, perte reelle 24.765 % (gap inclus), EV -0.0436 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.70 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 0.0 % x 59.67 % + P(rien) 98.0 % x 0.46 % ne couvrent pas P(stop) 2.0 % x 24.76 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+59.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 7.0 ATR (stop 26.484 %) — p(stop avant cible) 0.0043 [0.00 ; 0.02], R/R 2.228, perte reelle 26.787 % (gap inclus), EV 0.0542 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.13 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 28.376 %) — p(stop avant cible) 0.0036 [0.00 ; 0.01], R/R 2.102, perte reelle 28.393 % (gap inclus), EV 0.0527 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.18 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 30.268 %) — p(stop avant cible) 0.0028 [0.00 ; 0.01], R/R 1.964, perte reelle 30.376 % (gap inclus), EV 0.0591 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.08 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 15.915, ATR14 0.6021 (3.783 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.376 ATR = 1.423 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.189 % | 15.8849 | 92.85 % | 95.77 % | 97.07 % | 97.47 % | 98.27 % | 98.87 % |
| 0.1 ATR | 0.378 % | 15.8548 | 85.2 % | 89.42 % | 92.03 % | 93.33 % | 95.53 % | 97.13 % |
| 0.15 ATR | 0.568 % | 15.8247 | 78.95 % | 84.68 % | 87.99 % | 90.39 % | 92.89 % | 94.87 % |
| 0.2 ATR | 0.757 % | 15.7946 | 71.6 % | 79.44 % | 83.35 % | 86.86 % | 90.55 % | 93.33 % |
| 0.25 ATR | 0.946 % | 15.7645 | 66.26 % | 74.9 % | 79.92 % | 84.13 % | 88.92 % | 91.89 % |
| 0.35 ATR | 1.324 % | 15.7043 | 52.57 % | 65.12 % | 71.85 % | 78.26 % | 85.37 % | 88.6 % |
| 0.5 ATR | 1.892 % | 15.6139 | 37.66 % | 53.02 % | 61.45 % | 69.06 % | 79.37 % | 84.5 % |
| 0.75 ATR | 2.838 % | 15.4634 | 20.64 % | 37.0 % | 46.82 % | 56.93 % | 69.72 % | 77.82 % |
| 1.0 ATR | 3.783 % | 15.3129 | 8.86 % | 24.6 % | 33.91 % | 44.89 % | 59.45 % | 69.2 % |
| 1.25 ATR | 4.729 % | 15.1623 | 4.23 % | 15.12 % | 23.92 % | 35.29 % | 50.2 % | 62.53 % |
| 1.5 ATR | 5.675 % | 15.0118 | 2.01 % | 9.48 % | 16.55 % | 27.2 % | 42.38 % | 56.16 % |
| 2.0 ATR | 7.567 % | 14.7107 | 0.7 % | 4.44 % | 8.38 % | 15.17 % | 29.07 % | 45.38 % |
| 2.5 ATR | 9.459 % | 14.4096 | 0.3 % | 1.92 % | 3.94 % | 9.5 % | 19.51 % | 35.63 % |
| 3.0 ATR | 11.35 % | 14.1086 | 0.1 % | 0.91 % | 2.83 % | 6.17 % | 13.62 % | 28.23 % |
| 4.0 ATR | 15.134 % | 13.5064 | 0.0 % | 0.3 % | 0.71 % | 2.53 % | 7.42 % | 14.68 % |
| 6.0 ATR | 22.701 % | 12.3021 | 0.0 % | 0.1 % | 0.2 % | 0.2 % | 0.91 % | 3.08 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.69 ATR | 0.76 ATR | 0.98 ATR | 1.21 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.62 ATR | 0.83 ATR | 0.99 ATR | 1.12 ATR | 1.48 ATR | 1.94 ATR |
| **3 s.** | 0.31 ATR | 0.70 ATR | 0.79 ATR | 1.02 ATR | 1.22 ATR | 1.38 ATR | 1.90 ATR | 2.38 ATR |
| **5 s.** | 0.40 ATR | 0.89 ATR | 1.00 ATR | 1.32 ATR | 1.59 ATR | 1.80 ATR | 2.46 ATR | 3.32 ATR |
| **10 s.** | 0.61 ATR | 1.26 ATR | 1.42 ATR | 1.85 ATR | 2.21 ATR | 2.47 ATR | 3.58 ATR | 4.74 ATR |
| **20 s.** | 0.83 ATR | 1.79 ATR | 2.02 ATR | 2.68 ATR | 3.24 ATR | 3.61 ATR | 4.81 ATR | 5.67 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.426–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.892 %, prix 15.6139), p(touche) 37.66 % (en stress 84.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.625–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.838 %, prix 15.4633), p(touche) 37.0 % (en stress 91.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 19.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.785–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.783 %, prix 15.3129), p(touche) 33.91 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.998–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.783 %, prix 15.3129), p(touche) 44.89 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.416–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.675 %, prix 15.0118), p(touche) 42.38 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.019–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (9.459 %, prix 14.4096), p(touche) 35.63 % (en stress 98.98 %)  ✅ optimum identifie (75.2 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.017 | EV/share : $-0.011 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 59 % | T2 37 % | T3 15 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.6 | bear 6.5 | side 79.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.239% → cible +1.393% / stop −4.0%, p_fill 68%, n_eff≈76.1) : P(cible|rempli) **52%** · **EV/risk -0.021** (×p_fill ; si rempli -0.12% du capital)
  - **swing** (entrée dip −2.736% → cible +3.115% / stop −3.89%, p_fill 56%, n_eff≈65.3) : P(cible|rempli) **60%** · **EV/risk +0.033** (×p_fill ; si rempli +0.23% du capital)
  - **deep** (entrée dip −4.225% → cible +4.406% / stop −5.926%, p_fill 50%, n_eff≈56.8) : P(cible|rempli) **54%** · **EV/risk -0.039** (×p_fill ; si rempli -0.47% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→69% · +2.0%→46% · +3.0%→34% · +5.0%→10% · +8.0%→1%
- Range intraday médian 4.27% (p90 6.7%) · excursion haute méd. +1.81% / basse méd. −2.15%
- Profil de vol intra : ouverture 2.939% vs midi 0.872% vs clôture 0.991% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 16% · trend ↑2%/↓0% ; spike-down 59% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.149 ; neutre — autocorr -0.027)_ ; drift intra méd. 0.126% ; recovery-V 26%
- **σ réalisé intraday** 2.603% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 52% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 18.1833 (VA 18.1547–18.2972 ; dernier close 18.21)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 46% · rebond 66% · **stop −3.09%** sous le fill (sous le bruit) · cible +1.53% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. 0.19% · baisse 43% (gap-down >1% 24% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −1.66%) · haut méd +0.72% · range méd 1.65%
- Excursion ouverture 15min (n=160) : bas méd −0.93% (p90 −2.64%) · haut méd +1.02% · range méd 2.24%
- Excursion ouverture 30min (n=160) : bas méd −1.08% (p90 −3.16%) · haut méd +1.22% · range méd 2.66%
- Excursion ouverture 60min (n=160) : bas méd −1.21% (p90 −3.66%) · haut méd +1.31% · range méd 3.28%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 18.22 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 73% (119/159) · gap 32% · délai 0.0min · rebond 52% (64/119) (MFE +1.18%)
   - −1.0% : fill 30min 52% · séance 64% (107/159) · gap 24% · délai 1.2min · rebond 52% (60/107) (MFE +1.01%)
   - −1.5% : fill 30min 41% · séance 59% (98/159) · gap 21% · délai 6.7min · rebond 60% (63/98) (MFE +1.33%)
   - −2.0% : fill 30min 34% · séance 46% (78/159) · gap 11% · délai 4.5min · rebond 66% (53/78) (MFE +1.53%)
   - −3.0% : fill 30min 11% · séance 32% (56/159) · gap 2% · délai 50.4min · rebond 54% (36/56) (MFE +1.08%)
   - −4.0% : fill 30min 8% · séance 18% (35/159) · gap 2% · délai 50.0min · rebond 51% (22/35) (MFE +1.18%)
   - −5.0% : fill 30min 3% · séance 10% (19/159) · gap 2% · délai 203.7min · rebond 43% (9/19) (MFE +0.7%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.44% (p90 −1.78%) → stop au-delà de −1.26% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.48% (p90 −1.93%) → stop au-delà de −1.38% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.47% (p90 −1.43%) → stop au-delà de −1.17% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=656 jambes) : jambe baissière méd −1.08% (p90 −2.75%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (65 séances) :
      · −1.0% : fill 98% (64/65) · rebond 50% (37/64)
      · −2.0% : fill 85% (54/65) · rebond 71% (38/54)
      · −3.0% : fill 62% (41/65) · rebond 55% (27/41)
      · −4.0% : fill 36% (27/65) · rebond 60% (19/27)
      · −5.0% : fill 21% (15/65) · rebond 52% (8/15)
   - **flat** (23 séances) :
      · −1.0% : fill 59% (13/23) · rebond 42% (6/13)
      · −2.0% : fill 40% (8/23) · rebond 56% (5/8)
      · −3.0% : fill 30% (6/23) · rebond 38% (3/6)
      · −4.0% : fill 19% (3/23) · rebond 30% (1/3)
      · −5.0% : fill 11% (1/23) · rebond 0% (0/1)
   - **gap-up** (71 séances) :
      · −1.0% : fill 39% (30/71) · rebond 60% (17/30)
      · −2.0% : fill 19% (16/71) · rebond 55% (10/16)
      · −3.0% : fill 11% (9/71) · rebond 60% (6/9)
      · −4.0% : fill 3% (5/71) · rebond 23% (2/5)
      · −5.0% : fill 1% (3/71) · rebond 44% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 66% si les 15 1res min sont vertes (74 cas) · 26% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **52min** → P(séance verte=clôture>ouverture) 81% si début vert vs 12% si rouge (base 44% · écart 70 pts) ; prédictivité sature ensuite (plafond brut 228min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=69) : tient le vert **81%** · continue >prix actuel 60% ; creux résiduel méd -1.0% (q20 -2.13%) → **SL/trailing à −2.13%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.32% / q75 +2.8% → **scale +1.32% / runner +2.8%**, sortie à la clôture
  - **si ROUGE au coude** (n=91) : edge inversé — récupère vert seulement **12%** (continue à baisser 55%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.13%** (au-delà de la MAE q10 -3.13%), cible rebond +1.23% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.87% .. +3.67%] · haut q95 +4.01% · bas q05 -3.38%
   - 60min (n=160) : retour [-3.13% .. +4.25%] · haut q95 +4.63% · bas q05 -4.0%
   - 2h (n=160) : retour [-3.52% .. +4.46%] · haut q95 +5.17% · bas q05 -4.43%
   - 4h (n=160) : retour [-4.31% .. +4.56%] · haut q95 +5.68% · bas q05 -5.13%
   - 6h (n=160) : retour [-4.7% .. +4.64%] · haut q95 +5.7% · bas q05 -5.68%
   - session (n=160) : retour [-4.66% .. +4.98%] · haut q95 +5.7% · bas q05 -5.91%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.88%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.57 · part idiosyncratique 0.43
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 30.6  _(momentum baissier)_
- **ADX** : 10.9  _(pas de tendance nette)_
- **MACD** : hist -0.13  _(pas de croisement recent)_
- **BB** : %B 0.05 · largeur 15.8%
- **ATR** : 0.6 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.281  _(distribution)_
- **Vol ratio** : 0.75  _(volume normal)_
- **Choppiness** : 52.7  _(transition)_
- **MA** : MA20 17.13 · MA50 17.54 · MA200 19.11  _(prix < MA20)_
- **Dist MA** : MA20 -7.1% · MA50 -9.2% · MA200 -16.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (848001 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
