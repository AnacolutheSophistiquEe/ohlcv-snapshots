# MSTR

**Generated** : 2026-09-30T00:25:22.498392+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 9/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite normal · $154.72  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $154.72 (+1.2% vs entrée) · entrée $152.88 · stop $143.72 · T1 $171.19 · R/R 2.0  
> ↳ P(T1 av. stop) 33 % _(réel 5 s)_ · EV/risk 0.13 _(réel 5 s)_ (GBM 0.037) · ¼-Kelly 0.006 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -1.4 % ≠ (strike 155.0 − spot 154.72)/spot = +0.2 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $151.03–$154.72 (mid $152.88)
- Spot actuel : $154.72 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : $143.72 (R/R 2 (resserré, parité Claude) ; -5.99 % depuis l'entree)
- Targets : T1 $171.19 · R/R 2.0 | T2 $179.62 · R/R 2.92 | T3 $188.06 · R/R 3.84
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $143.72


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=10.46 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.11 %)** : le gap seul le franchit 1.516 % des séances (19 fois sur 1253).
   - exécution **1.142 pt plus bas** dans le cas TYPIQUE (médiane), 10.101 au p90, **20.262 au pire**
   - perte réelle **10.893 %** en moyenne _(tirée par la queue)_, jusqu'à **27.372 %** — au lieu des 7.11 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0574 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.349 % | p01 -7.775 % | pire -27.372 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1752** [0.1242 ; 0.237] _(largeur 11.3 pt, n_eff 173.1)_
   - swing : **0.4833** [0.4309 ; 0.5359] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.455** [0.4031 ; 0.5077] _(largeur 10.5 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 300 séances)** : VaR **-7.01 %** | CVaR **-9.02 %** | vol 4.89 %/j
   - _fenêtre arrêtée : rupture de regime a 360 seances en arriere (volatilite 3.06 % contre 5.33 % aujourd'hui, rapport 0.58)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.99 % vs -17.67 % si l'on extrapolait par √5 _(rapport 0.962 ; < 1 = le √5 surestime)_
- **β de baisse : 2.3644** (β de hausse 1.8257, asymétrie 1.2951) vs IWM — 604 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 142.2292 sur grid_snapped (1.09 ATR, 8.073 %) — p(stop avant cible) 0.5075 [0.45 ; 0.56], R/R 2.727, perte reelle 8.248 % (gap inclus), CVaR 9.737 %, EV 0.7112 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.1399 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 14.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.507, borne haute 0.560 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 17 des 19 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 41.9 % de la queue et il ne reste que 294.13 EUR a partager. Prix du risque 0.099 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.37 ATR (stop 4.777 %) — p(stop avant cible) 0.7031 [0.65 ; 0.75], R/R 4.502, perte reelle 4.996 % (gap inclus), EV 0.1757 % — **REFUSE**
      - refuse : cible atteinte seulement 10.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.703, borne haute 0.749 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - 🔴 support a 1.09 ATR (stop 8.972 %) — p(stop avant cible) 0.4754 [0.42 ; 0.53], R/R 2.466, perte reelle 9.122 % (gap inclus), EV 0.5778 % — **REFUSE**
      - refuse : cible atteinte seulement 14.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.27 ATR du spot — compartiment <1, mesure a 49.1 % de casse (IC clusterise [0.457 ; 0.522] sur 1123 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 2.06 ATR (stop 14.575 %) — p(stop avant cible) 0.2718 [0.23 ; 0.32], R/R 1.524, perte reelle 14.755 % (gap inclus), EV 0.5352 % — **REFUSE**
      - refuse : R/R 1.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.55 % > budget 12.00 %
   - ⚪ swing_based a 3.7 ATR (stop 24.085 %) — p(stop avant cible) 0.0995 [0.07 ; 0.13], R/R 0.92, perte reelle 24.462 % (gap inclus), EV 0.0793 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.83 % > budget 12.00 %
   - 🟢 support a 4.27 ATR (stop 27.405 %) — p(stop avant cible) 0.0598 [0.04 ; 0.09], R/R 0.807, perte reelle 27.873 % (gap inclus), EV 0.0774 % — **REFUSE**
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.96 % > budget 12.00 %
   - ⚪ grid_snapped a 0.37 ATR (stop 3.879 %) — p(stop avant cible) 0.7718 [0.73 ; 0.81], R/R 5.548, perte reelle 4.054 % (gap inclus), EV -0.125 % — **REFUSE**
      - refuse : cible atteinte seulement 8.7 % du temps (< 15 %) meme a 10 seances : le R/R de 5.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.772, borne haute 0.814 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 8.7 % x 22.49 % + P(rien) 14.1 % x 7.40 % ne couvrent pas P(stop) 77.2 % x 4.05 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 grid_snapped a 1.09 ATR (stop 8.073 %) — p(stop avant cible) 0.5075 [0.45 ; 0.56], R/R 2.727, perte reelle 8.248 % (gap inclus), EV 0.7112 % — **REFUSE**
      - refuse : cible atteinte seulement 14.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.507, borne haute 0.560 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.75 ATR (stop 10.145 %) — p(stop avant cible) 0.4233 [0.37 ; 0.48], R/R 2.193, perte reelle 10.256 % (gap inclus), EV 0.5271 % — **REFUSE**
      - refuse : cible atteinte seulement 14.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 grid_snapped a 2.06 ATR (stop 13.677 %) — p(stop avant cible) 0.2893 [0.24 ; 0.34], R/R 1.618, perte reelle 13.898 % (gap inclus), EV 0.7105 % — **REFUSE**
      - refuse : R/R 1.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.95 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 15.942 %) — p(stop avant cible) 0.2281 [0.19 ; 0.27], R/R 1.391, perte reelle 16.172 % (gap inclus), EV 0.3943 % — **REFUSE**
      - refuse : R/R 1.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.99 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 17.391 %) — p(stop avant cible) 0.191 [0.15 ; 0.23], R/R 1.269, perte reelle 17.723 % (gap inclus), EV 0.3207 % — **REFUSE**
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.66 % > budget 12.00 %
   - ⚪ grid_snapped a 3.7 ATR (stop 23.187 %) — p(stop avant cible) 0.1187 [0.09 ; 0.16], R/R 0.955, perte reelle 23.541 % (gap inclus), EV 0.0453 % — **REFUSE**
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.03 % > budget 12.00 %
   - 🟢 grid_snapped a 4.27 ATR (stop 26.506 %) — p(stop avant cible) 0.0716 [0.05 ; 0.10], R/R 0.837, perte reelle 26.887 % (gap inclus), EV 0.0929 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.05 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 28.986 %) — p(stop avant cible) 0.0517 [0.03 ; 0.08], R/R 0.762, perte reelle 29.5 % (gap inclus), EV 0.0531 % — **REFUSE**
      - refuse : R/R 0.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.52 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 31.884 %) — p(stop avant cible) 0.0286 [0.01 ; 0.05], R/R 0.694, perte reelle 32.424 % (gap inclus), EV 0.1477 % — **REFUSE**
      - refuse : R/R 0.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.27 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 34.783 %) — p(stop avant cible) 0.0179 [0.01 ; 0.04], R/R 0.636, perte reelle 35.382 % (gap inclus), EV 0.2 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.88 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 37.681 %) — p(stop avant cible) 0.0059 [0.00 ; 0.02], R/R 0.59, perte reelle 38.133 % (gap inclus), EV 0.299 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.64 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 40.58 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 0.547, perte reelle 41.139 % (gap inclus), EV 0.3401 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.84 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 43.478 %) — p(stop avant cible) 0.0004 [0.00 ; 0.01], R/R 0.517, perte reelle 43.536 % (gap inclus), EV 0.3501 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.68 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 46.377 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.485, perte reelle 46.377 % (gap inclus), EV 0.354 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.58 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 154.72, ATR14 8.9693 (5.797 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.394 ATR = 2.284 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.29 % | 154.2715 | 93.96 % | 96.47 % | 96.97 % | 97.67 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.58 % | 153.8231 | 88.12 % | 91.94 % | 93.44 % | 94.84 % | 96.65 % | 97.23 % |
| 0.15 ATR | 0.87 % | 153.3746 | 81.27 % | 87.1 % | 89.81 % | 91.91 % | 94.21 % | 95.48 % |
| 0.2 ATR | 1.159 % | 152.9261 | 73.62 % | 81.65 % | 84.96 % | 88.27 % | 91.46 % | 93.53 % |
| 0.25 ATR | 1.449 % | 152.4777 | 67.67 % | 77.82 % | 82.14 % | 86.15 % | 89.13 % | 91.99 % |
| 0.35 ATR | 2.029 % | 151.5808 | 54.88 % | 68.75 % | 75.28 % | 80.89 % | 85.67 % | 89.32 % |
| 0.5 ATR | 2.899 % | 150.2354 | 38.17 % | 55.24 % | 63.37 % | 71.28 % | 78.35 % | 84.5 % |
| 0.75 ATR | 4.348 % | 147.993 | 19.34 % | 37.6 % | 46.92 % | 57.94 % | 67.89 % | 76.8 % |
| 1.0 ATR | 5.797 % | 145.7507 | 9.26 % | 25.1 % | 34.61 % | 46.11 % | 58.54 % | 69.82 % |
| 1.25 ATR | 7.246 % | 143.5084 | 4.13 % | 14.52 % | 24.72 % | 35.59 % | 49.59 % | 62.42 % |
| 1.5 ATR | 8.696 % | 141.2661 | 2.11 % | 8.67 % | 17.26 % | 28.82 % | 42.78 % | 56.78 % |
| 2.0 ATR | 11.594 % | 136.7814 | 0.2 % | 3.12 % | 7.37 % | 15.98 % | 30.89 % | 46.82 % |
| 2.5 ATR | 14.493 % | 132.2968 | 0.1 % | 0.91 % | 2.42 % | 8.7 % | 21.24 % | 37.37 % |
| 3.0 ATR | 17.391 % | 127.8121 | 0.1 % | 0.5 % | 1.01 % | 4.55 % | 14.53 % | 28.03 % |
| 4.0 ATR | 23.188 % | 118.8429 | 0.0 % | 0.0 % | 0.3 % | 0.81 % | 6.2 % | 18.07 % |
| 6.0 ATR | 34.783 % | 100.9043 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.61 % | 4.41 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.39 ATR | 0.44 ATR | 0.57 ATR | 0.68 ATR | 0.74 ATR | 0.98 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.57 ATR | 0.65 ATR | 0.84 ATR | 1.00 ATR | 1.12 ATR | 1.44 ATR | 1.83 ATR |
| **3 s.** | 0.35 ATR | 0.70 ATR | 0.79 ATR | 1.04 ATR | 1.24 ATR | 1.41 ATR | 1.87 ATR | 2.24 ATR |
| **5 s.** | 0.44 ATR | 0.92 ATR | 1.03 ATR | 1.35 ATR | 1.65 ATR | 1.84 ATR | 2.41 ATR | 2.95 ATR |
| **10 s.** | 0.58 ATR | 1.24 ATR | 1.42 ATR | 1.91 ATR | 2.31 ATR | 2.59 ATR | 3.54 ATR | 4.43 ATR |
| **20 s.** | 0.81 ATR | 1.84 ATR | 2.10 ATR | 2.73 ATR | 3.30 ATR | 3.81 ATR | 5.18 ATR | 5.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.439–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.899 %, prix 150.2347), p(touche) 38.17 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.645–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.348 %, prix 147.9928), p(touche) 37.6 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.789–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.797 %, prix 145.7509), p(touche) 34.61 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.026–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.246 %, prix 143.509), p(touche) 35.59 % (en stress 95.96 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.419–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.696 %, prix 141.2655), p(touche) 42.78 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.096–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (14.493 %, prix 132.2964), p(touche) 37.37 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.037 | EV/share : $0.337 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 24 % | T2 12 % | T3 8 %
- Kelly (position) : f* 0.023 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 23.6 | bear 8.8 | side 67.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 546.0 (= 4 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.543% → cible +9.083% / stop −4.542%, p_fill 88%, n_eff≈97.8) : P(cible|rempli) **5%** · **EV/risk +0.011** (×p_fill ; si rempli +0.06% du capital)
  - **swing** (entrée dip −1.192% → cible +11.979% / stop −5.99%, p_fill 83%, n_eff≈98.2) : P(cible|rempli) **33%** · **EV/risk +0.130** (×p_fill ; si rempli +0.94% du capital)
  - **deep** (entrée dip −1.734% → cible +10.848% / stop −8.849%, p_fill 84%, n_eff≈94.5) : P(cible|rempli) **54%** · **EV/risk +0.162** (×p_fill ; si rempli +1.71% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→83% · +1.0%→78% · +2.0%→58% · +3.0%→41% · +5.0%→18% · +8.0%→9%
- Range intraday médian 5.33% (p90 9.67%) · excursion haute méd. +2.57% / basse méd. −2.28%
- Profil de vol intra : ouverture 3.323% vs midi 1.151% vs clôture 1.278% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 13% · trend ↑3%/↓0% ; spike-down 68% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.132 ; mean-reverting — autocorr -0.041)_ ; drift intra méd. 0.59% ; recovery-V 30%
- **σ réalisé intraday** 3.541% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 62% / bas 54% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 153.8116 (VA 152.7104–154.2521 ; dernier close 154.72)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 24% · rebond 79% · **stop −3.86%** sous le fill (sous le bruit) · cible +2.51% · R/R 0.65 (high win-rate)
- Gaps overnight (n=159) : méd. -0.05% · baisse 52% (gap-down >1% 37% · >2% 26%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −2.29%) · haut méd +0.82% · range méd 1.87%
- Excursion ouverture 15min (n=160) : bas méd −1.09% (p90 −2.85%) · haut méd +1.22% · range méd 2.58%
- Excursion ouverture 30min (n=160) : bas méd −1.2% (p90 −3.19%) · haut méd +1.42% · range méd 3.04%
- Excursion ouverture 60min (n=160) : bas méd −1.51% (p90 −3.58%) · haut méd +1.83% · range méd 3.74%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 154.72 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 72% (118/159) · gap 44% · délai 0.0min · rebond 45% (55/118) (MFE +0.52%)
   - −1.0% : fill 30min 56% · séance 67% (112/159) · gap 37% · délai 0.0min · rebond 44% (58/112) (MFE +0.79%)
   - −1.5% : fill 30min 47% · séance 64% (105/159) · gap 30% · délai 0.0min · rebond 51% (57/105) (MFE +1.08%)
   - −2.0% : fill 30min 40% · séance 58% (95/159) · gap 26% · délai 0.0min · rebond 60% (56/95) (MFE +1.28%)
   - −3.0% : fill 30min 28% · séance 44% (76/159) · gap 15% · délai 1.2min · rebond 59% (44/76) (MFE +1.58%)
   - −4.0% : fill 30min 20% · séance 34% (61/159) · gap 4% · délai 11.4min · rebond 76% (43/61) (MFE +1.92%)
   - −5.0% : fill 30min 14% · séance 24% (43/159) · gap 3% · délai 17.2min · rebond 79% (33/43) (MFE +2.51%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.66% (p90 −2.2%) → stop au-delà de −1.66% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.87% (p90 −2.23%) → stop au-delà de −1.72% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.83% (p90 −2.28%) → stop au-delà de −1.82% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=942 jambes) : jambe baissière méd −1.11% (p90 −2.6%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (76 séances) :
      · −1.0% : fill 96% (75/76) · rebond 41% (33/75)
      · −2.0% : fill 91% (69/76) · rebond 60% (40/69)
      · −3.0% : fill 74% (60/76) · rebond 56% (34/60)
      · −4.0% : fill 63% (51/76) · rebond 76% (36/51)
      · −5.0% : fill 46% (38/76) · rebond 81% (30/38)
   - **flat** (18 séances) :
      · −1.0% : fill 69% (13/18) · rebond 68% (10/13)
      · −2.0% : fill 52% (9/18) · rebond 54% (5/9)
      · −3.0% : fill 43% (7/18) · rebond 71% (4/7)
      · −4.0% : fill 20% (4/18) · rebond 80% (3/4)
      · −5.0% : fill 6% (2/18) · rebond 0% (0/2)
   - **gap-up** (65 séances) :
      · −1.0% : fill 33% (24/65) · rebond 39% (15/24)
      · −2.0% : fill 22% (17/65) · rebond 62% (11/17)
      · −3.0% : fill 11% (9/65) · rebond 69% (6/9)
      · −4.0% : fill 5% (6/65) · rebond 63% (4/6)
      · −5.0% : fill 3% (3/65) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 57% si les 15 1res min sont vertes (85 cas) · 32% si rouges (75 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:14** → P(séance verte=clôture>ouverture) 73% si début vert vs 9% si rouge (base 46% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=90) : tient le vert **73%** · continue >prix actuel 51% ; creux résiduel méd -1.31% (q20 -2.98%) → **SL/trailing à −2.98%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.0% / q75 +2.95% → **scale +2.0% / runner +2.95%**, sortie à la clôture
  - **si ROUGE au coude** (n=70) : edge inversé — récupère vert seulement **9%** (continue à baisser 56%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.79%** (au-delà de la MAE q10 -4.79%), cible rebond +1.43% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.26% .. +4.05%] · haut q95 +4.51% · bas q05 -3.63%
   - 60min (n=160) : retour [-3.46% .. +5.6%] · haut q95 +5.97% · bas q05 -4.56%
   - 2h (n=160) : retour [-4.65% .. +8.59%] · haut q95 +8.84% · bas q05 -5.68%
   - 4h (n=160) : retour [-4.88% .. +9.52%] · haut q95 +10.38% · bas q05 -6.01%
   - 6h (n=160) : retour [-5.11% .. +8.64%] · haut q95 +11.68% · bas q05 -6.13%
   - session (n=160) : retour [-5.03% .. +8.33%] · haut q95 +11.68% · bas q05 -6.38%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0.6% / strong 5.6%) · base = 10 séances trend-up (n_eff 7.3)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **43%**. Lecture précoce 30 min : signature présente → 23% vs absente 1% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.77% (p75 1.13% / p90 2.71%) · ~4.0 replis/séance, durée méd 34.08 min. P(nouveau plus-haut après repli) :
   - −0.5% → **86%** (reprise méd 20.0 min, n=37)
   - −1.0% → **60%** (reprise méd 31.69 min, n=14)
   - −1.5% → **43%** (reprise méd 42.45 min, n=10)
   - −2.0% → **19%** (reprise méd None min, n=7)
   - −3.0% → **38%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.71%** (p90, défaut prudent ; serré/agressif −1.13%) ; extension open→close méd +9.11% (q75 +12.7% / q95 +13.17%), MFE méd +11.91% / q90 +13.21%
   - Échelle scale-out : +11.91% (33%) / +13.03% (33%) / +13.21% (34%)
- **DÉSARMER** : repli > **−2.71%** depuis le plus-haut = décay → P(retournement) **75%** (préavis méd 182.05 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.21% : P(retournement après) 0% (mèche méd 0.05%)
- **CONTEXTE** : la dernière heure tient les gains 84% du temps (retour médian dernière heure +0.85%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.77 · part idiosyncratique 0.23
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 63.9  _(momentum haussier)_
- **ADX** : 40.3  _(tendance tres forte)_
- **MACD** : hist 0.453  _(pas de croisement recent)_
- **BB** : %B 0.68 · largeur 42.8%
- **ATR** : 8.97 (30.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.093  _(accumulation)_
- **Vol ratio** : 0.6  _(volume atone)_
- **Choppiness** : 36.6  _(marche directionnel)_
- **MA** : MA20 143.67 · MA50 120.05 · MA200 136.23  _(prix > MA20)_
- **Dist MA** : MA20 +7.7% · MA50 +28.9% · MA200 +13.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (848443 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
