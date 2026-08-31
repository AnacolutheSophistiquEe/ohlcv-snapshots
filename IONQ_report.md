# IONQ

**Generated** : 2026-08-31T00:28:02.156766+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $39.20  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $39.20 (+0.5% vs entrée) · entrée $39.02 · stop $38.16 · T1 $40.23 · R/R 1.41  
> ↳ P(T1 av. stop) 30 % _(réel 5 s)_ · EV/risk -0.114 _(réel 5 s)_ (GBM 0.048) · ¼-Kelly 0.02 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.19% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -31 % hors [0,100] (R² max 0.10). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $38.84–$39.20 (mid $39.02)
- Spot actuel : $39.20 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : $38.16 (stop swing_plan-based (-8.18%))
- Targets : T1 $40.23 · R/R 1.41 | T2 $41.44 · R/R 2.81 | T3 $42.65 · R/R 4.22
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $38.16


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.77 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.18 %)** : le gap seul le franchit 0.638 % des séances (8 fois sur 1254).
   - exécution **1.745 pt plus bas** dans le cas TYPIQUE (médiane), 6.74 au p90, **13.679 au pire**
   - perte réelle **11.379 %** en moyenne _(tirée par la queue)_, jusqu'à **21.859 %** — au lieu des 8.18 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0204 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 8 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.033 % | p01 -6.63 % | pire -21.859 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5464** [0.472 ; 0.6193] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4618** [0.4097 ; 0.5145] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4496** [0.3978 ; 0.5023] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (30.8 pt), swing (31.0 pt), deep (31.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-8.37 %** | CVaR **-10.04 %** | vol 6.11 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 9.77 % contre 6.02 % aujourd'hui, rapport 1.62)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -18.22 % vs -19.88 % si l'on extrapolait par √5 _(rapport 0.917 ; < 1 = le √5 surestime)_
