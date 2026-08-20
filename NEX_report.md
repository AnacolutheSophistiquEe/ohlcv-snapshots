# NEX

**Generated** : 2026-08-20T00:05:06.283944+00:00  
**Santé technique** : 5/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €138.30  

> 🟡 **WAIT-FOR-DIP** — spot +6.0 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €138.30 (+6.0% vs entrée) · entrée €130.45 · stop €125.86 · T1 €134.19 · R/R 0.81  
> ↳ P(T1 av. stop) 71 % · EV/risk 0.219 · ¼-Kelly 0.001 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €129.70–€131.19 (mid €130.45)
- Spot actuel : €138.30 (+6.0% au-dessus de la zone — repli à attendre)
- Stop : €125.86 (stop swing_plan-based (-9.0%))
- Targets : T1 €134.19 · R/R 0.81 | T2 €137.94 · R/R 1.63 | T3 €141.69 · R/R 2.45
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €125.86


## Edge, scénarios & sizing

- EV/risk : -0.02 | EV/share : €-0.090 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 50 % | T2 22 % | T3 9 %
- Kelly (position) : f* 0.003 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 24.8 | bear 42.4 | side 32.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 277.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.587% → cible +1.285% / stop −8.0%, p_fill 28%, n_eff≈15.0) : P(cible|rempli) **31%** · **EV/risk +0.002** (×p_fill ; si rempli +0.04% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=8, n_eff=6))
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→65% · +1.0%→51% · +2.0%→28% · +3.0%→14% · +5.0%→5% · +8.0%→1%
- Range intraday médian 3.11% (p90 5.26%) · excursion haute méd. +1.03% / basse méd. −1.48%
- Profil de vol intra : ouverture 1.826% vs midi 0.544% vs clôture 0.761% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (155 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 51% · recovery-V 17%)_
- **Régime intraday** : **chop** _(efficiency 0.113 ; mean-reverting — autocorr -0.033)_ ; drift intra méd. -0.516% ; recovery-V 12%
- **σ réalisé intraday** 2.18% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 74% / whipsaw 26%
- POC intraday (dernière séance, temps-au-prix) : 140.8637 (VA 139.8462–142.0663 ; dernier close 140.1)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 21% · rebond 57% · **stop −1.95%** sous le fill (sous le bruit) · cible +1.55% · R/R 0.79 (high win-rate)
- Gaps overnight (n=154) : méd. 0.17% · baisse 37% (gap-down >1% 8% · >2% 2%)
- Excursion ouverture 5min (n=155) : bas méd −0.47% (p90 −2.03%) · haut méd +0.3% · range méd 1.07%
- Excursion ouverture 15min (n=155) : bas méd −0.59% (p90 −2.16%) · haut méd +0.42% · range méd 1.36%
- Excursion ouverture 30min (n=155) : bas méd −0.6% (p90 −2.32%) · haut méd +0.55% · range méd 1.42%
- Excursion ouverture 60min (n=155) : bas méd −0.84% (p90 −2.59%) · haut méd +0.6% · range méd 1.58%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 140.1 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 72% (110/154) · gap 21% · délai 0.5min · rebond 47% (54/110) (MFE +0.87%)
   - −1.0% : fill 30min 37% · séance 63% (92/154) · gap 8% · délai 12.4min · rebond 45% (43/92) (MFE +0.84%)
   - −1.5% : fill 30min 22% · séance 50% (69/154) · gap 2% · délai 49.0min · rebond 52% (34/69) (MFE +1.05%)
   - −2.0% : fill 30min 14% · séance 32% (50/154) · gap 2% · délai 72.0min · rebond 46% (26/50) (MFE +0.96%)
   - −3.0% : fill 30min 4% · séance 21% (31/154) · gap 1% · délai 115.7min · rebond 57% (18/31) (MFE +1.55%)
   - −4.0% : fill 30min 1% · séance 7% (11/154) · gap 0% · délai 369.3min · rebond 16% (4/11) (MFE +0.77%)
   - −5.0% : fill 30min 0% · séance 2% (4/154) · gap 0% · délai 184.5min · rebond 89% (3/4) (MFE +1.52%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.1% (p90 −1.26%) → stop au-delà de −0.72% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.14% (p90 −1.44%) → stop au-delà de −0.6% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.13% (p90 −0.6%) → stop au-delà de −0.49% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=326 jambes) : jambe baissière méd −1.09% (p90 −2.42%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (46 séances) :
      · −1.0% : fill 76% (37/46) · rebond 40% (15/37)
      · −2.0% : fill 39% (25/46) · rebond 43% (13/25)
      · −3.0% : fill 27% (16/46) · rebond 47% (9/16)
      · −4.0% : fill 13% (7/46) · rebond 28% (3/7)
      · −5.0% : fill 7% (4/46) · rebond 89% (3/4)
   - **flat** (37 séances) :
      · −1.0% : fill 65% (24/37) · rebond 49% (13/24)
      · −2.0% : fill 38% (12/37) · rebond 51% (6/12)
      · −3.0% : fill 28% (8/37) · rebond 46% (3/8)
      · −4.0% : fill 9% (2/37) · rebond 0% (0/2)
      · −5.0% : fill 0% (0/37) · rebond 0% (0/0)
   - **gap-up** (71 séances) :
      · −1.0% : fill 55% (31/71) · rebond 47% (15/31)
      · −2.0% : fill 26% (13/71) · rebond 45% (7/13)
      · −3.0% : fill 14% (7/71) · rebond 82% (6/7)
      · −4.0% : fill 3% (2/71) · rebond 15% (1/2)
      · −5.0% : fill 0% (0/71) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=155) : 42% en base · 64% si les 15 1res min sont vertes (83 cas) · 18% si rouges (72 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=155) : COUDE à **29min** → P(séance verte=clôture>ouverture) 70% si début vert vs 18% si rouge (base 42% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 306min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **70%** · continue >prix actuel 50% ; creux résiduel méd -1.01% (q20 -2.07%) → **SL/trailing à −2.07%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.0% / q75 +1.59% → **scale +1.0% / runner +1.59%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **18%** (continue à baisser 58%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.25%** (au-delà de la MAE q10 -3.25%), cible rebond +0.96% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=155) : retour [-2.03% .. +2.32%] · haut q95 +2.71% · bas q05 -2.59%
   - 60min (n=155) : retour [-2.82% .. +2.77%] · haut q95 +2.94% · bas q05 -3.24%
   - 2h (n=155) : retour [-3.58% .. +2.51%] · haut q95 +2.95% · bas q05 -3.74%
   - 4h (n=155) : retour [-3.32% .. +2.6%] · haut q95 +3.28% · bas q05 -3.93%
   - 6h (n=155) : retour [-3.81% .. +3.56%] · haut q95 +4.11% · bas q05 -4.18%
   - session (n=155) : retour [-3.56% .. +2.99%] · haut q95 +4.18% · bas q05 -4.72%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.94%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 63.9  _(momentum haussier)_
- **ADX** : 18.9  _(pas de tendance nette)_
- **MACD** : hist 0.74  _(pas de croisement recent)_
- **BB** : %B 0.62 · largeur 15.7%
- **ATR** : 4.59 (69.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.175  _(distribution)_
- **Vol ratio** : 0.3  _(volume atone)_
- **Choppiness** : 44.2  _(transition)_
- **MA** : MA20 135.81 · MA50 139.77 · MA200 132.82  _(prix > MA20)_
- **Dist MA** : MA20 +1.8% · MA50 -1.1% · MA200 +4.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (106593 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
