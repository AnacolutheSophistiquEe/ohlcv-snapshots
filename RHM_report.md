# RHM

**Generated** : 2026-07-27T21:36:04.692068+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €1050.60  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot €1050.60 (+2.9% vs entrée) · entrée €1021.08 · stop €1000.65 · T1 €1036.92 · R/R 0.78  
> ↳ P(T1 av. stop) 52 % · EV/risk -0.004 · ¼-Kelly 0.011 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €1017.91–€1024.24 (mid €1021.08)
- Spot actuel : €1050.60 (+2.9% au-dessus de la zone — repli à attendre)
- Stop : €1000.65 (stop swing_plan-based (-7.81%))
- Targets : T1 €1036.92 · R/R 0.78 | T2 €1052.77 · R/R 1.55 | T3 €1068.62 · R/R 2.33
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €1000.65


## Edge, scénarios & sizing

- EV/risk : -0.004 | EV/share : €-0.076 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 25 % | T3 4 %
- Kelly (position) : f* 0.042 | ¼-Kelly 0.011 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 77.4 | bear 5.0 | side 17.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.806% → cible +1.552% / stop −2.0%, p_fill 25%, n_eff≈11.7) : P(cible|rempli) **36%** · **EV/risk -0.049** (×p_fill ; si rempli -0.40% du capital)
  - **swing** (entrée dip −6.182% → cible +3.47% / stop −1.735%, p_fill 19%, n_eff≈8.7) : P(cible|rempli) **2%** · **EV/risk -0.186** (×p_fill ; si rempli -1.67% du capital)
  - **deep** (entrée dip −9.55% → cible +4.908% / stop −2.454%, p_fill 27%, n_eff≈9.6) : P(cible|rempli) **7%** · **EV/risk -0.187** (×p_fill ; si rempli -1.68% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→62% · +2.0%→46% · +3.0%→26% · +5.0%→1% · +8.0%→0%
- Range intraday médian 3.99% (p90 6.65%) · excursion haute méd. +1.72% / basse méd. −1.72%
- Profil de vol intra : ouverture 2.493% vs midi 0.847% vs clôture 1.08% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 52% · recovery-V 40%)_
- **Régime intraday** : **chop** _(efficiency 0.094 ; neutre — autocorr -0.025)_ ; drift intra méd. -0.192% ; recovery-V 45%
- **σ réalisé intraday** 2.703% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 75% / bas 60% / whipsaw 36%
- POC intraday (dernière séance, temps-au-prix) : 1030.81 (VA 1028.71–1033.33 ; dernier close 1035.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 22% · rebond 61% · **stop −3.14%** sous le fill (sous le bruit) · cible +1.45% · R/R 0.46 (high win-rate)
- Gaps overnight (n=159) : méd. 0.09% · baisse 42% (gap-down >1% 12% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.7% (p90 −1.73%) · haut méd +0.59% · range méd 1.38%
- Excursion ouverture 15min (n=160) : bas méd −0.95% (p90 −1.99%) · haut méd +0.67% · range méd 1.86%
- Excursion ouverture 30min (n=160) : bas méd −0.99% (p90 −2.5%) · haut méd +0.87% · range méd 2.13%
- Excursion ouverture 60min (n=160) : bas méd −1.08% (p90 −2.67%) · haut méd +1.0% · range méd 2.25%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1035.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 77% (121/159) · gap 28% · délai 0.3min · rebond 59% (64/121) (MFE +1.34%)
   - −1.0% : fill 30min 48% · séance 68% (109/159) · gap 12% · délai 4.3min · rebond 62% (64/109) (MFE +1.4%)
   - −1.5% : fill 30min 31% · séance 54% (81/159) · gap 6% · délai 18.0min · rebond 51% (42/81) (MFE +1.14%)
   - −2.0% : fill 30min 21% · séance 44% (70/159) · gap 5% · délai 30.3min · rebond 61% (42/70) (MFE +1.31%)
   - −3.0% : fill 30min 10% · séance 30% (46/159) · gap 3% · délai 119.2min · rebond 60% (28/46) (MFE +1.31%)
   - −4.0% : fill 30min 5% · séance 22% (28/159) · gap 2% · délai 152.6min · rebond 61% (16/28) (MFE +1.45%)
   - −5.0% : fill 30min 2% · séance 11% (16/159) · gap 1% · délai 206.9min · rebond 48% (8/16) (MFE +0.74%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.67% (p90 −1.65%) → stop au-delà de −1.23% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.57% (p90 −1.74%) → stop au-delà de −1.41% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.3% (p90 −1.75%) → stop au-delà de −1.57% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=464 jambes) : jambe baissière méd −1.06% (p90 −2.53%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (52 séances) :
      · −1.0% : fill 94% (50/52) · rebond 62% (28/50)
      · −2.0% : fill 77% (39/52) · rebond 63% (25/39)
      · −3.0% : fill 50% (27/52) · rebond 59% (17/27)
      · −4.0% : fill 36% (16/52) · rebond 71% (11/16)
      · −5.0% : fill 17% (9/52) · rebond 77% (7/9)
   - **flat** (50 séances) :
      · −1.0% : fill 67% (36/50) · rebond 69% (24/36)
      · −2.0% : fill 28% (17/50) · rebond 72% (10/17)
      · −3.0% : fill 19% (10/50) · rebond 55% (5/10)
      · −4.0% : fill 17% (8/50) · rebond 36% (2/8)
      · −5.0% : fill 11% (6/50) · rebond 22% (1/6)
   - **gap-up** (57 séances) :
      · −1.0% : fill 44% (23/57) · rebond 49% (12/23)
      · −2.0% : fill 26% (14/57) · rebond 46% (7/14)
      · −3.0% : fill 20% (9/57) · rebond 66% (6/9)
      · −4.0% : fill 11% (4/57) · rebond 61% (3/4)
      · −5.0% : fill 4% (1/57) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 53% en base · 70% si les 15 1res min sont vertes (83 cas) · 38% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 78% si début vert vs 30% si rouge (base 53% · écart 48 pts) ; prédictivité sature ensuite (plafond brut 225min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **78%** · continue >prix actuel 51% ; creux résiduel méd -1.24% (q20 -2.16%) → **SL/trailing à −2.16%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.32% / q75 +1.89% → **scale +1.32% / runner +1.89%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **30%** (continue à baisser 52%) → **RÉDUIRE ~70%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.95%** (au-delà de la MAE q10 -4.95%), cible rebond +1.19% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.65% .. +3.04%] · haut q95 +3.75% · bas q05 -3.13%
   - 60min (n=160) : retour [-3.28% .. +3.02%] · haut q95 +3.92% · bas q05 -3.89%
   - 2h (n=160) : retour [-3.54% .. +2.78%] · haut q95 +4.05% · bas q05 -4.5%
   - 4h (n=160) : retour [-3.58% .. +2.9%] · haut q95 +4.42% · bas q05 -5.04%
   - 6h (n=160) : retour [-4.58% .. +3.1%] · haut q95 +4.53% · bas q05 -5.7%
   - session (n=160) : retour [-6.17% .. +4.14%] · haut q95 +4.74% · bas q05 -6.64%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.28%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 37.1  _(momentum baissier)_
- **ADX** : 24.5  _(pas de tendance nette)_
- **MACD** : hist 11.769  _(pas de croisement recent)_
- **BB** : %B 0.62 · largeur 20.1%
- **ATR** : 42.35 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.099  _(accumulation)_
- **Vol ratio** : 0.87  _(volume normal)_
- **Choppiness** : 44.2  _(transition)_
- **MA** : MA20 1026.86 · MA50 1115.02 · MA200 1473.43  _(prix > MA20)_
- **Dist MA** : MA20 +2.3% · MA50 -5.8% · MA200 -28.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90440 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
