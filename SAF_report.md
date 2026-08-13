# SAF

**Generated** : 2026-08-13T00:06:01.710146+00:00  
**Santé technique** : 9/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €362.60  

> 🟢 **ARMED** — plan valide, prix dans/proche de la zone d'entrée — exécutable  
> ↳ spot €362.60 (+0.3% vs entrée) · entrée €361.43 · stop €352.30 · T1 €367.64 · R/R 0.68  
> ↳ P(T1 av. stop) 61 % _(réel 5 s)_ · EV/risk 0.049 _(réel 5 s)_ (GBM 0.021) · ¼-Kelly 0.009 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 275 % hors [0,100] (R² max 0.75). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 18.4 < 20 (tendance pas encore confirmée) alors que Choppiness 35.9 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._
- 🔴 **Santé haussière vs sur-extension** — Santé technique 9/10 élevée alors que : RSI 77.8 > 70 (surachat) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €360.27–€362.60 (mid €361.43)
- Spot actuel : €362.60 (+0.3% au-dessus de la zone — repli à attendre)
- Stop : €352.30 (stop swing_plan-based (-2.84%))
- Targets : T1 €367.64 · R/R 0.68 | T2 €373.85 · R/R 1.36 | T3 €380.07 · R/R 2.04
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €352.30


## Edge, scénarios & sizing

