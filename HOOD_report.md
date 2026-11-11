# HOOD

**Generated** : 2026-11-11T01:28:47.246157+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite normal · $81.35  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-0 sess · macro taux)  
> ↳ spot $81.35 (+3.3% vs entrée) · entrée $78.73 · stop $76.36 · T1 $81.82 · R/R 1.3  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -1.6 % ≠ (strike 82.0 − spot 81.35)/spot = +0.8 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-10 : 81.35 · ATR Wilder 5.32 (6.54 %)_
- **Swing** : plage **75.36 → 70.84** (-7.36 % a -12.92 % sous la cloture, 0.85 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 72.79-74.59 (A) ; 69.93-72.25 (A). stop INDICATIF 64.25 (-9.3 % sous le bas ; sous le support 66.91-69.22 (- 0,5 ATR)).
- **Deep** : plage **70.84 → 60.72** (-12.92 % a -25.36 % sous la cloture, 1.9 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 69.93-72.25 (A) ; 66.91-69.22 (A) ; 62.63-63.51 (B). stop INDICATIF 55.4 (-8.76 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 5.24 ATR sous le plus haut 20 s., RSI(2) 38.7. Limite **78.69** (seance suivante), stop catastrophe 57.42, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 78.93-79.57 (A, -2.19 %) ; 75.51-77.87 (A, -4.28 %) ; 72.79-74.59 (A, -8.31 %) ; 69.93-72.25 (A, -11.19 %) ; 66.91-69.22 (A, -14.91 %) ; 62.63-63.51 (B, -21.92 %)
- Resistances reelles au-dessus : 84.75-84.75 (C, 4.18 %) ; 88.6-90.7 (A, 8.91 %) ; 91.44-93.36 (A, 12.4 %) ; 94.4-96.59 (A, 16.04 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.34 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (13.25 %)** : le gap seul le franchit 0.16 % des séances (2 fois sur 1253).
   - exécution **2.705 pt plus bas** dans le cas TYPIQUE (médiane), 4.169 au p90, **4.535 au pire**
   - perte réelle **15.955 %** en moyenne _(tirée par la queue)_, jusqu'à **17.785 %** — au lieu des 13.25 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0043 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 2 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.488 % | p01 -6.925 % | pire -17.785 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2851** [0.2218 ; 0.3555] _(largeur 13.4 pt, n_eff 173.1)_
   - swing : **0.4598** [0.4078 ; 0.5125] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4191** [0.3679 ; 0.4716] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (33.4 pt), swing (42.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 780 séances)** : VaR **-6.19 %** | CVaR **-9.08 %** | vol 4.32 %/j
   - _fenêtre arrêtée : rupture de regime a 840 seances en arriere (volatilite 2.25 % contre 4.51 % aujourd'hui, rapport 0.50)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.41 % vs -14.64 % si l'on extrapolait par √5 _(rapport 0.984 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7892** (β de hausse 1.6328, asymétrie 1.0958) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.324× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 73.8462 sur atr_based (1.5 ATR, 9.224 %) — p(stop avant cible) 0.4857 [0.43 ; 0.54], R/R 2.457, perte reelle 9.699 % (gap inclus), CVaR 12.449 %, EV 0.2668 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.5793 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 9.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 12.45 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 9.224 %) — p(stop avant cible) 0.4857 [0.43 ; 0.54], R/R 2.457, perte reelle 9.699 % (gap inclus), EV 0.2668 % — **REFUSE**
      - refuse : cible atteinte seulement 9.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.45 % > budget 12.00 %
   - ⚪ swing_based a 1.37 ATR (stop 11.49 %) — p(stop avant cible) 0.368 [0.32 ; 0.42], R/R 1.965, perte reelle 12.128 % (gap inclus), EV 0.4189 % — **REFUSE**
      - refuse : cible atteinte seulement 9.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.72 % > budget 12.00 %
   - 🟢 support a 2.42 ATR (stop 17.992 %) — p(stop avant cible) 0.1253 [0.09 ; 0.16], R/R 1.302, perte reelle 18.297 % (gap inclus), EV 0.7292 % — **REFUSE**
      - refuse : cible atteinte seulement 9.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.76 % > budget 12.00 %
   - 🟢 support a 3.57 ATR (stop 25.005 %) — p(stop avant cible) 0.0281 [0.01 ; 0.05], R/R 0.933, perte reelle 25.537 % (gap inclus), EV 0.9166 % — **REFUSE**
      - refuse : cible atteinte seulement 9.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.95 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.537 %) — p(stop avant cible) 0.9174 [0.88 ; 0.94], R/R 14.068, perte reelle 1.694 % (gap inclus), EV -0.2175 % — **REFUSE**
      - refuse : cible atteinte seulement 3.4 % du temps (< 15 %) meme a 10 seances : le R/R de 14.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.917, borne haute 0.943 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.22 %) : P(cible) 3.4 % x 23.83 % + P(rien) 4.9 % x 10.80 % ne couvrent pas P(stop) 91.7 % x 1.69 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 3.075 %) — p(stop avant cible) 0.8018 [0.76 ; 0.84], R/R 7.119, perte reelle 3.347 % (gap inclus), EV 0.1175 % — **REFUSE**
      - refuse : cible atteinte seulement 5.9 % du temps (< 15 %) meme a 10 seances : le R/R de 7.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.802, borne haute 0.841 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 4.612 %) — p(stop avant cible) 0.7128 [0.66 ; 0.76], R/R 4.92, perte reelle 4.843 % (gap inclus), EV 0.2157 % — **REFUSE**
      - refuse : cible atteinte seulement 7.6 % du temps (< 15 %) meme a 10 seances : le R/R de 4.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.713, borne haute 0.759 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 6.149 %) — p(stop avant cible) 0.6326 [0.58 ; 0.68], R/R 3.664, perte reelle 6.502 % (gap inclus), EV 0.1811 % — **REFUSE**
      - refuse : cible atteinte seulement 8.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.633, borne haute 0.682 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ grid_snapped a 1.37 ATR (stop 10.254 %) — p(stop avant cible) 0.4277 [0.38 ; 0.48], R/R 2.215, perte reelle 10.757 % (gap inclus), EV 0.3621 % — **REFUSE**
      - refuse : cible atteinte seulement 9.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.92 % > budget 12.00 %
   - ⚪ atr_grid a 2.0 ATR (stop 12.299 %) — p(stop avant cible) 0.3258 [0.28 ; 0.38], R/R 1.838, perte reelle 12.962 % (gap inclus), EV 0.5541 % — **REFUSE**
      - refuse : cible atteinte seulement 9.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.29 % > budget 12.00 %
   - 🟢 grid_snapped a 2.42 ATR (stop 16.756 %) — p(stop avant cible) 0.164 [0.13 ; 0.21], R/R 1.394, perte reelle 17.092 % (gap inclus), EV 0.6573 % — **REFUSE**
      - refuse : cible atteinte seulement 9.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.86 % > budget 12.00 %
   - 🟢 grid_snapped a 3.57 ATR (stop 23.769 %) — p(stop avant cible) 0.0323 [0.02 ; 0.06], R/R 0.983, perte reelle 24.246 % (gap inclus), EV 0.9184 % — **REFUSE**
      - refuse : cible atteinte seulement 9.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.63 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 27.672 %) — p(stop avant cible) 0.0225 [0.01 ; 0.04], R/R 0.85, perte reelle 28.029 % (gap inclus), EV 0.9215 % — **REFUSE**
      - refuse : cible atteinte seulement 9.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.59 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 30.747 %) — p(stop avant cible) 0.0178 [0.01 ; 0.04], R/R 0.771, perte reelle 30.906 % (gap inclus), EV 0.9221 % — **REFUSE**
      - refuse : cible atteinte seulement 9.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.02 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 33.822 %) — p(stop avant cible) 0.003 [0.00 ; 0.01], R/R 0.698, perte reelle 34.127 % (gap inclus), EV 1.0197 % — **REFUSE**
      - refuse : cible atteinte seulement 9.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.26 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 36.897 %) — p(stop avant cible) 0.0016 [0.00 ; 0.01], R/R 0.645, perte reelle 36.964 % (gap inclus), EV 1.0334 % — **REFUSE**
      - refuse : cible atteinte seulement 9.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.00 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 39.971 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.596, perte reelle 39.971 % (gap inclus), EV 1.0488 % — **REFUSE**
      - refuse : cible atteinte seulement 9.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.71 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 43.046 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.554, perte reelle 43.046 % (gap inclus), EV 1.0488 % — **REFUSE**
      - refuse : cible atteinte seulement 9.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.71 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 46.121 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.517, perte reelle 46.121 % (gap inclus), EV 1.0488 % — **REFUSE**
      - refuse : cible atteinte seulement 9.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.71 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 49.195 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.484, perte reelle 49.195 % (gap inclus), EV 1.0488 % — **REFUSE**
      - refuse : cible atteinte seulement 9.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.71 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 81.35, ATR14 5.0026 (6.149 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.371 ATR = 2.281 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.307 % | 81.0999 | 93.05 % | 95.26 % | 96.17 % | 96.66 % | 97.15 % | 98.05 % |
| 0.1 ATR | 0.615 % | 80.8497 | 85.4 % | 90.62 % | 92.33 % | 93.93 % | 94.82 % | 96.41 % |
| 0.15 ATR | 0.922 % | 80.5996 | 77.74 % | 85.69 % | 88.4 % | 90.8 % | 92.78 % | 95.07 % |
| 0.2 ATR | 1.23 % | 80.3495 | 71.3 % | 80.44 % | 84.26 % | 87.56 % | 90.55 % | 93.22 % |
| 0.25 ATR | 1.537 % | 80.0994 | 64.25 % | 74.7 % | 79.62 % | 84.02 % | 87.91 % | 90.86 % |
| 0.35 ATR | 2.152 % | 79.5991 | 52.17 % | 65.62 % | 72.45 % | 78.36 % | 83.84 % | 87.99 % |
| 0.5 ATR | 3.075 % | 78.8487 | 36.76 % | 53.63 % | 61.65 % | 69.36 % | 77.03 % | 82.34 % |
| 0.75 ATR | 4.612 % | 77.5981 | 19.34 % | 36.19 % | 46.42 % | 56.42 % | 66.26 % | 73.2 % |
| 1.0 ATR | 6.149 % | 76.3474 | 9.26 % | 23.49 % | 33.6 % | 44.89 % | 55.79 % | 65.81 % |
| 1.25 ATR | 7.687 % | 75.0968 | 4.83 % | 14.82 % | 23.01 % | 34.78 % | 48.27 % | 59.55 % |
| 1.5 ATR | 9.224 % | 73.8462 | 2.52 % | 10.08 % | 16.65 % | 27.7 % | 41.57 % | 53.9 % |
| 2.0 ATR | 12.299 % | 71.3449 | 0.4 % | 3.73 % | 7.16 % | 15.47 % | 30.79 % | 44.05 % |
| 2.5 ATR | 15.374 % | 68.8436 | 0.0 % | 1.41 % | 3.73 % | 8.19 % | 22.26 % | 34.91 % |
| 3.0 ATR | 18.448 % | 66.3423 | 0.0 % | 0.5 % | 2.12 % | 4.85 % | 15.45 % | 26.9 % |
| 4.0 ATR | 24.598 % | 61.3397 | 0.0 % | 0.3 % | 0.61 % | 1.82 % | 6.0 % | 15.09 % |
| 6.0 ATR | 36.897 % | 51.3346 | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.32 % | 4.93 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.37 ATR | 0.42 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 0.98 ATR | 1.24 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.62 ATR | 0.81 ATR | 0.97 ATR | 1.10 ATR | 1.51 ATR | 1.90 ATR |
| **3 s.** | 0.31 ATR | 0.69 ATR | 0.78 ATR | 1.01 ATR | 1.20 ATR | 1.37 ATR | 1.85 ATR | 2.31 ATR |
| **5 s.** | 0.41 ATR | 0.89 ATR | 1.00 ATR | 1.31 ATR | 1.61 ATR | 1.81 ATR | 2.38 ATR | 2.98 ATR |
| **10 s.** | 0.55 ATR | 1.19 ATR | 1.37 ATR | 1.90 ATR | 2.34 ATR | 2.67 ATR | 3.58 ATR | 4.43 ATR |
| **20 s.** | 0.70 ATR | 1.70 ATR | 1.95 ATR | 2.62 ATR | 3.16 ATR | 3.58 ATR | 5.00 ATR | 5.99 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.42 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.624–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.612 %, prix 77.5981), p(touche) 36.19 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.778–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.149 %, prix 76.3478), p(touche) 33.6 % (en stress 91.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.998–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.149 %, prix 76.3478), p(touche) 44.89 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.372–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.224 %, prix 73.8463), p(touche) 41.57 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.952–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (12.299 %, prix 71.3448), p(touche) 44.05 % (en stress 97.96 %)  ✅ optimum identifie (61.5 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.009 | EV/share : $-0.020 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 23 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.1 | bear 43.4 | side 43.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.227% → cible +3.934% / stop −3.0%, p_fill 29%, n_eff≈31.4) : P(cible|rempli) **11%** · **EV/risk -0.046** (×p_fill ; si rempli -0.48% du capital)
  - **swing** (entrée dip −7.101% → cible +8.265% / stop −6.619%, p_fill 16%, n_eff≈18.4) : P(cible|rempli) **41%** · **EV/risk +0.018** (×p_fill ; si rempli +0.71% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=11, n_eff=11))
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
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.66 · part idiosyncratique 0.34
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-11 — MSCI — décision d’exclusion potentielle de Strategy (MSTR) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 25.1  _(survente)_
- **ADX** : 30.5  _(tendance etablie)_
- **MACD** : hist -0.667  _(pas de croisement recent)_
- **BB** : %B 0.17 · largeur 33.8%
- **ATR** : 5.0 (32.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.041  _(neutre)_
- **Vol ratio** : 0.59  _(volume atone)_
- **Choppiness** : 37.7  _(marche directionnel)_
- **MA** : MA20 91.43 · MA50 105.08 · MA200 91.74  _(prix < MA20)_
- **Dist MA** : MA20 -11.0% · MA50 -22.6% · MA200 -11.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (697796 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
