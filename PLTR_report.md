# PLTR

**Generated** : 2026-07-24T21:59:59.645934+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $122.92  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot $122.92 (+3.5% vs entrée) · entrée $118.78 · stop $115.81 · T1 $120.73 · R/R 0.66  
> ↳ P(T1 av. stop) 55 % · EV/risk -0.006 · ¼-Kelly 0.014 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $118.39–$119.17 (mid $118.78)
- Spot actuel : $122.92 (+3.5% au-dessus de la zone — repli à attendre)
- Stop : $115.81 (stop swing_plan-based (-9.11%))
- Targets : T1 $120.73 · R/R 0.66 | T2 $122.69 · R/R 1.32 | T3 $124.64 · R/R 1.97
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $115.81


## Edge, scénarios & sizing

- EV/risk : -0.006 | EV/share : $-0.019 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 55 % | T2 19 % | T3 6 %
- Kelly (position) : f* 0.058 | ¼-Kelly 0.014 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.9 | bear 10.9 | side 75.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.364% → cible +1.644% / stop −2.5%, p_fill 23%, n_eff≈10.4) : P(cible|rempli) **29%** · **EV/risk -0.035** (×p_fill ; si rempli -0.38% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=9, n_eff=5))
  - **deep** : indisponible (échantillon insuffisant (n=8, n_eff=5))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→76% · +2.0%→48% · +3.0%→26% · +5.0%→6% · +8.0%→2%
