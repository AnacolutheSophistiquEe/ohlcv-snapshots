# SOFI

**Generated** : 2026-08-11T00:33:00.715833+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $18.12  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot $18.12 (+7.2% vs entrée) · entrée $16.91 · stop $15.99 · T1 $18.75 · R/R 2.0  
> ↳ P(T1 av. stop) 25 % · EV/risk 0.03 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $16.73–$17.08 (mid $16.91)
- Spot actuel : $18.12 (+7.2% au-dessus de la zone — repli à attendre)
- Stop : $15.99 (stop swing_plan-based (-11.76%))
- Targets : T1 $18.75 · R/R 2.0 | T2 $19.15 · R/R 2.43 | T3 $19.55 · R/R 2.87
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $15.99


## Edge, scénarios & sizing

- EV/risk : -0.106 | EV/share : $-0.098 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 18 % | T2 10 % | T3 7 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 65.5 | bear 18.6 | side 15.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 272.0 (= 15 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.04% → cible +4.537% / stop −2.269%, p_fill 27%, n_eff≈14.4) : P(cible|rempli) **14%** · **EV/risk +0.130** (×p_fill ; si rempli +1.09% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=7, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=7, n_eff=4))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→69% · +2.0%→49% · +3.0%→36% · +5.0%→11% · +8.0%→1%
- Range intraday médian 4.39% (p90 7.29%) · excursion haute méd. +1.9% / basse méd. −2.21%
- Profil de vol intra : ouverture 3.018% vs midi 0.901% vs clôture 1.006% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 16% · trend ↑2%/↓0% ; spike-down 65% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.145 ; mean-reverting — autocorr -0.047)_ ; drift intra méd. 0.355% ; recovery-V 19%
- **σ réalisé intraday** 2.843% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 61% / bas 57% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 18.1863 (VA 18.1112–18.2863 ; dernier close 18.38)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 51% · rebond 70% · **stop −2.97%** sous le fill (sous le bruit) · cible +1.89% · R/R 0.64 (high win-rate)
- Gaps overnight (n=159) : méd. 0.22% · baisse 44% (gap-down >1% 27% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −1.7%) · haut méd +0.74% · range méd 1.67%
- Excursion ouverture 15min (n=160) : bas méd −1.07% (p90 −2.93%) · haut méd +0.99% · range méd 2.31%
- Excursion ouverture 30min (n=160) : bas méd −1.19% (p90 −3.31%) · haut méd +1.16% · range méd 2.77%
- Excursion ouverture 60min (n=160) : bas méd −1.49% (p90 −3.78%) · haut méd +1.3% · range méd 3.43%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 18.38 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 72% (121/159) · gap 32% · délai 0.0min · rebond 54% (65/121) (MFE +1.21%)
   - −1.0% : fill 30min 54% · séance 66% (111/159) · gap 27% · délai 0.6min · rebond 63% (69/111) (MFE +1.32%)
   - −1.5% : fill 30min 48% · séance 62% (102/159) · gap 20% · délai 6.7min · rebond 66% (65/102) (MFE +1.58%)
   - −2.0% : fill 30min 38% · séance 51% (79/159) · gap 11% · délai 3.3min · rebond 70% (54/79) (MFE +1.89%)
   - −3.0% : fill 30min 17% · séance 36% (58/159) · gap 4% · délai 31.4min · rebond 66% (40/58) (MFE +1.57%)
   - −4.0% : fill 30min 10% · séance 22% (39/159) · gap 3% · délai 41.0min · rebond 57% (25/39) (MFE +1.46%)
   - −5.0% : fill 30min 4% · séance 9% (18/159) · gap 2% · délai 26.7min · rebond 40% (10/18) (MFE +0.71%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.41% (p90 −1.93%) → stop au-delà de −1.25% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.47% (p90 −1.71%) → stop au-delà de −1.29% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −1.71%) → stop au-delà de −1.06% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=658 jambes) : jambe baissière méd −1.11% (p90 −2.78%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (65 séances) :
      · −1.0% : fill 97% (64/65) · rebond 62% (40/64)
      · −2.0% : fill 86% (55/65) · rebond 73% (40/55)
      · −3.0% : fill 68% (44/65) · rebond 73% (33/44)
      · −4.0% : fill 40% (29/65) · rebond 65% (21/29)
      · −5.0% : fill 20% (14/65) · rebond 38% (8/14)
   - **flat** (22 séances) :
      · −1.0% : fill 54% (13/22) · rebond 45% (6/13)
      · −2.0% : fill 40% (8/22) · rebond 58% (4/8)
      · −3.0% : fill 34% (6/22) · rebond 57% (3/6)
      · −4.0% : fill 15% (3/22) · rebond 67% (1/3)
      · −5.0% : fill 1% (1/22) · rebond 0% (0/1)
   - **gap-up** (72 séances) :
      · −1.0% : fill 43% (34/72) · rebond 70% (23/34)
      · −2.0% : fill 25% (16/72) · rebond 66% (10/16)
      · −3.0% : fill 10% (8/72) · rebond 39% (4/8)
      · −4.0% : fill 8% (7/72) · rebond 20% (3/7)
      · −5.0% : fill 1% (3/72) · rebond 70% (2/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 59% si les 15 1res min sont vertes (72 cas) · 28% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 79% si début vert vs 12% si rouge (base 43% · écart 67 pts) ; prédictivité sature ensuite (plafond brut 228min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=69) : tient le vert **79%** · continue >prix actuel 55% ; creux résiduel méd -1.51% (q20 -2.82%) → **SL/trailing à −2.82%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.9% / q75 +2.85% → **scale +1.9% / runner +2.85%**, sortie à la clôture
  - **si ROUGE au coude** (n=91) : edge inversé — récupère vert seulement **12%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.08%** (au-delà de la MAE q10 -3.08%), cible rebond +1.13% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.88% .. +3.65%] · haut q95 +4.01% · bas q05 -3.56%
   - 60min (n=160) : retour [-3.12% .. +3.67%] · haut q95 +4.45% · bas q05 -4.0%
   - 2h (n=160) : retour [-3.58% .. +3.81%] · haut q95 +5.03% · bas q05 -4.57%
   - 4h (n=160) : retour [-3.79% .. +4.87%] · haut q95 +5.75% · bas q05 -5.04%
   - 6h (n=160) : retour [-4.56% .. +4.51%] · haut q95 +6.54% · bas q05 -5.08%
   - session (n=160) : retour [-4.48% .. +5.56%] · haut q95 +6.63% · bas q05 -5.14%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (4) pour des stats fiables : 2.5% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.93%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 52.9  _(neutre)_
- **ADX** : 15.9  _(pas de tendance nette)_
- **MACD** : hist 0.168  _(pas de croisement recent)_
- **BB** : %B 0.71 · largeur 20.8%
- **ATR** : 0.85 (14.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.002  _(neutre)_
- **Vol ratio** : 0.47  _(volume atone)_
- **Choppiness** : 41.5  _(transition)_
- **MA** : MA20 17.35 · MA50 17.46 · MA200 21.03  _(prix > MA20)_
- **Dist MA** : MA20 +4.4% · MA50 +3.8% · MA200 -13.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (84816 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
