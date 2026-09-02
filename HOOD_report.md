# HOOD

**Generated** : 2026-09-02T00:33:20.806248+00:00  
**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $103.51  

> 🟡 **WAIT-FOR-DIP** — spot +0.7 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $103.51 (+0.7% vs entrée) · entrée $102.79 · stop $96.54 · T1 $114.72 · R/R 1.91  
> ↳ P(T1 av. stop) 23 % _(réel 5 s)_ · EV/risk 0.125 _(réel 5 s)_ (GBM 0.034) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.100 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $102.07–$103.51 (mid $102.79)
- Spot actuel : $103.51 (+0.7% au-dessus de la zone — repli à attendre)
- Stop : $96.54 (stop swing_plan-based (-6.73%))
- Targets : T1 $114.72 · R/R 1.91 | T2 $117.19 · R/R 2.3 | T3 $119.66 · R/R 2.7
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $96.54


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.02 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (6.73 %)** : le gap seul le franchit 1.117 % des séances (14 fois sur 1253).
   - exécution **2.801 pt plus bas** dans le cas TYPIQUE (médiane), 6.729 au p90, **11.055 au pire**
   - perte réelle **10.236 %** en moyenne _(tirée par la queue)_, jusqu'à **17.785 %** — au lieu des 6.73 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0392 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 14 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.437 % | p01 -7.308 % | pire -17.785 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1286** [0.085 ; 0.1845] _(largeur 10.0 pt, n_eff 173.1)_
   - swing : **0.4172** [0.3661 ; 0.4697] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.406** [0.3552 ; 0.4584] _(largeur 10.3 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.5 pt), swing (31.6 pt), deep (31.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-6.19 %** | CVaR **-9.11 %** | vol 4.35 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 2.09 % contre 4.48 % aujourd'hui, rapport 0.47)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.55 % vs -14.36 % si l'on extrapolait par √5 _(rapport 1.013 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7638** (β de hausse 1.614, asymétrie 1.0928) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.493× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 94.1393 sur atr_based (1.5 ATR, 9.053 %) — p(stop avant cible) 0.4135 [0.36 ; 0.47], R/R 1.309, perte reelle 11.916 % (gap inclus), CVaR 9.071 %, EV 0.4592 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 18 des 18 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 60.2 % de la queue et il ne reste que -755.68 EUR a partager. Prix du risque -0.422 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.23 ATR (stop 4.356 %) — p(stop avant cible) 0.6758 [0.63 ; 0.72], R/R 2.209, perte reelle 7.064 % (gap inclus), EV -0.9223 % — **REFUSE**
      - refuse : p_stop_first 0.676, borne haute 0.724 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.04 ATR du spot — compartiment <1, mesure a 46.1 % de casse (IC clusterise [0.427 ; 0.494] sur 1133 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.92 %) : P(cible) 21.0 % x 15.60 % + P(rien) 11.5 % x 5.07 % ne couvrent pas P(stop) 67.6 % x 7.06 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 9.053 %) — p(stop avant cible) 0.4135 [0.36 ; 0.47], R/R 1.309, perte reelle 11.916 % (gap inclus), EV 0.4592 % — **REFUSE**
      - refuse : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 1.93 ATR (stop 14.654 %) — p(stop avant cible) 0.2094 [0.17 ; 0.25], R/R 0.877, perte reelle 17.785 % (gap inclus), EV 1.361 % — **REFUSE**
      - refuse : R/R 0.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.66 % > budget 12.00 %
   - 🟢 support a 3.93 ATR (stop 26.74 %) — p(stop avant cible) 0.0324 [0.02 ; 0.06], R/R 0.583, perte reelle 26.74 % (gap inclus), EV 2.0329 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.74 % > budget 12.00 %
   - 🔴 grid_snapped a 0.23 ATR (stop 3.173 %) — p(stop avant cible) 0.7609 [0.71 ; 0.80], R/R 2.927, perte reelle 5.331 % (gap inclus), EV -0.9934 % — **REFUSE**
      - refuse : p_stop_first 0.761, borne haute 0.804 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.99 %) : P(cible) 17.0 % x 15.60 % + P(rien) 6.9 % x 5.90 % ne couvrent pas P(stop) 76.1 % x 5.33 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 6.035 %) — p(stop avant cible) 0.5772 [0.52 ; 0.63], R/R 1.595, perte reelle 9.781 % (gap inclus), EV -1.0268 % — **REFUSE**
      - refuse : p_stop_first 0.577, borne haute 0.628 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.03 %) : P(cible) 25.6 % x 15.60 % + P(rien) 16.7 % x 3.73 % ne couvrent pas P(stop) 57.7 % x 9.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 7.544 %) — p(stop avant cible) 0.4959 [0.44 ; 0.55], R/R 1.487, perte reelle 10.494 % (gap inclus), EV -0.2262 % — **REFUSE**
      - refuse : R/R 1.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.23 %) : P(cible) 27.4 % x 15.60 % + P(rien) 23.0 % x 3.06 % ne couvrent pas P(stop) 49.6 % x 10.49 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 1.93 ATR (stop 13.471 %) — p(stop avant cible) 0.2536 [0.21 ; 0.30], R/R 0.978, perte reelle 15.955 % (gap inclus), EV 1.2465 % — **REFUSE**
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.47 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 16.597 %) — p(stop avant cible) 0.1548 [0.12 ; 0.20], R/R 0.877, perte reelle 17.785 % (gap inclus), EV 1.7856 % — **REFUSE**
      - refuse : R/R 0.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.60 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 18.106 %) — p(stop avant cible) 0.1211 [0.09 ; 0.16], R/R 0.862, perte reelle 18.106 % (gap inclus), EV 2.0164 % — **REFUSE**
      - refuse : R/R 0.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.11 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 21.124 %) — p(stop avant cible) 0.0808 [0.06 ; 0.11], R/R 0.739, perte reelle 21.124 % (gap inclus), EV 1.9708 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.12 % > budget 12.00 %
   - 🟢 grid_snapped a 3.93 ATR (stop 25.557 %) — p(stop avant cible) 0.0358 [0.02 ; 0.06], R/R 0.61, perte reelle 25.557 % (gap inclus), EV 2.0575 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.56 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 30.177 %) — p(stop avant cible) 0.0251 [0.01 ; 0.05], R/R 0.517, perte reelle 30.177 % (gap inclus), EV 2.0275 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.18 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 33.194 %) — p(stop avant cible) 0.0066 [0.00 ; 0.02], R/R 0.47, perte reelle 33.194 % (gap inclus), EV 2.1342 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.19 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 36.212 %) — p(stop avant cible) 0.0021 [0.00 ; 0.01], R/R 0.431, perte reelle 36.212 % (gap inclus), EV 2.1868 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.21 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 39.229 %) — p(stop avant cible) 0.0003 [0.00 ; 0.01], R/R 0.398, perte reelle 39.229 % (gap inclus), EV 2.2015 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.23 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 42.247 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.369, perte reelle 42.247 % (gap inclus), EV 2.2048 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.25 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 45.265 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.345, perte reelle 45.265 % (gap inclus), EV 2.2048 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 45.26 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 48.282 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.323, perte reelle 48.282 % (gap inclus), EV 2.2048 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 48.28 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 103.51, ATR14 6.2471 (6.035 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.373 ATR = 2.251 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.302 % | 103.1976 | 92.85 % | 94.96 % | 95.86 % | 96.36 % | 96.95 % | 97.95 % |
| 0.1 ATR | 0.604 % | 102.8853 | 85.5 % | 90.22 % | 91.93 % | 93.43 % | 94.51 % | 96.41 % |
| 0.15 ATR | 0.905 % | 102.5729 | 77.64 % | 84.98 % | 87.69 % | 89.89 % | 92.28 % | 94.97 % |
| 0.2 ATR | 1.207 % | 102.2606 | 71.6 % | 79.84 % | 83.45 % | 86.55 % | 90.14 % | 93.22 % |
| 0.25 ATR | 1.509 % | 101.9482 | 64.55 % | 74.19 % | 78.91 % | 83.01 % | 87.5 % | 90.86 % |
| 0.35 ATR | 2.112 % | 101.3235 | 52.37 % | 65.12 % | 71.64 % | 77.25 % | 83.13 % | 87.99 % |
| 0.5 ATR | 3.018 % | 100.3864 | 36.96 % | 53.23 % | 60.75 % | 67.85 % | 76.32 % | 82.44 % |
| 0.75 ATR | 4.526 % | 98.8246 | 19.44 % | 36.09 % | 45.81 % | 55.31 % | 65.55 % | 73.41 % |
| 1.0 ATR | 6.035 % | 97.2629 | 9.26 % | 22.88 % | 32.49 % | 43.48 % | 54.78 % | 65.91 % |
| 1.25 ATR | 7.544 % | 95.7011 | 4.83 % | 14.52 % | 22.3 % | 33.16 % | 46.75 % | 59.55 % |
| 1.5 ATR | 9.053 % | 94.1393 | 2.42 % | 9.98 % | 16.35 % | 26.69 % | 39.63 % | 53.8 % |
| 2.0 ATR | 12.071 % | 91.0157 | 0.5 % | 3.93 % | 7.37 % | 15.57 % | 29.67 % | 44.35 % |
| 2.5 ATR | 15.088 % | 87.8921 | 0.1 % | 1.51 % | 3.83 % | 8.19 % | 21.34 % | 34.8 % |
| 3.0 ATR | 18.106 % | 84.7686 | 0.0 % | 0.71 % | 2.32 % | 5.26 % | 15.35 % | 26.59 % |
| 4.0 ATR | 24.141 % | 78.5214 | 0.0 % | 0.4 % | 0.91 % | 2.22 % | 6.91 % | 14.89 % |
| 6.0 ATR | 36.212 % | 66.0272 | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.32 % | 4.62 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.37 ATR | 0.42 ATR | 0.56 ATR | 0.67 ATR | 0.74 ATR | 0.98 ATR | 1.24 ATR |
| **2 s.** | 0.24 ATR | 0.55 ATR | 0.62 ATR | 0.81 ATR | 0.96 ATR | 1.09 ATR | 1.50 ATR | 1.91 ATR |
| **3 s.** | 0.30 ATR | 0.68 ATR | 0.77 ATR | 0.99 ATR | 1.18 ATR | 1.35 ATR | 1.85 ATR | 2.33 ATR |
| **5 s.** | 0.39 ATR | 0.86 ATR | 0.97 ATR | 1.26 ATR | 1.58 ATR | 1.80 ATR | 2.38 ATR | 3.09 ATR |
| **10 s.** | 0.53 ATR | 1.15 ATR | 1.31 ATR | 1.83 ATR | 2.28 ATR | 2.61 ATR | 3.63 ATR | 4.68 ATR |
| **20 s.** | 0.71 ATR | 1.70 ATR | 1.97 ATR | 2.61 ATR | 3.14 ATR | 3.56 ATR | 4.95 ATR | 5.93 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.422–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.62–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.526 %, prix 98.8251), p(touche) 36.09 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.765–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.035 %, prix 97.2632), p(touche) 32.49 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (62.5 % des re-echantillons)
- **5 seance(s)** : plage utile 0.968–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.035 %, prix 97.2632), p(touche) 43.48 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.311–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.053 %, prix 94.1392), p(touche) 39.63 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.966–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (12.071 %, prix 91.0153), p(touche) 44.35 % (en stress 97.96 %)  ✅ optimum identifie (62.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.034 | EV/share : $0.214 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 21 % | T2 16 % | T3 14 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 48.8 | bear 36.2 | side 15.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 414.0 (= 4 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.389% → cible +2.447% / stop −5.0%, p_fill 88%, n_eff≈36.0) : P(cible|rempli) **36%** · **EV/risk -0.030** (×p_fill ; si rempli -0.17% du capital)
  - **swing** (entrée dip −0.694% → cible +11.608% / stop −6.078%, p_fill 85%, n_eff≈35.3) : P(cible|rempli) **23%** · **EV/risk +0.125** (×p_fill ; si rempli +0.89% du capital)
  - **deep** (entrée dip −0.923% → cible +18.647% / stop −9.323%, p_fill 90%, n_eff≈36.2) : P(cible|rempli) **20%** · **EV/risk +0.428** (×p_fill ; si rempli +4.43% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→81% · +2.0%→55% · +3.0%→35% · +5.0%→22% · +8.0%→9%
- Range intraday médian 5.22% (p90 9.06%) · excursion haute méd. +2.13% / basse méd. −2.32%
- Profil de vol intra : ouverture 3.849% vs midi 1.018% vs clôture 1.16% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 19% · trend ↑1%/↓0% ; spike-down 69% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.129 ; neutre — autocorr -0.01)_ ; drift intra méd. 0.035% ; recovery-V 32%
- **σ réalisé intraday** 3.478% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 46% / whipsaw 10%
- POC intraday (dernière séance, temps-au-prix) : 104.2157 (VA 102.7937–105.1637 ; dernier close 104.81)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 41% · rebond 79% · **stop −4.06%** sous le fill (sous le bruit) · cible +2.11% · R/R 0.52 (high win-rate)
- Gaps overnight (n=159) : méd. -0.07% · baisse 52% (gap-down >1% 32% · >2% 14%)
- Excursion ouverture 5min (n=160) : bas méd −0.94% (p90 −2.74%) · haut méd +1.04% · range méd 2.21%
- Excursion ouverture 15min (n=160) : bas méd −1.3% (p90 −3.79%) · haut méd +1.31% · range méd 2.84%
- Excursion ouverture 30min (n=160) : bas méd −1.38% (p90 −3.88%) · haut méd +1.64% · range méd 3.44%
- Excursion ouverture 60min (n=160) : bas méd −1.9% (p90 −3.92%) · haut méd +1.65% · range méd 3.9%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 104.81 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 80% (124/159) · gap 44% · délai 0.0min · rebond 61% (69/124) (MFE +1.47%)
   - −1.0% : fill 30min 60% · séance 68% (108/159) · gap 32% · délai 0.0min · rebond 64% (64/108) (MFE +1.65%)
   - −1.5% : fill 30min 51% · séance 60% (99/159) · gap 23% · délai 0.4min · rebond 64% (58/99) (MFE +1.35%)
   - −2.0% : fill 30min 40% · séance 51% (88/159) · gap 14% · délai 1.5min · rebond 69% (55/88) (MFE +1.45%)
   - −3.0% : fill 30min 28% · séance 41% (68/159) · gap 6% · délai 13.6min · rebond 79% (48/68) (MFE +2.11%)
   - −4.0% : fill 30min 17% · séance 29% (51/159) · gap 3% · délai 11.9min · rebond 72% (34/51) (MFE +2.29%)
   - −5.0% : fill 30min 9% · séance 17% (33/159) · gap 2% · délai 28.3min · rebond 67% (24/33) (MFE +2.22%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.62% (p90 −2.63%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.63% (p90 −2.36%) → stop au-delà de −1.79% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −2.42%) → stop au-delà de −1.66% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=772 jambes) : jambe baissière méd −1.13% (p90 −2.79%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (76 séances) :
      · −1.0% : fill 94% (73/76) · rebond 55% (39/73)
      · −2.0% : fill 81% (63/76) · rebond 64% (38/63)
      · −3.0% : fill 71% (53/76) · rebond 78% (37/53)
      · −4.0% : fill 51% (41/76) · rebond 71% (29/41)
      · −5.0% : fill 30% (28/76) · rebond 62% (19/28)
   - **flat** (17 séances) :
      · −1.0% : fill 62% (11/17) · rebond 80% (7/11)
      · −2.0% : fill 39% (9/17) · rebond 61% (6/9)
      · −3.0% : fill 12% (4/17) · rebond 18% (1/4)
      · −4.0% : fill 12% (4/17) · rebond 18% (1/4)
      · −5.0% : fill 5% (2/17) · rebond 100% (2/2)
   - **gap-up** (66 séances) :
      · −1.0% : fill 41% (24/66) · rebond 82% (18/24)
      · −2.0% : fill 21% (16/66) · rebond 90% (11/16)
      · −3.0% : fill 14% (11/66) · rebond 97% (10/11)
      · −4.0% : fill 10% (6/66) · rebond 91% (4/6)
      · −5.0% : fill 4% (3/66) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 68% si les 15 1res min sont vertes (75 cas) · 32% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **53min** → P(séance verte=clôture>ouverture) 72% si début vert vs 25% si rouge (base 48% · écart 47 pts) ; prédictivité sature ensuite (plafond brut 218min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **72%** · continue >prix actuel 48% ; creux résiduel méd -1.4% (q20 -2.54%) → **SL/trailing à −2.54%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.57% / q75 +3.12% → **scale +1.57% / runner +3.12%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **25%** (continue à baisser 58%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.91%** (au-delà de la MAE q10 -2.91%), cible rebond +1.93% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.24% .. +4.15%] · haut q95 +4.74% · bas q05 -5.08%
   - 60min (n=160) : retour [-3.68% .. +4.96%] · haut q95 +6.17% · bas q05 -5.61%
   - 2h (n=160) : retour [-4.81% .. +5.86%] · haut q95 +7.54% · bas q05 -6.05%
   - 4h (n=160) : retour [-4.87% .. +6.99%] · haut q95 +8.29% · bas q05 -6.77%
   - 6h (n=160) : retour [-5.75% .. +6.7%] · haut q95 +8.53% · bas q05 -7.11%
   - session (n=160) : retour [-5.4% .. +7.03%] · haut q95 +8.65% · bas q05 -7.14%


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

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 57.6  _(momentum haussier)_
- **ADX** : 18.8  _(pas de tendance nette)_
- **MACD** : hist 0.838  _(pas de croisement recent)_
- **BB** : %B 0.65 · largeur 27.1%
- **ATR** : 6.25 (58.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.1  _(distribution)_
- **Vol ratio** : 1.23  _(volume normal)_
- **Choppiness** : 54.0  _(transition)_
- **MA** : MA20 99.45 · MA50 101.26 · MA200 95.13  _(prix > MA20)_
- **Dist MA** : MA20 +4.1% · MA50 +2.2% · MA200 +8.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (773713 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
