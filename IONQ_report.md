# IONQ

**Generated** : 2026-09-03T00:27:42.521392+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $37.66  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $37.66 (+2.4% vs entrée) · entrée $36.79 · stop $35.74 · T1 $38.88 · R/R 1.99  
> ↳ P(T1 av. stop) 4 % _(réel 5 s)_ · EV/risk -0.06 _(réel 5 s)_ (GBM -0.003) · ¼-Kelly 0.017 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.84% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -41 % hors [0,100] (R² max 0.10). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.080 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $36.58–$37.00 (mid $36.79)
- Spot actuel : $37.66 (+2.4% au-dessus de la zone — repli à attendre)
- Stop : $35.74 (stop swing_plan-based (-13.25%))
- Targets : T1 $38.88 · R/R 1.99 | T2 $39.41 · R/R 2.5 | T3 $39.93 · R/R 2.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $35.74


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.86 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (13.25 %)** : le gap seul le franchit 0.08 % des séances (1 fois sur 1253).
   - exécution **8.609 pt plus bas** dans le cas TYPIQUE (médiane), 8.609 au p90, **8.609 au pire**
   - perte réelle **21.859 %** en moyenne _(tirée par la queue)_, jusqu'à **21.859 %** — au lieu des 13.25 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0069 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.035 % | p01 -6.632 % | pire -21.859 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4566** [0.3836 ; 0.531] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4527** [0.4008 ; 0.5054] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4371** [0.3855 ; 0.4897] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (37.8 pt), swing (43.2 pt), deep (44.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-8.37 %** | CVaR **-10.04 %** | vol 6.11 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 9.64 % contre 6.01 % aujourd'hui, rapport 1.60)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -18.23 % vs -19.88 % si l'on extrapolait par √5 _(rapport 0.917 ; < 1 = le √5 surestime)_
