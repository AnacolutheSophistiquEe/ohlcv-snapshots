# AL2SI

**Generated** : 2026-10-01T00:12:43.338830+00:00  
**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €27.94  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot €27.94 (+4.9% vs entrée) · entrée €26.63 · stop €24.83 · T1 €29.20 · R/R 1.43  
> ↳ ¼-Kelly 0.034 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -46 % hors [0,100] (R² max 0.92). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €26.39–€26.88 (mid €26.63)
- Spot actuel : €27.94 (+4.9% au-dessus de la zone — repli à attendre)
- Stop : €24.83 (plancher anti-bruit (R/R<2) ; -6.76 % depuis l'entree)
- Targets : T1 €29.20 · R/R 1.43 | T2 €31.22 · R/R 2.55 | T3 €33.24 · R/R 3.67
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €24.83


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.44 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (11.13 %)** : le gap seul le franchit 0.469 % des séances (6 fois sur 1280).
   - exécution **10.256 pt plus bas** dans le cas TYPIQUE (médiane), 21.511 au p90, **26.987 au pire**
   - perte réelle **22.515 %** en moyenne _(tirée par la queue)_, jusqu'à **38.117 %** — au lieu des 11.13 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0534 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.362 % | p01 -6.808 % | pire -38.117 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5769** [0.5025 ; 0.6487] _(largeur 14.6 pt, n_eff 173.1)_
   - swing : **0.4212** [0.37 ; 0.4737] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.3291** [0.2812 ; 0.3799] _(largeur 9.9 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : swing (26.4 pt), deep (26.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-7.23 %** | CVaR **-11.72 %** | vol 6.29 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 4.38 % contre 7.04 % aujourd'hui, rapport 0.62)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.76 % vs -13.9 % si l'on extrapolait par √5 _(rapport 1.062 ; < 1 = le √5 surestime)_
- **β de baisse : 1.2031** (β de hausse 0.9529, asymétrie 1.2626) vs FCHI — 619 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.845× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 27.4889 sur atr_grid (0.25 ATR, 1.614 %) — p(stop avant cible) 0.8683 [0.83 ; 0.90], R/R 10.903, perte reelle 1.739 % (gap inclus), CVaR 3.788 %, EV 0.637 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.1936 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 10.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.868, borne haute 0.901 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 3.79 % > budget 3.00 %
- Budget de queue : **3.0 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.171 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 44.7 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
   - ⚠ budget **borne** (brut 2.7 %) : les bornes sont un choix declare, pas une mesure.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 1.06 ATR (stop 9.897 %) — p(stop avant cible) 0.3765 [0.33 ; 0.43], R/R 1.642, perte reelle 11.549 % (gap inclus), EV 2.3518 % — **REFUSE**
      - refuse : R/R 1.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.31 % > budget 3.00 %
   - 🟢 support a 1.63 ATR (stop 13.545 %) — p(stop avant cible) 0.2544 [0.21 ; 0.30], R/R 1.116, perte reelle 16.985 % (gap inclus), EV 2.3851 % — **REFUSE**
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.97 % > budget 3.00 %
   - 🟢 support a 2.96 ATR (stop 22.135 %) — p(stop avant cible) 0.1353 [0.10 ; 0.17], R/R 0.66, perte reelle 28.718 % (gap inclus), EV 1.8589 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.66 % > budget 3.00 %
   - 🟢 support a 4.35 ATR (stop 31.082 %) — p(stop avant cible) 0.0814 [0.06 ; 0.11], R/R 0.516, perte reelle 36.753 % (gap inclus), EV 2.0336 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.31 % > budget 3.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.614 %) — p(stop avant cible) 0.8683 [0.83 ; 0.90], R/R 10.903, perte reelle 1.739 % (gap inclus), EV 0.637 % — **REFUSE**
      - refuse : cible atteinte seulement 10.6 % du temps (< 15 %) meme a 10 seances : le R/R de 10.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.868, borne haute 0.901 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 3.79 % > budget 3.00 %
   - ⚪ atr_grid a 0.5 ATR (stop 3.229 %) — p(stop avant cible) 0.7555 [0.71 ; 0.80], R/R 5.468, perte reelle 3.468 % (gap inclus), EV 0.9945 % — **REFUSE**
      - refuse : p_stop_first 0.755, borne haute 0.798 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 6.84 % > budget 3.00 %
   - ⚪ atr_grid a 0.75 ATR (stop 4.843 %) — p(stop avant cible) 0.6719 [0.62 ; 0.72], R/R 3.702, perte reelle 5.122 % (gap inclus), EV 1.1778 % — **REFUSE**
      - refuse : p_stop_first 0.672, borne haute 0.720 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 8.59 % > budget 3.00 %
   - ⚪ grid_snapped a 1.06 ATR (stop 8.812 %) — p(stop avant cible) 0.4465 [0.39 ; 0.50], R/R 1.894, perte reelle 10.014 % (gap inclus), EV 1.8809 % — **REFUSE**
      - refuse : R/R 1.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.54 % > budget 3.00 %
   - 🟢 grid_snapped a 1.63 ATR (stop 12.46 %) — p(stop avant cible) 0.2789 [0.23 ; 0.33], R/R 1.282, perte reelle 14.796 % (gap inclus), EV 2.6841 % — **REFUSE**
      - refuse : R/R 1.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.49 % > budget 3.00 %
   - ⚪ atr_grid a 2.25 ATR (stop 14.53 %) — p(stop avant cible) 0.243 [0.20 ; 0.29], R/R 1.05, perte reelle 18.055 % (gap inclus), EV 2.2647 % — **REFUSE**
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.40 % > budget 3.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 16.144 %) — p(stop avant cible) 0.214 [0.17 ; 0.26], R/R 0.956, perte reelle 19.845 % (gap inclus), EV 2.2511 % — **REFUSE**
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.78 % > budget 3.00 %
   - 🟢 grid_snapped a 2.96 ATR (stop 21.05 %) — p(stop avant cible) 0.1447 [0.11 ; 0.18], R/R 0.686, perte reelle 27.638 % (gap inclus), EV 1.8594 % — **REFUSE**
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.66 % > budget 3.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 25.831 %) — p(stop avant cible) 0.0963 [0.07 ; 0.13], R/R 0.574, perte reelle 33.045 % (gap inclus), EV 2.1185 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.66 % > budget 3.00 %
   - 🟢 grid_snapped a 4.35 ATR (stop 29.997 %) — p(stop avant cible) 0.0837 [0.06 ; 0.12], R/R 0.526, perte reelle 36.021 % (gap inclus), EV 2.0447 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.07 % > budget 3.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 32.289 %) — p(stop avant cible) 0.0759 [0.05 ; 0.11], R/R 0.502, perte reelle 37.797 % (gap inclus), EV 2.0435 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.65 % > budget 3.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 35.517 %) — p(stop avant cible) 0.0541 [0.03 ; 0.08], R/R 0.459, perte reelle 41.337 % (gap inclus), EV 2.3651 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.81 % > budget 3.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 38.746 %) — p(stop avant cible) 0.0435 [0.03 ; 0.07], R/R 0.434, perte reelle 43.674 % (gap inclus), EV 2.4581 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.99 % > budget 3.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 41.975 %) — p(stop avant cible) 0.0353 [0.02 ; 0.06], R/R 0.418, perte reelle 45.364 % (gap inclus), EV 2.6808 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.23 % > budget 3.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 45.204 %) — p(stop avant cible) 0.031 [0.02 ; 0.05], R/R 0.408, perte reelle 46.52 % (gap inclus), EV 2.6967 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.93 % > budget 3.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 48.433 %) — p(stop avant cible) 0.031 [0.02 ; 0.05], R/R 0.38, perte reelle 49.958 % (gap inclus), EV 2.5902 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.06 % > budget 3.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 51.662 %) — p(stop avant cible) 0.031 [0.02 ; 0.05], R/R 0.333, perte reelle 56.946 % (gap inclus), EV 2.3735 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.40 % > budget 3.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 27.94, ATR14 1.8043 (6.458 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.399 ATR = 2.577 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.323 % | 27.8498 | 86.76 % | 90.38 % | 92.73 % | 94.19 % | 95.35 % | 96.9 % |
| 0.1 ATR | 0.646 % | 27.7596 | 82.16 % | 86.75 % | 89.98 % | 91.93 % | 93.87 % | 96.0 % |
| 0.15 ATR | 0.969 % | 27.6694 | 78.14 % | 83.02 % | 86.84 % | 88.68 % | 91.89 % | 94.81 % |
| 0.2 ATR | 1.292 % | 27.5791 | 72.35 % | 78.9 % | 83.01 % | 85.53 % | 89.52 % | 92.61 % |
| 0.25 ATR | 1.614 % | 27.4889 | 66.37 % | 74.29 % | 78.88 % | 82.19 % | 87.24 % | 91.01 % |
| 0.35 ATR | 2.26 % | 27.3085 | 54.61 % | 65.46 % | 70.73 % | 75.39 % | 82.29 % | 87.51 % |
| 0.5 ATR | 3.229 % | 27.0379 | 40.39 % | 53.58 % | 61.59 % | 68.41 % | 77.65 % | 85.01 % |
| 0.75 ATR | 4.843 % | 26.5868 | 22.35 % | 37.19 % | 47.05 % | 55.22 % | 66.67 % | 76.22 % |
| 1.0 ATR | 6.458 % | 26.1357 | 12.75 % | 24.73 % | 33.5 % | 43.8 % | 56.78 % | 67.73 % |
| 1.25 ATR | 8.072 % | 25.6846 | 7.45 % | 17.37 % | 24.36 % | 35.83 % | 49.75 % | 61.34 % |
| 1.5 ATR | 9.687 % | 25.2336 | 3.63 % | 11.19 % | 17.09 % | 28.25 % | 42.53 % | 54.85 % |
| 2.0 ATR | 12.915 % | 24.3314 | 0.88 % | 5.1 % | 9.53 % | 16.63 % | 30.96 % | 43.06 % |
| 2.5 ATR | 16.144 % | 23.4293 | 0.1 % | 2.16 % | 4.52 % | 9.74 % | 20.87 % | 33.07 % |
| 3.0 ATR | 19.373 % | 22.5271 | 0.1 % | 0.98 % | 2.36 % | 6.59 % | 14.94 % | 25.87 % |
| 4.0 ATR | 25.831 % | 20.7229 | 0.0 % | 0.59 % | 1.18 % | 2.76 % | 8.51 % | 17.18 % |
| 6.0 ATR | 38.746 % | 17.1143 | 0.0 % | 0.0 % | 0.2 % | 0.49 % | 2.18 % | 7.99 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.40 ATR | 0.45 ATR | 0.60 ATR | 0.71 ATR | 0.81 ATR | 1.13 ATR | 1.41 ATR |
| **2 s.** | 0.24 ATR | 0.56 ATR | 0.63 ATR | 0.83 ATR | 0.99 ATR | 1.16 ATR | 1.60 ATR | 2.02 ATR |
| **3 s.** | 0.30 ATR | 0.70 ATR | 0.79 ATR | 1.01 ATR | 1.23 ATR | 1.40 ATR | 1.97 ATR | 2.45 ATR |
| **5 s.** | 0.36 ATR | 0.86 ATR | 0.97 ATR | 1.34 ATR | 1.64 ATR | 1.85 ATR | 2.48 ATR | 3.42 ATR |
| **10 s.** | 0.56 ATR | 1.24 ATR | 1.41 ATR | 1.91 ATR | 2.29 ATR | 2.57 ATR | 3.77 ATR | 5.11 ATR |
| **20 s.** | 0.79 ATR | 1.71 ATR | 1.92 ATR | 2.50 ATR | 3.10 ATR | 3.67 ATR | 5.56 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.451–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.229 %, prix 27.0378), p(touche) 40.39 % (en stress 83.33 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (88.1 % des re-echantillons)
- **2 seance(s)** : plage utile 0.631–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.843 %, prix 26.5869), p(touche) 37.19 % (en stress 84.31 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.788–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.458 %, prix 26.1356), p(touche) 33.5 % (en stress 89.22 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.974–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.458 %, prix 26.1356), p(touche) 43.8 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.414–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.687 %, prix 25.2335), p(touche) 42.53 % (en stress 97.06 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.918–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (12.915 %, prix 24.3315), p(touche) 43.06 % (en stress 97.03 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.183 | EV/share : €0.329 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 38 % | T2 20 % | T3 11 %
- Kelly (position) : f* 0.135 | ¼-Kelly 0.034 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 80.7 | bear 14.3 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 140.0 (= 5 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.123% → cible +3.299% / stop −1.979%, p_fill 64%, n_eff≈67.7) : P(cible|rempli) **15%** · **EV/risk -0.255** (×p_fill ; si rempli -0.79% du capital)
  - **swing** (entrée dip −4.672% → cible +9.646% / stop −6.774%, p_fill 43%, n_eff≈52.4) : P(cible|rempli) **38%** · **EV/risk -0.028** (×p_fill ; si rempli -0.43% du capital)
  - **deep** (entrée dip −7.224% → cible +12.657% / stop −10.44%, p_fill 47%, n_eff≈53.5) : P(cible|rempli) **41%** · **EV/risk -0.064** (×p_fill ; si rempli -1.43% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→87% · +1.0%→77% · +2.0%→70% · +3.0%→55% · +5.0%→37% · +8.0%→18%
- Range intraday médian 7.15% (p90 14.96%) · excursion haute méd. +3.55% / basse méd. −3.31%
- Profil de vol intra : ouverture 4.946% vs midi 1.547% vs clôture 1.751% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 93% · range 5% · trend ↑1%/↓0% ; spike-down 72% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; mean-reverting — autocorr -0.069)_ ; drift intra méd. -0.248% ; recovery-V 21%
- **σ réalisé intraday** 4.515% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 62% / bas 65% / whipsaw 27%
- POC intraday (dernière séance, temps-au-prix) : 29.6956 (VA 29.2389–30.2031 ; dernier close 28.38)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 25% · rebond 93% · **stop −3.81%** sous le fill (sous le bruit) · cible +2.18% · R/R 0.57 (high win-rate)
- Gaps overnight (n=158) : méd. 0.29% · baisse 40% (gap-down >1% 11% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.73% (p90 −3.48%) · haut méd +0.8% · range méd 2.29%
- Excursion ouverture 15min (n=160) : bas méd −1.21% (p90 −4.15%) · haut méd +1.4% · range méd 2.94%
- Excursion ouverture 30min (n=160) : bas méd −1.38% (p90 −4.48%) · haut méd +1.96% · range méd 3.62%
- Excursion ouverture 60min (n=160) : bas méd −1.53% (p90 −5.62%) · haut méd +2.08% · range méd 4.28%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 28.24 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 79% (122/158) · gap 21% · délai 0.3min · rebond 62% (81/122) (MFE +2.03%)
   - −1.0% : fill 30min 50% · séance 73% (116/158) · gap 11% · délai 5.3min · rebond 60% (77/116) (MFE +1.51%)
   - −1.5% : fill 30min 44% · séance 67% (103/158) · gap 7% · délai 6.9min · rebond 58% (64/103) (MFE +1.47%)
   - −2.0% : fill 30min 36% · séance 63% (96/158) · gap 5% · délai 13.6min · rebond 54% (58/96) (MFE +1.12%)
   - −3.0% : fill 30min 20% · séance 45% (77/158) · gap 2% · délai 37.6min · rebond 55% (51/77) (MFE +1.4%)
   - −4.0% : fill 30min 13% · séance 38% (66/158) · gap 1% · délai 65.6min · rebond 70% (52/66) (MFE +1.57%)
   - −5.0% : fill 30min 10% · séance 25% (51/158) · gap 1% · délai 58.4min · rebond 93% (48/51) (MFE +2.18%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −3.09%) → stop au-delà de −1.77% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.65% (p90 −3.86%) → stop au-delà de −2.05% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.56% (p90 −3.92%) → stop au-delà de −2.1% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1487 jambes) : jambe baissière méd −1.2% (p90 −2.96%) · ~17.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (47 séances) :
      · −1.0% : fill 91% (45/47) · rebond 54% (26/45)
      · −2.0% : fill 84% (41/47) · rebond 49% (22/41)
      · −3.0% : fill 69% (37/47) · rebond 50% (25/37)
      · −4.0% : fill 61% (33/47) · rebond 58% (24/33)
      · −5.0% : fill 44% (27/47) · rebond 86% (24/27)
   - **flat** (32 séances) :
      · −1.0% : fill 73% (24/32) · rebond 66% (17/24)
      · −2.0% : fill 56% (19/32) · rebond 49% (12/19)
      · −3.0% : fill 37% (14/32) · rebond 43% (8/14)
      · −4.0% : fill 33% (13/32) · rebond 66% (10/13)
      · −5.0% : fill 23% (9/32) · rebond 100% (9/9)
   - **gap-up** (79 séances) :
      · −1.0% : fill 64% (47/79) · rebond 60% (34/47)
      · −2.0% : fill 54% (36/79) · rebond 62% (24/36)
      · −3.0% : fill 34% (26/79) · rebond 67% (18/26)
      · −4.0% : fill 26% (20/79) · rebond 88% (18/20)
      · −5.0% : fill 16% (15/79) · rebond 100% (15/15)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 41% en base · 54% si les 15 1res min sont vertes (78 cas) · 29% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **31min** → P(séance verte=clôture>ouverture) 66% si début vert vs 21% si rouge (base 41% · écart 45 pts) ; prédictivité sature ensuite (plafond brut 252min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **66%** · continue >prix actuel 53% ; creux résiduel méd -2.53% (q20 -5.93%) → **SL/trailing à −5.93%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.27% / q75 +4.81% → **scale +3.27% / runner +4.81%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **21%** (continue à baisser 62%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.38%** (au-delà de la MAE q10 -6.38%), cible rebond +1.98% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.47% .. +5.28%] · haut q95 +6.9% · bas q05 -5.84%
   - 60min (n=160) : retour [-5.4% .. +5.04%] · haut q95 +7.49% · bas q05 -6.96%
   - 2h (n=160) : retour [-5.22% .. +7.25%] · haut q95 +9.23% · bas q05 -7.53%
   - 4h (n=160) : retour [-6.33% .. +7.51%] · haut q95 +9.97% · bas q05 -8.38%
   - 6h (n=160) : retour [-6.09% .. +8.27%] · haut q95 +11.42% · bas q05 -8.63%
   - session (n=160) : retour [-7.27% .. +9.93%] · haut q95 +12.81% · bas q05 -9.66%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.07%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.17 · part idiosyncratique 0.83
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 40.4  _(momentum baissier)_
- **ADX** : 21.1  _(pas de tendance nette)_
- **MACD** : hist -0.078  _(bearish_recent)_
- **BB** : %B 0.3 · largeur 13.8%
- **ATR** : 1.8 (47.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.035  _(neutre)_
- **Vol ratio** : 0.34  _(volume atone)_
- **Choppiness** : 61.4  _(transition)_
- **MA** : MA20 28.74 · MA50 27.55 · MA200 28.07  _(prix < MA20)_
- **Dist MA** : MA20 -2.8% · MA50 +1.4% · MA200 -0.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (847159 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
