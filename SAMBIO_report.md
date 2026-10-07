# 207940

**Generated** : 2026-10-07T22:02:48.569733+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 2/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · ₩1277000.00  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (2 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot ₩1277000.00 (+0.3% vs entrée) · entrée ₩1273169.00 · stop ₩1171315.48 · T1 ₩1292168.92 · R/R 0.19  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -1213 % hors [0,100] (R² max 0.53). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1270611.53–₩1275726.47 (mid ₩1273169.00)
- Spot actuel : ₩1277000.00 (+0.3% au-dessus de la zone — repli à attendre)
- Stop : ₩1171315.48 (plancher anti-bruit 5 s — stop EV-optimal −8% (first-passage 5 s réel) ; -8.00 % depuis l'entree)
- Targets : T1 ₩1292168.92 · R/R 0.19 | T2 ₩1311168.83 · R/R 0.37 | T3 ₩1330168.75 · R/R 0.56
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1171315.48


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.57 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (3.35 %)** : le gap seul le franchit 0.492 % des séances (6 fois sur 1219).
   - exécution **1.791 pt plus bas** dans le cas TYPIQUE (médiane), 2.066 au p90, **2.108 au pire**
   - perte réelle **4.948 %** en moyenne _(tirée par la queue)_, jusqu'à **5.458 %** — au lieu des 3.35 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0079 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.254 % | p01 -2.573 % | pire -5.458 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0037** [0.0002 ; 0.0227] _(largeur 2.2 pt, n_eff 173.1)_
   - swing : **0.499** [0.4465 ; 0.5515] _(largeur 10.5 pt, n_eff 345.6)_
   - deep : **0.52** [0.4673 ; 0.5723] _(largeur 10.5 pt, n_eff 345.6)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 95.6 observations effectives », dont la borne haute a 95 % vaut environ 3.1 %.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-4.16 %** | CVaR **-5.91 %** | vol 2.59 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 1.28 % contre 2.71 % aujourd'hui, rapport 0.47)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.62 % vs -6.24 % si l'on extrapolait par √5 _(rapport 0.9 ; < 1 = le √5 surestime)_
- **β de baisse : 0.3073** (β de hausse 0.222, asymétrie 1.3841) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.05 | EV/share : ₩-5135.316 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 38 % | T2 20 % | T3 6 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 57.2 | side 37.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.304% → cible +1.492% / stop −8.0%, p_fill 88%, n_eff≈95.6) : P(cible|rempli) **32%** · **EV/risk -0.047** (×p_fill ; si rempli -0.43% du capital)
  - **swing** (entrée dip −0.374% → cible +3.339% / stop −2.987%, p_fill 94%, n_eff≈109.7) : P(cible|rempli) **31%** · **EV/risk -0.269** (×p_fill ; si rempli -0.85% du capital)
  - **deep** (entrée dip −0.466% → cible +4.727% / stop −4.484%, p_fill 96%, n_eff≈107.1) : P(cible|rempli) **35%** · **EV/risk -0.245** (×p_fill ; si rempli -1.14% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→70% · +1.0%→53% · +2.0%→32% · +3.0%→20% · +5.0%→4% · +8.0%→2%
- Range intraday médian 3.64% (p90 6.02%) · excursion haute méd. +1.04% / basse méd. −1.54%
- Profil de vol intra : ouverture 2.265% vs midi 0.627% vs clôture 0.744% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 15% · trend ↑1%/↓3% ; spike-down 50% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.141 ; mean-reverting — autocorr -0.106)_ ; drift intra méd. -0.235% ; recovery-V 24%
- **σ réalisé intraday** 1.956% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 54% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 1368762.5 (VA 1354937.5–1388512.5 ; dernier close 1354000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 38% · rebond 60% · **stop −2.94%** sous le fill (sous le bruit) · cible +1.39% · R/R 0.47 (high win-rate)
- Gaps overnight (n=152) : méd. 0.07% · baisse 38% (gap-down >1% 16% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −2.0%) · haut méd +0.47% · range méd 1.25%
- Excursion ouverture 15min (n=160) : bas méd −0.88% (p90 −2.4%) · haut méd +0.56% · range méd 1.62%
- Excursion ouverture 30min (n=160) : bas méd −0.92% (p90 −2.53%) · haut méd +0.58% · range méd 1.8%
- Excursion ouverture 60min (n=160) : bas méd −1.08% (p90 −3.29%) · haut méd +0.74% · range méd 2.13%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1354000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 81% (111/152) · gap 24% · délai 0.4min · rebond 46% (51/111) (MFE +0.9%)
   - −1.0% : fill 30min 48% · séance 63% (89/152) · gap 16% · délai 1.4min · rebond 52% (43/89) (MFE +1.01%)
   - −1.5% : fill 30min 35% · séance 50% (71/152) · gap 8% · délai 3.5min · rebond 52% (33/71) (MFE +1.38%)
   - −2.0% : fill 30min 21% · séance 38% (57/152) · gap 5% · délai 7.6min · rebond 60% (31/57) (MFE +1.39%)
   - −3.0% : fill 30min 9% · séance 20% (34/152) · gap 2% · délai 53.3min · rebond 42% (17/34) (MFE +0.74%)
   - −4.0% : fill 30min 5% · séance 13% (19/152) · gap 2% · délai 67.5min · rebond 47% (9/19) (MFE +0.96%)
   - −5.0% : fill 30min 2% · séance 6% (10/152) · gap 2% · délai 110.1min · rebond 80% (8/10) (MFE +1.69%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.58% (p90 −1.86%) → stop au-delà de −1.4% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.9% (p90 −2.1%) → stop au-delà de −1.57% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.87% (p90 −2.09%) → stop au-delà de −1.58% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=402 jambes) : jambe baissière méd −1.07% (p90 −2.66%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (44 séances) :
      · −1.0% : fill 100% (43/44) · rebond 63% (24/43)
      · −2.0% : fill 69% (32/44) · rebond 72% (17/32)
      · −3.0% : fill 26% (18/44) · rebond 44% (9/18)
      · −4.0% : fill 18% (10/44) · rebond 58% (5/10)
      · −5.0% : fill 10% (6/44) · rebond 100% (6/6)
   - **flat** (40 séances) :
      · −1.0% : fill 56% (25/40) · rebond 39% (7/25)
      · −2.0% : fill 32% (13/40) · rebond 36% (6/13)
      · −3.0% : fill 28% (10/40) · rebond 50% (6/10)
      · −4.0% : fill 12% (5/40) · rebond 60% (3/5)
      · −5.0% : fill 5% (2/40) · rebond 55% (1/2)
   - **gap-up** (68 séances) :
      · −1.0% : fill 40% (21/68) · rebond 43% (12/21)
      · −2.0% : fill 20% (12/68) · rebond 53% (8/12)
      · −3.0% : fill 11% (6/68) · rebond 25% (2/6)
      · −4.0% : fill 9% (4/68) · rebond 19% (1/4)
      · −5.0% : fill 3% (2/68) · rebond 52% (1/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 78% si les 15 1res min sont vertes (54 cas) · 28% si rouges (106 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **24min** → P(séance verte=clôture>ouverture) 80% si début vert vs 22% si rouge (base 46% · écart 58 pts) ; prédictivité sature ensuite (plafond brut 220min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=60) : tient le vert **80%** · continue >prix actuel 52% ; creux résiduel méd -0.95% (q20 -1.91%) → **SL/trailing à −1.91%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.15% / q75 +2.6% → **scale +1.15% / runner +2.6%**, sortie à la clôture
  - **si ROUGE au coude** (n=100) : edge inversé — récupère vert seulement **22%** (continue à baisser 59%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.49%** (au-delà de la MAE q10 -3.49%), cible rebond +0.93% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.02% .. +2.69%] · haut q95 +3.0% · bas q05 -3.49%
   - 60min (n=160) : retour [-3.26% .. +2.21%] · haut q95 +3.43% · bas q05 -3.75%
   - 2h (n=160) : retour [-3.64% .. +3.17%] · haut q95 +3.98% · bas q05 -4.22%
   - 4h (n=160) : retour [-4.18% .. +3.04%] · haut q95 +4.11% · bas q05 -4.76%
   - 6h (n=160) : retour [-4.73% .. +3.16%] · haut q95 +4.53% · bas q05 -5.43%
   - session (n=160) : retour [-4.55% .. +3.12%] · haut q95 +4.53% · bas q05 -5.45%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 207940 = **plat / peu volatil** (vol intra méd 1.99%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.24 · part idiosyncratique 0.76
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 26.9  _(survente)_
- **ADX** : 25.3  _(tendance etablie)_
- **MACD** : hist -8337.112  _(pas de croisement recent)_
- **BB** : %B -0.15 · largeur 12.9%
- **ATR** : 37999.83 (17.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.114  _(distribution)_
- **Vol ratio** : 1.53  _(volume au-dessus de la moyenne)_
- **Choppiness** : 45.7  _(transition)_
- **MA** : MA20 1393980.57 · MA50 1475632.23 · MA200 1545518.06  _(prix < MA20)_
- **Dist MA** : MA20 -8.4% · MA50 -13.5% · MA200 -17.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (564476 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
