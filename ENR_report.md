# ENR

**Generated** : 2026-07-03T00:06:15.931204+00:00  
**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €164.12  

> 🟡 **WAIT-FOR-DIP** — spot +22.2 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €164.12 (+22.2% vs entrée) · entrée €134.25 · stop €131.15 · T1 €140.45 · R/R 2.0  
> ↳ P(T1 av. stop) 37 % · EV/risk 0.117 · ¼-Kelly 0.01 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €133.01–€135.49 (mid €134.25)
- Spot actuel : €164.12 (+22.2% au-dessus de la zone — repli à attendre)
- Stop : €131.15 (stop swing_plan-based (-20.09%))
- Targets : T1 €140.45 · R/R 2.0 | T2 €146.64 · R/R 4.0 | T3 €152.83 · R/R 5.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €131.15


## Edge, scénarios & sizing

- EV/risk : 0.117 | EV/share : €0.361 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 13 % | T3 4 %
- Kelly (position) : f* 0.041 | ¼-Kelly 0.01 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 46.0 | bear 26.1 | side 27.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 492.0 (= 3 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→65% · +2.0%→49% · +3.0%→26% · +5.0%→9% · +8.0%→1%
- Range intraday médian 4.39% (p90 6.09%) · excursion haute méd. +1.69% / basse méd. −1.78%
- Profil de vol intra : ouverture 2.164% vs midi 1.0% vs clôture 1.211% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 59% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; neutre — autocorr -0.024)_ ; drift intra méd. -0.382% ; recovery-V 14%
- **σ réalisé intraday** 2.638% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 65% / bas 65% / whipsaw 30%
- POC intraday (dernière séance, temps-au-prix) : 167.7544 (VA 164.6731–168.4794 ; dernier close 163.01)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 17% · rebond 75% · **stop −1.46%** sous le fill (sous le bruit) · cible +1.5% · R/R 1.03 (high win-rate)
- Gaps overnight (n=159) : méd. 0.44% · baisse 39% (gap-down >1% 20% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.64% (p90 −1.8%) · haut méd +0.45% · range méd 1.25%
- Excursion ouverture 15min (n=160) : bas méd −0.78% (p90 −2.21%) · haut méd +0.59% · range méd 1.54%
- Excursion ouverture 30min (n=160) : bas méd −0.95% (p90 −2.4%) · haut méd +0.6% · range méd 1.87%
- Excursion ouverture 60min (n=160) : bas méd −1.01% (p90 −2.57%) · haut méd +0.76% · range méd 2.03%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 163.01 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 72% (113/159) · gap 27% · délai 0.4min · rebond 50% (56/113) (MFE +1.08%)
   - −1.0% : fill 30min 49% · séance 66% (101/159) · gap 20% · délai 1.7min · rebond 55% (58/101) (MFE +1.14%)
   - −1.5% : fill 30min 38% · séance 60% (88/159) · gap 17% · délai 13.2min · rebond 62% (55/88) (MFE +1.48%)
   - −2.0% : fill 30min 23% · séance 43% (64/159) · gap 10% · délai 23.1min · rebond 60% (38/64) (MFE +1.27%)
   - −3.0% : fill 30min 17% · séance 35% (49/159) · gap 4% · délai 126.0min · rebond 70% (36/49) (MFE +1.61%)
   - −4.0% : fill 30min 8% · séance 26% (37/159) · gap 2% · délai 302.8min · rebond 64% (25/37) (MFE +1.67%)
   - −5.0% : fill 30min 2% · séance 17% (21/159) · gap 1% · délai 378.8min · rebond 75% (14/21) (MFE +1.5%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.57% (p90 −1.96%) → stop au-delà de −1.19% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.57% (p90 −2.3%) → stop au-delà de −1.54% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −1.54%) → stop au-delà de −0.92% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=503 jambes) : jambe baissière méd −1.07% (p90 −2.55%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (45 séances) :
      · −1.0% : fill 95% (44/45) · rebond 55% (24/44)
      · −2.0% : fill 70% (32/45) · rebond 65% (21/32)
      · −3.0% : fill 63% (28/45) · rebond 67% (20/28)
      · −4.0% : fill 52% (23/45) · rebond 61% (16/23)
      · −5.0% : fill 37% (15/45) · rebond 74% (10/15)
   - **flat** (27 séances) :
      · −1.0% : fill 67% (19/27) · rebond 63% (13/19)
      · −2.0% : fill 27% (8/27) · rebond 35% (3/8)
      · −3.0% : fill 20% (5/27) · rebond 80% (3/5)
      · −4.0% : fill 17% (4/27) · rebond 76% (2/4)
      · −5.0% : fill 11% (2/27) · rebond 74% (1/2)
   - **gap-up** (87 séances) :
      · −1.0% : fill 49% (38/87) · rebond 52% (21/38)
      · −2.0% : fill 33% (24/87) · rebond 60% (14/24)
      · −3.0% : fill 22% (16/87) · rebond 74% (13/16)
      · −4.0% : fill 13% (10/87) · rebond 67% (7/10)
      · −5.0% : fill 7% (4/87) · rebond 78% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 86% si les 15 1res min sont vertes (78 cas) · 19% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:24** → P(séance verte=clôture>ouverture) 83% si début vert vs 18% si rouge (base 48% · écart 65 pts) ; prédictivité sature ensuite (plafond brut 83min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **83%** · continue >prix actuel 66% ; creux résiduel méd -0.96% (q20 -2.09%) → **SL/trailing à −2.09%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.01% / q75 +2.71% → **scale +2.01% / runner +2.71%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **18%** (continue à baisser 55%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.74%** (au-delà de la MAE q10 -4.74%), cible rebond +1.18% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.26% .. +2.05%] · haut q95 +2.74% · bas q05 -2.71%
   - 60min (n=160) : retour [-2.42% .. +2.21%] · haut q95 +2.85% · bas q05 -3.21%
   - 2h (n=160) : retour [-3.04% .. +2.57%] · haut q95 +3.41% · bas q05 -3.74%
   - 4h (n=160) : retour [-3.01% .. +2.67%] · haut q95 +4.2% · bas q05 -3.88%
   - 6h (n=160) : retour [-3.2% .. +3.94%] · haut q95 +4.84% · bas q05 -4.46%
   - session (n=160) : retour [-4.92% .. +4.43%] · haut q95 +5.75% · bas q05 -6.06%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — ENR = **plat / peu volatil** (vol intra méd 2.43%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 59.6  _(momentum haussier)_
- **ADX** : 15.1  _(pas de tendance nette)_
- **MACD** : hist 0.859  _(pas de croisement recent)_
- **BB** : %B 0.67 · largeur 19.9%
- **ATR** : 7.44 (69.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.095  _(distribution)_
- **Vol ratio** : 0.45  _(volume atone)_
- **Choppiness** : 58.2  _(transition)_
- **MA** : MA20 158.72 · MA50 167.86 · MA200 139.19  _(prix > MA20)_
- **Dist MA** : MA20 +3.4% · MA50 -2.2% · MA200 +17.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (87580 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
