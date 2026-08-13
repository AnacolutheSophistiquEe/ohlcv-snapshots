# RHM

**Generated** : 2026-08-13T00:00:56.714851+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €1175.80  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €1175.80 (+0.9% vs entrée) · entrée €1165.50 · stop €1142.19 · T1 €1178.82 · R/R 0.57  
> ↳ P(T1 av. stop) 52 % _(réel 5 s)_ · EV/risk -0.012 _(réel 5 s)_ (GBM 0.097) · ¼-Kelly 0.043 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 7/10 élevée alors que : RSI 76.8 > 70 (surachat) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €1162.84–€1168.16 (mid €1165.50)
- Spot actuel : €1175.80 (+0.9% au-dessus de la zone — repli à attendre)
- Stop : €1142.19 (stop swing_plan-based (-6.69%))
- Targets : T1 €1178.82 · R/R 0.57 | T2 €1192.15 · R/R 1.14 | T3 €1205.47 · R/R 1.71
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €1142.19


## Edge, scénarios & sizing

- EV/risk : 0.097 | EV/share : €2.265 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 65 % | T2 42 % | T3 25 %
- Kelly (position) : f* 0.173 | ¼-Kelly 0.043 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 26.4 | bear 5.0 | side 68.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.878% → cible +1.143% / stop −2.0%, p_fill 84%, n_eff≈34.2) : P(cible|rempli) **52%** · **EV/risk -0.012** (×p_fill ; si rempli -0.03% du capital)
  - **swing** (entrée dip −1.922% → cible +2.556% / stop −4.861%, p_fill 49%, n_eff≈22.0) : P(cible|rempli) **72%** · **EV/risk +0.066** (×p_fill ; si rempli +0.65% du capital)
  - **deep** (entrée dip −2.979% → cible +3.615% / stop −7.371%, p_fill 43%, n_eff≈19.4) : P(cible|rempli) **59%** · **EV/risk -0.066** (×p_fill ; si rempli -1.13% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→70% · +2.0%→50% · +3.0%→31% · +5.0%→4% · +8.0%→1%
- Range intraday médian 4.12% (p90 6.98%) · excursion haute méd. +2.05% / basse méd. −1.62%
- Profil de vol intra : ouverture 2.658% vs midi 0.92% vs clôture 1.118% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 10% · trend ↑0%/↓0% ; spike-down 52% · recovery-V 37%)_
- **Régime intraday** : **chop** _(efficiency 0.083 ; neutre — autocorr -0.017)_ ; drift intra méd. -0.058% ; recovery-V 35%
- **σ réalisé intraday** 2.955% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 64% / whipsaw 38%
- POC intraday (dernière séance, temps-au-prix) : 1145.785 (VA 1143.415–1151.315 ; dernier close 1144.1)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 42% · rebond 67% · **stop −3.18%** sous le fill (sous le bruit) · cible +1.57% · R/R 0.49 (high win-rate)
- Gaps overnight (n=159) : méd. 0.2% · baisse 36% (gap-down >1% 11% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.71% (p90 −1.7%) · haut méd +0.64% · range méd 1.38%
- Excursion ouverture 15min (n=160) : bas méd −0.91% (p90 −1.99%) · haut méd +0.72% · range méd 1.82%
- Excursion ouverture 30min (n=160) : bas méd −0.92% (p90 −2.35%) · haut méd +0.91% · range méd 2.09%
- Excursion ouverture 60min (n=160) : bas méd −0.97% (p90 −2.62%) · haut méd +1.06% · range méd 2.25%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1144.1 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 72% (117/159) · gap 24% · délai 0.3min · rebond 58% (64/117) (MFE +1.32%)
   - −1.0% : fill 30min 42% · séance 64% (106/159) · gap 11% · délai 5.5min · rebond 65% (63/106) (MFE +1.33%)
   - −1.5% : fill 30min 28% · séance 54% (84/159) · gap 7% · délai 24.8min · rebond 61% (47/84) (MFE +1.36%)
   - −2.0% : fill 30min 20% · séance 42% (72/159) · gap 6% · délai 30.4min · rebond 67% (45/72) (MFE +1.57%)
   - −3.0% : fill 30min 10% · séance 26% (45/159) · gap 4% · délai 116.9min · rebond 62% (27/45) (MFE +1.39%)
   - −4.0% : fill 30min 4% · séance 19% (28/159) · gap 1% · délai 245.4min · rebond 64% (16/28) (MFE +1.5%)
   - −5.0% : fill 30min 1% · séance 10% (16/159) · gap 1% · délai 293.4min · rebond 56% (8/16) (MFE +1.7%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.55% (p90 −1.64%) → stop au-delà de −1.16% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.46% (p90 −1.77%) → stop au-delà de −1.34% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.29% (p90 −1.89%) → stop au-delà de −1.42% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=507 jambes) : jambe baissière méd −1.07% (p90 −2.56%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 94% (47/49) · rebond 65% (28/47)
      · −2.0% : fill 79% (38/49) · rebond 66% (25/38)
      · −3.0% : fill 53% (26/49) · rebond 63% (16/26)
      · −4.0% : fill 40% (16/49) · rebond 75% (11/16)
      · −5.0% : fill 22% (9/49) · rebond 83% (7/9)
   - **flat** (46 séances) :
      · −1.0% : fill 69% (33/46) · rebond 72% (21/33)
      · −2.0% : fill 27% (17/46) · rebond 72% (10/17)
      · −3.0% : fill 18% (10/46) · rebond 55% (5/10)
      · −4.0% : fill 16% (8/46) · rebond 36% (2/8)
      · −5.0% : fill 10% (6/46) · rebond 22% (1/6)
   - **gap-up** (64 séances) :
      · −1.0% : fill 43% (26/64) · rebond 59% (14/26)
      · −2.0% : fill 28% (17/64) · rebond 67% (10/17)
      · −3.0% : fill 13% (9/64) · rebond 66% (6/9)
      · −4.0% : fill 7% (4/64) · rebond 61% (3/4)
      · −5.0% : fill 3% (1/64) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 60% si les 15 1res min sont vertes (82 cas) · 41% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 70% si début vert vs 31% si rouge (base 50% · écart 39 pts) ; prédictivité sature ensuite (plafond brut 225min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **70%** · continue >prix actuel 43% ; creux résiduel méd -1.4% (q20 -3.22%) → **SL/trailing à −3.22%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.33% / q75 +1.91% → **scale +1.33% / runner +1.91%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **31%** (continue à baisser 46%) → **RÉDUIRE ~69%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.74%** (au-delà de la MAE q10 -4.74%), cible rebond +1.16% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.62% .. +3.33%] · haut q95 +3.84% · bas q05 -3.28%
   - 60min (n=160) : retour [-2.89% .. +3.15%] · haut q95 +4.21% · bas q05 -4.23%
   - 2h (n=160) : retour [-3.32% .. +3.1%] · haut q95 +4.35% · bas q05 -4.59%
   - 4h (n=160) : retour [-3.73% .. +3.38%] · haut q95 +4.74% · bas q05 -4.81%
   - 6h (n=160) : retour [-4.31% .. +3.49%] · haut q95 +4.81% · bas q05 -5.35%
   - session (n=160) : retour [-5.89% .. +4.23%] · haut q95 +5.09% · bas q05 -6.23%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.31%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 76.9  _(surachat)_
- **ADX** : 23.3  _(pas de tendance nette)_
- **MACD** : hist 10.428  _(pas de croisement recent)_
- **BB** : %B 0.76 · largeur 30.9%
- **ATR** : 56.06 (39.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.025  _(neutre)_
- **Vol ratio** : 0.63  _(volume normal)_
- **Choppiness** : 47.0  _(transition)_
- **MA** : MA20 1087.24 · MA50 1098.16 · MA200 1439.3  _(prix > MA20)_
- **Dist MA** : MA20 +8.1% · MA50 +7.1% · MA200 -18.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90931 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
