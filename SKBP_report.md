# 326030

**Generated** : 2026-07-21T21:47:21.713881+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩77600.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot ₩77600.00 (+5.8% vs entrée) · entrée ₩73364.29 · stop ₩72093.57 · T1 ₩75022.63 · R/R 1.31  
> ↳ P(T1 av. stop) 33 % · EV/risk -0.141 · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.73% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩73032.62–₩73695.95 (mid ₩73364.29)
- Spot actuel : ₩77600.00 (+5.8% au-dessus de la zone — repli à attendre)
- Stop : ₩72093.57 (stop swing_plan-based (-13.17%))
- Targets : T1 ₩75022.63 · R/R 1.31 | T2 ₩76680.97 · R/R 2.61 | T3 ₩78339.32 · R/R 3.92
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩72093.57


## Edge, scénarios & sizing

- EV/risk : -0.141 | EV/share : ₩-178.675 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 33 % | T2 9 % | T3 6 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 18.9 | bear 74.3 | side 6.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=5, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→71% · +1.0%→60% · +2.0%→42% · +3.0%→26% · +5.0%→9% · +8.0%→4%
- Range intraday médian 4.08% (p90 7.23%) · excursion haute méd. +1.55% / basse méd. −2.12%
- Profil de vol intra : ouverture 2.621% vs midi 0.762% vs clôture 0.782% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (136 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 16% · trend ↑2%/↓2% ; spike-down 60% · recovery-V 20%)_
- **Régime intraday** : **chop** _(efficiency 0.132 ; mean-reverting — autocorr -0.061)_ ; drift intra méd. -0.589% ; recovery-V 22%
- **σ réalisé intraday** 3.377% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 68% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 78032.5 (VA 77512.5–79267.5 ; dernier close 77100.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 16% · rebond 81% · **stop −2.91%** sous le fill (sous le bruit) · cible +1.92% · R/R 0.66 (high win-rate)
- Gaps overnight (n=135) : méd. 0.12% · baisse 42% (gap-down >1% 16% · >2% 7%)
- Excursion ouverture 5min (n=136) : bas méd −0.77% (p90 −2.3%) · haut méd +0.63% · range méd 1.89%
- Excursion ouverture 15min (n=136) : bas méd −0.95% (p90 −2.99%) · haut méd +0.7% · range méd 2.23%
- Excursion ouverture 30min (n=136) : bas méd −1.09% (p90 −3.1%) · haut méd +0.85% · range méd 2.56%
- Excursion ouverture 60min (n=136) : bas méd −1.27% (p90 −3.23%) · haut méd +1.07% · range méd 2.94%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 77100.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 79% (99/135) · gap 25% · délai 0.3min · rebond 50% (41/99) (MFE +0.95%)
   - −1.0% : fill 30min 56% · séance 70% (89/135) · gap 16% · délai 2.0min · rebond 54% (42/89) (MFE +1.01%)
   - −1.5% : fill 30min 41% · séance 56% (68/135) · gap 8% · délai 3.6min · rebond 57% (34/68) (MFE +1.15%)
   - −2.0% : fill 30min 29% · séance 50% (57/135) · gap 7% · délai 16.4min · rebond 64% (32/57) (MFE +1.43%)
   - −3.0% : fill 30min 11% · séance 36% (37/135) · gap 4% · délai 89.7min · rebond 56% (16/37) (MFE +1.32%)
   - −4.0% : fill 30min 8% · séance 22% (25/135) · gap 3% · délai 112.9min · rebond 54% (12/25) (MFE +1.03%)
   - −5.0% : fill 30min 6% · séance 16% (19/135) · gap 3% · délai 118.4min · rebond 81% (12/19) (MFE +1.92%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.41% (p90 −2.75%) → stop au-delà de −1.25% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.73% (p90 −1.92%) → stop au-delà de −1.4% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.73% (p90 −2.23%) → stop au-delà de −1.41% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=440 jambes) : jambe baissière méd −1.15% (p90 −2.49%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (40 séances) :
      · −1.0% : fill 100% (40/40) · rebond 63% (21/40)
      · −2.0% : fill 72% (28/40) · rebond 61% (14/28)
      · −3.0% : fill 48% (18/40) · rebond 49% (7/18)
      · −4.0% : fill 40% (15/40) · rebond 65% (8/15)
      · −5.0% : fill 31% (12/40) · rebond 85% (8/12)
   - **flat** (35 séances) :
      · −1.0% : fill 72% (25/35) · rebond 37% (9/25)
      · −2.0% : fill 58% (18/35) · rebond 74% (12/18)
      · −3.0% : fill 45% (11/35) · rebond 71% (6/11)
      · −4.0% : fill 33% (8/35) · rebond 39% (3/8)
      · −5.0% : fill 23% (6/35) · rebond 79% (4/6)
   - **gap-up** (60 séances) :
      · −1.0% : fill 46% (24/60) · rebond 58% (12/24)
      · −2.0% : fill 28% (11/60) · rebond 56% (6/11)
      · −3.0% : fill 21% (8/60) · rebond 47% (3/8)
      · −4.0% : fill 3% (2/60) · rebond 71% (1/2)
      · −5.0% : fill 1% (1/60) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=136) : 37% en base · 70% si les 15 1res min sont vertes (48 cas) · 15% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=136) : COUDE à **1:38** → P(séance verte=clôture>ouverture) 76% si début vert vs 6% si rouge (base 37% · écart 69 pts) ; prédictivité sature ensuite (plafond brut 195min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=54) : tient le vert **76%** · continue >prix actuel 47% ; creux résiduel méd -1.44% (q20 -2.19%) → **SL/trailing à −2.19%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.35% / q75 +2.0% → **scale +1.35% / runner +2.0%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **6%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.0%** (au-delà de la MAE q10 -4.0%), cible rebond +0.75% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=136) : retour [-2.79% .. +2.47%] · haut q95 +3.65% · bas q05 -4.04%
   - 60min (n=136) : retour [-3.82% .. +2.56%] · haut q95 +4.2% · bas q05 -4.51%
   - 2h (n=136) : retour [-3.49% .. +3.89%] · haut q95 +4.51% · bas q05 -4.69%
   - 4h (n=136) : retour [-4.24% .. +5.19%] · haut q95 +6.28% · bas q05 -5.79%
   - 6h (n=136) : retour [-4.65% .. +4.25%] · haut q95 +7.05% · bas q05 -6.0%
   - session (n=136) : retour [-4.75% .. +4.61%] · haut q95 +7.05% · bas q05 -6.0%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 326030 = **plat / peu volatil** (vol intra méd 2.3%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 33.1  _(momentum baissier)_
- **ADX** : 16.5  _(pas de tendance nette)_
- **MACD** : hist -381.743  _(pas de croisement recent)_
- **BB** : %B 0.2 · largeur 21.1%
- **ATR** : 4235.71 (50.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.141  _(distribution)_
- **Vol ratio** : 0.81  _(volume normal)_
- **Choppiness** : 50.8  _(transition)_
- **MA** : MA20 82850.0 · MA50 88520.0 · MA200 107192.0  _(prix < MA20)_
- **Dist MA** : MA20 -6.3% · MA50 -12.3% · MA200 -27.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (81159 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
