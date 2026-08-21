# PRY

**Generated** : 2026-08-21T00:13:22.058628+00:00  
**Santé technique** : 4/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €122.20  

> 🟡 **WAIT-FOR-DIP** — spot +6.3 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €122.20 (+6.3% vs entrée) · entrée €114.94 · stop €109.56 · T1 €118.56 · R/R 0.67  
> ↳ P(T1 av. stop) 81 % · EV/risk 0.301 · ¼-Kelly 0.002 · _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €114.21–€115.66 (mid €114.94)
- Spot actuel : €122.20 (+6.3% au-dessus de la zone — repli à attendre)
- Stop : €109.56 (stop swing_plan-based (-10.34%))
- Targets : T1 €118.56 · R/R 0.67 | T2 €122.18 · R/R 1.35 | T3 €125.81 · R/R 2.02
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €109.56


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.50 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (10.34 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1269).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 10.34 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.847 % | p01 -3.349 % | pire -9.998 % _(sur 1269 séances)_
- **P(stop avant cible)** _(source : daily, 1270 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.064** [0.0346 ; 0.1078] _(largeur 7.3 pt, n_eff 173.1)_
   - swing : **0.3299** [0.2819 ; 0.3807] _(largeur 9.9 pt, n_eff 345.8)_
   - deep : **0.4317** [0.3802 ; 0.4843] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (41.9 pt), swing (50.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-4.24 %** | CVaR **-5.72 %** | vol 2.62 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 1.81 % contre 2.98 % aujourd'hui, rapport 0.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.46 % vs -7.47 % si l'on extrapolait par √5 _(rapport 0.865 ; < 1 = le √5 surestime)_
- **β de baisse : 1.038** (β de hausse 1.2303, asymétrie 0.8437) vs FTSEMIB — 562 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.42× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : cela veut dire que la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier n'est alors PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable.**
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 6.598 %) — p(stop avant cible) 0.2717 [0.23 ; 0.32], R/R 0.344, perte reelle 8.587 % (gap inclus), EV -0.4674 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.47 %) : P(cible) 65.6 % x 2.95 % + P(rien) 7.2 % x -0.96 % ne couvrent pas P(stop) 27.2 % x 8.59 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.41 ATR (stop 11.937 %) — p(stop avant cible) 0.0861 [0.06 ; 0.12], R/R 0.247, perte reelle 11.937 % (gap inclus), EV 0.3047 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - 🟢 support a 3.39 ATR (stop 16.234 %) — p(stop avant cible) 0.0199 [0.01 ; 0.04], R/R 0.182, perte reelle 16.234 % (gap inclus), EV 0.4984 % — **REFUSE**
      - refuse : R/R 0.18 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.23 % > budget 12.0 %
   - 🟢 support a 9.23 ATR (stop 41.926 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.07, perte reelle 41.926 % (gap inclus), EV 0.4936 % — **REFUSE**
      - refuse : R/R 0.07 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.93 % > budget 12.0 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : -0.016 | EV/share : €-0.087 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 24 % | T3 8 %
- Kelly (position) : f* 0.009 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 19.7 | bear 51.0 | side 29.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 122.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.7% → cible +3.617% / stop −1.809%, p_fill 39%, n_eff≈18.8) : P(cible|rempli) **0%** · **EV/risk -0.227** (×p_fill ; si rempli -1.05% du capital)
  - **swing** (entrée dip −5.941% → cible +3.152% / stop −4.676%, p_fill 25%, n_eff≈10.4) : P(cible|rempli) **70%** · **EV/risk +0.058** (×p_fill ; si rempli +1.09% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=12, n_eff=8))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→69% · +2.0%→42% · +3.0%→30% · +5.0%→10% · +8.0%→4%
