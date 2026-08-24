# AL2SI

**Generated** : 2026-08-24T21:46:16.342660+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €26.46  

> 🟡 **WAIT-FOR-DIP** — spot +7.8 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €26.46 (+7.8% vs entrée) · entrée €24.55 · stop €23.10 · T1 €25.90 · R/R 0.93  
> ↳ P(T1 av. stop) 64 % _(réel 5 s)_ · EV/risk 0.054 _(réel 5 s)_ (GBM 0.137) · ¼-Kelly 0.02 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €24.28–€24.82 (mid €24.55)
- Spot actuel : €26.46 (+7.8% au-dessus de la zone — repli à attendre)
- Stop : €23.10 (stop swing_plan-based (-12.7%))
- Targets : T1 €25.90 · R/R 0.93 | T2 €27.24 · R/R 1.86 | T3 €28.58 · R/R 2.78
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €23.10


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.36 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.7 %)** : le gap seul le franchit 0.391 % des séances (5 fois sur 1280).
   - exécution **12.112 pt plus bas** dans le cas TYPIQUE (médiane), 21.036 au p90, **25.417 au pire**
   - perte réelle **24.668 %** en moyenne _(tirée par la queue)_, jusqu'à **38.117 %** — au lieu des 12.7 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0467 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.345 % | p01 -6.808 % | pire -38.117 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.281** [0.2181 ; 0.3512] _(largeur 13.3 pt, n_eff 173.1)_
   - swing : **0.5004** [0.4479 ; 0.5529] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.517** [0.4644 ; 0.5693] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 20.4 observations effectives », dont la borne haute a 95 % vaut environ 14.7 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (35.0 pt), swing (39.4 pt), deep (40.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-7.24 %** | CVaR **-11.87 %** | vol 6.3 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 3.90 % contre 7.25 % aujourd'hui, rapport 0.54)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.76 % vs -13.9 % si l'on extrapolait par √5 _(rapport 1.062 ; < 1 = le √5 surestime)_
- **β de baisse : 1.194** (β de hausse 0.941, asymétrie 1.2689) vs FCHI — 617 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.976× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 24.3297 sur swing_based (0.99 ATR, 8.051 %) — p(stop avant cible) 0.489 [0.44 ; 0.54], R/R 0.82, perte reelle 16.422 % (gap inclus), CVaR 8.123 %, EV -2.5345 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.7076 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : R/R 0.82 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 8.12 % > budget 3.00 %
- Budget de queue : **3.0 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.212 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 42.8 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
   - ⚠ budget **borne** (brut 2.79 %) : les bornes sont un choix declare, pas une mesure.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.99 ATR (stop 8.051 %) — p(stop avant cible) 0.489 [0.44 ; 0.54], R/R 0.82, perte reelle 16.422 % (gap inclus), EV -2.5345 % — **REFUSE**
      - refuse : R/R 0.82 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 8.12 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.53 %) : P(cible) 38.9 % x 13.47 % + P(rien) 12.2 % x 2.14 % ne couvrent pas P(stop) 48.9 % x 16.42 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.66 ATR (stop 17.233 %) — p(stop avant cible) 0.2237 [0.18 ; 0.27], R/R 0.499, perte reelle 27.014 % (gap inclus), EV -0.2188 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.26 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.22 %) : P(cible) 45.7 % x 13.47 % + P(rien) 31.9 % x -1.05 % ne couvrent pas P(stop) 22.4 % x 27.01 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.38 ATR (stop 26.681 %) — p(stop avant cible) 0.1087 [0.08 ; 0.14], R/R 0.413, perte reelle 32.641 % (gap inclus), EV 0.9099 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.69 % > budget 3.00 %
   - 🟢 support a 6.76 ATR (stop 39.72 %) — p(stop avant cible) 0.0413 [0.02 ; 0.07], R/R 0.339, perte reelle 39.72 % (gap inclus), EV 1.6614 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.72 % > budget 3.00 %
   - ⚪ atr_grid a 1.75 ATR (stop 9.604 %) — p(stop avant cible) 0.41 [0.36 ; 0.46], R/R 0.651, perte reelle 20.706 % (gap inclus), EV -2.5373 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 9.66 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.54 %) : P(cible) 42.5 % x 13.47 % + P(rien) 16.4 % x 1.34 % ne couvrent pas P(stop) 41.0 % x 20.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 10.976 %) — p(stop avant cible) 0.3509 [0.30 ; 0.40], R/R 0.598, perte reelle 22.515 % (gap inclus), EV -1.7603 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 11.03 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.76 %) : P(cible) 44.3 % x 13.47 % + P(rien) 20.6 % x 0.83 % ne couvrent pas P(stop) 35.1 % x 22.52 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 19.208 %) — p(stop avant cible) 0.1958 [0.16 ; 0.24], R/R 0.449, perte reelle 30.031 % (gap inclus), EV -0.2435 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.23 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.24 %) : P(cible) 46.2 % x 13.47 % + P(rien) 34.2 % x -1.72 % ne couvrent pas P(stop) 19.6 % x 30.03 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 21.952 %) — p(stop avant cible) 0.1544 [0.12 ; 0.20], R/R 0.449, perte reelle 30.031 % (gap inclus), EV 0.5195 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.97 % > budget 3.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 30.184 %) — p(stop avant cible) 0.0976 [0.07 ; 0.13], R/R 0.353, perte reelle 38.117 % (gap inclus), EV 0.5375 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.19 % > budget 3.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 32.928 %) — p(stop avant cible) 0.0875 [0.06 ; 0.12], R/R 0.353, perte reelle 38.117 % (gap inclus), EV 0.7267 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.93 % > budget 3.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 35.672 %) — p(stop avant cible) 0.0632 [0.04 ; 0.09], R/R 0.353, perte reelle 38.117 % (gap inclus), EV 1.2887 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.67 % > budget 3.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 41.161 %) — p(stop avant cible) 0.0413 [0.02 ; 0.07], R/R 0.327, perte reelle 41.161 % (gap inclus), EV 1.6019 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.16 % > budget 3.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 43.905 %) — p(stop avant cible) 0.0363 [0.02 ; 0.06], R/R 0.307, perte reelle 43.905 % (gap inclus), EV 1.5398 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.90 % > budget 3.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.137 | EV/share : €0.199 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 55 % | T2 35 % | T3 24 %
