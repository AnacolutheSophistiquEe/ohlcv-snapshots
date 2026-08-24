# AL2SI

**Generated** : 2026-08-24T00:11:30.850293+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €26.64  

> 🟡 **WAIT-FOR-DIP** — spot +3.5 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €26.64 (+3.5% vs entrée) · entrée €25.73 · stop €25.21 · T1 €26.36 · R/R 1.21  
> ↳ P(T1 av. stop) 28 % _(réel 5 s)_ · EV/risk 0.018 _(réel 5 s)_ (GBM 0.121) · ¼-Kelly 0.019 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €25.60–€25.85 (mid €25.73)
- Spot actuel : €26.64 (+3.5% au-dessus de la zone — repli à attendre)
- Stop : €25.21 (stop swing_plan-based (-13.08%))
- Targets : T1 €26.36 · R/R 1.21 | T2 €26.99 · R/R 2.42 | T3 €27.63 · R/R 3.65
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €25.21


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.36 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (13.08 %)** : le gap seul le franchit 0.391 % des séances (5 fois sur 1280).
   - exécution **11.732 pt plus bas** dans le cas TYPIQUE (médiane), 20.656 au p90, **25.037 au pire**
   - perte réelle **24.668 %** en moyenne _(tirée par la queue)_, jusqu'à **38.117 %** — au lieu des 13.08 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0453 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.345 % | p01 -6.808 % | pire -38.117 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2842** [0.221 ; 0.3546] _(largeur 13.4 pt, n_eff 173.1)_
   - swing : **0.4975** [0.445 ; 0.55] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.52** [0.4674 ; 0.5723] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 19.5 observations effectives », dont la borne haute a 95 % vaut environ 15.4 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (35.0 pt), swing (38.5 pt), deep (41.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-7.24 %** | CVaR **-11.87 %** | vol 6.3 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 3.90 % contre 7.39 % aujourd'hui, rapport 0.53)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.76 % vs -13.9 % si l'on extrapolait par √5 _(rapport 1.062 ; < 1 = le √5 surestime)_
- **β de baisse : 1.198** (β de hausse 0.941, asymétrie 1.2732) vs FCHI — 617 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.973× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 25.1636 sur atr_grid (1.0 ATR, 5.542 %) — p(stop avant cible) 0.615 [0.56 ; 0.67], R/R 0.978, perte reelle 12.959 % (gap inclus), CVaR 5.641 %, EV -3.5864 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0897 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.615, borne haute 0.665 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 0.98 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 5.64 % > budget 3.00 %
- Budget de queue : **3.0 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.212 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 42.8 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
   - ⚠ budget **borne** (brut 2.79 %) : les bornes sont un choix declare, pas une mesure.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 8.313 %) — p(stop avant cible) 0.475 [0.42 ; 0.53], R/R 0.772, perte reelle 16.422 % (gap inclus), EV -2.3376 % — **REFUSE**
      - refuse : R/R 0.77 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 8.38 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.34 %) : P(cible) 41.7 % x 12.68 % + P(rien) 10.8 % x 1.62 % ne couvrent pas P(stop) 47.5 % x 16.42 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.41 ATR (stop 16.255 %) — p(stop avant cible) 0.2424 [0.20 ; 0.29], R/R 0.469, perte reelle 27.014 % (gap inclus), EV -0.5564 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.29 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.56 %) : P(cible) 49.3 % x 12.68 % + P(rien) 26.4 % x -1.00 % ne couvrent pas P(stop) 24.2 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.74 ATR (stop 18.075 %) — p(stop avant cible) 0.2194 [0.18 ; 0.27], R/R 0.422, perte reelle 30.031 % (gap inclus), EV -0.8435 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.10 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.84 %) : P(cible) 49.3 % x 12.68 % + P(rien) 28.7 % x -1.77 % ne couvrent pas P(stop) 21.9 % x 30.03 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.43 ATR (stop 27.459 %) — p(stop avant cible) 0.1088 [0.08 ; 0.14], R/R 0.333, perte reelle 38.117 % (gap inclus), EV 0.2753 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.47 % > budget 3.00 %
   - 🟢 support a 6.77 ATR (stop 40.41 %) — p(stop avant cible) 0.0415 [0.02 ; 0.07], R/R 0.314, perte reelle 40.41 % (gap inclus), EV 1.5832 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.41 % > budget 3.00 %
   - ⚪ atr_grid a 1.0 ATR (stop 5.542 %) — p(stop avant cible) 0.615 [0.56 ; 0.67], R/R 0.978, perte reelle 12.959 % (gap inclus), EV -3.5864 % — **REFUSE**
      - refuse : p_stop_first 0.615, borne haute 0.665 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.98 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 5.64 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.59 %) : P(cible) 33.1 % x 12.68 % + P(rien) 5.4 % x 3.46 % ne couvrent pas P(stop) 61.5 % x 12.96 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 9.699 %) — p(stop avant cible) 0.4102 [0.36 ; 0.46], R/R 0.612, perte reelle 20.706 % (gap inclus), EV -2.6037 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 9.76 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.60 %) : P(cible) 45.4 % x 12.68 % + P(rien) 13.6 % x 1.03 % ne couvrent pas P(stop) 41.0 % x 20.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 11.084 %) — p(stop avant cible) 0.3515 [0.30 ; 0.40], R/R 0.563, perte reelle 22.515 % (gap inclus), EV -1.8536 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 11.14 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.85 %) : P(cible) 47.1 % x 12.68 % + P(rien) 17.7 % x 0.47 % ne couvrent pas P(stop) 35.1 % x 22.52 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 22.169 %) — p(stop avant cible) 0.1511 [0.12 ; 0.19], R/R 0.422, perte reelle 30.031 % (gap inclus), EV 0.5526 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.19 % > budget 3.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 30.482 %) — p(stop avant cible) 0.0974 [0.07 ; 0.13], R/R 0.333, perte reelle 38.117 % (gap inclus), EV 0.502 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.49 % > budget 3.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 33.253 %) — p(stop avant cible) 0.0844 [0.06 ; 0.12], R/R 0.333, perte reelle 38.117 % (gap inclus), EV 0.7428 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.26 % > budget 3.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 36.024 %) — p(stop avant cible) 0.0636 [0.04 ; 0.09], R/R 0.333, perte reelle 38.117 % (gap inclus), EV 1.2388 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.03 % > budget 3.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 44.337 %) — p(stop avant cible) 0.0365 [0.02 ; 0.06], R/R 0.286, perte reelle 44.337 % (gap inclus), EV 1.4735 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.34 % > budget 3.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.121 | EV/share : €0.062 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 33 % | T3 32 %
