# CEG

**Generated** : 2026-07-09T00:23:11.142708+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $244.52  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $244.52 (+0.3% vs entrée) · entrée $243.78 · stop $240.12 · T1 $247.14 · R/R 0.92  
> ↳ P(T1 av. stop) 49 % _(réel 5 s)_ · EV/risk -0.048 _(réel 5 s)_ (GBM -0.076) · ¼-Kelly 0.002 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $243.11–$244.45 (mid $243.78)
- Spot actuel : $244.52 (+0.3% au-dessus de la zone — repli à attendre)
- Stop : $240.12 (stop swing_plan-based (-2.2%))
- Targets : T1 $247.14 · R/R 0.92 | T2 $250.51 · R/R 1.84 | T3 $253.88 · R/R 2.76
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $240.12


## Edge, scénarios & sizing

- EV/risk : -0.076 | EV/share : $-0.278 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 50 % | T2 22 % | T3 9 %
- Kelly (position) : f* 0.006 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 78.4 | bear 5.9 | side 15.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.305% → cible +1.381% / stop −1.5%, p_fill 85%, n_eff≈35.0) : P(cible|rempli) **49%** · **EV/risk -0.048** (×p_fill ; si rempli -0.08% du capital)
  - **swing** (entrée dip −0.667% → cible +3.087% / stop −1.544%, p_fill 84%, n_eff≈33.6) : P(cible|rempli) **21%** · **EV/risk -0.361** (×p_fill ; si rempli -0.66% du capital)
  - **deep** (entrée dip −1.03% → cible +4.366% / stop −2.183%, p_fill 70%, n_eff≈30.3) : P(cible|rempli) **13%** · **EV/risk -0.450** (×p_fill ; si rempli -1.40% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→66% · +2.0%→38% · +3.0%→22% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.45% (p90 5.51%) · excursion haute méd. +1.5% / basse méd. −1.67%
- Profil de vol intra : ouverture 2.582% vs midi 0.739% vs clôture 0.793% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 51% · recovery-V 21%)_
- **Régime intraday** : **chop** _(efficiency 0.11 ; mean-reverting — autocorr -0.06)_ ; drift intra méd. -0.513% ; recovery-V 14%
- **σ réalisé intraday** 2.416% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 60% / whipsaw 13%
- POC intraday (dernière séance, temps-au-prix) : 240.5788 (VA 239.7312–242.1043 ; dernier close 239.63)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 48% · rebond 60% · **stop −3.19%** sous le fill (sous le bruit) · cible +1.08% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. 0.11% · baisse 45% (gap-down >1% 20% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −0.64% (p90 −1.64%) · haut méd +0.81% · range méd 1.69%
- Excursion ouverture 15min (n=160) : bas méd −0.8% (p90 −2.25%) · haut méd +1.0% · range méd 2.11%
- Excursion ouverture 30min (n=160) : bas méd −0.88% (p90 −2.84%) · haut méd +1.08% · range méd 2.31%
- Excursion ouverture 60min (n=160) : bas méd −1.11% (p90 −3.1%) · haut méd +1.3% · range méd 2.74%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 239.63 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 72% (120/159) · gap 28% · délai 0.0min · rebond 43% (59/120) (MFE +0.88%)
   - −1.0% : fill 30min 53% · séance 65% (105/159) · gap 20% · délai 1.5min · rebond 50% (58/105) (MFE +0.99%)
   - −1.5% : fill 30min 41% · séance 56% (91/159) · gap 11% · délai 3.9min · rebond 52% (49/91) (MFE +1.05%)
   - −2.0% : fill 30min 31% · séance 48% (71/159) · gap 8% · délai 10.0min · rebond 60% (44/71) (MFE +1.08%)
   - −3.0% : fill 30min 13% · séance 29% (43/159) · gap 3% · délai 42.3min · rebond 36% (17/43) (MFE +0.79%)
   - −4.0% : fill 30min 6% · séance 17% (28/159) · gap 2% · délai 48.4min · rebond 37% (12/28) (MFE +0.6%)
   - −5.0% : fill 30min 4% · séance 10% (19/159) · gap 1% · délai 45.6min · rebond 74% (12/19) (MFE +1.21%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.47% (p90 −1.4%) → stop au-delà de −0.84% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.3% (p90 −1.13%) → stop au-delà de −0.79% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.38% (p90 −1.63%) → stop au-delà de −1.0% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=476 jambes) : jambe baissière méd −1.09% (p90 −2.63%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (57 séances) :
      · −1.0% : fill 100% (57/57) · rebond 47% (34/57)
      · −2.0% : fill 83% (42/57) · rebond 57% (28/42)
      · −3.0% : fill 57% (27/57) · rebond 39% (11/27)
      · −4.0% : fill 38% (19/57) · rebond 34% (8/19)
      · −5.0% : fill 27% (15/57) · rebond 77% (11/15)
   - **flat** (35 séances) :
      · −1.0% : fill 66% (21/35) · rebond 40% (7/21)
      · −2.0% : fill 40% (12/35) · rebond 48% (4/12)
      · −3.0% : fill 27% (10/35) · rebond 28% (4/10)
      · −4.0% : fill 12% (5/35) · rebond 19% (1/5)
      · −5.0% : fill 4% (3/35) · rebond 50% (1/3)
   - **gap-up** (67 séances) :
      · −1.0% : fill 36% (27/67) · rebond 63% (17/27)
      · −2.0% : fill 23% (17/67) · rebond 79% (12/17)
      · −3.0% : fill 7% (6/67) · rebond 32% (2/6)
      · −4.0% : fill 4% (4/67) · rebond 90% (3/4)
      · −5.0% : fill 0% (1/67) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 71% si les 15 1res min sont vertes (90 cas) · 18% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:24** → P(séance verte=clôture>ouverture) 85% si début vert vs 10% si rouge (base 48% · écart 75 pts) ; prédictivité sature ensuite (plafond brut 194min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **85%** · continue >prix actuel 39% ; creux résiduel méd -0.97% (q20 -1.89%) → **SL/trailing à −1.89%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.83% / q75 +1.71% → **scale +0.83% / runner +1.71%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **10%** (continue à baisser 53%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.79%** (au-delà de la MAE q10 -2.79%), cible rebond +0.79% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.0% .. +2.29%] · haut q95 +2.94% · bas q05 -3.57%
   - 60min (n=160) : retour [-3.83% .. +2.82%] · haut q95 +3.46% · bas q05 -4.63%
   - 2h (n=160) : retour [-3.98% .. +3.09%] · haut q95 +4.22% · bas q05 -5.09%
   - 4h (n=160) : retour [-4.31% .. +3.35%] · haut q95 +5.22% · bas q05 -5.82%
   - 6h (n=160) : retour [-4.77% .. +3.44%] · haut q95 +5.28% · bas q05 -6.61%
   - session (n=160) : retour [-4.34% .. +3.45%] · haut q95 +5.28% · bas q05 -6.61%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 3.1% / strong 1.9%) · base = 8 séances trend-up (n_eff 6.2)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **19%**. Lecture précoce 30 min : signature présente → 10% vs absente 2% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.86% (p75 1.29% / p90 1.81%) · ~2.0 replis/séance, durée méd 56.12 min. P(nouveau plus-haut après repli) :
   - −0.5% → **60%** (reprise méd 17.64 min, n=21)
   - −1.0% → **42%** (reprise méd 20.49 min, n=9)
   - −1.5% → **37%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.81%** (p90, défaut prudent ; serré/agressif −1.29%) ; extension open→close méd +3.45% (q75 +4.8% / q95 +6.6%), MFE méd +3.73% / q90 +6.44%
   - Échelle scale-out : +3.73% (33%) / +5.32% (33%) / +6.44% (34%)
- **DÉSARMER** : repli > **−1.81%** depuis le plus-haut = décay → P(retournement) **70%** (préavis méd 295.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +6.44% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 85% du temps (retour médian dernière heure +0.37%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 33.2  _(momentum baissier)_
- **ADX** : 22.4  _(pas de tendance nette)_
- **MACD** : hist -1.412  _(pas de croisement recent)_
- **BB** : %B 0.27 · largeur 20.0%
- **ATR** : 9.97 (7.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.143  _(distribution)_
- **Vol ratio** : 0.67  _(volume normal)_
- **Choppiness** : 35.9  _(marche directionnel)_
- **MA** : MA20 256.3 · MA50 275.43 · MA200 314.93  _(prix < MA20)_
- **Dist MA** : MA20 -4.6% · MA50 -11.2% · MA200 -22.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88900 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
