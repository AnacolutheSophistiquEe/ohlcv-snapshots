# SAF

**Generated** : 2026-08-05T00:06:55.069981+00:00  
**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €355.40  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-5 sess · macro taux)  
> ↳ spot €355.40 (+0.8% vs entrée) · entrée €352.75 · stop €343.12 · T1 €361.27 · R/R 0.88  
> ↳ P(T1 av. stop) 51 % _(réel 5 s)_ · EV/risk -0.049 _(réel 5 s)_ (GBM 0.011) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 211 % hors [0,100] (R² max 0.75). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : RSI 72.1 > 70 (surachat) ; %B 1.06 (collé à la bande haute) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €351.04–€354.45 (mid €352.75)
- Spot actuel : €355.40 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : €343.12 (stop swing_plan-based (-3.46%))
- Targets : T1 €361.27 · R/R 0.88 | T2 €369.80 · R/R 1.77 | T3 €378.33 · R/R 2.66
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €343.12


## Edge, scénarios & sizing

- EV/risk : 0.011 | EV/share : €0.110 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 46 % | T2 23 % | T3 14 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 38.2 | side 56.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 355.0 (= 1 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.337% → cible +1.081% / stop −2.0%, p_fill 80%, n_eff≈33.0) : P(cible|rempli) **36%** · **EV/risk -0.081** (×p_fill ; si rempli -0.20% du capital)
  - **swing** (entrée dip −0.751% → cible +2.417% / stop −2.73%, p_fill 77%, n_eff≈29.4) : P(cible|rempli) **51%** · **EV/risk -0.049** (×p_fill ; si rempli -0.17% du capital)
  - **deep** (entrée dip −1.156% → cible +3.418% / stop −4.111%, p_fill 74%, n_eff≈26.5) : P(cible|rempli) **62%** · **EV/risk +0.114** (×p_fill ; si rempli +0.64% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→72% · +1.0%→55% · +2.0%→34% · +3.0%→14% · +5.0%→2% · +8.0%→1%
- Range intraday médian 2.72% (p90 4.55%) · excursion haute méd. +1.2% / basse méd. −0.98%
- Profil de vol intra : ouverture 1.679% vs midi 0.631% vs clôture 0.742% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 40% · recovery-V 20%)_
- **Régime intraday** : **chop** _(efficiency 0.097 ; mean-reverting — autocorr -0.058)_ ; drift intra méd. 0.128% ; recovery-V 23%
- **σ réalisé intraday** 1.981% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 73% / bas 47% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 351.4187 (VA 350.9438–352.6062 ; dernier close 350.7)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 17% · rebond 54% · **stop −1.63%** sous le fill (sous le bruit) · cible +1.2% · R/R 0.74 (high win-rate)
- Gaps overnight (n=159) : méd. 0.08% · baisse 48% (gap-down >1% 9% · >2% 1%)
- Excursion ouverture 5min (n=160) : bas méd −0.48% (p90 −1.7%) · haut méd +0.18% · range méd 0.94%
- Excursion ouverture 15min (n=160) : bas méd −0.62% (p90 −1.92%) · haut méd +0.32% · range méd 1.22%
- Excursion ouverture 30min (n=160) : bas méd −0.62% (p90 −1.92%) · haut méd +0.53% · range méd 1.45%
- Excursion ouverture 60min (n=160) : bas méd −0.71% (p90 −1.95%) · haut méd +0.59% · range méd 1.62%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 350.7 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 69% (113/159) · gap 22% · délai 0.2min · rebond 42% (44/113) (MFE +0.84%)
   - −1.0% : fill 30min 43% · séance 53% (83/159) · gap 9% · délai 0.4min · rebond 43% (31/83) (MFE +0.67%)
   - −1.5% : fill 30min 29% · séance 44% (70/159) · gap 3% · délai 7.5min · rebond 45% (26/70) (MFE +0.91%)
   - −2.0% : fill 30min 13% · séance 34% (52/159) · gap 1% · délai 52.5min · rebond 52% (24/52) (MFE +1.14%)
   - −3.0% : fill 30min 3% · séance 17% (29/159) · gap 1% · délai 87.1min · rebond 54% (17/29) (MFE +1.2%)
   - −4.0% : fill 30min 2% · séance 7% (13/159) · gap 0% · délai 126.9min · rebond 62% (7/13) (MFE +1.25%)
   - −5.0% : fill 30min 0% · séance 1% (3/159) · gap 0% · délai 360.2min · rebond 31% (1/3) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.24% (p90 −0.91%) → stop au-delà de −0.74% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −0.78%) → stop au-delà de −0.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=210 jambes) : jambe baissière méd −1.04% (p90 −2.45%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 82% (44/55) · rebond 37% (16/44)
      · −2.0% : fill 63% (32/55) · rebond 48% (15/32)
      · −3.0% : fill 30% (17/55) · rebond 50% (9/17)
      · −4.0% : fill 16% (9/55) · rebond 69% (5/9)
      · −5.0% : fill 2% (2/55) · rebond 0% (0/2)
   - **flat** (44 séances) :
      · −1.0% : fill 45% (19/44) · rebond 56% (10/19)
      · −2.0% : fill 21% (9/44) · rebond 75% (5/9)
      · −3.0% : fill 11% (5/44) · rebond 85% (4/5)
      · −4.0% : fill 1% (1/44) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/44) · rebond 0% (0/0)
   - **gap-up** (60 séances) :
      · −1.0% : fill 32% (20/60) · rebond 42% (5/20)
      · −2.0% : fill 17% (11/60) · rebond 43% (4/11)
      · −3.0% : fill 10% (7/60) · rebond 36% (4/7)
      · −4.0% : fill 5% (3/60) · rebond 30% (1/3)
      · −5.0% : fill 1% (1/60) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 70% si les 15 1res min sont vertes (71 cas) · 33% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **44min** → P(séance verte=clôture>ouverture) 78% si début vert vs 26% si rouge (base 51% · écart 53 pts) ; prédictivité sature ensuite (plafond brut 298min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **78%** · continue >prix actuel 57% ; creux résiduel méd -0.62% (q20 -1.56%) → **SL/trailing à −1.56%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.21% / q75 +1.73% → **scale +1.21% / runner +1.73%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **26%** (continue à baisser 47%) → **RÉDUIRE ~74%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.43%** (au-delà de la MAE q10 -2.43%), cible rebond +1.06% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.62% .. +1.8%] · haut q95 +2.02% · bas q05 -2.28%
   - 60min (n=160) : retour [-1.8% .. +2.18%] · haut q95 +2.53% · bas q05 -2.57%
   - 2h (n=160) : retour [-2.43% .. +2.36%] · haut q95 +2.65% · bas q05 -3.05%
   - 4h (n=160) : retour [-2.12% .. +2.24%] · haut q95 +2.98% · bas q05 -3.37%
   - 6h (n=160) : retour [-2.22% .. +2.78%] · haut q95 +3.2% · bas q05 -3.93%
   - session (n=160) : retour [-3.26% .. +2.7%] · haut q95 +3.64% · bas q05 -4.04%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.69%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 72.1  _(surachat)_
- **ADX** : 15.3  _(pas de tendance nette)_
- **MACD** : hist 1.737  _(bullish_recent)_
- **BB** : %B 1.06 · largeur 11.2%
- **ATR** : 9.63 (75.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.092  _(accumulation)_
- **Vol ratio** : 0.36  _(volume atone)_
- **Choppiness** : 44.5  _(transition)_
- **MA** : MA20 334.61 · MA50 325.37 · MA200 305.66  _(prix > MA20)_
- **Dist MA** : MA20 +6.2% · MA50 +9.2% · MA200 +16.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (94168 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
