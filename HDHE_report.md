# 267260

**Generated** : 2026-07-28T21:50:19.982633+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩705000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot ₩705000.00 (+3.1% vs entrée) · entrée ₩683840.13 · stop ₩629132.92 · T1 ₩740654.86 · R/R 1.04  
> ↳ P(T1 av. stop) 11 % _(réel 5 s)_ · EV/risk 0.035 _(réel 5 s)_ (GBM -0.168) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -1350 % hors [0,100] (R² max 0.94). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩679762.90–₩687917.36 (mid ₩683840.13)
- Spot actuel : ₩705000.00 (+3.1% au-dessus de la zone — repli à attendre)
- Stop : ₩629132.92 (stop swing_plan-based (-9.71%))
- Targets : T1 ₩740654.86 · R/R 1.04 | T2 ₩742734.03 · R/R 1.08 | T3 ₩744813.20 · R/R 1.11
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩629132.92


## Edge, scénarios & sizing

- EV/risk : -0.168 | EV/share : ₩-9163.458 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 11 % | T2 11 % | T3 11 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 16.9 | bear 20.5 | side 62.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.0% → cible +8.308% / stop −8.0%, p_fill 73%, n_eff≈30.0) : P(cible|rempli) **11%** · **EV/risk +0.035** (×p_fill ; si rempli +0.38% du capital)
  - **swing** (entrée dip −6.607% → cible +6.646% / stop −3.323%, p_fill 56%, n_eff≈22.8) : P(cible|rempli) **25%** · **EV/risk -0.145** (×p_fill ; si rempli -0.86% du capital)
  - **deep** (entrée dip −10.2% → cible +9.399% / stop −4.699%, p_fill 47%, n_eff≈18.3) : P(cible|rempli) **15%** · **EV/risk -0.293** (×p_fill ; si rempli -2.95% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→69% · +2.0%→46% · +3.0%→31% · +5.0%→11% · +8.0%→5%
- Range intraday médian 6.31% (p90 10.49%) · excursion haute méd. +1.84% / basse méd. −3.6%
- Profil de vol intra : ouverture 4.066% vs midi 1.087% vs clôture 1.157% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (141 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 77% · recovery-V 23%)_
- **Régime intraday** : **chop** _(efficiency 0.12 ; mean-reverting — autocorr -0.054)_ ; drift intra méd. -1.502% ; recovery-V 18%
- **σ réalisé intraday** 4.68% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 72% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 791550.0 (VA 784950.0–800350.0 ; dernier close 804000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 35% · rebond 85% · **stop −4.2%** sous le fill (sous le bruit) · cible +2.03% · R/R 0.48 (high win-rate)
- Gaps overnight (n=140) : méd. 1.12% · baisse 38% (gap-down >1% 22% · >2% 10%)
- Excursion ouverture 5min (n=141) : bas méd −1.61% (p90 −3.7%) · haut méd +0.95% · range méd 2.7%
- Excursion ouverture 15min (n=141) : bas méd −1.88% (p90 −4.63%) · haut méd +1.06% · range méd 3.39%
- Excursion ouverture 30min (n=141) : bas méd −2.21% (p90 −4.83%) · haut méd +1.08% · range méd 3.69%
- Excursion ouverture 60min (n=141) : bas méd −2.61% (p90 −5.5%) · haut méd +1.26% · range méd 4.13%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 804000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 71% (99/140) · gap 31% · délai 0.0min · rebond 53% (55/99) (MFE +1.2%)
   - −1.0% : fill 30min 56% · séance 69% (92/140) · gap 22% · délai 0.3min · rebond 55% (54/92) (MFE +1.16%)
   - −1.5% : fill 30min 48% · séance 62% (79/140) · gap 14% · délai 0.5min · rebond 65% (51/79) (MFE +1.28%)
   - −2.0% : fill 30min 43% · séance 59% (72/140) · gap 10% · délai 0.8min · rebond 69% (49/72) (MFE +1.7%)
   - −3.0% : fill 30min 32% · séance 50% (57/140) · gap 6% · délai 5.1min · rebond 79% (40/57) (MFE +1.92%)
   - −4.0% : fill 30min 23% · séance 42% (47/140) · gap 2% · délai 16.5min · rebond 76% (37/47) (MFE +2.29%)
   - −5.0% : fill 30min 14% · séance 35% (37/140) · gap 2% · délai 41.1min · rebond 85% (29/37) (MFE +2.03%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.72% (p90 −3.41%) → stop au-delà de −1.99% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.93% (p90 −3.31%) → stop au-delà de −1.97% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.04% (p90 −4.6%) → stop au-delà de −3.46% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=701 jambes) : jambe baissière méd −1.28% (p90 −3.57%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (48 séances) :
      · −1.0% : fill 98% (47/48) · rebond 49% (25/47)
      · −2.0% : fill 92% (40/48) · rebond 63% (24/40)
      · −3.0% : fill 82% (34/48) · rebond 78% (23/34)
      · −4.0% : fill 73% (30/48) · rebond 77% (24/30)
      · −5.0% : fill 62% (23/48) · rebond 86% (18/23)
   - **flat** (17 séances) :
      · −1.0% : fill 88% (14/17) · rebond 47% (7/14)
      · −2.0% : fill 79% (12/17) · rebond 78% (9/12)
      · −3.0% : fill 78% (11/17) · rebond 83% (8/11)
      · −4.0% : fill 57% (7/17) · rebond 68% (5/7)
      · −5.0% : fill 57% (7/17) · rebond 89% (6/7)
   - **gap-up** (75 séances) :
      · −1.0% : fill 48% (31/75) · rebond 66% (22/31)
      · −2.0% : fill 35% (20/75) · rebond 74% (16/20)
      · −3.0% : fill 26% (12/75) · rebond 77% (9/12)
      · −4.0% : fill 21% (10/75) · rebond 82% (8/10)
      · −5.0% : fill 14% (7/75) · rebond 78% (5/7)
- **P(clôture VERTE) selon le drive 15min** (n=141) : 34% en base · 50% si les 15 1res min sont vertes (66 cas) · 23% si rouges (75 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=141) : COUDE à **1:20** → P(séance verte=clôture>ouverture) 74% si début vert vs 10% si rouge (base 34% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=62) : tient le vert **74%** · continue >prix actuel 45% ; creux résiduel méd -1.47% (q20 -3.65%) → **SL/trailing à −3.65%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.23% / q75 +2.7% → **scale +1.23% / runner +2.7%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **10%** (continue à baisser 53%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.13%** (au-delà de la MAE q10 -5.13%), cible rebond +1.39% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=141) : retour [-5.07% .. +2.75%] · haut q95 +4.32% · bas q05 -5.59%
   - 60min (n=141) : retour [-5.55% .. +3.17%] · haut q95 +4.52% · bas q05 -6.01%
   - 2h (n=141) : retour [-6.79% .. +3.66%] · haut q95 +5.16% · bas q05 -7.36%
   - 4h (n=141) : retour [-6.94% .. +4.47%] · haut q95 +5.48% · bas q05 -8.25%
   - 6h (n=141) : retour [-6.9% .. +4.58%] · haut q95 +7.23% · bas q05 -8.79%
   - session (n=141) : retour [-6.94% .. +5.27%] · haut q95 +7.27% · bas q05 -9.0%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.43%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
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

- **RSI** : 33.0  _(momentum baissier)_
- **ADX** : 25.3  _(tendance etablie)_
- **MACD** : hist -291.245  _(pas de croisement recent)_
- **BB** : %B 0.07 · largeur 39.0%
- **ATR** : 66714.29 (76.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.085  _(distribution)_
- **Vol ratio** : 1.22  _(volume normal)_
- **Choppiness** : 61.8  _(marche en range (choppy))_
- **MA** : MA20 845850.0 · MA50 966700.0 · MA200 921490.81  _(prix < MA20)_
- **Dist MA** : MA20 -16.7% · MA50 -27.1% · MA200 -23.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83482 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
