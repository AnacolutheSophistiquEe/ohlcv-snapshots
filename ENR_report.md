# ENR

**Generated** : 2026-08-05T21:40:15.357509+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €150.86  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-5 sess · macro taux)  
> ↳ spot €150.86 (+14.5% vs entrée) · entrée €131.79 · stop €123.29 · T1 €137.04 · R/R 0.62  
> ↳ P(T1 av. stop) 53 % · EV/risk -0.013 · ¼-Kelly 0.001 · _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €130.74–€132.84 (mid €131.79)
- Spot actuel : €150.86 (+14.5% au-dessus de la zone — repli à attendre)
- Stop : €123.29 (stop swing_plan-based (-18.27%))
- Targets : T1 €137.04 · R/R 0.62 | T2 €142.29 · R/R 1.24 | T3 €147.55 · R/R 1.85
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €123.29


## Edge, scénarios & sizing

- EV/risk : -0.013 | EV/share : €-0.109 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 53 % | T2 26 % | T3 7 %
- Kelly (position) : f* 0.004 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 23.8 | bear 43.6 | side 32.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 151.0 (= 1 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=6, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→59% · +2.0%→40% · +3.0%→25% · +5.0%→10% · +8.0%→1%
- Range intraday médian 4.18% (p90 6.67%) · excursion haute méd. +1.31% / basse méd. −1.82%
- Profil de vol intra : ouverture 2.055% vs midi 0.924% vs clôture 1.17% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 13% · trend ↑2%/↓0% ; spike-down 59% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.136 ; neutre — autocorr -0.024)_ ; drift intra méd. -0.385% ; recovery-V 13%
- **σ réalisé intraday** 2.707% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 74% / whipsaw 39%
- POC intraday (dernière séance, temps-au-prix) : 145.608 (VA 145.424–148.368 ; dernier close 147.87)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 16% · rebond 63% · **stop −4.13%** sous le fill (sous le bruit) · cible +1.33% · R/R 0.32 (high win-rate)
- Gaps overnight (n=159) : méd. 0.25% · baisse 41% (gap-down >1% 22% · >2% 12%)
- Excursion ouverture 5min (n=160) : bas méd −0.55% (p90 −1.84%) · haut méd +0.46% · range méd 1.2%
- Excursion ouverture 15min (n=160) : bas méd −0.71% (p90 −2.22%) · haut méd +0.62% · range méd 1.54%
- Excursion ouverture 30min (n=160) : bas méd −0.85% (p90 −2.29%) · haut méd +0.64% · range méd 1.87%
- Excursion ouverture 60min (n=160) : bas méd −0.94% (p90 −2.57%) · haut méd +0.75% · range méd 2.03%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 147.87 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 73% (117/159) · gap 31% · délai 0.2min · rebond 56% (63/117) (MFE +1.16%)
   - −1.0% : fill 30min 50% · séance 70% (109/159) · gap 22% · délai 1.6min · rebond 64% (68/109) (MFE +1.55%)
   - −1.5% : fill 30min 38% · séance 63% (94/159) · gap 18% · délai 13.1min · rebond 67% (62/94) (MFE +1.74%)
   - −2.0% : fill 30min 24% · séance 48% (70/159) · gap 12% · délai 35.8min · rebond 61% (43/70) (MFE +1.48%)
   - −3.0% : fill 30min 14% · séance 32% (50/159) · gap 4% · délai 130.7min · rebond 60% (34/50) (MFE +1.41%)
   - −4.0% : fill 30min 7% · séance 22% (38/159) · gap 3% · délai 271.7min · rebond 59% (26/38) (MFE +1.22%)
   - −5.0% : fill 30min 2% · séance 16% (23/159) · gap 1% · délai 219.5min · rebond 63% (15/23) (MFE +1.33%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.56% (p90 −1.74%) → stop au-delà de −0.99% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.53% (p90 −1.68%) → stop au-delà de −0.96% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −1.02%) → stop au-delà de −0.85% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=511 jambes) : jambe baissière méd −1.08% (p90 −2.57%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (52 séances) :
      · −1.0% : fill 97% (51/52) · rebond 62% (30/51)
      · −2.0% : fill 74% (38/52) · rebond 58% (24/38)
      · −3.0% : fill 58% (31/52) · rebond 50% (20/31)
      · −4.0% : fill 43% (25/52) · rebond 53% (17/25)
      · −5.0% : fill 34% (17/52) · rebond 59% (11/17)
   - **flat** (27 séances) :
      · −1.0% : fill 71% (22/27) · rebond 78% (16/22)
      · −2.0% : fill 36% (10/27) · rebond 69% (5/10)
      · −3.0% : fill 13% (5/27) · rebond 80% (3/5)
      · −4.0% : fill 11% (4/27) · rebond 76% (2/4)
      · −5.0% : fill 7% (2/27) · rebond 74% (1/2)
   - **gap-up** (80 séances) :
      · −1.0% : fill 48% (36/80) · rebond 59% (22/36)
      · −2.0% : fill 34% (22/80) · rebond 64% (14/22)
      · −3.0% : fill 19% (14/80) · rebond 77% (11/14)
      · −4.0% : fill 10% (9/80) · rebond 69% (7/9)
      · −5.0% : fill 5% (4/80) · rebond 78% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 77% si les 15 1res min sont vertes (77 cas) · 23% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:24** → P(séance verte=clôture>ouverture) 83% si début vert vs 26% si rouge (base 48% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 282min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **83%** · continue >prix actuel 62% ; creux résiduel méd -1.0% (q20 -2.26%) → **SL/trailing à −2.26%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.11% / q75 +2.71% → **scale +2.11% / runner +2.71%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **26%** (continue à baisser 50%) → **RÉDUIRE ~74%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.43%** (au-delà de la MAE q10 -4.43%), cible rebond +1.45% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.26% .. +2.02%] · haut q95 +2.56% · bas q05 -2.71%
   - 60min (n=160) : retour [-2.35% .. +2.14%] · haut q95 +2.69% · bas q05 -2.84%
   - 2h (n=160) : retour [-2.84% .. +2.45%] · haut q95 +2.9% · bas q05 -3.7%
   - 4h (n=160) : retour [-3.19% .. +2.66%] · haut q95 +3.84% · bas q05 -4.15%
   - 6h (n=160) : retour [-3.75% .. +3.91%] · haut q95 +4.86% · bas q05 -4.62%
   - session (n=160) : retour [-5.32% .. +4.46%] · haut q95 +5.85% · bas q05 -6.2%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 1.3% / strong 4.4%) · base = 9 séances trend-up (n_eff 6.6)
