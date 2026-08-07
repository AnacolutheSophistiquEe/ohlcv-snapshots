# RHM

**Generated** : 2026-08-07T21:36:05.867649+00:00  
**Santé technique** : 6/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €1146.40  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot €1146.40 (+0.6% vs entrée) · entrée €1139.91 · stop €1087.15 · T1 €1170.19 · R/R 0.57  
> ↳ P(T1 av. stop) 77 % _(réel 5 s)_ · EV/risk 0.194 _(réel 5 s)_ (GBM -0.023) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €1133.85–€1145.97 (mid €1139.91)
- Spot actuel : €1146.40 (+0.6% au-dessus de la zone — repli à attendre)
- Stop : €1087.15 (stop swing_plan-based (-5.17%))
- Targets : T1 €1170.19 · R/R 0.57 | T2 €1200.47 · R/R 1.15 | T3 €1230.76 · R/R 1.72
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €1087.15


## Edge, scénarios & sizing

- EV/risk : -0.023 | EV/share : €-1.194 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 58 % | T2 36 % | T3 22 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 36.9 | bear 5.0 | side 58.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.296% → cible +1.188% / stop −2.0%, p_fill 90%, n_eff≈36.7) : P(cible|rempli) **62%** · **EV/risk +0.075** (×p_fill ; si rempli +0.17% du capital)
  - **swing** (entrée dip −0.567% → cible +2.657% / stop −4.629%, p_fill 89%, n_eff≈37.3) : P(cible|rempli) **77%** · **EV/risk +0.194** (×p_fill ; si rempli +1.01% du capital)
  - **deep** (entrée dip −0.876% → cible +3.757% / stop −6.965%, p_fill 89%, n_eff≈37.8) : P(cible|rempli) **70%** · **EV/risk +0.038** (×p_fill ; si rempli +0.30% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→69% · +2.0%→50% · +3.0%→30% · +5.0%→4% · +8.0%→1%
- Range intraday médian 4.12% (p90 6.86%) · excursion haute méd. +2.05% / basse méd. −1.58%
- Profil de vol intra : ouverture 2.608% vs midi 0.912% vs clôture 1.139% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 10% · trend ↑0%/↓0% ; spike-down 49% · recovery-V 40%)_
- **Régime intraday** : **chop** _(efficiency 0.088 ; neutre — autocorr -0.008)_ ; drift intra méd. 0.048% ; recovery-V 43%
- **σ réalisé intraday** 3.002% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 76% / bas 59% / whipsaw 38%
- POC intraday (dernière séance, temps-au-prix) : 1188.8975 (VA 1150.3275–1230.2225 ; dernier close 1149.6)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 20% · rebond 64% · **stop −2.8%** sous le fill (sous le bruit) · cible +1.5% · R/R 0.54 (high win-rate)
- Gaps overnight (n=159) : méd. 0.2% · baisse 38% (gap-down >1% 12% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.73% (p90 −1.74%) · haut méd +0.61% · range méd 1.36%
- Excursion ouverture 15min (n=160) : bas méd −0.91% (p90 −2.0%) · haut méd +0.71% · range méd 1.85%
- Excursion ouverture 30min (n=160) : bas méd −0.94% (p90 −2.7%) · haut méd +0.88% · range méd 2.12%
- Excursion ouverture 60min (n=160) : bas méd −0.98% (p90 −2.85%) · haut méd +1.02% · range méd 2.31%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1149.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 70% (116/159) · gap 26% · délai 0.3min · rebond 60% (64/116) (MFE +1.37%)
   - −1.0% : fill 30min 44% · séance 62% (105/159) · gap 12% · délai 1.9min · rebond 62% (61/105) (MFE +1.41%)
   - −1.5% : fill 30min 30% · séance 51% (82/159) · gap 7% · délai 15.5min · rebond 56% (44/82) (MFE +1.19%)
   - −2.0% : fill 30min 22% · séance 43% (72/159) · gap 6% · délai 26.5min · rebond 66% (45/72) (MFE +1.44%)
   - −3.0% : fill 30min 10% · séance 27% (46/159) · gap 4% · délai 116.8min · rebond 62% (28/46) (MFE +1.41%)
   - −4.0% : fill 30min 4% · séance 20% (28/159) · gap 1% · délai 245.4min · rebond 64% (16/28) (MFE +1.5%)
   - −5.0% : fill 30min 1% · séance 11% (16/159) · gap 1% · délai 293.4min · rebond 56% (8/16) (MFE +1.7%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.67% (p90 −1.67%) → stop au-delà de −1.18% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.48% (p90 −1.77%) → stop au-delà de −1.35% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.33% (p90 −1.93%) → stop au-delà de −1.55% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=496 jambes) : jambe baissière méd −1.07% (p90 −2.61%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (51 séances) :
      · −1.0% : fill 94% (49/51) · rebond 65% (29/49)
      · −2.0% : fill 79% (39/51) · rebond 66% (26/39)
      · −3.0% : fill 53% (27/51) · rebond 64% (17/27)
      · −4.0% : fill 40% (16/51) · rebond 75% (11/16)
      · −5.0% : fill 22% (9/51) · rebond 83% (7/9)
   - **flat** (45 séances) :
      · −1.0% : fill 67% (32/45) · rebond 68% (20/32)
      · −2.0% : fill 29% (17/45) · rebond 72% (10/17)
      · −3.0% : fill 19% (10/45) · rebond 55% (5/10)
      · −4.0% : fill 17% (8/45) · rebond 36% (2/8)
      · −5.0% : fill 11% (6/45) · rebond 22% (1/6)
   - **gap-up** (63 séances) :
      · −1.0% : fill 38% (24/63) · rebond 49% (12/24)
      · −2.0% : fill 26% (16/63) · rebond 62% (9/16)
      · −3.0% : fill 14% (9/63) · rebond 66% (6/9)
      · −4.0% : fill 8% (4/63) · rebond 61% (3/4)
      · −5.0% : fill 3% (1/63) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 54% en base · 64% si les 15 1res min sont vertes (82 cas) · 43% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:38** → P(séance verte=clôture>ouverture) 74% si début vert vs 30% si rouge (base 54% · écart 44 pts) ; prédictivité sature ensuite (plafond brut 299min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **74%** · continue >prix actuel 48% ; creux résiduel méd -1.03% (q20 -2.43%) → **SL/trailing à −2.43%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.37% / q75 +2.28% → **scale +1.37% / runner +2.28%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **30%** (continue à baisser 54%) → **RÉDUIRE ~70%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.52%** (au-delà de la MAE q10 -4.52%), cible rebond +1.13% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.63% .. +3.17%] · haut q95 +3.85% · bas q05 -3.36%
   - 60min (n=160) : retour [-2.97% .. +3.12%] · haut q95 +4.11% · bas q05 -4.32%
   - 2h (n=160) : retour [-3.36% .. +3.1%] · haut q95 +4.16% · bas q05 -4.62%
   - 4h (n=160) : retour [-3.79% .. +3.44%] · haut q95 +4.79% · bas q05 -4.91%
   - 6h (n=160) : retour [-4.34% .. +3.55%] · haut q95 +4.84% · bas q05 -5.49%
   - session (n=160) : retour [-5.96% .. +4.31%] · haut q95 +5.16% · bas q05 -6.26%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.31%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 77.2  _(surachat)_
- **ADX** : 25.2  _(tendance etablie)_
- **MACD** : hist 19.029  _(pas de croisement recent)_
- **BB** : %B 0.75 · largeur 32.3%
- **ATR** : 52.76 (31.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.003  _(neutre)_
- **Vol ratio** : 1.2  _(volume normal)_
- **Choppiness** : 39.7  _(transition)_
- **MA** : MA20 1061.78 · MA50 1102.76 · MA200 1448.23  _(prix > MA20)_
- **Dist MA** : MA20 +8.0% · MA50 +4.0% · MA200 -20.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89643 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
