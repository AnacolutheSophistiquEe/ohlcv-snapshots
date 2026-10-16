# MSTR

**Generated** : 2026-10-16T22:01:34.662802+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $136.83  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (10 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot $136.83 (+0.4% vs entrée) · entrée $136.30 · stop $131.53 · T1 $141.25 · R/R 1.04  
> ↳ ¼-Kelly 0.003 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.5% cohérent avec le bruit 5 s (EV-optimal ≈ −3.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -47 % hors [0,100] (R² max 0.94). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-16 : 136.83 · ATR Wilder 9.73 (7.11 %)_
- **Swing** : plage **125.38 → 116.88** (-8.36 % a -14.58 % sous la cloture, 0.87 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 123.33-127.8 (A) ; 118.4-123.01 (A) ; 113.2-117.85 (B). stop INDICATIF 107.15 (-8.32 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- **Deep** : plage **116.88 → 94.59** (-14.58 % a -30.87 % sous la cloture, 2.29 ATR) — touchee 45 % → 15 % du temps en 20 seances ; supports reels dans la plage : 113.2-117.85 (B) ; 100.05-104.78 (B). stop INDICATIF 84.35 (-10.83 % sous le bas ; sous le support 89.21-91.67 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (3.53 ATR sous le plus haut 20 s., RSI(2) 19.6 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 128.51-132.76 (B, -2.97 %) ; 123.33-127.8 (A, -6.6 %) ; 118.4-123.01 (A, -10.1 %) ; 113.2-117.85 (B, -13.87 %) ; 100.05-104.78 (B, -23.42 %) ; 89.21-91.67 (A, -33.0 %)
- Resistances reelles au-dessus : 144.92-149.75 (A, 5.91 %) ; 150.77-155.61 (A, 10.18 %) ; 156.01-156.11 (B, 14.02 %) ; 162.93-166.01 (A, 19.07 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=10.69 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.91 %)** : le gap seul le franchit 0.957 % des séances (12 fois sur 1254).
   - exécution **2.266 pt plus bas** dans le cas TYPIQUE (médiane), 17.498 au p90, **19.462 au pire**
   - perte réelle **12.861 %** en moyenne _(tirée par la queue)_, jusqu'à **27.372 %** — au lieu des 7.91 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0474 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 12 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.344 % | p01 -7.774 % | pire -27.372 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2796** [0.2168 ; 0.3497] _(largeur 13.3 pt, n_eff 173.1)_
   - swing : **0.4157** [0.3646 ; 0.4682] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.3426** [0.294 ; 0.3938] _(largeur 10.0 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-7.66 %** | CVaR **-10.07 %** | vol 5.38 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 8.77 % contre 5.27 % aujourd'hui, rapport 1.66)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.99 % vs -17.76 % si l'on extrapolait par √5 _(rapport 0.957 ; < 1 = le √5 surestime)_
- **β de baisse : 2.3578** (β de hausse 1.8276, asymétrie 1.2901) vs IWM — 606 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 124.4595 sur atr_grid (1.25 ATR, 9.041 %) — p(stop avant cible) 0.4636 [0.41 ; 0.52], R/R 2.912, perte reelle 9.18 % (gap inclus), CVaR 10.3 %, EV 0.7789 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.26 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 11.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 11 des 11 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 47.7 % de la queue et il ne reste que -683.37 EUR a partager. Prix du risque -0.347 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.06 ATR (stop 2.746 %) — p(stop avant cible) 0.8566 [0.82 ; 0.89], R/R 9.448, perte reelle 2.829 % (gap inclus), EV -0.4922 % — **REFUSE**
      - refuse : cible atteinte seulement 4.0 % du temps (< 15 %) meme a 10 seances : le R/R de 9.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.857, borne haute 0.890 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.06 ATR du spot — compartiment <1, mesure a 49.8 % de casse (IC clusterise [0.466 ; 0.530] sur 1220 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.49 %) : P(cible) 4.0 % x 26.73 % + P(rien) 10.3 % x 8.36 % ne couvrent pas P(stop) 85.7 % x 2.83 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_based a 1.5 ATR (stop 10.849 %) — p(stop avant cible) 0.3599 [0.31 ; 0.41], R/R 2.44, perte reelle 10.958 % (gap inclus), EV 1.1551 % — **REFUSE**
      - refuse : cible atteinte seulement 11.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 2.06 ATR (stop 17.253 %) — p(stop avant cible) 0.185 [0.15 ; 0.23], R/R 1.525, perte reelle 17.531 % (gap inclus), EV 0.6624 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.28 % > budget 12.00 %
   - 🟢 support a 3.3 ATR (stop 26.191 %) — p(stop avant cible) 0.0686 [0.05 ; 0.10], R/R 1.007, perte reelle 26.558 % (gap inclus), EV 0.4839 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.70 % > budget 12.00 %
   - ⚪ atr_grid a 0.75 ATR (stop 5.424 %) — p(stop avant cible) 0.6746 [0.62 ; 0.72], R/R 4.779, perte reelle 5.593 % (gap inclus), EV 0.2188 % — **REFUSE**
      - refuse : cible atteinte seulement 8.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.675, borne haute 0.722 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 7.233 %) — p(stop avant cible) 0.5538 [0.50 ; 0.61], R/R 3.602, perte reelle 7.421 % (gap inclus), EV 0.8437 % — **REFUSE**
      - refuse : cible atteinte seulement 11.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.554, borne haute 0.606 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.25 ATR (stop 9.041 %) — p(stop avant cible) 0.4636 [0.41 ; 0.52], R/R 2.912, perte reelle 9.18 % (gap inclus), EV 0.7789 % — **REFUSE**
      - refuse : cible atteinte seulement 11.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.75 ATR (stop 12.657 %) — p(stop avant cible) 0.3146 [0.27 ; 0.36], R/R 2.086, perte reelle 12.814 % (gap inclus), EV 0.8608 % — **REFUSE**
      - refuse : cible atteinte seulement 11.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.64 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 19.89 %) — p(stop avant cible) 0.1466 [0.11 ; 0.19], R/R 1.324, perte reelle 20.198 % (gap inclus), EV 0.5046 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.79 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 21.698 %) — p(stop avant cible) 0.1235 [0.09 ; 0.16], R/R 1.211, perte reelle 22.082 % (gap inclus), EV 0.4816 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.65 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 28.931 %) — p(stop avant cible) 0.0484 [0.03 ; 0.07], R/R 0.908, perte reelle 29.451 % (gap inclus), EV 0.4298 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.36 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 32.547 %) — p(stop avant cible) 0.0265 [0.01 ; 0.05], R/R 0.811, perte reelle 32.972 % (gap inclus), EV 0.5009 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.15 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 36.163 %) — p(stop avant cible) 0.0123 [0.00 ; 0.03], R/R 0.732, perte reelle 36.525 % (gap inclus), EV 0.602 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.13 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 39.78 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 0.656, perte reelle 40.728 % (gap inclus), EV 0.6933 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.47 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 43.396 %) — p(stop avant cible) 0.0004 [0.00 ; 0.01], R/R 0.615, perte reelle 43.462 % (gap inclus), EV 0.7026 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.32 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 47.012 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.559, perte reelle 47.859 % (gap inclus), EV 0.7065 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.23 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 50.629 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.528, perte reelle 50.629 % (gap inclus), EV 0.7053 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.23 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 54.245 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.483, perte reelle 55.322 % (gap inclus), EV 0.7048 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.24 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 57.861 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.462, perte reelle 57.87 % (gap inclus), EV 0.7043 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.23 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 136.83, ATR14 9.8964 (7.233 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.394 ATR = 2.85 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.362 % | 136.3352 | 94.06 % | 96.58 % | 97.08 % | 97.78 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.723 % | 135.8404 | 88.33 % | 92.15 % | 93.65 % | 94.95 % | 96.65 % | 97.23 % |
| 0.15 ATR | 1.085 % | 135.3455 | 81.59 % | 87.31 % | 90.02 % | 92.02 % | 94.31 % | 95.49 % |
| 0.2 ATR | 1.447 % | 134.8507 | 74.04 % | 81.97 % | 85.28 % | 88.59 % | 91.78 % | 93.44 % |
| 0.25 ATR | 1.808 % | 134.3559 | 68.21 % | 78.25 % | 82.46 % | 86.46 % | 89.34 % | 91.69 % |
| 0.35 ATR | 2.531 % | 133.3663 | 54.93 % | 68.98 % | 75.6 % | 81.21 % | 85.89 % | 89.03 % |
| 0.5 ATR | 3.616 % | 131.8818 | 38.13 % | 55.39 % | 63.71 % | 71.72 % | 78.68 % | 84.1 % |
| 0.75 ATR | 5.424 % | 129.4077 | 19.52 % | 38.07 % | 47.48 % | 58.59 % | 68.32 % | 76.21 % |
| 1.0 ATR | 7.233 % | 126.9336 | 9.46 % | 25.58 % | 35.28 % | 46.67 % | 59.09 % | 68.82 % |
| 1.25 ATR | 9.041 % | 124.4595 | 4.12 % | 14.8 % | 25.1 % | 35.96 % | 50.05 % | 61.44 % |
| 1.5 ATR | 10.849 % | 121.9854 | 2.11 % | 8.76 % | 17.44 % | 29.09 % | 42.94 % | 55.69 % |
| 2.0 ATR | 14.465 % | 117.0371 | 0.2 % | 3.12 % | 7.46 % | 16.06 % | 30.76 % | 45.74 % |
| 2.5 ATR | 18.082 % | 112.0889 | 0.1 % | 0.91 % | 2.42 % | 8.69 % | 21.12 % | 36.31 % |
| 3.0 ATR | 21.698 % | 107.1407 | 0.1 % | 0.5 % | 1.01 % | 4.55 % | 14.42 % | 26.97 % |
| 4.0 ATR | 28.931 % | 97.2443 | 0.0 % | 0.0 % | 0.3 % | 0.81 % | 6.09 % | 17.33 % |
| 6.0 ATR | 43.396 % | 77.4514 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.61 % | 4.21 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.39 ATR | 0.44 ATR | 0.57 ATR | 0.68 ATR | 0.74 ATR | 0.99 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.58 ATR | 0.65 ATR | 0.85 ATR | 1.01 ATR | 1.13 ATR | 1.45 ATR | 1.83 ATR |
| **3 s.** | 0.36 ATR | 0.71 ATR | 0.80 ATR | 1.06 ATR | 1.25 ATR | 1.42 ATR | 1.87 ATR | 2.24 ATR |
| **5 s.** | 0.45 ATR | 0.93 ATR | 1.04 ATR | 1.36 ATR | 1.66 ATR | 1.85 ATR | 2.41 ATR | 2.95 ATR |
| **10 s.** | 0.59 ATR | 1.25 ATR | 1.43 ATR | 1.91 ATR | 2.30 ATR | 2.58 ATR | 3.53 ATR | 4.40 ATR |
| **20 s.** | 0.79 ATR | 1.79 ATR | 2.04 ATR | 2.68 ATR | 3.20 ATR | 3.72 ATR | 5.12 ATR | 5.88 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.439–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.616 %, prix 131.8822), p(touche) 38.13 % (en stress 88.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.65–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.424 %, prix 129.4083), p(touche) 38.07 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.801–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.233 %, prix 126.9331), p(touche) 35.28 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.039–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (9.041 %, prix 124.4592), p(touche) 35.96 % (en stress 95.96 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.428–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.849 %, prix 121.9853), p(touche) 42.94 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 55.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.039–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (18.082 %, prix 112.0884), p(touche) 36.31 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 54.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.004 | EV/share : $0.020 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 32 % | T2 — | T3 —
- Kelly (position) : f* 0.014 | ¼-Kelly 0.003 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 35.0 | bear 5.5 | side 59.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 122.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.383% → cible +3.63% / stop −3.5%, p_fill 90%, n_eff≈99.3) : P(cible|rempli) **32%** · **EV/risk -0.030** (×p_fill ; si rempli -0.12% du capital)
  - **swing** (entrée dip −0.678% → cible +11.309% / stop −7.282%, p_fill 89%, n_eff≈104.8) : P(cible|rempli) **34%** · **EV/risk +0.110** (×p_fill ; si rempli +0.90% du capital)
  - **deep** (entrée dip −0.921% → cible +11.586% / stop −10.95%, p_fill 91%, n_eff≈103.2) : P(cible|rempli) **51%** · **EV/risk +0.170** (×p_fill ; si rempli +2.04% du capital)
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

**Factor** : R² 0.85 · part idiosyncratique 0.15
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral_cautious


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 34.6  _(momentum baissier)_
- **ADX** : 27.6  _(tendance etablie)_
- **MACD** : hist -3.431  _(pas de croisement recent)_
- **BB** : %B -0.13 · largeur 20.0%
- **ATR** : 9.9 (50.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.202  _(distribution)_
- **Vol ratio** : 1.52  _(volume au-dessus de la moyenne)_
- **Choppiness** : 51.0  _(transition)_
- **MA** : MA20 156.4 · MA50 134.92 · MA200 135.6  _(prix < MA20)_
- **Dist MA** : MA20 -12.5% · MA50 +1.4% · MA200 +0.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (793809 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
