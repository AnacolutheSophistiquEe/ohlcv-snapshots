# PLTR

**Generated** : 2026-08-24T22:02:38.759129+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $175.89  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $175.89 (+9.8% vs entrée) · entrée $160.17 · stop $145.26 · T1 $193.00 · R/R 2.2  
> ↳ P(T1 av. stop) 4 % · EV/risk -0.043 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $157.56–$162.78 (mid $160.17)
- Spot actuel : $175.89 (+9.8% au-dessus de la zone — repli à attendre)
- Stop : $145.26 (stop swing_plan-based (-17.41%))
- Targets : T1 $193.00 · R/R 2.2 | T2 $196.11 · R/R 2.41 | T3 $199.22 · R/R 2.62
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $145.26


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.79 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (17.41 %)** : le gap seul le franchit 0.08 % des séances (1 fois sur 1253).
   - exécution **0.522 pt plus bas** dans le cas TYPIQUE (médiane), 0.522 au p90, **0.522 au pire**
   - perte réelle **17.932 %** en moyenne _(tirée par la queue)_, jusqu'à **17.932 %** — au lieu des 17.41 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0004 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.882 % | p01 -6.139 % | pire -17.932 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0888** [0.0532 ; 0.138] _(largeur 8.5 pt, n_eff 173.1)_
   - swing : **0.4212** [0.37 ; 0.4737] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.4997** [0.4472 ; 0.5522] _(largeur 10.5 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.17 %** | CVaR **-8.43 %** | vol 4.27 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.44 % vs -13.82 % si l'on extrapolait par √5 _(rapport 0.972 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7041** (β de hausse 1.4118, asymétrie 1.207) vs IWM — 602 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 155.394 sur atr_grid (2.75 ATR, 11.653 %) — p(stop avant cible) 0.2661 [0.22 ; 0.31], R/R 0.923, perte reelle 14.376 % (gap inclus), CVaR 11.662 %, EV 0.238 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.92 < plancher 1.60 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 1.02 ATR (stop 6.284 %) — p(stop avant cible) 0.5107 [0.46 ; 0.56], R/R 1.288, perte reelle 10.298 % (gap inclus), EV -1.1889 % — **REFUSE**
      - refuse : p_stop_first 0.511, borne haute 0.563 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.29 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.19 %) : P(cible) 24.9 % x 13.26 % + P(rien) 24.0 % x 3.19 % ne couvrent pas P(stop) 51.1 % x 10.30 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 3.94 ATR (stop 18.635 %) — p(stop avant cible) 0.0899 [0.06 ; 0.12], R/R 0.712, perte reelle 18.635 % (gap inclus), EV 1.0792 % — **REFUSE**
      - refuse : R/R 0.71 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.63 % > budget 12.00 %
   - 🟢 support a 7.78 ATR (stop 34.933 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.38, perte reelle 34.933 % (gap inclus), EV 1.5634 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.93 % > budget 12.00 %
   - 🟢 support a 9.33 ATR (stop 41.482 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.32, perte reelle 41.482 % (gap inclus), EV 1.5699 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.48 % > budget 12.00 %
   - ⚪ atr_grid a 1.75 ATR (stop 7.415 %) — p(stop avant cible) 0.4276 [0.38 ; 0.48], R/R 1.107, perte reelle 11.982 % (gap inclus), EV -0.6629 % — **REFUSE**
      - refuse : R/R 1.11 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.66 %) : P(cible) 27.9 % x 13.26 % + P(rien) 29.3 % x 2.59 % ne couvrent pas P(stop) 42.8 % x 11.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 9.534 %) — p(stop avant cible) 0.3471 [0.30 ; 0.40], R/R 1.01, perte reelle 13.126 % (gap inclus), EV -0.2873 % — **REFUSE**
      - refuse : R/R 1.01 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.29 %) : P(cible) 28.2 % x 13.26 % + P(rien) 37.1 % x 1.44 % ne couvrent pas P(stop) 34.7 % x 13.13 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 11.653 %) — p(stop avant cible) 0.2661 [0.22 ; 0.31], R/R 0.923, perte reelle 14.376 % (gap inclus), EV 0.238 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 12.712 %) — p(stop avant cible) 0.2246 [0.18 ; 0.27], R/R 0.877, perte reelle 15.126 % (gap inclus), EV 0.4705 % — **REFUSE**
      - refuse : R/R 0.88 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.72 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 14.831 %) — p(stop avant cible) 0.1576 [0.12 ; 0.20], R/R 0.74, perte reelle 17.932 % (gap inclus), EV 0.4612 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.83 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 21.187 %) — p(stop avant cible) 0.0382 [0.02 ; 0.06], R/R 0.626, perte reelle 21.187 % (gap inclus), EV 1.376 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.19 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 23.305 %) — p(stop avant cible) 0.0198 [0.01 ; 0.04], R/R 0.569, perte reelle 23.305 % (gap inclus), EV 1.4625 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.31 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 25.424 %) — p(stop avant cible) 0.0075 [0.00 ; 0.02], R/R 0.522, perte reelle 25.424 % (gap inclus), EV 1.5307 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.42 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 27.543 %) — p(stop avant cible) 0.0045 [0.00 ; 0.02], R/R 0.482, perte reelle 27.543 % (gap inclus), EV 1.5618 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.54 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 29.661 %) — p(stop avant cible) 0.0037 [0.00 ; 0.01], R/R 0.447, perte reelle 29.661 % (gap inclus), EV 1.5568 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.66 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 31.78 %) — p(stop avant cible) 0.0029 [0.00 ; 0.01], R/R 0.417, perte reelle 31.78 % (gap inclus), EV 1.5584 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.78 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.045 | EV/share : $0.675 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 5 % | T2 5 % | T3 3 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 22.2 | side 72.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 528.0 (= 3 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=12, n_eff=8))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=3))
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
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : stretched_up
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

- **RSI** : 60.9  _(momentum haussier)_
- **ADX** : 33.3  _(tendance etablie)_
- **MACD** : hist 0.583  _(pas de croisement recent)_
- **BB** : %B 0.68 · largeur 55.6%
- **ATR** : 7.45 (60.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF 0.207  _(accumulation)_
- **Vol ratio** : 0.74  _(volume normal)_
- **Choppiness** : 47.6  _(transition)_
- **MA** : MA20 159.49 · MA50 139.83 · MA200 151.43  _(prix > MA20)_
- **Dist MA** : MA20 +10.3% · MA50 +25.8% · MA200 +16.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (824448 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
