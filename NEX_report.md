# NEX

**Generated** : 2026-09-16T00:11:15.601856+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €133.60  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-16 — US FOMC Rate Decision (J-0 sess · macro taux)  
> ↳ spot €133.60 (+1.2% vs entrée) · entrée €131.98 · stop €121.42 · T1 €133.81 · R/R 0.17  
> ↳ P(T1 av. stop) 31 % _(réel 5 s)_ · EV/risk -0.033 _(réel 5 s)_ (GBM -0.078) · ¼-Kelly 0.059 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -76 % hors [0,100] (R² max 0.91). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.310 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €131.61–€132.35 (mid €131.98)
- Spot actuel : €133.60 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : €121.42 (stop swing_plan-based (-6.09%))
- Targets : T1 €133.81 · R/R 0.17 | T2 €135.64 · R/R 0.35 | T3 €137.47 · R/R 0.52
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €121.42


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.64 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (6.09 %)** : le gap seul le franchit 0.469 % des séances (6 fois sur 1279).
   - exécution **2.078 pt plus bas** dans le cas TYPIQUE (médiane), 2.884 au p90, **3.506 au pire**
   - perte réelle **8.124 %** en moyenne _(tirée par la queue)_, jusqu'à **9.596 %** — au lieu des 6.09 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0095 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.516 % | p01 -3.644 % | pire -9.596 % _(sur 1279 séances)_
