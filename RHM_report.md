# RHM

**Generated** : 2026-08-24T00:02:25.699485+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · €1155.40  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €1155.40 (+0.5% vs entrée) · entrée €1149.50 · stop €1126.51 · T1 €1163.87 · R/R 0.63  
> ↳ P(T1 av. stop) 55 % _(réel 5 s)_ · EV/risk -0.009 _(réel 5 s)_ (GBM 0.086) · ¼-Kelly 0.033 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.140 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €1146.63–€1152.37 (mid €1149.50)
- Spot actuel : €1155.40 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : €1126.51 (stop swing_plan-based (-5.32%))
- Targets : T1 €1163.87 · R/R 0.63 | T2 €1178.24 · R/R 1.25 | T3 €1192.61 · R/R 1.88
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €1126.51


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.73 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (5.32 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1274).
   - exécution **2.532 pt plus bas** dans le cas TYPIQUE (médiane), 14.194 au p90, **17.109 au pire**
   - perte réelle **12.114 %** en moyenne _(tirée par la queue)_, jusqu'à **22.429 %** — au lieu des 5.32 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.016 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.562 % | p01 -3.746 % | pire -22.429 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0864** [0.0513 ; 0.1351] _(largeur 8.4 pt, n_eff 173.1)_
   - swing : **0.4018** [0.3511 ; 0.4541] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.5136** [0.461 ; 0.566] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (32.0 pt), swing (30.0 pt), deep (31.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 540 séances)** : VaR **-4.86 %** | CVaR **-6.73 %** | vol 2.97 %/j
   - _fenêtre arrêtée : rupture de regime a 600 seances en arriere (volatilite 1.99 % contre 3.38 % aujourd'hui, rapport 0.59)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.6 % vs -8.98 % si l'on extrapolait par √5 _(rapport 0.846 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5007** (β de hausse 0.587, asymétrie 0.853) vs GDAXI — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.227× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 1073.7225 sur support (1.16 ATR, 7.069 %) — p(stop avant cible) 0.4438 [0.39 ; 0.50], R/R 3.428, perte reelle 15.141 % (gap inclus), CVaR 7.082 %, EV -3.5305 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.59 ATR (stop 4.668 %) — p(stop avant cible) 0.6103 [0.56 ; 0.66], R/R 5.017, perte reelle 10.343 % (gap inclus), EV -3.2599 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.610, borne haute 0.661 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.26 %) : P(cible) 0.0 % x 51.90 % + P(rien) 39.0 % x 7.83 % ne couvrent pas P(stop) 61.0 % x 10.34 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 support a 1.16 ATR (stop 7.069 %) — p(stop avant cible) 0.4438 [0.39 ; 0.50], R/R 3.428, perte reelle 15.141 % (gap inclus), EV -3.5305 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - ⚠ support DETECTE a 0.49 ATR du spot — compartiment <1, mesure a 51.0 % de casse (IC clusterise [0.478 ; 0.541] sur 1127 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.53 %) : P(cible) 0.0 % x 51.90 % + P(rien) 55.6 % x 5.73 % ne couvrent pas P(stop) 44.4 % x 15.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.67 ATR (stop 21.817 %) — p(stop avant cible) 0.0382 [0.02 ; 0.06], R/R 2.314, perte reelle 22.429 % (gap inclus), EV -0.3236 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 21.82 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.32 %) : P(cible) 0.0 % x 51.90 % + P(rien) 96.2 % x 0.55 % ne couvrent pas P(stop) 3.8 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 8.4 %) — p(stop avant cible) 0.3855 [0.34 ; 0.44], R/R 2.314, perte reelle 22.429 % (gap inclus), EV -5.5676 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.57 %) : P(cible) 0.0 % x 51.90 % + P(rien) 61.4 % x 5.00 % ne couvrent pas P(stop) 38.6 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 10.5 %) — p(stop avant cible) 0.2822 [0.24 ; 0.33], R/R 2.314, perte reelle 22.429 % (gap inclus), EV -3.6023 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.60 %) : P(cible) 0.0 % x 51.90 % + P(rien) 71.8 % x 3.79 % ne couvrent pas P(stop) 28.2 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 12.6 %) — p(stop avant cible) 0.199 [0.16 ; 0.24], R/R 2.314, perte reelle 22.429 % (gap inclus), EV -2.2084 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.61 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.21 %) : P(cible) 0.0 % x 51.90 % + P(rien) 80.1 % x 2.81 % ne couvrent pas P(stop) 19.9 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 14.701 %) — p(stop avant cible) 0.1406 [0.11 ; 0.18], R/R 2.314, perte reelle 22.429 % (gap inclus), EV -1.3702 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.71 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.37 %) : P(cible) 0.0 % x 51.90 % + P(rien) 85.9 % x 2.07 % ne couvrent pas P(stop) 14.1 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 16.801 %) — p(stop avant cible) 0.1101 [0.08 ; 0.15], R/R 2.314, perte reelle 22.429 % (gap inclus), EV -1.002 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 16.81 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.00 %) : P(cible) 0.0 % x 51.90 % + P(rien) 89.0 % x 1.64 % ne couvrent pas P(stop) 11.0 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 23.101 %) — p(stop avant cible) 0.0156 [0.01 ; 0.03], R/R 2.246, perte reelle 23.101 % (gap inclus), EV -0.1339 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 23.10 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.13 %) : P(cible) 0.0 % x 51.90 % + P(rien) 98.4 % x 0.22 % ne couvrent pas P(stop) 1.6 % x 23.10 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 25.201 %) — p(stop avant cible) 0.0072 [0.00 ; 0.02], R/R 2.059, perte reelle 25.201 % (gap inclus), EV -0.1234 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 25.20 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 0.0 % x 51.90 % + P(rien) 99.3 % x 0.05 % ne couvrent pas P(stop) 0.7 % x 25.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 27.301 %) — p(stop avant cible) 0.0056 [0.00 ; 0.02], R/R 1.901, perte reelle 27.301 % (gap inclus), EV -0.076 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 27.30 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.08 %) : P(cible) 0.0 % x 51.90 % + P(rien) 99.4 % x 0.07 % ne couvrent pas P(stop) 0.6 % x 27.30 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 29.401 %) — p(stop avant cible) 0.0048 [0.00 ; 0.02], R/R 1.765, perte reelle 29.401 % (gap inclus), EV -0.0685 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 29.40 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.07 %) : P(cible) 0.0 % x 51.90 % + P(rien) 99.5 % x 0.07 % ne couvrent pas P(stop) 0.5 % x 29.40 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 31.501 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.647, perte reelle 31.501 % (gap inclus), EV 0.0941 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 31.50 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 33.601 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.544, perte reelle 33.601 % (gap inclus), EV 0.0941 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.54 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.60 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.086 | EV/share : €1.968 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 61 % | T2 38 % | T3 22 %
