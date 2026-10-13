# SMCI

**Generated** : 2026-10-13T22:02:27.074461+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $39.07  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot $39.07 (+10.8% vs entrée) · entrée $35.25 · stop $32.98 · T1 $39.24 · R/R 1.76  
> ↳ ¼-Kelly 0.018 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -118 % hors [0,100] (R² max 0.93). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-13 : 39.07 · ATR Wilder 2.31 (5.91 %)_
- **Swing** : plage **36.23 → 34.57** (-7.27 % a -11.53 % sous la cloture, 0.72 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 35.36-36.37 (A) ; 33.86-34.98 (A). stop INDICATIF 31.43 (-9.06 % sous le bas ; sous le support 32.59-33.64 (- 0,5 ATR)).
- **Deep** : plage **34.57 → 29.54** (-11.53 % a -24.4 % sous la cloture, 2.18 ATR) — touchee 44 % → 15 % du temps en 20 seances ; supports reels dans la plage : 33.86-34.98 (A) ; 31.03-33.94 (B) ; 32.59-33.64 (B) ; 29.68-30.65 (B). stop INDICATIF 27.35 (-7.41 % sous le bas ; sous le support 28.5-29.49 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (2.9 ATR sous le plus haut 20 s., RSI(2) 4.8 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 36.8-37.85 (B, -3.12 %) ; 35.36-36.37 (A, -6.91 %) ; 33.86-34.98 (A, -10.47 %) ; 31.03-33.94 (B, -13.13 %) ; 32.59-33.64 (B, -13.9 %) ; 29.68-30.65 (B, -21.55 %)
- Resistances reelles au-dessus : 40.74-41.53 (A, 4.27 %) ; 42.31-43.39 (B, 8.29 %) ; 43.69-44.72 (A, 11.82 %) ; 44.99-45.99 (A, 15.15 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.90 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (15.59 %)** : le gap seul le franchit 0.399 % des séances (5 fois sur 1253).
   - exécution **9.067 pt plus bas** dans le cas TYPIQUE (médiane), 12.585 au p90, **13.461 au pire**
   - perte réelle **23.404 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 15.59 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0312 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.795 % | p01 -10.307 % | pire -29.051 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4567** [0.3837 ; 0.5311] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4565** [0.4045 ; 0.5092] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.351** [0.3021 ; 0.4024] _(largeur 10.0 pt, n_eff 345.7)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_target_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 24.5 observations effectives », dont la borne haute a 95 % vaut environ 12.3 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (36.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.54 %** | CVaR **-12.24 %** | vol 5.8 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 3.66 % contre 6.50 % aujourd'hui, rapport 0.56)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.69 % vs -16.48 % si l'on extrapolait par √5 _(rapport 1.013 ; < 1 = le √5 surestime)_
- **β de baisse : 1.5095** (β de hausse 1.2181, asymétrie 1.2393) vs IWM — 606 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.733× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 37.3632 sur atr_grid (0.75 ATR, 4.369 %) — p(stop avant cible) 0.6921 [0.64 ; 0.74], R/R 2.706, perte reelle 4.976 % (gap inclus), CVaR 12.459 %, EV 0.042 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.4798 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.692, borne haute 0.739 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 12.46 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 23 des 23 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 38.9 % de la queue et il ne reste que -829.92 EUR a partager. Prix du risque -0.253 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 8.737 %) — p(stop avant cible) 0.4168 [0.37 ; 0.47], R/R 1.306, perte reelle 10.314 % (gap inclus), EV 0.5903 % — **REFUSE**
      - refuse : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.69 % > budget 12.00 %
   - ⚪ sr_based a 3.15 ATR (stop 21.262 %) — p(stop avant cible) 0.1153 [0.08 ; 0.15], R/R 0.583, perte reelle 23.116 % (gap inclus), EV 1.8851 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.54 % > budget 12.00 %
   - 🟢 support a 4.99 ATR (stop 31.994 %) — p(stop avant cible) 0.0654 [0.04 ; 0.10], R/R 0.419, perte reelle 32.13 % (gap inclus), EV 1.541 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.17 % > budget 12.00 %
   - 🟢 support a 6.0 ATR (stop 37.881 %) — p(stop avant cible) 0.0361 [0.02 ; 0.06], R/R 0.355, perte reelle 37.918 % (gap inclus), EV 1.4697 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.40 % > budget 12.00 %
   - 🔴 support a 6.89 ATR (stop 43.077 %) — p(stop avant cible) 0.0034 [0.00 ; 0.01], R/R 0.313, perte reelle 43.077 % (gap inclus), EV 1.614 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.95 % > budget 12.00 %
      - ⚠ support DETECTE a 6.89 ATR du spot — compartiment >=6, mesure a 45.1 % de casse (IC clusterise [0.312 ; 0.590] sur 51 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_grid a 0.25 ATR (stop 1.456 %) — p(stop avant cible) 0.8914 [0.86 ; 0.92], R/R 8.132, perte reelle 1.656 % (gap inclus), EV -0.0363 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 8.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.891, borne haute 0.921 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 10.6 % x 13.47 % + P(rien) 0.3 % x 5.93 % ne couvrent pas P(stop) 89.1 % x 1.66 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 2.912 %) — p(stop avant cible) 0.7827 [0.74 ; 0.82], R/R 4.113, perte reelle 3.274 % (gap inclus), EV 0.1136 % — **REFUSE**
      - refuse : p_stop_first 0.783, borne haute 0.824 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 4.369 %) — p(stop avant cible) 0.6921 [0.64 ; 0.74], R/R 2.706, perte reelle 4.976 % (gap inclus), EV 0.042 % — **REFUSE**
      - refuse : p_stop_first 0.692, borne haute 0.739 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.46 % > budget 12.00 %
   - ⚪ atr_grid a 1.0 ATR (stop 5.825 %) — p(stop avant cible) 0.6026 [0.55 ; 0.65], R/R 2.024, perte reelle 6.654 % (gap inclus), EV 0.1867 % — **REFUSE**
      - refuse : p_stop_first 0.603, borne haute 0.653 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.55 % > budget 12.00 %
   - ⚪ atr_grid a 1.25 ATR (stop 7.281 %) — p(stop avant cible) 0.5111 [0.46 ; 0.56], R/R 1.573, perte reelle 8.563 % (gap inclus), EV 0.2521 % — **REFUSE**
      - refuse : p_stop_first 0.511, borne haute 0.564 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.81 % > budget 12.00 %
   - ⚪ atr_grid a 1.75 ATR (stop 10.193 %) — p(stop avant cible) 0.3705 [0.32 ; 0.42], R/R 1.137, perte reelle 11.845 % (gap inclus), EV 0.629 % — **REFUSE**
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.25 % > budget 12.00 %
   - ⚪ atr_grid a 2.0 ATR (stop 11.649 %) — p(stop avant cible) 0.3007 [0.25 ; 0.35], R/R 0.996, perte reelle 13.523 % (gap inclus), EV 1.0516 % — **REFUSE**
      - refuse : R/R 1.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.74 % > budget 12.00 %
   - ⚪ atr_grid a 2.25 ATR (stop 13.106 %) — p(stop avant cible) 0.2476 [0.20 ; 0.30], R/R 0.89, perte reelle 15.132 % (gap inclus), EV 1.3287 % — **REFUSE**
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.00 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 14.562 %) — p(stop avant cible) 0.2096 [0.17 ; 0.25], R/R 0.805, perte reelle 16.724 % (gap inclus), EV 1.3626 % — **REFUSE**
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.54 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 16.018 %) — p(stop avant cible) 0.1833 [0.15 ; 0.23], R/R 0.73, perte reelle 18.436 % (gap inclus), EV 1.4525 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.56 % > budget 12.00 %
   - ⚪ grid_snapped a 3.15 ATR (stop 20.091 %) — p(stop avant cible) 0.1239 [0.09 ; 0.16], R/R 0.607, perte reelle 22.201 % (gap inclus), EV 1.9263 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.28 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 23.299 %) — p(stop avant cible) 0.1017 [0.07 ; 0.14], R/R 0.537, perte reelle 25.065 % (gap inclus), EV 1.8275 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.89 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 26.211 %) — p(stop avant cible) 0.0775 [0.05 ; 0.11], R/R 0.495, perte reelle 27.218 % (gap inclus), EV 1.8285 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.77 % > budget 12.00 %
   - 🟢 grid_snapped a 4.99 ATR (stop 30.823 %) — p(stop avant cible) 0.0685 [0.05 ; 0.10], R/R 0.435, perte reelle 30.936 % (gap inclus), EV 1.6059 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.98 % > budget 12.00 %
   - 🟢 grid_snapped a 6.0 ATR (stop 36.71 %) — p(stop avant cible) 0.0504 [0.03 ; 0.08], R/R 0.366, perte reelle 36.747 % (gap inclus), EV 1.3794 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.75 % > budget 12.00 %
   - 🔴 grid_snapped a 6.89 ATR (stop 41.906 %) — p(stop avant cible) 0.0074 [0.00 ; 0.02], R/R 0.321, perte reelle 41.961 % (gap inclus), EV 1.6111 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.98 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 46.598 %) — p(stop avant cible) 0.0021 [0.00 ; 0.01], R/R 0.285, perte reelle 47.253 % (gap inclus), EV 1.6094 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.07 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 39.07, ATR14 2.2757 (5.825 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.344 ATR = 2.004 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.291 % | 38.9562 | 90.74 % | 93.55 % | 94.95 % | 95.45 % | 96.65 % | 97.84 % |
| 0.1 ATR | 0.582 % | 38.8424 | 82.28 % | 87.5 % | 89.51 % | 91.41 % | 93.19 % | 95.17 % |
| 0.15 ATR | 0.874 % | 38.7286 | 75.13 % | 82.36 % | 85.27 % | 88.47 % | 90.85 % | 93.84 % |
| 0.2 ATR | 1.165 % | 38.6149 | 68.28 % | 77.62 % | 80.83 % | 85.95 % | 89.33 % | 92.51 % |
| 0.25 ATR | 1.456 % | 38.5011 | 62.03 % | 72.88 % | 76.49 % | 82.51 % | 87.2 % | 90.76 % |
| 0.35 ATR | 2.039 % | 38.2735 | 49.24 % | 63.41 % | 69.73 % | 77.25 % | 82.83 % | 88.19 % |
| 0.5 ATR | 2.912 % | 37.9321 | 34.84 % | 49.8 % | 58.53 % | 68.76 % | 77.03 % | 83.68 % |
| 0.75 ATR | 4.369 % | 37.3632 | 17.32 % | 33.27 % | 43.09 % | 55.21 % | 66.46 % | 75.46 % |
| 1.0 ATR | 5.825 % | 36.7943 | 7.85 % | 21.37 % | 30.27 % | 43.58 % | 57.01 % | 68.69 % |
| 1.25 ATR | 7.281 % | 36.2254 | 3.73 % | 14.92 % | 22.1 % | 32.96 % | 47.66 % | 60.99 % |
| 1.5 ATR | 8.737 % | 35.6564 | 1.51 % | 9.58 % | 16.15 % | 25.78 % | 41.36 % | 54.62 % |
| 2.0 ATR | 11.649 % | 34.5186 | 0.3 % | 3.53 % | 8.27 % | 15.98 % | 29.57 % | 43.43 % |
| 2.5 ATR | 14.562 % | 33.3807 | 0.2 % | 1.51 % | 4.24 % | 9.5 % | 19.31 % | 31.52 % |
| 3.0 ATR | 17.474 % | 32.2429 | 0.2 % | 1.21 % | 2.62 % | 5.46 % | 13.82 % | 23.72 % |
| 4.0 ATR | 23.299 % | 29.9671 | 0.0 % | 0.6 % | 1.51 % | 2.63 % | 7.42 % | 14.17 % |
| 6.0 ATR | 34.948 % | 25.4157 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.54 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.34 ATR | 0.39 ATR | 0.53 ATR | 0.64 ATR | 0.71 ATR | 0.94 ATR | 1.17 ATR |
| **2 s.** | 0.23 ATR | 0.50 ATR | 0.57 ATR | 0.76 ATR | 0.92 ATR | 1.05 ATR | 1.48 ATR | 1.88 ATR |
| **3 s.** | 0.27 ATR | 0.64 ATR | 0.72 ATR | 0.95 ATR | 1.16 ATR | 1.34 ATR | 1.89 ATR | 2.41 ATR |
| **5 s.** | 0.39 ATR | 0.86 ATR | 0.97 ATR | 1.25 ATR | 1.54 ATR | 1.79 ATR | 2.46 ATR | 3.16 ATR |
| **10 s.** | 0.55 ATR | 1.19 ATR | 1.36 ATR | 1.85 ATR | 2.22 ATR | 2.47 ATR | 3.60 ATR | 4.90 ATR |
| **20 s.** | 0.77 ATR | 1.71 ATR | 1.93 ATR | 2.44 ATR | 2.92 ATR | 3.39 ATR | 4.97 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.394–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.573–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.369 %, prix 37.363), p(touche) 33.27 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.719–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.369 %, prix 37.363), p(touche) 43.09 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 17.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.969–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.281 %, prix 36.2253), p(touche) 32.96 % (en stress 89.9 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.356–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.737 %, prix 35.6565), p(touche) 41.36 % (en stress 95.96 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.93–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (17.474 %, prix 32.2429), p(touche) 23.72 % (en stress 96.94 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.117 | EV/share : $0.266 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 28 % | T2 14 % | T3 11 %
- Kelly (position) : f* 0.074 | ¼-Kelly 0.018 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 15.8 | bear 5.0 | side 79.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 488.0 (= 14 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈60.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.439% → cible +5.108% / stop −2.554%, p_fill 19%, n_eff≈24.5) : P(cible|rempli) **0%** · **EV/risk +0.009** (×p_fill ; si rempli +0.12% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=11, n_eff=11))
  - **deep** : indisponible (échantillon insuffisant (n=13, n_eff=13))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→77% · +2.0%→62% · +3.0%→43% · +5.0%→22% · +8.0%→9%
- Range intraday médian 5.66% (p90 9.37%) · excursion haute méd. +2.56% / basse méd. −2.37%
- Profil de vol intra : ouverture 3.84% vs midi 1.155% vs clôture 1.48% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓0% ; spike-down 69% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; neutre — autocorr -0.011)_ ; drift intra méd. 0.304% ; recovery-V 40%
- **σ réalisé intraday** 3.371% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 61% / bas 61% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 43.4066 (VA 43.1796–43.8039 ; dernier close 43.68)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 23% · rebond 78% · **stop −4.35%** sous le fill (sous le bruit) · cible +2.23% · R/R 0.51 (high win-rate)
- Gaps overnight (n=159) : méd. 0.21% · baisse 42% (gap-down >1% 31% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.93% (p90 −2.5%) · haut méd +1.02% · range méd 2.13%
- Excursion ouverture 15min (n=160) : bas méd −1.13% (p90 −3.1%) · haut méd +1.28% · range méd 2.8%
- Excursion ouverture 30min (n=160) : bas méd −1.36% (p90 −3.6%) · haut méd +1.53% · range méd 3.54%
- Excursion ouverture 60min (n=160) : bas méd −1.66% (p90 −4.07%) · haut méd +1.81% · range méd 4.18%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 43.69 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 71% (116/159) · gap 37% · délai 0.0min · rebond 57% (69/116) (MFE +1.39%)
   - −1.0% : fill 30min 51% · séance 67% (109/159) · gap 31% · délai 0.0min · rebond 58% (64/109) (MFE +1.64%)
   - −1.5% : fill 30min 45% · séance 61% (99/159) · gap 20% · délai 0.2min · rebond 69% (65/99) (MFE +1.56%)
   - −2.0% : fill 30min 39% · séance 53% (86/159) · gap 16% · délai 1.1min · rebond 72% (57/86) (MFE +1.74%)
   - −3.0% : fill 30min 26% · séance 44% (72/159) · gap 8% · délai 12.8min · rebond 64% (44/72) (MFE +1.42%)
   - −4.0% : fill 30min 13% · séance 31% (52/159) · gap 4% · délai 41.3min · rebond 72% (34/52) (MFE +1.7%)
   - −5.0% : fill 30min 10% · séance 23% (41/159) · gap 3% · délai 49.2min · rebond 78% (30/41) (MFE +2.23%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.62% (p90 −2.8%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.66% (p90 −2.62%) → stop au-delà de −1.86% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.65% (p90 −2.32%) → stop au-delà de −1.68% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=870 jambes) : jambe baissière méd −1.18% (p90 −2.77%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (71 séances) :
      · −1.0% : fill 98% (69/71) · rebond 48% (36/69)
      · −2.0% : fill 94% (65/71) · rebond 74% (41/65)
      · −3.0% : fill 85% (58/71) · rebond 65% (35/58)
      · −4.0% : fill 62% (43/71) · rebond 71% (28/43)
      · −5.0% : fill 46% (34/71) · rebond 76% (24/34)
   - **flat** (13 séances) :
      · −1.0% : fill 85% (12/13) · rebond 75% (9/12)
      · −2.0% : fill 36% (5/13) · rebond 50% (3/5)
      · −3.0% : fill 29% (3/13) · rebond 43% (2/3)
      · −4.0% : fill 10% (1/13) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/13) · rebond 0% (0/0)
   - **gap-up** (75 séances) :
      · −1.0% : fill 38% (28/75) · rebond 74% (19/28)
      · −2.0% : fill 21% (16/75) · rebond 70% (13/16)
      · −3.0% : fill 11% (11/75) · rebond 70% (7/11)
      · −4.0% : fill 8% (8/75) · rebond 72% (5/8)
      · −5.0% : fill 8% (7/75) · rebond 86% (6/7)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 68% si les 15 1res min sont vertes (80 cas) · 27% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **39min** → P(séance verte=clôture>ouverture) 78% si début vert vs 18% si rouge (base 48% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 213min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **78%** · continue >prix actuel 54% ; creux résiduel méd -1.96% (q20 -3.57%) → **SL/trailing à −3.57%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.91% / q75 +4.23% → **scale +1.91% / runner +4.23%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **18%** (continue à baisser 53%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.85%** (au-delà de la MAE q10 -4.85%), cible rebond +1.68% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.7% .. +4.13%] · haut q95 +5.15% · bas q05 -4.15%
   - 60min (n=160) : retour [-4.08% .. +5.23%] · haut q95 +6.49% · bas q05 -5.23%
   - 2h (n=160) : retour [-4.2% .. +6.08%] · haut q95 +7.25% · bas q05 -5.52%
   - 4h (n=160) : retour [-4.43% .. +6.66%] · haut q95 +7.77% · bas q05 -5.98%
   - 6h (n=160) : retour [-4.87% .. +6.53%] · haut q95 +8.68% · bas q05 -6.54%
   - session (n=160) : retour [-4.8% .. +6.89%] · haut q95 +8.93% · bas q05 -6.91%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — SMCI = **volatil sans tendance propre (choppy)** (vol intra méd 3.54%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.48 · part idiosyncratique 0.52
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 42.0  _(momentum baissier)_
- **ADX** : 26.2  _(tendance etablie)_
- **MACD** : hist -0.514  _(bearish_recent)_
- **BB** : %B 0.17 · largeur 18.0%
- **ATR** : 2.28 (60.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.113  _(accumulation)_
- **Vol ratio** : 0.69  _(volume normal)_
- **Choppiness** : 55.9  _(transition)_
- **MA** : MA20 41.5 · MA50 38.44 · MA200 32.41  _(prix < MA20)_
- **Dist MA** : MA20 -5.9% · MA50 +1.6% · MA200 +20.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (896141 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
