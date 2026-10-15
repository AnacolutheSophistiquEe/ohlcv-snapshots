# HOOD

**Generated** : 2026-10-15T00:28:33.759930+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $101.10  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 41/121 fenêtres (p_fill pondéré 34 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot $101.10 (+4.6% vs entrée) · entrée $96.64 · stop $91.58 · T1 $102.30 · R/R 1.12  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -0.5 % ≠ (strike 110.0 − spot 101.10)/spot = +8.8 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-14 : 101.1 · ATR Wilder 5.51 (5.45 %)_
- **Swing** : plage **95.06 → 90.42** (-5.97 % a -10.56 % sous la cloture, 0.84 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 94.4-96.59 (B) ; 91.44-93.36 (A) ; 88.6-90.7 (B). stop INDICATIF 84.91 (-6.09 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- **Deep** : plage **90.42 → 80.29** (-10.56 % a -20.58 % sous la cloture, 1.84 ATR) — touchee 41 % → 15 % du temps en 20 seances ; supports reels dans la plage : 88.6-90.7 (B) ; 81.93-83.68 (A). stop INDICATIF 75.04 (-6.54 % sous le bas ; sous le support 77.8-79.57 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (COMBO) : 4.65 ATR sous le plus haut 20 s., RSI(2) 9.1. Limite **98.34** (seance suivante), stop catastrophe 76.3, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 94.4-96.59 (B, -4.46 %) ; 91.44-93.36 (A, -7.66 %) ; 88.6-90.7 (B, -10.29 %) ; 81.93-83.68 (A, -17.23 %) ; 77.8-79.57 (A, -21.3 %) ; 72.79-74.59 (A, -26.22 %)
- Resistances reelles au-dessus : 105.11-106.31 (B, 3.97 %) ; 108.81-111.46 (A, 7.63 %) ; 112.43-114.1 (A, 11.2 %) ; 117.46-120.05 (A, 16.18 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.18 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.42 %)** : le gap seul le franchit 0.559 % des séances (7 fois sur 1253).
   - exécution **1.699 pt plus bas** dans le cas TYPIQUE (médiane), 6.17 au p90, **8.365 au pire**
   - perte réelle **12.322 %** en moyenne _(tirée par la queue)_, jusqu'à **17.785 %** — au lieu des 9.42 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0162 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 7 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.416 % | p01 -7.308 % | pire -17.785 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2855** [0.2222 ; 0.3559] _(largeur 13.4 pt, n_eff 173.1)_
   - swing : **0.5196** [0.467 ; 0.5719] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4614** [0.4094 ; 0.5141] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : swing (30.0 pt), deep (30.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 780 séances)** : VaR **-6.03 %** | CVaR **-8.94 %** | vol 4.28 %/j
   - _fenêtre arrêtée : rupture de regime a 840 seances en arriere (volatilite 2.57 % contre 4.53 % aujourd'hui, rapport 0.57)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.55 % vs -14.5 % si l'on extrapolait par √5 _(rapport 1.003 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7744** (β de hausse 1.612, asymétrie 1.1008) vs IWM — 606 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.391× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 94.7749 sur atr_grid (1.25 ATR, 6.256 %) — p(stop avant cible) 0.5883 [0.54 ; 0.64], R/R 3.06, perte reelle 6.597 % (gap inclus), CVaR 9.936 %, EV 1.0607 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.1624 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.588, borne haute 0.639 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 23 des 23 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 27.9 % de la queue et il ne reste que 13.84 EUR a partager. Prix du risque 0.004 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 7.508 %) — p(stop avant cible) 0.5237 [0.47 ; 0.58], R/R 2.566, perte reelle 7.866 % (gap inclus), EV 1.1002 % — **REFUSE**
      - refuse : p_stop_first 0.524, borne haute 0.576 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 1.91 ATR (stop 12.118 %) — p(stop avant cible) 0.2793 [0.23 ; 0.33], R/R 1.579, perte reelle 12.785 % (gap inclus), EV 2.0382 % — **REFUSE**
      - refuse : R/R 1.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.81 % > budget 12.00 %
   - 🟢 support a 4.38 ATR (stop 24.491 %) — p(stop avant cible) 0.0336 [0.02 ; 0.06], R/R 0.805, perte reelle 25.06 % (gap inclus), EV 2.5194 % — **REFUSE**
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.36 % > budget 12.00 %
   - 🟢 support a 6.3 ATR (stop 34.096 %) — p(stop avant cible) 0.0031 [0.00 ; 0.01], R/R 0.587, perte reelle 34.382 % (gap inclus), EV 2.6368 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.60 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.251 %) — p(stop avant cible) 0.9198 [0.89 ; 0.94], R/R 14.719, perte reelle 1.371 % (gap inclus), EV -0.021 % — **REFUSE**
      - refuse : cible atteinte seulement 4.3 % du temps (< 15 %) meme a 10 seances : le R/R de 14.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.920, borne haute 0.945 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.02 %) : P(cible) 4.3 % x 20.18 % + P(rien) 3.7 % x 10.01 % ne couvrent pas P(stop) 92.0 % x 1.37 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 2.503 %) — p(stop avant cible) 0.8104 [0.77 ; 0.85], R/R 7.581, perte reelle 2.663 % (gap inclus), EV 0.6078 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.810, borne haute 0.849 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 3.754 %) — p(stop avant cible) 0.7226 [0.67 ; 0.77], R/R 5.144, perte reelle 3.924 % (gap inclus), EV 0.9305 % — **REFUSE**
      - refuse : cible atteinte seulement 12.7 % du temps (< 15 %) meme a 10 seances : le R/R de 5.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.723, borne haute 0.768 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 5.005 %) — p(stop avant cible) 0.6585 [0.61 ; 0.71], R/R 3.806, perte reelle 5.304 % (gap inclus), EV 0.803 % — **REFUSE**
      - refuse : cible atteinte seulement 14.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.658, borne haute 0.707 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.25 ATR (stop 6.256 %) — p(stop avant cible) 0.5883 [0.54 ; 0.64], R/R 3.06, perte reelle 6.597 % (gap inclus), EV 1.0607 % — **REFUSE**
      - refuse : p_stop_first 0.588, borne haute 0.639 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - 🟢 grid_snapped a 1.91 ATR (stop 11.056 %) — p(stop avant cible) 0.3245 [0.28 ; 0.38], R/R 1.734, perte reelle 11.642 % (gap inclus), EV 1.91 % — **REFUSE**
      - refuse : R/R 1.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.76 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 13.764 %) — p(stop avant cible) 0.2311 [0.19 ; 0.28], R/R 1.411, perte reelle 14.307 % (gap inclus), EV 2.0158 % — **REFUSE**
      - refuse : R/R 1.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.27 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 15.015 %) — p(stop avant cible) 0.1883 [0.15 ; 0.23], R/R 1.299, perte reelle 15.543 % (gap inclus), EV 2.1418 % — **REFUSE**
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.00 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 17.518 %) — p(stop avant cible) 0.1187 [0.09 ; 0.16], R/R 1.126, perte reelle 17.931 % (gap inclus), EV 2.345 % — **REFUSE**
      - refuse : R/R 1.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.50 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 20.02 %) — p(stop avant cible) 0.0748 [0.05 ; 0.11], R/R 0.991, perte reelle 20.361 % (gap inclus), EV 2.473 % — **REFUSE**
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.53 % > budget 12.00 %
   - 🟢 grid_snapped a 4.38 ATR (stop 23.43 %) — p(stop avant cible) 0.0361 [0.02 ; 0.06], R/R 0.843, perte reelle 23.942 % (gap inclus), EV 2.5307 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.86 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 27.528 %) — p(stop avant cible) 0.0251 [0.01 ; 0.05], R/R 0.723, perte reelle 27.9 % (gap inclus), EV 2.5279 % — **REFUSE**
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.08 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 30.03 %) — p(stop avant cible) 0.0211 [0.01 ; 0.04], R/R 0.667, perte reelle 30.241 % (gap inclus), EV 2.5166 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.63 % > budget 12.00 %
   - 🟢 grid_snapped a 6.3 ATR (stop 33.035 %) — p(stop avant cible) 0.0058 [0.00 ; 0.02], R/R 0.607, perte reelle 33.277 % (gap inclus), EV 2.6012 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.28 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 35.035 %) — p(stop avant cible) 0.0028 [0.00 ; 0.01], R/R 0.57, perte reelle 35.421 % (gap inclus), EV 2.6409 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.58 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 37.538 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.538, perte reelle 37.538 % (gap inclus), EV 2.6475 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.39 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 40.04 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.504, perte reelle 40.04 % (gap inclus), EV 2.6661 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.05 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 101.1, ATR14 5.0601 (5.005 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.372 ATR = 1.862 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.25 % | 100.847 | 93.15 % | 95.26 % | 96.17 % | 96.66 % | 97.15 % | 98.05 % |
| 0.1 ATR | 0.501 % | 100.594 | 85.6 % | 90.73 % | 92.43 % | 93.93 % | 94.82 % | 96.41 % |
| 0.15 ATR | 0.751 % | 100.341 | 77.64 % | 85.38 % | 88.19 % | 90.5 % | 92.68 % | 95.07 % |
| 0.2 ATR | 1.001 % | 100.088 | 71.3 % | 80.14 % | 83.96 % | 87.16 % | 90.45 % | 93.22 % |
| 0.25 ATR | 1.251 % | 99.835 | 64.35 % | 74.4 % | 79.31 % | 83.62 % | 87.8 % | 90.86 % |
| 0.35 ATR | 1.752 % | 99.329 | 52.27 % | 65.42 % | 72.05 % | 77.86 % | 83.64 % | 87.89 % |
| 0.5 ATR | 2.503 % | 98.57 | 37.06 % | 53.43 % | 61.15 % | 68.66 % | 76.63 % | 82.14 % |
| 0.75 ATR | 3.754 % | 97.3049 | 19.54 % | 35.99 % | 45.81 % | 55.81 % | 65.75 % | 72.9 % |
| 1.0 ATR | 5.005 % | 96.0399 | 9.26 % | 23.08 % | 32.9 % | 44.19 % | 55.18 % | 65.3 % |
| 1.25 ATR | 6.256 % | 94.7749 | 4.83 % | 14.62 % | 22.5 % | 33.77 % | 47.46 % | 58.73 % |
| 1.5 ATR | 7.508 % | 93.5099 | 2.52 % | 9.88 % | 16.35 % | 27.1 % | 40.55 % | 52.98 % |
| 2.0 ATR | 10.01 % | 90.9799 | 0.5 % | 3.83 % | 7.27 % | 15.37 % | 29.98 % | 43.12 % |
| 2.5 ATR | 12.513 % | 88.4498 | 0.1 % | 1.51 % | 3.83 % | 8.19 % | 21.65 % | 33.98 % |
| 3.0 ATR | 15.015 % | 85.9198 | 0.0 % | 0.71 % | 2.32 % | 5.26 % | 15.45 % | 26.08 % |
| 4.0 ATR | 20.02 % | 80.8597 | 0.0 % | 0.4 % | 0.91 % | 2.22 % | 6.91 % | 14.89 % |
| 6.0 ATR | 30.03 % | 70.7396 | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.32 % | 4.62 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.37 ATR | 0.42 ATR | 0.56 ATR | 0.67 ATR | 0.74 ATR | 0.98 ATR | 1.24 ATR |
| **2 s.** | 0.24 ATR | 0.55 ATR | 0.62 ATR | 0.81 ATR | 0.96 ATR | 1.09 ATR | 1.49 ATR | 1.90 ATR |
| **3 s.** | 0.31 ATR | 0.68 ATR | 0.77 ATR | 1.00 ATR | 1.19 ATR | 1.35 ATR | 1.85 ATR | 2.33 ATR |
| **5 s.** | 0.40 ATR | 0.88 ATR | 0.98 ATR | 1.28 ATR | 1.59 ATR | 1.80 ATR | 2.37 ATR | 3.09 ATR |
| **10 s.** | 0.54 ATR | 1.17 ATR | 1.34 ATR | 1.86 ATR | 2.30 ATR | 2.63 ATR | 3.64 ATR | 4.68 ATR |
| **20 s.** | 0.69 ATR | 1.65 ATR | 1.91 ATR | 2.56 ATR | 3.10 ATR | 3.54 ATR | 4.95 ATR | 5.93 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.422–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.621–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.754 %, prix 97.3047), p(touche) 35.99 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 21.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.766–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.005 %, prix 96.0399), p(touche) 32.9 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (63.4 % des re-echantillons)
- **5 seance(s)** : plage utile 0.983–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.005 %, prix 96.0399), p(touche) 44.19 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.339–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.508 %, prix 93.5094), p(touche) 40.55 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.905–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (10.01 %, prix 90.9799), p(touche) 43.12 % (en stress 97.96 %)  ✅ optimum identifie (65.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.044 | EV/share : $-0.220 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 19 % | T3 12 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 15.1 | bear 77.6 | side 7.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 91.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.01% → cible +2.68% / stop −3.0%, p_fill 56%, n_eff≈61.0) : P(cible|rempli) **41%** · **EV/risk +0.050** (×p_fill ; si rempli +0.27% du capital)
  - **swing** (entrée dip −4.415% → cible +5.854% / stop −5.236%, p_fill 34%, n_eff≈39.5) : P(cible|rempli) **57%** · **EV/risk +0.077** (×p_fill ; si rempli +1.21% du capital)
  - **deep** (entrée dip −6.823% → cible +7.984% / stop −8.057%, p_fill 35%, n_eff≈37.7) : P(cible|rempli) **56%** · **EV/risk +0.049** (×p_fill ; si rempli +1.13% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→78% · +2.0%→52% · +3.0%→35% · +5.0%→18% · +8.0%→6%
- Range intraday médian 4.88% (p90 8.86%) · excursion haute méd. +2.07% / basse méd. −2.24%
- Profil de vol intra : ouverture 3.683% vs midi 0.98% vs clôture 1.099% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 19% · trend ↑0%/↓2% ; spike-down 66% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.128 ; neutre — autocorr -0.016)_ ; drift intra méd. -0.529% ; recovery-V 19%
- **σ réalisé intraday** 3.385% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 36% / bas 57% / whipsaw 6%
- POC intraday (dernière séance, temps-au-prix) : 112.89 (VA 112.546–114.438 ; dernier close 112.73)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 23% · rebond 66% · **stop −4.04%** sous le fill (sous le bruit) · cible +2.22% · R/R 0.55 (high win-rate)
- Gaps overnight (n=159) : méd. 0.02% · baisse 49% (gap-down >1% 30% · >2% 15%)
- Excursion ouverture 5min (n=160) : bas méd −0.95% (p90 −2.87%) · haut méd +1.04% · range méd 2.21%
- Excursion ouverture 15min (n=160) : bas méd −1.34% (p90 −3.46%) · haut méd +1.29% · range méd 2.92%
- Excursion ouverture 30min (n=160) : bas méd −1.56% (p90 −3.72%) · haut méd +1.57% · range méd 3.42%
- Excursion ouverture 60min (n=160) : bas méd −1.9% (p90 −3.9%) · haut méd +1.67% · range méd 3.85%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 112.74 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 79% (123/159) · gap 38% · délai 0.0min · rebond 62% (72/123) (MFE +1.49%)
   - −1.0% : fill 30min 60% · séance 68% (108/159) · gap 30% · délai 0.0min · rebond 68% (67/108) (MFE +1.66%)
   - −1.5% : fill 30min 47% · séance 61% (98/159) · gap 21% · délai 1.4min · rebond 60% (56/98) (MFE +1.44%)
   - −2.0% : fill 30min 37% · séance 50% (85/159) · gap 15% · délai 2.8min · rebond 70% (56/85) (MFE +1.4%)
   - −3.0% : fill 30min 22% · séance 34% (63/159) · gap 5% · délai 12.5min · rebond 71% (45/63) (MFE +1.74%)
   - −4.0% : fill 30min 12% · séance 23% (45/159) · gap 2% · délai 32.1min · rebond 66% (32/45) (MFE +2.22%)
   - −5.0% : fill 30min 7% · séance 14% (28/159) · gap 1% · délai 30.3min · rebond 63% (20/28) (MFE +2.37%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.61% (p90 −2.55%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.6% (p90 −2.2%) → stop au-delà de −1.83% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.56% (p90 −2.14%) → stop au-delà de −1.69% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=751 jambes) : jambe baissière méd −1.14% (p90 −2.74%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 92% (71/75) · rebond 60% (39/71)
      · −2.0% : fill 75% (60/75) · rebond 68% (38/60)
      · −3.0% : fill 56% (48/75) · rebond 80% (35/48)
      · −4.0% : fill 38% (35/75) · rebond 74% (27/35)
      · −5.0% : fill 25% (24/75) · rebond 67% (17/24)
   - **flat** (17 séances) :
      · −1.0% : fill 66% (11/17) · rebond 70% (7/11)
      · −2.0% : fill 47% (9/17) · rebond 53% (5/9)
      · −3.0% : fill 20% (4/17) · rebond 7% (1/4)
      · −4.0% : fill 20% (4/17) · rebond 7% (1/4)
      · −5.0% : fill 16% (2/17) · rebond 15% (1/2)
   - **gap-up** (67 séances) :
      · −1.0% : fill 46% (26/67) · rebond 82% (21/26)
      · −2.0% : fill 26% (16/67) · rebond 86% (13/16)
      · −3.0% : fill 16% (11/67) · rebond 56% (9/11)
      · −4.0% : fill 9% (6/67) · rebond 63% (4/6)
      · −5.0% : fill 2% (2/67) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 63% si les 15 1res min sont vertes (75 cas) · 26% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **26min** → P(séance verte=clôture>ouverture) 66% si début vert vs 20% si rouge (base 42% · écart 46 pts) ; prédictivité sature ensuite (plafond brut 227min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **66%** · continue >prix actuel 46% ; creux résiduel méd -1.61% (q20 -2.72%) → **SL/trailing à −2.72%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.69% / q75 +2.73% → **scale +1.69% / runner +2.73%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **20%** (continue à baisser 57%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.08%** (au-delà de la MAE q10 -4.08%), cible rebond +1.63% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.16% .. +3.94%] · haut q95 +5.0% · bas q05 -5.03%
   - 60min (n=160) : retour [-4.26% .. +4.93%] · haut q95 +5.37% · bas q05 -5.54%
   - 2h (n=160) : retour [-4.88% .. +5.34%] · haut q95 +7.5% · bas q05 -6.04%
   - 4h (n=160) : retour [-4.77% .. +6.75%] · haut q95 +8.29% · bas q05 -6.73%
   - 6h (n=160) : retour [-6.02% .. +6.48%] · haut q95 +8.48% · bas q05 -7.25%
   - session (n=160) : retour [-5.78% .. +6.96%] · haut q95 +8.59% · bas q05 -7.61%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.1% des séances sont trend-up (mild 0% / strong 8.1%) · base = 13 séances trend-up (n_eff 8.5)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **31%**. Lecture précoce 30 min : signature présente → 19% vs absente 2% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.92% (p75 1.24% / p90 1.92%) · ~4.0 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **77%** (reprise méd 15.35 min, n=49)
   - −1.0% → **62%** (reprise méd 30.0 min, n=21)
   - −1.5% → **48%** (reprise méd 42.24 min, n=10)
   - −2.0% → **15%** (reprise méd None min, n=5)
   - −3.0% → **20%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.92%** (p90, défaut prudent ; serré/agressif −1.24%) ; extension open→close méd +6.2% (q75 +8.64% / q95 +11.94%), MFE méd +7.69% / q90 +13.19%
   - Échelle scale-out : +7.69% (33%) / +9.01% (33%) / +13.19% (34%)
- **DÉSARMER** : repli > **−1.92%** depuis le plus-haut = décay → P(retournement) **85%** (préavis méd 310.68 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.19% : P(retournement après) 0% (mèche méd 3.29%)
- **CONTEXTE** : la dernière heure tient les gains 73% du temps (retour médian dernière heure +0.39%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.6 · part idiosyncratique 0.4
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 19.8  _(survente)_
- **ADX** : 13.0  _(pas de tendance nette)_
- **MACD** : hist -1.619  _(pas de croisement recent)_
- **BB** : %B -0.03 · largeur 21.5%
- **ATR** : 5.06 (34.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.201  _(distribution)_
- **Vol ratio** : 1.05  _(volume normal)_
- **Choppiness** : 42.5  _(transition)_
- **MA** : MA20 114.08 · MA50 108.24 · MA200 93.91  _(prix < MA20)_
- **Dist MA** : MA20 -11.4% · MA50 -6.6% · MA200 +7.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (889158 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
