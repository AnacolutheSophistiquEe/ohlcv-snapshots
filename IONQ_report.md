# IONQ

**Generated** : 2026-09-01T00:27:51.775114+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $39.31  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $39.31 (+0.5% vs entrée) · entrée $39.13 · stop $38.27 · T1 $40.31 · R/R 1.37  
> ↳ P(T1 av. stop) 30 % _(réel 5 s)_ · EV/risk -0.129 _(réel 5 s)_ (GBM 0.048) · ¼-Kelly 0.02 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.2% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -31 % hors [0,100] (R² max 0.10). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $38.96–$39.31 (mid $39.13)
- Spot actuel : $39.31 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : $38.27 (stop swing_plan-based (-8.27%))
- Targets : T1 $40.31 · R/R 1.37 | T2 $41.48 · R/R 2.73 | T3 $42.65 · R/R 4.09
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $38.27


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.78 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.27 %)** : le gap seul le franchit 0.638 % des séances (8 fois sur 1253).
   - exécution **1.655 pt plus bas** dans le cas TYPIQUE (médiane), 6.65 au p90, **13.589 au pire**
   - perte réelle **11.379 %** en moyenne _(tirée par la queue)_, jusqu'à **21.859 %** — au lieu des 8.27 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0199 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 8 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.035 % | p01 -6.632 % | pire -21.859 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5513** [0.4769 ; 0.624] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4633** [0.4112 ; 0.516] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4458** [0.394 ; 0.4985] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (30.8 pt), swing (31.3 pt), deep (31.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-8.37 %** | CVaR **-10.04 %** | vol 6.11 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 9.71 % contre 6.02 % aujourd'hui, rapport 1.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -18.23 % vs -19.88 % si l'on extrapolait par √5 _(rapport 0.917 ; < 1 = le √5 surestime)_
