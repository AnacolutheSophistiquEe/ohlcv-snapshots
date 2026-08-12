# 005930

**Generated** : 2026-08-12T00:13:15.790882+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 8.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩239500.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot ₩239500.00 (+1.8% vs entrée) · entrée ₩235198.56 · stop ₩216382.68 · T1 ₩240000.00 · R/R 0.26  
> ↳ P(T1 av. stop) 36 % _(réel 5 s)_ · EV/risk -0.06 _(réel 5 s)_ (GBM -0.06) · ¼-Kelly 0.046 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.190 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩234238.27–₩236158.85 (mid ₩235198.56)
- Spot actuel : ₩239500.00 (+1.8% au-dessus de la zone — repli à attendre)
- Stop : ₩216382.68 (stop swing_plan-based (-13.55%))
- Targets : T1 ₩240000.00 · R/R 0.26 | T2 ₩262931.82 · R/R 1.47 | T3 ₩266114.47 · R/R 1.64
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩216382.68


## Edge, scénarios & sizing

- EV/risk : -0.06 | EV/share : ₩-1121.882 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 46 % | T2 21 % | T3 21 %
- Kelly (position) : f* 0.185 | ¼-Kelly 0.046 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.8 | bear 60.2 | side 33.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.793% → cible +2.041% / stop −8.0%, p_fill 83%, n_eff≈30.9) : P(cible|rempli) **36%** · **EV/risk -0.060** (×p_fill ; si rempli -0.58% du capital)
  - **swing** (entrée dip −3.953% → cible +14.3% / stop −9.992%, p_fill 72%, n_eff≈25.6) : P(cible|rempli) **10%** · **EV/risk -0.374** (×p_fill ; si rempli -5.19% du capital)
  - **deep** (entrée dip −6.103% → cible +27.708% / stop −15.332%, p_fill 66%, n_eff≈23.7) : P(cible|rempli) **3%** · **EV/risk -0.386** (×p_fill ; si rempli -8.94% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→68% · +2.0%→46% · +3.0%→34% · +5.0%→21% · +8.0%→5%
- Range intraday médian 6.09% (p90 9.84%) · excursion haute méd. +1.9% / basse méd. −3.08%
- Profil de vol intra : ouverture 3.066% vs midi 1.348% vs clôture 1.53% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (150 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑0%/↓1% ; spike-down 71% · recovery-V 20%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; mean-reverting — autocorr -0.097)_ ; drift intra méd. -1.677% ; recovery-V 17%
- **σ réalisé intraday** 4.643% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 35% / bas 80% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 231625.0 (VA 231125.0–233625.0 ; dernier close 231500.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 32% · rebond 58% · **stop −6.75%** sous le fill (sous le bruit) · cible +1.3% · R/R 0.19 (high win-rate)
- Gaps overnight (n=149) : méd. 0.48% · baisse 43% (gap-down >1% 35% · >2% 25%)
- Excursion ouverture 5min (n=150) : bas méd −0.68% (p90 −1.63%) · haut méd +0.69% · range méd 1.58%
- Excursion ouverture 15min (n=150) : bas méd −1.01% (p90 −2.75%) · haut méd +1.05% · range méd 2.24%
- Excursion ouverture 30min (n=150) : bas méd −1.24% (p90 −3.47%) · haut méd +1.15% · range méd 2.9%
- Excursion ouverture 60min (n=150) : bas méd −1.74% (p90 −3.62%) · haut méd +1.35% · range méd 3.19%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 231500.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 54% · séance 66% (93/149) · gap 38% · délai 0.0min · rebond 51% (50/93) (MFE +1.11%)
   - −1.0% : fill 30min 50% · séance 64% (87/149) · gap 35% · délai 0.0min · rebond 57% (49/87) (MFE +1.3%)
   - −1.5% : fill 30min 44% · séance 58% (77/149) · gap 27% · délai 0.3min · rebond 58% (46/77) (MFE +1.44%)
   - −2.0% : fill 30min 39% · séance 52% (68/149) · gap 25% · délai 0.2min · rebond 56% (39/68) (MFE +1.57%)
   - −3.0% : fill 30min 32% · séance 48% (59/149) · gap 20% · délai 1.7min · rebond 59% (38/59) (MFE +2.13%)
   - −4.0% : fill 30min 23% · séance 40% (47/149) · gap 15% · délai 26.2min · rebond 58% (31/47) (MFE +1.46%)
   - −5.0% : fill 30min 14% · séance 32% (36/149) · gap 10% · délai 50.8min · rebond 58% (23/36) (MFE +1.3%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.4% (p90 −2.21%) → stop au-delà de −1.13% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.43% (p90 −3.15%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.45% (p90 −4.24%) → stop au-delà de −1.81% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=699 jambes) : jambe baissière méd −1.29% (p90 −3.14%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (63 séances) :
      · −1.0% : fill 98% (60/63) · rebond 44% (30/60)
      · −2.0% : fill 90% (52/63) · rebond 44% (26/52)
      · −3.0% : fill 88% (47/63) · rebond 52% (29/47)
      · −4.0% : fill 78% (39/63) · rebond 48% (24/39)
      · −5.0% : fill 68% (31/63) · rebond 51% (18/31)
   - **flat** (13 séances) :
      · −1.0% : fill 58% (7/13) · rebond 70% (4/7)
      · −2.0% : fill 40% (4/13) · rebond 85% (3/4)
      · −3.0% : fill 40% (4/13) · rebond 85% (3/4)
      · −4.0% : fill 18% (2/13) · rebond 100% (2/2)
      · −5.0% : fill 18% (2/13) · rebond 100% (2/2)
   - **gap-up** (73 séances) :
      · −1.0% : fill 38% (20/73) · rebond 81% (15/20)
      · −2.0% : fill 23% (12/73) · rebond 83% (10/12)
      · −3.0% : fill 17% (8/73) · rebond 76% (6/8)
      · −4.0% : fill 13% (6/73) · rebond 94% (5/6)
      · −5.0% : fill 5% (3/73) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=150) : 37% en base · 60% si les 15 1res min sont vertes (73 cas) · 17% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=150) : COUDE à **1:15** → P(séance verte=clôture>ouverture) 83% si début vert vs 6% si rouge (base 37% · écart 77 pts) ; prédictivité sature ensuite (plafond brut 75min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **83%** · continue >prix actuel 53% ; creux résiduel méd -1.67% (q20 -4.25%) → **SL/trailing à −4.25%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.72% / q75 +3.48% → **scale +1.72% / runner +3.48%**, sortie à la clôture
  - **si ROUGE au coude** (n=72) : edge inversé — récupère vert seulement **6%** (continue à baisser 61%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.1%** (au-delà de la MAE q10 -7.1%), cible rebond +1.3% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=150) : retour [-2.82% .. +2.86%] · haut q95 +3.7% · bas q05 -3.86%
   - 60min (n=150) : retour [-3.2% .. +4.72%] · haut q95 +5.49% · bas q05 -5.27%
   - 2h (n=150) : retour [-4.84% .. +4.42%] · haut q95 +6.26% · bas q05 -6.5%
   - 4h (n=150) : retour [-6.5% .. +5.39%] · haut q95 +6.82% · bas q05 -7.92%
   - 6h (n=150) : retour [-7.21% .. +5.17%] · haut q95 +7.03% · bas q05 -8.27%
   - session (n=150) : retour [-7.48% .. +5.31%] · haut q95 +7.03% · bas q05 -9.16%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 4.0% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.95%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 44.6  _(momentum baissier)_
- **ADX** : 26.3  _(tendance etablie)_
- **MACD** : hist 1698.558  _(pas de croisement recent)_
- **BB** : %B 0.44 · largeur 31.8%
- **ATR** : 22985.71 (82.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.19  _(distribution)_
- **Vol ratio** : 0.77  _(volume normal)_
- **Choppiness** : 51.0  _(transition)_
- **MA** : MA20 244450.0 · MA50 290689.51 · MA200 197696.76  _(prix < MA20)_
- **Dist MA** : MA20 -2.0% · MA50 -17.6% · MA200 +21.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83941 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
