# SRT3

**Generated** : 2026-08-28T00:04:09.154158+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €250.00  

> 🟡 **WAIT-FOR-DIP** — spot +2.5 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €250.00 (+2.5% vs entrée) · entrée €243.98 · stop €240.32 · T1 €246.69 · R/R 0.74  
> ↳ P(T1 av. stop) 53 % _(réel 5 s)_ · EV/risk 0.013 _(réel 5 s)_ (GBM 0.056) · ¼-Kelly 0.037 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.050 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €243.44–€244.52 (mid €243.98)
- Spot actuel : €250.00 (+2.5% au-dessus de la zone — repli à attendre)
- Stop : €240.32 (stop swing_plan-based (-8.23%))
- Targets : T1 €246.69 · R/R 0.74 | T2 €249.41 · R/R 1.48 | T3 €252.12 · R/R 2.22
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €240.32


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.18 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.23 %)** : le gap seul le franchit 0.392 % des séances (5 fois sur 1274).
   - exécution **1.427 pt plus bas** dans le cas TYPIQUE (médiane), 4.282 au p90, **5.975 au pire**
   - perte réelle **10.096 %** en moyenne _(tirée par la queue)_, jusqu'à **14.205 %** — au lieu des 8.23 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0073 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.616 % | p01 -3.24 % | pire -14.205 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3894** [0.3191 ; 0.4634] _(largeur 14.4 pt, n_eff 173.1)_
   - swing : **0.429** [0.3776 ; 0.4816] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4397** [0.3881 ; 0.4923] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (49.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-4.12 %** | CVaR **-6.6 %** | vol 2.85 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.0 % vs -9.25 % si l'on extrapolait par √5 _(rapport 1.081 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0673** (β de hausse 1.1747, asymétrie 0.9086) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.338× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 220.7143 sur atr_grid (4.0 ATR, 11.714 %) — p(stop avant cible) 0.0809 [0.06 ; 0.11], R/R 0.125, perte reelle 14.205 % (gap inclus), CVaR 11.716 %, EV -0.0859 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.393 %) — p(stop avant cible) 0.2914 [0.25 ; 0.34], R/R 0.231, perte reelle 7.669 % (gap inclus), EV -0.9941 % — **REFUSE**
      - refuse : R/R 0.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.99 %) : P(cible) 70.3 % x 1.77 % + P(rien) 0.5 % x -0.70 % ne couvrent pas P(stop) 29.1 % x 7.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 3.49 ATR (stop 12.1 %) — p(stop avant cible) 0.0713 [0.05 ; 0.10], R/R 0.125, perte reelle 14.205 % (gap inclus), EV -0.0154 % — **REFUSE**
      - refuse : R/R 0.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.10 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.02 %) : P(cible) 82.4 % x 1.77 % + P(rien) 10.5 % x -4.37 % ne couvrent pas P(stop) 7.1 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 8.65 ATR (stop 27.212 %) — p(stop avant cible) 0.0016 [0.00 ; 0.01], R/R 0.065, perte reelle 27.212 % (gap inclus), EV 0.2136 % — **REFUSE**
      - refuse : R/R 0.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.21 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.732 %) — p(stop avant cible) 0.6461 [0.59 ; 0.70], R/R 1.069, perte reelle 1.655 % (gap inclus), EV -0.4432 % — **REFUSE**
      - refuse : p_stop_first 0.646, borne haute 0.695 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.44 %) : P(cible) 35.4 % x 1.77 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 64.6 % x 1.66 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.464 %) — p(stop avant cible) 0.55 [0.50 ; 0.60], R/R 0.627, perte reelle 2.823 % (gap inclus), EV -0.7566 % — **REFUSE**
      - refuse : p_stop_first 0.550, borne haute 0.602 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.76 %) : P(cible) 45.0 % x 1.77 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 55.0 % x 2.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.196 %) — p(stop avant cible) 0.446 [0.39 ; 0.50], R/R 0.38, perte reelle 4.652 % (gap inclus), EV -1.0948 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.09 %) : P(cible) 55.4 % x 1.77 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 44.6 % x 4.65 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 2.929 %) — p(stop avant cible) 0.3779 [0.33 ; 0.43], R/R 0.261, perte reelle 6.774 % (gap inclus), EV -1.4594 % — **REFUSE**
      - refuse : R/R 0.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.46 %) : P(cible) 62.2 % x 1.77 % + P(rien) 0.0 % x 0.00 % ne couvrent pas P(stop) 37.8 % x 6.77 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 3.661 %) — p(stop avant cible) 0.3289 [0.28 ; 0.38], R/R 0.231, perte reelle 7.669 % (gap inclus), EV -1.341 % — **REFUSE**
      - refuse : R/R 0.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.34 %) : P(cible) 66.8 % x 1.77 % + P(rien) 0.3 % x -0.41 % ne couvrent pas P(stop) 32.9 % x 7.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 5.125 %) — p(stop avant cible) 0.2549 [0.21 ; 0.30], R/R 0.214, perte reelle 8.26 % (gap inclus), EV -0.8059 % — **REFUSE**
      - refuse : R/R 0.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.81 %) : P(cible) 73.6 % x 1.77 % + P(rien) 0.9 % x -0.35 % ne couvrent pas P(stop) 25.5 % x 8.26 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 5.857 %) — p(stop avant cible) 0.2258 [0.18 ; 0.27], R/R 0.207, perte reelle 8.535 % (gap inclus), EV -0.5924 % — **REFUSE**
      - refuse : R/R 0.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.59 %) : P(cible) 76.0 % x 1.77 % + P(rien) 1.5 % x -0.61 % ne couvrent pas P(stop) 22.6 % x 8.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 6.589 %) — p(stop avant cible) 0.2044 [0.16 ; 0.25], R/R 0.191, perte reelle 9.276 % (gap inclus), EV -0.5401 % — **REFUSE**
      - refuse : R/R 0.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.54 %) : P(cible) 77.7 % x 1.77 % + P(rien) 1.9 % x -1.00 % ne couvrent pas P(stop) 20.4 % x 9.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 7.321 %) — p(stop avant cible) 0.1813 [0.14 ; 0.22], R/R 0.183, perte reelle 9.643 % (gap inclus), EV -0.3896 % — **REFUSE**
      - refuse : R/R 0.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.39 %) : P(cible) 79.3 % x 1.77 % + P(rien) 2.6 % x -1.68 % ne couvrent pas P(stop) 18.1 % x 9.64 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 8.054 %) — p(stop avant cible) 0.1629 [0.13 ; 0.20], R/R 0.175, perte reelle 10.096 % (gap inclus), EV -0.3255 % — **REFUSE**
      - refuse : R/R 0.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 80.0 % x 1.77 % + P(rien) 3.7 % x -2.64 % ne couvrent pas P(stop) 16.3 % x 10.10 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 8.786 %) — p(stop avant cible) 0.1369 [0.10 ; 0.18], R/R 0.157, perte reelle 11.278 % (gap inclus), EV -0.3065 % — **REFUSE**
      - refuse : R/R 0.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.31 %) : P(cible) 80.8 % x 1.77 % + P(rien) 5.5 % x -3.54 % ne couvrent pas P(stop) 13.7 % x 11.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 3.49 ATR (stop 11.104 %) — p(stop avant cible) 0.0849 [0.06 ; 0.12], R/R 0.125, perte reelle 14.205 % (gap inclus), EV -0.1112 % — **REFUSE**
      - refuse : R/R 0.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.11 %) : P(cible) 82.4 % x 1.77 % + P(rien) 9.2 % x -3.96 % ne couvrent pas P(stop) 8.5 % x 14.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 11.714 %) — p(stop avant cible) 0.0809 [0.06 ; 0.11], R/R 0.125, perte reelle 14.205 % (gap inclus), EV -0.0859 % — **REFUSE**
      - refuse : R/R 0.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.09 %) : P(cible) 82.4 % x 1.77 % + P(rien) 9.5 % x -4.13 % ne couvrent pas P(stop) 8.1 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 13.179 %) — p(stop avant cible) 0.0609 [0.04 ; 0.09], R/R 0.125, perte reelle 14.205 % (gap inclus), EV 0.0238 % — **REFUSE**
      - refuse : R/R 0.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.18 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 14.643 %) — p(stop avant cible) 0.0288 [0.01 ; 0.05], R/R 0.121, perte reelle 14.643 % (gap inclus), EV 0.1571 % — **REFUSE**
      - refuse : R/R 0.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.64 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 16.107 %) — p(stop avant cible) 0.0141 [0.01 ; 0.03], R/R 0.11, perte reelle 16.107 % (gap inclus), EV 0.1884 % — **REFUSE**
      - refuse : R/R 0.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.11 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 17.571 %) — p(stop avant cible) 0.0065 [0.00 ; 0.02], R/R 0.101, perte reelle 17.571 % (gap inclus), EV 0.2205 % — **REFUSE**
      - refuse : R/R 0.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.57 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 19.036 %) — p(stop avant cible) 0.006 [0.00 ; 0.02], R/R 0.093, perte reelle 19.036 % (gap inclus), EV 0.2131 % — **REFUSE**
      - refuse : R/R 0.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.04 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 20.5 %) — p(stop avant cible) 0.006 [0.00 ; 0.02], R/R 0.086, perte reelle 20.5 % (gap inclus), EV 0.2034 % — **REFUSE**
      - refuse : R/R 0.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.50 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 21.964 %) — p(stop avant cible) 0.0037 [0.00 ; 0.01], R/R 0.081, perte reelle 21.964 % (gap inclus), EV 0.2076 % — **REFUSE**
      - refuse : R/R 0.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.96 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 23.429 %) — p(stop avant cible) 0.0029 [0.00 ; 0.01], R/R 0.076, perte reelle 23.429 % (gap inclus), EV 0.2114 % — **REFUSE**
      - refuse : R/R 0.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.43 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 250.0, ATR14 7.3214 (2.929 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.382 ATR = 1.119 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.146 % | 249.6339 | 89.05 % | 92.99 % | 94.37 % | 96.04 % | 97.81 % | 98.49 % |
| 0.1 ATR | 0.293 % | 249.2679 | 82.54 % | 88.45 % | 90.71 % | 93.37 % | 95.72 % | 97.09 % |
| 0.15 ATR | 0.439 % | 248.9018 | 74.95 % | 83.91 % | 86.96 % | 90.5 % | 93.63 % | 95.08 % |
| 0.2 ATR | 0.586 % | 248.5357 | 68.44 % | 78.97 % | 83.0 % | 87.33 % | 92.24 % | 94.47 % |
| 0.25 ATR | 0.732 % | 248.1696 | 63.31 % | 75.62 % | 79.74 % | 84.95 % | 90.55 % | 93.17 % |
| 0.35 ATR | 1.025 % | 247.4375 | 53.16 % | 69.2 % | 74.21 % | 80.89 % | 87.06 % | 91.36 % |
| 0.5 ATR | 1.464 % | 246.3393 | 38.17 % | 56.66 % | 64.53 % | 74.16 % | 82.69 % | 88.84 % |
| 0.75 ATR | 2.196 % | 244.5089 | 19.72 % | 36.92 % | 48.02 % | 59.31 % | 72.34 % | 82.51 % |
| 1.0 ATR | 2.929 % | 242.6786 | 10.26 % | 24.68 % | 34.68 % | 47.62 % | 62.99 % | 75.48 % |
| 1.25 ATR | 3.661 % | 240.8482 | 4.83 % | 15.0 % | 24.7 % | 38.32 % | 53.73 % | 68.54 % |
| 1.5 ATR | 4.393 % | 239.0179 | 2.37 % | 10.07 % | 18.08 % | 31.09 % | 46.47 % | 62.91 % |
| 2.0 ATR | 5.857 % | 235.3571 | 0.79 % | 4.74 % | 8.5 % | 17.62 % | 35.32 % | 53.07 % |
| 2.5 ATR | 7.321 % | 231.6964 | 0.3 % | 2.17 % | 5.04 % | 11.09 % | 25.17 % | 43.02 % |
| 3.0 ATR | 8.786 % | 228.0357 | 0.2 % | 1.68 % | 3.16 % | 6.83 % | 18.21 % | 35.48 % |
| 4.0 ATR | 11.714 % | 220.7143 | 0.0 % | 0.69 % | 1.88 % | 3.96 % | 9.55 % | 21.41 % |
| 6.0 ATR | 17.571 % | 206.0714 | 0.0 % | 0.0 % | 0.0 % | 0.59 % | 2.19 % | 7.34 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.68 ATR | 0.75 ATR | 1.01 ATR | 1.24 ATR |
| **2 s.** | 0.26 ATR | 0.58 ATR | 0.65 ATR | 0.83 ATR | 0.99 ATR | 1.12 ATR | 1.51 ATR | 1.98 ATR |
| **3 s.** | 0.34 ATR | 0.72 ATR | 0.81 ATR | 1.04 ATR | 1.24 ATR | 1.43 ATR | 1.92 ATR | 2.51 ATR |
| **5 s.** | 0.48 ATR | 0.95 ATR | 1.07 ATR | 1.43 ATR | 1.73 ATR | 1.91 ATR | 2.63 ATR | 3.64 ATR |
| **10 s.** | 0.69 ATR | 1.38 ATR | 1.57 ATR | 2.11 ATR | 2.51 ATR | 2.87 ATR | 3.95 ATR | 5.24 ATR |
| **20 s.** | 1.02 ATR | 2.15 ATR | 2.40 ATR | 3.18 ATR | 3.75 ATR | 4.20 ATR | 5.62 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.432–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.464 %, prix 246.34), p(touche) 38.17 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.648–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.196 %, prix 244.51), p(touche) 36.92 % (en stress 88.24 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.807–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.929 %, prix 242.6775), p(touche) 34.68 % (en stress 92.16 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.07–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (3.661 %, prix 240.8475), p(touche) 38.32 % (en stress 92.08 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.566–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (5.857 %, prix 235.3575), p(touche) 35.32 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.401–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (7.321 %, prix 231.6975), p(touche) 43.02 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 55.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.056 | EV/share : €0.204 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 66 % | T2 37 % | T3 18 %
- Kelly (position) : f* 0.146 | ¼-Kelly 0.037 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 11.5 | bear 7.2 | side 81.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 500.0 (= 2 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.406% → cible +1.113% / stop −1.5%, p_fill 21%, n_eff≈13.0) : P(cible|rempli) **53%** · **EV/risk +0.013** (×p_fill ; si rempli +0.09% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=8, n_eff=6))
  - **deep** : indisponible (échantillon insuffisant (n=8, n_eff=6))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→78% · +2.0%→48% · +3.0%→25% · +5.0%→4% · +8.0%→0%
- Range intraday médian 3.33% (p90 6.3%) · excursion haute méd. +1.89% / basse méd. −1.47%
- Profil de vol intra : ouverture 2.035% vs midi 0.845% vs clôture 0.994% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 92% · range 8% · trend ↑0%/↓0% ; spike-down 51% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.098 ; neutre — autocorr -0.021)_ ; drift intra méd. 0.147% ; recovery-V 26%
- **σ réalisé intraday** 2.532% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 68% / bas 70% / whipsaw 39%
- POC intraday (dernière séance, temps-au-prix) : 244.5125 (VA 243.7725–245.6225 ; dernier close 246.7)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 15% · rebond 68% · **stop −2.69%** sous le fill (sous le bruit) · cible +1.89% · R/R 0.7 (high win-rate)
- Gaps overnight (n=159) : méd. 0.05% · baisse 48% (gap-down >1% 7% · >2% 1%)
- Excursion ouverture 5min (n=160) : bas méd −0.44% (p90 −1.81%) · haut méd +0.53% · range méd 1.21%
- Excursion ouverture 15min (n=160) : bas méd −0.57% (p90 −1.91%) · haut méd +0.64% · range méd 1.49%
- Excursion ouverture 30min (n=160) : bas méd −0.59% (p90 −2.04%) · haut méd +0.8% · range méd 1.71%
- Excursion ouverture 60min (n=160) : bas méd −0.75% (p90 −2.45%) · haut méd +0.82% · range méd 1.83%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 246.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 77% (120/159) · gap 25% · délai 0.4min · rebond 53% (67/120) (MFE +1.15%)
   - −1.0% : fill 30min 41% · séance 64% (104/159) · gap 7% · délai 3.0min · rebond 62% (61/104) (MFE +1.34%)
   - −1.5% : fill 30min 26% · séance 49% (86/159) · gap 5% · délai 19.6min · rebond 57% (49/86) (MFE +1.51%)
   - −2.0% : fill 30min 10% · séance 36% (66/159) · gap 1% · délai 106.0min · rebond 65% (38/66) (MFE +1.39%)
   - −3.0% : fill 30min 5% · séance 15% (35/159) · gap 1% · délai 113.2min · rebond 68% (22/35) (MFE +1.89%)
   - −4.0% : fill 30min 3% · séance 9% (18/159) · gap 0% · délai 55.3min · rebond 68% (13/18) (MFE +2.14%)
   - −5.0% : fill 30min 0% · séance 6% (10/159) · gap 0% · délai 122.6min · rebond 86% (9/10) (MFE +2.89%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.44% (p90 −1.97%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.17% (p90 −2.24%) → stop au-delà de −1.22% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −2.59%) → stop au-delà de −1.45% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=446 jambes) : jambe baissière méd −1.04% (p90 −2.34%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 78% (47/56) · rebond 73% (31/47)
      · −2.0% : fill 38% (29/56) · rebond 70% (18/29)
      · −3.0% : fill 20% (19/56) · rebond 63% (12/19)
      · −4.0% : fill 14% (12/56) · rebond 68% (10/12)
      · −5.0% : fill 7% (6/56) · rebond 100% (6/6)
   - **flat** (38 séances) :
      · −1.0% : fill 73% (26/38) · rebond 48% (12/26)
      · −2.0% : fill 48% (18/38) · rebond 54% (9/18)
      · −3.0% : fill 12% (7/38) · rebond 40% (3/7)
      · −4.0% : fill 4% (2/38) · rebond 0% (0/2)
      · −5.0% : fill 3% (1/38) · rebond 0% (0/1)
   - **gap-up** (65 séances) :
      · −1.0% : fill 46% (31/65) · rebond 58% (18/31)
      · −2.0% : fill 26% (19/65) · rebond 72% (11/19)
      · −3.0% : fill 13% (9/65) · rebond 90% (7/9)
      · −4.0% : fill 8% (4/65) · rebond 90% (3/4)
      · −5.0% : fill 7% (3/65) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 57% si les 15 1res min sont vertes (87 cas) · 37% si rouges (73 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **8min** → P(séance verte=clôture>ouverture) 57% si début vert vs 38% si rouge (base 48% · écart 19 pts) ; prédictivité sature ensuite (plafond brut 268min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=85) : tient le vert **57%** · continue >prix actuel 46% ; creux résiduel méd -1.43% (q20 -2.45%) → **SL/trailing à −2.45%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.34% / q75 +2.36% → **scale +1.34% / runner +2.36%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **38%** (continue à baisser 52%) → **RÉDUIRE ~62%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.51%** (au-delà de la MAE q10 -4.51%), cible rebond +1.41% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.86% .. +2.12%] · haut q95 +2.63% · bas q05 -3.25%
   - 60min (n=160) : retour [-2.58% .. +2.34%] · haut q95 +2.83% · bas q05 -3.66%
   - 2h (n=160) : retour [-2.18% .. +2.49%] · haut q95 +2.94% · bas q05 -3.82%
   - 4h (n=160) : retour [-2.52% .. +2.28%] · haut q95 +3.26% · bas q05 -3.83%
   - 6h (n=160) : retour [-2.57% .. +2.94%] · haut q95 +3.61% · bas q05 -3.92%
   - session (n=160) : retour [-3.59% .. +4.13%] · haut q95 +5.59% · bas q05 -4.59%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.33%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 65.4  _(momentum haussier)_
- **ADX** : 16.2  _(pas de tendance nette)_
- **MACD** : hist 1.462  _(pas de croisement recent)_
- **BB** : %B 0.9 · largeur 14.5%
- **ATR** : 7.32 (24.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.053  _(distribution)_
- **Vol ratio** : 0.47  _(volume atone)_
- **Choppiness** : 51.5  _(transition)_
- **MA** : MA20 236.2 · MA50 231.51 · MA200 232.4  _(prix > MA20)_
- **Dist MA** : MA20 +5.8% · MA50 +8.0% · MA200 +7.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (849452 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
