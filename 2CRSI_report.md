# AL2SI

**Generated** : 2026-07-30T00:10:21.281376+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €23.80  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €23.80 (+2.9% vs entrée) · entrée €23.14 · stop €22.19 · T1 €24.73 · R/R 1.67  
> ↳ P(T1 av. stop) 33 % _(réel 5 s)_ · EV/risk -0.143 _(réel 5 s)_ (GBM 0.22) · ¼-Kelly 0.014 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €22.82–€23.46 (mid €23.14)
- Spot actuel : €23.80 (+2.9% au-dessus de la zone — repli à attendre)
- Stop : €22.19 (stop swing_plan-based (-6.77%))
- Targets : T1 €24.73 · R/R 1.67 | T2 €26.32 · R/R 3.35 | T3 €27.90 · R/R 5.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €22.19


## Edge, scénarios & sizing

- EV/risk : 0.22 | EV/share : €0.209 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 24 % | T3 17 %
- Kelly (position) : f* 0.058 | ¼-Kelly 0.014 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 27.0 | bear 67.8 | side 5.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.26% → cible +3.069% / stop −4.051%, p_fill 91%, n_eff≈35.3) : P(cible|rempli) **42%** · **EV/risk -0.171** (×p_fill ; si rempli -0.76% du capital)
  - **swing** (entrée dip −2.77% → cible +6.862% / stop −4.114%, p_fill 80%, n_eff≈30.8) : P(cible|rempli) **33%** · **EV/risk -0.143** (×p_fill ; si rempli -0.74% du capital)
  - **deep** (entrée dip −4.285% → cible +9.705% / stop −4.853%, p_fill 77%, n_eff≈27.8) : P(cible|rempli) **23%** · **EV/risk -0.328** (×p_fill ; si rempli -2.05% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→79% · +2.0%→72% · +3.0%→62% · +5.0%→46% · +8.0%→24%
- Range intraday médian 8.82% (p90 22.19%) · excursion haute méd. +4.37% / basse méd. −3.94%
- Profil de vol intra : ouverture 5.861% vs midi 1.766% vs clôture 1.999% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (158 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 8% · trend ↑0%/↓1% ; spike-down 80% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.13 ; mean-reverting — autocorr -0.056)_ ; drift intra méd. -0.334% ; recovery-V 30%
- **σ réalisé intraday** 8.108% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 68% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 25.807 (VA 25.579–26.111 ; dernier close 25.74)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 46% · rebond 89% · **stop −5.42%** sous le fill (sous le bruit) · cible +2.75% · R/R 0.51 (high win-rate)
- Gaps overnight (n=157) : méd. 0.21% · baisse 40% (gap-down >1% 23% · >2% 11%)
- Excursion ouverture 5min (n=158) : bas méd −1.29% (p90 −5.07%) · haut méd +1.04% · range méd 3.08%
- Excursion ouverture 15min (n=158) : bas méd −1.68% (p90 −5.73%) · haut méd +1.55% · range méd 4.47%
- Excursion ouverture 30min (n=158) : bas méd −1.78% (p90 −5.85%) · haut méd +2.33% · range méd 4.97%
- Excursion ouverture 60min (n=158) : bas méd −2.4% (p90 −6.84%) · haut méd +2.74% · range méd 6.23%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 25.74 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 84% (124/157) · gap 30% · délai 0.3min · rebond 68% (83/124) (MFE +3.35%)
   - −1.0% : fill 30min 62% · séance 82% (119/157) · gap 23% · délai 0.4min · rebond 71% (83/119) (MFE +2.65%)
   - −1.5% : fill 30min 55% · séance 78% (109/157) · gap 16% · délai 1.0min · rebond 72% (73/109) (MFE +2.36%)
   - −2.0% : fill 30min 48% · séance 71% (96/157) · gap 11% · délai 3.1min · rebond 65% (63/96) (MFE +1.87%)
   - −3.0% : fill 30min 36% · séance 59% (78/157) · gap 6% · délai 7.5min · rebond 88% (66/78) (MFE +2.31%)
   - −4.0% : fill 30min 28% · séance 50% (66/157) · gap 4% · délai 19.0min · rebond 76% (51/66) (MFE +2.66%)
   - −5.0% : fill 30min 19% · séance 46% (58/157) · gap 4% · délai 42.0min · rebond 89% (54/58) (MFE +2.75%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.99% (p90 −5.52%) → stop au-delà de −3.84% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.32% (p90 −5.53%) → stop au-delà de −3.99% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.25% (p90 −5.56%) → stop au-delà de −3.95% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1544 jambes) : jambe baissière méd −1.3% (p90 −3.6%) · ~21.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 98% (51/55) · rebond 66% (34/51)
      · −2.0% : fill 88% (44/55) · rebond 57% (27/44)
      · −3.0% : fill 82% (39/55) · rebond 82% (32/39)
      · −4.0% : fill 72% (34/55) · rebond 79% (28/34)
      · −5.0% : fill 65% (31/55) · rebond 84% (28/31)
   - **flat** (33 séances) :
      · −1.0% : fill 85% (26/33) · rebond 84% (21/26)
      · −2.0% : fill 71% (20/33) · rebond 81% (15/20)
      · −3.0% : fill 55% (14/33) · rebond 95% (13/14)
      · −4.0% : fill 47% (13/33) · rebond 81% (11/13)
      · −5.0% : fill 41% (11/33) · rebond 100% (11/11)
   - **gap-up** (69 séances) :
      · −1.0% : fill 69% (42/69) · rebond 69% (28/42)
      · −2.0% : fill 57% (32/69) · rebond 64% (21/32)
      · −3.0% : fill 45% (25/69) · rebond 91% (21/25)
      · −4.0% : fill 36% (19/69) · rebond 68% (12/19)
      · −5.0% : fill 35% (16/69) · rebond 89% (15/16)
- **P(clôture VERTE) selon le drive 15min** (n=158) : 45% en base · 55% si les 15 1res min sont vertes (76 cas) · 37% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=158) : COUDE à **44min** → P(séance verte=clôture>ouverture) 72% si début vert vs 21% si rouge (base 45% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 252min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **72%** · continue >prix actuel 53% ; creux résiduel méd -2.63% (q20 -5.6%) → **SL/trailing à −5.6%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.24% / q75 +5.03% → **scale +3.24% / runner +5.03%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **21%** (continue à baisser 47%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −10.34%** (au-delà de la MAE q10 -10.34%), cible rebond +2.6% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=158) : retour [-5.19% .. +6.39%] · haut q95 +8.31% · bas q05 -7.7%
   - 60min (n=158) : retour [-5.95% .. +9.14%] · haut q95 +9.82% · bas q05 -7.87%
   - 2h (n=158) : retour [-5.98% .. +9.94%] · haut q95 +10.97% · bas q05 -8.03%
   - 4h (n=158) : retour [-8.43% .. +10.02%] · haut q95 +12.37% · bas q05 -11.16%
   - 6h (n=158) : retour [-7.48% .. +14.18%] · haut q95 +15.5% · bas q05 -11.24%
   - session (n=158) : retour [-9.87% .. +14.18%] · haut q95 +16.61% · bas q05 -14.6%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.49%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 28.6  _(survente)_
- **ADX** : 24.7  _(pas de tendance nette)_
- **MACD** : hist 0.051  _(bullish_recent)_
- **BB** : %B 0.19 · largeur 62.5%
- **ATR** : 3.17 (76.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.227  _(distribution)_
- **Vol ratio** : 0.48  _(volume atone)_
- **Choppiness** : 61.5  _(transition)_
- **MA** : MA20 29.58 · MA50 37.55 · MA200 24.6  _(prix < MA20)_
- **Dist MA** : MA20 -19.5% · MA50 -36.6% · MA200 -3.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89928 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
