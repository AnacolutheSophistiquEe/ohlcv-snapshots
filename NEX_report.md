# NEX

**Generated** : 2026-08-25T00:08:50.179381+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · €137.20  

> 🟡 **WAIT-FOR-DIP** — spot +4.9 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €137.20 (+4.9% vs entrée) · entrée €130.85 · stop €126.50 · T1 €134.82 · R/R 0.91  
> ↳ P(T1 av. stop) 68 % · EV/risk 0.07 · ¼-Kelly 0.001 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.220 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €130.05–€131.64 (mid €130.85)
- Spot actuel : €137.20 (+4.9% au-dessus de la zone — repli à attendre)
- Stop : €126.50 (stop swing_plan-based (-7.8%))
- Targets : T1 €134.82 · R/R 0.91 | T2 €138.79 · R/R 1.83 | T3 €142.76 · R/R 2.74
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €126.50


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.64 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (7.8 %)** : le gap seul le franchit 0.312 % des séances (4 fois sur 1280).
   - exécution **0.51 pt plus bas** dans le cas TYPIQUE (médiane), 1.423 au p90, **1.796 au pire**
   - perte réelle **8.571 %** en moyenne _(tirée par la queue)_, jusqu'à **9.596 %** — au lieu des 7.8 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0024 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.516 % | p01 -3.643 % | pire -9.596 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0052** [0.0005 ; 0.0256] _(largeur 2.5 pt, n_eff 173.1)_
   - swing : **0.2793** [0.234 ; 0.3283] _(largeur 9.4 pt, n_eff 345.8)_
   - deep : **0.4298** [0.3784 ; 0.4824] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 17.1 observations effectives », dont la borne haute a 95 % vaut environ 17.6 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (43.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-3.51 %** | CVaR **-5.25 %** | vol 2.3 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.51 % vs -7.85 % si l'on extrapolait par √5 _(rapport 0.956 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0169** (β de hausse 1.0895, asymétrie 0.9333) vs FCHI — 616 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 123.9095 sur grid_snapped (2.76 ATR, 9.687 %) — p(stop avant cible) 0.1408 [0.11 ; 0.18], R/R 1.983, perte reelle 9.687 % (gap inclus), CVaR 9.687 %, EV 0.7189 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 2.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.748 %) — p(stop avant cible) 0.4818 [0.43 ; 0.53], R/R 2.495, perte reelle 7.697 % (gap inclus), EV -1.028 % — **REFUSE**
      - refuse : cible atteinte seulement 2.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.50 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.03 %) : P(cible) 2.6 % x 19.21 % + P(rien) 49.2 % x 4.42 % ne couvrent pas P(stop) 48.2 % x 7.70 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 2.76 ATR (stop 10.671 %) — p(stop avant cible) 0.111 [0.08 ; 0.15], R/R 1.8, perte reelle 10.671 % (gap inclus), EV 0.7158 % — **REFUSE**
      - refuse : cible atteinte seulement 2.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ swing_based a 3.29 ATR (stop 12.334 %) — p(stop avant cible) 0.0742 [0.05 ; 0.11], R/R 1.557, perte reelle 12.334 % (gap inclus), EV 0.6853 % — **REFUSE**
      - refuse : cible atteinte seulement 2.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.56 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.33 % > budget 12.00 %
   - 🟢 support a 6.79 ATR (stop 23.414 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.82, perte reelle 23.414 % (gap inclus), EV 0.8027 % — **REFUSE**
      - refuse : cible atteinte seulement 2.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.82 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.82 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.41 % > budget 12.00 %
   - ⚪ atr_grid a 1.0 ATR (stop 3.165 %) — p(stop avant cible) 0.6376 [0.59 ; 0.69], R/R 3.728, perte reelle 5.152 % (gap inclus), EV -1.0219 % — **REFUSE**
      - refuse : cible atteinte seulement 2.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.638, borne haute 0.687 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.02 %) : P(cible) 2.3 % x 19.21 % + P(rien) 34.0 % x 5.38 % ne couvrent pas P(stop) 63.8 % x 5.15 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 6.331 %) — p(stop avant cible) 0.3634 [0.31 ; 0.42], R/R 2.364, perte reelle 8.124 % (gap inclus), EV -0.2474 % — **REFUSE**
      - refuse : cible atteinte seulement 2.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.25 %) : P(cible) 2.6 % x 19.21 % + P(rien) 61.0 % x 3.60 % ne couvrent pas P(stop) 36.3 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 7.913 %) — p(stop avant cible) 0.2334 [0.19 ; 0.28], R/R 2.241, perte reelle 8.571 % (gap inclus), EV 0.5567 % — **REFUSE**
      - refuse : cible atteinte seulement 2.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ grid_snapped a 2.76 ATR (stop 9.687 %) — p(stop avant cible) 0.1408 [0.11 ; 0.18], R/R 1.983, perte reelle 9.687 % (gap inclus), EV 0.7189 % — **REFUSE**
      - refuse : cible atteinte seulement 2.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ atr_grid a 4.5 ATR (stop 14.244 %) — p(stop avant cible) 0.0307 [0.02 ; 0.05], R/R 1.348, perte reelle 14.244 % (gap inclus), EV 0.738 % — **REFUSE**
      - refuse : cible atteinte seulement 2.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.35 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.24 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 15.827 %) — p(stop avant cible) 0.0146 [0.01 ; 0.03], R/R 1.214, perte reelle 15.827 % (gap inclus), EV 0.7564 % — **REFUSE**
      - refuse : cible atteinte seulement 2.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.21 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.83 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 17.409 %) — p(stop avant cible) 0.01 [0.00 ; 0.03], R/R 1.103, perte reelle 17.409 % (gap inclus), EV 0.7636 % — **REFUSE**
      - refuse : cible atteinte seulement 2.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.10 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.41 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 18.992 %) — p(stop avant cible) 0.0051 [0.00 ; 0.02], R/R 1.011, perte reelle 18.992 % (gap inclus), EV 0.7893 % — **REFUSE**
      - refuse : cible atteinte seulement 2.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.01 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.99 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 20.575 %) — p(stop avant cible) 0.0031 [0.00 ; 0.01], R/R 0.934, perte reelle 20.575 % (gap inclus), EV 0.7957 % — **REFUSE**
      - refuse : cible atteinte seulement 2.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.93 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.57 % > budget 12.00 %
   - 🟢 grid_snapped a 6.79 ATR (stop 22.43 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.856, perte reelle 22.43 % (gap inclus), EV 0.8041 % — **REFUSE**
      - refuse : cible atteinte seulement 2.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.86 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.43 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 25.323 %) — p(stop avant cible) 0.0008 [0.00 ; 0.01], R/R 0.758, perte reelle 25.323 % (gap inclus), EV 0.804 % — **REFUSE**
      - refuse : cible atteinte seulement 2.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.76 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.32 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : -0.019 | EV/share : €-0.082 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 47 % | T2 18 % | T3 9 %
