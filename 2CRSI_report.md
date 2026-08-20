# AL2SI

**Generated** : 2026-08-20T19:55:42.865303+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €25.78  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €25.78 (+6.3% vs entrée) · entrée €24.25 · stop €22.69 · T1 €25.64 · R/R 0.89  
> ↳ P(T1 av. stop) 54 % _(réel 5 s)_ · EV/risk -0.039 _(réel 5 s)_ (GBM 0.137) · ¼-Kelly 0.02 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €23.97–€24.52 (mid €24.25)
- Spot actuel : €25.78 (+6.3% au-dessus de la zone — repli à attendre)
- Stop : €22.69 (stop swing_plan-based (-12.0%))
- Targets : T1 €25.64 · R/R 0.89 | T2 €27.04 · R/R 1.79 | T3 €28.43 · R/R 2.68
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €22.69


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.36 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.0 %)** : le gap seul le franchit 0.391 % des séances ; quand il le franchit, l'exécution est **12.668 points plus bas** → perte réelle **24.668 %** _(et non 12.0 %)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.346 % | p01 -6.815 % | pire -38.117 % _(sur 1279 séances)_
- **P(stop avant cible)** _(source : daily, 1280 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2858** [0.2225 ; 0.3562] _(largeur 13.4 pt, n_eff 173.1)_
   - swing : **0.4946** [0.4421 ; 0.5472] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.5232** [0.4705 ; 0.5755] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 23.2 observations effectives », dont la borne haute a 95 % vaut environ 12.9 %.
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 24.0 observations effectives », dont la borne haute a 95 % vaut environ 12.5 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (34.4 pt), swing (38.5 pt), deep (38.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-7.36 %** | CVaR **-11.89 %** | vol 6.31 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 3.87 % contre 7.52 % aujourd'hui, rapport 0.51)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.77 % vs -13.92 % si l'on extrapolait par √5 _(rapport 1.061 ; < 1 = le √5 surestime)_
- **β de baisse : 1.198** (β de hausse 0.9252, asymétrie 1.2948) vs FCHI — 617 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.985× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Edge, scénarios & sizing

- EV/risk : 0.137 | EV/share : €0.214 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 56 % | T2 35 % | T3 24 %
- Kelly (position) : f* 0.08 | ¼-Kelly 0.02 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 85.7 | bear 8.7 | side 5.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 155.0 (= 6 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.704% → cible +2.575% / stop −2.0%, p_fill 65%, n_eff≈30.0) : P(cible|rempli) **22%** · **EV/risk -0.112** (×p_fill ; si rempli -0.34% du capital)
  - **swing** (entrée dip −5.951% → cible +5.757% / stop −6.431%, p_fill 43%, n_eff≈23.2) : P(cible|rempli) **54%** · **EV/risk -0.039** (×p_fill ; si rempli -0.58% du capital)
  - **deep** (entrée dip −9.197% → cible +8.142% / stop −9.992%, p_fill 52%, n_eff≈24.0) : P(cible|rempli) **52%** · **EV/risk -0.093** (×p_fill ; si rempli -1.78% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→78% · +2.0%→70% · +3.0%→57% · +5.0%→42% · +8.0%→20%
- Range intraday médian 8.18% (p90 22.19%) · excursion haute méd. +4.23% / basse méd. −4.05%
- Profil de vol intra : ouverture 5.578% vs midi 1.73% vs clôture 1.912% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 9% · trend ↑0%/↓1% ; spike-down 74% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; mean-reverting — autocorr -0.063)_ ; drift intra méd. -0.302% ; recovery-V 31%
- **σ réalisé intraday** 6.081% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 68% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 26.1945 (VA 25.9635–26.6235 ; dernier close 26.16)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 38% · rebond 86% · **stop −5.29%** sous le fill (sous le bruit) · cible +2.4% · R/R 0.45 (high win-rate)
- Gaps overnight (n=159) : méd. 0.0% · baisse 46% (gap-down >1% 20% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −1.18% (p90 −4.58%) · haut méd +0.95% · range méd 2.9%
- Excursion ouverture 15min (n=160) : bas méd −1.49% (p90 −5.58%) · haut méd +1.57% · range méd 3.54%
- Excursion ouverture 30min (n=160) : bas méd −1.61% (p90 −5.67%) · haut méd +2.06% · range méd 4.6%
- Excursion ouverture 60min (n=160) : bas méd −1.92% (p90 −6.63%) · haut méd +2.42% · range méd 5.47%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 26.16 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 83% (125/159) · gap 32% · délai 0.3min · rebond 69% (87/125) (MFE +2.68%)
   - −1.0% : fill 30min 62% · séance 82% (121/159) · gap 20% · délai 0.7min · rebond 70% (85/121) (MFE +2.73%)
   - −1.5% : fill 30min 50% · séance 79% (112/159) · gap 14% · délai 1.2min · rebond 70% (76/112) (MFE +2.04%)
   - −2.0% : fill 30min 42% · séance 68% (97/159) · gap 8% · délai 5.3min · rebond 60% (61/97) (MFE +1.64%)
   - −3.0% : fill 30min 30% · séance 56% (81/159) · gap 5% · délai 23.8min · rebond 76% (66/81) (MFE +1.99%)
   - −4.0% : fill 30min 23% · séance 49% (70/159) · gap 3% · délai 40.4min · rebond 71% (53/70) (MFE +2.33%)
   - −5.0% : fill 30min 16% · séance 38% (59/159) · gap 3% · délai 43.0min · rebond 86% (54/59) (MFE +2.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −1.02% (p90 −4.81%) → stop au-delà de −2.22% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.15% (p90 −5.0%) → stop au-delà de −3.18% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.1% (p90 −5.27%) → stop au-delà de −3.41% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1565 jambes) : jambe baissière méd −1.28% (p90 −3.29%) · ~19.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 99% (53/56) · rebond 73% (37/53)
      · −2.0% : fill 84% (45/56) · rebond 57% (27/45)
      · −3.0% : fill 70% (41/56) · rebond 79% (34/41)
      · −4.0% : fill 63% (36/56) · rebond 75% (29/36)
      · −5.0% : fill 44% (30/56) · rebond 84% (27/30)
   - **flat** (36 séances) :
      · −1.0% : fill 83% (29/36) · rebond 71% (22/29)
      · −2.0% : fill 66% (22/36) · rebond 73% (16/22)
      · −3.0% : fill 54% (16/36) · rebond 70% (13/16)
      · −4.0% : fill 48% (15/36) · rebond 70% (12/15)
      · −5.0% : fill 36% (12/36) · rebond 100% (12/12)
   - **gap-up** (67 séances) :
      · −1.0% : fill 67% (39/67) · rebond 64% (26/39)
      · −2.0% : fill 54% (30/67) · rebond 55% (18/30)
      · −3.0% : fill 44% (24/67) · rebond 76% (19/24)
      · −4.0% : fill 37% (19/67) · rebond 64% (12/19)
      · −5.0% : fill 33% (17/67) · rebond 79% (15/17)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 56% si les 15 1res min sont vertes (76 cas) · 34% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **44min** → P(séance verte=clôture>ouverture) 72% si début vert vs 18% si rouge (base 44% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 252min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **72%** · continue >prix actuel 52% ; creux résiduel méd -2.65% (q20 -5.02%) → **SL/trailing à −5.02%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.01% / q75 +5.0% → **scale +3.01% / runner +5.0%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **18%** (continue à baisser 51%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −9.02%** (au-delà de la MAE q10 -9.02%), cible rebond +2.61% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.25% .. +6.5%] · haut q95 +7.91% · bas q05 -7.44%
   - 60min (n=160) : retour [-5.85% .. +6.75%] · haut q95 +9.23% · bas q05 -7.7%
   - 2h (n=160) : retour [-6.02% .. +9.66%] · haut q95 +10.04% · bas q05 -8.01%
   - 4h (n=160) : retour [-7.27% .. +9.45%] · haut q95 +11.9% · bas q05 -10.25%
   - 6h (n=160) : retour [-6.71% .. +9.91%] · haut q95 +13.87% · bas q05 -10.82%
   - session (n=160) : retour [-7.97% .. +12.66%] · haut q95 +13.87% · bas q05 -11.25%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.44%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 46.3  _(neutre)_
- **ADX** : 13.0  _(pas de tendance nette)_
- **MACD** : hist 0.209  _(pas de croisement recent)_
- **BB** : %B 0.31 · largeur 18.9%
- **ATR** : 1.56 (49.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.219  _(distribution)_
- **Vol ratio** : 0.19  _(volume atone)_
- **Choppiness** : 51.6  _(transition)_
- **MA** : MA20 26.76 · MA50 30.28 · MA200 25.64  _(prix < MA20)_
- **Dist MA** : MA20 -3.7% · MA50 -14.9% · MA200 +0.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (412214 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
