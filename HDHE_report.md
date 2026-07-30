# 267260

**Generated** : 2026-07-30T00:15:07.394350+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 1/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩586000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩586000.00 (+1.2% vs entrée) · entrée ₩578932.01 · stop ₩532617.45 · T1 ₩620360.59 · R/R 0.89  
> ↳ P(T1 av. stop) 12 % _(réel 5 s)_ · EV/risk -0.12 _(réel 5 s)_ (GBM -0.177) · ¼-Kelly 0.001 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -9523 % hors [0,100] (R² max 0.94). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 1/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩574802.38–₩583061.64 (mid ₩578932.01)
- Spot actuel : ₩586000.00 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : ₩532617.45 (stop swing_plan-based (-6.52%))
- Targets : T1 ₩620360.59 · R/R 0.89 | T2 ₩630524.66 · R/R 1.11 | T3 ₩640688.72 · R/R 1.33
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩532617.45


## Edge, scénarios & sizing

- EV/risk : -0.177 | EV/share : ₩-8191.888 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 11 % | T2 11 % | T3 11 %
- Kelly (position) : f* 0.002 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 15.6 | bear 20.4 | side 64.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.207% → cible +7.156% / stop −8.0%, p_fill 89%, n_eff≈36.5) : P(cible|rempli) **12%** · **EV/risk -0.120** (×p_fill ; si rempli -1.07% du capital)
  - **swing** (entrée dip −2.65% → cible +7.951% / stop −3.975%, p_fill 88%, n_eff≈35.1) : P(cible|rempli) **26%** · **EV/risk -0.259** (×p_fill ; si rempli -1.18% du capital)
  - **deep** (entrée dip −4.098% → cible +11.244% / stop −5.622%, p_fill 84%, n_eff≈32.5) : P(cible|rempli) **16%** · **EV/risk -0.444** (×p_fill ; si rempli -2.96% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→69% · +2.0%→46% · +3.0%→31% · +5.0%→11% · +8.0%→5%
- Range intraday médian 6.53% (p90 10.49%) · excursion haute méd. +1.84% / basse méd. −3.65%
- Profil de vol intra : ouverture 4.11% vs midi 1.098% vs clôture 1.182% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (142 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.127 ; mean-reverting — autocorr -0.054)_ ; drift intra méd. -1.789% ; recovery-V 17%
- **σ réalisé intraday** 4.692% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 74% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 722450.0 (VA 705450.0–729250.0 ; dernier close 705000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 36% · rebond 80% · **stop −4.35%** sous le fill (sous le bruit) · cible +1.92% · R/R 0.44 (high win-rate)
- Gaps overnight (n=141) : méd. 0.74% · baisse 40% (gap-down >1% 24% · >2% 11%)
- Excursion ouverture 5min (n=142) : bas méd −1.62% (p90 −3.85%) · haut méd +0.94% · range méd 2.7%
- Excursion ouverture 15min (n=142) : bas méd −1.92% (p90 −4.62%) · haut méd +1.05% · range méd 3.39%
- Excursion ouverture 30min (n=142) : bas méd −2.23% (p90 −4.96%) · haut méd +1.07% · range méd 3.77%
- Excursion ouverture 60min (n=142) : bas méd −2.76% (p90 −5.69%) · haut méd +1.25% · range méd 4.18%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 705000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 72% (100/141) · gap 32% · délai 0.0min · rebond 51% (55/100) (MFE +1.07%)
   - −1.0% : fill 30min 57% · séance 69% (93/141) · gap 24% · délai 0.2min · rebond 54% (54/93) (MFE +1.01%)
   - −1.5% : fill 30min 48% · séance 63% (80/141) · gap 16% · délai 0.4min · rebond 63% (51/80) (MFE +1.27%)
   - −2.0% : fill 30min 44% · séance 60% (73/141) · gap 11% · délai 0.7min · rebond 67% (49/73) (MFE +1.61%)
   - −3.0% : fill 30min 34% · séance 51% (58/141) · gap 8% · délai 3.7min · rebond 76% (40/58) (MFE +1.89%)
   - −4.0% : fill 30min 24% · séance 43% (48/141) · gap 4% · délai 14.7min · rebond 73% (37/48) (MFE +2.22%)
   - −5.0% : fill 30min 16% · séance 36% (38/141) · gap 2% · délai 39.0min · rebond 80% (29/38) (MFE +1.92%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.72% (p90 −3.41%) → stop au-delà de −1.99% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.93% (p90 −3.31%) → stop au-delà de −1.97% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.04% (p90 −4.6%) → stop au-delà de −3.46% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=710 jambes) : jambe baissière méd −1.28% (p90 −3.6%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 98% (48/49) · rebond 46% (25/48)
      · −2.0% : fill 92% (41/49) · rebond 59% (24/41)
      · −3.0% : fill 83% (35/49) · rebond 73% (23/35)
      · −4.0% : fill 74% (31/49) · rebond 71% (24/31)
      · −5.0% : fill 64% (24/49) · rebond 78% (18/24)
   - **flat** (17 séances) :
      · −1.0% : fill 88% (14/17) · rebond 47% (7/14)
      · −2.0% : fill 79% (12/17) · rebond 78% (9/12)
      · −3.0% : fill 78% (11/17) · rebond 83% (8/11)
      · −4.0% : fill 57% (7/17) · rebond 68% (5/7)
      · −5.0% : fill 57% (7/17) · rebond 89% (6/7)
   - **gap-up** (75 séances) :
      · −1.0% : fill 48% (31/75) · rebond 66% (22/31)
      · −2.0% : fill 35% (20/75) · rebond 74% (16/20)
      · −3.0% : fill 26% (12/75) · rebond 77% (9/12)
      · −4.0% : fill 21% (10/75) · rebond 82% (8/10)
      · −5.0% : fill 14% (7/75) · rebond 78% (5/7)
- **P(clôture VERTE) selon le drive 15min** (n=142) : 33% en base · 50% si les 15 1res min sont vertes (66 cas) · 22% si rouges (76 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=142) : COUDE à **1:20** → P(séance verte=clôture>ouverture) 74% si début vert vs 10% si rouge (base 33% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=62) : tient le vert **74%** · continue >prix actuel 45% ; creux résiduel méd -1.47% (q20 -3.65%) → **SL/trailing à −3.65%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.23% / q75 +2.7% → **scale +1.23% / runner +2.7%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **10%** (continue à baisser 54%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.1%** (au-delà de la MAE q10 -5.1%), cible rebond +1.11% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=142) : retour [-5.07% .. +2.7%] · haut q95 +4.3% · bas q05 -5.57%
   - 60min (n=142) : retour [-5.64% .. +3.15%] · haut q95 +4.51% · bas q05 -6.01%
   - 2h (n=142) : retour [-6.75% .. +3.66%] · haut q95 +5.09% · bas q05 -7.34%
   - 4h (n=142) : retour [-6.94% .. +4.38%] · haut q95 +5.47% · bas q05 -8.41%
   - 6h (n=142) : retour [-7.57% .. +4.59%] · haut q95 +7.15% · bas q05 -9.22%
   - session (n=142) : retour [-7.47% .. +5.18%] · haut q95 +7.2% · bas q05 -9.67%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.44%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : extreme
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

- **RSI** : 31.2  _(momentum baissier)_
- **ADX** : 27.2  _(tendance etablie)_
- **MACD** : hist -10684.96  _(bearish_recent)_
- **BB** : %B -0.13 · largeur 46.2%
- **ATR** : 70785.71 (77.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.163  _(distribution)_
- **Vol ratio** : 2.85  _(volume au-dessus de la moyenne)_
- **Choppiness** : 41.1  _(transition)_
- **MA** : MA20 826550.0 · MA50 954840.0 · MA200 921547.67  _(prix < MA20)_
- **Dist MA** : MA20 -29.1% · MA50 -38.6% · MA200 -36.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83065 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
