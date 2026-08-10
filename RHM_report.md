# RHM

**Generated** : 2026-08-10T00:01:55.969798+00:00  
**Santé technique** : 6/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €1146.40  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot €1146.40 (+0.6% vs entrée) · entrée €1139.91 · stop €1087.15 · T1 €1170.19 · R/R 0.57  
> ↳ P(T1 av. stop) 77 % _(réel 5 s)_ · EV/risk 0.187 _(réel 5 s)_ (GBM -0.023) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_  

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
  - **intraday** (entrée dip −0.296% → cible +1.188% / stop −2.0%, p_fill 90%, n_eff≈36.8) : P(cible|rempli) **59%** · **EV/risk +0.020** (×p_fill ; si rempli +0.04% du capital)
  - **swing** (entrée dip −0.567% → cible +2.657% / stop −4.629%, p_fill 85%, n_eff≈37.2) : P(cible|rempli) **77%** · **EV/risk +0.187** (×p_fill ; si rempli +1.02% du capital)
  - **deep** (entrée dip −0.876% → cible +3.757% / stop −6.965%, p_fill 90%, n_eff≈37.6) : P(cible|rempli) **72%** · **EV/risk +0.063** (×p_fill ; si rempli +0.49% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→69% · +2.0%→50% · +3.0%→31% · +5.0%→4% · +8.0%→1%
- Range intraday médian 4.17% (p90 6.98%) · excursion haute méd. +2.05% / basse méd. −1.63%
- Profil de vol intra : ouverture 2.651% vs midi 0.923% vs clôture 1.117% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 10% · trend ↑0%/↓0% ; spike-down 50% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.086 ; neutre — autocorr -0.01)_ ; drift intra méd. -0.004% ; recovery-V 40%
- **σ réalisé intraday** 3.031% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 77% / bas 61% / whipsaw 41%
- POC intraday (dernière séance, temps-au-prix) : 1152.3425 (VA 1134.3875–1164.3125 ; dernier close 1146.5)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 20% · rebond 64% · **stop −2.8%** sous le fill (sous le bruit) · cible +1.5% · R/R 0.54 (high win-rate)
- Gaps overnight (n=159) : méd. 0.2% · baisse 37% (gap-down >1% 12% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.71% (p90 −1.73%) · haut méd +0.64% · range méd 1.39%
- Excursion ouverture 15min (n=160) : bas méd −0.91% (p90 −2.0%) · haut méd +0.72% · range méd 1.84%
- Excursion ouverture 30min (n=160) : bas méd −0.93% (p90 −2.58%) · haut méd +0.91% · range méd 2.16%
- Excursion ouverture 60min (n=160) : bas méd −0.97% (p90 −2.71%) · haut méd +1.06% · range méd 2.35%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1146.5 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 71% (116/159) · gap 25% · délai 0.3min · rebond 61% (65/116) (MFE +1.34%)
   - −1.0% : fill 30min 43% · séance 63% (105/159) · gap 12% · délai 4.1min · rebond 63% (62/105) (MFE +1.4%)
   - −1.5% : fill 30min 29% · séance 52% (82/159) · gap 7% · délai 18.4min · rebond 58% (45/82) (MFE +1.26%)
   - −2.0% : fill 30min 21% · séance 42% (71/159) · gap 6% · délai 26.8min · rebond 66% (44/71) (MFE +1.47%)
   - −3.0% : fill 30min 10% · séance 27% (45/159) · gap 4% · délai 116.9min · rebond 62% (27/45) (MFE +1.39%)
   - −4.0% : fill 30min 4% · séance 20% (28/159) · gap 1% · délai 245.4min · rebond 64% (16/28) (MFE +1.5%)
   - −5.0% : fill 30min 1% · séance 11% (16/159) · gap 1% · délai 293.4min · rebond 56% (8/16) (MFE +1.7%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.61% (p90 −1.65%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.46% (p90 −1.77%) → stop au-delà de −1.34% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.29% (p90 −1.89%) → stop au-delà de −1.42% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=501 jambes) : jambe baissière méd −1.07% (p90 −2.65%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 94% (48/50) · rebond 66% (29/48)
      · −2.0% : fill 79% (38/50) · rebond 66% (25/38)
      · −3.0% : fill 52% (26/50) · rebond 63% (16/26)
      · −4.0% : fill 40% (16/50) · rebond 75% (11/16)
      · −5.0% : fill 22% (9/50) · rebond 83% (7/9)
   - **flat** (45 séances) :
      · −1.0% : fill 67% (32/45) · rebond 68% (20/32)
      · −2.0% : fill 29% (17/45) · rebond 72% (10/17)
      · −3.0% : fill 19% (10/45) · rebond 55% (5/10)
      · −4.0% : fill 17% (8/45) · rebond 36% (2/8)
      · −5.0% : fill 11% (6/45) · rebond 22% (1/6)
   - **gap-up** (64 séances) :
      · −1.0% : fill 40% (25/64) · rebond 54% (13/25)
      · −2.0% : fill 25% (16/64) · rebond 62% (9/16)
      · −3.0% : fill 14% (9/64) · rebond 66% (6/9)
      · −4.0% : fill 7% (4/64) · rebond 61% (3/4)
      · −5.0% : fill 3% (1/64) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 62% si les 15 1res min sont vertes (82 cas) · 43% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:38** → P(séance verte=clôture>ouverture) 72% si début vert vs 30% si rouge (base 52% · écart 42 pts) ; prédictivité sature ensuite (plafond brut 299min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **72%** · continue >prix actuel 46% ; creux résiduel méd -1.1% (q20 -3.06%) → **SL/trailing à −3.06%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.29% / q75 +2.25% → **scale +1.29% / runner +2.25%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **30%** (continue à baisser 54%) → **RÉDUIRE ~70%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.52%** (au-delà de la MAE q10 -4.52%), cible rebond +1.13% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.63% .. +3.35%] · haut q95 +3.85% · bas q05 -3.32%
   - 60min (n=160) : retour [-2.94% .. +3.15%] · haut q95 +4.24% · bas q05 -4.29%
   - 2h (n=160) : retour [-3.34% .. +3.1%] · haut q95 +4.35% · bas q05 -4.61%
   - 4h (n=160) : retour [-3.78% .. +3.42%] · haut q95 +4.77% · bas q05 -4.88%
   - 6h (n=160) : retour [-4.33% .. +3.53%] · haut q95 +4.83% · bas q05 -5.45%
   - session (n=160) : retour [-5.92% .. +4.28%] · haut q95 +5.14% · bas q05 -6.25%


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)


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

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89725 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
