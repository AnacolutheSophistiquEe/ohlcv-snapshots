# RGTI

**Generated** : 2026-07-27T22:02:40.461587+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $15.64  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot $15.64 (+1.8% vs entrée) · entrée $15.37 · stop $14.98 · T1 $15.74 · R/R 0.95  
> ↳ P(T1 av. stop) 33 % _(réel 5 s)_ · EV/risk -0.213 _(réel 5 s)_ (GBM 0.085) · ¼-Kelly 0.014 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $15.29–$15.44 (mid $15.37)
- Spot actuel : $15.64 (+1.8% au-dessus de la zone — repli à attendre)
- Stop : $14.98 (stop swing_plan-based (-6.5%))
- Targets : T1 $15.74 · R/R 0.95 | T2 $16.12 · R/R 1.92 | T3 $16.49 · R/R 2.87
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $14.98


## Edge, scénarios & sizing

- EV/risk : 0.085 | EV/share : $0.033 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 51 % | T2 31 % | T3 30 %
- Kelly (position) : f* 0.056 | ¼-Kelly 0.014 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 17.5 | side 77.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.754% → cible +2.448% / stop −2.5%, p_fill 60%, n_eff≈28.1) : P(cible|rempli) **33%** · **EV/risk -0.213** (×p_fill ; si rempli -0.88% du capital)
  - **swing** (entrée dip −3.869% → cible +5.474% / stop −2.737%, p_fill 64%, n_eff≈26.5) : P(cible|rempli) **14%** · **EV/risk -0.370** (×p_fill ; si rempli -1.59% du capital)
  - **deep** (entrée dip −5.97% → cible +7.742% / stop −3.871%, p_fill 80%, n_eff≈28.5) : P(cible|rempli) **31%** · **EV/risk -0.048** (×p_fill ; si rempli -0.23% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→80% · +2.0%→71% · +3.0%→55% · +5.0%→36% · +8.0%→14%
- Range intraday médian 8.01% (p90 13.36%) · excursion haute méd. +3.41% / basse méd. −2.89%
- Profil de vol intra : ouverture 5.342% vs midi 1.659% vs clôture 1.861% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 75% · recovery-V 42%)_
- **Régime intraday** : **chop** _(efficiency 0.12 ; neutre — autocorr -0.018)_ ; drift intra méd. -0.505% ; recovery-V 36%
- **σ réalisé intraday** 4.839% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 59% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 14.4712 (VA 14.3407–14.6762 ; dernier close 14.17)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 62% · rebond 76% · **stop −6.87%** sous le fill (sous le bruit) · cible +2.55% · R/R 0.37 (high win-rate)
- Gaps overnight (n=159) : méd. -0.53% · baisse 58% (gap-down >1% 46% · >2% 30%)
- Excursion ouverture 5min (n=160) : bas méd −1.23% (p90 −2.8%) · haut méd +1.13% · range méd 2.56%
- Excursion ouverture 15min (n=160) : bas méd −1.52% (p90 −4.1%) · haut méd +1.54% · range méd 3.49%
- Excursion ouverture 30min (n=160) : bas méd −1.8% (p90 −5.33%) · haut méd +1.95% · range méd 4.65%
- Excursion ouverture 60min (n=160) : bas méd −2.07% (p90 −6.24%) · haut méd +2.23% · range méd 5.41%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 14.17 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 77% · séance 84% (135/159) · gap 51% · délai 0.0min · rebond 66% (89/135) (MFE +2.29%)
   - −1.0% : fill 30min 71% · séance 82% (131/159) · gap 46% · délai 0.0min · rebond 67% (87/131) (MFE +2.06%)
   - −1.5% : fill 30min 66% · séance 76% (123/159) · gap 40% · délai 0.0min · rebond 66% (82/123) (MFE +2.38%)
   - −2.0% : fill 30min 60% · séance 70% (114/159) · gap 30% · délai 0.0min · rebond 65% (75/114) (MFE +2.44%)
   - −3.0% : fill 30min 53% · séance 62% (97/159) · gap 12% · délai 1.2min · rebond 76% (71/97) (MFE +2.55%)
   - −4.0% : fill 30min 38% · séance 47% (76/159) · gap 4% · délai 5.8min · rebond 75% (55/76) (MFE +2.38%)
   - −5.0% : fill 30min 22% · séance 38% (62/159) · gap 1% · délai 21.6min · rebond 68% (46/62) (MFE +1.71%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.75% (p90 −2.76%) → stop au-delà de −1.79% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.19% (p90 −3.07%) → stop au-delà de −2.11% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.23% (p90 −4.07%) → stop au-delà de −2.39% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1176 jambes) : jambe baissière méd −1.31% (p90 −3.31%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (83 séances) :
      · −1.0% : fill 98% (82/83) · rebond 65% (51/82)
      · −2.0% : fill 88% (77/83) · rebond 65% (52/77)
      · −3.0% : fill 82% (69/83) · rebond 71% (49/69)
      · −4.0% : fill 62% (54/83) · rebond 71% (38/54)
      · −5.0% : fill 53% (46/83) · rebond 66% (35/46)
   - **flat** (15 séances) :
      · −1.0% : fill 91% (13/15) · rebond 90% (11/13)
      · −2.0% : fill 71% (11/15) · rebond 72% (8/11)
      · −3.0% : fill 56% (6/15) · rebond 84% (4/6)
      · −4.0% : fill 56% (6/15) · rebond 85% (4/6)
      · −5.0% : fill 35% (5/15) · rebond 87% (3/5)
   - **gap-up** (61 séances) :
      · −1.0% : fill 55% (36/61) · rebond 64% (25/36)
      · −2.0% : fill 42% (26/61) · rebond 62% (15/26)
      · −3.0% : fill 35% (22/61) · rebond 88% (18/22)
      · −4.0% : fill 22% (16/61) · rebond 83% (13/16)
      · −5.0% : fill 18% (11/61) · rebond 67% (8/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 66% si les 15 1res min sont vertes (81 cas) · 34% si rouges (79 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:32** → P(séance verte=clôture>ouverture) 90% si début vert vs 16% si rouge (base 51% · écart 74 pts) ; prédictivité sature ensuite (plafond brut 140min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **90%** · continue >prix actuel 53% ; creux résiduel méd -2.08% (q20 -3.08%) → **SL/trailing à −3.08%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.6% / q75 +4.26% → **scale +2.6% / runner +4.26%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **16%** (continue à baisser 57%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.69%** (au-delà de la MAE q10 -5.69%), cible rebond +2.17% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.26% .. +4.6%] · haut q95 +6.96% · bas q05 -6.56%
   - 60min (n=160) : retour [-6.03% .. +6.48%] · haut q95 +8.03% · bas q05 -7.05%
   - 2h (n=160) : retour [-7.22% .. +7.71%] · haut q95 +9.18% · bas q05 -8.2%
   - 4h (n=160) : retour [-7.8% .. +6.34%] · haut q95 +9.19% · bas q05 -8.8%
   - 6h (n=160) : retour [-8.41% .. +7.76%] · haut q95 +9.34% · bas q05 -10.19%
   - session (n=160) : retour [-7.51% .. +8.55%] · haut q95 +10.48% · bas q05 -10.24%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RGTI = **volatil sans tendance propre (choppy)** (vol intra méd 4.64%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 36.6  _(momentum baissier)_
- **ADX** : 29.5  _(tendance etablie)_
- **MACD** : hist 0.041  _(bullish_recent)_
- **BB** : %B 0.38 · largeur 41.6%
- **ATR** : 1.06 (4.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.169  _(distribution)_
- **Vol ratio** : 1.29  _(volume normal)_
- **Choppiness** : 48.5  _(transition)_
- **MA** : MA20 16.44 · MA50 19.48 · MA200 22.77  _(prix < MA20)_
- **Dist MA** : MA20 -4.9% · MA50 -19.7% · MA200 -31.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (82957 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
