# PLTR

**Generated** : 2026-10-23T22:04:19.221350+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 7/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $196.75  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-28 — US FOMC Rate Decision (J-4 sess · macro taux)  
> ↳ spot $196.75 (+0.9% vs entrée) · entrée $194.93 · stop $185.97 · T1 $204.96 · R/R 1.12  
> ↳ ¼-Kelly 0.013 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-23 : 196.75 · ATR Wilder 8.13 (4.13 %)_
- **Swing** : plage **187.4 → 180.65** (-4.75 % a -8.18 % sous la cloture, 0.83 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 184.45-188.37 (A) ; 180.18-182.44 (B). stop INDICATIF 170.22 (-5.77 % sous le bas ; sous le support 174.29-176.5 (- 0,5 ATR)).
- **Deep** : plage **180.65 → 165.9** (-8.18 % a -15.68 % sous la cloture, 1.81 ATR) — touchee 42 % → 15 % du temps en 20 seances ; supports reels dans la plage : 180.18-182.44 (B) ; 174.29-176.5 (B) ; 168.9-172.0 (B) ; 164.55-166.35 (A). stop INDICATIF 156.32 (-5.77 % sous le bas ; sous le support 160.39-163.7 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (1.99 ATR sous le plus haut 20 s., RSI(2) 49.1 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 190.0-190.39 (C, -3.23 %) ; 184.45-188.37 (A, -4.26 %) ; 180.18-182.44 (B, -7.27 %) ; 174.29-176.5 (B, -10.29 %) ; 168.9-172.0 (B, -12.58 %) ; 164.55-166.35 (A, -15.45 %)
- Resistances reelles au-dessus : 207.52-207.52 (C, 5.47 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.71 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (5.48 %)** : le gap seul le franchit 1.196 % des séances (15 fois sur 1254).
   - exécution **2.685 pt plus bas** dans le cas TYPIQUE (médiane), 8.433 au p90, **12.452 au pire**
   - perte réelle **9.434 %** en moyenne _(tirée par la queue)_, jusqu'à **17.932 %** — au lieu des 5.48 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0473 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.86 % | p01 -6.138 % | pire -17.932 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2469** [0.1872 ; 0.315] _(largeur 12.8 pt, n_eff 173.1)_
   - swing : **0.4025** [0.3518 ; 0.4548] _(largeur 10.3 pt, n_eff 345.7)_
   - deep : **0.3642** [0.3148 ; 0.4159] _(largeur 10.1 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.14 %** | CVaR **-8.42 %** | vol 4.26 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.3 % vs -13.77 % si l'on extrapolait par √5 _(rapport 0.966 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6997** (β de hausse 1.4125, asymétrie 1.2034) vs IWM — 606 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 187.8339 sur sr_based (0.47 ATR, 4.532 %) — p(stop avant cible) 0.5738 [0.52 ; 0.63], R/R 3.128, perte reelle 4.59 % (gap inclus), CVaR 5.199 %, EV 1.1262 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.1365 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.574, borne haute 0.625 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.47 ATR (stop 4.532 %) — p(stop avant cible) 0.5738 [0.52 ; 0.63], R/R 3.128, perte reelle 4.59 % (gap inclus), EV 1.1262 % — **REFUSE**
      - refuse : p_stop_first 0.574, borne haute 0.625 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_based a 1.5 ATR (stop 6.834 %) — p(stop avant cible) 0.4005 [0.35 ; 0.45], R/R 2.079, perte reelle 6.905 % (gap inclus), EV 1.7044 % — **REFUSE**
      - refuse : R/R 2.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ swing_based a 1.57 ATR (stop 9.559 %) — p(stop avant cible) 0.2859 [0.24 ; 0.34], R/R 1.492, perte reelle 9.624 % (gap inclus), EV 1.5215 % — **REFUSE**
      - refuse : R/R 1.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🔴 support a 2.26 ATR (stop 12.689 %) — p(stop avant cible) 0.1759 [0.14 ; 0.22], R/R 1.116, perte reelle 12.861 % (gap inclus), EV 1.6054 % — **REFUSE**
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.29 % > budget 12.00 %
      - ⚠ support DETECTE a 0.37 ATR du spot — compartiment <1, mesure a 47.8 % de casse (IC clusterise [0.449 ; 0.507] sur 1237 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 8.8 ATR (stop 42.478 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.338, perte reelle 42.478 % (gap inclus), EV 2.0685 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.55 % > budget 12.00 %
   - 🟢 support a 10.08 ATR (stop 48.333 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.297, perte reelle 48.333 % (gap inclus), EV 2.0685 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.55 % > budget 12.00 %
   - ⚪ grid_snapped a 0.47 ATR (stop 3.502 %) — p(stop avant cible) 0.6495 [0.60 ; 0.70], R/R 3.994, perte reelle 3.595 % (gap inclus), EV 0.8833 % — **REFUSE**
      - refuse : cible atteinte seulement 14.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.649, borne haute 0.698 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.25 ATR (stop 5.695 %) — p(stop avant cible) 0.4864 [0.43 ; 0.54], R/R 2.494, perte reelle 5.757 % (gap inclus), EV 1.2632 % — **REFUSE**
      - refuse : R/R 2.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 1.57 ATR (stop 8.53 %) — p(stop avant cible) 0.3129 [0.27 ; 0.36], R/R 1.664, perte reelle 8.631 % (gap inclus), EV 1.6541 % — **REFUSE**
      - refuse : R/R 1.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🔴 grid_snapped a 2.26 ATR (stop 11.659 %) — p(stop avant cible) 0.2081 [0.17 ; 0.25], R/R 1.214, perte reelle 11.824 % (gap inclus), EV 1.5586 % — **REFUSE**
      - refuse : R/R 1.21 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.34 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 13.669 %) — p(stop avant cible) 0.1505 [0.12 ; 0.19], R/R 1.034, perte reelle 13.893 % (gap inclus), EV 1.5211 % — **REFUSE**
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.34 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 15.947 %) — p(stop avant cible) 0.1023 [0.07 ; 0.14], R/R 0.888, perte reelle 16.168 % (gap inclus), EV 1.6223 % — **REFUSE**
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.40 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 18.225 %) — p(stop avant cible) 0.0742 [0.05 ; 0.11], R/R 0.781, perte reelle 18.379 % (gap inclus), EV 1.6643 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.45 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 20.503 %) — p(stop avant cible) 0.042 [0.02 ; 0.07], R/R 0.695, perte reelle 20.655 % (gap inclus), EV 1.8291 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.14 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 22.781 %) — p(stop avant cible) 0.0204 [0.01 ; 0.04], R/R 0.622, perte reelle 23.096 % (gap inclus), EV 1.9619 % — **REFUSE**
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.18 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 25.06 %) — p(stop avant cible) 0.0063 [0.00 ; 0.02], R/R 0.566, perte reelle 25.365 % (gap inclus), EV 2.0319 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.90 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 27.338 %) — p(stop avant cible) 0.0041 [0.00 ; 0.02], R/R 0.504, perte reelle 28.501 % (gap inclus), EV 2.0412 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.91 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 29.616 %) — p(stop avant cible) 0.0029 [0.00 ; 0.01], R/R 0.467, perte reelle 30.722 % (gap inclus), EV 2.0547 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.84 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 31.894 %) — p(stop avant cible) 0.0023 [0.00 ; 0.01], R/R 0.443, perte reelle 32.425 % (gap inclus), EV 2.0567 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.78 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 34.172 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 0.413, perte reelle 34.764 % (gap inclus), EV 2.0661 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.63 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 36.45 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 0.394, perte reelle 36.457 % (gap inclus), EV 2.0657 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.61 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 196.75, ATR14 8.9645 (4.556 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.36 ATR = 1.64 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.228 % | 196.3018 | 92.96 % | 95.47 % | 96.27 % | 97.07 % | 98.27 % | 98.67 % |
| 0.1 ATR | 0.456 % | 195.8536 | 85.01 % | 89.63 % | 91.53 % | 93.74 % | 95.23 % | 96.41 % |
| 0.15 ATR | 0.683 % | 195.4053 | 77.16 % | 83.89 % | 86.19 % | 90.1 % | 92.59 % | 94.26 % |
| 0.2 ATR | 0.911 % | 194.9571 | 69.22 % | 78.45 % | 81.85 % | 86.57 % | 90.36 % | 92.41 % |
| 0.25 ATR | 1.139 % | 194.5089 | 62.27 % | 73.51 % | 77.62 % | 83.03 % | 87.72 % | 90.77 % |
| 0.35 ATR | 1.595 % | 193.6124 | 51.01 % | 65.36 % | 71.07 % | 78.18 % | 83.65 % | 87.59 % |
| 0.5 ATR | 2.278 % | 192.2678 | 36.22 % | 52.47 % | 59.48 % | 68.79 % | 77.46 % | 82.67 % |
| 0.75 ATR | 3.417 % | 190.0266 | 19.42 % | 35.05 % | 44.35 % | 55.05 % | 66.19 % | 75.28 % |
| 1.0 ATR | 4.556 % | 187.7855 | 8.95 % | 22.86 % | 32.46 % | 43.64 % | 55.63 % | 66.15 % |
| 1.25 ATR | 5.695 % | 185.5444 | 4.43 % | 15.41 % | 23.29 % | 34.04 % | 45.69 % | 57.13 % |
| 1.5 ATR | 6.834 % | 183.3033 | 2.11 % | 10.47 % | 17.34 % | 26.57 % | 39.19 % | 52.51 % |
| 2.0 ATR | 9.113 % | 178.821 | 0.7 % | 3.93 % | 9.38 % | 15.76 % | 28.43 % | 39.08 % |
| 2.5 ATR | 11.391 % | 174.3388 | 0.1 % | 1.51 % | 3.43 % | 9.29 % | 18.68 % | 29.03 % |
| 3.0 ATR | 13.669 % | 169.8565 | 0.0 % | 0.6 % | 1.61 % | 4.85 % | 12.18 % | 21.64 % |
| 4.0 ATR | 18.225 % | 160.8921 | 0.0 % | 0.0 % | 0.3 % | 1.41 % | 4.57 % | 11.69 % |
| 6.0 ATR | 27.338 % | 142.9631 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.51 % | 3.59 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.36 ATR | 0.41 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 0.97 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.61 ATR | 0.79 ATR | 0.96 ATR | 1.10 ATR | 1.54 ATR | 1.92 ATR |
| **3 s.** | 0.29 ATR | 0.66 ATR | 0.74 ATR | 0.99 ATR | 1.20 ATR | 1.39 ATR | 1.96 ATR | 2.37 ATR |
| **5 s.** | 0.40 ATR | 0.86 ATR | 0.97 ATR | 1.28 ATR | 1.57 ATR | 1.80 ATR | 2.44 ATR | 2.98 ATR |
| **10 s.** | 0.56 ATR | 1.14 ATR | 1.28 ATR | 1.79 ATR | 2.18 ATR | 2.43 ATR | 3.29 ATR | 3.94 ATR |
| **20 s.** | 0.76 ATR | 1.59 ATR | 1.78 ATR | 2.30 ATR | 2.77 ATR | 3.17 ATR | 4.42 ATR | 5.65 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.411–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.278 %, prix 192.268), p(touche) 36.22 % (en stress 81.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.607–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.417 %, prix 190.0271), p(touche) 35.05 % (en stress 94.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.739–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.417 %, prix 190.0271), p(touche) 44.35 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 45.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.97–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.556 %, prix 187.7861), p(touche) 43.64 % (en stress 100.0 %)  ✅ optimum identifie (86.6 % des re-echantillons)
- **10 seance(s)** : plage utile 1.277–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (6.834 %, prix 183.3041), p(touche) 39.19 % (en stress 100.0 %)  ✅ optimum identifie (85.9 % des re-echantillons)
- **20 seance(s)** : plage utile 1.78–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (13.669 %, prix 169.8562), p(touche) 21.64 % (en stress 94.9 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (96.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.055 | EV/share : $0.493 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 42 % | T2 16 % | T3 7 %
- Kelly (position) : f* 0.051 | ¼-Kelly 0.013 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 23.0 | bear 5.2 | side 71.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 351.0 (= 2 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.421% → cible +2.288% / stop −2.5%, p_fill 89%, n_eff≈92.7) : P(cible|rempli) **39%** · **EV/risk +0.073** (×p_fill ; si rempli +0.21% du capital)
  - **swing** (entrée dip −0.924% → cible +5.142% / stop −4.599%, p_fill 79%, n_eff≈92.4) : P(cible|rempli) **48%** · **EV/risk +0.144** (×p_fill ; si rempli +0.84% du capital)
  - **deep** (entrée dip −1.425% → cible +7.308% / stop −6.933%, p_fill 81%, n_eff≈91.6) : P(cible|rempli) **43%** · **EV/risk +0.109** (×p_fill ; si rempli +0.93% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→73% · +2.0%→44% · +3.0%→24% · +5.0%→9% · +8.0%→2%
- Range intraday médian 3.72% (p90 6.89%) · excursion haute méd. +1.85% / basse méd. −1.67%
- Profil de vol intra : ouverture 2.899% vs midi 0.725% vs clôture 0.809% _(ouverture ~4.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (157 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 79% · range 20% · trend ↑1%/↓0% ; spike-down 55% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.112 ; neutre — autocorr -0.02)_ ; drift intra méd. 0.326% ; recovery-V 29%
- **σ réalisé intraday** 2.336% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 40% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 189.3098 (VA 188.5023–190.9247 ; dernier close 188.79)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 44% · rebond 70% · **stop −3.61%** sous le fill (sous le bruit) · cible +1.61% · R/R 0.45 (high win-rate)
- Gaps overnight (n=156) : méd. -0.06% · baisse 51% (gap-down >1% 29% · >2% 6%)
- Excursion ouverture 5min (n=157) : bas méd −0.81% (p90 −1.9%) · haut méd +0.74% · range méd 1.73%
- Excursion ouverture 15min (n=157) : bas méd −1.0% (p90 −2.43%) · haut méd +0.97% · range méd 2.2%
- Excursion ouverture 30min (n=157) : bas méd −1.11% (p90 −2.9%) · haut méd +1.17% · range méd 2.56%
- Excursion ouverture 60min (n=157) : bas méd −1.33% (p90 −3.06%) · haut méd +1.29% · range méd 2.76%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 188.75 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 75% (117/156) · gap 38% · délai 0.0min · rebond 61% (67/117) (MFE +1.35%)
   - −1.0% : fill 30min 55% · séance 62% (103/156) · gap 29% · délai 0.0min · rebond 66% (60/103) (MFE +1.43%)
   - −1.5% : fill 30min 42% · séance 50% (86/156) · gap 17% · délai 0.1min · rebond 64% (52/86) (MFE +1.42%)
   - −2.0% : fill 30min 35% · séance 44% (77/156) · gap 6% · délai 1.5min · rebond 70% (49/77) (MFE +1.61%)
   - −3.0% : fill 30min 16% · séance 23% (50/156) · gap 3% · délai 6.1min · rebond 53% (23/50) (MFE +1.19%)
   - −4.0% : fill 30min 10% · séance 15% (34/156) · gap 2% · délai 15.4min · rebond 52% (16/34) (MFE +1.04%)
   - −5.0% : fill 30min 4% · séance 10% (23/156) · gap 0% · délai 45.3min · rebond 48% (12/23) (MFE +0.93%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.48% (p90 −1.9%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.69% (p90 −1.84%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.56% (p90 −1.57%) → stop au-delà de −1.02% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=515 jambes) : jambe baissière méd −1.06% (p90 −2.33%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 91% (70/75) · rebond 63% (41/70)
      · −2.0% : fill 75% (57/75) · rebond 72% (36/57)
      · −3.0% : fill 42% (38/75) · rebond 52% (18/38)
      · −4.0% : fill 29% (27/75) · rebond 54% (13/27)
      · −5.0% : fill 19% (19/75) · rebond 53% (11/19)
   - **flat** (23 séances) :
      · −1.0% : fill 78% (19/23) · rebond 58% (9/19)
      · −2.0% : fill 45% (13/23) · rebond 61% (8/13)
      · −3.0% : fill 24% (9/23) · rebond 54% (4/9)
      · −4.0% : fill 15% (6/23) · rebond 43% (3/6)
      · −5.0% : fill 8% (3/23) · rebond 13% (1/3)
   - **gap-up** (58 séances) :
      · −1.0% : fill 25% (14/58) · rebond 85% (10/14)
      · −2.0% : fill 12% (7/58) · rebond 67% (5/7)
      · −3.0% : fill 3% (3/58) · rebond 66% (1/3)
      · −4.0% : fill 1% (1/58) · rebond 0% (0/1)
      · −5.0% : fill 1% (1/58) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=157) : 51% en base · 71% si les 15 1res min sont vertes (80 cas) · 29% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=157) : COUDE à **1:41** → P(séance verte=clôture>ouverture) 86% si début vert vs 15% si rouge (base 51% · écart 70 pts) ; prédictivité sature ensuite (plafond brut 230min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **86%** · continue >prix actuel 55% ; creux résiduel méd -0.8% (q20 -1.44%) → **SL/trailing à −1.44%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.07% / q75 +2.11% → **scale +1.07% / runner +2.11%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **15%** (continue à baisser 51%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.53%** (au-delà de la MAE q10 -2.53%), cible rebond +1.05% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=157) : retour [-2.87% .. +3.73%] · haut q95 +4.0% · bas q05 -3.52%
   - 60min (n=157) : retour [-3.01% .. +3.93%] · haut q95 +4.71% · bas q05 -3.64%
   - 2h (n=157) : retour [-3.61% .. +5.08%] · haut q95 +5.27% · bas q05 -4.46%
   - 4h (n=157) : retour [-3.99% .. +5.64%] · haut q95 +6.27% · bas q05 -5.01%
   - 6h (n=157) : retour [-4.0% .. +5.46%] · haut q95 +6.81% · bas q05 -5.37%
   - session (n=157) : retour [-3.98% .. +4.77%] · haut q95 +6.81% · bas q05 -5.37%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.7% des séances sont trend-up (mild 1.3% / strong 4.5%) · base = 9 séances trend-up (n_eff 7.0)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **26%**. Lecture précoce 30 min : signature présente → 13% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.91% (p75 1.39% / p90 1.52%) · ~2.0 replis/séance, durée méd 77.38 min. P(nouveau plus-haut après repli) :
   - −0.5% → **78%** (reprise méd 47.34 min, n=25)
   - −1.0% → **51%** (reprise méd 65.0 min, n=11)
   - −1.5% → **18%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.52%** (p90, défaut prudent ; serré/agressif −1.39%) ; extension open→close méd +4.55% (q75 +7.54% / q95 +12.13%), MFE méd +6.21% / q90 +12.4%
   - Échelle scale-out : +6.21% (33%) / +8.19% (33%) / +12.4% (34%)
- **DÉSARMER** : repli > **−1.52%** depuis le plus-haut = décay → P(retournement) **65%** (préavis méd 99.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.4% : P(retournement après) 0% (mèche méd 1.36%)
- **CONTEXTE** : la dernière heure tient les gains 53% du temps (retour médian dernière heure +0.12%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.62 · part idiosyncratique 0.38
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 55.4  _(momentum haussier)_
- **ADX** : 25.0  _(tendance etablie)_
- **MACD** : hist -1.187  _(pas de croisement recent)_
- **BB** : %B 0.54 · largeur 15.4%
- **ATR** : 8.96 (85.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.001  _(neutre)_
- **Vol ratio** : 0.73  _(volume normal)_
- **Choppiness** : 56.2  _(transition)_
- **MA** : MA20 195.51 · MA50 184.75 · MA200 153.15  _(prix > MA20)_
- **Dist MA** : MA20 +0.6% · MA50 +6.5% · MA200 +28.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (777270 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
