# PLTR

**Generated** : 2026-07-23T00:22:41.066573+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · $124.57  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)  
> ↳ spot $124.57 (+8.7% vs entrée) · entrée $114.56 · stop $112.19 · T1 $119.30 · R/R 2.0  
> ↳ P(T1 av. stop) 30 % · EV/risk -0.056 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $113.61–$115.51 (mid $114.56)
- Spot actuel : $124.57 (+8.7% au-dessus de la zone — repli à attendre)
- Stop : $112.19 (stop swing_plan-based (-9.94%))
- Targets : T1 $119.30 · R/R 2.0 | T2 $124.04 · R/R 4.0 | T3 $128.78 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $112.19


## Edge, scénarios & sizing

- EV/risk : -0.056 | EV/share : $-0.134 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 30 % | T2 16 % | T3 7 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 22.8 | bear 15.9 | side 61.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 125.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.653% → cible +1.851% / stop −5.0%, p_fill 18%, n_eff≈10.5) : P(cible|rempli) **29%** · **EV/risk +0.009** (×p_fill ; si rempli +0.26% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=6, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=6, n_eff=4))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→76% · +2.0%→48% · +3.0%→26% · +5.0%→6% · +8.0%→2%
- Range intraday médian 3.91% (p90 7.33%) · excursion haute méd. +1.9% / basse méd. −1.7%
- Profil de vol intra : ouverture 2.987% vs midi 0.739% vs clôture 0.849% _(ouverture ~4.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 22% · trend ↑0%/↓1% ; spike-down 54% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.122 ; neutre — autocorr 0.022)_ ; drift intra méd. 0.494% ; recovery-V 38%
- **σ réalisé intraday** 2.739% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 57% / bas 44% / whipsaw 10%
- POC intraday (dernière séance, temps-au-prix) : 132.9769 (VA 132.7256–133.7306 ; dernier close 132.61)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 19% · rebond 62% · **stop −2.34%** sous le fill (sous le bruit) · cible +1.4% · R/R 0.6 (high win-rate)
- Gaps overnight (n=159) : méd. -0.31% · baisse 59% (gap-down >1% 32% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.83% (p90 −1.97%) · haut méd +0.96% · range méd 1.88%
- Excursion ouverture 15min (n=160) : bas méd −0.98% (p90 −2.79%) · haut méd +1.17% · range méd 2.3%
- Excursion ouverture 30min (n=160) : bas méd −1.15% (p90 −3.44%) · haut méd +1.31% · range méd 2.74%
- Excursion ouverture 60min (n=160) : bas méd −1.34% (p90 −3.83%) · haut méd +1.47% · range méd 3.05%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 132.61 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 75% (118/159) · gap 43% · délai 0.0min · rebond 54% (63/118) (MFE +1.09%)
   - −1.0% : fill 30min 58% · séance 67% (108/159) · gap 32% · délai 0.0min · rebond 59% (61/108) (MFE +1.29%)
   - −1.5% : fill 30min 49% · séance 60% (93/159) · gap 24% · délai 0.2min · rebond 67% (58/93) (MFE +1.41%)
   - −2.0% : fill 30min 42% · séance 52% (77/159) · gap 16% · délai 1.5min · rebond 64% (48/77) (MFE +1.54%)
   - −3.0% : fill 30min 23% · séance 35% (55/159) · gap 8% · délai 4.2min · rebond 53% (26/55) (MFE +1.13%)
   - −4.0% : fill 30min 17% · séance 25% (41/159) · gap 4% · délai 15.3min · rebond 57% (21/41) (MFE +1.31%)
   - −5.0% : fill 30min 11% · séance 19% (28/159) · gap 2% · délai 25.4min · rebond 62% (15/28) (MFE +1.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −2.06%) → stop au-delà de −1.37% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −2.14%) → stop au-delà de −1.38% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.45% (p90 −1.42%) → stop au-delà de −1.09% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=548 jambes) : jambe baissière méd −1.07% (p90 −2.53%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (73 séances) :
      · −1.0% : fill 91% (68/73) · rebond 62% (41/68)
      · −2.0% : fill 77% (56/73) · rebond 63% (37/56)
      · −3.0% : fill 56% (40/73) · rebond 50% (20/40)
      · −4.0% : fill 43% (31/73) · rebond 56% (16/31)
      · −5.0% : fill 35% (23/73) · rebond 64% (13/23)
   - **flat** (28 séances) :
      · −1.0% : fill 76% (23/28) · rebond 40% (11/23)
      · −2.0% : fill 51% (12/28) · rebond 70% (7/12)
      · −3.0% : fill 40% (10/28) · rebond 75% (5/10)
      · −4.0% : fill 20% (7/28) · rebond 70% (4/7)
      · −5.0% : fill 4% (3/28) · rebond 57% (2/3)
   - **gap-up** (58 séances) :
      · −1.0% : fill 29% (17/58) · rebond 61% (9/17)
      · −2.0% : fill 16% (9/58) · rebond 59% (4/9)
      · −3.0% : fill 4% (5/58) · rebond 15% (1/5)
      · −4.0% : fill 2% (3/58) · rebond 20% (1/3)
      · −5.0% : fill 2% (2/58) · rebond 0% (0/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 55% en base · 68% si les 15 1res min sont vertes (80 cas) · 40% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **49min** → P(séance verte=clôture>ouverture) 81% si début vert vs 26% si rouge (base 55% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **81%** · continue >prix actuel 58% ; creux résiduel méd -0.98% (q20 -2.03%) → **SL/trailing à −2.03%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.49% / q75 +2.52% → **scale +1.49% / runner +2.52%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **26%** (continue à baisser 48%) → **RÉDUIRE ~74%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.43%** (au-delà de la MAE q10 -3.43%), cible rebond +1.39% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.78% .. +3.64%] · haut q95 +3.92% · bas q05 -3.97%
   - 60min (n=160) : retour [-3.55% .. +3.87%] · haut q95 +4.58% · bas q05 -4.43%
   - 2h (n=160) : retour [-3.84% .. +4.68%] · haut q95 +4.8% · bas q05 -4.51%
   - 4h (n=160) : retour [-4.35% .. +5.63%] · haut q95 +5.89% · bas q05 -5.08%
   - 6h (n=160) : retour [-4.94% .. +5.16%] · haut q95 +6.75% · bas q05 -5.53%
   - session (n=160) : retour [-4.67% .. +4.68%] · haut q95 +6.75% · bas q05 -5.52%


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
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 48.5  _(neutre)_
- **ADX** : 12.6  _(pas de tendance nette)_
- **MACD** : hist 0.499  _(pas de croisement recent)_
- **BB** : %B 0.44 · largeur 27.2%
- **ATR** : 6.87 (38.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.054  _(accumulation)_
- **Vol ratio** : 0.91  _(volume normal)_
- **Choppiness** : 67.3  _(marche en range (choppy))_
- **MA** : MA20 126.62 · MA50 132.15 · MA200 154.82  _(prix < MA20)_
- **Dist MA** : MA20 -1.6% · MA50 -5.7% · MA200 -19.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90977 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
