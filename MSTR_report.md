# MSTR

**Generated** : 2026-10-13T22:00:52.069943+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $152.18  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot $152.18 (+6.1% vs entrée) · entrée $143.42 · stop $131.44 · T1 $167.38 · R/R 2.0  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-13 : 152.18 · ATR Wilder 8.45 (5.56 %)_
- **Swing** : plage **142.32 → 134.88** (-6.48 % a -11.37 % sous la cloture, 0.88 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 139.45-143.0 (B) ; 132.55-136.25 (B). stop INDICATIF 123.57 (-8.38 % sous le bas ; sous le support 127.8-128.51 (- 0,5 ATR)).
- **Deep** : plage **134.88 → 115.48** (-11.37 % a -24.12 % sous la cloture, 2.29 ATR) — touchee 45 % → 15 % du temps en 20 seances ; supports reels dans la plage : 132.55-136.25 (B) ; 127.8-128.51 (C) ; 123.01-126.59 (A) ; 117.85-121.38 (A) ; 113.2-116.4 (B). stop INDICATIF 100.37 (-13.08 % sous le bas ; sous le support 104.6-105.5 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (2.25 ATR sous le plus haut 20 s., RSI(2) 26.5 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 143.85-147.37 (A, -3.16 %) ; 139.45-143.0 (B, -6.03 %) ; 132.55-136.25 (B, -10.47 %) ; 127.8-128.51 (C, -15.55 %) ; 123.01-126.59 (A, -16.82 %) ; 117.85-121.38 (A, -20.24 %)
- Resistances reelles au-dessus : 162.93-166.01 (A, 7.06 %) ; 168.96-171.5 (A, 11.03 %) ; 173.47-176.3 (A, 13.99 %) ; 178.0-181.5 (A, 16.97 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=10.54 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (13.63 %)** : le gap seul le franchit 0.239 % des séances (3 fois sur 1253).
   - exécution **12.948 pt plus bas** dans le cas TYPIQUE (médiane), 13.583 au p90, **13.742 au pire**
   - perte réelle **22.94 %** en moyenne _(tirée par la queue)_, jusqu'à **27.372 %** — au lieu des 13.63 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0223 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.349 % | p01 -7.775 % | pire -27.372 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2748** [0.2124 ; 0.3446] _(largeur 13.2 pt, n_eff 173.1)_
   - swing : **0.3439** [0.2953 ; 0.3951] _(largeur 10.0 pt, n_eff 345.7)_
   - deep : **0.441** [0.3893 ; 0.4936] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (27.5 pt), swing (33.7 pt), deep (35.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-7.63 %** | CVaR **-10.0 %** | vol 5.37 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 8.82 % contre 5.16 % aujourd'hui, rapport 1.71)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.99 % vs -17.67 % si l'on extrapolait par √5 _(rapport 0.962 ; < 1 = le √5 surestime)_
- **β de baisse : 2.3502** (β de hausse 1.8263, asymétrie 1.2869) vs IWM — 606 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 139.9577 sur atr_grid (1.5 ATR, 8.031 %) — p(stop avant cible) 0.5019 [0.45 ; 0.55], R/R 3.011, perte reelle 8.204 % (gap inclus), CVaR 9.666 %, EV 0.9644 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.128 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 13.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.502, borne haute 0.554 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 23 des 23 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 38.9 % de la queue et il ne reste que -829.92 EUR a partager. Prix du risque -0.253 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.79 ATR (stop 6.914 %) — p(stop avant cible) 0.5564 [0.50 ; 0.61], R/R 3.465, perte reelle 7.128 % (gap inclus), EV 0.9144 % — **REFUSE**
      - refuse : cible atteinte seulement 13.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.556, borne haute 0.608 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - 🟢 support a 1.96 ATR (stop 13.15 %) — p(stop avant cible) 0.2986 [0.25 ; 0.35], R/R 1.853, perte reelle 13.332 % (gap inclus), EV 0.9476 % — **REFUSE**
      - refuse : cible atteinte seulement 13.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.23 % > budget 12.00 %
   - 🟢 support a 4.39 ATR (stop 26.194 %) — p(stop avant cible) 0.0698 [0.05 ; 0.10], R/R 0.93, perte reelle 26.561 % (gap inclus), EV 0.4847 % — **REFUSE**
      - refuse : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.71 % > budget 12.00 %
   - 🟢 support a 5.89 ATR (stop 34.231 %) — p(stop avant cible) 0.019 [0.01 ; 0.04], R/R 0.713, perte reelle 34.646 % (gap inclus), EV 0.5396 % — **REFUSE**
      - refuse : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.76 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.339 %) — p(stop avant cible) 0.9391 [0.91 ; 0.96], R/R 18.134, perte reelle 1.362 % (gap inclus), EV -0.3257 % — **REFUSE**
      - refuse : cible atteinte seulement 2.6 % du temps (< 15 %) meme a 10 seances : le R/R de 18.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.939, borne haute 0.961 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 2.6 % x 24.70 % + P(rien) 3.5 % x 8.94 % ne couvrent pas P(stop) 93.9 % x 1.36 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 2.677 %) — p(stop avant cible) 0.8616 [0.82 ; 0.89], R/R 8.94, perte reelle 2.763 % (gap inclus), EV -0.5434 % — **REFUSE**
      - refuse : cible atteinte seulement 4.9 % du temps (< 15 %) meme a 10 seances : le R/R de 8.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.862, borne haute 0.895 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.54 %) : P(cible) 4.9 % x 24.70 % + P(rien) 8.9 % x 6.96 % ne couvrent pas P(stop) 86.2 % x 2.76 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 0.79 ATR (stop 5.838 %) — p(stop avant cible) 0.6243 [0.57 ; 0.67], R/R 4.116, perte reelle 6.001 % (gap inclus), EV 0.7843 % — **REFUSE**
      - refuse : cible atteinte seulement 11.3 % du temps (< 15 %) meme a 10 seances : le R/R de 4.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.624, borne haute 0.674 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.5 ATR (stop 8.031 %) — p(stop avant cible) 0.5019 [0.45 ; 0.55], R/R 3.011, perte reelle 8.204 % (gap inclus), EV 0.9644 % — **REFUSE**
      - refuse : cible atteinte seulement 13.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.502, borne haute 0.554 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - 🟢 grid_snapped a 1.96 ATR (stop 12.074 %) — p(stop avant cible) 0.3284 [0.28 ; 0.38], R/R 2.029, perte reelle 12.174 % (gap inclus), EV 1.0498 % — **REFUSE**
      - refuse : cible atteinte seulement 13.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.73 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 14.724 %) — p(stop avant cible) 0.2506 [0.21 ; 0.30], R/R 1.657, perte reelle 14.91 % (gap inclus), EV 0.8553 % — **REFUSE**
      - refuse : cible atteinte seulement 13.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.66 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 16.063 %) — p(stop avant cible) 0.2126 [0.17 ; 0.26], R/R 1.514, perte reelle 16.316 % (gap inclus), EV 0.7385 % — **REFUSE**
      - refuse : cible atteinte seulement 13.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.14 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 18.74 %) — p(stop avant cible) 0.1675 [0.13 ; 0.21], R/R 1.3, perte reelle 19.004 % (gap inclus), EV 0.5361 % — **REFUSE**
      - refuse : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.62 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 21.417 %) — p(stop avant cible) 0.1257 [0.09 ; 0.16], R/R 1.135, perte reelle 21.753 % (gap inclus), EV 0.5196 % — **REFUSE**
      - refuse : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.26 % > budget 12.00 %
   - 🟢 grid_snapped a 4.39 ATR (stop 25.118 %) — p(stop avant cible) 0.0847 [0.06 ; 0.12], R/R 0.97, perte reelle 25.464 % (gap inclus), EV 0.4014 % — **REFUSE**
      - refuse : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.70 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 29.449 %) — p(stop avant cible) 0.0463 [0.03 ; 0.07], R/R 0.826, perte reelle 29.908 % (gap inclus), EV 0.4279 % — **REFUSE**
      - refuse : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.68 % > budget 12.00 %
   - 🟢 grid_snapped a 5.89 ATR (stop 33.154 %) — p(stop avant cible) 0.0267 [0.01 ; 0.05], R/R 0.737, perte reelle 33.535 % (gap inclus), EV 0.4877 % — **REFUSE**
      - refuse : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.53 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 37.48 %) — p(stop avant cible) 0.0056 [0.00 ; 0.02], R/R 0.65, perte reelle 38.008 % (gap inclus), EV 0.6601 % — **REFUSE**
      - refuse : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.31 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 40.157 %) — p(stop avant cible) 0.0009 [0.00 ; 0.01], R/R 0.604, perte reelle 40.876 % (gap inclus), EV 0.7017 % — **REFUSE**
      - refuse : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.55 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 42.835 %) — p(stop avant cible) 0.0004 [0.00 ; 0.01], R/R 0.575, perte reelle 42.956 % (gap inclus), EV 0.7081 % — **REFUSE**
      - refuse : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.40 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 152.18, ATR14 8.1482 (5.354 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.394 ATR = 2.11 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.268 % | 151.7726 | 94.06 % | 96.57 % | 97.07 % | 97.78 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.535 % | 151.3652 | 88.32 % | 92.14 % | 93.64 % | 94.94 % | 96.65 % | 97.23 % |
| 0.15 ATR | 0.803 % | 150.9578 | 81.47 % | 87.3 % | 90.01 % | 92.01 % | 94.31 % | 95.48 % |
| 0.2 ATR | 1.071 % | 150.5503 | 73.92 % | 81.96 % | 85.27 % | 88.57 % | 91.77 % | 93.53 % |
| 0.25 ATR | 1.339 % | 150.1429 | 68.08 % | 78.12 % | 82.44 % | 86.45 % | 89.33 % | 91.89 % |
| 0.35 ATR | 1.874 % | 149.3281 | 54.98 % | 68.95 % | 75.48 % | 81.19 % | 85.87 % | 89.22 % |
| 0.5 ATR | 2.677 % | 148.1059 | 38.17 % | 55.34 % | 63.67 % | 71.69 % | 78.66 % | 84.29 % |
| 0.75 ATR | 4.016 % | 146.0688 | 19.44 % | 37.9 % | 47.43 % | 58.44 % | 68.29 % | 76.49 % |
| 1.0 ATR | 5.354 % | 144.0318 | 9.47 % | 25.4 % | 35.12 % | 46.61 % | 59.04 % | 69.1 % |
| 1.25 ATR | 6.693 % | 141.9947 | 4.13 % | 14.62 % | 24.92 % | 36.0 % | 50.0 % | 61.7 % |
| 1.5 ATR | 8.031 % | 139.9577 | 2.11 % | 8.67 % | 17.36 % | 29.12 % | 43.09 % | 55.95 % |
| 2.0 ATR | 10.709 % | 135.8836 | 0.2 % | 3.12 % | 7.37 % | 15.98 % | 30.89 % | 46.0 % |
| 2.5 ATR | 13.386 % | 131.8095 | 0.1 % | 0.91 % | 2.42 % | 8.7 % | 21.24 % | 36.55 % |
| 3.0 ATR | 16.063 % | 127.7353 | 0.1 % | 0.5 % | 1.01 % | 4.55 % | 14.53 % | 27.21 % |
| 4.0 ATR | 21.417 % | 119.5871 | 0.0 % | 0.0 % | 0.3 % | 0.81 % | 6.2 % | 17.56 % |
| 6.0 ATR | 32.126 % | 103.2907 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.61 % | 4.41 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.39 ATR | 0.44 ATR | 0.57 ATR | 0.68 ATR | 0.74 ATR | 0.99 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.58 ATR | 0.65 ATR | 0.85 ATR | 1.01 ATR | 1.12 ATR | 1.44 ATR | 1.83 ATR |
| **3 s.** | 0.36 ATR | 0.71 ATR | 0.80 ATR | 1.05 ATR | 1.25 ATR | 1.41 ATR | 1.87 ATR | 2.24 ATR |
| **5 s.** | 0.45 ATR | 0.93 ATR | 1.04 ATR | 1.36 ATR | 1.66 ATR | 1.85 ATR | 2.41 ATR | 2.95 ATR |
| **10 s.** | 0.59 ATR | 1.25 ATR | 1.43 ATR | 1.91 ATR | 2.31 ATR | 2.59 ATR | 3.54 ATR | 4.43 ATR |
| **20 s.** | 0.80 ATR | 1.80 ATR | 2.05 ATR | 2.69 ATR | 3.23 ATR | 3.75 ATR | 5.15 ATR | 5.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.439–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.677 %, prix 148.1061), p(touche) 38.17 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.648–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.016 %, prix 146.0684), p(touche) 37.9 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.799–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.354 %, prix 144.0323), p(touche) 35.12 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.038–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (6.693 %, prix 141.9946), p(touche) 36.0 % (en stress 95.96 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.431–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.031 %, prix 139.9584), p(touche) 43.09 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 53.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.053–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (13.386 %, prix 131.8092), p(touche) 36.55 % (en stress 98.98 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 53.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.009 | EV/share : $-0.110 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 13 % | T2 7 % | T3 5 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 30.1 | bear 5.2 | side 64.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 272.0 (= 2 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.622% → cible +2.749% / stop −3.5%, p_fill 43%, n_eff≈46.6) : P(cible|rempli) **28%** · **EV/risk -0.030** (×p_fill ; si rempli -0.24% du capital)
  - **swing** (entrée dip −5.759% → cible +16.705% / stop −8.352%, p_fill 25%, n_eff≈31.3) : P(cible|rempli) **10%** · **EV/risk +0.014** (×p_fill ; si rempli +0.45% du capital)
  - **deep** (entrée dip −8.899% → cible +9.242% / stop −8.816%, p_fill 23%, n_eff≈28.5) : P(cible|rempli) **43%** · **EV/risk -0.026** (×p_fill ; si rempli -1.00% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→78% · +2.0%→58% · +3.0%→41% · +5.0%→18% · +8.0%→9%
- Range intraday médian 5.36% (p90 9.67%) · excursion haute méd. +2.57% / basse méd. −2.28%
- Profil de vol intra : ouverture 3.353% vs midi 1.137% vs clôture 1.289% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 14% · trend ↑3%/↓0% ; spike-down 68% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.141 ; neutre — autocorr -0.029)_ ; drift intra méd. 0.341% ; recovery-V 26%
- **σ réalisé intraday** 3.531% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 56% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 157.5016 (VA 156.1046–160.2956 ; dernier close 160.03)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 22% · rebond 79% · **stop −3.87%** sous le fill (sous le bruit) · cible +2.49% · R/R 0.64 (high win-rate)
- Gaps overnight (n=159) : méd. 0.06% · baisse 49% (gap-down >1% 35% · >2% 24%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −2.12%) · haut méd +0.84% · range méd 1.88%
- Excursion ouverture 15min (n=160) : bas méd −1.08% (p90 −2.9%) · haut méd +1.24% · range méd 2.6%
- Excursion ouverture 30min (n=160) : bas méd −1.19% (p90 −3.22%) · haut méd +1.51% · range méd 3.04%
- Excursion ouverture 60min (n=160) : bas méd −1.52% (p90 −3.66%) · haut méd +1.86% · range méd 3.82%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 160.01 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 72% (118/159) · gap 42% · délai 0.0min · rebond 43% (54/118) (MFE +0.52%)
   - −1.0% : fill 30min 53% · séance 67% (112/159) · gap 35% · délai 0.0min · rebond 45% (58/112) (MFE +0.78%)
   - −1.5% : fill 30min 45% · séance 64% (105/159) · gap 28% · délai 0.0min · rebond 54% (59/105) (MFE +1.16%)
   - −2.0% : fill 30min 38% · séance 57% (94/159) · gap 24% · délai 0.1min · rebond 61% (57/94) (MFE +1.35%)
   - −3.0% : fill 30min 26% · séance 42% (74/159) · gap 14% · délai 1.2min · rebond 59% (42/74) (MFE +1.56%)
   - −4.0% : fill 30min 19% · séance 32% (59/159) · gap 4% · délai 11.3min · rebond 76% (41/59) (MFE +1.92%)
   - −5.0% : fill 30min 13% · séance 22% (42/159) · gap 3% · délai 17.2min · rebond 79% (32/42) (MFE +2.49%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.61% (p90 −2.16%) → stop au-delà de −1.63% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.87% (p90 −2.2%) → stop au-delà de −1.71% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.87% (p90 −2.26%) → stop au-delà de −1.81% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=927 jambes) : jambe baissière méd −1.1% (p90 −2.68%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (76 séances) :
      · −1.0% : fill 96% (75/76) · rebond 41% (33/75)
      · −2.0% : fill 91% (69/76) · rebond 60% (40/69)
      · −3.0% : fill 74% (60/76) · rebond 56% (34/60)
      · −4.0% : fill 63% (51/76) · rebond 76% (36/51)
      · −5.0% : fill 46% (38/76) · rebond 81% (30/38)
   - **flat** (18 séances) :
      · −1.0% : fill 69% (13/18) · rebond 68% (10/13)
      · −2.0% : fill 52% (9/18) · rebond 54% (5/9)
      · −3.0% : fill 43% (7/18) · rebond 71% (4/7)
      · −4.0% : fill 20% (4/18) · rebond 80% (3/4)
      · −5.0% : fill 6% (2/18) · rebond 0% (0/2)
   - **gap-up** (65 séances) :
      · −1.0% : fill 37% (24/65) · rebond 41% (15/24)
      · −2.0% : fill 24% (16/65) · rebond 70% (12/16)
      · −3.0% : fill 9% (7/65) · rebond 67% (4/7)
      · −4.0% : fill 4% (4/65) · rebond 58% (2/4)
      · −5.0% : fill 2% (2/65) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 57% si les 15 1res min sont vertes (86 cas) · 31% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:14** → P(séance verte=clôture>ouverture) 74% si début vert vs 8% si rouge (base 46% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=90) : tient le vert **74%** · continue >prix actuel 52% ; creux résiduel méd -1.25% (q20 -2.9%) → **SL/trailing à −2.9%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.05% / q75 +2.9% → **scale +2.05% / runner +2.9%**, sortie à la clôture
  - **si ROUGE au coude** (n=70) : edge inversé — récupère vert seulement **8%** (continue à baisser 56%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.61%** (au-delà de la MAE q10 -4.61%), cible rebond +1.43% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.19% .. +3.97%] · haut q95 +4.43% · bas q05 -3.67%
   - 60min (n=160) : retour [-3.97% .. +5.6%] · haut q95 +5.88% · bas q05 -4.75%
   - 2h (n=160) : retour [-4.57% .. +8.48%] · haut q95 +8.77% · bas q05 -5.63%
   - 4h (n=160) : retour [-5.17% .. +9.39%] · haut q95 +10.33% · bas q05 -6.01%
   - 6h (n=160) : retour [-5.25% .. +8.5%] · haut q95 +11.08% · bas q05 -6.13%
   - session (n=160) : retour [-4.99% .. +8.27%] · haut q95 +11.08% · bas q05 -6.31%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0.6% / strong 5.6%) · base = 10 séances trend-up (n_eff 7.3)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **39%**. Lecture précoce 30 min : signature présente → 22% vs absente 1% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.77% (p75 1.13% / p90 2.71%) · ~4.0 replis/séance, durée méd 34.08 min. P(nouveau plus-haut après repli) :
   - −0.5% → **86%** (reprise méd 20.0 min, n=37)
   - −1.0% → **60%** (reprise méd 31.69 min, n=14)
   - −1.5% → **43%** (reprise méd 42.45 min, n=10)
   - −2.0% → **19%** (reprise méd None min, n=7)
   - −3.0% → **38%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.71%** (p90, défaut prudent ; serré/agressif −1.13%) ; extension open→close méd +9.11% (q75 +12.7% / q95 +13.17%), MFE méd +11.91% / q90 +13.21%
   - Échelle scale-out : +11.91% (33%) / +13.03% (33%) / +13.21% (34%)
- **DÉSARMER** : repli > **−2.71%** depuis le plus-haut = décay → P(retournement) **75%** (préavis méd 182.05 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.21% : P(retournement après) 0% (mèche méd 0.05%)
- **CONTEXTE** : la dernière heure tient les gains 84% du temps (retour médian dernière heure +0.85%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.83 · part idiosyncratique 0.17
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 37.4  _(momentum baissier)_
- **ADX** : 32.2  _(tendance etablie)_
- **MACD** : hist -2.333  _(pas de croisement recent)_
- **BB** : %B 0.42 · largeur 26.8%
- **ATR** : 8.15 (22.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.029  _(neutre)_
- **Vol ratio** : 0.56  _(volume atone)_
- **Choppiness** : 61.0  _(transition)_
- **MA** : MA20 155.45 · MA50 132.15 · MA200 135.8  _(prix < MA20)_
- **Dist MA** : MA20 -2.1% · MA50 +15.2% · MA200 +12.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (902079 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
