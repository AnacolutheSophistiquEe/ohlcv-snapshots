# CEG

**Generated** : 2026-07-10T00:29:48.816739+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $250.74  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $250.74 (+1.4% vs entrée) · entrée $247.37 · stop $243.66 · T1 $250.87 · R/R 0.94  
> ↳ P(T1 av. stop) 30 % _(réel 5 s)_ · EV/risk -0.096 _(réel 5 s)_ (GBM -0.075) · ¼-Kelly 0.002 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $246.67–$248.07 (mid $247.37)
- Spot actuel : $250.74 (+1.4% au-dessus de la zone — repli à attendre)
- Stop : $243.66 (stop swing_plan-based (-4.5%))
- Targets : T1 $250.87 · R/R 0.94 | T2 $254.38 · R/R 1.89 | T3 $257.88 · R/R 2.83
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $243.66


## Edge, scénarios & sizing

- EV/risk : -0.075 | EV/share : $-0.280 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 49 % | T2 22 % | T3 7 %
- Kelly (position) : f* 0.006 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 82.5 | bear 5.4 | side 12.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.35% → cible +1.417% / stop −1.5%, p_fill 52%, n_eff≈23.7) : P(cible|rempli) **30%** · **EV/risk -0.096** (×p_fill ; si rempli -0.28% du capital)
  - **swing** (entrée dip −2.963% → cible +3.169% / stop −1.584%, p_fill 49%, n_eff≈20.0) : P(cible|rempli) **12%** · **EV/risk -0.339** (×p_fill ; si rempli -1.10% du capital)
  - **deep** (entrée dip −4.572% → cible +4.481% / stop −2.241%, p_fill 47%, n_eff≈20.4) : P(cible|rempli) **23%** · **EV/risk -0.168** (×p_fill ; si rempli -0.81% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→66% · +2.0%→38% · +3.0%→22% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.45% (p90 5.51%) · excursion haute méd. +1.5% / basse méd. −1.67%
- Profil de vol intra : ouverture 2.586% vs midi 0.741% vs clôture 0.789% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑0%/↓0% ; spike-down 50% · recovery-V 21%)_
- **Régime intraday** : **chop** _(efficiency 0.115 ; mean-reverting — autocorr -0.054)_ ; drift intra méd. -0.347% ; recovery-V 14%
- **σ réalisé intraday** 2.391% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 51% / bas 57% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 241.335 (VA 240.543–242.523 ; dernier close 244.51)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 47% · rebond 60% · **stop −3.19%** sous le fill (sous le bruit) · cible +1.08% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. 0.1% · baisse 46% (gap-down >1% 22% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −0.64% (p90 −1.6%) · haut méd +0.83% · range méd 1.68%
- Excursion ouverture 15min (n=160) : bas méd −0.79% (p90 −2.24%) · haut méd +1.0% · range méd 2.07%
- Excursion ouverture 30min (n=160) : bas méd −0.87% (p90 −2.8%) · haut méd +1.08% · range méd 2.32%
- Excursion ouverture 60min (n=160) : bas méd −1.09% (p90 −3.08%) · haut méd +1.31% · range méd 2.76%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 244.51 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 73% (120/159) · gap 29% · délai 0.0min · rebond 45% (59/120) (MFE +0.89%)
   - −1.0% : fill 30min 54% · séance 65% (105/159) · gap 22% · délai 1.5min · rebond 51% (58/105) (MFE +1.06%)
   - −1.5% : fill 30min 41% · séance 55% (91/159) · gap 11% · délai 3.9min · rebond 52% (49/91) (MFE +1.05%)
   - −2.0% : fill 30min 30% · séance 47% (71/159) · gap 8% · délai 10.0min · rebond 60% (44/71) (MFE +1.08%)
   - −3.0% : fill 30min 13% · séance 28% (43/159) · gap 3% · délai 42.3min · rebond 36% (17/43) (MFE +0.79%)
   - −4.0% : fill 30min 5% · séance 17% (28/159) · gap 2% · délai 48.4min · rebond 37% (12/28) (MFE +0.6%)
   - −5.0% : fill 30min 4% · séance 10% (19/159) · gap 1% · délai 45.6min · rebond 74% (12/19) (MFE +1.21%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.44% (p90 −1.37%) → stop au-delà de −0.83% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.25% (p90 −1.1%) → stop au-delà de −0.73% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.28% (p90 −1.59%) → stop au-delà de −0.97% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=478 jambes) : jambe baissière méd −1.08% (p90 −2.62%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (57 séances) :
      · −1.0% : fill 100% (57/57) · rebond 50% (34/57)
      · −2.0% : fill 79% (42/57) · rebond 57% (28/42)
      · −3.0% : fill 55% (27/57) · rebond 39% (11/27)
      · −4.0% : fill 36% (19/57) · rebond 34% (8/19)
      · −5.0% : fill 25% (15/57) · rebond 77% (11/15)
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
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 72% si les 15 1res min sont vertes (90 cas) · 18% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:24** → P(séance verte=clôture>ouverture) 86% si début vert vs 10% si rouge (base 49% · écart 75 pts) ; prédictivité sature ensuite (plafond brut 194min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **86%** · continue >prix actuel 41% ; creux résiduel méd -1.02% (q20 -1.87%) → **SL/trailing à −1.87%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.85% / q75 +1.69% → **scale +0.85% / runner +1.69%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **10%** (continue à baisser 53%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.79%** (au-delà de la MAE q10 -2.79%), cible rebond +0.79% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.0% .. +2.4%] · haut q95 +2.9% · bas q05 -3.54%
   - 60min (n=160) : retour [-3.83% .. +2.78%] · haut q95 +3.45% · bas q05 -4.61%
   - 2h (n=160) : retour [-3.97% .. +3.08%] · haut q95 +4.21% · bas q05 -5.07%
   - 4h (n=160) : retour [-4.2% .. +3.35%] · haut q95 +5.17% · bas q05 -5.79%
   - 6h (n=160) : retour [-4.77% .. +3.43%] · haut q95 +5.28% · bas q05 -6.32%
   - session (n=160) : retour [-4.34% .. +3.44%] · haut q95 +5.28% · bas q05 -6.32%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 3.7% / strong 1.9%) · base = 9 séances trend-up (n_eff 6.2)
- **ARMER** : fenêtre la + prédictive = **60 min** → P(reste trend-up à la clôture) **26%**. Lecture précoce 30 min : signature présente → 15% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.07% (p75 1.33% / p90 1.7%) · ~1.3 replis/séance, durée méd 60.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **65%** (reprise méd 22.57 min, n=22)
   - −1.0% → **58%** (reprise méd 114.96 min, n=10)
   - −1.5% → **37%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.7%** (p90, défaut prudent ; serré/agressif −1.33%) ; extension open→close méd +3.24% (q75 +3.91% / q95 +6.6%), MFE méd +3.42% / q90 +5.81%
   - Échelle scale-out : +3.42% (33%) / +5.29% (33%) / +5.81% (34%)
- **DÉSARMER** : repli > **−1.7%** depuis le plus-haut = décay → P(retournement) **63%** (préavis méd 295.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.81% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 89% du temps (retour médian dernière heure +0.38%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 39.1  _(momentum baissier)_
- **ADX** : 22.7  _(pas de tendance nette)_
- **MACD** : hist -0.637  _(pas de croisement recent)_
- **BB** : %B 0.39 · largeur 20.0%
- **ATR** : 9.94 (7.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.125  _(distribution)_
- **Vol ratio** : 0.69  _(volume normal)_
- **Choppiness** : 35.8  _(marche directionnel)_
- **MA** : MA20 256.26 · MA50 274.16 · MA200 314.53  _(prix < MA20)_
- **Dist MA** : MA20 -2.2% · MA50 -8.5% · MA200 -20.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88770 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