- **P(stop avant cible)** _(source : daily, 1280 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.004** [0.0003 ; 0.0233] _(largeur 2.3 pt, n_eff 173.1)_
   - swing : **0.3983** [0.3477 ; 0.4506] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3667** [0.3172 ; 0.4184] _(largeur 10.1 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 22.8 observations effectives », dont la borne haute a 95 % vaut environ 13.2 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (36.4 pt), swing (42.5 pt), deep (41.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-3.51 %** | CVaR **-5.28 %** | vol 2.31 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.51 % vs -7.85 % si l'on extrapolait par √5 _(rapport 0.957 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0077** (β de hausse 1.0948, asymétrie 0.9204) vs FCHI — 618 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 119.8643 sur atr_grid (3.0 ATR, 10.281 %) — p(stop avant cible) 0.1161 [0.09 ; 0.15], R/R 2.175, perte reelle 10.281 % (gap inclus), CVaR 10.281 %, EV 0.5744 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.141 %) — p(stop avant cible) 0.4192 [0.37 ; 0.47], R/R 2.753, perte reelle 8.124 % (gap inclus), EV -0.8999 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.90 %) : P(cible) 0.7 % x 22.37 % + P(rien) 57.4 % x 4.10 % ne couvrent pas P(stop) 41.9 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 1.51 ATR (stop 7.501 %) — p(stop avant cible) 0.2532 [0.21 ; 0.30], R/R 2.609, perte reelle 8.571 % (gap inclus), EV 0.1977 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 5.65 ATR (stop 21.674 %) — p(stop avant cible) 0.0021 [0.00 ; 0.01], R/R 1.032, perte reelle 21.674 % (gap inclus), EV 0.6668 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.67 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.857 %) — p(stop avant cible) 0.9077 [0.87 ; 0.93], R/R 11.79, perte reelle 1.897 % (gap inclus), EV -0.9835 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 11.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.908, borne haute 0.935 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.98 %) : P(cible) 0.4 % x 22.37 % + P(rien) 8.9 % x 7.43 % ne couvrent pas P(stop) 90.8 % x 1.90 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.714 %) — p(stop avant cible) 0.7921 [0.75 ; 0.83], R/R 6.78, perte reelle 3.299 % (gap inclus), EV -1.2475 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 6.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.792, borne haute 0.832 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.25 %) : P(cible) 0.7 % x 22.37 % + P(rien) 20.1 % x 6.03 % ne couvrent pas P(stop) 79.2 % x 3.30 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.57 %) — p(stop avant cible) 0.6928 [0.64 ; 0.74], R/R 5.046, perte reelle 4.432 % (gap inclus), EV -1.2316 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 5.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.693, borne haute 0.740 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.23 %) : P(cible) 0.7 % x 22.37 % + P(rien) 30.0 % x 5.61 % ne couvrent pas P(stop) 69.3 % x 4.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.427 %) — p(stop avant cible) 0.5891 [0.54 ; 0.64], R/R 4.09, perte reelle 5.468 % (gap inclus), EV -1.0237 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 4.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.589, borne haute 0.640 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.02 %) : P(cible) 0.7 % x 22.37 % + P(rien) 40.4 % x 5.06 % ne couvrent pas P(stop) 58.9 % x 5.47 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.284 %) — p(stop avant cible) 0.5098 [0.46 ; 0.56], R/R 3.207, perte reelle 6.975 % (gap inclus), EV -1.1641 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.510, borne haute 0.562 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.16 %) : P(cible) 0.7 % x 22.37 % + P(rien) 48.3 % x 4.63 % ne couvrent pas P(stop) 51.0 % x 6.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.51 ATR (stop 6.219 %) — p(stop avant cible) 0.3513 [0.30 ; 0.40], R/R 2.753, perte reelle 8.124 % (gap inclus), EV -0.3936 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.39 %) : P(cible) 0.7 % x 22.37 % + P(rien) 64.2 % x 3.59 % ne couvrent pas P(stop) 35.1 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 6.854 %) — p(stop avant cible) 0.3038 [0.26 ; 0.35], R/R 2.753, perte reelle 8.124 % (gap inclus), EV -0.0324 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 0.7 % x 22.37 % + P(rien) 68.9 % x 3.31 % ne couvrent pas P(stop) 30.4 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 8.568 %) — p(stop avant cible) 0.1911 [0.15 ; 0.23], R/R 2.331, perte reelle 9.596 % (gap inclus), EV 0.3152 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 9.424 %) — p(stop avant cible) 0.1493 [0.11 ; 0.19], R/R 2.331, perte reelle 9.596 % (gap inclus), EV 0.5449 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 10.281 %) — p(stop avant cible) 0.1161 [0.09 ; 0.15], R/R 2.175, perte reelle 10.281 % (gap inclus), EV 0.5744 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 11.995 %) — p(stop avant cible) 0.0778 [0.05 ; 0.11], R/R 1.865, perte reelle 11.995 % (gap inclus), EV 0.5701 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 13.708 %) — p(stop avant cible) 0.0382 [0.02 ; 0.06], R/R 1.632, perte reelle 13.708 % (gap inclus), EV 0.5768 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.71 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 15.422 %) — p(stop avant cible) 0.0188 [0.01 ; 0.04], R/R 1.45, perte reelle 15.422 % (gap inclus), EV 0.621 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.42 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 17.135 %) — p(stop avant cible) 0.0099 [0.00 ; 0.02], R/R 1.305, perte reelle 17.135 % (gap inclus), EV 0.624 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.14 % > budget 12.00 %
   - 🟢 grid_snapped a 5.65 ATR (stop 20.393 %) — p(stop avant cible) 0.0028 [0.00 ; 0.01], R/R 1.097, perte reelle 20.393 % (gap inclus), EV 0.6636 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.39 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 22.276 %) — p(stop avant cible) 0.0021 [0.00 ; 0.01], R/R 1.004, perte reelle 22.276 % (gap inclus), EV 0.6656 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.28 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 23.99 %) — p(stop avant cible) 0.0007 [0.00 ; 0.01], R/R 0.932, perte reelle 23.99 % (gap inclus), EV 0.6715 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.99 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 25.703 %) — p(stop avant cible) 0.0007 [0.00 ; 0.01], R/R 0.87, perte reelle 25.703 % (gap inclus), EV 0.6703 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.70 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 27.417 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.816, perte reelle 27.417 % (gap inclus), EV 0.6754 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.42 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 133.6, ATR14 4.5786 (3.427 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.349 ATR = 1.196 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.171 % | 133.3711 | 87.83 % | 91.45 % | 93.22 % | 95.27 % | 96.93 % | 97.8 % |
| 0.1 ATR | 0.343 % | 133.1421 | 82.14 % | 87.92 % | 90.46 % | 93.3 % | 95.54 % | 96.9 % |
| 0.15 ATR | 0.514 % | 132.9132 | 75.27 % | 83.6 % | 87.02 % | 90.34 % | 94.06 % | 95.6 % |
| 0.2 ATR | 0.685 % | 132.6843 | 68.69 % | 78.49 % | 83.28 % | 88.37 % | 92.67 % | 94.9 % |
| 0.25 ATR | 0.857 % | 132.4554 | 62.12 % | 73.77 % | 79.25 % | 85.22 % | 90.59 % | 93.7 % |
| 0.35 ATR | 1.199 % | 131.9975 | 49.85 % | 64.54 % | 71.98 % | 79.11 % | 86.63 % | 91.5 % |
| 0.5 ATR | 1.714 % | 131.3107 | 34.94 % | 52.75 % | 61.55 % | 70.84 % | 80.3 % | 87.3 % |
| 0.75 ATR | 2.57 % | 130.1661 | 20.61 % | 36.74 % | 47.59 % | 59.01 % | 70.2 % | 80.7 % |
| 1.0 ATR | 3.427 % | 129.0214 | 10.7 % | 24.36 % | 34.81 % | 48.67 % | 61.49 % | 74.0 % |
| 1.25 ATR | 4.284 % | 127.8768 | 4.91 % | 16.21 % | 24.98 % | 39.61 % | 54.36 % | 67.6 % |
| 1.5 ATR | 5.141 % | 126.7321 | 2.45 % | 11.0 % | 18.39 % | 30.54 % | 46.63 % | 59.9 % |
| 2.0 ATR | 6.854 % | 124.4429 | 0.79 % | 5.11 % | 9.93 % | 19.21 % | 35.25 % | 50.5 % |
| 2.5 ATR | 8.568 % | 122.1536 | 0.49 % | 2.65 % | 5.6 % | 11.33 % | 24.65 % | 38.7 % |
| 3.0 ATR | 10.281 % | 119.8643 | 0.2 % | 1.67 % | 3.24 % | 7.09 % | 17.62 % | 30.2 % |
| 4.0 ATR | 13.708 % | 115.2857 | 0.1 % | 0.49 % | 0.88 % | 1.87 % | 7.52 % | 17.9 % |
| 6.0 ATR | 20.562 % | 106.1286 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 1.39 % | 4.4 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.67 ATR | 0.77 ATR | 1.03 ATR | 1.25 ATR |
| **2 s.** | 0.24 ATR | 0.54 ATR | 0.62 ATR | 0.83 ATR | 0.99 ATR | 1.13 ATR | 1.58 ATR | 2.02 ATR |
| **3 s.** | 0.31 ATR | 0.71 ATR | 0.80 ATR | 1.05 ATR | 1.25 ATR | 1.44 ATR | 2.00 ATR | 2.63 ATR |
| **5 s.** | 0.42 ATR | 0.97 ATR | 1.10 ATR | 1.43 ATR | 1.74 ATR | 1.97 ATR | 2.66 ATR | 3.40 ATR |
| **10 s.** | 0.63 ATR | 1.39 ATR | 1.57 ATR | 2.11 ATR | 2.48 ATR | 2.83 ATR | 3.75 ATR | 4.82 ATR |
| **20 s.** | 0.96 ATR | 2.02 ATR | 2.23 ATR | 2.83 ATR | 3.42 ATR | 3.83 ATR | 5.17 ATR | 5.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.399–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (78.4 % des re-echantillons)
- **2 seance(s)** : plage utile 0.621–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.57 %, prix 130.1665), p(touche) 36.74 % (en stress 88.24 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.801–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.427 %, prix 129.0215), p(touche) 34.81 % (en stress 84.31 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.101–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.284 %, prix 127.8766), p(touche) 39.61 % (en stress 93.14 %)  ✅ optimum identifie (62.9 % des re-echantillons)
- **10 seance(s)** : plage utile 1.572–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.854 %, prix 124.4431), p(touche) 35.25 % (en stress 99.01 %)  ✅ optimum identifie (70.9 % des re-echantillons)
- **20 seance(s)** : plage utile 2.233–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.568 %, prix 122.1532), p(touche) 38.7 % (en stress 98.0 %)  ✅ optimum identifie (69.4 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.078 | EV/share : €-0.826 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 12 % | T3 3 %
- Kelly (position) : f* 0.236 | ¼-Kelly 0.059 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 12.6 | bear 28.0 | side 59.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.217% → cible +1.387% / stop −8.0%, p_fill 55%, n_eff≈22.8) : P(cible|rempli) **31%** · **EV/risk -0.033** (×p_fill ; si rempli -0.49% du capital)
  - **swing** (entrée dip −2.663% → cible +3.102% / stop −3.521%, p_fill 44%, n_eff≈18.7) : P(cible|rempli) **52%** · **EV/risk +0.036** (×p_fill ; si rempli +0.29% du capital)
  - **deep** (entrée dip −4.119% → cible +4.387% / stop −5.362%, p_fill 34%, n_eff≈18.8) : P(cible|rempli) **62%** · **EV/risk +0.099** (×p_fill ; si rempli +1.57% du capital)
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
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 39.5  _(momentum baissier)_
- **ADX** : 12.1  _(pas de tendance nette)_
- **MACD** : hist -0.713  _(pas de croisement recent)_
- **BB** : %B 0.05 · largeur 8.3%
- **ATR** : 4.58 (68.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.308  _(distribution)_
- **Vol ratio** : 0.33  _(volume atone)_
- **Choppiness** : 55.3  _(transition)_
- **MA** : MA20 138.85 · MA50 136.47 · MA200 134.59  _(prix < MA20)_
- **Dist MA** : MA20 -3.8% · MA50 -2.1% · MA200 -0.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (760144 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
