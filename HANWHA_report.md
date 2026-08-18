# 012450

**Generated** : 2026-08-18T21:54:08.622112+00:00  
**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1135000.00  

> 🟡 **WAIT-FOR-DIP** — spot +10.1 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩1135000.00 (+10.1% vs entrée) · entrée ₩1030741.12 · stop ₩957812.55 · T1 ₩1092413.96 · R/R 0.85  
> ↳ P(T1 av. stop) 83 % · EV/risk 0.301 · ¼-Kelly 0.004 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 16.8 < 20 (tendance pas encore confirmée) alors que Choppiness 32.8 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._
- 🔴 **Santé haussière vs sur-extension** — Santé technique 7/10 élevée alors que : RSI 71.7 > 70 (surachat) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩1018406.55–₩1043075.68 (mid ₩1030741.12)
- Spot actuel : ₩1135000.00 (+10.1% au-dessus de la zone — repli à attendre)
- Stop : ₩957812.55 (stop swing_plan-based (-15.61%))
- Targets : T1 ₩1092413.96 · R/R 0.85 | T2 ₩1154086.80 · R/R 1.69 | T3 ₩1215759.64 · R/R 2.54
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩957812.55


## Edge, scénarios & sizing

- EV/risk : 0.019 | EV/share : ₩1361.765 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 48 % | T2 22 % | T3 13 %
- Kelly (position) : f* 0.018 | ¼-Kelly 0.004 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 25.8 | bear 68.6 | side 5.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.174% → cible +2.676% / stop −8.0%, p_fill 31%, n_eff≈18.0) : P(cible|rempli) **20%** · **EV/risk -0.043** (×p_fill ; si rempli -1.11% du capital)
  - **swing** (entrée dip −9.184% → cible +5.983% / stop −7.075%, p_fill 21%, n_eff≈10.6) : P(cible|rempli) **44%** · **EV/risk -0.045** (×p_fill ; si rempli -1.50% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=8, n_eff=7))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→65% · +2.0%→46% · +3.0%→30% · +5.0%→19% · +8.0%→4%
