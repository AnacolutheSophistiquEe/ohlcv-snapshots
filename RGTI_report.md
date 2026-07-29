# RGTI

**Generated** : 2026-07-29T22:02:56.443081+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $13.22  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)  
> ↳ spot $13.22 (+1.3% vs entrée) · entrée $13.05 · stop $12.70 · T1 $13.42 · R/R 1.06  
> ↳ P(T1 av. stop) 39 % _(réel 5 s)_ · EV/risk -0.114 _(réel 5 s)_ (GBM 0.101) · ¼-Kelly 0.019 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.65% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -160 % hors [0,100] (R² max 0.42). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $12.97–$13.12 (mid $13.05)
- Spot actuel : $13.22 (+1.3% au-dessus de la zone — repli à attendre)
- Stop : $12.70 (stop swing_plan-based (-6.01%))
- Targets : T1 $13.42 · R/R 1.06 | T2 $13.80 · R/R 2.14 | T3 $14.18 · R/R 3.23
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $12.70


## Edge, scénarios & sizing

- EV/risk : 0.101 | EV/share : $0.035 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 46 % | T2 32 % | T3 32 %
- Kelly (position) : f* 0.076 | ¼-Kelly 0.019 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 17.2 | side 77.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.308% → cible +2.887% / stop −2.646%, p_fill 75%, n_eff≈31.8) : P(cible|rempli) **39%** · **EV/risk -0.114** (×p_fill ; si rempli -0.40% du capital)
  - **swing** (entrée dip −2.875% → cible +6.456% / stop −3.228%, p_fill 64%, n_eff≈29.3) : P(cible|rempli) **11%** · **EV/risk -0.411** (×p_fill ; si rempli -2.07% du capital)
  - **deep** (entrée dip −4.438% → cible +9.13% / stop −4.565%, p_fill 85%, n_eff≈31.7) : P(cible|rempli) **20%** · **EV/risk -0.337** (×p_fill ; si rempli -1.80% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→80% · +2.0%→71% · +3.0%→55% · +5.0%→38% · +8.0%→14%
- Range intraday médian 8.05% (p90 13.36%) · excursion haute méd. +3.41% / basse méd. −2.89%
- Profil de vol intra : ouverture 5.416% vs midi 1.677% vs clôture 1.874% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 76% · recovery-V 42%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; neutre — autocorr 0.002)_ ; drift intra méd. -0.474% ; recovery-V 38%
- **σ réalisé intraday** 4.927% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 42% / bas 63% / whipsaw 13%
- POC intraday (dernière séance, temps-au-prix) : 14.4873 (VA 14.4608–14.8318 ; dernier close 14.52)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 62% · rebond 74% · **stop −7.24%** sous le fill (sous le bruit) · cible +2.47% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. -0.53% · baisse 58% (gap-down >1% 46% · >2% 31%)
- Excursion ouverture 5min (n=160) : bas méd −1.25% (p90 −2.76%) · haut méd +1.13% · range méd 2.59%
- Excursion ouverture 15min (n=160) : bas méd −1.52% (p90 −4.32%) · haut méd +1.54% · range méd 3.59%
- Excursion ouverture 30min (n=160) : bas méd −1.8% (p90 −5.86%) · haut méd +1.95% · range méd 4.76%
- Excursion ouverture 60min (n=160) : bas méd −2.07% (p90 −6.5%) · haut méd +2.23% · range méd 5.47%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 14.52 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 76% · séance 83% (134/159) · gap 51% · délai 0.0min · rebond 64% (87/134) (MFE +2.25%)
   - −1.0% : fill 30min 70% · séance 81% (130/159) · gap 46% · délai 0.0min · rebond 66% (85/130) (MFE +2.04%)
   - −1.5% : fill 30min 65% · séance 75% (122/159) · gap 41% · délai 0.0min · rebond 65% (80/122) (MFE +2.28%)
   - −2.0% : fill 30min 60% · séance 69% (114/159) · gap 31% · délai 0.0min · rebond 64% (75/114) (MFE +2.37%)
   - −3.0% : fill 30min 53% · séance 62% (97/159) · gap 13% · délai 1.2min · rebond 74% (71/97) (MFE +2.47%)
   - −4.0% : fill 30min 39% · séance 47% (76/159) · gap 4% · délai 4.5min · rebond 72% (55/76) (MFE +2.34%)
   - −5.0% : fill 30min 23% · séance 39% (62/159) · gap 1% · délai 18.4min · rebond 65% (46/62) (MFE +1.66%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.75% (p90 −2.72%) → stop au-delà de −1.79% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.22% (p90 −2.99%) → stop au-delà de −2.09% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.23% (p90 −4.06%) → stop au-delà de −2.27% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1176 jambes) : jambe baissière méd −1.31% (p90 −3.32%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (83 séances) :
      · −1.0% : fill 98% (82/83) · rebond 63% (50/82)
      · −2.0% : fill 89% (78/83) · rebond 63% (52/78)
      · −3.0% : fill 83% (70/83) · rebond 68% (49/70)
      · −4.0% : fill 64% (55/83) · rebond 67% (38/55)
      · −5.0% : fill 55% (47/83) · rebond 62% (35/47)
   - **flat** (15 séances) :
      · −1.0% : fill 91% (13/15) · rebond 90% (11/13)
      · −2.0% : fill 71% (11/15) · rebond 72% (8/11)
      · −3.0% : fill 56% (6/15) · rebond 84% (4/6)
      · −4.0% : fill 56% (6/15) · rebond 85% (4/6)
      · −5.0% : fill 35% (5/15) · rebond 87% (3/5)
   - **gap-up** (61 séances) :
      · −1.0% : fill 52% (35/61) · rebond 64% (24/35)
      · −2.0% : fill 40% (25/61) · rebond 63% (15/25)
      · −3.0% : fill 33% (21/61) · rebond 89% (18/21)
      · −4.0% : fill 21% (15/61) · rebond 85% (13/15)
      · −5.0% : fill 17% (10/61) · rebond 68% (8/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 67% si les 15 1res min sont vertes (81 cas) · 33% si rouges (79 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:32** → P(séance verte=clôture>ouverture) 90% si début vert vs 15% si rouge (base 51% · écart 75 pts) ; prédictivité sature ensuite (plafond brut 140min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **90%** · continue >prix actuel 55% ; creux résiduel méd -1.98% (q20 -3.08%) → **SL/trailing à −3.08%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.65% / q75 +4.22% → **scale +2.65% / runner +4.22%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **15%** (continue à baisser 58%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.67%** (au-delà de la MAE q10 -5.67%), cible rebond +2.15% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.48% .. +4.97%] · haut q95 +6.92% · bas q05 -6.54%
   - 60min (n=160) : retour [-5.99% .. +6.25%] · haut q95 +7.5% · bas q05 -7.04%
   - 2h (n=160) : retour [-7.09% .. +7.66%] · haut q95 +9.16% · bas q05 -8.19%
   - 4h (n=160) : retour [-7.71% .. +6.32%] · haut q95 +9.19% · bas q05 -9.01%
   - 6h (n=160) : retour [-8.14% .. +7.65%] · haut q95 +9.24% · bas q05 -9.66%
   - session (n=160) : retour [-7.32% .. +8.45%] · haut q95 +10.38% · bas q05 -10.19%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RGTI = **volatil sans tendance propre (choppy)** (vol intra méd 4.64%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 32.2  _(momentum baissier)_
- **ADX** : 30.1  _(tendance etablie)_
- **MACD** : hist 0.001  _(bullish_recent)_
- **BB** : %B 0.09 · largeur 38.1%
- **ATR** : 1.15 (12.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.308  _(distribution)_
- **Vol ratio** : 0.89  _(volume normal)_
- **Choppiness** : 51.1  _(transition)_
- **MA** : MA20 15.68 · MA50 19.21 · MA200 22.31  _(prix < MA20)_
- **Dist MA** : MA20 -15.7% · MA50 -31.2% · MA200 -40.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83897 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
