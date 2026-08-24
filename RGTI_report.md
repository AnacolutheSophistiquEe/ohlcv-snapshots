# RGTI

**Generated** : 2026-08-24T00:28:54.689352+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $17.91  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $17.91 (+3.8% vs entrée) · entrée $17.25 · stop $16.90 · T1 $17.85 · R/R 1.71  
> ↳ P(T1 av. stop) 12 % _(réel 5 s)_ · EV/risk -0.118 _(réel 5 s)_ (GBM 0.276) · ¼-Kelly 0.041 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $17.13–$17.37 (mid $17.25)
- Spot actuel : $17.91 (+3.8% au-dessus de la zone — repli à attendre)
- Stop : $16.90 (stop swing_plan-based (-14.45%))
- Targets : T1 $17.85 · R/R 1.71 | T2 $18.45 · R/R 3.43 | T3 $19.05 · R/R 5.14
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.90


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.29 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (14.45 %)** : le gap seul le franchit 0.319 % des séances (4 fois sur 1254).
   - exécution **1.836 pt plus bas** dans le cas TYPIQUE (médiane), 12.774 au p90, **16.763 au pire**
   - perte réelle **19.597 %** en moyenne _(tirée par la queue)_, jusqu'à **31.213 %** — au lieu des 14.45 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0164 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.083 % | p01 -8.97 % | pire -31.213 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3005** [0.2359 ; 0.3717] _(largeur 13.6 pt, n_eff 173.1)_
   - swing : **0.5548** [0.5021 ; 0.6066] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.5544** [0.5017 ; 0.6062] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (45.7 pt), swing (49.3 pt), deep (47.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-8.8 %** | CVaR **-10.8 %** | vol 6.87 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 16.23 % contre 6.45 % aujourd'hui, rapport 2.52)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -21.75 % vs -22.11 % si l'on extrapolait par √5 _(rapport 0.984 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8381** (β de hausse 1.9836, asymétrie 0.9267) vs IWM — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.663× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 16.7782 sur atr_grid (1.0 ATR, 6.319 %) — p(stop avant cible) 0.7371 [0.69 ; 0.78], R/R 4.155, perte reelle 11.222 % (gap inclus), CVaR 6.405 %, EV -2.51 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.8731 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 6.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.737, borne haute 0.781 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 6.41 % > budget 4.41 %
- Budget de queue : **4.41 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.212 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 42.8 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 9.479 %) — p(stop avant cible) 0.6456 [0.59 ; 0.69], R/R 3.207, perte reelle 14.538 % (gap inclus), EV -2.6401 % — **REFUSE**
      - refuse : cible atteinte seulement 7.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.646, borne haute 0.695 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 9.52 % > budget 4.41 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.64 %) : P(cible) 7.0 % x 46.62 % + P(rien) 28.4 % x 12.23 % ne couvrent pas P(stop) 64.6 % x 14.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 2.44 ATR (stop 18.729 %) — p(stop avant cible) 0.2904 [0.24 ; 0.34], R/R 1.494, perte reelle 31.213 % (gap inclus), EV -1.7386 % — **REFUSE**
      - refuse : cible atteinte seulement 9.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.49 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.74 % > budget 4.41 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.74 %) : P(cible) 9.5 % x 46.62 % + P(rien) 61.5 % x 4.73 % ne couvrent pas P(stop) 29.0 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.04 ATR (stop 22.525 %) — p(stop avant cible) 0.1656 [0.13 ; 0.21], R/R 1.494, perte reelle 31.213 % (gap inclus), EV 0.8297 % — **REFUSE**
      - refuse : cible atteinte seulement 9.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.49 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.53 % > budget 4.41 %
   - ⚪ swing_based a 4.42 ATR (stop 31.271 %) — p(stop avant cible) 0.052 [0.03 ; 0.08], R/R 1.491, perte reelle 31.271 % (gap inclus), EV 2.5061 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.49 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.27 % > budget 4.41 %
   - 🟢 support a 4.75 ATR (stop 33.357 %) — p(stop avant cible) 0.0405 [0.02 ; 0.07], R/R 1.398, perte reelle 33.357 % (gap inclus), EV 2.5754 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.40 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.36 % > budget 4.41 %
   - ⚪ atr_grid a 1.0 ATR (stop 6.319 %) — p(stop avant cible) 0.7371 [0.69 ; 0.78], R/R 4.155, perte reelle 11.222 % (gap inclus), EV -2.51 % — **REFUSE**
      - refuse : cible atteinte seulement 6.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.737, borne haute 0.781 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 6.41 % > budget 4.41 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.51 %) : P(cible) 6.5 % x 46.62 % + P(rien) 19.8 % x 13.85 % ne couvrent pas P(stop) 73.7 % x 11.22 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 7.899 %) — p(stop avant cible) 0.6919 [0.64 ; 0.74], R/R 3.663, perte reelle 12.728 % (gap inclus), EV -2.4702 % — **REFUSE**
      - refuse : cible atteinte seulement 6.9 % du temps (< 15 %) meme a 10 seances : le R/R de 3.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.692, borne haute 0.739 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 7.96 % > budget 4.41 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.47 %) : P(cible) 6.9 % x 46.62 % + P(rien) 23.9 % x 13.06 % ne couvrent pas P(stop) 69.2 % x 12.73 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 12.639 %) — p(stop avant cible) 0.5165 [0.46 ; 0.57], R/R 2.648, perte reelle 17.61 % (gap inclus), EV -1.992 % — **REFUSE**
      - refuse : cible atteinte seulement 7.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.516, borne haute 0.569 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 12.66 % > budget 4.41 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.99 %) : P(cible) 7.5 % x 46.62 % + P(rien) 40.8 % x 8.78 % ne couvrent pas P(stop) 51.6 % x 17.61 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 25.277 %) — p(stop avant cible) 0.1178 [0.09 ; 0.15], R/R 1.494, perte reelle 31.213 % (gap inclus), EV 1.7208 % — **REFUSE**
      - refuse : cible atteinte seulement 9.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.49 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.28 % > budget 4.41 %
   - ⚪ atr_grid a 6.0 ATR (stop 37.916 %) — p(stop avant cible) 0.0186 [0.01 ; 0.04], R/R 1.23, perte reelle 37.916 % (gap inclus), EV 2.6181 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.23 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.92 % > budget 4.41 %
   - ⚪ atr_grid a 6.5 ATR (stop 41.075 %) — p(stop avant cible) 0.0101 [0.00 ; 0.03], R/R 1.135, perte reelle 41.075 % (gap inclus), EV 2.7094 % — **REFUSE**
      - refuse : cible atteinte seulement 10.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.07 % > budget 4.41 %
   - ⚪ atr_grid a 7.0 ATR (stop 44.235 %) — p(stop avant cible) 0.0072 [0.00 ; 0.02], R/R 1.054, perte reelle 44.235 % (gap inclus), EV 2.6951 % — **REFUSE**
      - refuse : cible atteinte seulement 10.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.05 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.24 % > budget 4.41 %
   - ⚪ atr_grid a 7.5 ATR (stop 47.395 %) — p(stop avant cible) 0.005 [0.00 ; 0.02], R/R 0.984, perte reelle 47.395 % (gap inclus), EV 2.6872 % — **REFUSE**
      - refuse : cible atteinte seulement 10.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.98 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.39 % > budget 4.41 %
   - ⚪ atr_grid a 8.0 ATR (stop 50.554 %) — p(stop avant cible) 0.0048 [0.00 ; 0.02], R/R 0.922, perte reelle 50.554 % (gap inclus), EV 2.6754 % — **REFUSE**
      - refuse : cible atteinte seulement 10.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.92 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 50.55 % > budget 4.41 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.276 | EV/share : $0.095 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 34 % | T3 34 %
