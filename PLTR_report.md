# PLTR

**Generated** : 2026-11-03T01:23:34.441748+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $178.62  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-05 — Bank of England — décision de taux (J-1 sess · macro taux)  
> ↳ spot $178.62 (+12.4% vs entrée) · entrée $158.89 · stop $149.36 · T1 $169.53 · R/R 1.12  
> ↳ ¼-Kelly 0.015 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +1.8 % ≠ (strike 187.5 − spot 178.62)/spot = +5.0 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -56 % hors [0,100] (R² max 0.97). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-02 : 178.62 · ATR Wilder 8.36 (4.68 %)_
- **Swing** : plage **168.93 → 161.64** (-5.42 % a -9.51 % sous la cloture, 0.87 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 165.08-168.91 (A) ; 160.39-164.55 (A). stop INDICATIF 151.5 (-6.27 % sous le bas ; sous le support 155.68-159.96 (- 0,5 ATR)).
- **Deep** : plage **161.64 → 146.89** (-9.51 % a -17.77 % sous la cloture, 1.76 ATR) — touchee 41 % → 15 % du temps en 20 seances ; supports reels dans la plage : 160.39-164.55 (A) ; 155.68-159.96 (B) ; 149.09-152.68 (B) ; 144.86-148.58 (B). stop INDICATIF 134.72 (-8.28 % sous le bas ; sous le support 138.9-142.34 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (COMBO) : 4.1 ATR sous le plus haut 20 s., RSI(2) 1.0. Limite **174.44** (seance suivante), stop catastrophe 140.98, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 169.42-172.0 (B, -3.71 %) ; 165.08-168.91 (A, -5.44 %) ; 160.39-164.55 (A, -7.88 %) ; 155.68-159.96 (B, -10.45 %) ; 149.09-152.68 (B, -14.52 %) ; 144.86-148.58 (B, -16.82 %)
- Resistances reelles au-dessus : 184.45-188.37 (A, 3.26 %) ; 190.0-190.39 (B, 6.37 %) ; 194.68-194.93 (A, 8.99 %) ; 198.88-202.63 (B, 11.34 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.71 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (16.38 %)** : le gap seul le franchit 0.08 % des séances (1 fois sur 1253).
   - exécution **1.552 pt plus bas** dans le cas TYPIQUE (médiane), 1.552 au p90, **1.552 au pire**
   - perte réelle **17.932 %** en moyenne _(tirée par la queue)_, jusqu'à **17.932 %** — au lieu des 16.38 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0012 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.861 % | p01 -6.139 % | pire -17.932 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2706** [0.2086 ; 0.3402] _(largeur 13.2 pt, n_eff 173.1)_
   - swing : **0.3267** [0.2789 ; 0.3774] _(largeur 9.9 pt, n_eff 345.7)_
   - deep : **0.2831** [0.2376 ; 0.3323] _(largeur 9.5 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.14 %** | CVaR **-8.42 %** | vol 4.26 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.31 % vs -13.82 % si l'on extrapolait par √5 _(rapport 0.963 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6964** (β de hausse 1.4174, asymétrie 1.1969) vs IWM — 605 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.788× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 173.8584 sur atr_grid (0.5 ATR, 2.666 %) — p(stop avant cible) 0.6551 [0.60 ; 0.70], R/R 2.478, perte reelle 2.758 % (gap inclus), CVaR 3.795 %, EV 0.4493 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.4533 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.655, borne haute 0.704 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 7.997 %) — p(stop avant cible) 0.3236 [0.28 ; 0.37], R/R 0.846, perte reelle 8.075 % (gap inclus), EV 0.831 % — **REFUSE**
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 3.87 ATR (stop 23.067 %) — p(stop avant cible) 0.0159 [0.01 ; 0.03], R/R 0.292, perte reelle 23.418 % (gap inclus), EV 1.1289 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.42 % > budget 12.00 %
   - 🟢 support a 6.38 ATR (stop 36.447 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 0.187, perte reelle 36.454 % (gap inclus), EV 1.2134 % — **REFUSE**
      - refuse : R/R 0.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.12 % > budget 12.00 %
   - 🟢 support a 7.59 ATR (stop 42.896 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.159, perte reelle 42.896 % (gap inclus), EV 1.2172 % — **REFUSE**
      - refuse : R/R 0.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.07 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.333 %) — p(stop avant cible) 0.816 [0.77 ; 0.85], R/R 4.993, perte reelle 1.369 % (gap inclus), EV 0.1336 % — **REFUSE**
      - refuse : p_stop_first 0.816, borne haute 0.854 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 2.666 %) — p(stop avant cible) 0.6551 [0.60 ; 0.70], R/R 2.478, perte reelle 2.758 % (gap inclus), EV 0.4493 % — **REFUSE**
      - refuse : p_stop_first 0.655, borne haute 0.704 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 0.75 ATR (stop 3.999 %) — p(stop avant cible) 0.5529 [0.50 ; 0.60], R/R 1.675, perte reelle 4.081 % (gap inclus), EV 0.5328 % — **REFUSE**
      - refuse : p_stop_first 0.553, borne haute 0.605 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.0 ATR (stop 5.332 %) — p(stop avant cible) 0.4598 [0.41 ; 0.51], R/R 1.266, perte reelle 5.399 % (gap inclus), EV 0.7201 % — **REFUSE**
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.25 ATR (stop 6.664 %) — p(stop avant cible) 0.3798 [0.33 ; 0.43], R/R 1.016, perte reelle 6.724 % (gap inclus), EV 0.8966 % — **REFUSE**
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.75 ATR (stop 9.33 %) — p(stop avant cible) 0.2661 [0.22 ; 0.31], R/R 0.727, perte reelle 9.397 % (gap inclus), EV 0.7963 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 10.663 %) — p(stop avant cible) 0.2358 [0.19 ; 0.28], R/R 0.631, perte reelle 10.829 % (gap inclus), EV 0.589 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 11.996 %) — p(stop avant cible) 0.1697 [0.13 ; 0.21], R/R 0.562, perte reelle 12.158 % (gap inclus), EV 0.8409 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.55 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 13.329 %) — p(stop avant cible) 0.1348 [0.10 ; 0.17], R/R 0.506, perte reelle 13.517 % (gap inclus), EV 0.8005 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.84 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 14.662 %) — p(stop avant cible) 0.1133 [0.08 ; 0.15], R/R 0.458, perte reelle 14.919 % (gap inclus), EV 0.7567 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.24 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 15.995 %) — p(stop avant cible) 0.0934 [0.07 ; 0.13], R/R 0.422, perte reelle 16.198 % (gap inclus), EV 0.8315 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.37 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 18.66 %) — p(stop avant cible) 0.0655 [0.04 ; 0.10], R/R 0.364, perte reelle 18.786 % (gap inclus), EV 0.8577 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.82 % > budget 12.00 %
   - ⚪ grid_snapped a 3.87 ATR (stop 22.219 %) — p(stop avant cible) 0.0218 [0.01 ; 0.04], R/R 0.303, perte reelle 22.563 % (gap inclus), EV 1.0952 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.00 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 23.992 %) — p(stop avant cible) 0.0062 [0.00 ; 0.02], R/R 0.278, perte reelle 24.607 % (gap inclus), EV 1.1733 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.55 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 26.658 %) — p(stop avant cible) 0.004 [0.00 ; 0.02], R/R 0.244, perte reelle 28.052 % (gap inclus), EV 1.1903 % — **REFUSE**
      - refuse : R/R 0.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.40 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 29.323 %) — p(stop avant cible) 0.0028 [0.00 ; 0.01], R/R 0.223, perte reelle 30.606 % (gap inclus), EV 1.2041 % — **REFUSE**
      - refuse : R/R 0.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.34 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 31.989 %) — p(stop avant cible) 0.0022 [0.00 ; 0.01], R/R 0.21, perte reelle 32.476 % (gap inclus), EV 1.2063 % — **REFUSE**
      - refuse : R/R 0.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.29 % > budget 12.00 %
   - 🟢 grid_snapped a 6.38 ATR (stop 35.599 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 0.192, perte reelle 35.599 % (gap inclus), EV 1.2145 % — **REFUSE**
      - refuse : R/R 0.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.12 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 37.321 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.183, perte reelle 37.39 % (gap inclus), EV 1.2149 % — **REFUSE**
      - refuse : R/R 0.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.08 % > budget 12.00 %
   - 🟢 grid_snapped a 7.59 ATR (stop 42.048 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.163, perte reelle 42.048 % (gap inclus), EV 1.2172 % — **REFUSE**
      - refuse : R/R 0.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.07 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 178.62, ATR14 9.5231 (5.332 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.362 ATR = 1.93 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.267 % | 178.1438 | 92.95 % | 95.46 % | 96.27 % | 97.07 % | 98.27 % | 98.67 % |
| 0.1 ATR | 0.533 % | 177.6677 | 85.1 % | 89.62 % | 91.52 % | 93.73 % | 95.22 % | 96.41 % |
| 0.15 ATR | 0.8 % | 177.1915 | 77.14 % | 83.87 % | 86.18 % | 89.99 % | 92.58 % | 94.25 % |
| 0.2 ATR | 1.066 % | 176.7154 | 69.28 % | 78.63 % | 82.04 % | 86.65 % | 90.35 % | 92.4 % |
| 0.25 ATR | 1.333 % | 176.2392 | 62.34 % | 73.69 % | 77.7 % | 83.01 % | 87.7 % | 90.76 % |
| 0.35 ATR | 1.866 % | 175.2869 | 51.16 % | 65.62 % | 71.24 % | 78.26 % | 83.74 % | 87.47 % |
| 0.5 ATR | 2.666 % | 173.8584 | 36.35 % | 52.82 % | 59.74 % | 68.86 % | 77.64 % | 82.65 % |
| 0.75 ATR | 3.999 % | 171.4776 | 19.44 % | 35.18 % | 44.5 % | 55.01 % | 66.36 % | 75.15 % |
| 1.0 ATR | 5.332 % | 169.0969 | 8.86 % | 22.88 % | 32.49 % | 43.58 % | 55.89 % | 65.91 % |
| 1.25 ATR | 6.664 % | 166.7161 | 4.43 % | 15.32 % | 23.21 % | 33.87 % | 45.93 % | 57.08 % |
| 1.5 ATR | 7.997 % | 164.3353 | 2.01 % | 10.38 % | 17.26 % | 26.39 % | 39.43 % | 52.36 % |
| 2.0 ATR | 10.663 % | 159.5737 | 0.7 % | 3.93 % | 9.28 % | 15.67 % | 28.66 % | 38.91 % |
| 2.5 ATR | 13.329 % | 154.8121 | 0.1 % | 1.41 % | 3.33 % | 9.2 % | 18.9 % | 28.95 % |
| 3.0 ATR | 15.995 % | 150.0506 | 0.0 % | 0.6 % | 1.61 % | 4.85 % | 12.5 % | 21.66 % |
| 4.0 ATR | 21.326 % | 140.5274 | 0.0 % | 0.0 % | 0.3 % | 1.42 % | 4.57 % | 11.7 % |
| 6.0 ATR | 31.989 % | 121.4811 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.51 % | 3.59 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.36 ATR | 0.41 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 0.97 ATR | 1.22 ATR |
| **2 s.** | 0.24 ATR | 0.54 ATR | 0.61 ATR | 0.79 ATR | 0.96 ATR | 1.09 ATR | 1.53 ATR | 1.92 ATR |
| **3 s.** | 0.29 ATR | 0.66 ATR | 0.74 ATR | 0.99 ATR | 1.20 ATR | 1.39 ATR | 1.96 ATR | 2.36 ATR |
| **5 s.** | 0.40 ATR | 0.86 ATR | 0.97 ATR | 1.28 ATR | 1.56 ATR | 1.80 ATR | 2.44 ATR | 2.98 ATR |
| **10 s.** | 0.56 ATR | 1.15 ATR | 1.29 ATR | 1.80 ATR | 2.19 ATR | 2.44 ATR | 3.31 ATR | 3.95 ATR |
| **20 s.** | 0.75 ATR | 1.59 ATR | 1.77 ATR | 2.30 ATR | 2.77 ATR | 3.17 ATR | 4.42 ATR | 5.65 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.412–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.611–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.999 %, prix 171.477), p(touche) 35.18 % (en stress 94.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.742–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.999 %, prix 171.477), p(touche) 44.5 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.969–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.332 %, prix 169.096), p(touche) 43.58 % (en stress 100.0 %)  ✅ optimum identifie (84.9 % des re-echantillons)
- **10 seance(s)** : plage utile 1.286–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.997 %, prix 164.3358), p(touche) 39.43 % (en stress 100.0 %)  ✅ optimum identifie (84.8 % des re-echantillons)
- **20 seance(s)** : plage utile 1.774–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (13.329 %, prix 154.8117), p(touche) 28.95 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (95.8 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.047 | EV/share : $0.451 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 32 % | T2 9 % | T3 4 %
- Kelly (position) : f* 0.059 | ¼-Kelly 0.015 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 33.1 | bear 5.0 | side 61.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 160.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=7, n_eff=6))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
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
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.69 · part idiosyncratique 0.31
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-05 — Bank of England — décision de taux (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-05 — Bank of England — décision de taux (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-05 — Bank of England — décision de taux (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 28.5  _(survente)_
- **ADX** : 20.7  _(pas de tendance nette)_
- **MACD** : hist -2.671  _(pas de croisement recent)_
- **BB** : %B -0.08 · largeur 16.0%
- **ATR** : 9.52 (94.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.045  _(neutre)_
- **Vol ratio** : 1.11  _(volume normal)_
- **Choppiness** : 55.1  _(transition)_
- **MA** : MA20 196.71 · MA50 186.88 · MA200 153.58  _(prix < MA20)_
- **Dist MA** : MA20 -9.2% · MA50 -4.4% · MA200 +16.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (746738 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
