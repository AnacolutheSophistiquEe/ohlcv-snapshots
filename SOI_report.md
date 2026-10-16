# SOI

**Generated** : 2026-10-16T21:48:09.720765+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 5/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €128.55  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (10 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot €128.55 (+0.4% vs entrée) · entrée €128.02 · stop €124.06 · T1 €135.94 · R/R 2.0  
> ↳ _probas brutes, non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -23 % hors [0,100] (R² max 0.95). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-16 : 128.55 · ATR Wilder 9.83 (7.64 %)_
- **Swing** : plage **114.08 → 106.78** (-11.26 % a -16.94 % sous la cloture, 0.74 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 110.4-120.25 (B) ; 104.8-109.4 (A). stop INDICATIF 93.04 (-12.87 % sous le bas ; sous le support 97.95-102.4 (- 0,5 ATR)).
- **Deep** : plage **106.78 → 74.57** (-16.94 % a -41.99 % sous la cloture, 3.28 ATR) — touchee 50 % → 15 % du temps en 20 seances ; supports reels dans la plage : 104.8-109.4 (A) ; 97.95-102.4 (B) ; 91.65-96.02 (A) ; 84.75-89.15 (B) ; 77.85-82.4 (A). stop INDICATIF 67.64 (-9.29 % sous le bas ; sous le support 72.55-72.9 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (COMBO) : 4.57 ATR sous le plus haut 20 s., RSI(2) 2.6. Limite **123.64** (seance suivante), stop catastrophe 84.33, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 110.4-120.25 (B, -6.46 %) ; 116.8-120.25 (A, -6.46 %) ; 104.8-109.4 (A, -14.9 %) ; 97.95-102.4 (B, -20.34 %) ; 91.65-96.02 (A, -25.31 %) ; 84.75-89.15 (B, -30.65 %)
- Resistances reelles au-dessus : 133.95-137.95 (A, 4.2 %) ; 139.3-143.95 (A, 8.36 %) ; 144.25-148.75 (A, 12.21 %) ; 149.65-154.4 (A, 16.41 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.06 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.58 %)** : le gap seul le franchit 0.469 % des séances (6 fois sur 1280).
   - exécution **4.305 pt plus bas** dans le cas TYPIQUE (médiane), 15.426 au p90, **20.714 au pire**
   - perte réelle **15.318 %** en moyenne _(tirée par la queue)_, jusqu'à **29.294 %** — au lieu des 8.58 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0316 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.73 % | p01 -5.224 % | pire -29.294 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4257** [0.3538 ; 0.5001] _(largeur 14.6 pt, n_eff 173.1)_
   - swing : **0.3834** [0.3333 ; 0.4354] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.3684** [0.3188 ; 0.4202] _(largeur 10.1 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.65 %** | CVaR **-13.33 %** | vol 6.59 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 4.18 % contre 7.06 % aujourd'hui, rapport 0.59)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.52 % vs -11.71 % si l'on extrapolait par √5 _(rapport 1.069 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0958** (β de hausse 1.5838, asymétrie 0.6919) vs FCHI — 619 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.032× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 113.8187 sur support (1.17 ATR, 11.46 %) — p(stop avant cible) 0.3829 [0.33 ; 0.43], R/R 2.711, perte reelle 11.872 % (gap inclus), CVaR 14.615 %, EV 3.0633 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.3143 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : R/R 2.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 14.61 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.06 ATR (stop 2.903 %) — p(stop avant cible) 0.7746 [0.73 ; 0.82], R/R 10.389, perte reelle 3.098 % (gap inclus), EV 2.0368 % — **REFUSE**
      - refuse : cible atteinte seulement 8.4 % du temps (< 15 %) meme a 10 seances : le R/R de 10.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.775, borne haute 0.816 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.06 ATR du spot — compartiment <1, mesure a 49.8 % de casse (IC clusterise [0.466 ; 0.530] sur 1220 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 1.17 ATR (stop 11.46 %) — p(stop avant cible) 0.3829 [0.33 ; 0.43], R/R 2.711, perte reelle 11.872 % (gap inclus), EV 3.0633 % — **REFUSE**
      - refuse : R/R 2.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.61 % > budget 12.00 %
   - 🟢 support a 2.33 ATR (stop 20.406 %) — p(stop avant cible) 0.1241 [0.09 ; 0.16], R/R 1.544, perte reelle 20.845 % (gap inclus), EV 4.2619 % — **REFUSE**
      - refuse : R/R 1.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.49 % > budget 12.00 %
   - ⚪ atr_grid a 0.75 ATR (stop 5.782 %) — p(stop avant cible) 0.5986 [0.55 ; 0.65], R/R 5.168, perte reelle 6.227 % (gap inclus), EV 2.9565 % — **REFUSE**
      - refuse : cible atteinte seulement 12.6 % du temps (< 15 %) meme a 10 seances : le R/R de 5.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.599, borne haute 0.649 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.75 ATR (stop 13.492 %) — p(stop avant cible) 0.3131 [0.27 ; 0.36], R/R 2.306, perte reelle 13.955 % (gap inclus), EV 3.2167 % — **REFUSE**
      - refuse : R/R 2.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.39 % > budget 12.00 %
   - ⚪ atr_grid a 2.0 ATR (stop 15.419 %) — p(stop avant cible) 0.2536 [0.21 ; 0.30], R/R 2.034, perte reelle 15.825 % (gap inclus), EV 3.4352 % — **REFUSE**
      - refuse : R/R 2.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.48 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 23.129 %) — p(stop avant cible) 0.0782 [0.05 ; 0.11], R/R 1.359, perte reelle 23.68 % (gap inclus), EV 4.3841 % — **REFUSE**
      - refuse : R/R 1.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.99 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 26.984 %) — p(stop avant cible) 0.0417 [0.02 ; 0.07], R/R 1.174, perte reelle 27.422 % (gap inclus), EV 4.4301 % — **REFUSE**
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.71 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 30.838 %) — p(stop avant cible) 0.027 [0.01 ; 0.05], R/R 1.041, perte reelle 30.901 % (gap inclus), EV 4.4154 % — **REFUSE**
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.25 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 34.693 %) — p(stop avant cible) 0.0221 [0.01 ; 0.04], R/R 0.927, perte reelle 34.728 % (gap inclus), EV 4.365 % — **REFUSE**
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.24 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 38.548 %) — p(stop avant cible) 0.0094 [0.00 ; 0.02], R/R 0.835, perte reelle 38.548 % (gap inclus), EV 4.385 % — **REFUSE**
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.83 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 42.403 %) — p(stop avant cible) 0.0016 [0.00 ; 0.01], R/R 0.759, perte reelle 42.403 % (gap inclus), EV 4.419 % — **REFUSE**
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.13 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 46.258 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.696, perte reelle 46.258 % (gap inclus), EV 4.4354 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.83 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 50.113 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.642, perte reelle 50.113 % (gap inclus), EV 4.4354 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.83 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 53.967 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.596, perte reelle 53.967 % (gap inclus), EV 4.4354 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.83 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 57.822 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.557, perte reelle 57.822 % (gap inclus), EV 4.4354 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.83 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 61.677 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.522, perte reelle 61.677 % (gap inclus), EV 4.4354 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.83 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 128.55, ATR14 9.9107 (7.71 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.359 ATR = 2.768 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.385 % | 128.0545 | 91.18 % | 94.21 % | 95.48 % | 96.56 % | 97.73 % | 98.7 % |
| 0.1 ATR | 0.771 % | 127.5589 | 84.8 % | 89.89 % | 91.75 % | 94.29 % | 96.04 % | 97.2 % |
| 0.15 ATR | 1.156 % | 127.0634 | 77.94 % | 84.99 % | 87.62 % | 90.85 % | 93.57 % | 95.1 % |
| 0.2 ATR | 1.542 % | 126.5679 | 69.12 % | 79.59 % | 83.4 % | 87.6 % | 91.1 % | 93.01 % |
| 0.25 ATR | 1.927 % | 126.0723 | 62.65 % | 75.76 % | 79.96 % | 85.83 % | 89.71 % | 92.41 % |
| 0.35 ATR | 2.698 % | 125.0813 | 50.88 % | 67.32 % | 72.99 % | 80.61 % | 85.36 % | 89.71 % |
| 0.5 ATR | 3.855 % | 123.5946 | 35.88 % | 55.15 % | 62.38 % | 72.64 % | 80.51 % | 86.81 % |
| 0.75 ATR | 5.782 % | 121.117 | 17.16 % | 35.03 % | 46.27 % | 57.78 % | 71.91 % | 79.92 % |
| 1.0 ATR | 7.71 % | 118.6393 | 8.24 % | 23.55 % | 33.79 % | 46.85 % | 63.7 % | 74.43 % |
| 1.25 ATR | 9.637 % | 116.1616 | 4.12 % | 15.7 % | 25.15 % | 37.01 % | 55.79 % | 69.03 % |
| 1.5 ATR | 11.564 % | 113.6839 | 2.25 % | 10.7 % | 18.37 % | 29.43 % | 47.77 % | 62.64 % |
| 2.0 ATR | 15.419 % | 108.7286 | 0.59 % | 4.61 % | 9.14 % | 18.01 % | 34.32 % | 52.15 % |
| 2.5 ATR | 19.274 % | 103.7732 | 0.29 % | 2.45 % | 5.01 % | 11.61 % | 23.74 % | 44.36 % |
| 3.0 ATR | 23.129 % | 98.8179 | 0.2 % | 0.79 % | 2.55 % | 7.19 % | 16.42 % | 36.36 % |
| 4.0 ATR | 30.838 % | 88.9072 | 0.1 % | 0.59 % | 1.38 % | 3.54 % | 9.4 % | 23.18 % |
| 6.0 ATR | 46.258 % | 69.0857 | 0.0 % | 0.29 % | 0.79 % | 1.57 % | 4.45 % | 11.99 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.36 ATR | 0.41 ATR | 0.54 ATR | 0.65 ATR | 0.71 ATR | 0.95 ATR | 1.20 ATR |
| **2 s.** | 0.26 ATR | 0.56 ATR | 0.63 ATR | 0.79 ATR | 0.97 ATR | 1.11 ATR | 1.56 ATR | 1.97 ATR |
| **3 s.** | 0.32 ATR | 0.69 ATR | 0.78 ATR | 1.02 ATR | 1.26 ATR | 1.44 ATR | 1.95 ATR | 2.50 ATR |
| **5 s.** | 0.46 ATR | 0.93 ATR | 1.05 ATR | 1.38 ATR | 1.69 ATR | 1.91 ATR | 2.68 ATR | 3.60 ATR |
| **10 s.** | 0.66 ATR | 1.43 ATR | 1.60 ATR | 2.06 ATR | 2.44 ATR | 2.75 ATR | 3.92 ATR | 5.78 ATR |
| **20 s.** | 0.97 ATR | 2.14 ATR | 2.46 ATR | 3.25 ATR | 3.86 ATR | 4.57 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.409–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (66.4 % des re-echantillons)
- **2 seance(s)** : plage utile 0.626–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.775–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.047–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 15.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.603–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 20.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.459–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 24.6 | bear 5.0 | side 70.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 257.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.418% → cible +6.189% / stop −3.095%, p_fill 85%, n_eff≈92.6) : P(cible|rempli) **16%** · **EV/risk -0.091** (×p_fill ; si rempli -0.33% du capital)
  - **swing** (entrée dip −0.739% → cible +15.798% / stop −7.899%, p_fill 88%, n_eff≈102.1) : P(cible|rempli) **25%** · **EV/risk +0.040** (×p_fill ; si rempli +0.36% du capital)
  - **deep** (entrée dip −1.016% → cible +16.12% / stop −11.683%, p_fill 88%, n_eff≈98.7) : P(cible|rempli) **42%** · **EV/risk +0.016** (×p_fill ; si rempli +0.21% du capital)
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
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.55 · part idiosyncratique 0.45
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 41.8  _(momentum baissier)_
- **ADX** : 23.9  _(pas de tendance nette)_
- **MACD** : hist -4.629  _(pas de croisement recent)_
- **BB** : %B -0.01 · largeur 30.2%
- **ATR** : 9.91 (65.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.132  _(distribution)_
- **Vol ratio** : 0.95  _(volume normal)_
- **Choppiness** : 39.4  _(transition)_
- **MA** : MA20 151.71 · MA50 135.19 · MA200 99.18  _(prix < MA20)_
- **Dist MA** : MA20 -15.3% · MA50 -4.9% · MA200 +29.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (781381 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
