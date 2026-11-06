# SOI

**Generated** : 2026-11-06T21:48:29.881638+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 6.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €94.34  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-06 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)  
> ↳ spot €94.34 (+3.5% vs entrée) · entrée €91.17 · stop €88.06 · T1 €96.35 · R/R 1.67  
> ↳ _probas brutes, non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-06 : 94.34 · ATR Wilder 10.51 (11.14 %)_
- **Swing** : plage **78.68 → 70.39** (-16.6 % a -25.39 % sous la cloture, 0.79 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 77.85-82.4 (A) ; 68.5-72.9 (B). stop INDICATIF 55.65 (-20.94 % sous le bas ; sous le support 60.9-65.16 (- 0,5 ATR)).
- **Deep** : plage **70.39 → 35.6** (-25.39 % a -62.26 % sous la cloture, 3.31 ATR) — touchee 50 % → 15 % du temps en 20 seances ; supports reels dans la plage : 68.5-72.9 (B) ; 60.9-65.16 (B) ; 54.8-59.3 (B) ; 48.55-53.65 (A) ; 43.14-47.59 (A) ; 36.01-41.03 (A). stop INDICATIF 22.79 (-36.0 % sous le bas ; sous le support 28.04-30.89 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 6.25 ATR sous le plus haut 20 s., RSI(2) 19.4. Limite **89.09** (seance suivante), stop catastrophe 47.07, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 84.75-89.15 (B, -5.5 %) ; 77.85-82.4 (A, -12.66 %) ; 68.5-72.9 (B, -22.73 %) ; 60.9-65.16 (B, -30.93 %) ; 54.8-59.3 (B, -37.14 %) ; 48.55-53.65 (A, -43.13 %)
- Resistances reelles au-dessus : 97.95-102.4 (A, 3.83 %) ; 104.8-109.55 (A, 11.09 %) ; 110.4-114.9 (A, 17.02 %) ; 116.8-121.8 (A, 23.81 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.30 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (18.37 %)** : le gap seul le franchit 0.156 % des séances (2 fois sur 1280).
   - exécution **5.636 pt plus bas** dans le cas TYPIQUE (médiane), 9.866 au p90, **10.924 au pire**
   - perte réelle **24.006 %** en moyenne _(tirée par la queue)_, jusqu'à **29.294 %** — au lieu des 18.37 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0088 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 2 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.808 % | p01 -5.347 % | pire -29.294 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4146** [0.3431 ; 0.4889] _(largeur 14.6 pt, n_eff 173.1)_
   - swing : **0.2636** [0.2193 ; 0.3119] _(largeur 9.3 pt, n_eff 345.8)_
   - deep : **0.2197** [0.1785 ; 0.2656] _(largeur 8.7 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (25.7 pt), swing (29.9 pt), deep (31.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 300 séances)** : VaR **-9.6 %** | CVaR **-14.22 %** | vol 6.43 %/j
   - _fenêtre arrêtée : rupture de regime a 360 seances en arriere (volatilite 2.86 % contre 6.85 % aujourd'hui, rapport 0.42)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.13 % vs -12.04 % si l'on extrapolait par √5 _(rapport 1.09 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0598** (β de hausse 1.5561, asymétrie 0.6811) vs FCHI — 623 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.017× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 86.5727 sur atr_grid (0.75 ATR, 8.233 %) — p(stop avant cible) 0.5622 [0.51 ; 0.61], R/R 4.355, perte reelle 8.576 % (gap inclus), CVaR 11.918 %, EV 1.7803 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.5607 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 8.3 % du temps (< 15 %) meme a 10 seances : le R/R de 4.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.562, borne haute 0.614 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 1.22 ATR (stop 16.712 %) — p(stop avant cible) 0.2547 [0.21 ; 0.30], R/R 2.185, perte reelle 17.098 % (gap inclus), EV 2.5818 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.68 % > budget 12.00 %
   - 🟢 support a 2.82 ATR (stop 34.202 %) — p(stop avant cible) 0.0207 [0.01 ; 0.04], R/R 1.092, perte reelle 34.202 % (gap inclus), EV 2.8665 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.75 % > budget 12.00 %
   - 🟢 support a 5.26 ATR (stop 61.031 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.612, perte reelle 61.031 % (gap inclus), EV 2.9246 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.57 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 2.744 %) — p(stop avant cible) 0.8012 [0.76 ; 0.84], R/R 12.831, perte reelle 2.911 % (gap inclus), EV 1.5747 % — **REFUSE**
      - refuse : cible atteinte seulement 4.8 % du temps (< 15 %) meme a 10 seances : le R/R de 12.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.801, borne haute 0.841 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 5.489 %) — p(stop avant cible) 0.6467 [0.60 ; 0.70], R/R 6.301, perte reelle 5.928 % (gap inclus), EV 2.2818 % — **REFUSE**
      - refuse : cible atteinte seulement 7.2 % du temps (< 15 %) meme a 10 seances : le R/R de 6.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.647, borne haute 0.696 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 8.233 %) — p(stop avant cible) 0.5622 [0.51 ; 0.61], R/R 4.355, perte reelle 8.576 % (gap inclus), EV 1.7803 % — **REFUSE**
      - refuse : cible atteinte seulement 8.3 % du temps (< 15 %) meme a 10 seances : le R/R de 4.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.562, borne haute 0.614 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.75 ATR (stop 19.211 %) — p(stop avant cible) 0.2021 [0.16 ; 0.25], R/R 1.901, perte reelle 19.644 % (gap inclus), EV 2.7773 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.96 % > budget 12.00 %
   - ⚪ atr_grid a 2.0 ATR (stop 21.956 %) — p(stop avant cible) 0.1408 [0.11 ; 0.18], R/R 1.676, perte reelle 22.291 % (gap inclus), EV 2.8789 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.90 % > budget 12.00 %
   - ⚪ atr_grid a 2.25 ATR (stop 24.7 %) — p(stop avant cible) 0.0875 [0.06 ; 0.12], R/R 1.495, perte reelle 24.978 % (gap inclus), EV 2.9649 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.19 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 27.444 %) — p(stop avant cible) 0.0544 [0.03 ; 0.08], R/R 1.349, perte reelle 27.691 % (gap inclus), EV 2.9151 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.71 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 38.422 %) — p(stop avant cible) 0.0086 [0.00 ; 0.02], R/R 0.972, perte reelle 38.443 % (gap inclus), EV 2.8801 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.48 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 43.911 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.851, perte reelle 43.911 % (gap inclus), EV 2.9246 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.57 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 49.4 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.756, perte reelle 49.4 % (gap inclus), EV 2.9246 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.57 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 54.889 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.68, perte reelle 54.889 % (gap inclus), EV 2.9246 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.57 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 65.867 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.567, perte reelle 65.867 % (gap inclus), EV 2.9246 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.57 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 71.356 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.523, perte reelle 71.356 % (gap inclus), EV 2.9246 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.57 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 76.844 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.486, perte reelle 76.844 % (gap inclus), EV 2.9246 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.57 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 82.333 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.454, perte reelle 82.333 % (gap inclus), EV 2.9246 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.57 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 87.822 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.425, perte reelle 87.822 % (gap inclus), EV 2.9246 % — **REFUSE**
      - refuse : cible atteinte seulement 10.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.57 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 94.34, ATR14 10.3564 (10.978 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.359 ATR = 3.941 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.549 % | 93.8222 | 91.18 % | 94.21 % | 95.48 % | 96.56 % | 97.73 % | 98.7 % |
| 0.1 ATR | 1.098 % | 93.3044 | 84.61 % | 89.89 % | 91.75 % | 94.29 % | 96.04 % | 97.2 % |
| 0.15 ATR | 1.647 % | 92.7865 | 77.65 % | 84.89 % | 87.52 % | 90.75 % | 93.57 % | 95.1 % |
| 0.2 ATR | 2.196 % | 92.2687 | 68.92 % | 79.78 % | 83.6 % | 87.8 % | 91.39 % | 93.31 % |
| 0.25 ATR | 2.744 % | 91.7509 | 62.55 % | 75.96 % | 80.16 % | 86.12 % | 90.11 % | 92.81 % |
| 0.35 ATR | 3.842 % | 90.7152 | 50.88 % | 67.52 % | 73.18 % | 80.91 % | 85.86 % | 90.21 % |
| 0.5 ATR | 5.489 % | 89.1618 | 36.27 % | 55.74 % | 62.97 % | 73.23 % | 81.11 % | 87.41 % |
| 0.75 ATR | 8.233 % | 86.5727 | 17.06 % | 35.33 % | 46.66 % | 58.27 % | 72.6 % | 80.62 % |
| 1.0 ATR | 10.978 % | 83.9836 | 8.24 % | 23.65 % | 34.09 % | 47.34 % | 64.49 % | 75.22 % |
| 1.25 ATR | 13.722 % | 81.3945 | 4.22 % | 15.8 % | 25.44 % | 37.7 % | 56.87 % | 70.23 % |
| 1.5 ATR | 16.467 % | 78.8054 | 2.35 % | 10.7 % | 18.57 % | 30.12 % | 49.06 % | 64.04 % |
| 2.0 ATR | 21.956 % | 73.6271 | 0.59 % | 4.61 % | 9.23 % | 18.31 % | 35.31 % | 53.45 % |
| 2.5 ATR | 27.444 % | 68.4489 | 0.29 % | 2.55 % | 5.11 % | 12.01 % | 24.53 % | 45.65 % |
| 3.0 ATR | 32.933 % | 63.2707 | 0.2 % | 0.88 % | 2.65 % | 7.38 % | 17.21 % | 37.56 % |
| 4.0 ATR | 43.911 % | 52.9143 | 0.1 % | 0.59 % | 1.38 % | 3.54 % | 10.19 % | 23.98 % |
| 6.0 ATR | 65.867 % | 32.2014 | 0.0 % | 0.29 % | 0.79 % | 1.57 % | 4.45 % | 12.39 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.36 ATR | 0.41 ATR | 0.54 ATR | 0.65 ATR | 0.71 ATR | 0.95 ATR | 1.20 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.63 ATR | 0.80 ATR | 0.97 ATR | 1.12 ATR | 1.56 ATR | 1.97 ATR |
| **3 s.** | 0.32 ATR | 0.70 ATR | 0.78 ATR | 1.03 ATR | 1.27 ATR | 1.45 ATR | 1.96 ATR | 2.52 ATR |
| **5 s.** | 0.47 ATR | 0.94 ATR | 1.06 ATR | 1.41 ATR | 1.72 ATR | 1.93 ATR | 2.72 ATR | 3.62 ATR |
| **10 s.** | 0.68 ATR | 1.47 ATR | 1.65 ATR | 2.11 ATR | 2.48 ATR | 2.81 ATR | 4.07 ATR | 5.81 ATR |
| **20 s.** | 1.01 ATR | 2.22 ATR | 2.54 ATR | 3.34 ATR | 3.92 ATR | 4.69 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.41 ATR au-dessus du haut de la grille, 0.25 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (61.9 % des re-echantillons)
- **2 seance(s)** : plage utile VIDE (borne basse 0.632 ATR au-dessus du haut de la grille, 0.5 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile VIDE (borne basse 0.783 ATR au-dessus du haut de la grille, 0.75 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile VIDE (borne basse 1.061 ATR au-dessus du haut de la grille, 1.0 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 17.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile VIDE (borne basse 1.648 ATR au-dessus du haut de la grille, 1.5 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 19.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile VIDE (borne basse 2.54 ATR au-dessus du haut de la grille, 1.5 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 42.5 | bear 40.2 | side 17.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.357% → cible +5.68% / stop −3.408%, p_fill 48%, n_eff≈51.0) : P(cible|rempli) **5%** · **EV/risk -0.047** (×p_fill ; si rempli -0.33% du capital)
  - **swing** (entrée dip −7.392% → cible +21.808% / stop −11.854%, p_fill 32%, n_eff≈39.2) : P(cible|rempli) **8%** · **EV/risk -0.049** (×p_fill ; si rempli -1.83% du capital)
  - **deep** (entrée dip −11.427% → cible +27.353% / stop −18.0%, p_fill 31%, n_eff≈36.5) : P(cible|rempli) **19%** · **EV/risk +0.005** (×p_fill ; si rempli +0.29% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→83% · +1.0%→74% · +2.0%→62% · +3.0%→46% · +5.0%→29% · +8.0%→10%
- Range intraday médian 7.0% (p90 13.76%) · excursion haute méd. +2.7% / basse méd. −3.24%
- Profil de vol intra : ouverture 4.423% vs midi 1.287% vs clôture 1.954% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 13% · trend ↑1%/↓1% ; spike-down 73% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; neutre — autocorr 0.002)_ ; drift intra méd. -0.88% ; recovery-V 29%
- **σ réalisé intraday** 3.81% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 78% / whipsaw 36%
- POC intraday (dernière séance, temps-au-prix) : 111.4765 (VA 109.8045–114.4025 ; dernier close 111.96)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 30% · rebond 66% · **stop −6.95%** sous le fill (sous le bruit) · cible +2.1% · R/R 0.3 (high win-rate)
- Gaps overnight (n=159) : méd. 0.56% · baisse 40% (gap-down >1% 26% · >2% 18%)
- Excursion ouverture 5min (n=160) : bas méd −1.01% (p90 −3.1%) · haut méd +0.82% · range méd 2.14%
- Excursion ouverture 15min (n=160) : bas méd −1.4% (p90 −3.34%) · haut méd +1.06% · range méd 2.95%
- Excursion ouverture 30min (n=160) : bas méd −1.56% (p90 −3.74%) · haut méd +1.13% · range méd 3.18%
- Excursion ouverture 60min (n=160) : bas méd −1.76% (p90 −4.51%) · haut méd +1.44% · range méd 3.65%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 111.65 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 77% (120/159) · gap 33% · délai 0.2min · rebond 61% (78/120) (MFE +1.63%)
   - −1.0% : fill 30min 55% · séance 73% (114/159) · gap 26% · délai 0.2min · rebond 63% (76/114) (MFE +1.69%)
   - −1.5% : fill 30min 48% · séance 65% (104/159) · gap 21% · délai 1.3min · rebond 58% (72/104) (MFE +1.84%)
   - −2.0% : fill 30min 44% · séance 62% (98/159) · gap 18% · délai 4.5min · rebond 66% (72/98) (MFE +1.89%)
   - −3.0% : fill 30min 30% · séance 47% (80/159) · gap 9% · délai 8.9min · rebond 73% (66/80) (MFE +1.88%)
   - −4.0% : fill 30min 21% · séance 39% (68/159) · gap 6% · délai 15.4min · rebond 72% (54/68) (MFE +1.92%)
   - −5.0% : fill 30min 14% · séance 30% (53/159) · gap 3% · délai 38.9min · rebond 66% (39/53) (MFE +2.1%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.44% (p90 −3.17%) → stop au-delà de −1.93% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.66% (p90 −3.07%) → stop au-delà de −1.96% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.7% (p90 −2.29%) → stop au-delà de −1.88% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1324 jambes) : jambe baissière méd −1.26% (p90 −3.04%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (59 séances) :
      · −1.0% : fill 95% (56/59) · rebond 52% (33/56)
      · −2.0% : fill 93% (54/59) · rebond 60% (37/54)
      · −3.0% : fill 80% (49/59) · rebond 64% (38/49)
      · −4.0% : fill 68% (42/59) · rebond 70% (35/42)
      · −5.0% : fill 59% (35/59) · rebond 68% (27/35)
   - **flat** (11 séances) :
      · −1.0% : fill 83% (10/11) · rebond 66% (7/10)
      · −2.0% : fill 74% (9/11) · rebond 65% (7/9)
      · −3.0% : fill 74% (9/11) · rebond 73% (7/9)
      · −4.0% : fill 68% (8/11) · rebond 85% (6/8)
      · −5.0% : fill 55% (7/11) · rebond 63% (5/7)
   - **gap-up** (89 séances) :
      · −1.0% : fill 58% (48/89) · rebond 74% (36/48)
      · −2.0% : fill 40% (35/89) · rebond 74% (28/35)
      · −3.0% : fill 22% (22/89) · rebond 92% (21/22)
      · −4.0% : fill 16% (18/89) · rebond 72% (13/18)
      · −5.0% : fill 8% (11/89) · rebond 60% (7/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 62% si les 15 1res min sont vertes (75 cas) · 31% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **10min** → P(séance verte=clôture>ouverture) 63% si début vert vs 28% si rouge (base 44% · écart 34 pts) ; prédictivité sature ensuite (plafond brut 284min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **63%** · continue >prix actuel 51% ; creux résiduel méd -2.33% (q20 -4.61%) → **SL/trailing à −4.61%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.95% / q75 +5.39% → **scale +2.95% / runner +5.39%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **28%** (continue à baisser 61%) → **RÉDUIRE ~72%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.99%** (au-delà de la MAE q10 -6.99%), cible rebond +2.08% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.33% .. +4.1%] · haut q95 +5.94% · bas q05 -5.72%
   - 60min (n=160) : retour [-4.39% .. +4.55%] · haut q95 +6.48% · bas q05 -5.91%
   - 2h (n=160) : retour [-5.15% .. +5.34%] · haut q95 +7.16% · bas q05 -6.63%
   - 4h (n=160) : retour [-5.33% .. +6.48%] · haut q95 +7.84% · bas q05 -7.2%
   - 6h (n=160) : retour [-6.3% .. +7.83%] · haut q95 +8.85% · bas q05 -7.75%
   - session (n=160) : retour [-7.87% .. +8.67%] · haut q95 +10.28% · bas q05 -9.9%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 6.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **38%**. Lecture précoce 30 min : signature présente → 16% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.98% (p75 1.4% / p90 1.99%) · ~5.0 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **90%** (reprise méd 24.99 min, n=53)
   - −1.0% → **91%** (reprise méd 44.55 min, n=28)
   - −1.5% → **80%** (reprise méd 50.92 min, n=16)
   - −2.0% → **85%** (reprise méd 52.07 min, n=12)
   - −3.0% → **100%** (reprise méd 60.96 min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.99%** (p90, défaut prudent ; serré/agressif −1.4%) ; extension open→close méd +8.74% (q75 +9.27% / q95 +13.89%), MFE méd +9.37% / q90 +14.21%
   - Échelle scale-out : +9.37% (33%) / +10.06% (33%) / +14.21% (34%)
- **DÉSARMER** : repli > **−1.99%** depuis le plus-haut = décay → P(retournement) **15%** (préavis méd 36.46 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +14.21% : P(retournement après) 0% (mèche méd 2.71%)
- **CONTEXTE** : la dernière heure tient les gains 78% du temps (retour médian dernière heure +1.29%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.53 · part idiosyncratique 0.47
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-06 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-10 — US CPI (headline) (J-3 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-10 — US CPI (headline) (J-3 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 32.7  _(momentum baissier)_
- **ADX** : 25.1  _(tendance etablie)_
- **MACD** : hist -3.144  _(pas de croisement recent)_
- **BB** : %B 0.02 · largeur 48.5%
- **ATR** : 10.36 (70.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.18  _(distribution)_
- **Vol ratio** : 1.55  _(volume au-dessus de la moyenne)_
- **Choppiness** : 43.3  _(transition)_
- **MA** : MA20 123.26 · MA50 135.4 · MA200 105.94  _(prix < MA20)_
- **Dist MA** : MA20 -23.5% · MA50 -30.3% · MA200 -10.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (706851 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
