# MSTR

**Generated** : 2026-08-07T21:58:44.523255+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $100.01  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $100.01 (+2.7% vs entrée) · entrée $97.41 · stop $93.51 · T1 $99.42 · R/R 0.52  
> ↳ P(T1 av. stop) 45 % _(réel 5 s)_ · EV/risk -0.035 _(réel 5 s)_ (GBM -0.017) · ¼-Kelly 0.019 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -1112 % hors [0,100] (R² max 0.89). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $97.01–$97.81 (mid $97.41)
- Spot actuel : $100.01 (+2.7% au-dessus de la zone — repli à attendre)
- Stop : $93.51 (stop swing_plan-based (-11.42%))
- Targets : T1 $99.42 · R/R 0.52 | T2 $101.42 · R/R 1.03 | T3 $103.43 · R/R 1.54
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $93.51


## Edge, scénarios & sizing

- EV/risk : -0.017 | EV/share : $-0.065 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 59 % | T2 25 % | T3 16 %
- Kelly (position) : f* 0.076 | ¼-Kelly 0.019 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 74.1 | bear 11.0 | side 14.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 200.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.594% → cible +2.06% / stop −4.0%, p_fill 36%, n_eff≈18.7) : P(cible|rempli) **45%** · **EV/risk -0.035** (×p_fill ; si rempli -0.39% du capital)
  - **swing** (entrée dip −5.713% → cible +4.606% / stop −6.053%, p_fill 43%, n_eff≈17.3) : P(cible|rempli) **75%** · **EV/risk +0.113** (×p_fill ; si rempli +1.60% du capital)
  - **deep** (entrée dip −8.84% → cible +6.514% / stop −9.39%, p_fill 40%, n_eff≈18.0) : P(cible|rempli) **62%** · **EV/risk -0.003** (×p_fill ; si rempli -0.07% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→74% · +2.0%→60% · +3.0%→41% · +5.0%→16% · +8.0%→8%
- Range intraday médian 5.47% (p90 9.85%) · excursion haute méd. +2.63% / basse méd. −2.47%
- Profil de vol intra : ouverture 3.446% vs midi 1.214% vs clôture 1.349% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 70% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.105 ; neutre — autocorr -0.012)_ ; drift intra méd. 0.113% ; recovery-V 38%
- **σ réalisé intraday** 3.752% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 78% / bas 55% / whipsaw 33%
- POC intraday (dernière séance, temps-au-prix) : 97.2334 (VA 96.3844–97.6579 ; dernier close 96.88)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 29% · rebond 74% · **stop −4.93%** sous le fill (sous le bruit) · cible +1.68% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. -0.37% · baisse 55% (gap-down >1% 42% · >2% 28%)
- Excursion ouverture 5min (n=160) : bas méd −0.9% (p90 −2.04%) · haut méd +0.76% · range méd 1.74%
- Excursion ouverture 15min (n=160) : bas méd −1.14% (p90 −2.82%) · haut méd +1.16% · range méd 2.42%
- Excursion ouverture 30min (n=160) : bas méd −1.33% (p90 −3.45%) · haut méd +1.46% · range méd 3.14%
- Excursion ouverture 60min (n=160) : bas méd −1.69% (p90 −4.22%) · haut méd +1.8% · range méd 3.79%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 96.88 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 79% (126/159) · gap 49% · délai 0.0min · rebond 50% (63/126) (MFE +1.22%)
   - −1.0% : fill 30min 65% · séance 75% (120/159) · gap 42% · délai 0.0min · rebond 59% (69/120) (MFE +1.2%)
   - −1.5% : fill 30min 56% · séance 68% (110/159) · gap 33% · délai 0.0min · rebond 59% (63/110) (MFE +1.54%)
   - −2.0% : fill 30min 49% · séance 62% (100/159) · gap 28% · délai 0.0min · rebond 60% (62/100) (MFE +1.37%)
   - −3.0% : fill 30min 35% · séance 50% (77/159) · gap 16% · délai 1.2min · rebond 59% (47/77) (MFE +1.57%)
   - −4.0% : fill 30min 24% · séance 42% (64/159) · gap 6% · délai 12.7min · rebond 64% (40/64) (MFE +1.65%)
   - −5.0% : fill 30min 17% · séance 29% (47/159) · gap 4% · délai 19.4min · rebond 74% (34/47) (MFE +1.68%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.85% (p90 −2.28%) → stop au-delà de −1.72% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.07% (p90 −2.73%) → stop au-delà de −2.2% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.08% (p90 −2.68%) → stop au-delà de −2.28% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=954 jambes) : jambe baissière méd −1.13% (p90 −2.68%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (77 séances) :
      · −1.0% : fill 100% (76/77) · rebond 51% (38/76)
      · −2.0% : fill 90% (69/77) · rebond 60% (40/69)
      · −3.0% : fill 78% (60/77) · rebond 59% (36/60)
      · −4.0% : fill 66% (50/77) · rebond 67% (33/50)
      · −5.0% : fill 47% (38/77) · rebond 76% (28/38)
   - **flat** (16 séances) :
      · −1.0% : fill 92% (15/16) · rebond 89% (11/15)
      · −2.0% : fill 65% (11/16) · rebond 48% (7/11)
      · −3.0% : fill 36% (6/16) · rebond 57% (4/6)
      · −4.0% : fill 23% (5/16) · rebond 13% (2/5)
      · −5.0% : fill 18% (4/16) · rebond 16% (2/4)
   - **gap-up** (66 séances) :
      · −1.0% : fill 38% (29/66) · rebond 70% (20/29)
      · −2.0% : fill 23% (20/66) · rebond 71% (15/20)
      · −3.0% : fill 15% (11/66) · rebond 56% (7/11)
      · −4.0% : fill 14% (9/66) · rebond 66% (5/9)
      · −5.0% : fill 7% (5/66) · rebond 93% (4/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 58% si les 15 1res min sont vertes (78 cas) · 40% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:13** → P(séance verte=clôture>ouverture) 79% si début vert vs 18% si rouge (base 49% · écart 61 pts) ; prédictivité sature ensuite (plafond brut 136min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **79%** · continue >prix actuel 55% ; creux résiduel méd -1.46% (q20 -2.65%) → **SL/trailing à −2.65%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.89% / q75 +3.07% → **scale +1.89% / runner +3.07%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **18%** (continue à baisser 58%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.03%** (au-delà de la MAE q10 -5.03%), cible rebond +1.62% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.51% .. +3.77%] · haut q95 +4.02% · bas q05 -3.96%
   - 60min (n=160) : retour [-4.86% .. +3.51%] · haut q95 +5.23% · bas q05 -5.48%
   - 2h (n=160) : retour [-4.6% .. +5.48%] · haut q95 +5.8% · bas q05 -5.48%
   - 4h (n=160) : retour [-6.31% .. +6.73%] · haut q95 +8.52% · bas q05 -7.11%
   - 6h (n=160) : retour [-5.94% .. +6.16%] · haut q95 +8.52% · bas q05 -8.05%
   - session (n=160) : retour [-5.63% .. +5.94%] · haut q95 +8.52% · bas q05 -8.05%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0.6% / strong 5.0%) · base = 9 séances trend-up (n_eff 6.0)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **14%**. Lecture précoce 30 min : signature présente → 7% vs absente 2% (base 6%)
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
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 52.4  _(neutre)_
- **ADX** : 11.1  _(pas de tendance nette)_
- **MACD** : hist 1.508  _(pas de croisement recent)_
- **BB** : %B 0.82 · largeur 11.7%
- **ATR** : 5.71 (3.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.112  _(accumulation)_
- **Vol ratio** : 1.83  _(volume au-dessus de la moyenne)_
- **Choppiness** : 60.3  _(transition)_
- **MA** : MA20 96.4 · MA50 106.34 · MA200 152.94  _(prix > MA20)_
- **Dist MA** : MA20 +3.7% · MA50 -6.0% · MA200 -34.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91334 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
