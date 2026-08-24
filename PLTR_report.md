# PLTR

**Generated** : 2026-08-24T00:25:58.678681+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · $179.94  

> 🟡 **WAIT-FOR-DIP** — spot +4.8 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $179.94 (+4.8% vs entrée) · entrée $171.78 · stop $167.49 · T1 $178.06 · R/R 1.46  
> ↳ P(T1 av. stop) 62 % · EV/risk 0.31 · ¼-Kelly 0.002 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 417 % hors [0,100] (R² max 0.40). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : RSI 79.0 > 70 (surachat) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $170.52–$173.04 (mid $171.78)
- Spot actuel : $179.94 (+4.8% au-dessus de la zone — repli à attendre)
- Stop : $167.49 (stop swing_plan-based (-15.32%))
- Targets : T1 $178.06 · R/R 1.46 | T2 $184.34 · R/R 2.93 | T3 $190.62 · R/R 4.39
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $167.49


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.79 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (15.32 %)** : le gap seul le franchit 0.08 % des séances (1 fois sur 1254).
   - exécution **2.612 pt plus bas** dans le cas TYPIQUE (médiane), 2.612 au p90, **2.612 au pire**
   - perte réelle **17.932 %** en moyenne _(tirée par la queue)_, jusqu'à **17.932 %** — au lieu des 15.32 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0021 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.88 % | p01 -6.138 % | pire -17.932 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0898** [0.054 ; 0.1392] _(largeur 8.5 pt, n_eff 173.1)_
   - swing : **0.4237** [0.3724 ; 0.4762] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.5026** [0.4501 ; 0.5551] _(largeur 10.5 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.2 %** | CVaR **-8.48 %** | vol 4.27 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.44 % vs -13.82 % si l'on extrapolait par √5 _(rapport 0.973 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7055** (β de hausse 1.4168, asymétrie 1.2038) vs IWM — 601 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 163.1171 sur atr_grid (1.75 ATR, 9.349 %) — p(stop avant cible) 0.3481 [0.30 ; 0.40], R/R 0.922, perte reelle 13.126 % (gap inclus), CVaR 9.367 %, EV -0.5113 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.92 < plancher 1.60 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 8.014 %) — p(stop avant cible) 0.406 [0.36 ; 0.46], R/R 1.01, perte reelle 11.982 % (gap inclus), EV -0.6382 % — **REFUSE**
      - refuse : R/R 1.01 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.64 %) : P(cible) 30.5 % x 12.11 % + P(rien) 28.9 % x 1.84 % ne couvrent pas P(stop) 40.6 % x 11.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 3.5 ATR (stop 21.478 %) — p(stop avant cible) 0.0361 [0.02 ; 0.06], R/R 0.564, perte reelle 21.478 % (gap inclus), EV 1.1948 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.48 % > budget 12.00 %
   - 🟢 support a 6.45 ATR (stop 37.288 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.325, perte reelle 37.288 % (gap inclus), EV 1.3581 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.29 % > budget 12.00 %
   - 🟢 support a 7.65 ATR (stop 43.691 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.277, perte reelle 43.691 % (gap inclus), EV 1.3597 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.69 % > budget 12.00 %
   - ⚪ atr_grid a 1.0 ATR (stop 5.342 %) — p(stop avant cible) 0.5602 [0.51 ; 0.61], R/R 1.351, perte reelle 8.963 % (gap inclus), EV -1.3824 % — **REFUSE**
      - refuse : p_stop_first 0.560, borne haute 0.612 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.35 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.38 %) : P(cible) 25.5 % x 12.11 % + P(rien) 18.5 % x 2.99 % ne couvrent pas P(stop) 56.0 % x 8.96 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 9.349 %) — p(stop avant cible) 0.3481 [0.30 ; 0.40], R/R 0.922, perte reelle 13.126 % (gap inclus), EV -0.5113 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.51 %) : P(cible) 30.8 % x 12.11 % + P(rien) 34.4 % x 0.97 % ne couvrent pas P(stop) 34.8 % x 13.13 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 12.02 %) — p(stop avant cible) 0.2547 [0.21 ; 0.30], R/R 0.842, perte reelle 14.376 % (gap inclus), EV 0.1705 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.03 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 14.692 %) — p(stop avant cible) 0.164 [0.13 ; 0.21], R/R 0.675, perte reelle 17.932 % (gap inclus), EV 0.1915 % — **REFUSE**
      - refuse : R/R 0.68 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.69 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 16.027 %) — p(stop avant cible) 0.1312 [0.10 ; 0.17], R/R 0.675, perte reelle 17.932 % (gap inclus), EV 0.5615 % — **REFUSE**
      - refuse : R/R 0.68 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.03 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 24.041 %) — p(stop avant cible) 0.0096 [0.00 ; 0.02], R/R 0.504, perte reelle 24.041 % (gap inclus), EV 1.3099 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.04 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 26.712 %) — p(stop avant cible) 0.0067 [0.00 ; 0.02], R/R 0.453, perte reelle 26.712 % (gap inclus), EV 1.3301 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.71 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 29.383 %) — p(stop avant cible) 0.0038 [0.00 ; 0.02], R/R 0.412, perte reelle 29.383 % (gap inclus), EV 1.3448 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.38 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 32.054 %) — p(stop avant cible) 0.0022 [0.00 ; 0.01], R/R 0.378, perte reelle 32.054 % (gap inclus), EV 1.3541 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.05 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.05 | EV/share : $0.216 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 19 % | T2 10 % | T3 10 %
