# IONQ

**Generated** : 2026-10-07T00:26:51.262705+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 7/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $43.31  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (2 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot $43.31 (+1.7% vs entrée) · entrée $42.57 · stop $41.73 · T1 $43.97 · R/R 1.67  
> ↳ ¼-Kelly 0.019 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.97% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +0.1 % ≠ (strike 43.0 − spot 43.31)/spot = -0.7 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 7/10 élevée alors que : RSI 72.8 > 70 (surachat) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $42.41–$42.73 (mid $42.57)
- Spot actuel : $43.31 (+1.7% au-dessus de la zone — repli à attendre)
- Stop : $41.73 (plancher anti-bruit (R/R<2) ; -1.97 % depuis l'entree)
- Targets : T1 $43.97 · R/R 1.67 | T2 $45.37 · R/R 3.33 | T3 $46.77 · R/R 5.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $41.73


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=9.02 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.23 %)** : le gap seul le franchit 0.319 % des séances (4 fois sur 1253).
   - exécution **1.463 pt plus bas** dans le cas TYPIQUE (médiane), 8.655 au p90, **11.629 au pire**
   - perte réelle **13.966 %** en moyenne _(tirée par la queue)_, jusqu'à **21.859 %** — au lieu des 10.23 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0119 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.069 % | p01 -6.632 % | pire -21.859 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5284** [0.4541 ; 0.6018] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.525** [0.4723 ; 0.5772] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4941** [0.4416 ; 0.5467] _(largeur 10.5 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.53 %** | CVaR **-10.49 %** | vol 6.09 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 11.45 % contre 5.33 % aujourd'hui, rapport 2.15)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -17.62 % vs -19.57 % si l'on extrapolait par √5 _(rapport 0.901 ; < 1 = le √5 surestime)_
