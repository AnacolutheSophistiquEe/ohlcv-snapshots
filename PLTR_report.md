# PLTR

**Generated** : 2026-11-19T01:25:16.273622+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite extreme · $156.68  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 12/125 fenêtres (p_fill pondéré 8 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot $156.68 (+4.5% vs entrée) · entrée $149.88 · stop $146.14 · T1 $156.84 · R/R 1.86  
> ↳ ¼-Kelly 0.029 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -37 % hors [0,100] (R² max 0.97). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-18 : 156.68 · ATR Wilder 8.57 (5.47 %)_
- **Swing** : plage **146.52 → 138.94** (-6.48 % a -11.32 % sous la cloture, 0.88 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 144.86-149.09 (B) ; 122.64-143.28 (A) ; 138.9-142.34 (B). stop INDICATIF 129.2 (-7.01 % sous le bas ; sous le support 133.49-136.88 (- 0,5 ATR)).
- **Deep** : plage **138.94 → 122.08** (-11.32 % a -22.09 % sous la cloture, 1.97 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 122.64-143.28 (A) ; 138.9-142.34 (B) ; 133.49-136.88 (B) ; 128.32-132.41 (B). stop INDICATIF 113.6 (-6.94 % sous le bas ; sous le support 117.89-119.41 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 5.36 ATR sous le plus haut 20 s., RSI(2) 6.9. Limite **152.39** (seance suivante), stop catastrophe 118.1, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 149.64-152.68 (A, -2.55 %) ; 144.86-149.09 (B, -4.84 %) ; 122.64-143.28 (A, -8.55 %) ; 138.9-142.34 (B, -9.15 %) ; 133.49-136.88 (B, -12.64 %) ; 128.32-132.41 (B, -15.49 %)
- Resistances reelles au-dessus : 160.39-164.55 (A, 2.37 %) ; 165.08-168.91 (A, 5.36 %) ; 169.42-172.0 (A, 8.13 %) ; 174.29-176.5 (A, 11.24 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.79 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (15.81 %)** : le gap seul le franchit 0.08 % des séances (1 fois sur 1253).
   - exécution **2.122 pt plus bas** dans le cas TYPIQUE (médiane), 2.122 au p90, **2.122 au pire**
   - perte réelle **17.932 %** en moyenne _(tirée par la queue)_, jusqu'à **17.932 %** — au lieu des 15.81 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0017 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.904 % | p01 -6.139 % | pire -17.932 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3033** [0.2385 ; 0.3746] _(largeur 13.6 pt, n_eff 173.1)_
   - swing : **0.2969** [0.2506 ; 0.3466] _(largeur 9.6 pt, n_eff 345.7)_
   - deep : **0.2646** [0.2202 ; 0.3129] _(largeur 9.3 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.1 %** | CVaR **-8.45 %** | vol 4.25 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.31 % vs -13.77 % si l'on extrapolait par √5 _(rapport 0.966 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7147** (β de hausse 1.421, asymétrie 1.2067) vs IWM — 604 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 146.106 sur swing_based (0.62 ATR, 6.749 %) — p(stop avant cible) 0.458 [0.41 ; 0.51], R/R 2.898, perte reelle 6.84 % (gap inclus), CVaR 7.578 %, EV 1.2009 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.3401 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 10.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.62 ATR (stop 6.749 %) — p(stop avant cible) 0.458 [0.41 ; 0.51], R/R 2.898, perte reelle 6.84 % (gap inclus), EV 1.2009 % — **REFUSE**
      - refuse : cible atteinte seulement 10.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_based a 1.5 ATR (stop 9.391 %) — p(stop avant cible) 0.3244 [0.28 ; 0.38], R/R 2.055, perte reelle 9.643 % (gap inclus), EV 1.0209 % — **REFUSE**
      - refuse : cible atteinte seulement 11.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 2.87 ATR (stop 20.873 %) — p(stop avant cible) 0.0647 [0.04 ; 0.09], R/R 0.946, perte reelle 20.948 % (gap inclus), EV 1.0498 % — **REFUSE**
      - refuse : cible atteinte seulement 11.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.97 % > budget 12.00 %
   - 🟢 support a 3.95 ATR (stop 27.65 %) — p(stop avant cible) 0.0031 [0.00 ; 0.01], R/R 0.686, perte reelle 28.909 % (gap inclus), EV 1.3985 % — **REFUSE**
      - refuse : cible atteinte seulement 11.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.62 % > budget 12.00 %
   - 🟢 support a 5.13 ATR (stop 35.003 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 0.563, perte reelle 35.2 % (gap inclus), EV 1.4039 % — **REFUSE**
      - refuse : cible atteinte seulement 11.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.52 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.565 %) — p(stop avant cible) 0.8627 [0.82 ; 0.90], R/R 12.431, perte reelle 1.594 % (gap inclus), EV 0.3226 % — **REFUSE**
      - refuse : cible atteinte seulement 4.0 % du temps (< 15 %) meme a 10 seances : le R/R de 12.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.863, borne haute 0.896 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ grid_snapped a 0.62 ATR (stop 5.734 %) — p(stop avant cible) 0.5308 [0.48 ; 0.58], R/R 3.4, perte reelle 5.829 % (gap inclus), EV 0.8773 % — **REFUSE**
      - refuse : cible atteinte seulement 8.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.531, borne haute 0.583 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.25 ATR (stop 7.826 %) — p(stop avant cible) 0.3958 [0.35 ; 0.45], R/R 2.481, perte reelle 7.99 % (gap inclus), EV 1.1917 % — **REFUSE**
      - refuse : cible atteinte seulement 10.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.75 ATR (stop 10.957 %) — p(stop avant cible) 0.2729 [0.23 ; 0.32], R/R 1.717, perte reelle 11.544 % (gap inclus), EV 0.8196 % — **REFUSE**
      - refuse : cible atteinte seulement 11.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.96 % > budget 12.00 %
   - ⚪ atr_grid a 2.0 ATR (stop 12.522 %) — p(stop avant cible) 0.2086 [0.17 ; 0.25], R/R 1.516, perte reelle 13.07 % (gap inclus), EV 0.9956 % — **REFUSE**
      - refuse : cible atteinte seulement 11.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.74 % > budget 12.00 %
   - ⚪ atr_grid a 2.25 ATR (stop 14.087 %) — p(stop avant cible) 0.1687 [0.13 ; 0.21], R/R 1.369, perte reelle 14.476 % (gap inclus), EV 0.8914 % — **REFUSE**
      - refuse : cible atteinte seulement 11.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.40 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 15.652 %) — p(stop avant cible) 0.1429 [0.11 ; 0.18], R/R 1.252, perte reelle 15.824 % (gap inclus), EV 0.9476 % — **REFUSE**
      - refuse : cible atteinte seulement 11.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.14 % > budget 12.00 %
   - ⚪ grid_snapped a 2.87 ATR (stop 19.859 %) — p(stop avant cible) 0.0732 [0.05 ; 0.10], R/R 0.993, perte reelle 19.956 % (gap inclus), EV 1.0649 % — **REFUSE**
      - refuse : cible atteinte seulement 11.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.00 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 21.913 %) — p(stop avant cible) 0.0476 [0.03 ; 0.07], R/R 0.898, perte reelle 22.077 % (gap inclus), EV 1.1238 % — **REFUSE**
      - refuse : cible atteinte seulement 11.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.00 % > budget 12.00 %
   - 🟢 grid_snapped a 3.95 ATR (stop 26.636 %) — p(stop avant cible) 0.0046 [0.00 ; 0.02], R/R 0.714, perte reelle 27.755 % (gap inclus), EV 1.3837 % — **REFUSE**
      - refuse : cible atteinte seulement 11.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.75 % > budget 12.00 %
   - 🟢 grid_snapped a 5.13 ATR (stop 33.988 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 0.572, perte reelle 34.668 % (gap inclus), EV 1.4045 % — **REFUSE**
      - refuse : cible atteinte seulement 11.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.51 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 37.566 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.527, perte reelle 37.599 % (gap inclus), EV 1.4048 % — **REFUSE**
      - refuse : cible atteinte seulement 11.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.45 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 40.696 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.487, perte reelle 40.696 % (gap inclus), EV 1.4072 % — **REFUSE**
      - refuse : cible atteinte seulement 11.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.44 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 43.827 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.452, perte reelle 43.827 % (gap inclus), EV 1.4068 % — **REFUSE**
      - refuse : cible atteinte seulement 11.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.44 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 46.957 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.422, perte reelle 46.957 % (gap inclus), EV 1.4068 % — **REFUSE**
      - refuse : cible atteinte seulement 11.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.44 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 50.088 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.396, perte reelle 50.088 % (gap inclus), EV 1.4068 % — **REFUSE**
      - refuse : cible atteinte seulement 11.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.44 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 156.68, ATR14 9.8096 (6.261 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.363 ATR = 2.273 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.313 % | 156.1895 | 92.75 % | 95.36 % | 96.17 % | 96.97 % | 98.27 % | 98.67 % |
| 0.1 ATR | 0.626 % | 155.699 | 84.99 % | 89.62 % | 91.42 % | 93.63 % | 95.22 % | 96.41 % |
| 0.15 ATR | 0.939 % | 155.2085 | 76.94 % | 83.77 % | 85.97 % | 89.79 % | 92.58 % | 94.25 % |
| 0.2 ATR | 1.252 % | 154.7181 | 69.18 % | 78.53 % | 81.84 % | 86.45 % | 90.35 % | 92.4 % |
| 0.25 ATR | 1.565 % | 154.2276 | 62.34 % | 73.79 % | 77.7 % | 82.81 % | 87.7 % | 90.76 % |
| 0.35 ATR | 2.191 % | 153.2466 | 51.26 % | 65.83 % | 71.24 % | 78.06 % | 83.74 % | 87.47 % |
| 0.5 ATR | 3.13 % | 151.7752 | 36.56 % | 53.12 % | 59.94 % | 69.06 % | 77.64 % | 82.65 % |
| 0.75 ATR | 4.696 % | 149.3228 | 19.54 % | 35.38 % | 44.9 % | 55.51 % | 66.87 % | 75.15 % |
| 1.0 ATR | 6.261 % | 146.8704 | 8.96 % | 23.29 % | 32.9 % | 43.98 % | 56.61 % | 65.91 % |
| 1.25 ATR | 7.826 % | 144.4179 | 4.53 % | 15.73 % | 23.41 % | 34.18 % | 46.54 % | 57.08 % |
| 1.5 ATR | 9.391 % | 141.9655 | 2.01 % | 10.58 % | 17.56 % | 26.79 % | 40.24 % | 52.36 % |
| 2.0 ATR | 12.522 % | 137.0607 | 0.7 % | 4.03 % | 9.59 % | 16.08 % | 29.37 % | 39.32 % |
| 2.5 ATR | 15.652 % | 132.1559 | 0.1 % | 1.41 % | 3.43 % | 9.5 % | 19.72 % | 29.47 % |
| 3.0 ATR | 18.783 % | 127.2511 | 0.0 % | 0.6 % | 1.72 % | 5.26 % | 13.41 % | 22.69 % |
| 4.0 ATR | 25.044 % | 117.4414 | 0.0 % | 0.0 % | 0.3 % | 1.52 % | 5.28 % | 12.83 % |
| 6.0 ATR | 37.566 % | 97.8221 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.51 % | 4.21 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.36 ATR | 0.41 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 0.97 ATR | 1.22 ATR |
| **2 s.** | 0.24 ATR | 0.54 ATR | 0.61 ATR | 0.80 ATR | 0.96 ATR | 1.11 ATR | 1.54 ATR | 1.93 ATR |
| **3 s.** | 0.29 ATR | 0.67 ATR | 0.75 ATR | 1.00 ATR | 1.21 ATR | 1.40 ATR | 1.97 ATR | 2.37 ATR |
| **5 s.** | 0.40 ATR | 0.87 ATR | 0.98 ATR | 1.29 ATR | 1.58 ATR | 1.82 ATR | 2.46 ATR | 3.07 ATR |
| **10 s.** | 0.56 ATR | 1.16 ATR | 1.31 ATR | 1.83 ATR | 2.23 ATR | 2.48 ATR | 3.42 ATR | 4.12 ATR |
| **20 s.** | 0.75 ATR | 1.59 ATR | 1.78 ATR | 2.32 ATR | 2.83 ATR | 3.27 ATR | 4.66 ATR | 5.82 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.414–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.13 %, prix 151.7759), p(touche) 36.56 % (en stress 81.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.614–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.696 %, prix 149.3223), p(touche) 35.38 % (en stress 94.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.748–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.696 %, prix 149.3223), p(touche) 44.9 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 51.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.978–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.261 %, prix 146.8703), p(touche) 43.98 % (en stress 100.0 %)  ✅ optimum identifie (84.9 % des re-echantillons)
- **10 seance(s)** : plage utile 1.311–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.391 %, prix 141.9662), p(touche) 40.24 % (en stress 100.0 %)  ✅ optimum identifie (85.5 % des re-echantillons)
- **20 seance(s)** : plage utile 1.782–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (15.652 %, prix 132.1564), p(touche) 29.47 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (96.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.037 | EV/share : $0.138 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 11 % | T2 — | T3 —
- Kelly (position) : f* 0.114 | ¼-Kelly 0.029 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 84.8 | side 10.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=12, n_eff=10))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→74% · +2.0%→43% · +3.0%→24% · +5.0%→9% · +8.0%→2%
- Range intraday médian 3.72% (p90 6.77%) · excursion haute méd. +1.85% / basse méd. −1.63%
- Profil de vol intra : ouverture 2.877% vs midi 0.713% vs clôture 0.813% _(ouverture ~4.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (157 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 76% · range 22% · trend ↑2%/↓0% ; spike-down 56% · recovery-V 38%)_
- **Régime intraday** : **chop** _(efficiency 0.136 ; mean-reverting — autocorr -0.036)_ ; drift intra méd. 0.287% ; recovery-V 42%
- **σ réalisé intraday** 2.426% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 45% / whipsaw 8%
- POC intraday (dernière séance, temps-au-prix) : 195.972 (VA 195.3–196.476 ; dernier close 196.73)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 44% · rebond 70% · **stop −3.36%** sous le fill (sous le bruit) · cible +1.83% · R/R 0.54 (high win-rate)
- Gaps overnight (n=156) : méd. -0.05% · baisse 50% (gap-down >1% 24% · >2% 6%)
- Excursion ouverture 5min (n=157) : bas méd −0.81% (p90 −1.82%) · haut méd +0.75% · range méd 1.63%
- Excursion ouverture 15min (n=157) : bas méd −0.99% (p90 −2.38%) · haut méd +1.1% · range méd 2.22%
- Excursion ouverture 30min (n=157) : bas méd −1.08% (p90 −2.85%) · haut méd +1.2% · range méd 2.5%
- Excursion ouverture 60min (n=157) : bas méd −1.29% (p90 −2.98%) · haut méd +1.3% · range méd 2.76%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 196.75 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 75% (116/156) · gap 36% · délai 0.0min · rebond 62% (70/116) (MFE +1.34%)
   - −1.0% : fill 30min 54% · séance 63% (102/156) · gap 24% · délai 0.1min · rebond 68% (65/102) (MFE +1.5%)
   - −1.5% : fill 30min 40% · séance 48% (82/156) · gap 15% · délai 1.5min · rebond 65% (54/82) (MFE +1.59%)
   - −2.0% : fill 30min 35% · séance 44% (74/156) · gap 6% · délai 4.6min · rebond 70% (50/74) (MFE +1.83%)
   - −3.0% : fill 30min 15% · séance 24% (46/156) · gap 2% · délai 9.3min · rebond 53% (24/46) (MFE +1.28%)
   - −4.0% : fill 30min 9% · séance 16% (30/156) · gap 1% · délai 25.1min · rebond 47% (15/30) (MFE +0.95%)
   - −5.0% : fill 30min 3% · séance 9% (19/156) · gap 0% · délai 79.0min · rebond 40% (11/19) (MFE +0.88%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.56% (p90 −1.89%) → stop au-delà de −1.32% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.79% (p90 −1.93%) → stop au-delà de −1.41% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −1.63%) → stop au-delà de −1.14% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=483 jambes) : jambe baissière méd −1.06% (p90 −2.37%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 94% (70/75) · rebond 66% (45/70)
      · −2.0% : fill 74% (56/75) · rebond 74% (38/56)
      · −3.0% : fill 42% (36/75) · rebond 48% (18/36)
      · −4.0% : fill 28% (24/75) · rebond 55% (13/24)
      · −5.0% : fill 14% (16/75) · rebond 56% (11/16)
   - **flat** (21 séances) :
      · −1.0% : fill 81% (17/21) · rebond 66% (9/17)
      · −2.0% : fill 38% (11/21) · rebond 64% (8/11)
      · −3.0% : fill 20% (7/21) · rebond 59% (4/7)
      · −4.0% : fill 12% (4/21) · rebond 42% (2/4)
      · −5.0% : fill 5% (1/21) · rebond 0% (0/1)
   - **gap-up** (60 séances) :
      · −1.0% : fill 26% (15/60) · rebond 75% (11/15)
      · −2.0% : fill 13% (7/60) · rebond 45% (4/7)
      · −3.0% : fill 6% (3/60) · rebond 93% (2/3)
      · −4.0% : fill 4% (2/60) · rebond 0% (0/2)
      · −5.0% : fill 4% (2/60) · rebond 0% (0/2)
- **P(clôture VERTE) selon le drive 15min** (n=157) : 54% en base · 65% si les 15 1res min sont vertes (87 cas) · 39% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=157) : COUDE à **1:41** → P(séance verte=clôture>ouverture) 87% si début vert vs 18% si rouge (base 54% · écart 68 pts) ; prédictivité sature ensuite (plafond brut 230min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **87%** · continue >prix actuel 54% ; creux résiduel méd -0.66% (q20 -1.49%) → **SL/trailing à −1.49%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.07% / q75 +1.8% → **scale +1.07% / runner +1.8%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **18%** (continue à baisser 50%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.79%** (au-delà de la MAE q10 -2.79%), cible rebond +0.89% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=157) : retour [-2.95% .. +3.37%] · haut q95 +3.8% · bas q05 -3.55%
   - 60min (n=157) : retour [-3.01% .. +3.84%] · haut q95 +4.11% · bas q05 -3.64%
   - 2h (n=157) : retour [-3.68% .. +4.68%] · haut q95 +4.75% · bas q05 -4.46%
   - 4h (n=157) : retour [-4.01% .. +4.66%] · haut q95 +5.39% · bas q05 -5.0%
   - 6h (n=157) : retour [-3.97% .. +4.83%] · haut q95 +5.39% · bas q05 -5.37%
   - session (n=157) : retour [-3.98% .. +5.0%] · haut q95 +5.58% · bas q05 -5.37%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.4% des séances sont trend-up (mild 1.9% / strong 4.5%) · base = 10 séances trend-up (n_eff 7.1)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **34%**. Lecture précoce 30 min : signature présente → 15% vs absente 4% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.99% (p75 1.44% / p90 1.62%) · ~2.0 replis/séance, durée méd 75.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 40.57 min, n=23)
   - −1.0% → **62%** (reprise méd 61.25 min, n=10)
   - −1.5% → **58%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.62%** (p90, défaut prudent ; serré/agressif −1.44%) ; extension open→close méd +4.56% (q75 +6.33% / q95 +11.7%), MFE méd +5.12% / q90 +9.42%
   - Échelle scale-out : +5.12% (33%) / +6.79% (33%) / +9.42% (34%)
- **DÉSARMER** : repli > **−1.62%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=0) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +9.42% : P(retournement après) 0% (mèche méd 1.36%)
- **CONTEXTE** : la dernière heure tient les gains 74% du temps (retour médian dernière heure +0.89%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.72 · part idiosyncratique 0.28
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bearish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 23.7  _(survente)_
- **ADX** : 30.3  _(tendance etablie)_
- **MACD** : hist -1.992  _(pas de croisement recent)_
- **BB** : %B 0.18 · largeur 35.6%
- **ATR** : 9.81 (96.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.006  _(neutre)_
- **Vol ratio** : 0.5  _(volume atone)_
- **Choppiness** : 45.5  _(transition)_
- **MA** : MA20 176.61 · MA50 183.98 · MA200 153.83  _(prix < MA20)_
- **Dist MA** : MA20 -11.3% · MA50 -14.8% · MA200 +1.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (683306 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
