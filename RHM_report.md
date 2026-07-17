# RHM

**Generated** : 2026-07-17T21:35:57.006286+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €984.20  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €984.20 (+1.4% vs entrée) · entrée €970.35 · stop €950.94 · T1 €999.35 · R/R 1.49  
> ↳ P(T1 av. stop) 19 % _(réel 5 s)_ · EV/risk -0.152 _(réel 5 s)_ (GBM 0.015) · ¼-Kelly 0.005 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €964.55–€976.15 (mid €970.35)
- Spot actuel : €984.20 (+1.4% au-dessus de la zone — repli à attendre)
- Stop : €950.94 (stop swing_plan-based (-6.33%))
- Targets : T1 €999.35 · R/R 1.49 | T2 €1028.34 · R/R 2.99 | T3 €1057.34 · R/R 4.48
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €950.94


## Edge, scénarios & sizing

- EV/risk : 0.015 | EV/share : €0.289 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 30 % | T2 4 % | T3 4 %
- Kelly (position) : f* 0.021 | ¼-Kelly 0.005 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 19.3 | bear 5.0 | side 75.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.408% → cible +2.988% / stop −2.0%, p_fill 63%, n_eff≈24.8) : P(cible|rempli) **19%** · **EV/risk -0.152** (×p_fill ; si rempli -0.48% du capital)
  - **swing** (entrée dip −3.092% → cible +6.682% / stop −3.341%, p_fill 43%, n_eff≈14.7) : P(cible|rempli) **8%** · **EV/risk -0.321** (×p_fill ; si rempli -2.47% du capital)
  - **deep** (entrée dip −4.781% → cible +9.45% / stop −4.725%, p_fill 38%, n_eff≈16.0) : P(cible|rempli) **6%** · **EV/risk -0.255** (×p_fill ; si rempli -3.18% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→62% · +2.0%→48% · +3.0%→30% · +5.0%→4% · +8.0%→0%
- Range intraday médian 4.16% (p90 6.86%) · excursion haute méd. +1.85% / basse méd. −1.72%
- Profil de vol intra : ouverture 2.554% vs midi 0.874% vs clôture 1.09% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 56% · recovery-V 37%)_
- **Régime intraday** : **chop** _(efficiency 0.109 ; neutre — autocorr -0.002)_ ; drift intra méd. -0.539% ; recovery-V 39%
- **σ réalisé intraday** 2.884% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 74% / whipsaw 42%
- POC intraday (dernière séance, temps-au-prix) : 965.9738 (VA 961.9913–968.6288 ; dernier close 965.3)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 24% · rebond 61% · **stop −3.12%** sous le fill (sous le bruit) · cible +1.45% · R/R 0.46 (high win-rate)
- Gaps overnight (n=159) : méd. 0.03% · baisse 45% (gap-down >1% 14% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.82% (p90 −1.7%) · haut méd +0.5% · range méd 1.44%
- Excursion ouverture 15min (n=160) : bas méd −0.98% (p90 −2.03%) · haut méd +0.67% · range méd 1.97%
- Excursion ouverture 30min (n=160) : bas méd −1.06% (p90 −2.75%) · haut méd +0.88% · range méd 2.21%
- Excursion ouverture 60min (n=160) : bas méd −1.1% (p90 −3.22%) · haut méd +1.0% · range méd 2.37%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 965.3 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 79% (121/159) · gap 30% · délai 0.2min · rebond 55% (62/121) (MFE +1.19%)
   - −1.0% : fill 30min 51% · séance 74% (110/159) · gap 14% · délai 5.1min · rebond 60% (63/110) (MFE +1.39%)
   - −1.5% : fill 30min 32% · séance 58% (82/159) · gap 7% · délai 20.0min · rebond 49% (41/82) (MFE +1.0%)
   - −2.0% : fill 30min 22% · séance 48% (71/159) · gap 6% · délai 30.7min · rebond 59% (41/71) (MFE +1.27%)
   - −3.0% : fill 30min 11% · séance 33% (48/159) · gap 3% · délai 118.8min · rebond 60% (30/48) (MFE +1.31%)
   - −4.0% : fill 30min 5% · séance 24% (29/159) · gap 2% · délai 152.5min · rebond 61% (17/29) (MFE +1.45%)
   - −5.0% : fill 30min 2% · séance 12% (16/159) · gap 1% · délai 206.9min · rebond 48% (8/16) (MFE +0.74%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.62% (p90 −1.62%) → stop au-delà de −1.24% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.57% (p90 −1.65%) → stop au-delà de −1.35% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.3% (p90 −1.64%) → stop au-delà de −1.32% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=460 jambes) : jambe baissière méd −1.1% (p90 −2.65%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (52 séances) :
      · −1.0% : fill 94% (50/52) · rebond 60% (27/50)
      · −2.0% : fill 76% (39/52) · rebond 60% (24/39)
      · −3.0% : fill 52% (28/52) · rebond 59% (18/28)
      · −4.0% : fill 38% (16/52) · rebond 71% (11/16)
      · −5.0% : fill 18% (9/52) · rebond 77% (7/9)
   - **flat** (50 séances) :
      · −1.0% : fill 80% (37/50) · rebond 69% (24/37)
      · −2.0% : fill 34% (18/50) · rebond 71% (10/18)
      · −3.0% : fill 23% (11/50) · rebond 56% (6/11)
      · −4.0% : fill 21% (9/50) · rebond 38% (3/9)
      · −5.0% : fill 13% (6/50) · rebond 22% (1/6)
   - **gap-up** (57 séances) :
      · −1.0% : fill 48% (23/57) · rebond 49% (12/23)
      · −2.0% : fill 29% (14/57) · rebond 46% (7/14)
      · −3.0% : fill 22% (9/57) · rebond 66% (6/9)
      · −4.0% : fill 12% (4/57) · rebond 61% (3/4)
      · −5.0% : fill 5% (1/57) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 66% si les 15 1res min sont vertes (83 cas) · 31% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 74% si début vert vs 24% si rouge (base 48% · écart 50 pts) ; prédictivité sature ensuite (plafond brut 295min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **74%** · continue >prix actuel 47% ; creux résiduel méd -1.27% (q20 -2.51%) → **SL/trailing à −2.51%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.2% / q75 +1.88% → **scale +1.2% / runner +1.88%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **24%** (continue à baisser 55%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.98%** (au-delà de la MAE q10 -4.98%), cible rebond +1.15% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.66% .. +3.11%] · haut q95 +3.8% · bas q05 -3.24%
   - 60min (n=160) : retour [-3.53% .. +3.09%] · haut q95 +4.02% · bas q05 -4.1%
   - 2h (n=160) : retour [-3.64% .. +2.82%] · haut q95 +4.12% · bas q05 -4.84%
   - 4h (n=160) : retour [-3.91% .. +2.99%] · haut q95 +4.53% · bas q05 -5.11%
   - 6h (n=160) : retour [-4.74% .. +3.01%] · haut q95 +4.53% · bas q05 -5.76%
   - session (n=160) : retour [-6.26% .. +4.2%] · haut q95 +4.75% · bas q05 -6.79%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.28%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 51.7  _(neutre)_
- **ADX** : 27.7  _(tendance etablie)_
- **MACD** : hist -1.893  _(pas de croisement recent)_
- **BB** : %B 0.35 · largeur 30.1%
- **ATR** : 51.06 (21.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.056  _(distribution)_
- **Vol ratio** : 0.78  _(volume normal)_
- **Choppiness** : 46.5  _(transition)_
- **MA** : MA20 1030.5 · MA50 1130.67 · MA200 1500.39  _(prix < MA20)_
- **Dist MA** : MA20 -4.5% · MA50 -13.0% · MA200 -34.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90376 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