- Range intraday médian 6.31% (p90 9.56%) · excursion haute méd. +1.91% / basse méd. −2.94%
- Profil de vol intra : ouverture 4.441% vs midi 1.239% vs clôture 1.279% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (159 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓0% ; spike-down 80% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; mean-reverting — autocorr -0.047)_ ; drift intra méd. -0.089% ; recovery-V 38%
- **σ réalisé intraday** 4.479% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 51% / bas 44% / whipsaw 11%
- POC intraday (dernière séance, temps-au-prix) : 1138475.0 (VA 1135025.0–1155725.0 ; dernier close 1160000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 33% · rebond 78% · **stop −5.03%** sous le fill (sous le bruit) · cible +2.07% · R/R 0.41 (high win-rate)
- Gaps overnight (n=158) : méd. 0.61% · baisse 32% (gap-down >1% 18% · >2% 8%)
- Excursion ouverture 5min (n=159) : bas méd −1.53% (p90 −4.05%) · haut méd +0.98% · range méd 2.92%
- Excursion ouverture 15min (n=159) : bas méd −1.97% (p90 −4.71%) · haut méd +1.28% · range méd 3.65%
- Excursion ouverture 30min (n=159) : bas méd −2.1% (p90 −5.12%) · haut méd +1.29% · range méd 4.1%
- Excursion ouverture 60min (n=159) : bas méd −2.17% (p90 −5.58%) · haut méd +1.59% · range méd 4.53%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1160000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 70% (112/158) · gap 20% · délai 0.1min · rebond 51% (57/112) (MFE +1.05%)
   - −1.0% : fill 30min 55% · séance 66% (107/158) · gap 18% · délai 0.9min · rebond 56% (63/107) (MFE +1.01%)
   - −1.5% : fill 30min 49% · séance 59% (98/158) · gap 10% · délai 1.4min · rebond 58% (56/98) (MFE +1.24%)
   - −2.0% : fill 30min 41% · séance 52% (81/158) · gap 8% · délai 3.6min · rebond 64% (50/81) (MFE +1.49%)
   - −3.0% : fill 30min 28% · séance 42% (60/158) · gap 2% · délai 5.3min · rebond 74% (42/60) (MFE +1.8%)
   - −4.0% : fill 30min 18% · séance 33% (46/158) · gap 2% · délai 21.8min · rebond 78% (37/46) (MFE +2.07%)
   - −5.0% : fill 30min 12% · séance 23% (33/158) · gap 1% · délai 26.0min · rebond 80% (27/33) (MFE +2.21%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.58% (p90 −2.51%) → stop au-delà de −2.05% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.69% (p90 −2.83%) → stop au-delà de −2.61% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.81% (p90 −2.87%) → stop au-delà de −2.63% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=773 jambes) : jambe baissière méd −1.2% (p90 −3.22%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (36 séances) :
      · −1.0% : fill 87% (34/36) · rebond 45% (15/34)
      · −2.0% : fill 82% (31/36) · rebond 61% (18/31)
      · −3.0% : fill 79% (28/36) · rebond 77% (20/28)
      · −4.0% : fill 68% (25/36) · rebond 90% (21/25)
      · −5.0% : fill 40% (16/36) · rebond 88% (14/16)
   - **flat** (20 séances) :
      · −1.0% : fill 90% (19/20) · rebond 49% (10/19)
      · −2.0% : fill 69% (15/20) · rebond 48% (7/15)
      · −3.0% : fill 53% (9/20) · rebond 37% (3/9)
      · −4.0% : fill 53% (9/20) · rebond 48% (5/9)
      · −5.0% : fill 51% (8/20) · rebond 52% (4/8)
   - **gap-up** (102 séances) :
      · −1.0% : fill 51% (54/102) · rebond 66% (38/54)
      · −2.0% : fill 35% (35/102) · rebond 74% (25/35)
      · −3.0% : fill 24% (23/102) · rebond 87% (19/23)
      · −4.0% : fill 14% (12/102) · rebond 80% (11/12)
      · −5.0% : fill 10% (9/102) · rebond 100% (9/9)
- **P(clôture VERTE) selon le drive 15min** (n=159) : 43% en base · 75% si les 15 1res min sont vertes (56 cas) · 20% si rouges (103 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=159) : COUDE à **35min** → P(séance verte=clôture>ouverture) 86% si début vert vs 10% si rouge (base 43% · écart 77 pts) ; prédictivité sature ensuite (plafond brut 184min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=57) : tient le vert **86%** · continue >prix actuel 57% ; creux résiduel méd -1.47% (q20 -3.26%) → **SL/trailing à −3.26%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.78% / q75 +4.31% → **scale +2.78% / runner +4.31%**, sortie à la clôture
  - **si ROUGE au coude** (n=102) : edge inversé — récupère vert seulement **10%** (continue à baisser 50%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.87%** (au-delà de la MAE q10 -5.87%), cible rebond +1.88% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=159) : retour [-5.07% .. +3.94%] · haut q95 +5.55% · bas q05 -6.21%
   - 60min (n=159) : retour [-5.2% .. +4.8%] · haut q95 +6.88% · bas q05 -6.28%
   - 2h (n=159) : retour [-6.95% .. +6.18%] · haut q95 +7.35% · bas q05 -8.44%
   - 4h (n=159) : retour [-7.4% .. +5.95%] · haut q95 +7.86% · bas q05 -8.96%
   - 6h (n=159) : retour [-6.81% .. +6.52%] · haut q95 +8.5% · bas q05 -9.16%
   - session (n=159) : retour [-6.97% .. +6.52%] · haut q95 +8.5% · bas q05 -9.16%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 012450 = **volatil sans tendance propre (choppy)** (vol intra méd 3.54%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 71.7  _(surachat)_
- **ADX** : 16.8  _(pas de tendance nette)_
- **MACD** : hist 27256.271  _(pas de croisement recent)_
- **BB** : %B 0.78 · largeur 47.1%
- **ATR** : 72928.57 (58.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.065  _(accumulation)_
- **Vol ratio** : 0.43  _(volume atone)_
- **Choppiness** : 32.8  _(marche directionnel)_
- **MA** : MA20 1003000.0 · MA50 1031460.0 · MA200 1145037.75  _(prix > MA20)_
- **Dist MA** : MA20 +13.2% · MA50 +10.0% · MA200 -0.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (82785 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
