# SRT3

**Generated** : 2026-08-11T00:03:15.647332+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · €238.40  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot €238.40 (+1.6% vs entrée) · entrée €234.59 · stop €227.55 · T1 €244.46 · R/R 1.4  
> ↳ P(T1 av. stop) 21 % _(réel 5 s)_ · EV/risk 0.089 _(réel 5 s)_ (GBM 0.025) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.080 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €233.89–€235.29 (mid €234.59)
- Spot actuel : €238.40 (+1.6% au-dessus de la zone — repli à attendre)
- Stop : €227.55 (stop swing_plan-based (-8.5%))
- Targets : T1 €244.46 · R/R 1.4 | T2 €244.77 · R/R 1.45 | T3 €245.09 · R/R 1.49
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €227.55


## Edge, scénarios & sizing

- EV/risk : 0.025 | EV/share : €0.175 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 11 % | T2 10 % | T3 10 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.0 | bear 79.0 | side 8.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 238.0 (= 1 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.598% → cible +4.205% / stop −3.0%, p_fill 47%, n_eff≈20.9) : P(cible|rempli) **21%** · **EV/risk +0.089** (×p_fill ; si rempli +0.57% du capital)
  - **swing** (entrée dip −3.511% → cible +3.337% / stop −5.17%, p_fill 30%, n_eff≈11.1) : P(cible|rempli) **77%** · **EV/risk +0.080** (×p_fill ; si rempli +1.36% du capital)
  - **deep** (entrée dip −5.437% → cible +4.719% / stop −7.913%, p_fill 30%, n_eff≈10.4) : P(cible|rempli) **55%** · **EV/risk +0.010** (×p_fill ; si rempli +0.26% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→78% · +2.0%→49% · +3.0%→25% · +5.0%→8% · +8.0%→0%
- Range intraday médian 3.61% (p90 7.06%) · excursion haute méd. +1.96% / basse méd. −1.55%
- Profil de vol intra : ouverture 2.137% vs midi 0.936% vs clôture 1.036% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 10% · trend ↑0%/↓0% ; spike-down 51% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.104 ; neutre — autocorr -0.011)_ ; drift intra méd. 0.001% ; recovery-V 27%
- **σ réalisé intraday** 2.752% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 73% / bas 70% / whipsaw 45%
- POC intraday (dernière séance, temps-au-prix) : 233.2719 (VA 232.7731–234.6019 ; dernier close 232.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 57% · rebond 73% · **stop −2.45%** sous le fill (sous le bruit) · cible +1.68% · R/R 0.69 (high win-rate)
- Gaps overnight (n=159) : méd. 0.04% · baisse 49% (gap-down >1% 14% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.34% (p90 −1.98%) · haut méd +0.58% · range méd 1.24%
- Excursion ouverture 15min (n=160) : bas méd −0.51% (p90 −2.05%) · haut méd +0.67% · range méd 1.5%
- Excursion ouverture 30min (n=160) : bas méd −0.55% (p90 −2.52%) · haut méd +0.86% · range méd 1.74%
- Excursion ouverture 60min (n=160) : bas méd −0.65% (p90 −2.8%) · haut méd +0.95% · range méd 1.86%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 232.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 54% · séance 78% (125/159) · gap 27% · délai 0.3min · rebond 57% (66/125) (MFE +1.2%)
   - −1.0% : fill 30min 42% · séance 66% (105/159) · gap 14% · délai 2.1min · rebond 60% (61/105) (MFE +1.35%)
   - −1.5% : fill 30min 35% · séance 57% (94/159) · gap 7% · délai 4.7min · rebond 73% (61/94) (MFE +1.68%)
   - −2.0% : fill 30min 21% · séance 41% (73/159) · gap 4% · délai 24.1min · rebond 65% (45/73) (MFE +1.67%)
   - −3.0% : fill 30min 7% · séance 19% (40/159) · gap 1% · délai 138.5min · rebond 57% (23/40) (MFE +1.67%)
   - −4.0% : fill 30min 4% · séance 11% (21/159) · gap 0% · délai 49.4min · rebond 76% (16/21) (MFE +2.62%)
   - −5.0% : fill 30min 1% · séance 8% (12/159) · gap 0% · délai 94.0min · rebond 65% (9/12) (MFE +2.48%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.44% (p90 −2.23%) → stop au-delà de −1.25% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.18% (p90 −2.42%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.65% (p90 −2.8%) → stop au-delà de −1.9% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=423 jambes) : jambe baissière méd −1.05% (p90 −2.6%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (72 séances) :
      · −1.0% : fill 82% (59/72) · rebond 68% (38/59)
      · −2.0% : fill 52% (42/72) · rebond 64% (27/42)
      · −3.0% : fill 31% (28/72) · rebond 48% (15/28)
      · −4.0% : fill 14% (15/72) · rebond 71% (11/15)
      · −5.0% : fill 8% (7/72) · rebond 92% (6/7)
   - **flat** (33 séances) :
      · −1.0% : fill 62% (20/33) · rebond 56% (10/20)
      · −2.0% : fill 46% (15/33) · rebond 55% (7/15)
      · −3.0% : fill 18% (6/33) · rebond 66% (4/6)
      · −4.0% : fill 14% (4/33) · rebond 70% (3/4)
      · −5.0% : fill 14% (4/33) · rebond 24% (2/4)
   - **gap-up** (54 séances) :
      · −1.0% : fill 52% (26/54) · rebond 50% (13/26)
      · −2.0% : fill 26% (16/54) · rebond 77% (11/16)
      · −3.0% : fill 7% (6/54) · rebond 78% (4/6)
      · −4.0% : fill 5% (2/54) · rebond 100% (2/2)
      · −5.0% : fill 4% (1/54) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 57% si les 15 1res min sont vertes (90 cas) · 40% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **3:25** → P(séance verte=clôture>ouverture) 70% si début vert vs 24% si rouge (base 50% · écart 46 pts) ; prédictivité sature ensuite (plafond brut 293min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **70%** · continue >prix actuel 47% ; creux résiduel méd -1.14% (q20 -1.94%) → **SL/trailing à −1.94%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.06% / q75 +2.21% → **scale +1.06% / runner +2.21%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **24%** (continue à baisser 55%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.35%** (au-delà de la MAE q10 -3.35%), cible rebond +1.39% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.01% .. +2.06%] · haut q95 +2.64% · bas q05 -3.53%
   - 60min (n=160) : retour [-3.17% .. +2.33%] · haut q95 +2.72% · bas q05 -3.84%
   - 2h (n=160) : retour [-2.24% .. +2.56%] · haut q95 +2.99% · bas q05 -3.87%
   - 4h (n=160) : retour [-2.6% .. +2.34%] · haut q95 +3.32% · bas q05 -4.22%
   - 6h (n=160) : retour [-2.68% .. +3.15%] · haut q95 +3.81% · bas q05 -5.73%
   - session (n=160) : retour [-3.72% .. +4.18%] · haut q95 +5.75% · bas q05 -5.73%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.32%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 50.8  _(neutre)_
- **ADX** : 17.5  _(pas de tendance nette)_
- **MACD** : hist 1.069  _(bullish_recent)_
- **BB** : %B 0.66 · largeur 19.7%
- **ATR** : 11.89 (96.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.079  _(distribution)_
- **Vol ratio** : 0.16  _(volume atone)_
- **Choppiness** : 60.2  _(transition)_
- **MA** : MA20 231.11 · MA50 230.58 · MA200 231.96  _(prix > MA20)_
- **Dist MA** : MA20 +3.2% · MA50 +3.4% · MA200 +2.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93549 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
