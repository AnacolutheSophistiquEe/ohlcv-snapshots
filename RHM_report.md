# RHM

**Generated** : 2026-07-15T21:36:11.140855+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €976.10  

> 🟡 **WAIT-FOR-DIP** — spot +1.2 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €976.10 (+1.2% vs entrée) · entrée €964.27 · stop €944.99 · T1 €993.15 · R/R 1.5  
> ↳ P(T1 av. stop) 29 % _(réel 5 s)_ · EV/risk 0.025 _(réel 5 s)_ (GBM 0.004) · ¼-Kelly 0.004 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €958.50–€970.05 (mid €964.27)
- Spot actuel : €976.10 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : €944.99 (stop swing_plan-based (-5.92%))
- Targets : T1 €993.15 · R/R 1.5 | T2 €1022.02 · R/R 3.0 | T3 €1050.90 · R/R 4.49
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €944.99


## Edge, scénarios & sizing

- EV/risk : 0.004 | EV/share : €0.069 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 30 % | T2 4 % | T3 4 %
- Kelly (position) : f* 0.017 | ¼-Kelly 0.004 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 22.4 | bear 8.3 | side 69.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.214% → cible +2.994% / stop −2.0%, p_fill 74%, n_eff≈27.7) : P(cible|rempli) **29%** · **EV/risk +0.025** (×p_fill ; si rempli +0.07% du capital)
  - **swing** (entrée dip −2.661% → cible +6.696% / stop −3.348%, p_fill 35%, n_eff≈14.9) : P(cible|rempli) **13%** · **EV/risk -0.206** (×p_fill ; si rempli -1.96% du capital)
  - **deep** (entrée dip −4.121% → cible +9.469% / stop −4.734%, p_fill 47%, n_eff≈18.2) : P(cible|rempli) **14%** · **EV/risk -0.230** (×p_fill ; si rempli -2.32% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→72% · +1.0%→61% · +2.0%→48% · +3.0%→30% · +5.0%→4% · +8.0%→0%
- Range intraday médian 4.16% (p90 6.65%) · excursion haute méd. +1.85% / basse méd. −1.72%
- Profil de vol intra : ouverture 2.577% vs midi 0.902% vs clôture 1.013% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 57% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.118 ; neutre — autocorr 0.012)_ ; drift intra méd. -0.645% ; recovery-V 36%
- **σ réalisé intraday** 2.83% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 74% / whipsaw 35%
- POC intraday (dernière séance, temps-au-prix) : 994.9175 (VA 989.9125–1004.9275 ; dernier close 990.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 32% · rebond 61% · **stop −3.26%** sous le fill (sous le bruit) · cible +1.31% · R/R 0.4 (high win-rate)
- Gaps overnight (n=159) : méd. 0.09% · baisse 41% (gap-down >1% 14% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.77% (p90 −1.53%) · haut méd +0.5% · range méd 1.38%
- Excursion ouverture 15min (n=160) : bas méd −1.0% (p90 −1.97%) · haut méd +0.67% · range méd 1.97%
- Excursion ouverture 30min (n=160) : bas méd −1.08% (p90 −2.59%) · haut méd +0.87% · range méd 2.17%
- Excursion ouverture 60min (n=160) : bas méd −1.1% (p90 −2.77%) · haut méd +1.0% · range méd 2.32%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 990.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 77% (120/159) · gap 28% · délai 0.3min · rebond 56% (63/120) (MFE +1.19%)
   - −1.0% : fill 30min 49% · séance 72% (107/159) · gap 14% · délai 5.6min · rebond 59% (61/107) (MFE +1.41%)
   - −1.5% : fill 30min 31% · séance 56% (80/159) · gap 8% · délai 22.3min · rebond 48% (40/80) (MFE +0.9%)
   - −2.0% : fill 30min 22% · séance 47% (69/159) · gap 6% · délai 30.7min · rebond 60% (40/69) (MFE +1.27%)
   - −3.0% : fill 30min 10% · séance 32% (46/159) · gap 3% · délai 118.9min · rebond 61% (29/46) (MFE +1.31%)
   - −4.0% : fill 30min 4% · séance 22% (27/159) · gap 2% · délai 152.5min · rebond 54% (15/27) (MFE +1.23%)
   - −5.0% : fill 30min 2% · séance 13% (16/159) · gap 2% · délai 206.9min · rebond 48% (8/16) (MFE +0.74%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.59% (p90 −1.53%) → stop au-delà de −1.22% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −1.68%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.26% (p90 −1.64%) → stop au-delà de −1.37% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=465 jambes) : jambe baissière méd −1.1% (p90 −2.63%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 93% (47/49) · rebond 59% (25/47)
      · −2.0% : fill 78% (37/49) · rebond 62% (23/37)
      · −3.0% : fill 50% (26/49) · rebond 61% (17/26)
      · −4.0% : fill 33% (14/49) · rebond 61% (9/14)
      · −5.0% : fill 21% (9/49) · rebond 77% (7/9)
   - **flat** (50 séances) :
      · −1.0% : fill 79% (37/50) · rebond 67% (24/37)
      · −2.0% : fill 36% (18/50) · rebond 71% (10/18)
      · −3.0% : fill 24% (11/50) · rebond 56% (6/11)
      · −4.0% : fill 22% (9/50) · rebond 38% (3/9)
      · −5.0% : fill 14% (6/50) · rebond 22% (1/6)
   - **gap-up** (60 séances) :
      · −1.0% : fill 48% (23/60) · rebond 49% (12/23)
      · −2.0% : fill 29% (14/60) · rebond 46% (7/14)
      · −3.0% : fill 22% (9/60) · rebond 66% (6/9)
      · −4.0% : fill 12% (4/60) · rebond 61% (3/4)
      · −5.0% : fill 5% (1/60) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 67% si les 15 1res min sont vertes (83 cas) · 30% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 79% si début vert vs 22% si rouge (base 48% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 295min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **79%** · continue >prix actuel 48% ; creux résiduel méd -1.37% (q20 -2.38%) → **SL/trailing à −2.38%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.19% / q75 +1.87% → **scale +1.19% / runner +1.87%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **22%** (continue à baisser 57%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.99%** (au-delà de la MAE q10 -4.99%), cible rebond +1.07% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.66% .. +3.13%] · haut q95 +3.83% · bas q05 -2.94%
   - 60min (n=160) : retour [-3.63% .. +3.1%] · haut q95 +4.04% · bas q05 -4.23%
   - 2h (n=160) : retour [-3.7% .. +2.86%] · haut q95 +4.15% · bas q05 -4.99%
   - 4h (n=160) : retour [-4.07% .. +3.02%] · haut q95 +4.54% · bas q05 -5.17%
   - 6h (n=160) : retour [-4.78% .. +3.4%] · haut q95 +4.54% · bas q05 -5.79%
   - session (n=160) : retour [-6.42% .. +4.23%] · haut q95 +4.76% · bas q05 -6.89%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.28%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 53.5  _(neutre)_
- **ADX** : 26.0  _(tendance etablie)_
- **MACD** : hist -2.889  _(bearish_recent)_
- **BB** : %B 0.29 · largeur 33.8%
- **ATR** : 50.03 (16.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.058  _(distribution)_
- **Vol ratio** : 0.57  _(volume atone)_
- **Choppiness** : 44.4  _(transition)_
- **MA** : MA20 1052.15 · MA50 1142.4 · MA200 1510.32  _(prix < MA20)_
- **Dist MA** : MA20 -7.2% · MA50 -14.6% · MA200 -35.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89997 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
