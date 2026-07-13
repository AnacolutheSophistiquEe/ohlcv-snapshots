# SMR

**Generated** : 2026-07-13T00:31:17.593853+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $9.04  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot $9.04 (+0.4% vs entrée) · entrée $9.00 · stop $8.67 · T1 $9.66 · R/R 2.0  
> ↳ P(T1 av. stop) 13 % _(réel 5 s)_ · EV/risk -0.166 _(réel 5 s)_ (GBM 0.036) · ¼-Kelly 0.037 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.68% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $8.96–$9.04 (mid $9.00)
- Spot actuel : $9.04 (+0.4% au-dessus de la zone — repli à attendre)
- Stop : $8.67 (stop swing_plan-based (-3.8%))
- Targets : T1 $9.66 · R/R 2.0 | T2 $9.70 · R/R 2.12 | T3 $9.74 · R/R 2.24
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $8.67


## Edge, scénarios & sizing

- EV/risk : 0.036 | EV/share : $0.012 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 35 % | T3 35 %
- Kelly (position) : f* 0.149 | ¼-Kelly 0.037 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 34.7 | bear 48.5 | side 16.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.422% → cible +7.367% / stop −3.684%, p_fill 86%, n_eff≈34.6) : P(cible|rempli) **13%** · **EV/risk -0.166** (×p_fill ; si rempli -0.71% du capital)
  - **swing** (entrée dip −0.78% → cible +6.086% / stop −3.044%, p_fill 89%, n_eff≈35.5) : P(cible|rempli) **37%** · **EV/risk +0.035** (×p_fill ; si rempli +0.12% du capital)
  - **deep** (entrée dip −1.114% → cible +8.607% / stop −4.304%, p_fill 81%, n_eff≈33.9) : P(cible|rempli) **22%** · **EV/risk -0.276** (×p_fill ; si rempli -1.47% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→76% · +2.0%→66% · +3.0%→55% · +5.0%→38% · +8.0%→18%
- Range intraday médian 7.26% (p90 12.61%) · excursion haute méd. +3.46% / basse méd. −3.16%
- Profil de vol intra : ouverture 4.952% vs midi 1.549% vs clôture 1.726% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 76% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.11 ; neutre — autocorr 0.023)_ ; drift intra méd. -0.251% ; recovery-V 18%
- **σ réalisé intraday** 4.955% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 59% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 8.9972 (VA 8.8531–9.0527 ; dernier close 9.03)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 61% · rebond 78% · **stop −6.64%** sous le fill (sous le bruit) · cible +3.09% · R/R 0.47 (high win-rate)
- Gaps overnight (n=159) : méd. -0.63% · baisse 59% (gap-down >1% 42% · >2% 29%)
- Excursion ouverture 5min (n=160) : bas méd −1.18% (p90 −3.43%) · haut méd +1.06% · range méd 2.81%
- Excursion ouverture 15min (n=160) : bas méd −1.73% (p90 −3.84%) · haut méd +1.38% · range méd 3.8%
- Excursion ouverture 30min (n=160) : bas méd −1.82% (p90 −5.0%) · haut méd +1.95% · range méd 4.47%
- Excursion ouverture 60min (n=160) : bas méd −2.13% (p90 −6.16%) · haut méd +2.61% · range méd 5.61%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 9.03 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 75% · séance 84% (132/159) · gap 52% · délai 0.0min · rebond 68% (83/132) (MFE +1.75%)
   - −1.0% : fill 30min 69% · séance 79% (126/159) · gap 42% · délai 0.0min · rebond 68% (84/126) (MFE +2.01%)
   - −1.5% : fill 30min 65% · séance 76% (120/159) · gap 38% · délai 0.0min · rebond 76% (88/120) (MFE +2.24%)
   - −2.0% : fill 30min 61% · séance 70% (114/159) · gap 29% · délai 0.2min · rebond 70% (83/114) (MFE +2.73%)
   - −3.0% : fill 30min 48% · séance 61% (102/159) · gap 12% · délai 2.1min · rebond 78% (84/102) (MFE +3.09%)
   - −4.0% : fill 30min 37% · séance 54% (85/159) · gap 6% · délai 9.3min · rebond 75% (66/85) (MFE +2.58%)
   - −5.0% : fill 30min 24% · séance 40% (62/159) · gap 4% · délai 19.5min · rebond 70% (46/62) (MFE +1.87%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.98% (p90 −2.72%) → stop au-delà de −2.05% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.03% (p90 −2.97%) → stop au-delà de −2.15% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.1% (p90 −3.31%) → stop au-delà de −2.2% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1181 jambes) : jambe baissière méd −1.39% (p90 −3.17%) · ~14.5 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (85 séances) :
      · −1.0% : fill 100% (85/85) · rebond 72% (57/85)
      · −2.0% : fill 93% (81/85) · rebond 75% (61/81)
      · −3.0% : fill 84% (77/85) · rebond 83% (65/77)
      · −4.0% : fill 75% (66/85) · rebond 81% (55/66)
      · −5.0% : fill 55% (46/85) · rebond 76% (37/46)
   - **flat** (13 séances) :
      · −1.0% : fill 76% (10/13) · rebond 41% (6/10)
      · −2.0% : fill 63% (8/13) · rebond 29% (4/8)
      · −3.0% : fill 59% (6/13) · rebond 27% (3/6)
      · −4.0% : fill 59% (6/13) · rebond 38% (2/6)
      · −5.0% : fill 47% (5/13) · rebond 70% (4/5)
   - **gap-up** (61 séances) :
      · −1.0% : fill 50% (31/61) · rebond 67% (21/31)
      · −2.0% : fill 40% (25/61) · rebond 67% (18/25)
      · −3.0% : fill 30% (19/61) · rebond 80% (16/19)
      · −4.0% : fill 22% (13/61) · rebond 67% (9/13)
      · −5.0% : fill 16% (11/61) · rebond 41% (5/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 56% si les 15 1res min sont vertes (69 cas) · 32% si rouges (91 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:25** → P(séance verte=clôture>ouverture) 76% si début vert vs 12% si rouge (base 43% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 233min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **76%** · continue >prix actuel 47% ; creux résiduel méd -2.34% (q20 -3.82%) → **SL/trailing à −3.82%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.21% / q75 +4.21% → **scale +2.21% / runner +4.21%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **12%** (continue à baisser 54%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.04%** (au-delà de la MAE q10 -6.04%), cible rebond +1.72% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.61% .. +4.91%] · haut q95 +6.59% · bas q05 -6.37%
   - 60min (n=160) : retour [-6.83% .. +5.71%] · haut q95 +7.98% · bas q05 -7.93%
   - 2h (n=160) : retour [-7.9% .. +8.46%] · haut q95 +11.34% · bas q05 -8.93%
   - 4h (n=160) : retour [-8.71% .. +8.24%] · haut q95 +11.34% · bas q05 -10.72%
   - 6h (n=160) : retour [-8.43% .. +8.76%] · haut q95 +11.55% · bas q05 -10.73%
   - session (n=160) : retour [-8.32% .. +10.78%] · haut q95 +11.74% · bas q05 -10.79%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 4.98%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 15.2  _(survente)_
- **ADX** : 14.7  _(pas de tendance nette)_
- **MACD** : hist -0.101  _(pas de croisement recent)_
- **BB** : %B 0.18 · largeur 30.2%
- **ATR** : 0.74 (6.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.105  _(distribution)_
- **Vol ratio** : 0.8  _(volume normal)_
- **Choppiness** : 43.3  _(transition)_
- **MA** : MA20 10.01 · MA50 11.08 · MA200 18.77  _(prix < MA20)_
- **Dist MA** : MA20 -9.7% · MA50 -18.4% · MA200 -51.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83439 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
