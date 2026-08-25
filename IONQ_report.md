# IONQ

**Generated** : 2026-08-25T00:27:37.322026+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $41.06  

> 🟡 **WAIT-FOR-DIP** — spot +3.0 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $41.06 (+3.0% vs entrée) · entrée $39.86 · stop $35.52 · T1 $48.54 · R/R 2.0  
> ↳ P(T1 av. stop) 6 % _(réel 5 s)_ · EV/risk 0.005 _(réel 5 s)_ (GBM -0.04) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $39.28–$40.44 (mid $39.86)
- Spot actuel : $41.06 (+3.0% au-dessus de la zone — repli à attendre)
- Stop : $35.52 (stop swing_plan-based (-13.48%))
- Targets : T1 $48.54 · R/R 2.0 | T2 $48.55 · R/R 2.0 | T3 $48.55 · R/R 2.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $35.52


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.78 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (13.48 %)** : le gap seul le franchit 0.08 % des séances (1 fois sur 1253).
   - exécution **8.379 pt plus bas** dans le cas TYPIQUE (médiane), 8.379 au p90, **8.379 au pire**
   - perte réelle **21.859 %** en moyenne _(tirée par la queue)_, jusqu'à **21.859 %** — au lieu des 13.48 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0067 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.035 % | p01 -6.632 % | pire -21.859 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2864** [0.223 ; 0.3569] _(largeur 13.4 pt, n_eff 173.1)_
   - swing : **0.5511** [0.4984 ; 0.6029] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.5677** [0.5151 ; 0.6192] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (34.7 pt), swing (33.9 pt), deep (32.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-8.47 %** | CVaR **-10.08 %** | vol 6.18 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 9.88 % contre 5.94 % aujourd'hui, rapport 1.66)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -18.23 % vs -19.88 % si l'on extrapolait par √5 _(rapport 0.917 ; < 1 = le √5 surestime)_
- **β de baisse : 2.2272** (β de hausse 1.9833, asymétrie 1.123) vs IWM — 602 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 35.9431 sur atr_grid (1.75 ATR, 12.462 %) — p(stop avant cible) 0.4587 [0.41 ; 0.51], R/R 1.362, perte reelle 21.859 % (gap inclus), CVaR 12.469 %, EV -3.1465 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.0391 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : R/R 1.36 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 12.47 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 23 des 23 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 51.1 % de la queue et il ne reste que 2.34 EUR a partager. Prix du risque 0.001 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 1.05 ATR (stop 9.525 %) — p(stop avant cible) 0.5852 [0.53 ; 0.64], R/R 2.132, perte reelle 13.966 % (gap inclus), EV -1.4838 % — **REFUSE**
      - refuse : p_stop_first 0.585, borne haute 0.636 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.74 ATR du spot — compartiment <1, mesure a 47.2 % de casse (IC clusterise [0.436 ; 0.506] sur 1081 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.48 %) : P(cible) 15.7 % x 29.77 % + P(rien) 25.8 % x 7.84 % ne couvrent pas P(stop) 58.5 % x 13.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.35 ATR (stop 18.828 %) — p(stop avant cible) 0.2418 [0.20 ; 0.29], R/R 1.362, perte reelle 21.859 % (gap inclus), EV 0.5988 % — **REFUSE**
      - refuse : R/R 1.36 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.83 % > budget 12.00 %
   - ⚪ swing_based a 3.36 ATR (stop 26.025 %) — p(stop avant cible) 0.0997 [0.07 ; 0.13], R/R 1.144, perte reelle 26.025 % (gap inclus), EV 1.4223 % — **REFUSE**
      - refuse : R/R 1.14 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.02 % > budget 12.00 %
   - 🟢 support a 3.79 ATR (stop 29.033 %) — p(stop avant cible) 0.0748 [0.05 ; 0.11], R/R 1.026, perte reelle 29.033 % (gap inclus), EV 1.2847 % — **REFUSE**
      - refuse : R/R 1.03 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.03 % > budget 12.00 %
   - ⚪ atr_grid a 1.75 ATR (stop 12.462 %) — p(stop avant cible) 0.4587 [0.41 ; 0.51], R/R 1.362, perte reelle 21.859 % (gap inclus), EV -3.1465 % — **REFUSE**
      - refuse : R/R 1.36 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.47 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.15 %) : P(cible) 16.9 % x 29.77 % + P(rien) 37.3 % x 5.00 % ne couvrent pas P(stop) 45.9 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 21.363 %) — p(stop avant cible) 0.1909 [0.15 ; 0.23], R/R 1.362, perte reelle 21.859 % (gap inclus), EV 1.2809 % — **REFUSE**
      - refuse : R/R 1.36 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.36 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 32.045 %) — p(stop avant cible) 0.0436 [0.03 ; 0.07], R/R 0.929, perte reelle 32.045 % (gap inclus), EV 1.32 % — **REFUSE**
      - refuse : R/R 0.93 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.05 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 35.606 %) — p(stop avant cible) 0.0163 [0.01 ; 0.03], R/R 0.836, perte reelle 35.606 % (gap inclus), EV 1.4209 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.61 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 39.166 %) — p(stop avant cible) 0.0075 [0.00 ; 0.02], R/R 0.76, perte reelle 39.166 % (gap inclus), EV 1.4216 % — **REFUSE**
      - refuse : R/R 0.76 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.17 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 42.727 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.697, perte reelle 42.727 % (gap inclus), EV 1.4569 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.73 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 46.287 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 0.643, perte reelle 46.287 % (gap inclus), EV 1.4543 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.29 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 49.848 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.597, perte reelle 49.848 % (gap inclus), EV 1.4943 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.85 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 53.408 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.558, perte reelle 53.408 % (gap inclus), EV 1.4943 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 53.41 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 56.969 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.523, perte reelle 56.969 % (gap inclus), EV 1.4943 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 56.97 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : -0.04 | EV/share : $-0.172 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 13 % | T2 13 % | T3 13 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 57.9 | bear 28.8 | side 13.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 123.0 (= 3 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.324% → cible +3.25% / stop −2.165%, p_fill 68%, n_eff≈29.4) : P(cible|rempli) **24%** · **EV/risk -0.075** (×p_fill ; si rempli -0.24% du capital)
  - **swing** (entrée dip −2.916% → cible +21.763% / stop −10.881%, p_fill 60%, n_eff≈28.4) : P(cible|rempli) **6%** · **EV/risk +0.005** (×p_fill ; si rempli +0.09% du capital)
  - **deep** (entrée dip −4.508% → cible +10.278% / stop −11.186%, p_fill 61%, n_eff≈33.5) : P(cible|rempli) **51%** · **EV/risk -0.071** (×p_fill ; si rempli -1.30% du capital)
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
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 48.7  _(neutre)_
- **ADX** : 19.9  _(pas de tendance nette)_
- **MACD** : hist 0.31  _(pas de croisement recent)_
- **BB** : %B 0.48 · largeur 40.4%
- **ATR** : 2.92 (19.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.03  _(neutre)_
- **Vol ratio** : 0.83  _(volume normal)_
- **Choppiness** : 60.5  _(transition)_
- **MA** : MA20 41.35 · MA50 44.21 · MA200 44.8  _(prix < MA20)_
- **Dist MA** : MA20 -0.7% · MA50 -7.1% · MA200 -8.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (806879 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