- Range intraday médian 4.4% (p90 6.51%) · excursion haute méd. +1.51% / basse méd. −1.61%
- Profil de vol intra : ouverture 2.538% vs midi 0.816% vs clôture 1.202% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (158 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 54% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; neutre — autocorr -0.014)_ ; drift intra méd. -0.71% ; recovery-V 24%
- **σ réalisé intraday** 2.714% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 60% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 124.3012 (VA 123.4237–124.3988 ; dernier close 124.02)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 19% · rebond 74% · **stop −2.38%** sous le fill (sous le bruit) · cible +1.45% · R/R 0.61 (high win-rate)
- Gaps overnight (n=157) : méd. 0.29% · baisse 40% (gap-down >1% 17% · >2% 9%)
- Excursion ouverture 5min (n=158) : bas méd −0.89% (p90 −2.1%) · haut méd +0.26% · range méd 1.42%
- Excursion ouverture 15min (n=158) : bas méd −1.03% (p90 −2.57%) · haut méd +0.53% · range méd 1.77%
- Excursion ouverture 30min (n=158) : bas méd −1.05% (p90 −2.95%) · haut méd +0.66% · range méd 1.99%
- Excursion ouverture 60min (n=158) : bas méd −1.21% (p90 −3.17%) · haut méd +0.86% · range méd 2.23%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 124.02 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 70% (113/157) · gap 24% · délai 0.2min · rebond 61% (71/113) (MFE +1.29%)
   - −1.0% : fill 30min 49% · séance 62% (96/157) · gap 17% · délai 0.4min · rebond 59% (58/96) (MFE +1.57%)
   - −1.5% : fill 30min 34% · séance 53% (83/157) · gap 13% · délai 3.3min · rebond 54% (46/83) (MFE +1.09%)
   - −2.0% : fill 30min 24% · séance 43% (67/157) · gap 9% · délai 5.4min · rebond 60% (42/67) (MFE +1.34%)
   - −3.0% : fill 30min 12% · séance 32% (48/157) · gap 3% · délai 70.2min · rebond 62% (32/48) (MFE +1.6%)
   - −4.0% : fill 30min 3% · séance 19% (26/157) · gap 1% · délai 185.0min · rebond 74% (19/26) (MFE +1.45%)
   - −5.0% : fill 30min 1% · séance 13% (18/157) · gap 1% · délai 394.2min · rebond 65% (13/18) (MFE +1.39%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −1.78%) → stop au-delà de −1.53% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.41% (p90 −2.02%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.02% (p90 −1.85%) → stop au-delà de −1.09% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=492 jambes) : jambe baissière méd −1.07% (p90 −2.51%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 91% (49/54) · rebond 47% (27/49)
      · −2.0% : fill 71% (39/54) · rebond 59% (26/39)
      · −3.0% : fill 59% (30/54) · rebond 64% (22/30)
      · −4.0% : fill 40% (17/54) · rebond 70% (12/17)
      · −5.0% : fill 31% (13/54) · rebond 60% (9/13)
   - **flat** (30 séances) :
      · −1.0% : fill 68% (17/30) · rebond 66% (11/17)
      · −2.0% : fill 41% (9/30) · rebond 89% (7/9)
      · −3.0% : fill 16% (5/30) · rebond 40% (2/5)
      · −4.0% : fill 7% (3/30) · rebond 59% (2/3)
      · −5.0% : fill 4% (2/30) · rebond 25% (1/2)
   - **gap-up** (73 séances) :
      · −1.0% : fill 40% (30/73) · rebond 74% (20/30)
      · −2.0% : fill 26% (19/73) · rebond 43% (9/19)
      · −3.0% : fill 21% (13/73) · rebond 63% (8/13)
      · −4.0% : fill 11% (6/73) · rebond 86% (5/6)
      · −5.0% : fill 5% (3/73) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=158) : 47% en base · 67% si les 15 1res min sont vertes (73 cas) · 31% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=158) : COUDE à **1:09** → P(séance verte=clôture>ouverture) 80% si début vert vs 23% si rouge (base 47% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **80%** · continue >prix actuel 60% ; creux résiduel méd -1.19% (q20 -1.97%) → **SL/trailing à −1.97%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.5% / q75 +2.65% → **scale +1.5% / runner +2.65%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **23%** (continue à baisser 65%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.11%** (au-delà de la MAE q10 -4.11%), cible rebond +1.37% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=158) : retour [-2.85% .. +2.95%] · haut q95 +3.44% · bas q05 -3.39%
   - 60min (n=158) : retour [-3.39% .. +2.56%] · haut q95 +3.9% · bas q05 -3.56%
   - 2h (n=158) : retour [-3.59% .. +2.65%] · haut q95 +4.01% · bas q05 -4.49%
   - 4h (n=158) : retour [-3.55% .. +3.29%] · haut q95 +4.11% · bas q05 -4.62%
   - 6h (n=158) : retour [-3.71% .. +3.78%] · haut q95 +4.57% · bas q05 -4.93%
   - session (n=158) : retour [-4.33% .. +4.05%] · haut q95 +5.42% · bas q05 -6.25%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.41%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 53.8  _(neutre)_
- **ADX** : 25.3  _(tendance etablie)_
- **MACD** : hist 0.494  _(pas de croisement recent)_
- **BB** : %B 0.38 · largeur 14.4%
- **ATR** : 5.37 (70.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.147  _(distribution)_
- **Vol ratio** : 0.36  _(volume atone)_
- **Choppiness** : 49.6  _(transition)_
- **MA** : MA20 124.35 · MA50 134.09 · MA200 112.86  _(prix < MA20)_
- **Dist MA** : MA20 -1.7% · MA50 -8.9% · MA200 +8.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (593350 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