- Kelly (position) : f* 0.007 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.1 | bear 9.8 | side 85.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 540.0 (= 3 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=6, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→78% · +2.0%→50% · +3.0%→29% · +5.0%→10% · +8.0%→4%
- Range intraday médian 3.92% (p90 7.17%) · excursion haute méd. +2.0% / basse méd. −1.71%
- Profil de vol intra : ouverture 3.051% vs midi 0.761% vs clôture 0.858% _(ouverture ~4.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 75% · range 23% · trend ↑2%/↓0% ; spike-down 53% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; neutre — autocorr -0.003)_ ; drift intra méd. 0.675% ; recovery-V 31%
- **σ réalisé intraday** 2.659% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 42% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 179.079 (VA 177.603–181.539 ; dernier close 179.94)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 19% · rebond 55% · **stop −3.36%** sous le fill (sous le bruit) · cible +1.02% · R/R 0.3 (high win-rate)
- Gaps overnight (n=159) : méd. -0.09% · baisse 54% (gap-down >1% 25% · >2% 12%)
- Excursion ouverture 5min (n=160) : bas méd −0.81% (p90 −2.04%) · haut méd +0.96% · range méd 1.97%
- Excursion ouverture 15min (n=160) : bas méd −0.85% (p90 −2.8%) · haut méd +1.17% · range méd 2.39%
- Excursion ouverture 30min (n=160) : bas méd −1.07% (p90 −3.47%) · haut méd +1.22% · range méd 2.71%
- Excursion ouverture 60min (n=160) : bas méd −1.33% (p90 −3.63%) · haut méd +1.39% · range méd 3.01%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 179.94 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 76% (119/159) · gap 36% · délai 0.0min · rebond 59% (66/119) (MFE +1.23%)
   - −1.0% : fill 30min 54% · séance 65% (108/159) · gap 25% · délai 0.0min · rebond 64% (65/108) (MFE +1.41%)
   - −1.5% : fill 30min 43% · séance 54% (93/159) · gap 20% · délai 0.8min · rebond 68% (62/93) (MFE +1.37%)
   - −2.0% : fill 30min 36% · séance 47% (79/159) · gap 12% · délai 1.8min · rebond 65% (50/79) (MFE +1.43%)
   - −3.0% : fill 30min 21% · séance 30% (55/159) · gap 7% · délai 5.0min · rebond 56% (27/55) (MFE +1.44%)
   - −4.0% : fill 30min 14% · séance 19% (38/159) · gap 4% · délai 11.2min · rebond 55% (19/38) (MFE +1.02%)
   - −5.0% : fill 30min 9% · séance 15% (27/159) · gap 1% · délai 25.2min · rebond 51% (13/27) (MFE +1.02%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.41% (p90 −2.0%) → stop au-delà de −1.25% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.68% (p90 −1.82%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −1.37%) → stop au-delà de −1.05% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=553 jambes) : jambe baissière méd −1.04% (p90 −2.46%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (74 séances) :
      · −1.0% : fill 91% (70/74) · rebond 65% (43/70)
      · −2.0% : fill 73% (58/74) · rebond 67% (38/58)
      · −3.0% : fill 52% (41/74) · rebond 54% (20/41)
      · −4.0% : fill 35% (30/74) · rebond 51% (14/30)
      · −5.0% : fill 29% (23/74) · rebond 58% (12/23)
   - **flat** (27 séances) :
      · −1.0% : fill 66% (21/27) · rebond 36% (9/21)
      · −2.0% : fill 55% (14/27) · rebond 53% (8/14)
      · −3.0% : fill 29% (10/27) · rebond 57% (5/10)
      · −4.0% : fill 18% (7/27) · rebond 84% (5/7)
      · −5.0% : fill 9% (3/27) · rebond 9% (1/3)
   - **gap-up** (58 séances) :
      · −1.0% : fill 33% (17/58) · rebond 82% (13/17)
      · −2.0% : fill 12% (7/58) · rebond 72% (4/7)
      · −3.0% : fill 5% (4/58) · rebond 73% (2/4)
      · −4.0% : fill 1% (1/58) · rebond 0% (0/1)
      · −5.0% : fill 1% (1/58) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 53% en base · 70% si les 15 1res min sont vertes (80 cas) · 34% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:38** → P(séance verte=clôture>ouverture) 84% si début vert vs 24% si rouge (base 53% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **84%** · continue >prix actuel 55% ; creux résiduel méd -0.94% (q20 -1.73%) → **SL/trailing à −1.73%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.4% / q75 +2.22% → **scale +1.4% / runner +2.22%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **24%** (continue à baisser 40%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.58%** (au-delà de la MAE q10 -2.58%), cible rebond +1.32% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.67% .. +3.82%] · haut q95 +4.25% · bas q05 -4.05%
   - 60min (n=160) : retour [-3.62% .. +3.98%] · haut q95 +4.9% · bas q05 -4.38%
   - 2h (n=160) : retour [-3.91% .. +5.61%] · haut q95 +6.6% · bas q05 -4.56%
   - 4h (n=160) : retour [-4.25% .. +5.66%] · haut q95 +6.64% · bas q05 -5.5%
   - 6h (n=160) : retour [-4.6% .. +6.2%] · haut q95 +7.22% · bas q05 -5.61%
   - session (n=160) : retour [-4.24% .. +6.06%] · haut q95 +7.22% · bas q05 -5.63%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 3.1% / strong 3.7%) · base = 11 séances trend-up (n_eff 7.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **41%**. Lecture précoce 30 min : signature présente → 19% vs absente 4% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.86% (p75 1.39% / p90 1.52%) · ~2.55 replis/séance, durée méd 75.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **78%** (reprise méd 33.99 min, n=35)
   - −1.0% → **41%** (reprise méd 64.44 min, n=10)
   - −1.5% → **18%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.52%** (p90, défaut prudent ; serré/agressif −1.39%) ; extension open→close méd +4.67% (q75 +7.59% / q95 +12.13%), MFE méd +6.82% / q90 +12.87%
   - Échelle scale-out : +6.82% (33%) / +8.47% (33%) / +12.87% (34%)
- **DÉSARMER** : repli > **−1.52%** depuis le plus-haut = décay → P(retournement) **64%** (préavis méd 92.5 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.87% : P(retournement après) 0% (mèche méd 1.36%)
- **CONTEXTE** : la dernière heure tient les gains 70% du temps (retour médian dernière heure +0.36%)


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 79.0  _(surachat)_
- **ADX** : 32.6  _(tendance etablie)_
- **MACD** : hist 1.092  _(pas de croisement recent)_
- **BB** : %B 0.75 · largeur 57.6%
- **ATR** : 9.61 (92.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.227  _(accumulation)_
- **Vol ratio** : 0.86  _(volume normal)_
- **Choppiness** : 46.8  _(transition)_
- **MA** : MA20 157.27 · MA50 138.93 · MA200 151.51  _(prix > MA20)_
- **Dist MA** : MA20 +14.4% · MA50 +29.5% · MA200 +18.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (811569 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
