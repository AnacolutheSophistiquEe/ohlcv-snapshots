# SOI

**Generated** : 2026-11-25T01:11:28.190535+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 8.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €92.12  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-4 sess · macro taux)  
> ↳ spot €92.12 (+2.0% vs entrée) · entrée €90.33 · stop €80.11 · T1 €106.43 · R/R 1.58  
> ↳ ¼-Kelly 0.034 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -32 % hors [0,100] (R² max 0.52). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.160 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 3/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-24 : 92.12 · ATR Wilder 10.2 (11.07 %)_
- **Swing** : plage **76.54 → 68.61** (-16.92 % a -25.52 % sous la cloture, 0.78 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 72.55-72.9 (C). stop INDICATIF 59.1 (-13.86 % sous le bas ; sous le support 64.2-68.5 (- 0,5 ATR)).
- **Deep** : plage **68.61 → 34.72** (-25.52 % a -62.31 % sous la cloture, 3.32 ATR) — touchee 50 % → 15 % du temps en 20 seances ; supports reels dans la plage : 64.2-68.5 (B) ; 58.94-63.5 (B) ; 53.65-57.9 (B) ; 48.55-50.38 (A) ; 43.14-47.59 (A) ; 36.01-41.03 (A). stop INDICATIF 22.68 (-34.67 % sous le bas ; sous le support 27.78-30.89 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (4.22 ATR sous le plus haut 20 s., RSI(2) 24.6 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 77.85-82.4 (A, -10.55 %) ; 72.55-72.9 (C, -20.86 %) ; 64.2-68.5 (B, -25.64 %) ; 58.94-63.5 (B, -31.07 %) ; 53.65-57.9 (B, -37.15 %) ; 48.55-50.38 (A, -45.31 %)
- Resistances reelles au-dessus : 97.95-102.4 (A, 6.33 %) ; 104.8-109.55 (A, 13.76 %) ; 110.4-114.9 (A, 19.84 %) ; 116.8-121.8 (A, 26.79 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.53 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (13.04 %)** : le gap seul le franchit 0.234 % des séances (3 fois sur 1280).
   - exécution **5.679 pt plus bas** dans le cas TYPIQUE (médiane), 14.139 au p90, **16.254 au pire**
   - perte réelle **21.456 %** en moyenne _(tirée par la queue)_, jusqu'à **29.294 %** — au lieu des 13.04 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0197 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.876 % | p01 -5.662 % | pire -29.294 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4077** [0.3365 ; 0.4819] _(largeur 14.5 pt, n_eff 173.1)_
   - swing : **0.2713** [0.2265 ; 0.3199] _(largeur 9.3 pt, n_eff 345.8)_
   - deep : **0.2637** [0.2194 ; 0.312] _(largeur 9.3 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 300 séances)** : VaR **-9.83 %** | CVaR **-14.35 %** | vol 6.55 %/j
   - _fenêtre arrêtée : rupture de regime a 360 seances en arriere (volatilite 3.12 % contre 6.39 % aujourd'hui, rapport 0.49)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.27 % vs -12.21 % si l'on extrapolait par √5 _(rapport 1.086 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0866** (β de hausse 1.5764, asymétrie 0.6893) vs FCHI — 622 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.184× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 84.524 sur support (0.31 ATR, 8.246 %) — p(stop avant cible) 0.5801 [0.53 ; 0.63], R/R 4.712, perte reelle 8.565 % (gap inclus), CVaR 11.755 %, EV 1.37 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.6911 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 6.9 % du temps (< 15 %) meme a 10 seances : le R/R de 4.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.580, borne haute 0.631 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (aucun budget derive)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.31 ATR (stop 8.246 %) — p(stop avant cible) 0.5801 [0.53 ; 0.63], R/R 4.712, perte reelle 8.565 % (gap inclus), EV 1.37 % — **REFUSE**
      - refuse : cible atteinte seulement 6.9 % du temps (< 15 %) meme a 10 seances : le R/R de 4.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.580, borne haute 0.631 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.31 ATR du spot — compartiment <1, mesure a 49.2 % de casse (IC clusterise [0.458 ; 0.523] sur 1200 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 1.02 ATR (stop 16.105 %) — p(stop avant cible) 0.3034 [0.26 ; 0.35], R/R 2.458, perte reelle 16.416 % (gap inclus), EV 1.805 % — **REFUSE**
      - refuse : cible atteinte seulement 8.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.99 % > budget 12.00 %
   - 🟢 support a 2.64 ATR (stop 34.017 %) — p(stop avant cible) 0.0193 [0.01 ; 0.04], R/R 1.186, perte reelle 34.017 % (gap inclus), EV 2.103 % — **REFUSE**
      - refuse : cible atteinte seulement 8.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.28 % > budget 12.00 %
   - 🔴 grid_snapped a 0.31 ATR (stop 6.825 %) — p(stop avant cible) 0.6169 [0.56 ; 0.67], R/R 5.603, perte reelle 7.202 % (gap inclus), EV 1.8438 % — **REFUSE**
      - refuse : cible atteinte seulement 6.5 % du temps (< 15 %) meme a 10 seances : le R/R de 5.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.617, borne haute 0.667 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - 🟢 grid_snapped a 1.02 ATR (stop 14.684 %) — p(stop avant cible) 0.3504 [0.30 ; 0.40], R/R 2.661, perte reelle 15.164 % (gap inclus), EV 1.4155 % — **REFUSE**
      - refuse : cible atteinte seulement 8.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.79 % > budget 12.00 %
   - ⚪ atr_grid a 1.75 ATR (stop 19.423 %) — p(stop avant cible) 0.2327 [0.19 ; 0.28], R/R 2.044, perte reelle 19.746 % (gap inclus), EV 1.8759 % — **REFUSE**
      - refuse : cible atteinte seulement 8.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.93 % > budget 12.00 %
   - ⚪ atr_grid a 2.0 ATR (stop 22.198 %) — p(stop avant cible) 0.1626 [0.13 ; 0.20], R/R 1.798, perte reelle 22.448 % (gap inclus), EV 1.983 % — **REFUSE**
      - refuse : cible atteinte seulement 8.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.01 % > budget 12.00 %
   - ⚪ atr_grid a 2.25 ATR (stop 24.972 %) — p(stop avant cible) 0.1111 [0.08 ; 0.15], R/R 1.598, perte reelle 25.248 % (gap inclus), EV 1.9219 % — **REFUSE**
      - refuse : cible atteinte seulement 8.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.59 % > budget 12.00 %
   - 🟢 grid_snapped a 2.64 ATR (stop 32.596 %) — p(stop avant cible) 0.0231 [0.01 ; 0.04], R/R 1.236, perte reelle 32.653 % (gap inclus), EV 2.0957 % — **REFUSE**
      - refuse : cible atteinte seulement 8.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.37 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 38.846 %) — p(stop avant cible) 0.008 [0.00 ; 0.02], R/R 1.039, perte reelle 38.846 % (gap inclus), EV 2.1094 % — **REFUSE**
      - refuse : cible atteinte seulement 8.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.04 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.15 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 44.396 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.909, perte reelle 44.396 % (gap inclus), EV 2.1531 % — **REFUSE**
      - refuse : cible atteinte seulement 8.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.24 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 49.945 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.808, perte reelle 49.945 % (gap inclus), EV 2.1531 % — **REFUSE**
      - refuse : cible atteinte seulement 8.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.24 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 55.494 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.727, perte reelle 55.494 % (gap inclus), EV 2.1531 % — **REFUSE**
      - refuse : cible atteinte seulement 8.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.24 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 61.044 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.661, perte reelle 61.044 % (gap inclus), EV 2.1531 % — **REFUSE**
      - refuse : cible atteinte seulement 8.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.24 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 66.593 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.606, perte reelle 66.593 % (gap inclus), EV 2.1531 % — **REFUSE**
      - refuse : cible atteinte seulement 8.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.24 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 72.143 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.559, perte reelle 72.143 % (gap inclus), EV 2.1531 % — **REFUSE**
      - refuse : cible atteinte seulement 8.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.24 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 77.692 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.519, perte reelle 77.692 % (gap inclus), EV 2.1531 % — **REFUSE**
      - refuse : cible atteinte seulement 8.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.24 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 83.242 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.485, perte reelle 83.242 % (gap inclus), EV 2.1531 % — **REFUSE**
      - refuse : cible atteinte seulement 8.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.24 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 88.791 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.454, perte reelle 88.791 % (gap inclus), EV 2.1531 % — **REFUSE**
      - refuse : cible atteinte seulement 8.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.24 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 92.12, ATR14 10.2243 (11.099 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.358 ATR = 3.973 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.555 % | 91.6088 | 91.18 % | 94.31 % | 95.58 % | 96.65 % | 97.73 % | 98.7 % |
| 0.1 ATR | 1.11 % | 91.0976 | 84.51 % | 89.89 % | 91.85 % | 94.39 % | 96.04 % | 97.2 % |
| 0.15 ATR | 1.665 % | 90.5864 | 77.45 % | 84.89 % | 87.43 % | 90.75 % | 93.47 % | 95.2 % |
| 0.2 ATR | 2.22 % | 90.0751 | 68.73 % | 79.78 % | 83.5 % | 87.8 % | 91.3 % | 93.41 % |
| 0.25 ATR | 2.775 % | 89.5639 | 62.45 % | 75.96 % | 80.06 % | 86.12 % | 90.01 % | 92.91 % |
| 0.35 ATR | 3.885 % | 88.5415 | 50.78 % | 67.42 % | 73.18 % | 81.1 % | 85.86 % | 90.41 % |
| 0.5 ATR | 5.549 % | 87.0079 | 36.27 % | 55.84 % | 62.97 % | 73.43 % | 81.31 % | 87.81 % |
| 0.75 ATR | 8.324 % | 84.4518 | 16.86 % | 35.13 % | 46.46 % | 58.27 % | 72.9 % | 81.12 % |
| 1.0 ATR | 11.099 % | 81.8957 | 8.04 % | 23.45 % | 34.09 % | 47.24 % | 64.89 % | 75.92 % |
| 1.25 ATR | 13.874 % | 79.3396 | 4.12 % | 15.8 % | 25.54 % | 37.89 % | 57.37 % | 71.03 % |
| 1.5 ATR | 16.648 % | 76.7836 | 2.25 % | 10.7 % | 18.66 % | 30.41 % | 49.85 % | 65.13 % |
| 2.0 ATR | 22.198 % | 71.6714 | 0.59 % | 4.61 % | 9.33 % | 18.6 % | 36.1 % | 54.65 % |
| 2.5 ATR | 27.747 % | 66.5593 | 0.29 % | 2.55 % | 5.21 % | 12.3 % | 25.22 % | 46.75 % |
| 3.0 ATR | 33.297 % | 61.4471 | 0.2 % | 0.88 % | 2.75 % | 7.68 % | 17.9 % | 38.56 % |
| 4.0 ATR | 44.396 % | 51.2229 | 0.1 % | 0.59 % | 1.38 % | 3.54 % | 10.29 % | 24.58 % |
| 6.0 ATR | 66.593 % | 30.7743 | 0.0 % | 0.29 % | 0.79 % | 1.57 % | 4.45 % | 12.69 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.36 ATR | 0.41 ATR | 0.54 ATR | 0.65 ATR | 0.71 ATR | 0.94 ATR | 1.19 ATR |
| **2 s.** | 0.26 ATR | 0.57 ATR | 0.63 ATR | 0.80 ATR | 0.97 ATR | 1.11 ATR | 1.56 ATR | 1.97 ATR |
| **3 s.** | 0.32 ATR | 0.70 ATR | 0.78 ATR | 1.03 ATR | 1.27 ATR | 1.45 ATR | 1.96 ATR | 2.54 ATR |
| **5 s.** | 0.47 ATR | 0.94 ATR | 1.06 ATR | 1.41 ATR | 1.73 ATR | 1.94 ATR | 2.75 ATR | 3.65 ATR |
| **10 s.** | 0.69 ATR | 1.50 ATR | 1.68 ATR | 2.14 ATR | 2.52 ATR | 2.86 ATR | 4.10 ATR | 5.81 ATR |
| **20 s.** | 1.05 ATR | 2.29 ATR | 2.61 ATR | 3.40 ATR | 3.97 ATR | 4.77 ATR | hors grille | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.41 ATR au-dessus du haut de la grille, 0.25 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (70.8 % des re-echantillons)
- **2 seance(s)** : plage utile VIDE (borne basse 0.631 ATR au-dessus du haut de la grille, 0.5 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile VIDE (borne basse 0.78 ATR au-dessus du haut de la grille, 0.75 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile VIDE (borne basse 1.06 ATR au-dessus du haut de la grille, 1.0 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile VIDE (borne basse 1.676 ATR au-dessus du haut de la grille, 1.5 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile VIDE (borne basse 2.607 ATR au-dessus du haut de la grille, 1.5 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.138 | EV/share : €1.411 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 25 % | T2 9 % | T3 5 %
- Kelly (position) : f* 0.135 | ¼-Kelly 0.034 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 15.5 | bear 62.9 | side 21.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.88% → cible +5.599% / stop −3.359%, p_fill 85%, n_eff≈90.3) : P(cible|rempli) **11%** · **EV/risk -0.196** (×p_fill ; si rempli -0.78% du capital)
  - **swing** (entrée dip −1.941% → cible +17.824% / stop −11.319%, p_fill 71%, n_eff≈83.3) : P(cible|rempli) **14%** · **EV/risk -0.183** (×p_fill ; si rempli -2.92% du capital)
  - **deep** (entrée dip −2.972% → cible +19.074% / stop −17.158%, p_fill 72%, n_eff≈82.7) : P(cible|rempli) **29%** · **EV/risk -0.080** (×p_fill ; si rempli -1.90% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→83% · +1.0%→74% · +2.0%→62% · +3.0%→46% · +5.0%→29% · +8.0%→10%
- Range intraday médian 7.0% (p90 13.76%) · excursion haute méd. +2.7% / basse méd. −3.24%
- Profil de vol intra : ouverture 4.423% vs midi 1.287% vs clôture 1.954% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 13% · trend ↑1%/↓1% ; spike-down 73% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; neutre — autocorr 0.002)_ ; drift intra méd. -0.88% ; recovery-V 29%
- **σ réalisé intraday** 3.81% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 78% / whipsaw 36%
- POC intraday (dernière séance, temps-au-prix) : 111.4765 (VA 109.8045–114.4025 ; dernier close 111.96)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 30% · rebond 66% · **stop −6.95%** sous le fill (sous le bruit) · cible +2.1% · R/R 0.3 (high win-rate)
- Gaps overnight (n=159) : méd. 0.56% · baisse 40% (gap-down >1% 26% · >2% 18%)
- Excursion ouverture 5min (n=160) : bas méd −1.01% (p90 −3.1%) · haut méd +0.82% · range méd 2.14%
- Excursion ouverture 15min (n=160) : bas méd −1.4% (p90 −3.34%) · haut méd +1.06% · range méd 2.95%
- Excursion ouverture 30min (n=160) : bas méd −1.56% (p90 −3.74%) · haut méd +1.13% · range méd 3.18%
- Excursion ouverture 60min (n=160) : bas méd −1.76% (p90 −4.51%) · haut méd +1.44% · range méd 3.65%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 111.65 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 77% (120/159) · gap 33% · délai 0.2min · rebond 61% (78/120) (MFE +1.63%)
   - −1.0% : fill 30min 55% · séance 73% (114/159) · gap 26% · délai 0.2min · rebond 63% (76/114) (MFE +1.69%)
   - −1.5% : fill 30min 48% · séance 65% (104/159) · gap 21% · délai 1.3min · rebond 58% (72/104) (MFE +1.84%)
   - −2.0% : fill 30min 44% · séance 62% (98/159) · gap 18% · délai 4.5min · rebond 66% (72/98) (MFE +1.89%)
   - −3.0% : fill 30min 30% · séance 47% (80/159) · gap 9% · délai 8.9min · rebond 73% (66/80) (MFE +1.88%)
   - −4.0% : fill 30min 21% · séance 39% (68/159) · gap 6% · délai 15.4min · rebond 72% (54/68) (MFE +1.92%)
   - −5.0% : fill 30min 14% · séance 30% (53/159) · gap 3% · délai 38.9min · rebond 66% (39/53) (MFE +2.1%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.44% (p90 −3.17%) → stop au-delà de −1.93% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.66% (p90 −3.07%) → stop au-delà de −1.96% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.7% (p90 −2.29%) → stop au-delà de −1.88% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1324 jambes) : jambe baissière méd −1.26% (p90 −3.04%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (59 séances) :
      · −1.0% : fill 95% (56/59) · rebond 52% (33/56)
      · −2.0% : fill 93% (54/59) · rebond 60% (37/54)
      · −3.0% : fill 80% (49/59) · rebond 64% (38/49)
      · −4.0% : fill 68% (42/59) · rebond 70% (35/42)
      · −5.0% : fill 59% (35/59) · rebond 68% (27/35)
   - **flat** (11 séances) :
      · −1.0% : fill 83% (10/11) · rebond 66% (7/10)
      · −2.0% : fill 74% (9/11) · rebond 65% (7/9)
      · −3.0% : fill 74% (9/11) · rebond 73% (7/9)
      · −4.0% : fill 68% (8/11) · rebond 85% (6/8)
      · −5.0% : fill 55% (7/11) · rebond 63% (5/7)
   - **gap-up** (89 séances) :
      · −1.0% : fill 58% (48/89) · rebond 74% (36/48)
      · −2.0% : fill 40% (35/89) · rebond 74% (28/35)
      · −3.0% : fill 22% (22/89) · rebond 92% (21/22)
      · −4.0% : fill 16% (18/89) · rebond 72% (13/18)
      · −5.0% : fill 8% (11/89) · rebond 60% (7/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 62% si les 15 1res min sont vertes (75 cas) · 31% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **10min** → P(séance verte=clôture>ouverture) 63% si début vert vs 28% si rouge (base 44% · écart 34 pts) ; prédictivité sature ensuite (plafond brut 284min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **63%** · continue >prix actuel 51% ; creux résiduel méd -2.33% (q20 -4.61%) → **SL/trailing à −4.61%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.95% / q75 +5.39% → **scale +2.95% / runner +5.39%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **28%** (continue à baisser 61%) → **RÉDUIRE ~72%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.99%** (au-delà de la MAE q10 -6.99%), cible rebond +2.08% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.33% .. +4.1%] · haut q95 +5.94% · bas q05 -5.72%
   - 60min (n=160) : retour [-4.39% .. +4.55%] · haut q95 +6.48% · bas q05 -5.91%
   - 2h (n=160) : retour [-5.15% .. +5.34%] · haut q95 +7.16% · bas q05 -6.63%
   - 4h (n=160) : retour [-5.33% .. +6.48%] · haut q95 +7.84% · bas q05 -7.2%
   - 6h (n=160) : retour [-6.3% .. +7.83%] · haut q95 +8.85% · bas q05 -7.75%
   - session (n=160) : retour [-7.87% .. +8.67%] · haut q95 +10.28% · bas q05 -9.9%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 6.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **38%**. Lecture précoce 30 min : signature présente → 16% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.98% (p75 1.4% / p90 1.99%) · ~5.0 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **90%** (reprise méd 24.99 min, n=53)
   - −1.0% → **91%** (reprise méd 44.55 min, n=28)
   - −1.5% → **80%** (reprise méd 50.92 min, n=16)
   - −2.0% → **85%** (reprise méd 52.07 min, n=12)
   - −3.0% → **100%** (reprise méd 60.96 min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.99%** (p90, défaut prudent ; serré/agressif −1.4%) ; extension open→close méd +8.74% (q75 +9.27% / q95 +13.89%), MFE méd +9.37% / q90 +14.21%
   - Échelle scale-out : +9.37% (33%) / +10.06% (33%) / +14.21% (34%)
- **DÉSARMER** : repli > **−1.99%** depuis le plus-haut = décay → P(retournement) **15%** (préavis méd 36.46 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +14.21% : P(retournement après) 0% (mèche méd 2.71%)
- **CONTEXTE** : la dernière heure tient les gains 78% du temps (retour médian dernière heure +1.29%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.49 · part idiosyncratique 0.51
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-25 — US Core PCE Price Index — octobre 2026 (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 40.5  _(momentum baissier)_
- **ADX** : 21.0  _(pas de tendance nette)_
- **MACD** : hist 0.334  _(bullish_recent)_
- **BB** : %B 0.21 · largeur 46.8%
- **ATR** : 10.22 (65.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.158  _(distribution)_
- **Vol ratio** : 0.78  _(volume normal)_
- **Choppiness** : 61.2  _(transition)_
- **MA** : MA20 106.36 · MA50 128.57 · MA200 110.14  _(prix < MA20)_
- **Dist MA** : MA20 -13.4% · MA50 -28.3% · MA200 -16.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (518055 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
