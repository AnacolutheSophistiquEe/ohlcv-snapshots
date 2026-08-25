# CEG

**Generated** : 2026-08-25T00:30:33.488350+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $273.43  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $273.43 (+0.8% vs entrée) · entrée $271.37 · stop $267.30 · T1 $275.49 · R/R 1.01  
> ↳ P(T1 av. stop) 24 % _(réel 5 s)_ · EV/risk -0.186 _(réel 5 s)_ (GBM -0.014) · ¼-Kelly 0.009 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -44 % hors [0,100] (R² max 0.96). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $270.71–$272.03 (mid $271.37)
- Spot actuel : $273.43 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : $267.30 (stop swing_plan-based (-5.15%))
- Targets : T1 $275.49 · R/R 1.01 | T2 $278.36 · R/R 1.72 | T3 $281.23 · R/R 2.42
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $267.30


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.00 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (5.15 %)** : le gap seul le franchit 0.694 % des séances (8 fois sur 1152).
   - exécution **1.356 pt plus bas** dans le cas TYPIQUE (médiane), 6.54 au p90, **10.674 au pire**
   - perte réelle **7.875 %** en moyenne _(tirée par la queue)_, jusqu'à **15.824 %** — au lieu des 5.15 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0189 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 8 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.823 % | p01 -4.438 % | pire -15.824 % _(sur 1152 séances)_
- **P(stop avant cible)** _(source : daily, 1153 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0566** [0.0293 ; 0.0986] _(largeur 6.9 pt, n_eff 173.1)_
   - swing : **0.4265** [0.3751 ; 0.4791] _(largeur 10.4 pt, n_eff 345.3)_
   - deep : **0.5016** [0.449 ; 0.5541] _(largeur 10.5 pt, n_eff 345.3)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 22.0 observations effectives », dont la borne haute a 95 % vaut environ 13.6 %.
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 21.9 observations effectives », dont la borne haute a 95 % vaut environ 13.7 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (35.3 pt), swing (39.2 pt), deep (34.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-4.5 %** | CVaR **-6.9 %** | vol 3.11 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 5.66 % contre 2.88 % aujourd'hui, rapport 1.97)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.64 % vs -9.59 % si l'on extrapolait par √5 _(rapport 1.004 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1874** (β de hausse 1.1939, asymétrie 0.9945) vs SPY — 529 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 249.531 sur atr_grid (2.5 ATR, 8.74 %) — p(stop avant cible) 0.354 [0.30 ; 0.41], R/R 2.885, perte reelle 12.871 % (gap inclus), CVaR 8.747 %, EV -1.6881 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 1.1 ATR (stop 5.984 %) — p(stop avant cible) 0.5366 [0.48 ; 0.59], R/R 3.98, perte reelle 9.329 % (gap inclus), EV -2.0293 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.537, borne haute 0.589 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.03 %) : P(cible) 0.4 % x 37.13 % + P(rien) 45.9 % x 6.14 % ne couvrent pas P(stop) 53.7 % x 9.33 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 support a 4.72 ATR (stop 18.649 %) — p(stop avant cible) 0.0391 [0.02 ; 0.06], R/R 1.991, perte reelle 18.649 % (gap inclus), EV 0.0128 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 18.65 % > budget 12.00 %
      - ⚠ support DETECTE a 0.86 ATR du spot — compartiment <1, mesure a 47.2 % de casse (IC clusterise [0.436 ; 0.506] sur 1081 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ grid_snapped a 1.1 ATR (stop 4.897 %) — p(stop avant cible) 0.5821 [0.53 ; 0.63], R/R 4.906, perte reelle 7.568 % (gap inclus), EV -1.4457 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 4.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.582, borne haute 0.633 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.45 %) : P(cible) 0.4 % x 37.13 % + P(rien) 41.4 % x 6.78 % ne couvrent pas P(stop) 58.2 % x 7.57 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 6.992 %) — p(stop avant cible) 0.4526 [0.40 ; 0.51], R/R 3.312, perte reelle 11.211 % (gap inclus), EV -2.0192 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.02 %) : P(cible) 0.4 % x 37.13 % + P(rien) 54.3 % x 5.34 % ne couvrent pas P(stop) 45.3 % x 11.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 8.74 %) — p(stop avant cible) 0.354 [0.30 ; 0.41], R/R 2.885, perte reelle 12.871 % (gap inclus), EV -1.6881 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.69 %) : P(cible) 0.4 % x 37.13 % + P(rien) 64.2 % x 4.23 % ne couvrent pas P(stop) 35.4 % x 12.87 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 10.489 %) — p(stop avant cible) 0.2807 [0.24 ; 0.33], R/R 2.346, perte reelle 15.824 % (gap inclus), EV -1.7253 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.73 %) : P(cible) 0.4 % x 37.13 % + P(rien) 71.5 % x 3.58 % ne couvrent pas P(stop) 28.1 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 12.237 %) — p(stop avant cible) 0.2169 [0.18 ; 0.26], R/R 2.346, perte reelle 15.824 % (gap inclus), EV -0.992 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.24 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.99 %) : P(cible) 0.5 % x 37.13 % + P(rien) 77.8 % x 2.91 % ne couvrent pas P(stop) 21.7 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 13.985 %) — p(stop avant cible) 0.1617 [0.13 ; 0.20], R/R 2.346, perte reelle 15.824 % (gap inclus), EV -0.5003 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.99 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.50 %) : P(cible) 0.5 % x 37.13 % + P(rien) 83.4 % x 2.26 % ne couvrent pas P(stop) 16.2 % x 15.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 grid_snapped a 4.72 ATR (stop 17.562 %) — p(stop avant cible) 0.0543 [0.03 ; 0.08], R/R 2.114, perte reelle 17.562 % (gap inclus), EV 0.0042 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 17.56 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 20.977 %) — p(stop avant cible) 0.015 [0.01 ; 0.03], R/R 1.77, perte reelle 20.977 % (gap inclus), EV 0.1445 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 20.98 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 22.725 %) — p(stop avant cible) 0.0107 [0.00 ; 0.03], R/R 1.634, perte reelle 22.725 % (gap inclus), EV 0.1548 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 22.72 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 24.473 %) — p(stop avant cible) 0.0085 [0.00 ; 0.02], R/R 1.517, perte reelle 24.473 % (gap inclus), EV 0.1776 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.52 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.47 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 26.221 %) — p(stop avant cible) 0.0072 [0.00 ; 0.02], R/R 1.416, perte reelle 26.221 % (gap inclus), EV 0.174 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.42 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.22 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 27.969 %) — p(stop avant cible) 0.0056 [0.00 ; 0.02], R/R 1.327, perte reelle 27.969 % (gap inclus), EV 0.1727 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.33 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.97 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : -0.014 | EV/share : $-0.057 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 48 % | T2 22 % | T3 6 %
