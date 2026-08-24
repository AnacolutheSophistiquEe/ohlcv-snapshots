# IONQ

**Generated** : 2026-08-24T00:27:29.215316+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $44.86  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $44.86 (+1.4% vs entrée) · entrée $44.25 · stop $43.39 · T1 $45.65 · R/R 1.63  
> ↳ P(T1 av. stop) 25 % _(réel 5 s)_ · EV/risk -0.035 _(réel 5 s)_ (GBM 0.124) · ¼-Kelly 0.029 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.95% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $43.97–$44.53 (mid $44.25)
- Spot actuel : $44.86 (+1.4% au-dessus de la zone — repli à attendre)
- Stop : $43.39 (stop swing_plan-based (-9.4%))
- Targets : T1 $45.65 · R/R 1.63 | T2 $47.04 · R/R 3.24 | T3 $48.44 · R/R 4.87
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $43.39


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.69 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.4 %)** : le gap seul le franchit 0.319 % des séances (4 fois sur 1254).
   - exécution **2.293 pt plus bas** dans le cas TYPIQUE (médiane), 9.485 au p90, **12.459 au pire**
   - perte réelle **13.966 %** en moyenne _(tirée par la queue)_, jusqu'à **21.859 %** — au lieu des 9.4 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0146 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.033 % | p01 -6.63 % | pire -21.859 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2897** [0.226 ; 0.3603] _(largeur 13.4 pt, n_eff 173.1)_
   - swing : **0.5485** [0.4958 ; 0.6004] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.571** [0.5184 ; 0.6224] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (34.6 pt), swing (35.6 pt), deep (32.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-8.5 %** | CVaR **-10.11 %** | vol 6.18 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 9.84 % contre 5.89 % aujourd'hui, rapport 1.67)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -18.22 % vs -19.88 % si l'on extrapolait par √5 _(rapport 0.917 ; < 1 = le √5 surestime)_
- **β de baisse : 2.2336** (β de hausse 1.9862, asymétrie 1.1246) vs IWM — 601 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 40.6236 sur sr_based (0.95 ATR, 9.444 %) — p(stop avant cible) 0.5925 [0.54 ; 0.64], R/R 2.222, perte reelle 13.966 % (gap inclus), CVaR 9.458 %, EV -1.5997 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0389 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 14.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.593, borne haute 0.643 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 9.46 % > budget 5.06 %
- Budget de queue : **5.06 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.212 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 42.8 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.95 ATR (stop 9.444 %) — p(stop avant cible) 0.5925 [0.54 ; 0.64], R/R 2.222, perte reelle 13.966 % (gap inclus), EV -1.5997 % — **REFUSE**
      - refuse : cible atteinte seulement 14.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.593, borne haute 0.643 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 9.46 % > budget 5.06 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.60 %) : P(cible) 14.2 % x 31.04 % + P(rien) 26.5 % x 8.52 % ne couvrent pas P(stop) 59.2 % x 13.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 support a 2.39 ATR (stop 18.655 %) — p(stop avant cible) 0.2563 [0.21 ; 0.30], R/R 1.42, perte reelle 21.859 % (gap inclus), EV 0.3686 % — **REFUSE**
      - refuse : R/R 1.42 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.66 % > budget 5.06 %
      - ⚠ support DETECTE a 0.85 ATR du spot — compartiment <1, mesure a 51.0 % de casse (IC clusterise [0.478 ; 0.541] sur 1127 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 3.72 ATR (stop 27.171 %) — p(stop avant cible) 0.0814 [0.06 ; 0.11], R/R 1.142, perte reelle 27.171 % (gap inclus), EV 1.4015 % — **REFUSE**
      - refuse : R/R 1.14 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.17 % > budget 5.06 %
   - ⚪ swing_based a 4.74 ATR (stop 33.735 %) — p(stop avant cible) 0.0284 [0.01 ; 0.05], R/R 0.92, perte reelle 33.735 % (gap inclus), EV 1.348 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.74 % > budget 5.06 %
   - 🟢 support a 5.17 ATR (stop 36.511 %) — p(stop avant cible) 0.0156 [0.01 ; 0.03], R/R 0.85, perte reelle 36.511 % (gap inclus), EV 1.3996 % — **REFUSE**
      - refuse : R/R 0.85 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.51 % > budget 5.06 %
   - ⚪ atr_grid a 1.75 ATR (stop 11.211 %) — p(stop avant cible) 0.5245 [0.47 ; 0.58], R/R 2.058, perte reelle 15.082 % (gap inclus), EV -0.9571 % — **REFUSE**
      - refuse : cible atteinte seulement 14.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.524, borne haute 0.577 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 11.22 % > budget 5.06 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.96 %) : P(cible) 14.7 % x 31.04 % + P(rien) 32.8 % x 7.26 % ne couvrent pas P(stop) 52.4 % x 15.08 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 12.813 %) — p(stop avant cible) 0.4586 [0.41 ; 0.51], R/R 1.42, perte reelle 21.859 % (gap inclus), EV -3.1273 % — **REFUSE**
      - refuse : R/R 1.42 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.82 % > budget 5.06 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.13 %) : P(cible) 15.3 % x 31.04 % + P(rien) 38.9 % x 5.56 % ne couvrent pas P(stop) 45.9 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 38.439 %) — p(stop avant cible) 0.0102 [0.00 ; 0.03], R/R 0.807, perte reelle 38.439 % (gap inclus), EV 1.4155 % — **REFUSE**
      - refuse : R/R 0.81 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.44 % > budget 5.06 %
   - ⚪ atr_grid a 6.5 ATR (stop 41.642 %) — p(stop avant cible) 0.0049 [0.00 ; 0.02], R/R 0.745, perte reelle 41.642 % (gap inclus), EV 1.4174 % — **REFUSE**
      - refuse : R/R 0.75 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.64 % > budget 5.06 %
   - ⚪ atr_grid a 7.0 ATR (stop 44.845 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 0.692, perte reelle 44.845 % (gap inclus), EV 1.4455 % — **REFUSE**
      - refuse : R/R 0.69 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.85 % > budget 5.06 %
   - ⚪ atr_grid a 7.5 ATR (stop 48.048 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 0.646, perte reelle 48.048 % (gap inclus), EV 1.4666 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 48.05 % > budget 5.06 %
   - ⚪ atr_grid a 8.0 ATR (stop 51.252 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.606, perte reelle 51.252 % (gap inclus), EV 1.4838 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 51.25 % > budget 5.06 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.124 | EV/share : $0.107 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 28 % | T3 28 %
- Kelly (position) : f* 0.115 | ¼-Kelly 0.029 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 60.5 | bear 32.3 | side 7.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 359.0 (= 8 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.358% → cible +3.157% / stop −1.948%, p_fill 68%, n_eff≈29.4) : P(cible|rempli) **25%** · **EV/risk -0.035** (×p_fill ; si rempli -0.10% du capital)
  - **swing** (entrée dip −2.994% → cible +7.059% / stop −6.604%, p_fill 58%, n_eff≈27.5) : P(cible|rempli) **56%** · **EV/risk +0.058** (×p_fill ; si rempli +0.67% du capital)
  - **deep** (entrée dip −4.62% → cible +9.984% / stop −10.076%, p_fill 61%, n_eff≈33.2) : P(cible|rempli) **51%** · **EV/risk -0.060** (×p_fill ; si rempli -1.00% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→82% · +2.0%→68% · +3.0%→59% · +5.0%→32% · +8.0%→15%
- Range intraday médian 7.64% (p90 12.17%) · excursion haute méd. +3.66% / basse méd. −2.75%
- Profil de vol intra : ouverture 5.31% vs midi 1.497% vs clôture 1.685% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 70% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.115 ; neutre — autocorr 0.011)_ ; drift intra méd. 0.322% ; recovery-V 29%
- **σ réalisé intraday** 4.532% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 50% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 44.7594 (VA 44.1094–45.0844 ; dernier close 44.85)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 35% · rebond 86% · **stop −5.07%** sous le fill (sous le bruit) · cible +2.81% · R/R 0.55 (high win-rate)
- Gaps overnight (n=159) : méd. -0.39% · baisse 54% (gap-down >1% 37% · >2% 18%)
- Excursion ouverture 5min (n=160) : bas méd −1.16% (p90 −2.83%) · haut méd +1.33% · range méd 2.79%
- Excursion ouverture 15min (n=160) : bas méd −1.59% (p90 −4.01%) · haut méd +1.52% · range méd 3.72%
- Excursion ouverture 30min (n=160) : bas méd −1.91% (p90 −5.15%) · haut méd +2.05% · range méd 4.53%
- Excursion ouverture 60min (n=160) : bas méd −2.25% (p90 −5.61%) · haut méd +2.32% · range méd 5.28%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 44.85 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 73% · séance 82% (133/159) · gap 47% · délai 0.0min · rebond 63% (88/133) (MFE +1.89%)
   - −1.0% : fill 30min 69% · séance 75% (125/159) · gap 37% · délai 0.0min · rebond 72% (91/125) (MFE +2.35%)
   - −1.5% : fill 30min 62% · séance 69% (118/159) · gap 32% · délai 0.0min · rebond 64% (79/118) (MFE +2.1%)
   - −2.0% : fill 30min 55% · séance 63% (108/159) · gap 18% · délai 0.1min · rebond 72% (75/108) (MFE +2.31%)
   - −3.0% : fill 30min 46% · séance 55% (94/159) · gap 9% · délai 6.6min · rebond 74% (69/94) (MFE +2.49%)
   - −4.0% : fill 30min 30% · séance 43% (76/159) · gap 6% · délai 15.5min · rebond 74% (58/76) (MFE +2.72%)
   - −5.0% : fill 30min 18% · séance 35% (64/159) · gap 3% · délai 24.8min · rebond 86% (56/64) (MFE +2.81%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.75% (p90 −2.89%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.88% (p90 −3.23%) → stop au-delà de −2.34% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.82% (p90 −2.73%) → stop au-delà de −1.84% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1125 jambes) : jambe baissière méd −1.31% (p90 −3.14%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (78 séances) :
      · −1.0% : fill 100% (78/78) · rebond 73% (58/78)
      · −2.0% : fill 90% (72/78) · rebond 77% (55/72)
      · −3.0% : fill 78% (63/78) · rebond 76% (48/63)
      · −4.0% : fill 60% (48/78) · rebond 76% (38/48)
      · −5.0% : fill 48% (40/78) · rebond 80% (33/40)
   - **flat** (15 séances) :
      · −1.0% : fill 77% (12/15) · rebond 62% (7/12)
      · −2.0% : fill 66% (11/15) · rebond 74% (5/11)
      · −3.0% : fill 60% (9/15) · rebond 43% (4/9)
      · −4.0% : fill 60% (9/15) · rebond 51% (4/9)
      · −5.0% : fill 44% (8/15) · rebond 95% (7/8)
   - **gap-up** (66 séances) :
      · −1.0% : fill 43% (35/66) · rebond 74% (26/35)
      · −2.0% : fill 28% (25/66) · rebond 52% (15/25)
      · −3.0% : fill 24% (22/66) · rebond 79% (17/22)
      · −4.0% : fill 19% (19/66) · rebond 79% (16/19)
      · −5.0% : fill 17% (16/66) · rebond 100% (16/16)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 58% si les 15 1res min sont vertes (80 cas) · 32% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **39min** → P(séance verte=clôture>ouverture) 70% si début vert vs 22% si rouge (base 46% · écart 48 pts) ; prédictivité sature ensuite (plafond brut 234min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **70%** · continue >prix actuel 43% ; creux résiduel méd -2.94% (q20 -4.58%) → **SL/trailing à −4.58%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.03% / q75 +4.69% → **scale +2.03% / runner +4.69%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **22%** (continue à baisser 54%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.74%** (au-delà de la MAE q10 -4.74%), cible rebond +2.07% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.1% .. +6.84%] · haut q95 +7.86% · bas q05 -5.64%
   - 60min (n=160) : retour [-4.98% .. +6.12%] · haut q95 +8.41% · bas q05 -6.18%
   - 2h (n=160) : retour [-6.38% .. +7.84%] · haut q95 +9.04% · bas q05 -7.04%
   - 4h (n=160) : retour [-7.04% .. +7.21%] · haut q95 +10.16% · bas q05 -8.09%
   - 6h (n=160) : retour [-7.2% .. +8.45%] · haut q95 +10.89% · bas q05 -8.3%
   - session (n=160) : retour [-6.6% .. +8.94%] · haut q95 +11.03% · bas q05 -8.35%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 7.7)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **30%**. Lecture précoce 30 min : signature présente → 15% vs absente 4% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.29% (p75 2.28% / p90 3.82%) · ~3.0 replis/séance, durée méd 69.04 min. P(nouveau plus-haut après repli) :
   - −0.5% → **85%** (reprise méd 24.37 min, n=47)
   - −1.0% → **78%** (reprise méd 68.85 min, n=30)
   - −1.5% → **68%** (reprise méd 81.24 min, n=16)
   - −2.0% → **67%** (reprise méd 84.17 min, n=12)
   - −3.0% → **75%** (reprise méd 175.72 min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−3.82%** (p90, défaut prudent ; serré/agressif −2.28%) ; extension open→close méd +8.23% (q75 +10.03% / q95 +16.4%), MFE méd +10.28% / q90 +13.1%
   - Échelle scale-out : +10.28% (33%) / +11.83% (33%) / +13.1% (34%)
- **DÉSARMER** : repli > **−3.82%** depuis le plus-haut = décay → P(retournement) **30%** (préavis méd 235.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.1% : P(retournement après) 0% (mèche méd 3.44%)
- **CONTEXTE** : la dernière heure tient les gains 80% du temps (retour médian dernière heure +0.52%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 62.1  _(momentum haussier)_
- **ADX** : 21.4  _(pas de tendance nette)_
- **MACD** : hist 0.607  _(pas de croisement recent)_
- **BB** : %B 0.72 · largeur 42.3%
- **ATR** : 2.87 (18.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.075  _(accumulation)_
- **Vol ratio** : 0.93  _(volume normal)_
- **Choppiness** : 59.5  _(transition)_
- **MA** : MA20 41.09 · MA50 44.54 · MA200 44.86  _(prix > MA20)_
- **Dist MA** : MA20 +9.2% · MA50 +0.7% · MA200 -0.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (816782 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
