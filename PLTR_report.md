# PLTR

**Generated** : 2026-08-28T00:27:02.240680+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $185.93  

> 🟡 **WAIT-FOR-DIP** — spot +4.2 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $185.93 (+4.2% vs entrée) · entrée $178.42 · stop $173.95 · T1 $184.69 · R/R 1.4  
> ↳ P(T1 av. stop) 53 % · EV/risk 0.13 · ¼-Kelly 0.002 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -159 % hors [0,100] (R² max 0.40). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $177.16–$179.67 (mid $178.42)
- Spot actuel : $185.93 (+4.2% au-dessus de la zone — repli à attendre)
- Stop : $173.95 (stop swing_plan-based (-12.77%))
- Targets : T1 $184.69 · R/R 1.4 | T2 $190.96 · R/R 2.81 | T3 $197.24 · R/R 4.21
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $173.95


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.79 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.77 %)** : le gap seul le franchit 0.239 % des séances (3 fois sur 1253).
   - exécution **1.902 pt plus bas** dans le cas TYPIQUE (médiane), 4.51 au p90, **5.162 au pire**
   - perte réelle **15.126 %** en moyenne _(tirée par la queue)_, jusqu'à **17.932 %** — au lieu des 12.77 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0056 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.882 % | p01 -6.139 % | pire -17.932 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3138** [0.2482 ; 0.3856] _(largeur 13.7 pt, n_eff 173.1)_
   - swing : **0.511** [0.4584 ; 0.5634] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4561** [0.4041 ; 0.5088] _(largeur 10.5 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.15 %** | CVaR **-8.41 %** | vol 4.26 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.44 % vs -13.82 % si l'on extrapolait par √5 _(rapport 0.972 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7084** (β de hausse 1.412, asymétrie 1.21) vs IWM — 601 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 163.7168 sur swing_based (2.44 ATR, 11.947 %) — p(stop avant cible) 0.2531 [0.21 ; 0.30], R/R 0.876, perte reelle 14.376 % (gap inclus), CVaR 11.955 %, EV 0.1439 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.815 %) — p(stop avant cible) 0.5153 [0.46 ; 0.57], R/R 1.298, perte reelle 9.704 % (gap inclus), EV -1.1432 % — **REFUSE**
      - refuse : p_stop_first 0.515, borne haute 0.568 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.14 %) : P(cible) 24.6 % x 12.60 % + P(rien) 23.9 % x 3.18 % ne couvrent pas P(stop) 51.5 % x 9.70 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.44 ATR (stop 11.947 %) — p(stop avant cible) 0.2531 [0.21 ; 0.30], R/R 0.876, perte reelle 14.376 % (gap inclus), EV 0.1439 % — **REFUSE**
      - refuse : R/R 0.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 4.27 ATR (stop 19.036 %) — p(stop avant cible) 0.0724 [0.05 ; 0.10], R/R 0.662, perte reelle 19.036 % (gap inclus), EV 1.0397 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.04 % > budget 12.00 %
   - 🟢 support a 9.44 ATR (stop 39.075 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.322, perte reelle 39.075 % (gap inclus), EV 1.395 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.07 % > budget 12.00 %
   - 🟢 support a 11.04 ATR (stop 45.271 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.278, perte reelle 45.271 % (gap inclus), EV 1.3941 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 45.27 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.969 %) — p(stop avant cible) 0.9087 [0.87 ; 0.94], R/R 5.185, perte reelle 2.43 % (gap inclus), EV -1.181 % — **REFUSE**
      - refuse : cible atteinte seulement 6.5 % du temps (< 15 %) meme a 10 seances : le R/R de 5.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.909, borne haute 0.936 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.18 %) : P(cible) 6.5 % x 12.60 % + P(rien) 2.6 % x 7.86 % ne couvrent pas P(stop) 90.9 % x 2.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.938 %) — p(stop avant cible) 0.8207 [0.78 ; 0.86], R/R 3.641, perte reelle 3.46 % (gap inclus), EV -0.9528 % — **REFUSE**
      - refuse : cible atteinte seulement 12.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.821, borne haute 0.858 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.95 %) : P(cible) 12.3 % x 12.60 % + P(rien) 5.6 % x 5.95 % ne couvrent pas P(stop) 82.1 % x 3.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.907 %) — p(stop avant cible) 0.7304 [0.68 ; 0.78], R/R 2.42, perte reelle 5.206 % (gap inclus), EV -1.137 % — **REFUSE**
      - refuse : p_stop_first 0.730, borne haute 0.775 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.14 %) : P(cible) 17.3 % x 12.60 % + P(rien) 9.7 % x 5.02 % ne couvrent pas P(stop) 73.0 % x 5.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.876 %) — p(stop avant cible) 0.6754 [0.62 ; 0.72], R/R 1.875, perte reelle 6.72 % (gap inclus), EV -1.4908 % — **REFUSE**
      - refuse : p_stop_first 0.675, borne haute 0.723 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.49 %) : P(cible) 19.6 % x 12.60 % + P(rien) 12.9 % x 4.50 % ne couvrent pas P(stop) 67.5 % x 6.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.845 %) — p(stop avant cible) 0.5875 [0.54 ; 0.64], R/R 1.533, perte reelle 8.218 % (gap inclus), EV -1.2801 % — **REFUSE**
      - refuse : p_stop_first 0.588, borne haute 0.638 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.28 %) : P(cible) 22.9 % x 12.60 % + P(rien) 18.4 % x 3.61 % ne couvrent pas P(stop) 58.8 % x 8.22 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 6.784 %) — p(stop avant cible) 0.458 [0.41 ; 0.51], R/R 1.184, perte reelle 10.642 % (gap inclus), EV -0.7239 % — **REFUSE**
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.72 %) : P(cible) 26.9 % x 12.60 % + P(rien) 27.3 % x 2.80 % ne couvrent pas P(stop) 45.8 % x 10.64 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 7.753 %) — p(stop avant cible) 0.4046 [0.35 ; 0.46], R/R 1.051, perte reelle 11.982 % (gap inclus), EV -0.6255 % — **REFUSE**
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.63 %) : P(cible) 27.9 % x 12.60 % + P(rien) 31.7 % x 2.24 % ne couvrent pas P(stop) 40.5 % x 11.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.44 ATR (stop 10.629 %) — p(stop avant cible) 0.3072 [0.26 ; 0.36], R/R 0.915, perte reelle 13.763 % (gap inclus), EV -0.3546 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.35 %) : P(cible) 28.2 % x 12.60 % + P(rien) 41.0 % x 0.77 % ne couvrent pas P(stop) 30.7 % x 13.76 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 13.567 %) — p(stop avant cible) 0.1916 [0.15 ; 0.24], R/R 0.773, perte reelle 16.302 % (gap inclus), EV 0.2371 % — **REFUSE**
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.57 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 15.506 %) — p(stop avant cible) 0.1373 [0.10 ; 0.18], R/R 0.703, perte reelle 17.932 % (gap inclus), EV 0.5394 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.51 % > budget 12.00 %
   - ⚪ grid_snapped a 4.27 ATR (stop 17.718 %) — p(stop avant cible) 0.0997 [0.07 ; 0.13], R/R 0.703, perte reelle 17.932 % (gap inclus), EV 0.8901 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.72 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 21.32 %) — p(stop avant cible) 0.0375 [0.02 ; 0.06], R/R 0.591, perte reelle 21.32 % (gap inclus), EV 1.1995 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.32 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 23.258 %) — p(stop avant cible) 0.022 [0.01 ; 0.04], R/R 0.542, perte reelle 23.258 % (gap inclus), EV 1.2878 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.26 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 25.196 %) — p(stop avant cible) 0.0077 [0.00 ; 0.02], R/R 0.5, perte reelle 25.196 % (gap inclus), EV 1.351 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.20 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 27.135 %) — p(stop avant cible) 0.0052 [0.00 ; 0.02], R/R 0.464, perte reelle 27.135 % (gap inclus), EV 1.3661 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.13 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 29.073 %) — p(stop avant cible) 0.0037 [0.00 ; 0.01], R/R 0.433, perte reelle 29.073 % (gap inclus), EV 1.3815 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.07 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 31.011 %) — p(stop avant cible) 0.0037 [0.00 ; 0.01], R/R 0.406, perte reelle 31.011 % (gap inclus), EV 1.374 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.01 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 185.93, ATR14 7.2074 (3.876 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.358 ATR = 1.388 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.194 % | 185.5696 | 92.45 % | 94.96 % | 95.76 % | 96.56 % | 97.87 % | 98.67 % |
| 0.1 ATR | 0.388 % | 185.2093 | 84.49 % | 89.01 % | 90.82 % | 93.02 % | 94.82 % | 96.41 % |
| 0.15 ATR | 0.581 % | 184.8489 | 77.14 % | 83.47 % | 85.67 % | 89.38 % | 92.17 % | 94.25 % |
| 0.2 ATR | 0.775 % | 184.4885 | 69.08 % | 78.12 % | 81.33 % | 85.95 % | 89.94 % | 92.4 % |
| 0.25 ATR | 0.969 % | 184.1282 | 62.03 % | 73.69 % | 77.4 % | 82.71 % | 87.6 % | 90.97 % |
| 0.35 ATR | 1.357 % | 183.4074 | 50.76 % | 65.73 % | 71.14 % | 78.06 % | 83.74 % | 87.89 % |
| 0.5 ATR | 1.938 % | 182.3263 | 36.25 % | 53.02 % | 59.74 % | 69.06 % | 78.15 % | 83.57 % |
| 0.75 ATR | 2.907 % | 180.5245 | 19.34 % | 35.38 % | 44.7 % | 55.51 % | 67.28 % | 76.49 % |
| 1.0 ATR | 3.876 % | 178.7226 | 8.96 % | 22.88 % | 32.59 % | 43.98 % | 56.61 % | 68.07 % |
| 1.25 ATR | 4.845 % | 176.9208 | 4.43 % | 15.52 % | 23.41 % | 34.58 % | 46.95 % | 59.45 % |
| 1.5 ATR | 5.815 % | 175.119 | 2.01 % | 10.38 % | 17.46 % | 26.69 % | 40.14 % | 54.52 % |
| 2.0 ATR | 7.753 % | 171.5153 | 0.6 % | 3.63 % | 9.18 % | 15.47 % | 29.07 % | 40.76 % |
| 2.5 ATR | 9.691 % | 167.9116 | 0.1 % | 1.41 % | 3.13 % | 9.0 % | 19.11 % | 30.18 % |
| 3.0 ATR | 11.629 % | 164.3079 | 0.0 % | 0.6 % | 1.51 % | 4.75 % | 12.91 % | 22.59 % |
| 4.0 ATR | 15.506 % | 157.1006 | 0.0 % | 0.0 % | 0.3 % | 1.52 % | 4.67 % | 11.81 % |
| 6.0 ATR | 23.258 % | 142.6858 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.51 % | 3.59 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.36 ATR | 0.41 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 0.97 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.61 ATR | 0.80 ATR | 0.96 ATR | 1.10 ATR | 1.53 ATR | 1.90 ATR |
| **3 s.** | 0.29 ATR | 0.66 ATR | 0.74 ATR | 0.99 ATR | 1.21 ATR | 1.39 ATR | 1.95 ATR | 2.35 ATR |
| **5 s.** | 0.40 ATR | 0.87 ATR | 0.98 ATR | 1.30 ATR | 1.57 ATR | 1.80 ATR | 2.42 ATR | 2.97 ATR |
| **10 s.** | 0.57 ATR | 1.17 ATR | 1.32 ATR | 1.82 ATR | 2.20 ATR | 2.46 ATR | 3.35 ATR | 3.96 ATR |
| **20 s.** | 0.79 ATR | 1.66 ATR | 1.85 ATR | 2.37 ATR | 2.84 ATR | 3.24 ATR | 4.44 ATR | 5.66 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.41–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.938 %, prix 182.3267), p(touche) 36.25 % (en stress 82.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.614–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.907 %, prix 180.525), p(touche) 35.38 % (en stress 95.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.745–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.907 %, prix 180.525), p(touche) 44.7 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.978–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.876 %, prix 178.7233), p(touche) 43.98 % (en stress 100.0 %)  ✅ optimum identifie (80.4 % des re-echantillons)
- **10 seance(s)** : plage utile 1.322–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.815 %, prix 175.1182), p(touche) 40.14 % (en stress 100.0 %)  ✅ optimum identifie (88.9 % des re-echantillons)
- **20 seance(s)** : plage utile 1.846–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (11.629 %, prix 164.3082), p(touche) 22.59 % (en stress 94.9 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (96.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.05 | EV/share : $0.223 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 21 % | T2 10 % | T3 10 %
- Kelly (position) : f* 0.009 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 29.4 | side 65.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 558.0 (= 3 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=12, n_eff=8))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→78% · +2.0%→50% · +3.0%→29% · +5.0%→10% · +8.0%→4%
- Range intraday médian 3.92% (p90 7.17%) · excursion haute méd. +2.0% / basse méd. −1.71%
- Profil de vol intra : ouverture 3.051% vs midi 0.761% vs clôture 0.858% _(ouverture ~4.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 75% · range 23% · trend ↑2%/↓0% ; spike-down 53% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; neutre — autocorr -0.003)_ ; drift intra méd. 0.675% ; recovery-V 31%
- **σ réalisé intraday** 2.659% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 42% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 179.079 (VA 177.603–181.539 ; dernier close 179.94)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 19% · rebond 48% · **stop −3.39%** sous le fill (sous le bruit) · cible +0.99% · R/R 0.29 (high win-rate)
- Gaps overnight (n=159) : méd. -0.1% · baisse 53% (gap-down >1% 26% · >2% 12%)
- Excursion ouverture 5min (n=160) : bas méd −0.81% (p90 −2.04%) · haut méd +0.96% · range méd 1.97%
- Excursion ouverture 15min (n=160) : bas méd −0.85% (p90 −2.8%) · haut méd +1.17% · range méd 2.39%
- Excursion ouverture 30min (n=160) : bas méd −1.07% (p90 −3.47%) · haut méd +1.22% · range méd 2.71%
- Excursion ouverture 60min (n=160) : bas méd −1.33% (p90 −3.63%) · haut méd +1.39% · range méd 3.01%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 179.94 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 76% (119/159) · gap 36% · délai 0.0min · rebond 59% (67/119) (MFE +1.23%)
   - −1.0% : fill 30min 54% · séance 66% (109/159) · gap 26% · délai 0.0min · rebond 64% (65/109) (MFE +1.5%)
   - −1.5% : fill 30min 42% · séance 53% (90/159) · gap 20% · délai 0.7min · rebond 65% (57/90) (MFE +1.28%)
   - −2.0% : fill 30min 36% · séance 47% (78/159) · gap 12% · délai 1.9min · rebond 67% (50/78) (MFE +1.39%)
   - −3.0% : fill 30min 21% · séance 30% (56/159) · gap 7% · délai 4.6min · rebond 56% (27/56) (MFE +1.41%)
   - −4.0% : fill 30min 14% · séance 19% (37/159) · gap 4% · délai 13.3min · rebond 48% (17/37) (MFE +0.99%)
   - −5.0% : fill 30min 9% · séance 15% (27/159) · gap 1% · délai 25.2min · rebond 51% (13/27) (MFE +1.03%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.41% (p90 −2.0%) → stop au-delà de −1.25% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.68% (p90 −1.82%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −1.37%) → stop au-delà de −1.05% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=553 jambes) : jambe baissière méd −1.04% (p90 −2.46%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (73 séances) :
      · −1.0% : fill 90% (69/73) · rebond 65% (42/69)
      · −2.0% : fill 72% (56/73) · rebond 66% (35/56)
      · −3.0% : fill 52% (41/73) · rebond 54% (20/41)
      · −4.0% : fill 35% (29/73) · rebond 50% (13/29)
      · −5.0% : fill 29% (23/73) · rebond 58% (12/23)
   - **flat** (27 séances) :
      · −1.0% : fill 73% (23/27) · rebond 42% (11/23)
      · −2.0% : fill 56% (15/27) · rebond 63% (10/15)
      · −3.0% : fill 31% (11/27) · rebond 59% (6/11)
      · −4.0% : fill 18% (7/27) · rebond 44% (4/7)
      · −5.0% : fill 9% (3/27) · rebond 9% (1/3)
   - **gap-up** (59 séances) :
      · −1.0% : fill 33% (17/59) · rebond 80% (12/17)
      · −2.0% : fill 12% (7/59) · rebond 79% (5/7)
      · −3.0% : fill 5% (4/59) · rebond 67% (1/4)
      · −4.0% : fill 1% (1/59) · rebond 0% (0/1)
      · −5.0% : fill 1% (1/59) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 53% en base · 70% si les 15 1res min sont vertes (80 cas) · 34% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:38** → P(séance verte=clôture>ouverture) 84% si début vert vs 24% si rouge (base 53% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **84%** · continue >prix actuel 55% ; creux résiduel méd -0.94% (q20 -1.73%) → **SL/trailing à −1.73%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.4% / q75 +2.22% → **scale +1.4% / runner +2.22%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **24%** (continue à baisser 40%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.58%** (au-delà de la MAE q10 -2.58%), cible rebond +1.32% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.67% .. +3.82%] · haut q95 +4.25% · bas q05 -4.05%
   - 60min (n=160) : retour [-3.62% .. +3.98%] · haut q95 +4.9% · bas q05 -4.38%
   - 2h (n=160) : retour [-3.91% .. +5.61%] · haut q95 +6.6% · bas q05 -4.56%
   - 4h (n=160) : retour [-4.25% .. +5.66%] · haut q95 +6.64% · bas q05 -5.5%
   - 6h (n=160) : retour [-4.6% .. +6.2%] · haut q95 +7.22% · bas q05 -5.61%
   - session (n=160) : retour [-4.24% .. +6.06%] · haut q95 +7.22% · bas q05 -5.63%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 3.1% / strong 3.7%) · base = 11 séances trend-up (n_eff 7.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **41%**. Lecture précoce 30 min : signature présente → 19% vs absente 4% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.86% (p75 1.39% / p90 1.52%) · ~2.55 replis/séance, durée méd 75.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **78%** (reprise méd 33.99 min, n=35)
   - −1.0% → **41%** (reprise méd 64.44 min, n=10)
   - −1.5% → **18%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.52%** (p90, défaut prudent ; serré/agressif −1.39%) ; extension open→close méd +4.67% (q75 +7.59% / q95 +12.13%), MFE méd +6.82% / q90 +12.87%
   - Échelle scale-out : +6.82% (33%) / +8.47% (33%) / +12.87% (34%)
- **DÉSARMER** : repli > **−1.52%** depuis le plus-haut = décay → P(retournement) **64%** (préavis méd 92.5 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.87% : P(retournement après) 0% (mèche méd 1.36%)
- **CONTEXTE** : la dernière heure tient les gains 70% du temps (retour médian dernière heure +0.36%)


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_up
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

- **RSI** : 62.9  _(momentum haussier)_
- **ADX** : 35.0  _(tendance etablie)_
- **MACD** : hist 0.053  _(pas de croisement recent)_
- **BB** : %B 0.78 · largeur 39.1%
- **ATR** : 7.21 (51.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.251  _(accumulation)_
- **Vol ratio** : 0.86  _(volume normal)_
- **Choppiness** : 64.3  _(marche en range (choppy))_
- **MA** : MA20 167.86 · MA50 142.63 · MA200 151.41  _(prix > MA20)_
- **Dist MA** : MA20 +10.8% · MA50 +30.4% · MA200 +22.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (841323 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
