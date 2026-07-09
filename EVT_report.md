# EVT

**Generated** : 2026-07-09T21:39:20.631222+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €4.99  

> 🟡 **WAIT-FOR-DIP** — spot +2.7 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €4.99 (+2.7% vs entrée) · entrée €4.86 · stop €4.69 · T1 €4.92 · R/R 0.35  
> ↳ P(T1 av. stop) 78 % _(réel 5 s)_ · EV/risk 0.043 _(réel 5 s)_ (GBM 0.018) · ¼-Kelly 0.033 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.5% cohérent avec le bruit 5 s (EV-optimal ≈ −3.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 7/10 élevée alors que : RSI 70.3 > 70 (surachat) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €4.85–€4.87 (mid €4.86)
- Spot actuel : €4.99 (+2.7% au-dessus de la zone — repli à attendre)
- Stop : €4.69 (stop swing_plan-based (-6.86%))
- Targets : T1 €4.92 · R/R 0.35 | T2 €4.97 · R/R 0.65 | T3 €5.02 · R/R 0.94
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €4.69


## Edge, scénarios & sizing

- EV/risk : 0.018 | EV/share : €0.003 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 68 % | T2 40 % | T3 27 %
- Kelly (position) : f* 0.132 | ¼-Kelly 0.033 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.1 | bear 6.2 | side 80.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 399.0 (= 80 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.581% → cible +1.113% / stop −3.499%, p_fill 29%, n_eff≈14.0) : P(cible|rempli) **78%** · **EV/risk +0.043** (×p_fill ; si rempli +0.52% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=13, n_eff=8))
  - **deep** : indisponible (échantillon insuffisant (n=9, n_eff=7))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→72% · +2.0%→45% · +3.0%→29% · +5.0%→9% · +8.0%→2%
