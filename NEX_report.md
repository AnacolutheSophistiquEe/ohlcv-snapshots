# NEX

**Generated** : 2026-08-21T21:43:36.061634+00:00  
**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €141.80  

> 🟡 **WAIT-FOR-DIP** — spot +2.9 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €141.80 (+2.9% vs entrée) · entrée €137.76 · stop €126.74 · T1 €139.55 · R/R 0.16  
> ↳ P(T1 av. stop) 50 % _(réel 5 s)_ · EV/risk 0.011 _(réel 5 s)_ (GBM -0.059) · ¼-Kelly 0.067 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
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
- **Couple retenu** : stop 135.3286 sur atr_based (1.5 ATR, 4.564 %) — p(stop avant cible) 0.5056 [0.45 ; 0.56], R/R 1.994, perte reelle 7.697 % (gap inclus), CVaR 4.581 %, EV -1.3112 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.638 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.506, borne haute 0.558 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.564 %) — p(stop avant cible) 0.5056 [0.45 ; 0.56], R/R 1.994, perte reelle 7.697 % (gap inclus), EV -1.3112 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.506, borne haute 0.558 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.31 %) : P(cible) 5.7 % x 15.35 % + P(rien) 43.8 % x 3.91 % ne couvrent pas P(stop) 50.6 % x 7.70 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 3.84 ATR (stop 13.85 %) — p(stop avant cible) 0.0398 [0.02 ; 0.06], R/R 1.108, perte reelle 13.85 % (gap inclus), EV 0.6053 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.11 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.85 % > budget 12.00 %
   - ⚪ swing_based a 4.37 ATR (stop 15.457 %) — p(stop avant cible) 0.0206 [0.01 ; 0.04], R/R 0.993, perte reelle 15.457 % (gap inclus), EV 0.6487 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.99 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.46 % > budget 12.00 %
   - 🟢 support a 7.9 ATR (stop 26.182 %) — p(stop avant cible) 0.0008 [0.00 ; 0.01], R/R 0.586, perte reelle 26.182 % (gap inclus), EV 0.7022 % — **REFUSE**
      - refuse : cible atteinte seulement 5.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.59 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.18 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : -0.059 | EV/share : €-0.648 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 42 % | T2 16 % | T3 5 %
