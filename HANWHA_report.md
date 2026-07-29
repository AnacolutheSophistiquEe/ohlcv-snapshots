# 012450

**Generated** : 2026-07-29T21:53:19.423959+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩809000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)  
> ↳ spot ₩809000.00 (+10.6% vs entrée) · entrée ₩731357.14 · stop ₩672848.57 · T1 ₩754076.24 · R/R 0.39  
> ↳ P(T1 av. stop) 22 % · EV/risk -0.16 · ¼-Kelly 0.019 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩726813.32–₩735900.96 (mid ₩731357.14)
- Spot actuel : ₩809000.00 (+10.6% au-dessus de la zone — repli à attendre)
- Stop : ₩672848.57 (stop swing_plan-based (-22.07%))
- Targets : T1 ₩754076.24 · R/R 0.39 | T2 ₩776795.35 · R/R 0.78 | T3 ₩799514.45 · R/R 1.16
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩672848.57


## Edge, scénarios & sizing

- EV/risk : -0.16 | EV/share : ₩-9372.869 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 22 % | T2 11 % | T3 11 %
- Kelly (position) : f* 0.075 | ¼-Kelly 0.019 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 14.2 | bear 77.4 | side 8.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=3, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→72% · +1.0%→57% · +2.0%→40% · +3.0%→22% · +5.0%→11% · +8.0%→1%
- Range intraday médian 5.84% (p90 8.67%) · excursion haute méd. +1.66% / basse méd. −3.17%
- Profil de vol intra : ouverture 4.121% vs midi 1.121% vs clôture 1.154% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (146 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓0% ; spike-down 88% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; mean-reverting — autocorr -0.055)_ ; drift intra méd. -1.512% ; recovery-V 36%
- **σ réalisé intraday** 4.589% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 40% / bas 61% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 875375.0 (VA 862775.0–876425.0 ; dernier close 882000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 36% · rebond 81% · **stop −4.94%** sous le fill (sous le bruit) · cible +1.99% · R/R 0.4 (high win-rate)
- Gaps overnight (n=145) : méd. 0.63% · baisse 33% (gap-down >1% 18% · >2% 8%)
- Excursion ouverture 5min (n=146) : bas méd −1.76% (p90 −4.05%) · haut méd +0.79% · range méd 2.82%
- Excursion ouverture 15min (n=146) : bas méd −2.12% (p90 −4.85%) · haut méd +1.08% · range méd 3.4%
- Excursion ouverture 30min (n=146) : bas méd −2.16% (p90 −5.31%) · haut méd +1.08% · range méd 3.95%
- Excursion ouverture 60min (n=146) : bas méd −2.37% (p90 −5.8%) · haut méd +1.29% · range méd 4.36%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 882000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 74% (105/145) · gap 22% · délai 0.2min · rebond 50% (53/105) (MFE +0.84%)
   - −1.0% : fill 30min 57% · séance 71% (101/145) · gap 18% · délai 1.0min · rebond 54% (59/101) (MFE +1.01%)
   - −1.5% : fill 30min 54% · séance 67% (94/145) · gap 11% · délai 1.4min · rebond 60% (54/94) (MFE +1.35%)
   - −2.0% : fill 30min 46% · séance 59% (78/145) · gap 8% · délai 3.5min · rebond 64% (48/78) (MFE +1.63%)
   - −3.0% : fill 30min 32% · séance 47% (57/145) · gap 2% · délai 5.5min · rebond 70% (39/57) (MFE +1.54%)
   - −4.0% : fill 30min 21% · séance 36% (43/145) · gap 2% · délai 14.1min · rebond 81% (35/43) (MFE +1.99%)
   - −5.0% : fill 30min 13% · séance 26% (31/145) · gap 1% · délai 17.3min · rebond 77% (25/31) (MFE +2.22%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.79% (p90 −2.6%) → stop au-delà de −2.12% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.19% (p90 −2.76%) → stop au-delà de −2.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.56% (p90 −2.77%) → stop au-delà de −2.67% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=693 jambes) : jambe baissière méd −1.27% (p90 −3.2%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (32 séances) :
      · −1.0% : fill 100% (32/32) · rebond 44% (14/32)
      · −2.0% : fill 93% (29/32) · rebond 64% (17/29)
      · −3.0% : fill 89% (26/32) · rebond 72% (18/26)
      · −4.0% : fill 75% (23/32) · rebond 88% (19/23)
      · −5.0% : fill 46% (15/32) · rebond 85% (13/15)
   - **flat** (19 séances) :
      · −1.0% : fill 88% (18/19) · rebond 41% (9/18)
      · −2.0% : fill 78% (15/19) · rebond 48% (7/15)
      · −3.0% : fill 60% (9/19) · rebond 37% (3/9)
      · −4.0% : fill 60% (9/19) · rebond 48% (5/9)
      · −5.0% : fill 58% (8/19) · rebond 52% (4/8)
   - **gap-up** (94 séances) :
      · −1.0% : fill 55% (51/94) · rebond 66% (36/51)
      · −2.0% : fill 41% (34/94) · rebond 72% (24/34)
      · −3.0% : fill 27% (22/94) · rebond 86% (18/22)
      · −4.0% : fill 14% (11/94) · rebond 100% (11/11)
      · −5.0% : fill 9% (8/94) · rebond 100% (8/8)
- **P(clôture VERTE) selon le drive 15min** (n=146) : 36% en base · 63% si les 15 1res min sont vertes (48 cas) · 20% si rouges (98 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=146) : COUDE à **49min** → P(séance verte=clôture>ouverture) 85% si début vert vs 10% si rouge (base 36% · écart 75 pts) ; prédictivité sature ensuite (plafond brut 47min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=48) : tient le vert **85%** · continue >prix actuel 55% ; creux résiduel méd -1.6% (q20 -3.31%) → **SL/trailing à −3.31%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.34% / q75 +3.56% → **scale +2.34% / runner +3.56%**, sortie à la clôture
  - **si ROUGE au coude** (n=98) : edge inversé — récupère vert seulement **10%** (continue à baisser 58%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.59%** (au-delà de la MAE q10 -5.59%), cible rebond +1.43% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=146) : retour [-5.47% .. +3.81%] · haut q95 +5.41% · bas q05 -6.31%
   - 60min (n=146) : retour [-5.29% .. +4.69%] · haut q95 +6.71% · bas q05 -7.03%
   - 2h (n=146) : retour [-7.76% .. +4.49%] · haut q95 +6.93% · bas q05 -8.38%
   - 4h (n=146) : retour [-7.28% .. +5.6%] · haut q95 +7.17% · bas q05 -9.55%
   - 6h (n=146) : retour [-7.18% .. +4.79%] · haut q95 +7.55% · bas q05 -10.28%
   - session (n=146) : retour [-7.59% .. +4.87%] · haut q95 +7.55% · bas q05 -10.28%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 012450 = **volatil sans tendance propre (choppy)** (vol intra méd 3.51%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 31.5  _(momentum baissier)_
- **ADX** : 17.8  _(pas de tendance nette)_
- **MACD** : hist -5305.105  _(pas de croisement recent)_
- **BB** : %B 0.11 · largeur 43.7%
- **ATR** : 77642.86 (72.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.202  _(distribution)_
- **Vol ratio** : 1.12  _(volume normal)_
- **Choppiness** : 52.2  _(transition)_
- **MA** : MA20 974450.0 · MA50 1065740.0 · MA200 1141042.51  _(prix < MA20)_
- **Dist MA** : MA20 -17.0% · MA50 -24.1% · MA200 -29.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (81910 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
