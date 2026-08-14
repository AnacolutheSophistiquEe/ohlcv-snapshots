# 005930

**Generated** : 2026-08-14T00:13:34.287918+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 8.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩268000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩268000.00 (+0.7% vs entrée) · entrée ₩266185.67 · stop ₩259268.52 · T1 ₩277933.83 · R/R 1.7  
> ↳ P(T1 av. stop) 17 % _(réel 5 s)_ · EV/risk -0.353 _(réel 5 s)_ (GBM -0.12) · ¼-Kelly 0.007 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.6% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.180 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩264371.33–₩268000.00 (mid ₩266185.67)
- Spot actuel : ₩268000.00 (+0.7% au-dessus de la zone — repli à attendre)
- Stop : ₩259268.52 (stop swing_plan-based (-10.1%))
- Targets : T1 ₩277933.83 · R/R 1.7 | T2 ₩289682.00 · R/R 3.4 | T3 ₩301430.17 · R/R 5.1
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩259268.52


## Edge, scénarios & sizing

- EV/risk : -0.12 | EV/share : ₩-828.875 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 24 % | T2 20 % | T3 20 %
- Kelly (position) : f* 0.029 | ¼-Kelly 0.007 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 41.2 | bear 25.5 | side 33.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.679% → cible +4.414% / stop −2.599%, p_fill 92%, n_eff≈36.1) : P(cible|rempli) **17%** · **EV/risk -0.353** (×p_fill ; si rempli -1.00% du capital)
  - **swing** (entrée dip −1.496% → cible +9.869% / stop −8.734%, p_fill 90%, n_eff≈34.6) : P(cible|rempli) **20%** · **EV/risk -0.387** (×p_fill ; si rempli -3.76% du capital)
  - **deep** (entrée dip −2.185% → cible +13.957% / stop −13.193%, p_fill 84%, n_eff≈32.2) : P(cible|rempli) **15%** · **EV/risk -0.523** (×p_fill ; si rempli -8.26% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→69% · +2.0%→46% · +3.0%→35% · +5.0%→22% · +8.0%→5%
- Range intraday médian 6.16% (p90 9.84%) · excursion haute méd. +1.9% / basse méd. −3.12%
- Profil de vol intra : ouverture 3.101% vs midi 1.358% vs clôture 1.537% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (152 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 11% · trend ↑0%/↓1% ; spike-down 71% · recovery-V 19%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; mean-reverting — autocorr -0.101)_ ; drift intra méd. -1.43% ; recovery-V 16%
- **σ réalisé intraday** 4.582% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 36% / bas 77% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 241687.5 (VA 237562.5–242437.5 ; dernier close 240000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 31% · rebond 58% · **stop −6.75%** sous le fill (sous le bruit) · cible +1.3% · R/R 0.19 (high win-rate)
- Gaps overnight (n=151) : méd. 0.47% · baisse 44% (gap-down >1% 34% · >2% 24%)
- Excursion ouverture 5min (n=152) : bas méd −0.68% (p90 −1.67%) · haut méd +0.69% · range méd 1.64%
- Excursion ouverture 15min (n=152) : bas méd −1.01% (p90 −2.72%) · haut méd +1.07% · range méd 2.24%
- Excursion ouverture 30min (n=152) : bas méd −1.24% (p90 −3.38%) · haut méd +1.15% · range méd 2.9%
- Excursion ouverture 60min (n=152) : bas méd −1.74% (p90 −3.61%) · haut méd +1.3% · range méd 3.18%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 240000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 53% · séance 67% (95/151) · gap 36% · délai 0.0min · rebond 51% (51/95) (MFE +1.12%)
   - −1.0% : fill 30min 50% · séance 65% (89/151) · gap 34% · délai 0.0min · rebond 59% (51/89) (MFE +1.31%)
   - −1.5% : fill 30min 42% · séance 56% (77/151) · gap 26% · délai 0.3min · rebond 58% (46/77) (MFE +1.44%)
   - −2.0% : fill 30min 38% · séance 50% (68/151) · gap 24% · délai 0.2min · rebond 56% (39/68) (MFE +1.57%)
   - −3.0% : fill 30min 30% · séance 46% (59/151) · gap 19% · délai 1.7min · rebond 59% (38/59) (MFE +2.13%)
   - −4.0% : fill 30min 22% · séance 39% (47/151) · gap 14% · délai 26.2min · rebond 58% (31/47) (MFE +1.46%)
   - −5.0% : fill 30min 14% · séance 31% (36/151) · gap 10% · délai 50.8min · rebond 58% (23/36) (MFE +1.3%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.43% (p90 −2.26%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.45% (p90 −3.13%) → stop au-delà de −1.57% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −3.91%) → stop au-delà de −1.62% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=713 jambes) : jambe baissière méd −1.28% (p90 −3.12%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (63 séances) :
      · −1.0% : fill 98% (60/63) · rebond 44% (30/60)
      · −2.0% : fill 90% (52/63) · rebond 44% (26/52)
      · −3.0% : fill 88% (47/63) · rebond 52% (29/47)
      · −4.0% : fill 78% (39/63) · rebond 48% (24/39)
      · −5.0% : fill 68% (31/63) · rebond 51% (18/31)
   - **flat** (14 séances) :
      · −1.0% : fill 65% (8/14) · rebond 78% (5/8)
      · −2.0% : fill 33% (4/14) · rebond 85% (3/4)
      · −3.0% : fill 33% (4/14) · rebond 85% (3/4)
      · −4.0% : fill 15% (2/14) · rebond 100% (2/2)
      · −5.0% : fill 15% (2/14) · rebond 100% (2/2)
   - **gap-up** (74 séances) :
      · −1.0% : fill 40% (21/74) · rebond 83% (16/21)
      · −2.0% : fill 23% (12/74) · rebond 83% (10/12)
      · −3.0% : fill 16% (8/74) · rebond 76% (6/8)
      · −4.0% : fill 13% (6/74) · rebond 94% (5/6)
      · −5.0% : fill 5% (3/74) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=152) : 38% en base · 59% si les 15 1res min sont vertes (75 cas) · 17% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=152) : COUDE à **1:15** → P(séance verte=clôture>ouverture) 84% si début vert vs 5% si rouge (base 38% · écart 78 pts) ; prédictivité sature ensuite (plafond brut 75min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **84%** · continue >prix actuel 55% ; creux résiduel méd -1.37% (q20 -4.22%) → **SL/trailing à −4.22%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.84% / q75 +3.45% → **scale +1.84% / runner +3.45%**, sortie à la clôture
  - **si ROUGE au coude** (n=73) : edge inversé — récupère vert seulement **5%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.06%** (au-delà de la MAE q10 -7.06%), cible rebond +1.28% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=152) : retour [-2.82% .. +2.85%] · haut q95 +3.69% · bas q05 -3.83%
   - 60min (n=152) : retour [-3.18% .. +4.62%] · haut q95 +5.45% · bas q05 -5.22%
   - 2h (n=152) : retour [-4.73% .. +4.31%] · haut q95 +6.24% · bas q05 -6.43%
   - 4h (n=152) : retour [-6.44% .. +5.27%] · haut q95 +6.81% · bas q05 -7.89%
   - 6h (n=152) : retour [-7.21% .. +5.06%] · haut q95 +6.99% · bas q05 -8.26%
   - session (n=152) : retour [-7.46% .. +5.3%] · haut q95 +6.99% · bas q05 -9.15%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.9% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.95%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 54.8  _(neutre)_
- **ADX** : 23.5  _(pas de tendance nette)_
- **MACD** : hist 5003.827  _(pas de croisement recent)_
- **BB** : %B 0.84 · largeur 29.9%
- **ATR** : 23057.14 (82.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.183  _(distribution)_
- **Vol ratio** : 1.18  _(volume normal)_
- **Choppiness** : 52.0  _(transition)_
- **MA** : MA20 243500.0 · MA50 286985.14 · MA200 199344.07  _(prix > MA20)_
- **Dist MA** : MA20 +10.1% · MA50 -6.6% · MA200 +34.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (82981 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
