# PRY

**Generated** : 2026-08-24T21:47:47.245834+00:00  
**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €117.60  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €117.60 (+4.2% vs entrée) · entrée €112.87 · stop €107.82 · T1 €116.59 · R/R 0.74  
> ↳ P(T1 av. stop) 57 % _(réel 5 s)_ · EV/risk -0.001 _(réel 5 s)_ (GBM -0.01) · ¼-Kelly 0.004 · _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €112.12–€113.61 (mid €112.87)
- Spot actuel : €117.60 (+4.2% au-dessus de la zone — repli à attendre)
- Stop : €107.82 (stop swing_plan-based (-8.32%))
- Targets : T1 €116.59 · R/R 0.74 | T2 €120.30 · R/R 1.47 | T3 €124.02 · R/R 2.21
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €107.82


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.50 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.32 %)** : le gap seul le franchit 0.079 % des séances (1 fois sur 1270).
   - exécution **1.678 pt plus bas** dans le cas TYPIQUE (médiane), 1.678 au p90, **1.678 au pire**
   - perte réelle **9.998 %** en moyenne _(tirée par la queue)_, jusqu'à **9.998 %** — au lieu des 8.32 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0013 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.846 % | p01 -3.346 % | pire -9.998 % _(sur 1270 séances)_
- **P(stop avant cible)** _(source : daily, 1271 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0621** [0.0332 ; 0.1055] _(largeur 7.2 pt, n_eff 173.1)_
   - swing : **0.3412** [0.2927 ; 0.3923] _(largeur 10.0 pt, n_eff 345.8)_
   - deep : **0.4299** [0.3785 ; 0.4825] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 20.9 observations effectives », dont la borne haute a 95 % vaut environ 14.4 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (36.0 pt), swing (42.8 pt), deep (41.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-4.27 %** | CVaR **-5.76 %** | vol 2.63 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 1.79 % contre 2.95 % aujourd'hui, rapport 0.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.48 % vs -7.48 % si l'on extrapolait par √5 _(rapport 0.865 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0292** (β de hausse 1.2267, asymétrie 0.839) vs FTSEMIB — 562 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.397× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 106.9569 sur swing_based (1.65 ATR, 9.05 %) — p(stop avant cible) 0.2142 [0.17 ; 0.26], R/R 3.142, perte reelle 9.998 % (gap inclus), CVaR 9.051 %, EV 1.2413 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 6.441 %) — p(stop avant cible) 0.3616 [0.31 ; 0.41], R/R 3.972, perte reelle 7.909 % (gap inclus), EV 0.651 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ swing_based a 1.65 ATR (stop 9.05 %) — p(stop avant cible) 0.2142 [0.17 ; 0.26], R/R 3.142, perte reelle 9.998 % (gap inclus), EV 1.2413 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - 🟢 support a 2.7 ATR (stop 13.57 %) — p(stop avant cible) 0.0619 [0.04 ; 0.09], R/R 2.315, perte reelle 13.57 % (gap inclus), EV 1.8014 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.57 % > budget 12.00 %
   - 🟢 support a 7.73 ATR (stop 35.169 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.893, perte reelle 35.169 % (gap inclus), EV 1.9465 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.17 % > budget 12.00 %
   - 🟢 support a 8.92 ATR (stop 40.267 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.78, perte reelle 40.267 % (gap inclus), EV 1.9465 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.78 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.27 % > budget 12.00 %
   - ⚪ atr_grid a 1.0 ATR (stop 4.294 %) — p(stop avant cible) 0.5332 [0.48 ; 0.59], R/R 5.609, perte reelle 5.601 % (gap inclus), EV 0.012 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 5.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.533, borne haute 0.585 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 3.5 ATR (stop 15.03 %) — p(stop avant cible) 0.0346 [0.02 ; 0.06], R/R 2.09, perte reelle 15.03 % (gap inclus), EV 1.9108 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 15.03 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 17.177 %) — p(stop avant cible) 0.0155 [0.01 ; 0.03], R/R 1.829, perte reelle 17.177 % (gap inclus), EV 1.9508 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 17.18 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 19.324 %) — p(stop avant cible) 0.0119 [0.00 ; 0.03], R/R 1.626, perte reelle 19.324 % (gap inclus), EV 1.9404 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 19.32 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 21.471 %) — p(stop avant cible) 0.0098 [0.00 ; 0.02], R/R 1.463, perte reelle 21.471 % (gap inclus), EV 1.9243 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.46 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.47 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 23.618 %) — p(stop avant cible) 0.0062 [0.00 ; 0.02], R/R 1.33, perte reelle 23.618 % (gap inclus), EV 1.9352 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.33 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.62 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 25.765 %) — p(stop avant cible) 0.0039 [0.00 ; 0.02], R/R 1.219, perte reelle 25.765 % (gap inclus), EV 1.9423 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.22 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.76 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 27.912 %) — p(stop avant cible) 0.0031 [0.00 ; 0.01], R/R 1.126, perte reelle 27.912 % (gap inclus), EV 1.9382 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.13 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.91 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 30.06 %) — p(stop avant cible) 0.0016 [0.00 ; 0.01], R/R 1.045, perte reelle 30.06 % (gap inclus), EV 1.9417 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.05 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.06 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : -0.01 | EV/share : €-0.051 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 23 % | T3 7 %