- EV/risk : 0.021 | EV/share : €0.191 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 58 % | T2 36 % | T3 23 %
- Kelly (position) : f* 0.035 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 39.3 | side 55.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 363.0 (= 1 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.296% → cible +0.768% / stop −2.0%, p_fill 81%, n_eff≈33.1) : P(cible|rempli) **67%** · **EV/risk -0.001** (×p_fill ; si rempli -0.00% du capital)
  - **swing** (entrée dip −0.322% → cible +1.718% / stop −2.526%, p_fill 86%, n_eff≈34.2) : P(cible|rempli) **61%** · **EV/risk +0.049** (×p_fill ; si rempli +0.14% du capital)
  - **deep** (entrée dip −0.454% → cible +2.43% / stop −3.794%, p_fill 87%, n_eff≈32.9) : P(cible|rempli) **67%** · **EV/risk +0.056** (×p_fill ; si rempli +0.24% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→55% · +2.0%→31% · +3.0%→12% · +5.0%→1% · +8.0%→1%
- Range intraday médian 2.66% (p90 4.41%) · excursion haute méd. +1.2% / basse méd. −0.94%
- Profil de vol intra : ouverture 1.672% vs midi 0.613% vs clôture 0.72% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 40% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.089 ; mean-reverting — autocorr -0.051)_ ; drift intra méd. 0.113% ; recovery-V 29%
- **σ réalisé intraday** 1.813% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 76% / bas 52% / whipsaw 30%
- POC intraday (dernière séance, temps-au-prix) : 360.7587 (VA 359.9013–361.8613 ; dernier close 361.1)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 16% · rebond 54% · **stop −1.63%** sous le fill (sous le bruit) · cible +1.2% · R/R 0.74 (high win-rate)
- Gaps overnight (n=159) : méd. 0.13% · baisse 46% (gap-down >1% 8% · >2% 1%)
- Excursion ouverture 5min (n=160) : bas méd −0.44% (p90 −1.84%) · haut méd +0.19% · range méd 0.94%
- Excursion ouverture 15min (n=160) : bas méd −0.62% (p90 −1.92%) · haut méd +0.32% · range méd 1.2%
- Excursion ouverture 30min (n=160) : bas méd −0.62% (p90 −1.93%) · haut méd +0.53% · range méd 1.38%
- Excursion ouverture 60min (n=160) : bas méd −0.69% (p90 −1.98%) · haut méd +0.57% · range méd 1.58%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 361.1 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 68% (113/159) · gap 20% · délai 0.2min · rebond 43% (45/113) (MFE +0.85%)
   - −1.0% : fill 30min 38% · séance 49% (83/159) · gap 8% · délai 0.4min · rebond 45% (32/83) (MFE +0.69%)
   - −1.5% : fill 30min 26% · séance 39% (69/159) · gap 3% · délai 7.5min · rebond 45% (26/69) (MFE +0.91%)
   - −2.0% : fill 30min 12% · séance 30% (52/159) · gap 1% · délai 52.5min · rebond 52% (24/52) (MFE +1.14%)
   - −3.0% : fill 30min 3% · séance 16% (29/159) · gap 0% · délai 87.1min · rebond 54% (17/29) (MFE +1.2%)
   - −4.0% : fill 30min 2% · séance 7% (13/159) · gap 0% · délai 126.9min · rebond 62% (7/13) (MFE +1.25%)
   - −5.0% : fill 30min 0% · séance 1% (3/159) · gap 0% · délai 360.2min · rebond 31% (1/3) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.23% (p90 −0.88%) → stop au-delà de −0.71% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −0.78%) → stop au-delà de −0.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=210 jambes) : jambe baissière méd −1.06% (p90 −2.39%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 83% (45/55) · rebond 41% (17/45)
      · −2.0% : fill 60% (32/55) · rebond 48% (15/32)
      · −3.0% : fill 29% (17/55) · rebond 50% (9/17)
      · −4.0% : fill 15% (9/55) · rebond 69% (5/9)
      · −5.0% : fill 2% (2/55) · rebond 0% (0/2)
   - **flat** (41 séances) :
      · −1.0% : fill 43% (19/41) · rebond 56% (10/19)
      · −2.0% : fill 20% (9/41) · rebond 75% (5/9)
      · −3.0% : fill 10% (5/41) · rebond 85% (4/5)
      · −4.0% : fill 1% (1/41) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/41) · rebond 0% (0/0)
   - **gap-up** (63 séances) :
      · −1.0% : fill 26% (19/63) · rebond 42% (5/19)
      · −2.0% : fill 14% (11/63) · rebond 43% (4/11)
      · −3.0% : fill 9% (7/63) · rebond 36% (4/7)
      · −4.0% : fill 4% (3/63) · rebond 30% (1/3)
      · −5.0% : fill 1% (1/63) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 67% si les 15 1res min sont vertes (74 cas) · 34% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **44min** → P(séance verte=clôture>ouverture) 77% si début vert vs 26% si rouge (base 51% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 294min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **77%** · continue >prix actuel 55% ; creux résiduel méd -0.74% (q20 -1.46%) → **SL/trailing à −1.46%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.0% / q75 +1.62% → **scale +1.0% / runner +1.62%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **26%** (continue à baisser 45%) → **RÉDUIRE ~74%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.41%** (au-delà de la MAE q10 -2.41%), cible rebond +1.05% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.59% .. +1.58%] · haut q95 +1.99% · bas q05 -2.25%
   - 60min (n=160) : retour [-1.64% .. +2.16%] · haut q95 +2.44% · bas q05 -2.52%
   - 2h (n=160) : retour [-2.28% .. +2.23%] · haut q95 +2.61% · bas q05 -2.97%
   - 4h (n=160) : retour [-2.07% .. +2.2%] · haut q95 +2.85% · bas q05 -3.21%
   - 6h (n=160) : retour [-2.17% .. +2.53%] · haut q95 +3.15% · bas q05 -3.49%
   - session (n=160) : retour [-3.08% .. +2.66%] · haut q95 +3.62% · bas q05 -4.01%


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
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 77.8  _(surachat)_
- **ADX** : 18.4  _(pas de tendance nette)_
- **MACD** : hist 2.007  _(pas de croisement recent)_
- **BB** : %B 0.85 · largeur 17.4%
- **ATR** : 9.13 (62.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.159  _(accumulation)_
- **Vol ratio** : 0.27  _(volume atone)_
- **Choppiness** : 35.9  _(marche directionnel)_
- **MA** : MA20 341.89 · MA50 332.6 · MA200 307.4  _(prix > MA20)_
- **Dist MA** : MA20 +6.1% · MA50 +9.0% · MA200 +18.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93465 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