- Kelly (position) : f* 0.081 | ¼-Kelly 0.02 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 85.7 | bear 5.6 | side 8.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 265.0 (= 10 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.275% → cible +2.448% / stop −2.0%, p_fill 56%, n_eff≈27.3) : P(cible|rempli) **29%** · **EV/risk +0.016** (×p_fill ; si rempli +0.06% du capital)
  - **swing** (entrée dip −7.212% → cible +5.473% / stop −5.915%, p_fill 42%, n_eff≈20.6) : P(cible|rempli) **64%** · **EV/risk +0.054** (×p_fill ; si rempli +0.76% du capital)
  - **deep** (entrée dip −11.148% → cible +7.74% / stop −9.265%, p_fill 40%, n_eff≈20.4) : P(cible|rempli) **49%** · **EV/risk -0.092** (×p_fill ; si rempli -2.16% du capital)
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

- **RSI** : 55.2  _(momentum haussier)_
- **ADX** : 10.6  _(pas de tendance nette)_
- **MACD** : hist 0.199  _(pas de croisement recent)_
- **BB** : %B 0.46 · largeur 19.0%
- **ATR** : 1.45 (48.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.216  _(distribution)_
- **Vol ratio** : 0.2  _(volume atone)_
- **Choppiness** : 55.7  _(transition)_
- **MA** : MA20 26.65 · MA50 28.89 · MA200 25.86  _(prix < MA20)_
- **Dist MA** : MA20 -0.7% · MA50 -8.4% · MA200 +2.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (838596 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
