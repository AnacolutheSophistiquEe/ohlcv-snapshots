# HOOD

**Generated** : 2026-11-03T01:29:19.961322+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 3/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $83.82  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-05 — Bank of England — décision de taux (J-1 sess · macro taux)  
> ↳ spot $83.82 (+0.4% vs entrée) · entrée $83.45 · stop $80.95 · T1 $86.37 · R/R 1.17  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +2.4 % ≠ (strike 87.0 − spot 83.82)/spot = +3.8 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-02 : 83.82 · ATR Wilder 5.42 (6.47 %)_
- **Swing** : plage **77.78 → 73.15** (-7.22 % a -12.73 % sous la cloture, 0.85 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 72.79-74.59 (A). stop INDICATIF 67.22 (-8.11 % sous le bas ; sous le support 69.93-72.25 (- 0,5 ATR)).
- **Deep** : plage **73.15 → 63.22** (-12.73 % a -24.59 % sous la cloture, 1.83 ATR) — touchee 41 % → 15 % du temps en 20 seances ; supports reels dans la plage : 72.79-74.59 (A) ; 69.93-72.25 (A) ; 66.91-69.22 (A) ; 62.63-63.51 (B). stop INDICATIF 57.79 (-8.58 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 5.98 ATR sous le plus haut 20 s., RSI(2) 3.2. Limite **81.11** (seance suivante), stop catastrophe 59.42, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 77.8-79.57 (A, -5.08 %) ; 72.79-74.59 (A, -11.02 %) ; 69.93-72.25 (A, -13.81 %) ; 66.91-69.22 (A, -17.42 %) ; 62.63-63.51 (B, -24.23 %) ; 52.65-54.84 (B, -34.58 %)
- Resistances reelles au-dessus : 88.6-90.7 (A, 5.7 %) ; 91.44-93.36 (A, 9.08 %) ; 94.4-96.59 (A, 12.62 %) ; 98.75-100.88 (A, 17.8 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.42 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.97 %)** : le gap seul le franchit 0.718 % des séances (9 fois sur 1253).
   - exécution **3.054 pt plus bas** dans le cas TYPIQUE (médiane), 6.888 au p90, **9.815 au pire**
   - perte réelle **11.533 %** en moyenne _(tirée par la queue)_, jusqu'à **17.785 %** — au lieu des 7.97 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0256 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 9 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.488 % | p01 -6.925 % | pire -17.785 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2911** [0.2273 ; 0.3618] _(largeur 13.5 pt, n_eff 173.1)_
   - swing : **0.414** [0.363 ; 0.4665] _(largeur 10.3 pt, n_eff 345.7)_
   - deep : **0.383** [0.3329 ; 0.435] _(largeur 10.2 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 780 séances)** : VaR **-6.16 %** | CVaR **-8.97 %** | vol 4.3 %/j
   - _fenêtre arrêtée : rupture de regime a 840 seances en arriere (volatilite 2.49 % contre 4.44 % aujourd'hui, rapport 0.56)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.4 % vs -14.5 % si l'on extrapolait par √5 _(rapport 0.993 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7758** (β de hausse 1.6438, asymétrie 1.0803) vs IWM — 605 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.441× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 76.5112 sur atr_grid (1.25 ATR, 8.725 %) — p(stop avant cible) 0.4888 [0.44 ; 0.54], R/R 3.486, perte reelle 9.165 % (gap inclus), CVaR 11.857 %, EV 0.437 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.776 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 3.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.36 ATR (stop 4.501 %) — p(stop avant cible) 0.7078 [0.66 ; 0.75], R/R 6.775, perte reelle 4.716 % (gap inclus), EV 0.2614 % — **REFUSE**
      - refuse : cible atteinte seulement 2.7 % du temps (< 15 %) meme a 10 seances : le R/R de 6.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.708, borne haute 0.754 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - 🔴 support a 0.84 ATR (stop 7.85 %) — p(stop avant cible) 0.5459 [0.49 ; 0.60], R/R 3.85, perte reelle 8.299 % (gap inclus), EV 0.2042 % — **REFUSE**
      - refuse : cible atteinte seulement 3.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.546, borne haute 0.598 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.26 ATR du spot — compartiment <1, mesure a 46.6 % de casse (IC clusterise [0.432 ; 0.500] sur 1220 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_based a 1.5 ATR (stop 10.47 %) — p(stop avant cible) 0.3959 [0.35 ; 0.45], R/R 2.91, perte reelle 10.98 % (gap inclus), EV 0.6566 % — **REFUSE**
      - refuse : cible atteinte seulement 3.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.32 % > budget 12.00 %
   - 🟢 support a 2.5 ATR (stop 19.433 %) — p(stop avant cible) 0.0775 [0.05 ; 0.11], R/R 1.618, perte reelle 19.745 % (gap inclus), EV 1.2707 % — **REFUSE**
      - refuse : cible atteinte seulement 3.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.92 % > budget 12.00 %
   - 🟢 support a 3.47 ATR (stop 26.239 %) — p(stop avant cible) 0.0273 [0.01 ; 0.05], R/R 1.197, perte reelle 26.697 % (gap inclus), EV 1.289 % — **REFUSE**
      - refuse : cible atteinte seulement 3.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.53 % > budget 12.00 %
   - ⚪ atr_grid a 1.25 ATR (stop 8.725 %) — p(stop avant cible) 0.4888 [0.44 ; 0.54], R/R 3.486, perte reelle 9.165 % (gap inclus), EV 0.437 % — **REFUSE**
      - refuse : cible atteinte seulement 3.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 1.75 ATR (stop 12.215 %) — p(stop avant cible) 0.3104 [0.26 ; 0.36], R/R 2.483, perte reelle 12.867 % (gap inclus), EV 0.8357 % — **REFUSE**
      - refuse : cible atteinte seulement 3.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.05 % > budget 12.00 %
   - ⚪ atr_grid a 2.0 ATR (stop 13.96 %) — p(stop avant cible) 0.2391 [0.20 ; 0.29], R/R 2.2, perte reelle 14.527 % (gap inclus), EV 0.8644 % — **REFUSE**
      - refuse : cible atteinte seulement 3.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.57 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 20.94 %) — p(stop avant cible) 0.064 [0.04 ; 0.09], R/R 1.503, perte reelle 21.253 % (gap inclus), EV 1.2481 % — **REFUSE**
      - refuse : cible atteinte seulement 3.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.34 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 27.92 %) — p(stop avant cible) 0.0213 [0.01 ; 0.04], R/R 1.13, perte reelle 28.281 % (gap inclus), EV 1.3026 % — **REFUSE**
      - refuse : cible atteinte seulement 3.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.67 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 31.41 %) — p(stop avant cible) 0.0159 [0.01 ; 0.03], R/R 1.013, perte reelle 31.552 % (gap inclus), EV 1.3066 % — **REFUSE**
      - refuse : cible atteinte seulement 3.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.00 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 34.9 %) — p(stop avant cible) 0.0026 [0.00 ; 0.01], R/R 0.904, perte reelle 35.339 % (gap inclus), EV 1.4098 % — **REFUSE**
      - refuse : cible atteinte seulement 3.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.20 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 38.39 %) — p(stop avant cible) 0.0008 [0.00 ; 0.01], R/R 0.832, perte reelle 38.39 % (gap inclus), EV 1.4252 % — **REFUSE**
      - refuse : cible atteinte seulement 3.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.88 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 41.88 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.763, perte reelle 41.88 % (gap inclus), EV 1.4331 % — **REFUSE**
      - refuse : cible atteinte seulement 3.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.71 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 45.37 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.704, perte reelle 45.37 % (gap inclus), EV 1.4331 % — **REFUSE**
      - refuse : cible atteinte seulement 3.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.71 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 48.86 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.654, perte reelle 48.86 % (gap inclus), EV 1.4331 % — **REFUSE**
      - refuse : cible atteinte seulement 3.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.71 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 52.35 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.61, perte reelle 52.35 % (gap inclus), EV 1.4331 % — **REFUSE**
      - refuse : cible atteinte seulement 3.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.71 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 55.84 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.572, perte reelle 55.84 % (gap inclus), EV 1.4331 % — **REFUSE**
      - refuse : cible atteinte seulement 3.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.71 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 83.825, ATR14 5.851 (6.98 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.371 ATR = 2.59 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.349 % | 83.5324 | 93.05 % | 95.26 % | 96.17 % | 96.66 % | 97.15 % | 98.05 % |
| 0.1 ATR | 0.698 % | 83.2399 | 85.4 % | 90.52 % | 92.33 % | 93.93 % | 94.82 % | 96.41 % |
| 0.15 ATR | 1.047 % | 82.9473 | 77.74 % | 85.48 % | 88.29 % | 90.7 % | 92.68 % | 95.07 % |
| 0.2 ATR | 1.396 % | 82.6548 | 71.3 % | 80.24 % | 84.16 % | 87.46 % | 90.45 % | 93.22 % |
| 0.25 ATR | 1.745 % | 82.3622 | 64.25 % | 74.5 % | 79.52 % | 83.92 % | 87.8 % | 90.86 % |
| 0.35 ATR | 2.443 % | 81.7771 | 52.17 % | 65.62 % | 72.35 % | 78.26 % | 83.74 % | 87.99 % |
| 0.5 ATR | 3.49 % | 80.8995 | 36.76 % | 53.63 % | 61.45 % | 69.06 % | 76.73 % | 82.24 % |
| 0.75 ATR | 5.235 % | 79.4367 | 19.23 % | 36.19 % | 46.32 % | 56.12 % | 65.96 % | 73.1 % |
| 1.0 ATR | 6.98 % | 77.974 | 9.16 % | 23.29 % | 33.2 % | 44.49 % | 55.39 % | 65.5 % |
| 1.25 ATR | 8.725 % | 76.5112 | 4.73 % | 14.62 % | 22.6 % | 34.18 % | 47.66 % | 58.93 % |
| 1.5 ATR | 10.47 % | 75.0485 | 2.42 % | 9.88 % | 16.35 % | 27.3 % | 40.96 % | 53.29 % |
| 2.0 ATR | 13.96 % | 72.123 | 0.4 % | 3.73 % | 7.16 % | 15.37 % | 30.18 % | 43.43 % |
| 2.5 ATR | 17.45 % | 69.1975 | 0.0 % | 1.41 % | 3.73 % | 8.09 % | 21.75 % | 34.29 % |
| 3.0 ATR | 20.94 % | 66.272 | 0.0 % | 0.5 % | 2.12 % | 4.85 % | 15.04 % | 26.28 % |
| 4.0 ATR | 27.92 % | 60.421 | 0.0 % | 0.3 % | 0.61 % | 1.82 % | 6.0 % | 14.48 % |
| 6.0 ATR | 41.88 % | 48.719 | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.32 % | 4.62 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.37 ATR | 0.42 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 0.98 ATR | 1.24 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.62 ATR | 0.81 ATR | 0.97 ATR | 1.09 ATR | 1.49 ATR | 1.90 ATR |
| **3 s.** | 0.31 ATR | 0.69 ATR | 0.78 ATR | 1.00 ATR | 1.19 ATR | 1.35 ATR | 1.84 ATR | 2.31 ATR |
| **5 s.** | 0.40 ATR | 0.88 ATR | 0.99 ATR | 1.29 ATR | 1.60 ATR | 1.81 ATR | 2.37 ATR | 2.98 ATR |
| **10 s.** | 0.54 ATR | 1.17 ATR | 1.35 ATR | 1.87 ATR | 2.31 ATR | 2.63 ATR | 3.56 ATR | 4.43 ATR |
| **20 s.** | 0.70 ATR | 1.67 ATR | 1.92 ATR | 2.58 ATR | 3.11 ATR | 3.53 ATR | 4.91 ATR | 5.92 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.42–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.624–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.235 %, prix 79.4368), p(touche) 36.19 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.775–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.98 %, prix 77.974), p(touche) 33.2 % (en stress 91.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 56.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.989–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.98 %, prix 77.974), p(touche) 44.49 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.349–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.47 %, prix 75.0485), p(touche) 40.96 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.92–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (13.96 %, prix 72.123), p(touche) 43.43 % (en stress 97.96 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (64.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.001 | EV/share : $-0.002 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 29 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.9 | bear 63.0 | side 30.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.443% → cible +3.506% / stop −3.0%, p_fill 87%, n_eff≈93.2) : P(cible|rempli) **21%** · **EV/risk -0.098** (×p_fill ; si rempli -0.34% du capital)
  - **swing** (entrée dip −0.99% → cible +11.702% / stop −7.05%, p_fill 87%, n_eff≈100.0) : P(cible|rempli) **22%** · **EV/risk -0.070** (×p_fill ; si rempli -0.57% du capital)
  - **deep** (entrée dip −1.52% → cible +12.311% / stop −10.632%, p_fill 87%, n_eff≈96.5) : P(cible|rempli) **47%** · **EV/risk +0.088** (×p_fill ; si rempli +1.07% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→79% · +2.0%→52% · +3.0%→34% · +5.0%→18% · +8.0%→6%
- Range intraday médian 4.75% (p90 8.94%) · excursion haute méd. +2.07% / basse méd. −2.15%
- Profil de vol intra : ouverture 3.568% vs midi 0.948% vs clôture 1.079% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 21% · trend ↑0%/↓1% ; spike-down 68% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.134 ; mean-reverting — autocorr -0.057)_ ; drift intra méd. -0.413% ; recovery-V 19%
- **σ réalisé intraday** 3.025% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 60% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 96.1559 (VA 95.5739–96.6651 ; dernier close 95.07)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 27% · rebond 71% · **stop −3.99%** sous le fill (sous le bruit) · cible +2.53% · R/R 0.63 (high win-rate)
- Gaps overnight (n=159) : méd. -0.16% · baisse 53% (gap-down >1% 34% · >2% 19%)
- Excursion ouverture 5min (n=160) : bas méd −0.79% (p90 −2.34%) · haut méd +0.88% · range méd 2.06%
- Excursion ouverture 15min (n=160) : bas méd −1.22% (p90 −2.96%) · haut méd +1.23% · range méd 2.63%
- Excursion ouverture 30min (n=160) : bas méd −1.41% (p90 −3.35%) · haut méd +1.36% · range méd 3.2%
- Excursion ouverture 60min (n=160) : bas méd −1.78% (p90 −3.71%) · haut méd +1.53% · range méd 3.53%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 95.07 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 79% (122/159) · gap 41% · délai 0.0min · rebond 60% (70/122) (MFE +1.4%)
   - −1.0% : fill 30min 58% · séance 70% (107/159) · gap 34% · délai 0.0min · rebond 65% (66/107) (MFE +1.62%)
   - −1.5% : fill 30min 46% · séance 62% (97/159) · gap 25% · délai 1.1min · rebond 55% (54/97) (MFE +1.31%)
   - −2.0% : fill 30min 36% · séance 50% (84/159) · gap 19% · délai 1.6min · rebond 63% (55/84) (MFE +1.3%)
   - −3.0% : fill 30min 24% · séance 35% (61/159) · gap 10% · délai 7.4min · rebond 74% (44/61) (MFE +1.88%)
   - −4.0% : fill 30min 15% · séance 27% (45/159) · gap 3% · délai 11.1min · rebond 71% (32/45) (MFE +2.53%)
   - −5.0% : fill 30min 7% · séance 17% (28/159) · gap 1% · délai 55.8min · rebond 47% (18/28) (MFE +1.02%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.61% (p90 −2.47%) → stop au-delà de −1.76% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −2.3%) → stop au-delà de −1.83% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −2.41%) → stop au-delà de −1.8% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=725 jambes) : jambe baissière méd −1.14% (p90 −2.78%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (72 séances) :
      · −1.0% : fill 91% (68/72) · rebond 57% (36/68)
      · −2.0% : fill 73% (58/72) · rebond 64% (37/58)
      · −3.0% : fill 59% (47/72) · rebond 82% (35/47)
      · −4.0% : fill 47% (36/72) · rebond 78% (28/36)
      · −5.0% : fill 31% (24/72) · rebond 47% (15/24)
   - **flat** (17 séances) :
      · −1.0% : fill 72% (11/17) · rebond 79% (8/11)
      · −2.0% : fill 38% (8/17) · rebond 55% (5/8)
      · −3.0% : fill 15% (3/17) · rebond 0% (0/3)
      · −4.0% : fill 15% (3/17) · rebond 0% (0/3)
      · −5.0% : fill 13% (2/17) · rebond 15% (1/2)
   - **gap-up** (70 séances) :
      · −1.0% : fill 45% (28/70) · rebond 78% (22/28)
      · −2.0% : fill 29% (18/70) · rebond 63% (13/18)
      · −3.0% : fill 13% (11/70) · rebond 56% (9/11)
      · −4.0% : fill 7% (6/70) · rebond 63% (4/6)
      · −5.0% : fill 2% (2/70) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 58% si les 15 1res min sont vertes (73 cas) · 27% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **53min** → P(séance verte=clôture>ouverture) 65% si début vert vs 18% si rouge (base 42% · écart 46 pts) ; prédictivité sature ensuite (plafond brut 228min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **65%** · continue >prix actuel 43% ; creux résiduel méd -1.45% (q20 -2.67%) → **SL/trailing à −2.67%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.32% / q75 +2.53% → **scale +1.32% / runner +2.53%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **18%** (continue à baisser 63%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.8%** (au-delà de la MAE q10 -3.8%), cible rebond +1.47% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.48% .. +3.77%] · haut q95 +4.35% · bas q05 -4.82%
   - 60min (n=160) : retour [-3.67% .. +4.97%] · haut q95 +5.48% · bas q05 -4.85%
   - 2h (n=160) : retour [-4.63% .. +4.96%] · haut q95 +6.62% · bas q05 -5.1%
   - 4h (n=160) : retour [-4.82% .. +5.74%] · haut q95 +7.31% · bas q05 -6.0%
   - 6h (n=160) : retour [-5.77% .. +6.28%] · haut q95 +7.31% · bas q05 -7.11%
   - session (n=160) : retour [-5.56% .. +6.85%] · haut q95 +7.46% · bas q05 -7.12%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.1% des séances sont trend-up (mild 0% / strong 8.1%) · base = 13 séances trend-up (n_eff 8.1)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **34%**. Lecture précoce 30 min : signature présente → 15% vs absente 4% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.88% (p75 1.28% / p90 2.57%) · ~3.72 replis/séance, durée méd 50.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **82%** (reprise méd 20.0 min, n=50)
   - −1.0% → **68%** (reprise méd 26.42 min, n=21)
   - −1.5% → **64%** (reprise méd 29.02 min, n=10)
   - −2.0% → **53%** (reprise méd None min, n=6)
   - −3.0% → **20%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.57%** (p90, défaut prudent ; serré/agressif −1.28%) ; extension open→close méd +6.81% (q75 +7.91% / q95 +11.09%), MFE méd +7.28% / q90 +11.48%
   - Échelle scale-out : +7.28% (33%) / +8.78% (33%) / +11.48% (34%)
- **DÉSARMER** : repli > **−2.57%** depuis le plus-haut = décay → P(retournement) **39%** (préavis méd 256.98 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +11.48% : P(retournement après) 0% (mèche méd 3.29%)
- **CONTEXTE** : la dernière heure tient les gains 79% du temps (retour médian dernière heure +0.47%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.71 · part idiosyncratique 0.29
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-05 — Bank of England — décision de taux (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-05 — Bank of England — décision de taux (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-05 — Bank of England — décision de taux (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 21.7  _(survente)_
- **ADX** : 27.2  _(tendance etablie)_
- **MACD** : hist -1.554  _(pas de croisement recent)_
- **BB** : %B 0.04 · largeur 33.8%
- **ATR** : 5.85 (56.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.074  _(distribution)_
- **Vol ratio** : 0.95  _(volume normal)_
- **Choppiness** : 41.7  _(transition)_
- **MA** : MA20 99.44 · MA50 108.0 · MA200 92.46  _(prix < MA20)_
- **Dist MA** : MA20 -15.7% · MA50 -22.4% · MA200 -9.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (738532 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
