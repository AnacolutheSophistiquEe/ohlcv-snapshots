# SOFI

**Generated** : 2026-08-04T00:32:06.610215+00:00  
**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $18.03  

> 🟡 **WAIT-FOR-DIP** — spot +2.8 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $18.03 (+2.8% vs entrée) · entrée $17.54 · stop $17.07 · T1 $18.47 · R/R 1.98  
> ↳ P(T1 av. stop) 0 % _(réel 5 s)_ · EV/risk 0.055 _(réel 5 s)_ (GBM -0.076) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.65% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 3734 % hors [0,100] (R² max 0.85). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $17.45–$17.62 (mid $17.54)
- Spot actuel : $18.03 (+2.8% au-dessus de la zone — repli à attendre)
- Stop : $17.07 (stop swing_plan-based (-11.25%))
- Targets : T1 $18.47 · R/R 1.98 | T2 $18.75 · R/R 2.57 | T3 $18.82 · R/R 2.72
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $17.07


## Edge, scénarios & sizing

- EV/risk : -0.076 | EV/share : $-0.035 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 11 % | T2 11 % | T3 11 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 8.7 | bear 30.1 | side 61.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 144.0 (= 8 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.731% → cible +5.302% / stop −2.651%, p_fill 39%, n_eff≈16.1) : P(cible|rempli) **0%** · **EV/risk +0.055** (×p_fill ; si rempli +0.37% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=8, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=8, n_eff=4))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→91% · +1.0%→70% · +2.0%→49% · +3.0%→36% · +5.0%→11% · +8.0%→0%
- Range intraday médian 4.41% (p90 6.91%) · excursion haute méd. +1.9% / basse méd. −2.18%
- Profil de vol intra : ouverture 3.065% vs midi 0.923% vs clôture 0.999% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 17% · trend ↑0%/↓0% ; spike-down 67% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.135 ; neutre — autocorr -0.02)_ ; drift intra méd. 0.007% ; recovery-V 22%
- **σ réalisé intraday** 2.983% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 51% / bas 62% / whipsaw 13%
- POC intraday (dernière séance, temps-au-prix) : 16.3747 (VA 16.1578–16.4057 ; dernier close 16.31)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 52% · rebond 71% · **stop −2.97%** sous le fill (sous le bruit) · cible +1.88% · R/R 0.63 (high win-rate)
- Gaps overnight (n=159) : méd. 0.09% · baisse 46% (gap-down >1% 27% · >2% 12%)
- Excursion ouverture 5min (n=160) : bas méd −0.67% (p90 −1.77%) · haut méd +0.72% · range méd 1.69%
- Excursion ouverture 15min (n=160) : bas méd −1.08% (p90 −2.99%) · haut méd +0.98% · range méd 2.33%
- Excursion ouverture 30min (n=160) : bas méd −1.2% (p90 −3.34%) · haut méd +1.2% · range méd 2.84%
- Excursion ouverture 60min (n=160) : bas méd −1.52% (p90 −3.79%) · haut méd +1.31% · range méd 3.48%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 16.31 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 75% (124/159) · gap 34% · délai 0.0min · rebond 51% (65/124) (MFE +1.07%)
   - −1.0% : fill 30min 55% · séance 68% (113/159) · gap 27% · délai 0.5min · rebond 61% (70/113) (MFE +1.23%)
   - −1.5% : fill 30min 50% · séance 65% (103/159) · gap 19% · délai 7.3min · rebond 67% (66/103) (MFE +1.57%)
   - −2.0% : fill 30min 40% · séance 52% (77/159) · gap 12% · délai 3.3min · rebond 71% (53/77) (MFE +1.88%)
   - −3.0% : fill 30min 18% · séance 40% (58/159) · gap 4% · délai 31.4min · rebond 66% (40/58) (MFE +1.57%)
   - −4.0% : fill 30min 11% · séance 24% (39/159) · gap 3% · délai 41.0min · rebond 57% (25/39) (MFE +1.46%)
   - −5.0% : fill 30min 5% · séance 9% (18/159) · gap 2% · délai 26.7min · rebond 40% (10/18) (MFE +0.71%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.4% (p90 −2.12%) → stop au-delà de −1.38% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.47% (p90 −1.82%) → stop au-delà de −1.42% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −1.94%) → stop au-delà de −1.13% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=659 jambes) : jambe baissière méd −1.12% (p90 −2.81%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (67 séances) :
      · −1.0% : fill 97% (66/67) · rebond 60% (41/66)
      · −2.0% : fill 85% (54/67) · rebond 71% (39/54)
      · −3.0% : fill 71% (44/67) · rebond 73% (33/44)
      · −4.0% : fill 42% (29/67) · rebond 65% (21/29)
      · −5.0% : fill 20% (14/67) · rebond 38% (8/14)
   - **flat** (24 séances) :
      · −1.0% : fill 54% (14/24) · rebond 46% (7/14)
      · −2.0% : fill 39% (8/24) · rebond 58% (4/8)
      · −3.0% : fill 34% (6/24) · rebond 57% (3/6)
      · −4.0% : fill 14% (3/24) · rebond 67% (1/3)
      · −5.0% : fill 1% (1/24) · rebond 0% (0/1)
   - **gap-up** (68 séances) :
      · −1.0% : fill 46% (33/68) · rebond 67% (22/33)
      · −2.0% : fill 24% (15/68) · rebond 78% (10/15)
      · −3.0% : fill 12% (8/68) · rebond 39% (4/8)
      · −4.0% : fill 9% (7/68) · rebond 20% (3/7)
      · −5.0% : fill 2% (3/68) · rebond 70% (2/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 55% si les 15 1res min sont vertes (72 cas) · 30% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 76% si début vert vs 13% si rouge (base 42% · écart 63 pts) ; prédictivité sature ensuite (plafond brut 228min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=68) : tient le vert **76%** · continue >prix actuel 54% ; creux résiduel méd -1.51% (q20 -3.36%) → **SL/trailing à −3.36%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.88% / q75 +2.81% → **scale +1.88% / runner +2.81%**, sortie à la clôture
  - **si ROUGE au coude** (n=92) : edge inversé — récupère vert seulement **13%** (continue à baisser 56%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.13%** (au-delà de la MAE q10 -3.13%), cible rebond +1.39% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.92% .. +3.36%] · haut q95 +3.76% · bas q05 -3.57%
   - 60min (n=160) : retour [-3.13% .. +3.36%] · haut q95 +3.95% · bas q05 -4.0%
   - 2h (n=160) : retour [-3.58% .. +3.6%] · haut q95 +4.43% · bas q05 -4.64%
   - 4h (n=160) : retour [-3.86% .. +4.62%] · haut q95 +5.68% · bas q05 -5.06%
   - 6h (n=160) : retour [-4.61% .. +4.1%] · haut q95 +5.72% · bas q05 -5.08%
   - session (n=160) : retour [-4.54% .. +5.18%] · haut q95 +5.72% · bas q05 -5.2%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (4) pour des stats fiables : 2.5% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.91%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 46.9  _(neutre)_
- **ADX** : 15.9  _(pas de tendance nette)_
- **MACD** : hist -0.042  _(pas de croisement recent)_
- **BB** : %B 0.7 · largeur 20.6%
- **ATR** : 0.94 (28.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.041  _(neutre)_
- **Vol ratio** : 0.91  _(volume normal)_
- **Choppiness** : 44.3  _(transition)_
- **MA** : MA20 17.33 · MA50 17.24 · MA200 21.26  _(prix > MA20)_
- **Dist MA** : MA20 +4.1% · MA50 +4.6% · MA200 -15.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (85759 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