- **β de baisse : 2.2187** (β de hausse 1.9941, asymétrie 1.1126) vs IWM — 602 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 34.9266 sur atr_based (1.5 ATR, 10.902 %) — p(stop avant cible) 0.5263 [0.47 ; 0.58], R/R 2.386, perte reelle 15.082 % (gap inclus), CVaR 10.912 %, EV -0.9628 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.0518 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 10.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.526, borne haute 0.579 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 31 des 31 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 43.2 % de la queue et il ne reste que -839.13 EUR a partager. Prix du risque -0.27 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.42 ATR (stop 5.459 %) — p(stop avant cible) 0.7617 [0.71 ; 0.80], R/R 4.387, perte reelle 8.204 % (gap inclus), EV -1.5969 % — **REFUSE**
      - refuse : cible atteinte seulement 7.6 % du temps (< 15 %) meme a 10 seances : le R/R de 4.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.762, borne haute 0.804 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.11 ATR du spot — compartiment <1, mesure a 45.9 % de casse (IC clusterise [0.428 ; 0.490] sur 1144 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.60 %) : P(cible) 7.6 % x 35.99 % + P(rien) 16.3 % x 11.86 % ne couvrent pas P(stop) 76.2 % x 8.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 10.902 %) — p(stop avant cible) 0.5263 [0.47 ; 0.58], R/R 2.386, perte reelle 15.082 % (gap inclus), EV -0.9628 % — **REFUSE**
      - refuse : cible atteinte seulement 10.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.526, borne haute 0.579 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.96 %) : P(cible) 10.2 % x 35.99 % + P(rien) 37.2 % x 8.89 % ne couvrent pas P(stop) 52.6 % x 15.08 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.76 ATR (stop 15.204 %) — p(stop avant cible) 0.3422 [0.29 ; 0.39], R/R 1.646, perte reelle 21.859 % (gap inclus), EV -1.2689 % — **REFUSE**
      - refuse : cible atteinte seulement 10.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.21 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.27 %) : P(cible) 10.8 % x 35.99 % + P(rien) 55.0 % x 4.24 % ne couvrent pas P(stop) 34.2 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.23 ATR (stop 25.893 %) — p(stop avant cible) 0.0992 [0.07 ; 0.13], R/R 1.39, perte reelle 25.893 % (gap inclus), EV 1.4857 % — **REFUSE**
      - refuse : cible atteinte seulement 11.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.89 % > budget 12.00 %
   - ⚪ atr_grid a 1.0 ATR (stop 7.268 %) — p(stop avant cible) 0.6674 [0.62 ; 0.72], R/R 3.383, perte reelle 10.638 % (gap inclus), EV -0.9714 % — **REFUSE**
      - refuse : cible atteinte seulement 9.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.667, borne haute 0.716 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.97 %) : P(cible) 9.3 % x 35.99 % + P(rien) 24.0 % x 11.59 % ne couvrent pas P(stop) 66.7 % x 10.64 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 9.085 %) — p(stop avant cible) 0.6172 [0.57 ; 0.67], R/R 2.764, perte reelle 13.019 % (gap inclus), EV -1.4892 % — **REFUSE**
      - refuse : cible atteinte seulement 9.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.617, borne haute 0.667 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.49 %) : P(cible) 9.4 % x 35.99 % + P(rien) 28.9 % x 10.98 % ne couvrent pas P(stop) 61.7 % x 13.02 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 16.352 %) — p(stop avant cible) 0.3011 [0.25 ; 0.35], R/R 1.646, perte reelle 21.859 % (gap inclus), EV -0.5114 % — **REFUSE**
      - refuse : cible atteinte seulement 10.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.36 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.51 %) : P(cible) 10.9 % x 35.99 % + P(rien) 59.0 % x 3.66 % ne couvrent pas P(stop) 30.1 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 18.169 %) — p(stop avant cible) 0.268 [0.22 ; 0.32], R/R 1.646, perte reelle 21.859 % (gap inclus), EV 0.1203 % — **REFUSE**
      - refuse : cible atteinte seulement 10.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.17 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 19.986 %) — p(stop avant cible) 0.2116 [0.17 ; 0.26], R/R 1.646, perte reelle 21.859 % (gap inclus), EV 0.9761 % — **REFUSE**
      - refuse : cible atteinte seulement 11.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.99 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 29.071 %) — p(stop avant cible) 0.0742 [0.05 ; 0.11], R/R 1.238, perte reelle 29.071 % (gap inclus), EV 1.3354 % — **REFUSE**
      - refuse : cible atteinte seulement 11.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.07 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 32.705 %) — p(stop avant cible) 0.0295 [0.02 ; 0.05], R/R 1.1, perte reelle 32.705 % (gap inclus), EV 1.4142 % — **REFUSE**
      - refuse : cible atteinte seulement 11.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.70 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 36.338 %) — p(stop avant cible) 0.0157 [0.01 ; 0.03], R/R 0.99, perte reelle 36.338 % (gap inclus), EV 1.4613 % — **REFUSE**
      - refuse : cible atteinte seulement 11.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.34 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 39.972 %) — p(stop avant cible) 0.0068 [0.00 ; 0.02], R/R 0.9, perte reelle 39.972 % (gap inclus), EV 1.4991 % — **REFUSE**
      - refuse : cible atteinte seulement 11.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.97 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 43.606 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.825, perte reelle 43.606 % (gap inclus), EV 1.5247 % — **REFUSE**
      - refuse : cible atteinte seulement 11.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.61 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 47.24 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 0.762, perte reelle 47.24 % (gap inclus), EV 1.5433 % — **REFUSE**
      - refuse : cible atteinte seulement 11.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.24 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 50.874 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.707, perte reelle 50.874 % (gap inclus), EV 1.5603 % — **REFUSE**
      - refuse : cible atteinte seulement 11.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 50.87 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 54.508 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.66, perte reelle 54.508 % (gap inclus), EV 1.5603 % — **REFUSE**
      - refuse : cible atteinte seulement 11.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 54.51 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 58.141 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.619, perte reelle 58.141 % (gap inclus), EV 1.5603 % — **REFUSE**
      - refuse : cible atteinte seulement 11.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 58.14 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 39.2, ATR14 2.8489 (7.268 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.382 ATR = 2.776 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.363 % | 39.0576 | 93.56 % | 95.27 % | 95.97 % | 97.47 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.727 % | 38.9151 | 85.92 % | 91.04 % | 92.04 % | 94.55 % | 96.04 % | 96.92 % |
| 0.15 ATR | 1.09 % | 38.7727 | 79.18 % | 86.2 % | 88.31 % | 91.62 % | 93.81 % | 95.79 % |
| 0.2 ATR | 1.454 % | 38.6302 | 71.73 % | 80.46 % | 84.27 % | 88.48 % | 91.07 % | 93.74 % |
| 0.25 ATR | 1.817 % | 38.4878 | 65.69 % | 76.64 % | 80.75 % | 85.86 % | 88.83 % | 92.21 % |
| 0.35 ATR | 2.544 % | 38.2029 | 53.22 % | 67.57 % | 74.09 % | 79.29 % | 84.16 % | 88.62 % |
| 0.5 ATR | 3.634 % | 37.7755 | 38.03 % | 54.68 % | 62.3 % | 71.01 % | 78.58 % | 84.72 % |
| 0.75 ATR | 5.451 % | 37.0633 | 22.23 % | 38.87 % | 48.19 % | 58.79 % | 68.93 % | 76.82 % |
| 1.0 ATR | 7.268 % | 36.3511 | 9.86 % | 24.47 % | 34.78 % | 45.76 % | 57.87 % | 68.1 % |
| 1.25 ATR | 9.085 % | 35.6388 | 3.62 % | 14.3 % | 24.09 % | 34.65 % | 50.05 % | 61.95 % |
| 1.5 ATR | 10.902 % | 34.9266 | 1.01 % | 7.05 % | 15.83 % | 25.56 % | 41.22 % | 56.1 % |
| 2.0 ATR | 14.535 % | 33.5021 | 0.1 % | 1.91 % | 4.94 % | 14.55 % | 28.53 % | 44.82 % |
| 2.5 ATR | 18.169 % | 32.0777 | 0.0 % | 0.2 % | 1.21 % | 5.76 % | 18.17 % | 33.74 % |
| 3.0 ATR | 21.803 % | 30.6532 | 0.0 % | 0.1 % | 0.4 % | 2.63 % | 11.37 % | 25.85 % |
| 4.0 ATR | 29.071 % | 27.8043 | 0.0 % | 0.1 % | 0.1 % | 0.2 % | 2.94 % | 10.56 % |
| 6.0 ATR | 43.606 % | 22.1064 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.1 % | 1.23 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.58 ATR | 0.71 ATR | 0.80 ATR | 1.00 ATR | 1.20 ATR |
| **2 s.** | 0.27 ATR | 0.57 ATR | 0.65 ATR | 0.85 ATR | 0.99 ATR | 1.11 ATR | 1.40 ATR | 1.70 ATR |
| **3 s.** | 0.34 ATR | 0.72 ATR | 0.81 ATR | 1.04 ATR | 1.23 ATR | 1.37 ATR | 1.77 ATR | 2.00 ATR |
| **5 s.** | 0.43 ATR | 0.92 ATR | 1.02 ATR | 1.29 ATR | 1.52 ATR | 1.75 ATR | 2.26 ATR | 2.62 ATR |
| **10 s.** | 0.59 ATR | 1.25 ATR | 1.39 ATR | 1.82 ATR | 2.17 ATR | 2.41 ATR | 3.16 ATR | 3.76 ATR |
| **20 s.** | 0.80 ATR | 1.77 ATR | 1.99 ATR | 2.55 ATR | 3.06 ATR | 3.38 ATR | 4.12 ATR | 5.19 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.431–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.653–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.451 %, prix 37.0632), p(touche) 38.87 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.809–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.268 %, prix 36.3509), p(touche) 34.78 % (en stress 92.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.017–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (9.085 %, prix 35.6387), p(touche) 34.65 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.393–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.902 %, prix 34.9264), p(touche) 41.22 % (en stress 97.98 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.992–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (14.535 %, prix 33.5023), p(touche) 44.82 % (en stress 98.98 %)  ✅ optimum identifie (68.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.048 | EV/share : $0.041 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 27 % | T3 27 %
- Kelly (position) : f* 0.081 | ¼-Kelly 0.02 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 61.1 | bear 30.6 | side 8.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.46% → cible +3.099% / stop −2.19%, p_fill 91%, n_eff≈37.8) : P(cible|rempli) **30%** · **EV/risk -0.114** (×p_fill ; si rempli -0.28% du capital)
  - **swing** (entrée dip −0.912% → cible +6.93% / stop −7.335%, p_fill 91%, n_eff≈37.3) : P(cible|rempli) **46%** · **EV/risk -0.003** (×p_fill ; si rempli -0.02% du capital)
  - **deep** (entrée dip −1.318% → cible +9.8% / stop −11.047%, p_fill 86%, n_eff≈35.4) : P(cible|rempli) **46%** · **EV/risk -0.070** (×p_fill ; si rempli -0.89% du capital)
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
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 43.6  _(momentum baissier)_
- **ADX** : 16.0  _(pas de tendance nette)_
- **MACD** : hist -0.24  _(bearish_recent)_
- **BB** : %B 0.14 · largeur 22.4%
- **ATR** : 2.85 (17.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.012  _(neutre)_
- **Vol ratio** : 1.03  _(volume normal)_
- **Choppiness** : 55.2  _(transition)_
- **MA** : MA20 42.63 · MA50 42.89 · MA200 44.48  _(prix < MA20)_
- **Dist MA** : MA20 -8.0% · MA50 -8.6% · MA200 -11.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (897631 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
