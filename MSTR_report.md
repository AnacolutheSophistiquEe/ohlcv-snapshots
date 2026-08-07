# MSTR

**Generated** : 2026-08-07T00:21:56.795141+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $96.85  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot $96.85 (+4.0% vs entrée) · entrée $93.09 · stop $87.58 · T1 $97.31 · R/R 0.77  
> ↳ P(T1 av. stop) 55 % _(réel 5 s)_ · EV/risk -0.025 _(réel 5 s)_ (GBM -0.169) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -1905 % hors [0,100] (R² max 0.89). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $92.25–$93.94 (mid $93.09)
- Spot actuel : $96.85 (+4.0% au-dessus de la zone — repli à attendre)
- Stop : $87.58 (stop swing_plan-based (-9.58%))
- Targets : T1 $97.31 · R/R 0.77 | T2 $101.53 · R/R 1.53 | T3 $105.75 · R/R 2.3
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $87.58


## Edge, scénarios & sizing

- EV/risk : -0.169 | EV/share : $-0.933 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 47 % | T2 26 % | T3 10 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 62.9 | bear 20.8 | side 16.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 194.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.76% → cible +2.026% / stop −4.0%, p_fill 61%, n_eff≈27.5) : P(cible|rempli) **50%** · **EV/risk -0.044** (×p_fill ; si rempli -0.29% du capital)
  - **swing** (entrée dip −3.884% → cible +4.531% / stop −5.926%, p_fill 45%, n_eff≈20.9) : P(cible|rempli) **55%** · **EV/risk -0.025** (×p_fill ; si rempli -0.32% du capital)
  - **deep** (entrée dip −5.995% → cible +6.408% / stop −9.09%, p_fill 57%, n_eff≈22.8) : P(cible|rempli) **57%** · **EV/risk +0.048** (×p_fill ; si rempli +0.77% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→74% · +2.0%→60% · +3.0%→42% · +5.0%→16% · +8.0%→8%
- Range intraday médian 5.55% (p90 9.85%) · excursion haute méd. +2.72% / basse méd. −2.51%
- Profil de vol intra : ouverture 3.445% vs midi 1.217% vs clôture 1.356% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 9% · trend ↑0%/↓0% ; spike-down 72% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.107 ; neutre — autocorr -0.008)_ ; drift intra méd. 0.082% ; recovery-V 38%
- **σ réalisé intraday** 3.81% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 76% / bas 57% / whipsaw 34%
- POC intraday (dernière séance, temps-au-prix) : 97.7256 (VA 96.6931–98.0206 ; dernier close 98.29)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 29% · rebond 74% · **stop −4.93%** sous le fill (sous le bruit) · cible +1.68% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. -0.35% · baisse 54% (gap-down >1% 40% · >2% 26%)
- Excursion ouverture 5min (n=160) : bas méd −0.9% (p90 −2.05%) · haut méd +0.76% · range méd 1.75%
- Excursion ouverture 15min (n=160) : bas méd −1.17% (p90 −2.82%) · haut méd +1.14% · range méd 2.43%
- Excursion ouverture 30min (n=160) : bas méd −1.34% (p90 −3.46%) · haut méd +1.46% · range méd 3.18%
- Excursion ouverture 60min (n=160) : bas méd −1.71% (p90 −4.23%) · haut méd +1.71% · range méd 3.8%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 98.29 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 79% (126/159) · gap 48% · délai 0.0min · rebond 52% (63/126) (MFE +1.33%)
   - −1.0% : fill 30min 64% · séance 75% (120/159) · gap 40% · délai 0.0min · rebond 58% (69/120) (MFE +1.32%)
   - −1.5% : fill 30min 55% · séance 68% (110/159) · gap 32% · délai 0.0min · rebond 58% (63/110) (MFE +1.52%)
   - −2.0% : fill 30min 48% · séance 61% (100/159) · gap 26% · délai 0.0min · rebond 59% (62/100) (MFE +1.32%)
   - −3.0% : fill 30min 36% · séance 50% (77/159) · gap 16% · délai 1.2min · rebond 59% (47/77) (MFE +1.57%)
   - −4.0% : fill 30min 24% · séance 42% (64/159) · gap 6% · délai 12.7min · rebond 64% (40/64) (MFE +1.65%)
   - −5.0% : fill 30min 17% · séance 29% (47/159) · gap 4% · délai 19.4min · rebond 74% (34/47) (MFE +1.68%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.88% (p90 −2.28%) → stop au-delà de −1.73% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.08% (p90 −2.74%) → stop au-delà de −2.25% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.08% (p90 −2.68%) → stop au-delà de −2.28% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=954 jambes) : jambe baissière méd −1.13% (p90 −2.69%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (76 séances) :
      · −1.0% : fill 100% (75/76) · rebond 49% (37/75)
      · −2.0% : fill 90% (68/76) · rebond 58% (39/68)
      · −3.0% : fill 81% (60/76) · rebond 59% (36/60)
      · −4.0% : fill 68% (50/76) · rebond 67% (33/50)
      · −5.0% : fill 49% (38/76) · rebond 76% (28/38)
   - **flat** (16 séances) :
      · −1.0% : fill 92% (15/16) · rebond 89% (11/15)
      · −2.0% : fill 65% (11/16) · rebond 48% (7/11)
      · −3.0% : fill 36% (6/16) · rebond 57% (4/6)
      · −4.0% : fill 23% (5/16) · rebond 13% (2/5)
      · −5.0% : fill 18% (4/16) · rebond 16% (2/4)
   - **gap-up** (67 séances) :
      · −1.0% : fill 38% (30/67) · rebond 71% (21/30)
      · −2.0% : fill 23% (21/67) · rebond 71% (16/21)
      · −3.0% : fill 15% (11/67) · rebond 56% (7/11)
      · −4.0% : fill 14% (9/67) · rebond 66% (5/9)
      · −5.0% : fill 7% (5/67) · rebond 93% (4/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 56% si les 15 1res min sont vertes (77 cas) · 40% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:13** → P(séance verte=clôture>ouverture) 78% si début vert vs 18% si rouge (base 48% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 136min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **78%** · continue >prix actuel 57% ; creux résiduel méd -1.44% (q20 -2.6%) → **SL/trailing à −2.6%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.95% / q75 +3.15% → **scale +1.95% / runner +3.15%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **18%** (continue à baisser 58%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.03%** (au-delà de la MAE q10 -5.03%), cible rebond +1.62% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.52% .. +3.78%] · haut q95 +4.03% · bas q05 -3.97%
   - 60min (n=160) : retour [-4.88% .. +3.51%] · haut q95 +5.23% · bas q05 -5.5%
   - 2h (n=160) : retour [-4.61% .. +5.49%] · haut q95 +5.8% · bas q05 -5.5%
   - 4h (n=160) : retour [-6.5% .. +6.73%] · haut q95 +8.52% · bas q05 -7.13%
   - 6h (n=160) : retour [-5.95% .. +6.29%] · haut q95 +8.52% · bas q05 -8.08%
   - session (n=160) : retour [-5.64% .. +5.97%] · haut q95 +8.52% · bas q05 -8.08%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0.6% / strong 5.0%) · base = 9 séances trend-up (n_eff 6.0)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **14%**. Lecture précoce 30 min : signature présente → 8% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.43% (p75 2.48% / p90 3.79%) · ~3.8 replis/séance, durée méd 50.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **80%** (reprise méd 25.0 min, n=32)
   - −1.0% → **71%** (reprise méd 35.0 min, n=20)
   - −1.5% → **57%** (reprise méd 74.97 min, n=13)
   - −2.0% → **40%** (reprise méd 89.44 min, n=8)
   - −3.0% → **79%** (reprise méd 89.44 min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−3.79%** (p90, défaut prudent ; serré/agressif −2.48%) ; extension open→close méd +7.18% (q75 +8.18% / q95 +12.92%), MFE méd +9.29% / q90 +12.58%
   - Échelle scale-out : +9.29% (33%) / +10.7% (33%) / +12.58% (34%)
- **DÉSARMER** : repli > **−3.79%** depuis le plus-haut = décay → P(retournement) **29%** (préavis méd 300.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.58% : P(retournement après) 0% (mèche méd 0.76%)
- **CONTEXTE** : la dernière heure tient les gains 96% du temps (retour médian dernière heure +0.68%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 52.2  _(neutre)_
- **ADX** : 11.1  _(pas de tendance nette)_
- **MACD** : hist 1.39  _(pas de croisement recent)_
- **BB** : %B 0.57 · largeur 11.3%
- **ATR** : 5.52 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.107  _(accumulation)_
- **Vol ratio** : 0.67  _(volume normal)_
- **Choppiness** : 61.1  _(transition)_
- **MA** : MA20 96.13 · MA50 107.42 · MA200 153.92  _(prix > MA20)_
- **Dist MA** : MA20 +0.7% · MA50 -9.8% · MA200 -37.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90616 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
