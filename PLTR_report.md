# PLTR

**Generated** : 2026-11-27T01:25:27.012385+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 6/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · $163.59  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (23 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot $163.59 (+0.9% vs entrée) · entrée $162.15 · stop $158.09 · T1 $166.75 · R/R 1.13  
> ↳ ¼-Kelly 0.023 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-25 : 163.59 · ATR Wilder 9.7 (5.93 %)_
- **Swing** : plage **152.13 → 143.55** (-7.0 % a -12.25 % sous la cloture, 0.89 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 147.56-151.06 (B) ; 140.96-145.06 (A). stop INDICATIF 131.25 (-8.57 % sous le bas ; sous le support 136.1-138.9 (- 0,5 ATR)).
- **Deep** : plage **143.55 → 123.28** (-12.25 % a -24.64 % sous la cloture, 2.09 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 140.96-145.06 (A) ; 125.25-142.28 (B) ; 136.1-138.9 (B) ; 131.15-135.96 (B). stop INDICATIF 113.04 (-8.31 % sous le bas ; sous le support 117.89-122.68 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (3.6 ATR sous le plus haut 20 s., RSI(2) 82.0 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 152.6-156.75 (B, -4.18 %) ; 147.56-151.06 (B, -7.66 %) ; 140.96-145.06 (A, -11.33 %) ; 125.25-142.28 (B, -13.03 %) ; 136.1-138.9 (B, -15.09 %) ; 131.15-135.96 (B, -16.89 %)
- Resistances reelles au-dessus : 170.77-175.41 (A, 4.39 %) ; 176.5-180.18 (A, 7.89 %) ; 182.43-187.28 (A, 11.52 %) ; 187.62-190.39 (A, 14.69 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.79 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.57 %)** : le gap seul le franchit 0.638 % des séances (8 fois sur 1254).
   - exécution **4.148 pt plus bas** dans le cas TYPIQUE (médiane), 8.08 au p90, **10.362 au pire**
   - perte réelle **11.982 %** en moyenne _(tirée par la queue)_, jusqu'à **17.932 %** — au lieu des 7.57 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0281 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 8 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.903 % | p01 -6.138 % | pire -17.932 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3119** [0.2464 ; 0.3836] _(largeur 13.7 pt, n_eff 173.1)_
   - swing : **0.381** [0.331 ; 0.433] _(largeur 10.2 pt, n_eff 345.7)_
   - deep : **0.3462** [0.2975 ; 0.3975] _(largeur 10.0 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.12 %** | CVaR **-8.46 %** | vol 4.27 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.4 % vs -13.82 % si l'on extrapolait par √5 _(rapport 0.97 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7565** (β de hausse 1.4496, asymétrie 1.2117) vs IWM — 603 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 152.7846 sur sr_based (0.73 ATR, 6.605 %) — p(stop avant cible) 0.4775 [0.43 ; 0.53], R/R 2.53, perte reelle 6.699 % (gap inclus), CVaR 7.502 %, EV 0.8526 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.26 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 13.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.73 ATR (stop 6.605 %) — p(stop avant cible) 0.4775 [0.43 ; 0.53], R/R 2.53, perte reelle 6.699 % (gap inclus), EV 0.8526 % — **REFUSE**
      - refuse : cible atteinte seulement 13.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_based a 1.5 ATR (stop 8.446 %) — p(stop avant cible) 0.3783 [0.33 ; 0.43], R/R 1.956, perte reelle 8.664 % (gap inclus), EV 0.7174 % — **REFUSE**
      - refuse : cible atteinte seulement 14.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🔴 support a 1.63 ATR (stop 11.692 %) — p(stop avant cible) 0.253 [0.21 ; 0.30], R/R 1.381, perte reelle 12.274 % (gap inclus), EV 0.4667 % — **REFUSE**
      - refuse : cible atteinte seulement 14.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.47 % > budget 12.00 %
      - ⚠ support DETECTE a 0.63 ATR du spot — compartiment <1, mesure a 48.1 % de casse (IC clusterise [0.449 ; 0.511] sur 1150 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ swing_based a 2.51 ATR (stop 16.669 %) — p(stop avant cible) 0.1291 [0.10 ; 0.17], R/R 1.008, perte reelle 16.81 % (gap inclus), EV 0.5109 % — **REFUSE**
      - refuse : cible atteinte seulement 14.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.03 % > budget 12.00 %
   - 🟢 support a 4.96 ATR (stop 30.453 %) — p(stop avant cible) 0.0025 [0.00 ; 0.01], R/R 0.535, perte reelle 31.678 % (gap inclus), EV 1.0091 % — **REFUSE**
      - refuse : cible atteinte seulement 14.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.63 % > budget 12.00 %
   - 🟢 support a 6.21 ATR (stop 37.495 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.451, perte reelle 37.539 % (gap inclus), EV 1.0204 % — **REFUSE**
      - refuse : cible atteinte seulement 14.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.34 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.408 %) — p(stop avant cible) 0.8782 [0.84 ; 0.91], R/R 11.784, perte reelle 1.438 % (gap inclus), EV 0.2175 % — **REFUSE**
      - refuse : cible atteinte seulement 5.1 % du temps (< 15 %) meme a 10 seances : le R/R de 11.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.878, borne haute 0.909 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ grid_snapped a 0.73 ATR (stop 5.778 %) — p(stop avant cible) 0.5316 [0.48 ; 0.58], R/R 2.881, perte reelle 5.883 % (gap inclus), EV 0.6472 % — **REFUSE**
      - refuse : cible atteinte seulement 11.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.532, borne haute 0.584 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🔴 grid_snapped a 1.63 ATR (stop 10.865 %) — p(stop avant cible) 0.2924 [0.25 ; 0.34], R/R 1.484, perte reelle 11.421 % (gap inclus), EV 0.3711 % — **REFUSE**
      - refuse : cible atteinte seulement 14.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.91 % > budget 12.00 %
   - ⚪ atr_grid a 2.25 ATR (stop 12.669 %) — p(stop avant cible) 0.2141 [0.17 ; 0.26], R/R 1.285, perte reelle 13.188 % (gap inclus), EV 0.525 % — **REFUSE**
      - refuse : cible atteinte seulement 14.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.81 % > budget 12.00 %
   - ⚪ grid_snapped a 2.51 ATR (stop 15.842 %) — p(stop avant cible) 0.1417 [0.11 ; 0.18], R/R 1.06, perte reelle 15.989 % (gap inclus), EV 0.5246 % — **REFUSE**
      - refuse : cible atteinte seulement 14.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.26 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 19.707 %) — p(stop avant cible) 0.073 [0.05 ; 0.10], R/R 0.856, perte reelle 19.806 % (gap inclus), EV 0.6738 % — **REFUSE**
      - refuse : cible atteinte seulement 14.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.85 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 22.522 %) — p(stop avant cible) 0.0415 [0.02 ; 0.07], R/R 0.748, perte reelle 22.671 % (gap inclus), EV 0.7604 % — **REFUSE**
      - refuse : cible atteinte seulement 14.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.27 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 25.338 %) — p(stop avant cible) 0.0053 [0.00 ; 0.02], R/R 0.649, perte reelle 26.12 % (gap inclus), EV 0.989 % — **REFUSE**
      - refuse : cible atteinte seulement 14.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.66 % > budget 12.00 %
   - 🟢 grid_snapped a 4.96 ATR (stop 29.625 %) — p(stop avant cible) 0.0026 [0.00 ; 0.01], R/R 0.552, perte reelle 30.725 % (gap inclus), EV 1.0086 % — **REFUSE**
      - refuse : cible atteinte seulement 14.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.59 % > budget 12.00 %
   - 🟢 grid_snapped a 6.21 ATR (stop 36.667 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.462, perte reelle 36.696 % (gap inclus), EV 1.0208 % — **REFUSE**
      - refuse : cible atteinte seulement 14.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.34 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 39.414 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.428, perte reelle 39.577 % (gap inclus), EV 1.0233 % — **REFUSE**
      - refuse : cible atteinte seulement 14.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.34 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 42.229 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.401, perte reelle 42.229 % (gap inclus), EV 1.0227 % — **REFUSE**
      - refuse : cible atteinte seulement 14.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.33 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 45.045 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.376, perte reelle 45.045 % (gap inclus), EV 1.0227 % — **REFUSE**
      - refuse : cible atteinte seulement 14.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.33 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 163.59, ATR14 9.2111 (5.631 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.363 ATR = 2.044 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.282 % | 163.1294 | 92.66 % | 95.37 % | 96.17 % | 96.97 % | 98.27 % | 98.67 % |
| 0.1 ATR | 0.563 % | 162.6689 | 84.91 % | 89.63 % | 91.43 % | 93.64 % | 95.23 % | 96.41 % |
| 0.15 ATR | 0.845 % | 162.2083 | 76.86 % | 83.79 % | 85.99 % | 89.8 % | 92.59 % | 94.26 % |
| 0.2 ATR | 1.126 % | 161.7478 | 69.22 % | 78.55 % | 81.85 % | 86.46 % | 90.36 % | 92.41 % |
| 0.25 ATR | 1.408 % | 161.2872 | 62.37 % | 73.82 % | 77.72 % | 82.83 % | 87.72 % | 90.77 % |
| 0.35 ATR | 1.971 % | 160.3661 | 51.31 % | 65.76 % | 71.27 % | 78.08 % | 83.76 % | 87.49 % |
| 0.5 ATR | 2.815 % | 158.9845 | 36.52 % | 53.07 % | 60.08 % | 69.19 % | 77.66 % | 82.67 % |
| 0.75 ATR | 4.223 % | 156.6817 | 19.52 % | 35.25 % | 44.96 % | 55.66 % | 66.8 % | 75.18 % |
| 1.0 ATR | 5.631 % | 154.3789 | 8.85 % | 23.16 % | 32.96 % | 44.24 % | 56.55 % | 65.95 % |
| 1.25 ATR | 7.038 % | 152.0762 | 4.43 % | 15.61 % | 23.39 % | 34.44 % | 46.5 % | 57.13 % |
| 1.5 ATR | 8.446 % | 149.7734 | 2.01 % | 10.57 % | 17.54 % | 27.07 % | 40.1 % | 52.41 % |
| 2.0 ATR | 11.261 % | 145.1679 | 0.7 % | 3.93 % | 9.38 % | 15.96 % | 29.14 % | 39.38 % |
| 2.5 ATR | 14.076 % | 140.5623 | 0.1 % | 1.41 % | 3.43 % | 9.49 % | 19.9 % | 29.54 % |
| 3.0 ATR | 16.892 % | 135.9568 | 0.0 % | 0.6 % | 1.71 % | 5.25 % | 13.5 % | 22.77 % |
| 4.0 ATR | 22.522 % | 126.7457 | 0.0 % | 0.0 % | 0.3 % | 1.52 % | 5.28 % | 13.13 % |
| 6.0 ATR | 33.784 % | 108.3236 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.51 % | 4.51 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.36 ATR | 0.41 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 0.97 ATR | 1.22 ATR |
| **2 s.** | 0.24 ATR | 0.54 ATR | 0.61 ATR | 0.80 ATR | 0.96 ATR | 1.10 ATR | 1.54 ATR | 1.92 ATR |
| **3 s.** | 0.29 ATR | 0.67 ATR | 0.75 ATR | 1.00 ATR | 1.21 ATR | 1.40 ATR | 1.96 ATR | 2.37 ATR |
| **5 s.** | 0.40 ATR | 0.87 ATR | 0.98 ATR | 1.30 ATR | 1.59 ATR | 1.82 ATR | 2.46 ATR | 3.07 ATR |
| **10 s.** | 0.56 ATR | 1.16 ATR | 1.31 ATR | 1.82 ATR | 2.22 ATR | 2.50 ATR | 3.43 ATR | 4.12 ATR |
| **20 s.** | 0.76 ATR | 1.59 ATR | 1.78 ATR | 2.32 ATR | 2.83 ATR | 3.29 ATR | 4.73 ATR | 5.89 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.414–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.815 %, prix 158.9849), p(touche) 36.52 % (en stress 81.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.613–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.223 %, prix 156.6816), p(touche) 35.25 % (en stress 93.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.749–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.223 %, prix 156.6816), p(touche) 44.96 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 51.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.983–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.631 %, prix 154.3782), p(touche) 44.24 % (en stress 100.0 %)  ✅ optimum identifie (85.6 % des re-echantillons)
- **10 seance(s)** : plage utile 1.309–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.446 %, prix 149.7732), p(touche) 40.1 % (en stress 100.0 %)  ✅ optimum identifie (87.2 % des re-echantillons)
- **20 seance(s)** : plage utile 1.784–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (14.076 %, prix 140.5631), p(touche) 29.54 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (93.5 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.028 | EV/share : $0.111 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 26 % | T2 — | T3 —
- Kelly (position) : f* 0.092 | ¼-Kelly 0.023 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 59.2 | bear 24.4 | side 16.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 149.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.882% → cible +2.84% / stop −2.5%, p_fill 74%, n_eff≈77.2) : P(cible|rempli) **24%** · **EV/risk +0.092** (×p_fill ; si rempli +0.31% du capital)
  - **swing** (entrée dip −1.939% → cible +6.42% / stop −5.742%, p_fill 53%, n_eff≈63.7) : P(cible|rempli) **35%** · **EV/risk +0.064** (×p_fill ; si rempli +0.70% du capital)
  - **deep** (entrée dip −2.994% → cible +18.301% / stop −9.15%, p_fill 49%, n_eff≈59.3) : P(cible|rempli) **19%** · **EV/risk +0.101** (×p_fill ; si rempli +1.88% du capital)
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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.76 · part idiosyncratique 0.24
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 56.4  _(momentum haussier)_
- **ADX** : 27.8  _(tendance etablie)_
- **MACD** : hist 0.036  _(bullish_recent)_
- **BB** : %B 0.44 · largeur 28.7%
- **ATR** : 9.21 (87.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.047  _(neutre)_
- **Vol ratio** : 0.83  _(volume normal)_
- **Choppiness** : 51.5  _(transition)_
- **MA** : MA20 166.31 · MA50 182.54 · MA200 154.3  _(prix < MA20)_
- **Dist MA** : MA20 -1.6% · MA50 -10.4% · MA200 +6.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (686179 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
