# CEG

**Generated** : 2026-10-20T00:26:40.938619+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $263.08  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 3/125 fenêtres (p_fill pondéré 2 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot $263.08 (+7.0% vs entrée) · entrée $245.98 · stop $226.30 · T1 $254.53 · R/R 0.43  
> ↳ _probas brutes, non calibrées · n=0_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +5.0 % ≠ (strike 285.0 − spot 263.08)/spot = +8.3 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-19 : 263.08 · ATR Wilder 13.65 (5.19 %)_
- **Swing** : plage **244.85 → 234.9** (-6.93 % a -10.71 % sous la cloture, 0.73 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 240.14-246.18 (A) ; 232.79-236.2 (A). stop INDICATIF 217.91 (-7.24 % sous le bas ; sous le support 224.73-229.27 (- 0,5 ATR)).
- **Deep** : plage **234.9 → 209.14** (-10.71 % a -20.5 % sous la cloture, 1.89 ATR) — touchee 46 % → 15 % du temps en 20 seances ; supports reels dans la plage : 232.79-236.2 (A) ; 224.73-229.27 (A) ; 216.13-228.28 (B). stop INDICATIF 193.95 (-7.26 % sous le bas ; sous le support 200.78-206.79 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (COMBO) : 3.42 ATR sous le plus haut 20 s., RSI(2) 2.9. Limite **256.26** (seance suivante), stop catastrophe 201.67, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 247.2-250.55 (A, -4.76 %) ; 240.14-246.18 (A, -6.42 %) ; 232.79-236.2 (A, -10.22 %) ; 224.73-229.27 (A, -12.85 %) ; 216.13-228.28 (B, -13.23 %) ; 200.78-206.79 (B, -21.4 %)
- Resistances reelles au-dessus : 275.99-282.34 (A, 4.91 %) ; 284.07-286.56 (A, 7.98 %) ; 291.53-294.09 (A, 10.81 %) ; 299.33-305.8 (A, 13.78 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.02 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (19.5 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1191).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 19.5 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.861 % | p01 -4.432 % | pire -15.824 % _(sur 1191 séances)_
- **P(stop avant cible)** _(source : daily, 1192 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0088** [0.0014 ; 0.032] _(largeur 3.1 pt, n_eff 173.1)_
   - swing : **0.2256** [0.1839 ; 0.2718] _(largeur 8.8 pt, n_eff 345.5)_
   - deep : **0.1997** [0.1602 ; 0.2443] _(largeur 8.4 pt, n_eff 345.5)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-4.32 %** | CVaR **-6.27 %** | vol 2.85 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 4.84 % contre 2.91 % aujourd'hui, rapport 1.66)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.08 % vs -9.7 % si l'on extrapolait par √5 _(rapport 1.039 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1742** (β de hausse 1.189, asymétrie 0.9876) vs SPY — 551 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 238.6503 sur grid_snapped (1.13 ATR, 9.286 %) — p(stop avant cible) 0.2989 [0.25 ; 0.35], R/R 4.43, perte reelle 9.404 % (gap inclus), CVaR 9.993 %, EV 0.0464 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.99 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 1.13 ATR (stop 10.664 %) — p(stop avant cible) 0.2446 [0.20 ; 0.29], R/R 3.868, perte reelle 10.772 % (gap inclus), EV 0.0395 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 0.25 ATR (stop 1.625 %) — p(stop avant cible) 0.8534 [0.81 ; 0.89], R/R 23.962, perte reelle 1.739 % (gap inclus), EV -0.135 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 23.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.853, borne haute 0.888 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 0.1 % x 41.66 % + P(rien) 14.6 % x 9.00 % ne couvrent pas P(stop) 85.3 % x 1.74 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+41.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.5 ATR (stop 3.25 %) — p(stop avant cible) 0.7073 [0.66 ; 0.75], R/R 12.139, perte reelle 3.432 % (gap inclus), EV -0.133 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 12.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.707, borne haute 0.753 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 0.1 % x 41.66 % + P(rien) 29.1 % x 7.67 % ne couvrent pas P(stop) 70.7 % x 3.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 4.875 %) — p(stop avant cible) 0.5857 [0.53 ; 0.64], R/R 8.281, perte reelle 5.031 % (gap inclus), EV -0.3444 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 8.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.586, borne haute 0.637 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.34 %) : P(cible) 0.1 % x 41.66 % + P(rien) 41.3 % x 6.15 % ne couvrent pas P(stop) 58.6 % x 5.03 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 1.13 ATR (stop 9.286 %) — p(stop avant cible) 0.2989 [0.25 ; 0.35], R/R 4.43, perte reelle 9.404 % (gap inclus), EV 0.0464 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.0 ATR (stop 12.999 %) — p(stop avant cible) 0.1735 [0.14 ; 0.22], R/R 3.182, perte reelle 13.092 % (gap inclus), EV 0.0511 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.32 % > budget 12.00 %
   - ⚪ atr_grid a 2.25 ATR (stop 14.624 %) — p(stop avant cible) 0.12 [0.09 ; 0.16], R/R 2.841, perte reelle 14.665 % (gap inclus), EV 0.1307 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.72 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 16.249 %) — p(stop avant cible) 0.0648 [0.04 ; 0.09], R/R 2.557, perte reelle 16.296 % (gap inclus), EV 0.2218 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.31 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 17.874 %) — p(stop avant cible) 0.0433 [0.03 ; 0.07], R/R 2.306, perte reelle 18.07 % (gap inclus), EV 0.2322 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.83 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 19.499 %) — p(stop avant cible) 0.0247 [0.01 ; 0.05], R/R 2.124, perte reelle 19.619 % (gap inclus), EV 0.3022 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.77 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 22.749 %) — p(stop avant cible) 0.0085 [0.00 ; 0.02], R/R 1.823, perte reelle 22.849 % (gap inclus), EV 0.3737 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.36 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 25.999 %) — p(stop avant cible) 0.0063 [0.00 ; 0.02], R/R 1.602, perte reelle 25.999 % (gap inclus), EV 0.389 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.41 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 29.249 %) — p(stop avant cible) 0.0028 [0.00 ; 0.01], R/R 1.416, perte reelle 29.413 % (gap inclus), EV 0.3898 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.41 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 32.499 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 1.282, perte reelle 32.499 % (gap inclus), EV 0.3935 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.29 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 35.748 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.165, perte reelle 35.748 % (gap inclus), EV 0.3948 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.29 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 38.998 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.068, perte reelle 38.998 % (gap inclus), EV 0.3948 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.29 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 42.248 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.986, perte reelle 42.248 % (gap inclus), EV 0.3948 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.29 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 45.498 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.916, perte reelle 45.498 % (gap inclus), EV 0.3948 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.29 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 48.748 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.855, perte reelle 48.748 % (gap inclus), EV 0.3948 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.29 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 51.998 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.801, perte reelle 51.998 % (gap inclus), EV 0.3948 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.29 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 263.08, ATR14 17.0994 (6.5 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.389 ATR = 2.528 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.325 % | 262.225 | 91.62 % | 94.62 % | 95.59 % | 96.66 % | 97.61 % | 98.03 % |
| 0.1 ATR | 0.65 % | 261.37 | 85.5 % | 90.43 % | 92.47 % | 94.07 % | 95.66 % | 96.82 % |
| 0.15 ATR | 0.975 % | 260.5151 | 79.05 % | 86.24 % | 88.48 % | 90.61 % | 93.82 % | 95.5 % |
| 0.2 ATR | 1.3 % | 259.6601 | 72.07 % | 80.86 % | 84.07 % | 86.73 % | 91.32 % | 94.19 % |
| 0.25 ATR | 1.625 % | 258.8051 | 65.31 % | 75.38 % | 79.33 % | 83.06 % | 88.61 % | 92.21 % |
| 0.35 ATR | 2.275 % | 257.0952 | 53.92 % | 66.02 % | 71.58 % | 76.81 % | 84.16 % | 88.71 % |
| 0.5 ATR | 3.25 % | 254.5303 | 38.78 % | 52.9 % | 59.63 % | 66.45 % | 77.01 % | 83.0 % |
| 0.75 ATR | 4.875 % | 250.2554 | 20.3 % | 36.67 % | 45.32 % | 53.51 % | 66.7 % | 76.1 % |
| 1.0 ATR | 6.5 % | 245.9806 | 11.28 % | 24.09 % | 33.37 % | 43.47 % | 57.7 % | 69.74 % |
| 1.25 ATR | 8.125 % | 241.7057 | 5.8 % | 16.13 % | 24.43 % | 35.71 % | 51.41 % | 63.6 % |
| 1.5 ATR | 9.75 % | 237.4308 | 2.79 % | 10.75 % | 17.44 % | 28.91 % | 44.36 % | 57.68 % |
| 2.0 ATR | 12.999 % | 228.8811 | 0.86 % | 4.3 % | 9.15 % | 17.8 % | 31.13 % | 46.38 % |
| 2.5 ATR | 16.249 % | 220.3314 | 0.43 % | 2.26 % | 4.74 % | 10.9 % | 21.04 % | 36.51 % |
| 3.0 ATR | 19.499 % | 211.7817 | 0.0 % | 1.08 % | 2.8 % | 6.9 % | 15.51 % | 28.62 % |
| 4.0 ATR | 25.999 % | 194.6823 | 0.0 % | 0.22 % | 0.86 % | 2.7 % | 7.05 % | 14.25 % |
| 6.0 ATR | 38.998 % | 160.4834 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.76 % | 2.74 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.39 ATR | 0.44 ATR | 0.58 ATR | 0.69 ATR | 0.76 ATR | 1.06 ATR | 1.32 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.62 ATR | 0.82 ATR | 0.98 ATR | 1.13 ATR | 1.56 ATR | 1.95 ATR |
| **3 s.** | 0.31 ATR | 0.67 ATR | 0.76 ATR | 1.01 ATR | 1.23 ATR | 1.41 ATR | 1.95 ATR | 2.47 ATR |
| **5 s.** | 0.38 ATR | 0.84 ATR | 0.96 ATR | 1.35 ATR | 1.68 ATR | 1.90 ATR | 2.61 ATR | 3.45 ATR |
| **10 s.** | 0.55 ATR | 1.30 ATR | 1.48 ATR | 1.93 ATR | 2.30 ATR | 2.59 ATR | 3.65 ATR | 4.65 ATR |
| **20 s.** | 0.79 ATR | 1.84 ATR | 2.07 ATR | 2.72 ATR | 3.25 ATR | 3.60 ATR | 4.74 ATR | 5.61 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.438–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.25 %, prix 254.5299), p(touche) 38.78 % (en stress 81.91 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.622–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.875 %, prix 250.2548), p(touche) 36.67 % (en stress 88.17 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.757–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.5 %, prix 245.9798), p(touche) 33.37 % (en stress 95.7 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.962–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.5 %, prix 245.9798), p(touche) 43.47 % (en stress 96.77 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.477–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.75 %, prix 237.4297), p(touche) 44.36 % (en stress 98.92 %)  ✅ optimum identifie (71.4 % des re-echantillons)
- **20 seance(s)** : plage utile 2.07–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (16.249 %, prix 220.3321), p(touche) 36.51 % (en stress 95.65 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (87.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 68.1 | side 26.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=3, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→61% · +2.0%→33% · +3.0%→18% · +5.0%→4% · +8.0%→0%
- Range intraday médian 3.35% (p90 5.52%) · excursion haute méd. +1.42% / basse méd. −1.56%
- Profil de vol intra : ouverture 2.454% vs midi 0.669% vs clôture 0.758% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑1%/↓0% ; spike-down 51% · recovery-V 15%)_
- **Régime intraday** : **chop** _(efficiency 0.116 ; neutre — autocorr 0.022)_ ; drift intra méd. -0.452% ; recovery-V 16%
- **σ réalisé intraday** 2.399% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 40% / bas 68% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 254.8755 (VA 253.3035–256.4475 ; dernier close 257.55)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 37% · rebond 57% · **stop −2.7%** sous le fill (sous le bruit) · cible +1.1% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.47% · baisse 38% (gap-down >1% 10% · >2% 3%)
- Excursion ouverture 5min (n=160) : bas méd −0.61% (p90 −1.58%) · haut méd +0.77% · range méd 1.41%
- Excursion ouverture 15min (n=160) : bas méd −0.79% (p90 −2.27%) · haut méd +0.93% · range méd 1.85%
- Excursion ouverture 30min (n=160) : bas méd −0.95% (p90 −2.61%) · haut méd +1.01% · range méd 2.12%
- Excursion ouverture 60min (n=160) : bas méd −1.14% (p90 −3.48%) · haut méd +1.13% · range méd 2.52%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 257.49 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 51% · séance 66% (103/159) · gap 26% · délai 1.3min · rebond 43% (50/103) (MFE +0.8%)
   - −1.0% : fill 30min 38% · séance 53% (87/159) · gap 10% · délai 2.5min · rebond 43% (40/87) (MFE +0.95%)
   - −1.5% : fill 30min 32% · séance 45% (72/159) · gap 6% · délai 10.5min · rebond 52% (36/72) (MFE +1.02%)
   - −2.0% : fill 30min 25% · séance 37% (59/159) · gap 3% · délai 21.2min · rebond 57% (33/59) (MFE +1.1%)
   - −3.0% : fill 30min 9% · séance 18% (32/159) · gap 2% · délai 31.6min · rebond 45% (14/32) (MFE +0.78%)
   - −4.0% : fill 30min 6% · séance 9% (18/159) · gap 1% · délai 9.3min · rebond 42% (10/18) (MFE +0.76%)
   - −5.0% : fill 30min 4% · séance 6% (11/159) · gap 0% · délai 17.8min · rebond 70% (8/11) (MFE +1.46%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.25% (p90 −1.1%) → stop au-delà de −0.8% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.32% (p90 −1.17%) → stop au-delà de −0.91% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.56% (p90 −2.23%) → stop au-delà de −1.08% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=464 jambes) : jambe baissière méd −1.08% (p90 −2.55%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (43 séances) :
      · −1.0% : fill 91% (40/43) · rebond 45% (21/40)
      · −2.0% : fill 80% (33/43) · rebond 57% (18/33)
      · −3.0% : fill 36% (18/43) · rebond 29% (6/18)
      · −4.0% : fill 28% (14/43) · rebond 39% (7/14)
      · −5.0% : fill 20% (10/43) · rebond 69% (7/10)
   - **flat** (27 séances) :
      · −1.0% : fill 47% (18/27) · rebond 11% (4/18)
      · −2.0% : fill 30% (11/27) · rebond 47% (6/11)
      · −3.0% : fill 13% (6/27) · rebond 24% (2/6)
      · −4.0% : fill 5% (3/27) · rebond 43% (2/3)
      · −5.0% : fill 1% (1/27) · rebond 100% (1/1)
   - **gap-up** (89 séances) :
      · −1.0% : fill 34% (29/89) · rebond 52% (15/29)
      · −2.0% : fill 16% (15/89) · rebond 61% (9/15)
      · −3.0% : fill 9% (8/89) · rebond 88% (6/8)
      · −4.0% : fill 1% (1/89) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/89) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 59% si les 15 1res min sont vertes (86 cas) · 30% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:31** → P(séance verte=clôture>ouverture) 85% si début vert vs 8% si rouge (base 44% · écart 77 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=83) : tient le vert **85%** · continue >prix actuel 57% ; creux résiduel méd -0.88% (q20 -1.57%) → **SL/trailing à −1.57%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.8% / q75 +1.26% → **scale +0.8% / runner +1.26%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **8%** (continue à baisser 66%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.22%** (au-delà de la MAE q10 -2.22%), cible rebond +0.94% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.58% .. +2.04%] · haut q95 +3.04% · bas q05 -4.75%
   - 60min (n=160) : retour [-3.48% .. +2.54%] · haut q95 +3.33% · bas q05 -4.99%
   - 2h (n=160) : retour [-3.71% .. +2.98%] · haut q95 +3.95% · bas q05 -5.37%
   - 4h (n=160) : retour [-3.72% .. +3.29%] · haut q95 +4.1% · bas q05 -5.37%
   - 6h (n=160) : retour [-3.86% .. +3.44%] · haut q95 +4.48% · bas q05 -5.37%
   - session (n=160) : retour [-3.61% .. +3.56%] · haut q95 +4.53% · bas q05 -5.47%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 4.4% / strong 2.5%) · base = 11 séances trend-up (n_eff 7.7)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **41%**. Lecture précoce 30 min : signature présente → 16% vs absente 4% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.07% (p75 1.89% / p90 2.36%) · ~1.0 replis/séance, durée méd 144.56 min. P(nouveau plus-haut après repli) :
   - −0.5% → **69%** (reprise méd 24.3 min, n=22)
   - −1.0% → **69%** (reprise méd 179.47 min, n=11)
   - −1.5% → **48%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.36%** (p90, défaut prudent ; serré/agressif −1.89%) ; extension open→close méd +3.62% (q75 +4.82% / q95 +6.2%), MFE méd +4.65% / q90 +5.84%
   - Échelle scale-out : +4.65% (33%) / +5.3% (33%) / +5.84% (34%)
- **DÉSARMER** : repli > **−2.36%** depuis le plus-haut = décay → P(retournement) **100%** (préavis méd 280.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.84% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 96% du temps (retour médian dernière heure +0.48%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.48 · part idiosyncratique 0.52
**Short/Insider** : SI —% | insider — | verdict buy_bias_strong
**Options** : neutral_cautious


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 49.4  _(neutre)_
- **ADX** : 18.8  _(pas de tendance nette)_
- **MACD** : hist -1.18  _(bearish_recent)_
- **BB** : %B 0.33 · largeur 23.2%
- **ATR** : 17.1 (91.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.035  _(neutre)_
- **Vol ratio** : 0.77  _(volume normal)_
- **Choppiness** : 50.8  _(transition)_
- **MA** : MA20 273.85 · MA50 275.5 · MA200 283.12  _(prix < MA20)_
- **Dist MA** : MA20 -3.9% · MA50 -4.5% · MA200 -7.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (741663 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
