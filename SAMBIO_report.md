# 207940

**Generated** : 2026-07-22T21:54:48.776358+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite high · ₩1372000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot ₩1372000.00 (+1.8% vs entrée) · entrée ₩1347125.00 · stop ₩1239355.00 · T1 ₩1373675.10 · R/R 0.25  
> ↳ P(T1 av. stop) 37 % _(réel 5 s)_ · EV/risk -0.012 _(réel 5 s)_ (GBM -0.07) · ¼-Kelly 0.051 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1341814.98–₩1352435.02 (mid ₩1347125.00)
- Spot actuel : ₩1372000.00 (+1.8% au-dessus de la zone — repli à attendre)
- Stop : ₩1239355.00 (stop swing_plan-based (-6.1%))
- Targets : T1 ₩1373675.10 · R/R 0.25 | T2 ₩1400225.20 · R/R 0.49 | T3 ₩1426775.30 · R/R 0.74
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1239355.00


## Edge, scénarios & sizing

- EV/risk : -0.07 | EV/share : ₩-7528.337 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 9 % | T3 4 %
- Kelly (position) : f* 0.205 | ¼-Kelly 0.051 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 8.9 | bear 15.5 | side 75.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.815% → cible +1.971% / stop −8.0%, p_fill 62%, n_eff≈24.7) : P(cible|rempli) **37%** · **EV/risk -0.012** (×p_fill ; si rempli -0.16% du capital)
  - **swing** (entrée dip −3.984% → cible +4.407% / stop −2.204%, p_fill 36%, n_eff≈13.1) : P(cible|rempli) **43%** · **EV/risk +0.097** (×p_fill ; si rempli +0.59% du capital)
  - **deep** (entrée dip −6.166% → cible +6.232% / stop −3.116%, p_fill 36%, n_eff≈11.2) : P(cible|rempli) **74%** · **EV/risk +0.426** (×p_fill ; si rempli +3.73% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→68% · +1.0%→50% · +2.0%→34% · +3.0%→21% · +5.0%→4% · +8.0%→1%
- Range intraday médian 3.93% (p90 6.08%) · excursion haute méd. +0.98% / basse méd. −1.69%
- Profil de vol intra : ouverture 2.342% vs midi 0.654% vs clôture 0.775% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (137 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 13% · trend ↑0%/↓3% ; spike-down 58% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.132 ; neutre — autocorr -0.021)_ ; drift intra méd. -0.462% ; recovery-V 37%
- **σ réalisé intraday** 3.165% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 62% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 1403787.5 (VA 1393437.5–1412412.5 ; dernier close 1393000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 16% · rebond 60% · **stop −1.96%** sous le fill (sous le bruit) · cible +1.72% · R/R 0.88 (high win-rate)
- Gaps overnight (n=136) : méd. 0.44% · baisse 29% (gap-down >1% 7% · >2% 4%)
- Excursion ouverture 5min (n=137) : bas méd −0.9% (p90 −2.42%) · haut méd +0.45% · range méd 1.52%
- Excursion ouverture 15min (n=137) : bas méd −1.09% (p90 −2.93%) · haut méd +0.51% · range méd 1.91%
- Excursion ouverture 30min (n=137) : bas méd −1.26% (p90 −3.12%) · haut méd +0.55% · range méd 2.41%
- Excursion ouverture 60min (n=137) : bas méd −1.3% (p90 −3.49%) · haut méd +0.64% · range méd 2.68%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1393000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 74% (91/136) · gap 18% · délai 1.2min · rebond 50% (39/91) (MFE +1.01%)
   - −1.0% : fill 30min 48% · séance 61% (73/136) · gap 7% · délai 2.5min · rebond 53% (31/73) (MFE +1.13%)
   - −1.5% : fill 30min 39% · séance 49% (56/136) · gap 6% · délai 3.8min · rebond 52% (25/56) (MFE +1.14%)
   - −2.0% : fill 30min 26% · séance 42% (49/136) · gap 4% · délai 8.9min · rebond 64% (26/49) (MFE +1.34%)
   - −3.0% : fill 30min 8% · séance 28% (31/136) · gap 2% · délai 105.3min · rebond 60% (17/31) (MFE +1.39%)
   - −4.0% : fill 30min 4% · séance 16% (16/136) · gap 2% · délai 73.7min · rebond 60% (9/16) (MFE +1.72%)
   - −5.0% : fill 30min 2% · séance 8% (9/136) · gap 2% · délai 190.8min · rebond 65% (6/9) (MFE +1.55%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.83% (p90 −2.45%) → stop au-delà de −1.64% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.0% (p90 −2.09%) → stop au-delà de −1.56% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.18% (p90 −2.45%) → stop au-delà de −1.88% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=332 jambes) : jambe baissière méd −1.1% (p90 −2.72%) · ~8.3 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (30 séances) :
      · −1.0% : fill 98% (29/30) · rebond 64% (14/29)
      · −2.0% : fill 85% (25/30) · rebond 65% (12/25)
      · −3.0% : fill 44% (13/30) · rebond 57% (7/13)
      · −4.0% : fill 26% (7/30) · rebond 58% (3/7)
      · −5.0% : fill 10% (4/30) · rebond 100% (4/4)
   - **flat** (41 séances) :
      · −1.0% : fill 69% (23/41) · rebond 31% (7/23)
      · −2.0% : fill 40% (10/41) · rebond 57% (5/10)
      · −3.0% : fill 30% (7/41) · rebond 97% (6/7)
      · −4.0% : fill 17% (4/41) · rebond 100% (4/4)
      · −5.0% : fill 8% (2/41) · rebond 89% (1/2)
   - **gap-up** (65 séances) :
      · −1.0% : fill 43% (21/65) · rebond 60% (10/21)
      · −2.0% : fill 26% (14/65) · rebond 68% (9/14)
      · −3.0% : fill 21% (11/65) · rebond 40% (4/11)
      · −4.0% : fill 11% (5/65) · rebond 33% (2/5)
      · −5.0% : fill 8% (3/65) · rebond 35% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=137) : 39% en base · 64% si les 15 1res min sont vertes (46 cas) · 26% si rouges (91 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=137) : COUDE à **33min** → P(séance verte=clôture>ouverture) 66% si début vert vs 25% si rouge (base 39% · écart 42 pts) ; prédictivité sature ensuite (plafond brut 218min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=48) : tient le vert **66%** · continue >prix actuel 36% ; creux résiduel méd -1.41% (q20 -2.83%) → **SL/trailing à −2.83%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.14% / q75 +1.86% → **scale +1.14% / runner +1.86%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **25%** (continue à baisser 50%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.34%** (au-delà de la MAE q10 -3.34%), cible rebond +1.25% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=137) : retour [-3.05% .. +2.55%] · haut q95 +3.2% · bas q05 -3.56%
   - 60min (n=137) : retour [-3.56% .. +2.49%] · haut q95 +3.36% · bas q05 -3.96%
   - 2h (n=137) : retour [-4.44% .. +3.34%] · haut q95 +4.2% · bas q05 -4.86%
   - 4h (n=137) : retour [-5.33% .. +3.67%] · haut q95 +4.82% · bas q05 -5.58%
   - 6h (n=137) : retour [-5.36% .. +4.01%] · haut q95 +4.82% · bas q05 -6.1%
   - session (n=137) : retour [-4.92% .. +3.61%] · haut q95 +4.82% · bas q05 -6.1%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 207940 = **plat / peu volatil** (vol intra méd 1.99%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 47.1  _(neutre)_
- **ADX** : 9.6  _(pas de tendance nette)_
- **MACD** : hist -597.509  _(bearish_recent)_
- **BB** : %B 0.37 · largeur 8.4%
- **ATR** : 67857.14 (86.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.0  _(neutre)_
- **Vol ratio** : 0.69  _(volume normal)_
- **Choppiness** : 68.5  _(marche en range (choppy))_
- **MA** : MA20 1387250.0 · MA50 1372140.0 · MA200 1613335.11  _(prix < MA20)_
- **Dist MA** : MA20 -1.1% · MA50 -0.0% · MA200 -15.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (82809 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
