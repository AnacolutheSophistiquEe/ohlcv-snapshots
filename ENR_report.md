# ENR

**Generated** : 2026-07-31T21:40:11.323980+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €147.44  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot €147.44 (+5.6% vs entrée) · entrée €139.63 · stop €137.23 · T1 €142.54 · R/R 1.21  
> ↳ P(T1 av. stop) 37 % · EV/risk -0.032 · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.72% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €139.04–€140.21 (mid €139.63)
- Spot actuel : €147.44 (+5.6% au-dessus de la zone — repli à attendre)
- Stop : €137.23 (stop swing_plan-based (-13.72%))
- Targets : T1 €142.54 · R/R 1.21 | T2 €145.46 · R/R 2.43 | T3 €148.38 · R/R 3.65
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €137.23


## Edge, scénarios & sizing

- EV/risk : -0.032 | EV/share : €-0.077 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 12 % | T3 7 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 9.1 | bear 50.0 | side 40.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=10, n_eff=5))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→60% · +2.0%→42% · +3.0%→25% · +5.0%→9% · +8.0%→0%
- Range intraday médian 3.95% (p90 6.24%) · excursion haute méd. +1.47% / basse méd. −1.78%
- Profil de vol intra : ouverture 2.032% vs midi 0.907% vs clôture 1.161% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 58% · recovery-V 23%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; neutre — autocorr -0.017)_ ; drift intra méd. -0.632% ; recovery-V 15%
- **σ réalisé intraday** 2.688% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 70% / whipsaw 40%
- POC intraday (dernière séance, temps-au-prix) : 137.8395 (VA 136.3295–138.7455 ; dernier close 135.7)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 17% · rebond 63% · **stop −4.13%** sous le fill (sous le bruit) · cible +1.33% · R/R 0.32 (high win-rate)
- Gaps overnight (n=159) : méd. 0.19% · baisse 41% (gap-down >1% 24% · >2% 13%)
- Excursion ouverture 5min (n=160) : bas méd −0.56% (p90 −1.72%) · haut méd +0.45% · range méd 1.18%
- Excursion ouverture 15min (n=160) : bas méd −0.72% (p90 −2.21%) · haut méd +0.61% · range méd 1.55%
- Excursion ouverture 30min (n=160) : bas méd −0.85% (p90 −2.3%) · haut méd +0.62% · range méd 1.89%
- Excursion ouverture 60min (n=160) : bas méd −0.96% (p90 −2.57%) · haut méd +0.72% · range méd 2.05%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 135.7 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 74% (118/159) · gap 31% · délai 0.2min · rebond 54% (63/118) (MFE +1.11%)
   - −1.0% : fill 30min 51% · séance 70% (108/159) · gap 24% · délai 1.2min · rebond 62% (66/108) (MFE +1.37%)
   - −1.5% : fill 30min 40% · séance 62% (93/159) · gap 20% · délai 11.6min · rebond 65% (61/93) (MFE +1.54%)
   - −2.0% : fill 30min 25% · séance 49% (70/159) · gap 13% · délai 28.6min · rebond 60% (43/70) (MFE +1.43%)
   - −3.0% : fill 30min 15% · séance 34% (50/159) · gap 4% · délai 130.7min · rebond 60% (34/50) (MFE +1.41%)
   - −4.0% : fill 30min 7% · séance 23% (38/159) · gap 3% · délai 271.7min · rebond 59% (26/38) (MFE +1.22%)
   - −5.0% : fill 30min 3% · séance 17% (23/159) · gap 1% · délai 219.5min · rebond 63% (15/23) (MFE +1.33%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.56% (p90 −1.89%) → stop au-delà de −1.02% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.52% (p90 −1.7%) → stop au-delà de −0.97% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −1.14%) → stop au-delà de −0.71% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=504 jambes) : jambe baissière méd −1.05% (p90 −2.6%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (51 séances) :
      · −1.0% : fill 97% (50/51) · rebond 60% (29/50)
      · −2.0% : fill 77% (38/51) · rebond 58% (24/38)
      · −3.0% : fill 61% (31/51) · rebond 50% (20/31)
      · −4.0% : fill 45% (25/51) · rebond 53% (17/25)
      · −5.0% : fill 36% (17/51) · rebond 59% (11/17)
   - **flat** (28 séances) :
      · −1.0% : fill 71% (22/28) · rebond 78% (16/22)
      · −2.0% : fill 36% (10/28) · rebond 69% (5/10)
      · −3.0% : fill 13% (5/28) · rebond 80% (3/5)
      · −4.0% : fill 11% (4/28) · rebond 76% (2/4)
      · −5.0% : fill 7% (2/28) · rebond 74% (1/2)
   - **gap-up** (80 séances) :
      · −1.0% : fill 48% (36/80) · rebond 55% (21/36)
      · −2.0% : fill 33% (22/80) · rebond 60% (14/22)
      · −3.0% : fill 20% (14/80) · rebond 77% (11/14)
      · −4.0% : fill 10% (9/80) · rebond 69% (7/9)
      · −5.0% : fill 6% (4/80) · rebond 78% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 80% si les 15 1res min sont vertes (76 cas) · 24% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:24** → P(séance verte=clôture>ouverture) 83% si début vert vs 26% si rouge (base 48% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 225min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **83%** · continue >prix actuel 62% ; creux résiduel méd -1.0% (q20 -2.25%) → **SL/trailing à −2.25%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.11% / q75 +2.71% → **scale +2.11% / runner +2.71%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **26%** (continue à baisser 52%) → **RÉDUIRE ~74%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.61%** (au-delà de la MAE q10 -4.61%), cible rebond +1.43% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.26% .. +2.04%] · haut q95 +2.59% · bas q05 -2.71%
   - 60min (n=160) : retour [-2.42% .. +2.22%] · haut q95 +2.71% · bas q05 -3.04%
   - 2h (n=160) : retour [-2.84% .. +2.52%] · haut q95 +2.94% · bas q05 -3.74%
   - 4h (n=160) : retour [-3.04% .. +2.67%] · haut q95 +3.86% · bas q05 -4.21%
   - 6h (n=160) : retour [-3.68% .. +3.51%] · haut q95 +4.3% · bas q05 -4.48%
   - session (n=160) : retour [-5.37% .. +4.32%] · haut q95 +5.37% · bas q05 -6.21%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 1.3% / strong 3.7%) · base = 8 séances trend-up (n_eff 6.1)