- **β de baisse : 2.229** (β de hausse 2.0023, asymétrie 1.1132) vs IWM — 604 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 38.7769 sur sr_based (1.16 ATR, 10.477 %) — p(stop avant cible) 0.5178 [0.47 ; 0.57], R/R 2.185, perte reelle 10.574 % (gap inclus), CVaR 11.486 %, EV 0.7679 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.3081 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.518, borne haute 0.570 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 1.16 ATR (stop 10.477 %) — p(stop avant cible) 0.5178 [0.47 ; 0.57], R/R 2.185, perte reelle 10.574 % (gap inclus), EV 0.7679 % — **REFUSE**
      - refuse : p_stop_first 0.518, borne haute 0.570 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 3.27 ATR (stop 24.067 %) — p(stop avant cible) 0.1008 [0.07 ; 0.14], R/R 0.959, perte reelle 24.091 % (gap inclus), EV 1.0843 % — **REFUSE**
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.12 % > budget 12.00 %
   - 🟢 support a 4.76 ATR (stop 33.74 %) — p(stop avant cible) 0.0227 [0.01 ; 0.04], R/R 0.684, perte reelle 33.788 % (gap inclus), EV 0.9668 % — **REFUSE**
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.82 % > budget 12.00 %
   - 🟢 support a 6.23 ATR (stop 43.206 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.535, perte reelle 43.207 % (gap inclus), EV 1.0333 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.84 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.615 %) — p(stop avant cible) 0.9043 [0.87 ; 0.93], R/R 13.994, perte reelle 1.651 % (gap inclus), EV 0.3265 % — **REFUSE**
      - refuse : cible atteinte seulement 6.7 % du temps (< 15 %) meme a 10 seances : le R/R de 13.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.904, borne haute 0.932 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 3.229 %) — p(stop avant cible) 0.8322 [0.79 ; 0.87], R/R 6.907, perte reelle 3.345 % (gap inclus), EV 0.3626 % — **REFUSE**
      - refuse : cible atteinte seulement 11.8 % du temps (< 15 %) meme a 10 seances : le R/R de 6.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.832, borne haute 0.869 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 4.844 %) — p(stop avant cible) 0.7806 [0.73 ; 0.82], R/R 4.648, perte reelle 4.971 % (gap inclus), EV -0.0447 % — **REFUSE**
      - refuse : cible atteinte seulement 14.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.781, borne haute 0.822 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 14.1 % x 23.11 % + P(rien) 7.8 % x 7.33 % ne couvrent pas P(stop) 78.1 % x 4.97 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 1.16 ATR (stop 9.437 %) — p(stop avant cible) 0.5815 [0.53 ; 0.63], R/R 2.42, perte reelle 9.548 % (gap inclus), EV 0.5432 % — **REFUSE**
      - refuse : p_stop_first 0.582, borne haute 0.633 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.75 ATR (stop 11.302 %) — p(stop avant cible) 0.485 [0.43 ; 0.54], R/R 2.03, perte reelle 11.381 % (gap inclus), EV 0.5854 % — **REFUSE**
      - refuse : R/R 2.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.07 % > budget 12.00 %
   - ⚪ atr_grid a 2.0 ATR (stop 12.916 %) — p(stop avant cible) 0.4153 [0.36 ; 0.47], R/R 1.779, perte reelle 12.986 % (gap inclus), EV 0.643 % — **REFUSE**
      - refuse : R/R 1.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.50 % > budget 12.00 %
   - ⚪ atr_grid a 2.25 ATR (stop 14.531 %) — p(stop avant cible) 0.3473 [0.30 ; 0.40], R/R 1.579, perte reelle 14.634 % (gap inclus), EV 0.4266 % — **REFUSE**
      - refuse : R/R 1.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.24 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 16.145 %) — p(stop avant cible) 0.2787 [0.23 ; 0.33], R/R 1.424, perte reelle 16.232 % (gap inclus), EV 0.5033 % — **REFUSE**
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.63 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 17.76 %) — p(stop avant cible) 0.239 [0.20 ; 0.29], R/R 1.297, perte reelle 17.819 % (gap inclus), EV 0.7013 % — **REFUSE**
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.04 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 19.375 %) — p(stop avant cible) 0.194 [0.15 ; 0.24], R/R 1.186, perte reelle 19.486 % (gap inclus), EV 0.8873 % — **REFUSE**
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.80 % > budget 12.00 %
   - 🟢 grid_snapped a 3.27 ATR (stop 23.027 %) — p(stop avant cible) 0.128 [0.10 ; 0.17], R/R 1.002, perte reelle 23.067 % (gap inclus), EV 1.0277 % — **REFUSE**
      - refuse : R/R 1.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.13 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 25.833 %) — p(stop avant cible) 0.0839 [0.06 ; 0.12], R/R 0.894, perte reelle 25.853 % (gap inclus), EV 1.0221 % — **REFUSE**
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.87 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 29.062 %) — p(stop avant cible) 0.0624 [0.04 ; 0.09], R/R 0.792, perte reelle 29.163 % (gap inclus), EV 0.8896 % — **REFUSE**
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.19 % > budget 12.00 %
   - 🟢 grid_snapped a 4.76 ATR (stop 32.7 %) — p(stop avant cible) 0.024 [0.01 ; 0.04], R/R 0.705, perte reelle 32.784 % (gap inclus), EV 0.9648 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.49 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 35.52 %) — p(stop avant cible) 0.0132 [0.00 ; 0.03], R/R 0.648, perte reelle 35.651 % (gap inclus), EV 1.0154 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.05 % > budget 12.00 %
   - 🟢 grid_snapped a 6.23 ATR (stop 42.166 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.548, perte reelle 42.166 % (gap inclus), EV 1.035 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.81 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 45.207 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 0.511, perte reelle 45.207 % (gap inclus), EV 1.0328 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.85 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 48.436 %) — p(stop avant cible) 0.0005 [0.00 ; 0.01], R/R 0.477, perte reelle 48.442 % (gap inclus), EV 1.0504 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.69 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 51.665 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.447, perte reelle 51.665 % (gap inclus), EV 1.0649 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.47 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 43.315, ATR14 2.7974 (6.458 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.378 ATR = 2.441 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.323 % | 43.1751 | 93.66 % | 95.36 % | 96.06 % | 97.47 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.646 % | 43.0353 | 85.9 % | 91.03 % | 92.13 % | 94.44 % | 95.83 % | 96.92 % |
| 0.15 ATR | 0.969 % | 42.8954 | 78.65 % | 86.09 % | 88.19 % | 91.41 % | 93.6 % | 95.69 % |
| 0.2 ATR | 1.292 % | 42.7555 | 71.1 % | 80.34 % | 84.16 % | 88.27 % | 90.85 % | 93.63 % |
| 0.25 ATR | 1.615 % | 42.6157 | 65.16 % | 76.21 % | 80.52 % | 85.64 % | 88.72 % | 92.09 % |
| 0.35 ATR | 2.26 % | 42.3359 | 52.77 % | 67.14 % | 73.86 % | 79.07 % | 83.94 % | 88.5 % |
| 0.5 ATR | 3.229 % | 41.9163 | 37.87 % | 54.13 % | 61.86 % | 70.68 % | 78.35 % | 84.6 % |
| 0.75 ATR | 4.844 % | 41.217 | 22.26 % | 38.91 % | 47.93 % | 58.54 % | 68.9 % | 77.0 % |
| 1.0 ATR | 6.458 % | 40.5176 | 10.07 % | 24.4 % | 34.41 % | 45.6 % | 57.83 % | 68.38 % |
| 1.25 ATR | 8.073 % | 39.8183 | 3.83 % | 14.31 % | 23.92 % | 34.58 % | 50.0 % | 62.01 % |
| 1.5 ATR | 9.687 % | 39.119 | 1.11 % | 7.06 % | 15.54 % | 25.28 % | 40.96 % | 56.26 % |
| 2.0 ATR | 12.916 % | 37.7203 | 0.1 % | 1.92 % | 4.94 % | 14.05 % | 28.05 % | 45.28 % |
| 2.5 ATR | 16.145 % | 36.3216 | 0.0 % | 0.2 % | 1.21 % | 5.66 % | 17.99 % | 34.29 % |
| 3.0 ATR | 19.375 % | 34.9229 | 0.0 % | 0.1 % | 0.4 % | 2.53 % | 11.28 % | 25.87 % |
| 4.0 ATR | 25.833 % | 32.1256 | 0.0 % | 0.1 % | 0.1 % | 0.2 % | 2.95 % | 10.57 % |
| 6.0 ATR | 38.749 % | 26.5309 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.1 % | 1.23 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.38 ATR | 0.43 ATR | 0.58 ATR | 0.71 ATR | 0.80 ATR | 1.00 ATR | 1.20 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.65 ATR | 0.85 ATR | 0.99 ATR | 1.11 ATR | 1.40 ATR | 1.70 ATR |
| **3 s.** | 0.33 ATR | 0.71 ATR | 0.80 ATR | 1.03 ATR | 1.22 ATR | 1.37 ATR | 1.76 ATR | 2.00 ATR |
| **5 s.** | 0.42 ATR | 0.92 ATR | 1.01 ATR | 1.29 ATR | 1.51 ATR | 1.74 ATR | 2.24 ATR | 2.60 ATR |
| **10 s.** | 0.59 ATR | 1.25 ATR | 1.39 ATR | 1.81 ATR | 2.15 ATR | 2.40 ATR | 3.15 ATR | 3.75 ATR |
| **20 s.** | 0.81 ATR | 1.78 ATR | 2.01 ATR | 2.58 ATR | 3.06 ATR | 3.38 ATR | 4.12 ATR | 5.19 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.428–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.65–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.844 %, prix 41.2168), p(touche) 38.91 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.804–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.458 %, prix 40.5177), p(touche) 34.41 % (en stress 92.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.014–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.073 %, prix 39.8182), p(touche) 34.58 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.388–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.687 %, prix 39.1191), p(touche) 40.96 % (en stress 97.98 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.013–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (16.145 %, prix 36.3218), p(touche) 34.29 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (67.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.061 | EV/share : $0.051 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 — | T3 —
- Kelly (position) : f* 0.077 | ¼-Kelly 0.019 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 80.8 | bear 5.0 | side 14.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 386.0 (= 10 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.713% → cible +3.285% / stop −1.971%, p_fill 59%, n_eff≈68.1) : P(cible|rempli) **29%** · **EV/risk -0.048** (×p_fill ; si rempli -0.16% du capital)
  - **swing** (entrée dip −3.772% → cible +8.709% / stop −6.711%, p_fill 56%, n_eff≈66.7) : P(cible|rempli) **41%** · **EV/risk -0.025** (×p_fill ; si rempli -0.30% du capital)
  - **deep** (entrée dip −5.822% → cible +11.083% / stop −10.286%, p_fill 56%, n_eff≈63.0) : P(cible|rempli) **44%** · **EV/risk -0.047** (×p_fill ; si rempli -0.87% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→87% · +1.0%→80% · +2.0%→64% · +3.0%→54% · +5.0%→28% · +8.0%→13%
- Range intraday médian 7.05% (p90 11.57%) · excursion haute méd. +3.57% / basse méd. −2.49%
- Profil de vol intra : ouverture 4.841% vs midi 1.378% vs clôture 1.552% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 22% · trend ↑0%/↓0% ; spike-down 62% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.122 ; neutre — autocorr 0.011)_ ; drift intra méd. -0.232% ; recovery-V 26%
- **σ réalisé intraday** 4.05% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 57% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 44.6406 (VA 44.2714–45.1154 ; dernier close 43.77)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 25% · rebond 78% · **stop −4.38%** sous le fill (sous le bruit) · cible +2.22% · R/R 0.51 (high win-rate)
- Gaps overnight (n=159) : méd. 0.03% · baisse 49% (gap-down >1% 34% · >2% 21%)
- Excursion ouverture 5min (n=160) : bas méd −1.0% (p90 −2.73%) · haut méd +1.28% · range méd 2.57%
- Excursion ouverture 15min (n=160) : bas méd −1.18% (p90 −3.76%) · haut méd +1.47% · range méd 3.38%
- Excursion ouverture 30min (n=160) : bas méd −1.31% (p90 −4.62%) · haut méd +1.81% · range méd 4.16%
- Excursion ouverture 60min (n=160) : bas méd −1.57% (p90 −5.28%) · haut méd +1.87% · range méd 4.67%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 43.77 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 76% (126/159) · gap 43% · délai 0.0min · rebond 61% (83/126) (MFE +1.81%)
   - −1.0% : fill 30min 60% · séance 70% (119/159) · gap 34% · délai 0.0min · rebond 67% (85/119) (MFE +1.91%)
   - −1.5% : fill 30min 53% · séance 65% (112/159) · gap 30% · délai 0.0min · rebond 70% (78/112) (MFE +2.06%)
   - −2.0% : fill 30min 46% · séance 54% (100/159) · gap 21% · délai 0.0min · rebond 69% (70/100) (MFE +2.17%)
   - −3.0% : fill 30min 37% · séance 43% (81/159) · gap 10% · délai 4.1min · rebond 70% (59/81) (MFE +2.38%)
   - −4.0% : fill 30min 22% · séance 33% (64/159) · gap 4% · délai 15.3min · rebond 69% (48/64) (MFE +2.23%)
   - −5.0% : fill 30min 11% · séance 25% (50/159) · gap 1% · délai 32.0min · rebond 78% (41/50) (MFE +2.22%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.75% (p90 −2.62%) → stop au-delà de −1.83% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.76% (p90 −2.65%) → stop au-delà de −1.69% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.68% (p90 −2.35%) → stop au-delà de −1.31% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1047 jambes) : jambe baissière méd −1.26% (p90 −2.97%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (80 séances) :
      · −1.0% : fill 100% (80/80) · rebond 69% (56/80)
      · −2.0% : fill 87% (73/80) · rebond 75% (54/73)
      · −3.0% : fill 72% (61/80) · rebond 72% (44/61)
      · −4.0% : fill 54% (47/80) · rebond 67% (34/47)
      · −5.0% : fill 38% (37/80) · rebond 70% (28/37)
   - **flat** (15 séances) :
      · −1.0% : fill 62% (10/15) · rebond 84% (9/10)
      · −2.0% : fill 43% (8/15) · rebond 90% (6/8)
      · −3.0% : fill 27% (5/15) · rebond 64% (4/5)
      · −4.0% : fill 23% (4/15) · rebond 57% (3/4)
      · −5.0% : fill 16% (3/15) · rebond 100% (3/3)
   - **gap-up** (64 séances) :
      · −1.0% : fill 41% (29/64) · rebond 55% (20/29)
      · −2.0% : fill 22% (19/64) · rebond 31% (10/19)
      · −3.0% : fill 15% (15/64) · rebond 60% (11/15)
      · −4.0% : fill 14% (13/64) · rebond 84% (11/13)
      · −5.0% : fill 12% (10/64) · rebond 100% (10/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 59% si les 15 1res min sont vertes (90 cas) · 26% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **56min** → P(séance verte=clôture>ouverture) 66% si début vert vs 19% si rouge (base 46% · écart 47 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=86) : tient le vert **66%** · continue >prix actuel 38% ; creux résiduel méd -1.76% (q20 -4.14%) → **SL/trailing à −4.14%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.64% / q75 +3.31% → **scale +1.64% / runner +3.31%**, sortie à la clôture
  - **si ROUGE au coude** (n=74) : edge inversé — récupère vert seulement **19%** (continue à baisser 59%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.23%** (au-delà de la MAE q10 -4.23%), cible rebond +1.94% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.23% .. +5.46%] · haut q95 +7.35% · bas q05 -5.49%
   - 60min (n=160) : retour [-5.25% .. +5.86%] · haut q95 +7.69% · bas q05 -6.74%
   - 2h (n=160) : retour [-6.37% .. +5.93%] · haut q95 +8.07% · bas q05 -7.06%
   - 4h (n=160) : retour [-6.75% .. +6.86%] · haut q95 +8.75% · bas q05 -7.93%
   - 6h (n=160) : retour [-6.62% .. +7.19%] · haut q95 +9.75% · bas q05 -7.92%
   - session (n=160) : retour [-6.36% .. +8.14%] · haut q95 +9.8% · bas q05 -8.19%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 7.5% des séances sont trend-up (mild 0% / strong 7.5%) · base = 12 séances trend-up (n_eff 7.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **35%**. Lecture précoce 30 min : signature présente → 13% vs absente 5% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.3% (p75 2.44% / p90 3.18%) · ~4.0 replis/séance, durée méd 70.31 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 30.0 min, n=48)
   - −1.0% → **77%** (reprise méd 34.75 min, n=35)
   - −1.5% → **67%** (reprise méd 44.94 min, n=18)
   - −2.0% → **61%** (reprise méd 64.1 min, n=13)
   - −3.0% → **74%** (reprise méd 175.76 min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−3.18%** (p90, défaut prudent ; serré/agressif −2.44%) ; extension open→close méd +8.16% (q75 +8.39% / q95 +13.57%), MFE méd +9.48% / q90 +12.4%
   - Échelle scale-out : +9.48% (33%) / +10.45% (33%) / +12.4% (34%)
- **DÉSARMER** : repli > **−3.18%** depuis le plus-haut = décay → P(retournement) **26%** (préavis méd 167.77 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.4% : P(retournement après) 0% (mèche méd 2.07%)
- **CONTEXTE** : la dernière heure tient les gains 70% du temps (retour médian dernière heure +0.1%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.5 · part idiosyncratique 0.5
**Short/Insider** : SI —% | insider — | verdict sell_bias_modere
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 72.8  _(surachat)_
- **ADX** : 22.8  _(pas de tendance nette)_
- **MACD** : hist 0.246  _(pas de croisement recent)_
- **BB** : %B 0.67 · largeur 30.4%
- **ATR** : 2.8 (21.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.27  _(distribution)_
- **Vol ratio** : 0.63  _(volume normal)_
- **Choppiness** : 51.2  _(transition)_
- **MA** : MA20 41.16 · MA50 40.95 · MA200 43.41  _(prix > MA20)_
- **Dist MA** : MA20 +5.2% · MA50 +5.8% · MA200 -0.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (532657 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
