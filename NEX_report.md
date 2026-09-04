# NEX

**Generated** : 2026-09-04T21:43:57.208453+00:00  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · €136.60  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)  
> ↳ spot €136.60 (+4.1% vs entrée) · entrée €131.23 · stop €127.41 · T1 €134.15 · R/R 0.76  
> ↳ P(T1 av. stop) 64 % _(réel 5 s)_ · EV/risk 0.015 _(réel 5 s)_ (GBM -0.016) · ¼-Kelly 0.003 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €130.64–€131.81 (mid €131.23)
- Spot actuel : €136.60 (+4.1% au-dessus de la zone — repli à attendre)
- Stop : €127.41 (stop swing_plan-based (-6.73%))
- Targets : T1 €134.15 · R/R 0.76 | T2 €137.07 · R/R 1.53 | T3 €139.99 · R/R 2.29
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €127.41


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.64 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (6.73 %)** : le gap seul le franchit 0.469 % des séances (6 fois sur 1280).
   - exécution **1.438 pt plus bas** dans le cas TYPIQUE (médiane), 2.244 au p90, **2.866 au pire**
   - perte réelle **8.124 %** en moyenne _(tirée par la queue)_, jusqu'à **9.596 %** — au lieu des 6.73 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0065 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.516 % | p01 -3.643 % | pire -9.596 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0043** [0.0003 ; 0.0239] _(largeur 2.4 pt, n_eff 173.1)_
   - swing : **0.4343** [0.3828 ; 0.4869] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4076** [0.3568 ; 0.46] _(largeur 10.3 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 18.5 observations effectives », dont la borne haute a 95 % vaut environ 16.2 %.
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 14.5 observations effectives », dont la borne haute a 95 % vaut environ 20.8 %.
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 12.7 observations effectives », dont la borne haute a 95 % vaut environ 23.7 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (40.3 pt), swing (45.8 pt), deep (38.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-3.5 %** | CVaR **-5.21 %** | vol 2.3 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.51 % vs -7.85 % si l'on extrapolait par √5 _(rapport 0.956 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0134** (β de hausse 1.1032, asymétrie 0.9186) vs FCHI — 620 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 123.225 sur atr_grid (3.5 ATR, 9.791 %) — p(stop avant cible) 0.1327 [0.10 ; 0.17], R/R 2.027, perte reelle 9.791 % (gap inclus), CVaR 9.791 %, EV 0.6551 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.38 ATR (stop 2.711 %) — p(stop avant cible) 0.671 [0.62 ; 0.72], R/R 4.282, perte reelle 4.635 % (gap inclus), EV -1.2157 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.671, borne haute 0.719 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.22 %) : P(cible) 1.1 % x 19.84 % + P(rien) 31.8 % x 5.25 % ne couvrent pas P(stop) 67.1 % x 4.63 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 4.196 %) — p(stop avant cible) 0.5295 [0.48 ; 0.58], R/R 2.959, perte reelle 6.706 % (gap inclus), EV -1.1101 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.529, borne haute 0.582 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.11 %) : P(cible) 1.5 % x 19.84 % + P(rien) 45.6 % x 4.70 % ne couvrent pas P(stop) 52.9 % x 6.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 2.66 ATR (stop 9.069 %) — p(stop avant cible) 0.1682 [0.13 ; 0.21], R/R 2.068, perte reelle 9.596 % (gap inclus), EV 0.5252 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 7.56 ATR (stop 22.775 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.871, perte reelle 22.775 % (gap inclus), EV 0.7438 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.78 % > budget 12.00 %
   - ⚪ grid_snapped a 0.38 ATR (stop 1.911 %) — p(stop avant cible) 0.7512 [0.70 ; 0.79], R/R 5.47, perte reelle 3.628 % (gap inclus), EV -1.2589 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.751, borne haute 0.794 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.26 %) : P(cible) 1.1 % x 19.84 % + P(rien) 23.8 % x 5.27 % ne couvrent pas P(stop) 75.1 % x 3.63 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 3.497 %) — p(stop avant cible) 0.5756 [0.52 ; 0.63], R/R 3.548, perte reelle 5.593 % (gap inclus), EV -0.9684 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.576, borne haute 0.627 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.97 %) : P(cible) 1.5 % x 19.84 % + P(rien) 40.9 % x 4.77 % ne couvrent pas P(stop) 57.6 % x 5.59 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 4.896 %) — p(stop avant cible) 0.4527 [0.40 ; 0.51], R/R 2.578, perte reelle 7.697 % (gap inclus), EV -0.9113 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.91 %) : P(cible) 1.5 % x 19.84 % + P(rien) 53.2 % x 4.27 % ne couvrent pas P(stop) 45.3 % x 7.70 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 5.595 %) — p(stop avant cible) 0.4085 [0.36 ; 0.46], R/R 2.443, perte reelle 8.124 % (gap inclus), EV -0.7284 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.73 %) : P(cible) 1.5 % x 19.84 % + P(rien) 57.6 % x 3.98 % ne couvrent pas P(stop) 40.8 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 6.294 %) — p(stop avant cible) 0.3484 [0.30 ; 0.40], R/R 2.443, perte reelle 8.124 % (gap inclus), EV -0.3139 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.31 %) : P(cible) 1.5 % x 19.84 % + P(rien) 63.7 % x 3.48 % ne couvrent pas P(stop) 34.8 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.66 ATR (stop 8.269 %) — p(stop avant cible) 0.2093 [0.17 ; 0.25], R/R 2.211, perte reelle 8.974 % (gap inclus), EV 0.4714 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 9.791 %) — p(stop avant cible) 0.1327 [0.10 ; 0.17], R/R 2.027, perte reelle 9.791 % (gap inclus), EV 0.6551 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 11.19 %) — p(stop avant cible) 0.0914 [0.06 ; 0.13], R/R 1.773, perte reelle 11.19 % (gap inclus), EV 0.6526 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.5 ATR (stop 12.589 %) — p(stop avant cible) 0.0682 [0.05 ; 0.10], R/R 1.576, perte reelle 12.589 % (gap inclus), EV 0.6218 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.59 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 13.988 %) — p(stop avant cible) 0.0344 [0.02 ; 0.06], R/R 1.419, perte reelle 13.988 % (gap inclus), EV 0.6578 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.99 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 15.386 %) — p(stop avant cible) 0.0198 [0.01 ; 0.04], R/R 1.29, perte reelle 15.386 % (gap inclus), EV 0.6968 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.39 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 16.785 %) — p(stop avant cible) 0.0138 [0.01 ; 0.03], R/R 1.182, perte reelle 16.785 % (gap inclus), EV 0.6881 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.79 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 18.184 %) — p(stop avant cible) 0.0056 [0.00 ; 0.02], R/R 1.091, perte reelle 18.184 % (gap inclus), EV 0.7232 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.18 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 19.583 %) — p(stop avant cible) 0.003 [0.00 ; 0.01], R/R 1.013, perte reelle 19.583 % (gap inclus), EV 0.7403 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.58 % > budget 12.00 %
   - 🟢 grid_snapped a 7.56 ATR (stop 21.975 %) — p(stop avant cible) 0.0022 [0.00 ; 0.01], R/R 0.903, perte reelle 21.975 % (gap inclus), EV 0.7417 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.97 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 22.38 %) — p(stop avant cible) 0.0022 [0.00 ; 0.01], R/R 0.887, perte reelle 22.38 % (gap inclus), EV 0.7408 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.38 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 136.6, ATR14 3.8214 (2.798 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.348 ATR = 0.974 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.14 % | 136.4089 | 87.84 % | 91.46 % | 93.22 % | 95.28 % | 96.93 % | 97.8 % |
| 0.1 ATR | 0.28 % | 136.2179 | 82.06 % | 87.73 % | 90.28 % | 93.11 % | 95.45 % | 96.9 % |
| 0.15 ATR | 0.42 % | 136.0268 | 75.29 % | 83.51 % | 86.84 % | 90.16 % | 93.97 % | 95.6 % |
| 0.2 ATR | 0.56 % | 135.8357 | 68.63 % | 78.41 % | 83.3 % | 88.29 % | 92.58 % | 94.91 % |
| 0.25 ATR | 0.699 % | 135.6446 | 62.06 % | 73.6 % | 79.17 % | 85.04 % | 90.5 % | 93.71 % |
| 0.35 ATR | 0.979 % | 135.2625 | 49.8 % | 64.38 % | 71.91 % | 78.94 % | 86.55 % | 91.51 % |
| 0.5 ATR | 1.399 % | 134.6893 | 34.8 % | 52.7 % | 61.59 % | 70.77 % | 80.32 % | 87.41 % |
| 0.75 ATR | 2.098 % | 133.7339 | 20.39 % | 36.7 % | 47.64 % | 58.96 % | 70.23 % | 80.92 % |
| 1.0 ATR | 2.798 % | 132.7786 | 10.69 % | 24.53 % | 35.07 % | 48.82 % | 61.42 % | 74.33 % |
| 1.25 ATR | 3.497 % | 131.8232 | 4.9 % | 16.29 % | 25.15 % | 39.76 % | 54.4 % | 67.93 % |
| 1.5 ATR | 4.196 % | 130.8679 | 2.45 % | 10.99 % | 18.47 % | 30.71 % | 46.79 % | 60.34 % |
| 2.0 ATR | 5.595 % | 128.9571 | 0.78 % | 5.2 % | 9.92 % | 19.29 % | 35.41 % | 51.05 % |
| 2.5 ATR | 6.994 % | 127.0464 | 0.49 % | 2.65 % | 5.6 % | 11.42 % | 24.93 % | 39.26 % |
| 3.0 ATR | 8.393 % | 125.1357 | 0.2 % | 1.67 % | 3.24 % | 7.19 % | 17.71 % | 30.67 % |
| 4.0 ATR | 11.19 % | 121.3143 | 0.1 % | 0.49 % | 0.88 % | 1.87 % | 7.62 % | 18.08 % |
| 6.0 ATR | 16.785 % | 113.6714 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 1.38 % | 4.4 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.67 ATR | 0.76 ATR | 1.03 ATR | 1.25 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.62 ATR | 0.83 ATR | 0.99 ATR | 1.14 ATR | 1.58 ATR | 2.04 ATR |
| **3 s.** | 0.31 ATR | 0.71 ATR | 0.80 ATR | 1.05 ATR | 1.26 ATR | 1.44 ATR | 2.00 ATR | 2.63 ATR |
| **5 s.** | 0.42 ATR | 0.97 ATR | 1.10 ATR | 1.44 ATR | 1.75 ATR | 1.97 ATR | 2.67 ATR | 3.41 ATR |
| **10 s.** | 0.63 ATR | 1.40 ATR | 1.58 ATR | 2.12 ATR | 2.50 ATR | 2.84 ATR | 3.76 ATR | 4.84 ATR |
| **20 s.** | 0.97 ATR | 2.04 ATR | 2.26 ATR | 2.86 ATR | 3.45 ATR | 3.85 ATR | 5.18 ATR | 5.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.398–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (78.6 % des re-echantillons)
- **2 seance(s)** : plage utile 0.62–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.098 %, prix 133.7341), p(touche) 36.7 % (en stress 88.24 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.803–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.798 %, prix 132.7779), p(touche) 35.07 % (en stress 85.29 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.105–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (3.497 %, prix 131.8231), p(touche) 39.76 % (en stress 94.12 %)  ✅ optimum identifie (62.1 % des re-echantillons)
- **10 seance(s)** : plage utile 1.579–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (5.595 %, prix 128.9572), p(touche) 35.41 % (en stress 98.04 %)  ✅ optimum identifie (71.8 % des re-echantillons)
- **20 seance(s)** : plage utile 2.257–4.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (6.994 %, prix 127.0462), p(touche) 39.26 % (en stress 98.02 %)  ✅ optimum identifie (70.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.016 | EV/share : €-0.061 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 56 % | T2 31 % | T3 14 %
- Kelly (position) : f* 0.011 | ¼-Kelly 0.003 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 8.1 | bear 73.1 | side 18.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 137.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.783% → cible +0.995% / stop −8.0%, p_fill 44%, n_eff≈18.5) : P(cible|rempli) **33%** · **EV/risk -0.021** (×p_fill ; si rempli -0.38% du capital)
  - **swing** (entrée dip −3.932% → cible +2.224% / stop −2.912%, p_fill 18%, n_eff≈14.5) : P(cible|rempli) **64%** · **EV/risk +0.015** (×p_fill ; si rempli +0.23% du capital)
  - **deep** (entrée dip −6.073% → cible +3.146% / stop −4.468%, p_fill 16%, n_eff≈12.7) : P(cible|rempli) **84%** · **EV/risk +0.064** (×p_fill ; si rempli +1.77% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→62% · +1.0%→50% · +2.0%→24% · +3.0%→10% · +5.0%→1% · +8.0%→0%
- Range intraday médian 2.95% (p90 4.72%) · excursion haute méd. +1.0% / basse méd. −1.4%
- Profil de vol intra : ouverture 1.749% vs midi 0.519% vs clôture 0.71% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 48% · recovery-V 16%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; mean-reverting — autocorr -0.031)_ ; drift intra méd. -0.557% ; recovery-V 13%
- **σ réalisé intraday** 1.973% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 57% / bas 68% / whipsaw 25%
- POC intraday (dernière séance, temps-au-prix) : 137.9625 (VA 137.4625–139.4625 ; dernier close 137.25)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 16% · rebond 50% · **stop −1.94%** sous le fill (sous le bruit) · cible +1.05% · R/R 0.54 (high win-rate)
- Gaps overnight (n=159) : méd. 0.36% · baisse 33% (gap-down >1% 5% · >2% 1%)
- Excursion ouverture 5min (n=160) : bas méd −0.54% (p90 −1.8%) · haut méd +0.18% · range méd 1.03%
- Excursion ouverture 15min (n=160) : bas méd −0.75% (p90 −1.96%) · haut méd +0.37% · range méd 1.29%
- Excursion ouverture 30min (n=160) : bas méd −0.77% (p90 −2.24%) · haut méd +0.45% · range méd 1.42%
- Excursion ouverture 60min (n=160) : bas méd −0.87% (p90 −2.48%) · haut méd +0.57% · range méd 1.62%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 137.5 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 46% · séance 61% (92/159) · gap 11% · délai 2.9min · rebond 44% (44/92) (MFE +0.74%)
   - −1.0% : fill 30min 28% · séance 54% (76/159) · gap 5% · délai 24.0min · rebond 41% (35/76) (MFE +0.64%)
   - −1.5% : fill 30min 15% · séance 42% (57/159) · gap 1% · délai 42.0min · rebond 38% (25/57) (MFE +0.74%)
   - −2.0% : fill 30min 10% · séance 30% (42/159) · gap 1% · délai 66.4min · rebond 45% (20/42) (MFE +0.78%)
   - −3.0% : fill 30min 4% · séance 16% (24/159) · gap 0% · délai 207.9min · rebond 50% (13/24) (MFE +1.05%)
   - −4.0% : fill 30min 0% · séance 5% (9/159) · gap 0% · délai 350.2min · rebond 11% (3/9) (MFE +0.48%)
   - −5.0% : fill 30min 0% · séance 2% (3/159) · gap 0% · délai 410.2min · rebond 42% (1/3) (MFE +0.73%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.15% (p90 −0.98%) → stop au-delà de −0.81% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.15% (p90 −0.9%) → stop au-delà de −0.6% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.13% (p90 −0.6%) → stop au-delà de −0.44% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=326 jambes) : jambe baissière méd −1.07% (p90 −2.37%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (30 séances) :
      · −1.0% : fill 80% (25/30) · rebond 55% (13/25)
      · −2.0% : fill 50% (16/30) · rebond 44% (7/16)
      · −3.0% : fill 32% (11/30) · rebond 44% (6/11)
      · −4.0% : fill 21% (6/30) · rebond 12% (2/6)
      · −5.0% : fill 12% (3/30) · rebond 42% (1/3)
   - **flat** (35 séances) :
      · −1.0% : fill 58% (21/35) · rebond 37% (9/21)
      · −2.0% : fill 32% (11/35) · rebond 32% (4/11)
      · −3.0% : fill 21% (7/35) · rebond 33% (3/7)
      · −4.0% : fill 7% (2/35) · rebond 0% (0/2)
      · −5.0% : fill 0% (0/35) · rebond 0% (0/0)
   - **gap-up** (94 séances) :
      · −1.0% : fill 44% (30/94) · rebond 38% (13/30)
      · −2.0% : fill 24% (15/94) · rebond 55% (9/15)
      · −3.0% : fill 9% (6/94) · rebond 78% (4/6)
      · −4.0% : fill 0% (1/94) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/94) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 70% si les 15 1res min sont vertes (85 cas) · 17% si rouges (75 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **30min** → P(séance verte=clôture>ouverture) 76% si début vert vs 19% si rouge (base 44% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 221min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **76%** · continue >prix actuel 53% ; creux résiduel méd -0.95% (q20 -1.91%) → **SL/trailing à −1.91%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.15% / q75 +1.81% → **scale +1.15% / runner +1.81%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **19%** (continue à baisser 60%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.29%** (au-delà de la MAE q10 -3.29%), cible rebond +0.98% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.93% .. +2.16%] · haut q95 +2.52% · bas q05 -2.59%
   - 60min (n=160) : retour [-2.81% .. +2.48%] · haut q95 +2.7% · bas q05 -3.23%
   - 2h (n=160) : retour [-3.34% .. +2.47%] · haut q95 +2.93% · bas q05 -3.71%
   - 4h (n=160) : retour [-2.91% .. +3.23%] · haut q95 +3.3% · bas q05 -3.8%
   - 6h (n=160) : retour [-3.63% .. +3.68%] · haut q95 +3.95% · bas q05 -4.15%
   - session (n=160) : retour [-3.42% .. +2.83%] · haut q95 +3.94% · bas q05 -4.65%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.93%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 41.4  _(momentum baissier)_
- **ADX** : 12.3  _(pas de tendance nette)_
- **MACD** : hist -0.399  _(bearish_recent)_
- **BB** : %B 0.15 · largeur 6.4%
- **ATR** : 3.82 (34.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.347  _(distribution)_
- **Vol ratio** : 0.87  _(volume normal)_
- **Choppiness** : 63.9  _(marche en range (choppy))_
- **MA** : MA20 139.78 · MA50 136.93 · MA200 134.07  _(prix < MA20)_
- **Dist MA** : MA20 -2.3% · MA50 -0.2% · MA200 +1.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (760436 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
