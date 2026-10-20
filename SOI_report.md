# SOI

**Generated** : 2026-10-20T21:47:45.748072+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 5/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €123.65  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (12 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot €123.65 (+1.0% vs entrée) · entrée €122.38 · stop €119.45 · T1 €127.02 · R/R 1.58  
> ↳ ¼-Kelly 0.027 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.4% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -35 % hors [0,100] (R² max 0.95). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-20 : 123.65 · ATR Wilder 9.55 (7.72 %)_
- **Swing** : plage **109.47 → 102.45** (-11.47 % a -17.14 % sous la cloture, 0.74 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 104.8-109.4 (A). stop INDICATIF 93.18 (-9.05 % sous le bas ; sous le support 97.95-102.4 (- 0,5 ATR)).
- **Deep** : plage **102.45 → 71.2** (-17.14 % a -42.41 % sous la cloture, 3.27 ATR) — touchee 50 % → 15 % du temps en 20 seances ; supports reels dans la plage : 97.95-102.4 (B) ; 91.65-96.02 (A) ; 84.75-89.15 (B) ; 77.85-82.4 (A) ; 72.55-72.9 (C). stop INDICATIF 59.43 (-16.54 % sous le bas ; sous le support 64.2-68.5 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 5.22 ATR sous le plus haut 20 s., RSI(2) 0.9. Limite **118.88** (seance suivante), stop catastrophe 80.69, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 116.8-120.25 (A, -2.75 %) ; 110.4-120.15 (B, -2.83 %) ; 104.8-109.4 (A, -11.52 %) ; 97.95-102.4 (B, -17.19 %) ; 91.65-96.02 (A, -22.35 %) ; 84.75-89.15 (B, -27.9 %)
- Resistances reelles au-dessus : 126.65-128.0 (A, 2.43 %) ; 132.0-136.1 (A, 6.75 %) ; 137.5-140.8 (A, 11.2 %) ; 142.9-146.0 (A, 15.57 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.06 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.17 %)** : le gap seul le franchit 0.234 % des séances (3 fois sur 1280).
   - exécution **8.549 pt plus bas** dans le cas TYPIQUE (médiane), 17.009 au p90, **19.124 au pire**
   - perte réelle **21.456 %** en moyenne _(tirée par la queue)_, jusqu'à **29.294 %** — au lieu des 10.17 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0265 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.73 % | p01 -5.224 % | pire -29.294 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4954** [0.4215 ; 0.5694] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.3708** [0.3211 ; 0.4226] _(largeur 10.1 pt, n_eff 345.8)_
   - deep : **0.3284** [0.2805 ; 0.3792] _(largeur 9.9 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.65 %** | CVaR **-13.33 %** | vol 6.59 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 4.18 % contre 6.80 % aujourd'hui, rapport 0.61)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.71 % vs -11.71 % si l'on extrapolait par √5 _(rapport 1.085 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0875** (β de hausse 1.5828, asymétrie 0.687) vs FCHI — 620 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.014× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 113.974 sur support (0.68 ATR, 7.825 %) — p(stop avant cible) 0.5347 [0.48 ; 0.59], R/R 3.374, perte reelle 8.198 % (gap inclus), CVaR 11.651 %, EV 2.128 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.0669 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.535, borne haute 0.587 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.68 ATR (stop 7.825 %) — p(stop avant cible) 0.5347 [0.48 ; 0.59], R/R 3.374, perte reelle 8.198 % (gap inclus), EV 2.128 % — **REFUSE**
      - refuse : p_stop_first 0.535, borne haute 0.587 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.52 ATR du spot — compartiment <1, mesure a 47.9 % de casse (IC clusterise [0.446 ; 0.513] sur 1112 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_based a 1.5 ATR (stop 11.88 %) — p(stop avant cible) 0.3829 [0.33 ; 0.43], R/R 2.258, perte reelle 12.249 % (gap inclus), EV 2.411 % — **REFUSE**
      - refuse : R/R 2.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.70 % > budget 12.00 %
   - 🟢 support a 1.85 ATR (stop 17.126 %) — p(stop avant cible) 0.2157 [0.17 ; 0.26], R/R 1.569, perte reelle 17.626 % (gap inclus), EV 3.0964 % — **REFUSE**
      - refuse : R/R 1.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.28 % > budget 12.00 %
   - 🟢 support a 4.29 ATR (stop 36.406 %) — p(stop avant cible) 0.0172 [0.01 ; 0.04], R/R 0.757, perte reelle 36.561 % (gap inclus), EV 3.5744 % — **REFUSE**
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.86 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.98 %) — p(stop avant cible) 0.8289 [0.79 ; 0.87], R/R 13.284, perte reelle 2.082 % (gap inclus), EV 1.5834 % — **REFUSE**
      - refuse : cible atteinte seulement 7.4 % du temps (< 15 %) meme a 10 seances : le R/R de 13.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.829, borne haute 0.866 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.25 ATR (stop 9.9 %) — p(stop avant cible) 0.4472 [0.40 ; 0.50], R/R 2.691, perte reelle 10.28 % (gap inclus), EV 2.3333 % — **REFUSE**
      - refuse : R/R 2.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.29 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 19.8 %) — p(stop avant cible) 0.1608 [0.12 ; 0.20], R/R 1.36, perte reelle 20.333 % (gap inclus), EV 3.4344 % — **REFUSE**
      - refuse : R/R 1.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.51 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 21.78 %) — p(stop avant cible) 0.1103 [0.08 ; 0.15], R/R 1.244, perte reelle 22.242 % (gap inclus), EV 3.5638 % — **REFUSE**
      - refuse : R/R 1.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.80 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 23.759 %) — p(stop avant cible) 0.0759 [0.05 ; 0.11], R/R 1.142, perte reelle 24.21 % (gap inclus), EV 3.6774 % — **REFUSE**
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.44 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 27.719 %) — p(stop avant cible) 0.0455 [0.03 ; 0.07], R/R 0.988, perte reelle 27.991 % (gap inclus), EV 3.6134 % — **REFUSE**
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.65 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 31.679 %) — p(stop avant cible) 0.0267 [0.01 ; 0.05], R/R 0.873, perte reelle 31.687 % (gap inclus), EV 3.6051 % — **REFUSE**
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.22 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 39.599 %) — p(stop avant cible) 0.0062 [0.00 ; 0.02], R/R 0.699, perte reelle 39.599 % (gap inclus), EV 3.5994 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.34 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 43.559 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.635, perte reelle 43.559 % (gap inclus), EV 3.6461 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.40 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 47.519 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.582, perte reelle 47.519 % (gap inclus), EV 3.6461 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.40 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 51.479 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.537, perte reelle 51.479 % (gap inclus), EV 3.6461 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.40 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 55.439 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.499, perte reelle 55.439 % (gap inclus), EV 3.6461 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.40 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 59.399 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.466, perte reelle 59.399 % (gap inclus), EV 3.6461 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.40 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 63.359 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.437, perte reelle 63.359 % (gap inclus), EV 3.6461 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.40 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 123.65, ATR14 9.7929 (7.92 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.36 ATR = 2.851 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.396 % | 123.1604 | 91.18 % | 94.21 % | 95.48 % | 96.56 % | 97.73 % | 98.7 % |
| 0.1 ATR | 0.792 % | 122.6707 | 84.8 % | 89.89 % | 91.75 % | 94.29 % | 96.04 % | 97.2 % |
| 0.15 ATR | 1.188 % | 122.1811 | 77.94 % | 84.99 % | 87.62 % | 90.85 % | 93.57 % | 95.1 % |
| 0.2 ATR | 1.584 % | 121.6914 | 69.22 % | 79.69 % | 83.5 % | 87.7 % | 91.2 % | 93.11 % |
| 0.25 ATR | 1.98 % | 121.2018 | 62.75 % | 75.86 % | 80.06 % | 85.93 % | 89.81 % | 92.51 % |
| 0.35 ATR | 2.772 % | 120.2225 | 50.98 % | 67.42 % | 73.08 % | 80.71 % | 85.46 % | 89.81 % |
| 0.5 ATR | 3.96 % | 118.7536 | 35.88 % | 55.25 % | 62.48 % | 72.74 % | 80.61 % | 86.91 % |
| 0.75 ATR | 5.94 % | 116.3054 | 17.06 % | 35.13 % | 46.37 % | 57.87 % | 72.01 % | 80.02 % |
| 1.0 ATR | 7.92 % | 113.8571 | 8.14 % | 23.45 % | 33.79 % | 46.95 % | 63.8 % | 74.53 % |
| 1.25 ATR | 9.9 % | 111.4089 | 4.12 % | 15.7 % | 25.25 % | 37.2 % | 55.98 % | 69.23 % |
| 1.5 ATR | 11.88 % | 108.9607 | 2.25 % | 10.7 % | 18.47 % | 29.63 % | 47.97 % | 62.84 % |
| 2.0 ATR | 15.84 % | 104.0643 | 0.59 % | 4.61 % | 9.23 % | 18.21 % | 34.52 % | 52.25 % |
| 2.5 ATR | 19.8 % | 99.1679 | 0.29 % | 2.45 % | 5.01 % | 11.81 % | 23.94 % | 44.46 % |
| 3.0 ATR | 23.759 % | 94.2714 | 0.2 % | 0.79 % | 2.55 % | 7.28 % | 16.62 % | 36.36 % |
| 4.0 ATR | 31.679 % | 84.4786 | 0.1 % | 0.59 % | 1.38 % | 3.54 % | 9.59 % | 23.18 % |
| 6.0 ATR | 47.519 % | 64.8929 | 0.0 % | 0.29 % | 0.79 % | 1.57 % | 4.45 % | 11.99 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.36 ATR | 0.41 ATR | 0.54 ATR | 0.65 ATR | 0.71 ATR | 0.95 ATR | 1.20 ATR |
| **2 s.** | 0.26 ATR | 0.56 ATR | 0.63 ATR | 0.80 ATR | 0.97 ATR | 1.11 ATR | 1.56 ATR | 1.97 ATR |
| **3 s.** | 0.32 ATR | 0.69 ATR | 0.78 ATR | 1.02 ATR | 1.26 ATR | 1.44 ATR | 1.96 ATR | 2.50 ATR |
| **5 s.** | 0.46 ATR | 0.93 ATR | 1.05 ATR | 1.39 ATR | 1.70 ATR | 1.92 ATR | 2.70 ATR | 3.61 ATR |
| **10 s.** | 0.66 ATR | 1.44 ATR | 1.61 ATR | 2.07 ATR | 2.45 ATR | 2.77 ATR | 3.94 ATR | 5.79 ATR |
| **20 s.** | 0.98 ATR | 2.14 ATR | 2.46 ATR | 3.25 ATR | 3.86 ATR | 4.57 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.409–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (64.2 % des re-echantillons)
- **2 seance(s)** : plage utile 0.627–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.777–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.05–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 16.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.61–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 18.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.465–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.077 | EV/share : €0.226 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 40 % | T2 — | T3 —
- Kelly (position) : f* 0.109 | ¼-Kelly 0.027 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 10.0 | bear 5.0 | side 85.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 124.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.024% → cible +3.789% / stop −2.4%, p_fill 77%, n_eff≈84.6) : P(cible|rempli) **31%** · **EV/risk -0.039** (×p_fill ; si rempli -0.12% du capital)
  - **swing** (entrée dip −2.25% → cible +12.486% / stop −8.102%, p_fill 62%, n_eff≈73.2) : P(cible|rempli) **26%** · **EV/risk -0.044** (×p_fill ; si rempli -0.57% du capital)
  - **deep** (entrée dip −3.48% → cible +13.918% / stop −12.308%, p_fill 67%, n_eff≈76.7) : P(cible|rempli) **40%** · **EV/risk -0.047** (×p_fill ; si rempli -0.87% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→79% · +2.0%→66% · +3.0%→55% · +5.0%→38% · +8.0%→18%
- Range intraday médian 7.97% (p90 14.88%) · excursion haute méd. +3.44% / basse méd. −3.03%
- Profil de vol intra : ouverture 4.948% vs midi 1.438% vs clôture 2.123% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 12% · trend ↑1%/↓2% ; spike-down 69% · recovery-V 43%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; neutre — autocorr -0.021)_ ; drift intra méd. 0.659% ; recovery-V 45%
- **σ réalisé intraday** 3.905% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 68% / bas 55% / whipsaw 29%
- POC intraday (dernière séance, temps-au-prix) : 164.595 (VA 162.435–167.025 ; dernier close 169.06)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 41% · rebond 75% · **stop −7.26%** sous le fill (sous le bruit) · cible +3.18% · R/R 0.44 (high win-rate)
- Gaps overnight (n=159) : méd. 0.49% · baisse 39% (gap-down >1% 24% · >2% 15%)
- Excursion ouverture 5min (n=160) : bas méd −0.97% (p90 −2.92%) · haut méd +0.92% · range méd 2.17%
- Excursion ouverture 15min (n=160) : bas méd −1.24% (p90 −4.28%) · haut méd +1.17% · range méd 2.96%
- Excursion ouverture 30min (n=160) : bas méd −1.48% (p90 −4.65%) · haut méd +1.29% · range méd 3.39%
- Excursion ouverture 60min (n=160) : bas méd −1.63% (p90 −4.95%) · haut méd +1.46% · range méd 3.65%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 170.7 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 74% (121/159) · gap 30% · délai 0.2min · rebond 74% (87/121) (MFE +2.15%)
   - −1.0% : fill 30min 53% · séance 69% (112/159) · gap 24% · délai 0.2min · rebond 74% (82/112) (MFE +2.11%)
   - −1.5% : fill 30min 46% · séance 60% (102/159) · gap 17% · délai 1.4min · rebond 76% (77/102) (MFE +2.4%)
   - −2.0% : fill 30min 40% · séance 55% (94/159) · gap 15% · délai 4.7min · rebond 74% (73/94) (MFE +2.54%)
   - −3.0% : fill 30min 26% · séance 41% (75/159) · gap 8% · délai 3.3min · rebond 75% (63/75) (MFE +3.18%)
   - −4.0% : fill 30min 19% · séance 34% (64/159) · gap 5% · délai 15.0min · rebond 77% (53/64) (MFE +2.54%)
   - −5.0% : fill 30min 12% · séance 27% (50/159) · gap 2% · délai 53.0min · rebond 67% (38/50) (MFE +2.27%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.7% (p90 −3.21%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.61% (p90 −2.3%) → stop au-delà de −1.91% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.8% (p90 −2.29%) → stop au-delà de −1.9% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1335 jambes) : jambe baissière méd −1.24% (p90 −3.03%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 93% (53/56) · rebond 67% (35/53)
      · −2.0% : fill 90% (51/56) · rebond 72% (38/51)
      · −3.0% : fill 73% (45/56) · rebond 73% (37/45)
      · −4.0% : fill 63% (39/56) · rebond 85% (35/39)
      · −5.0% : fill 50% (32/56) · rebond 74% (26/32)
   - **flat** (13 séances) :
      · −1.0% : fill 78% (11/13) · rebond 86% (9/11)
      · −2.0% : fill 68% (10/13) · rebond 88% (9/10)
      · −3.0% : fill 66% (9/13) · rebond 64% (7/9)
      · −4.0% : fill 60% (8/13) · rebond 79% (6/8)
      · −5.0% : fill 44% (7/13) · rebond 45% (5/7)
   - **gap-up** (90 séances) :
      · −1.0% : fill 54% (48/90) · rebond 78% (38/48)
      · −2.0% : fill 33% (33/90) · rebond 73% (26/33)
      · −3.0% : fill 18% (21/90) · rebond 87% (19/21)
      · −4.0% : fill 13% (17/90) · rebond 56% (12/17)
      · −5.0% : fill 10% (11/90) · rebond 60% (7/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 54% en base · 68% si les 15 1res min sont vertes (77 cas) · 41% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:25** → P(séance verte=clôture>ouverture) 78% si début vert vs 33% si rouge (base 54% · écart 45 pts) ; prédictivité sature ensuite (plafond brut 272min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **78%** · continue >prix actuel 62% ; creux résiduel méd -1.36% (q20 -3.77%) → **SL/trailing à −3.77%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.91% / q75 +4.81% → **scale +2.91% / runner +4.81%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **33%** (continue à baisser 50%) → **RÉDUIRE ~67%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.35%** (au-delà de la MAE q10 -7.35%), cible rebond +2.38% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.59% .. +5.74%] · haut q95 +6.51% · bas q05 -5.93%
   - 60min (n=160) : retour [-5.37% .. +4.91%] · haut q95 +7.61% · bas q05 -6.55%
   - 2h (n=160) : retour [-6.01% .. +5.57%] · haut q95 +7.84% · bas q05 -7.41%
   - 4h (n=160) : retour [-6.76% .. +7.19%] · haut q95 +8.48% · bas q05 -8.09%
   - 6h (n=160) : retour [-7.59% .. +8.57%] · haut q95 +9.11% · bas q05 -9.35%
   - session (n=160) : retour [-7.86% .. +8.91%] · haut q95 +11.32% · bas q05 -10.78%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 6.6)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **37%**. Lecture précoce 30 min : signature présente → 21% vs absente 2% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.98% (p75 1.39% / p90 1.98%) · ~4.89 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **90%** (reprise méd 25.0 min, n=57)
   - −1.0% → **90%** (reprise méd 45.44 min, n=31)
   - −1.5% → **80%** (reprise méd 50.92 min, n=16)
   - −2.0% → **85%** (reprise méd 52.07 min, n=12)
   - −3.0% → **100%** (reprise méd 60.96 min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.98%** (p90, défaut prudent ; serré/agressif −1.39%) ; extension open→close méd +8.74% (q75 +9.15% / q95 +13.89%), MFE méd +9.28% / q90 +14.1%
   - Échelle scale-out : +9.28% (33%) / +9.96% (33%) / +14.1% (34%)
- **DÉSARMER** : repli > **−1.98%** depuis le plus-haut = décay → P(retournement) **15%** (préavis méd 36.46 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +14.1% : P(retournement après) 0% (mèche méd 2.71%)
- **CONTEXTE** : la dernière heure tient les gains 79% du temps (retour médian dernière heure +1.27%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.52 · part idiosyncratique 0.48
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 29.1  _(survente)_
- **ADX** : 24.2  _(pas de tendance nette)_
- **MACD** : hist -5.103  _(pas de croisement recent)_
- **BB** : %B 0.04 · largeur 37.2%
- **ATR** : 9.79 (65.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.162  _(distribution)_
- **Vol ratio** : 1.62  _(volume au-dessus de la moyenne)_
- **Choppiness** : 35.8  _(marche directionnel)_
- **MA** : MA20 148.97 · MA50 135.38 · MA200 100.18  _(prix < MA20)_
- **Dist MA** : MA20 -17.0% · MA50 -8.7% · MA200 +23.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (753850 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
