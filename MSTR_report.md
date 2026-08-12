# MSTR

**Generated** : 2026-08-12T00:20:49.248386+00:00  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $96.09  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot $96.09 (+3.8% vs entrée) · entrée $92.53 · stop $86.96 · T1 $96.54 · R/R 0.72  
> ↳ P(T1 av. stop) 63 % _(réel 5 s)_ · EV/risk 0.02 _(réel 5 s)_ (GBM -0.129) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 304 % hors [0,100] (R² max 0.84). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $91.73–$93.33 (mid $92.53)
- Spot actuel : $96.09 (+3.8% au-dessus de la zone — repli à attendre)
- Stop : $86.96 (stop swing_plan-based (-9.5%))
- Targets : T1 $96.54 · R/R 0.72 | T2 $100.56 · R/R 1.44 | T3 $104.57 · R/R 2.16
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $86.96


## Edge, scénarios & sizing

- EV/risk : -0.129 | EV/share : $-0.716 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 51 % | T2 28 % | T3 12 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 63.2 | bear 20.6 | side 16.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 96.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.688% → cible +1.94% / stop −4.0%, p_fill 63%, n_eff≈28.8) : P(cible|rempli) **53%** · **EV/risk -0.011** (×p_fill ; si rempli -0.07% du capital)
  - **swing** (entrée dip −3.706% → cible +4.337% / stop −6.017%, p_fill 50%, n_eff≈21.7) : P(cible|rempli) **63%** · **EV/risk +0.020** (×p_fill ; si rempli +0.24% du capital)
  - **deep** (entrée dip −5.729% → cible +6.134% / stop −9.22%, p_fill 52%, n_eff≈23.0) : P(cible|rempli) **57%** · **EV/risk +0.032** (×p_fill ; si rempli +0.57% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→74% · +2.0%→60% · +3.0%→41% · +5.0%→15% · +8.0%→6%
- Range intraday médian 5.47% (p90 9.51%) · excursion haute méd. +2.63% / basse méd. −2.51%
- Profil de vol intra : ouverture 3.402% vs midi 1.206% vs clôture 1.347% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 71% · recovery-V 38%)_
- **Régime intraday** : **chop** _(efficiency 0.102 ; neutre — autocorr 0.002)_ ; drift intra méd. 0.039% ; recovery-V 35%
- **σ réalisé intraday** 3.818% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 78% / bas 57% / whipsaw 36%
- POC intraday (dernière séance, temps-au-prix) : 101.8936 (VA 98.6424–103.6276 ; dernier close 100.02)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 28% · rebond 74% · **stop −4.93%** sous le fill (sous le bruit) · cible +1.68% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. -0.35% · baisse 54% (gap-down >1% 41% · >2% 27%)
- Excursion ouverture 5min (n=160) : bas méd −0.9% (p90 −2.03%) · haut méd +0.78% · range méd 1.75%
- Excursion ouverture 15min (n=160) : bas méd −1.14% (p90 −2.82%) · haut méd +1.23% · range méd 2.43%
- Excursion ouverture 30min (n=160) : bas méd −1.3% (p90 −3.43%) · haut méd +1.47% · range méd 3.18%
- Excursion ouverture 60min (n=160) : bas méd −1.62% (p90 −4.19%) · haut méd +1.84% · range méd 3.81%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 100.02 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 78% (125/159) · gap 48% · délai 0.0min · rebond 50% (62/125) (MFE +1.17%)
   - −1.0% : fill 30min 64% · séance 74% (119/159) · gap 41% · délai 0.0min · rebond 59% (69/119) (MFE +1.2%)
   - −1.5% : fill 30min 55% · séance 67% (109/159) · gap 33% · délai 0.0min · rebond 59% (63/109) (MFE +1.54%)
   - −2.0% : fill 30min 49% · séance 61% (99/159) · gap 27% · délai 0.0min · rebond 60% (62/99) (MFE +1.38%)
   - −3.0% : fill 30min 35% · séance 49% (77/159) · gap 16% · délai 1.2min · rebond 59% (47/77) (MFE +1.57%)
   - −4.0% : fill 30min 23% · séance 41% (64/159) · gap 6% · délai 12.7min · rebond 64% (40/64) (MFE +1.65%)
   - −5.0% : fill 30min 16% · séance 28% (47/159) · gap 4% · délai 19.4min · rebond 74% (34/47) (MFE +1.68%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.88% (p90 −2.28%) → stop au-delà de −1.71% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.03% (p90 −2.73%) → stop au-delà de −2.15% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.08% (p90 −2.64%) → stop au-delà de −2.23% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=957 jambes) : jambe baissière méd −1.14% (p90 −2.74%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (76 séances) :
      · −1.0% : fill 100% (75/76) · rebond 51% (38/75)
      · −2.0% : fill 90% (68/76) · rebond 60% (40/68)
      · −3.0% : fill 78% (60/76) · rebond 59% (36/60)
      · −4.0% : fill 66% (50/76) · rebond 67% (33/50)
      · −5.0% : fill 47% (38/76) · rebond 76% (28/38)
   - **flat** (16 séances) :
      · −1.0% : fill 92% (15/16) · rebond 89% (11/15)
      · −2.0% : fill 65% (11/16) · rebond 48% (7/11)
      · −3.0% : fill 36% (6/16) · rebond 57% (4/6)
      · −4.0% : fill 23% (5/16) · rebond 13% (2/5)
      · −5.0% : fill 18% (4/16) · rebond 16% (2/4)
   - **gap-up** (67 séances) :
      · −1.0% : fill 36% (29/67) · rebond 70% (20/29)
      · −2.0% : fill 22% (20/67) · rebond 71% (15/20)
      · −3.0% : fill 15% (11/67) · rebond 56% (7/11)
      · −4.0% : fill 13% (9/67) · rebond 66% (5/9)
      · −5.0% : fill 6% (5/67) · rebond 93% (4/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 56% si les 15 1res min sont vertes (79 cas) · 40% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:13** → P(séance verte=clôture>ouverture) 76% si début vert vs 18% si rouge (base 48% · écart 58 pts) ; prédictivité sature ensuite (plafond brut 136min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=83) : tient le vert **76%** · continue >prix actuel 54% ; creux résiduel méd -1.52% (q20 -2.81%) → **SL/trailing à −2.81%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.82% / q75 +2.99% → **scale +1.82% / runner +2.99%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **18%** (continue à baisser 58%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.03%** (au-delà de la MAE q10 -5.03%), cible rebond +1.61% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.49% .. +3.75%] · haut q95 +4.02% · bas q05 -3.96%
   - 60min (n=160) : retour [-4.83% .. +3.51%] · haut q95 +5.22% · bas q05 -5.44%
   - 2h (n=160) : retour [-4.58% .. +5.47%] · haut q95 +5.8% · bas q05 -5.45%
   - 4h (n=160) : retour [-6.22% .. +6.72%] · haut q95 +8.52% · bas q05 -7.09%
   - 6h (n=160) : retour [-5.93% .. +5.8%] · haut q95 +8.52% · bas q05 -8.02%
   - session (n=160) : retour [-5.5% .. +5.89%] · haut q95 +8.52% · bas q05 -8.02%


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

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 45.5  _(neutre)_
- **ADX** : 10.8  _(pas de tendance nette)_
- **MACD** : hist 1.161  _(pas de croisement recent)_
- **BB** : %B 0.45 · largeur 10.9%
- **ATR** : 5.57 (2.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.016  _(neutre)_
- **Vol ratio** : 0.79  _(volume normal)_
- **Choppiness** : 59.3  _(transition)_
- **MA** : MA20 96.59 · MA50 103.99 · MA200 150.99  _(prix < MA20)_
- **Dist MA** : MA20 -0.5% · MA50 -7.6% · MA200 -36.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90442 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
