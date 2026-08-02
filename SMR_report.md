# SMR

**Generated** : 2026-08-02T15:04:44.760221+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $8.42  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $8.42 (+3.7% vs entrée) · entrée $8.12 · stop $7.91 · T1 $8.38 · R/R 1.24  
> ↳ P(T1 av. stop) 31 % _(réel 5 s)_ · EV/risk -0.07 _(réel 5 s)_ (GBM 0.119) · ¼-Kelly 0.034 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.53% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $8.07–$8.17 (mid $8.12)
- Spot actuel : $8.42 (+3.7% au-dessus de la zone — repli à attendre)
- Stop : $7.91 (stop swing_plan-based (-16.02%))
- Targets : T1 $8.38 · R/R 1.24 | T2 $8.64 · R/R 2.48 | T3 $8.90 · R/R 3.71
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $7.91


## Edge, scénarios & sizing

- EV/risk : 0.119 | EV/share : $0.024 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 48 % | T2 36 % | T3 36 %
- Kelly (position) : f* 0.135 | ¼-Kelly 0.034 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 76.8 | bear 13.9 | side 9.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.595% → cible +3.208% / stop −2.525%, p_fill 48%, n_eff≈19.3) : P(cible|rempli) **31%** · **EV/risk -0.070** (×p_fill ; si rempli -0.37% du capital)
  - **swing** (entrée dip −7.906% → cible +7.173% / stop −8.81%, p_fill 23%, n_eff≈11.0) : P(cible|rempli) **33%** · **EV/risk -0.059** (×p_fill ; si rempli -2.23% du capital)
  - **deep** (entrée dip −12.22% → cible +10.144% / stop −13.865%, p_fill 29%, n_eff≈11.4) : P(cible|rempli) **65%** · **EV/risk +0.029** (×p_fill ; si rempli +1.41% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→80% · +2.0%→65% · +3.0%→60% · +5.0%→41% · +8.0%→19%
- Range intraday médian 7.83% (p90 12.61%) · excursion haute méd. +3.65% / basse méd. −3.15%
- Profil de vol intra : ouverture 5.152% vs midi 1.565% vs clôture 1.85% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.127 ; mean-reverting — autocorr -0.039)_ ; drift intra méd. -0.114% ; recovery-V 37%
- **σ réalisé intraday** 4.892% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 69% / whipsaw 25%
- POC intraday (dernière séance, temps-au-prix) : 8.6694 (VA 8.4849–8.7156 ; dernier close 8.43)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 52% · rebond 77% · **stop −5.95%** sous le fill (sous le bruit) · cible +2.56% · R/R 0.43 (high win-rate)
- Gaps overnight (n=159) : méd. -0.53% · baisse 58% (gap-down >1% 43% · >2% 30%)
- Excursion ouverture 5min (n=160) : bas méd −1.08% (p90 −3.15%) · haut méd +1.12% · range méd 2.7%
- Excursion ouverture 15min (n=160) : bas méd −1.39% (p90 −3.62%) · haut méd +1.52% · range méd 3.52%
- Excursion ouverture 30min (n=160) : bas méd −1.79% (p90 −4.57%) · haut méd +2.13% · range méd 4.37%
- Excursion ouverture 60min (n=160) : bas méd −2.14% (p90 −5.72%) · haut méd +2.65% · range méd 5.36%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 8.43 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 73% · séance 81% (131/159) · gap 50% · délai 0.0min · rebond 67% (81/131) (MFE +1.83%)
   - −1.0% : fill 30min 66% · séance 78% (126/159) · gap 43% · délai 0.0min · rebond 69% (84/126) (MFE +2.13%)
   - −1.5% : fill 30min 62% · séance 75% (120/159) · gap 38% · délai 0.0min · rebond 75% (89/120) (MFE +2.31%)
   - −2.0% : fill 30min 57% · séance 69% (113/159) · gap 30% · délai 0.1min · rebond 70% (83/113) (MFE +2.52%)
   - −3.0% : fill 30min 46% · séance 59% (100/159) · gap 11% · délai 2.0min · rebond 75% (81/100) (MFE +2.59%)
   - −4.0% : fill 30min 35% · séance 52% (84/159) · gap 6% · délai 11.3min · rebond 77% (65/84) (MFE +2.56%)
   - −5.0% : fill 30min 25% · séance 41% (63/159) · gap 3% · délai 19.6min · rebond 71% (46/63) (MFE +2.13%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.7% (p90 −2.71%) → stop au-delà de −1.86% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.7% (p90 −2.97%) → stop au-delà de −2.15% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.03% (p90 −3.35%) → stop au-delà de −2.48% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1177 jambes) : jambe baissière méd −1.4% (p90 −3.28%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (85 séances) :
      · −1.0% : fill 100% (85/85) · rebond 70% (57/85)
      · −2.0% : fill 94% (81/85) · rebond 75% (62/81)
      · −3.0% : fill 85% (76/85) · rebond 77% (63/76)
      · −4.0% : fill 75% (66/85) · rebond 81% (54/66)
      · −5.0% : fill 60% (48/85) · rebond 74% (37/48)
   - **flat** (13 séances) :
      · −1.0% : fill 80% (10/13) · rebond 53% (6/10)
      · −2.0% : fill 69% (8/13) · rebond 22% (4/8)
      · −3.0% : fill 66% (6/13) · rebond 46% (3/6)
      · −4.0% : fill 66% (6/13) · rebond 56% (3/6)
      · −5.0% : fill 56% (5/13) · rebond 79% (4/5)
   - **gap-up** (61 séances) :
      · −1.0% : fill 46% (31/61) · rebond 73% (21/31)
      · −2.0% : fill 34% (24/61) · rebond 71% (17/24)
      · −3.0% : fill 22% (18/61) · rebond 80% (15/18)
      · −4.0% : fill 17% (12/61) · rebond 67% (8/12)
      · −5.0% : fill 12% (10/61) · rebond 42% (5/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 60% si les 15 1res min sont vertes (73 cas) · 32% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **40min** → P(séance verte=clôture>ouverture) 67% si début vert vs 19% si rouge (base 46% · écart 48 pts) ; prédictivité sature ensuite (plafond brut 176min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=84) : tient le vert **67%** · continue >prix actuel 44% ; creux résiduel méd -3.14% (q20 -5.06%) → **SL/trailing à −5.06%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.13% / q75 +4.13% → **scale +2.13% / runner +4.13%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **19%** (continue à baisser 54%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.71%** (au-delà de la MAE q10 -6.71%), cible rebond +2.14% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.46% .. +4.96%] · haut q95 +6.47% · bas q05 -6.01%
   - 60min (n=160) : retour [-6.38% .. +5.69%] · haut q95 +7.11% · bas q05 -7.68%
   - 2h (n=160) : retour [-7.49% .. +6.89%] · haut q95 +10.77% · bas q05 -8.27%
   - 4h (n=160) : retour [-7.67% .. +7.62%] · haut q95 +11.02% · bas q05 -10.32%
   - 6h (n=160) : retour [-7.79% .. +8.76%] · haut q95 +11.31% · bas q05 -10.16%
   - session (n=160) : retour [-7.78% .. +9.83%] · haut q95 +11.38% · bas q05 -10.71%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 5.0%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-08-05 — SMR earnings (J-2 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-05 — SMR earnings (J-2 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 50.6  _(neutre)_
- **ADX** : 23.0  _(pas de tendance nette)_
- **MACD** : hist 0.088  _(pas de croisement recent)_
- **BB** : %B 0.47 · largeur 24.3%
- **ATR** : 0.68 (5.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.04  _(neutre)_
- **Vol ratio** : 1.31  _(volume normal)_
- **Choppiness** : 63.3  _(marche en range (choppy))_
- **MA** : MA20 8.48 · MA50 9.97 · MA200 16.44  _(prix < MA20)_
- **Dist MA** : MA20 -0.8% · MA50 -15.5% · MA200 -48.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83376 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