- Kelly (position) : f* 0.132 | ¼-Kelly 0.033 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 40.9 | bear 52.0 | side 7.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.51% → cible +1.25% / stop −2.0%, p_fill 84%, n_eff≈34.7) : P(cible|rempli) **55%** · **EV/risk -0.009** (×p_fill ; si rempli -0.02% du capital)
  - **swing** (entrée dip −1.12% → cible +2.795% / stop −4.248%, p_fill 68%, n_eff≈29.0) : P(cible|rempli) **76%** · **EV/risk +0.180** (×p_fill ; si rempli +1.13% du capital)
  - **deep** (entrée dip −1.74% → cible +3.953% / stop −6.412%, p_fill 69%, n_eff≈26.9) : P(cible|rempli) **76%** · **EV/risk +0.195** (×p_fill ; si rempli +1.81% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→70% · +2.0%→50% · +3.0%→32% · +5.0%→5% · +8.0%→1%
- Range intraday médian 4.17% (p90 6.98%) · excursion haute méd. +2.05% / basse méd. −1.64%
- Profil de vol intra : ouverture 2.674% vs midi 0.943% vs clôture 1.127% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 92% · range 8% · trend ↑0%/↓0% ; spike-down 54% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.09 ; mean-reverting — autocorr -0.036)_ ; drift intra méd. -0.194% ; recovery-V 23%
- **σ réalisé intraday** 2.742% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 60% / whipsaw 33%
- POC intraday (dernière séance, temps-au-prix) : 1151.1575 (VA 1148.5825–1154.2475 ; dernier close 1152.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 17% · rebond 64% · **stop −2.8%** sous le fill (sous le bruit) · cible +1.5% · R/R 0.54 (high win-rate)
- Gaps overnight (n=159) : méd. 0.25% · baisse 31% (gap-down >1% 10% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.7% (p90 −1.74%) · haut méd +0.57% · range méd 1.39%
- Excursion ouverture 15min (n=160) : bas méd −0.91% (p90 −2.0%) · haut méd +0.67% · range méd 1.8%
- Excursion ouverture 30min (n=160) : bas méd −0.93% (p90 −2.19%) · haut méd +0.88% · range méd 2.07%
- Excursion ouverture 60min (n=160) : bas méd −0.97% (p90 −2.62%) · haut méd +1.0% · range méd 2.24%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1152.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 71% (117/159) · gap 21% · délai 0.4min · rebond 53% (61/117) (MFE +1.1%)
   - −1.0% : fill 30min 40% · séance 65% (108/159) · gap 10% · délai 5.9min · rebond 59% (61/108) (MFE +1.27%)
   - −1.5% : fill 30min 28% · séance 54% (88/159) · gap 6% · délai 24.4min · rebond 62% (50/88) (MFE +1.36%)
   - −2.0% : fill 30min 18% · séance 40% (74/159) · gap 5% · délai 33.7min · rebond 66% (46/74) (MFE +1.58%)
   - −3.0% : fill 30min 8% · séance 24% (46/159) · gap 3% · délai 120.4min · rebond 58% (27/46) (MFE +1.31%)
   - −4.0% : fill 30min 3% · séance 17% (28/159) · gap 1% · délai 245.4min · rebond 64% (16/28) (MFE +1.5%)
   - −5.0% : fill 30min 1% · séance 9% (16/159) · gap 1% · délai 293.4min · rebond 56% (8/16) (MFE +1.7%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.55% (p90 −1.61%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.44% (p90 −1.76%) → stop au-delà de −1.31% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.28% (p90 −1.77%) → stop au-delà de −1.25% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=533 jambes) : jambe baissière méd −1.07% (p90 −2.47%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (48 séances) :
      · −1.0% : fill 94% (46/48) · rebond 65% (27/46)
      · −2.0% : fill 80% (38/48) · rebond 66% (25/38)
      · −3.0% : fill 53% (26/48) · rebond 63% (16/26)
      · −4.0% : fill 41% (16/48) · rebond 75% (11/16)
      · −5.0% : fill 22% (9/48) · rebond 83% (7/9)
   - **flat** (47 séances) :
      · −1.0% : fill 67% (34/47) · rebond 64% (21/34)
      · −2.0% : fill 24% (17/47) · rebond 72% (10/17)
      · −3.0% : fill 16% (10/47) · rebond 55% (5/10)
      · −4.0% : fill 14% (8/47) · rebond 36% (2/8)
      · −5.0% : fill 9% (6/47) · rebond 22% (1/6)
   - **gap-up** (64 séances) :
      · −1.0% : fill 48% (28/64) · rebond 48% (13/28)
      · −2.0% : fill 30% (19/64) · rebond 63% (11/19)
      · −3.0% : fill 14% (10/64) · rebond 49% (6/10)
      · −4.0% : fill 6% (4/64) · rebond 61% (3/4)
      · −5.0% : fill 2% (1/64) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 62% si les 15 1res min sont vertes (77 cas) · 33% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:37** → P(séance verte=clôture>ouverture) 73% si début vert vs 19% si rouge (base 47% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **73%** · continue >prix actuel 44% ; creux résiduel méd -1.21% (q20 -2.72%) → **SL/trailing à −2.72%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.76% / q75 +1.81% → **scale +0.76% / runner +1.81%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **19%** (continue à baisser 59%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.7%** (au-delà de la MAE q10 -3.7%), cible rebond +0.95% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.61% .. +3.27%] · haut q95 +3.75% · bas q05 -3.11%
   - 60min (n=160) : retour [-2.78% .. +3.22%] · haut q95 +4.4% · bas q05 -3.85%
   - 2h (n=160) : retour [-3.2% .. +3.04%] · haut q95 +4.4% · bas q05 -4.48%
   - 4h (n=160) : retour [-3.4% .. +3.3%] · haut q95 +4.87% · bas q05 -4.63%
   - 6h (n=160) : retour [-4.15% .. +3.3%] · haut q95 +4.95% · bas q05 -5.04%
   - session (n=160) : retour [-5.21% .. +3.79%] · haut q95 +5.07% · bas q05 -5.93%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.31%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 45.6  _(neutre)_
- **ADX** : 21.5  _(pas de tendance nette)_
- **MACD** : hist -1.413  _(bearish_recent)_
- **BB** : %B 0.47 · largeur 13.8%
- **ATR** : 48.53 (15.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.141  _(distribution)_
- **Vol ratio** : 0.53  _(volume atone)_
- **Choppiness** : 66.5  _(marche en range (choppy))_
- **MA** : MA20 1159.78 · MA50 1094.02 · MA200 1417.7  _(prix < MA20)_
- **Dist MA** : MA20 -0.4% · MA50 +5.6% · MA200 -18.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (824783 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
