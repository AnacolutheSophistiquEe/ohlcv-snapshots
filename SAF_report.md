# SAF

**Generated** : 2026-08-20T19:50:58.508358+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €343.60  

> 🟡 **WAIT-FOR-DIP** — spot +8.8 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €343.60 (+8.8% vs entrée) · entrée €315.82 · stop €308.30 · T1 €321.96 · R/R 0.82  
> ↳ P(T1 av. stop) 53 % · EV/risk 0.017 · ¼-Kelly 0.003 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €314.59–€317.05 (mid €315.82)
- Spot actuel : €343.60 (+8.8% au-dessus de la zone — repli à attendre)
- Stop : €308.30 (stop swing_plan-based (-10.27%))
- Targets : T1 €321.96 · R/R 0.82 | T2 €328.10 · R/R 1.63 | T3 €334.25 · R/R 2.45
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €308.30


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.62 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (10.27 %)** : le gap seul le franchit 0.0 % des séances ; quand il le franchit, l'exécution est **0.0 points plus bas** → perte réelle **— %** _(et non 10.27 %)_
- Chocs d'ouverture : p05 -1.405 % | p01 -2.356 % | pire -9.986 % _(sur 1279 séances)_
- **P(stop avant cible)** _(source : daily, 1280 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0124** [0.0027 ; 0.0379] _(largeur 3.5 pt, n_eff 173.1)_
   - swing : **0.1511** [0.1163 ; 0.1917] _(largeur 7.5 pt, n_eff 345.8)_
   - deep : **0.2543** [0.2106 ; 0.3021] _(largeur 9.2 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-3.19 %** | CVaR **-4.0 %** | vol 2.05 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 1.31 % contre 2.53 % aujourd'hui, rapport 0.52)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.63 % vs -6.07 % si l'on extrapolait par √5 _(rapport 0.927 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3705** (β de hausse 1.3363, asymétrie 1.0256) vs FCHI — 617 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.017 | EV/share : €0.129 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 53 % | T2 30 % | T3 18 %
- Kelly (position) : f* 0.012 | ¼-Kelly 0.003 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 10.9 | side 84.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 344.0 (= 1 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=4, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→55% · +2.0%→30% · +3.0%→12% · +5.0%→1% · +8.0%→1%
- Range intraday médian 2.54% (p90 4.15%) · excursion haute méd. +1.2% / basse méd. −0.88%
- Profil de vol intra : ouverture 1.563% vs midi 0.572% vs clôture 0.702% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 41% · recovery-V 20%)_
- **Régime intraday** : **chop** _(efficiency 0.106 ; mean-reverting — autocorr -0.048)_ ; drift intra méd. -0.101% ; recovery-V 21%
- **σ réalisé intraday** 1.636% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 74% / bas 55% / whipsaw 31%
- POC intraday (dernière séance, temps-au-prix) : 357.595 (VA 353.915–358.285 ; dernier close 350.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 29% · rebond 49% · **stop −2.03%** sous le fill (sous le bruit) · cible +0.91% · R/R 0.45 (high win-rate)
- Gaps overnight (n=159) : méd. 0.14% · baisse 45% (gap-down >1% 7% · >2% 1%)
- Excursion ouverture 5min (n=160) : bas méd −0.42% (p90 −1.6%) · haut méd +0.18% · range méd 0.91%
- Excursion ouverture 15min (n=160) : bas méd −0.5% (p90 −1.91%) · haut méd +0.25% · range méd 1.12%
- Excursion ouverture 30min (n=160) : bas méd −0.53% (p90 −1.92%) · haut méd +0.54% · range méd 1.28%
- Excursion ouverture 60min (n=160) : bas méd −0.65% (p90 −1.93%) · haut méd +0.57% · range méd 1.54%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 350.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 52% · séance 67% (112/159) · gap 18% · délai 0.2min · rebond 39% (43/112) (MFE +0.78%)
   - −1.0% : fill 30min 36% · séance 50% (86/159) · gap 7% · délai 1.3min · rebond 40% (32/86) (MFE +0.61%)
   - −1.5% : fill 30min 23% · séance 39% (71/159) · gap 3% · délai 16.5min · rebond 41% (26/71) (MFE +0.88%)
   - −2.0% : fill 30min 11% · séance 29% (53/159) · gap 1% · délai 49.8min · rebond 49% (24/53) (MFE +0.91%)
   - −3.0% : fill 30min 2% · séance 14% (29/159) · gap 0% · délai 87.1min · rebond 54% (17/29) (MFE +1.2%)
   - −4.0% : fill 30min 2% · séance 6% (13/159) · gap 0% · délai 126.9min · rebond 62% (7/13) (MFE +1.25%)
   - −5.0% : fill 30min 0% · séance 1% (3/159) · gap 0% · délai 360.2min · rebond 31% (1/3) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.15% (p90 −0.78%) → stop au-delà de −0.68% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.12% (p90 −0.78%) → stop au-delà de −0.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=211 jambes) : jambe baissière méd −1.03% (p90 −2.33%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 80% (46/56) · rebond 38% (17/46)
      · −2.0% : fill 59% (33/56) · rebond 43% (15/33)
      · −3.0% : fill 26% (17/56) · rebond 50% (9/17)
      · −4.0% : fill 13% (9/56) · rebond 69% (5/9)
      · −5.0% : fill 2% (2/56) · rebond 0% (0/2)
   - **flat** (40 séances) :
      · −1.0% : fill 41% (19/40) · rebond 56% (10/19)
      · −2.0% : fill 19% (9/40) · rebond 75% (5/9)
      · −3.0% : fill 10% (5/40) · rebond 85% (4/5)
      · −4.0% : fill 1% (1/40) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/40) · rebond 0% (0/0)
   - **gap-up** (63 séances) :
      · −1.0% : fill 32% (21/63) · rebond 31% (5/21)
      · −2.0% : fill 12% (11/63) · rebond 43% (4/11)
      · −3.0% : fill 8% (7/63) · rebond 36% (4/7)
      · −4.0% : fill 3% (3/63) · rebond 30% (1/3)
      · −5.0% : fill 1% (1/63) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 65% si les 15 1res min sont vertes (76 cas) · 31% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **44min** → P(séance verte=clôture>ouverture) 73% si début vert vs 24% si rouge (base 49% · écart 49 pts) ; prédictivité sature ensuite (plafond brut 292min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **73%** · continue >prix actuel 54% ; creux résiduel méd -0.73% (q20 -1.51%) → **SL/trailing à −1.51%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.75% / q75 +1.53% → **scale +0.75% / runner +1.53%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **24%** (continue à baisser 49%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.38%** (au-delà de la MAE q10 -2.38%), cible rebond +1.03% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.58% .. +1.57%] · haut q95 +1.97% · bas q05 -2.19%
   - 60min (n=160) : retour [-1.65% .. +2.13%] · haut q95 +2.25% · bas q05 -2.49%
   - 2h (n=160) : retour [-2.16% .. +2.16%] · haut q95 +2.57% · bas q05 -2.94%
   - 4h (n=160) : retour [-1.93% .. +2.19%] · haut q95 +2.78% · bas q05 -3.03%
   - 6h (n=160) : retour [-2.16% .. +2.42%] · haut q95 +3.12% · bas q05 -3.16%
   - session (n=160) : retour [-2.81% .. +2.56%] · haut q95 +3.41% · bas q05 -4.0%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.69%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 52.8  _(neutre)_
- **ADX** : 16.4  _(pas de tendance nette)_
- **MACD** : hist -1.796  _(bearish_recent)_
- **BB** : %B 0.37 · largeur 13.9%
- **ATR** : 7.51 (47.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.092  _(distribution)_
- **Vol ratio** : 0.8  _(volume normal)_
- **Choppiness** : 56.8  _(transition)_
- **MA** : MA20 350.0 · MA50 339.65 · MA200 308.92  _(prix < MA20)_
- **Dist MA** : MA20 -1.8% · MA50 +1.2% · MA200 +11.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (404207 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