- **β de baisse : 2.2203** (β de hausse 1.9911, asymétrie 1.1151) vs IWM — 603 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 35.0066 sur atr_based (1.5 ATR, 10.947 %) — p(stop avant cible) 0.5291 [0.48 ; 0.58], R/R 2.36, perte reelle 15.082 % (gap inclus), CVaR 10.957 %, EV -1.0854 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.0569 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 10.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.529, borne haute 0.581 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.46 ATR (stop 6.252 %) — p(stop avant cible) 0.7387 [0.69 ; 0.78], R/R 4.026, perte reelle 8.842 % (gap inclus), EV -1.4476 % — **REFUSE**
      - refuse : cible atteinte seulement 8.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.739, borne haute 0.783 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.15 ATR du spot — compartiment <1, mesure a 46.4 % de casse (IC clusterise [0.430 ; 0.496] sur 1146 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.45 %) : P(cible) 8.0 % x 35.59 % + P(rien) 18.1 % x 12.36 % ne couvrent pas P(stop) 73.9 % x 8.84 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 10.947 %) — p(stop avant cible) 0.5291 [0.48 ; 0.58], R/R 2.36, perte reelle 15.082 % (gap inclus), EV -1.0854 % — **REFUSE**
      - refuse : cible atteinte seulement 10.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.529, borne haute 0.581 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.09 %) : P(cible) 10.1 % x 35.59 % + P(rien) 37.0 % x 8.89 % ne couvrent pas P(stop) 52.9 % x 15.08 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.79 ATR (stop 15.969 %) — p(stop avant cible) 0.3287 [0.28 ; 0.38], R/R 1.628, perte reelle 21.859 % (gap inclus), EV -1.1021 % — **REFUSE**
      - refuse : cible atteinte seulement 10.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.97 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.10 %) : P(cible) 10.8 % x 35.59 % + P(rien) 56.3 % x 3.97 % ne couvrent pas P(stop) 32.9 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.25 ATR (stop 26.628 %) — p(stop avant cible) 0.0897 [0.06 ; 0.12], R/R 1.337, perte reelle 26.628 % (gap inclus), EV 1.3406 % — **REFUSE**
      - refuse : cible atteinte seulement 10.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.63 % > budget 12.00 %
   - ⚪ atr_grid a 1.0 ATR (stop 7.298 %) — p(stop avant cible) 0.6685 [0.62 ; 0.72], R/R 3.346, perte reelle 10.638 % (gap inclus), EV -1.0478 % — **REFUSE**
      - refuse : cible atteinte seulement 9.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.668, borne haute 0.717 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.05 %) : P(cible) 9.2 % x 35.59 % + P(rien) 23.9 % x 11.60 % ne couvrent pas P(stop) 66.8 % x 10.64 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 9.123 %) — p(stop avant cible) 0.613 [0.56 ; 0.66], R/R 2.734, perte reelle 13.019 % (gap inclus), EV -1.4894 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.613, borne haute 0.663 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.49 %) : P(cible) 9.3 % x 35.59 % + P(rien) 29.4 % x 10.80 % ne couvrent pas P(stop) 61.3 % x 13.02 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 18.245 %) — p(stop avant cible) 0.2596 [0.22 ; 0.31], R/R 1.628, perte reelle 21.859 % (gap inclus), EV 0.0964 % — **REFUSE**
      - refuse : cible atteinte seulement 10.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.25 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 20.07 %) — p(stop avant cible) 0.2071 [0.17 ; 0.25], R/R 1.628, perte reelle 21.859 % (gap inclus), EV 0.8753 % — **REFUSE**
      - refuse : cible atteinte seulement 10.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.07 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 25.544 %) — p(stop avant cible) 0.0994 [0.07 ; 0.13], R/R 1.393, perte reelle 25.544 % (gap inclus), EV 1.3726 % — **REFUSE**
      - refuse : cible atteinte seulement 10.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.54 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 29.193 %) — p(stop avant cible) 0.0712 [0.05 ; 0.10], R/R 1.219, perte reelle 29.193 % (gap inclus), EV 1.1995 % — **REFUSE**
      - refuse : cible atteinte seulement 10.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.19 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 32.842 %) — p(stop avant cible) 0.0287 [0.01 ; 0.05], R/R 1.084, perte reelle 32.842 % (gap inclus), EV 1.2766 % — **REFUSE**
      - refuse : cible atteinte seulement 10.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.84 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 36.491 %) — p(stop avant cible) 0.0156 [0.01 ; 0.03], R/R 0.975, perte reelle 36.491 % (gap inclus), EV 1.323 % — **REFUSE**
      - refuse : cible atteinte seulement 10.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.49 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 40.14 %) — p(stop avant cible) 0.0061 [0.00 ; 0.02], R/R 0.887, perte reelle 40.14 % (gap inclus), EV 1.3648 % — **REFUSE**
      - refuse : cible atteinte seulement 10.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.14 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 43.789 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.813, perte reelle 43.789 % (gap inclus), EV 1.3876 % — **REFUSE**
      - refuse : cible atteinte seulement 10.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.79 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 47.438 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 0.75, perte reelle 47.438 % (gap inclus), EV 1.4068 % — **REFUSE**
      - refuse : cible atteinte seulement 10.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.44 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 51.087 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.697, perte reelle 51.087 % (gap inclus), EV 1.424 % — **REFUSE**
      - refuse : cible atteinte seulement 10.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 51.09 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 54.736 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.65, perte reelle 54.736 % (gap inclus), EV 1.424 % — **REFUSE**
      - refuse : cible atteinte seulement 10.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 54.74 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 58.385 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.61, perte reelle 58.385 % (gap inclus), EV 1.424 % — **REFUSE**
      - refuse : cible atteinte seulement 10.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 58.39 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 39.31, ATR14 2.8689 (7.298 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.383 ATR = 2.795 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.365 % | 39.1666 | 93.66 % | 95.36 % | 96.06 % | 97.47 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.73 % | 39.0231 | 86.0 % | 91.13 % | 92.13 % | 94.64 % | 96.04 % | 96.92 % |
| 0.15 ATR | 1.095 % | 38.8797 | 79.25 % | 86.29 % | 88.4 % | 91.71 % | 93.8 % | 95.69 % |
| 0.2 ATR | 1.46 % | 38.7362 | 71.8 % | 80.54 % | 84.36 % | 88.57 % | 91.06 % | 93.63 % |
| 0.25 ATR | 1.825 % | 38.5928 | 65.86 % | 76.71 % | 80.83 % | 85.95 % | 88.82 % | 92.09 % |
| 0.35 ATR | 2.554 % | 38.3059 | 53.37 % | 67.74 % | 74.27 % | 79.37 % | 84.15 % | 88.5 % |
| 0.5 ATR | 3.649 % | 37.8755 | 38.17 % | 54.84 % | 62.46 % | 71.08 % | 78.56 % | 84.6 % |
| 0.75 ATR | 5.474 % | 37.1583 | 22.36 % | 39.01 % | 48.34 % | 58.85 % | 68.9 % | 76.69 % |
| 1.0 ATR | 7.298 % | 36.4411 | 9.97 % | 24.5 % | 34.81 % | 45.9 % | 57.83 % | 67.97 % |
| 1.25 ATR | 9.123 % | 35.7239 | 3.63 % | 14.31 % | 24.12 % | 34.78 % | 50.0 % | 61.81 % |
| 1.5 ATR | 10.947 % | 35.0066 | 1.01 % | 7.06 % | 15.84 % | 25.68 % | 41.16 % | 55.95 % |
| 2.0 ATR | 14.596 % | 33.5722 | 0.1 % | 1.92 % | 4.94 % | 14.56 % | 28.56 % | 44.76 % |
| 2.5 ATR | 18.245 % | 32.1377 | 0.0 % | 0.2 % | 1.21 % | 5.76 % | 18.29 % | 33.78 % |
| 3.0 ATR | 21.895 % | 30.7033 | 0.0 % | 0.1 % | 0.4 % | 2.63 % | 11.38 % | 25.87 % |
| 4.0 ATR | 29.193 % | 27.8343 | 0.0 % | 0.1 % | 0.1 % | 0.2 % | 2.95 % | 10.57 % |
| 6.0 ATR | 43.789 % | 22.0965 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.1 % | 1.23 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.58 ATR | 0.71 ATR | 0.80 ATR | 1.00 ATR | 1.20 ATR |
| **2 s.** | 0.27 ATR | 0.58 ATR | 0.66 ATR | 0.85 ATR | 0.99 ATR | 1.11 ATR | 1.40 ATR | 1.70 ATR |
| **3 s.** | 0.34 ATR | 0.72 ATR | 0.81 ATR | 1.04 ATR | 1.23 ATR | 1.37 ATR | 1.77 ATR | 2.00 ATR |
| **5 s.** | 0.43 ATR | 0.92 ATR | 1.02 ATR | 1.30 ATR | 1.53 ATR | 1.75 ATR | 2.26 ATR | 2.62 ATR |
| **10 s.** | 0.59 ATR | 1.25 ATR | 1.39 ATR | 1.82 ATR | 2.17 ATR | 2.42 ATR | 3.16 ATR | 3.76 ATR |
| **20 s.** | 0.80 ATR | 1.77 ATR | 1.99 ATR | 2.55 ATR | 3.06 ATR | 3.38 ATR | 4.12 ATR | 5.19 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.433–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.655–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.474 %, prix 37.1582), p(touche) 39.01 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.812–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.298 %, prix 36.4412), p(touche) 34.81 % (en stress 92.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.02–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (9.123 %, prix 35.7237), p(touche) 34.78 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.391–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.947 %, prix 35.0067), p(touche) 41.16 % (en stress 97.98 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.989–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (14.596 %, prix 33.5723), p(touche) 44.76 % (en stress 98.98 %)  ✅ optimum identifie (68.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.048 | EV/share : $0.041 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 46 % | T2 27 % | T3 27 %
- Kelly (position) : f* 0.078 | ¼-Kelly 0.02 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 67.2 | bear 24.4 | side 8.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.45% → cible +3.0% / stop −2.199%, p_fill 91%, n_eff≈37.8) : P(cible|rempli) **30%** · **EV/risk -0.129** (×p_fill ; si rempli -0.31% du capital)
  - **swing** (entrée dip −0.972% → cible +6.708% / stop −7.369%, p_fill 88%, n_eff≈36.3) : P(cible|rempli) **44%** · **EV/risk -0.031** (×p_fill ; si rempli -0.26% du capital)
  - **deep** (entrée dip −1.403% → cible +9.486% / stop −11.103%, p_fill 86%, n_eff≈35.4) : P(cible|rempli) **47%** · **EV/risk -0.061** (×p_fill ; si rempli -0.78% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→80% · +2.0%→65% · +3.0%→55% · +5.0%→30% · +8.0%→14%
- Range intraday médian 7.47% (p90 12.17%) · excursion haute méd. +3.54% / basse méd. −2.69%
- Profil de vol intra : ouverture 5.242% vs midi 1.48% vs clôture 1.645% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 20% · trend ↑0%/↓0% ; spike-down 70% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.129 ; neutre — autocorr -0.009)_ ; drift intra méd. -0.2% ; recovery-V 22%
- **σ réalisé intraday** 4.246% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 56% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 38.84 (VA 38.68–39.72 ; dernier close 39.17)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 36% · rebond 77% · **stop −4.73%** sous le fill (sous le bruit) · cible +2.51% · R/R 0.53 (high win-rate)
- Gaps overnight (n=159) : méd. -0.41% · baisse 54% (gap-down >1% 38% · >2% 20%)
- Excursion ouverture 5min (n=160) : bas méd −1.2% (p90 −2.79%) · haut méd +1.32% · range méd 2.77%
- Excursion ouverture 15min (n=160) : bas méd −1.65% (p90 −3.96%) · haut méd +1.49% · range méd 3.62%
- Excursion ouverture 30min (n=160) : bas méd −1.93% (p90 −5.14%) · haut méd +1.95% · range méd 4.42%
- Excursion ouverture 60min (n=160) : bas méd −2.33% (p90 −5.41%) · haut méd +2.17% · range méd 5.15%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 39.2 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 72% · séance 80% (132/159) · gap 48% · délai 0.0min · rebond 58% (84/132) (MFE +1.81%)
   - −1.0% : fill 30min 68% · séance 74% (124/159) · gap 38% · délai 0.0min · rebond 67% (89/124) (MFE +2.08%)
   - −1.5% : fill 30min 62% · séance 68% (116/159) · gap 34% · délai 0.0min · rebond 66% (79/116) (MFE +1.84%)
   - −2.0% : fill 30min 56% · séance 62% (107/159) · gap 20% · délai 0.0min · rebond 69% (74/107) (MFE +2.19%)
   - −3.0% : fill 30min 46% · séance 55% (92/159) · gap 9% · délai 5.7min · rebond 67% (65/92) (MFE +2.19%)
   - −4.0% : fill 30min 27% · séance 45% (76/159) · gap 5% · délai 20.2min · rebond 64% (56/76) (MFE +2.02%)
   - −5.0% : fill 30min 18% · séance 36% (63/159) · gap 3% · délai 24.8min · rebond 77% (53/63) (MFE +2.51%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.76% (p90 −2.89%) → stop au-delà de −2.13% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.85% (p90 −2.89%) → stop au-delà de −2.21% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.84% (p90 −2.7%) → stop au-delà de −1.83% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1118 jambes) : jambe baissière méd −1.3% (p90 −3.06%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (79 séances) :
      · −1.0% : fill 100% (79/79) · rebond 66% (56/79)
      · −2.0% : fill 91% (73/79) · rebond 72% (54/73)
      · −3.0% : fill 80% (63/79) · rebond 66% (45/63)
      · −4.0% : fill 64% (50/79) · rebond 62% (37/50)
      · −5.0% : fill 50% (41/79) · rebond 69% (32/41)
   - **flat** (15 séances) :
      · −1.0% : fill 78% (12/15) · rebond 65% (7/12)
      · −2.0% : fill 69% (11/15) · rebond 79% (6/11)
      · −3.0% : fill 62% (9/15) · rebond 62% (6/9)
      · −4.0% : fill 54% (8/15) · rebond 53% (4/8)
      · −5.0% : fill 39% (7/15) · rebond 95% (6/7)
   - **gap-up** (65 séances) :
      · −1.0% : fill 38% (33/65) · rebond 74% (26/33)
      · −2.0% : fill 24% (23/65) · rebond 49% (14/23)
      · −3.0% : fill 20% (20/65) · rebond 76% (14/20)
      · −4.0% : fill 18% (18/65) · rebond 79% (15/18)
      · −5.0% : fill 15% (15/65) · rebond 100% (15/15)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 57% si les 15 1res min sont vertes (81 cas) · 28% si rouges (79 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:05** → P(séance verte=clôture>ouverture) 71% si début vert vs 17% si rouge (base 44% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **71%** · continue >prix actuel 45% ; creux résiduel méd -2.27% (q20 -4.03%) → **SL/trailing à −4.03%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.7% / q75 +4.24% → **scale +1.7% / runner +4.24%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **17%** (continue à baisser 54%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.75%** (au-delà de la MAE q10 -4.75%), cible rebond +1.8% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.82% .. +6.53%] · haut q95 +7.76% · bas q05 -5.53%
   - 60min (n=160) : retour [-4.94% .. +6.04%] · haut q95 +8.18% · bas q05 -6.1%
   - 2h (n=160) : retour [-6.35% .. +7.73%] · haut q95 +8.69% · bas q05 -6.99%
   - 4h (n=160) : retour [-6.91% .. +6.96%] · haut q95 +9.89% · bas q05 -8.08%
   - 6h (n=160) : retour [-7.17% .. +7.97%] · haut q95 +10.27% · bas q05 -8.15%
   - session (n=160) : retour [-6.48% .. +8.46%] · haut q95 +10.48% · bas q05 -8.28%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 7.7)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **28%**. Lecture précoce 30 min : signature présente → 14% vs absente 4% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.29% (p75 2.28% / p90 3.82%) · ~3.0 replis/séance, durée méd 69.04 min. P(nouveau plus-haut après repli) :
   - −0.5% → **85%** (reprise méd 24.37 min, n=47)
   - −1.0% → **78%** (reprise méd 68.85 min, n=30)
   - −1.5% → **68%** (reprise méd 81.24 min, n=16)
   - −2.0% → **67%** (reprise méd 84.17 min, n=12)
   - −3.0% → **75%** (reprise méd 175.72 min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−3.82%** (p90, défaut prudent ; serré/agressif −2.28%) ; extension open→close méd +8.23% (q75 +10.03% / q95 +16.4%), MFE méd +10.28% / q90 +13.1%
   - Échelle scale-out : +10.28% (33%) / +11.83% (33%) / +13.1% (34%)
- **DÉSARMER** : repli > **−3.82%** depuis le plus-haut = décay → P(retournement) **30%** (préavis méd 235.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.1% : P(retournement après) 0% (mèche méd 3.44%)
- **CONTEXTE** : la dernière heure tient les gains 80% du temps (retour médian dernière heure +0.52%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 41.8  _(momentum baissier)_
- **ADX** : 15.8  _(pas de tendance nette)_
- **MACD** : hist -0.345  _(bearish_recent)_
- **BB** : %B 0.14 · largeur 22.0%
- **ATR** : 2.87 (18.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.053  _(distribution)_
- **Vol ratio** : 1.91  _(volume au-dessus de la moyenne)_
- **Choppiness** : 54.6  _(transition)_
- **MA** : MA20 42.65 · MA50 42.54 · MA200 44.4  _(prix < MA20)_
- **Dist MA** : MA20 -7.8% · MA50 -7.6% · MA200 -11.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (783410 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
