# 326030

**Generated** : 2026-08-11T21:56:49.052832+00:00  
**Santé technique** : 8/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩90900.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot ₩90900.00 (+2.6% vs entrée) · entrée ₩88583.33 · stop ₩87254.58 · T1 ₩90024.81 · R/R 1.08  
> ↳ P(T1 av. stop) 53 % _(réel 5 s)_ · EV/risk 0.103 _(réel 5 s)_ (GBM 0.036) · ¼-Kelly 0.013 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 216 % hors [0,100] (R² max 0.96). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : RSI 75.3 > 70 (surachat) ; %B 1.14 (collé à la bande haute) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩88295.04–₩88871.63 (mid ₩88583.33)
- Spot actuel : ₩90900.00 (+2.6% au-dessus de la zone — repli à attendre)
- Stop : ₩87254.58 (stop swing_plan-based (-10.44%))
- Targets : T1 ₩90024.81 · R/R 1.08 | T2 ₩91466.28 · R/R 2.17 | T3 ₩92907.76 · R/R 3.25
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩87254.58


## Edge, scénarios & sizing

- EV/risk : 0.036 | EV/share : ₩48.268 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 49 % | T2 26 % | T3 10 %
- Kelly (position) : f* 0.052 | ¼-Kelly 0.013 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 78.3 | bear 6.4 | side 15.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.548% → cible +1.627% / stop −1.5%, p_fill 42%, n_eff≈19.5) : P(cible|rempli) **53%** · **EV/risk +0.103** (×p_fill ; si rempli +0.37% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=13, n_eff=9))
  - **deep** : indisponible (échantillon insuffisant (n=7, n_eff=4))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→68% · +2.0%→49% · +3.0%→34% · +5.0%→11% · +8.0%→5%
