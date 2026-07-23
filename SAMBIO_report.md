# 207940

**Generated** : 2026-07-23T21:53:29.762088+00:00  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite high · ₩1379000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)  
> ↳ spot ₩1379000.00 (+2.0% vs entrée) · entrée ₩1352375.00 · stop ₩1244185.00 · T1 ₩1375034.63 · R/R 0.21  
> ↳ P(T1 av. stop) 45 % _(réel 5 s)_ · EV/risk 0.007 _(réel 5 s)_ (GBM -0.072) · ¼-Kelly 0.059 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.090 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1347843.07–₩1356906.93 (mid ₩1352375.00)
- Spot actuel : ₩1379000.00 (+2.0% au-dessus de la zone — repli à attendre)
- Stop : ₩1244185.00 (stop swing_plan-based (-6.04%))
- Targets : T1 ₩1375034.63 · R/R 0.21 | T2 ₩1397694.27 · R/R 0.42 | T3 ₩1420353.90 · R/R 0.63
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1244185.00


## Edge, scénarios & sizing

- EV/risk : -0.072 | EV/share : ₩-7773.224 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 15 % | T3 4 %
- Kelly (position) : f* 0.238 | ¼-Kelly 0.059 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.0 | bear 17.8 | side 76.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.935% → cible +1.676% / stop −8.0%, p_fill 61%, n_eff≈23.8) : P(cible|rempli) **45%** · **EV/risk +0.007** (×p_fill ; si rempli +0.09% du capital)
  - **swing** (entrée dip −4.246% → cible +3.747% / stop −1.873%, p_fill 33%, n_eff≈12.5) : P(cible|rempli) **50%** · **EV/risk +0.165** (×p_fill ; si rempli +0.93% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=14, n_eff=10))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→68% · +1.0%→50% · +2.0%→34% · +3.0%→21% · +5.0%→4% · +8.0%→1%
- Range intraday médian 3.9% (p90 6.08%) · excursion haute méd. +0.98% / basse méd. −1.69%
- Profil de vol intra : ouverture 2.315% vs midi 0.651% vs clôture 0.781% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (138 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 13% · trend ↑0%/↓3% ; spike-down 59% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.136 ; neutre — autocorr -0.029)_ ; drift intra méd. -0.543% ; recovery-V 35%
- **σ réalisé intraday** 3.124% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 64% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 1400562.5 (VA 1395062.5–1403312.5 ; dernier close 1384000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 16% · rebond 60% · **stop −1.96%** sous le fill (sous le bruit) · cible +1.72% · R/R 0.88 (high win-rate)
- Gaps overnight (n=137) : méd. 0.44% · baisse 28% (gap-down >1% 7% · >2% 4%)
- Excursion ouverture 5min (n=138) : bas méd −0.88% (p90 −2.41%) · haut méd +0.48% · range méd 1.53%
- Excursion ouverture 15min (n=138) : bas méd −1.08% (p90 −2.91%) · haut méd +0.55% · range méd 1.92%
- Excursion ouverture 30min (n=138) : bas méd −1.25% (p90 −3.11%) · haut méd +0.59% · range méd 2.35%
- Excursion ouverture 60min (n=138) : bas méd −1.3% (p90 −3.49%) · haut méd +0.67% · range méd 2.68%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1384000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 74% (92/137) · gap 18% · délai 1.2min · rebond 52% (40/92) (MFE +1.03%)
   - −1.0% : fill 30min 47% · séance 60% (73/137) · gap 7% · délai 2.5min · rebond 53% (31/73) (MFE +1.13%)
   - −1.5% : fill 30min 38% · séance 48% (56/137) · gap 5% · délai 3.8min · rebond 52% (25/56) (MFE +1.14%)
   - −2.0% : fill 30min 26% · séance 42% (49/137) · gap 4% · délai 8.9min · rebond 64% (26/49) (MFE +1.34%)
   - −3.0% : fill 30min 8% · séance 28% (31/137) · gap 2% · délai 105.3min · rebond 60% (17/31) (MFE +1.39%)
   - −4.0% : fill 30min 4% · séance 16% (16/137) · gap 2% · délai 73.7min · rebond 60% (9/16) (MFE +1.72%)
   - −5.0% : fill 30min 2% · séance 8% (9/137) · gap 1% · délai 190.8min · rebond 65% (6/9) (MFE +1.55%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.75% (p90 −2.45%) → stop au-delà de −1.58% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.0% (p90 −2.09%) → stop au-delà de −1.56% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.18% (p90 −2.45%) → stop au-delà de −1.88% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=336 jambes) : jambe baissière méd −1.11% (p90 −2.69%) · ~8.0 jambes/séance
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
   - **gap-up** (66 séances) :
      · −1.0% : fill 42% (21/66) · rebond 60% (10/21)
      · −2.0% : fill 25% (14/66) · rebond 68% (9/14)
      · −3.0% : fill 20% (11/66) · rebond 40% (4/11)
      · −4.0% : fill 11% (5/66) · rebond 33% (2/5)
      · −5.0% : fill 7% (3/66) · rebond 35% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=138) : 38% en base · 61% si les 15 1res min sont vertes (47 cas) · 26% si rouges (91 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=138) : COUDE à **33min** → P(séance verte=clôture>ouverture) 66% si début vert vs 24% si rouge (base 38% · écart 42 pts) ; prédictivité sature ensuite (plafond brut 218min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=48) : tient le vert **66%** · continue >prix actuel 36% ; creux résiduel méd -1.41% (q20 -2.83%) → **SL/trailing à −2.83%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.14% / q75 +1.86% → **scale +1.14% / runner +1.86%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **24%** (continue à baisser 51%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.31%** (au-delà de la MAE q10 -3.31%), cible rebond +1.19% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=138) : retour [-3.04% .. +2.44%] · haut q95 +3.18% · bas q05 -3.55%
   - 60min (n=138) : retour [-3.56% .. +2.46%] · haut q95 +3.35% · bas q05 -3.93%
   - 2h (n=138) : retour [-4.42% .. +3.32%] · haut q95 +4.19% · bas q05 -4.85%
   - 4h (n=138) : retour [-5.33% .. +3.64%] · haut q95 +4.82% · bas q05 -5.54%
   - 6h (n=138) : retour [-5.33% .. +4.0%] · haut q95 +4.82% · bas q05 -6.1%
   - session (n=138) : retour [-4.91% .. +3.6%] · haut q95 +4.82% · bas q05 -6.1%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 207940 = **plat / peu volatil** (vol intra méd 2.01%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 46.7  _(neutre)_
- **ADX** : 9.0  _(pas de tendance nette)_
- **MACD** : hist -481.588  _(bearish_recent)_
- **BB** : %B 0.43 · largeur 8.4%
- **ATR** : 64785.71 (81.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.09  _(distribution)_
- **Vol ratio** : 0.82  _(volume normal)_
- **Choppiness** : 66.7  _(marche en range (choppy))_
- **MA** : MA20 1386950.0 · MA50 1370560.0 · MA200 1612265.67  _(prix < MA20)_
- **Dist MA** : MA20 -0.6% · MA50 +0.6% · MA200 -14.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83618 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
