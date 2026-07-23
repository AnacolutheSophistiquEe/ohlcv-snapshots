# 326030

**Generated** : 2026-07-23T00:18:48.073368+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩76800.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)  
> ↳ spot ₩76800.00 (+0.9% vs entrée) · entrée ₩76100.00 · stop ₩73750.00 · T1 ₩80800.00 · R/R 2.0  
> ↳ P(T1 av. stop) 6 % _(réel 5 s)_ · EV/risk -0.164 _(réel 5 s)_ (GBM -0.175) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.09% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩75761.41–₩76438.59 (mid ₩76100.00)
- Spot actuel : ₩76800.00 (+0.9% au-dessus de la zone — repli à attendre)
- Stop : ₩73750.00 (stop swing_plan-based (-4.44%))
- Targets : T1 ₩80800.00 · R/R 2.0 | T2 ₩80981.76 · R/R 2.08 | T3 ₩81163.51 · R/R 2.15
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩73750.00


## Edge, scénarios & sizing

- EV/risk : -0.175 | EV/share : ₩-411.228 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 8 % | T2 8 % | T3 8 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 17.1 | bear 17.0 | side 65.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.91% → cible +6.176% / stop −3.088%, p_fill 78%, n_eff≈31.8) : P(cible|rempli) **6%** · **EV/risk -0.164** (×p_fill ; si rempli -0.65% du capital)
  - **swing** (entrée dip −2.01% → cible +4.959% / stop −2.48%, p_fill 79%, n_eff≈30.8) : P(cible|rempli) **19%** · **EV/risk -0.334** (×p_fill ; si rempli -1.05% du capital)
  - **deep** (entrée dip −3.102% → cible +7.014% / stop −3.507%, p_fill 76%, n_eff≈27.9) : P(cible|rempli) **23%** · **EV/risk -0.241** (×p_fill ; si rempli -1.11% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→71% · +1.0%→60% · +2.0%→44% · +3.0%→28% · +5.0%→9% · +8.0%→4%
- Range intraday médian 4.08% (p90 7.23%) · excursion haute méd. +1.55% / basse méd. −2.12%
- Profil de vol intra : ouverture 2.628% vs midi 0.767% vs clôture 0.777% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (137 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 15% · trend ↑1%/↓2% ; spike-down 59% · recovery-V 20%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; mean-reverting — autocorr -0.074)_ ; drift intra méd. -0.452% ; recovery-V 22%
- **σ réalisé intraday** 3.388% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 65% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 77687.5 (VA 77622.5–78272.5 ; dernier close 77700.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 16% · rebond 81% · **stop −2.91%** sous le fill (sous le bruit) · cible +1.92% · R/R 0.66 (high win-rate)
- Gaps overnight (n=136) : méd. 0.1% · baisse 43% (gap-down >1% 17% · >2% 7%)
- Excursion ouverture 5min (n=137) : bas méd −0.77% (p90 −2.29%) · haut méd +0.66% · range méd 1.93%
- Excursion ouverture 15min (n=137) : bas méd −0.91% (p90 −2.98%) · haut méd +0.72% · range méd 2.28%
- Excursion ouverture 30min (n=137) : bas méd −1.08% (p90 −3.08%) · haut méd +0.88% · range méd 2.58%
- Excursion ouverture 60min (n=137) : bas méd −1.24% (p90 −3.22%) · haut méd +1.17% · range méd 2.94%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 77700.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 80% (100/136) · gap 26% · délai 0.2min · rebond 51% (42/100) (MFE +1.18%)
   - −1.0% : fill 30min 57% · séance 70% (90/136) · gap 17% · délai 1.8min · rebond 55% (43/90) (MFE +1.05%)
   - −1.5% : fill 30min 42% · séance 57% (69/136) · gap 10% · délai 3.2min · rebond 58% (35/69) (MFE +1.22%)
   - −2.0% : fill 30min 28% · séance 49% (57/136) · gap 7% · délai 16.4min · rebond 64% (32/57) (MFE +1.43%)
   - −3.0% : fill 30min 11% · séance 35% (37/136) · gap 3% · délai 89.7min · rebond 56% (16/37) (MFE +1.32%)
   - −4.0% : fill 30min 8% · séance 22% (25/136) · gap 3% · délai 112.9min · rebond 54% (12/25) (MFE +1.03%)
   - −5.0% : fill 30min 6% · séance 16% (19/136) · gap 3% · délai 118.4min · rebond 81% (12/19) (MFE +1.92%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.39% (p90 −2.62%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.66% (p90 −1.84%) → stop au-delà de −1.37% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.64% (p90 −2.03%) → stop au-delà de −1.38% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=446 jambes) : jambe baissière méd −1.15% (p90 −2.48%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (41 séances) :
      · −1.0% : fill 100% (41/41) · rebond 66% (22/41)
      · −2.0% : fill 68% (28/41) · rebond 61% (14/28)
      · −3.0% : fill 45% (18/41) · rebond 49% (7/18)
      · −4.0% : fill 37% (15/41) · rebond 65% (8/15)
      · −5.0% : fill 29% (12/41) · rebond 85% (8/12)
   - **flat** (35 séances) :
      · −1.0% : fill 72% (25/35) · rebond 37% (9/25)
      · −2.0% : fill 58% (18/35) · rebond 74% (12/18)
      · −3.0% : fill 45% (11/35) · rebond 71% (6/11)
      · −4.0% : fill 33% (8/35) · rebond 39% (3/8)
      · −5.0% : fill 23% (6/35) · rebond 79% (4/6)
   - **gap-up** (60 séances) :
      · −1.0% : fill 46% (24/60) · rebond 58% (12/24)
      · −2.0% : fill 28% (11/60) · rebond 56% (6/11)
      · −3.0% : fill 21% (8/60) · rebond 47% (3/8)
      · −4.0% : fill 3% (2/60) · rebond 71% (1/2)
      · −5.0% : fill 1% (1/60) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=137) : 38% en base · 71% si les 15 1res min sont vertes (49 cas) · 15% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=137) : COUDE à **1:38** → P(séance verte=clôture>ouverture) 77% si début vert vs 6% si rouge (base 38% · écart 70 pts) ; prédictivité sature ensuite (plafond brut 195min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=55) : tient le vert **77%** · continue >prix actuel 45% ; creux résiduel méd -1.42% (q20 -2.18%) → **SL/trailing à −2.18%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.35% / q75 +1.94% → **scale +1.35% / runner +1.94%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **6%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.0%** (au-delà de la MAE q10 -4.0%), cible rebond +0.75% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=137) : retour [-2.78% .. +2.47%] · haut q95 +3.64% · bas q05 -4.04%
   - 60min (n=137) : retour [-3.81% .. +2.55%] · haut q95 +4.12% · bas q05 -4.49%
   - 2h (n=137) : retour [-3.48% .. +3.84%] · haut q95 +4.51% · bas q05 -4.66%
   - 4h (n=137) : retour [-4.22% .. +5.09%] · haut q95 +6.25% · bas q05 -5.78%
   - 6h (n=137) : retour [-4.62% .. +4.23%] · haut q95 +7.0% · bas q05 -5.98%
   - session (n=137) : retour [-4.72% .. +4.51%] · haut q95 +7.0% · bas q05 -5.98%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 326030 = **plat / peu volatil** (vol intra méd 2.31%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 31.9  _(momentum baissier)_
- **ADX** : 17.0  _(pas de tendance nette)_
- **MACD** : hist -324.914  _(pas de croisement recent)_
- **BB** : %B 0.18 · largeur 22.1%
- **ATR** : 4214.29 (51.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.129  _(distribution)_
- **Vol ratio** : 0.75  _(volume normal)_
- **Choppiness** : 51.4  _(transition)_
- **MA** : MA20 82580.0 · MA50 88068.0 · MA200 107019.5  _(prix < MA20)_
- **Dist MA** : MA20 -7.0% · MA50 -12.8% · MA200 -28.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83310 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
