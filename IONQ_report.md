# IONQ

**Generated** : 2026-09-15T00:37:58.546500+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $37.50  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot $37.50 (+2.3% vs entrée) · entrée $36.67 · stop $35.91 · T1 $38.18 · R/R 1.99  
> ↳ P(T1 av. stop) 12 % _(réel 5 s)_ · EV/risk -0.045 _(réel 5 s)_ (GBM 0.089) · ¼-Kelly 0.016 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.06% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +10.2 % ≠ (strike 40.5 − spot 37.50)/spot = +8.0 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.240 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $36.49–$36.85 (mid $36.67)
- Spot actuel : $37.50 (+2.3% au-dessus de la zone — repli à attendre)
- Stop : $35.91 (stop swing_plan-based (-11.14%))
- Targets : T1 $38.18 · R/R 1.99 | T2 $38.79 · R/R 2.79 | T3 $39.41 · R/R 3.61
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $35.91


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.94 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (11.14 %)** : le gap seul le franchit 0.239 % des séances (3 fois sur 1253).
   - exécution **0.806 pt plus bas** dans le cas TYPIQUE (médiane), 8.737 au p90, **10.719 au pire**
   - perte réelle **15.082 %** en moyenne _(tirée par la queue)_, jusqu'à **21.859 %** — au lieu des 11.14 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0094 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.069 % | p01 -6.632 % | pire -21.859 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5801** [0.5058 ; 0.6518] _(largeur 14.6 pt, n_eff 173.1)_
   - swing : **0.4742** [0.422 ; 0.5269] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4759** [0.4236 ; 0.5286] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (38.0 pt), swing (42.4 pt), deep (43.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.61 %** | CVaR **-10.74 %** | vol 6.41 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 10.65 % contre 6.03 % aujourd'hui, rapport 1.77)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -18.23 % vs -19.88 % si l'on extrapolait par √5 _(rapport 0.917 ; < 1 = le √5 surestime)_
- **β de baisse : 2.2268** (β de hausse 1.9861, asymétrie 1.1212) vs IWM — 602 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.259× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 32.8335 sur support (1.41 ATR, 12.444 %) — p(stop avant cible) 0.4658 [0.41 ; 0.52], R/R 0.808, perte reelle 21.859 % (gap inclus), CVaR 12.452 %, EV -5.1244 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.0376 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 12.45 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.5 ATR (stop 6.751 %) — p(stop avant cible) 0.702 [0.65 ; 0.75], R/R 1.762, perte reelle 10.029 % (gap inclus), EV -2.7574 % — **REFUSE**
      - refuse : p_stop_first 0.702, borne haute 0.748 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.76 %) : P(cible) 22.4 % x 17.67 % + P(rien) 7.4 % x 4.49 % ne couvrent pas P(stop) 70.2 % x 10.03 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 9.399 %) — p(stop avant cible) 0.6093 [0.56 ; 0.66], R/R 1.265, perte reelle 13.966 % (gap inclus), EV -3.3951 % — **REFUSE**
      - refuse : p_stop_first 0.609, borne haute 0.660 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.40 %) : P(cible) 26.6 % x 17.67 % + P(rien) 12.4 % x 3.29 % ne couvrent pas P(stop) 60.9 % x 13.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.41 ATR (stop 12.444 %) — p(stop avant cible) 0.4658 [0.41 ; 0.52], R/R 0.808, perte reelle 21.859 % (gap inclus), EV -5.1244 % — **REFUSE**
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.45 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.12 %) : P(cible) 29.5 % x 17.67 % + P(rien) 23.9 % x -0.64 % ne couvrent pas P(stop) 46.6 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.2 ATR (stop 23.617 %) — p(stop avant cible) 0.1187 [0.09 ; 0.16], R/R 0.748, perte reelle 23.617 % (gap inclus), EV -0.3322 % — **REFUSE**
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.62 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 32.0 % x 17.67 % + P(rien) 56.1 % x -5.67 % ne couvrent pas P(stop) 11.9 % x 23.62 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.94 ATR (stop 34.551 %) — p(stop avant cible) 0.0216 [0.01 ; 0.04], R/R 0.511, perte reelle 34.551 % (gap inclus), EV -0.4852 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.55 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.49 %) : P(cible) 32.1 % x 17.67 % + P(rien) 65.8 % x -8.21 % ne couvrent pas P(stop) 2.2 % x 34.55 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.567 %) — p(stop avant cible) 0.9123 [0.88 ; 0.94], R/R 5.29, perte reelle 3.34 % (gap inclus), EV -1.5184 % — **REFUSE**
      - refuse : cible atteinte seulement 8.5 % du temps (< 15 %) meme a 10 seances : le R/R de 5.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.912, borne haute 0.939 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.52 %) : P(cible) 8.5 % x 17.67 % + P(rien) 0.3 % x 10.51 % ne couvrent pas P(stop) 91.2 % x 3.34 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.5 ATR (stop 5.04 %) — p(stop avant cible) 0.7689 [0.72 ; 0.81], R/R 2.491, perte reelle 7.093 % (gap inclus), EV -1.9977 % — **REFUSE**
      - refuse : p_stop_first 0.769, borne haute 0.811 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.00 %) : P(cible) 17.8 % x 17.67 % + P(rien) 5.3 % x 5.84 % ne couvrent pas P(stop) 76.9 % x 7.09 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 1.41 ATR (stop 10.733 %) — p(stop avant cible) 0.5355 [0.48 ; 0.59], R/R 1.171, perte reelle 15.082 % (gap inclus), EV -2.8062 % — **REFUSE**
      - refuse : p_stop_first 0.535, borne haute 0.588 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.81 %) : P(cible) 28.7 % x 17.67 % + P(rien) 17.8 % x 1.13 % ne couvrent pas P(stop) 53.5 % x 15.08 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 14.099 %) — p(stop avant cible) 0.3823 [0.33 ; 0.43], R/R 0.808, perte reelle 21.859 % (gap inclus), EV -3.8487 % — **REFUSE**
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.11 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.85 %) : P(cible) 30.0 % x 17.67 % + P(rien) 31.8 % x -2.47 % ne couvrent pas P(stop) 38.2 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 15.666 %) — p(stop avant cible) 0.3174 [0.27 ; 0.37], R/R 0.808, perte reelle 21.859 % (gap inclus), EV -2.8131 % — **REFUSE**
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.67 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.81 %) : P(cible) 30.2 % x 17.67 % + P(rien) 38.0 % x -3.21 % ne couvrent pas P(stop) 31.7 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 17.232 %) — p(stop avant cible) 0.2649 [0.22 ; 0.31], R/R 0.808, perte reelle 21.859 % (gap inclus), EV -1.9237 % — **REFUSE**
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.24 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.92 %) : P(cible) 31.2 % x 17.67 % + P(rien) 42.3 % x -3.90 % ne couvrent pas P(stop) 26.5 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 3.2 ATR (stop 21.907 %) — p(stop avant cible) 0.1667 [0.13 ; 0.21], R/R 0.806, perte reelle 21.907 % (gap inclus), EV -0.4975 % — **REFUSE**
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.91 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.50 %) : P(cible) 32.0 % x 17.67 % + P(rien) 51.4 % x -4.85 % ne couvrent pas P(stop) 16.7 % x 21.91 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 25.065 %) — p(stop avant cible) 0.0962 [0.07 ; 0.13], R/R 0.705, perte reelle 25.065 % (gap inclus), EV -0.4051 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.07 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.41 %) : P(cible) 32.0 % x 17.67 % + P(rien) 58.4 % x -6.25 % ne couvrent pas P(stop) 9.6 % x 25.07 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 28.198 %) — p(stop avant cible) 0.067 [0.04 ; 0.10], R/R 0.627, perte reelle 28.198 % (gap inclus), EV -0.5165 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.52 %) : P(cible) 32.1 % x 17.67 % + P(rien) 61.3 % x -7.01 % ne couvrent pas P(stop) 6.7 % x 28.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 4.94 ATR (stop 32.84 %) — p(stop avant cible) 0.0241 [0.01 ; 0.04], R/R 0.538, perte reelle 32.84 % (gap inclus), EV -0.4883 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.84 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.49 %) : P(cible) 32.1 % x 17.67 % + P(rien) 65.5 % x -8.18 % ne couvrent pas P(stop) 2.4 % x 32.84 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 37.598 %) — p(stop avant cible) 0.0097 [0.00 ; 0.02], R/R 0.47, perte reelle 37.598 % (gap inclus), EV -0.4385 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.60 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.44 %) : P(cible) 32.1 % x 17.67 % + P(rien) 67.0 % x -8.57 % ne couvrent pas P(stop) 1.0 % x 37.60 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 40.731 %) — p(stop avant cible) 0.0042 [0.00 ; 0.02], R/R 0.434, perte reelle 40.731 % (gap inclus), EV -0.4276 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.73 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.43 %) : P(cible) 32.1 % x 17.67 % + P(rien) 67.5 % x -8.77 % ne couvrent pas P(stop) 0.4 % x 40.73 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 43.864 %) — p(stop avant cible) 0.0016 [0.00 ; 0.01], R/R 0.403, perte reelle 43.864 % (gap inclus), EV -0.4289 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.86 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.43 %) : P(cible) 32.1 % x 17.67 % + P(rien) 67.8 % x -8.89 % ne couvrent pas P(stop) 0.2 % x 43.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 46.997 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 0.376, perte reelle 46.997 % (gap inclus), EV -0.4115 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.00 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.41 %) : P(cible) 32.1 % x 17.67 % + P(rien) 67.9 % x -8.91 % ne couvrent pas P(stop) 0.1 % x 47.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 50.13 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.352, perte reelle 50.13 % (gap inclus), EV -0.3946 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 50.13 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.39 %) : P(cible) 32.1 % x 17.67 % + P(rien) 67.9 % x -8.92 % ne couvrent pas P(stop) 0.0 % x 50.13 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 37.5, ATR14 2.3499 (6.266 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.38 ATR = 2.381 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.313 % | 37.3825 | 93.66 % | 95.36 % | 96.06 % | 97.47 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.627 % | 37.265 | 85.9 % | 91.13 % | 92.23 % | 94.64 % | 96.04 % | 96.92 % |
| 0.15 ATR | 0.94 % | 37.1475 | 78.95 % | 86.19 % | 88.4 % | 91.71 % | 93.8 % | 95.69 % |
| 0.2 ATR | 1.253 % | 37.03 | 71.4 % | 80.44 % | 84.36 % | 88.57 % | 91.06 % | 93.63 % |
| 0.25 ATR | 1.567 % | 36.9125 | 65.46 % | 76.51 % | 80.73 % | 85.95 % | 88.92 % | 92.09 % |
| 0.35 ATR | 2.193 % | 36.6776 | 52.97 % | 67.54 % | 74.17 % | 79.37 % | 84.25 % | 88.5 % |
| 0.5 ATR | 3.133 % | 36.3251 | 38.17 % | 54.54 % | 62.26 % | 71.08 % | 78.76 % | 84.5 % |
| 0.75 ATR | 4.7 % | 35.7376 | 22.36 % | 39.01 % | 48.23 % | 58.65 % | 69.11 % | 76.69 % |
| 1.0 ATR | 6.266 % | 35.1501 | 9.97 % | 24.5 % | 34.61 % | 45.7 % | 58.03 % | 68.07 % |
| 1.25 ATR | 7.833 % | 34.5627 | 3.63 % | 14.21 % | 24.02 % | 34.48 % | 50.2 % | 61.7 % |
| 1.5 ATR | 9.399 % | 33.9752 | 1.01 % | 7.06 % | 15.74 % | 25.38 % | 41.26 % | 55.85 % |
| 2.0 ATR | 12.533 % | 32.8003 | 0.1 % | 1.92 % | 5.05 % | 14.26 % | 28.35 % | 44.56 % |
| 2.5 ATR | 15.666 % | 31.6254 | 0.0 % | 0.2 % | 1.21 % | 5.76 % | 18.09 % | 33.78 % |
| 3.0 ATR | 18.799 % | 30.4504 | 0.0 % | 0.1 % | 0.4 % | 2.63 % | 11.38 % | 25.77 % |
| 4.0 ATR | 25.065 % | 28.1006 | 0.0 % | 0.1 % | 0.1 % | 0.2 % | 2.95 % | 10.57 % |
| 6.0 ATR | 37.598 % | 23.4009 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.1 % | 1.23 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.58 ATR | 0.71 ATR | 0.80 ATR | 1.00 ATR | 1.20 ATR |
| **2 s.** | 0.27 ATR | 0.57 ATR | 0.65 ATR | 0.85 ATR | 0.99 ATR | 1.11 ATR | 1.40 ATR | 1.70 ATR |
| **3 s.** | 0.34 ATR | 0.72 ATR | 0.81 ATR | 1.04 ATR | 1.23 ATR | 1.37 ATR | 1.77 ATR | 2.01 ATR |
| **5 s.** | 0.43 ATR | 0.92 ATR | 1.02 ATR | 1.29 ATR | 1.52 ATR | 1.74 ATR | 2.25 ATR | 2.62 ATR |
| **10 s.** | 0.60 ATR | 1.26 ATR | 1.40 ATR | 1.82 ATR | 2.16 ATR | 2.41 ATR | 3.16 ATR | 3.76 ATR |
| **20 s.** | 0.80 ATR | 1.76 ATR | 1.98 ATR | 2.55 ATR | 3.05 ATR | 3.38 ATR | 4.12 ATR | 5.19 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.431–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.654–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.7 %, prix 35.7375), p(touche) 39.01 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.809–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.266 %, prix 35.1502), p(touche) 34.61 % (en stress 92.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.016–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.833 %, prix 34.5626), p(touche) 34.48 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.395–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.399 %, prix 33.9754), p(touche) 41.26 % (en stress 97.98 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.981–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (12.533 %, prix 32.8001), p(touche) 44.56 % (en stress 98.98 %)  ✅ optimum identifie (68.8 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.089 | EV/share : $0.068 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 24 % | T3 24 %
- Kelly (position) : f* 0.065 | ¼-Kelly 0.016 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 63.5 | bear 29.6 | side 6.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.212% → cible +4.127% / stop −2.063%, p_fill 48%, n_eff≈24.0) : P(cible|rempli) **12%** · **EV/risk -0.045** (×p_fill ; si rempli -0.20% du capital)
  - **swing** (entrée dip −4.874% → cible +5.56% / stop −6.587%, p_fill 48%, n_eff≈18.9) : P(cible|rempli) **52%** · **EV/risk +0.002** (×p_fill ; si rempli +0.03% du capital)
  - **deep** (entrée dip −7.52% → cible +7.863% / stop −10.164%, p_fill 35%, n_eff≈16.7) : P(cible|rempli) **37%** · **EV/risk -0.076** (×p_fill ; si rempli -2.20% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→91% · +1.0%→82% · +2.0%→66% · +3.0%→55% · +5.0%→28% · +8.0%→12%
- Range intraday médian 7.27% (p90 11.71%) · excursion haute méd. +3.6% / basse méd. −2.65%
- Profil de vol intra : ouverture 4.994% vs midi 1.407% vs clôture 1.611% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 66% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.118 ; mean-reverting — autocorr -0.042)_ ; drift intra méd. 0.05% ; recovery-V 28%
- **σ réalisé intraday** 4.012% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 53% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 39.3778 (VA 39.1437–39.4753 ; dernier close 39.52)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 32% · rebond 77% · **stop −4.73%** sous le fill (sous le bruit) · cible +2.48% · R/R 0.52 (high win-rate)
- Gaps overnight (n=159) : méd. -0.44% · baisse 54% (gap-down >1% 39% · >2% 20%)
- Excursion ouverture 5min (n=160) : bas méd −1.14% (p90 −2.74%) · haut méd +1.35% · range méd 2.72%
- Excursion ouverture 15min (n=160) : bas méd −1.42% (p90 −3.85%) · haut méd +1.69% · range méd 3.56%
- Excursion ouverture 30min (n=160) : bas méd −1.81% (p90 −4.85%) · haut méd +2.05% · range méd 4.31%
- Excursion ouverture 60min (n=160) : bas méd −1.95% (p90 −5.3%) · haut méd +2.23% · range méd 4.91%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 39.52 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 78% (130/159) · gap 49% · délai 0.0min · rebond 58% (83/130) (MFE +1.8%)
   - −1.0% : fill 30min 67% · séance 72% (123/159) · gap 39% · délai 0.0min · rebond 67% (88/123) (MFE +2.21%)
   - −1.5% : fill 30min 61% · séance 67% (115/159) · gap 33% · délai 0.0min · rebond 69% (79/115) (MFE +1.96%)
   - −2.0% : fill 30min 54% · séance 60% (105/159) · gap 20% · délai 0.0min · rebond 71% (72/105) (MFE +2.19%)
   - −3.0% : fill 30min 43% · séance 51% (89/159) · gap 10% · délai 4.4min · rebond 68% (63/89) (MFE +2.33%)
   - −4.0% : fill 30min 26% · séance 42% (73/159) · gap 5% · délai 15.6min · rebond 65% (54/73) (MFE +2.14%)
   - −5.0% : fill 30min 17% · séance 32% (60/159) · gap 3% · délai 24.8min · rebond 77% (50/60) (MFE +2.48%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.76% (p90 −2.83%) → stop au-delà de −1.89% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.84% (p90 −2.85%) → stop au-delà de −1.94% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.78% (p90 −2.66%) → stop au-delà de −1.8% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1104 jambes) : jambe baissière méd −1.28% (p90 −2.98%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (81 séances) :
      · −1.0% : fill 100% (81/81) · rebond 66% (57/81)
      · −2.0% : fill 88% (74/81) · rebond 74% (55/74)
      · −3.0% : fill 75% (63/81) · rebond 68% (45/63)
      · −4.0% : fill 61% (50/81) · rebond 64% (37/50)
      · −5.0% : fill 46% (41/81) · rebond 69% (32/41)
   - **flat** (15 séances) :
      · −1.0% : fill 62% (11/15) · rebond 67% (7/11)
      · −2.0% : fill 55% (10/15) · rebond 79% (5/10)
      · −3.0% : fill 49% (8/15) · rebond 61% (5/8)
      · −4.0% : fill 42% (7/15) · rebond 54% (4/7)
      · −5.0% : fill 31% (6/15) · rebond 95% (5/6)
   - **gap-up** (63 séances) :
      · −1.0% : fill 36% (31/63) · rebond 73% (24/31)
      · −2.0% : fill 22% (21/63) · rebond 48% (12/21)
      · −3.0% : fill 19% (18/63) · rebond 76% (13/18)
      · −4.0% : fill 16% (16/63) · rebond 78% (13/16)
      · −5.0% : fill 14% (13/63) · rebond 100% (13/13)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 60% si les 15 1res min sont vertes (85 cas) · 28% si rouges (75 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:05** → P(séance verte=clôture>ouverture) 72% si début vert vs 17% si rouge (base 47% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 231min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **72%** · continue >prix actuel 41% ; creux résiduel méd -1.93% (q20 -3.68%) → **SL/trailing à −3.68%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.63% / q75 +2.84% → **scale +1.63% / runner +2.84%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **17%** (continue à baisser 53%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.75%** (au-delà de la MAE q10 -4.75%), cible rebond +1.8% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.52% .. +6.1%] · haut q95 +7.59% · bas q05 -5.47%
   - 60min (n=160) : retour [-4.88% .. +5.95%] · haut q95 +7.86% · bas q05 -6.04%
   - 2h (n=160) : retour [-6.29% .. +6.53%] · haut q95 +8.52% · bas q05 -6.97%
   - 4h (n=160) : retour [-6.89% .. +6.88%] · haut q95 +9.0% · bas q05 -8.03%
   - 6h (n=160) : retour [-7.11% .. +7.68%] · haut q95 +10.23% · bas q05 -8.07%
   - session (n=160) : retour [-6.38% .. +8.29%] · haut q95 +10.34% · bas q05 -8.2%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 7.7)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **23%**. Lecture précoce 30 min : signature présente → 13% vs absente 3% (base 7%)
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
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 40.0  _(momentum baissier)_
- **ADX** : 12.8  _(pas de tendance nette)_
- **MACD** : hist -0.33  _(pas de croisement recent)_
- **BB** : %B 0.24 · largeur 28.0%
- **ATR** : 2.35 (8.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.245  _(distribution)_
- **Vol ratio** : 0.9  _(volume normal)_
- **Choppiness** : 47.3  _(transition)_
- **MA** : MA20 40.42 · MA50 39.87 · MA200 44.03  _(prix < MA20)_
- **Dist MA** : MA20 -7.2% · MA50 -5.9% · MA200 -14.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (759965 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
