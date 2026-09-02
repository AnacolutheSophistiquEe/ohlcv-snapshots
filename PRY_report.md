# PRY

**Generated** : 2026-09-02T21:48:27.918464+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €119.10  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €119.10 (+1.8% vs entrée) · entrée €116.98 · stop €107.62 · T1 €118.50 · R/R 0.16  
> ↳ P(T1 av. stop) 22 % _(réel 5 s)_ · EV/risk -0.047 _(réel 5 s)_ (GBM -0.069) · ¼-Kelly 0.096 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.390 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €116.68–€117.28 (mid €116.98)
- Spot actuel : €119.10 (+1.8% au-dessus de la zone — repli à attendre)
- Stop : €107.62 (stop swing_plan-based (-7.55%))
- Targets : T1 €118.50 · R/R 0.16 | T2 €120.02 · R/R 0.32 | T3 €121.53 · R/R 0.49
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €107.62


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.50 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (7.55 %)** : le gap seul le franchit 0.079 % des séances (1 fois sur 1270).
   - exécution **2.448 pt plus bas** dans le cas TYPIQUE (médiane), 2.448 au p90, **2.448 au pire**
   - perte réelle **9.998 %** en moyenne _(tirée par la queue)_, jusqu'à **9.998 %** — au lieu des 7.55 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0019 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.846 % | p01 -3.346 % | pire -9.998 % _(sur 1270 séances)_
