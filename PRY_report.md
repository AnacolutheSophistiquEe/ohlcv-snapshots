# PRY

**Generated** : 2026-10-16T00:14:20.636551+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 3/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €109.90  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (9 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot €109.90 (+0.7% vs entrée) · entrée €109.09 · stop €100.37 · T1 €111.69 · R/R 0.3  
> ↳ _probas brutes, non calibrées · n=0_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -180 % hors [0,100] (R² max 0.84). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 16.9 < 20 (tendance pas encore confirmée) alors que Choppiness 35.2 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-15 : 109.9 · ATR Wilder 5.19 (4.72 %)_
- **Swing** : plage **104.25 → 100.75** (-5.14 % a -8.32 % sous la cloture, 0.67 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 103.98-105.76 (C). stop INDICATIF 96.11 (-4.61 % sous le bas ; sous le support 98.7-100.75 (- 0,5 ATR)).
- **Deep** : plage **100.75 → 91.45** (-8.32 % a -16.78 % sous la cloture, 1.79 ATR) — touchee 39 % → 15 % du temps en 20 seances ; supports reels dans la plage : 98.7-100.75 (B) ; 94.5-96.88 (A) ; 91.82-92.37 (A) ; 89.22-91.78 (A). stop INDICATIF 83.62 (-8.57 % sous le bas ; sous le support 86.22-86.95 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (COMBO) : 4.1 ATR sous le plus haut 20 s., RSI(2) 1.1. Limite **107.3** (seance suivante), stop catastrophe 86.54, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 103.98-105.76 (C, -3.77 %) ; 98.7-100.75 (B, -8.33 %) ; 94.5-96.88 (A, -11.85 %) ; 91.82-92.37 (A, -15.95 %) ; 89.22-91.78 (A, -16.49 %) ; 86.22-86.95 (B, -20.88 %)
- Resistances reelles au-dessus : 115.85-117.1 (A, 5.41 %) ; 122.29-123.2 (A, 11.27 %) ; 129.4-131.2 (A, 17.74 %) ; 134.3-134.9 (A, 22.2 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.65 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (6.33 %)** : le gap seul le franchit 0.315 % des séances (4 fois sur 1270).
   - exécution **1.566 pt plus bas** dans le cas TYPIQUE (médiane), 3.253 au p90, **3.668 au pire**
   - perte réelle **8.086 %** en moyenne _(tirée par la queue)_, jusqu'à **9.998 %** — au lieu des 6.33 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0055 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.865 % | p01 -3.601 % | pire -9.998 % _(sur 1270 séances)_
- **P(stop avant cible)** _(source : daily, 1271 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0003** [0.0 ; 0.0152] _(largeur 1.5 pt, n_eff 173.1)_
   - swing : **0.3825** [0.3324 ; 0.4345] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.2896** [0.2437 ; 0.339] _(largeur 9.5 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 81.0 observations effectives », dont la borne haute a 95 % vaut environ 3.7 %.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-4.11 %** | CVaR **-5.64 %** | vol 2.46 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 1.54 % contre 2.88 % aujourd'hui, rapport 0.54)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.6 % vs -7.57 % si l'on extrapolait par √5 _(rapport 0.872 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0299** (β de hausse 1.2321, asymétrie 0.8359) vs FTSEMIB — 566 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.361× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 96.9268 sur atr_grid (2.5 ATR, 11.805 %) — p(stop avant cible) 0.0715 [0.05 ; 0.10], R/R 3.4, perte reelle 11.939 % (gap inclus), CVaR 11.996 %, EV 1.2563 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.72 ATR (stop 5.745 %) — p(stop avant cible) 0.4046 [0.35 ; 0.46], R/R 6.852, perte reelle 5.923 % (gap inclus), EV 0.4035 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - 🔴 support a 1.14 ATR (stop 7.733 %) — p(stop avant cible) 0.2606 [0.22 ; 0.31], R/R 5.169, perte reelle 7.852 % (gap inclus), EV 0.806 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - ⚠ support DETECTE a 0.62 ATR du spot — compartiment <1, mesure a 49.8 % de casse (IC clusterise [0.465 ; 0.530] sur 1131 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 6.04 ATR (stop 30.846 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 1.255, perte reelle 32.353 % (gap inclus), EV 1.3788 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.75 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.18 %) — p(stop avant cible) 0.863 [0.82 ; 0.90], R/R 31.341, perte reelle 1.295 % (gap inclus), EV 0.0083 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 31.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.863, borne haute 0.896 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ grid_snapped a 0.72 ATR (stop 4.82 %) — p(stop avant cible) 0.5134 [0.46 ; 0.57], R/R 8.136, perte reelle 4.989 % (gap inclus), EV 0.0082 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 8.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.513, borne haute 0.566 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - 🔴 grid_snapped a 1.14 ATR (stop 6.808 %) — p(stop avant cible) 0.3247 [0.28 ; 0.38], R/R 5.845, perte reelle 6.944 % (gap inclus), EV 0.6204 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.0 ATR (stop 9.444 %) — p(stop avant cible) 0.1981 [0.16 ; 0.24], R/R 4.26, perte reelle 9.528 % (gap inclus), EV 0.8719 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.25 ATR (stop 10.624 %) — p(stop avant cible) 0.1374 [0.10 ; 0.18], R/R 3.786, perte reelle 10.719 % (gap inclus), EV 1.0606 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.5 ATR (stop 11.805 %) — p(stop avant cible) 0.0715 [0.05 ; 0.10], R/R 3.4, perte reelle 11.939 % (gap inclus), EV 1.2563 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.75 ATR (stop 12.985 %) — p(stop avant cible) 0.0662 [0.04 ; 0.10], R/R 3.082, perte reelle 13.169 % (gap inclus), EV 1.1975 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.23 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 14.165 %) — p(stop avant cible) 0.0408 [0.02 ; 0.07], R/R 2.844, perte reelle 14.269 % (gap inclus), EV 1.3077 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.87 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 16.526 %) — p(stop avant cible) 0.0169 [0.01 ; 0.03], R/R 2.41, perte reelle 16.84 % (gap inclus), EV 1.3825 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.60 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 18.887 %) — p(stop avant cible) 0.0101 [0.00 ; 0.03], R/R 2.041, perte reelle 19.89 % (gap inclus), EV 1.3754 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.84 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 21.248 %) — p(stop avant cible) 0.0079 [0.00 ; 0.02], R/R 1.819, perte reelle 22.317 % (gap inclus), EV 1.3609 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.13 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 23.609 %) — p(stop avant cible) 0.005 [0.00 ; 0.02], R/R 1.647, perte reelle 24.646 % (gap inclus), EV 1.3714 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.91 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 25.97 %) — p(stop avant cible) 0.0031 [0.00 ; 0.01], R/R 1.536, perte reelle 26.425 % (gap inclus), EV 1.3816 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.75 % > budget 12.00 %
   - 🟢 grid_snapped a 6.04 ATR (stop 29.92 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 1.255, perte reelle 32.353 % (gap inclus), EV 1.3788 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.75 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 33.053 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.228, perte reelle 33.053 % (gap inclus), EV 1.3861 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.64 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 35.414 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.146, perte reelle 35.414 % (gap inclus), EV 1.3861 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.64 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 37.775 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.074, perte reelle 37.775 % (gap inclus), EV 1.3861 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.64 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 109.9, ATR14 5.1893 (4.722 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.345 ATR = 1.629 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.236 % | 109.6405 | 91.88 % | 94.05 % | 94.74 % | 95.53 % | 97.2 % | 97.78 % |
| 0.1 ATR | 0.472 % | 109.3811 | 85.25 % | 89.0 % | 91.17 % | 92.94 % | 95.1 % | 96.17 % |
| 0.15 ATR | 0.708 % | 109.1216 | 77.92 % | 84.44 % | 87.5 % | 90.46 % | 92.91 % | 94.15 % |
| 0.2 ATR | 0.944 % | 108.8621 | 70.0 % | 79.29 % | 82.74 % | 86.98 % | 90.71 % | 92.23 % |
| 0.25 ATR | 1.18 % | 108.6027 | 62.28 % | 74.33 % | 78.57 % | 83.2 % | 88.11 % | 90.21 % |
| 0.35 ATR | 1.653 % | 108.0838 | 49.41 % | 63.83 % | 70.73 % | 76.54 % | 83.72 % | 87.39 % |
| 0.5 ATR | 2.361 % | 107.3054 | 35.05 % | 52.03 % | 59.92 % | 67.69 % | 76.52 % | 81.84 % |
| 0.75 ATR | 3.541 % | 106.008 | 19.41 % | 34.59 % | 43.35 % | 54.37 % | 64.84 % | 73.36 % |
| 1.0 ATR | 4.722 % | 104.7107 | 10.0 % | 23.29 % | 31.65 % | 44.33 % | 55.64 % | 65.29 % |
| 1.25 ATR | 5.902 % | 103.4134 | 5.64 % | 15.96 % | 24.01 % | 34.59 % | 47.15 % | 57.62 % |
| 1.5 ATR | 7.083 % | 102.1161 | 2.57 % | 9.71 % | 16.27 % | 24.55 % | 36.66 % | 49.14 % |
| 2.0 ATR | 9.444 % | 99.5214 | 0.4 % | 3.96 % | 7.64 % | 14.12 % | 24.38 % | 37.44 % |
| 2.5 ATR | 11.805 % | 96.9268 | 0.0 % | 1.59 % | 3.37 % | 7.95 % | 15.68 % | 26.74 % |
| 3.0 ATR | 14.165 % | 94.3321 | 0.0 % | 0.79 % | 1.69 % | 4.17 % | 9.79 % | 18.97 % |
| 4.0 ATR | 18.887 % | 89.1429 | 0.0 % | 0.1 % | 0.6 % | 1.79 % | 4.8 % | 11.1 % |
| 6.0 ATR | 28.331 % | 78.7643 | 0.0 % | 0.0 % | 0.0 % | 0.4 % | 1.8 % | 3.63 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.34 ATR | 0.40 ATR | 0.53 ATR | 0.66 ATR | 0.74 ATR | 1.00 ATR | 1.30 ATR |
| **2 s.** | 0.24 ATR | 0.53 ATR | 0.60 ATR | 0.79 ATR | 0.96 ATR | 1.11 ATR | 1.49 ATR | 1.91 ATR |
| **3 s.** | 0.30 ATR | 0.65 ATR | 0.72 ATR | 0.97 ATR | 1.22 ATR | 1.38 ATR | 1.86 ATR | 2.31 ATR |
| **5 s.** | 0.38 ATR | 0.86 ATR | 0.98 ATR | 1.29 ATR | 1.49 ATR | 1.72 ATR | 2.33 ATR | 2.89 ATR |
| **10 s.** | 0.53 ATR | 1.17 ATR | 1.30 ATR | 1.65 ATR | 1.98 ATR | 2.25 ATR | 2.98 ATR | 3.96 ATR |
| **20 s.** | 0.70 ATR | 1.48 ATR | 1.68 ATR | 2.21 ATR | 2.61 ATR | 2.93 ATR | 4.29 ATR | 5.63 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.396–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.601–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.541 %, prix 106.0084), p(touche) 34.59 % (en stress 88.12 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.725–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.541 %, prix 106.0084), p(touche) 43.35 % (en stress 95.05 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 54.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.983–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.722 %, prix 104.7105), p(touche) 44.33 % (en stress 99.01 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 47.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.301–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.083 %, prix 102.1158), p(touche) 36.66 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.677–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (9.444 %, prix 99.521), p(touche) 37.44 % (en stress 99.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 55.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 65.0 | bear 18.1 | side 16.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.728% → cible +2.378% / stop −8.0%, p_fill 76%, n_eff≈81.0) : P(cible|rempli) **22%** · **EV/risk -0.057** (×p_fill ; si rempli -0.60% du capital)
  - **swing** (entrée dip −1.608% → cible +5.366% / stop −4.799%, p_fill 66%, n_eff≈76.1) : P(cible|rempli) **26%** · **EV/risk -0.159** (×p_fill ; si rempli -1.15% du capital)
  - **deep** (entrée dip −2.487% → cible +7.657% / stop −7.264%, p_fill 63%, n_eff≈70.1) : P(cible|rempli) **26%** · **EV/risk -0.148** (×p_fill ; si rempli -1.72% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→64% · +2.0%→40% · +3.0%→25% · +5.0%→6% · +8.0%→2%
- Range intraday médian 3.71% (p90 6.32%) · excursion haute méd. +1.5% / basse méd. −1.61%
- Profil de vol intra : ouverture 2.21% vs midi 0.779% vs clôture 1.066% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 53% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.12 ; neutre — autocorr 0.003)_ ; drift intra méd. -0.354% ; recovery-V 21%
- **σ réalisé intraday** 2.479% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 65% / whipsaw 36%
- POC intraday (dernière séance, temps-au-prix) : 129.9327 (VA 129.5263–130.8813 ; dernier close 130.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 23% · rebond 60% · **stop −2.81%** sous le fill (sous le bruit) · cible +1.15% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.51% · baisse 35% (gap-down >1% 13% · >2% 3%)
- Excursion ouverture 5min (n=160) : bas méd −0.71% (p90 −2.05%) · haut méd +0.51% · range méd 1.3%
- Excursion ouverture 15min (n=160) : bas méd −0.93% (p90 −2.32%) · haut méd +0.61% · range méd 1.71%
- Excursion ouverture 30min (n=160) : bas méd −0.95% (p90 −2.41%) · haut méd +0.74% · range méd 1.88%
- Excursion ouverture 60min (n=160) : bas méd −1.05% (p90 −2.93%) · haut méd +0.83% · range méd 2.13%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 129.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 46% · séance 65% (109/159) · gap 19% · délai 0.4min · rebond 54% (61/109) (MFE +1.1%)
   - −1.0% : fill 30min 39% · séance 54% (90/159) · gap 13% · délai 1.3min · rebond 60% (54/90) (MFE +1.25%)
   - −1.5% : fill 30min 24% · séance 45% (72/159) · gap 7% · délai 21.4min · rebond 51% (39/72) (MFE +1.06%)
   - −2.0% : fill 30min 18% · séance 37% (60/159) · gap 3% · délai 42.5min · rebond 51% (34/60) (MFE +1.01%)
   - −3.0% : fill 30min 6% · séance 23% (40/159) · gap 1% · délai 93.7min · rebond 60% (26/40) (MFE +1.15%)
   - −4.0% : fill 30min 2% · séance 14% (25/159) · gap 0% · délai 282.0min · rebond 57% (15/25) (MFE +1.06%)
   - −5.0% : fill 30min 2% · séance 9% (16/159) · gap 0% · délai 394.7min · rebond 66% (11/16) (MFE +1.06%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.46% (p90 −1.89%) → stop au-delà de −1.42% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.31% (p90 −1.63%) → stop au-delà de −1.12% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.02% (p90 −1.76%) → stop au-delà de −1.27% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=487 jambes) : jambe baissière méd −1.06% (p90 −2.48%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (43 séances) :
      · −1.0% : fill 94% (39/43) · rebond 49% (19/39)
      · −2.0% : fill 77% (31/43) · rebond 58% (18/31)
      · −3.0% : fill 47% (23/43) · rebond 50% (14/23)
      · −4.0% : fill 30% (15/43) · rebond 57% (9/15)
      · −5.0% : fill 26% (12/43) · rebond 57% (8/12)
   - **flat** (27 séances) :
      · −1.0% : fill 48% (15/27) · rebond 74% (11/15)
      · −2.0% : fill 27% (8/27) · rebond 76% (7/8)
      · −3.0% : fill 16% (5/27) · rebond 41% (3/5)
      · −4.0% : fill 6% (2/27) · rebond 69% (1/2)
      · −5.0% : fill 2% (1/27) · rebond 0% (0/1)
   - **gap-up** (89 séances) :
      · −1.0% : fill 38% (36/89) · rebond 65% (24/36)
      · −2.0% : fill 23% (21/89) · rebond 30% (9/21)
      · −3.0% : fill 14% (12/89) · rebond 80% (9/12)
      · −4.0% : fill 9% (8/89) · rebond 54% (5/8)
      · −5.0% : fill 4% (3/89) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 63% si les 15 1res min sont vertes (77 cas) · 28% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:23** → P(séance verte=clôture>ouverture) 82% si début vert vs 21% si rouge (base 46% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 298min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=69) : tient le vert **82%** · continue >prix actuel 45% ; creux résiduel méd -1.18% (q20 -1.89%) → **SL/trailing à −1.89%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.07% / q75 +2.01% → **scale +1.07% / runner +2.01%**, sortie à la clôture
  - **si ROUGE au coude** (n=91) : edge inversé — récupère vert seulement **21%** (continue à baisser 66%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.77%** (au-delà de la MAE q10 -3.77%), cible rebond +1.33% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.93% .. +2.17%] · haut q95 +3.13% · bas q05 -3.36%
   - 60min (n=160) : retour [-3.28% .. +2.31%] · haut q95 +3.46% · bas q05 -3.58%
   - 2h (n=160) : retour [-3.32% .. +2.69%] · haut q95 +3.52% · bas q05 -4.05%
   - 4h (n=160) : retour [-3.46% .. +3.2%] · haut q95 +4.0% · bas q05 -4.46%
   - 6h (n=160) : retour [-3.73% .. +3.5%] · haut q95 +4.42% · bas q05 -4.65%
   - session (n=160) : retour [-4.58% .. +3.44%] · haut q95 +4.53% · bas q05 -6.29%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.44%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.72 · part idiosyncratique 0.28
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 32.3  _(momentum baissier)_
- **ADX** : 16.9  _(pas de tendance nette)_
- **MACD** : hist -1.588  _(pas de croisement recent)_
- **BB** : %B -0.17 · largeur 16.3%
- **ATR** : 5.19 (68.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.144  _(distribution)_
- **Vol ratio** : 1.41  _(volume normal)_
- **Choppiness** : 35.2  _(marche directionnel)_
- **MA** : MA20 123.47 · MA50 123.62 · MA200 120.74  _(prix < MA20)_
- **Dist MA** : MA20 -11.0% · MA50 -11.1% · MA200 -9.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (841451 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
