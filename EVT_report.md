# EVT

**Generated** : 2026-07-20T00:04:26.047163+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite high · €3.44  

> 🟡 **WAIT-FOR-DIP** — spot +9.6 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €3.44 (+9.6% vs entrée) · entrée €3.14 · stop €3.03 · T1 €3.25 · R/R 1.0  
> ↳ P(T1 av. stop) 25 % · EV/risk 0.057 · ¼-Kelly 0.009 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.5% cohérent avec le bruit 5 s (EV-optimal ≈ −3.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €3.11–€3.16 (mid €3.14)
- Spot actuel : €3.44 (+9.6% au-dessus de la zone — repli à attendre)
- Stop : €3.03 (stop swing_plan-based (-20.95%))
- Targets : T1 €3.25 · R/R 1.0 | T2 €3.36 · R/R 2.0 | T3 €3.47 · R/R 3.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €3.03


## Edge, scénarios & sizing

- EV/risk : 0.057 | EV/share : €0.006 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 25 % | T2 8 % | T3 8 %
- Kelly (position) : f* 0.037 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 23.8 | bear 58.1 | side 18.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=3, n_eff=2))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→74% · +2.0%→48% · +3.0%→30% · +5.0%→8% · +8.0%→2%
- Range intraday médian 4.43% (p90 6.8%) · excursion haute méd. +1.92% / basse méd. −1.83%
- Profil de vol intra : ouverture 2.88% vs midi 1.201% vs clôture 1.272% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 95% · range 5% · trend ↑0%/↓0% ; spike-down 55% · recovery-V 41%)_
- **Régime intraday** : **chop** _(efficiency 0.08 ; mean-reverting — autocorr -0.12)_ ; drift intra méd. -0.216% ; recovery-V 44%
- **σ réalisé intraday** 3.604% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 63% / bas 60% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 3.5112 (VA 3.4369–3.5409 ; dernier close 3.476)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.0%** sous le close veille · fill 76% · rebond 67% · **stop −3.39%** sous le fill (sous le bruit) · cible +1.57% · R/R 0.46 (high win-rate)
- Gaps overnight (n=159) : méd. -0.07% · baisse 52% (gap-down >1% 21% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.61% (p90 −2.83%) · haut méd +0.61% · range méd 1.38%
- Excursion ouverture 15min (n=160) : bas méd −0.82% (p90 −2.83%) · haut méd +0.84% · range méd 1.77%
- Excursion ouverture 30min (n=160) : bas méd −1.05% (p90 −2.84%) · haut méd +0.95% · range méd 2.2%
- Excursion ouverture 60min (n=160) : bas méd −1.11% (p90 −3.28%) · haut méd +0.96% · range méd 2.38%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.476 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 84% (133/159) · gap 32% · délai 0.2min · rebond 64% (88/133) (MFE +1.44%)
   - −1.0% : fill 30min 54% · séance 76% (120/159) · gap 21% · délai 0.8min · rebond 67% (79/120) (MFE +1.57%)
   - −1.5% : fill 30min 39% · séance 60% (98/159) · gap 16% · délai 2.2min · rebond 62% (63/98) (MFE +1.51%)
   - −2.0% : fill 30min 30% · séance 50% (79/159) · gap 11% · délai 14.3min · rebond 64% (52/79) (MFE +1.42%)
   - −3.0% : fill 30min 18% · séance 33% (56/159) · gap 6% · délai 3.7min · rebond 64% (41/56) (MFE +1.66%)
   - −4.0% : fill 30min 9% · séance 20% (31/159) · gap 3% · délai 35.2min · rebond 49% (18/31) (MFE +1.02%)
   - −5.0% : fill 30min 6% · séance 10% (18/159) · gap 2% · délai 4.9min · rebond 50% (11/18) (MFE +1.33%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −2.41%) → stop au-delà de −1.49% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.61% (p90 −2.06%) → stop au-delà de −1.4% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.61% (p90 −2.0%) → stop au-delà de −1.38% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=805 jambes) : jambe baissière méd −1.07% (p90 −2.33%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (65 séances) :
      · −1.0% : fill 95% (62/65) · rebond 68% (38/62)
      · −2.0% : fill 70% (46/65) · rebond 60% (29/46)
      · −3.0% : fill 42% (34/65) · rebond 68% (25/34)
      · −4.0% : fill 29% (21/65) · rebond 55% (14/21)
      · −5.0% : fill 18% (14/65) · rebond 56% (9/14)
   - **flat** (41 séances) :
      · −1.0% : fill 88% (32/41) · rebond 71% (25/32)
      · −2.0% : fill 53% (17/41) · rebond 73% (12/17)
      · −3.0% : fill 37% (10/41) · rebond 62% (7/10)
      · −4.0% : fill 22% (5/41) · rebond 20% (1/5)
      · −5.0% : fill 11% (3/41) · rebond 27% (1/3)
   - **gap-up** (53 séances) :
      · −1.0% : fill 44% (26/53) · rebond 56% (16/26)
      · −2.0% : fill 24% (16/53) · rebond 61% (11/16)
      · −3.0% : fill 18% (12/53) · rebond 57% (9/12)
      · −4.0% : fill 8% (5/53) · rebond 80% (3/5)
      · −5.0% : fill 1% (1/53) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 57% en base · 67% si les 15 1res min sont vertes (76 cas) · 48% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **6min** → P(séance verte=clôture>ouverture) 68% si début vert vs 46% si rouge (base 57% · écart 22 pts) ; prédictivité sature ensuite (plafond brut 290min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **68%** · continue >prix actuel 50% ; creux résiduel méd -1.84% (q20 -3.1%) → **SL/trailing à −3.1%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.29% / q75 +2.39% → **scale +1.29% / runner +2.39%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **46%** (continue à baisser 38%) → **RÉDUIRE ~54%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.03%** (au-delà de la MAE q10 -5.03%), cible rebond +2.12% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.31% .. +2.37%] · haut q95 +3.48% · bas q05 -4.73%
   - 60min (n=160) : retour [-4.02% .. +2.79%] · haut q95 +4.13% · bas q05 -5.43%
   - 2h (n=160) : retour [-4.1% .. +2.98%] · haut q95 +4.3% · bas q05 -5.51%
   - 4h (n=160) : retour [-3.26% .. +2.72%] · haut q95 +4.3% · bas q05 -6.88%
   - 6h (n=160) : retour [-3.75% .. +3.17%] · haut q95 +4.5% · bas q05 -7.21%
   - session (n=160) : retour [-4.6% .. +4.05%] · haut q95 +5.46% · bas q05 -7.35%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.92%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 13.6  _(survente)_
- **ADX** : 28.0  _(tendance etablie)_
- **MACD** : hist -0.185  _(bearish_recent)_
- **BB** : %B -0.01 · largeur 51.1%
- **ATR** : 0.3 (86.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.16  _(accumulation)_
- **Vol ratio** : 1.37  _(volume normal)_
- **Choppiness** : 27.6  _(marche directionnel)_
- **MA** : MA20 4.67 · MA50 4.8 · MA200 5.45  _(prix < MA20)_
- **Dist MA** : MA20 -26.3% · MA50 -28.4% · MA200 -36.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88537 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