- **ARMER** : fenêtre la + prédictive = **45 min** → P(reste trend-up à la clôture) **18%**. Lecture précoce 30 min : signature présente → 17% vs absente 2% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.81% (p75 1.14% / p90 1.33%) · ~3.0 replis/séance, durée méd 68.37 min. P(nouveau plus-haut après repli) :
   - −0.5% → **99%** (reprise méd 40.0 min, n=24)
   - −1.0% → **100%** (reprise méd 77.51 min, n=9)
- **RIDER — climb (trail + cibles)** : trail **−1.33%** (p90, défaut prudent ; serré/agressif −1.14%) ; extension open→close méd +4.34% (q75 +4.76% / q95 +6.23%), MFE méd +4.72% / q90 +6.39%
   - Échelle scale-out : +4.72% (33%) / +5.59% (33%) / +6.39% (34%)
- **DÉSARMER** : repli > **−1.33%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +6.39% : P(retournement après) 0% (mèche méd 0.4%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.53%)


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
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-04 — ENR earnings (J-3 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-04 — ENR earnings (J-3 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 47.2  _(neutre)_
- **ADX** : 21.3  _(pas de tendance nette)_
- **MACD** : hist -0.563  _(pas de croisement recent)_
- **BB** : %B 0.38 · largeur 19.0%
- **ATR** : 8.0 (82.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.174  _(distribution)_
- **Vol ratio** : 1.04  _(volume normal)_
- **Choppiness** : 52.3  _(transition)_
- **MA** : MA20 150.97 · MA50 157.38 · MA200 144.52  _(prix < MA20)_
- **Dist MA** : MA20 -2.3% · MA50 -6.3% · MA200 +2.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (94308 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