- Kelly (position) : f* 0.016 | ¼-Kelly 0.004 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 27.0 | bear 26.7 | side 46.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.826% → cible +1.473% / stop −8.0%, p_fill 51%, n_eff≈20.9) : P(cible|rempli) **26%** · **EV/risk -0.039** (×p_fill ; si rempli -0.61% du capital)
  - **swing** (entrée dip −4.026% → cible +3.294% / stop −4.474%, p_fill 35%, n_eff≈18.1) : P(cible|rempli) **57%** · **EV/risk -0.001** (×p_fill ; si rempli -0.02% du capital)
  - **deep** (entrée dip −6.219% → cible +4.659% / stop −6.868%, p_fill 46%, n_eff≈18.1) : P(cible|rempli) **66%** · **EV/risk +0.046** (×p_fill ; si rempli +0.68% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→68% · +2.0%→41% · +3.0%→28% · +5.0%→8% · +8.0%→1%
- Range intraday médian 4.25% (p90 6.33%) · excursion haute méd. +1.5% / basse méd. −1.6%
- Profil de vol intra : ouverture 2.383% vs midi 0.821% vs clôture 1.183% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 54% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; neutre — autocorr -0.001)_ ; drift intra méd. -0.683% ; recovery-V 23%
- **σ réalisé intraday** 2.619% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 59% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 125.1795 (VA 124.6845–125.8725 ; dernier close 123.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 19% · rebond 74% · **stop −2.38%** sous le fill (sous le bruit) · cible +1.45% · R/R 0.61 (high win-rate)
- Gaps overnight (n=159) : méd. 0.28% · baisse 40% (gap-down >1% 16% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −0.81% (p90 −2.04%) · haut méd +0.35% · range méd 1.38%
- Excursion ouverture 15min (n=160) : bas méd −1.03% (p90 −2.49%) · haut méd +0.56% · range méd 1.74%
- Excursion ouverture 30min (n=160) : bas méd −1.04% (p90 −2.92%) · haut méd +0.66% · range méd 1.99%
- Excursion ouverture 60min (n=160) : bas méd −1.21% (p90 −3.14%) · haut méd +0.86% · range méd 2.25%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 123.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 69% (114/159) · gap 23% · délai 0.3min · rebond 60% (71/114) (MFE +1.25%)
   - −1.0% : fill 30min 49% · séance 61% (97/159) · gap 16% · délai 0.6min · rebond 58% (58/97) (MFE +1.5%)
   - −1.5% : fill 30min 34% · séance 53% (84/159) · gap 13% · délai 4.5min · rebond 52% (46/84) (MFE +1.09%)
   - −2.0% : fill 30min 23% · séance 44% (68/159) · gap 8% · délai 13.1min · rebond 62% (43/68) (MFE +1.23%)
   - −3.0% : fill 30min 11% · séance 33% (49/159) · gap 3% · délai 77.1min · rebond 64% (33/49) (MFE +1.64%)
   - −4.0% : fill 30min 3% · séance 19% (26/159) · gap 1% · délai 185.0min · rebond 74% (19/26) (MFE +1.45%)
   - −5.0% : fill 30min 1% · séance 13% (18/159) · gap 1% · délai 394.2min · rebond 65% (13/18) (MFE +1.39%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.52% (p90 −1.75%) → stop au-delà de −1.51% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.37% (p90 −2.02%) → stop au-delà de −1.18% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.02% (p90 −1.85%) → stop au-delà de −1.09% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=495 jambes) : jambe baissière méd −1.07% (p90 −2.48%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 91% (49/54) · rebond 47% (27/49)
      · −2.0% : fill 71% (39/54) · rebond 59% (26/39)
      · −3.0% : fill 59% (30/54) · rebond 64% (22/30)
      · −4.0% : fill 40% (17/54) · rebond 70% (12/17)
      · −5.0% : fill 31% (13/54) · rebond 60% (9/13)
   - **flat** (32 séances) :
      · −1.0% : fill 65% (18/32) · rebond 58% (11/18)
      · −2.0% : fill 43% (10/32) · rebond 91% (8/10)
      · −3.0% : fill 22% (6/32) · rebond 63% (3/6)
      · −4.0% : fill 6% (3/32) · rebond 59% (2/3)
      · −5.0% : fill 3% (2/32) · rebond 25% (1/2)
   - **gap-up** (73 séances) :
      · −1.0% : fill 40% (30/73) · rebond 74% (20/30)
      · −2.0% : fill 26% (19/73) · rebond 43% (9/19)
      · −3.0% : fill 21% (13/73) · rebond 63% (8/13)
      · −4.0% : fill 11% (6/73) · rebond 86% (5/6)
      · −5.0% : fill 5% (3/73) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 69% si les 15 1res min sont vertes (74 cas) · 30% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:09** → P(séance verte=clôture>ouverture) 80% si début vert vs 22% si rouge (base 47% · écart 59 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **80%** · continue >prix actuel 57% ; creux résiduel méd -0.93% (q20 -1.85%) → **SL/trailing à −1.85%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.42% / q75 +2.63% → **scale +1.42% / runner +2.63%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **22%** (continue à baisser 63%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.1%** (au-delà de la MAE q10 -4.1%), cible rebond +1.26% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.83% .. +2.92%] · haut q95 +3.42% · bas q05 -3.39%
   - 60min (n=160) : retour [-3.29% .. +2.43%] · haut q95 +3.88% · bas q05 -3.54%
   - 2h (n=160) : retour [-3.57% .. +2.64%] · haut q95 +3.98% · bas q05 -4.41%
   - 4h (n=160) : retour [-3.5% .. +3.29%] · haut q95 +4.1% · bas q05 -4.59%
   - 6h (n=160) : retour [-3.71% .. +3.75%] · haut q95 +4.55% · bas q05 -4.85%
   - session (n=160) : retour [-4.33% .. +4.0%] · haut q95 +5.34% · bas q05 -6.25%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.41%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 41.2  _(momentum baissier)_
- **ADX** : 26.5  _(tendance etablie)_
- **MACD** : hist -0.097  _(bearish_recent)_
- **BB** : %B 0.18 · largeur 15.2%
- **ATR** : 5.05 (68.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.201  _(distribution)_
- **Vol ratio** : 0.94  _(volume normal)_
- **Choppiness** : 52.3  _(transition)_
- **MA** : MA20 123.7 · MA50 132.69 · MA200 113.36  _(prix < MA20)_
- **Dist MA** : MA20 -4.9% · MA50 -11.4% · MA200 +3.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (828232 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
