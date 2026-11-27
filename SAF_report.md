# SAF

**Generated** : 2026-11-27T01:09:35.470305+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €299.80  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 16/125 fenêtres (p_fill pondéré 14 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot €299.80 (+2.8% vs entrée) · entrée €291.59 · stop €268.26 · T1 €296.23 · R/R 0.2  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -57 % hors [0,100] (R² max 0.84). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-26 : 299.8 · ATR Wilder 9.6 (3.2 %)_
- **Swing** : plage **288.17 → 281.09** (-3.88 % a -6.24 % sous la cloture, 0.74 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 283.02-287.1 (B). stop INDICATIF 271.69 (-3.34 % sous le bas ; sous le support 276.49-280.94 (- 0,5 ATR)).
- **Deep** : plage **281.09 → 259.08** (-6.24 % a -13.58 % sous la cloture, 2.29 ATR) — touchee 41 % → 15 % du temps en 20 seances ; supports reels dans la plage : 276.49-280.94 (B) ; 270.56-273.87 (B) ; 265.22-269.9 (A) ; 259.68-263.34 (A). stop INDICATIF 248.95 (-3.91 % sous le bas ; sous le support 253.75-257.96 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (1.96 ATR sous le plus haut 20 s., RSI(2) 64.2 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 289.55-291.92 (B, -2.63 %) ; 283.02-287.1 (B, -4.24 %) ; 276.49-280.94 (B, -6.29 %) ; 270.56-273.87 (B, -8.65 %) ; 265.22-269.9 (A, -9.97 %) ; 259.68-263.34 (A, -12.16 %)
- Resistances reelles au-dessus : 306.9-310.9 (A, 2.37 %) ; 312.29-316.9 (A, 4.17 %) ; 317.14-320.7 (A, 5.78 %) ; 322.1-326.8 (A, 7.44 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.62 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (9.12 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1280).
   - exécution **0.866 pt plus bas** dans le cas TYPIQUE (médiane), 0.866 au p90, **0.866 au pire**
   - perte réelle **9.986 %** en moyenne _(tirée par la queue)_, jusqu'à **9.986 %** — au lieu des 9.12 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0007 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.397 % | p01 -2.356 % | pire -9.986 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0** [0.0 ; 0.0144] _(largeur 1.4 pt, n_eff 173.1)_
   - swing : **0.3342** [0.286 ; 0.3851] _(largeur 9.9 pt, n_eff 345.8)_
   - deep : **0.3261** [0.2783 ; 0.3768] _(largeur 9.8 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 13.2 observations effectives », dont la borne haute a 95 % vaut environ 22.7 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (47.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-3.23 %** | CVaR **-4.54 %** | vol 2.24 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 1.24 % contre 2.00 % aujourd'hui, rapport 0.62)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.61 % vs -6.2 % si l'on extrapolait par √5 _(rapport 0.904 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3306** (β de hausse 1.3548, asymétrie 0.9822) vs FCHI — 623 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 288.2107 sur atr_grid (1.25 ATR, 3.866 %) — p(stop avant cible) 0.4255 [0.37 ; 0.48], R/R 3.976, perte reelle 4.129 % (gap inclus), CVaR 5.74 %, EV 0.7205 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.8773 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.639 %) — p(stop avant cible) 0.3665 [0.32 ; 0.42], R/R 3.369, perte reelle 4.872 % (gap inclus), EV 0.6711 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ swing_based a 3.42 ATR (stop 12.287 %) — p(stop avant cible) 0.0718 [0.05 ; 0.10], R/R 1.313, perte reelle 12.496 % (gap inclus), EV 0.3274 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.59 % > budget 12.00 %
   - 🟢 support a 4.33 ATR (stop 15.076 %) — p(stop avant cible) 0.0196 [0.01 ; 0.04], R/R 1.019, perte reelle 16.104 % (gap inclus), EV 0.3006 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.18 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.773 %) — p(stop avant cible) 0.8512 [0.81 ; 0.89], R/R 20.13, perte reelle 0.815 % (gap inclus), EV 0.3613 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 20.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.851, borne haute 0.886 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 1.546 %) — p(stop avant cible) 0.731 [0.68 ; 0.78], R/R 10.17, perte reelle 1.614 % (gap inclus), EV 0.5081 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 10.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.731, borne haute 0.776 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 2.319 %) — p(stop avant cible) 0.6233 [0.57 ; 0.67], R/R 6.771, perte reelle 2.424 % (gap inclus), EV 0.701 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 6.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.623, borne haute 0.673 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 3.093 %) — p(stop avant cible) 0.5165 [0.46 ; 0.57], R/R 5.155, perte reelle 3.184 % (gap inclus), EV 0.7835 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 5.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.516, borne haute 0.569 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.25 ATR (stop 3.866 %) — p(stop avant cible) 0.4255 [0.37 ; 0.48], R/R 3.976, perte reelle 4.129 % (gap inclus), EV 0.7205 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 1.75 ATR (stop 5.412 %) — p(stop avant cible) 0.3141 [0.27 ; 0.36], R/R 2.916, perte reelle 5.629 % (gap inclus), EV 0.6724 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 6.185 %) — p(stop avant cible) 0.2878 [0.24 ; 0.34], R/R 2.587, perte reelle 6.345 % (gap inclus), EV 0.5973 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 6.958 %) — p(stop avant cible) 0.2347 [0.19 ; 0.28], R/R 2.326, perte reelle 7.055 % (gap inclus), EV 0.5202 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 7.731 %) — p(stop avant cible) 0.1873 [0.15 ; 0.23], R/R 2.096, perte reelle 7.831 % (gap inclus), EV 0.4902 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 8.504 %) — p(stop avant cible) 0.1412 [0.11 ; 0.18], R/R 1.9, perte reelle 8.639 % (gap inclus), EV 0.503 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 9.278 %) — p(stop avant cible) 0.1141 [0.08 ; 0.15], R/R 1.738, perte reelle 9.444 % (gap inclus), EV 0.4528 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 3.42 ATR (stop 11.52 %) — p(stop avant cible) 0.0902 [0.06 ; 0.12], R/R 1.408, perte reelle 11.661 % (gap inclus), EV 0.3037 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 grid_snapped a 4.33 ATR (stop 14.309 %) — p(stop avant cible) 0.0292 [0.02 ; 0.05], R/R 1.081, perte reelle 15.19 % (gap inclus), EV 0.2987 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.13 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 17.009 %) — p(stop avant cible) 0.0048 [0.00 ; 0.02], R/R 0.836, perte reelle 19.641 % (gap inclus), EV 0.3267 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.66 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 18.555 %) — p(stop avant cible) 0.0037 [0.00 ; 0.01], R/R 0.804, perte reelle 20.417 % (gap inclus), EV 0.3364 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.55 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 20.101 %) — p(stop avant cible) 0.0037 [0.00 ; 0.01], R/R 0.788, perte reelle 20.821 % (gap inclus), EV 0.3348 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.58 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 21.648 %) — p(stop avant cible) 0.0026 [0.00 ; 0.01], R/R 0.752, perte reelle 21.821 % (gap inclus), EV 0.34 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.49 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 23.194 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 0.708, perte reelle 23.194 % (gap inclus), EV 0.3496 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.30 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 24.74 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.663, perte reelle 24.74 % (gap inclus), EV 0.354 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.20 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 299.8, ATR14 9.2714 (3.093 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.347 ATR = 1.073 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.155 % | 299.3364 | 89.41 % | 92.64 % | 93.71 % | 95.57 % | 96.24 % | 97.1 % |
| 0.1 ATR | 0.309 % | 298.8728 | 81.67 % | 87.34 % | 89.29 % | 91.44 % | 93.47 % | 95.0 % |
| 0.15 ATR | 0.464 % | 298.4093 | 75.59 % | 83.91 % | 86.74 % | 89.17 % | 91.69 % | 93.31 % |
| 0.2 ATR | 0.619 % | 297.9457 | 68.33 % | 78.41 % | 82.91 % | 85.53 % | 88.92 % | 91.51 % |
| 0.25 ATR | 0.773 % | 297.4821 | 61.27 % | 73.7 % | 79.08 % | 83.37 % | 87.54 % | 90.51 % |
| 0.35 ATR | 1.082 % | 296.555 | 49.71 % | 63.79 % | 70.14 % | 77.36 % | 82.89 % | 87.61 % |
| 0.5 ATR | 1.546 % | 295.1643 | 35.39 % | 52.4 % | 59.63 % | 69.39 % | 76.66 % | 82.32 % |
| 0.75 ATR | 2.319 % | 292.8464 | 20.78 % | 35.62 % | 43.22 % | 54.13 % | 64.09 % | 72.53 % |
| 1.0 ATR | 3.093 % | 290.5286 | 10.1 % | 24.34 % | 33.1 % | 43.31 % | 55.29 % | 64.24 % |
| 1.25 ATR | 3.866 % | 288.2107 | 4.51 % | 15.9 % | 24.46 % | 34.06 % | 47.77 % | 57.54 % |
| 1.5 ATR | 4.639 % | 285.8928 | 2.35 % | 10.4 % | 16.9 % | 25.69 % | 39.56 % | 49.75 % |
| 2.0 ATR | 6.185 % | 281.2571 | 1.08 % | 4.71 % | 7.96 % | 16.24 % | 28.78 % | 40.46 % |
| 2.5 ATR | 7.731 % | 276.6214 | 0.2 % | 1.57 % | 3.93 % | 9.25 % | 19.88 % | 31.27 % |
| 3.0 ATR | 9.278 % | 271.9857 | 0.0 % | 0.98 % | 2.36 % | 6.2 % | 13.55 % | 24.78 % |
| 4.0 ATR | 12.37 % | 262.7143 | 0.0 % | 0.29 % | 0.79 % | 1.48 % | 5.44 % | 12.89 % |
| 6.0 ATR | 18.555 % | 244.1714 | 0.0 % | 0.1 % | 0.2 % | 0.39 % | 1.19 % | 3.9 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.54 ATR | 0.68 ATR | 0.77 ATR | 1.00 ATR | 1.23 ATR |
| **2 s.** | 0.24 ATR | 0.54 ATR | 0.61 ATR | 0.81 ATR | 0.98 ATR | 1.13 ATR | 1.53 ATR | 1.98 ATR |
| **3 s.** | 0.30 ATR | 0.65 ATR | 0.72 ATR | 1.00 ATR | 1.23 ATR | 1.40 ATR | 1.89 ATR | 2.37 ATR |
| **5 s.** | 0.39 ATR | 0.84 ATR | 0.96 ATR | 1.28 ATR | 1.54 ATR | 1.80 ATR | 2.45 ATR | 3.25 ATR |
| **10 s.** | 0.53 ATR | 1.18 ATR | 1.33 ATR | 1.80 ATR | 2.21 ATR | 2.49 ATR | 3.44 ATR | 4.21 ATR |
| **20 s.** | 0.69 ATR | 1.49 ATR | 1.76 ATR | 2.41 ATR | 2.98 ATR | 3.40 ATR | 4.64 ATR | 5.75 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.399 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.61–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.319 %, prix 292.8476), p(touche) 35.62 % (en stress 85.29 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 21.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.723–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.319 %, prix 292.8476), p(touche) 43.22 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.961–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.093 %, prix 290.5272), p(touche) 43.31 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.334–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (4.639 %, prix 285.8923), p(touche) 39.56 % (en stress 99.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.756–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.185 %, prix 281.2574), p(touche) 40.46 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 53.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.031 | EV/share : €-0.714 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 5 % | T3 1 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 9.2 | bear 5.8 | side 85.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈60.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.739% → cible +1.59% / stop −8.0%, p_fill 14%, n_eff≈13.2) : P(cible|rempli) **35%** · **EV/risk -0.001** (×p_fill ; si rempli -0.07% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→73% · +1.0%→50% · +2.0%→21% · +3.0%→6% · +5.0%→1% · +8.0%→1%
- Range intraday médian 2.44% (p90 3.66%) · excursion haute méd. +1.01% / basse méd. −0.95%
- Profil de vol intra : ouverture 1.464% vs midi 0.52% vs clôture 0.69% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 41% · recovery-V 14%)_
- **Régime intraday** : **chop** _(efficiency 0.108 ; mean-reverting — autocorr -0.041)_ ; drift intra méd. -0.714% ; recovery-V 9%
- **σ réalisé intraday** 1.704% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 70% / whipsaw 29%
- POC intraday (dernière séance, temps-au-prix) : 275.7587 (VA 272.0312–278.4212 ; dernier close 270.9)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 15% · rebond 30% · **stop −0.98%** sous le fill (sous le bruit) · cible +0.56% · R/R 0.57 (high win-rate)
- Gaps overnight (n=159) : méd. 0.15% · baisse 41% (gap-down >1% 4% · >2% 2%)
- Excursion ouverture 5min (n=160) : bas méd −0.42% (p90 −1.66%) · haut méd +0.23% · range méd 0.85%
- Excursion ouverture 15min (n=160) : bas méd −0.45% (p90 −1.94%) · haut méd +0.35% · range méd 1.04%
- Excursion ouverture 30min (n=160) : bas méd −0.54% (p90 −2.04%) · haut méd +0.51% · range méd 1.21%
- Excursion ouverture 60min (n=160) : bas méd −0.62% (p90 −2.06%) · haut méd +0.52% · range méd 1.48%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 271.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 50% · séance 63% (95/159) · gap 13% · délai 0.4min · rebond 34% (36/95) (MFE +0.77%)
   - −1.0% : fill 30min 30% · séance 50% (77/159) · gap 4% · délai 13.7min · rebond 43% (36/77) (MFE +0.61%)
   - −1.5% : fill 30min 18% · séance 34% (50/159) · gap 2% · délai 15.5min · rebond 32% (19/50) (MFE +0.66%)
   - −2.0% : fill 30min 10% · séance 28% (40/159) · gap 2% · délai 101.1min · rebond 36% (15/40) (MFE +0.73%)
   - −3.0% : fill 30min 2% · séance 15% (19/159) · gap 2% · délai 391.3min · rebond 30% (7/19) (MFE +0.56%)
   - −4.0% : fill 30min 2% · séance 3% (4/159) · gap 0% · délai 37.1min · rebond 24% (2/4) (MFE +0.38%)
   - −5.0% : fill 30min 2% · séance 2% (2/159) · gap 0% · délai 55.7min · rebond 0% (0/2) (MFE +0.11%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.25% (p90 −0.76%) → stop au-delà de −0.63% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.23% (p90 −0.64%) → stop au-delà de −0.43% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.09% (p90 −1.01%) → stop au-delà de −0.68% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=200 jambes) : jambe baissière méd −1.06% (p90 −2.63%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (27 séances) :
      · −1.0% : fill 82% (22/27) · rebond 28% (7/22)
      · −2.0% : fill 56% (15/27) · rebond 14% (5/15)
      · −3.0% : fill 37% (8/27) · rebond 26% (3/8)
      · −4.0% : fill 11% (2/27) · rebond 21% (1/2)
      · −5.0% : fill 9% (1/27) · rebond 0% (0/1)
   - **flat** (51 séances) :
      · −1.0% : fill 55% (28/51) · rebond 41% (14/28)
      · −2.0% : fill 30% (13/51) · rebond 45% (4/13)
      · −3.0% : fill 12% (5/51) · rebond 13% (1/5)
      · −4.0% : fill 0% (0/51) · rebond 0% (0/0)
      · −5.0% : fill 0% (0/51) · rebond 0% (0/0)
   - **gap-up** (81 séances) :
      · −1.0% : fill 31% (27/81) · rebond 65% (15/27)
      · −2.0% : fill 11% (12/81) · rebond 71% (6/12)
      · −3.0% : fill 7% (6/81) · rebond 67% (3/6)
      · −4.0% : fill 1% (2/81) · rebond 38% (1/2)
      · −5.0% : fill 0% (1/81) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 69% si les 15 1res min sont vertes (77 cas) · 23% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **41min** → P(séance verte=clôture>ouverture) 77% si début vert vs 16% si rouge (base 45% · écart 61 pts) ; prédictivité sature ensuite (plafond brut 39min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **77%** · continue >prix actuel 56% ; creux résiduel méd -0.74% (q20 -1.2%) → **SL/trailing à −1.2%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.91% / q75 +1.31% → **scale +0.91% / runner +1.31%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **16%** (continue à baisser 60%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.32%** (au-delà de la MAE q10 -2.32%), cible rebond +0.8% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.73% .. +1.21%] · haut q95 +1.77% · bas q05 -2.22%
   - 60min (n=160) : retour [-1.91% .. +1.59%] · haut q95 +1.82% · bas q05 -2.29%
   - 2h (n=160) : retour [-2.25% .. +1.74%] · haut q95 +2.19% · bas q05 -2.59%
   - 4h (n=160) : retour [-2.83% .. +1.83%] · haut q95 +2.3% · bas q05 -3.03%
   - 6h (n=160) : retour [-2.4% .. +2.06%] · haut q95 +2.56% · bas q05 -3.94%
   - session (n=160) : retour [-3.08% .. +1.92%] · haut q95 +2.83% · bas q05 -3.95%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.69%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.38 · part idiosyncratique 0.62
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 52.9  _(neutre)_
- **ADX** : 16.8  _(pas de tendance nette)_
- **MACD** : hist 0.067  _(pas de croisement recent)_
- **BB** : %B 0.51 · largeur 13.3%
- **ATR** : 9.27 (57.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.196  _(distribution)_
- **Vol ratio** : 0.1  _(volume atone)_
- **Choppiness** : 58.5  _(transition)_
- **MA** : MA20 299.54 · MA50 308.88 · MA200 314.44  _(prix > MA20)_
- **Dist MA** : MA20 +0.1% · MA50 -2.9% · MA200 -4.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (685368 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
