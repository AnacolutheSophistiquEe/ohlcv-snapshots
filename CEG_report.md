# CEG

**Generated** : 2026-08-03T00:26:10.299124+00:00  
**Santé technique** : 5/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $262.75  

> 🟡 **WAIT-FOR-DIP** — spot +3.7 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $262.75 (+3.7% vs entrée) · entrée $253.32 · stop $249.52 · T1 $256.33 · R/R 0.79  
> ↳ P(T1 av. stop) 62 % · EV/risk 0.311 · ¼-Kelly 0.005 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $252.71–$253.92 (mid $253.32)
- Spot actuel : $262.75 (+3.7% au-dessus de la zone — repli à attendre)
- Stop : $249.52 (stop swing_plan-based (-10.77%))
- Targets : T1 $256.33 · R/R 0.79 | T2 $259.34 · R/R 1.58 | T3 $262.36 · R/R 2.38
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $249.52


## Edge, scénarios & sizing

- EV/risk : -0.043 | EV/share : $-0.164 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 55 % | T2 29 % | T3 8 %
- Kelly (position) : f* 0.02 | ¼-Kelly 0.005 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 83.2 | bear 6.9 | side 9.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=13, n_eff=7))
  - **swing** : indisponible (échantillon insuffisant (n=7, n_eff=5))
  - **deep** : indisponible (échantillon insuffisant (n=7, n_eff=5))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→64% · +2.0%→38% · +3.0%→19% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.38% (p90 5.5%) · excursion haute méd. +1.44% / basse méd. −1.52%
