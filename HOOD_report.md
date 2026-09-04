# HOOD

**Generated** : 2026-09-04T00:35:44.985054+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $124.71  

> 🟡 **WAIT-FOR-DIP** — spot +2.0 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $124.71 (+2.0% vs entrée) · entrée $122.23 · stop $116.12 · T1 $125.91 · R/R 0.6  
> ↳ P(T1 av. stop) 45 % _(réel 5 s)_ · EV/risk 0.058 _(réel 5 s)_ (GBM 0.002) · ¼-Kelly 0.035 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −5.0% cohérent avec le bruit 5 s (EV-optimal ≈ −5.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -1.9 % ≠ (strike 105.0 − spot 124.71)/spot = -15.8 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : RSI 70.9 > 70 (surachat) ; %B 1.19 (collé à la bande haute) ; extension extrême (≥3×ATR, confluence MA20/50) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $121.49–$122.96 (mid $122.23)
- Spot actuel : $124.71 (+2.0% au-dessus de la zone — repli à attendre)
- Stop : $116.12 (stop swing_plan-based (-12.97%))
- Targets : T1 $125.91 · R/R 0.6 | T2 $129.59 · R/R 1.2 | T3 $133.27 · R/R 1.81
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $116.12


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.02 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.97 %)** : le gap seul le franchit 0.16 % des séances (2 fois sur 1253).
   - exécution **2.985 pt plus bas** dans le cas TYPIQUE (médiane), 4.449 au p90, **4.815 au pire**
   - perte réelle **15.955 %** en moyenne _(tirée par la queue)_, jusqu'à **17.785 %** — au lieu des 12.97 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0048 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 2 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.437 % | p01 -7.308 % | pire -17.785 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1287** [0.0851 ; 0.1846] _(largeur 10.0 pt, n_eff 173.1)_
   - swing : **0.2688** [0.2241 ; 0.3173] _(largeur 9.3 pt, n_eff 345.7)_
   - deep : **0.3821** [0.332 ; 0.4341] _(largeur 10.2 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (37.8 pt), swing (46.3 pt), deep (45.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-6.19 %** | CVaR **-9.11 %** | vol 4.38 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 2.14 % contre 4.70 % aujourd'hui, rapport 0.46)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.55 % vs -14.36 % si l'on extrapolait par √5 _(rapport 1.013 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7674** (β de hausse 1.5949, asymétrie 1.1081) vs IWM — 602 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.491× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 110.505 sur sr_based (1.47 ATR, 11.39 %) — p(stop avant cible) 0.3181 [0.27 ; 0.37], R/R 1.388, perte reelle 14.605 % (gap inclus), CVaR 11.398 %, EV 1.3832 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 1.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 15 des 15 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 65.4 % de la queue et il ne reste que -955.87 EUR a partager. Prix du risque -0.692 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 8.725 %) — p(stop avant cible) 0.4254 [0.37 ; 0.48], R/R 1.748, perte reelle 11.595 % (gap inclus), EV 0.9489 % — **REFUSE**
      - refuse : R/R 1.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 1.47 ATR (stop 11.39 %) — p(stop avant cible) 0.3181 [0.27 ; 0.37], R/R 1.388, perte reelle 14.605 % (gap inclus), EV 1.3832 % — **REFUSE**
      - refuse : R/R 1.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 3.12 ATR (stop 20.98 %) — p(stop avant cible) 0.0812 [0.06 ; 0.11], R/R 0.966, perte reelle 20.98 % (gap inclus), EV 2.5722 % — **REFUSE**
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.98 % > budget 12.00 %
   - ⚪ swing_based a 3.51 ATR (stop 23.282 %) — p(stop avant cible) 0.0462 [0.03 ; 0.07], R/R 0.871, perte reelle 23.282 % (gap inclus), EV 2.6252 % — **REFUSE**
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.28 % > budget 12.00 %
   - 🟢 support a 4.59 ATR (stop 29.528 %) — p(stop avant cible) 0.0249 [0.01 ; 0.05], R/R 0.686, perte reelle 29.528 % (gap inclus), EV 2.6254 % — **REFUSE**
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.53 % > budget 12.00 %
   - 🟢 support a 8.44 ATR (stop 51.92 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.39, perte reelle 51.92 % (gap inclus), EV 2.7864 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 51.92 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.454 %) — p(stop avant cible) 0.8935 [0.86 ; 0.92], R/R 6.328, perte reelle 3.203 % (gap inclus), EV -1.2252 % — **REFUSE**
      - refuse : cible atteinte seulement 5.8 % du temps (< 15 %) meme a 10 seances : le R/R de 6.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.893, borne haute 0.923 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.23 %) : P(cible) 5.8 % x 20.27 % + P(rien) 4.8 % x 9.42 % ne couvrent pas P(stop) 89.3 % x 3.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.908 %) — p(stop avant cible) 0.7741 [0.73 ; 0.82], R/R 4.104, perte reelle 4.939 % (gap inclus), EV -0.5813 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 4.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.774, borne haute 0.816 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.58 %) : P(cible) 10.7 % x 20.27 % + P(rien) 11.9 % x 9.03 % ne couvrent pas P(stop) 77.4 % x 4.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 4.362 %) — p(stop avant cible) 0.6759 [0.63 ; 0.72], R/R 2.869, perte reelle 7.064 % (gap inclus), EV -0.4545 % — **REFUSE**
      - refuse : cible atteinte seulement 14.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.676, borne haute 0.724 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.45 %) : P(cible) 14.1 % x 20.27 % + P(rien) 18.4 % x 8.01 % ne couvrent pas P(stop) 67.6 % x 7.06 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 5.816 %) — p(stop avant cible) 0.5942 [0.54 ; 0.65], R/R 2.165, perte reelle 9.362 % (gap inclus), EV -0.5017 % — **REFUSE**
      - refuse : p_stop_first 0.594, borne haute 0.645 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.50 %) : P(cible) 16.2 % x 20.27 % + P(rien) 24.4 % x 7.29 % ne couvrent pas P(stop) 59.4 % x 9.36 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.47 ATR (stop 10.285 %) — p(stop avant cible) 0.3676 [0.32 ; 0.42], R/R 1.595, perte reelle 12.711 % (gap inclus), EV 1.3313 % — **REFUSE**
      - refuse : R/R 1.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 13.087 %) — p(stop avant cible) 0.2632 [0.22 ; 0.31], R/R 1.27, perte reelle 15.955 % (gap inclus), EV 1.7645 % — **REFUSE**
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.09 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 14.541 %) — p(stop avant cible) 0.2094 [0.17 ; 0.25], R/R 1.14, perte reelle 17.785 % (gap inclus), EV 1.9475 % — **REFUSE**
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.54 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 15.995 %) — p(stop avant cible) 0.1824 [0.14 ; 0.23], R/R 1.14, perte reelle 17.785 % (gap inclus), EV 2.1543 % — **REFUSE**
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.00 % > budget 12.00 %
   - 🟢 grid_snapped a 3.12 ATR (stop 19.875 %) — p(stop avant cible) 0.088 [0.06 ; 0.12], R/R 1.02, perte reelle 19.875 % (gap inclus), EV 2.6011 % — **REFUSE**
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.88 % > budget 12.00 %
   - ⚪ grid_snapped a 3.51 ATR (stop 22.177 %) — p(stop avant cible) 0.0632 [0.04 ; 0.09], R/R 0.914, perte reelle 22.177 % (gap inclus), EV 2.6252 % — **REFUSE**
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.18 % > budget 12.00 %
   - 🟢 grid_snapped a 4.59 ATR (stop 28.423 %) — p(stop avant cible) 0.027 [0.01 ; 0.05], R/R 0.713, perte reelle 28.423 % (gap inclus), EV 2.6168 % — **REFUSE**
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.42 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 31.99 %) — p(stop avant cible) 0.0136 [0.01 ; 0.03], R/R 0.634, perte reelle 31.99 % (gap inclus), EV 2.663 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.99 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 34.898 %) — p(stop avant cible) 0.0033 [0.00 ; 0.01], R/R 0.581, perte reelle 34.898 % (gap inclus), EV 2.7581 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.90 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 37.806 %) — p(stop avant cible) 0.0021 [0.00 ; 0.01], R/R 0.536, perte reelle 37.806 % (gap inclus), EV 2.7644 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.81 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 40.714 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.498, perte reelle 40.714 % (gap inclus), EV 2.7864 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.71 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 43.623 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.465, perte reelle 43.623 % (gap inclus), EV 2.7864 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.62 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 46.531 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.436, perte reelle 46.531 % (gap inclus), EV 2.7864 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.53 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 124.71, ATR14 7.2536 (5.816 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.373 ATR = 2.169 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.291 % | 124.3473 | 92.95 % | 94.96 % | 95.86 % | 96.36 % | 96.95 % | 97.95 % |
| 0.1 ATR | 0.582 % | 123.9846 | 85.6 % | 90.22 % | 91.93 % | 93.43 % | 94.51 % | 96.3 % |
| 0.15 ATR | 0.872 % | 123.622 | 77.74 % | 84.98 % | 87.69 % | 89.89 % | 92.28 % | 94.87 % |
| 0.2 ATR | 1.163 % | 123.2593 | 71.7 % | 79.84 % | 83.45 % | 86.55 % | 90.04 % | 93.12 % |
| 0.25 ATR | 1.454 % | 122.8966 | 64.65 % | 74.19 % | 78.91 % | 83.01 % | 87.4 % | 90.76 % |
| 0.35 ATR | 2.036 % | 122.1712 | 52.37 % | 65.12 % | 71.64 % | 77.25 % | 83.03 % | 87.89 % |
| 0.5 ATR | 2.908 % | 121.0832 | 36.86 % | 53.12 % | 60.65 % | 67.85 % | 76.22 % | 82.34 % |
| 0.75 ATR | 4.362 % | 119.2698 | 19.34 % | 35.89 % | 45.71 % | 55.31 % | 65.45 % | 73.2 % |
| 1.0 ATR | 5.816 % | 117.4564 | 9.16 % | 22.78 % | 32.39 % | 43.48 % | 54.67 % | 65.71 % |
| 1.25 ATR | 7.27 % | 115.643 | 4.83 % | 14.42 % | 22.2 % | 33.16 % | 46.65 % | 59.34 % |
| 1.5 ATR | 8.725 % | 113.8296 | 2.42 % | 9.88 % | 16.15 % | 26.69 % | 39.53 % | 53.59 % |
| 2.0 ATR | 11.633 % | 110.2029 | 0.5 % | 3.93 % | 7.37 % | 15.47 % | 29.47 % | 44.15 % |
| 2.5 ATR | 14.541 % | 106.5761 | 0.1 % | 1.51 % | 3.83 % | 8.19 % | 21.14 % | 34.6 % |
| 3.0 ATR | 17.449 % | 102.9493 | 0.0 % | 0.71 % | 2.32 % | 5.26 % | 15.35 % | 26.59 % |
| 4.0 ATR | 23.265 % | 95.6957 | 0.0 % | 0.4 % | 0.91 % | 2.22 % | 6.91 % | 14.89 % |
| 6.0 ATR | 34.898 % | 81.1886 | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.32 % | 4.62 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.37 ATR | 0.42 ATR | 0.56 ATR | 0.67 ATR | 0.74 ATR | 0.98 ATR | 1.24 ATR |
| **2 s.** | 0.24 ATR | 0.55 ATR | 0.62 ATR | 0.81 ATR | 0.96 ATR | 1.08 ATR | 1.49 ATR | 1.91 ATR |
| **3 s.** | 0.30 ATR | 0.68 ATR | 0.76 ATR | 0.99 ATR | 1.18 ATR | 1.34 ATR | 1.85 ATR | 2.33 ATR |
| **5 s.** | 0.39 ATR | 0.86 ATR | 0.97 ATR | 1.26 ATR | 1.57 ATR | 1.80 ATR | 2.38 ATR | 3.09 ATR |
| **10 s.** | 0.53 ATR | 1.15 ATR | 1.31 ATR | 1.82 ATR | 2.27 ATR | 2.60 ATR | 3.63 ATR | 4.68 ATR |
| **20 s.** | 0.70 ATR | 1.69 ATR | 1.96 ATR | 2.60 ATR | 3.14 ATR | 3.56 ATR | 4.95 ATR | 5.93 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.421–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.618–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.362 %, prix 119.2701), p(touche) 35.89 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.763–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.816 %, prix 117.4569), p(touche) 32.39 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (62.6 % des re-echantillons)
- **5 seance(s)** : plage utile 0.968–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.816 %, prix 117.4569), p(touche) 43.48 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.308–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.725 %, prix 113.8291), p(touche) 39.53 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.955–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (11.633 %, prix 110.2025), p(touche) 44.15 % (en stress 97.96 %)  ✅ optimum identifie (63.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.002 | EV/share : $0.012 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 22 % | T3 22 %
- Kelly (position) : f* 0.139 | ¼-Kelly 0.035 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 17.2 | bear 61.3 | side 21.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 499.0 (= 4 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.989% → cible +3.011% / stop −5.0%, p_fill 63%, n_eff≈24.1) : P(cible|rempli) **45%** · **EV/risk +0.058** (×p_fill ; si rempli +0.47% du capital)
  - **swing** (entrée dip −4.381% → cible +17.964% / stop −8.982%, p_fill 25%, n_eff≈14.7) : P(cible|rempli) **3%** · **EV/risk +0.011** (×p_fill ; si rempli +0.38% du capital)
  - **deep** (entrée dip −6.766% → cible +9.521% / stop −9.358%, p_fill 27%, n_eff≈15.9) : P(cible|rempli) **43%** · **EV/risk -0.026** (×p_fill ; si rempli -0.91% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→81% · +2.0%→55% · +3.0%→35% · +5.0%→22% · +8.0%→9%
- Range intraday médian 5.22% (p90 9.06%) · excursion haute méd. +2.13% / basse méd. −2.32%
- Profil de vol intra : ouverture 3.858% vs midi 1.014% vs clôture 1.153% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 18% · trend ↑1%/↓0% ; spike-down 70% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; neutre — autocorr -0.025)_ ; drift intra méd. -0.047% ; recovery-V 30%
- **σ réalisé intraday** 3.467% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 49% / whipsaw 9%
- POC intraday (dernière séance, temps-au-prix) : 103.5331 (VA 103.0981–105.5994 ; dernier close 103.49)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 40% · rebond 79% · **stop −4.06%** sous le fill (sous le bruit) · cible +2.11% · R/R 0.52 (high win-rate)
- Gaps overnight (n=159) : méd. -0.05% · baisse 51% (gap-down >1% 32% · >2% 14%)
- Excursion ouverture 5min (n=160) : bas méd −0.96% (p90 −2.72%) · haut méd +1.03% · range méd 2.22%
- Excursion ouverture 15min (n=160) : bas méd −1.32% (p90 −3.72%) · haut méd +1.37% · range méd 2.89%
- Excursion ouverture 30min (n=160) : bas méd −1.42% (p90 −3.87%) · haut méd +1.62% · range méd 3.43%
- Excursion ouverture 60min (n=160) : bas méd −1.91% (p90 −3.92%) · haut méd +1.63% · range méd 3.89%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 103.51 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 80% (124/159) · gap 43% · délai 0.0min · rebond 62% (69/124) (MFE +1.5%)
   - −1.0% : fill 30min 61% · séance 69% (109/159) · gap 32% · délai 0.0min · rebond 65% (65/109) (MFE +1.7%)
   - −1.5% : fill 30min 50% · séance 61% (100/159) · gap 23% · délai 0.6min · rebond 63% (58/100) (MFE +1.32%)
   - −2.0% : fill 30min 40% · séance 52% (89/159) · gap 14% · délai 1.6min · rebond 70% (56/89) (MFE +1.41%)
   - −3.0% : fill 30min 28% · séance 40% (68/159) · gap 6% · délai 13.6min · rebond 79% (48/68) (MFE +2.11%)
   - −4.0% : fill 30min 16% · séance 29% (51/159) · gap 3% · délai 11.9min · rebond 72% (34/51) (MFE +2.29%)
   - −5.0% : fill 30min 9% · séance 16% (33/159) · gap 2% · délai 28.3min · rebond 67% (24/33) (MFE +2.22%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.63% (p90 −2.63%) → stop au-delà de −1.69% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.64% (p90 −2.36%) → stop au-delà de −1.79% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −2.42%) → stop au-delà de −1.66% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=776 jambes) : jambe baissière méd −1.13% (p90 −2.8%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (76 séances) :
      · −1.0% : fill 94% (73/76) · rebond 55% (39/73)
      · −2.0% : fill 81% (63/76) · rebond 64% (38/63)
      · −3.0% : fill 71% (53/76) · rebond 78% (37/53)
      · −4.0% : fill 51% (41/76) · rebond 71% (29/41)
      · −5.0% : fill 30% (28/76) · rebond 62% (19/28)
   - **flat** (16 séances) :
      · −1.0% : fill 63% (11/16) · rebond 80% (7/11)
      · −2.0% : fill 39% (9/16) · rebond 61% (6/9)
      · −3.0% : fill 12% (4/16) · rebond 18% (1/4)
      · −4.0% : fill 12% (4/16) · rebond 18% (1/4)
      · −5.0% : fill 5% (2/16) · rebond 100% (2/2)
   - **gap-up** (67 séances) :
      · −1.0% : fill 43% (25/67) · rebond 84% (19/25)
      · −2.0% : fill 24% (17/67) · rebond 92% (12/17)
      · −3.0% : fill 14% (11/67) · rebond 97% (10/11)
      · −4.0% : fill 9% (6/67) · rebond 91% (4/6)
      · −5.0% : fill 4% (3/67) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 65% si les 15 1res min sont vertes (75 cas) · 32% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **22min** → P(séance verte=clôture>ouverture) 66% si début vert vs 26% si rouge (base 47% · écart 40 pts) ; prédictivité sature ensuite (plafond brut 218min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **66%** · continue >prix actuel 48% ; creux résiduel méd -1.62% (q20 -3.42%) → **SL/trailing à −3.42%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.84% / q75 +3.2% → **scale +1.84% / runner +3.2%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **26%** (continue à baisser 54%) → **RÉDUIRE ~74%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.76%** (au-delà de la MAE q10 -3.76%), cible rebond +1.87% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.21% .. +4.14%] · haut q95 +4.67% · bas q05 -5.06%
   - 60min (n=160) : retour [-3.68% .. +4.96%] · haut q95 +6.16% · bas q05 -5.58%
   - 2h (n=160) : retour [-4.78% .. +5.78%] · haut q95 +7.54% · bas q05 -6.03%
   - 4h (n=160) : retour [-4.83% .. +6.94%] · haut q95 +8.27% · bas q05 -6.76%
   - 6h (n=160) : retour [-5.75% .. +6.65%] · haut q95 +8.52% · bas q05 -7.11%
   - session (n=160) : retour [-5.37% .. +7.02%] · haut q95 +8.64% · bas q05 -7.13%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.7% des séances sont trend-up (mild 0% / strong 8.7%) · base = 14 séances trend-up (n_eff 8.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **36%**. Lecture précoce 30 min : signature présente → 23% vs absente 2% (base 9%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.92% (p75 1.5% / p90 2.5%) · ~4.0 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **77%** (reprise méd 20.0 min, n=51)
   - −1.0% → **65%** (reprise méd 38.77 min, n=23)
   - −1.5% → **47%** (reprise méd 41.95 min, n=13)
   - −2.0% → **14%** (reprise méd None min, n=6)
   - −3.0% → **20%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.5%** (p90, défaut prudent ; serré/agressif −1.5%) ; extension open→close méd +6.95% (q75 +9.04% / q95 +12.46%), MFE méd +8.52% / q90 +13.87%
   - Échelle scale-out : +8.52% (33%) / +9.47% (33%) / +13.87% (34%)
- **DÉSARMER** : repli > **−2.5%** depuis le plus-haut = décay → P(retournement) **81%** (préavis méd 286.42 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.87% : P(retournement après) 0% (mèche méd 5.8%)
- **CONTEXTE** : la dernière heure tient les gains 67% du temps (retour médian dernière heure +0.38%)


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 70.9  _(surachat)_
- **ADX** : 19.9  _(pas de tendance nette)_
- **MACD** : hist 1.793  _(pas de croisement recent)_
- **BB** : %B 1.19 · largeur 32.7%
- **ATR** : 7.25 (75.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.106  _(accumulation)_
- **Vol ratio** : 2.42  _(volume au-dessus de la moyenne)_
- **Choppiness** : 42.1  _(transition)_
- **MA** : MA20 101.85 · MA50 101.88 · MA200 95.07  _(prix > MA20)_
- **Dist MA** : MA20 +22.4% · MA50 +22.4% · MA200 +31.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (759095 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
