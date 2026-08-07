# 326030

**Generated** : 2026-08-07T21:57:11.329000+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩85400.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩85400.00 (+1.1% vs entrée) · entrée ₩84458.33 · stop ₩83191.46 · T1 ₩85869.15 · R/R 1.11  
> ↳ P(T1 av. stop) 41 % _(réel 5 s)_ · EV/risk -0.112 _(réel 5 s)_ (GBM 0.002) · ¼-Kelly 0.009 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 122 % hors [0,100] (R² max 0.91). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 7/10 élevée alors que : %B 1.06 (collé à la bande haute) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩84176.17–₩84740.50 (mid ₩84458.33)
- Spot actuel : ₩85400.00 (+1.1% au-dessus de la zone — repli à attendre)
- Stop : ₩83191.46 (stop swing_plan-based (-7.29%))
- Targets : T1 ₩85869.15 · R/R 1.11 | T2 ₩87279.97 · R/R 2.23 | T3 ₩88690.78 · R/R 3.34
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩83191.46


## Edge, scénarios & sizing

- EV/risk : 0.002 | EV/share : ₩2.677 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 47 % | T2 23 % | T3 9 %
- Kelly (position) : f* 0.037 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 14.8 | bear 6.2 | side 79.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.107% → cible +1.67% / stop −1.5%, p_fill 67%, n_eff≈29.4) : P(cible|rempli) **41%** · **EV/risk -0.112** (×p_fill ; si rempli -0.25% du capital)
  - **swing** (entrée dip −2.431% → cible +3.735% / stop −4.98%, p_fill 57%, n_eff≈27.1) : P(cible|rempli) **40%** · **EV/risk -0.146** (×p_fill ; si rempli -1.27% du capital)
  - **deep** (entrée dip −3.751% → cible +5.282% / stop −7.573%, p_fill 60%, n_eff≈25.9) : P(cible|rempli) **51%** · **EV/risk +0.015** (×p_fill ; si rempli +0.19% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→66% · +2.0%→48% · +3.0%→32% · +5.0%→11% · +8.0%→5%
- Range intraday médian 4.39% (p90 7.69%) · excursion haute méd. +1.83% / basse méd. −2.34%
- Profil de vol intra : ouverture 2.909% vs midi 0.88% vs clôture 0.87% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (149 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 12% · trend ↑1%/↓1% ; spike-down 57% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.109 ; mean-reverting — autocorr -0.099)_ ; drift intra méd. 0.016% ; recovery-V 35%
- **σ réalisé intraday** 3.525% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 55% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 81785.0 (VA 81245.0–83135.0 ; dernier close 82900.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 48% · rebond 71% · **stop −3.83%** sous le fill (sous le bruit) · cible +1.6% · R/R 0.42 (high win-rate)
- Gaps overnight (n=148) : méd. 0.11% · baisse 41% (gap-down >1% 17% · >2% 7%)
- Excursion ouverture 5min (n=149) : bas méd −0.74% (p90 −2.26%) · haut méd +0.77% · range méd 2.05%
- Excursion ouverture 15min (n=149) : bas méd −0.91% (p90 −2.94%) · haut méd +0.88% · range méd 2.31%
- Excursion ouverture 30min (n=149) : bas méd −1.08% (p90 −2.96%) · haut méd +1.14% · range méd 2.73%
- Excursion ouverture 60min (n=149) : bas méd −1.16% (p90 −3.1%) · haut méd +1.5% · range méd 2.98%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 82900.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 78% (109/148) · gap 28% · délai 0.3min · rebond 56% (49/109) (MFE +1.34%)
   - −1.0% : fill 30min 54% · séance 68% (97/148) · gap 17% · délai 1.4min · rebond 58% (48/97) (MFE +1.25%)
   - −1.5% : fill 30min 40% · séance 54% (74/148) · gap 10% · délai 1.6min · rebond 65% (40/74) (MFE +1.52%)
   - −2.0% : fill 30min 29% · séance 48% (62/148) · gap 7% · délai 10.2min · rebond 71% (37/62) (MFE +1.6%)
   - −3.0% : fill 30min 12% · séance 33% (40/148) · gap 3% · délai 79.9min · rebond 58% (18/40) (MFE +1.39%)
   - −4.0% : fill 30min 6% · séance 21% (27/148) · gap 2% · délai 126.2min · rebond 62% (14/27) (MFE +1.35%)
   - −5.0% : fill 30min 5% · séance 14% (20/148) · gap 2% · délai 139.7min · rebond 83% (13/20) (MFE +1.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.4% (p90 −2.75%) → stop au-delà de −1.3% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.5% (p90 −1.42%) → stop au-delà de −1.23% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.46% (p90 −1.41%) → stop au-delà de −1.19% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=519 jambes) : jambe baissière méd −1.1% (p90 −2.45%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (45 séances) :
      · −1.0% : fill 95% (44/45) · rebond 66% (24/44)
      · −2.0% : fill 70% (31/45) · rebond 70% (17/31)
      · −3.0% : fill 46% (20/45) · rebond 61% (9/20)
      · −4.0% : fill 35% (16/45) · rebond 70% (9/16)
      · −5.0% : fill 23% (12/45) · rebond 85% (8/12)
   - **flat** (39 séances) :
      · −1.0% : fill 67% (27/39) · rebond 47% (11/27)
      · −2.0% : fill 51% (19/39) · rebond 77% (13/19)
      · −3.0% : fill 40% (12/39) · rebond 61% (6/12)
      · −4.0% : fill 31% (9/39) · rebond 50% (4/9)
      · −5.0% : fill 24% (7/39) · rebond 84% (5/7)
   - **gap-up** (64 séances) :
      · −1.0% : fill 47% (26/64) · rebond 58% (13/26)
      · −2.0% : fill 28% (12/64) · rebond 63% (7/12)
      · −3.0% : fill 18% (8/64) · rebond 47% (3/8)
      · −4.0% : fill 2% (2/64) · rebond 71% (1/2)
      · −5.0% : fill 1% (1/64) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=149) : 44% en base · 74% si les 15 1res min sont vertes (55 cas) · 22% si rouges (94 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=149) : COUDE à **13min** → P(séance verte=clôture>ouverture) 79% si début vert vs 16% si rouge (base 44% · écart 63 pts) ; prédictivité sature ensuite (plafond brut 201min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=56) : tient le vert **79%** · continue >prix actuel 64% ; creux résiduel méd -1.17% (q20 -2.83%) → **SL/trailing à −2.83%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.4% / q75 +3.04% → **scale +2.4% / runner +3.04%**, sortie à la clôture
  - **si ROUGE au coude** (n=93) : edge inversé — récupère vert seulement **16%** (continue à baisser 64%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.54%** (au-delà de la MAE q10 -4.54%), cible rebond +1.41% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=149) : retour [-2.7% .. +3.52%] · haut q95 +3.92% · bas q05 -3.72%
   - 60min (n=149) : retour [-3.27% .. +4.24%] · haut q95 +5.55% · bas q05 -4.06%
   - 2h (n=149) : retour [-3.28% .. +4.72%] · haut q95 +5.64% · bas q05 -4.37%
   - 4h (n=149) : retour [-4.35% .. +5.85%] · haut q95 +6.65% · bas q05 -5.91%
   - 6h (n=149) : retour [-4.88% .. +4.65%] · haut q95 +7.49% · bas q05 -6.24%
   - session (n=149) : retour [-4.94% .. +5.09%] · haut q95 +7.49% · bas q05 -6.46%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 326030 = **plat / peu volatil** (vol intra méd 2.43%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 67.9  _(momentum haussier)_
- **ADX** : 17.2  _(pas de tendance nette)_
- **MACD** : hist 1091.606  _(pas de croisement recent)_
- **BB** : %B 1.06 · largeur 13.5%
- **ATR** : 4150.0 (50.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.012  _(neutre)_
- **Vol ratio** : 1.08  _(volume normal)_
- **Choppiness** : 55.9  _(transition)_
- **MA** : MA20 79405.0 · MA50 84074.0 · MA200 105615.5  _(prix > MA20)_
- **Dist MA** : MA20 +7.5% · MA50 +1.6% · MA200 -19.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (84357 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