- Profil de vol intra : ouverture 2.475% vs midi 0.71% vs clôture 0.738% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 48% · recovery-V 15%)_
- **Régime intraday** : **chop** _(efficiency 0.118 ; mean-reverting — autocorr -0.039)_ ; drift intra méd. -0.156% ; recovery-V 6%
- **σ réalisé intraday** 2.196% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 61% / bas 61% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 264.338 (VA 262.43–264.55 ; dernier close 262.76)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 41% · rebond 62% · **stop −2.95%** sous le fill (sous le bruit) · cible +1.15% · R/R 0.39 (high win-rate)
- Gaps overnight (n=159) : méd. 0.22% · baisse 42% (gap-down >1% 19% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −0.6% (p90 −1.85%) · haut méd +0.82% · range méd 1.62%
- Excursion ouverture 15min (n=160) : bas méd −0.65% (p90 −2.12%) · haut méd +0.99% · range méd 2.01%
- Excursion ouverture 30min (n=160) : bas méd −0.82% (p90 −2.53%) · haut méd +1.04% · range méd 2.31%
- Excursion ouverture 60min (n=160) : bas méd −0.98% (p90 −2.76%) · haut méd +1.29% · range méd 2.65%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 262.76 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 69% (118/159) · gap 26% · délai 0.0min · rebond 46% (57/118) (MFE +0.93%)
   - −1.0% : fill 30min 47% · séance 61% (102/159) · gap 19% · délai 1.5min · rebond 54% (57/102) (MFE +1.18%)
   - −1.5% : fill 30min 36% · séance 47% (85/159) · gap 11% · délai 3.1min · rebond 51% (45/85) (MFE +1.04%)
   - −2.0% : fill 30min 27% · séance 41% (68/159) · gap 8% · délai 8.4min · rebond 62% (43/68) (MFE +1.15%)
   - −3.0% : fill 30min 11% · séance 24% (41/159) · gap 2% · délai 41.0min · rebond 38% (14/41) (MFE +0.79%)
   - −4.0% : fill 30min 6% · séance 14% (27/159) · gap 2% · délai 37.9min · rebond 46% (13/27) (MFE +0.83%)
   - −5.0% : fill 30min 3% · séance 8% (17/159) · gap 1% · délai 45.1min · rebond 76% (12/17) (MFE +1.23%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.43% (p90 −1.51%) → stop au-delà de −0.9% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.25% (p90 −0.98%) → stop au-delà de −0.64% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.3% (p90 −1.26%) → stop au-delà de −0.82% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=463 jambes) : jambe baissière méd −1.06% (p90 −2.59%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (57 séances) :
      · −1.0% : fill 96% (56/57) · rebond 49% (32/56)
      · −2.0% : fill 75% (42/57) · rebond 58% (27/42)
      · −3.0% : fill 52% (29/57) · rebond 42% (12/29)
      · −4.0% : fill 33% (20/57) · rebond 44% (9/20)
      · −5.0% : fill 20% (15/57) · rebond 77% (11/15)
   - **flat** (32 séances) :
      · −1.0% : fill 64% (18/32) · rebond 33% (5/18)
      · −2.0% : fill 32% (9/32) · rebond 48% (3/9)
      · −3.0% : fill 21% (7/32) · rebond 21% (1/7)
      · −4.0% : fill 9% (4/32) · rebond 20% (1/4)
      · −5.0% : fill 3% (2/32) · rebond 61% (1/2)
   - **gap-up** (70 séances) :
      · −1.0% : fill 35% (28/70) · rebond 75% (20/28)
      · −2.0% : fill 19% (17/70) · rebond 84% (13/17)
      · −3.0% : fill 5% (5/70) · rebond 29% (1/5)
      · −4.0% : fill 2% (3/70) · rebond 100% (3/3)
      · −5.0% : fill 0% (0/70) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 68% si les 15 1res min sont vertes (90 cas) · 22% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **32min** → P(séance verte=clôture>ouverture) 74% si début vert vs 13% si rouge (base 48% · écart 61 pts) ; prédictivité sature ensuite (plafond brut 194min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=92) : tient le vert **74%** · continue >prix actuel 49% ; creux résiduel méd -1.08% (q20 -2.45%) → **SL/trailing à −2.45%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.08% / q75 +1.9% → **scale +1.08% / runner +1.9%**, sortie à la clôture
  - **si ROUGE au coude** (n=68) : edge inversé — récupère vert seulement **13%** (continue à baisser 71%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.09%** (au-delà de la MAE q10 -3.09%), cible rebond +1.02% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.61% .. +2.29%] · haut q95 +2.73% · bas q05 -3.25%
   - 60min (n=160) : retour [-2.89% .. +2.86%] · haut q95 +3.38% · bas q05 -4.0%
   - 2h (n=160) : retour [-3.63% .. +3.0%] · haut q95 +4.19% · bas q05 -4.49%
   - 4h (n=160) : retour [-3.47% .. +3.35%] · haut q95 +4.41% · bas q05 -4.58%
   - 6h (n=160) : retour [-4.23% .. +3.48%] · haut q95 +4.65% · bas q05 -4.83%
   - session (n=160) : retour [-3.89% .. +3.47%] · haut q95 +4.67% · bas q05 -4.82%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 3.7% / strong 1.9%) · base = 9 séances trend-up (n_eff 6.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **28%**. Lecture précoce 30 min : signature présente → 15% vs absente 1% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.18% (p75 1.36% / p90 1.68%) · ~1.0 replis/séance, durée méd 90.1 min. P(nouveau plus-haut après repli) :
   - −0.5% → **71%** (reprise méd 32.71 min, n=20)
   - −1.0% → **67%** (reprise méd 175.01 min, n=9)
- **RIDER — climb (trail + cibles)** : trail **−1.68%** (p90, défaut prudent ; serré/agressif −1.36%) ; extension open→close méd +3.46% (q75 +4.38% / q95 +6.41%), MFE méd +3.74% / q90 +5.85%
   - Échelle scale-out : +3.74% (33%) / +5.06% (33%) / +5.85% (34%)
- **DÉSARMER** : repli > **−1.68%** depuis le plus-haut = décay → P(retournement) **70%** (préavis méd 295.0 min, n=0) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.85% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 92% du temps (retour médian dernière heure +0.37%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-06 — CEG earnings (J-2 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-06 — CEG earnings (J-2 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 54.5  _(neutre)_
- **ADX** : 13.3  _(pas de tendance nette)_
- **MACD** : hist 0.868  _(pas de croisement recent)_
- **BB** : %B 0.61 · largeur 15.6%
- **ATR** : 9.43 (11.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.007  _(neutre)_
- **Vol ratio** : 0.67  _(volume normal)_
- **Choppiness** : 50.7  _(transition)_
- **MA** : MA20 258.16 · MA50 263.2 · MA200 307.37  _(prix > MA20)_
- **Dist MA** : MA20 +1.8% · MA50 -0.2% · MA200 -14.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (86723 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
