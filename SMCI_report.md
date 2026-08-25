# SMCI

**Generated** : 2026-08-25T00:24:39.899000+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $35.17  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $35.17 (+5.8% vs entrée) · entrée $33.23 · stop $30.68 · T1 $35.75 · R/R 0.99  
> ↳ P(T1 av. stop) 40 % _(réel 5 s)_ · EV/risk -0.034 _(réel 5 s)_ (GBM 0.045) · ¼-Kelly 0.001 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $32.72–$33.73 (mid $33.23)
- Spot actuel : $35.17 (+5.8% au-dessus de la zone — repli à attendre)
- Stop : $30.68 (stop swing_plan-based (-12.76%))
- Targets : T1 $35.75 · R/R 0.99 | T2 $38.27 · R/R 1.98 | T3 $40.79 · R/R 2.96
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $30.68


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.74 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.76 %)** : le gap seul le franchit 0.718 % des séances (9 fois sur 1253).
   - exécution **4.582 pt plus bas** dans le cas TYPIQUE (médiane), 14.538 au p90, **16.291 au pire**
   - perte réelle **19.221 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 12.76 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0464 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 9 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.765 % | p01 -10.307 % | pire -29.051 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.183** [0.1309 ; 0.2456] _(largeur 11.5 pt, n_eff 173.1)_
   - swing : **0.512** [0.4594 ; 0.5644] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.5447** [0.492 ; 0.5966] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (40.0 pt), swing (44.7 pt), deep (38.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.54 %** | CVaR **-12.28 %** | vol 5.74 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 4.21 % contre 7.16 % aujourd'hui, rapport 0.59)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.69 % vs -16.05 % si l'on extrapolait par √5 _(rapport 1.04 ; < 1 = le √5 surestime)_
- **β de baisse : 1.5417** (β de hausse 1.247, asymétrie 1.2364) vs IWM — 602 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.939× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 31.3525 sur atr_based (1.5 ATR, 10.854 %) — p(stop avant cible) 0.3992 [0.35 ; 0.45], R/R 0.947, perte reelle 16.875 % (gap inclus), CVaR 10.916 %, EV -1.2497 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.95 < plancher 1.60 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 23 des 23 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 51.1 % de la queue et il ne reste que 2.34 EUR a partager. Prix du risque 0.001 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 10.854 %) — p(stop avant cible) 0.3992 [0.35 ; 0.45], R/R 0.947, perte reelle 16.875 % (gap inclus), EV -1.2497 % — **REFUSE**
      - refuse : R/R 0.95 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.25 %) : P(cible) 31.9 % x 15.98 % + P(rien) 28.2 % x 1.37 % ne couvrent pas P(stop) 39.9 % x 16.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 1.49 ATR (stop 12.874 %) — p(stop avant cible) 0.3107 [0.26 ; 0.36], R/R 0.832, perte reelle 19.221 % (gap inclus), EV -0.6675 % — **REFUSE**
      - refuse : R/R 0.83 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.92 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.67 %) : P(cible) 33.1 % x 15.98 % + P(rien) 35.9 % x 0.06 % ne couvrent pas P(stop) 31.1 % x 19.22 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.93 ATR (stop 23.317 %) — p(stop avant cible) 0.1295 [0.10 ; 0.17], R/R 0.595, perte reelle 26.856 % (gap inclus), EV 0.8614 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.33 % > budget 12.00 %
   - 🟢 support a 3.83 ATR (stop 29.857 %) — p(stop avant cible) 0.0895 [0.06 ; 0.12], R/R 0.535, perte reelle 29.857 % (gap inclus), EV 0.8856 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.86 % > budget 12.00 %
   - 🟢 support a 4.63 ATR (stop 35.629 %) — p(stop avant cible) 0.0706 [0.05 ; 0.10], R/R 0.449, perte reelle 35.629 % (gap inclus), EV 0.5498 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.63 % > budget 12.00 %
   - ⚪ atr_grid a 1.0 ATR (stop 7.236 %) — p(stop avant cible) 0.5627 [0.51 ; 0.61], R/R 1.18, perte reelle 13.549 % (gap inclus), EV -2.8939 % — **REFUSE**
      - refuse : p_stop_first 0.563, borne haute 0.614 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.18 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.89 %) : P(cible) 26.7 % x 15.98 % + P(rien) 17.0 % x 2.72 % ne couvrent pas P(stop) 56.3 % x 13.55 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 16.282 %) — p(stop avant cible) 0.2233 [0.18 ; 0.27], R/R 0.683, perte reelle 23.404 % (gap inclus), EV -0.2034 % — **REFUSE**
      - refuse : R/R 0.68 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.31 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 33.8 % x 15.98 % + P(rien) 43.9 % x -0.86 % ne couvrent pas P(stop) 22.3 % x 23.40 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 25.327 %) — p(stop avant cible) 0.106 [0.08 ; 0.14], R/R 0.572, perte reelle 27.955 % (gap inclus), EV 0.9723 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.33 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 39.8 %) — p(stop avant cible) 0.0173 [0.01 ; 0.04], R/R 0.402, perte reelle 39.8 % (gap inclus), EV 0.7947 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.80 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 43.418 %) — p(stop avant cible) 0.0037 [0.00 ; 0.01], R/R 0.368, perte reelle 43.418 % (gap inclus), EV 0.8239 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.42 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 47.036 %) — p(stop avant cible) 0.0026 [0.00 ; 0.01], R/R 0.34, perte reelle 47.036 % (gap inclus), EV 0.8159 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.04 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 50.654 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.316, perte reelle 50.654 % (gap inclus), EV 0.8103 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 50.65 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 54.272 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.294, perte reelle 54.272 % (gap inclus), EV 0.8038 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 54.27 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 57.89 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.276, perte reelle 57.89 % (gap inclus), EV 0.8151 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 57.89 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.045 | EV/share : $0.115 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 22 % | T3 15 %