- **ARMER** : fenêtre la + prédictive = **45 min** → P(reste trend-up à la clôture) **18%**. Lecture précoce 30 min : signature présente → 16% vs absente 4% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.83% (p75 1.19% / p90 1.45%) · ~3.0 replis/séance, durée méd 78.78 min. P(nouveau plus-haut après repli) :
   - −0.5% → **99%** (reprise méd 55.57 min, n=25)
   - −1.0% → **100%** (reprise méd 80.0 min, n=10)
- **RIDER — climb (trail + cibles)** : trail **−1.45%** (p90, défaut prudent ; serré/agressif −1.19%) ; extension open→close méd +4.46% (q75 +6.49% / q95 +8.61%), MFE méd +5.07% / q90 +9.14%
   - Échelle scale-out : +5.07% (33%) / +6.83% (33%) / +9.14% (34%)
- **DÉSARMER** : repli > **−1.45%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +9.14% : P(retournement après) 0% (mèche méd 0.54%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.37%)


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
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 48.8  _(neutre)_
- **ADX** : 19.1  _(pas de tendance nette)_
- **MACD** : hist 0.403  _(bullish_recent)_
- **BB** : %B 0.55 · largeur 14.3%
- **ATR** : 8.5 (90.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.171  _(distribution)_
- **Vol ratio** : 1.28  _(volume normal)_
- **Choppiness** : 54.6  _(transition)_
- **MA** : MA20 149.77 · MA50 156.16 · MA200 144.98  _(prix > MA20)_
- **Dist MA** : MA20 +0.7% · MA50 -3.4% · MA200 +4.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93759 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