- Range intraday médian 4.39% (p90 7.69%) · excursion haute méd. +1.9% / basse méd. −2.27%
- Profil de vol intra : ouverture 2.916% vs midi 0.888% vs clôture 0.873% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (150 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 12% · trend ↑1%/↓1% ; spike-down 56% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.108 ; mean-reverting — autocorr -0.101)_ ; drift intra méd. 0.157% ; recovery-V 36%
- **σ réalisé intraday** 3.534% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 57% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 83880.0 (VA 82840.0–84440.0 ; dernier close 85200.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 47% · rebond 71% · **stop −3.83%** sous le fill (sous le bruit) · cible +1.6% · R/R 0.42 (high win-rate)
- Gaps overnight (n=149) : méd. 0.1% · baisse 42% (gap-down >1% 17% · >2% 7%)
- Excursion ouverture 5min (n=150) : bas méd −0.73% (p90 −2.25%) · haut méd +0.81% · range méd 2.05%
- Excursion ouverture 15min (n=150) : bas méd −0.87% (p90 −2.93%) · haut méd +0.89% · range méd 2.31%
- Excursion ouverture 30min (n=150) : bas méd −1.04% (p90 −2.95%) · haut méd +1.26% · range méd 2.68%
- Excursion ouverture 60min (n=150) : bas méd −1.16% (p90 −3.08%) · haut méd +1.58% · range méd 2.97%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 85200.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 79% (110/149) · gap 27% · délai 0.3min · rebond 57% (50/110) (MFE +1.42%)
   - −1.0% : fill 30min 52% · séance 68% (98/149) · gap 17% · délai 1.6min · rebond 60% (49/98) (MFE +1.26%)
   - −1.5% : fill 30min 40% · séance 53% (74/149) · gap 9% · délai 1.6min · rebond 65% (40/74) (MFE +1.52%)
   - −2.0% : fill 30min 29% · séance 47% (62/149) · gap 7% · délai 10.2min · rebond 71% (37/62) (MFE +1.6%)
   - −3.0% : fill 30min 12% · séance 33% (40/149) · gap 3% · délai 79.9min · rebond 58% (18/40) (MFE +1.39%)
   - −4.0% : fill 30min 6% · séance 20% (27/149) · gap 2% · délai 126.2min · rebond 62% (14/27) (MFE +1.35%)
   - −5.0% : fill 30min 5% · séance 14% (20/149) · gap 2% · délai 139.7min · rebond 83% (13/20) (MFE +1.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.36% (p90 −2.72%) → stop au-delà de −1.28% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.48% (p90 −1.41%) → stop au-delà de −1.2% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.55% (p90 −1.41%) → stop au-delà de −1.16% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=524 jambes) : jambe baissière méd −1.11% (p90 −2.43%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (45 séances) :
      · −1.0% : fill 95% (44/45) · rebond 66% (24/44)
      · −2.0% : fill 70% (31/45) · rebond 70% (17/31)
      · −3.0% : fill 46% (20/45) · rebond 61% (9/20)
      · −4.0% : fill 35% (16/45) · rebond 70% (9/16)
      · −5.0% : fill 23% (12/45) · rebond 85% (8/12)
   - **flat** (40 séances) :
      · −1.0% : fill 69% (28/40) · rebond 52% (12/28)
      · −2.0% : fill 48% (19/40) · rebond 77% (13/19)
      · −3.0% : fill 38% (12/40) · rebond 61% (6/12)
      · −4.0% : fill 29% (9/40) · rebond 50% (4/9)
      · −5.0% : fill 22% (7/40) · rebond 84% (5/7)
   - **gap-up** (64 séances) :
      · −1.0% : fill 47% (26/64) · rebond 58% (13/26)
      · −2.0% : fill 28% (12/64) · rebond 63% (7/12)
      · −3.0% : fill 18% (8/64) · rebond 47% (3/8)
      · −4.0% : fill 2% (2/64) · rebond 71% (1/2)
      · −5.0% : fill 1% (1/64) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=150) : 45% en base · 75% si les 15 1res min sont vertes (56 cas) · 22% si rouges (94 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=150) : COUDE à **13min** → P(séance verte=clôture>ouverture) 80% si début vert vs 16% si rouge (base 45% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 201min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=57) : tient le vert **80%** · continue >prix actuel 66% ; creux résiduel méd -1.37% (q20 -2.79%) → **SL/trailing à −2.79%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.39% / q75 +2.91% → **scale +2.39% / runner +2.91%**, sortie à la clôture
  - **si ROUGE au coude** (n=93) : edge inversé — récupère vert seulement **16%** (continue à baisser 64%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.54%** (au-delà de la MAE q10 -4.54%), cible rebond +1.41% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=150) : retour [-2.69% .. +3.43%] · haut q95 +3.87% · bas q05 -3.68%
   - 60min (n=150) : retour [-3.21% .. +4.23%] · haut q95 +5.49% · bas q05 -4.05%
   - 2h (n=150) : retour [-3.26% .. +4.66%] · haut q95 +5.61% · bas q05 -4.32%
   - 4h (n=150) : retour [-4.33% .. +5.76%] · haut q95 +6.57% · bas q05 -5.89%
   - 6h (n=150) : retour [-4.85% .. +4.56%] · haut q95 +7.41% · bas q05 -6.2%
   - session (n=150) : retour [-4.92% .. +5.08%] · haut q95 +7.41% · bas q05 -6.46%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 326030 = **plat / peu volatil** (vol intra méd 2.43%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : stretched_up
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

- **RSI** : 75.3  _(surachat)_
- **ADX** : 18.8  _(pas de tendance nette)_
- **MACD** : hist 1675.724  _(pas de croisement recent)_
- **BB** : %B 1.14 · largeur 20.8%
- **ATR** : 4392.86 (58.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.097  _(accumulation)_
- **Vol ratio** : 1.24  _(volume normal)_
- **Choppiness** : 43.1  _(transition)_
- **MA** : MA20 80300.0 · MA50 84002.0 · MA200 105494.5  _(prix > MA20)_
- **Dist MA** : MA20 +13.2% · MA50 +8.2% · MA200 -13.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83843 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