- Range intraday médian 4.43% (p90 6.71%) · excursion haute méd. +1.87% / basse méd. −1.94%
- Profil de vol intra : ouverture 2.672% vs midi 1.217% vs clôture 1.241% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 95% · range 5% · trend ↑0%/↓0% ; spike-down 54% · recovery-V 41%)_
- **Régime intraday** : **chop** _(efficiency 0.087 ; mean-reverting — autocorr -0.12)_ ; drift intra méd. 0.128% ; recovery-V 45%
- **σ réalisé intraday** 2.943% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 65% / bas 67% / whipsaw 33%
- POC intraday (dernière séance, temps-au-prix) : 4.952 (VA 4.9149–4.9679 ; dernier close 4.854)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 31% · rebond 70% · **stop −2.37%** sous le fill (sous le bruit) · cible +1.87% · R/R 0.79 (high win-rate)
- Gaps overnight (n=159) : méd. -0.04% · baisse 51% (gap-down >1% 20% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.58% (p90 −2.08%) · haut méd +0.76% · range méd 1.38%
- Excursion ouverture 15min (n=160) : bas méd −0.78% (p90 −2.6%) · haut méd +0.86% · range méd 1.76%
- Excursion ouverture 30min (n=160) : bas méd −0.83% (p90 −2.76%) · haut méd +0.97% · range méd 2.19%
- Excursion ouverture 60min (n=160) : bas méd −0.91% (p90 −2.85%) · haut méd +1.0% · range méd 2.36%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 4.854 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 84% (133/159) · gap 33% · délai 0.3min · rebond 64% (87/133) (MFE +1.32%)
   - −1.0% : fill 30min 51% · séance 77% (121/159) · gap 20% · délai 2.2min · rebond 67% (78/121) (MFE +1.52%)
   - −1.5% : fill 30min 34% · séance 58% (97/159) · gap 14% · délai 12.7min · rebond 62% (61/97) (MFE +1.39%)
   - −2.0% : fill 30min 29% · séance 47% (78/159) · gap 11% · délai 14.7min · rebond 64% (51/78) (MFE +1.43%)
   - −3.0% : fill 30min 14% · séance 31% (55/159) · gap 5% · délai 31.3min · rebond 70% (42/55) (MFE +1.87%)
   - −4.0% : fill 30min 7% · séance 19% (30/159) · gap 1% · délai 65.4min · rebond 59% (19/30) (MFE +1.42%)
   - −5.0% : fill 30min 3% · séance 8% (17/159) · gap 0% · délai 63.2min · rebond 75% (12/17) (MFE +2.03%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.35% (p90 −2.12%) → stop au-delà de −1.48% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.4% (p90 −2.04%) → stop au-delà de −1.22% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −1.73%) → stop au-delà de −0.98% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=787 jambes) : jambe baissière méd −1.05% (p90 −2.33%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (64 séances) :
      · −1.0% : fill 94% (61/64) · rebond 68% (36/61)
      · −2.0% : fill 66% (45/64) · rebond 66% (29/45)
      · −3.0% : fill 43% (34/64) · rebond 76% (26/34)
      · −4.0% : fill 28% (21/64) · rebond 65% (15/21)
      · −5.0% : fill 16% (14/64) · rebond 74% (10/14)
   - **flat** (40 séances) :
      · −1.0% : fill 86% (31/40) · rebond 75% (24/31)
      · −2.0% : fill 46% (16/40) · rebond 63% (11/16)
      · −3.0% : fill 27% (9/40) · rebond 69% (7/9)
      · −4.0% : fill 17% (4/40) · rebond 30% (1/4)
      · −5.0% : fill 5% (2/40) · rebond 72% (1/2)
   - **gap-up** (55 séances) :
      · −1.0% : fill 49% (29/55) · rebond 56% (18/29)
      · −2.0% : fill 26% (17/55) · rebond 60% (11/17)
      · −3.0% : fill 19% (12/55) · rebond 57% (9/12)
      · −4.0% : fill 8% (5/55) · rebond 80% (3/5)
      · −5.0% : fill 1% (1/55) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 59% en base · 69% si les 15 1res min sont vertes (79 cas) · 47% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:05** → P(séance verte=clôture>ouverture) 81% si début vert vs 34% si rouge (base 59% · écart 47 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **81%** · continue >prix actuel 58% ; creux résiduel méd -1.44% (q20 -2.29%) → **SL/trailing à −2.29%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.17% / q75 +2.38% → **scale +1.17% / runner +2.38%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **34%** (continue à baisser 48%) → **RÉDUIRE ~66%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.72%** (au-delà de la MAE q10 -3.72%), cible rebond +1.49% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.36% .. +2.42%] · haut q95 +3.63% · bas q05 -2.86%
   - 60min (n=160) : retour [-2.77% .. +3.01%] · haut q95 +4.3% · bas q05 -3.31%
   - 2h (n=160) : retour [-2.99% .. +3.18%] · haut q95 +4.49% · bas q05 -3.67%
   - 4h (n=160) : retour [-2.93% .. +2.99%] · haut q95 +4.49% · bas q05 -3.93%
   - 6h (n=160) : retour [-3.34% .. +3.23%] · haut q95 +4.62% · bas q05 -4.32%
   - session (n=160) : retour [-4.17% .. +4.07%] · haut q95 +5.58% · bas q05 -5.31%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.89%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 70.3  _(surachat)_
- **ADX** : 17.7  _(pas de tendance nette)_
- **MACD** : hist 0.02  _(pas de croisement recent)_
- **BB** : %B 0.65 · largeur 15.1%
- **ATR** : 0.18 (2.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.132  _(accumulation)_
- **Vol ratio** : 0.56  _(volume atone)_
- **Choppiness** : 49.9  _(transition)_
- **MA** : MA20 4.88 · MA50 4.96 · MA200 5.52  _(prix > MA20)_
- **Dist MA** : MA20 +2.3% · MA50 +0.6% · MA200 -9.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (94395 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