- Range intraday médian 3.94% (p90 7.33%) · excursion haute méd. +1.9% / basse méd. −1.7%
- Profil de vol intra : ouverture 3.009% vs midi 0.741% vs clôture 0.849% _(ouverture ~4.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 76% · range 23% · trend ↑0%/↓1% ; spike-down 55% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; neutre — autocorr 0.019)_ ; drift intra méd. 0.199% ; recovery-V 36%
- **σ réalisé intraday** 2.743% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 47% / whipsaw 10%
- POC intraday (dernière séance, temps-au-prix) : 126.7719 (VA 124.1224–128.6644 ; dernier close 124.58)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 20% · rebond 56% · **stop −2.33%** sous le fill (sous le bruit) · cible +1.29% · R/R 0.55 (high win-rate)
- Gaps overnight (n=159) : méd. -0.28% · baisse 59% (gap-down >1% 31% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.84% (p90 −1.98%) · haut méd +0.94% · range méd 1.93%
- Excursion ouverture 15min (n=160) : bas méd −0.99% (p90 −2.83%) · haut méd +1.17% · range méd 2.31%
- Excursion ouverture 30min (n=160) : bas méd −1.17% (p90 −3.49%) · haut méd +1.26% · range méd 2.81%
- Excursion ouverture 60min (n=160) : bas méd −1.37% (p90 −4.0%) · haut méd +1.43% · range méd 3.11%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 124.58 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 75% (118/159) · gap 42% · délai 0.0min · rebond 52% (63/118) (MFE +1.07%)
   - −1.0% : fill 30min 58% · séance 67% (108/159) · gap 31% · délai 0.0min · rebond 57% (60/108) (MFE +1.27%)
   - −1.5% : fill 30min 50% · séance 60% (93/159) · gap 24% · délai 0.1min · rebond 68% (58/93) (MFE +1.38%)
   - −2.0% : fill 30min 43% · séance 52% (77/159) · gap 16% · délai 1.3min · rebond 61% (47/77) (MFE +1.43%)
   - −3.0% : fill 30min 24% · séance 36% (55/159) · gap 8% · délai 5.8min · rebond 50% (25/55) (MFE +1.0%)
   - −4.0% : fill 30min 18% · séance 27% (41/159) · gap 4% · délai 15.5min · rebond 59% (21/41) (MFE +1.09%)
   - −5.0% : fill 30min 11% · séance 20% (29/159) · gap 2% · délai 26.5min · rebond 56% (15/29) (MFE +1.29%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −2.06%) → stop au-delà de −1.37% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −2.14%) → stop au-delà de −1.38% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.45% (p90 −1.42%) → stop au-delà de −1.09% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=549 jambes) : jambe baissière méd −1.07% (p90 −2.54%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (72 séances) :
      · −1.0% : fill 91% (67/72) · rebond 62% (40/67)
      · −2.0% : fill 77% (55/72) · rebond 63% (36/55)
      · −3.0% : fill 56% (39/72) · rebond 50% (19/39)
      · −4.0% : fill 43% (30/72) · rebond 56% (15/30)
      · −5.0% : fill 35% (23/72) · rebond 64% (13/23)
   - **flat** (29 séances) :
      · −1.0% : fill 79% (24/29) · rebond 34% (11/24)
      · −2.0% : fill 57% (13/29) · rebond 56% (7/13)
      · −3.0% : fill 47% (11/29) · rebond 56% (5/11)
      · −4.0% : fill 29% (8/29) · rebond 82% (5/8)
      · −5.0% : fill 15% (4/29) · rebond 14% (2/4)
   - **gap-up** (58 séances) :
      · −1.0% : fill 29% (17/58) · rebond 61% (9/17)
      · −2.0% : fill 16% (9/58) · rebond 59% (4/9)
      · −3.0% : fill 4% (5/58) · rebond 15% (1/5)
      · −4.0% : fill 2% (3/58) · rebond 20% (1/3)
      · −5.0% : fill 2% (2/58) · rebond 0% (0/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 53% en base · 68% si les 15 1res min sont vertes (79 cas) · 39% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **49min** → P(séance verte=clôture>ouverture) 81% si début vert vs 25% si rouge (base 53% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **81%** · continue >prix actuel 58% ; creux résiduel méd -0.98% (q20 -2.03%) → **SL/trailing à −2.03%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.48% / q75 +2.52% → **scale +1.48% / runner +2.52%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **25%** (continue à baisser 50%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.36%** (au-delà de la MAE q10 -3.36%), cible rebond +1.36% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.76% .. +3.62%] · haut q95 +3.91% · bas q05 -4.07%
   - 60min (n=160) : retour [-3.67% .. +3.87%] · haut q95 +4.56% · bas q05 -4.42%
   - 2h (n=160) : retour [-4.12% .. +4.62%] · haut q95 +4.79% · bas q05 -4.61%
   - 4h (n=160) : retour [-4.59% .. +5.63%] · haut q95 +5.83% · bas q05 -5.6%
   - 6h (n=160) : retour [-5.27% .. +5.11%] · haut q95 +6.74% · bas q05 -5.94%
   - session (n=160) : retour [-4.99% .. +4.67%] · haut q95 +6.74% · bas q05 -5.96%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 2.5% / strong 2.5%) · base = 8 séances trend-up (n_eff 6.2)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **28%**. Lecture précoce 30 min : signature présente → 14% vs absente 2% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.76% (p75 0.9% / p90 1.61%) · ~3.0 replis/séance, durée méd 72.55 min. P(nouveau plus-haut après repli) :
   - −0.5% → **83%** (reprise méd 21.18 min, n=27)
   - −1.0% → **27%** (reprise méd None min, n=6)
   - −1.5% → **36%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.61%** (p90, défaut prudent ; serré/agressif −0.9%) ; extension open→close méd +4.43% (q75 +5.23% / q95 +7.65%), MFE méd +5.49% / q90 +8.71%
   - Échelle scale-out : +5.49% (33%) / +7.2% (33%) / +8.71% (34%)
- **DÉSARMER** : repli > **−1.61%** depuis le plus-haut = décay → P(retournement) **21%** (préavis méd 195.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +8.71% : P(retournement après) 0% (mèche méd 1.24%)
- **CONTEXTE** : la dernière heure tient les gains 71% du temps (retour médian dernière heure +0.2%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 35.7  _(momentum baissier)_
- **ADX** : 13.1  _(pas de tendance nette)_
- **MACD** : hist -0.434  _(bearish_recent)_
- **BB** : %B 0.31 · largeur 21.0%
- **ATR** : 6.47 (20.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.131  _(accumulation)_
- **Vol ratio** : 0.53  _(volume atone)_
- **Choppiness** : 60.9  _(transition)_
- **MA** : MA20 127.9 · MA50 131.61 · MA200 154.29  _(prix < MA20)_
- **Dist MA** : MA20 -3.9% · MA50 -6.6% · MA200 -20.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88100 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
