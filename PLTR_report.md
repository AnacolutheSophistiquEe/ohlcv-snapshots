# PLTR

**Generated** : 2026-10-13T22:03:57.453924+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 10/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $208.67  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot $208.67 (+3.9% vs entrée) · entrée $200.89 · stop $194.91 · T1 $208.63 · R/R 1.29  
> ↳ ¼-Kelly 0.012 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : triple_bullish (score 3)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 10/10 élevée alors que : RSI 76.8 > 70 (surachat) ; %B 0.96 (collé à la bande haute) ; extension extrême (≥3×ATR, confluence MA20/50) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 10/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-13 : 208.67 · ATR Wilder 6.56 (3.14 %)_
- **Swing** : plage **201.07 → 195.38** (-3.64 % a -6.37 % sous la cloture, 0.87 ATR) — touchee 50 % → 30 % du temps en 10 seances ; aucun support reel dans la plage. stop INDICATIF 191.4 (-2.04 % sous le bas ; sous le support 194.68-194.93 (- 0,5 ATR)).
- **Deep** : plage **195.38 → 183.45** (-6.37 % a -12.08 % sous la cloture, 1.82 ATR) — touchee 42 % → 15 % du temps en 20 seances ; supports reels dans la plage : 194.68-194.93 (B) ; 188.2-190.39 (B) ; 184.81-187.62 (A). stop INDICATIF 176.9 (-3.57 % sous le bas ; sous le support 180.18-182.44 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (0.65 ATR sous le plus haut 20 s., RSI(2) 90.2 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 194.68-194.93 (B, -6.58 %) ; 188.2-190.39 (B, -8.76 %) ; 184.81-187.62 (A, -10.09 %) ; 180.18-182.44 (B, -12.57 %) ; 174.29-176.5 (B, -15.42 %) ; 168.9-172.0 (B, -17.57 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.71 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (6.59 %)** : le gap seul le franchit 0.878 % des séances (11 fois sur 1253).
   - exécution **3.355 pt plus bas** dans le cas TYPIQUE (médiane), 8.082 au p90, **11.342 au pire**
   - perte réelle **10.642 %** en moyenne _(tirée par la queue)_, jusqu'à **17.932 %** — au lieu des 6.59 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0356 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 11 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.861 % | p01 -6.139 % | pire -17.932 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2231** [0.166 ; 0.2894] _(largeur 12.3 pt, n_eff 173.1)_
   - swing : **0.4993** [0.4468 ; 0.5518] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4966** [0.4441 ; 0.5492] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (26.7 pt), swing (30.4 pt), deep (30.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.14 %** | CVaR **-8.41 %** | vol 4.26 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.31 % vs -13.73 % si l'on extrapolait par √5 _(rapport 0.969 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6882** (β de hausse 1.4209, asymétrie 1.1881) vs IWM — 606 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.746× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 204.186 sur atr_grid (0.75 ATR, 2.149 %) — p(stop avant cible) 0.7115 [0.66 ; 0.76], R/R 2.86, perte reelle 2.233 % (gap inclus), CVaR 3.326 %, EV 0.2082 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.4236 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.712, borne haute 0.757 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.298 %) — p(stop avant cible) 0.5231 [0.47 ; 0.58], R/R 1.467, perte reelle 4.355 % (gap inclus), EV 0.4942 % — **REFUSE**
      - refuse : p_stop_first 0.523, borne haute 0.575 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 2.47 ATR (stop 9.022 %) — p(stop avant cible) 0.2721 [0.23 ; 0.32], R/R 0.702, perte reelle 9.103 % (gap inclus), EV 0.8667 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 3.58 ATR (stop 12.205 %) — p(stop avant cible) 0.1701 [0.13 ; 0.21], R/R 0.516, perte reelle 12.389 % (gap inclus), EV 0.8206 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.83 % > budget 12.00 %
   - ⚪ swing_based a 4.19 ATR (stop 13.961 %) — p(stop avant cible) 0.1239 [0.09 ; 0.16], R/R 0.449, perte reelle 14.219 % (gap inclus), EV 0.7476 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.60 % > budget 12.00 %
   - 🔴 support a 15.18 ATR (stop 45.458 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.141, perte reelle 45.458 % (gap inclus), EV 1.1633 % — **REFUSE**
      - refuse : R/R 0.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.33 % > budget 12.00 %
      - ⚠ support DETECTE a 10.59 ATR du spot — compartiment >=6, mesure a 45.1 % de casse (IC clusterise [0.312 ; 0.590] sur 51 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🔴 support a 17.11 ATR (stop 50.979 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.125, perte reelle 50.979 % (gap inclus), EV 1.1633 % — **REFUSE**
      - refuse : R/R 0.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.33 % > budget 12.00 %
      - ⚠ support DETECTE a 17.11 ATR du spot — compartiment >=6, mesure a 45.1 % de casse (IC clusterise [0.312 ; 0.590] sur 51 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_grid a 0.25 ATR (stop 0.716 %) — p(stop avant cible) 0.9011 [0.87 ; 0.93], R/R 8.63, perte reelle 0.74 % (gap inclus), EV -0.0367 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 8.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.901, borne haute 0.929 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.04 %) : P(cible) 9.9 % x 6.39 % + P(rien) 0.0 % x 1.56 % ne couvrent pas P(stop) 90.1 % x 0.74 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 1.433 %) — p(stop avant cible) 0.7925 [0.75 ; 0.83], R/R 4.354, perte reelle 1.467 % (gap inclus), EV 0.1614 % — **REFUSE**
      - refuse : p_stop_first 0.792, borne haute 0.833 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 2.149 %) — p(stop avant cible) 0.7115 [0.66 ; 0.76], R/R 2.86, perte reelle 2.233 % (gap inclus), EV 0.2082 % — **REFUSE**
      - refuse : p_stop_first 0.712, borne haute 0.757 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.0 ATR (stop 2.865 %) — p(stop avant cible) 0.6333 [0.58 ; 0.68], R/R 2.158, perte reelle 2.959 % (gap inclus), EV 0.3645 % — **REFUSE**
      - refuse : p_stop_first 0.633, borne haute 0.683 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.25 ATR (stop 3.581 %) — p(stop avant cible) 0.5787 [0.53 ; 0.63], R/R 1.75, perte reelle 3.65 % (gap inclus), EV 0.3993 % — **REFUSE**
      - refuse : p_stop_first 0.579, borne haute 0.630 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.75 ATR (stop 5.014 %) — p(stop avant cible) 0.4578 [0.41 ; 0.51], R/R 1.256, perte reelle 5.086 % (gap inclus), EV 0.7333 % — **REFUSE**
      - refuse : R/R 1.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 5.73 %) — p(stop avant cible) 0.424 [0.37 ; 0.48], R/R 1.103, perte reelle 5.791 % (gap inclus), EV 0.7399 % — **REFUSE**
      - refuse : R/R 1.10 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 2.47 ATR (stop 7.927 %) — p(stop avant cible) 0.3172 [0.27 ; 0.37], R/R 0.797, perte reelle 8.018 % (gap inclus), EV 0.9165 % — **REFUSE**
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 8.595 %) — p(stop avant cible) 0.2819 [0.24 ; 0.33], R/R 0.735, perte reelle 8.694 % (gap inclus), EV 0.928 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 grid_snapped a 3.58 ATR (stop 11.11 %) — p(stop avant cible) 0.2043 [0.16 ; 0.25], R/R 0.567, perte reelle 11.256 % (gap inclus), EV 0.7363 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 4.19 ATR (stop 12.867 %) — p(stop avant cible) 0.1567 [0.12 ; 0.20], R/R 0.489, perte reelle 13.07 % (gap inclus), EV 0.7886 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.50 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 14.326 %) — p(stop avant cible) 0.1217 [0.09 ; 0.16], R/R 0.436, perte reelle 14.633 % (gap inclus), EV 0.7343 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.07 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 15.758 %) — p(stop avant cible) 0.0996 [0.07 ; 0.13], R/R 0.4, perte reelle 15.964 % (gap inclus), EV 0.806 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.17 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 17.191 %) — p(stop avant cible) 0.09 [0.06 ; 0.12], R/R 0.368, perte reelle 17.364 % (gap inclus), EV 0.75 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.50 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 18.623 %) — p(stop avant cible) 0.071 [0.05 ; 0.10], R/R 0.341, perte reelle 18.751 % (gap inclus), EV 0.7776 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.80 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 20.056 %) — p(stop avant cible) 0.0422 [0.02 ; 0.07], R/R 0.316, perte reelle 20.243 % (gap inclus), EV 0.9378 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.79 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 21.489 %) — p(stop avant cible) 0.0282 [0.01 ; 0.05], R/R 0.293, perte reelle 21.771 % (gap inclus), EV 1.018 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.59 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 22.921 %) — p(stop avant cible) 0.0203 [0.01 ; 0.04], R/R 0.275, perte reelle 23.236 % (gap inclus), EV 1.0457 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.16 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 208.67, ATR14 5.9787 (2.865 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.361 ATR = 1.034 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.143 % | 208.3711 | 92.95 % | 95.46 % | 96.27 % | 97.07 % | 98.27 % | 98.67 % |
| 0.1 ATR | 0.287 % | 208.0721 | 84.99 % | 89.62 % | 91.52 % | 93.73 % | 95.22 % | 96.41 % |
| 0.15 ATR | 0.43 % | 207.7732 | 77.24 % | 83.97 % | 86.28 % | 90.09 % | 92.58 % | 94.25 % |
| 0.2 ATR | 0.573 % | 207.4743 | 69.18 % | 78.43 % | 81.94 % | 86.55 % | 90.35 % | 92.51 % |
| 0.25 ATR | 0.716 % | 207.1753 | 62.34 % | 73.59 % | 77.6 % | 82.91 % | 87.8 % | 90.86 % |
| 0.35 ATR | 1.003 % | 206.5775 | 51.06 % | 65.42 % | 71.04 % | 78.06 % | 83.74 % | 87.78 % |
| 0.5 ATR | 1.433 % | 205.6806 | 36.05 % | 52.52 % | 59.43 % | 68.76 % | 77.54 % | 83.06 % |
| 0.75 ATR | 2.149 % | 204.186 | 19.44 % | 34.98 % | 44.3 % | 55.11 % | 66.36 % | 75.87 % |
| 1.0 ATR | 2.865 % | 202.6913 | 8.86 % | 22.68 % | 32.29 % | 43.68 % | 56.0 % | 66.84 % |
| 1.25 ATR | 3.581 % | 201.1966 | 4.33 % | 15.22 % | 23.11 % | 33.97 % | 46.14 % | 57.8 % |
| 1.5 ATR | 4.298 % | 199.7019 | 2.01 % | 10.38 % | 17.26 % | 26.49 % | 39.63 % | 53.29 % |
| 2.0 ATR | 5.73 % | 196.7126 | 0.6 % | 3.73 % | 9.38 % | 15.77 % | 28.96 % | 39.84 % |
| 2.5 ATR | 7.163 % | 193.7232 | 0.1 % | 1.51 % | 3.33 % | 9.3 % | 19.31 % | 29.77 % |
| 3.0 ATR | 8.595 % | 190.7339 | 0.0 % | 0.6 % | 1.51 % | 4.75 % | 12.8 % | 22.28 % |
| 4.0 ATR | 11.461 % | 184.7552 | 0.0 % | 0.0 % | 0.3 % | 1.52 % | 4.67 % | 11.81 % |
| 6.0 ATR | 17.191 % | 172.7978 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.51 % | 3.59 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.36 ATR | 0.41 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 0.97 ATR | 1.21 ATR |
| **2 s.** | 0.23 ATR | 0.54 ATR | 0.61 ATR | 0.79 ATR | 0.95 ATR | 1.09 ATR | 1.53 ATR | 1.91 ATR |
| **3 s.** | 0.29 ATR | 0.66 ATR | 0.74 ATR | 0.98 ATR | 1.20 ATR | 1.38 ATR | 1.96 ATR | 2.36 ATR |
| **5 s.** | 0.40 ATR | 0.86 ATR | 0.97 ATR | 1.28 ATR | 1.57 ATR | 1.80 ATR | 2.45 ATR | 2.97 ATR |
| **10 s.** | 0.56 ATR | 1.15 ATR | 1.29 ATR | 1.81 ATR | 2.21 ATR | 2.46 ATR | 3.34 ATR | 3.96 ATR |
| **20 s.** | 0.77 ATR | 1.62 ATR | 1.81 ATR | 2.34 ATR | 2.82 ATR | 3.22 ATR | 4.44 ATR | 5.66 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.411–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.433 %, prix 205.6798), p(touche) 36.05 % (en stress 81.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.607–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.149 %, prix 204.1857), p(touche) 34.98 % (en stress 94.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.738–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.149 %, prix 204.1857), p(touche) 44.3 % (en stress 98.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.971–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.865 %, prix 202.6916), p(touche) 43.68 % (en stress 100.0 %)  ✅ optimum identifie (83.4 % des re-echantillons)
- **10 seance(s)** : plage utile 1.294–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (4.298 %, prix 199.7014), p(touche) 39.63 % (en stress 100.0 %)  ✅ optimum identifie (87.9 % des re-echantillons)
- **20 seance(s)** : plage utile 1.808–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (8.595 %, prix 190.7348), p(touche) 22.28 % (en stress 94.9 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (96.5 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.072 | EV/share : $0.432 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 26 % | T3 13 %
- Kelly (position) : f* 0.048 | ¼-Kelly 0.012 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 52.3 | bear 40.4 | side 7.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 559.0 (= 3 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.692% → cible +1.705% / stop −2.5%, p_fill 48%, n_eff≈51.6) : P(cible|rempli) **51%** · **EV/risk +0.046** (×p_fill ; si rempli +0.24% du capital)
  - **swing** (entrée dip −3.725% → cible +3.854% / stop −2.976%, p_fill 31%, n_eff≈38.7) : P(cible|rempli) **37%** · **EV/risk -0.022** (×p_fill ; si rempli -0.21% du capital)
  - **deep** (entrée dip −5.762% → cible +6.096% / stop −4.561%, p_fill 32%, n_eff≈37.8) : P(cible|rempli) **45%** · **EV/risk +0.033** (×p_fill ; si rempli +0.46% du capital)
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

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.63 · part idiosyncratique 0.37
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 76.8  _(surachat)_
- **ADX** : 37.0  _(tendance etablie)_
- **MACD** : hist 1.639  _(pas de croisement recent)_
- **BB** : %B 0.96 · largeur 20.8%
- **ATR** : 5.98 (11.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.237  _(accumulation)_
- **Vol ratio** : 0.79  _(volume normal)_
- **Choppiness** : 41.3  _(transition)_
- **MA** : MA20 190.59 · MA50 180.36 · MA200 152.48  _(prix > MA20)_
- **Dist MA** : MA20 +9.5% · MA50 +15.7% · MA200 +36.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (902099 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
