# EVT

**Generated** : 2026-08-10T21:38:55.812185+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €3.66  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot €3.66 (+3.4% vs entrée) · entrée €3.54 · stop €3.41 · T1 €3.66 · R/R 0.92  
> ↳ P(T1 av. stop) 55 % · EV/risk -0.175 · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.5% cohérent avec le bruit 5 s (EV-optimal ≈ −3.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €3.51–€3.56 (mid €3.54)
- Spot actuel : €3.66 (+3.4% au-dessus de la zone — repli à attendre)
- Stop : €3.41 (stop swing_plan-based (-10.96%))
- Targets : T1 €3.66 · R/R 0.92 | T2 €3.79 · R/R 1.92 | T3 €3.92 · R/R 2.92
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €3.41


## Edge, scénarios & sizing

- EV/risk : -0.041 | EV/share : €-0.005 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 16 % | T2 6 % | T3 6 %
- Kelly (position) : f* 0.001 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 24.3 | bear 5.4 | side 70.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.284% → cible +3.6% / stop −3.501%, p_fill 17%, n_eff≈9.3) : P(cible|rempli) **30%** · **EV/risk -0.003** (×p_fill ; si rempli -0.06% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=8, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=7, n_eff=5))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→70% · +2.0%→45% · +3.0%→24% · +5.0%→6% · +8.0%→1%
- Range intraday médian 3.85% (p90 6.25%) · excursion haute méd. +1.74% / basse méd. −1.78%
- Profil de vol intra : ouverture 2.686% vs midi 1.209% vs clôture 1.193% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 96% · range 4% · trend ↑0%/↓0% ; spike-down 53% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.07 ; mean-reverting — autocorr -0.139)_ ; drift intra méd. -0.387% ; recovery-V 30%
- **σ réalisé intraday** 3.232% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 65% / bas 67% / whipsaw 34%
- POC intraday (dernière séance, temps-au-prix) : 3.5195 (VA 3.4925–3.5195 ; dernier close 3.478)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.0%** sous le close veille · fill 68% · rebond 67% · **stop −3.18%** sous le fill (sous le bruit) · cible +1.58% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. 0.13% · baisse 44% (gap-down >1% 19% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −2.33%) · haut méd +0.63% · range méd 1.44%
- Excursion ouverture 15min (n=160) : bas méd −0.82% (p90 −2.65%) · haut méd +0.85% · range méd 1.76%
- Excursion ouverture 30min (n=160) : bas méd −0.98% (p90 −2.77%) · haut méd +0.96% · range méd 2.08%
- Excursion ouverture 60min (n=160) : bas méd −1.01% (p90 −2.95%) · haut méd +0.97% · range méd 2.38%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.478 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 81% (131/159) · gap 27% · délai 0.2min · rebond 68% (85/131) (MFE +1.44%)
   - −1.0% : fill 30min 48% · séance 68% (115/159) · gap 19% · délai 0.6min · rebond 67% (73/115) (MFE +1.58%)
   - −1.5% : fill 30min 34% · séance 55% (96/159) · gap 13% · délai 3.7min · rebond 59% (60/96) (MFE +1.32%)
   - −2.0% : fill 30min 24% · séance 43% (77/159) · gap 8% · délai 14.9min · rebond 64% (50/77) (MFE +1.43%)
   - −3.0% : fill 30min 13% · séance 28% (53/159) · gap 4% · délai 31.1min · rebond 68% (39/53) (MFE +1.65%)
   - −4.0% : fill 30min 7% · séance 15% (30/159) · gap 2% · délai 35.3min · rebond 49% (18/30) (MFE +1.04%)
   - −5.0% : fill 30min 5% · séance 8% (17/159) · gap 1% · délai 5.0min · rebond 50% (11/17) (MFE +1.35%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.3% (p90 −2.36%) → stop au-delà de −1.45% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.36% (p90 −1.81%) → stop au-delà de −1.26% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.52% (p90 −1.92%) → stop au-delà de −1.33% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=809 jambes) : jambe baissière méd −1.07% (p90 −2.31%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (58 séances) :
      · −1.0% : fill 95% (55/58) · rebond 71% (32/55)
      · −2.0% : fill 64% (41/58) · rebond 60% (25/41)
      · −3.0% : fill 38% (29/58) · rebond 68% (21/29)
      · −4.0% : fill 27% (20/58) · rebond 56% (14/20)
      · −5.0% : fill 16% (13/58) · rebond 57% (9/13)
   - **flat** (43 séances) :
      · −1.0% : fill 69% (32/43) · rebond 68% (24/32)
      · −2.0% : fill 46% (19/43) · rebond 68% (13/19)
      · −3.0% : fill 35% (12/43) · rebond 73% (9/12)
      · −4.0% : fill 15% (5/43) · rebond 20% (1/5)
      · −5.0% : fill 8% (3/43) · rebond 27% (1/3)
   - **gap-up** (58 séances) :
      · −1.0% : fill 43% (28/58) · rebond 59% (17/28)
      · −2.0% : fill 21% (17/58) · rebond 70% (12/17)
      · −3.0% : fill 12% (12/58) · rebond 57% (9/12)
      · −4.0% : fill 5% (5/58) · rebond 80% (3/5)
      · −5.0% : fill 1% (1/58) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 62% si les 15 1res min sont vertes (75 cas) · 40% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **6min** → P(séance verte=clôture>ouverture) 63% si début vert vs 39% si rouge (base 51% · écart 24 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **63%** · continue >prix actuel 42% ; creux résiduel méd -1.84% (q20 -2.89%) → **SL/trailing à −2.89%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.31% / q75 +2.16% → **scale +1.31% / runner +2.16%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **39%** (continue à baisser 43%) → **RÉDUIRE ~61%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.5%** (au-delà de la MAE q10 -4.5%), cible rebond +2.02% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.44% .. +2.4%] · haut q95 +3.5% · bas q05 -3.41%
   - 60min (n=160) : retour [-3.03% .. +2.74%] · haut q95 +4.23% · bas q05 -3.47%
   - 2h (n=160) : retour [-3.47% .. +3.11%] · haut q95 +4.23% · bas q05 -4.21%
   - 4h (n=160) : retour [-2.83% .. +2.66%] · haut q95 +4.23% · bas q05 -4.29%
   - 6h (n=160) : retour [-3.31% .. +3.22%] · haut q95 +4.44% · bas q05 -5.07%
   - session (n=160) : retour [-4.13% .. +4.05%] · haut q95 +5.34% · bas q05 -5.58%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.92%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 58.5  _(momentum haussier)_
- **ADX** : 39.0  _(tendance etablie)_
- **MACD** : hist 0.05  _(pas de croisement recent)_
- **BB** : %B 0.57 · largeur 37.4%
- **ATR** : 0.13 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.023  _(neutre)_
- **Vol ratio** : 1.16  _(volume normal)_
- **Choppiness** : 63.0  _(marche en range (choppy))_
- **MA** : MA20 3.57 · MA50 4.37 · MA200 5.21  _(prix > MA20)_
- **Dist MA** : MA20 +2.5% · MA50 -16.3% · MA200 -29.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90129 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
