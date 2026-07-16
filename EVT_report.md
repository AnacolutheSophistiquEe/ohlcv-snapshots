# EVT

**Generated** : 2026-07-16T21:38:42.966279+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite high · €3.46  

> 🟡 **WAIT-FOR-DIP** — spot +9.5 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €3.46 (+9.5% vs entrée) · entrée €3.16 · stop €3.05 · T1 €3.28 · R/R 1.09  
> ↳ P(T1 av. stop) 24 % · EV/risk 0.042 · ¼-Kelly 0.006 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.5% cohérent avec le bruit 5 s (EV-optimal ≈ −3.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €3.14–€3.19 (mid €3.16)
- Spot actuel : €3.46 (+9.5% au-dessus de la zone — repli à attendre)
- Stop : €3.05 (stop swing_plan-based (-20.59%))
- Targets : T1 €3.28 · R/R 1.09 | T2 €3.39 · R/R 2.09 | T3 €3.50 · R/R 3.09
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €3.05


## Edge, scénarios & sizing

- EV/risk : 0.042 | EV/share : €0.005 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 24 % | T2 8 % | T3 8 %
- Kelly (position) : f* 0.023 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 20.7 | bear 44.0 | side 35.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=3, n_eff=2))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→72% · +2.0%→46% · +3.0%→29% · +5.0%→8% · +8.0%→2%
- Range intraday médian 4.4% (p90 6.8%) · excursion haute méd. +1.83% / basse méd. −1.7%
- Profil de vol intra : ouverture 2.879% vs midi 1.21% vs clôture 1.266% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 95% · range 5% · trend ↑0%/↓0% ; spike-down 53% · recovery-V 41%)_
- **Régime intraday** : **chop** _(efficiency 0.085 ; mean-reverting — autocorr -0.116)_ ; drift intra méd. -0.239% ; recovery-V 44%
- **σ réalisé intraday** 3.581% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 59% / bas 61% / whipsaw 26%
- POC intraday (dernière séance, temps-au-prix) : 3.485 (VA 3.455–3.515 ; dernier close 3.49)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.0%** sous le close veille · fill 75% · rebond 65% · **stop −3.49%** sous le fill (sous le bruit) · cible +1.52% · R/R 0.44 (high win-rate)
- Gaps overnight (n=159) : méd. -0.06% · baisse 52% (gap-down >1% 22% · >2% 12%)
- Excursion ouverture 5min (n=160) : bas méd −0.61% (p90 −2.7%) · haut méd +0.69% · range méd 1.38%
- Excursion ouverture 15min (n=160) : bas méd −0.82% (p90 −2.77%) · haut méd +0.85% · range méd 1.77%
- Excursion ouverture 30min (n=160) : bas méd −0.95% (p90 −2.82%) · haut méd +0.97% · range méd 2.2%
- Excursion ouverture 60min (n=160) : bas méd −1.09% (p90 −3.18%) · haut méd +0.97% · range méd 2.38%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.49 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 84% (133/159) · gap 33% · délai 0.2min · rebond 63% (87/133) (MFE +1.32%)
   - −1.0% : fill 30min 52% · séance 75% (120/159) · gap 22% · délai 1.0min · rebond 65% (78/120) (MFE +1.52%)
   - −1.5% : fill 30min 37% · séance 58% (97/159) · gap 17% · délai 2.3min · rebond 60% (61/97) (MFE +1.35%)
   - −2.0% : fill 30min 30% · séance 48% (78/159) · gap 12% · délai 14.3min · rebond 61% (50/78) (MFE +1.32%)
   - −3.0% : fill 30min 16% · séance 32% (55/159) · gap 6% · délai 22.0min · rebond 62% (40/55) (MFE +1.55%)
   - −4.0% : fill 30min 10% · séance 21% (31/159) · gap 3% · délai 35.2min · rebond 49% (18/31) (MFE +1.02%)
   - −5.0% : fill 30min 7% · séance 11% (18/159) · gap 2% · délai 4.9min · rebond 50% (11/18) (MFE +1.33%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.35% (p90 −1.9%) → stop au-delà de −1.41% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −1.81%) → stop au-delà de −1.33% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.61% (p90 −1.69%) → stop au-delà de −1.3% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=804 jambes) : jambe baissière méd −1.08% (p90 −2.34%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (64 séances) :
      · −1.0% : fill 95% (61/64) · rebond 67% (37/61)
      · −2.0% : fill 69% (45/64) · rebond 58% (28/45)
      · −3.0% : fill 44% (34/64) · rebond 68% (25/34)
      · −4.0% : fill 30% (21/64) · rebond 55% (14/21)
      · −5.0% : fill 19% (14/64) · rebond 56% (9/14)
   - **flat** (40 séances) :
      · −1.0% : fill 87% (31/40) · rebond 69% (24/31)
      · −2.0% : fill 50% (16/40) · rebond 68% (11/16)
      · −3.0% : fill 32% (9/40) · rebond 53% (6/9)
      · −4.0% : fill 23% (5/40) · rebond 20% (1/5)
      · −5.0% : fill 12% (3/40) · rebond 27% (1/3)
   - **gap-up** (55 séances) :
      · −1.0% : fill 44% (28/55) · rebond 56% (17/28)
      · −2.0% : fill 24% (17/55) · rebond 60% (11/17)
      · −3.0% : fill 18% (12/55) · rebond 57% (9/12)
      · −4.0% : fill 8% (5/55) · rebond 80% (3/5)
      · −5.0% : fill 1% (1/55) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 57% en base · 67% si les 15 1res min sont vertes (77 cas) · 47% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:05** → P(séance verte=clôture>ouverture) 79% si début vert vs 34% si rouge (base 57% · écart 44 pts) ; prédictivité sature ensuite (plafond brut 286min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **79%** · continue >prix actuel 58% ; creux résiduel méd -1.45% (q20 -2.66%) → **SL/trailing à −2.66%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.17% / q75 +2.67% → **scale +1.17% / runner +2.67%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **34%** (continue à baisser 43%) → **RÉDUIRE ~66%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.81%** (au-delà de la MAE q10 -3.81%), cible rebond +1.63% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.47% .. +2.39%] · haut q95 +3.52% · bas q05 -5.0%
   - 60min (n=160) : retour [-4.44% .. +2.83%] · haut q95 +4.17% · bas q05 -5.56%
   - 2h (n=160) : retour [-4.53% .. +3.04%] · haut q95 +4.36% · bas q05 -5.74%
   - 4h (n=160) : retour [-3.37% .. +2.8%] · haut q95 +4.36% · bas q05 -7.2%
   - 6h (n=160) : retour [-3.81% .. +3.19%] · haut q95 +4.54% · bas q05 -7.8%
   - session (n=160) : retour [-4.62% .. +4.05%] · haut q95 +5.58% · bas q05 -7.8%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.91%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 16.2  _(survente)_
- **ADX** : 25.4  _(tendance etablie)_
- **MACD** : hist -0.171  _(bearish_recent)_
- **BB** : %B -0.11 · largeur 44.2%
- **ATR** : 0.3 (84.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.219  _(accumulation)_
- **Vol ratio** : 1.21  _(volume normal)_
- **Choppiness** : 27.0  _(marche directionnel)_
- **MA** : MA20 4.73 · MA50 4.84 · MA200 5.47  _(prix < MA20)_
- **Dist MA** : MA20 -26.8% · MA50 -28.5% · MA200 -36.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88776 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
