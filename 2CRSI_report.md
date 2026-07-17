# AL2SI

**Generated** : 2026-07-17T21:46:32.542859+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 9.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €25.96  

> 🟡 **WAIT-FOR-DIP** — spot +5.5 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €25.96 (+5.5% vs entrée) · entrée €24.61 · stop €23.40 · T1 €25.94 · R/R 1.1  
> ↳ P(T1 av. stop) 20 % _(réel 5 s)_ · EV/risk 0.005 _(réel 5 s)_ (GBM -0.028) · ¼-Kelly 0.027 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.93% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -34 % hors [0,100] (R² max 0.55). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €24.35–€24.88 (mid €24.61)
- Spot actuel : €25.96 (+5.5% au-dessus de la zone — repli à attendre)
- Stop : €23.40 (stop swing_plan-based (-16.76%))
- Targets : T1 €25.94 · R/R 1.1 | T2 €27.26 · R/R 2.19 | T3 €28.59 · R/R 3.29
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €23.40


## Edge, scénarios & sizing

- EV/risk : -0.028 | EV/share : €-0.035 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 37 % | T3 37 %
- Kelly (position) : f* 0.107 | ¼-Kelly 0.027 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 16.1 | bear 6.7 | side 77.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −5.189% → cible +5.385% / stop −4.927%, p_fill 62%, n_eff≈21.3) : P(cible|rempli) **20%** · **EV/risk +0.005** (×p_fill ; si rempli +0.04% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=12, n_eff=9))
  - **deep** : indisponible (échantillon insuffisant (n=10, n_eff=9))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→79% · +2.0%→72% · +3.0%→62% · +5.0%→40% · +8.0%→22%
- Range intraday médian 8.41% (p90 22.19%) · excursion haute méd. +3.92% / basse méd. −3.83%
- Profil de vol intra : ouverture 5.804% vs midi 1.724% vs clôture 1.957% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (150 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 10% · trend ↑0%/↓1% ; spike-down 76% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.146 ; mean-reverting — autocorr -0.044)_ ; drift intra méd. -0.703% ; recovery-V 23%
- **σ réalisé intraday** 8.332% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 41% / bas 74% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 24.6175 (VA 24.2125–26.1025 ; dernier close 24.54)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 46% · rebond 92% · **stop −6.91%** sous le fill (sous le bruit) · cible +2.8% · R/R 0.41 (high win-rate)
- Gaps overnight (n=149) : méd. 0.21% · baisse 40% (gap-down >1% 22% · >2% 9%)
- Excursion ouverture 5min (n=150) : bas méd −1.22% (p90 −5.02%) · haut méd +1.04% · range méd 3.08%
- Excursion ouverture 15min (n=150) : bas méd −1.6% (p90 −5.87%) · haut méd +1.55% · range méd 4.47%
- Excursion ouverture 30min (n=150) : bas méd −1.72% (p90 −6.24%) · haut méd +2.04% · range méd 4.96%
- Excursion ouverture 60min (n=150) : bas méd −2.29% (p90 −7.06%) · haut méd +2.54% · range méd 5.9%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 24.54 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 81% (116/149) · gap 28% · délai 0.3min · rebond 67% (77/116) (MFE +3.02%)
   - −1.0% : fill 30min 62% · séance 79% (111/149) · gap 22% · délai 0.3min · rebond 71% (77/111) (MFE +2.56%)
   - −1.5% : fill 30min 54% · séance 74% (101/149) · gap 15% · délai 1.0min · rebond 71% (67/101) (MFE +1.89%)
   - −2.0% : fill 30min 45% · séance 66% (88/149) · gap 9% · délai 1.4min · rebond 69% (59/88) (MFE +1.88%)
   - −3.0% : fill 30min 34% · séance 57% (72/149) · gap 7% · délai 9.0min · rebond 85% (60/72) (MFE +2.32%)
   - −4.0% : fill 30min 29% · séance 50% (62/149) · gap 5% · délai 19.0min · rebond 76% (48/62) (MFE +2.93%)
   - −5.0% : fill 30min 20% · séance 46% (54/149) · gap 4% · délai 42.0min · rebond 92% (51/54) (MFE +2.8%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.86% (p90 −5.57%) → stop au-delà de −2.96% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.99% (p90 −5.6%) → stop au-delà de −3.9% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.89% (p90 −5.84%) → stop au-delà de −3.47% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1446 jambes) : jambe baissière méd −1.25% (p90 −3.61%) · ~20.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (52 séances) :
      · −1.0% : fill 98% (48/52) · rebond 66% (32/48)
      · −2.0% : fill 86% (41/52) · rebond 55% (25/41)
      · −3.0% : fill 84% (37/52) · rebond 79% (30/37)
      · −4.0% : fill 72% (32/52) · rebond 75% (26/32)
      · −5.0% : fill 64% (29/52) · rebond 81% (26/29)
   - **flat** (32 séances) :
      · −1.0% : fill 84% (25/32) · rebond 83% (20/25)
      · −2.0% : fill 69% (19/32) · rebond 78% (14/19)
      · −3.0% : fill 51% (13/32) · rebond 94% (12/13)
      · −4.0% : fill 51% (13/32) · rebond 81% (11/13)
      · −5.0% : fill 44% (11/32) · rebond 100% (11/11)
   - **gap-up** (65 séances) :
      · −1.0% : fill 63% (38/65) · rebond 67% (25/38)
      · −2.0% : fill 50% (28/65) · rebond 79% (20/28)
      · −3.0% : fill 40% (22/65) · rebond 88% (18/22)
      · −4.0% : fill 34% (17/65) · rebond 72% (11/17)
      · −5.0% : fill 32% (14/65) · rebond 100% (14/14)
