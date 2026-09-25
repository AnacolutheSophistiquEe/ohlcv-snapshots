# NEX

**Generated** : 2026-09-25T21:48:52.855218+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €135.60  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)  
> ↳ spot €135.60 (+3.3% vs entrée) · entrée €131.28 · stop €126.63 · T1 €135.41 · R/R 0.89  
> ↳ P(T1 av. stop) 59 % _(réel 5 s)_ · EV/risk 0.079 _(réel 5 s)_ (GBM 0.034) · ¼-Kelly 0.012 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.230 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €130.46–€132.11 (mid €131.28)
- Spot actuel : €135.60 (+3.3% au-dessus de la zone — repli à attendre)
- Stop : €126.63 (stop swing_plan-based (-6.61%))
- Targets : T1 €135.41 · R/R 0.89 | T2 €139.53 · R/R 1.77 | T3 €143.66 · R/R 2.66
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €126.63


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.64 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (6.61 %)** : le gap seul le franchit 0.469 % des séances (6 fois sur 1280).
   - exécution **1.558 pt plus bas** dans le cas TYPIQUE (médiane), 2.364 au p90, **2.986 au pire**
   - perte réelle **8.124 %** en moyenne _(tirée par la queue)_, jusqu'à **9.596 %** — au lieu des 6.61 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0071 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.516 % | p01 -3.643 % | pire -9.596 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0036** [0.0002 ; 0.0225] _(largeur 2.2 pt, n_eff 173.1)_
   - swing : **0.3786** [0.3287 ; 0.4306] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.3592** [0.31 ; 0.4108] _(largeur 10.1 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 20.3 observations effectives », dont la borne haute a 95 % vaut environ 14.8 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (37.7 pt), swing (43.5 pt), deep (46.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-3.52 %** | CVaR **-5.28 %** | vol 2.31 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.51 % vs -7.88 % si l'on extrapolait par √5 _(rapport 0.953 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0008** (β de hausse 1.0841, asymétrie 0.9232) vs FCHI — 620 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 121.65 sur atr_grid (3.0 ATR, 10.288 %) — p(stop avant cible) 0.1102 [0.08 ; 0.15], R/R 1.997, perte reelle 10.288 % (gap inclus), CVaR 10.288 %, EV 0.522 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.144 %) — p(stop avant cible) 0.4264 [0.38 ; 0.48], R/R 2.529, perte reelle 8.124 % (gap inclus), EV -1.1337 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.13 %) : P(cible) 1.4 % x 20.55 % + P(rien) 56.0 % x 3.66 % ne couvrent pas P(stop) 42.6 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.21 ATR (stop 6.065 %) — p(stop avant cible) 0.3644 [0.32 ; 0.42], R/R 2.529, perte reelle 8.124 % (gap inclus), EV -0.6413 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.64 %) : P(cible) 1.4 % x 20.55 % + P(rien) 62.2 % x 3.28 % ne couvrent pas P(stop) 36.4 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 1.79 ATR (stop 8.048 %) — p(stop avant cible) 0.1931 [0.15 ; 0.24], R/R 2.397, perte reelle 8.571 % (gap inclus), EV 0.431 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 5.99 ATR (stop 22.467 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 0.914, perte reelle 22.467 % (gap inclus), EV 0.6133 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.47 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.857 %) — p(stop avant cible) 0.9124 [0.88 ; 0.94], R/R 10.813, perte reelle 1.9 % (gap inclus), EV -1.0391 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 10.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.912, borne haute 0.939 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.04 %) : P(cible) 0.3 % x 20.55 % + P(rien) 8.4 % x 7.43 % ne couvrent pas P(stop) 91.2 % x 1.90 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.715 %) — p(stop avant cible) 0.8027 [0.76 ; 0.84], R/R 6.228, perte reelle 3.299 % (gap inclus), EV -1.3761 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.803, borne haute 0.842 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.38 %) : P(cible) 1.0 % x 20.55 % + P(rien) 18.8 % x 5.71 % ne couvrent pas P(stop) 80.3 % x 3.30 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.572 %) — p(stop avant cible) 0.7083 [0.66 ; 0.75], R/R 4.636, perte reelle 4.432 % (gap inclus), EV -1.4125 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.708, borne haute 0.754 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.41 %) : P(cible) 1.1 % x 20.55 % + P(rien) 28.1 % x 5.37 % ne couvrent pas P(stop) 70.8 % x 4.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.79 ATR (stop 7.164 %) — p(stop avant cible) 0.2553 [0.21 ; 0.30], R/R 2.465, perte reelle 8.333 % (gap inclus), EV 0.0832 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 8.573 %) — p(stop avant cible) 0.1802 [0.14 ; 0.22], R/R 2.141, perte reelle 9.596 % (gap inclus), EV 0.2814 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 9.43 %) — p(stop avant cible) 0.1417 [0.11 ; 0.18], R/R 2.141, perte reelle 9.596 % (gap inclus), EV 0.4949 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 10.288 %) — p(stop avant cible) 0.1102 [0.08 ; 0.15], R/R 1.997, perte reelle 10.288 % (gap inclus), EV 0.522 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 12.002 %) — p(stop avant cible) 0.0738 [0.05 ; 0.10], R/R 1.712, perte reelle 12.002 % (gap inclus), EV 0.5186 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.00 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 13.717 %) — p(stop avant cible) 0.0362 [0.02 ; 0.06], R/R 1.498, perte reelle 13.717 % (gap inclus), EV 0.5253 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.72 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 15.431 %) — p(stop avant cible) 0.0178 [0.01 ; 0.04], R/R 1.331, perte reelle 15.431 % (gap inclus), EV 0.5675 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.43 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 17.146 %) — p(stop avant cible) 0.0094 [0.00 ; 0.02], R/R 1.198, perte reelle 17.146 % (gap inclus), EV 0.5694 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.15 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 18.861 %) — p(stop avant cible) 0.0044 [0.00 ; 0.02], R/R 1.089, perte reelle 18.861 % (gap inclus), EV 0.6018 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.86 % > budget 12.00 %
   - 🟢 grid_snapped a 5.99 ATR (stop 21.583 %) — p(stop avant cible) 0.002 [0.00 ; 0.01], R/R 0.952, perte reelle 21.583 % (gap inclus), EV 0.6104 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.58 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 24.004 %) — p(stop avant cible) 0.0007 [0.00 ; 0.01], R/R 0.856, perte reelle 24.004 % (gap inclus), EV 0.614 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.00 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 25.719 %) — p(stop avant cible) 0.0007 [0.00 ; 0.01], R/R 0.799, perte reelle 25.719 % (gap inclus), EV 0.6128 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.72 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 27.434 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.749, perte reelle 27.434 % (gap inclus), EV 0.6184 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.43 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 135.6, ATR14 4.65 (3.429 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.347 ATR = 1.19 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.171 % | 135.3675 | 87.75 % | 91.36 % | 93.12 % | 95.08 % | 96.93 % | 97.8 % |
| 0.1 ATR | 0.343 % | 135.135 | 81.86 % | 87.63 % | 90.28 % | 93.11 % | 95.55 % | 96.9 % |
| 0.15 ATR | 0.514 % | 134.9025 | 75.2 % | 83.42 % | 86.84 % | 90.16 % | 94.07 % | 95.6 % |
| 0.2 ATR | 0.686 % | 134.67 | 68.63 % | 78.21 % | 83.1 % | 88.19 % | 92.68 % | 94.91 % |
| 0.25 ATR | 0.857 % | 134.4375 | 62.06 % | 73.5 % | 79.08 % | 85.04 % | 90.6 % | 93.71 % |
| 0.35 ATR | 1.2 % | 133.9725 | 49.61 % | 64.18 % | 71.61 % | 78.74 % | 86.65 % | 91.51 % |
| 0.5 ATR | 1.715 % | 133.275 | 34.51 % | 52.31 % | 61.1 % | 70.47 % | 80.32 % | 87.31 % |
| 0.75 ATR | 2.572 % | 132.1125 | 20.39 % | 36.31 % | 47.15 % | 58.56 % | 70.23 % | 80.72 % |
| 1.0 ATR | 3.429 % | 130.95 | 10.69 % | 24.24 % | 34.58 % | 48.33 % | 61.62 % | 74.03 % |
| 1.25 ATR | 4.287 % | 129.7875 | 4.9 % | 16.19 % | 24.85 % | 39.37 % | 54.5 % | 67.53 % |
| 1.5 ATR | 5.144 % | 128.625 | 2.45 % | 11.19 % | 18.47 % | 30.51 % | 46.79 % | 59.94 % |
| 2.0 ATR | 6.858 % | 126.3 | 0.88 % | 5.3 % | 10.02 % | 19.39 % | 35.01 % | 50.45 % |
| 2.5 ATR | 8.573 % | 123.975 | 0.49 % | 2.65 % | 5.6 % | 11.42 % | 24.43 % | 38.76 % |
| 3.0 ATR | 10.288 % | 121.65 | 0.2 % | 1.67 % | 3.24 % | 7.09 % | 17.51 % | 30.27 % |
| 4.0 ATR | 13.717 % | 117.0 | 0.1 % | 0.49 % | 0.88 % | 1.87 % | 7.52 % | 17.88 % |
| 6.0 ATR | 20.575 % | 107.7 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 1.29 % | 4.3 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.67 ATR | 0.76 ATR | 1.03 ATR | 1.25 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.61 ATR | 0.82 ATR | 0.98 ATR | 1.13 ATR | 1.60 ATR | 2.06 ATR |
| **3 s.** | 0.30 ATR | 0.70 ATR | 0.79 ATR | 1.04 ATR | 1.25 ATR | 1.44 ATR | 2.00 ATR | 2.63 ATR |
| **5 s.** | 0.42 ATR | 0.96 ATR | 1.09 ATR | 1.43 ATR | 1.75 ATR | 1.97 ATR | 2.66 ATR | 3.40 ATR |
| **10 s.** | 0.63 ATR | 1.40 ATR | 1.58 ATR | 2.10 ATR | 2.47 ATR | 2.82 ATR | 3.75 ATR | 4.81 ATR |
| **20 s.** | 0.96 ATR | 2.02 ATR | 2.23 ATR | 2.84 ATR | 3.42 ATR | 3.83 ATR | 5.16 ATR | 5.90 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.396–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (78.2 % des re-echantillons)
- **2 seance(s)** : plage utile 0.614–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.572 %, prix 132.1124), p(touche) 36.31 % (en stress 88.24 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.793–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.429 %, prix 130.9503), p(touche) 34.58 % (en stress 84.31 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.093–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.287 %, prix 129.7868), p(touche) 39.37 % (en stress 93.14 %)  ✅ optimum identifie (61.2 % des re-echantillons)
- **10 seance(s)** : plage utile 1.576–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.858 %, prix 126.3006), p(touche) 35.01 % (en stress 98.04 %)  ✅ optimum identifie (70.0 % des re-echantillons)
- **20 seance(s)** : plage utile 2.233–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.573 %, prix 123.975), p(touche) 38.76 % (en stress 98.02 %)  ✅ optimum identifie (68.2 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.034 | EV/share : €0.157 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 51 % | T2 18 % | T3 8 %
- Kelly (position) : f* 0.049 | ¼-Kelly 0.012 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 46.2 | bear 22.0 | side 31.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 271.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.446% → cible +1.405% / stop −8.0%, p_fill 46%, n_eff≈20.3) : P(cible|rempli) **30%** · **EV/risk -0.023** (×p_fill ; si rempli -0.40% du capital)
  - **swing** (entrée dip −3.181% → cible +3.143% / stop −3.542%, p_fill 36%, n_eff≈17.2) : P(cible|rempli) **59%** · **EV/risk +0.079** (×p_fill ; si rempli +0.77% du capital)
  - **deep** (entrée dip −4.926% → cible +4.445% / stop −5.41%, p_fill 24%, n_eff≈15.1) : P(cible|rempli) **44%** · **EV/risk +0.040** (×p_fill ; si rempli +0.90% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→65% · +1.0%→51% · +2.0%→22% · +3.0%→10% · +5.0%→1% · +8.0%→0%
- Range intraday médian 2.95% (p90 4.72%) · excursion haute méd. +1.01% / basse méd. −1.35%
- Profil de vol intra : ouverture 1.739% vs midi 0.517% vs clôture 0.7% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 47% · recovery-V 15%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; mean-reverting — autocorr -0.041)_ ; drift intra méd. -0.566% ; recovery-V 11%
- **σ réalisé intraday** 1.96% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 68% / whipsaw 26%
- POC intraday (dernière séance, temps-au-prix) : 138.1975 (VA 137.3925–138.7725 ; dernier close 136.7)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 16% · rebond 50% · **stop −1.94%** sous le fill (sous le bruit) · cible +1.05% · R/R 0.54 (high win-rate)
- Gaps overnight (n=159) : méd. 0.36% · baisse 31% (gap-down >1% 5% · >2% 1%)
- Excursion ouverture 5min (n=160) : bas méd −0.55% (p90 −1.78%) · haut méd +0.15% · range méd 1.05%
- Excursion ouverture 15min (n=160) : bas méd −0.76% (p90 −1.95%) · haut méd +0.37% · range méd 1.29%
- Excursion ouverture 30min (n=160) : bas méd −0.8% (p90 −2.21%) · haut méd +0.48% · range méd 1.41%
- Excursion ouverture 60min (n=160) : bas méd −0.86% (p90 −2.44%) · haut méd +0.58% · range méd 1.59%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 136.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 45% · séance 61% (94/159) · gap 10% · délai 3.0min · rebond 45% (45/94) (MFE +0.74%)
   - −1.0% : fill 30min 27% · séance 53% (77/159) · gap 5% · délai 26.0min · rebond 43% (36/77) (MFE +0.73%)
   - −1.5% : fill 30min 14% · séance 42% (58/159) · gap 1% · délai 47.0min · rebond 36% (25/58) (MFE +0.67%)
   - −2.0% : fill 30min 10% · séance 29% (42/159) · gap 1% · délai 66.4min · rebond 45% (20/42) (MFE +0.78%)
   - −3.0% : fill 30min 4% · séance 16% (24/159) · gap 0% · délai 207.9min · rebond 50% (13/24) (MFE +1.05%)
   - −4.0% : fill 30min 0% · séance 5% (9/159) · gap 0% · délai 350.2min · rebond 11% (3/9) (MFE +0.48%)
   - −5.0% : fill 30min 0% · séance 2% (3/159) · gap 0% · délai 410.2min · rebond 42% (1/3) (MFE +0.73%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.15% (p90 −1.27%) → stop au-delà de −0.86% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.15% (p90 −0.88%) → stop au-delà de −0.6% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.13% (p90 −0.6%) → stop au-delà de −0.44% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=327 jambes) : jambe baissière méd −1.06% (p90 −2.3%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (30 séances) :
      · −1.0% : fill 80% (25/30) · rebond 55% (13/25)
      · −2.0% : fill 50% (16/30) · rebond 44% (7/16)
      · −3.0% : fill 32% (11/30) · rebond 44% (6/11)
      · −4.0% : fill 21% (6/30) · rebond 12% (2/6)
      · −5.0% : fill 12% (3/30) · rebond 42% (1/3)
   - **flat** (36 séances) :
      · −1.0% : fill 55% (21/36) · rebond 37% (9/21)
      · −2.0% : fill 30% (11/36) · rebond 32% (4/11)
      · −3.0% : fill 20% (7/36) · rebond 33% (3/7)
      · −4.0% : fill 6% (2/36) · rebond 0% (0/2)
      · −5.0% : fill 0% (0/36) · rebond 0% (0/0)
   - **gap-up** (93 séances) :
      · −1.0% : fill 45% (31/93) · rebond 42% (14/31)
      · −2.0% : fill 23% (15/93) · rebond 55% (9/15)
      · −3.0% : fill 9% (6/93) · rebond 78% (4/6)
      · −4.0% : fill 0% (1/93) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/93) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 71% si les 15 1res min sont vertes (86 cas) · 15% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **30min** → P(séance verte=clôture>ouverture) 78% si début vert vs 18% si rouge (base 43% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 221min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **78%** · continue >prix actuel 51% ; creux résiduel méd -1.0% (q20 -1.89%) → **SL/trailing à −1.89%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.06% / q75 +1.76% → **scale +1.06% / runner +1.76%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **18%** (continue à baisser 59%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.2%** (au-delà de la MAE q10 -3.2%), cible rebond +0.98% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.85% .. +2.03%] · haut q95 +2.5% · bas q05 -2.59%
   - 60min (n=160) : retour [-2.77% .. +2.4%] · haut q95 +2.64% · bas q05 -3.21%
   - 2h (n=160) : retour [-3.18% .. +2.43%] · haut q95 +2.93% · bas q05 -3.68%
   - 4h (n=160) : retour [-2.91% .. +3.17%] · haut q95 +3.22% · bas q05 -3.77%
   - 6h (n=160) : retour [-3.48% .. +3.64%] · haut q95 +3.9% · bas q05 -4.14%
   - session (n=160) : retour [-3.39% .. +2.81%] · haut q95 +3.91% · bas q05 -4.65%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.93%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 46.5  _(neutre)_
- **ADX** : 10.5  _(pas de tendance nette)_
- **MACD** : hist -0.121  _(pas de croisement recent)_
- **BB** : %B 0.28 · largeur 8.4%
- **ATR** : 4.65 (70.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.225  _(distribution)_
- **Vol ratio** : 0.7  _(volume normal)_
- **Choppiness** : 56.4  _(transition)_
- **MA** : MA20 138.16 · MA50 137.27 · MA200 135.18  _(prix < MA20)_
- **Dist MA** : MA20 -1.8% · MA50 -1.2% · MA200 +0.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (870279 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
