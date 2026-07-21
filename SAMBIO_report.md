# 207940

**Generated** : 2026-07-21T00:18:51.565763+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite high · ₩1345000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot ₩1345000.00 (+1.4% vs entrée) · entrée ₩1326875.00 · stop ₩1220725.00 · T1 ₩1354299.60 · R/R 0.26  
> ↳ P(T1 av. stop) 30 % _(réel 5 s)_ · EV/risk -0.023 _(réel 5 s)_ (GBM -0.063) · ¼-Kelly 0.05 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.080 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1321390.08–₩1332359.92 (mid ₩1326875.00)
- Spot actuel : ₩1345000.00 (+1.4% au-dessus de la zone — repli à attendre)
- Stop : ₩1220725.00 (stop swing_plan-based (-5.21%))
- Targets : T1 ₩1354299.60 · R/R 0.26 | T2 ₩1381724.20 · R/R 0.52 | T3 ₩1409148.81 · R/R 0.78
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1220725.00


## Edge, scénarios & sizing

- EV/risk : -0.063 | EV/share : ₩-6701.164 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 33 % | T2 9 % | T3 4 %
- Kelly (position) : f* 0.201 | ¼-Kelly 0.05 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 30.7 | bear 12.2 | side 57.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.348% → cible +2.067% / stop −8.0%, p_fill 68%, n_eff≈27.6) : P(cible|rempli) **30%** · **EV/risk -0.023** (×p_fill ; si rempli -0.27% du capital)
  - **swing** (entrée dip −2.968% → cible +4.622% / stop −2.311%, p_fill 59%, n_eff≈21.4) : P(cible|rempli) **25%** · **EV/risk -0.053** (×p_fill ; si rempli -0.21% du capital)
  - **deep** (entrée dip −4.582% → cible +6.536% / stop −3.268%, p_fill 49%, n_eff≈17.1) : P(cible|rempli) **27%** · **EV/risk -0.113** (×p_fill ; si rempli -0.76% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→69% · +1.0%→50% · +2.0%→34% · +3.0%→21% · +5.0%→4% · +8.0%→1%
- Range intraday médian 3.87% (p90 6.08%) · excursion haute méd. +0.98% / basse méd. −1.69%
- Profil de vol intra : ouverture 2.282% vs midi 0.656% vs clôture 0.799% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (135 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 12% · trend ↑0%/↓4% ; spike-down 56% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; neutre — autocorr -0.017)_ ; drift intra méd. -0.368% ; recovery-V 35%
- **σ réalisé intraday** 3.139% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 63% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 1388512.5 (VA 1374487.5–1394887.5 ; dernier close 1396000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 16% · rebond 60% · **stop −1.96%** sous le fill (sous le bruit) · cible +1.72% · R/R 0.88 (high win-rate)
- Gaps overnight (n=134) : méd. 0.41% · baisse 30% (gap-down >1% 7% · >2% 4%)
- Excursion ouverture 5min (n=135) : bas méd −0.85% (p90 −2.38%) · haut méd +0.45% · range méd 1.51%
- Excursion ouverture 15min (n=135) : bas méd −1.07% (p90 −2.84%) · haut méd +0.51% · range méd 1.88%
- Excursion ouverture 30min (n=135) : bas méd −1.21% (p90 −3.03%) · haut méd +0.55% · range méd 2.24%
- Excursion ouverture 60min (n=135) : bas méd −1.26% (p90 −3.37%) · haut méd +0.64% · range méd 2.52%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1396000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 73% (89/134) · gap 19% · délai 1.1min · rebond 50% (38/89) (MFE +1.01%)
   - −1.0% : fill 30min 47% · séance 62% (72/134) · gap 7% · délai 2.0min · rebond 55% (31/72) (MFE +1.27%)
   - −1.5% : fill 30min 38% · séance 49% (55/134) · gap 6% · délai 3.4min · rebond 54% (25/55) (MFE +1.38%)
   - −2.0% : fill 30min 25% · séance 42% (48/134) · gap 4% · délai 12.0min · rebond 62% (25/48) (MFE +1.32%)
   - −3.0% : fill 30min 8% · séance 28% (30/134) · gap 2% · délai 116.1min · rebond 58% (16/30) (MFE +1.39%)
   - −4.0% : fill 30min 5% · séance 16% (16/134) · gap 2% · délai 73.7min · rebond 60% (9/16) (MFE +1.72%)
   - −5.0% : fill 30min 2% · séance 8% (9/134) · gap 2% · délai 190.8min · rebond 65% (6/9) (MFE +1.55%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.89% (p90 −2.45%) → stop au-delà de −1.72% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.95% (p90 −2.17%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.08% (p90 −2.53%) → stop au-delà de −1.94% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=321 jambes) : jambe baissière méd −1.09% (p90 −2.72%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (30 séances) :
      · −1.0% : fill 98% (29/30) · rebond 64% (14/29)
      · −2.0% : fill 85% (25/30) · rebond 65% (12/25)
      · −3.0% : fill 44% (13/30) · rebond 57% (7/13)
      · −4.0% : fill 26% (7/30) · rebond 58% (3/7)
      · −5.0% : fill 10% (4/30) · rebond 100% (4/4)
   - **flat** (41 séances) :
      · −1.0% : fill 69% (23/41) · rebond 31% (7/23)
      · −2.0% : fill 40% (10/41) · rebond 57% (5/10)
      · −3.0% : fill 30% (7/41) · rebond 97% (6/7)
      · −4.0% : fill 17% (4/41) · rebond 100% (4/4)
      · −5.0% : fill 8% (2/41) · rebond 89% (1/2)
   - **gap-up** (63 séances) :
      · −1.0% : fill 43% (20/63) · rebond 65% (10/20)
      · −2.0% : fill 24% (13/63) · rebond 63% (8/13)
      · −3.0% : fill 19% (10/63) · rebond 28% (3/10)
      · −4.0% : fill 12% (5/63) · rebond 33% (2/5)
      · −5.0% : fill 8% (3/63) · rebond 35% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=135) : 39% en base · 64% si les 15 1res min sont vertes (46 cas) · 24% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=135) : COUDE à **33min** → P(séance verte=clôture>ouverture) 66% si début vert vs 23% si rouge (base 39% · écart 43 pts) ; prédictivité sature ensuite (plafond brut 218min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=48) : tient le vert **66%** · continue >prix actuel 36% ; creux résiduel méd -1.41% (q20 -2.83%) → **SL/trailing à −2.83%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.14% / q75 +1.86% → **scale +1.14% / runner +1.86%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **23%** (continue à baisser 50%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.41%** (au-delà de la MAE q10 -3.41%), cible rebond +1.25% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=135) : retour [-2.94% .. +2.79%] · haut q95 +3.23% · bas q05 -3.39%
   - 60min (n=135) : retour [-3.23% .. +2.53%] · haut q95 +3.37% · bas q05 -3.66%
   - 2h (n=135) : retour [-4.07% .. +3.38%] · haut q95 +4.23% · bas q05 -4.46%
   - 4h (n=135) : retour [-4.41% .. +3.75%] · haut q95 +4.82% · bas q05 -5.37%
   - 6h (n=135) : retour [-4.7% .. +4.04%] · haut q95 +4.82% · bas q05 -5.4%
   - session (n=135) : retour [-4.75% .. +3.64%] · haut q95 +4.82% · bas q05 -5.43%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 207940 = **plat / peu volatil** (vol intra méd 1.99%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 37.2  _(momentum baissier)_
- **ADX** : 10.6  _(pas de tendance nette)_
- **MACD** : hist -1465.514  _(bearish_recent)_
- **BB** : %B 0.31 · largeur 12.5%
- **ATR** : 68642.86 (87.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.078  _(distribution)_
- **Vol ratio** : 0.73  _(volume normal)_
- **Choppiness** : 68.9  _(marche en range (choppy))_
- **MA** : MA20 1377300.0 · MA50 1375600.0 · MA200 1615236.79  _(prix < MA20)_
- **Dist MA** : MA20 -2.3% · MA50 -2.2% · MA200 -16.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (84091 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
