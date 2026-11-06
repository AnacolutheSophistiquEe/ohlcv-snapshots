# MSTR

**Generated** : 2026-11-06T01:22:11.591957+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 5.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $129.41  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-06 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)  
> ↳ spot $129.41 (+2.0% vs entrée) · entrée $126.90 · stop $123.38 · T1 $133.95 · R/R 2.0  
> ↳ _probas brutes, non calibrées · n=0_  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -5.3 % ≠ (strike 135.0 − spot 129.41)/spot = +4.3 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 580 % hors [0,100] (R² max 0.79). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-05 : 129.41 · ATR Wilder 10.01 (7.73 %)_
- **Swing** : plage **116.98 → 108.6** (-9.61 % a -16.08 % sous la cloture, 0.84 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 113.2-117.85 (B). stop INDICATIF 95.05 (-12.48 % sous le bas ; sous le support 100.05-104.78 (- 0,5 ATR)).
- **Deep** : plage **108.6 → 85.63** (-16.08 % a -33.83 % sous la cloture, 2.29 ATR) — touchee 46 % → 15 % du temps en 20 seances ; supports reels dans la plage : 100.05-104.78 (B) ; 89.21-91.67 (A). stop INDICATIF 75.67 (-11.63 % sous le bas ; sous le support 80.68-81.81 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (2.9 ATR sous le plus haut 20 s., RSI(2) 25.5 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 118.4-123.33 (A, -4.7 %) ; 113.2-117.85 (B, -8.93 %) ; 100.05-104.78 (B, -19.03 %) ; 89.21-91.67 (A, -29.16 %) ; 80.68-81.81 (A, -36.78 %) ; 58.85-61.41 (C, -52.54 %)
- Resistances reelles au-dessus : 132.55-137.26 (A, 2.43 %) ; 139.45-144.2 (A, 7.75 %) ; 144.92-149.75 (A, 11.99 %) ; 150.77-155.69 (A, 16.5 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=10.85 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (11.81 %)** : le gap seul le franchit 0.239 % des séances (3 fois sur 1253).
   - exécution **14.768 pt plus bas** dans le cas TYPIQUE (médiane), 15.403 au p90, **15.562 au pire**
   - perte réelle **22.94 %** en moyenne _(tirée par la queue)_, jusqu'à **27.372 %** — au lieu des 11.81 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0266 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.493 % | p01 -7.775 % | pire -27.372 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.38** [0.3102 ; 0.4538] _(largeur 14.4 pt, n_eff 173.1)_
   - swing : **0.3534** [0.3044 ; 0.4048] _(largeur 10.0 pt, n_eff 345.7)_
   - deep : **0.3262** [0.2784 ; 0.3769] _(largeur 9.9 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : swing (26.5 pt), deep (28.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1080 séances)** : VaR **-7.85 %** | CVaR **-10.79 %** | vol 5.54 %/j
   - _fenêtre arrêtée : rupture de regime a 1140 seances en arriere (volatilite 9.71 % contre 5.32 % aujourd'hui, rapport 1.83)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.99 % vs -18.02 % si l'on extrapolait par √5 _(rapport 0.943 ; < 1 = le √5 surestime)_
- **β de baisse : 2.3654** (β de hausse 1.8641, asymétrie 1.2689) vs IWM — 605 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 119.0503 sur swing_based (0.75 ATR, 8.005 %) — p(stop avant cible) 0.5366 [0.48 ; 0.59], R/R 3.594, perte reelle 8.244 % (gap inclus), CVaR 10.057 %, EV 0.4861 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.4743 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 9.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.537, borne haute 0.589 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 10.06 % > budget 9.50 %
- Budget de queue : **9.5 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.122 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 37.9 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.75 ATR (stop 8.005 %) — p(stop avant cible) 0.5366 [0.48 ; 0.59], R/R 3.594, perte reelle 8.244 % (gap inclus), EV 0.4861 % — **REFUSE**
      - refuse : cible atteinte seulement 9.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.537, borne haute 0.589 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 10.06 % > budget 9.50 %
   - 🟢 support a 1.33 ATR (stop 12.415 %) — p(stop avant cible) 0.3393 [0.29 ; 0.39], R/R 2.364, perte reelle 12.532 % (gap inclus), EV 0.4691 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.21 % > budget 9.50 %
   - 🟢 support a 2.58 ATR (stop 21.866 %) — p(stop avant cible) 0.1139 [0.08 ; 0.15], R/R 1.332, perte reelle 22.237 % (gap inclus), EV 0.1969 % — **REFUSE**
      - refuse : cible atteinte seulement 10.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.71 % > budget 9.50 %
   - 🟢 support a 4.12 ATR (stop 33.426 %) — p(stop avant cible) 0.0207 [0.01 ; 0.04], R/R 0.875, perte reelle 33.845 % (gap inclus), EV 0.2458 % — **REFUSE**
      - refuse : cible atteinte seulement 10.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.59 % > budget 9.50 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.887 %) — p(stop avant cible) 0.9074 [0.87 ; 0.93], R/R 15.122, perte reelle 1.959 % (gap inclus), EV -0.3412 % — **REFUSE**
      - refuse : cible atteinte seulement 2.7 % du temps (< 15 %) meme a 10 seances : le R/R de 15.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.907, borne haute 0.935 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.34 %) : P(cible) 2.7 % x 29.63 % + P(rien) 6.6 % x 9.84 % ne couvrent pas P(stop) 90.7 % x 1.96 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 15.092 %) — p(stop avant cible) 0.2438 [0.20 ; 0.29], R/R 1.928, perte reelle 15.367 % (gap inclus), EV 0.4311 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.43 % > budget 9.50 %
   - ⚪ atr_grid a 2.25 ATR (stop 16.979 %) — p(stop avant cible) 0.1904 [0.15 ; 0.23], R/R 1.723, perte reelle 17.19 % (gap inclus), EV 0.367 % — **REFUSE**
      - refuse : cible atteinte seulement 10.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.78 % > budget 9.50 %
   - ⚪ atr_grid a 3.5 ATR (stop 26.411 %) — p(stop avant cible) 0.0617 [0.04 ; 0.09], R/R 1.106, perte reelle 26.796 % (gap inclus), EV 0.2062 % — **REFUSE**
      - refuse : cible atteinte seulement 10.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.89 % > budget 9.50 %
   - ⚪ atr_grid a 5.0 ATR (stop 37.73 %) — p(stop avant cible) 0.0051 [0.00 ; 0.02], R/R 0.776, perte reelle 38.172 % (gap inclus), EV 0.3736 % — **REFUSE**
      - refuse : cible atteinte seulement 10.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.77 % > budget 9.50 %
   - ⚪ atr_grid a 5.5 ATR (stop 41.503 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 0.707, perte reelle 41.88 % (gap inclus), EV 0.4156 % — **REFUSE**
      - refuse : cible atteinte seulement 10.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.97 % > budget 9.50 %
   - ⚪ atr_grid a 6.0 ATR (stop 45.276 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.654, perte reelle 45.276 % (gap inclus), EV 0.4221 % — **REFUSE**
      - refuse : cible atteinte seulement 10.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.83 % > budget 9.50 %
   - ⚪ atr_grid a 6.5 ATR (stop 49.049 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.602, perte reelle 49.219 % (gap inclus), EV 0.4214 % — **REFUSE**
      - refuse : cible atteinte seulement 10.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.83 % > budget 9.50 %
   - ⚪ atr_grid a 7.0 ATR (stop 52.822 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.561, perte reelle 52.822 % (gap inclus), EV 0.4201 % — **REFUSE**
      - refuse : cible atteinte seulement 10.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.83 % > budget 9.50 %
   - ⚪ atr_grid a 7.5 ATR (stop 56.595 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.521, perte reelle 56.902 % (gap inclus), EV 0.4197 % — **REFUSE**
      - refuse : cible atteinte seulement 10.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.84 % > budget 9.50 %
   - ⚪ atr_grid a 8.0 ATR (stop 60.368 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.49, perte reelle 60.497 % (gap inclus), EV 0.4247 % — **REFUSE**
      - refuse : cible atteinte seulement 10.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.84 % > budget 9.50 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 129.41, ATR14 9.7654 (7.546 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.39 ATR = 2.943 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.377 % | 128.9217 | 93.86 % | 96.47 % | 97.07 % | 97.67 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.755 % | 128.4335 | 87.92 % | 91.94 % | 93.64 % | 94.84 % | 96.65 % | 97.23 % |
| 0.15 ATR | 1.132 % | 127.9452 | 81.27 % | 87.2 % | 90.01 % | 91.91 % | 94.31 % | 95.48 % |
| 0.2 ATR | 1.509 % | 127.4569 | 73.62 % | 81.75 % | 85.27 % | 88.47 % | 91.77 % | 93.43 % |
| 0.25 ATR | 1.887 % | 126.9687 | 67.67 % | 78.02 % | 82.44 % | 86.35 % | 89.33 % | 91.68 % |
| 0.35 ATR | 2.641 % | 125.9921 | 54.48 % | 68.75 % | 75.48 % | 81.19 % | 85.87 % | 89.01 % |
| 0.5 ATR | 3.773 % | 124.5273 | 37.56 % | 55.04 % | 63.47 % | 71.79 % | 78.76 % | 84.29 % |
| 0.75 ATR | 5.66 % | 122.086 | 19.34 % | 37.7 % | 47.33 % | 58.54 % | 68.6 % | 76.59 % |
| 1.0 ATR | 7.546 % | 119.6446 | 9.47 % | 25.3 % | 35.02 % | 46.51 % | 59.35 % | 69.3 % |
| 1.25 ATR | 9.433 % | 117.2033 | 4.03 % | 14.62 % | 24.82 % | 35.79 % | 50.2 % | 61.91 % |
| 1.5 ATR | 11.319 % | 114.762 | 2.01 % | 8.57 % | 17.26 % | 29.02 % | 43.19 % | 56.26 % |
| 2.0 ATR | 15.092 % | 109.8793 | 0.1 % | 2.92 % | 7.16 % | 15.77 % | 30.79 % | 46.41 % |
| 2.5 ATR | 18.865 % | 104.9966 | 0.1 % | 0.71 % | 2.12 % | 8.19 % | 20.63 % | 36.86 % |
| 3.0 ATR | 22.638 % | 100.1139 | 0.1 % | 0.3 % | 0.71 % | 4.04 % | 13.82 % | 27.1 % |
| 4.0 ATR | 30.184 % | 90.3486 | 0.0 % | 0.0 % | 0.2 % | 0.61 % | 5.39 % | 16.84 % |
| 6.0 ATR | 45.276 % | 70.8179 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.41 % | 3.9 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.39 ATR | 0.43 ATR | 0.56 ATR | 0.67 ATR | 0.74 ATR | 0.99 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.57 ATR | 0.65 ATR | 0.84 ATR | 1.01 ATR | 1.12 ATR | 1.44 ATR | 1.82 ATR |
| **3 s.** | 0.36 ATR | 0.71 ATR | 0.80 ATR | 1.05 ATR | 1.25 ATR | 1.41 ATR | 1.86 ATR | 2.21 ATR |
| **5 s.** | 0.45 ATR | 0.93 ATR | 1.03 ATR | 1.35 ATR | 1.65 ATR | 1.84 ATR | 2.38 ATR | 2.88 ATR |
| **10 s.** | 0.59 ATR | 1.26 ATR | 1.44 ATR | 1.91 ATR | 2.29 ATR | 2.55 ATR | 3.45 ATR | 4.16 ATR |
| **20 s.** | 0.81 ATR | 1.82 ATR | 2.07 ATR | 2.70 ATR | 3.21 ATR | 3.69 ATR | 5.06 ATR | 5.83 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.434–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.773 %, prix 124.5274), p(touche) 37.56 % (en stress 85.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.645–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.66 %, prix 122.0854), p(touche) 37.7 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.797–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.546 %, prix 119.6447), p(touche) 35.02 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.035–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (9.433 %, prix 117.2028), p(touche) 35.79 % (en stress 94.95 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.435–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (11.319 %, prix 114.7621), p(touche) 43.19 % (en stress 100.0 %)  ✅ optimum identifie (60.5 % des re-echantillons)
- **20 seance(s)** : plage utile 2.074–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (18.865 %, prix 104.9968), p(touche) 36.86 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 55.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 70.7 | bear 19.7 | side 9.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 115.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.937% → cible +5.553% / stop −2.776%, p_fill 54%, n_eff≈60.4) : P(cible|rempli) **11%** · **EV/risk -0.035** (×p_fill ; si rempli -0.18% du capital)
  - **swing** (entrée dip −4.264% → cible +8.117% / stop −7.882%, p_fill 42%, n_eff≈49.7) : P(cible|rempli) **39%** · **EV/risk +0.027** (×p_fill ; si rempli +0.51% du capital)
  - **deep** (entrée dip −6.592% → cible +25.497% / stop −12.749%, p_fill 38%, n_eff≈44.1) : P(cible|rempli) **5%** · **EV/risk -0.099** (×p_fill ; si rempli -3.35% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→78% · +2.0%→58% · +3.0%→40% · +5.0%→19% · +8.0%→10%
- Range intraday médian 5.35% (p90 9.82%) · excursion haute méd. +2.51% / basse méd. −2.26%
- Profil de vol intra : ouverture 3.268% vs midi 1.123% vs clôture 1.265% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 17% · trend ↑2%/↓0% ; spike-down 69% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.139 ; mean-reverting — autocorr -0.04)_ ; drift intra méd. 0.468% ; recovery-V 35%
- **σ réalisé intraday** 3.406% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 59% / whipsaw 31%
- POC intraday (dernière séance, temps-au-prix) : 148.5395 (VA 146.6095–150.0835 ; dernier close 146.04)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 25% · rebond 73% · **stop −3.89%** sous le fill (sous le bruit) · cible +2.23% · R/R 0.57 (high win-rate)
- Gaps overnight (n=159) : méd. -0.06% · baisse 52% (gap-down >1% 38% · >2% 25%)
- Excursion ouverture 5min (n=160) : bas méd −0.78% (p90 −1.81%) · haut méd +0.88% · range méd 1.84%
- Excursion ouverture 15min (n=160) : bas méd −1.07% (p90 −2.68%) · haut méd +1.24% · range méd 2.55%
- Excursion ouverture 30min (n=160) : bas méd −1.2% (p90 −3.06%) · haut méd +1.47% · range méd 2.95%
- Excursion ouverture 60min (n=160) : bas méd −1.57% (p90 −3.47%) · haut méd +1.83% · range méd 3.74%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 146.01 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 76% (121/159) · gap 46% · délai 0.0min · rebond 44% (57/121) (MFE +0.7%)
   - −1.0% : fill 30min 55% · séance 67% (112/159) · gap 38% · délai 0.0min · rebond 48% (59/112) (MFE +0.91%)
   - −1.5% : fill 30min 45% · séance 61% (103/159) · gap 31% · délai 0.0min · rebond 53% (57/103) (MFE +1.16%)
   - −2.0% : fill 30min 38% · séance 54% (91/159) · gap 25% · délai 0.0min · rebond 60% (54/91) (MFE +1.25%)
   - −3.0% : fill 30min 28% · séance 41% (71/159) · gap 17% · délai 0.7min · rebond 52% (38/71) (MFE +1.5%)
   - −4.0% : fill 30min 21% · séance 32% (56/159) · gap 6% · délai 3.2min · rebond 72% (37/56) (MFE +1.65%)
   - −5.0% : fill 30min 17% · séance 25% (41/159) · gap 4% · délai 12.9min · rebond 73% (29/41) (MFE +2.23%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.65% (p90 −2.12%) → stop au-delà de −1.69% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.8% (p90 −2.19%) → stop au-delà de −1.71% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.76% (p90 −2.14%) → stop au-delà de −1.8% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=888 jambes) : jambe baissière méd −1.12% (p90 −2.6%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 97% (74/75) · rebond 49% (34/74)
      · −2.0% : fill 86% (66/75) · rebond 58% (37/66)
      · −3.0% : fill 71% (57/75) · rebond 49% (30/57)
      · −4.0% : fill 60% (48/75) · rebond 72% (32/48)
      · −5.0% : fill 49% (37/75) · rebond 74% (27/37)
   - **flat** (18 séances) :
      · −1.0% : fill 74% (14/18) · rebond 55% (10/14)
      · −2.0% : fill 46% (9/18) · rebond 54% (5/9)
      · −3.0% : fill 38% (7/18) · rebond 71% (4/7)
      · −4.0% : fill 17% (4/18) · rebond 80% (3/4)
      · −5.0% : fill 5% (2/18) · rebond 0% (0/2)
   - **gap-up** (66 séances) :
      · −1.0% : fill 30% (24/66) · rebond 41% (15/24)
      · −2.0% : fill 19% (16/66) · rebond 70% (12/16)
      · −3.0% : fill 7% (7/66) · rebond 67% (4/7)
      · −4.0% : fill 3% (4/66) · rebond 58% (2/4)
      · −5.0% : fill 2% (2/66) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 56% si les 15 1res min sont vertes (88 cas) · 32% si rouges (72 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:14** → P(séance verte=clôture>ouverture) 71% si début vert vs 7% si rouge (base 46% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 230min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=90) : tient le vert **71%** · continue >prix actuel 43% ; creux résiduel méd -1.55% (q20 -2.88%) → **SL/trailing à −2.88%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.62% / q75 +2.85% → **scale +1.62% / runner +2.85%**, sortie à la clôture
  - **si ROUGE au coude** (n=70) : edge inversé — récupère vert seulement **7%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.18%** (au-delà de la MAE q10 -5.18%), cible rebond +1.17% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.82% .. +3.69%] · haut q95 +3.94% · bas q05 -3.62%
   - 60min (n=160) : retour [-3.45% .. +5.63%] · haut q95 +6.12% · bas q05 -4.56%
   - 2h (n=160) : retour [-4.42% .. +7.83%] · haut q95 +8.96% · bas q05 -5.49%
   - 4h (n=160) : retour [-5.2% .. +8.2%] · haut q95 +10.02% · bas q05 -6.02%
   - 6h (n=160) : retour [-5.31% .. +8.86%] · haut q95 +10.13% · bas q05 -6.26%
   - session (n=160) : retour [-5.14% .. +8.51%] · haut q95 +10.13% · bas q05 -6.52%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 7.5% des séances sont trend-up (mild 0.6% / strong 6.9%) · base = 12 séances trend-up (n_eff 8.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **47%**. Lecture précoce 30 min : signature présente → 17% vs absente 6% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.9% (p75 1.29% / p90 2.02%) · ~4.0 replis/séance, durée méd 30.47 min. P(nouveau plus-haut après repli) :
   - −0.5% → **87%** (reprise méd 20.0 min, n=46)
   - −1.0% → **74%** (reprise méd 17.06 min, n=20)
   - −1.5% → **58%** (reprise méd 13.97 min, n=11)
   - −2.0% → **46%** (reprise méd 31.23 min, n=8)
   - −3.0% → **38%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.02%** (p90, défaut prudent ; serré/agressif −1.29%) ; extension open→close méd +8.69% (q75 +10.68% / q95 +13.17%), MFE méd +10.02% / q90 +13.15%
   - Échelle scale-out : +10.02% (33%) / +12.77% (33%) / +13.15% (34%)
- **DÉSARMER** : repli > **−2.02%** depuis le plus-haut = décay → P(retournement) **81%** (préavis méd 157.2 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.15% : P(retournement après) 0% (mèche méd 0.05%)
- **CONTEXTE** : la dernière heure tient les gains 71% du temps (retour médian dernière heure +0.81%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.87 · part idiosyncratique 0.13
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-06 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-10 — US CPI (headline) (J-3 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-10 — US CPI (headline) (J-3 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 45.2  _(neutre)_
- **ADX** : 16.1  _(pas de tendance nette)_
- **MACD** : hist -1.585  _(pas de croisement recent)_
- **BB** : %B 0.08 · largeur 21.8%
- **ATR** : 9.77 (52.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.043  _(neutre)_
- **Vol ratio** : 1.25  _(volume normal)_
- **Choppiness** : 55.3  _(transition)_
- **MA** : MA20 142.57 · MA50 144.6 · MA200 133.9  _(prix < MA20)_
- **Dist MA** : MA20 -9.2% · MA50 -10.5% · MA200 -3.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (736002 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
