# SMR

**Generated** : 2026-07-10T00:31:10.700282+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $9.03  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $9.03 (+0.4% vs entrée) · entrée $8.99 · stop $8.65 · T1 $9.66 · R/R 1.97  
> ↳ P(T1 av. stop) 13 % _(réel 5 s)_ · EV/risk -0.171 _(réel 5 s)_ (GBM 0.041) · ¼-Kelly 0.04 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.75% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $8.95–$9.03 (mid $8.99)
- Spot actuel : $9.03 (+0.4% au-dessus de la zone — repli à attendre)
- Stop : $8.65 (stop swing_plan-based (-3.96%))
- Targets : T1 $9.66 · R/R 1.97 | T2 $9.71 · R/R 2.12 | T3 $9.76 · R/R 2.26
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $8.65


## Edge, scénarios & sizing

- EV/risk : 0.041 | EV/share : $0.014 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 35 % | T3 35 %
- Kelly (position) : f* 0.159 | ¼-Kelly 0.04 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 24.6 | bear 56.8 | side 18.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.436% → cible +7.501% / stop −3.751%, p_fill 85%, n_eff≈34.4) : P(cible|rempli) **13%** · **EV/risk -0.171** (×p_fill ; si rempli -0.75% du capital)
  - **swing** (entrée dip −0.785% → cible +6.399% / stop −3.2%, p_fill 88%, n_eff≈35.4) : P(cible|rempli) **36%** · **EV/risk +0.020** (×p_fill ; si rempli +0.07% du capital)
  - **deep** (entrée dip −1.115% → cible +9.05% / stop −4.526%, p_fill 84%, n_eff≈34.2) : P(cible|rempli) **23%** · **EV/risk -0.257** (×p_fill ; si rempli -1.39% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→78% · +2.0%→66% · +3.0%→55% · +5.0%→38% · +8.0%→18%
- Range intraday médian 7.31% (p90 12.61%) · excursion haute méd. +3.5% / basse méd. −3.16%
- Profil de vol intra : ouverture 4.937% vs midi 1.55% vs clôture 1.739% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 75% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; neutre — autocorr 0.028)_ ; drift intra méd. -0.289% ; recovery-V 14%
- **σ réalisé intraday** 5.126% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 55% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 8.7248 (VA 8.6343–8.7894 ; dernier close 8.755)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 62% · rebond 77% · **stop −6.89%** sous le fill (sous le bruit) · cible +2.81% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. -0.76% · baisse 62% (gap-down >1% 43% · >2% 30%)
- Excursion ouverture 5min (n=160) : bas méd −1.18% (p90 −3.44%) · haut méd +1.09% · range méd 2.84%
- Excursion ouverture 15min (n=160) : bas méd −1.62% (p90 −3.9%) · haut méd +1.49% · range méd 3.86%
- Excursion ouverture 30min (n=160) : bas méd −1.82% (p90 −5.13%) · haut méd +2.14% · range méd 4.47%
- Excursion ouverture 60min (n=160) : bas méd −2.1% (p90 −6.27%) · haut méd +2.65% · range méd 5.63%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 8.755 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 76% · séance 83% (131/159) · gap 53% · délai 0.0min · rebond 67% (81/131) (MFE +1.74%)
   - −1.0% : fill 30min 69% · séance 80% (126/159) · gap 43% · délai 0.0min · rebond 67% (83/126) (MFE +1.96%)
   - −1.5% : fill 30min 65% · séance 77% (120/159) · gap 39% · délai 0.0min · rebond 75% (87/120) (MFE +2.21%)
   - −2.0% : fill 30min 61% · séance 71% (114/159) · gap 30% · délai 0.2min · rebond 69% (82/114) (MFE +2.54%)
   - −3.0% : fill 30min 50% · séance 62% (102/159) · gap 13% · délai 1.7min · rebond 77% (83/102) (MFE +2.81%)
   - −4.0% : fill 30min 38% · séance 56% (86/159) · gap 6% · délai 9.3min · rebond 75% (66/86) (MFE +2.58%)
   - −5.0% : fill 30min 25% · séance 41% (63/159) · gap 4% · délai 19.5min · rebond 70% (46/63) (MFE +1.86%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.88% (p90 −2.73%) → stop au-delà de −2.07% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.03% (p90 −2.97%) → stop au-delà de −2.13% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.05% (p90 −3.47%) → stop au-delà de −2.23% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1185 jambes) : jambe baissière méd −1.39% (p90 −3.19%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (86 séances) :
      · −1.0% : fill 100% (86/86) · rebond 72% (57/86)
      · −2.0% : fill 93% (82/86) · rebond 75% (61/82)
      · −3.0% : fill 84% (78/86) · rebond 83% (65/78)
      · −4.0% : fill 75% (67/86) · rebond 81% (55/67)
      · −5.0% : fill 56% (47/86) · rebond 76% (37/47)
   - **flat** (13 séances) :
      · −1.0% : fill 76% (10/13) · rebond 41% (6/10)
      · −2.0% : fill 63% (8/13) · rebond 29% (4/8)
      · −3.0% : fill 59% (6/13) · rebond 27% (3/6)
      · −4.0% : fill 59% (6/13) · rebond 38% (2/6)
      · −5.0% : fill 47% (5/13) · rebond 70% (4/5)
   - **gap-up** (60 séances) :
      · −1.0% : fill 49% (30/60) · rebond 63% (20/30)
      · −2.0% : fill 38% (24/60) · rebond 62% (17/24)
      · −3.0% : fill 28% (18/60) · rebond 77% (15/18)
      · −4.0% : fill 24% (13/60) · rebond 67% (9/13)
      · −5.0% : fill 18% (11/60) · rebond 41% (5/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 54% si les 15 1res min sont vertes (68 cas) · 34% si rouges (92 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:25** → P(séance verte=clôture>ouverture) 76% si début vert vs 13% si rouge (base 43% · écart 63 pts) ; prédictivité sature ensuite (plafond brut 233min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **76%** · continue >prix actuel 45% ; creux résiduel méd -2.45% (q20 -3.98%) → **SL/trailing à −3.98%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.21% / q75 +4.22% → **scale +2.21% / runner +4.22%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **13%** (continue à baisser 56%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.16%** (au-delà de la MAE q10 -6.16%), cible rebond +1.59% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.64% .. +4.91%] · haut q95 +6.59% · bas q05 -6.49%
   - 60min (n=160) : retour [-6.85% .. +5.76%] · haut q95 +8.12% · bas q05 -7.93%
   - 2h (n=160) : retour [-7.92% .. +8.78%] · haut q95 +11.36% · bas q05 -8.96%
   - 4h (n=160) : retour [-8.76% .. +8.33%] · haut q95 +11.36% · bas q05 -10.72%
   - 6h (n=160) : retour [-8.56% .. +8.76%] · haut q95 +11.58% · bas q05 -10.78%
   - session (n=160) : retour [-8.39% .. +10.82%] · haut q95 +11.74% · bas q05 -10.8%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 4.98%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 37.6  _(momentum baissier)_
- **ADX** : 14.0  _(pas de tendance nette)_
- **MACD** : hist -0.116  _(pas de croisement recent)_
- **BB** : %B 0.17 · largeur 29.6%
- **ATR** : 0.81 (9.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.156  _(distribution)_
- **Vol ratio** : 0.56  _(volume atone)_
- **Choppiness** : 46.7  _(transition)_
- **MA** : MA20 10.02 · MA50 11.13 · MA200 18.95  _(prix < MA20)_
- **Dist MA** : MA20 -9.9% · MA50 -18.9% · MA200 -52.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83302 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
