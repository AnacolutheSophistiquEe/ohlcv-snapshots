# PRY

**Generated** : 2026-09-11T21:57:18.676919+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €127.25  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-11 — US Core CPI (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot €127.25 (+2.5% vs entrée) · entrée €124.14 · stop €114.21 · T1 €125.97 · R/R 0.18  
> ↳ P(T1 av. stop) 20 % _(réel 5 s)_ · EV/risk -0.023 _(réel 5 s)_ (GBM -0.076) · ¼-Kelly 0.081 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.240 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €123.78–€124.51 (mid €124.14)
- Spot actuel : €127.25 (+2.5% au-dessus de la zone — repli à attendre)
- Stop : €114.21 (stop swing_plan-based (-8.94%))
- Targets : T1 €125.97 · R/R 0.18 | T2 €127.79 · R/R 0.37 | T3 €129.62 · R/R 0.55
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €114.21


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.50 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.94 %)** : le gap seul le franchit 0.079 % des séances (1 fois sur 1269).
   - exécution **1.058 pt plus bas** dans le cas TYPIQUE (médiane), 1.058 au p90, **1.058 au pire**
   - perte réelle **9.998 %** en moyenne _(tirée par la queue)_, jusqu'à **9.998 %** — au lieu des 8.94 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0008 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.847 % | p01 -3.349 % | pire -9.998 % _(sur 1269 séances)_
