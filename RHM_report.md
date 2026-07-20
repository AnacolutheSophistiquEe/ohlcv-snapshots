# RHM

**Generated** : 2026-07-20T21:35:48.496053+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €990.30  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €990.30 (+1.6% vs entrée) · entrée €974.92 · stop €955.43 · T1 €1004.12 · R/R 1.5  
> ↳ P(T1 av. stop) 23 % _(réel 5 s)_ · EV/risk -0.119 _(réel 5 s)_ (GBM 0.047) · ¼-Kelly 0.008 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €969.09–€980.76 (mid €974.92)
- Spot actuel : €990.30 (+1.6% au-dessus de la zone — repli à attendre)
- Stop : €955.43 (stop swing_plan-based (-6.65%))
- Targets : T1 €1004.12 · R/R 1.5 | T2 €1033.32 · R/R 3.0 | T3 €1062.52 · R/R 4.49
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €955.43


## Edge, scénarios & sizing

- EV/risk : 0.047 | EV/share : €0.913 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 4 % | T3 4 %
- Kelly (position) : f* 0.032 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 20.8 | bear 5.0 | side 74.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.551% → cible +2.995% / stop −2.0%, p_fill 60%, n_eff≈23.1) : P(cible|rempli) **23%** · **EV/risk -0.119** (×p_fill ; si rempli -0.40% du capital)
  - **swing** (entrée dip −3.416% → cible +6.697% / stop −3.348%, p_fill 46%, n_eff≈15.0) : P(cible|rempli) **7%** · **EV/risk -0.219** (×p_fill ; si rempli -1.61% du capital)
  - **deep** (entrée dip −5.275% → cible +9.47% / stop −4.735%, p_fill 40%, n_eff≈15.7) : P(cible|rempli) **5%** · **EV/risk -0.274** (×p_fill ; si rempli -3.22% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→64% · +2.0%→49% · +3.0%→31% · +5.0%→4% · +8.0%→0%
- Range intraday médian 4.16% (p90 6.86%) · excursion haute méd. +1.98% / basse méd. −1.72%
- Profil de vol intra : ouverture 2.567% vs midi 0.848% vs clôture 1.085% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 57% · recovery-V 38%)_
- **Régime intraday** : **chop** _(efficiency 0.111 ; neutre — autocorr -0.004)_ ; drift intra méd. -0.357% ; recovery-V 42%
- **σ réalisé intraday** 2.872% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 71% / whipsaw 40%
- POC intraday (dernière séance, temps-au-prix) : 985.4588 (VA 975.0788–986.7562 ; dernier close 987.6)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 24% · rebond 61% · **stop −3.12%** sous le fill (sous le bruit) · cible +1.45% · R/R 0.46 (high win-rate)
- Gaps overnight (n=159) : méd. 0.01% · baisse 46% (gap-down >1% 13% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.83% (p90 −1.76%) · haut méd +0.49% · range méd 1.47%
- Excursion ouverture 15min (n=160) : bas méd −0.98% (p90 −2.02%) · haut méd +0.67% · range méd 1.98%
- Excursion ouverture 30min (n=160) : bas méd −1.07% (p90 −2.75%) · haut méd +0.84% · range méd 2.23%
- Excursion ouverture 60min (n=160) : bas méd −1.12% (p90 −3.09%) · haut méd +1.01% · range méd 2.39%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 987.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 79% (122/159) · gap 31% · délai 0.2min · rebond 56% (63/122) (MFE +1.21%)
   - −1.0% : fill 30min 52% · séance 74% (111/159) · gap 13% · délai 4.2min · rebond 61% (64/111) (MFE +1.39%)
   - −1.5% : fill 30min 34% · séance 59% (83/159) · gap 7% · délai 17.7min · rebond 51% (42/83) (MFE +1.14%)
   - −2.0% : fill 30min 24% · séance 48% (72/159) · gap 6% · délai 29.9min · rebond 61% (42/72) (MFE +1.31%)
   - −3.0% : fill 30min 11% · séance 33% (48/159) · gap 3% · délai 118.8min · rebond 60% (30/48) (MFE +1.31%)
   - −4.0% : fill 30min 5% · séance 24% (29/159) · gap 2% · délai 152.5min · rebond 61% (17/29) (MFE +1.45%)
   - −5.0% : fill 30min 2% · séance 12% (16/159) · gap 1% · délai 206.9min · rebond 48% (8/16) (MFE +0.74%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.67% (p90 −1.74%) → stop au-delà de −1.28% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.7% (p90 −1.77%) → stop au-delà de −1.48% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.33% (p90 −1.77%) → stop au-delà de −1.59% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=462 jambes) : jambe baissière méd −1.09% (p90 −2.61%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (53 séances) :
      · −1.0% : fill 94% (51/53) · rebond 62% (28/51)
      · −2.0% : fill 77% (40/53) · rebond 63% (25/40)
      · −3.0% : fill 50% (28/53) · rebond 59% (18/28)
      · −4.0% : fill 36% (16/53) · rebond 71% (11/16)
      · −5.0% : fill 17% (9/53) · rebond 77% (7/9)
   - **flat** (50 séances) :
      · −1.0% : fill 80% (37/50) · rebond 69% (24/37)
      · −2.0% : fill 34% (18/50) · rebond 71% (10/18)
      · −3.0% : fill 23% (11/50) · rebond 56% (6/11)
      · −4.0% : fill 21% (9/50) · rebond 38% (3/9)
      · −5.0% : fill 13% (6/50) · rebond 22% (1/6)
   - **gap-up** (56 séances) :
      · −1.0% : fill 48% (23/56) · rebond 49% (12/23)
      · −2.0% : fill 29% (14/56) · rebond 46% (7/14)
      · −3.0% : fill 23% (9/56) · rebond 66% (6/9)
      · −4.0% : fill 12% (4/56) · rebond 61% (3/4)
      · −5.0% : fill 5% (1/56) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 67% si les 15 1res min sont vertes (84 cas) · 31% si rouges (76 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 75% si début vert vs 24% si rouge (base 49% · écart 50 pts) ; prédictivité sature ensuite (plafond brut 295min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **75%** · continue >prix actuel 49% ; creux résiduel méd -1.25% (q20 -2.46%) → **SL/trailing à −2.46%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.25% / q75 +1.88% → **scale +1.25% / runner +1.88%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **24%** (continue à baisser 55%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.98%** (au-delà de la MAE q10 -4.98%), cible rebond +1.14% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.66% .. +3.1%] · haut q95 +3.79% · bas q05 -3.22%
   - 60min (n=160) : retour [-3.51% .. +3.09%] · haut q95 +4.01% · bas q05 -4.07%
   - 2h (n=160) : retour [-3.62% .. +2.82%] · haut q95 +4.11% · bas q05 -4.77%
   - 4h (n=160) : retour [-3.87% .. +2.99%] · haut q95 +4.51% · bas q05 -5.1%
   - 6h (n=160) : retour [-4.73% .. +3.3%] · haut q95 +4.53% · bas q05 -5.75%
   - session (n=160) : retour [-6.21% .. +4.19%] · haut q95 +4.74% · bas q05 -6.77%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.29%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 50.0  _(neutre)_
- **ADX** : 28.4  _(tendance etablie)_
- **MACD** : hist 0.001  _(bullish_recent)_
- **BB** : %B 0.39 · largeur 26.8%
- **ATR** : 49.1 (13.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.051  _(distribution)_
- **Vol ratio** : 0.52  _(volume atone)_
- **Choppiness** : 45.0  _(transition)_
- **MA** : MA20 1020.54 · MA50 1127.0 · MA200 1495.68  _(prix < MA20)_
- **Dist MA** : MA20 -3.0% · MA50 -12.1% · MA200 -33.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90119 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
