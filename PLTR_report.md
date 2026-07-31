# PLTR

**Generated** : 2026-07-31T00:22:48.128706+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $122.26  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $122.26 (+3.4% vs entrée) · entrée $118.29 · stop $115.33 · T1 $120.26 · R/R 0.67  
> ↳ P(T1 av. stop) 37 % _(réel 5 s)_ · EV/risk -0.028 _(réel 5 s)_ (GBM 0.006) · ¼-Kelly 0.016 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $117.89–$118.68 (mid $118.29)
- Spot actuel : $122.26 (+3.4% au-dessus de la zone — repli à attendre)
- Stop : $115.33 (stop swing_plan-based (-8.88%))
- Targets : T1 $120.26 · R/R 0.67 | T2 $122.24 · R/R 1.33 | T3 $124.22 · R/R 2.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $115.33


## Edge, scénarios & sizing

- EV/risk : 0.006 | EV/share : $0.019 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 56 % | T2 19 % | T3 6 %
- Kelly (position) : f* 0.063 | ¼-Kelly 0.016 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 31.0 | bear 56.6 | side 12.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.251% → cible +1.671% / stop −2.5%, p_fill 32%, n_eff≈12.9) : P(cible|rempli) **37%** · **EV/risk -0.028** (×p_fill ; si rempli -0.22% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=11, n_eff=5))
  - **deep** : indisponible (échantillon insuffisant (n=10, n_eff=7))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→76% · +2.0%→48% · +3.0%→25% · +5.0%→6% · +8.0%→2%
- Range intraday médian 3.94% (p90 6.99%) · excursion haute méd. +1.9% / basse méd. −1.7%
- Profil de vol intra : ouverture 3.016% vs midi 0.737% vs clôture 0.867% _(ouverture ~4.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 23% · trend ↑0%/↓1% ; spike-down 55% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; momentum — autocorr 0.04)_ ; drift intra méd. 0.067% ; recovery-V 27%
- **σ réalisé intraday** 2.797% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 46% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 124.8303 (VA 123.7548–125.6668 ; dernier close 123.05)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 20% · rebond 51% · **stop −3.07%** sous le fill (sous le bruit) · cible +1.01% · R/R 0.33 (high win-rate)
- Gaps overnight (n=159) : méd. -0.14% · baisse 56% (gap-down >1% 30% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.88% (p90 −2.1%) · haut méd +0.95% · range méd 1.92%
- Excursion ouverture 15min (n=160) : bas méd −1.04% (p90 −3.02%) · haut méd +1.16% · range méd 2.35%
- Excursion ouverture 30min (n=160) : bas méd −1.22% (p90 −3.63%) · haut méd +1.18% · range méd 2.75%
- Excursion ouverture 60min (n=160) : bas méd −1.37% (p90 −4.08%) · haut méd +1.35% · range méd 3.05%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 123.05 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 75% (118/159) · gap 40% · délai 0.0min · rebond 52% (64/118) (MFE +1.07%)
   - −1.0% : fill 30min 58% · séance 67% (107/159) · gap 30% · délai 0.0min · rebond 58% (61/107) (MFE +1.25%)
   - −1.5% : fill 30min 49% · séance 58% (92/159) · gap 24% · délai 0.1min · rebond 67% (57/92) (MFE +1.38%)
   - −2.0% : fill 30min 42% · séance 51% (77/159) · gap 16% · délai 1.3min · rebond 60% (47/77) (MFE +1.43%)
   - −3.0% : fill 30min 24% · séance 37% (55/159) · gap 9% · délai 5.2min · rebond 50% (25/55) (MFE +0.99%)
   - −4.0% : fill 30min 18% · séance 26% (40/159) · gap 6% · délai 12.5min · rebond 55% (20/40) (MFE +1.02%)
   - −5.0% : fill 30min 12% · séance 20% (28/159) · gap 2% · délai 25.3min · rebond 51% (13/28) (MFE +1.01%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.32% (p90 −2.03%) → stop au-delà de −1.33% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.63% (p90 −2.14%) → stop au-delà de −1.37% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.48% (p90 −1.38%) → stop au-delà de −0.99% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=545 jambes) : jambe baissière méd −1.05% (p90 −2.56%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (71 séances) :
      · −1.0% : fill 92% (66/71) · rebond 60% (39/66)
      · −2.0% : fill 78% (55/71) · rebond 60% (35/55)
      · −3.0% : fill 58% (39/71) · rebond 47% (18/39)
      · −4.0% : fill 45% (30/71) · rebond 51% (14/30)
      · −5.0% : fill 37% (23/71) · rebond 58% (12/23)
   - **flat** (28 séances) :
      · −1.0% : fill 78% (23/28) · rebond 34% (11/23)
      · −2.0% : fill 57% (12/28) · rebond 56% (7/12)
      · −3.0% : fill 46% (10/28) · rebond 57% (5/10)
      · −4.0% : fill 29% (7/28) · rebond 84% (5/7)
      · −5.0% : fill 15% (3/28) · rebond 9% (1/3)
   - **gap-up** (60 séances) :
      · −1.0% : fill 32% (18/60) · rebond 72% (11/18)
      · −2.0% : fill 17% (10/60) · rebond 69% (5/10)
      · −3.0% : fill 7% (6/60) · rebond 66% (2/6)
      · −4.0% : fill 2% (3/60) · rebond 20% (1/3)
      · −5.0% : fill 2% (2/60) · rebond 0% (0/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 66% si les 15 1res min sont vertes (79 cas) · 35% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **49min** → P(séance verte=clôture>ouverture) 82% si début vert vs 21% si rouge (base 51% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **82%** · continue >prix actuel 60% ; creux résiduel méd -0.98% (q20 -2.02%) → **SL/trailing à −2.02%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.98% / q75 +2.55% → **scale +1.98% / runner +2.55%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **21%** (continue à baisser 50%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.31%** (au-delà de la MAE q10 -3.31%), cible rebond +1.45% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.07% .. +3.52%] · haut q95 +3.83% · bas q05 -4.31%
   - 60min (n=160) : retour [-3.93% .. +3.75%] · haut q95 +4.51% · bas q05 -4.46%
   - 2h (n=160) : retour [-4.14% .. +4.52%] · haut q95 +4.77% · bas q05 -4.84%
   - 4h (n=160) : retour [-4.47% .. +5.21%] · haut q95 +5.68% · bas q05 -5.91%
   - 6h (n=160) : retour [-5.07% .. +4.87%] · haut q95 +6.08% · bas q05 -6.33%
   - session (n=160) : retour [-4.98% .. +4.64%] · haut q95 +6.08% · bas q05 -6.33%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 2.5% / strong 2.5%) · base = 8 séances trend-up (n_eff 6.2)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **26%**. Lecture précoce 30 min : signature présente → 13% vs absente 2% (base 5%)
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
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-03 — PLTR earnings (J-2 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-03 — PLTR earnings (J-2 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 44.6  _(momentum baissier)_
- **ADX** : 12.7  _(pas de tendance nette)_
- **MACD** : hist -0.705  _(pas de croisement recent)_
- **BB** : %B 0.11 · largeur 14.1%
- **ATR** : 6.63 (27.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.119  _(accumulation)_
- **Vol ratio** : 0.77  _(volume normal)_
- **Choppiness** : 60.2  _(transition)_
- **MA** : MA20 129.36 · MA50 130.96 · MA200 153.16  _(prix < MA20)_
- **Dist MA** : MA20 -5.5% · MA50 -6.6% · MA200 -20.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88486 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
