# RHM

**Generated** : 2026-07-22T21:36:06.160265+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €1007.80  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot €1007.80 (+1.9% vs entrée) · entrée €988.98 · stop €969.20 · T1 €1004.39 · R/R 0.78  
> ↳ P(T1 av. stop) 30 % _(réel 5 s)_ · EV/risk -0.155 _(réel 5 s)_ (GBM 0.014) · ¼-Kelly 0.013 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €985.89–€992.06 (mid €988.98)
- Spot actuel : €1007.80 (+1.9% au-dessus de la zone — repli à attendre)
- Stop : €969.20 (stop swing_plan-based (-5.78%))
- Targets : T1 €1004.39 · R/R 0.78 | T2 €1019.81 · R/R 1.56 | T3 €1035.23 · R/R 2.34
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €969.20


## Edge, scénarios & sizing

- EV/risk : 0.014 | EV/share : €0.274 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 53 % | T2 27 % | T3 5 %
- Kelly (position) : f* 0.054 | ¼-Kelly 0.013 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 24.0 | bear 5.0 | side 71.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.867% → cible +1.559% / stop −2.0%, p_fill 47%, n_eff≈18.4) : P(cible|rempli) **30%** · **EV/risk -0.155** (×p_fill ; si rempli -0.66% du capital)
  - **swing** (entrée dip −4.108% → cible +3.486% / stop −1.743%, p_fill 42%, n_eff≈15.0) : P(cible|rempli) **35%** · **EV/risk -0.021** (×p_fill ; si rempli -0.09% du capital)
  - **deep** (entrée dip −6.351% → cible +4.93% / stop −2.465%, p_fill 35%, n_eff≈12.1) : P(cible|rempli) **10%** · **EV/risk -0.252** (×p_fill ; si rempli -1.77% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→64% · +2.0%→48% · +3.0%→29% · +5.0%→2% · +8.0%→0%
- Range intraday médian 4.12% (p90 6.86%) · excursion haute méd. +1.85% / basse méd. −1.72%
- Profil de vol intra : ouverture 2.542% vs midi 0.851% vs clôture 1.087% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 55% · recovery-V 40%)_
- **Régime intraday** : **chop** _(efficiency 0.102 ; neutre — autocorr -0.009)_ ; drift intra méd. -0.308% ; recovery-V 45%
- **σ réalisé intraday** 2.803% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 72% / bas 69% / whipsaw 41%
- POC intraday (dernière séance, temps-au-prix) : 1007.5688 (VA 995.5312–1009.9763 ; dernier close 997.7)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 23% · rebond 61% · **stop −3.14%** sous le fill (sous le bruit) · cible +1.45% · R/R 0.46 (high win-rate)
- Gaps overnight (n=159) : méd. 0.04% · baisse 45% (gap-down >1% 13% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.81% (p90 −1.75%) · haut méd +0.56% · range méd 1.42%
- Excursion ouverture 15min (n=160) : bas méd −0.98% (p90 −2.01%) · haut méd +0.72% · range méd 1.95%
- Excursion ouverture 30min (n=160) : bas méd −1.07% (p90 −2.75%) · haut méd +0.85% · range méd 2.18%
- Excursion ouverture 60min (n=160) : bas méd −1.12% (p90 −2.99%) · haut méd +1.01% · range méd 2.34%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 997.7 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 80% (123/159) · gap 30% · délai 0.2min · rebond 58% (65/123) (MFE +1.28%)
   - −1.0% : fill 30min 50% · séance 72% (110/159) · gap 13% · délai 4.2min · rebond 62% (64/110) (MFE +1.4%)
   - −1.5% : fill 30min 32% · séance 56% (82/159) · gap 7% · délai 17.8min · rebond 51% (42/82) (MFE +1.14%)
   - −2.0% : fill 30min 23% · séance 47% (71/159) · gap 5% · délai 30.1min · rebond 61% (42/71) (MFE +1.31%)
   - −3.0% : fill 30min 10% · séance 32% (47/159) · gap 3% · délai 119.0min · rebond 60% (29/47) (MFE +1.31%)
   - −4.0% : fill 30min 5% · séance 23% (28/159) · gap 2% · délai 152.6min · rebond 61% (16/28) (MFE +1.45%)
   - −5.0% : fill 30min 2% · séance 11% (16/159) · gap 1% · délai 206.9min · rebond 48% (8/16) (MFE +0.74%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.67% (p90 −1.67%) → stop au-delà de −1.25% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.57% (p90 −1.76%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.33% (p90 −1.77%) → stop au-delà de −1.59% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=461 jambes) : jambe baissière méd −1.07% (p90 −2.56%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (53 séances) :
      · −1.0% : fill 94% (51/53) · rebond 62% (28/51)
      · −2.0% : fill 77% (40/53) · rebond 63% (25/40)
      · −3.0% : fill 50% (28/53) · rebond 59% (18/28)
      · −4.0% : fill 36% (16/53) · rebond 71% (11/16)
      · −5.0% : fill 17% (9/53) · rebond 77% (7/9)
   - **flat** (51 séances) :
      · −1.0% : fill 71% (36/51) · rebond 69% (24/36)
      · −2.0% : fill 30% (17/51) · rebond 72% (10/17)
      · −3.0% : fill 20% (10/51) · rebond 55% (5/10)
      · −4.0% : fill 18% (8/51) · rebond 36% (2/8)
      · −5.0% : fill 12% (6/51) · rebond 22% (1/6)
   - **gap-up** (55 séances) :
      · −1.0% : fill 48% (23/55) · rebond 49% (12/23)
      · −2.0% : fill 29% (14/55) · rebond 46% (7/14)
      · −3.0% : fill 23% (9/55) · rebond 66% (6/9)
      · −4.0% : fill 12% (4/55) · rebond 61% (3/4)
      · −5.0% : fill 5% (1/55) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 68% si les 15 1res min sont vertes (84 cas) · 33% si rouges (76 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 76% si début vert vs 27% si rouge (base 50% · écart 49 pts) ; prédictivité sature ensuite (plafond brut 295min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **76%** · continue >prix actuel 47% ; creux résiduel méd -1.27% (q20 -2.36%) → **SL/trailing à −2.36%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.2% / q75 +1.88% → **scale +1.2% / runner +1.88%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **27%** (continue à baisser 53%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.97%** (au-delà de la MAE q10 -4.97%), cible rebond +1.16% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.65% .. +3.09%] · haut q95 +3.77% · bas q05 -3.19%
   - 60min (n=160) : retour [-3.39% .. +3.08%] · haut q95 +3.97% · bas q05 -4.0%
   - 2h (n=160) : retour [-3.59% .. +2.8%] · haut q95 +4.09% · bas q05 -4.62%
   - 4h (n=160) : retour [-3.73% .. +2.97%] · haut q95 +4.47% · bas q05 -5.07%
   - 6h (n=160) : retour [-4.71% .. +3.22%] · haut q95 +4.53% · bas q05 -5.74%
   - session (n=160) : retour [-6.18% .. +4.17%] · haut q95 +4.74% · bas q05 -6.72%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.29%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 30.1  _(momentum baissier)_
- **ADX** : 28.3  _(tendance etablie)_
- **MACD** : hist 4.279  _(bullish_recent)_
- **BB** : %B 0.47 · largeur 22.6%
- **ATR** : 43.66 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.189  _(accumulation)_
- **Vol ratio** : 0.56  _(volume atone)_
- **Choppiness** : 40.5  _(transition)_
- **MA** : MA20 1014.92 · MA50 1121.62 · MA200 1486.15  _(prix < MA20)_
- **Dist MA** : MA20 -0.7% · MA50 -10.1% · MA200 -32.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90970 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
