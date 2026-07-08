# SAF

**Generated** : 2026-07-08T00:07:24.427552+00:00  
**Santé technique** : 10/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €347.20  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot €347.20 (+0.4% vs entrée) · entrée €345.88 · stop €341.88 · T1 €353.86 · R/R 2.0  
> ↳ P(T1 av. stop) 42 % _(réel 5 s)_ · EV/risk 0.153 _(réel 5 s)_ (GBM 0.168) · ¼-Kelly 0.01 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 130 % hors [0,100] (R² max 0.19). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 10/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €344.56–€347.20 (mid €345.88)
- Spot actuel : €347.20 (+0.4% au-dessus de la zone — repli à attendre)
- Stop : €341.88 (stop swing_plan-based (-1.53%))
- Targets : T1 €353.86 · R/R 2.0 | T2 €361.85 · R/R 3.99 | T3 €369.84 · R/R 5.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €341.88


## Edge, scénarios & sizing

- EV/risk : 0.168 | EV/share : €0.669 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 18 % | T3 13 %
- Kelly (position) : f* 0.04 | ¼-Kelly 0.01 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 28.9 | side 66.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 347.0 (= 1 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.305% → cible +1.033% / stop −1.5%, p_fill 71%, n_eff≈30.6) : P(cible|rempli) **41%** · **EV/risk +0.064** (×p_fill ; si rempli +0.14% du capital)
  - **swing** (entrée dip −0.38% → cible +2.309% / stop −1.154%, p_fill 74%, n_eff≈31.4) : P(cible|rempli) **42%** · **EV/risk +0.153** (×p_fill ; si rempli +0.24% du capital)
  - **deep** (entrée dip −0.536% → cible +3.265% / stop −1.633%, p_fill 76%, n_eff≈33.1) : P(cible|rempli) **56%** · **EV/risk +0.508** (×p_fill ; si rempli +1.09% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→61% · +2.0%→39% · +3.0%→16% · +5.0%→5% · +8.0%→2%
- Range intraday médian 2.75% (p90 4.93%) · excursion haute méd. +1.52% / basse méd. −0.95%
- Profil de vol intra : ouverture 1.636% vs midi 0.661% vs clôture 0.77% _(ouverture ~2.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (143 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 17% · trend ↑0%/↓0% ; spike-down 32% · recovery-V 19%)_
- **Régime intraday** : **chop** _(efficiency 0.116 ; mean-reverting — autocorr -0.032)_ ; drift intra méd. 0.639% ; recovery-V 27%
- **σ réalisé intraday** 1.78% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 76% / bas 44% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 359.0506 (VA 357.2306–359.5056 ; dernier close 358.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 19% · rebond 59% · **stop −1.6%** sous le fill (sous le bruit) · cible +1.23% · R/R 0.77 (high win-rate)
- Gaps overnight (n=142) : méd. -0.06% · baisse 52% (gap-down >1% 13% · >2% 2%)
- Excursion ouverture 5min (n=143) : bas méd −0.31% (p90 −1.38%) · haut méd +0.33% · range méd 0.91%
- Excursion ouverture 15min (n=143) : bas méd −0.36% (p90 −1.53%) · haut méd +0.5% · range méd 1.17%
- Excursion ouverture 30min (n=143) : bas méd −0.44% (p90 −1.67%) · haut méd +0.58% · range méd 1.28%
- Excursion ouverture 60min (n=143) : bas méd −0.65% (p90 −1.85%) · haut méd +0.7% · range méd 1.47%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 358.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 54% · séance 64% (99/142) · gap 28% · délai 0.2min · rebond 39% (37/99) (MFE +0.82%)
   - −1.0% : fill 30min 40% · séance 48% (71/142) · gap 13% · délai 0.4min · rebond 44% (26/71) (MFE +0.62%)
   - −1.5% : fill 30min 26% · séance 40% (60/142) · gap 5% · délai 6.9min · rebond 38% (20/60) (MFE +0.89%)
   - −2.0% : fill 30min 13% · séance 30% (43/142) · gap 2% · délai 39.0min · rebond 48% (19/43) (MFE +0.91%)
   - −3.0% : fill 30min 4% · séance 19% (26/142) · gap 1% · délai 203.0min · rebond 59% (16/26) (MFE +1.23%)
   - −4.0% : fill 30min 3% · séance 9% (12/142) · gap 0% · délai 153.7min · rebond 53% (6/12) (MFE +1.49%)
   - −5.0% : fill 30min 0% · séance 2% (3/142) · gap 0% · délai 360.2min · rebond 31% (1/3) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.19% (p90 −0.92%) → stop au-delà de −0.76% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −0.91%) → stop au-delà de −0.69% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=166 jambes) : jambe baissière méd −1.05% (p90 −2.72%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 77% (39/50) · rebond 43% (15/39)
      · −2.0% : fill 53% (27/50) · rebond 51% (13/27)
      · −3.0% : fill 33% (16/50) · rebond 58% (9/16)
      · −4.0% : fill 15% (8/50) · rebond 59% (4/8)
      · −5.0% : fill 3% (2/50) · rebond 0% (0/2)
   - **flat** (40 séances) :
      · −1.0% : fill 39% (16/40) · rebond 62% (8/16)
      · −2.0% : fill 17% (7/40) · rebond 50% (3/7)
      · −3.0% : fill 8% (4/40) · rebond 69% (3/4)
      · −4.0% : fill 2% (1/40) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/40) · rebond 0% (0/0)
   - **gap-up** (52 séances) :
      · −1.0% : fill 23% (16/52) · rebond 26% (3/16)
      · −2.0% : fill 14% (9/52) · rebond 34% (3/9)
      · −3.0% : fill 11% (6/52) · rebond 55% (4/6)
      · −4.0% : fill 7% (3/52) · rebond 30% (1/3)
      · −5.0% : fill 2% (1/52) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=143) : 56% en base · 72% si les 15 1res min sont vertes (66 cas) · 36% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=143) : COUDE à **44min** → P(séance verte=clôture>ouverture) 81% si début vert vs 27% si rouge (base 56% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=66) : tient le vert **81%** · continue >prix actuel 63% ; creux résiduel méd -0.56% (q20 -1.41%) → **SL/trailing à −1.41%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.29% / q75 +1.83% → **scale +1.29% / runner +1.83%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **27%** (continue à baisser 45%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.47%** (au-delà de la MAE q10 -2.47%), cible rebond +0.97% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=143) : retour [-1.75% .. +1.68%] · haut q95 +2.0% · bas q05 -2.27%
   - 60min (n=143) : retour [-1.78% .. +2.29%] · haut q95 +2.88% · bas q05 -2.5%
   - 2h (n=143) : retour [-2.1% .. +2.27%] · haut q95 +3.38% · bas q05 -2.91%
   - 4h (n=143) : retour [-2.14% .. +2.42%] · haut q95 +3.44% · bas q05 -2.99%
   - 6h (n=143) : retour [-2.15% .. +3.37%] · haut q95 +3.62% · bas q05 -3.06%
   - session (n=143) : retour [-2.81% .. +3.62%] · haut q95 +4.01% · bas q05 -4.02%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 2.1% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.66%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 65.8  _(momentum haussier)_
- **ADX** : 34.5  _(tendance etablie)_
- **MACD** : hist 0.902  _(pas de croisement recent)_
- **BB** : %B 0.7 · largeur 22.5%
- **ATR** : 8.24 (60.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.099  _(accumulation)_
- **Vol ratio** : 0.36  _(volume atone)_
- **Choppiness** : 45.4  _(transition)_
- **MA** : MA20 332.15 · MA50 303.81 · MA200 301.96  _(prix > MA20)_
- **Dist MA** : MA20 +4.5% · MA50 +14.3% · MA200 +15.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92383 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