- Kelly (position) : f* 0.267 | ¼-Kelly 0.067 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 44.4 | bear 40.4 | side 15.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 425.0 (= 3 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.848% → cible +1.299% / stop −8.0%, p_fill 22%, n_eff≈13.9) : P(cible|rempli) **50%** · **EV/risk +0.011** (×p_fill ; si rempli +0.39% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=6, n_eff=5))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→64% · +1.0%→50% · +2.0%→24% · +3.0%→10% · +5.0%→2% · +8.0%→0%
- Range intraday médian 3.0% (p90 4.79%) · excursion haute méd. +1.0% / basse méd. −1.43%
- Profil de vol intra : ouverture 1.754% vs midi 0.529% vs clôture 0.729% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (159 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 49% · recovery-V 19%)_
- **Régime intraday** : **chop** _(efficiency 0.105 ; mean-reverting — autocorr -0.041)_ ; drift intra méd. -0.513% ; recovery-V 18%
- **σ réalisé intraday** 2.104% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 75% / whipsaw 31%
- POC intraday (dernière séance, temps-au-prix) : 137.6125 (VA 136.4125–137.8375 ; dernier close 138.9)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 20% · rebond 57% · **stop −1.95%** sous le fill (sous le bruit) · cible +1.55% · R/R 0.79 (high win-rate)
- Gaps overnight (n=158) : méd. 0.25% · baisse 36% (gap-down >1% 7% · >2% 2%)
- Excursion ouverture 5min (n=159) : bas méd −0.44% (p90 −1.94%) · haut méd +0.3% · range méd 1.05%
- Excursion ouverture 15min (n=159) : bas méd −0.59% (p90 −2.11%) · haut méd +0.42% · range méd 1.29%
- Excursion ouverture 30min (n=159) : bas méd −0.6% (p90 −2.31%) · haut méd +0.55% · range méd 1.41%
- Excursion ouverture 60min (n=159) : bas méd −0.84% (p90 −2.58%) · haut méd +0.58% · range méd 1.56%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 138.9 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 72% (113/158) · gap 20% · délai 0.5min · rebond 49% (56/113) (MFE +0.91%)
   - −1.0% : fill 30min 36% · séance 62% (94/158) · gap 7% · délai 12.5min · rebond 46% (44/94) (MFE +0.84%)
   - −1.5% : fill 30min 22% · séance 48% (70/158) · gap 2% · délai 32.5min · rebond 54% (35/70) (MFE +1.03%)
   - −2.0% : fill 30min 13% · séance 32% (51/158) · gap 2% · délai 66.6min · rebond 49% (27/51) (MFE +1.0%)
   - −3.0% : fill 30min 4% · séance 20% (31/158) · gap 1% · délai 115.7min · rebond 57% (18/31) (MFE +1.55%)
   - −4.0% : fill 30min 1% · séance 7% (11/158) · gap 0% · délai 369.3min · rebond 16% (4/11) (MFE +0.77%)
   - −5.0% : fill 30min 0% · séance 2% (4/158) · gap 0% · délai 184.5min · rebond 89% (3/4) (MFE +1.52%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.15% (p90 −1.24%) → stop au-delà de −0.79% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.14% (p90 −1.44%) → stop au-delà de −0.6% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.13% (p90 −0.6%) → stop au-delà de −0.49% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=329 jambes) : jambe baissière méd −1.09% (p90 −2.42%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (46 séances) :
      · −1.0% : fill 76% (37/46) · rebond 40% (15/37)
      · −2.0% : fill 39% (25/46) · rebond 43% (13/25)
      · −3.0% : fill 27% (16/46) · rebond 47% (9/16)
      · −4.0% : fill 13% (7/46) · rebond 28% (3/7)
      · −5.0% : fill 7% (4/46) · rebond 89% (3/4)
   - **flat** (39 séances) :
      · −1.0% : fill 70% (26/39) · rebond 49% (14/26)
      · −2.0% : fill 39% (13/39) · rebond 58% (7/13)
      · −3.0% : fill 24% (8/39) · rebond 46% (3/8)
      · −4.0% : fill 8% (2/39) · rebond 0% (0/2)
      · −5.0% : fill 0% (0/39) · rebond 0% (0/0)
   - **gap-up** (73 séances) :
      · −1.0% : fill 50% (31/73) · rebond 47% (15/31)
      · −2.0% : fill 24% (13/73) · rebond 45% (7/13)
      · −3.0% : fill 13% (7/73) · rebond 82% (6/7)
      · −4.0% : fill 3% (2/73) · rebond 15% (1/2)
      · −5.0% : fill 0% (0/73) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=159) : 45% en base · 66% si les 15 1res min sont vertes (85 cas) · 20% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=159) : COUDE à **45min** → P(séance verte=clôture>ouverture) 74% si début vert vs 22% si rouge (base 45% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 249min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **74%** · continue >prix actuel 50% ; creux résiduel méd -0.89% (q20 -2.05%) → **SL/trailing à −2.05%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.05% / q75 +1.64% → **scale +1.05% / runner +1.64%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **22%** (continue à baisser 55%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.04%** (au-delà de la MAE q10 -3.04%), cible rebond +1.04% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=159) : retour [-2.01% .. +2.32%] · haut q95 +2.63% · bas q05 -2.59%
   - 60min (n=159) : retour [-2.82% .. +2.52%] · haut q95 +2.86% · bas q05 -3.24%
   - 2h (n=159) : retour [-3.56% .. +2.36%] · haut q95 +2.94% · bas q05 -3.74%
   - 4h (n=159) : retour [-3.16% .. +2.53%] · haut q95 +3.09% · bas q05 -3.89%
   - 6h (n=159) : retour [-3.81% .. +3.49%] · haut q95 +3.95% · bas q05 -4.17%
   - session (n=159) : retour [-3.52% .. +2.9%] · haut q95 +4.18% · bas q05 -4.68%


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

_Bulletin compact généré depuis `<TICKER>_report_data.json` (664119 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