- Kelly (position) : f* 0.004 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 14.2 | bear 5.0 | side 80.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 598.0 (= 17 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.509% → cible +3.394% / stop −2.227%, p_fill 48%, n_eff≈20.3) : P(cible|rempli) **39%** · **EV/risk +0.134** (×p_fill ; si rempli +0.61% du capital)
  - **swing** (entrée dip −5.524% → cible +7.588% / stop −7.659%, p_fill 34%, n_eff≈16.4) : P(cible|rempli) **40%** · **EV/risk -0.034** (×p_fill ; si rempli -0.75% du capital)
  - **deep** (entrée dip −8.535% → cible +10.732% / stop −11.868%, p_fill 34%, n_eff≈18.7) : P(cible|rempli) **73%** · **EV/risk +0.119** (×p_fill ; si rempli +4.12% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→78% · +2.0%→61% · +3.0%→50% · +5.0%→29% · +8.0%→14%
- Range intraday médian 6.69% (p90 11.21%) · excursion haute méd. +3.0% / basse méd. −2.68%
- Profil de vol intra : ouverture 4.16% vs midi 1.286% vs clôture 1.677% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑0%/↓1% ; spike-down 71% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.113 ; mean-reverting — autocorr -0.061)_ ; drift intra méd. 0.054% ; recovery-V 32%
- **σ réalisé intraday** 4.115% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 67% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 36.8811 (VA 36.8514–37.2084 ; dernier close 37.24)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 30% · rebond 81% · **stop −4.21%** sous le fill (sous le bruit) · cible +2.62% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. 0.36% · baisse 44% (gap-down >1% 31% · >2% 17%)
- Excursion ouverture 5min (n=160) : bas méd −0.81% (p90 −2.83%) · haut méd +1.04% · range méd 2.22%
- Excursion ouverture 15min (n=160) : bas méd −1.18% (p90 −3.23%) · haut méd +1.47% · range méd 2.85%
- Excursion ouverture 30min (n=160) : bas méd −1.42% (p90 −3.75%) · haut méd +1.52% · range méd 3.73%
- Excursion ouverture 60min (n=160) : bas méd −1.7% (p90 −4.4%) · haut méd +1.79% · range méd 4.4%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 37.24 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 73% (120/159) · gap 39% · délai 0.0min · rebond 58% (72/120) (MFE +1.3%)
   - −1.0% : fill 30min 52% · séance 69% (111/159) · gap 31% · délai 0.0min · rebond 62% (66/111) (MFE +1.47%)
   - −1.5% : fill 30min 44% · séance 62% (99/159) · gap 22% · délai 0.1min · rebond 65% (60/99) (MFE +1.55%)
   - −2.0% : fill 30min 42% · séance 52% (87/159) · gap 17% · délai 0.8min · rebond 70% (56/87) (MFE +1.75%)
   - −3.0% : fill 30min 32% · séance 48% (76/159) · gap 12% · délai 8.2min · rebond 63% (47/76) (MFE +1.96%)
   - −4.0% : fill 30min 19% · séance 38% (57/159) · gap 6% · délai 26.3min · rebond 74% (37/57) (MFE +1.97%)
   - −5.0% : fill 30min 15% · séance 30% (46/159) · gap 4% · délai 39.5min · rebond 81% (33/46) (MFE +2.62%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −2.86%) → stop au-delà de −1.59% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −3.01%) → stop au-delà de −1.91% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.7% (p90 −2.87%) → stop au-delà de −1.94% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=901 jambes) : jambe baissière méd −1.21% (p90 −2.88%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (71 séances) :
      · −1.0% : fill 96% (69/71) · rebond 50% (37/69)
      · −2.0% : fill 89% (63/71) · rebond 65% (37/63)
      · −3.0% : fill 86% (58/71) · rebond 59% (34/58)
      · −4.0% : fill 69% (45/71) · rebond 73% (29/45)
      · −5.0% : fill 57% (37/71) · rebond 80% (26/37)
   - **flat** (11 séances) :
      · −1.0% : fill 97% (10/11) · rebond 96% (9/10)
      · −2.0% : fill 44% (6/11) · rebond 89% (4/6)
      · −3.0% : fill 28% (3/11) · rebond 100% (3/3)
      · −4.0% : fill 24% (2/11) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/11) · rebond 0% (0/0)
   - **gap-up** (77 séances) :
      · −1.0% : fill 43% (32/77) · rebond 74% (20/32)
      · −2.0% : fill 24% (18/77) · rebond 81% (15/18)
      · −3.0% : fill 19% (15/77) · rebond 70% (10/15)
      · −4.0% : fill 14% (10/77) · rebond 71% (6/10)
      · −5.0% : fill 13% (9/77) · rebond 85% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 69% si les 15 1res min sont vertes (78 cas) · 22% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **29min** → P(séance verte=clôture>ouverture) 72% si début vert vs 16% si rouge (base 46% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 213min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=84) : tient le vert **72%** · continue >prix actuel 44% ; creux résiduel méd -2.66% (q20 -3.77%) → **SL/trailing à −3.77%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.13% / q75 +3.85% → **scale +2.13% / runner +3.85%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **16%** (continue à baisser 59%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.34%** (au-delà de la MAE q10 -5.34%), cible rebond +1.65% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.05% .. +4.41%] · haut q95 +6.19% · bas q05 -4.32%
   - 60min (n=160) : retour [-4.23% .. +5.66%] · haut q95 +6.83% · bas q05 -5.29%
   - 2h (n=160) : retour [-4.78% .. +6.84%] · haut q95 +8.56% · bas q05 -5.81%
   - 4h (n=160) : retour [-5.25% .. +7.37%] · haut q95 +9.01% · bas q05 -6.9%
   - 6h (n=160) : retour [-5.77% .. +6.98%] · haut q95 +10.21% · bas q05 -6.92%
   - session (n=160) : retour [-7.11% .. +7.84%] · haut q95 +10.21% · bas q05 -7.83%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0% / strong 5.0%) · base = 8 séances trend-up (n_eff 5.5)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **13%**. Lecture précoce 30 min : signature présente → 7% vs absente 2% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.96% (p75 1.84% / p90 2.17%) · ~4.0 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **80%** (reprise méd 14.9 min, n=37)
   - −1.0% → **72%** (reprise méd 30.0 min, n=17)
   - −1.5% → **57%** (reprise méd 48.62 min, n=13)
   - −2.0% → **85%** (reprise méd 120.86 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.17%** (p90, défaut prudent ; serré/agressif −1.84%) ; extension open→close méd +7.84% (q75 +8.68% / q95 +9.89%), MFE méd +8.72% / q90 +10.39%
   - Échelle scale-out : +8.72% (33%) / +9.19% (33%) / +10.39% (34%)
- **DÉSARMER** : repli > **−2.17%** depuis le plus-haut = décay → P(retournement) **18%** (préavis méd 100.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.39% : P(retournement après) 0% (mèche méd 1.08%)
- **CONTEXTE** : la dernière heure tient les gains 92% du temps (retour médian dernière heure +1.13%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 59.2  _(momentum haussier)_
- **ADX** : 25.2  _(tendance etablie)_
- **MACD** : hist 0.238  _(pas de croisement recent)_
- **BB** : %B 0.62 · largeur 53.5%
- **ATR** : 2.54 (71.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.01  _(neutre)_
- **Vol ratio** : 0.72  _(volume normal)_
- **Choppiness** : 38.3  _(transition)_
- **MA** : MA20 33.11 · MA50 30.55 · MA200 31.39  _(prix > MA20)_
- **Dist MA** : MA20 +6.2% · MA50 +15.1% · MA200 +12.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (806594 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
