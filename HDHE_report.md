# 267260

**Generated** : 2026-08-13T00:15:06.808893+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩782000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩782000.00 (+1.4% vs entrée) · entrée ₩771348.65 · stop ₩709640.75 · T1 ₩836988.64 · R/R 1.06  
> ↳ P(T1 av. stop) 2 % _(réel 5 s)_ · EV/risk -0.088 _(réel 5 s)_ (GBM -0.183) · ¼-Kelly 0.002 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.010 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩764918.25–₩777779.04 (mid ₩771348.65)
- Spot actuel : ₩782000.00 (+1.4% au-dessus de la zone — repli à attendre)
- Stop : ₩709640.75 (stop swing_plan-based (-11.52%))
- Targets : T1 ₩836988.64 · R/R 1.06 | T2 ₩852250.46 · R/R 1.31 | T3 ₩867512.28 · R/R 1.56
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩709640.75


## Edge, scénarios & sizing

- EV/risk : -0.183 | EV/share : ₩-11323.398 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 12 % | T2 12 % | T3 12 %
- Kelly (position) : f* 0.009 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 10.7 | bear 52.1 | side 37.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.359% → cible +8.51% / stop −8.0%, p_fill 90%, n_eff≈36.1) : P(cible|rempli) **2%** · **EV/risk -0.088** (×p_fill ; si rempli -0.78% du capital)
  - **swing** (entrée dip −2.996% → cible +9.292% / stop −8.788%, p_fill 84%, n_eff≈36.2) : P(cible|rempli) **42%** · **EV/risk -0.097** (×p_fill ; si rempli -1.01% du capital)
  - **deep** (entrée dip −4.634% → cible +13.141% / stop −13.407%, p_fill 81%, n_eff≈32.0) : P(cible|rempli) **24%** · **EV/risk -0.334** (×p_fill ; si rempli -5.50% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→68% · +2.0%→46% · +3.0%→36% · +5.0%→12% · +8.0%→5%
- Range intraday médian 6.81% (p90 10.58%) · excursion haute méd. +1.77% / basse méd. −3.96%
- Profil de vol intra : ouverture 4.495% vs midi 1.219% vs clôture 1.27% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (152 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 81% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; mean-reverting — autocorr -0.062)_ ; drift intra méd. -1.706% ; recovery-V 22%
- **σ réalisé intraday** 4.778% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 69% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 742025.0 (VA 738875.0–748775.0 ; dernier close 741000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 34% · rebond 82% · **stop −4.53%** sous le fill (sous le bruit) · cible +2.54% · R/R 0.56 (high win-rate)
- Gaps overnight (n=151) : méd. 1.13% · baisse 40% (gap-down >1% 21% · >2% 11%)
- Excursion ouverture 5min (n=152) : bas méd −1.74% (p90 −4.04%) · haut méd +0.97% · range méd 2.95%
- Excursion ouverture 15min (n=152) : bas méd −1.98% (p90 −4.69%) · haut méd +1.06% · range méd 3.58%
- Excursion ouverture 30min (n=152) : bas méd −2.34% (p90 −5.1%) · haut méd +1.12% · range méd 3.84%
- Excursion ouverture 60min (n=152) : bas méd −2.95% (p90 −5.67%) · haut méd +1.33% · range méd 4.21%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 741000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 72% (107/151) · gap 32% · délai 0.0min · rebond 55% (60/107) (MFE +1.26%)
   - −1.0% : fill 30min 56% · séance 70% (100/151) · gap 21% · délai 0.2min · rebond 59% (60/100) (MFE +1.3%)
   - −1.5% : fill 30min 47% · séance 64% (87/151) · gap 15% · délai 0.4min · rebond 67% (57/87) (MFE +1.39%)
   - −2.0% : fill 30min 43% · séance 60% (79/151) · gap 11% · délai 0.7min · rebond 73% (55/79) (MFE +1.79%)
   - −3.0% : fill 30min 33% · séance 49% (62/151) · gap 6% · délai 1.8min · rebond 79% (44/62) (MFE +1.97%)
   - −4.0% : fill 30min 24% · séance 41% (51/151) · gap 4% · délai 16.5min · rebond 77% (40/51) (MFE +2.28%)
   - −5.0% : fill 30min 15% · séance 34% (40/151) · gap 1% · délai 39.2min · rebond 82% (31/40) (MFE +2.54%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.72% (p90 −3.6%) → stop au-delà de −2.41% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.93% (p90 −3.68%) → stop au-delà de −2.63% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.26% (p90 −5.02%) → stop au-delà de −3.41% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=785 jambes) : jambe baissière méd −1.23% (p90 −3.47%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (53 séances) :
      · −1.0% : fill 98% (52/53) · rebond 52% (28/52)
      · −2.0% : fill 94% (45/53) · rebond 68% (28/45)
      · −3.0% : fill 86% (39/53) · rebond 79% (27/39)
      · −4.0% : fill 74% (34/53) · rebond 77% (27/34)
      · −5.0% : fill 61% (26/53) · rebond 82% (20/26)
   - **flat** (17 séances) :
      · −1.0% : fill 88% (14/17) · rebond 47% (7/14)
      · −2.0% : fill 79% (12/17) · rebond 78% (9/12)
      · −3.0% : fill 78% (11/17) · rebond 83% (8/11)
      · −4.0% : fill 57% (7/17) · rebond 68% (5/7)
      · −5.0% : fill 57% (7/17) · rebond 89% (6/7)
   - **gap-up** (81 séances) :
      · −1.0% : fill 48% (34/81) · rebond 73% (25/34)
      · −2.0% : fill 35% (22/81) · rebond 79% (18/22)
      · −3.0% : fill 21% (12/81) · rebond 77% (9/12)
      · −4.0% : fill 17% (10/81) · rebond 82% (8/10)
      · −5.0% : fill 12% (7/81) · rebond 78% (5/7)
- **P(clôture VERTE) selon le drive 15min** (n=152) : 32% en base · 50% si les 15 1res min sont vertes (68 cas) · 23% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=152) : COUDE à **1:19** → P(séance verte=clôture>ouverture) 70% si début vert vs 10% si rouge (base 32% · écart 59 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=66) : tient le vert **70%** · continue >prix actuel 42% ; creux résiduel méd -1.81% (q20 -3.75%) → **SL/trailing à −3.75%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.45% / q75 +3.02% → **scale +1.45% / runner +3.02%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **10%** (continue à baisser 51%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.37%** (au-delà de la MAE q10 -5.37%), cible rebond +1.52% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=152) : retour [-5.39% .. +2.69%] · haut q95 +4.13% · bas q05 -5.74%
   - 60min (n=152) : retour [-5.66% .. +2.73%] · haut q95 +4.41% · bas q05 -6.06%
   - 2h (n=152) : retour [-7.04% .. +3.68%] · haut q95 +5.06% · bas q05 -7.58%
   - 4h (n=152) : retour [-6.95% .. +3.87%] · haut q95 +5.37% · bas q05 -8.63%
   - 6h (n=152) : retour [-8.15% .. +4.28%] · haut q95 +6.36% · bas q05 -9.36%
   - session (n=152) : retour [-7.6% .. +3.95%] · haut q95 +6.48% · bas q05 -9.68%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.51%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 42.6  _(momentum baissier)_
- **ADX** : 23.5  _(pas de tendance nette)_
- **MACD** : hist 16926.334  _(pas de croisement recent)_
- **BB** : %B 0.62 · largeur 38.9%
- **ATR** : 66660.0 (71.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.013  _(neutre)_
- **Vol ratio** : 0.65  _(volume normal)_
- **Choppiness** : 39.2  _(transition)_
- **MA** : MA20 746257.63 · MA50 877615.96 · MA200 923979.54  _(prix > MA20)_
- **Dist MA** : MA20 +4.8% · MA50 -10.9% · MA200 -15.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (82814 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
