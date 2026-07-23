# 326030

**Generated** : 2026-07-23T21:54:43.868571+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩79700.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)  
> ↳ spot ₩79700.00 (+1.8% vs entrée) · entrée ₩78275.00 · stop ₩77012.50 · T1 ₩80800.00 · R/R 2.0  
> ↳ P(T1 av. stop) 9 % _(réel 5 s)_ · EV/risk -0.271 _(réel 5 s)_ (GBM -0.115) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.61% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.160 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩77935.00–₩78615.00 (mid ₩78275.00)
- Spot actuel : ₩79700.00 (+1.8% au-dessus de la zone — repli à attendre)
- Stop : ₩77012.50 (stop swing_plan-based (-6.26%))
- Targets : T1 ₩80800.00 · R/R 2.0 | T2 ₩82079.77 · R/R 3.01 | T3 ₩83359.53 · R/R 4.03
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩77012.50


## Edge, scénarios & sizing

- EV/risk : -0.115 | EV/share : ₩-144.517 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 21 % | T2 7 % | T3 6 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 23.1 | bear 5.4 | side 71.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.786% → cible +3.226% / stop −1.613%, p_fill 58%, n_eff≈24.1) : P(cible|rempli) **9%** · **EV/risk -0.271** (×p_fill ; si rempli -0.76% du capital)
  - **swing** (entrée dip −3.934% → cible +4.842% / stop −2.421%, p_fill 48%, n_eff≈18.6) : P(cible|rempli) **41%** · **EV/risk +0.086** (×p_fill ; si rempli +0.43% du capital)
  - **deep** (entrée dip −6.074% → cible +6.847% / stop −3.424%, p_fill 51%, n_eff≈17.2) : P(cible|rempli) **36%** · **EV/risk +0.093** (×p_fill ; si rempli +0.62% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→71% · +1.0%→60% · +2.0%→42% · +3.0%→28% · +5.0%→9% · +8.0%→4%
- Range intraday médian 4.09% (p90 7.23%) · excursion haute méd. +1.55% / basse méd. −2.18%
- Profil de vol intra : ouverture 2.641% vs midi 0.769% vs clôture 0.793% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (138 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 15% · trend ↑1%/↓2% ; spike-down 60% · recovery-V 19%)_
- **Régime intraday** : **chop** _(efficiency 0.133 ; mean-reverting — autocorr -0.089)_ ; drift intra méd. -0.546% ; recovery-V 21%
- **σ réalisé intraday** 3.391% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 67% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 78887.5 (VA 78512.5–79187.5 ; dernier close 76600.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 16% · rebond 81% · **stop −2.91%** sous le fill (sous le bruit) · cible +1.92% · R/R 0.66 (high win-rate)
- Gaps overnight (n=137) : méd. 0.12% · baisse 42% (gap-down >1% 17% · >2% 7%)
- Excursion ouverture 5min (n=138) : bas méd −0.77% (p90 −2.28%) · haut méd +0.68% · range méd 1.99%
- Excursion ouverture 15min (n=138) : bas méd −0.88% (p90 −2.98%) · haut méd +0.74% · range méd 2.23%
- Excursion ouverture 30min (n=138) : bas méd −1.04% (p90 −3.06%) · haut méd +0.89% · range méd 2.56%
- Excursion ouverture 60min (n=138) : bas méd −1.22% (p90 −3.22%) · haut méd +1.22% · range méd 2.86%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 76600.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 80% (101/137) · gap 26% · délai 0.3min · rebond 50% (42/101) (MFE +0.94%)
   - −1.0% : fill 30min 56% · séance 71% (91/137) · gap 17% · délai 2.0min · rebond 54% (43/91) (MFE +1.01%)
   - −1.5% : fill 30min 42% · séance 56% (69/137) · gap 10% · délai 3.2min · rebond 58% (35/69) (MFE +1.22%)
   - −2.0% : fill 30min 28% · séance 48% (57/137) · gap 7% · délai 16.4min · rebond 64% (32/57) (MFE +1.43%)
   - −3.0% : fill 30min 11% · séance 35% (37/137) · gap 3% · délai 89.7min · rebond 56% (16/37) (MFE +1.32%)
   - −4.0% : fill 30min 7% · séance 21% (25/137) · gap 3% · délai 112.9min · rebond 54% (12/25) (MFE +1.03%)
   - −5.0% : fill 30min 6% · séance 16% (19/137) · gap 3% · délai 118.4min · rebond 81% (12/19) (MFE +1.92%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.36% (p90 −2.49%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.66% (p90 −1.84%) → stop au-delà de −1.37% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.64% (p90 −2.03%) → stop au-delà de −1.38% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=453 jambes) : jambe baissière méd −1.14% (p90 −2.43%) · ~9.0 jambes/séance
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
   - **gap-up** (61 séances) :
      · −1.0% : fill 49% (25/61) · rebond 53% (12/25)
      · −2.0% : fill 26% (11/61) · rebond 56% (6/11)
      · −3.0% : fill 20% (8/61) · rebond 47% (3/8)
      · −4.0% : fill 3% (2/61) · rebond 71% (1/2)
      · −5.0% : fill 1% (1/61) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=138) : 37% en base · 68% si les 15 1res min sont vertes (50 cas) · 15% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=138) : COUDE à **1:38** → P(séance verte=clôture>ouverture) 74% si début vert vs 6% si rouge (base 37% · écart 67 pts) ; prédictivité sature ensuite (plafond brut 192min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=56) : tient le vert **74%** · continue >prix actuel 43% ; creux résiduel méd -1.44% (q20 -2.35%) → **SL/trailing à −2.35%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.28% / q75 +1.93% → **scale +1.28% / runner +1.93%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **6%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.0%** (au-delà de la MAE q10 -4.0%), cible rebond +0.75% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=138) : retour [-2.78% .. +2.47%] · haut q95 +3.63% · bas q05 -4.03%
   - 60min (n=138) : retour [-3.8% .. +2.55%] · haut q95 +4.05% · bas q05 -4.46%
   - 2h (n=138) : retour [-3.48% .. +3.79%] · haut q95 +4.5% · bas q05 -4.63%
   - 4h (n=138) : retour [-4.13% .. +4.99%] · haut q95 +6.23% · bas q05 -5.76%
   - 6h (n=138) : retour [-4.59% .. +4.21%] · haut q95 +6.96% · bas q05 -5.97%
   - session (n=138) : retour [-4.69% .. +4.4%] · haut q95 +6.96% · bas q05 -5.97%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 326030 = **plat / peu volatil** (vol intra méd 2.31%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 38.5  _(momentum baissier)_
- **ADX** : 17.5  _(pas de tendance nette)_
- **MACD** : hist -60.137  _(pas de croisement recent)_
- **BB** : %B 0.36 · largeur 21.9%
- **ATR** : 4042.86 (44.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.158  _(distribution)_
- **Vol ratio** : 0.76  _(volume normal)_
- **Choppiness** : 52.9  _(transition)_
- **MA** : MA20 82235.0 · MA50 87690.0 · MA200 106866.5  _(prix < MA20)_
- **Dist MA** : MA20 -3.1% · MA50 -9.1% · MA200 -25.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (84598 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
