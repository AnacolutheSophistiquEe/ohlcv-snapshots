# HOOD

**Generated** : 2026-09-30T00:34:22.637326+00:00  
**Santé technique** : 7/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $116.24  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $116.24 (+1.9% vs entrée) · entrée $114.11 · stop $108.34 · T1 $122.28 · R/R 1.42  
> ↳ ¼-Kelly 0.002 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.010 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $112.76–$115.45 (mid $114.11)
- Spot actuel : $116.24 (+1.9% au-dessus de la zone — repli à attendre)
- Stop : $108.34 (plancher anti-bruit (R/R<2) ; -5.06 % depuis l'entree)
- Targets : T1 $122.28 · R/R 1.42 | T2 $128.26 · R/R 2.45 | T3 $134.23 · R/R 3.49
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $108.34


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.02 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (6.8 %)** : le gap seul le franchit 1.117 % des séances (14 fois sur 1253).
   - exécution **2.731 pt plus bas** dans le cas TYPIQUE (médiane), 6.659 au p90, **10.985 au pire**
   - perte réelle **10.236 %** en moyenne _(tirée par la queue)_, jusqu'à **17.785 %** — au lieu des 6.8 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0384 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 14 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.416 % | p01 -7.308 % | pire -17.785 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3085** [0.2433 ; 0.38] _(largeur 13.7 pt, n_eff 173.1)_
   - swing : **0.5223** [0.4696 ; 0.5746] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4677** [0.4156 ; 0.5204] _(largeur 10.5 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-6.16 %** | CVaR **-8.88 %** | vol 4.37 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 2.78 % contre 4.70 % aujourd'hui, rapport 0.59)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.55 % vs -14.36 % si l'on extrapolait par √5 _(rapport 1.013 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7754** (β de hausse 1.6058, asymétrie 1.1056) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.408× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 108.6781 sur grid_snapped (1.01 ATR, 6.505 %) — p(stop avant cible) 0.564 [0.51 ; 0.62], R/R 2.263, perte reelle 6.839 % (gap inclus), CVaR 10.096 %, EV 0.9632 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.3648 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.564, borne haute 0.616 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 17 des 19 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 41.9 % de la queue et il ne reste que 294.13 EUR a partager. Prix du risque 0.099 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 1.01 ATR (stop 7.275 %) — p(stop avant cible) 0.5244 [0.47 ; 0.58], R/R 2.028, perte reelle 7.632 % (gap inclus), EV 1.0966 % — **REFUSE**
      - refuse : p_stop_first 0.524, borne haute 0.577 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.67 ATR du spot — compartiment <1, mesure a 49.1 % de casse (IC clusterise [0.457 ; 0.522] sur 1123 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 2.7 ATR (stop 15.646 %) — p(stop avant cible) 0.1813 [0.14 ; 0.22], R/R 0.957, perte reelle 16.173 % (gap inclus), EV 2.2696 % — **REFUSE**
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.56 % > budget 12.00 %
   - 🟢 support a 4.3 ATR (stop 23.595 %) — p(stop avant cible) 0.0378 [0.02 ; 0.06], R/R 0.642, perte reelle 24.098 % (gap inclus), EV 2.635 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.17 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.242 %) — p(stop avant cible) 0.9101 [0.88 ; 0.94], R/R 11.447, perte reelle 1.352 % (gap inclus), EV -0.031 % — **REFUSE**
      - refuse : cible atteinte seulement 6.6 % du temps (< 15 %) meme a 10 seances : le R/R de 11.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.910, borne haute 0.937 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 6.6 % x 15.48 % + P(rien) 2.4 % x 7.31 % ne couvrent pas P(stop) 91.0 % x 1.35 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 2.483 %) — p(stop avant cible) 0.7989 [0.75 ; 0.84], R/R 5.842, perte reelle 2.65 % (gap inclus), EV 0.5166 % — **REFUSE**
      - refuse : p_stop_first 0.799, borne haute 0.839 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 3.725 %) — p(stop avant cible) 0.7156 [0.67 ; 0.76], R/R 3.966, perte reelle 3.903 % (gap inclus), EV 0.8551 % — **REFUSE**
      - refuse : p_stop_first 0.716, borne haute 0.761 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - 🔴 grid_snapped a 1.01 ATR (stop 6.505 %) — p(stop avant cible) 0.564 [0.51 ; 0.62], R/R 2.263, perte reelle 6.839 % (gap inclus), EV 0.9632 % — **REFUSE**
      - refuse : p_stop_first 0.564, borne haute 0.616 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.75 ATR (stop 8.691 %) — p(stop avant cible) 0.4413 [0.39 ; 0.49], R/R 1.7, perte reelle 9.107 % (gap inclus), EV 1.2957 % — **REFUSE**
      - refuse : R/R 1.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 9.933 %) — p(stop avant cible) 0.3643 [0.31 ; 0.42], R/R 1.471, perte reelle 10.526 % (gap inclus), EV 1.8214 % — **REFUSE**
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.05 % > budget 12.00 %
   - ⚪ atr_grid a 2.25 ATR (stop 11.174 %) — p(stop avant cible) 0.3157 [0.27 ; 0.37], R/R 1.312, perte reelle 11.8 % (gap inclus), EV 2.0027 % — **REFUSE**
      - refuse : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.00 % > budget 12.00 %
   - 🟢 grid_snapped a 2.7 ATR (stop 14.876 %) — p(stop avant cible) 0.2025 [0.16 ; 0.25], R/R 1.003, perte reelle 15.428 % (gap inclus), EV 2.2315 % — **REFUSE**
      - refuse : R/R 1.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.11 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 17.382 %) — p(stop avant cible) 0.1253 [0.09 ; 0.16], R/R 0.868, perte reelle 17.829 % (gap inclus), EV 2.4478 % — **REFUSE**
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.50 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 19.865 %) — p(stop avant cible) 0.0786 [0.05 ; 0.11], R/R 0.765, perte reelle 20.227 % (gap inclus), EV 2.581 % — **REFUSE**
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.43 % > budget 12.00 %
   - 🟢 grid_snapped a 4.3 ATR (stop 22.825 %) — p(stop avant cible) 0.0489 [0.03 ; 0.08], R/R 0.666, perte reelle 23.235 % (gap inclus), EV 2.6002 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.19 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 24.832 %) — p(stop avant cible) 0.0328 [0.02 ; 0.06], R/R 0.609, perte reelle 25.398 % (gap inclus), EV 2.6327 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.60 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 27.315 %) — p(stop avant cible) 0.0268 [0.01 ; 0.05], R/R 0.559, perte reelle 27.709 % (gap inclus), EV 2.6403 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.33 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 29.798 %) — p(stop avant cible) 0.0225 [0.01 ; 0.04], R/R 0.515, perte reelle 30.032 % (gap inclus), EV 2.6282 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.92 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 32.281 %) — p(stop avant cible) 0.0123 [0.00 ; 0.03], R/R 0.477, perte reelle 32.435 % (gap inclus), EV 2.667 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.30 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 34.764 %) — p(stop avant cible) 0.003 [0.00 ; 0.01], R/R 0.439, perte reelle 35.257 % (gap inclus), EV 2.7563 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.82 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 37.247 %) — p(stop avant cible) 0.0019 [0.00 ; 0.01], R/R 0.416, perte reelle 37.247 % (gap inclus), EV 2.7648 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.62 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 39.731 %) — p(stop avant cible) 0.0003 [0.00 ; 0.01], R/R 0.39, perte reelle 39.731 % (gap inclus), EV 2.7792 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.32 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 116.24, ATR14 5.7729 (4.966 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.373 ATR = 1.852 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.248 % | 115.9514 | 93.05 % | 95.16 % | 96.06 % | 96.56 % | 97.05 % | 98.05 % |
| 0.1 ATR | 0.497 % | 115.6627 | 85.5 % | 90.52 % | 92.23 % | 93.73 % | 94.72 % | 96.41 % |
| 0.15 ATR | 0.745 % | 115.3741 | 77.54 % | 85.18 % | 87.99 % | 90.29 % | 92.58 % | 95.07 % |
| 0.2 ATR | 0.993 % | 115.0854 | 71.5 % | 80.14 % | 83.75 % | 86.96 % | 90.35 % | 93.22 % |
| 0.25 ATR | 1.242 % | 114.7968 | 64.65 % | 74.5 % | 79.21 % | 83.42 % | 87.7 % | 90.86 % |
| 0.35 ATR | 1.738 % | 114.2195 | 52.37 % | 65.32 % | 71.95 % | 77.55 % | 83.43 % | 87.99 % |
| 0.5 ATR | 2.483 % | 113.3536 | 37.16 % | 53.43 % | 61.15 % | 68.25 % | 76.52 % | 82.24 % |
| 0.75 ATR | 3.725 % | 111.9104 | 19.54 % | 36.09 % | 45.71 % | 55.51 % | 65.65 % | 73.1 % |
| 1.0 ATR | 4.966 % | 110.4671 | 9.26 % | 22.98 % | 32.59 % | 43.68 % | 54.98 % | 65.5 % |
| 1.25 ATR | 6.208 % | 109.0239 | 4.83 % | 14.52 % | 22.3 % | 33.37 % | 46.95 % | 58.93 % |
| 1.5 ATR | 7.449 % | 107.5807 | 2.42 % | 9.78 % | 16.15 % | 26.9 % | 40.14 % | 53.29 % |
| 2.0 ATR | 9.933 % | 104.6943 | 0.5 % | 3.83 % | 7.27 % | 15.37 % | 29.57 % | 43.84 % |
| 2.5 ATR | 12.416 % | 101.8079 | 0.1 % | 1.51 % | 3.83 % | 8.19 % | 21.44 % | 34.6 % |
| 3.0 ATR | 14.899 % | 98.9214 | 0.0 % | 0.71 % | 2.32 % | 5.26 % | 15.45 % | 26.59 % |
| 4.0 ATR | 19.865 % | 93.1486 | 0.0 % | 0.4 % | 0.91 % | 2.22 % | 6.91 % | 14.89 % |
| 6.0 ATR | 29.798 % | 81.6029 | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.32 % | 4.62 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.37 ATR | 0.42 ATR | 0.56 ATR | 0.67 ATR | 0.74 ATR | 0.98 ATR | 1.24 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.62 ATR | 0.81 ATR | 0.96 ATR | 1.09 ATR | 1.49 ATR | 1.90 ATR |
| **3 s.** | 0.31 ATR | 0.68 ATR | 0.76 ATR | 0.99 ATR | 1.18 ATR | 1.34 ATR | 1.85 ATR | 2.33 ATR |
| **5 s.** | 0.39 ATR | 0.87 ATR | 0.97 ATR | 1.26 ATR | 1.58 ATR | 1.80 ATR | 2.37 ATR | 3.09 ATR |
| **10 s.** | 0.54 ATR | 1.16 ATR | 1.32 ATR | 1.84 ATR | 2.28 ATR | 2.62 ATR | 3.64 ATR | 4.68 ATR |
| **20 s.** | 0.70 ATR | 1.67 ATR | 1.94 ATR | 2.60 ATR | 3.14 ATR | 3.56 ATR | 4.95 ATR | 5.93 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.423–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.622–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.725 %, prix 111.9101), p(touche) 36.09 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.764–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.966 %, prix 110.4675), p(touche) 32.59 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (61.2 % des re-echantillons)
- **5 seance(s)** : plage utile 0.972–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.966 %, prix 110.4675), p(touche) 43.68 % (en stress 98.99 %)  ✅ optimum identifie (62.1 % des re-echantillons)
- **10 seance(s)** : plage utile 1.322–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.449 %, prix 107.5813), p(touche) 40.14 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.939–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (9.933 %, prix 104.6939), p(touche) 43.84 % (en stress 97.96 %)  ✅ optimum identifie (65.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.011 | EV/share : $0.064 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 19 % | T3 12 %
- Kelly (position) : f* 0.007 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 75.8 | bear 19.2 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 410.0 (= 4 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.835% → cible +4.346% / stop −3.0%, p_fill 76%, n_eff≈82.1) : P(cible|rempli) **15%** · **EV/risk -0.054** (×p_fill ; si rempli -0.22% du capital)
  - **swing** (entrée dip −1.834% → cible +7.163% / stop −5.059%, p_fill 74%, n_eff≈86.3) : P(cible|rempli) **34%** · **EV/risk -0.028** (×p_fill ; si rempli -0.19% du capital)
  - **deep** (entrée dip −2.83% → cible +8.314% / stop −7.667%, p_fill 68%, n_eff≈77.0) : P(cible|rempli) **49%** · **EV/risk +0.036** (×p_fill ; si rempli +0.41% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→87% · +1.0%→78% · +2.0%→53% · +3.0%→34% · +5.0%→18% · +8.0%→6%
- Range intraday médian 4.79% (p90 8.67%) · excursion haute méd. +2.08% / basse méd. −2.24%
- Profil de vol intra : ouverture 3.563% vs midi 1.005% vs clôture 1.064% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 19% · trend ↑1%/↓0% ; spike-down 67% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.128 ; neutre — autocorr -0.028)_ ; drift intra méd. 0.578% ; recovery-V 34%
- **σ réalisé intraday** 3.483% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 42% / whipsaw 8%
- POC intraday (dernière séance, temps-au-prix) : 123.065 (VA 122.039–123.635 ; dernier close 122.07)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 40% · rebond 79% · **stop −3.96%** sous le fill (sous le bruit) · cible +2.13% · R/R 0.54 (high win-rate)
- Gaps overnight (n=159) : méd. -0.01% · baisse 50% (gap-down >1% 32% · >2% 15%)
- Excursion ouverture 5min (n=160) : bas méd −0.94% (p90 −2.69%) · haut méd +1.03% · range méd 2.22%
- Excursion ouverture 15min (n=160) : bas méd −1.3% (p90 −3.18%) · haut méd +1.42% · range méd 2.89%
- Excursion ouverture 30min (n=160) : bas méd −1.38% (p90 −3.85%) · haut méd +1.64% · range méd 3.4%
- Excursion ouverture 60min (n=160) : bas méd −1.84% (p90 −3.9%) · haut méd +1.71% · range méd 3.89%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 122.11 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 79% (123/159) · gap 42% · délai 0.0min · rebond 60% (67/123) (MFE +1.5%)
   - −1.0% : fill 30min 61% · séance 68% (108/159) · gap 32% · délai 0.0min · rebond 63% (62/108) (MFE +1.64%)
   - −1.5% : fill 30min 51% · séance 61% (99/159) · gap 24% · délai 0.6min · rebond 63% (57/99) (MFE +1.34%)
   - −2.0% : fill 30min 39% · séance 51% (88/159) · gap 15% · délai 1.4min · rebond 70% (55/88) (MFE +1.42%)
   - −3.0% : fill 30min 28% · séance 40% (67/159) · gap 8% · délai 11.2min · rebond 79% (47/67) (MFE +2.13%)
   - −4.0% : fill 30min 15% · séance 27% (48/159) · gap 3% · délai 15.4min · rebond 70% (31/48) (MFE +2.25%)
   - −5.0% : fill 30min 8% · séance 16% (32/159) · gap 2% · délai 29.7min · rebond 67% (23/32) (MFE +2.18%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.64% (p90 −2.61%) → stop au-delà de −1.73% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.65% (p90 −2.3%) → stop au-delà de −1.8% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.59% (p90 −2.35%) → stop au-delà de −1.77% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=769 jambes) : jambe baissière méd −1.12% (p90 −2.69%) · ~9.5 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 95% (72/75) · rebond 51% (36/72)
      · −2.0% : fill 82% (62/75) · rebond 65% (37/62)
      · −3.0% : fill 71% (52/75) · rebond 78% (36/52)
      · −4.0% : fill 47% (38/75) · rebond 70% (26/38)
      · −5.0% : fill 30% (27/75) · rebond 62% (18/27)
   - **flat** (17 séances) :
      · −1.0% : fill 66% (11/17) · rebond 83% (7/11)
      · −2.0% : fill 36% (9/17) · rebond 62% (6/9)
      · −3.0% : fill 11% (4/17) · rebond 18% (1/4)
      · −4.0% : fill 11% (4/17) · rebond 18% (1/4)
      · −5.0% : fill 5% (2/17) · rebond 100% (2/2)
   - **gap-up** (67 séances) :
      · −1.0% : fill 42% (25/67) · rebond 84% (19/25)
      · −2.0% : fill 23% (17/67) · rebond 91% (12/17)
      · −3.0% : fill 13% (11/67) · rebond 97% (10/11)
      · −4.0% : fill 9% (6/67) · rebond 90% (4/6)
      · −5.0% : fill 4% (3/67) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 70% si les 15 1res min sont vertes (75 cas) · 33% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **21min** → P(séance verte=clôture>ouverture) 71% si début vert vs 26% si rouge (base 50% · écart 45 pts) ; prédictivité sature ensuite (plafond brut 218min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **71%** · continue >prix actuel 53% ; creux résiduel méd -1.5% (q20 -3.06%) → **SL/trailing à −3.06%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.92% / q75 +3.55% → **scale +1.92% / runner +3.55%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **26%** (continue à baisser 59%) → **RÉDUIRE ~74%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.73%** (au-delà de la MAE q10 -3.73%), cible rebond +1.63% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.13% .. +4.75%] · haut q95 +5.22% · bas q05 -5.01%
   - 60min (n=160) : retour [-3.67% .. +5.04%] · haut q95 +6.37% · bas q05 -5.51%
   - 2h (n=160) : retour [-4.71% .. +6.52%] · haut q95 +7.73% · bas q05 -5.99%
   - 4h (n=160) : retour [-4.74% .. +7.67%] · haut q95 +8.52% · bas q05 -6.67%
   - 6h (n=160) : retour [-5.75% .. +7.98%] · haut q95 +8.81% · bas q05 -7.1%
   - session (n=160) : retour [-5.31% .. +8.28%] · haut q95 +8.89% · bas q05 -7.12%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.1% des séances sont trend-up (mild 0% / strong 8.1%) · base = 13 séances trend-up (n_eff 8.8)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 22% vs absente 2% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.92% (p75 1.49% / p90 2.51%) · ~4.0 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **78%** (reprise méd 20.0 min, n=49)
   - −1.0% → **66%** (reprise méd 38.17 min, n=22)
   - −1.5% → **48%** (reprise méd 41.9 min, n=12)
   - −2.0% → **15%** (reprise méd None min, n=6)
   - −3.0% → **20%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.51%** (p90, défaut prudent ; serré/agressif −1.49%) ; extension open→close méd +7.0% (q75 +9.08% / q95 +12.54%), MFE méd +8.53% / q90 +13.94%
   - Échelle scale-out : +8.53% (33%) / +9.52% (33%) / +13.94% (34%)
- **DÉSARMER** : repli > **−2.51%** depuis le plus-haut = décay → P(retournement) **81%** (préavis méd 284.27 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.94% : P(retournement après) 0% (mèche méd 5.8%)
- **CONTEXTE** : la dernière heure tient les gains 67% du temps (retour médian dernière heure +0.39%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.63 · part idiosyncratique 0.37
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 51.1  _(neutre)_
- **ADX** : 16.7  _(pas de tendance nette)_
- **MACD** : hist -0.387  _(bearish_recent)_
- **BB** : %B 0.51 · largeur 22.3%
- **ATR** : 5.77 (47.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.012  _(neutre)_
- **Vol ratio** : 0.59  _(volume atone)_
- **Choppiness** : 44.4  _(transition)_
- **MA** : MA20 115.89 · MA50 104.92 · MA200 94.43  _(prix > MA20)_
- **Dist MA** : MA20 +0.3% · MA50 +10.8% · MA200 +23.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (845933 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
