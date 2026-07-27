# PRY

**Generated** : 2026-07-27T00:11:13.697195+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · €126.90  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot €126.90 (+0.7% vs entrée) · entrée €125.97 · stop €115.90 · T1 €127.83 · R/R 0.18  
> ↳ P(T1 av. stop) 37 % _(réel 5 s)_ · EV/risk -0.068 _(réel 5 s)_ (GBM -0.02) · ¼-Kelly 0.092 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -30 % hors [0,100] (R² max 0.86). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €125.60–€126.35 (mid €125.97)
- Spot actuel : €126.90 (+0.7% au-dessus de la zone — repli à attendre)
- Stop : €115.90 (stop swing_plan-based (-3.22%))
- Targets : T1 €127.83 · R/R 0.18 | T2 €129.68 · R/R 0.37 | T3 €131.54 · R/R 0.55
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €115.90


## Edge, scénarios & sizing

- EV/risk : -0.02 | EV/share : €-0.203 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 51 % | T2 29 % | T3 12 %
- Kelly (position) : f* 0.367 | ¼-Kelly 0.092 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 46.7 | bear 27.7 | side 25.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 127.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.728% → cible +1.472% / stop −8.0%, p_fill 75%, n_eff≈29.8) : P(cible|rempli) **37%** · **EV/risk -0.068** (×p_fill ; si rempli -0.72% du capital)
  - **swing** (entrée dip −1.601% → cible +3.291% / stop −1.645%, p_fill 64%, n_eff≈25.1) : P(cible|rempli) **28%** · **EV/risk -0.160** (×p_fill ; si rempli -0.41% du capital)
  - **deep** (entrée dip −2.481% → cible +4.654% / stop −2.327%, p_fill 69%, n_eff≈26.4) : P(cible|rempli) **32%** · **EV/risk -0.059** (×p_fill ; si rempli -0.20% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→65% · +2.0%→40% · +3.0%→29% · +5.0%→9% · +8.0%→4%
- Range intraday médian 3.88% (p90 6.32%) · excursion haute méd. +1.5% / basse méd. −1.58%
- Profil de vol intra : ouverture 2.274% vs midi 0.796% vs clôture 1.133% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (140 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 54% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; neutre — autocorr -0.006)_ ; drift intra méd. -0.48% ; recovery-V 18%
- **σ réalisé intraday** 2.603% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 63% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 127.7415 (VA 126.3765–128.0145 ; dernier close 126.56)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 21% · rebond 66% · **stop −2.71%** sous le fill (sous le bruit) · cible +1.36% · R/R 0.5 (high win-rate)
- Gaps overnight (n=139) : méd. 0.2% · baisse 42% (gap-down >1% 20% · >2% 12%)
- Excursion ouverture 5min (n=140) : bas méd −0.68% (p90 −2.09%) · haut méd +0.53% · range méd 1.38%
- Excursion ouverture 15min (n=140) : bas méd −0.91% (p90 −2.43%) · haut méd +0.67% · range méd 1.71%
- Excursion ouverture 30min (n=140) : bas méd −0.94% (p90 −2.94%) · haut méd +0.84% · range méd 1.86%
- Excursion ouverture 60min (n=140) : bas méd −1.15% (p90 −3.17%) · haut méd +0.89% · range méd 2.1%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 126.56 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 71% (101/139) · gap 28% · délai 0.2min · rebond 60% (63/101) (MFE +1.18%)
   - −1.0% : fill 30min 50% · séance 62% (85/139) · gap 20% · délai 0.3min · rebond 55% (50/85) (MFE +1.46%)
   - −1.5% : fill 30min 34% · séance 52% (73/139) · gap 17% · délai 1.6min · rebond 48% (39/73) (MFE +0.88%)
   - −2.0% : fill 30min 24% · séance 44% (59/139) · gap 12% · délai 4.3min · rebond 54% (36/59) (MFE +1.2%)
   - −3.0% : fill 30min 14% · séance 34% (43/139) · gap 4% · délai 76.8min · rebond 63% (29/43) (MFE +1.58%)
   - −4.0% : fill 30min 4% · séance 21% (23/139) · gap 2% · délai 182.8min · rebond 66% (16/23) (MFE +1.36%)
   - −5.0% : fill 30min 2% · séance 12% (15/139) · gap 1% · délai 332.6min · rebond 84% (12/15) (MFE +1.58%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.28% (p90 −1.61%) → stop au-delà de −1.39% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.22% (p90 −1.6%) → stop au-delà de −1.05% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.09% (p90 −1.56%) → stop au-delà de −1.02% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=423 jambes) : jambe baissière méd −1.07% (p90 −2.47%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 89% (45/50) · rebond 46% (25/45)
      · −2.0% : fill 70% (36/50) · rebond 59% (24/36)
      · −3.0% : fill 61% (28/50) · rebond 69% (21/28)
      · −4.0% : fill 37% (15/50) · rebond 60% (10/15)
      · −5.0% : fill 26% (11/50) · rebond 89% (9/11)
   - **flat** (26 séances) :
      · −1.0% : fill 65% (14/26) · rebond 66% (9/14)
      · −2.0% : fill 38% (7/26) · rebond 82% (5/7)
      · −3.0% : fill 25% (5/26) · rebond 40% (2/5)
      · −4.0% : fill 12% (3/26) · rebond 59% (2/3)
      · −5.0% : fill 6% (2/26) · rebond 25% (1/2)
   - **gap-up** (63 séances) :
      · −1.0% : fill 41% (26/63) · rebond 62% (16/26)
      · −2.0% : fill 25% (16/63) · rebond 30% (7/16)
      · −3.0% : fill 17% (10/63) · rebond 59% (6/10)
      · −4.0% : fill 12% (5/63) · rebond 81% (4/5)
      · −5.0% : fill 3% (2/63) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=140) : 50% en base · 78% si les 15 1res min sont vertes (65 cas) · 27% si rouges (75 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=140) : COUDE à **1:10** → P(séance verte=clôture>ouverture) 86% si début vert vs 21% si rouge (base 50% · écart 65 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=65) : tient le vert **86%** · continue >prix actuel 65% ; creux résiduel méd -1.29% (q20 -2.05%) → **SL/trailing à −2.05%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.4% / q75 +2.6% → **scale +1.4% / runner +2.6%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **21%** (continue à baisser 66%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.78%** (au-delà de la MAE q10 -3.78%), cible rebond +1.13% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=140) : retour [-2.85% .. +2.69%] · haut q95 +3.44% · bas q05 -3.35%
   - 60min (n=140) : retour [-2.91% .. +2.33%] · haut q95 +3.91% · bas q05 -3.48%
   - 2h (n=140) : retour [-3.58% .. +3.35%] · haut q95 +4.11% · bas q05 -3.69%
   - 4h (n=140) : retour [-3.46% .. +3.64%] · haut q95 +4.53% · bas q05 -4.45%
   - 6h (n=140) : retour [-3.71% .. +3.75%] · haut q95 +4.93% · bas q05 -4.63%
   - session (n=140) : retour [-4.32% .. +4.78%] · haut q95 +5.97% · bas q05 -5.53%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 5.0% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.4%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 31.5  _(momentum baissier)_
- **ADX** : 27.9  _(tendance etablie)_
- **MACD** : hist -0.809  _(pas de croisement recent)_
- **BB** : %B 0.21 · largeur 21.1%
- **ATR** : 5.63 (79.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.131  _(distribution)_
- **Vol ratio** : 0.74  _(volume normal)_
- **Choppiness** : 54.5  _(transition)_
- **MA** : MA20 135.16 · MA50 142.64 · MA200 109.66  _(prix < MA20)_
- **Dist MA** : MA20 -6.1% · MA50 -11.0% · MA200 +15.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93676 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
