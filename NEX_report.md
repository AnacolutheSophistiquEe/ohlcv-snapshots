# NEX

**Generated** : 2026-09-04T00:09:31.277754+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · €138.80  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)  
> ↳ spot €138.80 (+5.0% vs entrée) · entrée €132.22 · stop €128.55 · T1 €135.13 · R/R 0.79  
> ↳ P(T1 av. stop) 68 % · EV/risk -0.029 · ¼-Kelly 0.003 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €131.64–€132.80 (mid €132.22)
- Spot actuel : €138.80 (+5.0% au-dessus de la zone — repli à attendre)
- Stop : €128.55 (stop swing_plan-based (-7.38%))
- Targets : T1 €135.13 · R/R 0.79 | T2 €138.04 · R/R 1.59 | T3 €140.95 · R/R 2.38
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €128.55


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.64 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (7.38 %)** : le gap seul le franchit 0.312 % des séances (4 fois sur 1280).
   - exécution **0.93 pt plus bas** dans le cas TYPIQUE (médiane), 1.843 au p90, **2.216 au pire**
   - perte réelle **8.571 %** en moyenne _(tirée par la queue)_, jusqu'à **9.596 %** — au lieu des 7.38 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0037 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.516 % | p01 -3.643 % | pire -9.596 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0043** [0.0003 ; 0.0239] _(largeur 2.4 pt, n_eff 173.1)_
   - swing : **0.4382** [0.3866 ; 0.4908] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4134** [0.3624 ; 0.4658] _(largeur 10.3 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 15.7 observations effectives », dont la borne haute a 95 % vaut environ 19.1 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (44.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-3.51 %** | CVaR **-5.25 %** | vol 2.3 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.51 % vs -7.85 % si l'on extrapolait par √5 _(rapport 0.956 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0158** (β de hausse 1.104, asymétrie 0.9201) vs FCHI — 619 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 125.3677 sur grid_snapped (3.37 ATR, 9.677 %) — p(stop avant cible) 0.1345 [0.10 ; 0.17], R/R 1.858, perte reelle 9.677 % (gap inclus), CVaR 9.677 %, EV 0.6551 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 3.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.88 ATR (stop 3.866 %) — p(stop avant cible) 0.5525 [0.50 ; 0.60], R/R 2.875, perte reelle 6.254 % (gap inclus), EV -1.0549 % — **REFUSE**
      - refuse : cible atteinte seulement 3.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.552, borne haute 0.604 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.05 %) : P(cible) 3.3 % x 17.98 % + P(rien) 41.4 % x 4.36 % ne couvrent pas P(stop) 55.2 % x 6.25 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 3.37 ATR (stop 10.422 %) — p(stop avant cible) 0.1191 [0.09 ; 0.16], R/R 1.725, perte reelle 10.422 % (gap inclus), EV 0.6283 % — **REFUSE**
      - refuse : cible atteinte seulement 3.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 8.48 ATR (stop 23.922 %) — p(stop avant cible) 0.0007 [0.00 ; 0.01], R/R 0.752, perte reelle 23.922 % (gap inclus), EV 0.7382 % — **REFUSE**
      - refuse : cible atteinte seulement 3.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.92 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.66 %) — p(stop avant cible) 0.9136 [0.88 ; 0.94], R/R 10.996, perte reelle 1.635 % (gap inclus), EV -0.7925 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 11.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.914, borne haute 0.940 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.79 %) : P(cible) 1.1 % x 17.98 % + P(rien) 7.6 % x 6.75 % ne couvrent pas P(stop) 91.4 % x 1.64 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.32 %) — p(stop avant cible) 0.8401 [0.80 ; 0.88], R/R 6.684, perte reelle 2.69 % (gap inclus), EV -1.1167 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 6.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.840, borne haute 0.876 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.12 %) : P(cible) 1.5 % x 17.98 % + P(rien) 14.5 % x 6.00 % ne couvrent pas P(stop) 84.0 % x 2.69 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.88 ATR (stop 3.121 %) — p(stop avant cible) 0.6264 [0.57 ; 0.68], R/R 3.555, perte reelle 5.057 % (gap inclus), EV -1.0302 % — **REFUSE**
      - refuse : cible atteinte seulement 2.9 % du temps (< 15 %) meme a 10 seances : le R/R de 3.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.626, borne haute 0.676 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.03 %) : P(cible) 2.9 % x 17.98 % + P(rien) 34.4 % x 4.67 % ne couvrent pas P(stop) 62.6 % x 5.06 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 4.62 %) — p(stop avant cible) 0.4727 [0.42 ; 0.53], R/R 2.336, perte reelle 7.697 % (gap inclus), EV -1.081 % — **REFUSE**
      - refuse : cible atteinte seulement 3.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.08 %) : P(cible) 3.3 % x 17.98 % + P(rien) 49.4 % x 3.97 % ne couvrent pas P(stop) 47.3 % x 7.70 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 5.28 %) — p(stop avant cible) 0.4256 [0.37 ; 0.48], R/R 2.213, perte reelle 8.124 % (gap inclus), EV -0.8656 % — **REFUSE**
      - refuse : cible atteinte seulement 3.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.87 %) : P(cible) 3.3 % x 17.98 % + P(rien) 54.1 % x 3.69 % ne couvrent pas P(stop) 42.6 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 5.94 %) — p(stop avant cible) 0.3858 [0.34 ; 0.44], R/R 2.213, perte reelle 8.124 % (gap inclus), EV -0.5301 % — **REFUSE**
      - refuse : cible atteinte seulement 3.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 3.3 % x 17.98 % + P(rien) 58.1 % x 3.46 % ne couvrent pas P(stop) 38.6 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 6.6 %) — p(stop avant cible) 0.3261 [0.28 ; 0.38], R/R 2.213, perte reelle 8.124 % (gap inclus), EV -0.1062 % — **REFUSE**
      - refuse : cible atteinte seulement 3.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.11 %) : P(cible) 3.3 % x 17.98 % + P(rien) 64.1 % x 3.04 % ne couvrent pas P(stop) 32.6 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 7.26 %) — p(stop avant cible) 0.2708 [0.23 ; 0.32], R/R 2.158, perte reelle 8.333 % (gap inclus), EV 0.219 % — **REFUSE**
      - refuse : cible atteinte seulement 3.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 7.92 %) — p(stop avant cible) 0.2228 [0.18 ; 0.27], R/R 2.098, perte reelle 8.571 % (gap inclus), EV 0.5 % — **REFUSE**
      - refuse : cible atteinte seulement 3.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 3.37 ATR (stop 9.677 %) — p(stop avant cible) 0.1345 [0.10 ; 0.17], R/R 1.858, perte reelle 9.677 % (gap inclus), EV 0.6551 % — **REFUSE**
      - refuse : cible atteinte seulement 3.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.5 ATR (stop 11.88 %) — p(stop avant cible) 0.0811 [0.06 ; 0.11], R/R 1.513, perte reelle 11.88 % (gap inclus), EV 0.6407 % — **REFUSE**
      - refuse : cible atteinte seulement 3.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 5.0 ATR (stop 13.2 %) — p(stop avant cible) 0.0501 [0.03 ; 0.08], R/R 1.362, perte reelle 13.2 % (gap inclus), EV 0.6276 % — **REFUSE**
      - refuse : cible atteinte seulement 3.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.20 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 14.52 %) — p(stop avant cible) 0.0266 [0.01 ; 0.05], R/R 1.238, perte reelle 14.52 % (gap inclus), EV 0.6729 % — **REFUSE**
      - refuse : cible atteinte seulement 3.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.52 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 15.84 %) — p(stop avant cible) 0.0139 [0.01 ; 0.03], R/R 1.135, perte reelle 15.84 % (gap inclus), EV 0.6907 % — **REFUSE**
      - refuse : cible atteinte seulement 3.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.84 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 17.16 %) — p(stop avant cible) 0.0103 [0.00 ; 0.03], R/R 1.048, perte reelle 17.16 % (gap inclus), EV 0.6877 % — **REFUSE**
      - refuse : cible atteinte seulement 3.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.16 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 18.48 %) — p(stop avant cible) 0.0056 [0.00 ; 0.02], R/R 0.973, perte reelle 18.48 % (gap inclus), EV 0.7114 % — **REFUSE**
      - refuse : cible atteinte seulement 3.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.48 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 19.8 %) — p(stop avant cible) 0.003 [0.00 ; 0.01], R/R 0.908, perte reelle 19.8 % (gap inclus), EV 0.7296 % — **REFUSE**
      - refuse : cible atteinte seulement 3.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.80 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 21.12 %) — p(stop avant cible) 0.0022 [0.00 ; 0.01], R/R 0.851, perte reelle 21.12 % (gap inclus), EV 0.7335 % — **REFUSE**
      - refuse : cible atteinte seulement 3.3 % du temps (< 15 %) meme a 10 seances : le R/R de 0.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.12 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 138.8, ATR14 3.6643 (2.64 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.348 ATR = 0.919 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.132 % | 138.6168 | 87.84 % | 91.46 % | 93.22 % | 95.28 % | 96.93 % | 97.8 % |
| 0.1 ATR | 0.264 % | 138.4336 | 82.06 % | 87.73 % | 90.28 % | 93.11 % | 95.45 % | 96.9 % |
| 0.15 ATR | 0.396 % | 138.2504 | 75.39 % | 83.51 % | 86.84 % | 90.16 % | 93.97 % | 95.6 % |
| 0.2 ATR | 0.528 % | 138.0671 | 68.63 % | 78.41 % | 83.2 % | 88.19 % | 92.48 % | 94.91 % |
| 0.25 ATR | 0.66 % | 137.8839 | 62.06 % | 73.6 % | 79.08 % | 84.94 % | 90.41 % | 93.71 % |
| 0.35 ATR | 0.924 % | 137.5175 | 49.8 % | 64.38 % | 71.81 % | 78.84 % | 86.45 % | 91.51 % |
| 0.5 ATR | 1.32 % | 136.9679 | 34.8 % | 52.7 % | 61.49 % | 70.67 % | 80.22 % | 87.41 % |
| 0.75 ATR | 1.98 % | 136.0518 | 20.39 % | 36.7 % | 47.54 % | 58.86 % | 70.23 % | 80.92 % |
| 1.0 ATR | 2.64 % | 135.1357 | 10.69 % | 24.53 % | 35.07 % | 48.72 % | 61.42 % | 74.43 % |
| 1.25 ATR | 3.3 % | 134.2196 | 4.9 % | 16.29 % | 25.15 % | 39.67 % | 54.4 % | 68.03 % |
| 1.5 ATR | 3.96 % | 133.3036 | 2.45 % | 10.99 % | 18.47 % | 30.61 % | 46.79 % | 60.44 % |
| 2.0 ATR | 5.28 % | 131.4714 | 0.78 % | 5.2 % | 9.92 % | 19.29 % | 35.41 % | 51.05 % |
| 2.5 ATR | 6.6 % | 129.6393 | 0.49 % | 2.65 % | 5.6 % | 11.42 % | 24.93 % | 39.26 % |
| 3.0 ATR | 7.92 % | 127.8071 | 0.2 % | 1.67 % | 3.24 % | 7.19 % | 17.71 % | 30.67 % |
| 4.0 ATR | 10.56 % | 124.1429 | 0.1 % | 0.49 % | 0.88 % | 1.87 % | 7.62 % | 18.08 % |
| 6.0 ATR | 15.84 % | 116.8143 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 1.38 % | 4.4 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.67 ATR | 0.76 ATR | 1.03 ATR | 1.25 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.62 ATR | 0.83 ATR | 0.99 ATR | 1.14 ATR | 1.58 ATR | 2.04 ATR |
| **3 s.** | 0.31 ATR | 0.71 ATR | 0.80 ATR | 1.05 ATR | 1.26 ATR | 1.44 ATR | 2.00 ATR | 2.63 ATR |
| **5 s.** | 0.42 ATR | 0.97 ATR | 1.10 ATR | 1.43 ATR | 1.75 ATR | 1.97 ATR | 2.67 ATR | 3.41 ATR |
| **10 s.** | 0.63 ATR | 1.40 ATR | 1.58 ATR | 2.12 ATR | 2.50 ATR | 2.84 ATR | 3.76 ATR | 4.84 ATR |
| **20 s.** | 0.98 ATR | 2.04 ATR | 2.26 ATR | 2.86 ATR | 3.45 ATR | 3.85 ATR | 5.18 ATR | 5.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.398–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (78.1 % des re-echantillons)
- **2 seance(s)** : plage utile 0.62–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.98 %, prix 136.0518), p(touche) 36.7 % (en stress 88.24 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.801–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.64 %, prix 135.1357), p(touche) 35.07 % (en stress 85.29 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.103–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (3.3 %, prix 134.2196), p(touche) 39.67 % (en stress 94.12 %)  ✅ optimum identifie (63.6 % des re-echantillons)
- **10 seance(s)** : plage utile 1.579–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (5.28 %, prix 131.4714), p(touche) 35.41 % (en stress 98.04 %)  ✅ optimum identifie (72.2 % des re-echantillons)
- **20 seance(s)** : plage utile 2.257–4.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (6.6 %, prix 129.6392), p(touche) 39.26 % (en stress 98.02 %)  ✅ optimum identifie (70.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.017 | EV/share : €-0.062 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 55 % | T2 31 % | T3 14 %
- Kelly (position) : f* 0.01 | ¼-Kelly 0.003 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 10.2 | bear 73.0 | side 16.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 278.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.152% → cible +0.984% / stop −8.0%, p_fill 38%, n_eff≈15.7) : P(cible|rempli) **36%** · **EV/risk -0.005** (×p_fill ; si rempli -0.10% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=13, n_eff=9))
  - **deep** : indisponible (échantillon insuffisant (n=11, n_eff=7))
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

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 47.5  _(neutre)_
- **ADX** : 12.4  _(pas de tendance nette)_
- **MACD** : hist -0.237  _(bearish_recent)_
- **BB** : %B 0.37 · largeur 6.0%
- **ATR** : 3.66 (26.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.339  _(distribution)_
- **Vol ratio** : 0.24  _(volume atone)_
- **Choppiness** : 62.3  _(marche en range (choppy))_
- **MA** : MA20 139.94 · MA50 137.03 · MA200 133.99  _(prix < MA20)_
- **Dist MA** : MA20 -0.8% · MA50 +1.3% · MA200 +3.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (755182 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
