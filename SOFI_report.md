# SOFI

**Generated** : 2026-08-25T00:34:53.997902+00:00  
**Santé technique** : 6/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $18.24  

> 🟡 **WAIT-FOR-DIP** — spot +7.5 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $18.24 (+7.5% vs entrée) · entrée $16.96 · stop $15.82 · T1 $19.25 · R/R 2.01  
> ↳ P(T1 av. stop) 18 % · EV/risk 0.124 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $16.78–$17.14 (mid $16.96)
- Spot actuel : $18.24 (+7.5% au-dessus de la zone — repli à attendre)
- Stop : $15.82 (stop swing_plan-based (-13.26%))
- Targets : T1 $19.25 · R/R 2.01 | T2 $19.46 · R/R 2.19 | T3 $19.67 · R/R 2.38
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $15.82


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=5.99 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (13.26 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1253).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 13.26 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.268 % | p01 -6.52 % | pire -11.105 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0921** [0.0557 ; 0.1419] _(largeur 8.6 pt, n_eff 173.1)_
   - swing : **0.4602** [0.4082 ; 0.5129] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.554** [0.5013 ; 0.6058] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (54.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.46 %** | CVaR **-8.8 %** | vol 4.18 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.5 % vs -14.19 % si l'on extrapolait par √5 _(rapport 1.021 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8289** (β de hausse 1.6916, asymétrie 1.0812) vs IWM — 602 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.285× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 16.3954 sur atr_grid (2.5 ATR, 10.113 %) — p(stop avant cible) 0.3629 [0.31 ; 0.41], R/R 3.446, perte reelle 11.105 % (gap inclus), CVaR 10.114 %, EV -0.6912 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 1.01 ATR (stop 6.57 %) — p(stop avant cible) 0.519 [0.47 ; 0.57], R/R 4.599, perte reelle 8.322 % (gap inclus), EV -0.8138 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.519, borne haute 0.571 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.81 %) : P(cible) 0.1 % x 38.27 % + P(rien) 48.0 % x 7.22 % ne couvrent pas P(stop) 51.9 % x 8.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 3.25 ATR (stop 15.612 %) — p(stop avant cible) 0.1269 [0.10 ; 0.17], R/R 2.451, perte reelle 15.612 % (gap inclus), EV 0.3936 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 15.61 % > budget 12.00 %
   - 🟢 support a 4.55 ATR (stop 20.893 %) — p(stop avant cible) 0.0472 [0.03 ; 0.07], R/R 1.832, perte reelle 20.893 % (gap inclus), EV 0.4373 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 20.89 % > budget 12.00 %
   - ⚪ grid_snapped a 1.01 ATR (stop 5.312 %) — p(stop avant cible) 0.618 [0.57 ; 0.67], R/R 5.206, perte reelle 7.351 % (gap inclus), EV -1.1743 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.618, borne haute 0.668 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.17 %) : P(cible) 0.1 % x 38.27 % + P(rien) 38.1 % x 8.75 % ne couvrent pas P(stop) 61.8 % x 7.35 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 8.091 %) — p(stop avant cible) 0.438 [0.39 ; 0.49], R/R 3.943, perte reelle 9.707 % (gap inclus), EV -0.817 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.82 %) : P(cible) 0.1 % x 38.27 % + P(rien) 56.1 % x 6.05 % ne couvrent pas P(stop) 43.8 % x 9.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 10.113 %) — p(stop avant cible) 0.3629 [0.31 ; 0.41], R/R 3.446, perte reelle 11.105 % (gap inclus), EV -0.6912 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.69 %) : P(cible) 0.1 % x 38.27 % + P(rien) 63.6 % x 5.19 % ne couvrent pas P(stop) 36.3 % x 11.11 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 3.25 ATR (stop 14.354 %) — p(stop avant cible) 0.1548 [0.12 ; 0.20], R/R 2.666, perte reelle 14.354 % (gap inclus), EV 0.2891 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.35 % > budget 12.00 %
   - 🟢 grid_snapped a 4.55 ATR (stop 19.635 %) — p(stop avant cible) 0.0574 [0.04 ; 0.09], R/R 1.949, perte reelle 19.635 % (gap inclus), EV 0.4603 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 19.63 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 22.249 %) — p(stop avant cible) 0.0354 [0.02 ; 0.06], R/R 1.72, perte reelle 22.249 % (gap inclus), EV 0.4307 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 22.25 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 24.272 %) — p(stop avant cible) 0.0256 [0.01 ; 0.05], R/R 1.577, perte reelle 24.272 % (gap inclus), EV 0.4331 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.58 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.27 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 26.294 %) — p(stop avant cible) 0.0056 [0.00 ; 0.02], R/R 1.456, perte reelle 26.294 % (gap inclus), EV 0.5658 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.46 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.29 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 28.317 %) — p(stop avant cible) 0.0041 [0.00 ; 0.02], R/R 1.352, perte reelle 28.317 % (gap inclus), EV 0.5666 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.35 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.32 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 30.34 %) — p(stop avant cible) 0.0032 [0.00 ; 0.01], R/R 1.261, perte reelle 30.34 % (gap inclus), EV 0.5732 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.26 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.34 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 32.362 %) — p(stop avant cible) 0.0024 [0.00 ; 0.01], R/R 1.183, perte reelle 32.362 % (gap inclus), EV 0.5847 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.36 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : -0.113 | EV/share : $-0.129 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 9 % | T2 7 % | T3 6 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 68.9 | bear 14.1 | side 16.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 383.0 (= 21 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.187% → cible +4.138% / stop −2.069%, p_fill 22%, n_eff≈10.2) : P(cible|rempli) **18%** · **EV/risk +0.054** (×p_fill ; si rempli +0.50% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=5, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=4, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→69% · +2.0%→48% · +3.0%→36% · +5.0%→12% · +8.0%→1%
- Range intraday médian 4.32% (p90 7.29%) · excursion haute méd. +1.84% / basse méd. −2.18%
- Profil de vol intra : ouverture 3.005% vs midi 0.875% vs clôture 0.988% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 15% · trend ↑2%/↓0% ; spike-down 64% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.146 ; mean-reverting — autocorr -0.036)_ ; drift intra méd. 0.051% ; recovery-V 17%
- **σ réalisé intraday** 2.738% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 61% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 18.9512 (VA 18.8717–18.9778 ; dernier close 18.9)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 48% · rebond 69% · **stop −2.95%** sous le fill (sous le bruit) · cible +1.86% · R/R 0.63 (high win-rate)
- Gaps overnight (n=159) : méd. 0.38% · baisse 40% (gap-down >1% 24% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −1.7%) · haut méd +0.69% · range méd 1.59%
- Excursion ouverture 15min (n=160) : bas méd −0.99% (p90 −2.94%) · haut méd +0.96% · range méd 2.24%
- Excursion ouverture 30min (n=160) : bas méd −1.08% (p90 −3.21%) · haut méd +1.13% · range méd 2.71%
- Excursion ouverture 60min (n=160) : bas méd −1.38% (p90 −3.78%) · haut méd +1.25% · range méd 3.33%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 18.9 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 71% (120/159) · gap 29% · délai 0.0min · rebond 52% (64/120) (MFE +1.18%)
   - −1.0% : fill 30min 50% · séance 63% (108/159) · gap 24% · délai 1.0min · rebond 57% (67/108) (MFE +1.17%)
   - −1.5% : fill 30min 41% · séance 60% (100/159) · gap 18% · délai 10.2min · rebond 68% (66/100) (MFE +1.45%)
   - −2.0% : fill 30min 33% · séance 48% (79/159) · gap 11% · délai 5.8min · rebond 69% (54/79) (MFE +1.86%)
   - −3.0% : fill 30min 14% · séance 34% (58/159) · gap 3% · délai 38.3min · rebond 65% (40/58) (MFE +1.34%)
   - −4.0% : fill 30min 8% · séance 18% (37/159) · gap 2% · délai 42.1min · rebond 57% (24/37) (MFE +1.46%)
   - −5.0% : fill 30min 4% · séance 7% (17/159) · gap 2% · délai 31.4min · rebond 40% (10/17) (MFE +0.74%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.43% (p90 −1.72%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.47% (p90 −1.63%) → stop au-delà de −1.22% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.42% (p90 −1.51%) → stop au-delà de −1.12% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=669 jambes) : jambe baissière méd −1.08% (p90 −2.78%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (64 séances) :
      · −1.0% : fill 98% (63/64) · rebond 59% (39/63)
      · −2.0% : fill 87% (54/64) · rebond 74% (39/54)
      · −3.0% : fill 70% (44/64) · rebond 68% (32/44)
      · −4.0% : fill 38% (28/64) · rebond 65% (20/28)
      · −5.0% : fill 19% (14/64) · rebond 38% (8/14)
   - **flat** (22 séances) :
      · −1.0% : fill 52% (12/22) · rebond 35% (5/12)
      · −2.0% : fill 42% (8/22) · rebond 71% (5/8)
      · −3.0% : fill 26% (5/22) · rebond 59% (3/5)
      · −4.0% : fill 11% (2/22) · rebond 72% (1/2)
      · −5.0% : fill 0% (0/22) · rebond 0% (0/0)
   - **gap-up** (73 séances) :
      · −1.0% : fill 42% (33/73) · rebond 62% (23/33)
      · −2.0% : fill 23% (17/73) · rebond 56% (10/17)
      · −3.0% : fill 12% (9/73) · rebond 57% (5/9)
      · −4.0% : fill 6% (7/73) · rebond 20% (3/7)
      · −5.0% : fill 1% (3/73) · rebond 70% (2/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 41% en base · 61% si les 15 1res min sont vertes (72 cas) · 25% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 78% si début vert vs 10% si rouge (base 41% · écart 69 pts) ; prédictivité sature ensuite (plafond brut 228min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **78%** · continue >prix actuel 54% ; creux résiduel méd -1.53% (q20 -2.61%) → **SL/trailing à −2.61%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.9% / q75 +2.85% → **scale +1.9% / runner +2.85%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **10%** (continue à baisser 60%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.11%** (au-delà de la MAE q10 -3.11%), cible rebond +1.11% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.94% .. +3.87%] · haut q95 +4.11% · bas q05 -3.5%
   - 60min (n=160) : retour [-3.2% .. +3.99%] · haut q95 +4.6% · bas q05 -4.02%
   - 2h (n=160) : retour [-3.7% .. +4.13%] · haut q95 +5.43% · bas q05 -4.97%
   - 4h (n=160) : retour [-4.01% .. +4.63%] · haut q95 +5.69% · bas q05 -5.08%
   - 6h (n=160) : retour [-4.64% .. +4.14%] · haut q95 +5.74% · bas q05 -5.12%
   - session (n=160) : retour [-4.56% .. +5.24%] · haut q95 +5.78% · bas q05 -5.37%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.89%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 45.8  _(neutre)_
- **ADX** : 15.3  _(pas de tendance nette)_
- **MACD** : hist 0.041  _(pas de croisement recent)_
- **BB** : %B 0.61 · largeur 20.6%
- **ATR** : 0.74 (4.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.067  _(accumulation)_
- **Vol ratio** : 0.55  _(volume atone)_
- **Choppiness** : 72.4  _(marche en range (choppy))_
- **MA** : MA20 17.82 · MA50 17.7 · MA200 20.46  _(prix > MA20)_
- **Dist MA** : MA20 +2.3% · MA50 +3.0% · MA200 -10.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (801731 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
