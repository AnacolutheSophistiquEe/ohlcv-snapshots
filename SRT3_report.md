# SRT3

**Generated** : 2026-08-24T21:37:17.683167+00:00  
**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €243.10  

> 🟡 **WAIT-FOR-DIP** — spot +4.5 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €243.10 (+4.5% vs entrée) · entrée €232.74 · stop €225.19 · T1 €238.87 · R/R 0.81  
> ↳ P(T1 av. stop) 66 % · EV/risk 0.135 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.070 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €231.52–€233.97 (mid €232.74)
- Spot actuel : €243.10 (+4.5% au-dessus de la zone — repli à attendre)
- Stop : €225.19 (stop swing_plan-based (-7.37%))
- Targets : T1 €238.87 · R/R 0.81 | T2 €245.00 · R/R 1.62 | T3 €251.12 · R/R 2.43
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €225.19


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.18 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (7.37 %)** : le gap seul le franchit 0.471 % des séances (6 fois sur 1274).
   - exécution **1.659 pt plus bas** dans le cas TYPIQUE (médiane), 4.718 au p90, **6.835 au pire**
   - perte réelle **9.643 %** en moyenne _(tirée par la queue)_, jusqu'à **14.205 %** — au lieu des 7.37 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0107 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.616 % | p01 -3.24 % | pire -14.205 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0368** [0.0159 ; 0.0729] _(largeur 5.7 pt, n_eff 173.1)_
   - swing : **0.3494** [0.3006 ; 0.4007] _(largeur 10.0 pt, n_eff 345.8)_
   - deep : **0.4816** [0.4293 ; 0.5342] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (45.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-4.12 %** | CVaR **-6.6 %** | vol 2.85 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.0 % vs -9.25 % si l'on extrapolait par √5 _(rapport 1.081 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0636** (β de hausse 1.1723, asymétrie 0.9073) vs GDAXI — 602 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.343× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 235.55 sur atr_grid (1.0 ATR, 3.106 %) — p(stop avant cible) 0.5198 [0.47 ; 0.57], R/R 0.469, perte reelle 7.038 % (gap inclus), CVaR 3.149 %, EV -2.0871 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.0899 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.520, borne haute 0.572 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 0.47 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 3.15 % > budget 3.00 %
- Budget de queue : **3.0 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.212 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 42.8 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
   - ⚠ budget **borne** (brut 1.89 %) : les bornes sont un choix declare, pas une mesure.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.659 %) — p(stop avant cible) 0.4337 [0.38 ; 0.49], R/R 0.415, perte reelle 7.948 % (gap inclus), EV -1.6652 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 4.69 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.67 %) : P(cible) 54.6 % x 3.30 % + P(rien) 2.0 % x -0.96 % ne couvrent pas P(stop) 43.4 % x 7.95 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.48 ATR (stop 9.669 %) — p(stop avant cible) 0.174 [0.14 ; 0.22], R/R 0.273, perte reelle 12.088 % (gap inclus), EV -0.4586 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 9.67 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.46 %) : P(cible) 66.9 % x 3.30 % + P(rien) 15.7 % x -3.57 % ne couvrent pas P(stop) 17.4 % x 12.09 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 7.48 ATR (stop 25.19 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.131, perte reelle 25.19 % (gap inclus), EV 0.179 % — **REFUSE**
      - refuse : R/R 0.13 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.19 % > budget 3.00 %
   - ⚪ atr_grid a 1.0 ATR (stop 3.106 %) — p(stop avant cible) 0.5198 [0.47 ; 0.57], R/R 0.469, perte reelle 7.038 % (gap inclus), EV -2.0871 % — **REFUSE**
      - refuse : p_stop_first 0.520, borne haute 0.572 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.47 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 3.15 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.09 %) : P(cible) 47.6 % x 3.30 % + P(rien) 0.4 % x 0.19 % ne couvrent pas P(stop) 52.0 % x 7.04 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 3.882 %) — p(stop avant cible) 0.4659 [0.41 ; 0.52], R/R 0.43, perte reelle 7.669 % (gap inclus), EV -1.8542 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 3.92 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.85 %) : P(cible) 52.3 % x 3.30 % + P(rien) 1.1 % x -0.60 % ne couvrent pas P(stop) 46.6 % x 7.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 6.211 %) — p(stop avant cible) 0.321 [0.27 ; 0.37], R/R 0.356, perte reelle 9.276 % (gap inclus), EV -1.0394 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 6.23 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.04 %) : P(cible) 62.2 % x 3.30 % + P(rien) 5.7 % x -2.00 % ne couvrent pas P(stop) 32.1 % x 9.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.48 ATR (stop 8.628 %) — p(stop avant cible) 0.2137 [0.17 ; 0.26], R/R 0.293, perte reelle 11.278 % (gap inclus), EV -0.6536 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 8.63 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.65 %) : P(cible) 66.1 % x 3.30 % + P(rien) 12.5 % x -3.40 % ne couvrent pas P(stop) 21.4 % x 11.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 10.87 %) — p(stop avant cible) 0.1461 [0.11 ; 0.19], R/R 0.232, perte reelle 14.205 % (gap inclus), EV -0.574 % — **REFUSE**
      - refuse : R/R 0.23 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 10.87 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.57 %) : P(cible) 67.0 % x 3.30 % + P(rien) 18.4 % x -3.84 % ne couvrent pas P(stop) 14.6 % x 14.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 12.423 %) — p(stop avant cible) 0.0937 [0.07 ; 0.13], R/R 0.232, perte reelle 14.205 % (gap inclus), EV -0.1698 % — **REFUSE**
      - refuse : R/R 0.23 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.42 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.17 %) : P(cible) 67.2 % x 3.30 % + P(rien) 23.4 % x -4.52 % ne couvrent pas P(stop) 9.4 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 13.976 %) — p(stop avant cible) 0.0659 [0.04 ; 0.10], R/R 0.232, perte reelle 14.205 % (gap inclus), EV -0.0031 % — **REFUSE**
      - refuse : R/R 0.23 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.98 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.00 %) : P(cible) 67.2 % x 3.30 % + P(rien) 26.2 % x -4.91 % ne couvrent pas P(stop) 6.6 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 15.529 %) — p(stop avant cible) 0.0375 [0.02 ; 0.06], R/R 0.213, perte reelle 15.529 % (gap inclus), EV 0.0518 % — **REFUSE**
      - refuse : R/R 0.21 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.53 % > budget 3.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 17.081 %) — p(stop avant cible) 0.0133 [0.00 ; 0.03], R/R 0.193, perte reelle 17.081 % (gap inclus), EV 0.1503 % — **REFUSE**
      - refuse : R/R 0.19 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.08 % > budget 3.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 18.634 %) — p(stop avant cible) 0.0116 [0.00 ; 0.03], R/R 0.177, perte reelle 18.634 % (gap inclus), EV 0.139 % — **REFUSE**
      - refuse : R/R 0.18 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.63 % > budget 3.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 20.187 %) — p(stop avant cible) 0.0103 [0.00 ; 0.03], R/R 0.163, perte reelle 20.187 % (gap inclus), EV 0.1304 % — **REFUSE**
      - refuse : R/R 0.16 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.19 % > budget 3.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 21.74 %) — p(stop avant cible) 0.0058 [0.00 ; 0.02], R/R 0.152, perte reelle 21.74 % (gap inclus), EV 0.1561 % — **REFUSE**
      - refuse : R/R 0.15 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.74 % > budget 3.00 %
   - 🟢 grid_snapped a 7.48 ATR (stop 24.15 %) — p(stop avant cible) 0.0028 [0.00 ; 0.01], R/R 0.137, perte reelle 24.15 % (gap inclus), EV 0.1748 % — **REFUSE**
      - refuse : R/R 0.14 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.15 % > budget 3.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : -0.018 | EV/share : €-0.138 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 29 % | T3 15 %
