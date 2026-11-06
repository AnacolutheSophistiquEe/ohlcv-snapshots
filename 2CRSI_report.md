# AL2SI

**Generated** : 2026-11-06T21:49:53.296148+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 13.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €15.88  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-06 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)  
> ↳ spot €15.88 (+2.7% vs entrée) · entrée €15.46 · stop €14.40 · T1 €17.58 · R/R 2.0  
> ↳ _probas brutes, non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-06 : 15.88 · ATR Wilder 2.79 (17.56 %)_
- **Swing** : plage **12.63 → 10.58** (-20.47 % a -33.36 % sous la cloture, 0.73 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 12.4-13.24 (A) ; 10.76-12.08 (A). stop INDICATIF 7.91 (-25.29 % sous le bas ; sous le support 9.3-10.52 (- 0,5 ATR)).
- **Deep** : plage **10.58 → 5.58** (-33.36 % a -64.84 % sous la cloture, 1.79 ATR) — touchee 41 % → 15 % du temps en 20 seances ; supports reels dans la plage : 9.3-10.52 (A) ; 7.85-8.83 (A) ; 6.35-7.32 (A) ; 4.45-6.09 (A). stop INDICATIF 1.65 (-70.52 % sous le bas ; sous le support 3.04-4.39 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 5.15 ATR sous le plus haut 20 s., RSI(2) 27.5. Limite **14.49** (seance suivante), stop catastrophe 3.33, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 14.2-15.0 (A, -5.54 %) ; 12.4-13.24 (A, -16.62 %) ; 10.76-12.08 (A, -23.93 %) ; 9.3-10.52 (A, -33.75 %) ; 7.85-8.83 (A, -44.4 %) ; 6.35-7.32 (A, -53.9 %)
- Resistances reelles au-dessus : 20.1-21.05 (A, 26.57 %) ; 22.6-23.55 (A, 42.32 %) ; 25.0-26.38 (A, 57.43 %) ; 28.18-29.04 (A, 77.46 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.67 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (17.12 %)** : le gap seul le franchit 0.469 % des séances (6 fois sur 1280).
   - exécution **9.149 pt plus bas** dans le cas TYPIQUE (médiane), 28.672 au p90, **36.347 au pire**
   - perte réelle **31.149 %** en moyenne _(tirée par la queue)_, jusqu'à **53.467 %** — au lieu des 17.12 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0658 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.501 % | p01 -7.775 % | pire -53.467 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.109** [0.0691 ; 0.1618] _(largeur 9.3 pt, n_eff 173.1)_
   - swing : **0.2476** [0.2043 ; 0.2951] _(largeur 9.1 pt, n_eff 345.8)_
   - deep : **0.2182** [0.1771 ; 0.264] _(largeur 8.7 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : swing (28.3 pt), deep (29.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.65 %** | CVaR **-15.03 %** | vol 7.0 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 4.81 % contre 8.41 % aujourd'hui, rapport 0.57)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -15.54 % vs -14.4 % si l'on extrapolait par √5 _(rapport 1.079 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1853** (β de hausse 0.9632, asymétrie 1.2306) vs FCHI — 623 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.003× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 15.1248 sur atr_grid (0.25 ATR, 4.756 %) — p(stop avant cible) 0.7429 [0.69 ; 0.79], R/R 12.161, perte reelle 5.768 % (gap inclus), CVaR 19.421 %, EV 0.8949 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.9742 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 12.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.743, borne haute 0.787 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 19.42 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 7 des 7 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 43.6 % de la queue et il ne reste que -237.28 EUR a partager. Prix du risque -0.196 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.56 ATR (stop 16.248 %) — p(stop avant cible) 0.2455 [0.20 ; 0.29], R/R 3.443, perte reelle 20.376 % (gap inclus), EV 2.6842 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 33.24 % > budget 12.00 %
      - ⚠ support DETECTE a 0.56 ATR du spot — compartiment <1, mesure a 45.0 % de casse (IC clusterise [0.421 ; 0.482] sur 1160 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🔴 support a 0.89 ATR (stop 22.545 %) — p(stop avant cible) 0.1472 [0.11 ; 0.19], R/R 2.454, perte reelle 28.589 % (gap inclus), EV 2.6966 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.87 % > budget 12.00 %
      - ⚠ support DETECTE a 0.89 ATR du spot — compartiment <1, mesure a 45.0 % de casse (IC clusterise [0.421 ; 0.482] sur 1160 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 1.26 ATR (stop 29.598 %) — p(stop avant cible) 0.0977 [0.07 ; 0.13], R/R 1.932, perte reelle 36.308 % (gap inclus), EV 2.5457 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.72 % > budget 12.00 %
   - ⚪ swing_based a 2.15 ATR (stop 46.501 %) — p(stop avant cible) 0.0494 [0.03 ; 0.08], R/R 1.27, perte reelle 55.251 % (gap inclus), EV 2.5911 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 55.11 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 4.756 %) — p(stop avant cible) 0.7429 [0.69 ; 0.79], R/R 12.161, perte reelle 5.768 % (gap inclus), EV 0.8949 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 12.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.743, borne haute 0.787 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 19.42 % > budget 12.00 %
   - ⚪ atr_grid a 1.75 ATR (stop 33.289 %) — p(stop avant cible) 0.0875 [0.06 ; 0.12], R/R 1.562, perte reelle 44.894 % (gap inclus), EV 1.9643 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 53.32 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 52.311 %) — p(stop avant cible) 0.0494 [0.03 ; 0.08], R/R 1.158, perte reelle 60.555 % (gap inclus), EV 2.3291 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 60.35 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 57.066 %) — p(stop avant cible) 0.0462 [0.03 ; 0.07], R/R 1.114, perte reelle 62.973 % (gap inclus), EV 2.2417 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 62.05 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 66.577 %) — p(stop avant cible) 0.0133 [0.00 ; 0.03], R/R 1.054, perte reelle 66.577 % (gap inclus), EV 2.8932 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.57 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 76.089 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.922, perte reelle 76.089 % (gap inclus), EV 3.1433 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.59 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 85.6 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.819, perte reelle 85.6 % (gap inclus), EV 3.1433 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.59 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 95.111 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.738, perte reelle 95.111 % (gap inclus), EV 3.1433 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.59 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 15.88, ATR14 3.0207 (19.022 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.401 ATR = 7.628 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.951 % | 15.729 | 87.35 % | 90.87 % | 93.12 % | 94.59 % | 95.65 % | 97.2 % |
| 0.1 ATR | 1.902 % | 15.5779 | 82.55 % | 87.14 % | 90.28 % | 92.22 % | 94.16 % | 96.3 % |
| 0.15 ATR | 2.853 % | 15.4269 | 78.33 % | 83.51 % | 87.33 % | 89.07 % | 92.28 % | 95.2 % |
| 0.2 ATR | 3.804 % | 15.2759 | 72.65 % | 79.29 % | 83.5 % | 86.02 % | 89.91 % | 93.01 % |
| 0.25 ATR | 4.756 % | 15.1248 | 66.67 % | 74.68 % | 79.37 % | 82.78 % | 87.73 % | 91.41 % |
| 0.35 ATR | 6.658 % | 14.8228 | 54.8 % | 65.55 % | 71.12 % | 76.08 % | 82.99 % | 87.91 % |
| 0.5 ATR | 9.511 % | 14.3696 | 40.69 % | 53.68 % | 61.98 % | 69.19 % | 78.54 % | 85.51 % |
| 0.75 ATR | 14.267 % | 13.6145 | 22.65 % | 37.98 % | 47.64 % | 56.1 % | 67.95 % | 77.12 % |
| 1.0 ATR | 19.022 % | 12.8593 | 12.75 % | 25.12 % | 34.09 % | 44.69 % | 57.86 % | 68.93 % |
| 1.25 ATR | 23.778 % | 12.1041 | 7.45 % | 17.96 % | 25.05 % | 37.01 % | 51.04 % | 62.64 % |
| 1.5 ATR | 28.533 % | 11.3489 | 3.63 % | 11.58 % | 17.78 % | 29.43 % | 43.82 % | 56.34 % |
| 2.0 ATR | 38.044 % | 9.8386 | 0.88 % | 5.4 % | 10.02 % | 17.52 % | 32.25 % | 45.05 % |
| 2.5 ATR | 47.555 % | 8.3282 | 0.1 % | 2.36 % | 4.91 % | 10.33 % | 22.06 % | 35.06 % |
| 3.0 ATR | 57.066 % | 6.8179 | 0.1 % | 1.18 % | 2.65 % | 7.09 % | 15.73 % | 27.17 % |
| 4.0 ATR | 76.089 % | 3.7971 | 0.0 % | 0.79 % | 1.47 % | 3.15 % | 8.9 % | 17.78 % |
| 6.0 ATR | 114.133 % | -2.2443 | 0.0 % | 0.0 % | 0.29 % | 0.79 % | 2.57 % | 8.39 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.40 ATR | 0.45 ATR | 0.61 ATR | 0.72 ATR | 0.82 ATR | 1.13 ATR | 1.41 ATR |
| **2 s.** | 0.25 ATR | 0.56 ATR | 0.64 ATR | 0.85 ATR | 1.00 ATR | 1.18 ATR | 1.63 ATR | 2.07 ATR |
| **3 s.** | 0.30 ATR | 0.71 ATR | 0.80 ATR | 1.03 ATR | 1.25 ATR | 1.42 ATR | 2.00 ATR | 2.49 ATR |
| **5 s.** | 0.37 ATR | 0.88 ATR | 0.99 ATR | 1.38 ATR | 1.69 ATR | 1.90 ATR | 2.55 ATR | 3.53 ATR |
| **10 s.** | 0.58 ATR | 1.29 ATR | 1.46 ATR | 1.97 ATR | 2.36 ATR | 2.66 ATR | 3.84 ATR | 5.23 ATR |
| **20 s.** | 0.81 ATR | 1.78 ATR | 2.00 ATR | 2.63 ATR | 3.23 ATR | 3.76 ATR | 5.66 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.454 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (88.0 % des re-echantillons)
- **2 seance(s)** : plage utile VIDE (borne basse 0.638 ATR au-dessus du haut de la grille, 0.5 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile VIDE (borne basse 0.799 ATR au-dessus du haut de la grille, 0.75 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile VIDE (borne basse 0.993 ATR au-dessus du haut de la grille, 0.75 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 55.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile VIDE (borne basse 1.459 ATR au-dessus du haut de la grille, 1.0 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile VIDE (borne basse 2.003 ATR au-dessus du haut de la grille, 1.0 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 17.2 | bear 30.8 | side 52.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.642% → cible +13.699% / stop −6.849%, p_fill 60%, n_eff≈64.8) : P(cible|rempli) **2%** · **EV/risk -0.033** (×p_fill ; si rempli -0.38% du capital)
  - **swing** (entrée dip −5.818% → cible +35.495% / stop −12.0%, p_fill 36%, n_eff≈43.4) : P(cible|rempli) **4%** · **EV/risk -0.077** (×p_fill ; si rempli -2.54% du capital)
  - **deep** (entrée dip −8.987% → cible +40.22% / stop −18.0%, p_fill 36%, n_eff≈40.7) : P(cible|rempli) **4%** · **EV/risk -0.080** (×p_fill ; si rempli -4.07% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→74% · +2.0%→66% · +3.0%→50% · +5.0%→34% · +8.0%→17%
- Range intraday médian 6.93% (p90 16.1%) · excursion haute méd. +2.93% / basse méd. −3.31%
- Profil de vol intra : ouverture 4.806% vs midi 1.518% vs clôture 1.661% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 9% · trend ↑1%/↓0% ; spike-down 74% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; mean-reverting — autocorr -0.07)_ ; drift intra méd. 0.151% ; recovery-V 25%
- **σ réalisé intraday** 4.419% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 71% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 26.6325 (VA 26.2575–26.7325 ; dernier close 26.53)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 28% · rebond 91% · **stop −3.21%** sous le fill (sous le bruit) · cible +2.26% · R/R 0.7 (high win-rate)
- Gaps overnight (n=158) : méd. -0.0% · baisse 51% (gap-down >1% 16% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.93% (p90 −3.16%) · haut méd +0.82% · range méd 2.21%
- Excursion ouverture 15min (n=160) : bas méd −1.22% (p90 −3.92%) · haut méd +1.23% · range méd 2.91%
- Excursion ouverture 30min (n=160) : bas méd −1.42% (p90 −4.38%) · haut méd +1.57% · range méd 3.4%
- Excursion ouverture 60min (n=160) : bas méd −1.64% (p90 −5.26%) · haut méd +2.01% · range méd 4.04%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 26.62 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 81% (125/158) · gap 30% · délai 0.1min · rebond 61% (81/125) (MFE +1.75%)
   - −1.0% : fill 30min 56% · séance 76% (120/158) · gap 16% · délai 0.4min · rebond 61% (79/120) (MFE +1.71%)
   - −1.5% : fill 30min 50% · séance 72% (107/158) · gap 8% · délai 2.4min · rebond 63% (68/107) (MFE +1.74%)
   - −2.0% : fill 30min 42% · séance 66% (98/158) · gap 6% · délai 7.8min · rebond 59% (60/98) (MFE +1.61%)
   - −3.0% : fill 30min 26% · séance 51% (79/158) · gap 3% · délai 31.2min · rebond 59% (53/79) (MFE +1.59%)
   - −4.0% : fill 30min 16% · séance 39% (65/158) · gap 2% · délai 55.8min · rebond 71% (49/65) (MFE +1.67%)
   - −5.0% : fill 30min 11% · séance 28% (50/158) · gap 2% · délai 48.7min · rebond 91% (46/50) (MFE +2.26%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −2.9%) → stop au-delà de −1.95% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −2.91%) → stop au-delà de −2.06% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.34% (p90 −3.18%) → stop au-delà de −2.05% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1398 jambes) : jambe baissière méd −1.21% (p90 −2.94%) · ~16.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (53 séances) :
      · −1.0% : fill 95% (51/53) · rebond 58% (30/51)
      · −2.0% : fill 87% (46/53) · rebond 59% (26/46)
      · −3.0% : fill 76% (41/53) · rebond 59% (28/41)
      · −4.0% : fill 58% (34/53) · rebond 61% (23/34)
      · −5.0% : fill 44% (27/53) · rebond 92% (24/27)
   - **flat** (34 séances) :
      · −1.0% : fill 72% (25/34) · rebond 66% (17/25)
      · −2.0% : fill 54% (19/34) · rebond 49% (11/19)
      · −3.0% : fill 40% (15/34) · rebond 60% (9/15)
      · −4.0% : fill 37% (14/34) · rebond 77% (11/14)
      · −5.0% : fill 30% (11/34) · rebond 80% (10/11)
   - **gap-up** (71 séances) :
      · −1.0% : fill 61% (44/71) · rebond 63% (32/44)
      · −2.0% : fill 52% (33/71) · rebond 65% (23/33)
      · −3.0% : fill 34% (23/71) · rebond 59% (16/23)
      · −4.0% : fill 23% (17/71) · rebond 88% (15/17)
      · −5.0% : fill 13% (12/71) · rebond 100% (12/12)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 56% si les 15 1res min sont vertes (77 cas) · 29% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:03** → P(séance verte=clôture>ouverture) 76% si début vert vs 15% si rouge (base 42% · écart 61 pts) ; prédictivité sature ensuite (plafond brut 252min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **76%** · continue >prix actuel 47% ; creux résiduel méd -2.0% (q20 -4.42%) → **SL/trailing à −4.42%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.14% / q75 +3.25% → **scale +2.14% / runner +3.25%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **15%** (continue à baisser 54%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.15%** (au-delà de la MAE q10 -4.15%), cible rebond +1.5% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.12% .. +5.57%] · haut q95 +6.82% · bas q05 -5.16%
   - 60min (n=160) : retour [-4.85% .. +7.25%] · haut q95 +8.2% · bas q05 -6.05%
   - 2h (n=160) : retour [-4.79% .. +9.19%] · haut q95 +9.95% · bas q05 -6.15%
   - 4h (n=160) : retour [-5.98% .. +9.6%] · haut q95 +9.98% · bas q05 -7.39%
   - 6h (n=160) : retour [-5.66% .. +10.41%] · haut q95 +12.17% · bas q05 -8.1%
   - session (n=160) : retour [-7.13% .. +9.93%] · haut q95 +12.72% · bas q05 -8.49%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 4.85%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.16 · part idiosyncratique 0.84
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-06 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-10 — US CPI (headline) (J-3 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-10 — US CPI (headline) (J-3 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 29.6  _(survente)_
- **ADX** : 20.1  _(pas de tendance nette)_
- **MACD** : hist -1.173  _(pas de croisement recent)_
- **BB** : %B 0.09 · largeur 84.8%
- **ATR** : 3.02 (72.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF 0.189  _(accumulation)_
- **Vol ratio** : 0.93  _(volume normal)_
- **Choppiness** : 30.2  _(marche directionnel)_
- **MA** : MA20 24.3 · MA50 26.44 · MA200 29.83  _(prix < MA20)_
- **Dist MA** : MA20 -34.6% · MA50 -39.9% · MA200 -46.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (685996 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
