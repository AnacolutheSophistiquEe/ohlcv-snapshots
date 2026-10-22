# IONQ

**Generated** : 2026-10-22T00:24:21.312114+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 6/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · $32.28  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (13 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot $32.28 (+0.4% vs entrée) · entrée $32.14 · stop $31.04 · T1 $34.33 · R/R 1.99  
> ↳ _probas brutes, non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +7.2 % ≠ (strike 33.5 − spot 32.28)/spot = +3.8 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-21 : 32.28 · ATR Wilder 2.62 (8.11 %)_
- **Swing** : plage **29.05 → 27.07** (-9.99 % a -16.15 % sous la cloture, 0.76 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 27.83-28.32 (B). stop INDICATIF 24.19 (-10.63 % sous le bas ; sous le support 25.5-26.33 (- 0,5 ATR)).
- **Deep** : plage **27.07 → 22.7** (-16.15 % a -29.67 % sous la cloture, 1.67 ATR) — touchee 47 % → 15 % du temps en 20 seances ; supports reels dans la plage : 25.5-26.33 (A) ; 22.27-23.49 (B). stop INDICATIF 19.3 (-14.99 % sous le bas ; sous le support 20.61-21.5 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 5.97 ATR sous le plus haut 20 s., RSI(2) 68.3. Limite **30.97** (seance suivante), stop catastrophe 20.49, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 29.99-31.1 (A, -3.66 %) ; 27.83-28.32 (B, -12.27 %) ; 25.5-26.33 (A, -18.43 %) ; 22.27-23.49 (B, -27.25 %) ; 20.61-21.5 (B, -33.4 %) ; 17.88-18.81 (A, -41.73 %)
- Resistances reelles au-dessus : 33.29-34.18 (A, 3.13 %) ; 34.77-36.03 (A, 7.71 %) ; 36.57-37.28 (A, 13.29 %) ; 38.0-38.46 (A, 17.72 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=9.18 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.0 %)** : le gap seul le franchit 0.399 % des séances (5 fois sur 1253).
   - exécution **2.441 pt plus bas** dans le cas TYPIQUE (médiane), 8.894 au p90, **12.859 au pire**
   - perte réelle **13.019 %** en moyenne _(tirée par la queue)_, jusqu'à **21.859 %** — au lieu des 9.0 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.016 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.087 % | p01 -6.632 % | pire -21.859 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4095** [0.3382 ; 0.4838] _(largeur 14.6 pt, n_eff 173.1)_
   - swing : **0.4796** [0.4273 ; 0.5322] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.465** [0.4129 ; 0.5177] _(largeur 10.5 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.84 %** | CVaR **-10.52 %** | vol 6.14 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 10.15 % contre 5.50 % aujourd'hui, rapport 1.85)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -17.92 % vs -19.94 % si l'on extrapolait par √5 _(rapport 0.899 ; < 1 = le √5 surestime)_
- **β de baisse : 2.198** (β de hausse 1.9996, asymétrie 1.0992) vs IWM — 605 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 28.4234 sur atr_based (1.5 ATR, 11.947 %) — p(stop avant cible) 0.4788 [0.43 ; 0.53], R/R 2.727, perte reelle 12.045 % (gap inclus), CVaR 12.884 %, EV 0.223 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.5052 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 12.88 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.18 ATR (stop 4.013 %) — p(stop avant cible) 0.8152 [0.77 ; 0.85], R/R 7.968, perte reelle 4.123 % (gap inclus), EV 0.2403 % — **REFUSE**
      - refuse : cible atteinte seulement 6.2 % du temps (< 15 %) meme a 10 seances : le R/R de 7.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.815, borne haute 0.853 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.18 ATR du spot — compartiment <1, mesure a 47.1 % de casse (IC clusterise [0.438 ; 0.503] sur 1171 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🔴 support a 0.89 ATR (stop 9.651 %) — p(stop avant cible) 0.6004 [0.55 ; 0.65], R/R 3.375, perte reelle 9.734 % (gap inclus), EV 0.2624 % — **REFUSE**
      - refuse : cible atteinte seulement 9.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.600, borne haute 0.651 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.86 ATR du spot — compartiment <1, mesure a 47.1 % de casse (IC clusterise [0.438 ; 0.503] sur 1171 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_based a 1.5 ATR (stop 11.947 %) — p(stop avant cible) 0.4788 [0.43 ; 0.53], R/R 2.727, perte reelle 12.045 % (gap inclus), EV 0.223 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.88 % > budget 12.00 %
   - 🟢 support a 2.49 ATR (stop 22.352 %) — p(stop avant cible) 0.1609 [0.13 ; 0.20], R/R 1.455, perte reelle 22.579 % (gap inclus), EV 0.2689 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.08 % > budget 12.00 %
   - ⚪ atr_grid a 1.75 ATR (stop 13.939 %) — p(stop avant cible) 0.3901 [0.34 ; 0.44], R/R 2.347, perte reelle 13.998 % (gap inclus), EV 0.1301 % — **REFUSE**
      - refuse : cible atteinte seulement 10.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.40 % > budget 12.00 %
   - ⚪ atr_grid a 2.0 ATR (stop 15.93 %) — p(stop avant cible) 0.3153 [0.27 ; 0.37], R/R 2.054, perte reelle 15.997 % (gap inclus), EV 0.0578 % — **REFUSE**
      - refuse : cible atteinte seulement 10.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.35 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 23.895 %) — p(stop avant cible) 0.125 [0.09 ; 0.16], R/R 1.364, perte reelle 24.087 % (gap inclus), EV 0.3184 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.37 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 27.877 %) — p(stop avant cible) 0.0885 [0.06 ; 0.12], R/R 1.176, perte reelle 27.934 % (gap inclus), EV 0.0897 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.98 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 31.86 %) — p(stop avant cible) 0.041 [0.02 ; 0.07], R/R 1.029, perte reelle 31.939 % (gap inclus), EV 0.0265 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.42 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 35.842 %) — p(stop avant cible) 0.0138 [0.01 ; 0.03], R/R 0.914, perte reelle 35.943 % (gap inclus), EV 0.1393 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.92 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 39.825 %) — p(stop avant cible) 0.0059 [0.00 ; 0.02], R/R 0.825, perte reelle 39.825 % (gap inclus), EV 0.1633 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.85 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 43.807 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.75, perte reelle 43.807 % (gap inclus), EV 0.1933 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.52 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 47.789 %) — p(stop avant cible) 0.0005 [0.00 ; 0.01], R/R 0.687, perte reelle 47.789 % (gap inclus), EV 0.209 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.38 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 51.772 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.635, perte reelle 51.772 % (gap inclus), EV 0.2236 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.20 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 55.754 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.589, perte reelle 55.754 % (gap inclus), EV 0.2236 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.20 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 59.737 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.55, perte reelle 59.737 % (gap inclus), EV 0.2236 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.20 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 63.719 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.516, perte reelle 63.719 % (gap inclus), EV 0.2236 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.20 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 32.28, ATR14 2.5711 (7.965 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.382 ATR = 3.043 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.398 % | 32.1514 | 93.86 % | 95.56 % | 96.27 % | 97.57 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.796 % | 32.0229 | 86.3 % | 91.33 % | 92.43 % | 94.64 % | 95.83 % | 96.82 % |
| 0.15 ATR | 1.195 % | 31.8943 | 79.05 % | 86.49 % | 88.5 % | 91.61 % | 93.6 % | 95.59 % |
| 0.2 ATR | 1.593 % | 31.7658 | 71.4 % | 80.75 % | 84.36 % | 88.47 % | 90.85 % | 93.43 % |
| 0.25 ATR | 1.991 % | 31.6372 | 65.36 % | 76.61 % | 80.83 % | 85.95 % | 88.82 % | 91.89 % |
| 0.35 ATR | 2.788 % | 31.3801 | 53.17 % | 67.64 % | 74.27 % | 79.47 % | 84.15 % | 88.3 % |
| 0.5 ATR | 3.982 % | 30.9945 | 38.17 % | 54.74 % | 62.36 % | 71.18 % | 78.66 % | 84.39 % |
| 0.75 ATR | 5.974 % | 30.3517 | 22.46 % | 39.62 % | 48.64 % | 59.05 % | 69.31 % | 76.8 % |
| 1.0 ATR | 7.965 % | 29.7089 | 10.17 % | 25.0 % | 35.12 % | 46.31 % | 58.33 % | 68.17 % |
| 1.25 ATR | 9.956 % | 29.0662 | 3.83 % | 14.42 % | 24.22 % | 35.09 % | 50.51 % | 61.81 % |
| 1.5 ATR | 11.947 % | 28.4234 | 1.11 % | 7.16 % | 15.84 % | 25.78 % | 41.46 % | 56.16 % |
| 2.0 ATR | 15.93 % | 27.1379 | 0.1 % | 1.92 % | 5.25 % | 14.56 % | 28.46 % | 45.28 % |
| 2.5 ATR | 19.912 % | 25.8523 | 0.0 % | 0.2 % | 1.31 % | 6.07 % | 18.39 % | 34.39 % |
| 3.0 ATR | 23.895 % | 24.5668 | 0.0 % | 0.1 % | 0.4 % | 2.83 % | 11.69 % | 26.08 % |
| 4.0 ATR | 31.86 % | 21.9957 | 0.0 % | 0.1 % | 0.1 % | 0.2 % | 3.35 % | 10.88 % |
| 6.0 ATR | 47.789 % | 16.8536 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.1 % | 1.33 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.58 ATR | 0.71 ATR | 0.80 ATR | 1.01 ATR | 1.20 ATR |
| **2 s.** | 0.27 ATR | 0.58 ATR | 0.66 ATR | 0.86 ATR | 1.00 ATR | 1.12 ATR | 1.40 ATR | 1.71 ATR |
| **3 s.** | 0.34 ATR | 0.72 ATR | 0.82 ATR | 1.05 ATR | 1.23 ATR | 1.38 ATR | 1.78 ATR | 2.03 ATR |
| **5 s.** | 0.43 ATR | 0.93 ATR | 1.03 ATR | 1.31 ATR | 1.53 ATR | 1.76 ATR | 2.27 ATR | 2.67 ATR |
| **10 s.** | 0.60 ATR | 1.26 ATR | 1.40 ATR | 1.82 ATR | 2.17 ATR | 2.42 ATR | 3.20 ATR | 3.80 ATR |
| **20 s.** | 0.80 ATR | 1.78 ATR | 2.01 ATR | 2.58 ATR | 3.07 ATR | 3.40 ATR | 4.18 ATR | 5.23 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.432–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.661–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.974 %, prix 30.3516), p(touche) 39.62 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.817–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.965 %, prix 29.7089), p(touche) 35.12 % (en stress 92.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.029–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (9.956 %, prix 29.0662), p(touche) 35.09 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 21.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.402–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (11.947 %, prix 28.4235), p(touche) 41.46 % (en stress 97.98 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.013–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (69.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 10.8 | bear 67.3 | side 21.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.447% → cible +6.836% / stop −3.418%, p_fill 95%, n_eff≈101.7) : P(cible|rempli) **18%** · **EV/risk +0.023** (×p_fill ; si rempli +0.08% du capital)
  - **swing** (entrée dip −0.985% → cible +16.19% / stop −8.095%, p_fill 88%, n_eff≈103.0) : P(cible|rempli) **23%** · **EV/risk +0.017** (×p_fill ; si rempli +0.15% du capital)
  - **deep** (entrée dip −1.442% → cible +16.73% / stop −12.123%, p_fill 87%, n_eff≈97.6) : P(cible|rempli) **34%** · **EV/risk -0.092** (×p_fill ; si rempli -1.28% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→87% · +1.0%→80% · +2.0%→64% · +3.0%→54% · +5.0%→28% · +8.0%→13%
- Range intraday médian 7.05% (p90 11.57%) · excursion haute méd. +3.57% / basse méd. −2.49%
- Profil de vol intra : ouverture 4.841% vs midi 1.378% vs clôture 1.552% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 22% · trend ↑0%/↓0% ; spike-down 62% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.122 ; neutre — autocorr 0.011)_ ; drift intra méd. -0.232% ; recovery-V 26%
- **σ réalisé intraday** 4.05% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 57% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 44.6406 (VA 44.2714–45.1154 ; dernier close 43.77)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 25% · rebond 78% · **stop −4.38%** sous le fill (sous le bruit) · cible +2.22% · R/R 0.51 (high win-rate)
- Gaps overnight (n=159) : méd. 0.03% · baisse 49% (gap-down >1% 34% · >2% 21%)
- Excursion ouverture 5min (n=160) : bas méd −1.0% (p90 −2.73%) · haut méd +1.28% · range méd 2.57%
- Excursion ouverture 15min (n=160) : bas méd −1.18% (p90 −3.76%) · haut méd +1.47% · range méd 3.38%
- Excursion ouverture 30min (n=160) : bas méd −1.31% (p90 −4.62%) · haut méd +1.81% · range méd 4.16%
- Excursion ouverture 60min (n=160) : bas méd −1.57% (p90 −5.28%) · haut méd +1.87% · range méd 4.67%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 43.77 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 76% (126/159) · gap 43% · délai 0.0min · rebond 61% (83/126) (MFE +1.81%)
   - −1.0% : fill 30min 60% · séance 70% (119/159) · gap 34% · délai 0.0min · rebond 67% (85/119) (MFE +1.91%)
   - −1.5% : fill 30min 53% · séance 65% (112/159) · gap 30% · délai 0.0min · rebond 70% (78/112) (MFE +2.06%)
   - −2.0% : fill 30min 46% · séance 54% (100/159) · gap 21% · délai 0.0min · rebond 69% (70/100) (MFE +2.17%)
   - −3.0% : fill 30min 37% · séance 43% (81/159) · gap 10% · délai 4.1min · rebond 70% (59/81) (MFE +2.38%)
   - −4.0% : fill 30min 22% · séance 33% (64/159) · gap 4% · délai 15.3min · rebond 69% (48/64) (MFE +2.23%)
   - −5.0% : fill 30min 11% · séance 25% (50/159) · gap 1% · délai 32.0min · rebond 78% (41/50) (MFE +2.22%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.75% (p90 −2.62%) → stop au-delà de −1.83% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.76% (p90 −2.65%) → stop au-delà de −1.69% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.68% (p90 −2.35%) → stop au-delà de −1.31% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1047 jambes) : jambe baissière méd −1.26% (p90 −2.97%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (80 séances) :
      · −1.0% : fill 100% (80/80) · rebond 69% (56/80)
      · −2.0% : fill 87% (73/80) · rebond 75% (54/73)
      · −3.0% : fill 72% (61/80) · rebond 72% (44/61)
      · −4.0% : fill 54% (47/80) · rebond 67% (34/47)
      · −5.0% : fill 38% (37/80) · rebond 70% (28/37)
   - **flat** (15 séances) :
      · −1.0% : fill 62% (10/15) · rebond 84% (9/10)
      · −2.0% : fill 43% (8/15) · rebond 90% (6/8)
      · −3.0% : fill 27% (5/15) · rebond 64% (4/5)
      · −4.0% : fill 23% (4/15) · rebond 57% (3/4)
      · −5.0% : fill 16% (3/15) · rebond 100% (3/3)
   - **gap-up** (64 séances) :
      · −1.0% : fill 41% (29/64) · rebond 55% (20/29)
      · −2.0% : fill 22% (19/64) · rebond 31% (10/19)
      · −3.0% : fill 15% (15/64) · rebond 60% (11/15)
      · −4.0% : fill 14% (13/64) · rebond 84% (11/13)
      · −5.0% : fill 12% (10/64) · rebond 100% (10/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 59% si les 15 1res min sont vertes (90 cas) · 26% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **56min** → P(séance verte=clôture>ouverture) 66% si début vert vs 19% si rouge (base 46% · écart 47 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=86) : tient le vert **66%** · continue >prix actuel 38% ; creux résiduel méd -1.76% (q20 -4.14%) → **SL/trailing à −4.14%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.64% / q75 +3.31% → **scale +1.64% / runner +3.31%**, sortie à la clôture
  - **si ROUGE au coude** (n=74) : edge inversé — récupère vert seulement **19%** (continue à baisser 59%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.23%** (au-delà de la MAE q10 -4.23%), cible rebond +1.94% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.23% .. +5.46%] · haut q95 +7.35% · bas q05 -5.49%
   - 60min (n=160) : retour [-5.25% .. +5.86%] · haut q95 +7.69% · bas q05 -6.74%
   - 2h (n=160) : retour [-6.37% .. +5.93%] · haut q95 +8.07% · bas q05 -7.06%
   - 4h (n=160) : retour [-6.75% .. +6.86%] · haut q95 +8.75% · bas q05 -7.93%
   - 6h (n=160) : retour [-6.62% .. +7.19%] · haut q95 +9.75% · bas q05 -7.92%
   - session (n=160) : retour [-6.36% .. +8.14%] · haut q95 +9.8% · bas q05 -8.19%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 7.5% des séances sont trend-up (mild 0% / strong 7.5%) · base = 12 séances trend-up (n_eff 7.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **35%**. Lecture précoce 30 min : signature présente → 13% vs absente 5% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.3% (p75 2.44% / p90 3.18%) · ~4.0 replis/séance, durée méd 70.31 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 30.0 min, n=48)
   - −1.0% → **77%** (reprise méd 34.75 min, n=35)
   - −1.5% → **67%** (reprise méd 44.94 min, n=18)
   - −2.0% → **61%** (reprise méd 64.1 min, n=13)
   - −3.0% → **74%** (reprise méd 175.76 min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−3.18%** (p90, défaut prudent ; serré/agressif −2.44%) ; extension open→close méd +8.16% (q75 +8.39% / q95 +13.57%), MFE méd +9.48% / q90 +12.4%
   - Échelle scale-out : +9.48% (33%) / +10.45% (33%) / +12.4% (34%)
- **DÉSARMER** : repli > **−3.18%** depuis le plus-haut = décay → P(retournement) **26%** (préavis méd 167.77 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.4% : P(retournement après) 0% (mèche méd 2.07%)
- **CONTEXTE** : la dernière heure tient les gains 70% du temps (retour médian dernière heure +0.1%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.55 · part idiosyncratique 0.46
**Short/Insider** : SI —% | insider — | verdict sell_bias_modere
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 23.5  _(survente)_
- **ADX** : 26.8  _(tendance etablie)_
- **MACD** : hist -1.006  _(pas de croisement recent)_
- **BB** : %B 0.2 · largeur 56.8%
- **ATR** : 2.57 (14.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.267  _(distribution)_
- **Vol ratio** : 0.54  _(volume atone)_
- **Choppiness** : 32.2  _(marche directionnel)_
- **MA** : MA20 38.99 · MA50 40.04 · MA200 42.69  _(prix < MA20)_
- **Dist MA** : MA20 -17.2% · MA50 -19.4% · MA200 -24.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (763679 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
