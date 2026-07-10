# AL2SI

**Generated** : 2026-07-10T21:46:38.245195+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 15.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Buy  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €30.70  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)  
> ↳ spot €30.70 (+22.2% vs entrée) · entrée €25.13 · stop €22.11 · T1 €33.02 · R/R 2.61  
> ↳ P(T1 av. stop) 10 % · EV/risk 0.379 · ¼-Kelly 0.002 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Buy'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €24.42–€25.83 (mid €25.13)
- Spot actuel : €30.70 (+22.2% au-dessus de la zone — repli à attendre)
- Stop : €22.11 (stop swing_plan-based (-27.98%))
- Targets : T1 €33.02 · R/R 2.61 | T2 €35.02 · R/R 3.27 | T3 €39.79 · R/R 4.85
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €22.11


## Edge, scénarios & sizing

- EV/risk : 0.379 | EV/share : €1.143 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 10 % | T2 6 % | T3 1 %
- Kelly (position) : f* 0.006 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 31.2 | bear 5.0 | side 63.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 276.0 (= 9 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=7, n_eff=6))
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=4, n_eff=4))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→81% · +2.0%→75% · +3.0%→65% · +5.0%→42% · +8.0%→24%
- Range intraday médian 8.23% (p90 20.17%) · excursion haute méd. +4.23% / basse méd. −3.23%
- Profil de vol intra : ouverture 5.692% vs midi 1.679% vs clôture 1.974% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (144 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 11% · trend ↑0%/↓2% ; spike-down 74% · recovery-V 37%)_
- **Régime intraday** : **chop** _(efficiency 0.163 ; neutre — autocorr -0.015)_ ; drift intra méd. 0.425% ; recovery-V 32%
- **σ réalisé intraday** 8.554% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 66% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 32.8275 (VA 29.1045–36.5505 ; dernier close 32.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 39% · rebond 89% · **stop −7.17%** sous le fill (sous le bruit) · cible +2.37% · R/R 0.33 (high win-rate)
- Gaps overnight (n=143) : méd. 0.23% · baisse 36% (gap-down >1% 21% · >2% 8%)
- Excursion ouverture 5min (n=144) : bas méd −1.1% (p90 −5.28%) · haut méd +1.04% · range méd 3.05%
- Excursion ouverture 15min (n=144) : bas méd −1.55% (p90 −6.27%) · haut méd +1.54% · range méd 4.45%
- Excursion ouverture 30min (n=144) : bas méd −1.61% (p90 −6.69%) · haut méd +2.03% · range méd 4.86%
- Excursion ouverture 60min (n=144) : bas méd −2.24% (p90 −7.47%) · haut méd +2.53% · range méd 5.76%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 32.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 79% (110/143) · gap 28% · délai 0.3min · rebond 67% (73/110) (MFE +3.01%)
   - −1.0% : fill 30min 59% · séance 77% (105/143) · gap 21% · délai 0.4min · rebond 74% (74/105) (MFE +2.62%)
   - −1.5% : fill 30min 50% · séance 71% (95/143) · gap 12% · délai 1.5min · rebond 69% (62/95) (MFE +1.84%)
   - −2.0% : fill 30min 43% · séance 62% (82/143) · gap 8% · délai 3.1min · rebond 69% (55/82) (MFE +1.88%)
   - −3.0% : fill 30min 30% · séance 52% (66/143) · gap 6% · délai 9.0min · rebond 81% (54/66) (MFE +2.37%)
   - −4.0% : fill 30min 25% · séance 44% (56/143) · gap 5% · délai 13.6min · rebond 74% (43/56) (MFE +2.67%)
   - −5.0% : fill 30min 20% · séance 39% (48/143) · gap 5% · délai 18.7min · rebond 89% (45/48) (MFE +2.37%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.91% (p90 −5.63%) → stop au-delà de −3.2% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.95% (p90 −5.7%) → stop au-delà de −4.21% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.89% (p90 −5.86%) → stop au-delà de −3.81% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1368 jambes) : jambe baissière méd −1.25% (p90 −3.4%) · ~19.5 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 98% (46/50) · rebond 68% (31/46)
      · −2.0% : fill 85% (39/50) · rebond 56% (24/39)
      · −3.0% : fill 82% (35/50) · rebond 76% (28/35)
      · −4.0% : fill 69% (30/50) · rebond 71% (24/30)
      · −5.0% : fill 60% (27/50) · rebond 77% (24/27)
   - **flat** (30 séances) :
      · −1.0% : fill 81% (23/30) · rebond 79% (18/23)
      · −2.0% : fill 64% (17/30) · rebond 86% (13/17)
      · −3.0% : fill 42% (11/30) · rebond 92% (10/11)
      · −4.0% : fill 42% (11/30) · rebond 94% (10/11)
      · −5.0% : fill 34% (9/30) · rebond 100% (9/9)
   - **gap-up** (63 séances) :
      · −1.0% : fill 60% (36/63) · rebond 77% (25/36)
      · −2.0% : fill 45% (26/63) · rebond 75% (18/26)
      · −3.0% : fill 35% (20/63) · rebond 85% (16/20)
      · −4.0% : fill 28% (15/63) · rebond 64% (9/15)
      · −5.0% : fill 27% (12/63) · rebond 100% (12/12)
- **P(clôture VERTE) selon le drive 15min** (n=144) : 50% en base · 69% si les 15 1res min sont vertes (69 cas) · 35% si rouges (75 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=144) : COUDE à **31min** → P(séance verte=clôture>ouverture) 76% si début vert vs 25% si rouge (base 50% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 241min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **76%** · continue >prix actuel 59% ; creux résiduel méd -2.06% (q20 -4.49%) → **SL/trailing à −4.49%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.7% / q75 +6.09% → **scale +3.7% / runner +6.09%**, sortie à la clôture
  - **si ROUGE au coude** (n=72) : edge inversé — récupère vert seulement **25%** (continue à baisser 61%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −13.96%** (au-delà de la MAE q10 -13.96%), cible rebond +2.37% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=144) : retour [-5.42% .. +8.77%] · haut q95 +9.62% · bas q05 -7.83%
   - 60min (n=144) : retour [-6.07% .. +10.36%] · haut q95 +10.46% · bas q05 -8.98%
   - 2h (n=144) : retour [-6.1% .. +10.42%] · haut q95 +10.92% · bas q05 -9.55%
   - 4h (n=144) : retour [-11.96% .. +12.35%] · haut q95 +13.66% · bas q05 -13.23%
   - 6h (n=144) : retour [-10.72% .. +15.12%] · haut q95 +20.5% · bas q05 -15.71%
   - session (n=144) : retour [-10.79% .. +21.13%] · haut q95 +22.69% · bas q05 -16.99%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.28%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 63.0  _(momentum haussier)_
- **ADX** : 22.0  _(pas de tendance nette)_
- **MACD** : hist 0.277  _(pas de croisement recent)_
- **BB** : %B 0.42 · largeur 91.8%
- **ATR** : 5.03 (91.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.009  _(neutre)_
- **Vol ratio** : 0.39  _(volume atone)_
- **Choppiness** : 54.0  _(transition)_
- **MA** : MA20 33.22 · MA50 40.49 · MA200 23.68  _(prix < MA20)_
- **Dist MA** : MA20 -7.6% · MA50 -24.2% · MA200 +29.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92380 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
