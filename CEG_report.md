# CEG

**Generated** : 2026-08-06T00:28:21.135025+00:00  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $265.12  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot $265.12 (+8.2% vs entrée) · entrée $244.99 · stop $234.93 · T1 $251.74 · R/R 0.67  
> ↳ P(T1 av. stop) 71 % · EV/risk 0.053 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $243.65–$246.34 (mid $244.99)
- Spot actuel : $265.12 (+8.2% au-dessus de la zone — repli à attendre)
- Stop : $234.93 (stop swing_plan-based (-11.39%))
- Targets : T1 $251.74 · R/R 0.67 | T2 $258.48 · R/R 1.34 | T3 $265.22 · R/R 2.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $234.93


## Edge, scénarios & sizing

- EV/risk : -0.049 | EV/share : $-0.496 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 56 % | T2 39 % | T3 21 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 78.5 | bear 7.7 | side 13.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=12, n_eff=6))
  - **swing** : indisponible (échantillon insuffisant (n=6, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=5, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→64% · +2.0%→38% · +3.0%→19% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.38% (p90 5.5%) · excursion haute méd. +1.44% / basse méd. −1.52%
- Profil de vol intra : ouverture 2.461% vs midi 0.689% vs clôture 0.744% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓0% ; spike-down 47% · recovery-V 18%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; mean-reverting — autocorr -0.037)_ ; drift intra méd. 0.0% ; recovery-V 13%
- **σ réalisé intraday** 2.186% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 63% / bas 58% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 273.2646 (VA 271.0474–274.5316 ; dernier close 273.69)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 40% · rebond 62% · **stop −2.95%** sous le fill (sous le bruit) · cible +1.15% · R/R 0.39 (high win-rate)
- Gaps overnight (n=159) : méd. 0.26% · baisse 42% (gap-down >1% 19% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −0.6% (p90 −1.85%) · haut méd +0.84% · range méd 1.63%
- Excursion ouverture 15min (n=160) : bas méd −0.66% (p90 −2.09%) · haut méd +1.0% · range méd 2.03%
- Excursion ouverture 30min (n=160) : bas méd −0.85% (p90 −2.52%) · haut méd +1.07% · range méd 2.31%
- Excursion ouverture 60min (n=160) : bas méd −0.99% (p90 −2.76%) · haut méd +1.3% · range méd 2.67%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 273.69 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 55% · séance 68% (117/159) · gap 26% · délai 0.0min · rebond 46% (56/117) (MFE +0.93%)
   - −1.0% : fill 30min 46% · séance 60% (101/159) · gap 19% · délai 1.5min · rebond 54% (56/101) (MFE +1.18%)
   - −1.5% : fill 30min 36% · séance 46% (85/159) · gap 11% · délai 3.1min · rebond 51% (45/85) (MFE +1.04%)
   - −2.0% : fill 30min 26% · séance 40% (68/159) · gap 8% · délai 8.4min · rebond 62% (43/68) (MFE +1.15%)
   - −3.0% : fill 30min 11% · séance 24% (41/159) · gap 2% · délai 41.0min · rebond 38% (14/41) (MFE +0.79%)
   - −4.0% : fill 30min 6% · séance 14% (27/159) · gap 2% · délai 37.9min · rebond 46% (13/27) (MFE +0.83%)
   - −5.0% : fill 30min 3% · séance 7% (17/159) · gap 1% · délai 45.1min · rebond 76% (12/17) (MFE +1.23%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.41% (p90 −1.47%) → stop au-delà de −0.88% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.3% (p90 −1.15%) → stop au-delà de −0.83% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −1.37%) → stop au-delà de −1.06% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=462 jambes) : jambe baissière méd −1.05% (p90 −2.59%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 96% (55/56) · rebond 49% (31/55)
      · −2.0% : fill 76% (42/56) · rebond 58% (27/42)
      · −3.0% : fill 52% (29/56) · rebond 42% (12/29)
      · −4.0% : fill 33% (20/56) · rebond 44% (9/20)
      · −5.0% : fill 20% (15/56) · rebond 77% (11/15)
   - **flat** (32 séances) :
      · −1.0% : fill 64% (18/32) · rebond 33% (5/18)
      · −2.0% : fill 32% (9/32) · rebond 48% (3/9)
      · −3.0% : fill 21% (7/32) · rebond 21% (1/7)
      · −4.0% : fill 9% (4/32) · rebond 20% (1/4)
      · −5.0% : fill 3% (2/32) · rebond 61% (1/2)
   - **gap-up** (71 séances) :
      · −1.0% : fill 34% (28/71) · rebond 75% (20/28)
      · −2.0% : fill 18% (17/71) · rebond 84% (13/17)
      · −3.0% : fill 4% (5/71) · rebond 29% (1/5)
      · −4.0% : fill 2% (3/71) · rebond 100% (3/3)
      · −5.0% : fill 0% (0/71) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 68% si les 15 1res min sont vertes (90 cas) · 26% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **32min** → P(séance verte=clôture>ouverture) 75% si début vert vs 13% si rouge (base 49% · écart 62 pts) ; prédictivité sature ensuite (plafond brut 194min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=93) : tient le vert **75%** · continue >prix actuel 51% ; creux résiduel méd -1.08% (q20 -2.24%) → **SL/trailing à −2.24%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.08% / q75 +2.16% → **scale +1.08% / runner +2.16%**, sortie à la clôture
  - **si ROUGE au coude** (n=67) : edge inversé — récupère vert seulement **13%** (continue à baisser 71%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.09%** (au-delà de la MAE q10 -3.09%), cible rebond +1.03% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.58% .. +2.29%] · haut q95 +2.72% · bas q05 -3.25%
   - 60min (n=160) : retour [-2.88% .. +2.81%] · haut q95 +3.38% · bas q05 -3.98%
   - 2h (n=160) : retour [-3.61% .. +3.0%] · haut q95 +4.19% · bas q05 -4.47%
   - 4h (n=160) : retour [-3.45% .. +3.46%] · haut q95 +4.37% · bas q05 -4.57%
   - 6h (n=160) : retour [-4.22% .. +3.46%] · haut q95 +4.63% · bas q05 -4.8%
   - session (n=160) : retour [-3.85% .. +3.46%] · haut q95 +4.67% · bas q05 -4.8%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 4.4% / strong 1.9%) · base = 10 séances trend-up (n_eff 6.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 15% vs absente 4% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.05% (p75 1.33% / p90 1.45%) · ~1.45 replis/séance, durée méd 90.1 min. P(nouveau plus-haut après repli) :
   - −0.5% → **65%** (reprise méd 23.89 min, n=22)
   - −1.0% → **74%** (reprise méd 54.64 min, n=10)
- **RIDER — climb (trail + cibles)** : trail **−1.45%** (p90, défaut prudent ; serré/agressif −1.33%) ; extension open→close méd +3.33% (q75 +4.19% / q95 +6.07%), MFE méd +3.68% / q90 +5.35%
   - Échelle scale-out : +3.68% (33%) / +4.76% (33%) / +5.35% (34%)
- **DÉSARMER** : repli > **−1.45%** depuis le plus-haut = décay → P(retournement) **70%** (préavis méd 295.0 min, n=0) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.35% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 93% du temps (retour médian dernière heure +0.39%)


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-08-06 — CEG earnings (J-0 sess · earnings)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 59.9  _(momentum haussier)_
- **ADX** : 12.8  _(pas de tendance nette)_
- **MACD** : hist 0.83  _(pas de croisement recent)_
- **BB** : %B 0.59 · largeur 12.8%
- **ATR** : 10.06 (16.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.076  _(distribution)_
- **Vol ratio** : 1.13  _(volume normal)_
- **Choppiness** : 53.1  _(transition)_
- **MA** : MA20 261.96 · MA50 262.1 · MA200 305.47  _(prix > MA20)_
- **Dist MA** : MA20 +1.2% · MA50 +1.2% · MA200 -13.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (85788 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
