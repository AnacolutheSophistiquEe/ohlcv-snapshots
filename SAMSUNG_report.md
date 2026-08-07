# 005930

**Generated** : 2026-08-07T21:50:15.761066+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 8.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩231000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot ₩231000.00 (+2.1% vs entrée) · entrée ₩226211.82 · stop ₩202368.97 · T1 ₩262931.82 · R/R 1.54  
> ↳ P(T1 av. stop) 7 % _(réel 5 s)_ · EV/risk -0.422 _(réel 5 s)_ (GBM 0.176) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩221581.89–₩230841.76 (mid ₩226211.82)
- Spot actuel : ₩231000.00 (+2.1% au-dessus de la zone — repli à attendre)
- Stop : ₩202368.97 (stop swing_plan-based (-12.39%))
- Targets : T1 ₩262931.82 · R/R 1.54 | T2 ₩287183.29 · R/R 2.56 | T3 ₩295450.41 · R/R 2.9
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩202368.97


## Edge, scénarios & sizing

- EV/risk : 0.176 | EV/share : ₩4197.935 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 14 % | T2 2 % | T3 1 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 38.8 | bear 50.5 | side 10.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.944% → cible +4.884% / stop −3.126%, p_fill 89%, n_eff≈34.2) : P(cible|rempli) **9%** · **EV/risk -0.490** (×p_fill ; si rempli -1.73% du capital)
  - **swing** (entrée dip −2.068% → cible +16.233% / stop −10.54%, p_fill 81%, n_eff≈30.8) : P(cible|rempli) **7%** · **EV/risk -0.422** (×p_fill ; si rempli -5.48% du capital)
  - **deep** (entrée dip −3.208% → cible +28.436% / stop −15.995%, p_fill 74%, n_eff≈28.4) : P(cible|rempli) **2%** · **EV/risk -0.440** (×p_fill ; si rempli -9.57% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→66% · +2.0%→46% · +3.0%→34% · +5.0%→21% · +8.0%→5%
- Range intraday médian 6.09% (p90 9.84%) · excursion haute méd. +1.88% / basse méd. −3.08%
- Profil de vol intra : ouverture 3.047% vs midi 1.338% vs clôture 1.528% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (149 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑1%/↓1% ; spike-down 71% · recovery-V 20%)_
- **Régime intraday** : **chop** _(efficiency 0.129 ; mean-reverting — autocorr -0.091)_ ; drift intra méd. -1.684% ; recovery-V 18%
- **σ réalisé intraday** 4.667% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 37% / bas 79% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 231375.0 (VA 230025.0–232725.0 ; dernier close 230000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 33% · rebond 58% · **stop −6.75%** sous le fill (sous le bruit) · cible +1.3% · R/R 0.19 (high win-rate)
- Gaps overnight (n=148) : méd. 0.26% · baisse 44% (gap-down >1% 36% · >2% 26%)
- Excursion ouverture 5min (n=149) : bas méd −0.7% (p90 −1.64%) · haut méd +0.65% · range méd 1.56%
- Excursion ouverture 15min (n=149) : bas méd −1.07% (p90 −2.76%) · haut méd +1.04% · range méd 2.24%
- Excursion ouverture 30min (n=149) : bas méd −1.29% (p90 −3.51%) · haut méd +1.13% · range méd 2.96%
- Excursion ouverture 60min (n=149) : bas méd −1.75% (p90 −3.63%) · haut méd +1.27% · range méd 3.18%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 230000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 55% · séance 68% (93/148) · gap 38% · délai 0.0min · rebond 51% (50/93) (MFE +1.11%)
   - −1.0% : fill 30min 50% · séance 65% (87/148) · gap 36% · délai 0.0min · rebond 57% (49/87) (MFE +1.3%)
   - −1.5% : fill 30min 45% · séance 60% (77/148) · gap 27% · délai 0.3min · rebond 58% (46/77) (MFE +1.44%)
   - −2.0% : fill 30min 40% · séance 53% (68/148) · gap 26% · délai 0.2min · rebond 56% (39/68) (MFE +1.57%)
   - −3.0% : fill 30min 32% · séance 48% (59/148) · gap 20% · délai 1.7min · rebond 59% (38/59) (MFE +2.13%)
   - −4.0% : fill 30min 23% · séance 41% (47/148) · gap 15% · délai 26.2min · rebond 58% (31/47) (MFE +1.46%)
   - −5.0% : fill 30min 14% · séance 33% (36/148) · gap 10% · délai 50.8min · rebond 58% (23/36) (MFE +1.3%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.38% (p90 −2.33%) → stop au-delà de −1.19% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.43% (p90 −3.15%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.45% (p90 −4.24%) → stop au-delà de −1.81% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=692 jambes) : jambe baissière méd −1.29% (p90 −3.16%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (63 séances) :
      · −1.0% : fill 98% (60/63) · rebond 44% (30/60)
      · −2.0% : fill 90% (52/63) · rebond 44% (26/52)
      · −3.0% : fill 88% (47/63) · rebond 52% (29/47)
      · −4.0% : fill 78% (39/63) · rebond 48% (24/39)
      · −5.0% : fill 68% (31/63) · rebond 51% (18/31)
   - **flat** (13 séances) :
      · −1.0% : fill 58% (7/13) · rebond 70% (4/7)
      · −2.0% : fill 40% (4/13) · rebond 85% (3/4)
      · −3.0% : fill 40% (4/13) · rebond 85% (3/4)
      · −4.0% : fill 18% (2/13) · rebond 100% (2/2)
      · −5.0% : fill 18% (2/13) · rebond 100% (2/2)
   - **gap-up** (72 séances) :
      · −1.0% : fill 40% (20/72) · rebond 81% (15/20)
      · −2.0% : fill 24% (12/72) · rebond 83% (10/12)
      · −3.0% : fill 18% (8/72) · rebond 76% (6/8)
      · −4.0% : fill 14% (6/72) · rebond 94% (5/6)
      · −5.0% : fill 5% (3/72) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=149) : 38% en base · 62% si les 15 1res min sont vertes (72 cas) · 17% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=149) : COUDE à **1:15** → P(séance verte=clôture>ouverture) 83% si début vert vs 6% si rouge (base 38% · écart 77 pts) ; prédictivité sature ensuite (plafond brut 75min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **83%** · continue >prix actuel 53% ; creux résiduel méd -1.67% (q20 -4.25%) → **SL/trailing à −4.25%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.72% / q75 +3.48% → **scale +1.72% / runner +3.48%**, sortie à la clôture
  - **si ROUGE au coude** (n=71) : edge inversé — récupère vert seulement **6%** (continue à baisser 60%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.12%** (au-delà de la MAE q10 -7.12%), cible rebond +1.3% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=149) : retour [-2.82% .. +2.86%] · haut q95 +3.7% · bas q05 -3.87%
   - 60min (n=149) : retour [-3.22% .. +4.76%] · haut q95 +5.54% · bas q05 -5.29%
   - 2h (n=149) : retour [-4.89% .. +4.47%] · haut q95 +6.28% · bas q05 -6.52%
   - 4h (n=149) : retour [-6.53% .. +5.45%] · haut q95 +6.83% · bas q05 -7.94%
   - 6h (n=149) : retour [-7.21% .. +5.27%] · haut q95 +7.05% · bas q05 -8.27%
   - session (n=149) : retour [-7.49% .. +5.37%] · haut q95 +7.05% · bas q05 -9.16%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 4.0% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.95%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 46.7  _(neutre)_
- **ADX** : 26.6  _(tendance etablie)_
- **MACD** : hist 860.912  _(bullish_recent)_
- **BB** : %B 0.3 · largeur 34.0%
- **ATR** : 23842.86 (85.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.257  _(distribution)_
- **Vol ratio** : 0.67  _(volume normal)_
- **Choppiness** : 51.0  _(transition)_
- **MA** : MA20 247950.0 · MA50 293615.93 · MA200 196319.45  _(prix < MA20)_
- **Dist MA** : MA20 -6.8% · MA50 -21.3% · MA200 +17.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (81838 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
