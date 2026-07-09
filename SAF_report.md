# SAF

**Generated** : 2026-07-09T00:07:12.544322+00:00  
**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €331.70  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot €331.70 (+7.2% vs entrée) · entrée €309.28 · stop €305.13 · T1 €317.57 · R/R 2.0  
> ↳ P(T1 av. stop) 35 % · EV/risk 0.128 · ¼-Kelly 0.006 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €307.62–€310.94 (mid €309.28)
- Spot actuel : €331.70 (+7.2% au-dessus de la zone — repli à attendre)
- Stop : €305.13 (stop swing_plan-based (-8.01%))
- Targets : T1 €317.57 · R/R 2.0 | T2 €325.86 · R/R 4.0 | T3 €334.16 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €305.13


## Edge, scénarios & sizing

- EV/risk : 0.128 | EV/share : €0.531 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 15 % | T3 10 %
- Kelly (position) : f* 0.024 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 11.4 | side 83.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 332.0 (= 1 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=11, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=4, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→60% · +2.0%→39% · +3.0%→16% · +5.0%→5% · +8.0%→2%
- Range intraday médian 2.77% (p90 4.93%) · excursion haute méd. +1.52% / basse méd. −0.95%
- Profil de vol intra : ouverture 1.644% vs midi 0.659% vs clôture 0.765% _(ouverture ~2.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (144 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 33% · recovery-V 18%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; mean-reverting — autocorr -0.037)_ ; drift intra méd. 0.455% ; recovery-V 23%
- **σ réalisé intraday** 1.786% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 72% / bas 47% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 352.7675 (VA 352.4325–355.4475 ; dernier close 347.2)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 20% · rebond 53% · **stop −1.55%** sous le fill (sous le bruit) · cible +1.2% · R/R 0.77 (high win-rate)
- Gaps overnight (n=143) : méd. -0.06% · baisse 51% (gap-down >1% 13% · >2% 2%)
- Excursion ouverture 5min (n=144) : bas méd −0.33% (p90 −1.47%) · haut méd +0.31% · range méd 0.92%
- Excursion ouverture 15min (n=144) : bas méd −0.37% (p90 −1.5%) · haut méd +0.5% · range méd 1.18%
- Excursion ouverture 30min (n=144) : bas méd −0.46% (p90 −1.67%) · haut méd +0.58% · range méd 1.29%
- Excursion ouverture 60min (n=144) : bas méd −0.66% (p90 −1.81%) · haut méd +0.69% · range méd 1.49%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 347.2 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 55% · séance 64% (100/143) · gap 28% · délai 0.2min · rebond 38% (37/100) (MFE +0.78%)
   - −1.0% : fill 30min 41% · séance 49% (72/143) · gap 13% · délai 0.4min · rebond 43% (26/72) (MFE +0.62%)
   - −1.5% : fill 30min 26% · séance 41% (61/143) · gap 5% · délai 7.6min · rebond 36% (20/61) (MFE +0.89%)
   - −2.0% : fill 30min 13% · séance 31% (44/143) · gap 2% · délai 53.9min · rebond 45% (19/44) (MFE +0.86%)
   - −3.0% : fill 30min 4% · séance 20% (27/143) · gap 1% · délai 218.0min · rebond 53% (16/27) (MFE +1.2%)
   - −4.0% : fill 30min 3% · séance 8% (12/143) · gap 0% · délai 153.7min · rebond 53% (6/12) (MFE +1.49%)
   - −5.0% : fill 30min 0% · séance 2% (3/143) · gap 0% · délai 360.2min · rebond 31% (1/3) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.19% (p90 −0.92%) → stop au-delà de −0.76% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −0.91%) → stop au-delà de −0.69% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=167 jambes) : jambe baissière méd −1.07% (p90 −2.72%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 77% (39/50) · rebond 43% (15/39)
      · −2.0% : fill 53% (27/50) · rebond 51% (13/27)
      · −3.0% : fill 33% (16/50) · rebond 58% (9/16)
      · −4.0% : fill 15% (8/50) · rebond 59% (4/8)
      · −5.0% : fill 3% (2/50) · rebond 0% (0/2)
   - **flat** (40 séances) :
      · −1.0% : fill 39% (16/40) · rebond 62% (8/16)
      · −2.0% : fill 17% (7/40) · rebond 50% (3/7)
      · −3.0% : fill 8% (4/40) · rebond 69% (3/4)
      · −4.0% : fill 2% (1/40) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/40) · rebond 0% (0/0)
   - **gap-up** (53 séances) :
      · −1.0% : fill 27% (17/53) · rebond 21% (3/17)
      · −2.0% : fill 19% (10/53) · rebond 24% (3/10)
      · −3.0% : fill 15% (7/53) · rebond 36% (4/7)
      · −4.0% : fill 7% (3/53) · rebond 30% (1/3)
      · −5.0% : fill 1% (1/53) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=144) : 55% en base · 72% si les 15 1res min sont vertes (66 cas) · 35% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=144) : COUDE à **44min** → P(séance verte=clôture>ouverture) 81% si début vert vs 26% si rouge (base 55% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=66) : tient le vert **81%** · continue >prix actuel 63% ; creux résiduel méd -0.56% (q20 -1.41%) → **SL/trailing à −1.41%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.29% / q75 +1.83% → **scale +1.29% / runner +1.83%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **26%** (continue à baisser 47%) → **RÉDUIRE ~74%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.45%** (au-delà de la MAE q10 -2.45%), cible rebond +0.92% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=144) : retour [-1.72% .. +1.65%] · haut q95 +1.99% · bas q05 -2.27%
   - 60min (n=144) : retour [-1.76% .. +2.26%] · haut q95 +2.83% · bas q05 -2.47%
   - 2h (n=144) : retour [-2.08% .. +2.25%] · haut q95 +3.38% · bas q05 -2.9%
   - 4h (n=144) : retour [-2.14% .. +2.35%] · haut q95 +3.43% · bas q05 -2.98%
   - 6h (n=144) : retour [-2.15% .. +3.33%] · haut q95 +3.6% · bas q05 -3.05%
   - session (n=144) : retour [-3.31% .. +3.61%] · haut q95 +3.98% · bas q05 -4.01%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 2.1% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.66%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 48.9  _(neutre)_
- **ADX** : 32.6  _(tendance etablie)_
- **MACD** : hist -0.849  _(bearish_recent)_
- **BB** : %B 0.46 · largeur 19.3%
- **ATR** : 8.77 (63.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.097  _(accumulation)_
- **Vol ratio** : 0.56  _(volume atone)_
- **Choppiness** : 48.3  _(transition)_
- **MA** : MA20 334.16 · MA50 305.08 · MA200 302.18  _(prix < MA20)_
- **Dist MA** : MA20 -0.7% · MA50 +8.7% · MA200 +9.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90825 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
