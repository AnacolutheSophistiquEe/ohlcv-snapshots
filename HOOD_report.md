# HOOD

**Generated** : 2026-08-24T00:32:57.929180+00:00  
**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $108.13  

> 🟡 **WAIT-FOR-DIP** — spot +1.1 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $108.13 (+1.1% vs entrée) · entrée $106.92 · stop $103.71 · T1 $112.34 · R/R 1.69  
> ↳ P(T1 av. stop) 11 % _(réel 5 s)_ · EV/risk 0.012 _(réel 5 s)_ (GBM 0.066) · ¼-Kelly 0.013 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.070 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._
- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : RSI 71.1 > 70 (surachat) ; %B 1.27 (collé à la bande haute) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $106.43–$107.40 (mid $106.92)
- Spot actuel : $108.13 (+1.1% au-dessus de la zone — repli à attendre)
- Stop : $103.71 (stop swing_plan-based (-7.35%))
- Targets : T1 $112.34 · R/R 1.69 | T2 $113.23 · R/R 1.97 | T3 $114.12 · R/R 2.24
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $103.71


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.10 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.35 %)** : le gap seul le franchit 1.037 % des séances (13 fois sur 1254).
   - exécution **2.64 pt plus bas** dans le cas TYPIQUE (médiane), 6.331 au p90, **10.435 au pire**
   - perte réelle **10.494 %** en moyenne _(tirée par la queue)_, jusqu'à **17.785 %** — au lieu des 7.35 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0326 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 13 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.456 % | p01 -7.299 % | pire -17.785 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1432** [0.0971 ; 0.2011] _(largeur 10.4 pt, n_eff 173.1)_
   - swing : **0.515** [0.4624 ; 0.5674] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.5549** [0.5022 ; 0.6066] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (32.2 pt), swing (36.7 pt), deep (37.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-6.19 %** | CVaR **-9.11 %** | vol 4.33 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 2.01 % contre 4.47 % aujourd'hui, rapport 0.45)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.53 % vs -14.49 % si l'on extrapolait par √5 _(rapport 1.003 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7606** (β de hausse 1.6089, asymétrie 1.0943) vs IWM — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.519× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 99.3303 sur support (1.14 ATR, 8.138 %) — p(stop avant cible) 0.4641 [0.41 ; 0.52], R/R 1.084, perte reelle 11.287 % (gap inclus), CVaR 8.163 %, EV -0.7376 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.1944 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : R/R 1.08 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 8.16 % > budget 3.72 %
- Budget de queue : **3.72 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.212 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 42.8 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 1.14 ATR (stop 8.138 %) — p(stop avant cible) 0.4641 [0.41 ; 0.52], R/R 1.084, perte reelle 11.287 % (gap inclus), EV -0.7376 % — **REFUSE**
      - refuse : R/R 1.08 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 8.16 % > budget 3.72 %
      - ⚠ support DETECTE a 0.92 ATR du spot — compartiment <1, mesure a 51.0 % de casse (IC clusterise [0.478 ; 0.541] sur 1127 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.74 %) : P(cible) 34.4 % x 12.23 % + P(rien) 19.2 % x 1.55 % ne couvrent pas P(stop) 46.4 % x 11.29 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.91 ATR (stop 16.739 %) — p(stop avant cible) 0.159 [0.12 ; 0.20], R/R 0.688, perte reelle 17.785 % (gap inclus), EV 0.9364 % — **REFUSE**
      - refuse : R/R 0.69 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.74 % > budget 3.72 %
   - ⚪ swing_based a 3.36 ATR (stop 18.972 %) — p(stop avant cible) 0.1053 [0.08 ; 0.14], R/R 0.645, perte reelle 18.972 % (gap inclus), EV 1.1662 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.97 % > budget 3.72 %
   - 🟢 support a 5.53 ATR (stop 29.566 %) — p(stop avant cible) 0.0262 [0.01 ; 0.05], R/R 0.414, perte reelle 29.566 % (gap inclus), EV 1.2026 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.57 % > budget 3.72 %
   - ⚪ atr_grid a 2.0 ATR (stop 9.758 %) — p(stop avant cible) 0.3907 [0.34 ; 0.44], R/R 0.993, perte reelle 12.322 % (gap inclus), EV -0.1207 % — **REFUSE**
      - refuse : R/R 0.99 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 9.77 % > budget 3.72 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 37.0 % x 12.23 % + P(rien) 24.0 % x 0.72 % ne couvrent pas P(stop) 39.1 % x 12.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 10.978 %) — p(stop avant cible) 0.3574 [0.31 ; 0.41], R/R 0.927, perte reelle 13.192 % (gap inclus), EV 0.005 % — **REFUSE**
      - refuse : R/R 0.93 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 10.99 % > budget 3.72 %
   - ⚪ atr_grid a 4.5 ATR (stop 21.955 %) — p(stop avant cible) 0.0688 [0.05 ; 0.10], R/R 0.557, perte reelle 21.955 % (gap inclus), EV 1.187 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.95 % > budget 3.72 %
   - ⚪ atr_grid a 5.0 ATR (stop 24.395 %) — p(stop avant cible) 0.0394 [0.02 ; 0.06], R/R 0.501, perte reelle 24.395 % (gap inclus), EV 1.2189 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.40 % > budget 3.72 %
   - ⚪ atr_grid a 6.5 ATR (stop 31.713 %) — p(stop avant cible) 0.0185 [0.01 ; 0.04], R/R 0.386, perte reelle 31.713 % (gap inclus), EV 1.202 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.71 % > budget 3.72 %
   - ⚪ atr_grid a 7.0 ATR (stop 34.152 %) — p(stop avant cible) 0.0038 [0.00 ; 0.02], R/R 0.358, perte reelle 34.152 % (gap inclus), EV 1.3378 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.15 % > budget 3.72 %
   - ⚪ atr_grid a 7.5 ATR (stop 36.592 %) — p(stop avant cible) 0.0022 [0.00 ; 0.01], R/R 0.334, perte reelle 36.592 % (gap inclus), EV 1.3523 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.59 % > budget 3.72 %
   - ⚪ atr_grid a 8.0 ATR (stop 39.031 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 0.313, perte reelle 39.031 % (gap inclus), EV 1.3597 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.03 % > budget 3.72 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.066 | EV/share : $0.213 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 22 % | T2 22 % | T3 22 %
- Kelly (position) : f* 0.05 | ¼-Kelly 0.013 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 75.4 | bear 19.3 | side 5.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 541.0 (= 5 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.124% → cible +5.07% / stop −3.0%, p_fill 74%, n_eff≈30.8) : P(cible|rempli) **11%** · **EV/risk +0.012** (×p_fill ; si rempli +0.05% du capital)
  - **swing** (entrée dip −2.471% → cible +8.321% / stop −5.002%, p_fill 62%, n_eff≈25.9) : P(cible|rempli) **24%** · **EV/risk -0.044** (×p_fill ; si rempli -0.36% du capital)
  - **deep** (entrée dip −3.818% → cible +16.993% / stop −8.497%, p_fill 51%, n_eff≈24.6) : P(cible|rempli) **16%** · **EV/risk -0.089** (×p_fill ; si rempli -1.49% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→80% · +2.0%→56% · +3.0%→36% · +5.0%→22% · +8.0%→8%
- Range intraday médian 5.11% (p90 8.97%) · excursion haute méd. +2.18% / basse méd. −2.27%
- Profil de vol intra : ouverture 3.796% vs midi 1.047% vs clôture 1.151% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 17% · trend ↑1%/↓0% ; spike-down 68% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; neutre — autocorr -0.001)_ ; drift intra méd. 0.049% ; recovery-V 36%
- **σ réalisé intraday** 3.62% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 44% / bas 46% / whipsaw 8%
- POC intraday (dernière séance, temps-au-prix) : 107.6269 (VA 106.8176–108.4361 ; dernier close 108.13)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 28% · rebond 80% · **stop −4.62%** sous le fill (sous le bruit) · cible +2.37% · R/R 0.51 (high win-rate)
- Gaps overnight (n=159) : méd. 0.04% · baisse 48% (gap-down >1% 32% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.94% (p90 −2.68%) · haut méd +0.93% · range méd 2.18%
- Excursion ouverture 15min (n=160) : bas méd −1.24% (p90 −3.85%) · haut méd +1.26% · range méd 2.84%
- Excursion ouverture 30min (n=160) : bas méd −1.38% (p90 −4.15%) · haut méd +1.7% · range méd 3.44%
- Excursion ouverture 60min (n=160) : bas méd −1.79% (p90 −4.65%) · haut méd +1.73% · range méd 3.9%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 108.13 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 78% (124/159) · gap 39% · délai 0.0min · rebond 58% (66/124) (MFE +1.47%)
   - −1.0% : fill 30min 59% · séance 69% (110/159) · gap 32% · délai 0.0min · rebond 63% (65/110) (MFE +1.54%)
   - −1.5% : fill 30min 50% · séance 59% (100/159) · gap 24% · délai 0.2min · rebond 60% (58/100) (MFE +1.34%)
   - −2.0% : fill 30min 39% · séance 50% (88/159) · gap 16% · délai 0.2min · rebond 68% (55/88) (MFE +1.37%)
   - −3.0% : fill 30min 27% · séance 38% (68/159) · gap 7% · délai 6.5min · rebond 73% (46/68) (MFE +1.84%)
   - −4.0% : fill 30min 17% · séance 28% (50/159) · gap 3% · délai 10.8min · rebond 80% (34/50) (MFE +2.37%)
   - −5.0% : fill 30min 10% · séance 17% (33/159) · gap 2% · délai 19.0min · rebond 76% (25/33) (MFE +2.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.64% (p90 −2.43%) → stop au-delà de −1.57% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.64% (p90 −2.4%) → stop au-delà de −1.73% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −2.43%) → stop au-delà de −1.71% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=768 jambes) : jambe baissière méd −1.13% (p90 −2.84%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (72 séances) :
      · −1.0% : fill 98% (70/72) · rebond 51% (36/70)
      · −2.0% : fill 82% (60/72) · rebond 62% (36/60)
      · −3.0% : fill 69% (50/72) · rebond 70% (33/50)
      · −4.0% : fill 53% (39/72) · rebond 83% (29/39)
      · −5.0% : fill 32% (27/72) · rebond 72% (20/27)
   - **flat** (20 séances) :
      · −1.0% : fill 64% (14/20) · rebond 80% (9/14)
      · −2.0% : fill 40% (11/20) · rebond 61% (7/11)
      · −3.0% : fill 14% (6/20) · rebond 23% (2/6)
      · −4.0% : fill 13% (5/20) · rebond 16% (1/5)
      · −5.0% : fill 6% (3/20) · rebond 82% (2/3)
   - **gap-up** (67 séances) :
      · −1.0% : fill 43% (26/67) · rebond 82% (20/26)
      · −2.0% : fill 22% (17/67) · rebond 90% (12/17)
      · −3.0% : fill 15% (12/67) · rebond 98% (11/12)
      · −4.0% : fill 8% (6/67) · rebond 88% (4/6)
      · −5.0% : fill 4% (3/67) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 67% si les 15 1res min sont vertes (76 cas) · 33% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:23** → P(séance verte=clôture>ouverture) 79% si début vert vs 23% si rouge (base 49% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 227min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **79%** · continue >prix actuel 49% ; creux résiduel méd -1.18% (q20 -2.4%) → **SL/trailing à −2.4%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.27% / q75 +2.68% → **scale +1.27% / runner +2.68%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **23%** (continue à baisser 54%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.54%** (au-delà de la MAE q10 -3.54%), cible rebond +1.71% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.44% .. +4.55%] · haut q95 +5.1% · bas q05 -5.19%
   - 60min (n=160) : retour [-4.07% .. +4.77%] · haut q95 +6.34% · bas q05 -5.74%
   - 2h (n=160) : retour [-4.97% .. +5.19%] · haut q95 +7.59% · bas q05 -6.14%
   - 4h (n=160) : retour [-5.09% .. +6.33%] · haut q95 +8.38% · bas q05 -6.84%
   - 6h (n=160) : retour [-5.77% .. +6.12%] · haut q95 +8.39% · bas q05 -7.13%
   - session (n=160) : retour [-5.53% .. +6.46%] · haut q95 +8.44% · bas q05 -7.22%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.1% des séances sont trend-up (mild 0% / strong 8.1%) · base = 13 séances trend-up (n_eff 8.7)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 19% vs absente 3% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.92% (p75 1.51% / p90 2.85%) · ~3.22 replis/séance, durée méd 36.99 min. P(nouveau plus-haut après repli) :
   - −0.5% → **78%** (reprise méd 18.0 min, n=47)
   - −1.0% → **60%** (reprise méd 33.9 min, n=22)
   - −1.5% → **33%** (reprise méd 52.28 min, n=12)
   - −2.0% → **14%** (reprise méd None min, n=6)
   - −3.0% → **20%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.85%** (p90, défaut prudent ; serré/agressif −1.51%) ; extension open→close méd +6.37% (q75 +9.03% / q95 +12.96%), MFE méd +8.27% / q90 +14.38%
   - Échelle scale-out : +8.27% (33%) / +9.8% (33%) / +14.38% (34%)
- **DÉSARMER** : repli > **−2.85%** depuis le plus-haut = décay → P(retournement) **80%** (préavis méd 259.06 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +14.38% : P(retournement après) 0% (mèche méd 5.8%)
- **CONTEXTE** : la dernière heure tient les gains 83% du temps (retour médian dernière heure +0.49%)


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : stretched_up
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

- **RSI** : 71.1  _(surachat)_
- **ADX** : 15.7  _(pas de tendance nette)_
- **MACD** : hist 1.24  _(pas de croisement recent)_
- **BB** : %B 1.27 · largeur 19.7%
- **ATR** : 5.28 (41.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.07  _(distribution)_
- **Vol ratio** : 2.56  _(volume au-dessus de la moyenne)_
- **Choppiness** : 50.2  _(transition)_
- **MA** : MA20 93.88 · MA50 100.31 · MA200 96.08  _(prix > MA20)_
- **Dist MA** : MA20 +15.2% · MA50 +7.8% · MA200 +12.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (817321 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
