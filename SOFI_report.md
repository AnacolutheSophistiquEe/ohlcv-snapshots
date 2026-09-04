# SOFI

**Generated** : 2026-09-04T00:37:14.740617+00:00  
**Santé technique** : 9/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $18.50  

> 🟡 **WAIT-FOR-DIP** — spot +3.4 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $18.50 (+3.4% vs entrée) · entrée $17.90 · stop $17.59 · T1 $18.52 · R/R 2.0  
> ↳ P(T1 av. stop) 44 % · EV/risk 0.167 · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.73% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +0.9 % ≠ (strike 18.0 − spot 18.50)/spot = -2.7 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 9/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $17.84–$17.97 (mid $17.90)
- Spot actuel : $18.50 (+3.4% au-dessus de la zone — repli à attendre)
- Stop : $17.59 (stop swing_plan-based (-12.71%))
- Targets : T1 $18.52 · R/R 2.0 | T2 $18.70 · R/R 2.58 | T3 $18.88 · R/R 3.16
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $17.59


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=5.99 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.71 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1253).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 12.71 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.268 % | p01 -6.52 % | pire -11.105 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5467** [0.4723 ; 0.6196] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4204** [0.3692 ; 0.4729] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.3583** [0.3091 ; 0.4099] _(largeur 10.1 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (57.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1080 séances)** : VaR **-5.98 %** | CVaR **-8.45 %** | vol 3.98 %/j
   - _fenêtre arrêtée : rupture de regime a 1140 seances en arriere (volatilite 5.86 % contre 3.54 % aujourd'hui, rapport 1.65)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.5 % vs -14.19 % si l'on extrapolait par √5 _(rapport 1.021 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8204** (β de hausse 1.7072, asymétrie 1.0663) vs IWM — 602 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.33× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 16.4238 sur atr_grid (2.25 ATR, 11.247 %) — p(stop avant cible) 0.2914 [0.25 ; 0.34], R/R 3.2, perte reelle 11.247 % (gap inclus), CVaR 11.247 %, EV -0.2084 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 1.14 ATR (stop 8.123 %) — p(stop avant cible) 0.4234 [0.37 ; 0.48], R/R 3.707, perte reelle 9.707 % (gap inclus), EV -0.814 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.81 %) : P(cible) 0.2 % x 35.99 % + P(rien) 57.5 % x 5.62 % ne couvrent pas P(stop) 42.3 % x 9.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 2.7 ATR (stop 15.933 %) — p(stop avant cible) 0.1059 [0.08 ; 0.14], R/R 2.259, perte reelle 15.933 % (gap inclus), EV 0.4464 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.93 % > budget 12.00 %
   - 🟢 support a 3.92 ATR (stop 22.038 %) — p(stop avant cible) 0.0359 [0.02 ; 0.06], R/R 1.633, perte reelle 22.038 % (gap inclus), EV 0.3806 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.04 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.25 %) — p(stop avant cible) 0.921 [0.89 ; 0.95], R/R 13.082, perte reelle 2.751 % (gap inclus), EV -1.4603 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 13.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.921, borne haute 0.946 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.46 %) : P(cible) 0.1 % x 35.99 % + P(rien) 7.8 % x 13.27 % ne couvrent pas P(stop) 92.1 % x 2.75 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.499 %) — p(stop avant cible) 0.8429 [0.80 ; 0.88], R/R 8.389, perte reelle 4.29 % (gap inclus), EV -1.9076 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 8.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.843, borne haute 0.878 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.91 %) : P(cible) 0.1 % x 35.99 % + P(rien) 15.6 % x 10.65 % ne couvrent pas P(stop) 84.3 % x 4.29 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 3.749 %) — p(stop avant cible) 0.7235 [0.67 ; 0.77], R/R 6.271, perte reelle 5.739 % (gap inclus), EV -1.5995 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 6.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.724, borne haute 0.769 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.60 %) : P(cible) 0.2 % x 35.99 % + P(rien) 27.5 % x 9.08 % ne couvrent pas P(stop) 72.4 % x 5.74 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.14 ATR (stop 7.174 %) — p(stop avant cible) 0.4718 [0.42 ; 0.52], R/R 4.005, perte reelle 8.985 % (gap inclus), EV -0.8902 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.89 %) : P(cible) 0.2 % x 35.99 % + P(rien) 52.6 % x 6.24 % ne couvrent pas P(stop) 47.2 % x 8.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 9.997 %) — p(stop avant cible) 0.356 [0.31 ; 0.41], R/R 3.241, perte reelle 11.105 % (gap inclus), EV -0.7275 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.73 %) : P(cible) 0.2 % x 35.99 % + P(rien) 64.2 % x 4.92 % ne couvrent pas P(stop) 35.6 % x 11.11 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 11.247 %) — p(stop avant cible) 0.2914 [0.25 ; 0.34], R/R 3.2, perte reelle 11.247 % (gap inclus), EV -0.2084 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.21 %) : P(cible) 0.2 % x 35.99 % + P(rien) 70.7 % x 4.25 % ne couvrent pas P(stop) 29.1 % x 11.25 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.7 ATR (stop 14.984 %) — p(stop avant cible) 0.1329 [0.10 ; 0.17], R/R 2.402, perte reelle 14.984 % (gap inclus), EV 0.3639 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.98 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 17.495 %) — p(stop avant cible) 0.0695 [0.05 ; 0.10], R/R 2.057, perte reelle 17.495 % (gap inclus), EV 0.4767 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.50 % > budget 12.00 %
   - 🟢 grid_snapped a 3.92 ATR (stop 21.089 %) — p(stop avant cible) 0.0379 [0.02 ; 0.06], R/R 1.706, perte reelle 21.089 % (gap inclus), EV 0.4092 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.09 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 24.993 %) — p(stop avant cible) 0.0198 [0.01 ; 0.04], R/R 1.44, perte reelle 24.993 % (gap inclus), EV 0.4357 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.99 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 27.492 %) — p(stop avant cible) 0.004 [0.00 ; 0.02], R/R 1.309, perte reelle 27.492 % (gap inclus), EV 0.5294 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.49 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 29.992 %) — p(stop avant cible) 0.0031 [0.00 ; 0.01], R/R 1.2, perte reelle 29.992 % (gap inclus), EV 0.5335 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.99 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 32.491 %) — p(stop avant cible) 0.0023 [0.00 ; 0.01], R/R 1.108, perte reelle 32.491 % (gap inclus), EV 0.5442 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.49 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 34.99 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 1.029, perte reelle 34.99 % (gap inclus), EV 0.5452 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.99 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 37.49 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.96, perte reelle 37.49 % (gap inclus), EV 0.5537 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.49 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 39.989 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.9, perte reelle 39.989 % (gap inclus), EV 0.5537 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.99 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 18.505, ATR14 0.925 (4.999 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.375 ATR = 1.874 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.25 % | 18.4587 | 92.85 % | 95.77 % | 96.97 % | 97.37 % | 98.27 % | 98.87 % |
| 0.1 ATR | 0.5 % | 18.4125 | 85.2 % | 89.52 % | 91.93 % | 93.23 % | 95.53 % | 97.13 % |
| 0.15 ATR | 0.75 % | 18.3663 | 79.05 % | 84.98 % | 88.19 % | 90.39 % | 92.78 % | 94.76 % |
| 0.2 ATR | 1.0 % | 18.32 | 71.6 % | 79.74 % | 83.55 % | 86.86 % | 90.45 % | 93.22 % |
| 0.25 ATR | 1.25 % | 18.2738 | 66.26 % | 75.2 % | 80.12 % | 84.13 % | 88.82 % | 91.79 % |
| 0.35 ATR | 1.75 % | 18.1813 | 52.47 % | 65.52 % | 72.15 % | 78.26 % | 85.26 % | 88.5 % |
| 0.5 ATR | 2.499 % | 18.0425 | 37.66 % | 53.53 % | 61.65 % | 68.96 % | 79.17 % | 84.29 % |
| 0.75 ATR | 3.749 % | 17.8113 | 20.24 % | 36.79 % | 47.02 % | 56.93 % | 69.61 % | 77.41 % |
| 1.0 ATR | 4.999 % | 17.58 | 8.86 % | 24.29 % | 33.8 % | 44.99 % | 59.25 % | 68.58 % |
| 1.25 ATR | 6.248 % | 17.3488 | 4.13 % | 14.92 % | 23.71 % | 35.49 % | 49.9 % | 61.81 % |
| 1.5 ATR | 7.498 % | 17.1175 | 2.01 % | 9.48 % | 16.75 % | 27.5 % | 41.77 % | 55.24 % |
| 2.0 ATR | 9.997 % | 16.655 | 0.7 % | 4.33 % | 8.38 % | 15.37 % | 28.96 % | 44.87 % |
| 2.5 ATR | 12.497 % | 16.1925 | 0.3 % | 1.92 % | 3.83 % | 9.5 % | 19.61 % | 35.52 % |
| 3.0 ATR | 14.996 % | 15.73 | 0.1 % | 0.91 % | 2.83 % | 6.07 % | 13.92 % | 28.13 % |
| 4.0 ATR | 19.994 % | 14.805 | 0.0 % | 0.3 % | 0.71 % | 2.53 % | 7.42 % | 14.68 % |
| 6.0 ATR | 29.992 % | 12.955 | 0.0 % | 0.1 % | 0.2 % | 0.2 % | 0.91 % | 3.08 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.68 ATR | 0.76 ATR | 0.97 ATR | 1.20 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.63 ATR | 0.83 ATR | 0.99 ATR | 1.11 ATR | 1.48 ATR | 1.94 ATR |
| **3 s.** | 0.31 ATR | 0.70 ATR | 0.79 ATR | 1.02 ATR | 1.22 ATR | 1.38 ATR | 1.90 ATR | 2.37 ATR |
| **5 s.** | 0.40 ATR | 0.90 ATR | 1.00 ATR | 1.33 ATR | 1.60 ATR | 1.81 ATR | 2.46 ATR | 3.30 ATR |
| **10 s.** | 0.61 ATR | 1.25 ATR | 1.40 ATR | 1.84 ATR | 2.21 ATR | 2.48 ATR | 3.60 ATR | 4.74 ATR |
| **20 s.** | 0.82 ATR | 1.75 ATR | 1.99 ATR | 2.67 ATR | 3.23 ATR | 3.60 ATR | 4.81 ATR | 5.67 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.426–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.499 %, prix 18.0426), p(touche) 37.66 % (en stress 84.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.627–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.749 %, prix 17.8112), p(touche) 36.79 % (en stress 91.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 17.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.788–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.999 %, prix 17.5799), p(touche) 33.8 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.0–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.999 %, prix 17.5799), p(touche) 44.99 % (en stress 97.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.401–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.498 %, prix 17.1175), p(touche) 41.77 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.994–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (9.997 %, prix 16.6551), p(touche) 44.87 % (en stress 98.98 %)  ✅ optimum identifie (73.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.039 | EV/share : $-0.012 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 24 % | T2 18 % | T3 12 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 52.8 | bear 11.7 | side 35.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 278.0 (= 15 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.243% → cible +3.467% / stop −1.733%, p_fill 24%, n_eff≈9.0) : P(cible|rempli) **12%** · **EV/risk -0.030** (×p_fill ; si rempli -0.21% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=5, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=4, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→69% · +2.0%→49% · +3.0%→36% · +5.0%→12% · +8.0%→1%
- Range intraday médian 4.39% (p90 7.54%) · excursion haute méd. +1.83% / basse méd. −2.18%
- Profil de vol intra : ouverture 3.045% vs midi 0.853% vs clôture 0.992% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 15% · trend ↑2%/↓0% ; spike-down 63% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.147 ; mean-reverting — autocorr -0.043)_ ; drift intra méd. -0.255% ; recovery-V 26%
- **σ réalisé intraday** 2.625% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 60% / whipsaw 13%
- POC intraday (dernière séance, temps-au-prix) : 17.1559 (VA 17.0219–17.3066 ; dernier close 17.06)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 48% · rebond 66% · **stop −3.09%** sous le fill (sous le bruit) · cible +1.78% · R/R 0.58 (high win-rate)
- Gaps overnight (n=159) : méd. 0.24% · baisse 44% (gap-down >1% 24% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −1.76%) · haut méd +0.71% · range méd 1.64%
- Excursion ouverture 15min (n=160) : bas méd −1.0% (p90 −2.75%) · haut méd +0.99% · range méd 2.29%
- Excursion ouverture 30min (n=160) : bas méd −1.12% (p90 −3.2%) · haut méd +1.11% · range méd 2.66%
- Excursion ouverture 60min (n=160) : bas méd −1.42% (p90 −3.7%) · haut méd +1.3% · range méd 3.29%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 17.05 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 74% (120/159) · gap 31% · délai 0.0min · rebond 51% (63/120) (MFE +1.13%)
   - −1.0% : fill 30min 53% · séance 66% (109/159) · gap 24% · délai 1.4min · rebond 55% (63/109) (MFE +1.01%)
   - −1.5% : fill 30min 42% · séance 62% (100/159) · gap 20% · délai 9.8min · rebond 64% (66/100) (MFE +1.39%)
   - −2.0% : fill 30min 35% · séance 48% (79/159) · gap 10% · délai 9.8min · rebond 66% (54/79) (MFE +1.78%)
   - −3.0% : fill 30min 12% · séance 34% (57/159) · gap 3% · délai 50.3min · rebond 54% (37/57) (MFE +1.08%)
   - −4.0% : fill 30min 8% · séance 18% (36/159) · gap 2% · délai 48.8min · rebond 52% (23/36) (MFE +1.2%)
   - −5.0% : fill 30min 3% · séance 10% (20/159) · gap 2% · délai 192.2min · rebond 44% (10/20) (MFE +0.72%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.44% (p90 −1.91%) → stop au-delà de −1.39% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.48% (p90 −2.07%) → stop au-delà de −1.42% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.47% (p90 −1.46%) → stop au-delà de −1.21% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=673 jambes) : jambe baissière méd −1.08% (p90 −2.77%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (66 séances) :
      · −1.0% : fill 98% (65/66) · rebond 54% (39/65)
      · −2.0% : fill 85% (55/66) · rebond 71% (39/55)
      · −3.0% : fill 66% (42/66) · rebond 57% (28/42)
      · −4.0% : fill 37% (28/66) · rebond 60% (20/28)
      · −5.0% : fill 22% (16/66) · rebond 54% (9/16)
   - **flat** (21 séances) :
      · −1.0% : fill 66% (12/21) · rebond 42% (5/12)
      · −2.0% : fill 45% (7/21) · rebond 55% (4/7)
      · −3.0% : fill 35% (6/21) · rebond 38% (3/6)
      · −4.0% : fill 22% (3/21) · rebond 30% (1/3)
      · −5.0% : fill 13% (1/21) · rebond 0% (0/1)
   - **gap-up** (72 séances) :
      · −1.0% : fill 42% (32/72) · rebond 62% (19/32)
      · −2.0% : fill 21% (17/72) · rebond 58% (11/17)
      · −3.0% : fill 11% (9/72) · rebond 60% (6/9)
      · −4.0% : fill 3% (5/72) · rebond 22% (2/5)
      · −5.0% : fill 1% (3/72) · rebond 44% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 41% en base · 61% si les 15 1res min sont vertes (74 cas) · 25% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **52min** → P(séance verte=clôture>ouverture) 79% si début vert vs 12% si rouge (base 41% · écart 67 pts) ; prédictivité sature ensuite (plafond brut 228min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=67) : tient le vert **79%** · continue >prix actuel 56% ; creux résiduel méd -1.09% (q20 -2.26%) → **SL/trailing à −2.26%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.38% / q75 +2.95% → **scale +1.38% / runner +2.95%**, sortie à la clôture
  - **si ROUGE au coude** (n=93) : edge inversé — récupère vert seulement **12%** (continue à baisser 54%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.24%** (au-delà de la MAE q10 -3.24%), cible rebond +1.13% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.89% .. +3.71%] · haut q95 +4.01% · bas q05 -3.39%
   - 60min (n=160) : retour [-3.13% .. +3.69%] · haut q95 +4.52% · bas q05 -4.0%
   - 2h (n=160) : retour [-3.58% .. +3.9%] · haut q95 +5.22% · bas q05 -4.62%
   - 4h (n=160) : retour [-4.48% .. +4.59%] · haut q95 +5.68% · bas q05 -5.14%
   - 6h (n=160) : retour [-4.76% .. +4.07%] · haut q95 +5.7% · bas q05 -5.75%
   - session (n=160) : retour [-4.69% .. +5.05%] · haut q95 +5.7% · bas q05 -5.97%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.9%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 51.3  _(neutre)_
- **ADX** : 13.9  _(pas de tendance nette)_
- **MACD** : hist -0.079  _(bearish_recent)_
- **BB** : %B 0.63 · largeur 11.0%
- **ATR** : 0.92 (34.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.109  _(distribution)_
- **Vol ratio** : 0.93  _(volume normal)_
- **Choppiness** : 61.2  _(transition)_
- **MA** : MA20 18.25 · MA50 17.86 · MA200 20.01  _(prix > MA20)_
- **Dist MA** : MA20 +1.4% · MA50 +3.6% · MA200 -7.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (751951 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