- **β de baisse : 2.219** (β de hausse 1.9891, asymétrie 1.1156) vs IWM — 603 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 33.3541 sur support (1.3 ATR, 11.434 %) — p(stop avant cible) 0.4994 [0.45 ; 0.55], R/R 1.121, perte reelle 15.082 % (gap inclus), CVaR 11.443 %, EV -2.0634 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.0035 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.499, borne haute 0.552 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 1.3 ATR (stop 11.434 %) — p(stop avant cible) 0.4994 [0.45 ; 0.55], R/R 1.121, perte reelle 15.082 % (gap inclus), EV -2.0634 % — **REFUSE**
      - refuse : p_stop_first 0.499, borne haute 0.552 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.06 %) : P(cible) 32.3 % x 16.91 % + P(rien) 17.7 % x 0.02 % ne couvrent pas P(stop) 49.9 % x 15.08 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.87 ATR (stop 22.559 %) — p(stop avant cible) 0.1541 [0.12 ; 0.20], R/R 0.75, perte reelle 22.559 % (gap inclus), EV -0.0226 % — **REFUSE**
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.56 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.02 %) : P(cible) 35.8 % x 16.91 % + P(rien) 48.8 % x -5.31 % ne couvrent pas P(stop) 15.4 % x 22.56 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.4 ATR (stop 33.446 %) — p(stop avant cible) 0.0244 [0.01 ; 0.04], R/R 0.506, perte reelle 33.446 % (gap inclus), EV -0.0473 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.45 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.05 %) : P(cible) 35.9 % x 16.91 % + P(rien) 61.7 % x -8.60 % ne couvrent pas P(stop) 2.4 % x 33.45 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.774 %) — p(stop avant cible) 0.9009 [0.87 ; 0.93], R/R 4.658, perte reelle 3.63 % (gap inclus), EV -1.6317 % — **REFUSE**
      - refuse : cible atteinte seulement 9.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.901, borne haute 0.929 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.63 %) : P(cible) 9.5 % x 16.91 % + P(rien) 0.4 % x 8.65 % ne couvrent pas P(stop) 90.1 % x 3.63 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 3.549 %) — p(stop avant cible) 0.815 [0.77 ; 0.85], R/R 3.141, perte reelle 5.384 % (gap inclus), EV -1.4797 % — **REFUSE**
      - refuse : p_stop_first 0.815, borne haute 0.853 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.48 %) : P(cible) 16.6 % x 16.91 % + P(rien) 1.9 % x 5.65 % ne couvrent pas P(stop) 81.5 % x 5.38 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 5.323 %) — p(stop avant cible) 0.746 [0.70 ; 0.79], R/R 2.219, perte reelle 7.62 % (gap inclus), EV -1.8891 % — **REFUSE**
      - refuse : p_stop_first 0.746, borne haute 0.790 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.89 %) : P(cible) 21.1 % x 16.91 % + P(rien) 4.3 % x 5.34 % ne couvrent pas P(stop) 74.6 % x 7.62 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 7.097 %) — p(stop avant cible) 0.6612 [0.61 ; 0.71], R/R 1.638, perte reelle 10.324 % (gap inclus), EV -2.0045 % — **REFUSE**
      - refuse : p_stop_first 0.661, borne haute 0.710 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.00 %) : P(cible) 26.8 % x 16.91 % + P(rien) 7.0 % x 4.02 % ne couvrent pas P(stop) 66.1 % x 10.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 12.42 %) — p(stop avant cible) 0.4494 [0.40 ; 0.50], R/R 0.774, perte reelle 21.859 % (gap inclus), EV -4.4205 % — **REFUSE**
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.43 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.42 %) : P(cible) 33.1 % x 16.91 % + P(rien) 21.9 % x -0.91 % ne couvrent pas P(stop) 44.9 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 14.195 %) — p(stop avant cible) 0.3767 [0.33 ; 0.43], R/R 0.774, perte reelle 21.859 % (gap inclus), EV -3.2583 % — **REFUSE**
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.26 %) : P(cible) 33.7 % x 16.91 % + P(rien) 28.6 % x -2.54 % ne couvrent pas P(stop) 37.7 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 15.969 %) — p(stop avant cible) 0.3206 [0.27 ; 0.37], R/R 0.774, perte reelle 21.859 % (gap inclus), EV -2.3248 % — **REFUSE**
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.97 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.32 %) : P(cible) 34.0 % x 16.91 % + P(rien) 34.0 % x -3.13 % ne couvrent pas P(stop) 32.1 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 17.743 %) — p(stop avant cible) 0.271 [0.23 ; 0.32], R/R 0.774, perte reelle 21.859 % (gap inclus), EV -1.4748 % — **REFUSE**
      - refuse : R/R 0.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.75 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.47 %) : P(cible) 35.0 % x 16.91 % + P(rien) 37.9 % x -3.89 % ne couvrent pas P(stop) 27.1 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 24.841 %) — p(stop avant cible) 0.105 [0.08 ; 0.14], R/R 0.681, perte reelle 24.841 % (gap inclus), EV 0.0281 % — **REFUSE**
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.84 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 28.389 %) — p(stop avant cible) 0.0697 [0.05 ; 0.10], R/R 0.596, perte reelle 28.389 % (gap inclus), EV -0.0991 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.39 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 35.9 % x 16.91 % + P(rien) 57.2 % x -7.32 % ne couvrent pas P(stop) 7.0 % x 28.39 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 35.487 %) — p(stop avant cible) 0.0135 [0.01 ; 0.03], R/R 0.477, perte reelle 35.487 % (gap inclus), EV 0.0063 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.49 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 39.035 %) — p(stop avant cible) 0.0076 [0.00 ; 0.02], R/R 0.433, perte reelle 39.035 % (gap inclus), EV 0.0108 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.03 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 42.584 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.397, perte reelle 42.584 % (gap inclus), EV 0.0097 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.58 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 46.133 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 0.367, perte reelle 46.133 % (gap inclus), EV 0.0079 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.13 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 49.681 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.34, perte reelle 49.681 % (gap inclus), EV 0.0436 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.68 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 53.23 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.318, perte reelle 53.23 % (gap inclus), EV 0.0432 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 53.23 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 56.779 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.298, perte reelle 56.779 % (gap inclus), EV 0.0432 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 56.78 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 37.66, ATR14 2.6729 (7.097 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.382 ATR = 2.711 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.355 % | 37.5264 | 93.66 % | 95.36 % | 96.06 % | 97.47 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.71 % | 37.3927 | 85.9 % | 91.13 % | 92.13 % | 94.64 % | 96.04 % | 96.92 % |
| 0.15 ATR | 1.065 % | 37.2591 | 79.05 % | 86.29 % | 88.4 % | 91.71 % | 93.8 % | 95.69 % |
| 0.2 ATR | 1.419 % | 37.1254 | 71.6 % | 80.54 % | 84.36 % | 88.57 % | 91.06 % | 93.63 % |
| 0.25 ATR | 1.774 % | 36.9918 | 65.76 % | 76.71 % | 80.83 % | 85.95 % | 88.82 % | 92.09 % |
| 0.35 ATR | 2.484 % | 36.7245 | 53.27 % | 67.74 % | 74.27 % | 79.37 % | 84.15 % | 88.5 % |
| 0.5 ATR | 3.549 % | 36.3236 | 38.17 % | 54.84 % | 62.46 % | 71.08 % | 78.56 % | 84.5 % |
| 0.75 ATR | 5.323 % | 35.6554 | 22.36 % | 39.11 % | 48.44 % | 58.85 % | 68.9 % | 76.59 % |
| 1.0 ATR | 7.097 % | 34.9871 | 9.97 % | 24.6 % | 34.81 % | 45.9 % | 57.83 % | 67.86 % |
| 1.25 ATR | 8.872 % | 34.3189 | 3.63 % | 14.31 % | 24.22 % | 34.78 % | 50.0 % | 61.6 % |
| 1.5 ATR | 10.646 % | 33.6507 | 1.01 % | 7.06 % | 15.84 % | 25.68 % | 41.16 % | 55.75 % |
| 2.0 ATR | 14.195 % | 32.3143 | 0.1 % | 1.92 % | 4.94 % | 14.56 % | 28.46 % | 44.56 % |
| 2.5 ATR | 17.743 % | 30.9779 | 0.0 % | 0.2 % | 1.21 % | 5.76 % | 18.19 % | 33.57 % |
| 3.0 ATR | 21.292 % | 29.6414 | 0.0 % | 0.1 % | 0.4 % | 2.63 % | 11.38 % | 25.87 % |
| 4.0 ATR | 28.389 % | 26.9686 | 0.0 % | 0.1 % | 0.1 % | 0.2 % | 2.95 % | 10.57 % |
| 6.0 ATR | 42.584 % | 21.6229 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.1 % | 1.23 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.58 ATR | 0.71 ATR | 0.80 ATR | 1.00 ATR | 1.20 ATR |
| **2 s.** | 0.27 ATR | 0.58 ATR | 0.66 ATR | 0.85 ATR | 0.99 ATR | 1.11 ATR | 1.40 ATR | 1.70 ATR |
| **3 s.** | 0.34 ATR | 0.72 ATR | 0.81 ATR | 1.04 ATR | 1.23 ATR | 1.38 ATR | 1.77 ATR | 2.00 ATR |
| **5 s.** | 0.43 ATR | 0.92 ATR | 1.02 ATR | 1.30 ATR | 1.53 ATR | 1.75 ATR | 2.26 ATR | 2.62 ATR |
| **10 s.** | 0.59 ATR | 1.25 ATR | 1.39 ATR | 1.82 ATR | 2.17 ATR | 2.41 ATR | 3.16 ATR | 3.76 ATR |
| **20 s.** | 0.80 ATR | 1.76 ATR | 1.98 ATR | 2.54 ATR | 3.06 ATR | 3.38 ATR | 4.12 ATR | 5.19 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.432–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.656–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.323 %, prix 35.6554), p(touche) 39.11 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.813–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.097 %, prix 34.9873), p(touche) 34.81 % (en stress 92.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.02–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.872 %, prix 34.3188), p(touche) 34.78 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.391–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.646 %, prix 33.6507), p(touche) 41.16 % (en stress 97.98 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 50.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.98–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (14.195 %, prix 32.3142), p(touche) 44.56 % (en stress 98.98 %)  ✅ optimum identifie (68.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.003 | EV/share : $-0.004 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 27 % | T2 27 % | T3 27 %
- Kelly (position) : f* 0.068 | ¼-Kelly 0.017 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 61.5 | bear 29.8 | side 8.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.312% → cible +5.688% / stop −2.844%, p_fill 55%, n_eff≈24.2) : P(cible|rempli) **4%** · **EV/risk -0.060** (×p_fill ; si rempli -0.31% du capital)
  - **swing** (entrée dip −5.079% → cible +17.216% / stop −8.608%, p_fill 38%, n_eff≈17.8) : P(cible|rempli) **11%** · **EV/risk -0.071** (×p_fill ; si rempli -1.62% du capital)
  - **deep** (entrée dip −7.854% → cible +9.008% / stop −11.554%, p_fill 33%, n_eff≈16.7) : P(cible|rempli) **36%** · **EV/risk -0.104** (×p_fill ; si rempli -3.70% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→80% · +2.0%→65% · +3.0%→55% · +5.0%→29% · +8.0%→12%
- Range intraday médian 7.38% (p90 11.71%) · excursion haute méd. +3.6% / basse méd. −2.67%
- Profil de vol intra : ouverture 5.098% vs midi 1.433% vs clôture 1.63% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 19% · trend ↑0%/↓0% ; spike-down 68% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; neutre — autocorr -0.022)_ ; drift intra méd. -0.154% ; recovery-V 22%
- **σ réalisé intraday** 4.165% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 56% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 37.8451 (VA 37.7666–38.0021 ; dernier close 37.79)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 34% · rebond 77% · **stop −4.71%** sous le fill (sous le bruit) · cible +2.5% · R/R 0.53 (high win-rate)
- Gaps overnight (n=159) : méd. -0.47% · baisse 55% (gap-down >1% 41% · >2% 21%)
- Excursion ouverture 5min (n=160) : bas méd −1.14% (p90 −2.77%) · haut méd +1.34% · range méd 2.77%
- Excursion ouverture 15min (n=160) : bas méd −1.53% (p90 −3.93%) · haut méd +1.7% · range méd 3.62%
- Excursion ouverture 30min (n=160) : bas méd −1.88% (p90 −5.06%) · haut méd +2.09% · range méd 4.4%
- Excursion ouverture 60min (n=160) : bas méd −2.15% (p90 −5.37%) · haut méd +2.27% · range méd 5.11%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 37.78 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 72% · séance 80% (132/159) · gap 49% · délai 0.0min · rebond 57% (84/132) (MFE +1.81%)
   - −1.0% : fill 30min 69% · séance 75% (124/159) · gap 41% · délai 0.0min · rebond 66% (88/124) (MFE +2.07%)
   - −1.5% : fill 30min 63% · séance 69% (116/159) · gap 34% · délai 0.0min · rebond 68% (79/116) (MFE +1.84%)
   - −2.0% : fill 30min 55% · séance 62% (106/159) · gap 21% · délai 0.0min · rebond 70% (73/106) (MFE +2.04%)
   - −3.0% : fill 30min 46% · séance 54% (91/159) · gap 11% · délai 4.5min · rebond 68% (64/91) (MFE +2.33%)
   - −4.0% : fill 30min 28% · séance 45% (75/159) · gap 5% · délai 15.7min · rebond 65% (55/75) (MFE +2.12%)
   - −5.0% : fill 30min 18% · séance 34% (62/159) · gap 3% · délai 24.8min · rebond 77% (52/62) (MFE +2.5%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.76% (p90 −2.88%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.84% (p90 −2.88%) → stop au-delà de −2.06% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.83% (p90 −2.66%) → stop au-delà de −1.82% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1111 jambes) : jambe baissière méd −1.3% (p90 −3.0%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (80 séances) :
      · −1.0% : fill 100% (80/80) · rebond 64% (56/80)
      · −2.0% : fill 88% (73/80) · rebond 73% (54/73)
      · −3.0% : fill 78% (63/80) · rebond 68% (45/63)
      · −4.0% : fill 63% (50/80) · rebond 64% (37/50)
      · −5.0% : fill 47% (41/80) · rebond 69% (32/41)
   - **flat** (15 séances) :
      · −1.0% : fill 78% (12/15) · rebond 65% (7/12)
      · −2.0% : fill 69% (11/15) · rebond 79% (6/11)
      · −3.0% : fill 62% (9/15) · rebond 62% (6/9)
      · −4.0% : fill 54% (8/15) · rebond 53% (4/8)
      · −5.0% : fill 39% (7/15) · rebond 95% (6/7)
   - **gap-up** (64 séances) :
      · −1.0% : fill 38% (32/64) · rebond 74% (25/32)
      · −2.0% : fill 24% (22/64) · rebond 48% (13/22)
      · −3.0% : fill 20% (19/64) · rebond 75% (13/19)
      · −4.0% : fill 18% (17/64) · rebond 78% (14/17)
      · −5.0% : fill 15% (14/64) · rebond 100% (14/14)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 56% si les 15 1res min sont vertes (83 cas) · 28% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:05** → P(séance verte=clôture>ouverture) 69% si début vert vs 17% si rouge (base 44% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 234min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **69%** · continue >prix actuel 41% ; creux résiduel méd -2.02% (q20 -3.91%) → **SL/trailing à −3.91%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.67% / q75 +3.0% → **scale +1.67% / runner +3.0%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **17%** (continue à baisser 54%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.75%** (au-delà de la MAE q10 -4.75%), cible rebond +1.8% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.7% .. +6.4%] · haut q95 +7.7% · bas q05 -5.49%
   - 60min (n=160) : retour [-4.92% .. +6.01%] · haut q95 +8.05% · bas q05 -6.06%
   - 2h (n=160) : retour [-6.33% .. +7.44%] · haut q95 +8.53% · bas q05 -6.98%
   - 4h (n=160) : retour [-6.9% .. +6.9%] · haut q95 +9.35% · bas q05 -8.08%
   - 6h (n=160) : retour [-7.15% .. +7.77%] · haut q95 +10.25% · bas q05 -8.08%
   - session (n=160) : retour [-6.45% .. +8.37%] · haut q95 +10.43% · bas q05 -8.24%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 7.7)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **26%**. Lecture précoce 30 min : signature présente → 13% vs absente 4% (base 7%)
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
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 35.2  _(momentum baissier)_
- **ADX** : 16.2  _(pas de tendance nette)_
- **MACD** : hist -0.562  _(pas de croisement recent)_
- **BB** : %B 0.07 · largeur 25.9%
- **ATR** : 2.67 (11.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.078  _(distribution)_
- **Vol ratio** : 0.62  _(volume normal)_
- **Choppiness** : 48.2  _(transition)_
- **MA** : MA20 42.34 · MA50 41.73 · MA200 44.3  _(prix < MA20)_
- **Dist MA** : MA20 -11.1% · MA50 -9.7% · MA200 -15.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (493043 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
