# 207940

**Generated** : 2026-07-22T00:19:03.190409+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite high · ₩1395000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot ₩1395000.00 (+2.2% vs entrée) · entrée ₩1364375.00 · stop ₩1255225.00 · T1 ₩1391276.58 · R/R 0.25  
> ↳ P(T1 av. stop) 41 % _(réel 5 s)_ · EV/risk 0.01 _(réel 5 s)_ (GBM -0.07) · ¼-Kelly 0.052 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.020 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1358994.68–₩1369755.32 (mid ₩1364375.00)
- Spot actuel : ₩1395000.00 (+2.2% au-dessus de la zone — repli à attendre)
- Stop : ₩1255225.00 (stop swing_plan-based (-6.93%))
- Targets : T1 ₩1391276.58 · R/R 0.25 | T2 ₩1418178.16 · R/R 0.49 | T3 ₩1445079.73 · R/R 0.74
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1255225.00


## Edge, scénarios & sizing

- EV/risk : -0.07 | EV/share : ₩-7630.988 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 10 % | T3 4 %
- Kelly (position) : f* 0.208 | ¼-Kelly 0.052 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 10.7 | bear 15.2 | side 74.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.196% → cible +1.972% / stop −8.0%, p_fill 60%, n_eff≈22.1) : P(cible|rempli) **41%** · **EV/risk +0.010** (×p_fill ; si rempli +0.13% du capital)
  - **swing** (entrée dip −4.832% → cible +4.409% / stop −2.204%, p_fill 26%, n_eff≈9.6) : P(cible|rempli) **51%** · **EV/risk +0.143** (×p_fill ; si rempli +1.24% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=9, n_eff=7))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→68% · +1.0%→50% · +2.0%→34% · +3.0%→21% · +5.0%→4% · +8.0%→1%
- Range intraday médian 3.93% (p90 6.09%) · excursion haute méd. +0.98% / basse méd. −1.79%
- Profil de vol intra : ouverture 2.323% vs midi 0.655% vs clôture 0.808% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (136 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 14% · trend ↑0%/↓4% ; spike-down 57% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.132 ; neutre — autocorr -0.017)_ ; drift intra méd. -0.577% ; recovery-V 33%
- **σ réalisé intraday** 3.188% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 65% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 1352962.5 (VA 1344262.5–1363837.5 ; dernier close 1358000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 16% · rebond 60% · **stop −1.96%** sous le fill (sous le bruit) · cible +1.72% · R/R 0.88 (high win-rate)
- Gaps overnight (n=135) : méd. 0.43% · baisse 30% (gap-down >1% 7% · >2% 4%)
- Excursion ouverture 5min (n=136) : bas méd −0.88% (p90 −2.44%) · haut méd +0.45% · range méd 1.51%
- Excursion ouverture 15min (n=136) : bas méd −1.08% (p90 −2.93%) · haut méd +0.51% · range méd 1.9%
- Excursion ouverture 30min (n=136) : bas méd −1.25% (p90 −3.13%) · haut méd +0.54% · range méd 2.35%
- Excursion ouverture 60min (n=136) : bas méd −1.28% (p90 −3.49%) · haut méd +0.63% · range méd 2.58%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1358000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 73% (90/135) · gap 18% · délai 1.1min · rebond 49% (38/90) (MFE +0.95%)
   - −1.0% : fill 30min 48% · séance 62% (73/135) · gap 7% · délai 2.5min · rebond 53% (31/73) (MFE +1.13%)
   - −1.5% : fill 30min 40% · séance 50% (56/135) · gap 6% · délai 3.8min · rebond 52% (25/56) (MFE +1.14%)
   - −2.0% : fill 30min 26% · séance 43% (49/135) · gap 4% · délai 8.9min · rebond 64% (26/49) (MFE +1.34%)
   - −3.0% : fill 30min 8% · séance 29% (31/135) · gap 2% · délai 105.3min · rebond 60% (17/31) (MFE +1.39%)
   - −4.0% : fill 30min 5% · séance 16% (16/135) · gap 2% · délai 73.7min · rebond 60% (9/16) (MFE +1.72%)
   - −5.0% : fill 30min 2% · séance 8% (9/135) · gap 2% · délai 190.8min · rebond 65% (6/9) (MFE +1.55%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.89% (p90 −2.45%) → stop au-delà de −1.72% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.95% (p90 −2.17%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.08% (p90 −2.53%) → stop au-delà de −1.94% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=327 jambes) : jambe baissière méd −1.1% (p90 −2.75%) · ~8.0 jambes/séance
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
   - **gap-up** (64 séances) :
      · −1.0% : fill 45% (21/64) · rebond 60% (10/21)
      · −2.0% : fill 27% (14/64) · rebond 68% (9/14)
      · −3.0% : fill 22% (11/64) · rebond 40% (4/11)
      · −4.0% : fill 12% (5/64) · rebond 33% (2/5)
      · −5.0% : fill 8% (3/64) · rebond 35% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=136) : 38% en base · 64% si les 15 1res min sont vertes (46 cas) · 23% si rouges (90 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=136) : COUDE à **33min** → P(séance verte=clôture>ouverture) 66% si début vert vs 22% si rouge (base 38% · écart 44 pts) ; prédictivité sature ensuite (plafond brut 218min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=48) : tient le vert **66%** · continue >prix actuel 36% ; creux résiduel méd -1.41% (q20 -2.83%) → **SL/trailing à −2.83%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.14% / q75 +1.86% → **scale +1.14% / runner +1.86%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **22%** (continue à baisser 51%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.37%** (au-delà de la MAE q10 -3.37%), cible rebond +1.19% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=136) : retour [-3.06% .. +2.67%] · haut q95 +3.21% · bas q05 -3.56%
   - 60min (n=136) : retour [-3.57% .. +2.51%] · haut q95 +3.37% · bas q05 -4.0%
   - 2h (n=136) : retour [-4.45% .. +3.36%] · haut q95 +4.22% · bas q05 -4.88%
   - 4h (n=136) : retour [-5.34% .. +3.71%] · haut q95 +4.82% · bas q05 -5.61%
   - 6h (n=136) : retour [-5.4% .. +4.03%] · haut q95 +4.82% · bas q05 -6.1%
   - session (n=136) : retour [-4.93% .. +3.62%] · haut q95 +4.82% · bas q05 -6.1%


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

- **RSI** : 50.5  _(neutre)_
- **ADX** : 10.0  _(pas de tendance nette)_
- **MACD** : hist -26.931  _(bearish_recent)_
- **BB** : %B 0.58 · largeur 11.2%
- **ATR** : 68000.0 (86.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.017  _(neutre)_
- **Vol ratio** : 0.93  _(volume normal)_
- **Choppiness** : 68.5  _(marche en range (choppy))_
- **MA** : MA20 1382300.0 · MA50 1374140.0 · MA200 1614362.67  _(prix > MA20)_
- **Dist MA** : MA20 +0.9% · MA50 +1.5% · MA200 -13.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83646 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
