# 267260

**Generated** : 2026-10-08T00:17:32.311349+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 2/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · ₩628000.00  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (2 séance(s) de retard, drapeau lu sur first_passage_by_horizon); usable=false (intervalle le plus large 26.9 pt > 25)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot ₩628000.00 (+3.8% vs entrée) · entrée ₩605271.14 · stop ₩556849.45 · T1 ₩619521.14 · R/R 0.29  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩603131.05–₩607411.23 (mid ₩605271.14)
- Spot actuel : ₩628000.00 (+3.8% au-dessus de la zone — repli à attendre)
- Stop : ₩556849.45 (plancher anti-bruit 5 s — stop EV-optimal −8% (first-passage 5 s réel) ; -8.00 % depuis l'entree)
- Targets : T1 ₩619521.14 · R/R 0.29 | T2 ₩633771.14 · R/R 0.59 | T3 ₩648021.14 · R/R 0.88
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩556849.45


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.11 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.5 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1218).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 12.5 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.671 % | p01 -4.805 % | pire -11.715 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0619** [0.033 ; 0.1052] _(largeur 7.2 pt, n_eff 173.1)_
   - swing : **0.4871** [0.4347 ; 0.5397] _(largeur 10.5 pt, n_eff 345.6)_
   - deep : **0.4552** [0.4033 ; 0.5079] _(largeur 10.5 pt, n_eff 345.6)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 28.6 observations effectives », dont la borne haute a 95 % vaut environ 10.5 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (26.9 pt), swing (31.6 pt), deep (33.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.75 %** | CVaR **-8.95 %** | vol 4.46 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 2.75 % contre 4.88 % aujourd'hui, rapport 0.57)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.82 % vs -12.03 % si l'on extrapolait par √5 _(rapport 0.899 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0383** (β de hausse 0.8432, asymétrie 1.2313) vs KS11 — 552 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.101 | EV/share : ₩-4887.364 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 13 % | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.6 | bear 7.3 | side 85.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.62% → cible +2.354% / stop −8.0%, p_fill 40%, n_eff≈49.2) : P(cible|rempli) **40%** · **EV/risk -0.003** (×p_fill ; si rempli -0.05% du capital)
  - **swing** (entrée dip −7.962% → cible +5.513% / stop −4.931%, p_fill 23%, n_eff≈28.6) : P(cible|rempli) **28%** · **EV/risk -0.100** (×p_fill ; si rempli -2.15% du capital)
  - **deep** (entrée dip −12.302% → cible +8.182% / stop −7.763%, p_fill 26%, n_eff≈29.5) : P(cible|rempli) **33%** · **EV/risk -0.073** (×p_fill ; si rempli -2.21% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→65% · +2.0%→44% · +3.0%→29% · +5.0%→10% · +8.0%→3%
- Range intraday médian 5.43% (p90 9.76%) · excursion haute méd. +1.61% / basse méd. −3.14%
- Profil de vol intra : ouverture 3.843% vs midi 1.047% vs clôture 1.133% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 83% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; mean-reverting — autocorr -0.093)_ ; drift intra méd. -0.48% ; recovery-V 24%
- **σ réalisé intraday** 3.079% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 59% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 670212.5 (VA 668787.5–678762.5 ; dernier close 676000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 25% · rebond 73% · **stop −4.4%** sous le fill (sous le bruit) · cible +2.21% · R/R 0.5 (high win-rate)
- Gaps overnight (n=152) : méd. 0.37% · baisse 41% (gap-down >1% 22% · >2% 12%)
- Excursion ouverture 5min (n=160) : bas méd −1.48% (p90 −3.62%) · haut méd +0.73% · range méd 2.47%
- Excursion ouverture 15min (n=160) : bas méd −1.66% (p90 −3.95%) · haut méd +0.84% · range méd 2.96%
- Excursion ouverture 30min (n=160) : bas méd −1.82% (p90 −4.62%) · haut méd +0.95% · range méd 3.19%
- Excursion ouverture 60min (n=160) : bas méd −1.95% (p90 −4.76%) · haut méd +1.08% · range méd 3.55%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 678000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 74% (104/152) · gap 34% · délai 0.0min · rebond 52% (51/104) (MFE +1.05%)
   - −1.0% : fill 30min 57% · séance 68% (97/152) · gap 22% · délai 0.0min · rebond 57% (55/97) (MFE +1.29%)
   - −1.5% : fill 30min 51% · séance 65% (90/152) · gap 18% · délai 0.3min · rebond 62% (56/90) (MFE +1.26%)
   - −2.0% : fill 30min 44% · séance 58% (82/152) · gap 12% · délai 1.1min · rebond 68% (56/82) (MFE +1.78%)
   - −3.0% : fill 30min 32% · séance 47% (67/152) · gap 8% · délai 3.4min · rebond 70% (48/67) (MFE +1.77%)
   - −4.0% : fill 30min 20% · séance 34% (51/152) · gap 4% · délai 8.6min · rebond 74% (37/51) (MFE +1.72%)
   - −5.0% : fill 30min 12% · séance 25% (39/152) · gap 2% · délai 37.1min · rebond 73% (29/39) (MFE +2.21%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.88% (p90 −3.14%) → stop au-delà de −2.06% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.99% (p90 −3.0%) → stop au-delà de −2.07% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.08% (p90 −3.96%) → stop au-delà de −3.05% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=825 jambes) : jambe baissière méd −1.15% (p90 −3.12%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (51 séances) :
      · −1.0% : fill 100% (51/51) · rebond 53% (27/51)
      · −2.0% : fill 99% (48/51) · rebond 67% (31/48)
      · −3.0% : fill 82% (42/51) · rebond 75% (30/42)
      · −4.0% : fill 61% (33/51) · rebond 76% (24/33)
      · −5.0% : fill 47% (26/51) · rebond 77% (21/26)
   - **flat** (16 séances) :
      · −1.0% : fill 97% (15/16) · rebond 65% (9/15)
      · −2.0% : fill 66% (11/16) · rebond 55% (8/11)
      · −3.0% : fill 54% (9/16) · rebond 34% (5/9)
      · −4.0% : fill 35% (7/16) · rebond 63% (4/7)
      · −5.0% : fill 35% (7/16) · rebond 72% (5/7)
   - **gap-up** (85 séances) :
      · −1.0% : fill 39% (31/85) · rebond 59% (19/31)
      · −2.0% : fill 28% (23/85) · rebond 79% (17/23)
      · −3.0% : fill 19% (16/85) · rebond 75% (13/16)
      · −4.0% : fill 13% (11/85) · rebond 72% (9/11)
      · −5.0% : fill 6% (6/85) · rebond 55% (3/6)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 35% en base · 42% si les 15 1res min sont vertes (61 cas) · 32% si rouges (99 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:30** → P(séance verte=clôture>ouverture) 76% si début vert vs 13% si rouge (base 35% · écart 63 pts) ; prédictivité sature ensuite (plafond brut 176min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=63) : tient le vert **76%** · continue >prix actuel 52% ; creux résiduel méd -1.32% (q20 -3.55%) → **SL/trailing à −3.55%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.42% / q75 +2.59% → **scale +1.42% / runner +2.59%**, sortie à la clôture
  - **si ROUGE au coude** (n=97) : edge inversé — récupère vert seulement **13%** (continue à baisser 49%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.23%** (au-delà de la MAE q10 -4.23%), cible rebond +0.97% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.33% .. +2.67%] · haut q95 +3.81% · bas q05 -5.1%
   - 60min (n=160) : retour [-5.12% .. +2.44%] · haut q95 +4.27% · bas q05 -5.68%
   - 2h (n=160) : retour [-5.67% .. +3.46%] · haut q95 +4.58% · bas q05 -6.42%
   - 4h (n=160) : retour [-6.35% .. +3.35%] · haut q95 +4.79% · bas q05 -7.79%
   - 6h (n=160) : retour [-6.77% .. +4.49%] · haut q95 +5.4% · bas q05 -8.54%
   - session (n=160) : retour [-6.53% .. +4.5%] · haut q95 +5.73% · bas q05 -8.69%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.48%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.17 · part idiosyncratique 0.83
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 22.7  _(survente)_
- **ADX** : 16.2  _(pas de tendance nette)_
- **MACD** : hist -4898.394  _(pas de croisement recent)_
- **BB** : %B -0.09 · largeur 19.2%
- **ATR** : 28500.0 (3.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.208  _(distribution)_
- **Vol ratio** : 1.98  _(volume au-dessus de la moyenne)_
- **Choppiness** : 48.1  _(transition)_
- **MA** : MA20 707600.0 · MA50 726966.88 · MA200 909195.84  _(prix < MA20)_
- **Dist MA** : MA20 -11.2% · MA50 -13.6% · MA200 -30.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (563709 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