- **P(stop avant cible)** _(source : daily, 1270 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0004** [0.0 ; 0.0154] _(largeur 1.5 pt, n_eff 173.1)_
   - swing : **0.418** [0.3669 ; 0.4705] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.3661** [0.3166 ; 0.4178] _(largeur 10.1 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 17.3 observations effectives », dont la borne haute a 95 % vaut environ 17.4 %.
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 12.7 observations effectives », dont la borne haute a 95 % vaut environ 23.6 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (36.2 pt), swing (47.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-4.19 %** | CVaR **-4.89 %** | vol 2.57 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 1.79 % contre 2.92 % aujourd'hui, rapport 0.61)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.48 % vs -7.49 % si l'on extrapolait par √5 _(rapport 0.865 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0275** (β de hausse 1.2214, asymétrie 0.8412) vs FTSEMIB — 563 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.412× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 112.0566 sur swing_based (2.72 ATR, 11.94 %) — p(stop avant cible) 0.082 [0.06 ; 0.11], R/R 1.807, perte reelle 11.94 % (gap inclus), CVaR 11.94 %, EV 1.3532 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 15 des 15 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 65.8 % de la queue et il ne reste que -887.74 EUR a partager. Prix du risque -0.635 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.342 %) — p(stop avant cible) 0.466 [0.41 ; 0.52], R/R 2.947, perte reelle 7.321 % (gap inclus), EV -0.4353 % — **REFUSE**
      - refuse : cible atteinte seulement 2.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.44 %) : P(cible) 2.7 % x 21.57 % + P(rien) 50.7 % x 4.71 % ne couvrent pas P(stop) 46.6 % x 7.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.72 ATR (stop 11.94 %) — p(stop avant cible) 0.082 [0.06 ; 0.11], R/R 1.807, perte reelle 11.94 % (gap inclus), EV 1.3532 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 5.14 ATR (stop 20.56 %) — p(stop avant cible) 0.0098 [0.00 ; 0.02], R/R 1.049, perte reelle 20.56 % (gap inclus), EV 1.4876 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.56 % > budget 12.00 %
   - 🟢 support a 10.74 ATR (stop 40.521 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.532, perte reelle 40.521 % (gap inclus), EV 1.5024 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.53 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.52 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.89 %) — p(stop avant cible) 0.8958 [0.86 ; 0.92], R/R 11.537, perte reelle 1.87 % (gap inclus), EV -0.7051 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 11.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.896, borne haute 0.925 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.71 %) : P(cible) 1.1 % x 21.57 % + P(rien) 9.3 % x 7.86 % ne couvrent pas P(stop) 89.6 % x 1.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 1.781 %) — p(stop avant cible) 0.7976 [0.75 ; 0.84], R/R 7.509, perte reelle 2.873 % (gap inclus), EV -0.6793 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 7.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.798, borne haute 0.837 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.68 %) : P(cible) 1.4 % x 21.57 % + P(rien) 18.8 % x 6.94 % ne couvrent pas P(stop) 79.8 % x 2.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 2.671 %) — p(stop avant cible) 0.6998 [0.65 ; 0.75], R/R 5.224, perte reelle 4.13 % (gap inclus), EV -0.6589 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 5.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.700, borne haute 0.746 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.66 %) : P(cible) 1.8 % x 21.57 % + P(rien) 28.2 % x 6.54 % ne couvrent pas P(stop) 70.0 % x 4.13 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 3.562 %) — p(stop avant cible) 0.614 [0.56 ; 0.66], R/R 4.074, perte reelle 5.296 % (gap inclus), EV -0.6759 % — **REFUSE**
      - refuse : cible atteinte seulement 2.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.614, borne haute 0.664 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.68 %) : P(cible) 2.1 % x 21.57 % + P(rien) 36.5 % x 5.82 % ne couvrent pas P(stop) 61.4 % x 5.30 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 4.452 %) — p(stop avant cible) 0.5425 [0.49 ; 0.59], R/R 3.667, perte reelle 5.884 % (gap inclus), EV -0.3268 % — **REFUSE**
      - refuse : cible atteinte seulement 2.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.542, borne haute 0.595 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 2.4 % x 21.57 % + P(rien) 43.3 % x 5.41 % ne couvrent pas P(stop) 54.2 % x 5.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 6.233 %) — p(stop avant cible) 0.3889 [0.34 ; 0.44], R/R 2.728, perte reelle 7.909 % (gap inclus), EV 0.1585 % — **REFUSE**
      - refuse : cible atteinte seulement 3.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 7.123 %) — p(stop avant cible) 0.3321 [0.28 ; 0.38], R/R 2.512, perte reelle 8.587 % (gap inclus), EV 0.3673 % — **REFUSE**
      - refuse : cible atteinte seulement 3.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 8.014 %) — p(stop avant cible) 0.267 [0.22 ; 0.32], R/R 2.158, perte reelle 9.998 % (gap inclus), EV 0.4628 % — **REFUSE**
      - refuse : cible atteinte seulement 3.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 2.72 ATR (stop 10.74 %) — p(stop avant cible) 0.1489 [0.11 ; 0.19], R/R 2.009, perte reelle 10.74 % (gap inclus), EV 1.1332 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 12.466 %) — p(stop avant cible) 0.0795 [0.05 ; 0.11], R/R 1.731, perte reelle 12.466 % (gap inclus), EV 1.3282 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.47 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 14.246 %) — p(stop avant cible) 0.0471 [0.03 ; 0.07], R/R 1.514, perte reelle 14.246 % (gap inclus), EV 1.4135 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.25 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 16.027 %) — p(stop avant cible) 0.0195 [0.01 ; 0.04], R/R 1.346, perte reelle 16.027 % (gap inclus), EV 1.5147 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.03 % > budget 12.00 %
   - 🟢 grid_snapped a 5.14 ATR (stop 19.359 %) — p(stop avant cible) 0.011 [0.00 ; 0.03], R/R 1.114, perte reelle 19.359 % (gap inclus), EV 1.4971 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.36 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 21.37 %) — p(stop avant cible) 0.0091 [0.00 ; 0.02], R/R 1.01, perte reelle 21.37 % (gap inclus), EV 1.4825 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.37 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 23.15 %) — p(stop avant cible) 0.0071 [0.00 ; 0.02], R/R 0.932, perte reelle 23.15 % (gap inclus), EV 1.4823 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.15 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 24.931 %) — p(stop avant cible) 0.0044 [0.00 ; 0.02], R/R 0.865, perte reelle 24.931 % (gap inclus), EV 1.494 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.93 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 26.712 %) — p(stop avant cible) 0.0036 [0.00 ; 0.01], R/R 0.808, perte reelle 26.712 % (gap inclus), EV 1.4955 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.71 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 28.493 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.757, perte reelle 28.493 % (gap inclus), EV 1.5028 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.49 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 127.25, ATR14 4.5321 (3.562 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.346 ATR = 1.232 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.178 % | 127.0234 | 92.07 % | 94.05 % | 94.84 % | 95.62 % | 97.3 % | 97.88 % |
| 0.1 ATR | 0.356 % | 126.7968 | 85.43 % | 88.99 % | 91.26 % | 93.03 % | 95.2 % | 96.26 % |
| 0.15 ATR | 0.534 % | 126.5702 | 77.9 % | 84.33 % | 87.59 % | 90.55 % | 93.0 % | 94.24 % |
| 0.2 ATR | 0.712 % | 126.3436 | 69.77 % | 79.07 % | 82.72 % | 86.87 % | 90.7 % | 92.22 % |
| 0.25 ATR | 0.89 % | 126.117 | 62.24 % | 74.4 % | 78.75 % | 83.18 % | 88.2 % | 90.3 % |
| 0.35 ATR | 1.247 % | 125.6638 | 49.55 % | 63.99 % | 71.1 % | 76.82 % | 83.9 % | 87.47 % |
| 0.5 ATR | 1.781 % | 124.9839 | 35.18 % | 52.08 % | 60.28 % | 68.16 % | 76.6 % | 81.82 % |
| 0.75 ATR | 2.671 % | 123.8509 | 19.23 % | 34.52 % | 43.3 % | 54.63 % | 64.9 % | 73.13 % |
| 1.0 ATR | 3.562 % | 122.7179 | 10.01 % | 23.31 % | 31.68 % | 44.28 % | 55.6 % | 64.95 % |
| 1.25 ATR | 4.452 % | 121.5848 | 5.65 % | 15.97 % | 24.03 % | 34.33 % | 47.2 % | 57.17 % |
| 1.5 ATR | 5.342 % | 120.4518 | 2.48 % | 9.62 % | 15.99 % | 24.28 % | 36.6 % | 48.69 % |
| 2.0 ATR | 7.123 % | 118.1857 | 0.4 % | 3.97 % | 7.45 % | 13.73 % | 24.5 % | 37.37 % |
| 2.5 ATR | 8.904 % | 115.9196 | 0.0 % | 1.59 % | 3.38 % | 7.76 % | 15.7 % | 26.77 % |
| 3.0 ATR | 10.685 % | 113.6536 | 0.0 % | 0.79 % | 1.69 % | 4.18 % | 9.9 % | 19.19 % |
| 4.0 ATR | 14.246 % | 109.1214 | 0.0 % | 0.1 % | 0.6 % | 1.79 % | 4.8 % | 11.11 % |
| 6.0 ATR | 21.37 % | 100.0571 | 0.0 % | 0.0 % | 0.0 % | 0.4 % | 1.8 % | 3.64 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.66 ATR | 0.74 ATR | 1.00 ATR | 1.30 ATR |
| **2 s.** | 0.24 ATR | 0.53 ATR | 0.60 ATR | 0.78 ATR | 0.96 ATR | 1.11 ATR | 1.49 ATR | 1.91 ATR |
| **3 s.** | 0.30 ATR | 0.65 ATR | 0.72 ATR | 0.97 ATR | 1.22 ATR | 1.38 ATR | 1.85 ATR | 2.30 ATR |
| **5 s.** | 0.38 ATR | 0.86 ATR | 0.98 ATR | 1.28 ATR | 1.48 ATR | 1.70 ATR | 2.31 ATR | 2.88 ATR |
| **10 s.** | 0.53 ATR | 1.17 ATR | 1.30 ATR | 1.65 ATR | 1.98 ATR | 2.26 ATR | 2.99 ATR | 3.96 ATR |
| **20 s.** | 0.70 ATR | 1.46 ATR | 1.66 ATR | 2.21 ATR | 2.62 ATR | 2.95 ATR | 4.30 ATR | 5.64 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.397–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.601–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.671 %, prix 123.8512), p(touche) 34.52 % (en stress 86.14 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.725–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.671 %, prix 123.8512), p(touche) 43.3 % (en stress 94.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 55.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.983–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.562 %, prix 122.7174), p(touche) 44.28 % (en stress 99.01 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.302–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.342 %, prix 120.4523), p(touche) 36.6 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.663–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.123 %, prix 118.186), p(touche) 37.37 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 56.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.076 | EV/share : €-0.755 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 46 % | T2 26 % | T3 7 %
- Kelly (position) : f* 0.323 | ¼-Kelly 0.081 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.5 | bear 7.1 | side 7.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 254.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.446% → cible +1.47% / stop −8.0%, p_fill 36%, n_eff≈17.3) : P(cible|rempli) **20%** · **EV/risk -0.023** (×p_fill ; si rempli -0.51% du capital)
  - **swing** (entrée dip −5.379% → cible +3.287% / stop −3.764%, p_fill 24%, n_eff≈12.7) : P(cible|rempli) **68%** · **EV/risk +0.055** (×p_fill ; si rempli +0.84% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=11, n_eff=8))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→65% · +2.0%→39% · +3.0%→25% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.87% (p90 6.32%) · excursion haute méd. +1.25% / basse méd. −1.6%