- Kelly (position) : f* 0.001 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 15.4 | bear 7.7 | side 76.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 486.0 (= 2 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.939% → cible +1.177% / stop −1.5%, p_fill 38%, n_eff≈15.9) : P(cible|rempli) **55%** · **EV/risk +0.113** (×p_fill ; si rempli +0.45% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=12, n_eff=8))
  - **deep** : indisponible (échantillon insuffisant (n=10, n_eff=8))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→78% · +2.0%→48% · +3.0%→25% · +5.0%→4% · +8.0%→0%
- Range intraday médian 3.33% (p90 6.3%) · excursion haute méd. +1.89% / basse méd. −1.47%
- Profil de vol intra : ouverture 2.035% vs midi 0.845% vs clôture 0.994% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 92% · range 8% · trend ↑0%/↓0% ; spike-down 51% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.098 ; neutre — autocorr -0.021)_ ; drift intra méd. 0.147% ; recovery-V 26%
- **σ réalisé intraday** 2.532% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 68% / bas 70% / whipsaw 39%
- POC intraday (dernière séance, temps-au-prix) : 244.5125 (VA 243.7725–245.6225 ; dernier close 246.7)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 58% · rebond 72% · **stop −2.11%** sous le fill (sous le bruit) · cible +1.57% · R/R 0.74 (high win-rate)
- Gaps overnight (n=159) : méd. 0.06% · baisse 49% (gap-down >1% 13% · >2% 3%)
- Excursion ouverture 5min (n=160) : bas méd −0.44% (p90 −1.81%) · haut méd +0.53% · range méd 1.21%
- Excursion ouverture 15min (n=160) : bas méd −0.57% (p90 −1.91%) · haut méd +0.64% · range méd 1.49%
- Excursion ouverture 30min (n=160) : bas méd −0.59% (p90 −2.04%) · haut méd +0.8% · range méd 1.71%
- Excursion ouverture 60min (n=160) : bas méd −0.75% (p90 −2.45%) · haut méd +0.82% · range méd 1.83%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 246.7 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 55% · séance 76% (125/159) · gap 25% · délai 0.2min · rebond 53% (64/125) (MFE +1.16%)
   - −1.0% : fill 30min 44% · séance 65% (106/159) · gap 13% · délai 1.6min · rebond 58% (59/106) (MFE +1.16%)
   - −1.5% : fill 30min 34% · séance 58% (97/159) · gap 6% · délai 5.0min · rebond 72% (62/97) (MFE +1.57%)
   - −2.0% : fill 30min 18% · séance 40% (75/159) · gap 3% · délai 94.7min · rebond 60% (45/75) (MFE +1.61%)
   - −3.0% : fill 30min 6% · séance 18% (40/159) · gap 1% · délai 184.6min · rebond 62% (24/40) (MFE +1.94%)
   - −4.0% : fill 30min 3% · séance 9% (21/159) · gap 0% · délai 49.4min · rebond 76% (16/21) (MFE +2.62%)
   - −5.0% : fill 30min 1% · séance 6% (12/159) · gap 0% · délai 94.0min · rebond 65% (9/12) (MFE +2.48%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.44% (p90 −1.97%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.17% (p90 −2.24%) → stop au-delà de −1.22% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −2.59%) → stop au-delà de −1.45% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=446 jambes) : jambe baissière méd −1.04% (p90 −2.34%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (69 séances) :
      · −1.0% : fill 82% (58/69) · rebond 68% (36/58)
      · −2.0% : fill 53% (43/69) · rebond 53% (26/43)
      · −3.0% : fill 30% (28/69) · rebond 57% (16/28)
      · −4.0% : fill 12% (15/69) · rebond 71% (11/15)
      · −5.0% : fill 6% (7/69) · rebond 92% (6/7)
   - **flat** (33 séances) :
      · −1.0% : fill 68% (21/33) · rebond 54% (10/21)
      · −2.0% : fill 47% (16/33) · rebond 62% (8/16)
      · −3.0% : fill 16% (6/33) · rebond 66% (4/6)
      · −4.0% : fill 12% (4/33) · rebond 70% (3/4)
      · −5.0% : fill 12% (4/33) · rebond 24% (2/4)
   - **gap-up** (57 séances) :
      · −1.0% : fill 47% (27/57) · rebond 45% (13/27)
      · −2.0% : fill 22% (16/57) · rebond 77% (11/16)
      · −3.0% : fill 6% (6/57) · rebond 78% (4/6)
      · −4.0% : fill 4% (2/57) · rebond 100% (2/2)
      · −5.0% : fill 3% (1/57) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 57% si les 15 1res min sont vertes (87 cas) · 37% si rouges (73 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **8min** → P(séance verte=clôture>ouverture) 57% si début vert vs 38% si rouge (base 48% · écart 19 pts) ; prédictivité sature ensuite (plafond brut 268min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=85) : tient le vert **57%** · continue >prix actuel 46% ; creux résiduel méd -1.43% (q20 -2.45%) → **SL/trailing à −2.45%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.34% / q75 +2.36% → **scale +1.34% / runner +2.36%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **38%** (continue à baisser 52%) → **RÉDUIRE ~62%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.51%** (au-delà de la MAE q10 -4.51%), cible rebond +1.41% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.86% .. +2.12%] · haut q95 +2.63% · bas q05 -3.25%
   - 60min (n=160) : retour [-2.58% .. +2.34%] · haut q95 +2.83% · bas q05 -3.66%
   - 2h (n=160) : retour [-2.18% .. +2.49%] · haut q95 +2.94% · bas q05 -3.82%
   - 4h (n=160) : retour [-2.52% .. +2.28%] · haut q95 +3.26% · bas q05 -3.83%
   - 6h (n=160) : retour [-2.57% .. +2.94%] · haut q95 +3.61% · bas q05 -3.92%
   - session (n=160) : retour [-3.59% .. +4.13%] · haut q95 +5.59% · bas q05 -4.59%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.33%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 65.1  _(momentum haussier)_
- **ADX** : 14.1  _(pas de tendance nette)_
- **MACD** : hist 1.524  _(pas de croisement recent)_
- **BB** : %B 0.82 · largeur 14.1%
- **ATR** : 7.55 (26.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.065  _(distribution)_
- **Vol ratio** : 0.86  _(volume normal)_
- **Choppiness** : 47.8  _(transition)_
- **MA** : MA20 232.67 · MA50 230.21 · MA200 232.03  _(prix > MA20)_
- **Dist MA** : MA20 +4.5% · MA50 +5.6% · MA200 +4.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (843234 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
