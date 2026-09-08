# 207940

**Generated** : 2026-09-08T00:31:14.166707+00:00  
**Santé technique** : 5/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1466000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot ₩1466000.00 (+3.4% vs entrée) · entrée ₩1417625.00 · stop ₩1304215.00 · T1 ₩1435169.88 · R/R 0.15  
> ↳ P(T1 av. stop) 89 % · EV/risk 0.125 · ¼-Kelly 0.105 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1414116.02–₩1421133.98 (mid ₩1417625.00)
- Spot actuel : ₩1466000.00 (+3.4% au-dessus de la zone — repli à attendre)
- Stop : ₩1304215.00 (stop swing_plan-based (-10.77%))
- Targets : T1 ₩1435169.88 · R/R 0.15 | T2 ₩1452714.76 · R/R 0.31 | T3 ₩1470259.64 · R/R 0.46
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1304215.00


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.57 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (10.77 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1217).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 10.77 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.298 % | p01 -2.673 % | pire -5.458 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0046** [0.0004 ; 0.0245] _(largeur 2.4 pt, n_eff 173.1)_
   - swing : **0.3352** [0.287 ; 0.3862] _(largeur 9.9 pt, n_eff 345.6)_
   - deep : **0.3444** [0.2958 ; 0.3956] _(largeur 10.0 pt, n_eff 345.6)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 10.0 observations effectives », dont la borne haute a 95 % vaut environ 29.9 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (55.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-4.06 %** | CVaR **-5.87 %** | vol 2.55 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 1.59 % contre 2.78 % aujourd'hui, rapport 0.57)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.7 % vs -6.25 % si l'on extrapolait par √5 _(rapport 0.913 ; < 1 = le √5 surestime)_
- **β de baisse : 0.3213** (β de hausse 0.2175, asymétrie 1.4768) vs KS11 — 552 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.023 | EV/share : ₩-2615.265 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 58 % | T2 37 % | T3 11 %
- Kelly (position) : f* 0.422 | ¼-Kelly 0.105 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 59.4 | bear 34.5 | side 6.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.304% → cible +1.238% / stop −8.0%, p_fill 26%, n_eff≈10.0) : P(cible|rempli) **46%** · **EV/risk +0.023** (×p_fill ; si rempli +0.73% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=6, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→65% · +2.0%→44% · +3.0%→25% · +5.0%→6% · +8.0%→2%
- Range intraday médian 4.11% (p90 6.65%) · excursion haute méd. +1.47% / basse méd. −2.06%
- Profil de vol intra : ouverture 2.698% vs midi 0.748% vs clôture 0.902% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 14% · trend ↑1%/↓2% ; spike-down 53% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; mean-reverting — autocorr -0.07)_ ; drift intra méd. -0.107% ; recovery-V 32%
- **σ réalisé intraday** 2.434% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 59% / bas 39% / whipsaw 9%
- POC intraday (dernière séance, temps-au-prix) : 1441612.5 (VA 1433662.5–1454862.5 ; dernier close 1446000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 44% · rebond 65% · **stop −2.83%** sous le fill (sous le bruit) · cible +1.47% · R/R 0.52 (high win-rate)
- Gaps overnight (n=159) : méd. 0.07% · baisse 40% (gap-down >1% 15% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.79% (p90 −2.18%) · haut méd +0.5% · range méd 1.38%
- Excursion ouverture 15min (n=160) : bas méd −1.03% (p90 −2.84%) · haut méd +0.6% · range méd 1.8%
- Excursion ouverture 30min (n=160) : bas méd −1.08% (p90 −3.14%) · haut méd +0.75% · range méd 2.06%
- Excursion ouverture 60min (n=160) : bas méd −1.26% (p90 −3.49%) · haut méd +0.92% · range méd 2.31%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1447000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 80% (113/159) · gap 25% · délai 0.2min · rebond 56% (55/113) (MFE +1.17%)
   - −1.0% : fill 30min 52% · séance 65% (91/159) · gap 15% · délai 1.2min · rebond 56% (44/91) (MFE +1.23%)
   - −1.5% : fill 30min 42% · séance 55% (74/159) · gap 10% · délai 2.7min · rebond 58% (38/74) (MFE +1.45%)
   - −2.0% : fill 30min 28% · séance 44% (60/159) · gap 6% · délai 5.9min · rebond 65% (34/60) (MFE +1.47%)
   - −3.0% : fill 30min 12% · séance 24% (36/159) · gap 3% · délai 38.3min · rebond 48% (18/36) (MFE +0.94%)
   - −4.0% : fill 30min 6% · séance 14% (19/159) · gap 3% · délai 54.6min · rebond 56% (10/19) (MFE +1.36%)
   - −5.0% : fill 30min 3% · séance 7% (10/159) · gap 2% · délai 111.5min · rebond 80% (8/10) (MFE +1.69%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.78% (p90 −2.14%) → stop au-delà de −1.5% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.95% (p90 −2.14%) → stop au-delà de −1.72% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.89% (p90 −2.13%) → stop au-delà de −1.69% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=406 jambes) : jambe baissière méd −1.07% (p90 −2.7%) · ~7.2 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (43 séances) :
      · −1.0% : fill 100% (42/43) · rebond 64% (23/42)
      · −2.0% : fill 73% (32/43) · rebond 76% (18/32)
      · −3.0% : fill 31% (18/43) · rebond 44% (9/18)
      · −4.0% : fill 22% (10/43) · rebond 59% (5/10)
      · −5.0% : fill 12% (6/43) · rebond 100% (6/6)
   - **flat** (48 séances) :
      · −1.0% : fill 66% (29/48) · rebond 36% (9/29)
      · −2.0% : fill 40% (14/48) · rebond 35% (6/14)
      · −3.0% : fill 35% (10/48) · rebond 49% (6/10)
      · −4.0% : fill 15% (5/48) · rebond 60% (3/5)
      · −5.0% : fill 6% (2/48) · rebond 55% (1/2)
   - **gap-up** (68 séances) :
      · −1.0% : fill 36% (20/68) · rebond 66% (12/20)
      · −2.0% : fill 24% (14/68) · rebond 72% (10/14)
      · −3.0% : fill 12% (8/68) · rebond 53% (3/8)
      · −4.0% : fill 7% (4/68) · rebond 42% (2/4)
      · −5.0% : fill 4% (2/68) · rebond 52% (1/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 71% si les 15 1res min sont vertes (55 cas) · 30% si rouges (105 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **34min** → P(séance verte=clôture>ouverture) 76% si début vert vs 25% si rouge (base 45% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 218min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=59) : tient le vert **76%** · continue >prix actuel 40% ; creux résiduel méd -1.35% (q20 -1.93%) → **SL/trailing à −1.93%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.22% / q75 +2.22% → **scale +1.22% / runner +2.22%**, sortie à la clôture
  - **si ROUGE au coude** (n=101) : edge inversé — récupère vert seulement **25%** (continue à baisser 52%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.55%** (au-delà de la MAE q10 -3.55%), cible rebond +1.25% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.22% .. +2.59%] · haut q95 +3.22% · bas q05 -3.6%
   - 60min (n=160) : retour [-3.53% .. +2.49%] · haut q95 +3.36% · bas q05 -4.16%
   - 2h (n=160) : retour [-3.49% .. +3.29%] · haut q95 +4.21% · bas q05 -4.67%
   - 4h (n=160) : retour [-4.32% .. +2.83%] · haut q95 +4.82% · bas q05 -5.37%
   - 6h (n=160) : retour [-4.67% .. +3.5%] · haut q95 +4.82% · bas q05 -5.39%
   - session (n=160) : retour [-4.21% .. +3.24%] · haut q95 +4.82% · bas q05 -5.42%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 207940 = **plat / peu volatil** (vol intra méd 2.03%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 40.8  _(momentum baissier)_
- **ADX** : 16.8  _(pas de tendance nette)_
- **MACD** : hist -17155.208  _(pas de croisement recent)_
- **BB** : %B 0.1 · largeur 12.0%
- **ATR** : 51428.57 (47.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.13  _(accumulation)_
- **Vol ratio** : 0.67  _(volume normal)_
- **Choppiness** : 46.3  _(transition)_
- **MA** : MA20 1540250.0 · MA50 1474420.0 · MA200 1578591.6  _(prix < MA20)_
- **Dist MA** : MA20 -4.8% · MA50 -0.6% · MA200 -7.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (482200 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
