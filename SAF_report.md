# SAF

**Generated** : 2026-07-17T00:07:16.407001+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €328.10  

> 🟡 **WAIT-FOR-DIP** — spot +2.8 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €328.10 (+2.8% vs entrée) · entrée €319.08 · stop €312.70 · T1 €322.42 · R/R 0.52  
> ↳ P(T1 av. stop) 57 % · EV/risk 0.033 · ¼-Kelly 0.019 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €318.42–€319.75 (mid €319.08)
- Spot actuel : €328.10 (+2.8% au-dessus de la zone — repli à attendre)
- Stop : €312.70 (stop swing_plan-based (-7.14%))
- Targets : T1 €322.42 · R/R 0.52 | T2 €325.75 · R/R 1.05 | T3 €329.08 · R/R 1.57
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €312.70


## Edge, scénarios & sizing

- EV/risk : 0.033 | EV/share : €0.213 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 57 % | T2 35 % | T3 14 %
- Kelly (position) : f* 0.077 | ¼-Kelly 0.019 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.4 | bear 9.5 | side 85.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=13, n_eff=5))
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→71% · +1.0%→57% · +2.0%→38% · +3.0%→15% · +5.0%→4% · +8.0%→1%
- Range intraday médian 2.7% (p90 4.55%) · excursion haute méd. +1.52% / basse méd. −0.95%
- Profil de vol intra : ouverture 1.622% vs midi 0.617% vs clôture 0.754% _(ouverture ~2.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (150 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 39% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; mean-reverting — autocorr -0.06)_ ; drift intra méd. 0.205% ; recovery-V 33%
- **σ réalisé intraday** 1.765% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 68% / bas 55% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 325.3769 (VA 324.6719–327.1394 ; dernier close 329.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 20% · rebond 49% · **stop −1.79%** sous le fill (sous le bruit) · cible +0.95% · R/R 0.53 (high win-rate)
- Gaps overnight (n=149) : méd. -0.08% · baisse 53% (gap-down >1% 12% · >2% 2%)
- Excursion ouverture 5min (n=150) : bas méd −0.4% (p90 −1.5%) · haut méd +0.22% · range méd 0.92%
- Excursion ouverture 15min (n=150) : bas méd −0.51% (p90 −1.62%) · haut méd +0.43% · range méd 1.18%
- Excursion ouverture 30min (n=150) : bas méd −0.55% (p90 −1.75%) · haut méd +0.54% · range méd 1.28%
- Excursion ouverture 60min (n=150) : bas méd −0.71% (p90 −1.91%) · haut méd +0.61% · range méd 1.5%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 329.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 67% (105/149) · gap 28% · délai 0.2min · rebond 36% (38/105) (MFE +0.73%)
   - −1.0% : fill 30min 44% · séance 53% (77/149) · gap 12% · délai 0.4min · rebond 42% (28/77) (MFE +0.61%)
   - −1.5% : fill 30min 30% · séance 45% (66/149) · gap 4% · délai 12.4min · rebond 37% (22/66) (MFE +0.87%)
   - −2.0% : fill 30min 13% · séance 35% (48/149) · gap 2% · délai 54.2min · rebond 41% (20/48) (MFE +0.74%)
   - −3.0% : fill 30min 4% · séance 20% (28/149) · gap 1% · délai 202.9min · rebond 49% (16/28) (MFE +0.95%)
   - −4.0% : fill 30min 2% · séance 9% (13/149) · gap 0% · délai 126.9min · rebond 62% (7/13) (MFE +1.25%)
   - −5.0% : fill 30min 0% · séance 1% (3/149) · gap 0% · délai 360.2min · rebond 31% (1/3) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.24% (p90 −0.91%) → stop au-delà de −0.76% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −0.91%) → stop au-delà de −0.69% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=176 jambes) : jambe baissière méd −1.09% (p90 −2.63%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 81% (43/54) · rebond 39% (16/43)
      · −2.0% : fill 61% (31/54) · rebond 44% (14/31)
      · −3.0% : fill 32% (17/54) · rebond 50% (9/17)
      · −4.0% : fill 17% (9/54) · rebond 69% (5/9)
      · −5.0% : fill 2% (2/54) · rebond 0% (0/2)
   - **flat** (41 séances) :
      · −1.0% : fill 44% (17/41) · rebond 68% (9/17)
      · −2.0% : fill 15% (7/41) · rebond 50% (3/7)
      · −3.0% : fill 8% (4/41) · rebond 69% (3/4)
      · −4.0% : fill 2% (1/41) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/41) · rebond 0% (0/0)
   - **gap-up** (54 séances) :
      · −1.0% : fill 26% (17/54) · rebond 21% (3/17)
      · −2.0% : fill 18% (10/54) · rebond 24% (3/10)
      · −3.0% : fill 15% (7/54) · rebond 36% (4/7)
      · −4.0% : fill 6% (3/54) · rebond 30% (1/3)
      · −5.0% : fill 1% (1/54) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=150) : 54% en base · 72% si les 15 1res min sont vertes (67 cas) · 36% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=150) : COUDE à **44min** → P(séance verte=clôture>ouverture) 82% si début vert vs 29% si rouge (base 54% · écart 53 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=67) : tient le vert **82%** · continue >prix actuel 64% ; creux résiduel méd -0.57% (q20 -1.41%) → **SL/trailing à −1.41%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.32% / q75 +1.78% → **scale +1.32% / runner +1.78%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **29%** (continue à baisser 49%) → **RÉDUIRE ~71%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.58%** (au-delà de la MAE q10 -2.58%), cible rebond +0.87% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=150) : retour [-1.59% .. +1.58%] · haut q95 +1.94% · bas q05 -2.24%
   - 60min (n=150) : retour [-1.66% .. +2.17%] · haut q95 +2.72% · bas q05 -2.37%
   - 2h (n=150) : retour [-2.29% .. +2.2%] · haut q95 +2.9% · bas q05 -2.96%
   - 4h (n=150) : retour [-2.28% .. +2.19%] · haut q95 +3.35% · bas q05 -3.14%
   - 6h (n=150) : retour [-2.34% .. +3.06%] · haut q95 +3.49% · bas q05 -3.44%
   - session (n=150) : retour [-3.47% .. +3.28%] · haut q95 +3.76% · bas q05 -4.01%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 2.0% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.66%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 46.9  _(neutre)_
- **ADX** : 22.9  _(pas de tendance nette)_
- **MACD** : hist -3.833  _(pas de croisement recent)_
- **BB** : %B 0.22 · largeur 11.5%
- **ATR** : 8.85 (62.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF 0.137  _(accumulation)_
- **Vol ratio** : 0.44  _(volume atone)_
- **Choppiness** : 44.1  _(transition)_
- **MA** : MA20 338.88 · MA50 311.91 · MA200 303.37  _(prix < MA20)_
- **Dist MA** : MA20 -3.2% · MA50 +5.2% · MA200 +8.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88251 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
