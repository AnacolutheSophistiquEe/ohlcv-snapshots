# AL2SI

**Generated** : 2026-11-26T21:49:29.594700+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 14.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €17.36  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (24 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot €17.36 (+1.2% vs entrée) · entrée €17.16 · stop €15.79 · T1 €20.19 · R/R 2.21  
> ↳ _probas brutes, non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-26 : 17.36 · ATR Wilder 2.14 (12.32 %)_
- **Swing** : plage **14.93 → 13.36** (-14.02 % a -23.03 % sous la cloture, 0.73 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 14.2-15.1 (A). stop INDICATIF 11.93 (-10.71 % sous le bas ; sous le support 13.0-13.24 (- 0,5 ATR)).
- **Deep** : plage **13.36 → 9.14** (-23.03 % a -47.33 % sous la cloture, 1.97 ATR) — touchee 42 % → 15 % du temps en 20 seances ; supports reels dans la plage : 13.0-13.24 (B) ; 11.76-12.4 (A) ; 10.52-11.36 (A) ; 9.3-10.1 (A). stop INDICATIF 6.78 (-25.84 % sous le bas ; sous le support 7.85-8.83 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (3.2 ATR sous le plus haut 20 s., RSI(2) 82.6 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 16.1-16.65 (B, -4.09 %) ; 14.2-15.1 (A, -13.02 %) ; 13.0-13.24 (B, -23.73 %) ; 11.76-12.4 (A, -28.57 %) ; 10.52-11.36 (A, -34.56 %) ; 9.3-10.1 (A, -41.82 %)
- Resistances reelles au-dessus : 19.75-20.8 (A, 13.77 %) ; 22.6-23.55 (A, 30.18 %) ; 25.0-25.4 (A, 44.01 %) ; 26.38-26.7 (A, 51.96 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.75 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.25 %)** : le gap seul le franchit 0.547 % des séances (7 fois sur 1280).
   - exécution **13.123 pt plus bas** dans le cas TYPIQUE (médiane), 32.007 au p90, **41.217 au pire**
   - perte réelle **28.883 %** en moyenne _(tirée par la queue)_, jusqu'à **53.467 %** — au lieu des 12.25 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.091 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 7 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.519 % | p01 -7.775 % | pire -53.467 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0921** [0.0557 ; 0.1419] _(largeur 8.6 pt, n_eff 173.1)_
   - swing : **0.3297** [0.2817 ; 0.3805] _(largeur 9.9 pt, n_eff 345.8)_
   - deep : **0.2847** [0.2391 ; 0.3339] _(largeur 9.5 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.65 %** | CVaR **-15.03 %** | vol 7.27 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 5.08 % contre 8.78 % aujourd'hui, rapport 0.58)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -15.82 % vs -14.48 % si l'on extrapolait par √5 _(rapport 1.092 ; < 1 = le √5 surestime)_
- **β de baisse : 1.2575** (β de hausse 1.0517, asymétrie 1.1957) vs FCHI — 623 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.904× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 15.665 sur atr_grid (1.0 ATR, 9.764 %) — p(stop avant cible) 0.4823 [0.43 ; 0.53], R/R 3.255, perte reelle 13.034 % (gap inclus), CVaR 32.292 %, EV 0.7179 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 2.1397 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 8.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : CVaR 95 % 32.29 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 6 des 6 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 87.1 % de la queue et il ne reste que -469.04 EUR a partager. Prix du risque -2.415 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.42 ATR (stop 8.191 %) — p(stop avant cible) 0.5666 [0.51 ; 0.62], R/R 3.861, perte reelle 10.989 % (gap inclus), EV 0.3898 % — **REFUSE**
      - refuse : cible atteinte seulement 8.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.567, borne haute 0.618 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 31.74 % > budget 12.00 %
      - ⚠ support DETECTE a 0.42 ATR du spot — compartiment <1, mesure a 48.1 % de casse (IC clusterise [0.449 ; 0.511] sur 1150 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_based a 1.5 ATR (stop 14.646 %) — p(stop avant cible) 0.2994 [0.25 ; 0.35], R/R 2.163, perte reelle 19.612 % (gap inclus), EV 1.1826 % — **REFUSE**
      - refuse : cible atteinte seulement 8.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.60 % > budget 12.00 %
   - ⚪ swing_based a 1.53 ATR (stop 19.072 %) — p(stop avant cible) 0.2198 [0.18 ; 0.27], R/R 1.664, perte reelle 25.496 % (gap inclus), EV 0.9163 % — **REFUSE**
      - refuse : cible atteinte seulement 8.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.41 % > budget 12.00 %
   - 🟢 support a 2.45 ATR (stop 28.064 %) — p(stop avant cible) 0.1178 [0.09 ; 0.15], R/R 1.272, perte reelle 33.363 % (gap inclus), EV 1.2171 % — **REFUSE**
      - refuse : cible atteinte seulement 8.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.43 % > budget 12.00 %
   - 🟢 support a 3.6 ATR (stop 39.239 %) — p(stop avant cible) 0.0821 [0.06 ; 0.11], R/R 0.787, perte reelle 53.918 % (gap inclus), EV 0.1063 % — **REFUSE**
      - refuse : cible atteinte seulement 9.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 60.56 % > budget 12.00 %
   - ⚪ atr_grid a 1.0 ATR (stop 9.764 %) — p(stop avant cible) 0.4823 [0.43 ; 0.53], R/R 3.255, perte reelle 13.034 % (gap inclus), EV 0.7179 % — **REFUSE**
      - refuse : cible atteinte seulement 8.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 32.29 % > budget 12.00 %
   - ⚪ atr_grid a 1.25 ATR (stop 12.205 %) — p(stop avant cible) 0.3588 [0.31 ; 0.41], R/R 2.597, perte reelle 16.335 % (gap inclus), EV 1.3989 % — **REFUSE**
      - refuse : cible atteinte seulement 8.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.39 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 29.291 %) — p(stop avant cible) 0.1172 [0.09 ; 0.15], R/R 1.104, perte reelle 38.44 % (gap inclus), EV 0.631 % — **REFUSE**
      - refuse : cible atteinte seulement 8.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 50.40 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 43.937 %) — p(stop avant cible) 0.0756 [0.05 ; 0.11], R/R 0.764, perte reelle 55.509 % (gap inclus), EV 0.3359 % — **REFUSE**
      - refuse : cible atteinte seulement 9.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 60.56 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 48.819 %) — p(stop avant cible) 0.0726 [0.05 ; 0.10], R/R 0.739, perte reelle 57.4 % (gap inclus), EV 0.2344 % — **REFUSE**
      - refuse : cible atteinte seulement 9.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 61.27 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 53.701 %) — p(stop avant cible) 0.0641 [0.04 ; 0.09], R/R 0.675, perte reelle 62.826 % (gap inclus), EV 0.1726 % — **REFUSE**
      - refuse : cible atteinte seulement 9.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 63.28 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 58.583 %) — p(stop avant cible) 0.0641 [0.04 ; 0.09], R/R 0.675, perte reelle 62.826 % (gap inclus), EV 0.1726 % — **REFUSE**
      - refuse : cible atteinte seulement 9.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 63.28 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 63.465 %) — p(stop avant cible) 0.0376 [0.02 ; 0.06], R/R 0.663, perte reelle 64.001 % (gap inclus), EV 0.7161 % — **REFUSE**
      - refuse : cible atteinte seulement 9.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 59.94 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 68.347 %) — p(stop avant cible) 0.0061 [0.00 ; 0.02], R/R 0.621, perte reelle 68.347 % (gap inclus), EV 1.4616 % — **REFUSE**
      - refuse : cible atteinte seulement 9.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.45 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 73.229 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.579, perte reelle 73.229 % (gap inclus), EV 1.5556 % — **REFUSE**
      - refuse : cible atteinte seulement 9.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.64 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 78.111 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.543, perte reelle 78.111 % (gap inclus), EV 1.5556 % — **REFUSE**
      - refuse : cible atteinte seulement 9.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.64 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 17.36, ATR14 1.695 (9.764 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.397 ATR = 3.876 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.488 % | 17.2753 | 87.55 % | 90.97 % | 93.12 % | 94.69 % | 95.75 % | 97.2 % |
| 0.1 ATR | 0.976 % | 17.1905 | 82.75 % | 87.24 % | 90.28 % | 92.22 % | 94.16 % | 96.3 % |
| 0.15 ATR | 1.465 % | 17.1058 | 78.43 % | 83.61 % | 87.33 % | 89.07 % | 92.28 % | 95.2 % |
| 0.2 ATR | 1.953 % | 17.021 | 72.45 % | 79.29 % | 83.4 % | 85.93 % | 89.91 % | 93.01 % |
| 0.25 ATR | 2.441 % | 16.9363 | 66.27 % | 74.68 % | 79.37 % | 82.78 % | 87.73 % | 91.41 % |
| 0.35 ATR | 3.417 % | 16.7668 | 54.41 % | 65.16 % | 71.02 % | 75.89 % | 82.89 % | 87.91 % |
| 0.5 ATR | 4.882 % | 16.5125 | 40.39 % | 53.48 % | 61.89 % | 69.09 % | 78.44 % | 85.51 % |
| 0.75 ATR | 7.323 % | 16.0888 | 22.45 % | 37.59 % | 47.05 % | 55.81 % | 67.75 % | 77.12 % |
| 1.0 ATR | 9.764 % | 15.665 | 12.55 % | 24.73 % | 33.4 % | 44.09 % | 57.47 % | 68.93 % |
| 1.25 ATR | 12.205 % | 15.2413 | 7.25 % | 17.76 % | 24.56 % | 36.32 % | 50.54 % | 62.64 % |
| 1.5 ATR | 14.646 % | 14.8175 | 3.63 % | 11.48 % | 17.39 % | 28.74 % | 43.32 % | 56.34 % |
| 2.0 ATR | 19.528 % | 13.97 | 0.88 % | 5.3 % | 9.72 % | 16.93 % | 31.65 % | 45.05 % |
| 2.5 ATR | 24.41 % | 13.1225 | 0.1 % | 2.36 % | 4.81 % | 9.94 % | 21.56 % | 35.06 % |
| 3.0 ATR | 29.291 % | 12.275 | 0.1 % | 1.18 % | 2.65 % | 6.89 % | 15.33 % | 27.27 % |
| 4.0 ATR | 39.055 % | 10.58 | 0.0 % | 0.79 % | 1.47 % | 2.95 % | 8.7 % | 18.18 % |
| 6.0 ATR | 58.583 % | 7.19 | 0.0 % | 0.0 % | 0.29 % | 0.79 % | 2.97 % | 9.79 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.40 ATR | 0.45 ATR | 0.60 ATR | 0.71 ATR | 0.81 ATR | 1.12 ATR | 1.41 ATR |
| **2 s.** | 0.25 ATR | 0.56 ATR | 0.63 ATR | 0.84 ATR | 0.99 ATR | 1.17 ATR | 1.62 ATR | 2.05 ATR |
| **3 s.** | 0.30 ATR | 0.70 ATR | 0.79 ATR | 1.01 ATR | 1.24 ATR | 1.41 ATR | 1.98 ATR | 2.48 ATR |
| **5 s.** | 0.37 ATR | 0.87 ATR | 0.98 ATR | 1.36 ATR | 1.66 ATR | 1.87 ATR | 2.50 ATR | 3.48 ATR |
| **10 s.** | 0.58 ATR | 1.27 ATR | 1.44 ATR | 1.94 ATR | 2.33 ATR | 2.62 ATR | 3.80 ATR | 5.29 ATR |
| **20 s.** | 0.81 ATR | 1.78 ATR | 2.00 ATR | 2.63 ATR | 3.25 ATR | 3.80 ATR | 5.95 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.451–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (4.882 %, prix 16.5125), p(touche) 40.39 % (en stress 82.35 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (82.9 % des re-echantillons)
- **2 seance(s)** : plage utile VIDE (borne basse 0.633 ATR au-dessus du haut de la grille, 0.5 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile VIDE (borne basse 0.788 ATR au-dessus du haut de la grille, 0.75 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.981–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (9.764 %, prix 15.665), p(touche) 44.09 % (en stress 95.1 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.442–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (14.646 %, prix 14.8175), p(touche) 43.32 % (en stress 96.08 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile VIDE (borne basse 2.003 ATR au-dessus du haut de la grille, 1.5 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 66.8 | bear 22.5 | side 10.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 156.0 (= 9 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.131% → cible +17.648% / stop −8.0%, p_fill 78%, n_eff≈83.6) : P(cible|rempli) **1%** · **EV/risk -0.084** (×p_fill ; si rempli -0.86% du capital)
  - **swing** (entrée dip −2.486% → cible +19.29% / stop −10.013%, p_fill 66%, n_eff≈76.2) : P(cible|rempli) **13%** · **EV/risk -0.116** (×p_fill ; si rempli -1.75% du capital)
  - **deep** (entrée dip −3.644% → cible +20.72% / stop −15.2%, p_fill 68%, n_eff≈75.6) : P(cible|rempli) **17%** · **EV/risk -0.074** (×p_fill ; si rempli -1.65% du capital)
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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.25 · part idiosyncratique 0.75
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-3 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-3 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 55.2  _(momentum haussier)_
- **ADX** : 19.6  _(pas de tendance nette)_
- **MACD** : hist 0.18  _(bullish_recent)_
- **BB** : %B 0.59 · largeur 46.5%
- **ATR** : 1.7 (31.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.056  _(accumulation)_
- **Vol ratio** : 1.94  _(volume au-dessus de la moyenne)_
- **Choppiness** : 50.8  _(transition)_
- **MA** : MA20 16.65 · MA50 23.19 · MA200 29.9  _(prix > MA20)_
- **Dist MA** : MA20 +4.3% · MA50 -25.1% · MA200 -41.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (683075 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