- **P(stop avant cible)** _(source : daily, 1271 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0004** [0.0 ; 0.0154] _(largeur 1.5 pt, n_eff 173.1)_
   - swing : **0.4052** [0.3544 ; 0.4576] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3531** [0.3041 ; 0.4045] _(largeur 10.0 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 20.9 observations effectives », dont la borne haute a 95 % vaut environ 14.3 %.
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 16.9 observations effectives », dont la borne haute a 95 % vaut environ 17.8 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (34.2 pt), swing (43.8 pt), deep (42.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-4.27 %** | CVaR **-5.76 %** | vol 2.64 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 1.80 % contre 2.91 % aujourd'hui, rapport 0.62)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.48 % vs -7.48 % si l'on extrapolait par √5 _(rapport 0.865 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0288** (β de hausse 1.2251, asymétrie 0.8398) vs FTSEMIB — 564 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.413× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 106.1357 sur atr_grid (3.0 ATR, 10.885 %) — p(stop avant cible) 0.1307 [0.10 ; 0.17], R/R 2.751, perte reelle 10.885 % (gap inclus), CVaR 10.885 %, EV 1.2801 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 2.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.66 ATR (stop 4.538 %) — p(stop avant cible) 0.5375 [0.48 ; 0.59], R/R 4.941, perte reelle 6.061 % (gap inclus), EV -0.3144 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 4.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.537, borne haute 0.590 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.31 %) : P(cible) 0.7 % x 29.95 % + P(rien) 45.6 % x 6.01 % ne couvrent pas P(stop) 53.8 % x 6.06 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 2.06 ATR (stop 9.619 %) — p(stop avant cible) 0.2128 [0.17 ; 0.26], R/R 2.995, perte reelle 9.998 % (gap inclus), EV 0.9638 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 3.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 3.5 ATR (stop 14.833 %) — p(stop avant cible) 0.0335 [0.02 ; 0.06], R/R 2.019, perte reelle 14.833 % (gap inclus), EV 1.5702 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.83 % > budget 12.00 %
   - 🟢 support a 9.38 ATR (stop 36.16 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.828, perte reelle 36.16 % (gap inclus), EV 1.6002 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.16 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.907 %) — p(stop avant cible) 0.8904 [0.85 ; 0.92], R/R 15.954, perte reelle 1.877 % (gap inclus), EV -0.6312 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 15.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.890, borne haute 0.920 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.63 %) : P(cible) 0.7 % x 29.95 % + P(rien) 10.3 % x 8.12 % ne couvrent pas P(stop) 89.0 % x 1.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.66 ATR (stop 3.493 %) — p(stop avant cible) 0.6124 [0.56 ; 0.66], R/R 5.654, perte reelle 5.296 % (gap inclus), EV -0.6028 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 5.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.612, borne haute 0.663 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.60 %) : P(cible) 0.7 % x 29.95 % + P(rien) 38.1 % x 6.39 % ne couvrent pas P(stop) 61.2 % x 5.30 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.5 ATR (stop 5.443 %) — p(stop avant cible) 0.447 [0.40 ; 0.50], R/R 4.09, perte reelle 7.321 % (gap inclus), EV -0.0843 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 4.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.08 %) : P(cible) 0.7 % x 29.95 % + P(rien) 54.6 % x 5.46 % ne couvrent pas P(stop) 44.7 % x 7.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 6.35 %) — p(stop avant cible) 0.3882 [0.34 ; 0.44], R/R 3.786, perte reelle 7.909 % (gap inclus), EV 0.2999 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ grid_snapped a 2.06 ATR (stop 8.574 %) — p(stop avant cible) 0.2596 [0.22 ; 0.31], R/R 2.995, perte reelle 9.998 % (gap inclus), EV 0.6 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 3.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 9.071 %) — p(stop avant cible) 0.2341 [0.19 ; 0.28], R/R 2.995, perte reelle 9.998 % (gap inclus), EV 0.8312 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 3.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 10.885 %) — p(stop avant cible) 0.1307 [0.10 ; 0.17], R/R 2.751, perte reelle 10.885 % (gap inclus), EV 1.2801 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 grid_snapped a 3.5 ATR (stop 13.788 %) — p(stop avant cible) 0.054 [0.03 ; 0.08], R/R 2.172, perte reelle 13.788 % (gap inclus), EV 1.4821 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.79 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 16.328 %) — p(stop avant cible) 0.0202 [0.01 ; 0.04], R/R 1.834, perte reelle 16.328 % (gap inclus), EV 1.6066 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.33 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 18.142 %) — p(stop avant cible) 0.0121 [0.00 ; 0.03], R/R 1.651, perte reelle 18.142 % (gap inclus), EV 1.6082 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.14 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 19.956 %) — p(stop avant cible) 0.0101 [0.00 ; 0.03], R/R 1.501, perte reelle 19.956 % (gap inclus), EV 1.5921 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.96 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 21.77 %) — p(stop avant cible) 0.0087 [0.00 ; 0.02], R/R 1.376, perte reelle 21.77 % (gap inclus), EV 1.5844 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.77 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 23.585 %) — p(stop avant cible) 0.0059 [0.00 ; 0.02], R/R 1.27, perte reelle 23.585 % (gap inclus), EV 1.5909 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.59 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 25.399 %) — p(stop avant cible) 0.0038 [0.00 ; 0.02], R/R 1.179, perte reelle 25.399 % (gap inclus), EV 1.5962 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.40 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 27.213 %) — p(stop avant cible) 0.003 [0.00 ; 0.01], R/R 1.1, perte reelle 27.213 % (gap inclus), EV 1.5938 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.21 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 29.027 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 1.032, perte reelle 29.027 % (gap inclus), EV 1.5984 % — **REFUSE**
      - refuse : cible atteinte seulement 0.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.03 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 119.1, ATR14 4.3214 (3.628 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.345 ATR = 1.252 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.181 % | 118.8839 | 92.08 % | 94.05 % | 94.84 % | 95.63 % | 97.3 % | 97.88 % |
| 0.1 ATR | 0.363 % | 118.6679 | 85.45 % | 89.0 % | 91.27 % | 93.04 % | 95.2 % | 96.27 % |
| 0.15 ATR | 0.544 % | 118.4518 | 77.82 % | 84.24 % | 87.6 % | 90.56 % | 93.01 % | 94.25 % |
| 0.2 ATR | 0.726 % | 118.2357 | 69.6 % | 78.89 % | 82.74 % | 86.88 % | 90.71 % | 92.23 % |
| 0.25 ATR | 0.907 % | 118.0196 | 62.08 % | 74.33 % | 78.87 % | 83.3 % | 88.21 % | 90.31 % |
| 0.35 ATR | 1.27 % | 117.5875 | 49.31 % | 64.02 % | 71.23 % | 77.04 % | 83.92 % | 87.49 % |
| 0.5 ATR | 1.814 % | 116.9393 | 35.15 % | 52.33 % | 60.42 % | 68.39 % | 76.62 % | 81.84 % |
| 0.75 ATR | 2.721 % | 115.8589 | 19.21 % | 34.49 % | 43.55 % | 54.77 % | 64.94 % | 73.16 % |
| 1.0 ATR | 3.628 % | 114.7786 | 10.0 % | 23.29 % | 31.65 % | 44.43 % | 55.74 % | 65.09 % |
| 1.25 ATR | 4.536 % | 113.6982 | 5.74 % | 15.96 % | 24.01 % | 34.39 % | 47.45 % | 57.32 % |
| 1.5 ATR | 5.443 % | 112.6179 | 2.48 % | 9.71 % | 16.07 % | 24.25 % | 37.06 % | 48.84 % |
| 2.0 ATR | 7.257 % | 110.4571 | 0.4 % | 3.96 % | 7.44 % | 13.82 % | 24.98 % | 37.84 % |
| 2.5 ATR | 9.071 % | 108.2964 | 0.0 % | 1.59 % | 3.37 % | 7.75 % | 16.08 % | 27.45 % |
| 3.0 ATR | 10.885 % | 106.1357 | 0.0 % | 0.79 % | 1.69 % | 4.17 % | 10.19 % | 19.88 % |
| 4.0 ATR | 14.514 % | 101.8143 | 0.0 % | 0.1 % | 0.6 % | 1.79 % | 4.9 % | 11.5 % |
| 6.0 ATR | 21.77 % | 93.1714 | 0.0 % | 0.0 % | 0.0 % | 0.4 % | 1.8 % | 3.63 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.34 ATR | 0.40 ATR | 0.53 ATR | 0.66 ATR | 0.74 ATR | 1.00 ATR | 1.31 ATR |
| **2 s.** | 0.24 ATR | 0.53 ATR | 0.60 ATR | 0.78 ATR | 0.96 ATR | 1.11 ATR | 1.49 ATR | 1.91 ATR |
| **3 s.** | 0.30 ATR | 0.65 ATR | 0.73 ATR | 0.97 ATR | 1.22 ATR | 1.38 ATR | 1.85 ATR | 2.30 ATR |
| **5 s.** | 0.39 ATR | 0.86 ATR | 0.99 ATR | 1.28 ATR | 1.48 ATR | 1.70 ATR | 2.31 ATR | 2.88 ATR |
| **10 s.** | 0.54 ATR | 1.17 ATR | 1.31 ATR | 1.67 ATR | 2.00 ATR | 2.28 ATR | 3.04 ATR | 3.98 ATR |
| **20 s.** | 0.70 ATR | 1.47 ATR | 1.68 ATR | 2.23 ATR | 2.66 ATR | 2.99 ATR | 4.38 ATR | 5.65 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.396–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.603–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.721 %, prix 115.8593), p(touche) 34.49 % (en stress 86.14 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.729–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.721 %, prix 115.8593), p(touche) 43.55 % (en stress 95.05 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 56.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.986–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.628 %, prix 114.7791), p(touche) 44.43 % (en stress 99.01 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.309–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.443 %, prix 112.6174), p(touche) 37.06 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.675–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.257 %, prix 110.4569), p(touche) 37.84 % (en stress 99.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 55.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.069 | EV/share : €-0.641 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 53 % | T2 30 % | T3 14 %
- Kelly (position) : f* 0.383 | ¼-Kelly 0.096 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 8.5 | bear 6.2 | side 85.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.783% → cible +1.298% / stop −8.0%, p_fill 50%, n_eff≈20.9) : P(cible|rempli) **22%** · **EV/risk -0.047** (×p_fill ; si rempli -0.76% du capital)
  - **swing** (entrée dip −3.922% → cible +2.902% / stop −3.776%, p_fill 37%, n_eff≈16.9) : P(cible|rempli) **59%** · **EV/risk +0.005** (×p_fill ; si rempli +0.06% du capital)
  - **deep** (entrée dip −6.058% → cible +4.104% / stop −5.793%, p_fill 51%, n_eff≈18.8) : P(cible|rempli) **57%** · **EV/risk +0.055** (×p_fill ; si rempli +0.62% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→65% · +2.0%→38% · +3.0%→25% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.96% (p90 6.32%) · excursion haute méd. +1.25% / basse méd. −1.6%
- Profil de vol intra : ouverture 2.359% vs midi 0.759% vs clôture 1.106% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 53% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.122 ; neutre — autocorr -0.02)_ ; drift intra méd. -0.859% ; recovery-V 17%
- **σ réalisé intraday** 2.472% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 67% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 118.2512 (VA 117.0762–118.6037 ; dernier close 117.56)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 29% · rebond 68% · **stop −2.77%** sous le fill (sous le bruit) · cible +1.69% · R/R 0.61 (high win-rate)
- Gaps overnight (n=159) : méd. 0.4% · baisse 36% (gap-down >1% 14% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −2.12%) · haut méd +0.38% · range méd 1.38%
- Excursion ouverture 15min (n=160) : bas méd −1.0% (p90 −2.37%) · haut méd +0.58% · range méd 1.71%
- Excursion ouverture 30min (n=160) : bas méd −1.03% (p90 −2.96%) · haut méd +0.69% · range méd 1.97%
- Excursion ouverture 60min (n=160) : bas méd −1.13% (p90 −3.19%) · haut méd +0.86% · range méd 2.21%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 117.1 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 54% · séance 70% (110/159) · gap 21% · délai 0.3min · rebond 49% (63/110) (MFE +0.99%)
   - −1.0% : fill 30min 44% · séance 60% (93/159) · gap 14% · délai 1.3min · rebond 56% (57/93) (MFE +1.11%)
   - −1.5% : fill 30min 31% · séance 50% (73/159) · gap 10% · délai 10.9min · rebond 52% (42/73) (MFE +1.06%)
   - −2.0% : fill 30min 21% · séance 41% (60/159) · gap 6% · délai 28.6min · rebond 56% (38/60) (MFE +1.1%)
   - −3.0% : fill 30min 7% · séance 29% (42/159) · gap 2% · délai 91.4min · rebond 68% (30/42) (MFE +1.69%)
   - −4.0% : fill 30min 2% · séance 19% (26/159) · gap 1% · délai 337.0min · rebond 54% (16/26) (MFE +1.15%)
   - −5.0% : fill 30min 1% · séance 12% (17/159) · gap 1% · délai 395.2min · rebond 62% (12/17) (MFE +1.17%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.47% (p90 −1.75%) → stop au-delà de −1.4% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.37% (p90 −2.0%) → stop au-delà de −1.15% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.02% (p90 −1.77%) → stop au-delà de −1.07% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=496 jambes) : jambe baissière méd −1.07% (p90 −2.63%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (42 séances) :
      · −1.0% : fill 91% (38/42) · rebond 42% (20/38)
      · −2.0% : fill 74% (31/42) · rebond 60% (20/31)
      · −3.0% : fill 56% (25/42) · rebond 70% (18/25)
      · −4.0% : fill 38% (15/42) · rebond 50% (9/15)
      · −5.0% : fill 31% (12/42) · rebond 48% (8/12)
   - **flat** (27 séances) :
      · −1.0% : fill 63% (17/27) · rebond 74% (13/17)
      · −2.0% : fill 35% (8/27) · rebond 76% (7/8)
      · −3.0% : fill 21% (5/27) · rebond 41% (3/5)
      · −4.0% : fill 8% (2/27) · rebond 69% (1/2)
      · −5.0% : fill 2% (1/27) · rebond 0% (0/1)
   - **gap-up** (90 séances) :
      · −1.0% : fill 45% (38/90) · rebond 60% (24/38)
      · −2.0% : fill 28% (21/90) · rebond 40% (11/21)
      · −3.0% : fill 19% (12/90) · rebond 77% (9/12)
      · −4.0% : fill 14% (9/90) · rebond 55% (6/9)
      · −5.0% : fill 7% (4/90) · rebond 100% (4/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 63% si les 15 1res min sont vertes (76 cas) · 27% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **58min** → P(séance verte=clôture>ouverture) 73% si début vert vs 20% si rouge (base 44% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **73%** · continue >prix actuel 51% ; creux résiduel méd -1.14% (q20 -2.22%) → **SL/trailing à −2.22%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.26% / q75 +2.27% → **scale +1.26% / runner +2.27%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **20%** (continue à baisser 66%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.08%** (au-delà de la MAE q10 -4.08%), cible rebond +1.04% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.05% .. +2.8%] · haut q95 +3.17% · bas q05 -3.38%
   - 60min (n=160) : retour [-3.32% .. +2.22%] · haut q95 +3.47% · bas q05 -3.59%
   - 2h (n=160) : retour [-3.44% .. +2.64%] · haut q95 +3.6% · bas q05 -4.21%
   - 4h (n=160) : retour [-3.47% .. +3.21%] · haut q95 +4.02% · bas q05 -4.52%
   - 6h (n=160) : retour [-3.75% .. +3.7%] · haut q95 +4.49% · bas q05 -4.73%
   - session (n=160) : retour [-4.81% .. +3.64%] · haut q95 +5.05% · bas q05 -6.35%


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
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 34.3  _(momentum baissier)_
- **ADX** : 27.6  _(tendance etablie)_
- **MACD** : hist -0.245  _(bearish_recent)_
- **BB** : %B 0.2 · largeur 13.5%
- **ATR** : 4.32 (52.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.387  _(distribution)_
- **Vol ratio** : 0.92  _(volume normal)_
- **Choppiness** : 49.2  _(transition)_
- **MA** : MA20 124.1 · MA50 128.7 · MA200 114.66  _(prix < MA20)_
- **Dist MA** : MA20 -4.0% · MA50 -7.5% · MA200 +3.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (495854 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