- Kelly (position) : f* 0.075 | ¼-Kelly 0.019 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.6 | bear 6.3 | side 8.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 266.0 (= 10 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.428% → cible +2.459% / stop −2.0%, p_fill 56%, n_eff≈27.3) : P(cible|rempli) **28%** · **EV/risk +0.018** (×p_fill ; si rempli +0.06% du capital)
  - **swing** (entrée dip −7.538% → cible +5.499% / stop −5.994%, p_fill 42%, n_eff≈20.6) : P(cible|rempli) **67%** · **EV/risk +0.080** (×p_fill ; si rempli +1.14% du capital)
  - **deep** (entrée dip −11.647% → cible +7.777% / stop −9.409%, p_fill 35%, n_eff≈19.5) : P(cible|rempli) **49%** · **EV/risk -0.088** (×p_fill ; si rempli -2.36% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→78% · +2.0%→69% · +3.0%→57% · +5.0%→44% · +8.0%→20%
- Range intraday médian 7.66% (p90 22.19%) · excursion haute méd. +4.29% / basse méd. −3.9%
- Profil de vol intra : ouverture 5.503% vs midi 1.744% vs clôture 1.892% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 9% · trend ↑0%/↓1% ; spike-down 73% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; mean-reverting — autocorr -0.062)_ ; drift intra méd. -0.16% ; recovery-V 29%
- **σ réalisé intraday** 5.795% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 66% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 27.013 (VA 26.519–27.165 ; dernier close 26.76)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 36% · rebond 86% · **stop −5.29%** sous le fill (sous le bruit) · cible +2.4% · R/R 0.45 (high win-rate)
- Gaps overnight (n=159) : méd. 0.01% · baisse 46% (gap-down >1% 20% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −1.1% (p90 −4.38%) · haut méd +0.93% · range méd 2.77%
- Excursion ouverture 15min (n=160) : bas méd −1.45% (p90 −5.56%) · haut méd +1.52% · range méd 3.44%
- Excursion ouverture 30min (n=160) : bas méd −1.54% (p90 −5.61%) · haut méd +2.06% · range méd 4.54%
- Excursion ouverture 60min (n=160) : bas méd −1.77% (p90 −6.33%) · haut méd +2.42% · range méd 5.44%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 26.76 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 82% (124/159) · gap 31% · délai 0.3min · rebond 70% (86/124) (MFE +2.64%)
   - −1.0% : fill 30min 60% · séance 81% (121/159) · gap 20% · délai 0.8min · rebond 70% (85/121) (MFE +2.66%)
   - −1.5% : fill 30min 49% · séance 76% (112/159) · gap 13% · délai 1.2min · rebond 70% (76/112) (MFE +2.04%)
   - −2.0% : fill 30min 41% · séance 65% (97/159) · gap 8% · délai 5.3min · rebond 60% (61/97) (MFE +1.64%)
   - −3.0% : fill 30min 29% · séance 54% (81/159) · gap 4% · délai 23.8min · rebond 76% (66/81) (MFE +1.99%)
   - −4.0% : fill 30min 22% · séance 47% (70/159) · gap 3% · délai 40.4min · rebond 71% (53/70) (MFE +2.33%)
   - −5.0% : fill 30min 15% · séance 36% (59/159) · gap 3% · délai 43.0min · rebond 86% (54/59) (MFE +2.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.91% (p90 −4.63%) → stop au-delà de −2.1% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.11% (p90 −4.91%) → stop au-delà de −3.09% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.09% (p90 −5.17%) → stop au-delà de −3.2% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1547 jambes) : jambe baissière méd −1.28% (p90 −3.26%) · ~19.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 99% (52/54) · rebond 73% (36/52)
      · −2.0% : fill 84% (45/54) · rebond 57% (27/45)
      · −3.0% : fill 70% (41/54) · rebond 79% (34/41)
      · −4.0% : fill 64% (36/54) · rebond 75% (29/36)
      · −5.0% : fill 45% (30/54) · rebond 84% (27/30)
   - **flat** (38 séances) :
      · −1.0% : fill 78% (30/38) · rebond 74% (23/30)
      · −2.0% : fill 57% (22/38) · rebond 73% (16/22)
      · −3.0% : fill 46% (16/38) · rebond 70% (13/16)
      · −4.0% : fill 42% (15/38) · rebond 70% (12/15)
      · −5.0% : fill 31% (12/38) · rebond 100% (12/12)
   - **gap-up** (67 séances) :
      · −1.0% : fill 67% (39/67) · rebond 64% (26/39)
      · −2.0% : fill 54% (30/67) · rebond 55% (18/30)
      · −3.0% : fill 44% (24/67) · rebond 76% (19/24)
      · −4.0% : fill 37% (19/67) · rebond 64% (12/19)
      · −5.0% : fill 33% (17/67) · rebond 79% (15/17)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 55% si les 15 1res min sont vertes (77 cas) · 34% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 71% si début vert vs 17% si rouge (base 45% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 252min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=85) : tient le vert **71%** · continue >prix actuel 48% ; creux résiduel méd -2.35% (q20 -5.44%) → **SL/trailing à −5.44%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.7% / q75 +5.25% → **scale +2.7% / runner +5.25%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **17%** (continue à baisser 53%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.49%** (au-delà de la MAE q10 -7.49%), cible rebond +2.06% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.2% .. +6.46%] · haut q95 +7.87% · bas q05 -7.39%
   - 60min (n=160) : retour [-5.84% .. +6.58%] · haut q95 +9.09% · bas q05 -7.67%
   - 2h (n=160) : retour [-5.98% .. +9.58%] · haut q95 +10.0% · bas q05 -7.98%
   - 4h (n=160) : retour [-7.05% .. +9.36%] · haut q95 +11.79% · bas q05 -10.07%
   - 6h (n=160) : retour [-6.71% .. +9.73%] · haut q95 +13.66% · bas q05 -10.74%
   - session (n=160) : retour [-7.89% .. +12.54%] · haut q95 +13.66% · bas q05 -11.2%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.36%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 60.9  _(momentum haussier)_
- **ADX** : 11.4  _(pas de tendance nette)_
- **MACD** : hist 0.205  _(pas de croisement recent)_
- **BB** : %B 0.49 · largeur 19.0%
- **ATR** : 1.48 (48.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.265  _(distribution)_
- **Vol ratio** : 0.44  _(volume atone)_
- **Choppiness** : 50.0  _(transition)_
- **MA** : MA20 26.68 · MA50 29.36 · MA200 25.78  _(prix < MA20)_
- **Dist MA** : MA20 -0.1% · MA50 -9.3% · MA200 +3.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (820321 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
