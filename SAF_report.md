# SAF

**Generated** : 2026-10-05T00:10:05.174605+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · €330.10  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 3/121 fenêtres (p_fill pondéré 2 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot €330.10 (+6.1% vs entrée) · entrée €311.04 · stop €303.16 · T1 €319.86 · R/R 1.12  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -36 % hors [0,100] (R² max 0.89). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €309.80–€312.29 (mid €311.04)
- Spot actuel : €330.10 (+6.1% au-dessus de la zone — repli à attendre)
- Stop : €303.16 (plancher anti-bruit (R/R<2) ; -2.53 % depuis l'entree)
- Targets : T1 €319.86 · R/R 1.12 | T2 €328.67 · R/R 2.24 | T3 €337.49 · R/R 3.36
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €303.16


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.62 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (8.16 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1280).
   - exécution **1.826 pt plus bas** dans le cas TYPIQUE (médiane), 1.826 au p90, **1.826 au pire**
   - perte réelle **9.986 %** en moyenne _(tirée par la queue)_, jusqu'à **9.986 %** — au lieu des 8.16 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0014 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.377 % | p01 -2.356 % | pire -9.986 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0** [0.0 ; 0.0144] _(largeur 1.4 pt, n_eff 173.1)_
   - swing : **0.4205** [0.3693 ; 0.473] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.3665** [0.317 ; 0.4182] _(largeur 10.1 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 15.8 observations effectives », dont la borne haute a 95 % vaut environ 19.0 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (44.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-3.21 %** | CVaR **-4.01 %** | vol 2.08 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 1.33 % contre 2.17 % aujourd'hui, rapport 0.61)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.66 % vs -6.06 % si l'on extrapolait par √5 _(rapport 0.934 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3857** (β de hausse 1.3517, asymétrie 1.0252) vs FCHI — 619 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 320.2429 sur atr_grid (1.25 ATR, 2.986 %) — p(stop avant cible) 0.4977 [0.45 ; 0.55], R/R 3.058, perte reelle 3.089 % (gap inclus), CVaR 3.928 %, EV 0.7128 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.2157 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 11.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.498, borne haute 0.550 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 3.583 %) — p(stop avant cible) 0.4132 [0.36 ; 0.47], R/R 2.564, perte reelle 3.685 % (gap inclus), EV 0.8398 % — **REFUSE**
      - refuse : cible atteinte seulement 13.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ swing_based a 1.62 ATR (stop 5.213 %) — p(stop avant cible) 0.262 [0.22 ; 0.31], R/R 1.797, perte reelle 5.258 % (gap inclus), EV 1.0648 % — **REFUSE**
      - refuse : R/R 1.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 4.49 ATR (stop 12.079 %) — p(stop avant cible) 0.044 [0.03 ; 0.07], R/R 0.754, perte reelle 12.535 % (gap inclus), EV 0.8325 % — **REFUSE**
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.18 % > budget 12.00 %
   - 🟢 support a 8.93 ATR (stop 22.675 %) — p(stop avant cible) 0.0026 [0.00 ; 0.01], R/R 0.417, perte reelle 22.675 % (gap inclus), EV 0.8421 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 0.25 ATR (stop 0.597 %) — p(stop avant cible) 0.8906 [0.85 ; 0.92], R/R 15.236, perte reelle 0.62 % (gap inclus), EV 0.1374 % — **REFUSE**
      - refuse : cible atteinte seulement 4.4 % du temps (< 15 %) meme a 10 seances : le R/R de 15.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.891, borne haute 0.920 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 1.194 %) — p(stop avant cible) 0.7733 [0.73 ; 0.81], R/R 7.584, perte reelle 1.246 % (gap inclus), EV 0.314 % — **REFUSE**
      - refuse : cible atteinte seulement 6.4 % du temps (< 15 %) meme a 10 seances : le R/R de 7.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.773, borne haute 0.815 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 1.792 %) — p(stop avant cible) 0.6773 [0.63 ; 0.72], R/R 5.065, perte reelle 1.865 % (gap inclus), EV 0.4164 % — **REFUSE**
      - refuse : cible atteinte seulement 8.5 % du temps (< 15 %) meme a 10 seances : le R/R de 5.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.677, borne haute 0.725 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 2.389 %) — p(stop avant cible) 0.5977 [0.55 ; 0.65], R/R 3.798, perte reelle 2.487 % (gap inclus), EV 0.5126 % — **REFUSE**
      - refuse : cible atteinte seulement 10.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.598, borne haute 0.648 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.25 ATR (stop 2.986 %) — p(stop avant cible) 0.4977 [0.45 ; 0.55], R/R 3.058, perte reelle 3.089 % (gap inclus), EV 0.7128 % — **REFUSE**
      - refuse : cible atteinte seulement 11.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.498, borne haute 0.550 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ grid_snapped a 1.62 ATR (stop 4.587 %) — p(stop avant cible) 0.3178 [0.27 ; 0.37], R/R 2.025, perte reelle 4.665 % (gap inclus), EV 0.9607 % — **REFUSE**
      - refuse : cible atteinte seulement 14.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 5.972 %) — p(stop avant cible) 0.2324 [0.19 ; 0.28], R/R 1.561, perte reelle 6.052 % (gap inclus), EV 1.0669 % — **REFUSE**
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 6.569 %) — p(stop avant cible) 0.1896 [0.15 ; 0.23], R/R 1.423, perte reelle 6.637 % (gap inclus), EV 0.9987 % — **REFUSE**
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 7.167 %) — p(stop avant cible) 0.15 [0.12 ; 0.19], R/R 1.302, perte reelle 7.255 % (gap inclus), EV 0.9818 % — **REFUSE**
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 8.361 %) — p(stop avant cible) 0.1089 [0.08 ; 0.14], R/R 1.107, perte reelle 8.535 % (gap inclus), EV 0.9229 % — **REFUSE**
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 9.556 %) — p(stop avant cible) 0.0767 [0.05 ; 0.11], R/R 0.964, perte reelle 9.804 % (gap inclus), EV 0.8756 % — **REFUSE**
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 4.49 ATR (stop 11.453 %) — p(stop avant cible) 0.0549 [0.03 ; 0.08], R/R 0.804, perte reelle 11.757 % (gap inclus), EV 0.8216 % — **REFUSE**
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 5.5 ATR (stop 13.139 %) — p(stop avant cible) 0.0299 [0.02 ; 0.05], R/R 0.674, perte reelle 14.007 % (gap inclus), EV 0.8111 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.59 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 14.333 %) — p(stop avant cible) 0.0175 [0.01 ; 0.04], R/R 0.585, perte reelle 16.162 % (gap inclus), EV 0.8001 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.82 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 15.528 %) — p(stop avant cible) 0.0087 [0.00 ; 0.02], R/R 0.52, perte reelle 18.165 % (gap inclus), EV 0.8117 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.58 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 16.722 %) — p(stop avant cible) 0.006 [0.00 ; 0.02], R/R 0.483, perte reelle 19.569 % (gap inclus), EV 0.8222 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.38 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 17.917 %) — p(stop avant cible) 0.0053 [0.00 ; 0.02], R/R 0.47, perte reelle 20.091 % (gap inclus), EV 0.8274 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.29 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 19.111 %) — p(stop avant cible) 0.0046 [0.00 ; 0.02], R/R 0.461, perte reelle 20.504 % (gap inclus), EV 0.8336 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.17 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 330.1, ATR14 7.8857 (2.389 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.344 ATR = 0.822 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.119 % | 329.7057 | 89.22 % | 92.54 % | 93.71 % | 95.67 % | 96.34 % | 97.1 % |
| 0.1 ATR | 0.239 % | 329.3114 | 81.37 % | 87.14 % | 89.1 % | 91.34 % | 93.47 % | 94.81 % |
| 0.15 ATR | 0.358 % | 328.9171 | 75.0 % | 83.22 % | 86.15 % | 88.58 % | 91.3 % | 92.71 % |
| 0.2 ATR | 0.478 % | 328.5229 | 68.04 % | 78.02 % | 82.51 % | 85.24 % | 88.92 % | 91.01 % |
| 0.25 ATR | 0.597 % | 328.1286 | 60.98 % | 73.41 % | 78.88 % | 83.17 % | 87.64 % | 90.11 % |
| 0.35 ATR | 0.836 % | 327.34 | 49.31 % | 63.3 % | 69.74 % | 76.87 % | 82.69 % | 87.11 % |
| 0.5 ATR | 1.194 % | 326.1571 | 35.2 % | 51.72 % | 59.04 % | 68.41 % | 75.96 % | 81.62 % |
| 0.75 ATR | 1.792 % | 324.1857 | 20.59 % | 35.33 % | 42.63 % | 52.95 % | 63.2 % | 71.13 % |
| 1.0 ATR | 2.389 % | 322.2143 | 9.8 % | 23.55 % | 32.22 % | 41.93 % | 53.71 % | 61.84 % |
| 1.25 ATR | 2.986 % | 320.2429 | 4.41 % | 15.21 % | 23.67 % | 32.97 % | 46.19 % | 55.04 % |
| 1.5 ATR | 3.583 % | 318.2714 | 2.25 % | 9.91 % | 16.4 % | 24.7 % | 37.88 % | 47.05 % |
| 2.0 ATR | 4.778 % | 314.3286 | 0.98 % | 4.42 % | 7.47 % | 15.16 % | 26.71 % | 37.16 % |
| 2.5 ATR | 5.972 % | 310.3857 | 0.2 % | 1.47 % | 3.63 % | 8.56 % | 18.2 % | 28.47 % |
| 3.0 ATR | 7.167 % | 306.4429 | 0.0 % | 0.88 % | 2.06 % | 5.71 % | 12.07 % | 22.28 % |
| 4.0 ATR | 9.556 % | 298.5572 | 0.0 % | 0.2 % | 0.59 % | 1.08 % | 4.55 % | 10.89 % |
| 6.0 ATR | 14.333 % | 282.7857 | 0.0 % | 0.1 % | 0.2 % | 0.39 % | 1.09 % | 3.0 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.34 ATR | 0.40 ATR | 0.54 ATR | 0.68 ATR | 0.76 ATR | 0.99 ATR | 1.22 ATR |
| **2 s.** | 0.23 ATR | 0.53 ATR | 0.60 ATR | 0.80 ATR | 0.97 ATR | 1.11 ATR | 1.50 ATR | 1.95 ATR |
| **3 s.** | 0.29 ATR | 0.64 ATR | 0.71 ATR | 0.98 ATR | 1.21 ATR | 1.38 ATR | 1.86 ATR | 2.32 ATR |
| **5 s.** | 0.38 ATR | 0.82 ATR | 0.93 ATR | 1.25 ATR | 1.49 ATR | 1.75 ATR | 2.39 ATR | 3.15 ATR |
| **10 s.** | 0.52 ATR | 1.12 ATR | 1.29 ATR | 1.72 ATR | 2.10 ATR | 2.39 ATR | 3.27 ATR | 3.94 ATR |
| **20 s.** | 0.66 ATR | 1.41 ATR | 1.60 ATR | 2.24 ATR | 2.78 ATR | 3.20 ATR | 4.23 ATR | 5.49 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.396–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.603–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.792 %, prix 324.1846), p(touche) 35.33 % (en stress 86.27 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.714–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (1.792 %, prix 324.1846), p(touche) 42.63 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.93–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (2.389 %, prix 322.2139), p(touche) 41.93 % (en stress 98.04 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.286–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (3.583 %, prix 318.2725), p(touche) 37.88 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.604–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (4.778 %, prix 314.3278), p(touche) 37.16 % (en stress 99.01 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.008 | EV/share : €-0.059 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 15 % | T3 9 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 43.2 | bear 51.8 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 330.0 (= 1 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈60.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.62% → cible +1.227% / stop −8.0%, p_fill 13%, n_eff≈15.8) : P(cible|rempli) **36%** · **EV/risk +0.000** (×p_fill ; si rempli +0.01% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→70% · +1.0%→50% · +2.0%→24% · +3.0%→8% · +5.0%→2% · +8.0%→1%
- Range intraday médian 2.49% (p90 4.07%) · excursion haute méd. +0.98% / basse méd. −0.99%
- Profil de vol intra : ouverture 1.488% vs midi 0.546% vs clôture 0.685% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 40% · recovery-V 18%)_
- **Régime intraday** : **chop** _(efficiency 0.099 ; mean-reverting — autocorr -0.058)_ ; drift intra méd. -0.278% ; recovery-V 20%
- **σ réalisé intraday** 1.556% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 68% / whipsaw 39%
- POC intraday (dernière séance, temps-au-prix) : 332.2313 (VA 330.9188–333.8062 ; dernier close 330.1)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 23% · rebond 30% · **stop −1.38%** sous le fill (sous le bruit) · cible +0.71% · R/R 0.51 (high win-rate)
- Gaps overnight (n=159) : méd. 0.28% · baisse 36% (gap-down >1% 1% · >2% 0%)
- Excursion ouverture 5min (n=160) : bas méd −0.37% (p90 −1.37%) · haut méd +0.21% · range méd 0.8%
- Excursion ouverture 15min (n=160) : bas méd −0.37% (p90 −1.58%) · haut méd +0.37% · range méd 1.02%
- Excursion ouverture 30min (n=160) : bas méd −0.45% (p90 −1.67%) · haut méd +0.52% · range méd 1.11%
- Excursion ouverture 60min (n=160) : bas méd −0.61% (p90 −1.81%) · haut méd +0.57% · range méd 1.36%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 330.1 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 46% · séance 59% (92/159) · gap 8% · délai 1.0min · rebond 36% (35/92) (MFE +0.77%)
   - −1.0% : fill 30min 24% · séance 47% (74/159) · gap 1% · délai 30.6min · rebond 47% (36/74) (MFE +0.87%)
   - −1.5% : fill 30min 9% · séance 28% (46/159) · gap 0% · délai 80.2min · rebond 28% (18/46) (MFE +0.62%)
   - −2.0% : fill 30min 3% · séance 23% (38/159) · gap 0% · délai 218.5min · rebond 30% (14/38) (MFE +0.71%)
   - −3.0% : fill 30min 1% · séance 9% (16/159) · gap 0% · délai 398.1min · rebond 20% (6/16) (MFE +0.54%)
   - −4.0% : fill 30min 0% · séance 1% (4/159) · gap 0% · délai 282.8min · rebond 72% (3/4) (MFE +1.17%)
   - −5.0% : fill 30min 0% · séance 0% (1/159) · gap 0% · délai 457.9min · rebond 0% (0/1) (MFE +0.86%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.24% (p90 −0.91%) → stop au-delà de −0.64% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.23% (p90 −0.66%) → stop au-delà de −0.44% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.08% (p90 −0.99%) → stop au-delà de −0.67% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=198 jambes) : jambe baissière méd −1.05% (p90 −2.41%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (23 séances) :
      · −1.0% : fill 83% (19/23) · rebond 30% (6/19)
      · −2.0% : fill 53% (13/23) · rebond 24% (5/13)
      · −3.0% : fill 21% (6/23) · rebond 18% (2/6)
      · −4.0% : fill 5% (2/23) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/23) · rebond 0% (0/0)
   - **flat** (45 séances) :
      · −1.0% : fill 52% (24/45) · rebond 48% (13/24)
      · −2.0% : fill 29% (11/45) · rebond 23% (2/11)
      · −3.0% : fill 11% (4/45) · rebond 19% (1/4)
      · −4.0% : fill 0% (0/45) · rebond 0% (0/0)
      · −5.0% : fill 0% (0/45) · rebond 0% (0/0)
   - **gap-up** (91 séances) :
      · −1.0% : fill 32% (31/91) · rebond 60% (17/31)
      · −2.0% : fill 9% (14/91) · rebond 56% (7/14)
      · −3.0% : fill 4% (6/91) · rebond 27% (3/6)
      · −4.0% : fill 1% (2/91) · rebond 38% (1/2)
      · −5.0% : fill 0% (1/91) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 66% si les 15 1res min sont vertes (75 cas) · 27% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **35min** → P(séance verte=clôture>ouverture) 79% si début vert vs 20% si rouge (base 46% · écart 59 pts) ; prédictivité sature ensuite (plafond brut 34min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **79%** · continue >prix actuel 60% ; creux résiduel méd -0.73% (q20 -1.22%) → **SL/trailing à −1.22%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.0% / q75 +1.41% → **scale +1.0% / runner +1.41%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **20%** (continue à baisser 59%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.24%** (au-delà de la MAE q10 -2.24%), cible rebond +0.86% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.49% .. +1.27%] · haut q95 +1.76% · bas q05 -1.94%
   - 60min (n=160) : retour [-1.63% .. +1.69%] · haut q95 +1.9% · bas q05 -1.98%
   - 2h (n=160) : retour [-1.79% .. +1.94%] · haut q95 +2.35% · bas q05 -2.39%
   - 4h (n=160) : retour [-1.87% .. +1.93%] · haut q95 +2.53% · bas q05 -2.72%
   - 6h (n=160) : retour [-2.06% .. +2.31%] · haut q95 +2.78% · bas q05 -2.78%
   - session (n=160) : retour [-2.86% .. +2.04%] · haut q95 +2.99% · bas q05 -3.47%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.68%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.52 · part idiosyncratique 0.48
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 58.2  _(momentum haussier)_
- **ADX** : 13.0  _(pas de tendance nette)_
- **MACD** : hist 0.593  _(pas de croisement recent)_
- **BB** : %B 0.52 · largeur 6.2%
- **ATR** : 7.89 (47.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.203  _(distribution)_
- **Vol ratio** : 1.08  _(volume normal)_
- **Choppiness** : 64.2  _(marche en range (choppy))_
- **MA** : MA20 329.77 · MA50 340.2 · MA200 315.31  _(prix > MA20)_
- **Dist MA** : MA20 +0.1% · MA50 -3.0% · MA200 +4.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (837123 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
