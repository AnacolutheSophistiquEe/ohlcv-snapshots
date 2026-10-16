# PRY

**Generated** : 2026-10-16T21:50:56.351107+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 6/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €109.40  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (10 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot €109.40 (+0.6% vs entrée) · entrée €108.72 · stop €100.02 · T1 €111.30 · R/R 0.3  
> ↳ _probas brutes, non calibrées · n=0_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 18.7 < 20 (tendance pas encore confirmée) alors que Choppiness 34.9 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-16 : 109.4 · ATR Wilder 5.12 (4.68 %)_
- **Swing** : plage **103.81 → 100.34** (-5.11 % a -8.28 % sous la cloture, 0.68 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 98.7-100.75 (B). stop INDICATIF 91.93 (-8.38 % sous le bas ; sous le support 94.5-96.88 (- 0,5 ATR)).
- **Deep** : plage **100.34 → 91.15** (-8.28 % a -16.68 % sous la cloture, 1.79 ATR) — touchee 39 % → 15 % du temps en 20 seances ; supports reels dans la plage : 98.7-100.75 (B) ; 94.5-96.88 (A) ; 91.82-92.37 (A) ; 89.22-91.78 (A). stop INDICATIF 83.66 (-8.23 % sous le bas ; sous le support 86.22-86.95 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (COMBO) : 4.25 ATR sous le plus haut 20 s., RSI(2) 1.0. Limite **106.84** (seance suivante), stop catastrophe 86.34, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 103.98-105.76 (C, -3.33 %) ; 98.7-100.75 (B, -7.91 %) ; 94.5-96.88 (A, -11.45 %) ; 91.82-92.37 (A, -15.57 %) ; 89.22-91.78 (A, -16.11 %) ; 86.22-86.95 (B, -20.52 %)
- Resistances reelles au-dessus : 115.85-117.1 (A, 5.9 %) ; 119.65-119.65 (B, 9.37 %) ; 122.29-123.2 (A, 11.78 %) ; 129.4-131.2 (A, 18.28 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.65 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (6.08 %)** : le gap seul le franchit 0.315 % des séances (4 fois sur 1270).
   - exécution **1.816 pt plus bas** dans le cas TYPIQUE (médiane), 3.503 au p90, **3.918 au pire**
   - perte réelle **8.086 %** en moyenne _(tirée par la queue)_, jusqu'à **9.998 %** — au lieu des 6.08 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0063 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.865 % | p01 -3.601 % | pire -9.998 % _(sur 1270 séances)_
- **P(stop avant cible)** _(source : daily, 1271 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0003** [0.0 ; 0.0152] _(largeur 1.5 pt, n_eff 173.1)_
   - swing : **0.3882** [0.3379 ; 0.4403] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.3008** [0.2543 ; 0.3506] _(largeur 9.6 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 82.4 observations effectives », dont la borne haute a 95 % vaut environ 3.6 %.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-4.11 %** | CVaR **-5.64 %** | vol 2.46 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 1.57 % contre 2.86 % aujourd'hui, rapport 0.55)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.62 % vs -7.57 % si l'on extrapolait par √5 _(rapport 0.875 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0302** (β de hausse 1.2316, asymétrie 0.8365) vs FTSEMIB — 565 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.347× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 97.8045 sur atr_grid (2.25 ATR, 10.599 %) — p(stop avant cible) 0.1423 [0.11 ; 0.18], R/R 3.857, perte reelle 10.693 % (gap inclus), CVaR 10.865 %, EV 0.9975 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.63 ATR (stop 5.559 %) — p(stop avant cible) 0.427 [0.38 ; 0.48], R/R 7.207, perte reelle 5.722 % (gap inclus), EV 0.3264 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - 🔴 support a 1.05 ATR (stop 7.559 %) — p(stop avant cible) 0.2697 [0.23 ; 0.32], R/R 5.363, perte reelle 7.69 % (gap inclus), EV 0.7843 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - ⚠ support DETECTE a 0.53 ATR du spot — compartiment <1, mesure a 49.8 % de casse (IC clusterise [0.466 ; 0.530] sur 1220 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 5.98 ATR (stop 30.777 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 1.275, perte reelle 32.353 % (gap inclus), EV 1.297 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.16 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.178 %) — p(stop avant cible) 0.8637 [0.82 ; 0.90], R/R 31.907, perte reelle 1.292 % (gap inclus), EV 0.0038 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 31.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.864, borne haute 0.897 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ grid_snapped a 0.63 ATR (stop 4.372 %) — p(stop avant cible) 0.5431 [0.49 ; 0.60], R/R 9.088, perte reelle 4.538 % (gap inclus), EV 0.0776 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 9.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.543, borne haute 0.595 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - 🔴 grid_snapped a 1.05 ATR (stop 6.372 %) — p(stop avant cible) 0.3695 [0.32 ; 0.42], R/R 6.31, perte reelle 6.536 % (gap inclus), EV 0.5034 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 1.75 ATR (stop 8.244 %) — p(stop avant cible) 0.2489 [0.21 ; 0.30], R/R 4.939, perte reelle 8.349 % (gap inclus), EV 0.7635 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.0 ATR (stop 9.422 %) — p(stop avant cible) 0.2028 [0.16 ; 0.25], R/R 4.339, perte reelle 9.505 % (gap inclus), EV 0.8155 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.25 ATR (stop 10.599 %) — p(stop avant cible) 0.1423 [0.11 ; 0.18], R/R 3.857, perte reelle 10.693 % (gap inclus), EV 0.9975 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 2.5 ATR (stop 11.777 %) — p(stop avant cible) 0.0768 [0.05 ; 0.11], R/R 3.324, perte reelle 12.405 % (gap inclus), EV 1.1452 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.74 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 12.955 %) — p(stop avant cible) 0.0716 [0.05 ; 0.10], R/R 3.039, perte reelle 13.57 % (gap inclus), EV 1.0857 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.83 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 14.132 %) — p(stop avant cible) 0.0463 [0.03 ; 0.07], R/R 2.794, perte reelle 14.758 % (gap inclus), EV 1.1958 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.58 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 16.488 %) — p(stop avant cible) 0.0225 [0.01 ; 0.04], R/R 2.395, perte reelle 17.221 % (gap inclus), EV 1.2702 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.57 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 18.843 %) — p(stop avant cible) 0.0158 [0.01 ; 0.03], R/R 2.116, perte reelle 19.492 % (gap inclus), EV 1.2593 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.87 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 21.198 %) — p(stop avant cible) 0.0078 [0.00 ; 0.02], R/R 1.85, perte reelle 22.286 % (gap inclus), EV 1.2776 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.53 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 23.554 %) — p(stop avant cible) 0.0049 [0.00 ; 0.02], R/R 1.676, perte reelle 24.612 % (gap inclus), EV 1.2885 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.32 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 25.909 %) — p(stop avant cible) 0.0031 [0.00 ; 0.01], R/R 1.563, perte reelle 26.389 % (gap inclus), EV 1.2961 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.16 % > budget 12.00 %
   - 🟢 grid_snapped a 5.98 ATR (stop 29.59 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 1.275, perte reelle 32.353 % (gap inclus), EV 1.297 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.16 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 32.975 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 1.251, perte reelle 32.975 % (gap inclus), EV 1.299 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.10 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 35.331 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.167, perte reelle 35.331 % (gap inclus), EV 1.301 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.05 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 37.686 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.094, perte reelle 37.686 % (gap inclus), EV 1.301 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.05 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 109.4, ATR14 5.1536 (4.711 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.345 ATR = 1.625 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.236 % | 109.1423 | 91.88 % | 94.05 % | 94.74 % | 95.53 % | 97.2 % | 97.78 % |
| 0.1 ATR | 0.471 % | 108.8846 | 85.25 % | 89.0 % | 91.17 % | 92.94 % | 95.1 % | 96.17 % |
| 0.15 ATR | 0.707 % | 108.627 | 77.92 % | 84.44 % | 87.5 % | 90.46 % | 92.91 % | 94.15 % |
| 0.2 ATR | 0.942 % | 108.3693 | 69.9 % | 79.29 % | 82.74 % | 86.98 % | 90.71 % | 92.23 % |
| 0.25 ATR | 1.178 % | 108.1116 | 62.18 % | 74.33 % | 78.57 % | 83.2 % | 88.11 % | 90.21 % |
| 0.35 ATR | 1.649 % | 107.5963 | 49.31 % | 63.83 % | 70.73 % | 76.54 % | 83.72 % | 87.39 % |
| 0.5 ATR | 2.355 % | 106.8232 | 34.95 % | 52.03 % | 59.92 % | 67.69 % | 76.52 % | 81.84 % |
| 0.75 ATR | 3.533 % | 105.5348 | 19.41 % | 34.69 % | 43.45 % | 54.47 % | 64.94 % | 73.46 % |
| 1.0 ATR | 4.711 % | 104.2464 | 10.0 % | 23.39 % | 31.75 % | 44.43 % | 55.74 % | 65.39 % |
| 1.25 ATR | 5.888 % | 102.958 | 5.64 % | 16.06 % | 24.11 % | 34.69 % | 47.25 % | 57.72 % |
| 1.5 ATR | 7.066 % | 101.6696 | 2.57 % | 9.81 % | 16.37 % | 24.65 % | 36.76 % | 49.24 % |
| 2.0 ATR | 9.422 % | 99.0929 | 0.4 % | 4.06 % | 7.74 % | 14.21 % | 24.48 % | 37.54 % |
| 2.5 ATR | 11.777 % | 96.5161 | 0.0 % | 1.68 % | 3.47 % | 8.05 % | 15.78 % | 26.84 % |
| 3.0 ATR | 14.132 % | 93.9393 | 0.0 % | 0.89 % | 1.79 % | 4.27 % | 9.89 % | 19.07 % |
| 4.0 ATR | 18.843 % | 88.7857 | 0.0 % | 0.2 % | 0.6 % | 1.89 % | 4.9 % | 11.2 % |
| 6.0 ATR | 28.265 % | 78.4786 | 0.0 % | 0.0 % | 0.0 % | 0.4 % | 1.8 % | 3.63 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.34 ATR | 0.40 ATR | 0.53 ATR | 0.66 ATR | 0.74 ATR | 1.00 ATR | 1.30 ATR |
| **2 s.** | 0.24 ATR | 0.53 ATR | 0.60 ATR | 0.79 ATR | 0.96 ATR | 1.12 ATR | 1.49 ATR | 1.92 ATR |
| **3 s.** | 0.30 ATR | 0.65 ATR | 0.73 ATR | 0.97 ATR | 1.22 ATR | 1.38 ATR | 1.87 ATR | 2.32 ATR |
| **5 s.** | 0.38 ATR | 0.86 ATR | 0.99 ATR | 1.29 ATR | 1.49 ATR | 1.72 ATR | 2.34 ATR | 2.90 ATR |
| **10 s.** | 0.53 ATR | 1.17 ATR | 1.30 ATR | 1.65 ATR | 1.98 ATR | 2.26 ATR | 2.99 ATR | 3.98 ATR |
| **20 s.** | 0.70 ATR | 1.48 ATR | 1.68 ATR | 2.21 ATR | 2.62 ATR | 2.94 ATR | 4.32 ATR | 5.64 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.395–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.601–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.533 %, prix 105.5349), p(touche) 34.69 % (en stress 88.12 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.726–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.533 %, prix 105.5349), p(touche) 43.45 % (en stress 95.05 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 55.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.986–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.711 %, prix 104.2462), p(touche) 44.43 % (en stress 99.01 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.304–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.066 %, prix 101.6698), p(touche) 36.76 % (en stress 98.02 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.681–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (9.422 %, prix 99.0923), p(touche) 37.54 % (en stress 99.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 55.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 48.0 | bear 27.4 | side 24.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.62% → cible +2.37% / stop −8.0%, p_fill 76%, n_eff≈82.4) : P(cible|rempli) **23%** · **EV/risk -0.062** (×p_fill ; si rempli -0.65% du capital)
  - **swing** (entrée dip −1.369% → cible +5.34% / stop −4.776%, p_fill 70%, n_eff≈79.9) : P(cible|rempli) **26%** · **EV/risk -0.175** (×p_fill ; si rempli -1.20% du capital)
  - **deep** (entrée dip −2.114% → cible +7.609% / stop −7.219%, p_fill 71%, n_eff≈78.7) : P(cible|rempli) **27%** · **EV/risk -0.135** (×p_fill ; si rempli -1.38% du capital)
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

**Factor** : R² 0.74 · part idiosyncratique 0.26
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 31.6  _(momentum baissier)_
- **ADX** : 18.7  _(pas de tendance nette)_
- **MACD** : hist -1.849  _(pas de croisement recent)_
- **BB** : %B -0.06 · largeur 19.4%
- **ATR** : 5.15 (67.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.09  _(distribution)_
- **Vol ratio** : 1.37  _(volume normal)_
- **Choppiness** : 34.9  _(marche directionnel)_
- **MA** : MA20 122.81 · MA50 123.29 · MA200 120.83  _(prix < MA20)_
- **Dist MA** : MA20 -10.9% · MA50 -11.3% · MA200 -9.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (786130 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
