# NEX

**Generated** : 2026-08-24T00:08:54.489931+00:00  
**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €141.80  

> 🟡 **WAIT-FOR-DIP** — spot +2.9 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €141.80 (+2.9% vs entrée) · entrée €137.76 · stop €126.74 · T1 €139.55 · R/R 0.16  
> ↳ P(T1 av. stop) 50 % _(réel 5 s)_ · EV/risk 0.01 _(réel 5 s)_ (GBM -0.059) · ¼-Kelly 0.066 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.210 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €137.40–€138.12 (mid €137.76)
- Spot actuel : €141.80 (+2.9% au-dessus de la zone — repli à attendre)
- Stop : €126.74 (stop swing_plan-based (-9.31%))
- Targets : T1 €139.55 · R/R 0.16 | T2 €141.34 · R/R 0.32 | T3 €143.13 · R/R 0.49
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €126.74


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.64 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (9.31 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1280).
   - exécution **0.286 pt plus bas** dans le cas TYPIQUE (médiane), 0.286 au p90, **0.286 au pire**
   - perte réelle **9.596 %** en moyenne _(tirée par la queue)_, jusqu'à **9.596 %** — au lieu des 9.31 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0002 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.516 % | p01 -3.643 % | pire -9.596 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0052** [0.0005 ; 0.0256] _(largeur 2.5 pt, n_eff 173.1)_
   - swing : **0.2809** [0.2355 ; 0.33] _(largeur 9.4 pt, n_eff 345.8)_
   - deep : **0.4323** [0.3808 ; 0.4849] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 13.9 observations effectives », dont la borne haute a 95 % vaut environ 21.5 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (48.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-3.51 %** | CVaR **-5.25 %** | vol 2.3 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.51 % vs -7.85 % si l'on extrapolait par √5 _(rapport 0.956 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0172** (β de hausse 1.0895, asymétrie 0.9336) vs FCHI — 617 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 126.7 sur atr_grid (3.5 ATR, 10.649 %) — p(stop avant cible) 0.1116 [0.08 ; 0.15], R/R 1.441, perte reelle 10.649 % (gap inclus), CVaR 10.649 %, EV 0.617 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.44 < plancher 1.60 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.564 %) — p(stop avant cible) 0.5056 [0.45 ; 0.56], R/R 1.994, perte reelle 7.697 % (gap inclus), EV -1.3112 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.506, borne haute 0.558 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.31 %) : P(cible) 5.7 % x 15.35 % + P(rien) 43.8 % x 3.91 % ne couvrent pas P(stop) 50.6 % x 7.70 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 3.84 ATR (stop 13.677 %) — p(stop avant cible) 0.0447 [0.03 ; 0.07], R/R 1.122, perte reelle 13.677 % (gap inclus), EV 0.6009 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.12 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.68 % > budget 12.00 %
   - ⚪ swing_based a 4.37 ATR (stop 15.283 %) — p(stop avant cible) 0.021 [0.01 ; 0.04], R/R 1.004, perte reelle 15.283 % (gap inclus), EV 0.6525 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.00 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.28 % > budget 12.00 %
   - 🟢 support a 7.9 ATR (stop 26.008 %) — p(stop avant cible) 0.0008 [0.00 ; 0.01], R/R 0.59, perte reelle 26.008 % (gap inclus), EV 0.7024 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.59 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.01 % > budget 12.00 %
   - ⚪ atr_grid a 1.0 ATR (stop 3.043 %) — p(stop avant cible) 0.6469 [0.60 ; 0.70], R/R 3.035, perte reelle 5.057 % (gap inclus), EV -1.118 % — **REFUSE**
      - refuse : cible atteinte seulement 4.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.647, borne haute 0.696 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.12 %) : P(cible) 4.5 % x 15.35 % + P(rien) 30.8 % x 4.74 % ne couvrent pas P(stop) 64.7 % x 5.06 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 5.324 %) — p(stop avant cible) 0.4415 [0.39 ; 0.49], R/R 1.889, perte reelle 8.124 % (gap inclus), EV -0.9388 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.94 %) : P(cible) 5.7 % x 15.35 % + P(rien) 50.2 % x 3.55 % ne couvrent pas P(stop) 44.1 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 6.846 %) — p(stop avant cible) 0.327 [0.28 ; 0.38], R/R 1.889, perte reelle 8.124 % (gap inclus), EV -0.0666 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.07 %) : P(cible) 5.7 % x 15.35 % + P(rien) 61.7 % x 2.79 % ne couvrent pas P(stop) 32.7 % x 8.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 8.367 %) — p(stop avant cible) 0.217 [0.18 ; 0.26], R/R 1.599, perte reelle 9.596 % (gap inclus), EV 0.2817 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.60 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 10.649 %) — p(stop avant cible) 0.1116 [0.08 ; 0.15], R/R 1.441, perte reelle 10.649 % (gap inclus), EV 0.617 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.44 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.44 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ grid_snapped a 3.84 ATR (stop 12.609 %) — p(stop avant cible) 0.0701 [0.05 ; 0.10], R/R 1.217, perte reelle 12.609 % (gap inclus), EV 0.5847 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.22 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.61 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 16.734 %) — p(stop avant cible) 0.0146 [0.01 ; 0.03], R/R 0.917, perte reelle 16.734 % (gap inclus), EV 0.6426 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.92 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.73 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 18.255 %) — p(stop avant cible) 0.0059 [0.00 ; 0.02], R/R 0.841, perte reelle 18.255 % (gap inclus), EV 0.6789 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.25 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 19.776 %) — p(stop avant cible) 0.0031 [0.00 ; 0.01], R/R 0.776, perte reelle 19.776 % (gap inclus), EV 0.6978 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.78 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.78 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 21.298 %) — p(stop avant cible) 0.0023 [0.00 ; 0.01], R/R 0.721, perte reelle 21.298 % (gap inclus), EV 0.7005 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.72 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.30 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 22.819 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.673, perte reelle 22.819 % (gap inclus), EV 0.7025 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.67 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.82 % > budget 12.00 %
   - 🟢 grid_snapped a 7.9 ATR (stop 24.94 %) — p(stop avant cible) 0.0008 [0.00 ; 0.01], R/R 0.615, perte reelle 24.94 % (gap inclus), EV 0.7032 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.62 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.94 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : -0.059 | EV/share : €-0.653 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 42 % | T2 16 % | T3 4 %
- Kelly (position) : f* 0.265 | ¼-Kelly 0.066 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 44.4 | bear 40.4 | side 15.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 425.0 (= 3 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.848% → cible +1.299% / stop −8.0%, p_fill 21%, n_eff≈13.9) : P(cible|rempli) **50%** · **EV/risk +0.010** (×p_fill ; si rempli +0.39% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=6, n_eff=5))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
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
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 69.1  _(momentum haussier)_
- **ADX** : 16.5  _(pas de tendance nette)_
- **MACD** : hist 0.584  _(pas de croisement recent)_
- **BB** : %B 0.75 · largeur 16.1%
- **ATR** : 4.31 (55.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.21  _(distribution)_
- **Vol ratio** : 0.75  _(volume normal)_
- **Choppiness** : 51.3  _(transition)_
- **MA** : MA20 136.4 · MA50 139.26 · MA200 133.08  _(prix > MA20)_
- **Dist MA** : MA20 +4.0% · MA50 +1.8% · MA200 +6.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (822399 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
