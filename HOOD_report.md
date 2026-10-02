# HOOD

**Generated** : 2026-10-02T00:31:22.045529+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $111.16  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)  
> ↳ spot $111.16 (+4.6% vs entrée) · entrée $106.25 · stop $98.91 · T1 $120.93 · R/R 2.0  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +2.2 % ≠ (strike 115.0 − spot 111.16)/spot = +3.5 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $104.99–$107.51 (mid $106.25)
- Spot actuel : $111.16 (+4.6% au-dessus de la zone — repli à attendre)
- Stop : $98.91 (R/R 2 (resserré, parité Claude) ; -6.91 % depuis l'entree)
- Targets : T1 $120.93 · R/R 2.0 | T2 $127.78 · R/R 2.93 | T3 $134.63 · R/R 3.87
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $98.91


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.02 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (11.02 %)** : le gap seul le franchit 0.399 % des séances (5 fois sur 1253).
   - exécution **0.884 pt plus bas** dans le cas TYPIQUE (médiane), 5.301 au p90, **6.765 au pire**
   - perte réelle **13.192 %** en moyenne _(tirée par la queue)_, jusqu'à **17.785 %** — au lieu des 11.02 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0087 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.416 % | p01 -7.308 % | pire -17.785 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3158** [0.25 ; 0.3877] _(largeur 13.8 pt, n_eff 173.1)_
   - swing : **0.3953** [0.3448 ; 0.4475] _(largeur 10.3 pt, n_eff 345.7)_
   - deep : **0.4221** [0.3709 ; 0.4746] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : swing (29.8 pt), deep (30.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 480 séances)** : VaR **-7.0 %** | CVaR **-9.78 %** | vol 4.77 %/j
   - _fenêtre arrêtée : rupture de regime a 540 seances en arriere (volatilite 2.69 % contre 4.71 % aujourd'hui, rapport 0.57)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.55 % vs -14.36 % si l'on extrapolait par √5 _(rapport 1.013 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7721** (β de hausse 1.6119, asymétrie 1.0994) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.397× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 103.5011 sur atr_grid (1.25 ATR, 6.89 %) — p(stop avant cible) 0.5433 [0.49 ; 0.60], R/R 2.906, perte reelle 7.266 % (gap inclus), CVaR 10.703 %, EV 1.3499 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.1304 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 14.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.543, borne haute 0.595 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 8.268 %) — p(stop avant cible) 0.4534 [0.40 ; 0.51], R/R 2.425, perte reelle 8.707 % (gap inclus), EV 1.7084 % — **REFUSE**
      - refuse : R/R 2.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 1.71 ATR (stop 12.019 %) — p(stop avant cible) 0.2824 [0.24 ; 0.33], R/R 1.658, perte reelle 12.736 % (gap inclus), EV 2.5025 % — **REFUSE**
      - refuse : R/R 1.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.98 % > budget 12.00 %
   - 🟢 support a 3.22 ATR (stop 20.331 %) — p(stop avant cible) 0.0727 [0.05 ; 0.10], R/R 1.022, perte reelle 20.666 % (gap inclus), EV 2.964 % — **REFUSE**
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.82 % > budget 12.00 %
   - 🟢 support a 5.26 ATR (stop 31.585 %) — p(stop avant cible) 0.0157 [0.01 ; 0.03], R/R 0.665, perte reelle 31.737 % (gap inclus), EV 2.9875 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.88 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.378 %) — p(stop avant cible) 0.9093 [0.88 ; 0.94], R/R 14.129, perte reelle 1.494 % (gap inclus), EV 0.0039 % — **REFUSE**
      - refuse : cible atteinte seulement 3.9 % du temps (< 15 %) meme a 10 seances : le R/R de 14.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.909, borne haute 0.936 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 2.756 %) — p(stop avant cible) 0.783 [0.74 ; 0.82], R/R 7.157, perte reelle 2.95 % (gap inclus), EV 0.7615 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.783, borne haute 0.824 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 4.134 %) — p(stop avant cible) 0.684 [0.63 ; 0.73], R/R 4.846, perte reelle 4.357 % (gap inclus), EV 1.177 % — **REFUSE**
      - refuse : cible atteinte seulement 11.9 % du temps (< 15 %) meme a 10 seances : le R/R de 4.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.684, borne haute 0.731 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.0 ATR (stop 5.512 %) — p(stop avant cible) 0.6197 [0.57 ; 0.67], R/R 3.594, perte reelle 5.875 % (gap inclus), EV 1.082 % — **REFUSE**
      - refuse : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.620, borne haute 0.670 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.25 ATR (stop 6.89 %) — p(stop avant cible) 0.5433 [0.49 ; 0.60], R/R 2.906, perte reelle 7.266 % (gap inclus), EV 1.3499 % — **REFUSE**
      - refuse : cible atteinte seulement 14.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.543, borne haute 0.595 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 grid_snapped a 1.71 ATR (stop 11.081 %) — p(stop avant cible) 0.3165 [0.27 ; 0.37], R/R 1.805, perte reelle 11.7 % (gap inclus), EV 2.3529 % — **REFUSE**
      - refuse : R/R 1.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.93 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 13.78 %) — p(stop avant cible) 0.2374 [0.19 ; 0.28], R/R 1.473, perte reelle 14.334 % (gap inclus), EV 2.4647 % — **REFUSE**
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.41 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 15.158 %) — p(stop avant cible) 0.1983 [0.16 ; 0.24], R/R 1.346, perte reelle 15.69 % (gap inclus), EV 2.5488 % — **REFUSE**
      - refuse : R/R 1.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.27 % > budget 12.00 %
   - 🟢 grid_snapped a 3.22 ATR (stop 19.394 %) — p(stop avant cible) 0.088 [0.06 ; 0.12], R/R 1.071, perte reelle 19.712 % (gap inclus), EV 2.9501 % — **REFUSE**
      - refuse : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.95 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 22.048 %) — p(stop avant cible) 0.0566 [0.04 ; 0.08], R/R 0.941, perte reelle 22.446 % (gap inclus), EV 2.9727 % — **REFUSE**
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.50 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 24.804 %) — p(stop avant cible) 0.0331 [0.02 ; 0.06], R/R 0.832, perte reelle 25.364 % (gap inclus), EV 2.9805 % — **REFUSE**
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.60 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 27.56 %) — p(stop avant cible) 0.0265 [0.01 ; 0.05], R/R 0.756, perte reelle 27.929 % (gap inclus), EV 2.9834 % — **REFUSE**
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.43 % > budget 12.00 %
   - 🟢 grid_snapped a 5.26 ATR (stop 30.648 %) — p(stop avant cible) 0.021 [0.01 ; 0.04], R/R 0.685, perte reelle 30.813 % (gap inclus), EV 2.9824 % — **REFUSE**
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.94 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 33.072 %) — p(stop avant cible) 0.0061 [0.00 ; 0.02], R/R 0.634, perte reelle 33.311 % (gap inclus), EV 3.0632 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.58 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 35.828 %) — p(stop avant cible) 0.0019 [0.00 ; 0.01], R/R 0.579, perte reelle 36.492 % (gap inclus), EV 3.1137 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.61 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 38.584 %) — p(stop avant cible) 0.0009 [0.00 ; 0.01], R/R 0.547, perte reelle 38.584 % (gap inclus), EV 3.1227 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.48 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 41.34 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.511, perte reelle 41.34 % (gap inclus), EV 3.1316 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.28 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 44.096 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.479, perte reelle 44.096 % (gap inclus), EV 3.1316 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.28 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 111.16, ATR14 6.1271 (5.512 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.374 ATR = 2.061 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.276 % | 110.8536 | 93.05 % | 95.16 % | 96.06 % | 96.56 % | 97.05 % | 98.05 % |
| 0.1 ATR | 0.551 % | 110.5473 | 85.5 % | 90.52 % | 92.23 % | 93.73 % | 94.72 % | 96.41 % |
| 0.15 ATR | 0.827 % | 110.2409 | 77.54 % | 85.18 % | 87.99 % | 90.29 % | 92.58 % | 95.07 % |
| 0.2 ATR | 1.102 % | 109.9346 | 71.5 % | 80.14 % | 83.75 % | 86.96 % | 90.35 % | 93.22 % |
| 0.25 ATR | 1.378 % | 109.6282 | 64.65 % | 74.5 % | 79.21 % | 83.42 % | 87.7 % | 90.86 % |
| 0.35 ATR | 1.929 % | 109.0155 | 52.37 % | 65.32 % | 71.95 % | 77.55 % | 83.43 % | 87.89 % |
| 0.5 ATR | 2.756 % | 108.0964 | 37.26 % | 53.53 % | 61.25 % | 68.35 % | 76.52 % | 82.14 % |
| 0.75 ATR | 4.134 % | 106.5646 | 19.64 % | 36.09 % | 45.81 % | 55.61 % | 65.55 % | 72.9 % |
| 1.0 ATR | 5.512 % | 105.0329 | 9.37 % | 23.08 % | 32.8 % | 43.88 % | 54.88 % | 65.3 % |
| 1.25 ATR | 6.89 % | 103.5011 | 4.93 % | 14.52 % | 22.3 % | 33.37 % | 46.95 % | 58.73 % |
| 1.5 ATR | 8.268 % | 101.9693 | 2.52 % | 9.78 % | 16.15 % | 26.9 % | 40.04 % | 53.08 % |
| 2.0 ATR | 11.024 % | 98.9057 | 0.5 % | 3.83 % | 7.27 % | 15.37 % | 29.57 % | 43.74 % |
| 2.5 ATR | 13.78 % | 95.8421 | 0.1 % | 1.51 % | 3.83 % | 8.19 % | 21.44 % | 34.5 % |
| 3.0 ATR | 16.536 % | 92.7786 | 0.0 % | 0.71 % | 2.32 % | 5.26 % | 15.45 % | 26.49 % |
| 4.0 ATR | 22.048 % | 86.6514 | 0.0 % | 0.4 % | 0.91 % | 2.22 % | 6.91 % | 14.89 % |
| 6.0 ATR | 33.072 % | 74.3971 | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.32 % | 4.62 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.37 ATR | 0.42 ATR | 0.56 ATR | 0.67 ATR | 0.74 ATR | 0.98 ATR | 1.25 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.62 ATR | 0.81 ATR | 0.96 ATR | 1.09 ATR | 1.49 ATR | 1.90 ATR |
| **3 s.** | 0.31 ATR | 0.68 ATR | 0.77 ATR | 1.00 ATR | 1.19 ATR | 1.34 ATR | 1.85 ATR | 2.33 ATR |
| **5 s.** | 0.39 ATR | 0.87 ATR | 0.98 ATR | 1.26 ATR | 1.58 ATR | 1.80 ATR | 2.37 ATR | 3.09 ATR |
| **10 s.** | 0.54 ATR | 1.15 ATR | 1.32 ATR | 1.84 ATR | 2.28 ATR | 2.62 ATR | 3.64 ATR | 4.68 ATR |
| **20 s.** | 0.69 ATR | 1.67 ATR | 1.93 ATR | 2.59 ATR | 3.13 ATR | 3.56 ATR | 4.95 ATR | 5.93 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.423–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.622–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.134 %, prix 106.5646), p(touche) 36.09 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.766–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.512 %, prix 105.0329), p(touche) 32.8 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (60.8 % des re-echantillons)
- **5 seance(s)** : plage utile 0.976–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.512 %, prix 105.0329), p(touche) 43.88 % (en stress 98.99 %)  ✅ optimum identifie (60.6 % des re-echantillons)
- **10 seance(s)** : plage utile 1.321–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.268 %, prix 101.9693), p(touche) 40.04 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.933–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (11.024 %, prix 98.9057), p(touche) 43.74 % (en stress 97.96 %)  ✅ optimum identifie (65.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.009 | EV/share : $-0.067 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 18 % | T2 9 % | T3 3 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 80.9 | bear 14.1 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 395.0 (= 4 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.01% → cible +2.593% / stop −3.0%, p_fill 58%, n_eff≈61.6) : P(cible|rempli) **41%** · **EV/risk +0.047** (×p_fill ; si rempli +0.24% du capital)
  - **swing** (entrée dip −4.417% → cible +13.816% / stop −6.908%, p_fill 33%, n_eff≈38.6) : P(cible|rempli) **26%** · **EV/risk +0.103** (×p_fill ; si rempli +2.17% du capital)
  - **deep** (entrée dip −6.822% → cible +16.759% / stop −8.874%, p_fill 35%, n_eff≈37.7) : P(cible|rempli) **45%** · **EV/risk +0.200** (×p_fill ; si rempli +5.02% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→78% · +2.0%→53% · +3.0%→35% · +5.0%→18% · +8.0%→6%
- Range intraday médian 4.88% (p90 8.86%) · excursion haute méd. +2.08% / basse méd. −2.3%
- Profil de vol intra : ouverture 3.664% vs midi 0.978% vs clôture 1.099% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 20% · trend ↑0%/↓2% ; spike-down 68% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.136 ; mean-reverting — autocorr -0.032)_ ; drift intra méd. -0.503% ; recovery-V 20%
- **σ réalisé intraday** 3.351% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 39% / bas 53% / whipsaw 6%
- POC intraday (dernière séance, temps-au-prix) : 114.38 (VA 112.7–114.66 ; dernier close 112.56)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 24% · rebond 65% · **stop −4.05%** sous le fill (sous le bruit) · cible +2.21% · R/R 0.55 (high win-rate)
- Gaps overnight (n=159) : méd. 0.02% · baisse 49% (gap-down >1% 31% · >2% 15%)
- Excursion ouverture 5min (n=160) : bas méd −1.01% (p90 −2.88%) · haut méd +1.0% · range méd 2.21%
- Excursion ouverture 15min (n=160) : bas méd −1.34% (p90 −3.53%) · haut méd +1.29% · range méd 2.92%
- Excursion ouverture 30min (n=160) : bas méd −1.64% (p90 −3.76%) · haut méd +1.55% · range méd 3.42%
- Excursion ouverture 60min (n=160) : bas méd −1.99% (p90 −3.98%) · haut méd +1.67% · range méd 3.85%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 112.5 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 80% (123/159) · gap 39% · délai 0.0min · rebond 62% (71/123) (MFE +1.43%)
   - −1.0% : fill 30min 61% · séance 69% (108/159) · gap 31% · délai 0.0min · rebond 67% (67/108) (MFE +1.65%)
   - −1.5% : fill 30min 48% · séance 62% (98/159) · gap 22% · délai 1.1min · rebond 59% (55/98) (MFE +1.33%)
   - −2.0% : fill 30min 38% · séance 52% (86/159) · gap 15% · délai 2.8min · rebond 70% (56/86) (MFE +1.4%)
   - −3.0% : fill 30min 23% · séance 35% (64/159) · gap 5% · délai 13.1min · rebond 70% (45/64) (MFE +1.73%)
   - −4.0% : fill 30min 12% · séance 24% (46/159) · gap 2% · délai 30.5min · rebond 65% (32/46) (MFE +2.21%)
   - −5.0% : fill 30min 7% · séance 14% (29/159) · gap 1% · délai 30.0min · rebond 64% (21/29) (MFE +2.33%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.6% (p90 −2.61%) → stop au-delà de −1.72% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.63% (p90 −2.25%) → stop au-delà de −1.85% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −2.18%) → stop au-delà de −1.77% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=759 jambes) : jambe baissière méd −1.13% (p90 −2.7%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (74 séances) :
      · −1.0% : fill 92% (70/74) · rebond 58% (38/70)
      · −2.0% : fill 78% (60/74) · rebond 68% (38/60)
      · −3.0% : fill 59% (48/74) · rebond 80% (35/48)
      · −4.0% : fill 40% (35/74) · rebond 74% (27/35)
      · −5.0% : fill 26% (24/74) · rebond 67% (17/24)
   - **flat** (17 séances) :
      · −1.0% : fill 66% (11/17) · rebond 70% (7/11)
      · −2.0% : fill 47% (9/17) · rebond 53% (5/9)
      · −3.0% : fill 20% (4/17) · rebond 7% (1/4)
      · −4.0% : fill 20% (4/17) · rebond 7% (1/4)
      · −5.0% : fill 16% (2/17) · rebond 15% (1/2)
   - **gap-up** (68 séances) :
      · −1.0% : fill 48% (27/68) · rebond 82% (22/27)
      · −2.0% : fill 27% (17/68) · rebond 85% (13/17)
      · −3.0% : fill 17% (12/68) · rebond 55% (9/12)
      · −4.0% : fill 10% (7/68) · rebond 61% (4/7)
      · −5.0% : fill 3% (3/68) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 68% si les 15 1res min sont vertes (73 cas) · 26% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **26min** → P(séance verte=clôture>ouverture) 72% si début vert vs 20% si rouge (base 44% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 218min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **72%** · continue >prix actuel 50% ; creux résiduel méd -1.45% (q20 -2.7%) → **SL/trailing à −2.7%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.69% / q75 +2.9% → **scale +1.69% / runner +2.9%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **20%** (continue à baisser 57%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.09%** (au-delà de la MAE q10 -4.09%), cible rebond +1.63% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.33% .. +3.97%] · haut q95 +4.33% · bas q05 -5.14%
   - 60min (n=160) : retour [-4.52% .. +4.94%] · haut q95 +5.47% · bas q05 -5.69%
   - 2h (n=160) : retour [-4.95% .. +5.51%] · haut q95 +7.52% · bas q05 -6.11%
   - 4h (n=160) : retour [-4.97% .. +6.89%] · haut q95 +8.31% · bas q05 -6.8%
   - 6h (n=160) : retour [-6.14% .. +6.62%] · haut q95 +8.51% · bas q05 -7.39%
   - session (n=160) : retour [-5.89% .. +7.0%] · haut q95 +8.62% · bas q05 -7.66%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.1% des séances sont trend-up (mild 0% / strong 8.1%) · base = 13 séances trend-up (n_eff 8.5)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **31%**. Lecture précoce 30 min : signature présente → 20% vs absente 2% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.92% (p75 1.24% / p90 1.92%) · ~4.0 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **77%** (reprise méd 15.35 min, n=49)
   - −1.0% → **62%** (reprise méd 30.0 min, n=21)
   - −1.5% → **48%** (reprise méd 42.24 min, n=10)
   - −2.0% → **15%** (reprise méd None min, n=5)
   - −3.0% → **20%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.92%** (p90, défaut prudent ; serré/agressif −1.24%) ; extension open→close méd +6.2% (q75 +8.64% / q95 +11.94%), MFE méd +7.69% / q90 +13.19%
   - Échelle scale-out : +7.69% (33%) / +9.01% (33%) / +13.19% (34%)
- **DÉSARMER** : repli > **−1.92%** depuis le plus-haut = décay → P(retournement) **85%** (préavis méd 310.68 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.19% : P(retournement après) 0% (mèche méd 3.29%)
- **CONTEXTE** : la dernière heure tient les gains 73% du temps (retour médian dernière heure +0.39%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.64 · part idiosyncratique 0.36
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 48.4  _(neutre)_
- **ADX** : 16.0  _(pas de tendance nette)_
- **MACD** : hist -1.191  _(bearish_recent)_
- **BB** : %B 0.26 · largeur 19.1%
- **ATR** : 6.13 (51.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.111  _(distribution)_
- **Vol ratio** : 0.73  _(volume normal)_
- **Choppiness** : 46.7  _(transition)_
- **MA** : MA20 116.55 · MA50 105.17 · MA200 94.34  _(prix < MA20)_
- **Dist MA** : MA20 -4.6% · MA50 +5.7% · MA200 +17.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (843081 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
