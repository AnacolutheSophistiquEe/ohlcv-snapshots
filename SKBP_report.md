# 326030

**Generated** : 2026-07-19T20:53:17.043326+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩79400.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot ₩79400.00 (+6.4% vs entrée) · entrée ₩74592.86 · stop ₩73150.71 · T1 ₩76261.06 · R/R 1.16  
> ↳ P(T1 av. stop) 34 % · EV/risk -0.168 · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.93% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩74259.22–₩74926.50 (mid ₩74592.86)
- Spot actuel : ₩79400.00 (+6.4% au-dessus de la zone — repli à attendre)
- Stop : ₩73150.71 (stop swing_plan-based (-14.31%))
- Targets : T1 ₩76261.06 · R/R 1.16 | T2 ₩77929.26 · R/R 2.31 | T3 ₩79597.47 · R/R 3.47
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩73150.71


## Edge, scénarios & sizing

- EV/risk : -0.168 | EV/share : ₩-242.879 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 9 % | T3 6 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 11.0 | bear 57.7 | side 31.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=4, n_eff=2))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→72% · +1.0%→61% · +2.0%→42% · +3.0%→26% · +5.0%→9% · +8.0%→4%
- Range intraday médian 4.08% (p90 7.23%) · excursion haute méd. +1.55% / basse méd. −2.12%
- Profil de vol intra : ouverture 2.613% vs midi 0.759% vs clôture 0.784% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (135 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 16% · trend ↑2%/↓2% ; spike-down 59% · recovery-V 20%)_
- **Régime intraday** : **chop** _(efficiency 0.134 ; mean-reverting — autocorr -0.046)_ ; drift intra méd. -0.482% ; recovery-V 24%
- **σ réalisé intraday** 3.361% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 67% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 78842.5 (VA 78162.5–80457.5 ; dernier close 79100.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 16% · rebond 81% · **stop −2.91%** sous le fill (sous le bruit) · cible +1.92% · R/R 0.66 (high win-rate)
- Gaps overnight (n=134) : méd. 0.1% · baisse 42% (gap-down >1% 16% · >2% 8%)
- Excursion ouverture 5min (n=135) : bas méd −0.77% (p90 −2.17%) · haut méd +0.66% · range méd 1.86%
- Excursion ouverture 15min (n=135) : bas méd −0.91% (p90 −2.95%) · haut méd +0.72% · range méd 2.19%
- Excursion ouverture 30min (n=135) : bas méd −1.08% (p90 −2.98%) · haut méd +0.88% · range méd 2.52%
- Excursion ouverture 60min (n=135) : bas méd −1.24% (p90 −3.28%) · haut méd +1.17% · range méd 2.93%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 79100.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 79% (98/134) · gap 25% · délai 0.4min · rebond 51% (41/98) (MFE +1.18%)
   - −1.0% : fill 30min 55% · séance 69% (88/134) · gap 16% · délai 2.2min · rebond 53% (41/88) (MFE +1.01%)
   - −1.5% : fill 30min 40% · séance 56% (67/134) · gap 8% · délai 3.8min · rebond 56% (33/67) (MFE +1.11%)
   - −2.0% : fill 30min 28% · séance 49% (56/134) · gap 8% · délai 16.9min · rebond 63% (31/56) (MFE +1.25%)
   - −3.0% : fill 30min 11% · séance 35% (36/134) · gap 4% · délai 81.8min · rebond 54% (15/36) (MFE +1.15%)
   - −4.0% : fill 30min 8% · séance 23% (25/134) · gap 3% · délai 112.9min · rebond 54% (12/25) (MFE +1.03%)
   - −5.0% : fill 30min 6% · séance 16% (19/134) · gap 3% · délai 118.4min · rebond 81% (12/19) (MFE +1.92%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.41% (p90 −2.75%) → stop au-delà de −1.25% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.73% (p90 −1.92%) → stop au-delà de −1.4% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.73% (p90 −2.23%) → stop au-delà de −1.41% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=433 jambes) : jambe baissière méd −1.15% (p90 −2.5%) · ~8.9 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (40 séances) :
      · −1.0% : fill 100% (40/40) · rebond 63% (21/40)
      · −2.0% : fill 72% (28/40) · rebond 61% (14/28)
      · −3.0% : fill 48% (18/40) · rebond 49% (7/18)
      · −4.0% : fill 40% (15/40) · rebond 65% (8/15)
      · −5.0% : fill 31% (12/40) · rebond 85% (8/12)
   - **flat** (34 séances) :
      · −1.0% : fill 70% (24/34) · rebond 30% (8/24)
      · −2.0% : fill 55% (17/34) · rebond 70% (11/17)
      · −3.0% : fill 41% (10/34) · rebond 66% (5/10)
      · −4.0% : fill 35% (8/34) · rebond 39% (3/8)
      · −5.0% : fill 25% (6/34) · rebond 79% (4/6)
   - **gap-up** (60 séances) :
      · −1.0% : fill 46% (24/60) · rebond 58% (12/24)
      · −2.0% : fill 28% (11/60) · rebond 56% (6/11)
      · −3.0% : fill 21% (8/60) · rebond 47% (3/8)
      · −4.0% : fill 3% (2/60) · rebond 71% (1/2)
      · −5.0% : fill 1% (1/60) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=135) : 38% en base · 70% si les 15 1res min sont vertes (48 cas) · 16% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=135) : COUDE à **1:38** → P(séance verte=clôture>ouverture) 76% si début vert vs 7% si rouge (base 38% · écart 69 pts) ; prédictivité sature ensuite (plafond brut 195min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=54) : tient le vert **76%** · continue >prix actuel 47% ; creux résiduel méd -1.44% (q20 -2.19%) → **SL/trailing à −2.19%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.35% / q75 +2.0% → **scale +1.35% / runner +2.0%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **7%** (continue à baisser 61%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.03%** (au-delà de la MAE q10 -4.03%), cible rebond +0.73% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=135) : retour [-2.82% .. +2.48%] · haut q95 +3.66% · bas q05 -4.05%
   - 60min (n=135) : retour [-3.83% .. +2.56%] · haut q95 +4.26% · bas q05 -4.54%
   - 2h (n=135) : retour [-3.49% .. +3.93%] · haut q95 +4.52% · bas q05 -4.71%
   - 4h (n=135) : retour [-4.25% .. +5.29%] · haut q95 +6.3% · bas q05 -5.81%
   - 6h (n=135) : retour [-4.68% .. +4.28%] · haut q95 +7.09% · bas q05 -6.02%
   - session (n=135) : retour [-4.78% .. +4.72%] · haut q95 +7.09% · bas q05 -6.06%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 326030 = **plat / peu volatil** (vol intra méd 2.3%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-3 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-3 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 45.1  _(neutre)_
- **ADX** : 14.0  _(pas de tendance nette)_
- **MACD** : hist -474.457  _(pas de croisement recent)_
- **BB** : %B 0.23 · largeur 19.1%
- **ATR** : 4807.14 (68.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.11  _(distribution)_
- **Vol ratio** : 0.61  _(volume normal)_
- **Choppiness** : 51.7  _(transition)_
- **MA** : MA20 83755.0 · MA50 89394.0 · MA200 107494.0  _(prix < MA20)_
- **Dist MA** : MA20 -5.2% · MA50 -11.2% · MA200 -26.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (80990 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
