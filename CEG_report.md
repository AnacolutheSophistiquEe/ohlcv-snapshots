# CEG

**Generated** : 2026-07-07T21:55:11.300528+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $239.71  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot $239.71 (+4.4% vs entrée) · entrée $229.58 · stop $226.13 · T1 $232.71 · R/R 0.91  
> ↳ P(T1 av. stop) 51 % · EV/risk -0.065 · ¼-Kelly 0.003 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $228.95–$230.20 (mid $229.58)
- Spot actuel : $239.71 (+4.4% au-dessus de la zone — repli à attendre)
- Stop : $226.13 (stop swing_plan-based (-9.85%))
- Targets : T1 $232.71 · R/R 0.91 | T2 $235.84 · R/R 1.81 | T3 $238.97 · R/R 2.72
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $226.13


## Edge, scénarios & sizing

- EV/risk : -0.065 | EV/share : $-0.223 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 51 % | T2 23 % | T3 9 %
- Kelly (position) : f* 0.013 | ¼-Kelly 0.003 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 68.2 | bear 7.2 | side 24.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=9, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=6, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→66% · +2.0%→38% · +3.0%→22% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.45% (p90 5.51%) · excursion haute méd. +1.5% / basse méd. −1.6%
- Profil de vol intra : ouverture 2.576% vs midi 0.74% vs clôture 0.788% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 50% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.111 ; mean-reverting — autocorr -0.052)_ ; drift intra méd. -0.46% ; recovery-V 15%
- **σ réalisé intraday** 2.444% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 51% / bas 58% / whipsaw 13%
- POC intraday (dernière séance, temps-au-prix) : 243.7369 (VA 242.0456–245.2744 ; dernier close 245.91)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 47% · rebond 63% · **stop −3.25%** sous le fill (sous le bruit) · cible +1.09% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. 0.18% · baisse 44% (gap-down >1% 21% · >2% 9%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −1.68%) · haut méd +0.8% · range méd 1.7%
- Excursion ouverture 15min (n=160) : bas méd −0.82% (p90 −2.26%) · haut méd +1.0% · range méd 2.12%
- Excursion ouverture 30min (n=160) : bas méd −0.9% (p90 −2.92%) · haut méd +1.08% · range méd 2.32%
- Excursion ouverture 60min (n=160) : bas méd −1.09% (p90 −3.15%) · haut méd +1.31% · range méd 2.76%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 245.91 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 72% (119/159) · gap 26% · délai 0.0min · rebond 44% (59/119) (MFE +0.89%)
   - −1.0% : fill 30min 52% · séance 64% (104/159) · gap 21% · délai 1.6min · rebond 51% (58/104) (MFE +1.06%)
   - −1.5% : fill 30min 40% · séance 55% (90/159) · gap 11% · délai 4.1min · rebond 50% (48/90) (MFE +1.0%)
   - −2.0% : fill 30min 31% · séance 47% (70/159) · gap 9% · délai 9.2min · rebond 63% (44/70) (MFE +1.09%)
   - −3.0% : fill 30min 13% · séance 27% (42/159) · gap 3% · délai 36.7min · rebond 39% (17/42) (MFE +0.73%)
   - −4.0% : fill 30min 6% · séance 18% (28/159) · gap 2% · délai 48.4min · rebond 37% (12/28) (MFE +0.6%)
   - −5.0% : fill 30min 4% · séance 11% (19/159) · gap 1% · délai 45.6min · rebond 74% (12/19) (MFE +1.21%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.47% (p90 −1.4%) → stop au-delà de −0.84% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.3% (p90 −1.13%) → stop au-delà de −0.79% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.38% (p90 −1.63%) → stop au-delà de −1.0% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=478 jambes) : jambe baissière méd −1.08% (p90 −2.64%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 100% (56/56) · rebond 50% (34/56)
      · −2.0% : fill 82% (41/56) · rebond 61% (28/41)
      · −3.0% : fill 55% (26/56) · rebond 43% (11/26)
      · −4.0% : fill 40% (19/56) · rebond 34% (8/19)
      · −5.0% : fill 28% (15/56) · rebond 77% (11/15)
   - **flat** (35 séances) :
      · −1.0% : fill 66% (21/35) · rebond 40% (7/21)
      · −2.0% : fill 40% (12/35) · rebond 48% (4/12)
      · −3.0% : fill 27% (10/35) · rebond 28% (4/10)
      · −4.0% : fill 12% (5/35) · rebond 19% (1/5)
      · −5.0% : fill 4% (3/35) · rebond 50% (1/3)
   - **gap-up** (68 séances) :
      · −1.0% : fill 36% (27/68) · rebond 63% (17/27)
      · −2.0% : fill 23% (17/68) · rebond 79% (12/17)
      · −3.0% : fill 7% (6/68) · rebond 32% (2/6)
      · −4.0% : fill 4% (4/68) · rebond 90% (3/4)
      · −5.0% : fill 0% (1/68) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 73% si les 15 1res min sont vertes (89 cas) · 18% si rouges (71 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:24** → P(séance verte=clôture>ouverture) 85% si début vert vs 11% si rouge (base 49% · écart 74 pts) ; prédictivité sature ensuite (plafond brut 194min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **85%** · continue >prix actuel 39% ; creux résiduel méd -0.97% (q20 -1.89%) → **SL/trailing à −1.89%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.83% / q75 +1.71% → **scale +0.83% / runner +1.71%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **11%** (continue à baisser 51%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.85%** (au-delà de la MAE q10 -2.85%), cible rebond +0.9% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.0% .. +2.3%] · haut q95 +2.98% · bas q05 -3.63%
   - 60min (n=160) : retour [-3.83% .. +2.85%] · haut q95 +3.47% · bas q05 -4.65%
   - 2h (n=160) : retour [-4.07% .. +3.11%] · haut q95 +4.22% · bas q05 -5.19%
   - 4h (n=160) : retour [-4.42% .. +3.35%] · haut q95 +5.26% · bas q05 -5.85%
   - 6h (n=160) : retour [-4.81% .. +3.45%] · haut q95 +5.28% · bas q05 -6.84%
   - session (n=160) : retour [-4.34% .. +3.46%] · haut q95 +5.28% · bas q05 -6.84%


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
**Options** : neutral_cautious


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 34.0  _(momentum baissier)_
- **ADX** : 21.2  _(pas de tendance nette)_
- **MACD** : hist -1.794  _(bearish_recent)_
- **BB** : %B 0.16 · largeur 19.6%
- **ATR** : 10.13 (7.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.207  _(distribution)_
- **Vol ratio** : 0.84  _(volume normal)_
- **Choppiness** : 36.5  _(marche directionnel)_
- **MA** : MA20 256.61 · MA50 276.8 · MA200 315.31  _(prix < MA20)_
- **Dist MA** : MA20 -6.6% · MA50 -13.4% · MA200 -24.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (87014 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
