# AL2SI

**Generated** : 2026-08-07T21:46:03.673945+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · €27.60  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot €27.60 (+10.1% vs entrée) · entrée €25.06 · stop €22.43 · T1 €26.89 · R/R 0.7  
> ↳ P(T1 av. stop) 61 % _(réel 5 s)_ · EV/risk -0.03 _(réel 5 s)_ (GBM 0.14) · ¼-Kelly 0.027 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €24.70–€25.43 (mid €25.06)
- Spot actuel : €27.60 (+10.1% au-dessus de la zone — repli à attendre)
- Stop : €22.43 (stop swing_plan-based (-18.74%))
- Targets : T1 €26.89 · R/R 0.7 | T2 €28.72 · R/R 1.39 | T3 €30.55 · R/R 2.09
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €22.43


## Edge, scénarios & sizing

- EV/risk : 0.14 | EV/share : €0.369 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 58 % | T2 32 % | T3 20 %
- Kelly (position) : f* 0.107 | ¼-Kelly 0.027 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 69.1 | bear 25.0 | side 6.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 276.0 (= 10 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.174% → cible +3.264% / stop −2.991%, p_fill 56%, n_eff≈24.9) : P(cible|rempli) **33%** · **EV/risk -0.107** (×p_fill ; si rempli -0.58% du capital)
  - **swing** (entrée dip −9.185% → cible +7.298% / stop −10.521%, p_fill 49%, n_eff≈18.6) : P(cible|rempli) **61%** · **EV/risk -0.030** (×p_fill ; si rempli -0.65% du capital)
  - **deep** (entrée dip −14.198% → cible +10.321% / stop −16.704%, p_fill 39%, n_eff≈16.7) : P(cible|rempli) **45%** · **EV/risk -0.119** (×p_fill ; si rempli -5.10% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→78% · +2.0%→70% · +3.0%→60% · +5.0%→42% · +8.0%→19%
- Range intraday médian 8.37% (p90 22.19%) · excursion haute méd. +4.23% / basse méd. −4.64%
- Profil de vol intra : ouverture 5.656% vs midi 1.759% vs clôture 1.96% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 11% · trend ↑0%/↓1% ; spike-down 77% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.139 ; mean-reverting — autocorr -0.061)_ ; drift intra méd. -0.202% ; recovery-V 33%
- **σ réalisé intraday** 7.293% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 69% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 28.1187 (VA 27.5403–28.5637 ; dernier close 28.02)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 44% · rebond 86% · **stop −5.28%** sous le fill (sous le bruit) · cible +2.4% · R/R 0.45 (high win-rate)
- Gaps overnight (n=159) : méd. 0.23% · baisse 38% (gap-down >1% 22% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −1.3% (p90 −4.84%) · haut méd +1.1% · range méd 3.13%
- Excursion ouverture 15min (n=160) : bas méd −1.73% (p90 −5.86%) · haut méd +1.62% · range méd 4.2%
- Excursion ouverture 30min (n=160) : bas méd −1.75% (p90 −5.86%) · haut méd +2.35% · range méd 4.89%
- Excursion ouverture 60min (n=160) : bas méd −2.25% (p90 −6.96%) · haut méd +2.84% · range méd 6.15%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 28.02 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 82% (124/159) · gap 28% · délai 0.3min · rebond 68% (83/124) (MFE +3.33%)
   - −1.0% : fill 30min 59% · séance 81% (120/159) · gap 22% · délai 0.4min · rebond 68% (83/120) (MFE +2.59%)
   - −1.5% : fill 30min 53% · séance 77% (110/159) · gap 16% · délai 0.8min · rebond 70% (74/110) (MFE +2.2%)
   - −2.0% : fill 30min 44% · séance 67% (95/159) · gap 10% · délai 3.4min · rebond 62% (61/95) (MFE +1.79%)
   - −3.0% : fill 30min 34% · séance 57% (78/159) · gap 5% · délai 8.0min · rebond 80% (64/78) (MFE +2.05%)
   - −4.0% : fill 30min 27% · séance 49% (67/159) · gap 4% · délai 22.0min · rebond 75% (52/67) (MFE +2.49%)
   - −5.0% : fill 30min 18% · séance 44% (60/159) · gap 3% · délai 42.3min · rebond 86% (55/60) (MFE +2.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −1.0% (p90 −5.34%) → stop au-delà de −3.05% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.36% (p90 −5.44%) → stop au-delà de −3.88% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.36% (p90 −5.44%) → stop au-delà de −3.83% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1558 jambes) : jambe baissière méd −1.3% (p90 −3.52%) · ~20.9 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 99% (51/54) · rebond 68% (34/51)
      · −2.0% : fill 84% (43/54) · rebond 56% (26/43)
      · −3.0% : fill 78% (39/54) · rebond 82% (32/39)
      · −4.0% : fill 68% (34/54) · rebond 79% (28/34)
      · −5.0% : fill 61% (31/54) · rebond 84% (28/31)
   - **flat** (35 séances) :
      · −1.0% : fill 87% (28/35) · rebond 79% (22/28)
      · −2.0% : fill 68% (21/35) · rebond 83% (16/21)
      · −3.0% : fill 54% (15/35) · rebond 82% (13/15)
      · −4.0% : fill 48% (14/35) · rebond 84% (12/14)
      · −5.0% : fill 42% (12/35) · rebond 100% (12/12)
   - **gap-up** (70 séances) :
      · −1.0% : fill 66% (41/70) · rebond 61% (27/41)
      · −2.0% : fill 56% (31/70) · rebond 56% (19/31)
      · −3.0% : fill 45% (24/70) · rebond 76% (19/24)
      · −4.0% : fill 38% (19/70) · rebond 64% (12/19)
      · −5.0% : fill 34% (17/70) · rebond 79% (15/17)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 59% si les 15 1res min sont vertes (78 cas) · 35% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **3:06** → P(séance verte=clôture>ouverture) 86% si début vert vs 11% si rouge (base 47% · écart 75 pts) ; prédictivité sature ensuite (plafond brut 252min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **86%** · continue >prix actuel 58% ; creux résiduel méd -1.74% (q20 -3.87%) → **SL/trailing à −3.87%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.55% / q75 +5.8% → **scale +2.55% / runner +5.8%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **11%** (continue à baisser 64%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.25%** (au-delà de la MAE q10 -8.25%), cible rebond +1.27% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.66% .. +6.18%] · haut q95 +8.22% · bas q05 -7.64%
   - 60min (n=160) : retour [-5.91% .. +9.04%] · haut q95 +9.58% · bas q05 -7.84%
   - 2h (n=160) : retour [-6.17% .. +9.84%] · haut q95 +10.32% · bas q05 -8.02%
   - 4h (n=160) : retour [-7.73% .. +9.66%] · haut q95 +12.31% · bas q05 -10.85%
   - 6h (n=160) : retour [-6.8% .. +10.62%] · haut q95 +14.76% · bas q05 -11.11%
   - session (n=160) : retour [-8.45% .. +13.69%] · haut q95 +15.13% · bas q05 -12.21%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.44%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 54.6  _(neutre)_
- **ADX** : 20.0  _(pas de tendance nette)_
- **MACD** : hist 0.595  _(pas de croisement recent)_
- **BB** : %B 0.61 · largeur 25.2%
- **ATR** : 2.64 (67.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.162  _(distribution)_
- **Vol ratio** : 0.33  _(volume atone)_
- **Choppiness** : 61.9  _(marche en range (choppy))_
- **MA** : MA20 26.87 · MA50 35.0 · MA200 24.99  _(prix > MA20)_
- **Dist MA** : MA20 +2.7% · MA50 -21.1% · MA200 +10.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92963 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
