# SRT3

**Generated** : 2026-07-27T00:03:04.084952+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · €221.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot €221.00 (+5.4% vs entrée) · entrée €209.59 · stop €205.83 · T1 €213.21 · R/R 0.96  
> ↳ P(T1 av. stop) 49 % · EV/risk 0.01 · ¼-Kelly 0.007 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.79% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €208.86–€210.31 (mid €209.59)
- Spot actuel : €221.00 (+5.4% au-dessus de la zone — repli à attendre)
- Stop : €205.83 (stop swing_plan-based (-13.08%))
- Targets : T1 €213.21 · R/R 0.96 | T2 €216.84 · R/R 1.93 | T3 €220.47 · R/R 2.89
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €205.83


## Edge, scénarios & sizing

- EV/risk : 0.01 | EV/share : €0.036 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 49 % | T2 21 % | T3 9 %
- Kelly (position) : f* 0.027 | ¼-Kelly 0.007 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.3 | bear 68.2 | side 18.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=5, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→75% · +2.0%→46% · +3.0%→26% · +5.0%→10% · +8.0%→0%
- Range intraday médian 3.65% (p90 7.09%) · excursion haute méd. +1.89% / basse méd. −1.74%
- Profil de vol intra : ouverture 2.169% vs midi 0.903% vs clôture 1.031% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 11% · trend ↑0%/↓0% ; spike-down 53% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.113 ; neutre — autocorr 0.004)_ ; drift intra méd. -0.186% ; recovery-V 29%
- **σ réalisé intraday** 3.003% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 68% / bas 60% / whipsaw 31%
- POC intraday (dernière séance, temps-au-prix) : 216.4156 (VA 214.7969–218.4969 ; dernier close 218.9)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 61% · rebond 73% · **stop −2.59%** sous le fill (sous le bruit) · cible +1.86% · R/R 0.72 (high win-rate)
- Gaps overnight (n=159) : méd. -0.09% · baisse 52% (gap-down >1% 17% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.42% (p90 −2.47%) · haut méd +0.5% · range méd 1.26%
- Excursion ouverture 15min (n=160) : bas méd −0.59% (p90 −2.58%) · haut méd +0.65% · range méd 1.62%
- Excursion ouverture 30min (n=160) : bas méd −0.65% (p90 −2.8%) · haut méd +0.77% · range méd 1.77%
- Excursion ouverture 60min (n=160) : bas méd −0.72% (p90 −2.82%) · haut méd +0.82% · range méd 1.93%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 218.9 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 80% (126/159) · gap 31% · délai 0.2min · rebond 57% (64/126) (MFE +1.19%)
   - −1.0% : fill 30min 49% · séance 67% (106/159) · gap 17% · délai 0.4min · rebond 65% (65/106) (MFE +1.46%)
   - −1.5% : fill 30min 40% · séance 61% (93/159) · gap 8% · délai 3.3min · rebond 73% (61/93) (MFE +1.86%)
   - −2.0% : fill 30min 26% · séance 45% (72/159) · gap 5% · délai 13.3min · rebond 62% (44/72) (MFE +1.68%)
   - −3.0% : fill 30min 8% · séance 23% (41/159) · gap 2% · délai 144.0min · rebond 57% (24/41) (MFE +1.68%)
   - −4.0% : fill 30min 5% · séance 13% (21/159) · gap 1% · délai 49.4min · rebond 76% (16/21) (MFE +2.62%)
   - −5.0% : fill 30min 1% · séance 9% (12/159) · gap 1% · délai 94.0min · rebond 65% (9/12) (MFE +2.48%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.43% (p90 −2.23%) → stop au-delà de −1.42% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.39% (p90 −2.26%) → stop au-delà de −1.42% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.46% (p90 −2.81%) → stop au-delà de −1.46% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=423 jambes) : jambe baissière méd −1.05% (p90 −2.8%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (77 séances) :
      · −1.0% : fill 86% (65/77) · rebond 72% (44/65)
      · −2.0% : fill 56% (43/77) · rebond 65% (28/43)
      · −3.0% : fill 33% (29/77) · rebond 49% (16/29)
      · −4.0% : fill 16% (15/77) · rebond 71% (11/15)
      · −5.0% : fill 8% (7/77) · rebond 92% (6/7)
   - **flat** (33 séances) :
      · −1.0% : fill 60% (18/33) · rebond 43% (8/18)
      · −2.0% : fill 49% (14/33) · rebond 47% (6/14)
      · −3.0% : fill 23% (6/33) · rebond 66% (4/6)
      · −4.0% : fill 18% (4/33) · rebond 70% (3/4)
      · −5.0% : fill 18% (4/33) · rebond 24% (2/4)
   - **gap-up** (49 séances) :
      · −1.0% : fill 50% (23/49) · rebond 67% (13/23)
      · −2.0% : fill 28% (15/49) · rebond 72% (10/15)
      · −3.0% : fill 10% (6/49) · rebond 78% (4/6)
      · −4.0% : fill 6% (2/49) · rebond 100% (2/2)
      · −5.0% : fill 5% (1/49) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 60% si les 15 1res min sont vertes (89 cas) · 40% si rouges (71 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **8min** → P(séance verte=clôture>ouverture) 63% si début vert vs 37% si rouge (base 50% · écart 26 pts) ; prédictivité sature ensuite (plafond brut 268min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=85) : tient le vert **63%** · continue >prix actuel 48% ; creux résiduel méd -1.44% (q20 -2.46%) → **SL/trailing à −2.46%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.36% / q75 +2.74% → **scale +1.36% / runner +2.74%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **37%** (continue à baisser 55%) → **RÉDUIRE ~63%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.31%** (au-delà de la MAE q10 -6.31%), cible rebond +1.67% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.18% .. +2.12%] · haut q95 +2.68% · bas q05 -3.62%
   - 60min (n=160) : retour [-3.41% .. +2.32%] · haut q95 +2.81% · bas q05 -4.13%
   - 2h (n=160) : retour [-2.41% .. +2.63%] · haut q95 +3.11% · bas q05 -4.66%
   - 4h (n=160) : retour [-2.77% .. +2.76%] · haut q95 +3.37% · bas q05 -6.1%
   - 6h (n=160) : retour [-2.79% .. +3.52%] · haut q95 +4.04% · bas q05 -7.5%
   - session (n=160) : retour [-3.81% .. +4.71%] · haut q95 +6.1% · bas q05 -7.5%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.26%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 44.6  _(momentum baissier)_
- **ADX** : 18.3  _(pas de tendance nette)_
- **MACD** : hist -2.379  _(bearish_recent)_
- **BB** : %B 0.22 · largeur 18.3%
- **ATR** : 12.54 (100.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.025  _(neutre)_
- **Vol ratio** : 0.96  _(volume normal)_
- **Choppiness** : 53.0  _(transition)_
- **MA** : MA20 232.71 · MA50 231.64 · MA200 231.63  _(prix < MA20)_
- **Dist MA** : MA20 -5.0% · MA50 -4.6% · MA200 -4.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88687 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
