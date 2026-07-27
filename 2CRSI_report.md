# AL2SI

**Generated** : 2026-07-27T21:45:14.088276+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €27.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot €27.00 (+9.8% vs entrée) · entrée €24.58 · stop €23.47 · T1 €26.78 · R/R 1.98  
> ↳ P(T1 av. stop) 25 % _(réel 5 s)_ · EV/risk -0.179 _(réel 5 s)_ (GBM 0.289) · ¼-Kelly 0.013 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €24.14–€25.02 (mid €24.58)
- Spot actuel : €27.00 (+9.8% au-dessus de la zone — repli à attendre)
- Stop : €23.47 (stop swing_plan-based (-13.06%))
- Targets : T1 €26.78 · R/R 1.98 | T2 €28.97 · R/R 3.95 | T3 €31.17 · R/R 5.94
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €23.47


## Edge, scénarios & sizing

- EV/risk : 0.289 | EV/share : €0.320 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 19 % | T3 12 %
- Kelly (position) : f* 0.052 | ¼-Kelly 0.013 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 36.8 | bear 52.3 | side 10.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 270.0 (= 10 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.076% → cible +3.996% / stop −4.268%, p_fill 62%, n_eff≈24.4) : P(cible|rempli) **41%** · **EV/risk -0.038** (×p_fill ; si rempli -0.26% du capital)
  - **swing** (entrée dip −8.966% → cible +8.936% / stop −4.497%, p_fill 45%, n_eff≈16.7) : P(cible|rempli) **25%** · **EV/risk -0.179** (×p_fill ; si rempli -1.77% du capital)
  - **deep** (entrée dip −13.847% → cible +12.637% / stop −6.318%, p_fill 49%, n_eff≈15.2) : P(cible|rempli) **10%** · **EV/risk -0.352** (×p_fill ; si rempli -4.53% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→80% · +2.0%→74% · +3.0%→64% · +5.0%→45% · +8.0%→24%
- Range intraday médian 8.95% (p90 22.19%) · excursion haute méd. +4.29% / basse méd. −4.31%
- Profil de vol intra : ouverture 5.945% vs midi 1.751% vs clôture 2.032% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (156 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 9% · trend ↑0%/↓1% ; spike-down 79% · recovery-V 37%)_
- **Régime intraday** : **chop** _(efficiency 0.136 ; mean-reverting — autocorr -0.042)_ ; drift intra méd. -0.097% ; recovery-V 34%
- **σ réalisé intraday** 8.361% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 65% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 27.6325 (VA 27.3725–27.8925 ; dernier close 27.64)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 46% · rebond 89% · **stop −5.51%** sous le fill (sous le bruit) · cible +3.1% · R/R 0.56 (high win-rate)
- Gaps overnight (n=155) : méd. 0.21% · baisse 39% (gap-down >1% 22% · >2% 10%)
- Excursion ouverture 5min (n=156) : bas méd −1.29% (p90 −5.15%) · haut méd +1.04% · range méd 3.14%
- Excursion ouverture 15min (n=156) : bas méd −1.68% (p90 −5.84%) · haut méd +1.55% · range méd 4.51%
- Excursion ouverture 30min (n=156) : bas méd −1.78% (p90 −5.86%) · haut méd +2.41% · range méd 4.97%
- Excursion ouverture 60min (n=156) : bas méd −2.4% (p90 −6.96%) · haut méd +2.85% · range méd 6.3%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 27.64 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 83% (122/155) · gap 29% · délai 0.3min · rebond 72% (83/122) (MFE +3.6%)
   - −1.0% : fill 30min 62% · séance 81% (117/155) · gap 22% · délai 0.4min · rebond 75% (83/117) (MFE +3.13%)
   - −1.5% : fill 30min 55% · séance 77% (107/155) · gap 15% · délai 1.0min · rebond 75% (73/107) (MFE +2.58%)
   - −2.0% : fill 30min 48% · séance 70% (94/155) · gap 10% · délai 3.1min · rebond 68% (63/94) (MFE +1.94%)
   - −3.0% : fill 30min 36% · séance 60% (77/155) · gap 6% · délai 8.1min · rebond 87% (65/77) (MFE +2.34%)
   - −4.0% : fill 30min 28% · séance 50% (65/155) · gap 4% · délai 22.1min · rebond 75% (50/65) (MFE +2.72%)
   - −5.0% : fill 30min 20% · séance 46% (57/155) · gap 4% · délai 64.4min · rebond 89% (53/57) (MFE +3.1%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −1.04% (p90 −5.54%) → stop au-delà de −3.86% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.35% (p90 −5.54%) → stop au-delà de −4.02% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.35% (p90 −5.58%) → stop au-delà de −3.97% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1523 jambes) : jambe baissière méd −1.29% (p90 −3.63%) · ~21.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 98% (50/54) · rebond 70% (34/50)
      · −2.0% : fill 88% (43/54) · rebond 60% (27/43)
      · −3.0% : fill 80% (38/54) · rebond 80% (31/38)
      · −4.0% : fill 70% (33/54) · rebond 77% (27/33)
      · −5.0% : fill 63% (30/54) · rebond 83% (27/30)
   - **flat** (33 séances) :
      · −1.0% : fill 85% (26/33) · rebond 84% (21/26)
      · −2.0% : fill 71% (20/33) · rebond 81% (15/20)
      · −3.0% : fill 55% (14/33) · rebond 95% (13/14)
      · −4.0% : fill 47% (13/33) · rebond 81% (11/13)
      · −5.0% : fill 41% (11/33) · rebond 100% (11/11)
   - **gap-up** (68 séances) :
      · −1.0% : fill 67% (41/68) · rebond 73% (28/41)
      · −2.0% : fill 56% (31/68) · rebond 69% (21/31)
      · −3.0% : fill 47% (25/68) · rebond 91% (21/25)
      · −4.0% : fill 38% (19/68) · rebond 68% (12/19)
      · −5.0% : fill 37% (16/68) · rebond 89% (15/16)
- **P(clôture VERTE) selon le drive 15min** (n=156) : 47% en base · 57% si les 15 1res min sont vertes (75 cas) · 38% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=156) : COUDE à **44min** → P(séance verte=clôture>ouverture) 75% si début vert vs 21% si rouge (base 47% · écart 53 pts) ; prédictivité sature ensuite (plafond brut 252min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **75%** · continue >prix actuel 56% ; creux résiduel méd -2.59% (q20 -5.85%) → **SL/trailing à −5.85%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.22% / q75 +5.55% → **scale +3.22% / runner +5.55%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **21%** (continue à baisser 49%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −10.47%** (au-delà de la MAE q10 -10.47%), cible rebond +2.81% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=156) : retour [-5.23% .. +6.52%] · haut q95 +8.42% · bas q05 -7.72%
   - 60min (n=156) : retour [-5.97% .. +9.26%] · haut q95 +9.87% · bas q05 -8.03%
   - 2h (n=156) : retour [-6.01% .. +10.01%] · haut q95 +11.18% · bas q05 -8.17%
   - 4h (n=156) : retour [-8.62% .. +10.18%] · haut q95 +12.41% · bas q05 -11.24%
   - 6h (n=156) : retour [-7.93% .. +14.32%] · haut q95 +16.09% · bas q05 -11.27%
   - session (n=156) : retour [-9.96% .. +15.77%] · haut q95 +17.32% · bas q05 -15.26%


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 26.6  _(survente)_
- **ADX** : 24.5  _(pas de tendance nette)_
- **MACD** : hist 0.186  _(bullish_recent)_
- **BB** : %B 0.31 · largeur 60.4%
- **ATR** : 3.68 (84.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.104  _(distribution)_
- **Vol ratio** : 0.72  _(volume normal)_
- **Choppiness** : 49.7  _(transition)_
- **MA** : MA20 30.51 · MA50 38.15 · MA200 24.49  _(prix < MA20)_
- **Dist MA** : MA20 -11.5% · MA50 -29.2% · MA200 +10.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93270 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
