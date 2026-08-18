# RHM

**Generated** : 2026-08-18T00:01:56.340583+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €1216.80  

> 🟡 **WAIT-FOR-DIP** — spot +1.7 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €1216.80 (+1.7% vs entrée) · entrée €1196.25 · stop €1172.33 · T1 €1209.61 · R/R 0.56  
> ↳ P(T1 av. stop) 49 % _(réel 5 s)_ · EV/risk 0.014 _(réel 5 s)_ (GBM 0.14) · ¼-Kelly 0.054 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €1193.58–€1198.92 (mid €1196.25)
- Spot actuel : €1216.80 (+1.7% au-dessus de la zone — repli à attendre)
- Stop : €1172.33 (stop swing_plan-based (-8.5%))
- Targets : T1 €1209.61 · R/R 0.56 | T2 €1222.98 · R/R 1.12 | T3 €1236.34 · R/R 1.68
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €1172.33


## Edge, scénarios & sizing

- EV/risk : 0.14 | EV/share : €3.358 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 69 % | T2 45 % | T3 28 %
- Kelly (position) : f* 0.215 | ¼-Kelly 0.054 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.6 | bear 5.4 | side 81.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.694% → cible +1.117% / stop −2.0%, p_fill 42%, n_eff≈18.1) : P(cible|rempli) **49%** · **EV/risk +0.014** (×p_fill ; si rempli +0.07% du capital)
  - **swing** (entrée dip −3.713% → cible +2.498% / stop −4.971%, p_fill 25%, n_eff≈12.3) : P(cible|rempli) **65%** · **EV/risk -0.011** (×p_fill ; si rempli -0.22% du capital)
  - **deep** (entrée dip −5.74% → cible +3.533% / stop −7.617%, p_fill 21%, n_eff≈14.1) : P(cible|rempli) **21%** · **EV/risk -0.140** (×p_fill ; si rempli -4.98% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→74% · +2.0%→52% · +3.0%→34% · +5.0%→5% · +8.0%→1%
- Range intraday médian 4.17% (p90 6.98%) · excursion haute méd. +2.23% / basse méd. −1.51%
- Profil de vol intra : ouverture 2.667% vs midi 0.933% vs clôture 1.107% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 10% · trend ↑0%/↓0% ; spike-down 51% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.086 ; neutre — autocorr -0.003)_ ; drift intra méd. 0.133% ; recovery-V 33%
- **σ réalisé intraday** 2.88% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 74% / bas 60% / whipsaw 37%
- POC intraday (dernière séance, temps-au-prix) : 1200.275 (VA 1195.925–1207.525 ; dernier close 1201.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 40% · rebond 67% · **stop −3.18%** sous le fill (sous le bruit) · cible +1.57% · R/R 0.49 (high win-rate)
- Gaps overnight (n=159) : méd. 0.24% · baisse 34% (gap-down >1% 10% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.67% (p90 −1.53%) · haut méd +0.59% · range méd 1.37%
- Excursion ouverture 15min (n=160) : bas méd −0.87% (p90 −1.97%) · haut méd +0.73% · range méd 1.8%
- Excursion ouverture 30min (n=160) : bas méd −0.91% (p90 −2.26%) · haut méd +0.99% · range méd 2.04%
- Excursion ouverture 60min (n=160) : bas méd −0.92% (p90 −2.58%) · haut méd +1.08% · range méd 2.32%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1201.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 70% (117/159) · gap 23% · délai 0.4min · rebond 56% (63/117) (MFE +1.28%)
   - −1.0% : fill 30min 39% · séance 63% (106/159) · gap 10% · délai 6.2min · rebond 63% (62/106) (MFE +1.31%)
   - −1.5% : fill 30min 26% · séance 53% (85/159) · gap 6% · délai 28.4min · rebond 62% (48/85) (MFE +1.38%)
   - −2.0% : fill 30min 20% · séance 40% (72/159) · gap 6% · délai 30.4min · rebond 67% (45/72) (MFE +1.57%)
   - −3.0% : fill 30min 9% · séance 24% (45/159) · gap 4% · délai 116.9min · rebond 62% (27/45) (MFE +1.39%)
   - −4.0% : fill 30min 4% · séance 18% (28/159) · gap 1% · délai 245.4min · rebond 64% (16/28) (MFE +1.5%)
   - −5.0% : fill 30min 1% · séance 10% (16/159) · gap 1% · délai 293.4min · rebond 56% (8/16) (MFE +1.7%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.52% (p90 −1.62%) → stop au-delà de −1.14% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.44% (p90 −1.75%) → stop au-delà de −1.31% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.29% (p90 −1.78%) → stop au-delà de −1.27% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=519 jambes) : jambe baissière méd −1.07% (p90 −2.55%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (48 séances) :
      · −1.0% : fill 94% (46/48) · rebond 65% (27/46)
      · −2.0% : fill 80% (38/48) · rebond 66% (25/38)
      · −3.0% : fill 53% (26/48) · rebond 63% (16/26)
      · −4.0% : fill 41% (16/48) · rebond 75% (11/16)
      · −5.0% : fill 22% (9/48) · rebond 83% (7/9)
   - **flat** (47 séances) :
      · −1.0% : fill 64% (33/47) · rebond 72% (21/33)
      · −2.0% : fill 25% (17/47) · rebond 72% (10/17)
      · −3.0% : fill 17% (10/47) · rebond 55% (5/10)
      · −4.0% : fill 15% (8/47) · rebond 36% (2/8)
      · −5.0% : fill 10% (6/47) · rebond 22% (1/6)
   - **gap-up** (64 séances) :
      · −1.0% : fill 44% (27/64) · rebond 53% (14/27)
      · −2.0% : fill 26% (17/64) · rebond 67% (10/17)
      · −3.0% : fill 12% (9/64) · rebond 66% (6/9)
      · −4.0% : fill 7% (4/64) · rebond 61% (3/4)
      · −5.0% : fill 2% (1/64) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 62% si les 15 1res min sont vertes (81 cas) · 40% si rouges (79 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 69% si début vert vs 31% si rouge (base 51% · écart 39 pts) ; prédictivité sature ensuite (plafond brut 300min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **69%** · continue >prix actuel 42% ; creux résiduel méd -1.49% (q20 -3.08%) → **SL/trailing à −3.08%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.31% / q75 +2.03% → **scale +1.31% / runner +2.03%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **31%** (continue à baisser 46%) → **RÉDUIRE ~69%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.74%** (au-delà de la MAE q10 -4.74%), cible rebond +1.16% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.62% .. +3.31%] · haut q95 +3.81% · bas q05 -3.22%
   - 60min (n=160) : retour [-2.84% .. +3.23%] · haut q95 +4.51% · bas q05 -4.1%
   - 2h (n=160) : retour [-3.27% .. +3.1%] · haut q95 +4.51% · bas q05 -4.56%
   - 4h (n=160) : retour [-3.61% .. +3.37%] · haut q95 +4.87% · bas q05 -4.72%
   - 6h (n=160) : retour [-4.27% .. +3.43%] · haut q95 +5.0% · bas q05 -5.21%
   - session (n=160) : retour [-5.78% .. +4.19%] · haut q95 +5.11% · bas q05 -6.17%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.32%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 76.1  _(surachat)_
- **ADX** : 24.1  _(pas de tendance nette)_
- **MACD** : hist 9.703  _(pas de croisement recent)_
- **BB** : %B 0.82 · largeur 27.1%
- **ATR** : 58.24 (45.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.11  _(distribution)_
- **Vol ratio** : 0.48  _(volume atone)_
- **Choppiness** : 57.2  _(transition)_
- **MA** : MA20 1119.81 · MA50 1097.66 · MA200 1431.24  _(prix > MA20)_
- **Dist MA** : MA20 +8.7% · MA50 +10.9% · MA200 -15.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89467 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
