# SOFI

**Generated** : 2026-07-16T00:34:38.683743+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $17.87  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-5 sess · macro taux)  
> ↳ spot $17.87 (+5.9% vs entrée) · entrée $16.87 · stop $16.58 · T1 $17.46 · R/R 2.03  
> ↳ P(T1 av. stop) 29 % · EV/risk -0.133 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 402 % hors [0,100] (R² max 0.85). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $16.76–$16.99 (mid $16.87)
- Spot actuel : $17.87 (+5.9% au-dessus de la zone — repli à attendre)
- Stop : $16.58 (stop swing_plan-based (-7.21%))
- Targets : T1 $17.46 · R/R 2.03 | T2 $18.04 · R/R 4.03 | T3 $18.62 · R/R 6.03
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.58


## Edge, scénarios & sizing

- EV/risk : -0.133 | EV/share : $-0.039 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 29 % | T2 18 % | T3 12 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 26.0 | bear 24.2 | side 49.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 143.0 (= 8 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.531% → cible +1.546% / stop −4.0%, p_fill 41%, n_eff≈17.8) : P(cible|rempli) **54%** · **EV/risk +0.044** (×p_fill ; si rempli +0.43% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=10, n_eff=6))
  - **deep** : indisponible (échantillon insuffisant (n=10, n_eff=6))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→69% · +2.0%→48% · +3.0%→35% · +5.0%→10% · +8.0%→0%
- Range intraday médian 4.41% (p90 6.91%) · excursion haute méd. +1.89% / basse méd. −2.15%
- Profil de vol intra : ouverture 2.999% vs midi 0.947% vs clôture 0.994% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 14% · trend ↑1%/↓1% ; spike-down 65% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.118 ; neutre — autocorr 0.001)_ ; drift intra méd. 0.151% ; recovery-V 27%
- **σ réalisé intraday** 3.171% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 62% / bas 56% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 18.7812 (VA 18.7537–18.9462 ; dernier close 18.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 49% · rebond 73% · **stop −3.19%** sous le fill (sous le bruit) · cible +2.1% · R/R 0.66 (high win-rate)
- Gaps overnight (n=159) : méd. 0.06% · baisse 48% (gap-down >1% 25% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −1.79%) · haut méd +0.74% · range méd 1.7%
- Excursion ouverture 15min (n=160) : bas méd −0.99% (p90 −3.17%) · haut méd +1.14% · range méd 2.34%
- Excursion ouverture 30min (n=160) : bas méd −1.12% (p90 −3.2%) · haut méd +1.31% · range méd 2.86%
- Excursion ouverture 60min (n=160) : bas méd −1.35% (p90 −3.47%) · haut méd +1.47% · range méd 3.48%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 18.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 76% (123/159) · gap 31% · délai 0.0min · rebond 58% (68/123) (MFE +1.31%)
   - −1.0% : fill 30min 50% · séance 67% (112/159) · gap 25% · délai 0.4min · rebond 66% (72/112) (MFE +1.39%)
   - −1.5% : fill 30min 43% · séance 62% (101/159) · gap 18% · délai 1.7min · rebond 67% (64/101) (MFE +1.81%)
   - −2.0% : fill 30min 35% · séance 49% (75/159) · gap 11% · délai 2.7min · rebond 73% (51/75) (MFE +2.1%)
   - −3.0% : fill 30min 18% · séance 33% (54/159) · gap 3% · délai 17.8min · rebond 72% (38/54) (MFE +1.85%)
   - −4.0% : fill 30min 8% · séance 21% (37/159) · gap 2% · délai 47.4min · rebond 64% (23/37) (MFE +1.84%)
   - −5.0% : fill 30min 4% · séance 10% (20/159) · gap 1% · délai 58.5min · rebond 47% (10/20) (MFE +0.93%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.47% (p90 −1.73%) → stop au-delà de −1.38% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.48% (p90 −1.7%) → stop au-delà de −1.43% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.47% (p90 −1.71%) → stop au-delà de −1.13% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=674 jambes) : jambe baissière méd −1.08% (p90 −2.76%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (67 séances) :
      · −1.0% : fill 96% (65/67) · rebond 69% (42/65)
      · −2.0% : fill 80% (51/67) · rebond 74% (37/51)
      · −3.0% : fill 61% (40/67) · rebond 76% (29/40)
      · −4.0% : fill 39% (27/67) · rebond 65% (19/27)
      · −5.0% : fill 21% (14/67) · rebond 47% (8/14)
   - **flat** (26 séances) :
      · −1.0% : fill 56% (17/26) · rebond 33% (10/17)
      · −2.0% : fill 36% (10/26) · rebond 39% (5/10)
      · −3.0% : fill 28% (7/26) · rebond 34% (4/7)
      · −4.0% : fill 19% (4/26) · rebond 64% (1/4)
      · −5.0% : fill 2% (2/26) · rebond 0% (0/2)
   - **gap-up** (66 séances) :
      · −1.0% : fill 43% (30/66) · rebond 73% (20/30)
      · −2.0% : fill 24% (14/66) · rebond 87% (9/14)
      · −3.0% : fill 8% (7/66) · rebond 84% (5/7)
      · −4.0% : fill 4% (6/66) · rebond 62% (3/6)
      · −5.0% : fill 2% (4/66) · rebond 61% (2/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 55% si les 15 1res min sont vertes (74 cas) · 34% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 76% si début vert vs 15% si rouge (base 45% · écart 61 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **76%** · continue >prix actuel 52% ; creux résiduel méd -1.57% (q20 -3.78%) → **SL/trailing à −3.78%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.64% / q75 +2.76% → **scale +1.64% / runner +2.76%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **15%** (continue à baisser 55%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.04%** (au-delà de la MAE q10 -4.04%), cible rebond +1.37% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.81% .. +3.62%] · haut q95 +4.01% · bas q05 -3.45%
   - 60min (n=160) : retour [-3.21% .. +3.56%] · haut q95 +4.33% · bas q05 -4.03%
   - 2h (n=160) : retour [-3.84% .. +3.75%] · haut q95 +4.92% · bas q05 -5.04%
   - 4h (n=160) : retour [-3.81% .. +4.56%] · haut q95 +5.68% · bas q05 -5.08%
   - 6h (n=160) : retour [-4.24% .. +4.05%] · haut q95 +5.7% · bas q05 -5.16%
   - session (n=160) : retour [-4.12% .. +5.03%] · haut q95 +5.7% · bas q05 -5.23%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (4) pour des stats fiables : 2.5% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.94%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 54.7  _(neutre)_
- **ADX** : 25.6  _(tendance etablie)_
- **MACD** : hist -0.016  _(bearish_recent)_
- **BB** : %B 0.47 · largeur 11.2%
- **ATR** : 0.94 (22.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.103  _(distribution)_
- **Vol ratio** : 0.81  _(volume normal)_
- **Choppiness** : 57.0  _(transition)_
- **MA** : MA20 17.94 · MA50 16.98 · MA200 21.92  _(prix < MA20)_
- **Dist MA** : MA20 -0.4% · MA50 +5.3% · MA200 -18.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (85492 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