- Kelly (position) : f* 0.004 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 11.8 | bear 24.2 | side 64.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 412.0 (= 3 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.109% → cible +1.358% / stop −8.0%, p_fill 36%, n_eff≈17.1) : P(cible|rempli) **42%** · **EV/risk +0.004** (×p_fill ; si rempli +0.08% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=13, n_eff=9))
  - **deep** : indisponible (échantillon insuffisant (n=12, n_eff=8))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→64% · +1.0%→50% · +2.0%→24% · +3.0%→10% · +5.0%→1% · +8.0%→0%
- Range intraday médian 3.0% (p90 4.72%) · excursion haute méd. +1.0% / basse méd. −1.43%
- Profil de vol intra : ouverture 1.747% vs midi 0.528% vs clôture 0.728% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 48% · recovery-V 19%)_
- **Régime intraday** : **chop** _(efficiency 0.108 ; neutre — autocorr -0.028)_ ; drift intra méd. -0.4% ; recovery-V 18%
- **σ réalisé intraday** 2.084% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 71% / whipsaw 29%
- POC intraday (dernière séance, temps-au-prix) : 141.89 (VA 141.33–142.87 ; dernier close 141.35)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 19% · rebond 57% · **stop −1.95%** sous le fill (sous le bruit) · cible +1.55% · R/R 0.79 (high win-rate)
- Gaps overnight (n=159) : méd. 0.2% · baisse 37% (gap-down >1% 7% · >2% 2%)
- Excursion ouverture 5min (n=160) : bas méd −0.43% (p90 −1.93%) · haut méd +0.29% · range méd 1.05%
- Excursion ouverture 15min (n=160) : bas méd −0.57% (p90 −2.08%) · haut méd +0.44% · range méd 1.3%
- Excursion ouverture 30min (n=160) : bas méd −0.59% (p90 −2.31%) · haut méd +0.57% · range méd 1.41%
- Excursion ouverture 60min (n=160) : bas méd −0.81% (p90 −2.58%) · haut méd +0.59% · range méd 1.57%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 141.35 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 73% (114/159) · gap 19% · délai 0.5min · rebond 50% (57/114) (MFE +0.99%)
   - −1.0% : fill 30min 35% · séance 61% (94/159) · gap 7% · délai 12.5min · rebond 46% (44/94) (MFE +0.84%)
   - −1.5% : fill 30min 22% · séance 47% (70/159) · gap 2% · délai 32.5min · rebond 54% (35/70) (MFE +1.03%)
   - −2.0% : fill 30min 13% · séance 31% (51/159) · gap 2% · délai 66.6min · rebond 49% (27/51) (MFE +1.0%)
   - −3.0% : fill 30min 3% · séance 19% (31/159) · gap 1% · délai 115.7min · rebond 57% (18/31) (MFE +1.55%)
   - −4.0% : fill 30min 1% · séance 7% (11/159) · gap 0% · délai 369.3min · rebond 16% (4/11) (MFE +0.77%)
   - −5.0% : fill 30min 0% · séance 2% (4/159) · gap 0% · délai 184.5min · rebond 89% (3/4) (MFE +1.52%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.15% (p90 −1.15%) → stop au-delà de −0.77% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.15% (p90 −0.96%) → stop au-delà de −0.58% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.16% (p90 −0.6%) → stop au-delà de −0.45% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=329 jambes) : jambe baissière méd −1.09% (p90 −2.42%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (46 séances) :
      · −1.0% : fill 76% (37/46) · rebond 40% (15/37)
      · −2.0% : fill 39% (25/46) · rebond 43% (13/25)
      · −3.0% : fill 27% (16/46) · rebond 47% (9/16)
      · −4.0% : fill 13% (7/46) · rebond 28% (3/7)
      · −5.0% : fill 7% (4/46) · rebond 89% (3/4)
   - **flat** (40 séances) :
      · −1.0% : fill 65% (26/40) · rebond 49% (14/26)
      · −2.0% : fill 37% (13/40) · rebond 58% (7/13)
      · −3.0% : fill 23% (8/40) · rebond 46% (3/8)
      · −4.0% : fill 8% (2/40) · rebond 0% (0/2)
      · −5.0% : fill 0% (0/40) · rebond 0% (0/0)
   - **gap-up** (73 séances) :
      · −1.0% : fill 50% (31/73) · rebond 47% (15/31)
      · −2.0% : fill 24% (13/73) · rebond 45% (7/13)
      · −3.0% : fill 13% (7/73) · rebond 82% (6/7)
      · −4.0% : fill 3% (2/73) · rebond 15% (1/2)
      · −5.0% : fill 0% (0/73) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 68% si les 15 1res min sont vertes (86 cas) · 20% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **45min** → P(séance verte=clôture>ouverture) 75% si début vert vs 22% si rouge (base 46% · écart 53 pts) ; prédictivité sature ensuite (plafond brut 249min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **75%** · continue >prix actuel 48% ; creux résiduel méd -0.83% (q20 -2.03%) → **SL/trailing à −2.03%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.06% / q75 +1.63% → **scale +1.06% / runner +1.63%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **22%** (continue à baisser 55%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.04%** (au-delà de la MAE q10 -3.04%), cible rebond +1.04% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.01% .. +2.31%] · haut q95 +2.62% · bas q05 -2.59%
   - 60min (n=160) : retour [-2.82% .. +2.66%] · haut q95 +2.83% · bas q05 -3.24%
   - 2h (n=160) : retour [-3.55% .. +2.56%] · haut q95 +2.94% · bas q05 -3.74%
   - 4h (n=160) : retour [-3.12% .. +2.74%] · haut q95 +3.04% · bas q05 -3.88%
   - 6h (n=160) : retour [-3.81% .. +3.51%] · haut q95 +3.91% · bas q05 -4.17%
   - session (n=160) : retour [-3.51% .. +2.88%] · haut q95 +4.18% · bas q05 -4.67%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.94%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 56.3  _(momentum haussier)_
- **ADX** : 15.4  _(pas de tendance nette)_
- **MACD** : hist 0.301  _(pas de croisement recent)_
- **BB** : %B 0.52 · largeur 15.5%
- **ATR** : 4.34 (57.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.22  _(distribution)_
- **Vol ratio** : 0.3  _(volume atone)_
- **Choppiness** : 69.9  _(marche en range (choppy))_
- **MA** : MA20 136.74 · MA50 139.04 · MA200 133.18  _(prix > MA20)_
- **Dist MA** : MA20 +0.3% · MA50 -1.3% · MA200 +3.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (807864 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
