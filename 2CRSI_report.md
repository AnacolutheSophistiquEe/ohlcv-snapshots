# AL2SI

**Generated** : 2026-11-11T01:11:32.768114+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 13.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €16.90  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-0 sess · macro taux)  
> ↳ spot €16.90 (+0.8% vs entrée) · entrée €16.76 · stop €15.86 · T1 €18.27 · R/R 1.68  
> ↳ _probas brutes, non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-10 : 16.9 · ATR Wilder 2.64 (15.62 %)_
- **Swing** : plage **13.81 → 11.8** (-18.27 % a -30.2 % sous la cloture, 0.76 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 12.4-13.24 (B) ; 10.76-12.08 (A). stop INDICATIF 7.98 (-32.35 % sous le bas ; sous le support 9.3-10.52 (- 0,5 ATR)).
- **Deep** : plage **11.8 → 7.08** (-30.2 % a -58.13 % sous la cloture, 1.79 ATR) — touchee 41 % → 15 % du temps en 20 seances ; supports reels dans la plage : 10.76-12.08 (A) ; 9.3-10.52 (A) ; 7.85-8.83 (A) ; 6.35-7.32 (A). stop INDICATIF 3.06 (-56.69 % sous le bas ; sous le support 4.39-6.09 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (4.6 ATR sous le plus haut 20 s., RSI(2) 52.4 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 14.2-15.0 (A, -11.24 %) ; 12.4-13.24 (B, -21.66 %) ; 10.76-12.08 (A, -28.52 %) ; 9.3-10.52 (A, -37.75 %) ; 7.85-8.83 (A, -47.75 %) ; 6.35-7.32 (A, -56.69 %)
- Resistances reelles au-dessus : 20.1-21.05 (A, 18.93 %) ; 22.6-23.55 (A, 33.73 %) ; 25.0-25.4 (A, 47.93 %) ; 26.38-26.7 (A, 56.09 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.67 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (13.58 %)** : le gap seul le franchit 0.547 % des séances (7 fois sur 1280).
   - exécution **11.793 pt plus bas** dans le cas TYPIQUE (médiane), 30.677 au p90, **39.887 au pire**
   - perte réelle **28.883 %** en moyenne _(tirée par la queue)_, jusqu'à **53.467 %** — au lieu des 13.58 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0837 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 7 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.501 % | p01 -7.775 % | pire -53.467 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2023** [0.1477 ; 0.2668] _(largeur 11.9 pt, n_eff 173.1)_
   - swing : **0.2447** [0.2016 ; 0.292] _(largeur 9.0 pt, n_eff 345.8)_
   - deep : **0.2272** [0.1854 ; 0.2735] _(largeur 8.8 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-7.45 %** | CVaR **-14.08 %** | vol 6.78 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 4.85 % contre 8.43 % aujourd'hui, rapport 0.57)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -15.54 % vs -14.4 % si l'on extrapolait par √5 _(rapport 1.079 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1882** (β de hausse 0.9698, asymétrie 1.2252) vs FCHI — 622 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.998× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 15.3893 sur atr_grid (0.5 ATR, 8.939 %) — p(stop avant cible) 0.5218 [0.47 ; 0.57], R/R 5.324, perte reelle 11.248 % (gap inclus), CVaR 28.744 %, EV 1.421 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 2.2545 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 5.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.522, borne haute 0.574 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 28.74 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 7 des 7 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 40.1 % de la queue et il ne reste que -144.51 EUR a partager. Prix du risque -0.112 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.08 ATR (stop 6.575 %) — p(stop avant cible) 0.6351 [0.58 ; 0.68], R/R 7.138, perte reelle 8.39 % (gap inclus), EV 1.1079 % — **REFUSE**
      - refuse : cible atteinte seulement 2.7 % du temps (< 15 %) meme a 10 seances : le R/R de 7.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.635, borne haute 0.684 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 27.46 % > budget 12.00 %
      - ⚠ support DETECTE a 0.08 ATR du spot — compartiment <1, mesure a 48.2 % de casse (IC clusterise [0.451 ; 0.515] sur 1149 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 1.22 ATR (stop 26.989 %) — p(stop avant cible) 0.1158 [0.09 ; 0.15], R/R 1.867, perte reelle 32.083 % (gap inclus), EV 2.3875 % — **REFUSE**
      - refuse : cible atteinte seulement 3.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.77 % > budget 12.00 %
   - 🟢 support a 2.28 ATR (stop 45.924 %) — p(stop avant cible) 0.0603 [0.04 ; 0.09], R/R 1.078, perte reelle 55.567 % (gap inclus), EV 1.8489 % — **REFUSE**
      - refuse : cible atteinte seulement 3.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 57.56 % > budget 12.00 %
   - ⚪ atr_grid a 0.5 ATR (stop 8.939 %) — p(stop avant cible) 0.5218 [0.47 ; 0.57], R/R 5.324, perte reelle 11.248 % (gap inclus), EV 1.421 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 5.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.522, borne haute 0.574 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 28.74 % > budget 12.00 %
   - ⚪ atr_grid a 0.75 ATR (stop 13.409 %) — p(stop avant cible) 0.3167 [0.27 ; 0.37], R/R 3.418, perte reelle 17.519 % (gap inclus), EV 2.291 % — **REFUSE**
      - refuse : cible atteinte seulement 3.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 33.16 % > budget 12.00 %
   - ⚪ atr_grid a 1.75 ATR (stop 31.287 %) — p(stop avant cible) 0.106 [0.08 ; 0.14], R/R 1.382, perte reelle 43.336 % (gap inclus), EV 1.3366 % — **REFUSE**
      - refuse : cible atteinte seulement 3.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 55.26 % > budget 12.00 %
   - ⚪ atr_grid a 2.0 ATR (stop 35.757 %) — p(stop avant cible) 0.083 [0.06 ; 0.12], R/R 1.201, perte reelle 49.874 % (gap inclus), EV 1.5334 % — **REFUSE**
      - refuse : cible atteinte seulement 3.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 57.48 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 49.165 %) — p(stop avant cible) 0.0603 [0.04 ; 0.09], R/R 1.047, perte reelle 57.173 % (gap inclus), EV 1.7521 % — **REFUSE**
      - refuse : cible atteinte seulement 3.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 58.83 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 53.635 %) — p(stop avant cible) 0.0571 [0.04 ; 0.09], R/R 0.955, perte reelle 62.69 % (gap inclus), EV 1.4526 % — **REFUSE**
      - refuse : cible atteinte seulement 3.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 62.95 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 62.574 %) — p(stop avant cible) 0.04 [0.02 ; 0.06], R/R 0.944, perte reelle 63.419 % (gap inclus), EV 1.7886 % — **REFUSE**
      - refuse : cible atteinte seulement 3.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 60.62 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 71.513 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.837, perte reelle 71.513 % (gap inclus), EV 2.6143 % — **REFUSE**
      - refuse : cible atteinte seulement 3.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.88 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 80.452 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.744, perte reelle 80.452 % (gap inclus), EV 2.6143 % — **REFUSE**
      - refuse : cible atteinte seulement 3.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.88 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 89.391 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.67, perte reelle 89.391 % (gap inclus), EV 2.6143 % — **REFUSE**
      - refuse : cible atteinte seulement 3.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.88 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 98.331 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.609, perte reelle 98.331 % (gap inclus), EV 2.6143 % — **REFUSE**
      - refuse : cible atteinte seulement 3.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.88 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 16.9, ATR14 3.0214 (17.878 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.4 ATR = 7.151 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.894 % | 16.7489 | 87.35 % | 90.87 % | 93.12 % | 94.59 % | 95.65 % | 97.2 % |
| 0.1 ATR | 1.788 % | 16.5979 | 82.45 % | 87.14 % | 90.28 % | 92.13 % | 94.16 % | 96.3 % |
| 0.15 ATR | 2.682 % | 16.4468 | 78.24 % | 83.51 % | 87.33 % | 88.98 % | 92.28 % | 95.2 % |
| 0.2 ATR | 3.576 % | 16.2957 | 72.45 % | 79.29 % | 83.5 % | 85.93 % | 89.91 % | 93.01 % |
| 0.25 ATR | 4.47 % | 16.1446 | 66.57 % | 74.68 % | 79.47 % | 82.78 % | 87.83 % | 91.41 % |
| 0.35 ATR | 6.257 % | 15.8425 | 54.71 % | 65.55 % | 71.22 % | 75.98 % | 83.09 % | 87.91 % |
| 0.5 ATR | 8.939 % | 15.3893 | 40.69 % | 53.78 % | 62.18 % | 69.19 % | 78.73 % | 85.51 % |
| 0.75 ATR | 13.409 % | 14.6339 | 22.65 % | 37.98 % | 47.74 % | 56.1 % | 68.15 % | 77.12 % |
| 1.0 ATR | 17.878 % | 13.8786 | 12.75 % | 25.12 % | 34.09 % | 44.69 % | 58.06 % | 68.93 % |
| 1.25 ATR | 22.348 % | 13.1232 | 7.45 % | 17.96 % | 25.05 % | 37.01 % | 51.24 % | 62.64 % |
| 1.5 ATR | 26.817 % | 12.3679 | 3.63 % | 11.58 % | 17.78 % | 29.43 % | 44.02 % | 56.34 % |
| 2.0 ATR | 35.757 % | 10.8571 | 0.88 % | 5.4 % | 10.02 % | 17.52 % | 32.44 % | 45.05 % |
| 2.5 ATR | 44.696 % | 9.3464 | 0.1 % | 2.36 % | 4.91 % | 10.33 % | 22.26 % | 35.06 % |
| 3.0 ATR | 53.635 % | 7.8357 | 0.1 % | 1.18 % | 2.65 % | 7.09 % | 15.92 % | 27.17 % |
| 4.0 ATR | 71.513 % | 4.8143 | 0.0 % | 0.79 % | 1.47 % | 3.15 % | 9.1 % | 17.98 % |
| 6.0 ATR | 107.27 % | -1.2286 | 0.0 % | 0.0 % | 0.29 % | 0.79 % | 2.77 % | 8.59 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.40 ATR | 0.45 ATR | 0.61 ATR | 0.72 ATR | 0.82 ATR | 1.13 ATR | 1.41 ATR |
| **2 s.** | 0.25 ATR | 0.56 ATR | 0.64 ATR | 0.85 ATR | 1.00 ATR | 1.18 ATR | 1.63 ATR | 2.07 ATR |
| **3 s.** | 0.30 ATR | 0.71 ATR | 0.80 ATR | 1.03 ATR | 1.25 ATR | 1.42 ATR | 2.00 ATR | 2.49 ATR |
| **5 s.** | 0.37 ATR | 0.88 ATR | 0.99 ATR | 1.38 ATR | 1.69 ATR | 1.90 ATR | 2.55 ATR | 3.53 ATR |
| **10 s.** | 0.59 ATR | 1.29 ATR | 1.47 ATR | 1.98 ATR | 2.37 ATR | 2.68 ATR | 3.87 ATR | 5.29 ATR |
| **20 s.** | 0.81 ATR | 1.78 ATR | 2.00 ATR | 2.63 ATR | 3.24 ATR | 3.78 ATR | 5.70 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.454 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (87.0 % des re-echantillons)
- **2 seance(s)** : plage utile VIDE (borne basse 0.639 ATR au-dessus du haut de la grille, 0.5 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile VIDE (borne basse 0.8 ATR au-dessus du haut de la grille, 0.75 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.993–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (17.878 %, prix 13.8786), p(touche) 44.69 % (en stress 97.06 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile VIDE (borne basse 1.466 ATR au-dessus du haut de la grille, 1.0 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile VIDE (borne basse 2.003 ATR au-dessus du haut de la grille, 1.0 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 72.0 | bear 8.2 | side 19.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.807% → cible +9.012% / stop −5.407%, p_fill 80%, n_eff≈86.3) : P(cible|rempli) **6%** · **EV/risk -0.171** (×p_fill ; si rempli -1.16% du capital)
  - **swing** (entrée dip −1.795% → cible +22.098% / stop −12.0%, p_fill 77%, n_eff≈88.6) : P(cible|rempli) **9%** · **EV/risk -0.106** (×p_fill ; si rempli -1.66% du capital)
  - **deep** (entrée dip −2.585% → cible +37.859% / stop −18.0%, p_fill 74%, n_eff≈82.2) : P(cible|rempli) **6%** · **EV/risk -0.090** (×p_fill ; si rempli -2.19% du capital)
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
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.18 · part idiosyncratique 0.82
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 27.2  _(survente)_
- **ADX** : 21.0  _(pas de tendance nette)_
- **MACD** : hist -0.816  _(pas de croisement recent)_
- **BB** : %B 0.21 · largeur 92.4%
- **ATR** : 3.02 (71.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.209  _(accumulation)_
- **Vol ratio** : 0.44  _(volume atone)_
- **Choppiness** : 31.2  _(marche directionnel)_
- **MA** : MA20 23.13 · MA50 26.08 · MA200 29.87  _(prix < MA20)_
- **Dist MA** : MA20 -26.9% · MA50 -35.2% · MA200 -43.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (688499 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
