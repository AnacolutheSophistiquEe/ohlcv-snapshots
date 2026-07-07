# AL2SI

**Generated** : 2026-07-07T00:08:32.578497+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 15.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · €39.22  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €39.22 (+2.8% vs entrée) · entrée €38.17 · stop €35.88 · T1 €42.74 · R/R 2.0  
> ↳ P(T1 av. stop) 4 % _(réel 5 s)_ · EV/risk -0.073 _(réel 5 s)_ (GBM 0.081) · ¼-Kelly 0.079 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −5.99% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €37.69–€38.65 (mid €38.17)
- Spot actuel : €39.22 (+2.8% au-dessus de la zone — repli à attendre)
- Stop : €35.88 (stop swing_plan-based (-17.18%))
- Targets : T1 €42.74 · R/R 2.0 | T2 €45.41 · R/R 3.16 | T3 €48.07 · R/R 4.32
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €35.88


## Edge, scénarios & sizing

- EV/risk : 0.081 | EV/share : €0.185 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 39 % | T3 39 %
- Kelly (position) : f* 0.314 | ¼-Kelly 0.079 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 14.6 | bear 65.8 | side 19.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 510.0 (= 13 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.68% → cible +11.982% / stop −5.991%, p_fill 68%, n_eff≈25.6) : P(cible|rempli) **4%** · **EV/risk -0.073** (×p_fill ; si rempli -0.65% du capital)
  - **swing** (entrée dip −5.886% → cible +36.128% / stop −12.0%, p_fill 52%, n_eff≈18.2) : P(cible|rempli) **16%** · **EV/risk -0.160** (×p_fill ; si rempli -3.66% du capital)
  - **deep** (entrée dip −9.098% → cible +68.163% / stop −18.0%, p_fill 50%, n_eff≈15.3) : P(cible|rempli) **9%** · **EV/risk -0.307** (×p_fill ; si rempli -11.04% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→81% · +2.0%→76% · +3.0%→65% · +5.0%→41% · +8.0%→22%
- Range intraday médian 7.78% (p90 17.21%) · excursion haute méd. +4.23% / basse méd. −3.05%
- Profil de vol intra : ouverture 5.546% vs midi 1.693% vs clôture 1.943% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (141 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑0%/↓2% ; spike-down 72% · recovery-V 38%)_
- **Régime intraday** : **chop** _(efficiency 0.16 ; neutre — autocorr -0.023)_ ; drift intra méd. 1.114% ; recovery-V 32%
- **σ réalisé intraday** 8.473% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 51% / bas 65% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 36.678 (VA 36.342–37.686 ; dernier close 36.78)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 37% · rebond 88% · **stop −6.02%** sous le fill (sous le bruit) · cible +2.8% · R/R 0.47 (high win-rate)
- Gaps overnight (n=140) : méd. 0.23% · baisse 37% (gap-down >1% 22% · >2% 9%)
- Excursion ouverture 5min (n=141) : bas méd −0.99% (p90 −5.43%) · haut méd +1.05% · range méd 2.98%
- Excursion ouverture 15min (n=141) : bas méd −1.46% (p90 −5.86%) · haut méd +1.51% · range méd 3.94%
- Excursion ouverture 30min (n=141) : bas méd −1.54% (p90 −6.05%) · haut méd +2.05% · range méd 4.69%
- Excursion ouverture 60min (n=141) : bas méd −2.0% (p90 −7.01%) · haut méd +2.64% · range méd 5.73%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 36.78 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 78% (107/140) · gap 28% · délai 0.3min · rebond 68% (71/107) (MFE +2.83%)
   - −1.0% : fill 30min 57% · séance 75% (102/140) · gap 22% · délai 0.4min · rebond 72% (71/102) (MFE +2.59%)
   - −1.5% : fill 30min 47% · séance 69% (92/140) · gap 13% · délai 1.9min · rebond 67% (59/92) (MFE +1.75%)
   - −2.0% : fill 30min 40% · séance 60% (79/140) · gap 9% · délai 3.8min · rebond 66% (52/79) (MFE +1.71%)
   - −3.0% : fill 30min 28% · séance 49% (63/140) · gap 6% · délai 10.5min · rebond 79% (51/63) (MFE +2.33%)
   - −4.0% : fill 30min 22% · séance 41% (53/140) · gap 6% · délai 15.0min · rebond 75% (41/53) (MFE +2.75%)
   - −5.0% : fill 30min 20% · séance 37% (46/140) · gap 5% · délai 18.8min · rebond 88% (43/46) (MFE +2.8%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.72% (p90 −5.72%) → stop au-delà de −3.26% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.92% (p90 −5.74%) → stop au-delà de −4.26% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.75% (p90 −5.86%) → stop au-delà de −3.99% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1340 jambes) : jambe baissière méd −1.24% (p90 −3.25%) · ~20.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 97% (45/49) · rebond 66% (30/45)
      · −2.0% : fill 84% (38/49) · rebond 52% (23/38)
      · −3.0% : fill 81% (34/49) · rebond 74% (27/34)
      · −4.0% : fill 67% (29/49) · rebond 68% (23/29)
      · −5.0% : fill 63% (27/49) · rebond 77% (24/27)
   - **flat** (30 séances) :
      · −1.0% : fill 81% (23/30) · rebond 79% (18/23)
      · −2.0% : fill 64% (17/30) · rebond 86% (13/17)
      · −3.0% : fill 42% (11/30) · rebond 92% (10/11)
      · −4.0% : fill 42% (11/30) · rebond 94% (10/11)
      · −5.0% : fill 34% (9/30) · rebond 100% (9/9)
   - **gap-up** (61 séances) :
      · −1.0% : fill 56% (34/61) · rebond 73% (23/34)
      · −2.0% : fill 40% (24/61) · rebond 69% (16/24)
      · −3.0% : fill 29% (18/61) · rebond 80% (14/18)
      · −4.0% : fill 22% (13/61) · rebond 70% (8/13)
      · −5.0% : fill 20% (10/61) · rebond 100% (10/10)
- **P(clôture VERTE) selon le drive 15min** (n=141) : 51% en base · 67% si les 15 1res min sont vertes (68 cas) · 37% si rouges (73 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=141) : COUDE à **31min** → P(séance verte=clôture>ouverture) 75% si début vert vs 27% si rouge (base 51% · écart 48 pts) ; prédictivité sature ensuite (plafond brut 241min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **75%** · continue >prix actuel 57% ; creux résiduel méd -2.06% (q20 -4.57%) → **SL/trailing à −4.57%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.64% / q75 +6.3% → **scale +3.64% / runner +6.3%**, sortie à la clôture
  - **si ROUGE au coude** (n=70) : edge inversé — récupère vert seulement **27%** (continue à baisser 58%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.52%** (au-delà de la MAE q10 -8.52%), cible rebond +2.37% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=141) : retour [-4.86% .. +9.45%] · haut q95 +9.95% · bas q05 -7.7%
   - 60min (n=141) : retour [-5.94% .. +10.89%] · haut q95 +11.06% · bas q05 -7.87%
   - 2h (n=141) : retour [-5.61% .. +10.56%] · haut q95 +12.27% · bas q05 -8.03%
   - 4h (n=141) : retour [-7.75% .. +13.35%] · haut q95 +14.1% · bas q05 -10.73%
   - 6h (n=141) : retour [-7.32% .. +15.34%] · haut q95 +21.01% · bas q05 -11.22%
   - session (n=141) : retour [-9.83% .. +21.2%] · haut q95 +23.75% · bas q05 -14.32%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.22%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 43.3  _(momentum baissier)_
- **ADX** : 23.7  _(pas de tendance nette)_
- **MACD** : hist 0.872  _(bullish_recent)_
- **BB** : %B 0.57 · largeur 109.9%
- **ATR** : 6.08 (97.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.0  _(neutre)_
- **Vol ratio** : 0.83  _(volume normal)_
- **Choppiness** : 39.2  _(transition)_
- **MA** : MA20 36.52 · MA50 40.86 · MA200 23.2  _(prix > MA20)_
- **Dist MA** : MA20 +7.4% · MA50 -4.0% · MA200 +69.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (94051 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