- **P(clôture VERTE) selon le drive 15min** (n=150) : 44% en base · 60% si les 15 1res min sont vertes (72 cas) · 32% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=150) : COUDE à **31min** → P(séance verte=clôture>ouverture) 70% si début vert vs 22% si rouge (base 44% · écart 48 pts) ; prédictivité sature ensuite (plafond brut 241min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **70%** · continue >prix actuel 54% ; creux résiduel méd -2.55% (q20 -5.65%) → **SL/trailing à −5.65%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.71% / q75 +6.41% → **scale +3.71% / runner +6.41%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **22%** (continue à baisser 59%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −10.63%** (au-delà de la MAE q10 -10.63%), cible rebond +2.32% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=150) : retour [-5.42% .. +7.39%] · haut q95 +8.92% · bas q05 -7.78%
   - 60min (n=150) : retour [-6.04% .. +9.59%] · haut q95 +10.02% · bas q05 -8.59%
   - 2h (n=150) : retour [-6.09% .. +10.07%] · haut q95 +11.72% · bas q05 -8.61%
   - 4h (n=150) : retour [-10.19% .. +10.84%] · haut q95 +13.02% · bas q05 -12.18%
   - 6h (n=150) : retour [-9.79% .. +14.72%] · haut q95 +18.98% · bas q05 -13.32%
   - session (n=150) : retour [-10.3% .. +19.99%] · haut q95 +20.3% · bas q05 -16.27%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.31%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 41.1  _(momentum baissier)_
- **ADX** : 24.7  _(pas de tendance nette)_
- **MACD** : hist -0.492  _(bearish_recent)_
- **BB** : %B 0.28 · largeur 64.9%
- **ATR** : 4.04 (88.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.01  _(neutre)_
- **Vol ratio** : 1.17  _(volume normal)_
- **Choppiness** : 44.2  _(transition)_
- **MA** : MA20 30.38 · MA50 39.41 · MA200 24.09  _(prix < MA20)_
- **Dist MA** : MA20 -14.6% · MA50 -34.1% · MA200 +7.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90445 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
