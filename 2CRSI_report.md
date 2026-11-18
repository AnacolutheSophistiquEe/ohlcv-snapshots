# AL2SI

**Generated** : 2026-11-18T01:12:51.426202+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 13.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €16.53  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 39/125 fenêtres (p_fill pondéré 28 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot €16.53 (+5.3% vs entrée) · entrée €15.70 · stop €14.76 · T1 €17.58 · R/R 2.0  
> ↳ _probas brutes, non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-17 : 16.53 · ATR Wilder 2.28 (13.78 %)_
- **Swing** : plage **13.87 → 12.12** (-16.11 % a -26.68 % sous la cloture, 0.77 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 12.4-13.24 (B). stop INDICATIF 10.08 (-16.82 % sous le bas ; sous le support 11.22-12.08 (- 0,5 ATR)).
- **Deep** : plage **12.12 → 8.04** (-26.68 % a -51.38 % sous la cloture, 1.79 ATR) — touchee 41 % → 15 % du temps en 20 seances ; supports reels dans la plage : 11.22-12.08 (A) ; 10.0-10.82 (A) ; 8.83-9.86 (A) ; 7.12-8.22 (A). stop INDICATIF 4.29 (-46.61 % sous le bas ; sous le support 5.43-6.45 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 5.49 ATR sous le plus haut 20 s., RSI(2) 9.1. Limite **15.39** (seance suivante), stop catastrophe 6.28, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 14.2-15.1 (A, -8.65 %) ; 12.4-13.24 (B, -19.9 %) ; 11.22-12.08 (A, -26.92 %) ; 10.0-10.82 (A, -34.54 %) ; 8.83-9.86 (A, -40.35 %) ; 7.12-8.22 (A, -50.27 %)
- Resistances reelles au-dessus : 20.1-21.05 (A, 21.6 %) ; 22.6-23.55 (A, 36.72 %) ; 25.0-25.4 (A, 51.24 %) ; 26.38-26.7 (A, 59.59 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.67 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (21.75 %)** : le gap seul le franchit 0.391 % des séances (5 fois sur 1280).
   - exécution **5.415 pt plus bas** dans le cas TYPIQUE (médiane), 25.577 au p90, **31.717 au pire**
   - perte réelle **33.787 %** en moyenne _(tirée par la queue)_, jusqu'à **53.467 %** — au lieu des 21.75 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.047 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.501 % | p01 -7.775 % | pire -53.467 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1641** [0.1147 ; 0.2246] _(largeur 11.0 pt, n_eff 173.1)_
   - swing : **0.2435** [0.2005 ; 0.2907] _(largeur 9.0 pt, n_eff 345.8)_
   - deep : **0.2377** [0.1951 ; 0.2846] _(largeur 8.9 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : swing (42.6 pt), deep (44.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.5 %** | CVaR **-14.89 %** | vol 7.01 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 4.69 % contre 8.42 % aujourd'hui, rapport 0.56)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -15.54 % vs -14.4 % si l'on extrapolait par √5 _(rapport 1.079 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1779** (β de hausse 0.9663, asymétrie 1.219) vs FCHI — 623 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.879× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 15.7736 sur atr_grid (0.25 ATR, 4.576 %) — p(stop avant cible) 0.7545 [0.71 ; 0.80], R/R 10.56, perte reelle 6.015 % (gap inclus), CVaR 25.074 %, EV 0.6337 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 2.3777 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 2.4 % du temps (< 15 %) meme a 10 seances : le R/R de 10.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.754, borne haute 0.798 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 25.07 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 7 des 7 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 77.2 % de la queue et il ne reste que -727.42 EUR a partager. Prix du risque -1.8 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.67 ATR (stop 18.059 %) — p(stop avant cible) 0.2377 [0.20 ; 0.28], R/R 2.655, perte reelle 23.925 % (gap inclus), EV 1.8251 % — **REFUSE**
      - refuse : cible atteinte seulement 3.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.46 % > budget 12.00 %
   - 🟢 support a 1.1 ATR (stop 25.893 %) — p(stop avant cible) 0.1323 [0.10 ; 0.17], R/R 1.993, perte reelle 31.876 % (gap inclus), EV 2.2257 % — **REFUSE**
      - refuse : cible atteinte seulement 3.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.86 % > budget 12.00 %
   - 🟢 support a 1.74 ATR (stop 37.629 %) — p(stop avant cible) 0.0927 [0.07 ; 0.13], R/R 1.21, perte reelle 52.516 % (gap inclus), EV 0.977 % — **REFUSE**
      - refuse : cible atteinte seulement 3.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 61.05 % > budget 12.00 %
   - 🟢 support a 2.16 ATR (stop 45.252 %) — p(stop avant cible) 0.0756 [0.05 ; 0.11], R/R 1.131, perte reelle 56.142 % (gap inclus), EV 1.2602 % — **REFUSE**
      - refuse : cible atteinte seulement 3.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 61.05 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 4.576 %) — p(stop avant cible) 0.7545 [0.71 ; 0.80], R/R 10.56, perte reelle 6.015 % (gap inclus), EV 0.6337 % — **REFUSE**
      - refuse : cible atteinte seulement 2.4 % du temps (< 15 %) meme a 10 seances : le R/R de 10.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.754, borne haute 0.798 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 25.07 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 50.337 %) — p(stop avant cible) 0.0699 [0.05 ; 0.10], R/R 1.054, perte reelle 60.278 % (gap inclus), EV 1.2435 % — **REFUSE**
      - refuse : cible atteinte seulement 3.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 62.70 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 54.913 %) — p(stop avant cible) 0.0668 [0.04 ; 0.10], R/R 1.011, perte reelle 62.826 % (gap inclus), EV 1.0975 % — **REFUSE**
      - refuse : cible atteinte seulement 3.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 63.34 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 64.065 %) — p(stop avant cible) 0.0335 [0.02 ; 0.06], R/R 0.987, perte reelle 64.326 % (gap inclus), EV 1.8378 % — **REFUSE**
      - refuse : cible atteinte seulement 3.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 58.28 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 73.218 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.868, perte reelle 73.218 % (gap inclus), EV 2.541 % — **REFUSE**
      - refuse : cible atteinte seulement 3.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.91 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 82.37 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.771, perte reelle 82.37 % (gap inclus), EV 2.541 % — **REFUSE**
      - refuse : cible atteinte seulement 3.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.91 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 91.522 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.694, perte reelle 91.522 % (gap inclus), EV 2.541 % — **REFUSE**
      - refuse : cible atteinte seulement 3.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.91 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 16.53, ATR14 3.0257 (18.304 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.398 ATR = 7.285 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.915 % | 16.3787 | 87.35 % | 90.87 % | 93.12 % | 94.69 % | 95.75 % | 97.2 % |
| 0.1 ATR | 1.83 % | 16.2274 | 82.45 % | 87.14 % | 90.28 % | 92.22 % | 94.16 % | 96.3 % |
| 0.15 ATR | 2.746 % | 16.0761 | 78.14 % | 83.51 % | 87.33 % | 89.07 % | 92.28 % | 95.2 % |
| 0.2 ATR | 3.661 % | 15.9249 | 72.35 % | 79.2 % | 83.4 % | 85.93 % | 89.91 % | 93.01 % |
| 0.25 ATR | 4.576 % | 15.7736 | 66.37 % | 74.48 % | 79.27 % | 82.68 % | 87.83 % | 91.41 % |
| 0.35 ATR | 6.407 % | 15.471 | 54.51 % | 65.26 % | 70.92 % | 75.79 % | 82.99 % | 87.91 % |
| 0.5 ATR | 9.152 % | 15.0171 | 40.39 % | 53.48 % | 61.89 % | 69.0 % | 78.64 % | 85.51 % |
| 0.75 ATR | 13.728 % | 14.2607 | 22.55 % | 37.78 % | 47.35 % | 55.81 % | 68.05 % | 77.12 % |
| 1.0 ATR | 18.304 % | 13.5043 | 12.65 % | 24.93 % | 33.89 % | 44.49 % | 57.96 % | 68.93 % |
| 1.25 ATR | 22.88 % | 12.7479 | 7.35 % | 17.86 % | 24.95 % | 36.81 % | 51.14 % | 62.64 % |
| 1.5 ATR | 27.457 % | 11.9914 | 3.63 % | 11.48 % | 17.68 % | 29.33 % | 43.92 % | 56.34 % |
| 2.0 ATR | 36.609 % | 10.4786 | 0.88 % | 5.4 % | 10.02 % | 17.52 % | 32.34 % | 45.05 % |
| 2.5 ATR | 45.761 % | 8.9657 | 0.1 % | 2.36 % | 4.91 % | 10.33 % | 22.26 % | 35.06 % |
| 3.0 ATR | 54.913 % | 7.4529 | 0.1 % | 1.18 % | 2.65 % | 7.09 % | 15.92 % | 27.17 % |
| 4.0 ATR | 73.218 % | 4.4271 | 0.0 % | 0.79 % | 1.47 % | 3.15 % | 9.3 % | 18.08 % |
| 6.0 ATR | 109.826 % | -1.6243 | 0.0 % | 0.0 % | 0.29 % | 0.79 % | 2.97 % | 9.09 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.40 ATR | 0.45 ATR | 0.60 ATR | 0.72 ATR | 0.81 ATR | 1.12 ATR | 1.41 ATR |
| **2 s.** | 0.24 ATR | 0.56 ATR | 0.64 ATR | 0.84 ATR | 1.00 ATR | 1.17 ATR | 1.62 ATR | 2.07 ATR |
| **3 s.** | 0.30 ATR | 0.70 ATR | 0.79 ATR | 1.02 ATR | 1.25 ATR | 1.42 ATR | 2.00 ATR | 2.49 ATR |
| **5 s.** | 0.37 ATR | 0.88 ATR | 0.99 ATR | 1.38 ATR | 1.68 ATR | 1.90 ATR | 2.55 ATR | 3.53 ATR |
| **10 s.** | 0.59 ATR | 1.29 ATR | 1.46 ATR | 1.97 ATR | 2.36 ATR | 2.68 ATR | 3.89 ATR | 5.36 ATR |
| **20 s.** | 0.81 ATR | 1.78 ATR | 2.00 ATR | 2.63 ATR | 3.24 ATR | 3.79 ATR | 5.80 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.451 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (83.6 % des re-echantillons)
- **2 seance(s)** : plage utile VIDE (borne basse 0.635 ATR au-dessus du haut de la grille, 0.5 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile VIDE (borne basse 0.794 ATR au-dessus du haut de la grille, 0.75 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.989–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (18.304 %, prix 13.5043), p(touche) 44.49 % (en stress 97.06 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile VIDE (borne basse 1.463 ATR au-dessus du haut de la grille, 1.0 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile VIDE (borne basse 2.003 ATR au-dessus du haut de la grille, 1.0 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 73.3 | bear 5.0 | side 21.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −5.034% → cible +11.976% / stop −5.988%, p_fill 28%, n_eff≈33.8) : P(cible|rempli) **6%** · **EV/risk +0.024** (×p_fill ; si rempli +0.51% du capital)
  - **swing** (entrée dip −11.08% → cible +37.865% / stop −12.0%, p_fill 14%, n_eff≈18.6) : P(cible|rempli) **10%** · **EV/risk +0.007** (×p_fill ; si rempli +0.61% du capital)
  - **deep** (entrée dip −17.122% → cible +47.919% / stop −18.0%, p_fill 13%, n_eff≈16.9) : P(cible|rempli) **12%** · **EV/risk -0.037** (×p_fill ; si rempli -5.18% du capital)
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

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.21 · part idiosyncratique 0.79
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 28.5  _(survente)_
- **ADX** : 20.0  _(pas de tendance nette)_
- **MACD** : hist -0.082  _(pas de croisement recent)_
- **BB** : %B 0.29 · largeur 99.5%
- **ATR** : 3.03 (70.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF 0.149  _(accumulation)_
- **Vol ratio** : 0.29  _(volume atone)_
- **Choppiness** : 32.6  _(marche directionnel)_
- **MA** : MA20 20.88 · MA50 25.02 · MA200 29.93  _(prix < MA20)_
- **Dist MA** : MA20 -20.8% · MA50 -33.9% · MA200 -44.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (672148 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
