# SAF

**Generated** : 2026-08-12T00:05:46.951659+00:00  
**Santé technique** : 9/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €361.10  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot €361.10 (+0.3% vs entrée) · entrée €359.92 · stop €350.84 · T1 €366.24 · R/R 0.7  
> ↳ P(T1 av. stop) 62 % _(réel 5 s)_ · EV/risk 0.01 _(réel 5 s)_ (GBM 0.024) · ¼-Kelly 0.009 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 261 % hors [0,100] (R² max 0.75). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 17.7 < 20 (tendance pas encore confirmée) alors que Choppiness 37.5 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._
- 🔴 **Santé haussière vs sur-extension** — Santé technique 9/10 élevée alors que : RSI 78.4 > 70 (surachat) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €358.75–€361.10 (mid €359.92)
- Spot actuel : €361.10 (+0.3% au-dessus de la zone — repli à attendre)
- Stop : €350.84 (stop swing_plan-based (-2.84%))
- Targets : T1 €366.24 · R/R 0.7 | T2 €372.55 · R/R 1.39 | T3 €378.87 · R/R 2.09
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €350.84


## Edge, scénarios & sizing

- EV/risk : 0.024 | EV/share : €0.214 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 57 % | T2 37 % | T3 22 %
- Kelly (position) : f* 0.036 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 38.7 | side 56.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 361.0 (= 1 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.296% → cible +0.785% / stop −2.0%, p_fill 79%, n_eff≈33.2) : P(cible|rempli) **62%** · **EV/risk -0.036** (×p_fill ; si rempli -0.09% du capital)
  - **swing** (entrée dip −0.324% → cible +1.754% / stop −2.524%, p_fill 85%, n_eff≈34.0) : P(cible|rempli) **62%** · **EV/risk +0.010** (×p_fill ; si rempli +0.03% du capital)
  - **deep** (entrée dip −0.396% → cible +2.481% / stop −3.789%, p_fill 86%, n_eff≈32.5) : P(cible|rempli) **68%** · **EV/risk +0.080** (×p_fill ; si rempli +0.35% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→55% · +2.0%→31% · +3.0%→12% · +5.0%→1% · +8.0%→1%
- Range intraday médian 2.68% (p90 4.55%) · excursion haute méd. +1.2% / basse méd. −0.98%
- Profil de vol intra : ouverture 1.695% vs midi 0.627% vs clôture 0.731% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 39% · recovery-V 19%)_
- **Régime intraday** : **chop** _(efficiency 0.093 ; mean-reverting — autocorr -0.069)_ ; drift intra méd. 0.087% ; recovery-V 21%
- **σ réalisé intraday** 1.878% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 74% / bas 52% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 357.0512 (VA 356.3388–358.6187 ; dernier close 356.7)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 16% · rebond 54% · **stop −1.63%** sous le fill (sous le bruit) · cible +1.2% · R/R 0.74 (high win-rate)
- Gaps overnight (n=159) : méd. 0.12% · baisse 46% (gap-down >1% 8% · >2% 1%)
- Excursion ouverture 5min (n=160) : bas méd −0.44% (p90 −1.54%) · haut méd +0.2% · range méd 0.94%
- Excursion ouverture 15min (n=160) : bas méd −0.62% (p90 −1.86%) · haut méd +0.36% · range méd 1.2%
- Excursion ouverture 30min (n=160) : bas méd −0.62% (p90 −1.91%) · haut méd +0.56% · range méd 1.38%
- Excursion ouverture 60min (n=160) : bas méd −0.69% (p90 −1.92%) · haut méd +0.59% · range méd 1.58%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 356.7 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 55% · séance 67% (113/159) · gap 21% · délai 0.2min · rebond 42% (45/113) (MFE +0.85%)
   - −1.0% : fill 30min 40% · séance 49% (82/159) · gap 8% · délai 0.4min · rebond 43% (31/82) (MFE +0.67%)
   - −1.5% : fill 30min 27% · séance 41% (69/159) · gap 3% · délai 7.5min · rebond 45% (26/69) (MFE +0.91%)
   - −2.0% : fill 30min 12% · séance 31% (52/159) · gap 1% · délai 52.5min · rebond 52% (24/52) (MFE +1.14%)
   - −3.0% : fill 30min 3% · séance 16% (29/159) · gap 0% · délai 87.1min · rebond 54% (17/29) (MFE +1.2%)
   - −4.0% : fill 30min 2% · séance 7% (13/159) · gap 0% · délai 126.9min · rebond 62% (7/13) (MFE +1.25%)
   - −5.0% : fill 30min 0% · séance 1% (3/159) · gap 0% · délai 360.2min · rebond 31% (1/3) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.23% (p90 −0.88%) → stop au-delà de −0.71% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −0.78%) → stop au-delà de −0.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=210 jambes) : jambe baissière méd −1.04% (p90 −2.45%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 82% (44/54) · rebond 37% (16/44)
      · −2.0% : fill 63% (32/54) · rebond 48% (15/32)
      · −3.0% : fill 30% (17/54) · rebond 50% (9/17)
      · −4.0% : fill 16% (9/54) · rebond 69% (5/9)
      · −5.0% : fill 2% (2/54) · rebond 0% (0/2)
   - **flat** (43 séances) :
      · −1.0% : fill 43% (19/43) · rebond 56% (10/19)
      · −2.0% : fill 20% (9/43) · rebond 75% (5/9)
      · −3.0% : fill 10% (5/43) · rebond 85% (4/5)
      · −4.0% : fill 1% (1/43) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/43) · rebond 0% (0/0)
   - **gap-up** (62 séances) :
      · −1.0% : fill 28% (19/62) · rebond 42% (5/19)
      · −2.0% : fill 15% (11/62) · rebond 43% (4/11)
      · −3.0% : fill 9% (7/62) · rebond 36% (4/7)
      · −4.0% : fill 4% (3/62) · rebond 30% (1/3)
      · −5.0% : fill 1% (1/62) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 70% si les 15 1res min sont vertes (73 cas) · 32% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **44min** → P(séance verte=clôture>ouverture) 77% si début vert vs 25% si rouge (base 51% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 293min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **77%** · continue >prix actuel 55% ; creux résiduel méd -0.74% (q20 -1.46%) → **SL/trailing à −1.46%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.0% / q75 +1.62% → **scale +1.0% / runner +1.62%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **25%** (continue à baisser 49%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.43%** (au-delà de la MAE q10 -2.43%), cible rebond +1.05% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.6% .. +1.64%] · haut q95 +2.0% · bas q05 -2.27%
   - 60min (n=160) : retour [-1.69% .. +2.17%] · haut q95 +2.47% · bas q05 -2.54%
   - 2h (n=160) : retour [-2.33% .. +2.25%] · haut q95 +2.63% · bas q05 -2.99%
   - 4h (n=160) : retour [-2.1% .. +2.22%] · haut q95 +2.93% · bas q05 -3.35%
   - 6h (n=160) : retour [-2.18% .. +2.6%] · haut q95 +3.15% · bas q05 -3.6%
   - session (n=160) : retour [-3.14% .. +2.67%] · haut q95 +3.64% · bas q05 -4.01%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.7%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : stretched_up
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 78.4  _(surachat)_
- **ADX** : 17.7  _(pas de tendance nette)_
- **MACD** : hist 2.196  _(pas de croisement recent)_
- **BB** : %B 0.87 · largeur 16.9%
- **ATR** : 9.09 (61.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.184  _(accumulation)_
- **Vol ratio** : 0.18  _(volume atone)_
- **Choppiness** : 37.5  _(marche directionnel)_
- **MA** : MA20 340.13 · MA50 331.3 · MA200 307.09  _(prix > MA20)_
- **Dist MA** : MA20 +6.2% · MA50 +9.0% · MA200 +17.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (94428 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
