# SMCI

**Generated** : 2026-11-03T01:22:23.516277+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $30.46  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-05 — Bank of England — décision de taux (J-1 sess · macro taux)  
> ↳ spot $30.46 (+4.2% vs entrée) · entrée $29.22 · stop $28.44 · T1 $30.53 · R/R 1.68  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.68% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +0.1 % ≠ (strike 33.0 − spot 30.46)/spot = +8.3 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -32 % hors [0,100] (R² max 0.75). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-02 : 30.46 · ATR Wilder 2.46 (8.07 %)_
- **Swing** : plage **27.41 → 25.57** (-10.0 % a -16.04 % sous la cloture, 0.75 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 26.86-27.75 (B) ; 25.13-26.06 (A). stop INDICATIF 22.15 (-13.39 % sous le bas ; sous le support 23.38-24.19 (- 0,5 ATR)).
- **Deep** : plage **25.57 → 19.64** (-16.04 % a -35.53 % sous la cloture, 2.41 ATR) — touchee 44 % → 15 % du temps en 20 seances ; supports reels dans la plage : 25.13-26.06 (A) ; 23.38-24.19 (A) ; 20.71-21.79 (B) ; 18.79-20.2 (A). stop INDICATIF 16.02 (-18.42 % sous le bas ; sous le support 17.25-17.25 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 6.23 ATR sous le plus haut 20 s., RSI(2) 6.6. Limite **29.23** (seance suivante), stop catastrophe 19.4, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 28.5-29.68 (B, -2.56 %) ; 26.86-27.75 (B, -8.9 %) ; 25.13-26.06 (A, -14.45 %) ; 23.38-24.19 (A, -20.58 %) ; 20.71-21.79 (B, -28.46 %) ; 18.79-20.2 (A, -33.68 %)
- Resistances reelles au-dessus : 32.58-33.64 (A, 6.96 %) ; 33.86-34.98 (A, 11.16 %) ; 35.36-36.4 (A, 16.09 %) ; 36.8-37.85 (A, 20.81 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.14 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (17.5 %)** : le gap seul le franchit 0.319 % des séances (4 fois sur 1253).
   - exécution **8.258 pt plus bas** dans le cas TYPIQUE (médiane), 10.894 au p90, **11.551 au pire**
   - perte réelle **24.92 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 17.5 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0237 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.86 % | p01 -10.307 % | pire -29.051 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4697** [0.3964 ; 0.544] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.3092** [0.2622 ; 0.3594] _(largeur 9.7 pt, n_eff 345.7)_
   - deep : **0.245** [0.2019 ; 0.2923] _(largeur 9.0 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.9 pt), swing (47.5 pt), deep (46.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1020 séances)** : VaR **-7.98 %** | CVaR **-12.63 %** | vol 5.95 %/j
   - _fenêtre arrêtée : rupture de regime a 1080 seances en arriere (volatilite 3.78 % contre 6.23 % aujourd'hui, rapport 0.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -17.54 % vs -16.89 % si l'on extrapolait par √5 _(rapport 1.038 ; < 1 = le √5 surestime)_
- **β de baisse : 1.5208** (β de hausse 1.2037, asymétrie 1.2634) vs IWM — 605 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.793× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 29.807 sur atr_grid (0.25 ATR, 2.144 %) — p(stop avant cible) 0.8741 [0.84 ; 0.91], R/R 14.513, perte reelle 2.415 % (gap inclus), CVaR 6.838 %, EV 0.5151 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.7152 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 4.2 % du temps (< 15 %) meme a 10 seances : le R/R de 14.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.874, borne haute 0.906 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 6.84 % > budget 5.06 %
- Budget de queue : **5.06 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.131 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 40.6 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 12.863 %) — p(stop avant cible) 0.302 [0.26 ; 0.35], R/R 2.425, perte reelle 14.453 % (gap inclus), EV 1.3598 % — **REFUSE**
      - refuse : cible atteinte seulement 7.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.29 % > budget 5.06 %
   - 🟢 support a 1.93 ATR (stop 19.049 %) — p(stop avant cible) 0.1677 [0.13 ; 0.21], R/R 1.661, perte reelle 21.099 % (gap inclus), EV 1.56 % — **REFUSE**
      - refuse : cible atteinte seulement 7.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.06 % > budget 5.06 %
   - 🟢 support a 2.71 ATR (stop 25.713 %) — p(stop avant cible) 0.1048 [0.08 ; 0.14], R/R 1.321, perte reelle 26.525 % (gap inclus), EV 1.3492 % — **REFUSE**
      - refuse : cible atteinte seulement 7.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.41 % > budget 5.06 %
   - 🟢 support a 4.2 ATR (stop 38.517 %) — p(stop avant cible) 0.0217 [0.01 ; 0.04], R/R 0.909, perte reelle 38.549 % (gap inclus), EV 1.1439 % — **REFUSE**
      - refuse : cible atteinte seulement 7.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.15 % > budget 5.06 %
   - ⚪ atr_grid a 0.25 ATR (stop 2.144 %) — p(stop avant cible) 0.8741 [0.84 ; 0.91], R/R 14.513, perte reelle 2.415 % (gap inclus), EV 0.5151 % — **REFUSE**
      - refuse : cible atteinte seulement 4.2 % du temps (< 15 %) meme a 10 seances : le R/R de 14.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.874, borne haute 0.906 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 6.84 % > budget 5.06 %
   - ⚪ atr_grid a 0.5 ATR (stop 4.288 %) — p(stop avant cible) 0.7387 [0.69 ; 0.78], R/R 7.22, perte reelle 4.855 % (gap inclus), EV 0.5183 % — **REFUSE**
      - refuse : cible atteinte seulement 5.5 % du temps (< 15 %) meme a 10 seances : le R/R de 7.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.739, borne haute 0.783 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 12.19 % > budget 5.06 %
   - ⚪ atr_grid a 0.75 ATR (stop 6.432 %) — p(stop avant cible) 0.6042 [0.55 ; 0.65], R/R 4.784, perte reelle 7.327 % (gap inclus), EV 0.675 % — **REFUSE**
      - refuse : cible atteinte seulement 6.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.604, borne haute 0.655 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 16.65 % > budget 5.06 %
   - ⚪ atr_grid a 1.0 ATR (stop 8.576 %) — p(stop avant cible) 0.4733 [0.42 ; 0.53], R/R 3.522, perte reelle 9.952 % (gap inclus), EV 1.0457 % — **REFUSE**
      - refuse : cible atteinte seulement 7.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 20.98 % > budget 5.06 %
   - ⚪ atr_grid a 1.25 ATR (stop 10.72 %) — p(stop avant cible) 0.3894 [0.34 ; 0.44], R/R 2.88, perte reelle 12.169 % (gap inclus), EV 1.0878 % — **REFUSE**
      - refuse : cible atteinte seulement 7.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.88 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.54 % > budget 5.06 %
   - ⚪ atr_grid a 3.5 ATR (stop 30.015 %) — p(stop avant cible) 0.0679 [0.04 ; 0.10], R/R 1.162, perte reelle 30.158 % (gap inclus), EV 1.205 % — **REFUSE**
      - refuse : cible atteinte seulement 7.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.21 % > budget 5.06 %
   - ⚪ atr_grid a 5.0 ATR (stop 42.878 %) — p(stop avant cible) 0.0031 [0.00 ; 0.01], R/R 0.817, perte reelle 42.878 % (gap inclus), EV 1.1789 % — **REFUSE**
      - refuse : cible atteinte seulement 7.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.50 % > budget 5.06 %
   - ⚪ atr_grid a 5.5 ATR (stop 47.166 %) — p(stop avant cible) 0.002 [0.00 ; 0.01], R/R 0.738, perte reelle 47.523 % (gap inclus), EV 1.1691 % — **REFUSE**
      - refuse : cible atteinte seulement 7.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.64 % > budget 5.06 %
   - ⚪ atr_grid a 6.0 ATR (stop 51.454 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 0.631, perte reelle 55.543 % (gap inclus), EV 1.1645 % — **REFUSE**
      - refuse : cible atteinte seulement 7.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.78 % > budget 5.06 %
   - ⚪ atr_grid a 6.5 ATR (stop 55.742 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 0.626, perte reelle 56.012 % (gap inclus), EV 1.1639 % — **REFUSE**
      - refuse : cible atteinte seulement 7.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.79 % > budget 5.06 %
   - ⚪ atr_grid a 7.0 ATR (stop 60.03 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.584, perte reelle 60.03 % (gap inclus), EV 1.1719 % — **REFUSE**
      - refuse : cible atteinte seulement 7.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.60 % > budget 5.06 %
   - ⚪ atr_grid a 7.5 ATR (stop 64.317 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.545, perte reelle 64.317 % (gap inclus), EV 1.1719 % — **REFUSE**
      - refuse : cible atteinte seulement 7.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.60 % > budget 5.06 %
   - ⚪ atr_grid a 8.0 ATR (stop 68.605 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.511, perte reelle 68.605 % (gap inclus), EV 1.1719 % — **REFUSE**
      - refuse : cible atteinte seulement 7.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.60 % > budget 5.06 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 30.46, ATR14 2.6121 (8.576 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.348 ATR = 2.984 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.429 % | 30.3294 | 90.84 % | 93.65 % | 94.95 % | 95.55 % | 96.75 % | 97.95 % |
| 0.1 ATR | 0.858 % | 30.1988 | 82.28 % | 87.6 % | 89.51 % | 91.51 % | 93.29 % | 95.28 % |
| 0.15 ATR | 1.286 % | 30.0682 | 75.33 % | 82.56 % | 85.37 % | 88.68 % | 91.06 % | 94.05 % |
| 0.2 ATR | 1.715 % | 29.9376 | 68.38 % | 77.72 % | 80.93 % | 86.25 % | 89.63 % | 92.81 % |
| 0.25 ATR | 2.144 % | 29.807 | 62.24 % | 73.08 % | 76.69 % | 82.91 % | 87.7 % | 91.27 % |
| 0.35 ATR | 3.001 % | 29.5457 | 49.75 % | 63.91 % | 70.23 % | 77.96 % | 83.64 % | 88.91 % |
| 0.5 ATR | 4.288 % | 29.1539 | 34.84 % | 50.3 % | 59.03 % | 69.46 % | 77.95 % | 84.5 % |
| 0.75 ATR | 6.432 % | 28.5009 | 17.42 % | 33.87 % | 43.79 % | 56.02 % | 67.68 % | 76.59 % |
| 1.0 ATR | 8.576 % | 27.8479 | 7.85 % | 21.98 % | 30.98 % | 44.39 % | 58.23 % | 69.92 % |
| 1.25 ATR | 10.72 % | 27.1948 | 3.73 % | 15.32 % | 22.81 % | 33.87 % | 48.98 % | 62.22 % |
| 1.5 ATR | 12.863 % | 26.5418 | 1.51 % | 9.78 % | 16.65 % | 26.39 % | 42.48 % | 55.85 % |
| 2.0 ATR | 17.151 % | 25.2357 | 0.3 % | 3.63 % | 8.68 % | 16.48 % | 30.59 % | 44.66 % |
| 2.5 ATR | 21.439 % | 23.9296 | 0.2 % | 1.51 % | 4.44 % | 10.01 % | 20.22 % | 32.75 % |
| 3.0 ATR | 25.727 % | 22.6236 | 0.2 % | 1.21 % | 2.62 % | 5.97 % | 14.74 % | 24.95 % |
| 4.0 ATR | 34.303 % | 20.0114 | 0.0 % | 0.6 % | 1.51 % | 2.83 % | 8.13 % | 15.09 % |
| 6.0 ATR | 51.454 % | 14.7871 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.54 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.64 ATR | 0.71 ATR | 0.94 ATR | 1.17 ATR |
| **2 s.** | 0.23 ATR | 0.51 ATR | 0.58 ATR | 0.77 ATR | 0.94 ATR | 1.07 ATR | 1.49 ATR | 1.89 ATR |
| **3 s.** | 0.28 ATR | 0.65 ATR | 0.73 ATR | 0.96 ATR | 1.18 ATR | 1.36 ATR | 1.92 ATR | 2.43 ATR |
| **5 s.** | 0.40 ATR | 0.88 ATR | 0.99 ATR | 1.28 ATR | 1.57 ATR | 1.82 ATR | 2.50 ATR | 3.31 ATR |
| **10 s.** | 0.57 ATR | 1.22 ATR | 1.40 ATR | 1.90 ATR | 2.27 ATR | 2.52 ATR | 3.72 ATR | 5.03 ATR |
| **20 s.** | 0.81 ATR | 1.76 ATR | 1.99 ATR | 2.49 ATR | 3.00 ATR | 3.50 ATR | 5.07 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.398–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.581–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (6.432 %, prix 28.5008), p(touche) 33.87 % (en stress 88.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.73–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (6.432 %, prix 28.5008), p(touche) 43.79 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 18.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.987–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (10.72 %, prix 27.1947), p(touche) 33.87 % (en stress 90.91 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.403–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (12.863 %, prix 26.5419), p(touche) 42.48 % (en stress 96.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.985–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (17.151 %, prix 25.2358), p(touche) 44.66 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.016 | EV/share : $-0.013 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 27 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 38.0 | bear 5.0 | side 57.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.057% → cible +4.469% / stop −2.682%, p_fill 30%, n_eff≈31.2) : P(cible|rempli) **9%** · **EV/risk +0.045** (×p_fill ; si rempli +0.40% du capital)
  - **swing** (entrée dip −8.924% → cible +14.819% / stop −9.416%, p_fill 12%, n_eff≈14.5) : P(cible|rempli) **13%** · **EV/risk -0.046** (×p_fill ; si rempli -3.73% du capital)
  - **deep** (entrée dip −13.797% → cible +21.304% / stop −14.922%, p_fill 13%, n_eff≈15.5) : P(cible|rempli) **13%** · **EV/risk -0.039** (×p_fill ; si rempli -4.45% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→74% · +2.0%→57% · +3.0%→40% · +5.0%→22% · +8.0%→8%
- Range intraday médian 5.72% (p90 9.37%) · excursion haute méd. +2.42% / basse méd. −2.68%
- Profil de vol intra : ouverture 3.884% vs midi 1.151% vs clôture 1.47% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 74% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.14 ; mean-reverting — autocorr -0.077)_ ; drift intra méd. -0.659% ; recovery-V 28%
- **σ réalisé intraday** 3.524% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 60% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 33.7346 (VA 33.3821–34.0871 ; dernier close 32.95)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 29% · rebond 74% · **stop −4.61%** sous le fill (sous le bruit) · cible +2.15% · R/R 0.47 (high win-rate)
- Gaps overnight (n=159) : méd. 0.0% · baisse 50% (gap-down >1% 38% · >2% 23%)
- Excursion ouverture 5min (n=160) : bas méd −1.11% (p90 −2.79%) · haut méd +0.93% · range méd 2.16%
- Excursion ouverture 15min (n=160) : bas méd −1.42% (p90 −3.55%) · haut méd +1.01% · range méd 2.85%
- Excursion ouverture 30min (n=160) : bas méd −1.65% (p90 −3.98%) · haut méd +1.23% · range méd 3.58%
- Excursion ouverture 60min (n=160) : bas méd −1.91% (p90 −4.46%) · haut méd +1.48% · range méd 4.31%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 32.94 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 73% (116/159) · gap 42% · délai 0.0min · rebond 49% (64/116) (MFE +0.98%)
   - −1.0% : fill 30min 58% · séance 70% (109/159) · gap 38% · délai 0.0min · rebond 51% (60/109) (MFE +1.09%)
   - −1.5% : fill 30min 52% · séance 66% (100/159) · gap 28% · délai 0.0min · rebond 56% (62/100) (MFE +1.13%)
   - −2.0% : fill 30min 47% · séance 59% (87/159) · gap 23% · délai 0.1min · rebond 56% (54/87) (MFE +1.2%)
   - −3.0% : fill 30min 34% · séance 48% (73/159) · gap 11% · délai 2.7min · rebond 62% (43/73) (MFE +1.34%)
   - −4.0% : fill 30min 21% · séance 35% (54/159) · gap 5% · délai 12.5min · rebond 72% (36/54) (MFE +1.72%)
   - −5.0% : fill 30min 15% · séance 29% (44/159) · gap 2% · délai 21.5min · rebond 74% (31/44) (MFE +2.15%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.69% (p90 −2.8%) → stop au-delà de −1.93% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.71% (p90 −2.84%) → stop au-delà de −1.86% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.65% (p90 −2.25%) → stop au-delà de −1.73% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=876 jambes) : jambe baissière méd −1.19% (p90 −2.78%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 98% (68/70) · rebond 39% (32/68)
      · −2.0% : fill 96% (64/70) · rebond 57% (37/64)
      · −3.0% : fill 86% (58/70) · rebond 60% (33/58)
      · −4.0% : fill 64% (44/70) · rebond 70% (29/44)
      · −5.0% : fill 53% (36/70) · rebond 71% (24/36)
   - **flat** (14 séances) :
      · −1.0% : fill 90% (13/14) · rebond 84% (10/13)
      · −2.0% : fill 57% (6/14) · rebond 47% (4/6)
      · −3.0% : fill 20% (3/14) · rebond 43% (2/3)
      · −4.0% : fill 7% (1/14) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/14) · rebond 0% (0/0)
   - **gap-up** (75 séances) :
      · −1.0% : fill 36% (28/75) · rebond 66% (18/28)
      · −2.0% : fill 21% (17/75) · rebond 58% (13/17)
      · −3.0% : fill 13% (12/75) · rebond 78% (8/12)
      · −4.0% : fill 11% (9/75) · rebond 81% (6/9)
      · −5.0% : fill 10% (8/75) · rebond 91% (7/8)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 67% si les 15 1res min sont vertes (78 cas) · 24% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:46** → P(séance verte=clôture>ouverture) 83% si début vert vs 11% si rouge (base 43% · écart 72 pts) ; prédictivité sature ensuite (plafond brut 213min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **83%** · continue >prix actuel 59% ; creux résiduel méd -1.33% (q20 -2.94%) → **SL/trailing à −2.94%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.67% / q75 +2.72% → **scale +1.67% / runner +2.72%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **11%** (continue à baisser 55%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.93%** (au-delà de la MAE q10 -3.93%), cible rebond +1.31% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.17% .. +4.1%] · haut q95 +5.04% · bas q05 -5.27%
   - 60min (n=160) : retour [-4.12% .. +4.96%] · haut q95 +6.21% · bas q05 -5.43%
   - 2h (n=160) : retour [-4.55% .. +5.52%] · haut q95 +7.12% · bas q05 -5.93%
   - 4h (n=160) : retour [-4.91% .. +6.39%] · haut q95 +7.24% · bas q05 -6.41%
   - 6h (n=160) : retour [-5.14% .. +6.41%] · haut q95 +7.8% · bas q05 -6.61%
   - session (n=160) : retour [-6.33% .. +6.37%] · haut q95 +7.95% · bas q05 -6.95%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (4) pour des stats fiables : 2.5% des séances seulement sont des jours de hausse propre — SMCI = **volatil sans tendance propre (choppy)** (vol intra méd 3.59%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.52 · part idiosyncratique 0.48
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-05 — Bank of England — décision de taux (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-05 — Bank of England — décision de taux (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-05 — Bank of England — décision de taux (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 31.1  _(momentum baissier)_
- **ADX** : 20.5  _(pas de tendance nette)_
- **MACD** : hist -0.353  _(pas de croisement recent)_
- **BB** : %B 0.17 · largeur 48.0%
- **ATR** : 2.61 (84.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.181  _(distribution)_
- **Vol ratio** : 0.99  _(volume normal)_
- **Choppiness** : 58.8  _(transition)_
- **MA** : MA20 36.14 · MA50 38.1 · MA200 32.67  _(prix < MA20)_
- **Dist MA** : MA20 -15.7% · MA50 -20.0% · MA200 -6.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (737181 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