- Kelly (position) : f* 0.164 | ¼-Kelly 0.041 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 17.3 | side 77.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 287.0 (= 16 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.694% → cible +3.486% / stop −2.0%, p_fill 33%, n_eff≈14.6) : P(cible|rempli) **12%** · **EV/risk -0.118** (×p_fill ; si rempli -0.73% du capital)
  - **swing** (entrée dip −8.131% → cible +7.796% / stop −6.878%, p_fill 18%, n_eff≈12.9) : P(cible|rempli) **58%** · **EV/risk +0.051** (×p_fill ; si rempli +1.92% du capital)
  - **deep** (entrée dip −12.561% → cible +11.024% / stop −10.84%, p_fill 25%, n_eff≈14.5) : P(cible|rempli) **57%** · **EV/risk +0.081** (×p_fill ; si rempli +3.56% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→79% · +2.0%→72% · +3.0%→57% · +5.0%→42% · +8.0%→14%
- Range intraday médian 7.89% (p90 13.36%) · excursion haute méd. +4.06% / basse méd. −2.61%
- Profil de vol intra : ouverture 5.522% vs midi 1.598% vs clôture 1.838% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 22% · trend ↑0%/↓0% ; spike-down 70% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.128 ; neutre — autocorr -0.026)_ ; drift intra méd. 0.515% ; recovery-V 31%
- **σ réalisé intraday** 4.56% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 45% / whipsaw 5%
- POC intraday (dernière séance, temps-au-prix) : 17.6928 (VA 17.3518–17.9911 ; dernier close 17.895)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 44% · rebond 74% · **stop −6.28%** sous le fill (sous le bruit) · cible +2.24% · R/R 0.36 (high win-rate)
- Gaps overnight (n=159) : méd. -0.48% · baisse 58% (gap-down >1% 41% · >2% 28%)
- Excursion ouverture 5min (n=160) : bas méd −1.19% (p90 −2.84%) · haut méd +1.28% · range méd 2.63%
- Excursion ouverture 15min (n=160) : bas méd −1.44% (p90 −3.96%) · haut méd +1.88% · range méd 3.78%
- Excursion ouverture 30min (n=160) : bas méd −1.83% (p90 −4.65%) · haut méd +2.1% · range méd 4.66%
- Excursion ouverture 60min (n=160) : bas méd −2.13% (p90 −5.98%) · haut méd +2.53% · range méd 5.53%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 17.895 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 77% · séance 83% (134/159) · gap 48% · délai 0.0min · rebond 64% (86/134) (MFE +2.42%)
   - −1.0% : fill 30min 68% · séance 75% (126/159) · gap 41% · délai 0.0min · rebond 67% (81/126) (MFE +1.87%)
   - −1.5% : fill 30min 60% · séance 68% (119/159) · gap 35% · délai 0.0min · rebond 67% (78/119) (MFE +2.16%)
   - −2.0% : fill 30min 56% · séance 62% (111/159) · gap 28% · délai 0.0min · rebond 71% (76/111) (MFE +2.37%)
   - −3.0% : fill 30min 48% · séance 56% (98/159) · gap 13% · délai 1.2min · rebond 73% (71/98) (MFE +2.45%)
   - −4.0% : fill 30min 35% · séance 44% (78/159) · gap 5% · délai 6.2min · rebond 74% (57/78) (MFE +2.24%)
   - −5.0% : fill 30min 18% · séance 35% (64/159) · gap 3% · délai 25.1min · rebond 67% (48/64) (MFE +1.8%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.67% (p90 −2.2%) → stop au-delà de −1.53% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.87% (p90 −2.65%) → stop au-delà de −1.98% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.94% (p90 −2.91%) → stop au-delà de −2.04% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1171 jambes) : jambe baissière méd −1.29% (p90 −3.14%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (84 séances) :
      · −1.0% : fill 96% (82/84) · rebond 61% (49/82)
      · −2.0% : fill 85% (77/84) · rebond 70% (52/77)
      · −3.0% : fill 81% (71/84) · rebond 68% (49/71)
      · −4.0% : fill 67% (58/84) · rebond 71% (41/58)
      · −5.0% : fill 54% (49/84) · rebond 65% (37/49)
   - **flat** (16 séances) :
      · −1.0% : fill 96% (15/16) · rebond 95% (13/15)
      · −2.0% : fill 71% (12/16) · rebond 85% (10/12)
      · −3.0% : fill 48% (7/16) · rebond 90% (5/7)
      · −4.0% : fill 32% (6/16) · rebond 85% (4/6)
      · −5.0% : fill 20% (5/16) · rebond 87% (3/5)
   - **gap-up** (59 séances) :
      · −1.0% : fill 41% (29/59) · rebond 66% (19/29)
      · −2.0% : fill 29% (22/59) · rebond 63% (14/22)
      · −3.0% : fill 24% (20/59) · rebond 89% (17/20)
      · −4.0% : fill 15% (14/59) · rebond 84% (12/14)
      · −5.0% : fill 12% (10/59) · rebond 68% (8/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 71% si les 15 1res min sont vertes (80 cas) · 29% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **51min** → P(séance verte=clôture>ouverture) 89% si début vert vs 15% si rouge (base 52% · écart 73 pts) ; prédictivité sature ensuite (plafond brut 91min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **89%** · continue >prix actuel 52% ; creux résiduel méd -2.13% (q20 -3.51%) → **SL/trailing à −3.51%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.53% / q75 +5.77% → **scale +2.53% / runner +5.77%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **15%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.35%** (au-delà de la MAE q10 -5.35%), cible rebond +2.07% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.17% .. +4.96%] · haut q95 +6.49% · bas q05 -6.26%
   - 60min (n=160) : retour [-5.56% .. +6.35%] · haut q95 +6.68% · bas q05 -6.83%
   - 2h (n=160) : retour [-6.39% .. +6.97%] · haut q95 +9.12% · bas q05 -7.59%
   - 4h (n=160) : retour [-7.13% .. +8.07%] · haut q95 +9.21% · bas q05 -7.87%
   - 6h (n=160) : retour [-7.45% .. +8.87%] · haut q95 +10.37% · bas q05 -8.62%
   - session (n=160) : retour [-7.26% .. +9.29%] · haut q95 +10.63% · bas q05 -8.63%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 7.4)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **30%**. Lecture précoce 30 min : signature présente → 14% vs absente 6% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.25% (p75 1.66% / p90 2.45%) · ~4.39 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **82%** (reprise méd 15.0 min, n=47)
   - −1.0% → **83%** (reprise méd 35.0 min, n=29)
   - −1.5% → **84%** (reprise méd 94.96 min, n=17)
   - −2.0% → **86%** (reprise méd 54.27 min, n=9)
   - −3.0% → **67%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.45%** (p90, défaut prudent ; serré/agressif −1.66%) ; extension open→close méd +8.3% (q75 +9.62% / q95 +9.99%), MFE méd +9.65% / q90 +11.14%
   - Échelle scale-out : +9.65% (33%) / +10.43% (33%) / +11.14% (34%)
- **DÉSARMER** : repli > **−2.45%** depuis le plus-haut = décay → P(retournement) **23%** (préavis méd 141.49 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +11.14% : P(retournement après) 0% (mèche méd 1.88%)
- **CONTEXTE** : la dernière heure tient les gains 67% du temps (retour médian dernière heure +0.16%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 59.6  _(momentum haussier)_
- **ADX** : 16.7  _(pas de tendance nette)_
- **MACD** : hist 0.074  _(pas de croisement recent)_
- **BB** : %B 0.67 · largeur 37.5%
- **ATR** : 1.13 (11.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.084  _(accumulation)_
- **Vol ratio** : 1.15  _(volume normal)_
- **Choppiness** : 55.1  _(transition)_
- **MA** : MA20 16.84 · MA50 17.43 · MA200 20.05  _(prix > MA20)_
- **Dist MA** : MA20 +6.3% · MA50 +2.8% · MA200 -10.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (825170 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
