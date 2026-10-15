# SMCI

**Generated** : 2026-10-15T00:21:33.590596+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $35.80  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 35/121 fenêtres (p_fill pondéré 28 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot $35.80 (+6.0% vs entrée) · entrée $33.78 · stop $31.43 · T1 $36.41 · R/R 1.12  
> ↳ ¼-Kelly 0.014 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +2.4 % ≠ (strike 40.0 − spot 35.80)/spot = +11.7 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -221 % hors [0,100] (R² max 0.93). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-14 : 35.8 · ATR Wilder 2.39 (6.68 %)_
- **Swing** : plage **32.88 → 31.14** (-8.16 % a -13.01 % sous la cloture, 0.73 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 31.11-33.94 (B) ; 32.59-33.64 (B). stop INDICATIF 28.65 (-7.99 % sous le bas ; sous le support 29.85-31.03 (- 0,5 ATR)).
- **Deep** : plage **31.14 → 25.94** (-13.01 % a -27.55 % sous la cloture, 2.18 ATR) — touchee 44 % → 15 % du temps en 20 seances ; supports reels dans la plage : 31.11-33.94 (B) ; 29.85-31.03 (B) ; 28.5-29.68 (B) ; 26.67-27.75 (B) ; 25.41-26.06 (A). stop INDICATIF 22.99 (-11.34 % sous le bas ; sous le support 24.19-25.13 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (COMBO) : 4.17 ATR sous le plus haut 20 s., RSI(2) 1.3. Limite **34.6** (seance suivante), stop catastrophe 25.04, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 33.86-34.98 (A, -2.29 %) ; 31.11-33.94 (B, -5.2 %) ; 32.59-33.64 (B, -6.03 %) ; 29.85-31.03 (B, -13.32 %) ; 28.5-29.68 (B, -17.09 %) ; 26.67-27.75 (B, -22.49 %)
- Resistances reelles au-dessus : 36.8-37.85 (A, 2.79 %) ; 38.28-39.47 (A, 6.93 %) ; 39.52-40.13 (A, 10.39 %) ; 40.74-41.53 (A, 13.8 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.90 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.2 %)** : le gap seul le franchit 0.798 % des séances (10 fois sur 1253).
   - exécution **3.705 pt plus bas** dans le cas TYPIQUE (médiane), 14.879 au p90, **16.851 au pire**
   - perte réelle **18.539 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 12.2 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0506 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 10 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.795 % | p01 -10.307 % | pire -29.051 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.435** [0.3627 ; 0.5094] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4029** [0.3522 ; 0.4552] _(largeur 10.3 pt, n_eff 345.7)_
   - deep : **0.3557** [0.3066 ; 0.4072] _(largeur 10.1 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (26.4 pt), swing (32.3 pt), deep (32.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.63 %** | CVaR **-12.3 %** | vol 5.82 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 3.67 % contre 6.50 % aujourd'hui, rapport 0.56)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.91 % vs -16.7 % si l'on extrapolait par √5 _(rapport 1.012 ; < 1 = le √5 surestime)_
- **β de baisse : 1.5217** (β de hausse 1.2181, asymétrie 1.2492) vs IWM — 606 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.759× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 32.8652 sur atr_grid (1.25 ATR, 8.198 %) — p(stop avant cible) 0.4611 [0.41 ; 0.51], R/R 2.937, perte reelle 9.576 % (gap inclus), CVaR 20.506 %, EV 1.9315 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.7297 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : R/R 2.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 20.51 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 23 des 23 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 27.9 % de la queue et il ne reste que 13.84 EUR a partager. Prix du risque 0.004 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 9.837 %) — p(stop avant cible) 0.3947 [0.34 ; 0.45], R/R 2.46, perte reelle 11.437 % (gap inclus), EV 1.8657 % — **REFUSE**
      - refuse : R/R 2.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.22 % > budget 12.00 %
   - ⚪ sr_based a 1.66 ATR (stop 14.263 %) — p(stop avant cible) 0.2199 [0.18 ; 0.27], R/R 1.714, perte reelle 16.409 % (gap inclus), EV 2.5117 % — **REFUSE**
      - refuse : R/R 1.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.56 % > budget 12.00 %
   - 🟢 support a 3.45 ATR (stop 25.956 %) — p(stop avant cible) 0.0828 [0.06 ; 0.12], R/R 1.042, perte reelle 27.001 % (gap inclus), EV 2.822 % — **REFUSE**
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.69 % > budget 12.00 %
   - 🟢 support a 4.43 ATR (stop 32.38 %) — p(stop avant cible) 0.0657 [0.04 ; 0.10], R/R 0.865, perte reelle 32.52 % (gap inclus), EV 2.4987 % — **REFUSE**
      - refuse : R/R 0.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.56 % > budget 12.00 %
   - 🟢 support a 5.29 ATR (stop 38.051 %) — p(stop avant cible) 0.0359 [0.02 ; 0.06], R/R 0.739, perte reelle 38.084 % (gap inclus), EV 2.4503 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.48 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.64 %) — p(stop avant cible) 0.9006 [0.87 ; 0.93], R/R 14.995, perte reelle 1.876 % (gap inclus), EV 0.3374 % — **REFUSE**
      - refuse : cible atteinte seulement 5.2 % du temps (< 15 %) meme a 10 seances : le R/R de 15.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.901, borne haute 0.929 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 3.279 %) — p(stop avant cible) 0.7848 [0.74 ; 0.83], R/R 7.473, perte reelle 3.764 % (gap inclus), EV 0.7759 % — **REFUSE**
      - refuse : cible atteinte seulement 9.4 % du temps (< 15 %) meme a 10 seances : le R/R de 7.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.785, borne haute 0.826 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 4.919 %) — p(stop avant cible) 0.686 [0.64 ; 0.73], R/R 4.983, perte reelle 5.645 % (gap inclus), EV 0.9989 % — **REFUSE**
      - refuse : cible atteinte seulement 11.8 % du temps (< 15 %) meme a 10 seances : le R/R de 4.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.686, borne haute 0.733 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 14.31 % > budget 12.00 %
   - ⚪ atr_grid a 1.0 ATR (stop 6.558 %) — p(stop avant cible) 0.5758 [0.52 ; 0.63], R/R 3.688, perte reelle 7.627 % (gap inclus), EV 1.3329 % — **REFUSE**
      - refuse : cible atteinte seulement 13.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.576, borne haute 0.627 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 18.30 % > budget 12.00 %
   - ⚪ atr_grid a 1.25 ATR (stop 8.198 %) — p(stop avant cible) 0.4611 [0.41 ; 0.51], R/R 2.937, perte reelle 9.576 % (gap inclus), EV 1.9315 % — **REFUSE**
      - refuse : R/R 2.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.51 % > budget 12.00 %
   - ⚪ grid_snapped a 1.66 ATR (stop 12.873 %) — p(stop avant cible) 0.2654 [0.22 ; 0.31], R/R 1.902, perte reelle 14.788 % (gap inclus), EV 2.4182 % — **REFUSE**
      - refuse : R/R 1.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.95 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 16.396 %) — p(stop avant cible) 0.1785 [0.14 ; 0.22], R/R 1.489, perte reelle 18.886 % (gap inclus), EV 2.6842 % — **REFUSE**
      - refuse : R/R 1.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.74 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 18.035 %) — p(stop avant cible) 0.1419 [0.11 ; 0.18], R/R 1.361, perte reelle 20.662 % (gap inclus), EV 2.8954 % — **REFUSE**
      - refuse : R/R 1.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.05 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 19.675 %) — p(stop avant cible) 0.1299 [0.10 ; 0.17], R/R 1.287, perte reelle 21.849 % (gap inclus), EV 2.9153 % — **REFUSE**
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.22 % > budget 12.00 %
   - 🟢 grid_snapped a 3.45 ATR (stop 24.565 %) — p(stop avant cible) 0.0899 [0.06 ; 0.12], R/R 1.082, perte reelle 26.007 % (gap inclus), EV 2.8758 % — **REFUSE**
      - refuse : R/R 1.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.16 % > budget 12.00 %
   - 🟢 grid_snapped a 4.43 ATR (stop 30.99 %) — p(stop avant cible) 0.0701 [0.05 ; 0.10], R/R 0.905, perte reelle 31.093 % (gap inclus), EV 2.5698 % — **REFUSE**
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.13 % > budget 12.00 %
   - 🟢 grid_snapped a 5.29 ATR (stop 36.66 %) — p(stop avant cible) 0.0504 [0.03 ; 0.08], R/R 0.767, perte reelle 36.699 % (gap inclus), EV 2.366 % — **REFUSE**
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.70 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 39.35 %) — p(stop avant cible) 0.0146 [0.01 ; 0.03], R/R 0.715, perte reelle 39.369 % (gap inclus), EV 2.5799 % — **REFUSE**
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.31 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 42.629 %) — p(stop avant cible) 0.0034 [0.00 ; 0.01], R/R 0.66, perte reelle 42.629 % (gap inclus), EV 2.6002 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.90 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 45.908 %) — p(stop avant cible) 0.0021 [0.00 ; 0.01], R/R 0.611, perte reelle 46.037 % (gap inclus), EV 2.5972 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.01 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 49.187 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.547, perte reelle 51.428 % (gap inclus), EV 2.5874 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.15 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 52.466 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.506, perte reelle 55.543 % (gap inclus), EV 2.5864 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.22 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 35.8, ATR14 2.3479 (6.558 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.344 ATR = 2.256 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.328 % | 35.6826 | 90.74 % | 93.55 % | 94.95 % | 95.45 % | 96.65 % | 97.84 % |
| 0.1 ATR | 0.656 % | 35.5652 | 82.18 % | 87.5 % | 89.51 % | 91.41 % | 93.19 % | 95.17 % |
| 0.15 ATR | 0.984 % | 35.4478 | 75.03 % | 82.36 % | 85.27 % | 88.47 % | 90.85 % | 93.84 % |
| 0.2 ATR | 1.312 % | 35.3304 | 68.18 % | 77.62 % | 80.83 % | 85.95 % | 89.33 % | 92.51 % |
| 0.25 ATR | 1.64 % | 35.213 | 61.93 % | 72.88 % | 76.49 % | 82.51 % | 87.2 % | 90.76 % |
| 0.35 ATR | 2.295 % | 34.9782 | 49.24 % | 63.51 % | 69.83 % | 77.35 % | 82.93 % | 88.19 % |
| 0.5 ATR | 3.279 % | 34.6261 | 34.84 % | 49.9 % | 58.63 % | 68.86 % | 77.13 % | 83.68 % |
| 0.75 ATR | 4.919 % | 34.0391 | 17.32 % | 33.37 % | 43.19 % | 55.31 % | 66.57 % | 75.46 % |
| 1.0 ATR | 6.558 % | 33.4521 | 7.85 % | 21.47 % | 30.37 % | 43.68 % | 57.11 % | 68.69 % |
| 1.25 ATR | 8.198 % | 32.8652 | 3.73 % | 14.92 % | 22.2 % | 33.06 % | 47.76 % | 60.99 % |
| 1.5 ATR | 9.837 % | 32.2782 | 1.51 % | 9.58 % | 16.25 % | 25.88 % | 41.46 % | 54.62 % |
| 2.0 ATR | 13.117 % | 31.1043 | 0.3 % | 3.53 % | 8.38 % | 15.98 % | 29.57 % | 43.43 % |
| 2.5 ATR | 16.396 % | 29.9304 | 0.2 % | 1.51 % | 4.24 % | 9.5 % | 19.31 % | 31.52 % |
| 3.0 ATR | 19.675 % | 28.7564 | 0.2 % | 1.21 % | 2.62 % | 5.46 % | 13.82 % | 23.72 % |
| 4.0 ATR | 26.233 % | 26.4086 | 0.0 % | 0.6 % | 1.51 % | 2.63 % | 7.42 % | 14.17 % |
| 6.0 ATR | 39.35 % | 21.7129 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.54 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.34 ATR | 0.39 ATR | 0.53 ATR | 0.64 ATR | 0.71 ATR | 0.94 ATR | 1.17 ATR |
| **2 s.** | 0.23 ATR | 0.50 ATR | 0.57 ATR | 0.76 ATR | 0.93 ATR | 1.06 ATR | 1.48 ATR | 1.88 ATR |
| **3 s.** | 0.27 ATR | 0.64 ATR | 0.72 ATR | 0.95 ATR | 1.16 ATR | 1.34 ATR | 1.90 ATR | 2.41 ATR |
| **5 s.** | 0.39 ATR | 0.86 ATR | 0.97 ATR | 1.25 ATR | 1.54 ATR | 1.80 ATR | 2.46 ATR | 3.16 ATR |
| **10 s.** | 0.55 ATR | 1.19 ATR | 1.36 ATR | 1.86 ATR | 2.22 ATR | 2.47 ATR | 3.60 ATR | 4.90 ATR |
| **20 s.** | 0.77 ATR | 1.71 ATR | 1.93 ATR | 2.44 ATR | 2.92 ATR | 3.39 ATR | 4.97 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.394–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.574–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.919 %, prix 34.039), p(touche) 33.37 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.721–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.919 %, prix 34.039), p(touche) 43.19 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 16.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.972–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.198 %, prix 32.8651), p(touche) 33.06 % (en stress 89.9 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.36–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.837 %, prix 32.2784), p(touche) 41.46 % (en stress 95.96 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.93–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (16.396 %, prix 29.9302), p(touche) 31.52 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 57.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.067 | EV/share : $0.156 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 18 % | T3 12 %
- Kelly (position) : f* 0.056 | ¼-Kelly 0.014 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 15.3 | bear 5.0 | side 79.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 257.0 (= 8 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.564% → cible +3.365% / stop −2.5%, p_fill 47%, n_eff≈51.6) : P(cible|rempli) **29%** · **EV/risk +0.043** (×p_fill ; si rempli +0.23% du capital)
  - **swing** (entrée dip −5.642% → cible +7.77% / stop −6.95%, p_fill 28%, n_eff≈34.2) : P(cible|rempli) **41%** · **EV/risk -0.028** (×p_fill ; si rempli -0.70% du capital)
  - **deep** (entrée dip −8.713% → cible +20.054% / stop −10.776%, p_fill 28%, n_eff≈32.5) : P(cible|rempli) **30%** · **EV/risk +0.096** (×p_fill ; si rempli +3.73% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→77% · +2.0%→62% · +3.0%→43% · +5.0%→22% · +8.0%→9%
- Range intraday médian 5.66% (p90 9.37%) · excursion haute méd. +2.56% / basse méd. −2.37%
- Profil de vol intra : ouverture 3.84% vs midi 1.155% vs clôture 1.48% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓0% ; spike-down 69% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; neutre — autocorr -0.011)_ ; drift intra méd. 0.304% ; recovery-V 40%
- **σ réalisé intraday** 3.371% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 61% / bas 61% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 43.4066 (VA 43.1796–43.8039 ; dernier close 43.68)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 23% · rebond 78% · **stop −4.35%** sous le fill (sous le bruit) · cible +2.23% · R/R 0.51 (high win-rate)
- Gaps overnight (n=159) : méd. 0.21% · baisse 42% (gap-down >1% 31% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.93% (p90 −2.5%) · haut méd +1.02% · range méd 2.13%
- Excursion ouverture 15min (n=160) : bas méd −1.13% (p90 −3.1%) · haut méd +1.28% · range méd 2.8%
- Excursion ouverture 30min (n=160) : bas méd −1.36% (p90 −3.6%) · haut méd +1.53% · range méd 3.54%
- Excursion ouverture 60min (n=160) : bas méd −1.66% (p90 −4.07%) · haut méd +1.81% · range méd 4.18%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 43.69 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 71% (116/159) · gap 37% · délai 0.0min · rebond 57% (69/116) (MFE +1.39%)
   - −1.0% : fill 30min 51% · séance 67% (109/159) · gap 31% · délai 0.0min · rebond 58% (64/109) (MFE +1.64%)
   - −1.5% : fill 30min 45% · séance 61% (99/159) · gap 20% · délai 0.2min · rebond 69% (65/99) (MFE +1.56%)
   - −2.0% : fill 30min 39% · séance 53% (86/159) · gap 16% · délai 1.1min · rebond 72% (57/86) (MFE +1.74%)
   - −3.0% : fill 30min 26% · séance 44% (72/159) · gap 8% · délai 12.8min · rebond 64% (44/72) (MFE +1.42%)
   - −4.0% : fill 30min 13% · séance 31% (52/159) · gap 4% · délai 41.3min · rebond 72% (34/52) (MFE +1.7%)
   - −5.0% : fill 30min 10% · séance 23% (41/159) · gap 3% · délai 49.2min · rebond 78% (30/41) (MFE +2.23%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.62% (p90 −2.8%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.66% (p90 −2.62%) → stop au-delà de −1.86% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.65% (p90 −2.32%) → stop au-delà de −1.68% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=870 jambes) : jambe baissière méd −1.18% (p90 −2.77%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (71 séances) :
      · −1.0% : fill 98% (69/71) · rebond 48% (36/69)
      · −2.0% : fill 94% (65/71) · rebond 74% (41/65)
      · −3.0% : fill 85% (58/71) · rebond 65% (35/58)
      · −4.0% : fill 62% (43/71) · rebond 71% (28/43)
      · −5.0% : fill 46% (34/71) · rebond 76% (24/34)
   - **flat** (13 séances) :
      · −1.0% : fill 85% (12/13) · rebond 75% (9/12)
      · −2.0% : fill 36% (5/13) · rebond 50% (3/5)
      · −3.0% : fill 29% (3/13) · rebond 43% (2/3)
      · −4.0% : fill 10% (1/13) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/13) · rebond 0% (0/0)
   - **gap-up** (75 séances) :
      · −1.0% : fill 38% (28/75) · rebond 74% (19/28)
      · −2.0% : fill 21% (16/75) · rebond 70% (13/16)
      · −3.0% : fill 11% (11/75) · rebond 70% (7/11)
      · −4.0% : fill 8% (8/75) · rebond 72% (5/8)
      · −5.0% : fill 8% (7/75) · rebond 86% (6/7)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 68% si les 15 1res min sont vertes (80 cas) · 27% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **39min** → P(séance verte=clôture>ouverture) 78% si début vert vs 18% si rouge (base 48% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 213min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **78%** · continue >prix actuel 54% ; creux résiduel méd -1.96% (q20 -3.57%) → **SL/trailing à −3.57%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.91% / q75 +4.23% → **scale +1.91% / runner +4.23%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **18%** (continue à baisser 53%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.85%** (au-delà de la MAE q10 -4.85%), cible rebond +1.68% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.7% .. +4.13%] · haut q95 +5.15% · bas q05 -4.15%
   - 60min (n=160) : retour [-4.08% .. +5.23%] · haut q95 +6.49% · bas q05 -5.23%
   - 2h (n=160) : retour [-4.2% .. +6.08%] · haut q95 +7.25% · bas q05 -5.52%
   - 4h (n=160) : retour [-4.43% .. +6.66%] · haut q95 +7.77% · bas q05 -5.98%
   - 6h (n=160) : retour [-4.87% .. +6.53%] · haut q95 +8.68% · bas q05 -6.54%
   - session (n=160) : retour [-4.8% .. +6.89%] · haut q95 +8.93% · bas q05 -6.91%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — SMCI = **volatil sans tendance propre (choppy)** (vol intra méd 3.54%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.47 · part idiosyncratique 0.53
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 34.2  _(momentum baissier)_
- **ADX** : 25.4  _(tendance etablie)_
- **MACD** : hist -0.832  _(bearish_recent)_
- **BB** : %B -0.2 · largeur 19.4%
- **ATR** : 2.35 (67.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF 0.048  _(neutre)_
- **Vol ratio** : 0.82  _(volume normal)_
- **Choppiness** : 44.6  _(transition)_
- **MA** : MA20 41.45 · MA50 38.53 · MA200 32.43  _(prix < MA20)_
- **Dist MA** : MA20 -13.6% · MA50 -7.1% · MA200 +10.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (890631 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
