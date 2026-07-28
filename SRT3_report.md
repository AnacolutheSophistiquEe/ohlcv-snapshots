# SRT3

**Generated** : 2026-07-28T21:37:22.287183+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · €222.40  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot €222.40 (+5.6% vs entrée) · entrée €210.64 · stop €206.65 · T1 €214.44 · R/R 0.95  
> ↳ P(T1 av. stop) 48 % · EV/risk -0.002 · ¼-Kelly 0.006 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.89% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €209.88–€211.40 (mid €210.64)
- Spot actuel : €222.40 (+5.6% au-dessus de la zone — repli à attendre)
- Stop : €206.65 (stop swing_plan-based (-13.43%))
- Targets : T1 €214.44 · R/R 0.95 | T2 €218.24 · R/R 1.9 | T3 €222.04 · R/R 2.86
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €206.65


## Edge, scénarios & sizing

- EV/risk : -0.002 | EV/share : €-0.009 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 48 % | T2 19 % | T3 10 %
- Kelly (position) : f* 0.025 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.1 | bear 75.4 | side 11.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=5, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→75% · +2.0%→46% · +3.0%→26% · +5.0%→10% · +8.0%→0%
- Range intraday médian 3.65% (p90 7.09%) · excursion haute méd. +1.89% / basse méd. −1.74%
- Profil de vol intra : ouverture 2.188% vs midi 0.907% vs clôture 1.033% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 11% · trend ↑0%/↓0% ; spike-down 54% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; neutre — autocorr -0.001)_ ; drift intra méd. -0.309% ; recovery-V 27%
- **σ réalisé intraday** 2.995% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 62% / whipsaw 30%
- POC intraday (dernière séance, temps-au-prix) : 219.6662 (VA 216.8988–221.2038 ; dernier close 216.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 61% · rebond 74% · **stop −2.54%** sous le fill (sous le bruit) · cible +1.79% · R/R 0.7 (high win-rate)
- Gaps overnight (n=159) : méd. -0.04% · baisse 51% (gap-down >1% 17% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.41% (p90 −2.47%) · haut méd +0.57% · range méd 1.29%
- Excursion ouverture 15min (n=160) : bas méd −0.57% (p90 −2.54%) · haut méd +0.66% · range méd 1.63%
- Excursion ouverture 30min (n=160) : bas méd −0.63% (p90 −2.8%) · haut méd +0.82% · range méd 1.78%
- Excursion ouverture 60min (n=160) : bas méd −0.74% (p90 −2.82%) · haut méd +0.87% · range méd 1.95%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 216.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 80% (126/159) · gap 30% · délai 0.2min · rebond 56% (64/126) (MFE +1.18%)
   - −1.0% : fill 30min 48% · séance 68% (106/159) · gap 17% · délai 0.4min · rebond 63% (64/106) (MFE +1.42%)
   - −1.5% : fill 30min 39% · séance 61% (93/159) · gap 8% · délai 4.5min · rebond 74% (61/93) (MFE +1.79%)
   - −2.0% : fill 30min 25% · séance 44% (72/159) · gap 4% · délai 13.3min · rebond 62% (44/72) (MFE +1.68%)
   - −3.0% : fill 30min 8% · séance 22% (41/159) · gap 2% · délai 144.0min · rebond 57% (24/41) (MFE +1.68%)
   - −4.0% : fill 30min 5% · séance 12% (21/159) · gap 1% · délai 49.4min · rebond 76% (16/21) (MFE +2.62%)
   - −5.0% : fill 30min 1% · séance 9% (12/159) · gap 1% · délai 94.0min · rebond 65% (9/12) (MFE +2.48%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −2.22%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.18% (p90 −2.18%) → stop au-delà de −1.25% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.46% (p90 −2.81%) → stop au-delà de −1.46% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=426 jambes) : jambe baissière méd −1.05% (p90 −2.74%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (76 séances) :
      · −1.0% : fill 86% (64/76) · rebond 72% (43/64)
      · −2.0% : fill 57% (43/76) · rebond 65% (28/43)
      · −3.0% : fill 33% (29/76) · rebond 49% (16/29)
      · −4.0% : fill 16% (15/76) · rebond 71% (11/15)
      · −5.0% : fill 8% (7/76) · rebond 92% (6/7)
   - **flat** (33 séances) :
      · −1.0% : fill 60% (18/33) · rebond 43% (8/18)
      · −2.0% : fill 49% (14/33) · rebond 47% (6/14)
      · −3.0% : fill 23% (6/33) · rebond 66% (4/6)
      · −4.0% : fill 18% (4/33) · rebond 70% (3/4)
      · −5.0% : fill 18% (4/33) · rebond 24% (2/4)
   - **gap-up** (50 séances) :
      · −1.0% : fill 52% (24/50) · rebond 60% (13/24)
      · −2.0% : fill 27% (15/50) · rebond 72% (10/15)
      · −3.0% : fill 9% (6/50) · rebond 78% (4/6)
      · −4.0% : fill 6% (2/50) · rebond 100% (2/2)
      · −5.0% : fill 5% (1/50) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 58% si les 15 1res min sont vertes (90 cas) · 40% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:16** → P(séance verte=clôture>ouverture) 67% si début vert vs 32% si rouge (base 49% · écart 35 pts) ; prédictivité sature ensuite (plafond brut 293min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **67%** · continue >prix actuel 44% ; creux résiduel méd -1.27% (q20 -2.35%) → **SL/trailing à −2.35%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.13% / q75 +2.5% → **scale +1.13% / runner +2.5%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **32%** (continue à baisser 52%) → **RÉDUIRE ~68%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.8%** (au-delà de la MAE q10 -3.8%), cible rebond +1.49% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.16% .. +2.12%] · haut q95 +2.67% · bas q05 -3.61%
   - 60min (n=160) : retour [-3.41% .. +2.32%] · haut q95 +2.79% · bas q05 -4.05%
   - 2h (n=160) : retour [-2.37% .. +2.61%] · haut q95 +3.11% · bas q05 -4.58%
   - 4h (n=160) : retour [-2.75% .. +2.72%] · haut q95 +3.36% · bas q05 -6.01%
   - 6h (n=160) : retour [-2.77% .. +3.51%] · haut q95 +4.01% · bas q05 -7.45%
   - session (n=160) : retour [-3.8% .. +4.66%] · haut q95 +6.06% · bas q05 -7.45%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.26%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 51.3  _(neutre)_
- **ADX** : 18.7  _(pas de tendance nette)_
- **MACD** : hist -2.503  _(pas de croisement recent)_
- **BB** : %B 0.29 · largeur 19.8%
- **ATR** : 13.28 (100.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.034  _(neutre)_
- **Vol ratio** : 1.17  _(volume normal)_
- **Choppiness** : 55.2  _(transition)_
- **MA** : MA20 231.87 · MA50 231.66 · MA200 231.66  _(prix < MA20)_
- **Dist MA** : MA20 -4.1% · MA50 -4.0% · MA200 -4.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88936 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
