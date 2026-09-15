# SMCI

**Generated** : 2026-09-15T00:33:49.214341+00:00  
**Santé technique** : 6/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · $36.73  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot $36.73 (+7.7% vs entrée) · entrée $34.11 · stop $31.85 · T1 $35.92 · R/R 0.8  
> ↳ P(T1 av. stop) 70 % · EV/risk 0.169 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -12.7 % ≠ (strike 35.0 − spot 36.73)/spot = -4.7 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.030 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $33.75–$34.47 (mid $34.11)
- Spot actuel : $36.73 (+7.7% au-dessus de la zone — repli à attendre)
- Stop : $31.85 (stop swing_plan-based (-13.29%))
- Targets : T1 $35.92 · R/R 0.8 | T2 $37.72 · R/R 1.6 | T3 $39.53 · R/R 2.4
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $31.85


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.82 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (13.29 %)** : le gap seul le franchit 0.718 % des séances (9 fois sur 1253).
   - exécution **4.052 pt plus bas** dans le cas TYPIQUE (médiane), 14.008 au p90, **15.761 au pire**
   - perte réelle **19.221 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 13.29 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0426 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 9 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.795 % | p01 -10.307 % | pire -29.051 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5357** [0.4613 ; 0.6089] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4104** [0.3595 ; 0.4628] _(largeur 10.3 pt, n_eff 345.7)_
   - deep : **0.3439** [0.2953 ; 0.3951] _(largeur 10.0 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (44.9 pt), swing (48.7 pt), deep (50.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.63 %** | CVaR **-12.34 %** | vol 5.8 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 3.75 % contre 6.57 % aujourd'hui, rapport 0.57)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.69 % vs -16.48 % si l'on extrapolait par √5 _(rapport 1.013 ; < 1 = le √5 surestime)_
- **β de baisse : 1.5284** (β de hausse 1.2297, asymétrie 1.2429) vs IWM — 602 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.878× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 32.7712 sur atr_grid (1.75 ATR, 10.778 %) — p(stop avant cible) 0.3294 [0.28 ; 0.38], R/R 0.452, perte reelle 16.875 % (gap inclus), CVaR 10.841 %, EV -1.7194 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 15 des 15 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 65.8 % de la queue et il ne reste que -887.74 EUR a partager. Prix du risque -0.635 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.69 ATR (stop 7.756 %) — p(stop avant cible) 0.4505 [0.40 ; 0.50], R/R 0.539, perte reelle 14.137 % (gap inclus), EV -2.6993 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.70 %) : P(cible) 49.1 % x 7.62 % + P(rien) 5.8 % x -1.29 % ne couvrent pas P(stop) 45.1 % x 14.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 2.21 ATR (stop 17.115 %) — p(stop avant cible) 0.1615 [0.13 ; 0.20], R/R 0.326, perte reelle 23.404 % (gap inclus), EV -0.3375 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.14 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.34 %) : P(cible) 57.6 % x 7.62 % + P(rien) 26.3 % x -3.60 % ne couvrent pas P(stop) 16.2 % x 23.40 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.99 ATR (stop 28.087 %) — p(stop avant cible) 0.0718 [0.05 ; 0.10], R/R 0.262, perte reelle 29.051 % (gap inclus), EV 0.3378 % — **REFUSE**
      - refuse : R/R 0.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.09 % > budget 12.00 %
   - 🟢 support a 5.0 ATR (stop 34.348 %) — p(stop avant cible) 0.0579 [0.04 ; 0.09], R/R 0.222, perte reelle 34.348 % (gap inclus), EV 0.0903 % — **REFUSE**
      - refuse : R/R 0.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.35 % > budget 12.00 %
   - 🟢 support a 5.9 ATR (stop 39.875 %) — p(stop avant cible) 0.0141 [0.01 ; 0.03], R/R 0.191, perte reelle 39.875 % (gap inclus), EV 0.2408 % — **REFUSE**
      - refuse : R/R 0.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.88 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.54 %) — p(stop avant cible) 0.8249 [0.78 ; 0.86], R/R 1.888, perte reelle 4.035 % (gap inclus), EV -1.995 % — **REFUSE**
      - refuse : p_stop_first 0.825, borne haute 0.862 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.99 %) : P(cible) 17.5 % x 7.62 % + P(rien) 0.0 % x 3.45 % ne couvrent pas P(stop) 82.5 % x 4.04 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.69 ATR (stop 6.074 %) — p(stop avant cible) 0.5528 [0.50 ; 0.60], R/R 0.644, perte reelle 11.824 % (gap inclus), EV -3.3135 % — **REFUSE**
      - refuse : p_stop_first 0.553, borne haute 0.605 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.31 %) : P(cible) 42.4 % x 7.62 % + P(rien) 2.3 % x -0.32 % ne couvrent pas P(stop) 55.3 % x 11.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.5 ATR (stop 9.238 %) — p(stop avant cible) 0.3901 [0.34 ; 0.44], R/R 0.466, perte reelle 16.347 % (gap inclus), EV -2.6489 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.65 %) : P(cible) 50.9 % x 7.62 % + P(rien) 10.1 % x -1.49 % ne couvrent pas P(stop) 39.0 % x 16.35 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 10.778 %) — p(stop avant cible) 0.3294 [0.28 ; 0.38], R/R 0.452, perte reelle 16.875 % (gap inclus), EV -1.7194 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.72 %) : P(cible) 53.8 % x 7.62 % + P(rien) 13.3 % x -1.95 % ne couvrent pas P(stop) 32.9 % x 16.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.21 ATR (stop 15.434 %) — p(stop avant cible) 0.1884 [0.15 ; 0.23], R/R 0.326, perte reelle 23.404 % (gap inclus), EV -0.9958 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.47 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.00 %) : P(cible) 56.6 % x 7.62 % + P(rien) 24.5 % x -3.67 % ne couvrent pas P(stop) 18.8 % x 23.40 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 18.477 %) — p(stop avant cible) 0.1357 [0.10 ; 0.17], R/R 0.306, perte reelle 24.92 % (gap inclus), EV -0.085 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.09 %) : P(cible) 58.2 % x 7.62 % + P(rien) 28.2 % x -4.04 % ne couvrent pas P(stop) 13.6 % x 24.92 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 21.556 %) — p(stop avant cible) 0.1147 [0.08 ; 0.15], R/R 0.284, perte reelle 26.856 % (gap inclus), EV 0.0587 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.57 % > budget 12.00 %
   - 🟢 grid_snapped a 3.99 ATR (stop 26.405 %) — p(stop avant cible) 0.0743 [0.05 ; 0.11], R/R 0.273, perte reelle 27.955 % (gap inclus), EV 0.4076 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.41 % > budget 12.00 %
   - 🟢 grid_snapped a 5.0 ATR (stop 32.667 %) — p(stop avant cible) 0.06 [0.04 ; 0.09], R/R 0.233, perte reelle 32.667 % (gap inclus), EV 0.1563 % — **REFUSE**
      - refuse : R/R 0.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.67 % > budget 12.00 %
   - 🟢 grid_snapped a 5.9 ATR (stop 38.194 %) — p(stop avant cible) 0.0353 [0.02 ; 0.06], R/R 0.2, perte reelle 38.194 % (gap inclus), EV 0.1185 % — **REFUSE**
      - refuse : R/R 0.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.19 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 43.112 %) — p(stop avant cible) 0.003 [0.00 ; 0.01], R/R 0.177, perte reelle 43.112 % (gap inclus), EV 0.2663 % — **REFUSE**
      - refuse : R/R 0.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.11 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 46.191 %) — p(stop avant cible) 0.0016 [0.00 ; 0.01], R/R 0.165, perte reelle 46.191 % (gap inclus), EV 0.2636 % — **REFUSE**
      - refuse : R/R 0.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.19 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 49.271 %) — p(stop avant cible) 0.0016 [0.00 ; 0.01], R/R 0.155, perte reelle 49.271 % (gap inclus), EV 0.2587 % — **REFUSE**
      - refuse : R/R 0.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.27 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 36.73, ATR14 2.2621 (6.159 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.342 ATR = 2.106 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.308 % | 36.6169 | 90.33 % | 93.15 % | 94.55 % | 95.05 % | 96.34 % | 97.54 % |
| 0.1 ATR | 0.616 % | 36.5038 | 81.97 % | 87.1 % | 89.1 % | 91.1 % | 92.99 % | 94.87 % |
| 0.15 ATR | 0.924 % | 36.3907 | 74.72 % | 81.85 % | 84.76 % | 88.07 % | 90.55 % | 93.53 % |
| 0.2 ATR | 1.232 % | 36.2776 | 67.77 % | 77.12 % | 80.32 % | 85.54 % | 89.02 % | 92.2 % |
| 0.25 ATR | 1.54 % | 36.1645 | 61.73 % | 72.58 % | 76.19 % | 82.2 % | 86.99 % | 90.45 % |
| 0.35 ATR | 2.156 % | 35.9382 | 49.04 % | 63.31 % | 69.53 % | 77.05 % | 82.72 % | 87.89 % |
| 0.5 ATR | 3.079 % | 35.5989 | 34.84 % | 49.8 % | 58.22 % | 68.55 % | 77.03 % | 83.57 % |
| 0.75 ATR | 4.619 % | 35.0334 | 17.32 % | 33.17 % | 42.89 % | 54.9 % | 66.57 % | 75.36 % |
| 1.0 ATR | 6.159 % | 34.4679 | 8.06 % | 21.67 % | 30.68 % | 43.48 % | 57.22 % | 68.58 % |
| 1.25 ATR | 7.699 % | 33.9023 | 3.83 % | 15.02 % | 22.5 % | 33.16 % | 48.17 % | 61.6 % |
| 1.5 ATR | 9.238 % | 33.3368 | 1.51 % | 9.68 % | 16.45 % | 26.19 % | 41.97 % | 55.24 % |
| 2.0 ATR | 12.318 % | 32.2057 | 0.3 % | 3.53 % | 8.38 % | 16.08 % | 30.08 % | 43.84 % |
| 2.5 ATR | 15.397 % | 31.0746 | 0.2 % | 1.51 % | 4.34 % | 9.81 % | 19.82 % | 32.03 % |
| 3.0 ATR | 18.477 % | 29.9436 | 0.2 % | 1.21 % | 2.62 % | 5.66 % | 14.23 % | 24.13 % |
| 4.0 ATR | 24.635 % | 27.6814 | 0.0 % | 0.6 % | 1.51 % | 2.63 % | 7.42 % | 14.17 % |
| 6.0 ATR | 36.953 % | 23.1571 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.54 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.34 ATR | 0.39 ATR | 0.53 ATR | 0.64 ATR | 0.71 ATR | 0.95 ATR | 1.18 ATR |
| **2 s.** | 0.22 ATR | 0.50 ATR | 0.57 ATR | 0.75 ATR | 0.93 ATR | 1.06 ATR | 1.49 ATR | 1.88 ATR |
| **3 s.** | 0.27 ATR | 0.63 ATR | 0.72 ATR | 0.95 ATR | 1.17 ATR | 1.35 ATR | 1.90 ATR | 2.42 ATR |
| **5 s.** | 0.39 ATR | 0.86 ATR | 0.97 ATR | 1.26 ATR | 1.56 ATR | 1.81 ATR | 2.48 ATR | 3.22 ATR |
| **10 s.** | 0.55 ATR | 1.20 ATR | 1.38 ATR | 1.88 ATR | 2.25 ATR | 2.49 ATR | 3.62 ATR | 4.90 ATR |
| **20 s.** | 0.76 ATR | 1.73 ATR | 1.95 ATR | 2.46 ATR | 2.94 ATR | 3.42 ATR | 4.97 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.393–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.572–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.619 %, prix 35.0334), p(touche) 33.17 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.716–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.619 %, prix 35.0334), p(touche) 42.89 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 15.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.967–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.699 %, prix 33.9022), p(touche) 33.16 % (en stress 89.9 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.378–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.238 %, prix 33.3369), p(touche) 41.97 % (en stress 95.96 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 19.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.949–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (15.397 %, prix 31.0747), p(touche) 32.03 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (60.4 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.013 | EV/share : $0.030 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 51 % | T2 30 % | T3 19 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 83.7 | bear 6.7 | side 9.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 367.0 (= 10 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.242% → cible +2.368% / stop −1.909%, p_fill 33%, n_eff≈16.5) : P(cible|rempli) **49%** · **EV/risk +0.033** (×p_fill ; si rempli +0.19% du capital)
  - **swing** (entrée dip −7.131% → cible +5.296% / stop −6.632%, p_fill 20%, n_eff≈11.0) : P(cible|rempli) **72%** · **EV/risk +0.062** (×p_fill ; si rempli +2.06% du capital)
  - **deep** (entrée dip −11.021% → cible +7.489% / stop −10.383%, p_fill 13%, n_eff≈11.9) : P(cible|rempli) **60%** · **EV/risk +0.006** (×p_fill ; si rempli +0.51% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→92% · +1.0%→76% · +2.0%→61% · +3.0%→46% · +5.0%→28% · +8.0%→12%
- Range intraday médian 6.2% (p90 10.79%) · excursion haute méd. +2.57% / basse méd. −2.36%
- Profil de vol intra : ouverture 4.155% vs midi 1.244% vs clôture 1.619% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓1% ; spike-down 71% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; neutre — autocorr -0.019)_ ; drift intra méd. 0.322% ; recovery-V 35%
- **σ réalisé intraday** 3.833% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 64% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 40.5704 (VA 39.4716–40.8634 ; dernier close 39.59)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 27% · rebond 81% · **stop −4.2%** sous le fill (sous le bruit) · cible +2.59% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. 0.25% · baisse 45% (gap-down >1% 36% · >2% 17%)
- Excursion ouverture 5min (n=160) : bas méd −0.9% (p90 −2.79%) · haut méd +0.96% · range méd 2.29%
- Excursion ouverture 15min (n=160) : bas méd −1.29% (p90 −3.21%) · haut méd +1.42% · range méd 2.85%
- Excursion ouverture 30min (n=160) : bas méd −1.44% (p90 −3.93%) · haut méd +1.5% · range méd 3.68%
- Excursion ouverture 60min (n=160) : bas méd −1.72% (p90 −4.91%) · haut méd +1.81% · range méd 4.41%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 39.59 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 72% (120/159) · gap 42% · délai 0.0min · rebond 58% (73/120) (MFE +1.37%)
   - −1.0% : fill 30min 55% · séance 69% (111/159) · gap 36% · délai 0.0min · rebond 62% (67/111) (MFE +1.61%)
   - −1.5% : fill 30min 49% · séance 63% (101/159) · gap 22% · délai 0.0min · rebond 71% (66/101) (MFE +1.61%)
   - −2.0% : fill 30min 43% · séance 55% (88/159) · gap 17% · délai 0.5min · rebond 74% (58/88) (MFE +1.91%)
   - −3.0% : fill 30min 31% · séance 48% (75/159) · gap 10% · délai 7.1min · rebond 63% (47/75) (MFE +1.9%)
   - −4.0% : fill 30min 17% · séance 36% (57/159) · gap 5% · délai 36.7min · rebond 78% (38/57) (MFE +1.88%)
   - −5.0% : fill 30min 13% · séance 27% (46/159) · gap 3% · délai 42.5min · rebond 81% (34/46) (MFE +2.59%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.59% (p90 −2.79%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.7% (p90 −2.95%) → stop au-delà de −1.99% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.74% (p90 −2.73%) → stop au-delà de −2.03% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=897 jambes) : jambe baissière méd −1.19% (p90 −2.87%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 97% (68/70) · rebond 50% (36/68)
      · −2.0% : fill 92% (64/70) · rebond 70% (39/64)
      · −3.0% : fill 86% (58/70) · rebond 60% (35/58)
      · −4.0% : fill 65% (45/70) · rebond 78% (30/45)
      · −5.0% : fill 49% (37/70) · rebond 80% (27/37)
   - **flat** (13 séances) :
      · −1.0% : fill 100% (13/13) · rebond 92% (11/13)
      · −2.0% : fill 41% (6/13) · rebond 89% (4/6)
      · −3.0% : fill 26% (3/13) · rebond 100% (3/3)
      · −4.0% : fill 22% (2/13) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/13) · rebond 0% (0/0)
   - **gap-up** (76 séances) :
      · −1.0% : fill 40% (30/76) · rebond 77% (20/30)
      · −2.0% : fill 24% (18/76) · rebond 84% (15/18)
      · −3.0% : fill 16% (14/76) · rebond 70% (9/14)
      · −4.0% : fill 12% (10/76) · rebond 71% (6/10)
      · −5.0% : fill 11% (9/76) · rebond 85% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 64% si les 15 1res min sont vertes (77 cas) · 28% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:47** → P(séance verte=clôture>ouverture) 80% si début vert vs 9% si rouge (base 47% · écart 72 pts) ; prédictivité sature ensuite (plafond brut 213min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=87) : tient le vert **80%** · continue >prix actuel 48% ; creux résiduel méd -1.35% (q20 -3.0%) → **SL/trailing à −3.0%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.8% / q75 +2.95% → **scale +1.8% / runner +2.95%**, sortie à la clôture
  - **si ROUGE au coude** (n=73) : edge inversé — récupère vert seulement **9%** (continue à baisser 48%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.57%** (au-delà de la MAE q10 -4.57%), cible rebond +2.07% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.18% .. +4.68%] · haut q95 +5.63% · bas q05 -4.48%
   - 60min (n=160) : retour [-4.4% .. +5.2%] · haut q95 +6.46% · bas q05 -5.33%
   - 2h (n=160) : retour [-4.66% .. +6.65%] · haut q95 +7.25% · bas q05 -5.84%
   - 4h (n=160) : retour [-5.17% .. +7.01%] · haut q95 +8.34% · bas q05 -6.68%
   - 6h (n=160) : retour [-5.44% .. +6.82%] · haut q95 +9.16% · bas q05 -6.9%
   - session (n=160) : retour [-6.74% .. +7.68%] · haut q95 +9.32% · bas q05 -7.21%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — SMCI = **volatil sans tendance propre (choppy)** (vol intra méd 3.61%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 53.9  _(neutre)_
- **ADX** : 25.0  _(tendance etablie)_
- **MACD** : hist -0.257  _(bearish_recent)_
- **BB** : %B 0.31 · largeur 13.6%
- **ATR** : 2.26 (55.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.034  _(neutre)_
- **Vol ratio** : 0.92  _(volume normal)_
- **Choppiness** : 63.7  _(marche en range (choppy))_
- **MA** : MA20 37.72 · MA50 32.71 · MA200 31.51  _(prix < MA20)_
- **Dist MA** : MA20 -2.6% · MA50 +12.3% · MA200 +16.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (750123 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
