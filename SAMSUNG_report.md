# 005930

**Generated** : 2026-07-30T00:13:55.631095+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩208500.00  

> ⛔ **STAND-DOWN** — mise optimale nulle (Kelly ≤ 0) — edge trop ténu pour s'engager (EV blended à peine positive ; cf. badge pour la méthode/n des probas)  
> ↳ spot ₩208500.00 (+12.0% vs entrée) · entrée ₩186161.97 · stop ₩167973.26 · T1 ₩222539.39 · R/R 2.0  
> ↳ P(T1 av. stop) 8 % · EV/risk 0.218 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -64 % hors [0,100] (R² max 0.97). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩183165.67–₩189158.27 (mid ₩186161.97)
- Spot actuel : ₩208500.00 (+12.0% au-dessus de la zone — repli à attendre)
- Stop : ₩167973.26 (stop swing_plan-based (-19.44%))
- Targets : T1 ₩222539.39 · R/R 2.0 | T2 ₩226754.82 · R/R 2.23 | T3 ₩230970.26 · R/R 2.46
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩167973.26


## Edge, scénarios & sizing

- EV/risk : 0.218 | EV/share : ₩3959.972 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 8 % | T2 4 % | T3 2 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 7.9 | bear 69.8 | side 22.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.873% → cible +5.154% / stop −3.655%, p_fill 33%, n_eff≈12.1) : P(cible|rempli) **4%** · **EV/risk -0.044** (×p_fill ; si rempli -0.48% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=8, n_eff=7))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→65% · +2.0%→45% · +3.0%→30% · +5.0%→20% · +8.0%→5%
- Range intraday médian 5.58% (p90 9.05%) · excursion haute méd. +1.83% / basse méd. −2.61%
- Profil de vol intra : ouverture 2.823% vs midi 1.21% vs clôture 1.417% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (142 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 13% · trend ↑1%/↓1% ; spike-down 67% · recovery-V 21%)_
- **Régime intraday** : **chop** _(efficiency 0.133 ; mean-reverting — autocorr -0.086)_ ; drift intra méd. -1.17% ; recovery-V 20%
- **σ réalisé intraday** 4.301% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 41% / bas 76% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 229762.5 (VA 222412.5–232912.5 ; dernier close 219500.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 31% · rebond 63% · **stop −6.63%** sous le fill (sous le bruit) · cible +1.38% · R/R 0.21 (high win-rate)
- Gaps overnight (n=141) : méd. 0.12% · baisse 46% (gap-down >1% 37% · >2% 25%)
- Excursion ouverture 5min (n=142) : bas méd −0.56% (p90 −1.46%) · haut méd +0.64% · range méd 1.41%
- Excursion ouverture 15min (n=142) : bas méd −0.9% (p90 −2.34%) · haut méd +1.04% · range méd 2.08%
- Excursion ouverture 30min (n=142) : bas méd −1.21% (p90 −2.82%) · haut méd +1.1% · range méd 2.49%
- Excursion ouverture 60min (n=142) : bas méd −1.56% (p90 −3.41%) · haut méd +1.35% · range méd 3.06%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 219500.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 54% · séance 67% (88/141) · gap 39% · délai 0.0min · rebond 53% (48/88) (MFE +1.4%)
   - −1.0% : fill 30min 50% · séance 64% (82/141) · gap 37% · délai 0.0min · rebond 60% (47/82) (MFE +1.39%)
   - −1.5% : fill 30min 45% · séance 58% (72/141) · gap 27% · délai 0.2min · rebond 58% (43/72) (MFE +1.64%)
   - −2.0% : fill 30min 42% · séance 50% (63/141) · gap 25% · délai 0.0min · rebond 55% (36/63) (MFE +1.48%)
   - −3.0% : fill 30min 32% · séance 45% (54/141) · gap 21% · délai 0.8min · rebond 58% (35/54) (MFE +1.85%)
   - −4.0% : fill 30min 24% · séance 38% (43/141) · gap 15% · délai 16.3min · rebond 60% (29/43) (MFE +1.65%)
   - −5.0% : fill 30min 15% · séance 31% (33/141) · gap 10% · délai 60.3min · rebond 63% (22/33) (MFE +1.38%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.34% (p90 −1.75%) → stop au-delà de −1.14% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.38% (p90 −2.56%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.31% (p90 −2.14%) → stop au-delà de −1.12% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=628 jambes) : jambe baissière méd −1.31% (p90 −3.08%) · ~12.2 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (61 séances) :
      · −1.0% : fill 97% (58/61) · rebond 48% (30/58)
      · −2.0% : fill 89% (50/61) · rebond 44% (25/50)
      · −3.0% : fill 86% (45/61) · rebond 52% (28/45)
      · −4.0% : fill 76% (37/61) · rebond 55% (24/37)
      · −5.0% : fill 65% (29/61) · rebond 59% (18/29)
   - **flat** (13 séances) :
      · −1.0% : fill 58% (7/13) · rebond 70% (4/7)
      · −2.0% : fill 40% (4/13) · rebond 85% (3/4)
      · −3.0% : fill 40% (4/13) · rebond 85% (3/4)
      · −4.0% : fill 18% (2/13) · rebond 100% (2/2)
      · −5.0% : fill 18% (2/13) · rebond 100% (2/2)
   - **gap-up** (67 séances) :
      · −1.0% : fill 36% (17/67) · rebond 86% (13/17)
      · −2.0% : fill 17% (9/67) · rebond 94% (8/9)
      · −3.0% : fill 9% (5/67) · rebond 89% (4/5)
      · −4.0% : fill 8% (4/67) · rebond 88% (3/4)
      · −5.0% : fill 2% (2/67) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=142) : 42% en base · 67% si les 15 1res min sont vertes (70 cas) · 17% si rouges (72 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=142) : COUDE à **1:14** → P(séance verte=clôture>ouverture) 82% si début vert vs 8% si rouge (base 42% · écart 74 pts) ; prédictivité sature ensuite (plafond brut 129min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **82%** · continue >prix actuel 52% ; creux résiduel méd -1.59% (q20 -4.19%) → **SL/trailing à −4.19%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.54% / q75 +3.38% → **scale +1.54% / runner +3.38%**, sortie à la clôture
  - **si ROUGE au coude** (n=66) : edge inversé — récupère vert seulement **8%** (continue à baisser 56%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.19%** (au-delà de la MAE q10 -7.19%), cible rebond +1.03% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=142) : retour [-2.64% .. +3.09%] · haut q95 +4.03% · bas q05 -3.2%
   - 60min (n=142) : retour [-3.13% .. +4.87%] · haut q95 +5.97% · bas q05 -3.59%
   - 2h (n=142) : retour [-4.49% .. +4.76%] · haut q95 +6.34% · bas q05 -5.12%
   - 4h (n=142) : retour [-6.19% .. +5.83%] · haut q95 +6.84% · bas q05 -7.74%
   - 6h (n=142) : retour [-7.2% .. +5.65%] · haut q95 +7.54% · bas q05 -8.02%
   - session (n=142) : retour [-7.19% .. +5.81%] · haut q95 +7.54% · bas q05 -8.57%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 4.2% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.8%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : stretched_down
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

- **RSI** : 32.3  _(momentum baissier)_
- **ADX** : 26.7  _(tendance etablie)_
- **MACD** : hist -5398.529  _(pas de croisement recent)_
- **BB** : %B -0.03 · largeur 42.5%
- **ATR** : 24164.29 (88.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.263  _(distribution)_
- **Vol ratio** : 2.18  _(volume au-dessus de la moyenne)_
- **Choppiness** : 43.0  _(transition)_
- **MA** : MA20 269100.0 · MA50 301250.0 · MA200 191358.92  _(prix < MA20)_
- **Dist MA** : MA20 -22.5% · MA50 -30.8% · MA200 +9.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (81889 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