- Kelly (position) : f* 0.037 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 84.3 | bear 7.0 | side 8.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.751% → cible +1.516% / stop −1.5%, p_fill 69%, n_eff≈28.1) : P(cible|rempli) **24%** · **EV/risk -0.186** (×p_fill ; si rempli -0.40% du capital)
  - **swing** (entrée dip −1.654% → cible +2.708% / stop −3.555%, p_fill 56%, n_eff≈22.0) : P(cible|rempli) **43%** · **EV/risk -0.157** (×p_fill ; si rempli -1.00% du capital)
  - **deep** (entrée dip −2.556% → cible +3.83% / stop −5.382%, p_fill 52%, n_eff≈21.9) : P(cible|rempli) **75%** · **EV/risk +0.136** (×p_fill ; si rempli +1.39% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→68% · +2.0%→38% · +3.0%→16% · +5.0%→4% · +8.0%→0%
- Range intraday médian 3.36% (p90 5.5%) · excursion haute méd. +1.44% / basse méd. −1.41%
- Profil de vol intra : ouverture 2.487% vs midi 0.665% vs clôture 0.785% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 48% · recovery-V 14%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; mean-reverting — autocorr -0.06)_ ; drift intra méd. -0.434% ; recovery-V 7%
- **σ réalisé intraday** 2.331% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 62% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 275.8521 (VA 273.1364–276.4911 ; dernier close 272.85)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 23% · rebond 44% · **stop −2.3%** sous le fill (sous le bruit) · cible +0.96% · R/R 0.42 (high win-rate)
- Gaps overnight (n=159) : méd. 0.46% · baisse 35% (gap-down >1% 15% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.6% (p90 −1.86%) · haut méd +0.86% · range méd 1.66%
- Excursion ouverture 15min (n=160) : bas méd −0.66% (p90 −2.25%) · haut méd +1.02% · range méd 2.01%
- Excursion ouverture 30min (n=160) : bas méd −0.8% (p90 −2.8%) · haut méd +1.1% · range méd 2.25%
- Excursion ouverture 60min (n=160) : bas méd −0.97% (p90 −3.05%) · haut méd +1.3% · range méd 2.61%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 272.85 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 50% · séance 67% (115/159) · gap 22% · délai 1.4min · rebond 46% (58/115) (MFE +0.94%)
   - −1.0% : fill 30min 41% · séance 56% (99/159) · gap 15% · délai 2.2min · rebond 48% (54/99) (MFE +0.96%)
   - −1.5% : fill 30min 31% · séance 40% (82/159) · gap 8% · délai 4.2min · rebond 46% (44/82) (MFE +0.8%)
   - −2.0% : fill 30min 24% · séance 36% (66/159) · gap 6% · délai 10.3min · rebond 54% (40/66) (MFE +1.07%)
   - −3.0% : fill 30min 9% · séance 23% (41/159) · gap 2% · délai 46.1min · rebond 44% (16/41) (MFE +0.96%)
   - −4.0% : fill 30min 4% · séance 12% (25/159) · gap 1% · délai 50.1min · rebond 53% (12/25) (MFE +0.97%)
   - −5.0% : fill 30min 2% · séance 6% (15/159) · gap 0% · délai 44.6min · rebond 75% (10/15) (MFE +1.27%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.31% (p90 −1.16%) → stop au-delà de −0.8% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.3% (p90 −1.02%) → stop au-delà de −0.88% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.4% (p90 −1.38%) → stop au-delà de −1.07% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=469 jambes) : jambe baissière méd −1.09% (p90 −2.62%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (53 séances) :
      · −1.0% : fill 96% (52/53) · rebond 52% (30/52)
      · −2.0% : fill 77% (40/53) · rebond 53% (25/40)
      · −3.0% : fill 55% (28/53) · rebond 38% (12/28)
      · −4.0% : fill 37% (19/53) · rebond 53% (9/19)
      · −5.0% : fill 18% (13/53) · rebond 76% (9/13)
   - **flat** (29 séances) :
      · −1.0% : fill 62% (17/29) · rebond 27% (5/17)
      · −2.0% : fill 26% (9/29) · rebond 48% (3/9)
      · −3.0% : fill 17% (7/29) · rebond 21% (1/7)
      · −4.0% : fill 8% (4/29) · rebond 20% (1/4)
      · −5.0% : fill 3% (2/29) · rebond 61% (1/2)
   - **gap-up** (77 séances) :
      · −1.0% : fill 34% (30/77) · rebond 51% (19/30)
      · −2.0% : fill 18% (17/77) · rebond 58% (12/17)
      · −3.0% : fill 8% (6/77) · rebond 76% (3/6)
      · −4.0% : fill 1% (2/77) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/77) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 63% si les 15 1res min sont vertes (93 cas) · 24% si rouges (67 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:23** → P(séance verte=clôture>ouverture) 82% si début vert vs 8% si rouge (base 46% · écart 74 pts) ; prédictivité sature ensuite (plafond brut 194min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=85) : tient le vert **82%** · continue >prix actuel 45% ; creux résiduel méd -1.01% (q20 -1.87%) → **SL/trailing à −1.87%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.82% / q75 +1.41% → **scale +0.82% / runner +1.41%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **8%** (continue à baisser 63%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.58%** (au-delà de la MAE q10 -2.58%), cible rebond +0.91% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.11% .. +2.29%] · haut q95 +2.63% · bas q05 -3.47%
   - 60min (n=160) : retour [-3.68% .. +2.57%] · haut q95 +3.28% · bas q05 -4.68%
   - 2h (n=160) : retour [-3.72% .. +2.9%] · haut q95 +3.97% · bas q05 -4.78%
   - 4h (n=160) : retour [-3.56% .. +3.35%] · haut q95 +4.16% · bas q05 -4.83%
   - 6h (n=160) : retour [-4.25% .. +3.15%] · haut q95 +4.47% · bas q05 -4.87%
   - session (n=160) : retour [-3.99% .. +3.29%] · haut q95 +4.5% · bas q05 -4.87%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 4.4% / strong 1.9%) · base = 10 séances trend-up (n_eff 6.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 13% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.05% (p75 1.33% / p90 1.45%) · ~1.45 replis/séance, durée méd 90.1 min. P(nouveau plus-haut après repli) :
   - −0.5% → **65%** (reprise méd 23.89 min, n=22)
   - −1.0% → **74%** (reprise méd 54.64 min, n=10)
- **RIDER — climb (trail + cibles)** : trail **−1.45%** (p90, défaut prudent ; serré/agressif −1.33%) ; extension open→close méd +3.33% (q75 +4.19% / q95 +6.07%), MFE méd +3.68% / q90 +5.35%
   - Échelle scale-out : +3.68% (33%) / +4.76% (33%) / +5.35% (34%)
- **DÉSARMER** : repli > **−1.45%** depuis le plus-haut = décay → P(retournement) **70%** (préavis méd 295.0 min, n=0) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.35% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 93% du temps (retour médian dernière heure +0.39%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict buy_bias_strong
**Options** : neutral_cautious


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 56.3  _(momentum haussier)_
- **ADX** : 17.0  _(pas de tendance nette)_
- **MACD** : hist -0.264  _(bearish_recent)_
- **BB** : %B 0.62 · largeur 10.6%
- **ATR** : 9.56 (9.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.296  _(distribution)_
- **Vol ratio** : 0.94  _(volume normal)_
- **Choppiness** : 61.7  _(transition)_
- **MA** : MA20 270.1 · MA50 263.29 · MA200 298.42  _(prix > MA20)_
- **Dist MA** : MA20 +1.2% · MA50 +3.9% · MA200 -8.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (806871 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