- Profil de vol intra : ouverture 2.336% vs midi 0.768% vs clôture 1.076% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 52% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.116 ; neutre — autocorr -0.012)_ ; drift intra méd. -0.636% ; recovery-V 15%
- **σ réalisé intraday** 2.481% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 59% / bas 66% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 121.41 (VA 121.11–121.91 ; dernier close 122.5)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 27% · rebond 68% · **stop −2.77%** sous le fill (sous le bruit) · cible +1.69% · R/R 0.61 (high win-rate)
- Gaps overnight (n=159) : méd. 0.38% · baisse 38% (gap-down >1% 13% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.79% (p90 −2.04%) · haut méd +0.45% · range méd 1.37%
- Excursion ouverture 15min (n=160) : bas méd −0.99% (p90 −2.37%) · haut méd +0.59% · range méd 1.71%
- Excursion ouverture 30min (n=160) : bas méd −1.02% (p90 −2.92%) · haut méd +0.74% · range méd 1.89%
- Excursion ouverture 60min (n=160) : bas méd −1.1% (p90 −3.14%) · haut méd +0.86% · range méd 2.21%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 122.25 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 51% · séance 70% (110/159) · gap 20% · délai 0.4min · rebond 51% (63/110) (MFE +1.04%)
   - −1.0% : fill 30min 42% · séance 57% (92/159) · gap 13% · délai 1.2min · rebond 56% (56/92) (MFE +1.11%)
   - −1.5% : fill 30min 29% · séance 48% (73/159) · gap 9% · délai 10.9min · rebond 52% (42/73) (MFE +1.06%)
   - −2.0% : fill 30min 20% · séance 39% (60/159) · gap 6% · délai 28.6min · rebond 56% (38/60) (MFE +1.1%)
   - −3.0% : fill 30min 7% · séance 27% (42/159) · gap 2% · délai 91.4min · rebond 68% (30/42) (MFE +1.69%)
   - −4.0% : fill 30min 2% · séance 18% (26/159) · gap 1% · délai 337.0min · rebond 54% (16/26) (MFE +1.15%)
   - −5.0% : fill 30min 1% · séance 11% (17/159) · gap 1% · délai 395.2min · rebond 62% (12/17) (MFE +1.17%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.37% (p90 −1.74%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.37% (p90 −1.67%) → stop au-delà de −1.11% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.02% (p90 −1.65%) → stop au-delà de −1.04% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=496 jambes) : jambe baissière méd −1.06% (p90 −2.62%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (42 séances) :
      · −1.0% : fill 91% (38/42) · rebond 42% (20/38)
      · −2.0% : fill 74% (31/42) · rebond 60% (20/31)
      · −3.0% : fill 56% (25/42) · rebond 70% (18/25)
      · −4.0% : fill 38% (15/42) · rebond 50% (9/15)
      · −5.0% : fill 31% (12/42) · rebond 48% (8/12)
   - **flat** (27 séances) :
      · −1.0% : fill 54% (16/27) · rebond 74% (12/16)
      · −2.0% : fill 30% (8/27) · rebond 76% (7/8)
      · −3.0% : fill 18% (5/27) · rebond 41% (3/5)
      · −4.0% : fill 6% (2/27) · rebond 69% (1/2)
      · −5.0% : fill 2% (1/27) · rebond 0% (0/1)
   - **gap-up** (90 séances) :
      · −1.0% : fill 43% (38/90) · rebond 60% (24/38)
      · −2.0% : fill 27% (21/90) · rebond 40% (11/21)
      · −3.0% : fill 19% (12/90) · rebond 77% (9/12)
      · −4.0% : fill 14% (9/90) · rebond 55% (6/9)
      · −5.0% : fill 7% (4/90) · rebond 100% (4/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 66% si les 15 1res min sont vertes (77 cas) · 26% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:09** → P(séance verte=clôture>ouverture) 76% si début vert vs 21% si rouge (base 45% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **76%** · continue >prix actuel 50% ; creux résiduel méd -0.89% (q20 -1.92%) → **SL/trailing à −1.92%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.34% / q75 +2.62% → **scale +1.34% / runner +2.62%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **21%** (continue à baisser 63%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.06%** (au-delà de la MAE q10 -4.06%), cible rebond +1.22% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.97% .. +2.76%] · haut q95 +3.15% · bas q05 -3.36%
   - 60min (n=160) : retour [-3.3% .. +2.2%] · haut q95 +3.46% · bas q05 -3.59%
   - 2h (n=160) : retour [-3.37% .. +2.64%] · haut q95 +3.48% · bas q05 -4.12%
   - 4h (n=160) : retour [-3.47% .. +3.18%] · haut q95 +3.96% · bas q05 -4.48%
   - 6h (n=160) : retour [-3.73% .. +3.63%] · haut q95 +4.47% · bas q05 -4.69%
   - session (n=160) : retour [-4.61% .. +3.54%] · haut q95 +4.96% · bas q05 -6.32%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.41%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-11 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 54.2  _(neutre)_
- **ADX** : 21.9  _(pas de tendance nette)_
- **MACD** : hist 0.944  _(pas de croisement recent)_
- **BB** : %B 0.77 · largeur 12.0%
- **ATR** : 4.53 (56.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.241  _(distribution)_
- **Vol ratio** : 1.49  _(volume normal)_
- **Choppiness** : 58.5  _(transition)_
- **MA** : MA20 123.22 · MA50 126.33 · MA200 115.93  _(prix > MA20)_
- **Dist MA** : MA20 +3.3% · MA50 +0.7% · MA200 +9.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (768867 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
